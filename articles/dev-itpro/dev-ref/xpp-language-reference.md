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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 72181
ms.assetid: fe5d3cdd-8b3d-4967-98a2-dadada18a421
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5fe5690b1f3a0f14b15fcc70a9ce5aaeb197208
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369739"
---
# <a name="x-language-reference"></a><span data-ttu-id="42983-103">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="42983-103">X++ language reference</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42983-104">X++ は、Microsoft Dynamics 365 for Finance and Operations がエンタープライズ リソース プランニング (ERP) プログラミングおよびデータベース アプリケーションで使用する、オブジェクト指向、アプリケーション対応、およびデータ対応のプログラミング言語です。</span><span class="sxs-lookup"><span data-stu-id="42983-104">X++ is an object-oriented, application-aware, and data-aware programming language that Microsoft Dynamics 365 for Finance and Operations uses in enterprise resource planning (ERP) programming and in database applications.</span></span> <span data-ttu-id="42983-105">次の表で強調表示された幅広いシステム プログラミング領域のシステム クラスを提供します。</span><span class="sxs-lookup"><span data-stu-id="42983-105">It provides system classes for a broad range of system programming areas, highlighted in the following table.</span></span>

| <span data-ttu-id="42983-106">**X++ 言語属性**</span><span class="sxs-lookup"><span data-stu-id="42983-106">**X++ language attributes**</span></span> | <span data-ttu-id="42983-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="42983-107">**Description**</span></span> |
|-----|-----|
| <span data-ttu-id="42983-108">**クラス**</span><span class="sxs-lookup"><span data-stu-id="42983-108">**Classes**</span></span>                 | <span data-ttu-id="42983-109">システム クラスに加えて、Dynamics 365 for Finance and Operations はさまざまなタイプの業務プロセスを管理するためのアプリケーション クラスも提供します。</span><span class="sxs-lookup"><span data-stu-id="42983-109">In addition to system classes, Dynamics 365 for Finance and Operations also provides application classes for managing many types of business processes.</span></span> <span data-ttu-id="42983-110">クラスのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="42983-110">Reflection on classes is supported.</span></span>            |
| <span data-ttu-id="42983-111">**テーブル**</span><span class="sxs-lookup"><span data-stu-id="42983-111">**Tables**</span></span>                  | <span data-ttu-id="42983-112">X++ のプログラマーは、Dynamics 365 for Finance and Operations リレーショナル テーブルにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="42983-112">X++ programmers can access the relational tables in Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="42983-113">X++ には標準 SQL の大部分のキーワードと一致するキーワードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="42983-113">X++ includes keywords that match most of the keywords in standard SQL.</span></span> <span data-ttu-id="42983-114">テーブルのリフレクションがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="42983-114">Reflection on tables is supported.</span></span> |
| <span data-ttu-id="42983-115">**ユーザー インターフェイス**</span><span class="sxs-lookup"><span data-stu-id="42983-115">**User interface**</span></span>          | <span data-ttu-id="42983-116">フォームやレポートなどのユーザー インターフェイス項目の操作。</span><span class="sxs-lookup"><span data-stu-id="42983-116">Manipulation of user interface items, such as forms and reports.</span></span>|
| <span data-ttu-id="42983-117">**推奨チェック**</span><span class="sxs-lookup"><span data-stu-id="42983-117">**Best practice checks**</span></span>    | <span data-ttu-id="42983-118">X++ コードはコンパイル中に構文エラーがチェックされます。</span><span class="sxs-lookup"><span data-stu-id="42983-118">X++ code is checked for syntax errors during compile time.</span></span> <span data-ttu-id="42983-119">コンパイル プロセスでは、ベスト プラクティス チェックも実行されます。</span><span class="sxs-lookup"><span data-stu-id="42983-119">The compile process also performs best practice checks.</span></span> <span data-ttu-id="42983-120">ベスト プラクティスの違反によりコンパイラのメッセージを生成できます。</span><span class="sxs-lookup"><span data-stu-id="42983-120">Violations of best practices can generate compiler messages.</span></span>|
| <span data-ttu-id="42983-121">**ガベージ コレクション**</span><span class="sxs-lookup"><span data-stu-id="42983-121">**Garbage collection**</span></span>      | <span data-ttu-id="42983-122">X++ ランタイム実行エンジンには、メモリ領域を再利用できるように、参照されなくなったオブジェクトを破棄する自動メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="42983-122">The X++ runtime execution engines have automatic mechanisms to discard objects that are no longer referenced, so that memory space can be reused.</span></span> |
| <span data-ttu-id="42983-123">**相互運用性**</span><span class="sxs-lookup"><span data-stu-id="42983-123">**Interoperability**</span></span>        | <span data-ttu-id="42983-124">Dynamics 365 for Finance and Operations は、X++ および C\# (または他の .NET Framework 言語) で書かれたクラス間の相互運用性をサポートします。</span><span class="sxs-lookup"><span data-stu-id="42983-124">Dynamics 365 for Finance and Operations supports interoperability between classes written in X++ and in C\# (or other .NET Framework languages).</span></span>                                                       |
| <span data-ttu-id="42983-125">**ファイルの操作**</span><span class="sxs-lookup"><span data-stu-id="42983-125">**File manipulation**</span></span>       | <span data-ttu-id="42983-126">ファイル入力および出力はサポートされており、XML 構築および解析を含みます。</span><span class="sxs-lookup"><span data-stu-id="42983-126">File input and output is supported, including XML building and parsing.</span></span> |
| <span data-ttu-id="42983-127">**取立**</span><span class="sxs-lookup"><span data-stu-id="42983-127">**Collections**</span></span>             | <span data-ttu-id="42983-128">動的配列はサポートされ、X++ にはいくつかのコレクション オブジェクトが含まれています。</span><span class="sxs-lookup"><span data-stu-id="42983-128">Dynamic arrays are supported and the X++ includes several collection objects.</span></span>|

<span data-ttu-id="42983-129">X++ 言語プログラミング ガイドは、以下のセクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="42983-129">The X++ language programming guide is divided into these sections:</span></span> 
+ [<span data-ttu-id="42983-130">X++ 属性クラス</span><span class="sxs-lookup"><span data-stu-id="42983-130">X++ attribute classes</span></span>](xpp-attribute-classes.md) 
+ [<span data-ttu-id="42983-131">X++ クラスおよびメソッド</span><span class="sxs-lookup"><span data-stu-id="42983-131">X++ classes and methods</span></span>](xpp-classes-methods.md) 
+ [<span data-ttu-id="42983-132">X++ データの選択と操作</span><span class="sxs-lookup"><span data-stu-id="42983-132">X++ data selection and manipulation</span></span>](xpp-data-query.md) 
+ [<span data-ttu-id="42983-133">X++ マクロ</span><span class="sxs-lookup"><span data-stu-id="42983-133">X++ macros</span></span>](xpp-macros.md) 
+ [<span data-ttu-id="42983-134">X++ 演算子</span><span class="sxs-lookup"><span data-stu-id="42983-134">X++ operators</span></span>](xpp-operators.md) 
+ [<span data-ttu-id="42983-135">X++ ステートメントおよびループ</span><span class="sxs-lookup"><span data-stu-id="42983-135">X++ statements and loops</span></span>](xpp-statements-loops.md)
+ [<span data-ttu-id="42983-136">X++ の変数とデータ型</span><span class="sxs-lookup"><span data-stu-id="42983-136">X++ variables and data types</span></span>](xpp-variables-data-types.md)

## <a name="additional-resources"></a><span data-ttu-id="42983-137">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="42983-137">Additional resources</span></span>
+ [<span data-ttu-id="42983-138">X++ 構文</span><span class="sxs-lookup"><span data-stu-id="42983-138">X++ Syntax</span></span>](xpp-syntax.md)
+ [<span data-ttu-id="42983-139">X++ と C# の比較</span><span class="sxs-lookup"><span data-stu-id="42983-139">X++ and C# Comparison</span></span>](xpp-cs-comparison.md)


