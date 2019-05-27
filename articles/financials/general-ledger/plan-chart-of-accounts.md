---
title: 勘定科目表の計画
description: このトピックでは、組織の勘定科目表を計画する際に役立つ情報を提供します。
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93d5ef19a4b1cb2885c611c8675ac06fd841ac56
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556642"
---
# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="1c816-103">勘定科目表の計画</span><span class="sxs-lookup"><span data-stu-id="1c816-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c816-104">このトピックでは、組織の勘定科目表を計画する際に役立つ情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c816-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="1c816-105">組織の財務情報を追跡および管理するには、勘定科目表を設定します。</span><span class="sxs-lookup"><span data-stu-id="1c816-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="1c816-106">勘定科目表は、財務フレームワークを定義する勘定の集合です。</span><span class="sxs-lookup"><span data-stu-id="1c816-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="1c816-107">これらの勘定でトランザクションをさらに追跡するには、区分を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="1c816-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="1c816-108">これらのセグメントは、財務分析コードと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1c816-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="1c816-109">たとえば、経費勘定には、部門、コスト センター、および目的という財務分析コードが含まれる場合があります。</span><span class="sxs-lookup"><span data-stu-id="1c816-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="1c816-110">ユーザー定義のルールは、これらの財務分析コードを主勘定およびその他の財務分析コードに関連付ける方法や、トランザクションを入力する方法を指示します。</span><span class="sxs-lookup"><span data-stu-id="1c816-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="1c816-111">これらのユーザー定義のルールは勘定構造または詳細ルールと呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="1c816-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="1c816-112">勘定科目表は、法人の一般会計科目の構造化された一覧です。</span><span class="sxs-lookup"><span data-stu-id="1c816-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="1c816-113">この一覧は、所轄官庁や株主への財務報告を準備するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="1c816-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="1c816-114">勘定はまずタイプごとにグループ化され、さらに大きなカテゴリに集約されます。</span><span class="sxs-lookup"><span data-stu-id="1c816-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="1c816-115">最も大きなレベルでは、収益および費用 (営業勘定) と資産および負債 (残高勘定) にグループ化されます。</span><span class="sxs-lookup"><span data-stu-id="1c816-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="1c816-116">勘定科目表は、組織のすべての法人によって共有および使用できます。</span><span class="sxs-lookup"><span data-stu-id="1c816-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="1c816-117">法人に使用される勘定科目表は、**元帳** ページで定義されます。</span><span class="sxs-lookup"><span data-stu-id="1c816-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="1c816-118">組織の勘定科目表の構成を計画するときは、次のようなさまざまな要因を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c816-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="1c816-119">組織が拠点を置く国または地域の報告要件</span><span class="sxs-lookup"><span data-stu-id="1c816-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="1c816-120">自分の法人のレポート要件</span><span class="sxs-lookup"><span data-stu-id="1c816-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="1c816-121">外部組織または組織にとって必要な細分化の程度</span><span class="sxs-lookup"><span data-stu-id="1c816-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="1c816-122">**勘定科目表** ページで、勘定科目表を作成します。</span><span class="sxs-lookup"><span data-stu-id="1c816-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="1c816-123">主勘定は、**勘定科目表** ページまたは **主勘定** ページから作成できます。</span><span class="sxs-lookup"><span data-stu-id="1c816-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="1c816-124">自分の主勘定には、勘定科目表の区切り文字として使用される特殊文字を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="1c816-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="1c816-125">それ以外の場合、動作が不安定になることがあります。また、勘定と分析コードの組み合わせを入力するとき、常にルックアップまたはダイアログ ボックスを使用する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="1c816-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="1c816-126">詳細については、「[主勘定の作成](tasks/create-main-account.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c816-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1c816-127">Microsoft Dynamics for Finance and Operations バージョン 8.0 (2018 年 4 月) では、**総勘定元帳パラメーター** ページから勘定科目表の区切り記号を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="1c816-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="1c816-128">主勘定を主勘定カテゴリにリンクし、既定の財務諸表を変更を加えずに使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1c816-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="1c816-129">したがって、より迅速かつ簡単にレポートを作成および管理できます。</span><span class="sxs-lookup"><span data-stu-id="1c816-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="1c816-130">**勘定構造のコンフィギュレーション** ページで、勘定構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="1c816-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="1c816-131">勘定構造では、有効な組み合わせを定義します。</span><span class="sxs-lookup"><span data-stu-id="1c816-131">Account structures define valid combinations.</span></span> <span data-ttu-id="1c816-132">これらの組み合わせは、主勘定と共に、勘定科目表を形成します。</span><span class="sxs-lookup"><span data-stu-id="1c816-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="1c816-133">詳細については、「[勘定構造の作成](tasks/create-account-structures.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c816-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="1c816-134">**法人の上書き**</span><span class="sxs-lookup"><span data-stu-id="1c816-134">**Legal entity overrides**</span></span>

<span data-ttu-id="1c816-135">主勘定には、ある法人に対して有効でないものもあり、特定の期間にだけ有効な主勘定もあります。</span><span class="sxs-lookup"><span data-stu-id="1c816-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="1c816-136">このシナリオでは、**法人の上書き** セクションを使用して、主勘定を保留にする法人の識別、法人のオーナーの識別、分析コードの有効期間の識別ができます。</span><span class="sxs-lookup"><span data-stu-id="1c816-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="1c816-137">共有レベルの上書きを、法人レベルの上書きより強い制限にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="1c816-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="1c816-138">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="1c816-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="1c816-139">財務分析コード</span><span class="sxs-lookup"><span data-stu-id="1c816-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="1c816-140">詳細ルール構造の作成と割り当て</span><span class="sxs-lookup"><span data-stu-id="1c816-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)
