---
title: Dynamics 365 Finance バージョン 10.0.7 (2020 年 1 月) の新機能と変更点
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.7 の新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 8c60ba00ddcdf50c2d8897cb6d13089c3be1b9eb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009146"
---
# <a name="whats-new-or-changed-in-dynamics-365-finance-version-1007-january-2020"></a><span data-ttu-id="53c09-103">Dynamics 365 Finance バージョン 10.0.7 (2020 年 1 月) の新機能と変更点</span><span class="sxs-lookup"><span data-stu-id="53c09-103">What's new or changed in Dynamics 365 Finance version 10.0.7 (January 2020)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="53c09-104">このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.7 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="53c09-104">This topic describes features that are new or changed for Microsoft Dynamics 365 Finance, version 10.0.7.</span></span> <span data-ttu-id="53c09-105">このバージョンには 10.0.283 のビルド番号が含まれており、次のように使用できます。</span><span class="sxs-lookup"><span data-stu-id="53c09-105">This version has a build number of 10.0.283 and is available as follows:</span></span>

- <span data-ttu-id="53c09-106">プレビューリリースは 2019 年 10 月です。</span><span class="sxs-lookup"><span data-stu-id="53c09-106">Preview release is in October 2019.</span></span>
- <span data-ttu-id="53c09-107">Ga (自動更新) は 2019 年 11 月です。</span><span class="sxs-lookup"><span data-stu-id="53c09-107">General availability (self-update) is in November 2019.</span></span>
- <span data-ttu-id="53c09-108">自動更新は 2020 年 1 月です。</span><span class="sxs-lookup"><span data-stu-id="53c09-108">Auto-update is in January 2020.</span></span>

<span data-ttu-id="53c09-109">プラットフォーム更新プログラム 31 の詳細については [追加リソース](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-109">For more information about Platform update 31, see [Additional resources](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md#additional-resources).</span></span>

## <a name="budget-register-entry-enhancements"></a><span data-ttu-id="53c09-110">予算登録エントリの機能拡張</span><span class="sxs-lookup"><span data-stu-id="53c09-110">Budget register entry enhancements</span></span>

<span data-ttu-id="53c09-111">**数量のみの予算登録エントリ** 機能により、数量のみの金額の予算登録エントリを転記する機能が有効になります。</span><span class="sxs-lookup"><span data-stu-id="53c09-111">The **Budget register entries for quantity only** feature enables the ability to post a budget register entry with quantity-only amounts.</span></span> <span data-ttu-id="53c09-112">たとえば、価格が 0 で数量が 32 の予算エントリを転記すると、金額は 0 になります。</span><span class="sxs-lookup"><span data-stu-id="53c09-112">For example, you could post a budget entry of quantity 32 with a price of zero, resulting in an amount of zero.</span></span> <span data-ttu-id="53c09-113">次に、財務報告レポートのコンテキスト内でこの数量を使用し、この数量とは別に金額の計算を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-113">You can then use this quantity within the context of a financial reporting report to display a calculation of an amount divided by this quantity.</span></span> <span data-ttu-id="53c09-114">詳細については、[予算作成の概要](../budgeting/basic-budgeting-overview-configuration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-114">For more information, see [Budgeting overview](../budgeting/basic-budgeting-overview-configuration.md).</span></span> 

<span data-ttu-id="53c09-115">**予算登録エントリの金額タイプの既定値** 機能により、予算明細行の主勘定に基づいて、収益または経費に対する金額タイプの規定値を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-115">The **Budget register entries defaulting of amount type** feature enables the defaulting of amount type to revenue or expense based on the main account of the budget line.</span></span> <span data-ttu-id="53c09-116">詳細については、[予算作成の概要](../budgeting/basic-budgeting-overview-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-116">For details, see [Budgeting overview](../budgeting/basic-budgeting-overview-configuration.md) for details.</span></span> 


## <a name="ability-to-export-records-from-the-accounts-payable-invoice-pool-form"></a><span data-ttu-id="53c09-117">買掛金勘定の請求書のプール フォームからレコードをエクスポートする機能</span><span class="sxs-lookup"><span data-stu-id="53c09-117">Ability to export records from the Accounts payable invoice pool form</span></span>
<span data-ttu-id="53c09-118">この機能により、**買掛金勘定の請求のプール** フォームから Excel にレコードをエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="53c09-118">This feature lets you export records from the **Accounts payable invoice pool** form to Excel.</span></span> <span data-ttu-id="53c09-119">この能力により、Excel のグリッド データのレビューおよび分析を行うことが容易になります。</span><span class="sxs-lookup"><span data-stu-id="53c09-119">This capability makes it easier to review and analyze the grid data in Excel.</span></span> 

## <a name="ledger-settlement-by-user"></a><span data-ttu-id="53c09-120">ユーザー別の元帳決済</span><span class="sxs-lookup"><span data-stu-id="53c09-120">Ledger settlement by user</span></span>

<span data-ttu-id="53c09-121">元帳決済は、マークされたトランザクションをユーザーごとに決済するようになりました。</span><span class="sxs-lookup"><span data-stu-id="53c09-121">Ledger settlement will now settle marked transactions by user.</span></span>  <span data-ttu-id="53c09-122">ページを開くと、決済用にユーザーごとにマークされたトランザクション、またはユーザーによってマークされていないトランザクションのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-122">When opening the page, only transactions marked by the user for settlement or transactions not marked by anyone will display.</span></span> <span data-ttu-id="53c09-123">また、ユーザー ID ごとにトランザクションをクリアするための新しいボタンが導入されました。</span><span class="sxs-lookup"><span data-stu-id="53c09-123">Also, a new button has been introduced to clear transactions by user ID.</span></span>  <span data-ttu-id="53c09-124">これにより、会計マネージャーは、決済を完了する前に休暇に出かけた、または組織を離れたユーザーのトランザクションをクリアすることができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-124">This will allow an accounting manager to clear transactions for a user who might have left on vacation before finishing the settlement or for a user who has left the organization.</span></span> <span data-ttu-id="53c09-125">このアクションにより、決済用にマークするために、他のユーザーのトランザクションを確保することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-125">The action will free up those transactions for another user to mark them for settlement.</span></span> 

## <a name="forecast-position-reports-public-sector"></a><span data-ttu-id="53c09-126">予測職位のレポート (公的部門)</span><span class="sxs-lookup"><span data-stu-id="53c09-126">Forecast position reports (Public Sector)</span></span>

<span data-ttu-id="53c09-127">**予測職位の集計** レポートを使用して、指定した予算計画およびシナリオにおける予測職位情報を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-127">You can use the **Forecast position summary** report to generate forecast position information for a budget plan and scenario that you specify.</span></span> <span data-ttu-id="53c09-128">**予測職位の集計** レポートには、予測職位の原価が勘定配布ごとに表示されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-128">The **Forecast position summary** report shows forecast position costs by account distributions.</span></span> <span data-ttu-id="53c09-129">予測職位の原価は、割り当てられた勘定配布ごとにグループ化されて表示されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-129">The forecast position costs are shown, grouped by their assigned account distributions.</span></span> <span data-ttu-id="53c09-130">原価金額は、勘定配布に割り当てられている割合ごとに考慮されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-130">The cost amounts are factored by the percentage assigned to the account distribution.</span></span> 

## <a name="purchasing-cards-public-sector"></a><span data-ttu-id="53c09-131">購買カード (公的機関)</span><span class="sxs-lookup"><span data-stu-id="53c09-131">Purchasing cards (Public Sector)</span></span>

<span data-ttu-id="53c09-132">機関は購買カードを使用することにより、従業員は標準の購買要求プロセスを使用せずに商品およびサービスを調達することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-132">Agencies use purchasing cards so that employees can procure goods and services without using the standard purchase requisition process.</span></span> <span data-ttu-id="53c09-133">購買カードに関連するページおよびフィールドにより、購買を追跡するためのメカニズムが提供されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-133">The pages and fields that are related to purchasing cards provide a mechanism for tracking purchases.</span></span> <span data-ttu-id="53c09-134">従業員が購買カードを使用して行った購買はそれぞれ仕入先請求書に記録されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-134">Each purchase that an employee makes by using a purchasing card is recorded on a vendor invoice.</span></span> <span data-ttu-id="53c09-135">ただし、請求書は商品またはサービスを提供した仕入先に対して小切手または電子支払を使用して支払われません。</span><span class="sxs-lookup"><span data-stu-id="53c09-135">However, the invoice isn't paid by using a check or electronic payment to the vendor that provided the goods or services.</span></span> <span data-ttu-id="53c09-136">その代わり、このタイプの請求書はそれぞれ、購買カード サービスを提供する仕入先に支払うために作成された別の仕入先請求書に関連付けられます (つまり、金融機関)。</span><span class="sxs-lookup"><span data-stu-id="53c09-136">Instead, each invoice of this type is associated with another vendor invoice that is created to pay the vendor that provides the purchasing card services (that is, the financial institution).</span></span> <span data-ttu-id="53c09-137">購買カード サービスのプロバイダーに支払う義務のある残高について月ごとに支払いが行われる時に、カードの購買の支払いが行われます。</span><span class="sxs-lookup"><span data-stu-id="53c09-137">The card purchases are paid off when the balance that is owed to the purchasing card services provider is paid each month.</span></span>

## <a name="mark-a-purchase-agreement-as-closed"></a><span data-ttu-id="53c09-138">購買契約書を「クローズ済」としてマークする</span><span class="sxs-lookup"><span data-stu-id="53c09-138">Mark a purchase agreement as "Closed"</span></span>

<span data-ttu-id="53c09-139">ユーザーは、有効に使用されていない契約について知らせるために、購買契約書を「クローズ済」としてマークすることができるようになりました。これにより、ユーザーは購買契約書からリリース注文を作成できなくなります。</span><span class="sxs-lookup"><span data-stu-id="53c09-139">Users can now mark a purchase agreement as "Closed" to signal that the agreement is no longer actively used, making it so users will not be able to create release orders from the purchase agreement.</span></span>

## <a name="delayed-tax-calculation-on-journal"></a><span data-ttu-id="53c09-140">仕訳帳の税金計算遅延</span><span class="sxs-lookup"><span data-stu-id="53c09-140">Delayed tax calculation on journal</span></span>

<span data-ttu-id="53c09-141">この機能により、非常に多数のトランザクションが含まれている場合に、仕訳帳での税計算のパフォーマンスが改善されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-141">This feature improves the performance of tax calculations on journals when that contain a significant number of transactions.</span></span> <span data-ttu-id="53c09-142">この機能が有効になっている場合、ユーザーが **売上税** コマンドをクリックするか、仕訳帳を転記するときにのみ、税額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-142">Tax amounts will only be calculated when you click the **Sales Tax** command or when you post the journal when this feature is enabled.</span></span> <span data-ttu-id="53c09-143">詳細については、[仕訳帳の税金計算遅延の有効化](../general-ledger/enable-delayed-tax-calculation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-143">For more information, see [Enable delayed tax calculation on journal](../general-ledger/enable-delayed-tax-calculation.md).</span></span>

## <a name="reverse-journal-posting"></a><span data-ttu-id="53c09-144">仕訳帳の転記の取消</span><span class="sxs-lookup"><span data-stu-id="53c09-144">Reverse journal posting</span></span>

<span data-ttu-id="53c09-145">この機能により、転記された仕訳帳全体、またはその発生元に関係なく伝票トランザクション リストから 1 つ以上の伝票を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-145">This feature lets you reverse an entire posted journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> <span data-ttu-id="53c09-146">詳細については、[仕訳帳の転記の取消](../general-ledger/reverse-journal-posting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-146">For more information, see [Reverse journal posting](../general-ledger/reverse-journal-posting.md).</span></span>

## <a name="prohibit-submission-to-workflow-when-there-are-unallocated-charges-on-a-vendor-invoice"></a><span data-ttu-id="53c09-147">仕入先請求書に配賦されていない費用がある場合は、ワークフローへの送信を禁止する</span><span class="sxs-lookup"><span data-stu-id="53c09-147">Prohibit submission to workflow when there are unallocated charges on a vendor invoice</span></span>
<span data-ttu-id="53c09-148">この機能により、未配賦の料金が含まれている場合に仕入先請求書がワークフロー プロセスに送信されないようになります。</span><span class="sxs-lookup"><span data-stu-id="53c09-148">This feature lets you prevent a vendor invoice from being submitted to the workflow process when it contains unallocated charges.</span></span> <span data-ttu-id="53c09-149">代わりに、請求書を送信した担当者が未配賦の料金があるという警告を受け取り、ワークフローに送信する前にユーザーが修正できるようにします。</span><span class="sxs-lookup"><span data-stu-id="53c09-149">Instead, the person who submitted the invoice receives an alert that there are unallocated charges and lets the user make corrections before submitting it to workflow.</span></span>

## <a name="account-groups-selection-for-chinese-voucher-types"></a><span data-ttu-id="53c09-150">中国の伝票タイプに対する勘定グループの選択</span><span class="sxs-lookup"><span data-stu-id="53c09-150">Account groups selection for Chinese voucher types</span></span>

<span data-ttu-id="53c09-151">この機能により、中国の伝票タイプを設定する時、勘定グループを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-151">This feature allows you to select accounts groups when setting up voucher types for China.</span></span> 

### <a name="enable-the-feature"></a><span data-ttu-id="53c09-152">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="53c09-152">Enable the feature</span></span>
1. <span data-ttu-id="53c09-153">**ワークスペース > 機能の管理** で機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="53c09-153">Enable the feature in the **Workspaces > Feature management**.</span></span>
2. <span data-ttu-id="53c09-154">これにより、伝票タイプの設定が保存される新しいテーブルが導入されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-154">This introduces a new table where voucher type setup is stored.</span></span> <span data-ttu-id="53c09-155">既存の中国の伝票タイプの設定情報を新しいテーブルにコピーするには、**システム管理 > 定期処理のタスク > データベース > 整合性チェック** に移動します。</span><span class="sxs-lookup"><span data-stu-id="53c09-155">To copy existing Chinese voucher type setup information to a new table, go to **System administration > Periodic tasks > Database > Consistency check**.</span></span> <span data-ttu-id="53c09-156">**プログラム > 一般会計** を展開し、**伝票の制限タイプ** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-156">Expand **Program > General ledger** and select **Restriction type for voucher**.</span></span> 
3. <span data-ttu-id="53c09-157">**確認/修正** フィールドで **確認** を選択し、新しいテーブルをコピーするように既存の設定が設定されているかどうかを確認することができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-157">Select **Check** in the **Check/Fix** field to check whether there are settings in existing setup to copy to a new table.</span></span>
4. <span data-ttu-id="53c09-158">**確認/修正** フィールドで **修正** を選択すると、既存の設定から新しいテーブルに設定をコピーすることができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-158">Select **Fix** in the **Check/Fix** field to copy settings from an existing table to a new table.</span></span>

### <a name="set-up-voucher-type"></a><span data-ttu-id="53c09-159">伝票タイプの設定</span><span class="sxs-lookup"><span data-stu-id="53c09-159">Set up voucher type</span></span>
1. <span data-ttu-id="53c09-160">**一般会計 > 仕訳帳の設定 > 中国の伝票タイプ > 伝票タイプ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="53c09-160">Go to **General ledger > Journal setup > Chinese voucher type > Voucher type**.</span></span>
2. <span data-ttu-id="53c09-161">**ルール** クイック タブの下で、固有の制限のある明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-161">Under the **Rules** FastTab, select the line with specific restriction.</span></span>
3. <span data-ttu-id="53c09-162">**影響を受ける勘定** クイック タブの下で **追加** をクリックして、選択されたルールに対する勘定を設定します。</span><span class="sxs-lookup"><span data-stu-id="53c09-162">Under the **Impacted accounts** FastTab, click **Add** and set up the accounts for the selected rule:</span></span>
- <span data-ttu-id="53c09-163">**勘定タイプ** フィールドで、**元帳**、**顧客**、**仕入先**、**プロジェクト**、**固定資産**、**銀行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-163">In the **Account type** field, select **Ledger**, **Customer**, **Vendor**, **Project**, **Fixed assets**, **Bank**</span></span>
- <span data-ttu-id="53c09-164">**勘定コード** において、**勘定**、**グループ**、または **すべて** を選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-164">In the **Account code**, select **Account**, **Group**, or **All**.</span></span> <span data-ttu-id="53c09-165">**グループ** 値は **元帳** 勘定コードでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="53c09-165">Note that the value **Group** is not available for **Ledger** account code.</span></span>
- <span data-ttu-id="53c09-166">**勘定コード** フィールドで **グループ** を選択した場合、**勘定タイプ** の値に一致するように、**グループ番号** フィールドで、**顧客グループ**、**仕入先グループ**、**プロジェクト グループ**、**固定資産グループ**、または **銀行グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-166">In the **Group number** field, select **Customer group**, **Vendor group**, **Project group**, **Fixed asset group**, or **Bank group** to match the value in the **Account type** field, if you selected **Group** in the **Account code** field.</span></span>
- <span data-ttu-id="53c09-167">**勘定コード** フィールドで **テーブル** を選択した場合、**勘定番号** フィールドにおいて、**勘定タイプ** の値に、**勘定科目**、**顧客勘定**、**仕入先勘定**、**プロジェクト ID**、**固定資産番号**、または **銀行口座番号** をそれぞれ選択します。</span><span class="sxs-lookup"><span data-stu-id="53c09-167">In the **Account number** field, select **Ledger account**, **Customer account**, **Vendor account**, **Project ID**, **Fixed asset number**, or **Bank account value** in the **Account type** field, if you selected **Table** in the **Account code** field.</span></span>


<span data-ttu-id="53c09-168">中国の伝票タイプの設定方法に関する詳細は[中国の伝票の設定](../localizations/tasks/set-up-chinese-vouchers.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-168">For details about how to set up Chinese voucher types, see [Set up Chinese vouchers](../localizations/tasks/set-up-chinese-vouchers.md).</span></span>

## <a name="sort-by-resource-in-the-project-invoice-proposal"></a><span data-ttu-id="53c09-169">プロジェクトの仮発行請求書のリソースで並べ替え</span><span class="sxs-lookup"><span data-stu-id="53c09-169">Sort by resource in the project invoice proposal</span></span>

<span data-ttu-id="53c09-170">**プロジェクトの請求書の提案作成中のリソースによる並べ替えの有効化** 機能により、プロジェクトの経理担当者は、新しいプロジェクトの請求書提案の作成時に、請求に使えるプロジェクト トランザクションをリソースの順に並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-170">The **Enable sorting by resource during project invoice proposal creation** feature allows the project accountant to sort the project transactions available for billing by the resource when creating a new project invoice proposal.</span></span> <span data-ttu-id="53c09-171">使用可能なプロジェクト取引を表示するグリッドには、リソース ID とリソースのための別のフィールドがあります。これにより、ユーザーは、リソース名に対してフィルタ処理や並べ替えを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-171">The grid displaying the available project transactions will have a separate field for Resource ID and Resource, allowing the user to filter and sort on the resource name.</span></span> <span data-ttu-id="53c09-172">この機能は既定で無効になっており、**ワークスぺース > 機能管理** で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="53c09-172">This feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span>

## <a name="run-settle-and-post-sales-tax-in-batch-mode"></a><span data-ttu-id="53c09-173">バッチ モードでの消費税の決済と転記の実行</span><span class="sxs-lookup"><span data-stu-id="53c09-173">Run Settle and post sales tax in batch mode</span></span> 

<span data-ttu-id="53c09-174">ユーザーは、イタリア、ベルギーおよびオーストラリアで、**決済と売上税の転記** をバッチ モードで実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="53c09-174">Users can now run **Settle and post sales tax** in batch mode in Italy, Belgium, and Australia.</span></span> <span data-ttu-id="53c09-175">設定情報の詳細については、[売上税決済期間の設定](../general-ledger/tasks/set-up-sales-tax-settlement-periods.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-175">Refer to [Set up sales tax settlement periods](../general-ledger/tasks/set-up-sales-tax-settlement-periods.md) for setup information.</span></span> 

## <a name="tax-engine"></a><span data-ttu-id="53c09-176">税エンジン</span><span class="sxs-lookup"><span data-stu-id="53c09-176">Tax engine</span></span> 

<span data-ttu-id="53c09-177">税エンジン (GTE) は、現在のみインドのみで使用可能となっています。</span><span class="sxs-lookup"><span data-stu-id="53c09-177">The tax engine (GTE) is currently only available for India.</span></span> 

### <a name="create-tax-component-with-pre-defined-rules"></a><span data-ttu-id="53c09-178">事前定義済ルールを使用した税コンポーネントの作成</span><span class="sxs-lookup"><span data-stu-id="53c09-178">Create tax component with pre-defined rules</span></span>

<span data-ttu-id="53c09-179">新しい税コンポーネントを作成する代わりに、ユーザーは、逆請求および非控除などの、よく使用される課税ルールをサポートする事前定義済の税ルールを作成できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="53c09-179">Instead of creating a new tax component, users can now create it with predefined tax rules that support the most commonly used taxation rules like reverse charge and non-deductible.</span></span> <span data-ttu-id="53c09-180">詳細については、[税コンポーネントの作成](../localizations/tax-engine-create-tax-component.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-180">For more information, see [Create tax component](../localizations/tax-engine-create-tax-component.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="53c09-181">追加リソース</span><span class="sxs-lookup"><span data-stu-id="53c09-181">Additional resources</span></span>

### <a name="platform-update-31"></a><span data-ttu-id="53c09-182">プラットフォーム update 31</span><span class="sxs-lookup"><span data-stu-id="53c09-182">Platform update 31</span></span>

<span data-ttu-id="53c09-183">Microsoft Dynamics 365 Finance 10.0.7 には、プラットフォーム更新プログラム 31 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53c09-183">Microsoft Dynamics 365 Finance 10.0.7 includes Platform update 31.</span></span> <span data-ttu-id="53c09-184">詳細については、[プラットフォーム更新プログラム 31 の新機能と変更点](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-184">To learn more, see [What's new and changed in Platform update 31](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-31.md).</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="53c09-185">バグ修正</span><span class="sxs-lookup"><span data-stu-id="53c09-185">Bug fixes</span></span> 
<span data-ttu-id="53c09-186">10.0.7 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53c09-186">For information about the bug fixes included in each of the updates that are part of 10.0.7, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493).</span></span>


### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="53c09-187">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="53c09-187">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="53c09-188">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="53c09-188">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="53c09-189">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="53c09-189">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="53c09-190">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="53c09-190">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="53c09-191">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="53c09-191">Removed and deprecated features</span></span>

<span data-ttu-id="53c09-192">[削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="53c09-192">The [Removed or deprecated features](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="53c09-193">*削除された* 機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="53c09-193">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="53c09-194">*削除予定* の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="53c09-194">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="53c09-195">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="53c09-195">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="53c09-196">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="53c09-196">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="53c09-197">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="53c09-197">Typically, these are functional updates that need to be made to the compiler.</span></span>

