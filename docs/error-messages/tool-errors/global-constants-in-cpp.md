---
title: C++ のグローバル定数
ms.date: 11/04/2016
helpviewer_keywords:
- global constants
- constants, global
ms.assetid: df5a9bd4-d0a8-4c1c-956e-b481d0bded7d
ms.openlocfilehash: 3da61b7718dadba9b454ee079651ce6372f21756
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50432618"
---
# <a name="global-constants-in-c"></a>C++ のグローバル定数

C++ のグローバル定数は、静的リンケージを持ちます。 これは、C とは異なりますグローバルを使用しようとする場合は、複数のファイルで C++ の定数エラーが発生した未解決外部です。 コンパイラは、変数の予約された領域を離れることはありません、グローバル定数を最適化します。

このエラーを解決する方法の 1 つは、const の初期化をヘッダー ファイルに含めるし、必要に応じて、関数のプロトタイプする場合と同様に、CPP ファイルにそのヘッダーを含めるには。 非定数、変数を作成し、それを評価するときの定数参照を使用する可能性もあることです。

次の例では、C2019 が生成されます。

```
// global_constants.cpp
// LNK2019 expected
void test(void);
const int lnktest1 = 0;

int main() {
   test();
}
```

この場合、次のようになります。

```
// global_constants_2.cpp
// compile with: global_constants.cpp
extern int lnktest1;

void test() {
  int i = lnktest1;   // LNK2019
}
```

## <a name="see-also"></a>関連項目

[リンカー ツール エラー LNK2019](../../error-messages/tool-errors/linker-tools-error-lnk2019.md)