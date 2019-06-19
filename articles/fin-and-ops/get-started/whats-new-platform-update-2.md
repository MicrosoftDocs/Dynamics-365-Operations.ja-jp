---
title: Dynamics AX プラットフォーム更新プログラム 2 (2016 年 8 月) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics AX プラットフォーム更新プログラム 2 の新機能または変更された機能について説明します。 このバージョンは 2016 年 8 月にリリースされ、ビルド番号は 7.0.4230.16130 です。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 140993
ms.assetid: 7ab12871-d7b9-4bf8-9bde-1ab372db421a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: f2d217c5c1fac6fa5f4d425925d534cb6e77f275
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547993"
---
# <a name="whats-new-or-changed-in-dynamics-ax-platform-update-2-august-2016"></a><span data-ttu-id="83c15-104">Dynamics AX プラットフォーム更新プログラム 2 (2016 年 8 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="83c15-104">What's new or changed in Dynamics AX platform update 2 (August 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83c15-105">このトピックでは、Microsoft Dynamics AX プラットフォーム更新プログラム 2 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="83c15-105">This topic describes features that are either new or changed in Microsoft Dynamics AX platform update 2.</span></span> <span data-ttu-id="83c15-106">このバージョンは 2016 年 8 月にリリースされ、ビルド番号は 7.0.4230.16130 です。</span><span class="sxs-lookup"><span data-stu-id="83c15-106">This version was released in August 2016 and has a build number of 7.0.4230.16130.</span></span>

## <a name="deployment"></a><span data-ttu-id="83c15-107">配置</span><span class="sxs-lookup"><span data-stu-id="83c15-107">Deployment</span></span>

| <span data-ttu-id="83c15-108">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-108">What can you do?</span></span> | <span data-ttu-id="83c15-109">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-110">Dynamics AX の Azure Resource Manager (ARM) 配置を有効にします。</span><span class="sxs-lookup"><span data-stu-id="83c15-110">Enable Azure Resource Manager (ARM) deployments of Dynamics AX.</span></span> | <span data-ttu-id="83c15-111">この機能はパブリック プレビューになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-111">This feature is now in public preview.</span></span> <span data-ttu-id="83c15-112">ARM 展開を使用して、Azure の最新機能を利用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-112">With ARM deployments, you can now take advantage of the latest features of Azure.</span></span> <span data-ttu-id="83c15-113">詳細については、[Azure リソース マネージャーの研修](../../dev-itpro/deployment/arm-onboarding.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83c15-113">For more information, see [Azure Resource Manager onboarding](../../dev-itpro/deployment/arm-onboarding.md).</span></span> |

## <a name="development-and-customization"></a><span data-ttu-id="83c15-114">開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="83c15-114">Development and customization</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="83c15-115">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-115">What can you do?</span></span></th>
<th><span data-ttu-id="83c15-116">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-116">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83c15-117">アプリケーションをアップグレードせずに、Microsoft Dynamics AX プラットフォームを新しいリリースにアップグレードします。</span><span class="sxs-lookup"><span data-stu-id="83c15-117">Upgrade the Microsoft Dynamics AX platform to a new release without upgrading your application.</span></span></td>
<td><span data-ttu-id="83c15-118">Microsoft Dynamics AX プラットフォームは、Microsoft Dynamics AX 7.0 (2016 年 2 月) バージョン以降、Dynamics AX アプリケーションの以前のバージョンと互換性が確保されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-118">The Microsoft Dynamics AX platform is now compatible with previous versions of the Dynamics AX application, starting with the Microsoft Dynamics AX 7.0 (February 2016) version.</span></span> <span data-ttu-id="83c15-119">したがって、アプリケーション全体をアップグレードしなくても、プラットフォームの最新の機能を最新の状態に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-119">Therefore, you can stay up to date with the latest improvements to the platform without having to upgrade your whole application.</span></span> <span data-ttu-id="83c15-120">この機能はプレビュー モードであり、プラットフォーム モデルをオーバーレイしないユーザーが利用できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-120">This feature is in preview mode and is available to those who don't overlay the platform models.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83c15-121">コードおよびメタデータ (追加のサポート) を拡張します。</span><span class="sxs-lookup"><span data-stu-id="83c15-121">Extend your code and metadata (additional support).</span></span></td>
<td><span data-ttu-id="83c15-122">追加の拡張機能を使用して、標準の Microsoft モデルのカスタマイズ (オーバーレイ) を減らすことができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-122">Additional extensibility features let you do less customization (over-layering) of the standard Microsoft models.</span></span>
<ul>
<li><span data-ttu-id="83c15-123">ビューを拡張します。</span><span class="sxs-lookup"><span data-stu-id="83c15-123">Extend a view.</span></span></li>
<li><span data-ttu-id="83c15-124">テーブル拡張機能に新しいマップを追加します。</span><span class="sxs-lookup"><span data-stu-id="83c15-124">Add a new mapping to a table extension.</span></span></li>
<li><span data-ttu-id="83c15-125">コードビハインド拡張子フォームを有効にします。</span><span class="sxs-lookup"><span data-stu-id="83c15-125">Enable code-behind extension forms.</span></span> <span data-ttu-id="83c15-126">たとえば、イベント ハンドラーを記述し、メソッドを書き込み、さらにフォーム拡張子にグローバル状態を格納する、拡張フォームに関連付けられているランタイム クラスを定義します。</span><span class="sxs-lookup"><span data-stu-id="83c15-126">For example, define a run-time class that is associated with an extension form where you write event handlers, write methods, and store a global state for your form extension.</span></span></li>
<li><span data-ttu-id="83c15-127"><strong>Lookup</strong>、<strong>LookupReference</strong>、<strong>ResolveReference</strong>、<strong>jumpRef</strong> メソッドのオーバーライドの代わりとなる拡張機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="83c15-127">Provide an extension alternative to overrides of the <strong>Lookup</strong>, <strong>LookupReference</strong>, <strong>ResolveReference</strong>, and <strong>jumpRef</strong> methods.</span></span></li>
</ul>
<span data-ttu-id="83c15-128">2016 年 8 月リリースの<strong>アプリケーション プラットフォーム</strong>および <strong>Test Essentials</strong> モデルは<em>カスタマイズすることはできない</em> (重ねて) ため、拡張機能が Dynamics AX の主な機能です。</span><span class="sxs-lookup"><span data-stu-id="83c15-128">Extensibility features are key features of the Dynamics AX platform because the <strong>Application Platform</strong> and <strong>Test Essentials</strong> models <em>cannot be customized</em> (over-layered) in the August 2016 release.</span></span> <span data-ttu-id="83c15-129">また、<strong>アプリケーション基準</strong>モデル内の要素をカスタマイズする場合、このモデルが次の Dynamics AX プラットフォーム更新でカスタマイズからロックされる予定であるとの警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="83c15-129">Also, if you customize elements in the <strong>Application Foundation</strong> model, you will get warnings as this model is scheduled to be locked from customizations in the next Dynamics AX platform update.</span></span></td>
</tr>
</tbody>
</table>

## <a name="cloud-operations"></a><span data-ttu-id="83c15-130">クラウドの工程</span><span class="sxs-lookup"><span data-stu-id="83c15-130">Cloud operations</span></span>

| <span data-ttu-id="83c15-131">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-131">What can you do?</span></span> | <span data-ttu-id="83c15-132">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-132">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-133">テスト用の実稼働環境データベースの複製を作成します。</span><span class="sxs-lookup"><span data-stu-id="83c15-133">Create replicas of production environment databases for testing.</span></span> | <span data-ttu-id="83c15-134">実稼働環境からのデータベースのコピーを使用して、階層 2 サンドボックス環境を更新するよう Microsoft に要求を送信することができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-134">You can submit a request to Microsoft to update your Tier-2 sandbox environment by using a copy of your database from your production environment.</span></span> |
| <span data-ttu-id="83c15-135">リアルタイムで Microsoft Azure SQL データベースのクエリの実行を監視します。</span><span class="sxs-lookup"><span data-stu-id="83c15-135">Monitor the execution of Microsoft Azure SQL Database queries in real time.</span></span> | <span data-ttu-id="83c15-136">ブロックされたクエリおよびブロックしているクエリを表示することにより、SQL の問題をリアルタイムでトラブルシューティングすることができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-136">You can troubleshoot SQL issues in real time by viewing the queries that are blocked and the queries that are blocking them.</span></span> <span data-ttu-id="83c15-137">また、現在これらをロックしているテーブルの、集計済みロック情報を表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="83c15-137">You can also view aggregated lock information for tables that currently have locks on them.</span></span> |

## <a name="user-interface"></a><span data-ttu-id="83c15-138">ユーザー インターフェイス</span><span class="sxs-lookup"><span data-stu-id="83c15-138">User interface</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="83c15-139">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-139">What can you do?</span></span></th>
<th><span data-ttu-id="83c15-140">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-140">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="83c15-141">既存の手順を再生せずに、ステップの並べ替えや新しいステップの挿入によって、タスク録画を簡単に編集できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-141">Easily edit task recordings by rearranging steps or inserting new steps without playing back any existing steps.</span></span></td>
<td><span data-ttu-id="83c15-142">タスク レコーダーは、<strong>編集</strong> メニュー (現在は <strong>記録テキストの変更</strong> となっています) の新しいツールを通じて強化されています。</span><span class="sxs-lookup"><span data-stu-id="83c15-142">Task recorder has been improved through new tools on the <strong>Edit</strong> menu (currently titled <strong>Change recording text</strong>).</span></span> <span data-ttu-id="83c15-143">新しいツールを使用すると、記録のステップの順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-143">The new tools let you change the order of steps in the recording.</span></span> <span data-ttu-id="83c15-144">最初に移動するステップを選択し、次にステップが移動する場所を選択します。</span><span class="sxs-lookup"><span data-stu-id="83c15-144">First select the step to move, and then select the location to move the step to.</span></span> <span data-ttu-id="83c15-145">また、既存のステップの間に新しいステップを挿入することもできます。</span><span class="sxs-lookup"><span data-stu-id="83c15-145">You can also insert new steps between existing steps.</span></span> <span data-ttu-id="83c15-146">まず新しいステップを挿入する場所を選択し、次に単に新しい手順を記録します。</span><span class="sxs-lookup"><span data-stu-id="83c15-146">First select the location where you want to insert the new steps, and then just record the new steps.</span></span> <span data-ttu-id="83c15-147">既存のステップを再生する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="83c15-147">You don't have to play back any existing steps.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83c15-148">拡張可能なコントロールは、非公開のアプリケーション プログラム インターフェイス (API) から導かれます。</span><span class="sxs-lookup"><span data-stu-id="83c15-148">Extensible controls are guided away from non-public application programming interfaces (APIs).</span></span></td>
<td><span data-ttu-id="83c15-149">拡張可能なコントロールが将来中断されることを最小にするために、拡張可能なコントロールで使用できる JavaScript アプリケーショ ンプログラミング インターフェイス (API) をパブリックなものと非パブリックなものとを区別するための努力がなされています。</span><span class="sxs-lookup"><span data-stu-id="83c15-149">To minimize future breaks in extensible controls, an effort has been made to differentiate between the public and non-public JavaScript application programming interfaces (APIs) available to extensible controls.</span></span> <span data-ttu-id="83c15-150">この作業の一環として、ドキュメントが使用できるようになりました。拡張可能コントロール作成者が使用できるパブリック JavaScript API は <a href="../../dev-itpro/user-interface/public-javascript-apis.md" data-raw-source="[here](../../dev-itpro/user-interface/public-javascript-apis.md)"> こちら</a>です。</span><span class="sxs-lookup"><span data-stu-id="83c15-150">As part of this effort, documentation is now available <a href="../../dev-itpro/user-interface/public-javascript-apis.md" data-raw-source="[here](../../dev-itpro/user-interface/public-javascript-apis.md)">here</a> for the public JavaScript APIs that extensible control authors can use.</span></span> <span data-ttu-id="83c15-151">また、プラットフォーム アップデート 3 以降、公開されていない API は必要に応じて削除または変更できるため、拡張可能コントロールの作成者は、コントロールが公開 API のみ使用していることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83c15-151">Additionally, extensible control authors should start ensuring their controls are only using public APIs, as starting with Platform Update 3 any non-public API may be removed or modified as needed.</span></span> <span data-ttu-id="83c15-152">非公開 API の計画された変更の 1 つは、アクセス レベルを明確に示すために名前の接頭語にアンダースコアを付けることです。</span><span class="sxs-lookup"><span data-stu-id="83c15-152">One planned modification for the non-public APIs is to prefix the names with underscores to clearly denote their access level.</span></span> <span data-ttu-id="83c15-153">今回のリリースでは、この名前の変更が行われている API は、それらが使用されていない精度の高いものだけです。</span><span class="sxs-lookup"><span data-stu-id="83c15-153">In this release, the only APIs that are undergoing this name change are those for which we have high confidence they are not being used.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="83c15-154">更新した Gantt 管理を使用し、対話型のスケジューリング シナリオを開発します。</span><span class="sxs-lookup"><span data-stu-id="83c15-154">Use the updated Gantt control to develop interactive scheduling scenarios.</span></span></td>
<td><span data-ttu-id="83c15-155">更新された Gantt コントロールは、新しいインタラクティブなスケジューリング シナリオの開発を可能にし、アクティビティの外観をカスタマイズするための強化された API を提供します。</span><span class="sxs-lookup"><span data-stu-id="83c15-155">The updated Gantt control enables the development of new interactive scheduling scenarios and delivers enhanced APIs for customizing the appearance of activities.</span></span> <span data-ttu-id="83c15-156">次に新しい API の一部を挙げます:</span><span class="sxs-lookup"><span data-stu-id="83c15-156">Here are some of the new APIs:</span></span>
<ul>
<li><span data-ttu-id="83c15-157">垂直のドラッグ アンド ドロップのアクティビティ</span><span class="sxs-lookup"><span data-stu-id="83c15-157">Vertical drag-and-drop of activities</span></span></li>
<li><span data-ttu-id="83c15-158">追加/削除のアクティビティ</span><span class="sxs-lookup"><span data-stu-id="83c15-158">Add/remove activities</span></span></li>
<li><span data-ttu-id="83c15-159">集計バーにある引当済期間のプレビュー</span><span class="sxs-lookup"><span data-stu-id="83c15-159">Preview booked periods in summary bar</span></span></li>
<li><span data-ttu-id="83c15-160">アクティビティ ボーダーの色とスタイルの変更</span><span class="sxs-lookup"><span data-stu-id="83c15-160">Change color and style of activity borders</span></span></li>
<li><span data-ttu-id="83c15-161">グリッド内のテキストの色、スタイル、および背景を変更する</span><span class="sxs-lookup"><span data-stu-id="83c15-161">Change color, style and background of text in grid</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="microsoft-office-integration"></a><span data-ttu-id="83c15-162">Microsoft Office 統合</span><span class="sxs-lookup"><span data-stu-id="83c15-162">Microsoft Office integration</span></span>

| <span data-ttu-id="83c15-163">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-163">What can you do?</span></span> | <span data-ttu-id="83c15-164">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-164">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-165">Skype プレゼンス インジケーターの上にカーソルを置いて、Skype 連絡先カードを表示します。</span><span class="sxs-lookup"><span data-stu-id="83c15-165">View Skype contact cards by hovering over Skype presence indicators.</span></span> | <span data-ttu-id="83c15-166">Skype プレゼンス インジケーターの上にカーソルを置くと、Skype 連絡先カードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="83c15-166">Skype contact cards are now shown when you hover over Skype presence indicators.</span></span> <span data-ttu-id="83c15-167">この機能により、連絡先情報と連絡先画像に簡単にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="83c15-167">This feature provides easy access to contact information and a contact image.</span></span> |
| <span data-ttu-id="83c15-168">セクション スタイルのテーブルを持つ Microsoft Word 文書をデザインして生成します。</span><span class="sxs-lookup"><span data-stu-id="83c15-168">Design and generate Microsoft Word documents that have section-style tables.</span></span> | <span data-ttu-id="83c15-169">Word ドキュメントの生成では、読みやすさを向上してスペースを空けるために、グリッド スタイル テーブルに加え、セクション スタイル テーブルをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-169">Word document generation now supports section-style tables in addition to grid-style tables, to improve readability and provide more space.</span></span> <span data-ttu-id="83c15-170">Word テンプレート デザイナーも更新されており、セクション スタイル テーブルをテンプレートに追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-170">The Word template designer has also been updated, so that section-style tables can now be added into templates.</span></span> |
| <span data-ttu-id="83c15-171">スクリーン リーダーを Office アドインと併せて使用します。</span><span class="sxs-lookup"><span data-stu-id="83c15-171">Use screen readers together with the Office Add-ins.</span></span> | <span data-ttu-id="83c15-172">Office アドインは、スクリーン リーダーの完全なサポートの使用によって、よりアクセスしやすくなりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-172">Office Add-ins are now more accessible through full support for screen readers.</span></span> |

## <a name="analytics"></a><span data-ttu-id="83c15-173">分析</span><span class="sxs-lookup"><span data-stu-id="83c15-173">Analytics</span></span>

| <span data-ttu-id="83c15-174">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-174">What can you do?</span></span> | <span data-ttu-id="83c15-175">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-175">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-176">顧客が所有するデータ ウェアハウスにエンティティをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="83c15-176">Export entities to customer-owned data warehouses.</span></span> | <span data-ttu-id="83c15-177">Dynamics AX でプロビジョニングされたエンティティ格納は、Microsoft Power BI および Microsoft Cortana Intelligence Suite との統合用に構成されています。</span><span class="sxs-lookup"><span data-stu-id="83c15-177">The entity store that is provisioned with Dynamics AX is configured for integration with Microsoft Power BI and Microsoft Cortana Intelligence Suite.</span></span> <span data-ttu-id="83c15-178">サードパーティのビジネス インテリジェンス (BI) ツールまたは既存のデータ ウェアハウスとの統合を要求する場合は、SQL データベースにデータ エンティティをエクスポートできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-178">If you require integration with a third-party business intelligence (BI) tool or a preexisting data warehouse, you can now export data entities to your own SQL database.</span></span> <span data-ttu-id="83c15-179">データはフル プッシュまたは増分プッシュとしてエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-179">Data can be exported as a full push or as an incremental push.</span></span> <span data-ttu-id="83c15-180">したがって、この機能を頻繁に更新することができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-180">Therefore, this feature enables frequent updates.</span></span> |
| <span data-ttu-id="83c15-181">ドキュメント回覧エージェントを Windows サービス アプリケーションとして実行します。</span><span class="sxs-lookup"><span data-stu-id="83c15-181">Run the Document Routing Agent as a Windows service application.</span></span> | <span data-ttu-id="83c15-182">ドキュメント回覧エージェントは、実行モードを選択するオプションを提供するようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-182">The Document Routing Agent now offers an option to select the mode of execution.</span></span> <span data-ttu-id="83c15-183">Windows サービスとして実行中、コンピューターの起動時にアプリケーションは自動的に開始され、特定のユーザー アカウントのセキュリティ コンテキストで実行するよう構成されます。</span><span class="sxs-lookup"><span data-stu-id="83c15-183">While running as a Windows service, the application can be automatically started when the computer boots and configured to run under the security context of a specific user account.</span></span> <span data-ttu-id="83c15-184">この機能拡張は、ネットワーク プリント サーバーなどの共有リソース上でドキュメント ルート指定エージェントをホストしている顧客からの直接のフィードバックに基づいて追加されました。</span><span class="sxs-lookup"><span data-stu-id="83c15-184">This enhancement was added based on direct feedback from customers hosting the Document Routing Agent on shared resources like Network Print Servers.</span></span> |
| <span data-ttu-id="83c15-185">エクスポートされたレポートは、ターゲット言語が日本語の場合、Yu ゴシック フォントを使用します。</span><span class="sxs-lookup"><span data-stu-id="83c15-185">Exported reports use the Yu Gothic font when the target language is Japanese.</span></span> | <span data-ttu-id="83c15-186">すぐに使えるレポート、つまり独立系ソフトウェア ベンダー (ISV) が Dynamics AX ツールを使用して作成するレポートは、ターゲット言語が日本語の場合に Yu Gothic フォントでエクスポート ドキュメントを生成します。</span><span class="sxs-lookup"><span data-stu-id="83c15-186">Out-of-box reports, or reports that independent software vendors (ISVs) develop by using Dynamics AX tools, generate exported documents in the Yu Gothic font when the target language is Japanese.</span></span> <span data-ttu-id="83c15-187">以前は、既定では、レポートが、すべての複数バイト言語のフル文字セットをサポートしていない Sego UI フォントを使用していました。</span><span class="sxs-lookup"><span data-stu-id="83c15-187">Previously, by default, reports used the Sego UI font, which doesn't support the full character set for all multi-byte languages.</span></span> <span data-ttu-id="83c15-188">したがって、ターゲット言語が日本語の場合、エクスポートされたドキュメントが不正な形式で表示されました。</span><span class="sxs-lookup"><span data-stu-id="83c15-188">Therefore, exported documents appeared malformed when the target language was Japanese.</span></span> |
| <span data-ttu-id="83c15-189">コントローラー拡張機能を使用して、エクスポートおよびアーカイブされたドキュメントの既定のファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="83c15-189">Use controller extensions to establish default file names for exported and archived documents.</span></span> | <span data-ttu-id="83c15-190">開発者は、トランザクション属性 (顧客名や請求書番号など) とこれらのドキュメントを関連付けるために使用できるコンテキスト名を持つドキュメントを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-190">Developers can produce documents that have contextual names that they can use to associate those documents with transactional attributes (such as customer name or invoice number).</span></span> <span data-ttu-id="83c15-191">コンテキスト名により、エクスポートおよびアーカイブされたドキュメントのフレンドリ名を作成できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-191">Contextual names enable the creation of friendly names for exported and archived documents.</span></span> |

## <a name="security"></a><span data-ttu-id="83c15-192">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="83c15-192">Security</span></span>

| <span data-ttu-id="83c15-193">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-193">What can you do?</span></span> | <span data-ttu-id="83c15-194">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-194">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-195">Azure AD 企業間サービスを使用して、企業間のシナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="83c15-195">Enable business-to-business scenarios by using the Azure AD Business to Business service.</span></span> | <span data-ttu-id="83c15-196">外部ユーザーは、外部から管理された ID を使用して Dynamics AX に招待することができます。</span><span class="sxs-lookup"><span data-stu-id="83c15-196">External users can be invited to Dynamics AX using an externally managed identity.</span></span> <span data-ttu-id="83c15-197">外部ユーザーは、もはや既存の Azure AD テナントの一部である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="83c15-197">External users no longer have to be part of an existing Azure AD tenant.</span></span> |
| <span data-ttu-id="83c15-198">サービス間の認証を有効にします。</span><span class="sxs-lookup"><span data-stu-id="83c15-198">Enable service-to-service authentication.</span></span> | <span data-ttu-id="83c15-199">登録されたサービスは、ユーザーがサインインしなくても Dynamics AX に接続できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-199">Registered services can connect to Dynamics AX without requiring a user to sign in.</span></span> |

## <a name="integrations"></a><span data-ttu-id="83c15-200">統合</span><span class="sxs-lookup"><span data-stu-id="83c15-200">Integrations</span></span>

| <span data-ttu-id="83c15-201">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="83c15-201">What can you do?</span></span> | <span data-ttu-id="83c15-202">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="83c15-202">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="83c15-203">データ エンティティへの差分更新のエクスポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="83c15-203">Enable the export of incremental updates to a data entity.</span></span> | <span data-ttu-id="83c15-204">定期的なデータ プロジェクトの設定で、増分更新がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="83c15-204">The setup of recurring data projects now supports incremental updates.</span></span> <span data-ttu-id="83c15-205">つまり、ユーザーは、そのエンティティに対する変更を定期的にエクスポートするエクスポート データ プロジェクトを設定できます。</span><span class="sxs-lookup"><span data-stu-id="83c15-205">In other words, users can set up an export data project that periodically exports any changes to that entity.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="83c15-206">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="83c15-206">Additional resources</span></span>

[<span data-ttu-id="83c15-207">新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="83c15-207">What's new or changed</span></span>](whats-new-changed.md)
