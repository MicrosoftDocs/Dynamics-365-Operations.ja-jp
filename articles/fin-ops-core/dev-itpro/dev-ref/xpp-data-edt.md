---
title: X++ 拡張データ型
description: このトピックでは、X++の拡張データ型について説明します。
author: RobinARH
ms.date: 06/17/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150183
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aee2caa5133092a9b55ad5b36041a21cec4e0340
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866013"
---
# <a name="x-extended-data-types"></a><span data-ttu-id="ed700-103">X++ 拡張データ型</span><span class="sxs-lookup"><span data-stu-id="ed700-103">X++ extended data types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed700-104">このトピックでは、X++の拡張データ型について説明します。</span><span class="sxs-lookup"><span data-stu-id="ed700-104">This topic describes extended data types in X++.</span></span> 

<span data-ttu-id="ed700-105">*拡張データ型* は **ブール**、**int**、**int64**、**実数**、**str**、および **日付** プリミティブ データ型、および **コンテナー** 複合型に基づくユーザー定義型です。</span><span class="sxs-lookup"><span data-stu-id="ed700-105">*Extended data types* are user-defined types that are based on the **boolean**, **int**, **int64**, **real**, **str**, and **date** primitive data types, and on the **container** composite type.</span></span> <span data-ttu-id="ed700-106">EDT はプリミティブ データ型または補助名および追加のプロパティを持つコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ed700-106">An EDT is a primitive data type or container that has a supplementary name and additional properties.</span></span> <span data-ttu-id="ed700-107">たとえば、文字列を基準にして、**名前** という新しい EDT を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ed700-107">For example, you can create a new EDT that is named **Name** and base it on a string.</span></span> <span data-ttu-id="ed700-108">新しい EDT は、開発環境の変数とフィールド宣言で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ed700-108">You can then use the new EDT in variable and field declarations in the development environment.</span></span> 

<span data-ttu-id="ed700-109">また、EDT を他の EDT の基準にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ed700-109">You can also base EDTs on other EDTs.</span></span> <span data-ttu-id="ed700-110">EDTs は、標準的なデータ型ですが、特定の名前および追加のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="ed700-110">EDTs are standard data types, but they have a specific name and additional properties.</span></span> <span data-ttu-id="ed700-111">EDTs は、それらが基づいている標準データ型と同じ値とタイプ[換算](xpp-conversion-run-time-functions.md)を適用します。</span><span class="sxs-lookup"><span data-stu-id="ed700-111">EDTs undergo the same value and type [conversions](xpp-conversion-run-time-functions.md) as the standard data types that they are based on.</span></span> <span data-ttu-id="ed700-112">EDT の利点を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ed700-112">Here are the benefits of EDTs:</span></span>

-   <span data-ttu-id="ed700-113">変数は意味のあるデータ型を持つため、コードは読みやすくなります。</span><span class="sxs-lookup"><span data-stu-id="ed700-113">Code is easier to read, because variables have a meaningful data type.</span></span> <span data-ttu-id="ed700-114">たとえば、データ型は **str** の代わりに **名前** です。</span><span class="sxs-lookup"><span data-stu-id="ed700-114">For example, the data type is **Name** instead of **str**.</span></span>
-   <span data-ttu-id="ed700-115">EDT に設定するプロパティは、そのタイプのすべてのインスタンスで使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed700-115">The properties that you set for an EDT are used by all instances of that type.</span></span> <span data-ttu-id="ed700-116">したがって、EDT は作業を減らし、一貫性を促進するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ed700-116">Therefore, EDTs help reduce work and promote consistency.</span></span> <span data-ttu-id="ed700-117">たとえば、勘定番号 (**AccountNum** データ型) には、システム全体で同じプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="ed700-117">For example, account numbers (**AccountNum** data type) have the same properties throughout the system.</span></span>
-   <span data-ttu-id="ed700-118">EDT の階層を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="ed700-118">You can create hierarchies of EDTs.</span></span> <span data-ttu-id="ed700-119">EDT は、親から適切なプロパティを継承でき、その他のプロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ed700-119">The EDTs can inherit the appropriate properties from the parent, and you can change other properties.</span></span> <span data-ttu-id="ed700-120">たとえば、**ItemCode** データ型が、**MarkupItemCode** および **PriceDiscItemCode** データ型の基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="ed700-120">For example, the **ItemCode** data type is used as the basis for the **MarkupItemCode** and **PriceDiscItemCode** data types.</span></span>

## <a name="create-an-edt"></a><span data-ttu-id="ed700-121">EDT の作成</span><span class="sxs-lookup"><span data-stu-id="ed700-121">Create an EDT</span></span>

<span data-ttu-id="ed700-122">この機能は、言語コンストラクトとして実装されていません。</span><span class="sxs-lookup"><span data-stu-id="ed700-122">This feature isn't implemented as a language construct.</span></span> <span data-ttu-id="ed700-123">EDT を作成するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ed700-123">To create an EDT, follow these steps.</span></span>

1.  <span data-ttu-id="ed700-124">ソリューション エクスプローラーで、プロジェクトを右クリックして **追加** をポイントしてから **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ed700-124">In Solution Explorer, right-click on the project, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="ed700-125">**新しい項目の追加** ダイアログ ボックスで、**インストール済み** を選択してから左ウィンドウの **アーティファクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ed700-125">In the **Add New Item** dialog box, select **Installed** and then **Artifacts** in the left pane.</span></span>
3.  <span data-ttu-id="ed700-126">中央ウィンドウで、作成する EDT タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="ed700-126">In the middle pane, select the EDT type to create.</span></span>
4.  <span data-ttu-id="ed700-127">名前を入力し、次に **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ed700-127">Enter a name, and then click **Add**.</span></span>

## <a name="edt-example"></a><span data-ttu-id="ed700-128">EDT 例</span><span class="sxs-lookup"><span data-stu-id="ed700-128">EDT example</span></span>

```xpp
public void EdtMethod()
{
    // Example of declaring EDT variables where
    // a UserGroupID (integer) variable is declared and initialized to 1.
    UserGroupID groupID = 1;

    // An Amount (real) variable is declared.
    Amount currency;
}
```


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]