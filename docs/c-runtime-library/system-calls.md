---
title: システム コール
ms.date: 11/04/2016
f1_keywords:
- c.system
helpviewer_keywords:
- Windows [C++], system calls
- system calls
ms.assetid: 0255f2ec-a5a0-487e-8b09-9dad001d81ed
ms.openlocfilehash: b4b56fb0d61675aada1e8c8ba37d3382853da32c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50511840"
---
# <a name="system-calls"></a>システム コール

次の関数は、Windows オペレーティング システムの呼び出しに使用します。

## <a name="system-call-functions"></a>システム コール関数

|関数|使用|
|--------------|---------|
|[_findclose](../c-runtime-library/reference/findclose.md)|以前の検索操作で使用したリソースを解放します|
|[_findfirst、_findfirst32、_findfirst64、_findfirsti64、_findfirst32i64、_findfirst64i32、_wfindfirst、_wfindfirst32、_wfindfirst64、_wfindfirsti64、_wfindfirst32i64、_wfindfirst64i32](../c-runtime-library/reference/findfirst-functions.md)|指定した属性を持つファイルを検索します|
|[_findnext、_findnext32、_findnext64、_findnexti64、_findnext32i64、_findnext64i32、_wfindnext、_wfindnext32、_wfindnexti64、_wfindnext64、_wfindnexti64](../c-runtime-library/reference/findnext-functions.md)|指定した属性を持つ次のファイルを検索します|

## <a name="see-also"></a>参照

[カテゴリ別ユニバーサル C ランタイム ルーチン](../c-runtime-library/run-time-routines-by-category.md)<br/>
[ファイル処理](../c-runtime-library/file-handling.md)<br/>
[ディレクトリ制御](../c-runtime-library/directory-control.md)<br/>
[下位入出力](../c-runtime-library/low-level-i-o.md)<br/>
