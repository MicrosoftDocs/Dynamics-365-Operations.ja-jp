---
title: Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)
description: この記事では、Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー ツールについて説明します。
author: kfend
manager: AnnBe
ms.date: 10/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 10dddaf951abb6acf4027e095745df353edea783
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183222"
---
# <a name="business-process-modeler-bpm-in-lifecycle-services-lcs"></a><span data-ttu-id="f5fab-103">Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)</span><span class="sxs-lookup"><span data-stu-id="f5fab-103">Business process modeler (BPM) in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f5fab-104">Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) は、業務プロセス ライブラリとフローチャートに基づいて反復可能な実装を作成、表示、および変更するために使用することができるツールです。</span><span class="sxs-lookup"><span data-stu-id="f5fab-104">Business process modeler (BPM) in Microsoft Dynamics Lifecycle Services (LCS) is a tool that you can use to create, view, and modify repeatable implementations that are based on business process libraries and flowcharts.</span></span> <span data-ttu-id="f5fab-105">BPM は、[アメリカ生産性 &amp; 品質センター (APQC)](https://www.apqc.org/) によって説明された業界標準プロセスを使用して、業務プロセスを配置するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-105">BPM helps you align your business processes with industry-standard processes that are described by the [American Productivity &amp; Quality Center (APQC)](https://www.apqc.org/).</span></span> <span data-ttu-id="f5fab-106">Finance and Operations アプリで、業務上の要件と既定のプロセスの間でフィットギャップ分析を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-106">You can perform fit-gap analysis between your business requirements and the default processes in the Finance and Operations apps.</span></span> <span data-ttu-id="f5fab-107">また、新しい業務プロセスを追加して、まだ定義されていないプロセスのためにフローチャートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-107">Additionally, you can add new business processes and create flowcharts for processes that aren't already defined.</span></span>

<span data-ttu-id="f5fab-108">BPM は次のプログラムと互換性があります。</span><span class="sxs-lookup"><span data-stu-id="f5fab-108">BPM is compatible with the following programs:</span></span>

- <span data-ttu-id="f5fab-109">**Microsoft Word** - 業務プロセスのドキュメントを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-109">**Microsoft Word** – You can generate documentation for business processes.</span></span>
- <span data-ttu-id="f5fab-110">**Microsoft Visio** – 業務プロセスのマップを Visio ファイルにエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-110">**Microsoft Visio** – You can export business process maps to Visio files.</span></span>

> [!NOTE]
> <span data-ttu-id="f5fab-111">このトピックに記載されている情報は、Finance and Operations アプリにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-111">The information in this topic is specific only to Finance and Operations apps.</span></span> <span data-ttu-id="f5fab-112">ビジネス プロセス モデラーおよび Microsoft Dynamics AX 2012 の詳細については、[ビジネス プロセス モデラー](ax-2012/business-process-modeler-lcs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f5fab-112">For information about Business process modeler and Microsoft Dynamics AX 2012, see [Business process modeler](ax-2012/business-process-modeler-lcs.md).</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="f5fab-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="f5fab-113">Prerequisites</span></span>

<span data-ttu-id="f5fab-114">BPM を効果的に使用するには、Microsoft Office 2010 と Microsoft Azure DevOps プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="f5fab-114">To effectively use BPM, you must have Microsoft Office 2010 and a Microsoft Azure DevOps project.</span></span>

## <a name="getting-started"></a><span data-ttu-id="f5fab-115">はじめに</span><span class="sxs-lookup"><span data-stu-id="f5fab-115">Getting started</span></span>

<span data-ttu-id="f5fab-116">BPM にアクセスするには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="f5fab-116">Follow these steps to access BPM.</span></span>

1. <span data-ttu-id="f5fab-117">[LCS](https://lcs.dynamics.com/)  に移動します。</span><span class="sxs-lookup"><span data-stu-id="f5fab-117">Go to [LCS](https://lcs.dynamics.com/).</span></span>
2. <span data-ttu-id="f5fab-118">サインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="f5fab-118">Sign in, open a project, and then select the **Business process modeler** tile.</span></span> <span data-ttu-id="f5fab-119">**業務プロセス ライブラリ** ページには 3 つのセクションがあります。</span><span class="sxs-lookup"><span data-stu-id="f5fab-119">The **Business process libraries** page has three sections:</span></span>

    - <span data-ttu-id="f5fab-120">**自分のライブラリ** – このセクションには、ユーザーが作成または追加したビジネス プロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5fab-120">**My libraries** – This section contains business processes that the user has created or added.</span></span>
    - <span data-ttu-id="f5fab-121">**コーポレート ライブラリ** - このセクションには、組織内のユーザーがアップロードした独自の業務プロセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="f5fab-121">**Corporate libraries** – This section contains custom business processes that someone in your organization has uploaded.</span></span>
    - <span data-ttu-id="f5fab-122">**グローバル ライブラリ** – このセクションには、産業間の標準の業務プロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f5fab-122">**Global libraries** – This section contains cross-industry standard business processes.</span></span>

3. <span data-ttu-id="f5fab-123">標準的なビジネス プロセス ライブラリを **グローバル ライブラリ** セクションから **マイ ライブラリ** セクションにコピーするには、**グローバル ライブラリ** セクションでタイルの右上隅を選択し、**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f5fab-123">To copy a standard business process library from the **Global libraries** section to the **My libraries** section, select the upper-right corner of the tile in the **Global libraries** section, and then select **Copy**.</span></span>
4. <span data-ttu-id="f5fab-124">業務プロセス ライブラリが**自分のライブラリ** セクションに追加された後、タイルを選択して業務プロセス ライブラリを表示します。</span><span class="sxs-lookup"><span data-stu-id="f5fab-124">After the business process library has been added to the **My libraries** section, select the tile to view the business process library.</span></span>

## <a name="working-in-bpm-libraries"></a><span data-ttu-id="f5fab-125">BPM ライブラリでの作業</span><span class="sxs-lookup"><span data-stu-id="f5fab-125">Working in BPM libraries</span></span>

<span data-ttu-id="f5fab-126">次のトピックでは、BPM ライブラリを使用して作業する方法について詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="f5fab-126">The following topics provide more information about how to work with BPM libraries:</span></span>

- [<span data-ttu-id="f5fab-127">BPM ライブラリの作成、編集、または参照</span><span class="sxs-lookup"><span data-stu-id="f5fab-127">Create, edit, or browse a BPM library</span></span>](creating-editing-browsing.md)
- [<span data-ttu-id="f5fab-128">BPM ライブラリと Azure DevOps の同期</span><span class="sxs-lookup"><span data-stu-id="f5fab-128">Synchronize a BPM library with Azure DevOps</span></span>](synchronize-bpm-vsts.md)
- [<span data-ttu-id="f5fab-129">BPM のタスクの完了</span><span class="sxs-lookup"><span data-stu-id="f5fab-129">Complete tasks in BPM</span></span>](complete-tasks-bpm.md)
- [<span data-ttu-id="f5fab-130">BPM 付き活動ダイアグラムを使用する</span><span class="sxs-lookup"><span data-stu-id="f5fab-130">Use activity diagrams with BPM</span></span>](using-activity-diagrams.md)
- [<span data-ttu-id="f5fab-131">ビジネス プロセス モデラーの業務プロセス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="f5fab-131">Business process libraries in Business process modeler</span></span>](business-process-libraries-business-process-modeler.md)
- [<span data-ttu-id="f5fab-132">ビジネス プロセス モデラーのフローチャート</span><span class="sxs-lookup"><span data-stu-id="f5fab-132">Flowcharts in Business process modeler</span></span>](flowcharts-business-process-modeler.md)


