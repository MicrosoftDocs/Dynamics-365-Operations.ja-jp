---
title: 拡張機能を使用してテーブルに関係を追加
description: このトピックでは、テーブルにリレーションを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: db426b2349414db4fb1adcaf6007c642dd668618
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369769"
---
# <a name="add-relations-to-tables-through-extension"></a><span data-ttu-id="f7e34-103">拡張機能を使用してテーブルに関係を追加</span><span class="sxs-lookup"><span data-stu-id="f7e34-103">Add relations to tables through extension</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7e34-104">複数のテーブルにあるデータとの高機能かつ安全な相互作用を可能にするには、2 つのテーブル間のリンクを記述するリレーションを定義して参照整合性を保証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7e34-104">To enable rich and secure interactions with data in multiple tables, you must help guarantee referential integrity by defining relations that describe the link between two tables.</span></span> <span data-ttu-id="f7e34-105">関係を定義することにより、入力されたデータの検証および関連情報のルックアップ機能を有効にできます。</span><span class="sxs-lookup"><span data-stu-id="f7e34-105">By defining relations, you enable validation of the data that is entered and lookup capabilities for the related information.</span></span> 

<span data-ttu-id="f7e34-106">テーブルを拡張することにより新しいリレーションを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="f7e34-106">You can add a new relation by extending a table.</span></span>

<span data-ttu-id="f7e34-107">次の例では、新しいフィールド **MyInventLocationId** が InventTable テーブルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="f7e34-107">In the following example, a new field, **MyInventLocationId**, is added to the InventTable table.</span></span> <span data-ttu-id="f7e34-108">このフィールドは、倉庫が含まれる InventLocation テーブルへの参照です。</span><span class="sxs-lookup"><span data-stu-id="f7e34-108">This field is a reference to the InventLocation table that contains warehouses.</span></span>

1. <span data-ttu-id="f7e34-109">新しい拡張モデルで、InventTable テーブルの拡張機能を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7e34-109">In the new extension model, create an extension of the InventTable table.</span></span>
1. <span data-ttu-id="f7e34-110">通常のテーブルにリレーションを作成するのと同じように、新しいリレーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7e34-110">Create a new relation, just as you would create a relation on a regular table.</span></span>
1. <span data-ttu-id="f7e34-111">**関連テーブル**、**関係タイプ**、**カーディナリティ** プロパティと、関係に適用される他のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7e34-111">Specify the **Related Table**, **Relationship Type**, and **Cardinality** properties, and any other properties that apply to the relation.</span></span>
1. <span data-ttu-id="f7e34-112">同じ値を持つ InventTable テーブルと InventLocation テーブルからフィールドを指定してリンクを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7e34-112">Add the link by specifying the fields from the InventTable table and the InventLocation table that have the same value.</span></span> <span data-ttu-id="f7e34-113">この場合、フィールドは InventTable テーブルでは **MyInventLocationId** であり、InventLocation テーブルでは **InventLocationId** となります。</span><span class="sxs-lookup"><span data-stu-id="f7e34-113">In this case, the fields are **MyInventLocationId** in the InventTable table and **InventLocationId** in the InventLocation table.</span></span>

<span data-ttu-id="f7e34-114">次の図は、新しいリレーションを示しています。</span><span class="sxs-lookup"><span data-stu-id="f7e34-114">The following illustration shows the new relation.</span></span>

![新しい関係](media/AddRelationToExistingTable.jpg)
