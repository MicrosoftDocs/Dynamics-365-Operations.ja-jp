---
title: ワークフロー内の並列分岐のコンフィギュレーション
description: 並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b5270660f0dbe4351f0088787468a563d2f36cf
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747810"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="dbdbe-103">ワークフロー内の並列分岐のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dbdbe-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbdbe-104">並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="dbdbe-105">並列分岐は、基本的に、親ワークフローのコンテキストで実行されるワークフローです。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="dbdbe-106">分岐に名前をつける</span><span class="sxs-lookup"><span data-stu-id="dbdbe-106">Name a branch</span></span>

<span data-ttu-id="dbdbe-107">並列分岐の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="dbdbe-108">並列分岐を右クリックし、**プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="dbdbe-109">**プロパティ** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="dbdbe-110">左ウィンドウで **基本設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="dbdbe-111">**名前** フィールドに、並列分岐の一意な名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="dbdbe-112">**閉じる** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="dbdbe-113">分岐の要素のデザインとコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="dbdbe-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="dbdbe-114">並列分岐の要素のデザインとコンフィギュレーションを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="dbdbe-115">並列分岐をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="dbdbe-116">他のワークフローを作成する場合と同様に、ワークフロー要素をキャンバスにドラッグし、要素をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="dbdbe-117">詳細については、[ワークフロー作成の概要](create-workflow.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dbdbe-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dbdbe-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="dbdbe-118">Additional resources</span></span>

[<span data-ttu-id="dbdbe-119">ワークフローの作成の概要</span><span class="sxs-lookup"><span data-stu-id="dbdbe-119">Create workflows overview</span></span>](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]