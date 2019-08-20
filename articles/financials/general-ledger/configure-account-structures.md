---
title: 勘定構造のコンフィギュレーション
description: このトピックでは、勘定構造と財務分析コードについて説明します。
author: aprilolson
manager: AnnBe
ms.date: 06/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c278cefd47b14c44c1949505404d08628cb7f52f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839500"
---
# <a name="configure-account-structures"></a><span data-ttu-id="e9fa4-103">勘定構造のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="e9fa4-103">Configure account structures</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e9fa4-104">勘定構造は、主勘定と財務分析コードを使用し、勘定番号の入力時に使用される順序と値を特定するルールのセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-104">Account structures use the main account and financial dimensions to create a set of rules that determine the order and values used when entering the account number.</span></span> <span data-ttu-id="e9fa4-105">業務に必要な数だけ勘定構造を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-105">You can set up as many account structures as you need for your business.</span></span> <span data-ttu-id="e9fa4-106">勘定構造は会社の元帳の設定に割り当てられ、共有されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-106">The account structures are assigned to a company’s ledger setup, so they can be shared.</span></span>

<span data-ttu-id="e9fa4-107">勘定構造を作成する場合、セグメントの最大数は 11 です。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-107">When creating an account structure, the maximum number of segments is 11.</span></span> <span data-ttu-id="e9fa4-108">これよりも多くのセグメントが必要な場合、ユーザー エクスペリエンスに影響を及ぼすので、設定と要件を十分に評価してください。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-108">If you need more segments than this, thoroughly evaluate your setup and requirements, as it will impact the user experience.</span></span> <span data-ttu-id="e9fa4-109">データ入力時またはユーザー定義フィールドを使用する代わりに階層を使用しているレポートのシナリオでは、セグメントを派生させることができるかどうかを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-109">Consider if a segment could be derived in a reporting scenario using a hierarchy instead of during data entry, or by using a user-defined field.</span></span> <span data-ttu-id="e9fa4-110">たとえば、場所に関するレポートを作成したいが、部門またはコスト センターによって場所を解決できる場合、財務分析コードとしての場所は必要ではありません。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-110">For example, if you want to report on location, but you can figure location by department or cost center, you would not need location as a financial dimension.</span></span> <span data-ttu-id="e9fa4-111">評価後に 11 を超えるセグメントが必要と特定する場合、詳細ルールを使用する追加のセグメントを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-111">If after evaluation you do determine more than 11 segments are needed, you can add additional segments using advanced rules.</span></span>

<span data-ttu-id="e9fa4-112">勘定構造には主勘定が必要です。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-112">Account structures require the main account.</span></span> <span data-ttu-id="e9fa4-113">主勘定は構造の最初のセグメントである必要はありませんが、勘定番号エントリ中に使用される勘定構造を識別します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-113">The main account does not need to be the first segment in the structure, but it does identify what account structure is being used during the account number entry.</span></span> <span data-ttu-id="e9fa4-114">このため、元帳に割り当てられた 1 つの構造に 1 つの主勘定の値のみが存在し、重複しないことになります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-114">Because of this, a main account value can only exist in one structure assigned to the ledger so that they do not overlap.</span></span> <span data-ttu-id="e9fa4-115">勘定構造が識別された後、許可された値の一覧がフィルタ処理され、ユーザーは有効な分析コード値のみからピッキングでき、正しくない仕訳帳入力の可能性を減らせます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-115">After the account structure is identified, the allowed values list is filtered to guide the user through picking only valid dimension values, decreasing the possibility of an incorrect journal entry.</span></span>

> [!NOTE] 
> <span data-ttu-id="e9fa4-116">財務分析コードに対する予算を計画する場合、勘定構造の一部にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-116">If you plan to budget against a financial dimension, it will need to be part of an account structure.</span></span> <span data-ttu-id="e9fa4-117">現在、予算作成は詳細ルールを使用しません。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-117">Budgeting does not currently utilize advanced rules.</span></span>

## <a name="example"></a><span data-ttu-id="e9fa4-118">例</span><span class="sxs-lookup"><span data-stu-id="e9fa4-118">Example</span></span>
<span data-ttu-id="e9fa4-119">勘定構造の設定のベスト プラクティスを説明するため、会社が勘定とビジネスの単位の財務分析コード レベルで貸借対照表勘定 (100000..399999) を追跡するとします。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-119">To illustrate a best practice for setting up an account structure, let's assume that a company wants to track their balance sheet accounts (100000..399999) at the account and business unit financial dimension level.</span></span> <span data-ttu-id="e9fa4-120">収益と経費勘定 (400000..999999) については、財務分析コードの事業単位、部門、および原価部門を追跡します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-120">For revenue and expense accounts (400000..999999), they track financial dimensions Business Unit, Department, and Cost center.</span></span> <span data-ttu-id="e9fa4-121">販売する場合は、顧客の追跡も行います。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-121">If they make a sale, they also like to track Customer.</span></span> <span data-ttu-id="e9fa4-122">このシナリオを使用し、1 つは賃借対照表勘定用、もう 1 つは損益勘定用の、2 つの勘定構造を会社の勘定元帳に割り当てることが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-122">Using this scenario, it would be recommended to have two account structures assigned to the company’s ledger - one for Balance sheet accounts, and one for Profit and Loss accounts.</span></span> <span data-ttu-id="e9fa4-123">ユーザー エクスペリエンスおよび検証の最適化のため、顧客は売上勘定が使用される場合にのみ使用される詳細なルールである必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-123">To optimize the user experience and validation, Customer should be an advanced rule that is only used when a sales account is used.</span></span>

<span data-ttu-id="e9fa4-124">**貸借対照表勘定構造**</span><span class="sxs-lookup"><span data-stu-id="e9fa4-124">**Balance sheet account structure**</span></span>

|<span data-ttu-id="e9fa4-125">主勘定</span><span class="sxs-lookup"><span data-stu-id="e9fa4-125">Main account</span></span>          | <span data-ttu-id="e9fa4-126">事業単位</span><span class="sxs-lookup"><span data-stu-id="e9fa4-126">Business unit</span></span>    |
|----------------------|-----------|
|<span data-ttu-id="e9fa4-127">100000..399999</span><span class="sxs-lookup"><span data-stu-id="e9fa4-127">100000..399999</span></span> | <span data-ttu-id="e9fa4-128">\*;” “</span><span class="sxs-lookup"><span data-stu-id="e9fa4-128">\*;” “</span></span>|

<span data-ttu-id="e9fa4-129">**損益勘定構造**</span><span class="sxs-lookup"><span data-stu-id="e9fa4-129">**Profit and loss account structure**</span></span>

|<span data-ttu-id="e9fa4-130">主勘定</span><span class="sxs-lookup"><span data-stu-id="e9fa4-130">Main account</span></span>          | <span data-ttu-id="e9fa4-131">事業単位</span><span class="sxs-lookup"><span data-stu-id="e9fa4-131">Business unit</span></span>    |<span data-ttu-id="e9fa4-132">部門</span><span class="sxs-lookup"><span data-stu-id="e9fa4-132">Department</span></span>          | <span data-ttu-id="e9fa4-133">コスト センター</span><span class="sxs-lookup"><span data-stu-id="e9fa4-133">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="e9fa4-134">400000..999999</span><span class="sxs-lookup"><span data-stu-id="e9fa4-134">400000..999999</span></span> | <span data-ttu-id="e9fa4-135">\*;” “</span><span class="sxs-lookup"><span data-stu-id="e9fa4-135">\*;” “</span></span>|<span data-ttu-id="e9fa4-136">\*;” “</span><span class="sxs-lookup"><span data-stu-id="e9fa4-136">\*;” “</span></span>|<span data-ttu-id="e9fa4-137">\*;” “</span><span class="sxs-lookup"><span data-stu-id="e9fa4-137">\*;” “</span></span>|<span data-ttu-id="e9fa4-138">\*;” “</span><span class="sxs-lookup"><span data-stu-id="e9fa4-138">\*;” “</span></span>|

<span data-ttu-id="e9fa4-139">**顧客を追加するための詳細ルール**</span><span class="sxs-lookup"><span data-stu-id="e9fa4-139">**Advanced rule for adding a Customer**</span></span>

<span data-ttu-id="e9fa4-140">基準: 主勘定は 400000 と 499999 の間にし、それから顧客を追加します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-140">Criteria: Where Main account is between 400000 and 499999, then add customer.</span></span> <span data-ttu-id="e9fa4-141">それを空白のままにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-141">It cannot be left blank.</span></span>

|<span data-ttu-id="e9fa4-142">顧客</span><span class="sxs-lookup"><span data-stu-id="e9fa4-142">Customer</span></span>         |
|-----------------|
|* |

<span data-ttu-id="e9fa4-143">この簡略化された例では、すべての値と空白が許可されているため \* および “ “ が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-143">In this simplified example, all values and blank are allowed so \* and “ “ are used.</span></span>

## <a name="segments-and-allowed-values"></a><span data-ttu-id="e9fa4-144">区分および許可された値</span><span class="sxs-lookup"><span data-stu-id="e9fa4-144">Segments and allowed values</span></span>
<span data-ttu-id="e9fa4-145">**セグメント**および**許可された値の詳細**セクションは、転記中の検証で参照されるルールの入力の経験のようなグリッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-145">The **Segments** and **Allowed values details** section provides a grid like experience for entering the rules that will be followed on validation during posting.</span></span> <span data-ttu-id="e9fa4-146">グリッドのセルへの直接入力、Excel からのインポート、またはそれを説明する**許可された値の詳細**セクションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-146">You can type directly in the cells in the grid, import it from Excel, or use the **Allowed value details** section to guide you through it.</span></span>

<span data-ttu-id="e9fa4-147">**許可された値の詳細**セクションを使用すると、開始点、相互間、包含点などの**演算子**を使用する基準を作成できます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-147">The **Allowed value details** section guides you through creating criteria using **Operators** such as begins with, is between, includes, and many others.</span></span>

<span data-ttu-id="e9fa4-148">[![許可された値](./media/account.png)](./media/account.png)</span><span class="sxs-lookup"><span data-stu-id="e9fa4-148">[![Allow values](./media/account.png)](./media/account.png)</span></span> 

<span data-ttu-id="e9fa4-149">許可される値は、勘定構造の設定に従って他に選択できる値がない場合に、仕訳帳または勘定配布エントリ ページに既定で設定されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-149">Allowed values will default onto a journal or accounting distribution entry page when there are no other possible values to select according to the account structure setup.</span></span>

<span data-ttu-id="e9fa4-150">ここでは、**損益勘定構造**の例を示します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-150">Here's an example of the **Profit and loss account structure**.</span></span>

|<span data-ttu-id="e9fa4-151">主勘定</span><span class="sxs-lookup"><span data-stu-id="e9fa4-151">Main account</span></span>          | <span data-ttu-id="e9fa4-152">事業単位</span><span class="sxs-lookup"><span data-stu-id="e9fa4-152">Business unit</span></span>    |<span data-ttu-id="e9fa4-153">部門</span><span class="sxs-lookup"><span data-stu-id="e9fa4-153">Department</span></span>          | <span data-ttu-id="e9fa4-154">原価部門</span><span class="sxs-lookup"><span data-stu-id="e9fa4-154">Cost center</span></span>    |
|----------------------|-----------|----------------------|-----------|
|<span data-ttu-id="e9fa4-155">400000..999999</span><span class="sxs-lookup"><span data-stu-id="e9fa4-155">400000..999999</span></span> | <span data-ttu-id="e9fa4-156">002</span><span class="sxs-lookup"><span data-stu-id="e9fa4-156">002</span></span> | <span data-ttu-id="e9fa4-157">022</span><span class="sxs-lookup"><span data-stu-id="e9fa4-157">022</span></span> | <span data-ttu-id="e9fa4-158">014</span><span class="sxs-lookup"><span data-stu-id="e9fa4-158">014</span></span> |

<span data-ttu-id="e9fa4-159">仕訳帳に入力し、損益範囲の勘定を選択する場合、事業単位 002 を選択すると、022 と 014 の値は勘定制御の既定値として設定されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-159">When entering a journal and selecting an account in the profit and loss range, selecting business unit '002' will cause values 022 and 014 to be the default on the account control.</span></span> <span data-ttu-id="e9fa4-160">この動作は、勘定配分ページでも発生します。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-160">This behavior will also occur with the accounting distribution page.</span></span> 

## <a name="more-than-7-criteria-needed"></a><span data-ttu-id="e9fa4-161">7 を超える基準が必要です</span><span class="sxs-lookup"><span data-stu-id="e9fa4-161">More than 7 criteria needed</span></span>

<span data-ttu-id="e9fa4-162">7 を超える基準が必要な場合、次の行に追加し続けることができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-162">If you have more than 7 criteria that are needed, you can continue adding them on the next line.</span></span> <span data-ttu-id="e9fa4-163">**許可された値の詳細**セクションの作業中、7 番目の基準が入力された後、**+ 新規追加**基準が有効ではなくなることがわかります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-163">You will notice when working in the **Allowed value details** section that the **+Add new** criteria is nt longer active after the seventh criteria is entered.</span></span> <span data-ttu-id="e9fa4-164">これは、以下のようなさまざまな要因によります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-164">This is due to many factors such as:</span></span> 
 - <span data-ttu-id="e9fa4-165">列の幅</span><span class="sxs-lookup"><span data-stu-id="e9fa4-165">Column width</span></span> 
 - <span data-ttu-id="e9fa4-166">データを保管する方法</span><span class="sxs-lookup"><span data-stu-id="e9fa4-166">How the data is stored</span></span> 
 - <span data-ttu-id="e9fa4-167">**許可された値の情報**コントロールのパフォーマンス</span><span class="sxs-lookup"><span data-stu-id="e9fa4-167">Performance of the **Allowed value details** control</span></span>
 - <span data-ttu-id="e9fa4-168">有用性</span><span class="sxs-lookup"><span data-stu-id="e9fa4-168">Usability</span></span>  
 
<span data-ttu-id="e9fa4-169">基準を追加するために、**セグメント内で複製**および**許可された値のセクション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-169">To continue to add additional criteria, click **Duplicate in the Segment** and **Allowed values section**.</span></span> <span data-ttu-id="e9fa4-170">これにより新しい明細行に基準がコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-170">This will copy the criteria to a new line.</span></span> <span data-ttu-id="e9fa4-171">**許可された値の詳細**セクションの入力または修正ができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-171">You can then type over or modify the **Allowed value details** section.</span></span>

## <a name="best-practices"></a><span data-ttu-id="e9fa4-172">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="e9fa4-172">Best practices</span></span>
<span data-ttu-id="e9fa4-173">勘定構造を設定する場合、ベスト プラクティスに従うことができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-173">When setting up your account structures there are some best practices you can follow.</span></span> <span data-ttu-id="e9fa4-174">ただし、これはガイダンスですので、業務、拡大計画、およびメンテナンス計画に関する組織全体にわたるディスカッションはディスカッションの一部とみなされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-174">However, this is only guidance so a holistic discussion about your business, growth plan, and maintenance plan should be considered as part of that discussion.</span></span>

- <span data-ttu-id="e9fa4-175">主勘定を勘定構造の先頭にするか、あるいはできるだけ前にすることにより、ユーザーは勘定項目中にガイド付きエクスペリエンスを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-175">Make main account first or as close to the front of the account structure as possible, so users get the best guided experience they can during account entry.</span></span>

- <span data-ttu-id="e9fa4-176">法人間での保守を減らすため、できるだけ多くの勘定構造を再利用してください。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-176">Reuse account structures as much as possible to reduce maintenance across your legal entities.</span></span>

- <span data-ttu-id="e9fa4-177">法人間での変動のため、詳細ルールの使用を考慮することにより勘定構造を再利用できます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-177">For variations across legal entities, consider using advanced rules so that account structures can be reused.</span></span>

- <span data-ttu-id="e9fa4-178">許可された値を定義する場合、できるだけ範囲とワイルドカードを使用してください。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-178">When defining allowed values, use ranges and wildcards as much as possible.</span></span> <span data-ttu-id="e9fa4-179">これによりメンテナンスなしで成長および変更できるだけでなく、このコンフィギュレーションによりシステムがより理想的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-179">This not only allows you to grow and change without maintenance, but the system also performs more ideally with this configuration.</span></span>

- <span data-ttu-id="e9fa4-180">勘定構造のセグメントごとにただアスタリスクを設定するのではなく、詳細ルールにのみ依存するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-180">Do not just put an asterisk for every segment in the account structure and then solely rely on the advanced rules.</span></span> <span data-ttu-id="e9fa4-181">これは管理しにくいだけでなく、メンテナンス中にシステムが転記できなくなるというユーザー エラーを発生させる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-181">This can be difficult to manage and often leads to user error during maintenance that can make the system unable to post.</span></span>

## <a name="account-structure-activation"></a><span data-ttu-id="e9fa4-182">勘定構造の有効化</span><span class="sxs-lookup"><span data-stu-id="e9fa4-182">Account structure activation</span></span>
<span data-ttu-id="e9fa4-183">勘定構造への新しい設定や変更に問題がなければ、それを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-183">When you are satifisfied with your new setup or a change to an account structure, you must activate it.</span></span> <span data-ttu-id="e9fa4-184">勘定構造が元帳に割り当てられている場合、この有効化は実行時間の長いプロセスになることがあり、システムの転記されていないトランザクションは新しい構造と同期される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-184">If an account structure is assigned to a ledger, this activation can be a long running process, as all unposted transactions in the system must be synced to the new structure.</span></span> <span data-ttu-id="e9fa4-185">転記済トランザクションは勘定構造の変更による影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="e9fa4-185">Posted transactions are not impacted with account structure changes.</span></span>

<span data-ttu-id="e9fa4-186">詳細については次を参照してください。[勘定科目表の計画](plan-chart-of-accounts.md)、[財務分析コード](financial-dimensions.md)、[勘定と分析コードの組み合わせの入力 (セグメント化エントリ コントロール)](enter-account-dimension-combinations-segmented-entry-control.md).</span><span class="sxs-lookup"><span data-stu-id="e9fa4-186">For more information, see [Plan your chart of accounts](plan-chart-of-accounts.md), [Financial dimensions](financial-dimensions.md) and [Enter account and dimension combinations (segmented entry control)](enter-account-dimension-combinations-segmented-entry-control.md).</span></span>
