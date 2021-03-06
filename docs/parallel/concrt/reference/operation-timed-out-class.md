---
title: operation_timed_out クラス
ms.date: 11/04/2016
f1_keywords:
- operation_timed_out
- CONCRT/concurrency::operation_timed_out
- CONCRT/concurrency::operation_timed_out::operation_timed_out
helpviewer_keywords:
- operation_timed_out class
ms.assetid: 963efe1d-a6e0-477c-9a70-d93d8412c897
ms.openlocfilehash: 8b25a35ac359fe052f9ae3c1cb15363acfbe93e5
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50561175"
---
# <a name="operationtimedout-class"></a>operation_timed_out クラス

このクラスは、操作がタイムアウトした場合にスローされる例外を表します。

## <a name="syntax"></a>構文

```
class operation_timed_out : public std::exception;
```

## <a name="members"></a>メンバー

### <a name="public-constructors"></a>パブリック コンストラクター

|名前|説明|
|----------|-----------------|
|[operation_timed_out](#ctor)|オーバーロードされます。 `operation_timed_out` オブジェクトを構築します。|

## <a name="inheritance-hierarchy"></a>継承階層

`exception`

`operation_timed_out`

## <a name="requirements"></a>必要条件

**ヘッダー:** concrt.h

**名前空間:** concurrency

##  <a name="ctor"></a> operation_timed_out

`operation_timed_out` オブジェクトを構築します。

```
explicit _CRTIMP operation_timed_out(_In_z_ const char* _Message) throw();

operation_timed_out() throw();
```

### <a name="parameters"></a>パラメーター

*メッセージ (_m)*<br/>
エラーの説明メッセージ。

## <a name="see-also"></a>関連項目

[コンカレンシー名前空間](concurrency-namespace.md)
