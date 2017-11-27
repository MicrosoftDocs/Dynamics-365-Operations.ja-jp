--- 
title: "コンフィギュレーション プロバイダーを作成し、電子申告 (ER) が有効なプロバイダーとしてマーク付けする"
description: "次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 809a1466b0f4674f503bc654175d8f94b37a6508
ms.openlocfilehash: 2dfa04f280249884af2a237807fb283059444a6c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/02/2017

---
# <a name="create-a-configuration-provider-and-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="28d95-103">コンフィギュレーション プロバイダーを作成し、電子申告 (ER) が有効なプロバイダーとしてマーク付けする</span><span class="sxs-lookup"><span data-stu-id="28d95-103">Create a configuration provider and mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28d95-104">次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="28d95-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="28d95-105">各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。</span><span class="sxs-lookup"><span data-stu-id="28d95-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="28d95-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="28d95-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="28d95-107">プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="28d95-107">Create a provider</span></span>
1. <span data-ttu-id="28d95-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="28d95-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="28d95-109">[コンフィギュレーション プロバイダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d95-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="28d95-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d95-110">Click New.</span></span>
    * <span data-ttu-id="28d95-111">プロバイダー レコードには固有の名称とURL があります。</span><span class="sxs-lookup"><span data-stu-id="28d95-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="28d95-112">このページの内容を確認し、Litware, Inc. (http://www.litware.com) のレコードがすでに存在する場合、この手順をスキップします。</span><span class="sxs-lookup"><span data-stu-id="28d95-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="28d95-113">[名前] フィールドに「Litware, Inc.」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d95-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="28d95-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="28d95-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="28d95-115">[インターネット アドレス] フィールドに「http://www.litware.com」を入力します。</span><span class="sxs-lookup"><span data-stu-id="28d95-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="28d95-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="28d95-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="28d95-117">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d95-117">Click Save.</span></span>
7. <span data-ttu-id="28d95-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28d95-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="28d95-119">有効なプロバイダーとして選択する</span><span class="sxs-lookup"><span data-stu-id="28d95-119">Select as an active provider</span></span>
1. <span data-ttu-id="28d95-120">Litware, Inc. を選択して プロバイダー</span><span class="sxs-lookup"><span data-stu-id="28d95-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="28d95-121">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="28d95-121">Click Set active.</span></span>


