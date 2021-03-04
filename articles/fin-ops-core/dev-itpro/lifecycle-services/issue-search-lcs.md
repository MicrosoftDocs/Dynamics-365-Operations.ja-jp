---
title: Lifecycle Services (LCS) での問題検索
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 18881
ms.assetid: 160b2882-c70c-44b1-9780-68dc47afb2e8
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5681be8582994b36484b261d1e5fddeb240b98c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129961"
---
# <a name="issue-search-in-lifecycle-services-lcs"></a><span data-ttu-id="e206f-103">Lifecycle Services (LCS) での問題検索</span><span class="sxs-lookup"><span data-stu-id="e206f-103">Issue search in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e206f-104">この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e206f-104">This article provides information about the Issue search tool on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="e206f-105">製品の問題と規制機能を検索する方法について説明し、各ステータスに用意されている情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="e206f-105">It explains how to search for product issues and regulatory features, and describes the information that is provided for each status.</span></span>

<a name="prerequisites"></a><span data-ttu-id="e206f-106">前提条件</span><span class="sxs-lookup"><span data-stu-id="e206f-106">Prerequisites</span></span>
-------------

<span data-ttu-id="e206f-107">None</span><span class="sxs-lookup"><span data-stu-id="e206f-107">None</span></span>

## <a name="search-for-product-issues-and-regulatory-features"></a><span data-ttu-id="e206f-108">製品の問題や規制機能を検索</span><span class="sxs-lookup"><span data-stu-id="e206f-108">Search for product issues and regulatory features</span></span>
<span data-ttu-id="e206f-109">問題検索を使用して製品の問題を検索し、問題が解決済みか、未処理か、または回避方法があるか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="e206f-109">You can use Issue search to search for product issues, and determine whether an issue has been resolved, is open, or has a workaround.</span></span> <span data-ttu-id="e206f-110">また、規制フィーチャーを検索し、フィーチャーが使用可能であるか、または将来のリリースで計画されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="e206f-110">You can also search for regulatory features, and determine whether a feature is available or is planned in a future release.</span></span> <span data-ttu-id="e206f-111">最後に、ホワイト ペーパー、認証、および登録の規制を検索できます。</span><span class="sxs-lookup"><span data-stu-id="e206f-111">Finally, you can find regulatory white papers, certifications, and registrations.</span></span>

1.  <span data-ttu-id="e206f-112">[Microsoft Dynamics Lifecycle Services (LCS) に移動](https://lcs.dynamics.com)</span><span class="sxs-lookup"><span data-stu-id="e206f-112">[Go to Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="e206f-113">作業するプロジェクトを選択してください。</span><span class="sxs-lookup"><span data-stu-id="e206f-113">Select a project to work in.</span></span>
3.  <span data-ttu-id="e206f-114">**問題検索** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-114">Click the **Issue search** tile.</span></span>
4.  <span data-ttu-id="e206f-115">検索用語を入力します。</span><span class="sxs-lookup"><span data-stu-id="e206f-115">Enter search terms.</span></span> <span data-ttu-id="e206f-116">キーワードまたはキーワードのグループ、または Microsoft サポート技術情報 (KB) 番号を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="e206f-116">You can enter a keyword or group of keywords, or a Microsoft Knowledge Base (KB) number.</span></span> <span data-ttu-id="e206f-117">また、ドル記号 ($) を使用してアプリケーション オブジェクト ツリー (AOT) のオブジェクト パスを $\\*ObjectType\\Object* または $\\*ObjectType\\Object*\#*Method* の形式で指定することができます (たとえば、**$\\Classes\\Tax\#Save**)。</span><span class="sxs-lookup"><span data-stu-id="e206f-117">You can also use a dollar sign ($) to indicate an Application Object Tree (AOT) object path in the format $\\*ObjectType\\Object* or $\\*ObjectType\\Object*\#*Method* (for example, **$\\Classes\\Tax\#Save**).</span></span> <span data-ttu-id="e206f-118">**AND** や **OR** などの標準検索演算子がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e206f-118">Standard search operators such as **AND** and **OR** are supported.</span></span>

<span data-ttu-id="e206f-119">解決済みまたは未処理の問題、回避策、および修正されないまたは延期される問題のための結果リストをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="e206f-119">You can filter the results list for resolved or open issues, workarounds, and issues that won't be fixed or are postponed.</span></span> <span data-ttu-id="e206f-120">また、アプリケーション バージョンでフィルタ処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="e206f-120">You can also filter by the application version.</span></span> <span data-ttu-id="e206f-121">既定では、結果は関連別に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="e206f-121">By default, the results are sorted by relevance.</span></span> <span data-ttu-id="e206f-122">ただし、日付の昇順、降順、バージョンの昇順、または降順で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="e206f-122">However, you can sort by date ascending, date descending, version ascending, or version descending instead.</span></span> <span data-ttu-id="e206f-123">既定では、すべてのステータスと製品バージョンのフィルターが選択されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-123">By default, all status and product version filters are selected.</span></span> <span data-ttu-id="e206f-124">**注記:** Microsoft Dynamics AX 2009 の結果は、規制機能を検索する場合にのみ Microsoft Dynamics AX 2012 プロジェクトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="e206f-124">**Note:** Results for Microsoft Dynamics AX 2009 are included in Microsoft Dynamics AX 2012 projects only when you search for regulatory features.</span></span> <span data-ttu-id="e206f-125">次のテーブルでは、製品の問題別に検索する際の各ステータスについて提供される情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="e206f-125">The following table describes the information that is provided for each status when you search by product issue.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e206f-126">ステータス</span><span class="sxs-lookup"><span data-stu-id="e206f-126">Status</span></span></th>
<th><span data-ttu-id="e206f-127">色</span><span class="sxs-lookup"><span data-stu-id="e206f-127">Color</span></span></th>
<th><span data-ttu-id="e206f-128">結果の説明</span><span class="sxs-lookup"><span data-stu-id="e206f-128">Description of results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e206f-129">解決済</span><span class="sxs-lookup"><span data-stu-id="e206f-129">Resolved</span></span></td>
<td><span data-ttu-id="e206f-130">緑</span><span class="sxs-lookup"><span data-stu-id="e206f-130">Green</span></span></td>
<td><span data-ttu-id="e206f-131">KB 番号、タイトル、バージョン、問題および変更の説明、および修正プログラムが提供されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-131">The KB number, title, version, description of the problem and change, and hotfix are provided.</span></span> <span data-ttu-id="e206f-132">修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-132">A list of objects that are affected by the hotfix is also provided whenever possible.</span></span>
<ul>
<li><span data-ttu-id="e206f-133">修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-133">To download the hotfix, click <strong>Download hotfix</strong>.</span></span></li>
<li><span data-ttu-id="e206f-134">修正プログラムで変更されたコードを確認するには、<strong>変更を表示</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-134">To determine what code was changed in a hotfix, click <strong>View changes</strong>.</span></span> <span data-ttu-id="e206f-135">追加されたコードは緑色の強調表示で示され、削除されたコードは赤い強調表示で示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-135">Added code is indicated by a green highlight, and deleted code is indicated by a red highlight.</span></span> <span data-ttu-id="e206f-136"><strong>重要:</strong> コード変更の一覧は、参考用にのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-136"><strong>Important:</strong> The list of code changes is provided for reference only.</span></span> <span data-ttu-id="e206f-137">コードの変更は、上位の開発レイヤーに手動で挿入しないでください。</span><span class="sxs-lookup"><span data-stu-id="e206f-137">Code changes should not be manually inserted into a higher development layer.</span></span> <span data-ttu-id="e206f-138">それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。</span><span class="sxs-lookup"><span data-stu-id="e206f-138">Otherwise, they become unsupported customized objects that the partner or customer assumes full responsibility for.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e206f-139">求人開始</span><span class="sxs-lookup"><span data-stu-id="e206f-139">Open</span></span></td>
<td><span data-ttu-id="e206f-140">赤</span><span class="sxs-lookup"><span data-stu-id="e206f-140">Red</span></span></td>
<td><span data-ttu-id="e206f-141">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-141">A bug number, title, version, and description of the problem are provided.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e206f-142">回避策</span><span class="sxs-lookup"><span data-stu-id="e206f-142">Workarounds</span></span></td>
<td><span data-ttu-id="e206f-143">茶</span><span class="sxs-lookup"><span data-stu-id="e206f-143">Brown</span></span></td>
<td><span data-ttu-id="e206f-144">問題番号、タイトル、バージョン、問題の説明、および軽減策が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-144">The issue number, title, version, problem description, and mitigation are provided.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e206f-145">延期</span><span class="sxs-lookup"><span data-stu-id="e206f-145">Postponed</span></span></td>
<td><span data-ttu-id="e206f-146">灰色</span><span class="sxs-lookup"><span data-stu-id="e206f-146">Gray</span></span></td>
<td><span data-ttu-id="e206f-147">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-147">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="e206f-148">この問題の回避策が利用できる場合は、説明&#39;されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-148">If a workaround is available, it&#39;s described.</span></span> <span data-ttu-id="e206f-149">このステータスを持つ不具合は評価されており、現時点では修正されません&#39;。</span><span class="sxs-lookup"><span data-stu-id="e206f-149">A bug that has this status has been evaluated and won&#39;t be fixed at this time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e206f-150">仕様</span><span class="sxs-lookup"><span data-stu-id="e206f-150">By design</span></span></td>
<td><span data-ttu-id="e206f-151">灰色</span><span class="sxs-lookup"><span data-stu-id="e206f-151">Gray</span></span></td>
<td><span data-ttu-id="e206f-152">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-152">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="e206f-153">デザインの説明については可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-153">An explanation of the design is provided whenever possible.</span></span> <span data-ttu-id="e206f-154">このステータスを持つ不具合が評価され、この機能は設計通りに機能していると判断されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-154">A bug that has this status has been evaluated, and it has been determined that this functionality is working as designed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e206f-155">再現不可能</span><span class="sxs-lookup"><span data-stu-id="e206f-155">Not reproducible</span></span></td>
<td><span data-ttu-id="e206f-156">灰色</span><span class="sxs-lookup"><span data-stu-id="e206f-156">Gray</span></span></td>
<td><span data-ttu-id="e206f-157">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-157">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="e206f-158">問題の説明については可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-158">An explanation of the problem is provided whenever possible.</span></span> <span data-ttu-id="e206f-159">このステータスを持つ不具合は評価されており、現時点では修正は発行されません&#39;。</span><span class="sxs-lookup"><span data-stu-id="e206f-159">A bug that has this status has been evaluated, and a fix won&#39;t be issued at this time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e206f-160">修正されません</span><span class="sxs-lookup"><span data-stu-id="e206f-160">Will not be fixed</span></span></td>
<td><span data-ttu-id="e206f-161">灰色</span><span class="sxs-lookup"><span data-stu-id="e206f-161">Gray</span></span></td>
<td><span data-ttu-id="e206f-162">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-162">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="e206f-163">この問題の回避策が利用できる場合は、説明&#39;されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-163">If a workaround is available, it&#39;s described.</span></span> <span data-ttu-id="e206f-164">このステータスを持つ不具合は評価されており、修正されません&#39;。</span><span class="sxs-lookup"><span data-stu-id="e206f-164">A bug that has this status has been evaluated and won&#39;t be fixed.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e206f-165">次のテーブルでは、規制機能別に検索する際の各ステータスについて提供される情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="e206f-165">The following table describes the information that is provided for each status when you search by regulatory feature.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e206f-166">ステータス</span><span class="sxs-lookup"><span data-stu-id="e206f-166">Status</span></span></th>
<th><span data-ttu-id="e206f-167">色</span><span class="sxs-lookup"><span data-stu-id="e206f-167">Color</span></span></th>
<th><span data-ttu-id="e206f-168">結果の説明</span><span class="sxs-lookup"><span data-stu-id="e206f-168">Description of results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e206f-169">解決済</span><span class="sxs-lookup"><span data-stu-id="e206f-169">Resolved</span></span></td>
<td><span data-ttu-id="e206f-170">緑</span><span class="sxs-lookup"><span data-stu-id="e206f-170">Green</span></span></td>
<td><span data-ttu-id="e206f-171">機能の更新について: KB 番号、タイトル、バージョン、問題の説明、および修正プログラムが提供されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-171">For feature updates: The KB number, title, version, description of the problem, and hotfix are provided.</span></span> <span data-ttu-id="e206f-172">修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-172">A list of objects that are affected by the hotfix is also provided whenever possible.</span></span>
<ul>
<li><span data-ttu-id="e206f-173">修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-173">To download the hotfix, click <strong>Download hotfix</strong>.</span></span></li>
<li><span data-ttu-id="e206f-174">修正プログラムの KB 記事を読むには、<strong>KB 記事を読む</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-174">To read the KB article for the hotfix, click <strong>Read KB article</strong>.</span></span></li>
</ul>
<span data-ttu-id="e206f-175">ホワイト ペーパー、証明書、登録、およびレポートについて: ホワイト ペーパーのタイトル、製品バージョン、および説明が用意されており、さらに証明書、登録、またはレポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e206f-175">For white papers, certifications, registrations, and reports: The title, product version, and description of the white paper, certification, registration, or report are provided.</span></span>
<ul>
<li><span data-ttu-id="e206f-176">ドキュメントを読むには、<strong>ドキュメントを読む</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e206f-176">To read the documentation, click <strong>Read documentation</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e206f-177">求人開始</span><span class="sxs-lookup"><span data-stu-id="e206f-177">Open</span></span></td>
<td><span data-ttu-id="e206f-178">赤</span><span class="sxs-lookup"><span data-stu-id="e206f-178">Red</span></span></td>
<td><span data-ttu-id="e206f-179">バグ番号、タイトル、バージョン、予定されているリリース日、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e206f-179">A bug number, title, version, planned release date, and description of the problem are provided.</span></span></td>
</tr>
</tbody>
</table>

## <a name="issue-details"></a><span data-ttu-id="e206f-180">問題の詳細</span><span class="sxs-lookup"><span data-stu-id="e206f-180">Issue details</span></span>
<span data-ttu-id="e206f-181">コードの変更は参照用に提供されているため、手動で上位の開発レイヤーに挿入しないでください。</span><span class="sxs-lookup"><span data-stu-id="e206f-181">The code changes are provided for reference only and should not be manually inserted into a higher development layer.</span></span> <span data-ttu-id="e206f-182">それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。</span><span class="sxs-lookup"><span data-stu-id="e206f-182">Otherwise, they become unsupported customized objects that the partner or customer assumes full responsibility for.</span></span>



