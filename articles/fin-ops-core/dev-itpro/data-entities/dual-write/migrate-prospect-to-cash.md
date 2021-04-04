---
title: データ統合からデュアル書き込みへの見込顧客の現金データへの移行
description: このトピックでは、データ統合からデュアル書き込みへの見込顧客の現金データへの移行方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: 93614e43b108671de686458887c1d6dd6fe04f7a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570567"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a><span data-ttu-id="1b289-103">データ統合からデュアル書き込みへの見込顧客の現金データへの移行</span><span class="sxs-lookup"><span data-stu-id="1b289-103">Migrate Prospect to cash data from Data Integrator to dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1b289-104">データ統合からデュアル書き込みへの見込顧客の現金データへ移行するには、次の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="1b289-104">To migrate your Prospect to cash data from Data Integrator to dual-write, follow these steps.</span></span>

1. <span data-ttu-id="1b289-105">見込顧客から現金データの統合ジョブを実行して、最終的な完全同期を 1 つ実行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-105">Run the Prospect to cash Data Integrator jobs to do one final full synchronization.</span></span> <span data-ttu-id="1b289-106">これにより、両方のシステム (Finance and Operations アプリと Customer Engagement アプリ) がすべてのデータが確実に設定されます。</span><span class="sxs-lookup"><span data-stu-id="1b289-106">In this way, you ensure that both systems (Finance and Operations apps and customer engagement apps) have all the data.</span></span>
2. <span data-ttu-id="1b289-107">データが失われる可能性を防ぐには、Microsoft Dynamics 365 Sales から Excel ファイルまたはコンマ区切り値 (CSV) ファイルに、見込顧客を現金データにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="1b289-107">To help prevent potential data loss, export the Prospect to cash data from Microsoft Dynamics 365 Sales to an Excel file or a comma-separated values (CSV) file.</span></span> <span data-ttu-id="1b289-108">次のエンティティからデータをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="1b289-108">Export data from the following entities:</span></span>

    - [<span data-ttu-id="1b289-109">口座</span><span class="sxs-lookup"><span data-stu-id="1b289-109">Account</span></span>](#account-table)
    - [<span data-ttu-id="1b289-110">連絡</span><span class="sxs-lookup"><span data-stu-id="1b289-110">Contact</span></span>](#contact-table)
    - [<span data-ttu-id="1b289-111">請求書</span><span class="sxs-lookup"><span data-stu-id="1b289-111">Invoice</span></span>](#invoice-table)
    - <span data-ttu-id="1b289-112">製品の請求</span><span class="sxs-lookup"><span data-stu-id="1b289-112">Invoice products</span></span>
    - [<span data-ttu-id="1b289-113">注文</span><span class="sxs-lookup"><span data-stu-id="1b289-113">Order</span></span>](#order-table)
    - [<span data-ttu-id="1b289-114">受注製品</span><span class="sxs-lookup"><span data-stu-id="1b289-114">Order products</span></span>](#order-products-table)
    - [<span data-ttu-id="1b289-115">製品</span><span class="sxs-lookup"><span data-stu-id="1b289-115">Products</span></span>](#products-table)
    - [<span data-ttu-id="1b289-116">見積</span><span class="sxs-lookup"><span data-stu-id="1b289-116">Quote</span></span>](#quote-and-quote-product-tables)
    - [<span data-ttu-id="1b289-117">見積製品</span><span class="sxs-lookup"><span data-stu-id="1b289-117">Quote products</span></span>](#quote-and-quote-product-tables)

3. <span data-ttu-id="1b289-118">販売環境から見込顧客から入金ソリューションをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="1b289-118">Uninstall the Prospect to cash solution from the Sales environment.</span></span> <span data-ttu-id="1b289-119">この手順により、見込顧客からの入金ソリューションの列と対応するデータが削除されます。</span><span class="sxs-lookup"><span data-stu-id="1b289-119">This step removes the columns and corresponding data that the Prospect to cash solution introduced.</span></span>
4. <span data-ttu-id="1b289-120">二重書き込みソリューションをインストールします。</span><span class="sxs-lookup"><span data-stu-id="1b289-120">Install the dual-write solution.</span></span>
5. <span data-ttu-id="1b289-121">1 つ以上の法人に対して、Finance and Operations アプリと Customer Engagement アプリの間に二重書き込み接続を作成します。</span><span class="sxs-lookup"><span data-stu-id="1b289-121">Create a dual-write connection between the Finance and Operations app and the customer engagement app for one or more legal entities.</span></span>
6. <span data-ttu-id="1b289-122">デュアル書き込みテーブル マップを有効にし、必要な参照データに対して初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-122">Enable dual-write table maps, and run the initial synchronization for the required reference data.</span></span> <span data-ttu-id="1b289-123">(詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) をご覧ください。) 必須データの例として、顧客グループ、支払条件、支払スケジュールがあります。</span><span class="sxs-lookup"><span data-stu-id="1b289-123">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) Examples of required data include customer groups, payment terms, and payment schedules.</span></span> <span data-ttu-id="1b289-124">初期化が必要なテーブル (勘定、見積、見積行、注文、注文など) に対して二重書き込みマップを有効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1b289-124">Don't enable the dual-write maps for tables that require initialization, such as the account, quote, quote line, order, and order line tables.</span></span>
7. <span data-ttu-id="1b289-125">Customer Engagement アプリで、**詳細設定 \> システム設定 \> データ管理 \> 複製検出ルール** に移動し、すべてのルールを無効にします。</span><span class="sxs-lookup"><span data-stu-id="1b289-125">In the customer engagement app, go to **Advanced Settings \> System Settings \> Data Management \> Duplicate detection rules**, and disable all the rules.</span></span>
8. <span data-ttu-id="1b289-126">手順 2 に示したテーブルを初期化します。</span><span class="sxs-lookup"><span data-stu-id="1b289-126">Initialize the tables that are listed in step 2.</span></span> <span data-ttu-id="1b289-127">手順については、このトピックの残りのセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b289-127">For instructions, see the remaining sections of this topic.</span></span>
9. <span data-ttu-id="1b289-128">Finance and Operations アプリを開き、テーブル マップ (勘定、見積、見積依頼行、注文、注文の行テーブル マップなど) を有効にします。</span><span class="sxs-lookup"><span data-stu-id="1b289-128">Open the Finance and Operations app, and enable the table maps, such as the account, quote, quote line, order, and order line table maps.</span></span> <span data-ttu-id="1b289-129">その後初期同期を実行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-129">Then run the initial synchronization.</span></span> <span data-ttu-id="1b289-130">(詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。) このプロセスでは、Finance and Operations 処理ステータス、出荷先住所と請求先住所、サイト、倉庫などの追加情報をアプリケーションから同期します。</span><span class="sxs-lookup"><span data-stu-id="1b289-130">(For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).) This process will sync additional information from the Finance and Operations app, such as processing status, shipping and billing addresses, sites, and warehouses.</span></span>

## <a name="account-table"></a><span data-ttu-id="1b289-131">アカウント テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-131">Account table</span></span>

1. <span data-ttu-id="1b289-132">**会社** 列に、**USIM** などの会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-132">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="1b289-133">**関係タイプ** 列に、**顧客** を静的値として入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-133">In the **Relationship Type** column, enter **Customer** as a static value.</span></span> <span data-ttu-id="1b289-134">すべての勘定レコードをビジネス ロジックで顧客として分類する場合はそうではありません。</span><span class="sxs-lookup"><span data-stu-id="1b289-134">You might not want to classify every account record as a customer in your business logic.</span></span>
3. <span data-ttu-id="1b289-135">**顧客グループ ID** 列に、Finance and Operations アプリの顧客グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-135">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="1b289-136">見込顧客からの入金ソリューションの既定値は **10** です。</span><span class="sxs-lookup"><span data-stu-id="1b289-136">The default value from the Prospect to cash solution is **10**.</span></span>
4. <span data-ttu-id="1b289-137">**勘定番号** をカスタマイズせずに見込顧客から入金ソリューションを使用している場合は、**当事者番号** 列に **勘定番号** の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-137">If you're using the Prospect to cash solution without any customization of **Account Number**, enter an **Account Number** value in the **Party Number** column.</span></span> <span data-ttu-id="1b289-138">カスタマイズが存在し、当事者番号が分からない場合は、この情報を Finance and Operations アプリから取り込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1b289-138">If there are customizations, and you don't know the party number, pull this information from the Finance and Operations app.</span></span>

## <a name="contact-table"></a><span data-ttu-id="1b289-139">連絡先テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-139">Contact table</span></span>

1. <span data-ttu-id="1b289-140">**会社** 列に、**USIM** などの会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-140">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="1b289-141">CSV ファイルの **IsActiveCustomer** 値に基づいて、次の列を設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-141">Set the following columns, based on the **IsActiveCustomer** value in the CSV file:</span></span>

    - <span data-ttu-id="1b289-142">CSV ファイルで **IsActiveCustomer** が **はい** に設定されている場合は、**販売可能** 列を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-142">If **IsActiveCustomer** is set to **Yes** in the CSV file, set the **Sellable** column to **Yes**.</span></span> <span data-ttu-id="1b289-143">**顧客グループ ID** 列に、Finance and Operations アプリの顧客グループ番号を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-143">In the **Customer Group ID** column, enter the customer group number from the Finance and Operations app.</span></span> <span data-ttu-id="1b289-144">見込顧客からの入金ソリューションの既定値は **10** です。</span><span class="sxs-lookup"><span data-stu-id="1b289-144">The default value from the Prospect to cash solution is **10**.</span></span>
    - <span data-ttu-id="1b289-145">**ISActiveCustomer** が CSV ファイルで **"いいえ**" に設定されている場合は、**販売可能** 列を **"いいえ"** に設定し、**連絡先対象** を **顧客** に設定します 。</span><span class="sxs-lookup"><span data-stu-id="1b289-145">If **IsActiveCustomer** is set to **No** in the CSV file, set the **Sellable** column to **No**, and set the **Contact For** column to **Customer**.</span></span>

3. <span data-ttu-id="1b289-146">**連絡先番号** をカスタマイズせずに見込顧客を現金化ソリューションを使用している場合は、次の列を設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-146">If you're using the Prospect to cash solution without any customization of **Contact Number**, set the following columns:</span></span>

    - <span data-ttu-id="1b289-147">連絡先番号を CSV ファイル (**msdynce\_contactnumber**) から **連絡先** テーブルの連絡先 (**msdyn\_contactnumber**) に移行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-147">Migrate the contact number from the CSV file (**msdynce\_contactnumber**) to the contact number in the **Contact** table (**msdyn\_contactnumber**).</span></span>
    - <span data-ttu-id="1b289-148">**当事者番号** 列の **連絡先番号** テーブルの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b289-148">Use values from the **Contact Number** table in the **Party Number** column.</span></span>
    - <span data-ttu-id="1b289-149">**アカウント番号/当事者番号 ID** 列の **連絡先番号** テーブルの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b289-149">Use values from the **Contact Number** table in the **Account Number/Contact Person ID** column.</span></span>

## <a name="invoice-table"></a><span data-ttu-id="1b289-150">請求テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-150">Invoice table</span></span>

<span data-ttu-id="1b289-151">**請求書** テーブルのデータは、Finance and Operations アプリから Customer Engagement アプリに対して一方向に流れる設計なので、初期化の後で初期化を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1b289-151">Because data from the **Invoice** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="1b289-152">初期同期を実行して、必要なすべてのデータを Finance and Operations アプリから Customer Engagement アプリに移行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-152">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="1b289-153">詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b289-153">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="order-table"></a><span data-ttu-id="1b289-154">オーダー テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-154">Order table</span></span>

1. <span data-ttu-id="1b289-155">**会社** 列に、**USIM** などの会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-155">In the **Company** column, enter the company name, such as **USMF**.</span></span>
2. <span data-ttu-id="1b289-156">CSV ファイル内の **オーダー ID** 列の値を **販売注文番号** 列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="1b289-156">Copy the value of the **Order ID** column in the CSV file to the **Sales Order Number** column.</span></span>
3. <span data-ttu-id="1b289-157">CSV ファイル内の **顧客** 列の値を **販売注文番号** 列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="1b289-157">Copy the value of the **Customer** column in the CSV file to the **Invoice customer number** column.</span></span>
4. <span data-ttu-id="1b289-158">CSV ファイルの **国/地域に出荷** 列の値を **国/地域に出荷** 列にコピーします。</span><span class="sxs-lookup"><span data-stu-id="1b289-158">Copy the value of the **Ship To Country/Region** column in the CSV file to the **Ship To Country/Region** column.</span></span> <span data-ttu-id="1b289-159">この値の例として、**US** と **United States** があります。</span><span class="sxs-lookup"><span data-stu-id="1b289-159">Examples of this value include **US** and **United States**.</span></span>
5. <span data-ttu-id="1b289-160">**入荷希望日** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-160">Set the **Requested Receipt Date** column.</span></span> <span data-ttu-id="1b289-161">入荷日を使用しない場合は、CSVファイル内の **配送指定日** 列、**履行日** 列、**提出日** 列を使用します。</span><span class="sxs-lookup"><span data-stu-id="1b289-161">If you aren't using a receipt date, use the **Requested Delivery Date**, **Date Fulfilled**, and **Date Submitted** columns in the CSV file.</span></span> <span data-ttu-id="1b289-162">この値の例は **2020-03-27T00:00:00Z** です。</span><span class="sxs-lookup"><span data-stu-id="1b289-162">An example of this value is **2020-03-27T00:00:00Z**.</span></span>
6. <span data-ttu-id="1b289-163">**言語** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-163">Set the **Language** column.</span></span> <span data-ttu-id="1b289-164">この値の例は **en-us** です。</span><span class="sxs-lookup"><span data-stu-id="1b289-164">An example of this value is **en-us**.</span></span>
7. <span data-ttu-id="1b289-165">**品目ベース** 列を使用して **オーダー タイプ** 列を設定します。</span><span class="sxs-lookup"><span data-stu-id="1b289-165">Set the **Order Type** column by using the **Item-based** column.</span></span>

## <a name="order-products-table"></a><span data-ttu-id="1b289-166">オーダー製品テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-166">Order products table</span></span>

- <span data-ttu-id="1b289-167">**会社** 列に、**USIM** などの会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="1b289-167">In the **Company** column, enter the company name, such as **USMF**.</span></span>

## <a name="products-table"></a><span data-ttu-id="1b289-168">製品テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-168">Products table</span></span>

<span data-ttu-id="1b289-169">**製品** テーブルのデータは、Finance and Operations アプリから Customer Engagement アプリに対して一方向に流れる設計なので、初期化の後で初期化を行う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1b289-169">Because data from the **Products** table is designed to flow one way, from the Finance and Operations app to the customer engagement app, initialization isn't required.</span></span> <span data-ttu-id="1b289-170">初期同期を実行して、必要なすべてのデータを Finance and Operations アプリから Customer Engagement アプリに移行します。</span><span class="sxs-lookup"><span data-stu-id="1b289-170">Run the initial synchronization to migrate all the required data from the Finance and Operations app to the customer engagement app.</span></span> <span data-ttu-id="1b289-171">詳細については、[初期同期に関する考慮事項](initial-sync-guidance.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b289-171">For more information, see [Considerations for initial synchronization](initial-sync-guidance.md).</span></span>

## <a name="quote-and-quote-product-tables"></a><span data-ttu-id="1b289-172">見積および見積製品テーブル</span><span class="sxs-lookup"><span data-stu-id="1b289-172">Quote and Quote product tables</span></span>

<span data-ttu-id="1b289-173">**見積** テーブルについては、このトピックの前にある [オーダー テーブル](#order-table) セクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="1b289-173">For the **Quote** table, follow the instructions in the [Order table](#order-table) section earlier in this topic.</span></span> <span data-ttu-id="1b289-174">**見積製品** テーブルについては、[オーダー製品テーブル](#order-products-table) セクションの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="1b289-174">For the **Quote product** table, follow the instructions in the [Order products table](#order-products-table) section.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]