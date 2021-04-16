---
title: 仕入先デザインの切り替え
description: このトピックでは、Finance and Operations アプリと Dataverse との間の仕入先データの統合を切り替える方法について説明します。
author: RamaKrishnamoorthy
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
ms.openlocfilehash: 5a18fed2eac4c120dca20a1d7797d047639275b9
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750597"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="6aae8-103">仕入先デザインの切り替え</span><span class="sxs-lookup"><span data-stu-id="6aae8-103">Switch between vendor designs</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="vendor-data-flow"></a><span data-ttu-id="6aae8-104">仕入先データ フロー</span><span class="sxs-lookup"><span data-stu-id="6aae8-104">Vendor data flow</span></span> 

<span data-ttu-id="6aae8-105">**取引先企業** テーブルを使用して **組織** タイプの仕入先を保存し、**連絡先** テーブルを使用して **個人** タイプの仕入先を保存する場合は、次のワークフローをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="6aae8-105">If you choose to use the **Account** table to store vendors of the **Organization** type and the **Contact** table to store vendors of the **Person** type, configure the following workflows.</span></span> <span data-ttu-id="6aae8-106">それ以外の場合、このコンフィギュレーションは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="6aae8-106">Otherwise, this configuration isn't required.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-organization-type"></a><span data-ttu-id="6aae8-107">組織タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="6aae8-107">Use the extended vendor design for vendors of the Organization type</span></span>

<span data-ttu-id="6aae8-108">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6aae8-108">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="6aae8-109">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-109">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="6aae8-110">取引先企業テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="6aae8-110">Create Vendors in Accounts Table</span></span>
+ <span data-ttu-id="6aae8-111">仕入先テーブルでの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="6aae8-111">Create Vendors in Vendors Table</span></span>
+ <span data-ttu-id="6aae8-112">取引先企業テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="6aae8-112">Update Vendors in Accounts Table</span></span>
+ <span data-ttu-id="6aae8-113">仕入先テーブルでの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="6aae8-113">Update Vendors in Vendors Table</span></span>

<span data-ttu-id="6aae8-114">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="6aae8-114">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="6aae8-115">**仕入先** テーブルのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を作成** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-115">Create a workflow process for the **Vendor** table, and select the **Create Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="6aae8-116">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-116">Then select **OK**.</span></span> <span data-ttu-id="6aae8-117">このワークフローでは、**取引先企業** テーブルの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-117">This workflow handles the vendor creation scenario for the **Account** table.</span></span>

    ![取引先企業テーブル ワークフロー プロセスでの仕入先の作成](media/create_process.png)

2. <span data-ttu-id="6aae8-119">**仕入先** テーブルのワークフロー プロセスを作成して、**取引先企業テーブルで仕入先を更新** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-119">Create a workflow process for the **Vendor** table, and select the **Update Vendors in Accounts Table** workflow process template.</span></span> <span data-ttu-id="6aae8-120">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-120">Then select **OK**.</span></span> <span data-ttu-id="6aae8-121">このワークフローでは、**取引先企業** テーブルの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-121">This workflow handles the vendor update scenario for the **Account** table.</span></span>
3. <span data-ttu-id="6aae8-122">**仕入先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルで取引先企業を作成** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-122">Create a workflow process for the **Account** table, and select the **Create Vendors in Vendors Table** workflow process template.</span></span>
4. <span data-ttu-id="6aae8-123">**取引先企業** テーブルのワークフロー プロセスを作成して、**仕入先テーブルで取引先企業を更新** ワークフロー プロセス テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-123">Create a workflow process for the **Account** table, and select the **Update Vendors in Vendors Table** workflow process template.</span></span>
5. <span data-ttu-id="6aae8-124">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6aae8-124">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="6aae8-125">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-125">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>

    ![バックグラウンド ワークフロー ボタンへの変換](media/background_workflow.png)

6. <span data-ttu-id="6aae8-127">**取引先企業** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **組織** タイプの仕入先情報を保存するために **取引先企業**  テーブルの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-127">Activate the workflows that you created for the **Account** and **Vendor** tables to start to use the **Account** table to store information for vendors of the **Organization** type.</span></span>

## <a name="use-the-extended-vendor-design-for-vendors-of-the-person-type"></a><span data-ttu-id="6aae8-128">個人タイプの仕入先に対して拡張された仕入先設計を使用します</span><span class="sxs-lookup"><span data-stu-id="6aae8-128">Use the extended vendor design for vendors of the Person type</span></span>

<span data-ttu-id="6aae8-129">**Dynamics365FinanceExtended** ソリューション パッケージには、次のワークフロー プロセス テンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6aae8-129">The **Dynamics365FinanceExtended** solution package contains the following workflow process templates.</span></span> <span data-ttu-id="6aae8-130">各テンプレートのワークフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-130">You will create a workflow for each template.</span></span>

+ <span data-ttu-id="6aae8-131">仕入先テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="6aae8-131">Create Vendors of type Person in Vendors Table</span></span>
+ <span data-ttu-id="6aae8-132">取引先担当者テーブルでの個人タイプの仕入先の作成</span><span class="sxs-lookup"><span data-stu-id="6aae8-132">Create Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="6aae8-133">取引先担当者テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="6aae8-133">Update Vendors of type Person in Contacts Table</span></span>
+ <span data-ttu-id="6aae8-134">仕入先テーブルでの個人タイプの仕入先の更新</span><span class="sxs-lookup"><span data-stu-id="6aae8-134">Update Vendors of type Person in Vendors Table</span></span>

<span data-ttu-id="6aae8-135">ワークフロー プロセス テンプレートを使用して新しいワークフロー プロセスを作成するには、次のステップに従います。</span><span class="sxs-lookup"><span data-stu-id="6aae8-135">To create new workflow processes by using the workflow process templates, follow these steps.</span></span>

1. <span data-ttu-id="6aae8-136">**仕入先** テーブルのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を作成する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-136">Create a workflow process for the **Vendor** table, and select the **Create Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="6aae8-137">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-137">Then select **OK**.</span></span> <span data-ttu-id="6aae8-138">このワークフローでは、**連絡先** テーブルの仕入先作成シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-138">This workflow handles the vendor creation scenario for the **Contact** table.</span></span>
2. <span data-ttu-id="6aae8-139">**仕入先** テーブルのワークフロー プロセスを作成して、**連絡先テーブルでタイプが個人の仕入先を更新する** ワークフロー テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-139">Create a workflow process for the **Vendor** table, and select the **Update Vendors of type Person in Contacts Table** workflow process template.</span></span> <span data-ttu-id="6aae8-140">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-140">Then select **OK**.</span></span> <span data-ttu-id="6aae8-141">このワークフローでは、**連絡先** テーブルの仕入先更新シナリオを処理します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-141">This workflow handles the vendor update scenario for the **Contact** table.</span></span>
3. <span data-ttu-id="6aae8-142">**連絡先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を作成する** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-142">Create a workflow process for the **Contact** table, and select the **Create Vendors of type Person in Vendors Table** template.</span></span>
4. <span data-ttu-id="6aae8-143">**連絡先** テーブルのワークフロー プロセスを作成して、**仕入先テーブルでタイプが個人の仕入先を更新する** テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-143">Create a workflow process for the **Contact** table, and select the **Update Vendors of type Person in Vendors Table** template.</span></span>
5. <span data-ttu-id="6aae8-144">ワークフローは、必要に応じてリアルタイムまたはバックグラウンドのワークフローとしてコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="6aae8-144">You can configure the workflows as either real-time workflows or background workflows, depending on your requirements.</span></span> <span data-ttu-id="6aae8-145">ワークフローをバックグラウンド ワークフローとしてコンフィギュレーションするには、**バックグラウンド ワークフローに変換** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-145">To configure a workflow as a background workflow, select **Convert to a background workflow**.</span></span>
6. <span data-ttu-id="6aae8-146">**連絡先** テーブルと **仕入先** テーブルで作成したワークフローを有効にして、その **個人** タイプの仕入先情報を保存するために **連絡先** テーブルの使用を開始します。</span><span class="sxs-lookup"><span data-stu-id="6aae8-146">Activate the workflows that you created on the **Contact** and **Vendor** tables to start to use the **Contact** table to store information for vendors of the **Person** type.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]