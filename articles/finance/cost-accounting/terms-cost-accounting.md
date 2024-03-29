---
title: 原価会計用語
description: この記事では、原価計算で使用する重要な用語を定義します。
author: aprilolson
ms.date: 08/31/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedger
audience: Application User
ms.reviewer: twheeloc
ms.custom: 223114
ms.assetid: 1c798592-77d0-4a8f-beaa-9159c75957da
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5827ad66b9eedaab88dbda97c1ebbcd15f6d9ac8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881936"
---
# <a name="cost-accounting-terminology"></a>原価会計用語

[!include [banner](../includes/banner.md)]

この記事では、原価計算で使用する重要な用語を定義します。

**配賦基準**

配賦基準は活動を測定および数量化するために使用される基準です。たとえば使用された機械の時間、消費されたキロワット時間、または占有された平方フィート単位などです。 これは、1 つまたは複数のオブジェクトのコスト配賦の基礎として使用されています。

**原価会計**

原価計算では、総勘定元帳、補助元帳、予算、および統計情報などのさまざまなソースから、データを収集することができます。 次に分析、集計、および原価データを評価し、管理者が価格の更新、予算、原価管理などの最善の決定ができるようにします。 原価分析に使用されるソース データは、原価計算では別に処理されます。 したがって、原価計算の更新はソース データに影響しません。 ただし、さまざまなソースから原価データを収集し、特に原価要素として、総勘定元帳から主勘定をインポートすると、同じデータが総勘定元帳と原価計算の両方に存在するため、データ冗長があります。 この冗長性は、外部レポートでの財務管理および内部レポートでの原価計算を使用するために必要です。

**原価会計元帳**

カレンダー、通貨および原価要素分析コードで定義され、コストを測定する際のプロセスとポリシーをコントロールします。 

**原価エントリ**

原価エントリとは、総勘定元帳エントリのデータ コネクタによる転送の結果、原価配賦および原価仕訳帳に転記された原価エントリです。

**原価オブジェクト**

原価管理に対して選択されるオブジェクトのすべてのタイプです。 コストまたは収益は、直接転記または原価オブジェクトに割り当てられます。 一般的なコストのオブジェクトを挙げます。

-  製品
-  プロジェクト
-  部門
-  コスト センター

管理者は、原価を定量化するのに原価オブジェクトを使用し、収益性分析を推進します。

**原価要素**

追跡およびコストの分類の機能として使用します。 原価要素には、基本と二次という 2 つのタイプがあります。

主要原価要素は、財務会計から原価会計へのコストの流れを表します。 構造は通常、原価要素が主勘定に対応できる一般会計で損益勘定構造に対応します。 業務上の要件に応じて、すべての主勘定が原価要素として表される必要があります。 

第 2 原価要素は、これらのコストが原価会計でのみ使用されるため、内部のコストの流れを表します。 これらは、間接費の計算で使用される意味のあるバケットにコストを集計するために、原価ロールアップのルールで使用されます。 

**原価分類**

原価分類グループは、共有された特性に基づいて原価をグループ分けします。 たとえば、原価は、要素、トレーサビリティ、および動作にグループ化できます。

-   **要素による** – 材料、労務、および経費。
-   **トレーサビリティによる** – 直接原価および間接原価。 直接原価は原価オブジェクトに直接割り当てられます。 間接原価は、原価オブジェクトを直接追跡できません。 間接原価は、原価オブジェクトに割り当てられます。
-   **動作にる** - 固定、変数、半変数。

**原価動作**

原価動作は、鍵となる事業活動の変更に関連する動作に基づいて原価を分類します。 原価を効率的に管理するには、管理者は原価の動作を理解する必要があります。 原価の動作のパターンには 3 つのタイプ、つまり固定、変数、半変数があります。

- **固定費** - 固定費は、活動レベルの変更に関係なく、短期的に変化しないコストです。 たとえば、固定費は、家賃などの業務の基本的な作業経費であり、活動の増加および減少の影響を受けません。

- **変動費** - 変動費は、活動レベルの変化に従って変化します。 たとえば、特定の直接材料の原価は、販売された各製品に関連付けられます。 販売された製品が多くなれば、直接的な材料の原価は多くなります。

- **半変動費** - 半変動費は部分的に固定費であり、また部分的に変動費な費用です。 たとえば、インターネット アクセス料金には、標準的な月額のアクセス料金とブロードバンド使用料金が含まれます。 標準的な月額アクセス料金は固定費で、ブロードバンド使用料金は変動費です。

**原価管理単位**

原価管理単位は、原価構造を表します。 構造は、原価オブジェクト分析コードとそれらに対応する原価オブジェクトの間で、コストがどのように階層順に流れるかを決定します。 

**原価配分**

関連する配賦基準を適用することによって、1 つのコスト オブジェクトから 1 つまたは複数の他のコスト オブジェクトへコストを配分するために使用されます。 コスト配分とコスト配賦は、コスト配分は常に元のコストおよび相互的でない処理の主要コスト要素レベルで起こるという点が異なります。

**原価配賦**

配賦基準を適用することによって、コスト オブジェクトの残高を他のコスト オブジェクトに配賦するために使用します。 Finance では、相互配賦手法をサポートします。 相互配賦手法では、補助コスト オブジェクトが交換する相互サービスが完全に認識されます。 システムは、配賦を実行し、繰り返し処理する順序を自動的に決定します。 コスト オブジェクトの残高は 1 つの配賦基準によって配賦されます。 コスト オブジェクト分析コードとその各メンバーにまたがる配賦がサポートされています。 配賦の順序は、コスト制御ユニットによって制御されます。

**原価配賦ポリシー**

原価配賦のポリシーは、配賦する必要がある数量と金額を定義します。 配賦ルールには配賦元のルールが含まれます。これは配賦されている原価の決定、および原価が割り当てられるところを決定する配賦先のルールを決定します。 たとえば、融資サービスのすべての原価は、組織 (つまり、配賦ターゲット) のさまざまな部門に割り当てることができる配賦ソースです。

**原価ロールアップ**

コストロールアップのルールの目的は、意味のあるバケットにコストを集計することです。 集約のレベルは、ユーザー定義であり、第 2 原価要素の割り当てが含まれます。 原価のロールアップを使用しない場合、コストのすべての要素が、1 つの原価オブジェクトから他の原価オブジェクトに割り当てられます。

**原価率のポリシー**

原価率は原価オブジェクトあたりの価格を計算するために使用されます。 価格の要素を理解するために、原価率のポリシーを定義します。 原価率には、履歴原価率と予定原価率という 2 種類のタイプがあります。 履歴原価率は原価オブジェクトの配賦基準に対して乗数で使用される計算された率です。 この率は、前の期間の原価配賦に基づいて計算されます。 計画されたレートは、ユーザー定義のレートです。

**分析コード階層**

カテゴリ階層、および分類階層という 2 つの分析コード階層があります。 [分析コードカテゴリ階層] タイプはレポート用に使用します。 コスト要素分析コードのみをサポートします。 [分析コード分類階層] タイプはポリシーの定義、およびレポート用に使用します。 コスト オブジェクト、コスト要素、および統計分析コードなどのすべての分析コードをサポートします。 

**データ コネクタ**

原価会計は、データ コネクタのセットを経由してのソース システムからのデータの統合をサポートします。 使用できるデータ コネクタは次のとおりです。

-  インポートされたトランザクション (コンフィギュレーション済み)
-  Dynamics 365 Finance (事前に構成済)
-  Dynamics AX (コンフィギュレーションが必須)

**注記:** データ コネクタは、データ エンティティに基づくトランザクションをインポートします。

**データ プロバイダー**

ほとんどのソース システムでは、原価会計で1つまたは複数のデータ ソースに一致するデータを提供できます。 原価会計のデータ ソースとのソース システムデータを調整するには、データ プロバイダーはコンフィギュレーションされている必要があります。 次の表は、データ ソースおよびデータ コネクタごとにデータ プロバイダーが使用できるかを一覧で示しています。

|  **データ ソース** |  **インポートされたトランザクション データ コネクタ** | **Dynamics 365 Finance データ コネクタ**  | **Dynamics AX データ コネクタ**  |
|---|---|---|---|
| 原価要素分析コード メンバー  |  有 | 有  | 有  |
|  原価オブジェクト分析コード メンバー |  有 | 有  | 有  |
|  統計分析コード メンバー | 有  | 無  | 無  |
|  一般会計 | 有  | 有  | 有  |
|  予算項目  | 有  | 有  | 有  |
|  統計測定 | 有  | 有  | 有  |

**式**

フォーミュラの配賦基準では、正しい配賦基準を実現する高度な式を定義できます。 フォーミュラ配賦基準を手動で作成することができます。 式の定義には次の演算子を使用できます。

|  **記号:** | **テキスト**  |
|---|---|
|  ( ) | かっこ  |
|  < |  より小さい |
|  > |  より大きい |
|  + |  追加 |
|  - |  減算 |
| *  | 乗算  |

従来型の IF ステートメントはサポートされていません。 ただし、ステートメントを作成し、それが正しいかを検証できます。

|  **明細書の検証** | **結果**  |
|---|---|
|  a > b| True  |
|  a > b |  False |

**間接費**

間接費は、事業の遂行に必要な経費を示します。 これらは、特定の営業活動に直接リンクすることができない費用です。 間接費の例を次に示します。

-   会計処理手数料
-   減価償却
-   保険
-   関心事項
-   弁護料
-   税申告
-   光熱費

**間接費率**

レートは、原価オブジェクトと原価要素ごとに定義されます。 レートには2つのタイプがあります。会計年度期間およびユーザー指定。 会計年度期間の期間率は、間接費の計算によって計算されます。 ユーザー固有のレートはユーザー定義され、間接費の計算であらかじめ設定されたレートの原価オブジェクト間の原価を配賦に使用できます。

**公開済**

このフィールドを [はい] に設定した場合、次のロールのいずれかに割り当てられているユーザーは 原価管理ワークスペースでレポートを表示することができます。

-  原価会計マネージャー
-  原価経理担当
-  原価経理担当係
-  原価オブジェクト コントローラー

このフィールドを [いいえ] に設定した場合、次のロールのいずれかに割り当てられているユーザーのみが 原価管理ワークスペースでレポートを表示することができます。

-  原価会計マネージャー
-  原価経理担当
-  原価経理担当係

**統計分析コード**

統計分析コードとそのメンバーは、原価会計の非通貨入力を登録および制御するために使用されます。 統計分析コードのメンバーは、次の 2 つの目的で使用できます。

-  コスト配分やコスト配賦などのポリシーにおける配賦基準として。
-  非金銭消費の報告として。

統計分析コードは、配賦または原価率の計算の基準として使用できる活動の番号または合計を表します。 これは手動で作成するか、またはソース システムからインポートされます。 統計分析コードの例には、従業員数、各デバイスのライセンスされたソフトウェアの数、各マシンのパワー消費量、またはコスト センターの平方メートルが含まれます。

**ステートメント**

明細書は原価の管理を担当する管理者が使用するビューです。 明細書は原価コントローラーで定義され、実際原価および予算化されたコスト、および誤差の簡単な概要を表示します。 マネージャーは、詳細が要求された際さらに掘り下げることができます。 信頼できるデータのみが管理者に表示されることを確実にするために、明細書に表示されるデータはアクセス ルールの対象になります。

**バージョン**

さまざまなバージョンがさまざまな結果をシミュレーション、表示および比較するために使用されます。 既定では、すべての実際原価は、*実績* として知られる 1 つの基準のバージョンで表示されます。 予算と計算のために、必要を満たす数多くのバージョンを使用できます。 たとえば、予算データをオリジナル版にインポートし、変更されたバージョンで予算を変更できます。 計算のために、複数のバージョンを作成できます。 これらのさまざまなバージョンでは、原価配賦に適用される異なる計算ルールを使用して、計算を作成できます。




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
