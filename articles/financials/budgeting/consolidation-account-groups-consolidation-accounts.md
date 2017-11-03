---
title: "連結勘定グループおよび追加連結勘定"
description: "このトピックでは、連結勘定グループおよび追加連結勘定に関する情報、および Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での使用方法を説明します。"
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fcdaa26eb2f15bbf6f7d80bd59a54899f637a2c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a><span data-ttu-id="016f9-103">連結勘定グループおよび追加連結勘定</span><span class="sxs-lookup"><span data-stu-id="016f9-103">Consolidation account groups and additional consolidation accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="016f9-104">このトピックでは、連結勘定グループおよび追加連結勘定に関する情報、および Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition での使用方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="016f9-104">This topic provides information about consolidation account groups and additional consolidation accounts, and explains how they are used in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<a name="consolidation-account-groups"></a><span data-ttu-id="016f9-105">連結勘定グループ</span><span class="sxs-lookup"><span data-stu-id="016f9-105">Consolidation account groups</span></span>
----------------------------

<span data-ttu-id="016f9-106">連結勘定グループで、データを連結するのに使用する勘定のグループを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="016f9-106">Consolidation account groups let you create groups of the accounts that you want to use to consolidate data.</span></span> <span data-ttu-id="016f9-107">連結勘定グループは通常、政府指定の勘定科目表を表すか、会社の本社によって定義されるグループにアカウントをマップします。</span><span class="sxs-lookup"><span data-stu-id="016f9-107">Most often, a consolidation account group represents a government-mandated chart of accounts or maps accounts to a group that is defined by the company's headquarters.</span></span> <span data-ttu-id="016f9-108">[**連結**] モジュールの [**設定**] 領域で連結勘定グループを検索できます。</span><span class="sxs-lookup"><span data-stu-id="016f9-108">You can find consolidation account groups in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="016f9-109">新しいグループを追加するときに、勘定グループと名前の固有 ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="016f9-109">When you add a new group, you enter a unique identifier for the account group and a name.</span></span>

## <a name="additional-consolidation-accounts"></a><span data-ttu-id="016f9-110">追加連結勘定</span><span class="sxs-lookup"><span data-stu-id="016f9-110">Additional consolidation accounts</span></span>
<span data-ttu-id="016f9-111">連結統合で、既存の勘定科目表から連結勘定グループに勘定を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="016f9-111">Additional consolidation accounts let you assign an account from an existing chart of accounts to a consolidation account group.</span></span> <span data-ttu-id="016f9-112">その後、連結勘定の値と名前を指定できます。</span><span class="sxs-lookup"><span data-stu-id="016f9-112">You can then specify a consolidation account value and name.</span></span> 

<span data-ttu-id="016f9-113">[**連結**] モジュールの [**設定**] 領域で追加の連結勘定を検索できます。</span><span class="sxs-lookup"><span data-stu-id="016f9-113">You can find additional consolidation accounts in the **Setup** area of the **Consolidations** module.</span></span> <span data-ttu-id="016f9-114">新しい連結勘定を作成するときに、次の情報を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="016f9-114">When you create a new consolidation account, you must specify the following information:</span></span>

-   <span data-ttu-id="016f9-115">**主勘定** – このフィールドは、このページで選択した勘定科目表に基づいているすべての主勘定を示すルックアップです。</span><span class="sxs-lookup"><span data-stu-id="016f9-115">**Main account** – This field is a lookup that shows all the main accounts that are based on the chart of accounts that you selected on the page.</span></span> <span data-ttu-id="016f9-116">アカウントを選択すると、名前が [**主勘定名**] フィールドに自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="016f9-116">When you select an account, the name is automatically entered in the **Main account name** field.</span></span>
-   <span data-ttu-id="016f9-117">**連結勘定グループ** – このフィールドを使用して、勘定を割り当てるグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="016f9-117">**Consolidation account group** – Use this field to specify the group to assign the account to.</span></span> <span data-ttu-id="016f9-118">2 つの異なる方法で連結する場合、4 つすべての連結勘定グループに同じ勘定を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="016f9-118">If you consolidate in two different ways, you must add the same account to all four consolidation account groups.</span></span>
-   <span data-ttu-id="016f9-119">**連結勘定** – 連結勘定の値を入力します。</span><span class="sxs-lookup"><span data-stu-id="016f9-119">**Consolidation account** – Enter the value of the consolidation account.</span></span> <span data-ttu-id="016f9-120">この値は、勘定科目表の勘定である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="016f9-120">This value doesn't have to be an account from a chart of accounts.</span></span> <span data-ttu-id="016f9-121">必要とするどの値でも可能です。</span><span class="sxs-lookup"><span data-stu-id="016f9-121">It can be any value that you require.</span></span>
-   <span data-ttu-id="016f9-122">**連結勘定名** – 照会およびレポートに表示させる勘定の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="016f9-122">**Consolidation account name** – Enter the name of account as you want it to appear on inquiries and reports.</span></span>
-   <span data-ttu-id="016f9-123">**SAT レベル** – このフィールドは、メキシコの税務当局に取引明細書をレポートするのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="016f9-123">**SAT level** – This field is used to report account statements to the Mexican tax authorities.</span></span> 

<span data-ttu-id="016f9-124">連結勘定グループおよび追加の連結勘定の作成を終了すると、[オンラインで連結] プロセスでこのグループを選択できます。</span><span class="sxs-lookup"><span data-stu-id="016f9-124">When you've finished creating your consolidation account groups and additional consolidation accounts, you can select the group in the Consolidate online process.</span></span>


<span data-ttu-id="016f9-125">詳細については、[連結グループおよび追加の連結勘定の作成](../general-ledger/tasks/create-consolidation-groups.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="016f9-125">For more information, see [Create consolidation groups and additional consolidation accounts](../general-ledger/tasks/create-consolidation-groups.md).</span></span> 




