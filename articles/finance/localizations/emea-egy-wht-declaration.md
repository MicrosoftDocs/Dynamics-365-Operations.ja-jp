---
title: エジプトの源泉徴収税申告
description: このトピックでは、エジプトの源泉徴収税申告を構成および生成する方法について説明します。
author: sndray
manager: AnnBe
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: cec903c56439957bcafb77c3da774a903d4433a1
ms.sourcegitcommit: a3052f76ad71894dbef66566c07c6e2c31505870
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/10/2021
ms.locfileid: "5574336"
---
#  <a name="withholding-tax-declaration-for-egypt-eg-00005"></a><span data-ttu-id="fd5ab-103">エジプトの源泉徴収税申告 (EG-00005)</span><span class="sxs-lookup"><span data-stu-id="fd5ab-103">Withholding tax declaration for Egypt (EG-00005)</span></span>

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

## <a name="overview"></a><span data-ttu-id="fd5ab-104">概要</span><span class="sxs-lookup"><span data-stu-id="fd5ab-104">Overview</span></span>
<span data-ttu-id="fd5ab-105">このトピックでは、源泉徴収税申告と、エジプトの法人向けの源泉徴収税申告フォーム 41 と 11 の設定および生成する方法について説明します</span><span class="sxs-lookup"><span data-stu-id="fd5ab-105">This topic explains how to set up and generate the withholding tax declaration and the withholding tax declaration forms 41 and 11 for legal entities in Egypt</span></span> 

<span data-ttu-id="fd5ab-106">すべてのエジプトの法人は、ローカルの仕入先およびサービス プロバイダーから保持されるすべての税金を集計するフォーム 41 を準備する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-106">All Egyptian entities must prepare the form  41 which summarizes all taxes that are retained from local suppliers and service providers.</span></span> <span data-ttu-id="fd5ab-107">フォーム 41 に加えて、フォーム 11 を使用して外国のプロバイダーから課税されるすべての留保の詳細を生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-107">In addition to form 41, form 11 must be generated to detail all of the retained taxed from foreign providers.</span></span> 

<span data-ttu-id="fd5ab-108">Dynamics 365 Finance の **源泉徴収税申告** レポートには、次のレポートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-108">The **Withholding tax declaration** report in Dynamics 365 Finance includes the following reports:</span></span>

- <span data-ttu-id="fd5ab-109">申告 フォーム ナンバー。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-109">Declaration form No.</span></span> <span data-ttu-id="fd5ab-110">41</span><span class="sxs-lookup"><span data-stu-id="fd5ab-110">41</span></span>
- <span data-ttu-id="fd5ab-111">申告 フォーム ナンバー。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-111">Declaration form No.</span></span> <span data-ttu-id="fd5ab-112">11</span><span class="sxs-lookup"><span data-stu-id="fd5ab-112">11</span></span>
    
    
## <a name="prerequisites"></a><span data-ttu-id="fd5ab-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="fd5ab-113">Prerequisites</span></span>
<span data-ttu-id="fd5ab-114">法人の基本住所がエジプトである必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-114">The primary address of the legal entity must be in Egypt.</span></span>
<span data-ttu-id="fd5ab-115">**機能の管理** ワークスペースで、次の機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-115">In the **Feature management** workspace, the following feature must be enabled:</span></span>

   - <span data-ttu-id="fd5ab-116">**グローバル源泉徴収税**</span><span class="sxs-lookup"><span data-stu-id="fd5ab-116">**Global withholding tax**</span></span>

<span data-ttu-id="fd5ab-117">この機能を有効にする方法についての詳細は、[機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-117">For more information about how to enable features, see [Feature management overview.](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)</span></span>

1. <span data-ttu-id="fd5ab-118">**税** > **設定** > **パラメーター** > **総勘定元帳パラメーター** に移動し、**源泉徴収税** タブで、**グローバル源泉徴収税を有効にする** を **はい** にします。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-118">Go to **Tax** > **Setup** > **Parameters** > **General ledger parameters**, and on the **Withholding tax** tab, set **Enable global withholding tax** to **Yes**.</span></span>
2. <span data-ttu-id="fd5ab-119">**電子申告** ワークスペースで、リポジトリから次の電子申告形式をインポートします。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-119">In the **Electronic reporting** workspace, import the following Electronic reporting formats from the repository:</span></span>

    - <span data-ttu-id="fd5ab-120">WHT 申告 Excel (EG)</span><span class="sxs-lookup"><span data-stu-id="fd5ab-120">WHT Declaration Excel (EG)</span></span>

    > [!NOTE]
    > <span data-ttu-id="fd5ab-121">上記の形式は **税申告モデル** に基づいており、**税申告モデル マッピング** を使用します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-121">The format above is based on the **Tax declaration model** and uses the **Tax declaration model mapping**.</span></span> <span data-ttu-id="fd5ab-122">この追加の構成が自動的にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-122">This additional configuration is automatically imported.</span></span>

<span data-ttu-id="fd5ab-123">電子申告構成をインポートする方法の詳細については、[Lifecycle Services から電子申告構成をダウンロードする](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-123">For more information about how to import Electronic reporting configurations, see [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

## <a name="download-electronic-reporting-configurations"></a><span data-ttu-id="fd5ab-124">電子申告構成のダウンロード</span><span class="sxs-lookup"><span data-stu-id="fd5ab-124">Download Electronic reporting configurations</span></span>

<span data-ttu-id="fd5ab-125">エジプトの WHT 申告フォームの実装は、電子申告 (ER) の構成に基づいています。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-125">The implementation of the WHT declaration forms for Egypt is based on Electronic reporting (ER) configurations.</span></span> <span data-ttu-id="fd5ab-126">構成可能なレポートの機能および概念に関する詳細については、[電子申告](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照にしてください。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-126">For more information about the capabilities and concepts of configurable reporting, see [Electronic reporting](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).</span></span>

<span data-ttu-id="fd5ab-127">生産およびユーザー受け入れテスト (UAT) 環境については、[Lifecycle Services から電子申告構成をダウンロードする](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md) のトピックにある手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-127">For production and user acceptance testing (UAT) environments, follow the instructions in the topic, [Download Electronic reporting configurations from Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="fd5ab-128">エジプト法人の源泉徴収申告を生成するには、次の構成をアップロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-128">To generate the Withholding declarations in an Egyptian legal entity, you need to upload the following configurations:</span></span>

- <span data-ttu-id="fd5ab-129">税申告モデル.バージョン.82.xml またはそれ以降のバージョン</span><span class="sxs-lookup"><span data-stu-id="fd5ab-129">Tax declaration model.version.82.xml or later version</span></span>
- <span data-ttu-id="fd5ab-130">税申告モデル マッピング.バージョン.82.133.xml またはそれ以降のバージョン</span><span class="sxs-lookup"><span data-stu-id="fd5ab-130">Tax declaration model mapping.version.82.133.xml or a later version</span></span>
- <span data-ttu-id="fd5ab-131">WHT 申告 Excel (EG).バージョン.82.21 またはそれ以降のバージョン</span><span class="sxs-lookup"><span data-stu-id="fd5ab-131">WHT Declaration Excel (EG).version.82.21  or a later version</span></span>

<span data-ttu-id="fd5ab-132">Lifecycle Services (LCS) またはグローバル リポジトリから電子申告構成のダウンロードを完了した後、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-132">After you finish downloading the ER configurations from Lifecycle Services (LCS) or the global repository, complete the following steps.</span></span>

1. <span data-ttu-id="fd5ab-133">**電子申告** ワークスペースに移動し、**レポート構成** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-133">Go to the **Electronic reporting** workspace and select the **Reporting configurations** tile.</span></span>
1. <span data-ttu-id="fd5ab-134">アクション ウィンドウの **構成** ページで、**交換 > XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-134">On the **Configurations** page, on the Action Pane, select **Exchange > Load from XML file**.</span></span>
1. <span data-ttu-id="fd5ab-135">前の箇条書きに表示された順序ですべてのファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-135">Upload all the files in the order in which they are listed in the previous bullets.</span></span> <span data-ttu-id="fd5ab-136">すべての構成をアップロードした後、構成ツリーが Finance に存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-136">After all of the configurations are uploaded, the configuration tree should be present in Finance.</span></span>

## <a name="set-up-application-specific-parameters"></a><span data-ttu-id="fd5ab-137">申請固有のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="fd5ab-137">Set up application-specific parameters</span></span>

<span data-ttu-id="fd5ab-138">申請固有のパラメーター オプションを使用すると、ユーザーは **源泉徴収税品目グループ** の構成またはルックアップの定義で設定された他の基準に応じて、生成されるレポートの各行で税トランザクションが分類および計算される方法を設定できます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-138">The application-specific parameters option lets users establish the criteria of how the tax transactions will be classified and calculated in each line of a generated report depending on the configuration of **withholding tax item group** or other criteria established in the definition of lookup.</span></span>

<span data-ttu-id="fd5ab-139">源泉徴収申告フォーム 41 には、**割引コードタイプ** と呼ばれる税務当局分類に従って分類する必要がある源泉徴収税トランザクションがある特定の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-139">Withholding declaration form 41 includes a specific column where the withholding tax transaction must be classified in accordance with the tax authority classification named **Discount code type**.</span></span> <span data-ttu-id="fd5ab-140">これらの新しい分類をトランザクションの転記時に新しいエントリ データとして含める代わりに、エジプトの源泉徴収レポートの要件を満たすため、**構成** > **アプリケーション固有のパラメーターの設定** > **設定** で紹介された異なるルックアップに基づいて分類が決定されます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-140">Instead of including these new classifications as new entry data when the transactions are posted, the classifications will be determined based on the different lookups introduced in **Configurations** > **Set up application-specific parameters** > **Setup** to meet the requirements of withholding reports for Egypt.</span></span> 

<span data-ttu-id="fd5ab-141">次の構成を使用して、源泉徴収申告フォーム 41 レポートでトランザクションを分類します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-141">The following configuration is used to classify the transactions in the Withholding declaration form 41 report:</span></span>

- <span data-ttu-id="fd5ab-142">**DiscountTaxTypeLookup**-> 列 ナンバー 18</span><span class="sxs-lookup"><span data-stu-id="fd5ab-142">**DiscountTaxTypeLookup**-> Column No 18</span></span> 

<span data-ttu-id="fd5ab-143">WHT 申告および関連する帳簿レポートの生成に使用される異なるルックアップを設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-143">Complete the following steps to set up the different lookups used to generate the WHT declaration and related books reports.</span></span> 

1. <span data-ttu-id="fd5ab-144">**電子申告** ワークスペースで、**構成** > **設定** を選択して、WHT 申告レポートでトランザクションを分類する方法を識別するルールを設定します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-144">In the **Electronic reporting** workspace, select **Configurations** > **Setup** to set up the rules to identify how transactions are classified in the WHT declaration report.</span></span> 
2. <span data-ttu-id="fd5ab-145">現在のバージョンを選択し、**ルックアップ** クイック タブでルックアップ名を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-145">Select the current version, and on the **Lookups** FastTab, select the lookup name.</span></span> <span data-ttu-id="fd5ab-146">たとえば、**DiscountTaxTypeLookup** です。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-146">For example, **DiscountTaxTypeLookup**.</span></span> <span data-ttu-id="fd5ab-147">このルックアップは、税務当局にとって必要な割引タイプのリストを識別します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-147">This lookup identifies the list of discount types required by the tax authority.</span></span>
3. <span data-ttu-id="fd5ab-148">**条件** クイック タブで、**追加** を選択し、**ルックアップの結果** の列の新しい行で **列 18** の分類を表す関連する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-148">On the **Conditions** FastTab, select **Add** and in the new line in the **Lookup result** column, select the related line that represents the classification in the **Column 18**.</span></span>
4. <span data-ttu-id="fd5ab-149">**源泉徴収税品目グループ** の列で、分類の識別に使用する関連するコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-149">In the **Withholding tax item group** column, select the related code that's used to identify the classification.</span></span> <span data-ttu-id="fd5ab-150">たとえば、**許可された割引** です。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-150">For example, **Allowed discount**.</span></span>  
5. <span data-ttu-id="fd5ab-151">使用可能なすべてのルックアップで手順 3 および 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-151">Repeat steps 3 and 4 for all available lookups.</span></span>
6. <span data-ttu-id="fd5ab-152">再び **追加** を選択して、最後のレコード行を含め、**ルックアップの結果** の列で **適用できません** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-152">Select **Add** again to include the final record line, and in the **Lookup result** column, select **Not applicable**.</span></span> 
7. <span data-ttu-id="fd5ab-153">残りの列で、**空白でない** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-153">In the remaining columns, select **Not blank**.</span></span> 

> [!NOTE]

## <a name="set-up-general-ledger-parameters"></a><span data-ttu-id="fd5ab-154">総勘定元帳パラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="fd5ab-154">Set up General ledger parameters</span></span>

<span data-ttu-id="fd5ab-155">Microsoft Excel で WHT 申告フォーム レポートを生成するには、**総勘定元帳パラメーター** ページで電子申告形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-155">To generate the WHT declaration form reports in Microsoft Excel, define an ER format on the **General ledger parameters** page.</span></span>

1. <span data-ttu-id="fd5ab-156">**税** > **設定** > **総勘定元帳パラメーター** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-156">Go to **Tax** > **Setup** > **General ledger parameters**.</span></span>
2. <span data-ttu-id="fd5ab-157">**源泉徴収税** タブの **WHT 申告フォーマット マッピング** フィールドで、**WHT 申告 Excel (EG)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-157">On the **Withholding tax** tab, in the **WHT declaration format mapping** field, select **WHT Declaration Excel (EG)**.</span></span> <span data-ttu-id="fd5ab-158">フィールドを空白のままにすると、標準消費税レポートが SSRS 形式で生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-158">If you leave the field blank, the standard sales tax report will be generated in SSRS format.</span></span>


![申告 フォーム](media/egypt-wht-declaration-setup1.png)

## <a name="generate-the-withholding-declaration-forms"></a><span data-ttu-id="fd5ab-160">源泉徴収申告フォームの生成</span><span class="sxs-lookup"><span data-stu-id="fd5ab-160">Generate the Withholding declaration forms</span></span>
<span data-ttu-id="fd5ab-161">特定の期間の源泉徴収申告フォームを準備および送信するプロセスは、支払税の決済および転記ジョブ中に転記された源泉徴収税トランザクションに基づいています。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-161">The process of preparing and submitting a Withholding declaration form for a specific period is based on the withholding tax transactions posted during the settle and post payment tax job.</span></span> <span data-ttu-id="fd5ab-162">グローバル源泉徴収税の詳細については、[グローバル源泉徴収税](../general-ledger/global-withholding-tax-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-162">For more information about global withholding tax, see [Global withholding tax](../general-ledger/global-withholding-tax-overview.md).</span></span>

<span data-ttu-id="fd5ab-163">次の手順を実行して、税申告レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-163">Complete the following steps to generate the tax declaration report.</span></span>

1. <span data-ttu-id="fd5ab-164">**税** > **申告** > **源泉徴収税** > \**源泉徴収税の支払* に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-164">Go to **Tax** > **Declarations** > **Withholding tax** > \**Withholding tax payment*.</span></span>
2. <span data-ttu-id="fd5ab-165">決済期間を選択し、レポートの開始日を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-165">Select the settlement period and then select the from date for the report.</span></span> 
3. <span data-ttu-id="fd5ab-166">トランザクションの日付を入力して **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-166">Enter the transaction date and then select **OK**.</span></span>
4. <span data-ttu-id="fd5ab-167">開かれているダイアログ ボックスで、1 つ以上のフォーム タイプ **フォーム ナンバー 41**、**フォーム ナンバー 11** または **なし** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-167">In the dialog box that opens, select one or more of the form types \*\*Form No 41 \*\*, **Form No 11**, or **None**.</span></span> <span data-ttu-id="fd5ab-168">**なし** を選択すると、標準レポートが生成されます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-168">If you select **None**, the standard report is generated.</span></span> 
5. <span data-ttu-id="fd5ab-169">言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-169">Select the language.</span></span> <span data-ttu-id="fd5ab-170">すべてのレポートは、**en-us** および **ar-eg** に移動されます。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-170">All reports are translated in **en-us** and **ar-eg**.</span></span>
6. <span data-ttu-id="fd5ab-171">税支払が行われる銀行の支店と名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-171">Enter the branch and name of the bank where the tax payment will be paid.</span></span>
7. <span data-ttu-id="fd5ab-172">ビジネス タイプを選択し、チェック番号および文書番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-172">Select the business type and then enter the check and document numbers.</span></span> 
8. <span data-ttu-id="fd5ab-173">エンティティ タイプを入力します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-173">Enter the entity type.</span></span> 
9. <span data-ttu-id="fd5ab-174">フォームを割り当てる登録者の名前を入力し、**OK** を選択してレポートの生成を確認します。</span><span class="sxs-lookup"><span data-stu-id="fd5ab-174">Enter the name of person registered to assign the form and select **OK** to confirm the report generation.</span></span> 

 
[!INCLUDE[footer-include](../../includes/footer-banner.md)]
