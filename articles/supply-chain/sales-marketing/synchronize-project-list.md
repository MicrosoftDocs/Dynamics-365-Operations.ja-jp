---
title: "Finance and Operations から Field Service へのプロジェクト リストの同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: ja-jp
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="30061-103">Finance and Operations から Field Service へのプロジェクト リストの同期</span><span class="sxs-lookup"><span data-stu-id="30061-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="30061-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="30061-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="30061-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="30061-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="30061-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="30061-106">Templates and tasks</span></span>
<span data-ttu-id="30061-107">次のテンプレートおよび基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30061-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="30061-108">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="30061-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="30061-109">プロジェクト (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="30061-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="30061-110">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="30061-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="30061-111">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="30061-111">Projects</span></span>

<span data-ttu-id="30061-112">プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="30061-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="30061-113">勘定 (Sales から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="30061-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="30061-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="30061-114">Entity set</span></span>
<span data-ttu-id="30061-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="30061-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="30061-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="30061-116">Field Service</span></span>           | <span data-ttu-id="30061-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="30061-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="30061-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="30061-118">msdynce_externalprojects</span></span> | <span data-ttu-id="30061-119">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="30061-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="30061-120">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="30061-120">Entity flow</span></span>
<span data-ttu-id="30061-121">Finance and Operations にプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="30061-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="30061-122">処理中のプロジェクトと**プロジェクト タイプ**時間、原材料および**プロジェクト ステージ**は、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の**外部プロジェクト** エンティティに同期されます。</span><span class="sxs-lookup"><span data-stu-id="30061-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="30061-123">**外部プロジェクト**のリストは、Field Service のワーク オーダーと Finance and Operations のプロジェクトをペアリングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="30061-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="30061-124">Field Service CRM ソリューション 外部プロジェクトは、Operations からすべてのプロジェクトを取得する新しいエンティティです。</span><span class="sxs-lookup"><span data-stu-id="30061-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="30061-125">外部プロジェクト フィールドが、ワーク オーダー エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="30061-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="30061-126">このフィールドはルックアップで、ワーク オーダーとプロジェクトのタグ付けを購入し、それから販売注文は Operations によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="30061-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="30061-127">システム ステータスがオープンに変わった場合 - 上位のステータスへの Progress(690,970,000) で、外部プロジェクト フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="30061-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="30061-128">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="30061-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="30061-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="30061-129">In Finance and Operations</span></span>
<span data-ttu-id="30061-130">データ エンティティ プロジェクトの変更追跡を有効化</span><span class="sxs-lookup"><span data-stu-id="30061-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="30061-131">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="30061-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="30061-132">プロジェクト (Finance and Operations から Field Service): プロジェクト</span><span class="sxs-lookup"><span data-stu-id="30061-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="30061-133">[![データ統合のテンプレートのマッピング](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="30061-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

