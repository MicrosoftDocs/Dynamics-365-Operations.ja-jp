---
title: API、クラス、テーブルのリファレンス
description: このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。
author: RobinARH
ms.date: 07/23/2019
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 63853
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 149e524c550f810d514b548e9cb0ea65ba28d81f
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923255"
---
# <a name="api-class-and-table-resources"></a><span data-ttu-id="2ac67-103">API、クラス、テーブルのリファレンス</span><span class="sxs-lookup"><span data-stu-id="2ac67-103">API, class, and table resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ac67-104">このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="2ac67-104">This topic describes where to find API documentation in Visual Studio and on the Microsoft docs site.</span></span>

## <a name="application-classes-and-tables"></a><span data-ttu-id="2ac67-105">アプリケーション クラスおよびテーブル</span><span class="sxs-lookup"><span data-stu-id="2ac67-105">Application classes and tables</span></span>

### <a name="application-class-and-table-documentation-is-in-visual-studio"></a><span data-ttu-id="2ac67-106">アプリケーション クラスおよびテーブル ドキュメントは Visual Studio にあります</span><span class="sxs-lookup"><span data-stu-id="2ac67-106">Application class and table documentation is in Visual Studio</span></span>

<span data-ttu-id="2ac67-107">Microsoft Visual Studio のアプリケーション クラスについては、ドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ac67-107">You can find documentation for the Application classes in Microsoft Visual Studio.</span></span> <span data-ttu-id="2ac67-108">アプリケーション エクスプローラーでクラス名を検索し、そのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="2ac67-108">Search for the class name in Application Explorer and then display the code.</span></span> <span data-ttu-id="2ac67-109">クラスに関する追加のメタデータは **プロパティ** ウィンドウ内にあります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-109">You can find additional metadata about the class in the **Properties** window.</span></span> <span data-ttu-id="2ac67-110">[技術参照レポート](/dynamics/s-e/global/axtechrefrep_61) 内のすべてのテーブルの一覧をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="2ac67-110">You can download a list of all the tables in the [Technical Reference Reports](/dynamics/s-e/global/axtechrefrep_61).</span></span> <span data-ttu-id="2ac67-111">詳細については、[標準データ エンティティに関する情報の検索](../data-entities/data-entities-report.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2ac67-111">For more information, see [Find information about standard data entities](../data-entities/data-entities-report.md).</span></span>

### <a name="programming-with-application-tables-and-classes"></a><span data-ttu-id="2ac67-112">アプリケーション テーブルおよびクラスを使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="2ac67-112">Programming with application tables and classes</span></span>

<span data-ttu-id="2ac67-113">アプリケーション テーブルはアプリケーション クラスと類似していますが、クラスとの違いは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2ac67-113">Application tables are similar to application classes, but with the following differences from classes:</span></span>

- <span data-ttu-id="2ac67-114">テーブルは維持されます。</span><span class="sxs-lookup"><span data-stu-id="2ac67-114">Tables are persistent.</span></span>
- <span data-ttu-id="2ac67-115">テーブル フィールドは、常にパブリックになります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-115">Table fields are always public.</span></span>
- <span data-ttu-id="2ac67-116">テーブルは、ほとんどの場合、実際のオブジェクトに対応します。</span><span class="sxs-lookup"><span data-stu-id="2ac67-116">A table almost always corresponds to a real object.</span></span>
- <span data-ttu-id="2ac67-117">後で他のテーブルで拡張する場合は、テーブルの定義を消去する必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-117">The definition of a table must sometimes be erased if you later want another table to extend it.</span></span>

### <a name="design-pattern-of-private-new-in-application-classes"></a><span data-ttu-id="2ac67-118">アプリケーション クラスの新規プライベート設計パターン</span><span class="sxs-lookup"><span data-stu-id="2ac67-118">Design pattern of private new in application classes</span></span>

<span data-ttu-id="2ac67-119">すべてのアプリケーション クラスはアプリケーション エクスプ ローラー &gt; クラスの下にあります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-119">All application classes are under Application Explorer &gt; Classes.</span></span> <span data-ttu-id="2ac67-120">クラスにアプリケーション エクスプローラーの **新規** ノードがなくても、すべてのアプリケーション クラスに `new` という名前のコンストラクター メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-120">Every application class has the constructor method named `new`, even if the class has no **new** node in the Application Explorer.</span></span> <span data-ttu-id="2ac67-121">クラスに明示的な **新規** ノードがない場合、暗黙的な **新規** メソッドがパブリックになります。</span><span class="sxs-lookup"><span data-stu-id="2ac67-121">If the class has no explicit **new** node, the implicit **new** method is public.</span></span> <span data-ttu-id="2ac67-122">アプリケーション クラスで場合によって使用される設計パターンは、明示的な **新規** コンストラクター メソッドを **プライベート** として宣言します。</span><span class="sxs-lookup"><span data-stu-id="2ac67-122">A design pattern that is sometimes used in the application classes is to declare the explicit **new** constructor method as **private**.</span></span> <span data-ttu-id="2ac67-123">その後、**パブリック静的** メソッドを追加して **新規** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2ac67-123">Then a **public static** method is added to call the **new** method.</span></span> <span data-ttu-id="2ac67-124">静的メソッドは、必要に応じてさまざまな条件に基づき、**新規** メソッドの呼び出しを制限または制御できます。</span><span class="sxs-lookup"><span data-stu-id="2ac67-124">The static method can restrict or control the call the **new** method based on various conditions, if necessary.</span></span>

## <a name="system-classes-and-tables"></a><span data-ttu-id="2ac67-125">システム クラスおよびテーブル</span><span class="sxs-lookup"><span data-stu-id="2ac67-125">System classes and tables</span></span>

### <a name="system-api-class-and-table-documentation-is-on-the-microsoft-docs-site"></a><span data-ttu-id="2ac67-126">システム API、クラス、およびテーブル ドキュメントが Microsoft ドキュメント サイトにあります</span><span class="sxs-lookup"><span data-stu-id="2ac67-126">System API, class, and table documentation is on the Microsoft docs site</span></span>

<span data-ttu-id="2ac67-127">Microsoft docs サイトで使用可能なアプリケーション エクスプローラーの **システム ドキュメント** の下に、表示されているクラスおよび機能のドキュメント。</span><span class="sxs-lookup"><span data-stu-id="2ac67-127">Documentation for the classes and functions that are listed under **System Documentation** in Application Explorer is available on the Microsoft docs site.</span></span>

## <a name="x-compile-time-functions"></a><span data-ttu-id="2ac67-128">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-128">X++ compile-time functions</span></span>

[<span data-ttu-id="2ac67-129">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-129">X++ compile-time functions</span></span>](xpp-compile-time-functions.md)

## <a name="x-run-time-functions"></a><span data-ttu-id="2ac67-130">X++ ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-130">X++ run-time functions</span></span>

<span data-ttu-id="2ac67-131">[X++ ランタイム関数](xpp-string-run-time-functions.md):</span><span class="sxs-lookup"><span data-stu-id="2ac67-131">[X++ run-time functions](xpp-string-run-time-functions.md):</span></span>

- [<span data-ttu-id="2ac67-132">X++ コンテナー ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-132">X++ container run-time functions</span></span>](xpp-container-run-time-functions.md)
- [<span data-ttu-id="2ac67-133">X++ ビジネス ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-133">X++ business run-time functions</span></span>](xpp-business-run-time-functions.md)
- [<span data-ttu-id="2ac67-134">X++ 変換ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-134">X++ conversion run-time functions</span></span>](xpp-conversion-run-time-functions.md)
- [<span data-ttu-id="2ac67-135">X++ 日付ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-135">X++ date run-time functions</span></span>](xpp-date-run-time-functions.md)
- [<span data-ttu-id="2ac67-136">X++ 数学ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-136">X++ math run-time functions</span></span>](xpp-math-run-time-functions.md)
- [<span data-ttu-id="2ac67-137">X++ リフレクション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-137">X++ reflection run-time functions</span></span>](xpp-reflection-run-time-functions.md)
- [<span data-ttu-id="2ac67-138">X++ セッション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-138">X++ session run-time functions</span></span>](xpp-session-run-time-functions.md)
- [<span data-ttu-id="2ac67-139">X++ 文字列ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="2ac67-139">X++ string run-time functions</span></span>](xpp-string-run-time-functions.md)

## <a name="system-tables"></a><span data-ttu-id="2ac67-140">システム テーブル</span><span class="sxs-lookup"><span data-stu-id="2ac67-140">System tables</span></span>

[<span data-ttu-id="2ac67-141">システム テーブル</span><span class="sxs-lookup"><span data-stu-id="2ac67-141">System tables</span></span>](system-tables.md)

## <a name="system-classes"></a><span data-ttu-id="2ac67-142">システム クラス</span><span class="sxs-lookup"><span data-stu-id="2ac67-142">System classes</span></span>

<span data-ttu-id="2ac67-143">システム クラスのリファレンス ドキュメントは .NET API ブラウザーに含まれています。</span><span class="sxs-lookup"><span data-stu-id="2ac67-143">The reference documentation for the system classes is in the .NET API browser.</span></span>

[<span data-ttu-id="2ac67-144">Microsoft.Dynamics.Ax.Xpp 名前空間</span><span class="sxs-lookup"><span data-stu-id="2ac67-144">Microsoft.Dynamics.Ax.Xpp namespace</span></span>](/dotnet/api/microsoft.dynamics.ax.xpp)

[<span data-ttu-id="2ac67-145">Dynamics.AX.Application 名前空間</span><span class="sxs-lookup"><span data-stu-id="2ac67-145">Dynamics.AX.Application namespace</span></span>](/dotnet/api/dynamics.ax.application)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]