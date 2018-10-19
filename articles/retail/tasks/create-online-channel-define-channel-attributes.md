--- 
title: "オンライン チャンネルの作成およびチャンネルの属性の定義"
description: "この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。"
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="ca332-103">オンライン チャンネルの作成およびチャンネルの属性の定義</span><span class="sxs-lookup"><span data-stu-id="ca332-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ca332-104">この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。</span><span class="sxs-lookup"><span data-stu-id="ca332-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="ca332-105">新しいオンライン チャンネルを作成する前に、組織階層を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ca332-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="ca332-106">この手順では、デモ データの会社 USRT を使用します。</span><span class="sxs-lookup"><span data-stu-id="ca332-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="ca332-107">新しいオンライン チャンネルの作成</span><span class="sxs-lookup"><span data-stu-id="ca332-107">Create a new online channel</span></span>
1. <span data-ttu-id="ca332-108">[小売りとコマース] > [チャンネル] > [オンライン ストア] に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca332-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="ca332-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-109">Click New.</span></span>
3. <span data-ttu-id="ca332-110">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca332-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ca332-111">[倉庫] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="ca332-112">[ストア タイムゾーン] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="ca332-113">[既定の顧客] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="ca332-114">[顧客のアドレス帳] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="ca332-115">[支払条件] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="ca332-116">[支払方法] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="ca332-117">[電子メール通知 プロファイル] フィールドで値を入力するか選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="ca332-118">[財務分析コード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ca332-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="ca332-119">[事業単位] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="ca332-120">同様に、そのほかの既定の分析コードの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="ca332-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="ca332-121">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="ca332-122">組織階層にオンライン チャンネルを追加します</span><span class="sxs-lookup"><span data-stu-id="ca332-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="ca332-123">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ca332-123">Close the page.</span></span>
2. <span data-ttu-id="ca332-124">[組織管理] > [組織] > [組織階層] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ca332-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="ca332-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ca332-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="ca332-126">[表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-126">Click View.</span></span>
5. <span data-ttu-id="ca332-127">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-127">Click Edit.</span></span>
    * <span data-ttu-id="ca332-128">新しいチャンネルを挿入する階層ノードを選択できます。</span><span class="sxs-lookup"><span data-stu-id="ca332-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="ca332-129">[挿入] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-129">Click Insert.</span></span>
7. <span data-ttu-id="ca332-130">[小売チャンネル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-130">Click Retail channel.</span></span>
8. <span data-ttu-id="ca332-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-131">Click OK.</span></span>
9. <span data-ttu-id="ca332-132">[発行] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="ca332-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="ca332-133">[有効日] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="ca332-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="ca332-134">[発行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ca332-134">Click Publish.</span></span>


