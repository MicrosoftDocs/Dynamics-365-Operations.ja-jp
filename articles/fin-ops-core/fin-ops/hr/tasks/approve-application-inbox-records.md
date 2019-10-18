---
title: 申請受信トレイ レコードの承認
description: この手順は、従業員セルフサービス ページを通して受け取った申請を確認する方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMApplicationBasket, HRMApplicationBasketApprove, HRMApplication
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28a82ea8747fcbbceb835291ad5cd3d87091a736
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190698"
---
# <a name="approve-application-inbox-records"></a><span data-ttu-id="fd853-103">申請受信トレイ レコードの承認</span><span class="sxs-lookup"><span data-stu-id="fd853-103">Approve application inbox records</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd853-104">この手順は、従業員セルフサービス ページを通して受け取った申請を確認する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fd853-104">This procedure shows how to review applications received through the Employee self-service pages.</span></span> <span data-ttu-id="fd853-105">申請の確認に加えて、選択した申請受信トレイ レコードを承認できます。</span><span class="sxs-lookup"><span data-stu-id="fd853-105">In addition to reviewing the applications, you can approve the application in box records that you select.</span></span> <span data-ttu-id="fd853-106">申請受信トレイ レコードは、採用審査のために会社に提出された雇用申請を表します。</span><span class="sxs-lookup"><span data-stu-id="fd853-106">Application inbox records represent employment applications that were submitted to the company for consideration.</span></span> <span data-ttu-id="fd853-107">レコードが承認されると、申請者レコードは、申請を提出したユーザー用に作成されます。</span><span class="sxs-lookup"><span data-stu-id="fd853-107">After approving a record, an applicant record will be created for the person who submitted the application.</span></span> <span data-ttu-id="fd853-108">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="fd853-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="review-application-inbox-record"></a><span data-ttu-id="fd853-109">申請受信トレイ レコードを確認します</span><span class="sxs-lookup"><span data-stu-id="fd853-109">Review application inbox record</span></span>
1. <span data-ttu-id="fd853-110">[人事管理] > [採用] > [申請] > [申請受信トレイ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd853-110">Go to Human resources > Recruitment > Applications > Application inbox.</span></span>
2. <span data-ttu-id="fd853-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="fd853-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="fd853-112">[住所] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd853-112">Expand the Addresses section.</span></span>
4. <span data-ttu-id="fd853-113">[連絡先情報] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd853-113">Expand the Contact information section.</span></span>
5. <span data-ttu-id="fd853-114">[添付ファイル] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd853-114">Expand the Attachments section.</span></span>

## <a name="approve-application-inbox-record"></a><span data-ttu-id="fd853-115">申請受信トレイ レコードを承認します</span><span class="sxs-lookup"><span data-stu-id="fd853-115">Approve application inbox record</span></span>
1. <span data-ttu-id="fd853-116">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="fd853-116">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="fd853-117">後で参照するために、[名前] フィールドの値をメモする</span><span class="sxs-lookup"><span data-stu-id="fd853-117">Note the value in the Name field to reference later</span></span>
3. <span data-ttu-id="fd853-118">[承認] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd853-118">Click Approve.</span></span>
4. <span data-ttu-id="fd853-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd853-119">Click OK.</span></span>
5. <span data-ttu-id="fd853-120">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fd853-120">Close the page.</span></span>

## <a name="view-the-newly-created-application-record"></a><span data-ttu-id="fd853-121">新しく作成された申請レコードを表示します</span><span class="sxs-lookup"><span data-stu-id="fd853-121">View the newly created application record</span></span>
1. <span data-ttu-id="fd853-122">[人事管理] > [採用] > [応募] > [応募] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd853-122">Go to Human resources > Recruitment > Applications > Applications.</span></span>
2. <span data-ttu-id="fd853-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd853-123">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="fd853-124">[添付ファイル] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="fd853-124">Expand the Attachments section.</span></span>
