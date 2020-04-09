---
title: 在庫品目要求からの発注品目の入庫
description: このトピックでは、在庫品目要求から発注書の品目を受け取る方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f288a47f952a30d98a4a5b96409dc53f880d41d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139063"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="3edf2-103">在庫品目要求からの発注品目の入庫</span><span class="sxs-lookup"><span data-stu-id="3edf2-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3edf2-104">このトピックでは、在庫品目要求から発注書の品目を受け取る方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="3edf2-105">品目トランザクションではなく在庫品目要求を使用することによって、品目が実際に使用される直前の配送を計画したり、発注書を作成したり、品目を売買契約の枠組みに含めたり、在庫品目要求を生産計画に含めたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="3edf2-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="3edf2-106">このタスクでは、USSI データ セットを使用します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="3edf2-107">ナビゲーション ウィンドウで、**モジュール > プロジェクト管理および会計 > プロジェクト > すべてのプロジェクト**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="3edf2-108">一覧で、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="3edf2-109">アクション ウィンドウで、**計画**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="3edf2-110">**在庫品目要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="3edf2-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-111">Select **New**.</span></span>
6. <span data-ttu-id="3edf2-112">新しい行で、**品目番号**フィールドに値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="3edf2-113">**数量**フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="3edf2-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-114">Select **Save**.</span></span>
9. <span data-ttu-id="3edf2-115">アクション ウィンドウで、**管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="3edf2-116">**機能**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-116">Select **Functions**.</span></span>
11. <span data-ttu-id="3edf2-117">**発注書の作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="3edf2-118">**すべてを含む**のチェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="3edf2-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="3edf2-119">**仕入先**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="3edf2-120">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-120">Select **OK**.</span></span>
15. <span data-ttu-id="3edf2-121">ナビゲーション ウィンドウで、**モジュール > 買掛金勘定 > 発注書 > すべての発注書**に移動します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="3edf2-122">一覧で、目的の行のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="3edf2-123">アクション ウィンドウで、**購買**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="3edf2-124">**確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="3edf2-125">アクション ウィンドウで、**入庫**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="3edf2-126">**製品受領書**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="3edf2-127">**製品受領書**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="3edf2-128">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3edf2-128">Select **OK**.</span></span>

