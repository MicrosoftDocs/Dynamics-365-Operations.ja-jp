---
title: 現金売りトランザクションと現金管理トランザクションの編集と監査
description: このトピックでは、Microsoft Dynamics 365 Commerce で現金売りトランザクションと現金管理トランザクションを編集および監査する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 296dbf03ed65c1994562149a2c4b8fccd9073f0d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221922"
---
# <a name="edit-and-audit-cash-and-carry-and-cash-management-transactions"></a><span data-ttu-id="feac7-103">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="feac7-103">Edit and audit cash and carry and cash management transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="feac7-104">このトピックでは、Microsoft Dynamics 365 Commerce で現金売りトランザクションと現金管理トランザクションを編集および監査する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="feac7-104">This topic describes how to edit and audit cash and carry and cash management transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="feac7-105">概要</span><span class="sxs-lookup"><span data-stu-id="feac7-105">Overview</span></span>

<span data-ttu-id="feac7-106">Dynamics 365 Commerce のお客様は、ファースト パーティの販売時点管理 (POS) アプリケーションとサード パーティの POS アプリケーションの両方を使用します。</span><span class="sxs-lookup"><span data-stu-id="feac7-106">Dynamics 365 Commerce customers use both a first-party point of sale (POS) application and third-party POS applications.</span></span> <span data-ttu-id="feac7-107">ファースト パーティのアプリケーションの場合、店舗トランザクションは、バッチ処理を通じてチャンネルから Commerce 本社に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-107">In the case of the first-party application, store transactions are pulled into Commerce headquarters from the channels through a batch process.</span></span> <span data-ttu-id="feac7-108">サード パーティのアプリケーションの場合、トランザクションは統合によって Commerce 本社に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-108">In the case of third-party applications, transactions are pulled into Commerce headquarters through integration.</span></span> <span data-ttu-id="feac7-109">どちらの場合も、トランザクションを Commerce 本社に取り込んだ後に、整合性チェックプロセスを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="feac7-109">In both cases, after transactions are pulled into Commerce headquarters, a consistency check process must be performed.</span></span> <span data-ttu-id="feac7-110">このプロセスでは、トランザクションに対して複数の検証が実行され、正常に検証されたトランザクションのみが、Commerce 本社に転記できるように明細書に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-110">This process runs multiple validations on the transactions, and only transactions that are successfully validated are pulled into the statement so that they can be posted in Commerce headquarters.</span></span>

<span data-ttu-id="feac7-111">さまざまな理由でコマース トランザクションの検証が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="feac7-111">Commerce transactions might fail validation for various reasons.</span></span> <span data-ttu-id="feac7-112">統合コードまたは POS アプリケーションのバグにより、データ不整合が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="feac7-112">A bug in the integration code or in the POS application might cause inconsistent data.</span></span> <span data-ttu-id="feac7-113">また、ユーザー エラーによってデータ不整合が発生することもあります。</span><span class="sxs-lookup"><span data-stu-id="feac7-113">Alternatively, a user error might cause inconsistent data.</span></span> <span data-ttu-id="feac7-114">たとえば、ユーザーがチャネルに同期された後に製品を削除したり、ユーザーがその期間のトランザクションを転記せずに会計年度期間を締めたとします。</span><span class="sxs-lookup"><span data-stu-id="feac7-114">For example, a user deletes a product after it was synced to the channel, or a user closes a fiscal period without posting transactions for that period.</span></span> <span data-ttu-id="feac7-115">これらのトランザクションにフラグが設定され明細書から除外されますが、お客様が日々の売上を財務に転記する日々のプロセスを妨害する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="feac7-115">Although these transactions are flagged and are excluded from the statements, they can disrupt a customer's daily process of posting daily sales to the financials.</span></span> <span data-ttu-id="feac7-116">Commerce では、すべての変更の監査を管理しながら、検証に失敗したトランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-116">In Commerce, you can edit the transactions that fail validation while you also maintain an audit of all the changes.</span></span>

## <a name="edit-transactions"></a><span data-ttu-id="feac7-117">トランザクションの編集</span><span class="sxs-lookup"><span data-stu-id="feac7-117">Edit transactions</span></span>

<span data-ttu-id="feac7-118">Commerce バージョン 10.0.5 では、売上や返品のような現金売りトランザクションのみ編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-118">In Commerce version 10.0.5, the only transactions that can be edited are cash and carry transactions, such as sales and returns.</span></span> <span data-ttu-id="feac7-119">顧客注文とオンライン注文は編集できません。</span><span class="sxs-lookup"><span data-stu-id="feac7-119">Customer orders and online orders can't be edited.</span></span> <span data-ttu-id="feac7-120">Commerce バージョン 10.0.6 では、現金管理トランザクションも編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-120">In Commerce version 10.0.6 and later, cash management transactions can also be edited.</span></span>

<span data-ttu-id="feac7-121">Commerce 本社でトランザクションを編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feac7-121">To edit transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="feac7-122">[Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="feac7-122">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="feac7-123">Commerce 本社で、**店舗の財務** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="feac7-123">In Commerce headquarters, open the **Store financials** workspace.</span></span> <span data-ttu-id="feac7-124">**トランザクションの検証エラー** タイルでは、1 つ以上の検証ルールに当てはまらなかった、トランザクション ページの事前にフィルターされたビューが使用できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-124">The **Transaction validation failures** tile provides a prefiltered view of the transaction page that failed one or more validation rules.</span></span>
1. <span data-ttu-id="feac7-125">トランザクション ページを開き、検証に失敗したレコードを選択し、**Office アドイン**、**選択したトランザクションの編集** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-125">Open the transaction page, select the record that failed validation, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="feac7-126">選択したトランザクションの詳細を示す Excel ファイルが開きます。</span><span class="sxs-lookup"><span data-stu-id="feac7-126">An Excel file that shows the details of the selected transaction is opened.</span></span> <span data-ttu-id="feac7-127">このファイルには、次のワークシートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-127">This file contains the following worksheets:</span></span>

    - <span data-ttu-id="feac7-128">**明細行** – このワークシートには、トランザクションのヘッダーや製品明細行と、トランザクションの関連データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="feac7-128">**Lines** – This worksheet has the header and product lines for the transaction, and related data for the transaction.</span></span>
    - <span data-ttu-id="feac7-129">**支払** – このワークシートには、トランザクションの支払明細行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-129">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="feac7-130">**割引** – このワークシートには、トランザクションの割引に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-130">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="feac7-131">**税金** – このワークシートには、トランザクションの税金に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-131">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="feac7-132">**諸費用** – このワークシートには、トランザクションの諸費用に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-132">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="feac7-133">Excel ファイルで適切なフィールドを変更してから、Dynamics Excel アドインの公開機能を使用してデータをアップロードして Commerce 本社に戻します。</span><span class="sxs-lookup"><span data-stu-id="feac7-133">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="feac7-134">データの公開後、変更がシステムに反映されます。</span><span class="sxs-lookup"><span data-stu-id="feac7-134">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="feac7-135">公開時には、ユーザーが行った変更に対する検証は行われません。</span><span class="sxs-lookup"><span data-stu-id="feac7-135">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="feac7-136">変更の完全な監査証跡を表示するには、ヘッダーレベル変更用の **小売トランザクション** ヘッダー、および適切なトランザクション ページの該当するセクションやレコードにある **監査追跡の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-136">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="feac7-137">たとえば、販売明細行に関連するすべての変更は、**販売トランザクション** ページに表示され、支 に関連するすべての変更は、**支払トランザクション** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="feac7-137">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="feac7-138">変更については、次の監査の詳細が維持されます。</span><span class="sxs-lookup"><span data-stu-id="feac7-138">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="feac7-139">変更日時</span><span class="sxs-lookup"><span data-stu-id="feac7-139">Modified date and time</span></span>
    - <span data-ttu-id="feac7-140">フィールド</span><span class="sxs-lookup"><span data-stu-id="feac7-140">Field</span></span>
    - <span data-ttu-id="feac7-141">元の値</span><span class="sxs-lookup"><span data-stu-id="feac7-141">Old value</span></span>
    - <span data-ttu-id="feac7-142">新しい値</span><span class="sxs-lookup"><span data-stu-id="feac7-142">New value</span></span>
    - <span data-ttu-id="feac7-143">変更者</span><span class="sxs-lookup"><span data-stu-id="feac7-143">Modified by</span></span>

1. <span data-ttu-id="feac7-144">変更して公開した後、**店舗トランザクションの検証** を度実行して、それらの変更に一貫性があり有効であるかを検証します。</span><span class="sxs-lookup"><span data-stu-id="feac7-144">After you've made and published your changes, run **Validate store transactions** to validate that those changes are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="feac7-145">検証に失敗したトランザクションのみを編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-145">You can edit only transactions that failed validation.</span></span> <span data-ttu-id="feac7-146">検証に合格したトランザクションを編集する場合は、トランザクションの検証状態を **エラー** または **なし** に変更して、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="feac7-146">If you want to edit a transaction that passed validation, change the validation status of the transaction to **Error** or **None**, and then publish the change.</span></span> <span data-ttu-id="feac7-147">その後、トランザクションのヘッダーまたはその他の子レコードのデータを編集して、ヘッダーまたはレコードを公開できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-147">You can then edit the data on the header or in any other child records of the transaction, and publish the header or records.</span></span>

## <a name="bulk-edit-transactions-that-are-linked-to-a-statement"></a><span data-ttu-id="feac7-148">明細書にリンクされているトランザクションの一括編集</span><span class="sxs-lookup"><span data-stu-id="feac7-148">Bulk-edit transactions that are linked to a statement</span></span>

<span data-ttu-id="feac7-149">Commerce バージョン 10.0.6 以降のバージョンでは、明細書レベルでトランザクションを一括編集できるオプションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="feac7-149">Commerce version 10.0.6 and later support the option to bulk-edit transactions at the statement level.</span></span>

<span data-ttu-id="feac7-150">Commerce 本社で明細書にリンクされているトランザクションを一括編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feac7-150">To bulk-edit transactions that are linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="feac7-151">**明細書** ページを開き、編集が必要なトランザクションを含む明細書を選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-151">Open the **Statements** page, and select the statement that contains the transactions that must be edited.</span></span>
1. <span data-ttu-id="feac7-152">**Microsoft Office で開く** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-152">Select the **Open in Microsoft Office** button.</span></span>
1. <span data-ttu-id="feac7-153">編集する対象に応じて、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-153">Depending on what must be edited, select one of the following options:</span></span>

    - <span data-ttu-id="feac7-154">**現金売りトランザクションの編集** – このオプションを選択すると、明細書に含まれるすべての現金売りトランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-154">**Edit cash and carry transactions** – This option lets you edit all the cash and carry transactions that are included in the statement.</span></span> <span data-ttu-id="feac7-155">次の Excel ワークシートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-155">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="feac7-156">**トランザクション** – このワークシートには、販売トランザクションのヘッダーレベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-156">**Transaction** – This worksheet has all the header-level information for the sales transactions.</span></span>
        - <span data-ttu-id="feac7-157">**販売トランザクション** – このワークシートには、販売トランザクションの行レベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-157">**Sales transaction** – This worksheet has all the line-level information for the sales transactions.</span></span>
        - <span data-ttu-id="feac7-158">**支払トランザクション** – このワークシートには、販売トランザクションの支払行レベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-158">**Payment transactions** – This worksheet has all the payment line information for the sales transactions.</span></span>
        - <span data-ttu-id="feac7-159">**割引トランザクション** – このワークシートには、販売トランザクションの割引行レベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-159">**Discount transactions** – This worksheet has all the discount line information for the sales transactions.</span></span>
        - <span data-ttu-id="feac7-160">**税金トランザクション** – このワークシートには、販売トランザクションの税金行レベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-160">**Tax transactions** – This worksheet has all the tax line information for the sales transactions.</span></span>
        - <span data-ttu-id="feac7-161">**諸費用トランザクション** – このワークシートには、販売トランザクションの諸費用行レベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-161">**Charge transactions** – This worksheet has all the charge line information for the sales transactions.</span></span>

    - <span data-ttu-id="feac7-162">**現金管理トランザクションの編集** – このオプションを選択すると、明細書に含まれるすべての現金管理トランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-162">**Edit cash management transactions** – This option lets you edit all the cash management transactions that are included in the statement.</span></span> <span data-ttu-id="feac7-163">次の Excel ワークシートを使用できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-163">The following Excel worksheets are available:</span></span>

        - <span data-ttu-id="feac7-164">**トランザクション** – このワークシートには、現金管理トランザクションのヘッダーレベルの情報がすべて含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-164">**Transaction** – This worksheet has all the header-level information for the cash management transactions.</span></span>
        - <span data-ttu-id="feac7-165">**銀行支払/入金トランザクション** – このワークシートには、すべての銀行入金トランザクションの詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-165">**Bank tender transactions** – This worksheet has all the bank drop transaction details.</span></span>
        - <span data-ttu-id="feac7-166">**金庫保管支払/入金トランザクション** – このワークシートには、すべての金庫保管入金トランザクションの詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-166">**Safe tender transactions** – This worksheet has all the safe drop transaction details.</span></span>
        - <span data-ttu-id="feac7-167">**支払/入金申告** – このワークシートには、すべての支払/入金申告トランザクションの詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-167">**Tender declaration** – This worksheet has all the tender declaration transaction details.</span></span>
        - <span data-ttu-id="feac7-168">**収入および経費トランザクション** – このワークシートには、すべての収入および経費トランザクションの明細行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-168">**Income-expense transaction** – This worksheet has all the income-expense transaction line details.</span></span>
        - <span data-ttu-id="feac7-169">**支払トランザクション** – このワークシートには、**請求書の支払** 処理と収入および経費トランザクションの支払いに関連する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="feac7-169">**Payment transactions** – This worksheet has all the payment-related information for the **Pay invoice** operation and the income-expense transaction.</span></span>

1. <span data-ttu-id="feac7-170">必要なトランザクションを編集します。</span><span class="sxs-lookup"><span data-stu-id="feac7-170">Edit the required transactions.</span></span>

    > [!NOTE]
    > <span data-ttu-id="feac7-171">編集されたトランザクションを一括公開する場合、検証は実行されません。</span><span class="sxs-lookup"><span data-stu-id="feac7-171">Validations aren't done when you publish bulk-edited transactions.</span></span> <span data-ttu-id="feac7-172">すべての編集が正確であることを確認し、ワークシート全体のデータの忠実性を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="feac7-172">You must make sure that all your edits are accurate, and that the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="feac7-173">たとえば、未処理のトランザクションの会計期間または在庫期間が終了するシナリオを管理できるようにトランザクションの日付を変更する場合は、**営業日** 列を含むすべての Excel ワークシートの日付を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="feac7-173">For example, if you want to change the transaction date, so that you can manage scenarios where the fiscal or inventory period for the open transactions is closed, you must change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="feac7-174">**明細書** ページにある **再検証トランザクション** を選択して、編集されたトランザクションを検証できます。</span><span class="sxs-lookup"><span data-stu-id="feac7-174">To validate transactions after they have been edited, you can select **Revalidate transactions** on the **Statements** page.</span></span> <span data-ttu-id="feac7-175">検証ジョブの実行が完了するまで待ってから、明細書を転記してください。</span><span class="sxs-lookup"><span data-stu-id="feac7-175">Wait for the validation job to finish running before you post the statement.</span></span>

1. <span data-ttu-id="feac7-176">集計が既に生成されている場合は、**集計トランザクション** ページを開き、**販売注文 xml の再生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-176">If the aggregation has already been generated, open the **Aggregated transactions** page, and select **Regenerate sales order xml**.</span></span>

## <a name="bulk-edit-transactions-that-arent-linked-to-a-statement"></a><span data-ttu-id="feac7-177">明細書にリンクされていないトランザクションの一括編集</span><span class="sxs-lookup"><span data-stu-id="feac7-177">Bulk-edit transactions that aren't linked to a statement</span></span>

<span data-ttu-id="feac7-178">Commerce バージョン 10.0.10 以降では、明細書にリンクされていない検証に失敗したトランザクションを一括編集するためのオプションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="feac7-178">Commerce version 10.0.10 and later support the option to bulk-edit transactions that fail validation but aren't linked to a statement.</span></span>

<span data-ttu-id="feac7-179">Commerce 本社で明細書にリンクされていないトランザクションを一括編集するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="feac7-179">To bulk-edit transactions that aren't linked to a statement in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="feac7-180">**すべての店舗** ページを開き、トランザクションの編集が必要な店舗を選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-180">Open the **All stores** page, and select the store that transactions must be edited for.</span></span>
1. <span data-ttu-id="feac7-181">**Microsoft Office で開く** ボタンを選択し、**現金売りトランザクションの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="feac7-181">Select the **Open in Microsoft Office** button, and then select **Edit cash and carry transactions**.</span></span>
1. <span data-ttu-id="feac7-182">必要なトランザクションを編集し、公開します。</span><span class="sxs-lookup"><span data-stu-id="feac7-182">Edit the required transactions, and then publish them.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="feac7-183">追加リソース</span><span class="sxs-lookup"><span data-stu-id="feac7-183">Additional resources</span></span>

[<span data-ttu-id="feac7-184">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="feac7-184">Edit and audit online order and asynchronous customer order transactions</span></span>](edit-order-trans.md)

[<span data-ttu-id="feac7-185">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="feac7-185">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="feac7-186">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="feac7-186">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="feac7-187">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="feac7-187">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]