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
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2019-05-14
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 3cdf650c6ab7b8004c01c5c8b839af7a26f57ee4
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367015"
---
# <a name="extensibility-home-page"></a><span data-ttu-id="c569f-103">拡張機能のホーム ページ</span><span class="sxs-lookup"><span data-stu-id="c569f-103">Extensibility home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c569f-104">Dynamics 365 Finance、Supply Chain、およびコマースは、パートナー、付加価値再販業者 (VAR) や、さらには一部の顧客によって大幅にカスタマイズされます。</span><span class="sxs-lookup"><span data-stu-id="c569f-104">Dynamics 365 Finance, Supply Chain, and Commerce are extensively customized by partners, value added resellers (VARs), and even some customers.</span></span> <span data-ttu-id="c569f-105">製品をカスタマイズする機能は、アプリケーション コードのオーバーレイによって長くサポートされてきた強みです。</span><span class="sxs-lookup"><span data-stu-id="c569f-105">The ability to customize the product is a strength that has historically been supported through overlayering of the application code.</span></span> <span data-ttu-id="c569f-106">クラウドへの移行を、柔軟なサービスの提供や頻繁な更新と合わせて行う場合、更新がカスタム ソリューションに及ぼす影響を小さくとどめるため、侵入性の低いカスタマイズが必要となります。</span><span class="sxs-lookup"><span data-stu-id="c569f-106">The move to the cloud, together with more agile servicing and frequent updates, requires a less intrusive customization model, so that updates are less likely to affect custom solutions.</span></span> <span data-ttu-id="c569f-107">この新しいモデルは *拡張性* と呼ばれており、オーバーレイによるカスタマイズに取って代わる存在となりました。</span><span class="sxs-lookup"><span data-stu-id="c569f-107">This new model is called *extensibility* and has replaced customization through overlayering.</span></span>

<span data-ttu-id="c569f-108">拡張性は、Finance、Supply Chain、およびコマースにおける唯一のカスタマイズ フレームワークです。</span><span class="sxs-lookup"><span data-stu-id="c569f-108">Extensibility is the only customization framework in Finance, Supply Chain, and Commerce.</span></span> <span data-ttu-id="c569f-109">オーバーレイはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="c569f-109">Overlayering isn't supported.</span></span>

## <a name="introduction"></a><span data-ttu-id="c569f-110">はじめに</span><span class="sxs-lookup"><span data-stu-id="c569f-110">Introduction</span></span>

<span data-ttu-id="c569f-111">この概要のトピックでは、カスタマイズに関する一般情報を取り上げています。</span><span class="sxs-lookup"><span data-stu-id="c569f-111">These introductory topics contain general information about customization.</span></span> <span data-ttu-id="c569f-112">カスタマイズからオーバーレイを経て純粋な拡張ベース モデルに至る場合などに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="c569f-112">This information includes information about when the transition occurs from customization through overlayering to a purely extension-based model.</span></span> <span data-ttu-id="c569f-113">このトピックでは、Microsoft への拡張性の要求を記録する方法と、よく寄せられる質問 (FAQ) への回答についても解説します。</span><span class="sxs-lookup"><span data-stu-id="c569f-113">These topics also explain how to log extensibility requests to Microsoft, and provide answers to frequently asked questions (FAQ).</span></span>

+ [<span data-ttu-id="c569f-114">アプリケーション機能拡張計画</span><span class="sxs-lookup"><span data-stu-id="c569f-114">Application extensibility plans</span></span>](extensibility-roadmap.md)
+ [<span data-ttu-id="c569f-115">拡張性の要求</span><span class="sxs-lookup"><span data-stu-id="c569f-115">Extensibility requests</span></span>](extensibility-requests.md) 
+ [<span data-ttu-id="c569f-116">拡張性に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c569f-116">Extensibility FAQ</span></span>](app-sealing-faq.md) 

## <a name="whats-new"></a><span data-ttu-id="c569f-117">新機能</span><span class="sxs-lookup"><span data-stu-id="c569f-117">What's new</span></span>

<span data-ttu-id="c569f-118">2017 年 7 月以降に行われた拡張性関連の更新については [拡張性の新機能および変更された機能](extensibility-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c569f-118">Read [What's new or changed for extensibility](extensibility-new.md) for extensibility-related updates that have been made since July 2017.</span></span>

## <a name="getting-started"></a><span data-ttu-id="c569f-119">はじめに</span><span class="sxs-lookup"><span data-stu-id="c569f-119">Getting started</span></span>

<span data-ttu-id="c569f-120">このセクションのトピックは、拡張機能の構築を開始するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c569f-120">The topics in this section will help you start to build extensions.</span></span> <span data-ttu-id="c569f-121">また、オーバーレイ コードに基づいた現在のソリューションを、拡張機能ベースのソリューションに移行する上でも参考になる内容です。</span><span class="sxs-lookup"><span data-stu-id="c569f-121">They will also help you migrate solutions that are currently based on overlayered code to extension-based solutions.</span></span> <span data-ttu-id="c569f-122">このセクションには、簡単なカスタマイズについて説明した実践ラボが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c569f-122">This section includes hands-on labs that walk you through simple customizations.</span></span>

+ [<span data-ttu-id="c569f-123">オーバーレイから拡張機能への移行</span><span class="sxs-lookup"><span data-stu-id="c569f-123">Migrate from overlayering to extensions</span></span>](migrate-overlayer-extension.md)
+ [<span data-ttu-id="c569f-124">拡張機能によってモデル要素をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="c569f-124">Customize model elements through extension</span></span>](customize-model-elements-extensions.md)
+ [<span data-ttu-id="c569f-125">拡張機能およびオーバーレイによるカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c569f-125">Customize through extension and overlayering</span></span>](customization-overlayering-extensions.md)
<!--+ [Customize by overlayering metadata source code (Office Mix)](https://mix.office.com/watch/1ol6ov90jrd4w)-->

## <a name="fundamentals-on-extensions"></a><span data-ttu-id="c569f-126">拡張機能の基本</span><span class="sxs-lookup"><span data-stu-id="c569f-126">Fundamentals on extensions</span></span>

<span data-ttu-id="c569f-127">このセクションでは、拡張機能の作成に関する基本や原則、手法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c569f-127">This section includes fundamentals, principles, and practices for making extensions.</span></span> <span data-ttu-id="c569f-128">以下のトピックの指針では、拡張機能を使用してカスタマイズに取り組む方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c569f-128">The guiding principles in these topics discuss how customization must be approached through extensions.</span></span> <span data-ttu-id="c569f-129">この原則には、名前付けのガイドラインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c569f-129">These principles include naming guidelines.</span></span> <span data-ttu-id="c569f-130">また、これらのトピックでは、拡張機能やコマンド チェーンなど、基盤となるフレームワークについても説明します。</span><span class="sxs-lookup"><span data-stu-id="c569f-130">Additionally, these topics discuss the foundation framework, such as extensions and chain of command.</span></span>

+ [<span data-ttu-id="c569f-131">侵入的なカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="c569f-131">Intrusive customizations</span></span>](intrusive-customizations.md)
+ [<span data-ttu-id="c569f-132">X++ の拡張モデルのクラス</span><span class="sxs-lookup"><span data-stu-id="c569f-132">Class extension model in X++</span></span>](class-extensions.md)
+ [<span data-ttu-id="c569f-133">クラスの拡張機能 - メソッドのラッピングとコマンド チェーン</span><span class="sxs-lookup"><span data-stu-id="c569f-133">Class extension - Method wrapping and Chain of Command</span></span>](method-wrapping-coc.md)
+ [<span data-ttu-id="c569f-134">拡張機能の名前付けガイドライン</span><span class="sxs-lookup"><span data-stu-id="c569f-134">Naming guidelines for extensions</span></span>](naming-guidelines-extensions.md)
+ [<span data-ttu-id="c569f-135">オーバーレイを拡張機能にリファクタリングするため、モデルの制限を緩和する</span><span class="sxs-lookup"><span data-stu-id="c569f-135">Relax model restrictions to refactor overlayering into extensions</span></span>](refactoring-over-layering.md)

## <a name="how-do-i-create-extensions"></a><span data-ttu-id="c569f-136">拡張機能の作成方法</span><span class="sxs-lookup"><span data-stu-id="c569f-136">How do I create extensions?</span></span>

<span data-ttu-id="c569f-137">このセクションは "方法" を含みます</span><span class="sxs-lookup"><span data-stu-id="c569f-137">This section includes "How do I?"</span></span> <span data-ttu-id="c569f-138">トピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="c569f-138">topics that explain how to customize specific object types or code.</span></span> <span data-ttu-id="c569f-139">このトピックのほとんどは、簡潔で要点を押さえた内容となっています。</span><span class="sxs-lookup"><span data-stu-id="c569f-139">Most of these topics are brief and to the point.</span></span> <span data-ttu-id="c569f-140">ここには多くのトピックがあるため、特定のトピックを検索すると便利にご利用いただける場合があります。</span><span class="sxs-lookup"><span data-stu-id="c569f-140">Because there are many topics here, it might be practical to search for a specific topic.</span></span>

### <a name="data-types"></a><span data-ttu-id="c569f-141">データ型</span><span class="sxs-lookup"><span data-stu-id="c569f-141">Data types</span></span>
+ [<span data-ttu-id="c569f-142">拡張機能を使用して列挙体に値を追加</span><span class="sxs-lookup"><span data-stu-id="c569f-142">Add values to enums through extension</span></span>](add-enum-value.md)
+ [<span data-ttu-id="c569f-143">拡張機能を通じて拡張データ型 (EDT) を変更する</span><span class="sxs-lookup"><span data-stu-id="c569f-143">Modify extended data types (EDTs) through extension</span></span>](modify-edt.md) 

### <a name="classes"></a><span data-ttu-id="c569f-144">クラス</span><span class="sxs-lookup"><span data-stu-id="c569f-144">Classes</span></span>
+ [<span data-ttu-id="c569f-145">ファクトリ メソッドのサブクラスの登録</span><span class="sxs-lookup"><span data-stu-id="c569f-145">Register subclasses for factory methods</span></span>](register-subclass-factory-methods.md)
+ [<span data-ttu-id="c569f-146">EventHandlerResult を使用して応答</span><span class="sxs-lookup"><span data-stu-id="c569f-146">Respond by using EventHandlerResult</span></span>](respond-event-handler-result.md)
+ [<span data-ttu-id="c569f-147">RunBase クラスの拡張</span><span class="sxs-lookup"><span data-stu-id="c569f-147">Extend the RunBase class</span></span>](extend-runbase-class.md)
+ [<span data-ttu-id="c569f-148">デリゲートを使用してアプリケーション起動をカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="c569f-148">Customize application startup by using delegates</span></span>](startup-customizations.md)

### <a name="tables"></a><span data-ttu-id="c569f-149">テーブル</span><span class="sxs-lookup"><span data-stu-id="c569f-149">Tables</span></span>
+ [<span data-ttu-id="c569f-150">拡張機能を使用したテーブル内の既存のフィールドの変更</span><span class="sxs-lookup"><span data-stu-id="c569f-150">Modify existing fields in a table through extension</span></span>](modify-existing-field.md)
+ [<span data-ttu-id="c569f-151">拡張機能を使用してテーブルにフィールドを追加</span><span class="sxs-lookup"><span data-stu-id="c569f-151">Add fields to tables through extension</span></span>](add-field-extension.md)
+ [<span data-ttu-id="c569f-152">拡張機能を使用してテーブルにインデックスを追加</span><span class="sxs-lookup"><span data-stu-id="c569f-152">Add indexes to tables through extension</span></span>](add-index.md)
+ [<span data-ttu-id="c569f-153">拡張機能を使用してテーブルに関係を追加</span><span class="sxs-lookup"><span data-stu-id="c569f-153">Add relations to tables through extension</span></span>](add-relation.md)
+ [<span data-ttu-id="c569f-154">拡張機能を使用して、テーブルのプロパティを変更する</span><span class="sxs-lookup"><span data-stu-id="c569f-154">Modify table properties through extension</span></span>](modify-properties.md)
+ [<span data-ttu-id="c569f-155">拡張機能を使用してテーブルにメソッドを追加</span><span class="sxs-lookup"><span data-stu-id="c569f-155">Add methods to tables through extension</span></span>](add-method-table.md)
+ [<span data-ttu-id="c569f-156">テーブル レコードの有効期間中の業務処理の実行</span><span class="sxs-lookup"><span data-stu-id="c569f-156">Perform business actions throughout the lifecycle of table records</span></span>](subscribe-table-events.md)

### <a name="forms"></a><span data-ttu-id="c569f-157">フォーム</span><span class="sxs-lookup"><span data-stu-id="c569f-157">Forms</span></span>
+ [<span data-ttu-id="c569f-158">フォームへの新しいデータ ソースの追加</span><span class="sxs-lookup"><span data-stu-id="c569f-158">Add a new data source to a form</span></span>](add-datasource.md)
+ [<span data-ttu-id="c569f-159">拡張機能によって、フォームのキャプションを変更します。</span><span class="sxs-lookup"><span data-stu-id="c569f-159">Change the captions of forms through extension</span></span>](change-caption-form.md)
+ [<span data-ttu-id="c569f-160">拡張機能を使用して、フォーム コントロールのプロパティを変更する</span><span class="sxs-lookup"><span data-stu-id="c569f-160">Modify the properties of form controls through extension</span></span>](modify-control-properties.md)

### <a name="others"></a><span data-ttu-id="c569f-161">その他</span><span class="sxs-lookup"><span data-stu-id="c569f-161">Others</span></span>
+ [<span data-ttu-id="c569f-162">選択したデータ型の小数点以下の精度の拡張</span><span class="sxs-lookup"><span data-stu-id="c569f-162">Extending decimal point precision for selected data types</span></span>](decimal-point-precision.md)
+ [<span data-ttu-id="c569f-163">拡張機能を通じた新しい在庫分析コードの追加</span><span class="sxs-lookup"><span data-stu-id="c569f-163">Add new inventory dimensions through extension</span></span>](inventory-dimensions.md)

### <a name="reports"></a><span data-ttu-id="c569f-164">レポート</span><span class="sxs-lookup"><span data-stu-id="c569f-164">Reports</span></span>
+ [<span data-ttu-id="c569f-165">電子申告 (ER) 機能の一覧の拡張</span><span class="sxs-lookup"><span data-stu-id="c569f-165">Extend the list of Electronic reporting (ER) functions</span></span>](../analytics/general-electronic-reporting-formulas-list-extension.md)
+ [<span data-ttu-id="c569f-166">拡張機能を使用してアプリケーション スイート レポートをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="c569f-166">Customize App Suite reports by using extensions</span></span>](../analytics/customize-app-suite-reports-with-extensions.md)

### <a name="blog-posts"></a><span data-ttu-id="c569f-167">ブログの投稿</span><span class="sxs-lookup"><span data-stu-id="c569f-167">Blog posts</span></span>

<span data-ttu-id="c569f-168">カスタマイズに関する情報は、さまざまなトピックが取り上げられるブログでも共有されます。</span><span class="sxs-lookup"><span data-stu-id="c569f-168">Information about customization is also shared through blogs where various topics are discussed.</span></span> <span data-ttu-id="c569f-169">このセクションには、そのようなブログの一部への参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="c569f-169">This section includes reference to some of these blogs.</span></span>

+ [<span data-ttu-id="c569f-170">Dynamics 365 for Finance and Operations の拡張</span><span class="sxs-lookup"><span data-stu-id="c569f-170">Extending Dynamics 365 for Finance and Operations</span></span>](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extending-dynamics-365-for-operations)
+ [<span data-ttu-id="c569f-171">拡張メソッド</span><span class="sxs-lookup"><span data-stu-id="c569f-171">Extension methods</span></span>](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/x-in-ax7-extension-methods/)
+ [<span data-ttu-id="c569f-172">拡張可能な基本列挙型</span><span class="sxs-lookup"><span data-stu-id="c569f-172">Extensible base enumerations</span></span>](https://kashperuk.blogspot.dk/2016/09/development-tutorial-extensible-base.html)
+ [<span data-ttu-id="c569f-173">静的イベント サブスクリプション</span><span class="sxs-lookup"><span data-stu-id="c569f-173">Static event subscription</span></span>](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/x-in-ax7-static-event-subscription/)
+ [<span data-ttu-id="c569f-174">onValidatingWrite へのサブスクライブ</span><span class="sxs-lookup"><span data-stu-id="c569f-174">Subscribing to onValidatingWrite</span></span>](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/subscribing-to-onvalidatingwrite/)
+ [<span data-ttu-id="c569f-175">Dynamics 365 for Finance and Operations での拡張機能のご要望を採用します。</span><span class="sxs-lookup"><span data-stu-id="c569f-175">Embrace the extensions mindset with Dynamics 365 for Finance and Operations</span></span>](https://community.dynamics.com/ax/b/axinthefield/posts/embrace-the-extensions-mindset-with-dynamics-365-for-finance-and-operations-2-sysextension-framework)
+ [<span data-ttu-id="c569f-176">拡張可能な X++ - メソッドの署名</span><span class="sxs-lookup"><span data-stu-id="c569f-176">Extensible X++ - Method Signatures</span></span>](https://community.dynamics.com/365/financeandoperations/b/mfp/posts/extensible-x-method-signatures/)

## <a name="how-do-i-create-an-extensible-solution"></a><span data-ttu-id="c569f-177">拡張可能なソリューションを作成するには</span><span class="sxs-lookup"><span data-stu-id="c569f-177">How do I create an extensible solution?</span></span>

<span data-ttu-id="c569f-178">このセクションでは、コードのユーザーがソリューションを拡張できるように、拡張可能なソリューションを作成する方法や、ソリューションを拡張可能にする方法に関するベスト プラクティスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c569f-178">This section includes some best practices on how to create/make your solution extensible, so that consumers of your code can extend your solution.</span></span>

+ [<span data-ttu-id="c569f-179">拡張可能なコードの書き込み</span><span class="sxs-lookup"><span data-stu-id="c569f-179">Write extensible code</span></span>](writing-extensible-code.md)
+ [<span data-ttu-id="c569f-180">クラス</span><span class="sxs-lookup"><span data-stu-id="c569f-180">Classes</span></span>](extensible-classes.md)
+ [<span data-ttu-id="c569f-181">メソッド</span><span class="sxs-lookup"><span data-stu-id="c569f-181">Methods</span></span>](extensible-methods.md)
+ [<span data-ttu-id="c569f-182">フォーム</span><span class="sxs-lookup"><span data-stu-id="c569f-182">Forms</span></span>](extensible-forms.md)
+ [<span data-ttu-id="c569f-183">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="c569f-183">Extended data types</span></span>](extensible-edts.md)
+ [<span data-ttu-id="c569f-184">拡張可能な列挙</span><span class="sxs-lookup"><span data-stu-id="c569f-184">Extensible enums</span></span>](extensible-enums.md)
+ [<span data-ttu-id="c569f-185">委任</span><span class="sxs-lookup"><span data-stu-id="c569f-185">Delegates</span></span>](extensible-code-delegates.md)
+ [<span data-ttu-id="c569f-186">テーブル</span><span class="sxs-lookup"><span data-stu-id="c569f-186">Tables</span></span>](extensible-tables.md)
+ [<span data-ttu-id="c569f-187">メソッドを拡張可能にする属性</span><span class="sxs-lookup"><span data-stu-id="c569f-187">Attributes that make methods extensible</span></span>](extensibility-attributes.md)

## <a name="breaking-changes"></a><span data-ttu-id="c569f-188">変更の分割</span><span class="sxs-lookup"><span data-stu-id="c569f-188">Breaking changes</span></span>

<span data-ttu-id="c569f-189">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</span><span class="sxs-lookup"><span data-stu-id="c569f-189">When you make your solution extensible, you also help guarantee that you won't break those extension points later.</span></span> 

+ <span data-ttu-id="c569f-190">消費者に重大な影響が及ぶのを防ぐ指針に関しては、[重大な変更](breaking-changes.md) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="c569f-190">For pointers that can help you avoid breaking your consumers, see [Breaking changes](breaking-changes.md).</span></span>
+ <span data-ttu-id="c569f-191">[互換性チェック ツール](compatibility-checker-tool.md) を使用すると、指定されたベースライ ンリリースまたは更新に対して、メタデータの互換性に影響する変更を検出できます。</span><span class="sxs-lookup"><span data-stu-id="c569f-191">The [compatibility checker tool](compatibility-checker-tool.md) can detect metadata breaking changes against a given baseline release or update, helping to ensure backward compatibility.</span></span>
