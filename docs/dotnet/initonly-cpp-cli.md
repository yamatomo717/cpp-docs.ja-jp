---
title: initonly (C++/CLI)
ms.date: 11/04/2016
f1_keywords:
- initonly_cpp
- initonly
helpviewer_keywords:
- initonly attribute [C++]
ms.assetid: f745d7fa-dc08-46f1-9b97-0977be58a008
ms.openlocfilehash: 85a127398997872a20a2360f1a852ebaaf17e33b
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50651283"
---
# <a name="initonly-ccli"></a>initonly (C++/CLI)

**initonly**はその変数の代入を示す状況依存のキーワードは、同じクラスの静的コンス トラクターまたは宣言の一部としてのみ発生することができます。

`initionly` を使用する方法を次の例に示します。

```
// mcpp_initonly.cpp
// compile with: /clr /c
ref struct Y1 {
   initonly
   static int staticConst1;

   initonly
   static int staticConst2 = 0;

   static Y1() {
      staticConst1 = 0;
   }
};
```

## <a name="see-also"></a>関連項目

[クラスと構造体](../windows/classes-and-structs-cpp-component-extensions.md)