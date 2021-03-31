---
title: POS アクセス許可グループの作成
description: このトピックでは、POS アクセス許可グループの作成方法を説明します。
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2439d1912b3ca013f4a524f3354923d2a3f76ca
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221284"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="a5ef9-103">POS アクセス許可グループの作成</span><span class="sxs-lookup"><span data-stu-id="a5ef9-103">Create POS permission groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5ef9-104">このトピックでは、POS アクセス許可グループの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="a5ef9-105">このタスクの作成に使用するデモ データの会社は USRT です。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="a5ef9-106">このタスクは、Commerce 工程マネージャー ロールを対象としています。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="a5ef9-107">ナビゲーション ウィンドウで、**モジュール > Retail と Commerce > 従業員 > アクセス許可グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="a5ef9-108">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-108">Select **New**.</span></span>
3. <span data-ttu-id="a5ef9-109">**POS アクセス許可グループ ID** フィールドに、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="a5ef9-110">**説明** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="a5ef9-111">**タイム レコーダー エントリの表示** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="a5ef9-112">これで、POS アクセス許可グループのさまざまなアクセス許可を有効、または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="a5ef9-113">複数のアクセス許可に対して、POS ユーザーが操作を実行することができるかどうか評価するために使用する値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="a5ef9-114">このタスク ガイドは、レジ担当者に支給される可能性があるいくつかのアクセス許可を有効にします。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="a5ef9-115">**注文の作成を許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="a5ef9-116">**注文の編集を許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="a5ef9-117">**注文の取得を許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="a5ef9-118">**パスワードの変更を許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="a5ef9-119">**ブラインド クローズを許可** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="a5ef9-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-120">Select **Save**.</span></span> <span data-ttu-id="a5ef9-121">変更が保存された後、Commerce チャネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="a5ef9-122">ナビゲーション ウィンドウで、**モジュール > 人事部 > ジョブ > ジョブ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="a5ef9-123">次に、ジョブに対して POS アクセス許可グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="a5ef9-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="a5ef9-125">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-125">Select **Edit**.</span></span>
15. <span data-ttu-id="a5ef9-126">**ジョブ分類** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="a5ef9-127">[POS アクセス許可グループ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="a5ef9-128">作業者の POS アクセス許可が職位のレベルで上書きされない場合、このジョブの職位のすべての作業者は、この POS アクセス許可グループの設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-128">All Workers in Positions for this Job will use this POS permission group's settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="a5ef9-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-129">Select **Save**.</span></span> <span data-ttu-id="a5ef9-130">変更が保存された後、チャネルへ変更をプッシュするために、スタッフ配送スケジュールを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5ef9-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]