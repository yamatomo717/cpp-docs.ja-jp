---
title: no_registry
ms.date: 10/18/2018
f1_keywords:
- no_registry
helpviewer_keywords:
- no_registry attribute
ms.assetid: d30de4e2-551c-428c-98fd-951330d578d3
ms.openlocfilehash: bd101f5ca1776518ff4c5092da99134110bbb0b0
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50503026"
---
# <a name="noregistry"></a>no_registry

**no_registry**レジストリにインポートされたタイプ ライブラリを検索しないようにコンパイラに指示`#import`します。

## <a name="syntax"></a>構文

```
#import filename no_registry
```

### <a name="parameters"></a>パラメーター

*ファイル名*<br/>
タイプ ライブラリ。

## <a name="remarks"></a>Remarks

参照されるタイプ ライブラリがインクルード ディレクトリで見つからない場合、タイプ ライブラリがレジストリである場合でも、コンパイルは失敗します。  **no_registry**で暗黙的にインポートされた他のタイプ ライブラリに伝達`auto_search`します。

ファイル名で指定され、`#import` に直接渡されるタイプ ライブラリの場合、コンパイラはレジストリを検索しません。

ときに`auto_search`が指定されている追加`#import`に s が生成されます、 **no_registry**の初期設定`#import`(場合初期`#import`ディレクティブが**no_registry**、 `auto_search`-生成された`#import`も**no_registry**)。

**no_registry**クロス コンパイラをレジストリ内のファイルの古いバージョンの検索のリスクを負うことがなく、参照されるタイプ ライブラリをインポートする場合に便利です。 **no_registry**もタイプ ライブラリが登録されていない場合に便利です。

## <a name="see-also"></a>関連項目

[#import の属性](../preprocessor/hash-import-attributes-cpp.md)<br/>
[#import ディレクティブ](../preprocessor/hash-import-directive-cpp.md)