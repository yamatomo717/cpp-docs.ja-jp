---
title: CD2DEllipse クラス
ms.date: 11/04/2016
f1_keywords:
- CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse
- AFXRENDERTARGET/CD2DEllipse::CD2DEllipse
helpviewer_keywords:
- CD2DEllipse [MFC], CD2DEllipse
ms.assetid: e9f02f54-acf2-427e-b349-db50cd9a77df
ms.openlocfilehash: aa280215aaac55e3aaa9542ca1ab2bd9d21655e8
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50642040"
---
# <a name="cd2dellipse-class"></a>CD2DEllipse クラス

`D2D1_ELLIPSE`のラッパー。

## <a name="syntax"></a>構文

```
class CD2DEllipse : public D2D1_ELLIPSE;
```

## <a name="members"></a>メンバー

### <a name="public-constructors"></a>パブリック コンストラクター

|名前|説明|
|----------|-----------------|
|[CD2DEllipse::CD2DEllipse](#cd2dellipse)|オーバーロードされます。 構築、`CD2DEllipse`オブジェクトから`D2D1_ELLIPSE`オブジェクト。|

## <a name="inheritance-hierarchy"></a>継承階層

`D2D1_ELLIPSE`

`CD2DEllipse`

## <a name="requirements"></a>必要条件

**ヘッダー:** afxrendertarget.h

##  <a name="cd2dellipse"></a>  CD2DEllipse::CD2DEllipse

CD2DRectF オブジェクトから CD2DEllipse オブジェクトを構築します。

```
CD2DEllipse(const CD2DRectF& rect);
CD2DEllipse(const D2D1_ELLIPSE& ellipse);
  CD2DEllipse(const D2D1_ELLIPSE* ellipse);

CD2DEllipse(
    const CD2DPointF& ptCenter,
    const CD2DSizeF& sizeRadius);
```

### <a name="parameters"></a>パラメーター

*rect*<br/>
元の四角形

*楕円*<br/>
ソース楕円

*ptCenter*<br/>
楕円の中心点。

*sizeRadius*<br/>
X 半径と楕円の Y 半径。

## <a name="see-also"></a>関連項目

[クラス](../../mfc/reference/mfc-classes.md)
