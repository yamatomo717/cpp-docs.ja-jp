---
title: コンパイラ エラー C3455
ms.date: 11/04/2016
f1_keywords:
- C3455
helpviewer_keywords:
- C3455
ms.assetid: 218e5cfe-5391-4eeb-81c2-85c47e3a6cd2
ms.openlocfilehash: 4451ddbd8d5a7125112ef8e1c58e8843095bffd4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614397"
---
# <a name="compiler-error-c3455"></a>コンパイラ エラー C3455

'attribute': どの属性コンストラクターも引数に一致しませんでした

無効な値が属性の宣言に使用されました。  詳細については、「 [attribute](../../windows/attributes/attribute.md) 」を参照してください。

## <a name="example"></a>例

次の例では C3455 が生成されます。

```
// C3455.cpp
// compile with: /clr /c
using namespace System;

[attribute("MyAt")]   // C3455
// try the following line instead
// [attribute(All)]
ref struct MyAttr {
   MyAttr() {}
};
```