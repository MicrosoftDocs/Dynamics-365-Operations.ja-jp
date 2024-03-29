---
title: 受信したドキュメントを解析する
description: この記事では、受信したドキュメントを解析できる電子申告の形式を設定する方法について説明します。
author: kfend
ms.date: 11/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2017-11-10
ms.dyn365.ops.version: 7.2999999999999998
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
ms.openlocfilehash: a256c84ab4b2cbd6a877d8ff69db83e15ed8b3f1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269708"
---
# <a name="parse-incoming-documents"></a>受信したドキュメントを解析する
[!include [banner](../includes/banner.md)]

この記事では、以下 3 つのタスクについて説明します:

- [アプリケーション データを更新するために受信したドキュメントを解析する](#parse-incoming-documents-to-update-application-data)
- [受信ドキュメントを Excel 形式で解析する](#parse-incoming-documents-in-excel-format)
- [CSV 形式で受信したドキュメントを解析する](#parse-incoming-documents-in-csv-format)

## <a name="parse-incoming-documents-to-update-application-data"></a>アプリケーション データを更新するために受信したドキュメントを解析する
電子申告 (ER) 書式をデザインしてアプリケーション内で実行し、受信した電子ドキュメントを解析し、その内容を使用してアプリケーション データを更新することができます。

導入された次の新しい ER 機能は、XML 形式の受信する電子ドキュメンの解析を改善します。

- **CASE** 形式要素は、XML 形式の受信電子ドキュメントを解析するように構成された ER 形式のルート要素として使用することができます。 **FILE** 形式要素は、**CASE** 要素の入れ子になった要素としてサポートされます。 したがって、1 つの ER フォーマットを設定して、異なるルート XML 要素を含む可能性のある受信電子ドキュメントを解析することができます。
- **入れ子になった要素の順序を解析** 属性が ER 形式の XML 形式要素に導入されました。 この属性を使用すると、読み込まれるファイルで予期される 1 つの XML 要素を定義することができます。 ネストされた要素には 2 つの有効なシーケンスがあります。

    - **形式どおり** - 受信ファイルは、ファイル内の入れ子になった要素の順序は、ER 形式に記載されている順序と同じ場合に有効です。
    - **任意** - 着信ファイルは、そのファイル内の順番に関係なく、ER 形式のすべての入れ子になった要素が解析ファイルに存在する場合に有効です。

この機能の詳細をよく理解するためには、タスク ガイド、\[ER - 受信ドキュメントを解析してアプリケーション データを更新する\] (「7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発」(10677) ビジネス プロセスの一部) を再生します。 このタスク ガイドは、Web サービスからの応答を ER 形式を使用して解析する方法を説明しています。

タスク ガイドのいくつかの手順を完了するには、次のファイルをダウンロードする必要があります。

| コンテンツの説明           | ファイル                                                              |
|-------------------------------|-------------------------------------------------------------------|
| ER データ モデル構成   | [EFSTAmodel.xml](https://download.microsoft.com/download/9/d/9/9d9c8562-7281-4db9-8bb3-b9083c6e2b5d/EFSTAmodel.xml)  |
| ER フォーマット構成       | [EFSTAformat.xml](https://download.microsoft.com/download/8/8/e/88e230cf-120f-4d58-93eb-779f2db1190f/EFSTAformat.xml) |
| Web サービス応答サンプル 1 | [Response1.xml](https://download.microsoft.com/download/8/0/5/805cc4fc-c6d2-447f-90e8-67ca6e970f2d/Response1.xml)   |
| Web サービス応答サンプル 2 | [Response2.xml](https://download.microsoft.com/download/e/0/a/e0a53eca-0d75-4958-8e3d-f9b1d91f1421/Response2.xml)   |
| Web サービス応答サンプル 3 | [Response3.xml](https://download.microsoft.com/download/e/c/2/ec24dcfa-84cd-44b9-9398-ff90f9627986/Response3.xml)   |
| Web サービス応答サンプル 4 | [Response4.xml](https://download.microsoft.com/download/6/6/b/66ba9a89-989a-454a-96c2-5e50b7e53fd7/Response4.xml)   |

## <a name="parse-incoming-documents-in-excel-format"></a>受信ドキュメントを Excel 形式で解析する

Microsoft Excel のブック (XLSX 形式のファイル) でデータを表す、受信した Microsoft Excel ファイルを解析する電子申告 (ER) の形式を設計できます。 その後、アプリケーションのデータを更新するのに、これらのファイルからの内容を使用できます。 これは、次のような場合に便利です。

- 新しいモデルおよびフォーマットをデザインし、実行時にテストします。 この場合、Excel は実際のアプリケーション データをシミュレーションします。
- アプリケーションを超えたデータを Excel で管理し、特定のレポートを送信するのに、このデータをインポートします。

受信ドキュメントを解析するための新しい ER 形式を設計する場合、Excel ワークブックを受信ファイルのテンプレートとしてインポートできます。 Excel の名前付きセルに保存されているデータ型を自動的に検出するには、**Excel からの更新** ダイアログ ボックスで **セル コンポーネントに Excel データ型を適用する** オプションを **はい** に設定します。

![Excel から更新ダイアログ ボックスの ER テンプレート インポートでセル コンポーネントに Excel データ型を適用するオプションをはいに設定します。](./media/er-parse-incoming-documents-update-from-excel.png)

編集した ER 形式の 1 つの [セル](er-fillable-excel.md#cell-component) コンポーネントに、データ型なし (無効) または不正なデータ型が自動的に検出された場合、後で **形式** タブの **データ型** フィールドでセルを手動で変更することが可能です。 これらのデータ型は、受信ファイルからのデータを使ってデータ モデルに入力する方法を指定する際に、形式モデルのマッピングで使用されます。

![モデル マッピング デザイナー ページのデータ モデル フィールドに形式フィールドのバインドのためにセルのデータ型を使用する。](./media/er-parse-incoming-documents-configure-model-mapping.gif)

既定では、この形式を実行して実際の受信ファイルを解析すると、Excel テンプレートをインポートしたときと同じように、ER は各セルのデータ型を検出しようとします。 場合によっては、誤ったデータ型が検出され、誤ったデータ変換やランタイム例外が発生することがあります。 Finance バージョン 10.0.25 以降では、編集された ER フォーマットの **形式** タブの **データ型** フィールドで各セル コンポーネントに対して指定されたデータ変換データ型を実行時に ER フレームワークに強制的に使用させることができます。 この動作を強制するには、**機能管理** ワークスペースで **ER 形式で定義されたセル データ タイプのみをデータ解析に強制使用する** 機能を有効にします。

この機能の詳細については、タスク ガイド **Microsoft Excel ファイルからの ER インポート データ (第 1 部: 形式の設計)** および  **Microsoft Excel ファイルからの ER インポート データ (第 2 部: データのインポート)** を実行してください (7.5.4.3 IT サービス/ソリューション コンポーネントの取得/開発 (10677) 業務プロセスの一部)。 これらのタスク ガイドは、 受信ドキュメントから情報をインポートしてアプリケーション データを更新する、ER 形式を使用した受信した Excel ファイルの解析方法を説明します。 タスク ガイドは [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=874684)からダウンロードできます。

上記のタスク ガイドを完了するには、次のファイルをダウンロードしてください。

| コンテンツの説明                         | ファイル                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| .XLSX 形式の受信ファイル - テンプレート    | [1099import template.xlsx](https://download.microsoft.com/download/b/8/b/b8ba3c9c-97c6-4fc2-898f-7701aac6035c/1099import-template.xlsx) |
| .XLSX 形式の受信ファイル - サンプル データ | [1099import data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx)     |

次のタスク ガイド [外部ファイルから電子申告にデータをインポートするのに必要なコンフィギュレーションの ER 作成](./tasks/er-required-configurations-import-data.md) を、現在の財務と運用アプリケーションで実行していない場合、次のファイルをダウンロードしてください。

| コンテンツの説明    | ファイル                                                            |
|------------------------|-----------------------------------------------------------------|
| ER モデル構成 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |

##  <a name="parse-incoming-documents-in-csv-format"></a>CSV 形式で受信したドキュメントを解析する

電子申告 (ER) 書式をデザインして、プレーン テキスト内 (CSV 形式のファイル) の表形式データを表す受信した電子ドキュメントを解析し、これらのドキュメントからの内容を使用してアプリケーション データを更新することができます。 次のアプローチを使用できます。

+ 解析ファイル内の各明細行は別々のレコードとみなすように指定して、新しいルート シーケンス要素を追加することによりフォーマットのデザインを開始します。

    + 追加されたシーケンス要素で、適切な値を選択します。たとえば、**シーケンス要素の区切り記号** フィールド グループの **特殊文字** フィールドの **改行 - Windows (CR LF)**。

+ 追加されたルート シーケンス要素の入れ子になった順序要素を追加して、解析ファイル内の各行が一連のフィールドとみなされるように指定して、フォーマットのデザインを続行します。

    + 解析明細行でフィールド区切りとして認識される **区切り記号** フィールドで、文字列を指定することができます。

        > [!NOTE]
        > - 異なるシーケンス要素に異なるフィールド区切りを定義して、フィールドが異なる文字で区切られている特定のファイルの明細行を解析することができます。
        > - **カスタム区切り記号** フィールドは、特定のシーケンス要素では空白のままにできます。 空のフィールドは、この順序を使用して解析されるファイル行が .txt (固定長テキスト) ファイル行のように解析されることを意味します。

    + **見積申請** フィールドで、このシーケンス要素で解析される明細行の一部のフィールドが特定の文字で囲まれることが期待される場合は値を選択します。  次のオプションを使用できます。

        + **すべて** – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を含めます。 これを選択した場合、フィールド見積に使用される **引用符** フィールドで目的の文字を定義します。 たとえば、二重引用符文字。
        + **テキストのみ** – は **文字列** データ型の任意のフィールドの解析行に引用符を含めます。 これを選択した場合、フィールド見積に使用される **引用符** フィールドで目的の文字を定義します。
        + **親のみから派生** – 親シーケンス要素に定義されている、同じ **見積申請** フィールド設定を使用します。 **引用符** フィールドの設定も親シーケンス要素の設定から取得されることに注意してください。
        + **なし** – 任意のデータ型の任意のフィールドについて、解析明細行の引用文字を除外します。

+ 解析明細行のフィールド セットを表す、追加されたシーケンス要素の入れ子になった要素を追加して、フォーマットのデザインを完成させます。 **文字列**、**DateTime**、**数値** のような **テキスト** グループの必要な要素を追加して、異なるデータ型の個々のフィールドのセットとして解析行の構造を記述することができます。

    + 解析の明細行の個々のフィールドを表す形式要素については、既定では、**多様性** フィールドでは何も選択されません。 これは、解析行のフィールドの値が必須と見なされることを意味します。 **多様性** フィールドで、**ゼロ、1 つ** を選択してオプションとして解析明細行のこのフィールドの値を検討します。

        > [!NOTE]
        > データソースの品目 **isMatch** は、**多様性** フィールドで **ゼロ、1 つ** が選択されている場合、この形式を各 **文字列**、**日時**、または **数値** 形式要素の ER データモデルにマップすると使用できます。 このフィールドに値が含まれているときは、**isMatch** は **True** を返します。 フィールドに値がない場合は、**False** が返されます。

この機能の詳細については、**ER 外部 CSV ファイルからデータをインポートするフォーマット構成を作成する**(「IT サービス/ソリューション コンポーネントの取得/開発 (10677)」の一部) タスク ガイドを再生してください。これは、ER フォーマットを使用して、受信した CSV ファイルを解析してアプリケーション データを更新する方法について説明しています。

上記のタスクガイドを完成させるには、次のファイルをダウンロードしてください。

| 肩書き                                  | ファイル名                                                            |
|----------------------------------------|----------------------------------------------------------------------|
| ER フォーマット構成                | [1099formatcsv.xml](https://download.microsoft.com/download/c/0/1/c014b0fa-d4ee-4de6-8f55-fa539df9ce83/1099formatcsv.xml)  |
| .csv 形式の受信ファイルのサンプル | [1099entriescsv.csv](https://download.microsoft.com/download/0/0/c/00c7c78c-55d5-46ba-b6ac-971fb9646502/1099entriescsv.csv) |

タスク ガイドを再生していない場合は、上記のタスク ガイドを完了するために必要な次のファイルをダウンロードしてください。現在の財務と運用アプリケーションの **外部ファイルから電子申告にデータをインポートするのに必要なコンフィギュレーションの ER 作成**。

| タイトル                  | ファイル名                                                       |
|------------------------|-----------------------------------------------------------------|
| ER モデル構成 | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

