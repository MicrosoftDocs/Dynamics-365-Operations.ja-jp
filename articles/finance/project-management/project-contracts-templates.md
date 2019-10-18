---
title: プロジェクト契約およびプロジェクトを Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト契約とプロジェクトを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 76c62f3a503ff2a8c93143390fc91ef81fbf7d0f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250464"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c583b-103">プロジェクト契約およびプロジェクトを Project Service Automation から Finance and Operations に直接同期します</span><span class="sxs-lookup"><span data-stu-id="c583b-103">Synchronize project contracts and projects directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c583b-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト契約とプロジェクトを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c583b-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE] 
> <span data-ttu-id="c583b-105">Enterprise edition 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-105">If you're using Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c583b-106">Project Service Automation から Finance のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="c583b-106">Data flow for Project Service Automation to Finance</span></span>

> [!NOTE]
> <span data-ttu-id="c583b-107">Project Service Automation から Finance への統合ソリューションを使用する前に、Dynamics 365 データ統合機能についてよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-107">Before you can use the Project Service Automation to Finance integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="c583b-108">Project Service Automation の Finance への統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="c583b-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c583b-109">データ統合機能で利用できる統合テンプレートは、Project Service Automation から Finance へのプロジェクト契約、プロジェクト、プロジェクト契約明細行、およびプロジェクト契約明細行のマイルストーンのデータのフローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c583b-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c583b-110">次の図は、データが Project Service Automation と Finance との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c583b-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c583b-111">[![Project Service Automation と Finance の統合のデータ フロー](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="c583b-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c583b-112">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="c583b-112">Templates and tasks</span></span>

<span data-ttu-id="c583b-113">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="c583b-113">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c583b-114">次のテンプレートおよび基本的なタスクは Project Service Automation から Finance へプロジェクト契約とプロジェクトを同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-114">The following templates and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance:</span></span>

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a><span data-ttu-id="c583b-115">Dynamics 365 Project Service Automation v2.x との統合</span><span class="sxs-lookup"><span data-stu-id="c583b-115">Integrating with Dynamics 365 Project Service Automation v2.x</span></span>
- <span data-ttu-id="c583b-116">**データ統合でのテンプレートの名前:** プロジェクトおよび契約 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="c583b-116">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c583b-117">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="c583b-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c583b-118">プロジェクト契約は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-118">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-119">プロジェクトは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-119">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-120">プロジェクト契約明細行は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-120">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-121">プロジェクト契約明細行のマイルストーンは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-121">Project contract line milestones PSA to Fin and Ops</span></span>
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a><span data-ttu-id="c583b-122">Dynamics 365 Project Service Automation v3.x との統合</span><span class="sxs-lookup"><span data-stu-id="c583b-122">Integrating with Dynamics 365 Project Service Automation v3.x</span></span>
<span data-ttu-id="c583b-123">Project Service Automation にはスキーマの変更があり、プロジェクト契約明細行のマイルストーン テンプレートに影響します。Project Service Automation v3.x を Dynamics 365 と統合するには、テンプレートの v2 バージョンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-123">There is a schema change in Project Service Automation that impacts the Project contract line milestone template and use of the v2 version of the template is required to integrate Project Service Automation v3.x with Dynamics 365.</span></span>

- <span data-ttu-id="c583b-124">**データ統合でのテンプレートの名前:** プロジェクトおよび契約 (Project Service Automation 3.x から Finance and Operations) - v2</span><span class="sxs-lookup"><span data-stu-id="c583b-124">**Name of the template in Data integration:** Projects and Contracts (PSA 3.x to Fin and Ops) - v2</span></span>
- <span data-ttu-id="c583b-125">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="c583b-125">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c583b-126">プロジェクト契約は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-126">Project contracts PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-127">プロジェクトは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-127">Projects PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-128">プロジェクト契約明細行は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-128">Project contract lines PSA to Fin and Ops</span></span>
    - <span data-ttu-id="c583b-129">プロジェクト契約明細行のマイルストーンは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c583b-129">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="c583b-130">プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-130">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="c583b-131">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="c583b-131">Entity set</span></span>

| <span data-ttu-id="c583b-132">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c583b-132">Project Service Automation</span></span>       | <span data-ttu-id="c583b-133">財務</span><span class="sxs-lookup"><span data-stu-id="c583b-133">Finance</span></span>                                                |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="c583b-134">注文</span><span class="sxs-lookup"><span data-stu-id="c583b-134">Orders</span></span>                           | <span data-ttu-id="c583b-135">プロジェクト契約の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="c583b-135">Integration entity for project contract</span></span>                |
| <span data-ttu-id="c583b-136">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="c583b-136">Projects</span></span>                         | <span data-ttu-id="c583b-137">プロジェクトの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="c583b-137">Integration entity for project</span></span>                         |
| <span data-ttu-id="c583b-138">注文明細行</span><span class="sxs-lookup"><span data-stu-id="c583b-138">Order lines</span></span>                      | <span data-ttu-id="c583b-139">プロジェクト契約明細行の統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="c583b-139">Integration entity for project contract line</span></span>           |
| <span data-ttu-id="c583b-140">プロジェクト契約明細行のマイルストーン</span><span class="sxs-lookup"><span data-stu-id="c583b-140">Project contract line milestones</span></span> | <span data-ttu-id="c583b-141">プロジェクト契約明細行のマイルス トーンの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="c583b-141">Integration entity for project contract line milestone</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c583b-142">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="c583b-142">Entity flow</span></span>

<span data-ttu-id="c583b-143">プロジェクト契約は Project Service Automation で管理され、プロジェクト契約として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-143">Project contracts are managed in Project Service Automation, and they are synchronized to Finance as project contracts.</span></span> <span data-ttu-id="c583b-144">統合テンプレートの一部として、プロジェクト契約の Finance で統合ソースを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c583b-144">As part of the integration template, you can set the integration source in Finance for the project contract.</span></span>

<span data-ttu-id="c583b-145">時間/実費払いプロジェクト、固定価格プロジェクトは Project Service Automation で管理され、プロジェクトとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-145">Time and material project and Fixed price projects are managed in Project Service Automation, and they are synchronized to Finance as projects.</span></span> <span data-ttu-id="c583b-146">テンプレート統合の一部として、プロジェクトの Finance で統合ソースを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c583b-146">As part of the template integration, you can set the integration source in Finance for the project.</span></span>

<span data-ttu-id="c583b-147">プロジェクト契約明細行は Project Service Automation で管理され、プロジェクト契約の請求ルールとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-147">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rules.</span></span> <span data-ttu-id="c583b-148">請求方法が既定のプロジェクト タイプと異なる場合、契約明細行プロジェクトおよびプロジェクト グループのプロジェクト タイプは同期更新されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-148">If the billing method differs from the default project type, the synchronization updates the project type for the contract line project and project group.</span></span>

<span data-ttu-id="c583b-149">プロジェクト契約明細行のマイルストーンは Project Service Automation で管理され、プロジェクト契約の請求ルールのマイルストーンとして Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-149">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-integration-solution"></a><span data-ttu-id="c583b-150">Finance統合ソリューション に対する Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c583b-150">Project Service Automation to Finance integration solution</span></span>

<span data-ttu-id="c583b-151">**プロジェクト契約 ID** フィールドは**プロジェクト契約**ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="c583b-151">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="c583b-152">このフィールドは統合をサポートするための自然で固有のキーとなっています。</span><span class="sxs-lookup"><span data-stu-id="c583b-152">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="c583b-153">新しいプロジェクト契約が作成され、**プロジェクト契約 ID** 値が存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-153">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="c583b-154">値は **ORD** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。</span><span class="sxs-lookup"><span data-stu-id="c583b-154">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c583b-155">次に例を示します: **ORD-01022-Z4M9Q0**。</span><span class="sxs-lookup"><span data-stu-id="c583b-155">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="c583b-156">**プロジェクト番号**フィールドは、**プロジェクト** ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="c583b-156">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="c583b-157">このフィールドは統合をサポートするための自然で固有のキーとなっています。</span><span class="sxs-lookup"><span data-stu-id="c583b-157">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="c583b-158">新しいプロジェクトが作成され、**プロジェクト番号**値が存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-158">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="c583b-159">値は **PRJ** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。</span><span class="sxs-lookup"><span data-stu-id="c583b-159">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="c583b-160">次に例を示します: **PRJ-01049-CCNID0**。</span><span class="sxs-lookup"><span data-stu-id="c583b-160">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="c583b-161">Project Service Automation から Finance 統合ソリューションを適用した場合、アップグレート スクリプトは、既存のプロジェクト契約の**プロジェクト契約 ID** フィールドおよび Project Service Automation の既存のプロジェクトの**プロジェクト番号**フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="c583b-161">When the Project Service Automation to Finance integration solution is applied, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c583b-162">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="c583b-162">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="c583b-163">プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-163">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="c583b-164">接続の設定、**msdyn\_organizationalunits** の統合キー フィールドのマッピングを **msdyn\_名前\[名前\]** へ追加します。</span><span class="sxs-lookup"><span data-stu-id="c583b-164">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="c583b-165">最初に、接続の設定にプロジェクトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-165">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="c583b-166">詳細については、[Common Data Service for Apps へのデータ統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c583b-166">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="c583b-167">接続の設定、**msdyn\_プロジェクト**の統合キー フィールドのマッピングを **msdynce\_projectnumber \[プロジェクト番号\]** へ追加します。</span><span class="sxs-lookup"><span data-stu-id="c583b-167">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="c583b-168">最初に、接続の設定にプロジェクトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-168">You might first need to add a project to the connection set.</span></span> <span data-ttu-id="c583b-169">詳細については、[Common Data Service for Apps へのデータ統合](https://docs.microsoft.com/powerapps/administrator/data-integrator)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c583b-169">For more information, see [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>
- <span data-ttu-id="c583b-170">**SourceDataID** のプロジェクト契約およびプロジェクトは異なる値に更新、またはマッピングから削除することができます。</span><span class="sxs-lookup"><span data-stu-id="c583b-170">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="c583b-171">既定のテンプレート値は **Project Service Automation** です。</span><span class="sxs-lookup"><span data-stu-id="c583b-171">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="c583b-172">**PaymentTerms** マッピングは、Finance で有効な支払条件が反映できるように更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-172">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance.</span></span> <span data-ttu-id="c583b-173">プロジェクト タスクからマッピングを削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="c583b-173">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="c583b-174">既定値のマップにはデモ データの既定値があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-174">The default value map has default values for demo data.</span></span> <span data-ttu-id="c583b-175">次のテーブルでは、Project Service Automation の値を示します。</span><span class="sxs-lookup"><span data-stu-id="c583b-175">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="c583b-176">先頭値</span><span class="sxs-lookup"><span data-stu-id="c583b-176">Value</span></span> | <span data-ttu-id="c583b-177">説明</span><span class="sxs-lookup"><span data-stu-id="c583b-177">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="c583b-178">1</span><span class="sxs-lookup"><span data-stu-id="c583b-178">1</span></span>     | <span data-ttu-id="c583b-179">正味 30</span><span class="sxs-lookup"><span data-stu-id="c583b-179">Net 30</span></span>        |
    | <span data-ttu-id="c583b-180">2</span><span class="sxs-lookup"><span data-stu-id="c583b-180">2</span></span>     | <span data-ttu-id="c583b-181">2 10、正味 30</span><span class="sxs-lookup"><span data-stu-id="c583b-181">2% 10, Net 30</span></span> |
    | <span data-ttu-id="c583b-182">3</span><span class="sxs-lookup"><span data-stu-id="c583b-182">3</span></span>     | <span data-ttu-id="c583b-183">正味 45</span><span class="sxs-lookup"><span data-stu-id="c583b-183">Net 45</span></span>        |
    | <span data-ttu-id="c583b-184">4</span><span class="sxs-lookup"><span data-stu-id="c583b-184">4</span></span>     | <span data-ttu-id="c583b-185">正味 60</span><span class="sxs-lookup"><span data-stu-id="c583b-185">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="c583b-186">Power Query</span><span class="sxs-lookup"><span data-stu-id="c583b-186">Power Query</span></span>

<span data-ttu-id="c583b-187">次の条件が満たされた場合、フィルター処理する Microsoft Power Query for Excel を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-187">You must use Microsoft Power Query for Excel to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="c583b-188">Dynamics 365 Sales の販売注文があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-188">You have sales orders in Dynamics 365 Sales.</span></span>
- <span data-ttu-id="c583b-189">Project Service Automation に複数の組織単位があり、これらの組織単位は Finance の複数の法人にマップされます。</span><span class="sxs-lookup"><span data-stu-id="c583b-189">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance.</span></span>

<span data-ttu-id="c583b-190">Power Query を使用する必要がある場合は、これらのガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="c583b-190">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="c583b-191">プロジェクトおよび契約 (Project Service Automation から Finance and Operations) テンプレートは**作業項目 (msdyn\_ordertype = 192350001)** タイプの販売注文のみを含む既定のフィルターです。</span><span class="sxs-lookup"><span data-stu-id="c583b-191">The Projects and contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="c583b-192">このフィルターでは、Finance での販売注文のプロジェクト契約が作成されていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="c583b-192">This filter helps guarantee that project contracts aren't created for sales orders in Finance.</span></span> <span data-ttu-id="c583b-193">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-193">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="c583b-194">統合接続セットの法人に同期させる必要がある契約組織のみを含む Power Query フィルターを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-194">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="c583b-195">Contoso 米国の契約組織単位とプロジェクト契約した USSI 法人に同期させる必要がありますが、Contoso グローバルの契約組織単位であるプロジェクト契約は USMF 法人に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c583b-195">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="c583b-196">このフィルターをタスクのマッピングに追加しない場合、すべてのプロジェクト契約は契約組織単位に関係なく、接続セットに対して定義されている法人に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c583b-196">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set, regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c583b-197">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="c583b-197">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="c583b-198">**CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState**、および **AddressZipCode** フィールドは、プロジェクト契約の既定のマッピングに含まれません。</span><span class="sxs-lookup"><span data-stu-id="c583b-198">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="c583b-199">プロジェクト契約のこのデータを同期することが必要な場合に、マッピングを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c583b-199">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
>
> <span data-ttu-id="c583b-200">**説明**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber**、および **ProjectType** フィールドは、プロジェクトの既定のマッピングに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c583b-200">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="c583b-201">プロジェクトのこのデータを同期することが必要な場合に、マッピングを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="c583b-201">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="c583b-202">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="c583b-202">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="c583b-203">マッピングは、Project Service Automation から Finance に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="c583b-203">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c583b-204">[![テンプレートのマッピング](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="c583b-204">[![Template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="c583b-205">[![テンプレートのマッピング](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="c583b-205">[![Template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="c583b-206">[![テンプレートのマッピング](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="c583b-206">[![Template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="c583b-207">[![テンプレートのマッピング](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="c583b-207">[![Template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a><span data-ttu-id="c583b-208">プロジェクトおよび契約におけるプロジェクト契約明細行のマイルストーンのマッピング (Project Service Automation 3.x から Dynamics へ) - v2 テンプレート:</span><span class="sxs-lookup"><span data-stu-id="c583b-208">Project contract line milestone mapping in the Projects and Contracts (PSA 3.x to Dynamics) - v2 template:</span></span>

<span data-ttu-id="c583b-209">[![テンプレートのマッピング](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span><span class="sxs-lookup"><span data-stu-id="c583b-209">[![Template mapping](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)</span></span>
