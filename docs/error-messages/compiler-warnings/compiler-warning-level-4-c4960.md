---
title: コンパイラの警告 (レベル 4) C4960
ms.date: 11/04/2016
f1_keywords:
- C4960
helpviewer_keywords:
- C4960
ms.assetid: 3b4ed286-9e8d-46f1-af0c-00ba669693a9
ms.openlocfilehash: ff4a9b3d78a108a45abb18c22049b104e630bf15
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50516364"
---
# <a name="compiler-warning-level-4-c4960"></a>コンパイラの警告 (レベル 4) C4960

'function' はプロファイルするには多き過ぎます

[/LTCG:PGOPTIMIZE](../../build/reference/ltcg-link-time-code-generation.md)を使用するときに、命令が 65,535 を超える関数を含む入力モジュールが検出されました。 このような大きい関数は、ガイド付き最適化のプロファイルに使用できません。

この警告を解決するには、関数のサイズを小さくします。