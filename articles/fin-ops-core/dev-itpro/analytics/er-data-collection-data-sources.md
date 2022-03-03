---
title: 電子申告形式でのデータ収集データ ソースの使用
description: このトピックでは、電子申告 (ER) 形式でデータ収集データ ソースを使用する方法について説明します。
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 185fb9a33cb4cc655dfdf640b4c239d617426c64
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323904"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>電子申告形式でのデータ収集データ ソースの使用

[!include [banner](../includes/banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) フレームワークのオペレーション デザイナーを使用して、異なる形式で送信ドキュメントを生成するために使用する ER ソリューションの形式コンポーネントをコンフィギュレーションすることができます。 コンフィギュレーションされた形式コンポーネントの階層構造は、さまざまなタイプの形式要素で構成されます。 これらの形式要素は、生成されたドキュメントに実行時に必要な情報を入力するために使用されます。 既定では、ER 形式の実行時に、形式要素は形式階層に表示されているのと同じ順序で、上から下に 1 つずつ実行されます。

ER がバインディングを含む形式要素を実行すると、そのバインディングの式が実行され、形式要素は生成されたドキュメントに値を追加します。 たとえば、バインディングはデータ モデル フィールドの値を形式要素に渡します。 実行時にデータ モデル フィールドの値を収集し、集計を行い、生成されたドキュメントに収集された値を入力するように、データ収集データ ソースを設定できます。 この方法を使用するには、初期バインディングを変更して、構成済みのデータ収集データ ソースを使用してデータ モデル フィールドの値を形式要素に渡します。 データ収集データ ソースを通じて値を渡すことにより、使用に必要な詳細を収集することができます。

データ収集データ ソースを構成する場合は、データ ソースで管理される値の型を指定します。 現在、値の収集には次の[データ型](er-formula-supported-data-types-primitive.md)がサポートされています。

- ブール値
- 日
- DateTime
- GUID
- Int64
- 整数
- 実績
- 文字列
- 時刻

データ収集データ ソースの `Collect(Value)` メソッドを使用して、収集のためにデータ ソースに値を渡すことができます。 このメソッドでは、`Value` 引数は、関連するデータ型のデータ ソース フィールドの定数または有効なパスです。

データ収集データ ソースの `Result` プロパティを使用して、収集される値の一覧にアクセスします。 このプロパティは、[レコード リスト](er-formula-supported-data-types-composite.md#record-list)を返します。 レコード リストのレコードには、収集された値にアクセスするために使用する `Value` フィールドが含まれます。

既定では、データ収集データ ソースは固有の値のみを収集します。

すべての値を収集するには、設定されたデータ収集データ ソースの **すべての値を収集** フィールドを、**はい** に設定します。 **すべての値を収集** フィールドが **はい** に設定されている場合は、パラメーター化された `Sum(Flag)` プロパティが使用可能になります。 このプロパティを使用すると、現在収集中のすべての値の合計を取得できます。 このプロパティでは、`Flag` 引数は合計値をリセットする必要があるかどうかを示す[ブール値](er-formula-supported-data-types-primitive.md#boolean)です。

- **False** 値を指定すると、以前に集計された金額から集計が継続されます。
- **True** 値を指定すると、新しい集計が開始されます。

現在、集計には次のデータ型がサポートされています。

- Int64
- 整数
- 実績

この機能の詳細を知るには、次の例を実行します。

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>例: データ収集データ ソースを使用した棚卸と集計を行うための電子申告形式の構成

この例は、システム管理者または電子申告機能コンサルタント ロールのユーザーが、実行中の合計を計算し、合計値を収集するために使用されるデータ収集データ ソースを含む電子申告形式を構成する方法を示しています。

この例の手順は、Microsoft Dynamics 365 Finance の USMF 社を使用して説明します。

### <a name="upload-and-use-the-provided-er-solution"></a>提供された ER ソリューションのアップロードと使用

1. [サンプル ER のコンフィギュレーションのインポート](er-defer-sequence-element.md#import-the-sample-er-configurations)。
2. [構成プロバイダーをアクティブにします](er-defer-sequence-element.md#activate-a-configurations-provider)。
3. [インポートされたモデル マッピングを確認します](er-defer-sequence-element.md#review-the-imported-model-mapping)。
4. [インポートされた形式を確認する](er-defer-sequence-element.md#review-the-imported-format)。
5. [インポートされた形式の実行](er-defer-sequence-element.md#run-the-imported-format)。

### <a name="run-the-format-of-the-provided-er-solution"></a>提供されている ER ソリューションの形式を実行する

1. **フォーマット デザイナー** ページで、**実行** を選択します。
2. **電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。
3. Web ブラウザーからファイルをダウンロードし、確認します。

    ![最初の形式の実行結果を含むダウンロード済ファイル](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>ER ソリューションの形式を変更して累計税額を計算する

トランザクション量が現在の例のボリュームよりも大きくなる場合、集計に要する時間が増加しパフォーマンスが低下する可能性があります。 形式の設定を変更することにより、パフォーマンスの問題を防ぐことができます。 税額にアクセスして生成されたレポートに含めることができるため、この情報を再利用して税額を合計することができます。

1. **形式デザイナー** ページの **マッピング** タブで、**ルートの追加** を選択します。
2. **データ ソースの追加** ダイアログ ボックスで、**機能** \> **データ収集** を選択します。
3. **データ収集データ ソース プロパティ** ダイアログ ボックスで、次の手順に従います。

    1. **名前** フィールドに、**CollectedTaxValues** と入力します。
    2. **品目タイプ** フィールドで、**実数** を選択します。
    3. **すべての値を収集** フィールドで、**はい** を選択します。
    4. **OK** を選択します。

4. **レポート\\明細行\\レコード\\TaxAmount** 数値形式要素を選択します。

    > [!NOTE]
    > 現在、`@.Value` バインディングは、この要素に対して構成されています。 `model.Data.List.Value` フィールドから税額が入力されている場合は、生成されたドキュメントです。

5. **式の編集** を選択します。
6. **フォーミュラ デザイナー** ページで、次の手順に従います。

    1. **式** フィールドで、`@.Value` を `CollectedTaxValues.Collect(@.Value)` に置き換えます。
    2. 変更を保存して、ページを閉じます。

    > [!NOTE]
    > 新しいバインディングは、生成されるドキュメントに同じ税額を渡します。 ただし、これらの値は、**CollectedTaxValues** データ ソースでも収集されます。

7. **レポート\\明細行\\レコード\\RunningTotal** 数値形式要素を選択します。
8. **式の編集** を選択します。
9. **フォーミュラ デザイナー** ページで、次の手順に従います。

    1. **式** フィールドに、`CollectedTaxValues.Sum(false)` と入力します。
    2. 変更を保存して、ページを閉じます。

    > [!NOTE]
    > 新しいバインディングは、生成されたドキュメントに、既に入力されている税額の合計額を渡します。

    ![形式デザイナー ページのバインディングを更新した数値要素](./media/er-data-collection-data-sources-02.png)

10. **保存** を選択して、**実行** を選択します。
11. **電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。
12. Web ブラウザーからファイルをダウンロードし、確認します。

    ![変更した形式の実行結果を含むダウンロード済ファイル](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>収集された税額一覧を評価するための形式を変更する

1. **形式デザイナー** ページの **形式** タブで、**レポート\\明細行\\レコード\\RunningTotal** の数値形式要素を選択し、次の手順を実行します。

    1. **数値タイプ** フィールドで、値を **実数** から **整数** に変更します。
    2. **数値形式** フィールドで、値を **F2** から **F0** に変更します。

3. **マッピング** タブで、**式の編集** を選択します。
4. **フォーミュラ デザイナー** ページで、次の手順に従います。

    1. **式** フィールドに、`COUNT(CollectedTaxValues.Result)` と入力します。
    2. 変更を保存して、ページを閉じます。

    > [!NOTE]
    > 新しいバインディングは、生成されたドキュメントに、収集された税額一覧にあるレコード数を渡します。

5. **保存** を選択して、**実行** を選択します。
6. **電子レポート パラメーター** ダイアログ ボックスで、**OK** を選択します。
7. Web ブラウザーからファイルをダウンロードし、確認します。

    ![別の変更した形式の実行結果を含むダウンロード済ファイル](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>累計を計算してデータを収集する必要がある場合、データ収集データ ソースを使用するの場合と組み込みのデータ収集関数を使用する場合の違いは何ですか?

データ収集データ ソースと組み込みの[データ収集](er-functions-category-data-collection.md)関数は、生成された送信ドキュメントに渡される情報に基づいて、データの収集、集計、および棚卸に使用できます。 ただし、使用する手法を決定する際には、次の点を考慮する必要があります。

| データ ソース | 組み込み関数 |
|-------------| ------------------ |
| 値だけが収集されます。 | <p>名前付きの値が収集されます。 したがって、個別の値グループの合計を計算できます。</p><p>また、グループを一覧として抽出することもできます。</p><p>テキスト値を収集することもできます。</p> |
| 固有の値は自動的に収集されます。 | 収集された値から固有値の一覧を抽出するには、追加の設定が必要です。 |
| パフォーマンスは、収集される値のボリュームにより異なります。 | 実際、パフォーマンスは、収集された値のボリュームに依存しません。 |
| この手法は、すべてのタイプの送信ドキュメントに対して機能します。 | この手法は、テキスト ドキュメントと XML ドキュメントに対してのみ機能します。 |

## <a name="additional-resources"></a>追加リソース

- [棚卸および集計を行うための形式のコンフィギュレーション](./tasks/er-format-counting-summing-1.md)
- [電子申告形式におけるシーケンス要素の実行の延期](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
