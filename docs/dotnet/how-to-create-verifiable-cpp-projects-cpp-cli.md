---
title: '方法: 確認可能な C++ プロジェクトを作成する (C++/CLI)'
ms.date: 11/04/2016
helpviewer_keywords:
- verifiable assemblies [C++], creating
- conversions, C++ projects
- Visual C++ projects
ms.assetid: 4ef2cc1a-e3e5-4d67-8d8d-9c614f8ec5d3
ms.openlocfilehash: acd37469f0702b73cdb1386fcf43091c8d27aebb
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50630439"
---
# <a name="how-to-create-verifiable-c-projects-ccli"></a>方法: 検証可能な C++ プロジェクトを作成 (C +/cli CLI)

Visual C アプリケーション ウィザードでは、検証可能なプロジェクトは作成されません。

> [!IMPORTANT]
> Visual Studio 2015 で非推奨とされ、Visual Studio 2017 がサポートしていない、 **/clr: 純粋な**と **/clr:safe**検証可能なプロジェクトを作成します。 検証可能なコードが必要な場合は、c# コードを変換することをお勧めします。

ただし、以前のバージョンをサポートする Visual C コンパイラ ツールセットを使用している場合 **/clr: 純粋な**と **/clr:safe**、検証可能にするプロジェクトを変換できます。 このトピックでは、プロジェクトのプロパティを設定し、検証可能なアプリケーションを生成するために、Visual C プロジェクトを変換するプロジェクトのソース ファイルを変更する方法について説明します。

## <a name="compiler-and-linker-settings"></a>コンパイラとリンカーの設定

既定は、.NET プロジェクトは/clr コンパイラ フラグを使用し、x86 を対象とハードウェアにリンカーを構成します。 検証可能なコードは、/clr:safe フラグを使用する必要があり、ネイティブ機械語命令ではなく MSIL を生成するようにリンカーに指示する必要があります。

### <a name="to-change-the-compiler-and-linker-settings"></a>コンパイラとリンカーの設定を変更するには

1. プロジェクトのプロパティ ページを表示します。 詳細については、「[プロジェクト プロパティの操作](../ide/working-with-project-properties.md)」を参照してください。

1. **全般**ページで、**構成プロパティ**、ノード セット、**共通言語ランタイム サポート**プロパティを**安全な MSIL 共通言語ランタイム サポート (//clr:safe)** します。

1. **詳細**ページで、**リンカー** 、ノード セット、 **CLR イメージ タイプ**プロパティを**安全 IL イメージの強制 (//clrimagetype:safe)** します。

## <a name="removing-native-data-types"></a>ネイティブ データ型を削除します。

実際に使われていない場合でも、ネイティブ データ型は検証不可能であるために、ネイティブ型を含むすべてのヘッダー ファイルを削除する必要があります。

> [!NOTE]
> 次の手順は、Windows フォーム アプリケーション (.NET) とコンソール アプリケーション (.NET) のプロジェクトに適用されます。

### <a name="to-remove-references-to-native-data-types"></a>ネイティブ データ型への参照を削除するには

1. Stdafx.h ファイル内のすべてをコメントします。

## <a name="configuring-an-entry-point"></a>エントリ ポイントを構成します。

検証可能なアプリケーションでは、C ランタイム ライブラリ (CRT) を使用できないため、これらは、標準のエントリ ポイントとしての main 関数を呼び出すには、CRT に依存できません。 つまり、リンカーに最初に呼び出される関数の名前を明示的に指定する必要があります。 (ここでは、Main() は、CRT 以外のエントリ ポイントを指定する main() または _tmain() の代わりに使用されますが、エントリ ポイントは、明示的に指定する必要があります、ため、この名前は任意)。

> [!NOTE]
> 次の手順は、コンソール アプリケーション (.NET) のプロジェクトに適用されます。

#### <a name="to-configure-an-entry-point"></a>エントリ ポイントを構成するには

1. プロジェクトのメインの .cpp ファイルで Main() _tmain() に変更します。

1. プロジェクトのプロパティ ページを表示します。 詳細については、「[プロジェクト プロパティの操作](../ide/working-with-project-properties.md)」を参照してください。

1. **[詳細設定]** ページで、**リンカー**ノード、入力`Main`として、**エントリ ポイント**プロパティの値。

## <a name="see-also"></a>関連項目

- [純粋なコードと検証可能なコード (C++/CLI)](../dotnet/pure-and-verifiable-code-cpp-cli.md)
