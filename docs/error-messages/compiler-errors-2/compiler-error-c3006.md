---
title: コンパイラ エラー C3006
ms.date: 11/04/2016
f1_keywords:
- C3006
helpviewer_keywords:
- C3006
ms.assetid: 449082ec-fd45-4c47-8ab3-ba6a719e4dc4
ms.openlocfilehash: 7200d0ab3b14a1f9faa310f466963d74f7c98985
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50436206"
---
# <a name="compiler-error-c3006"></a>コンパイラ エラー C3006

'clause': OpenMP 'directive' ディレクティブ上の句には、必要な引数がありません

OpenMP ディレクティブに必要な引数がありません。

次の例では C3006 が生成されます。

```
// C3006.c
// compile with: /openmp
int main()
{
   #pragma omp parallel shared   // C3006
   // Try the following line instead:
   // #pragma omp parallel shared(x) {}

}
```