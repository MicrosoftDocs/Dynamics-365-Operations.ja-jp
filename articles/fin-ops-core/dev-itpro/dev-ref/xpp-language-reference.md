---
title: X++ 言語リファレンス
description: このトピックでは、X++ のプログラミング ガイドを提供します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 72181
ms.assetid: fe5d3cdd-8b3d-4967-98a2-dadada18a421
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eba91c78f1f2fb0b1d2a42d9b6fd575c54d8e119
ms.sourcegitcommit: c3bc5dd007d9f063631232497bd4cda9214e2e5b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2019
ms.locfileid: "2872431"
---
# <a name="x-language-reference"></a><span data-ttu-id="0a574-103">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="0a574-103">X++ language reference</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a574-104">X++ は、エンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。</span><span class="sxs-lookup"><span data-stu-id="0a574-104">X++ is an object-oriented, application-aware, and data-aware programming language used in enterprise resource planning (ERP) programming and in database applications.</span></span> <span data-ttu-id="0a574-105">次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="0a574-105">It provides system classes for a broad range of system programming areas, highlighted in the following table.</span></span>

| <span data-ttu-id="0a574-106">X++ 言語属性</span><span class="sxs-lookup"><span data-stu-id="0a574-106">X++ language attributes</span></span> | <span data-ttu-id="0a574-107">説明</span><span class="sxs-lookup"><span data-stu-id="0a574-107">Description</span></span> |
|-----|-----|
| <span data-ttu-id="0a574-108">**クラス**</span><span class="sxs-lookup"><span data-stu-id="0a574-108">**Classes**</span></span>                 | <span data-ttu-id="0a574-109">システム クラスに加えて、さまざまなタイプの業務プロセスを管理するためのアプリケーション クラスもあります。</span><span class="sxs-lookup"><span data-stu-id="0a574-109">In addition to system classes, there are also application classes for managing many types of business processes.</span></span> <span data-ttu-id="0a574-110">クラスのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0a574-110">Reflection on classes is supported.</span></span>            |
| <span data-ttu-id="0a574-111">**テーブル**</span><span class="sxs-lookup"><span data-stu-id="0a574-111">**Tables**</span></span>                  | <span data-ttu-id="0a574-112">X++ のプログラマーは、リレーショナル テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="0a574-112">X++ programmers can access the relational tables.</span></span> <span data-ttu-id="0a574-113">X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0a574-113">X++ includes keywords that match most of the keywords in standard SQL.</span></span> <span data-ttu-id="0a574-114">テーブルのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0a574-114">Reflection on tables is supported.</span></span> |
| <span data-ttu-id="0a574-115">**ユーザー インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="0a574-115">**User interface**</span></span>          | <span data-ttu-id="0a574-116">フォームやレポートなどのユーザー インターフェイス項目の操作。</span><span class="sxs-lookup"><span data-stu-id="0a574-116">Manipulation of user interface items, such as forms and reports.</span></span>|
| <span data-ttu-id="0a574-117">**推奨チェック**</span><span class="sxs-lookup"><span data-stu-id="0a574-117">**Best practice checks**</span></span>    | <span data-ttu-id="0a574-118">X++ コードはコンパイル中に構文エラーがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="0a574-118">X++ code is checked for syntax errors during compile time.</span></span> <span data-ttu-id="0a574-119">コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。</span><span class="sxs-lookup"><span data-stu-id="0a574-119">The compile process also performs best practice checks.</span></span> <span data-ttu-id="0a574-120">ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。</span><span class="sxs-lookup"><span data-stu-id="0a574-120">Violations of best practices can generate compiler messages.</span></span>|
| <span data-ttu-id="0a574-121">**ガベージ コレクション**</span><span class="sxs-lookup"><span data-stu-id="0a574-121">**Garbage collection**</span></span>      | <span data-ttu-id="0a574-122">X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="0a574-122">The X++ runtime execution engines have automatic mechanisms to discard objects that are no longer referenced, so that memory space can be reused.</span></span> |
| <span data-ttu-id="0a574-123">**相互運用性**</span><span class="sxs-lookup"><span data-stu-id="0a574-123">**Interoperability**</span></span>        | <span data-ttu-id="0a574-124">X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0a574-124">Interoperability between classes written in X++ and in C\# (or other .NET Framework languages) is supported.</span></span>                                                       |
| <span data-ttu-id="0a574-125">**ファイルの操作**</span><span class="sxs-lookup"><span data-stu-id="0a574-125">**File manipulation**</span></span>       | <span data-ttu-id="0a574-126">ファイル入力および出力はサポートされており、XML 構築および解析を含みます。</span><span class="sxs-lookup"><span data-stu-id="0a574-126">File input and output is supported, including XML building and parsing.</span></span> |
| <span data-ttu-id="0a574-127">**取立**</span><span class="sxs-lookup"><span data-stu-id="0a574-127">**Collections**</span></span>             | <span data-ttu-id="0a574-128">動的配列はサポートされ、X++ にはいくつかのコレクション オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0a574-128">Dynamic arrays are supported and the X++ includes several collection objects.</span></span>|

<span data-ttu-id="0a574-129">X++ 言語プログラミング ガイドは、以下のセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="0a574-129">The X++ language programming guide is divided into these sections:</span></span> 
+ [<span data-ttu-id="0a574-130">X++ 属性クラス</span><span class="sxs-lookup"><span data-stu-id="0a574-130">X++ attribute classes</span></span>](xpp-attribute-classes.md) 
+ [<span data-ttu-id="0a574-131">X++ クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="0a574-131">X++ classes and methods</span></span>](xpp-classes-methods.md) 
+ [<span data-ttu-id="0a574-132">X++ データの選択と操作</span><span class="sxs-lookup"><span data-stu-id="0a574-132">X++ data selection and manipulation</span></span>](xpp-data-query.md) 
+ [<span data-ttu-id="0a574-133">X++ マクロ</span><span class="sxs-lookup"><span data-stu-id="0a574-133">X++ macros</span></span>](xpp-macros.md) 
+ [<span data-ttu-id="0a574-134">X++ 演算子</span><span class="sxs-lookup"><span data-stu-id="0a574-134">X++ operators</span></span>](xpp-operators.md) 
+ [<span data-ttu-id="0a574-135">X++ ステートメントおよびループ</span><span class="sxs-lookup"><span data-stu-id="0a574-135">X++ statements and loops</span></span>](xpp-statements-loops.md)
+ [<span data-ttu-id="0a574-136">X++ の変数とデータ型</span><span class="sxs-lookup"><span data-stu-id="0a574-136">X++ variables and data types</span></span>](xpp-variables-data-types.md)

## <a name="additional-resources"></a><span data-ttu-id="0a574-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="0a574-137">Additional resources</span></span>
+ [<span data-ttu-id="0a574-138">X++ 構文</span><span class="sxs-lookup"><span data-stu-id="0a574-138">X++ Syntax</span></span>](xpp-syntax.md)
+ [<span data-ttu-id="0a574-139">X++ と C# の比較</span><span class="sxs-lookup"><span data-stu-id="0a574-139">X++ and C# Comparison</span></span>](xpp-cs-comparison.md)


