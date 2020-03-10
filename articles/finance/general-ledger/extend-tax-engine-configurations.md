---
title: 税エンジン コンフィギュレーションの拡張
description: このトピックでは、税エンジンのコンフィギュレーションの拡張について説明します。
author: yijialuan
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable
audience: IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: India
ms.author: riluan
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 53dd729fe36e21ea60d65019afd3d33dfc5c8de1
ms.sourcegitcommit: 4f668b23f5bfc6d6502858850d2ed59d7a79cfbb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/14/2020
ms.locfileid: "3059389"
---
# <a name="extend-tax-engine-configurations"></a><span data-ttu-id="5c80c-103">税エンジン コンフィギュレーションの拡張</span><span class="sxs-lookup"><span data-stu-id="5c80c-103">Extend tax engine configurations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c80c-104">[税エンジン](tax-engine.md) (GTE とも呼ばれます) では、法的要件および業務要件に基づいて、税の適用、計算、転記、および決済を決定する税ルールを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-104">The [Tax engine](tax-engine.md) (also referred to as GTE) lets you configure tax rules that determine tax applicability, calculation, posting, and settlement, based on legal and business requirements.</span></span> <span data-ttu-id="5c80c-105">このトピックでは、インドに適用される次のシナリオを使用して、税エンジン コンフィギュレーション拡張プロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-105">This topic walks you through the Tax engine configuration extension process using the following example scenarios that apply to India.</span></span>

-   <span data-ttu-id="5c80c-106">連邦直轄領商品およびサービス税 (UTGST) の税エンジンのコンフィギュレーションを拡張します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-106">Extend the Tax engine configuration for Union Territory Goods and Services Tax (UTGST).</span></span>
-   <span data-ttu-id="5c80c-107">参照モデルを使用すると、さまざまな国/地域からの商品輸入の注文の税率の基本的な関税 (BCD) を適用できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-107">Use a reference model to apply a tax rate of Basic Customs Duty (BCD) for import order of goods from different countries/regions.</span></span>

> [!NOTE]
> <span data-ttu-id="5c80c-108">税エンジン機能は、インドに基本住所がある法人に対してのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-108">The Tax engine functionality is only available for legal entities with a primary address in India.</span></span>

<span data-ttu-id="5c80c-109">次の税用語がこのトピックで使用されます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-109">The following tax terms are mentioned in this topic.</span></span>

|<span data-ttu-id="5c80c-110">税用語</span><span class="sxs-lookup"><span data-stu-id="5c80c-110">Tax term</span></span> | <span data-ttu-id="5c80c-111">完全名</span><span class="sxs-lookup"><span data-stu-id="5c80c-111">Full name</span></span>|
|-----|-----------|
|<span data-ttu-id="5c80c-112">販売税</span><span class="sxs-lookup"><span data-stu-id="5c80c-112">GST</span></span> | <span data-ttu-id="5c80c-113">商品およびサービス税</span><span class="sxs-lookup"><span data-stu-id="5c80c-113">Goods and services Tax</span></span>|
|<span data-ttu-id="5c80c-114">UTGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-114">UTGST</span></span> | <span data-ttu-id="5c80c-115">連邦直轄領商品及びサービス税</span><span class="sxs-lookup"><span data-stu-id="5c80c-115">Union Territory Goods and Services Tax</span></span>|
|<span data-ttu-id="5c80c-116">CGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-116">CGST</span></span> | <span data-ttu-id="5c80c-117">中央商品及びサービス税</span><span class="sxs-lookup"><span data-stu-id="5c80c-117">Central Goods and Services Tax</span></span>|
|<span data-ttu-id="5c80c-118">IGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-118">IGST</span></span> | <span data-ttu-id="5c80c-119">統合商品及びサービス税</span><span class="sxs-lookup"><span data-stu-id="5c80c-119">Integrated Goods and Services Tax</span></span> |
|<span data-ttu-id="5c80c-120">BCD</span><span class="sxs-lookup"><span data-stu-id="5c80c-120">BCD</span></span>| <span data-ttu-id="5c80c-121">基本関税</span><span class="sxs-lookup"><span data-stu-id="5c80c-121">Basic Customs Duty</span></span>|

## <a name="prerequisites"></a><span data-ttu-id="5c80c-122">必要条件</span><span class="sxs-lookup"><span data-stu-id="5c80c-122">Prerequisites</span></span>
<span data-ttu-id="5c80c-123">シナリオ例の作成に取りかかる前に、次の作業を完了させてください。 [税エンジン インポート コンフィギュレーション](tax-engine-import-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="5c80c-123">Before you can complete the example scenarios, complete the following tasks, [Tax engine import configuration](tax-engine-import-configuration.md).</span></span>

### <a name="add-a-configuration-provider-and-make-it-the-active-provider"></a><span data-ttu-id="5c80c-124">コンフィギュレーション プロバイダーを追加し、アクティブなプロバイダーとする。</span><span class="sxs-lookup"><span data-stu-id="5c80c-124">Add a configuration provider and make it the active provider</span></span>
1. <span data-ttu-id="5c80c-125">**組織管理** > **ワークスペース** > **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-125">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span>
2. <span data-ttu-id="5c80c-126">**コンフィギュレーション プロバイダー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-126">Click **Configuration providers**.</span></span>
3. <span data-ttu-id="5c80c-127">新しいコンフィギュレーション プロバイダーを作成し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-127">Create a new configuration provider and close the page.</span></span>
4. <span data-ttu-id="5c80c-128">作成したコンフィギュレーション プロバイダーで、**...** > **有効な設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-128">Click **...** > **Set active** on the configuration provider that you created.</span></span>

![アクティブ ソリューション](media/gte-extension-active-solution.png)

## <a name="scenario-1-extend-the-tax-engine-configuration-for-utgst"></a><span data-ttu-id="5c80c-130">シナリオ 1 : UTGST 用税コンフィギュレーションを拡張する</span><span class="sxs-lookup"><span data-stu-id="5c80c-130">Scenario 1: Extend the Tax engine configuration for UTGST</span></span>

<span data-ttu-id="5c80c-131">議会を持たない連邦直轄領のため、GST 評議会は SGST に相当する、UTGST を導入しました。</span><span class="sxs-lookup"><span data-stu-id="5c80c-131">For union territories that don’t have a legislature, the GST Council introduced UTGST, which is comparable to SGST.</span></span> <span data-ttu-id="5c80c-132">インドの次の連邦直轄領に UTGST が適用されます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-132">UTGST applies to the following union territories of India:</span></span>

-   <span data-ttu-id="5c80c-133">Chandigarh</span><span class="sxs-lookup"><span data-stu-id="5c80c-133">Chandigarh</span></span>
-   <span data-ttu-id="5c80c-134">Lakshadweep</span><span class="sxs-lookup"><span data-stu-id="5c80c-134">Lakshadweep</span></span>
-   <span data-ttu-id="5c80c-135">Daman および Diu</span><span class="sxs-lookup"><span data-stu-id="5c80c-135">Daman and Diu</span></span>
-   <span data-ttu-id="5c80c-136">Dadra および Nagar Haveli</span><span class="sxs-lookup"><span data-stu-id="5c80c-136">Dadra and Nagar Haveli</span></span>
-   <span data-ttu-id="5c80c-137">Andaman および Nicobar Islands</span><span class="sxs-lookup"><span data-stu-id="5c80c-137">Andaman and Nicobar Islands</span></span>

<span data-ttu-id="5c80c-138">SGST は、独自の議会を持ち、販売税プロセスにおいて「州」と見なされるニューデリーや Puducherry などの連邦直轄領にも適用できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-138">SGST can also be applied in union territories such as New Delhi and Puducherry, which have their own legislatures and can be considered “states” per the GST process.</span></span>

<span data-ttu-id="5c80c-139">UTGSTでは、任意の取引で税金の次の組み合わせを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-139">For UTGST, the following combinations of taxes can be applied for any transaction:</span></span>

-   <span data-ttu-id="5c80c-140">州内での商品やサービス (イントラスタット) の供給: CGST + SGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-140">Supply of goods and services within a state (intrastate): CGST + SGST</span></span>
-   <span data-ttu-id="5c80c-141">連邦直轄領内での商品やサービスの供給 (イントラ -UT) : CGST + UTGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-141">Supply of goods and services within union territories (intra-UT): CGST + UTGST</span></span>
-   <span data-ttu-id="5c80c-142">州または連邦直轄領にまたがる商品やサービスの供給 (イントラスタット/イントラ -UT) : IGST</span><span class="sxs-lookup"><span data-stu-id="5c80c-142">Supply of goods and services across states or union territories (interstate/inter-UT): IGST</span></span>

<span data-ttu-id="5c80c-143">UTGST のインプット タックス クレジット の使用率の順序は、SGST の インプット タックス クレジットの場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c80c-143">The order of utilization for the Input Tax Credit of UTGST is the same as it is for the Input Tax Credit of SGST.</span></span> <span data-ttu-id="5c80c-144">そのため、SGST または UTGST のインプット タックス クレジットは、ず SGST または UTGST、に対してそれぞれ設定されます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-144">Therefore, Input Tax Credit of SGST or UTGST is first set off against SGST or UTGST, respectively.</span></span> <span data-ttu-id="5c80c-145">出力税負債、および、残高は IGST 出力税負債に対して設定できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-145">The Output Tax liabilities and any balance can be set off against IGST Output Tax liabilities.</span></span>

<span data-ttu-id="5c80c-146">このシナリオでは、次の作業を完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="5c80c-146">To support this scenario, you must complete the following tasks:</span></span>
1. [<span data-ttu-id="5c80c-147">拡張コンフィギュレーションを作成します</span><span class="sxs-lookup"><span data-stu-id="5c80c-147">Create extension configurations</span></span>](#create-extension-configurations)  
2. [<span data-ttu-id="5c80c-148">課税対象のドキュメントを拡張して、IntraStateInUnionTerritory フラグを含むようにします</span><span class="sxs-lookup"><span data-stu-id="5c80c-148">Extend the taxable document so that it includes the IntraStateInUnionTerritory flag</span></span>](#extend-the-taxable-document-so-that-it-includes-the-intrastateinunionterritory-flag)
3. [<span data-ttu-id="5c80c-149">拡張された課税対象のドキュメントのデータ マッピングを完了します</span><span class="sxs-lookup"><span data-stu-id="5c80c-149">Complete data mapping for the extended taxable document</span></span>](#complete-data-mapping-for-the-extended-taxable-document)
4. [<span data-ttu-id="5c80c-150">税 (インド販売税 Contoso) のデータ モデルを変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-150">Change the data model of Tax (India GST Contoso)</span></span>](#change-the-data-model-of-tax-india-gst-contoso)
5. [<span data-ttu-id="5c80c-151">州販売税 (SGST) の適用条件を変更します</span><span class="sxs-lookup"><span data-stu-id="5c80c-151">Change the applicability of State GST (SGST)</span></span>](#change-the-applicability-of-sgst)
6. [<span data-ttu-id="5c80c-152">UTGST タスク コンポーネントを構成します</span><span class="sxs-lookup"><span data-stu-id="5c80c-152">Configure the UTGST task component</span></span>](#configure-the-utgst-tax-component)
7. [<span data-ttu-id="5c80c-153">UTGST を含めるための明細行の式を変更します</span><span class="sxs-lookup"><span data-stu-id="5c80c-153">Modify the formulas of lines to include UTGST</span></span>](#modify-the-formulas-of-lines-to-include-utgst)
8. [<span data-ttu-id="5c80c-154">税に関する文書のコンフィギュレーションを完了します</span><span class="sxs-lookup"><span data-stu-id="5c80c-154">Complete the tax document configuration</span></span>](#complete-the-tax-document-configuration)
9. [<span data-ttu-id="5c80c-155">拡張されたコンフィギュレーションをインポートし、特定の会社に配置します</span><span class="sxs-lookup"><span data-stu-id="5c80c-155">Import the extended configuration and deploy it to a specific company</span></span>](#import-the-configuration-and-deploy-it-to-a-specific-company) 


### <a name="create-extension-configurations"></a><span data-ttu-id="5c80c-156">拡張機能のコンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="5c80c-156">Create extension configurations</span></span>
<span data-ttu-id="5c80c-157">拡張機能のコンフィギュレーションを作成するには、次の手順が必要です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-157">The following steps are needed to create extension configurations:</span></span>
-   <span data-ttu-id="5c80c-158">課税対象のドキュメント (インド) から派生した新しい課税対象ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-158">Create a new taxable document that is derived from Taxable Document (India)</span></span>
-   <span data-ttu-id="5c80c-159">課税対象のドキュメント (インド販売税) から派生した新しい課税対象ドキュメントを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-159">Create a new tax document that is derived from Tax (India GST)</span></span>

1. <span data-ttu-id="5c80c-160">**ローカライズ コンフィギュレーション**ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして**税のコンフィギュレーション**。</span><span class="sxs-lookup"><span data-stu-id="5c80c-160">In the **Localization configurations** workspace (**Organization administration** > **Workspaces** > **Electronic reporting**), click **Tax configurations**.</span></span>
2. <span data-ttu-id="5c80c-161">ツリーで、**課税対象のドキュメント (インド)** コンフィギュレーションを見つけ、**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-161">In the tree, find the **Taxable Document (India)** configuration, and then click **Create configuration**.</span></span>
3. <span data-ttu-id="5c80c-162">**課税対象のドキュメント モデルから派生**オプションを選択し、名前と、派生課税対象ドキュメントの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-162">Select the **Derive from Taxable document model** option, and then enter a name and description for the derived taxable document.</span></span> <span data-ttu-id="5c80c-163">たとえば、**課税対象のドキュメント (インド Contoso)** と名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-163">For this example, enter the name **Taxable Document (India Contoso)**.</span></span>
4. <span data-ttu-id="5c80c-164">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-164">Click **Create configuration**.</span></span>
5. <span data-ttu-id="5c80c-165">ツリーで、**税 (インド販売税)** コンフィギュレーションを選択し、**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-165">In the tree, select the **Tax (India GST)** configuration, and then click **Create configuration**.</span></span>
6. <span data-ttu-id="5c80c-166">**税コンフィギュレーションから派生**オプションを選択し、名前と、派生課税対象ドキュメントの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-166">Select the **Derive from Tax configuration** option, and then enter a name and description for the derived tax document.</span></span> <span data-ttu-id="5c80c-167">たとえば、**税 (インドContoso)** と名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-167">For this example, enter the name **Tax (India GST Contoso)**.</span></span>
7. <span data-ttu-id="5c80c-168">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-168">Click **Create configuration**.</span></span>

### <a name="extend-the-taxable-document-so-that-it-includes-the-intrastateinunionterritory-flag"></a><span data-ttu-id="5c80c-169">課税対象のドキュメントを拡張して、IntraStateInUnionTerritory フラグを含むようにします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-169">Extend the taxable document so that it includes the IntraStateInUnionTerritory flag.</span></span>

<span data-ttu-id="5c80c-170">**IntraStateInUnionTerritory** フラグを**課税対象のドキュメント (インド Contoso)** に追加するため、次の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-170">Complete the following steps to add the **IntraStateInUnionTerritory** flag to **Taxable Document (India Contoso)**.</span></span>

 1. <span data-ttu-id="5c80c-171">ツリーで、[拡張機能コンフィギュレーションの作成](#create-extension-configurations)で作成した**課税対象のドキュメント (インド Contoso)** コンフィギュレーションを見つけ、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-171">In the tree, find the **Taxable Document (India Contoso)** configuration that you created in [Create extension configurations](#create-extension-configurations), and then click **Designer**.</span></span>
 2. <span data-ttu-id="5c80c-172">ツリーで、**課税対象のドキュメント** > **ヘッダー** > **明細行**と移動し、**新規**をクリックして新しいノードを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-172">In the tree, go to **Taxable document** > **Header** > **Lines**, and then click **New** to create a new node.</span></span>
 3. <span data-ttu-id="5c80c-173">ノードの名前を入力し、アイテムの種類を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-173">Enter a name for the node, and select the item type:</span></span>
    -   <span data-ttu-id="5c80c-174">**名前:** IntraStateInUnionTerritory</span><span class="sxs-lookup"><span data-stu-id="5c80c-174">**Name:** IntraStateInUnionTerritory</span></span>
    -   <span data-ttu-id="5c80c-175">**アイテムの種類:** Enum</span><span class="sxs-lookup"><span data-stu-id="5c80c-175">**Item type:** Enum</span></span>

    ![新しいノードの作成](media/gte-create-node-tax-document.png)

 4. <span data-ttu-id="5c80c-177">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-177">Click **Add**.</span></span>
 5. <span data-ttu-id="5c80c-178">**ノード** クイック タブで、**項目参照を切り替える**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-178">On the **Node** FastTab, click **Switch item reference**.</span></span>
 6. <span data-ttu-id="5c80c-179">ツリーで **NoYes** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-179">Select **NoYes** in the tree, and then click **OK**.</span></span>
 7. <span data-ttu-id="5c80c-180">コンフィギュレーションを保存し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-180">Save the configuration, and close the designer.</span></span>
 8. <span data-ttu-id="5c80c-181">ツリーで選択されている**課税対象のドキュメント (インド Contoso)** で、**バージョン**リストにある**ステータスを変更** > **完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-181">With **Taxable Document (India Contoso)** still selected in the tree, click **Change status** > **Complete** in the **Versions** list.</span></span>

    ![コンフィギュレーションの状態の更新](media/gte-change-configuration-status.png)

 9. <span data-ttu-id="5c80c-183">**UTGST** のように説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-183">Enter a description such as **UTGST**, and then click **OK**.</span></span>
 10. <span data-ttu-id="5c80c-184">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-184">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>
 11. <span data-ttu-id="5c80c-185">ステータスが**完了**に更新されると、コンフィギュレーションを配置できる状態です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-185">After the status is updated to **Complete**, the configuration is ready for deployment.</span></span>

### <a name="complete-data-mapping-for-the-extended-taxable-document"></a><span data-ttu-id="5c80c-186">拡張された課税対象ドキュメントのデータ マッピングを完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-186">Complete data mapping for the extended taxable document</span></span>
<span data-ttu-id="5c80c-187">発注書または販売注文、および課税対象のドキュメントでの参照モードなどの各課税対象ドキュメントのデータ マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-187">There are data mappings for each taxable document, such as a purchase order or sales order, and reference mode in the taxable document.</span></span> <span data-ttu-id="5c80c-188">データ マッピングの目的は、課税対象取引から取得した値を GTE に渡し、税の適用または税の計算に使用することです。</span><span class="sxs-lookup"><span data-stu-id="5c80c-188">The purpose of data mapping is to get the value from taxable transactions and pass it into GTE for tax applicability or tax calculation.</span></span> <span data-ttu-id="5c80c-189">利便性のために、**課税対象ドキュメント ソース**と呼ばれ、課税金額、HSN、SAC などの最も一般的な税に関連するフィールドをカプセル化する特別なデータ ソースがあります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-189">For convenience, there is a special data source called **Taxable document source**, which encapsulates most common tax relevant fields like assessable value, HSN, or SAC.</span></span> <span data-ttu-id="5c80c-190">したがって、拡張課税対象ドキュメントに追加のフィールドの値を取得し、マップするための2つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-190">So, there are two methods for retrieving and mapping the value of the additional field to your extended taxable document.</span></span>

-   <span data-ttu-id="5c80c-191">方法 1 : 既存の課税対象ドキュメントのソースで追加のフィールドを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-191">Method 1: Enable the additional field for the existing taxable document source.</span></span>
-   <span data-ttu-id="5c80c-192">方法 2 : 電子レポート (ER) データ マッピングを使用します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-192">Method 2: Use Electronic reporting (ER) data mapping.</span></span>

#### <a name="method-1-data-mapping-by-taxable-document-source"></a><span data-ttu-id="5c80c-193">方法 1 : 課税対象ドキュメントのソースによるデータ マッピング</span><span class="sxs-lookup"><span data-stu-id="5c80c-193">Method 1: Data mapping by taxable document source</span></span>
<span data-ttu-id="5c80c-194">この方法を使用する前に、[税エンジンの統合](tax-engine-integration.md)を必ず読み、基になる概念を理解するようにします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-194">Before you use this method, be sure to read about [Tax engine integration](tax-engine-integration.md) so you understand the underlying concepts.</span></span> <span data-ttu-id="5c80c-195">税エンジンでは、州か連邦直轄領かを識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-195">The Tax engine must determine whether a state is a union territory.</span></span> <span data-ttu-id="5c80c-196">したがってこの方法は、データ プロバイダーを変更し、税エンジンにこの情報を提供するようにします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-196">Therefore, in this method, you will modify the data provider so that it provides this information to the Tax engine.</span></span>

1. <span data-ttu-id="5c80c-197">州マスターの連邦直轄領の名前を検索します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-197">Find the system name of the Union Territory of State master.</span></span>
    1. <span data-ttu-id="5c80c-198">**組織管理** > **グローバル アドレス帳** > **アドレス** > **アドレスの設定**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-198">Go to **Organization administration** > **Global address book** > **Addresses** > **Address setup**.</span></span> 
    2. <span data-ttu-id="5c80c-199">**連邦直轄領**列を右クリックし、**フォーム情報** > **フォーム名: LogisticsAddressSetup** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-199">Right-click the **Union territory** column, and then click **Form information** > **Form Name: LogisticsAddressSetup**.</span></span> <span data-ttu-id="5c80c-200">たとえば、列のシステムの名前が **LogisticsAddressState.UnionTerritory_IN** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-200">For this example, notice that the system name for the column is **LogisticsAddressState.UnionTerritory_IN**.</span></span>

    ![連邦直轄領の GTE 拡張](media/gte-extension-union-territory-form-info.png)

2. <span data-ttu-id="5c80c-202">連邦直轄領内のイントラスタット取引の税エンジン モデル フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-202">Add a tax engine model field for intrastate transactions in a union territory.</span></span>

    <span data-ttu-id="5c80c-203">モデル アプリケーション スイートの新しいプロジェクトを作成し、新しいクラスである TaxableDocRowDPExtLineSubscriberSample を追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-203">Create a new project of model Application Suite, and add the new class, TaxableDocRowDPExtLineSubscriberSample.</span></span> <span data-ttu-id="5c80c-204">取引が連邦直轄領内のイントラスタット取引かどうかを判断し、フラグを GTE に渡すための以下のロジックを実装します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-204">Implement the following logic to determine if a transaction is an intrastate transaction in a union territory and pass the flag to GTE.</span></span>
   
    ```xpp   
    public class TaxableDocRowDPExtLineSubscriberSample
    {
        public static const str IsIntraStateInUnionTerritory = 'IntraStateInUnionTerritory';

        [SubscribesTo(classStr(TaxableDocRowDataProviderExtensionLine),               delegateStr(TaxableDocRowDataProviderExtensionLine, initExtensionFieldsForLine))]
        public static void initExtensionFieldsForLine(TaxableDocumentValidFields _validFields)
        {
        _validFields.add(IsIntraStateInUnionTerritory, Types::Enum, enumNum(NoYes));
        }

        [SubscribesTo(classStr(TaxableDocRowDataProviderExtensionLine), delegateStr(TaxableDocRowDataProviderExtensionLine, fillInExtensionFieldsForLine))]
        public static void fillInExtensionFieldsForLine(TaxableDocumentLineObject _lineObj)
        {
        _lineObj.setFieldValue(IsIntraStateInUnionTerritory, TaxableDocRowDPExtLineSubscriberSample::IsIntraStateWithUnionTerritory(_lineObj), enumNum(NoYes));
        }

        private static NoYes IsIntraStateWithUnionTerritory(TaxableDocumentLineObject _lineObj)
        {
        boolean                     isIntraStateWithUnionTerritory = NoYes::No;
        LogisticsPostalAddress      partyAddress;
        LogisticsPostalAddress      taxAddress;
        LogisticsAddressState       partyState;
        SalesPurchJournalLine       documentLineMap;                TaxModelTaxable_IN          taxModelTaxable;
        documentLineMap = SalesPurchJournalLine::findRecId(_lineObj.getTransactionLineTableId(), _lineObj.getTransactionLineRecordId());
        taxModelTaxable = TaxModelDocLineFactory_IN::newTaxModelDocLine(documentLineMap);
        partyAddress = taxModelTaxable.getPartyLogisticsPostalAddress();
        taxAddress = taxModelTaxable.getTaxLogisticsPostalAddressTable();
        if (partyAddress && taxAddress
            && partyAddress.CountryRegionId == taxAddress.CountryRegionId
            && partyAddress.State != ''
            && taxAddress.State != ''
            && partyAddress.State == taxAddress.State)
        {
            partyState = LogisticsAddressState::find(partyAddress.CountryRegionId, partyAddress.State);
                isIntraStateWithUnionTerritory = partyState.UnionTerritory_IN;
        }
        return isIntraStateWithUnionTerritory;
        }

    }
    ```

3. <span data-ttu-id="5c80c-205">デザイナーでのデータ連結を実行します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-205">Complete the data binding in the Designer.</span></span>
   1. <span data-ttu-id="5c80c-206">**課税対象ドキュメント (インド Contoso)** コンフィギュレーションに移動し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-206">Navigate to the **Taxable Document (India Contoso)** configuration, and then click **Designer**.</span></span>

      ![税コンフィギュレーション デザイナー](media/gte-extension-tax-configuration-designer.png)

   2. <span data-ttu-id="5c80c-208">**データ ソースへのマップ モデル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-208">Click **Map model to datasource**</span></span>
   3. <span data-ttu-id="5c80c-209">発注書または販売注文など、それぞれの課税対象ドキュメントと参照モデルのためのたくさんのデータ マッピングがあります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-209">You will find there are lots of data mapping for each taxable document and reference model, like purchase order or sales order.</span></span> <span data-ttu-id="5c80c-210">ビジネスの要求に応じて、データ マッピングを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-210">You need to do your data mapping per your business requirement.</span></span> <span data-ttu-id="5c80c-211">例:</span><span class="sxs-lookup"><span data-stu-id="5c80c-211">For example:</span></span>
      1. <span data-ttu-id="5c80c-212">販売注文明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-212">Select a sales order document line.</span></span>
      2. <span data-ttu-id="5c80c-213">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-213">Click **Designer**.</span></span>

         ![データ マッピング](media/gte-extension-data-mapping.png)

   4. <span data-ttu-id="5c80c-215">1 ~ 5 の手順を実行した後、データ ソースの、**販売注文** > **ヘッダー** > **明細行**の下に、**IntraStateInUnionTerritory** を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-215">After completing steps 1-5, you should be able to find the field **IntraStateInUnionTerritory** in the data source under **Sales order** > **Header** > **Lines**.</span></span> <span data-ttu-id="5c80c-216">このフィールドを、課税対象のドキュメントの **IntraStateInUnionTerritory:Enumeration** 値に連結することができます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-216">You can bind this field to the **IntraStateInUnionTerritory:Enumeration** value in the taxable document.</span></span>

      ![データ バインディング](media/gte-extension-data-binding.png)

   5. <span data-ttu-id="5c80c-218">コンフィギュレーションを保存し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-218">Save the configuration, and close the designer.</span></span>
   6. <span data-ttu-id="5c80c-219">**コンフィギュレーション** ワークスペースで、**ステータスを変更** > **完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-219">In the **Configurations** workspace, click **Change status** > **Complete**.</span></span>

      ![コンフィギュレーション状態の変更](media/gte-change-configuration-status.png)

   7. <span data-ttu-id="5c80c-221">**UTGST** のように説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-221">Enter a description such as **UTGST**, and then click **OK**.</span></span>
   8. <span data-ttu-id="5c80c-222">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-222">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>

#### <a name="method-2-data-mapping-using-the-er-model-mapping-designer"></a><span data-ttu-id="5c80c-223">方法 2 : ER モデル マッピング デザイナーを使用してデータ マッピングします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-223">Method 2: Data mapping using the ER model mapping designer</span></span>
<span data-ttu-id="5c80c-224">この方法を使用する前に、ER およびテーブルの関係、クラス、および発注書に関するメソッドに精通するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="5c80c-224">Before you use this method, be sure that you are familiar with ER and the table relation, class, and method for purchase orders.</span></span> 
1. <span data-ttu-id="5c80c-225">発注書に対してモデル マッピング デザイナーを開き、**PurchLine** をルート データ ソースとしてテーブル レコードに追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-225">Open the model mapping designer for a purchase order, add table records **PurchLine** as a root data source.</span></span>

   ![Purchline 拡張機能](media/gte-extension-purchline.png)

2. <span data-ttu-id="5c80c-227">Data model\Enumeration **YesNo Global** および Dynamics 365 for Operations \Enumeration **NoYes** を追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-227">Add Data model\Enumeration **YesNo Global** and Dynamics 365 for Operations\Enumeration **NoYes**.</span></span>

   ![列挙型の追加](media/gte-extension-add-enumerations.png)

3. <span data-ttu-id="5c80c-229">**データ ソース**ツリーで、**発注書** > **明細行**の下に計算済フィールドとして **$PurchLine** を追加し、既存の課税対象ドキュメントである**発注書**と **PurchLine** テーブル レコードの関係を構築します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-229">In the **Data Source** tree, add a calculated field **$PurchLine** under **purchase order** > **lines**  to build the connection between the existing taxable document **purchase order** and the table records **PurchLine**.</span></span> <span data-ttu-id="5c80c-230">**式の編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-230">Click **Edit formula**.</span></span>

   ![式の編集](media/gte-extension-edit-formula.png)

4. <span data-ttu-id="5c80c-232">**PurchLine** および**発注書**間の関係を記述する式を入力します:</span><span class="sxs-lookup"><span data-stu-id="5c80c-232">Input the formula that describe the relationship between **PurchLine** and **purchase order**:</span></span> 

   ```FIRST(FILTER(PurchLine, PurchLine.RecId='purchase order'.Header.Lines.RecId))```

   ![フォーミュラの追加](media/gte-extension-add-formula.png)

5. <span data-ttu-id="5c80c-234">**保存**をクリックし、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-234">Click **Save** and close the page.</span></span>
6. <span data-ttu-id="5c80c-235">**$PurchLine** で、計算済フィールド **\$IsIntraStateInUnionTerritory** を追加し、次の式を使用します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-235">Add the calculated field **\$IsIntraStateInUnionTerritory** in **$PurchLine**, and use the following formula.</span></span> 
   
   ```xpp
   AND('purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getPartyLogisticsPostalAddress.'>Relations'.State.StateId = 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getTaxLogisticsPostalAddress.'>Relations'.State.StateId, 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getPartyLogisticsPostalAddress.'>Relations'.State.UnionTerritory_IN = NoYesAx.Yes, 'purchase order'.'$PurchLine'.'initTaxModelDocLine_IN()'.getTaxLogisticsPostalAddress.'>Relations'.State.UnionTerritory_IN = NoYesAx.Yes)
   ```

7. <span data-ttu-id="5c80c-236">**モデル マッピング デザイナー**でマッピングを完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-236">In the **Model mapping designer**, complete the mapping:</span></span>
   1. <span data-ttu-id="5c80c-237">**Data Sources** ツリーで、**$IntraStateInUnionTerritory** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-237">In the **Data Sources** tree, select **$IntraStateInUnionTerritory**.</span></span>
   2. <span data-ttu-id="5c80c-238">**Data Model** ツリーで、**IntraStateInUnionTerritory** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-238">In the **Data Model**, select **IntraStateInUnionTerritory**.</span></span>
   3. <span data-ttu-id="5c80c-239">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-239">Click **Edit**.</span></span>

      ![データ マッピングの編集](media/gte-extension-data-binding2.png)

   4. <span data-ttu-id="5c80c-241">ブール値を、拡張課税対象ドキュメントの **IntraStateInUnionTerritory** フィールドで使用される列挙値に変換するために次の式を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-241">Input the following formula to convert the Boolean value to the enumeration value, which is used by the extended taxable document field **IntraStateInUnionTerritory**.</span></span>

      ```xpp
      CASE('purchase order'.'$PurchLine'.'$IsIntraStateInUnionTerritory', true, NoYesModel.Yes, false, NoYesModel.No)
      ```

   5. <span data-ttu-id="5c80c-242">**保存**をクリックし、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-242">Click **Save** and close the page.</span></span>

8. <span data-ttu-id="5c80c-243">コンフィギュレーションを保存し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-243">Save the configuration, and close the designer.</span></span>
9. <span data-ttu-id="5c80c-244">**コンフィギュレーション** ワークスペースで、**ステータスを変更** > **完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-244">In the **Configurations** workspace, click **Change status** > **Complete**.</span></span>

    ![コンフィギュレーション状態の変更](media/gte-change-configuration-status.png)

10. <span data-ttu-id="5c80c-246">**UTGST** のように説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-246">Enter a description such as **UTGST**, and then click **OK**.</span></span>
11. <span data-ttu-id="5c80c-247">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-247">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>

### <a name="change-the-data-model-of-tax-india-gst-contoso"></a><span data-ttu-id="5c80c-248">税 (インド販売税 Contoso) のデータ モデルを変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-248">Change the data model of Tax (India GST Contoso)</span></span>

1. <span data-ttu-id="5c80c-249">**税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-249">Go to the **Tax (India GST Contoso)** configuration and then click **Designer**.</span></span>
2. <span data-ttu-id="5c80c-250">**税務書類**をクリックして、データ モデルとして**課税対象ドキュメント (インド Contoso)** を選択し、データ モデル バージョンとして **1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-250">Click **Tax document**, and then select **Taxable Document (India Contoso)** as the data model, and select **1** as the data model version.</span></span>

    ![税務書類](media/gte-tax-document-designer.png)

3. <span data-ttu-id="5c80c-252">**保存**をクリックしてコンフィギュレーションを保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-252">Click **Save** to save the configuration.</span></span>

### <a name="change-the-applicability-of-sgst"></a><span data-ttu-id="5c80c-253">SGST の適用条件を変更</span><span class="sxs-lookup"><span data-stu-id="5c80c-253">Change the applicability of SGST</span></span>

1. <span data-ttu-id="5c80c-254">**税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**ドラフト**の状態になっているバージョンを選択し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-254">Go to the **Tax (India GST Contoso)** configuration, select the version that has a status of **Draft**, and then click **Designer**.</span></span>
2. <span data-ttu-id="5c80c-255">**税務書類** > **ヘッダー** > **明細行** > **販売税** > **SGST** と移動し、**ルックアップ**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-255">Go to **Tax document** > **Header** > **Lines** > **GST** > **SGST**, and then click the **Lookups** tab.</span></span>
3. <span data-ttu-id="5c80c-256">**列**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-256">Click **Columns**.</span></span>
4. <span data-ttu-id="5c80c-257">**利用可能な列**一覧から、**IntraStateInUnionTerritory** を選択し、右矢印ボタンをクリックして列を**選択した列**リストに移動させます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-257">Select **IntraStateInUnionTerritory** from the **Available columns** list, and then click the right arrow button to move the column to the **Selected columns** list.</span></span>
5. <span data-ttu-id="5c80c-258">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-258">Click **OK**.</span></span>
6. <span data-ttu-id="5c80c-259">**IntraStateInUnionTerritory** 列で、**いいえ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-259">For the **IntraStateInUnionTerritory** column, select **No**.</span></span>
7. <span data-ttu-id="5c80c-260">**保存**をクリックしてコンフィギュレーションを保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-260">Click **Save** to save the configuration.</span></span>

### <a name="configure-the-utgst-tax-component"></a><span data-ttu-id="5c80c-261">UTGST 税コンポーネントを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-261">Configure the UTGST tax component</span></span>

1. <span data-ttu-id="5c80c-262">**税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**ドラフト**の状態になっているバージョンを選択し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-262">Go to the **Tax (India GST Contoso)** configuration, select the version that has a status of **Draft**, and then click **Designer**.</span></span>
2. <span data-ttu-id="5c80c-263">UTGST 税コンポーネントを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-263">Add the UTGST tax component.</span></span>
    1. <span data-ttu-id="5c80c-264">**税務書類** > **ヘッダー** > **明細行** > **販売税** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-264">Go to **Tax document** > **Header** > **Lines** > **GST**.</span></span> <span data-ttu-id="5c80c-265">**追加**をクリックし、**税コンポーネント**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-265">Click **Add**, and then select **Tax component**.</span></span>
    2. <span data-ttu-id="5c80c-266">UTGST 税コンポーネントに名前と説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-266">Enter a name and description for the UTGST tax component, and then click **OK**.</span></span>
3. <span data-ttu-id="5c80c-267">UTGST 税コンポーネントの税措置を構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-267">Configure tax measures for the UTGST tax component.</span></span>
   1. <span data-ttu-id="5c80c-268">税務書類ツリーを展開し、UTGST 税コンポーネントをクリックして、措置を作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-268">Expand the tax document tree, and click the UTGST tax component to create a measure for.</span></span>
   2. <span data-ttu-id="5c80c-269">**追加** をクリックし、**税措置**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-269">Click **Add**, and then select **Tax measure**.</span></span>
   3. <span data-ttu-id="5c80c-270">UTGST の適用可能性以外、プロパティ、検索、式、転記の場合、および会計など、すべてのロジックは SGST の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c80c-270">All the logic, such as properties, lookups, formulas, postings, and accounting, except applicability of UTGST, is the same as it is for SGST.</span></span> <span data-ttu-id="5c80c-271">したがって、SGST で使用するすべての税基準を**名前**一覧で選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-271">Therefore, select all the tax measures that SGST uses in the **Name** list and then click **OK**.</span></span> 

      ![一覧表示されている措置](media/gte-utgst-list.png)

4. <span data-ttu-id="5c80c-273">ルックアップの率/パーセンテージを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-273">Configure rate/percentage lookups.</span></span>
    1. <span data-ttu-id="5c80c-274">**UTGST** 税コンポーネント ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-274">Expand the **UTGST** tax component node.</span></span>
    2. <span data-ttu-id="5c80c-275">**率/パーセンテージ**型の基準を選択する。</span><span class="sxs-lookup"><span data-stu-id="5c80c-275">Select the measure of the **Rate/Percentage** type.</span></span>
    3. <span data-ttu-id="5c80c-276">**ルックアップ** > **列**をクリックして、税率/パーセンテージの値に関連する属性の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-276">Click **Lookups** > **Columns** to see a list of the attributes that are relevant to the tax rate/percentage value.</span></span>
    4. <span data-ttu-id="5c80c-277">SGST が使用するのと同じ属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-277">Select the same attributes that SGST uses.</span></span>
        > [!Note]
        > <span data-ttu-id="5c80c-278">**追加**をクリックしないでください。</span><span class="sxs-lookup"><span data-stu-id="5c80c-278">Don’t click **Add**.</span></span> <span data-ttu-id="5c80c-279">ここで入力した値は、実際の単価表に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="5c80c-279">Values that you enter here have no effect on the actual rate table.</span></span> <span data-ttu-id="5c80c-280">そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定**で構成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-280">That table should be configured at **Tax** > **Tax configuration** > **Tax setup**.</span></span>

    5. <span data-ttu-id="5c80c-281">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-281">Save the tax document.</span></span>

5. <span data-ttu-id="5c80c-282">プロパティを構成する。</span><span class="sxs-lookup"><span data-stu-id="5c80c-282">Configure properties.</span></span>
   1. <span data-ttu-id="5c80c-283">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-283">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-284">**プロパティ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-284">Click the **Properties** tab.</span></span>
   2. <span data-ttu-id="5c80c-285">**条件**の横にある**編集** (鉛筆アイコン) クリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-285">Click **Edit** (the pencil icon) next to **Condition**.</span></span>
   3. <span data-ttu-id="5c80c-286">SGST が使用するのと同じ条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-286">Enter the same condition that SGST uses.</span></span>

      ![SGST 条件](media/gte-sgst-condition.png)

   4. <span data-ttu-id="5c80c-288">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-288">Save the tax document.</span></span>

6. <span data-ttu-id="5c80c-289">税の適用可能性のルックアップを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-289">Configure tax applicability lookups.</span></span>
    1. <span data-ttu-id="5c80c-290">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-290">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-291">**ルックアップ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-291">Click the **Lookup** tab.</span></span>
    2. <span data-ttu-id="5c80c-292">**列**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-292">Click **Columns**.</span></span>
    3. <span data-ttu-id="5c80c-293">**インポート オーダー**および **IntraStateInUnionTerritory** を参照列として選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-293">Select **Import Order** and **IntraStateInUnionTerritory** as lookup columns.</span></span>
    4. <span data-ttu-id="5c80c-294">**コンフィギュレーション** をソース タイプとして選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-294">Select **Configuration** as the source type.</span></span>
    5. <span data-ttu-id="5c80c-295">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-295">Click **Add**.</span></span> <span data-ttu-id="5c80c-296">**インポート オーダー**列には**いいえ**を選択し、**IntraStateInUnionTerritory** 列には**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-296">Select **No** for the **Import Order** column and select **Yes** for the **IntraStateInUnionTerritory** column.</span></span>   
    6. <span data-ttu-id="5c80c-297">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-297">Save the tax document.</span></span>

7. <span data-ttu-id="5c80c-298">コンフィギュレーション形式</span><span class="sxs-lookup"><span data-stu-id="5c80c-298">Configure formulas.</span></span> <span data-ttu-id="5c80c-299">式は、グループ ノードのレベル (行、税コンポーネントまたは税タイプ) または基準ノード レベルで構成できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-299">Formulas can be configured at either the group node level (line, tax component, or tax type) or the measure node level.</span></span> <span data-ttu-id="5c80c-300">ただし、常にグループ ノード レベルで税の計算式を設定することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-300">However, we recommend that you always configure tax calculation formulas at the group node level.</span></span> <span data-ttu-id="5c80c-301">税額の配分式は、グループ ノード レベル (行、税コンポーネントまたは税タイプ) または基準ノード レベルで構成できます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-301">Tax amount distribution formulas can be configured at either the group node level or the measure node level.</span></span>
    1. <span data-ttu-id="5c80c-302">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-302">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-303">**式**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-303">Click the **Formula** tab.</span></span>
    2. <span data-ttu-id="5c80c-304">**税式の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-304">Click **Add Tax formula**.</span></span>
    3. <span data-ttu-id="5c80c-305">**詳細**クイック タブで、カテゴリとして**計算**を選択し、式と条件を編集します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-305">On the **Details** FastTab, select **Calculation** as the category, and then edit the formula and condition.</span></span>
    4. <span data-ttu-id="5c80c-306">UTGST 税コンポーネントが SGST とすべて同じ式になるまで手順 2 ~ 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-306">Repeat steps 2 through 3 until the UTGST tax component has all the same formulas as SGST.</span></span>
    5. <span data-ttu-id="5c80c-307">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-307">Save the tax document.</span></span>

8. <span data-ttu-id="5c80c-308">転記プロファイルを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-308">Configure a posting profile.</span></span> <span data-ttu-id="5c80c-309">**税コンポーネント**タイプのノードのみ、転記プロファイルの定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-309">Only nodes of the **Tax Component** type support a posting profile definition.</span></span>
    1. <span data-ttu-id="5c80c-310">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-310">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-311">**転記**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-311">Click the **Postings** tab.</span></span>
    2. <span data-ttu-id="5c80c-312">**転記プロファイルの追加**をクリックして新しい転記プロファイルの定義を作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-312">Click **Add Posting Profile** to create a new posting profile definition.</span></span>
    3. <span data-ttu-id="5c80c-313">**詳細**クイック タブで、前のタスクで定義されている税基準の会計処理を入力し、借方と貸方の会計補助元帳の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-313">On the **Details** FastTab, enter the accounting treatment for the tax measures that you defined in the previous task, and provide the names of the debit and credit accounting subledgers.</span></span>
    4. <span data-ttu-id="5c80c-314">**編集**をクリックして、転記プロファイルの条件を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-314">Click **Edit** to enter a condition for the posting profile.</span></span>
    5. <span data-ttu-id="5c80c-315">必要に応じて、転記プロファイルの説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-315">Optional: Enter a description for the posting profile.</span></span>
    6. <span data-ttu-id="5c80c-316">UTGST 税コンポーネントが SGST とすべて同じ転記プロファイルとなるまで手順 2 ~ 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-316">Repeat steps 2 through 5 until the UTGST tax component has all the same posting profiles as SGST.</span></span>
    7. <span data-ttu-id="5c80c-317">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-317">Save the tax document.</span></span>

9. <span data-ttu-id="5c80c-318">会計のルックアップを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-318">Configure accounting lookups.</span></span> <span data-ttu-id="5c80c-319">**税タイプ**および**税コンポーネント**タイプのノードのみ会計ルックアップの定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-319">Only nodes of the **Tax Type** and **Tax Component** types support an accounting lookup definition.</span></span>
    1. <span data-ttu-id="5c80c-320">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-320">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-321">**会計**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-321">Click the **Accounting** tab.</span></span>
    2. <span data-ttu-id="5c80c-322">**列**をクリックして、税金の計算に使用される主勘定を決定するために使用できる属性の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-322">Click **Columns** to see a list of the attributes that can be used to determine the main accounts that will be used for accounting taxes.</span></span>
    3. <span data-ttu-id="5c80c-323">SGST が使用するのと同じ属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-323">Select the same attributes that SGST uses.</span></span>
        > [!NOTE]
        > <span data-ttu-id="5c80c-324">**追加**をクリックしないでください。</span><span class="sxs-lookup"><span data-stu-id="5c80c-324">Don’t click **Add**.</span></span> <span data-ttu-id="5c80c-325">ここで入力した値は、実際の税主勘定決定テーブルに影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="5c80c-325">Values that you enter have no effect on the actual tax main accounts decision table.</span></span> <span data-ttu-id="5c80c-326">そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定**で構成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-326">That table should be configured at **Tax** > **Tax configuration** > **Tax setup**.</span></span>

    4. <span data-ttu-id="5c80c-327">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-327">Save the tax document.</span></span>

10. <span data-ttu-id="5c80c-328">クレジット プールを構成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-328">Configure credit pools.</span></span> <span data-ttu-id="5c80c-329">**税コンポーネント**タイプのノードのみクレジット プールの定義をサポートします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-329">Only nodes of the **Tax Component** type support a credit pool definition.</span></span>
    1. <span data-ttu-id="5c80c-330">**Tax document** > **Header** > **Lines** > **GST** > **UTGST** と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-330">Go to **Tax document** > **Header** > **Lines** > **GST** > **UTGST**.</span></span> <span data-ttu-id="5c80c-331">**クレジット プール**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-331">Click the **Credit Pool** tab.</span></span>
    2. <span data-ttu-id="5c80c-332">**列**をクリックして、このコンポーネントの税決済に関連する属性の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-332">Click **Columns** to see a list of the attributes that are relevant to the tax settlement of this component.</span></span> <span data-ttu-id="5c80c-333">通常、選択された列は、**販売税登録番号**のように適切な税登録番号です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-333">Typically, the selected column is the appropriate tax registration number, like **GST Registration Number**.</span></span>
    3. <span data-ttu-id="5c80c-334">SGST が使用するのと同じ属性を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-334">Select the same attributes that SGST uses.</span></span>
        > [!NOTE]
        > <span data-ttu-id="5c80c-335">**追加**をクリックしないでください。</span><span class="sxs-lookup"><span data-stu-id="5c80c-335">Don’t click **Add**.</span></span> <span data-ttu-id="5c80c-336">ここで入力した値は、実際の単価表に影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="5c80c-336">Values that you enter here have no effect on the actual rate table.</span></span> <span data-ttu-id="5c80c-337">そのテーブルは、**税** > **税コンフィギュレーション** > **税の設定**で構成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-337">That table should be configured at **Tax** > **Tax configuration** > **Tax setup**.</span></span>

    4. <span data-ttu-id="5c80c-338">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-338">Save the tax document.</span></span>

### <a name="modify-the-formulas-of-lines-to-include-utgst"></a><span data-ttu-id="5c80c-339">UTGST を含めるために明細行の式を変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-339">Modify the formulas of lines to include UTGST</span></span>

1. <span data-ttu-id="5c80c-340">**税務書類** > **ヘッダー** > **明細行**と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-340">Go to **Tax document** > **Header** > **Lines**.</span></span> <span data-ttu-id="5c80c-341">**式**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-341">Click the **Formulas** tab.</span></span>
2. <span data-ttu-id="5c80c-342">**基準金額**、**明細行の税額**、および**価格に含まれる税額**基準を含むすべての数式を変更し、数式が UTGST を反映するようにします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-342">Change any formulas that contain the **Base Amount**, **Line tax amount**, and **Tax amount included in price** measures, so that the formulas reflect UTGST.</span></span> <span data-ttu-id="5c80c-343">たとえば、**内税額**式を次のように変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-343">For example, change the **Tax amount inclusive** formula as shown here.</span></span>

   ![内税の式](media/gte-tax-amount-inclusive.png)
    
3. <span data-ttu-id="5c80c-345">税務書類を保存します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-345">Save the tax document.</span></span>
4. <span data-ttu-id="5c80c-346">デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-346">Close the designer.</span></span>

### <a name="complete-the-tax-document-configuration"></a><span data-ttu-id="5c80c-347">税務書類のコンフィギュレーションを完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-347">Complete the tax document configuration</span></span>
1. <span data-ttu-id="5c80c-348">**ローカライズ コンフィギュレーション**ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして**税のコンフィギュレーション**。</span><span class="sxs-lookup"><span data-stu-id="5c80c-348">In the **Localization configurations** workspace (**Organization administration** > **Workspaces** > **Electronic reporting**), click **Tax configurations**.</span></span>
2. <span data-ttu-id="5c80c-349">**コンフィギュレーション** ワークスペースで、**状態の変更**をクリックし、**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-349">In the **Configurations** workspace, click **Change status**, and then select **Complete**.</span></span>
3. <span data-ttu-id="5c80c-350">**UTGST** のように説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-350">Enter a description such as **UTGST**, and then click **OK**.</span></span>
4. <span data-ttu-id="5c80c-351">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-351">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>
5. <span data-ttu-id="5c80c-352">ステータスが**完了**に更新されると、コンフィギュレーションを配置できる状態です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-352">After the status is updated to **Complete**, the configuration is ready for deployment.</span></span>

### <a name="import-the-configuration-and-deploy-it-to-a-specific-company"></a><span data-ttu-id="5c80c-353">コンフィギュレーションをインポートし、特定の会社に配置します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-353">Import the configuration and deploy it to a specific company</span></span>
1. <span data-ttu-id="5c80c-354">**税** > **設定** > **税コンフィギュレーション** > **税の設定**と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-354">Go to **Tax** > **Setup** > **Tax configuration** > **Tax setup**.</span></span>
2. <span data-ttu-id="5c80c-355">新しいレコードを作成し、税の設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-355">Create a new record and define tax setup.</span></span>

    ![新しい税の設定](media/gte-extension-new-tax-setup.png)

3. <span data-ttu-id="5c80c-357">**コンフィギュレーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-357">Click **Configurations**.</span></span>

4. <span data-ttu-id="5c80c-358">**税コンフィギュレーション**タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-358">Click the **Tax configuration** tab.</span></span>
5. <span data-ttu-id="5c80c-359">**利用可能な構成**セクションで、**新規**をクリックして税コンフィギュレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-359">In the **Available configurations** section, click **New** to create a tax configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5c80c-360">税に追加されるコンフィギュレーションは、**使用可能なコンフィギュレーション**タブに一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-360">The configuration that is added to tax gets listed on the **Available configuration** tab</span></span>
    
    ![新しいコンフィギュレーション](media/gte-extension-new-configuration2.png)

6. <span data-ttu-id="5c80c-362">**税 (インド販売税)** のように、必要なコンフィギュレーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-362">Select the required configuration, such as **Tax (India GST)**.</span></span> <span data-ttu-id="5c80c-363">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-363">Click **Save**.</span></span>
7. <span data-ttu-id="5c80c-364">**同期化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-364">Click **Synchronize**.</span></span>

    ![コンフィギュレーションの同期](media/gte-extension-synchronize-configuration.png)

8. <span data-ttu-id="5c80c-366">**有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-366">Click **Activate**.</span></span>

    ![コンフィギュレーションをアクティブにします。](media/gte-extension-activate-configuration.png)

    ![コンフィギュレーションをアクティブにします。](media/gte-extension-active-configuration.png)

9. <span data-ttu-id="5c80c-369">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-369">Click **Close**.</span></span>
10. <span data-ttu-id="5c80c-370">**会社**クイック タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-370">Click the **Companies** FastTab.</span></span>
11. <span data-ttu-id="5c80c-371">**新規**をクリックし、**会社**フィールドで、**INMF** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-371">Click **New** and then select **INMF** in the **Companies** field.</span></span>
12. <span data-ttu-id="5c80c-372">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-372">Click **Save**.</span></span>
13. <span data-ttu-id="5c80c-373">**有効化**をクリックして、会社のコンフィギュレーションを有効にします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-373">Click **Activate** to activate the configuration for the company.</span></span>

    ![会社のコンフィギュレーションの有効化します。](media/gte-extension-activate-configuration-to-company.png)

14. <span data-ttu-id="5c80c-375">**設定**をクリックして、新しいバージョンのデータを設定します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-375">Click **Setup** to set up data for the new version.</span></span>

## <a name="scenario-2-using-a-reference-model"></a><span data-ttu-id="5c80c-376">シナリオ 2 : 参照モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-376">Scenario 2: Using a reference model</span></span>

<span data-ttu-id="5c80c-377">Microsoft 製のコンフィギュレーションごとに、BCD の税率は、優先的関係者/インポート オーダー/カスタム輸入税率コード/エクスポート オーダー/エクスポート カスタム輸出税率コードによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-377">Per the Microsoft-provided configuration, the tax rate for the BCD is determined by Preferential Party/Import Order/Import Custom Tariff Code/Export Order/Export Custom Tariff Code.</span></span> <span data-ttu-id="5c80c-378">このシナリオを使って、さまざまな国/地域からの商品のインポート オーダーに BCD の異なる税率を適用することをサポートするために参照モデルを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-378">We will use this scenario to explain how to use a reference model to support applying a different tax rate for the BCD on the import order of goods from different countries/regions.</span></span>

<span data-ttu-id="5c80c-379">このシナリオでは、次の作業を完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="5c80c-379">To support this scenario, you must complete the following tasks:</span></span>
1. [<span data-ttu-id="5c80c-380">拡張コンフィギュレーションの作成</span><span class="sxs-lookup"><span data-stu-id="5c80c-380">Create extension configurations</span></span>](#create-extension-configurations)
2. [<span data-ttu-id="5c80c-381">原産国/地域の参照モデルを追加します</span><span class="sxs-lookup"><span data-stu-id="5c80c-381">Add a reference model for country/region of origin</span></span>](#add-a-reference-model-for-countryregion-of-origin)
3. [<span data-ttu-id="5c80c-382">参照モデルのデータ マッピングを完了します</span><span class="sxs-lookup"><span data-stu-id="5c80c-382">Complete data mapping for the reference model</span></span>](#complete-data-mapping-for-the-reference-model)
4. [<span data-ttu-id="5c80c-383">課税対象ドキュメントのフィールドに参照モデルをリンクします</span><span class="sxs-lookup"><span data-stu-id="5c80c-383">Link the reference model to field in taxable document</span></span>](#link-the-reference-model-to-a-field-in-the-taxable-document)
5. [<span data-ttu-id="5c80c-384">BCD税率のルックアップを変更します</span><span class="sxs-lookup"><span data-stu-id="5c80c-384">Change the lookup of the BCD tax rate</span></span>](#change-the-lookup-of-the-bcd-tax-rate)
6. [<span data-ttu-id="5c80c-385">税に関する文書のコンフィギュレーションを完了します</span><span class="sxs-lookup"><span data-stu-id="5c80c-385">Complete the tax document configuration</span></span>](#complete-the-tax-document-configuration)
7. [<span data-ttu-id="5c80c-386">コンフィギュレーションをインポートし、特定の会社に配置します</span><span class="sxs-lookup"><span data-stu-id="5c80c-386">Import the configuration and deploy it to a specific company</span></span>](#import-the-configuration-and-deploy-it-to-a-specific-company)

### <a name="add-a-reference-model-for-countryregion-of-origin"></a><span data-ttu-id="5c80c-387">原産国/地域の参照モデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-387">Add a reference model for country/region of origin</span></span>

1. <span data-ttu-id="5c80c-388">**ローカライズ コンフィギュレーション**ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして**税のコンフィギュレーション**。</span><span class="sxs-lookup"><span data-stu-id="5c80c-388">In the **Localization configurations** workspace (**Organization administration** > **Workspaces** > **Electronic reporting**), click **Tax configurations**.</span></span>
2. <span data-ttu-id="5c80c-389">**課税対象ドキュメント (インド Contoso)** コンフィギュレーションを検索、選択し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-389">Find and select the **Taxable Document (India Contoso)** configuration, and then click **Designer**.</span></span>
3. <span data-ttu-id="5c80c-390">**...** > **参照モデル**をクリックして、すべての使用可能な参照モデルを表示できるように、ビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-390">Click **...** > **Reference model** to change the view so that you can view all the available reference models.</span></span>
4. <span data-ttu-id="5c80c-391">**新規**をクリックして、新しい参照モデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-391">Click **New** to add a new reference model.</span></span>
    -   <span data-ttu-id="5c80c-392">**名前** - 原産国</span><span class="sxs-lookup"><span data-stu-id="5c80c-392">**Name** - Country of origin</span></span>
    -   <span data-ttu-id="5c80c-393">**ノード タイプ**- モデル ルート</span><span class="sxs-lookup"><span data-stu-id="5c80c-393">**Node type** - Model root</span></span>
5. <span data-ttu-id="5c80c-394">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-394">Click **Add**.</span></span>
6. <span data-ttu-id="5c80c-395">**原産国**を強調表示して、**新規**をクリックし、新しい参照モデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-395">Highlight **Country of Origin**, click **New** to add new reference model.</span></span>
    -   <span data-ttu-id="5c80c-396">**名前** - 原産国</span><span class="sxs-lookup"><span data-stu-id="5c80c-396">**Name** - Countries of origin</span></span>
    -   <span data-ttu-id="5c80c-397">**ノード タイプ** - 有効な子ノード</span><span class="sxs-lookup"><span data-stu-id="5c80c-397">**Node type** - Child of an active node</span></span>
    -   <span data-ttu-id="5c80c-398">**品目タイプ** - レコードの一覧</span><span class="sxs-lookup"><span data-stu-id="5c80c-398">**Item type** - Record list</span></span>
7. <span data-ttu-id="5c80c-399">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-399">Click **Add**.</span></span>
8. <span data-ttu-id="5c80c-400">**原産国**を強調表示して、**新規**をクリックし、新しい参照モデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-400">Highlight **Countries of Origin**, click **New** to add new reference model.</span></span>
    -   <span data-ttu-id="5c80c-401">**名前** - 原産国</span><span class="sxs-lookup"><span data-stu-id="5c80c-401">**Name** - Country of origin</span></span>
    -   <span data-ttu-id="5c80c-402">**ノード タイプ** - 有効な子ノード</span><span class="sxs-lookup"><span data-stu-id="5c80c-402">**Node type** - Child of an active node</span></span>
    -   <span data-ttu-id="5c80c-403">**品目タイプ**文字列</span><span class="sxs-lookup"><span data-stu-id="5c80c-403">**Item type** - String</span></span>
9. <span data-ttu-id="5c80c-404">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-404">Click **Add**.</span></span>
10. <span data-ttu-id="5c80c-405">**原産国**を強調表示して、**ナチュラル キー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-405">Highlight **Country of Origin**, click **Natural key**.</span></span>
11. <span data-ttu-id="5c80c-406">**原産国\\原産国\\原産国**を、**ナチュラル キー**として選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-406">Select **Country of Origin\\Countries of Origin\\Country of Origin** as the **Natural key**.</span></span>
12. <span data-ttu-id="5c80c-407">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-407">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>

<span data-ttu-id="5c80c-408">状態を**完了**に更新すると、コンフィギュレーションを配置できる状態になります。</span><span class="sxs-lookup"><span data-stu-id="5c80c-408">After you update the status to be **Complete**, the configuration is ready for deployment.</span></span>

### <a name="complete-data-mapping-for-the-reference-model"></a><span data-ttu-id="5c80c-409">参照モデルのデータ マッピングを完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-409">Complete data mapping for the reference model</span></span>
1. <span data-ttu-id="5c80c-410">**ローカライズ コンフィギュレーション**ワークスペース (**組織管理** > **ワークスペース** > **電子申告**)、をクリックして**税のコンフィギュレーション**。</span><span class="sxs-lookup"><span data-stu-id="5c80c-410">In the **Localization configurations** workspace (**Organization administration** > **Workspaces** > **Electronic reporting**), click **Tax configurations**.</span></span>
2. <span data-ttu-id="5c80c-411">**課税対象ドキュメント (インド Contoso)** コンフィギュレーションを検索、選択し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-411">Find and select the **Taxable Document (India Contoso)** configuration, and then click **Designer**.</span></span>
3. <span data-ttu-id="5c80c-412">**モデルからデータ ソースへのマップ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-412">Click **Map model to datasource**.</span></span>
4. <span data-ttu-id="5c80c-413">**原産国** を選択し、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-413">Select **Country of Origin** and then click **Add**.</span></span>
5. <span data-ttu-id="5c80c-414">一覧で**原産国**を選択して、**デザイナー**をクリックし、モデル マッピングのデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-414">With **Country of Origin** selected in the list, click **Designer** to open the designer of the model mapping.</span></span>
6. <span data-ttu-id="5c80c-415">ルートとして **LogisticsAddressCountryRegion** テーブル レコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-415">Add table records **LogisticsAddressCountryRegion** as a root.</span></span>
    1. <span data-ttu-id="5c80c-416">**データ ソース タイプ**で、**テーブル レコード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-416">Select **Table records** in the **Data source type** tree.</span></span>
    2. <span data-ttu-id="5c80c-417">**ルートの追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-417">Click **Add root**.</span></span>
    3. <span data-ttu-id="5c80c-418">**名前**フィールドに、**LogisticsAddressCountryRegion** という名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-418">Enter the name **LogisticsAddressCountryRegion** in the **Name** field.</span></span>
    4. <span data-ttu-id="5c80c-419">テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-419">Select a table.</span></span>
    5. <span data-ttu-id="5c80c-420">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-420">Click **OK**.</span></span>
    
    ![テーブル レコードの追加](media/gte-extension-add-table-records.png)

7. <span data-ttu-id="5c80c-422">テーブルをバインドします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-422">Bind the table.</span></span>

    1. <span data-ttu-id="5c80c-423">**データ ソース**ツリーで、手順 5 で作成した **LogisticsAddressCountryRegion** テーブル レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-423">In the **Data sources** tree, select the **LogisticsAddressCountryRegion** table record that you created in step 5.</span></span>
    2. <span data-ttu-id="5c80c-424">**日付モデル**ツリーで、**原産国: レコードの一覧**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-424">In the **Date model** tree, select **Countries of Origin: Record list**.</span></span>
    3. <span data-ttu-id="5c80c-425">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-425">Click **Bind**.</span></span>
    
    ![テーブルのバインド](media/gte-extension-bind-table.png)

8. <span data-ttu-id="5c80c-427">フィールドをバインドします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-427">Bind the field.</span></span>

    1. <span data-ttu-id="5c80c-428">**データ ソース**ツリーで、**国/地域 (CountryRegionID): 文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-428">In the **Data sources** tree, select **Country/region(CountryRegionID): String**.</span></span>
    2. <span data-ttu-id="5c80c-429">**データ モデル**ツリーで、**原産国: 文字列**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-429">In the **Date model** tree, select **Country of Origin: String**.</span></span>
    3. <span data-ttu-id="5c80c-430">**バインド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-430">Click **Bind**.</span></span>

    ![フィールドのバインド](media/gte-extension-bind-field.png)

9. <span data-ttu-id="5c80c-432">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-432">Click **Save**.</span></span>

### <a name="link-the-reference-model-to-a-field-in-the-taxable-document"></a><span data-ttu-id="5c80c-433">課税対象ドキュメントで、参照モデルをフィールドにリンクします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-433">Link the reference model to a field in the taxable document</span></span>

1. <span data-ttu-id="5c80c-434">**...** > **課税対象ドキュメント**をクリックし、**課税対象ドキュメント**に対するビューを変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-434">Click **...** > **Taxable document** to change the view to **Taxable document**.</span></span>
2. <span data-ttu-id="5c80c-435">**課税対象ドキュメント** > **ヘッダー** > **明細行** > **販売税** > **原産国/地域**と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-435">Navigate to **Taxable document** > **Header** > **Lines** > **GST** > **Country/Region of Origin**.</span></span>
3. <span data-ttu-id="5c80c-436">**ノード** クイック タブで、**参照モデルを選択**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-436">On the **Node** FastTab, click **Select reference model**.</span></span> 
4. <span data-ttu-id="5c80c-437">参照モデルに**原産国**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-437">Choose **Country of Origin** for the reference model.</span></span>
5. <span data-ttu-id="5c80c-438">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-438">Click **OK**.</span></span>
6. <span data-ttu-id="5c80c-439">コンフィギュレーションを保存し、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5c80c-439">Save the configuration and close the designer.</span></span>
7. <span data-ttu-id="5c80c-440">**コンフィギュレーション** ワークスペースで、**状態の変更**をクリックし、**完了**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-440">In the **Configurations** workspace, click **Change status**, and then select **Complete**.</span></span>
8. <span data-ttu-id="5c80c-441">**原産国の参照モデルの追加**のように説明を入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-441">Enter a description such as **Add reference model for Country of Origin**, and then click **OK**.</span></span>
9. <span data-ttu-id="5c80c-442">エラーがある場合は、デザイナーを開き、**検証**をクリックし、エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-442">If there are any errors, open the designer, click **Validate**, and fix the errors.</span></span>

<span data-ttu-id="5c80c-443">ステータスが**完了**に更新されると、コンフィギュレーションを配置できる状態です。</span><span class="sxs-lookup"><span data-stu-id="5c80c-443">After the status is updated to **Complete**, the configuration is ready for deployment.</span></span>

### <a name="change-the-lookup-of-the-bcd-tax-rate"></a><span data-ttu-id="5c80c-444">BCD 税率のルックアップを変更します</span><span class="sxs-lookup"><span data-stu-id="5c80c-444">Change the lookup of the BCD tax rate</span></span>

1.  <span data-ttu-id="5c80c-445">**税 (インド販売税 Contoso)** コンフィギュレーションに移動し、**デザイナー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-445">Go to the **Tax (India GST Contoso)** configuration, and then click **Designer**.</span></span>
2.  <span data-ttu-id="5c80c-446">**税 (インド販売税 Contoso)** のデータ モデルを、拡張された課税対象ドキュメントの更新されたバージョンに変更します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-446">Change the data model of **Tax (India GST Contoso)** to the updated version of the extended taxable document.</span></span> <span data-ttu-id="5c80c-447">これを行うには、[シナリオ 1、タスク 3 : 拡張された課税対象ドキュメントのデータ マッピングを完了](#complete-data-mapping-for-the-extended-taxable-document) にある手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-447">To do this, complete the steps in [Scenario 1, Task 3: Complete data mapping for the extended taxable document](#complete-data-mapping-for-the-extended-taxable-document).</span></span>
3.  <span data-ttu-id="5c80c-448">**税務書類** > **ヘッダー** > **明細行** > **カスタム関税** > **BCD** > **レート**と移動します。</span><span class="sxs-lookup"><span data-stu-id="5c80c-448">Go to **Tax document** > **Header** > **Lines** > **Custom Duty** > **BCD** > **Rate**.</span></span> <span data-ttu-id="5c80c-449">**ルックアップ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-449">Click the **Lookup** tab.</span></span>
4.  <span data-ttu-id="5c80c-450">**列**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-450">Click **Columns**.</span></span>
5.  <span data-ttu-id="5c80c-451">ルックアップ列として**原産国/地域**を選択し、右矢印ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-451">Select **Country/Region of Origin** as the lookup column, and then click the right arrow button.</span></span>
6.  <span data-ttu-id="5c80c-452">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5c80c-452">Click **Save**.</span></span>

