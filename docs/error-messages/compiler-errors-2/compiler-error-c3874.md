---
title: コンパイラ エラー C3874
ms.date: 11/04/2016
f1_keywords:
- C3874
helpviewer_keywords:
- C3874
ms.assetid: fd55fc05-69a7-4237-b3b7-dca1d5400b4f
ms.openlocfilehash: 73476d50b6cfe098ee9d8084837c2090e198a6cd
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50445046"
---
# <a name="compiler-error-c3874"></a>コンパイラ エラー C3874

'function' の戻り値の型 'type' ではなく ' int' をする必要があります。

関数のコンパイラで想定されていた戻り値の型ではありません。

次の例では、C3874 が生成されます。

```
// C3874b.cpp
double main()
{   // C3874
}
```