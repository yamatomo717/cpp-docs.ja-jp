---
title: ウィザードとしてのプロパティ シート
ms.date: 11/04/2016
helpviewer_keywords:
- property sheets, as wizards
ms.assetid: 1ea66ecb-23b0-484a-838d-58671a2999b5
ms.openlocfilehash: e8ba740d31681de214d2a497bc2694a94d09d84d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50542624"
---
# <a name="property-sheets-as-wizards"></a>ウィザードとしてのプロパティ シート

ウィザードのプロパティ シートの主要な特性は、タブの代わりに、[次へ] または [完了]、バックアップ、および [キャンセル] ボタンを持つナビゲーションが提供されることです。 呼び出す必要があります[CPropertySheet::SetWizardMode](../mfc/reference/cpropertysheet-class.md#setwizardmode)呼び出す前に[する](../mfc/reference/cpropertysheet-class.md#domodal)でこの機能を活用するためにプロパティ シート オブジェクトです。

ユーザーは同じ[CPropertyPage::OnSetActive](../mfc/reference/cpropertypage-class.md#onsetactive)と[CPropertyPage::OnKillActive](../mfc/reference/cpropertypage-class.md#onkillactive)別のページに 1 つのページから移動中に通知します。 [次へ] および [完了] ボタンは、相互に排他的なコントロールです。つまり、一度に 1 つだけ表示されます。 最初のページで、[次へ] ボタンを有効にする必要があります。 ユーザーは、最後のページでは、[完了] ボタンが有効にする必要があります。 フレームワークによっては、これが自動的に行われませんが。 呼び出す必要が[CPropertySheet::SetWizardButton](../mfc/reference/cpropertysheet-class.md#setwizardbuttons)これを実現する最後のページにします。

すべての既定のボタンを表示するには [完了] ボタンを表示し、[次へ] ボタンを移動します。 次のボタンに、相対的な位置を維持するため、[戻る] ボタンを移動します。

## <a name="example"></a>例

[!code-cpp[NVC_MFCDocView#5](../mfc/codesnippet/cpp/property-sheets-as-wizards_1.cpp)]

## <a name="see-also"></a>関連項目

[プロパティ シート](../mfc/property-sheets-mfc.md)

