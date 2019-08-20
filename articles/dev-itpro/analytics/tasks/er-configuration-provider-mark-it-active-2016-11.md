---
title: コンフィギュレーション プロバイダーを作成し、有効としてマークする
description: このトピックでは、システム管理者または電子レポート開発者のロールに割り当てられたユーザーが、Dynamics 365 for Finance and Operations で電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0dfbcf70493a43320e17d4d2734fe6343d43eaf3
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850330"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="329de-103">コンフィギュレーション プロバイダーを作成し、有効としてマークする</span><span class="sxs-lookup"><span data-stu-id="329de-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="329de-104">このトピックでは、システム管理者または電子レポート開発者のロールに割り当てられたユーザーが、Dynamics 365 for Finance and Operations で電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="329de-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER) in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="329de-105">各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。</span><span class="sxs-lookup"><span data-stu-id="329de-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="329de-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="329de-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="329de-107">プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="329de-107">Create a provider</span></span>
1. <span data-ttu-id="329de-108">左上隅の**ナビゲーション ウィンドウ**に移動して、**組織管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="329de-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="329de-109">**ワークスペース > 電子申告**に移動します。</span><span class="sxs-lookup"><span data-stu-id="329de-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="329de-110">**関連リンク > コンフィギュレーション プロバイダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="329de-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="329de-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="329de-111">Select **New**.</span></span>
    - <span data-ttu-id="329de-112">プロバイダー レコードには固有の名称とURL があります。</span><span class="sxs-lookup"><span data-stu-id="329de-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="329de-113">このページの内容を確認し、Litware, Inc. (https://www.litware.com) の記録が既に存在している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="329de-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="329de-114">名前フィールドに、`Litware, Inc.` と入力します。</span><span class="sxs-lookup"><span data-stu-id="329de-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="329de-115">インターネット アドレス フィールドに `https://www.litware.com` と入力します。</span><span class="sxs-lookup"><span data-stu-id="329de-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="329de-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="329de-116">Select **Save**.</span></span>
8. <span data-ttu-id="329de-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="329de-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="329de-118">有効なプロバイダーとして選択する</span><span class="sxs-lookup"><span data-stu-id="329de-118">Select as an active provider</span></span>
1. <span data-ttu-id="329de-119">Litware, Inc. を選択して プロバイダー</span><span class="sxs-lookup"><span data-stu-id="329de-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="329de-120">**有効に設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="329de-120">Select **Set active**.</span></span>

