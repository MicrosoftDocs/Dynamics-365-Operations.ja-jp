---
title: 在庫ブロックの作成および管理
description: このトピックでは、在庫ブロックを使用して、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956161"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="4fcf1-103">在庫ブロックの作成および管理</span><span class="sxs-lookup"><span data-stu-id="4fcf1-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4fcf1-104">このトピックでは、在庫ブロックを使用して、現物手持在庫が他の元伝票に引当されないようにする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="4fcf1-105">このトピックの手順を開始する前に、使用可能な現物手持在庫の品目が必要です。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="4fcf1-106">在庫のブロック</span><span class="sxs-lookup"><span data-stu-id="4fcf1-106">Block inventory</span></span>

<span data-ttu-id="4fcf1-107">在庫がブロックされるように在庫ブロック レコードを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="4fcf1-108">**在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="4fcf1-109">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="4fcf1-110">新しいブロック レコードのヘッダーで、**品目番号** フィールドにブロックする品目を設定し、説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="4fcf1-111">**全般** クイック タブの **数量** フィールドに、ブロックする品目の数を入力します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="4fcf1-112">**在庫分析コード** クイック タブで、ブロックする品目が現在保管されているサイトと倉庫を指定します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="4fcf1-113">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="4fcf1-114">在庫ブロックの条件の更新</span><span class="sxs-lookup"><span data-stu-id="4fcf1-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="4fcf1-115">在庫ブロック レコードを更新するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="4fcf1-116">**在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="4fcf1-117">一覧ペインで、関連するブロック レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="4fcf1-118">必要に応じてレコードを編集します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-118">Edit the record as required.</span></span> <span data-ttu-id="4fcf1-119">たとえば、**予定日** フィールドの値を変更して、ブロックされた在庫の引当可能日を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="4fcf1-120">**入庫予定** オプションが選択されている場合、予想されるトランザクションに日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="4fcf1-121">(ブロック レコードを手動で作成する場合、既定で **入庫予定** オプションが選択されます。)</span><span class="sxs-lookup"><span data-stu-id="4fcf1-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="4fcf1-122">アクション ウィンドウで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="4fcf1-123">在庫のブロック解除</span><span class="sxs-lookup"><span data-stu-id="4fcf1-123">Unblock inventory</span></span>

<span data-ttu-id="4fcf1-124">在庫がブロック解除されるように在庫ブロック レコードを削除するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="4fcf1-125">**在庫管理\>定期処理タスク\>在庫ブロック** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="4fcf1-126">一覧ペインで、関連するブロック レコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="4fcf1-127">アクション ウィンドウで **削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="4fcf1-128">操作を確認するように求められます。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="4fcf1-129">**はい** を選択して続行します。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="4fcf1-130">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4fcf1-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
