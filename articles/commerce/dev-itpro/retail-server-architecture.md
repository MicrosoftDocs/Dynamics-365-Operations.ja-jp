---
title: Commerce Scale Unit アーキテクチャ
description: この記事では、Commerce Scale Unit のアーキテクチャについて説明します。 Commerce Scale Unit は、Modern 販売時点管理 (POS) および E コマース クライアントのステートレス サービスとビジネス ロジックを提供します。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 31521
ms.assetid: 3a169648-592b-4616-9834-598c0244a852
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0a32c63a3db17f3b780aff49c73b01f9fb440f48
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683179"
---
# <a name="commerce-scale-unit-architecture"></a>Commerce Scale Unit アーキテクチャ

[!include [banner](../includes/banner.md)]

この記事では、Commerce Scale Unit のアーキテクチャについて説明します。 Commerce Scale Unit は、Modern 販売時点管理 (MPOS) および E コマース クライアントのステートレス サービスとビジネス ロジックを提供します。

<a name="commerce-scale-unit-architecture"></a>Commerce Scale Unit アーキテクチャ
--------------------------

Commerce Runtime は Commerce Scale Unit レイヤーにラップされます。 Commerce Scale Unit は、タブレットや電話で店舗とオンラインの両方のシン クライアントをサポートするために、Web API および OData を使用します。 Commerce Runtime は、Commerce Data Exchange サービスを通じて Headquarters と通信します。 次の図は、Commerce Scale Unit のアーキテクチャを示しています。 

[![Commerce Scale Unit アーキテクチャ ダイアグラム](./media/retailserver.png)](./media/retailserver.png) 

Commerce Scale Unit は次の概念を使用します。

<table>
<thead>
<tr class="header">
<th>概念</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>エンティティ タイプ</td>
<td>エンティティ タイプは監視するライフ サイクルを持つエンティティです。 各エンティティ タイプには、キーがあります。 エンティティ タイプの例は<strong>顧客</strong>です。</td>
</tr>
<tr class="even">
<td>複合型</td>
<td>複合型は、特定の関連プロパティをグループ化して重複を防止するよう設計された OData 概念です。 これらの関連するプロパティは、複数のエンティティで再利用できます。 たとえば、<strong>顧客</strong>は顧客のアドレスを持つエンティティ タイプです。 この顧客アドレスは、アドレス行、市町村、都道府県、および郵便番号を含むラッパーです。 したがって、<strong>顧客の住所</strong>は、他のエンティティ タイプにより再利用できる複合型です。 たとえば、<strong>注文</strong>エンティティ タイプは、<strong>顧客</strong>エンティティ タイプに関連付けられている同じ住所情報を必要とし、したがって<strong>顧客住所</strong>複合型を再利用します。</td>
</tr>
<tr class="odd">
<td>コントローラー</td>
<td>コントローラーは、エンティティ タイプの作成、読み取り、更新、および削除 (CRUD) の動作とアクションをコントロールするエンティティ タイプのマッピングです。 各 commerce エンティティに、コントローラーが用意されています。 以下のコントローラーをカスタマイズすることができます。
<ul>
<li>カート</li>
<li>カタログ</li>
<li>カテゴリ</li>
<li>コマース</li>
<li>コマース リスト</li>
<li>複合キー エンティティ</li>
<li>コントローラ アセンブリ リゾルバー</li>
<li>顧客</li>
<li>従業員</li>
<li>バインドできないアクション</li>
<li>組織単位</li>
<li>ピッキング リスト</li>
<li>製品</li>
<li>発注書</li>
<li>販売注文</li>
<li>シフト</li>
<li>在庫棚卸仕訳帳</li>
<li>移動オーダー</li>
</ul></td>
</tr>
<tr class="even">
<td>メタデータ</td>
<td>メタデータは、クライアントとサーバーの間の契約を定義します。</td>
</tr>
</tbody>
</table>

自分自身のエンティティ タイプまたは複合タイプを作成して、既存のコントローラーを拡張し、新しいコントローラーを追加し、メタデータをカスタマイズすることができます。 Commerce Runtime をカスタマイズする場合は、Commerce Scale Unit のさまざまなコンポーネントもカスタマイズし、これらの変更を Retail Modern POS クライアントに公開する必要があります。

