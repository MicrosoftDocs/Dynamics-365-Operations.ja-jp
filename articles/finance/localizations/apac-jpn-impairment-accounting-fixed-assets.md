---
title: 日本の固定資産の減損会計
description: このトピックでは、日本の固定資産の減損会計に関する情報について説明します。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentAssetTransInquire_JP, AssetImpairmentIndicator_JP, AssetImpairmentManageTestResult_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 28811
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e730804b2b31cbdadeeb05a0e48e2daa2b8a92f8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183755"
---
# <a name="impairment-accounting-for-fixed-assets-for-japan"></a><span data-ttu-id="5428b-103">日本の固定資産の減損会計</span><span class="sxs-lookup"><span data-stu-id="5428b-103">Impairment accounting for fixed assets for Japan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5428b-104">このトピックでは、日本の固定資産の減損会計に関する情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="5428b-104">This topic includes information about impairment accounting for fixed assets in Japan.</span></span>

<span data-ttu-id="5428b-105">固定資産の減損を設定および計算するには、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-105">You can perform the following tasks to set up and calculate fixed asset impairments:</span></span>

-   <span data-ttu-id="5428b-106">減損された可能性のある固定資産の一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="5428b-106">Generate a list of fixed assets that might be impaired.</span></span> <span data-ttu-id="5428b-107">一覧の各資産の値引き前キャッシュ フロー、公正価額、復旧可能な金額を手動で確認し、計算して、固定資産が減損されるかどうかを決定できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-107">You can then manually review and calculate the undiscounted cash flow, fair value, or recoverable amounts of each asset in the list to determine whether the fixed assets are impaired.</span></span>
-   <span data-ttu-id="5428b-108">固定資産の値引き前キャッシュ フローなど減損のインジケーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="5428b-108">Update impairment indicators, such as the undiscounted cash flow of the fixed assets.</span></span>
-   <span data-ttu-id="5428b-109">減損のインジケーターを使用して減損の認識テストを実行し、減損された固定資産の一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="5428b-109">Run the impairment recognition test by using the impairment indicators to generate a list of impaired fixed assets.</span></span>
-   <span data-ttu-id="5428b-110">固定資産が減損される程度を示す回収可能金額を指定し、減損された固定資産の仕訳帳トランザクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-110">Specify recoverable values that indicate the extent to which the fixed assets are impaired, and then create journal transactions for these impaired fixed assets.</span></span> <span data-ttu-id="5428b-111">仕訳帳を転記する前に、減損に関する詳細を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-111">You can specify the details about the impairment before you post the journal.</span></span>
-   <span data-ttu-id="5428b-112">固定資産の減損のトランザクションの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="5428b-112">View the details of the impairment transactions for fixed assets.</span></span>

## <a name="how-can-i-identify-impairments-in-fixed-assets"></a><span data-ttu-id="5428b-113">固定資産の減損をどのように識別できますか。</span><span class="sxs-lookup"><span data-stu-id="5428b-113">How can I identify impairments in fixed assets?</span></span>
<span data-ttu-id="5428b-114">固定資産の減損を識別するために減損のインジケーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-114">You can use impairment indicators to identify impairment in fixed assets.</span></span><span data-ttu-id="5428b-115"> **減損の確認**ページで、減損しているとみられる固定資産の一覧を生成できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-115"> On the **Impairment review** page, you can generate a list of fixed assets that might be impaired.</span></span> <span data-ttu-id="5428b-116">値引き前キャッシュ フローを手動で計算し、**減損インジケーターの更新**ページで固定資産の減損インジケーターを更新します。</span><span class="sxs-lookup"><span data-stu-id="5428b-116">You can then manually calculate the undiscounted cash flow and update impairment indicators for the fixed assets on the **Update impairment indicators** page.</span></span> <span data-ttu-id="5428b-117">減損の認識テストの実行時に、固定資産の減損を識別するには、更新した減損インジケーターを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-117">When you run the impairment recognition test, you can use the impairment indicators that you updated to identify impairments in fixed assets.</span></span>

## <a name="can-i-select-which-assets-to-test-for-impairment"></a><span data-ttu-id="5428b-118">減損をテストする資産を選択できますか。</span><span class="sxs-lookup"><span data-stu-id="5428b-118">Can I select which assets to test for impairment?</span></span>
<span data-ttu-id="5428b-119">減損をテストする資産を選択できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-119">Yes, you can select which assets to test for impairment.</span></span> <span data-ttu-id="5428b-120">基準を指定するには、**減損認識のテスト**ページの**クエリ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5428b-120">To specify the criteria, click **Query** on the **Impairment recognition test** page.</span></span>

## <a name="how-often-can-i-check-fixed-assets-for-impairment"></a><span data-ttu-id="5428b-121">減損について固定資産をどれほどの頻度で確認できますか。</span><span class="sxs-lookup"><span data-stu-id="5428b-121">How often can I check fixed assets for impairment?</span></span>
<span data-ttu-id="5428b-122">バッチ ジョブを作成して、スケジュールに基づいて減損について固定資産を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-122">By creating a batch job, you can check the fixed assets for impairment according to a schedule.</span></span>

## <a name="are-there-types-of-fixed-assets-that-are-excluded-from-impairment-testing-and-accounting"></a><span data-ttu-id="5428b-123">減損のテストおよび会計から除外された固定資産のタイプがありますか。</span><span class="sxs-lookup"><span data-stu-id="5428b-123">Are there types of fixed assets that are excluded from impairment testing and accounting?</span></span>
<span data-ttu-id="5428b-124">固定資産の次のタイプは、減損のテストおよび会計から除外されます。</span><span class="sxs-lookup"><span data-stu-id="5428b-124">Yes, the following types of fixed assets are excluded from impairment testing and accounting:</span></span>

-   <span data-ttu-id="5428b-125">リースした固定資産</span><span class="sxs-lookup"><span data-stu-id="5428b-125">Leased fixed assets</span></span>
-   <span data-ttu-id="5428b-126">共有資産</span><span class="sxs-lookup"><span data-stu-id="5428b-126">Shared assets</span></span>
-   <span data-ttu-id="5428b-127">無形固定資産の固定資産</span><span class="sxs-lookup"><span data-stu-id="5428b-127">Goodwill fixed asset</span></span>

<span data-ttu-id="5428b-128">営業権と共有資産を計算するために資産グループの減損を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5428b-128">You must use the impairment for cash generating units to account for goodwill and shared assets.</span></span>

## <a name="can-i-generate-reports-that-i-can-use-to-review-impaired-assets-and-impairment-amounts"></a><span data-ttu-id="5428b-129">減損された資産と減損金額を確認するために使用するレポートを生成できますか。</span><span class="sxs-lookup"><span data-stu-id="5428b-129">Can I generate reports that I can use to review impaired assets and impairment amounts?</span></span>
<span data-ttu-id="5428b-130">減損された資産と減損の会計に関する情報を含む次のレポートを生成できます。</span><span class="sxs-lookup"><span data-stu-id="5428b-130">Yes, you can generate the following reports that contain information about impaired assets and impairment accounting:</span></span>

-   <span data-ttu-id="5428b-131">固定資産トランザクション レポート</span><span class="sxs-lookup"><span data-stu-id="5428b-131">Fixed asset transactions report</span></span>
-   <span data-ttu-id="5428b-132">固定資産減損トランザクション レポート</span><span class="sxs-lookup"><span data-stu-id="5428b-132">Fixed asset impairment transactions report</span></span>
-   <span data-ttu-id="5428b-133">減損損失レポートのための固定資産の確認</span><span class="sxs-lookup"><span data-stu-id="5428b-133">Review fixed assets for impairment report</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5428b-134">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5428b-134">Additional resources</span></span>
- [<span data-ttu-id="5428b-135">キャッシュ生成単位の固定資産の減損会計</span><span class="sxs-lookup"><span data-stu-id="5428b-135">Fixed asset impairment accounting on cash generating units</span></span>](apac-jpn-impairment-accounting-cash-generating-unit.md)
- [<span data-ttu-id="5428b-136">個別資産の減損インジケーターの管理</span><span class="sxs-lookup"><span data-stu-id="5428b-136">Maintain impairment indicators on individual assets</span></span>](./tasks/maintain-impairment-indicators-individual-assets.md)
- [<span data-ttu-id="5428b-137">バッチごとの減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="5428b-137">Propose and post the impairment amount by batch</span></span>](./tasks/propose-post-impairment-amount-batch.md)
- [<span data-ttu-id="5428b-138">固定資産仕訳帳を使用した減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="5428b-138">Propose and post the impairment amount by using fixed asset journal</span></span>](./tasks/propose-post-impairment-amount-fixed-asset-journal.md)
- [<span data-ttu-id="5428b-139">認識テストの実行と個別資産の減損損失の計算</span><span class="sxs-lookup"><span data-stu-id="5428b-139">Run the recognition test and calculate the impairment amount on individual assets</span></span>](./tasks/run-recognition-test-calculate.md)
- [<span data-ttu-id="5428b-140">減損会計の共通パラメーターおよび転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="5428b-140">Set up impairment accounting common parameters and posting profile</span></span>](./tasks/impairment-accounting.md)


