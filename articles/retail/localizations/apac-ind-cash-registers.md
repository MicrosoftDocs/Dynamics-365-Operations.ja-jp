---
title: インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合
description: このトピックでは、インドで使用可能なキャッシュ レジスター機能の概要を示します。 また、機能を設定するためのガイドラインを示します。
author: EvgenyPopovMBS
manager: annbe
ms.date: 01/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Retail, Operations
ms.search.region: India
ms.search.industry: Retail
ms.author: v-pakris
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: 46e9045867265dbe1cd051ffba79d1a31abdd76c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537610"
---
# <a name="goods-and-services-tax-gst-integration-for-cash-registers-for-india"></a><span data-ttu-id="d0de3-104">インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合</span><span class="sxs-lookup"><span data-stu-id="d0de3-104">Goods and Services Tax (GST) integration for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0de3-105">このトピックでは、Microsoft Dynamics 365 for Retail に関連するフィーチャのチュートリアルを提供します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-105">This topic provides a walkthrough of the features that are related to Goods and Services Tax (GST) in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d0de3-106">また、さまざまな種類の小売業務取引に対する GST の影響をハイライトして、レシートが販売時点管理 (POS) で印刷される小売り取引の会計および転記を示します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-106">It also highlights the effect of GST on various types of retail business transactions, and shows the accounting and posting of retail transactions where the receipt is printed at the point of sale (POS).</span></span>

> [!NOTE]
> <span data-ttu-id="d0de3-107">このトピックは、Microsoft Dynamics 365 for Finance and Operations および Microsoft Dynamics 365 for Retail の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-107">This topic applies to both Microsoft Dynamics 365 for Finance and Operations, and Microsoft Dynamics 365 for Retail.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d0de3-108">必要条件</span><span class="sxs-lookup"><span data-stu-id="d0de3-108">Prerequisites</span></span>

- <span data-ttu-id="d0de3-109">Finance and Operations でのインド向け GST を設定します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-109">Set up GST for India in Finance and Operations.</span></span> <span data-ttu-id="d0de3-110">詳細については、[インドの商品及びサービス税 (GST)](../../financials/localizations/apac-ind-gst.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0de3-110">For more information, see [India Goods and Services Tax (GST)](../../financials/localizations/apac-ind-gst.md).</span></span>
- <span data-ttu-id="d0de3-111">小売チャネル コンポーネントを構成します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-111">Configure Retail channel components.</span></span> <span data-ttu-id="d0de3-112">インド固有の機能を有効にするには、小売チャネル コンポーネントの拡張機能を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-112">To enable India-specific functionality, you must configure extensions for Retail channel components.</span></span> <span data-ttu-id="d0de3-113">詳細については、[配置ガイドライン](./apac-ind-loc-deployment-guidelines.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0de3-113">For more information, see the [deployment guidelines](./apac-ind-loc-deployment-guidelines.md).</span></span>

## <a name="india-tax-entities-for-retail"></a><span data-ttu-id="d0de3-114">小売り業向けインドの税エンティティ</span><span class="sxs-lookup"><span data-stu-id="d0de3-114">India tax entities for Retail</span></span>

<span data-ttu-id="d0de3-115">次の表は、小売でのインドの税エンティティ用ナビゲーション パスを示します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-115">The following table shows the navigation paths for the India tax entities in Retail.</span></span>

| <span data-ttu-id="d0de3-116">インドの税エンティティ</span><span class="sxs-lookup"><span data-stu-id="d0de3-116">India tax entities</span></span>                  | <span data-ttu-id="d0de3-117">小売でのナビゲーション パス</span><span class="sxs-lookup"><span data-stu-id="d0de3-117">Navigation path in Retail</span></span>                                                     |
|-------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="d0de3-118">ビジネス業種</span><span class="sxs-lookup"><span data-stu-id="d0de3-118">Business verticals</span></span>                  | <span data-ttu-id="d0de3-119">小売 \> チャネル設定 \> 売上税 \> ビジネス業種</span><span class="sxs-lookup"><span data-stu-id="d0de3-119">Retail \> Channel setup \> Sales taxes \> Business verticals</span></span>                  |
| <span data-ttu-id="d0de3-120">エンタープライズ税登録番号</span><span class="sxs-lookup"><span data-stu-id="d0de3-120">Enterprise tax registration numbers</span></span> | <span data-ttu-id="d0de3-121">小売り \> チャネル設定 \> 売上税 \> エンタープライズ税登録番号</span><span class="sxs-lookup"><span data-stu-id="d0de3-121">Retail \> Channel setup \> Sales taxes \> Enterprise tax registration numbers</span></span> |
| <span data-ttu-id="d0de3-122">GST 参照番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="d0de3-122">GST reference number sequence group</span></span> | <span data-ttu-id="d0de3-123">小売 \> チャネル設定 \> 売上税 \> GST 参照番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="d0de3-123">Retail \> Channel setup \> Sales taxes \> GST reference number sequence group</span></span> |
| <span data-ttu-id="d0de3-124">HSN コード</span><span class="sxs-lookup"><span data-stu-id="d0de3-124">HSN codes</span></span>                           | <span data-ttu-id="d0de3-125">小売 \> チャネル設定 \> 売上税 \> HSN コード</span><span class="sxs-lookup"><span data-stu-id="d0de3-125">Retail \> Channel setup \> Sales taxes \> HSN codes</span></span>                           |
| <span data-ttu-id="d0de3-126">サービス アカウント コード</span><span class="sxs-lookup"><span data-stu-id="d0de3-126">Service accounting codes</span></span>            | <span data-ttu-id="d0de3-127">小売 \> チャネル設定 \> 売上税 \> サービス アカウント コード</span><span class="sxs-lookup"><span data-stu-id="d0de3-127">Retail \> Channel setup \> Sales taxes \> Service accounting codes</span></span>            |
| <span data-ttu-id="d0de3-128">相殺階層プロファイルを管理する</span><span class="sxs-lookup"><span data-stu-id="d0de3-128">Maintain setoff hierarchy profiles</span></span>  | <span data-ttu-id="d0de3-129">小売 \> チャネル設定 \> 売上税 \> 相殺階層プロファイルを管理する</span><span class="sxs-lookup"><span data-stu-id="d0de3-129">Retail \> Channel setup \> Sales taxes \> Maintain setoff hierarchy profiles</span></span>  |
| <span data-ttu-id="d0de3-130">VAT スケジュール</span><span class="sxs-lookup"><span data-stu-id="d0de3-130">VAT schedules</span></span>                       | <span data-ttu-id="d0de3-131">小売 \> チャネル設定 \> 売上税 \> VAT スケジュール</span><span class="sxs-lookup"><span data-stu-id="d0de3-131">Retail \> Channel setup \> Sales taxes \> VAT schedules</span></span>                       |
| <span data-ttu-id="d0de3-132">税設定</span><span class="sxs-lookup"><span data-stu-id="d0de3-132">Tax setup</span></span>                           | <span data-ttu-id="d0de3-133">小売 \> チャネル設定 \> 売上税 \> 税コンフィギュレーション \> 税設定</span><span class="sxs-lookup"><span data-stu-id="d0de3-133">Retail \> Channel setup \> Sales taxes \> Tax configuration \> Tax setup</span></span>      |

> [!NOTE]
> <span data-ttu-id="d0de3-134">小売でのインドの税エンティティ用ナビゲーション パスは、Finance and Operations でのナビゲーション パスと異なります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-134">The navigation paths for the India tax entities in Retail differ from the navigations paths in Finance and Operations.</span></span> <span data-ttu-id="d0de3-135">Finance and Operations のナビゲーション パスの詳細については、[インドの商品及びサービス税 (GST)](../../financials/localizations/apac-ind-gst.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0de3-135">For information about the navigation paths in Finance and Operations, see [India Goods and Services Tax (GST)](../../financials/localizations/apac-ind-gst.md).</span></span>

## <a name="validate-tax-information-for-the-retail-store"></a><span data-ttu-id="d0de3-136">小売店舗の税情報の検証</span><span class="sxs-lookup"><span data-stu-id="d0de3-136">Validate tax information for the retail store</span></span>

<span data-ttu-id="d0de3-137">小売店舗の税情報は、選択した小売倉庫から取得されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-137">The tax information for the retail store comes from the selected retail warehouse.</span></span> <span data-ttu-id="d0de3-138">この倉庫は倉庫マスターで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-138">This warehouse is defined in the warehouse master.</span></span> <span data-ttu-id="d0de3-139">店舗からの構成済み税情報は POS レシートに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-139">The configured tax information from the store is printed on the POS receipt.</span></span> <span data-ttu-id="d0de3-140">また、財務転記のために小売用バック オフィスの小売販売注文で更新されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-140">It's also updated on the retail sales order at the retail headquarters for the financial postings.</span></span>

<span data-ttu-id="d0de3-141">以下の手順に従い、小売店舗の税情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-141">Follow these steps to view the tax information for a retail store.</span></span>

1. <span data-ttu-id="d0de3-142">**小売** \> **チャンネル** \> **小売店舗** \> **すべての小売店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-142">Go to **Retail** \> **Channels** \> **Retail stores** \> **All retail stores**.</span></span>
2. <span data-ttu-id="d0de3-143">小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-143">Select a retail store.</span></span>
3. <span data-ttu-id="d0de3-144">**税金情報** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-144">Select the **Tax information** FastTab.</span></span>

## <a name="configure-language-texts-and-custom-fields"></a><span data-ttu-id="d0de3-145">言語テキストおよびカスタム フィールドのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d0de3-145">Configure language texts and custom fields</span></span>

<span data-ttu-id="d0de3-146">POS レシート形式で使用される言語テキストおよびカスタム フィールドを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-146">You can configure the language text and custom fields that are used in the POS receipt formats.</span></span> <span data-ttu-id="d0de3-147">レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-147">The default company of the user who creates the receipt setup should be the same as the legal entity where the language text setup is created.</span></span> <span data-ttu-id="d0de3-148">または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-148">Alternatively, the same language texts should be created in both the user's default company and the legal entity of the store that the setup is created for.</span></span>

### <a name="set-up-the-pos-language-text"></a><span data-ttu-id="d0de3-149">POS 言語テキストの設定</span><span class="sxs-lookup"><span data-stu-id="d0de3-149">Set up the POS language text</span></span>

1. <span data-ttu-id="d0de3-150">**小売** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **言語テキスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-150">Go to **Retail** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Language text**.</span></span>
2. <span data-ttu-id="d0de3-151">**POS** タブの、**POS 言語テキスト** クイックタブで、テキストの言語 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-151">On the **POS** tab, on the **POS language text** FastTab, select the language ID for the text.</span></span> <span data-ttu-id="d0de3-152">言語はユーザーの優先言語と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-152">The language should match the user's preferred language.</span></span>
3. <span data-ttu-id="d0de3-153">**テキスト ID** フィールドに、**900001** 異常の一意の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-153">In the **Text ID** field, enter a unique ID that is equal to or more than **900001**.</span></span>
4. <span data-ttu-id="d0de3-154">**テキスト**フィールドで、言語テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-154">In the **Text** field, enter the language text.</span></span>

![言語テキスト](media/apac-ind-gst-language-text.png)

### <a name="create-custom-fields"></a><span data-ttu-id="d0de3-156">カスタム フィールドの作成</span><span class="sxs-lookup"><span data-stu-id="d0de3-156">Create custom fields</span></span>

<span data-ttu-id="d0de3-157">カスタム フィールドを作成するときは、**キャプション テキスト ID** フィールドの値が、**言語テキスト** ページの **テキスト ID** フィールドに入力した値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-157">When you create custom fields, the value of the **Caption text ID** field must match the value that you entered for the **Text ID** field on the **Language text** page.</span></span>

1. <span data-ttu-id="d0de3-158">**小売** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **カスタム フィールド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-158">Go to **Retail** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Custom fields**.</span></span>
2. <span data-ttu-id="d0de3-159">フィールドの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-159">Enter a name for the field.</span></span>
3. <span data-ttu-id="d0de3-160">フィールド タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-160">Select the field type.</span></span>
4. <span data-ttu-id="d0de3-161">**キャプション テキスト ID** フィールドで、**言語テキスト** ページの言語テキストのいずれかに **テキスト ID** 値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-161">In the **Caption text ID** field, enter the **Text ID** value for one of the language texts on the **Language text** page.</span></span>

![カスタム フィールド](media/apac-ind-gst-custom-fields.png)

## <a name="create-the-receipt-format"></a><span data-ttu-id="d0de3-163">受領書フォーマットの作成</span><span class="sxs-lookup"><span data-stu-id="d0de3-163">Create the receipt format</span></span>

<span data-ttu-id="d0de3-164">受領書フォーマット デザイナーを使用して、適切な領収書セクションにカスタム フィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-164">You can use Receipt format designer to add custom fields to the appropriate receipt sections.</span></span> <span data-ttu-id="d0de3-165">詳細については、[レシートのテンプレートおよび印刷](../receipt-templates-printing.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d0de3-165">For more information, see [Receipt templates and printing](../receipt-templates-printing.md).</span></span>

1. <span data-ttu-id="d0de3-166">**小売** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **受領書フォーマット**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-166">Go to **Retail** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Receipt formats**.</span></span>
2. <span data-ttu-id="d0de3-167">**レシート** 領収書タイプのために領収書書式を選択して、必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-167">Select a receipt format for the **Receipt** receipt type, and make the required changes.</span></span>

![受領書フォーマットのデザイン](media/apac-ind-gst-receipt-format.png)

## <a name="update-receipt-profiles"></a><span data-ttu-id="d0de3-169">領収書プロファイルの更新</span><span class="sxs-lookup"><span data-stu-id="d0de3-169">Update receipt profiles</span></span>

<span data-ttu-id="d0de3-170">領収書フォーマットの作成すると、領収書プロファイルにフォーマットを割当てることができます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-170">After you create a receipt format, you can assign that format to a receipt profile.</span></span>

<span data-ttu-id="d0de3-171">以下の手順を実行して、領収書プロファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-171">Follow these steps to update a receipt profile.</span></span>

1. <span data-ttu-id="d0de3-172">**小売** \> **設定** \> **POS** \> **レシート プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-172">Go to **Retail** \> **Setup** \> **POS** \> **Receipt profile**.</span></span>
2. <span data-ttu-id="d0de3-173">更新するレシート プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-173">Select the receipt profile to update.</span></span>
3. <span data-ttu-id="d0de3-174">**編集**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-174">Select **Edit**.</span></span>
4. <span data-ttu-id="d0de3-175">リスト内のレシート タイプごとに、受領書フォーマットを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-175">For each receipt type in the list, select a receipt format.</span></span>

## <a name="update-the-pos-invoice-number"></a><span data-ttu-id="d0de3-176">POS 請求書番号の更新</span><span class="sxs-lookup"><span data-stu-id="d0de3-176">Update the POS invoice number</span></span>

<span data-ttu-id="d0de3-177">顧客の小売取引の請求書番号を使用して POS レシート番号を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-177">You can reconcile the POS receipt number with the invoice number for customer retail transactions.</span></span> <span data-ttu-id="d0de3-178">**小売パラメータ** ページの **転記** タブで **POS 請求書番号を更新** オプションに **はい** をセットする場合、対応する小売販売注文の **取引 ID** フィールドに POS 請求書番号が入力されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-178">If you set the **Update POS invoice number** option to **Yes** on the **Posting** tab of the **Retail parameters** page, the POS receipt number is entered in the **Transaction ID** field for corresponding retail sales orders.</span></span>

<span data-ttu-id="d0de3-179">既存の領収書番号書式に店舗番号と端末番号の両方が含まれる場合にのみ、**POS 請求書番号を更新** オプションに **はい** をセットすることができます。 </span><span class="sxs-lookup"><span data-stu-id="d0de3-179">You can set the **Update POS invoice number** option to **Yes** only if the existing receipt number format includes both the store number and the terminal number.</span></span> <span data-ttu-id="d0de3-180">次の図は、レシート番号付けに店舗番号と端末番号が含まれる、POS 機能プロファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-180">The following illustration shows a POS functionality profile where the receipt numbering includes the store number and the terminal number.</span></span>

![POS 機能プロファイル](media/apac-ind-gst-pos-functionality-profile.png)

## <a name="run-a-distribution-schedule"></a><span data-ttu-id="d0de3-182">配送スケジュールの実行</span><span class="sxs-lookup"><span data-stu-id="d0de3-182">Run a distribution schedule</span></span>

<span data-ttu-id="d0de3-183">小売用バックオフィスからの税エンジン (GTE) データを POS データベースに同期させるには、**配送スケジュール** ページにジョブを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-183">To synchronize Tax Engine (GTE) data from retail headquarter to the POS database, you must add a job to the **Distribution schedule** page.</span></span>

<span data-ttu-id="d0de3-184">以下の手順に従い、ジョブが存在していることを検証して、ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-184">Follow these steps to verify that the job exists and to run the job.</span></span>

1. <span data-ttu-id="d0de3-185">**小売** \> **定期処理** \> **データ配送** \> **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-185">Go to **Retail** \> **Periodic** \> **Data distribution** \> **Distribution schedule**.</span></span>
2. <span data-ttu-id="d0de3-186">新しいジョブ、**1180** が **汎用税エンジン** のために追加されていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-186">Verify that a new job, **1180**, has been added for **Generic tax engine**.</span></span>
3. <span data-ttu-id="d0de3-187">すべてのジョブを実行します (**9999**)。</span><span class="sxs-lookup"><span data-stu-id="d0de3-187">Run all the jobs (**9999**).</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="d0de3-188">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="d0de3-188">Example scenarios</span></span>

<span data-ttu-id="d0de3-189">次のシナリオ例はインドの取引サンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-189">The following example scenarios walk you through sample transactions for India:</span></span>

- <span data-ttu-id="d0de3-190">シナリオ 1: 登録済の顧客に対する販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-190">Scenario 1: Sell to a registered customer</span></span>
- <span data-ttu-id="d0de3-191">シナリオ 2: 顧客に対する課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-191">Scenario 2: Sell taxable goods to a consumer</span></span>
- <span data-ttu-id="d0de3-192">シナリオ 3: GSTが価格に包まれる、匿名の顧客への課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-192">Scenario 3: Sell taxable goods to an anonymous customer where GST is price-inclusive</span></span>
- <span data-ttu-id="d0de3-193">シナリオ 4: 免税品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-193">Scenario 4: Sell an exempted good</span></span>
- <span data-ttu-id="d0de3-194">シナリオ 5: GST を含む取引の返品</span><span class="sxs-lookup"><span data-stu-id="d0de3-194">Scenario 5: Return the transaction that has GST</span></span>

### <a name="scenario-1-sell-to-a-registered-customer"></a><span data-ttu-id="d0de3-195">シナリオ 1: 登録済の顧客に対する販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-195">Scenario 1: Sell to a registered customer</span></span>

<span data-ttu-id="d0de3-196">登録済み顧客への販売は *企業間* (B2B) 販売と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-196">Sales to a registered customer are known as *business-to-business* (B2B) sales.</span></span> <span data-ttu-id="d0de3-197">店舗の場所と供給の位置 (つまり、顧客の住所) が同じ州にある場合、取引は *イントラスタット販売* で、中央 GST (CGST) および州 GST (SGST) が支払われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-197">If the store location and the place of supply (that is, the customer address) are in the same state, the transaction is an *intrastate sale*, and Central GST (CGST) and State GST (SGST) must be paid.</span></span> <span data-ttu-id="d0de3-198">店舗の場所および供給の位置が異なる州にある場所、取引は *州間販売* で、統合された GST (IGST) が支払われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0de3-198">If the store location and the place of supply are in different states, the transaction is an *interstate sale*, and Integrated GST (IGST) must be paid.</span></span>

> [!NOTE]
> <span data-ttu-id="d0de3-199">これらの取引の場合、顧客の住所および登録番号のフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="d0de3-199">For these transactions, the fields for the customer address and the registration number are required.</span></span>

1. <span data-ttu-id="d0de3-200">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-200">Sign in to the POS.</span></span>
2. <span data-ttu-id="d0de3-201">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-201">Enter the items, and then select **Enter**.</span></span>

    ![POS 顧客注文](media/apac-ind-gst-pos-customer-order.png)

3. <span data-ttu-id="d0de3-203">GST 計算を検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-203">Validate the GST calculations.</span></span> <span data-ttu-id="d0de3-204">税の設定で定義されているレートを検討します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-204">Consider the rate that is defined in the tax setup.</span></span>

    | <span data-ttu-id="d0de3-205">品目/サービス</span><span class="sxs-lookup"><span data-stu-id="d0de3-205">Item/service</span></span> | <span data-ttu-id="d0de3-206">単価</span><span class="sxs-lookup"><span data-stu-id="d0de3-206">Unit price</span></span> | <span data-ttu-id="d0de3-207">税率</span><span class="sxs-lookup"><span data-stu-id="d0de3-207">Tax rates</span></span>          | <span data-ttu-id="d0de3-208">CGST</span><span class="sxs-lookup"><span data-stu-id="d0de3-208">CGST</span></span>     | <span data-ttu-id="d0de3-209">SGST</span><span class="sxs-lookup"><span data-stu-id="d0de3-209">SGST</span></span>      |
    |--------------|------------|--------------------|----------|-----------|
    | <span data-ttu-id="d0de3-210">M0001</span><span class="sxs-lookup"><span data-stu-id="d0de3-210">M0001</span></span>        | <span data-ttu-id="d0de3-211">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-211">10,000.00</span></span>  | <span data-ttu-id="d0de3-212">CGST 12%、SGST 11%</span><span class="sxs-lookup"><span data-stu-id="d0de3-212">CGST 12%, SGST 11%</span></span> | <span data-ttu-id="d0de3-213">1,200.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-213">1,200.00</span></span> | <span data-ttu-id="d0de3-214">1,100.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-214">1,100.00</span></span>  |
    | <span data-ttu-id="d0de3-215">M0002</span><span class="sxs-lookup"><span data-stu-id="d0de3-215">M0002</span></span>        | <span data-ttu-id="d0de3-216">5,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-216">5,000.00</span></span>   | <span data-ttu-id="d0de3-217">CGST 10%、SGST 10%</span><span class="sxs-lookup"><span data-stu-id="d0de3-217">CGST 10%, SGST 10%</span></span> | <span data-ttu-id="d0de3-218">500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-218">500.00</span></span>   | <span data-ttu-id="d0de3-219">500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-219">500.00</span></span>    |
    | <span data-ttu-id="d0de3-220">S0001</span><span class="sxs-lookup"><span data-stu-id="d0de3-220">S0001</span></span>        | <span data-ttu-id="d0de3-221">1,200.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-221">1,200.00</span></span>   | <span data-ttu-id="d0de3-222">CGST 11%、SGST 5%</span><span class="sxs-lookup"><span data-stu-id="d0de3-222">CGST 11%, SGST 5%</span></span>  | <span data-ttu-id="d0de3-223">132.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-223">132.00</span></span>   | <span data-ttu-id="d0de3-224">60.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-224">60.00</span></span>     |
    |              | <span data-ttu-id="d0de3-225">16,200.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-225">16,200.00</span></span>  |                    | <span data-ttu-id="d0de3-226">1,832.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-226">1,832.00</span></span> | <span data-ttu-id="d0de3-227">1,660.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-227">1,660.00</span></span>  |
    | <span data-ttu-id="d0de3-228">合計金額</span><span class="sxs-lookup"><span data-stu-id="d0de3-228">Total amount</span></span> |            |                    |          | <span data-ttu-id="d0de3-229">19,692.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-229">19,692.00</span></span> |

4. <span data-ttu-id="d0de3-230">**注文** \> **顧客注文の作成** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-230">Select **Orders** \> **Create customer order**.</span></span>
5. <span data-ttu-id="d0de3-231">**顧客の追加** を選択して、顧客アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-231">Select **Add customer**, and select the customer account.</span></span>
6. <span data-ttu-id="d0de3-232">**すべて集荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-232">Select **Pick up all**.</span></span>
7. <span data-ttu-id="d0de3-233">店舗および集荷日を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-233">Select the store and the pick-up date.</span></span>
8. <span data-ttu-id="d0de3-234">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-234">Select **OK**.</span></span>

    ![POS 顧客注文](./media/apac-ind-gst-pos-customer-order2.png)

    > [!NOTE]
    > <span data-ttu-id="d0de3-236">この例では、店舗場所の州が Delhi で、顧客住所の州も Delhi です。</span><span class="sxs-lookup"><span data-stu-id="d0de3-236">In this example, the state of the store location is Delhi, and the state of the customer address is also Delhi.</span></span> <span data-ttu-id="d0de3-237">州が同じであるため、イントラスタット GST が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-237">Because the state is the same, intrastate GST is calculated.</span></span>

9. <span data-ttu-id="d0de3-238">**正確** を選択して預金支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-238">Select **Exact** to process the deposit payment.</span></span>
10. <span data-ttu-id="d0de3-239">領収書の検証:</span><span class="sxs-lookup"><span data-stu-id="d0de3-239">Validate the receipt:</span></span>

    1. <span data-ttu-id="d0de3-240">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-240">Select **Show journal**.</span></span>
    2. <span data-ttu-id="d0de3-241">取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-241">Select the transactions.</span></span>
    3. <span data-ttu-id="d0de3-242">**レシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-242">Select **Receipt**.</span></span>

    ![レシート例](media/apac-ind-gst-s1-receipt1.png)

11. <span data-ttu-id="d0de3-244">小売用バックオフィスで販売注文および税ドキュメントを検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-244">Validate the sales order and tax document in Retail headquarters:</span></span>

    1. <span data-ttu-id="d0de3-245">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-245">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-246">販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-246">Select the sales order.</span></span>
    3. <span data-ttu-id="d0de3-247">アクション ペインの、**販売** タブの、**税** グループで、**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-247">On the Action Pane, on the **Sell** tab, in the **Tax** group, select **Tax document**.</span></span>

    ![税務書類](media/apac-ind-gst-tax-document.png)

12. <span data-ttu-id="d0de3-249">顧客の注文を取り消して処理します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-249">Recall and process the customer order:</span></span>

    1. <span data-ttu-id="d0de3-250">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-250">Sign in to the POS.</span></span>
    2. <span data-ttu-id="d0de3-251">**注文の取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-251">Select **Recall order**.</span></span>
    3. <span data-ttu-id="d0de3-252">注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-252">Search for and select the order.</span></span>
    4. <span data-ttu-id="d0de3-253">**ピッキングと梱包** \> **集荷** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-253">Select **Picking and packing** \> **Pickup**</span></span>
    5. <span data-ttu-id="d0de3-254">**すべて選択** および **集荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-254">Select **Select all** and then **Pickup**.</span></span>

    ![顧客注文の処理](media/apac-ind-gst-process-customer-order.png)

13. <span data-ttu-id="d0de3-256">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-256">Select **Exact** to process the payment.</span></span>
14. <span data-ttu-id="d0de3-257">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-257">Validate the receipt.</span></span>

    ![レシート例](media/apac-ind-gst-s1-receipt2.png)

15. <span data-ttu-id="d0de3-259">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-259">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="d0de3-260">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-260">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-261">販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-261">Select the sales order.</span></span>
    3. <span data-ttu-id="d0de3-262">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-262">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="d0de3-263">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-263">Select **Voucher**.</span></span>

        | <span data-ttu-id="d0de3-264">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="d0de3-264">Ledger account name</span></span>  | <span data-ttu-id="d0de3-265">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-265">Debit amount (Rs.)</span></span> | <span data-ttu-id="d0de3-266">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-266">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="d0de3-267">顧客口座</span><span class="sxs-lookup"><span data-stu-id="d0de3-267">Customer account</span></span>     | <span data-ttu-id="d0de3-268">19,692.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-268">19,692.00</span></span>          |                     |
        | <span data-ttu-id="d0de3-269">CGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-269">CGST payable account</span></span> |                    | <span data-ttu-id="d0de3-270">1,832.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-270">1,832.00</span></span>            |
        | <span data-ttu-id="d0de3-271">SGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-271">SGST payable account</span></span> |                    | <span data-ttu-id="d0de3-272">1,660.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-272">1,660.00</span></span>            |
        | <span data-ttu-id="d0de3-273">売上勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-273">Sales account</span></span>        |                    | <span data-ttu-id="d0de3-274">16,200.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-274">16,200.00</span></span>           |

    5. <span data-ttu-id="d0de3-275">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-275">Select **Tax document**.</span></span>
    6. <span data-ttu-id="d0de3-276">領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-276">Verify that the receipt number is updated as the transaction ID.</span></span>

        ![税務書類](media/apac-ind-gst-tax-document2.png)

### <a name="scenario-2-sell-taxable-goods-to-a-consumer"></a><span data-ttu-id="d0de3-278">シナリオ 2: 顧客に対する課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-278">Scenario 2: Sell taxable goods to a consumer</span></span>

<span data-ttu-id="d0de3-279">未登録の顧客に販売するとき、その販売は *企業と顧客間* (B2C) 販売と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-279">When you sell to unregistered customers, the sales are referred to as *business-to-consumer* (B2C) sales.</span></span> <span data-ttu-id="d0de3-280">税は B2B および B2C 販売と同じ方法で計算されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-280">Tax is calculated in the same manner for B2B and B2C sales.</span></span>

1. <span data-ttu-id="d0de3-281">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-281">Sign in to the POS.</span></span>
2. <span data-ttu-id="d0de3-282">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-282">Enter an item, and then select **Enter**.</span></span>
3. <span data-ttu-id="d0de3-283">**顧客の追加** を選択して、顧客アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-283">Select **Add customer**, and select the customer account.</span></span>

    ![取引の例](media/apac-ind-gst-example-trx.png)

    > [!NOTE]
    > <span data-ttu-id="d0de3-285">この例では、店舗場所の州は Delhi ですが、顧客住所の州は Bengaluru (Bangalore) です。</span><span class="sxs-lookup"><span data-stu-id="d0de3-285">In this example, the state of the store location is Delhi, but the state of the customer address is Bengaluru (Bangalore).</span></span> <span data-ttu-id="d0de3-286">州が異なるため、州間 GST が計算されます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-286">Because the states differ, interstate GST is computed.</span></span>

4. <span data-ttu-id="d0de3-287">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-287">Select **Exact** to process the payment.</span></span>
5. <span data-ttu-id="d0de3-288">領収書の検証:</span><span class="sxs-lookup"><span data-stu-id="d0de3-288">Validate the receipt:</span></span>

    1. <span data-ttu-id="d0de3-289">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-289">Select **Show journal**.</span></span>
    2. <span data-ttu-id="d0de3-290">取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-290">Select the transactions.</span></span>
    3. <span data-ttu-id="d0de3-291">**レシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-291">Select **Receipt**.</span></span>

    ![領収書の検証](media/apac-ind-gst-receipt-validation.png)

6. <span data-ttu-id="d0de3-293">小売用バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-293">Validate the retail sales invoice in Retail headquarters:</span></span>

    1. <span data-ttu-id="d0de3-294">**小売** \> **小売 IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-294">Go to **Retail** \> **Retail IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="d0de3-295">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="d0de3-295">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="d0de3-296">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-296">Close the page.</span></span>

7. <span data-ttu-id="d0de3-297">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="d0de3-297">Post the statement:</span></span>

    1. <span data-ttu-id="d0de3-298">**小売** \> **チャネル** \> **小売店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-298">Go to **Retail** \> **Channels** \> **Retail stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="d0de3-299">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-299">Create a statement.</span></span>
    3. <span data-ttu-id="d0de3-300">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-300">Select **Calculate statement** and then **Post statement**.</span></span>

8. <span data-ttu-id="d0de3-301">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-301">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="d0de3-302">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-302">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-303">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-303">Select the sales invoice.</span></span>
    3. <span data-ttu-id="d0de3-304">**販売注文行** \> **税金情報** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-304">Select **Sales order lines** \> **Tax information**.</span></span>
    4. <span data-ttu-id="d0de3-305">該当するタブで、場所 (店舗アドレス) および顧客の住所を確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-305">On the appropriate tabs, verify the location (store address) and the customer address.</span></span>

        ![税金情報](media/apac-ind-gst-tax-info.png)

    5. <span data-ttu-id="d0de3-307">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-307">Select **OK**.</span></span>
    6. <span data-ttu-id="d0de3-308">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-308">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    7. <span data-ttu-id="d0de3-309">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-309">Select **Voucher**.</span></span>

        | <span data-ttu-id="d0de3-310">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="d0de3-310">Ledger account name</span></span>  | <span data-ttu-id="d0de3-311">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-311">Debit amount (Rs.)</span></span> | <span data-ttu-id="d0de3-312">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-312">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="d0de3-313">顧客口座</span><span class="sxs-lookup"><span data-stu-id="d0de3-313">Customer account</span></span>     | <span data-ttu-id="d0de3-314">12,500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-314">12,500.00</span></span>          |                     |
        | <span data-ttu-id="d0de3-315">IGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-315">IGST payable account</span></span> |                    | <span data-ttu-id="d0de3-316">2,500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-316">2,500.00</span></span>            |
        | <span data-ttu-id="d0de3-317">売上勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-317">Sales account</span></span>        |                    | <span data-ttu-id="d0de3-318">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-318">10,000.00</span></span>           |

    8. <span data-ttu-id="d0de3-319">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-319">Select **Tax document**.</span></span>
    9. <span data-ttu-id="d0de3-320">領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-320">Verify that the receipt number is updated as the transaction ID.</span></span>

### <a name="scenario-3-sell-taxable-goods-to-an-anonymous-customer-where-gst-is-price-inclusive"></a><span data-ttu-id="d0de3-321">シナリオ 3: GSTが価格に包まれる、匿名の顧客への課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-321">Scenario 3: Sell taxable goods to an anonymous customer where GST is price-inclusive</span></span>

1. <span data-ttu-id="d0de3-322">小売店舗での価格包含性を定義します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-322">Define price-inclusiveness at the retail store:</span></span>

    1. <span data-ttu-id="d0de3-323">**小売** \> **チャンネル** \> **小売店舗** \> **すべての小売店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-323">Go to **Retail** \> **Channels** \> **Retail stores** \> **All retail stores**.</span></span>
    2. <span data-ttu-id="d0de3-324">小売店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-324">Select a retail store.</span></span>
    3. <span data-ttu-id="d0de3-325">**税込価格** オプションに **はい** をセットします。</span><span class="sxs-lookup"><span data-stu-id="d0de3-325">Set the **Prices include sales tax** option to **Yes**.</span></span>

2. <span data-ttu-id="d0de3-326">配送スケジュールを実行します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-326">Run the distribution schedule:</span></span>

    1. <span data-ttu-id="d0de3-327">**小売** \> **小売 IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-327">Go to **Retail** \> **Retail IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="d0de3-328">POS データベース内の変更を更新するジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-328">Run the job to update the changes in the POS database.</span></span>
    3. <span data-ttu-id="d0de3-329">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-329">Close the page.</span></span>

3. <span data-ttu-id="d0de3-330">トランザクションの入力:</span><span class="sxs-lookup"><span data-stu-id="d0de3-330">Enter a transaction:</span></span>

    1. <span data-ttu-id="d0de3-331">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-331">Sign in to the POS.</span></span>
    2. <span data-ttu-id="d0de3-332">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-332">Enter an item, and then select **Enter**.</span></span> <span data-ttu-id="d0de3-333">この例では、次の値を持つ品目を使用します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-333">For this example, use an item that has the following values:</span></span>

        - <span data-ttu-id="d0de3-334">**課税対象値:** 10,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-334">**Taxable value:** 10,000.00</span></span>
        - <span data-ttu-id="d0de3-335">**CGST:** 12 %</span><span class="sxs-lookup"><span data-stu-id="d0de3-335">**CGST:** 12 percent</span></span>
        - <span data-ttu-id="d0de3-336">**SGST:** 11 %</span><span class="sxs-lookup"><span data-stu-id="d0de3-336">**SGST:** 11 percent</span></span>

    ![取引の例](media/apac-ind-gst-trx-example.png)

4. <span data-ttu-id="d0de3-338">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-338">Select **Exact** to process the payment.</span></span>
5. <span data-ttu-id="d0de3-339">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-339">Validate the receipt.</span></span>

    ![レシート例](media/apac-ind-gst-s3-receipt4.png)

6. <span data-ttu-id="d0de3-341">小売用バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-341">Validate the retail sales invoice in Retail headquarters:</span></span>

    1. <span data-ttu-id="d0de3-342">**小売** \> **小売 IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-342">Go to **Retail** \> **Retail IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="d0de3-343">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="d0de3-343">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="d0de3-344">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-344">Close the page.</span></span>

7. <span data-ttu-id="d0de3-345">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="d0de3-345">Post the statement:</span></span>

    1. <span data-ttu-id="d0de3-346">**小売** \> **チャネル** \> **小売店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-346">Go to **Retail** \> **Channels** \> **Retail stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="d0de3-347">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-347">Create a statement.</span></span>
    3. <span data-ttu-id="d0de3-348">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-348">Select **Calculate statement** and then **Post statement**.</span></span>

8. <span data-ttu-id="d0de3-349">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-349">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="d0de3-350">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-350">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-351">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-351">Select the sales invoice.</span></span>
    3. <span data-ttu-id="d0de3-352">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-352">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="d0de3-353">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-353">Select **Voucher**.</span></span>

        | <span data-ttu-id="d0de3-354">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="d0de3-354">Ledger account name</span></span>  | <span data-ttu-id="d0de3-355">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-355">Debit amount (Rs.)</span></span> | <span data-ttu-id="d0de3-356">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-356">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="d0de3-357">顧客口座</span><span class="sxs-lookup"><span data-stu-id="d0de3-357">Customer account</span></span>     | <span data-ttu-id="d0de3-358">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-358">10,000.00</span></span>          |                     |
        | <span data-ttu-id="d0de3-359">CGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-359">CGST payable account</span></span> |                    | <span data-ttu-id="d0de3-360">975.61</span><span class="sxs-lookup"><span data-stu-id="d0de3-360">975.61</span></span>              |
        | <span data-ttu-id="d0de3-361">SGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-361">SGST payable account</span></span> |                    | <span data-ttu-id="d0de3-362">894.31</span><span class="sxs-lookup"><span data-stu-id="d0de3-362">894.31</span></span>              |
        | <span data-ttu-id="d0de3-363">売上勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-363">Sales account</span></span>        |                    | <span data-ttu-id="d0de3-364">8,130.08</span><span class="sxs-lookup"><span data-stu-id="d0de3-364">8,130.08</span></span>            |

    5. <span data-ttu-id="d0de3-365">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-365">Select **Tax document**.</span></span>
    6. <span data-ttu-id="d0de3-366">GST 参照番号順序グループで定義されている GST 番号順序に従って取引 ID が更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-366">Verify that the transaction ID is updated according to the GST number sequence that is defined in the GST reference number sequence group.</span></span>

        ![税務書類のトランザクション ID](media/apac-ind-gst-tax-doc-trx-id.png)

### <a name="scenario-4-sell-an-exempted-good"></a><span data-ttu-id="d0de3-368">シナリオ 4: 免税品の販売</span><span class="sxs-lookup"><span data-stu-id="d0de3-368">Scenario 4: Sell an exempted good</span></span>

1. <span data-ttu-id="d0de3-369">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-369">Sign in to the POS.</span></span>
2. <span data-ttu-id="d0de3-370">免税品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-370">Enter an exempted item.</span></span>

    ![免税品目トランザクション](media/apac-ind-gst-exempted-item-trx.png)

3. <span data-ttu-id="d0de3-372">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-372">Select **Exact** to process the payment.</span></span>
4. <span data-ttu-id="d0de3-373">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-373">Validate the receipt.</span></span>

    ![レシート example.png](media/apac-ind-gst-receipt-4.png)

5. <span data-ttu-id="d0de3-375">小売用バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-375">Validate the retail sales invoice in Retail headquarters:</span></span>

    1. <span data-ttu-id="d0de3-376">**小売** \> **小売 IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-376">Go to **Retail** \> **Retail IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="d0de3-377">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="d0de3-377">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="d0de3-378">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-378">Close the page.</span></span>

6. <span data-ttu-id="d0de3-379">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="d0de3-379">Post the statement:</span></span>

    1. <span data-ttu-id="d0de3-380">**小売** \> **チャネル** \> **小売店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-380">Go to **Retail** \> **Channels** \> **Retail stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="d0de3-381">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-381">Create a statement.</span></span>
    3. <span data-ttu-id="d0de3-382">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-382">Select **Calculate statement** and then **Post statement**.</span></span>

7. <span data-ttu-id="d0de3-383">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-383">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="d0de3-384">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-384">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-385">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-385">Select the sales invoice.</span></span>
    3. <span data-ttu-id="d0de3-386">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-386">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="d0de3-387">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-387">Select **Voucher**.</span></span>

        | <span data-ttu-id="d0de3-388">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="d0de3-388">Ledger account name</span></span>    | <span data-ttu-id="d0de3-389">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-389">Debit amount (Rs.)</span></span> | <span data-ttu-id="d0de3-390">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-390">Credit amount (Rs.)</span></span> |
        |------------------------|--------------------|---------------------|
        | <span data-ttu-id="d0de3-391">顧客口座</span><span class="sxs-lookup"><span data-stu-id="d0de3-391">Customer account</span></span>       | <span data-ttu-id="d0de3-392">12,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-392">12,000.00</span></span>          |                     |
        | <span data-ttu-id="d0de3-393">販売 - 完成品</span><span class="sxs-lookup"><span data-stu-id="d0de3-393">Sales - Finished Goods</span></span> |                    | <span data-ttu-id="d0de3-394">12,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-394">12,000.00</span></span>           |

    5. <span data-ttu-id="d0de3-395">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-395">Select **Tax document**.</span></span>
    6. <span data-ttu-id="d0de3-396">**免税** オプションに **はい** をセットします。</span><span class="sxs-lookup"><span data-stu-id="d0de3-396">Verify that the **Exempt** option is set to **Yes**.</span></span>

### <a name="scenario-5-return-the-transaction-that-has-gst"></a><span data-ttu-id="d0de3-397">シナリオ5: GST を含む取引の返品:</span><span class="sxs-lookup"><span data-stu-id="d0de3-397">Scenario 5: Return the transaction that has GST:</span></span>

1. <span data-ttu-id="d0de3-398">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="d0de3-398">Sign in to the POS.</span></span>
2. <span data-ttu-id="d0de3-399">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-399">Select **Show journal**.</span></span>
3. <span data-ttu-id="d0de3-400">取引を選択してから、**返品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-400">Select the transaction, and then select **Return**.</span></span>
4. <span data-ttu-id="d0de3-401">**すべて選択** および **返品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-401">Select **Select all** and then **Return**.</span></span>
5. <span data-ttu-id="d0de3-402">返品する必要がある選択されたオリジナルの取引に基づき、GST 計算が正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-402">Verify that the GST calculation is done correctly, based on the selected original transactions that must be returned.</span></span>

    ![POS 返品取引](media/apac-ind-gst-return-trx.png)

6. <span data-ttu-id="d0de3-404">**正確** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-404">Select **Exact**.</span></span>
7. <span data-ttu-id="d0de3-405">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-405">Validate the receipt.</span></span>

    ![レシート例](media/apac-ind-gst-receipt-5.png)

8. <span data-ttu-id="d0de3-407">小売用バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-407">Validate the retail sales invoice in Retail headquarters:</span></span>

    1. <span data-ttu-id="d0de3-408">**小売** \> **小売 IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-408">Go to **Retail** \> **Retail IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="d0de3-409">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="d0de3-409">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="d0de3-410">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d0de3-410">Close the page.</span></span>

9. <span data-ttu-id="d0de3-411">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="d0de3-411">Post the statement:</span></span>

    1. <span data-ttu-id="d0de3-412">**小売** \> **チャネル** \> **小売店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-412">Go to **Retail** \> **Channels** \> **Retail stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="d0de3-413">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-413">Create a statement.</span></span>
    3. <span data-ttu-id="d0de3-414">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-414">Select **Calculate statement** and then **Post statement**.</span></span>

10. <span data-ttu-id="d0de3-415">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="d0de3-415">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="d0de3-416">**小売** \> **顧客** \> **すべての販売注文** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-416">Go to **Retail** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="d0de3-417">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-417">Select the sales invoice.</span></span>
    3. <span data-ttu-id="d0de3-418">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-418">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="d0de3-419">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-419">Select **Voucher**.</span></span>

        | <span data-ttu-id="d0de3-420">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="d0de3-420">Ledger account name</span></span>  | <span data-ttu-id="d0de3-421">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-421">Debit amount (Rs.)</span></span> | <span data-ttu-id="d0de3-422">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="d0de3-422">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="d0de3-423">顧客口座</span><span class="sxs-lookup"><span data-stu-id="d0de3-423">Customer account</span></span>     |                    | <span data-ttu-id="d0de3-424">12,500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-424">12,500.00</span></span>           |
        | <span data-ttu-id="d0de3-425">IGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-425">IGST payable account</span></span> | <span data-ttu-id="d0de3-426">2,500.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-426">2,500.00</span></span>           |                     |
        | <span data-ttu-id="d0de3-427">売上勘定</span><span class="sxs-lookup"><span data-stu-id="d0de3-427">Sales account</span></span>        | <span data-ttu-id="d0de3-428">10,000.00</span><span class="sxs-lookup"><span data-stu-id="d0de3-428">10,000.00</span></span>          |                     |

    5. <span data-ttu-id="d0de3-429">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-429">Select **Tax document**.</span></span>
    6. <span data-ttu-id="d0de3-430">返品領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0de3-430">Verify that the return receipt number is updated as the transaction ID.</span></span>
