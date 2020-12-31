---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Dataverse との間の仕入先データの統合を切り替える方法について説明します。
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
ms.openlocfilehash: 731efd3ae841960f3a2c0b9be210c5c68ac835f5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685512"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="d674a-103">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="d674a-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="d674a-104">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="d674a-104">Vendor data flow</span></span> 

<span data-ttu-id="d674a-105">**取引先企業** エンティティを使用して **組織** タイプの仕入先を保存し、**連絡先** エンティティを使用して **個人** タイプの仕入先を保存する場合は、次のワークフローをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="d674a-105">If you choose to use the **Account** entity to store vendors of the **Organization** type and the **Contact** entity to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="d674a-106">それ以外の場合、このコンフィギュレーションは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="d674a-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="d674a-107">組織タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="d674a-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="d674a-108">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d674a-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="d674a-109">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="d674a-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="d674a-110">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="d674a-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="d674a-111">仕入先テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="d674a-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="d674a-112">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="d674a-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="d674a-113">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="d674a-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="d674a-114">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="d674a-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="d674a-115">**仕入先** エンティティのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を作成** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-115">Create a workflow process for the **Vendor** entity, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="d674a-116">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-116">Then select **OK**.</span></span> <span data-ttu-id="d674a-117">このワークフローでは、**アカウント** エンティティの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="d674a-117">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>

    ![取引先企業テーブル ワークフロー プロセスでの仕入先の作成](media/create_process.png)

2. <span data-ttu-id="d674a-119">**仕入先** エンティティのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を更新** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-119">Create a workflow process for the **Vendor** entity, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="d674a-120">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-120">Then select **OK**.</span></span> <span data-ttu-id="d674a-121">このワークフローでは、**アカウント** エンティティの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="d674a-121">This workflow handles the vendor update scenario for the **Account** entity.</span></span>
3. <span data-ttu-id="d674a-122">**取引先企業** エンティティのワークフロー プロセスを作成して、**仕入先テーブルで仕入先を作成** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-122">Create a workflow process for the **Account** entity, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="d674a-123">**取引先企業** エンティティのワークフロー プロセスを作成して、**仕入先テーブルで仕入先を更新** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-123">Create a workflow process for the **Account** entity, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="d674a-124">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="d674a-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="d674a-125">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![バックグラウンド ワークフロー ボタンへの変換](media/background_workflow.png)

6. <span data-ttu-id="d674a-127">**取引先企業** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **組織** タイプの仕入先情報を保存するために **取引先企業**  エンティティの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="d674a-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** entity to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="d674a-128">個人タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="d674a-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="d674a-129">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d674a-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="d674a-130">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="d674a-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="d674a-131">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="d674a-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="d674a-132">取引先担当者テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="d674a-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="d674a-133">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="d674a-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="d674a-134">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="d674a-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="d674a-135">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="d674a-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="d674a-136">**仕入先** エンティティのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-136">Create a workflow process for the **Vendor** entity, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="d674a-137">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-137">Then select **OK**.</span></span> <span data-ttu-id="d674a-138">このワークフローでは、**連絡先** エンティティの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="d674a-138">This workflow handles the vendor creation scenario for the **Contact** entity.</span></span>
2. <span data-ttu-id="d674a-139">**仕入先** エンティティのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-139">Create a workflow process for the **Vendor** entity, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="d674a-140">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-140">Then select **OK**.</span></span> <span data-ttu-id="d674a-141">このワークフローでは、**連絡先** エンティティの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="d674a-141">This workflow handles the vendor update scenario for the **Contact** entity.</span></span>
3. <span data-ttu-id="d674a-142">**連絡先** エンティティのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-142">Create a workflow process for the **Contact** entity, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="d674a-143">**連絡先** エンティティのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-143">Create a workflow process for the **Contact** entity, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="d674a-144">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="d674a-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="d674a-145">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d674a-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="d674a-146">**連絡先** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **個人** タイプの仕入先情報を保存するために **連絡先** エンティティの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="d674a-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** entity to store information for vendors of the **Person** type.</span></span>
