---
title: Lifecycle Services からの二重書き込みの設定
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS). からデュアル書き込み接続を設定する方法について説明します。
author: RamaKrishnamoorthy
ms.date: 05/11/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: eb4170ef6cb09c862f6a4163670c519d5d8077fb
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103572"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="dc1ce-103">Lifecycle Services からの二重書き込みの設定</span><span class="sxs-lookup"><span data-stu-id="dc1ce-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="dc1ce-104">このトピックでは、 Microsoft Dynamics Lifecycle Services (LCS)から二重書き込みを有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-104">This topic explains how to enable dual-write from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc1ce-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="dc1ce-105">Prerequisites</span></span>

<span data-ttu-id="dc1ce-106">Power Platform の統合を完了する必要があります。次のトピックを参照ください:</span><span class="sxs-lookup"><span data-stu-id="dc1ce-106">You must complete the Power Platform integration as described in the following topics:</span></span>

+ [<span data-ttu-id="dc1ce-107">Power Platform 統合: 環境のデプロイ中に有効にします</span><span class="sxs-lookup"><span data-stu-id="dc1ce-107">Power Platform Integration - Enable during environment deployment</span></span>](../../power-platform/overview.md#enable-during-environment-deployment)
+ [<span data-ttu-id="dc1ce-108">Power Platform 統合 - 環境のデプロイ後に設定します</span><span class="sxs-lookup"><span data-stu-id="dc1ce-108">Power Platform integration - Set up after environment deployment</span></span>](../../power-platform/overview.md#set-up-after-environment-deployment)

## <a name="set-up-dual-write-for-new-dataverse-environments"></a><span data-ttu-id="dc1ce-109">新しい Dataverse 環境で使用する二重書き込みの設定</span><span class="sxs-lookup"><span data-stu-id="dc1ce-109">Set up dual-write for new Dataverse environments</span></span>

<span data-ttu-id="dc1ce-110">以下の手順で、LCS  **環境の詳細** ページから二重書き込みを設定します:</span><span class="sxs-lookup"><span data-stu-id="dc1ce-110">Follow these steps to set up dual-write from LCS **Environment Details** page:</span></span>

1. <span data-ttu-id="dc1ce-111">**環境の詳細** ページで、**Power Platform の統合** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-111">On the **Environment Details** page, expand the **Power Platform Integration** section.</span></span>

2. <span data-ttu-id="dc1ce-112">**二重書き込みアプリケーション** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-112">Select the **Dual-write application** button.</span></span>

    ![Power Platform 統合](media/powerplat_integration_step2.png)

3. <span data-ttu-id="dc1ce-114">条件を確認して、**構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-114">Review the terms and conditions, and then select **Configure**.</span></span>

4. <span data-ttu-id="dc1ce-115">続行するには **OK** を選択してください。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-115">Select **OK** to continue.</span></span>

5. <span data-ttu-id="dc1ce-116">環境の詳細ページを定期的に更新することで、進捗状況を監視できます。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-116">You can monitor the progress by periodically refreshing the environment details page.</span></span> <span data-ttu-id="dc1ce-117">通常、所要時間は 30 分以下です。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-117">Setup typically takes 30 minutes or less.</span></span>  

6. <span data-ttu-id="dc1ce-118">設定が完了すると、プロセスが正常に完了した場合、または失敗した場合にメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-118">When the setup is complete, a message will inform you if the process was successful or if there was a failure.</span></span> <span data-ttu-id="dc1ce-119">設定に失敗した場合は、関連するエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-119">If the setup failed, then a related error message is displayed.</span></span> <span data-ttu-id="dc1ce-120">エラーがある場合は、修正をしないと次の手順に進めません。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-120">You must fix any errors before moving to the next step.</span></span>

7. <span data-ttu-id="dc1ce-121">**Power Platform 環境へのリンク** を選択して、Dataverse と現在の環境のデータベースとのリンクを作成します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-121">Select **Link to Power Platform environment** to create a link between Dataverse and the current environment's databases.</span></span> <span data-ttu-id="dc1ce-122">通常、所要時間は 5 分以下です。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-122">This typically takes less than 5 minutes.</span></span>

    :::image type="content" source="media/powerplat_integration_step3.png" alt-text="Power Platform 環境へのリンク":::

8. <span data-ttu-id="dc1ce-124">リンクが完了すると、ハイパーリンクが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-124">When the linking is complete, a hyperlink is displayed.</span></span> <span data-ttu-id="dc1ce-125">このリンクを使用して、Finance and Operations 環境内の二重書き込み管理領域にログインします。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-125">Use the link to sign in to the dual-write administration area in the Finance and Operations environment.</span></span> <span data-ttu-id="dc1ce-126">そこから、エンティティ マッピングを設定します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-126">From there, you can set up entity mappings.</span></span>

## <a name="set-up-dual-write-for-an-existing-dataverse-environment"></a><span data-ttu-id="dc1ce-127">既存の Dataverse 環境で使用する二重書き込みの設定</span><span class="sxs-lookup"><span data-stu-id="dc1ce-127">Set up dual-write for an existing Dataverse environment</span></span>

<span data-ttu-id="dc1ce-128">既存の Dataverse 環境に対して二重書き込みを設定するには、Microsoft の [サポート チケット](../../lifecycle-services/lcs-support.md) を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-128">To set up dual-write for an existing Dataverse environment, you must create a Microsoft [support ticket](../../lifecycle-services/lcs-support.md).</span></span> <span data-ttu-id="dc1ce-129">このチケットには次の情報が必要となります:</span><span class="sxs-lookup"><span data-stu-id="dc1ce-129">The ticket must include:</span></span>

+ <span data-ttu-id="dc1ce-130">ご利用の Finance and Operations 環境の ID。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-130">Your Finance and Operations environment ID.</span></span>
+ <span data-ttu-id="dc1ce-131">Lifecycle Services から環境名を入力します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-131">Your environment name from Lifecycle Services.</span></span>
+ <span data-ttu-id="dc1ce-132">Dataverse 管理センターの組織 ID、または Power Platform 管理センターの Power Platform環境 ID。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-132">The Dataverse organization ID or Power Platform Environment ID from Power Platform Admin Center.</span></span> <span data-ttu-id="dc1ce-133">チケットの中で、ID が Power Platform 統合で使用するインスタンスであることを要求してください。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-133">In your ticket, request that the ID be the instance used for Power Platform integration.</span></span>

> [!NOTE]
> <span data-ttu-id="dc1ce-134">LCS を使用して環境のリンクを解除することはできません。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-134">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="dc1ce-135">環境のリンクを解除するには、Finance and Operations 環境の **データ統合** ワークスペースを開き、**リンク解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dc1ce-135">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
