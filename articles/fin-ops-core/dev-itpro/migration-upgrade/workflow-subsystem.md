---
title: Finance and Operations のワークフロー サブシステムのアップデート
description: このトピックでは、Finance and Operations のワークフロー システムを確認します。
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 13511
ms.assetid: 0e3aa2cd-2327-45ba-bf38-0ef543fa8f67
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24cd0154dba2669c3ca756e8c627757565d53461
ms.sourcegitcommit: 9a053d020e672a87b660f27009a492544e6c81a9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2020
ms.locfileid: "3641460"
---
# <a name="workflow-subsystem-updates-in-finance-and-operations"></a><span data-ttu-id="26251-103">Finance and Operations のワークフロー サブシステムのアップデート</span><span class="sxs-lookup"><span data-stu-id="26251-103">Workflow subsystem updates in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="26251-104">このトピックでは、Finance and Operations のワークフロー システムを確認します。</span><span class="sxs-lookup"><span data-stu-id="26251-104">This topic reviews the workflow system in Finance and Operations.</span></span> <span data-ttu-id="26251-105">Microsoft Dynamics AX 2012 以降に実装された変更について説明し、ワークフロー システムに関する詳細へのリンクも示します。</span><span class="sxs-lookup"><span data-stu-id="26251-105">It describes the changes that have been implemented since Microsoft Dynamics AX 2012 and also includes links to more information about the workflow system.</span></span> 

<span data-ttu-id="26251-106">Dynamics AX 2012 を使用したことがあれば、Finance and Operations のワークフロー システムはおなじみのものです。</span><span class="sxs-lookup"><span data-stu-id="26251-106">The workflow system in Finance and Operations will be familiar to you if you've used Dynamics AX 2012.</span></span> <span data-ttu-id="26251-107">Dynamics AX 2012 のワークフロー サブシステムの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="26251-107">For more information about the workflow subsystem in Dynamics AX 2012, see the following topics.</span></span>

| <span data-ttu-id="26251-108">このテーマについて学ぶには</span><span class="sxs-lookup"><span data-stu-id="26251-108">To learn about this subject</span></span> | <span data-ttu-id="26251-109">このトピックを参照</span><span class="sxs-lookup"><span data-stu-id="26251-109">See this topic</span></span>                                             |
|-----------------------------|------------------------------------------------------------|
| <span data-ttu-id="26251-110">ワークフロー システム</span><span class="sxs-lookup"><span data-stu-id="26251-110">The workflow system</span></span>         | <https://technet.microsoft.com/library/dd309672.aspx> |
| <span data-ttu-id="26251-111">モジュールごとのワークフロー タイプ</span><span class="sxs-lookup"><span data-stu-id="26251-111">Workflow types by module</span></span>    | <https://technet.microsoft.com/library/dd362043.aspx> |
| <span data-ttu-id="26251-112">ワークフロー要素</span><span class="sxs-lookup"><span data-stu-id="26251-112">Workflow elements</span></span>           | <https://technet.microsoft.com/library/dd309626.aspx> |
| <span data-ttu-id="26251-113">ワークフロー アクション</span><span class="sxs-lookup"><span data-stu-id="26251-113">Workflow actions</span></span>            | <https://technet.microsoft.com/library/dd362144.aspx> |
| <span data-ttu-id="26251-114">ワークフローの参加者</span><span class="sxs-lookup"><span data-stu-id="26251-114">Workflow participants</span></span>       | <https://technet.microsoft.com/library/dd309598.aspx> |
| <span data-ttu-id="26251-115">ワークフローの例</span><span class="sxs-lookup"><span data-stu-id="26251-115">Workflow examples</span></span>           | <https://technet.microsoft.com/library/dd309636.aspx> |
| <span data-ttu-id="26251-116">ワークフローの開発</span><span class="sxs-lookup"><span data-stu-id="26251-116">Developing a workflow</span></span>       | <https://msdn.microsoft.com/library/cc967389.aspx>    |
| <span data-ttu-id="26251-117">ワークフローの実装</span><span class="sxs-lookup"><span data-stu-id="26251-117">Implementing a workflow</span></span>     | <https://msdn.microsoft.com/library/cc585061.aspx>    |

## <a name="primary-changes-to-the-workflow-system"></a><span data-ttu-id="26251-118">ワークフロー システムの主な変更</span><span class="sxs-lookup"><span data-stu-id="26251-118">Primary changes to the workflow system</span></span>
<span data-ttu-id="26251-119">以下は、Finance and Operations に実装された主な変更点です。</span><span class="sxs-lookup"><span data-stu-id="26251-119">Here are the primary changes that have been implemented in Finance and Operations:</span></span>

-   <span data-ttu-id="26251-120">新しいアプリケーション状態機械機能との統合により、ワークフロー イベントを基になるエンティティの状態機械での状態遷移に関連付けできます。</span><span class="sxs-lookup"><span data-stu-id="26251-120">Integration with the new Application State Machine feature enables workflow events to be bound to state transitions on the underlying entity's state machine.</span></span> <span data-ttu-id="26251-121">このバインディングにより、ビジネス ロジックをステート マシン内で集中化することが可能になり、また、ワークフロー システムをそのステート マシンの宣言コンシューマーにすることが可能になります。</span><span class="sxs-lookup"><span data-stu-id="26251-121">This binding enables business logic to be centralized within the state machine and also enables the workflow system to be a declarative consumer of that state machine.</span></span> <span data-ttu-id="26251-122">ワークフロー メタデータは、特定のワークフロー イベントが発生したときに実行される状態遷移を参照できます。</span><span class="sxs-lookup"><span data-stu-id="26251-122">The workflow metadata can reference a state transition that is performed when a specific workflow event occurs.</span></span> <span data-ttu-id="26251-123">したがって、追加のコードを記述することなく、ワークフロー内で状態遷移を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="26251-123">Therefore, you can do state transitions within a workflow without writing any additional code.</span></span>
-   <span data-ttu-id="26251-124">ワークフロー エディターは、1 回クリックしてダウンロードするプログラムになりました。</span><span class="sxs-lookup"><span data-stu-id="26251-124">The workflow editor is now a program that you click one time to download.</span></span> <span data-ttu-id="26251-125">このエディターは、サービスを使用して Finance and Operations と通信します。つまり、Dynamics AX 2012 からの豊富でグラフィカルなワークフロー 設計操作を引き継ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="26251-125">The editor communicates with Finance and Operations by using services, which means that you can carry forward the rich, graphical workflow design experience from Dynamics AX 2012.</span></span>
-   <span data-ttu-id="26251-126">ワークフロー開発ウィザードは Microsoft Visual Studio にポート済みです。</span><span class="sxs-lookup"><span data-stu-id="26251-126">Workflow development wizards have been ported into Microsoft Visual Studio.</span></span>


<a name="additional-resources"></a><span data-ttu-id="26251-127">追加リソース</span><span class="sxs-lookup"><span data-stu-id="26251-127">Additional resources</span></span>
--------

[<span data-ttu-id="26251-128">開発者向け技術概念ガイド</span><span class="sxs-lookup"><span data-stu-id="26251-128">Technical Concepts Guide for Developers</span></span>](../dev-tools/developer-home-page.md)



