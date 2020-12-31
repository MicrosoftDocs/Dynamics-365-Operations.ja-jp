---
title: Lifecycle Services からの二重書き込み設定
description: このトピックでは、新しい Finance and Operations 環境と新しい Dataverse 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。
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
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683528"
---
# <a name="dual-write-setup-from-lifecycle-services"></a><span data-ttu-id="6a686-103">Lifecycle Services からの二重書き込み設定</span><span class="sxs-lookup"><span data-stu-id="6a686-103">Dual-write setup from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="6a686-104">このトピックでは、新しい Finance and Operations 環境と新しい Dataverse 環境間での二重書き込み接続を Microsoft Dynamics Lifecycle Services (LCS) から設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6a686-104">This topic explains how to set up a dual-write connection between a new Finance and Operations environment and a new Dataverse environment from Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6a686-105">必要条件</span><span class="sxs-lookup"><span data-stu-id="6a686-105">Prerequisites</span></span>

<span data-ttu-id="6a686-106">二重書き込み接続を設定するには、管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a686-106">You must be an admin to set up a dual-write connection.</span></span>

+ <span data-ttu-id="6a686-107">テナントにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a686-107">You must have access to the tenant.</span></span>
+ <span data-ttu-id="6a686-108">Finance and Operations 環境および Dataverse 環境の両方において管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a686-108">You must be an admin in both Finance and Operations environments and Dataverse environments.</span></span>

## <a name="set-up-a-dual-write-connection"></a><span data-ttu-id="6a686-109">二重書き込み接続の設定</span><span class="sxs-lookup"><span data-stu-id="6a686-109">Set up a dual-write connection</span></span>

<span data-ttu-id="6a686-110">二重書き込み接続を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6a686-110">Follow these steps to set up the dual-write connection.</span></span>

1. <span data-ttu-id="6a686-111">LCS で、プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="6a686-111">In LCS, go to your project.</span></span>
2. <span data-ttu-id="6a686-112">**コンフィギュレーション** を選択して、新しい環境を配置します。</span><span class="sxs-lookup"><span data-stu-id="6a686-112">Select **Configure** to deploy a new environment.</span></span>
3. <span data-ttu-id="6a686-113">バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-113">Select the version.</span></span> 
4. <span data-ttu-id="6a686-114">トポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-114">Select the topology.</span></span> <span data-ttu-id="6a686-115">使用可能なトポロジが 1 つだけの場合、自動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="6a686-115">If only one topology is available, it's automatically selected.</span></span>
5. <span data-ttu-id="6a686-116">**配置設定** ウィザードの最初の手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="6a686-116">Complete the first steps in the **Deployment settings** wizard.</span></span>
6. <span data-ttu-id="6a686-117">**Dataverse** タブで、次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="6a686-117">On the **Dataverse** tab, follow one of these steps:</span></span>

    - <span data-ttu-id="6a686-118">テナントに Dataverse が既にプロビジョニングされている場合、それを選択できます。</span><span class="sxs-lookup"><span data-stu-id="6a686-118">If a Dataverse environment is already provisioned for your tenant, you can select it.</span></span>

        1. <span data-ttu-id="6a686-119">**Dataverse のコンフィギュレーション** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6a686-119">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="6a686-120">**使用可能な環境** フィールドで、Finance and Operations データと統合する環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-120">In the **Available environments** field, select the environment to integrate with your Finance and Operations data.</span></span> <span data-ttu-id="6a686-121">一覧には、管理者特権を持っているすべての環境が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6a686-121">The list includes all environments where you have admin privileges.</span></span>
        3. <span data-ttu-id="6a686-122">**同意** チェック ボックスをオンにして、使用条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="6a686-122">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![テナントに Dataverse が既にプロビジョニングされている場合の Dataverse タブ](../dual-write/media/lcs_setup_1.png)

    - <span data-ttu-id="6a686-124">テナントに Dataverse 環境がまだ存在しない場合、新しい環境がプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="6a686-124">If your tenant doesn't already have a Dataverse environment, a new environment will be provisioned.</span></span>

        1. <span data-ttu-id="6a686-125">**Dataverse のコンフィギュレーション** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="6a686-125">Set the **Configure Dataverse** option to **Yes**.</span></span>
        2. <span data-ttu-id="6a686-126">Dataverse 環境の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6a686-126">Enter a name for the Dataverse environment.</span></span>
        3. <span data-ttu-id="6a686-127">環境を配置する地域を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-127">Select the region to deploy the environment in.</span></span>
        4. <span data-ttu-id="6a686-128">環境の既定の言語と通貨を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-128">Select the default language and currency for the environment.</span></span>

            > [!NOTE]
            > <span data-ttu-id="6a686-129">言語と通貨を後で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="6a686-129">You can't change the language and currency later.</span></span>

        5. <span data-ttu-id="6a686-130">**同意** チェック ボックスをオンにして、使用条件に同意することを示します。</span><span class="sxs-lookup"><span data-stu-id="6a686-130">Select the **Agree** check box to indicate that you agree to the terms and conditions.</span></span>

        ![テナントに Dataverse 環境がまだ存在しない場合の Dataverse タブ](../dual-write/media/lcs_setup_2.png)

7. <span data-ttu-id="6a686-132">**配置設定** ウィザードの残りの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="6a686-132">Complete the remaining steps in the **Deployment settings** wizard.</span></span>
8. <span data-ttu-id="6a686-133">環境の状態が **配置** になった後、環境の詳細ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6a686-133">After the environment has a status of **Deployed**, open the environment details page.</span></span> <span data-ttu-id="6a686-134">**Dataverse 環境情報** セクションには、リンクされている Finance and Operations 環境および Dataverse 環境の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a686-134">The **Dataverse environment information** section shows the names of the Finance and Operations environment and the Dataverse environment that are linked.</span></span>

    ![Dataverse 環境情報セクション](../dual-write/media/lcs_setup_3.png)

9. <span data-ttu-id="6a686-136">Finance and Operations 環境の管理者がリンクを完了するには、LCS にサインインし、**アプリの CDS にリンク** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6a686-136">An admin of the Finance and Operations environment must sign in to LCS and select **Link to CDS for Apps** to complete the link.</span></span> <span data-ttu-id="6a686-137">環境の詳細ページには、管理者の連絡先情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6a686-137">The environment details page shows the admin's contact information.</span></span>

    <span data-ttu-id="6a686-138">リンクが完了した後、状態が **環境のリンクが正常に完了しました** に更新されます。</span><span class="sxs-lookup"><span data-stu-id="6a686-138">After the link is completed, the status is updated to **Environment linking successfully completed**.</span></span>

10. <span data-ttu-id="6a686-139">Finance and Operations 環境で **データ統合** ワークスペースを開いて、使用可能なテンプレートを管理するには、**アプリの CDS にリンク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-139">To open the **Data integration** workspace in the Finance and Operations environment and control the templates that are available, select **Link to CDS for Apps**.</span></span>

    ![Dataverse 環境情報セクションのアプリの CDS ボタンににリンク](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> <span data-ttu-id="6a686-141">LCS を使用して環境のリンクを解除することはできません。</span><span class="sxs-lookup"><span data-stu-id="6a686-141">You can't unlink environments by using LCS.</span></span> <span data-ttu-id="6a686-142">環境のリンクを解除するには、Finance and Operations 環境の **データ統合** ワークスペースを開き、**リンク解除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6a686-142">To unlink an environment, open the **Data integration** workspace in the Finance and Operations environment, and then select **Unlink**.</span></span>
