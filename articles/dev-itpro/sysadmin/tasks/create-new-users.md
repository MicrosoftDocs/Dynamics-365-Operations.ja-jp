--- 
title: "新規ユーザーの作成"
description: "ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。"
author: maertenm
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ed320111f3be9a496c54c1ff038179fdbbab5246
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-new-users"></a><span data-ttu-id="5e3b5-103">新規ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="5e3b5-103">Create new users</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5e3b5-104">ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="5e3b5-105">システム管理者は、この手順を実行してシステムにユーザーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="5e3b5-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="5e3b5-107">新しいユーザーを追加する</span><span class="sxs-lookup"><span data-stu-id="5e3b5-107">Add a new user</span></span>
1. <span data-ttu-id="5e3b5-108">[システム管理] > [ユーザー] > [ユーザー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="5e3b5-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-109">Click New.</span></span>
3. <span data-ttu-id="5e3b5-110">[ユーザー ID] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="5e3b5-111">ユーザーを示す固有の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="5e3b5-112">ユーザー ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-112">A user ID is required.</span></span>  
4. <span data-ttu-id="5e3b5-113">[ユーザー名] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="5e3b5-114">ユーザーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="5e3b5-115">[ドメイン] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="5e3b5-116">ユーザーのドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="5e3b5-117">[エイリアス] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="5e3b5-118">ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="5e3b5-119">[会社] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="5e3b5-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="5e3b5-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5e3b5-122">ユーザーの会社の選択</span><span class="sxs-lookup"><span data-stu-id="5e3b5-122">Select the user's company</span></span>  
10. <span data-ttu-id="5e3b5-123">[ロールの割り当て] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-123">Click Assign roles.</span></span>
11. <span data-ttu-id="5e3b5-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5e3b5-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-125">Click OK.</span></span>
13. <span data-ttu-id="5e3b5-126">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="5e3b5-127">ユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="5e3b5-127">Import users</span></span>
1. <span data-ttu-id="5e3b5-128">[ユーザーのインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-128">Click Import users.</span></span>
2. <span data-ttu-id="5e3b5-129">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5e3b5-130">[ユーザーのインポート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-130">Click Import users.</span></span>
4. <span data-ttu-id="5e3b5-131">[閉じる] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e3b5-131">Click Close.</span></span>


