---
title: ER モデルおよび形式のデータ バインディングにおける相対パスの使用
description: .
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable , ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: a026eec379f98fd32080df50b5e114b423db34ad
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182810"
---
# <a name="use-a-relative-path-in-data-bindings-of-er-models-and-formats"></a><span data-ttu-id="62bff-103">ER モデルおよび形式のデータ バインディングにおける相対パスの使用</span><span class="sxs-lookup"><span data-stu-id="62bff-103">Use a relative path in data bindings of ER models and formats</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="62bff-104">電子申告 (ER) ツールは、ユーザーが電子フォーマット構造を定義できるようにし、アプリケーションに存在するデータとアルゴリズムを使用してこれらの構造を入力する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="62bff-104">The Electronic reporting (ER) tool lets users define electronic format structures and then describe how those structures should be filled by using data and algorithms that exist in the application.</span></span> <span data-ttu-id="62bff-105">詳細については、[電子申告 (ER) コンフィギュレーションの作成](electronic-reporting-configuration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="62bff-105">For more information, see [Create Electronic reporting (ER) configurations](electronic-reporting-configuration.md).</span></span> <span data-ttu-id="62bff-106">Finance and Operations のデータを取得し、それを使用して電子ドキュメントを生成するためのデータ フローを指定するには、以下を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bff-106">To specify the data flow for retrieving Finance and Operations data and using it to generate  an electronic document, you need to do the following:</span></span>

- <span data-ttu-id="62bff-107">設計されたドメイン固有のデータ モデルの要素に対するコンフィギュレーションされたデータ ソースをバインドします。</span><span class="sxs-lookup"><span data-stu-id="62bff-107">Bind configured data sources to elements of the designed domain-specific data model.</span></span> <span data-ttu-id="62bff-108">モデル構造と選択されたデータ ソースは、複雑な階層構造の一部であることがあります。</span><span class="sxs-lookup"><span data-stu-id="62bff-108">The model structure and selected data sources might be part of a complex hierarchical structure.</span></span> <span data-ttu-id="62bff-109">このため、最終バインディングは非常に大きくなり、異なるタイプのさまざまな要素 (たとえば、関係、テーブル、およびメソッド) を含むことがあります。</span><span class="sxs-lookup"><span data-stu-id="62bff-109">Because of this, final bindings can be quite large and contain many elements of different types (for example, relations, tables, and methods,).</span></span> <span data-ttu-id="62bff-110">バインディングは読み取れず、特に所有者でない場合、確認や把握が非常に複雑になることがあります。</span><span class="sxs-lookup"><span data-stu-id="62bff-110">The bindings can become less readable and quite complex to review and understand, especially for non-owners.</span></span> 
- <span data-ttu-id="62bff-111">データ モデル要素と形式コンポーネントをバインドして、データ モデルから生成された形式の出力に設定するデータを定義します。</span><span class="sxs-lookup"><span data-stu-id="62bff-111">Bind data model elements with format components to define what data will be populated from the data model to the generated format’s output.</span></span>

<span data-ttu-id="62bff-112">ER マッピング デザイナーの使用可能性を改善するために、相対パス機能がリリースされました。</span><span class="sxs-lookup"><span data-stu-id="62bff-112">To improve usability of ER mapping designers, the relative path feature has been released.</span></span> <span data-ttu-id="62bff-113">既定では、ER デザイン エクスペリエンスが有効になっているアプリケーションのすべての新しいインスタンスに対して、相対パスの表示オプションが有効になっています (Microsoft Dynamics 365 Finance、Microsoft Regulatory Configuration Service)。</span><span class="sxs-lookup"><span data-stu-id="62bff-113">By default, the relative path representation option is turned on for any new instance of the application where ER design experience is enabled (Microsoft Dynamics 365 Finance, Microsoft Regulatory Configuration Service).</span></span> <span data-ttu-id="62bff-114">この ER バインディングのプレゼンテーションと共に動作している時に、フル パスを使用しつづけられるように、相対パス パラメータを実装しています。</span><span class="sxs-lookup"><span data-stu-id="62bff-114">We implemented the relative path parameter so that users can keep using the full path when work with this presentation of ER bindings.</span></span>

<span data-ttu-id="62bff-115">[![ユーザー パラメーター](./media/relative-path-01.png)](./media/relative-path-01.png)</span><span class="sxs-lookup"><span data-stu-id="62bff-115">[![User parameters](./media/relative-path-01.png)](./media/relative-path-01.png)</span></span>

 
<span data-ttu-id="62bff-116">相対パス使用パラメーターが有効になっている場合、1 つの文字 @ は現在のモデル要素のバインドの親項目へのパスに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="62bff-116">When the relative path usage parameter is turned on, a single @ character replaces the path to the parent item in the binding of the current model element.</span></span> <span data-ttu-id="62bff-117">バインド パス全体が短くなり、マッピング全体がより明確で、理解しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="62bff-117">The entire binding path becomes shorter, which makes the entire mapping more obvious and easier to understand.</span></span> <span data-ttu-id="62bff-118">ほとんどの場合、データ モデルのすべてのバインドを表示するために ER デザイナーにおいて追加でスクロールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="62bff-118">In most cases, no additional scrolling is required in the ER designer to view all the bindings of the data model.</span></span>

<span data-ttu-id="62bff-119">[![モデル マッピング デザイナー](./media/relative-path-02.png)](./media/relative-path-02.png)</span><span class="sxs-lookup"><span data-stu-id="62bff-119">[![Model mapping designer](./media/relative-path-02.png)](./media/relative-path-02.png)</span></span>
 
<span data-ttu-id="62bff-120">新しい ER 式のデザインを開始する場合、文字を 1 つ入力するだけで親項目のフィールドへのバインドを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="62bff-120">When you start designing a new ER expression, you need to enter only one character to define a binding to a field of the parent item.</span></span>

<span data-ttu-id="62bff-121">[![フォーミュラ デザイナー](./media/relative-path-03.png)](./media/relative-path-03.png)</span><span class="sxs-lookup"><span data-stu-id="62bff-121">[![Formula designer](./media/relative-path-03.png)](./media/relative-path-03.png)</span></span>
 
<span data-ttu-id="62bff-122">絶対パスを使用して親モデル項目のデータ ソースを変更する場合、入れ子になったすべての項目と共に、このモデル項目を新しいデータ ソースに手動で再バインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="62bff-122">When you decide to change the data source of the parent model item, with absolute path usage, you have to manually rebind this model item, as well as all nested items, to a new data source.</span></span> <span data-ttu-id="62bff-123">相対パスの使用が有効になっていて、親項目にバインドされる新しいデータ ソースを選択した場合、この親項目に入れ子になっているすべての要素をワン クリックで自動的に再バインドできるオプションが提供されます。</span><span class="sxs-lookup"><span data-stu-id="62bff-123">When relative path usage is turned on, and you select a new data source to be bound to a parent item, you are offered an option to automatically rebind all nested elements of this parent item with one click.</span></span>

<span data-ttu-id="62bff-124">[![既存のパス メッセージの置換](./media/relative-path-04.png)](./media/relative-path-04.png)</span><span class="sxs-lookup"><span data-stu-id="62bff-124">[![Replace existing path message](./media/relative-path-04.png)](./media/relative-path-04.png)</span></span>
 
<span data-ttu-id="62bff-125">入れ子になった項目の再バインドを確定すると、既存の親項目も含め、入れ子になった各項目のパスに新しい親項目が配置されます。</span><span class="sxs-lookup"><span data-stu-id="62bff-125">If you confirm rebinding of nested items, the new parent item will be placed to the path of each nested item containing the existing parent item.</span></span>
<span data-ttu-id="62bff-126">この機能は ER フレームワークの下位互換性を損なうことはありません。</span><span class="sxs-lookup"><span data-stu-id="62bff-126">This feature does not break the backward compatibility of the ER framework.</span></span> <span data-ttu-id="62bff-127">以前に設計されたすべての ER コンフィギュレーションは、この新しい機能と共に動作し、アップグレードや変換は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="62bff-127">All previously designed ER configurations will work with this new feature, and no upgrades or conversions are required.</span></span>

> [!NOTE]
> <span data-ttu-id="62bff-128">モデル マッピングで入れ子になっている要素のバインディングを大量に変更することによって生じるすべての変更は、コンフィギュレーションの差分 (変更の追跡) に正しく保存されます。</span><span class="sxs-lookup"><span data-stu-id="62bff-128">All changes that are introduced by mass modification of bindings of nested elements in model mappings are correctly saved in a configuration delta (trace of changes).</span></span> <span data-ttu-id="62bff-129">これにより、顧客はモデル マッピングの派生バージョンを、この新しい機能を使用して変更された新しいベース バージョンに再ベースすることができます。</span><span class="sxs-lookup"><span data-stu-id="62bff-129">This allows customers to rebase their derived version of model mappings to any new base version of it that has been modified by using this new feature.</span></span>
