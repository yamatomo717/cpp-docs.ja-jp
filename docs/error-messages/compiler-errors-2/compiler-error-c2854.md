---
title: コンパイラ エラー C2854
ms.date: 11/04/2016
f1_keywords:
- C2854
helpviewer_keywords:
- C2854
ms.assetid: 917fec9c-790a-4149-8dfc-00d17a09199c
ms.openlocfilehash: a1c30e1fa0f70e5e7bb4b1c97421ca06913fc6f4
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50628970"
---
# <a name="compiler-error-c2854"></a>コンパイラ エラー C2854

#pragma hdrstop に構文エラー

`#pragma hdrstop`無効なファイル名を提供します。 プラグマの後にかっこや引用符で省略可能なファイル名を指定できます。

次の例では、C2854 が生成されます。

```
// C2854.cpp
// compile with: /c
#pragma hdrstop( "\\source\\pchfiles\\myheader.pch" ]   // C2854
// try the following line instead
// #pragma hdrstop( "\\source\\pchfiles\\myheader.pch" )
```