---
title: コンパイラの警告 (レベル 1) C4124
ms.date: 11/04/2016
f1_keywords:
- C4124
helpviewer_keywords:
- C4124
ms.assetid: c08c3a65-9584-47a1-a147-44f00c4b230e
ms.openlocfilehash: 04732619571420e777244b81bf4b93b775477a20
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50582569"
---
# <a name="compiler-warning-level-1-c4124"></a>コンパイラの警告 (レベル 1) C4124

_ _fastcall スタック チェックでは効率的ではありません。

`__fastcall`キーワードは、スタック チェックが有効で使用されました。

`__fastcall`規則には、高速のコードが生成されますが、低速コードをスタック チェックします。 使用する場合`__fastcall`、スタックのチェックをオフにする、 **check_stack**プラグマまたは/Gs します。

最初にこれらの条件下で宣言された関数にのみ警告が表示されます。