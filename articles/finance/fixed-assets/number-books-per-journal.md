---
title: 仕訳帳ごとの帳簿数
description: このトピックでは、バッチ ジョブを使用して固定資産の取得または償却提案を作成するときの仕訳帳と資産帳簿のリレーションシップについて説明します。 各取得および減価償却に含まれる帳簿の最大数を定義できます。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-19
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: fb2a25d9e2ffc26f0a37a09cdf3e28a7ca4b84bc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892410"
---
# <a name="number-of-books-per-journal"></a><span data-ttu-id="f3276-104">仕訳帳ごとの帳簿数</span><span class="sxs-lookup"><span data-stu-id="f3276-104">Number of books per journal</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3276-105">このトピックでは、バッチ ジョブを使用して固定資産の取得または償却提案を作成するときの仕訳帳と資産帳簿のリレーションシップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f3276-105">This topic describes the relationship between journals and asset books when you create a fixed asset acquisition or depreciation proposal through a batch job.</span></span> <span data-ttu-id="f3276-106">**固定資産パラメータ** ページ (**固定資産 \> 設定 \> 固定資産パラメータ**) の **一般** タブの **仕訳帳ごとの帳簿数** セクションのフィールドを使用して、各取得および減価償却に含まれる帳簿の最大数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="f3276-106">You can define the maximum number of books that are included for each acquisition and for depreciation by using the fields in the **Number of books per journal** section on the **General** tab of the **Fixed assets parameters** page (**Fixed assets \> Setup \> Fixed assets parameters**).</span></span> <span data-ttu-id="f3276-107">これらのフィールドを使用すると、取得仕訳帳と減価償却仕訳帳ごとに資産帳簿の数を配分できます。</span><span class="sxs-lookup"><span data-stu-id="f3276-107">These fields let you distribute the number of asset books per acquisition journal and depreciation journal.</span></span>

<span data-ttu-id="f3276-108">取得提案の場合、既定値は 10,000 帳簿以上です。</span><span class="sxs-lookup"><span data-stu-id="f3276-108">For an acquisition proposal, the default value is at least 10,000 books.</span></span> <span data-ttu-id="f3276-109">減価償却の場合、既定値は少なくとも 2,000 帳簿です。</span><span class="sxs-lookup"><span data-stu-id="f3276-109">For a depreciation proposal, the default value is at least 2,000 books.</span></span>

<span data-ttu-id="f3276-110">たとえば、4,000 の固定資産があり、各資産に 2 つの帳簿が関連付けられている場合は、1 帳簿が現レイヤーに転記され、もう 1 帳簿が税レイヤーに転記されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-110">For example, if there are 4,000 fixed assets, and two books are associated with each asset, one book will be posted to the current layer, and the other book will be posted to the tax layer.</span></span> <span data-ttu-id="f3276-111">バッチ処理によって 4,000 の固定資産を取得した場合、1 つの固定資産取得仕訳帳を作成するバッチジョブには、4,000 の資産帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3276-111">If you acquire 4,000 fixed assets through batch processing, the batch job that creates one fixed asset acquisition journal will contain 4,000 asset books.</span></span>

> [!NOTE]
> <span data-ttu-id="f3276-112">バッチジョブが完了するまでは、作成された仕訳帳が引き続き使用されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-112">The journal that is created will continue to be used until the batch job is completed.</span></span>
>
> <span data-ttu-id="f3276-113">派生した帳簿は、仕訳帳ごとの帳簿の最大数には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f3276-113">The derived books aren't included in the maximum number of books per journal.</span></span>

<span data-ttu-id="f3276-114">バッチ処理を使用すると、取得した同じ資産のセットに対して減価償却を実行できます。</span><span class="sxs-lookup"><span data-stu-id="f3276-114">You can use  batch processing to run depreciation for the same set of acquired assets.</span></span> <span data-ttu-id="f3276-115">たとえば、バッチジョブでは 2 つの減価償却仕訳帳が作成されます。各減価償却は、2,000 帳簿から構成されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-115">For example, a batch job creates two depreciation journals, each of which consists of 2,000 asset books.</span></span> <span data-ttu-id="f3276-116">最初の仕訳帳には、1 から 2,000 の番号が付いた固定資産に関連付けられている帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3276-116">The first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,000.</span></span> <span data-ttu-id="f3276-117">2 番目の仕訳帳には、2,001 から 4,000 の番号が付いた固定資産に関連付けられている帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3276-117">The second journal will then contain books that are associated with the fixed assets that are numbered 2,001 through 4,000.</span></span>

<span data-ttu-id="f3276-118">バッチ処理ジョブでは、クローズされた帳簿は除外されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-118">The batch processing job excludes closed books.</span></span> <span data-ttu-id="f3276-119">たとえば、減価償却のバッチジョブでは、最初の 2,000 帳簿のうちの 10 がクローズしています。</span><span class="sxs-lookup"><span data-stu-id="f3276-119">For example, in a batch job for depreciation, 10 of the first 2,000 books are closed.</span></span> <span data-ttu-id="f3276-120">この場合、最初の仕訳帳には、1 から 2,011 の番号が付いた固定資産に関連付けられている帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3276-120">In this case, the first journal will contain books that are associated with the fixed assets that are numbered 1 through 2,011.</span></span> <span data-ttu-id="f3276-121">2 番目の仕訳帳には、2,012 から 4,000 の番号が付いた固定資産に関連付けられている帳簿が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f3276-121">The second journal will then contain books that are associated with the fixed assets that are numbered 2,012 through 4,000.</span></span>

> [!NOTE]
> <span data-ttu-id="f3276-122">区切り記号 (-や/など) が異なる固定資産の ID があり、バッチ ジョブで固定資産トランザクションを作成する場合は、区切り記号のタイプごとに個別のバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f3276-122">If you have fixed asset IDs with different separators (such as – or /), and you create fixed asset transactions in batch jobs, you must run a separate batch job for each type of separator.</span></span> <span data-ttu-id="f3276-123">同じバッチ ジョブ内で異なる区切り記号は処理できません。</span><span class="sxs-lookup"><span data-stu-id="f3276-123">The system can't process different separators within the same batch job.</span></span>

<span data-ttu-id="f3276-124">帳簿数の制限は、重複する資産 ID が同じ仕訳帳に存在しない場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-124">The limit on the number of books is applied if duplicate asset IDs don't exist in the same journal.</span></span> <span data-ttu-id="f3276-125">ただし、資産 ID が帳簿 ID と同じである場合は、仕訳帳ごとの帳簿の数を制限して、資産 ID を同じ仕訳帳に保持することができます。</span><span class="sxs-lookup"><span data-stu-id="f3276-125">However, if the asset ID is the same as the book ID, the number of books per journal can be exceeded to keep the asset ID in the same journal.</span></span>

<span data-ttu-id="f3276-126">たとえば、5,001 の固定資産 ID がある場合は、各固定資産 ID に 3 つの帳簿が関連付けられ、各資産帳簿が同じ転記階層に転記されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-126">For example, there are 5,001 fixed asset IDs, three books are associated with each fixed asset ID, and each asset book is posted to the same posting layer.</span></span> <span data-ttu-id="f3276-127">集計を行わずに 3 つの連続する月に対して減価償却を実行します。</span><span class="sxs-lookup"><span data-stu-id="f3276-127">You run depreciation for three consecutive months, without summarizing.</span></span>  <span data-ttu-id="f3276-128">バッチジョブによって減価償却仕訳帳が作成され、システムは 667 の固定資産 ID と各固定資産 ID に対して  3 つの帳簿がある 7 つの仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="f3276-128">The depreciation journal will be created through a batch job, and the system will create seven journals that have 667 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="f3276-129">この結果、2,001 帳簿になります。</span><span class="sxs-lookup"><span data-stu-id="f3276-129">The result will be 2,001 books.</span></span> <span data-ttu-id="f3276-130">したがって、3 か月で、同じ仕訳帳に同じ資産 ID を保持するための 6,003 の仕訳帳明細行が存在することになります。</span><span class="sxs-lookup"><span data-stu-id="f3276-130">Therefore, in three months, there will be 6,003 journal lines to maintain the same asset IDs in the same journal.</span></span> <span data-ttu-id="f3276-131">また、各固定資産 ID に対して 332 の固定資産 ID と 3 つの帳簿を持つ仕訳帳が 1 つ作成されます。</span><span class="sxs-lookup"><span data-stu-id="f3276-131">The system will also create one journal that has 332 fixed asset IDs and three books for each fixed asset ID.</span></span> <span data-ttu-id="f3276-132">3 か月で、明細行が 2,988 行になります。</span><span class="sxs-lookup"><span data-stu-id="f3276-132">In three months, there will be 2,988 lines.</span></span>

> [!NOTE] 
> <span data-ttu-id="f3276-133">償却提案の作成時に **減価償却の集計** パラメータが有効になっている場合は、**仕訳帳あたりの帳簿数 - 償却提案** フィールドの値は無効になります。</span><span class="sxs-lookup"><span data-stu-id="f3276-133">If the **Summarize depreciation** parameter is turned on when you're creating a depreciation proposal, then the value in the **Number of books per journal - Depreciation proposal** field has no effect.</span></span> <span data-ttu-id="f3276-134">この場合、仕訳帳ごとの帳簿数は 6000 となり、内部定義の上限に達しています。</span><span class="sxs-lookup"><span data-stu-id="f3276-134">In this case number of books per journal is 6000, which is the internal defined limit.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
