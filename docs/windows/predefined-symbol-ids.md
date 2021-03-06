---
title: 定義済みのシンボル ID
ms.date: 02/14/2019
helpviewer_keywords:
- symbols [C++], predefined IDs
- predefined symbol IDs
ms.assetid: 91a5d610-1a04-47e8-b8a4-63ad650a90df
ms.openlocfilehash: d7402bf7aaaf7c72382b57963d5d759adaa71115
ms.sourcegitcommit: 470de1337035dd33682d935b4b6c6d8b1bdb0bbb
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2019
ms.locfileid: "56320797"
---
# <a name="predefined-symbol-ids"></a>定義済みのシンボル ID

新しいプロジェクトを開始する時点で、ユーザーが使用できるように、プロジェクトの種類に応じていくつかのシンボル ID が事前に定義されています。 これらのシンボル ID は、MFC など、さまざまなライブラリとプロジェクトの種類をサポートします。 これらのシンボル ID は、アプリケーションに通常含まれている共通のタスクか、マウスやポインターなどのハードウェア アイテムのアクションを表します。

これらのシンボル ID は、リソースを使用する際に重要になります。 また、アクセラレータ テーブルを編集するときにも使用できます。既に仮想キーに関連付けられているシンボル ID もあります。 手順で利用可能なことも、[プロパティ ウィンドウ](/visualstudio/ide/reference/properties-window)します。 定義済みの任意のシンボル ID を新しいリソースに割り当てたり、これらのシンボル ID にアクセラレータ キーを割り当てたりできます。シンボル ID に関連付けられている機能は、自動的にそのキーの組み合わせに関連付けられます。

これらのライブラリには、プロジェクトの一部として表示される以下の定義済みのシンボルがあります。

- [MFC の定義済みシンボル](../windows/mfc-predefined-symbols.md)

- [ATL の定義済みシンボル](../windows/atl-predefined-symbols.md)

- [Win32 の定義済みシンボル](../windows/win32-predefined-symbols.md)

   > [!NOTE]
   > 定義済みのシンボルは、常に読み取り専用です。

## <a name="requirements"></a>必要条件

Win32、MFC、または ATL

## <a name="see-also"></a>関連項目

[リソース識別子 (シンボル)](../windows/symbols-resource-identifiers.md)<br/>
[シンボルを作成します。](../windows/creating-new-symbols.md)<br/>
[シンボルを管理します。](../windows/changing-a-symbol-or-symbol-name-id.md)<br/>