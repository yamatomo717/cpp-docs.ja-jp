---
title: コンパイラ エラー C2574
ms.date: 11/04/2016
f1_keywords:
- C2574
helpviewer_keywords:
- C2574
ms.assetid: 3e1c5c18-ee8b-4dbb-bfc0-d3b8991af71b
ms.openlocfilehash: 764ff36441c563edd538c41be5c23c12f80e2537
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50604959"
---
# <a name="compiler-error-c2574"></a>コンパイラ エラー C2574

'デコンス トラクター': 静的に宣言することはできません

デストラクターおよびコンス トラクターを宣言できます`static`します。

次の例では、C2574 が生成されます。

```
// C2574.cpp
// compile with: /c
class A {
   virtual static ~A();   // C2574
   //  try the following line instead
   // virtual ~A();
};
```