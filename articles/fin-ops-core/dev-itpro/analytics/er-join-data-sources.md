---
title: 複数のアプリケーション テーブルからデータを取得するには、ER モデル マッピングで結合データ ソースを使用します。
description: このトピックでは、電子申告 (ER) で結合タイプのデータ ソースを使用する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-03-01
ms.dyn365.ops.version: Release 10.0.1
ms.openlocfilehash: 0d7df12026d6d668b1f48a48cd12bf4b12e0f94e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686419"
---
# <a name="use-join-data-sources-to-get-data-from-multiple-application-tables-in-electronic-reporting-er-model-mappings"></a><span data-ttu-id="48585-103">電子申告 (ER) モデル マッピングで複数のアプリケーション テーブルからデータを取得するには、結合データ ソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="48585-103">Use JOIN data sources to get data from multiple application tables in Electronic reporting (ER) model mappings</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="48585-104">電子申告 (ER) モデル マッピングまたはフォーマットを構成する際、[追加](#review)することができるのは、**結合** タイプに必要なデータ ソースです。</span><span class="sxs-lookup"><span data-stu-id="48585-104">While configuring Electronic reporting (ER) model mappings or formats, you can [add](#review) required data sources of the **Join** type.</span></span> <span data-ttu-id="48585-105">デザイン時に、**結合** データ ソースは、それぞれレコードの一覧を返す複数のデータ ソースのセットとして構成されます。</span><span class="sxs-lookup"><span data-stu-id="48585-105">At design time, a **Join** data source is configured as a set of several data sources each of which returns a list of records.</span></span> <span data-ttu-id="48585-106">最初のデータ ソースを除くすべてのソースについて、現在のデータ ソースと以前のデータ ソースのレコードを結合するために必要な条件を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48585-106">For every data source except the first one, you need to define necessary conditions to join records of the current and previous data sources.</span></span> <span data-ttu-id="48585-107">実行時に、**結合** タイプの構成済みデータ ソースは、入れ子になったデータ ソースのレコードからフィールドを含むレコードの単一の結合リストを[返します](#executeERformat)。</span><span class="sxs-lookup"><span data-stu-id="48585-107">At runtime, a configured data source of **Join** type [returns](#executeERformat) a single joined list of records containing fields from the records of nested data sources.</span></span>

<span data-ttu-id="48585-108">次のタイプの結合が現在サポートされています:</span><span class="sxs-lookup"><span data-stu-id="48585-108">The following types of joins are currently supported:</span></span>

- <span data-ttu-id="48585-109">LEFT OUTER JOIN:</span><span class="sxs-lookup"><span data-stu-id="48585-109">Outer (left) join:</span></span>
    - <span data-ttu-id="48585-110">最初 (左端) のデータ ソースのレコードをすべて結合してから、設定された条件に従って、2 番目 (右端) のデータ ソースのレコードに一致するものをすべて結合します。</span><span class="sxs-lookup"><span data-stu-id="48585-110">Join all records of the first (left-most) data source and then any matching in accordance to configured conditions records of the second (right-most) data source.</span></span>
- <span data-ttu-id="48585-111">RIGHT INNER JOIN:</span><span class="sxs-lookup"><span data-stu-id="48585-111">Inner (right) join:</span></span>
    - <span data-ttu-id="48585-112">設定された条件に従って、互いに一致する最初 (左端) のデータ ソースのレコードのみ、および 2 番目 (右端) のデータ ソースのみを結合します。</span><span class="sxs-lookup"><span data-stu-id="48585-112">Join only records of the first (left-most) data source and only records of the second (right-most) data source matching to each other in accordance to configured conditions.</span></span>

<span data-ttu-id="48585-113">構成済み **結合** データ ソースでは、すべてのデータ ソースが **テーブル レコード** タイプの場合は、結合データ ソースの実行は、単一の SQL ステートメントを使用して[データベース レベルで実行](#analyze) できます。</span><span class="sxs-lookup"><span data-stu-id="48585-113">In the configured **Join** data source, when all data sources are the **Table records** type, execution of the Join data source can be [performed at the database level](#analyze) using a single SQL statement.</span></span> <span data-ttu-id="48585-114">このステートメントは、データベース呼び出しの回数を減らし、モデル マッピングのパフォーマンスを向上させます。</span><span class="sxs-lookup"><span data-stu-id="48585-114">This statement reduces the number of database calls, which improves model-mapping performance.</span></span> <span data-ttu-id="48585-115">それ以外の場合、**結合データ** ソースはメモリ内で実行されます。</span><span class="sxs-lookup"><span data-stu-id="48585-115">Otherwise, execution of **Join data** source is performed in memory.</span></span>

> [!NOTE]
> <span data-ttu-id="48585-116">結合タイプのデータ ソースで、レコードを結合するための条件を指定する ER 式で **VALUEIN** 関数を使用することは、まだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="48585-116">Using the **VALUEIN** function in ER expressions that specify conditions for joining records in data sources of Join type is not supported yet.</span></span> <span data-ttu-id="48585-117">この関数の詳細については、[電子申告のフォーミュラ デザイナー](general-electronic-reporting-formula-designer.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48585-117">Visit the [Formula designer in Electronic reporting](general-electronic-reporting-formula-designer.md) page for more details about this function.</span></span>

<span data-ttu-id="48585-118">この機能の詳細を知るには、このトピックの例を実行します。</span><span class="sxs-lookup"><span data-stu-id="48585-118">To learn more about this feature, complete the example in this topic.</span></span>

## <a name="example-use-join-data-sources-in-er-model-mappings"></a><span data-ttu-id="48585-119">例: ER モデル マッピングで結合データ ソースを使用する</span><span class="sxs-lookup"><span data-stu-id="48585-119">Example: Use JOIN data sources in ER model mappings</span></span>

<span data-ttu-id="48585-120">次の手順では、システム管理者または電子申告開発者が、データ アクセスのパフォーマンスを向上させるために、**結合** タイプのデータ ソースを使用して、一度に複数のアプリケーション テーブルからデータを取得するように、電子申告 (ER) モデル マッピングを構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="48585-120">The following steps explain how the System administrator or Electronic reporting developer can configure an Electronic reporting (ER) model mapping to get data from multiple application tables at once by using data sources of the **Join** type to improve data access performance.</span></span> <span data-ttu-id="48585-121">これらの手順は、Dynamics 365 Finance または Regulatory Configuration Services (RCS) のどの会社向けにも実行できます。</span><span class="sxs-lookup"><span data-stu-id="48585-121">These steps can be performed for any company of Dynamics 365 Finance or Regulatory Configuration Services (RCS).</span></span>

### <a name="prerequisites"></a><span data-ttu-id="48585-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="48585-122">Prerequisites</span></span>

<span data-ttu-id="48585-123">このトピックの例を実行するには、これらの手順を実行するために使用されているサービスに応じて、次のいずれかの方法にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="48585-123">To complete the examples in this topic, you must have access to one of the following depending on what service is used to compete these steps:</span></span>

<span data-ttu-id="48585-124">**次のいずれかのロールに対応する財務にアクセスします。**</span><span class="sxs-lookup"><span data-stu-id="48585-124">**Access to Finance for one of the following roles:**</span></span>

- <span data-ttu-id="48585-125">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="48585-125">Electronic reporting developer</span></span>
- <span data-ttu-id="48585-126">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="48585-126">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="48585-127">システム管理者</span><span class="sxs-lookup"><span data-stu-id="48585-127">System administrator</span></span>

<span data-ttu-id="48585-128">**次のいずれかのロールに対応する RCS にアクセスします。**</span><span class="sxs-lookup"><span data-stu-id="48585-128">**Access to RCS for one of the following roles:**</span></span>

- <span data-ttu-id="48585-129">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="48585-129">Electronic reporting developer</span></span>
- <span data-ttu-id="48585-130">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="48585-130">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="48585-131">システム管理者</span><span class="sxs-lookup"><span data-stu-id="48585-131">System administrator</span></span>

<span data-ttu-id="48585-132">また、まず[コンフィギュレーション プロバイダーを作成し、それを有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) にある手順を完了する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="48585-132">You also must first complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

<span data-ttu-id="48585-133">事前に [Microsoft ダウンロード センター](https://go.microsoft.com/fwlink/?linkid=000000) からダウンロードして、次のサンプル ER 構成ファイルをローカルに保存しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="48585-133">In advance, you must also download from [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=000000) and save locally the following sample ER configuration files:</span></span>

| <span data-ttu-id="48585-134">**コンテンツの説明**</span><span class="sxs-lookup"><span data-stu-id="48585-134">**Content description**</span></span>  | <span data-ttu-id="48585-135">**ファイル名**</span><span class="sxs-lookup"><span data-stu-id="48585-135">**File name**</span></span>   |
|--------------------------|-----------------|
| <span data-ttu-id="48585-136">データ ソースとして使用される、サンプル **ER データ モデル** 構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="48585-136">Sample **ER data model** configuration file, which is used as the data source for the examples.</span></span>| [<span data-ttu-id="48585-137">結合データ ソース version.1.xml を知るためのモデル</span><span class="sxs-lookup"><span data-stu-id="48585-137">Model to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="48585-138">ER データ モデルを実行する、サンプル **ER モデル マッピング** 構成ファイルの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="48585-138">Sample **ER model mapping** configuration file, which implements the ER data model for the examples.</span></span> | [<span data-ttu-id="48585-139">結合データ ソース version.1.xml を知るためのマッピング</span><span class="sxs-lookup"><span data-stu-id="48585-139">Mapping to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="48585-140">サンプル **ER フォーマット** 構成ファイル。</span><span class="sxs-lookup"><span data-stu-id="48585-140">Sample **ER format** configuration file.</span></span> <span data-ttu-id="48585-141">このファイルでは、例として ER フォーマット コンポーネントを設定するデータについて説明します。</span><span class="sxs-lookup"><span data-stu-id="48585-141">This file describes the data to populate the ER format component for the examples.</span></span> | [<span data-ttu-id="48585-142">結合データ ソース version.1.xml を知るためのフォーマット</span><span class="sxs-lookup"><span data-stu-id="48585-142">Format to learn JOIN data sources.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="activate-a-configurations-provider"></a><span data-ttu-id="48585-143">コンフィギュレーション プロバイダーの有効化</span><span class="sxs-lookup"><span data-stu-id="48585-143">Activate a configurations provider</span></span>

1. <span data-ttu-id="48585-144">Web ブラウザーの最初のセッションで、Finance または RCS にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="48585-144">Access either Finance or RCS in the first session of your web browser.</span></span>
2. <span data-ttu-id="48585-145">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48585-145">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
3. <span data-ttu-id="48585-146">**ローカライズ構成** ページの **構成プロバイダー** セクションで、[Litware, Inc.](http://www.litware.com) サンプル会社の構成プロバイダーが一覧に表示されていること、および **有効** とマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-146">On the **Localization configurations** page, in the **Configuration providers** section, make sure that the configuration provider for the [Litware, Inc.](http://www.litware.com) sample company is listed, and that it's marked as **Active**.</span></span> <span data-ttu-id="48585-147">このコンフィギュレーション プロバイダーが表示されない場合は、[コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け](tasks/er-configuration-provider-mark-it-active-2016-11.md)手順のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="48585-147">If you don't see this configuration provider, follow the steps in [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>

    ![電子申告ワークスペース](./media/GER-JoinDS-ActiveProvider.PNG)

### <a name="import-sample-er-configuration-files"></a><span data-ttu-id="48585-149">サンプル ER 構成ファイルのインポート</span><span class="sxs-lookup"><span data-stu-id="48585-149">Import sample ER configuration files</span></span>

1. <span data-ttu-id="48585-150">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-150">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="48585-151">ER データ モデルの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="48585-151">Import the ER data model configuration file.</span></span>
    1. <span data-ttu-id="48585-152">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-152">Select **Exchange**.</span></span>
    2. <span data-ttu-id="48585-153">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-153">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48585-154">**参照** を選択して、**結合データ ソース version.1.1.xml を知るためのモデル** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="48585-154">Select **Browse** to find the **Model to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="48585-155">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-155">Select **OK**.</span></span>
3. <span data-ttu-id="48585-156">ER モデル マッピングの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="48585-156">Import the ER model-mapping configuration file.</span></span>
    1. <span data-ttu-id="48585-157">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-157">Select **Exchange**.</span></span>
    2. <span data-ttu-id="48585-158">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-158">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48585-159">**参照** を選択して、**結合データ ソース version.1.1.xml を知るためのマッピング** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="48585-159">Select **Browse** to find the **Mapping to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="48585-160">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-160">Select **OK**.</span></span>
4. <span data-ttu-id="48585-161">ER フォーマットの構成ファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="48585-161">Import the ER format configuration file.</span></span>
    1. <span data-ttu-id="48585-162">**交換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-162">Select **Exchange**.</span></span>
    2. <span data-ttu-id="48585-163">**XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-163">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="48585-164">**参照** を選択して、**結合データ ソース version.1.1.xml を知るためのフォーマット** ファイルを見つけます。</span><span class="sxs-lookup"><span data-stu-id="48585-164">Select **Browse** to find the **Format to learn JOIN data sources.version.1.1.xml** file.</span></span>
    4. <span data-ttu-id="48585-165">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-165">Select **OK**.</span></span>
5. <span data-ttu-id="48585-166">構成ツリーで、 **結合データ ソースを知るためのモデル** 項目を、その他のモデル項目 (使用可能な場合) と同様に展開します。</span><span class="sxs-lookup"><span data-stu-id="48585-166">In the configurations tree, expand the **Model to learn JOIN data sources** item as well as other model items (when available).</span></span>
6. <span data-ttu-id="48585-167">**バージョン** クイック タブのバージョン詳細に加えて、ツリー内の ER 構成の一覧を確認します。これらはサンプル レポートのデータ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-167">Observe the list of ER configurations in the tree as well as version details on the **Versions** fast tab – they will be used as the source of data for your sample report.</span></span>

    ![電子申告構成のページ](./media/GER-JoinDS-ConfigurationsTree.PNG)

### <a name="turn-on-execution-trace-options"></a><span data-ttu-id="48585-169">実行追跡オプションを有効にする</span><span class="sxs-lookup"><span data-stu-id="48585-169">Turn on execution trace options</span></span>

1. <span data-ttu-id="48585-170">**コンフィギュレーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-170">Select **CONFIGURATIONS**.</span></span>
2. <span data-ttu-id="48585-171">**ユーザー パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-171">Select **User parameters**.</span></span>
3. <span data-ttu-id="48585-172">次のスクリーンショットのように、実行追跡パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="48585-172">Set execution trace parameters as shown on the screenshot below.</span></span>

    ![電子申告のユーザー パラメーター ページ](./media/GER-JoinDS-Parameters.PNG)

    <span data-ttu-id="48585-174">これらのパラメーターを有効にすると、インポートされた ER フォーマット ファイルを実行するたびに、実行追跡が生成されます。</span><span class="sxs-lookup"><span data-stu-id="48585-174">With these parameters turned on, for every execution of the imported ER format file, the execution trace will be generated.</span></span> <span data-ttu-id="48585-175">生成された実行追跡の詳細を使用して、ER 形式と ER モデル マッピング コンポーネントの実行を分析できます。</span><span class="sxs-lookup"><span data-stu-id="48585-175">Using details of generated execution trace, you can analyze the execution of ER format and ER model-mapping components.</span></span> <span data-ttu-id="48585-176">ER 実行追跡機能についての詳細は、[ER 形式の実行を追跡してパフォーマンス問題をトラブルシュートする](trace-execution-er-troubleshoot-perf.md) ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="48585-176">Visit the [Trace execution of ER format to troubleshoot performance issues](trace-execution-er-troubleshoot-perf.md) page for more details about ER execution trace feature.</span></span>

### <a name="review-er-model-mapping-part-1"></a><span data-ttu-id="48585-177">ER モデル マッピング (1) を確認する</span><span class="sxs-lookup"><span data-stu-id="48585-177">Review ER model mapping (part 1)</span></span>

<span data-ttu-id="48585-178">ER モデル マッピング コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-178">Review settings of the ER model-mapping component.</span></span> <span data-ttu-id="48585-179">このコンポーネントは、ER 構成のバージョンに関する情報、コンフィギュレーションの詳細、および **結合** タイプのデータ ソースを使用しないコンフィギュレーション プロバイダーの情報にアクセスできるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="48585-179">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers without using data sources of the **Join** type.</span></span>

1. <span data-ttu-id="48585-180">**結合データ ソースを知るためのマッピング** コンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-180">Select **Mapping to learn JOIN data sources** configuration.</span></span>
2. <span data-ttu-id="48585-181">**デザイナー** を選択して、マッピングの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="48585-181">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="48585-182">**デザイナー** を選択して、マッピングの詳細を確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-182">Select **Designer** to review the mapping details.</span></span>
4. <span data-ttu-id="48585-183">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-183">Select **Show details**.</span></span>
5. <span data-ttu-id="48585-184">構成ツリーで、**Set1** および **Set1.Details** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="48585-184">In the configurations tree, expand the **Set1** and **Set1.Details** data model items:</span></span>

    1. <span data-ttu-id="48585-185">**Details: Record list = Versions** のバインドは、**Set1.Details** 項目が **バージョン** データ ソースにバインドされていて、**ERSolutionVersionTable** テーブルのレコードを返すことを示します。</span><span class="sxs-lookup"><span data-stu-id="48585-185">Binding **Details: Record list = Versions** indicates that the **Set1.Details** item is bound to the **Versions** data source returning records of the **ERSolutionVersionTable** table.</span></span> <span data-ttu-id="48585-186">このテーブルの各レコードは、ER コンフィギュレーションの 1 つのバージョンを表します。</span><span class="sxs-lookup"><span data-stu-id="48585-186">Each record of this table represents a single version of an ER configuration.</span></span> <span data-ttu-id="48585-187">このテーブルの内容は、**バージョン** クイック タブ (**コンフィギュレーション** ページ) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="48585-187">The content of this table is presented in the **Versions** fast tab on the **Configurations** page.</span></span>
    2. <span data-ttu-id="48585-188">**ConfigurationVersion: String = @.PublicVersionNumber** のバインドは、各 ER コンフィギュレーションのバージョンの公開バージョンの値が **PublicVersionNumber** フィールド (**ERSolutionVersionTable** テーブルの) から取得され、**ConfigurationVersion** 項目に配置されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="48585-188">Binding **ConfigurationVersion: String = @.PublicVersionNumber** means that the value of the public version of each ER configuration’s version is taken from the **PublicVersionNumber** field of the **ERSolutionVersionTable** table and placed to the **ConfigurationVersion** item.</span></span>
    3. <span data-ttu-id="48585-189">**ConfigurationTitle: String = @.'>Relations'.Solution.Name** のバインドは、ER コンフィギュレーションの名前が **名前** フィールド (**ERSolutionTable** テーブルの) から取得され、多対一の関係 (**> 関係**、**ERSolutionVersionTable** および **ERSolutionTable** テーブル間) を使用して評価することを示します。</span><span class="sxs-lookup"><span data-stu-id="48585-189">Binding **ConfigurationTitle: String = @.'>Relations'.Solution.Name** indicates that the name of an ER configuration is taken from the **Name** field of the **ERSolutionTable** table assessing by using the many-to-one relation (**'>Relations'**) between the **ERSolutionVersionTable** and **ERSolutionTable** tables.</span></span> <span data-ttu-id="48585-190">現在のアプリケーション インスタンスの ER コンフィギュレーション名は、**コンフィギュレーション** ページの構成ツリーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="48585-190">Names of ER configurations of the current application instance are presented in the configurations tree on the **Configurations** page.</span></span>
    4. <span data-ttu-id="48585-191">**@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** のバインドは、現在のコンフィギュレーションを所有するコンフィギュレーション プロバイダーの名前が、**名前** フィールド (**ERVendorTable** テーブルの) から取得され、多対一の関係 (**ERSolutionTable** および **ERVendorTable** テーブル間) を使用することで評価することを意味します。</span><span class="sxs-lookup"><span data-stu-id="48585-191">Binding **@.'>Relations'.Solution.'>Relations'.SolutionVendor.Name** means that the name of the configuration provider that owns the current configuration is taken from the **Name** field of the **ERVendorTable** table assessing by using the many-to-one relation between **ERSolutionTable** and **ERVendorTable** tables.</span></span> <span data-ttu-id="48585-192">ER コンフィギュレーション名は、各コンフィギュレーションのページ ヘッダーの、**コンフィギュレーション** ページの構成ツリーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="48585-192">Names of ER configuration providers are presented in the configurations tree on the **Configurations** page on the page header for each configuration.</span></span> <span data-ttu-id="48585-193">ER コンフィギュレーション プロバイダーの一覧全体は、**組織管理\>電子申告\>コンフィギュレーション プロバイダー** テーブルページにあります。</span><span class="sxs-lookup"><span data-stu-id="48585-193">The entire list of ER configuration providers can be found on the **Organization administration \> Electronic reporting \> Configuration provider** table page.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set1Review.PNG)

6. <span data-ttu-id="48585-195">構成ツリーで、**Set1.Summary** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="48585-195">In the configurations tree, expand the **Set1.Summary** data model item:</span></span>

    1. <span data-ttu-id="48585-196">**VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** は、**Set1.Summary.VersionsNumber** 項目が **VersionsNumber** アグリゲーション フィールドにバインドされていることを示します。これは **VersionsSummary** データ ソースの、**GroupBy** タイプで、**ERSolutionVersionTable** テーブルのレコード数を **バージョン** データ ソース経由で返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="48585-196">Binding **VersionsNumber: Integer = VersionsSummary.aggregated.VersionsNumber** indicates that the **Set1.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **VersionsSummary** data source of the **GroupBy** type that was configured to return the number of records of the **ERSolutionVersionTable** table via the **Versions** data source.</span></span>

    ![GROUPBY データ ソース パラメーター ページ](./media/GER-JoinDS-Set1GroupByReview.PNG)

7. <span data-ttu-id="48585-198">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48585-198">Close the page.</span></span>

### <a name="review-er-model-mapping-part-2"></a><a name="review"></a> <span data-ttu-id="48585-199">ER モデル マッピング (2) を確認する</span><span class="sxs-lookup"><span data-stu-id="48585-199">Review ER model mapping (part 2)</span></span>

<span data-ttu-id="48585-200">ER モデル マッピング コンポーネントの設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-200">Review settings of the ER model-mapping component.</span></span> <span data-ttu-id="48585-201">このコンポーネントは、ER 構成のバージョンに関する情報、コンフィギュレーションの詳細、および **結合** タイプのデータ ソースを使用するコンフィギュレーション プロバイダーの情報にアクセスできるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="48585-201">The component is configured to access information about versions of ER configurations, details of configurations and configuration providers with using a data source of the **Join** type.</span></span>

1. <span data-ttu-id="48585-202">構成ツリーで、**Set2** および **Set2.Details** データ モデル項目を展開します。</span><span class="sxs-lookup"><span data-stu-id="48585-202">In the configurations tree, expand the **Set2** and **Set2.Details** data model items.</span></span> <span data-ttu-id="48585-203">**Details: Record list = Details** のバインドは、**Set2.Details** 項目が **Join** タイプのデータ ソースとして構成された **詳細** データ ソースにバインドされていることを示します。</span><span class="sxs-lookup"><span data-stu-id="48585-203">The binding **Details: Record list = Details** indicates that the **Set2.Details** item is bound to the **Details** data source configured as the data source of the **Join** type.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Review.PNG)

    <span data-ttu-id="48585-205">**結合** データ ソースは、**Functions\Join** データ ソースを選択することによって追加できます。</span><span class="sxs-lookup"><span data-stu-id="48585-205">The **Join** data source can be added by selecting the **Functions\Join** data source:</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-AddJoinDS.PNG)

2. <span data-ttu-id="48585-207">**詳細** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-207">Select **Detail** s data source.</span></span>
3. <span data-ttu-id="48585-208">**編集** を、**データ ソース** ウィンドウで選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-208">Select **Edit** in the **Data sources** pane.</span></span>
4. <span data-ttu-id="48585-209">**結合を編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-209">Select **Edit join**.</span></span>
5. <span data-ttu-id="48585-210">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-210">Select **Show details**.</span></span>

    ![結合データ ソース パラメーター ページ](./media/GER-JoinDS-JoinDSEditor.PNG)

    <span data-ttu-id="48585-212">このページは、**結合タイプ** の必要なデータ ソースをデザインするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-212">This page is used to design the required data source of the **Join type**.</span></span> <span data-ttu-id="48585-213">このデータ ソースは、実行時に、**結合リスト** グリッドのデータ ソースから 1 つの結合されたレコード リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="48585-213">At runtime, this data source will create a single joined list of records from the data sources in the **Joined list** grid.</span></span> <span data-ttu-id="48585-214">レコードの結合は、グリッドで最初となる **ConfigurationProviders** データ ソースから始まります (**タイプ** 列はそのために空白)。</span><span class="sxs-lookup"><span data-stu-id="48585-214">Join of records will start from the **ConfigurationProviders** data source that is in the grid as a first one (the **Type** column is blank for it).</span></span> <span data-ttu-id="48585-215">したがって、他のすべてのデータ ソースのレコードは、このグリッドでの順序に基づいて、親データ ソースのレコードに結合されます。</span><span class="sxs-lookup"><span data-stu-id="48585-215">Records of every other data source will be joined consequently to records of the parent data source based on its order in this grid.</span></span> <span data-ttu-id="48585-216">すべての結合データ ソースは、ターゲット データ ソースの下で入れ子になったデータ ソースとして構成される必要があります (`1Versions` データ ソースは `1Configurations` 1 の下で入れ子となっており、`1Configurations` データ ソースは、**ConfigurationProviders** 1 の下で入れ子になっています)。</span><span class="sxs-lookup"><span data-stu-id="48585-216">Every joining data source must be configured as a data source nested under a target data source (`1Versions` data source is nested under `1Configurations` one; `1Configurations` data source is nested under **ConfigurationProviders** one).</span></span> <span data-ttu-id="48585-217">構成された各データ ソースには、結合の条件が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="48585-217">Each configured data source must contain the conditions for the join.</span></span> <span data-ttu-id="48585-218">この特定の **結合** データ ソースでは、次の結合が定義されています:</span><span class="sxs-lookup"><span data-stu-id="48585-218">In the data source for this particular **Join**, the following joins are defined:</span></span>

    - <span data-ttu-id="48585-219">**ConfigurationProviders** データ ソース (**ERVendorTable** テーブル参照) の各レコードは、**1Configurations**(**ERSolutionTable** テーブル参照) のみに結合されます。**SolutionVendor** および **RecId** フィールドの値は同じになります。</span><span class="sxs-lookup"><span data-stu-id="48585-219">Each record of the **ConfigurationProviders** data source (referred to the **ERVendorTable** table) is joined with only records of the **1Configurations** one (referred to in the **ERSolutionTable** table) having the same value in the **SolutionVendor** and **RecId** fields.</span></span> <span data-ttu-id="48585-220">**内部結合** タイプは、この結合に対して使用され、次の条件では、レコードの一致にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-220">The **Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="48585-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span><span class="sxs-lookup"><span data-stu-id="48585-221">FILTER (Configurations, Configurations.SolutionVendor = ConfigurationProviders.RecId)</span></span>

    - <span data-ttu-id="48585-222">**1Configurations** データ ソース (**ERSolutionTable** テーブル参照) の各レコードは、**1Versions**(**ERSolutionVersionTable** テーブル参照) のみに結合されます。**Solution** および **RecId** フィールドの値は同じになります。</span><span class="sxs-lookup"><span data-stu-id="48585-222">Each record of the **1Configurations** data source (referred to the **ERSolutionTable** table) is joined with the only records of the **1Versions** one (referred to the **ERSolutionVersionTable** table) having the same value in the **Solution** and **RecId** fields.</span></span> <span data-ttu-id="48585-223">**内部結合** タイプは、この結合に対して使用され、次の条件では、レコードの一致にも使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-223">**Inner join** type is used for this join as well as the following conditions for matching records:</span></span>

    <span data-ttu-id="48585-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span><span class="sxs-lookup"><span data-stu-id="48585-224">FILTER (ConfigurationVersions, ConfigurationVersions.Solution = ConfigurationProviders.'1Configurations'.RecId)</span></span>

    - <span data-ttu-id="48585-225">**実行** オプションは、**クエリ** として構成され、この結合データ ソースは、SQL の直接呼び出しとしてデータベース レベルで実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="48585-225">**Execute** option is configured as **Query** meaning that this join data source will be executed at runtime on database level as a direct SQL call.</span></span>

    <span data-ttu-id="48585-226">アプリケーション テーブルを表すデータ ソースのレコードを結合するには、これらのテーブル間で既存の AOT リレーションについて記述しているもの以外のフィールドのペアを使用して、結合条件を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="48585-226">For joining records of data sources representing application tables, you can specify join conditions by using pairs of fields other than ones that describe existing in AOT relations between these tables.</span></span> <span data-ttu-id="48585-227">この結合のタイプは、データベース レベルで実行するように構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="48585-227">This type of join can be configured to execute at the database level as well.</span></span>

6. <span data-ttu-id="48585-228">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48585-228">Close the page.</span></span>
7. <span data-ttu-id="48585-229">**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-229">Select **Cancel**.</span></span>
8. <span data-ttu-id="48585-230">構成ツリーで、**Set2.Summary** データ モデル項目を展開します:</span><span class="sxs-lookup"><span data-stu-id="48585-230">In the configurations tree, expand the **Set2.Summary** data model item:</span></span>

    - <span data-ttu-id="48585-231">**VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** は、**Set2.Summary.VersionsNumber** 項目が **VersionsNumber** アグリゲーション フィールドにバインドされていることを示します。これは **DetailsSummary** データ ソース (**GroupBy** タイプ) で、**詳細** データ ソース (**結合** タイプ) の結合されたレコードを返すように構成されています。</span><span class="sxs-lookup"><span data-stu-id="48585-231">Binding **VersionsNumber: Integer = DetailsSummary.aggregated.VersionsNumber** indicates that the **Set2.Summary.VersionsNumber** item is bound to the **VersionsNumber** aggregation field of the **DetailsSummary** data source of the **GroupBy** type that was configured to return the number of joined records of the **Details** data source of the **Join** type.</span></span>
    - <span data-ttu-id="48585-232">**実行** 場所オプションは、**クエリ** として構成され、この **GroupBy** データ ソースは、SQL の直接呼び出しとしてデータベース レベルで、実行時に実行されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="48585-232">The **Execution** location option is configured as **Query** meaning that this **GroupBy** data source will be run at runtime as a direct SQL call at the database level.</span></span> <span data-ttu-id="48585-233">この動作が可能なのは、**Join** タイプの基本データ ソース **Details** が、データベース レベルで実行されるように構成されているためです。</span><span class="sxs-lookup"><span data-stu-id="48585-233">This behavior is possible because the base data source **Details** of the **Join** type is configured as executed at the database level.</span></span>

    ![GROUPBY データ ソース パラメーター ページ](./media/GER-JoinDS-Set2GroupByReview.PNG)

9. <span data-ttu-id="48585-235">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48585-235">Close the page.</span></span>
10. <span data-ttu-id="48585-236">**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-236">Select **Cancel**.</span></span>

### <a name="execute-er-format"></a><a name="executeERformat"></a><span data-ttu-id="48585-237">ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="48585-237">Execute ER format</span></span>

1. <span data-ttu-id="48585-238">最初のセッションと同じ資格情報と会社を使用して、Webブラウザーの 2 番目のセッションで Finance または RCS にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="48585-238">Access Finance or RCS in the second session of your web browser using same credentials and company as in the first session.</span></span>
2. <span data-ttu-id="48585-239">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48585-239">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="48585-240">**結合データ ソースを知るためのモデル** 構成を展開します。</span><span class="sxs-lookup"><span data-stu-id="48585-240">Expand **Model to learn JOIN data sources** configuration.</span></span>
4. <span data-ttu-id="48585-241">**結合データ ソースを知るための形式** 構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-241">Select **Format to learn JOIN data sources** configuration.</span></span>
5. <span data-ttu-id="48585-242">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="48585-242">Select **Designer**.</span></span>
6. <span data-ttu-id="48585-243">**詳細を表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-243">Select **Show details**.</span></span>
7. <span data-ttu-id="48585-244">**マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-244">Select **Mapping**.</span></span>
8. <span data-ttu-id="48585-245">**展開 / 折りたたみ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-245">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="48585-246">この形式は、ER 構成のバージョン (**バージョン** 順序) ごとに、生成されたテキスト ファイルに新しい行を挿入するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="48585-246">This format is designed to populate a generated text file with a new line for every version of an ER configuration (**Version** sequence).</span></span> <span data-ttu-id="48585-247">生成される各行には、現在の構成を所有する構成プロバイダー名、構成名、およびセミコロン記号で区切られた構成バージョンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="48585-247">Each generated line will contain the name of a configuration provider owning the current configuration, the configuration name, and the configuration version separated by semicolon mark.</span></span> <span data-ttu-id="48585-248">生成されるファイルの最終行には、ER コンフィギュレーションの検出されたバージョン数が含まれます (**集計** シーケンス) 。</span><span class="sxs-lookup"><span data-stu-id="48585-248">The final line of generated file will contain the number of discovered versions of ER configurations (**Summary** sequence).</span></span>

    ![ER 形式デザイナーのページ](./media/GER-JoinDS-FormatReview.PNG)

    <span data-ttu-id="48585-250">**データ** および **集計** データ ソースは、生成されたファイルにコンフィギュレーション バージョンの詳細を設定するために使用されます:</span><span class="sxs-lookup"><span data-stu-id="48585-250">The **Data** and **Summary** data sources are used to populate configuration version details to the generated file:</span></span>

    - <span data-ttu-id="48585-251">**Set1** データ モデルの情報は、ER 形式実行時に、ユーザー ダイアログ ページで **いいえ** を **セレクター** データ ソースに対して選択する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-251">Information from the **Set1** data model is used when you choose **No** for the **Selector** data source at runtime on the user dialog page when running ER format.</span></span>
    - <span data-ttu-id="48585-252">**Set2** データ モデルの情報は、ユーザー ダイアログ ページで **はい** を **セレクター** データ ソースに対して選択する際に使用されます。</span><span class="sxs-lookup"><span data-stu-id="48585-252">Information from the **Set2** data model is used when you choose **Yes** for the **Selector** data source at runtime on the user dialog page.</span></span>

    ![ER 形式デザイナーのページ](./media/GER-JoinDS-FormatMappingReview.PNG)

9. <span data-ttu-id="48585-254">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-254">Select **Run**.</span></span>
10. <span data-ttu-id="48585-255">ダイアログ ページで、**いいえ** を **結合データ ソースの使用** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-255">On the dialog page, select **No** in the **Use JOIN data source** field.</span></span>
11. <span data-ttu-id="48585-256">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-256">Select **OK**.</span></span>
12. <span data-ttu-id="48585-257">生成されたファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-257">Review generated file.</span></span>

    ![ER ユーザー ダイアログ ページ](./media/GER-JoinDS-Set1Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><span data-ttu-id="48585-259">ER 形式実行追跡の分析</span><span class="sxs-lookup"><span data-stu-id="48585-259">Analyze ER format execution trace</span></span>

1. <span data-ttu-id="48585-260">Finance または RCS の最初のセッションで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-260">In the first session of Finance or RCS, select **Designer**.</span></span>
2. <span data-ttu-id="48585-261">**パフォーマンスの追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-261">Select **Performance trac** e.</span></span>
3. <span data-ttu-id="48585-262">**パフォーマンスの追跡** グリッドで、現在のモデル マッピング コンポーネントを使用した ER 形式の、最新の実行追跡の最上位レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-262">In the **Performance trace** grid, select the top-most record of the latest execution trace of an ER format that used the current model mapping component.</span></span>
4. <span data-ttu-id="48585-263">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-263">Select **OK**.</span></span>

    <span data-ttu-id="48585-264">実行の統計は、アプリケーション テーブルへの重複した呼び出しについて通知します:</span><span class="sxs-lookup"><span data-stu-id="48585-264">Execution statistics informs you about duplicated calls to application tables:</span></span>

    - <span data-ttu-id="48585-265">**ERSolutionTable** は、**ERSolutionVersionTable** テーブルに含まれるコンフィギュレーション バージョン レコードの数だけ呼び出されますが、そのような呼び出しの数はパフォーマンス向上のため、所用時間が減ることがあります。</span><span class="sxs-lookup"><span data-stu-id="48585-265">**ERSolutionTable** has been called as many times as you have configuration version records in the **ERSolutionVersionTable** table, while the number of such calls could be reduced in times for performance improvement.</span></span>
    - <span data-ttu-id="48585-266">**ERVendorTable** は、**ERSolutionVersionTable** テーブルで検出されるコンフィギュレーション バージョン レコードの 2 倍呼び出されますが、そのような呼び出しの数も減ることがあります。</span><span class="sxs-lookup"><span data-stu-id="48585-266">**ERVendorTable** has been called twice for every configuration version record that was discovered in the **ERSolutionVersionTable** table, while the number of such calls could be reduced as well.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set1Run2.PNG)

5. <span data-ttu-id="48585-268">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48585-268">Close the page.</span></span>

### <a name="execute-er-format"></a><span data-ttu-id="48585-269">ER 形式の実行</span><span class="sxs-lookup"><span data-stu-id="48585-269">Execute ER format</span></span>

1. <span data-ttu-id="48585-270">Finance または RCS の 2 番目のセッションを使用して、Web ブラウザー タブに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="48585-270">Switch to your web browser tab with the second session of Finance or RCS.</span></span>
2. <span data-ttu-id="48585-271">**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-271">Select **Run**.</span></span>
3. <span data-ttu-id="48585-272">ダイアログ ページで、**はい** を **結合データ ソースの使用** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-272">On the dialog page, select **Yes** in the **Use JOIN data source** field.</span></span>
4. <span data-ttu-id="48585-273">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-273">Select **OK**.</span></span>
5. <span data-ttu-id="48585-274">生成されたファイルを確認します。</span><span class="sxs-lookup"><span data-stu-id="48585-274">Review generated file.</span></span>

    ![ER ユーザー ダイアログ ページ](./media/GER-JoinDS-Set2Run.PNG)

#### <a name="analyze-er-format-execution-trace"></a><a name="analyze"></a> <span data-ttu-id="48585-276">ER 形式実行追跡の分析</span><span class="sxs-lookup"><span data-stu-id="48585-276">Analyze ER format execution trace</span></span>

1. <span data-ttu-id="48585-277">Finance または RCS の最初のセッションで、**デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-277">In the first session of Finance or RCS, select **Designer**.</span></span>
2. <span data-ttu-id="48585-278">**パフォーマンスの追跡** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-278">Select **Performance trace**.</span></span>
3. <span data-ttu-id="48585-279">**パフォーマンスの追跡** グリッドで、現在のモデル マッピング コンポーネントを使用した ER 形式の、最新の実行追跡を表す最上位レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-279">In the **Performance trace** grid, select top-most record representing the latest execution trace of an ER format that used the current model mapping component.</span></span>
4. <span data-ttu-id="48585-280">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48585-280">Select **OK**.</span></span>

    <span data-ttu-id="48585-281">統計には、次の情報が表示されます:</span><span class="sxs-lookup"><span data-stu-id="48585-281">Statistics informs you about the following:</span></span>

    - <span data-ttu-id="48585-282">必須フィールドにアクセスする、**ERVendorTable**、**ERSolutionTable**、および **ERSolutionVersionTable** テーブルからレコードを取得するため、アプリケーション データベースが 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48585-282">Application database has been called once to get records from **ERVendorTable**, **ERSolutionTable**, and **ERSolutionVersionTable** tables to access required fields.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Run2.PNG)

    - <span data-ttu-id="48585-284">**詳細** データ ソースで構成された結合を使用して、コンフィギュレーション バージョン数を計算するのに、アプリケーション データベースが 1 回呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="48585-284">Application database has been called once to calculate the number of configuration versions by using joins that were configured in the **Details** data source.</span></span>

    ![ER モデル マッピング デザイナーのページ](./media/GER-JoinDS-Set2Run3.PNG)

## <a name="limitations"></a><span data-ttu-id="48585-286">制限</span><span class="sxs-lookup"><span data-stu-id="48585-286">Limitations</span></span>

<span data-ttu-id="48585-287">このトピックの例で示しているように、**JOIN** データソースは、最終的に結合する必要があるレコードの個々のデータセットを表す複数のデータソースを使用して構築できます。</span><span class="sxs-lookup"><span data-stu-id="48585-287">As you can see from the example in this topic, the **JOIN** data source can be built from several data sources that describe the individual datasets of the records that must eventually be joined.</span></span> <span data-ttu-id="48585-288">これらのデータソースは、組み込みの ER [フィルタ](er-functions-list-filter.md) 機能を使用して構成できます。</span><span class="sxs-lookup"><span data-stu-id="48585-288">You can configure those data sources by using the built-in ER [FILTER](er-functions-list-filter.md) function.</span></span> <span data-ttu-id="48585-289">**JOIN** データソースの範囲を超えてデータソースを呼び出すように構成する場合は、データ選択の条件の一部として会社の範囲を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="48585-289">When you configure the data source so that it's called beyond the **JOIN** data source, you can use company ranges as part of the condition for data selection.</span></span> <span data-ttu-id="48585-290">**JOIN** データソースの初期実装では、このタイプのデータソースには対応していません。</span><span class="sxs-lookup"><span data-stu-id="48585-290">The initial implementation of the **JOIN** data source doesn't support data sources of this type.</span></span> <span data-ttu-id="48585-291">たとえば、**JOIN** データソースの実行範囲内で、[フィルタ](er-functions-list-filter.md) ベースのデータソースを呼び出した場合で、呼び出されたデータソースにデータ選択の条件の一部として企業範囲が含まれていると例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="48585-291">For example, when you call a [FILTER](er-functions-list-filter.md)-based data source within the scope of execution of a **JOIN** data source, if the called data source contains company ranges as part of the condition for data selection, an exception occurs.</span></span>

<span data-ttu-id="48585-292">Microsoft Dynamics 365 Finance バージョン 10.0.12（2020 年 8 月）では、**JOIN** データソースの実行範囲内で呼び出される[フィルタ](er-functions-list-filter.md)ベースのデータソースのデータ選択条件の一部として、会社の範囲を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="48585-292">In Microsoft Dynamics 365 Finance version 10.0.12 (August 2020), you can use company ranges as part of the condition for data selection in [FILTER](er-functions-list-filter.md)-based data sources that are called within the scope of execution of a **JOIN** data source.</span></span> <span data-ttu-id="48585-293">アプリケーションの [クエリ](../dev-ref/xpp-library-objects.md#query-object-model) ビルダーには制限があるため、この 会社の範囲は **JOIN** データソースの最初のデータソースに対してのみサポートされてい ます。</span><span class="sxs-lookup"><span data-stu-id="48585-293">Because of the limitations of the application [query](../dev-ref/xpp-library-objects.md#query-object-model) builder, the company ranges are supported only for the first data source of a **JOIN** data source.</span></span>

### <a name="example"></a><span data-ttu-id="48585-294">例</span><span class="sxs-lookup"><span data-stu-id="48585-294">Example</span></span>

<span data-ttu-id="48585-295">例えば、複数の企業の外国貿易取引のリストと、それらの取引で参照される在庫項目の詳細を取得するには、アプリケーション データベースを 1 回呼び出しをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="48585-295">For example, you must make a single call to the application database to get the list of foreign trade transactions of multiple companies and the details of the inventory item that is referred to in those transactions.</span></span>

<span data-ttu-id="48585-296">この場合は、ER モデルマッピングに次のようなアーティファクトを構成します：</span><span class="sxs-lookup"><span data-stu-id="48585-296">In this case, you configure the following artifacts in your ER model mapping:</span></span>

- <span data-ttu-id="48585-297">**イントラスタット** **イントラスタット** テーブルを表すルート データソースです。</span><span class="sxs-lookup"><span data-stu-id="48585-297">**Intrastat** root data source that represents the **Intrastat** table.</span></span>
- <span data-ttu-id="48585-298">**項目** **InventTable** テーブルを表すルート データソースです。</span><span class="sxs-lookup"><span data-stu-id="48585-298">**Items** root data source that represents the **InventTable** table.</span></span>
- <span data-ttu-id="48585-299">**会社** 取引にアクセスする必要のある会社（この例では **DEMF** と  **GBSI**）のリストを返すルート データソースです。</span><span class="sxs-lookup"><span data-stu-id="48585-299">**Companies** root data source that returns the list of companies (**DEMF** and **GBSI** in this example) where transactions must be accessed.</span></span> <span data-ttu-id="48585-300">会社コードは、 **Companies.Code** で利用できます。</span><span class="sxs-lookup"><span data-stu-id="48585-300">The company code is available from the **Companies.Code** field.</span></span>
- <span data-ttu-id="48585-301">**X1** 式 `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))` を持つルート データ ソースです。</span><span class="sxs-lookup"><span data-stu-id="48585-301">**X1** root data source that has the expression `FILTER (Intrastat, VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code))`.</span></span> <span data-ttu-id="48585-302">データ選択の条件の一部として、この式には会社の範囲 `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)` の定義が含まれています。</span><span class="sxs-lookup"><span data-stu-id="48585-302">As part of the condition for data selection, this expression contains the definition of company ranges `VALUEIN(Intrastat.dataAreaId, Companies, Companies.Code)`.</span></span>
- <span data-ttu-id="48585-303">**X2** データソースを **X1** データ ソースのネストされた項目として指定します。</span><span class="sxs-lookup"><span data-stu-id="48585-303">**X2** data source as a nested item of the **X1** data source.</span></span> <span data-ttu-id="48585-304">これには、式 `FILTER (Items, Items.ItemId = X1.ItemId)` が含まれ ます。</span><span class="sxs-lookup"><span data-stu-id="48585-304">It includes the expression `FILTER (Items, Items.ItemId = X1.ItemId)`.</span></span>

<span data-ttu-id="48585-305">最後に、**X1** を第 1 のデータソース、**X2** を第 2 のデータソースとする **JOIN** データソースを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="48585-305">Finally, you can configure a **JOIN** data source where **X1** is the first data source and **X2** is the second data source.</span></span> <span data-ttu-id="48585-306">**クエリ** を **Execute** オプションとして指定することで、ER はこのデータソースをデータベース レベルで直接 SQL 呼び出しとして実行するように強制します。</span><span class="sxs-lookup"><span data-stu-id="48585-306">You can specify **Query** as the **Execute** option to force ER to run this data source on the database level as a direct SQL call.</span></span>

<span data-ttu-id="48585-307">ER の実行を [トレース](trace-execution-er-troubleshoot-perf.md) しながら設定されたデータソースを実行すると、ER のパフォーマンス トレースの一部として、以下のステートメントがER モデル マッピング デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="48585-307">When the configured data source is run while the ER execution is [traced](trace-execution-er-troubleshoot-perf.md), the following statement is shown in the ER model mapping designer as part of the ER performance trace.</span></span>

`SELECT ... FROM INTRASTAT T1 CROSS JOIN INVENTTABLE T2 WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF',N'GBSI') )) AND ((T2.PARTITION=?) AND (T2.ITEMID=T1.ITEMID AND (T2.DATAAREAID = T1.DATAAREAID) AND (T2.PARTITION = T1.PARTITION))) ORDER BY T1.DISPATCHID,T1.SEQNUM`

> [!NOTE]
> <span data-ttu-id="48585-308">実行された **JOIN** データソースの追加されたデータ ソースに対して、データの選択条件が会社の範囲をまれるように構成がされている **JOIN** データソースを実行するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="48585-308">An error occurs if you run a **JOIN** data source that has been configured so that it contains data selection conditions that have company ranges for additional data sources of the executed **JOIN** data source.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="48585-309">追加リソース</span><span class="sxs-lookup"><span data-stu-id="48585-309">Additional resources</span></span>

[<span data-ttu-id="48585-310">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="48585-310">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="48585-311">パフォーマンス上の問題をトラブルシューティングするため ER 形式の追跡実行</span><span class="sxs-lookup"><span data-stu-id="48585-311">Trace execution of ER format to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
