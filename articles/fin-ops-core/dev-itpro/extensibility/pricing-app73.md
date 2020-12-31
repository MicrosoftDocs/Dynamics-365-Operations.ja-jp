---
title: 価格と割引の拡張性
description: このトピックでは、価格設定機能を展開する方法を説明します。
author: smithanataraj
manager: AnnBe
ms.date: 12/21/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2017-12-10
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: 373f1850ff27181cdcccf09dad7be5847c066200
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4409488"
---
# <a name="price-and-discount-extensibility"></a><span data-ttu-id="1dacf-103">価格と割引の拡張性</span><span class="sxs-lookup"><span data-stu-id="1dacf-103">Price and discount extensibility</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dacf-104">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 以降では、価格設定の領域が拡張します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-104">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 and later, the pricing area is extensible.</span></span> <span data-ttu-id="1dacf-105">価格と割引のいくつかの一般的なカスタマイズは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="1dacf-105">Some common customizations for price and discounts include:</span></span>
- <span data-ttu-id="1dacf-106">新しい価格タイプの検索メカニズムに加えて、新しい価格グループ タイプと対応する価格タイプ (**PriceType** と **PriceGroupType** の列挙値) を追加します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-106">Adding new price group types and the corresponding price types (enum values for **PriceType** and **PriceGroupType**), in addition to adding search mechanisms for the new price types.</span></span>
- <span data-ttu-id="1dacf-107">追加のパラメーターを **PriceDisc** クラスに渡すことを含め、価格と割引の検索を変更します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-107">Modifying the price and discount search, including passing in any additional parameters to the **PriceDisc** class.</span></span> 

## <a name="pricetype-and-pricegrouptype-enums"></a><span data-ttu-id="1dacf-108">PriceType および PriceGroupType 列挙</span><span class="sxs-lookup"><span data-stu-id="1dacf-108">PriceType and PriceGroupType enums</span></span>
<span data-ttu-id="1dacf-109">通常、新しいタイプの価格割引検索を追加すると、**PriceType** と **PriceGroupType** の 2 つの列挙型へ新しい列挙型値が追加されて開始します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-109">Typically, adding a new type of price discount search starts with adding a new enum value in the two enums: **PriceType** and **PriceGroupType**.</span></span> <span data-ttu-id="1dacf-110">拡張機能をサポートするために、**PriceType** と **PriceGroupType** の列挙型の値は、クラス階層 **PriceGroupTypeTradeAgreementMapping** と **PriceTypeTradeAgreementMapping** にそれぞれカプセル化されました。</span><span class="sxs-lookup"><span data-stu-id="1dacf-110">To support extensibility, **PriceType** and **PriceGroupType** enum values are now encapsulated in the class hierarchies **PriceGroupTypeTradeAgreementMapping** and **PriceTypeTradeAgreementMapping**, respectively.</span></span> <span data-ttu-id="1dacf-111">これらは、新しい **PriceType** および **PriceGroupType** 拡張列挙値に対して拡張できます。</span><span class="sxs-lookup"><span data-stu-id="1dacf-111">These can be extended for any new **PriceType** and **PriceGroupType** extended enum values.</span></span>

<span data-ttu-id="1dacf-112">**Customer**、**Vendor**、および **InventTable** テーブルの価格タイプに対応するフィールドのマッピングは、**PriceTypeTradeAgreementMapping** で定義されています。</span><span class="sxs-lookup"><span data-stu-id="1dacf-112">The mapping of fields on the **Customer**, **Vendor**, and **InventTable** tables that  correspond to the price types is defined in **PriceTypeTradeAgreementMapping**.</span></span> 

<span data-ttu-id="1dacf-113">次の図は、実装を強調表示しています。</span><span class="sxs-lookup"><span data-stu-id="1dacf-113">The following diagram highlights the implementation.</span></span> <span data-ttu-id="1dacf-114">メソッドはサブクラスを 1 つだけ示すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1dacf-114">Note that the methods show only one of the sub-classes.</span></span> <span data-ttu-id="1dacf-115">実装は、各サブクラスにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1dacf-115">The implementation needs to be on each sub-class.</span></span> 

![PriceGroupTypeTradeAgreementMapping](media/PricingFall20171.png)

## <a name="pricedisc-class"></a><span data-ttu-id="1dacf-117">PriceDisc クラス</span><span class="sxs-lookup"><span data-stu-id="1dacf-117">PriceDisc class</span></span>

<span data-ttu-id="1dacf-118">**PriceDisc** クラスは、価格と割引の検索エンジンです。</span><span class="sxs-lookup"><span data-stu-id="1dacf-118">The **PriceDisc** class is the search engine for price and discounts.</span></span> <span data-ttu-id="1dacf-119">このクラスは、**PriceDiscParameters** オブジェクトを、価格および割引検索で使用されるパラメーターを渡すメンバとして使用します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-119">This class uses a **PriceDiscParameters** object as a member for passing in the parameters that are used in the price and discount search.</span></span> <span data-ttu-id="1dacf-120">これにより、特定のソリューションの追加の検索パラメーターを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="1dacf-120">This enables you to pass in the additional search parameters for the specific solutions.</span></span> <span data-ttu-id="1dacf-121">特定の **PriceGroupType** 検索のパラメータのみ、**PriceDisc** クラスの対応する find メソッドを使用して渡されます。</span><span class="sxs-lookup"><span data-stu-id="1dacf-121">Only the parameters for a given **PriceGroupType** search are passed through the corresponding find methods on the **PriceDisc** class.</span></span> 

<span data-ttu-id="1dacf-122">**PriceDiscParameters** クラスのインスタンス化をラップし、変更する機能は、AppSuite 全体で実行されたすべての価格と割引の検索呼び出しで有効になっています。</span><span class="sxs-lookup"><span data-stu-id="1dacf-122">The ability to wrap and modify the instantiation of the **PriceDiscParameters** class is enabled for all price and discount search calls made throughout AppSuite.</span></span>

<span data-ttu-id="1dacf-123">次の図では、どのように **PriceDisc** クラスを拡張して、既存の検索を変更したり、拡張された **PriceType** 列挙値に対応する新しい検索メソッドを追加したりできるかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="1dacf-123">In the following diagram, you can see how the **PriceDisc** class can be extended to modify existing searches or to add new search methods that correspond to the extended **PriceType** enum values.</span></span>

![PriceDiscClass](media/PricingFall20172.png)

## <a name="add-a-new-price-search"></a><span data-ttu-id="1dacf-125">新しい価格検索の追加</span><span class="sxs-lookup"><span data-stu-id="1dacf-125">Add a new price search</span></span>

<span data-ttu-id="1dacf-126">このシナリオでは、**PriceGroupType** 列挙を新しい値 **PriceGroupTypeISVExtension**、および 2 つの対応する **PriceType** 列挙値である **ISVPurchPriceType** と **ISVSalesPriceType** で拡張しました。</span><span class="sxs-lookup"><span data-stu-id="1dacf-126">In this scenario, you have extended the **PriceGroupType** enum with a new value **PriceGroupTypeISVExtension**, and two corresponding **PriceType** enum values - **ISVPurchPriceType** and **ISVSalesPriceType**.</span></span> 

![WalkThrough1](media/PricingFall20173.png)

<span data-ttu-id="1dacf-128">次の図は、**PriceType** 値および **PriceGroupType** 値に対して新しい価格検索を追加する方法を示しています</span><span class="sxs-lookup"><span data-stu-id="1dacf-128">The following diagram illustrates how a new price search can be added for the **PriceType** and **PriceGroupType** values.</span></span>

![WalkThrough2](media/PricingFall20174.png)

<span data-ttu-id="1dacf-130">以下に例を示します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-130">This example shows the following:</span></span>

- <span data-ttu-id="1dacf-131">新しく作成された **PriceGroupType** 値については、属性 **ISVPriceGroupType** で修飾された **PriceGroupTypeTradeAgreementMappingISVPriceGroupType** クラスは、価格グループ タイプの動作を定義します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-131">For the newly created **PriceGroupType** value, a **PriceGroupTypeTradeAgreementMappingISVPriceGroupType** class decorated with the attribute **ISVPriceGroupType** defines the behavior of the price group type.</span></span>
- <span data-ttu-id="1dacf-132">新しく作成された **PriceType** 値については、**PriceTypeTradeAgreementMappingISVPurchPriceType** および **PriceTypeTradeAgreementMappingISVSalesPriceType** クラスは、購買および販売に対応します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-132">For the newly created **PriceType** value, the **PriceTypeTradeAgreementMappingISVPurchPriceType** and **PriceTypeTradeAgreementMappingISVSalesPriceType** classes correspond to Purchase and Sales.</span></span>
- <span data-ttu-id="1dacf-133">**PriceDiscParameters** クラスを拡張して価格割引検索の汎用パラメータを追加します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-133">Augmenting the **PriceDiscParameters** class to add any generic parameters for the price discount search.</span></span>
- <span data-ttu-id="1dacf-134">**PriceDisc** クラスを拡張して新しい価格タイプの新しい価格割引検索メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="1dacf-134">Augmenting the **PriceDisc** class to create the new price discount search methods for the new price types.</span></span>
- <span data-ttu-id="1dacf-135">**PriceDiscParameters** には、価格と割引の検索に関連するすべてのクラスからアクセスでき、これらは要件に基づいて拡張できます。</span><span class="sxs-lookup"><span data-stu-id="1dacf-135">The **PriceDiscParameters** is accessible from all classes related to price and discount search and these could be augmented, based on the requirements.</span></span> 
