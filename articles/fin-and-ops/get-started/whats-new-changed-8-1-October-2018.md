---
title: "Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) の新機能および変更された機能"
description: "このトピックでは、Dynamics 365 for Finance and Operations バージョン 8.1 の新機能または変更された機能について説明します。 このバージョンは 2018 年 10 月にリリースされました。"
author: tonyafehr
manager: AnnBe
ms.date: 10/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: 
ms.assetid: b264a51c-52d1-45c5-b698-64c5242c592a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: Release 8.1
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 80794240825262b1e31896d2181a47e9eb2a45c6
ms.contentlocale: ja-jp
ms.lasthandoff: 10/02/2018

---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-version-81-october-2018"></a><span data-ttu-id="4b30b-104">Dynamics 365 for Finance and Operations バージョン 8.1 (2018 年 10 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="4b30b-104">What's new or changed in Dynamics 365 for Finance and Operations version 8.1 (October 2018)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4b30b-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 (2018 年 10 月) の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="4b30b-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Finance and Operations version 8.1 (October 2018).</span></span> <span data-ttu-id="4b30b-106">このバージョンは 2018 年 10 月にリリースされ、ビルド番号は 8.1.136 です。</span><span class="sxs-lookup"><span data-stu-id="4b30b-106">This version was released in October 2018 and has a build number of 8.1.136.</span></span>

### <a name="announcing-the-dynamics-365-october-18-release-notes"></a><span data-ttu-id="4b30b-107">Dynamics 365 2018 年 10 月リリース ノートの発表</span><span class="sxs-lookup"><span data-stu-id="4b30b-107">Announcing the Dynamics 365 October '18 release notes</span></span>
<span data-ttu-id="4b30b-108">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="4b30b-108">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span> 

<span data-ttu-id="4b30b-109">[2018 年 10 月リリース ノートを確認](https://go.microsoft.com/fwlink/?linkid=870424).</span><span class="sxs-lookup"><span data-stu-id="4b30b-109">[Check out the October '18 release notes](https://go.microsoft.com/fwlink/?linkid=870424).</span></span> <span data-ttu-id="4b30b-110">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-110">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span> 

## <a name="use-shared-number-sequences-to-copy-customers-or-vendors"></a><span data-ttu-id="4b30b-111">共有番号順序を使用して、顧客または仕入先をコピーする</span><span class="sxs-lookup"><span data-stu-id="4b30b-111">Use shared number sequences to copy customers or vendors</span></span>
<span data-ttu-id="4b30b-112">共有番号順序を使用して、顧客 ID または仕入先 ID を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-112">You can use shared number sequences to assign customer IDs or vendor IDs.</span></span> <span data-ttu-id="4b30b-113">また、共有番号順序を使用して、同じ顧客 ID または仕入先 ID を維持したまま、法人間で顧客をコピーすることもできます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-113">Shared number sequences also let you copy customers or vendors from one legal entity to another legal entity but use the same IDs in both legal entities.</span></span>

<span data-ttu-id="4b30b-114">追加の詳細については、[共有番号順序を使用して顧客をコピー](../../financials/accounts-receivable/copy-customer.md)および[共有番号順序を使用して仕入先をコピー](../../financials/accounts-payable/vendor-copy.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-114">For additional details, see [Copy customers by using shared number sequences](../../financials/accounts-receivable/copy-customer.md) and [Copy vendors by using shared number sequences](../../financials/accounts-payable/vendor-copy.md).</span></span>

## <a name="customer-transactions-list-page"></a><span data-ttu-id="4b30b-115">顧客トランザクション リスト ページ</span><span class="sxs-lookup"><span data-stu-id="4b30b-115">Customer transactions list page</span></span>
<span data-ttu-id="4b30b-116">アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。</span><span class="sxs-lookup"><span data-stu-id="4b30b-116">The **View settlements** button on the Action Pane provides quick access to the settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="4b30b-117">同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-117">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

<span data-ttu-id="4b30b-118">**グローバル トランザクション**ボタンが顧客ページに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-118">The **Global transactions** button has been added to the customer page.</span></span> <span data-ttu-id="4b30b-119">このボタンを使用して、すべての法人間で顧客のすべてのトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-119">This button lets you view all transactions for a customer across all legal entities.</span></span> <span data-ttu-id="4b30b-120">**顧客トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-120">The **Customer transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="4b30b-121">オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-121">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> 

<span data-ttu-id="4b30b-122">オープン顧客トランザクションの期日および割引日を更新することもでき、**顧客トランザクション**リスト ページに期日を追加できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-122">You can also update due dates and discount dates for open customer transactions, and you can add due dates to the **Customer transactions** list page.</span></span> 

<span data-ttu-id="4b30b-123">詳細については、[顧客トランザクション リスト ページ](../../financials/accounts-receivable/customer-transactions-list-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-123">For more information, see [Customer transaction list page](../../financials/accounts-receivable/customer-transactions-list-page.md).</span></span>

## <a name="vendor-transaction-list-page"></a><span data-ttu-id="4b30b-124">仕入先トランザクション リスト ページ</span><span class="sxs-lookup"><span data-stu-id="4b30b-124">Vendor transaction list page</span></span> 
<span data-ttu-id="4b30b-125">アクション ペインの**決済の表示**ボタンは、決済履歴にすばやくアクセスしたり、決済トランザクション全体についての詳細を説明したりします。</span><span class="sxs-lookup"><span data-stu-id="4b30b-125">The **View settlements** button on the Action Pane provides quick access to the settlement history and more information about the whole settlement transaction.</span></span> <span data-ttu-id="4b30b-126">同じ決済に含まれていたり、または同じ支払仕訳帳で作成された支払である場合、選択したトランザクションに関連する追加トランザクションを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-126">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

<span data-ttu-id="4b30b-127">**グローバル トランザクション**ボタンが仕入先ページに追加されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-127">The **Global transactions** button has been added to the vendor page.</span></span> <span data-ttu-id="4b30b-128">このボタンを使用して、すべての法人間で仕入先のすべてのトランザクションを表示できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-128">This button lets you view all transactions for a vendor across all legal entities.</span></span> <span data-ttu-id="4b30b-129">**仕入先トランザクション**リスト ページでは、ユーザーのセキュリティ設定に基づいて、ユーザーがアクセスする法人に対してのみトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-129">The **Vendor transaction** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="4b30b-130">オープン トランザクションを表示するフィルターは、より多くのトランザクションの組み合わせを見ることができる新しいフィルターで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-130">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="4b30b-131">通貨換算のトランザクションを非表示にすることができる **通貨の再評価を非表示にする** フィルターが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-131">A **Hide currency revaluations** filter has also been added that lets you hide currency translation transactions.</span></span> 

<span data-ttu-id="4b30b-132">未処理の顧客トランザクションのために、期日および割引の日付を更新することもできます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-132">You can also update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="4b30b-133">リリース 8.1 では、**仕入先トランザクション** リスト ページに期日を追加できるようにエクスペリエンスが改善されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-133">In release 8.1, the experience has been improved so that you can add due dates to the **Vendor transaction** list page.</span></span> 

<span data-ttu-id="4b30b-134">詳細については、[仕入先トランザクション リスト ページ](../../financials/accounts-payable/vendor-transaction-list-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-134">For more information, see [Vendor transaction list page](../../financials/accounts-payable/vendor-transaction-list-page.md).</span></span>

## <a name="financial-dimensions"></a><span data-ttu-id="4b30b-135">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="4b30b-135">Financial dimensions</span></span>
<span data-ttu-id="4b30b-136">顧客および仕入先などのマスター レコードの値は、新しい分析コードの既定値として使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-136">You can use values from master records, such as customer and vendor, as default values in new dimensions.</span></span> <span data-ttu-id="4b30b-137">新しい分析コードが作成されると、マスター レコード ID は、マスター レコードの分析コード値で入力されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-137">When the new dimensions are created, the master record ID is entered in the dimension values for those master records.</span></span> <span data-ttu-id="4b30b-138">たとえば、新しい顧客を作成するときに、顧客 ID は顧客分析コードで入力されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-138">For example, when you create a new customer, the customer ID is entered in the customer dimension.</span></span> <span data-ttu-id="4b30b-139">販売注文、請求書、または顧客 ID が必要なその他のドキュメントを作成するときは、既存の既定ルールが使用され、顧客 ID がドキュメントに追加されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-139">When you create sales orders, invoices, or other documents that require a customer ID, the existing defaulting rules are used, and the customer ID is added to the document.</span></span>

<span data-ttu-id="4b30b-140">ドキュメントにその分析コードを入力すると、他の分析コードの情報が自動的に入力されるように分析コードをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-140">You can configure a dimension so that information for other dimensions is automatically entered when you enter that dimension in a document.</span></span> <span data-ttu-id="4b30b-141">たとえば、コスト センター 10 を入力した場合、値 **20** が部門分析コードに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-141">For example, if you enter cost center 10, a value of **20** can be automatically entered in the department dimension.</span></span>

<span data-ttu-id="4b30b-142">エンティティを使用して、派生分析コードのセグメントと値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-142">You can set up the derived dimensions segments and values by using entities.</span></span>

<span data-ttu-id="4b30b-143">詳細については、「[財務分析コード](../../financials/general-ledger/financial-dimensions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-143">For more information, see [Financial dimensions](../../financials/general-ledger/financial-dimensions.md).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="4b30b-144">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="4b30b-144">Extensibility enhancements</span></span>
<span data-ttu-id="4b30b-145">Finance and Operations の今回のリリースでは、コマンド チェーン、委任、またはメンバーへのアクセスを提供することにより拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。</span><span class="sxs-lookup"><span data-stu-id="4b30b-145">In this release of Finance and Operations, numerous extensibility enhancements have been made to support extensibility through chain of command, delegates, or by providing access to members.</span></span> <span data-ttu-id="4b30b-146">さらに、列挙、メタデータ、および SQL 操作に拡張が加えられました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-146">In addition, enhancements have been made to enumerations, metadata, and SQL operations.</span></span> <span data-ttu-id="4b30b-147">詳しくは、[Dynamics 365 for Finance and Operations バージョン 8.1 の拡張機能の変更](../../dev-itpro/extensibility/extensibility-changes-81.md)をご覧ください</span><span class="sxs-lookup"><span data-stu-id="4b30b-147">For detailed information, see [Extensibility changes in Dynamics 365 for Finance and Operations version 8.1](../../dev-itpro/extensibility/extensibility-changes-81.md)</span></span> 

## <a name="phantom-items"></a><span data-ttu-id="4b30b-148">ファントム品目</span><span class="sxs-lookup"><span data-stu-id="4b30b-148">Phantom items</span></span>
<span data-ttu-id="4b30b-149">ファントム明細行タイプは、部品表 (BOM) および複数レベルの BOM 構造の明細行に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-149">The Phantom line type can be used for the lines of a bill of materials (BOM) and multilevel BOM structures.</span></span> <span data-ttu-id="4b30b-150">ファントム BOM は、工順ネットワークのある BOM にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-150">Phantom BOMs can also be used for a BOM that has a route network.</span></span> 

<span data-ttu-id="4b30b-151">詳細については、[ファントム品目](../../supply-chain/production-control/phantom-items.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-151">For more information, see [Phantom items](../../supply-chain/production-control/phantom-items.md).</span></span>

## <a name="russian-localization"></a><span data-ttu-id="4b30b-152">ロシア語のローカライズ</span><span class="sxs-lookup"><span data-stu-id="4b30b-152">Russian localization</span></span>
<span data-ttu-id="4b30b-153">Dynamics 365 for Finance and Operations では、ロシアの必須規制要件がサポートされるようになりました (オンプレミス展開のみ)。</span><span class="sxs-lookup"><span data-stu-id="4b30b-153">Dynamics 365 for Finance and Operations now supports mandatory regulatory requirements in Russia (for on-premises deployment only).</span></span> <span data-ttu-id="4b30b-154">ロシア語ローカライズのこのリリースは、以下の機能領域が対象となっています: 買掛金勘定、売掛金勘定、前貸しホルダー、銀行および現金、クライアント銀行インターフェイスのエクスポート部分、固定資産、総勘定元帳と G/L 報告、財務報告書の電子報告、在庫、アドレス/FIAS、現金の移動、商品の移動、経費の評価、遅延経費、為替差異、仕掛品分野における VAT および利益税登録。</span><span class="sxs-lookup"><span data-stu-id="4b30b-154">This release of Russian localization covers the following functional areas: accounts payable, accounts receivable, advance holders, bank and cash, export part of Client-Bank interface, fixed assets, general ledger and G/L reporting, electronic reporting for financial reports, inventory, addresses/FIAS, VAT and profit tax registers in areas of cash movement, goods movement, rated expenses, deferred expenses, exchange difference and WIP.</span></span> 

<span data-ttu-id="4b30b-155">詳細については、[ロシア](../../financials/localizations/russia.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b30b-155">For more information, see [Russia](../../financials/localizations/russia.md).</span></span>

## <a name="vat-reporting-for-the-united-arab-emirates"></a><span data-ttu-id="4b30b-156">アラブ首長国連邦の VAT レポート</span><span class="sxs-lookup"><span data-stu-id="4b30b-156">VAT reporting for the United Arab Emirates</span></span>   
<span data-ttu-id="4b30b-157">Finance and Operations の標準売上税機能は、アラブ首長国連邦の VAT 法の法律要件の大部分を満たすようになりました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-157">Standard sales tax functionality in Finance and Operations now fulfils the majority of legislation requirements of United Arab Emirates VAT law.</span></span> <span data-ttu-id="4b30b-158">次の国固有の機能は、アラブ首長国連邦に固有です。</span><span class="sxs-lookup"><span data-stu-id="4b30b-158">The following country-specific features are specific to the United Arab Emirates:</span></span>

  - <span data-ttu-id="4b30b-159">VAT 報告で必要な追加のフィールドで、法人コンフィギュレーションが拡張されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-159">Legal entity configuration has been extended with additional fields required in VAT reporting.</span></span>
  - <span data-ttu-id="4b30b-160">GCC 領土内の課税対象の国内工程を正しく記録するため、アラブ首長国連邦 (ARE 国コンテキスト) で VAT 逆請求機能が有効になりました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-160">VAT reverse charge functionality has been enabled for UAE (ARE country context) to properly record taxable domestic operations within GCC territory.</span></span>
  - <span data-ttu-id="4b30b-161">追加の列および VAT 集計情報によって、追加の販売、請求書、および貸方票の印刷レイアウトが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-161">Additional sales, invoice, and credit notes print layouts have been added with additional columns and VAT summary information.</span></span>
  - <span data-ttu-id="4b30b-162">アラブ首長国連邦の販売の請求書および貸方票は、ユーザー インターフェイスの新しい ar-AE アラビア語を含む 2 つの言語で印刷されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-162">Sales Invoice and Credit notes for UAE now print in two languages, including a new ar-AE Arabic language for user interface.</span></span>
  - <span data-ttu-id="4b30b-163">VAT 還付申告レポートは、e-TAX FTA ポータルへのアップロードに対応する電子ファイル形式で印刷されます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-163">VAT Return declaration report is printed to an electronic file format ready for uploading to e-TAX FTA portal.</span></span>
  - <span data-ttu-id="4b30b-164">標準監査ファイル機能がアラブ首長国連邦のローカル機能と共有されました。</span><span class="sxs-lookup"><span data-stu-id="4b30b-164">Standard audit file functionality has been shared with UAE local functionality.</span></span> <span data-ttu-id="4b30b-165">これは、bht 連邦税所轄官庁 FTA VAT 監査ファイル - (FAF) に必要であり、コンマ区切りファイル形式にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="4b30b-165">This is required by bht Federal Tax Authorities FTA VAT audit file - (FAF) and can be exported to a comma separated file format.</span></span>

