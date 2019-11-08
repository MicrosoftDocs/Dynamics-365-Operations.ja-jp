---
title: 複数のアプリケーション テーブルからデータを取得するには、ER モデル マッピングで結合データ ソースを使用します。
description: このトピックでは、電子申告 (ER) で結合タイプのデータ ソースを使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 224acc19ee5dda430cd9471aa50e9d870a4f8c60
ms.sourcegitcommit: 564aa8eec89defdbe2abaf38d0ebc4cca3e28109
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2019
ms.locfileid: "2667957"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="65de9-103">電子申告 (ER) モデル マッピングで複数のアプリケーション テーブルからデータを取得するには、結合データ ソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="65de9-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="65de9-104">電子申告 (ER) モデル マッピングまたはフォーマットを構成する際、[追加](#review)することができるのは、**結合**タイプに必要なデータ ソースです。</span><span class="sxs-lookup"><span data-stu-id="65de9-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="65de9-105">デザイン時に、**結合**データ ソースは、それぞれレコードの一覧を返す複数のデータ ソースのセットとして構成されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="65de9-106">最初のデータ ソースを除くすべてのソースについて、現在のデータ ソースと以前のデータ ソースのレコードを結合するために必要な条件を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de9-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="65de9-107">実行時に、**結合**タイプの構成済みデータ ソースは、入れ子になったデータ ソースのレコードからフィールドを含むレコードの単一の結合リストを[返します](#executeERformat)。</span><span class="sxs-lookup"><span data-stu-id="65de9-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="65de9-108">次のタイプの結合が現在サポートされています:</span><span class="sxs-lookup"><span data-stu-id="65de9-108">The following type of joins are currently supported:</span></span>

- <span data-ttu-id="65de9-109">LEFT OUTER JOIN:</span><span class="sxs-lookup"><span data-stu-id="65de9-109">Outer (left) join:</span></span>
    - <span data-ttu-id="65de9-110">最初 (左端) のデータ ソースのレコードをすべて結合してから、設定された条件に従って、2 番目 (右端) のデータ ソースのレコードに一致するものをすべて結合します。</span><span class="sxs-lookup"><span data-stu-id="65de9-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="65de9-111">RIGHT INNER JOIN:</span><span class="sxs-lookup"><span data-stu-id="65de9-111">Inner (right) join:</span></span>
    - <span data-ttu-id="65de9-112">設定された条件に従って、互いに一致する最初 (左端) のデータ ソースのレコードのみ、および 2 番目 (右端) のデータ ソースのみを結合します。</span><span class="sxs-lookup"><span data-stu-id="65de9-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="65de9-113">構成済み**結合**データ ソースでは、すべてのデータ ソースが**テーブル レコード**タイプの場合は、結合データ ソースの実行は、単一の SQL ステートメントを使用して[データベース レベルで実行](#analyze) できます。</span><span class="sxs-lookup"><span data-stu-id="65de9-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="65de9-114">これにより、データベース呼び出しの数が減り、モデル マッピングのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="65de9-114">This reduces the number of database calls, which improves model mapping performance.</span></span> <span data-ttu-id="65de9-115">それ以外の場合、**結合データ**ソースはメモリ内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="65de9-116">結合タイプのデータ ソースで、レコードを結合するための条件を指定する ER 式で **VALUEIN** 関数を使用することは、まだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="65de9-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="65de9-117">この関数の詳細については、[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="65de9-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="65de9-118">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="65de9-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="65de9-119">例: ER モデル マッピングで結合データ ソースを使用する</span><span class="sxs-lookup"><span data-stu-id="65de9-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="65de9-120">次の手順では、システム管理者または電子申告開発者が、データ アクセスのパフォーマンスを向上させるために、**結合**タイプのデータ ソースを使用して、一度に複数のアプリケーション テーブルからデータを取得するように、電子申告 (ER) モデル マッピングを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="65de9-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="65de9-121">これらの手順は、Dynamics 365 Finance または Regulatory Configuration Services (RCS) のどの会社向けにも実行できます。</span><span class="sxs-lookup"><span data-stu-id="65de9-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="65de9-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="65de9-122">Prerequisites</span></span>

<span data-ttu-id="65de9-123">このトピックの例を実行するには、これらの手順を実行するために使用されているサービスに応じて、次のいずれかの方法にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de9-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="65de9-124">**次のいずれかのロールに対応する財務にアクセスします。**</span><span class="sxs-lookup"><span data-stu-id="65de9-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="65de9-125">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="65de9-125">Electronic reporting developer</span></span>
- <span data-ttu-id="65de9-126">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="65de9-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="65de9-127">システム管理者</span><span class="sxs-lookup"><span data-stu-id="65de9-127">System administrator</span></span>

<span data-ttu-id="65de9-128">**次のいずれかのロールに対応する RCS にアクセスします。**</span><span class="sxs-lookup"><span data-stu-id="65de9-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="65de9-129">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="65de9-129">Electronic reporting developer</span></span>
- <span data-ttu-id="65de9-130">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="65de9-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="65de9-131">システム管理者</span><span class="sxs-lookup"><span data-stu-id="65de9-131">System administrator</span></span>

<span data-ttu-id="65de9-132">また、まず[コンフィギュレーション プロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) にある手順を完了する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="65de9-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="65de9-133">事前に [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=000000) からダウンロードして、次のサンプル ER 構成ファイルをローカルに保存しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de9-133">In advance, you must also download from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) and save locally the following sample ER configuration files:</span></span>

| <span data-ttu-id="65de9-134">**コンテンツの説明**</span><span class="sxs-lookup"><span data-stu-id="65de9-134">**Content description**</span></span>  | <span data-ttu-id="65de9-135">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="65de9-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="65de9-136">データ ソースとして使用される、サンプル **ER データ モデル**構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="65de9-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="65de9-137">結合データ ソース version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="65de9-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="65de9-138">ER データ モデルを実行する、サンプル **ER モデル マッピング**構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="65de9-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="65de9-139">結合データ ソース version.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="65de9-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="65de9-140">サンプル **ER フォーマット**構成ファイル。</span><span class="sxs-lookup"><span data-stu-id="65de9-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="65de9-141">このファイルでは、例として ER フォーマット コンポーネントを設定するデータについて説明します。</span><span class="sxs-lookup"><span data-stu-id="65de9-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="65de9-142">結合データ ソース version.1.xml を知るためのフォーマット</span><span class="sxs-lookup"><span data-stu-id="65de9-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="65de9-143">コンフィギュレーション プロバイダーの有効化</span><span class="sxs-lookup"><span data-stu-id="65de9-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="65de9-144">Web ブラウザーの最初のセッションで、Finance または RCS にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="65de9-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="65de9-145">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65de9-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="65de9-146">**ローカライズのコンフィギュレーション**ページの**コンフィギュレーション プロバイダー**セクションで、Litware, Inc. (http://www.litware.com) サンプル会社のコンフィギュレーション プロバイダーが一覧に表示されていること、および**有効**とマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the Litware, Inc. (http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="65de9-147">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)手順のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="65de9-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![電子申告ワークスペース](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="65de9-149">サンプル ER 構成ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="65de9-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="65de9-150">**コンフィギュレーションをレポートする**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="65de9-151">ER データ モデルの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="65de9-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="65de9-152">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="65de9-153">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="65de9-154">**参照**を選択して、**結合データ ソース version.1.1.xml を知るためのモデル**ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="65de9-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="65de9-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-155">Select **OK**.</span></span>
3. <span data-ttu-id="65de9-156">ER モデル マッピングの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="65de9-156">Import the ER model mapping configuration file.</span></span>
    1. <span data-ttu-id="65de9-157">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="65de9-158">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="65de9-159">**参照**を選択して、**結合データ ソース version.1.1.xml を知るためのマッピング**ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="65de9-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="65de9-160">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-160">Select **OK**.</span></span>
4.  <span data-ttu-id="65de9-161">ER フォーマットの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="65de9-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="65de9-162">**交換**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="65de9-163">**XML ファイルから読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="65de9-164">**参照**を選択して、**結合データ ソース version.1.1.xml を知るためのフォーマット**ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="65de9-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="65de9-165">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-165">Select **OK**.</span></span>
5.  <span data-ttu-id="65de9-166">構成ツリーで、 **結合データ ソースを知るためのモデル**項目を、その他のモデル項目 (使用可能な場合) と同様に展開します。</span><span class="sxs-lookup"><span data-stu-id="65de9-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6.  <span data-ttu-id="65de9-167">**バージョン** クイック タブのバージョン詳細に加えて、ツリー内の ER 構成の一覧を確認します。これらはサンプル レポートのデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** fast tab – they will be used as the source of data for your sample report.</span></span>

    ![電子申告構成のページ](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="65de9-169">実行追跡オプションを有効にする</span><span class="sxs-lookup"><span data-stu-id="65de9-169">Turn on execution trace options</span></span>
1.  <span data-ttu-id="65de9-170">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-170">Select **CONFIGURATIONS**.</span></span>
2.  <span data-ttu-id="65de9-171">**ユーザー パラメーター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-171">Select **User parameters**.</span></span>
3.  <span data-ttu-id="65de9-172">次のスクリーンショットのように、実行追跡パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="65de9-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![電子申告のユーザー パラメーター ページ](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="65de9-174">これらのパラメーターを有効にすると、インポートされた ER フォーマット ファイルを実行するたびに、実行追跡が生成されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="65de9-175">生成された実行追跡の詳細を使用して、ER フォーマットと ER モデル マッピング コンポーネントの実行を分析できます。</span><span class="sxs-lookup"><span data-stu-id="65de9-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model mapping components.</span></span> <span data-ttu-id="65de9-176">ER 実行追跡機能についての詳細は、[ER 形式の実行を追跡してパフォーマンス問題をトラブルシュートする](trace-execution-er-troubleshoot-perf.md) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65de9-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="65de9-177">ER モデル マッピング (1) を確認する</span><span class="sxs-lookup"><span data-stu-id="65de9-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="65de9-178">ER モデル マッピング コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-178">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="65de9-179">このコンポーネントは、ER 構成のバージョンに関する情報、コンフィギュレーションの詳細、および**結合**タイプのデータ ソースを使用しないコンフィギュレーション プロバイダーの情報にアクセスできるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1.  <span data-ttu-id="65de9-180">**結合データ ソースを知るためのマッピング**コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2.  <span data-ttu-id="65de9-181">**デザイナー**を選択して、マッピングの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="65de9-181">Select **Designer** to open the list of mappings.</span></span>
3.  <span data-ttu-id="65de9-182">**デザイナー**を選択して、マッピングの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-182">Select **Designer** to review the mapping details.</span></span> 
4.  <span data-ttu-id="65de9-183">**詳細を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-183">Select **Show details**.</span></span>
5.  <span data-ttu-id="65de9-184">構成ツリーで、**Set1** および **Set1.Details** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="65de9-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="65de9-185">**Details: Record list = Versions**のバインドは、**Set1.Details** 項目が**バージョン**データ ソースにバインドされていて、**ERSolutionVersionTable** テーブルのレコードを返すことを示します。</span><span class="sxs-lookup"><span data-stu-id="65de9-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="65de9-186">このテーブルの各レコードは、ER コンフィギュレーションの 1 つのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="65de9-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="65de9-187">このテーブルの内容は、**バージョン**クイック タブ (**コンフィギュレーション**ページ) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-187">The content of this table is presented in the **Versions** fast tab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="65de9-188">**ConfigurationVersion: String = @.PublicVersionNumber** のバインドは、各 ER コンフィギュレーションのバージョンの公開バージョンの値が **PublicVersionNumber** フィールド (**ERSolutionVersionTable** テーブルの) から取得され、**ConfigurationVersion** 項目に配置されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="65de9-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="65de9-189">**ConfigurationTitle: String = @.'>Relations'.Solution.Name** のバインドは、ER コンフィギュレーションの名前が**名前**フィールド (**ERSolutionTable** テーブルの) から取得され、多対一の関係 (**> 関係**、**ERSolutionVersionTable** および **ERSolutionTable** テーブル間) を使用して評価することを示します。</span><span class="sxs-lookup"><span data-stu-id="65de9-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="65de9-190">現在のアプリケーション インスタンスの ER コンフィギュレーション名は、**コンフィギュレーション**ページの構成ツリーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="65de9-191">**@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** のバインドは、現在のコンフィギュレーションを所有するコンフィギュレーション プロバイダーの名前が、**名前**フィールド (**ERVendorTable** テーブルの) から取得され、多対一の関係 (**ERSolutionTable** および **ERVendorTable** テーブル間) を使用することで評価することを意味します。</span><span class="sxs-lookup"><span data-stu-id="65de9-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="65de9-192">ER コンフィギュレーション名は、各コンフィギュレーションのページ ヘッダーの、**コンフィギュレーション**ページの構成ツリーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="65de9-193">ER コンフィギュレーション プロバイダーの一覧全体は、**組織管理\>電子申告\>コンフィギュレーション プロバイダー**テーブルページにあります。</span><span class="sxs-lookup"><span data-stu-id="65de9-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set1Review.PNG)

6.  <span data-ttu-id="65de9-195">構成ツリーで、**Set1.Summary** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="65de9-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="65de9-196">**VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** は、**Set1.Summary.VersionsNumber** 項目が **VersionsNumber** アグリゲーション フィールドにバインドされていることを示します。これは **VersionsSummary** データ ソースの、**GroupBy** タイプで、**ERSolutionVersionTable** テーブルのレコード数を**バージョン**データ ソース経由で返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![GROUPBY データ ソース パラメーター ページ](./media/GER-JoinDS-Set1GroupByReview.PNG)

7.  <span data-ttu-id="65de9-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65de9-198">Close the page.</span></span>

### <a name="review"></a> <span data-ttu-id="65de9-199">ER モデル マッピング (2) を確認する</span><span class="sxs-lookup"><span data-stu-id="65de9-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="65de9-200">ER モデル マッピング コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-200">Review settings of the ER model mapping component.</span></span> <span data-ttu-id="65de9-201">このコンポーネントは、ER 構成のバージョンに関する情報、コンフィギュレーションの詳細、および**結合**タイプのデータ ソースを使用するコンフィギュレーション プロバイダーの情報にアクセスできるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1.  <span data-ttu-id="65de9-202">構成ツリーで、**Set2** および **Set2.Details** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="65de9-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="65de9-203">**Details: Record list = Details**のバインドは、**Set2.Details** 項目が**詳細**データ ソースにバインドされていることを示します。詳細データ ソースは**結合**タイプのデータ ソースとして構成されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-203">Note that the binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="65de9-205">**結合**データ ソースは、**Functions\Join** データ ソースを選択することによって追加できます。</span><span class="sxs-lookup"><span data-stu-id="65de9-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-AddJoinDS.PNG)

2.  <span data-ttu-id="65de9-207">**詳細**データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-207">Select **Detail**s data source.</span></span>
3.  <span data-ttu-id="65de9-208">**編集**を、**データ ソース**ウィンドウで選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-208">Select **Edit** in the **Data sources** pane.</span></span>
4.  <span data-ttu-id="65de9-209">**結合を編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-209">Select **Edit join**.</span></span>
5.  <span data-ttu-id="65de9-210">**詳細を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-210">Select **Show details**.</span></span>

    ![結合データ ソース パラメーター ページ](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="65de9-212">このページは、**結合タイプ**の必要なデータ ソースをデザインするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="65de9-213">このデータ ソースは、実行時に、**結合リスト**グリッドのデータ ソースから 1 つの結合されたレコード リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="65de9-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="65de9-214">レコードの結合は、グリッドで最初となる **ConfigurationProviders** データ ソースから始まります (**タイプ**列はそのために空白)。</span><span class="sxs-lookup"><span data-stu-id="65de9-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="65de9-215">したがって、他のすべてのデータ ソースのレコードは、このグリッドでの順序に基づいて、親データ ソースのレコードに結合されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="65de9-216">すべての結合データ ソースは、ターゲット データ ソース下で入れ子になったデータ ソースとして構成される必要があります (**1Versions** データ ソースは **1Configurations** 下で、**1Configurations** データ ソースは、**ConfigurationProviders** 下で入れ子になっています)。</span><span class="sxs-lookup"><span data-stu-id="65de9-216">Every joining data source must be configured as a data source nested under a target data source (**1Versions** data source is nested under **1Configurations** one; **1Configurations** data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="65de9-217">構成された各データ ソースには、結合の条件が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="65de9-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="65de9-218">この特定の**結合**データ ソースでは、次の結合が定義されています:</span><span class="sxs-lookup"><span data-stu-id="65de9-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="65de9-219">**ConfigurationProviders** データ ソース (**ERVendorTable** テーブル参照) の各レコードは、**1Configurations**(**ERSolutionTable** テーブル参照) のみに結合されます。**SolutionVendor** および **RecId** フィールドの値は同じになります。</span><span class="sxs-lookup"><span data-stu-id="65de9-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="65de9-220">**内部結合**タイプは、この結合に対して使用され、次の条件では、レコードの一致にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span> 

    <span data-ttu-id="65de9-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span><span class="sxs-lookup"><span data-stu-id="65de9-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="65de9-222">**1Configurations** データ ソース (**ERSolutionTable** テーブル参照) の各レコードは、**1Versions**(**ERSolutionVersionTable** テーブル参照) のみに結合されます。**Solution** および **RecId** フィールドの値は同じになります。</span><span class="sxs-lookup"><span data-stu-id="65de9-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="65de9-223">**内部結合**タイプは、この結合に対して使用され、次の条件では、レコードの一致にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="65de9-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span><span class="sxs-lookup"><span data-stu-id="65de9-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="65de9-225">**実行**オプションは、**クエリ**として構成され、この結合データ ソースは、SQL の直接呼び出しとしてデータベース レベルで実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="65de9-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="65de9-226">アプリケーション テーブルを表すデータ ソースのレコードを結合するには、これらのテーブル間で既存の AOT リレーションについて記述しているもの以外のフィールドのペアを使用して、結合条件を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="65de9-226">Note that for joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="65de9-227">この結合のタイプは、データベース レベルで実行するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="65de9-227">This type of join can be configured to execute at the database level as well.</span></span>

6.  <span data-ttu-id="65de9-228">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65de9-228">Close the page.</span></span>
7.  <span data-ttu-id="65de9-229">**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-229">Select **Cancel**.</span></span>
8.  <span data-ttu-id="65de9-230">構成ツリーで、**Set2.Summary** データ モデル項目を展開します:</span><span class="sxs-lookup"><span data-stu-id="65de9-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="65de9-231">**VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** は、**Set2.Summary.VersionsNumber** 項目が **VersionsNumber** アグリゲーション フィールドにバインドされていることを示します。これは **DetailsSummary** データ ソース (**GroupBy** タイプ) で、**詳細**データ ソース (**結合**タイプ) の結合されたレコードを返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="65de9-232">**実行**ロケーション オプションは、**クエリ**として構成され、この **GroupBy** データ ソースは、SQL の直接呼び出しとしてデータベース レベルで実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="65de9-232">Note that the **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be executed at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="65de9-233">これが可能なのは、**詳細** (**結合**タイプ) の基本データソースが、データベースレベルで実行されるように構成されているためです。</span><span class="sxs-lookup"><span data-stu-id="65de9-233">This is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![GROUPBY データ ソース パラメーター ページ](./media/GER-JoinDS-Set2GroupByReview.PNG)

9.  <span data-ttu-id="65de9-235">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65de9-235">Close the page.</span></span>
10. <span data-ttu-id="65de9-236">**キャンセル**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-236">Select **Cancel**.</span></span>

### <a name="executeERformat"></a><span data-ttu-id="65de9-237">ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="65de9-237">Execute ER format</span></span>

1.  <span data-ttu-id="65de9-238">最初のセッションと同じ資格情報と会社を使用して、Webブラウザーの 2 番目のセッションで Finance または RCS にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="65de9-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2.  <span data-ttu-id="65de9-239">**組織管理 \> 電子申告 \> コンフィギュレーション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65de9-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="65de9-240">**結合データ ソースを知るためのモデル**構成を展開します。</span><span class="sxs-lookup"><span data-stu-id="65de9-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4.  <span data-ttu-id="65de9-241">**結合データ ソースを知るための形式**構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5.  <span data-ttu-id="65de9-242">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65de9-242">Select **Designer**.</span></span>
6.  <span data-ttu-id="65de9-243">**詳細を表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-243">Select **Show details**.</span></span>
7.  <span data-ttu-id="65de9-244">**マッピング**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-244">Select **Mapping**.</span></span>
8.  <span data-ttu-id="65de9-245">**展開 / 折りたたみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="65de9-246">この形式は、ER コンフィギュレーション のバージョン (**バージョン**順序) ごとに、生成されたテキスト ファイルに新しい行を挿入するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="65de9-246">Note that this format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="65de9-247">生成される各行には、現在のコンフィギュレーションを所有するコンフィギュレーション プロバイダー名、コンフィギュレーション名、およびセミコロン記号で区切られたコンフィギュレーション バージョンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="65de9-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="65de9-248">生成されるファイルの最終行には、ER コンフィギュレーションの検出されたバージョン数が含まれます (**集計**シーケンス) 。</span><span class="sxs-lookup"><span data-stu-id="65de9-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![ER 形式デザイナーのページ](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="65de9-250">**データ**および**集計**データ ソースは、生成されたファイルにコンフィギュレーション バージョンの詳細を設定するために使用されます:</span><span class="sxs-lookup"><span data-stu-id="65de9-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="65de9-251">**Set1** データ モデルの情報は、ER 形式実行時に、ユーザー ダイアログ ページで**いいえ**を**セレクター**データ ソースに対して選択する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="65de9-252">**Set2** データ モデルの情報は、ユーザー ダイアログ ページで**はい**を**セレクター**データ ソースに対して選択する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![ER 形式デザイナーのページ](./media/GER-JoinDS-FormatMappingReview.PNG)

9.  <span data-ttu-id="65de9-254">**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-254">Select **Run**.</span></span>
10. <span data-ttu-id="65de9-255">ダイアログ ページで、**いいえ**を**結合データ ソースの使用**フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="65de9-256">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-256">Select **OK**.</span></span>
12. <span data-ttu-id="65de9-257">生成されたファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-257">Review generated file.</span></span>

    ![ER ユーザー ダイアログ ページ](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="65de9-259">ER 形式実行追跡の分析</span><span class="sxs-lookup"><span data-stu-id="65de9-259">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="65de9-260">Finance または RCS の最初のセッションで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="65de9-261">**パフォーマンスの追跡**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-261">Select **Performance trac**e.</span></span>
3.  <span data-ttu-id="65de9-262">**パフォーマンスの追跡**グリッドで、現在のモデル マッピング コンポーネントを使用した ER 形式の、最新の実行追跡の最上位レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="65de9-263">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-263">Select **OK**.</span></span>

    <span data-ttu-id="65de9-264">実行の統計は、アプリケーション テーブルへの重複した呼び出しについて通知します。</span><span class="sxs-lookup"><span data-stu-id="65de9-264">Note that execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="65de9-265">**ERSolutionTable** は、**ERSolutionVersionTable** テーブルに含まれるコンフィギュレーション バージョン レコードの数だけ呼び出されますが、そのような呼び出しの数はパフォーマンス向上のため、所用時間が減ることがあります。</span><span class="sxs-lookup"><span data-stu-id="65de9-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="65de9-266">**ERVendorTable** は、**ERSolutionVersionTable** テーブルで検出されるコンフィギュレーション バージョン レコードの 2 倍呼び出されますが、そのような呼び出しの数も減ることがあります。</span><span class="sxs-lookup"><span data-stu-id="65de9-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set1Run2.PNG)

5.  <span data-ttu-id="65de9-268">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="65de9-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="65de9-269">ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="65de9-269">Execute ER format</span></span>

1.  <span data-ttu-id="65de9-270">Finance または RCS の 2 番目のセッションを使用して、Web ブラウザー タブに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="65de9-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2.  <span data-ttu-id="65de9-271">**実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-271">Select **Run**.</span></span>
3.  <span data-ttu-id="65de9-272">ダイアログ ページで、**はい**を**結合データ ソースの使用**フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4.  <span data-ttu-id="65de9-273">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-273">Select **OK**.</span></span>
5.  <span data-ttu-id="65de9-274">生成されたファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="65de9-274">Review generated file.</span></span>

    ![ER ユーザー ダイアログ ページ](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze"></a> <span data-ttu-id="65de9-276">ER 形式実行追跡の分析</span><span class="sxs-lookup"><span data-stu-id="65de9-276">Analyze ER format execution trace</span></span>

1.  <span data-ttu-id="65de9-277">Finance または RCS の最初のセッションで、**デザイナー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2.  <span data-ttu-id="65de9-278">**パフォーマンスの追跡**を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-278">Select **Performance trace**.</span></span>
3.  <span data-ttu-id="65de9-279">**パフォーマンスの追跡**グリッドで、現在のモデル マッピング コンポーネントを使用した ER 形式の、最新の実行追跡を表す最上位レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4.  <span data-ttu-id="65de9-280">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65de9-280">Select **OK**.</span></span>

    <span data-ttu-id="65de9-281">実行の統計は、次の情報を通知します:</span><span class="sxs-lookup"><span data-stu-id="65de9-281">Note that execution statistics informs you about the following:</span></span>

    - <span data-ttu-id="65de9-282">必須フィールドにアクセスする、**ERVendorTable**、**ERSolutionTable**、および **ERSolutionVersionTable** テーブルからレコードを取得するため、アプリケーション データベースが 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="65de9-284">**詳細**データ ソースで構成された結合を使用して、コンフィギュレーション バージョン数を計算するのに、アプリケーション データベースが 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="65de9-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="additional-resources"></a><span data-ttu-id="65de9-286">追加リソース</span><span class="sxs-lookup"><span data-stu-id="65de9-286">Additional resources</span></span>

[<span data-ttu-id="65de9-287">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="65de9-287">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="65de9-288">パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行</span><span class="sxs-lookup"><span data-stu-id="65de9-288">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)

