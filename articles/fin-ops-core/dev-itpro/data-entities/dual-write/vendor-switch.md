---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Common Data Service との間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
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
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 0ecc401706911f8b92146b95bb6415185df8b451
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997555"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="cf2a6-103">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="cf2a6-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="cf2a6-104">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="cf2a6-104">Vendor data flow</span></span> 

<span data-ttu-id="cf2a6-105">**取引先企業** エンティティを使用して **組織** タイプの仕入先を保存し、 **連絡先** エンティティを使用して **個人** タイプの仕入先を保存する場合は、次のワークフローをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="cf2a6-106">それ以外の場合、このコンフィギュレーションは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="cf2a6-107">組織タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="cf2a6-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="cf2a6-108">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="cf2a6-109">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="cf2a6-110">アカウント エンティティでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="cf2a6-110">Create Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="cf2a6-111">仕入先エンティティでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="cf2a6-111">Create Vendors in Vendors Entity</span></span>
+ <span data-ttu-id="cf2a6-112">アカウント エンティティでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="cf2a6-112">Update Vendors in Accounts Entity</span></span>
+ <span data-ttu-id="cf2a6-113">仕入先エンティティでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="cf2a6-113">Update Vendors in Vendors Entity</span></span>

<span data-ttu-id="cf2a6-114">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="cf2a6-115">**仕入先** エンティティのワークフロー プロセスを作成して、 **アカウント エンティティで仕入先を作成** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="cf2a6-116">その後、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-116">Then select **OK**.</span></span> <span data-ttu-id="cf2a6-117">このワークフローでは、 **アカウント** エンティティの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![アカウント エンティティ ワークフロー プロセスでの仕入先の作成](media/create_process.png)

2. <span data-ttu-id="cf2a6-119">**仕入先** エンティティのワークフロー プロセスを作成して、 **アカウント エンティティで仕入先を更新** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Entity** workflow process template.</span></span> <span data-ttu-id="cf2a6-120">その後、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-120">Then select **OK**.</span></span> <span data-ttu-id="cf2a6-121">このワークフローでは、 **アカウント** エンティティの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="cf2a6-122">**アカウント** エンティティのワークフロー プロセスを作成して、 **仕入先エンティティで仕入先を作成** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Entity** workflow process template.</span></span>
4. <span data-ttu-id="cf2a6-123">**アカウント** エンティティのワークフロー プロセスを作成して、 **仕入先エンティティで仕入先を更新** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Entity** workflow process template.</span></span>
5. <span data-ttu-id="cf2a6-124">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="cf2a6-125">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、 **バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![バックグラウンド ワークフロー ボタンへの変換](media/background_workflow.png)

6. <span data-ttu-id="cf2a6-127">**アカウント** エンティティと **仕入先** エンティティで作成したワークフローを有効にして、その **組織** タイプの仕入先情報を保存するために **アカウント**  エンティティの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-127">Activate the workflows that you created for the **Account** and **Vendor** entities to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="cf2a6-128">個人タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="cf2a6-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="cf2a6-129">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="cf2a6-130">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="cf2a6-131">仕入先エンティティでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="cf2a6-131">Create Vendors of type Person in Vendors Entity</span></span>
+ <span data-ttu-id="cf2a6-132">連絡先エンティティでタイプが個人の仕入先を作成する</span><span class="sxs-lookup"><span data-stu-id="cf2a6-132">Create Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="cf2a6-133">連絡先エンティティでタイプが個人の仕入先を更新する</span><span class="sxs-lookup"><span data-stu-id="cf2a6-133">Update Vendors of type Person in Contacts Entity</span></span>
+ <span data-ttu-id="cf2a6-134">仕入先エンティティでタイプが個人の仕入先を作成する</span><span class="sxs-lookup"><span data-stu-id="cf2a6-134">Update Vendors of type Person in Vendors Entity</span></span>

<span data-ttu-id="cf2a6-135">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="cf2a6-136">**仕入先** エンティティのワークフロー プロセスを作成して、 **連絡先エンティティでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="cf2a6-137">その後、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-137">Then select **OK**.</span></span> <span data-ttu-id="cf2a6-138">このワークフローでは、 **連絡先** エンティティの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="cf2a6-139">**仕入先** エンティティのワークフロー プロセスを作成して、 **連絡先エンティティでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Entity** workflow process template.</span></span> <span data-ttu-id="cf2a6-140">その後、 **OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-140">Then select **OK**.</span></span> <span data-ttu-id="cf2a6-141">このワークフローでは、 **連絡先** エンティティの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="cf2a6-142">**連絡先** エンティティのワークフロー プロセスを作成して、 **仕入先エンティティでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Entity** template.</span></span>
4. <span data-ttu-id="cf2a6-143">**連絡先** エンティティのワークフロー プロセスを作成して、 **仕入先エンティティでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Entity** template.</span></span>
5. <span data-ttu-id="cf2a6-144">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="cf2a6-145">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、 **バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="cf2a6-146">**連絡先** エンティティと **仕入先** エンティティで作成したワークフローを有効にして、その **個人** タイプの仕入先情報を保存するために **連絡先** エンティティの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="cf2a6-146">Activate the workflows that you created on the **Contact** and **Vendor** entities to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
