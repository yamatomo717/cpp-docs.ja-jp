---
title: コンパイラ エラー C3748
ms.date: 11/04/2016
f1_keywords:
- C3748
helpviewer_keywords:
- C3748
ms.assetid: 6fe71a0a-dd93-4ce6-9729-b9616360cf34
ms.openlocfilehash: ef1c446f9feb3d40add62513a31fc81a382b98e1
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50628411"
---
# <a name="compiler-error-c3748"></a>コンパイラ エラー C3748

'interface': マネージ インターフェイスは、イベントを発生しない可能性があります

[_ _Event](../../cpp/event.md)インターフェイス内でキーワードは使用できません。

次の例では、C3748 が生成されます。

```
// C3748.cpp
__interface I {
// try the following line instead
// struct I {
   __event void f();   // C3748
};

int main() {
}
```