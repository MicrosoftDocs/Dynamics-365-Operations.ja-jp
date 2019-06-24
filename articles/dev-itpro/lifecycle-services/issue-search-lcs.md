---
title: Lifecycle Services (LCS) での問題検索
description: この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。 製品の問題と規制機能を検索する方法について説明し、各ステータスに用意されている情報について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 18881
ms.assetid: 160b2882-c70c-44b1-9780-68dc47afb2e8
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc24c26ce0fb7d208d3f387a1d6556a4fd63875d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544042"
---
# <a name="issue-search-in-lifecycle-services-lcs"></a>Lifecycle Services (LCS) での問題検索

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Dynamics Lifecycle Services (LCS) の問題検索ツールに関する情報を提供します。 製品の問題と規制機能を検索する方法について説明し、各ステータスに用意されている情報について説明します。

<a name="prerequisites"></a>前提条件
-------------

None

## <a name="search-for-product-issues-and-regulatory-features"></a>製品の問題や規制機能を検索
問題検索を使用して製品の問題を検索し、問題が解決済みか、未処理か、または回避方法があるか判断することができます。 また、規制フィーチャーを検索し、フィーチャーが使用可能であるか、または将来のリリースで計画されているか判断することができます。 最後に、ホワイト ペーパー、認証、および Microsoft Dynamics 365 for Finance and Operations の登録の規制を検索できます。

1.  [Microsoft Dynamics Lifecycle Services (LCS) に移動](https://lcs.dynamics.com)
2.  作業するプロジェクトを選択してください。
3.  **問題検索**タイルをクリックします。
4.  検索用語を入力します。 キーワードまたはキーワードのグループ、または Microsoft サポート技術情報 (KB) 番号を入力することができます。 また、ドル記号 ($) を使用してアプリケーション オブジェクト ツリー (AOT) のオブジェクト パスを $\\*ObjectType\\Object* または $\\*ObjectType\\Object*\#*Method* の形式で指定することができます (たとえば、**$\\Classes\\Tax\#Save**)。 **AND** や **OR** などの標準検索演算子がサポートされます。

解決済みまたは未処理の問題、回避策、および修正されないまたは延期される問題のための結果リストをフィルター処理することができます。 また、Finance and Operations のバージョンでフィルター処理することができます。 既定では、結果は関連別に並べ替えられます。 ただし、日付の昇順、降順、バージョンの昇順、または降順で並べ替えることができます。 既定では、すべてのステータスと製品バージョンのフィルターが選択されます。 **注記:** Microsoft Dynamics AX 2009 の結果は、規制機能を検索する場合にのみ Microsoft Dynamics AX 2012 プロジェクトに含まれます。 次のテーブルでは、製品の問題別に検索する際の各ステータスについて提供される情報について説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>ステータス</th>
<th>色</th>
<th>結果の説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>解決済</td>
<td>緑</td>
<td>KB 番号、タイトル、バージョン、問題および変更の説明、および修正プログラムが提供されています。 修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。
<ul>
<li>修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</li>
<li>修正プログラムで変更されたコードを確認するには、<strong>変更を表示</strong> をクリックします。 追加されたコードは緑色の強調表示で示され、削除されたコードは赤い強調表示で示されます。 <strong>重要:</strong> コード変更の一覧は、参考用にのみ提供されています。 コードの変更は、上位の開発レイヤーに手動で挿入しないでください。 それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。</li>
</ul></td>
</tr>
<tr class="even">
<td>求人開始</td>
<td>赤</td>
<td>バグ番号、タイトル、バージョン、および問題の説明が表示されます。</td>
</tr>
<tr class="odd">
<td>回避策</td>
<td>茶</td>
<td>問題番号、タイトル、バージョン、問題の説明、および軽減策が表示されます。</td>
</tr>
<tr class="even">
<td>延期</td>
<td>灰色</td>
<td>バグ番号、タイトル、バージョン、および問題の説明が表示されます。 この問題の回避策が利用できる場合は、説明&#39;されています。 このステータスを持つ不具合は評価されており、現時点では修正されません&#39;。</td>
</tr>
<tr class="odd">
<td>仕様</td>
<td>灰色</td>
<td>バグ番号、タイトル、バージョン、および問題の説明が表示されます。 デザインの説明については可能な場合に提供されます。 このステータスを持つ不具合が評価され、この機能は設計通りに機能していると判断されています。</td>
</tr>
<tr class="even">
<td>再現不可能</td>
<td>灰色</td>
<td>バグ番号、タイトル、バージョン、および問題の説明が表示されます。 問題の説明については可能な場合に提供されます。 このステータスを持つ不具合は評価されており、現時点では修正は発行されません&#39;。</td>
</tr>
<tr class="odd">
<td>修正されません</td>
<td>灰色</td>
<td>バグ番号、タイトル、バージョン、および問題の説明が表示されます。 この問題の回避策が利用できる場合は、説明&#39;されています。 このステータスを持つ不具合は評価されており、修正されません&#39;。</td>
</tr>
</tbody>
</table>

次のテーブルでは、規制機能別に検索する際の各ステータスについて提供される情報について説明します。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>ステータス</th>
<th>色</th>
<th>結果の説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>解決済</td>
<td>緑</td>
<td>機能の更新について: KB 番号、タイトル、バージョン、問題の説明、および修正プログラムが提供されています。 修正プログラムの影響を受けるオブジェクトの一覧については、可能な場合に提供されます。
<ul>
<li>修正プログラムをダウンロードするには、<strong>修正プログラムをダウンロード</strong> をクリックします。</li>
<li>修正プログラムの KB 記事を読むには、<strong>KB 記事を読む</strong> をクリックします。</li>
</ul>
ホワイト ペーパー、証明書、登録、およびレポートについて: ホワイト ペーパーのタイトル、製品バージョン、および説明が用意されており、さらに証明書、登録、またはレポートが用意されています。
<ul>
<li>ドキュメントを読むには、<strong>ドキュメントを読む</strong> をクリックします。</li>
</ul></td>
</tr>
<tr class="even">
<td>求人開始</td>
<td>赤</td>
<td>バグ番号、タイトル、バージョン、予定されているリリース日、および問題の説明が表示されます。</td>
</tr>
</tbody>
</table>

## <a name="issue-details"></a>問題の詳細
コードの変更は参照用に提供されているため、手動で上位の開発レイヤーに挿入しないでください。 それ以外の場合、パートナーまたは顧客がすべて責任を負うと想定される、サポートされていないカスタマイズされたオブジェクトとなります。



