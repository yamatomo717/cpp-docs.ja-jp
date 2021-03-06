---
title: includelib (C++ COM 属性)
ms.date: 10/02/2018
f1_keywords:
- vc-attr.includelib
helpviewer_keywords:
- includelib attribute
ms.assetid: cd90ea6e-5ae8-4f11-b8d1-662db95412b2
ms.openlocfilehash: 4cfadc84b9131aa787323b4967ae9cfc4baabbcb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50570418"
---
# <a name="includelib-c"></a>includelib (C++)

生成された .idl ファイルに含まれる、.idl ファイルまたは .h ファイル。

## <a name="syntax"></a>構文

```cpp
[ includelib(name.idl) ];
```

### <a name="parameters"></a>パラメーター

*name.idl*<br/>
生成された .idl ファイルの一部として含めるする .idl ファイルの名前。

## <a name="remarks"></a>Remarks

**Includelib** C++ 属性により、.idl ファイルまたは .h ファイルの後、生成された .idl ファイルに含まれる、`importlib`ステートメント。

## <a name="example"></a>例

次のコードは、.cpp ファイルで示されます。

```cpp
// cpp_attr_ref_includelib.cpp
// compile with: /LD
[module(name="MyLib")];
[includelib("includelib.idl")];
```

## <a name="requirements"></a>必要条件

### <a name="attribute-context"></a>属性コンテキスト

|||
|-|-|
|**対象**|任意の場所|
|**反復可能**|はい|
|**必要な属性**|なし|
|**無効な属性**|なし|

詳細については、「 [属性コンテキスト](cpp-attributes-com-net.md#contexts)」を参照してください。

## <a name="see-also"></a>関連項目

[IDL 属性](idl-attributes.md)<br/>
[スタンドアロン属性](stand-alone-attributes.md)<br/>
[import](import.md)<br/>
[importidl](importidl.md)<br/>
[include](include-cpp.md)<br/>
[importlib](importlib.md)