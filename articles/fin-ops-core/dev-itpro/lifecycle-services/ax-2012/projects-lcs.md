---
title: Lifecycle Services (LCS) のプロジェクト
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトについて説明します。
author: manalidongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 18941
ms.assetid: 6634d000-b031-40d7-ad2a-c6626e4cbdc2
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c03bc864ca39a617768cad20f15edb3c9c152b09
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744801"
---
# <a name="projects-in-lifecycle-services-lcs"></a><span data-ttu-id="062d3-103">Lifecycle Services (LCS) のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="062d3-103">Projects in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="062d3-104">この記事では、Microsoft Dynamics Lifecycle Services (LCS) のプロジェクトに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="062d3-104">This article provides information about projects in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="062d3-105">いくつかの重要な機能について説明し、プロジェクト方法のロールについても説明します。</span><span class="sxs-lookup"><span data-stu-id="062d3-105">It describes some important features and also explains the role of the project methodology.</span></span>

<span data-ttu-id="062d3-106">プロジェクトは、LCS でのエクスペリエンスの主要開催者です。</span><span class="sxs-lookup"><span data-stu-id="062d3-106">Projects are the main organizer of your experience in LCS.</span></span> <span data-ttu-id="062d3-107">プロジェクトに関連する手法は、プロジェクトに含まれる既定のフェーズとタスクを決定します。</span><span class="sxs-lookup"><span data-stu-id="062d3-107">The methodology that is associated with a project determines the default phases and tasks that are included in that project.</span></span>

## <a name="key-features"></a><span data-ttu-id="062d3-108">主な機能</span><span class="sxs-lookup"><span data-stu-id="062d3-108">Key features</span></span>

| <span data-ttu-id="062d3-109">機能</span><span class="sxs-lookup"><span data-stu-id="062d3-109">Feature</span></span>              | <span data-ttu-id="062d3-110">説明</span><span class="sxs-lookup"><span data-stu-id="062d3-110">Description</span></span>                                                                                                                                                                                |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="062d3-111">対象者を招待します。</span><span class="sxs-lookup"><span data-stu-id="062d3-111">Invite who you want.</span></span> | <span data-ttu-id="062d3-112">顧客とパートナーは、お互いにプロジェクトへの参加を呼びかけることができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-112">Customers and partners can invite each other to participate in projects.</span></span> <span data-ttu-id="062d3-113">見込顧客も招待することができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-113">You also can invite prospects.</span></span> <span data-ttu-id="062d3-114">クラウド駆動のサポートを使用する場合は、Microsoft のサポート エンジニアを招待することもできます。</span><span class="sxs-lookup"><span data-stu-id="062d3-114">If you use Cloud-powered support, you can also invite Microsoft support engineers.</span></span> |
| <span data-ttu-id="062d3-115">所有権を変更します。</span><span class="sxs-lookup"><span data-stu-id="062d3-115">Change ownership.</span></span>    | <span data-ttu-id="062d3-116">必要に応じてプロジェクトの所有権を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-116">You can change the ownership of a project as you require.</span></span> <span data-ttu-id="062d3-117">たとえば、パートナーから顧客へ、または顧客の異なる人へ所有権を変更できます。</span><span class="sxs-lookup"><span data-stu-id="062d3-117">For example, you can change the ownership from a partner to a customer, or to a different person at a customer.</span></span>                  |

<span data-ttu-id="062d3-118">ご自分の実装プロジェクトの方法に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="062d3-118">You must follow the methodology in your implementation project.</span></span> <span data-ttu-id="062d3-119">方法フレームワークは、実装をガイドするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="062d3-119">The methodology framework is designed to guide you through the implementation.</span></span> <span data-ttu-id="062d3-120">LCS でアクションを実行する際は、フェーズとタスクを完了としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-120">As you perform actions in LCS, you can begin to mark the phases and tasks as completed.</span></span> <span data-ttu-id="062d3-121">ロックされた方法タスクは、前提条件を完了した後に完了としてマークすることができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-121">Locked methodology tasks can be marked as completed after you complete the prerequisite.</span></span> <span data-ttu-id="062d3-122">ロック アイコンをクリックして、タスクを完了とマークする前に何を終了する必要があるか知ることができます。</span><span class="sxs-lookup"><span data-stu-id="062d3-122">You can click the lock icon to learn what you must complete before you can mark a task as completed.</span></span> <span data-ttu-id="062d3-123">方法論のフェーズとタスクに従って作業すると、環境を構成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="062d3-123">As you work through the phases and tasks in the methodology, environments become available for you to configure.</span></span> 

## <a name="delete-a-project"></a><span data-ttu-id="062d3-124">プロジェクトの削除</span><span class="sxs-lookup"><span data-stu-id="062d3-124">Delete a project</span></span> 
<span data-ttu-id="062d3-125">LCS を開くと、最新のプロジェクトに関する表示が得られます。</span><span class="sxs-lookup"><span data-stu-id="062d3-125">When you have LCS opened, you have a view on recent projects.</span></span> <span data-ttu-id="062d3-126">「すべてのプロジェクト」オプションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="062d3-126">Click the option 'All projects'.</span></span> <span data-ttu-id="062d3-127">次に、リスト スタイル内のすべてのプロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="062d3-127">You then have a view on all projects in a list style.</span></span> <span data-ttu-id="062d3-128">プロジェクトを選択し、Trashbin アイコンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="062d3-128">Select a project and click the Trashbin icon.</span></span> <span data-ttu-id="062d3-129">関連するすべての情報を含むプロジェクトは削除されます。</span><span class="sxs-lookup"><span data-stu-id="062d3-129">The project with all related information will be deleted.</span></span>





[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]