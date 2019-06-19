---
title: 拡張機能のホーム ページ
description: このトピックでは、拡張性に関するトピックへのリンクを提供します。
author: FrankDahl
manager: AnnBe
ms.date: 05/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-14
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: e58f4291d6413117657a6aaa2e215c8d7386cb47
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595379"
---
# <a name="extensibility-home-page"></a><span data-ttu-id="d3c7c-103">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="d3c7c-103">Extensibility home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3c7c-104">Microsoft Dynamics 365 for Finance and Operations は、パートナー、付加価値再販業者 (VAR) や、さらには一部の顧客によって大幅にカスタマイズされます。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-104">Microsoft Dynamics 365 for Finance and Operations is extensively customized by partners, value added resellers (VARs), and even some customers.</span></span> <span data-ttu-id="d3c7c-105">製品をカスタマイズする機能は、アプリケーション コードのオーバーレイによって長くサポートされてきた強みです。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-105">The ability to customize the product is a strength that has historically been supported through overlayering of the application code.</span></span> <span data-ttu-id="d3c7c-106">クラウドへの移行を、柔軟なサービスの提供や頻繁な更新と合わせて行う場合、更新がカスタム ソリューションに及ぼす影響を小さくとどめるため、侵入性の低いカスタマイズが必要となります。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-106">The move to the cloud, together with more agile servicing and frequent updates, requires a less intrusive customization model, so that updates are less likely to affect custom solutions.</span></span> <span data-ttu-id="d3c7c-107">この新しいモデルは *拡張性* と呼ばれており、オーバーレイによるカスタマイズに取って代わる存在となりました。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-107">This new model is called *extensibility* and has replaced customization through overlayering.</span></span>

<span data-ttu-id="d3c7c-108">拡張性は、Finance and Operations と Microsoft Dynamics 365 for Retail における唯一のカスタマイズ フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-108">Extensibility is the only customization framework in Finance and Operations and Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="d3c7c-109">オーバーレイはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-109">Overlayering isn't supported.</span></span>

## <a name="introduction"></a><span data-ttu-id="d3c7c-110">はじめに</span><span class="sxs-lookup"><span data-stu-id="d3c7c-110">Introduction</span></span>

<span data-ttu-id="d3c7c-111">この概要のトピックでは、カスタマイズに関する一般情報を取り上げています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-111">These introductory topics contain general information about customization.</span></span> <span data-ttu-id="d3c7c-112">カスタマイズからオーバーレイを経て純粋な拡張ベース モデルに至る場合などに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-112">This information includes information about when the transition occurs from customization through overlayering to a purely extension-based model.</span></span> <span data-ttu-id="d3c7c-113">このトピックでは、Microsoft への拡張性の要求を記録する方法と、よく寄せられる質問 (FAQ) への回答についても解説します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-113">These topics also explain how to log extensibility requests to Microsoft, and provide answers to frequently asked questions (FAQ).</span></span>

+ [<span data-ttu-id="d3c7c-114">アプリケーション機能拡張計画</span><span class="sxs-lookup"><span data-stu-id="d3c7c-114">Application extensibility plans</span></span>](extensibility-roadmap.md)
+ [<span data-ttu-id="d3c7c-115">拡張性の要求</span><span class="sxs-lookup"><span data-stu-id="d3c7c-115">Extensibility requests</span></span>](extensibility-requests.md) 
+ [<span data-ttu-id="d3c7c-116">拡張性に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d3c7c-116">Extensibility FAQ</span></span>](app-sealing-faq.md) 

## <a name="whats-new"></a><span data-ttu-id="d3c7c-117">新機能</span><span class="sxs-lookup"><span data-stu-id="d3c7c-117">What's new</span></span>

<span data-ttu-id="d3c7c-118">2017 年 7 月以降に行われた拡張性関連の更新については [拡張性の新機能](extensibility-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-118">Read [What's new for extensibility](extensibility-new.md) for extensibility-related updates that have been made since July 2017.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d3c7c-119">はじめに</span><span class="sxs-lookup"><span data-stu-id="d3c7c-119">Getting started</span></span>

<span data-ttu-id="d3c7c-120">このセクションのトピックは、拡張機能の構築を開始するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-120">The topics in this section will help you start to build extensions.</span></span> <span data-ttu-id="d3c7c-121">また、オーバーレイ コードに基づいた現在のソリューションを、拡張機能ベースのソリューションに移行する上でも参考になる内容です。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-121">They will also help you migrate solutions that are currently based on overlayered code to extension-based solutions.</span></span> <span data-ttu-id="d3c7c-122">このセクションには、簡単なカスタマイズについて説明した実践ラボが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-122">This section includes hands-on labs that walk you through simple customizations.</span></span>

+ [<span data-ttu-id="d3c7c-123">オーバーレイから拡張機能への移行</span><span class="sxs-lookup"><span data-stu-id="d3c7c-123">Migrate from overlayering to extensions</span></span>](migrate-overlayer-extension.md)
+ [<span data-ttu-id="d3c7c-124">拡張機能を使用したモデル要素のカスタマイズ (チュートリアル)</span><span class="sxs-lookup"><span data-stu-id="d3c7c-124">Customize model elements using extensions (tutorial)</span></span>](customize-model-elements-extensions.md)
+ [<span data-ttu-id="d3c7c-125">カスタマイズ: オーバーレイと機能拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-125">Customization: overlayering and extensions</span></span>](customization-overlayering-extensions.md)
<!--+ [Customize by overlayering metadata source code (Office Mix)](https://mix.office.com/watch/1ol6ov90jrd4w)-->

## <a name="fundamentals-on-extensions"></a><span data-ttu-id="d3c7c-126">拡張機能の基本</span><span class="sxs-lookup"><span data-stu-id="d3c7c-126">Fundamentals on extensions</span></span>

<span data-ttu-id="d3c7c-127">このセクションでは、拡張機能の作成に関する基本や原則、手法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-127">This section includes fundamentals, principles, and practices for making extensions.</span></span> <span data-ttu-id="d3c7c-128">以下のトピックの指針では、拡張機能を使用してカスタマイズに取り組む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-128">The guiding principles in these topics discuss how customization must be approached through extensions.</span></span> <span data-ttu-id="d3c7c-129">この原則には、名前付けのガイドラインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-129">These principles include naming guidelines.</span></span> <span data-ttu-id="d3c7c-130">また、これらのトピックでは、拡張機能やコマンド チェーンなど、基盤となるフレームワークについても説明します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-130">Additionally, these topics discuss the foundation framework, such as extensions and chain of command.</span></span>

+ [<span data-ttu-id="d3c7c-131">侵入的なカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="d3c7c-131">Intrusive customizations</span></span>](intrusive-customizations.md)
+ [<span data-ttu-id="d3c7c-132">クラスの拡張機能</span><span class="sxs-lookup"><span data-stu-id="d3c7c-132">Class extensions</span></span>](class-extensions.md)
+ [<span data-ttu-id="d3c7c-133">クラスの拡張機能: メソッドのラッピングとコマンド チェーン</span><span class="sxs-lookup"><span data-stu-id="d3c7c-133">Class extension: Method wrapping and Chain of Command</span></span>](method-wrapping-coc.md)
+ [<span data-ttu-id="d3c7c-134">名前付けのガイドライン</span><span class="sxs-lookup"><span data-stu-id="d3c7c-134">Naming guidelines</span></span>](naming-guidelines-extensions.md)
+ [<span data-ttu-id="d3c7c-135">オーバレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する</span><span class="sxs-lookup"><span data-stu-id="d3c7c-135">Relax model restrictions to enable the refactoring of over-layering into extensions</span></span>](refactoring-over-layering.md)

## <a name="how-do-i-create-extensions"></a><span data-ttu-id="d3c7c-136">拡張機能の作成方法</span><span class="sxs-lookup"><span data-stu-id="d3c7c-136">How do I create extensions?</span></span>

<span data-ttu-id="d3c7c-137">このセクションは "方法" を含みます</span><span class="sxs-lookup"><span data-stu-id="d3c7c-137">This section includes "How do I?"</span></span> <span data-ttu-id="d3c7c-138">トピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-138">topics that explain how to customize specific object types or code.</span></span> <span data-ttu-id="d3c7c-139">このトピックのほとんどは、簡潔で要点を押さえた内容となっています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-139">Most of these topics are brief and to the point.</span></span> <span data-ttu-id="d3c7c-140">ここには多くのトピックがあるため、特定のトピックを検索すると便利にご利用いただける場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-140">Because there are many topics here, it might be practical to search for a specific topic.</span></span>

### <a name="data-types"></a><span data-ttu-id="d3c7c-141">データ型</span><span class="sxs-lookup"><span data-stu-id="d3c7c-141">Data types</span></span>
+ [<span data-ttu-id="d3c7c-142">列挙値の追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-142">Add an enum value</span></span>](add-enum-value.md)
+ [<span data-ttu-id="d3c7c-143">拡張データ型の変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-143">Modify an extended data type</span></span>](modify-edt.md) 

### <a name="classes"></a><span data-ttu-id="d3c7c-144">クラス</span><span class="sxs-lookup"><span data-stu-id="d3c7c-144">Classes</span></span>
+ [<span data-ttu-id="d3c7c-145">ファクトリ メソッドのサブクラスの登録</span><span class="sxs-lookup"><span data-stu-id="d3c7c-145">Register a subclass for factory methods</span></span>](register-subclass-factory-methods.md)
+ [<span data-ttu-id="d3c7c-146">EventHandlerResult を使用した応答</span><span class="sxs-lookup"><span data-stu-id="d3c7c-146">Respond with EventHandlerResult</span></span>](respond-event-handler-result.md)
+ [<span data-ttu-id="d3c7c-147">RunBase クラスの拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-147">Extend the RunBase class</span></span>](extend-runbase-class.md)
+ [<span data-ttu-id="d3c7c-148">デリゲートを使用したアプリケーション起動のカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="d3c7c-148">Use delegates to customize Application startup</span></span>](startup-customizations.md)

### <a name="tables"></a><span data-ttu-id="d3c7c-149">テーブル</span><span class="sxs-lookup"><span data-stu-id="d3c7c-149">Tables</span></span>
+ [<span data-ttu-id="d3c7c-150">テーブルの既存のフィールドの変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-150">Modify an existing field in a table</span></span>](modify-existing-field.md)
+ [<span data-ttu-id="d3c7c-151">既存のテーブルへの新しいフィールドの追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-151">Add a new field to an existing table</span></span>](add-field-extension.md)
+ [<span data-ttu-id="d3c7c-152">既存のテーブルへのインデックスの追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-152">Add an index to an existing table</span></span>](add-index.md)
+ [<span data-ttu-id="d3c7c-153">既存のテーブルへのリレーションの追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-153">Add a relation to an existing table</span></span>](add-relation.md)
+ [<span data-ttu-id="d3c7c-154">既存のテーブルのプロパティの変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-154">Modify properties on an existing table</span></span>](modify-properties.md)
+ [<span data-ttu-id="d3c7c-155">テーブルへのメソッドの追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-155">Add a method to a table</span></span>](add-method-table.md)
+ [<span data-ttu-id="d3c7c-156">テーブル レコードの有効期間中の業務処理の実行</span><span class="sxs-lookup"><span data-stu-id="d3c7c-156">Perform business actions throughout the lifecycle of a table record</span></span>](subscribe-table-events.md)

### <a name="forms"></a><span data-ttu-id="d3c7c-157">フォーム</span><span class="sxs-lookup"><span data-stu-id="d3c7c-157">Forms</span></span>
+ [<span data-ttu-id="d3c7c-158">フォームへの新しいデータ ソースの追加</span><span class="sxs-lookup"><span data-stu-id="d3c7c-158">Add a new data source to a form</span></span>](add-datasource.md)
+ [<span data-ttu-id="d3c7c-159">フォームのキャプションの変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-159">Change the caption on a form</span></span>](change-caption-form.md)
+ [<span data-ttu-id="d3c7c-160">フォーム コントロールのプロパティの変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-160">Modify form control properties</span></span>](modify-control-properties.md)

### <a name="others"></a><span data-ttu-id="d3c7c-161">その他</span><span class="sxs-lookup"><span data-stu-id="d3c7c-161">Others</span></span>
+ [<span data-ttu-id="d3c7c-162">小数点以下の精度の拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-162">Extending decimal point precision</span></span>](decimal-point-precision.md)

### <a name="reports"></a><span data-ttu-id="d3c7c-163">レポート</span><span class="sxs-lookup"><span data-stu-id="d3c7c-163">Reports</span></span>
+ [<span data-ttu-id="d3c7c-164">電子申告機能の一覧の拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-164">Extend the list of Electronic reporting functions</span></span>](../analytics/general-electronic-reporting-formulas-list-extension.md)
+ [<span data-ttu-id="d3c7c-165">アプリ スイート レポートのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="d3c7c-165">Customize App Suite reports</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

### <a name="blog-posts"></a><span data-ttu-id="d3c7c-166">ブログの投稿</span><span class="sxs-lookup"><span data-stu-id="d3c7c-166">Blog posts</span></span>

<span data-ttu-id="d3c7c-167">カスタマイズに関する情報は、さまざまなトピックが取り上げられるブログでも共有されます。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-167">Information about customization is also shared through blogs where various topics are discussed.</span></span> <span data-ttu-id="d3c7c-168">このセクションには、そのようなブログの一部への参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-168">This section includes reference to some of these blogs.</span></span>

+ [<span data-ttu-id="d3c7c-169">Dynamics 365 for Finance and Operations の拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-169">Extending Dynamics 365 for Finance and Operations</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-dynamics-365-for-operations/)
+ [<span data-ttu-id="d3c7c-170">クラスの状態の機能拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-170">Extending class state</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/01/31/extending-class-state/)
+ [<span data-ttu-id="d3c7c-171">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="d3c7c-171">Extension methods</span></span>](https://blogs.msdn.microsoft.com/mfp/2015/12/15/x-in-ax7-extension-methods/)
+ [<span data-ttu-id="d3c7c-172">拡張可能な基本列挙型</span><span class="sxs-lookup"><span data-stu-id="d3c7c-172">Extensible base enumerations</span></span>](https://kashperuk.blogspot.dk/2016/09/development-tutorial-extensible-base.html)
+ [<span data-ttu-id="d3c7c-173">静的イベント サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="d3c7c-173">Static event subscription</span></span>](https://blogs.msdn.microsoft.com/mfp/2015/12/10/x-in-ax7-static-event-subscription/)
+ [<span data-ttu-id="d3c7c-174">デリゲートを通じての応答</span><span class="sxs-lookup"><span data-stu-id="d3c7c-174">Responding through delegates</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/01/31/responding-through-delegates/)
+ [<span data-ttu-id="d3c7c-175">onValidatingWrite へのサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="d3c7c-175">Subscribing to onValidatingWrite</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/01/31/subscribing-to-onvalidatingwrite/)
+ [<span data-ttu-id="d3c7c-176">在庫分析コードの機能拡張</span><span class="sxs-lookup"><span data-stu-id="d3c7c-176">Extending inventory dimensions</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/08/10/extensible-inventory-dimensions/)
+ [<span data-ttu-id="d3c7c-177">Dynamics 365 for Finance and Operations での拡張機能のご要望を採用します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-177">Embrace the extensions mindset with Dynamics 365 for Finance and Operations</span></span>](https://blogs.msdn.microsoft.com/axinthefield/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations/)
+ [<span data-ttu-id="d3c7c-178">拡張可能な X++ - メソッドの署名</span><span class="sxs-lookup"><span data-stu-id="d3c7c-178">Extensible X++ - Method Signatures</span></span>](https://blogs.msdn.microsoft.com/mfp/2017/08/31/extensible-x-method-signatures/)

## <a name="how-do-i-create-an-extensible-solution"></a><span data-ttu-id="d3c7c-179">拡張可能なソリューションを作成するには</span><span class="sxs-lookup"><span data-stu-id="d3c7c-179">How do I create an extensible solution?</span></span>

<span data-ttu-id="d3c7c-180">このセクションでは、コードのユーザーがソリューションを拡張できるように、拡張可能なソリューションを作成する方法や、ソリューションを拡張可能にする方法に関するベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-180">This section includes some best practices on how to create/make your solution extensible, so that consumers of your code can extend your solution.</span></span>

+ [<span data-ttu-id="d3c7c-181">拡張可能なコードの記述</span><span class="sxs-lookup"><span data-stu-id="d3c7c-181">Writing extensible code</span></span>](writing-extensible-code.md)
+ [<span data-ttu-id="d3c7c-182">クラス</span><span class="sxs-lookup"><span data-stu-id="d3c7c-182">Classes</span></span>](extensible-classes.md)
+ [<span data-ttu-id="d3c7c-183">メソッド</span><span class="sxs-lookup"><span data-stu-id="d3c7c-183">Methods</span></span>](extensible-methods.md)
+ [<span data-ttu-id="d3c7c-184">フォーム</span><span class="sxs-lookup"><span data-stu-id="d3c7c-184">Forms</span></span>](extensible-forms.md)
+ [<span data-ttu-id="d3c7c-185">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="d3c7c-185">Extended data types</span></span>](extensible-edts.md)
+ [<span data-ttu-id="d3c7c-186">拡張可能な列挙</span><span class="sxs-lookup"><span data-stu-id="d3c7c-186">Extensible enums</span></span>](extensible-enums.md)
+ [<span data-ttu-id="d3c7c-187">委任</span><span class="sxs-lookup"><span data-stu-id="d3c7c-187">Delegates</span></span>](extensible-code-delegates.md)
+ [<span data-ttu-id="d3c7c-188">テーブル</span><span class="sxs-lookup"><span data-stu-id="d3c7c-188">Tables</span></span>](extensible-tables.md)
+ [<span data-ttu-id="d3c7c-189">メソッドの拡張属性</span><span class="sxs-lookup"><span data-stu-id="d3c7c-189">Extensibility attributes for methods</span></span>](extensibility-attributes.md)

## <a name="breaking-changes"></a><span data-ttu-id="d3c7c-190">重大な変更</span><span class="sxs-lookup"><span data-stu-id="d3c7c-190">Breaking changes</span></span>
<span data-ttu-id="d3c7c-191">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-191">When you make your solution extensible, you also help guarantee that you won't break those extension points later.</span></span> <span data-ttu-id="d3c7c-192">消費者に重大な影響が及ぶのを防ぐ指針に関しては、[重大な変更](breaking-changes.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="d3c7c-192">For pointers that can help you avoid breaking your consumers, see [Breaking changes](breaking-changes.md).</span></span>
