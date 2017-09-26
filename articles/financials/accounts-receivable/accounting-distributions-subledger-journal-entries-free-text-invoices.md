---
title: "自由書式の請求書の勘定配布と補助元帳仕訳"
description: "勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義するために使用されます。 自由書式の請求書が仕訳されたときに計上する必要のあるすべての金額に勘定配布があります。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b530b5c8b5e252efb253dcf5b4ad080e2f646e5f
ms.contentlocale: ja-jp
ms.lasthandoff: 05/25/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a>自由書式の請求書の勘定配布と補助元帳仕訳

[!include[banner](../includes/banner.md)]


勘定配布は収益、税金、雑費などの金額がどのように自由書式の請求書に計上されるかを定義するために使用されます。 自由書式の請求書が仕訳されたときに計上する必要のあるすべての金額に勘定配布があります。

<a name="accounting-distributions"></a>勘定配布
------------------------

自由書式の請求書ページで次のボタンを使用して、自由書式の請求の各金額の勘定配布を表示すること、また場合によっては変更することができます。

-   **金額の配分**—税または請求金額などの明細行と子明細行の勘定配布を表示または変更します。 売上税トランザクション ページまたは諸費用トランザクション ページから子明細行の勘定配布を直接表示または変更することもできます。
    -   請求金額または通貨の丸めなど、自由書式の請求書ヘッダーの金額を変更します。
    -   自由書式の請求明細行金額を変更します。
-   **配分の表示**—すべての伝票の明細行の勘定配布を表示します。 このビューで勘定配布を変更できません。
    -   表示のヘッダーと明細金額。

## <a name="distributing-amounts"></a>金額の配分
自由書式の請求書を入力すると、各金額は次のように配分されます。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>金額のタイプ</th>
<th>主勘定の表示元</th>
<th>表示される既定の財務分析コードを決定する優先順位</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>自由書式の請求明細行</td>
<td>自由書式の請求明細行の勘定科目。</td>
<td><ol>
<li>主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</li>
<li>主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</li>
<li>自由書式の請求明細行の既定の財務分析コードの値を使用します。</li>
<li>勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</li>
</ol></td>
</tr>
<tr class="even">
<td>固定資産番号と価値モデルの組み合わせの自由書式の請求明細行
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>メモ </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>自由書式の請求明細行の主勘定は固定資産の処分勘定になります。</td>
</tr>
</tbody>
</table>
</div></td>
<td>自由書式の請求明細行の勘定科目。</td>
<td><ol>
<li>自由書式の請求明細行の既定の財務分析コードの値を使用します。</li>
<li>勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</li>
</ol></td>
</tr>
<tr class="odd">
<td>自由書式の請求書の割引金額</td>
<td>現金割引ページの [顧客割引の主勘定] フィールド。</td>
<td><ol>
<li>主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</li>
<li>主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</li>
<li>自由書式の請求明細行の既定の財務分析コードの値を使用します。</li>
<li>勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</li>
</ol></td>
</tr>
<tr class="even">
<td>自由書式の請求書の売上税金額</td>
<td>元帳転記グループ ページの [売上税支払] フィールド。</td>
<td><ol>
<li>自由書式の請求明細行金額または費用明細金額の配賦で定義された財務分析コードを使用します。</li>
<li>自由書式の請求明細行の既定の財務分析コードの値を使用します。</li>
<li>勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</li>
</ol></td>
</tr>
<tr class="odd">
<td>自由書式の請求書の費用明細金額</td>
<td>諸費用コード ページの [貸方勘定] フィールド。</td>
<td><ol>
<li>主勘定が配賦勘定の場合、配賦勘定定義の既定値を使用します。</li>
<li>主勘定が配賦勘定でない場合は、自由書式の請求明細行の財務分析コードの既定のテンプレートを使用します。</li>
<li>自由書式の請求明細行の既定の財務分析コードの値を使用します。</li>
<li>勘定科目表ページで、勘定科目の既定の財務分析コードの値を使用します。</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>税の配分
税金の勘定配布は、税金が計算されるまで作成できません。 売上税を計算するには、[自由書式の請求書] フォームで次の作業のいずれかを完了する必要があります。
-   売上税を表示する。
-   請求金額の合計を表示する。
-   キャッシュ フローを表示する。
-   自由書式の請求書全体の勘定配布を表示する。
-   補助元帳を表示する。

## <a name="subledger-journals-for-free-text-invoices"></a>自由書式の請求書の補助元帳
自由書式の請求書を転記する前に、請求書が適切な勘定に転記されることを保証するために借方と貸方が含まれる請求書の完全な勘定項目を表示できます。 全勘定項目の表示は補助元帳と呼ばれます。 自由書式の請求書を仕訳入力する前に、プレビューした結果、補助元帳仕訳が正しくない場合、補助元帳仕訳は変更できません。 代わりに、勘定配布または転記プロファイルを変更する必要があります。 勘定配布は、勘定項目の借方または貸方のいずれか一方を定義するために使用されます。 相殺補助元帳仕訳勘定項目は、顧客勘定または税などの転記プロファイルから作成されます。




