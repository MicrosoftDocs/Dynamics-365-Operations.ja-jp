---
title: 分割されたモデル
description: このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。
author: maertenm
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26941
ms.assetid: feaa09c5-efc7-4594-921e-b42536b18852
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83d394d6cd4b7af6c9fdc60693ba0d88035c4c89
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191662"
---
# <a name="model-split"></a><span data-ttu-id="9801c-103">分割されたモデル</span><span class="sxs-lookup"><span data-stu-id="9801c-103">Model split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9801c-104">このトピックでは、スタックの 3 つの主要モデル、つまりアプリケーション プラットフォーム、アプリケーション基盤、アプリケーション スイートへの分割について説明します。</span><span class="sxs-lookup"><span data-stu-id="9801c-104">This topic explains the split of the stack into three main models -  the Application Platform, the Application Foundation, and the Application Suite.</span></span>

## <a name="overview"></a><span data-ttu-id="9801c-105">概要</span><span class="sxs-lookup"><span data-stu-id="9801c-105">Overview</span></span>

<span data-ttu-id="9801c-106">モジュール コードを開発することは、モデル分割の原動力です。</span><span class="sxs-lookup"><span data-stu-id="9801c-106">Developing modular code is the driving force behind the model split.</span></span> <span data-ttu-id="9801c-107">複数のモデルにスタックを分割すると、コンパイル時間の短縮、実稼動環境でのパートナー IP の適切な区別など、多くの利点が提供されます。</span><span class="sxs-lookup"><span data-stu-id="9801c-107">Splitting the stack into multiple models provides many benefits, including faster compile time and a greater distinction between partner's IP in production.</span></span> <span data-ttu-id="9801c-108">メイン モデルは、**アプリケーション プラットフォーム**、**アプリケーション基盤**、**アプリケーション スイート**の 3 つがあります。</span><span class="sxs-lookup"><span data-stu-id="9801c-108">There are three main models: the **Application Platform**, the **Application Foundation**, and the **Application Suite**.</span></span> 

<span data-ttu-id="9801c-109">[![First\_ModelSplit](./media/first_modelsplit.png)](./media/first_modelsplit.png)</span><span class="sxs-lookup"><span data-stu-id="9801c-109">[![First\_ModelSplit](./media/first_modelsplit.png)](./media/first_modelsplit.png)</span></span> 

<span data-ttu-id="9801c-110"><strong>アプリケーション プラットフォーム</strong>は最下位モデルであり、カーネルとやり取りする最下位レベルの要素が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9801c-110">The <strong>Application Platform</strong> is the lowest model and contains the lowest level elements that interface with the kernel.</span></span> <span data-ttu-id="9801c-111"><strong>Application Object Server **(</strong>AOS<strong>) は、**アプリケーション プラットフォーム</strong>を使用してのみ起動できます。</span><span class="sxs-lookup"><span data-stu-id="9801c-111">The <strong>Application Object Server \*\*(</strong>AOS<strong>) can be started with only the \*\*Application Platform</strong>.</span></span> <span data-ttu-id="9801c-112"><strong>アプリケーション基盤</strong>は、<strong>アプリケーション プラットフォーム</strong>の一番上に配置され、すべてのアプリケーションによって共有されるフレームワーク機能を含みます。</span><span class="sxs-lookup"><span data-stu-id="9801c-112">The <strong>Application Foundation</strong> sits atop the <strong>Application Platform</strong> and contains framework functionalities that are shared by all applications.</span></span> <span data-ttu-id="9801c-113">最後に、<strong>アプリケーション スイート</strong>は<strong>アプリケーション基準</strong>の上部に位置し、アプリケーションの特定要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="9801c-113">Finally, the <strong>Application Suite</strong> sits atop the <strong>Application Foundation</strong> and contains application specific elements.</span></span> <span data-ttu-id="9801c-114">付録のモデル内訳表は、これらの各モデルのコンポーネントの例を示します。</span><span class="sxs-lookup"><span data-stu-id="9801c-114">The Model Breakdown table in the appendix provides examples of components in each of these models.</span></span> <span data-ttu-id="9801c-115">各モデルは、独自のアセンブリにコンパイルされ、下位レイヤー モデル アセンブリに依存します。</span><span class="sxs-lookup"><span data-stu-id="9801c-115">Each model is compiled into its own assembly with dependencies on lower layer model assemblies.</span></span> <span data-ttu-id="9801c-116"><strong>アプリケーション プラットフォーム</strong>は、他のモデルには依存しません。</span><span class="sxs-lookup"><span data-stu-id="9801c-116">The <strong>Application Platform</strong> does not depend on any other models.</span></span> <span data-ttu-id="9801c-117">これは、モデルをアセンブリに直接マッピングすることを意味します。</span><span class="sxs-lookup"><span data-stu-id="9801c-117">This implies a direct mapping of the model to an assembly.</span></span> 

<span data-ttu-id="9801c-118">[![ModelAssembly\_ModelSplit](./media/modelassembly_modelsplit1.jpg)](./media/modelassembly_modelsplit1.jpg)</span><span class="sxs-lookup"><span data-stu-id="9801c-118">[![ModelAssembly\_ModelSplit](./media/modelassembly_modelsplit1.jpg)](./media/modelassembly_modelsplit1.jpg)</span></span> 

<span data-ttu-id="9801c-119">モジュール スタックで開発することで、**アプリケーション スイート**で変更を行い、残りのスタックに触れることなくコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="9801c-119">Developing in the modular stack allows changes to be made in the **Application Suite** and compiled without touching the rest of the stack.</span></span> <span data-ttu-id="9801c-120">新しい変更のあるモデルのみコンパイルされる必要があり、コンパイルの時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="9801c-120">Only models with new changes need to be compiled, greatly reducing compile time.</span></span> <span data-ttu-id="9801c-121">詳細については、この記事の終わりにある「モデルの内訳」セクションで確認できます。</span><span class="sxs-lookup"><span data-stu-id="9801c-121">More information can be found in the "Model Breakdown" section at the end of this article.</span></span>

## <a name="customizing-models"></a><span data-ttu-id="9801c-122">モデルのカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="9801c-122">Customizing models</span></span>
<span data-ttu-id="9801c-123">カスタマイズの方法には、オーバーレイと拡張の 2 種類があります。</span><span class="sxs-lookup"><span data-stu-id="9801c-123">There are two methods for customizing: overlayering and extensions.</span></span> <span data-ttu-id="9801c-124">オーバーレイヤーにより、下位レベルでモデル内の要素を変更、つまりオーバーレイする複数のレイヤーに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="9801c-124">Overlayering allows for changes to be made at multiple layers that alter, or overlay, elements in models at lower levels.</span></span> <span data-ttu-id="9801c-125">拡張子を使用すると、要素のイベントやプラグイン ポイントに新しい要素を追加したり、コードをアタッチすることができます。</span><span class="sxs-lookup"><span data-stu-id="9801c-125">Extensions allow for new elements to be added or code to be attached to element events or plug-in points.</span></span> <span data-ttu-id="9801c-126">使用されるカスタマイズのタイプは、モデルがどのようにコンパイルされ、最終的にパッケージ化されるかに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="9801c-126">The type of customization used impacts how a model will be compiled and ultimately packaged.</span></span> <span data-ttu-id="9801c-127">1 つ以上のモデルが、アセンブリにコンパイルされます。</span><span class="sxs-lookup"><span data-stu-id="9801c-127">One or more models are compiled into an assembly.</span></span> <span data-ttu-id="9801c-128">アセンブリ、非コード メタデータ、およびそれをコンパイルされたコンポーネントはパッケージを形成します。</span><span class="sxs-lookup"><span data-stu-id="9801c-128">An assembly, its non-code metadata, and its compiled artifacts, form a package.</span></span> <span data-ttu-id="9801c-129">パッケージは、独立した配置可能な単位です。</span><span class="sxs-lookup"><span data-stu-id="9801c-129">A package is an independent deployable unit.</span></span> <span data-ttu-id="9801c-130">拡張機能のカスタマイズのみが含まれるモデルは、独自のアセンブリにコンパイルして独自のパッケージに配置できます。</span><span class="sxs-lookup"><span data-stu-id="9801c-130">A model that contains only extension customizations can be compiled into its own assembly and be deployed in its own package.</span></span> <span data-ttu-id="9801c-131">任意のオーバーレイが含まれるモデルは、オーバーレイ モデルに基づいてアセンブリにコンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9801c-131">A model that contains any overlayering must be compiled into the assembly based on the overlayed model.</span></span> 

<span data-ttu-id="9801c-132">[![カスタマイズ アセンブリ](./media/customization-assemblies.png)](./media/customization-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="9801c-132">[![Customization Assemblies](./media/customization-assemblies.png)](./media/customization-assemblies.png)</span></span>   

<span data-ttu-id="9801c-133">拡張機能の使用には、以下を含むいくつかの利点があります。</span><span class="sxs-lookup"><span data-stu-id="9801c-133">Using extensions has several advantages, including:</span></span>

-   <span data-ttu-id="9801c-134">アプリケーション ライフ サイクル管理の目的で、拡張コンポーネントのみを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9801c-134">For application lifecycle management purposes, you need to manage only your extension artifacts.</span></span>
-   <span data-ttu-id="9801c-135">カスタマイズの構築ではアプリケーション全体を再コンパイルする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="9801c-135">Building a customization does not require you to recompile the entire application.</span></span>
-   <span data-ttu-id="9801c-136">クラウドで Microsoft はユーザーのカスタマイズに影響を与えずに、インストール、パッチ、アップグレード、および内部 API の変更を行えます。</span><span class="sxs-lookup"><span data-stu-id="9801c-136">In the cloud, Microsoft can install, patch, upgrade, and change internal APIs without affecting your customizations.</span></span>
-   <span data-ttu-id="9801c-137">他のカスタマイズを意識せずに、ソリューションを別々に処理することができます。</span><span class="sxs-lookup"><span data-stu-id="9801c-137">You can service your solutions independently without concerns about other customizations.</span></span>

<span data-ttu-id="9801c-138">現在、コード拡張、テーブル拡張、フォーム拡張、メニュー拡張、列挙拡張がサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9801c-138">There are currently support code extensions, table extensions, form extensions, menu extensions, and enum extensions.</span></span> <span data-ttu-id="9801c-139">[拡張機能およびオーバーレイによってカスタマイズする](../extensibility/customization-overlayering-extensions.md)と[拡張機能を使用してモデル要素をカスタマイズする](../extensibility/customize-model-elements-extensions.md) の「拡張機能」セクションでは、拡張機能の使い方について詳しく説明されています。</span><span class="sxs-lookup"><span data-stu-id="9801c-139">The Extensions section in [Customize with extensions and overlayering](../extensibility/customization-overlayering-extensions.md) and [Customize model elements using extensions](../extensibility/customize-model-elements-extensions.md) provide a more detailed explanation on how to use extensions.</span></span>  <span data-ttu-id="9801c-140">拡張子は、可能な限りサポートされている要素で使用する必要があり、既存の Microsoft コードを変更する必要がない場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="9801c-140">Extensions should be used on supported elements wherever possible and are best applied when no change to existing Microsoft code is needed.</span></span> <span data-ttu-id="9801c-141">メソッドの機能をマスクするための変更には、コード自体を変更するためのオーバーレイが必要です。</span><span class="sxs-lookup"><span data-stu-id="9801c-141">A change to mask a method’s functionality requires overlayering to change the code itself.</span></span>  <span data-ttu-id="9801c-142">オーバーレイヤーは、カスタマイズが基本機能をカスタマイズする場合に、拡張機能がカバーしない領域に存在する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9801c-142">Overlayering should be in areas not covered by extensions and when the customization alters the base functionality.</span></span> <span data-ttu-id="9801c-143">次の図は、2 つのカスタマイズ戦略の違いをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="9801c-143">The illustration below summarizes differences between the two customization strategies.</span></span> 

<span data-ttu-id="9801c-144">[![カスタマイズの概要](./media/customization-overview.png)](./media/customization-overview.png)</span><span class="sxs-lookup"><span data-stu-id="9801c-144">[![Customization Overview](./media/customization-overview.png)](./media/customization-overview.png)</span></span>

## <a name="model-breakdown"></a><span data-ttu-id="9801c-145">モデルの内訳</span><span class="sxs-lookup"><span data-stu-id="9801c-145">Model breakdown</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9801c-146"><strong>モデル</strong></span><span class="sxs-lookup"><span data-stu-id="9801c-146"><strong>Model</strong></span></span></td>
<td><span data-ttu-id="9801c-147"><strong>概念</strong></span><span class="sxs-lookup"><span data-stu-id="9801c-147"><strong>Concept</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9801c-148">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="9801c-148">Application Platform</span></span></td>
<td><span data-ttu-id="9801c-149">アプリケーション ロジックに対応するカーネル機能へのアプリケーション プラットフォーム インターフェイス。</span><span class="sxs-lookup"><span data-stu-id="9801c-149">The Application Platform interfaces to kernel functionalities that are application logic agnostic.</span></span> <span data-ttu-id="9801c-150">AOS は、このモデルだけで開始することができます。</span><span class="sxs-lookup"><span data-stu-id="9801c-150">The AOS can be started with just this model.</span></span>
<ul>
<li><span data-ttu-id="9801c-151">AIF 基準オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9801c-151">AIF base objects</span></span></li>
<li><span data-ttu-id="9801c-152">バッチ</span><span class="sxs-lookup"><span data-stu-id="9801c-152">Batch</span></span></li>
<li><span data-ttu-id="9801c-153">フォーム基本対象</span><span class="sxs-lookup"><span data-stu-id="9801c-153">Form base objects</span></span></li>
<li><span data-ttu-id="9801c-154">RunbaseSysOperations\* ベース オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9801c-154">RunbaseSysOperations\* base objects</span></span></li>
<li><span data-ttu-id="9801c-155">DictXX オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9801c-155">DictXX objects</span></span></li>
<li><span data-ttu-id="9801c-156">Appl、情報、グローバル、ClassFactory</span><span class="sxs-lookup"><span data-stu-id="9801c-156">Appl, Info, Global, ClassFactory</span></span></li>
<li><span data-ttu-id="9801c-157">データ アクセス オブジェクト</span><span class="sxs-lookup"><span data-stu-id="9801c-157">Data access objects</span></span></li>
<li><span data-ttu-id="9801c-158">ヘルパー クラス</span><span class="sxs-lookup"><span data-stu-id="9801c-158">Helper Classes</span></span></li>
<li><span data-ttu-id="9801c-159">ENUM/EDT/Macros/ConfigKey/LicenseCode</span><span class="sxs-lookup"><span data-stu-id="9801c-159">ENUM/EDT/Macros/ConfigKey/LicenseCode</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9801c-160">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="9801c-160">Application Foundation</span></span></td>
<td><ul>
<li><span data-ttu-id="9801c-161">アプリケーション基準機能:</span><span class="sxs-lookup"><span data-stu-id="9801c-161">Application foundation features:</span></span>
<ul>
<li><span data-ttu-id="9801c-162">フレームワーク分析コード</span><span class="sxs-lookup"><span data-stu-id="9801c-162">Dimension framework</span></span></li>
<li><span data-ttu-id="9801c-163">グローバル アドレス帳</span><span class="sxs-lookup"><span data-stu-id="9801c-163">Global Address Book</span></span></li>
<li><span data-ttu-id="9801c-164">番号順序</span><span class="sxs-lookup"><span data-stu-id="9801c-164">Number Sequence</span></span></li>
<li><span data-ttu-id="9801c-165">OrgModel</span><span class="sxs-lookup"><span data-stu-id="9801c-165">OrgModel</span></span></li>
</ul></li>
<li><span data-ttu-id="9801c-166">機能領域:</span><span class="sxs-lookup"><span data-stu-id="9801c-166">Feature areas:</span></span>
<ul>
<li><span data-ttu-id="9801c-167">ビジネス インテリジェンス</span><span class="sxs-lookup"><span data-stu-id="9801c-167">Business Intelligence</span></span></li>
<li><span data-ttu-id="9801c-168">レポート</span><span class="sxs-lookup"><span data-stu-id="9801c-168">Reports</span></span></li>
<li><span data-ttu-id="9801c-169">アップグレード フレームワーク</span><span class="sxs-lookup"><span data-stu-id="9801c-169">Upgrade framework</span></span></li>
<li><span data-ttu-id="9801c-170">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="9801c-170">Security</span></span></li>
<li><span data-ttu-id="9801c-171">電子署名</span><span class="sxs-lookup"><span data-stu-id="9801c-171">E-Signature</span></span></li>
<li><span data-ttu-id="9801c-172">データのインスポート/エクスポート</span><span class="sxs-lookup"><span data-stu-id="9801c-172">Data Import/Export</span></span></li>
<li><span data-ttu-id="9801c-173">ワークフロー</span><span class="sxs-lookup"><span data-stu-id="9801c-173">Workflow</span></span></li>
</ul></li>
<li><span data-ttu-id="9801c-174">SYS オブジェクト:</span><span class="sxs-lookup"><span data-stu-id="9801c-174">SYS objects:</span></span>
<ul>
<li><span data-ttu-id="9801c-175">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="9801c-175">Best Practices</span></span></li>
<li><span data-ttu-id="9801c-176">チェックリスト</span><span class="sxs-lookup"><span data-stu-id="9801c-176">CheckList</span></span></li>
<li><span data-ttu-id="9801c-177">保険証書</span><span class="sxs-lookup"><span data-stu-id="9801c-177">Policy</span></span></li>
<li><span data-ttu-id="9801c-178">RecordTemplate</span><span class="sxs-lookup"><span data-stu-id="9801c-178">RecordTemplate</span></span></li>
</ul></li>
<li><span data-ttu-id="9801c-179">その他:</span><span class="sxs-lookup"><span data-stu-id="9801c-179">Miscellaneous:</span></span>
<ul>
<li><span data-ttu-id="9801c-180">通貨</span><span class="sxs-lookup"><span data-stu-id="9801c-180">Currency</span></span></li>
<li><span data-ttu-id="9801c-181">測定単位</span><span class="sxs-lookup"><span data-stu-id="9801c-181">Unit of Measure</span></span></li>
</ul></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9801c-182">Application Suite</span><span class="sxs-lookup"><span data-stu-id="9801c-182">Application Suite</span></span></td>
<td><ul>
<li><span data-ttu-id="9801c-183">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="9801c-183">Supply Chain Management</span></span></li>
<li><span data-ttu-id="9801c-184">人材管理</span><span class="sxs-lookup"><span data-stu-id="9801c-184">Human Capital Management</span></span></li>
<li><span data-ttu-id="9801c-185">プロフェッショナル サービスなど</span><span class="sxs-lookup"><span data-stu-id="9801c-185">Professional Services, etc.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>




