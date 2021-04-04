---
title: Supply Chain Management から Field Service へのプロジェクト リストの同期
description: このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 3d17b226cabd0668bcdb52e9a7fdfc5973fe49b9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243060"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="96edf-103">Supply Chain Management から Field Service へのプロジェクト リストの同期</span><span class="sxs-lookup"><span data-stu-id="96edf-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="96edf-104">このトピックでは、Dynamics 365 Supply Chain Management から Dynamics 365 Field Service にプロジェクトを同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="96edf-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="96edf-105">[![Supply Chain Management および Field Service 間の業務プロセスの同期](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="96edf-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="96edf-106">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="96edf-106">Templates and tasks</span></span>
<span data-ttu-id="96edf-107">次のテンプレートと基本的なタスクは、Supply Chain Management から Field Service にプロジェクトの同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96edf-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="96edf-108">**データ統合でのテンプレート**</span><span class="sxs-lookup"><span data-stu-id="96edf-108">**Template in Data integration**</span></span>
- <span data-ttu-id="96edf-109">プロジェクト (Supply Chain Management から Field Service)</span><span class="sxs-lookup"><span data-stu-id="96edf-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="96edf-110">**データ統合プロジェクトのタスク**</span><span class="sxs-lookup"><span data-stu-id="96edf-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="96edf-111">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="96edf-111">Projects</span></span>

<span data-ttu-id="96edf-112">プロジェクト リストの同期が処理される前に、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="96edf-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="96edf-113">アカウント (Sales から Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="96edf-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="96edf-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="96edf-114">Entity set</span></span>
| <span data-ttu-id="96edf-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="96edf-115">Field Service</span></span>           | <span data-ttu-id="96edf-116">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="96edf-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="96edf-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="96edf-117">msdynce_externalprojects</span></span> | <span data-ttu-id="96edf-118">プロジェクト</span><span class="sxs-lookup"><span data-stu-id="96edf-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="96edf-119">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="96edf-119">Entity flow</span></span>
<span data-ttu-id="96edf-120">プロジェクトは Supply Chain Management で作成されます。</span><span class="sxs-lookup"><span data-stu-id="96edf-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="96edf-121">**プロジェクト タイプ** を **時間、原材料** に、および **プロジェクト ステージ** を **処理中** に設定されたプロジェクトは、プロジェクト番号、プロジェクト名、プロジェクト ステージおよび顧客口座情報を含め、Field Service の **外部プロジェクト** エンティティに同期されます。</span><span class="sxs-lookup"><span data-stu-id="96edf-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="96edf-122">**外部プロジェクト** のリストは、Field Service のワーク オーダーと Supply Chain Management のプロジェクトをペアリングするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="96edf-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="96edf-123">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="96edf-123">Field Service CRM solution</span></span>
<span data-ttu-id="96edf-124">**外部プロジェクト** エンティティは、Supply Chain Management からすべてのプロジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="96edf-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="96edf-125">**外部プロジェクト** フィールドが、**ワーク オーダー** エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="96edf-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="96edf-126">これはルックアップ フィールドであるため、ワーク オーダーがプロジェクトにタグ付けられ、販売注文は Supply Chain Management によりプロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="96edf-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="96edf-127">**システム ステータス** が **オープン – 処理中 (690,970,000)** から上位のステータスへ変更した後、**外部プロジェクト** フィールドはロックされ、値の追加、削除、また変更はできなくなります。</span><span class="sxs-lookup"><span data-stu-id="96edf-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="96edf-128">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="96edf-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="96edf-129">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="96edf-129">Supply Chain Management</span></span>
<span data-ttu-id="96edf-130">データ エンティティ プロジェクトの変更追跡を有効にします。</span><span class="sxs-lookup"><span data-stu-id="96edf-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="96edf-131">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="96edf-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="96edf-132">プロジェクト (Supply Chain Management から Field Service): プロジェクト</span><span class="sxs-lookup"><span data-stu-id="96edf-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="96edf-133">[![データ統合のテンプレートのマッピング](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="96edf-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]