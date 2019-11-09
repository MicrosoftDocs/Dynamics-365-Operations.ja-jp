---
title: 社内の商品移動の移動文書の設定
description: この手順では、社内の製品移動に関わるドキュメントを作成する方法を示します。
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransferOrders, InventLocationIdLookup, TransportationDocument, HcmWorkerLookUp, SrsReportViewerForm, InventTransferParmShip
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe4dd04595c961e1c66178e6ac6955e945869ded
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185684"
---
# <a name="set-up-the-transfer-documents-for-goods-movement-inside-a-company"></a><span data-ttu-id="9e8ea-103">社内の商品移動の移動文書の設定</span><span class="sxs-lookup"><span data-stu-id="9e8ea-103">Set up the transfer documents for goods movement inside a company</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e8ea-104">この手順では、社内の製品移動に関わるドキュメントを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-104">This procedure shows how to create transfer documents for goods movement inside a company.</span></span> <span data-ttu-id="9e8ea-105">この手順はリトアニアに主たる所在地を置く法人のみが使用できます。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-105">This procedure is only available for legal entities with a primary address in Lithuania.</span></span> <span data-ttu-id="9e8ea-106">この手順は、リトアニアに主たる事務所を置く企業 DEMF のデモデータを使用して作成されました。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-106">The procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="9e8ea-107">この手順を完了するには、「社内の製品移動に関わるドキュメントの設定」の手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-107">Before you can complete this procedure, you must complete the “Set up transfer documents for goods movement inside a company” procedure.</span></span> <span data-ttu-id="9e8ea-108">この手順は在庫経理担当者を対象としています。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-108">This procedure is intended for inventory accountants.</span></span> <span data-ttu-id="9e8ea-109">この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-transfer-order"></a><span data-ttu-id="9e8ea-110">移動オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="9e8ea-110">Create a transfer order</span></span>
1. <span data-ttu-id="9e8ea-111">[在庫管理] > [受信した注文] > [移動オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-111">Go to Inventory management > Inbound orders > Transfer order.</span></span>
2. <span data-ttu-id="9e8ea-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-112">Click New.</span></span>
3. <span data-ttu-id="9e8ea-113">[移動元倉庫] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-113">In the From warehouse field, enter or select a value.</span></span>
4. <span data-ttu-id="9e8ea-114">[移動先倉庫] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-114">In the To warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="9e8ea-115">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-115">Click Add.</span></span>
6. <span data-ttu-id="9e8ea-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-116">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="9e8ea-117">[品目番号] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-117">In the Item number field, enter or select a value.</span></span>

## <a name="enter-transportation-details-for-the-transfer-order"></a><span data-ttu-id="9e8ea-118">移動オーダーの配送情報を入力する</span><span class="sxs-lookup"><span data-stu-id="9e8ea-118">Enter transportation details for the transfer order</span></span>
1. <span data-ttu-id="9e8ea-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-119">Click Save.</span></span>
2. <span data-ttu-id="9e8ea-120">アクション ウィンドウで、[発送] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-120">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9e8ea-121">[輸送の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-121">Click Transportation details.</span></span>
4. <span data-ttu-id="9e8ea-122">[配送情報の印刷] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-122">Select Yes in the Print transportation details field.</span></span>
5. <span data-ttu-id="9e8ea-123">[製品配送元] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-123">In the Goods issued by field, enter or select a value.</span></span>
6. <span data-ttu-id="9e8ea-124">[パッケージ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-124">In the Package field, type a value.</span></span>
7. <span data-ttu-id="9e8ea-125">[積荷のリスクレベル] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-125">In the Risk level of the load field, type a value.</span></span>
8. <span data-ttu-id="9e8ea-126">[配送業者] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-126">In the Carrier field, enter or select a value.</span></span>
9. <span data-ttu-id="9e8ea-127">[モデル] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-127">In the Model field, enter or select a value.</span></span>
10. <span data-ttu-id="9e8ea-128">[登録番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-128">In the Registration number field, type a value.</span></span>
11. <span data-ttu-id="9e8ea-129">[トレーラー登録番号] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-129">In the Trailer registration number field, type a value.</span></span>
12. <span data-ttu-id="9e8ea-130">[ドライバー] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-130">In the Driver field, enter or select a value.</span></span>
13. <span data-ttu-id="9e8ea-131">[ドライバー名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-131">In the Driver name field, type a value.</span></span>
14. <span data-ttu-id="9e8ea-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-132">Click Save.</span></span>
15. <span data-ttu-id="9e8ea-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-133">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-unposted-transfer-order"></a><span data-ttu-id="9e8ea-134">未転記の移動オーダーの梱包明細を表示する </span><span class="sxs-lookup"><span data-stu-id="9e8ea-134">View the packing slip for the unposted transfer order</span></span>
1. <span data-ttu-id="9e8ea-135">[梱包明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-135">Click Packing slip.</span></span>
2. <span data-ttu-id="9e8ea-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-136">Click OK.</span></span>
3. <span data-ttu-id="9e8ea-137">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-137">Close the page.</span></span>

## <a name="view-the-packing-slip-for-the-posted-transfer-order"></a><span data-ttu-id="9e8ea-138">転記済みの移動オーダーの梱包明細を表示する </span><span class="sxs-lookup"><span data-stu-id="9e8ea-138">View the packing slip for the posted transfer order</span></span>
1. <span data-ttu-id="9e8ea-139">アクション ウィンドウで、[移動オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-139">On the Action Pane, click Transfer order.</span></span>
2. <span data-ttu-id="9e8ea-140">アクション ウィンドウで、[発送] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-140">On the Action Pane, click Ship.</span></span>
3. <span data-ttu-id="9e8ea-141">[発送移動オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-141">Click Ship transfer order.</span></span>
4. <span data-ttu-id="9e8ea-142">[一般] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-142">Click the General tab.</span></span>
5. <span data-ttu-id="9e8ea-143">[更新] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-143">In the Update field, select an option.</span></span>
6. <span data-ttu-id="9e8ea-144">[概要] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-144">Click the Overview tab.</span></span>
7. <span data-ttu-id="9e8ea-145">[梱包明細] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-145">In the Packing slip field, type a value.</span></span>
8. <span data-ttu-id="9e8ea-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-146">Click OK.</span></span>
9. <span data-ttu-id="9e8ea-147">アクション ウィンドウで、[発送] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-147">On the Action Pane, click Ship.</span></span>
10. <span data-ttu-id="9e8ea-148">[梱包明細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-148">Click Packing slip.</span></span>
11. <span data-ttu-id="9e8ea-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9e8ea-149">Click OK.</span></span>
