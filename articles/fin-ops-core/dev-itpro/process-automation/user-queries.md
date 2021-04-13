---
title: 構成可能なユーザーのクエリ
description: このトピックでは、構成可能なクエリを作成し、プロセス自動化フレームワークで使用する方法について説明します。
author: RyanCCarlson2
ms.date: 09/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-09-10
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 690787be87c34bbb4e46375c17bad2bec0a60a0a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745111"
---
# <a name="user-configurable-queries"></a><span data-ttu-id="8ae2a-103">構成可能なユーザーのクエリ</span><span class="sxs-lookup"><span data-stu-id="8ae2a-103">User-configurable queries</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ae2a-104">このトピックでは、構成可能なクエリを作成し、プロセス自動化フレームワークで使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-104">This topic describes how to create configurable queries and use them with the process automation framework.</span></span> <span data-ttu-id="8ae2a-105">プロセスが **SysQueryForm** フォームによるユーザーの構成可能なクエリをサポートしていない場合は 、このタスクを省略できます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-105">If a process won't support user-configurable queries via the **SysQueryForm** form, you can skip this task.</span></span>

<span data-ttu-id="8ae2a-106">プロセス自動化フレームワークでは、**SysQueryForm** フォームを介したカスタム クエリのサポートが制限されています。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-106">The process automation framework provides limited support for custom queries via the **SysQueryForm** form.</span></span> <span data-ttu-id="8ae2a-107">カスタム クエリを使用すると、ユーザーはカスタムの基準を追加して、プロセスの実行方法を制限することができます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-107">A custom query lets a user add custom criteria to limit how a process runs.</span></span> <span data-ttu-id="8ae2a-108">フレームワークには、ユーザーが指定したカスタムの基準を抽出するためのロジックと、それらの基準を格納するためのテーブルがあります。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-108">The framework has logic to extract user-provided custom criteria and tables to store those criteria.</span></span> <span data-ttu-id="8ae2a-109">カスタム クエリ基準は、指定された一連の発生ごとに格納され、個別に変更できます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-109">The custom query criteria are stored for each occurrence of a given series and can be modified individually.</span></span> <span data-ttu-id="8ae2a-110">フレームワークには、各発生のプロセスの実行に使用されるクエリにカスタム基準を適用するための API も用意されています。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-110">The framework also provides an API to apply the custom criteria to the query that is used to run the process for each occurrence.</span></span>

> [!NOTE]
> <span data-ttu-id="8ae2a-111">ユーザーがクエリ基準を適用するときには、すべてのクエリ オブジェクトは保存されません。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-111">When a user applies query criteria, the whole query object isn't saved.</span></span> <span data-ttu-id="8ae2a-112">代わりに、クエリ基準は個別に保存され、クエリの拡張機能のサポートが強化されます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-112">Instead the query criteria are saved individually, to allow for better support of query extensions.</span></span> <span data-ttu-id="8ae2a-113">したがって、この方法を使用する場合、既存のクエリ基準の既存のクエリに対する拡張機能によって破壊的変更が発生することはありません。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-113">Therefore, extensions that are made to existing queries for existing query criteria should not cause breaking changes when this approach is used.</span></span> <span data-ttu-id="8ae2a-114">この場合、新しい拡張機能では、保存されたシリーズまたは発生にクエリ基準を変更または再作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-114">In this case, a new extension should not require modification or re-creation of the query criteria for a saved series or occurrences.</span></span> <span data-ttu-id="8ae2a-115">ただし、クエリ基準の変更または再作成は可能です。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-115">However, modification or re-creation of the query criteria is allowed.</span></span>

## <a name="processscheduleiqueryable-interface"></a><span data-ttu-id="8ae2a-116">ProcessScheduleIQueryable インターフェイス</span><span class="sxs-lookup"><span data-stu-id="8ae2a-116">ProcessScheduleIQueryable interface</span></span>

<span data-ttu-id="8ae2a-117">**ProcessScheduleIQueryable** インターフェイスは、元のクエリ (ユーザーによって変更される前のクエリ) とユーザーが変更したクエリを取得します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-117">The **ProcessScheduleIQueryable** interface retrieves the original query (that is, the query as it was before the user modified it) and the user-modified query.</span></span> <span data-ttu-id="8ae2a-118">これらのクエリは、プロセスの実行時に基準を適用するため、またはユーザーが変更を行うときに基準を抽出するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-118">These queries are used either to apply criteria when the process runs or to extract criteria when the user makes changes.</span></span> <span data-ttu-id="8ae2a-119">これらの基準は、プロセス自動化フレームワークによって格納されます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-119">These criteria are stored by the process automation framework.</span></span>

<span data-ttu-id="8ae2a-120">このインターフェイスは、プロセス自動化の指定された実装の基準フォームでアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-120">This interface is accessed in the criteria form for a given implementation of process automation.</span></span> <span data-ttu-id="8ae2a-121">このインターフェイスへのアクセス例については、**VendPaymProposalAutomationCriteria** フォームを参照してください 。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-121">For an example of access to this interface, see the **VendPaymProposalAutomationCriteria** form.</span></span> <span data-ttu-id="8ae2a-122">このフォームには、**SysQueryForm** フォームのサンプル実装も含まれてい ます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-122">That form also has a sample implementation of the **SysQueryForm** form.</span></span>

| <span data-ttu-id="8ae2a-123">メソッド</span><span class="sxs-lookup"><span data-stu-id="8ae2a-123">Method</span></span> | <span data-ttu-id="8ae2a-124">説明</span><span class="sxs-lookup"><span data-stu-id="8ae2a-124">Description</span></span> |
|---|---|
| `public Query getOriginalQuery()` | <span data-ttu-id="8ae2a-125">このメソッドは、変更されていない元のクエリを取得して、比較基準として使用します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-125">This method gets the original, unmodified query to use as a basis for comparison.</span></span> |
| `public Query getQueryForApplicationOrExtractionOfQueryCriteria()` | <span data-ttu-id="8ae2a-126">このメソッドは、変更済みかまたは変更される予定のクエリを取得して、クエリ基準を適用または抽出するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-126">This method gets the query that has been or will be modified, and that is used to apply or extract query criteria.</span></span> |

> [!NOTE]
> <span data-ttu-id="8ae2a-127">**ProcessScheduleIQueryable** の実装に使用されるクエリは、自動化する基になるプロセスの実行時に使用されるクエリと同じ構造を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-127">The query that is used on the implementation of **ProcessScheduleIQueryable** must have the same structure as the query that is used during the run of the underlying process that is being automated.</span></span> <span data-ttu-id="8ae2a-128">本質的に付加されない構造的な誤差があると、保存されたクエリ基準がランタイムに適用されると、ランタイム エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-128">Any structural deviation that isn't additive in nature will cause runtime errors when the saved query criteria are applied at runtime.</span></span> <span data-ttu-id="8ae2a-129">クエリの構造が変わらないようにするには、設計されたクエリを使用するか、クエリを構築する共有ロジックを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-129">To ensure that the query structure remains the same, you should either use a designed query or use shared logic that builds up the query.</span></span>

## <a name="processschedulequerycriteriaapplicator-class"></a><span data-ttu-id="8ae2a-130">ProcessScheduleQueryCriteriaApplicator クラス</span><span class="sxs-lookup"><span data-stu-id="8ae2a-130">ProcessScheduleQueryCriteriaApplicator class</span></span>

<span data-ttu-id="8ae2a-131">**ProcessScheduleQueryCriteriaApplicator** クラスは、特定の発生に対して保存されているクエリ基準を、プロセスの実行時に使用されるクエリのランタイム インスタンスに適用するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-131">The **ProcessScheduleQueryCriteriaApplicator** class is used to apply the saved query criteria for a given occurrence to the runtime instance of the query that is used when a process is run.</span></span> <span data-ttu-id="8ae2a-132">この API は、実行中にクエリが保存された基準を受け入れる準備ができた時点で、取り込みプロセスによって呼び出される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-132">This API must be called by an uptaking process at a point in the run where the query is ready to accept the saved criteria.</span></span> <span data-ttu-id="8ae2a-133">クエリを構築する設計されたクエリまたは共有ロジックが使用されている場合、この呼び出しは通常、クエリが正しく初期化された後に発生します。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-133">If a designed query or shared logic that builds up the query is used, this call can typically occur after the query has been correctly initialized.</span></span> <span data-ttu-id="8ae2a-134">この API がどのように使用されるかを示す例については、**CustVendCreatePaymJournal.constructFromAutomationExecutionContract** メソッドを参照してください 。</span><span class="sxs-lookup"><span data-stu-id="8ae2a-134">For an example that shows how this API is used, see the **CustVendCreatePaymJournal.constructFromAutomationExecutionContract** method.</span></span>

| <span data-ttu-id="8ae2a-135">メソッド</span><span class="sxs-lookup"><span data-stu-id="8ae2a-135">Method</span></span> | <span data-ttu-id="8ae2a-136">説明</span><span class="sxs-lookup"><span data-stu-id="8ae2a-136">Description</span></span> |
|---|---|
| `public static void applyCriteriaForOccurrenceExecution(Query _queryToApplyCriteria, RefRecId _scheduleOccurrenceRecId)` | |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]