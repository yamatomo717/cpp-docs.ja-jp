---
title: out_of_memory クラス
ms.date: 11/04/2016
f1_keywords:
- out_of_memory
- AMPRT/out_of_memory
- AMPRT/Concurrency::out_of_memory::out_of_memory
helpviewer_keywords:
- out_of_memory class
ms.assetid: 3aa7e682-8f13-4ae6-9188-31fb423956e4
ms.openlocfilehash: 2d5d028739bdf1b1ac31fafe3719b7f3a98fbb07
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50591896"
---
# <a name="outofmemory-class"></a>out_of_memory クラス

システムまたはデバイスのメモリ不足のためにメソッドが失敗した場合にスローされる例外。

## <a name="syntax"></a>構文

```
class out_of_memory : public runtime_exception;
```

## <a name="members"></a>メンバー

### <a name="public-constructors"></a>パブリック コンストラクター

|名前|説明|
|----------|-----------------|
|[out_of_memory コンス トラクター](#ctor)|`out_of_memory` クラスの新しいインスタンスを初期化します。|

## <a name="inheritance-hierarchy"></a>継承階層

`exception`

`runtime_exception`

`out_of_memory`

## <a name="requirements"></a>必要条件

**ヘッダー:** amprt.h

**名前空間:** Concurrency
## <a name="ctor"></a> out_of_memory

クラスの新しいインスタンスを初期化します。

### <a name="syntax"></a>構文

```
explicit out_of_memory(
    const char * _Message ) throw();

out_of_memory () throw();
```

### <a name="parameters"></a>パラメーター

*メッセージ (_m)*<br/>
エラーの説明。

### <a name="return-value"></a>戻り値

`out_of_memory` クラスの新しいインスタンス。

## <a name="see-also"></a>関連項目

[コンカレンシー名前空間 (C++ AMP)](concurrency-namespace-cpp-amp.md)
