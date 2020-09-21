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
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ac3bf768e3ec298114aef4f5716c60f34fc11cc
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/03/2020
ms.locfileid: "3764987"
---
# <a name="x-language-reference"></a><span data-ttu-id="b3280-103">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="b3280-103">X++ language reference</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3280-104">X++ は、エンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。</span><span class="sxs-lookup"><span data-stu-id="b3280-104">X++ is an object-oriented, application-aware, and data-aware programming language used in enterprise resource planning (ERP) programming and in database applications.</span></span> <span data-ttu-id="b3280-105">次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3280-105">It provides system classes for a broad range of system programming areas, highlighted in the following table.</span></span>

| <span data-ttu-id="b3280-106">X++ 言語機能</span><span class="sxs-lookup"><span data-stu-id="b3280-106">X++ language feature</span></span> | <span data-ttu-id="b3280-107">説明</span><span class="sxs-lookup"><span data-stu-id="b3280-107">Description</span></span> |
|-----|-----|
| <span data-ttu-id="b3280-108">クラス</span><span class="sxs-lookup"><span data-stu-id="b3280-108">Classes</span></span>              | <span data-ttu-id="b3280-109">システム クラスに加えて、さまざまなタイプの業務プロセスを管理するためのアプリケーション クラスもあります。</span><span class="sxs-lookup"><span data-stu-id="b3280-109">In addition to system classes, there are also application classes for managing many types of business processes.</span></span> <span data-ttu-id="b3280-110">クラスのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b3280-110">Reflection on classes is supported.</span></span> |
| <span data-ttu-id="b3280-111">テーブル</span><span class="sxs-lookup"><span data-stu-id="b3280-111">Tables</span></span>               | <span data-ttu-id="b3280-112">X++ のプログラマーは、リレーショナル テーブルにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b3280-112">X++ programmers can access the relational tables.</span></span> <span data-ttu-id="b3280-113">X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b3280-113">X++ includes keywords that match most of the keywords in standard SQL.</span></span> <span data-ttu-id="b3280-114">テーブルのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b3280-114">Reflection on tables is supported.</span></span> |
| <span data-ttu-id="b3280-115">ユーザー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b3280-115">User interface</span></span>       | <span data-ttu-id="b3280-116">フォームやレポートなどのユーザー インターフェイス項目の操作。</span><span class="sxs-lookup"><span data-stu-id="b3280-116">Manipulation of user interface items, such as forms and reports.</span></span>|
| <span data-ttu-id="b3280-117">推奨チェック</span><span class="sxs-lookup"><span data-stu-id="b3280-117">Best practice checks</span></span> | <span data-ttu-id="b3280-118">X++ コードはコンパイル中に構文エラーがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="b3280-118">X++ code is checked for syntax errors during compile time.</span></span> <span data-ttu-id="b3280-119">コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。</span><span class="sxs-lookup"><span data-stu-id="b3280-119">The compile process also performs best practice checks.</span></span> <span data-ttu-id="b3280-120">ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。</span><span class="sxs-lookup"><span data-stu-id="b3280-120">Violations of best practices can generate compiler messages.</span></span>|
| <span data-ttu-id="b3280-121">ガベージ コレクション</span><span class="sxs-lookup"><span data-stu-id="b3280-121">Garbage collection</span></span>   | <span data-ttu-id="b3280-122">X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="b3280-122">The X++ runtime execution engines have automatic mechanisms to discard objects that are no longer referenced, so that memory space can be reused.</span></span> |
| <span data-ttu-id="b3280-123">相互運用性</span><span class="sxs-lookup"><span data-stu-id="b3280-123">Interoperability</span></span>     | <span data-ttu-id="b3280-124">X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="b3280-124">Interoperability between classes written in X++ and in C\# (or other .NET Framework languages) is supported.</span></span>                                      |
| <span data-ttu-id="b3280-125">ファイルの操作</span><span class="sxs-lookup"><span data-stu-id="b3280-125">File manipulation</span></span>    | <span data-ttu-id="b3280-126">ファイル入力および出力はサポートされており、XML 構築および解析を含みます。</span><span class="sxs-lookup"><span data-stu-id="b3280-126">File input and output is supported, including XML building and parsing.</span></span> |
| <span data-ttu-id="b3280-127">取立</span><span class="sxs-lookup"><span data-stu-id="b3280-127">Collections</span></span>          | <span data-ttu-id="b3280-128">動的配列はサポートされ、X++ にはいくつかのコレクション オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3280-128">Dynamic arrays are supported and the X++ includes several collection objects.</span></span>|

<span data-ttu-id="b3280-129">X++ 言語プログラミング ガイドは、以下のセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="b3280-129">The X++ language programming guide is divided into these sections:</span></span> 

+ [<span data-ttu-id="b3280-130">変数とデータ型</span><span class="sxs-lookup"><span data-stu-id="b3280-130">Variables and data types</span></span>](xpp-variables-data-types.md)
+ [<span data-ttu-id="b3280-131">ステートメント、ループ、および例外処理</span><span class="sxs-lookup"><span data-stu-id="b3280-131">Statements, loops, and exception handling</span></span>](xpp-conditional.md)
+ [<span data-ttu-id="b3280-132">演算子</span><span class="sxs-lookup"><span data-stu-id="b3280-132">Operators</span></span>](xpp-operators.md) 
+ [<span data-ttu-id="b3280-133">クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="b3280-133">Classes and methods</span></span>](xpp-classes-methods.md) 
+ [<span data-ttu-id="b3280-134">データの選択と操作</span><span class="sxs-lookup"><span data-stu-id="b3280-134">Data selection and manipulation</span></span>](xpp-data/xpp-data-home-page.md)
+ [<span data-ttu-id="b3280-135">マクロ</span><span class="sxs-lookup"><span data-stu-id="b3280-135">Macros</span></span>](xpp-macros.md) 
+ [<span data-ttu-id="b3280-136">属性クラス</span><span class="sxs-lookup"><span data-stu-id="b3280-136">Attribute classes</span></span>](xpp-attribute-classes.md) 

## <a name="additional-resources"></a><span data-ttu-id="b3280-137">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b3280-137">Additional resources</span></span>
+ [<span data-ttu-id="b3280-138">X++ 構文</span><span class="sxs-lookup"><span data-stu-id="b3280-138">X++ Syntax</span></span>](xpp-syntax.md)
+ [<span data-ttu-id="b3280-139">X++ と C# の比較</span><span class="sxs-lookup"><span data-stu-id="b3280-139">X++ and C# Comparison</span></span>](xpp-cs-comparison.md)


