---
title: プロジェクト販売注文
description: このトピックでは、時間/実費払いプロジェクトに対するプロジェクト ベースの販売注文を作成する方法について説明します。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
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
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185500"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="d45aa-103">時間/実費払いプロジェクトに対するプロジェクト販売注文</span><span class="sxs-lookup"><span data-stu-id="d45aa-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="d45aa-104">このトピックでは、プロジェクトの販売注文を作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d45aa-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="d45aa-105">販売注文は、タイプが**時間/実費払い**のプロジェクトに対してのみ作成できます。</span><span class="sxs-lookup"><span data-stu-id="d45aa-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="d45aa-106">時間/実費払いプロジェクトがプロジェクト契約に複数の資金調達元がある場合、**プロジェクト管理および会計パラメーター**ページの**複数の資金調達元があるプロジェクトの販売注文を許可する**パラメーターを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="d45aa-107">複数の資金調達元があるプロジェクト販売注文のサポートは、アプリケーション リリース 10.0.2 以降で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="d45aa-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="d45aa-108">複数の資金調達先があるプロジェクト販売注文のサポートを有効にするためのパラメーターは 2020 年 4 月リリース ウェーブで削除されます。その後、機能は常に有効になります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="d45aa-109">プロジェクト ベースの販売注文は 2 通りの方法で作成できます。</span><span class="sxs-lookup"><span data-stu-id="d45aa-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="d45aa-110">プロジェクト自体に移動します。</span><span class="sxs-lookup"><span data-stu-id="d45aa-110">Go to the project itself.</span></span> <span data-ttu-id="d45aa-111">アクション ウィンドウで、**管理 > 品目作業 > 販売注文**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d45aa-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="d45aa-112">プロジェクト情報は、既定でプロジェクトから販売注文になります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="d45aa-113">プロジェクト契約に複数の資金調達元がある場合は、販売注文の顧客を設定する資金調達元を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="d45aa-114">プロジェクトに 1つだけ資金調達元がある場合、顧客は自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="d45aa-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="d45aa-115">**すべての販売注文**リスト ページに移動し、新しい販売注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="d45aa-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="d45aa-116">販売注文のプロジェクトを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="d45aa-117">プロジェクトを選択すると、顧客が資金調達元から設定されます。またはプロジェクト契約に複数の資金調達元がある場合は、資金調達元を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d45aa-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>
