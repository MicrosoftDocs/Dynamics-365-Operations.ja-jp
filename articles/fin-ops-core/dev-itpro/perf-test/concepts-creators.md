---
title: 承認テスト ライブラリの作成者
description: このトピックでは承認テスト ライブラリの作成者に関する情報を提供します。
author: MichaelFruergaardPontoppidan
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2019-03-27
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 6d19cee4522f6c830b9f551471b3fe977f8da161
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866208"
---
# <a name="creators-in-the-acceptance-test-library"></a><span data-ttu-id="37dbc-103">承認テスト ライブラリの作成者</span><span class="sxs-lookup"><span data-stu-id="37dbc-103">Creators in the Acceptance test library</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37dbc-104">作成者クラスは、テスト データの作成に使用される Fluent アプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="37dbc-104">Creator classes provide fluent application programming interfaces (APIs) that are used to create test data.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="37dbc-105">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="37dbc-105">Naming convention</span></span>

`AtlCreator<ModuleName><EntityName>`

<span data-ttu-id="37dbc-106">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="37dbc-106">In this naming convention:</span></span>

+ <span data-ttu-id="37dbc-107">`<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="37dbc-107">`<ModuleName>` is optional and is based on the names of the modules on the main menu.</span></span> <span data-ttu-id="37dbc-108">短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37dbc-108">You should use a short version or an abbreviation to support brevity of test code.</span></span>
+ <span data-ttu-id="37dbc-109">`<EntityName>` はオプションであり、コマンドが異なる種類のエンティティに適用される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="37dbc-109">`<EntityName>` is optional and is used when the command applies to different types of entities.</span></span>

## <a name="examples"></a><span data-ttu-id="37dbc-110">例</span><span class="sxs-lookup"><span data-stu-id="37dbc-110">Examples</span></span>

```xpp
AtlCreatorCostGroup

AtlCreatorCustomer
```

## <a name="fluent-setter-methods"></a><span data-ttu-id="37dbc-111">Fluent セッター メソッド</span><span class="sxs-lookup"><span data-stu-id="37dbc-111">Fluent setter methods</span></span>

<span data-ttu-id="37dbc-112">作成者クラスは、構築中のエンティティのプロパティの設定に使用する Fluent セッター メソッドを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="37dbc-112">Creator classes should provide fluent setter methods that are used to set the properties of the entity that is being constructed.</span></span>

### <a name="naming-convention"></a><span data-ttu-id="37dbc-113">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="37dbc-113">Naming convention</span></span>

`set<EntityPropertyName>`

<span data-ttu-id="37dbc-114">この命名規則では、`<EntityPropertyName>` は Fluent メソッドを使用してエンティティに設定されるプロパティ名です。</span><span class="sxs-lookup"><span data-stu-id="37dbc-114">In this naming convention, `<EntityPropertyName>` is the name of the property that is being set for the entity by using the fluent method.</span></span>

### <a name="example"></a><span data-ttu-id="37dbc-115">例</span><span class="sxs-lookup"><span data-stu-id="37dbc-115">Example</span></span>

```xpp
item = new AtlCreatorProductsReleasedVariant()
    .setItemId('DemoItem')
    .setColor(ecoResColor)
    .setStyle(ecoResStyle)
    .setConfig(ecoResConfig)
    .setSize(ecoResSize)
    .create();
```

## <a name="when-should-creators-be-used-instead-of-entities"></a><span data-ttu-id="37dbc-116">エンティティの代わりに作成者を使用するのはいつですか。</span><span class="sxs-lookup"><span data-stu-id="37dbc-116">When should creators be used instead of entities?</span></span>

<span data-ttu-id="37dbc-117">エンティティと作成者を選択するのに役立つ情報は、[エンティティまたは作成者クラスを実装する必要があるか](atl-faq.md#should-i-implement-an-entity-or-a-creator-class) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="37dbc-117">For information that will help you choose between entities and creators, see [Should I implement an entity or a creator class](atl-faq.md#should-i-implement-an-entity-or-a-creator-class).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]