---
title: 小型パーセルの出荷
description: このトピックでは、小型パーセルの出荷 (SPS) 機能に関する情報を提供します。 この機能は、Microsoft Dynamics 365 Supply Chain Management を有効にして、梱包コンテナに関する詳細を配送業者に送信した後、配送業者から出荷ラベル、出荷レート、追跡番号を受け取ります。
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 37f07139853c30da25c067a3d736b4b9bf4eb361
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/04/2021
ms.locfileid: "5501177"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="88563-104">小型パーセルの出荷</span><span class="sxs-lookup"><span data-stu-id="88563-104">Small parcel shipping</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="88563-105">小型パーセルの出荷 (SPS) 機能により、Microsoft Dynamics 365 Supply Chain Management は配送業者 API を介した通信のフレームワークを提供することにより、出荷の配送業者と直接やり取りできます。</span><span class="sxs-lookup"><span data-stu-id="88563-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="88563-106">この機能は、コンテナの出荷かトラックより少ない (LTL) 出荷を使用する代わりに、個々の販売注文を業務用の配送業者経由で出荷する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="88563-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="88563-107">SPS 機能は、専用の *レート エンジン* を通じて配送業者とやりとりします。</span><span class="sxs-lookup"><span data-stu-id="88563-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="88563-108">配送業者または配送業者のサービスと協力して、このレート エンジンを開発している必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="88563-109">このレート エンジンは、Supply Chain Management を有効にして、梱包コンテナに関する詳細を配送業者に送信した後、配送業者から出荷ラベル、出荷レート、追跡番号を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="88563-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="88563-110">返品される出荷レートは、関連付けられている販売注文に雑費として追加されます。</span><span class="sxs-lookup"><span data-stu-id="88563-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="88563-111">その後、返品された出荷ラベルは、Zebra Programming Language (ZPL) プリンターを使用して自動的に印刷され、出荷に適用されます。</span><span class="sxs-lookup"><span data-stu-id="88563-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="88563-112">配送業者は、倉庫で梱包を取り出す際に、この出荷ラベルをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="88563-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="88563-113">SPS をサポートするシステムの準備</span><span class="sxs-lookup"><span data-stu-id="88563-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="88563-114">SPS 機能を使用する前に、機能管理で SPS 機能を有効にし、レート エンジンを追加し、**輸送管理** モジュールと **倉庫管理** モジュールを設定して、それをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="88563-115">SPS 機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="88563-115">Turn on the SPS feature</span></span>

<span data-ttu-id="88563-116">この SPS 機能を使用するには、システム上で有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="88563-117">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ワークスペースを使用して、この機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="88563-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="88563-118">この機能は、次のようにして表示されます。</span><span class="sxs-lookup"><span data-stu-id="88563-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="88563-119">**モジュール:** *輸送管理*</span><span class="sxs-lookup"><span data-stu-id="88563-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="88563-120">**機能名:** *小型パーセルの出荷*</span><span class="sxs-lookup"><span data-stu-id="88563-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="88563-121">レート エンジンの配置と設定</span><span class="sxs-lookup"><span data-stu-id="88563-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="88563-122">Supply Chain Management にはレート エンジンは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="88563-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="88563-123">必要なレートを取得または作成し、システムに追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="88563-124">ただし、テスト用に使用できるデモ レート エンジンが Microsoft に提供されています。</span><span class="sxs-lookup"><span data-stu-id="88563-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="88563-125">デモ レート エンジンのダウンロードと配置</span><span class="sxs-lookup"><span data-stu-id="88563-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="88563-126">デモ レート エンジンを利用するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="88563-127">GitHub で、[デモ レート エンジン用の Dynamic-link ライブラリ (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS) をダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="88563-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="88563-128">Supply Chain Management サーバーで、DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** フォルダに DLL を保存します。</span><span class="sxs-lookup"><span data-stu-id="88563-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="88563-129">機能レート エンジンを作成および配置する</span><span class="sxs-lookup"><span data-stu-id="88563-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="88563-130">生産環境またはテスト環境で使用できるような機能レート エンジンを作成して配置する方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88563-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="88563-131">新しい輸送管理エンジンの作成</span><span class="sxs-lookup"><span data-stu-id="88563-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="88563-132">輸送管理エンジンの設定</span><span class="sxs-lookup"><span data-stu-id="88563-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="88563-133">SPS レート エンジンの作成方法の詳細については、次のブログ投稿: [小型パーセルの出荷: Microsoft Dynamics 365 で小型パーセルの出荷の出荷機能を活用する方法](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5) を示しています。</span><span class="sxs-lookup"><span data-stu-id="88563-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="88563-134">Supply Chain Management でのレート エンジンの設定</span><span class="sxs-lookup"><span data-stu-id="88563-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="88563-135">SPS のレート エンジンを作成して配置したら、次の手順に従ってセットアップします。</span><span class="sxs-lookup"><span data-stu-id="88563-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="88563-136">**輸送管理 \> 設定 \> エンジン \> レート エンジン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="88563-137">アクション ウィンドウで **新規** を選択して、行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="88563-138">新しい行で、次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="88563-139">**評価エンジン** - レート エンジンの一意の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="88563-140">デモ レート エンジンを使用している場合は、*デモ レート エンジン* を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="88563-141">**名前** - レート エンジンの簡単な説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="88563-142">デモ レート エンジンを使用している場合は、*デモ レート エンジン* を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="88563-143">**評価メタデータ ID** - レートの計算に使用する基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="88563-144">たとえば、レートが距離に基づいて計算される場合があります。</span><span class="sxs-lookup"><span data-stu-id="88563-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="88563-145">デモ レート エンジンを使用する場合は、このフィールドを空白のままにしておきます。</span><span class="sxs-lookup"><span data-stu-id="88563-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="88563-146">**エンジン アセンブリ** - 配置した DLL パッケージのファイル名を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="88563-147">デモ レート エンジンを使用している場合は、*TMSSmallParcelShippingEngine.dll* と入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="88563-148">**エンジン クラス** - レート エンジンに対して設定されたクラス名を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="88563-149">デモ レート エンジンを使用している場合は、*TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine* と入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="88563-150">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="88563-150">Example scenario</span></span>

<span data-ttu-id="88563-151">このシナリオの例では、このトピックの説明に従って、システムを準備した後に SPS を設定して使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="88563-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="88563-152">このシナリオでは、前述のデモ レート エンジンを使用します。</span><span class="sxs-lookup"><span data-stu-id="88563-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="88563-153">デモ データを有効化する</span><span class="sxs-lookup"><span data-stu-id="88563-153">Make demo data available</span></span>

<span data-ttu-id="88563-154">ここで指定されたデモ レコードと値を使用してシナリオを実行するには、標準 [デモ データ](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) がインストールされているシステムを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="88563-155">また、開始する前に **USMF** 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="88563-156">シナリオを設定する</span><span class="sxs-lookup"><span data-stu-id="88563-156">Set up the scenario</span></span>

<span data-ttu-id="88563-157">このシナリオの例では、デモの配送業者、配送業者グループ、梱包ポリシー、梱包プロファイルが必要です。</span><span class="sxs-lookup"><span data-stu-id="88563-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="88563-158">次のサブセクションでは、シナリオに必要なレコードの準備方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="88563-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="88563-159">生産シナリオでは、一般に、ここで説明しているプロセスと似て設定プロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="88563-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="88563-160">ただし、異なる値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="88563-161">配送業者の設定</span><span class="sxs-lookup"><span data-stu-id="88563-161">Set up carriers</span></span>

<span data-ttu-id="88563-162">配送業者を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="88563-163">**輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="88563-164">アクション ペインで、**新規** を選択して、配送業者を追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="88563-165">ヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="88563-166">**出荷の配送業者:** *デモ配送業者*</span><span class="sxs-lookup"><span data-stu-id="88563-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="88563-167">**名前:** *デモ配送業者*</span><span class="sxs-lookup"><span data-stu-id="88563-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="88563-168">**モード:** *陸送*</span><span class="sxs-lookup"><span data-stu-id="88563-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="88563-169">**概要** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="88563-170">**出荷配送業者をアクティブにする:** *はい*</span><span class="sxs-lookup"><span data-stu-id="88563-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="88563-171">**配送業者評価をアクティブにする:** *はい*</span><span class="sxs-lookup"><span data-stu-id="88563-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="88563-172">**サービス** クイック タブで、**新規** を選択してグリッドにサービスを追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="88563-173">新しいサービスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="88563-174">**配送業者サービス:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="88563-175">**名前:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="88563-176">**輸送方法:** *陸送*</span><span class="sxs-lookup"><span data-stu-id="88563-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="88563-177">必要に応じて、その他のすべてのフィールドに任意の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="88563-178">(新しい出荷の配送業者レコードを保存すると、新しい荷渡方法が作成され、**配送方法** フィールドは自動的に設定されます。)</span><span class="sxs-lookup"><span data-stu-id="88563-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="88563-179">**評価プロファイル** クイックタブで、**新規** を選択して、評価プロファイルをグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="88563-180">新しいプロファイルで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="88563-181">**評価プロファイル:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="88563-182">**名前:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="88563-183">**レート エンジン:** *デモ レート エンジン*</span><span class="sxs-lookup"><span data-stu-id="88563-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="88563-184">必要に応じて、その他のすべてのフィールドに任意の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="88563-185">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="88563-186">配送業者の設定方法の詳細については、[出荷配送業者の設定](../transportation/tasks/set-up-shipping-carriers.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="88563-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="88563-187">配送業者サービス アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="88563-187">Set up carrier service accounts</span></span>

<span data-ttu-id="88563-188">配送業者のサービス アカウントを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="88563-189">**輸送管理 \> 設定 \> 評価 \> 配送業者サービスアカウント** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="88563-190">アクション ペインで、**新規** を選択して、配送業者サービス アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="88563-191">新しいアカウントで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="88563-192">**出荷の配送業者:** *デモ配送業者*</span><span class="sxs-lookup"><span data-stu-id="88563-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="88563-193">**配送業者サービス:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="88563-194">**配送業者の顧客アカウント番号:** 出荷の配送業者への接続を検証および認証するために使用される配送業者顧客アカウント番号。</span><span class="sxs-lookup"><span data-stu-id="88563-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="88563-195">あなたの配送業者がこの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="88563-195">Your carrier will provide this value.</span></span> <span data-ttu-id="88563-196">デモ サービスを使用する場合は、任意の値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="88563-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="88563-197">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="88563-197">**Site:** *6*</span></span>
    - <span data-ttu-id="88563-198">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="88563-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="88563-199">多くの場合、接続を認証するために必要な値は、**配送業者の顧客アカウント番号** の値のみです。</span><span class="sxs-lookup"><span data-stu-id="88563-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="88563-200">ただし、配送業者に認証パラメータを追加する必要がある場合は、必要に応じて組織でこのページをカスタマイズし、追加のフィールドを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88563-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="88563-201">コンテナー梱包ポリシーの設定</span><span class="sxs-lookup"><span data-stu-id="88563-201">Set up a container packing policy</span></span>

<span data-ttu-id="88563-202">コンテナー梱包ポリシーを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="88563-203">ZPL プリンター定義をまだ設定していない場合は、ドキュメント ルート指定アプリケーションを使用して設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="88563-204">詳細については、[ドキュメント印刷の概要](../../fin-ops-core/dev-itpro/analytics/print-documents.md) と関連トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="88563-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="88563-205">**倉庫管理 \> 設定 \> コンテナ― \> コンテナ―梱包ポリシー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="88563-206">アクション ペインで、**新規** を選択して、コンテナー梱包ポリシーを追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="88563-207">新規ポリシーのヘッダーで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="88563-208">**コンテナー梱包ポリシー:** *デモ梱包ポリシー*</span><span class="sxs-lookup"><span data-stu-id="88563-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="88563-209">**説明:** ポリシーの説明</span><span class="sxs-lookup"><span data-stu-id="88563-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="88563-210">**概要** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="88563-211">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="88563-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="88563-212">**最終出荷の既定の場所:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="88563-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="88563-213">**重量単位:** *KG*</span><span class="sxs-lookup"><span data-stu-id="88563-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="88563-214">**コンテナーのクロージング ポリシー:** *自動リリース*</span><span class="sxs-lookup"><span data-stu-id="88563-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="88563-215">**コンテナー リリース ポリシー:** *最終的な出荷場所で使用可能にする*</span><span class="sxs-lookup"><span data-stu-id="88563-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="88563-216">**コンテナー マニフェスト** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="88563-217">**コンテナーのクローズ時の自動マニフェスト:** *はい*</span><span class="sxs-lookup"><span data-stu-id="88563-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="88563-218">**コンテナーのマニフェスト要件:** *輸送管理*</span><span class="sxs-lookup"><span data-stu-id="88563-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="88563-219">**コンテナー内容の印刷:** *なし*</span><span class="sxs-lookup"><span data-stu-id="88563-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="88563-220">**配送業者ラベル印刷** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="88563-221">**コンテナー出荷ラベルの印刷:** *常に*</span><span class="sxs-lookup"><span data-stu-id="88563-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="88563-222">**印刷名:** 出荷ラベルを印刷する ZPL プリンターの名前</span><span class="sxs-lookup"><span data-stu-id="88563-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="88563-223">梱包プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="88563-223">Set up a packing profile</span></span>

<span data-ttu-id="88563-224">梱包プロファイルを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="88563-225">**倉庫管理 \> 設定 \> 梱包 \> 梱包プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="88563-226">アクション ペインで、**新規** を選択して、梱包プロファイルをグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="88563-227">新しいプロファイルで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="88563-228">**梱包プロファイル ID:** *デモ梱包プロファイル*</span><span class="sxs-lookup"><span data-stu-id="88563-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="88563-229">**説明:** ポリシーの説明</span><span class="sxs-lookup"><span data-stu-id="88563-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="88563-230">**コンテナー梱包ポリシー:** *デモ梱包ポリシー*</span><span class="sxs-lookup"><span data-stu-id="88563-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="88563-231">**コンテナー ID モード:** *自動*</span><span class="sxs-lookup"><span data-stu-id="88563-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="88563-232">**コンテナー タイプ:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="88563-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="88563-233">SPS 配送業者を使用する顧客の設定</span><span class="sxs-lookup"><span data-stu-id="88563-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="88563-234">作成した配送業者を使用できるよう顧客を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="88563-235">**売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="88563-236">グリッドで、顧客 *US-027* を見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="88563-237">アクション ペインで、**一般** タブの **設定** グループで、**配送業者顧客アカウント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="88563-238">**配送業者の顧客アカウント** ページで、アクション ペイン上で、**新規** を選択して、グリッドにアカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="88563-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="88563-239">新しいアカウントで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="88563-240">**出荷の配送業者:** *デモ配送業者*</span><span class="sxs-lookup"><span data-stu-id="88563-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="88563-241">**配送業者の顧客番号:** *12345* (このシナリオでは値の変更は重要ではなく、次のセクションで参照します。)</span><span class="sxs-lookup"><span data-stu-id="88563-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="88563-242">シナリオ例を確認する</span><span class="sxs-lookup"><span data-stu-id="88563-242">Go through the example scenario</span></span>

<span data-ttu-id="88563-243">前のセクションの説明に従ってサンプル データすべての設定が完了し、サンプル シナリオを実行できます。</span><span class="sxs-lookup"><span data-stu-id="88563-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="88563-244">販売注文を作成して、作業を処理する</span><span class="sxs-lookup"><span data-stu-id="88563-244">Create a sales order and process the work</span></span>

<span data-ttu-id="88563-245">これらの手順に従って、販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="88563-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="88563-246">**販売とマーケティング \> 販売注文 \> すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="88563-247">**新規** を選択して新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="88563-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="88563-248">**販売注文の作成** ダイアログ ボックスで、**顧客アカウント** フィールドを、*US-027* に設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="88563-249">**OK** を選択して販売注文を作成し、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88563-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="88563-250">新しい販売注文が開かれます。</span><span class="sxs-lookup"><span data-stu-id="88563-250">The new sales order is opened.</span></span> <span data-ttu-id="88563-251">**販売注文ヘッダー** クイック タブで、**配送業者顧客勘定番号** フィールドを、先にこの顧客に対して選択した値 (*12345*) に設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="88563-252">**販売注文明細行** セクションで、販売明細行を追加し、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="88563-253">**品目番号:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="88563-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="88563-254">**数量:** *1*</span><span class="sxs-lookup"><span data-stu-id="88563-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="88563-255">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="88563-255">**Site:** *6*</span></span>
    - <span data-ttu-id="88563-256">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="88563-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="88563-257">**ヘッダー** 表示に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="88563-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="88563-258">**出荷** クイック タブで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="88563-259">**出荷の配送業者:** *デモ配送業者*</span><span class="sxs-lookup"><span data-stu-id="88563-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="88563-260">**配送業者サービス:** *デモ配送業者サービス*</span><span class="sxs-lookup"><span data-stu-id="88563-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="88563-261">**明細行** ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="88563-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="88563-262">販売明細行の配送方法を更新するように求めるメッセージが表示された場合は、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="88563-263">**販売注文明細行** セクションで、上で設定した注文明細行を選択し、**在庫 \> 予約** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="88563-264">**引当** ページで、**引当ロット** を選択して、選択した明細行の全数量を倉庫に引当します。</span><span class="sxs-lookup"><span data-stu-id="88563-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="88563-265">**引当** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="88563-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="88563-266">アクション ウィンドウの **倉庫** タブで、**倉庫へのリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="88563-267">ピッキング場所から梱包明細に品目を移動する作業が作成されます。</span><span class="sxs-lookup"><span data-stu-id="88563-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="88563-268">**販売注文明細行** セクションで、**倉庫 \> 出荷の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="88563-269">**出荷の詳細** ページで、出荷 ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="88563-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="88563-270">これは、梱包ステーションで出荷を梱包する際に必要となります。</span><span class="sxs-lookup"><span data-stu-id="88563-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="88563-271">**出荷の詳細** ページを閉じて、販売注文に戻ります。</span><span class="sxs-lookup"><span data-stu-id="88563-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="88563-272">販売注文番号をメモしてから、**倉庫管理 \> 作業 \> すべての作業** に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="88563-273">販売注文番号を使用して、注文に対して作成された作業を検索および選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="88563-274">アクション ペインの、**作業** タブで、**作業の完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="88563-275">**作業完了** ページで、**ユーザー ID** フィールドで、ユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="88563-276">その後、アクション ペインで、**作業の検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="88563-277">その作業が検証を合格したら、アクション ペインで、**作業の完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="88563-278">梱包計画に対する品目の移動をシミュレートするために、作業が完了とマークされています。</span><span class="sxs-lookup"><span data-stu-id="88563-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="88563-279">出荷を梱包する</span><span class="sxs-lookup"><span data-stu-id="88563-279">Pack the shipment</span></span>

<span data-ttu-id="88563-280">出荷を梱包するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="88563-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="88563-281">**倉庫管理 \> 設定 \> 作業者** の順に移動し、ユーザー アカウントが倉庫管理の作業者勘定に関連付けられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88563-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="88563-282">**倉庫管理 \> 梱包とコンテナー詰め \> 梱包** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88563-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="88563-283">**梱包ステーションの選択** ダイアログ ボックスで、次の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="88563-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="88563-284">**サイト:** *6*</span><span class="sxs-lookup"><span data-stu-id="88563-284">**Site:** *6*</span></span>
    - <span data-ttu-id="88563-285">**倉庫:** *62*</span><span class="sxs-lookup"><span data-stu-id="88563-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="88563-286">**場所:** *梱包*</span><span class="sxs-lookup"><span data-stu-id="88563-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="88563-287">**梱包プロファイル ID:** *デモ梱包プロファイル*</span><span class="sxs-lookup"><span data-stu-id="88563-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="88563-288">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-288">Select **OK**.</span></span>
1. <span data-ttu-id="88563-289">**梱包** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="88563-289">The **Pack** page appears.</span></span> <span data-ttu-id="88563-290">生産のシナリオでは、作業員がライセンス プレートか出荷 ID をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="88563-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="88563-291">ただし、このシナリオでは、**すべての出荷** ページを開き、作成した出荷の出荷番号を参照します。</span><span class="sxs-lookup"><span data-stu-id="88563-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="88563-292">次に、**梱包** ページの **ライセンス プレートまたは出荷** フィールドにこの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="88563-293">または、以前にメモした出荷 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="88563-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="88563-294">アクション ウィンドウで、**新規コンテナ―** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="88563-295">表示されるダイアログ ボックスには、新しいコンテナーに関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="88563-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="88563-296">既定の値はそのままにして、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="88563-297">**梱包** ページの **品目梱包** クイック タブの **ID** フィールドで、その品目を梱包する *A0002* を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="88563-298">品目がコンテナーに追加されます。</span><span class="sxs-lookup"><span data-stu-id="88563-298">The item is added to the container.</span></span>
1. <span data-ttu-id="88563-299">アクション ペインで、**出荷のコンテナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="88563-300">表示される **出荷のコンテナー** ページには、今作成したコンテナーの行があります。</span><span class="sxs-lookup"><span data-stu-id="88563-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="88563-301">ただし、配送業者からまだ出荷ラベルと追跡番号を受け取っていないので、その行の **コンテナのマニフェスト ID** フィールドは空白です。</span><span class="sxs-lookup"><span data-stu-id="88563-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="88563-302">アクション ウィンドウで、**コンテナ―を閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="88563-303">**コンテナーを閉じる** ダイアログ ボックスで、**総重量** フィールドを *1 kg* に設定し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="88563-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="88563-304">先に選択した ZPL プリンターに出荷ラベルが印刷されます。</span><span class="sxs-lookup"><span data-stu-id="88563-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="88563-305">これは次の例に類似しているはずです。</span><span class="sxs-lookup"><span data-stu-id="88563-305">It should resemble the following example.</span></span>

    <span data-ttu-id="88563-306">![出荷ラベルの例](media/sps-label-example.png "出荷ラベルの例")</span><span class="sxs-lookup"><span data-stu-id="88563-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="88563-307">**コンテナーのマニフェスト ID** と **運賃合計** の値が、配送業者から受信したとして追加されました。</span><span class="sxs-lookup"><span data-stu-id="88563-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]