---
title: 拡張機能の名前付けのガイドライン
description: このトピックでは、拡張機能の名前付けガイドラインについて説明します。
author: LarsBlaaberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 8DA4DA85-0C2D-4CAF-B350-DAC9C1BE4DF9
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.openlocfilehash: bded8792df973a00c68fb931d839be7cd137ecdc
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833494"
---
# <a name="naming-guidelines-for-extensions"></a><span data-ttu-id="011d1-103">拡張機能の名前付けのガイドライン</span><span class="sxs-lookup"><span data-stu-id="011d1-103">Naming guidelines for extensions</span></span>

[!include [banner](../includes/banner.md)]

## <a name="naming-model-elements"></a><span data-ttu-id="011d1-104">モデル要素に名前を付ける</span><span class="sxs-lookup"><span data-stu-id="011d1-104">Naming model elements</span></span>
<span data-ttu-id="011d1-105">モデル内の要素には、インストール時にすべてのモデルで一意の名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-105">Any element in a model must be given a name, which is unique across all models at installation time.</span></span> <span data-ttu-id="011d1-106">すべての潜在的なモデルの場合、実装時に共にインストールされるモデルは不明であり、すべての要素名にはソリューション固有の接頭辞が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-106">Given that all potential models, that your model will be installed together with, are unknown at implementation time, then every element name should include a prefix, which is specific to your solution.</span></span> <span data-ttu-id="011d1-107">モデルに複数のソリューションが含まれている場合は、さまざまな接頭語によって、モデルでは、各ソリューションを識別できます。</span><span class="sxs-lookup"><span data-stu-id="011d1-107">If a model contains multiple solutions, then each solution within the model can be identified by different prefixes.</span></span>

<span data-ttu-id="011d1-108">接頭語の選択は、他の関係者からの他のモデルの要素に同じ接頭語が選択されるというリスクを最小限に抑えるように慎重に行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-108">The prefix must be carefully chosen to minimize the risk that other models from other parties have chosen the same prefix for their elements.</span></span>
<span data-ttu-id="011d1-109">モデルに要素の名前を付けるときに接頭語を含めると、モデルが他のモデルと一緒に後でインストールされるときに名前の競合のリスクが大幅に引き下げられます。</span><span class="sxs-lookup"><span data-stu-id="011d1-109">By including the prefix when naming elements in your model, then you have significantly lowered the risk of naming conflicts, when your model is later installed alongside other models.</span></span>

<span data-ttu-id="011d1-110">他のモデル内の機能を拡張するとき、拡張される要素には接頭語がすでに含まれています。</span><span class="sxs-lookup"><span data-stu-id="011d1-110">When you extend functionality in other models, then elements being extended already contains a prefix.</span></span> <span data-ttu-id="011d1-111">接頭語を拡張要素に追加し、それぞれの後に複数の接頭語を続けずに、拡張要素に名前を付けるときに接頭語やその他の語句、省略形をインフィックスとして含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-111">Instead of adding your prefix to the extension elements resulting in multiple prefixes after each other, then you should rather include your prefix or another term or abbreviation as an infix when naming the extension element.</span></span>

<span data-ttu-id="011d1-112">拡張機能の特定の名前付けに関する詳細を次に示します。</span><span class="sxs-lookup"><span data-stu-id="011d1-112">Here are details about the specific naming of extensions.</span></span>

## <a name="naming-extensions"></a><span data-ttu-id="011d1-113">拡張機能に名前を付ける</span><span class="sxs-lookup"><span data-stu-id="011d1-113">Naming Extensions</span></span>

<span data-ttu-id="011d1-114">拡張要素、すなわちテーブル拡張子、ビュー拡張子、フォーム拡張子など、他のモデルの拡張子と競合のリスクを最小限にする一意の名前を付ける必要があります。現在と将来の両方で行なえます。</span><span class="sxs-lookup"><span data-stu-id="011d1-114">An extension element, i.e. table extension, view extension, form extension, etc.,  must be given a unique name, that minimizes the risk of conflicts with extensions in other models; both now and in the future.</span></span> <span data-ttu-id="011d1-115">競合のリスクを最小限に抑えるために、名前には、拡張機能を他のモデル内の同じ要素の他の拡張機能と区別するための用語、省略形、または接中辞が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-115">To minimize the risk of conflicts, the name should therefore include a term, abbreviation or infix, that distinguishes the extension from other extension to the same element in other models.</span></span>

- <span data-ttu-id="011d1-116">**必ず**拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。</span><span class="sxs-lookup"><span data-stu-id="011d1-116">**DO** include either the name of the model in which the extension element resides, or the prefix the extension is associated with.</span></span>
<span data-ttu-id="011d1-117">WHS 接頭語を使用してその他すべての要素の名前を付ける HCMWorker テーブルの拡張クラスは、ウェアハウジング モジュールにより HCMWorker.WHSExtension という名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-117">An extension of the HCMWorker table by a Warehousing module using the WHS prefix to name all other elements, could be named HCMWorker.WHSExtension.</span></span> <span data-ttu-id="011d1-118">モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="011d1-118">The prefix used to name other elements in the module, is inserted as an infix in the name.</span></span>
<span data-ttu-id="011d1-119">ApplicationSuite の ContactPerson テーブルの拡張子は、ApplicationSuite モデルから ContactPerson テーブルへすべての拡張機能を含む拡張子である場合、ContactPerson.ApplicationSuiteExtension という名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-119">An extension of the ContactPerson table in the ApplicationSuite could be named ContactPerson.ApplicationSuiteExtension, if the extension is meant to contain all extensions to the ContactPerson table from the ApplicationSuite model.</span></span>

- <span data-ttu-id="011d1-120">**必ず**末尾に Extension という用語を付けます。</span><span class="sxs-lookup"><span data-stu-id="011d1-120">**DO** suffix the name with the term Extension.</span></span>
<span data-ttu-id="011d1-121">InventLocation テーブルの拡張は、次のパターン InventLocation に従う必要があります。<Model>拡張</span><span class="sxs-lookup"><span data-stu-id="011d1-121">An extension of the InventLocation table should follow the following pattern InventLocation.<Model>Extension</span></span>

- <span data-ttu-id="011d1-122">拡張子に <ElementBeingExtended>.Extension のような簡単な名前を**つけないで**ください。</span><span class="sxs-lookup"><span data-stu-id="011d1-122">**DO** NOT name the extension simply as <ElementBeingExtended>.Extension.</span></span>
<span data-ttu-id="011d1-123">競合のリスクが高すぎるため、InventLocation テーブルの拡張子は InventLocation.Extension という名前を付けることができません。</span><span class="sxs-lookup"><span data-stu-id="011d1-123">An extension of the InventLocation table must not be named InventLocation.Extension, as the risk of conflicts is too high.</span></span>


## <a name="naming-extension-classes"></a><span data-ttu-id="011d1-124">拡張クラスの名前を付ける</span><span class="sxs-lookup"><span data-stu-id="011d1-124">Naming Extension classes</span></span>

<span data-ttu-id="011d1-125">強化を介して拡張可能なテーブル、クラス、または他の要素ロジックを拡張するために使用される拡張子クラスには、すべてのモデルのすべてのタイプで一意の名前を付ける必要が今後もあります。</span><span class="sxs-lookup"><span data-stu-id="011d1-125">Extension classes used to augment logic on tables, classes, or other elements which can be extended through augmentation, need to be given a name which is unique across all types in all models; both now and in the future.</span></span>

<span data-ttu-id="011d1-126">拡張クラスに拡張されている型の名前を含めることは望ましいですが、同時に、その名前にその他の型とクラスを区別する用語、省略形または接頭語も含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-126">It is preferable that the extension class includes the name of the type being extended, but at the same time, the name must also include a term, abbreviation or prefix, that distinguishes the class from other types.</span></span>

- <span data-ttu-id="011d1-127">**必ず**拡張クラスの名前を強化された型の名前で開始し、_Extension という用語で終了します。</span><span class="sxs-lookup"><span data-stu-id="011d1-127">**DO** start the name of the extension class with the name of the type being augmented, and end it with the term _Extension.</span></span>
<span data-ttu-id="011d1-128">ContactPerson テーブルを増補する拡張クラスは、ContactPerson という名前で開始し、_Extension、および ContactPersonWHS_Extension などで終了する必要があります</span><span class="sxs-lookup"><span data-stu-id="011d1-128">An extension class augmenting the ContactPerson table should start with the name ContactPerson, and end with _Extension, e.g. ContactPersonWHS_Extension</span></span>

- <span data-ttu-id="011d1-129">**必ず**拡張要素が存在するモデルの名前、または拡張子が関連付けられている接頭辞のいずれかを含めます。</span><span class="sxs-lookup"><span data-stu-id="011d1-129">**DO** include either the name of the model in which the extension element resides, or the prefix the extension is associated with.</span></span>
<span data-ttu-id="011d1-130">WHS 接頭語を使用してその他すべての要素の名前を付ける ContactPerson テーブルを拡張する拡張クラスは、ウェアハウジング モジュールにより ContactPersonWHS_Extension という名前付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-130">An extension class augmenting the ContactPerson table by a Warehousing module using the WHS prefix to name all other elements, could be named ContactPersonWHS_Extension.</span></span> <span data-ttu-id="011d1-131">モジュール内の他の要素に名前を付けるために使用される接頭語は、接中辞として挿入されます。</span><span class="sxs-lookup"><span data-stu-id="011d1-131">The prefix used to name other elements in the module, is inserted as an infix in the name.</span></span>
<span data-ttu-id="011d1-132">ApplicationSuite モデルの ContactPerson テーブル を増補する拡張クラスは、拡張クラス ApplicationSuite の ContactPerson テーブルへすべての拡張機能を含む拡張をしている場合、ContactPersonApplicationSuite 拡張子という名前にすることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-132">An extension class augmenting the ContactPerson table in the ApplicationSuite model could be named ContactPersonApplicationSuite_Extension, if the extension class is meant to contain all extension to the ContactPerson table in the ApplicationSuite model.</span></span>

- <span data-ttu-id="011d1-133">拡張子に <ElementBeingExtended>_Extension のような簡単な名前を**つけないでください**。</span><span class="sxs-lookup"><span data-stu-id="011d1-133">**DO NOT** name the extension simply as <ElementBeingExtended>_Extension.</span></span>
<span data-ttu-id="011d1-134">競合のリスクが高すぎるため、InventLocation テーブルを増補する拡張クラスは InventLocation_Extension という名前を付けることができません。</span><span class="sxs-lookup"><span data-stu-id="011d1-134">An extension class augmenting the InventLocation table must not be named InventLocation_Extension, as the risk of conflicts is too high.</span></span>

## <a name="naming-fields-field-groups-indexes-relations-and-other-metadata-nodes-in-extension-elements"></a><span data-ttu-id="011d1-135">拡張要素のフィールド、フィールド グループ、インデックス、関係およびその他のメタデータ ノードに名前を付ける</span><span class="sxs-lookup"><span data-stu-id="011d1-135">Naming Fields, Field groups, Indexes, Relations and other metadata nodes in Extension elements</span></span>

<span data-ttu-id="011d1-136">拡張要素のフィールド、インデックス、関係、およびその他のメタデータ要素は、その他の拡張要素と同じように、拡張されている両方の要素間で一意である必要もあります。</span><span class="sxs-lookup"><span data-stu-id="011d1-136">Fields, indexes, relations and other metadata elements on extension elements also need be unique across both the element being extended as well as other extension elements.</span></span>
<span data-ttu-id="011d1-137">したがって、これらのメタデータ ノードには、モデル間の競合のリスクを制限する用語、省略形または接頭辞も含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-137">These metadata nodes therefore also need to include a term, abbreviation or prefix, that limits the risk of conflicts across models.</span></span>

- <span data-ttu-id="011d1-138">**必ず**メタデータ ノードの名前の先頭に接頭語、用語、または省略形を含めます。</span><span class="sxs-lookup"><span data-stu-id="011d1-138">**DO** include a prefix, term, or abbreviation in the beginning of the metadata node name.</span></span>
<span data-ttu-id="011d1-139">承認する作業者の外部キー フィールドは、テーブルの拡張機能の一部として追加され、WHS がホスティング モデル内の他の要素の専用接頭語の 1 つとして想定した場合 WHSApprovingWorker という名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-139">An approving worker foreign key field added to as part of a table extension could be named WHSApprovingWorker, assuming WHS is one of prefixes dedicated to other elements in the hosting model.</span></span>


## <a name="naming-members-in-extension-classes"></a><span data-ttu-id="011d1-140">拡張クラス内のメンバーの名前を付ける</span><span class="sxs-lookup"><span data-stu-id="011d1-140">Naming members in extension classes</span></span>
<span data-ttu-id="011d1-141">クラス レベルの変数、および拡張クラスのメソッドには、拡張される型全体で一意の名前と、同じタイプを拡張する他のすべての拡張クラスを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="011d1-141">Class level variables, and methods on extension classes must be provided a name that is unique across the type being augmented, and all other extension classes augmenting the same type.</span></span>

- <span data-ttu-id="011d1-142">**必ず**メンバー名の先頭に接頭辞、用語、または省略形を含めます。</span><span class="sxs-lookup"><span data-stu-id="011d1-142">**DO** include a prefix, term, or abbreviation in the beginning of the member name.</span></span>
<span data-ttu-id="011d1-143">WHS がモデル内の他の要素で使用される接頭語の 1 つである場合、承認する作業者クラス レベルの変数に WHSApprovingWorker という名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-143">An approving worker class level variable could be named WHSApprovingWorker, if WHS is one of the prefixes used by other element in the model.</span></span>
<span data-ttu-id="011d1-144">WHS がホスティング モデルの他の要素で使用される接頭語の 1 つである場合、approveWork メソッドは WHSApproveWork という名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="011d1-144">An approveWork method could be named WHSApproveWork, if WHS is one of the prefixes used by other elements in the hosting model.</span></span>

