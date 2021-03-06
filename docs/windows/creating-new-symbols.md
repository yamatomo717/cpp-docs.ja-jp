---
title: '方法: シンボル (C++) の作成します。'
ms.date: 02/14/2019
f1_keywords:
- vc.editors.symbol.creating
- vc.editors.symbol.managing
- vc.editors.resourcesymbols
- vc.editors.symbol.resource
helpviewer_keywords:
- New Symbol dialog box [C++]
- symbols [C++], creating
- resources [C++], viewing
- resource symbols
- symbols [C++], viewing
- New Symbol dialog box [C++]
- Resource Symbols dialog box [C++]
- Change Symbol dialog box [C++]
- resource symbols
- View Use button
- resource editors [C++], resource symbols
ms.assetid: 35168d31-3af6-4ecd-9362-3707d47b53f3
ms.openlocfilehash: 01b810d162da4d59c2044fe02a1da5c0929d41b9
ms.sourcegitcommit: 470de1337035dd33682d935b4b6c6d8b1bdb0bbb
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56320602"
---
# <a name="how-to-create-symbols-c"></a>方法: シンボル (C++) の作成します。

新しいプロジェクトを開始しているときに割り当てられるが、リソースの作成する前に必要なシンボル名をマップする便利なことがあります。

**リソース シンボル**C++ ダイアログ ボックスでは、新しいリソース シンボルの追加、シンボルが表示されます、またはシンボルが使用中は、ソース コード内の場所へのスキップを変更することができます。

ダイアログ ボックスには、次のプロパティが含まれています。

|プロパティ|説明|
|--------------------------|------------------------------------------|
|**Name**|シンボルの名前を表示します。 詳細については、次を参照してください。[シンボル名の制限](../windows/symbol-name-restrictions.md)します。|
|**[値]**|シンボルの数値を表示します。 詳細については、次を参照してください。[シンボル値の制限](../windows/symbol-value-restrictions.md)します。|
|**使用中**|シンボルが 1 つ以上のリソースで使用されることを指定する場合にオンにします。 リソースの一覧が [次のリソースで使用] ボックスに表示されます。|
|**読み取り専用のシンボルを表示します。**|読み取り専用のリソースを表示する場合にオンにします。 既定で、**リソース シンボル** ダイアログ ボックスにリソース スクリプト ファイルで変更可能なリソースのみが表示されますが、このオプションを選択すると、変更可能なリソースは太字で表示されます。 および読み取り専用のリソースはプレーン テキストで表示されます。|
|**使用されます。**|シンボル一覧で選択したシンボルを使用するリソースが表示されます。 特定のリソース エディターに移動するでリソースを選択します。、**使用者** を選択**ビュー使用**します。|
|**新規**|開く、**新しいシンボル** ダイアログ ボックスで、名前を定義することができ、必要に応じて、新しいシンボル リソース識別子の値。|
|**変更**|開く、**シンボルの変更** ダイアログ ボックスで、名前またはシンボルの値を変更することができます。 使用中のコントロールまたはリソースのシンボルを変更するには、対応するリソース エディターを使用する必要があります。 詳細については、次を参照してください。[未使用のシンボルを変更する](../windows/changing-unassigned-symbols.md)します。|
|**ビューの使用**|対応するリソース エディターで、シンボルが含まれたリソースを開きます。|

## <a name="create-symbols"></a>シンボルを作成します。

### <a name="to-create-a-new-symbol"></a>新しいシンボルを作成するには

1. **リソース シンボル** ダイアログ ボックスで、選択**新規**します。

1. **名前**ボックスに、シンボル名を入力します。

1. 割り当てられたシンボル値を受け入れるか、新しい値を入力、**値**ボックス。

1. 選択**OK**新しいシンボルをシンボルの一覧に追加します。

> [!NOTE]
> 既に存在するシンボルの名前を入力すると、その名前のシンボルが既に定義されていることを示すメッセージ ボックスが表示されます。 複数の同じ名前のシンボルを定義することはできませんが、同じ数値を持つ異なるシンボルを定義することができます。 詳細については、次を参照してください。[シンボル名の制限](../windows/symbol-name-restrictions.md)と[シンボル値の制限](../windows/symbol-value-restrictions.md)します。

### <a name="to-view-resource-symbols"></a>リソース シンボルを表示するには

1. [リソース ビュー](../windows/resource-view-window.md)、.rc ファイルを右クリックします。

   > [!NOTE]
   > プロジェクトに .rc ファイルがまだ含まれていない場合は、「 [リソース スクリプト ファイルの新規作成](../windows/how-to-create-a-resource-script-file.md)」を参照してください。

1. 選択**リソース シンボル**リソース シンボル テーブルを表示するショートカット メニューから、**リソース シンボル** ダイアログ ボックス。

   > [!NOTE]
   > 定義済みのシンボルを表示するには、確認、**読み取り専用のシンボルを表示**チェック ボックスをオンします。

### <a name="to-open-the-resource-editor-for-a-given-symbol"></a>特定のシンボルに対するリソース エディターを開く

シンボルを参照しているときに、**リソース シンボル**、特定のシンボルの使用方法の詳細についてをする可能性があります。 **ビュー使用**ボタンはこの情報を取得する簡単な方法を提供します。

#### <a name="to-move-to-the-resource-editor-where-a-symbol-is-being-used"></a>シンボルが使用されている場所のリソース エディターに移動するには

1. 内のシンボルを選択して、**名前**のボックス、**リソース シンボル** ダイアログ ボックス。

1. **使用者**ボックスで、興味のあるリソースの種類を選択します。

1. 選択、**ビュー使用**ボタンをクリックします。

   リソースが適切なエディターに表示されます。

## <a name="requirements"></a>必要条件

Win32

## <a name="see-also"></a>関連項目

[リソース識別子 (シンボル)](../windows/symbols-resource-identifiers.md)<br/>
[シンボルを管理します。](../windows/changing-a-symbol-or-symbol-name-id.md)<br/>
[定義済みシンボル ID](../windows/predefined-symbol-ids.md)<br/>