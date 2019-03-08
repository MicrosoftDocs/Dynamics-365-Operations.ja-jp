---
title: Dynamics AX application version 7.0.1 (2016 年 5 月) の新機能および変更された機能
description: この記事では、Microsoft Dynamics AX application version 7.0.1 の新機能および変更された機能について説明します。 このバージョンは、2016 年 5 月にリリースされ、7.0.1265.23014 のビルド番号を持ちます。
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c830952b5d9e4887a816b5ab66d0944bddf5b505
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "314512"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="7e960-104">Dynamics AX application version 7.0.1 (2016 年 5 月) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="7e960-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e960-105">この記事では、Microsoft Dynamics AX application version 7.0.1 の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e960-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="7e960-106">このバージョンは、2016 年 5 月にリリースされ、7.0.1265.23014 のビルド番号を持ちます。</span><span class="sxs-lookup"><span data-stu-id="7e960-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="7e960-107">電子申告 (ER)</span><span class="sxs-lookup"><span data-stu-id="7e960-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="7e960-108">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="7e960-108">What can you do?</span></span> | <span data-ttu-id="7e960-109">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="7e960-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="7e960-110">ユーザーが必要な財務分析コードを選択するために、電子申告 (ER) レポートをデザインするための実行時間のダイアログ ボックスをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7e960-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="7e960-111">ER レポートを実行するためのダイアログ ボックスでは、実行時にユーザーが複数の財務分析コードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="7e960-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="7e960-112">選択した財務分析コードの詳細は、生成される電子ドキュメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="7e960-113">目的のデータ ソースへの単一のマッピングを介して、ER レポートのデザイン時に複数の財務分析コードへのアクセスをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7e960-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="7e960-114">ユーザーが選択するか、現在の法人またはインスタンス用にコンフィギュレーションするかによる財務分析コードの数に関係なく、財務分析コードの詳細と共にトランザクション データを表示する電子ドキュメントを生成するのには、同じ ER レポートのコンフィギュレーションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e960-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="7e960-115">OPENXML ワークシート形式で作成した電子文書の動的に生成された列にデータを入力するため、ER レポートをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="7e960-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="7e960-116">ER レポートでは、水平方向に複製された列を使用して、生成された OPENXML ワークシートにデータを入力します。</span><span class="sxs-lookup"><span data-stu-id="7e960-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="7e960-117">したがって、同じ ER レポートのコンフィギュレーションは、動的に生成された列の数が異なる電子ドキュメントを生成するために再利用できます。</span><span class="sxs-lookup"><span data-stu-id="7e960-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="7e960-118">形式の出力結果が特定の送信先に指定されるように ER の送信先をコンフィギュレーションします。ファイル、電子メール、またはアーカイブ (Microsoft SharePoint フォルダーまたは Microsoft Azure ストレージ)。</span><span class="sxs-lookup"><span data-stu-id="7e960-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="7e960-119">以前は、ER コンフィギュレーションを実行したときに、ユーザーはメッセージ ボックスに保存したりファイルを開く必要がありました。</span><span class="sxs-lookup"><span data-stu-id="7e960-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="7e960-120">現在は各形式のコンフィギュレーション、および各出力のコンポーネント (フォルダやファイル) の出力先を別々に事前にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="7e960-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="7e960-121">適切なアクセス権を持っているユーザーは、実行時に送信先の設定を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="7e960-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="7e960-122">POS – Microsoft Dynamics AX 小売</span><span class="sxs-lookup"><span data-stu-id="7e960-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="7e960-123">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="7e960-123">What can you do?</span></span> | <span data-ttu-id="7e960-124">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="7e960-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="7e960-125">Google Chrome ブラウザーを使用します。</span><span class="sxs-lookup"><span data-stu-id="7e960-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="7e960-126">小売業者は、クロム ブラウザーからクラウド POS を起動でき、クラウド POS の Microsoft Edge および Internet Explorer バージョンで利用可能なすべての機能を経験することができます。</span><span class="sxs-lookup"><span data-stu-id="7e960-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="7e960-127">財務報告</span><span class="sxs-lookup"><span data-stu-id="7e960-127">Financial reporting</span></span>

| <span data-ttu-id="7e960-128">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="7e960-128">What can you do?</span></span> | <span data-ttu-id="7e960-129">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="7e960-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="7e960-130">財務レポートのデータ マートを再構築します。</span><span class="sxs-lookup"><span data-stu-id="7e960-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="7e960-131">Dynamics AX データベースを環境間で移動したり、Dynamics AX 環境への他の侵害となる変更をする場合、財務レポート データベースを再構築する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e960-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="7e960-132">その再構築をするために Windows PowerShell スクリプトが提供されています。</span><span class="sxs-lookup"><span data-stu-id="7e960-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="7e960-133">有効ではないレポート デザイナー オプションを選択する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7e960-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="7e960-134">Management Reporter の市場バージョンで使用されていたいくつかのレポート デザイナー オプションは、この Dynamics AX バージョンには適用されません。</span><span class="sxs-lookup"><span data-stu-id="7e960-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="7e960-135">これらのオプションは、財務諸表のデザイン、出力、およびリンクに関連していました。</span><span class="sxs-lookup"><span data-stu-id="7e960-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="7e960-136">これらのオプションは、ユーザーによるエラーを防ぐために財務諸表デザイナーから削除されました。</span><span class="sxs-lookup"><span data-stu-id="7e960-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="7e960-137">財務管理</span><span class="sxs-lookup"><span data-stu-id="7e960-137">Financial management</span></span>

| <span data-ttu-id="7e960-138">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="7e960-138">What can you do?</span></span> | <span data-ttu-id="7e960-139">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="7e960-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="7e960-140">買掛金勘定支払の確認後支払ファイルを生成します。</span><span class="sxs-lookup"><span data-stu-id="7e960-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="7e960-141">確認後支払ファイルは小切手の不正を禁止するのに役立つよう生成されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="7e960-142">倉庫および生産</span><span class="sxs-lookup"><span data-stu-id="7e960-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7e960-143">何ができますか。</span><span class="sxs-lookup"><span data-stu-id="7e960-143">What can you do?</span></span></th>
<th><span data-ttu-id="7e960-144">これは、なぜ重要ですか。</span><span class="sxs-lookup"><span data-stu-id="7e960-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7e960-145">特定の場所で一連の製品を作成する作業を管理するための倉庫作業ポリシーを定義します。</span><span class="sxs-lookup"><span data-stu-id="7e960-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="7e960-146">倉庫のプロセスは常に作業を含みません。</span><span class="sxs-lookup"><span data-stu-id="7e960-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="7e960-147">新しい倉庫作業ポリシーを使用して、原材料のピッキング用に作成される作業、および特定の場所での一連の製品に対する完成品のプット アウェイを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="7e960-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e960-148">生産出荷の場所がライセンス プレートにより制御されていないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="7e960-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="7e960-149">これにより生産出荷の場所がライセンス プレートにより制御されていないことを指定できます。</span><span class="sxs-lookup"><span data-stu-id="7e960-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="7e960-150">この機能はたとえば、上流製造オーダー品目が下流製造オーダーの生産入荷の場所として機能する場所に直接完了を報告するとき、便利です。</span><span class="sxs-lookup"><span data-stu-id="7e960-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e960-151">同じ品目でさまざまな製品分析コードを持つ品目を含む BOM をサポートします。</span><span class="sxs-lookup"><span data-stu-id="7e960-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="7e960-152">実稼動環境で 1 つまたは複数の製品分析コードを使用している場合、同じ品目の異なるバリアントに基づいて、品目を生産したい状況を手に入れることができます。</span><span class="sxs-lookup"><span data-stu-id="7e960-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="7e960-153">詳細については、<a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">このブログ</a>を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7e960-153">For more information, see <a href="https://blogs.msdn.microsoft.com/axmfg/2015/12/22/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item/">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e960-154">BOM の最初のレベルでの循環構造による製造オーダーは、原材料リソースを計画するための BOM レベルの計算から除外されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="7e960-155">BOM 階層で循環を引き起こす製造オーダーの製品バリアントには、適切な BOM レベルを割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="7e960-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7e960-156">原材料リソースの計画および原価計算のため、個別の BOM レベルを計算します。</span><span class="sxs-lookup"><span data-stu-id="7e960-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="7e960-157">原材料リソースを計画するため、BOM レベルは新しい <strong>ReqItemLevel</strong> テーブルで計算されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="7e960-158">終了した製造オーダーは、計算で無視されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="7e960-159">製造原価計算のため、BOM レベルは <strong>InventTable</strong> で計算されます。</span><span class="sxs-lookup"><span data-stu-id="7e960-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="7e960-160">終了した製造オーダーは、計算で含められます。</span><span class="sxs-lookup"><span data-stu-id="7e960-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="7e960-161">原材料リソース計画、たとえば、マスター プランの計画のスケジューリングと展開を実行する場合、原材料リソースを計画するために使用される BOM レベルのみ再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e960-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="7e960-162">つまり、製造原価計算に使用される BOM レベルを計算する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7e960-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="7e960-163">たとえば、在庫原価計算のような原価操作を実行している場合、製造原価計算に使用される BOM レベルのみ再計算する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e960-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="7e960-164">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="7e960-164">Additional resources</span></span>

[<span data-ttu-id="7e960-165">新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="7e960-165">What's new or changed</span></span>](whats-new-changed.md)

[<span data-ttu-id="7e960-166">新規または更新されたタスク ガイド (2016年 5月)</span><span class="sxs-lookup"><span data-stu-id="7e960-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)
