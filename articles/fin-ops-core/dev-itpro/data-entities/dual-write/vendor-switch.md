---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Dataverse との間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 78d4c547f544d95c66490e5610374a5c4598b266
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565602"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="e5fb2-103">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="e5fb2-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="e5fb2-104">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="e5fb2-104">Vendor data flow</span></span> 

<span data-ttu-id="e5fb2-105">**取引先企業** テーブルを使用して **組織** タイプの仕入先を保存し、**連絡先** テーブルを使用して **個人** タイプの仕入先を保存する場合は、次のワークフローをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="e5fb2-106">それ以外の場合、このコンフィギュレーションは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="e5fb2-107">組織タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="e5fb2-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="e5fb2-108">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e5fb2-109">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e5fb2-110">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="e5fb2-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="e5fb2-111">仕入先テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="e5fb2-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="e5fb2-112">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="e5fb2-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="e5fb2-113">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="e5fb2-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="e5fb2-114">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e5fb2-115">**仕入先** テーブルのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を作成** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="e5fb2-116">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-116">Then select **OK**.</span></span> <span data-ttu-id="e5fb2-117">このワークフローでは、**取引先企業** テーブルの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![取引先企業テーブル ワークフロー プロセスでの仕入先の作成](media/create_process.png)

2. <span data-ttu-id="e5fb2-119">**仕入先** テーブルのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を更新** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="e5fb2-120">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-120">Then select **OK**.</span></span> <span data-ttu-id="e5fb2-121">このワークフローでは、**取引先企業** テーブルの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="e5fb2-122">**仕入先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルで取引先企業を作成** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="e5fb2-123">**取引先企業** テーブルのワークフロー プロセスを作成して、**仕入先テーブルで取引先企業を更新** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="e5fb2-124">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e5fb2-125">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![バックグラウンド ワークフロー ボタンへの変換](media/background_workflow.png)

6. <span data-ttu-id="e5fb2-127">**取引先企業** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **組織** タイプの仕入先情報を保存するために **取引先企業**  テーブルの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="e5fb2-128">個人タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="e5fb2-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="e5fb2-129">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="e5fb2-130">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="e5fb2-131">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="e5fb2-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="e5fb2-132">取引先担当者テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="e5fb2-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="e5fb2-133">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="e5fb2-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="e5fb2-134">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="e5fb2-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="e5fb2-135">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="e5fb2-136">**仕入先** テーブルのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="e5fb2-137">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-137">Then select **OK**.</span></span> <span data-ttu-id="e5fb2-138">このワークフローでは、**連絡先** テーブルの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="e5fb2-139">**仕入先** テーブルのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="e5fb2-140">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-140">Then select **OK**.</span></span> <span data-ttu-id="e5fb2-141">このワークフローでは、**連絡先** テーブルの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="e5fb2-142">**連絡先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を作成する** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="e5fb2-143">**連絡先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を更新する** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="e5fb2-144">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="e5fb2-145">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="e5fb2-146">**連絡先** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **個人** タイプの仕入先情報を保存するために **連絡先** テーブルの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="e5fb2-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]