---
title: _com_error::operator =
ms.date: 11/04/2016
f1_keywords:
- _com_error::operator=
helpviewer_keywords:
- operator= _com_error objects
- = operator [C++], with specific Visual C++ objects
- operator = _com_error objects
ms.assetid: b9cc4094-d055-450c-b45a-0a95317488f8
ms.openlocfilehash: 68eb486ec109d98890ebf3adc0c086368380142b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50449596"
---
# <a name="comerroroperator-"></a>_com_error::operator =

**Microsoft 固有の仕様**

既存の `_com_error` オブジェクトを別のオブジェクトに割り当てます。

## <a name="syntax"></a>構文

```
_com_error& operator = (
   const _com_error& that
) throw ( );
```

#### <a name="parameters"></a>パラメーター

*それ*<br/>
`_com_error` オブジェクト。

**Microsoft 固有の仕様はここまで**

## <a name="see-also"></a>関連項目

[_com_error クラス](../cpp/com-error-class.md)