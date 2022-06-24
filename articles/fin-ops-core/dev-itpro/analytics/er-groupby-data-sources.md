---
title: GROUPBY データ ソースを使用したレコードのグループ化と集約計算
description: この記事では、電子申告 (ER) で GROUPBY 型のデータ ソースを使用する方法について説明します。
author: NickSelin
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b20b5db0794157560f27f15594a84083966642f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861790"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>GROUPBY データ ソースを使用したレコードのグループ化と集約計算

[!include[banner](../includes/banner.md)]

[電子申告 (ER)](general-electronic-reporting.md) モデル マッピングまたはフォーマットを構成するときに、**GroupBy** 型に必要なデータ ソースを [追加](#AddMmDataSource2) できます。

設計時に、**GroupBy** データ ソースは、次の要素を識別するように構成されます:

- 実行時にグループ化されるレコードを含む [基本データ ソース](#BaseDataSource)
- 実行時にレコードのグループ化に使用される基本データ ソースの [グループ化フィールド](#GroupingFields)
- 実行時に検出された各グループに対して行われる集計計算を指定する [集計関数](#AggregateFunctions)

実行時に、構成済の **GroupBy** データ ソースは、グループ化フィールドで同じ値を持つレコードをグループ化し、レコードの一覧を返します。 各レコードは、1 つのグループを表します。 各グループについて、データ ソースは、初期レコードがグループ化されたフィールド値、計算済集計関数の値、およびグループに属する基本データ ソースのレコードの一覧を公開します。

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>集計関数

実行時には、すべての集計計算がレコードのグループごとに行われます。 この計算は、**GroupBy** 型の編集可能なデータ ソースでグループ化に対して選択されたデータ ソースのレコード内の 1 つのフィールドまたは式の値を使用して行われます。 現在、次の集計関数がサポートされています:

- **AVG** – この関数は、グループ内の値の平均を返します。 数値フィールドでのみ使用できます。
- **COUNT** – この関数は、グループ内にある品目の数を返します。
- **Min** – この関数は、グループ内の値の中から最小値を返します。
- **Max** – この関数は、グループ内の値の中から最大値を返します。
- **SUM** – この関数は、グループ内のすべての値の合計を返します。 数値フィールドでのみ使用できます。

## <a name="execution-location"></a><a name="ExecutionLocation"></a>実行場所

**GroupBy** データ ソースを編集し、グループ化する必要があるレコードを含む基本データ ソースを指定すると、システムは、その **GroupBy** データ ソースの実行に最も効率的な [場所](#ExecutionLocation) を自動的に検出します。 基本データ ソースが [クエリ可能](er-functions-list-filter.md#usage-notes) である場合 (つまり、データベース レベルで実行できる場合)、アプリケーション データベースは、編集可能な **GroupBy** データ ソースの実行場所としても指定されます。 それ以外の場合は、アプリケーション サーバー メモリが実行場所として指定されます。

自動的に検出された実行場所は、構成済データ ソースに適用できる場所を選択して手動で変更できます。 選択した実行場所が [該当しない](er-components-inspections.md#i5) 場合、検証エラーが設計時にスローされます。

> [!TIP]
> データベースの場所を使用して、多数のレコードを公開するデータ ソースをグループ化することをお勧めします。

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>メモリ消費

既定では、**GroupBy** データ ソースがメモリ内で実行される場合、アプリケーション サーバー メモリは、検出された各グループに属する基本データ ソースのレコードを 1 つのグループのレコードとして格納するために使用されます。 集計関数のみを計算するように構成され、実行時にグループのレコードが使用されない場合、メモリー消費を削減するために、**GroupBy** データ ソースのレコード記憶域を抑制することができます。 この方法でメモリ消費を削減するには、**機能管理** ワークスペースで **レコードのグループ化を集約の計算のみに使用する場合は、ER のメモリ使用量を削減する** 機能を有効にします。

## <a name="alternatives"></a><a name="Alternatives"></a>代替

同様の集計は、データ ソースの [さまざまな](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) 型または ER の組み込み関数を使用して計算できます。

この機能の詳細を知るには、次の例を実行します。

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>例: 集約計算とレコードのグループ化に GROUPBY データ ソースを使用する

この例では、システム管理者または電子申告業務コンサルタント ロールのユーザーが、集計関数とグループ レコードの計算に使用される **GROUPBY** データ ソースを含む ER モデル マッピングを構成する方法を示します。 イントラスタット申告の生成時に、このモデル マッピングを使用して制御レポートを印刷します。 そのレポートでは、報告されたイントラスタット トランザクションを確認することができます。

この例の手順は、Microsoft Dynamics 365 Finance の **DEMF** 社を使用して説明します。 

### <a name="prepare-sample-data"></a>サンプル データの準備

**イントラスタット** ページに報告用のイントラスタット トランザクションがあることを確認します。 この例では、**Transport** フィールドでトランザクションをグループ化するため、異なる転送コードのトランザクションが必要です。

![イントラスタット ページでのイントラスタット トランザクションの準備。](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a> ER フレームワークを構成する

[ER フレームワークの構成](er-quick-start2-customize-report.md#ConfigureFramework)に記載の手順に従って、 ER パラメーターの最小限のセットを構成します。 ER フレームワークを使用して ER モデル マッピングを設計する前に、この設定を完了する必要があります。

### <a name="import-the-standard-er-format-configuration"></a>標準 ER フォーマットの構成をインポートする

[標準的な ER フォーマットの構成をインポートする](er-quick-start2-customize-report.md#ImportERSolution1) に記載の手順に従って、標準的な ER の構成を現在の Dynamics 365 Finance のインスタンスに追加します。 リポジトリから **イントラスタット モデル** 構成のバージョン 1 をインポートします。

### <a name="create-a-custom-data-model-configuration"></a>カスタム データ モデルの構成を作成する

[カスタム データ モデルの構成を追加する](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) の手順に従って、インポートされた **イントラスタット モデル** 構成から派生した新しい **イントラスタット モデル (Litware)** ER データ モデル構成を手動で追加します。

### <a name="configure-a-custom-data-model-component"></a>カスタム データ モデル コンポーネントを構成する

次の手順に従って、派生した **イントラスタット モデル (Litware)** データ モデルに必要な変更を行い、必要な詳細を持つ転送コードを公開できるようにします。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで **イントラスタット モデル (Litware)** を選択します。
3. **デザイナー** をクリックします。
4. **データ モデル デザイナー** ページのモデル ツリーで **イントラスタット** を選択します。
5. **新規** を選択して、選択した **イントラスタット** ノードに新しい入れ子になったノードを追加します。 データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. **Name** フィールドに **Transport** と入力します。
    2. **品目タイプ** フィールドで、**レコード リスト** を選択します。
    3. **追加** を選択して新しいノードを追加します。

6. **新規** を選択して、追加した **転送** ノードに新しい入れ子になったノードを追加します。 データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. **Name** フィールドに **Code** と入力します。
    2. **品目タイプ** フィールドで、**文字列** を選択します。
    3. **追加** を選択して新しいノードを追加します。

7. **新規** を選択して、**転送** ノードに別の新しい入れ子になったノードを追加します。 データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. **Name** フィールドに **TotalInvoicedAmount** と入力します。
    2. **品目タイプ** フィールドで、**実数** を選択します。
    3. **追加** を選択して新しいノードを追加します。

8. **新規** を選択して、**転送** ノードに別の新しい入れ子になったノードを追加します。 データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. **Name** フィールドに **NumberOfTransactions** と入力します。
    2. **項目タイプ** フィールドで、**整数** を選択します。
    3. **追加** を選択して新しいノードを追加します。

9. **新規** を選択して、**転送** ノードに別の新しい入れ子になったノードを追加します。 データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :

    1. **Name** フィールドに **Transaction** と入力します。
    2. **品目タイプ** フィールドで、**レコード リスト** を選択します。
    3. **追加** を選択して新しいノードを追加します。

10. 追加した **トランザクション** ノードの場合は、**ノード** FastTab で **品目参照の切り替え** を選択します。
11. **品目参照の切り替え** ダイアログ ボックスのデータ モデル ツリーで、**CommodityRecord** を選択します。 その後、**OK** を選択します。

![ER データ モデル デザイナーで構成されたデータ モデルです。](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>カスタム データ モデルの設計を完了する

[データ モデルの設計を完了する](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) の手順に従い、派生した **イントラスタット モデル (Litware)** データ モデルの設計を完了します。

### <a name="create-a-new-model-mapping-configuration"></a>新しいモデル マッピング構成を作成する

[新しいモデル マッピングの構成を作成する](er-quick-start1-new-solution.md#CreateModelMapping) の手順に従って、新しい **イントラスタットのサンプル マッピング** ER モデル マッピング構成を派生した **イントラスタット モデル (Litware)** の構成に手動で追加します。

### <a name="add-a-new-model-mapping-component"></a>新しいモデル マッピング コンポーネントを追加する

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページにある構成ツリーで **イントラスタット モデル** の構成を展開します。
3. **イントラスタットのサンプル マッピング** の構成を選択します。
4. **デザイナー** を選択して、マッピングの一覧を開きます。
5. 既存のマッピング コンポーネントを削除するには、**削除** を選択します。
6. **新規** を選択して、新しいマッピング コンポーネントを追加します。
7. **Definition** フィールドで、**Intrastat** を選択します。
8. **Name** フィールドに、**Intrastat mapping** と入力します。
9. **デザイナー** を選択して、新しいマッピングを構成します。

### <a name="design-the-added-model-mapping-component"></a>追加されたモデル マッピング コンポーネントを設計する

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>データ ソースを追加してアプリケーション テーブルにアクセスする

イントラスタット トランザクションの詳細を含むアプリケーション テーブルにアクセスするには、データ ソースを構成します。

1. **モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。
2. **データ ソース** ペインで **ルートの追加** を選択して、**イントラスタット** テーブルへのアクセスに使用する新しいデータ ソースを追加します。 **イントラスタット** テーブルの各レコードは、1 つのイントラスタット トランザクションを表します。
3. **データ ソース プロパティ** ダイアログ ボックスの **Name** フィールドに、**Transaction** と入力します。
4. **Table** フィールドに、**Intrastat** と入力します。
5. **OK** を選択して新しいデータ ソースを追加します。

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>イントラスタット トランザクションをグループ化するためにデータ ソースを追加する

**GroupBy** データ ソースを構成して、イントラスタット トランザクションをグループ化し、集計関数を計算します。

1. **モデル マッピング デザイナー** ページの **データ ソース型** ペインで、**関数\\グループ化** を選択します。
2. **データ ソース** ペインで **ルートの追加** を選択して、イントラスタット トランザクションのグループ化と集計関数の計算に使用する新しいデータ ソースを追加します。
3. **データ ソース プロパティ** ダイアログ ボックスの **Name** フィールドに、**TransportRecord** と入力します。
4. グループ条件を構成するには、**グループを編集** を選択します。
5. **'Group By' パラメーターの編集** ページの右ウィンドウにあるデータ ソースの一覧で、**トランザクション** データ ソースを選択して展開します。
6. **フィールドを追加 \> グループ化の対象** を選択して、**Transaction** データ ソースが、構成済の **GroupBy** データ ソースの <a name="BaseDataSource">基本データ ソース</a> として選択されていることを示します。 **Transaction** データ ソースのレコードがグループ化され、このデータ ソースのフィールド値が集計関数での計算に使用されます。
7. **Transaction\Transport** フィールドを選択し、**フィールドを追加 \> グループ化されたフィールド** を選択して、基本データ ソースの **Transport** フィールドが、構成済の **GroupBy** データ ソースの <a name="GroupingFields">グループ基準</a> として選択されていることを示します。 つまり、**Transaction** データ ソースのレコードは、**Transport** フィールドの値に基づいてグループ化されます。 構成済 **GroupBy** データ ソースのすべてのレコードは、基本データ ソースのレコード内にある 1 つの転送コードを表します。
8. **Transaction\AmountMST** フィールドを選択し、次の手順に従います:

    1. **フィールドを追加 \> 集計フィールド** を選択して、<a name="AggregateFunctions">集計関数</a> がこのフィールドに対して計算されることを示します。
    2. **集計** ペインで、選択した **Transaction\AmountMST** フィールドに対して追加されたレコードの **Method** フィールドで、**Sum** 関数を選択します。
    3. **Name** オプション フィールドに **TotalInvoicedAmount** と入力します。

    これらの設定では、各転送グループについて、**Transaction\AmountMST** フィールドの合計金額が計算されるように指定します。

9. **Transaction\RecId** フィールドを選択し、次の手順に従います:

    1. **フィールドを追加 \> 集計フィールド** を選択して、集計関数がこのフィールドに対して計算されることを示します。
    2. **集計** ペインで、選択した **Transaction\RecId** フィールドに対して追加されたレコードの **Method** フィールドで、**Count** 関数を選択します。
    3. **Name** オプション フィールドに **NumberOfTransactions** と入力します。

    これらの設定では、各転送グループについて、グループ内のトランザクション数が計算されるように指定します。

10. **保存** を選択します。
11. 編集可能なデータ ソースの <a name="ExecutionLocation">実行</a> パラメーターを確認します。 **Execution location** フィールドで **自動検出** が自動的に選択され、**Execution at** フィールドに値 **SQL** が含まれていることに注意してください。 これらの設定は、選択した **Transaction** 基本データ ソースが現在クエリ可能であることを指定し、編集可能な **GroupBy** データ ソースをデータベース レベルで実行できるようにします。
12. **Execution location** フィールドの検索を開き、使用可能な値の一覧を確認します。 **クエリ** または **メモリ内** を選択して、この **GroupBy** データ ソースをデータベース レベルまたはアプリケーション サーバー メモリで強制的に実行できます。
13. **保存** を選択して、**'Group By' パラメーターの編集** ページを閉じます。
14. **OK** を選択して、**GroupBy** データ ソースの設定を完了します。

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>GroupBy データ ソースをデータ モデル フィールドにバインドする

構成されたデータ ソースをデータ モデルのフィールドにバインドして、実行時にアプリケーション データでデータ モデルを入力する方法を指定します。

1. **モデル マッピング デザイナー** ページの **データ モデル** ペインで、**転送** ノードを展開します。
2. **データ ソース** ペインで、**TransportRecord** データ ソースを展開します。
3. 検出された転送グループの一覧を公開するためのバインドを追加します:

    1. **データ モデル** ペインで、**転送** 項目を選択します。
    2. **データ ソース** ペインで、**TransportRecord** データ ソースを選択します。
    3. **バインド** を選択します。

4. 検出された各転送グループの転送コードを公開するためのバインドを追加します:

    1. **Transport.Code** データ モデル項目を選択します。
    2. **TransportRecord.grouped.TransportMode** のグループ化されたフィールドを選択します。
    3. **バインド** を選択します。

5. 検出された各転送グループについて、計算された集計関数の値を公開するためのバインドを追加します。

    1. **Transport.NumberOfTransactions** データ モデル項目を選択します。
    2. **TransportRecord.aggregated.NumberOfTransactions** 集計フィールドを選択します。
    3. **バインド** を選択します。
    4. **Transport.TotalInvoicedAmount** データ モデル項目を選択します。
    5. **TransportRecord.aggregated.TotalInvoicedAmount** 集計フィールドを選択します。
    6. **バインド** を選択します。

6. 検出された各転送グループに属するトランザクション レコードを公開するためのバインドを追加します。

    1. **Transport.Transaction** データ モデル項目を選択します。
    2. **TransportRecord.lines** フィールドを選択します。
    3. **バインド** を選択します。

    **Transport.Transaction** データ モデル項目と **TransportRecord.lines** データ ソース フィールドの入れ子になった項目のバインドの構成を継続して、検出された各転送グループに属するイントラスタット トランザクションの詳細を実行時に公開できます。

![ER モデル マッピング デザイナーで構成されたモデル マッピングです。](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>追加されたモデル マッピング コンポーネントをデバッグする

[ER データソース デバッガー](er-debug-data-sources.md) を使用して、構成済モデル マッピングをテストします。

1. **モデル マッピング デザイナー** ページで **デバッグの開始** を選択します。
2. **デバッグ データソース** ページの左ペインで、**TransportRecord** データソースを選択し、**すべてのレコードの読み取り** を選択します。
3. **TransportRecord** データ ソースを展開し、新規を選択し、次の手順に従います:

    1. **TransportRecord.grouped.TransportMode** データ ソースを選択します。
    2. **値の取得** を選択します。
    3. **TransportRecord.grouped.NumberOfTransactions** データ ソースを選択します。
    4. **値の取得** を選択します。
    5. **TransportRecord.grouped.TotalInvoicedAmount** データ ソースを選択します。
    6. **値の取得** を選択します。

4. 右ペインで **すべて展開** を選択します。

**TransportRecord** データ ソースは 2 つのレコードを公開し、2 つの転送コードを表示します。 転送コードごとに、トランザクション数と請求金額の合計が計算されます。

> [!NOTE]
> データベース呼び出しを最適化するために **GroupBy** データ ソースが呼び出される場合は、"遅延読み取り" 手法が使用されます。 したがって、**GroupBy** データ ソースのフィールド値の一部は、データ モデル フィールドにバインドされている場合にのみ、ER データ ソース デバッガーで計算されます。

![デバッグ データソース ページでのデータ ソースデバッグの結果。](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>グループ合計を計算するときに、総計を計算する方法はありますか?

はい。 総計を計算するには、前に構成した **GroupBy** データ ソースが基本データ ソースとして使用されている別の **GroupBy** データ ソースを構成します。 次の図は、**GroupBy** 型の **TransportRecord** データ ソースの **SUM** 集計に基づいて、集計 **SUM** 関数の計算に使用される **GroupBy** 型の **Totals** データ ソースを示します。

![ER モデル マッピング デザイナーの Totals データ ソース。](./media/er-groupby-data-sources-configure-model-mapping2.png)

次の図は、**Totals** データ ソース デバッグの結果を示しています。

![デバッグ データソース ページでの Totals データ ソース デバッグの結果。](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>追加リソース

- [電子申告の概要](general-electronic-reporting.md)
- [実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する](er-debug-data-sources.md)
- [電子申告形式でのデータ収集データ ソースの使用](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
