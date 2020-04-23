---
title: オープン作業一覧のシステム グループ化
description: このトピックでは、モバイル デバイスでオープン作業一覧をフィルターする方法について説明します。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05b697cce8ecb9ece282fc659ab4d97c4b747c5e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217221"
---
# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="b9856-103">オープン作業一覧のシステム グループ化</span><span class="sxs-lookup"><span data-stu-id="b9856-103">System grouping on an open work list</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9856-104">システム グルーピング フィールドを使用すると、モバイル デバイスのメニュー項目を編集することなく、オープン作業一覧をフィルターできます。</span><span class="sxs-lookup"><span data-stu-id="b9856-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="b9856-105">適用される場合、単一の作業ヘッダー フィールドで作業リストをフィルタリングするためのシステム グループ化が機能します。</span><span class="sxs-lookup"><span data-stu-id="b9856-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="b9856-106">明細行レベルのフィールドをフィルターするためにシステム グループを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="b9856-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="b9856-107">オープン作業一覧のシステム グループ化を設定する</span><span class="sxs-lookup"><span data-stu-id="b9856-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="b9856-108">オープン作業一覧のシステム グループ化を設定するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="b9856-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="b9856-109">モバイル デバイスのメニュー項目から、**モード: 間接** および **活動コード: オープン作業一覧の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b9856-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="b9856-110">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9856-110">The following options become available.</span></span> <span data-ttu-id="b9856-111">これらのオプションは、オープン作業一覧にシステム グループ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9856-111">These options are required for system grouping on an open work list.</span></span> 

|        <span data-ttu-id="b9856-112">オプション</span><span class="sxs-lookup"><span data-stu-id="b9856-112">Option</span></span>         |                                                                                                                                                                                                                                                                         <span data-ttu-id="b9856-113">説明</span><span class="sxs-lookup"><span data-stu-id="b9856-113">Description</span></span>                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9856-114">システム グループ化の許可</span><span class="sxs-lookup"><span data-stu-id="b9856-114">Allow system grouping</span></span> |                                                                                                                                                                                                                                                 <span data-ttu-id="b9856-115">選択された作業リスト メニュー品目のシステム グループ化を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b9856-115">Enables system groping for a selected work list menu item.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="b9856-116">システム グループ化フィールド</span><span class="sxs-lookup"><span data-stu-id="b9856-116">System grouping field</span></span> | <span data-ttu-id="b9856-117"><strong>システム作業の許可</strong> が <strong>はい</strong> に設定されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9856-117">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="b9856-118">ピッキング作業をどのように作業者にグループ化するかを決定するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b9856-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="b9856-119">たとえば、<strong>ShipmentId</strong> フィールドを選択した場合、作業者はピッキング作業をグループ化する出荷 ID をスキャンします。</span><span class="sxs-lookup"><span data-stu-id="b9856-119">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="b9856-120">出荷のすべての作業が作業者に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b9856-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="b9856-121">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="b9856-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="b9856-122"><strong>システム グループ化ラベル</strong> フィールドを使用して、作業者に何をスキャンするかを通知します。</span><span class="sxs-lookup"><span data-stu-id="b9856-122">Use the <strong>System grouping label</strong> field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="b9856-123">システム グループ化ラベル</span><span class="sxs-lookup"><span data-stu-id="b9856-123">System grouping label</span></span> |                       <span data-ttu-id="b9856-124"><strong>システム作業の許可</strong> が <strong>はい</strong> に設定されている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="b9856-124">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="b9856-125">ピッキング作業がグループ化されたときに、何をスキャンするかを作業者に通知する情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="b9856-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="b9856-126">たとえば、<strong>ShipmentId</strong> フィールドを使用して出荷別にピッキング作業をグループ化する場合、このフィールドに出荷 ID を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="b9856-126">For example, if you use the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="b9856-127">このフィールドは、システムによってグループ化された既存の作業を使用するメニュー項目の作成を要求します。</span><span class="sxs-lookup"><span data-stu-id="b9856-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="b9856-128">また、<strong>システム グループ化</strong> フィールドでグループ化するフィールドを選択する必要もあります。</span><span class="sxs-lookup"><span data-stu-id="b9856-128">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span>                       |

