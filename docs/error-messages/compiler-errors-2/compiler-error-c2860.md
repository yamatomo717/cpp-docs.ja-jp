---
title: コンパイラ エラー C2860
ms.date: 11/04/2016
f1_keywords:
- C2860
helpviewer_keywords:
- C2860
ms.assetid: ccc83553-90ed-4e94-b5e9-38b58ae38e31
ms.openlocfilehash: 7d468fb2a71ce23bcd527cb02663dd5f7b7eecad
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50585199"
---
# <a name="compiler-error-c2860"></a>コンパイラ エラー C2860

'void' '(void)' を除く、引数の型にすることはできません

型`void`引数の型とその他の引数として使用できません。

次の例では、C2860 が生成されます。

```
// C2860.cpp
// compile with: /c
void profunc1(void, int i);   // C2860
void func10(void);   // OK
```