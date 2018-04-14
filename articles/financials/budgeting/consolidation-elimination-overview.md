---
title: "連結と削除の概要"
description: "この記事は、連結および消去プロセスに関する一般情報を提供します。 これには、よく寄せられる質問への回答が含まれます。"
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerConsolidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13151
ms.assetid: 9d8f55cb-b2cf-4e01-89cf-0e21f5c8ae1f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c7f25fcf3f6b87515d3a10acf17c011a249940b
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---

# <a name="consolidation-and-elimination-overview"></a><span data-ttu-id="b2d10-104">連結と削除の概要</span><span class="sxs-lookup"><span data-stu-id="b2d10-104">Consolidation and elimination overview</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b2d10-105">この記事は、連結および消去プロセスに関する一般情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-105">This article provides general information about the consolidation and elimination process.</span></span> <span data-ttu-id="b2d10-106">これには、よく寄せられる質問への回答が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-106">It includes answers to some frequently asked questions.</span></span>

<span data-ttu-id="b2d10-107">データを連結する場合、複数の関連会社の財務結果は 1 つの連結した会社の結果にまとめられます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-107">When you consolidate data, the financial results for multiple subsidiary companies are combined into results for a single, consolidated company.</span></span> <span data-ttu-id="b2d10-108">関連会社は、さまざまなバージョンまたはシステムを使用している場合があり、完全に所有されていない場合や、さまざまな通貨を使用している場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-108">Subsidiaries might be on different versions or systems, they might not be fully owned, and they might use different currencies.</span></span> <span data-ttu-id="b2d10-109">データを連結するための複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-109">There are multiple options for consolidating data:</span></span>

-   <span data-ttu-id="b2d10-110">**オンラインで連結** – このオプションは、選択された勘定および分析コードで、毎日の残高を連結し、連結会社に保存します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-110">**Consolidate online** – This option consolidates daily balances by the selected accounts and dimensions, and stores them in a consolidation company.</span></span>
-   <span data-ttu-id="b2d10-111">**財務報告** – このオプションは、トランザクションおよび残高の連結を有効にして、いつでも生成します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-111">**Financial reporting** – This option enables consolidation of transactions and balances, and can be generated at any time.</span></span> <span data-ttu-id="b2d10-112">階層が複数のレベルを作成し、複数のレポート通貨を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-112">Multiple levels of hierarchies can be created, and multiple reporting currencies can be viewed.</span></span>
-   <span data-ttu-id="b2d10-113">**インポートして連結** – このオプションは、連結会社に残高をインポートします。</span><span class="sxs-lookup"><span data-stu-id="b2d10-113">**Consolidate with import** – This option imports balances into a consolidation company.</span></span>
-   <span data-ttu-id="b2d10-114">**会社の残高のエクスポート** – このオプションは、会社の残高のエクスポート ファイルを提供します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-114">**Export company balances** – This option provides an export file of company balances.</span></span> <span data-ttu-id="b2d10-115">ファイルは、他のインスタンスまたはシステムにインポートできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-115">The file can then be imported into other instances or systems.</span></span> <span data-ttu-id="b2d10-116">財務報告は Microsoft Excel ファイルに残高をエクスポートするためにも使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-116">Financial reporting can also be used to export the balances to a Microsoft Excel file.</span></span>

<span data-ttu-id="b2d10-117">削除はさまざまな方法で報告できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-117">Eliminations can be reported in multiple ways:</span></span>

-   <span data-ttu-id="b2d10-118">削除ルールがシステムで設定され、連結プロセス中または削除提案を通して処理されます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-118">Elimination rules can be set up in the system, and then processed during the consolidation process or through an elimination proposal.</span></span> <span data-ttu-id="b2d10-119">このルールは、法人の設定で [財務消去プロセスで使用] が選択された会社すべてに転記できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-119">The rules can be posted to any company that has **Use for financial elimination process** selected in the legal entity setup.</span></span>
-   <span data-ttu-id="b2d10-120">手動で削除トランザクションを特定および転記するために、個別の会社が作成また使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-120">A separate company can be created and used to manually determine and post elimination transactions.</span></span> <span data-ttu-id="b2d10-121">この会社は、連結プロセスまたは財務報告に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-121">This company can be used in the consolidation process or in financial reporting.</span></span>
-   <span data-ttu-id="b2d10-122">会社間活動を特定するために使用される勘定と財務分析コードは、財務報告の行定義と列定義でフィルター処理することができ、完全なドリルダウン機能が使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-122">The accounts and financial dimensions that are used to determine intercompany activity can be filtered on a row definition or column definition in Financial reporting, and full drill-down capabilities can be used.</span></span> <span data-ttu-id="b2d10-123">次に計算された列または行は、連結合計から勘定と財務分析コードを削除するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-123">A calculated column or row can then be used to remove the accounts and financial dimensions from the consolidated total.</span></span>

<span data-ttu-id="b2d10-124">多くの連結のシナリオがあり、それぞれの方法は、さまざまな方法でシナリオを処理できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-124">There are many consolidation scenarios, and each method can handle the scenarios in different ways.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b2d10-125">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b2d10-125">Frequently asked questions</span></span>
1.  <span data-ttu-id="b2d10-126">データベースでの消去の転記を希望します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-126">I prefer to post eliminations in a database.</span></span> <span data-ttu-id="b2d10-127">どのようなオプションがありますか?</span><span class="sxs-lookup"><span data-stu-id="b2d10-127">What are my options?</span></span>

<span data-ttu-id="b2d10-128">複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-128">You have multiple options.</span></span> <span data-ttu-id="b2d10-129">[オンラインで連結] オプションを使用して、プロセス中または提案としての消去を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-129">You can use the **Consolidate online** option, and include eliminations during the process or as a proposal.</span></span> <span data-ttu-id="b2d10-130">トランザクションが連結会社に転記されます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-130">The transactions will be posted in the consolidation company.</span></span> <span data-ttu-id="b2d10-131">消去を含む手動で作成した個別の会社を作成し、財務報告または連結プロセスでその会社を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-131">Alternatively, you can have a separate company that you manually create the eliminations in, and then use that company in Financial reporting or in the consolidation process.</span></span>

2.  <span data-ttu-id="b2d10-132">複数のレポート通貨で、連結の結果が必要です。</span><span class="sxs-lookup"><span data-stu-id="b2d10-132">We need our consolidated results in multiple reporting currencies.</span></span>

<span data-ttu-id="b2d10-133">[財務報告] オプションには、無制限のレポート通貨があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-133">The **Financial reporting** option has unlimited reporting currencies.</span></span> <span data-ttu-id="b2d10-134">主勘定に設定された為替レート タイプおよび為替換算方法に基づいて、データはレポート生成時に換算されます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-134">The data is translated during report generation, based on the exchange rate type and currency translation method that are set on the main account.</span></span> <span data-ttu-id="b2d10-135">ただし、レポート通貨に [オンラインで連結] オプションが 1 つしかないため、このオプションを使用する場合、レポート通貨それぞれに 1 つの連結会社が必要です。</span><span class="sxs-lookup"><span data-stu-id="b2d10-135">However, because the **Consolidate online** option has only one reporting currency, a consolidated company is required for each reporting currency if you use that option.</span></span> <span data-ttu-id="b2d10-136">[財務報告] オプションがお勧めの方法です。</span><span class="sxs-lookup"><span data-stu-id="b2d10-136">The **Financial reporting** option is the recommended method.</span></span>

3.  <span data-ttu-id="b2d10-137">各会社のトランザクション レベルの詳細の表示を希望します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-137">I want to see transaction-level detail for each company.</span></span>

<span data-ttu-id="b2d10-138">[財務報告] オプションがソリューションです。できるだけ多くの会社で、レポート ツリー定義に含まれるトランザクション レベルの詳細が表示できるためです。</span><span class="sxs-lookup"><span data-stu-id="b2d10-138">The **Financial reporting** option is the solution, because transaction-level detail can be viewed for as many companies as are included in the reporting tree definition.</span></span>

4.  <span data-ttu-id="b2d10-139">予算計画または予算管理を使用していて、それを連結する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-139">We are using budget planning or budget control, and it must be consolidated.</span></span>
<span data-ttu-id="b2d10-140">[財務報告] オプションは、すべての予算計画または予算管理のデータを連結するソリューションです。</span><span class="sxs-lookup"><span data-stu-id="b2d10-140">The **Financial reporting** option is the solution to consolidate any budget planning or budget control data.</span></span>

5.  <span data-ttu-id="b2d10-141">弊社の関連会社は、世界中に拡大し、複数の勘定科目表があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-141">Our subsidiaries are spread throughout the world, and we have multiple charts of accounts.</span></span> <span data-ttu-id="b2d10-142">弊社のデータを連結するのに最適な方法は何ですか?</span><span class="sxs-lookup"><span data-stu-id="b2d10-142">What is the best method for consolidating our data?</span></span>

<span data-ttu-id="b2d10-143">複数の勘定科目表を処理する必要がある場合、複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-143">You have multiple options when you must handle multiple charts of accounts.</span></span> <span data-ttu-id="b2d10-144">[オンラインで連結] オプションを使用 し、主勘定または連結勘定グループで定義された連結勘定のどちらを使用するかを次に選択します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-144">You can use the **Consolidate online** option, and then choose to use either the consolidation account that is defined on the main account or a consolidation account group.</span></span> <span data-ttu-id="b2d10-145">[財務報告] オプションを使用 し、行定義の財務分析コードに複数のリンクを追加し、勘定をマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-145">You can also use the **Financial reporting** option, include multiple links to the financial dimensions in the row definition, and map the accounts.</span></span>

6.  <span data-ttu-id="b2d10-146">複数レベルの連結が必要です。</span><span class="sxs-lookup"><span data-stu-id="b2d10-146">We require multiple levels of consolidation.</span></span> <span data-ttu-id="b2d10-147">言い換えると、最初に英国ポンド (GBP) にすべての欧州関連会社を連結します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-147">In other words, we first consolidate all our European subsidiaries to the British pound (GBP).</span></span> <span data-ttu-id="b2d10-148">次に、そのデータを取得して、連結された金額を米ドルに換算します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-148">We then take that data and translate the consolidated amount to US dollars.</span></span> <span data-ttu-id="b2d10-149">どのようにしますか?</span><span class="sxs-lookup"><span data-stu-id="b2d10-149">How can we do this?</span></span>

<span data-ttu-id="b2d10-150">複数のレベルの連結が必要となり、さまざまな通貨が各レベルで使用されている場合は、[オンラインで連結] オプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-150">When multiple levels of consolidation are required, and different currencies are used at each level, you must use the **Consolidate online** option.</span></span> <span data-ttu-id="b2d10-151">会計通貨とレポート通貨が異なる複数の連結会社を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-151">Multiple consolidation companies must be created that differ in their accounting and reporting currencies.</span></span> <span data-ttu-id="b2d10-152">次に連結を複数回実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-152">The consolidation must then be run multiple times.</span></span> <span data-ttu-id="b2d10-153">[財務報告] オプションは、元の会社の各会計通貨から選択した通貨に常に換算します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-153">The **Financial reporting** option always translates from each source company's accounting currency to the selected currency.</span></span>

7.  <span data-ttu-id="b2d10-154">別のシステムを使用する関連会社があります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-154">We have subsidiaries on a different system.</span></span> <span data-ttu-id="b2d10-155">どのように連結すればいいでしょうか?</span><span class="sxs-lookup"><span data-stu-id="b2d10-155">How can we consolidate them?</span></span>

<span data-ttu-id="b2d10-156">[インポートして連結] オプションを使用して、連結会社に残高を結び付けます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-156">Use the **Consolidate with import** option to bring the balances into a consolidation company.</span></span>

8.  <span data-ttu-id="b2d10-157">関連会社の一部は完全に所有されていません。</span><span class="sxs-lookup"><span data-stu-id="b2d10-157">Some of our subsidiaries are not fully owned.</span></span> <span data-ttu-id="b2d10-158">それらを連結するのに最適な方法は何ですか?</span><span class="sxs-lookup"><span data-stu-id="b2d10-158">What is the best method for consolidating them?</span></span>

<span data-ttu-id="b2d10-159">一部を所有している関連会社のために複数のオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-159">You have multiple options for partially owned subsidiaries.</span></span> <span data-ttu-id="b2d10-160">[財務報告] オプションを使用して、レポート ツリー定義と所有権を定義できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-160">By using the **Financial reporting** option, you can define a reporting tree definition and the ownership.</span></span> <span data-ttu-id="b2d10-161">計算された行または列を使用して、部分的に所有された金額を表すこともできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-161">You can also use a calculated row or column to represent the partially owned amount.</span></span> <span data-ttu-id="b2d10-162">レポートの独自の行として少数株主持分を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-162">You can even show the minority interest as its own row on a report.</span></span> <span data-ttu-id="b2d10-163">[オンラインで連結] オプションを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-163">You can also use the **Consolidate online** option.</span></span> <span data-ttu-id="b2d10-164">[法人] タブには、[所有権] の列があり、親会社が所有する割合を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-164">The **Legal entities** tab has an **Ownership** column, where you can define the percentage that is owned by the parent company.</span></span>

9.  <span data-ttu-id="b2d10-165">当組織では事業単位で連結を表示する必要があります。または組織階層を使用することを希望します。</span><span class="sxs-lookup"><span data-stu-id="b2d10-165">Our organization must show consolidations by business unit or wants to use the organization hierarchies.</span></span>

<span data-ttu-id="b2d10-166">[財務報告] オプションがソリューションです。</span><span class="sxs-lookup"><span data-stu-id="b2d10-166">The **Financial reporting** option is the solution.</span></span> <span data-ttu-id="b2d10-167">法人がある組織階層、またはそれらの中にある財務分析コードは "財務報告" で報告できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-167">Organization hierarchies that have legal entities or financial dimensions in them can be reported on in Financial reporting.</span></span> <span data-ttu-id="b2d10-168">法人および分析コード値の組み合わせによるレポート ツリー定義を使用して、独自の複数レベルの階層を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-168">You can also create your own multilevel hierarchies by using a reporting tree definition that has a combination of legal entities and dimension values.</span></span>

10. <span data-ttu-id="b2d10-169">システムには複数のインスタンスがあります。</span><span class="sxs-lookup"><span data-stu-id="b2d10-169">We have more than one instance of the system.</span></span>

<span data-ttu-id="b2d10-170">[会社の残高のエクスポート] オプションを使用して、1 つのインスタンスからエクスポートし、次に他のインスタンスで [インポートして連結] オプションを使用してデータを連結できます。</span><span class="sxs-lookup"><span data-stu-id="b2d10-170">By using the **Export company balances** option to export from one instance and then using the **Consolidate with import** option on the other instance, you can consolidate the data.</span></span>


<span data-ttu-id="b2d10-171">詳細については、「[連結会社の通貨再評価](..\general-ledger\currency-revaluation-consolidation-company.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2d10-171">For more information, see [Currency revalution in a consolidation company](..\general-ledger\currency-revaluation-consolidation-company.md).</span></span>



