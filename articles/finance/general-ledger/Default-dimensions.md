---
title: 財務分析コードおよび転記
description: この記事では、勘定科目表をつくるコンポーネントについて、さらにコンポーネントがどのように連携するかについて説明します。
author: aprilolson
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerChartofAccounts,DimensionDetails
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 89696f08755a7ff2b01ec7e0cf8550a3b5914bc0
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715473"
---
# <a name="financial-dimensions-and-posting"></a>財務分析コードおよび転記 

[!include [banner](../includes/banner.md)]

勘定科目表を計画し設定する場合、ドキュメントまたは仕訳帳を転記するときにさまざまなコンポーネントがどのように連携するかを考慮する必要があります。 これらのコンポーネントには、高度なルール、詳細ルール、および差引勘定と固定の分析コードが含まれます。 この記事では、各コンポーネントについて、さらにコンポーネントがどのように連携するかについて説明します。

## <a name="chart-of-accounts-and-financial-dimension-components"></a>勘定科目表と財務分析コード コンポーネント

主勘定および財務分析コード値の有効な組み合わせを定義するために、リッチでルールに基づくシステムが使用されます。 このセクションでは、各コンポーネントの機能の概要が示し、コンポーネントをどこで検索できるかを説明します。

### <a name="account-structures"></a>勘定構造

勘定構造は、元帳を設定するときに必須です。 少なくとも 1 つの勘定構造を定義および有効にする必要があり、さらにそれを元帳に割り当てる必要があります。 勘定構造は自体に主勘定を持っている必要があります。 ビジネスに最も適したセグメントの順序を定義できます。 主勘定が定義された後、システムは、使用される勘定構造を決定できます。 主勘定を最初にまたは構造のフロントに挿入することで、値を制限し、既定値として最後の既知の有効な値をシステムが適用するのにも役立ちます。 勘定構造で、最大 10 個の追加の財務分析コードを持つことができます。 勘定構造は、他の値との組み合わせでどの分析コード値が有効かを定義します。 また、分析コード値を必須値とするかどうかを定義します。

### <a name="advanced-rules"></a>詳細ルール

詳細ルールは、勘定科目表を設定する際の、オプションのコンポーネントです。 勘定構造に必要な数だけ詳細ルールを追加することができます。 詳細ルールは、特定基準が満たされた場合に、追加の財務分析コードを追跡する必要があるシナリオを処理するためによく使用されます。 たとえば、旅行経費勘定を使用している場合は、従業員が出張したイベントなどの追加情報を追跡したいかもしれません。 複数の詳細ルールがある場合は、ルールの名前に基づいて、アルファベット順に適用されます。 ルールを追加するセグメントは、勘定構造のセグメントの後にのみ適用できます。

### <a name="balancing-dimension"></a>差引勘定分析コード

必要に応じて、差引勘定の財務分析コードを定義できます。 **元帳** ページで、差引勘定されるべき財務分析コードを定義することができます。 次に、その財務分析コードにトランザクションが転記されると、財務分析コードのバランスが保たれるように、システムは自動的にエントリを作成および転記します。

### <a name="defaultfixed-financial-dimensions-on-the-main-account"></a>主勘定での既定/固定の財務分析コード

既定の分析コードは、マスター レコード (たとえば、顧客または仕入先レコード)、ドキュメント ヘッダー、および主勘定などのさまざまな場所から取得されます。 この記事では、法人別の主勘定の既定の分析コードに焦点を当てます。 主勘定には、元帳のすべての勘定構造で使用される各財務分析コードに **固定なし** または **固定** 値があるかどうかを定義できます。 財務分析コードが **固定なし** の場合、既定値を使用して、その値を上書きできます。 この動作は、既定値がマスター レコードから取得された場合でも、システムのすべての既定値に適用されます。 財務分析コードが **固定** 値に設定されている場合、既定値としてにそれがどこから所得されたか、またはユーザーが入力した値かに関係なく、値は常に適用されます。

## <a name="order-in-which-default-dimensions-are-applied-during-posting"></a>転記時に既定の分析コードが適用される順序

多くの場合、ユーザーには、さまざまなコンポーネントが実行される順序についての質問があります。 この動作は、設定するためのアプローチに影響するので、既定の分析コードに適用される順序を理解することは非常に重要です。

> [!NOTE]
> この情報は、アプリケーションでの既定の分析コードのアプリケーションにのみ適用されます。 Microsoft Excel または Data Management Framework を使用してデータをインポートする場合は、動作が異なります。

### <a name="example-1"></a>例 1

**勘定構造**

| 主勘定            | 事業単位           | 部門              | コスト センター             |
|-------------------------|-------------------------|-------------------------|-------------------------|
| すべての値を使用できます。 | すべての値を使用できます。 | すべての値を使用できます。 | すべての値を使用できます。 |

**主勘定**

| 主勘定 | 氏名          | 個法 | 部門                                 |
|--------------|---------------|--------------|--------------------------------------------|
| 401100       | 製品の売上 | USMF         | 固定 – 022 販売およびマーケティング部門 |

次の図は、主勘定 401100 で設定されている固定の既定の分析コードを示します。

[![既定の財務分析コード。](./media/default-dimensions.png)](./media/default-dimensions.png)

この基本的な例では、部門分析コードが既定値 **023** (工程) を使用するよう設定されている一般仕訳帳を入力します。 勘定科目を入力および転記します。 次の図は、一般会計ヘッダーでの既定の財務分析コードを示します。

[![一般仕訳帳。](./media/general-journal.png)](./media/general-journal.png)

仕訳帳ヘッダーの既定の分析コードは、売上勘定明細行に既定で 023 が適用される部門を発生します。 次の図は、ヘッダーから取得される **023** 既定の分析コード値が適用される、一般仕訳帳明細行を示します。

[![仕訳伝票。](./media/journal-voucher.png)](./media/journal-voucher.png)

ただし、明細行が転記されると、固定分析コードが適用され、明細行が部門 022 に転記されます。 次の図は、売上勘定に固定分析コードが適用されている転記済の伝票を示します。

[![固定分析コードが適用された伝票トランザクション。](./media/voucher-transactions.png)](./media/voucher-transactions.png)

### <a name="example-2"></a>例 2

この例では、最初の例と同じ設定を使用します。 ただし、2 番目のコンポーネントを追加し、差引勘定の分析コードとして部門分析コードを使用します。 次の図では、**部門** は USMF 元帳の差引勘定の財務分析コードとして設定されます。

[![差引勘定の財務分析コードとしての部門を示す図。](./media/ledger.png)](./media/ledger.png)

同じ仕訳帳ヘッダーの設定を使用する場合、同じトランザクションが転記され、固定分析コードが最初に適用されます。 次に、すべての部門がバランス済みエントリを持つことを保証するよう、分散ロジックが適用されます。 次の図は、固定分析コードを適用した後のバランシング エントリが含まれている伝票トランザクションを示します。

[![バランシング エントリが適用された後の伝票トランザクション。](./media/voucher-transactions2.png)](./media/voucher-transactions2.png)

### <a name="example-3"></a>例 3

この例では、詳細ルールを追加します。 詳細ルールは、売上勘定 401100 および部門 022 (販売およびマーケティング) を使用している場合、システムが顧客という追加のセグメントを追跡すべきことを指定します。

この例は、順序のため重要です。 主勘定を入力した後は、勘定構造が決定されます。 勘定構造の設定を参照する場合は、システムは該当する主勘定、事業単位、部門、およびコスト センターを決定できます。 この時点では、仕訳伝票の転記時に既定の分析コードが適用されるまで固定分析コードは適用されないため、詳細ルールはトリガーされていません。 次の図では、詳細ルールの条件が満たされていないため、顧客セグメントが存在していません。

[![勘定科目。](./media/drop-down.png)](./media/drop-down.png)

固定分析コードがプロセスの最後に適用されたため、転記が成功しません。 分析コードの検証は、主勘定が 401100 および部門 022 である場合に必要である顧客のセグメントを決定します。 転記は、検証エラーが原因で発生しません。 次の図は、分析コードの検証が、顧客を必要なセグメントであると決定した後に表示されるメッセージを示します。

[![メッセージの詳細。](./media/message.png)](./media/message.png)

この例では、詳細ルールがトリガーされ、顧客セグメントを入力できるよう、既定値を上書きする必要があります。 ただし、このソリューションは常に可能ではなく、一部のユーザーは転記ルールに注意していないかもしれません。 したがって、勘定科目表を設定する際に既定の分析コードが適用される順序を理解しておくことが重要です。

この例で目的を達成するため、いくつかの方法でコンフィギュレーションを変更することができます。 たとえば、売上勘定の新しい勘定構造を作成し、構造に顧客セグメントを含めることができます。 また、既存の勘定構造に行を追加し、主勘定および有効な部門の値を指定することもできます。 次に、追加の顧客の構造で、顧客セグメントが存在する上で、売上勘定の個別の勘定構造を持つことが役立つかもしれません。

## <a name="additional-resources"></a>その他のリソース 

次のリソースの一部は、ソフトウェアの以前のバージョンを参照します。 ただし、既定の分析コードの適用に関する情報の大部分および概念の多くは、以前のバージョンでも同じであり、参照はまだ有効です。

[単位間会計の残高調整済み仕訳帳](example-balanced-journals-interunit-accounting.md)

[勘定科目表の計画](plan-chart-of-accounts.md) 

[AX 2012 の勘定科目表の計画ブログ](/archive/blogs/axsa/planning-your-chart-of-accounts-in-ax-2012-part-1-of-7)– このリンクは 7 部から成るシリーズの 1 部に移動します。

[勘定配布で既定分析コード](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-in-accounting-distributions-part-1-introduction)

[分析コード フレームワークで既定分析コード](/archive/blogs/ax_gfm_framework_team_blog/dimension-defaulting-part-1-financial-dimensions-discovery)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
