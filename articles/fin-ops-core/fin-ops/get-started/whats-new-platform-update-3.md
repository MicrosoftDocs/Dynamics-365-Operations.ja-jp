---
title: Dynamics 365 for Operations プラットフォーム更新プログラム 3 (2016 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 3 の新機能または変更された機能について説明します。 このバージョンは 2016 年 11 月にリリースされ、ビルド番号は 7.0.4307.16141 です。
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: 220184
ms.assetid: 8beb4e7f-4a71-4c50-adf7-7733e6a150d9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Platform update 3
ms.openlocfilehash: c9b2eacf9e805b7b1d71df8ca4c47565ab4cc16c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752208"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-operations-platform-update-3-november-2016"></a><span data-ttu-id="0f5fd-104">Dynamics 365 for Operations プラットフォーム更新プログラム 3 (2016 年 11 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0f5fd-104">What's new or changed in Dynamics 365 for Operations platform update 3 (November 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f5fd-105">このトピックでは、Dynamics 365 for Operations プラットフォーム更新プログラム 3 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-105">This topic describes features that are either new or changed in Dynamics 365 for Operations platform update 3.</span></span> <span data-ttu-id="0f5fd-106">このバージョンは 2016 年 11 月にリリースされ、ビルド番号は 7.0.4307.16141 です。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-106">This version was released in November 2016 and has a build number of 7.0.4307.16141.</span></span>

## <a name="general"></a><span data-ttu-id="0f5fd-107">一般</span><span class="sxs-lookup"><span data-stu-id="0f5fd-107">General</span></span>

| <span data-ttu-id="0f5fd-108">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-108">What you can do</span></span> | <span data-ttu-id="0f5fd-109">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-109">Why is this important</span></span> |
|-----------------|-----------------------|
| <span data-ttu-id="0f5fd-110">Dynamics AX は、Dynamics 365 for Operations にブランド改称されています。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-110">Dynamics AX has been rebranded to Dynamics 365 for Operations.</span></span> | <span data-ttu-id="0f5fd-111">Microsoft Dynamics AX は、現在新しい Microsoft Dynamics 365 傘下の一部になりました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-111">Microsoft Dynamics AX is now part of the new Microsoft Dynamics 365 umbrella.</span></span> <span data-ttu-id="0f5fd-112">この変更により、製品名と製品アイコンの両方のリブランディングが義務づけられました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-112">This change has mandated rebranding in terms of both the product name and the product icon.</span></span> <span data-ttu-id="0f5fd-113">Dynamics AX の新しい名称は Dynamics 365 for Operations です。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-113">The new name for Dynamics AX is Dynamics 365 for Operations.</span></span> |
| <span data-ttu-id="0f5fd-114">Dynamics 365 for Operations 試用版を使用する</span><span class="sxs-lookup"><span data-stu-id="0f5fd-114">Use a Dynamics 365 for Operations trial</span></span> | <span data-ttu-id="0f5fd-115">Dynamics 365 for Operations の 30 日間試用版は、簡単な電子メールでのサインアップでお試しいただけます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-115">A 30-day trial of Dynamics 365 for Operations will be made available through a simple email signup.</span></span> <span data-ttu-id="0f5fd-116">Dynamics 365 for Operations の試用版には、ステップ バイ ステップのタスク ガイドが記載されている「はじめに」ガイドが含まれており、実行中の特定のシナリオを見ることができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-116">The trial version of Dynamics 365 for Operations includes a Getting started guide that provides a step-by-step task guide, which allows you to view specific scenarios in action.</span></span> <span data-ttu-id="0f5fd-117">この製品は、シナリオの探索や練習に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-117">The product is available to explore and exercise scenarios.</span></span> <span data-ttu-id="0f5fd-118">製品の使用を簡単にするため、また経験がより意味あるものになるためにデモ データが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-118">Demo data is included to ease the use of the product and to make the experience more meaningful.</span></span> <span data-ttu-id="0f5fd-119">トライアル版の有効期限が終了する 3 日前に、通知の電子メールが送信されます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-119">A reminder email will be sent 3 days prior to the trial expiration.</span></span> <span data-ttu-id="0f5fd-120">その時点で購入体験を開始して購入を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-120">A buy experience can be initiated at that time to complete the purchase.</span></span> |

## <a name="development-and-customization"></a><span data-ttu-id="0f5fd-121">開発とカスタマイズ</span><span class="sxs-lookup"><span data-stu-id="0f5fd-121">Development and customization</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f5fd-122">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-122">What you can do</span></span></th>
<th><span data-ttu-id="0f5fd-123">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-123">Why is this important</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f5fd-124">ラベル ファイルを拡張して、ラベルをカスタマイズおよびローカライズします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-124">Extend label files to customize and localize labels.</span></span></td>
<td><span data-ttu-id="0f5fd-125">既存のラベルの文字列の値を変更して、既存のモデルを編集またはオーバーレイする必要なしに既存のラベル ファイルに新しい言語を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-125">You can modify the string values of existing labels and add new languages to existing label files without the need to edit or overlay existing models.</span></span> <span data-ttu-id="0f5fd-126"><a href="../../dev-itpro/extensibility/customization-overlayering-extensions.md">カスタマイズ: オーバーレイおよび拡張機能</a>の「ラベルの拡張機能」をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-126">Refer to the "Label extensions" section in <a href="../../dev-itpro/extensibility/customization-overlayering-extensions.md">Customization: Overlayering and extensions</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-127">シームレスなサービスと継続的な更新を利用します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-127">Take advantage of seamless servicing and continuous updates.</span></span></td>
<td><span data-ttu-id="0f5fd-128">Dynamics 365 for Operations プラットフォームには次のようなモデルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-128">The Dynamics 365 for Operations platform includes the following models:</span></span>
<ul>
<li><span data-ttu-id="0f5fd-129">アプリケーション プラットフォーム</span><span class="sxs-lookup"><span data-stu-id="0f5fd-129">Application Platform</span></span></li>
<li><span data-ttu-id="0f5fd-130">アプリケーション基準</span><span class="sxs-lookup"><span data-stu-id="0f5fd-130">Application Foundation</span></span></li>
<li><span data-ttu-id="0f5fd-131">Test Essentials</span><span class="sxs-lookup"><span data-stu-id="0f5fd-131">Test Essentials</span></span></li>
<li><span data-ttu-id="0f5fd-132">対応するフォーム アダプタ モデル</span><span class="sxs-lookup"><span data-stu-id="0f5fd-132">Corresponding form adaptor models</span></span></li>
</ul>
<span data-ttu-id="0f5fd-133">プラットフォームのロックにより、 Dynamics 365 for Operations プラットフォームのシームレスなサービスと継続的な更新への道筋を作ります。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-133">Locking the platform paves the way for seamless servicing and continuous update of the Dynamics 365 for Operations platform.</span></span> <span data-ttu-id="0f5fd-134">いずれかのプラットフォームをオーバーレイすると、このリリースにアップグレードすることはできません。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-134">If you overlay any of the platform models, you will not be able to upgrade to this release.</span></span> <span data-ttu-id="0f5fd-135">メタデータおよびコードの拡張機能を使用するには、コードをリファクターする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-135">You will need to refactor your code to use metadata and code extensions.</span></span> <span data-ttu-id="0f5fd-136">カスタマイズの拡張機能を使用する方法に関するチュートリアルについては、<a href="../../dev-itpro/extensibility/customize-model-elements-extensions.md">拡張機能を使用してモデル要素をカスタマイズする</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-136">For a tutorial about how to use extensions for customization, see <a href="../../dev-itpro/extensibility/customize-model-elements-extensions.md">Customize model elements using extensions</a>.</span></span> <span data-ttu-id="0f5fd-137">また、<a href="../../dev-itpro/extensibility/customization-overlayering-extensions.md">カスタマイズ: オーバーレイと拡張機能</a> を参照することができます。これはカスタマイズの一般的なトピックです。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-137">You can also refer to <a href="../../dev-itpro/extensibility/customization-overlayering-extensions.md">Customization: Overlayering and extensions</a>, which is a general topic on customizations.</span></span>
<blockquote>[!NOTE] <span data-ttu-id="0f5fd-138">ディレクトリ モデルに関して、コードがディレクトリ モデル内の要素をオーバーレイする場合、最新の Dynamics 365 for Operations アプリケーションを実行している新しい環境を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-138">Regarding the Directory model, if your code overlayers elements in the Directory model, you will need to deploy new environments running the latest Dynamics 365 for Operations application.</span></span> <span data-ttu-id="0f5fd-139">ディレクトリ モデルのオーバーレイヤーは、プラットフォーム更新プログラム 3 の上にアプリケーションの 2016 年 2 月または 2016 年 5 月リリースを実行している環境ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-139">Overlayering the directory model is not supported on environments running the February 2016 or May 2016 releases of the application on top of Platform Update 3.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-140">フォームの一部をフォーム エクステンションに追加し、移動 /F9 機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-140">Add a form part to a form extension and use Go to/F9 functionality.</span></span></td>
<td><span data-ttu-id="0f5fd-141">フォーム拡張機能を使用すると、フォームをオーバーレイヤーすることなく、どのフォームにもフォーム パーツ参照を追加できるようになります。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-141">Using a form extension, you can now add a Form Part reference to any form without overlayering the form.</span></span> <span data-ttu-id="0f5fd-142">さらに、フォーム デザイナーでフォームの一部を参照するときに、移動 (F9) を使用して参照されているフォームに移動することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-142">In addition, you can use Go to (F9) to go to the referenced form when browsing a form part in the form designer.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-143">データ エンティティの拡張機能に新しいマップを追加します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-143">Add a new mapping to a data entity extension.</span></span></td>
<td><span data-ttu-id="0f5fd-144">新しいマッピングをデータ エンティティ拡張機能に追加することができるようになりました。これは、オーバーレイせずにデータ エンティティを新しいマップに関連付けることができることを意味します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-144">You can now add a new mapping to a data entity extension, which means you can associate the data entity with a new map without overlayering.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-145">フォームの拡張機能を使用してフォーム キャプションを変更します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-145">Change a form caption using a form extension.</span></span></td>
<td><span data-ttu-id="0f5fd-146">フォームをオーバーレイせずに、フォームのキャプションを変更することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-146">You can now change the caption of a form without overlayering the form.</span></span> <span data-ttu-id="0f5fd-147">フォーム拡張機能を使用して、キャプション プロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-147">Using a form extension you can change the caption property.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-148">EDT拡張機能を使用して EDT FormHelp プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-148">Change an EDT FormHelp property using an EDT extension.</span></span></td>
<td><span data-ttu-id="0f5fd-149">拡張データ型 (EDT) 拡張機能を使用すると、FormHelp プロパティを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-149">Using an extended data type (EDT) extension, you can change the FormHelp property.</span></span> <span data-ttu-id="0f5fd-150">これにより、EDT を重ねて使用することなく EDT を使用するどの場所でもカスタム ルックアップ フォームを変更または追加できます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-150">This lets you to change or add a custom lookup form anywhere an EDT is used without overlayering the EDT.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-151">テーブル拡張機能を使用して、テーブル フィールドのラベルを変更します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-151">Change the label of a table field using a table extension.</span></span> <span data-ttu-id="0f5fd-152">テーブル拡張を使用して、作成者、作成日時、更新者、変更日時のテーブル プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-152">Change the Created By, Created Date Time, Modified By, Modified Date Time properties of a table using a table extension.</span></span></td>
<td><span data-ttu-id="0f5fd-153">テーブルをオーバーレイせずに、テーブルの既存のフィールドのラベルを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-153">You can change the label of an existing field of a table without overlayering the table.</span></span> <span data-ttu-id="0f5fd-154">これは、テーブル拡張を使用して行うことができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-154">This can be done using a table extension.</span></span> <span data-ttu-id="0f5fd-155">オーバーレイなしでテーブルの作成者、作成日時、修正者、修正日時のプロパティの値を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-155">You can also modify the values of the properties Created By, Created Date Time, Modified By, Modified Date Time of a table without overlayering.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-156">データ エンティティの固定フィールド関係を定義するときは、拡張可能列挙型を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-156">Refer to an extensible enum when defining fixed field relations for a data entity.</span></span></td>
<td><span data-ttu-id="0f5fd-157">データ エンティティ上に固定フィールド関係を定義するときは、拡張可能列挙型を参照することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-157">You can refer to an extensible enumeration when defining a fixed field relation on a data entity.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-158">Visual Studio デバッガーで、拡張機能フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-158">View extension fields in the Visual Studio debugger.</span></span></td>
<td><span data-ttu-id="0f5fd-159">テーブルおよびその他の拡張可能要素をデバッグするときは、デバッガーで拡張フィールドを表示できます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-159">When debugging tables and other similar extensible elements, you can view extension fields in the debugger.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-160">拡張機能を使用してアプリケーションをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-160">Customize application reports using extensions.</span></span></td>
<td><span data-ttu-id="0f5fd-161">一般的なカスタマイズのための標準アプリケーション ソリューションのオーバーレイに関連付けられている複雑さと経費を回避します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-161">Avoid the expense and complexity associated with overlayering standard application solutions for common customizations.</span></span> <span data-ttu-id="0f5fd-162">Dynamics 365 for Operations には、要素の拡張子を使用してアプリケーション レポートをカスタマイズするためのサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-162">Dynamics 365 for Operations now includes support for customizing application reports using element extensions.</span></span> <span data-ttu-id="0f5fd-163">この機能拡張により、アプリケーション参照を変更することなく、既存のメニュー項目をカスタム レポート デザインにリダイレクトできます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-163">This enhancement means that you can redirect existing menu items to custom reports designs without changing application references.</span></span> <span data-ttu-id="0f5fd-164">また、アプリケーション コードを複製またはオーバーレイせずに、レポート データ プロバイダー クラスによって返されるデータセットを拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-164">You can also extend the datasets returned by Report Data Providers classes without duplicating or overlayering application code.</span></span> <span data-ttu-id="0f5fd-165">アプリケーション カスタマイズの拡張機能の使用に関する詳細については、<a href="../../dev-itpro/extensibility/customize-model-elements-extensions.md">拡張機能を使用してモデル要素をカスタマイズする</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-165">For detailed information about using extensions for application customizations, see <a href="../../dev-itpro/extensibility/customize-model-elements-extensions.md">Customize model elements using extensions</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-166">組み込みのドキュメント ブランド管理ツールを使用して、売上請求書、購買梱包明細書、および仕入先請求書などの主要なビジネス ドキュメント用の最新のレポート デザインをカスタマイズします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-166">Use built-in document brand management tools to customize modern report designs for core business documents, including Sales Invoices, Purchase Packing Slips, and Vendor Invoice Documents.</span></span> <span data-ttu-id="0f5fd-167">Lifecycle Services (LCS) にある Application Suite Modern Designs モデル ファイルをソリューションにそのまま追加します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-167">Simply add the Application Suite Modern Designs model file available on Lifecycle Services (LCS) to your solution.</span></span></td>
<td><span data-ttu-id="0f5fd-168">この機能は、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-168">This feature provides the following:</span></span>
<ul>
<li><span data-ttu-id="0f5fd-169">単一の法人が運営している複数の商業ブランドを管理するためのコンフィギュレーション ベース ソリューション。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-169">A configuration-based solution for managing multiple commercial brands operated by a single legal entity.</span></span></li>
<li><span data-ttu-id="0f5fd-170">さまざまなコア ビジネス ドキュメントの現代レポートのデザイン。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-170">Modern report designs for a variety of core business documents.</span></span></li>
<li><span data-ttu-id="0f5fd-171">アクティブなサービスを中断することなく、顧客が管理フォームを使用してドキュメント ヘッダー情報を管理する方法。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-171">A way for customers to manage document header information using administration forms without disrupting active services.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-172">拡張機能を使ってヘルプをカスタマイズする</span><span class="sxs-lookup"><span data-stu-id="0f5fd-172">Customize Help using extensions</span></span></td>
<td><span data-ttu-id="0f5fd-173">Dynamics 365 for Operations ヘルプ フォームにタブを追加して、すぐに使用可能なタスク ガイドおよびトピック ソースと共に、サードパーティーのヘルプ コンテンツを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-173">You can add a tab to the Dynamics 365 for Operations Help form to display third-party Help content, alongside the Task guides and topic sources that ship out of the box.</span></span> <span data-ttu-id="0f5fd-174">以前のバージョンでは、ヘルプの追加ソースで使用できるように、ユーザーの検索文字列にアクセスする唯一の方法は、フォームをオーバーレイにすることでした。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-174">In previous versions, the only way to access to a user's search terms, so that they can be used in the additional source of Help, was to overlayer the form.</span></span> <span data-ttu-id="0f5fd-175">ヘルプ フォーム (SysHelpPane) にデリゲートが追加されました。ユーザーの検索語を傍受し、それらを使用してサードパーティ製システムのヘルプ コンテンツを検索できます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-175">A delegate has now been added to the Help form (SysHelpPane), so you can intercept a user's search terms and use them to search for Help content in third-party systems.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-176">コンフィギュレーション キーのプロパティのサポートされていない変更を禁止します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-176">Prevent unsupported changes of configuration key properties.</span></span></td>
<td><span data-ttu-id="0f5fd-177">参照されるコンフィギュレーション キーがバイナリ モデルで定義されている場合は、コンフィギュレーション キーのプロパティ (たとえば、フォームのコントロール) は変更できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-177">You can no longer change a Configuration key property (for example, on a form control) if the referenced configuration key is defined in a binary model.</span></span> <span data-ttu-id="0f5fd-178">バイナリ モデルは、そのソース コードなしでインストールされているモデルです。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-178">A binary model is a model installed without its source code.</span></span> <span data-ttu-id="0f5fd-179">ISV はライセンスと構成キーを定義し、バイナリー モデルとして配布します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-179">ISVs define licenses and configuration keys and distribute them as binary models.</span></span> <span data-ttu-id="0f5fd-180">この機能は、構成キーの割り当ての変更が、開発ツールで正式にサポートされていないことを開発者に示します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-180">This feature indicates to developers that changing configuration key assignments is not officially supported by the development tools.</span></span> <span data-ttu-id="0f5fd-181">この機能は、開発者が Visual Studio 開発ツール以外のテキスト エディターで変更を行うことを防止するものではありません。これは不正な使用とみなされます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-181">This feature does not prevent a developer from making the change in a text editor outside of the Visual Studio development tools, which would be considered unauthorized use.</span></span></td>
</tr>
</tbody>
</table>

## <a name="servicing-environments"></a><span data-ttu-id="0f5fd-182">サービス環境</span><span class="sxs-lookup"><span data-stu-id="0f5fd-182">Servicing environments</span></span>

| <span data-ttu-id="0f5fd-183">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-183">What you can do</span></span> | <span data-ttu-id="0f5fd-184">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-184">Why is this important</span></span> |
|-----------------|-----------------------|
| <span data-ttu-id="0f5fd-185">最大 3 つの配置可能パッケージをマージします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-185">Merge up to 3 deployable packages.</span></span> | <span data-ttu-id="0f5fd-186">この機能は、これらのパッケージの適用に起因するダウンタイムを大幅に削減し、これらのパッケージと全体の待機時間の適用を最適化します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-186">This feature significantly reduces the downtime resulting from the application of these packages, and optimizes applying these packages and the overall wait time.</span></span> |
| <span data-ttu-id="0f5fd-187">配置可能なパッケージをダウンタイムを短縮して適用します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-187">Apply deployable packages with reduced downtime.</span></span> | <span data-ttu-id="0f5fd-188">現在、LCS を通じて展開された環境で、単一パッケージを適用するのに必要な平均ダウンタイムは最大 5 時間です。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-188">Currently, the average downtime needed to apply a single package in an environment deployed through LCS can be up to 5 hours.</span></span> <span data-ttu-id="0f5fd-189">この機能により、パッケージ アプリケーションが最適化されるため、ダウンタイムが大幅に減少します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-189">With this feature, the package application is optimized so that the downtime is greatly reduced.</span></span> |
| <span data-ttu-id="0f5fd-190">LCS の監視および診断ツールを使用してデッドロックをトラブルシューティングします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-190">Troubleshoot deadlocks using monitoring and diagnostics tool in LCS.</span></span> | <span data-ttu-id="0f5fd-191">この機能では、LCS 内のモニタリングおよび診断ツールを使用してデッドロックをトラブルシューティングして、デッドロックがあるクエリを確認し、デッドロック グラフを確認することにより拡張トラブルシューティングを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-191">With this feature you can troubleshoot deadlocks using the monitoring and diagnostics tools in LCS to review the query that has deadlocks and perform advanced troubleshooting by reviewing the deadlock graphs.</span></span> |

## <a name="lifecycle-services"></a><span data-ttu-id="0f5fd-192">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0f5fd-192">Lifecycle Services</span></span>

<span data-ttu-id="0f5fd-193">Lifecycle Services (LCS) は、毎月の新しい機能をリリースします。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-193">Lifecycle Services (LCS) releases new features every month.</span></span> <span data-ttu-id="0f5fd-194">新機能の詳細については、[LCS ブログ](https://blogs.msdn.microsoft.com/lcs/) にアクセスしてください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-194">For information about what's new, visit the [LCS blog](https://blogs.msdn.microsoft.com/lcs/).</span></span> <span data-ttu-id="0f5fd-195">検索語「リリース計画」を使用して、毎月のリリースと新機能情報を検索して表示します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-195">Use the search term, "release plans" to search for and view the monthly release and new feature information.</span></span>

## <a name="client"></a><span data-ttu-id="0f5fd-196">クライアント</span><span class="sxs-lookup"><span data-stu-id="0f5fd-196">Client</span></span>

| <span data-ttu-id="0f5fd-197">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-197">What you can do</span></span> | <span data-ttu-id="0f5fd-198">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-198">Why is this important</span></span> |
|-----------------|-----------------------|
| <span data-ttu-id="0f5fd-199">グリッド内で下向きの矢印を使用して、新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-199">Use the down arrow in a grid to add a new row.</span></span> | <span data-ttu-id="0f5fd-200">グリッドに行を追加するとき、現在の行に不完全な情報が含まれている場合、新しい行を作成するために下方向キーを使用しても無視されます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-200">When adding rows to a grid, the use of down arrow to create a new row would be ignored if the current row contained incomplete information.</span></span> <span data-ttu-id="0f5fd-201">この動作は、**新規追加** ボタンとそのショートカット **Alt + N** の使用と一致しませんでした。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-201">This behavior was inconsistent with the use of the **Add New** button and its shortcut **Alt+N**.</span></span> <span data-ttu-id="0f5fd-202">新しい行の作成に下向きの矢印を使用することが現在は首尾一貫しています。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-202">Using the down arrow to create a new row is now consistent.</span></span> |
| <span data-ttu-id="0f5fd-203">一部の API は使用されなくなりました</span><span class="sxs-lookup"><span data-stu-id="0f5fd-203">Some APIs are now deprecated</span></span> | <span data-ttu-id="0f5fd-204">新しい Web ベースのプラットフォームの導入により、Dynamics 365 for Operations プラットフォームでは新しい対話型コントロールの完全なセットが提供されます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-204">With the introduction of a new web-based platform, the Dynamics 365 for Operations platform offers a complete set of new interactive controls.</span></span> <span data-ttu-id="0f5fd-205">場合によっては、ほとんど使用していないプロパティまたはメソッドが、Dynamics AX 2012 に存在したコントロールで非推奨でした。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-205">In some cases, seldom used properties or methods were deprecated on controls that existed in Dynamics AX 2012.</span></span> <span data-ttu-id="0f5fd-206">FormListControl の場合、ほとんど使用メソッドが実装されていませんでしたが、それらの API は非推奨としてマークされていませんでした。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-206">In the case of the FormListControl, some seldom used methods were not implemented but their API were not marked as deprecated.</span></span> <span data-ttu-id="0f5fd-207">このリリースでは、これらのメソッドは非推奨としてマークされました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-207">With this release, those methods are now marked as deprecated.</span></span> |

## <a name="mobile-app"></a><span data-ttu-id="0f5fd-208">モバイル アプリ</span><span class="sxs-lookup"><span data-stu-id="0f5fd-208">Mobile app</span></span>

| <span data-ttu-id="0f5fd-209">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-209">What you can do</span></span> | <span data-ttu-id="0f5fd-210">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-210">Why is this important</span></span> |
|-----------------|-----------------------|
| <span data-ttu-id="0f5fd-211">移動中にユーザーが生産性を維持できるようにモバイル ワークスペースを設計する。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-211">Design mobile workspaces to enable your users to stay productive while on the move.</span></span> | <span data-ttu-id="0f5fd-212">Dynamics 365 for Operations は、携帯電話アプリをサポートします (iPhone の iTunes App Store、Android 電話の Google Play Store および Window 電話の Windows Store で使用可能)。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-212">Dynamics 365 for Operations brings support for a mobile phone app (available on the iTunes App Store for iPhones, Google Play Store for Android phones, and Windows Store for Window phones).</span></span> <span data-ttu-id="0f5fd-213">モバイル アプローチにより、リッチなオフラインおよびモバイルのやりとりを可能にしながら、ビジネス ロジックとモデリングを製品から再利用でき、使いやすいデザイナー体験が可能になります。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-213">The mobile approach allows you to reuse business logic and modeling from the product while enabling rich offline and mobile interactions, and an easy-to-use designer experience.</span></span> <span data-ttu-id="0f5fd-214">開発者は、Microsoft Visual Studio で簡単なフォームを作成し、この機能を公開するモバイル ページを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-214">Developers can create simplified forms in Microsoft Visual Studio and then design mobile pages that expose this functionality.</span></span> <span data-ttu-id="0f5fd-215">このモバイル ソリューションを使用すると、フォームやモバイル アプリの定義を簡単に変更して、製品のカスタマイズを組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-215">This mobile solution makes it easy to change the forms and mobile app definitions in order to include customizations made to the product.</span></span> <span data-ttu-id="0f5fd-216">詳細については、[モバイル プラットフォームのリソース](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-216">For more information, see [Mobile platform resources](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span> |

## <a name="analytics"></a><span data-ttu-id="0f5fd-217">分析</span><span class="sxs-lookup"><span data-stu-id="0f5fd-217">Analytics</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0f5fd-218">実行可能事項</span><span class="sxs-lookup"><span data-stu-id="0f5fd-218">What you can do</span></span></th>
<th><span data-ttu-id="0f5fd-219">これは、なぜ重要ですか</span><span class="sxs-lookup"><span data-stu-id="0f5fd-219">Why is this important</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0f5fd-220">列挙されたフィールドを持つ Power BI レポートを作成します。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-220">Create Power BI reports with enumerated fields.</span></span></td>
<td><span data-ttu-id="0f5fd-221">列挙型フィールドを持つ Microsoft Power BI レポートを作成するとき、Power BI Desktop に式を記述し、列挙値をその文字列値に拡張する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-221">When creating Microsoft Power BI reports with enumerated fields, you had to write formulas in Power BI desktop and expand the enumerated values into their string values.</span></span> <span data-ttu-id="0f5fd-222">現在は、列挙されたフィールドがエンティティ格納に展開され、レポートで直接対応するラベル フィールドを使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-222">Now enumerated fields are expanded in Entity store and you can use the corresponding label field directly in your reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0f5fd-223">人事管理向けの 5 つの新しい Power BI コンテンツ パックにアクセス</span><span class="sxs-lookup"><span data-stu-id="0f5fd-223">Access five new Power BI content packs for Human resources</span></span></td>
<td><span data-ttu-id="0f5fd-224">新しいコンテンツ パックは、人事管理組織、人事管理マネージャーによって以下を分析することができます。</span><span class="sxs-lookup"><span data-stu-id="0f5fd-224">The new content packs enable human resource organizations and human resources managers to analyze the following:</span></span>
<p><span data-ttu-id="0f5fd-225">要員指標</span><span class="sxs-lookup"><span data-stu-id="0f5fd-225">Workforce metrics</span></span></p>
<ul>
<li><span data-ttu-id="0f5fd-226">年齢、性別、配偶者の有無などの統計内訳</span><span class="sxs-lookup"><span data-stu-id="0f5fd-226">Demographic breakdowns by age, gender, and marital status</span></span></li>
<li><span data-ttu-id="0f5fd-227">年ごとの減少率を比較し、従業員が組織を退職する理由の一覧を表示</span><span class="sxs-lookup"><span data-stu-id="0f5fd-227">Compare attrition rates year over year and see a list of reasons employees have given for leaving the organization</span></span></li>
<li><span data-ttu-id="0f5fd-228">空いている職位の一覧を参照するとともに、空いている職位と空いていない職位を対比</span><span class="sxs-lookup"><span data-stu-id="0f5fd-228">View a list of open positions, as well as a comparison of open to closed positions</span></span></li>
</ul>
<p><span data-ttu-id="0f5fd-229">報酬と給付金</span><span class="sxs-lookup"><span data-stu-id="0f5fd-229">Compensation and benefits</span></span></p>
<ul>
<li><span data-ttu-id="0f5fd-230">時給払いおよび月給払いの従業員を比較</span><span class="sxs-lookup"><span data-stu-id="0f5fd-230">Compare hourly and salaried employees</span></span></li>
<li><span data-ttu-id="0f5fd-231">福利厚生を受けられる登録された従業員数を表示</span><span class="sxs-lookup"><span data-stu-id="0f5fd-231">View the number of employees enrolled in available benefits</span></span></li>
<li><span data-ttu-id="0f5fd-232">雇用タイプ採用別に従業員を表示</span><span class="sxs-lookup"><span data-stu-id="0f5fd-232">View employees by employment type</span></span></li>
</ul>
<p><span data-ttu-id="0f5fd-233">採用</span><span class="sxs-lookup"><span data-stu-id="0f5fd-233">Recruiting</span></span></p>
<ul>
<li><span data-ttu-id="0f5fd-234">申請者の数、出身地やどの職位を申請しているかに基づいて申請者を分析</span><span class="sxs-lookup"><span data-stu-id="0f5fd-234">Analyze applicants based on the number of applicants, where they're coming from, and what positions they're applying for</span></span></li>
</ul>
<p><span data-ttu-id="0f5fd-235">組織トレーニング</span><span class="sxs-lookup"><span data-stu-id="0f5fd-235">Organizational training</span></span></p>
<ul>
<li><span data-ttu-id="0f5fd-236">場所別のコース登録</span><span class="sxs-lookup"><span data-stu-id="0f5fd-236">Course registration by location</span></span></li>
<li><span data-ttu-id="0f5fd-237">状態別のコースの出席</span><span class="sxs-lookup"><span data-stu-id="0f5fd-237">Couse attendance by status</span></span></li>
<li><span data-ttu-id="0f5fd-238">コースに登録する従業員の一覧</span><span class="sxs-lookup"><span data-stu-id="0f5fd-238">List of employees registered for courses</span></span></li>
</ul>
<p><span data-ttu-id="0f5fd-239">従業員のコンピテンシーと開発</span><span class="sxs-lookup"><span data-stu-id="0f5fd-239">Employee competencies and development</span></span></p>
<ul>
<li><span data-ttu-id="0f5fd-240">従業員が保持するスキルの一覧</span><span class="sxs-lookup"><span data-stu-id="0f5fd-240">List of skills held by employees</span></span></li>
<li><span data-ttu-id="0f5fd-241">チーム メンバー別のスキル タイプの内訳</span><span class="sxs-lookup"><span data-stu-id="0f5fd-241">Breakdown of skill types by team member</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0f5fd-242">追加リソース</span><span class="sxs-lookup"><span data-stu-id="0f5fd-242">Additional resources</span></span>

[<span data-ttu-id="0f5fd-243">Finance and Operations ホーム ページの新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0f5fd-243">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]