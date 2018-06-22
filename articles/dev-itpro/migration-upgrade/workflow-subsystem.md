---
title: "Finance and Operations でのワークフロー サブシステムの更新"
description: "この記事では、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについて説明します。 Microsoft Dynamics AX 2012 以降に実装された変更について説明し、ワークフロー システムに関する詳細へのリンクも示します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 13511
ms.assetid: 0e3aa2cd-2327-45ba-bf38-0ef543fa8f67
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5a35c82fa3c7779b183c472572c9bd57272c3fc9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="workflow-subsystem-updates-in-finance-and-operations"></a><span data-ttu-id="e1f5c-104">Finance and Operations でのワークフロー サブシステムの更新</span><span class="sxs-lookup"><span data-stu-id="e1f5c-104">Workflow subsystem updates in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e1f5c-105">この記事では、Microsoft Dynamics 365 for Finance and Operations のワークフロー システムについて説明します。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-105">This article reviews the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e1f5c-106">Microsoft Dynamics AX 2012 以降に実装された変更について説明し、ワークフロー システムに関する詳細へのリンクも示します。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-106">It describes the changes that have been implemented since Microsoft Dynamics AX 2012 and also includes links to more information about the workflow system.</span></span> 

<span data-ttu-id="e1f5c-107">Microsoft Dynamics AX 2012 を使用していれば、Finance and Operations のワークフロー システムは既におなじみのものです。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-107">The workflow system in Finance and Operations will already be familiar to you if you've used Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="e1f5c-108">Microsoft Dynamics AX 2012 のワークフロー サブシステムの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-108">For more information about the workflow subsystem in Dynamics AX 2012, see the following topics.</span></span>

| <span data-ttu-id="e1f5c-109">このテーマについて学ぶには</span><span class="sxs-lookup"><span data-stu-id="e1f5c-109">To learn about this subject</span></span> | <span data-ttu-id="e1f5c-110">このトピックを参照</span><span class="sxs-lookup"><span data-stu-id="e1f5c-110">See this topic</span></span>                                             |
|-----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e1f5c-111">ワークフロー システム</span><span class="sxs-lookup"><span data-stu-id="e1f5c-111">The workflow system</span></span>         | <http://technet.microsoft.com/en-us/library/dd309672.aspx> |
| <span data-ttu-id="e1f5c-112">モジュールごとのワークフロー タイプ</span><span class="sxs-lookup"><span data-stu-id="e1f5c-112">Workflow types by module</span></span>    | <http://technet.microsoft.com/EN-US/library/dd362043.aspx> |
| <span data-ttu-id="e1f5c-113">ワークフロー要素</span><span class="sxs-lookup"><span data-stu-id="e1f5c-113">Workflow elements</span></span>           | <http://technet.microsoft.com/en-us/library/dd309626.aspx> |
| <span data-ttu-id="e1f5c-114">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="e1f5c-114">Workflow actions</span></span>            | <http://technet.microsoft.com/EN-US/library/dd362144.aspx> |
| <span data-ttu-id="e1f5c-115">ワークフローの参加者</span><span class="sxs-lookup"><span data-stu-id="e1f5c-115">Workflow participants</span></span>       | <http://technet.microsoft.com/EN-US/library/dd309598.aspx> |
| <span data-ttu-id="e1f5c-116">ワークフローの例</span><span class="sxs-lookup"><span data-stu-id="e1f5c-116">Workflow examples</span></span>           | <http://technet.microsoft.com/en-us/library/dd309636.aspx> |
| <span data-ttu-id="e1f5c-117">ワークフローの開発</span><span class="sxs-lookup"><span data-stu-id="e1f5c-117">Developing a workflow</span></span>       | <http://msdn.microsoft.com/EN-US/library/cc967389.aspx>    |
| <span data-ttu-id="e1f5c-118">ワークフローの実装</span><span class="sxs-lookup"><span data-stu-id="e1f5c-118">Implementing a workflow</span></span>     | <http://msdn.microsoft.com/en-us/library/cc585061.aspx>    |

## <a name="primary-changes-to-the-workflow-system"></a><span data-ttu-id="e1f5c-119">ワークフロー システムの主な変更</span><span class="sxs-lookup"><span data-stu-id="e1f5c-119">Primary changes to the workflow system</span></span>
<span data-ttu-id="e1f5c-120">Finance and Operations で実装された基本変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-120">Here are the primary changes that have been implemented in Finance and Operations:</span></span>

-   <span data-ttu-id="e1f5c-121">新しいアプリケーション状態機械機能との統合により、ワークフロー イベントを基になるエンティティの状態機械での状態遷移に関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-121">Integration with the new Application State Machine feature enables workflow events to be bound to state transitions on the underlying entity's state machine.</span></span> <span data-ttu-id="e1f5c-122">このバインディングにより、ビジネス ロジックをステート マシン内で集中化することが可能になり、また、ワークフロー システムをそのステート マシンの宣言コンシューマーにすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-122">This binding enables business logic to be centralized within the state machine and also enables the workflow system to be a declarative consumer of that state machine.</span></span> <span data-ttu-id="e1f5c-123">ワークフロー メタデータは、特定のワークフロー イベントが発生したときに実行される状態遷移を参照できます。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-123">The workflow metadata can reference a state transition that is performed when a specific workflow event occurs.</span></span> <span data-ttu-id="e1f5c-124">したがって、追加のコードを記述することなく、ワークフロー内で状態遷移を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-124">Therefore, you can do state transitions within a workflow without writing any additional code.</span></span>
-   <span data-ttu-id="e1f5c-125">ワークフロー エディターは、1 回クリックしてダウンロードするプログラムになりました。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-125">The workflow editor is now a program that you click one time to download.</span></span> <span data-ttu-id="e1f5c-126">エディターは、サービスを使用して、Finance and Operations と通信します。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-126">The editor communicates with Finance and Operations by using services.</span></span> <span data-ttu-id="e1f5c-127">したがって、Finance and Operations は、Dynamics AX 2012 の豊富なグラフィカルなワークフロー設計操作を引き継ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-127">Therefore, Finance and Operations can carry forward the rich, graphical workflow design experience from Dynamics AX 2012.</span></span>
-   <span data-ttu-id="e1f5c-128">ワークフロー開発ウィザードは Microsoft Visual Studio にポート済みです。</span><span class="sxs-lookup"><span data-stu-id="e1f5c-128">Workflow development wizards have been ported into Microsoft Visual Studio.</span></span>


<a name="additional-resources"></a><span data-ttu-id="e1f5c-129">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="e1f5c-129">Additional resources</span></span>
--------

[<span data-ttu-id="e1f5c-130">開発者向け技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="e1f5c-130">Technical Concepts Guide for Developers</span></span>](../dev-tools/developer-home-page.md)



