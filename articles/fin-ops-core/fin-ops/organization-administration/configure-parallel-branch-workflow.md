---
title: ワークフロー内の並列分岐のコンフィギュレーション
description: 並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2058eaac77282946559cae11fcec8152658fc96b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811360"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="196b5-103">ワークフロー内の並列分岐のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="196b5-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="196b5-104">並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="196b5-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="196b5-105">並列分岐は、基本的に、親ワークフローのコンテキストで実行されるワークフローです。</span><span class="sxs-lookup"><span data-stu-id="196b5-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="196b5-106">分岐に名前をつける</span><span class="sxs-lookup"><span data-stu-id="196b5-106">Name a branch</span></span>

<span data-ttu-id="196b5-107">並列分岐の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="196b5-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="196b5-108">並列分岐を右クリックし、**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="196b5-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="196b5-109">**プロパティ**フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="196b5-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="196b5-110">左ウィンドウで**基本設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="196b5-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="196b5-111">**名前**フィールドに、並列分岐の一意な名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="196b5-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="196b5-112">**閉じる**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="196b5-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="196b5-113">分岐の要素のデザインとコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="196b5-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="196b5-114">並列分岐の要素のデザインとコンフィギュレーションを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="196b5-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="196b5-115">並列分岐をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="196b5-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="196b5-116">他のワークフローを作成する場合と同様に、ワークフロー要素をキャンバスにドラッグし、要素をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="196b5-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="196b5-117">詳細については、[ワークフロー作成の概要](create-workflow.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="196b5-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="196b5-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="196b5-118">Additional resources</span></span>

[<span data-ttu-id="196b5-119">ワークフローの作成の概要</span><span class="sxs-lookup"><span data-stu-id="196b5-119">Create workflows overview</span></span>](create-workflow.md)
