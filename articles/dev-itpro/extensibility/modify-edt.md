---
title: "拡張データ型の変更"
description: "拡張機能を使用して、拡張データ型 (EDT) で複数のプロパティをカスタマイズすることができます。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 9
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 494df508b7615f956afbd3935eab14b26191a719
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="modify-an-extended-data-type"></a><span data-ttu-id="a22bc-103">拡張データ型の変更</span><span class="sxs-lookup"><span data-stu-id="a22bc-103">Modify an extended data type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a22bc-104">既存の拡張データ型 (EDT) で拡張機能を使用してカスタマイズできるプロパティがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="a22bc-104">There are several properties that can be customized on existing extended data types (EDTs) through extension:</span></span>
- <span data-ttu-id="a22bc-105">ラベル</span><span class="sxs-lookup"><span data-stu-id="a22bc-105">Label</span></span>
- <span data-ttu-id="a22bc-106">ヘルプ テキスト</span><span class="sxs-lookup"><span data-stu-id="a22bc-106">Help text</span></span>
- <span data-ttu-id="a22bc-107">フォーム ヘルプ</span><span class="sxs-lookup"><span data-stu-id="a22bc-107">Form help</span></span>
- <span data-ttu-id="a22bc-108">国地域コード</span><span class="sxs-lookup"><span data-stu-id="a22bc-108">Country region codes</span></span>
- <span data-ttu-id="a22bc-109">文字列サイズ</span><span class="sxs-lookup"><span data-stu-id="a22bc-109">String size</span></span> 
    + <span data-ttu-id="a22bc-110">EDT が別の EDT から拡張されない場合、値のみを修正することができます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-110">You can only modify the value if the EDT does not extend from another EDT.</span></span>
    + <span data-ttu-id="a22bc-111">新しい文字列のサイズは、基準 EDT 値に等しい値または超える値にのみセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-111">You can only set the new String size to a value equal to or larger than the base EDT value.</span></span>

<span data-ttu-id="a22bc-112">プロパティ シートを使用して、新たに追加された要素のと同様にプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="a22bc-112">You modify the properties as you would for newly added elements, using the property sheet.</span></span>

![EDT の変更](media/EDT01.jpg) 
 
<span data-ttu-id="a22bc-114">コードをコンパイルした後、アプリケーションで変更を確認できます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-114">After compiling the code, you can see the changes in the application.</span></span>

![EDT の変更](media/EDT02.jpg) 

<span data-ttu-id="a22bc-116">Visual Studio のアプリケーション エクスプ ローラーでは作成された拡張機能を表示できます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-116">You can view the created extensions in the Application Explorer in Visual Studio.</span></span>

![EDT の変更](media/EDT03.jpg) 

## <a name="if-the-edt-is-modified-in-more-than-one-model"></a><span data-ttu-id="a22bc-118">1 つ以上のモデルで EDT が変更される場合</span><span class="sxs-lookup"><span data-stu-id="a22bc-118">If the EDT is modified in more than one model</span></span>
<span data-ttu-id="a22bc-119">複数の ISV に同じ拡張データ型がある場合、最上位モデル ID を持つモデルから EDT のプロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-119">If multiple ISVs have extended the same extended data type, the properties of the EDT from the model with the highest Model ID will be used.</span></span> <span data-ttu-id="a22bc-120">たとえば、ISV 1 が モデル AwesomeModel with ID 12 で「Awesome 品目番号」に ItemId のラベルを変更し、ISV 2 がモデル SuperModel with ID 15 で「Super 品目番号」に ItemId のラベルを変更した場合、エンドユーザーはユーザー インターフェイスで「品目番号」の代わりに「Awesome 品目番号」を表示します。</span><span class="sxs-lookup"><span data-stu-id="a22bc-120">For example, if ISV 1 modified the label of ItemId to “Awesome item number” in model AwesomeModel with ID 12, while ISV 2 modified the label of ItemId to “Super item number” in model SuperModel with ID 15, the end user would see “Awesome item number” in the user interface instead of “Item number”.</span></span>

> [!TIP]
> <span data-ttu-id="a22bc-121">既存の EDT を拡張する代わりに、既存の EDT から派生する新しいものを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-121">Instead of extending an existing EDT, you can create a new one, deriving it from the existing EDT.</span></span> <span data-ttu-id="a22bc-122">これにより、拡張方法を使用して編集するよりも多くのプロパティを編集できます。</span><span class="sxs-lookup"><span data-stu-id="a22bc-122">This allows you to edit more properties than you could edit using the extension approach.</span></span> <span data-ttu-id="a22bc-123">つまり、新しい EDT を使用するには、この EDT を使用してフィールドを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a22bc-123">This means that you would need to modify the fields using this EDT to use your new EDT.</span></span>


