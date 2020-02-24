---
title: オンライン チャンネルの作成およびチャンネルの属性の定義
description: この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bac365217c20bececa1b4ff2b9de12288326dcc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023167"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="5fd60-103">オンライン チャンネルの作成およびチャンネルの属性の定義</span><span class="sxs-lookup"><span data-stu-id="5fd60-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5fd60-104">この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。</span><span class="sxs-lookup"><span data-stu-id="5fd60-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="5fd60-105">新しいオンライン チャンネルを作成する前に、組織階層を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fd60-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="5fd60-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="5fd60-107">新しいオンライン チャンネルの作成</span><span class="sxs-lookup"><span data-stu-id="5fd60-107">Create a new online channel</span></span>
1. <span data-ttu-id="5fd60-108">Retail と Commerce > チャネル > オンライン ストアに移動します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="5fd60-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-109">Click New.</span></span>
3. <span data-ttu-id="5fd60-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="5fd60-111">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="5fd60-112">[ストア タイムゾーン] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="5fd60-113">[既定の顧客] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="5fd60-114">[顧客のアドレス帳] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="5fd60-115">[支払条件] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="5fd60-116">[支払方法] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="5fd60-117">[電子メール通知 プロファイル] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="5fd60-118">[財務分析コード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="5fd60-119">[事業単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="5fd60-120">同様に、そのほかの既定の分析コードの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="5fd60-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="5fd60-122">組織階層にオンライン チャンネルを追加します</span><span class="sxs-lookup"><span data-stu-id="5fd60-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="5fd60-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5fd60-123">Close the page.</span></span>
2. <span data-ttu-id="5fd60-124">[組織管理] > [組織] > [組織階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="5fd60-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5fd60-126">[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-126">Click View.</span></span>
5. <span data-ttu-id="5fd60-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-127">Click Edit.</span></span>
    * <span data-ttu-id="5fd60-128">新しいチャンネルを挿入する階層ノードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5fd60-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="5fd60-129">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-129">Click Insert.</span></span>
7. <span data-ttu-id="5fd60-130">Commerce チャネルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="5fd60-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-131">Click OK.</span></span>
9. <span data-ttu-id="5fd60-132">[発行] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="5fd60-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="5fd60-133">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="5fd60-134">[発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5fd60-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="5fd60-135">ほぼリアルタイムのオーダー通知のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5fd60-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="5fd60-136">Retail と Commerce > バックオフィスの設定 > パラメーター > Commerce パラメーターの順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="5fd60-137">電子商取引 オーダー作成のリアルタイム サービス使用を、「はい」に設定します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="5fd60-138">チャンネル データベースへの同期変更に、1070 配送スケジュールを実行します。</span><span class="sxs-lookup"><span data-stu-id="5fd60-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


