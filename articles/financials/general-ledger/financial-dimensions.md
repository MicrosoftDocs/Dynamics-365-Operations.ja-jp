---
title: "財務分析コード"
description: "このトピックは、財務分析コードのさまざまなタイプと設定方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ems.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25871
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3950dc3fcd1e293802c88bf2616a27e139b48399
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="financial-dimensions"></a><span data-ttu-id="ae228-103">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="ae228-103">Financial dimensions</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ae228-104">このトピックは、財務分析コードのさまざまなタイプと設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="ae228-104">This topic explains the various types of financial dimensions and how they are set up.</span></span>

<span data-ttu-id="ae228-105">共有勘定科目表の勘定の区分として使用する財務分析コードを作成するには、**財務分析コード**ページを使用します。</span><span class="sxs-lookup"><span data-stu-id="ae228-105">Use the **Financial dimensions** page to create financial dimensions that you can use as account segments for charts of accounts.</span></span> <span data-ttu-id="ae228-106">財務分析コードには、カスタム分析コードと、エンティティがサポートしている財務分析コードの 2 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="ae228-106">There are two types of financial dimensions: custom dimensions and entity-backed dimensions.</span></span> <span data-ttu-id="ae228-107">カスタム分析コードは法人間で共有され、値はユーザーにより入力され管理されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-107">Custom dimensions are shared across legal entities, and the values are entered and maintained by users.</span></span> <span data-ttu-id="ae228-108">エンティティがサポートしている分析コードのために、[顧客] や [店舗] エンティティなどシステムの他の場所で値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-108">For entity-backed dimensions, the values are defined somewhere else in the system, such as Customers or Stores entities.</span></span> <span data-ttu-id="ae228-109">エンティティがサポートしている分析コードには、法人間で共有されるものや、会社固有のものがあります。</span><span class="sxs-lookup"><span data-stu-id="ae228-109">Some entity-backed dimensions are shared across legal entities, whereas other entity-backed dimensions are company-specific.</span></span> 

<span data-ttu-id="ae228-110">財務分析コードを作成した後、[**財務分析コード値**] ページを使用して、各財務分析コードに追加のプロパティを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="ae228-110">After you've created the financial dimensions, use the **Financial dimension values** page to assign additional properties to each financial dimension.</span></span> 

<span data-ttu-id="ae228-111">財務分析コードを使用して、法人を表すことができます。</span><span class="sxs-lookup"><span data-stu-id="ae228-111">You can use financial dimensions to represent legal entities.</span></span> <span data-ttu-id="ae228-112">Microsoft Dynamics 365 for Finance および Operations、Enterprise Edition では、法人を作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="ae228-112">You don't have to create the legal entities in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="ae228-113">ただし、財務分析コードは、法人の運営や業務上の要件に対処するようには設計されていません。</span><span class="sxs-lookup"><span data-stu-id="ae228-113">However, financial dimensions aren’t designed to address the operational or business requirements of legal entities.</span></span> <span data-ttu-id="ae228-114">Finance および Operations の単位間会計機能は、各トランザクションによって作成された勘定項目のみ対処するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="ae228-114">The interunit accounting functionality in Finance and Operations is designed to address only the accounting entries that are created by each transaction.</span></span> 

<span data-ttu-id="ae228-115">法人として財務分析コードを設定する前に、次の分野の業務プロセスを評価し、この設定が組織で使用できるかどうかを判断します:</span><span class="sxs-lookup"><span data-stu-id="ae228-115">Before you set up financial dimensions as legal entities, evaluate your business processes in the following areas to determine whether this setup will work for your organization:</span></span>

- <span data-ttu-id="ae228-116">棚卸資産</span><span class="sxs-lookup"><span data-stu-id="ae228-116">Inventory</span></span>
- <span data-ttu-id="ae228-117">財務分析コードと法人間の販売および購買</span><span class="sxs-lookup"><span data-stu-id="ae228-117">Sales and purchases between financial dimensions and legal entities</span></span>
- <span data-ttu-id="ae228-118">売上税の計算および報告</span><span class="sxs-lookup"><span data-stu-id="ae228-118">Sales tax calculation and reporting</span></span>
- <span data-ttu-id="ae228-119">業務レポート</span><span class="sxs-lookup"><span data-stu-id="ae228-119">Operational reporting</span></span>

<span data-ttu-id="ae228-120">次に、いくつか制限を示します。</span><span class="sxs-lookup"><span data-stu-id="ae228-120">Here are some of the limitations:</span></span>

- <span data-ttu-id="ae228-121">法人でのみ売上税機能を使用できます。財務分析コードでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="ae228-121">You can use sales tax functionality only with legal entities, not with financial dimensions.</span></span>
- <span data-ttu-id="ae228-122">一部のレポートには、財務分析コードが含まれていません。</span><span class="sxs-lookup"><span data-stu-id="ae228-122">Some reports don't include financial dimensions.</span></span> <span data-ttu-id="ae228-123">したがって、財務分析コードによるレポートは、レポートの修正が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae228-123">Therefore, to report by financial dimension, you might have to modify the reports.</span></span>

## <a name="custom-dimensions"></a><span data-ttu-id="ae228-124">カスタム分析コード</span><span class="sxs-lookup"><span data-stu-id="ae228-124">Custom dimensions</span></span>

<span data-ttu-id="ae228-125">ユーザー定義の財務分析コードを作成するには、[**値の使用元**] フィールドで**&lt;カスタム分析コード&gt;**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae228-125">To create a user-defined financial dimension, in the **Use values from** field, select **&lt; Custom dimension &gt;**.</span></span> <span data-ttu-id="ae228-126">また主勘定マスクを指定して、分析コード値に対して入力できる情報の量やタイプを制限することもできます。</span><span class="sxs-lookup"><span data-stu-id="ae228-126">You can also specify an account mask to limit the amount and type of information that you can enter for dimension values.</span></span> <span data-ttu-id="ae228-127">文字またはハイフン (-) など、各分析コード値の変化しない文字を入力できます。</span><span class="sxs-lookup"><span data-stu-id="ae228-127">You can enter characters that remain the same for each dimension value, such as letters or a hyphen (-).</span></span> <span data-ttu-id="ae228-128">また、分析コード値が作成されるたびに変更される、番号と文字のプレースホルダーとなる番号記号 (\#) とアンパサンド (&) を入力できます。</span><span class="sxs-lookup"><span data-stu-id="ae228-128">You can also enter number signs (\#) and ampersands (&) as placeholders for letters and numbers that will change every time that a dimension value is created.</span></span> <span data-ttu-id="ae228-129">番号のプレースホルダーとして番号記号 (\#)、文字のプレースホルダーとしてアンパサンド (&) を使用します。</span><span class="sxs-lookup"><span data-stu-id="ae228-129">Use a number sign (\#) as a placeholder for a number and an ampersand (&) as a placeholder for a letter.</span></span> <span data-ttu-id="ae228-130">マスクの書式設定のためのフィールドは、[**値の使用元**] フィールドで**&lt;カスタム分析コード&gt;**を選択した場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ae228-130">The field for the format mask is available only when you select **&lt; Custom dimension &gt;** in the **Use values from** field.</span></span>

<span data-ttu-id="ae228-131">**例**</span><span class="sxs-lookup"><span data-stu-id="ae228-131">**Example**</span></span>

<span data-ttu-id="ae228-132">分析コード値を文字 2 桁 (CC)、番号 3 桁に制限するには、マスクの書式設定として **CC-\#\#\#** を入力します。</span><span class="sxs-lookup"><span data-stu-id="ae228-132">To limit the dimension value to the letters "CC" and three numbers, enter **CC-\#\#\#** as the format mask.</span></span>

## <a name="entity-backed-dimensions"></a><span data-ttu-id="ae228-133">エンティティがサポートする分析コード</span><span class="sxs-lookup"><span data-stu-id="ae228-133">Entity-backed dimensions</span></span>

<span data-ttu-id="ae228-134">エンティティがサポートする分析コードを作成するには、[**値の使用元**] フィールドで、財務分析コードの基になるシステム定義エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="ae228-134">To create an entity-backed financial dimension, in the **Use values from** field, select a system-defined entity to base the financial dimension on.</span></span> <span data-ttu-id="ae228-135">財務分析コード値がそのエンティティから作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-135">Financial dimension values are then created from that entity.</span></span> <span data-ttu-id="ae228-136">たとえば、プロジェクトの分析コード値を作成するには、[**プロジェクト**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="ae228-136">For example, to create dimension values for projects, select **Projects**.</span></span> <span data-ttu-id="ae228-137">各プロジェクト名に対して分析コード値が作成されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-137">A dimension value is then created for each project name.</span></span> <span data-ttu-id="ae228-138">**財務分析コード値**ページには、エンティティの値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-138">The **Financial dimension values** page shows the values for the entity.</span></span> <span data-ttu-id="ae228-139">それらの値が会社固有のものである場合、そのページでは会社も表示されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-139">If those values are company-specific, the page also shows the company.</span></span>

## <a name="activating-dimensions"></a><span data-ttu-id="ae228-140">分析コードの有効化</span><span class="sxs-lookup"><span data-stu-id="ae228-140">Activating dimensions</span></span>

<span data-ttu-id="ae228-141">財務分析コードを有効にすると、財務分析コードの名前が含まれるようテーブルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-141">When you activate a financial dimension, the table is updated so that it includes the name of the financial dimension.</span></span> <span data-ttu-id="ae228-142">削除された分析コードは削除されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-142">Deleted dimensions are removed.</span></span> <span data-ttu-id="ae228-143">財務分析コードを有効にする前に、分析コード値を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="ae228-143">You can enter dimension values before you activate a financial dimension.</span></span> <span data-ttu-id="ae228-144">ただし、財務分析コードは有効化されていないと消費できません。</span><span class="sxs-lookup"><span data-stu-id="ae228-144">However, a financial dimension can't be consumed anywhere until it's activated.</span></span> <span data-ttu-id="ae228-145">たとえば、財務分析コードが有効化される前に、勘定構造に財務分析コードを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="ae228-145">For example, you can't add a financial dimension to an account structure until the financial dimension has been activated.</span></span> <span data-ttu-id="ae228-146">**有効化**をクリックすると、すべての分析コードが更新され、ステータスの変更を表示します。</span><span class="sxs-lookup"><span data-stu-id="ae228-146">When you click **Activate**, all dimensions are updated and show status changes.</span></span> 

## <a name="translations"></a><span data-ttu-id="ae228-147">翻訳</span><span class="sxs-lookup"><span data-stu-id="ae228-147">Translations</span></span>

<span data-ttu-id="ae228-148">[**テキスト翻訳**] ページでは、様々な言語で、選択した財務分析コードのテキストを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="ae228-148">On the **Text translation** page, you can enter text for the selected financial dimension in various languages.</span></span> <span data-ttu-id="ae228-149">[**主勘定翻訳**] ページでは、様々な言語で、主勘定のテキストを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="ae228-149">On the **Main account translation** page, you can enter text for the main account in various languages.</span></span> 

## <a name="legal-entity-overrides"></a><span data-ttu-id="ae228-150">法人の上書き</span><span class="sxs-lookup"><span data-stu-id="ae228-150">Legal entity overrides</span></span>

<span data-ttu-id="ae228-151">分析コードには、ある法人に対して有効でないものもあります。</span><span class="sxs-lookup"><span data-stu-id="ae228-151">Not all dimensions are valid for all legal entities.</span></span> <span data-ttu-id="ae228-152">また、一部の分析コードは、特定の期間にだけ有効な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ae228-152">Additionally, some dimensions might be relevant only for a specific period.</span></span> <span data-ttu-id="ae228-153">これらのケースでは、[**法人の上書き**] セクションを使用して、分析コードを保留にする法人の指定、法人のオーナーの指定、分析コードの有効期間の指定ができます。</span><span class="sxs-lookup"><span data-stu-id="ae228-153">In these cases, you can use the **Legal entity overrides** section to specify the companies that the dimension should be suspended for, the owner, and the period when the dimension is active.</span></span>

## <a name="deleting-financial-dimensions"></a><span data-ttu-id="ae228-154">削除中の財務分析コード</span><span class="sxs-lookup"><span data-stu-id="ae228-154">Deleting financial dimensions</span></span>

<span data-ttu-id="ae228-155">データの整合性を維持するために財務分析コードを削除されることはほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="ae228-155">To help maintain referential integrity of the data, financial dimensions can rarely be deleted.</span></span> <span data-ttu-id="ae228-156">財務分析コードを削除しようとする場合は、次の基準が評価されます。</span><span class="sxs-lookup"><span data-stu-id="ae228-156">If you try to delete a financial dimension, the following criteria are evaluated:</span></span>

- <span data-ttu-id="ae228-157">財務分析コードが転記済または未転記のトランザクションで使用されている、もしくは任意の分析コード値の組み合わせであるか。</span><span class="sxs-lookup"><span data-stu-id="ae228-157">Has the financial dimension been used on any posted or unposted transactions, or any type of dimension value combination?</span></span>
- <span data-ttu-id="ae228-158">財務分析コードは有効な勘定構造、詳細なルール構造、もしくは財務分析コードセットで使用されているか。</span><span class="sxs-lookup"><span data-stu-id="ae228-158">Is the financial dimension used in any active account structure, advanced rule structure, or financial dimension set?</span></span>
- <span data-ttu-id="ae228-159">財務分析コードは、既定の財務分析コードの統合形式の一部であるか。</span><span class="sxs-lookup"><span data-stu-id="ae228-159">Is the financial dimension part of a default financial dimension integration format?</span></span>
- <span data-ttu-id="ae228-160">財務分析コードは既定の分析コードとして設定されているか。</span><span class="sxs-lookup"><span data-stu-id="ae228-160">Has the financial dimension been set up as a default dimension?</span></span>

<span data-ttu-id="ae228-161">条件が合致した場合は、財務分析コードを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="ae228-161">If any of the criteria are met, you can't delete the financial dimension.</span></span>


<span data-ttu-id="ae228-162">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ae228-162">For more information, see the following topics:</span></span>
- [<span data-ttu-id="ae228-163">財務分析コードの定義</span><span class="sxs-lookup"><span data-stu-id="ae228-163">Define financial dimensions</span></span>](tasks/define-financial-dimensions.md)
- [<span data-ttu-id="ae228-164">財務分析コード用の既定テンプレートの管理</span><span class="sxs-lookup"><span data-stu-id="ae228-164">Maintain financial dimension default templates</span></span>](tasks/maintain-financial-dimension-default-templates.md)

