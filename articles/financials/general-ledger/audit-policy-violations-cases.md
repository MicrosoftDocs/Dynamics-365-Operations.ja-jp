---
title: "監査ポリシー違反およびケース"
description: "記事は、監査ポリシー ルール違反からどのように監査ケースが生成されるかを説明します。 また、監査ポリシーがドキュメントの選択の日付範囲を使用する、さまざまな方法に関する情報が含まれます。"
author: ryansandness
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13091
ms.assetid: e0e66c6d-c396-4a9d-b3b6-3641d130fdc0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2376a1d6e86eba9f5021cc08dcfaea52f131a3d7
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-violations-and-cases"></a><span data-ttu-id="a720e-104">監査ポリシー違反およびケース</span><span class="sxs-lookup"><span data-stu-id="a720e-104">Audit policy violations and cases</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a720e-105">記事は、監査ポリシー ルール違反からどのように監査ケースが生成されるかを説明します。</span><span class="sxs-lookup"><span data-stu-id="a720e-105">The article explains how audit cases are generated from violations of audit policy rules.</span></span> <span data-ttu-id="a720e-106">また、監査ポリシーがドキュメントの選択の日付範囲を使用する、さまざまな方法に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a720e-106">It also includes information about the various ways that audit policies use the document selection date range.</span></span>

<a name="how-audit-cases-are-generated"></a><span data-ttu-id="a720e-107">監査ケースの生成方法</span><span class="sxs-lookup"><span data-stu-id="a720e-107">How audit cases are generated</span></span>
-----------------------------

<span data-ttu-id="a720e-108">監査ポリシーが、監査ポリシー ルールとして定義およびコンフィギュレーションしたビジネス ルールに適合しない、経費精算書、発注書、および仕入先請求書の識別に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-108">Audit policies are used to identify expense reports, purchase orders, and vendor invoices that don't comply with business rules that you define and configure as audit policy rules.</span></span> 

<span data-ttu-id="a720e-109">監査ポリシーはバッチ モードで実行されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-109">Audit policies are run in batch mode.</span></span> <span data-ttu-id="a720e-110">監査ポリシーを実行するとき、そのポリシーの一部であるすべてのポリシー ルールが同時に実行されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-110">When you run an audit policy, all the policy rules that are part of that policy are run at the same time.</span></span>

<span data-ttu-id="a720e-111">各ポリシー ルールは、一連のドキュメントを評価します。</span><span class="sxs-lookup"><span data-stu-id="a720e-111">Each policy rule evaluates a set of documents.</span></span> <span data-ttu-id="a720e-112">ポリシー ルールは、ドキュメント選択の日付の範囲と指定した基準に一致するドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="a720e-112">The policy rule selects documents that are in the document selection date range and that match the specified criteria.</span></span> <span data-ttu-id="a720e-113">たとえば、ポリシー ルールが 50.00 ドルを超える食事の経費精算書を選択する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a720e-113">For example, one policy rule might select expense reports that have meals that exceed 50.00.</span></span> <span data-ttu-id="a720e-114">別のポリシー ルールが、固有の仕入先に支払可能な仕入先請求書を選択する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a720e-114">Another policy rule might select vendor invoices that are payable to a specific vendor.</span></span> <span data-ttu-id="a720e-115">選択したセット内のドキュメントごとに、違反が生成されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-115">For each document that is selected in the set, a violation is generated.</span></span> <span data-ttu-id="a720e-116">違反とは、請求書 12345 など、特定のドキュメントがそのがポリシー ルールに適合しないレコードです。</span><span class="sxs-lookup"><span data-stu-id="a720e-116">That violation is a record that a particular document, such as invoice 12345, doesn't comply with the policy rule.</span></span> 

<span data-ttu-id="a720e-117">複数の監査違反レコードがグループ化され、監査ケースに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="a720e-117">Multiple audit violation records are grouped together and associated with audit cases.</span></span> <span data-ttu-id="a720e-118">既定では、各監査ポリシーのケースは、監査ポリシー ルールごとにグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-118">By default, cases for each audit policy are grouped by audit policy rule.</span></span> <span data-ttu-id="a720e-119">必要であれば、**ケースのグループ化基準** ページを使用して他のグループ化基準を選択します。</span><span class="sxs-lookup"><span data-stu-id="a720e-119">If you prefer, you can select other grouping criteria by using the **Case grouping criteria** page.</span></span> <span data-ttu-id="a720e-120">たとえば、プロジェクト ID で経費ヘッダーを、仕入先 ID で仕入先請求書をグループ化できます。</span><span class="sxs-lookup"><span data-stu-id="a720e-120">For example, you can group expense headers by project ID and vendor invoices by vendor account.</span></span> <span data-ttu-id="a720e-121">その場合は、プロジェクト ID が同じすべての経費ヘッダーの違反は同じケースにグループ化され、仕入先 ID が同じすべての仕入先請求書は同じケースにグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-121">In this case, all expense header violations that have the same project ID will be grouped in the same case, and all vendor invoices that have the same vendor account will be grouped in the same case.</span></span> 

> [!NOTE]
> <span data-ttu-id="a720e-122">[**重複**] クエリ タイプに基づく監査ポリシー ルールの場合、違反はポリシー ルールまたは **ケースのグループ化基準** ページで指定した基準によってグループ化されません。</span><span class="sxs-lookup"><span data-stu-id="a720e-122">For audit policy rules that are based on a **Duplicate** query type, violations aren't grouped by policy rule or by the criteria that are specified on the **Case grouping criteria** page.</span></span> <span data-ttu-id="a720e-123">代わりに、監査ポリシー ルールに組み込まれた基準によってグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-123">Instead, they are grouped by the criteria that are built into the audit policy rule.</span></span> <span data-ttu-id="a720e-124">たとえば、ポリシー ルールが、金額、商社 ID および日付が同じ重複経費の経費精算書を評価する場合、これらのフィールドの値が同じすべての経費は 1 つのケースとなります。</span><span class="sxs-lookup"><span data-stu-id="a720e-124">For example, if a policy rule evaluates expense reports for duplicate expenses of the same amount, merchant ID, and date, all expenses that have the same values in those fields will be one case.</span></span> <span data-ttu-id="a720e-125">異なる値を持つすべての経費が別のケースとなります。</span><span class="sxs-lookup"><span data-stu-id="a720e-125">Any expenses that have different values will be a separate case.</span></span>

<span data-ttu-id="a720e-126">監査ケースが生成されると、それらはケース管理の標準的なプロセスを使用して扱われます。</span><span class="sxs-lookup"><span data-stu-id="a720e-126">After the audit cases have been generated, they are handled by using the typical processes for case management.</span></span>

## <a name="document-selection-date-ranges"></a><span data-ttu-id="a720e-127">ドキュメントの選択の日付範囲</span><span class="sxs-lookup"><span data-stu-id="a720e-127">Document selection date ranges</span></span>
<span data-ttu-id="a720e-128">監査ポリシーを実行すると、各ポリシー ルールは、ドキュメント選択の日付範囲に入る日付が付いている指定されたタイプのドキュメントを選択します。</span><span class="sxs-lookup"><span data-stu-id="a720e-128">When an audit policy is run, each policy rule selects documents of the specified type that have a date that is in the document selection date range.</span></span> <span data-ttu-id="a720e-129">ドキュメント選択の日付の範囲は、**追加のオプション**ページで指定されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-129">The document selection date range is specified on the **Additional options** page.</span></span> <span data-ttu-id="a720e-130">多くのドキュメントには、それらのドキュメントに関連付けられている複数の日付があります。</span><span class="sxs-lookup"><span data-stu-id="a720e-130">Many documents have more than one date associated with them.</span></span> <span data-ttu-id="a720e-131">監査ポリシー ルールで使用する日付フィールドは、**ポリシー ルール タイプ**ページで指定されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-131">The date field that the audit policy rule uses is specified on the **Policy rule type** page.</span></span>

<span data-ttu-id="a720e-132">監査ポリシーがドキュメント選択日付の範囲に使用する、他の方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a720e-132">Here are some other ways that an audit policy uses the document selection date range:</span></span>

-   <span data-ttu-id="a720e-133">このポリシーは、ドキュメント選択の日付の範囲の最終日に、有効な各ポリシー ルールのバージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="a720e-133">The policy uses the version of each policy rule that is effective on the last day of the document selection date range.</span></span> <span data-ttu-id="a720e-134">**監査ポリシー** リスト ページで、各ポリシー ルールの有効日を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a720e-134">You can view the effective dates for each policy rule on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="a720e-135">このポリシーは、ドキュメント選択の日付の範囲の最終日のポリシーに関連付けられている組織ノードを使用します。</span><span class="sxs-lookup"><span data-stu-id="a720e-135">The policy uses the organization nodes that are associated with the policy on the last day of the document selection date range.</span></span> <span data-ttu-id="a720e-136">ポリシーに現在関連付けられている組織ノードだけが、**監査ポリシー** リスト ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a720e-136">Only the organization nodes that are currently associated with the policy appear on the **Audit policies** list page.</span></span>
-   <span data-ttu-id="a720e-137">[**リスト検索**] クエリ タイプに基づくポリシー ルールでは、ポリシーは、ドキュメント選択の日付の範囲の最終日に有効な監視対象のエンティティのドキュメントを評価します。</span><span class="sxs-lookup"><span data-stu-id="a720e-137">For policy rules that are based on a **List search** query type, the policy evaluates documents for monitored entities that are effective on the last day of the document selection date range.</span></span>


<span data-ttu-id="a720e-138">詳細については、「[監査ポリシー ルール](audit-policy-rules.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a720e-138">For more information, see [Audit policy rules](audit-policy-rules.md)</span></span>




