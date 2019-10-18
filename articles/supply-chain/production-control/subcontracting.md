---
title: 外注
description: このトピックは、Dynamics 365 Supply Chain Management で製造での外注のチュートリアルの構築に役立ちます。
author: christophernread
manager: AnnBe
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 83d1d7adf91c246ecad574043cbb60ca260bb328
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249916"
---
# <a name="subcontracting"></a><span data-ttu-id="42eef-103">外注</span><span class="sxs-lookup"><span data-stu-id="42eef-103">Subcontracting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42eef-104">このトピックは、Microsoft Dynamics 365 Supply Chain Management で製造での外注のチュートリアルの構築に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="42eef-104">This topic will help you build a walkthrough of subcontracting in manufacturing in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="42eef-105">このトピックの最初の部分では、データの設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="42eef-105">The first part of this topic describes the setup of the data.</span></span> <span data-ttu-id="42eef-106">2 番目の部分では、チュートリアルの手順が示されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-106">The second part takes you through the steps in the walkthrough.</span></span>

## <a name="target-audience"></a><span data-ttu-id="42eef-107">対象者</span><span class="sxs-lookup"><span data-stu-id="42eef-107">Target audience</span></span>

<span data-ttu-id="42eef-108">このトピックでは、製造での外注を設定する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="42eef-108">In this topic, you will learn how to set up subcontracting in manufacturing.</span></span> <span data-ttu-id="42eef-109">外注活動フローの基本設定を行うには、HQUS 法人で既存のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="42eef-109">You will use existing data in the HQUS legal entity to do the basic setup of a subcontracting activity flow.</span></span> <span data-ttu-id="42eef-110">HQUS 法人のデモ データには、チュートリアルで手順をサポートするために事前に設定された設定パラメータが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42eef-110">The demo data in the HQUS legal entity includes setup parameters that have been preset to support the steps in the walkthrough.</span></span> <span data-ttu-id="42eef-111">チュートリアルではさまざまなロールに対する重要な問題点や課題に取り組んでいますが、システム管理者がその作業を完了できます。</span><span class="sxs-lookup"><span data-stu-id="42eef-111">Even though the walkthrough addresses key pain points and challenges for various roles, it can be completed by the system admin.</span></span>

## <a name="demo-scenario"></a><span data-ttu-id="42eef-112">デモのシナリオ</span><span class="sxs-lookup"><span data-stu-id="42eef-112">Demo scenario</span></span>

<span data-ttu-id="42eef-113">HQUS 法人では、ハイエンド スピーカーが製造されています。</span><span class="sxs-lookup"><span data-stu-id="42eef-113">In the HQUS legal entity, high-end speakers are manufactured.</span></span> <span data-ttu-id="42eef-114">製造プロセス中に、スピーカーは次の 3 つの工程を経由します。</span><span class="sxs-lookup"><span data-stu-id="42eef-114">During the manufacturing process, speakers go through the following three operations.</span></span>

- <span data-ttu-id="42eef-115">**事前アセンブリ** – スピーカー キャビネットが組み立てられます。</span><span class="sxs-lookup"><span data-stu-id="42eef-115">**Pre-assembly** – The speaker cabinet is assembled.</span></span> <span data-ttu-id="42eef-116">工程を開始する前に、材料倉庫でキャビネットの材料がピッキングされます。</span><span class="sxs-lookup"><span data-stu-id="42eef-116">The material for the cabinet is picked in the material warehouse before the operation is started.</span></span>
- <span data-ttu-id="42eef-117">**コーティング** – スピーカー キャビネットがアセンブリされた後に、コーティングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="42eef-117">**Coating** – After the speaker cabinet has been assembled, it must be coated.</span></span> <span data-ttu-id="42eef-118">仕入先 (下請業者) によって、この工程が完了します。</span><span class="sxs-lookup"><span data-stu-id="42eef-118">This operation is completed by a vendor (subcontractor).</span></span> <span data-ttu-id="42eef-119">事前に組み立てられたスピーカー キャビネットは、2 つの材料と共にコーティング下請業者に出荷されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-119">The pre-assembled speaker cabinet is shipped to the coating subcontractor together with two materials.</span></span>
- <span data-ttu-id="42eef-120">**仕上げ** – 事前に組み立てられたスピーカー キャビネットが下請業者によりコーティングされた後に、スピーカーの最終的なアセンブリを完了できるよう HQUS 法人に返されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-120">**Finish** – After the pre-assembled speaker cabinet has been coated by the subcontractor, it's returned to the HQUS legal entity so that final assembly of the speaker can be completed.</span></span>

<span data-ttu-id="42eef-121">次の図は、3 つの工程および消費する材料を示します。</span><span class="sxs-lookup"><span data-stu-id="42eef-121">The following illustration shows the three operations and the materials that they consume.</span></span>

![事前アセンブリ、コーティング、仕上げの工程、および消費する材料](./media/subcontract01_operations-materials.png)

## <a name="setup"></a><span data-ttu-id="42eef-123">段取り</span><span class="sxs-lookup"><span data-stu-id="42eef-123">Setup</span></span>

<span data-ttu-id="42eef-124">このチュートリアルを開始する前に、データを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42eef-124">Before you start the walkthrough, you must set up the data.</span></span>

### <a name="set-up-the-finished-product"></a><span data-ttu-id="42eef-125">完成した製品の設定</span><span class="sxs-lookup"><span data-stu-id="42eef-125">Set up the finished product</span></span>

<span data-ttu-id="42eef-126">この手順では、リリースされた製品 D8100、"コーティングされたキャビネット" の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="42eef-126">This procedure takes you through the setup of released product D8100, "Coated Cabinet."</span></span>

1. <span data-ttu-id="42eef-127">**製品情報管理 \> 製品 \> リリース済製品**の順に選択し、**リリース済製品の詳細**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-127">Select **Product information management \> Products \> Released products** to open the **Released product details** page.</span></span>
2. <span data-ttu-id="42eef-128">クイック フィルター フィールドで、**D8100** を入力して既存のリリース済製品を検索します。</span><span class="sxs-lookup"><span data-stu-id="42eef-128">In the quick filter field, enter **D8100** to find the existing released product.</span></span>

    ![リリース済製品の詳細ページでリリース済製品 D8100 のフィルタ処理](./media/subcontract02_filtering-released-products.png)

3. <span data-ttu-id="42eef-130">アクション ウィンドウの、**エンジニア**タブで、**工順**を選択し、**工順**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-130">On the Action Pane, on the **Engineer** tab, select **Route** to open the **Route** page.</span></span>

    <span data-ttu-id="42eef-131">**工順**ページにリリース済製品 D8100 の 8 つの工順バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-131">The **Route** page shows the eight route versions for released product D8100.</span></span> <span data-ttu-id="42eef-132">8 つの工順バージョンは、サイト 1 とサイト 5 で 4 つの工順に分割されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-132">The eight route versions are divided among four routes on site 1 and site 5.</span></span> <span data-ttu-id="42eef-133">工順 000400 は原価計算に使用され、工順 00041 はコーティング工程が内部の工程である場合に使用され、および工順 00042 はコーティング工程が外部の工程である場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-133">Route 000400 is used for costing, route 00041 is used when the Coating operation is an internal operation, and route 00042 is used when the Coating operation is an external operation.</span></span>

    ![工順ページでの 8 つの工順バージョン](./media/subcontract03_route-page.png)

4. <span data-ttu-id="42eef-135">上部ウィンドウの、**バージョン**グリッドで、サイト **5** の工順バージョン **00042**  を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-135">In the upper pane, in the **Versions** grid, select route version **00042** for site **5**.</span></span>
5. <span data-ttu-id="42eef-136">下部ウィンドウの、**概要**タブで、グリッドの工順 **20** (**Cbnt CtSc**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-136">In the lower pane, on the **Overview** tab, select operation **20** (**Cbnt CtSc**) in the grid.</span></span>

    ![選択されたサイト 5 の工順バージョン 00042 の工程 20](./media/subcontract04_route-version-operation.png)

6. <span data-ttu-id="42eef-138">**一般**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-138">Select the **General** tab.</span></span>

    <span data-ttu-id="42eef-139">フィールドの**工順タイプ**フィールドが**仕入先**に設定されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-139">Notice that the field **Route type** field is set to **Vendor**.</span></span> <span data-ttu-id="42eef-140">この値は、工程 20 (Cbnt CtSc) が外注作業であることを示します。</span><span class="sxs-lookup"><span data-stu-id="42eef-140">This value indicates that operation 20 (Cbnt CtSc) is a subcontracted operation.</span></span>

    ![一般タブで、工順タイプ フィールドを仕入先に設定](./media/subcontract05_general-tab.png)

7. <span data-ttu-id="42eef-142">**リソース要件**タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-142">Select the **Resource requirements** tab.</span></span>

    <span data-ttu-id="42eef-143">生産計画立案時に適用可能なリソースを検索する機能が使用されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-143">Capabilities will be used to find an applicable resource during production scheduling.</span></span> <span data-ttu-id="42eef-144">工程 20 (Cbnt CtSc) では、リソースに 2 つの機能、**コーティング**および**コーティングされたキャビネット**が必要であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-144">For operation 20 (Cbnt CtSc), notice that a resource that has two capabilities, **Coating** and **Coated cabinets**, is required.</span></span>

    ![リソース要件タブのコーティング機能およびコーティングされたキャビネット機能](./media/subcontract06_resource-requirements-tab.png)

8. <span data-ttu-id="42eef-146">**適用可能なリソース**を選択して、**適用可能なリソース**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-146">Select **Applicable resources** to open the **Applicable resources** dialog box.</span></span>

    <span data-ttu-id="42eef-147">工程のリソース要件に一致する 3 つのリソースが検索されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-147">Three resources are found that match the resource requirements for the operation.</span></span> <span data-ttu-id="42eef-148">**仕入先**タイプがリソース 8851 および 8852 であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-148">Notice that resources 8851 and 8852 are of the **Vendor** type.</span></span>

    ![適用可能なリソースダイアログ ボックスの 3 つの適用可能なリソース](./media/subcontract07_applicable-resources-dialog.png)

9. <span data-ttu-id="42eef-150">**OK** を選択して、**適用可能なリソース**ダイアログ ボックスを閉じ、**工順**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-150">Select **OK** to close the **Applicable resources** dialog box and return to the **Route** page.</span></span>
10. <span data-ttu-id="42eef-151">**工順**ページを閉じ、**リリース済製品の詳細**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-151">Close the **Route** page to return to the **Released product details** page.</span></span>

    ![リリース済製品の詳細ページ](./media/subcontract08_released-product-details-page.png)

11. <span data-ttu-id="42eef-153">アクション ウィンドウの、**エンジニア**タブで、**BOM バージョン**を選択し、**BOM バージョン**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-153">On the Action Pane, on the **Engineer** tab, select **BOM versions** to open the **BOM versions** page.</span></span>

    <span data-ttu-id="42eef-154">**BOM バージョン**ページに、リリース済製品 D8100 の 4 つの部品表 (BOM) バージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-154">The **BOM versions** page shows the four bill of materials (BOM) versions for released product D8100.</span></span> <span data-ttu-id="42eef-155">BOM 000040 は原価計算および計画に使用され、BOM 000041 はコーティング工程が社内で行われた場合に使用され、および BOM 000042 と 000043 はコーティング工程を外注した場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-155">BOM 000040 is used for costing and planning, BOM 000041 is used if the Coating operation is done in-house, and BOMs 000042 and 000043 are used if the Coating operation is subcontracted.</span></span>

    <span data-ttu-id="42eef-156">その品目 S8050 は、**サービス**品目タイプの製品であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-156">Notice that item S8050 is a product of the **Service** item type.</span></span> <span data-ttu-id="42eef-157">この品目は、外注業務を表します。</span><span class="sxs-lookup"><span data-stu-id="42eef-157">This item represents the subcontracted work.</span></span>

    ![BOM バージョン ページの 4 つの BOM バージョン](./media/subcontract09_bom-versions-page.png)

12. <span data-ttu-id="42eef-159">**部品表明細行**クイック タブで、**編集**を選択して **BOM 明細行の編集**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-159">On the **Bill of materials lines** FastTab, select **Edit** to open the **Edit BOM line** dialog box.</span></span>

    <span data-ttu-id="42eef-160">リリース済製品 D8100 の製造オーダーが作成および見積をする場合、発注書は品目 S8050 に対して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-160">When a production order is created and estimated for released product D8100, a purchase order will be automatically generated for item S8050.</span></span> <span data-ttu-id="42eef-161">この発注書は、製造オーダーにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="42eef-161">This purchase order will be linked to the production order.</span></span> <span data-ttu-id="42eef-162">発注書を自動的に生成するには、**行タイプ**フィールドを**仕入先**に設定し、下請業者の仕入先勘定を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42eef-162">For purchase orders to be automatically generated, the **Line type** field must be set to **Vendor**, and the vendor account for the subcontractor must be selected.</span></span> <span data-ttu-id="42eef-163">この場合、仕入先勘定は US-801です。</span><span class="sxs-lookup"><span data-stu-id="42eef-163">In this case, the vendor account is US-801.</span></span>

    <span data-ttu-id="42eef-164">BOM 明細行が、工程番号 (この場合、20) を通じてコーティング工程に関連付けられていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-164">Notice that the BOM line is connected to the Coating operation through the operation number (in this case, 20).</span></span>

    ![BOM 明細行のダイアログ ボックスの編集](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a><span data-ttu-id="42eef-166">倉庫作業者のパスワードの作成</span><span class="sxs-lookup"><span data-stu-id="42eef-166">Create a password for warehouse workers</span></span>

<span data-ttu-id="42eef-167">携帯デバイスを使用する倉庫作業者のパスワードを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42eef-167">You must define a password for the warehouse workers who use the hand-held device.</span></span>

1. <span data-ttu-id="42eef-168">**倉庫管理 \> 設定 \> 作業者**の順に選択して、**作業ユーザー**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-168">Select **Warehouse management \> Setup \> Worker** to open the **Work users** page.</span></span>
2. <span data-ttu-id="42eef-169">**ユーザー**クイック タブで、ユーザー **51** の行を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-169">On the **Users** FastTab, select the row for user **51**.</span></span>

    ![作業ユーザー ページ](./media/subcontract11_work-users-page.png)

3. <span data-ttu-id="42eef-171">**パスワードのリセット**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-171">Select **Reset password**.</span></span>
4. <span data-ttu-id="42eef-172">**パスワード**および**パスワードの確認**フィールドに、**1** を入力します。</span><span class="sxs-lookup"><span data-stu-id="42eef-172">In the **Password** and **Confirm password** fields, enter **1**.</span></span>
5. <span data-ttu-id="42eef-173">**パスワードの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-173">Select **Set password**.</span></span>

## <a name="step-by-step-walkthrough"></a><span data-ttu-id="42eef-174">ステップ バイ ステップ チュートリアル</span><span class="sxs-lookup"><span data-stu-id="42eef-174">Step-by-step walkthrough</span></span>

<span data-ttu-id="42eef-175">**シナリオおよび背景**</span><span class="sxs-lookup"><span data-stu-id="42eef-175">**Scenario and background**</span></span>

<span data-ttu-id="42eef-176">製品 D8100、"コーティングされたキャビネット"に対して 10 個の製造オーダーが作成されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-176">A production order of 10 pieces is created for product D8100, "Coated Cabinet."</span></span> <span data-ttu-id="42eef-177">キャビネットのコーティングは、仕入先 US-801、完全なコーティング ソリューションで行われる外注された工程です。</span><span class="sxs-lookup"><span data-stu-id="42eef-177">The coating of the cabinets is a sub-contracted operation that is done at vendor US-801, Perfect Coating Solutions.</span></span> <span data-ttu-id="42eef-178">製造オーダーは、3 つの工程で構成されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-178">The production order consists of three operations.</span></span> <span data-ttu-id="42eef-179">最初の工程は、社内工程としてキャビネットが事前に組み立てられます。</span><span class="sxs-lookup"><span data-stu-id="42eef-179">In the first operation, the cabinet is pre-assembled as an in-house operation.</span></span> <span data-ttu-id="42eef-180">原材料倉庫で、事前組み立ての材料がピッキング用にリリースされます。</span><span class="sxs-lookup"><span data-stu-id="42eef-180">The material for the pre-assembly is released for picking in the raw material warehouse.</span></span> <span data-ttu-id="42eef-181">事前アセンブリを完了した後に、事前に組み立てられたキャビネットがコーティング工程に必要な 2 つの材料と共に、完全なコーティング ソリューションに送られます。</span><span class="sxs-lookup"><span data-stu-id="42eef-181">After the pre-assembly is completed, the pre-assembled cabinet is sent to Perfect Coating Solutions together with two materials that are required for the Coating operation.</span></span> <span data-ttu-id="42eef-182">仕入先からコーティングされたキャビネットを受け取ると、完了済と報告される前に、最終的な社内アセンブリ工程が実行されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-182">When the coated cabinet is received back from the vendor, it goes through a final in-house assembly operation before it's reported as finished.</span></span>

1. <span data-ttu-id="42eef-183">**生産管理 \> 製造オーダー \> すべての製造オーダー**の順に選択し、**すべての製造オーダー**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-183">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
2. <span data-ttu-id="42eef-184">アクション ウィンドウで、**新しい製造オーダー**を選択して**製造オーダーの作成**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-184">On the Action Pane, select **New production order** to open the **Create production order** dialog box.</span></span>

    ![製造オーダー ダイアログ ボックスの作成](./media/subcontract12_create-production-order-dialog.png)

3. <span data-ttu-id="42eef-186">**品目番号**フィールドで、**D8100** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-186">In the **Item number** field, select **D8100**.</span></span>
4. <span data-ttu-id="42eef-187">品目番号を選択した後に、在庫分析コードのフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-187">After you select the item number, fields for the inventory dimensions appear.</span></span> <span data-ttu-id="42eef-188">**色**フィールドで、**クロム**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-188">In the **Color** field, select **Chrome**.</span></span>

    <span data-ttu-id="42eef-189">BOM および工順の有効なバージョンを挿入するかどうかを尋ねるメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-189">A message box appears that asks whether the active versions for the BOM and route should be inserted.</span></span>

    ![メッセージ ボックス](./media/subcontract13_message-box.png)

5. <span data-ttu-id="42eef-191">**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-191">Select **Yes**.</span></span> 

    <span data-ttu-id="42eef-192">**製造オーダーの作成**ダイアログ ボックスでは、**BOM 番号**および**工順番号**フィールドで、製品 D8100 の BOM および工順の有効なバージョンがそれぞれ自動で選択されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-192">In the **Create production order** dialog box, the active versions of the BOM and route for product D8100 are automatically selected in the **BOM number** and **Route number** fields, respectively.</span></span> <span data-ttu-id="42eef-193">この場合、BOM **000040** および工順 **000040** が選択されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-193">In this case, BOM **000040** and route **000040** are selected.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="42eef-194">BOM および工順の両方については、原価計算と計画にバージョン 000040 が使用されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-194">For both the BOM and the route, version 000040 is used for costing and planning.</span></span>

6. <span data-ttu-id="42eef-195">**サイト**フィールドで、**5** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-195">In the **Site** field, select **5**.</span></span>
7. <span data-ttu-id="42eef-196">**倉庫**フィールドで、**51** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-196">In the **Warehouse** field, select **51**.</span></span>
8. <span data-ttu-id="42eef-197">**BOM 番号**および**工順番号**フィールドで、自動的に選択された値を **000042** に変更します。</span><span class="sxs-lookup"><span data-stu-id="42eef-197">In the **BOM number** and **Route number** fields, change the value that was automatically selected to **000042**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42eef-198">BOM および工順の両方については、バージョン 000042 を使用してキャビネットのコーティングを仕入先 US-801 に外注します。</span><span class="sxs-lookup"><span data-stu-id="42eef-198">For both the BOM and the route, version 000042 is used to subcontract the coating of the cabinet to vendor US-801.</span></span>

    ![製造オーダーの作成ダイアログ ボックスで設定された値](./media/subcontract14_create-production-order-dialog-set.png)

9. <span data-ttu-id="42eef-200">**作成**を選択して製造オーダーを作成し、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-200">Select **Create** to create the production order and return to the **All production orders** page.</span></span>

    ![すべての製造オーダー ページの新規製造オーダー](./media/subcontract15_new-production-order.png)

10. <span data-ttu-id="42eef-202">アクション ウィンドウの、**新しい製造オーダー**タブで、**見積**を選択して**見積**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-202">On the Action Pane, on the **Production order** tab, select **Estimate** to open the **Estimate** dialog box.</span></span>

    ![見積ダイアログ ボックス](./media/subcontract16_estimate-dialog.png)

11. <span data-ttu-id="42eef-204">**OK** を選択して見積を確認し、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-204">Select **OK** to confirm the estimate and return to the **All production orders** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42eef-205">製造オーダーの見積時に、仕入先 US-801 に対してサービス品目 S8050 の発注書が生成されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-205">When the production order is estimated, the purchase order for service item S8050 is generated for vendor US-801.</span></span>

12. <span data-ttu-id="42eef-206">アクション ウィンドウの、**製造オーダー**タブで、**BOM** を選択して **BOM** ページを開き、製造オーダーの BOM 明細行を表示できます。</span><span class="sxs-lookup"><span data-stu-id="42eef-206">On the Action Pane, on the **Production order** tab, select **BOM** to open the **BOM** page, where you can view the BOM lines for the production order.</span></span>

    <span data-ttu-id="42eef-207">サービス品目 S8050 については、製造オーダーの見積が行われたときに生成された発注書への参照があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-207">For service item S8050, notice that there is a reference to the purchase order that was generated when the production order was estimated.</span></span>

    ![BOM ページの製造オーダー BOM 明細行](./media/subcontract17_production-order-bom-lines.png)

13. <span data-ttu-id="42eef-209">**BOM** ページを閉じて、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-209">Close the **BOM** page to return to the **All production orders** page.</span></span>
14. <span data-ttu-id="42eef-210">アクション ウィンドウの、**スケジュール**タブで、**ジョブのスケジュール**を選択して**ジョブのスケジューリング**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-210">On the Action Pane, on the **Schedule** tab, select **Schedule jobs** to open the **Job scheduling** dialog box.</span></span>
15. <span data-ttu-id="42eef-211">次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-211">Specify the following values:</span></span>

    - <span data-ttu-id="42eef-212">**スケジューリング指示**フィールドで、**今日からフォワード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-212">In the **Scheduling direction** field, select **Forward from tomorrow**.</span></span>
    - <span data-ttu-id="42eef-213">**有限能力**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-213">Set the **Finite capacity** option to **Yes**.</span></span>

    ![ジョブのスケジューリング ダイアログ ボックス](./media/subcontract18_job-scheduling-dialog.png)

16. <span data-ttu-id="42eef-215">**OK** を選択して、**ジョブのスケジューリング**ダイアログ ボックスを閉じ、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-215">Select **OK** to close the **Job scheduling** dialog box and return to the **All production orders** page.</span></span>
17. <span data-ttu-id="42eef-216">アクション ウィンドウの、**スケジュール**タブで、**ガント**を選択して**ガント チャート - リソース ビュー**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-216">On the Action Pane, on the **Schedule** tab, select **Gantt** to open the **Gantt chart - Resource view** page.</span></span>

    <span data-ttu-id="42eef-217">ガント チャートでは、リソースで生産ジョブをスケジュールする方法の視覚概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="42eef-217">The Gantt chart provides a visual overview of how the production jobs are scheduled on the resources.</span></span> <span data-ttu-id="42eef-218">外部のコーティング工程が 3 つのジョブから成ることに注意してください: プロセス ジョブ、配送ジョブ、および待ち時間ジョブ。</span><span class="sxs-lookup"><span data-stu-id="42eef-218">Notice that the external Coating operation consists of three jobs: a process job, a transport job, and a queue time job.</span></span>

    ![ガント チャートのガント チャート - リソース ビュー ページ](./media/subcontract19_gantt-chart.png)

18. <span data-ttu-id="42eef-220">**ガント チャート - リソース ビュー**ページを閉じて、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-220">Close the **Gantt chart - Resource view** page to return to the **All production orders** page.</span></span>
19. <span data-ttu-id="42eef-221">アクション ウィンドウの、**新しい製造オーダー**タブで、**リリース**を選択して**リリース**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-221">On the Action Pane, on the **Production order** tab, select **Release** to open the **Release** dialog box.</span></span>

    ![ダイアログ ボックスをリリース](./media/subcontract20_release-dialog.png)

20. <span data-ttu-id="42eef-223">**OK** を選択して**リリース**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="42eef-223">Select **OK** to close the **Release** dialog box.</span></span>
21. <span data-ttu-id="42eef-224">**生産管理 \> 定期処理のタスク \> 倉庫にリリース \> BOM およびフォーミュラ明細行の自動リリース**の順に選択して、**BOM およびフォーミュラ明細行の自動リリース**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-224">Select **Production control \> Periodic tasks \> Release to warehouse \> Automatic release of BOM and formula lines** to open the **Automatic release of BOM and formula lines** dialog box.</span></span>

    ![BOM およびフォーミュラ明細行ダイアログ ボックスの自動リリース](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. <span data-ttu-id="42eef-226">**OK** を選択して BOM およびフォーミュラ明細行の自動リリース ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="42eef-226">Select **OK** to run the Automatic release of BOM and formula lines job.</span></span>

    <span data-ttu-id="42eef-227">このジョブでは、原材料の倉庫へのピッキング作業をリリースします。</span><span class="sxs-lookup"><span data-stu-id="42eef-227">This job releases pick work for raw materials to the warehouse.</span></span>

23. <span data-ttu-id="42eef-228">**生産管理 \> 製造オーダー \> すべての製造オーダー**の順に選択し、**すべての製造オーダー**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-228">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
24. <span data-ttu-id="42eef-229">クイック フィルター フィールドを使用して、処理中の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-229">Use the quick filter field to select the production order that you've been working on.</span></span>
25. <span data-ttu-id="42eef-230">アクション ウィンドウの、**倉庫**タブで、**作業の詳細**を選択し、**作業**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-230">On the Action Pane, on the **Warehouse** tab, select **Work details** to open the **Work** page.</span></span>

    <span data-ttu-id="42eef-231">ページに原材料ピッキングに対する 2 つの作業セットが表示されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-231">Notice that the page shows two sets of work for raw material picking.</span></span> <span data-ttu-id="42eef-232">最初の作業は材料 M8100 および M8101 対象です。</span><span class="sxs-lookup"><span data-stu-id="42eef-232">The first work is for materials M8100 and M8101.</span></span> <span data-ttu-id="42eef-233">これらの材料は工程 10 で消費されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-233">These materials are consumed by operation 10.</span></span> <span data-ttu-id="42eef-234">2 つ目の作業は材料 M8202 および M8250 対象です。</span><span class="sxs-lookup"><span data-stu-id="42eef-234">The second work is for materials M8202 and M8250.</span></span> <span data-ttu-id="42eef-235">これらの材料は、外注作業である工程 20 で消費されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-235">These materials are consumed by operation 20, which is the subcontracted operation.</span></span>

    ![作業ページの原材料ピッキングに対する 2 つの作業セット](./media/subcontract22_work-page.png)

26. <span data-ttu-id="42eef-237">工程 10 の倉庫作業を処理する倉庫アプリを開始します。</span><span class="sxs-lookup"><span data-stu-id="42eef-237">Start the warehouse app to process the warehouse work for operation 10.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. <span data-ttu-id="42eef-238">**生産管理 \> 製造オーダー \> すべての製造オーダー**の順に選択し、**すべての製造オーダー**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-238">Select **Production control \> Production orders \> All production orders** to open the **All production orders** page.</span></span>
28. <span data-ttu-id="42eef-239">クイック フィルター フィールドを使用して、処理中の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-239">Use the quick filter field to select the production order that you've been working on.</span></span>
29. <span data-ttu-id="42eef-240">アクション ウィンドウの、**新しい製造オーダー**タブで、**開始**を選択して**開始**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-240">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
30. <span data-ttu-id="42eef-241">**一般**タブで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-241">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="42eef-242">**開始工程番号**</span><span class="sxs-lookup"><span data-stu-id="42eef-242">In the **From Oper. No.**</span></span> <span data-ttu-id="42eef-243">フィールドで、**10** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-243">field, select **10**.</span></span>
    - <span data-ttu-id="42eef-244">**終了工程番号**</span><span class="sxs-lookup"><span data-stu-id="42eef-244">In the **To Oper. No.**</span></span> <span data-ttu-id="42eef-245">フィールドで、**10** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-245">field, select **10**.</span></span>

    ![一般タブで設定されている値](./media/subcontract23_start-dialog.png)

31. <span data-ttu-id="42eef-247">**OK** を選択して、**開始**ダイアログ ボックスを閉じ、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-247">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="42eef-248">製造オーダーのステータスが**開始済**であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="42eef-248">Notice that the status of the production order is now **Started**.</span></span> <span data-ttu-id="42eef-249">工程 10 の材料は、ピッキング リスト仕訳帳の自動転記で消費されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-249">The materials for operation 10 are consumed by an automatic posting of the picking list journal.</span></span> <span data-ttu-id="42eef-250">工程 10 の時間消費量は、工順カード仕訳帳の自動転記で扱われます。</span><span class="sxs-lookup"><span data-stu-id="42eef-250">Time consumption for operation 10 is accounted for by an automatic posting of a route card journal.</span></span>

32. <span data-ttu-id="42eef-251">工程 20 の倉庫作業を処理する倉庫アプリを開始します。</span><span class="sxs-lookup"><span data-stu-id="42eef-251">Start the warehouse app to process the warehouse work for operation 20.</span></span>

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. <span data-ttu-id="42eef-252">アクション ウィンドウの、**新しい製造オーダー**タブで、**開始**を選択して**開始**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-252">On the Action Pane, on the **Production order** tab, select **Start** to open the **Start** dialog box.</span></span>
34. <span data-ttu-id="42eef-253">**一般**タブで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-253">On the **General** tab, specify the following values:</span></span>

    - <span data-ttu-id="42eef-254">**開始工程番号**</span><span class="sxs-lookup"><span data-stu-id="42eef-254">In the **From Oper. No.**</span></span> <span data-ttu-id="42eef-255">フィールドで、**20** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-255">field, select **20**.</span></span>
    - <span data-ttu-id="42eef-256">**終了工程番号**</span><span class="sxs-lookup"><span data-stu-id="42eef-256">In the **To Oper. No.**</span></span> <span data-ttu-id="42eef-257">フィールドで、**20** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-257">field, select **20**.</span></span>
    - <span data-ttu-id="42eef-258">**数量**フィールドに **10** と入力します。</span><span class="sxs-lookup"><span data-stu-id="42eef-258">In the **Quantity** field, enter **10**.</span></span>
    - <span data-ttu-id="42eef-259">**ピッキング リスト転記**オプションを**いいえ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-259">Set the **Post picking list now** option to **No**.</span></span>

    ![一般タブで設定されている値](./media/subcontract24_general-tab.png)

35. <span data-ttu-id="42eef-261">**OK** を選択して、**開始**ダイアログ ボックスを閉じ、**すべての製造オーダー**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-261">Select **OK** to close the **Start** dialog box and return to the **All production orders** page.</span></span>

    <span data-ttu-id="42eef-262">コーティング工程、およびサービス品目に使用される材料のピッキング リストが作成されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-262">A picking list is created for the materials that are used for the Coating operation, and for the service item.</span></span> <span data-ttu-id="42eef-263">サービス品目は外注作業の原価を表します。</span><span class="sxs-lookup"><span data-stu-id="42eef-263">The service item represents the cost of the subcontracted operation.</span></span>

36. <span data-ttu-id="42eef-264">アクション ウィンドウの、**表示**タブで、**ピッキング リスト**を選択して**ピッキング リスト**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-264">On the Action Pane, on the **View** tab, select **Picking list** to open the **Picking list** page.</span></span>
37. <span data-ttu-id="42eef-265">転記されていないピッキング リストを選択し、仕訳帳明細行を表示する仕訳帳番号を選択します。</span><span class="sxs-lookup"><span data-stu-id="42eef-265">Select the picking list that isn't posted, and then select the journal number to view the journal lines.</span></span>

    ![ピッキング リスト ページの仕訳帳明細行](./media/subcontract25_picking-list.png)

38. <span data-ttu-id="42eef-267">アクション ウィンドウで、**印刷** \> **ピッキング リスト レポート**を選択し、**ピッキング リスト レポート**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-267">On the Action Pane, select **Print** \> **Picking list report** to open the **Picking list report** dialog box.</span></span>
39. <span data-ttu-id="42eef-268">**納品書レイアウトの使用**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-268">Set the **Use delivery note layout** option to **Yes**.</span></span>

    ![ピッキング リスト レポート ダイアログ ボックス](./media/subcontract26_picking-list-report-dialog.png)

40. <span data-ttu-id="42eef-270">**OK** を選択して**ピッキング リスト**レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="42eef-270">Select **OK** to generate a **Picking list** report.</span></span>

    <span data-ttu-id="42eef-271">この場合、仕入先納品書は生産ピッキング リスト仕訳帳から印刷されます。</span><span class="sxs-lookup"><span data-stu-id="42eef-271">In this case, a vendor delivery note is printed from the production picking list journal.</span></span> <span data-ttu-id="42eef-272">納品書では、コーティング工程を行う仕入先に出荷される材料を指定します。</span><span class="sxs-lookup"><span data-stu-id="42eef-272">The delivery note specifies the materials that are shipped to the vendor who will do the Coating operation.</span></span>

    ![ピッキング リスト レポート](./media/subcontract27_picking-list-report.png)

41. <span data-ttu-id="42eef-274">**ピッキング リスト**レポートを閉じ、**ピッキング リスト**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-274">Close the **Picking list** report to return to the **Picking list** page.</span></span>
42. <span data-ttu-id="42eef-275">アクション ウィンドウで、**転記**を選択して**仕訳帳の転記**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-275">On the Action Pane, select **Post** to open the **Post journal** dialog box.</span></span>

    ![転記仕訳帳ダイアログ ボックス](./media/subcontract28_post-journal-dialog.png)

43. <span data-ttu-id="42eef-277">**OK** を選択して**転記仕訳帳**ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="42eef-277">Select **OK** to close the **Post journal** dialog box.</span></span>
44. <span data-ttu-id="42eef-278">発注書を開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-278">Open the purchase order.</span></span>

    ![発注書ページ](./media/subcontract29_purchase-order-page.png)

45. <span data-ttu-id="42eef-280">アクション ウィンドウの、**購買**タブで**確認**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="42eef-280">On the Action Pane, on the **Purchase** tab, select **Confirm**.</span></span>
46. <span data-ttu-id="42eef-281">**転記**を選択して**転記仕訳帳**ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="42eef-281">Select **Post** to open the **Post journal** dialog box.</span></span>
47. <span data-ttu-id="42eef-282">**OK** を選択して、**転記仕訳帳**ダイアログ ボックスを閉じ、**発注書**ページに戻ります。</span><span class="sxs-lookup"><span data-stu-id="42eef-282">Select **OK** to close the **Post journal** dialog box and return to the **Purchase order** page.</span></span>
48. <span data-ttu-id="42eef-283">単価を **33** から **40** に変更します。</span><span class="sxs-lookup"><span data-stu-id="42eef-283">Change the unit price from **33** to **40**.</span></span>

    ![発注書ページで変更された単価](./media/subcontract30_unit-price.png)

49. <span data-ttu-id="42eef-285">発注書を再度確認します。</span><span class="sxs-lookup"><span data-stu-id="42eef-285">Confirm the purchase order again.</span></span>
50. <span data-ttu-id="42eef-286">製品受領書。</span><span class="sxs-lookup"><span data-stu-id="42eef-286">Product receipt.</span></span>

    ![製品受領書ダイアログ ボックスの転記](./media/subcontract31_posting-product-receipt-dialog.png)

51. <span data-ttu-id="42eef-288">仕入請求書。</span><span class="sxs-lookup"><span data-stu-id="42eef-288">Purchase invoice.</span></span>
52. <span data-ttu-id="42eef-289">照合状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="42eef-289">Update the match status.</span></span>

    ![仕入先請求ページ](./media/subcontract32_vendor-invoice-page.png)

53. <span data-ttu-id="42eef-291">完了レポート。</span><span class="sxs-lookup"><span data-stu-id="42eef-291">Report as finished.</span></span>

    ![完了レポート ダイアログ ボックス](./media/subcontract33_report-as-finished-dialog.png)

54. <span data-ttu-id="42eef-293">終了。</span><span class="sxs-lookup"><span data-stu-id="42eef-293">End.</span></span>

    ![終了ダイアログ ボックス](./media/subcontract34_end-dialog.png)

55. <span data-ttu-id="42eef-295">原価の比較。</span><span class="sxs-lookup"><span data-stu-id="42eef-295">Cost comparison.</span></span>

    ![原価の比較チャート](./media/subcontract35_cost-comparison-charts.png)

<span data-ttu-id="42eef-297">データの設定がありません。</span><span class="sxs-lookup"><span data-stu-id="42eef-297">Missing setup in data.</span></span>
