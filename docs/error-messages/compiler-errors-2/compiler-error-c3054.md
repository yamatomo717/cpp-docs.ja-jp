---
title: コンパイラ エラー C3054
ms.date: 11/04/2016
f1_keywords:
- C3054
helpviewer_keywords:
- C3054
ms.assetid: 6f4b7ac5-0d12-474b-b611-76ff26ee41ac
ms.openlocfilehash: c45a59f136b989190a46fd9fbe00fdd0e4b89527
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50470129"
---
# <a name="compiler-error-c3054"></a>コンパイラ エラー C3054

'#pragma omp parallel' は、ジェネリック クラスまたはジェネリック関数では現在サポートされていません

詳細については、次を参照してください。[ジェネリック](../../windows/generics-cpp-component-extensions.md)と[OpenMP](../../parallel/openmp/openmp-in-visual-cpp.md)します。

## <a name="example"></a>例

次の例では C3054 が生成されます。

```
// C3054.cpp
// compile with: /openmp /clr /c
#include <omp.h>

ref struct MyBaseClass {
   // Delete the following 7 lines to resolve.
   generic <class ItemType>
   void Test(ItemType i) {   // C3054
      #pragma omp parallel num_threads(4)
      {
         int i = omp_get_thread_num();
      }
   }

   // OK
   void Test2() {
      #pragma omp parallel num_threads(4)
      {
         int i = omp_get_thread_num();
      }
   }
};
```