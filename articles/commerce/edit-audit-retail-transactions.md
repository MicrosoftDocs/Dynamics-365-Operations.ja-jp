---
title: 小売店舗トランザクションの編集と監査
description: このトピックでは、店舗トランザクションを編集および監査するための機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 97211ee36dbaa704d3a967e9b742ff1cae708707
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004392"
---
# <a name="edit-and-audit-retail-store-transactions"></a><span data-ttu-id="04b0c-103">小売店舗トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="04b0c-103">Edit and audit retail store transactions</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="04b0c-104">Dynamics 365 Commerce のお客様は、サード パーティの販売時点管理 (POS) アプリケーションの他に、ファースト パーティのアプリケーションも使用します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-104">Dynamics 365 Commerce customers use first-party as well as third-party point of sale (POS) applications.</span></span> <span data-ttu-id="04b0c-105">ファースト パーティの POS アプリケーションを使用すると、店舗トランザクションは、バッチ処理を通じてチャンネルから Headquarters に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-105">With the first-party POS application, store transactions are pulled into Headquarters from the channels through a batch process.</span></span> <span data-ttu-id="04b0c-106">サード パーティのアプリケーションを使用すると、トランザクションは統合によって Headquarters に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-106">With third-party applications, transactions are pulled into Headquarters through integration.</span></span> <span data-ttu-id="04b0c-107">どちらの場合も、トランザクションを Headquarters に取り込んでから、トランザクションに対して複数の検証を実行する整合性チェック プロセスを実行します。そうすると、正常に検証されたトランザクションのみが Headquarters に転記される明細書に取り込まれます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-107">In both cases, after transactions are pulled into Headquarters, a consistency check process needs to be executed that runs multiple validations on the transactions so that only successfully validated transactions are pulled into the statement to be posted in Headquarters.</span></span> 

<span data-ttu-id="04b0c-108">さまざまな理由でコマース トランザクションの検証が失敗することがあります。</span><span class="sxs-lookup"><span data-stu-id="04b0c-108">Commerce transactions fail validation for various reasons.</span></span> <span data-ttu-id="04b0c-109">たとえば、統合コードまたは POS のアプリケーションのバグにより、矛盾したデータが発生したり、製品をチャネルと同期してから削除したり、その期間のトランザクションを転記せずに会計年度期間を決算したりするなどのユーザー エラーが発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="04b0c-109">For example, a bug in the integration code or a bug in the POS application may cause inconsistent data, or a user error, such as deleting a product after it was synchronized to the channel or closing a fiscal period without posting transactions for that period, can cause inconsistent data.</span></span>

<span data-ttu-id="04b0c-110">これらのトランザクションにフラグが設定され明細書から除外されますが、トランザクションは、お客様が日々の売上を財務に転記する日々のプロセスを妨害する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="04b0c-110">While these transactions get flagged and are excluded from the statements, the transactions can disrupt a customer’s daily process of posting daily sales to the financials.</span></span>

<span data-ttu-id="04b0c-111">Commerce では、すべての変更の監査を管理しながら、検証に合格しなかった特定の小売トランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-111">In Commerce, you can edit the specific transactions that fail validation while maintaining audit of all the changes.</span></span> 

## <a name="edit-and-audit-transactions"></a><span data-ttu-id="04b0c-112">トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="04b0c-112">Edit and audit transactions</span></span>

<span data-ttu-id="04b0c-113">Retail バージョン 10.0.5 では、売上や返品のような現金売りトランザクションのみ編集できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-113">In Retail version 10.0.5, cash and carry transactions like sales and returns are the only transactions that can be edited.</span></span> <span data-ttu-id="04b0c-114">顧客注文やオンライン注文の編集はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="04b0c-114">Editing customer orders or online orders is not supported.</span></span> <span data-ttu-id="04b0c-115">Retail バージョン 10.0.6 では、現金管理トランザクションの編集もサポートされています。</span><span class="sxs-lookup"><span data-stu-id="04b0c-115">In Retail version 10.0.6 and higher, editing cash management transactions is also supported.</span></span>

1. <span data-ttu-id="04b0c-116">Dynamics Excel アドインをインストールします。</span><span class="sxs-lookup"><span data-stu-id="04b0c-116">Install the Dynamics Excel Add-in.</span></span>

2. <span data-ttu-id="04b0c-117">**店舗の財務** ワークスペースに移動します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-117">Go to the **Store financials** workspace.</span></span> <span data-ttu-id="04b0c-118">**"トランザクションの検証エラー"** タイルでは、1 つ以上の検証ルールに当てはまらなかった、トランザクション フォームの事前にフィルターされたビューが使用できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-118">The **Transaction validation failures** tile provides a pre-filtered view of the transaction form that failed one or more of the validation rules.</span></span>
 
3. <span data-ttu-id="04b0c-119">フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-119">Open the form.</span></span> <span data-ttu-id="04b0c-120">検証に失敗したレコード、**Office アドイン**、**選択したトランザクションの編集**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="04b0c-120">Click the record that failed validation, click **Office Add in**, and then click **Edit selected transaction**.</span></span> <span data-ttu-id="04b0c-121">選択したトランザクションの詳細を含む Excel ファイルを開くと、次のワークシートが表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-121">An Excel file with the details of the selected transaction opens, with the following worksheets:</span></span>

    - <span data-ttu-id="04b0c-122">行: このワークシートでは、トランザクションのヘッダーや製品行、関連データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-122">Lines: This worksheet has the header and product lines and related data for the transaction.</span></span>
    - <span data-ttu-id="04b0c-123">支払: このワークシートでは、トランザクションの支払行の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-123">Payments: This worksheet has the details of the payment lines for the transaction.</span></span>
    - <span data-ttu-id="04b0c-124">割引: このワークシートでは、トランザクションの割引に関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-124">Discounts: This worksheet has the discount-related details for the transaction.</span></span>
    - <span data-ttu-id="04b0c-125">税金: このワークシートでは、トランザクションの税金に関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-125">Taxes: This worksheet has the tax-related details for the transaction.</span></span>
    - <span data-ttu-id="04b0c-126">諸費用: このワークシートでは、トランザクションの諸費用に関する詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-126">Charges: This worksheet has the charges-related data for the transaction.</span></span>

4. <span data-ttu-id="04b0c-127">Excel ファイルでは、適切なフィールドを変更してから Dynamics Excel アドインの発行機能を使用して、データを Headquarters に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-127">In the Excel file, you modify the appropriate fields and then upload the data back into Headquarters using the Dynamics Excel Add-in publish functionality.</span></span> <span data-ttu-id="04b0c-128">公開後、変更はシステムに反映されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-128">Once published, the changes will be reflected in the system.</span></span> <span data-ttu-id="04b0c-129">公開時には、ユーザーが行った変更に対する検証は行われません。</span><span class="sxs-lookup"><span data-stu-id="04b0c-129">During publish, no validation is done on changes that users make.</span></span>

5. <span data-ttu-id="04b0c-130">変更の完全な監査証跡を表示するには、ヘッダーレベル変更用の **小売トランザクション** のヘッダー、および適切なトランザクション ページの該当するセクションやレコードにある **監査追跡の表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04b0c-130">A complete audit trail of the changes can be viewed by clicking **View audit trail** in the **Retail transaction** header for the header-level changes and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="04b0c-131">たとえば、販売行に関するすべての変更が **販売トランザクション** ページに表示され、支払に関連する変更は、**支払トランザクション** ページに表示されます。変更用に管理されている監査の詳細は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="04b0c-131">For example, all changes relating to sales lines will be visible on the **Sales transactions** page, changes relating to payments will be visible on the **Payment transactions** page, etc. The audit details that are maintained for the changes are as follows.</span></span>

   - <span data-ttu-id="04b0c-132">変更日時</span><span class="sxs-lookup"><span data-stu-id="04b0c-132">Modified date and time</span></span>
   - <span data-ttu-id="04b0c-133">フィールド</span><span class="sxs-lookup"><span data-stu-id="04b0c-133">Field</span></span> 
   - <span data-ttu-id="04b0c-134">元の値</span><span class="sxs-lookup"><span data-stu-id="04b0c-134">Old value</span></span>
   - <span data-ttu-id="04b0c-135">新しい値</span><span class="sxs-lookup"><span data-stu-id="04b0c-135">New value</span></span>
   - <span data-ttu-id="04b0c-136">変更者</span><span class="sxs-lookup"><span data-stu-id="04b0c-136">Modified by</span></span>

6. <span data-ttu-id="04b0c-137">変更して公開した後、**店舗トランザクションの検証** オプションを再度実行して、実行した変更に一貫性があり有効であるかを検証します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-137">After your changes are made and published, run the **Validate store transactions** option again to validate that the changes you made are consistent and valid.</span></span>

> [!NOTE]
> <span data-ttu-id="04b0c-138">検証に失敗したトランザクションのみを編集できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-138">You can only edit transactions that failed validation.</span></span> <span data-ttu-id="04b0c-139">検証に合格したトランザクションを編集する場合は、変更するトランザクションの検証状態を **エラー** または **なし** に変更します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-139">If you want to edit transactions that passed validation, change the validation status of the transaction you want to change to **Error** or **None** and then you will be able to edit it.</span></span> 


## <a name="bulk-edit-transactions"></a><span data-ttu-id="04b0c-140">トランザクションの一括編集</span><span class="sxs-lookup"><span data-stu-id="04b0c-140">Bulk edit transactions</span></span>

<span data-ttu-id="04b0c-141">Retail バージョン 10.0.6 およびそれ以降のバージョンでは、明細書レベルでトランザクションを一括編集できるオプションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="04b0c-141">In Retail version 10.0.6 and higher, the option to bulk edit transactions at a statement level is supported.</span></span> 

1. <span data-ttu-id="04b0c-142">Excel アドインを使用して変更するトランザクションを含む明細書を開くには、上記のステップ 1 から 3 を実行します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-142">Use the Excel Add-in to open a statement that has transactions you want to modify using steps 1-3 above.</span></span>

2. <span data-ttu-id="04b0c-143">以下のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="04b0c-143">Choose one of the options below.</span></span>

    - <span data-ttu-id="04b0c-144">**現金売りトランザクションの編集**。</span><span class="sxs-lookup"><span data-stu-id="04b0c-144">**Edit cash and carry transactions**.</span></span> <span data-ttu-id="04b0c-145">このオプションを使用すると、明細書にあるすべての現金売りトランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-145">This option enables you to edit all the cash and carry transactions included in the statement.</span></span> <span data-ttu-id="04b0c-146">次の Excel ワークシートは使用可能です。</span><span class="sxs-lookup"><span data-stu-id="04b0c-146">The following Excel worksheets are available.</span></span>
    
       - <span data-ttu-id="04b0c-147">**トランザクション**: このワークシートでは、販売トランザクションのヘッダーレベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-147">**Transaction**: This worksheet has all the header-level information for the sales transactions.</span></span>
       - <span data-ttu-id="04b0c-148">**販売トランザクション**: このワークシートでは、販売トランザクションの行レベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-148">**Sales transaction**: This worksheet has all the lines-level information for the sales transactions.</span></span>
       - <span data-ttu-id="04b0c-149">**支払トランザクション**: このワークシートでは、販売トランザクションの支払行レベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-149">**Payment transactions**: This worksheet has all the payment lines information for the sales transactions.</span></span>
       - <span data-ttu-id="04b0c-150">**割引トランザクション**: このワークシートでは、販売トランザクションの割引行レベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-150">**Discount transactions**: This worksheet has all the discount lines information for the sales transactions.</span></span>
       - <span data-ttu-id="04b0c-151">**税金トランザクション**: このワークシートでは、販売トランザクションの税金行レベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-151">**Tax transactions**: This worksheet has all the tax lines information for the sales transactions.</span></span>
       - <span data-ttu-id="04b0c-152">**諸費用トランザクション**: このワークシートでは、販売トランザクションの諸費用行レベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-152">**Charge transactions**: This worksheet has all the charge lines information for the sales transactions.</span></span>

    - <span data-ttu-id="04b0c-153">**現金管理トランザクションの編集**。</span><span class="sxs-lookup"><span data-stu-id="04b0c-153">**Edit cash management transactions**.</span></span> <span data-ttu-id="04b0c-154">このオプションを使用すると、明細書にあるすべての現金管理トランザクションを編集できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-154">This option enables you to edit all the cash management transactions included in the statement.</span></span> <span data-ttu-id="04b0c-155">次の Excel ワークシートは使用可能です。</span><span class="sxs-lookup"><span data-stu-id="04b0c-155">The following Excel worksheets are available.</span></span>
     
       - <span data-ttu-id="04b0c-156">**トランザクション**: このワークシートでは、現金管理トランザクションのヘッダーレベルの情報がすべて表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-156">**Transaction**: This worksheet has all the header-level information for the cash management transactions.</span></span>
       - <span data-ttu-id="04b0c-157">**銀行支払/入金トランザクション**: このワークシートでは、すべての銀行入金トランザクションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-157">**Bank tender transactions**: This worksheet has all the bank drop transaction details.</span></span>
       - <span data-ttu-id="04b0c-158">**金庫保管支払/入金トランザクション**: このワークシートでは、すべての金庫保管入金トランザクションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-158">**Safe tender transactions**: This worksheet has all the safe drop transaction details.</span></span>
       - <span data-ttu-id="04b0c-159">**支払/入金申告**: このワークシートでは、すべての支払/入金申告トランザクションの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-159">**Tender declaration**: This worksheet has all the tender declaration transaction details.</span></span>
       - <span data-ttu-id="04b0c-160">**収入および経費トランザクション**: このワークシートでは、すべての収入および経費トランザクションの明細行の詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-160">**Income-expense transaction**: This worksheet has all the income-expense transaction line details.</span></span>
       - <span data-ttu-id="04b0c-161">**支払トランザクション**: このワークシートでは、**請求書の支払** 処理と収入および経費トランザクションの支払いに関連する情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-161">**Payment transactions**: This worksheet has all the payment-related information for the **Pay invoice** operation as well as the income-expense transaction.</span></span>

3.  <span data-ttu-id="04b0c-162">編集されたトランザクションを一括公開する場合、検証は実行されません。</span><span class="sxs-lookup"><span data-stu-id="04b0c-162">Validations are not performed when you publish bulk edited transactions.</span></span> <span data-ttu-id="04b0c-163">すべての編集が正確であることを確認し、ワークシート全体のデータの忠実性を維持する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b0c-163">You must ensure that all your edits are accurate and the fidelity of data across the worksheets is maintained.</span></span> <span data-ttu-id="04b0c-164">たとえば、未処理のトランザクションの会計期間または在庫期間が終了するシナリオを管理するためにトランザクションの日付を変更する場合は、**営業日** 列を含むすべての Excel ワークシートの日付を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04b0c-164">For example, if you want to change the transaction date to manage the scenarios where the fiscal or inventory period for the open transactions is closed, you need to change the date on all the Excel worksheets that have the **Business date** column.</span></span> <span data-ttu-id="04b0c-165">**明細書** ページにある **再検証トランザクション** から編集されたトランザクションを検証できます。</span><span class="sxs-lookup"><span data-stu-id="04b0c-165">To validate transactions after they have been edited, you can use **Revalidate transactions** on the **Statements** page.</span></span>
