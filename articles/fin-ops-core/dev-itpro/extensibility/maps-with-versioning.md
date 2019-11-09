---
title: バージョン管理で使用されるテーブル マップの拡張
description: このトピックでは、バージョン管理に使用できるテーブル マップを拡張する方法について説明します。
author: LarsBlaaberg
manager: AnnBe
ms.date: 12/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 89563
ms.assetid: ''
ms.search.region: Global
ms.author: lolsen
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 11
ms.openlocfilehash: cb15f492b8ba2f6341babb95e1ca6ceeabdfdb1e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248828"
---
# <a name="extend-table-maps-that-are-used-for-versioning"></a><span data-ttu-id="5d906-103">バージョン管理で使用されるテーブル マップの拡張</span><span class="sxs-lookup"><span data-stu-id="5d906-103">Extend table maps that are used for versioning</span></span>

[!include [banner](../includes/banner.md)]

## <a name="purchlinemap-table-map-logic"></a><span data-ttu-id="5d906-104">PurchLineMap テーブル マップ ロジック</span><span class="sxs-lookup"><span data-stu-id="5d906-104">PurchLineMap table map logic</span></span>

<span data-ttu-id="5d906-105">テーブル拡張機能を使用して新しいフィールドが **PurchLine** および **PurchLineHistory** テーブルに追加された場合、発注書のバージョンが更新されるときに、新しいフィールドをテーブル間でコピーする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d906-105">When new fields are added to the **PurchLine** and **PurchLineHistory** tables using table extensions, the new fields must be copied between the tables when a purchase order is versioned.</span></span> <span data-ttu-id="5d906-106">**PurchLineMap** テーブル マップは、新しい購買注文バージョンが作成または編集されたときに **PurchLine** テーブルおよび **PurchLineHistory** テーブルの間でコピーする必要があるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="5d906-106">The **PurchLineMap** table map specifies the fields that must be copied between the **PurchLine** table and the **PurchLineHistory** table when a new purchase order version is created or edited.</span></span> <span data-ttu-id="5d906-107">これを行うためには、**PurchLineMap** マップ テーブルを拡張してフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d906-107">To accomplish this, extend the **PurchLineMap** map table to include the additional fields.</span></span> <span data-ttu-id="5d906-108">また、**PurchLineMap** は、購買注文明細行をアーカイブするとき、**VersioningPurchaseOrder** によって使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d906-108">Additionally, the **PurchLineMap** is used by the **VersioningPurchaseOrder** class when archiving purchase order lines.</span></span> <span data-ttu-id="5d906-109">このモデルを次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="5d906-109">The model is shown in the following diagram.</span></span>

![VersioningPurchaseOrder](media/MapsWithVersioning1.png)

<span data-ttu-id="5d906-111">コピーする新しいフィールドを指定できるようにするため、**PurchLineMap**テーブル マップ ロジックとその使用がリファクタリングされています。</span><span class="sxs-lookup"><span data-stu-id="5d906-111">To be able to specify new fields to be copied, the **PurchLineMap** table map logic and its usage have been refactored.</span></span> <span data-ttu-id="5d906-112">コピー ロジックが **PurchLineVersioning** 移動されているため、**VersioningPurchaseOrder** クラスは**PurchLineMap** テーブルマップの代わりに、**PurchLineVersioning** を参照します。</span><span class="sxs-lookup"><span data-stu-id="5d906-112">The copy logic has been moved to the **PurchLineVersioning** class, so the **VersioningPurchaseOrder** class references the **PurchLineVersioning** class instead of the **PurchLineMap** table map.</span></span> <span data-ttu-id="5d906-113">**PurchLineVersioning** クラスは、フィールドをコピーするロジックや、**PurchLineIVersioningFieldSet**インターフェイス を実行するクラスからの確認が必須かどうかを決定するロジックを委任します。</span><span class="sxs-lookup"><span data-stu-id="5d906-113">The **PurchLineVersioning** class delegates the logic to copy the fields and the logic to determine whether a confirmation is required from the classes that implement the **PurchLineIVersioningFieldSet** interface.</span></span> <span data-ttu-id="5d906-114">インターフェイスを実装する各クラスは、コピーするフィールドを指定するテーブル マップに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="5d906-114">Each class that implements the interface is associated with a table map that specifies the fields to copy.</span></span>

<span data-ttu-id="5d906-115">**PurchLineDictVersioning** クラスは、リフレクションを使用して **PurchLineIVersioningFieldSet** オブジェクトをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="5d906-115">The **PurchLineDictVersioning** class instantiates the **PurchLineIVersioningFieldSet** object using reflection.</span></span> <span data-ttu-id="5d906-116">**PurchLineDictVersioning** クラスは、コピーする必要があるフィールドのセット全体を収集します。</span><span class="sxs-lookup"><span data-stu-id="5d906-116">The **PurchLineDictVersioning** class collects the entire set of fields which need to be copied.</span></span> <span data-ttu-id="5d906-117">フィールドデータは、**PurchLineIVersioningFieldSet** を実装するクラスに関連付けられているすべてのテーブル マップに基づいて収集されます。</span><span class="sxs-lookup"><span data-stu-id="5d906-117">The field data is collected based on all the table maps associated with a class that implements **PurchLineIVersioningFieldSet**.</span></span> <span data-ttu-id="5d906-118">次の図は、新しいクラスとその依存関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="5d906-118">The following diagram displays the new classes and their dependencies.</span></span>

![ソリューション](media/MapsWithVersioning2.png)

## <a name="how-to-extend-purchline-and-purchlinehistory-tables-with-new-fields"></a><span data-ttu-id="5d906-120">新しいフィールドで PurchLine および PurchLineHistory テーブルを拡張する方法</span><span class="sxs-lookup"><span data-stu-id="5d906-120">How to extend PurchLine and PurchLineHistory tables with new fields</span></span>

<span data-ttu-id="5d906-121">発注書の新しいバージョンを作成するときにコピーする必要がある新しいフィールドを持つ **PurchLine** および **PurchLineHistory** テーブルを拡張するために、ISVModule2 モデルが必要であるとします。</span><span class="sxs-lookup"><span data-stu-id="5d906-121">Suppose that you want the ISVModule2 model to extend the **PurchLine** and **PurchLineHistory** tables with new fields that must be copied when creating a new version of a purchase order.</span></span> 

> [!NOTE] 
> <span data-ttu-id="5d906-122">ISVModule2 モデルに開発者がアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d906-122">You must have developer access to the ISVModule2 model.</span></span> 

<span data-ttu-id="5d906-123">このタスクを完了するには、次の手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d906-123">To complete this task, you must perform the following steps:</span></span>
1. <span data-ttu-id="5d906-124">**PurchLine** と **PurchLineHistory** テーブルへのテーブル拡張機能を使用して、フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="5d906-124">Add fields by using table extensions to the **PurchLine** and **PurchLineHistory** tables.</span></span>
2. <span data-ttu-id="5d906-125">コピーする必要があるフィールドを含む新しいテーブル マップを作成し、2 つの新しいテーブル拡張で新しいテーブル マップを実装します。</span><span class="sxs-lookup"><span data-stu-id="5d906-125">Create a new table map containing the fields that must be copied, and implement the new table map on the two new table extensions.</span></span>
3. <span data-ttu-id="5d906-126">新しいクラスを作成して **PurchLineIVersioningFieldSet** インターフェースを実装し、以下の必須メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="5d906-126">Create a new class to implement the **PurchLineIVersioningFieldSet** interface and implement the following required methods.</span></span>
    - <span data-ttu-id="5d906-127">**copyVersion** メソッド - 新しいテーブル マップの 2 つのレコード間でデータをコピーをします。</span><span class="sxs-lookup"><span data-stu-id="5d906-127">**copyVersion** method - Copies data between two records of the new table map type.</span></span>
    - <span data-ttu-id="5d906-128">**fieldSetTableMapId** メソッド - は新しいテーブルマップの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="5d906-128">**fieldSetTableMapId** method - Returns the ID of the new table map.</span></span>
    - <span data-ttu-id="5d906-129">**isChangeConfirmationRequired** メソッド - 新しく追加されたフィールド値が必要とする作成された確認への変更に基づいて、true または false を返します。</span><span class="sxs-lookup"><span data-stu-id="5d906-129">**isChangeConfirmationRequired** method - Returns true or false based on whether the change to the newly added field values requires a confirmation to be created.</span></span>

<span data-ttu-id="5d906-130">これらの手順で説明するクラス、インターフェイス、および拡張機能を次の図に示します。</span><span class="sxs-lookup"><span data-stu-id="5d906-130">The classes, interfaces, and extensions described in these steps are shown in the following diagram.</span></span>

![MapClassExtensions](media/TableMaps.png)
