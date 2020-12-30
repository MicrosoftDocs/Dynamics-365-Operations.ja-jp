---
title: 品目を使用して、基本倉庫が有効な品目の品目を着荷仕訳帳登録します。
description: この手順では、在庫管理モジュールで、"基本倉庫保管" を使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 940fa33b10c5f60f469187b11dd066091581996f
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4432295"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="ec862-103">品目を使用して、基本倉庫が有効な品目の品目を着荷仕訳帳登録します。</span><span class="sxs-lookup"><span data-stu-id="ec862-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec862-104">この手順では、在庫管理モジュールで、"基本倉庫保管" を使用する場合に、着荷仕訳帳を使用して品目を登録する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ec862-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="ec862-105">これは通常、入荷係により行われます。</span><span class="sxs-lookup"><span data-stu-id="ec862-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="ec862-106">表示されているサンプル値を使用して、デモ データの会社 USMF でこの手順を実行できます。</span><span class="sxs-lookup"><span data-stu-id="ec862-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="ec862-107">USMF を使用していない場合、このガイドを開始する前に、未処理の発注書明細行と共に確認済の発注書が必要です。</span><span class="sxs-lookup"><span data-stu-id="ec862-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="ec862-108">明細行の品目は在庫がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec862-108">The item on the line must be stocked.</span></span> <span data-ttu-id="ec862-109">その品目は、倉庫管理プロセスが有効化された保管分析コード グループと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec862-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="ec862-110">着荷仕訳帳ヘッダーの作成</span><span class="sxs-lookup"><span data-stu-id="ec862-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="ec862-111">[在庫管理] > [仕訳入力] > [品目到着] > [品目到着] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ec862-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="ec862-112">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-112">Click New.</span></span>
3. <span data-ttu-id="ec862-113">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec862-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ec862-114">USMF を使用している場合、「WHS」と入力できます。</span><span class="sxs-lookup"><span data-stu-id="ec862-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="ec862-115">その他のデータを使用している場合、名前を選択した仕訳帳は次のプロパティを必要とします : ピッキング場所の確認 は いいえ に設定し、検査管理 は いいえ に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec862-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="ec862-116">[梱包明細] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ec862-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="ec862-117">これは、仕入先によって発行された梱包明細の梱包明細 ID です。</span><span class="sxs-lookup"><span data-stu-id="ec862-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="ec862-118">固有の参照番号を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec862-118">Add a unique number.</span></span>  
5. <span data-ttu-id="ec862-119">[番号] フィールドで発注書を選択します。</span><span class="sxs-lookup"><span data-stu-id="ec862-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="ec862-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="ec862-121">行を着荷仕訳帳に追加する</span><span class="sxs-lookup"><span data-stu-id="ec862-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="ec862-122">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-122">Click Functions.</span></span>
2. <span data-ttu-id="ec862-123">[行の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-123">Click Create lines.</span></span>
    * <span data-ttu-id="ec862-124">この明細行はこの仕訳帳に手動で入力でき、または自動的に作成できます。</span><span class="sxs-lookup"><span data-stu-id="ec862-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="ec862-125">そして、これを自動的に作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ec862-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="ec862-126">[数量の初期化] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="ec862-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="ec862-127">さらに、購買注文明細行で登録されていない数量と仕訳帳明細行の数量を初期化します。</span><span class="sxs-lookup"><span data-stu-id="ec862-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="ec862-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="ec862-129">仕訳帳の転記</span><span class="sxs-lookup"><span data-stu-id="ec862-129">Post the journal</span></span>
1. <span data-ttu-id="ec862-130">[転記] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-130">Click Post.</span></span>
2. <span data-ttu-id="ec862-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="ec862-132">製品受領書の生成</span><span class="sxs-lookup"><span data-stu-id="ec862-132">Generate the product receipt</span></span>
1. <span data-ttu-id="ec862-133">[機能] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-133">Click Functions.</span></span>
2. <span data-ttu-id="ec862-134">[製品受領書] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-134">Click Product receipt.</span></span>
3. <span data-ttu-id="ec862-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ec862-135">Click OK.</span></span>

