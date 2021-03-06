---
title: ドキュメント ビューの作成
ms.date: 11/04/2016
helpviewer_keywords:
- documents [MFC], creating
- views [MFC], and frame windows
- views [MFC], creating
- tables [MFC]
- MFC, views
- document/view architecture [MFC], creating document/view
- object creators
- MFC, documents
- tables [MFC], objects each MFC object creates
ms.assetid: bda14f41-ed50-439d-af9e-591174e7dd64
ms.openlocfilehash: eccc65df784d000f8dccc244e295da522658b626
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50633560"
---
# <a name="documentview-creation"></a>ドキュメントおよびビューの作成

フレームワークの実装を提供する、**新規**と**オープン**でコマンドを (特に)、**ファイル**メニュー。 新しいドキュメントとその関連するビューとフレーム ウィンドウの作成は、アプリケーション オブジェクト、ドキュメント テンプレートを新しく作成されたドキュメント、および新しく作成されたフレーム ウィンドウの間で協調的です。 次の表は、オブジェクトの作成内容をまとめたものです。

### <a name="object-creators"></a>オブジェクトの作成者

|Creator|作成します|
|-------------|-------------|
|Application オブジェクト|ドキュメント テンプレート|
|ドキュメント テンプレート|ドキュメント|
|ドキュメント テンプレート|フレーム ウィンドウ|
|フレーム ウィンドウ|表示|

## <a name="see-also"></a>関連項目

[ドキュメント テンプレートとドキュメント/ビューの作成手順](../mfc/document-templates-and-the-document-view-creation-process.md)<br/>
[ドキュメント テンプレートの作成](../mfc/document-template-creation.md)<br/>
[各種 MFC オブジェクト間の関係](../mfc/relationships-among-mfc-objects.md)<br/>
[新しいドキュメント、ウィンドウ、ビューの作成](../mfc/creating-new-documents-windows-and-views.md)

