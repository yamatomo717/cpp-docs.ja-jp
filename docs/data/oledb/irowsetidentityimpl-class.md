---
title: IRowsetIdentityImpl クラス
ms.date: 11/04/2016
f1_keywords:
- ATL::IRowsetIdentityImpl
- ATL.IRowsetIdentityImpl
- IRowsetIdentityImpl
- IsSameRow
- IRowsetIdentityImpl.IsSameRow
- ATL.IRowsetIdentityImpl.IsSameRow
- IRowsetIdentityImpl::IsSameRow
- ATL::IRowsetIdentityImpl::IsSameRow
helpviewer_keywords:
- IRowsetIdentityImpl class
- IsSameRow method
ms.assetid: 56821edf-e045-40c8-96bd-231552cd5799
ms.openlocfilehash: b70ebdaa44331d9fa545763f0dd19e6320dd652b
ms.sourcegitcommit: c40469825b6101baac87d43e5f4aed6df6b078f5
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/12/2018
ms.locfileid: "51556219"
---
# <a name="irowsetidentityimpl-class"></a>IRowsetIdentityImpl クラス

OLE DB 実装[IRowsetIdentity](https://docs.microsoft.com/previous-versions/windows/desktop/ms715913(v=vs.85))インターフェイスで、行の id のテストが可能です。

## <a name="syntax"></a>構文

```cpp
template <class T, class RowClass = CSimpleRow>
class ATL_NO_VTABLE IRowsetIdentityImpl
   : public IRowsetIdentity
```

### <a name="parameters"></a>パラメーター

*T*<br/>
派生したクラス`IRowsetIdentityImpl`します。

*RowClass*<br/>
記憶域ユニット、`HROW`します。

## <a name="requirements"></a>必要条件

**ヘッダー:** atldb.h

## <a name="members"></a>メンバー

### <a name="methods"></a>メソッド

|||
|-|-|
|[IsSameRow](#issamerow)|同じ行を参照しているかどうかを 2 つの行ハンドルを比較します。|

## <a name="issamerow"></a> Irowsetidentityimpl::issamerow

同じ行を参照しているかどうかを 2 つの行ハンドルを比較します。

### <a name="syntax"></a>構文

```cpp
STDMETHOD(IsSameRow )(HROW hThisRow,
   HROW hThatRow);
```

#### <a name="parameters"></a>パラメーター

参照してください[IRowsetIdentity::IsSameRow](https://docs.microsoft.com/previous-versions/windows/desktop/ms719629(v=vs.85))で、 *OLE DB プログラマーズ リファレンス*します。

### <a name="remarks"></a>Remarks

行ハンドルを比較するには、このメソッドのキャスト、`HROW`ハンドルと`RowClass`メンバーおよび呼び出し`memcmp`ポインターにします。

## <a name="see-also"></a>関連項目

[OLE DB プロバイダー テンプレート](../../data/oledb/ole-db-provider-templates-cpp.md)<br/>
[OLE DB プロバイダー テンプレートのアーキテクチャ](../../data/oledb/ole-db-provider-template-architecture.md)