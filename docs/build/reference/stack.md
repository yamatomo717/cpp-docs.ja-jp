---
title: /STACK
ms.date: 11/04/2016
f1_keywords:
- /stack
helpviewer_keywords:
- -STACK editbin option
- STACK editbin option
- stack, setting size
- /STACK editbin option
ms.assetid: a39bcff0-c945-4355-80cc-8e4f24a5f142
ms.openlocfilehash: 89591a9d0a7f19422275b6bce6f4c5a7a723e800
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50647708"
---
# <a name="stack"></a>/STACK

```
/STACK:reserve[,commit]
```

## <a name="remarks"></a>Remarks

このオプションは、スタックのサイズをバイト単位で設定され、10 進数または C 言語表記では引数を受け取ります。 /STACK オプションは、実行可能ファイルのみに適用されます。

*予約*引数は、仮想メモリのスタック割り当ての合計を指定します。 指定した値を最も近い 4 バイトに切り上げられます。

省略可能な`commit`引数は、オペレーティング システムによって解釈されるは。 Windows NT、Windows 95、および Windows 98、`commit`を一度に割り当てる物理メモリの量を指定します。 仮想メモリがコミットされると、ページング ファイル内にメモリ空間が予約されます。 高度な`commit`値は、アプリケーションがより多くのスタック領域が必要がありますが、メモリ量と起動時間が増加時間を保存します。

## <a name="see-also"></a>関連項目

[EDITBIN オプション](../../build/reference/editbin-options.md)