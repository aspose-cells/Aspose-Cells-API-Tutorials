---
title: .NET でプログラム的にドキュメント変換の進行状況を追跡する
linktitle: .NET でプログラム的にドキュメント変換の進行状況を追跡する
second_title: Aspose.Cells .NET Excel 処理 API
description: この詳細なチュートリアルでは、Aspose.Cells for .NET を使用してドキュメント変換の進行状況をプログラムで追跡する方法を学習します。
type: docs
weight: 20
url: /ja/net/converting-excel-files-to-other-formats/tracking-document-conversion-progress/
---
## 導入
Aspose.Cells for .NET を使用してドキュメント変換プロセスを強化したいとお考えですか? そうであれば、ここが最適な場所です。このチュートリアルでは、Excel ドキュメントを PDF 形式に変換する際の変換の進行状況を追跡する方法について詳しく説明します。この操作を実行するための重要な手順を案内するだけでなく、その過程で役立つヒントもいくつか紹介します。それでは、始めましょう。
## 前提条件
ドキュメント変換の追跡の詳細に入る前に、いくつかの前提条件を満たす必要があります。
1. C# の基礎知識: C# を使用してコーディングするため、このプログラミング言語の基本的な理解が役立ちます。
2. Visual Studio がインストールされている: これは開発環境として機能します。任意のバージョンを使用できますが、常に最新のバージョンを選択することをお勧めします。
3.  Aspose.Cells for .NET: Aspose.Cellsがインストールされていることを確認してください。[Aspose ウェブサイト](https://releases.aspose.com/cells/net/).
4.  Excelファイル: 変換用のサンプルExcelファイルを用意します。簡単な`.xlsx`従うべきファイル。
## パッケージのインポート
前提条件が満たされたので、必要なパッケージを C# プロジェクトにインポートします。手順は次のとおりです。
### 新しいプロジェクトを作成する
1. Visual Studio を開いて、新しいプロジェクトを作成します。簡単にするために、コンソール アプリ テンプレートを選択します。
### Aspose.Cells への参照を追加する
2. ソリューション エクスプローラーで [参照] を右クリックし、[参照の追加] を選択して、Aspose.Cells アセンブリが自動的に追加されていない場合はそこに移動します。パッケージ マネージャー コンソールで次のコマンドを実行して、NuGet パッケージ マネージャーを使用することもできます。
```bash
Install-Package Aspose.Cells
```
### 名前空間のインポート
3. あなたの一番上に`Program.cs`ファイルに次の using ディレクティブを追加します。
```csharp
using Aspose.Cells.Rendering;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
これでプロジェクトのセットアップはすべて完了です。

基礎ができたので、ドキュメント変換を追跡する実際のプロセスをわかりやすいステップに分解してみましょう。 
## ステップ1: ディレクトリを定義する
まず、ソース ファイルと出力ファイルを保存するディレクトリを指定します。手順は次のとおりです。
```csharp
//ソースディレクトリ
string sourceDir = "Your Document Directory";
//出力ディレクトリ
string outputDir = "Your Document Directory";
```
必ず交換してください`"Your Document Directory"`システム上の実際のパスを入力します。これにより、ファイルを簡単に見つけることができます。
## ステップ2: ワークブックを読み込む
次に、Excelブックを読み込む必要があります。`Workbook`クラス。方法は次のとおりです。
```csharp
Workbook workbook = new Workbook(sourceDir + "PagesBook1.xlsx");
```
このコード行は、`Workbook`指定した Excel ファイルと対話できるようにするオブジェクトです。
## ステップ3: PDF保存オプションを設定する
さて、PDF保存オプションを設定しましょう。ここから進捗状況を追跡する魔法が始まります。`PdfSaveOptions`それにコールバックを割り当てます。
```csharp
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
pdfSaveOptions.PageSavingCallback = new TestPageSavingCallback();
```
カスタムコールバック（`TestPageSavingCallback`) を使用すると、ページ変換の進行状況を追跡するための独自のロジックを実装できます。
## ステップ4: ワークブックをPDFとして保存する
すべての設定が完了したら、ワークブックをPDFとして保存します。`Save`方法の`Workbook`次のようにクラスを作成します:
```csharp
workbook.Save(outputDir + "DocumentConversionProgress.pdf", pdfSaveOptions);
```
この行は変換プロセスをトリガーし、ページの処理中にコールバック メソッドを呼び出します。
## ステップ5: コールバッククラスを実装する
では、`TestPageSavingCallback`クラス。ここで、各ページの保存の開始時と終了時に何が起こるかを定義します。
```csharp
public class TestPageSavingCallback : IPageSavingCallback
{
    public void PageStartSaving(PageStartSavingArgs args)
    {
        Console.WriteLine("Start saving page index {0} of pages {1}", args.PageIndex, args.PageCount);
        //ページインデックス 2 より前のページは出力しません。
        if (args.PageIndex < 2)
        {
            args.IsToOutput = false;
        }
    }
    public void PageEndSaving(PageEndSavingArgs args)
    {
        Console.WriteLine("End saving page index {0} of pages {1}", args.PageIndex, args.PageCount);
        //ページインデックス 8 以降のページは出力しません。
        if (args.PageIndex >= 8)
        {
            args.HasMorePages = false;
        }
    }
}
```
- `PageStartSaving`このメソッドは、ページの保存が開始される直前に呼び出されます。ここでは、各ページの保存プロセスの開始を記録します。さらに、ページを出力するかどうかを制御できます。この場合、インデックス 2 より前のページはスキップされます。
- `PageEndSaving`: このメソッドは、ページが保存された後に呼び出されます。これにより、各ページの保存が終了したときにログに記録し、さらにページを処理するかどうかを制御できます。この例では、ページ インデックス 8 の後に停止します。
## 結論
おめでとうございます! Aspose.Cells for .NET を使用して、ドキュメント変換の進行状況を追跡するシステムを正常に実装しました。このアプローチにより、変換プロセスを監視できるだけでなく、どのページを含めるか、または除外するかを制御することもできるため、ドキュメント管理の効率が大幅に向上します。
## よくある質問
### Aspose.Cells とは何ですか?
Aspose.Cells は、開発者がプログラムによって Excel ファイルを作成、操作、変換できるようにする強力な .NET ライブラリです。
### Aspose.Cells の無料トライアルを入手するにはどうすればよいですか?
無料トライアルは以下からダウンロードできます。[Aspose ウェブサイト](https://releases.aspose.com/).
### 変換プロセスをカスタマイズすることは可能ですか?
はい、コールバックを使用すると、変換中にページが処理される方法をカスタマイズできます。
### 出力ファイル名を制御できますか?
もちろんです! ワークブックを保存するときに、出力ファイルに任意の名前を指定できます。
### Aspose.Cells のサポートはどこで見つかりますか?
サポートを受けるには、[Aspose フォーラム](https://forum.aspose.com/c/cells/9).