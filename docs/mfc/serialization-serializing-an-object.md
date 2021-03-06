---
title: 'シリアル化 : オブジェクトのシリアル化'
ms.date: 11/04/2016
helpviewer_keywords:
- serializing objects [MFC]
- serialization [MFC], objects
- objects [MFC], serializing
ms.assetid: 1db772b1-ad55-4fcf-b133-126cca082510
ms.openlocfilehash: 10a7c52e6187f4db8345e1eadb88faeefa50b419
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50588527"
---
# <a name="serialization-serializing-an-object"></a>シリアル化 : オブジェクトのシリアル化

この記事[シリアル化: シリアル化可能なクラスの作成](../mfc/serialization-making-a-serializable-class.md)クラスをシリアル化可能にする方法を示しています。 シリアル化可能なクラスを作成したら、そのクラスを使用してファイルとの間のオブジェクトをシリアル化することができます、 [CArchive](../mfc/reference/carchive-class.md)オブジェクト。 この記事で説明します。

- [CArchive オブジェクトがどのような](../mfc/what-is-a-carchive-object.md)します。

- [CArchive を作成する方法は 2](../mfc/two-ways-to-create-a-carchive-object.md)します。

- [CArchive を使用する方法 <\<と >> 演算子](../mfc/using-the-carchive-output-and-input-operators.md)します。

- [格納とアーカイブを通じた Cobject の読み込み](../mfc/storing-and-loading-cobjects-via-an-archive.md)します。

フレームワークのドキュメントをシリアル化のためのアーカイブを作成するか明示的に作成させることができます、`CArchive`自分でオブジェクトします。 使用してファイルと、シリアル化可能なオブジェクトのデータを転送することができます、<\<と >> 演算子の`CArchive`または場合によっては、呼び出すことによって、`Serialize`の関数を`CObject`-クラスを派生します。

## <a name="see-also"></a>関連項目

[シリアル化](../mfc/serialization-in-mfc.md)

