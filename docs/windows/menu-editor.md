---
title: メニュー エディター (C++)
ms.date: 02/15/2019
f1_keywords:
- vc.editors.menu.F1
- vc.editors.menu
helpviewer_keywords:
- resource editors [C++], Menu editor
- editors, menus
- Menu editor
- menus [C++], Menu editor
- mnemonics [C++], associating menu items
- menus [C++], associating commands with mnemonic keys
- menus [C++], creating
- menus [C++], adding items
- commands [C++], adding to menus
- menu items, adding to menus
- submenus
- submenus [C++], creating
- menus [C++], creating
- context menus [C++], Menu Editor
- pop-up menus [C++], creating
- menus [C++], pop-up
- menus [C++], creating
- shortcut menus [C++], creating
- pop-up menus [C++], displaying
- pop-up menus [C++], connecting to applications
- context menus [C++], connecting to applications
- shortcut menus [C++], connecting to applications
- pop-up menus
- menu commands [C++], selecting
- menus [C++], selecting
- commands [C++], menu commands
- commands [C++], copying on menus
- menu items, moving
- commands [C++], moving on menus
- menu items, copying
- menu items, deleting
- commands [C++], deleting from menus
- menus [C++], deleting
ms.assetid: 421fb215-6e12-4ec9-a3af-82d77f87bfa6
ms.openlocfilehash: 8e97fb88a8860ab0831f62bf2413b1f8f7174c7b
ms.sourcegitcommit: 24592ba0a38c7c996ffd3d55fe1024231a59ccc2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/18/2019
ms.locfileid: "56336684"
---
# <a name="menu-editor-c"></a>メニュー エディター (C++)

メニューを使用すると、論理的かつ見つけやすい方法でコマンドを配置できます。 **メニュー**エディターを作成して、完成したアプリケーションで 1 つによく似たメニュー バーを直接操作してメニューを編集します。

> [!TIP]
> 使用しているときに、**メニュー**多くの場合、エディター頻繁に使用されるコマンドのポップアップ メニューを表示する、マウスの右ボタンをクリックすることができます。 使用できるコマンドは、ポインターの位置によって異なります。

> [!NOTE]
> Microsoft Foundation Class ライブラリ (MFC) プログラムおよび ATL プログラムでは、使用することができます**コード ウィザード**をコードにメニュー コマンドをフックします。 詳しくは「 [イベントの追加](../ide/adding-an-event-visual-cpp.md)」をご覧ください。

## <a name="how-to"></a>方法

> [!NOTE]
> **リソース ウィンドウ**Express エディションでは使用できません。

**メニュー**エディターを使用できます。

### <a name="to-create-a-standard-menu"></a>標準メニューを作成するには

1. **ビュー**メニューの **リソース ビュー**を右クリックし、**メニュー**見出しと選択**リソースの追加**します。 **[メニュー]** をクリックします。

1. メニュー バーで、"ここへ入力" と表示されている四角形の **[新しい項目]** ボックスを選びます。

   ![メニュー エディターの新しい項目ボックス](../windows/media/vcmenueditornewitembox.gif "vcMenuEditorNewItemBox")<br/>
   [新しい項目] ボックス

1. たとえば「ファイル」など、新しいメニューの名前を入力します。

   入力したテキストは、 **メニュー** エディターと、 **プロパティ ウィンドウ** の [[キャプション]](/visualstudio/ide/reference/properties-window)ボックスの両方に表示されます。 新しいメニューのプロパティはこのどちらからでも編集できます。

   メニュー バーで新しいメニューの名前を指定すると、さらに別のメニューを追加できるように [新しい項目] ボックスが右に移動し、最初のメニューの下に新しい [新しい項目] ボックスが表示されます。この新しいボックスでメニュー コマンドを追加できます。

   ![展開された 新しい項目ボックス](../windows/media/vcmenueditornewitemboxexpanded.gif "vcMenuEditorNewItemBoxExpanded")<br/>
   メニュー名の入力後にフォーカスが移動した [新しい項目] ボックス

   > [!NOTE]
   > メニュー バーの単一項目のメニューを作成するには、設定、**ポップアップ**プロパティを**False**します。

### <a name="to-create-a-submenu"></a>サブメニューを作成するには

1. サブメニューを作成するメニュー コマンドを選択します。

1. 右側に表示される **[新しいアイテム]** ボックスに、新しいメニュー コマンドの名前を入力します。 サブメニューのメニューには、この新しいコマンドが最初に表示されます。

1. サブメニューのメニューにメニュー コマンドを追加します。

## <a name="to-insert-a-new-menu-between-existing-menus"></a>既存のメニュー間に新規メニューを挿入するには

既存のメニューの名前とキーを押して選択、**挿入**キーまたはメニュー バーを右クリックし、選択**Insert New**ショートカット メニューから。

**新しい項目の**ボックスが選択した項目の前に挿入されます。

### <a name="to-add-commands-to-a-menu"></a>メニューにコマンドを追加するには

1. メニューを作成します。

1. たとえば、メニューの名前を選択**ファイル**します。

   各メニューが展開され、コマンド用の新しい項目ボックスが表示されます。 コマンドを追加するなど、**新規**、**オープン**と**閉じる**を**ファイル**メニュー。

1. [新しい項目] ボックスに新しいメニュー コマンドの名前を入力します。

   > [!NOTE]
   > 入力したテキストは、 **メニュー** エディターと、 **プロパティ ウィンドウ** の [[キャプション]](/visualstudio/ide/reference/properties-window)ボックスの両方に表示されます。 新しいメニューのプロパティはこのどちらからでも編集できます。

   > [!TIP]
   > ユーザーがメニュー コマンドを選択できるようにするニーモニック キー (ホット キー) を定義することができます。 アンパサンドを入力 (`&`) ニーモニックとして指定する文字の前にします。 この文字を入力することで、ユーザーはメニュー コマンドを選択できます。

1. **プロパティ**ウィンドウで、メニュー コマンドを適用するプロパティを選択します。 詳細については、次を参照してください。[メニュー コマンドのプロパティ](../windows/menu-command-properties.md)します。

1. **プロンプト**ボックスに、**プロパティ**ウィンドウで、アプリケーションのステータス バーに表示するプロンプト文字列を入力します。

   この手順では、作成したメニュー コマンドと同じリソース識別子を持つ文字列テーブルにエントリを作成します。

   > [!NOTE]
   > プロンプトがメニュー項目に適用できるだけ、**ポップアップ**プロパティの**True**します。 たとえば、トップレベルのメニュー項目にサブメニュー項目がある場合、プロンプトを適用できます。 目的を**プロンプト**をどうなるかを示すためには、ユーザーがメニュー項目を選択した場合。

1. キーを押して**Enter**メニュー コマンドを完了します。

   新しい項目ボックスが選択され、追加のメニュー コマンドを作成できるようになります。

### <a name="to-select-multiple-menu-commands"></a>複数のメニュー コマンドを選択するには

複数のメニュー名または削除、またはプロパティを変更するなどの一括操作を実行するメニュー コマンドを選択することができます。

押しながら、 **Ctrl**キーで、メニューまたはサブメニューのコマンドを選択します。

### <a name="to-move-and-copy-menus-and-menu-commands"></a>移動し、メニューとメニュー コマンドをコピーするには

> [!NOTE]
> ドラッグでコピーした項目を別のメニュー ウィンドウの別のメニューに貼り付けることもできます。

#### <a name="to-move-or-copy-menus-or-menu-commands-using-the-drag-and-drop-method"></a>ドラッグ アンド ドロップ操作を使用してメニューやメニュー コマンドを移動またはコピーするには

1. 移動する項目を次の場所にドラッグまたはコピーします。

   - 現在のメニュー上の新しい場所。

   - 別のメニュー (他のメニューに移動するには、そのメニューにマウス ポインターをドラッグします)。

1. 挿入ガイドで目的の位置が示されたら、メニュー コマンドをドロップします。

#### <a name="to-move-or-copy-menus-or-menu-commands-using-shortcut-menu-commands"></a>ショートカット メニューのコマンドを使用してメニューやメニュー コマンドを移動またはコピーするには

1. 1 つ以上のメニューまたはメニュー コマンドを右クリックします。

1. ショートカット メニューの **[切り取り]** (移動する場合) または **[コピー]** を選択します。

1. 別のメニュー項目を移動する場合はリソースまたはリソース スクリプト ファイル、[別のウィンドウで開きます](/visualstudio/ide/customizing-window-layouts-in-visual-studio)します。

1. メニューやメニュー コマンドを移動またはコピーする位置を選択します。

1. ショートカット メニューの **[貼り付け]** を選択します。 移動またはコピーする項目は、選択した項目の前に配置されます。

### <a name="to-delete-a-menu-or-menu-command"></a>メニューまたはメニュー コマンドを削除するには

メニュー名やコマンドを右クリックし **削除**ショートカット メニューから。

> [!NOTE]
> 同様に、ショートカット メニューを使用して、コピー、切り取り、貼り付け、新しい項目の挿入、区切り記号の挿入、ID の編集、ポップアップとして表示、ニーモニックの確認などの操作を実行することができます。

## <a name="pop-up-menus"></a>ポップアップ メニュー

[ポップアップ メニュー](../mfc/menus-mfc.md) には、頻繁に使用するコマンドが表示されます。 これらは状況依存となっていて、マウス ポインターの場所に応じて表示できます。 アプリケーションでポップアップ メニューを使用には、メニュー自体をビルドし、アプリケーション コードに接続する必要があります。

アプリケーション コードがメニュー リソースをロードして使用する必要があるメニュー リソースを作成したら、 [TrackPopupMenu](/windows/desktop/api/winuser/nf-winuser-trackpopupmenu)がメニューを表示します。 外部を選択して、ポップアップ メニューが閉じるか、コマンドが選択すると、その関数を返します。 ユーザーがコマンドを選択した場合は、そのコマンドのメッセージが、ハンドルが渡されたウィンドウに送信されます。

### <a name="to-create-a-pop-up-menu"></a>ポップアップ メニューを作成するには

1. 空のタイトルでメニューを作成する (指定しない、**キャプション**)。

1. [新しいメニューにメニュー コマンドを追加](../windows/adding-commands-to-a-menu.md)します。 最初のメニュー コマンド、空のメニュー タイトルの下に移動 (一時的なキャプションという`Type Here`)。 **キャプション** とその他の情報を入力します。

   ポップアップ メニューのその他のメニュー コマンドに対して、この手順を繰り返します。

1. メニュー リソースを保存します。

### <a name="to-connect-a-pop-up-menu-to-your-application"></a>ショートカット メニューをアプリケーションに関連付けるには

1. (たとえば) WM_CONTEXTMENU のメッセージ ハンドラーを追加します。 詳細については、次を参照してください。[関数へのメッセージの割り当て](../mfc/reference/mapping-messages-to-functions.md)します。

1. 次のコードをメッセージ ハンドラーに追加します。

    ```cpp
    CMenu menu;
    VERIFY(menu.LoadMenu(IDR_MENU1));
    CMenu* pPopup = menu.GetSubMenu(0);
    ASSERT(pPopup != NULL);
    pPopup->TrackPopupMenu(TPM_LEFTALIGN | TPM_RIGHTBUTTON, point.x, point.y, AfxGetMainWnd());
    ```

   > [!NOTE]
   > [CPoint](../atl-mfc-shared/reference/cpoint-class.md)渡されたハンドラーが画面座標では、メッセージによって。

> [!NOTE]
> ポップアップ メニューをアプリケーションに接続するには、MFC が必要です。

### <a name="to-view-a-menu-resource-as-a-pop-up-menu"></a>メニュー リソースをポップアップ メニューとして表示するには

通常、作業するとき、**メニュー**エディター、メニュー バーでメニュー リソースが表示されます。 ただし、プログラムの実行中にアプリケーションのメニュー バーにメニュー リソースが追加されている場合もあります。

メニューを右クリックし、**ポップアップ表示**ショートカット メニューから。

   このオプションは、単なる表示設定で、メニューは変更されません。

> [!NOTE]
> メニュー バーの表示に変更するには、選択**ポップアップ表示**もう一度 (チェック マークが削除し、メニュー バーの表示を返します)。

## <a name="requirements"></a>必要条件

Win32

## <a name="see-also"></a>関連項目

[リソース エディター](../windows/resource-editors.md)<br/>
[メニュー コマンド](../windows/menu-command-properties.md)<br/>

<!--
[User-Interface Objects and Command IDs](../mfc/user-interface-objects-and-command-ids.md)<br/>
[Menus](../mfc/menus-mfc.md)<br/>
[Menus](https://msdn.microsoft.com/library/windows/desktop/ms646977.aspx)-->