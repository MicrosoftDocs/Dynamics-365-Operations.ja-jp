---
title: 固定資産の圧縮記帳の設定
description: この記事は、固定資産の圧縮記帳に関する情報、および固定資産の圧縮記帳を Microsoft Dynamics 365 Finance で設定する方法について説明します。 圧縮記帳は、政府助成金を使用して取得される固定資産の特別な会計処理です。 耐用年数中に、これらの資産の法人所得税を繰延する場合に使用できます。
author: yijialuan
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetReductionEntryMassUpdate_JP, AssetReductionEntryProfile_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 2871
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7dac9e8eca7ff3e181ad6761c93dff9da19f21d3
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772880"
---
# <a name="set-up-reduction-entries-for-fixed-assets"></a>固定資産の圧縮記帳の設定

[!include [banner](../includes/banner.md)]

この記事は、固定資産の圧縮記帳に関する情報、および固定資産の圧縮記帳を設定する方法について説明します。 圧縮記帳は、政府助成金を使用して取得される固定資産の特別な会計処理です。 耐用年数中に、これらの資産の法人所得税を繰延する場合に使用できます。 

政府助成金を使用して固定資産を取得すると、助成は非課税の収益として処理されます。 ただし、すべての政府補助金を収益として説明すると、結果として法人所得税が大きくなり、補助金の助成効果が減少します。 したがって、圧縮記帳と呼ばれる特殊な会計処理が許可されています。 基本的に、圧縮記帳は、取得した固定資産の耐用年数中の法人所得税を延期します。 2 種類の会計処理が許可されています。

-   **直接オフ メソッド** – 政府助成金の金額は、固定資産の取得原価から直接控除されます。
-   **積立メソッド** – 政府助成金の金額は、貸借対照表の株主資本側面の個別の値として管理されます。 政府助成金の金額は、固定資産の正味簿価額に影響を与えません。

圧縮記帳の固定資産転記プロファイルを設定できます。 または**処分**タイプのトランザクションの勘定を設定できます。 圧縮記帳の固定資産を転記する時、トランザクション金額はこれらの勘定から取得されます。

## <a name="prerequisites"></a>必要条件
次の表に、開始する前に準備が整っている必要のある前提条件を示します。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>カテゴリ</th>
<th>前提条件</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>国/地域</td>
<td>法人の基本住所が日本である必要があります。 または、法人のローカライズされた機能の地域が日本である必要があります。</td>
</tr>
<tr class="even">
<td>関連する設定作業</td>
<td><ul>
<li>既定の帳簿、理由コード、および番号順序などの、基本的な固定資産パラメーターを<strong>固定資産パラメーター</strong>ページで確実に設定&#39;します。</li>
<li>固定資産グループを<strong>固定資産グループ</strong>ページで定義します。</li>
<li>減価償却量を転記するための、通貨および丸めルールを設定します。</li>
<li><strong>固定資産の場所</strong>ページで固定資産の場所を設定します。</li>
<li>減価償却の会計カレンダーを設定し、元帳にカレンダーを割り当てます。</li>
<li>固定資産レコードが作成済みであることを確認&#39;します。</li>
<li><strong>帳簿</strong>ページで固定資産に帳簿が設定されていることを確認&#39;します。</li>
</ul></td>
</tr>
</tbody>
</table>

圧縮記帳の機能は、既存の固定資産の機能の最上部に実装されています。 圧縮記帳を使用するには、既存の固定資産の機能の使用に加えて次の作業を行う必要があります。

### <a name="assigning-a-reduction-entry-document-to-a-fixed-asset-book"></a>固定資産帳簿への圧縮記帳ドキュメントの割り当て

**固定資産**ページを使用して固定資産に圧縮記帳ドキュメントを割り当てることができます。

### <a name="assigning-a-reduction-entry-document-to-multiple-fixed-asset-books"></a>圧縮記帳ドキュメントの複数の固定資産帳簿への割り当て

**圧縮記帳の一括更新**ページを使用して、圧縮記帳ドキュメントを複数の固定資産に割り当てます。

### <a name="setting-up-a-fixed-asset-posting-profile-for-reduction-entries"></a>圧縮記帳への固定資産転記プロファイルの設定

**固定資産転記プロファイル** ページを使用して、圧縮記帳の転記プロファイルを設定します。 また、圧縮記帳に適用された資産を減価償却する、転記プロファイルを設定できます。

## <a name="depreciate-fixed-assets-with-reduction-entry-posted"></a>圧縮記帳が転記されている固定資産の減価償却

[圧縮記帳の転記が存在する固定資産の減価償却](./tasks/depreciation-fixed-assets-reduction-entry-posted.md) を参照してください。

## <a name="create-and-assign-a-reduction-entry-document-for-a-government-grant-subsidy"></a>政府助成金の圧縮記帳ドキュメントの作成および割り当て

[政府助成金の圧縮記帳ドキュメントの作成および割り当て](./tasks/create-assign-reduction-document.md)を参照してください。

## <a name="dispose-of-a-fixed-asset-with-reduction-entry"></a>圧縮記帳のある固定資産の処分

[圧縮記帳のある固定資産の処分](./tasks/dispose-fixed-asset-reduction-entry.md)を参照してください


## <a name="technical-information-for-system-administrators"></a>システム管理者向け技術情報
このタスクを完了するために使用するページに対するアクセス権限がない場合は、システム管理者に連絡し、次の表に示される情報を提供します。

| カテゴリ           | 前提条件                                                                                                                                               |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| コンフィギュレーション キー | **資産コンフィギュレーション** キーが、**データ ディクショナリ** &gt; **コンフィギュレーション キー**ノードで使用可能であることを確認します。 |


