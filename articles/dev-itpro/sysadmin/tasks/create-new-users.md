---
title: 新規ユーザーの作成
description: ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916487"
---
# <a name="create-new-users"></a><span data-ttu-id="090b1-103">新規ユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="090b1-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="090b1-104">ユーザーは、ジョブの実行のためにシステムへアクセスする必要がある、組織の内部従業員、または外部顧客や仕入先です。</span><span class="sxs-lookup"><span data-stu-id="090b1-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="090b1-105">システム管理者は、この手順を実行してシステムにユーザーを追加できます。</span><span class="sxs-lookup"><span data-stu-id="090b1-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="090b1-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="090b1-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="090b1-107">新しいユーザーを追加する</span><span class="sxs-lookup"><span data-stu-id="090b1-107">Add a new user</span></span>
1. <span data-ttu-id="090b1-108">**ナビゲーション ウィンドウ > モジュール > システム管理 > ユーザー > ユーザー**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="090b1-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="090b1-109">**アクション ウィンドウ**で、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="090b1-110">**ユーザー ID** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="090b1-111">ユーザーを示す固有の ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="090b1-112">ユーザー ID が必要です。</span><span class="sxs-lookup"><span data-stu-id="090b1-112">A user ID is required.</span></span>  
4. <span data-ttu-id="090b1-113">**ユーザー名**フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="090b1-114">ユーザーの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="090b1-115">**ドメイン** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="090b1-116">ユーザーのドメインを入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="090b1-117">**エイリアス** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="090b1-118">ユーザーのエイリアスを入力します。</span><span class="sxs-lookup"><span data-stu-id="090b1-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="090b1-119">**会社**フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="090b1-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="090b1-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="090b1-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="090b1-121">**ユーザーのロール** セクションで、**ロールの割り当て**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="090b1-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="090b1-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="090b1-123">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-123">Click **OK**.</span></span>
12. <span data-ttu-id="090b1-124">**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="090b1-125">ユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="090b1-125">Import users</span></span>
1. <span data-ttu-id="090b1-126">**アクション ウィンドウ**で、**ユーザーのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="090b1-127">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="090b1-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="090b1-128">**ユーザーのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-128">Click **Import users**.</span></span>
4. <span data-ttu-id="090b1-129">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="090b1-129">Click **Close**.</span></span>

