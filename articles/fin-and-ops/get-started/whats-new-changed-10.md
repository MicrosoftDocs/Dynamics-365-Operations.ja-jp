---
title: Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能
description: このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 のプレビュー中の機能について説明します。 このバージョンは、2019 年 4 月にリリースされます。
author: tonyafehr
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: a362a31d-44df-45c5-b698-64c5264c592e
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: Release 10
ms.openlocfilehash: 3e7c99b374cf74325ecee9993038a2035add23d2
ms.sourcegitcommit: bacec397ee48ac583596be156c87ead474ee07df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "777119"
---
# <a name="whats-new-or-changed-in-finance-and-operations-version-100-april-2019"></a><span data-ttu-id="a5136-104">Finance and Operations バージョン 10.0 (2019 年 4 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="a5136-104">What's new or changed in Finance and Operations version 10.0 (April 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5136-105">このトピックでは Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5136-105">This topic describes features that are new or changed in Microsoft Dynamics 365 for Finance and Operations version 10.0.</span></span> <span data-ttu-id="a5136-106">このバージョンのビルド番号は 10.0.8 です。</span><span class="sxs-lookup"><span data-stu-id="a5136-106">This version has a build number of 10.0.8.</span></span> <span data-ttu-id="a5136-107">バージョン 10.0 の詳細については [追加リソース](whats-new-changed-10.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-107">For more information about version 10.0, see [Additional resources](whats-new-changed-10.md#additional-resources).</span></span>

<span data-ttu-id="a5136-108">Microsoft Dynamics 365 for Retail の機能については [Dynamics 365 for Retail (2019 年 4 月) の新機能および変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-108">To learn about the features in Microsoft Dynamics 365 for Retail, see [What's new or changed in Dynamics 365 for Retail (April 2019)](https://docs.microsoft.com/dynamics365/unified-operations/retail/get-started/april-whats-new).</span></span>

## <a name="extensibility-enhancements"></a><span data-ttu-id="a5136-109">拡張性の強化</span><span class="sxs-lookup"><span data-stu-id="a5136-109">Extensibility enhancements</span></span>

<span data-ttu-id="a5136-110">Finance and Operations の今回のリリースでは、列挙、メタデータ、メソッドの強化など、拡張性をサポートするために、さまざまな拡張機能の強化が加えられています。</span><span class="sxs-lookup"><span data-stu-id="a5136-110">In this release of Finance and Operations, numerous extensibility enhancements have been made to support extensibility including enhancements to enumerations, metadata, and methods.</span></span> <span data-ttu-id="a5136-111">詳細については、[Dynamics 365 for Finance and Operations バージョン 10.0 で変更された拡張機能](../../dev-itpro/extensibility/extensibility-changes-10.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-111">For detailed information, see [Extensibility changes in Dynamics 365 for Finance and Operations version 10.0](../../dev-itpro/extensibility/extensibility-changes-10.md).</span></span>

## <a name="catch-weight-product-processing-with-warehouse-management"></a><span data-ttu-id="a5136-112">倉庫管理による CW 製品の処理</span><span class="sxs-lookup"><span data-stu-id="a5136-112">Catch weight product processing with warehouse management</span></span>
<span data-ttu-id="a5136-113">この機能を使用すると、倉庫管理プロセス内の CW 製品を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a5136-113">This feature allows you to use catch weight products within warehouse management processes.</span></span> <span data-ttu-id="a5136-114">この機能は、今回のリリースの制限対象者のみに提供できます。</span><span class="sxs-lookup"><span data-stu-id="a5136-114">This feature is only available to a limited audience for this release.</span></span> 

<span data-ttu-id="a5136-115">詳細については、[倉庫管理の CW 製品処理](../../supply-chain/warehousing/catch-weight-processing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-115">For more information, see [Catch weight product processing with warehouse management](../../supply-chain/warehousing/catch-weight-processing.md).</span></span>

## <a name="non-gst-transactions-for-india"></a><span data-ttu-id="a5136-116">インド向けの非販売税トランザクション</span><span class="sxs-lookup"><span data-stu-id="a5136-116">Non-GST transactions for India</span></span> 
<span data-ttu-id="a5136-117">この機能を使用すると、税エンジンを使用して非販売税トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a5136-117">This feature allows you to create non-GST transactions with the Tax engine.</span></span> <span data-ttu-id="a5136-118">非販売税トランザクションを作成するには、それぞれの課税対象トランザクション行の **税情報** で **非販売税** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5136-118">To create a non-GST transaction, select the **Non-GST** check box in the **Tax information** of each taxable transaction line.</span></span> <span data-ttu-id="a5136-119">また、**参照番号順序グループ** に **供給の請求** の **番号順序コード** があることも確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5136-119">You also need to make sure that there is a **Number sequence code** for **Bill of supply** in the **Reference number sequence group**.</span></span> <span data-ttu-id="a5136-120">これらのトランザクションは、販売税還付 (GSTR) で非販売税トランザクションとして識別されます。</span><span class="sxs-lookup"><span data-stu-id="a5136-120">These transactions will be identified as non-GST transactions in the GST return (GSTR).</span></span> 

## <a name="regulatory-updates"></a><span data-ttu-id="a5136-121">規制の更新</span><span class="sxs-lookup"><span data-stu-id="a5136-121">Regulatory updates</span></span>
<span data-ttu-id="a5136-122">Finance and Operations の規制の更新については、[ローカライズおよび規制機能 – 規制の更新](../../financials/localizations/regulatory-updates.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-122">For information about the regulatory updates for Finance and Operations, see [Localization and Regulatory features – Regulatory updates](../../financials/localizations/regulatory-updates.md).</span></span> <span data-ttu-id="a5136-123">また、Lifecycle Services (LCS) にログインし、国、機能のタイプ、およびリリースを検索できる問題検索ツールを使用して、計画された規制の更新を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a5136-123">Alternatively, you can sign in to Lifecycle Services (LCS) and view the planned regulatory updates using the issue search tool, where you can search by country, type of feature, and release.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a5136-124">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a5136-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a5136-125">バグ修正</span><span class="sxs-lookup"><span data-stu-id="a5136-125">Bug fixes</span></span>
<span data-ttu-id="a5136-126">Finance and Operations 10.0 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 資料](https://go.microsoft.com/fwlink/?linkid=2080156)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-126">For information about the bug fixes included in each of the updates that are part of Finance and Operations version 10.0, sign in to Lifecycle Services (LCS) and view the [KB article](https://go.microsoft.com/fwlink/?linkid=2080156).</span></span>

### <a name="platform-update-24"></a><span data-ttu-id="a5136-127">プラットフォーム update 24</span><span class="sxs-lookup"><span data-stu-id="a5136-127">Platform update 24</span></span>
<span data-ttu-id="a5136-128">Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 には、プラットフォーム更新プログラム 24 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="a5136-128">Microsoft Dynamics 365 for Finance and Operations version 10.0 includes Platform update 24.</span></span> <span data-ttu-id="a5136-129">プラットフォーム更新プロフラム 24 については [Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](whats-new-platform-update-24.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a5136-129">To learn more about Platform update 24, see [What's new and changed in Finance and Operations platform update 24 (March 2019)](whats-new-platform-update-24.md).</span></span>

### <a name="dynamics-365-april-19-release-notes"></a><span data-ttu-id="a5136-130">Dynamics 365 2019 年 4 月 リリース ノート</span><span class="sxs-lookup"><span data-stu-id="a5136-130">Dynamics 365 April '19 release notes</span></span>
<span data-ttu-id="a5136-131">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="a5136-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="a5136-132">[2019 年 4 月リリース ノートをご覧ください](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index)。</span><span class="sxs-lookup"><span data-stu-id="a5136-132">[Check out the April '19 release notes](https://docs.microsoft.com/en-us/business-applications-release-notes/April19/index).</span></span> <span data-ttu-id="a5136-133">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="a5136-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="a5136-134">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="a5136-134">Removed and deprecated features</span></span>
<span data-ttu-id="a5136-135">[削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="a5136-135">The [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="a5136-136">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="a5136-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="a5136-137">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a5136-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="a5136-138">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="a5136-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>
