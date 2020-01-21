---
title: Dynamics 365 Finance バージョン 10.0.8 (2020 年 1 月) のプレビュー機能
description: このトピックでは、Dynamics 365 Finance バージョン 10.0.8 の新機能または変更された機能について説明します。
author: roschlom
manager: AnnBe
ms.date: 11/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 20a1a337c92d8f270ee95d0c076ce07fe5696a47
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945871"
---
# <a name="preview-features-in-dynamics-365-finance-version-1008-january-2020"></a><span data-ttu-id="8daaa-103">Dynamics 365 Finance バージョン 10.0.8 (2020 年 1 月) のプレビュー機能</span><span class="sxs-lookup"><span data-stu-id="8daaa-103">Preview features in Dynamics 365 Finance version 10.0.8 (January 2020)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8daaa-104">このトピックでは、Microsoft Dynamics 365 Finance バージョン 10.0.8 用 Finance and Operations 向けプラットフォーム更新プログラム 32 の新機能または変更されたプレビュー機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8daaa-104">This topic describes preview features that are new or changed for Platform update 32 for Microsoft Dynamics 365 Finance, version 10.0.8.</span></span> <span data-ttu-id="8daaa-105">このバージョンのビルド番号は 8.0.xxxx で、次のように使用できます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-105">This version has a build number of 8.0.xxxx and is available as follows:</span></span>

- <span data-ttu-id="8daaa-106">2019 年 11 月プレビュー リリース。</span><span class="sxs-lookup"><span data-stu-id="8daaa-106">Preview release is in November 2019.</span></span>
- <span data-ttu-id="8daaa-107">2020 年 1 月の一般提供 (自己更新)。</span><span class="sxs-lookup"><span data-stu-id="8daaa-107">General availability (self-update) is in January 2020.</span></span>
- <span data-ttu-id="8daaa-108">2020 年 2 月の自動更新が進行中です。</span><span class="sxs-lookup"><span data-stu-id="8daaa-108">Auto-update is in February 2020.</span></span>

<span data-ttu-id="8daaa-109">プラットフォーム更新プログラム 32 の詳細については [追加リソース](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md#additional-resources) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8daaa-109">For more information about Platform update 32, see [Additional resources](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-32.md#additional-resources).</span></span>

## <a name="feature-name"></a><span data-ttu-id="8daaa-110">機能名</span><span class="sxs-lookup"><span data-stu-id="8daaa-110">Feature name</span></span>

<span data-ttu-id="8daaa-111">説明</span><span class="sxs-lookup"><span data-stu-id="8daaa-111">Description</span></span> 

## <a name="expense-receipt-processing"></a><span data-ttu-id="8daaa-112">経費の領収書</span><span class="sxs-lookup"><span data-stu-id="8daaa-112">Expense receipt processing</span></span>

[!NOTE]
> - <span data-ttu-id="8daaa-113">この機能では現在、英語の領収書のみがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8daaa-113">This feature currently only supports the English language receipts.</span></span>
> - <span data-ttu-id="8daaa-114">この機能は現在、米国のみでサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8daaa-114">This feature is currently only supported in the United States.</span></span>
> - <span data-ttu-id="8daaa-115">この機能では、ユーザー データを学習の構築に使用することはありません。</span><span class="sxs-lookup"><span data-stu-id="8daaa-115">This feature does not use your data to build the learning.</span></span> <span data-ttu-id="8daaa-116">アップロードした領収書に基づかない、領収書処理用の一般的な機械学習モデルを構築してきました。</span><span class="sxs-lookup"><span data-stu-id="8daaa-116">We have built a general machine learning model for receipt processing that is not based on the receipts you upload.</span></span>
> - <span data-ttu-id="8daaa-117">Dynamics 365 Finance では、フィールド データを抽出するために Cognitive Services に手を差し伸べ、Cognitive Services は処理が完了するまで最大 24 時間、領収書のコピーが保持されます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-117">Dynamics 365 Finance will reach out to our Cognitive Services in order to extract the field data, the cognitive services will retain a copy of your receipt for up to 24 hours while processing completes.</span></span> <span data-ttu-id="8daaa-118">完了した Cognitive Services で、領収書が削除されます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-118">Once completed Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8daaa-119">領収書は、Dynamics 365 Finance に格納されます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-119">Receipts are stored within Dynamics 365 Finance.</span></span> <span data-ttu-id="8daaa-120">参照 [Form Recognizer の新機能を使用して領収書を理解する](https://azure.microsoft.com/en-us/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)</span><span class="sxs-lookup"><span data-stu-id="8daaa-120">Reference [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/en-us/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)</span></span>

<span data-ttu-id="8daaa-121">経費レポートの作成時にエンド ユーザー エクスペリエンスを向上させるために設計された、 領収書 OCR 処理の導入により経費入力が強化されました。</span><span class="sxs-lookup"><span data-stu-id="8daaa-121">Expense entry has been enhanced through the introduction of Receipt OCR processing, designed to improve the end user experience when creating expense reports.</span></span>

<span data-ttu-id="8daaa-122">主要な機能:</span><span class="sxs-lookup"><span data-stu-id="8daaa-122">Key features:</span></span>
- <span data-ttu-id="8daaa-123">領収書からマーチャント名、日付、合計金額を抽出する</span><span class="sxs-lookup"><span data-stu-id="8daaa-123">Extracts Merchant name, Date and Total amount from a receipt</span></span>
- <span data-ttu-id="8daaa-124">領収書を経費トランザクションに一致させるように試行する</span><span class="sxs-lookup"><span data-stu-id="8daaa-124">Attempts to match the receipt to an expense transaction</span></span>

<span data-ttu-id="8daaa-125">この機能は、**経費レポート再想像**機能を使用してサポートされています。</span><span class="sxs-lookup"><span data-stu-id="8daaa-125">This feature is supported using the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="8daaa-126">この機能を有効にするには、**機能管理** ワークスペースを使用して、**経費レポートを再想像**し、**自動照合を有効にして、領収書機能から経費を作成します**。</span><span class="sxs-lookup"><span data-stu-id="8daaa-126">To turn on this feature, use the **Feature management** workspace and enable **Expense reports re-imagined** and **Auto-match and create expense from receipt** features.</span></span>

<span data-ttu-id="8daaa-127">詳細については、[経費精算書の再設計](ExpenseWorkspaceNew.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8daaa-127">For more information, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>



## <a name="additional-resources"></a><span data-ttu-id="8daaa-128">追加リソース</span><span class="sxs-lookup"><span data-stu-id="8daaa-128">Additional resources</span></span>

### <a name="platform-update-xx"></a><span data-ttu-id="8daaa-129">プラットフォーム更新プログラム xx</span><span class="sxs-lookup"><span data-stu-id="8daaa-129">Platform update xx</span></span>

<span data-ttu-id="8daaa-130">Microsoft Dynamics 365 Supply Chain Management 10.0.8 には、プラットフォーム更新プログラム 32 が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8daaa-130">Microsoft Dynamics 365 Supply Chain Management 10.0.8 includes Platform update 32.</span></span> <span data-ttu-id="8daaa-131">プラットフォーム更新プログラム xx の詳細については、[プラットフォーム更新プログラム 32 のプレビュー機能](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-xx.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8daaa-131">To learn more about Platform update xx, see [Preview features in Platform update 32](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-xx.md).</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="8daaa-132">バグ修正</span><span class="sxs-lookup"><span data-stu-id="8daaa-132">Bug fixes</span></span> 
<span data-ttu-id="8daaa-133">10.0.7 の一部である更新プログラムのそれぞれに含まれるバグ修正については、Lifecycle Services (LCS) にログインし、[KB 記事](https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8daaa-133">For information about the bug fixes included in each of the updates that are part of 10.0.7, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=386529&dbType=3&qc=e03ced97fa18dc4439f36de17b00da7257dc15869a72e5b2435fec0acec0c493).</span></span>


### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="8daaa-134">Dynamics 365: 2019 リリースのウェーブ 2 プラン</span><span class="sxs-lookup"><span data-stu-id="8daaa-134">Dynamics 365: 2019 release wave 2 plan</span></span>

<span data-ttu-id="8daaa-135">当社のビジネス アプリやプラットフォームの次回および最近リリースされた機能について検討中ですか?</span><span class="sxs-lookup"><span data-stu-id="8daaa-135">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="8daaa-136">[Dynamics 365: 2019 リリース ウェーブ 2 プラン](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index) をご確認ください。</span><span class="sxs-lookup"><span data-stu-id="8daaa-136">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/en-us/dynamics365-release-plan/2019wave2/index).</span></span> <span data-ttu-id="8daaa-137">あらゆる詳細情報を端から端まで徹底的に捕捉して一元化しました。計画を策定する際に 1 つのドキュメントでそれらの情報を参照できます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-137">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-features"></a><span data-ttu-id="8daaa-138">削除済みおよび非推奨の機能</span><span class="sxs-lookup"><span data-stu-id="8daaa-138">Removed and deprecated features</span></span>

<span data-ttu-id="8daaa-139">[削除済みまたは非推奨の機能](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) のトピックは Dynamics 365 for Finance and Operations の削除済みまたは非推奨の機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="8daaa-139">The [Removed or deprecated features](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md) topic describes features that have been removed or deprecated for Dynamics 365 for Finance and Operations.</span></span>

- <span data-ttu-id="8daaa-140">*削除された*機能は製品では使用できません。</span><span class="sxs-lookup"><span data-stu-id="8daaa-140">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="8daaa-141">*削除予定*の機能は現在開発中ではなく、将来の更新で削除される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8daaa-141">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="8daaa-142">製品から機能が削除される前に、非推奨の通知が削除の 12 ヶ月前に [削除済みまたは非推奨の機能](../../dev-itpro/migration-upgrade/deprecated-features.md) のトピックに発表されます。</span><span class="sxs-lookup"><span data-stu-id="8daaa-142">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features](../../dev-itpro/migration-upgrade/deprecated-features.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="8daaa-143">コンパイル時に影響する重大な変更が、サンドボックス環境および実稼働環境と互換性のあるバイナリの場合、廃止時間は 12 か月以内になります。</span><span class="sxs-lookup"><span data-stu-id="8daaa-143">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="8daaa-144">通常、これらはコンパイラに加える必要がある機能の更新です。</span><span class="sxs-lookup"><span data-stu-id="8daaa-144">Typically, these are functional updates that need to be made to the compiler.</span></span>
