---
title: コンパイラ エラー C2806
ms.date: 11/04/2016
f1_keywords:
- C2806
helpviewer_keywords:
- C2806
ms.assetid: 7c9ff1f4-1590-4c47-991d-b1075a173b48
ms.openlocfilehash: 1d37f5d1c6e253c01ae8a3b7640fb3ee4cf12534
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50490373"
---
# <a name="compiler-error-c2806"></a>コンパイラ エラー C2806

'operator 演算子' が仮パラメーターが多すぎます

オーバー ロードされた演算子は、パラメーターが多すぎます。

次の例では、C2806 が生成されます。

```
// C2806.cpp
// compile with: /c
class X {
public:
   X operator++ ( int, int );   // C2806 more than 1 parameter
   X operator++ ( int );   // OK
} ;
```