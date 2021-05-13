---
title: 移動オーダーに対する税機能のサポート
description: このトピックでは、税計算サービスを使用した移動オーダーの新しい税機能のサポートについて説明します。
author: kailiang
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d1b99046b0e439c9dadbb240050e270a7b2a6914
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920958"
---
# <a name="tax-feature-support-for-transfer-orders"></a><span data-ttu-id="e3b12-103">移動オーダーに対する税機能のサポート</span><span class="sxs-lookup"><span data-stu-id="e3b12-103">Tax feature support for transfer orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e3b12-104">このトピックでは、移動オーダーの税計算と転記の統合に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-104">This topic provides information about tax calculation and posting integration in transfer orders.</span></span> <span data-ttu-id="e3b12-105">この機能により、在庫移動の移動オーダーで税計算および転記を設定できます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-105">This functionality lets you set up tax calculation and posting in transfer orders for stock transfers.</span></span> <span data-ttu-id="e3b12-106">欧州連合 (EU) の付加価値税 (VAT) 規制では、在庫移動は EU 内供給および EU 内取得と見なされます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-106">Under European Union (EU) value-added tax (VAT) regulations, stock transfers are considered intra-community supply and intra-community acquisitions.</span></span>

<span data-ttu-id="e3b12-107">この機能を構成および使用するには、次の 3 つの主要な手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-107">To configure and use this functionality, you must complete three main steps:</span></span>

1. <span data-ttu-id="e3b12-108">**RCS の設定**: Regulatory Configuration Service で、移動オーダーでの税コード決定に適用できる税機能、税コード、および税コード を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-108">**RCS setup:** In Regulatory Configuration Service, set up the tax feature, tax codes, and tax codes applicability for tax code determination in transfer orders.</span></span>
2. <span data-ttu-id="e3b12-109">**Finance 設定:** Microsoft Dynamics 365 Finance では、**移動オーダーの税機能** を有効にし、在庫用の税サービス パラメーターを設定し、コア税パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-109">**Finance setup:** In Microsoft Dynamics 365 Finance, turn on the **Tax in transfer order** feature, set up the tax service parameters for inventory, and set up core tax parameters.</span></span>
3. <span data-ttu-id="e3b12-110">**在庫の設定**: 移動オーダー トランザクションの在庫コンフィギュレーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-110">**Inventory setup:** Set up the inventory configuration for transfer order transactions.</span></span>

## <a name="set-up-rcs-for-tax-and-transfer-order-transactions"></a><span data-ttu-id="e3b12-111">税および移動オーダー トランザクション用の RCS の設定</span><span class="sxs-lookup"><span data-stu-id="e3b12-111">Set up RCS for tax and transfer order transactions</span></span>

<span data-ttu-id="e3b12-112">次の手順に従って、移動オーダーに関連する税金を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-112">Follow these steps to set up the tax that is involved in a transfer order.</span></span> <span data-ttu-id="e3b12-113">ここに示されている例では、移動オーダーはオランダからベルギーへのものです。</span><span class="sxs-lookup"><span data-stu-id="e3b12-113">In the example that is shown here, the transfer order is from the Netherlands to Belgium.</span></span>

1. <span data-ttu-id="e3b12-114">**税機能** ページの **バージョン** タブで、ドラフト機能バージョンを選択し、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-114">On the **Tax features** page, on the **Versions** tab, select the draft feature version, and then select **Edit**.</span></span>

    ![編集の選択](../media/image1.png)

2. <span data-ttu-id="e3b12-116">**税機能の設定** ページの **税コード** タブで、**追加** を選択して新しい税コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-116">On the **Tax features setup** page, on the **Tax codes** tab, select **Add** to create new tax codes.</span></span> <span data-ttu-id="e3b12-117">この例では 、**NL-Exempt**、**BE-RC-21**、**BE-RC+21** の 3 つの税コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-117">For this example, three tax codes are created: **NL-Exempt**, **BE-RC-21**, and **BE-RC+21**.</span></span>

    - <span data-ttu-id="e3b12-118">移動オーダーがオランダの倉庫から出荷される場合、オランダ VAT 控除税コード (**NL-Exempt**) が適用されます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-118">When a transfer order is shipped from a warehouse in the Netherlands, the Netherlands VAT exempted tax code (**NL-Exempt**) is applied.</span></span>
      
        <span data-ttu-id="e3b12-119">税コード **NL-Exempt** を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-119">Create the tax code **NL-Exempt**.</span></span>
        1. <span data-ttu-id="e3b12-120">**追加** を選択し、**税コード** フィールドに **NL-Exempt** を入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-120">Select **Add**, enter **NL-Exempt** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="e3b12-121">**税コンポーネント** フィールドで **正味金額別** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-121">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="e3b12-122">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-122">Select **Save**.</span></span>
        4. <span data-ttu-id="e3b12-123">**レート** テーブルで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-123">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="e3b12-124">**一般** セクションで 、**非課税である** を **はい** に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-124">Swtich **Is Exempt** to **Yes** in the **General** section.</span></span>

        ![NL-Exempt 税コード](../media/image2.png)

    - <span data-ttu-id="e3b12-126">ベルギーの倉庫で移動オーダーを受け取る場合は 、**BE-RC-21** および **BE-RC+21** 税コードを使用して逆請求メカニズムが適用されます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-126">When a transfer order is received at a Belgium warehouse, the reverse charge mechanism is applied by using the **BE-RC-21** and **BE-RC+21** tax codes.</span></span>
        
        <span data-ttu-id="e3b12-127">税コード **BE-RC-21** を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-127">Create the tax code **BE-RC-21**.</span></span>      
        1. <span data-ttu-id="e3b12-128">**追加** を選択し、**税コード** フィールドに **BE-RC-21** を入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-128">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="e3b12-129">**税コンポーネント** フィールドで **正味金額別** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-129">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="e3b12-130">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-130">Select **Save**.</span></span>
        4. <span data-ttu-id="e3b12-131">**レート** テーブルで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-131">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="e3b12-132">**税率** フィールドに **-21** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-132">Enter **-21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="e3b12-133">**一般** セクションで 、**逆請求である** を **はい** に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-133">Swtich **Is Reverse Charge** to **Yes** in the **General** section.</span></span>
        7. <span data-ttu-id="e3b12-134">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-134">Select **Save**.</span></span>

        ![逆請求の BE-RC-21 税コード](../media/image3.png)
        
        <span data-ttu-id="e3b12-136">税コード **BE-RC+21** を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-136">Create the tax code **BE-RC+21**.</span></span>
        1. <span data-ttu-id="e3b12-137">**追加** を選択し、**税コード** フィールドに **BE-RC-21** を入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-137">Select **Add**, enter **BE-RC-21** in the **Tax code** field.</span></span>
        2. <span data-ttu-id="e3b12-138">**税コンポーネント** フィールドで **正味金額別** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-138">Select **By Net Amount** in the **Tax component** field.</span></span>
        3. <span data-ttu-id="e3b12-139">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-139">Select **Save**.</span></span>
        4. <span data-ttu-id="e3b12-140">**レート** テーブルで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-140">Select **Add** in the **Rate** table.</span></span>
        5. <span data-ttu-id="e3b12-141">**税率** フィールドに **21** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-141">Enter **21** in the **Tax Rate** field.</span></span>
        6. <span data-ttu-id="e3b12-142">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-142">Select **Save**.</span></span>

        ![逆請求の BE-RC+21 税コード](../media/image4.png)

3. <span data-ttu-id="e3b12-144">税コードの適用方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-144">Define the applicability of the tax codes.</span></span>

    1. <span data-ttu-id="e3b12-145">**列の管理** を選択し、該当するテーブルの作成に使用する列を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-145">Select **Manage columns**, and then select columns that should be used to build the applicability table.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e3b12-146">**業務プロセス** および **税提示方法** 列をテーブルに追加してください。</span><span class="sxs-lookup"><span data-stu-id="e3b12-146">Be sure to add the **Business process** and **Tax directions** columns to the table.</span></span> <span data-ttu-id="e3b12-147">両方の列は、移動オーダーの税金の機能にとって重要なものです。</span><span class="sxs-lookup"><span data-stu-id="e3b12-147">Both columns are essential to the functionality for tax in transfer orders.</span></span>

    2. <span data-ttu-id="e3b12-148">適合性ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-148">Add applicability rules.</span></span> <span data-ttu-id="e3b12-149">**税コード**、**税グループ**、および **品目別税グループ** フィールドは空白にしない。</span><span class="sxs-lookup"><span data-stu-id="e3b12-149">Don't leave the **Tax codes**, **Tax group**, and **Item tax group** fields blank.</span></span>
        
        <span data-ttu-id="e3b12-150">移動オーダー出荷の新しいルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-150">Add a new rule for transfer order shipment.</span></span>
        1. <span data-ttu-id="e3b12-151">**適用性ルール** テーブルで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-151">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="e3b12-152">**業務プロセス** フィールドで **在庫** を選択して、このルールを移動オーダーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-152">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="e3b12-153">**国/地域から出荷** フィールドに **NLD** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-153">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="e3b12-154">**国/地域へ出荷** フィールドに **BEL** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-154">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="e3b12-155">**税提示方法** フィールドで、**出力** を選択して、移動オーダーの出荷にルールを適用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e3b12-155">In the **Tax direction** field, select **Output** to make the rule applicable to transfer order shipment.</span></span>
        6. <span data-ttu-id="e3b12-156">**税コード** フィールドで、**NL-Exempt** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-156">In the **Tax codes** field, select **NL-Exempt**.</span></span>
        7. <span data-ttu-id="e3b12-157">**税グループ** フィールドと **品目別税グループ** で、Finance システムに定義されている関連売上税グループと品目売上税グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-157">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>
        
        <span data-ttu-id="e3b12-158">移動オーダー入荷の別ルールを追加します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-158">Add another rule for transfer order receipt.</span></span>
        1. <span data-ttu-id="e3b12-159">**適用性ルール** テーブルで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-159">Select **Add** in the **Applicability rules** table.</span></span>
        2. <span data-ttu-id="e3b12-160">**業務プロセス** フィールドで **在庫** を選択して、このルールを移動オーダーに適用できます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-160">In the **Business process** field, select **Inventory** to make the rule applicable for a transfer order.</span></span>
        3. <span data-ttu-id="e3b12-161">**国/地域から出荷** フィールドに **NLD** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-161">In the **Ship From Country/Region** field, enter **NLD**.</span></span>
        4. <span data-ttu-id="e3b12-162">**国/地域へ出荷** フィールドに **BEL** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-162">In the **Ship To Country/Region** field, enter **BEL**.</span></span>
        5. <span data-ttu-id="e3b12-163">**税提示方法** フィールドで、**入力** を選択して、移動オーダーの入荷にルールを適用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="e3b12-163">In the **Tax direction** field, select **Input** to make the rule applicable to transfer order receipt.</span></span>
        6. <span data-ttu-id="e3b12-164">**税コード** フィールドで 、**BE-RC+21** および **BE-RC-21** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-164">In the **Tax codes** field, select **BE-RC+21** and **BE-RC-21**.</span></span>
        7. <span data-ttu-id="e3b12-165">**税グループ** フィールドと **品目別税グループ** で、Finance システムに定義されている関連売上税グループと品目売上税グループを入力します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-165">In the **Tax Group** field and the **Item Tax Group**, enter the related sales tax group and item sales tax group which are defined in your Finance system.</span></span>

        ![適合性ルール](../media/image5.png)

4. <span data-ttu-id="e3b12-167">新しい税機能のバージョンを完成して公開します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-167">Complete and publish the new tax feature version.</span></span>

    <span data-ttu-id="e3b12-168">[![新しいバージョンのステータスの変更](../media/image6.png)](../media/image6.png)</span><span class="sxs-lookup"><span data-stu-id="e3b12-168">[![Changing the status of the new version](../media/image6.png)](../media/image6.png)</span></span>

## <a name="set-up-finance-for-transfer-order-transactions"></a><span data-ttu-id="e3b12-169">移動オーダー トランザクション用の Finance の設定</span><span class="sxs-lookup"><span data-stu-id="e3b12-169">Set up Finance for transfer order transactions</span></span>

<span data-ttu-id="e3b12-170">移動オーダーの税を有効化および設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="e3b12-170">Follow these steps to enable and set up taxes for transfer orders.</span></span>

1. <span data-ttu-id="e3b12-171">Finance に、**ワークスペース** \> **機能管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-171">In Finance, go to **Workspaces** \> **Feature management**.</span></span>
2. <span data-ttu-id="e3b12-172">リストで、**移動オーダーの税** 機能を検索して選択し、**今すぐ有効化** を選択して有効にします。</span><span class="sxs-lookup"><span data-stu-id="e3b12-172">In the list, find and select the **Tax in transfer order** feature, and then select **Enable now** to turn it on.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e3b12-173">**移動オーダーの税** 機能は、税サービスに完全に依存しています。</span><span class="sxs-lookup"><span data-stu-id="e3b12-173">The **Tax in transfer order** feature is fully dependent on the tax service.</span></span> <span data-ttu-id="e3b12-174">そのため、税サービスをインストールした後にのみ有効化できます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-174">Therefore, it can be turned on only after you've installed the tax service.</span></span>

    ![移動オーダーの税機能](../media/image7.png)

3. <span data-ttu-id="e3b12-176">税サービスを有効にし、**在庫** 業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-176">Enable the tax service, and select the **Inventory** business process.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e3b12-177">税サービスおよび移動オーダーの税機能を使用するには、Finance の各法人についてこの手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-177">You must complete this step for each legal entity in Finance where you want the tax service and the functionality for tax in transfer orders to be available.</span></span>

    1. <span data-ttu-id="e3b12-178">**税** \> **設定** \> **税コンフィギュレーション** \> **税サービスの設定** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-178">Go to **Tax** \> **Setup** \> **Tax configuration** \> **Tax service setup**.</span></span>
    2. <span data-ttu-id="e3b12-179">**業務プロセス** フィールドで、**在庫** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-179">In the **Business process** field, select **Inventory**.</span></span>

    ![業務プロセス フィールドの設定](../media/image8.png)

4. <span data-ttu-id="e3b12-181">逆請求メカニズムが設定済みである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-181">Verify that the reverse charge mechanism is set up.</span></span> <span data-ttu-id="e3b12-182">**総勘定元帳** \> **設定** \> **パラメーター** に移動し、**逆請求** タブで、**逆請求を有効にする** オプションが **はい** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="e3b12-182">Go to **General ledger** \> **Setup** \> **Parameters**, and then, on the **Reverse charge** tab, verify that the **Enable reverse charge** option is set to **Yes**.</span></span>

    ![逆請求を有効にするオプション](../media/image9.png)

5. <span data-ttu-id="e3b12-184">税サービス のガイダンスに従って、Finance で関連する税コード、税グループ、品目別税グループ、および VAT 登録番号が設定されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-184">Verify that the related tax codes, tax groups, item tax groups, and VAT registration numbers have been set up in Finance according to the tax service guidance.</span></span>
6. <span data-ttu-id="e3b12-185">中間輸送勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-185">Set up an interim transit account.</span></span> <span data-ttu-id="e3b12-186">この手順が必要になるのは、移動オーダーに適用されている税が課税控除または逆請求のメカニズムに適用できない場合のみです。</span><span class="sxs-lookup"><span data-stu-id="e3b12-186">This step is required only when the tax that is applied to a transfer order isn't applicable to a tax exempted or reverse charge mechanism.</span></span>

    1. <span data-ttu-id="e3b12-187">**税** \> **設定** \> **売上税** \> **元帳転記グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-187">Go to **Tax** \> **Setup** \> **Sales tax** \> **Ledger posting groups**.</span></span>
    2. <span data-ttu-id="e3b12-188">**中間輸送** フィールドで、勘定科目を選択します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-188">In the **Interim transit** field, select a ledger account.</span></span>

    ![中間輸送勘定の選択](../media/image10.png)

## <a name="set-up-basic-inventory-for-transfer-order-transactions"></a><span data-ttu-id="e3b12-190">移動オーダー トランザクション用の基本在庫の設定</span><span class="sxs-lookup"><span data-stu-id="e3b12-190">Set up basic inventory for transfer order transactions</span></span>

<span data-ttu-id="e3b12-191">移動オーダー トランザクションを有効にするには、次の手順に従って基本在庫を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-191">Follow these steps to set up basic inventory to enable transfer order transactions.</span></span>

1. <span data-ttu-id="e3b12-192">異なる国または地域にある倉庫の出荷先サイトおよび出荷先サイトを作成し、各サイトの基本住所を追加します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-192">Create ship-from and ship-to sites for your warehouses in different countries or regions, and add the primary address for each site.</span></span>

    1. <span data-ttu-id="e3b12-193">**倉庫管理** \> **設定** \> **倉庫** \> **サイト** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-193">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Sites**.</span></span>
    2. <span data-ttu-id="e3b12-194">**新規** を選択して、後で倉庫に割り当てるサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-194">Select **New** to create the site that you will assign to a warehouse later.</span></span>
    3. <span data-ttu-id="e3b12-195">作成する必要がある他のすべてのサイトについて、手順 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-195">Repeat step 2 for all the other sites that you must create.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e3b12-196">作成したサイトの 1 つを **輸送** という名前にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-196">One of the sites that you create should be named **Transit**.</span></span> <span data-ttu-id="e3b12-197">この手順の後のステップで、このサイトを流通倉庫に割り当て、税関連の在庫伝票を移動オーダーの「出荷」トランザクションと「入荷」トランザクションで転記できます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-197">In later steps of this procedure, you will assign this site to the transit warehouse, so that tax-related inventory vouchers can be posted in "ship" and "receive" transactions for transfer orders.</span></span> <span data-ttu-id="e3b12-198">輸送サイトの住所は税計算から除外されます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-198">The address of the transit site is irrelevant to tax calculation.</span></span> <span data-ttu-id="e3b12-199">したがって、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-199">Therefore, you can leave it blank.</span></span>

    ![サイトの設定](../media/image11.png)

2. <span data-ttu-id="e3b12-201">出荷元倉庫、流通倉庫、および出荷先倉庫を作成します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-201">Create ship-from, transit, and ship-to warehouses.</span></span> <span data-ttu-id="e3b12-202">倉庫で管理されている住所情報は、税計算時にサイト住所を上書きします。</span><span class="sxs-lookup"><span data-stu-id="e3b12-202">Any address information that is maintained in a warehouse will override the site address during tax calculation.</span></span>

    1. <span data-ttu-id="e3b12-203">**倉庫管理** \> **設定** \> **倉庫** \> **倉庫** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-203">Go to **Warehouse management** \> **Setup** \> **Warehouse** \> **Warehouses**.</span></span>
    2. <span data-ttu-id="e3b12-204">**新規** を選択して倉庫を作成し、対応する際とに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e3b12-204">Select **New** to create a warehouse, and assign it to the corresponding site.</span></span>
    3. <span data-ttu-id="e3b12-205">必要に応じて、各サイトに倉庫を作成するには、手順 2 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-205">Repeat step 2 to create a warehouse for each site as required.</span></span>

    ![倉庫の設定](../media/image12.png)

    > [!NOTE]
    > <span data-ttu-id="e3b12-207">出荷元倉庫の場合、移動オーダー トランザクションの **流通倉庫** フィールドで流通倉庫を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3b12-207">For a ship-from warehouse, a transit warehouse must be selected in the **Transit warehouse** field for transfer order transactions.</span></span>
    >
    > ![流通倉庫の選択](../media/image13.png)

3. <span data-ttu-id="e3b12-209">在庫転記コンフィギュレーションが移動オーダー トランザクションに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-209">Verify that the inventory posting configuration is set up for transfer order transactions.</span></span>

    1. <span data-ttu-id="e3b12-210">**在庫管理** \> **設定** \> **転記** \> **転記** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-210">Go to **Inventory management** \> **Setup** \> **Posting** \> **Posting**.</span></span>
    2. <span data-ttu-id="e3b12-211">**在庫** タブで、勘定科目が **在庫出庫** と **在庫入庫** 転記の両方に対して設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-211">On the **Inventory** tab, verify that a ledger account is set up for both **Inventory issue** and **Inventory receipt** posting.</span></span>

        ![在庫出庫と在庫入庫転記の設定](../media/image14.png)

    3. <span data-ttu-id="e3b12-213">勘定科目が **単位間支払** 転記用に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-213">Verify that a ledger account is set up for **Inter-unit payable** posting.</span></span>

        ![単位間支払転記の設定](../media/image15.png)

    4. <span data-ttu-id="e3b12-215">勘定科目が **単位間売掛金** 転記用に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e3b12-215">Verify that a ledger account is set up for **Inter-unit receivable** posting.</span></span>

        ![単位間売掛金転記の設定](../media/image16.png)
