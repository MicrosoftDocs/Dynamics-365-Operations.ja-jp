---
title: "Project Service Automation からプロジェクト契約をプロジェクト契約に直接同期する Finance and Operations"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト契約およびプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 12/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 8d8e3268ae8c612bad87c3c6416f223219149ee6
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-contracts-and-projects-from-project-service-automation-directly-to-project-contracts-and-projects-in-finance-and-operations"></a><span data-ttu-id="764e0-103">Project Service Automation からプロジェクト契約とプロジェクトを、プロジェクト契約およびプロジェクトの Finance and Operations に直接同期します。</span><span class="sxs-lookup"><span data-stu-id="764e0-103">Synchronize project contracts and projects from Project Service Automation directly to project contracts and projects in Finance and Operations</span></span>

<span data-ttu-id="764e0-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations へプロジェクト契約およびプロジェクトを、直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="764e0-104">This topic describes the template and underlying tasks that are used to synchronize project contracts and projects directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="764e0-105">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-105">If you are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="764e0-106">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="764e0-106">Data flow for Project Service Automation to Finance and Operations</span></span>

> [!NOTE]
> <span data-ttu-id="764e0-107">Project Service Automation から Finance and Operations の統合ソリューションを使用する前に、Dynamics 365 データ統合機能についてよく理解しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-107">Before you can use the Project Service Automation to Finance and Operations integration solution, you should be familiar with the Dynamics 365 Data integration feature.</span></span>

<span data-ttu-id="764e0-108">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="764e0-108">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="764e0-109">データ統合機能で利用できる統合テンプレートは、Project Service Automation から Finance and Operations へのプロジェクト契約、プロジェクト、プロジェクト契約明細行、およびプロジェクト契約明細行のマイルストーンのデータのフローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="764e0-109">The integration template that is available with the Data integration feature enables the flow of data about project contracts, projects, project contract lines, and project contract line milestones from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="764e0-110">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="764e0-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="764e0-111">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span><span class="sxs-lookup"><span data-stu-id="764e0-111">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectsAndContractsFlow.JPG)](./media/ProjectsAndContractsFlow.JPG)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="764e0-112">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="764e0-112">Templates and tasks</span></span>

<span data-ttu-id="764e0-113">使用可能なテンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="764e0-113">To access the available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="764e0-114">次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations へプロジェクト契約とプロジェクトを同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-114">The following template and underlying tasks are used to synchronize project contracts and projects from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="764e0-115">**データ統合でのテンプレートの名前:** プロジェクトおよび契約 (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="764e0-115">**Name of the template in Data integration:** Projects and contracts (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="764e0-116">**プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="764e0-116">**Name of the tasks in the project:**</span></span>

  - <span data-ttu-id="764e0-117">プロジェクト契約は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="764e0-117">Project contracts PSA to Fin and Ops</span></span>
  - <span data-ttu-id="764e0-118">プロジェクトは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="764e0-118">Projects PSA to Fin and Ops</span></span>
  - <span data-ttu-id="764e0-119">プロジェクト契約明細行は Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="764e0-119">Project contract lines PSA to Fin and Ops</span></span>
  - <span data-ttu-id="764e0-120">プロジェクト契約明細行のマイルストーンは Project Service Automation から Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="764e0-120">Project contract line milestones PSA to Fin and Ops</span></span>

<span data-ttu-id="764e0-121">プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-121">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>

## <a name="entity-set"></a><span data-ttu-id="764e0-122">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="764e0-122">Entity set</span></span>

| <span data-ttu-id="764e0-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="764e0-123">Project Service Automation</span></span>       | <span data-ttu-id="764e0-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="764e0-124">Finance and Operations</span></span>                                 |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="764e0-125">注文</span><span class="sxs-lookup"><span data-stu-id="764e0-125">Orders</span></span>                           | <span data-ttu-id="764e0-126">プロジェクト契約の統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="764e0-126">Integration entity for project contract.</span></span>                |
| <span data-ttu-id="764e0-127">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="764e0-127">Projects</span></span>                         | <span data-ttu-id="764e0-128">プロジェクトの統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="764e0-128">Integration entity for project.</span></span>                         |
| <span data-ttu-id="764e0-129">注文明細行</span><span class="sxs-lookup"><span data-stu-id="764e0-129">Order lines</span></span>                      | <span data-ttu-id="764e0-130">プロジェクト契約明細行の統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="764e0-130">Integration entity for project contract line.</span></span>          |
| <span data-ttu-id="764e0-131">プロジェクト契約明細行のマイルストーン</span><span class="sxs-lookup"><span data-stu-id="764e0-131">Project contract line milestones</span></span> | <span data-ttu-id="764e0-132">プロジェクト契約明細行のマイルストーンの統合エンティティ。</span><span class="sxs-lookup"><span data-stu-id="764e0-132">Integration entity for project contract line milestone.</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="764e0-133">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="764e0-133">Entity flow</span></span>

<span data-ttu-id="764e0-134">プロジェクト契約は Project Service Automation で管理され、プロジェクト契約として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-134">Project contracts are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contracts.</span></span> <span data-ttu-id="764e0-135">統合テンプレートの一部として、プロジェクト契約の Finance and Operations で統合ソースを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="764e0-135">As part of the integration template, you can set the integration source in Finance and Operations for the project contract.</span></span>

<span data-ttu-id="764e0-136">時間、実費払い、固定価格プロジェクトは Project Service Automation で管理され、プロジェクトとして Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-136">Time and material and fixed price projects are managed in Project Service Automation, and they are synchronized to Finance and Operations as projects.</span></span> <span data-ttu-id="764e0-137">テンプレート統合の一部として、プロジェクトの Finance and Operations で統合ソースを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="764e0-137">As part of the template integration, you can set the integration source in Finance and Operations for the project.</span></span>

<span data-ttu-id="764e0-138">プロジェクト契約明細行は Project Service Automation で管理され、プロジェクト契約の請求ルールとして Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-138">Project contract lines are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rules.</span></span> <span data-ttu-id="764e0-139">請求方法が既定のプロジェクト タイプと異なる場合、契約明細行プロジェクトおよびプロジェクト グループのプロジェクト タイプは同期し更新されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-139">The synchronization will update the project type for the contract line project and project group if the billing method is different than the default project type.</span></span>

<span data-ttu-id="764e0-140">プロジェクト契約明細行のマイルストーンは Project Service Automation で管理され、プロジェクト契約の請求ルールのマイルストーンとして Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-140">Project contract line milestones are managed in Project Service Automation, and they are synchronized to Finance and Operations as project contract billing rule milestones.</span></span>

## <a name="project-service-automation-to-finance-and-operations-integration-solution"></a><span data-ttu-id="764e0-141">Finance and Operations 統合ソリューションと Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="764e0-141">Project Service Automation to Finance and Operations integration solution</span></span>

<span data-ttu-id="764e0-142">**プロジェクト契約 ID** フィールドは**プロジェクト契約**ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="764e0-142">The **Project contract ID** field is available on the **Project contracts** page.</span></span> <span data-ttu-id="764e0-143">このフィールドは統合をサポートするための自然で固有のキーとなっています。</span><span class="sxs-lookup"><span data-stu-id="764e0-143">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="764e0-144">新しいプロジェクト契約が作成され、**プロジェクト契約 ID** 値が存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-144">When a new project contract is created, if a **Project contract ID** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="764e0-145">値は **ORD** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。</span><span class="sxs-lookup"><span data-stu-id="764e0-145">The value consists of **ORD** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="764e0-146">次に例を示します: **ORD-01022-Z4M9Q0**。</span><span class="sxs-lookup"><span data-stu-id="764e0-146">Here is an example: **ORD-01022-Z4M9Q0**.</span></span>

<span data-ttu-id="764e0-147">**プロジェクト番号**フィールドは、**プロジェクト** ページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="764e0-147">The **Project Number** field is available on the **Projects** page.</span></span> <span data-ttu-id="764e0-148">このフィールドは統合をサポートするための自然で固有のキーとなっています。</span><span class="sxs-lookup"><span data-stu-id="764e0-148">This field has been made a natural and unique key to support the integration.</span></span>

<span data-ttu-id="764e0-149">新しいプロジェクトが作成され、**プロジェクト番号**値が存在しない場合、番号順序を使用して自動的に生成されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-149">When a new project is created, if a **Project Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="764e0-150">値は **PRJ** で構成され、インクリメント番号順序、次に 6 文字の接尾語が続きます。</span><span class="sxs-lookup"><span data-stu-id="764e0-150">The value consists of **PRJ** followed by an incrementing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="764e0-151">次に例を示します: **PRJ-01049-CCNID0**。</span><span class="sxs-lookup"><span data-stu-id="764e0-151">Here is an example: **PRJ-01049-CCNID0**.</span></span>

<span data-ttu-id="764e0-152">Project Service Automation から Finance and Operations 統合ソリューションを適用した場合<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>、アップグレード スクリプトは既存のプロジェクト契約の**プロジェクト契約 ID** フィールドおよび Project Service Automation の既存のプロジェクトの**プロジェクト番号**フィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="764e0-152">When the Project Service Automation to Finance and Operations integration solution is applied<TO DO: link in the top level document link where we will be adding the instructions for applying the PSA solution>, an upgrade script sets the **Project contract ID** field for existing project contracts and the **Project Number** field for existing projects in Project Service Automation.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="764e0-153">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="764e0-153">Prerequisites and mapping setup</span></span>

- <span data-ttu-id="764e0-154">プロジェクト契約とプロジェクトの同期を行う前に、勘定を同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-154">Before synchronization of project contracts and projects can occur, you must synchronize accounts.</span></span>
- <span data-ttu-id="764e0-155">接続の設定、**msdyn\_organizationalunits** の統合キー フィールドのマッピングを **msdyn\_名前\[名前\]** へ追加します。</span><span class="sxs-lookup"><span data-stu-id="764e0-155">In your connection set, add an integration key field mapping for **msdyn\_organizationalunits** to **msdyn\_name \[Name\]**.</span></span> <span data-ttu-id="764e0-156">まず最初に、接続の設定にプロジェクトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-156">You might first have to add a project to the connection set.</span></span> <span data-ttu-id="764e0-157">統合キーの詳細情報については、Dynamics 365 データ統合を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764e0-157">For more information about integration keys, see Dynamics 365 Data integration.</span></span>
- <span data-ttu-id="764e0-158">接続の設定、**msdyn\_プロジェクト**の統合キー フィールドのマッピングを **msdynce\_projectnumber \[プロジェクト番号\]** へ追加します。</span><span class="sxs-lookup"><span data-stu-id="764e0-158">In your connection set, add an integration key field mapping for **msdyn\_projects** to **msdynce\_projectnumber \[Project Number\]**.</span></span> <span data-ttu-id="764e0-159">まず最初に、接続の設定にプロジェクトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-159">You might first have to add a project to the connection set.</span></span> <span data-ttu-id="764e0-160">統合キーの詳細情報については、Dynamics 365 データ統合を参照してください。</span><span class="sxs-lookup"><span data-stu-id="764e0-160">For more information about integration keys, see Dynamics 365 Data integration.</span></span>
- <span data-ttu-id="764e0-161">**SourceDataID** のプロジェクト契約およびプロジェクトは異なる値に更新、またはマッピングから削除することができます。</span><span class="sxs-lookup"><span data-stu-id="764e0-161">**SourceDataID** for project contracts and projects can be updated to a different value or removed from the mapping.</span></span> <span data-ttu-id="764e0-162">既定のテンプレート値は **Project Service Automation** です。</span><span class="sxs-lookup"><span data-stu-id="764e0-162">The default template value is **Project Service Automation**.</span></span>
- <span data-ttu-id="764e0-163">**PaymentTerms** マッピングは、Finance and Operations で有効な支払条件が反映できるように更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-163">The **PaymentTerms** mapping must be updated so that it reflects valid terms of payment in Finance and Operations.</span></span> <span data-ttu-id="764e0-164">プロジェクト タスクからマッピングを削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="764e0-164">You can also remove the mapping from the project task.</span></span> <span data-ttu-id="764e0-165">既定値のマップにはデモ データの既定値があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-165">The default value map has default values for demo data.</span></span> <span data-ttu-id="764e0-166">次のテーブルでは、Project Service Automation の値を示します。</span><span class="sxs-lookup"><span data-stu-id="764e0-166">The following table shows the values in Project Service Automation.</span></span>

    | <span data-ttu-id="764e0-167">先頭値</span><span class="sxs-lookup"><span data-stu-id="764e0-167">Value</span></span> | <span data-ttu-id="764e0-168">説明</span><span class="sxs-lookup"><span data-stu-id="764e0-168">Description</span></span>   |
    |-------|---------------|
    | <span data-ttu-id="764e0-169">1</span><span class="sxs-lookup"><span data-stu-id="764e0-169">1</span></span>     | <span data-ttu-id="764e0-170">正味 30</span><span class="sxs-lookup"><span data-stu-id="764e0-170">Net 30</span></span>        |
    | <span data-ttu-id="764e0-171">2</span><span class="sxs-lookup"><span data-stu-id="764e0-171">2</span></span>     | <span data-ttu-id="764e0-172">2%10, 正味 30</span><span class="sxs-lookup"><span data-stu-id="764e0-172">2% 10, Net 30</span></span> |
    | <span data-ttu-id="764e0-173">3</span><span class="sxs-lookup"><span data-stu-id="764e0-173">3</span></span>     | <span data-ttu-id="764e0-174">正味 45</span><span class="sxs-lookup"><span data-stu-id="764e0-174">Net 45</span></span>        |
    | <span data-ttu-id="764e0-175">4</span><span class="sxs-lookup"><span data-stu-id="764e0-175">4</span></span>     | <span data-ttu-id="764e0-176">正味 60</span><span class="sxs-lookup"><span data-stu-id="764e0-176">Net 60</span></span>        |

## <a name="power-query"></a><span data-ttu-id="764e0-177">Power Query</span><span class="sxs-lookup"><span data-stu-id="764e0-177">Power Query</span></span>
<span data-ttu-id="764e0-178">次の条件が満たされた場合、フィルター処理する Microsoft Power Query を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-178">You must use Microsoft Power Query to filter data if the following conditions are met:</span></span>

- <span data-ttu-id="764e0-179">Microsoft Dynamics 365 for Sales の販売注文があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-179">You have sales orders in Microsoft Dynamics 365 for Sales.</span></span>
- <span data-ttu-id="764e0-180">Project Service Automation に複数の組織単位があり、これらの組織単位は Finance and Operations の複数の法人にマップされます。</span><span class="sxs-lookup"><span data-stu-id="764e0-180">You have multiple organizational units in Project Service Automation, and these organizational units will be mapped to multiple legal entities in Finance and Operations.</span></span>

<span data-ttu-id="764e0-181">Power Query を使用する必要がある場合は、これらのガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="764e0-181">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="764e0-182">プロジェクト契約 (Project Service Automation から Finance and Operations) テンプレートは**作業項目 (msdyn\_ordertype = 192350001)** タイプの販売注文のみを含む既定のフィルターです。</span><span class="sxs-lookup"><span data-stu-id="764e0-182">The Project contracts (PSA to Fin and Ops) template has a default filter that includes only sales orders of the **Work item (msdyn\_ordertype = 192350001)** type.</span></span> <span data-ttu-id="764e0-183">このフィルターでは、Finance and Operations での販売注文のプロジェクト契約が作成されていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="764e0-183">This filter ensures that project contracts aren't created for sales orders in Finance and Operations.</span></span> <span data-ttu-id="764e0-184">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-184">If you create your own template, you must add this filter.</span></span>
- <span data-ttu-id="764e0-185">統合接続セットの法人に同期させる必要がある契約組織のみを含む Power Query フィルターを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-185">You must create a Power Query filter that includes only the contract organizations that should be synchronized to the legal entity of the integration connection set.</span></span> <span data-ttu-id="764e0-186">Contoso 米国の契約組織単位とプロジェクト契約した USSI 法人に同期させる必要がありますが、Contoso グローバルの契約組織単位であるプロジェクト契約は USMF 法人に同期させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="764e0-186">For example, project contracts that you have with the contract organizational unit of Contoso US should be synchronized to the USSI legal entity, but project contracts that you have with the contract organizational unit of Contoso Global should be synchronized to the USMF legal entity.</span></span> <span data-ttu-id="764e0-187">このフィルターをタスクのマッピングに追加しない場合、すべてのプロジェクト契約は契約組織単位に関係なく、接続セットに対して定義されている法人に同期されます。</span><span class="sxs-lookup"><span data-stu-id="764e0-187">If you don't add this filter to your task mapping, all project contracts will be synchronized to the legal entity that is defined for the connection set,  regardless of the contract organizational unit.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="764e0-188">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="764e0-188">Template mapping in Data integration</span></span>

> [!NOTE] 
> <span data-ttu-id="764e0-189">**CustomerReference**、**AddressCity**、**AddressCountryRegionID**、**AddressDescription**、**AddressLine1**、**AddressLine2**、**AddressState**、および **AddressZipCode** フィールドは、プロジェクト契約の既定のマッピングに含まれません。</span><span class="sxs-lookup"><span data-stu-id="764e0-189">The **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState**, and **AddressZipCode** fields aren't included in the default mapping for project contracts.</span></span> <span data-ttu-id="764e0-190">プロジェクト契約のこのデータを同期することが必要な場合に、マッピングを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="764e0-190">You can add the mappings if you require that this data be synchronized for project contracts.</span></span>
> <span data-ttu-id="764e0-191">**説明**、**ParentID**、**ProjectGroup**、**ProjectManagerPersonnelNumber**、および **ProjectType** フィールドは、プロジェクトの既定のマッピングに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="764e0-191">The **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber**, and **ProjectType** fields aren't included in the default mapping for projects.</span></span> <span data-ttu-id="764e0-192">プロジェクトのこのデータを同期することが必要な場合に、マッピングを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="764e0-192">You can add the mappings if you require that this data be synchronized for projects.</span></span>

<span data-ttu-id="764e0-193">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="764e0-193">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="764e0-194">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="764e0-194">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="764e0-195">[![テンプレートのマッピング](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="764e0-195">[![Template mapping](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)</span></span>

<span data-ttu-id="764e0-196">[![テンプレートのマッピング](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="764e0-196">[![Template mapping](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)</span></span>

<span data-ttu-id="764e0-197">[![テンプレートのマッピング](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="764e0-197">[![Template mapping](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)</span></span>

<span data-ttu-id="764e0-198">[![テンプレートのマッピング](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span><span class="sxs-lookup"><span data-stu-id="764e0-198">[![Template mapping](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)</span></span>

