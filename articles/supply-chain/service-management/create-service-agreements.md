---
title: "サービス契約の作成"
description: "このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2a46173a3566a56a21add9d42c111d456b1ae7c1
ms.openlocfilehash: 517bc1b9de9b2512f42e4f32b4a19e517e349e8e
ms.contentlocale: ja-jp
ms.lasthandoff: 02/19/2018

---

# <a name="create-service-agreements"></a><span data-ttu-id="f69d9-103">サービス契約の作成</span><span class="sxs-lookup"><span data-stu-id="f69d9-103">Create service agreements</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f69d9-104">このトピックでは、サービス管理モジュールおよびプロジェクト管理と会計モジュールの機能を使用して、サービス合意を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-104">This topic describes how to use features in the Service management and the Project management and accounting modules to create service agreements.</span></span>

## <a name="create-a-service-agreement-from-service-management"></a><span data-ttu-id="f69d9-105">サービス管理からのサービス合意の作成</span><span class="sxs-lookup"><span data-stu-id="f69d9-105">Create a service agreement from Service management</span></span>

1. <span data-ttu-id="f69d9-106">**サービス管理**に移動します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-106">Navigate to **Service management**.</span></span>
2. <span data-ttu-id="f69d9-107">**サービス契約** をクリックして、ページ ヘッダーで新しいサービス契約項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-107">Click **Service agreements** to create a new service agreement line in the page header.</span></span> 
3. <span data-ttu-id="f69d9-108">[**新規**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f69d9-108">Click **New**.</span></span> <span data-ttu-id="f69d9-109">説明を入力し、**プロジェクト ID** フィールドでプロジェクトへの参照を選択し、サービス合意の残りのフィールドおよび項目に情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-109">Enter a description, select a reference to a project in the **Project ID** field, and fill in the rest of the fields and lines for the service agreement.</span></span> <span data-ttu-id="f69d9-110">[**保存**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f69d9-110">Click **Save**.</span></span>
4. <span data-ttu-id="f69d9-111">**関係** タブで、**サービス対象** または **サービス タスク** を選択して、サービス合意のサービス対象関係またはサービス作業関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-111">On the **Relations** tab, select **Service objects** or **Service tasks** to create service object relations or service task relations for the service agreement.</span></span> <span data-ttu-id="f69d9-112">関係を作成したサービス対象およびサービス作業は、サービス合意項目で関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f69d9-112">The service objects and tasks that you have created relations for can be attached on the lines of the service agreement.</span></span>
5. <span data-ttu-id="f69d9-113">ページの下半分で、サービス テンプレートまたは別のサービス契約から明細行をコピーするか、またはサービス契約項目を手動で作成して、サービス契約項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-113">In the lower half of the page, create service agreement lines by copying lines from a service template, another service agreement, or manually creating the service-agreement lines.</span></span>

> [!NOTE]
> <span data-ttu-id="f69d9-114">あるサービス合意に別のサービス合意項目をコピーする場合は、サービス対象やサービス タスク関係もコピーするかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f69d9-114">If you copy lines into the service agreement from another service agreement, you can indicate whether you also want to copy service object and service task relations.</span></span> <span data-ttu-id="f69d9-115">これらの関係をコピーすると、これらの関係がサービス合意の既存の関係に追加されます。</span><span class="sxs-lookup"><span data-stu-id="f69d9-115">If you copy these relations, they are added to any existing relations on the service agreement.</span></span> <span data-ttu-id="f69d9-116">サービス テンプレートからサービス合意項目をコピーする場合は、サービス対象関係およびサービス作業関係が、新しいサービス合意項目のサービス対象関係およびサービス作業関係として自動的にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="f69d9-116">If you copy service-agreement lines from a service template, the service-object and service-task relations are automatically copied as service-object relations and service-task relations on the new service-agreement lines.</span></span>

## <a name="create-service-agreement-lines-manually"></a><span data-ttu-id="f69d9-117">手動によるサービス契約項目の作成</span><span class="sxs-lookup"><span data-stu-id="f69d9-117">Create service agreement lines manually</span></span>

1. <span data-ttu-id="f69d9-118">**サービス契約** ページから、行グリッドにサービス契約項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-118">From the **Service agreements** page, add a service agreement line in the lines grid.</span></span> 
2. <span data-ttu-id="f69d9-119">このサービス契約項目の適切な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-119">Enter the appropriate information for the service agreement line.</span></span> 
3. <span data-ttu-id="f69d9-120">**CTRL + S** キーを押して項目を保存し、ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="f69d9-120">Press **CTRL+S** to save the line, and then close the page.</span></span>

## <a name="create-a-service-agreement-from-project"></a><span data-ttu-id="f69d9-121">プロジェクトからのサービス合意の作成</span><span class="sxs-lookup"><span data-stu-id="f69d9-121">Create a service agreement from Project</span></span>

1. <span data-ttu-id="f69d9-122">**プロジェクト管理と会計**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f69d9-122">Click **Project management and accounting**.</span></span>
2. <span data-ttu-id="f69d9-123">**すべてのプロジェクト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f69d9-123">Click **All projects**.</span></span>
3. <span data-ttu-id="f69d9-124">リストからプロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-124">Select the project from the list.</span></span>
4. <span data-ttu-id="f69d9-125">**アクション ウィンドウ**で、**管理**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f69d9-125">On the **Action Pane**, click **Manage**.</span></span> <span data-ttu-id="f69d9-126">**新規** アクション グループで、**サービス** をクリックして **サービス契約**を選択します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-126">In the **New** Action group, click **Service** and select **Service agreement**.</span></span>
5. <span data-ttu-id="f69d9-127">このトピックで前述されているように、**サービス契約の作成** というタイトルのセクションで手順に従ってプロジェクト参照を入力します。</span><span class="sxs-lookup"><span data-stu-id="f69d9-127">Follow the steps in the section titled **Create a service agreement** as described earlier in this topic to enter the project reference.</span></span>


## <a name="related-topics"></a><span data-ttu-id="f69d9-128">関連トピック</span><span class="sxs-lookup"><span data-stu-id="f69d9-128">Related topics</span></span>

[<span data-ttu-id="f69d9-129">サービス合意 </span><span class="sxs-lookup"><span data-stu-id="f69d9-129">Service agreements</span></span>](service-agreements.md)



