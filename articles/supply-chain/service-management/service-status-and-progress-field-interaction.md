---
title: サービスのステータスと進捗状況フィールドの相互作用
description: サービス注文フォームでは、サービス注文ヘッダーの進捗状況フィールドがサービス注文全体のステータスを反映し、ステータス レポートが個々のサービス注文明細行のステータスを示します。
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e83df9ca8ee19b5e29d4eccf2bd883ee6ddff62
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677649"
---
# <a name="service-status-and-progress-field-interaction"></a>サービスのステータスと進捗状況フィールドの相互作用

[!include [banner](../includes/banner.md)]

**ステータス** では、サービス注文ヘッダーの **進捗状況** フィールドがサービス注文全体のステータスを反映し、**ステータス** レポートが個々のサービス注文明細行のステータスを示します。

<table>
<colgroup>
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>進捗状況</p></th>
<th><p>明細行 1 のステータス</p></th>
<th><p>明細行 2 のステータス</p></th>
<th><p>明細行 3 のステータス</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>進行中</strong></p></td>
<td><p><strong>作成済</strong></p></td>
<td><p><strong>作成済</strong></p></td>
<td><p><strong>作成済</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>進行中</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>作成済</strong></p></td>
<td><p><strong>作成済</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>進行中</strong></p></td>
<td><p><strong>作成済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>転記済</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>転記済</strong></p></td>
<td><p><strong>転記済</strong></p></td>
<td><p><strong>転記済</strong></p></td>
<td><p><strong>転記済</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>転記済</strong></p></td>
<td><p><strong>転記済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
<td><p><strong>キャンセル済</strong></p></td>
</tr>
</tbody>
</table>

すべての明細行のステータスが **作成済** の場合、サービス注文の進捗状況は進行中であり、一部の明細行のステータスが **キャンセル済** または **転記済** の場合も進行中です。

サービス注文のすべての明細行が **転記済** とマークされている場合、サービス注文の進捗状況は **転記済** です。 一部の明細行が **転記済** で、一部の明細行が **キャンセル済** の場合も、進捗状況は **転記済** です。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
