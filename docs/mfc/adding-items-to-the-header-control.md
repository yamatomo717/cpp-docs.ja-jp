---
title: ヘッダー コントロールへの項目の追加
ms.date: 11/04/2016
helpviewer_keywords:
- controls [MFC], header
- CHeaderCtrl class [MFC], adding items
- header controls [MFC], adding items to
ms.assetid: 2e9a28b1-7302-4a93-8037-c5a4183e589a
ms.openlocfilehash: c751458a3a2e7e049364ef22a161a3dc9f81df13
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50483565"
---
# <a name="adding-items-to-the-header-control"></a>ヘッダー コントロールへの項目の追加

ヘッダー コントロールを作成した後 ([CHeaderCtrl](../mfc/reference/cheaderctrl-class.md))、その親ウィンドウに「ヘッダー項目」する必要がある数だけ追加: 列ごとに、通常は 1 つ。

### <a name="to-add-a-header-item"></a>ヘッダー項目を追加するには

1. 準備、 [HD_ITEM](/windows/desktop/api/commctrl/ns-commctrl-_hd_itema)構造体。

1. 呼び出す[として](../mfc/reference/cheaderctrl-class.md#insertitem)、構造体を渡します。

1. 他のアイテムには、手順 1. および 2. を繰り返します。

詳細については、次を参照してください。[ヘッダー コントロールに項目を追加](/windows/desktop/Controls/header-controls)Windows SDK に含まれています。

## <a name="see-also"></a>関連項目

[CHeaderCtrl の使い方](../mfc/using-cheaderctrl.md)<br/>
[コントロール](../mfc/controls-mfc.md)

