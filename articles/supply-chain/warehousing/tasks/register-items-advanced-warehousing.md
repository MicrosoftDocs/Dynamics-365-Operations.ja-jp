---
title: 品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録
description: このトピックでは、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示すシナリオを示します。
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c58aa1cec6c0bfe33fa1ef90267dcd8ac1218157
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830837"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="2249c-103">品目の着荷仕訳帳を使用した高度な倉庫管理に対応した品目の登録</span><span class="sxs-lookup"><span data-stu-id="2249c-103">Register items for an advanced warehousing enabled item using an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2249c-104">このトピックでは、高度な倉庫管理プロセスを使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示すシナリオを示します。</span><span class="sxs-lookup"><span data-stu-id="2249c-104">This topic presents a scenario that shows how to register items using the item arrival journal when you are using advanced warehouse management processes.</span></span> <span data-ttu-id="2249c-105">これは通常、入荷係により行われます。</span><span class="sxs-lookup"><span data-stu-id="2249c-105">This would usually be done by a receiving clerk.</span></span>

## <a name="enable-sample-data"></a><span data-ttu-id="2249c-106">サンプルデータの有効化</span><span class="sxs-lookup"><span data-stu-id="2249c-106">Enable sample data</span></span>

<span data-ttu-id="2249c-107">このトピックで指定したサンプルのレコードと値を使用してこのシナリオを実行するには、標準のデモ データがインストールされているシステムを使用している必要があります。また、開始する前に *USMF* 法人を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-107">To work through this scenario using the sample records and values specified in this topic, you must be using a system where the standard demo data is installed, and you must select the *USMF* legal entity before you begin.</span></span>

<span data-ttu-id="2249c-108">代わりに、次のデータがある場合は、独自のデータから値を代入してこのシナリオを実行できます。</span><span class="sxs-lookup"><span data-stu-id="2249c-108">You can instead work through this scenario by substituting values from your own data provided that you have the following data available:</span></span>

- <span data-ttu-id="2249c-109">確認された発注書に対して、オープンな発注書の明細行を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-109">You must have a confirmed purchase order with an open purchase order line.</span></span>
- <span data-ttu-id="2249c-110">明細行の品目は在庫がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-110">The item on the line must be stocked.</span></span> <span data-ttu-id="2249c-111">製品バリアントを使用することはできません。追跡分析コードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="2249c-111">It must not use product variants, and must not have tracking dimensions.</span></span>
- <span data-ttu-id="2249c-112">その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-112">The item must be associated with a storage dimension group that has warehouse management process enabled.</span></span>
- <span data-ttu-id="2249c-113">使用される倉庫は、倉庫管理プロセスに対して有効化されている必要があり、また受入に使う場所は、ライセンス プレートにより管理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-113">The warehouse that's used must be enabled for warehouse management processes and the location that you use for receiving must be license plate controlled.</span></span>

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a><span data-ttu-id="2249c-114">倉庫管理を使用する着品目仕訳帳ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="2249c-114">Create an item arrival journal header that uses warehouse management</span></span>

<span data-ttu-id="2249c-115">次のシナリオでは、倉庫管理を使用して着品目仕訳帳ヘッダーを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2249c-115">The following scenario shows how to create an item arrival journal header that uses warehouse management:</span></span>

1. <span data-ttu-id="2249c-116">前のセクションで示した要件を満たす確認済発注書がシステムに含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-116">Make sure your system contains a confirmed purchase order that fulfils the requirements outlined in the previous section.</span></span> <span data-ttu-id="2249c-117">このシナリオでは、品目番号 *M9200* の *10 PL* (10 パレット) の明細行を持つ、会社 *USMF*、仕入先アカウント *1001*、倉庫 *51* の発注書にを使用します。</span><span class="sxs-lookup"><span data-stu-id="2249c-117">This scenario uses a purchase order for company *USMF*, vendor account *1001*, warehouse *51*, with an order line for *10 PL* (10 pallets) of item number *M9200*.</span></span>
1. <span data-ttu-id="2249c-118">使用する発注書番号をメモします。</span><span class="sxs-lookup"><span data-stu-id="2249c-118">Make a note of the purchase order number that you will use.</span></span>
1. <span data-ttu-id="2249c-119">**在庫管理 \> 仕訳入力 \> 品目到着 \> 品目到着** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2249c-119">Go to **Inventory management \> Journal entries \> Item arrival \> Item arrival**.</span></span>
1. <span data-ttu-id="2249c-120">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-120">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="2249c-121">**倉庫管理仕訳帳の作成** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="2249c-121">The **Create warehouse management journal** dialog box opens.</span></span> <span data-ttu-id="2249c-122">**名前** フィールドで、仕訳名を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-122">Select a journal name in the **Name** field.</span></span>
    - <span data-ttu-id="2249c-123">*USFM* サンプル データを使用している場合は、*WHS* を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-123">If you are using *USMF* sample data, select *WHS*.</span></span>
    - <span data-ttu-id="2249c-124">独自のデータを使用している場合は、選択した仕訳帳で **ピッキング場所の確認** が *いいえ* に、**検査管理** が *いいえ* に設定されている 必要があります 。</span><span class="sxs-lookup"><span data-stu-id="2249c-124">If you're using your own data, the journal you choose must have **Check picking location** set to *No* and **Quarantine management** set to *No*.</span></span>
1. <span data-ttu-id="2249c-125">**照会** を *発注書* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-125">Set **Reference** to *Purchase order*.</span></span>
1. <span data-ttu-id="2249c-126">**アカウント番号** を *1001* を設定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-126">Set **Account number** to *1001*.</span></span>
1. <span data-ttu-id="2249c-127">**番号** をこの演習で指定した発注書の番号に設定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-127">Set **Number** to the number of the purchase order that you identified for this exercise.</span></span>

    <span data-ttu-id="2249c-128">![着荷仕訳帳](../media/item-arrival-journal-header.png "着荷仕訳帳")</span><span class="sxs-lookup"><span data-stu-id="2249c-128">![Item arrival journal](../media/item-arrival-journal-header.png "Item arrival journal")</span></span>

1. <span data-ttu-id="2249c-129">仕訳帳ヘッダーを作成するには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-129">Select the **OK** to create the journal header.</span></span>
1. <span data-ttu-id="2249c-130">**仕訳帳明細行** セクションで、**行の追加** を選択 し、次のデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="2249c-130">In the **Journal lines** section, select **Add line** and enter the following data:</span></span>
    - <span data-ttu-id="2249c-131">**品目番号** - *M9200* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-131">**Item number** – Set to *M9200*.</span></span> <span data-ttu-id="2249c-132">**サイト**、**倉庫**、および **数量** は、10 パレット (各 1000) の在庫トランザクション データに基づいて設定されます。</span><span class="sxs-lookup"><span data-stu-id="2249c-132">The **Site**, **Warehouse**, and **Quantity** will get set based on the inventory transaction data for the 10 pallets (1000 ea.).</span></span>
    - <span data-ttu-id="2249c-133">**場所** - *001* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-133">**Location** – Set to  *001*.</span></span> <span data-ttu-id="2249c-134">この特定の場所はライセンス プレートを追跡しません。</span><span class="sxs-lookup"><span data-stu-id="2249c-134">This specific location does not track license plates.</span></span>

    <span data-ttu-id="2249c-135">![品目到着の仕訳帳明細行](../media/item-arrival-journal-line.png "品目到着の仕訳帳明細行")</span><span class="sxs-lookup"><span data-stu-id="2249c-135">![Item arrival journal line](../media/item-arrival-journal-line.png "Item arrival journal line")</span></span>

    > [!NOTE]
    > <span data-ttu-id="2249c-136">**日付** フィールドは、この品目の手持在庫数量が在庫に登録される日付を決定します。</span><span class="sxs-lookup"><span data-stu-id="2249c-136">The **Date** field determines the date on which the on-hand quantity of this item will be registered in the inventory.</span></span>  
    >
    > <span data-ttu-id="2249c-137">**ロット ID** は、提供された情報から一意に識別される場合に、システムによって設定されます。</span><span class="sxs-lookup"><span data-stu-id="2249c-137">The **Lot ID** will be populated by the system if it can be uniquely identified from the information provided.</span></span> <span data-ttu-id="2249c-138">それ以外の場合は手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-138">Otherwise you will have to enter this manually.</span></span> <span data-ttu-id="2249c-139">これは、特定の元伝票明細行にこの登録をリンクする必須のフィールドです。</span><span class="sxs-lookup"><span data-stu-id="2249c-139">This is a required field, which links this registration to a specific source document line.</span></span>  

1. <span data-ttu-id="2249c-140">アクション ペインで、**検証** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-140">Select **Validate** on the Action Pane.</span></span> <span data-ttu-id="2249c-141">これは、仕訳帳が転記できる状態かどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="2249c-141">This checks that the journal is ready to be posted.</span></span> <span data-ttu-id="2249c-142">検証が失敗する場合、仕訳帳を転記する前にエラーを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2249c-142">If the validation fails you will need to fix the errors before you can post the journal.</span></span>  
1. <span data-ttu-id="2249c-143">**仕訳帳の確認** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="2249c-143">The **Check journal** dialog box opens.</span></span> <span data-ttu-id="2249c-144">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-144">Select **OK**.</span></span>
1. <span data-ttu-id="2249c-145">メッセージ バーをレビューします。</span><span class="sxs-lookup"><span data-stu-id="2249c-145">Review the message bar.</span></span> <span data-ttu-id="2249c-146">操作が完了したというメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="2249c-146">There should be a message denoting that the operation was completed.</span></span>  
1. <span data-ttu-id="2249c-147">アクション ペインで、**転記** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-147">Select **Post** on the Action Pane.</span></span>
1. <span data-ttu-id="2249c-148">**仕訳帳の転記** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="2249c-148">The **Post journal** dialog box opens.</span></span> <span data-ttu-id="2249c-149">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2249c-149">Select **OK**.</span></span>
1. <span data-ttu-id="2249c-150">メッセージ バーをレビューします。</span><span class="sxs-lookup"><span data-stu-id="2249c-150">Review the message bar.</span></span> <span data-ttu-id="2249c-151">操作完了というメッセージが表示されるはずです。</span><span class="sxs-lookup"><span data-stu-id="2249c-151">There should be messages denoting that the operation completed.</span></span>
1. <span data-ttu-id="2249c-152">アクション ペインで **機能 > 製品入庫** を選択して、発注書の明細行を更新し 、製品入庫を転記します。</span><span class="sxs-lookup"><span data-stu-id="2249c-152">Select **Functions > Product receipt** on the Action Pane to update the purchase order line and post a product receipt.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
