---
title: /FS (同期 PDB 書き込みの強制)
ms.date: 11/04/2016
f1_keywords:
- /FS
helpviewer_keywords:
- -FS compiler option [C++]
- /FS compiler option [C++]
ms.assetid: b2caaffe-f6e1-4963-b068-648f06b105e0
ms.openlocfilehash: 180fe17e2047744a68f477654dc95aa74b25f281
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50660913"
---
# <a name="fs-force-synchronous-pdb-writes"></a>/FS (同期 PDB 書き込みの強制)

プログラム データベース (PDB) ファイルへの書き込み: によって作成された[/Zi](../../build/reference/z7-zi-zi-debug-information-format.md)または[/ZI](../../build/reference/z7-zi-zi-debug-information-format.md)— MSPDBSRV をシリアル化します。実行可能ファイルです。

## <a name="syntax"></a>構文

```
/FS
```

## <a name="remarks"></a>Remarks

既定では、ときに **/Zi**または **/ZI**を指定すると、コンパイラが型情報とシンボリック デバッグ情報を記述する PDB ファイルをロックします。 これにより、型の数が多い場合、コンパイル時に型情報の生成にかかる時間が大幅に短くなることがあります。 ウイルス対策プログラムなどの別のプロセスによって PDB ファイルが一時的にロックされている場合、コンパイラによる書き込みは失敗し、重大なエラーが発生することがあります。 この問題は、cl.exe の複数のコピーが同じ PDB ファイルにアクセスするときにも発生することがあります。たとえば、ソリューションで個別のプロジェクトが同じ中間ディレクトリまたは出力ディレクトリを使用する場合や、並列ビルドが有効になっている場合です。 **/FS**コンパイラ オプションは、コンパイラが PDB ファイルをロックするを防ぎます、MSPDBSRV 経由への書き込みを強制します。EXE へのアクセスをシリアル化します。 これにより、ビルド時間が大幅に長くなることがあります。cl.exe の複数のインスタンスが PDB ファイルに同時にアクセスするときに発生する可能性があるすべてのエラーを防止できないこともあります。 個別のプロジェクトによりそれぞれ別々の中間ディレクトリと出力ディレクトリに書き込まれるように、または、他のプロジェクトに依存するいずれかのプロジェクトでプロジェクトのビルドがシリアル化されるように、ソリューションを変更することをお勧めします。

[/MP](../../build/reference/mp-build-with-multiple-processes.md)オプションにより **/FS**既定。

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 開発環境において、このコンパイラ オプションを設定する方法

1. プロジェクトの **[プロパティ ページ]** ダイアログ ボックスを開きます。 詳細については、「[プロジェクトのプロパティの操作](../../ide/working-with-project-properties.md)」を参照してください。

1. 選択、 **C/C++** フォルダー。

1. 選択、**コマンドライン**プロパティ ページ。

1. 変更、**追加オプション**含めるプロパティを`/FS`選び、 **OK**します。

### <a name="to-set-this-compiler-option-programmatically"></a>このコンパイラ オプションをコードから設定するには

- 以下を参照してください。<xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>

## <a name="see-also"></a>関連項目

[コンパイラ オプション](../../build/reference/compiler-options.md)<br/>
[コンパイラ オプションの設定](../../build/reference/setting-compiler-options.md)