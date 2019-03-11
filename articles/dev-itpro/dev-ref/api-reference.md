---
title: API、クラス、およびテーブルの参照
description: このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。
author: RobinARH
manager: AnnBe
ms.date: 12/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 63853
ms.assetid: 46e5e47b-2c80-44fd-a7a3-e41884da2f55
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec3d156aefd1c725381858cc9667273983238f1e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369929"
---
# <a name="api-class-and-table-reference"></a><span data-ttu-id="cf2f3-103">API、クラス、およびテーブルの参照</span><span class="sxs-lookup"><span data-stu-id="cf2f3-103">API, class, and table reference</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf2f3-104">このトピックでは、Visual Studio および Microsoft のドキュメント サイトで API ドキュメントを見つける場所について説明します。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-104">This topic describes where to find API documentation in Visual Studio and on the Microsoft docs site.</span></span>

## <a name="application-classes-and-tables"></a><span data-ttu-id="cf2f3-105">アプリケーション クラスおよびテーブル</span><span class="sxs-lookup"><span data-stu-id="cf2f3-105">Application classes and tables</span></span>

### <a name="application-class-and-table-documentation-is-in-visual-studio"></a><span data-ttu-id="cf2f3-106">アプリケーション クラスおよびテーブル ドキュメントは Visual Studio にあります</span><span class="sxs-lookup"><span data-stu-id="cf2f3-106">Application class and table documentation is in Visual Studio</span></span>

<span data-ttu-id="cf2f3-107">Microsoft Visual Studio 内のアプリケーション クラス用ドキュメントは、アプリケーション エクスプローラーのアプリケーション プログラミング インターフェイス (API) を検索してからコードを表示することにより見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-107">You can find documentation for the Application classes in Microsoft Visual Studio by searching for the application programming interface (API) in Application Explorer and then displaying the code.</span></span> <span data-ttu-id="cf2f3-108">API に関する追加のメタデータは **プロパティ** ウィンドウ内で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-108">You can find additional metadata about the API in the **Properties** window.</span></span> <span data-ttu-id="cf2f3-109">また、[技術参照レポート](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep) 内のすべてのテーブルの一覧をダウンロードすることができます。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-109">You can also download a list of all the tables in the [Technical Reference Reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span>

### <a name="programming-with-application-tables-and-classes"></a><span data-ttu-id="cf2f3-110">アプリケーション テーブルおよびクラスを使用したプログラミング</span><span class="sxs-lookup"><span data-stu-id="cf2f3-110">Programming with application tables and classes</span></span>

<span data-ttu-id="cf2f3-111">アプリケーション テーブルはアプリケーション クラスと類似していますが、クラスとの違いは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-111">Application tables are being similar to application classes, but with the following differences from classes:</span></span>

-   <span data-ttu-id="cf2f3-112">テーブルは維持されます。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-112">Tables are persistent.</span></span>
-   <span data-ttu-id="cf2f3-113">テーブル フィールドは、常にパブリックになります。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-113">Table fields are always public.</span></span>
-   <span data-ttu-id="cf2f3-114">テーブルは、ほとんどの場合、実際のオブジェクトに対応します。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-114">A table almost always corresponds to a real object.</span></span>
-   <span data-ttu-id="cf2f3-115">後で他のテーブルで拡張する場合は、テーブルの定義を消去する必要になる場合があります。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-115">The definition of a table must sometimes be erased if you later want another table to extend it.</span></span>

### <a name="design-pattern-of-private-new-in-application-classes"></a><span data-ttu-id="cf2f3-116">アプリケーション クラスの新規プライベート設計パターン</span><span class="sxs-lookup"><span data-stu-id="cf2f3-116">Design pattern of private new in application classes</span></span>

<span data-ttu-id="cf2f3-117">すべてのアプリケーション クラスはアプリケーション エクスプ ローラー &gt; クラスの下にあります。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-117">All application classes are under Application Explorer &gt; Classes.</span></span> <span data-ttu-id="cf2f3-118">クラスに AOT の新しいノードがなくても、すべてのアプリケーション クラスに `new` という名のコンストラクター メソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-118">Every application class has the constructor method named `new`, even if the class has no new node in the AOT.</span></span> <span data-ttu-id="cf2f3-119">クラスに明示的な新しいノードがない場合、`new` メソッドがパブリックになります。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-119">If the class has no explicit new node, the implicit `new` method is public.</span></span> <span data-ttu-id="cf2f3-120">アプリケーション クラスで場合によって使用される設計パターンは、明示的な `new` コンストラクター メソッドを `private` として宣言します。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-120">A design pattern that is sometimes used in the application classes is to declare the explicit `new` constructor method as `private`.</span></span> <span data-ttu-id="cf2f3-121">その後、`public static` メソッドを追加して `new` メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-121">Then a `public static` method is added to call the `new` method.</span></span> <span data-ttu-id="cf2f3-122">必要に応じて、静的メソッドは、さまざまな条件に基づき `new` メソッドの呼び出しを制限または制御できます。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-122">The static method can restrict or control the call the `new` method based on various conditions, if necessary.</span></span>

## <a name="system-classes-and-tables"></a><span data-ttu-id="cf2f3-123">システム クラスおよびテーブル</span><span class="sxs-lookup"><span data-stu-id="cf2f3-123">System classes and tables</span></span>
### <a name="system-api-class-and-table-documentation-is-on-the-microsoft-docs-site"></a><span data-ttu-id="cf2f3-124">システム API、クラス、およびテーブル ドキュメントが Microsoft ドキュメント サイトにあります</span><span class="sxs-lookup"><span data-stu-id="cf2f3-124">System API, class, and table documentation is on the Microsoft docs site</span></span>

<span data-ttu-id="cf2f3-125">Microsoft docs サイトで使用可能なアプリケーション エクスプローラーの**システム ドキュメント**の下に、表示されているクラスおよび機能のドキュメント。</span><span class="sxs-lookup"><span data-stu-id="cf2f3-125">Documentation for the classes and functions that are listed under **System Documentation** in Application Explorer is available on the Microsoft docs site.</span></span>

## <a name="x-compile-time-functions"></a><span data-ttu-id="cf2f3-126">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-126">X++ compile-time functions</span></span>
[<span data-ttu-id="cf2f3-127">X++ コンパイル時関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-127">X++ compile-time functions</span></span>](xpp-compile-time-functions.md)

## <a name="x-run-time-functions"></a><span data-ttu-id="cf2f3-128">X++ ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-128">X++ run-time functions</span></span>
<span data-ttu-id="cf2f3-129">[X++ ランタイム関数](xpp-string-run-time-functions.md):</span><span class="sxs-lookup"><span data-stu-id="cf2f3-129">[X++ run-time functions](xpp-string-run-time-functions.md):</span></span>

-   [<span data-ttu-id="cf2f3-130">X++ コンテナー ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-130">X++ container run-time functions</span></span>](xpp-container-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-131">X++ ビジネス ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-131">X++ business run-time functions</span></span>](xpp-business-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-132">X++ 変換ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-132">X++ conversion run-time functions</span></span>](xpp-conversion-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-133">X++ 日付ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-133">X++ date run-time functions</span></span>](xpp-date-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-134">X++ 数学ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-134">X++ math run-time functions</span></span>](xpp-math-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-135">X++ リフレクション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-135">X++ reflection run-time functions</span></span>](xpp-reflection-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-136">X++ セッション ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-136">X++ session run-time functions</span></span>](xpp-session-run-time-functions.md)
-   [<span data-ttu-id="cf2f3-137">X++ 文字列ランタイム関数</span><span class="sxs-lookup"><span data-stu-id="cf2f3-137">X++ string run-time functions</span></span>](xpp-string-run-time-functions.md)

## <a name="system-tables"></a><span data-ttu-id="cf2f3-138">システム テーブル</span><span class="sxs-lookup"><span data-stu-id="cf2f3-138">System tables</span></span>
[<span data-ttu-id="cf2f3-139">システム テーブル</span><span class="sxs-lookup"><span data-stu-id="cf2f3-139">System tables</span></span>](system-tables.md)

## <a name="system-classes"></a><span data-ttu-id="cf2f3-140">システム クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-140">System classes</span></span>
-   [<span data-ttu-id="cf2f3-141">A クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-141">A classes</span></span>](a-classes.md)
-   [<span data-ttu-id="cf2f3-142">B クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-142">B classes</span></span>](b-classes.md)
-   [<span data-ttu-id="cf2f3-143">C クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-143">C classes</span></span>](c-classes.md)
-   [<span data-ttu-id="cf2f3-144">D クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-144">D classes</span></span>](d-classes.md)
-   [<span data-ttu-id="cf2f3-145">E クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-145">E classes</span></span>](e-classes.md)
-   [<span data-ttu-id="cf2f3-146">F クラス: FormBuildAnimateControl への FieldBinding</span><span class="sxs-lookup"><span data-stu-id="cf2f3-146">F classes: FieldBinding to FormBuildAnimateControl</span></span>](fieldbinding-classes.md)
-   [<span data-ttu-id="cf2f3-147">F クラス: FormBuildFastTabSummarySeparator への FormBuildButtonControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-147">F classes: FormBuildButtonControl to FormBuildFastTabSummarySeparator</span></span>](FormBuildButtonControl-classes.md)
-   [<span data-ttu-id="cf2f3-148">F クラス: FormBuildRealControl への FormBuildFilterPaneControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-148">F classes: FormBuildFilterPaneControl to FormBuildRealControl</span></span>](FormBuildFilterPaneControl-classes.md)
-   [<span data-ttu-id="cf2f3-149">F クラス: FormButtonSeparatorControl への FormBuildReferenceControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-149">F classes: FormBuildReferenceControl to FormButtonSeparatorControl</span></span>](FormBuildReferenceControl-classes.md)
-   [<span data-ttu-id="cf2f3-150">F クラス: FormControlEventArgs への FormChangeTracker</span><span class="sxs-lookup"><span data-stu-id="cf2f3-150">F classes: FormChangeTracker to FormControlEventArgs</span></span>](FormChangeTracker-classes.md)
-   [<span data-ttu-id="cf2f3-151">F クラス: FormFastTabHeaderControl への FormDataObject</span><span class="sxs-lookup"><span data-stu-id="cf2f3-151">F classes: FormDataObject to FormFastTabHeaderControl</span></span>](FormDataObject-classes.md)
-   [<span data-ttu-id="cf2f3-152">F クラス: FormGridControl への FormFastTabSummarySeparator</span><span class="sxs-lookup"><span data-stu-id="cf2f3-152">F classes: FormFastTabSummarySeparator to FormGridControl</span></span>](FormFastTabSummarySeparator-classes.md)
-   [<span data-ttu-id="cf2f3-153">F クラス: FormIntControl への FormGroupControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-153">F classes: FormGroupControl to FormIntControl</span></span>](FormGroupControl-classes.md)
-   [<span data-ttu-id="cf2f3-154">F クラス: FormNotifyEventArgs への FormListBoxControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-154">F classes: FormListBoxControl to FormNotifyEventArgs</span></span>](FormListBoxControl-classes.md)
-   [<span data-ttu-id="cf2f3-155">F クラス: FormRealControl への FormObject</span><span class="sxs-lookup"><span data-stu-id="cf2f3-155">F classes: FormObject to FormRealControl</span></span>](FormObject-classes.md)
-   [<span data-ttu-id="cf2f3-156">F クラス: FormStringControl への FormReferenceControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-156">F classes: FormReferenceControl to FormStringControl</span></span>](FormReferenceControl-classes.md)
-   [<span data-ttu-id="cf2f3-157">F クラス: FormWindowControl への FormTabControl</span><span class="sxs-lookup"><span data-stu-id="cf2f3-157">F classes: FormTabControl to FormWindowControl</span></span>](FormTabControl-classes.md)
-   [<span data-ttu-id="cf2f3-158">G クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-158">G classes</span></span>](g-classes.md)
-   [<span data-ttu-id="cf2f3-159">H クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-159">H classes</span></span>](h-classes.md)
-   [<span data-ttu-id="cf2f3-160">I クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-160">I classes</span></span>](i-classes.md)
-   [<span data-ttu-id="cf2f3-161">J クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-161">J classes</span></span>](j-classes.md)
-   [<span data-ttu-id="cf2f3-162">K クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-162">K classes</span></span>](k-classes.md)
-   [<span data-ttu-id="cf2f3-163">L クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-163">L classes</span></span>](l-classes.md)
-   [<span data-ttu-id="cf2f3-164">M クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-164">M classes</span></span>](m-classes.md)
-   [<span data-ttu-id="cf2f3-165">N クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-165">N classes</span></span>](n-classes.md)
-   [<span data-ttu-id="cf2f3-166">O クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-166">O classes</span></span>](o-classes.md)
-   [<span data-ttu-id="cf2f3-167">P クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-167">P classes</span></span>](p-classes.md)
-   [<span data-ttu-id="cf2f3-168">Q クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-168">Q classes</span></span>](q-classes.md)
-   [<span data-ttu-id="cf2f3-169">R クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-169">R classes</span></span>](r-classes.md)
-   [<span data-ttu-id="cf2f3-170">S クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-170">S classes</span></span>](s-classes.md)
-   [<span data-ttu-id="cf2f3-171">T クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-171">T classes</span></span>](t-classes.md)
-   [<span data-ttu-id="cf2f3-172">U クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-172">U classes</span></span>](u-classes.md)
-   [<span data-ttu-id="cf2f3-173">V クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-173">V classes</span></span>](v-classes.md)
-   [<span data-ttu-id="cf2f3-174">W クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-174">W classes</span></span>](w-classes.md)
-   [<span data-ttu-id="cf2f3-175">X クラス</span><span class="sxs-lookup"><span data-stu-id="cf2f3-175">X classes</span></span>](x-classes.md)





