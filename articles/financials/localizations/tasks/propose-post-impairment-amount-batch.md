---
title: バッチごとの減損損失の提案と転記
description: このタスクは、バッチによる減損損失額の提案と転記について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3a2b6fb1f21d8011592f2c376437d81fe0f2e8e
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852618"
---
# <a name="propose-and-post-the-impairment-amount-by-batch"></a><span data-ttu-id="5603c-103">バッチごとの減損損失の提案と転記</span><span class="sxs-lookup"><span data-stu-id="5603c-103">Propose and post the impairment amount by batch</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5603c-104">このタスクは、バッチによる減損損失額の提案と転記について説明します。</span><span class="sxs-lookup"><span data-stu-id="5603c-104">This task walks you through proposing and posting the impairment amount by batch.</span></span> <span data-ttu-id="5603c-105">このタスクを完了するには、減損テストが確認され、保存されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5603c-105">Before you can complete this task, you must have an impairment test confirmed and saved.</span></span> <span data-ttu-id="5603c-106">この手順では、JPMF デモ会社のデータを使用します。</span><span class="sxs-lookup"><span data-stu-id="5603c-106">This task uses the JPMF demo company data.</span></span>

1. <span data-ttu-id="5603c-107">[固定資産] > [定期処理のタスク] > [減損提案] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5603c-107">Go to Fixed assets > Periodic tasks > Impairment proposal.</span></span>
2. <span data-ttu-id="5603c-108">[仕訳帳名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5603c-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="5603c-109">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5603c-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5603c-110">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5603c-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5603c-111">[減損テスト ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5603c-111">In the Impairment test ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="5603c-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5603c-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="5603c-113">[バックグラウンドで実行] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5603c-113">Expand the Run in the background section.</span></span>
8. <span data-ttu-id="5603c-114">[バッチ処理] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="5603c-114">Select Yes in the Batch processing field.</span></span>
9. <span data-ttu-id="5603c-115">[仕訳帳の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5603c-115">Click Create journal.</span></span>
10. <span data-ttu-id="5603c-116">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5603c-116">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
    * <span data-ttu-id="5603c-117">バッチは非同期的に処理されます。</span><span class="sxs-lookup"><span data-stu-id="5603c-117">The batch is processed asynchronously.</span></span> <span data-ttu-id="5603c-118">仕訳帳はまだ作成されていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5603c-118">The journal may not be created yet.</span></span>  
11. <span data-ttu-id="5603c-119">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="5603c-119">Refresh the page.</span></span>
    * <span data-ttu-id="5603c-120">ページを更新して、最新の情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5603c-120">You can refresh the page to see the latest information.</span></span> <span data-ttu-id="5603c-121">バッチがいつ処理されるかによっては、複数回更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5603c-121">You may need to refresh multiple times depending on when the batch is processed.</span></span>  
12. <span data-ttu-id="5603c-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5603c-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5603c-123">バッチがいつ処理されたかによっては、複数回ページを更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5603c-123">You may need to refresh the page multiple times depending on when the batch is been processed.</span></span>  
13. <span data-ttu-id="5603c-124">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5603c-124">Click Lines.</span></span>
    * <span data-ttu-id="5603c-125">固定資産が正しく作成され、減損損失額が正しいことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5603c-125">Confirm that the correct fixed assets were created and that they have the correct impairment amount.</span></span>  
14. <span data-ttu-id="5603c-126">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5603c-126">Click Post.</span></span>

