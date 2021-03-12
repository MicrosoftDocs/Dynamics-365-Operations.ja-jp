---
title: 製品ライフサイクルの状態をリリース済製品マスターに割り当て
description: ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9f8f519c54ffe4f1a2a44da51ac5d97c56182a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992223"
---
# <a name="assign-a-product-lifecycle-state-to-a-released-product-master"></a><span data-ttu-id="de728-103">製品ライフサイクルの状態をリリース済製品マスターに割り当て</span><span class="sxs-lookup"><span data-stu-id="de728-103">Assign a product lifecycle state to a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de728-104">ここでは、リリースされた製品およびそのバリアントに、製品ライフサイクルの状態を割り当てる手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="de728-104">This procedure shows how to assign a product lifecycle state to a released product master and its variants.</span></span> <span data-ttu-id="de728-105">前提条件: まずタスク ガイド「新しい製品のライフサイクルの状態の作成」を実行し、このタスク ガイドを実行する前に作成された、少なくとも 1 つの製品ライフサイクルの状態があることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="de728-105">Prerequisite: You need to play the task guide "Create a new product lifecycle state" first to make sure that you have at least one product lifecycle state created before you can play this task guide.</span></span>


## <a name="find-a-released-product-master"></a><span data-ttu-id="de728-106">リリース済製品マスターを検索します。</span><span class="sxs-lookup"><span data-stu-id="de728-106">Find a released product master</span></span>
1. <span data-ttu-id="de728-107">[製品情報管理] > [製品] > [リリースされた製品] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="de728-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="de728-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="de728-108">In the list, find and select the desired record.</span></span>

> [!NOTE]
> <span data-ttu-id="de728-109">製品マスターには、製品サブタイプの製品マスターがあります。</span><span class="sxs-lookup"><span data-stu-id="de728-109">A product master has the Product subtype Product master.</span></span>  

## <a name="update-the-lifecycle-state"></a><span data-ttu-id="de728-110">ライフサイクルの状態を更新します。</span><span class="sxs-lookup"><span data-stu-id="de728-110">Update the lifecycle state</span></span>
1. <span data-ttu-id="de728-111">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de728-111">Click Edit.</span></span>
2. <span data-ttu-id="de728-112">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="de728-112">In the Product lifecycle state field, enter or select a value.</span></span>
3. <span data-ttu-id="de728-113">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de728-113">Click Save.</span></span>
4. <span data-ttu-id="de728-114">[はい] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de728-114">Click Yes.</span></span>

> [!NOTE]
> <span data-ttu-id="de728-115">[はい] を選択した場合、リリースされた製品マスターとして同じ元のステータスを持つ関連するすべてのリリースされた製品バリアントは、新製品ライフサイクルの状態にも更新されます。</span><span class="sxs-lookup"><span data-stu-id="de728-115">If Yes is selected, all the related released product variants that have the same original status as the released product master are also updated to the new product lifecycle state.</span></span> <span data-ttu-id="de728-116">[いいえ] を選択した場合、すべてのバリアントは実際の状態を保持します。</span><span class="sxs-lookup"><span data-stu-id="de728-116">If No is selected, all variants keep their actual state.</span></span> <span data-ttu-id="de728-117">リリースされた製品マスターから別の製品ライフサイクルの状態を持つバリアントは、更新されません。</span><span class="sxs-lookup"><span data-stu-id="de728-117">Variants that have a different product lifecycle state from the released product master are not updated.</span></span>  

## <a name="verify-the-lifecycle-state-of-the-variants"></a><span data-ttu-id="de728-118">バリアントのライフサイクルの状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="de728-118">Verify the lifecycle state of the variants</span></span>
1. <span data-ttu-id="de728-119">[リリース済製品バリアント] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="de728-119">Click Released product variants.</span></span>

> [!NOTE]
> <span data-ttu-id="de728-120">すべてのバリアントが、リリースされた製品マスターから選択済ライフサイクルの状態を継承したことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="de728-120">Note that all variants have inherited the selected lifecycle state from the released product master.</span></span>  

2. <span data-ttu-id="de728-121">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="de728-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="de728-122">[製品ライフサイクルの状態] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="de728-122">In the Product lifecycle state field, enter or select a value.</span></span>

