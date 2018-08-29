--- 
title: "コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="f9d27-103">コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け</span><span class="sxs-lookup"><span data-stu-id="f9d27-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9d27-104">次の手順では、システム管理者または電子レポート開発者に割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f9d27-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="f9d27-105">各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。</span><span class="sxs-lookup"><span data-stu-id="f9d27-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="f9d27-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="f9d27-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="f9d27-107">プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="f9d27-107">Create a provider</span></span>
1. <span data-ttu-id="f9d27-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="f9d27-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="f9d27-109">[コンフィギュレーション プロバイダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9d27-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="f9d27-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9d27-110">Click New.</span></span>
    * <span data-ttu-id="f9d27-111">プロバイダー レコードには固有の名称とURL があります。</span><span class="sxs-lookup"><span data-stu-id="f9d27-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="f9d27-112">このページの内容を確認し、Litware, Inc. (`http://www.litware.com`) の記録が既に存在している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="f9d27-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="f9d27-113">[名前] フィールドに「Litware, Inc.」を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9d27-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="f9d27-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="f9d27-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="f9d27-115">[インターネット アドレス] フィールドに `http://www.litware.com`を入力します。</span><span class="sxs-lookup"><span data-stu-id="f9d27-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="f9d27-116">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9d27-116">Click Save.</span></span>
7. <span data-ttu-id="f9d27-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f9d27-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="f9d27-118">有効なプロバイダーとして選択する</span><span class="sxs-lookup"><span data-stu-id="f9d27-118">Select as an active provider</span></span>
1. <span data-ttu-id="f9d27-119">Litware, Inc. を選択して プロバイダー</span><span class="sxs-lookup"><span data-stu-id="f9d27-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="f9d27-120">[有効に設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f9d27-120">Click Set active.</span></span>


