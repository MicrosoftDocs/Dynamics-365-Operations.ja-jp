---
title: インターフェイスとして使用されるテーブル マップの拡張
description: このトピックでは、インターフェイスとして使用されるテーブル マップを拡張する方法について説明します。
author: LarsBlaaberg
manager: AnnBe
ms.date: 12/10/2017
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
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: 56b20f2440668f6f04f31b63f3000499669c1027
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512064"
---
# <a name="extend-table-maps-that-are-used-as-interfaces"></a><span data-ttu-id="2be04-103">インターフェイスとして使用されるテーブル マップの拡張</span><span class="sxs-lookup"><span data-stu-id="2be04-103">Extend table maps that are used as interfaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2be04-104">**SalesPurchLine** および **SalesPurchTable** テーブル マップは、さまざまな製品機能により使用される一般的なフィールドおよびメソッドのセットを公開します。</span><span class="sxs-lookup"><span data-stu-id="2be04-104">The **SalesPurchLine** and **SalesPurchTable** table maps expose a set of common fields and methods that are used by a variety of product features.</span></span> <span data-ttu-id="2be04-105">フィールドのマッピングとメソッドの実装は、クラス階層にリファクタリングされています。</span><span class="sxs-lookup"><span data-stu-id="2be04-105">The mapping of fields and the implementation of methods have been refactored into a class hierarchy.</span></span> <span data-ttu-id="2be04-106">変更の一部は以下のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2be04-106">Some of these changes include:</span></span>
- <span data-ttu-id="2be04-107">テーブル マップのメソッドは、クラス階層に移動されました。</span><span class="sxs-lookup"><span data-stu-id="2be04-107">Methods on the table maps have been moved to the class hierarchy.</span></span>
- <span data-ttu-id="2be04-108">フィールドは、クラス階層で parm メソッドを通して公開されます。</span><span class="sxs-lookup"><span data-stu-id="2be04-108">Fields are exposed through parm-methods on the class hierarchy.</span></span>
- <span data-ttu-id="2be04-109">テーブル マップは引き続き存在し、テーブル マップへのマッピングも引き続き実装されていますが、テーブル マップのフィールドは廃止され、フィールド マッピングは削除されています。</span><span class="sxs-lookup"><span data-stu-id="2be04-109">The table map still exists and tables still implement the mapping to the table map, but the fields on the table map have been made obsolete, and field mapping has been removed.</span></span>
- <span data-ttu-id="2be04-110">テーブル マップ上のメソッドは廃止されました。</span><span class="sxs-lookup"><span data-stu-id="2be04-110">The methods on the table map have been made obsolete.</span></span>

## <a name="salespurchtableinterface-hierarchy"></a><span data-ttu-id="2be04-111">SalesPurchTableInterface 階層</span><span class="sxs-lookup"><span data-stu-id="2be04-111">SalesPurchTableInterface hierarchy</span></span>

<span data-ttu-id="2be04-112">新しい **SalesPurchTableInterface** クラスは、**SalesPurchTable** テーブル マップのリファクタリングによって導入された ApplicationSuite 機能の抽象基本クラスです。</span><span class="sxs-lookup"><span data-stu-id="2be04-112">The new **SalesPurchTableInterface** class is the abstract base class for the ApplicationSuite functionality that has been introduced by the refactoring of the **SalesPurchTable** table map.</span></span> <span data-ttu-id="2be04-113">このクラスにはフィールドとメソッドの抽象メソッドが含まれています。これらはインターフェイスを実装する各テーブルに存在している必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-113">The class contains abstract methods for fields and methods, which must exist for each table implementing the interface.</span></span> <span data-ttu-id="2be04-114">これにより、メソッドに既定のロジックを含めることができ、すべての実装においてよく用いられます。</span><span class="sxs-lookup"><span data-stu-id="2be04-114">It also contains the default logic in methods, which is common across all implementations.</span></span> <span data-ttu-id="2be04-115">**SalesPurchTable** テーブル マップを実装する各テーブルは、**SalesPurchTableInterface** クラスの階層の派生クラスとして表す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-115">Each table that implements the **SalesPurchTable** table map must be represented as a derived class in the **SalesPurchTableInterface** class hierarchy.</span></span> <span data-ttu-id="2be04-116">各派生クラスは、**SalesPurchTableInterfaceFactory** 属性クラスで修飾される必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-116">Each derived class must be decorated with a **SalesPurchTableInterfaceFactory** attribute class.</span></span> <span data-ttu-id="2be04-117">属性を使用して派生クラスをテーブルに関連付けます。これで、**SalesPurchTable** レコードに応じて、適切なタイプのクラスのインスタンスを作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="2be04-117">The attribute is used to associate the derived class with the table, so that it is possible to instantiate a class of the correct type depending on a **SalesPurchTable** record.</span></span>

![MapsAsInterfaces](media/MapsAsInterfaces1.png)

<span data-ttu-id="2be04-119">テーブル マップ メソッドが廃止されたにもかかわらず、対応するメソッドはまだ実装テーブルに存在します。</span><span class="sxs-lookup"><span data-stu-id="2be04-119">Even though the table map methods have been made obsolete, the corresponding methods still exist on the implementing tables.</span></span> <span data-ttu-id="2be04-120">これらのメソッドのロジックは、テーブル マップのメソッドへの呼び出しを階層の基本クラスの対応するメソッドにデリゲートすることからリファクタリングされています。</span><span class="sxs-lookup"><span data-stu-id="2be04-120">The logic in these methods have been refactored from delegating calls to the method on the table map, to the corresponding method on the base class of the hierarchy.</span></span>

## <a name="extension-scenario"></a><span data-ttu-id="2be04-121">拡張子シナリオ</span><span class="sxs-lookup"><span data-stu-id="2be04-121">Extension scenario</span></span>

<span data-ttu-id="2be04-122">この例では、ISVModule2 モデルによってインターフェイス クラス階層と **SalesPurchTable** テーブル マップを実装しているテーブルを拡張させる場合、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-122">In this example, if you want your ISVModule2 model to extend the interface class hierarchy and the tables implementing the **SalesPurchTable** table map, you must perform the following steps:</span></span>
1. <span data-ttu-id="2be04-123">**SalesPurchTable** テーブル マップを実装する必要なテーブルに、テーブル拡張機能を使用してフィールドとメソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2be04-123">Add the fields and methods through table extension to the necessary tables implementing the **SalesPurchTable** table map.</span></span>
2. <span data-ttu-id="2be04-124">新規のインターフェイス クラス階層を作成し、新しいフィールドを parm メソッドやその他の追加メソッドとして公開します。</span><span class="sxs-lookup"><span data-stu-id="2be04-124">Create a new interface class hierarchy, which exposes the new fields as parm-methods and other additional methods.</span></span> <span data-ttu-id="2be04-125">クラス階層構造の基本クラスは、具体的であり、抽象的ではない必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-125">The base class of the class hierarchy must be concrete and not abstract.</span></span>
3. <span data-ttu-id="2be04-126">拡張された各テーブルの派生クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2be04-126">Create derived classes for each table that has been extended.</span></span>
    1. <span data-ttu-id="2be04-127">各派生クラスを **SalesPurchTableInterfaceFactory** 属性クラスで修飾し、クラスを正しいテーブルに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="2be04-127">Decorate each derived class with the **SalesPurchTableInterfaceFactory** attribute class to associate the class with the correct table.</span></span>
    2. <span data-ttu-id="2be04-128">新しいクラス階層の基本クラスに静的ファクトリ メソッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="2be04-128">Create a static factory method on the base class of the new class hierarchy.</span></span> <span data-ttu-id="2be04-129">ファクトリ メソッドは、**SalesPurchTableInterfaceFactory** 属性を利用する適切な派生クラスをインスタンス化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-129">The factory method should instantiate the proper derived class that leverages the **SalesPurchTableInterfaceFactory** attribute.</span></span> <span data-ttu-id="2be04-130">派生クラスが見つからない場合は、基本クラスのインスタンスを戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2be04-130">If no derived class can be found, then an instance of the base class must be returned.</span></span>
4. <span data-ttu-id="2be04-131">**SalesPurchTableInterface** クラスの拡張クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="2be04-131">Create an extension class of the **SalesPurchTableInterface** class.</span></span> <span data-ttu-id="2be04-132">このクラスは、**SalesPurchTableInterface** クラスを、新しいクラス階層のファクトリ メソッドを呼び出して新しいクラス階層からインスタンスを作成するメソッドで補強します。</span><span class="sxs-lookup"><span data-stu-id="2be04-132">The class augments the **SalesPurchTableInterface** class with a method that creates an instance from the new class hierarchy by calling the factory method on the new class hierarchy.</span></span>
    
<span data-ttu-id="2be04-133">上記のクラスと拡張機能は、次の図に示されています。</span><span class="sxs-lookup"><span data-stu-id="2be04-133">The class and extensions described above are shown in the following diagram.</span></span>

![MapsAsInterfacesWalkThrough](media/MapsAsInterfaces2.png)

<span data-ttu-id="2be04-135">この図には、**SalesPurchTable** を実装する **ISV1Header** テーブルを含み、独自の **SalesPurchTableInterface** 派生クラスを含む ISVModule1 モデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2be04-135">The diagram contains an ISVModule1 model, which includes the **ISV1Header** table that implements the **SalesPurchTable** table map and contains its own **SalesPurchTableInterface** derived class.</span></span> <span data-ttu-id="2be04-136">このモデルは ISVModule2 から独立しているため、ISVModule2 のロジックが、**ISV2SalesPurchTableInterface** クラス階層からインスタンスを作成すると、**SalesPurchTable** レコードが **ISV1Header** タイプの場合に基本クラスのインスタンスが返されます。</span><span class="sxs-lookup"><span data-stu-id="2be04-136">The model is independent of the ISVModule2, so when logic in the ISVModule2 creates an instance from the **ISV2SalesPurchTableInterface** class hierarchy, then an instance of the base class will be returned when the **SalesPurchTable** record is of type **ISV1Header**.</span></span> <span data-ttu-id="2be04-137">基本クラスのメソッドが、未知のテーブルに対して適切な結果を返す場合、同じインストール内で 2 つの ISV モデルが共存します。</span><span class="sxs-lookup"><span data-stu-id="2be04-137">If the methods on the base class return a reasonable result for unknown tables, then the two ISV models will co-exist within the same installation.</span></span>
