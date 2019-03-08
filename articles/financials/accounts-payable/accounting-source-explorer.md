---
title: 会計ソース エクスプローラー
description: この記事は、総勘定元帳の勘定項目の背後にあるソース情報の詳細分析に使用できる会計のソース エクスプローラに関する情報を提供します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingSourceExplorer
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: de5de039c0e3332943bae4846768fc628810906e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "330198"
---
# <a name="accounting-source-explorer"></a><span data-ttu-id="307bf-103">会計ソース エクスプローラー</span><span class="sxs-lookup"><span data-stu-id="307bf-103">Accounting source explorer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="307bf-104">この記事は、総勘定元帳の勘定項目の背後にあるソース情報の詳細分析に使用できる会計のソース エクスプローラに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="307bf-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="307bf-105">会計のソース エクスプローラーは、ソース情報を表示する新しいページです。</span><span class="sxs-lookup"><span data-stu-id="307bf-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="307bf-106">会計のソース エクスプローラーをスタンドアロンのツールとして、または総勘定元帳の勘定項目の後にある詳細を分析するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="307bf-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="307bf-107">たとえば、試算表の残高または伝票トランザクションの最も詳細なソース情報を得るために会計のソース エクスプローラーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="307bf-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="307bf-108">これにより、MS Excel へのエクスポート機能を使用して、Microsoft Excel で情報をより詳しく分析できます (たとえば、ピボット テーブルで、またはピボット テーブルのレポートで)。</span><span class="sxs-lookup"><span data-stu-id="307bf-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="307bf-109">会計のソース エクスプローラーは、総勘定元帳と同じ勘定科目ごとの合計金額を常に表示します (たとえば、試算表で)。</span><span class="sxs-lookup"><span data-stu-id="307bf-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="307bf-110">試算表の場合と同様に、別の列の区分を表示できます。</span><span class="sxs-lookup"><span data-stu-id="307bf-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="307bf-111">適切な財務分析コード セットを選択します。</span><span class="sxs-lookup"><span data-stu-id="307bf-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="307bf-112">パラメーターを使用すると、分析の日付範囲を定義できます。</span><span class="sxs-lookup"><span data-stu-id="307bf-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="307bf-113">この機能は、試算表の機能に似ています。</span><span class="sxs-lookup"><span data-stu-id="307bf-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="307bf-114">元伝票フレームワークを使用するすべてのドキュメントでは、会計のソース エクスプローラーは、勘定配布に基づき、または必要に応じてプロジェクト勘定配布に基づき、追加情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="307bf-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="307bf-115">この情報は、金額タイプ、プロジェクト、活動、カテゴリ、および明細行プロパティを含みます。</span><span class="sxs-lookup"><span data-stu-id="307bf-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="307bf-116">次に実行できる分析の例を示します。</span><span class="sxs-lookup"><span data-stu-id="307bf-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="307bf-117">発注書と仕入先請求書の差異、これは各差異が差額などの金額タイプにより表示されるためです。</span><span class="sxs-lookup"><span data-stu-id="307bf-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="307bf-118">プロジェクト、事業単位、主勘定ごとの支払請求可能な時間および経費に対する支払請求不可能な時間および経費</span><span class="sxs-lookup"><span data-stu-id="307bf-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="307bf-119">元伝票参照 ID の概念を使用する元伝票では、会計のソース エクスプローラーは、顧客、仕入先、作業者、製品、数量、単位テキスト、および説明などの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="307bf-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="307bf-120">次に実行できる分析の例を示します。</span><span class="sxs-lookup"><span data-stu-id="307bf-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="307bf-121">経費精算書に基づく、事業単位ごとの宿泊費、および会計年度期間のホテルのブランド</span><span class="sxs-lookup"><span data-stu-id="307bf-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="307bf-122">仕入先、製品、部門ごとの割引</span><span class="sxs-lookup"><span data-stu-id="307bf-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="307bf-123">これらのドキュメントでは、会計のソース エクスプローラーから実際の元伝票に移動できます。</span><span class="sxs-lookup"><span data-stu-id="307bf-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>



