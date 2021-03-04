---
title: インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合
description: このトピックでは、インドで使用可能なキャッシュ レジスター機能の概要を示します。 また、機能を設定するためのガイドラインを示します。
author: EvgenyPopovMBS
manager: annbe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.region: India
ms.search.industry: Retail
ms.author: epopov
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: 7.3.1
ms.openlocfilehash: 42f106078dac64d7b00977e22ae4dd8ebb767f75
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972824"
---
# <a name="goods-and-services-tax-gst-integration-for-cash-registers-for-india"></a><span data-ttu-id="48835-104">インド向けキャッシュ レジスターの商品及びサービス税 (GST) 統合</span><span class="sxs-lookup"><span data-stu-id="48835-104">Goods and Services Tax (GST) integration for cash registers for India</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="48835-105">このトピックでは、関連するフィーチャのチュートリアルを提供します。</span><span class="sxs-lookup"><span data-stu-id="48835-105">This topic provides a walkthrough of the features that are related to Goods and Services Tax (GST).</span></span> <span data-ttu-id="48835-106">また、さまざまな種類のコマース業務取引に対する GST の影響をハイライトして、レシートが販売時点管理 (POS) で印刷される小売り取引の会計および転記を示します。</span><span class="sxs-lookup"><span data-stu-id="48835-106">It also highlights the effect of GST on various types of commerce business transactions, and shows the accounting and posting of transactions where the receipt is printed at the point of sale (POS).</span></span>


## <a name="prerequisites"></a><span data-ttu-id="48835-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="48835-107">Prerequisites</span></span>

- <span data-ttu-id="48835-108">インドの GST を設定します。</span><span class="sxs-lookup"><span data-stu-id="48835-108">Set up GST for India.</span></span> <span data-ttu-id="48835-109">詳細については、[インドの商品及びサービス税 (GST)](../../financials/localizations/apac-ind-gst.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48835-109">For more information, see [India Goods and Services Tax (GST)](../../financials/localizations/apac-ind-gst.md).</span></span>
- <span data-ttu-id="48835-110">コマース チャネル コンポーネントを構成します。</span><span class="sxs-lookup"><span data-stu-id="48835-110">Configure Commerce channel components.</span></span> <span data-ttu-id="48835-111">インド固有の機能を有効にするには、チャネル コンポーネントの拡張機能を構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-111">To enable India-specific functionality, you must configure extensions for channel components.</span></span> <span data-ttu-id="48835-112">詳細については、[配置ガイドライン](./apac-ind-loc-deployment-guidelines.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48835-112">For more information, see the [deployment guidelines](./apac-ind-loc-deployment-guidelines.md).</span></span>

## <a name="india-tax-entities-for-commerce"></a><span data-ttu-id="48835-113">コマース向けインドの税エンティティ</span><span class="sxs-lookup"><span data-stu-id="48835-113">India tax entities for Commerce</span></span>

<span data-ttu-id="48835-114">次の表は、コマースでのインドの税エンティティ用ナビゲーション パスを示します。</span><span class="sxs-lookup"><span data-stu-id="48835-114">The following table shows the navigation paths for the India tax entities in Commerce.</span></span>

| <span data-ttu-id="48835-115">インドの税エンティティ</span><span class="sxs-lookup"><span data-stu-id="48835-115">India tax entities</span></span>                  | <span data-ttu-id="48835-116">コマースでのナビゲーション パス</span><span class="sxs-lookup"><span data-stu-id="48835-116">Navigation path in Commerce</span></span>                                                     |
|-------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="48835-117">ビジネス業種</span><span class="sxs-lookup"><span data-stu-id="48835-117">Business verticals</span></span>                  | <span data-ttu-id="48835-118">小売とコマース \> チャネル設定 \> 売上税 \> ビジネス業種</span><span class="sxs-lookup"><span data-stu-id="48835-118">Retail and Commerce \> Channel setup \> Sales taxes \> Business verticals</span></span>                  |
| <span data-ttu-id="48835-119">エンタープライズ税登録番号</span><span class="sxs-lookup"><span data-stu-id="48835-119">Enterprise tax registration numbers</span></span> | <span data-ttu-id="48835-120">小売とコマース \> チャネル設定 \> 売上税 \> エンタープライズ税登録番号</span><span class="sxs-lookup"><span data-stu-id="48835-120">Retail and Commerce \> Channel setup \> Sales taxes \> Enterprise tax registration numbers</span></span> |
| <span data-ttu-id="48835-121">GST 参照番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="48835-121">GST reference number sequence group</span></span> | <span data-ttu-id="48835-122">小売とコマース \> チャネル設定 \> 売上税 \> GST 参照番号順序グループ</span><span class="sxs-lookup"><span data-stu-id="48835-122">Retail and Commerce \> Channel setup \> Sales taxes \> GST reference number sequence group</span></span> |
| <span data-ttu-id="48835-123">HSN コード</span><span class="sxs-lookup"><span data-stu-id="48835-123">HSN codes</span></span>                           | <span data-ttu-id="48835-124">小売とコマース \> チャネル設定 \> 売上税 \> HSN コード </span><span class="sxs-lookup"><span data-stu-id="48835-124">Retail and Commerce \> Channel setup \> Sales taxes \> HSN codes</span></span>                           |
| <span data-ttu-id="48835-125">サービス アカウント コード</span><span class="sxs-lookup"><span data-stu-id="48835-125">Service accounting codes</span></span>            | <span data-ttu-id="48835-126">小売とコマース \> チャネル設定 \> 売上税 \> サービス アカウント コード</span><span class="sxs-lookup"><span data-stu-id="48835-126">Retail and Commerce \> Channel setup \> Sales taxes \> Service accounting codes</span></span>            |
| <span data-ttu-id="48835-127">相殺階層プロファイルを管理する</span><span class="sxs-lookup"><span data-stu-id="48835-127">Maintain setoff hierarchy profiles</span></span>  | <span data-ttu-id="48835-128">小売とコマース \> チャネル設定 \> 売上税 \> 相殺階層プロファイルを管理する</span><span class="sxs-lookup"><span data-stu-id="48835-128">Retail and Commerce \> Channel setup \> Sales taxes \> Maintain setoff hierarchy profiles</span></span>  |
| <span data-ttu-id="48835-129">VAT スケジュール</span><span class="sxs-lookup"><span data-stu-id="48835-129">VAT schedules</span></span>                       | <span data-ttu-id="48835-130">小売とコマース \> チャネル設定 \> 売上税 \> VAT スケジュール </span><span class="sxs-lookup"><span data-stu-id="48835-130">Retail and Commerce \> Channel setup \> Sales taxes \> VAT schedules</span></span>                       |
| <span data-ttu-id="48835-131">税設定</span><span class="sxs-lookup"><span data-stu-id="48835-131">Tax setup</span></span>                           | <span data-ttu-id="48835-132">小売とコマース \> チャネル設定 \> 売上税 \> 税コンフィギュレーション \> 税設定</span><span class="sxs-lookup"><span data-stu-id="48835-132">Retail and Commerce \> Channel setup \> Sales taxes \> Tax configuration \> Tax setup</span></span>      |

> [!NOTE]
> <span data-ttu-id="48835-133">コマースでのインドの税エンティティ用ナビゲーション パスは、Finance でのナビゲーション パスと異なります。</span><span class="sxs-lookup"><span data-stu-id="48835-133">The navigation paths for the India tax entities in Commerce differ from the navigations paths in Finance.</span></span> <span data-ttu-id="48835-134">Finance のナビゲーション パスの詳細については、[インドの商品及びサービス税 (GST)](../../financials/localizations/apac-ind-gst.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48835-134">For information about the navigation paths in Finance, see [India Goods and Services Tax (GST)](../../financials/localizations/apac-ind-gst.md).</span></span>

## <a name="validate-tax-information-for-the-store"></a><span data-ttu-id="48835-135">店舗の税情報の検証</span><span class="sxs-lookup"><span data-stu-id="48835-135">Validate tax information for the store</span></span>

<span data-ttu-id="48835-136">店舗の税情報は、選択した倉庫から取得されます。</span><span class="sxs-lookup"><span data-stu-id="48835-136">The tax information for the store comes from the selected warehouse.</span></span> <span data-ttu-id="48835-137">この倉庫は倉庫マスターで定義されます。</span><span class="sxs-lookup"><span data-stu-id="48835-137">This warehouse is defined in the warehouse master.</span></span> <span data-ttu-id="48835-138">店舗からの構成済み税情報は POS レシートに印刷されます。</span><span class="sxs-lookup"><span data-stu-id="48835-138">The configured tax information from the store is printed on the POS receipt.</span></span> <span data-ttu-id="48835-139">また、財務転記のためにバック オフィスの販売注文で更新されます。</span><span class="sxs-lookup"><span data-stu-id="48835-139">It's also updated on the sales order at the headquarters for the financial postings.</span></span>

<span data-ttu-id="48835-140">以下の手順に従い、店舗の税情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="48835-140">Follow these steps to view the tax information for a store.</span></span>

1. <span data-ttu-id="48835-141">**小売とコマース** \> **チャネル** \> **店舗** \> **すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-141">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **All stores**.</span></span>
2. <span data-ttu-id="48835-142">店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-142">Select a store.</span></span>
3. <span data-ttu-id="48835-143">**税金情報** クイックタブを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-143">Select the **Tax information** FastTab.</span></span>

## <a name="configure-language-texts-and-custom-fields"></a><span data-ttu-id="48835-144">言語テキストおよびカスタム フィールドのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="48835-144">Configure language texts and custom fields</span></span>

<span data-ttu-id="48835-145">POS レシート形式で使用される言語テキストおよびカスタム フィールドを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="48835-145">You can configure the language text and custom fields that are used in the POS receipt formats.</span></span> <span data-ttu-id="48835-146">レシート設定を作成するユーザーの既定の会社は、言語テキスト設定が作成された法人と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-146">The default company of the user who creates the receipt setup should be the same as the legal entity where the language text setup is created.</span></span> <span data-ttu-id="48835-147">または、ユーザーの既定の会社、および設定の作成対象の店舗の法人の両方で、同じ言語テキストを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-147">Alternatively, the same language texts should be created in both the user's default company and the legal entity of the store that the setup is created for.</span></span>

### <a name="set-up-the-pos-language-text"></a><span data-ttu-id="48835-148">POS 言語テキストの設定</span><span class="sxs-lookup"><span data-stu-id="48835-148">Set up the POS language text</span></span>

1. <span data-ttu-id="48835-149">**小売とコマース** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **言語テキスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-149">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Language text**.</span></span>
2. <span data-ttu-id="48835-150">**POS** タブの、**POS 言語テキスト** クイックタブで、テキストの言語 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-150">On the **POS** tab, on the **POS language text** FastTab, select the language ID for the text.</span></span> <span data-ttu-id="48835-151">言語はユーザーの優先言語と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-151">The language should match the user's preferred language.</span></span>
3. <span data-ttu-id="48835-152">**テキスト ID** フィールドに、**900001** 異常の一意の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="48835-152">In the **Text ID** field, enter a unique ID that is equal to or more than **900001**.</span></span>
4. <span data-ttu-id="48835-153">**テキスト** フィールドで、言語テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="48835-153">In the **Text** field, enter the language text.</span></span>

![言語テキスト](media/apac-ind-gst-language-text.png)

### <a name="create-custom-fields"></a><span data-ttu-id="48835-155">カスタム フィールドの作成</span><span class="sxs-lookup"><span data-stu-id="48835-155">Create custom fields</span></span>

<span data-ttu-id="48835-156">カスタム フィールドを作成するときは、**キャプション テキスト ID** フィールドの値が、**言語テキスト** ページの **テキスト ID** フィールドに入力した値と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-156">When you create custom fields, the value of the **Caption text ID** field must match the value that you entered for the **Text ID** field on the **Language text** page.</span></span>

1. <span data-ttu-id="48835-157">**小売とコマース** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **カスタム フィールド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-157">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Custom fields**.</span></span>
2. <span data-ttu-id="48835-158">フィールドの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="48835-158">Enter a name for the field.</span></span>
3. <span data-ttu-id="48835-159">フィールド タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-159">Select the field type.</span></span>
4. <span data-ttu-id="48835-160">**キャプション テキスト ID** フィールドで、**言語テキスト** ページの言語テキストのいずれかに **テキスト ID** 値を入力します。</span><span class="sxs-lookup"><span data-stu-id="48835-160">In the **Caption text ID** field, enter the **Text ID** value for one of the language texts on the **Language text** page.</span></span>

![カスタム フィールド](media/apac-ind-gst-custom-fields.png)

## <a name="create-the-receipt-format"></a><span data-ttu-id="48835-162">受領書フォーマットの作成</span><span class="sxs-lookup"><span data-stu-id="48835-162">Create the receipt format</span></span>

<span data-ttu-id="48835-163">受領書フォーマット デザイナーを使用して、適切な領収書セクションにカスタム フィールドを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="48835-163">You can use Receipt format designer to add custom fields to the appropriate receipt sections.</span></span> <span data-ttu-id="48835-164">詳細については、[受領書フォーマットの設定しデザインします](../receipt-templates-printing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="48835-164">For more information, see [Set up and design receipt formats](../receipt-templates-printing.md).</span></span>

1. <span data-ttu-id="48835-165">**小売とコマース** \> **チャネル設定** \> **POS 設定** \> **POS プロファイル** \> **受領書フォーマット** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-165">Go to **Retail and Commerce** \> **Channel setup** \> **POS setup** \> **POS profile** \> **Receipt formats**.</span></span>
2. <span data-ttu-id="48835-166">**レシート** 領収書タイプのために領収書書式を選択して、必要な変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="48835-166">Select a receipt format for the **Receipt** receipt type, and make the required changes.</span></span>

![受領書フォーマットのデザイン](media/apac-ind-gst-receipt-format.png)

## <a name="update-receipt-profiles"></a><span data-ttu-id="48835-168">領収書プロファイルの更新</span><span class="sxs-lookup"><span data-stu-id="48835-168">Update receipt profiles</span></span>

<span data-ttu-id="48835-169">領収書フォーマットの作成すると、領収書プロファイルにフォーマットを割当てることができます。</span><span class="sxs-lookup"><span data-stu-id="48835-169">After you create a receipt format, you can assign that format to a receipt profile.</span></span>

<span data-ttu-id="48835-170">以下の手順を実行して、領収書プロファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="48835-170">Follow these steps to update a receipt profile.</span></span>

1. <span data-ttu-id="48835-171">**小売とコマース** \> **設定** \> **POS** \> **レシート プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-171">Go to **Retail and Commerce** \> **Setup** \> **POS** \> **Receipt profile**.</span></span>
2. <span data-ttu-id="48835-172">更新するレシート プロファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-172">Select the receipt profile to update.</span></span>
3. <span data-ttu-id="48835-173">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-173">Select **Edit**.</span></span>
4. <span data-ttu-id="48835-174">リスト内のレシート タイプごとに、受領書フォーマットを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-174">For each receipt type in the list, select a receipt format.</span></span>

## <a name="update-the-pos-invoice-number"></a><span data-ttu-id="48835-175">POS 請求書番号の更新</span><span class="sxs-lookup"><span data-stu-id="48835-175">Update the POS invoice number</span></span>

<span data-ttu-id="48835-176">顧客の取引の請求書番号を使用して POS レシート番号を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="48835-176">You can reconcile the POS receipt number with the invoice number for customer transactions.</span></span> <span data-ttu-id="48835-177">**コマースパラメータ** ページの **転記** タブで **POS 請求書番号を更新** オプションに **はい** をセットする場合、対応する販売注文の **取引 ID** フィールドに POS 請求書番号が入力されます。</span><span class="sxs-lookup"><span data-stu-id="48835-177">If you set the **Update POS invoice number** option to **Yes** on the **Posting** tab of the **Commerce parameters** page, the POS receipt number is entered in the **Transaction ID** field for corresponding sales orders.</span></span>

<span data-ttu-id="48835-178">既存の領収書番号書式に店舗番号と端末番号の両方が含まれる場合にのみ、**POS 請求書番号を更新** オプションに **はい** をセットすることができます。 </span><span class="sxs-lookup"><span data-stu-id="48835-178">You can set the **Update POS invoice number** option to **Yes** only if the existing receipt number format includes both the store number and the terminal number.</span></span> <span data-ttu-id="48835-179">次の図は、レシート番号付けに店舗番号と端末番号が含まれる、POS 機能プロファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="48835-179">The following illustration shows a POS functionality profile where the receipt numbering includes the store number and the terminal number.</span></span>

![POS 機能プロファイル](media/apac-ind-gst-pos-functionality-profile.png)

## <a name="run-a-distribution-schedule"></a><span data-ttu-id="48835-181">配送スケジュールの実行</span><span class="sxs-lookup"><span data-stu-id="48835-181">Run a distribution schedule</span></span>

<span data-ttu-id="48835-182">バックオフィスからの税エンジン (GTE) データを POS データベースに同期させるには、**配送スケジュール** ページにジョブを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-182">To synchronize Tax Engine (GTE) data from headquarter to the POS database, you must add a job to the **Distribution schedule** page.</span></span>

<span data-ttu-id="48835-183">以下の手順に従い、ジョブが存在していることを検証して、ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="48835-183">Follow these steps to verify that the job exists and to run the job.</span></span>

1. <span data-ttu-id="48835-184">**小売とコマース** \> **定期処理** \> **データ配送** \> **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-184">Go to **Retail and Commerce** \> **Periodic** \> **Data distribution** \> **Distribution schedule**.</span></span>
2. <span data-ttu-id="48835-185">新しいジョブ、**1180** が **汎用税エンジン** のために追加されていることを検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-185">Verify that a new job, **1180**, has been added for **Generic tax engine**.</span></span>
3. <span data-ttu-id="48835-186">すべてのジョブを実行します (**9999**)。</span><span class="sxs-lookup"><span data-stu-id="48835-186">Run all the jobs (**9999**).</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="48835-187">シナリオ例</span><span class="sxs-lookup"><span data-stu-id="48835-187">Example scenarios</span></span>

<span data-ttu-id="48835-188">次のシナリオ例はインドの取引サンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="48835-188">The following example scenarios walk you through sample transactions for India:</span></span>

- <span data-ttu-id="48835-189">シナリオ 1: 登録済の顧客に対する販売</span><span class="sxs-lookup"><span data-stu-id="48835-189">Scenario 1: Sell to a registered customer</span></span>
- <span data-ttu-id="48835-190">シナリオ 2: 顧客に対する課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-190">Scenario 2: Sell taxable goods to a consumer</span></span>
- <span data-ttu-id="48835-191">シナリオ 3: GSTが価格に包まれる、匿名の顧客への課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-191">Scenario 3: Sell taxable goods to an anonymous customer where GST is price-inclusive</span></span>
- <span data-ttu-id="48835-192">シナリオ 4: 免税品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-192">Scenario 4: Sell an exempted good</span></span>
- <span data-ttu-id="48835-193">シナリオ 5: GST を含む取引の返品</span><span class="sxs-lookup"><span data-stu-id="48835-193">Scenario 5: Return the transaction that has GST</span></span>

### <a name="scenario-1-sell-to-a-registered-customer"></a><span data-ttu-id="48835-194">シナリオ 1: 登録済の顧客に対する販売</span><span class="sxs-lookup"><span data-stu-id="48835-194">Scenario 1: Sell to a registered customer</span></span>

<span data-ttu-id="48835-195">登録済み顧客への販売は *企業間* (B2B) 販売と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="48835-195">Sales to a registered customer are known as *business-to-business* (B2B) sales.</span></span> <span data-ttu-id="48835-196">店舗の場所と供給の位置 (つまり、顧客の住所) が同じ州にある場合、取引は *イントラスタット販売* で、中央 GST (CGST) および州 GST (SGST) が支払われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-196">If the store location and the place of supply (that is, the customer address) are in the same state, the transaction is an *intrastate sale*, and Central GST (CGST) and State GST (SGST) must be paid.</span></span> <span data-ttu-id="48835-197">店舗の場所および供給の位置が異なる州にある場所、取引は *州間販売* で、統合された GST (IGST) が支払われる必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-197">If the store location and the place of supply are in different states, the transaction is an *interstate sale*, and Integrated GST (IGST) must be paid.</span></span>

> [!NOTE]
> <span data-ttu-id="48835-198">これらの取引の場合、顧客の住所および登録番号のフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="48835-198">For these transactions, the fields for the customer address and the registration number are required.</span></span>

1. <span data-ttu-id="48835-199">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-199">Sign in to the POS.</span></span>
2. <span data-ttu-id="48835-200">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-200">Enter the items, and then select **Enter**.</span></span>

    ![POS の顧客注文画面の「アクション」が選択されている](media/apac-ind-gst-pos-customer-order.png)

3. <span data-ttu-id="48835-202">GST 計算を検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-202">Validate the GST calculations.</span></span> <span data-ttu-id="48835-203">税の設定で定義されているレートを検討します。</span><span class="sxs-lookup"><span data-stu-id="48835-203">Consider the rate that is defined in the tax setup.</span></span>

    | <span data-ttu-id="48835-204">品目/サービス</span><span class="sxs-lookup"><span data-stu-id="48835-204">Item/service</span></span> | <span data-ttu-id="48835-205">単価</span><span class="sxs-lookup"><span data-stu-id="48835-205">Unit price</span></span> | <span data-ttu-id="48835-206">税率</span><span class="sxs-lookup"><span data-stu-id="48835-206">Tax rates</span></span>          | <span data-ttu-id="48835-207">CGST</span><span class="sxs-lookup"><span data-stu-id="48835-207">CGST</span></span>     | <span data-ttu-id="48835-208">SGST</span><span class="sxs-lookup"><span data-stu-id="48835-208">SGST</span></span>      |
    |--------------|------------|--------------------|----------|-----------|
    | <span data-ttu-id="48835-209">M0001</span><span class="sxs-lookup"><span data-stu-id="48835-209">M0001</span></span>        | <span data-ttu-id="48835-210">10,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-210">10,000.00</span></span>  | <span data-ttu-id="48835-211">CGST 12%、SGST 11%</span><span class="sxs-lookup"><span data-stu-id="48835-211">CGST 12%, SGST 11%</span></span> | <span data-ttu-id="48835-212">1,200.00</span><span class="sxs-lookup"><span data-stu-id="48835-212">1,200.00</span></span> | <span data-ttu-id="48835-213">1,100.00</span><span class="sxs-lookup"><span data-stu-id="48835-213">1,100.00</span></span>  |
    | <span data-ttu-id="48835-214">M0002</span><span class="sxs-lookup"><span data-stu-id="48835-214">M0002</span></span>        | <span data-ttu-id="48835-215">5,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-215">5,000.00</span></span>   | <span data-ttu-id="48835-216">CGST 10%、SGST 10%</span><span class="sxs-lookup"><span data-stu-id="48835-216">CGST 10%, SGST 10%</span></span> | <span data-ttu-id="48835-217">500.00</span><span class="sxs-lookup"><span data-stu-id="48835-217">500.00</span></span>   | <span data-ttu-id="48835-218">500.00</span><span class="sxs-lookup"><span data-stu-id="48835-218">500.00</span></span>    |
    | <span data-ttu-id="48835-219">S0001</span><span class="sxs-lookup"><span data-stu-id="48835-219">S0001</span></span>        | <span data-ttu-id="48835-220">1,200.00</span><span class="sxs-lookup"><span data-stu-id="48835-220">1,200.00</span></span>   | <span data-ttu-id="48835-221">CGST 11%、SGST 5%</span><span class="sxs-lookup"><span data-stu-id="48835-221">CGST 11%, SGST 5%</span></span>  | <span data-ttu-id="48835-222">132.00</span><span class="sxs-lookup"><span data-stu-id="48835-222">132.00</span></span>   | <span data-ttu-id="48835-223">60.00</span><span class="sxs-lookup"><span data-stu-id="48835-223">60.00</span></span>     |
    |              | <span data-ttu-id="48835-224">16,200.00</span><span class="sxs-lookup"><span data-stu-id="48835-224">16,200.00</span></span>  |                    | <span data-ttu-id="48835-225">1,832.00</span><span class="sxs-lookup"><span data-stu-id="48835-225">1,832.00</span></span> | <span data-ttu-id="48835-226">1,660.00</span><span class="sxs-lookup"><span data-stu-id="48835-226">1,660.00</span></span>  |
    | <span data-ttu-id="48835-227">合計金額</span><span class="sxs-lookup"><span data-stu-id="48835-227">Total amount</span></span> |            |                    |          | <span data-ttu-id="48835-228">19,692.00</span><span class="sxs-lookup"><span data-stu-id="48835-228">19,692.00</span></span> |

4. <span data-ttu-id="48835-229">**注文** \> **顧客注文の作成** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-229">Select **Orders** \> **Create customer order**.</span></span>
5. <span data-ttu-id="48835-230">**顧客の追加** を選択して、顧客アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-230">Select **Add customer**, and select the customer account.</span></span>
6. <span data-ttu-id="48835-231">**すべて集荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-231">Select **Pick up all**.</span></span>
7. <span data-ttu-id="48835-232">店舗および集荷日を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-232">Select the store and the pick-up date.</span></span>
8. <span data-ttu-id="48835-233">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-233">Select **OK**.</span></span>

    ![POS の顧客注文画面の「注文」が選択されている](./media/apac-ind-gst-pos-customer-order2.png)

    > [!NOTE]
    > <span data-ttu-id="48835-235">この例では、店舗場所の州が Delhi で、顧客住所の州も Delhi です。</span><span class="sxs-lookup"><span data-stu-id="48835-235">In this example, the state of the store location is Delhi, and the state of the customer address is also Delhi.</span></span> <span data-ttu-id="48835-236">州が同じであるため、イントラスタット GST が計算されます。</span><span class="sxs-lookup"><span data-stu-id="48835-236">Because the state is the same, intrastate GST is calculated.</span></span>

9. <span data-ttu-id="48835-237">**正確** を選択して預金支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="48835-237">Select **Exact** to process the deposit payment.</span></span>
10. <span data-ttu-id="48835-238">領収書の検証:</span><span class="sxs-lookup"><span data-stu-id="48835-238">Validate the receipt:</span></span>

    1. <span data-ttu-id="48835-239">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-239">Select **Show journal**.</span></span>
    2. <span data-ttu-id="48835-240">取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-240">Select the transactions.</span></span>
    3. <span data-ttu-id="48835-241">**レシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-241">Select **Receipt**.</span></span>

    ![シナリオ 1 一番目の検証レシートの例](media/apac-ind-gst-s1-receipt1.png)

11. <span data-ttu-id="48835-243">バックオフィスで販売注文および税ドキュメントを検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-243">Validate the sales order and tax document in Headquarters:</span></span>

    1. <span data-ttu-id="48835-244">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-244">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-245">販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-245">Select the sales order.</span></span>
    3. <span data-ttu-id="48835-246">アクション ペインの、**販売** タブの、**税** グループで、**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-246">On the Action Pane, on the **Sell** tab, in the **Tax** group, select **Tax document**.</span></span>

    ![税務書類ページ](media/apac-ind-gst-tax-document.png)

12. <span data-ttu-id="48835-248">顧客の注文を取り消して処理します:</span><span class="sxs-lookup"><span data-stu-id="48835-248">Recall and process the customer order:</span></span>

    1. <span data-ttu-id="48835-249">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-249">Sign in to the POS.</span></span>
    2. <span data-ttu-id="48835-250">**注文の取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-250">Select **Recall order**.</span></span>
    3. <span data-ttu-id="48835-251">注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-251">Search for and select the order.</span></span>
    4. <span data-ttu-id="48835-252">**ピッキングと梱包** \> **集荷** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-252">Select **Picking and packing** \> **Pickup**</span></span>
    5. <span data-ttu-id="48835-253">**すべて選択** および **集荷** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-253">Select **Select all** and then **Pickup**.</span></span>

    ![顧客注文の処理](media/apac-ind-gst-process-customer-order.png)

13. <span data-ttu-id="48835-255">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="48835-255">Select **Exact** to process the payment.</span></span>
14. <span data-ttu-id="48835-256">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-256">Validate the receipt.</span></span>

    ![シナリオ 1 二番目の検証レシートの例](media/apac-ind-gst-s1-receipt2.png)

15. <span data-ttu-id="48835-258">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-258">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="48835-259">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-259">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-260">販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-260">Select the sales order.</span></span>
    3. <span data-ttu-id="48835-261">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-261">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="48835-262">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-262">Select **Voucher**.</span></span>

        | <span data-ttu-id="48835-263">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="48835-263">Ledger account name</span></span>  | <span data-ttu-id="48835-264">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-264">Debit amount (Rs.)</span></span> | <span data-ttu-id="48835-265">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-265">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="48835-266">顧客口座</span><span class="sxs-lookup"><span data-stu-id="48835-266">Customer account</span></span>     | <span data-ttu-id="48835-267">19,692.00</span><span class="sxs-lookup"><span data-stu-id="48835-267">19,692.00</span></span>          |                     |
        | <span data-ttu-id="48835-268">CGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-268">CGST payable account</span></span> |                    | <span data-ttu-id="48835-269">1,832.00</span><span class="sxs-lookup"><span data-stu-id="48835-269">1,832.00</span></span>            |
        | <span data-ttu-id="48835-270">SGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-270">SGST payable account</span></span> |                    | <span data-ttu-id="48835-271">1,660.00</span><span class="sxs-lookup"><span data-stu-id="48835-271">1,660.00</span></span>            |
        | <span data-ttu-id="48835-272">売上勘定</span><span class="sxs-lookup"><span data-stu-id="48835-272">Sales account</span></span>        |                    | <span data-ttu-id="48835-273">16,200.00</span><span class="sxs-lookup"><span data-stu-id="48835-273">16,200.00</span></span>           |

    5. <span data-ttu-id="48835-274">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-274">Select **Tax document**.</span></span>
    6. <span data-ttu-id="48835-275">領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-275">Verify that the receipt number is updated as the transaction ID.</span></span>

        ![「トランザクション ID」フィールドが選択された税務書類ページ](media/apac-ind-gst-tax-document2.png)

### <a name="scenario-2-sell-taxable-goods-to-a-consumer"></a><span data-ttu-id="48835-277">シナリオ 2: 顧客に対する課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-277">Scenario 2: Sell taxable goods to a consumer</span></span>

<span data-ttu-id="48835-278">未登録の顧客に販売するとき、その販売は *企業と顧客間* (B2C) 販売と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="48835-278">When you sell to unregistered customers, the sales are referred to as *business-to-consumer* (B2C) sales.</span></span> <span data-ttu-id="48835-279">税は B2B および B2C 販売と同じ方法で計算されます。</span><span class="sxs-lookup"><span data-stu-id="48835-279">Tax is calculated in the same manner for B2B and B2C sales.</span></span>

1. <span data-ttu-id="48835-280">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-280">Sign in to the POS.</span></span>
2. <span data-ttu-id="48835-281">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-281">Enter an item, and then select **Enter**.</span></span>
3. <span data-ttu-id="48835-282">**顧客の追加** を選択して、顧客アカウントを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-282">Select **Add customer**, and select the customer account.</span></span>

    ![取引の例](media/apac-ind-gst-example-trx.png)

    > [!NOTE]
    > <span data-ttu-id="48835-284">この例では、店舗場所の州は Delhi ですが、顧客住所の州は Bengaluru (Bangalore) です。</span><span class="sxs-lookup"><span data-stu-id="48835-284">In this example, the state of the store location is Delhi, but the state of the customer address is Bengaluru (Bangalore).</span></span> <span data-ttu-id="48835-285">州が異なるため、州間 GST が計算されます。</span><span class="sxs-lookup"><span data-stu-id="48835-285">Because the states differ, interstate GST is computed.</span></span>

4. <span data-ttu-id="48835-286">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="48835-286">Select **Exact** to process the payment.</span></span>
5. <span data-ttu-id="48835-287">領収書の検証:</span><span class="sxs-lookup"><span data-stu-id="48835-287">Validate the receipt:</span></span>

    1. <span data-ttu-id="48835-288">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-288">Select **Show journal**.</span></span>
    2. <span data-ttu-id="48835-289">取引を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-289">Select the transactions.</span></span>
    3. <span data-ttu-id="48835-290">**レシート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-290">Select **Receipt**.</span></span>

    ![領収書の検証](media/apac-ind-gst-receipt-validation.png)

6. <span data-ttu-id="48835-292">バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="48835-292">Validate the sales invoice in Headquarters:</span></span>

    1. <span data-ttu-id="48835-293">**小売とコマース** \> **小売とコマース IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-293">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="48835-294">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="48835-294">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="48835-295">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48835-295">Close the page.</span></span>

7. <span data-ttu-id="48835-296">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="48835-296">Post the statement:</span></span>

    1. <span data-ttu-id="48835-297">**小売とコマース** \> **チャネル** \> **店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-297">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="48835-298">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="48835-298">Create a statement.</span></span>
    3. <span data-ttu-id="48835-299">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-299">Select **Calculate statement** and then **Post statement**.</span></span>

8. <span data-ttu-id="48835-300">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-300">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="48835-301">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-301">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-302">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-302">Select the sales invoice.</span></span>
    3. <span data-ttu-id="48835-303">**販売注文行** \> **税金情報** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-303">Select **Sales order lines** \> **Tax information**.</span></span>
    4. <span data-ttu-id="48835-304">該当するタブで、場所 (店舗アドレス) および顧客の住所を確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-304">On the appropriate tabs, verify the location (store address) and the customer address.</span></span>

        ![税金情報](media/apac-ind-gst-tax-info.png)

    5. <span data-ttu-id="48835-306">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-306">Select **OK**.</span></span>
    6. <span data-ttu-id="48835-307">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-307">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    7. <span data-ttu-id="48835-308">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-308">Select **Voucher**.</span></span>

        | <span data-ttu-id="48835-309">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="48835-309">Ledger account name</span></span>  | <span data-ttu-id="48835-310">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-310">Debit amount (Rs.)</span></span> | <span data-ttu-id="48835-311">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-311">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="48835-312">顧客口座</span><span class="sxs-lookup"><span data-stu-id="48835-312">Customer account</span></span>     | <span data-ttu-id="48835-313">12,500.00</span><span class="sxs-lookup"><span data-stu-id="48835-313">12,500.00</span></span>          |                     |
        | <span data-ttu-id="48835-314">IGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-314">IGST payable account</span></span> |                    | <span data-ttu-id="48835-315">2,500.00</span><span class="sxs-lookup"><span data-stu-id="48835-315">2,500.00</span></span>            |
        | <span data-ttu-id="48835-316">売上勘定</span><span class="sxs-lookup"><span data-stu-id="48835-316">Sales account</span></span>        |                    | <span data-ttu-id="48835-317">10,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-317">10,000.00</span></span>           |

    8. <span data-ttu-id="48835-318">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-318">Select **Tax document**.</span></span>
    9. <span data-ttu-id="48835-319">領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-319">Verify that the receipt number is updated as the transaction ID.</span></span>

### <a name="scenario-3-sell-taxable-goods-to-an-anonymous-customer-where-gst-is-price-inclusive"></a><span data-ttu-id="48835-320">シナリオ 3: GSTが価格に包まれる、匿名の顧客への課税対象商品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-320">Scenario 3: Sell taxable goods to an anonymous customer where GST is price-inclusive</span></span>

1. <span data-ttu-id="48835-321">店舗での価格包含性を定義します。</span><span class="sxs-lookup"><span data-stu-id="48835-321">Define price-inclusiveness at the store:</span></span>

    1. <span data-ttu-id="48835-322">**小売とコマース** \> **チャネル** \> **店舗** \> **すべての店舗** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-322">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **All stores**.</span></span>
    2. <span data-ttu-id="48835-323">店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-323">Select a store.</span></span>
    3. <span data-ttu-id="48835-324">**税込価格** オプションに **はい** をセットします。</span><span class="sxs-lookup"><span data-stu-id="48835-324">Set the **Prices include sales tax** option to **Yes**.</span></span>

2. <span data-ttu-id="48835-325">配送スケジュールを実行します:</span><span class="sxs-lookup"><span data-stu-id="48835-325">Run the distribution schedule:</span></span>

    1. <span data-ttu-id="48835-326">**小売とコマース** \> **小売とコマース IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-326">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="48835-327">POS データベース内の変更を更新するジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="48835-327">Run the job to update the changes in the POS database.</span></span>
    3. <span data-ttu-id="48835-328">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48835-328">Close the page.</span></span>

3. <span data-ttu-id="48835-329">トランザクションの入力:</span><span class="sxs-lookup"><span data-stu-id="48835-329">Enter a transaction:</span></span>

    1. <span data-ttu-id="48835-330">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-330">Sign in to the POS.</span></span>
    2. <span data-ttu-id="48835-331">品目を入力してから、**入力** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-331">Enter an item, and then select **Enter**.</span></span> <span data-ttu-id="48835-332">この例では、次の値を持つ品目を使用します:</span><span class="sxs-lookup"><span data-stu-id="48835-332">For this example, use an item that has the following values:</span></span>

        - <span data-ttu-id="48835-333">**課税対象値:** 10,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-333">**Taxable value:** 10,000.00</span></span>
        - <span data-ttu-id="48835-334">**CGST:** 12 %</span><span class="sxs-lookup"><span data-stu-id="48835-334">**CGST:** 12 percent</span></span>
        - <span data-ttu-id="48835-335">**SGST:** 11 %</span><span class="sxs-lookup"><span data-stu-id="48835-335">**SGST:** 11 percent</span></span>

    ![取引の例](media/apac-ind-gst-trx-example.png)

4. <span data-ttu-id="48835-337">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="48835-337">Select **Exact** to process the payment.</span></span>
5. <span data-ttu-id="48835-338">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-338">Validate the receipt.</span></span>

    ![シナリオ 3 領収書の例](media/apac-ind-gst-s3-receipt4.png)

6. <span data-ttu-id="48835-340">バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="48835-340">Validate the sales invoice in Headquarters:</span></span>

    1. <span data-ttu-id="48835-341">**小売とコマース** \> **小売とコマース IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-341">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="48835-342">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="48835-342">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="48835-343">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48835-343">Close the page.</span></span>

7. <span data-ttu-id="48835-344">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="48835-344">Post the statement:</span></span>

    1. <span data-ttu-id="48835-345">**小売とコマース** \> **チャネル** \> **店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-345">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="48835-346">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="48835-346">Create a statement.</span></span>
    3. <span data-ttu-id="48835-347">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-347">Select **Calculate statement** and then **Post statement**.</span></span>

8. <span data-ttu-id="48835-348">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-348">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="48835-349">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-349">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-350">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-350">Select the sales invoice.</span></span>
    3. <span data-ttu-id="48835-351">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-351">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="48835-352">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-352">Select **Voucher**.</span></span>

        | <span data-ttu-id="48835-353">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="48835-353">Ledger account name</span></span>  | <span data-ttu-id="48835-354">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-354">Debit amount (Rs.)</span></span> | <span data-ttu-id="48835-355">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-355">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="48835-356">顧客口座</span><span class="sxs-lookup"><span data-stu-id="48835-356">Customer account</span></span>     | <span data-ttu-id="48835-357">10,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-357">10,000.00</span></span>          |                     |
        | <span data-ttu-id="48835-358">CGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-358">CGST payable account</span></span> |                    | <span data-ttu-id="48835-359">975.61</span><span class="sxs-lookup"><span data-stu-id="48835-359">975.61</span></span>              |
        | <span data-ttu-id="48835-360">SGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-360">SGST payable account</span></span> |                    | <span data-ttu-id="48835-361">894.31</span><span class="sxs-lookup"><span data-stu-id="48835-361">894.31</span></span>              |
        | <span data-ttu-id="48835-362">売上勘定</span><span class="sxs-lookup"><span data-stu-id="48835-362">Sales account</span></span>        |                    | <span data-ttu-id="48835-363">8,130.08</span><span class="sxs-lookup"><span data-stu-id="48835-363">8,130.08</span></span>            |

    5. <span data-ttu-id="48835-364">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-364">Select **Tax document**.</span></span>
    6. <span data-ttu-id="48835-365">GST 参照番号順序グループで定義されている GST 番号順序に従って取引 ID が更新されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-365">Verify that the transaction ID is updated according to the GST number sequence that is defined in the GST reference number sequence group.</span></span>

        ![税務書類のトランザクション ID](media/apac-ind-gst-tax-doc-trx-id.png)

### <a name="scenario-4-sell-an-exempted-good"></a><span data-ttu-id="48835-367">シナリオ 4: 免税品の販売</span><span class="sxs-lookup"><span data-stu-id="48835-367">Scenario 4: Sell an exempted good</span></span>

1. <span data-ttu-id="48835-368">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-368">Sign in to the POS.</span></span>
2. <span data-ttu-id="48835-369">免税品目を入力します。</span><span class="sxs-lookup"><span data-stu-id="48835-369">Enter an exempted item.</span></span>

    ![免税品目トランザクション](media/apac-ind-gst-exempted-item-trx.png)

3. <span data-ttu-id="48835-371">**正確** を選択して支払を処理します。</span><span class="sxs-lookup"><span data-stu-id="48835-371">Select **Exact** to process the payment.</span></span>
4. <span data-ttu-id="48835-372">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-372">Validate the receipt.</span></span>

    ![レシート example.png](media/apac-ind-gst-receipt-4.png)

5. <span data-ttu-id="48835-374">バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="48835-374">Validate the sales invoice in Headquarters:</span></span>

    1. <span data-ttu-id="48835-375">**小売とコマース** \> **小売とコマース IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-375">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="48835-376">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="48835-376">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="48835-377">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48835-377">Close the page.</span></span>

6. <span data-ttu-id="48835-378">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="48835-378">Post the statement:</span></span>

    1. <span data-ttu-id="48835-379">**小売とコマース** \> **チャネル** \> **店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-379">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="48835-380">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="48835-380">Create a statement.</span></span>
    3. <span data-ttu-id="48835-381">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-381">Select **Calculate statement** and then **Post statement**.</span></span>

7. <span data-ttu-id="48835-382">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-382">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="48835-383">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-383">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-384">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-384">Select the sales invoice.</span></span>
    3. <span data-ttu-id="48835-385">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-385">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="48835-386">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-386">Select **Voucher**.</span></span>

        | <span data-ttu-id="48835-387">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="48835-387">Ledger account name</span></span>    | <span data-ttu-id="48835-388">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-388">Debit amount (Rs.)</span></span> | <span data-ttu-id="48835-389">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-389">Credit amount (Rs.)</span></span> |
        |------------------------|--------------------|---------------------|
        | <span data-ttu-id="48835-390">顧客口座</span><span class="sxs-lookup"><span data-stu-id="48835-390">Customer account</span></span>       | <span data-ttu-id="48835-391">12,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-391">12,000.00</span></span>          |                     |
        | <span data-ttu-id="48835-392">販売 - 完成品</span><span class="sxs-lookup"><span data-stu-id="48835-392">Sales - Finished Goods</span></span> |                    | <span data-ttu-id="48835-393">12,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-393">12,000.00</span></span>           |

    5. <span data-ttu-id="48835-394">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-394">Select **Tax document**.</span></span>
    6. <span data-ttu-id="48835-395">**免税** オプションに **はい** をセットします。</span><span class="sxs-lookup"><span data-stu-id="48835-395">Verify that the **Exempt** option is set to **Yes**.</span></span>

### <a name="scenario-5-return-the-transaction-that-has-gst"></a><span data-ttu-id="48835-396">シナリオ5: GST を含む取引の返品:</span><span class="sxs-lookup"><span data-stu-id="48835-396">Scenario 5: Return the transaction that has GST:</span></span>

1. <span data-ttu-id="48835-397">POS へのサインイン</span><span class="sxs-lookup"><span data-stu-id="48835-397">Sign in to the POS.</span></span>
2. <span data-ttu-id="48835-398">**仕訳帳の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-398">Select **Show journal**.</span></span>
3. <span data-ttu-id="48835-399">取引を選択してから、**返品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-399">Select the transaction, and then select **Return**.</span></span>
4. <span data-ttu-id="48835-400">**すべて選択** および **返品** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-400">Select **Select all** and then **Return**.</span></span>
5. <span data-ttu-id="48835-401">返品する必要がある選択されたオリジナルの取引に基づき、GST 計算が正常に実行されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-401">Verify that the GST calculation is done correctly, based on the selected original transactions that must be returned.</span></span>

    ![POS 返品取引](media/apac-ind-gst-return-trx.png)

6. <span data-ttu-id="48835-403">**正確** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-403">Select **Exact**.</span></span>
7. <span data-ttu-id="48835-404">領収書を検証します。</span><span class="sxs-lookup"><span data-stu-id="48835-404">Validate the receipt.</span></span>

    ![シナリオ 4 領収書の例](media/apac-ind-gst-receipt-5.png)

8. <span data-ttu-id="48835-406">バックオフィスでの小売販売請求書を確認します:</span><span class="sxs-lookup"><span data-stu-id="48835-406">Validate the sales invoice in Headquarters:</span></span>

    1. <span data-ttu-id="48835-407">**小売とコマース** \> **小売とコマース IT** \> **データ配送** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-407">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Data distribution**.</span></span>
    2. <span data-ttu-id="48835-408">ジョブ **P-0001** を実行します (**チャネル取引**)。</span><span class="sxs-lookup"><span data-stu-id="48835-408">Run job **P-0001** (**Channel transactions**).</span></span>
    3. <span data-ttu-id="48835-409">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="48835-409">Close the page.</span></span>

9. <span data-ttu-id="48835-410">明細書の転記:</span><span class="sxs-lookup"><span data-stu-id="48835-410">Post the statement:</span></span>

    1. <span data-ttu-id="48835-411">**小売とコマース** \> **チャネル** \> **店舗** \> **未処理の明細書** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-411">Go to **Retail and Commerce** \> **Channels** \> **Stores** \> **Open statements**.</span></span>
    2. <span data-ttu-id="48835-412">明細書を作成します。</span><span class="sxs-lookup"><span data-stu-id="48835-412">Create a statement.</span></span>
    3. <span data-ttu-id="48835-413">**明細書の計算** および **明細書の転記** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-413">Select **Calculate statement** and then **Post statement**.</span></span>

10. <span data-ttu-id="48835-414">伝票取引を検証します:</span><span class="sxs-lookup"><span data-stu-id="48835-414">Validate the voucher transactions:</span></span>

    1. <span data-ttu-id="48835-415">**小売とコマース** \> **顧客** \> **すべての販売注文** に移動します。</span><span class="sxs-lookup"><span data-stu-id="48835-415">Go to **Retail and Commerce** \> **Customers** \> **All sales orders**.</span></span>
    2. <span data-ttu-id="48835-416">売上請求書を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-416">Select the sales invoice.</span></span>
    3. <span data-ttu-id="48835-417">アクション ウィンドウの、**請求書** タブで、**請求仕訳帳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-417">On the Action Pane, on the **Invoice** tab, select **Invoice journals**.</span></span>
    4. <span data-ttu-id="48835-418">**伝票** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-418">Select **Voucher**.</span></span>

        | <span data-ttu-id="48835-419">勘定科目名</span><span class="sxs-lookup"><span data-stu-id="48835-419">Ledger account name</span></span>  | <span data-ttu-id="48835-420">借方金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-420">Debit amount (Rs.)</span></span> | <span data-ttu-id="48835-421">クレジット金額 (Rs.)</span><span class="sxs-lookup"><span data-stu-id="48835-421">Credit amount (Rs.)</span></span> |
        |----------------------|--------------------|---------------------|
        | <span data-ttu-id="48835-422">顧客口座</span><span class="sxs-lookup"><span data-stu-id="48835-422">Customer account</span></span>     |                    | <span data-ttu-id="48835-423">12,500.00</span><span class="sxs-lookup"><span data-stu-id="48835-423">12,500.00</span></span>           |
        | <span data-ttu-id="48835-424">IGST 未払勘定</span><span class="sxs-lookup"><span data-stu-id="48835-424">IGST payable account</span></span> | <span data-ttu-id="48835-425">2,500.00</span><span class="sxs-lookup"><span data-stu-id="48835-425">2,500.00</span></span>           |                     |
        | <span data-ttu-id="48835-426">売上勘定</span><span class="sxs-lookup"><span data-stu-id="48835-426">Sales account</span></span>        | <span data-ttu-id="48835-427">10,000.00</span><span class="sxs-lookup"><span data-stu-id="48835-427">10,000.00</span></span>          |                     |

    5. <span data-ttu-id="48835-428">**税務書類** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-428">Select **Tax document**.</span></span>
    6. <span data-ttu-id="48835-429">返品領収書番号が取引 ID として更新されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="48835-429">Verify that the return receipt number is updated as the transaction ID.</span></span>

## <a name="update-credit-notes-with-references-to-original-invoices"></a><span data-ttu-id="48835-430">元の請求書への参照を含む訂正票を更新します</span><span class="sxs-lookup"><span data-stu-id="48835-430">Update credit notes with references to original invoices</span></span>

> [!NOTE]
> <span data-ttu-id="48835-431">この機能は、アプリケーション更新プログラム 10.0.3 以降で使用できます。</span><span class="sxs-lookup"><span data-stu-id="48835-431">This functionality is available with Application update 10.0.3 and later.</span></span>

<span data-ttu-id="48835-432">GSTR レポートに正しく反映されるためには、売上訂正票に元の売上請求書への参照が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="48835-432">In order to be correctly reflected in the GSTR reporting, sales credit notes should contain references to original sales invoices.</span></span> <span data-ttu-id="48835-433">明細書から店舗のトランザクションを転記すると、返品トランザクションに対してこの参照を確立できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="48835-433">When  store transactions are posted through statements, it is not always possible to establish this reference for return transactions.</span></span> <span data-ttu-id="48835-434">**元の請求書に関連する訂正票の更新** 手順を使用して、訂正票の **元の GST トランザクション ID** のリンクを更新し、リンクが関連付けられている元の売上請求書を正しく参照するようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="48835-434">You can use the **Update credit notes with references to original invoices** procedure to update the **Original GST transaction ID** link in credit notes so that the link correctly references the related original sales invoice.</span></span> <span data-ttu-id="48835-435">この手順は、**小売とコマース > 小売とコマース IT > POS の転記** メニューにあります。</span><span class="sxs-lookup"><span data-stu-id="48835-435">The procedure is located on the **Retail and Commerce > Retail and Commerce IT > POS posting** menu.</span></span>

<span data-ttu-id="48835-436">また、**コマース パラメーター** ページの **返品を集計しない** パラメーターを有効にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="48835-436">It is also recommended that you enable the **Do not aggregate returns** parameter on the **Commerce parameters** page.</span></span> <span data-ttu-id="48835-437">この場合、明細書を転記する時、各返品トランザクションは別の販売注文として転記されます。</span><span class="sxs-lookup"><span data-stu-id="48835-437">In this case, each return transaction will be posted as a separate sale order when posting a statement.</span></span> <span data-ttu-id="48835-438">このオプションは、トランザクション集計が有効になっている場合にのみ使用可能です。</span><span class="sxs-lookup"><span data-stu-id="48835-438">This option is only available if the transaction aggregation is enabled.</span></span>

## <a name="manage-customer-registration-numbers-from-pos"></a><span data-ttu-id="48835-439">POS からの顧客登録番号の管理</span><span class="sxs-lookup"><span data-stu-id="48835-439">Manage customer registration numbers from POS</span></span>

> [!NOTE]
> <span data-ttu-id="48835-440">この機能は、アプリケーション更新プログラム 10.0.6 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="48835-440">This functionality is available in Application update 10.0.6 and later.</span></span>

<span data-ttu-id="48835-441">顧客マスター レコードおよび顧客住所レコードを POS で作成または編集する場合、GSTIN、VAT 番号 (TIN)、および PAN 番号などの顧客登録番号を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="48835-441">You can specify customer registration numbers, such as GSTIN, VAT number (TIN), and PAN number, when creating or editing a customer master record and a customer address record in POS.</span></span> <span data-ttu-id="48835-442">顧客登録番号は領収書に印刷されるか、POS で顧客を検索するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="48835-442">The customer registration numbers may be printed in receipts or used for searching customers in POS.</span></span>

### <a name="configure-printing-customer-registration-numbers-in-receipts"></a><span data-ttu-id="48835-443">領収書の顧客登録番号印刷のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="48835-443">Configure printing customer registration numbers in receipts</span></span>

<span data-ttu-id="48835-444">領収書への顧客登録番号の印刷を有効にするには、[言語テキストおよびカスタム フィールドのコンフィギュレーション](#configure-language-texts-and-custom-fields) セクションで説明されている次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="48835-444">To enable printing customer registration numbers in receipts, follow the procedure outlined in the [Configure language texts and custom fields](#configure-language-texts-and-custom-fields) section.</span></span> <span data-ttu-id="48835-445">次の名前を使用して言語テキストおよびカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="48835-445">Add language texts and custom fields with the following names:</span></span>

- <span data-ttu-id="48835-446">**TAXREGISTRATIONGST_IN** GST 登録番号用。</span><span class="sxs-lookup"><span data-stu-id="48835-446">**TAXREGISTRATIONGST_IN** for the GST registration number;</span></span>
- <span data-ttu-id="48835-447">**TAXREGISTRATIONTIN_IN** VAT 登録番号用。</span><span class="sxs-lookup"><span data-stu-id="48835-447">**TAXREGISTRATIONTIN_IN** for the VAT registration number;</span></span>
- <span data-ttu-id="48835-448">**TAXREGISTRATIONPAN_IN** PAN 登録番号用。</span><span class="sxs-lookup"><span data-stu-id="48835-448">**TAXREGISTRATIONPAN_IN** for the PAN number.</span></span>

<span data-ttu-id="48835-449">領収書プロファイルへカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="48835-449">Add the custom fields to receipt profiles.</span></span>

### <a name="enable-searching-customers-by-tax-registration-numbers-in-pos"></a><span data-ttu-id="48835-450">POS での税務登録番号による顧客検索を有効にする</span><span class="sxs-lookup"><span data-stu-id="48835-450">Enable searching customers by tax registration numbers in POS</span></span>

<span data-ttu-id="48835-451">POS での税務登録番号による顧客検索を有効にするには、**コマース パラメーター** ページの **POS 検索基準** タブにおいて、**顧客検索基準** クイック タブにレコードを追加し、**顧客検索基準** ドロップダウン リスト内の **税務登録番号** を選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-451">To enable searching customers by tax registration numbers in POS, on the **POS search criteria** tab of the **Commerce parameters** page, add a record on the **Customer search criteria** fast-tab and select **Tax registration number** in the **Customer search criteria** drop-down list.</span></span> <span data-ttu-id="48835-452">**絞り込み可能** チェック ボックスはオフにし、**ショートカットとして表示** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="48835-452">Select the **Display as shortcut** checkbox while keeping the **Can be refined** checkbox clear.</span></span> <span data-ttu-id="48835-453">**配送スケジュール** ページで、1110 のジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="48835-453">Run the 1110 job on the **Distribution schedules** page.</span></span>
