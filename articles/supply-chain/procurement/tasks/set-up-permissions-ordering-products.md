---
title: 誰かの代わりに製品を注文するためのアクセス許可の設定
description: このトピックでは、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を説明します。
author: kamaybac
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0408085d401a34a409bfe46bc6845a9c81a2eea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811897"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="65762-103">誰かの代わりに製品を注文するためのアクセス許可の設定</span><span class="sxs-lookup"><span data-stu-id="65762-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65762-104">このトピックでは、他の作業者に代わって購買要求を作成するためのアクセス許可を作業者に付与する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="65762-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="65762-105">つまり、購買要求「作成者」が他の「要求者」の要求を作成できます。</span><span class="sxs-lookup"><span data-stu-id="65762-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="65762-106">この手順では、違う法人または作業単位で品目とサービスを注文する作業者のアクセス許可を付与する方法も示します。</span><span class="sxs-lookup"><span data-stu-id="65762-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="65762-107">通常、これらのタスクは、購買マネージャーが実行します。</span><span class="sxs-lookup"><span data-stu-id="65762-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="65762-108">USMF デモ会社または独自のデータでこの手順を使うことができます。</span><span class="sxs-lookup"><span data-stu-id="65762-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="65762-109">別の作業者の代わりに購買要求を入力するアクセス許可を付与します</span><span class="sxs-lookup"><span data-stu-id="65762-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="65762-110">ナビゲーション ウィンドウで、**モジュール > 調達 > 設定 > ポリシー > 購買要求アクセス許可** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="65762-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="65762-111">**現在のビュー** フィールドが **作成者** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="65762-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="65762-112">左ウィンドウの一覧は、他のユーザーに代わって要求を作成する許可を付与されるユーザーを示します。</span><span class="sxs-lookup"><span data-stu-id="65762-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="65762-113">アクセス許可を付与する個人を選択します (作成者)。</span><span class="sxs-lookup"><span data-stu-id="65762-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="65762-114">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-114">Select **Add**.</span></span>
4. <span data-ttu-id="65762-115">依頼者として追加する個人を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="65762-116">依頼者は、作成者が代わりに要求を作成できる人物です。</span><span class="sxs-lookup"><span data-stu-id="65762-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="65762-117">**認証** フィールドで、選択した作業者に代わって作成者が購買要求を作成できるよう **特定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="65762-118">作成者がその作業者に報告するすべての作業者に代わって購買要求を作成できるよう **レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="65762-119">**有効開始** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="65762-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="65762-120">**有効期限** フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="65762-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="65762-121">選択した作業者の購買要求を作成するためのアクセス許可を持つ作成者を表示します。</span><span class="sxs-lookup"><span data-stu-id="65762-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="65762-122">**現在のビュー** フィールドで、**依頼者** を選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="65762-123">選択した作業者の代わりに購買要求を作成するアクセス許可を与える作成者の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="65762-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="65762-124">[クイック フィルター] を使用して、依頼者としてちょうど追加したばかりの作業者を検索します。</span><span class="sxs-lookup"><span data-stu-id="65762-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="65762-125">依頼者を選択します。</span><span class="sxs-lookup"><span data-stu-id="65762-125">Select the requester.</span></span> <span data-ttu-id="65762-126">作成者の一覧は、左ウィンドウで選択された要求者に代わって品目を注文するアクセス許可があるユーザーを表示します。</span><span class="sxs-lookup"><span data-stu-id="65762-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="65762-127">ここで追加の作成者を追加できます。</span><span class="sxs-lookup"><span data-stu-id="65762-127">You can add additional preparers here.</span></span> <span data-ttu-id="65762-128">このビューは、そのユーザーの主要な法人および作業単位ではない場合の、法人および作業単位内で依頼人のアクセス許可を付与することができます。</span><span class="sxs-lookup"><span data-stu-id="65762-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]