---
title: コンパイラ エラー C3046
ms.date: 11/04/2016
f1_keywords:
- C3046
helpviewer_keywords:
- C3046
ms.assetid: 2e53d835-faa1-4ec0-9807-41f3dc552635
ms.openlocfilehash: 56fffc0e9aab19f8ad8510ad886ec255a327249d
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50502805"
---
# <a name="compiler-error-c3046"></a>コンパイラ エラー C3046

OpenMP '#pragma omp sections' の領域で構造化ブロックがありません

[sections](../../parallel/openmp/reference/sections-openmp.md) ディレクティブに空のコード ブロックが含まれています。

次の例では C3046 が生成されます。

```
// C3046.cpp
// compile with: /openmp /c
#include "omp.h"

int main() {
   int n2 = 2, n3 = 3;

   #pragma omp parallel
   {
      ++n2;

      #pragma omp sections
      {
/*
         ++n2;

         #pragma omp section
         {
            ++n3;
         }
*/
       }   // C3046 uncomment code to resolve this C3046
   }
}
```