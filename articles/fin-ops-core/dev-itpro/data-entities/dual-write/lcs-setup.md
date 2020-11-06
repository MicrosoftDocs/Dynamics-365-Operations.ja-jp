---
title: Lifecycle Services からの二重書き込み設定
description: このトピックでは、新しい Finance and Operations 環境と新しい Common Data Service 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: f49eba1748861af6ee3353a6c58005ee84ccae23
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998111"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="0437f-103">Lifecycle Services からの二重書き込み設定</span><span class="sxs-lookup"><span data-stu-id="0437f-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="0437f-104">このトピックでは、新しい Finance and Operations 環境と新しい Common Data Service 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0437f-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Common Data Service environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0437f-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="0437f-105">Prerequisites</span></span>

<span data-ttu-id="0437f-106">二重書き込み接続を設定するには、管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0437f-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="0437f-107">テナントにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="0437f-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="0437f-108">Finance and Operations 環境および Common Data Service 環境の両方において管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="0437f-108">You must be an admin in both Finance and Operations environments and Common Data Service environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="0437f-109">二重書き込み接続の設定</span><span class="sxs-lookup"><span data-stu-id="0437f-109">Set up a dual-write connection</span></span>

<span data-ttu-id="0437f-110">二重書き込み接続を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="0437f-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="0437f-111">LCS で、プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="0437f-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="0437f-112">**コンフィギュレーション** を選択して、新しい環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="0437f-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="0437f-113">バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-113">Select the version.</span></span> 
4. <span data-ttu-id="0437f-114">トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-114">Select the topology.</span></span> <span data-ttu-id="0437f-115">使用可能なトポロジが 1 つだけの場合、自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="0437f-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="0437f-116">**配置設定** ウィザードの最初の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="0437f-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="0437f-117">**Common Data Service** タブで、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="0437f-117">On the **Common Data Service** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="0437f-118">テナントに Common Data Service が既にプロビジョニングされている場合、それを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0437f-118">If a Common Data Service environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="0437f-119">**Common Data Service のコンフィギュレーション** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0437f-119">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="0437f-120">**使用可能な環境** フィールドで、Finance and Operations データと統合する環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="0437f-121">一覧には、管理者特権を持っているすべての環境が含まれます。</span><span class="sxs-lookup"><span data-stu-id="0437f-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="0437f-122">**同意** チェック ボックスをオンにして、使用条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="0437f-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![テナントに Common Data Service が既にプロビジョニングされている場合の Common Data Service タブ](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="0437f-124">テナントに Common Data Service 環境がまだ存在しない場合、新しい環境がプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="0437f-124">If your tenant doesn't already have a Common Data Service environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="0437f-125">**Common Data Service のコンフィギュレーション** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="0437f-125">Set the **Configure Common Data Service** option to **Yes**.</span></span>
        2. <span data-ttu-id="0437f-126">Common Data Service 環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="0437f-126">Enter a name for the Common Data Service environment.</span></span>
        3. <span data-ttu-id="0437f-127">環境を配置する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="0437f-128">環境の既定の言語と通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="0437f-129">言語と通貨を後で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="0437f-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="0437f-130">**同意** チェック ボックスをオンにして、使用条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="0437f-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![テナントに Common Data Service 環境がまだ存在しない場合の Common Data Service タブ](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="0437f-132">**配置設定** ウィザードの残りの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="0437f-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="0437f-133">環境の状態が **配置** になった後、環境の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="0437f-133">After the environment has a status of **Deployed** , open the environment details page.</span></span> <span data-ttu-id="0437f-134">**Common Data Service 環境情報** セクションには、リンクされている Finance and Operations 環境および Common Data Service 環境の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0437f-134">The **Common Data Service environment information** section shows the names of the Finance and Operations environment and the Common Data Service environment that are linked.</span></span>

    ![Common Data Service 環境情報セクション](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="0437f-136">Finance and Operations 環境の管理者がリンクを完了するには、LCS にサインインし、 **アプリの CDS にリンク** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0437f-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="0437f-137">環境の詳細ページには、管理者の連絡先情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0437f-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="0437f-138">リンクが完了した後、状態が **環境のリンクが正常に完了しました** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="0437f-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="0437f-139">Finance and Operations 環境で **データ統合** ワークスペースを開いて、使用可能なテンプレートを管理するには、 **アプリの CDS にリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Common Data Service 環境情報セクションのアプリの CDS ボタンににリンク](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="0437f-141">LCS を使用して環境のリンクを解除することはできません。</span><span class="sxs-lookup"><span data-stu-id="0437f-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="0437f-142">環境のリンクを解除するには、Finance and Operations 環境の **データ統合** ワークスペースを開き、 **リンク解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="0437f-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
