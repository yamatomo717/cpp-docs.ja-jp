---
title: __writeeflags
ms.date: 11/04/2016
f1_keywords:
- __writeeflags
helpviewer_keywords:
- __writeeflags intrinsics
ms.assetid: a62a522c-d7fa-4f10-a620-a3b32bdf3f17
ms.openlocfilehash: 8509bf37019d1525cdaca33bf1819d85ace7d75a
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50600045"
---
# <a name="writeeflags"></a>__writeeflags

指定した値をプログラムに書き込みますステータスと制御 (空文) を登録します。

## <a name="syntax"></a>構文

```
void __writeeflags(unsigned Value);
void __writeeflags(unsigned __int64 Value);
```

#### <a name="parameters"></a>パラメーター

|パラメーター|説明|
|---------------|-----------------|
|*[値]*|[in]立てるレジスタに書き込む値。 `Value`パラメーターは、32 ビット、32 ビット プラットフォームの時間の長いと 64 ビット、64 ビット プラットフォームの時間の長い。|

## <a name="remarks"></a>Remarks

これらのルーチンは組み込みとしてのみ使用できます。

## <a name="requirements"></a>必要条件

|組み込み|アーキテクチャ|
|---------------|------------------|
|`__writeeflags`|x86、x64|

**ヘッダー ファイル** \<intrin.h >

**Microsoft 固有の仕様はここまで**

## <a name="see-also"></a>関連項目

[コンパイラの組み込み](../intrinsics/compiler-intrinsics.md)<br/>
[__readeflags](../intrinsics/readeflags.md)