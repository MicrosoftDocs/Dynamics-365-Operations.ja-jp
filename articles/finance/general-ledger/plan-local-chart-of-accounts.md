---
title: ローカル勘定科目表の計画
description: このトピックでは、組織の法的/ローカル要件がある場合に、勘定科目表の計画に役立つ情報を提供します。
author: VeselinaE
ms.date: 10/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts, LedgerConsolidateAccountGroup, MainAccountConsolidateAccount, DimensionDetails, MainAccountDetails
ROBOTS: ''
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.tgt_pltfrm: ''
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.search.industry: ''
ms.author: veneva
ms.search.validFrom: 10/07/2021
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e224a2e24b4ba293c953c6c883307038128e2f04
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798299"
---
# <a name="plan-your-local-chart-of-accounts"></a>ローカル勘定科目表の計画

[!include [banner](../includes/banner.md)]

このトピックでは、ビジネスを行う特定の地域の要件を満たす必要がある法人が組織に含まれる場合に、勘定科目表の計画に役立つ情報を提供します。 このトピックでは、次の用語を使用して勘定科目表を説明します:

- **グローバル** – 組織がグローバルに使用する勘定科目表。 ほとんどの場合、この勘定科目表に連結します。
- **ローカル** – 特定の国または地域の法人が使用する勘定科目表。
- **共有** – 複数の法人が使用できる勘定科目表。 グローバル勘定科目表とローカル勘定科目表の両方を共有できます。

複数の勘定科目表を作成して共有できます。 共有勘定科目表は複数の法人で使用できますが、各法人に割り当てることができる勘定科目表は 1 つのみです。 法人が使用する勘定科目表は、**元帳** ページで定義されます。

勘定科目表を設計する場合、多くの組織はグローバル勘定科目表を目指します。 共有勘定科目表の機能により、グローバル勘定科目表を作成できます。 1 つの勘定科目表を作成して使用する利点があります。 たとえば、ガバナンスやコントロール、メンテナンス、およびレポートが容易になります。

ほとんどの組織ではグローバル勘定科目表を好み、それは実装が最も簡単なタイプです。 しかし、一部の法人は次の理由からローカル勘定科目表を必要とします:

- ローカルの法的要件
- ローカル会計基準の要件
- 業界の要件
- 会社固有のレポートと分析の要件

法人がローカル勘定科目表を使用する必要がある場合、次の 2 つのオプションを使用して実装できます:

- グローバル勘定科目表を割り当て、ローカル要件を満たす他の方法を定義します。
- 法人にローカル勘定科目表を割り当て、グローバル勘定科目表への関係を定義します。

使用するオプションは、組織構造とレポート構造によって決まります。

[![グローバルまたはローカルの勘定科目表のどちらを使用するかを組織構造によって決定する方法を示す図](./media/local-chart-of-accounts-diagram.png)](./media/local-chart-of-accounts-diagram.png)

グローバル勘定科目表が法人に割り当てられている場合、ローカル レポート要件を満たすために次のオプションを使用できます:

- ローカル連結を行う。
- 財務分析コードを使用してローカル勘定科目表を追跡する。
- グローバル勘定科目表でローカルの主勘定を作成する。
- ローカル勘定科目表に外部マッピングを行う。

ローカル勘定科目表が法人に割り当てられている場合、グローバル レポート要件を満たすために現在利用できる唯一のオプションは、グローバル連結です。

## <a name="global-chart-of-accounts-assigned-to-a-legal-entity"></a>法人に割り当てられたグローバル勘定科目表

グローバル勘定科目表を法人に割り当てる必要がある場合、前述のように、システムを構成するための 4 つのオプションを使用できます。 4 つのオプションすべてについて、1 つの勘定科目表が構成され、**元帳** ページの各法人にリンクされます。 その後、各オプションでは、異なる方法を使用して、ローカライズ要件を満たします。 次のセクションでは、ローカライズ要件に合わせてシステムを構成するための高レベルの手順について説明します。 また、各オプションの長所と短所についても説明します。

### <a name="do-local-consolidation"></a>ローカル連結を行う

ローカル連結は、ローカル勘定科目表の要件を満たし、この目的のために設計されたシステム機能を活用する場合に推奨される方法です。

#### <a name="set-up-consolidation-for-a-local-chart-of-accounts"></a>ローカル勘定科目表に対する連結の設定

1. 必要なすべての主勘定を含む 1 つのグローバル勘定科目表を作成します。
2. 各法人では、**元帳** ページ上のグローバル勘定科目表を割り当てます。
3. 必要なローカライズごとに連結法人を作成します。
4. 次の手順のいずれかを実行します。

    - ローカライズが 1 つだけ必要な場合は、**主勘定** ページで連結勘定を構成するか、**連結グループ** ページと **追加連結勘定** ページを使用します。
    - 複数のローカライズが必要な場合や、勘定番号と勘定名の両方に翻訳が必要な場合は、**連結グループ** ページと **追加連結勘定** ページを使用して、ローカライズ要件を表します。

5. 連結プロセスを実行して、グローバル勘定科目表を使用するソース法人から、ローカル勘定科目表を使用する連結会社に値を変換します。

#### <a name="advantages"></a>メリット

- この方法では、組織全体で一貫した作業方法を提供します。
- ローカルな状況の翻訳が 1 件行われます。
- この方法では、主勘定 ID と各主勘定の名前の両方の翻訳をサポートします。
- 複数のローカライズをサポートします。

#### <a name="disadvantages"></a>欠点

- 追加の連結会社が作成されます。
- 追加の連結プロセスが完了します。
- この方法では、連結プロセスの完了後にのみ、ローカライズされたグラフでレポートすることができます。

### <a name="use-a-financial-dimension-to-track-the-local-chart-of-accounts"></a>財務分析コードを使用してローカル勘定科目表を追跡する

この方法では、財務分析コードの値がローカライズに必要なローカルの主勘定を表す財務分析コードを使用します。 1 つのローカライズだけが必要な場合には適しています。 ただし、ローカライズや財務分析コードを追加すると、使用しにくくなります。

#### <a name="set-up-a-financial-dimension-for-a-local-chart-of-accounts"></a>ローカル勘定科目表の財務分析コードを設定する

1. 必要なすべての主勘定を含む 1 つのグローバル勘定科目表を作成します。
2. 各法人では、**元帳** ページ上のグローバル勘定科目表を割り当てます。
3. ローカル勘定科目表を表す財務分析コードを作成します。
4. ローカル勘定科目表で主勘定を表す財務分析コード値を作成します。
5. "ローカル勘定科目表" の財務分析コードが含まれるように勘定構造を更新します。
6. "ローカル勘定科目表" の財務分析コードには常に値があり、空白の値が許可されていないことを確認します。 派生分析コードまたは固定分析コードの使用を検討してください。
7. "ローカル勘定科目表" の財務分析コードが最初に選択された財務分析コードである財務分析コード セットを作成します。 財務分析コード セットは、試算表の生成時に使用できます。

#### <a name="advantages"></a>メリット

- グローバル勘定科目表とローカル勘定科目表の両方の主勘定は、トランザクション レベルで存在します。 主勘定はグローバルで、財務分析コード値はローカルです。
- この方法により、グローバルな財務状況とローカルな財務状況の両方について、リアルタイムのレポートとビューが提供されます。

#### <a name="disadvantages"></a>欠点

- 一般会計パラメーターで、**集計勘定に使用される値** フィールドが **勘定配布** に設定されている場合、経費/資産/収益の主勘定を表す財務分析コードが、売掛金勘定と買掛金勘定の集計勘定に対して正しく使用されません。 適切な財務分析コード値が使用されるように、フィールドを元伝票に設定することをお勧めします。
- 多くのローカル勘定科目表が必要で、1 つの財務分析コードがそれらすべてに使用される場合、使用される財務分析コード値のリストが長くなり、使用が困難になる可能性があります。
- 多くのローカル勘定科目表が必要で、それぞれを表すために個別の財務分析コードが使用される場合、財務分析コードと財務分析コード セットを追加すると、システムの使いやすさとパフォーマンスが影響を受ける可能性があります。
- これらすべての要因がシステムのパフォーマンスに影響を与える可能性があるため、必要な財務分析コードの数、各分析コードの値の数、財務分析コード セットの数を慎重に検討することをお勧めします。

### <a name="create-local-main-accounts-in-the-global-chart-of-accounts"></a>グローバル勘定科目表でローカルの主勘定を作成する

*コピー エディターからの質問:* この方法では、グローバル勘定科目表のローカル主勘定に、グローバル勘定科目表にあるローカル勘定科目表の主勘定が含まれます。

*元のバージョン:* グローバル CoA 内のローカル主勘定の方法では、ローカル CoA の主勘定がグローバル CoA に含まれます。

*このような場合:* この方法では、ローカ勘定科目表のローカル主勘定がグローバル勘定科目表に含まれます。


#### <a name="set-up-local-main-accounts-in-the-global-chart-of-accounts"></a>グローバル勘定科目表でローカルの主勘定を設定する

1. グローバル勘定科目表とローカル勘定科目表の両方の主勘定を含む勘定科目表を 1 つ作成します。
2. 各法人では、**元帳** ページ上の勘定科目表を割り当てます。
3. 勘定科目表で勘定合計を作成し、同じ目的を表す主勘定をまとめます。
4. 各ローカル アカウントで法人の上書きを作成し、そのローカル アカウントが対象としていない他の法人からのトランザクションを回避します。
5. グローバル アカウントごとに法人の上書きを作成し、ローカライズの法人からのトランザクションを回避します。

#### <a name="advantages"></a>メリット

- グローバルな財務状況とローカルな財務状況の両方のリアルタイム ビューは、特定のレポートやシステムの特定のビュー (貸借対照表の財務諸表など) で使用できます。 勘定合計の **期間** ボタンを使用してアクセスすることもできます。
- 勘定科目にセグメントを追加することはできません。

#### <a name="disadvantages"></a>欠点

- 勘定合計の使用と表示は制限されます。 たとえば、**試算表** リスト ページに勘定合計は表示されません。
- メンテナンスには追加作業が必要です。
- 財務諸表を作成するには、さらに手作業が必要です。

### <a name="do-external-mapping-to-the-local-chart-of-accounts"></a>ローカル勘定科目表に外部マッピングを行う

グローバル勘定科目表の採用は、システム外でマッピングとローカライズを管理することを前提としています。 この方法では、Microsoft Dynamics 365 Finance でグローバル勘定科目表を 1 つ作成し、システム外部の要件を処理するだけです。

#### <a name="set-up-external-mapping-to-a-local-chart-of-accounts"></a>ローカル勘定科目表に外部マッピングを設定する

1. 必要なすべての主勘定を含む 1 つのグローバル勘定科目表を作成します。
2. 各法人では、**元帳** ページ上のグローバル勘定科目表を割り当てます。
3. Finance 以外のローカル勘定科目表にマッピングを行います。

#### <a name="advantages"></a>メリット

- この方法では、組織全体で統一された作業方法を提供します。

#### <a name="disadvantages"></a>欠点

- システムからのローカル レポートは使用できません。
- この方法では、財務諸表の作成時にエラーが発生しやすくなります。

## <a name="local-chart-of-accounts-assigned-to-legal-entity"></a>法人に割り当てられたローカル勘定科目表

組織が、法人間でグローバル勘定科目表を使用しない場合は、固有のローカル勘定科目表ごとに個別の勘定科目表が作成されます。 その後、各法人は、**元帳** ページの対応する勘定科目表にリンクされます。

### <a name="do-global-consolidation"></a>グローバル連結を行う

この方法では、連結会社を使用して、各ソースのローカル会社の残高を連結会社の結合されたグローバル勘定科目表にロールアップして結合します。 この方法では、連結会社で各ローカル勘定科目表とグローバル勘定科目表のマッピングを維持する必要があります。

#### <a name="set-up-global-consolidation"></a>グローバル連結を設定する

1. 異なるローカル勘定科目表を持つ法人ごとに個別の勘定科目表を作成します。 法人に同じローカル勘定科目表がある場合は、必要なローカル勘定科目表は 1 つのみで、共有することができます。
2. 各法人では、**元帳** ページ上の適切な勘定科目表を割り当てます。
3. オプション: 異なるグローバル勘定科目表を持つ各連結会社のグローバル勘定科目表に対して、勘定科目表を作成します。
4. 必要な連結レベルごとに連結法人を作成し、**元帳** ページで適切な勘定科目表を割り当てします。
5. 次の手順のいずれかを実行します。

    - 連結が 1 つのみ必要な場合は、**主勘定** ページで連結勘定を構成します。
    - 複数の連結が必要な場合や、勘定番号と勘定名の両方に翻訳が必要な場合は、**連結グループ** ページと **追加連結勘定** ページを使用して、グローバル勘定科目表の要件を表します。

6. 連結プロセスを実行して、ローカル法人から連結法人に残高を転送します。 この連結法人では、手順 5 で定義した連結勘定を使用します。

#### <a name="advantages"></a>メリット

- ローカル会計基準の形式はネイティブに適用されます。
- この方法により、ローカルの財務チームはより簡単に作業できます。

#### <a name="disadvantages"></a>欠点

- グローバルな状況のリアルタイム ビューは使用できません。
- 連結プロセスが頻度に実行される場合があります。

## <a name="additional-resources"></a>追加リソース

- [勘定科目表の計画](plan-chart-of-accounts.md)
- [元帳のコンフィギュレーション](configure-ledger.md)
- [財務分析コードおよび転記](Default-dimensions.md#balancing-dimension)
- [財務分析コード セット](financial-dimension-sets.md)
- [連結と削除の概要](../budgeting/consolidation-elimination-overview.md)
- [連結勘定グループおよび追加の連結勘定](../budgeting/consolidation-account-groups-consolidation-accounts.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]