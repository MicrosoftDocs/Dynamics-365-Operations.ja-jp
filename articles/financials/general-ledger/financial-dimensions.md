---
title: "財務分析コード"
description: "このトピックは、財務分析コードのさまざまなタイプと設定方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: d6b7b1219974cb5de1a625d87c3bce2a4439470b
ms.openlocfilehash: 9973d03de031ad2fa5647bb167c12b9231633a22
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---

# <a name="financial-dimensions"></a><span data-ttu-id="b99bf-103">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="b99bf-103">Financial dimensions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b99bf-104">このトピックは、財務分析コードのさまざまなタイプと設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="b99bf-105">共有勘定科目表の勘定の区分として使用する財務分析コードを作成するには、**財務分析コード**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="b99bf-106">財務分析コードには、カスタム分析コードと、エンティティがサポートしている財務分析コードの 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="b99bf-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="b99bf-107">カスタム分析コードは法人間で共有され、値はユーザーにより入力され管理されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="b99bf-108">エンティティがサポートしている分析コードでは、顧客または店舗エンティティなどシステムの他の場所で値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as in Customers or Stores entities.</span></span> <span data-ttu-id="b99bf-109">エンティティがサポートしている分析コードには、法人間で共有されるものや、会社固有のものがあります。</span><span class="sxs-lookup"><span data-stu-id="b99bf-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span>

<span data-ttu-id="b99bf-110">財務分析コードを作成した後、**財務分析コード値**ページを使用して、各財務分析コードに追加のプロパティを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span>

<span data-ttu-id="b99bf-111">財務分析コードを使用して、法人を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="b99bf-112">Microsoft Dynamics 365 for Finance and Operations では、法人を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b99bf-113">ただし、財務分析コードは、法人の運営や業務上の要件に対処するようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-113">However, financial dimensions aren't designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="b99bf-114">Finance および Operations の単位間会計機能は、各トランザクションによって作成された勘定項目のみ対処するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="b99bf-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span>

<span data-ttu-id="b99bf-115">法人として財務分析コードを設定する前に、次の分野の業務プロセスを評価し、この設定が組織で使用できるかどうかを判断します:</span><span class="sxs-lookup"><span data-stu-id="b99bf-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="b99bf-116">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="b99bf-116">Inventory</span></span>
- <span data-ttu-id="b99bf-117">財務分析コードと法人間の販売および購買</span><span class="sxs-lookup"><span data-stu-id="b99bf-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="b99bf-118">売上税の計算および報告</span><span class="sxs-lookup"><span data-stu-id="b99bf-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="b99bf-119">業務レポート</span><span class="sxs-lookup"><span data-stu-id="b99bf-119">Operational reporting</span></span>

<span data-ttu-id="b99bf-120">次に、いくつか制限を示します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="b99bf-121">法人でのみ売上税機能を使用できます。財務分析コードでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="b99bf-122">一部のレポートには、財務分析コードが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="b99bf-123">したがって、財務分析コードによるレポートは、レポートの修正が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b99bf-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="b99bf-124">カスタム分析コード</span><span class="sxs-lookup"><span data-stu-id="b99bf-124">Custom dimensions</span></span>

<span data-ttu-id="b99bf-125">ユーザー定義の財務分析コードを作成するには、**値の使用元**フィールドで、**&lt;&nbsp;カスタム分析コード&nbsp;&gt;** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt;&nbsp;Custom dimension&nbsp;&gt;**.</span></span>

<span data-ttu-id="b99bf-126">主勘定マスクを指定して、分析コード値に対して入力できる情報の量やタイプを制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-126">You can also specify an account mask to limit the amount and type of information that can be entered for dimension values.</span></span> <span data-ttu-id="b99bf-127">文字またはハイフン (-) など、各分析コード値の変化しない文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="b99bf-128">また、分析コード値が作成されるたびに変更される、文字のプレースホルダーとなる番号記号 (\#) とアンパサンド (&) を入力できます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-128">You can also enter number signs (\#) and ampersands (&) as placeholders for characters that will change every time that a dimension value is created.</span></span> <span data-ttu-id="b99bf-129">番号のプレースホルダーとして番号記号 (\#)、文字のプレースホルダーとしてアンパサンド (&) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="b99bf-130">マスクの書式設定のためのフィールドは、**値の使用元**フィールドで**&lt;&nbsp;カスタム分析コード&nbsp;&gt;** を選択した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-130">The field for the format mask is available only when you select **&lt;&nbsp;Custom dimension&nbsp;&gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="b99bf-131">**例**</span><span class="sxs-lookup"><span data-stu-id="b99bf-131">**Example**</span></span>

<span data-ttu-id="b99bf-132">分析コード値を文字 2 桁 (CC)、番号 3 桁に制限するには、マスクの書式設定として **CC-\#\#\#** を入力します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="b99bf-133">エンティティがサポートする分析コード</span><span class="sxs-lookup"><span data-stu-id="b99bf-133">Entity-backed dimensions</span></span>

<span data-ttu-id="b99bf-134">エンティティがサポートする分析コードを作成するには、**値の使用元** フィールドで、財務分析コードの基になるシステム定義エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="b99bf-135">財務分析コード値がそのエンティティから作成されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="b99bf-136">たとえば、プロジェクトの分析コード値を作成するには、**プロジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="b99bf-137">各プロジェクト名に対して分析コード値が作成されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="b99bf-138">**財務分析コード値**ページには、エンティティの値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="b99bf-139">それらの値が会社固有のものである場合、そのページでは会社も表示されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="b99bf-140">分析コードの有効化</span><span class="sxs-lookup"><span data-stu-id="b99bf-140">Activating dimensions</span></span>

<span data-ttu-id="b99bf-141">財務分析コードを有効にすると、財務分析コードの名前が含まれるようテーブルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="b99bf-142">削除された分析コードは削除されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="b99bf-143">財務分析コードを有効にする前に、分析コード値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="b99bf-144">ただし、財務分析コードは有効化されていないと消費できません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="b99bf-145">たとえば、財務分析コードが有効化される前に、勘定構造に財務分析コードを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="b99bf-146">**有効化**を選択すると、すべての分析コードが更新され、ステータスの変更を表示します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-146">When you select **Activate**, all dimensions are updated and show status changes.</span></span>

## <a name="translations"></a><span data-ttu-id="b99bf-147">翻訳</span><span class="sxs-lookup"><span data-stu-id="b99bf-147">Translations</span></span>

<span data-ttu-id="b99bf-148">**テキスト翻訳** ページでは、様々な言語で、選択した財務分析コードのテキストを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="b99bf-149">**主勘定翻訳** ページでは、様々な言語で、主勘定のテキストを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="b99bf-150">法人の上書き</span><span class="sxs-lookup"><span data-stu-id="b99bf-150">Legal entity overrides</span></span>

<span data-ttu-id="b99bf-151">分析コードには、ある法人に対して有効でないものもあります。</span><span class="sxs-lookup"><span data-stu-id="b99bf-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="b99bf-152">また、一部の分析コードは、特定の期間にだけ有効な場合があります。</span><span class="sxs-lookup"><span data-stu-id="b99bf-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="b99bf-153">これらのケースでは、**法人の上書き** セクションを使用して、分析コードを保留にする法人の指定、法人のオーナーの指定、分析コードの有効期間の指定ができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="b99bf-154">削除中の財務分析コード</span><span class="sxs-lookup"><span data-stu-id="b99bf-154">Deleting financial dimensions</span></span>

<span data-ttu-id="b99bf-155">データの整合性を維持するために財務分析コードを削除されることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="b99bf-156">財務分析コードを削除しようとする場合は、次の基準が評価されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="b99bf-157">転記済または未転記のトランザクションで、もしくは任意の分析コード値の組み合わせで財務分析コードが使用されているか。</span><span class="sxs-lookup"><span data-stu-id="b99bf-157">Has the financial dimension been used on any posted or unposted transactions, or in any type of dimension value combination?</span></span>
- <span data-ttu-id="b99bf-158">財務分析コードは有効な勘定構造、詳細なルール構造、もしくは財務分析コードセットで使用されているか。</span><span class="sxs-lookup"><span data-stu-id="b99bf-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="b99bf-159">財務分析コードは、既定の財務分析コードの統合形式の一部であるか。</span><span class="sxs-lookup"><span data-stu-id="b99bf-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="b99bf-160">財務分析コードは既定の分析コードとして設定されているか。</span><span class="sxs-lookup"><span data-stu-id="b99bf-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="b99bf-161">条件が合致した場合は、財務分析コードを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>

## <a name="default-dimension-values"></a><span data-ttu-id="b99bf-162">既定の分析コード値</span><span class="sxs-lookup"><span data-stu-id="b99bf-162">Default dimension values</span></span>

<span data-ttu-id="b99bf-163">顧客および仕入先などのマスター レコードの値は、新しい分析コードの既定値として使用できます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-163">You can use values from master records, such as customer and vendor, as default values in new dimensions.</span></span> <span data-ttu-id="b99bf-164">新しい分析コードが作成されると、マスター レコード ID は、マスター レコードの分析コード値で入力されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-164">When the new dimensions are created, the master record ID is entered in the dimension values for those master records.</span></span> <span data-ttu-id="b99bf-165">たとえば、新しい顧客を作成するときに、顧客 ID は顧客分析コードで入力されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-165">For example, when you create a new customer, the customer ID is entered in the customer dimension.</span></span> <span data-ttu-id="b99bf-166">販売注文、請求書、または顧客 ID が必要なその他のドキュメントを作成するときは、既存の既定ルールが使用され、顧客 ID がドキュメントに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-166">When you create sales orders, invoices, or other documents that require a customer ID, the existing defaulting rules are used, and the customer ID is added to the document.</span></span>

<span data-ttu-id="b99bf-167">この機能は、分析コードの設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-167">This feature is controlled by a setting in the dimension.</span></span> <span data-ttu-id="b99bf-168">**DimensionName** が分析コードの名前である場合、この設定の名前は**作成されたそれぞれの新しい DimensionName でこの分析コードに値をコピーする**です。</span><span class="sxs-lookup"><span data-stu-id="b99bf-168">This setting is named **Copy values to this dimension on each new DimensionName created**, where **DimensionName** is the name of the dimension.</span></span> <span data-ttu-id="b99bf-169">既定では、機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="b99bf-169">By default, the feature is turned off.</span></span> <span data-ttu-id="b99bf-170">ただし、いつでも有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-170">However, it can be turned on at any time.</span></span>

<span data-ttu-id="b99bf-171">分析コードのレコードが既に存在する場合、この機能を有効にすると、マスター レコードが更新されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-171">If records already exist for the dimension, the master records are updated when you turn the feature on.</span></span> <span data-ttu-id="b99bf-172">ただし、既存のドキュメントおよびトランザクションは更新されません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-172">However, existing documents and transactions aren't updated.</span></span>

## <a name="derived-dimensions"></a><span data-ttu-id="b99bf-173">派生分析コード</span><span class="sxs-lookup"><span data-stu-id="b99bf-173">Derived dimensions</span></span>

<span data-ttu-id="b99bf-174">ドキュメントにその分析コードを入力すると、他の分析コードの情報が自動的に入力されるように分析コードをコンフィギュレーションすることができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-174">You can configure a dimension so that information for other dimensions is automatically entered when you enter that dimension in a document.</span></span> <span data-ttu-id="b99bf-175">たとえば、コスト センター 10 を入力した場合、値 **20** が部門分析コードに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-175">For example, if you enter cost center 10, a value of **20** can be automatically entered in the department dimension.</span></span>

<span data-ttu-id="b99bf-176">分析コードのページに派生した値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-176">You can set up derived values on the dimensions page.</span></span>

1. <span data-ttu-id="b99bf-177">分析コードを選択し、その後**派生分析コード**を選択します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-177">Select a dimension and then select **Derived dimensions**.</span></span>

    <span data-ttu-id="b99bf-178">**派生分析コード**ページには、グリッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b99bf-178">The **Derived dimensions** page includes a grid.</span></span> <span data-ttu-id="b99bf-179">選択した分析コードのセグメントは、このグリッドの最初の列です。</span><span class="sxs-lookup"><span data-stu-id="b99bf-179">The selected dimension segment is the first column in this grid.</span></span>

2. <span data-ttu-id="b99bf-180">派生するセグメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-180">Add the segments that should be derived.</span></span> <span data-ttu-id="b99bf-181">各セグメントは、列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-181">Each segment appears as a column.</span></span>

<span data-ttu-id="b99bf-182">最初の列で分析コードから派生する分析コードの組み合わせを入力します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-182">Enter the dimension combinations that should be derived from the dimension in the first column.</span></span> <span data-ttu-id="b99bf-183">たとえば、コスト センターを部門および場所の派生元の分析コードとして使用するには、コスト センター 10、部門 20、および場所 30 を入力します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-183">For example, to use the cost center as the dimension that the department and location are derived from, enter cost center 10, department 20, and location 30.</span></span> <span data-ttu-id="b99bf-184">次に、マスター レコードまたはトランザクションのページに、コスト センター 10 を入力すると、部門 20 および場所 30 が既定で入力されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-184">Then, when you enter cost center 10 in a master record or on a transaction page, department 20 and location 30 are entered by default.</span></span>

<span data-ttu-id="b99bf-185">派生分析コードのプロセスは、既存の派生分析コードの値を上書きしません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-185">The derived dimension process doesn't override existing values for derived dimensions.</span></span> <span data-ttu-id="b99bf-186">たとえば、コスト センター 10 を入力し、他の分析コードを入力しない場合、部門 20 と場所 30 は既定で入力されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-186">For example, if you enter cost center 10, and no other dimension is entered, department 20 and location 30 are entered by default.</span></span> <span data-ttu-id="b99bf-187">ただし、コスト センターを変更する場合は、既に確立されている値は変更されません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-187">However, if you change the cost center, the values that have already been established aren't changed.</span></span> <span data-ttu-id="b99bf-188">このため、マスター レコードに既定の分析コードを設定することができ、それらの分析コードは、派生した分析コードによって変更されません。</span><span class="sxs-lookup"><span data-stu-id="b99bf-188">Therefore, you can establish default dimensions on master records, and those dimensions won't be changed by derived dimensions.</span></span>

### <a name="derived-dimensions-and-entities"></a><span data-ttu-id="b99bf-189">派生分析コードおよびエンティティ</span><span class="sxs-lookup"><span data-stu-id="b99bf-189">Derived dimensions and entities</span></span>

<span data-ttu-id="b99bf-190">エンティティを使用して、派生分析コードのセグメントと値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-190">You can set up the derived dimensions segments and values by using entities.</span></span>

- <span data-ttu-id="b99bf-191">派生分析コードのエンティティはドライブ分析コードと、そこで使用されるセグメントを設定します。</span><span class="sxs-lookup"><span data-stu-id="b99bf-191">The Derived dimensions entity sets up the driving dimensions and the segments that are used for those dimensions.</span></span>
- <span data-ttu-id="b99bf-192">DerivedDimensionValue エンティティでは、各ドライブ分析コード用の派生の値をインポートできます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-192">The DerivedDimensionValue entity lets you import the values that should be derived for each driving dimension.</span></span>

<span data-ttu-id="b99bf-193">エンティティを使用してデータをインポートするときに、そのエンティティが分析コードをインポートする場合は、エンティティが具体的にそれらの分析コードを上書きしない限り、インポート中に派生分析コードのルールが適用されます。</span><span class="sxs-lookup"><span data-stu-id="b99bf-193">When you use an entity to import data, if that entity imports dimensions, the derived dimension rules are applied during the import unless the entity specifically overrides those dimensions.</span></span>

<span data-ttu-id="b99bf-194">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b99bf-194">For more information, see the following topics:</span></span>

- [<span data-ttu-id="b99bf-195">財務分析コードの定義</span><span class="sxs-lookup"><span data-stu-id="b99bf-195">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="b99bf-196">財務分析コード用の既定テンプレートの管理</span><span class="sxs-lookup"><span data-stu-id="b99bf-196">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

