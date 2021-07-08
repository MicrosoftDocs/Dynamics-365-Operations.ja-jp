---
title: テーブル マップ拡張
description: テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。
author: MichaelFruergaardPontoppidan
ms.date: 12/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: fec5b918d2d35e70dadaf39cee73edb25cebe889
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193395"
---
# <a name="table-map-extension"></a><span data-ttu-id="af9db-103">テーブル マップ拡張</span><span class="sxs-lookup"><span data-stu-id="af9db-103">Table map extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af9db-104">テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="af9db-104">To extend table maps, we have refactored table maps into a model, which allows you to extend a solution with additional fields and methods.</span></span> <span data-ttu-id="af9db-105">このトピックでは、テーブルのマップを拡張するためのモデルが必要な理由を説明します。</span><span class="sxs-lookup"><span data-stu-id="af9db-105">This topic discusses why you need a model to extend a table map.</span></span>

<span data-ttu-id="af9db-106">拡張機能を使用して既存のテーブル マップにフィールドを追加すると、いくつかの問題が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="af9db-106">Adding a field to an existing table map through extension can present some challenges.</span></span> <span data-ttu-id="af9db-107">実装時にこれらの問題に対処しない場合は、ランタイム エラーになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="af9db-107">If these issues are not addressed during the implementation, there can be runtime errors.</span></span> <span data-ttu-id="af9db-108">エラーは、開発者がテーブル マップの実装に関連するすべてのテーブルを変更できないために発生します。</span><span class="sxs-lookup"><span data-stu-id="af9db-108">The errors occur because the developer cannot modify all the tables that are involved in implementing the table map.</span></span> <span data-ttu-id="af9db-109">メソッドがテーブル マップ上でインスタンス メソッドとして直接呼び出された場合、メソッドをテーブル マップに追加する場合も同じです。</span><span class="sxs-lookup"><span data-stu-id="af9db-109">The same is true for adding a method to a table map if the method is called directly as an instance method on the table map.</span></span> <span data-ttu-id="af9db-110">テーブル マップのフィールドがどのようにテーブル マップを実装するすべてのテーブルのフィールドにマップされる必要があるかを、強制する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="af9db-110">There is no way to enforce how fields on table maps must be mapped to fields on all tables that implement the table map.</span></span> <span data-ttu-id="af9db-111">同様に、テーブル マップのメソッドがどのようにテーブル マップを実装するすべてのテーブルのメソッドにマップされる必要があるかを、強制する方法はありません。</span><span class="sxs-lookup"><span data-stu-id="af9db-111">Similarly, there is no way to enforce how methods on table maps must be also be methods on all tables that implement the table map.</span></span>

<span data-ttu-id="af9db-112">次の図は、**SalesPurchTable** テーブル マップを示しています。これは、**ApplicationSuite** モデルの **SalesTable**、**PurchTable**、および **SalesBasket** テーブルによって実装されています。</span><span class="sxs-lookup"><span data-stu-id="af9db-112">The following diagram shows the **SalesPurchTable** table map, which is implemented by the **SalesTable**, **PurchTable**, and **SalesBasket** tables in the **ApplicationSuite** model.</span></span> <span data-ttu-id="af9db-113">さらに、**ISV1Header** テーブルは **SalesPurchTable** テーブル マップを実装しますが、**ISV1Header** は **ISVModule1** モデルの一部です。</span><span class="sxs-lookup"><span data-stu-id="af9db-113">In addition, the **ISV1Header** table implements the **SalesPurchTable** table map, but **ISV1Header** is part of an **ISVModule1** model.</span></span>

![MapExtensionsProblem](media/MapExtensions1.png)

<span data-ttu-id="af9db-115">たとえば、**AccountingGroupId** という名前の新しいフィールドおよび **validateAccountingGroup** という名前の新しいメソッドが **ApplicationSuite** モデルでテーブル マップに追加されます。それから、そのテーブル マップを実装するテーブルは、フィールドおよび追加されるメソッドも含むよう更新できます。</span><span class="sxs-lookup"><span data-stu-id="af9db-115">For example, if a new field named **AccountingGroupId** and a new method named **validateAccountingGroup** are added to the table map in the **ApplicationSuite** model, then the tables that you implement the table map can be updated to include the field and method added as well.</span></span> <span data-ttu-id="af9db-116">ただし、**ISVModule1** モデルの **ISV1Header** テーブルは、開発者が **ApplicationSuite** モデルに変更を加えるコントロールの外にあります。</span><span class="sxs-lookup"><span data-stu-id="af9db-116">The **ISV1Header** table in the **ISVModule1** model is, however, outside of the control of the developer making the changes to the **ApplicationSuite** model.</span></span>

![MapExtensionsProblem](media/MapExtensions2.png)

<span data-ttu-id="af9db-118">ビジネス ロジックを **ApplicationSuite** モデルに追加する場合、そのロジックは新しい **AccountingGroupId** フィールドをクエリし、テーブル マップ レコードのタイプが **ISV1Header** である場合、ランタイム エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="af9db-118">If you add business logic to the **ApplicationSuite** model, and that logic queries the new **AccountingGroupId** field and the table map record is of type **ISV1Header**, a runtime error occurs.</span></span>

```xpp
SalesPurchTable      headerTable;
...
...
if (headerTable.AccountingGroupId)
```

<span data-ttu-id="af9db-119">同様に、ビジネス ロジックを **ApplicationSuite** モデルに追加する場合、およびそのロジックが **validateAccountingGroup** を照会する場合、ランタイム エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="af9db-119">Similarly, if you add business logic to the **ApplicationSuite** model, and that logic queries **validateAccountingGroup**, then a runtime error occurs.</span></span>

```xpp
SalesPurchTable      headerTable;
...
...
if (headerTable.validateAccountingGroup())
```

<span data-ttu-id="af9db-120">結果として、新しいフィールドにマッピングを追加して新しいメソッドを **ISV1Header** テーブルに追加しない限り、ソリューションは破損します。</span><span class="sxs-lookup"><span data-stu-id="af9db-120">As a result, the solution is broken, unless you add mapping to the new field and add the new method to the **ISV1Header** table.</span></span> 

<span data-ttu-id="af9db-121">フィールドまたはメソッドを追加する機能が拡張機能を介してテーブル マップに追加された場合は、競合は解決されません。</span><span class="sxs-lookup"><span data-stu-id="af9db-121">The conflict is not resolved if the ability to add fields or methods is added to table maps through extension.</span></span> <span data-ttu-id="af9db-122">これは、**ISVModule2** に **ApplicationSuite** モデルのテーブル マップと実装テーブルの拡張が含まれている次の図に示されています。</span><span class="sxs-lookup"><span data-stu-id="af9db-122">This is illustrated in the following diagram, where **ISVModule2** includes extensions of the table map and the implementing tables in the **ApplicationSuite** model.</span></span> <span data-ttu-id="af9db-123">**ISVModule2** を実装する開発者は、**ISVModule1** モデルの **ISV1Header** テーブルを制御できません。**ISV1Header** テーブルには、**AccountingGroupId** フィールドのマッピングと **validateAccountingGroup** メソッドの実装がありません。</span><span class="sxs-lookup"><span data-stu-id="af9db-123">The developer implementing **ISVModule2** has no control over the **ISV1Header** table in the **ISVModule1** model, so the **ISV1Header** table lacks a mapping of the **AccountingGroupId** field and implementation of the **validateAccountingGroup** method.</span></span>

![MapExtensionsProblem](media/MapExtensions3.png)

<span data-ttu-id="af9db-125">コンパイラがテーブル マップのすべてのフィールドとメソッドを、テーブル マップを実装するすべてのテーブルにマップする必要がある場合でも、競合は解決されません。</span><span class="sxs-lookup"><span data-stu-id="af9db-125">Even if the the compiler enforced that all fields and methods on a table map must be mapped to all tables implementing the table map, the conflict would not be resolved.</span></span> <span data-ttu-id="af9db-126">マップされた新しいフィールドまたは実装された新しいメソッドがないテーブルは、追加されたフィールド/メソッドを含むモデルが適用されるときにコンパイルするため、ランタイム エラーを受け取る代わりに、フィールドまたはメソッドを追加することで重大な変更をクリアします。</span><span class="sxs-lookup"><span data-stu-id="af9db-126">Instead of receiving runtime errors, adding a field or a method would clear a breaking change, as tables not having a new field mapped or a new method implemented would compile when the model containing the added field/method is applied.</span></span> <span data-ttu-id="af9db-127">テーブル マップを拡張するために、テーブル マップをモデルにリファクタリングしました。追加のフィールドとメソッドを使用してソリューションを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="af9db-127">To extend table maps, we have refactored table maps into a model, which allows you to extend a solution with additional fields and methods.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]