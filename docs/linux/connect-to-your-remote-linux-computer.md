---
title: Visual Studio でのリモートの Linux コンピューターへの接続
description: Visual Studio の C++ プロジェクト内からリモートの Linux マシンに接続する方法。
ms.date: 07/20/2018
ms.assetid: 5eeaa683-4e63-4c46-99ef-2d5f294040d4
ms.openlocfilehash: ce6a3c02846586dbc46b0c9bc0db0d579878c814
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50575241"
---
# <a name="connect-to-your-remote-linux-computer"></a>リモートの Linux コンピューターへの接続

Visual Studio で C++ の Linux プロジェクトをビルドするときに、Linux コードはリモートの Linux コンピューターにコピーされ、Visual Studio の設定に基づいてコンパイルされます。 このリモート接続をセットアップするには、次のようにします。

1. 最初にプロジェクトをビルドするか、新しいエントリを手動で作成します。その場合、**[ツール]、[オプション]** の順に選択し、**[クロス プラットフォーム]、[接続マネージャー]** ノードの順に開き、**[追加]** ボタンをクリックします。

   ![接続マネージャー](media/settings_connectionmanager.png)

   いずれの場合も、**[Connect to Remote System]** (リモート システムへの接続) ウィンドウが表示されます。

   ![リモート システムへの接続](media/connect.png)

1. 次の情報を入力します。

   | 入力 | 説明
   | ----- | ---
   | **ホスト名**           | ターゲット デバイスの名前または IP アドレス
   | **ポート**                | SSH サービスが実行されているポート (通常は 22)
   | **ユーザー名**           | 認証するユーザー
   | **認証の種類** | パスワードと秘密キーの両方がサポートされます。
   | **パスワード**            | 入力したユーザー名のパスワード
   | **秘密キー ファイル**    | ssh 接続用に作成された秘密キー ファイル
   | **パスフレーズ**          | 上で選択した秘密キーで使用されるパスフレーズ

1. **[接続]** ボタンをクリックすると、リモート コンピューターへの接続が試行されます。  接続に失敗した場合は、変更する必要がある入力ボックスが赤色で示されます。

   ![接続マネージャーのエラー](media/settings_connectionmanagererror.png)