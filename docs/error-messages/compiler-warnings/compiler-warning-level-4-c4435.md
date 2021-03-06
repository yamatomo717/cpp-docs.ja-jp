---
title: コンパイラの警告 (レベル 4) C4435
ms.date: 11/04/2016
ms.assetid: a04524af-2b71-4ff9-9729-d9d1d1904ed7
ms.openlocfilehash: 7db1d483f571289c5b890c223ba1e59ba3d1f41e
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50572329"
---
# <a name="compiler-warning-level-4-c4435"></a>コンパイラの警告 (レベル 4) C4435

'class1': /vd2 下のオブジェクトのレイアウトは仮想ベース 'class2' により変更されます。

既定では、この警告はオフに設定されています。 詳細については、「 [既定で無効になっているコンパイラ警告](../../preprocessor/compiler-warnings-that-are-off-by-default.md) 」を参照してください。

コンパイル/vd1 のオプションを既定値で、派生クラスがない、`vtordisp`示された仮想ベースのフィールド。  場合/vd2 または`#pragma vtordisp(2)`は実際には、`vtordisp`フィールドが存在する場合、オブジェクトのレイアウトの変更になります。  別の相互作用するモジュールがコンパイルされている場合のバイナリの互換性の問題に可能性`vtordisp`設定します。

## <a name="example"></a>例

次の例では、C4435 が生成されます。

```cpp
// C4435.cpp
// compile with: /c /W4
#pragma warning(default : 4435)
class A
{
public:
    virtual ~A() {}
};

class B : public virtual A  // C4435
{};
```

## <a name="see-also"></a>関連項目

[vtordisp](../../preprocessor/vtordisp.md)<br/>
[/vd (ディスプレイスメントの無効化)](../../build/reference/vd-disable-construction-displacements.md)