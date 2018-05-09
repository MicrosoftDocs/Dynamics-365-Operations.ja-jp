--- 
title: "誰かの代わりに製品を注文するためのアクセス許可の設定"
description: "この手順では、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を示します。"
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 30d91d2ffab74250b3a8a46d7b7c5441a94d8dfd
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="2e6b5-103">誰かの代わりに製品を注文するためのアクセス許可の設定</span><span class="sxs-lookup"><span data-stu-id="2e6b5-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2e6b5-104">この手順では、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="2e6b5-105">つまり、購買要求「作成者」が他の「要求者」の要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="2e6b5-106">この手順では、違う法人または作業単位で品目とサービスを注文する作業者のアクセス許可を付与する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="2e6b5-107">通常、これらのタスクは、購買マネージャーが実行します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="2e6b5-108">USMF デモ会社または独自のデータでこの手順を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="2e6b5-109">別の作業者の代わりに購買要求を入力するアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="2e6b5-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="2e6b5-110">[調達] > [設定] > [ポリシー] > [購買要求アクセス許可] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="2e6b5-111">[現在のビュー] フィールドが作成者によって設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="2e6b5-112">左ウィンドウの一覧は、他のユーザーに代わって要求を作成する許可を付与されるユーザーを示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="2e6b5-113">アクセス許可を付与する個人を選択します (作成者)。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="2e6b5-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-114">Click Add.</span></span>
4. <span data-ttu-id="2e6b5-115">依頼者として追加する個人を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="2e6b5-116">依頼者は、作成者が代わりに要求を作成できる人物です。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="2e6b5-117">[認証] フィールドで、選択した作業者に代わって作成者が購買要求を作成できるよう [特定] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="2e6b5-118">作成者がその作業者に報告するすべての作業者に代わって購買要求を作成できるよう [レポート] を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="2e6b5-119">[有効開始] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="2e6b5-120">[有効期限] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="2e6b5-121">選択した作業者の購買要求を作成するためのアクセス許可を持つ作成者を表示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="2e6b5-122">[現在のビュー] フィールドで、「依頼者」を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="2e6b5-123">選択した作業者の代わりに購買要求を作成するアクセス許可を与える作成者の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="2e6b5-124">[クイック フィルター] を使用して、依頼者としてちょうど追加したばかりの作業者を検索します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="2e6b5-125">依頼者を選択します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-125">Select the requester.</span></span>
    * <span data-ttu-id="2e6b5-126">作成者の一覧は、左ウィンドウで選択された要求者に代わって品目を注文するアクセス許可があるユーザーを表示します。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="2e6b5-127">ここで追加の作成者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-127">You can add additional preparers here.</span></span>   <span data-ttu-id="2e6b5-128">このビューは、そのユーザーの主要な法人および作業単位ではない場合の、法人および作業単位内で依頼人のアクセス許可を付与することができます。</span><span class="sxs-lookup"><span data-stu-id="2e6b5-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


