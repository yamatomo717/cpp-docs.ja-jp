---
title: _CIlog10
ms.date: 11/04/2016
apiname:
- _CIlog10
apilocation:
- msvcr100.dll
- msvcr120.dll
- msvcr80.dll
- msvcr90.dll
- msvcr110_clr0400.dll
- msvcrt.dll
- msvcr110.dll
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- CIlog10
- _CIlog10
helpviewer_keywords:
- _CIlog10 intrinsic
- CIlog10 intrinsic
ms.assetid: 05d7fcaa-3cff-4cc5-8d44-015e7cacba24
ms.openlocfilehash: 0814043f56122e5e5363940ead338f8617279b09
ms.sourcegitcommit: e98671a4f741b69d6277da02e6b4c9b1fd3c0ae5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2019
ms.locfileid: "55702948"
---
# <a name="cilog10"></a>_CIlog10

スタックのトップ値に対して `log10` 演算を実行します。

## <a name="syntax"></a>構文

```
void __cdecl _CIlog10();
```

## <a name="remarks"></a>コメント

このバージョンの `log10` 関数には、コンパイラで認識される特殊な呼び出し規則があります。 この関数は、コピーの生成を防ぎ、レジスタ割り当てが容易になるため、実行時間が短縮されます。

結果の値は、スタックのトップにプッシュされます。

## <a name="requirements"></a>要件

**プラットフォーム:** x86

## <a name="see-also"></a>「

[関数リファレンス (アルファベット順)](../c-runtime-library/reference/crt-alphabetical-function-reference.md)<br/>
[log、logf、log10、log10f](../c-runtime-library/reference/log-logf-log10-log10f.md)