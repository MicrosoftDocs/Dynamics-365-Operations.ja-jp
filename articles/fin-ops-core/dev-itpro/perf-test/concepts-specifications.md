---
title: 詳細のクラス
description: このトピックでは、詳細のクラスに関する情報を提供します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 03/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: MichaelFruergaardPontoppidan
ms.search.validFrom: 2018-XX-XX
ms.dyn365.ops.version: App Update 10.0.2
ms.openlocfilehash: 696834d934f10d9e9040466044d2692085dd729a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183094"
---
# <a name="specification-classes"></a><span data-ttu-id="171ef-103">詳細のクラス</span><span class="sxs-lookup"><span data-stu-id="171ef-103">Specification classes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="171ef-104">詳細のクラスはエンティティが満たすべき一連の条件の定義に使用される Fluent アプリケーション プログラミング インターフェイス (API) を提供します。</span><span class="sxs-lookup"><span data-stu-id="171ef-104">A specification class provides fluent application programming interfaces (APIs) that are used to define the set of criteria that an entity should meet.</span></span> <span data-ttu-id="171ef-105">詳細は検証シナリオでよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="171ef-105">Specifications are often used in validation scenarios.</span></span> <span data-ttu-id="171ef-106">通常それらはクエリ クラスと一緒に使用されます。</span><span class="sxs-lookup"><span data-stu-id="171ef-106">They are usually used together with query classes.</span></span>

<span data-ttu-id="171ef-107">詳細のクラスの利点は、検証コードが非常に簡潔で表現的になることです。</span><span class="sxs-lookup"><span data-stu-id="171ef-107">An advantage of specification classes is that the validation code becomes very concise and expressive.</span></span> <span data-ttu-id="171ef-108">基本的に 1 行のコードで複数の検証を行えます。</span><span class="sxs-lookup"><span data-stu-id="171ef-108">Basically, you can do multiple validations in a single line of code.</span></span>

## <a name="naming-convention"></a><span data-ttu-id="171ef-109">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="171ef-109">Naming convention</span></span>

`AtlSpec<ModuleName><#EntityName>`

<span data-ttu-id="171ef-110">この命名規則で:</span><span class="sxs-lookup"><span data-stu-id="171ef-110">In this naming convention:</span></span>

- <span data-ttu-id="171ef-111">`<ModuleName>` はオプションで、メイン メニューのモジュール名に基づいています。</span><span class="sxs-lookup"><span data-stu-id="171ef-111">`<ModuleName>` is optional and is based on the names of the modules on the main menu.</span></span> <span data-ttu-id="171ef-112">ただし、短いテスト コードをサポートするために、短いバージョンまたは省略形を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="171ef-112">However, a short version or an abbreviation should be used to support brevity of test code.</span></span>
- <span data-ttu-id="171ef-113">`<#EntityName>` は承認テスト ライブラリ (ATL) 全体で使用されるエンティティ名を表します。</span><span class="sxs-lookup"><span data-stu-id="171ef-113">`<#EntityName>` represents the name of the entity that is used throughout the Acceptance test library (ATL).</span></span>

## <a name="examples"></a><span data-ttu-id="171ef-114">例</span><span class="sxs-lookup"><span data-stu-id="171ef-114">Examples</span></span>

```
AtlSpecWHSLoadLine

AtlSpecWHSWorkLine
```

## <a name="implementation"></a><span data-ttu-id="171ef-115">実装</span><span class="sxs-lookup"><span data-stu-id="171ef-115">Implementation</span></span>

<span data-ttu-id="171ef-116">詳細のクラスは仕様のさまざまな条件を指定する Fluent セッター メソッドを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="171ef-116">Specification classes should provide fluent setter methods to specify various criteria of the specification.</span></span>

### <a name="example"></a><span data-ttu-id="171ef-117">例</span><span class="sxs-lookup"><span data-stu-id="171ef-117">Example</span></span>

<span data-ttu-id="171ef-118">次のコードは、指定された条件を満たす 6 行が作業に含まれることを確認します。</span><span class="sxs-lookup"><span data-stu-id="171ef-118">The following code verifies that the work contains six lines that meet the specified criteria.</span></span> <span data-ttu-id="171ef-119">たとえば、1 行目は **1** の行番号として **1** を、作業タイプとして **ピッキング** を、数量として **1** を、状態として **終了済み** を、場所として **一括** を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="171ef-119">For example, the first line should have **1** as the line number of **1**, **Pick** as the work type, **1** as the quantity, **Closed** as the status, and **bulk** as the location.</span></span>

```
work.lines().assertExpectedLines(
    workLines.spec().withLineNum(1).withWorkType(WHSWorkType::Pick).setQuantity(1).setStatus(WHSWorkStatus::Closed).setLocation(locations.bulk()),
    workLines.spec().withLineNum(2).withWorkType(WHSWorkType::Pick).setQuantity(1).setStatus(WHSWorkStatus::Closed).setLocation(locations.floor()),
    workLines.spec().withLineNum(3).withWorkType(WHSWorkType::Put) .setQuantity(2).setStatus(WHSWorkStatus::Closed).setLocation(locations.stage()),
    workLines.spec().withLineNum(4).withWorkType(WHSWorkType::Pick).setQuantity(2).setStatus(WHSWorkStatus::Cancelled).setLocation(locations.stage()),
    workLines.spec().withLineNum(5).withWorkType(WHSWorkType::Put).setQuantity(2).setStatus(WHSWorkStatus::Cancelled)
);
```
