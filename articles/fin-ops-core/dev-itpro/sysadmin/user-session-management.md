---
title: ユーザー セッション管理
description: ユーザー セッション設定は、ユーザーのセッションが期限切れになるまでにユーザーがサインインできる時間を表します。
author: paulliew
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: paulliew
ms.search.validFrom: 2020-11-30
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: bcaae66509b7126d744416fc9e1c0d714b62a5b3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745729"
---
# <a name="user-session-management"></a><span data-ttu-id="ff486-103">ユーザー セッション管理</span><span class="sxs-lookup"><span data-stu-id="ff486-103">User session management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ff486-104">ユーザー セッション設定は、ユーザーのセッションが期限切れになるまでにユーザーがサインインできる時間を表します。</span><span class="sxs-lookup"><span data-stu-id="ff486-104">The user session setting represents the amount of time a user can be signed in before the user’s session expires.</span></span> <span data-ttu-id="ff486-105">ユーザーのセッションが期限切れになった後、ユーザーは資格情報を使用してサインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff486-105">After the user’s session expires, the user is required to sign in with their credentials.</span></span>

<span data-ttu-id="ff486-106">**セッション最大長** は最大 2,160 時間 (90 日間) で、最短 1 時間です。</span><span class="sxs-lookup"><span data-stu-id="ff486-106">The **Maximum session length** can be up to 2,160 hours (90 days), with a minimum of 1 hour.</span></span>  

> [!NOTE] 
> <span data-ttu-id="ff486-107">この機能は、バージョン 10.0.16 の時点のパブリック プレビューで利用できます。</span><span class="sxs-lookup"><span data-stu-id="ff486-107">This feature is available in public preview as of version 10.0.16.</span></span> <span data-ttu-id="ff486-108">この機能を有効にするには、機能の管理ページに移動して、**(プレビュー) ユーザー用のセッション管理の有効化** 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ff486-108">To enable this feature, go to the Feature management page and enable the **(Preview) Enable session management for users** feature.</span></span> 

<span data-ttu-id="ff486-109">セッションの最大長を変更するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ff486-109">To change the maximum session length, follow these steps:</span></span> 

1. <span data-ttu-id="ff486-110"> *\*システム管理 > ユーザー > ユーザーセッション管理** に移動します。</span><span class="sxs-lookup"><span data-stu-id="ff486-110">Go to **System administration > Users > User session management**.</span></span> 
2. <span data-ttu-id="ff486-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-111">Select **New**.</span></span>  
3. <span data-ttu-id="ff486-112">新しい行で、**ユーザー ID** フィールドのドロップダウン メニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-112">In the new row, select the drop-down menu in the **User ID** field.</span></span>  
4. <span data-ttu-id="ff486-113">ユーザー リストからユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-113">In the user list, select a user.</span></span> 
5. <span data-ttu-id="ff486-114">**セッションの最大長 (時間)** に、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff486-114">In **Maximum session length (hours)**, enter a value.</span></span> 
6. <span data-ttu-id="ff486-115">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-115">Select **Save**.</span></span> 

<span data-ttu-id="ff486-116">ユーザーのセッション最大長を更新するには:</span><span class="sxs-lookup"><span data-stu-id="ff486-116">To update the user’s maximum session length:</span></span> 

1. <span data-ttu-id="ff486-117">行を選択して、更新するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-117">Select the user that you want to update by selecting the row.</span></span> 
2. <span data-ttu-id="ff486-118">**セッションの最大長 (時間)** に、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff486-118">In **Maximum session length (hours)**, enter a value.</span></span> 
3. <span data-ttu-id="ff486-119">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-119">Select **Save**.</span></span> 

<span data-ttu-id="ff486-120">ユーザーのセッション最大長を削除し、別のユーザーのセッションと置き換えるには:</span><span class="sxs-lookup"><span data-stu-id="ff486-120">To delete a user’s maximum session length and replace it with another user’s session:</span></span> 

1. <span data-ttu-id="ff486-121">行を選択して、削除するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-121">Select the user that you want to delete by selecting the row.</span></span> 
2. <span data-ttu-id="ff486-122">**ユーザー ID** フィールドで、ドロップダウン メニューを選択して、別のユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-122">In the **User ID** field, select the drop-down menu and select another user.</span></span> 
3. <span data-ttu-id="ff486-123">**セッションの最大長 (時間)** 列に、1 時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="ff486-123">In the **Maximum session length (hours)** column, enter an hour.</span></span> 
4. <span data-ttu-id="ff486-124">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-124">Select **Save**.</span></span> 
 
<span data-ttu-id="ff486-125">ユーザーのセッション最大長を削除するには:</span><span class="sxs-lookup"><span data-stu-id="ff486-125">To delete the user’s maximum session length:</span></span> 

1. <span data-ttu-id="ff486-126">行を選択して、削除するユーザーを選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-126">Select the user that you want to delete by selecting the row.</span></span> 
2. <span data-ttu-id="ff486-127">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-127">Select **Delete**.</span></span>

<span data-ttu-id="ff486-128">ユーザーのセッション最大長を削除するには:</span><span class="sxs-lookup"><span data-stu-id="ff486-128">To delete the multiple users’ maximum session length:</span></span> 

1. <span data-ttu-id="ff486-129">削除する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-129">Select the rows that you want to delete.</span></span> 
2. <span data-ttu-id="ff486-130">**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ff486-130">Select **Delete**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]