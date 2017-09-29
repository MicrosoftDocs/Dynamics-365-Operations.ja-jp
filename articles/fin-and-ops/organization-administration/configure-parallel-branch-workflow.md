---
title: "ワークフロー内の並列分岐コンフィギュレーション"
description: "並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。"
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 88c927505dde933f10f77922397aeb1c89a5fce5
ms.contentlocale: ja-jp
ms.lasthandoff: 07/18/2017

---

# <a name="configure-a-parallel-branch-in-a-workflow"></a><span data-ttu-id="2f5cd-103">ワークフロー内の並列分岐コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f5cd-103">Configure a parallel branch in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2f5cd-104">並列分岐をコンフィギュレーションするには、ワークフロー エディターで次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="2f5cd-105">並列分岐は、基本的に、親ワークフローのコンテキストで実行されるワークフローです。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="2f5cd-106">分岐に名前をつける</span><span class="sxs-lookup"><span data-stu-id="2f5cd-106">Name a branch</span></span>
<span data-ttu-id="2f5cd-107">並列分岐の名前を入力するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-107">Follow these steps to enter a name for a parallel branch.</span></span>
1.  <span data-ttu-id="2f5cd-108">並列分岐を右クリックし、[**プロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="2f5cd-109">[**プロパティ**] フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-109">The **Properties** form is displayed.</span></span>
2.  <span data-ttu-id="2f5cd-110">左ウィンドウで [**基本設定**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-110">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="2f5cd-111">[**名前**]フィールドに、並列分岐の一意な名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4.  <span data-ttu-id="2f5cd-112">[**閉じる**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="2f5cd-113">分岐の要素のデザインとコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2f5cd-113">Design and configure the elements of a branch</span></span>
<span data-ttu-id="2f5cd-114">並列分岐の要素のデザインとコンフィギュレーションを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>
1.  <span data-ttu-id="2f5cd-115">並列分岐をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-115">Double-click the parallel branch.</span></span>
2.  <span data-ttu-id="2f5cd-116">他のワークフローを作成する場合と同様に、ワークフロー要素をキャンバスにドラッグし、要素をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="2f5cd-117">詳細については、「ワークフローの作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2f5cd-117">For more information, see Create a workflow.</span></span>



<a name="see-also"></a><span data-ttu-id="2f5cd-118">参照</span><span class="sxs-lookup"><span data-stu-id="2f5cd-118">See also</span></span>
--------

[<span data-ttu-id="2f5cd-119">ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="2f5cd-119">Create a workflow</span></span>](create-workflow.md)




