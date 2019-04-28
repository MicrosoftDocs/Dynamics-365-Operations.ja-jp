---
title: Finance and Operations から Field Service へのプロジェクト リストの同期
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/14/2019
ms.locfileid: "842607"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="b7cef-103">Finance and Operations から Field Service へのプロジェクト リストの同期</span><span class="sxs-lookup"><span data-stu-id="b7cef-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b7cef-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b7cef-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b7cef-105">[![Finance and Operations および Field Service 間の業務プロセスの同期](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="b7cef-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="b7cef-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="b7cef-106">Templates and tasks</span></span>
<span data-ttu-id="b7cef-107">次のテンプレートと基本的なタスクは、Microsoft Dynamics 365 for Finance and Operations から Microsoft Dynamics 365 for Field Service にプロジェクトの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7cef-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="b7cef-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="b7cef-108">**Template in Data integration**</span></span>
- <span data-ttu-id="b7cef-109">プロジェクト (Finance and Operations から Field Service)</span><span class="sxs-lookup"><span data-stu-id="b7cef-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="b7cef-110">**データ統合プロジェクトのタスク**</span><span class="sxs-lookup"><span data-stu-id="b7cef-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="b7cef-111">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="b7cef-111">Projects</span></span>

<span data-ttu-id="b7cef-112">プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="b7cef-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="b7cef-113">勘定 (Sales から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="b7cef-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="b7cef-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="b7cef-114">Entity set</span></span>
| <span data-ttu-id="b7cef-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="b7cef-115">Field Service</span></span>           | <span data-ttu-id="b7cef-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7cef-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="b7cef-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="b7cef-117">msdynce_externalprojects</span></span> | <span data-ttu-id="b7cef-118">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="b7cef-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="b7cef-119">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="b7cef-119">Entity flow</span></span>
<span data-ttu-id="b7cef-120">Finance and Operations にプロジェクトが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b7cef-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="b7cef-121">**プロジェクト タイプ**を**時間、原材料**に、および**プロジェクト ステージ**を**処理中**に設定されたプロジェクトは、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の**外部プロジェクト** エンティティに同期されます。</span><span class="sxs-lookup"><span data-stu-id="b7cef-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="b7cef-122">**外部プロジェクト**のリストは、Field Service のワーク オーダーと Finance and Operations のプロジェクトをペアリングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b7cef-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="b7cef-123">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="b7cef-123">Field Service CRM solution</span></span>
<span data-ttu-id="b7cef-124">**外部プロジェクト** エンティティは、Finance and Operations からすべてのプロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="b7cef-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="b7cef-125">**外部プロジェクト** フィールドが、**ワーク オーダー** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="b7cef-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="b7cef-126">これはルックアップ フィールドであるため、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Finance and Operations によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="b7cef-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="b7cef-127">**システム ステータス**が**オープン – 処理中 (690,970,000)** から上位のステータスへ変更した後、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="b7cef-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b7cef-128">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="b7cef-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="b7cef-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b7cef-129">Finance and Operations</span></span>
<span data-ttu-id="b7cef-130">データ エンティティ プロジェクトの変更追跡を有効にします。</span><span class="sxs-lookup"><span data-stu-id="b7cef-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b7cef-131">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="b7cef-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="b7cef-132">プロジェクト (Finance and Operations から Field Service): プロジェクト</span><span class="sxs-lookup"><span data-stu-id="b7cef-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="b7cef-133">[![データ統合のテンプレートのマッピング](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="b7cef-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
