---
title: "デモ環境の配置"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。 これは、Dynamics 365 for Finance and Operations および Dynamics 365 for Retail に適用されます。"
author: sarvanisathish
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 141093
ms.assetid: dcd23629-246d-4fbc-adf5-7245bb2121e4
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bf3d85eb424ee050c163e22e70b7094554cced9a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="deploy-a-demo-environment"></a><span data-ttu-id="fb20f-104">デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="fb20f-104">Deploy a demo environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb20f-105">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Azure にデモ環境を配置する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-105">This topic explains how to deploy a demo environment on Microsoft Azure using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="fb20f-106">このトピックは、以下のデモ環境の配置に適用されます。</span><span class="sxs-lookup"><span data-stu-id="fb20f-106">This topic applies to deploying a demo environment for:</span></span>

- <span data-ttu-id="fb20f-107">Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fb20f-107">Dynamics 365 for Finance and Operations</span></span>
- <span data-ttu-id="fb20f-108">Dynamics 365 for Retail</span><span class="sxs-lookup"><span data-stu-id="fb20f-108">Dynamics 365 for Retail</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fb20f-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="fb20f-109">Prerequisites</span></span>
<span data-ttu-id="fb20f-110">展開を開始する前に、次の前提条件が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-110">Before you begin your deployment, the following prerequisites must be in place:</span></span>

- <span data-ttu-id="fb20f-111">Azure サブスクリプションがあり、そのサブスクリプションの共同管理者であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-111">Verify that you have an Azure subscription, and that you are a co-administrator on it.</span></span>
- <span data-ttu-id="fb20f-112">LCS プロジェクトへのアクセスが可能であり、環境を展開するためのアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-112">Verify that you have access to an LCS project and permissions to deploy an environment.</span></span>
- <span data-ttu-id="fb20f-113">[Azure Resource Manager オンボード](arm-onboarding.md) のトピックを使用して、Azure サブスクリプションが LCS プロジェクトに接続済みであることを確認します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-113">Verify that you’ve connected your Azure subscription to your LCS project by using the information in the [Azure Resource Manager onboarding](arm-onboarding.md) topic.</span></span>

## <a name="deploy-a-demo-environment"></a><span data-ttu-id="fb20f-114">デモ環境の配置</span><span class="sxs-lookup"><span data-stu-id="fb20f-114">Deploy a demo environment</span></span>
<span data-ttu-id="fb20f-115">LCS を使用して Azure でデモ環境を配置するには、この手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-115">Use this procedure to deploy a demo environment on Azure using LCS.</span></span> 

1. <span data-ttu-id="fb20f-116">LCS でプロジェクトを開き、**環境**セクションでプラス記号 (**+**) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-116">In LCS, open your project, and then, in the **Environments** section, click the plus sign (**+**).</span></span>
2. <span data-ttu-id="fb20f-117">Azure 環境トポロジを選択し、**デモ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-117">Select the Azure environment topology, and then select **Demo**.</span></span>
3. <span data-ttu-id="fb20f-118">トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-118">Select a topology.</span></span>
    - <span data-ttu-id="fb20f-119">Finance and Operations で、Finance and Operations 用の最新の Azure Resource Manager (ARM) トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-119">For Finance and Operations, select the most recent Azure Resource Manager (ARM) topology for Finance and Operations.</span></span>
    - <span data-ttu-id="fb20f-120">Retail で、**Dynamics 365 for Retail - デモ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-120">For Retail, select **Dynamics 365 for Retail - Demo**.</span></span>
4. <span data-ttu-id="fb20f-121">**環境の配置**ダイアログ ボックスに、環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-121">In the **Deploy environment** dialog box, enter the name of the environment.</span></span> <span data-ttu-id="fb20f-122">この名前は Azure サブスクリプションで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb20f-122">This name should be unique in the Azure subscription.</span></span> <span data-ttu-id="fb20f-123">環境を簡単に識別できるようにするには、ユーザー名とトポロジを使用して略語を作成することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="fb20f-123">To make environments easy to identify, consider forming an acronym using the user’s name and the topology.</span></span>
5. <span data-ttu-id="fb20f-124">仮想マシン (VM) のサイズを選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-124">Select the size of the virtual machine (VM).</span></span> <span data-ttu-id="fb20f-125">ARM 用に有効になっている VM のすべてのサイズは、v2 で終わります。</span><span class="sxs-lookup"><span data-stu-id="fb20f-125">All the sizes for VMs that are enabled for ARM end with v2.</span></span> <span data-ttu-id="fb20f-126">Finance and Operations のワークロードには、D\* v2 サイズを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb20f-126">You must use D\* v2 sizes for Finance and Operations workloads.</span></span> <span data-ttu-id="fb20f-127">D12v2 をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-127">We recommend D12v2.</span></span>
6. <span data-ttu-id="fb20f-128">**インスタンス** フィールドを 1 に設定します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-128">Set the **Instances** field to 1.</span></span>


~~~
**Note:** The size of the VM and the number of instances affect the cost of your subscription. For more information, see [Azure pricing](https://azure.microsoft.com/en-us/pricing/).
~~~

7. <span data-ttu-id="fb20f-129">**詳細設定**をクリックし、配置にカスタマイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-129">Click **Advanced settings** to add customizations to your deployment.</span></span> <span data-ttu-id="fb20f-130">デモ環境では、既定の設定のままにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-130">For the demo environment, we recommend that you keep the default settings.</span></span>
8. <span data-ttu-id="fb20f-131">ライセンスおよび価格条件に同意し、 **次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-131">Agree to the licensing and pricing terms, and then click **Next**.</span></span>
9. <span data-ttu-id="fb20f-132">**確認**メッセージ ボックスで、**配置**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-132">In the **Confirm** message box, click **Deploy**.</span></span>
10. <span data-ttu-id="fb20f-133">配置のステータスを表示するには、**クラウド ホスト環境**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="fb20f-133">Open the **Cloud hosted environments** page to view the status of the deployment.</span></span> <span data-ttu-id="fb20f-134">配置が正常に完了すると、環境が準備されます。</span><span class="sxs-lookup"><span data-stu-id="fb20f-134">After the deployment is successfully completed, the environment will be ready.</span></span>

## <a name="log-on-to-your-demo-environment"></a><span data-ttu-id="fb20f-135">デモ環境へのログオン</span><span class="sxs-lookup"><span data-stu-id="fb20f-135">Log on to your demo environment</span></span>
<span data-ttu-id="fb20f-136">デモ環境にログオンするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-136">To log on to your demo environment, do the following.</span></span>

1. <span data-ttu-id="fb20f-137">LCS で、**クラウド ホスト環境**ページを開き、配置したデモ環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="fb20f-137">In LCS, open the **Cloud-hosted environments** page, and select the demo environment that you just deployed.</span></span>

2. <span data-ttu-id="fb20f-138">右にスクロールし、**環境の詳細** ウィンドウの **クラウド サービス** で、適切なリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="fb20f-138">Scroll to the right and in the **Environment details** pane, under **Cloud services**, click the appropriate link:</span></span>

      - <span data-ttu-id="fb20f-139">**Finance and Operations にログオン**</span><span class="sxs-lookup"><span data-stu-id="fb20f-139">**Log on to Finance and Operations**</span></span>
      - <span data-ttu-id="fb20f-140">**小売にログオン**</span><span class="sxs-lookup"><span data-stu-id="fb20f-140">**Log on to Retail**</span></span>
