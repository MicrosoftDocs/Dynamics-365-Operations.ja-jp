---
title: Dynamics 365 Finance バージョン 10.0.7 の機能のプレビュー (2020 年 1 月)
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.7 の新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 10/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 95e565f9f5d0bd85f134d4c481c115b2eabe65cc
ms.sourcegitcommit: 381ea71cf22898587ca6af4700b51ad1b4d1a397
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2019
ms.locfileid: "2660822"
---
# <a name="preview-features-in-dynamics-365-finance-version-1007-january-2020"></a><span data-ttu-id="8f7e2-103">Dynamics 365 Finance バージョン 10.0.7 の機能のプレビュー (2020 年 1 月)</span><span class="sxs-lookup"><span data-stu-id="8f7e2-103">Preview features in Dynamics 365 Finance version 10.0.7 (January 2020)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8f7e2-104">このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.7 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Finance version 10.0.7.</span></span> <span data-ttu-id="8f7e2-105">このバージョンのビルド番号は 10.0.283 です。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-105">This version has a build number of 10.0.283.</span></span> <span data-ttu-id="8f7e2-106">一般提供開始日は 2020 年 1 月ですが、新機能は 10 月の初期リリースで使用できます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-106">While the general availability date is in January 2020, the new features are available for early release in October.</span></span> <span data-ttu-id="8f7e2-107">バージョン 10.0.7 の詳細については [追加リソース](../../fin-ops-core/fin-ops/get-started/whats-new-changed-7-0-february-2016.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-107">For more information about version 10.0.7, see [Additional resources](../../fin-ops-core/fin-ops/get-started/whats-new-changed-7-0-february-2016.md#additional-resources).</span></span>

## <a name="budget-register-entry-enhancements"></a><span data-ttu-id="8f7e2-108">予算登録エントリの機能拡張</span><span class="sxs-lookup"><span data-stu-id="8f7e2-108">Budget register entry enhancements</span></span>

<span data-ttu-id="8f7e2-109">**数量のみの予算登録エントリ**機能により、数量のみの金額の予算登録エントリを転記する機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-109">The **Budget register entries for quantity only** feature enables the ability to post a budget register entry with quantity-only amounts.</span></span> <span data-ttu-id="8f7e2-110">たとえば、価格が 0 で数量が 32 の予算エントリを転記すると、金額は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-110">For example, you could post a budget entry of 32 quantity with a price of zero, resulting in an amount of zero.</span></span> <span data-ttu-id="8f7e2-111">次に、財務報告レポートのコンテキスト内でこの数量を使用し、この数量とは別に金額の計算を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-111">You may then use this quantity within the context of a financial reporting report to display a calculation of an amount devided by this quantity.</span></span> <span data-ttu-id="8f7e2-112">詳細については、[予算作成の概要](../budgeting/basic-budgeting-overview-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-112">See [budgeting overview](../budgeting/basic-budgeting-overview-configuration.md) for details.</span></span> 

<span data-ttu-id="8f7e2-113">**予算登録エントリの金額タイプの既定値**機能により、予算明細行の主勘定に基づいて、収益または経費に対する金額タイプの規定値を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-113">The **Budget register entries defaulting of amount type** feature enables the defaulting of amount type to revenue or expense based on the main account of the budget line.</span></span> <span data-ttu-id="8f7e2-114">詳細については、[予算作成の概要](../budgeting/basic-budgeting-overview-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-114">See [budgeting overview](../budgeting/basic-budgeting-overview-configuration.md) for details.</span></span> 


## <a name="ability-to-export-records-from-the-accounts-payable-invoice-pool-form"></a><span data-ttu-id="8f7e2-115">買掛金勘定の請求書のプール フォームからレコードをエクスポートする機能</span><span class="sxs-lookup"><span data-stu-id="8f7e2-115">Ability to export records from the Accounts payable invoice pool form</span></span>
<span data-ttu-id="8f7e2-116">この機能により、**買掛金勘定の請求のプール** フォームから Excel にレコードをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-116">This feature lets you export records from the **Accounts payable invoice pool** form to Excel.</span></span> <span data-ttu-id="8f7e2-117">この能力により、Excel のグリッド データの表示および分析を行うための生産的な環境が提供されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-117">This capability provides a productive environment to review and analyze the grid data in Excel.</span></span> 

## <a name="ledger-settlement-by-user"></a><span data-ttu-id="8f7e2-118">ユーザー別の元帳決済</span><span class="sxs-lookup"><span data-stu-id="8f7e2-118">Ledger settlement by user</span></span>

<span data-ttu-id="8f7e2-119">元帳決済は、マークされたトランザクションをユーザーごとに決済するようになりました。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-119">Ledger settlement will now settle marked transactions by user.</span></span>  <span data-ttu-id="8f7e2-120">ページを開くと、決済用にユーザーごとにマークされたトランザクション、またはユーザーによってマークされていないトランザクションのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-120">When opening the page, only transactions marked by the user for settlement or transactions not marked by anyone will display.</span></span> <span data-ttu-id="8f7e2-121">また、ユーザー ID ごとにトランザクションのマークを解除するための新しいボタンが導入されました。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-121">Also, a new button has been introduced to unmark transaction by user ID.</span></span>  <span data-ttu-id="8f7e2-122">これにより、会計マネージャーは、決済を完了する前に休暇に出かけた、または組織を離れたユーザーのトランザクションのマークを解除することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-122">This will allow an accounting manager to unmark transactions for a user that left on vacation before finishing the settlement or for a user who has left the organization.</span></span>  <span data-ttu-id="8f7e2-123">このアクションにより、決済用にマークするために、他のユーザーのトランザクションを確保することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-123">The action will free up those transactions for another user to mark them for settlement.</span></span> 


## <a name="forecast-position-reports-public-sector"></a><span data-ttu-id="8f7e2-124">予測職位のレポート (公的部門)</span><span class="sxs-lookup"><span data-stu-id="8f7e2-124">Forecast position reports (Public Sector)</span></span>

<span data-ttu-id="8f7e2-125">**予測職位の集計**レポートを使用して、指定した予算計画およびシナリオにおいて予測職位情報を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-125">You can use the **Forecast position summary** report to generate forecast position information for during a budget plan and scenario that you specify.</span></span>  <span data-ttu-id="8f7e2-126">**予測職位の集計**レポートには、予測職位の原価が勘定配布ごとに表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-126">The **Forecast position summary** report shows forecast position costs by account distributions.</span></span> <span data-ttu-id="8f7e2-127">予測職位の原価は、割り当てられた勘定配布ごとにグループ化されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-127">The forecast position costs are shown, grouped by their assigned account distributions.</span></span> <span data-ttu-id="8f7e2-128">原価金額は、勘定配布に割り当てられている割合ごとに考慮されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-128">The cost amounts are factored by the percentage assigned to the account distribution.</span></span> 

## <a name="purchasing-cards-public-sector"></a><span data-ttu-id="8f7e2-129">購買カード (公的機関)</span><span class="sxs-lookup"><span data-stu-id="8f7e2-129">Purchasing cards (Public Sector)</span></span>

<span data-ttu-id="8f7e2-130">機関は購買カードを使用することにより、従業員は標準の購買要求プロセスを使用せずに商品およびサービスを調達することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-130">Agencies use purchasing cards so that employees can procure goods and services without using the standard purchase requisition process.</span></span> <span data-ttu-id="8f7e2-131">購買カードに関連するページおよびフィールドにより、購買を追跡するためのメカニズムが提供されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-131">The pages and fields that are related to purchasing cards provide a mechanism for tracking purchases.</span></span> <span data-ttu-id="8f7e2-132">従業員が購買カードを使用して行った購買はそれぞれ仕入先請求書に記録されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-132">Each purchase that an employee makes by using a purchasing card is recorded on a vendor invoice.</span></span> <span data-ttu-id="8f7e2-133">ただし、請求書は商品またはサービスを提供した仕入先に対して小切手または電子支払を使用して支払われません。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-133">However, the invoice isn't paid by using a check or electronic payment to the vendor that provided the goods or services.</span></span> <span data-ttu-id="8f7e2-134">その代わり、このタイプの請求書はそれぞれ、購買カード サービスを提供する仕入先に支払うために作成された別の仕入先請求書に関連付けられます (つまり、金融機関)。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-134">Instead, each invoice of this type is associated with another vendor invoice that is created to pay the vendor that provides the purchasing card services (that is, the financial institution).</span></span> <span data-ttu-id="8f7e2-135">購買カード サービスのプロバイダーに支払う義務のある残高について月ごとに支払いが行われる時に、カードの購買の支払いが行われます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-135">The card purchases are paid off when the balance that is owed to the purchasing card services provider is paid each month.</span></span>

## <a name="mark-a-purchase-agreement-as-closed"></a><span data-ttu-id="8f7e2-136">購買契約書を「決済済」としてマークする</span><span class="sxs-lookup"><span data-stu-id="8f7e2-136">Mark a Purchase agreement as "Closed"</span></span>

<span data-ttu-id="8f7e2-137">ユーザーは、有効に使用されていない契約について知らせるために、購買契約書を「決済済」としてマークすることができるようになりました。これにより、ユーザーは購買契約書からリリース注文を作成できなくなります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-137">Users can now mark a Purchase agreement as "Closed" to signal the agreement is no longer actively used, making it so users will not be able to create release orders from the purchase agreement.</span></span>

## <a name="delayed-tax-calculation-on-journal"></a><span data-ttu-id="8f7e2-138">仕訳帳の税金計算遅延</span><span class="sxs-lookup"><span data-stu-id="8f7e2-138">Delayed tax calculation on journal</span></span>

<span data-ttu-id="8f7e2-139">この機能により、非常に多数のトランザクションが含まれている場合に、仕訳帳での税計算のパフォーマンスが改善されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-139">This feature improves the performance of tax calculations on journals when the they contain a significant number of transactions.</span></span> <span data-ttu-id="8f7e2-140">この機能が有効になっている場合、ユーザーが**売上税**コマンドをクリックするか、仕訳帳を転記するときにのみ、税額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-140">Tax amounts will only be calculated when you click the **Sales Tax** command or when you post the journal when this feature is enabled.</span></span> <span data-ttu-id="8f7e2-141">詳細については、[仕訳帳の税金計算遅延の有効化](../general-ledger/enable-delayed-tax-calculation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-141">For more information, see [Enable delayed tax calculation on journal](../general-ledger/enable-delayed-tax-calculation.md) for details.</span></span>

## <a name="reverse-journal-posting"></a><span data-ttu-id="8f7e2-142">仕訳帳の転記の取消</span><span class="sxs-lookup"><span data-stu-id="8f7e2-142">Reverse journal posting</span></span>

<span data-ttu-id="8f7e2-143">この機能により、転記された仕訳帳全体、またはその発生元に関係なく伝票トランザクション リストから 1 つ以上の伝票を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-143">This feature lets you reverse an entire posted journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> <span data-ttu-id="8f7e2-144">詳細については、[仕訳帳の転記の取消](../general-ledger/reverse-journal-posting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-144">Please refer to [Reverse journal posting](../general-ledger/reverse-journal-posting.md) for details.</span></span>

## <a name="prohibit-submission-to-workflow-when-there-are-unallocated-charges-on-a-vendor-invoice"></a><span data-ttu-id="8f7e2-145">仕入先請求書に配賦されていない費用がある場合は、ワークフローへの送信を禁止する</span><span class="sxs-lookup"><span data-stu-id="8f7e2-145">Prohibit submission to workflow when there are unallocated charges on a vendor invoice</span></span>
<span data-ttu-id="8f7e2-146">この機能により、未配賦の料金が含まれている場合に仕入先請求書がワークフロー プロセスに送信されないようになります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-146">This feature lets you prevent a vendor invoice from being submitted to the workflow process when it contains unallocated charges.</span></span> <span data-ttu-id="8f7e2-147">代わりに、請求書を送信した担当者が未配賦の料金があるという警告を受け取り、ワークフローに送信する前に修正できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-147">Instead, the person who submitted the invoice receives an alert that it has unallocated charges and lets them correct it before submitting it to workflow.</span></span>


## <a name="account-groups-selection-for-chinese-voucher-types"></a><span data-ttu-id="8f7e2-148">中国の伝票タイプに対する勘定グループの選択</span><span class="sxs-lookup"><span data-stu-id="8f7e2-148">Account groups selection for Chinese voucher types</span></span>

<span data-ttu-id="8f7e2-149">この機能により、中国の伝票タイプを設定する時、勘定グループを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-149">This feature allows you to select accounts groups when setting up voucher types for China.</span></span> 

### <a name="enable-the-feature"></a><span data-ttu-id="8f7e2-150">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="8f7e2-150">Enable the feature</span></span>
1. <span data-ttu-id="8f7e2-151">**ワークスペース > 機能の管理**で機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-151">Enable the feature in the **Workspaces > Feature management**.</span></span>
2. <span data-ttu-id="8f7e2-152">機能により、伝票タイプの設定が保存される新しいテーブルが導入されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-152">Feature introduces a new table where voucher type setup is stored.</span></span> <span data-ttu-id="8f7e2-153">既存の中国の伝票タイプの設定を新しいテーブルにコピーするには、**システム管理 > 定期処理のタスク > データベース > 整合性チェック**に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-153">To copy existing Chinese voucher types setup to a new table, go to **System administration > Periodic tasks > Database > Consistency check**.</span></span> <span data-ttu-id="8f7e2-154">**プログラム > 一般会計**を展開し、**伝票の制限タイプ** チェック ボックスをマークします。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-154">Expand **Program > General ledger** and mark **Restriction type for voucher** check box.</span></span> 
3. <span data-ttu-id="8f7e2-155">**確認/修正**フィールドで**確認**を選択し、新しいテーブルをコピーするように既存の設定が設定されているかどうかを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-155">Select **Check** in the **Check/Fix** field to check whether there are settings in existing setup to copy to a new table.</span></span>
4. <span data-ttu-id="8f7e2-156">**確認/修正**フィールドで**修正**を選択すると、既存の設定から新しいテーブルに設定をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-156">Select **Fix** in the **Check/Fix** field to copy settings from existing table to a new table.</span></span>

### <a name="set-up-voucher-type"></a><span data-ttu-id="8f7e2-157">伝票タイプの設定</span><span class="sxs-lookup"><span data-stu-id="8f7e2-157">Set up Voucher type</span></span>
1. <span data-ttu-id="8f7e2-158">**一般会計 > 仕訳帳の設定 > 中国の伝票タイプ > 伝票タイプ**に移動します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-158">Go to **General ledger > Journal setup > Chinese voucher type > Voucher type**.</span></span>
2. <span data-ttu-id="8f7e2-159">**ルール** クイック タブの下で、固有の制限のある明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-159">Under the **Rules** FastTab, select the line with specific restriction.</span></span>
2. <span data-ttu-id="8f7e2-160">**影響を受ける勘定** クイック タブの下で**追加**をクリックして、選択されたルールに対する勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-160">Under the **Impacted accounts** FastTab, click **Add** and set up the accounts for the selected rule:</span></span>
- <span data-ttu-id="8f7e2-161">**勘定タイプ** フィールドで、**元帳**、**顧客**、**仕入先**、**プロジェクト**、**固定資産**、**銀行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-161">In the **Account type** field, select **Ledger**, **Customer**, **Vendor**, **Project**, **Fixed assets**, **Bank**</span></span>
- <span data-ttu-id="8f7e2-162">**勘定コード**において、**勘定**、**グループ**、または**すべて**を選択します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-162">In the **Account code**, select **Account**, **Group**, or **All**.</span></span> <span data-ttu-id="8f7e2-163">**グループ**値は**元帳**勘定コードでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-163">Note that the value **Group** is not available for **Ledger** account code.</span></span>
- <span data-ttu-id="8f7e2-164">**グループ番号**フィールドで、**勘定コード** フィールドで**グループ**を選択した場合、**勘定タイプ**の値に、顧客グループ、仕入先グループ、プロジェクト グループ、固定資産グループ、または銀行グループをそれぞれ選択します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-164">In the **Group number** field, select customer group, vendor group, project group, fixed asset group, or bank group respectively to the value in **Account type**, if you selected **Group** in the field **Account code**.</span></span>
- <span data-ttu-id="8f7e2-165">**勘定番号**フィールドにおいて、**勘定コード** フィールドで**テーブル**を選択した場合、**勘定タイプ**の値に、勘定科目、顧客勘定、仕入先勘定、プロジェクト ID、固定資産番号、または銀行勘定をそれぞれ選択します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-165">In the **Account number** field, select ledger account, customer account, vendor account, project ID, fixed asset number, or bank account respectively value in **Account type**, if you selected **Table** in the field **Account code**</span></span>

<span data-ttu-id="8f7e2-166">中国の伝票タイプの設定方法に関する詳細はトピックで確認します [中国の伝票の設定](../localizations/tasks/set-up-chinese-vouchers.md)。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-166">Find more details about how to set up Chinese voucher types in the topic [Set up Chinese vouchers](../localizations/tasks/set-up-chinese-vouchers.md)</span></span>

## <a name="sort-by-resource-in-the-project-invoice-proposal"></a><span data-ttu-id="8f7e2-167">プロジェクトの仮発行請求書のリソースで並べ替え</span><span class="sxs-lookup"><span data-stu-id="8f7e2-167">Sort by resource in the project invoice proposal</span></span>

<span data-ttu-id="8f7e2-168">**プロジェクトの請求書の提案作成中のリソースによる並べ替えの有効化**機能により、プロジェクトの経理担当者が、新しいプロジェクトの請求書提案の作成時に、リソースによって並び替えられる請求に使用可能なプロジェクト取引をソートできる機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-168">The **Enable sorting by resource during project invoice proposal creation** feature enables the ability for the project accountant to sort the project transactions available for billing to be sorted by the resource when creating a new project invoice proposal.</span></span> <span data-ttu-id="8f7e2-169">使用可能なプロジェクト取引を表示するグリッドには、リソース ID とリソースのための別のフィールドがあります。これにより、ユーザーは、リソース名に対してフィルター処理や並べ替えを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-169">The grid displaying the available project transactions will have a separate field for Resource ID and Resource, allowing the user to filter and sort on the resource name.</span></span> <span data-ttu-id="8f7e2-170">この機能は既定で無効になっており、**ワークスぺース > 機能管理**で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-170">This feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span>

## <a name="run-settle-and-post-sales-tax-in-batch-mode"></a><span data-ttu-id="8f7e2-171">バッチ モードでの消費税の決済と転記の実行</span><span class="sxs-lookup"><span data-stu-id="8f7e2-171">Run Settle and post sales tax in batch mode</span></span> 

<span data-ttu-id="8f7e2-172">ユーザーは、イタリア、ベルギー、およびオーストラリアで**消費税の決済と転記**を実行できるようになりました。設定については、[消費税精算期間の設定](../general-ledger/tasks/set-up-sales-tax-settlement-periods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-172">Users can now run **Settle and post sales tax** in batch mode in Italy, Belgium and Australia, please refer to [Set up sales tax settlement periods](../general-ledger/tasks/set-up-sales-tax-settlement-periods.md) for the setup.</span></span> 

## <a name="tax-engine"></a><span data-ttu-id="8f7e2-173">税エンジン</span><span class="sxs-lookup"><span data-stu-id="8f7e2-173">Tax engine</span></span> 

<span data-ttu-id="8f7e2-174">税エンジン (GTE) は、現在のみインドのみで使用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-174">The tax engine (GTE) is currently only available for India.</span></span> 

### <a name="create-tax-component-with-pre-defined-rules"></a><span data-ttu-id="8f7e2-175">事前定義済ルールを使用した税コンポーネントの作成</span><span class="sxs-lookup"><span data-stu-id="8f7e2-175">Create tax component with pre-defined rules</span></span>

<span data-ttu-id="8f7e2-176">最初から新しい税コンポーネントを作成する代わりに、ユーザーは、逆請求、非控除などの、よく使用される課税ルールをサポートする事前定義済の税ルールを作成できるようになりました。詳細については、[税コンポーネントの作成](../localizations/tax-engine-create-tax-component.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-176">Instead of creating a new tax component from scratch, users can now create it with predefined tax rules which support the most commonly used taxation rules like reverse charge, non-deductible, etc., please refer to [Create tax component](../localizations/tax-engine-create-tax-component.md) for details.</span></span>



## <a name="additional-resources"></a><span data-ttu-id="8f7e2-177">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8f7e2-177">Additional resources</span></span>

### <a name="platform-update-31"></a><span data-ttu-id="8f7e2-178">プラットフォーム update 31</span><span class="sxs-lookup"><span data-stu-id="8f7e2-178">Platform update 31</span></span>

<span data-ttu-id="8f7e2-179">Microsoft Dynamics 365 Supply Chain Management 10.0.7 には、プラットフォーム更新プログラム 31 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-179">Microsoft Dynamics 365 Supply Chain Management 10.0.7 includes Platform update 31.</span></span> <span data-ttu-id="8f7e2-180">プラットフォーム更新プログラム 31 に関する詳細については、[プラットフォーム更新プログラム 31 のプレビュー機能](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-180">To learn more about Platform update 31, see [Preview features in Platform update 31](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md).</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="8f7e2-181">バグ修正</span><span class="sxs-lookup"><span data-stu-id="8f7e2-181">Bug fixes</span></span> 
<span data-ttu-id="8f7e2-182">10.0.7 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-182">For information about the bug fixes included in each of the updates that are part of 10.0.7, sign in to Lifecycle Services (LCS) and view the [KB article](https://https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493).</span></span>


### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="8f7e2-183">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="8f7e2-183">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="8f7e2-184">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="8f7e2-184">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="8f7e2-185">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-185">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="8f7e2-186">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-186">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="8f7e2-187">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="8f7e2-187">Removed and deprecated features</span></span>

<span data-ttu-id="8f7e2-188">[削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-188">The [Removed or deprecated features](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="8f7e2-189">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-189">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="8f7e2-190">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-190">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="8f7e2-191">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-191">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="8f7e2-192">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-192">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="8f7e2-193">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="8f7e2-193">Typically, these are functional updates that need to be made to the compiler.</span></span>

