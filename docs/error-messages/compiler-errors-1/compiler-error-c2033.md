---
title: コンパイラ エラー C2033
ms.date: 11/04/2016
f1_keywords:
- C2033
helpviewer_keywords:
- C2033
ms.assetid: fd5a1637-9db2-4c98-a7cc-b63b39737cd9
ms.openlocfilehash: 8147c707c70e6c3f21ed81b2acf0a59b72065408
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50480432"
---
# <a name="compiler-error-c2033"></a>コンパイラ エラー C2033

'identifier' : ビット フィールドは間接参照できません

ビット フィールドが、許可されていないポインターとして宣言されました。

次の例では C2033 が生成されます。

```
// C2033.cpp
struct S {
   int *b : 1;  // C2033
};
```

考えられる解決方法:

```
// C2033b.cpp
// compile with: /c
struct S {
   int b : 1;
};
```