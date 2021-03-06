---
title: 'MFC: ドキュメントとビューを用いないデータベース クラスの使用'
ms.date: 11/04/2016
helpviewer_keywords:
- ODBC applications [C++], without views
- documents [C++], applications without
- ODBC applications [C++]
- document/view architecture [C++], in databases
- files [C++], MFC
- database classes [C++], MFC
- CRecordView class, using in database applications
- database applications [C++], without views
- database applications [C++], application wizard options
- application wizards [C++], creating database applications
- ODBC [C++], file support in database applications
- ODBC applications [C++], without documents
- database applications [C++], without documents
- user interface [C++], drawing information
ms.assetid: 15bf52d4-91cf-4b1d-8b37-87c3ae70123a
ms.openlocfilehash: 558917f1a1485f1a886356b3c272842579f6b03e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50602216"
---
# <a name="mfc-using-database-classes-without-documents-and-views"></a>MFC: ドキュメントとビューを用いないデータベース クラスの使用

場合があります、データベース アプリケーションのフレームワークのドキュメント/ビュー アーキテクチャを使用しない場合があります。 このトピックでは、次の内容について説明します。

- [ドキュメントを使用する必要がない場合](#_core_when_you_don.92.t_need_documents)ドキュメントのシリアル化などです。

- [アプリケーション ウィザードのオプション](#_core_appwizard_options_for_documents_and_views)シリアル化したりせずにアプリケーションをサポートするドキュメントに関連する**ファイル**などのメニュー コマンド**新規**、**オープン**、**保存**、および**として保存**します。

- [最小限のドキュメントを使用するアプリケーションを操作する方法](#_core_applications_with_minimal_documents)します。

- [ドキュメントやビューのないアプリケーションを構成する方法](#_core_applications_with_no_document)します。

##  <a name="_core_when_you_don.92.t_need_documents"></a> ドキュメントを必要するときに

一部のアプリケーションでは、ドキュメントの異なる概念があります。 これらのアプリケーション通常、ほとんどすべてのファイルから読み込むストレージを使用してメモリを**ファイルを開く**コマンド。 更新されたファイルに書き込みますで一度にすべての記憶域、**ファイルの保存の**または**名前を付けて保存**コマンド。 データ ファイルは、どのようなユーザーに表示されます。

ただし、アプリケーションのいくつかのカテゴリには、ドキュメントは不要です。 データベース アプリケーションは、トランザクションの観点から動作します。 アプリケーションでは、データベースからレコードを選択し、多くの場合、1 つずつと、ユーザーに提示します。 どのようなユーザーに表示されるは、通常、メモリ内で 1 つだけ可能性のある 1 つ現在レコードです。

アプリケーションがデータを格納するためのドキュメントが必要としない場合は、フレームワークのドキュメント/ビュー アーキテクチャの一部またはすべてを省略することができます。 省略する量は、希望の方法によって異なります。 できます。

- 場所としては、データ ソースへの接続を保存し、シリアル化などの通常のドキュメントの機能を提供する最小限のドキュメントを使用します。 これは、機能は、データのいくつかのビューを目的というように、一度に更新すること、すべてのビューを同期する必要すると便利です。

- 描画する、直接ビューを使用するのではなく、フレーム ウィンドウを使用します。 この場合は、ドキュメントを除外し、フレーム ウィンドウ オブジェクトのすべてのデータまたはデータ接続を格納します。

##  <a name="_core_appwizard_options_for_documents_and_views"></a> ドキュメントとビューのアプリケーション ウィザードのオプション

MFC アプリケーション ウィザードのいくつかのオプションが**データベース サポート を選択**、次の表にリストされています。 MFC アプリケーション ウィザードを使用してアプリケーションを作成する場合、これらすべてのオプションはドキュメントとビューを使用してアプリケーションを生成します。 いくつかのオプションは、ドキュメントと不要なドキュメント機能を省略するビューを提供します。 詳細については、次を参照してください。[データベースのサポート、MFC アプリケーション ウィザード](../mfc/reference/database-support-mfc-application-wizard.md)します。

|オプション|表示|ドキュメント|
|------------|----------|--------------|
|**None**|`CView`の派生クラスです。|データベースのサポートにはありません。 これは、既定の設定です。<br /><br /> 選択した場合、**ドキュメント/ビュー アーキテクチャ サポート**オプションを[アプリケーションの種類、MFC アプリケーション ウィザード](../mfc/reference/application-type-mfc-application-wizard.md) ページで、シリアル化を含む完全なドキュメントのサポートを取得し、**新規**、**オープン**、**保存**、および**名前を付けて保存**コマンドを**ファイル**メニュー。 参照してください[ドキュメントを持たないアプリケーション](#_core_applications_with_no_document)します。|
|**ヘッダー ファイルのみ**|`CView`の派生クラスです。|アプリケーションの基本的なレベルのデータベースのサポートを提供します。<br /><br /> Afxdb.h が含まれています。 リンクのライブラリを追加しますが、データベース固有のクラスを作成できません。 レコード セットを後で作成でき、それらを検証し、レコードの更新に使用できます。|
|**ファイル サポートのないデータベース ビュー**|を派生 `CRecordView`|ドキュメントのサポートがないシリアル化のサポートを提供します。 ドキュメントはレコード セットを格納して、複数のビューを調整シリアル化をサポートしていませんまたは**新規**、**オープン**、**保存**、および**名前を付けて保存**コマンド。 参照してください[最小限ドキュメント アプリケーション](#_core_applications_with_minimal_documents)します。 データベース ビューを含める場合は、データのソースを指定する必要があります。<br /><br /> データベースのヘッダー ファイル、ライブラリのリンク、レコード ビュー、およびレコード セットが含まれています。 (アプリケーションでのみ使用できます、**ドキュメント/ビュー アーキテクチャ サポート**オプションを選択、[アプリケーションの種類、MFC アプリケーション ウィザード](../mfc/reference/application-type-mfc-application-wizard.md)ページです)。|
|**ファイルのサポートのあるデータベース ビュー**|を派生 `CRecordView`|シリアル化を含む、完全なドキュメントのサポートを提供し、ドキュメントに関連する**ファイル**メニュー コマンド。 ファイルあたりの単位とその必要はありませんシリアル化ではなく、データベース アプリケーションは通常、レコード単位で動作します。 ただし、シリアル化のための特別な用途があります。 参照してください[最小限ドキュメント アプリケーション](#_core_applications_with_minimal_documents)します。 データベース ビューを含める場合は、データのソースを指定する必要があります。<br /><br /> データベースのヘッダー ファイル、ライブラリのリンク、レコード ビュー、およびレコード セットが含まれています。 (アプリケーションでのみ使用できます、**ドキュメント/ビュー アーキテクチャ サポート**オプションを選択、[アプリケーションの種類、MFC アプリケーション ウィザード](../mfc/reference/application-type-mfc-application-wizard.md)ページです)。|

シリアル化とシリアル化のための代替の使用に代わる方法の詳細については、次を参照してください。[シリアル化: シリアル化とします。データベースの入力/出力](../mfc/serialization-serialization-vs-database-input-output.md)します。

##  <a name="_core_applications_with_minimal_documents"></a> 最小限のドキュメントでのアプリケーション

MFC アプリケーション ウィザードでは、フォーム ベースのデータ アクセス アプリケーションをサポートする 2 つのオプションがあります。 各オプションの作成、 `CRecordView`-派生ビュー クラスおよびドキュメント。 ドキュメントからのままに異なります。

###  <a name="_core_a_document_without_file_support"></a> ファイルをサポートしないドキュメント

アプリケーション ウィザードのデータベース オプションを選択します。**データベース ファイルをサポートしないビュー**場合、ドキュメントのシリアル化する必要はありません。 ドキュメントには、次にさまざまな目的があります。

- 格納する便利な場所は、`CRecordset`オブジェクト。

   この使用量は通常のドキュメントの概念に対応して: ドキュメントのデータを格納する (または、この場合は、一連のレコード)、ビューは、ドキュメントのビューとします。

- このアプリケーションでは、(複数レコード ビュー) などの複数のビューでは、ドキュメントは、ビューの調整をサポートします。

   複数のビューが、同じデータを表示する場合は使用できます、`CDocument::UpdateAllViews`メンバー関数は、任意のビューには、データが変更されたときに、すべてのビューへの更新プログラムを調整します。

通常、このオプションを使用するには、単純なフォーム ベース アプリケーション用。 アプリケーション ウィザードは、自動的にこのようなアプリケーションの使いやすい構造をサポートします。

###  <a name="_core_a_document_with_file_support"></a> ファイルをサポート ドキュメント

アプリケーション ウィザードのデータベース オプションを選択します。**ファイルのサポートのあるデータベース ビュー**ドキュメントに関連する用途がある場合**ファイル**メニュー コマンドやドキュメントのシリアル化します。 プログラムの部分のデータ アクセスできるドキュメントを使用する、同じ方法で」の説明に従って[ファイルをサポートしないドキュメント](#_core_a_document_without_file_support)します。 たとえば、ドキュメントのシリアル化の機能を使用するユーザーの設定やその他の有用な情報を格納するシリアル化されたユーザー プロファイルのドキュメントを読み書きします。 詳細については、次を参照してください。[シリアル化: シリアル化とします。データベースの入力/出力](../mfc/serialization-serialization-vs-database-input-output.md)します。

アプリケーション ウィザードが、このオプションをサポートしますが、ドキュメントをシリアル化するコードを記述する必要があります。 ドキュメント データ メンバーのシリアル化された情報を格納します。

##  <a name="_core_applications_with_no_document"></a> ドキュメントを持たないアプリケーション

ドキュメントまたはビューを使用しないアプリケーションを作成したい場合があります。 データを格納するドキュメントを使わない場合 (など、`CRecordset`オブジェクト)、フレーム ウィンドウ クラスに、アプリケーション クラス。 その他の要件は、アプリケーションがユーザー インターフェイスを表示するかどうかによって異なります。

###  <a name="_core_database_support_with_a_user_interface"></a> ユーザー インターフェイスを持つデータベースのサポート

(たとえば、コンソール コマンド ライン インターフェイス以外の) ユーザー インターフェイスがあれば、ビューではなく、フレーム ウィンドウのクライアント領域に直接アプリケーションを描画します。 このようなアプリケーションが使用しない`CRecordView`、 `CFormView`、または`CDialog`通常は、メイン ユーザー インターフェイスを使用して`CDialog`通常ダイアログ。

###  <a name="_core_writing_applications_without_documents"></a> ドキュメントを使用しないアプリケーションの作成

アプリケーション ウィザードがドキュメントを使用しないアプリケーションの作成をサポートしていないため、記述する必要あります独自`CWinApp`-クラスを派生し、必要な場合も作成、`CFrameWnd`または`CMDIFrameWnd`クラス。 オーバーライド`CWinApp::InitInstance`としてアプリケーション オブジェクトを宣言します。

```cpp
CYourNameApp theApp;
```

フレームワークでは、メッセージ マップ機構と他の多くの機能も提供します。

###  <a name="_core_database_support_separate_from_the_user_interface"></a> データベース サポートは別のユーザー インターフェイス

一部のアプリケーションでは、ユーザー インターフェイスのない、または最低限の 1 つだけ必要があります。 たとえば、作成するいるとします。

- その他のアプリケーション (クライアント) が、アプリケーションとデータ ソース間でデータの特別な処理の呼び出しを中間のデータ アクセス オブジェクト。

- 1 つのデータベース形式から別または計算を行うし、バッチ更新を実行する 1 つにデータを移動するアプリケーションなど、ユーザーの介入なしにデータを処理するアプリケーション。

ドキュメントを所有していないため、`CRecordset`オブジェクト内の埋め込みデータ メンバーとして保存する可能性があります、 `CWinApp`-アプリケーションのクラスを派生します。 選択肢は次のとおりです。

- 永続的なを保持しない`CRecordset`すべてのオブジェクトします。 レコード セット クラスのコンス トラクターに NULL を渡すことができます。 その場合は、フレームワークによって一時テーブルが作成`CDatabase`オブジェクトで、レコード セットの情報を使用して`GetDefaultConnect`メンバー関数。 これは、最も可能性の高い別の方法です。

- 作成、`CRecordset`オブジェクトのグローバル変数。 この変数が動的に作成するレコード セット オブジェクトへのポインターにする必要があります、`CWinApp::InitInstance`をオーバーライドします。 これは、フレームワークが初期化される前に、オブジェクトを作成する際に回避できます。

- レコード セット オブジェクトを使用して、ドキュメントやビューのコンテキスト内と同様です。 メンバーに、アプリケーションまたはフレーム ウィンドウ オブジェクトの関数に対応するレコード セットを作成します。

## <a name="see-also"></a>関連項目

[MFC データベース クラス](../data/mfc-database-classes-odbc-and-dao.md)