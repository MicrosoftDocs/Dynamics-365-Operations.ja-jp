---
title: "原価要素分析コード"
description: "原価計算のコアの柱の 1 つとして、原価要素分析コードは、分類または原価がどこに流れているのかを追跡するために使用されます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f47c75b6f6f4533501070f78698de82cf70f9bd
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="cost-element-dimensions"></a>原価要素分析コード

[!include [banner](../includes/banner.md)]

原価計算のコアの柱の 1 つとして、原価要素分析コードは、分類または原価がどこに流れているのかを追跡するために使用されます。 

要素原価は、勘定科目表で関連する品目原価に対応します。 基本的には、原価が流れる業務の最下位レベルにある任意の要素のタイプがあります。 概念としての原価要素は、勘定科目からすべての原価関連リソースに及びます。 現在、原価会計は勘定科目をサポートします。

## <a name="two-types-of-cost-elements"></a>2 つのタイプの原価要素
原価要素の 2 つのタイプがあります: 主要原価要素と副次原価要素。 次の表では、2 つのタイプの差異について説明します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>主要原価要素</strong></td>
<td><strong>副次原価要素</strong></td>
</tr>
<tr class="even">
<td>主要原価要素は、財務会計から原価計算までの原価の流れを表します。 原価要素構造は、原価要素が主勘定に対応できる総勘定元帳で損益勘定構造に対応します。 業務上のニーズに応じて、すべての主勘定が原価要素として表されるわけではありません。 次の主要原価要素の例があります:
<ul>
<li>売却済商品の原価 (COGs)</li>
<li>間接材料原価</li>
<li>人件費</li>
<li>エネルギー原価</li>
</ul></td>
<td>副次原価要素は、原価計算でのみ作成および使用されるため、内部の原価の流れを表します。 それらを使用して原価のソースが追跡できるセキュリティ保護をします。 これらの原価要素は原価配賦および間接費計算に使用されます。 次の副次原価要素の例があります:
<ul>
<li>生産原価</li>
<li>生産、材料およびマーケティングの間接費</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>原価要素分析コードと原価要素分析コード メンバー
原価要素は、*原価要素分析コード*と呼ばれます。 個別の分析コード値は、*原価要素分析コード メンバー*と呼ばれます。 たとえば、法定レポートの基準となる米国の勘定科目表の構造 (COA) があります。 この COA は、原価要素分析コードとして使用されます。 主要原価要素である勘定は、原価計算の原価要素分析コード メンバーとして表されます。 次のスクリーン ショットは、原価要素分析コード メンバーとしての実際の主勘定である原価要素分析コードとしての主勘定の例を示しています。 

[![原価要素分析コード](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>データ コネクタを使用して原価要素分析コード メンバーのインポート
原価計算の原価要素分析コード メンバーの設定を容易にするために、ビルド済みの、またはカスタム ビルドのいずれかのデータ コネクタを使用して、1 つ以上のソース システムから主要原価要素を取得できます。

## <a name="implementation-considerations"></a>実装の考慮事項
原価要素は原価の詳細の最下位レベルを表すので、原価要素構造を導入する際に、管理レポート作成に必要なすべての原価要素が含まれていることを確認する必要があります。 原価管理の原価要素の適切な番号を見つけることはすることは課題です。 多くの原価要素があると、各原価要素をコントロールすることが難しくなる場合があります。 代わりとして、原価要素をグループ化し、集計レベルで原価管理を管理できます。




