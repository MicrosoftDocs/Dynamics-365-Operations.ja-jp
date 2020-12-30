---
title: 手持在庫データ エンティティの拡張
description: このトピックでは、INVENTORSITEONHANDENTITY と INVENTWAREHOUSEONHANDENTITY ビューに拡張フィールドを追加して、手持在庫データ エンティティの機能が拡張で使用できるようにする例を示します。
author: sherry-zheng
manager: tfehr
ms.date: 07/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-27
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e3bf3a7d48b0aa3e48845882be0ee86da17ed040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432034"
---
# <a name="extend-inventory-on-hand-data-entities"></a><span data-ttu-id="9b59d-103">手持在庫データ エンティティの拡張</span><span class="sxs-lookup"><span data-stu-id="9b59d-103">Extend inventory on-hand data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b59d-104">Microsoft Dynamics 365 Supply Chain Management には、[拡張機能を使用してテーブルにフィールドを追加](../../fin-ops-core/dev-itpro/extensibility/add-field-extension) できる [拡張性](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) 機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="9b59d-104">Microsoft Dynamics 365 Supply Chain Management provides [extensibility](../../fin-ops-core/dev-itpro/extensibility/extensibility-home-page.md) features that let you [add fields to tables through extension](../../fin-ops-core/dev-itpro/extensibility/add-field-extension).</span></span> <span data-ttu-id="9b59d-105">このトピックでは、`INVENTORSITEONHANDENTITY` と `INVENTWAREHOUSEONHANDENTITY` ビューに拡張フィールドを追加して、手持在庫データ エンティティの機能が拡張で使用できるようにする例を示します。</span><span class="sxs-lookup"><span data-stu-id="9b59d-105">This topic provides an example that shows how to add extended fields to the `INVENTORSITEONHANDENTITY` and `INVENTWAREHOUSEONHANDENTITY` views, so that the capabilities of the inventory on-hand data entities can work with the extensions.</span></span> <span data-ttu-id="9b59d-106">データ エンティティの詳細については、[データ管理の概要](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b59d-106">For more information about data entities, see [Data management overview](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).</span></span>

> [!NOTE]
> <span data-ttu-id="9b59d-107">手持在庫データ エンティティの一覧を以下に示します:</span><span class="sxs-lookup"><span data-stu-id="9b59d-107">Here is a list of some of the inventory on-hand data entities:</span></span>
>
> - <span data-ttu-id="9b59d-108">サイトごとの手持在庫</span><span class="sxs-lookup"><span data-stu-id="9b59d-108">Inventory on-hand by site</span></span>
> - <span data-ttu-id="9b59d-109">サイトごとの手持在庫 V2</span><span class="sxs-lookup"><span data-stu-id="9b59d-109">Inventory on-hand by site V2</span></span>
> - <span data-ttu-id="9b59d-110">倉庫ごとの手持在庫</span><span class="sxs-lookup"><span data-stu-id="9b59d-110">Inventory on-hand by warehouse</span></span>
> - <span data-ttu-id="9b59d-111">倉庫別手持在庫 v2</span><span class="sxs-lookup"><span data-stu-id="9b59d-111">Inventory on-hand by warehouse v2</span></span>

<span data-ttu-id="9b59d-112">`inventSiteOnHandView` ビューによって使用されるテーブルにフィールドを追加した後、拡張機能が正しく認識されるようにエンジンを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b59d-112">After you add fields to tables that are used by the `inventSiteOnHandView` view, you must sync the engine so that the extensions are correctly recognized.</span></span>

1. <span data-ttu-id="9b59d-113">拡張子フィールドを追加して、`InventSiteOnHandView` ビューを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9b59d-113">Extend the `InventSiteOnHandView` view by adding the extension field.</span></span>
1. <span data-ttu-id="9b59d-114">拡張子フィールドで `InventSiteOnHandAggregatedView` ビューを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9b59d-114">Extend the `InventSiteOnHandAggregatedView` view with the extension fields.</span></span>
1. <span data-ttu-id="9b59d-115">`getExtensionFields()` メソッドを変更して、`InventSiteOnHandAggregatedViewBuilder` viewBuilder クラスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="9b59d-115">Extend the `InventSiteOnHandAggregatedViewBuilder` viewBuilder class by modifying the `getExtensionFields()` method.</span></span> <span data-ttu-id="9b59d-116">このようにして、viewBuilder の同期が実行されたときに、古いビュー フィールドを新しいビュー フィールドにマップします。</span><span class="sxs-lookup"><span data-stu-id="9b59d-116">In this way, you map old view fields to new view fields when viewBuilder synchronization is run.</span></span>

<span data-ttu-id="9b59d-117">たとえば、拡張機能を使用して、次の 4 つのフィールドを `InventTable` テーブルに追加したとします。</span><span class="sxs-lookup"><span data-stu-id="9b59d-117">For example, you've added the following four fields to the `InventTable` table through extension:</span></span>

- <span data-ttu-id="9b59d-118">カスタム フィールド 1</span><span class="sxs-lookup"><span data-stu-id="9b59d-118">Custom field 1</span></span>
- <span data-ttu-id="9b59d-119">カスタム フィールド 2</span><span class="sxs-lookup"><span data-stu-id="9b59d-119">Custom field 2</span></span>
- <span data-ttu-id="9b59d-120">カスタム フィールド 3</span><span class="sxs-lookup"><span data-stu-id="9b59d-120">Custom field 3</span></span>
- <span data-ttu-id="9b59d-121">カスタム フィールド 4</span><span class="sxs-lookup"><span data-stu-id="9b59d-121">Custom field 4</span></span>

<span data-ttu-id="9b59d-122">この場合は、次の方法で `getExtensionFields()` メソッドを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b59d-122">In the case, you must modify the `getExtensionFields()` method in the following way.</span></span>

```xpp
[ExtensionOf(classStr(InventSiteOnHandAggregatedViewBuilder))]
public final class InventOnHandAggregatedViewBuilder\_Extension
{
    protected Map getExtensionFields()
    {
        next getExtensionFields();
        Map extensionFields = new Map(Types::Int64, Types::Int64);
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 1), fieldNum(InventSiteOnHandAggregatedView, Custom field 1));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 2), fieldNum(InventSiteOnHandAggregatedView, Custom field 2));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 3), fieldNum(InventSiteOnHandAggregatedView, Custom field 3));
        extensionFields.insert(fieldNum(InventSiteOnHandView, Custom field 4), fieldNum(InventSiteOnHandAggregatedView, Custom field 4));
        return extensionFields;
    }
}
```

<span data-ttu-id="9b59d-123">これらの手順を完了した後で、新しいフィールドを追加することで、サイト別の手持在庫と倉庫データ エンティティ別の手持在庫を拡張できます。</span><span class="sxs-lookup"><span data-stu-id="9b59d-123">After you complete these steps, you can extend the inventory on-hand by site and inventory on-hand by warehouse data entities by adding the new fields.</span></span> <span data-ttu-id="9b59d-124">このようにして、これらのデータ エンティティを使用するデータ移行中に、拡張フィールドが認識されて含まれるようにします。</span><span class="sxs-lookup"><span data-stu-id="9b59d-124">In this way, you ensure that the extended fields are recognized and included during data migration that uses those data entities.</span></span>
