---
title: コンパイラ エラー C3138
ms.date: 11/04/2016
f1_keywords:
- C3138
helpviewer_keywords:
- C3138
ms.assetid: 364ee9e8-9358-410e-bd35-9c4a226a3753
ms.openlocfilehash: d812c14c2f364681fe28a58bdaed68fe3ed8ad30
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50614475"
---
# <a name="compiler-error-c3138"></a>コンパイラ エラー C3138

'interface': 'attribute' インターフェイスは IDispatch から継承するインターフェイスから、または IDispatch から継承する必要が

持つインターフェイス、[デュアル](../../windows/dual.md)または[dispinterface](../../windows/dispinterface.md)属性がない`IDispatch`直接的または間接的な基底インターフェイスとして。

次の例では、C3138 が生成されます。

```
// C3138.cpp
#include <unknwn.h>

[ object, uuid("77ac9240-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyCustomInterface
{
   HRESULT mf1(void);
};

[ dispinterface, uuid("3536f8a0-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyDispInterface : IUnknown
{
   [id(1)] HRESULT mf2(void);
};

[ object, dual, uuid("34e90a10-6e9a-11d2-97de-0000f805d73b") ]
__interface IMyDualInterface : IMyCustomInterface  // C3138 expected
{
   HRESULT mf3(void);
};
```