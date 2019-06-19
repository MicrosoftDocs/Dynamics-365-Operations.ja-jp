---
title: 拡張機能を使用して列挙体に値を追加
description: このトピックでは、列挙型を拡張することによって列挙型に新しい値を追加する方法について説明します。
author: smithanataraj
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: d59e20efdc6da946f71c131bcf40e9d9cdb61edd
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550923"
---
# <a name="add-values-to-enums-through-extension"></a><span data-ttu-id="9cf0f-103">拡張機能を使用して列挙体に値を追加</span><span class="sxs-lookup"><span data-stu-id="9cf0f-103">Add values to enums through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9cf0f-104">新しい値を列挙型に追加するには、列挙型を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-104">To add new values to an enum, you should extend the enum.</span></span> <span data-ttu-id="9cf0f-105">**拡張可能** (**IsExtensible = true**) としてマークされている列挙は拡張できます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-105">Any enum that is marked as **Extensible** (**IsExtensible = true**) can be extended.</span></span> <span data-ttu-id="9cf0f-106">拡張機能の情報は、次の図に示すように、Microsoft Visual Studio の **プロパティ** ウィンドウで見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-106">You can find the extensibility information in the **Properties** window in Microsoft Visual Studio, as shown in the following illustration.</span></span>

![拡張可能な列挙](media/AddEnum01.png)

<span data-ttu-id="9cf0f-108">拡張可能な列挙の列挙値が同期されると、拡張可能な列挙の値が non-deterministic であるのに対して、ベースライン列挙の整数値は deterministic です。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-108">When enum values of extensible enums are synchronized, the integer values of the baseline enum are deterministic, whereas the integer values of the extension enum values are non-deterministic.</span></span> <span data-ttu-id="9cf0f-109">値は、同期時に生成されます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-109">The values are generated during synchronization.</span></span> <span data-ttu-id="9cf0f-110">したがって、列挙値の整数値に依存する X++ ロジックを持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-110">Therefore, you can't have logic that depends on the integer value of the enum values.</span></span> <span data-ttu-id="9cf0f-111">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-111">Here are some examples:</span></span>

+ <span data-ttu-id="9cf0f-112">`<`、`>`、`..` などの範囲比較</span><span class="sxs-lookup"><span data-stu-id="9cf0f-112">Range comparisons, such as `<`, `>`, and `..`</span></span>
+ <span data-ttu-id="9cf0f-113">ビューおよびクエリのモデル化された範囲</span><span class="sxs-lookup"><span data-stu-id="9cf0f-113">Modeled ranges in views and queries</span></span>
+ <span data-ttu-id="9cf0f-114">コードから作成されたクエリの範囲</span><span class="sxs-lookup"><span data-stu-id="9cf0f-114">Query ranges that are created from code</span></span> 

<span data-ttu-id="9cf0f-115">通常、拡張された列挙型は、それが使用される場所で独自の実装を必要とします。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-115">Usually, an extended enum must have its own implementation wherever it's used.</span></span> <span data-ttu-id="9cf0f-116">列挙のすべての使用を確認して、必要な場合に実装を取得します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-116">Look for all uses of the enum, and uptake the implementation where it's required.</span></span> <span data-ttu-id="9cf0f-117">検索するいくつかの重要な場所を次に示します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-117">Here are some significant places to look for:</span></span>

+ <span data-ttu-id="9cf0f-118">ブロックの切り替え:</span><span class="sxs-lookup"><span data-stu-id="9cf0f-118">Switch blocks:</span></span>

    - <span data-ttu-id="9cf0f-119">Switch ブロックに、既定の case ブロックまたは例外が発生しない既定のケース ブロックがない場合、デリゲートが指定されている場合、デリゲートを購読することにより拡張の列挙値を処理します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-119">If the switch block doesn't have a default case block or a default case block that doesn't throw an exception, handle the extended enum value by subscribing to a delegate, if a delegate is provided.</span></span> <span data-ttu-id="9cf0f-120">それ以外の場合、メソッドにポストイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-120">Otherwise, add a post-event handler to the method.</span></span> 
    - <span data-ttu-id="9cf0f-121">列挙型に例外をスローする既定のケース ブロックを持つスイッチが使用されている場合、Microsoft に問い合わせ、デリゲートを要求します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-121">If the enum is used in a switch that has a default case block that throws an exception, contact Microsoft to request a delegate.</span></span>

+ <span data-ttu-id="9cf0f-122">列挙型に、列挙型を処理する関連付けられたクラス階層がある場合は、列挙型固有の実装に対してサブクラスを作成し、必要に応じて基本クラスにコンストラクターを取り込みます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-122">If the enum has an associated class hierarchy that handles the enum, create a subclass for the extended enum–specific implementation, and uptake the construct on the base class as required.</span></span> <span data-ttu-id="9cf0f-123">詳細については、[ファクトリ メソッドのサブクラスの登録](register-subclass-factory-methods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-123">For more information, see [Register a subclass for factory methods](register-subclass-factory-methods.md).</span></span>
    
## <a name="extend-an-enum"></a><span data-ttu-id="9cf0f-124">列挙型を拡張します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-124">Extend an enum</span></span>

<span data-ttu-id="9cf0f-125">列挙型を拡張するには 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-125">There are two ways to extend an enum:</span></span>

+ <span data-ttu-id="9cf0f-126">新しい列挙拡張子を使用するモデル参照を持つプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-126">Create a project that has a model reference where you want the new enum extension.</span></span> <span data-ttu-id="9cf0f-127">拡張する列挙値を右クリックし、**拡張を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-127">Right-click the enum to extend, and then select **Create extension**.</span></span>

    ![拡張列挙を作成する (方法1)](media/AddEnum02.png)

+ <span data-ttu-id="9cf0f-129">拡張する列挙値を右クリックし、**新しいプロジェクトで拡張を作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-129">Right-click the enum to extend, and then select **Create extension in new project**.</span></span> <span data-ttu-id="9cf0f-130">拡張列挙を作成する必要のあるモデルを選択するように求められます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-130">You're prompted to select the model that the extension enum should be created in.</span></span>
        
    ![拡張列挙を作成する (方法2)](media/AddEnum03.png)
        
<span data-ttu-id="9cf0f-132">選択されたモデルで列挙型拡張が作成されます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-132">The enum extension is created in the selected model.</span></span> <span data-ttu-id="9cf0f-133">新しい列挙値をこの拡張に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="9cf0f-133">You can add new enum values to this extension.</span></span>
