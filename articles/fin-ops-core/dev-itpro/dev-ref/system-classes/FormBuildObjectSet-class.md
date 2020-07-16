---
title: FormBuildObjectSet クラス
description: このトピックでは、FormBuildObjectSet クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eff207541e2fb7b07589f3c6c268a7efbf9fb47
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502960"
---
# <a name="class-formbuildobjectset"></a><span data-ttu-id="44f98-103">クラス FormBuildObjectSet</span><span class="sxs-lookup"><span data-stu-id="44f98-103">Class FormBuildObjectSet</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildObjectSet extends Object
```

<span data-ttu-id="44f98-104">FormBuildObjectSet クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="44f98-104">The FormBuildObjectSet class lets you create, read, update, and delete X++ code and metadata.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f98-105">備考</span><span class="sxs-lookup"><span data-stu-id="44f98-105">Remarks</span></span>

<span data-ttu-id="44f98-106">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="44f98-106">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

## <a name="examples"></a><span data-ttu-id="44f98-107">例</span><span class="sxs-lookup"><span data-stu-id="44f98-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="44f98-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="44f98-108">Methods</span></span>

| <span data-ttu-id="44f98-109">方法</span><span class="sxs-lookup"><span data-stu-id="44f98-109">Method</span></span>                         | <span data-ttu-id="44f98-110">説明</span><span class="sxs-lookup"><span data-stu-id="44f98-110">Description</span></span>                                                                                                                             |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f98-111">public int id()</span><span class="sxs-lookup"><span data-stu-id="44f98-111">public int id()</span></span>                |                                                                                                                                         |
| <span data-ttu-id="44f98-112">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="44f98-112">public str name(\[str value\])</span></span> | <span data-ttu-id="44f98-113">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="44f98-113">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span> |
| <span data-ttu-id="44f98-114">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="44f98-114">public void finalize()</span></span>         |                                                                                                                                         |

## <a name="method-id"></a><span data-ttu-id="44f98-115">メソッド id</span><span class="sxs-lookup"><span data-stu-id="44f98-115">Method id</span></span>

```xpp
public int id()
```

### <a name="return-value---id"></a><span data-ttu-id="44f98-116">戻り値 - id</span><span class="sxs-lookup"><span data-stu-id="44f98-116">Return Value - id</span></span>

## <a name="method-name"></a><span data-ttu-id="44f98-117">メソッド名</span><span class="sxs-lookup"><span data-stu-id="44f98-117">Method name</span></span>

<span data-ttu-id="44f98-118">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="44f98-118">Gets or sets the name that is used in code to identify a form, report, table, query, or other application object.</span></span>

```xpp
public str name([str value])
```

### <a name="parameters---name"></a><span data-ttu-id="44f98-119">パラメーター - 名前</span><span class="sxs-lookup"><span data-stu-id="44f98-119">Parameters - name</span></span>

<span data-ttu-id="44f98-120">値</span><span class="sxs-lookup"><span data-stu-id="44f98-120">value</span></span>  
<span data-ttu-id="44f98-121">コントロールに割り当てる名前。</span><span class="sxs-lookup"><span data-stu-id="44f98-121">The name to assign to the control.</span></span>

### <a name="return-value---name"></a><span data-ttu-id="44f98-122">戻り値 - name</span><span class="sxs-lookup"><span data-stu-id="44f98-122">Return Value - name</span></span>

<span data-ttu-id="44f98-123">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="44f98-123">The name that is used in code to identify an application object.</span></span>

### <a name="remarks---name"></a><span data-ttu-id="44f98-124">備考 - 名前</span><span class="sxs-lookup"><span data-stu-id="44f98-124">Remarks - name</span></span>

<span data-ttu-id="44f98-125">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="44f98-125">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="44f98-126">文字で始める必要があります。</span><span class="sxs-lookup"><span data-stu-id="44f98-126">It must start with a letter.</span></span>
-   <span data-ttu-id="44f98-127">250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="44f98-127">It cannot exceed 250 characters.</span></span>
-   <span data-ttu-id="44f98-128">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="44f98-128">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="44f98-129">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="44f98-129">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="44f98-130">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="44f98-130">Tables cannot have the same name as other public objects, such as extended data types, base enums, or classes.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="44f98-131">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="44f98-131">Method finalize</span></span>

```xpp
public void finalize()
```

