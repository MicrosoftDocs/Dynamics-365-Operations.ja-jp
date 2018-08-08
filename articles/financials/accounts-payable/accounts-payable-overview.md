---
title: "買掛金勘定のコンフィギュレーション"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations の買掛金勘定の基本機能およびオプション機能の設定に使用するページについて説明します。 また、買掛金勘定の設定を開始する前に実行しなければならない設定手順について説明します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, DeliveryMode, PaymTerm, VendGroup, VendParameters, VendPaymMode, VendTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 24671
ms.assetid: 82561fe7-b2d6-464c-9347-79d0ce0f9743
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6a832a30870f77578503bae6eea17ad1d0881d91
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="configure-accounts-payable"></a><span data-ttu-id="3025a-104">買掛金勘定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3025a-104">Configure Accounts payable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3025a-105">この記事は、Microsoft Dynamics 365 for Finance and Operations の買掛金勘定の基本機能およびオプション機能の設定に使用するページについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3025a-105">This article describes the pages that you use to set up basic and optional functionality for Accounts payable in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3025a-106">また、買掛金勘定の設定を開始する前に実行しなければならない設定手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="3025a-106">It also describes setup steps that you must complete before you start to set up Accounts payable.</span></span>

<a name="prerequisites-for-accounts-payable-setup"></a><span data-ttu-id="3025a-107">買掛金勘定設定の前提条件</span><span class="sxs-lookup"><span data-stu-id="3025a-107">Prerequisites for Accounts payable setup</span></span>
----------------------------------------

<span data-ttu-id="3025a-108">買掛金勘定を設定できるようにするには、その前に次の設定を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3025a-108">Before you can set up Accounts payable, you must complete the following setup:</span></span>

-   <span data-ttu-id="3025a-109">総勘定元帳:</span><span class="sxs-lookup"><span data-stu-id="3025a-109">In General ledger:</span></span>
    -   <span data-ttu-id="3025a-110">支払仕訳帳を使用する予定がある場合は、支払仕訳帳を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-110">If you plan to use payment journals, set up payment journals.</span></span>
    -   <span data-ttu-id="3025a-111">為替レート調整を実行する予定がある場合は、通貨ページで通貨コードを、為替レート タイプ ページで為替レート タイプを、通貨の為替レート ページで通貨の為替レートを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-111">If you plan to run exchange rate adjustments, set up currency codes on the Currencies page, set up exchange rate types on the Exchange rate types page, and set up currency exchange rates on the Currency exchange rates page.</span></span>
-   <span data-ttu-id="3025a-112">[現金および銀行管理] で、支払方法に使用する銀行口座を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-112">In Cash and bank management, set up bank accounts to use with methods of payment.</span></span>

## <a name="setup-pages-for-accounts-payable"></a><span data-ttu-id="3025a-113">買掛金勘定の設定ページ</span><span class="sxs-lookup"><span data-stu-id="3025a-113">Setup pages for Accounts payable</span></span>

<span data-ttu-id="3025a-114">次のページを使用して、法人ごとの買掛金勘定の基本機能を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-114">Use the following pages to set up the basic functionality of Accounts payable for each legal entity.</span></span> <span data-ttu-id="3025a-115">このページは推奨される設定の順に列挙されています。</span><span class="sxs-lookup"><span data-stu-id="3025a-115">The pages are listed in the recommended order of setup.</span></span> <span data-ttu-id="3025a-116">設定プロセスを簡略化するには、作成した最初のレコードからテンプレートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="3025a-116">To make the setup process easier, you can create templates from the first records that you create.</span></span> <span data-ttu-id="3025a-117">通常、テンプレートには組織が特定のタイプの仕入先に対して実装したい機能を反映させるために、多数のフィールドに値が入力されています。</span><span class="sxs-lookup"><span data-stu-id="3025a-117">In a template, values are typically entered in many fields to reflect the features that the organization wants to implement for a particular type of vendor.</span></span>
1.  <span data-ttu-id="3025a-118">支払条件ページで、販売注文、発注書、顧客、および仕入先に対して割り当てる支払条件を定義します。請求書の期限もこの条件によって決まります。</span><span class="sxs-lookup"><span data-stu-id="3025a-118">On the Terms of payment page, define the terms of payment that you assign to sales orders, purchase orders, customers, and vendors, and that determine invoice due dates.</span></span> <span data-ttu-id="3025a-119">詳細については、「[仕入先の支払手数料の定義](tasks/define-vendor-payment-fees.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3025a-119">For more information, see [Define vendor payment fees](tasks/define-vendor-payment-fees.md).</span></span>
2.  <span data-ttu-id="3025a-120">支払方法 - 仕入先ページでは、組織から仕入先への支払方法に関する情報を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-120">On the Methods of payment - vendors page, create and maintain information about how the organization pays its vendors.</span></span>
3.  <span data-ttu-id="3025a-121">仕入先グループ ページでは、転記、決済、支払、レポート、予測に必要な重要なパラメータを共有する仕入先のグループを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-121">On the Vendor groups page, create and maintain groups of vendors that share important parameters for posting, settlement and payment, reporting, and forecasting.</span></span>
4.  <span data-ttu-id="3025a-122">仕入先転記プロファイル ページでは、仕入先トランザクションの総勘定元帳への転記方法を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-122">On the Vendor posting profiles page, define how vendor transactions are posted to the general ledger.</span></span>
5.  <span data-ttu-id="3025a-123">買掛金管理パラメーター ページでは、特定の設定が指定されなかった場合に適用される既定の設定、さまざまな機能のパラメーター、および、買掛金勘定の各種の番号順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-123">On the Accounts payable parameters page, set up default settings that are applied if a more specific setting isn't specified, parameters for various kinds of functionality, and the various number sequences for Accounts payable.</span></span>
6.  <span data-ttu-id="3025a-124">フォームの設定ページでは、仕入先に関連したドキュメント、組織が仕入先からの受入を追跡するためのドキュメント、仕入先への支払フローの理由を入力するためのドキュメントなど、各種ドキュメントの形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="3025a-124">On the Form setup page, define the format of various documents that are related to vendors, and that the organization uses to keep track of receipts from vendors and enter reasons for the flow of payments to vendors.</span></span>
7.  <span data-ttu-id="3025a-125">仕入先ページでは、仕入先勘定、および組織が売上税を報告する税務当局を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-125">On the Vendors page, create and maintain vendor accounts, and also the tax authorities that your organization reports sales taxes to.</span></span>

## <a name="optional-setup-pages-for-accounts-payable"></a><span data-ttu-id="3025a-126">買掛金勘定のオプションの設定ページ</span><span class="sxs-lookup"><span data-stu-id="3025a-126">Optional setup pages for Accounts payable</span></span>
<span data-ttu-id="3025a-127">基本機能に加えて、買掛金勘定に設定できる他の機能があります。</span><span class="sxs-lookup"><span data-stu-id="3025a-127">In addition to the basic functionality, Accounts payable has other functionality that you can set up.</span></span>

<span data-ttu-id="3025a-128">追加のセットアップ ページは機能別にまとめられています。</span><span class="sxs-lookup"><span data-stu-id="3025a-128">The additional setup pages are organized by functionality.</span></span>

<span data-ttu-id="3025a-129">**ポリシー**</span><span class="sxs-lookup"><span data-stu-id="3025a-129">**Policies**</span></span>
-   <span data-ttu-id="3025a-130">仕入先請求ポリシー ページでは、仕入先請求ポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-130">On the Vendor invoice policy page, set up vendor invoice policies.</span></span>

<span data-ttu-id="3025a-131">**請求書照合**</span><span class="sxs-lookup"><span data-stu-id="3025a-131">**Invoice matching**</span></span>

-   <span data-ttu-id="3025a-132">請求合計の許容範囲ページでは、請求合計の許容範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-132">On the Invoice totals tolerances page, set up tolerances for invoice totals.</span></span>
-   <span data-ttu-id="3025a-133">照合ポリシー ページでは、ツーウェイ マッチング ポリシーとスリーウェイ マッチング ポリシーを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-133">On the Matching policy page, set up two-way and three-way matching policies.</span></span>
-   <span data-ttu-id="3025a-134">価格許容範囲ページでは、単価の許容範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-134">On the Price tolerances page, set up tolerances for unit prices.</span></span>
-   <span data-ttu-id="3025a-135">価格許容範囲品目グループ ページでは、品目価格の許容範囲グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-135">On the Item price tolerance groups page, set up tolerance groups for item prices.</span></span>
-   <span data-ttu-id="3025a-136">仕入先価格許容範囲グループ ページでは、仕入先の価格の許容範囲グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-136">On the Vendor price tolerance groups page, set up  tolerance groups for vendor prices.</span></span>
-   <span data-ttu-id="3025a-137">諸費用の許容範囲ページでは、諸費用の許容範囲を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-137">On the Charges tolerances page, set up tolerances for charges.</span></span>

<span data-ttu-id="3025a-138">**ワークフロー**</span><span class="sxs-lookup"><span data-stu-id="3025a-138">**Workflow**</span></span>

-   <span data-ttu-id="3025a-139">買掛金管理ワークフロー ページでは、仕訳承認および購買要求のワークフロー コンフィギュレーションを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-139">On the Accounts payable workflows page, set up workflow configurations for journal approvals and purchase requisitions.</span></span>

<span data-ttu-id="3025a-140">**理由**</span><span class="sxs-lookup"><span data-stu-id="3025a-140">**Reasons**</span></span>

-   <span data-ttu-id="3025a-141">仕入先の理由ページでは、理由コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-141">On the Vendor reasons page, set up reason codes.</span></span>

<span data-ttu-id="3025a-142">**諸掛**</span><span class="sxs-lookup"><span data-stu-id="3025a-142">**Charges**</span></span>

-   <span data-ttu-id="3025a-143">諸費用コード ページでは、発注書に使用する諸費用のコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-143">On the Charges code page, set up codes for the charges that are used in purchase orders.</span></span>
-   <span data-ttu-id="3025a-144">仕入先の諸費用グループ ページでは、仕入先の諸費用グループを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-144">On the Vendor charges group page, create and maintain charges groups for vendors.</span></span>
-   <span data-ttu-id="3025a-145">品目請求金額グループ ページでは、品目の諸費用グループを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-145">On the Item charge groups page, create and maintain charges groups for items.</span></span>
-   <span data-ttu-id="3025a-146">自動請求 ページでは、注文に自動的に割り当てられる諸費用を定義します。</span><span class="sxs-lookup"><span data-stu-id="3025a-146">On the Auto charges page, define the charges that are automatically assigned to orders.</span></span>

<span data-ttu-id="3025a-147">**提供品**</span><span class="sxs-lookup"><span data-stu-id="3025a-147">**Supplementary items**</span></span>

-   <span data-ttu-id="3025a-148">提供品グループ - 仕入先ページでは、仕入先の提供品グループを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-148">On the Supplementary item groups - Vendor page, create and maintain supplementary item groups for vendors.</span></span>
-   <span data-ttu-id="3025a-149">提供品グループ - 在庫ページでは、品目の提供品グループを作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-149">On the Supplementary item groups - Inventory page, create and maintain supplementary item groups for items.</span></span>

<span data-ttu-id="3025a-150">**配布**</span><span class="sxs-lookup"><span data-stu-id="3025a-150">**Distribution**</span></span>

-   <span data-ttu-id="3025a-151">配送条件ページでは、売り手から買い手に品目を配送するときの条件を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-151">On the Terms of delivery page, create and maintain the conditions for an item's transfer from seller to buyer.</span></span>
-   <span data-ttu-id="3025a-152">荷渡方法ページでは、売り手から買い手に注文を配送するときの配送方法を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-152">On the Modes of delivery page, create and maintain the methods of transport that are used when an order is delivered from the seller to the buyer.</span></span>
-   <span data-ttu-id="3025a-153">行先コード ページでは、配送先の ID コードと説明を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-153">On the Destination codes page, create and maintain identifiers and descriptions for delivery destinations.</span></span>

<span data-ttu-id="3025a-154">**フォーム**</span><span class="sxs-lookup"><span data-stu-id="3025a-154">**Forms**</span></span>

-   <span data-ttu-id="3025a-155">フォーム メモ ページでは、各種のフォームに表示される標準のテキストを作成します。</span><span class="sxs-lookup"><span data-stu-id="3025a-155">On the Form notes page, create the standard text that appears on various pages.</span></span>
-   <span data-ttu-id="3025a-156">フォーム並べ替えパラメーター ページでは、在庫要求、入庫リスト、梱包明細、および請求書の並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-156">On the Form sorting parameters page, set up the sorting order for requisitions, receipt lists, packing slips, and invoices.</span></span>
-   <span data-ttu-id="3025a-157">印刷管理設定 ページでは、ページのオリジナルおよびコピーの印刷管理情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-157">On the Print management setup page, set up print management information for originals and copies of pages.</span></span>

<span data-ttu-id="3025a-158">**支払利息**</span><span class="sxs-lookup"><span data-stu-id="3025a-158">**Payments**</span></span>

-   <span data-ttu-id="3025a-159">現金割引ページでは、現金割引の適用条件を設定および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-159">On the Cash discounts page, set up and manage the terms for obtaining cash discounts.</span></span> <span data-ttu-id="3025a-160">現金割引コードは仕入先に関連付けられ、発注書に適用されます。</span><span class="sxs-lookup"><span data-stu-id="3025a-160">The cash discount codes are linked to vendors and are applied to purchase orders.</span></span>
-   <span data-ttu-id="3025a-161">支払スケジュール ページでは、仕入先への分割支払の管理に使用される支払スケジュールを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-161">On the Payment schedules page, set up the payment schedules that are used to manage installment payments to vendors.</span></span>
-   <span data-ttu-id="3025a-162">支払期日ページでは、期限の計算に使用される支払期日を定義したり、支払期日として特定の曜日または特定の日を指定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-162">On the Payment days page, define the payment days that are used to calculate due dates, and specify payment days for a specific day of the week or month.</span></span>
-   <span data-ttu-id="3025a-163">支払手数料ページでは、仕入先に関連付けられる支払手数料を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-163">On the Payment fee page, create and maintain the payment fees that are associated with vendors.</span></span>
-   <span data-ttu-id="3025a-164">支払指示ページでは、支払指示を作成および管理します。</span><span class="sxs-lookup"><span data-stu-id="3025a-164">On the Payment instruction page, create and maintain payment instructions.</span></span>

<span data-ttu-id="3025a-165">**統計**</span><span class="sxs-lookup"><span data-stu-id="3025a-165">**Statistics**</span></span>

-   <span data-ttu-id="3025a-166">エイジング期間の定義ページでは、仕入先勘定の満期分布を分析するためのユーザー定義の期間を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-166">On the Aging period definitions page, set up user-defined intervals that are used to analyze the maturity distribution of vendor accounts.</span></span>
-   <span data-ttu-id="3025a-167">業種ページでは、仕入先に割り当てる業種 (LOB) コードを作成します。</span><span class="sxs-lookup"><span data-stu-id="3025a-167">On the Line of business page, create the line of business (LOB) codes that are assigned to vendors.</span></span>

<span data-ttu-id="3025a-168">**税金 1099**</span><span class="sxs-lookup"><span data-stu-id="3025a-168">**Tax 1099**</span></span>

-   <span data-ttu-id="3025a-169">**1099 フィールド** ページでは、最新の米国内国歳入庁 (IRS) 要件に基づいて、IRS に報告する必要がある最小額を検証および更新します。</span><span class="sxs-lookup"><span data-stu-id="3025a-169">On the **1099 fields** page, verify and update the minimum amounts that must be reported to the Internal Revenue Service (IRS), based on the latest IRS requirements.</span></span>

## <a name="optional-setup-for-other-modules"></a><span data-ttu-id="3025a-170">**オプションの設定 (他のモジュール)**</span><span class="sxs-lookup"><span data-stu-id="3025a-170">**Optional setup for other modules**</span></span>
<span data-ttu-id="3025a-171">**組織管理**</span><span class="sxs-lookup"><span data-stu-id="3025a-171">**Organization administration**</span></span>

-   <span data-ttu-id="3025a-172">番号順序ページでは、請求書番号の番号順序グループを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-172">On the Number sequences page, set up number sequence groups for invoice numbers.</span></span>
-   <span data-ttu-id="3025a-173">次のページでは、住所情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-173">On the following pages, set up address information:</span></span>
    -   <span data-ttu-id="3025a-174">住所の設定</span><span class="sxs-lookup"><span data-stu-id="3025a-174">Address setup</span></span>
    -   <span data-ttu-id="3025a-175">NAF コード</span><span class="sxs-lookup"><span data-stu-id="3025a-175">NAF codes</span></span>
    -   <span data-ttu-id="3025a-176">郵便番号のインポート</span><span class="sxs-lookup"><span data-stu-id="3025a-176">Import ZIP/postal codes</span></span>

<span data-ttu-id="3025a-177">**総勘定元帳**</span><span class="sxs-lookup"><span data-stu-id="3025a-177">**General ledger**</span></span>

-   <span data-ttu-id="3025a-178">財務分析コード ページでは、財務分析コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-178">On the Financial dimensions page, set up financial dimensions.</span></span>
-   <span data-ttu-id="3025a-179">次のページでは、税金情報を設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-179">On the following pages, set up tax information:</span></span>
    -   <span data-ttu-id="3025a-180">消費税コード</span><span class="sxs-lookup"><span data-stu-id="3025a-180">Sales tax codes</span></span>
    -   <span data-ttu-id="3025a-181">消費税グループ</span><span class="sxs-lookup"><span data-stu-id="3025a-181">Sales tax groups</span></span>
    -   <span data-ttu-id="3025a-182">品目消費税グループ</span><span class="sxs-lookup"><span data-stu-id="3025a-182">Item sales tax groups</span></span>
    -   <span data-ttu-id="3025a-183">勘定グループ</span><span class="sxs-lookup"><span data-stu-id="3025a-183">Account group</span></span>
    -   <span data-ttu-id="3025a-184">売上税非課税コード</span><span class="sxs-lookup"><span data-stu-id="3025a-184">Sales tax exempt codes</span></span>
    -   <span data-ttu-id="3025a-185">地方税務署</span><span class="sxs-lookup"><span data-stu-id="3025a-185">Sales tax jurisdictions</span></span>
    -   <span data-ttu-id="3025a-186">消費税所轄官庁</span><span class="sxs-lookup"><span data-stu-id="3025a-186">Sales tax authorities</span></span>
    -   <span data-ttu-id="3025a-187">消費税決済期間</span><span class="sxs-lookup"><span data-stu-id="3025a-187">Sales tax settlement periods</span></span>

<span data-ttu-id="3025a-188">**現金および銀行管理**</span><span class="sxs-lookup"><span data-stu-id="3025a-188">**Cash and bank management**</span></span>

-   <span data-ttu-id="3025a-189">支払目的コード ページでは、中央銀行の支払目的コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="3025a-189">On the Payment purpose codes page, set up the Central Bank purpose code.</span></span>






