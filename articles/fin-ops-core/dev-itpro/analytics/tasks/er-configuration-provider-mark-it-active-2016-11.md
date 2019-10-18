---
title: コンフィギュレーション プロバイダーを作成し、有効としてマークする
description: このトピックでは、システム管理者または電子レポート開発者のロールに割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法について説明します。
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
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249207"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="07f29-103">コンフィギュレーション プロバイダーを作成し、有効としてマークする</span><span class="sxs-lookup"><span data-stu-id="07f29-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="07f29-104">このトピックでは、システム管理者または電子レポート開発者のロールに割り当てられたユーザーが、電子レポート (ER) のコンフィギュレーション プロバイダーを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="07f29-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="07f29-105">各 ER コンフィギュレーションは、コンフィギュレーションの作成者としてプロバイダーを参照するようになります。</span><span class="sxs-lookup"><span data-stu-id="07f29-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="07f29-106">この例では、サンプル会社 Litware, Inc. のコンフィギュレーションを作成します。ER コンフィギュレーションはすべての会社間で共有されるため、これらの手順はすべての会社で実行されます。</span><span class="sxs-lookup"><span data-stu-id="07f29-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="07f29-107">プロバイダーの作成</span><span class="sxs-lookup"><span data-stu-id="07f29-107">Create a provider</span></span>
1. <span data-ttu-id="07f29-108">左上隅の**ナビゲーション ウィンドウ**に移動して、**組織管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="07f29-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="07f29-109">**ワークスペース > 電子申告**に移動します。</span><span class="sxs-lookup"><span data-stu-id="07f29-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="07f29-110">**関連リンク > コンフィギュレーション プロバイダー**に移動します。</span><span class="sxs-lookup"><span data-stu-id="07f29-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="07f29-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07f29-111">Select **New**.</span></span>
    - <span data-ttu-id="07f29-112">プロバイダー レコードには固有の名称とURL があります。</span><span class="sxs-lookup"><span data-stu-id="07f29-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="07f29-113">このページの内容を確認し、Litware, Inc. (https://www.litware.com) の記録が既に存在している場合、この手順を省略します。</span><span class="sxs-lookup"><span data-stu-id="07f29-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="07f29-114">名前フィールドに、`Litware, Inc.` と入力します。</span><span class="sxs-lookup"><span data-stu-id="07f29-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="07f29-115">インターネット アドレス フィールドに `https://www.litware.com` と入力します。</span><span class="sxs-lookup"><span data-stu-id="07f29-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="07f29-116">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="07f29-116">Select **Save**.</span></span>
8. <span data-ttu-id="07f29-117">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="07f29-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="07f29-118">有効なプロバイダーとして選択する</span><span class="sxs-lookup"><span data-stu-id="07f29-118">Select as an active provider</span></span>
1. <span data-ttu-id="07f29-119">Litware, Inc. を選択して プロバイダー</span><span class="sxs-lookup"><span data-stu-id="07f29-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="07f29-120">**有効に設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="07f29-120">Select **Set active**.</span></span>

![電子申告ワークスペース ページ](../media/GER-Task-ActiveProvider-1.png)