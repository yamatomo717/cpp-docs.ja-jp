---
title: 集約型の初期化
ms.date: 11/04/2016
helpviewer_keywords:
- aggregate types [C++]
- union keyword [C], declarations
- types [C], initializing
- union keyword [C]
- aggregates [C++], initializing
ms.assetid: a8f8ed75-39db-4592-93b9-d3920d915810
ms.openlocfilehash: f6816a6f63de262b927a3c5aeed8774ba29c2eaa
ms.sourcegitcommit: f4be868c0d1d78e550fba105d4d3c993743a1f4b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/12/2019
ms.locfileid: "56151495"
---
# <a name="initializing-aggregate-types"></a>集約型の初期化

"*集約*" 型は、構造体、共用体、または配列型です。 集約型に集約型のメンバーが含まれる場合、初期化の規則が再帰的に適用されます。

## <a name="syntax"></a>構文

*initializer*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**{**  *initializer-list*  **}** /* 集計初期化用 \*/<br/>
&nbsp;&nbsp;&nbsp;&nbsp;**{**  *initializer-list*  **, }**

*initializer-list*:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*initializer*<br/>
&nbsp;&nbsp;&nbsp;&nbsp;*initializer-list*  **,**  *initializer*

*初期化子リスト*は、コンマで区切った初期化子のリストです。 リストの各初期化子は定数式または初期化子リストです。 したがって、初期化子リストは入れ子にできます。 このフォームは、このセクションの例に示すように集約型の集約メンバーを初期化する場合に便利です。 ただし、自動識別子の初期化子が単一の式である場合は、定数式である必要はありません。識別子に割り当てるための適切な型を持っているだけでかまいません。

各初期化子リストについて、定数式の値が、集約変数の対応するメンバーに順に割り当てられます。

*初期化子リスト*の値の数が集約型より少ない場合、集約型の残りのメンバーまたは要素は 0 に初期化されます。 明示的に初期化されない自動識別子の初期値は定義されません。 *初期化子リスト*に集約型よりも多くの値がある場合、エラーが発生します。 これらの規則は、埋め込まれた各初期化子リストと、集約全体に適用されます。

構造体の初期化子は、同じ型の式、または中かっこ (**{ }**) で囲まれているメンバーの初期化子のリストです。 名前のないビット フィールド メンバーは初期化されません。

共用体が初期化される場合、*初期化子リスト*は単一の定数式である必要があります。 定数式の値は共用体の最初のメンバーに割り当てられます。

配列のサイズが不明な場合、初期化子の数が配列のサイズを決定し、その型は完全になります。 初期化子の繰り返しを C で指定したり、前の値をすべて指定せずに配列の途中で要素を初期化したりする方法はありません。 プログラムでこの操作を必要とする場合、アセンブリ言語でルーチンを記述します。

初期化子の数が配列のサイズを設定することもできます。

```C
int x[ ] = { 0, 1, 2 }
```

ただし、サイズを指定し、誤った数の初期化子を設定すると、コンパイラはエラーを生成します。

**Microsoft 固有の仕様**

配列の最大サイズは **size_t** によって定義されます。 STDDEF.H ヘッダー ファイルに定義されている **size_t** は、0x00000000 - 0x7CFFFFFF の範囲の `unsigned int` です。

**Microsoft 固有の仕様はここまで**

## <a name="examples"></a>使用例

次の例では、配列の初期化子を示しています。

```C
int P[4][3] =
{
    { 1, 1, 1 },
    { 2, 2, 2 },
    { 3, 3, 3,},
    { 4, 4, 4,},
};
```

このステートメントは、4 × 3 の配列として `P` を宣言し、4 番目の行まで、その最初の行の要素を 1、2 番目の要素を 2、などのように初期化します。 3 行目と 4 行目の初期化子リストでは、最後の定数式の後にコンマが含まれていることに注意してください。 最後の初期化子リスト (`{4, 4, 4,},`) の後にもコンマが続きます。 これらの追加のコンマは許可されますが、必須ではありません。定数式を区切るコンマ、および初期化子リストを区切るコンマのみが必須です。

集約メンバーに埋め込まれた初期化子リストがない場合、値は単純にサブ集約の各メンバーに順に割り当てられます。 したがって、前の例の初期化は次と同じ結果をもたらします。

```C
int P[4][3] =
{
   1, 1, 1, 2, 2, 2, 3, 3, 3, 4, 4, 4
};
```

中かっこは、リストの個別の初期化子の周囲にも表示され、前の例を明確にするうえで役立ちます。

集約変数を初期化するときは、中かっこと初期化子リストを正しく使用する必要があります。 次の例では、コンパイラによる中かっこの解釈を詳細に示しています。

```C
typedef struct
{
    int n1, n2, n3;
} triplet;

triplet nlist[2][3] =
{
    { {  1, 2, 3 }, {  4, 5, 6 }, {  7, 8, 9 } },  /* Row 1 */
    { { 10,11,12 }, { 13,14,15 }, { 16,17,18 } }   /* Row 2 */
};
```

この例では、`nlist` は構造体の 2 × 3 の配列として宣言され、各構造体に 3 つのメンバーがあります。 次のように、初期化の 1 行目は `nlist` の最初の行に値を割り当てます。

1. 行 1 の最初の左の中かっこは、`nlist` の最初の集約メンバー (つまり、`nlist[0]`) の初期化を開始していることをコンパイラに通知します。

1. 2 番目の左の中かっこは、`nlist[0]` の最初の集約メンバー (つまり、`nlist[0][0]` の構造体) の初期化を開始していることを示します。

1. 最初の右中かっこは構造体 `nlist[0][0]` の初期化を終了します。次の左中かっこは `nlist[0][1]` の初期化を開始します。

1. プロセスは、最後の右中かっこが `nlist[0]` の初期化を終了する行の末尾まで続行されます。

行 2 は、同様の方法で `nlist` の 2 行目に値を割り当てます。 行 1 および行 2 の初期化子を囲む中かっこの外側のセットが必要であることに注意してください。 外側の中かっこを省略する次の構造はエラーを発生させます。

```C
triplet nlist[2][3] =  /* THIS CAUSES AN ERROR */
{
     {  1, 2, 3 },{  4, 5, 6 },{  7, 8, 9 },   /* Line 1 */
     { 10,11,12 },{ 13,14,15 },{ 16,17,18 }    /* Line 2 */
};
```

この構造では、行 1 の最初の左中かっこは 3 つの構造体の配列である `nlist[0]` の初期化を開始します。 値 1、2、および 3 は最初の構造体の 3 つのメンバーに割り当てられます。 次の右中かっこが見つかった場合 (値 3 の後)、`nlist[0]` の初期化は完了し、3 つの構造体配列の残りの 2 つの構造体は自動的に 0 に初期化されます。 同様に、`{ 4,5,6 }` は `nlist` の 2 番目の行の最初の構造体を初期化します。 `nlist[1]` の残りの 2 つ構造体は 0 に設定されます。 コンパイラは、次の初期化子リスト ( `{ 7,8,9 }` ) を見つけると、`nlist[2]` の初期化を試みます。 `nlist` には 2 行しかないため、この試行によりエラーが発生します。

次の例では、`int` の `x` の 3 つのメンバーが 1、2、および 3 にそれぞれ初期化されます。

```C
struct list
{
    int i, j, k;
    float m[2][3];
} x = {
        1,
        2,
        3,
       {4.0, 4.0, 4.0}
      };
```

上記の `list` 構造体では、`m` の最初の行の 3 つの要素は 4.0 に初期化されます。`m` の残りの行の要素は、既定で 0.0 に初期化されます。

```C
union
{
    char x[2][3];
    int i, j, k;
} y = { {
            {'1'},
            {'4'}
        }
      };
```

共用体変数 `y` は、この例では初期化されます。 共用体の最初の要素は配列であるため、初期化子は初期化子の集約です。 初期化子リスト `{'1'}` は配列の最初の行に値を割り当てます。 リストには 1 種類の値のみが表示されるため、最初の列の要素は、文字 `1` に初期化され、行の残りの 2 つの要素は、既定で値 0 に初期化されます。 同様に、`x` の 2 番目の行の最初の要素は、文字 `4` に初期化され、行の残りの 2 つの要素は値 0 に初期化されます。

## <a name="see-also"></a>関連項目

[初期化](../c-language/initialization.md)
