---
title: '方法: 追加、編集、またはコントロールを削除'
ms.date: 02/15/2019
f1_keywords:
- vc.editors.dialog.dialog
- vc.controls.activex
- vc.editors.dialog.insertActiveXControls
helpviewer_keywords:
- Dialog Editor [C++], creating controls
- dialog boxes [C++], adding controls to
- Toolbox [C++], Dialog Editor tab
- controls [C++], types
- syslink controls in dialog boxes
- custom controls [C++], dialog boxes
- controls [C++], standard
- Dialog Editor [C++], creating controls
- controls [C++], adding to dialog boxes
- controls [C++], adding multiple
- dialog box controls [C++], size
- controls [C++], sizing
- dialog boxes [C++], adding ActiveX controls
- ActiveX controls [C++], adding to dialog boxes
- Insert ActiveX Control dialog box [C++]
- controls [C++], editing properties
- ActiveX controls [C++], properties
- controls [C++], undoing changes
- controls [C++], editing properties
- dialog box controls [C++], editing properties
- dialog box controls [C++], deleting
- controls [C++], deleting
- Dialog Editor [C++], default control events
- controls [C++], default control events
- events [C++], controls
- dialog box controls [C++], events
- member variables, defining for controls
- variables, dialog box control member variables
- controls [C++], member variables
- Dialog Editor [C++], defining member variables for controls
- controls [C++], troubleshooting
- Dialog Editor [C++], troubleshooting
- dialog boxes [C++], troubleshooting
- InitCommonControls
- RichEdit 1.0 control
- rich edit controls [C++], RichEdit 1.0
ms.assetid: 73cef03f-5c8c-456a-87d1-1458dff185cf
ms.openlocfilehash: 87acb2c8356508358f68c1ae4c8d5deaa94ecd9a
ms.sourcegitcommit: 24592ba0a38c7c996ffd3d55fe1024231a59ccc2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2019
ms.locfileid: "56336567"
---
# <a name="how-to-add-edit-or-delete-controls"></a>方法: 追加、編集、またはコントロールを削除

使用して、**ダイアログ**エディター、追加できますが、サイズを変更、編集、およびダイアログ ボックスのコントロールを削除します。 をその ID などのコントロールのプロパティを編集することもできるかどうか、最初に表示される実行時にします。

**ダイアログ エディター**タブに表示されます、[ツールボックス ウィンドウ](/visualstudio/ide/reference/toolbox)作業するとき、**ダイアログ**エディター。 カスタマイズすることも、**ツールボックス**ウィンドウを簡単に使用します。 詳細については、次を参照してください。[ツールボックスを使用して](/visualstudio/ide/using-the-toolbox)と[表示または非表示のツールボックス ウィンドウ](showing-or-hiding-the-dialog-editor-toolbar.md)します。

> [!TIP]
> 使用しているときに、**ダイアログ**エディター、多くの場合はボタンを選択するマウスの右頻繁に使用されるコマンドのショートカット メニューを表示します。

## <a name="add-controls"></a>コントロールを追加します。

新しいダイアログ ボックスにコントロールを追加するからコントロールをドラッグ、**ツールボックス** ダイアログ ボックスを作成します。 次いでコントロールの移動、またはサイズと形状の変更ができます。

ダイアログ ボックスにカスタム コントロールを追加するには選択して、**カスタム コントロール**アイコン、**ツールボックス**ダイアログ ボックスにドラッグするとします。 追加する、 **Syslink**を制御し、カスタム コントロールを追加、変更、コントロールの**クラス**プロパティを**Syslink**します。 この操作は、プロパティが更新され、表示により、 **Syslink**プロパティを制御します。 MFC ラッパー クラスについては、次を参照してください。 [CLinkCtrl](../mfc/reference/clinkctrl-class.md)します。

### <a name="to-add-a-control"></a>コントロールを追加するには

1. ダイアログ ボックスのタブ付きウィンドウがエディター フレーム内の現在のドキュメントであることを確認します。 ダイアログ ボックスが現在のドキュメントでない場合は表示されません、**ダイアログ エディターのタブ**で、**ツールボックス**します。

1. **ダイアログ エディター**のタブ、**ツールボックス**ウィンドウで、し、コントロールを選択します。

   - コントロールを配置する場所 ダイアログ ボックスを選択します。 選択したコントロールが表示されます。

   - ドラッグ アンド ドロップのコントロール、**ツールボックス**ウィンドウ、ダイアログ ボックス上の場所にします。

   - コントロールをダブルクリック、**ツールボックス**ウィンドウ (ダイアログ ボックスに表示)、したい場所に、コントロールの位置を指定します。

### <a name="to-add-multiple-controls"></a>複数のコントロールを追加するには

1. 押しながら、 **Ctrl**キーでコントロールを選び、**ツールボックス**ウィンドウ。

1. リリース、 **Ctrl**キーを何度でも、特定のコントロールを追加すると、ダイアログ ボックスを選択します。

1. キーを押して**Esc**コントロールの配置を停止します。

### <a name="to-size-a-control-while-you-add-it"></a>追加するコントロールのサイズ

1. コントロールを選び、**ツールボックス**ウィンドウ。

1. ダイアログ ボックスで、新しいコントロールの左上隅となる (これに十字が表示されます)、カーソルを置きます。

1. 選択し、ダイアログ ボックスで、コントロールの左上隅に固定するマウス ボタンを押したまま、目的のサイズになるまで、右、下にカーソルをドラッグします。

   > [!NOTE]
   > 実際に描画するコントロールの四隅のいずれかを固定できます。 この手順では、例として、左上隅にあるを使用します。

1. マウスのボタンを離します。 指定したサイズでダイアログ ボックスにコントロールが配置されます。

   > [!TIP]
   > コントロールのサイズを変更するには、コントロールの境界線にサイズ変更ハンドルを移動することによって、ダイアログ ボックスの上にドロップするとします。 詳細については、次を参照してください。[個々 のコントロールをサイズ変更](../windows/sizing-individual-controls.md)します。

## <a name="edit-controls"></a>コントロールを編集します。

### <a name="to-edit-the-properties-of-a-control-or-controls"></a>コントロールまたはコントロールのプロパティを編集するには

1. ダイアログ ボックスで、変更するコントロールを選択します。

   > [!NOTE]
   > 複数のコントロールを選択した場合は、選択したコントロールの共通プロパティのみを編集できます。

1. [プロパティ ウィンドウ](/visualstudio/ide/reference/properties-window)コントロールのプロパティを変更します。

   > [!NOTE]
   > 設定すると、**ビットマップ**ボタン、オプション ボタン、またはチェック ボックス コントロールと同じプロパティを**True**BS_BITMAP の実装は、コントロールのスタイル。 詳細については、次を参照してください。[ボタンのスタイル](../mfc/reference/styles-used-by-mfc.md#button-styles)します。 コントロールとビットマップの関連付けの例は、次を参照してください。 [CButton::SetBitmap](../mfc/reference/cbutton-class.md#setbitmap)します。 は、ビットマップは、コントロールに表示されません、**ダイアログ**リソース エディター。

### <a name="to-undo-changes-to-the-properties-of-a-control"></a>コントロールのプロパティの変更を元に戻す

1. コントロールにフォーカスがあるかどうかを確認、**ダイアログ**エディター。

1. 選択**を元に戻す**から、**編集**メニュー (コントロールにフォーカスがない場合、**を元に戻す**コマンドは使用できません)。

### <a name="to-define-a-member-variable-for-a-non-button-dialog-box-control"></a>ボタン以外のダイアログ ボックス コントロールのメンバー変数を定義するには

ボタン以外のダイアログ ボックス コントロールのメンバー変数を定義するには、次の手順を使用できます。

> [!NOTE]
> このプロセスは、MFC プロジェクト内のダイアログ コントロールにのみ適用されます。 ATL プロジェクトで使用する必要があります、**新しい Windows メッセージおよびイベント ハンドラー**  ダイアログ ボックス。 詳細については、次を参照してください[メッセージの種類は、ユーザー インターフェイス オブジェクトに関連付けられた](../mfc/reference/message-types-associated-with-user-interface-objects.md)、[メッセージ ハンドラーの編集](../mfc/reference/editing-a-message-handler.md)、および[リフレクションメッセージ用のメッセージハンドラーを定義する](../mfc/reference/defining-a-message-handler-for-a-reflected-message.md)。

1. [ダイアログ エディター](../windows/dialog-editor.md)コントロールを選択します。

1. キーを押しながら、 **Ctrl**キーをダイアログ ボックス コントロールをダブルクリックします。

   [メンバー変数の追加ウィザード](../ide/add-member-variable-wizard.md)が表示されます。

1. 適切な情報を入力、**メンバー変数の追加**ウィザード。 詳細については、次を参照してください。[ダイアログ データ エクス チェンジ](../mfc/dialog-data-exchange.md)します。

1. 選択**OK**に戻る、**ダイアログ**エディター。

   > [!TIP]
   > ダイアログ ボックス コントロールから既存のハンドラーにジャンプするには、コントロールをダブルクリックします。

使用することも、**メンバー変数** タブで、 [MFC クラス ウィザード](../mfc/reference/mfc-class-wizard.md)に指定したクラスの新しいメンバー変数を追加し、既に定義されているメンバー変数を表示します。

## <a name="delete-controls"></a>コントロールを削除します。

コントロールを選択 ダイアログ ボックスで、キーを押します、**削除**キー、またはに移動、**編集**メニュー選択し、**削除**します。

## <a name="other-issues"></a>その他の問題

### <a name="troubleshooting"></a>トラブルシューティング

ダイアログ ボックスに、一般的なコントロールまたはリッチ エディット コントロールを追加すると、ダイアログ ボックスのテストまたはダイアログ自体は表示されないときに表示されません。

問題の例。

1. Windows アプリケーション (コンソール アプリケーションではなく) を作成するためにアプリケーション設定を変更する、Win32 プロジェクトを作成します。

1. [リソース ビュー](../windows/resource-view-window.md)、.rc ファイルをダブルクリックします。

1. ダイアログ オプションで、をダブルクリック、**について**ボックス。

1. 追加、 **IP アドレス コントロール** ダイアログ ボックス。

1. 保存と**すべてリビルド**します。

1. プログラムを実行します。

1. ダイアログ ボックスの**ヘルプ**メニューの 、**について**コマンドし、確認ダイアログ ボックスは表示されません。

現時点では、**ダイアログ**エディターは、自動的に、リッチ エディット コントロールをダイアログ ボックスにドラッグ アンド ドロップ、次の一般的なコントロールまたはときに、プロジェクトにコードを追加しません。 Visual Studio はエラーまたは警告がこの問題が発生します。 を解決するには、コントロールのコードを手動で追加します。

||||
|-|-|-|
|スライダー コントロール|ツリー コントロール|Date Time Picker|
|スピン コントロール|タブ コントロール|月間予定表|
|プログレス コントロール|アニメーション コントロール|IP アドレスの管理|
|ホット キー|リッチ エディット コントロール|拡張コンボ ボックス|
|リスト コントロール|リッチ エディット 2.0 コントロール|カスタム コントロール|

コモン コントロール ダイアログ ボックスを使用するにを呼び出す必要があります[InitCommonControlsEx](/windows/desktop/api/commctrl/nf-commctrl-initcommoncontrolsex)または`AFXInitCommonControls` ダイアログ ボックスを作成する前にします。

リッチ エディット コントロールを使用して呼び出す必要がある`LoadLibrary`します。 詳細については、次を参照してください。[リッチのエディット コントロールについて](/windows/desktop/Controls/about-rich-edit-controls)Windows sdk と[リッチ エディット コントロールの概要](../mfc/overview-of-the-rich-edit-control.md)します。

> [!NOTE]
> リッチ エディット コントロールを MFC を使用するには、まず[AfxInitRichEdit2](../mfc/reference/application-information-and-management.md#afxinitrichedit2)リッチ エディット 2.0 コントロール (RICHED20 を読み込めません。DLL)、または呼び出す[AfxInitRichEdit](../mfc/reference/application-information-and-management.md#afxinitrichedit)古い RichEdit 1.0 コントロール (RICHED32 を読み込めません。DLL) です。
>
> 現在を使用することが[CRichEditCtrl](../mfc/reference/cricheditctrl-class.md)古い RichEdit 1.0 コントロールでは、クラスが`CRichEditCtrl`はリッチ エディット 2.0 コントロールをサポートするためにのみ設計されています。 リッチ エディット 1.0 とリッチ エディット 2.0 は似ていますが、ため、ほとんどのメソッドは機能します。 ただしの 1.0 と 2.0 のコントロールをいくつかのメソッドが正常に動作しない可能性がありますまたはまったく動作しないようにいくつかの違いに注意してください。

### <a name="activex-controls"></a>ActiveX コントロール

Visual Studio では、ActiveX コントロールをダイアログ ボックスに挿入することができます。 詳細については、次を参照してください。 [MFC ActiveX コントロール](../mfc/mfc-activex-controls.md)と[ActiveX コントロール コンテナー](../mfc/activex-control-containers.md)します。

ショートカット メニューを使用することができます、**ダイアログ**エディターにすばやく追加するには、ActiveX コントロールのダイアログ ボックスが登録されているし、ActiveX コントロールを追加することができます、**ツールボックス**すばやくアクセスできます。

**ActiveX コントロールの挿入** ダイアログ ボックスでは、使用中に、ダイアログ ボックスに ActiveX コントロールを挿入することができます、[ダイアログ エディター](../windows/dialog-editor.md)します。 このダイアログ ボックスには、次のプロパティが含まれています。

|プロパティ|説明|
|---|---|
|**ActiveX コントロール**|Active X コントロールの一覧が表示されます。 このダイアログ ボックスからコントロールを挿入すると、ラッパー クラスを生成しません。 ラッパー クラスを必要がある場合を使用して、[クラス ビュー](/visualstudio/ide/viewing-the-structure-of-code)を作成する (詳細については、次を参照してください。[クラスの追加](../ide/adding-a-class-visual-cpp.md))。 このダイアログ ボックスで、Active X コントロールが表示されない場合は、ベンダーの指示に従ってコントロールをインストールしてみてください。|
|**パス**|ActiveX コントロールが掲載されているファイルを表示します。|

> [!CAUTION]
> システム上の ActiveX コントロールの中には、配布が法的に許可されていないものもあります。 コントロールをインストールしたソフトウェアのライセンス契約を参照するか、ソフトウェア会社に問い合わせてください。

#### <a name="to-add-an-activex-control"></a>ActiveX コントロールを追加するには

1. 開いているダイアログ ボックスのボックスに、**ダイアログ**エディター。

1. [ショートカット] メニューとダイアログ ボックスの本文内を右クリックして**ActiveX コントロールの挿入**します。

   **ActiveX コントロールの挿入**システム上のすべての ActiveX コントロールを示すダイアログ ボックスが表示されます。 ダイアログ ボックスの下部には、ActiveX コントロール ファイルへのパスが表示されます。

1. ダイアログ ボックスに追加するコントロールを選択**OK**します。

   コントロールがダイアログ ボックスに表示されます。このダイアログ ボックスで、他のコントロールでするのと同じように、コントロールの編集またはそのハンドラーの作成を行います。

> [!NOTE]
> ActiveX コントロールを追加することができます、**ツールボックス**ウィンドウを簡単にアクセスします。

#### <a name="to-edit-properties-for-an-activex-control"></a>ActiveX コントロールのプロパティを編集するには

独立系ベンダーによって提供される ActiveX コントロールは、独自のプロパティと特性が搭載可能性があります。 ActiveX コントロールのプロパティが表示されます、**プロパティ**ウィンドウ。 ActiveX コントロールの作成者によって作成されたすべてのプロパティ ページを表示することも、**プロパティ ページ** ダイアログ ボックス (表示する、**プロパティ ページ**特定の ActiveX コントロールをクリックして、 **プロパティ ページ**ボタン、[プロパティ ウィンドウ](/visualstudio/ide/reference/properties-window))。

ActiveX コントロールの一部として付属するプロパティ シートによって、ActiveX コントロールのプロパティ ページには、さまざまなタブが表示されます。

> [!NOTE]
> 次の手順では、プロパティ ページを使用して ActiveX コントロールを編集するには適用されます。 参照および新しい ActiveX プロパティを編集することができますも**プロパティ**ウィンドウ。

1. 選択、 **ActiveX**コントロール。

1. **ビュー**メニューの **プロパティ ページ**プロパティを表示します。

1. プロパティ ページで、必要に応じて変更を加えます。

## <a name="requirements"></a>必要条件

Win32

## <a name="see-also"></a>関連項目

[ダイアログ エディター](../windows/dialog-editor.md)<br/>
[ダイアログ ボックスのコントロール](controls-in-dialog-boxes.md)<br/>
[リソース ファイル](../windows/resource-files-visual-studio.md)<br/>

<!-- excluded links
[Mapping Messages to Functions](../mfc/reference/mapping-messages-to-functions.md)<br/>
[Adding Functionality with Code Wizards](../ide/adding-functionality-with-code-wizards-cpp.md)<br/>
[Adding a Class](../ide/adding-a-class-visual-cpp.md)<br/>
[Adding a Member Function](../ide/adding-a-member-function-visual-cpp.md)<br/>
[Adding a Member Variable](../ide/adding-a-member-variable-visual-cpp.md)<br/>
[Overriding a Virtual Function](../ide/overriding-a-virtual-function-visual-cpp.md)<br/>
[MFC Message Handler](../mfc/reference/adding-an-mfc-message-handler.md)
[Declaring a Variable Based on Your New Control Class](../mfc/reference/declaring-a-variable-based-on-your-new-control-class.md)<br/>
-->