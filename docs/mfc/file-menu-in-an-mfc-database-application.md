---
title: MFC データベース アプリケーションの [ファイル] メニュー
ms.date: 11/04/2016
helpviewer_keywords:
- File menu
- database applications [MFC], File menu commands
ms.assetid: 92dafb75-c1b3-4860-80a0-87a83bfc36f2
ms.openlocfilehash: ce56dd5f04312ae9e7b7f747ce81cb704f3d085d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50629204"
---
# <a name="file-menu-in-an-mfc-database-application"></a>MFC データベース アプリケーションの [ファイル] メニュー

[ファイル] メニューにどのようにする必要がある、オープン、クローズの解釈、保存、およびとして保存がコマンド MFC データベース アプリケーションを作成してシリアル化を使用しない場合この質問のスタイルのガイドラインはありませんが、ここでは、いくつかの提案。

- 開いているファイル メニューのコマンドを完全に排除します。

- 「開いているデータベース」として開く コマンドを解釈し、ユーザー、アプリケーションが認識するデータ ソースの一覧を表示します。

- として、おそらく、「プロファイルを開きます」開いているコマンドを解釈します。 「ユーザー プロファイル」については、彼をなど、ユーザーの基本設定などを含むシリアル化されたドキュメントを格納するファイルを使用してがシリアル化されたファイルを開くか、または (必要に応じて、パスワードを除く)、ログイン ID と、データ ソースと最もオープンを保持します。最近使用したとします。

MFC アプリケーション ウィザードでは、ドキュメントに関連するファイル メニュー コマンドが存在しないと、アプリケーションの作成をサポートします。 選択、**データベース ファイルをサポートしないビュー**オプションを**データベース サポート**ページ。

特別な方法でファイルのメニュー コマンドを解釈するほとんどの場合で 1 つまたは複数のコマンド ハンドラーをオーバーライドする必要があります、 `CWinApp`-クラスを派生します。 たとえば、完全にオーバーライドする`OnFileOpen`(実装する、`ID_FILE_OPEN`コマンド) を意味する"データベースを開く:"

- 基底クラスのバージョンを呼び出さないでください`OnFileOpen`コマンドのフレームワークの既定の実装を完全に置換するため、します。

- データ ソースを一覧表示するダイアログ ボックスを表示する代わりにハンドラーを使用します。 このようなダイアログ ボックスを表示するには呼び出すことによって`CDatabase::OpenEx`または`CDatabase::Open`パラメーターと共に**NULL**。 ユーザーのコンピューターにすべての利用可能なデータ ソースを表示する ODBC ダイアログ ボックスが開きます。

- 保存先を削除するおそらく必要ありますので、データベース アプリケーションは通常、ドキュメント全体を保存しない、シリアル化されたドキュメントを使用して、プロファイル情報を格納する場合を除き、実装として保存します。 それ以外の場合、たとえば、「トランザクションをコミットします」[保存] コマンドを実装する可能性があります。 参照してください[テクニカル ノート 22:](../mfc/tn022-standard-commands-implementation.md)詳細については、これらのコマンドをオーバーライドします。

## <a name="see-also"></a>関連項目

[シリアル化: シリアル化とデータベースの入力/出力](../mfc/serialization-serialization-vs-database-input-output.md)

