---
title: クライアント側の設計 API
description: このトピックでは、クライアント側での設計のための API の概要と、それらの使用に関する推奨事項について説明します。
author: makhabaz
manager: AnnBe
ms.date: 07/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 255544
ms.assetid: ''
ms.search.region: Global
ms.author: makhabaz
ms.search.validFrom: 2017-07-20
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: 97a1279bab499d72897ef3d71898cbcd6d23dcb5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368902"
---
# <a name="client-side-design-apis"></a><span data-ttu-id="c3b40-103">クライアント側の設計 API</span><span class="sxs-lookup"><span data-stu-id="c3b40-103">Client-side design APIs</span></span>

[!include [banner](../../../includes/banner.md)]

<span data-ttu-id="c3b40-104">このトピックでは、クライアント側での設計のためのプリケーション プログラミング インターフェイス (API) の概要と、それらの使用に関する推奨事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="c3b40-104">This topic provides an overview of the application programming interfaces (APIs) for client-side design and includes recommendations for using them.</span></span>

## <a name="terminology"></a><span data-ttu-id="c3b40-105">用語</span><span class="sxs-lookup"><span data-stu-id="c3b40-105">Terminology</span></span>
<span data-ttu-id="c3b40-106">次のリストには、クライアント側の設計 API に適用される用語がいくつか含まれています。</span><span class="sxs-lookup"><span data-stu-id="c3b40-106">The following list includes some frequently used terms that apply to the client-side design APIs.</span></span>

- <span data-ttu-id="c3b40-107">**デザイン** - 既定デザインを上書きするためにページ、アクション、またはその他のコンポーネント オブジェクトで必要に応じて指定できるプロパティ。</span><span class="sxs-lookup"><span data-stu-id="c3b40-107">**Design** – A property that can optionally be specified on a Page, Action, or other component object to override its default design.</span></span>
- <span data-ttu-id="c3b40-108">**コンポーネント** - コンポーネントには、次の 4 つのタイプがあります。</span><span class="sxs-lookup"><span data-stu-id="c3b40-108">**Component** – A component can be one of four types:</span></span>

  - <span data-ttu-id="c3b40-109">**ブロック コンテナー** (既定) - CSS ブロック動作を持つコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="c3b40-109">**Block container** (default) – A container that has CSS block behaviors.</span></span> <span data-ttu-id="c3b40-110">(つまり、コンテナーは、CSS **display: block** スタイル申告を持つ要素に相当します。)</span><span class="sxs-lookup"><span data-stu-id="c3b40-110">(In other words, the container is equivalent to an element that has a CSS **display: block** style declaration.)</span></span>
  - <span data-ttu-id="c3b40-111">**フレックス コンテナー** – CSS フレックス動作のあるコンテナー。</span><span class="sxs-lookup"><span data-stu-id="c3b40-111">**Flex container** – A container that has CSS flex behaviors.</span></span> <span data-ttu-id="c3b40-112">(つまり、コンテナーは、CSS **display: flex** スタイル申告を持つ要素に相当します。)</span><span class="sxs-lookup"><span data-stu-id="c3b40-112">(In other words, the container is equivalent to an element that has a CSS **display: flex** style declaration.)</span></span>
  - <span data-ttu-id="c3b40-113">**コントロール参照** - ページまたはアクションの静的メタデータ (XML) に存在するコントロールを参照するコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="c3b40-113">**Control reference** – A component that refers to a control that exists in the static metadata (XML) of the Page or Action.</span></span>
  - <span data-ttu-id="c3b40-114">**新しいコントロール** – 新しいコントロールをインスタンス化するコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="c3b40-114">**New control** – A component that instantiates a new control.</span></span> <span data-ttu-id="c3b40-115">(つまり、コントロールは、ページまたはアクションの静的メタデータ [XML] にはまだ存在しません。)</span><span class="sxs-lookup"><span data-stu-id="c3b40-115">(In other words, the control doesn't already exist in the static metadata [XML] of the Page or Action.)</span></span>

    <span data-ttu-id="c3b40-116">コンポーネントは JavaScript Object Notation (JSON) オブジェクトによってデザイン内に表され、この JSON オブジェクトのプロパティは、コンポーネントのプロパティを表します。</span><span class="sxs-lookup"><span data-stu-id="c3b40-116">A component is represented in the design by a JavaScript Object Notation (JSON) object, and the properties of this JSON object represent the properties of the component.</span></span> <span data-ttu-id="c3b40-117">デザイン プロパティ階層のほとんどすべての JSON オブジェクトはコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="c3b40-117">Almost every JSON object in the design property hierarchy is a component.</span></span>

- <span data-ttu-id="c3b40-118">**項目** – コンテナーに入れ子にされたコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="c3b40-118">**Item** – A component that is nested in a container.</span></span>
- <span data-ttu-id="c3b40-119">**プロパティ** – コンポーネントで複数のタイプのプロパティを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-119">**Property** – Several types of properties can be set on a component:</span></span>

  - <span data-ttu-id="c3b40-120">コンテナー固有</span><span class="sxs-lookup"><span data-stu-id="c3b40-120">Container-specific</span></span>
  - <span data-ttu-id="c3b40-121">品目固有</span><span class="sxs-lookup"><span data-stu-id="c3b40-121">Item-specific</span></span>
  - <span data-ttu-id="c3b40-122">コントロール固有</span><span class="sxs-lookup"><span data-stu-id="c3b40-122">Control-specific</span></span>
  - <span data-ttu-id="c3b40-123">リスト固有</span><span class="sxs-lookup"><span data-stu-id="c3b40-123">List-specific</span></span>
  - <span data-ttu-id="c3b40-124">一般 (不特定)</span><span class="sxs-lookup"><span data-stu-id="c3b40-124">Generic (non-specific)</span></span>

    <span data-ttu-id="c3b40-125">プロパティは、コンポーネントの JSON オブジェクトのキーと値のペアとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-125">Properties are specified as key-value pairs on the component's JSON object.</span></span> <span data-ttu-id="c3b40-126">適用可能なプロパティは、プロパティが適用されるコンポーネントのタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="c3b40-126">The properties that are applicable depend on the type of component that the property is applied to.</span></span>

    <span data-ttu-id="c3b40-127">使用可能な値の定義済リストを持つプロパティについては、ドキュメントで示されている最初の値がプロパティの既定値です。</span><span class="sxs-lookup"><span data-stu-id="c3b40-127">For properties that have a predefined list of possible values, the first value that is shown in the documentation is the property's default value.</span></span> <span data-ttu-id="c3b40-128">ほとんどの場合、プロパティをまったく指定していない (つまり、JSON オブジェクトからのプロパティを省略する) 場合、プロパティは既定値を設定していた場合と同じように動作します。</span><span class="sxs-lookup"><span data-stu-id="c3b40-128">In most cases, if you don't specify a property at all (that is, if you omit the property from the JSON object), the property behaves as if you had set its default value.</span></span>

    <span data-ttu-id="c3b40-129">一般的なプロパティは、すべてのコンポーネントのタイプに適用できます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-129">Generic properties can be applied to all component types.</span></span>

    <span data-ttu-id="c3b40-130">プロパティを指定するときは、次のガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="c3b40-130">When you specify properties, follow these guidelines:</span></span>

  - <span data-ttu-id="c3b40-131">プロパティ名は引用符で囲まないでください。</span><span class="sxs-lookup"><span data-stu-id="c3b40-131">You should not enclose property names in quotation marks.</span></span>
  - <span data-ttu-id="c3b40-132">ドキュメントでそれ以外が指定されない限り、すべてのプロパティ値を二重引用符で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="c3b40-132">You must enclose all property values in double quotation marks, unless the documentation specifies otherwise.</span></span>

- <span data-ttu-id="c3b40-133">**継承** – コントロールに色、フォントサイズ、またはフォントの太さが適用されている場合、すべての子孫コントロールは再割り当てされない限り、同じプロパティを継承します。</span><span class="sxs-lookup"><span data-stu-id="c3b40-133">**Inheritance** – If a color, font size, or font weight is applied to a control, all descendant controls inherit the same property, unless they are reassigned.</span></span> <span data-ttu-id="c3b40-134">コントロールにスペースを適用する場合は、コントロールの品目 (非コンテナー) 子孫によって継承されます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-134">If padding is applied to a control, it's inherited by the item (non-container) descendants of the control.</span></span> <span data-ttu-id="c3b40-135">その他のプロパティは継承されません。</span><span class="sxs-lookup"><span data-stu-id="c3b40-135">No other properties are inherited.</span></span>

## <a name="using-design-apis"></a><span data-ttu-id="c3b40-136">設計 API の使用</span><span class="sxs-lookup"><span data-stu-id="c3b40-136">Using design APIs</span></span>
<span data-ttu-id="c3b40-137">次のコードは、予約管理の例のビジネス ロジック コードの変更されたセグメントです。</span><span class="sxs-lookup"><span data-stu-id="c3b40-137">The following code is a modified segment of business logic code from a Reservation Management example.</span></span> <span data-ttu-id="c3b40-138">具体的には、このコードは、引当の詳細ページのデザインを指定する変数から取得されます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-138">Specifically, this code is from a variable that specifies the design for a reservation details page.</span></span> <span data-ttu-id="c3b40-139">コメントはコードに含まれており、いくつかの可能性を強調します。</span><span class="sxs-lookup"><span data-stu-id="c3b40-139">Comments are included in the code to highlight a few possibilities.</span></span>

> [!NOTE]
> <span data-ttu-id="c3b40-140">コントロールに適用される色、フォント サイズ、またはフォントの太さはコントロールのすべての子にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-140">Any color, font size, or font weight that is applied to a control is also applied to all children of that control.</span></span> <span data-ttu-id="c3b40-141">埋め込みは、コンテナー以外の子によって継承されます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-141">Padding is inherited by non-container children.</span></span> <span data-ttu-id="c3b40-142">その他のプロパティは継承されません。</span><span class="sxs-lookup"><span data-stu-id="c3b40-142">No other properties are inherited.</span></span> <span data-ttu-id="c3b40-143">コンテナーにはリスト、ページ、グループ、およびパーツが含まれます。</span><span class="sxs-lookup"><span data-stu-id="c3b40-143">Containers include lists, pages, groups, and parts.</span></span>

<span data-ttu-id="c3b40-144">子または品目を持たないコントロールを作成した後、コントロール名は引用符で囲む必要があります (次のコードの **FMCustomer\_FullName** を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="c3b40-144">After a control is created that doesn't have any children or items, the control name just has to be written in quotation marks (see **FMCustomer\_FullName** in the following code).</span></span> <span data-ttu-id="c3b40-145">ただし、任意のカスタマイズがコントロールに適用される場合、コードはブロックされる必要があり、**名前**ラベルを使用する必要があります (次のコードで **FMCustomer\_画像**を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="c3b40-145">However, if any customization will be applied to that control, the code must be blocked, and the **name** label must be used (see **FMCustomer\_Image** in the following code).</span></span>

```
// Page root container
"flexFlow":"column nowrap",
"items":[
    // Upper third of page, contains 4 rows
    {
        "flexFlow":"column nowrap",
        "background":"theme", // set background color to the theme color
        "color":"light",      // set the foreground (e.g. font) color to light
        "fontSize":"small",
        "border": "none",
        "padding":"small",
        "items":[
            // Row 1/4 with customer image and name
            {
                "flexFlow":"row nowrap",
                "alignItems":"center",
                "justifyItems":"center",
                "labelStyle":"hidden", // don't show label for field
                "fontSize":"large",
                "fontWeight":"bold",
                "items":[
                    {
                    // Customer image – since we're modifying the imageStyle, etc., this
                    // code must be blocked and the "FMCustomer_Image" must be labeled
                    // with "name".
                        "name":"FMCustomer_Image",
                        "imageStyle":"circular",
                        height:3,
                        width:3
                    },
                    // don't need to create a new object or use the "name" label if
                    // there is no customization
                    "FMCustomer_FullName",
                ]
            },
            // Row 2/4 with vehicle description
            . . .
        }
    }
```

<span data-ttu-id="c3b40-146">次の図は、前のコードで生成された顧客画像、顧客名、フォント、背景色などを示しています。</span><span class="sxs-lookup"><span data-stu-id="c3b40-146">The following illustration shows the customer image, customer name, font, background color, and so on, that preceding code produces.</span></span>

![サンプル画像](media/detail-page.png)
