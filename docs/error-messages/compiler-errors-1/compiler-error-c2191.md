---
title: コンパイラ エラー C2191
ms.date: 11/04/2016
f1_keywords:
- C2191
helpviewer_keywords:
- C2191
ms.assetid: 051b8350-e5de-4f51-ab6e-96d32366bcef
ms.openlocfilehash: 23dfe1d95ab75f253fc2a7b4b00dfcd1aaaa3bbf
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50623523"
---
# <a name="compiler-error-c2191"></a>コンパイラ エラー C2191

最初よりも長い 2 番目のパラメーター リスト

C 関数は、2 回目に長いパラメーター リストで宣言されました。 C では、オーバー ロードされた関数はサポートされません。

## <a name="example"></a>例

次の例では、C2191 が生成されます。

```
// C2191.c
// compile with: /Za /c
void func( int );
void func( int, float );   // C2191 different parameter list
void func2( int, float );   // OK
```