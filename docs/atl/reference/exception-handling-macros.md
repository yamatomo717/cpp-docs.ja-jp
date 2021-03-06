---
title: 例外処理マクロ
ms.date: 11/04/2016
f1_keywords:
- atldef/ATL::_ATLCATCH
- atldef/ATL::_ATLCATCHALL
- atldef/ATL::_ATLTRY
helpviewer_keywords:
- exception handling, macros
- C++ exception handling, macros
ms.assetid: a8385d34-3fb0-4006-a42a-de045cacf0f4
ms.openlocfilehash: cf4b7ffb8c6b197dc1c4eea4b6c569e173bb188d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50544405"
---
# <a name="exception-handling-macros"></a>例外処理マクロ

これらのマクロは、例外処理のサポートを提供します。

|||
|-|-|
|[_ATLCATCH](#_atlcatch)|関連付けられているで発生するエラーを処理するステートメント`_ATLTRY`します。|
|[_ATLCATCHALL](#_atlcatchall)|関連付けられているで発生するエラーを処理するステートメント`_ATLTRY`します。|
|[_ATLTRY](#_atltry)|エラーが発生する可能性があります、保護されたコードのセクションをマークします。|

## <a name="requirements"></a>要件:

**ヘッダー:** atldef.h

##  <a name="_atlcatch"></a>  _ATLCATCH

関連付けられているで発生するエラーを処理するステートメント`_ATLTRY`します。

```
_ATLCATCH(e)
```

### <a name="parameters"></a>パラメーター

*e*<br/>
キャッチする例外。

### <a name="remarks"></a>Remarks

組み合わせて使用`_ATLTRY`します。 C++ に解決される[(CAtlException e) をキャッチ](../../cpp/try-throw-and-catch-statements-cpp.md)特定の種類の C++ 例外を処理するためです。

##  <a name="_atlcatchall"></a>  _ATLCATCHALL

関連付けられているで発生するエラーを処理するステートメント`_ATLTRY`します。

```
_ATLCATCHALL
```

### <a name="remarks"></a>Remarks

組み合わせて使用`_ATLTRY`します。 C++ に解決される[catch (...)](../../cpp/try-throw-and-catch-statements-cpp.md)すべての種類の C++ 例外を処理するためです。

##  <a name="_atltry"></a>  _ATLTRY

エラーが発生する可能性があります、保護されたコードのセクションをマークします。

```
_ATLTRY
```

### <a name="remarks"></a>Remarks

組み合わせて使用[_ATLCATCH](#_atlcatch)または[_ATLCATCHALL](#_atlcatchall)します。 C++ のシンボルに解決される[お試しください](../../cpp/try-throw-and-catch-statements-cpp.md)します。

## <a name="see-also"></a>関連項目

[[マクロ]](../../atl/reference/atl-macros.md)
