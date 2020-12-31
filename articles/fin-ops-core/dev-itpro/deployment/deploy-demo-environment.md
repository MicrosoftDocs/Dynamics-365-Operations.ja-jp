---
title: デモ環境の配置
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。 これは Dynamics 365 Finance、Supply Chain Management、およびコマースに適用されます。
author: sarvanisathish
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: 3015dc5a904774a4d19c46fd72f32b00280e477b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680544"
---
# <a name="deploy-a-demo-environment"></a><span data-ttu-id="62300-104">デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="62300-104">Deploy a demo environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="62300-105">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="62300-105">This topic explains how to deploy a demo environment on Microsoft Azure using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="62300-106">このトピックは、以下のデモ環境の配置に適用されます。</span><span class="sxs-lookup"><span data-stu-id="62300-106">This topic applies to deploying a demo environment for:</span></span>

- <span data-ttu-id="62300-107">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="62300-107">Dynamics 365 Finance</span></span>
- <span data-ttu-id="62300-108">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="62300-108">Dynamics 365 Supply Chain Management</span></span>
- <span data-ttu-id="62300-109">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="62300-109">Dynamics 365 Commerce</span></span>

## <a name="prerequisites"></a><span data-ttu-id="62300-110">必要条件</span><span class="sxs-lookup"><span data-stu-id="62300-110">Prerequisites</span></span>
<span data-ttu-id="62300-111">展開を開始する前に、次の前提条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62300-111">Before you begin your deployment, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="62300-112">Azure サブスクリプションがあり、そのサブスクリプションの共同管理者であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62300-112">Verify that you have an Azure subscription, and that you are a co-administrator on it.</span></span>
- <span data-ttu-id="62300-113">LCS プロジェクトへのアクセスが可能であり、環境を展開するためのアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62300-113">Verify that you have access to an LCS project and permissions to deploy an environment.</span></span>
- <span data-ttu-id="62300-114">[Azure Resource Managerr (ARM) オンボード プロセス を完了する](arm-onboarding.md) に記載された情報を参考に、Azure のサブスクリプションが LCS プロジェクトに接続済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="62300-114">Verify that you’ve connected your Azure subscription to your LCS project by using the information in the [Complete the Azure Resource Manager (ARM) onboarding process](arm-onboarding.md) topic.</span></span>

## <a name="deploy-a-demo-environment"></a><span data-ttu-id="62300-115">デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="62300-115">Deploy a demo environment</span></span>
<span data-ttu-id="62300-116">LCS を使用して Azure でデモ環境を配置するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="62300-116">Use this procedure to deploy a demo environment on Azure using LCS.</span></span> 

1. <span data-ttu-id="62300-117">LCS でプロジェクトを開き、**環境** セクションでプラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62300-117">In LCS, open your project, and then, in the **Environments** section, click the plus sign (**+**).</span></span>
2. <span data-ttu-id="62300-118">Azure 環境トポロジを選択し、**デモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-118">Select the Azure environment topology, and then select **Demo**.</span></span>
3. <span data-ttu-id="62300-119">トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-119">Select a topology.</span></span>
    - <span data-ttu-id="62300-120">Finance and Operations では、Finance and Operations の最新の Azure Resource Manager (ARM) トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-120">For Finance and Operations, select the most recent Azure Resource Manager (ARM) topology for Finance and Operations.</span></span>
    - <span data-ttu-id="62300-121">コマースで、**Dynamics 365 for Commerce - デモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-121">For Commerce, select **Dynamics 365 for Commerce - Demo**.</span></span>
4. <span data-ttu-id="62300-122">**環境の配置** ダイアログ ボックスに、環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="62300-122">In the **Deploy environment** dialog box, enter the name of the environment.</span></span> <span data-ttu-id="62300-123">この名前は Azure サブスクリプションで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="62300-123">This name should be unique in the Azure subscription.</span></span> <span data-ttu-id="62300-124">環境を簡単に識別できるようにするには、ユーザー名とトポロジを使用して略語を作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="62300-124">To make environments easy to identify, consider forming an acronym using the user’s name and the topology.</span></span>
5. <span data-ttu-id="62300-125">仮想マシン (VM) のサイズを選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-125">Select the size of the virtual machine (VM).</span></span> <span data-ttu-id="62300-126">ARM 用に有効になっている VM のすべてのサイズは、v2 で終わります。</span><span class="sxs-lookup"><span data-stu-id="62300-126">All the sizes for VMs that are enabled for ARM end with v2.</span></span> <span data-ttu-id="62300-127">Finance and Operations のワークロードには、D\* v2 サイズを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62300-127">You must use D\* v2 sizes for Finance and Operations workloads.</span></span> <span data-ttu-id="62300-128">D12v2 をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="62300-128">We recommend D12v2.</span></span>
6. <span data-ttu-id="62300-129">**インスタンス** フィールドを 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="62300-129">Set the **Instances** field to 1.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="62300-130">VM のサイズ と インスタンス の数は、サブスクリプションのコストに影響します。</span><span class="sxs-lookup"><span data-stu-id="62300-130">The size of the VM and the number of instances affect the cost of your subscription.</span></span> <span data-ttu-id="62300-131">詳細については、 [Azure の価格設定](https://azure.microsoft.com/pricing/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62300-131">For more information, see [Azure pricing](https://azure.microsoft.com/pricing/).</span></span>


7. <span data-ttu-id="62300-132">**詳細設定** をクリックし、配置にカスタマイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="62300-132">Click **Advanced settings** to add customizations to your deployment.</span></span> <span data-ttu-id="62300-133">デモ環境では、既定の設定のままにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="62300-133">For the demo environment, we recommend that you keep the default settings.</span></span>
8. <span data-ttu-id="62300-134">ライセンスおよび価格条件に同意し、 **次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62300-134">Agree to the licensing and pricing terms, and then click **Next**.</span></span>
9. <span data-ttu-id="62300-135">**確認** メッセージ ボックスで、**配置** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="62300-135">In the **Confirm** message box, click **Deploy**.</span></span>
10. <span data-ttu-id="62300-136">配置のステータスを表示するには、**クラウド ホスト環境** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="62300-136">Open the **Cloud hosted environments** page to view the status of the deployment.</span></span> <span data-ttu-id="62300-137">配置が正常に完了すると、環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="62300-137">After the deployment is successfully completed, the environment will be ready.</span></span>

## <a name="log-on-to-your-demo-environment"></a><span data-ttu-id="62300-138">デモ環境へのログオン</span><span class="sxs-lookup"><span data-stu-id="62300-138">Log on to your demo environment</span></span>
<span data-ttu-id="62300-139">デモ環境にログオンするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="62300-139">To log on to your demo environment, do the following.</span></span>

1. <span data-ttu-id="62300-140">LCS で、**クラウド ホスト環境** ページを開き、配置したデモ環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="62300-140">In LCS, open the **Cloud-hosted environments** page, and select the demo environment that you just deployed.</span></span>

2. <span data-ttu-id="62300-141">右にスクロールし、**環境の詳細** ウィンドウの **クラウド サービス** で、適切なリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="62300-141">Scroll to the right and in the **Environment details** pane, under **Cloud services**, click the appropriate link:</span></span>

      - <span data-ttu-id="62300-142">**Finance and Operations にログオン**</span><span class="sxs-lookup"><span data-stu-id="62300-142">**Log on to Finance and Operations**</span></span>
      - <span data-ttu-id="62300-143">**コマースにログオン**</span><span class="sxs-lookup"><span data-stu-id="62300-143">**Log on to Commerce**</span></span>
