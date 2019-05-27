---
title: 承認テスト ライブラリの作成者
description: このトピックでは承認テスト ライブラリの作成者に関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: RobinARH
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 1e4254f638ee0a04bfc95a1ee952940f2e803deb
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537141"
---
# <a name="creators-in-the-acceptance-test-library"></a><span data-ttu-id="30282-103">承認テスト ライブラリの作成者</span><span class="sxs-lookup"><span data-stu-id="30282-103">Creators in the Acceptance test library</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="30282-104">作成者クラスは、テスト データの作成に使用される Fluent アプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="30282-104">Creator classes provide fluent application programming interfaces (APIs) that are used to create test data.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="30282-105">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="30282-105">Naming convention</span></span>

`AtlCreator<ModuleName><EntityName>`

<span data-ttu-id="30282-106">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="30282-106">In this naming convention:</span></span>

+ <span data-ttu-id="30282-107">`<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="30282-107">`<ModuleName>` is optional and is based on the names of the modules on the main menu.</span></span> <span data-ttu-id="30282-108">短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30282-108">You should use a short version or an abbreviation to support brevity of test code.</span></span>
+ <span data-ttu-id="30282-109">`<EntityName>` はオプションであり、コマンドが異なる種類のエンティティに適用される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="30282-109">`<EntityName>` is optional and is used when the command applies to different types of entities.</span></span>

## <a name="examples"></a><span data-ttu-id="30282-110">例</span><span class="sxs-lookup"><span data-stu-id="30282-110">Examples</span></span>

```
AtlCreatorCostGroup

AtlCreatorCustomer
```

## <a name="fluent-setter-methods"></a><span data-ttu-id="30282-111">Fluent セッター メソッド</span><span class="sxs-lookup"><span data-stu-id="30282-111">Fluent setter methods</span></span>

<span data-ttu-id="30282-112">作成者クラスは、構築中のエンティティのプロパティの設定に使用する Fluent セッター メソッドを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30282-112">Creator classes should provide fluent setter methods that are used to set the properties of the entity that is being constructed.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="30282-113">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="30282-113">Naming convention</span></span>

`set<EntityPropertyName>`

<span data-ttu-id="30282-114">この命名規則では、`<EntityPropertyName>` は Fluent メソッドを使用してエンティティに設定されるプロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="30282-114">In this naming convention, `<EntityPropertyName>` is the name of the property that is being set for the entity by using the fluent method.</span></span>

### <a name="example"></a><span data-ttu-id="30282-115">例</span><span class="sxs-lookup"><span data-stu-id="30282-115">Example</span></span>

```
item = new AtlCreatorProductItem()
    .setItemId('DemoItem')
    .setItemGroup(invent.itemGroups().carAudio())
    .setItemModelGroup(invent.modelGroups().fifo())
    .setStorageDimGroup(invent.storageDimGroups().siteWarehousePhysical())
    .setTrackingDimGroup(invent.trackingDimGroups().serialControlled())
    .setDefaultWarehouse(invent.warehouses().default())
    .create();
```

## <a name="when-should-creators-be-used-instead-of-entities"></a><span data-ttu-id="30282-116">エンティティの代わりに作成者を使用するのはいつですか。</span><span class="sxs-lookup"><span data-stu-id="30282-116">When should creators be used instead of entities?</span></span>

<span data-ttu-id="30282-117">エンティティと作成者を選択するのに役立つ情報は、[エンティティまたは作成者クラスを実装する必要があるか](atl-faq.md#should-i-implement-an-entity-or-a-creator-class) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="30282-117">For information that will help you choose between entities and creators, see [Should I implement an entity or a creator class](atl-faq.md#should-i-implement-an-entity-or-a-creator-class).</span></span>
