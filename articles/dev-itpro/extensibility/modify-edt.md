---
title: "拡張データ型の変更"
description: "拡張機能を使用して、拡張データ型 (EDT) で複数のプロパティをカスタマイズすることができます。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 06/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: aa5eab6dbf2cc604239cac199817ead6bef6f3de
ms.openlocfilehash: 7f4e3699dd4cfaa3b37ab18d434c08cf827a976e
ms.contentlocale: ja-jp
ms.lasthandoff: 06/08/2018

---

# <a name="modify-an-extended-data-type"></a><span data-ttu-id="2d3cd-103">拡張データ型の変更</span><span class="sxs-lookup"><span data-stu-id="2d3cd-103">Modify an extended data type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d3cd-104">既存の拡張データ型 (EDT) で拡張機能を使用してカスタマイズできるプロパティがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-104">There are several properties that can be customized on existing extended data types (EDTs) through extension:</span></span>
- <span data-ttu-id="2d3cd-105">ラベル</span><span class="sxs-lookup"><span data-stu-id="2d3cd-105">Label</span></span>
- <span data-ttu-id="2d3cd-106">ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="2d3cd-106">Help text</span></span>
- <span data-ttu-id="2d3cd-107">フォーム ヘルプ</span><span class="sxs-lookup"><span data-stu-id="2d3cd-107">Form help</span></span>
- <span data-ttu-id="2d3cd-108">国地域コード</span><span class="sxs-lookup"><span data-stu-id="2d3cd-108">Country region codes</span></span>
- <span data-ttu-id="2d3cd-109">文字列サイズ</span><span class="sxs-lookup"><span data-stu-id="2d3cd-109">String size</span></span> 
    + <span data-ttu-id="2d3cd-110">EDT が別の EDT から拡張されない場合、値のみを修正することができます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-110">You can only modify the value if the EDT does not extend from another EDT.</span></span>
    + <span data-ttu-id="2d3cd-111">新しい文字列のサイズは、基準 EDT 値に等しい値または超える値にのみセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-111">You can only set the new String size to a value equal to or larger than the base EDT value.</span></span>

<span data-ttu-id="2d3cd-112">プロパティ シートを使用して、新たに追加された要素のと同様にプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-112">You modify the properties as you would for newly added elements, using the property sheet.</span></span>

![EDT の変更](media/EDT01.jpg) 
 
<span data-ttu-id="2d3cd-114">コードをコンパイルした後、アプリケーションで変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-114">After compiling the code, you can see the changes in the application.</span></span>

![EDT の変更](media/EDT02.jpg) 

<span data-ttu-id="2d3cd-116">Visual Studio のアプリケーション エクスプ ローラーでは作成された拡張機能を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-116">You can view the created extensions in the Application Explorer in Visual Studio.</span></span>

![EDT の変更](media/EDT03.jpg) 

## <a name="if-the-edt-is-modified-in-more-than-one-model"></a><span data-ttu-id="2d3cd-118">1 つ以上のモデルで EDT が変更される場合</span><span class="sxs-lookup"><span data-stu-id="2d3cd-118">If the EDT is modified in more than one model</span></span>
<span data-ttu-id="2d3cd-119">複数の ISV が同じ拡張データ型を拡張した場合は、モデル ID が最も高い (USR に最も近い) モデルの EDT のプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-119">If multiple ISVs have extended the same extended data type, the properties of the EDT from the model with the highest Model ID (closest to USR) will be used.</span></span> <span data-ttu-id="2d3cd-120">同じレイヤーに変更を加えた複数のモデルがある場合は、モデル ID の最も高いモデルからの変更が使用されます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-120">If there are multiple models with changes in the same layer, changes from the model with the highest Model ID will be used.</span></span> <span data-ttu-id="2d3cd-121">たとえば、ISV 1 が モデル AwesomeModel (USR レイヤー) with ID 15 で「Awesome 品目番号」に ItemId のラベルを変更し、ISV 2 がモデル SuperModel (USR レイヤー) with ID 12 で「Super 品目番号」に ItemId のラベルを変更した場合、エンドユーザーにはユーザー インターフェイスで「品目番号」の代わりに「Awesome 品目番号」と表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-121">For example, if ISV 1 modified the label of ItemId to “Awesome item number” in model AwesomeModel (USR layer) with ID 15, while ISV 2 modified the label of ItemId to “Super item number” in model SuperModel (USR layer) with ID 12, the end user would see “Awesome item number” in the user interface instead of “Item number”.</span></span>

> [!TIP]
> <span data-ttu-id="2d3cd-122">既存の EDT を拡張する代わりに、既存の EDT から派生する新しいものを作成できます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-122">Instead of extending an existing EDT, you can create a new one, deriving it from the existing EDT.</span></span> <span data-ttu-id="2d3cd-123">これにより、拡張方法を使用して編集するよりも多くのプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-123">This allows you to edit more properties than you could edit using the extension approach.</span></span> <span data-ttu-id="2d3cd-124">つまり、新しい EDT を使用するには、この EDT を使用してフィールドを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d3cd-124">This means that you would need to modify the fields using this EDT to use your new EDT.</span></span>


