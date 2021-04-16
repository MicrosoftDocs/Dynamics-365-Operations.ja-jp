---
title: リース承認ワークフローの設定
description: このトピックでは、新しいリースが作成されたときに実行される承認ワークフローの設定方法について説明します。
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4d5416b3b24d5fbb3ac46afb3c672212d41d42d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827557"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="dcf0b-103">リース承認ワークフローの設定</span><span class="sxs-lookup"><span data-stu-id="dcf0b-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcf0b-104">このトピックでは、新しいリースが作成されたときに実行される承認ワークフローの設定方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="dcf0b-105">ワークフローの使用方法の詳細については、[リース承認ワークフローの使用](use-create-lease-wrkflw.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="dcf0b-106">**資産リース \> 設定 \> リース ワークフロー** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="dcf0b-107">**リース ワークフロー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="dcf0b-108">表示されるダイアログボックスの **ワークフロー タイプ** で、**リース ワークフロー** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="dcf0b-109">アプリケーションが開きます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-109">The application is opened.</span></span> <span data-ttu-id="dcf0b-110">実行されたら、Azure Active Directory (Azure AD) にサインインします。ワークフロー アプリケーションにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="dcf0b-111">**リース ワークフローの承認** 要素をワークフローにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="dcf0b-112">1 つのノードを **開始** から **リース ワークフローの承認** に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="dcf0b-113">次に、**リース ワークフローの承認** を **終了** に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="dcf0b-114">**リース ワークフローの承認** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="dcf0b-115">**プロパティ** をクリックし、**基本設定** でワークフローの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="dcf0b-116">このページでは、ワークフローに対してさらにパラメーターを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="dcf0b-117">**自動アクション** が有効になっている場合、システムによって自動的に特定のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="dcf0b-118">通知は、**通知** タブで指定されている場合に送信できます。**詳細設定** タブでは、最終承認者の指定、制限時間の設定、および完了する必要がある特定のアクションの指定を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="dcf0b-119">すべてのワークフロー パラメーターの設定が終了したら **閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="dcf0b-120">**ステップ 1** を選択し、次に **プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="dcf0b-121">**基本設定** で、ステップの名前を入力し、承認の件名行を作成します。また、承認の指示を指定します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="dcf0b-122">**割り当て** ページで、割り当てタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="dcf0b-123">特定のユーザーを承認に割り当てるには、**ユーザー** を選択し、リースを承認するユーザーを選択して、**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="dcf0b-124">**保存して終了** を選択して、ワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="dcf0b-125">次に、メッセージが表示されたら、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="dcf0b-126">**ワークフローの作成** ページで、**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="dcf0b-127">新しいワークフローを選択し、**バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="dcf0b-128">**有効にする** をオンにして、ワークフローが有効になっていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="dcf0b-129">**閉じる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-129">Select **Close**.</span></span> <span data-ttu-id="dcf0b-130">新しい有効なバージョンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dcf0b-130">The new active version appears.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]