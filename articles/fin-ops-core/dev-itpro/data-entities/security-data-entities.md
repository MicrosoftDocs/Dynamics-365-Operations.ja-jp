---
title: セキュリティとデータ エンティティ
description: この記事では、データ エンティティのセキュリティについて説明します。
author: peakerbl
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 17852
ms.assetid: a9ede141-56fa-4310-997d-aeef184f7a52
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f54f11fd760ad39ab72b9108c0add350a14fb1bf
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108407"
---
# <a name="security-and-data-entities"></a>セキュリティとデータ エンティティ

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

> [!NOTE]
> データ エンティティは拡張可能なデータ セキュリティ (XDS) の概念をサポートしません。

## <a name="entry-points"></a>エントリ ポイント
データ エンティティはエントリ ポイントのセキュリティをサポートします。 このサポートは、メニュー項目とページのサポートと似ています。 セキュリティ モデルを定義する際の柔軟性を高めるため、データ エンティティでは統合モードごとに個別のセキュリティ設定が可能となっています。 現在、データ エンティティに対して 2 つのエントリ ポイント/統合モードは識別されます。

| エントリ ポイント     | 説明                                                                                                          |
|-----------------|----------------------------------------------------------------------------------------------------------------------|
| データ サービス   | エンティティ用の OData サービス (API) を使用できる機能。                                                              |
| データ管理 | インポート/エクスポートおよびコネクタの統合など、エンティティ用の非同期統合オプションを使用できる機能。 |

## <a name="target-scenarios"></a>ターゲット シナリオ
データ エンティティは、シナリオの複数のカテゴリをサポートできます。 各カテゴリでは、別々に確保する必要があります。

- **データ管理 (ファイルに基づくインポート/エクスポートなど)** - 通常、データ マネージャーがこれらのシナリオを実行します。 これらのシナリオでは、クライアントの UI から通常アクセスできないデータにアクセスできます。 したがって、データ マネージャーがインポート/エクスポート操作のみを実行できるよう、関連ページへのアクセスとは独立してデータ管理シナリオを保護したいと考えることは多くあります。
- **OData 経由の全般的な統合** – 多くの統合シナリオでは、データ エンティティをサービスとして公開する必要があるため、OData (オンライン ストアフロントや製品ライフサイクル管理 \[PLM\] システムなど) を介してデータにアクセスすることができます。 多くの場合、この目的のためにページ アクセスとは別に作成されている、データ エンティティへのアクセスを制御する必要があります。 つまり、クライアントの UI を使用してアクセス許可を与えることなく、サービス インターフェイスへのアクセスを許可します。
- **Microsoft Office 統合 (Excel での編集など)** – Office 統合シナリオでも、OData 経由でアクセスするデータ エンティティが必要です。 ただし、エンドユーザーの観点からは、これらのシナリオは、たとえば Microsoft Excel が一部の編集作業を簡略化するのに使用されるなど、クライアントの自然の拡張として見なすことができます。 したがって、通常、ページ アクセスとは独立して Microsoft Office の統合を保護する理由はありません。

## <a name="privilegeduty-mapping"></a>権限/職務権限マッピング
データ エンティティの対象シナリオに応じて、1 つまたは複数の新しい特権を作成し、既存の職務を拡張する必要があります。 または、新しい権限をターゲット シナリオ用に特別に作成された職務にマップすることができます。 この方法は、シナリオに必要なアクセス権以上のアクセス権がユーザーに付与されないようにします。

次のテーブルに、作成する必要のある権限を示します。 また、職務にこれらの特権をマップする方法についても説明します。 データ エンティティが複数のシナリオをサポートすることを意図している場合、権限と職務権限マッピングを組み合わせたセットを作成する必要があります。

<table>
<thead>
<tr>
<th>ターゲット シナリオ</th>
<th>権限</th>
<th>職務マッピング</th>
</tr>
</thead>
<tbody>
<tr>
<td>データ エンティティは、データ管理を目的としています。</td>
<td>次の新しい権限を作成します。
<ul>
<li><em>&lt;DataEntity&gt;</em><strong>インポート</strong>
<ul>
<li>交付 = 作成</li>
<li>IntegrationMode=DataManagement</li>
</ul>
</li>
<li><em>&lt;DataEntity&gt;</em><strong>エクスポート</strong>
<ul>
<li>付与 = 読み取り</li>
<li>IntegrationMode=DataManagement</li>
</ul>
</li>
</ul>
</td>
<td>新しい権限を持つ関連データの管理業務を拡張します。 詳細については、この記事で後述する「データ管理者ロール」セクションを参照してください。</td>
</tr>
<tr>
<td>データ エンティティは、OData を介した一般的な統合を目的としています。</td>
<td>次の新しい権限を作成します。
<ul>
<li><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
<ul>
<li>付与 = 読み取り</li>
<li>IntegrationMode=DataServices</li>
</ul>
</li>
<li><em>&lt;DataEntity&gt;</em><strong>管理</strong>
<ul>
<li>交付 = 削除</li>
<li>IntegrationMode=DataServices</li>
</ul>
</li>
</ul>
</td>
<td>統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。 詳細については、この記事で後述する「職務名のガイドライン」セクションを参照してください。</td>
</tr>
<tr>
<td>データ エンティティは、Microsoft Office との統合を目的としています。</td>
<td>次の新しい権限を作成します。
<ul>
<li><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
<ul>
<li>付与 = 読み取り</li>
<li>IntegrationMode=DataServices</li>
</ul>
</li>
<li><em>&lt;DataEntity&gt;</em><strong>管理</strong>
<ul>
<li>交付 = 削除</li>
<li>IntegrationMode=DataServices</li>
</ul>
</li>
</ul>
</td>
<td>新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</td>
</tr>
</tbody>
</table>

前のテーブルで説明されている方法は最小特権の原則に準拠しているため、それを使用することをお勧めします。 ただし、場合によっては、次のより簡単な方法を使用することができます。 ただし、この方法は安全性が低い場合があることに注意してください。 管理および拡張が少し困難になる場合もあります。

<table>
<thead>
<tr>
<th>ターゲット シナリオ</th>
<th>権限</th>
<th>職務マッピング</th>
<th>潜在的な問題</th>
</tr>
</thead>
<tbody>
<tr>
<td>データ エンティティは、データ管理、OData による一般的な統合、および Microsoft Office との統合を目的としています。</td>
<td>次の新しい権限を作成します。
<ul>
<li><em>&lt;DataEntity&gt;</em> <strong>ビュー</strong>
<ul>
<li>付与 = 読み取り</li>
<li>IntegrationMode=All</li>
</ul>
</li>
<li><em>&lt;DataEntity&gt;</em><strong>管理</strong>
<ul>
<li>交付 = 削除</li>
<li>IntegrationMode=All</li>
</ul>
</li>
</ul>
</td>
<td>
<ol>
<li>新しい権限を持つ関連データの管理業務を拡張します。</li>
<li>統合シナリオの新しい職務を作成し、関連する新しい特権をこれらの職務にマッピングします。</li>
<li>新しい権限を持つ関連ページへのアクセスを提供する関連する既存の任務を拡張します。</li>
</ol>
</td>
<td>この方法を使用するときは、データのインポート/エクスポートへのアクセス許可を付与されているデータ マネージャーは、システムに Web サービスからもアクセスできます。 同様に、データ エンティティに関連付けられているページへのアクセスを許可されているユーザーは、Web サービスからでもシステムにアクセスできます。 このユーザーは、関連するデータ管理職務権限を付与されていない場合にのみ、データのインポート/エクスポートを禁止されます。</td>
</tr>
</tbody>
</table>

## <a name="duty-naming-guidelines"></a>職務名のガイドライン
特定の統合シナリオのデータ エンティティを作成するとき、個別の職務も作成する必要があります。 これらの任務は、外部アプリケーションまたはサービスに、データ エンティティへの必要なアクセスを許可します。 作成する職務は、クライアント UI を介してアクセスするための対応する職務と同じ命名規則に従ってください。 ただし、「サービスを使用する」接尾辞を追加する必要があります。

<table>
<thead>
<tr>
<th>職務タイプ</th>
<th>職務オブジェクト名の接尾語</th>
<th>職務名のテンプレート</th>
</tr>
</thead>
<tbody>
<tr>
<td>有効化</td>
<td>…IntegrationEnable</td>
<td>有効化 … サービスの使用</td>
</tr>
<tr>
<td>レコード</td>
<td>…IntegrationMaintain</td>
<td>メンテナンス … サービスの使用</td>
</tr>
<tr>
<td>認証する</td>
<td>…IntegrationApprove (リリース、確認、仕分入力)</td>
<td>承認 (リリース、確認、仕訳入力) … サービスの使用</td>
</tr>
<tr>
<td>照会</td>
<td>…IntegrationInquire</td>
<td>照会先 … サービスの使用</td>
</tr>
</tbody>
</table>

これらのガイドラインに従う職務権限名の例を次に示します。

- サービスを使用した工順マスターの管理
- サービスを使用しているケース進捗状況の照会

## <a name="data-administrator-role"></a>データ管理者ロール
**DataManagementApplicationAdministrator** セキュリティ ロールによって、関連したユーザーが **データ管理** ワークスペースでフル インポート/エクスポート機能を実行できます。 このセキュリティ ロールには、5 つのデータ エンティティ カテゴリに割り当てられた 2 つのセキュリティ職務があります。 1 つの関税は、関連するカテゴリのデータ エンティティを介してデータをインポートすることであり、1 つは関連するカテゴリのデータ エンティティを介してデータをエクスポートすることです。 したがって、このセキュリティ ロールには合計 10 のセキュリティ義務が割り当てられます。

- DataManagementApplicationDocumentEntitiesMaintain
- DataManagementApplicationDocumentEntitiesView
- DataManagementApplicationMasterEntitiesMaintain
- DataManagementApplicationMasterEntitiesView
- DataManagementApplicationParametersEntitiesMaintain
- DataManagementApplicationParametersEntitiesView
- DataManagementApplicationReferenceEntitiesMaintain
- DataManagementApplicationReferenceEntitiesView
- DataManagementApplicationTransactionEntitiesMaintain
- DataManagementApplicationTransactionEntitiesView

**データ管理** ワークスペースで使用できるデータ エンティティを作成するとき、データ エンティティで指定される **エンティティ カテゴリ** プロパティに基づいて、新しいセキュリティ権限を持つこれらの職務を拡張する必要があります。 (新しいセキュリティ権限を使用して職務を拡張する方法については、この記事の前半の「特権/職務マッピング」セクションを参照してください)。また、職務を使用して、特定のデータ管理シナリオ用の新しいロールを作成することもできます。

## <a name="modeling-new-entry-point-security-in-the-application-explorer"></a>アプリケーション エクスプローラーでの新しいエントリ ポイント セキュリティのモデリング
セキュリティのモデリングのパターンは、エントリ ポイントに対する権限を持つセキュリティのモデリングのパターンと似ています。 セキュリティをモデル化するには、次の手順を実行します。

1. 新しい権限の作成を作成します。
2. 新しいデータ エンティティのアクセス許可を作成します。
3. **名前** を **データ エンティティ** に設定します。
4. **アクセス レベル** を選択します。
5. **統合モード** を選択します (すべて &gt; Data Services &gt; データ管理)。 これは、オブジェクトの種類のデータ エンティティに固有です。

    - **すべて** - OData とデータのインポート/エクスポートの両方に適用される同じセキュリティ設定を適用します。
    - **データ管理** - データのインポート/エクスポートおよびコネクタの統合のみに適用されます。
    - **データ サービス** - OData サービスにのみ適用されます。

[![RolebasedSecurity.](./media/rolebasedsecurity.png)](./media/rolebasedsecurity.png)

## <a name="sensitive-data"></a>機密データ
テーブル保護フレームワーク (TPF) は、財務と運用に格納されているデータへの厳密なアクセス制御を使用できます。 この機能は、テーブルおよびテーブルのフィールドの AOSAuthorization プロパティを介して公開されます。 AOSAuthorization を使用してテーブルまたはフィールドにマークを付ける場合、セキュリティ フレームワークでは、そのリソースへの明示的なアクセス権がユーザーに付与されている必要があります。 この要件は、テーブルまたはフィールドにデータエンティティでアクセスする場合にも適用されます。 この項では、データ エンティティの TPF アクセス許可を付与するためのガイドラインについて説明します。

### <a name="data-management"></a>データ管理 
データ移行で対象となるデータ エンティティについては、TPF アクセス許可を対応するインポート/エクスポート権限に割り当てる必要があります。 この方法で、すべてのデータがインポート/エクスポートできることを保証できます。

### <a name="integration-by-using-odata"></a>OData を使用する統合
統合シナリオで対象とされるデータ エンティティについては、割り当てる必要がある TPF アクセス許可は、作業する全体としてのデータ エンティティに対して TPF で保護されたフィールドが必須かどうかに依存します。

- **TPF で保護されたフィールドが必須の場合**: 必須のフィールドは、常に読み取り/書き込みとなるフィールドです。 この場合、TPF のアクセス許可は、データ エンティティへのアクセスを許可する同じ権限に対して付与する必要があります。
- **TPF で保護されたフィールドが必須ではない場合**: 必須ではないフィールドの例としては、作業者の社会保障番号のフィールドおよび仕入先の銀行口座番号のフィールドがあります。 この場合、このフィールドにアクセスするための TPF アクセス許可は別の権限を通じて付与する必要があり、その権限は TPF で保護されたフィールドへのアクセスを必要とするロールに直接割り当てる必要があります。 ただし、フィールドがエンティティのマップ済フィールドである場合、そのロールはクライアント UI のページを通してフィールドへアクセスできるなら、ロールへのそのアクセスが既に許可された可能性があります。

エンティティにとって必須ではない TPF で保護されたフィールドへの明示的なアクセスを許可することには、いくつかの利点があります。

- だれが機密データへのアクセス権を持つかをより簡単に検出することができます。
- ロールに職務権限と特権の両方を割り当てる場合にのみにロールがアクセス権を取得するので、だれかが誤って機密データへのアクセスできるリスクを軽減できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

