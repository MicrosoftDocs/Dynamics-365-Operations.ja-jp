---
title: "オープン作業一覧のシステム グループ化"
description: "このトピックでは、モバイル デバイスでオープン作業一覧をフィルターする方法について説明します。"
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6403fea54be4036f7a15c05b46f70d258d97c3e2
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="08f58-103">オープン作業一覧のシステム グループ化</span><span class="sxs-lookup"><span data-stu-id="08f58-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="08f58-104">システム グルーピング フィールドを使用すると、モバイル デバイスのメニュー項目を編集することなく、オープン作業一覧をフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="08f58-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="08f58-105">適用される場合、単一の作業ヘッダー フィールドで作業リストをフィルタリングするためのシステム グループ化が機能します。</span><span class="sxs-lookup"><span data-stu-id="08f58-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="08f58-106">明細行レベルのフィールドをフィルターするためにシステム グループを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="08f58-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="08f58-107">オープン作業一覧のシステム グループ化を設定する</span><span class="sxs-lookup"><span data-stu-id="08f58-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="08f58-108">オープン作業一覧のシステム グループ化を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="08f58-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="08f58-109">モバイル デバイスのメニュー項目から、[**モード: 間接**] および [**活動コード: オープン作業一覧の表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="08f58-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="08f58-110">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="08f58-110">The following options become available.</span></span> <span data-ttu-id="08f58-111">これらのオプションは、オープン作業一覧にシステム グループ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08f58-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="08f58-112">オプション</span><span class="sxs-lookup"><span data-stu-id="08f58-112">Option</span></span>        | <span data-ttu-id="08f58-113">説明</span><span class="sxs-lookup"><span data-stu-id="08f58-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="08f58-114">システム グループ化の許可</span><span class="sxs-lookup"><span data-stu-id="08f58-114">Allow system grouping</span></span>   | <span data-ttu-id="08f58-115">選択された作業リスト メニュー品目のシステム グループ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="08f58-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="08f58-116">システム グループ化フィールド</span><span class="sxs-lookup"><span data-stu-id="08f58-116">System grouping field</span></span>   | <span data-ttu-id="08f58-117">[**システム作業の許可**] が [**はい**] に設定されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="08f58-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="08f58-118">ピッキング作業をどのように作業者にグループ化するかを決定するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="08f58-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="08f58-119">たとえば、**[ShipmentId]** フィールドを選択した場合、作業者はピッキング作業をグループ化する出荷 ID をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="08f58-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="08f58-120">出荷のすべての作業が作業者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="08f58-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="08f58-121">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="08f58-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="08f58-122">[**システム グループ化ラベル**] フィールドを使用して、作業者に何をスキャンするかを通知します。</span><span class="sxs-lookup"><span data-stu-id="08f58-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="08f58-123">システム グループ化ラベル</span><span class="sxs-lookup"><span data-stu-id="08f58-123">System grouping label</span></span>   | <span data-ttu-id="08f58-124">[**システム作業の許可**] が [**はい**] に設定されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="08f58-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="08f58-125">ピッキング作業がグループ化されたときに、何をスキャンするかを作業者に通知する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="08f58-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="08f58-126">たとえば、[**ShipmentId**] フィールドを使用して出荷別にピッキング作業をグループ化する場合、このフィールドに出荷 ID を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="08f58-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="08f58-127">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="08f58-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="08f58-128">また、[**システム グループ化**] フィールドでグループ化するフィールドを選択する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="08f58-128">You must also select the field to group by in the **System grouping** field.</span></span>|

