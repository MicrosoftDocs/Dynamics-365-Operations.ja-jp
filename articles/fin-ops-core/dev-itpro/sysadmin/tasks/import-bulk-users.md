---
title: Azure Active Directory からユーザーをインポートする
description: システム管理者はこの手順を使用して、選択したユーザーを手動でインポートするか、Azure Active Directory から多数のユーザーをインポートすることができます。
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 56b6666310309817ff30ccb3902721880b829ee0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679817"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="3efc9-103">Azure Active Directory からユーザーをインポートする</span><span class="sxs-lookup"><span data-stu-id="3efc9-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="3efc9-104">選択したユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="3efc9-104">Import select users</span></span>

<span data-ttu-id="3efc9-105">システム管理者はこの手順を使用して、Azure Active Directory (Azure AD) から選択したユーザーをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3efc9-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="3efc9-106">ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="3efc9-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3efc9-107">ユーザーをインポートする前に、現在の会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3efc9-108">**システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="3efc9-109">**ユーザーのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3efc9-109">Click **Import users**.</span></span>
4. <span data-ttu-id="3efc9-110">インポートするユーザーを選択し、**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="3efc9-111">インポートが完了したら、ユーザーにロールを割り当てるために必要になります。</span><span class="sxs-lookup"><span data-stu-id="3efc9-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="3efc9-112">ユーザーの一括インポート</span><span class="sxs-lookup"><span data-stu-id="3efc9-112">Import users in bulk</span></span>

<span data-ttu-id="3efc9-113">システム管理者はこの手順を使用して、Azure Active Directory から多数のユーザーをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="3efc9-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="3efc9-114">バッチ インポート オプションを使用する場合は、ユーザーを選択できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="3efc9-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="3efc9-115">バッチ ジョブとしてインポート処理を実行する</span><span class="sxs-lookup"><span data-stu-id="3efc9-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="3efc9-116">ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="3efc9-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="3efc9-117">ユーザーをインポートする前に、現在の会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="3efc9-118">**システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="3efc9-119">**バッチ インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3efc9-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="3efc9-120">**バックグラウンドで実行** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="3efc9-121">**バッチ処理** フィールドで \*\*はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-121">Select \*\*Yes in the **Batch processing** field.</span></span>
6. <span data-ttu-id="3efc9-122">**バッチ グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="3efc9-123">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="3efc9-123">This is an optional step.</span></span>  
7. <span data-ttu-id="3efc9-124">**個人** フィールドでは、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="3efc9-125">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="3efc9-125">This is an optional step.</span></span>  
8. <span data-ttu-id="3efc9-126">**重要なジョブ** フィールドでは、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="3efc9-127">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="3efc9-127">bThis is an optional step.</span></span>  
9. <span data-ttu-id="3efc9-128">**監視カテゴリ** フィールドでは、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-128">In the \*\*Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="3efc9-129">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3efc9-129">Click **OK**.</span></span>

<span data-ttu-id="3efc9-130">インポートが完了したら、ユーザーにロールを割り当てるために必要になります。</span><span class="sxs-lookup"><span data-stu-id="3efc9-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="3efc9-131">サンドボックス環境で実行</span><span class="sxs-lookup"><span data-stu-id="3efc9-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="3efc9-132">**バッチインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="3efc9-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3efc9-133">Select **OK**.</span></span>
