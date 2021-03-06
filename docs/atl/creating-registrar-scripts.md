---
title: ATL レジストラーのスクリプトを作成します。
ms.date: 11/04/2016
helpviewer_keywords:
- scripting, registry scripting
- ATL, registry
- registrar scripts [ATL]
- scripts, Registrar scripts
- scripts, creating
ms.assetid: cbd5024b-8061-4a71-be65-7fee90374a35
ms.openlocfilehash: bc76e41ab0d2cd2d26ef227e6368cb420a8a6401
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50480239"
---
# <a name="creating-registrar-scripts"></a>Creating Registrar Scripts

レジストラー スクリプトでは、システム レジストリへの API に基づくのではなく、データ ドリブンのアクセスを提供します。 レジストリにキーを追加するスクリプトで 1 つまたは 2 つの行がかかるので、データに基づくアクセスは通常は効率的です。

[ATL コントロール ウィザード](../atl/reference/atl-control-wizard.md)COM サーバーのレジストラー スクリプトを自動的に生成されます。 このスクリプトは、オブジェクトに関連付けられた .rgs ファイルで見つかります。

ATL レジストラーのスクリプト エンジンでは、実行時に、レジストラー スクリプトを処理します。 ATL は、サーバーのセットアップ中にスクリプト エンジンを自動的に呼び出します。

この記事では、次のレジストラー スクリプトに関連するトピックについて説明します。

- [バッカス ナウア記法 (BNF) 構文を理解する](../atl/understanding-backus-nauer-form-bnf-syntax.md)

- [パース ツリーを理解する](../atl/understanding-parse-trees.md)

- [レジストリ スクリプトの例](../atl/registry-scripting-examples.md)

- [置き換え可能パラメーターの使用 (レジストラー プリプロセッサ)](../atl/using-replaceable-parameters-the-registrar-s-preprocessor.md)

- [スクリプトの呼び出し](../atl/invoking-scripts.md)

## <a name="see-also"></a>関連項目

[レジストリ コンポーネント (レジストラー)](../atl/atl-registry-component-registrar.md)

