---
title: モードレス ダイアログ ボックスの作成
ms.date: 11/04/2016
helpviewer_keywords:
- MFC dialog boxes [MFC], modeless
- modeless dialog boxes [MFC], creating
- MFC dialog boxes [MFC], creating
ms.assetid: 70d78c7f-3d40-477b-9f78-0f33c359f88b
ms.openlocfilehash: 4cc2bc0ce54ad658a8bf13e70a8fa54479cbbf79
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50453705"
---
# <a name="creating-modeless-dialog-boxes"></a>モードレス ダイアログ ボックスの作成

モードレス ダイアログ ボックスのダイアログ クラスで独自のパブリック コンス トラクターを提供する必要があります。 モードレス ダイアログ ボックスを作成する、パブリック コンス トラクターを呼び出すし、呼び出してダイアログ オブジェクトの[作成](../mfc/reference/cdialog-class.md#create)メンバー関数は、ダイアログ リソースを読み込めません。 呼び出すことができます**作成**中またはコンス トラクターの呼び出し後。 ダイアログ リソースに、プロパティが設定されている場合**WS_VISIBLE**、ダイアログ ボックスがすぐに表示されます。 呼び出す必要があるそうでない場合、 [ShowWindow](../mfc/reference/cwnd-class.md#showwindow)メンバー関数。

## <a name="see-also"></a>関連項目

[ダイアログ ボックスの有効期間](../mfc/life-cycle-of-a-dialog-box.md)

