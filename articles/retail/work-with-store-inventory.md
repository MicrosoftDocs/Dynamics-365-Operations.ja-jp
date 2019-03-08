---
title: 店舗在庫管理
description: このトピックでは、在庫の管理に使用できるドキュメントのタイプについて説明します。
author: rubencdelgado
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 21391
ms.assetid: bfef3717-d0e0-491d-8466-d8a9c995177d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 02f8afbe3bb6f94c66a8b5aa02531c219adc3963
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "339237"
---
# <a name="store-inventory-management"></a><span data-ttu-id="0313a-103">店舗在庫管理</span><span class="sxs-lookup"><span data-stu-id="0313a-103">Store inventory management</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0313a-104">このトピックでは、在庫の管理に使用できるドキュメントのタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0313a-104">This topic describes the types of documents that you can use to manage inventory.</span></span>

<span data-ttu-id="0313a-105">組織の在庫を管理するには、次のドキュメント タイプを使用できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-105">You can use the following types of documents to manage your organization's inventory.</span></span>

<span data-ttu-id="0313a-106">Dynamics 365 for Retail で在庫処理および POS アプリケーションを使用する場合、POS は在庫分析コードおよび特定の在庫品目タイプに対して限定的なサポートを提供することに注意することが重要です。</span><span class="sxs-lookup"><span data-stu-id="0313a-106">When working with inventory in Dynamics 365 for Retail and using the POS application, it is important to note that POS provides limited support for inventory dimensions and certain inventory item types.</span></span>  

<span data-ttu-id="0313a-107">POS ソリューションは、以下の品目構成をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="0313a-107">The POS solution does not support the following item configurations:</span></span>
- <span data-ttu-id="0313a-108">BOM 品目 (BOM フレームワークの一部のコンポーネントを利用するキット製品を除く)</span><span class="sxs-lookup"><span data-stu-id="0313a-108">BOM items (except kit products, which utilize some components of the BOM framework)</span></span>
- <span data-ttu-id="0313a-109">CW 品目</span><span class="sxs-lookup"><span data-stu-id="0313a-109">Catch weight items</span></span>
- <span data-ttu-id="0313a-110">バッチ管理されている品目</span><span class="sxs-lookup"><span data-stu-id="0313a-110">Batch-controlled items</span></span>

<span data-ttu-id="0313a-111">POS アプリケーションは現在、POS の次の追跡用分析コードをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="0313a-111">The POS application currently does not support the following tracking dimensions in the POS:</span></span>
- <span data-ttu-id="0313a-112">バッチ追跡用分析コード</span><span class="sxs-lookup"><span data-stu-id="0313a-112">Batch tracking dimension</span></span>
- <span data-ttu-id="0313a-113">所有者分析コード</span><span class="sxs-lookup"><span data-stu-id="0313a-113">Owner dimension</span></span>

<span data-ttu-id="0313a-114">POS ソリューションは、以下の分析コードに対して限定的なサポートを提供します。</span><span class="sxs-lookup"><span data-stu-id="0313a-114">The POS solution provides limited support for the following dimensions.</span></span> <span data-ttu-id="0313a-115">限定的なサポートということは、POS が倉庫/店舗のセットアップ構成に基づいて自動的に在庫トランザクションにこれらの分析コードのいくつかを既定設定する可能性を示しています。</span><span class="sxs-lookup"><span data-stu-id="0313a-115">Limited support indicates that the POS may default some of these dimensions into inventory transactions automatically based on warehouse/store setup configuration.</span></span> <span data-ttu-id="0313a-116">POSは、販売トランザクションが手動で ERP に入力された場合のような方法で分析コードを完全にはサポートしません。</span><span class="sxs-lookup"><span data-stu-id="0313a-116">POS will not fully support the dimensions in the way they are supported if a sales transaction is manually entered into the ERP.</span></span> 

- <span data-ttu-id="0313a-117">保管場所</span><span class="sxs-lookup"><span data-stu-id="0313a-117">Location</span></span>
- <span data-ttu-id="0313a-118">ライセンス プレート (商品と店舗倉庫で**倉庫管理プロセスを使用**が有効になっている場合にのみ適用可能)</span><span class="sxs-lookup"><span data-stu-id="0313a-118">License plate (only applicable when **Uuse warehouse management process** has been enabled on the item and the store warehouse)</span></span>
- <span data-ttu-id="0313a-119">シリアル番号</span><span class="sxs-lookup"><span data-stu-id="0313a-119">Serial number</span></span>
- <span data-ttu-id="0313a-120">在庫状態</span><span class="sxs-lookup"><span data-stu-id="0313a-120">Inventory status</span></span>

> [!NOTE]
> <span data-ttu-id="0313a-121">すべての組織は、POS を通して本番環境の展開前に、開発環境またはテスト環境で品目コンフィギュレーションをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0313a-121">All organizations must test item configurations through POS in development or test environments before deploying them to production.</span></span> <span data-ttu-id="0313a-122">通常の現金払いの販売トランザクションを実行したり、POS を通して商品の顧客注文(該当する場合)を作成したりして、品目のテストをします。</span><span class="sxs-lookup"><span data-stu-id="0313a-122">Test your items by performing regular cash and carry sales transacting and creating customer orders (if applicable) through the POS with your items.</span></span> <span data-ttu-id="0313a-123">テストには、テスト環境で明細書転記プロセスを完全に実行し、問題がないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0313a-123">Testing must include running a full statement posting processes in your test environment and verifying that there are no issues.</span></span>
> <span data-ttu-id="0313a-124">適切なテストを行わずに、POS アプリケーションでサポートされていない方法でアイテムを構成すると、問題を修正する簡単な方法がないまま、明細書転記プロセスが生産に失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0313a-124">Configuring items in a way that is not supported by the POS application, without proper testing, can result in your statement posting process failing in production without an easy way to correct the issues.</span></span> <span data-ttu-id="0313a-125">アプリケーションに対するパートナーまたは顧客のカスタマイズは、これらの転記プロセスが正常に完了させるために必要に応じて考慮することができます。</span><span class="sxs-lookup"><span data-stu-id="0313a-125">Partner or customer customizations to the application may optionally be considered to allow these posting processes to successfully complete.</span></span> <span data-ttu-id="0313a-126">カスタマイズが不要な場合、組織は標準の POS アプリケーション/注文の作成/明細書転記プロセスでサポートされている方法で製品の製品コンフィギュレーションが行われていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0313a-126">If customizations are not needed, the organization must ensure that the product configuration of your products has been done in a way that is supported by the standard POS application/order creation/statement posting process.</span></span>

## <a name="purchase-orders"></a><span data-ttu-id="0313a-127">発注書</span><span class="sxs-lookup"><span data-stu-id="0313a-127">Purchase orders</span></span>

<span data-ttu-id="0313a-128">発注書は本社で作成されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-128">Purchase orders are created at the head office.</span></span> <span data-ttu-id="0313a-129">小売倉庫が発注書ヘッダーに含まれている場合、Microsoft Dynamics 365 for Retail の Modern POS (MPOS) または Cloud POS を使用して、注文を店舗で受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="0313a-129">If a retail warehouse is included in the purchase order header, the order can be received at the store by using Modern POS (MPOS) or Cloud POS in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="0313a-130">店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-130">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="0313a-131">または、数量を確定して本社に送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="0313a-131">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="0313a-132">本社では、店舗で受け取った数量が Dynamics 365 for Retail の発注書の**今回受入**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-132">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the purchase order.</span></span>

## <a name="transfer-orders"></a><span data-ttu-id="0313a-133">移動オーダー</span><span class="sxs-lookup"><span data-stu-id="0313a-133">Transfer orders</span></span>

<span data-ttu-id="0313a-134">移動オーダーでは、特定の店舗が品目の出荷元の場所であることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-134">A transfer order can specify that a particular store is a location that items can be shipped from.</span></span> <span data-ttu-id="0313a-135">この場合、移動オーダーは MPOS またはクラウド POS のピッキング要求として店舗に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-135">In this case, the transfer order appears at the store as a picking request in MPOS or Cloud POS.</span></span> <span data-ttu-id="0313a-136">必要な数量をピッキングした後、その数量が確定され、本社に送信されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-136">After the quantities that are requested are picked, they are committed and sent to the head office.</span></span> <span data-ttu-id="0313a-137">本社では、店舗でピッキングされた数量が Dynamics 365 for Retail の移動オーダーの**今すぐ出荷**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-137">At the head office, the quantities that were picked at the store are displayed in Dynamics 365 for Retail, in the **Ship now** field on the transfer order.</span></span> <span data-ttu-id="0313a-138">移動オーダーでは、特定の店舗が品目の出荷先の場所であることを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-138">A transfer order may specify that a particular store is a location that items can be shipped to.</span></span> <span data-ttu-id="0313a-139">この場合、移動オーダーは MPOS またはクラウド POS の入荷要求として店舗に表示されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-139">In this case, the transfer order appears at the store as a receiving request in MPOS or Cloud POS.</span></span> <span data-ttu-id="0313a-140">店舗で受け入れる数量が入力された後、追加変更に対してその数量をローカルに保存できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-140">After the quantities that are received at the store are entered, they can be saved locally for additional modification.</span></span> <span data-ttu-id="0313a-141">または、数量を確定して本社に送信することもできます。</span><span class="sxs-lookup"><span data-stu-id="0313a-141">Alternatively, the quantities can be committed and sent to the head office.</span></span> <span data-ttu-id="0313a-142">本社では、店舗で受け取った数量が Dynamics 365 for Retail の移動オーダーの**今回受入**フィールドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-142">At the head office, the quantities that were received at the store are displayed in Dynamics 365 for Retail, in the **Receive now** field on the transfer order.</span></span>

## <a name="stock-counts"></a><span data-ttu-id="0313a-143">在庫数</span><span class="sxs-lookup"><span data-stu-id="0313a-143">Stock counts</span></span>

<span data-ttu-id="0313a-144">在庫棚卸は、計画済または計画外のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="0313a-144">Stock counts can be either scheduled or unscheduled.</span></span> <span data-ttu-id="0313a-145">計画済の在庫棚卸は、棚卸を行う必要がある品目を指定する本社で開始されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-145">Scheduled stock counts are initiated at the head office, which specifies the items that must be counted.</span></span> <span data-ttu-id="0313a-146">本社で店舗に送信可能な棚卸ドキュメントが作成され、実際の手持在庫数量が店舗で MPOS またはクラウド POS に入力されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-146">The head office creates a counting document that can be received at the store, where the quantities of actual on-hand stock are entered in MPOS or Cloud POS.</span></span> <span data-ttu-id="0313a-147">手動在庫棚卸は店舗で開始され、MPOS またはクラウド POS で実際の手持在庫数量が更新されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-147">Unscheduled stock counts are initiated at a store, and the quantities of actual on-hand stock are updated in either MPOS or Cloud POS.</span></span> <span data-ttu-id="0313a-148">計画済在庫棚卸とは異なり、計画外在庫棚卸に品目の定義済リストはありません。</span><span class="sxs-lookup"><span data-stu-id="0313a-148">Unlike scheduled stock counts, unscheduled stock counts do not have a predefined list of items.</span></span> <span data-ttu-id="0313a-149">いずれかのタイプの在庫棚卸が完了すると、その在庫棚卸が確定され、本社に送信されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-149">When a stock count of either type is completed, it is committed and sent to the head office.</span></span> <span data-ttu-id="0313a-150">本社でその在庫棚卸が検証され、転記されます。</span><span class="sxs-lookup"><span data-stu-id="0313a-150">At the head office, the count is validated and posted.</span></span>

## <a name="inventory-lookup"></a><span data-ttu-id="0313a-151">在庫検索</span><span class="sxs-lookup"><span data-stu-id="0313a-151">Inventory lookup</span></span>

<span data-ttu-id="0313a-152">複数の店舗および倉庫の現在の手持在庫製品の数量は、在庫検索ページで表示できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-152">The current product quantity on hand for multiple stores and warehouses can be viewed on the Inventory lookup page.</span></span> <span data-ttu-id="0313a-153">手持在庫の現在の数量に加えて、将来の納期回答可能在庫 (ATP) 数量は、各店舗ごとに表示できます。</span><span class="sxs-lookup"><span data-stu-id="0313a-153">In addition to the current quantity on hand, the future available to promise (ATP) quantities can be viewed for each individual store.</span></span> <span data-ttu-id="0313a-154">これを行うには、表示したい ATP の店舗を選択して、次に **店舗の使用可能性を表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0313a-154">To do so, select the store that you want to view the ATP for and then click **Show store availability**.</span></span>
