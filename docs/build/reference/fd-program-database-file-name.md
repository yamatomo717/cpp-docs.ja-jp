---
title: /Fd (プログラム データベース ファイル名)
ms.date: 11/04/2016
f1_keywords:
- /FD
- VC.Project.VCCLWCECompilerTool.ProgramDataBaseFileName
- VC.Project.VCCLCompilerTool.ProgramDataBaseFileName
helpviewer_keywords:
- /FD compiler option [C++]
- program database file name [C++]
- -FD compiler option [C++]
- PDB files, creating
- program database compiler option [C++]
- .pdb files, creating
- FD compiler option [C++]
ms.assetid: 3977a9ed-f0ac-45df-bf06-01cedd2ba85a
ms.openlocfilehash: 449b0a2be44f438c35feeb446df6d7c47f270c35
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50494318"
---
# <a name="fd-program-database-file-name"></a>/Fd (プログラム データベース ファイル名)

によって作成されたプログラム データベース (PDB) ファイルのファイル名を示す[/Z7、/Zi、/ZI (デバッグ情報の形式)](../../build/reference/z7-zi-zi-debug-information-format.md)します。

## <a name="syntax"></a>構文

```
/Fdpathname
```

## <a name="remarks"></a>Remarks

せず **/Fd**、PDB ファイル名の既定値は VC*x*0. pdb、場所*x*使用中の Visual C のメジャー バージョンします。

ファイル名 (パスは、円記号で終わる) が含まれていないパス名を指定する場合、コンパイラは、VC をという名前の .pdb ファイルを作成*x*指定したディレクトリ内の 0. pdb です。

拡張機能が含まれていないファイル名を指定する場合、コンパイラは、拡張機能として .pdb を使用します。

このオプションには、最小リビルドとインクリメンタル コンパイルに使用される状態 (.idb) ファイル名もします。

### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Visual Studio 開発環境において、このコンパイラ オプションを設定する方法

1. プロジェクトの **[プロパティ ページ]** ダイアログ ボックスを開きます。 詳細については、「[プロジェクトのプロパティの操作](../../ide/working-with-project-properties.md)」を参照してください。

1. **[C/C++]** フォルダーをクリックします。

1. **[出力ファイル]** プロパティ ページをクリックします。

1. 変更、**プログラム データベース ファイル名**プロパティ。

### <a name="to-set-this-compiler-option-programmatically"></a>このコンパイラ オプションをコードから設定するには

- 以下を参照してください。<xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.ProgramDataBaseFileName%2A>

## <a name="example"></a>例

このコマンドラインは、PROG.pdb と .idb ファイル PROG.idb という名前をという名前の .pdb ファイルを作成します。

```
CL /DDEBUG /Zi /FdPROG.PDB PROG.CPP
```

## <a name="see-also"></a>関連項目

[出力ファイル (/F) オプション](../../build/reference/output-file-f-options.md)<br/>
[コンパイラ オプション](../../build/reference/compiler-options.md)<br/>
[コンパイラ オプションの設定](../../build/reference/setting-compiler-options.md)<br/>
[パス名の指定](../../build/reference/specifying-the-pathname.md)