---
title: 増加償却の提案と転記
description: 日本の場合、確認済加速償却ドキュメントのデータに基づいて加速償却を提案することができます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset, AssetAcceleratedDepDocument_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e57166ba614a44a7acd61c21a53a89966f6ff181
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988244"
---
# <a name="propose-and-post-accelerated-depreciation"></a><span data-ttu-id="5d18f-103">増加償却の提案と転記</span><span class="sxs-lookup"><span data-stu-id="5d18f-103">Propose and post accelerated depreciation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5d18f-104">日本の場合、確認済加速償却ドキュメントのデータに基づいて加速償却を提案することができます。</span><span class="sxs-lookup"><span data-stu-id="5d18f-104">For Japan, you can propose an accelerated depreciation based on the data on confirmed accelerated depreciation documents.</span></span> <span data-ttu-id="5d18f-105">注記: 加速償却の提案は通常の減価償却を提案しません。</span><span class="sxs-lookup"><span data-stu-id="5d18f-105">Note: The accelerated depreciation proposal will not propose ordinary depreciation.</span></span> <span data-ttu-id="5d18f-106">この手順では、通常の減価償却の転記後に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d18f-106">This procedure must be completed after you post ordinary depreciation.</span></span>



<span data-ttu-id="5d18f-107">この手順は確認済加速減価償却ドキュメントに基づく加速償却の提案および転記について説明します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-107">This procedure walks you through proposing and posting an accelerated depreciation document based on confirmed accelerated depreciation documents.</span></span> 



<span data-ttu-id="5d18f-108">この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d18f-108">In order to complete this procedure, the Fixed asset configuration key must be selected.</span></span>



<span data-ttu-id="5d18f-109">この手順は、デモ データ会社 JPMF を使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="5d18f-109">This procedure was created using the demo data company JPMF.</span></span>

1. <span data-ttu-id="5d18f-110">[固定資産] > [仕訳入力] > [固定資産仕訳帳] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-110">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="5d18f-111">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-111">Click New.</span></span>
3. <span data-ttu-id="5d18f-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5d18f-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-113">Click Save.</span></span>
5. <span data-ttu-id="5d18f-114">[明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-114">Click Lines.</span></span>
6. <span data-ttu-id="5d18f-115">[提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-115">Click Proposals.</span></span>
7. <span data-ttu-id="5d18f-116">[加速償却提案] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-116">Click Accelerated depreciation proposal.</span></span>
8. <span data-ttu-id="5d18f-117">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-117">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="5d18f-118">既定では、すべての確認済加速償却を提案するよう基準がコンフィギュレーションされています。</span><span class="sxs-lookup"><span data-stu-id="5d18f-118">By default, the criteria is configured to propose all confirmed accelerated depreciation documents.</span></span> <span data-ttu-id="5d18f-119">ある特定のドキュメントの提案など、その他のニーズがある場合は変更できます。</span><span class="sxs-lookup"><span data-stu-id="5d18f-119">You can change this if there is any other needs such as proposing for one specific document.</span></span>  
9. <span data-ttu-id="5d18f-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-120">Click OK.</span></span>
    * <span data-ttu-id="5d18f-121">加速償却が提案されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-121">Confirm that the accelerated depreciation was proposed.</span></span>  
    * <span data-ttu-id="5d18f-122">注記: 通常の減価償却は取り扱わないため、提案および転記にはユーザーによる操作が必要です。</span><span class="sxs-lookup"><span data-stu-id="5d18f-122">Note: The ordinary depreciation is not handled, and therefore, still needs user's operation to propose and post it.</span></span>  
10. <span data-ttu-id="5d18f-123">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5d18f-123">Click Post.</span></span>
11. <span data-ttu-id="5d18f-124">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5d18f-124">Close the page.</span></span>
12. <span data-ttu-id="5d18f-125">[固定資産] > [定期処理タスク] > [加速償却] > [加速償却ドキュメント] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-125">Go to Fixed assets > Periodic tasks > Accelerated depreciation > Accelerated depreciation document.</span></span>
    * <span data-ttu-id="5d18f-126">転記済ドキュメントのステータスが更新されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5d18f-126">Confirm that the status of posted document has been updated.</span></span>  

