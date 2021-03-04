---
title: Finance and Operations へのコード移行の準備
description: このトピックでは、コード アップグレード サービスと Visual Studio ツールを使用して、Dynamics AX 2012 R3 から Finance and Operations に移行する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 11/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 25971
ms.assetid: a911b0f2-a7b0-4643-bf5b-16e55c9397be
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bbe780b9e23b20ca3f9bff7d193610cbc172e58
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127171"
---
# <a name="prepare-to-migrate-code-to-finance-and-operations"></a><span data-ttu-id="89d53-103">Finance and Operations へのコード移行の準備</span><span class="sxs-lookup"><span data-stu-id="89d53-103">Prepare to migrate code to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89d53-104">このトピックでは、Lifecycle Services のコード アップグレード サービスと Visual Studio ツールを使用して、コードとメタデータを Dynamics AX 2012 R3 から Finance and Operations に移行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89d53-104">This topic describes how the Lifecycle Services code upgrade service and Visual Studio tools help you migrate your code and metadata from Dynamics AX 2012 R3 to Finance and Operations.</span></span> <span data-ttu-id="89d53-105">これらの手順のほとんどは、Finance and Operations の 2 つのメジャー バージョンの間でのコードの移行にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-105">Most of these steps also apply to code migration between two major versions of Finance and Operations.</span></span> 

<a name="prerequisites"></a><span data-ttu-id="89d53-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="89d53-106">Prerequisites</span></span>
-------------

<span data-ttu-id="89d53-107">リモート デスクトップを使用して Finance and Operations 開発環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-107">You will need access to a Finance and Operations development environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="89d53-108">コードをアップグレードする前に、Finance and Operations の開発、カスタマイズ、およびユーザー インターフェイスの概念の幾つかをよく理解しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="89d53-108">We recommend you become familiar with some of the Finance and  Operations development, customization, and user interface concepts before you upgrade your code.</span></span> <span data-ttu-id="89d53-109">次にいくつかの参照を挙げます。</span><span class="sxs-lookup"><span data-stu-id="89d53-109">Here are some references.</span></span>

-   [<span data-ttu-id="89d53-110">開発ツール</span><span class="sxs-lookup"><span data-stu-id="89d53-110">Development tools</span></span>](../dev-tools/developer-home-page.md)
-   [<span data-ttu-id="89d53-111">モデルとパッケージ</span><span class="sxs-lookup"><span data-stu-id="89d53-111">Models and packages</span></span>](../dev-tools/models.md)
-   [<span data-ttu-id="89d53-112">X++ プログラミング言語</span><span class="sxs-lookup"><span data-stu-id="89d53-112">X++ programming language</span></span>](../dev-ref/xpp-language-reference.md)
-   [<span data-ttu-id="89d53-113">拡張機能およびオーバーレイ</span><span class="sxs-lookup"><span data-stu-id="89d53-113">Extensions and Overlayering</span></span>](../extensibility/extensibility-home-page.md)
-   [<span data-ttu-id="89d53-114">ユーザー インターフェイス開発</span><span class="sxs-lookup"><span data-stu-id="89d53-114">User interface development</span></span>](../user-interface/user-interface-development-home-page.md)

## <a name="overview-of-the-code-migration-process"></a><span data-ttu-id="89d53-115">コード移行プロセスの概要</span><span class="sxs-lookup"><span data-stu-id="89d53-115">Overview of the code migration process</span></span>
### <a name="model-split"></a><span data-ttu-id="89d53-116">分割されたモデル</span><span class="sxs-lookup"><span data-stu-id="89d53-116">Model split</span></span>

<span data-ttu-id="89d53-117">Finance and Operations アプリケーションは、次のいくつかのパッケージ、またはアセンブリに分割されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-117">The Finance and Operations application is split into several packages, or assemblies:</span></span> 

<span data-ttu-id="89d53-118">**プラットフォームパッケージ**</span><span class="sxs-lookup"><span data-stu-id="89d53-118">**Platform Packages**</span></span>

-   <span data-ttu-id="89d53-119">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="89d53-119">Application Platform</span></span>
-   <span data-ttu-id="89d53-120">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="89d53-120">Application Foundation</span></span>
-   <span data-ttu-id="89d53-121">Test Essentials</span><span class="sxs-lookup"><span data-stu-id="89d53-121">Test Essentials</span></span>

<span data-ttu-id="89d53-122">**アプリケーション パッケージ**</span><span class="sxs-lookup"><span data-stu-id="89d53-122">**Application Packages**</span></span>

-   <span data-ttu-id="89d53-123">Application Suite</span><span class="sxs-lookup"><span data-stu-id="89d53-123">Application Suite</span></span>
-   <span data-ttu-id="89d53-124">他のアプリケーション パッケージ</span><span class="sxs-lookup"><span data-stu-id="89d53-124">Other application packages.</span></span>

<span data-ttu-id="89d53-125">ISV および Dynamics AX 2012 R3 から移行された顧客コードは、正しいパッケージに再ベースラインされます。</span><span class="sxs-lookup"><span data-stu-id="89d53-125">ISV and customer code that is migrated from Dynamics AX 2012 R3 will be re-baselined into the correct package.</span></span>

### <a name="auto-migration-using-the-lcs-code-upgrade-service"></a><span data-ttu-id="89d53-126">LCS コードのアップグレード サービスを使用して自動移行</span><span class="sxs-lookup"><span data-stu-id="89d53-126">Auto-migration using the LCS Code Upgrade service</span></span>

<span data-ttu-id="89d53-127">LCS コードのアップグレード サービスは、Dynamics AX 2012 R3 モデル ストアを入力として受け取り、次の作業を完了します。</span><span class="sxs-lookup"><span data-stu-id="89d53-127">The LCS code upgrade service takes a Dynamics AX 2012 R3 model store as input and completes the following tasks:</span></span>

-   <span data-ttu-id="89d53-128">メタデータを最新の形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="89d53-128">Converts metadata into the latest format.</span></span>
-   <span data-ttu-id="89d53-129">適切なモデルに移動およびマージすることで、メタデータのベースラインを再度設定します。</span><span class="sxs-lookup"><span data-stu-id="89d53-129">Re-baselines metadata, by moving and merging, into the right model.</span></span>
-   <span data-ttu-id="89d53-130">ソリューションのアップグレードに必要な作業を理解する見積を提供します。</span><span class="sxs-lookup"><span data-stu-id="89d53-130">Provides an estimation to understand the effort required to upgrade the solution.</span></span>
-   <span data-ttu-id="89d53-131">ソリューションの一部を自動移行する移行ルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="89d53-131">Runs migration rules that auto-migrate parts of a solution.</span></span>
-   <span data-ttu-id="89d53-132">TODO を使って手動で修正する内容を開発者に知らせる移行ルールを実行します。</span><span class="sxs-lookup"><span data-stu-id="89d53-132">Runs migration rules that inform developers what to manually fix by using TODOs.</span></span>
-   <span data-ttu-id="89d53-133">アップグレードされたソリューションを Azure DevOps プロジェクトに自動的にチェックインします。</span><span class="sxs-lookup"><span data-stu-id="89d53-133">Automatically checks-in the upgraded solution into your Azure DevOps project.</span></span>

<span data-ttu-id="89d53-134">コード アップグレード サービスを設定および実行する方法については、[[Lifecycle Services (LCS) でコード アップグレード サービスを構成および実行する](../lifecycle-services/configure-execute-code-upgrade.md)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-134">To configure and run the code upgrade service, see [Configure the code upgrade service in Lifecycle Services (LCS)](../lifecycle-services/configure-execute-code-upgrade.md).</span></span>

### <a name="manual-migration-steps"></a><span data-ttu-id="89d53-135">手動での移行の手順</span><span class="sxs-lookup"><span data-stu-id="89d53-135">Manual migration steps</span></span>

<span data-ttu-id="89d53-136">LCS コード アップグレード サービス構成のコードをアップグレードした後、開発者の VM と Azure DevOps にアップグレードされたコード ブランチに接続します。</span><span class="sxs-lookup"><span data-stu-id="89d53-136">After you upgrade your code using the LCS code upgrade service configure your developer VM and Azure DevOps to connect to the upgraded code branch.</span></span>

-   [<span data-ttu-id="89d53-137">1 ボックス開発環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="89d53-137">Configure one-box development environments</span></span>](../dev-tools/configure-developer-vm.md)
-   [<span data-ttu-id="89d53-138">コード移動中の Azure DevOps マッピングのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="89d53-138">Configure the Azure DevOps mapping during code migration</span></span>](configure-vso-solution.md)

<span data-ttu-id="89d53-139">コードのアップグレード サービスは、コードをコンパイルするために開くことができる Visual Studio ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="89d53-139">The code upgrade service will provide with Visual Studio solutions that you can open to compile your code.</span></span> <span data-ttu-id="89d53-140">競合を含むすべての要素向けの **コード マージ** ソリューションと、すべてのアップグレードされた要素向けの **アップグレード** ソリューション。</span><span class="sxs-lookup"><span data-stu-id="89d53-140">A **code merge** solution for all elements that contain conflicts and an **upgraded** solutions for all your upgraded elements.</span></span> <span data-ttu-id="89d53-141">通常、以下の順序でコンパイル エラーを修正して、アプリケーションをコンパイルできます。</span><span class="sxs-lookup"><span data-stu-id="89d53-141">Typically, you can compile the application by fixing compilation errors in the order shown below.</span></span> <span data-ttu-id="89d53-142">順序はパッケージの依存関係のグラフに基づいて決定され、グラフの中で最も低いパッケージから開始されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-142">The order is determined based on the package dependencies graph, start with the lowest package in the graph.</span></span> <span data-ttu-id="89d53-143">パッケージの依存関係を調べるには、[モデルおよびパッケージ](../dev-tools/models.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-143">To determine package dependencies, see [Models and packages](../dev-tools/models.md).</span></span> <span data-ttu-id="89d53-144">標準的な注文は、Application Platform、Application Foundation、Directory など、Application Suite です。</span><span class="sxs-lookup"><span data-stu-id="89d53-144">A typical order is Application Platform, Application Foundation, Directory, ...etc., Application Suite.</span></span> <span data-ttu-id="89d53-145">各アップグレードされたモデル対象:</span><span class="sxs-lookup"><span data-stu-id="89d53-145">For each of your upgraded models:</span></span>

-   <span data-ttu-id="89d53-146">マージの競合を修正します。</span><span class="sxs-lookup"><span data-stu-id="89d53-146">Fix merge conflicts.</span></span>
-   <span data-ttu-id="89d53-147">モデルの分割 (パッケージ全体の参照) に関連するコンパイル エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="89d53-147">Fix compilation errors related to a model split (references across packages).</span></span>
    -   <span data-ttu-id="89d53-148">一般的なエラー メッセージは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="89d53-148">Typical error messages are:</span></span>
        -   <span data-ttu-id="89d53-149">&lt;要素タイプ&gt; X は、存在しない &lt;要素タイプ&gt; Y を参照します。</span><span class="sxs-lookup"><span data-stu-id="89d53-149">&lt;Element Type&gt; X refers to &lt;Element Type&gt; Y which does not exist.</span></span>
        -   <span data-ttu-id="89d53-150">名前 &lt;Name&gt; はクラス、テーブル、または拡張データ型を示すものではありません。</span><span class="sxs-lookup"><span data-stu-id="89d53-150">The name &lt;Name&gt; does not denote a class, a table or an extended data type.</span></span>
    -   <span data-ttu-id="89d53-151">たとえば、オーバーレイされたカスタマイズは、パッケージの依存関係グラフの上位にある要素またはコードを参照している場合があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-151">For example, your overlayering customizations may be referencing elements or code that are higher in the package dependency graph:</span></span>
        -   <span data-ttu-id="89d53-152">ディレクトリ モデル内のメソッドは、アプリケーション スイート パッケージ内のテーブルを参照しています。</span><span class="sxs-lookup"><span data-stu-id="89d53-152">A method in the Directory model is referencing a table in the Application Suite package.</span></span>
        -   <span data-ttu-id="89d53-153">ディレクトリ パッケージ内のフォームは、アプリケーション スイート パッケージ内のデータ ソースを参照しています。</span><span class="sxs-lookup"><span data-stu-id="89d53-153">A form in the Directory package is referencing a data source in the Application Suite package.</span></span>
    -   <span data-ttu-id="89d53-154">モデル要素またはビジネス ロジックを上位のパッケージに移動することによって、これらの依存関係に対応するようにコードをリファクターする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-154">You will have to refactor your code to address these dependencies by moving model elements or business logic to higher level packages.</span></span>
    -   <span data-ttu-id="89d53-155">[コードの移行中にデリゲートを使用してモデル間の依存関係を解決する](delegates-migration.md) は、これらの問題を解決する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="89d53-155">[Solve dependencies among models by using delegates during code migration](delegates-migration.md) describes how to use delegates to solve some of these issues.</span></span>
-   <span data-ttu-id="89d53-156">コンパイル エラーを修正します。</span><span class="sxs-lookup"><span data-stu-id="89d53-156">Fix compilation errors.</span></span>

<span data-ttu-id="89d53-157">すべてのコンパイル エラーを解決した後は、すべてのパッケージがコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="89d53-157">After you have resolved all of the compilation errors, all packages will compile.</span></span> <span data-ttu-id="89d53-158">次に、次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-158">Next, you must complete the following tasks:</span></span>

1.  <span data-ttu-id="89d53-159">ガイド付きコード アップグレード TODO とコード アップグレード固有のベスト プラクティス警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="89d53-159">Address guided code upgrade TODOs and code upgrade-specific best practice warnings.</span></span> <span data-ttu-id="89d53-160">いくつかの例と詳細を以下のセクションに示します。</span><span class="sxs-lookup"><span data-stu-id="89d53-160">Some examples and details are in the sections below.</span></span>
2.  <span data-ttu-id="89d53-161">たとえば、ActiveX や代替の検索など、非推奨のコントロールを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89d53-161">Replace deprecated controls, for example, ActiveX or find an alternative.</span></span>
3.  <span data-ttu-id="89d53-162">すべてのフォームにフォーム パターンとサブ パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="89d53-162">Apply form patterns and sub patterns to all forms.</span></span>
4.  <span data-ttu-id="89d53-163">すべてのシナリオが、カスタム パターンに対して異なるサイズで、複数のブラウザーで動作することを検証します。</span><span class="sxs-lookup"><span data-stu-id="89d53-163">Validate that all scenarios work in multiple browsers with different sizes for custom patterns.</span></span>
5.  <span data-ttu-id="89d53-164">記述してテストを実行します。</span><span class="sxs-lookup"><span data-stu-id="89d53-164">Write and run tests.</span></span>

## <a name="best-practice-setup"></a><span data-ttu-id="89d53-165">ベスト プラクティスの設定</span><span class="sxs-lookup"><span data-stu-id="89d53-165">Best practice setup</span></span>
<span data-ttu-id="89d53-166">ベスト プラクティス フレームワークには、移行を完了するために解決する必要があるベスト プラクティス警告のサブセットがあります。</span><span class="sxs-lookup"><span data-stu-id="89d53-166">In the Best Practice framework, there is a subset of Best Practice warnings that need to be resolved to complete migration.</span></span> <span data-ttu-id="89d53-167">これは、Dynamics AX 2012 R3 またはそれ以前から移行する場合に適用されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-167">This applies if you are migrating from Dynamics AX 2012 R3 or earlier.</span></span>

1.  <span data-ttu-id="89d53-168">Visual Studio で、**Dynamics 365 &gt; オプション &gt; ベスト プラクティス** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-168">In Visual Studio, click **Dynamics 365 &gt; Options &gt; Best Practices**.</span></span>
2.  <span data-ttu-id="89d53-169">**モデル** ドロップダウン メニューで、**アプリケーション スイート** を選択します (作業しているすべてのモデルで繰り返します)</span><span class="sxs-lookup"><span data-stu-id="89d53-169">In the **Model** drop-down menu, select **Application Suite** (Repeat with all models you are working on)</span></span>

<span data-ttu-id="89d53-170">これらのルールは、ソリューションの移行中に「オン」に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-170">These rules should be set to “ON” while migrating your solution.</span></span> <span data-ttu-id="89d53-171">この設定は、AxRuleSet フォルダー内の XML ファイルによって実行されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-171">The setting is driven by an XML file in the AxRuleSet folder.</span></span> <span data-ttu-id="89d53-172">たとえば、C:\\Packages\\ApplicationSuite\\Foundation\\AxRuleSet の下にある、アプリケーション スイート xml ファイル、BPRules.xml を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-172">For example, see the Application Suite xml file, BPRules.xml, located under C:\\Packages\\ApplicationSuite\\Foundation\\AxRuleSet.</span></span> 

<span data-ttu-id="89d53-173">[![bpupgraderules](./media/bpupgraderules.png)](./media/bpupgraderules.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-173">[![bpupgraderules](./media/bpupgraderules.png)](./media/bpupgraderules.png)</span></span> 

<span data-ttu-id="89d53-174">移行を完了するには、すべての移行固有のベスト プラクティス ルールを修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-174">To complete the migration, you need to fix all migration-specific Best Practice rules.</span></span> <span data-ttu-id="89d53-175">エラーは警告としてエラー リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-175">The errors will show up in the error list as warnings.</span></span> <span data-ttu-id="89d53-176">エラー一覧には、コンパイラの警告やベスト プラクティスのエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-176">In the error list, you will see compiler warnings and best practice errors.</span></span> <span data-ttu-id="89d53-177">ベスト プラクティスのエラーには接頭語として **BP** のテキストが付けられます。</span><span class="sxs-lookup"><span data-stu-id="89d53-177">Best Practice errors are prefixed with the text **BP**.</span></span> <span data-ttu-id="89d53-178">たとえば、**BPErrorFormControlPatternUnspecified**。</span><span class="sxs-lookup"><span data-stu-id="89d53-178">For example, **BPErrorFormControlPatternUnspecified**.</span></span>

## <a name="debugging"></a><span data-ttu-id="89d53-179">デバッグ</span><span class="sxs-lookup"><span data-stu-id="89d53-179">Debugging</span></span>
<span data-ttu-id="89d53-180">既定では、Finance and Operations は作業中のファイルのデバッグ環境を最適化します。</span><span class="sxs-lookup"><span data-stu-id="89d53-180">By default, Finance and Operations optimizes the debugging experience for the files that you are working on.</span></span> <span data-ttu-id="89d53-181">結果として、プロジェクトに含まれていないファイル (F11) にステップ インすると、 PDB が読み込まれず、コードをデバッグできなくなります。</span><span class="sxs-lookup"><span data-stu-id="89d53-181">As a result, when you step into a file (F11) that is not in your project, the PDBs are not loaded and you can’t debug the code.</span></span> <span data-ttu-id="89d53-182">この問題を回避するには、<strong>Dynamics 365 **&gt;**オプション</strong>&gt;<strong>デバッグ</strong> をクリックしてプロジェクトのデバッグ設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="89d53-182">To work around this, change the project debugging setting by clicking <strong>Dynamics 365 \*\*&gt; \*\*Options</strong> &gt; <strong>Debugging</strong>.</span></span> <span data-ttu-id="89d53-183"><strong>ソリューション内の項目に対してのみシンボルを読み込む</strong> チェックボックスが選択されていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="89d53-183">Verify that the <strong>Load symbols only for items in the solution</strong> check box is not selected.</span></span> <span data-ttu-id="89d53-184">このオプションは、デバッガの速度を大幅に向上させるため、既定で選択されています。</span><span class="sxs-lookup"><span data-stu-id="89d53-184">This option is selected by default because it improves the debugger speed significantly.</span></span> <span data-ttu-id="89d53-185">Intellitrace をオフにしたい場合、別のデバッグ設定をします。</span><span class="sxs-lookup"><span data-stu-id="89d53-185">Another debugging setting that you may want to turn off is Intellitrace.</span></span> <span data-ttu-id="89d53-186">Intellitrace はアプリケーションの完全な実行履歴を収集します。</span><span class="sxs-lookup"><span data-stu-id="89d53-186">Intellitrace collects the complete execution history of an application.</span></span> <span data-ttu-id="89d53-187">デバッグ時に IDE で多くのノイズが作成されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-187">It creates a lot of noise in the IDE when debugging.</span></span> <span data-ttu-id="89d53-188">Intellitrace をオフにするには、<strong>オプション</strong>&gt;<strong>IntelliTrace</strong>&gt;<strong>IntelliTrace を有効にする</strong> をクリックしてチェック ボックスをオフにし、<strong>OK</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-188">To turn off Intellitrace, click <strong>Options</strong> &gt; <strong>IntelliTrace</strong> &gt; <strong>Enable IntelliTrace</strong>, clear the check box, and then click <strong>OK</strong>.</span></span> <span data-ttu-id="89d53-189">Intellitrace は Visual Studio の Enterprise 版でのみ使用できることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-189">Note that Intellitrace is only available in the Enterprise version of Visual Studio.</span></span>  

## <a name="address-code-migration-tasks"></a><span data-ttu-id="89d53-190">アドレス コード移行タスク</span><span class="sxs-lookup"><span data-stu-id="89d53-190">Address code migration tasks</span></span>
<span data-ttu-id="89d53-191">メタデータを Finance and Operations に移行するとき、複数の自動アップグレード スクリプトが実行されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-191">When metadata is migrated to Finance and Operations, multiple auto-upgrade scripts are run.</span></span> <span data-ttu-id="89d53-192">開発者が手動で移行タスクを完了する必要がある場合、行う内容とベスト プラクティス (BP) が追加されました。</span><span class="sxs-lookup"><span data-stu-id="89d53-192">In the case where developers need to complete manual migration tasks, TO DOs and Best Practices (BP) have been added.</span></span>

-   <span data-ttu-id="89d53-193">TO DO には `/* TODO: (Code Upgrade)` の接頭語が付いており、コード移行の一部として修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-193">TO DOs are prefixed with `/* TODO: (Code Upgrade)`, and need to be fixed as a part of code migration.</span></span>
-   <span data-ttu-id="89d53-194">BP 移行固有のルールはコード移行の一環として修正される必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-194">BP migration specific rules also need to be fixed as part of code migration.</span></span>

<span data-ttu-id="89d53-195">以下のこの例では、**PurchCommitment\_PSN** フォームを使用して、ナビゲーションを修正する移行タスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="89d53-195">This example below uses the **PurchCommitment\_PSN** form to walk you through the migration task of fixing navigation.</span></span> <span data-ttu-id="89d53-196">具体的には、重複するボタンおよびアクション ウィンドウ TODO などの例が表示されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-196">Specifically, you will see examples of duplicate buttons and Action Pane TODOs.</span></span>

### <a name="setup"></a><span data-ttu-id="89d53-197">セットアップ</span><span class="sxs-lookup"><span data-stu-id="89d53-197">Setup</span></span>

1.  <span data-ttu-id="89d53-198">Visual Studio で、**アプリケーション エクスプローラー** を開き、フォーム PurchCommitment\_PSN を検索します。</span><span class="sxs-lookup"><span data-stu-id="89d53-198">In Visual Studio, open **Application Explorer**, and search for the form, PurchCommitment\_PSN.</span></span>
2.  <span data-ttu-id="89d53-199">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-199">Click **OK**.</span></span>
3.  <span data-ttu-id="89d53-200">プロジェクトを右クリックし、**プロパティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89d53-200">Right-click the project and select **Properties**.</span></span>
4.  <span data-ttu-id="89d53-201">モデル プロパティで **アプリケーション スイート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89d53-201">In the Model property, select **Application Suite**.</span></span>
5.  <span data-ttu-id="89d53-202">会社プロパティで、FRSI を選択します。</span><span class="sxs-lookup"><span data-stu-id="89d53-202">In the Company property, select FRSI.</span></span>
6.  <span data-ttu-id="89d53-203">注記: このフォームは、フランスのデモ データ会社 FRSI に配置されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-203">Note: The form is located in the French demo data company FRSI.</span></span>
7.  <span data-ttu-id="89d53-204">**Ctrl+F5** キーを押してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="89d53-204">Press **Ctrl+F5 to** see the form.</span></span>

<span data-ttu-id="89d53-205">フォームは完成しているように見えますが、移行を完了するために必要なコード移行タスクがあります。</span><span class="sxs-lookup"><span data-stu-id="89d53-205">While the form looks complete, there are still code migration tasks necessary to be migration-complete.</span></span> 

<span data-ttu-id="89d53-206">[![i](./media/i1.png)](./media/i1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-206">[![i](./media/i1.png)](./media/i1.png)</span></span>

### <a name="navigation-migration-tasks"></a><span data-ttu-id="89d53-207">ナビゲーション移行タスク</span><span class="sxs-lookup"><span data-stu-id="89d53-207">Navigation migration tasks</span></span>

1.  <span data-ttu-id="89d53-208">Visual Studio で、プロジェクトをビルドし、ツール バーで **表示** &gt; **タスク一覧** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-208">In Visual Studio, build the project, and then on the toolbar, click **View** &gt; **Task List**.</span></span>
2.  <span data-ttu-id="89d53-209">**コメント** ドロップダウン リストをクリックして、TO DO: (コード アップグレード) タスクを表示します。</span><span class="sxs-lookup"><span data-stu-id="89d53-209">Click the **Comments** drop-down list to view the TO DO: (Code Upgrade) tasks.</span></span>
3.  <span data-ttu-id="89d53-210">一覧で、ActionPane TODO を検索します。</span><span class="sxs-lookup"><span data-stu-id="89d53-210">In the list, find the ActionPane TODOs.</span></span>

<span data-ttu-id="89d53-211">[![j](./media/j1.png)](./media/j1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-211">[![j](./media/j1.png)](./media/j1.png)</span></span>

### <a name="code-upgrade-rule---action-pane"></a><span data-ttu-id="89d53-212">コード アップグレード ルール - アクション ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="89d53-212">Code upgrade rule - Action Pane</span></span>

<span data-ttu-id="89d53-213">Finance and Operations では、次の主要なアクションはシステム定義ボタンとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-213">In Finance and Operations, the following core actions are provided as system-defined buttons:</span></span>

-   <span data-ttu-id="89d53-214">新規</span><span class="sxs-lookup"><span data-stu-id="89d53-214">New</span></span>
-   <span data-ttu-id="89d53-215">消去</span><span class="sxs-lookup"><span data-stu-id="89d53-215">Delete</span></span>
-   <span data-ttu-id="89d53-216">編集</span><span class="sxs-lookup"><span data-stu-id="89d53-216">Edit</span></span>
-   <span data-ttu-id="89d53-217">輸出</span><span class="sxs-lookup"><span data-stu-id="89d53-217">Export</span></span>

<span data-ttu-id="89d53-218">自動移行の一環として、アクション ペイン ルールは冗長ボタンを識別するために実行されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-218">As part of the auto-migration, the Action Pane rule is run to identify redundant buttons.</span></span> <span data-ttu-id="89d53-219">この移行の部分を完了するには、手動で行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-219">To complete this part of migration, you need to manually:</span></span>

-   <span data-ttu-id="89d53-220">コードを削除するか移動します。</span><span class="sxs-lookup"><span data-stu-id="89d53-220">Remove or move the code.</span></span>
-   <span data-ttu-id="89d53-221">アプリケーション コード内の冗長なコントロールを削除します。</span><span class="sxs-lookup"><span data-stu-id="89d53-221">Delete redundant controls in the application code.</span></span>

> [!NOTE]
> <span data-ttu-id="89d53-222">以下のセクションでは、システム定義ボタンを複製するモデル化されたボタンのコードを移行および変更する方法の例を示します。</span><span class="sxs-lookup"><span data-stu-id="89d53-222">In the section below, we will provide examples of how to migrate and modify the code on modeled buttons that replicate system-defined buttons.</span></span> <span data-ttu-id="89d53-223">ただし、実際には、この記事で行われたのと同様の変更を加える前に、シナリオに関してコードをまず評価して、それがまだ必要かどうかを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-223">However, in practice, before making changes similar to those made in this article, the code must first be evaluated with respect to the scenario to determine if it is still needed.</span></span> <span data-ttu-id="89d53-224">最初に、システム定義の削除ボタンと重複する、DeleteCmdButton に対する TODO を修正します。</span><span class="sxs-lookup"><span data-stu-id="89d53-224">First, fix the TODO for the DeleteCmdButton, which duplicates the system-defined Delete button.</span></span>

1.  <span data-ttu-id="89d53-225">Visual Studio では、次に示す TODO を検索して、TODO をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-225">In Visual Studio, find the TODO shown below, and then double-click the TODO.</span></span>

    <span data-ttu-id="89d53-226">[![k](./media/k1.png)](./media/k1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-226">[![k](./media/k1.png)](./media/k1.png)</span></span>

2.  <span data-ttu-id="89d53-227">以下に示すように、TODO とコード行を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89d53-227">Replace the TODO and the line of code as shown below.</span></span>
    -   <span data-ttu-id="89d53-228">システム定義の **削除** ボタンの状態は、firstmaster データソースの AllowDelete プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="89d53-228">The state of the system-defined **Delete** button is controlled by the AllowDelete property on the firstmaster datasource.</span></span> <span data-ttu-id="89d53-229">AllowDelete を false に設定することにより、キーボード ショートカットが使用されている場合に削除タスクは実行されません。</span><span class="sxs-lookup"><span data-stu-id="89d53-229">By setting AllowDelete to false, the delete task is kept from executing when the keyboard shortcut is used.</span></span>

        ```xpp
        // Delete button
        /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving all references to the form task override method and remove the control: DeleteCmdButton */
        deleteCmdButton.enabled(purchCommitmentHeader && purchCommitmentHeader.canDelete());
        PurchCommitmentHeader_DS.allowDelete(purchCommitmentHeader && purchCommitmentHeader.canDelete());
        ```

3.  <span data-ttu-id="89d53-230">エディターで、DeleteCmdButton を探してフォーム デザインから削除します。</span><span class="sxs-lookup"><span data-stu-id="89d53-230">In the editor, find and remove DeleteCmdButton from the form design.</span></span> 

    <span data-ttu-id="89d53-231">[![l](./media/l1.png)](./media/l1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-231">[![l](./media/l1.png)](./media/l1.png)</span></span>

4.  <span data-ttu-id="89d53-232">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="89d53-232">Press **Ctrl+S** to save the form.</span></span>
    -   <span data-ttu-id="89d53-233">次に、システム編集ボタンと重複する EditCmdButton に焦点を当てて、このボタンに関連付けられた 2 つの "仕事" の処理とこのボタンの削除を行います。</span><span class="sxs-lookup"><span data-stu-id="89d53-233">Next, we will focus on the EditCmdButton that duplicates the system Edit button, handing the two TODOs associated with this button as well as removing this button.</span></span>

5.  <span data-ttu-id="89d53-234">Visual Studio では、次に示す TODO を検索して、TODO をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-234">In Visual Studio, find the TODO shown below, and then double-click the TODO.</span></span>

    <span data-ttu-id="89d53-235">[![m](./media/m1.png)](./media/m1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-235">[![m](./media/m1.png)](./media/m1.png)</span></span>

6.  <span data-ttu-id="89d53-236">**編集** ボタンの表示はフォームの表示/編集モードで制御されるため、このコードを変更してプロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-236">Because the visibility of the **Edit** button is controlled by the View/Edit mode of the form, you will need to modify this code so it sets that property.</span></span> <span data-ttu-id="89d53-237">次の図に示すように、TODO とコード行を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="89d53-237">Replace the TODO and the line of code as shown in the following graphic.</span></span>

    ```xpp
    /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving all references to the form task override method and remove the control: EditCmdButton */
    editCmdButton.enabled(purchCommitmentHeader && isInDraftOrUnderRevisionStatus && !isInWorkFlowReviewState && !isLineReferenced);

    if(purchCommitmentHeader && isInDraftOrUnderRevisionStatus && !isInWorkFlowReviewState && !isLineReferenced)
    {
        element.design().ViewEditMode(ViewEditMode::Auto);
    }
    else
    {
        element.design().ViewEditMode(ViewEditMode::View);

    }
    ```

7.  <span data-ttu-id="89d53-238">このボタンのその他の TODO をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="89d53-238">Double-click the other TODO for this button.</span></span>

    <span data-ttu-id="89d53-239">[![n](./media/n1.png)](./media/n1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-239">[![n](./media/n1.png)](./media/n1.png)</span></span>

8.  <span data-ttu-id="89d53-240">モデル化された **編集** ボタンでコードを検査します。</span><span class="sxs-lookup"><span data-stu-id="89d53-240">Inspect the code on the modeled **Edit** button.</span></span> <span data-ttu-id="89d53-241">このロジックは、フォームの task() メソッドに移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="89d53-241">This logic will need to be moved to the form’s task() method.</span></span>

    ```xpp
    [Control("CommandButton")]
    class EditCmdButton
    {
        /* TODO: (Code Upgrade) [Action Pane Rule] Please consider moving this button code to the task override method and remove the control EditCmdButton. */
        void clicked()
        {
            if (purchCommitmentHeader.WorkflowApprovalState ==     
                PurchCommitmentWorkflowApprovalState_PSN::Approved)
            {
                if (Box::yesNo(strFmt("@SPS2140", purchCommitmentHeader.CommitmentNumber), 
                    DialogButton::No) == DialogButton::Yes)
                {
                    super();

                    PurchCommitmentHeader_PSN::setWorkflowState(purchCommitmentHeader.RecId, 
                        PurchCommitmentWorkflowApprovalState_PSN::NotSubmitted);
                }
            }
            else
            {
                super();
            }
        }
    }
    ```

9.  <span data-ttu-id="89d53-242">Visual Studio デザイナーの左側で、**メソッド** &gt; **上書き** を右クリックし、**タスク** を選択して、フォームのタスク メソッドの上書きを追加します。</span><span class="sxs-lookup"><span data-stu-id="89d53-242">On the left side of the Visual Studio designer, right-click **Methods** &gt; **Override**, and select **Task**, to add an override for the form’s Task method.</span></span>
10. <span data-ttu-id="89d53-243">システム定義の **編集** ボタンをクリックしたときに上記のコードがトリガーされるように、以下に示すようにタスク メソッドを更新します。</span><span class="sxs-lookup"><span data-stu-id="89d53-243">Update the task method as shown below so that the code from above is triggered when the system-defined **Edit** button is clicked.</span></span>

    ```xpp
    /// 
        ///
        /// 
        /// 
        /// 
        public int task(int _taskId)
        {
            #Task
            int ret;

            switch (_taskId)
            {
                case #taskEditRecord:

                    if (purchCommitmentHeader.WorkflowApprovalState == PurchCommitmentWorkflowApprovalState_PSN::Approved)
                    {
                        if (Box::yesNo(strFmt("@SPS2140", purchCommitmentHeader.CommitmentNumber), DialogButton::No) == DialogButton::Yes)
                        {
                            ret = super(_taskId);

                            PurchCommitmentHeader_PSN::setWorkflowState(purchCommitmentHeader.RecId, PurchCommitmentWorkflowApprovalState_PSN::NotSubmitted);
                        }
                    }
                    else
                    {
                        ret = super(_taskId);
                    }

                    break;

                default:
                    ret = super(_taskId);
                    break;
            }

            return ret;
        }
    ```

11. <span data-ttu-id="89d53-244">エディターで、**EditCmdButton** を探してフォーム デザインから削除します。</span><span class="sxs-lookup"><span data-stu-id="89d53-244">In the Editor, find and remove the **EditCmdButton** from the form design.</span></span> 

    <span data-ttu-id="89d53-245">[![o](./media/o1.png)](./media/o1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-245">[![o](./media/o1.png)](./media/o1.png)</span></span>

12. <span data-ttu-id="89d53-246">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="89d53-246">Press **Ctrl+S** to save the form.</span></span>
13. <span data-ttu-id="89d53-247">**Ctrl+F5** キーを押してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="89d53-247">Press **Ctrl+F5** to view the form.</span></span> <span data-ttu-id="89d53-248">**確約** タブの **削除** および **編集** ボタンが削除されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="89d53-248">Notice the **Delete** and **Edit** buttons in the **Commitment** tab have been removed.</span></span>

## <a name="resolve-casting-exceptions"></a><span data-ttu-id="89d53-249">キャスト例外を解決</span><span class="sxs-lookup"><span data-stu-id="89d53-249">Resolve casting exceptions</span></span>
<span data-ttu-id="89d53-250">Finance and Operations では、X++ は完全に中間言語 (IL) ベースであるため、解釈された Dynamics AX 2012 よりも厳密なランタイム タイプ動作を行います。</span><span class="sxs-lookup"><span data-stu-id="89d53-250">In Finance and Operations, X++ is completely intermediate-language (IL) based and therefore has a stricter runtime type behavior than the interpreted Dynamics AX2 012.</span></span> <span data-ttu-id="89d53-251">この厳しいランタイム タイプの動作により、移行された Dynamics AX 2012 R3 メタデータの例外を生成できます。</span><span class="sxs-lookup"><span data-stu-id="89d53-251">This stricter runtime type behavior can generate exceptions in migrated Dynamics AX 2012 R3 metadata.</span></span> <span data-ttu-id="89d53-252">移行中にこれらの例外が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="89d53-252">It is likely you will encounter these exceptions during your migration.</span></span> <span data-ttu-id="89d53-253">キャスト例外は、ダウンキャスト、タイム オブジェクトを設計するためのキャスト ランタイム、サイド キャストなど、さまざまな実行時シナリオで発生させることができます。</span><span class="sxs-lookup"><span data-stu-id="89d53-253">The casting exceptions can be raised in different runtime scenarios, such as down-casting, casting runtime to design time objects, and side-casting.</span></span> <span data-ttu-id="89d53-254">以下のセクションで、フォーム CosJournalName が実行時にコントロールを生成し、強い型付けのために .NET 例外を発生させる型の不一致がある例について説明します。</span><span class="sxs-lookup"><span data-stu-id="89d53-254">In the section below, we will walk through an example where a form, CosJournalName, is generating controls at runtime, and has a type mismatch which causes a .NET exception because it is strongly typed.</span></span>

### <a name="example-side-casting-exception"></a><span data-ttu-id="89d53-255">例: サイドキャストの例外</span><span class="sxs-lookup"><span data-stu-id="89d53-255">Example: Side-casting exception</span></span>

1.  <span data-ttu-id="89d53-256">Visual Studio で、**プロジェクト プロパティ** を選択して右クリックし、USMF が既定の会社であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="89d53-256">In Visual Studio, select and right-click **Project Properties**, and verify that USMF is the default company.</span></span>
2.  <span data-ttu-id="89d53-257">表示メニュー項目に CosJournalName を追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。</span><span class="sxs-lookup"><span data-stu-id="89d53-257">Add the display menu item CosJournalName to your project, and set the menu item as your Startup object.</span></span>
3.  <span data-ttu-id="89d53-258">プロジェクトに CosJournalName フォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="89d53-258">Add the CosJournalName form to your project.</span></span>
4.  <span data-ttu-id="89d53-259">プロジェクトに cosDimCheckBoxController クラスを追加します。</span><span class="sxs-lookup"><span data-stu-id="89d53-259">Add the cosDimCheckBoxController class to your project.</span></span>
5.  <span data-ttu-id="89d53-260">プロジェクトのリビルドします。</span><span class="sxs-lookup"><span data-stu-id="89d53-260">Rebuild your project.</span></span>
6.  <span data-ttu-id="89d53-261">**Ctrl+F5** キーを押してフォームを実行します。</span><span class="sxs-lookup"><span data-stu-id="89d53-261">Press **Ctrl+F5** to run the form.</span></span>
7.  <span data-ttu-id="89d53-262">フォームを実行するときに、次のような例外が発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-262">Note that you will get an exception, similar to the following, when running the form.</span></span>

    <span data-ttu-id="89d53-263">[![u](./media/u1.png)](./media/u1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-263">[![u](./media/u1.png)](./media/u1.png)</span></span>

8.  <span data-ttu-id="89d53-264">cosDimCheckBoxController クラスを右クリックし、**コードの表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="89d53-264">Right-click the class, cosDimCheckBoxController, and then select **View Code**.</span></span>
9.  <span data-ttu-id="89d53-265">cosDimCheckBoxController::getBuildControl() にブレークポイントを設定します。</span><span class="sxs-lookup"><span data-stu-id="89d53-265">Set a breakpoint on the cosDimCheckBoxController::getBuildControl().</span></span>
10. <span data-ttu-id="89d53-266">**F5** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="89d53-266">Press **F5**.</span></span>
    -   <span data-ttu-id="89d53-267">ブレークポイントをヒットします。</span><span class="sxs-lookup"><span data-stu-id="89d53-267">The breakpoint will be hit.</span></span> <span data-ttu-id="89d53-268">これがキャスティング エラーが発生する場所です。</span><span class="sxs-lookup"><span data-stu-id="89d53-268">This is where the casting error occurs.</span></span> <span data-ttu-id="89d53-269">キャスト エラーの理由は、型のコントロールを返そうとしているためです。FormBuildCheckboxControl とオブジェクトは FormBuildStringControl を想定しています。</span><span class="sxs-lookup"><span data-stu-id="89d53-269">The reason for the casting error is because we are trying to return a control of type: FormBuildCheckboxControl and the object is expecting FormBuildStringControl.</span></span>

11. <span data-ttu-id="89d53-270">buildcontrol をポイントしてタイプを表示し、相違点に注目します。</span><span class="sxs-lookup"><span data-stu-id="89d53-270">Hover over the buildcontrol to see the type and notice the differences.</span></span>

    <span data-ttu-id="89d53-271">[![v](./media/v1.png)](./media/v1.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-271">[![v](./media/v1.png)](./media/v1.png)</span></span>

12. <span data-ttu-id="89d53-272">**F10** キーを押して例外をヒットします。</span><span class="sxs-lookup"><span data-stu-id="89d53-272">Press **F10** to hit the exception.</span></span>

    <span data-ttu-id="89d53-273">[![w](./media/w2.png)](./media/w2.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-273">[![w](./media/w2.png)](./media/w2.png)</span></span>

13. <span data-ttu-id="89d53-274">デバッグを停止します。</span><span class="sxs-lookup"><span data-stu-id="89d53-274">Stop debugging.</span></span>
14. <span data-ttu-id="89d53-275">例外を修正するには、メソッド宣言を FormBuildStringControl から FormBuildCheckBoxControl に変更します。</span><span class="sxs-lookup"><span data-stu-id="89d53-275">To fix the exception, change the method declaration from FormBuildStringControl to FormBuildCheckBoxControl.</span></span>

    ```xpp
    protected FormBuildStringControl getBuildControl()
    protected FormBuildCheckBoxControl getBuildControl()
    ```
    
15. <span data-ttu-id="89d53-276">プロジェクトをリビルドして、**Ctrl+F5** を押します。</span><span class="sxs-lookup"><span data-stu-id="89d53-276">Rebuild the project, and press **Ctrl+F5**.</span></span> <span data-ttu-id="89d53-277">キャスト エラーが解決されたため、フォームが正常に開きます。</span><span class="sxs-lookup"><span data-stu-id="89d53-277">The form should open successfully because the casting error is resolved.</span></span>

    <span data-ttu-id="89d53-278">[![a](./media/a-1024x576.png)](./media/a.png)</span><span class="sxs-lookup"><span data-stu-id="89d53-278">[![a](./media/a-1024x576.png)](./media/a.png)</span></span>

## <a name="migrating-context-menus-and-mouse-double-click-code"></a><span data-ttu-id="89d53-279">コンテキスト メニューとマウス ダブルクリック コードの移行</span><span class="sxs-lookup"><span data-stu-id="89d53-279">Migrating context menus and mouse double-click code</span></span>
<span data-ttu-id="89d53-280">コンテキスト メニューとマウスのダブルクリック アクションを処理する Dynamics AX 2012 コードを移行するには、このトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="89d53-280">Refer to these topics to migrate code Dynamics AX 2012 that deals with context menus and mouse double-click actions.</span></span>

-   [<span data-ttu-id="89d53-281">コードの移行 - コンテキスト メニュー コード</span><span class="sxs-lookup"><span data-stu-id="89d53-281">Code migration - Context menu code</span></span>](code-migration-context-menus.md)
-   [<span data-ttu-id="89d53-282">コードの移行 - マウス ダブルクリック ロジック</span><span class="sxs-lookup"><span data-stu-id="89d53-282">Code migration - Mouse double-click logic</span></span>](code-migration-double-click.md)




