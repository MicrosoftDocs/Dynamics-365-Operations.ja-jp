---
title: 製品ライフサイクルの状態をリリース済製品マスターに割り当て
description: ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd9d40bb331b9e024617c8be55330dfce8ba1cc6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "309475"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="4690e-103">製品ライフサイクルの状態をリリース済製品マスターに割り当て</span><span class="sxs-lookup"><span data-stu-id="4690e-103">Assign a product lifecycle state to a released product master</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4690e-104">ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="4690e-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="4690e-105">前提条件: まずタスク ガイド「新しい製品のライフサイクルの状態の作成」を実行し、このタスク ガイドを実行する前に作成された、少なくとも 1 つの製品ライフサイクルの状態があることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4690e-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="4690e-106">リリース済製品マスターを検索します。</span><span class="sxs-lookup"><span data-stu-id="4690e-106">Find a released product master</span></span>
1. <span data-ttu-id="4690e-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4690e-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4690e-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4690e-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="4690e-109">製品マスターには、製品サブタイプの製品マスターがあります。</span><span class="sxs-lookup"><span data-stu-id="4690e-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="4690e-110">ライフサイクルの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="4690e-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="4690e-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4690e-111">Click Edit.</span></span>
2. <span data-ttu-id="4690e-112">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4690e-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="4690e-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4690e-113">Click Save.</span></span>
4. <span data-ttu-id="4690e-114">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4690e-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="4690e-115">[はい] を選択した場合、リリースされた製品マスターとして同じ元のステータスを持つ関連するすべてのリリースされた製品バリアントは、新製品ライフサイクルの状態にも更新されます。</span><span class="sxs-lookup"><span data-stu-id="4690e-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="4690e-116">[いいえ] を選択した場合、すべてのバリアントは実際の状態を保持します。</span><span class="sxs-lookup"><span data-stu-id="4690e-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="4690e-117">リリースされた製品マスターから別の製品ライフサイクルの状態を持つバリアントは、更新されません。</span><span class="sxs-lookup"><span data-stu-id="4690e-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="4690e-118">バリアントのライフサイクルの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="4690e-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="4690e-119">[リリース済製品バリアント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4690e-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="4690e-120">すべてのバリアントが、リリースされた製品マスターから選択済ライフサイクルの状態を継承したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="4690e-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="4690e-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="4690e-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4690e-122">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="4690e-122">In the Product lifecycle state field, enter or select a value.</span></span>

