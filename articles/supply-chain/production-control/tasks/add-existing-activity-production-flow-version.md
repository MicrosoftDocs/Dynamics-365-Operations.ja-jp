--- 
title: "生産フロー バージョンへの既存の活動の追加"
description: "生産フローの新バージョンを作成する際に、旧バージョン向けに作成された活動を新バージョンに加えることができます。"
author: cvocph
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a04535fcd2bf4141268145e5658c22815c624681
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="add-an-existing-activity-to-a-production-flow-version"></a><span data-ttu-id="72ec1-103">生産フロー バージョンへの既存の活動の追加</span><span class="sxs-lookup"><span data-stu-id="72ec1-103">Add an existing activity to a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="72ec1-104">生産フローの新バージョンを作成する際に、旧バージョン向けに作成された活動を新バージョンに加えることができます。</span><span class="sxs-lookup"><span data-stu-id="72ec1-104">When creating new versions of production flows, you can choose to add activities created for the older versions, to the new version.</span></span> <span data-ttu-id="72ec1-105">この手順では、活動をコピーしないで既存の生産フロー向けの新バージョンの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-105">This procedure shows how a new version is created for an existing production flow, without copying the activities.</span></span> <span data-ttu-id="72ec1-106">次の手順では、既存の活動が新バージョンに追加されます。</span><span class="sxs-lookup"><span data-stu-id="72ec1-106">In the next step, an existing activity is added to the new version.</span></span> 

<span data-ttu-id="72ec1-107">この作業には、既に作成されたバージョンおよび活動を含む生産フローが必要です。</span><span class="sxs-lookup"><span data-stu-id="72ec1-107">This task requires production flow with version and activities already created.</span></span>


## <a name="create-a-new-production-flow-version"></a><span data-ttu-id="72ec1-108">新しい生産フロー バージョンの作成</span><span class="sxs-lookup"><span data-stu-id="72ec1-108">Create a new production flow version</span></span>
1. <span data-ttu-id="72ec1-109">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="72ec1-110">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="72ec1-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="72ec1-112">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-112">Click Edit.</span></span>
5. <span data-ttu-id="72ec1-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-113">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="72ec1-114">[有効期限] フィールドに日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-114">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="72ec1-115">新規生産フロー バージョンを作成する前に、有効なバージョンの期限切れの日時をチェックすることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72ec1-115">Note that before you create a new production flow version, make sure to check the expiration date and time of the active version.</span></span> <span data-ttu-id="72ec1-116">新規バージョンは有効な開始日（バージョン終了日の翌日）で作成します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-116">The new version will be created with an effective start date, which connects to the expiry date of the selected version.</span></span>  
7. <span data-ttu-id="72ec1-117">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-117">Click Add.</span></span>
8. <span data-ttu-id="72ec1-118">[バージョンからのコピー] フィールドで、「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-118">Select No in the Copy from version field.</span></span>
    * <span data-ttu-id="72ec1-119">コピーしたバージョンの活動の大半が新しい活動と交換された場合、[空のバージョンで開始する] に「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-119">Select No to start with an empty version if most of the activities of the copied version will be replaced by new activities.</span></span> <span data-ttu-id="72ec1-120">変更のない活動を、手動で「活動形式における既存機能に加える」に加えます。</span><span class="sxs-lookup"><span data-stu-id="72ec1-120">Add the unchanged activities to the Add existing function in the activity form manually.</span></span>  
9. <span data-ttu-id="72ec1-121">[重複するかんばんルール] フィールドで、「いいえ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-121">Select No in the Duplicate kanban rules field.</span></span>
    * <span data-ttu-id="72ec1-122">活動が新しいバージョンにコピーされていない場合、新しいバージョンの作成時にかんばんルールをコピーすることはできません。</span><span class="sxs-lookup"><span data-stu-id="72ec1-122">When the activities are not copied to the new version, it is not possible to copy the kanban rules at the time of creation of the new version.</span></span>   <span data-ttu-id="72ec1-123">代わりに、旧生産フローバージョンのかんばんルールを新規バージョンの活動を使用するかんばんルールと交換するために、交換かんばん機能かんばんルール形式で作成します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-123">Instead you will use the create replacement kanban function later in the kanban rule form, to replace kanban rules of the old production flow version with kanban rules using the activities of the new version.</span></span>  
10. <span data-ttu-id="72ec1-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-124">Click OK.</span></span>
11. <span data-ttu-id="72ec1-125">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-125">In the list, find and select the desired record.</span></span>

## <a name="add-an-existing-activity"></a><span data-ttu-id="72ec1-126">既存の活動を追加する</span><span class="sxs-lookup"><span data-stu-id="72ec1-126">Add an existing activity</span></span>
1. <span data-ttu-id="72ec1-127">[活動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-127">Click Activities.</span></span>
2. <span data-ttu-id="72ec1-128">[既存を追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="72ec1-128">Click Add existing to open the drop dialog.</span></span>
    * <span data-ttu-id="72ec1-129">新規生産フロー バージョンに追加される既存の活動を検索、選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-129">Find and select an existing activity to be added to the new production flow version.</span></span>  <span data-ttu-id="72ec1-130">リストは、フローの以前のバージョンに代わるこの生産フローのために作成されたすべての活動を示すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72ec1-130">Note that the list shows all activities that have been created for this production flow for all previous versions of the flow.</span></span>  
3. <span data-ttu-id="72ec1-131">[活動] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="72ec1-131">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="72ec1-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72ec1-132">Click OK.</span></span>


