---
title: Azure Active Directory からユーザーをインポートする
description: システム管理者はこの手順を使用して、選択したユーザーを手動でインポートするか、Azure Active Directory から多数のユーザーをインポートすることができます。
author: peakerbl
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0c2600ad8f441e6b73b143c27afa08ad0a5c2748
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5571008"
---
# <a name="import-users-from-azure-active-directory"></a><span data-ttu-id="05da6-103">Azure Active Directory からユーザーをインポートする</span><span class="sxs-lookup"><span data-stu-id="05da6-103">Import users from Azure Active Directory</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a><span data-ttu-id="05da6-104">選択したユーザーのインポート</span><span class="sxs-lookup"><span data-stu-id="05da6-104">Import select users</span></span>

<span data-ttu-id="05da6-105">システム管理者はこの手順を使用して、Azure Active Directory (Azure AD) から選択したユーザーをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="05da6-105">This procedure can be used by system administrators to import select users from Azure Active Directory (Azure AD).</span></span>

1. <span data-ttu-id="05da6-106">ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="05da6-106">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="05da6-107">ユーザーをインポートする前に、現在の会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="05da6-107">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="05da6-108">**システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05da6-108">Go to **System administration > Users > User** s.</span></span>
3. <span data-ttu-id="05da6-109">**ユーザーのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05da6-109">Click **Import users**.</span></span>
4. <span data-ttu-id="05da6-110">インポートするユーザーを選択し、**ユーザーのインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-110">Select the users that should be imported and select **Import users**.</span></span>

<span data-ttu-id="05da6-111">インポートが完了したら、ユーザーにロールを割り当てるために必要になります。</span><span class="sxs-lookup"><span data-stu-id="05da6-111">After import is completed it will be required to assign roles to users.</span></span>

## <a name="import-users-in-bulk"></a><span data-ttu-id="05da6-112">ユーザーの一括インポート</span><span class="sxs-lookup"><span data-stu-id="05da6-112">Import users in bulk</span></span>

<span data-ttu-id="05da6-113">システム管理者はこの手順を使用して、Azure Active Directory から多数のユーザーをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="05da6-113">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>
<span data-ttu-id="05da6-114">バッチ インポート オプションを使用する場合は、ユーザーを選択できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="05da6-114">Note that it is not possible to select users when using the Batch import option.</span></span>

## <a name="run-the-import-as-a-batch-job"></a><span data-ttu-id="05da6-115">バッチ ジョブとしてインポート処理を実行する</span><span class="sxs-lookup"><span data-stu-id="05da6-115">Run the import as a batch job</span></span>
1. <span data-ttu-id="05da6-116">ユーザーは、既定の会社として現在のセッション会社と共にインポートされます。</span><span class="sxs-lookup"><span data-stu-id="05da6-116">User will be imported with the current session company as their default company.</span></span> <span data-ttu-id="05da6-117">ユーザーをインポートする前に、現在の会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="05da6-117">Change current company if applicable before importing users.</span></span>
2. <span data-ttu-id="05da6-118">**システム管理 > ユーザー > ユーザー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="05da6-118">Go to **System administration > Users > Users**.</span></span>
3. <span data-ttu-id="05da6-119">**バッチ インポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05da6-119">Click **Batch import**.</span></span>
4. <span data-ttu-id="05da6-120">**バックグラウンドで実行** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="05da6-120">Expand the **Run in the background** section.</span></span>
4. <span data-ttu-id="05da6-121">**バッチ処理** フィールドで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-121">Select **Yes** in the **Batch processing** field.</span></span>
6. <span data-ttu-id="05da6-122">**バッチ グループ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-122">In the **Batch group** field, enter or select a value.</span></span> <span data-ttu-id="05da6-123">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="05da6-123">This is an optional step.</span></span>  
7. <span data-ttu-id="05da6-124">**個人** フィールドでは、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-124">Select **Yes** in the **Private** field.</span></span> <span data-ttu-id="05da6-125">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="05da6-125">This is an optional step.</span></span>  
8. <span data-ttu-id="05da6-126">**重要なジョブ** フィールドでは、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-126">Select **Yes** in the **Critical job** field.</span></span> <span data-ttu-id="05da6-127">これは、オプションのステップです。</span><span class="sxs-lookup"><span data-stu-id="05da6-127">This is an optional step.</span></span>  
9. <span data-ttu-id="05da6-128">**監視カテゴリ** フィールドでは、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-128">In the **Monitoring category** field, select an option.</span></span>
10. <span data-ttu-id="05da6-129">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="05da6-129">Click **OK**.</span></span>

<span data-ttu-id="05da6-130">インポートが完了したら、ユーザーにロールを割り当てるために必要になります。</span><span class="sxs-lookup"><span data-stu-id="05da6-130">After import is completed, it will be required to assign roles to users.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="05da6-131">サンドボックス環境で実行</span><span class="sxs-lookup"><span data-stu-id="05da6-131">Run in a sandbox environment</span></span>
1. <span data-ttu-id="05da6-132">**バッチインポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-132">Select **Batch import**.</span></span>
2. <span data-ttu-id="05da6-133">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="05da6-133">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]