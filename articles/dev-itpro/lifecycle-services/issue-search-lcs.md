---
title: "Lifecycle Services (LCS) での問題検索"
description: "この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。 製品の問題と規制機能を検索する方法について説明し、各ステータスに用意されている情報について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 18881
ms.assetid: 160b2882-c70c-44b1-9780-68dc47afb2e8
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: dc24c26ce0fb7d208d3f387a1d6556a4fd63875d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="issue-search-in-lifecycle-services-lcs"></a><span data-ttu-id="65cdb-104">Lifecycle Services (LCS) での問題検索</span><span class="sxs-lookup"><span data-stu-id="65cdb-104">Issue search in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65cdb-105">この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="65cdb-105">This article provides information about the Issue search tool on Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="65cdb-106">製品の問題と規制機能を検索する方法について説明し、各ステータスに用意されている情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="65cdb-106">It explains how to search for product issues and regulatory features, and describes the information that is provided for each status.</span></span>

<a name="prerequisites"></a><span data-ttu-id="65cdb-107">前提条件</span><span class="sxs-lookup"><span data-stu-id="65cdb-107">Prerequisites</span></span>
-------------

<span data-ttu-id="65cdb-108">None</span><span class="sxs-lookup"><span data-stu-id="65cdb-108">None</span></span>

## <a name="search-for-product-issues-and-regulatory-features"></a><span data-ttu-id="65cdb-109">製品の問題や規制機能を検索</span><span class="sxs-lookup"><span data-stu-id="65cdb-109">Search for product issues and regulatory features</span></span>
<span data-ttu-id="65cdb-110">問題検索を使用して製品の問題を検索し、問題が解決済みか、未処理か、または回避方法があるか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-110">You can use Issue search to search for product issues, and determine whether an issue has been resolved, is open, or has a workaround.</span></span> <span data-ttu-id="65cdb-111">また、規制フィーチャーを検索し、フィーチャーが使用可能であるか、または将来のリリースで計画されているか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-111">You can also search for regulatory features, and determine whether a feature is available or is planned in a future release.</span></span> <span data-ttu-id="65cdb-112">最後に、ホワイト ペーパー、認証、および Microsoft Dynamics 365 for Finance and Operations の登録の規制を検索できます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-112">Finally, you can find regulatory white papers, certifications, and registrations for Microsoft Dynamics 365 for Finance and Operations.</span></span>

1.  <span data-ttu-id="65cdb-113">[Microsoft Dynamics Lifecycle Services (LCS) に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="65cdb-113">[Go to Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="65cdb-114">作業するプロジェクトを選択してください。</span><span class="sxs-lookup"><span data-stu-id="65cdb-114">Select a project to work in.</span></span>
3.  <span data-ttu-id="65cdb-115">**問題検索**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-115">Click the **Issue search** tile.</span></span>
4.  <span data-ttu-id="65cdb-116">検索用語を入力します。</span><span class="sxs-lookup"><span data-stu-id="65cdb-116">Enter search terms.</span></span> <span data-ttu-id="65cdb-117">キーワードまたはキーワードのグループ、または Microsoft サポート技術情報 (KB) 番号を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-117">You can enter a keyword or group of keywords, or a Microsoft Knowledge Base (KB) number.</span></span> <span data-ttu-id="65cdb-118">また、ドル記号 ($) を使用してアプリケーション オブジェクト ツリー (AOT) のオブジェクト パスを $\\*ObjectType\\Object* または $\\*ObjectType\\Object*\#*Method* の形式で指定することができます (たとえば、**$\\Classes\\Tax\#Save**)。</span><span class="sxs-lookup"><span data-stu-id="65cdb-118">You can also use a dollar sign ($) to indicate an Application Object Tree (AOT) object path in the format $\\*ObjectType\\Object* or $\\*ObjectType\\Object*\#*Method* (for example, **$\\Classes\\Tax\#Save**).</span></span> <span data-ttu-id="65cdb-119">**AND** や **OR** などの標準検索演算子がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-119">Standard search operators such as **AND** and **OR** are supported.</span></span>

<span data-ttu-id="65cdb-120">解決済みまたは未処理の問題、回避策、および修正されないまたは延期される問題のための結果リストをフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-120">You can filter the results list for resolved or open issues, workarounds, and issues that won't be fixed or are postponed.</span></span> <span data-ttu-id="65cdb-121">また、Finance and Operations のバージョンでフィルター処理することができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-121">You can also filter by the version of Finance and Operations.</span></span> <span data-ttu-id="65cdb-122">既定では、結果は関連別に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-122">By default, the results are sorted by relevance.</span></span> <span data-ttu-id="65cdb-123">ただし、日付の昇順、降順、バージョンの昇順、または降順で並べ替えることができます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-123">However, you can sort by date ascending, date descending, version ascending, or version descending instead.</span></span> <span data-ttu-id="65cdb-124">既定では、すべてのステータスと製品バージョンのフィルターが選択されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-124">By default, all status and product version filters are selected.</span></span> <span data-ttu-id="65cdb-125">**注記:** Microsoft Dynamics AX 2009 の結果は、規制機能を検索する場合にのみ Microsoft Dynamics AX 2012 プロジェクトに含まれます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-125">**Note:** Results for Microsoft Dynamics AX 2009 are included in Microsoft Dynamics AX 2012 projects only when you search for regulatory features.</span></span> <span data-ttu-id="65cdb-126">次のテーブルでは、製品の問題別に検索する際の各ステータスについて提供される情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="65cdb-126">The following table describes the information that is provided for each status when you search by product issue.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65cdb-127">ステータス</span><span class="sxs-lookup"><span data-stu-id="65cdb-127">Status</span></span></th>
<th><span data-ttu-id="65cdb-128">色</span><span class="sxs-lookup"><span data-stu-id="65cdb-128">Color</span></span></th>
<th><span data-ttu-id="65cdb-129">結果の説明</span><span class="sxs-lookup"><span data-stu-id="65cdb-129">Description of results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65cdb-130">解決済</span><span class="sxs-lookup"><span data-stu-id="65cdb-130">Resolved</span></span></td>
<td><span data-ttu-id="65cdb-131">緑</span><span class="sxs-lookup"><span data-stu-id="65cdb-131">Green</span></span></td>
<td><span data-ttu-id="65cdb-132">KB 番号、タイトル、バージョン、問題および変更の説明、および修正プログラムが提供されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-132">The KB number, title, version, description of the problem and change, and hotfix are provided.</span></span> <span data-ttu-id="65cdb-133">修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-133">A list of objects that are affected by the hotfix is also provided whenever possible.</span></span>
<ul>
<li><span data-ttu-id="65cdb-134">修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-134">To download the hotfix, click <strong>Download hotfix</strong>.</span></span></li>
<li><span data-ttu-id="65cdb-135">修正プログラムで変更されたコードを確認するには、<strong>変更を表示</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-135">To determine what code was changed in a hotfix, click <strong>View changes</strong>.</span></span> <span data-ttu-id="65cdb-136">追加されたコードは緑色の強調表示で示され、削除されたコードは赤い強調表示で示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-136">Added code is indicated by a green highlight, and deleted code is indicated by a red highlight.</span></span> <span data-ttu-id="65cdb-137"><strong>重要:</strong> コード変更の一覧は、参考用にのみ提供されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-137"><strong>Important:</strong> The list of code changes is provided for reference only.</span></span> <span data-ttu-id="65cdb-138">コードの変更は、上位の開発レイヤーに手動で挿入しないでください。</span><span class="sxs-lookup"><span data-stu-id="65cdb-138">Code changes should not be manually inserted into a higher development layer.</span></span> <span data-ttu-id="65cdb-139">それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。</span><span class="sxs-lookup"><span data-stu-id="65cdb-139">Otherwise, they become unsupported customized objects that the partner or customer assumes full responsibility for.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65cdb-140">求人開始</span><span class="sxs-lookup"><span data-stu-id="65cdb-140">Open</span></span></td>
<td><span data-ttu-id="65cdb-141">赤</span><span class="sxs-lookup"><span data-stu-id="65cdb-141">Red</span></span></td>
<td><span data-ttu-id="65cdb-142">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-142">A bug number, title, version, and description of the problem are provided.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65cdb-143">回避策</span><span class="sxs-lookup"><span data-stu-id="65cdb-143">Workarounds</span></span></td>
<td><span data-ttu-id="65cdb-144">茶</span><span class="sxs-lookup"><span data-stu-id="65cdb-144">Brown</span></span></td>
<td><span data-ttu-id="65cdb-145">問題番号、タイトル、バージョン、問題の説明、および軽減策が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-145">The issue number, title, version, problem description, and mitigation are provided.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65cdb-146">延期</span><span class="sxs-lookup"><span data-stu-id="65cdb-146">Postponed</span></span></td>
<td><span data-ttu-id="65cdb-147">灰色</span><span class="sxs-lookup"><span data-stu-id="65cdb-147">Gray</span></span></td>
<td><span data-ttu-id="65cdb-148">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-148">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="65cdb-149">この問題の回避策が利用できる場合は、説明されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-149">If a workaround is available, it&#39;s described.</span></span> <span data-ttu-id="65cdb-150">このステータスを持つ不具合は評価されており、現時点では修正されません。</span><span class="sxs-lookup"><span data-stu-id="65cdb-150">A bug that has this status has been evaluated and won&#39;t be fixed at this time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65cdb-151">仕様</span><span class="sxs-lookup"><span data-stu-id="65cdb-151">By design</span></span></td>
<td><span data-ttu-id="65cdb-152">灰色</span><span class="sxs-lookup"><span data-stu-id="65cdb-152">Gray</span></span></td>
<td><span data-ttu-id="65cdb-153">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-153">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="65cdb-154">デザインの説明については可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-154">An explanation of the design is provided whenever possible.</span></span> <span data-ttu-id="65cdb-155">このステータスを持つ不具合が評価され、この機能は設計通りに機能していると判断されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-155">A bug that has this status has been evaluated, and it has been determined that this functionality is working as designed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65cdb-156">再現不可能</span><span class="sxs-lookup"><span data-stu-id="65cdb-156">Not reproducible</span></span></td>
<td><span data-ttu-id="65cdb-157">灰色</span><span class="sxs-lookup"><span data-stu-id="65cdb-157">Gray</span></span></td>
<td><span data-ttu-id="65cdb-158">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-158">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="65cdb-159">問題の説明については可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-159">An explanation of the problem is provided whenever possible.</span></span> <span data-ttu-id="65cdb-160">このステータスを持つ不具合は評価されており、現時点では修正は発行されません。</span><span class="sxs-lookup"><span data-stu-id="65cdb-160">A bug that has this status has been evaluated, and a fix won&#39;t be issued at this time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="65cdb-161">修正されません</span><span class="sxs-lookup"><span data-stu-id="65cdb-161">Will not be fixed</span></span></td>
<td><span data-ttu-id="65cdb-162">灰色</span><span class="sxs-lookup"><span data-stu-id="65cdb-162">Gray</span></span></td>
<td><span data-ttu-id="65cdb-163">バグ番号、タイトル、バージョン、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-163">A bug number, title, version, and description of the problem are provided.</span></span> <span data-ttu-id="65cdb-164">この問題の回避策が利用できる場合は、説明されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-164">If a workaround is available, it&#39;s described.</span></span> <span data-ttu-id="65cdb-165">このステータスを持つ不具合は評価されており、修正されません。</span><span class="sxs-lookup"><span data-stu-id="65cdb-165">A bug that has this status has been evaluated and won&#39;t be fixed.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="65cdb-166">次のテーブルでは、規制機能別に検索する際の各ステータスについて提供される情報について説明します。</span><span class="sxs-lookup"><span data-stu-id="65cdb-166">The following table describes the information that is provided for each status when you search by regulatory feature.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="65cdb-167">ステータス</span><span class="sxs-lookup"><span data-stu-id="65cdb-167">Status</span></span></th>
<th><span data-ttu-id="65cdb-168">色</span><span class="sxs-lookup"><span data-stu-id="65cdb-168">Color</span></span></th>
<th><span data-ttu-id="65cdb-169">結果の説明</span><span class="sxs-lookup"><span data-stu-id="65cdb-169">Description of results</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="65cdb-170">解決済</span><span class="sxs-lookup"><span data-stu-id="65cdb-170">Resolved</span></span></td>
<td><span data-ttu-id="65cdb-171">緑</span><span class="sxs-lookup"><span data-stu-id="65cdb-171">Green</span></span></td>
<td><span data-ttu-id="65cdb-172">機能の更新について: KB 番号、タイトル、バージョン、問題の説明、および修正プログラムが提供されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-172">For feature updates: The KB number, title, version, description of the problem, and hotfix are provided.</span></span> <span data-ttu-id="65cdb-173">修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-173">A list of objects that are affected by the hotfix is also provided whenever possible.</span></span>
<ul>
<li><span data-ttu-id="65cdb-174">修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-174">To download the hotfix, click <strong>Download hotfix</strong>.</span></span></li>
<li><span data-ttu-id="65cdb-175">修正プログラムの KB 記事を読むには、<strong>KB 記事を読む</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-175">To read the KB article for the hotfix, click <strong>Read KB article</strong>.</span></span></li>
</ul>
<span data-ttu-id="65cdb-176">ホワイト ペーパー、証明書、登録、およびレポートについて: ホワイト ペーパーのタイトル、製品バージョン、および説明が用意されており、さらに証明書、登録、またはレポートが用意されています。</span><span class="sxs-lookup"><span data-stu-id="65cdb-176">For white papers, certifications, registrations, and reports: The title, product version, and description of the white paper, certification, registration, or report are provided.</span></span>
<ul>
<li><span data-ttu-id="65cdb-177">ドキュメントを読むには、<strong>ドキュメントを読む</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="65cdb-177">To read the documentation, click <strong>Read documentation</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="65cdb-178">求人開始</span><span class="sxs-lookup"><span data-stu-id="65cdb-178">Open</span></span></td>
<td><span data-ttu-id="65cdb-179">赤</span><span class="sxs-lookup"><span data-stu-id="65cdb-179">Red</span></span></td>
<td><span data-ttu-id="65cdb-180">バグ番号、タイトル、バージョン、予定されているリリース日、および問題の説明が表示されます。</span><span class="sxs-lookup"><span data-stu-id="65cdb-180">A bug number, title, version, planned release date, and description of the problem are provided.</span></span></td>
</tr>
</tbody>
</table>

## <a name="issue-details"></a><span data-ttu-id="65cdb-181">問題の詳細</span><span class="sxs-lookup"><span data-stu-id="65cdb-181">Issue details</span></span>
<span data-ttu-id="65cdb-182">コードの変更は参照用に提供されているため、手動で上位の開発レイヤーに挿入しないでください。</span><span class="sxs-lookup"><span data-stu-id="65cdb-182">The code changes are provided for reference only and should not be manually inserted into a higher development layer.</span></span> <span data-ttu-id="65cdb-183">それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。</span><span class="sxs-lookup"><span data-stu-id="65cdb-183">Otherwise, they become unsupported customized objects that the partner or customer assumes full responsibility for.</span></span>




