---
title: "Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)"
description: "この記事では、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラーに関する情報を提供します。 このツールを使用すると、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。 また、前提条件の一覧を示し、ビジネス プロセス モデラーの使用を開始する方法についても説明します。"
author: kfend
manager: AnnBe
ms.date: 09/25/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 15031
ms.assetid: 01c38560-f588-4558-a7ec-3af1bb518069
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 165dedf4736bdfd17588bb0df9959d048fc825e9
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="business-process-modeler-bpm-in-lifecycle-services-lcs"></a><span data-ttu-id="d3b6e-105">Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM)</span><span class="sxs-lookup"><span data-stu-id="d3b6e-105">Business process modeler (BPM) in Lifecycle Services (LCS)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3b6e-106">この記事では、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラーに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-106">This article provides information about Business process modeler in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="d3b6e-107">このツールを使用すると、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-107">You can use this tool to create, view, and modify business process libraries and flowcharts for Microsoft Dynamics AX.</span></span> <span data-ttu-id="d3b6e-108">また、前提条件の一覧を示し、ビジネス プロセス モデラーの使用を開始する方法についても説明します。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-108">The article also lists the prerequisites and explains how to start using Business process modeler.</span></span>

<span data-ttu-id="d3b6e-109">Microsoft Dynamics Lifecycle Services では、ビジネス プロセス モデラ－を使用して、Microsoft Dynamics AX の業務プロセス ライブラリおよびフローチャートを作成、表示、および変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-109">In Microsoft Dynamics Lifecycle Services, you can use Business process modeler to create, view, and modify business-process libraries and flowcharts for Microsoft Dynamics AX.</span></span> <span data-ttu-id="d3b6e-110">ビジネス プロセス モデラーは、[アメリカ生産性品質センター (APQC)](http://www.apqc.org/) によって説明された業界標準プロセスを使用して、Microsoft Dynamics AX プロセスを配置するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-110">Business process modeler helps you align your Microsoft Dynamics AX processes with industry-standard processes as described by [American Productivity & Quality Center (APQC)](http://www.apqc.org/).</span></span> <span data-ttu-id="d3b6e-111">Microsoft Dynamics AX で、業務上のニーズと既定のプロセスの間でフィットギャップ分析を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-111">You can perform fit-gap analysis between the business needs and the default processes in Microsoft Dynamics AX.</span></span> <span data-ttu-id="d3b6e-112">また、新しい業務プロセスを追加して、Microsoft Dynamics AX 2012 でまだ定義されていないプロセスのためにフローチャートを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-112">You can also add new business processes and create flowcharts for processes that are not already defined in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="d3b6e-113">ビジネス プロセス モデラーのコンポーネントは、次のアプリケーションで使用することができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-113">You can use Business process modeler artifacts with the following applications:</span></span>

-   <span data-ttu-id="d3b6e-114">Microsoft Visual Studio Team Foundation Server (TFS) – ギャップの連結リストを生成して、プロセス フローへの参照を含む作業項目としてそれらを TFS に手動でインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-114">Microsoft Visual Studio Team Foundation Server (TFS) – You can generate a consolidated list of gaps and import them manually into TFS as work items that include a reference to the process flow.</span></span>
-   <span data-ttu-id="d3b6e-115">Microsoft Word – 業務プロセスのドキュメントを生成できます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-115">Microsoft Word – You can generate documentation for business processes.</span></span>
-   <span data-ttu-id="d3b6e-116">Microsoft Visio – 業務プロセスのマップを Visio ファイルにエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-116">Microsoft Visio – You can export business process maps to Visio files.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d3b6e-117">前提条件</span><span class="sxs-lookup"><span data-stu-id="d3b6e-117">Prerequisites</span></span>
<span data-ttu-id="d3b6e-118">ビジネス プロセス モデラーを使用するには、次の製品が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-118">To use the Business process modeler, the following products are required:</span></span>

-   <span data-ttu-id="d3b6e-119">AX 2012 R3 および Microsoft Dynamics AX 2012 R2 の累積的な更新プログラム 7 に含まれるタスク レコーダーは、ビジネス プロセス モデラーにおけるカスタム プロセスの生成をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-119">The Task recorder that is included in AX 2012 R3 and cumulative update 7 for Microsoft Dynamics AX 2012 R2 supports generating custom processes in Business process modeler.</span></span> <span data-ttu-id="d3b6e-120">前のリリースでは、更新されたタスク レコーダーは修正プログラムとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-120">For earlier releases, an updated Task recorder is available as a hotfix.</span></span> <span data-ttu-id="d3b6e-121">この修正プログラムには、クライアントの更新プログラムとモデル ファイルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-121">The hotfix includes a client update and a model file.</span></span> <span data-ttu-id="d3b6e-122">Microsoft Dynamics AX 2012 のすべてのクライアントに、クライアント用更新プログラムをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-122">You must install the client update on all Microsoft Dynamics AX 2012 clients.</span></span> <span data-ttu-id="d3b6e-123">2 つの修正プログラムを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-123">There are two hotfixes available:</span></span>
    -   <span data-ttu-id="d3b6e-124">Microsoft Dynamics AX 2012 R2 – サポート技術情報の記事 [2863182](http://go.microsoft.com/fwlink/?LinkId=309911)</span><span class="sxs-lookup"><span data-stu-id="d3b6e-124">Microsoft Dynamics AX 2012 R2 – Knowledgebase article [2863182](http://go.microsoft.com/fwlink/?LinkId=309911)</span></span>
    -   <span data-ttu-id="d3b6e-125">Microsoft Dynamics AX 2012 と Microsoft Dynamics AX 2012 Feature Pack – サポート技術情報の記事 [2863182](http://go.microsoft.com/fwlink/?LinkId=309910)</span><span class="sxs-lookup"><span data-stu-id="d3b6e-125">Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 Feature Pack – Knowledgebase article [2863182](http://go.microsoft.com/fwlink/?LinkId=309910)</span></span>
-   <span data-ttu-id="d3b6e-126">Microsoft Office 2010 以降のバージョンではドキュメントの生成をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-126">Microsoft Office 2010 or later versions supports generating documents.</span></span>
-   <span data-ttu-id="d3b6e-127">Windows Media Player は業務プロセス ビデオの再生をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-127">Windows Media Player supports playing business process videos.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d3b6e-128">はじめに</span><span class="sxs-lookup"><span data-stu-id="d3b6e-128">Getting started</span></span>
<span data-ttu-id="d3b6e-129">ビジネス プロセス モデラーにアクセスするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-129">To access Business process modeler, follow these steps:</span></span>

1.  <span data-ttu-id="d3b6e-130">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="d3b6e-130">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="d3b6e-131">サインインしてプロジェクトを開き、**ビジネス プロセス モデラー** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-131">Sign in, open a project, and then click the **Business process modeler** tile.</span></span> <span data-ttu-id="d3b6e-132">**業務プロセス ライブラリ**には 3 つのセクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-132">The **Business process libraries** displays three sections:</span></span>
    -   <span data-ttu-id="d3b6e-133">**自分のライブラリ**には、ユーザーが作成または追加したビジネス プロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-133">**My libraries** contains business processes that the user has created or added.</span></span>
    -   <span data-ttu-id="d3b6e-134">**コーポレート ライブラリ**には、組織内のユーザーによってアップロードされた独自の業務プロセスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-134">**Corporate libraries** contains custom-created business processes that have been uploaded by someone in your organization.</span></span>
    -   <span data-ttu-id="d3b6e-135">**グローバル ライブラリ**には、産業間の標準の業務プロセスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-135">**Global libraries** contains cross-industry standard business processes.</span></span>

3.  <span data-ttu-id="d3b6e-136">標準的なビジネス プロセス ライブラリを **グローバル ライブラリ** セクションから **マイ ライブラリ** セクションにコピーするには、**グローバル ライブラリ** セクションでタイルを右クリックし、[アプリ] バーで **コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-136">To copy a standard business process library from the **Global libraries** section to the **My libraries** section, right-click the tile in the **Global libraries** section, and then on the app bar, click **Copy**.</span></span>
4.  <span data-ttu-id="d3b6e-137">業務プロセス ライブラリが**自分のライブラリ** セクションに追加された後、タイルをクリックして業務プロセス ライブラリを表示します。</span><span class="sxs-lookup"><span data-stu-id="d3b6e-137">After the business process library has been added to the **My libraries** section, click the tile to view the business process library.</span></span>


<a name="additional-resources"></a><span data-ttu-id="d3b6e-138">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="d3b6e-138">Additional resources</span></span>
--------

[<span data-ttu-id="d3b6e-139">ビジネス プロセス モデラーの業務プロセス ライブラリ</span><span class="sxs-lookup"><span data-stu-id="d3b6e-139">Business process libraries in Business process modeler</span></span>](../business-process-libraries-business-process-modeler.md)

[<span data-ttu-id="d3b6e-140">ビジネス プロセス モデラーのフローチャート</span><span class="sxs-lookup"><span data-stu-id="d3b6e-140">Flowcharts in Business process modeler</span></span>](../flowcharts-business-process-modeler.md)




