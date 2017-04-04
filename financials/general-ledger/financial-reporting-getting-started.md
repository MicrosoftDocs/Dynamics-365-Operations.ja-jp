---
title: "財務報告"
description: "このトピックでは、ダイアログ ボックスでは、Microsoft Dynamics 365の財務報告にアクセスするには、財務報告の機能の使用方法について説明します。 これは、決められた既定の財務諸表の説明を示します。"
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10444
ms.assetid: 3eae6dc3-ee06-4b6d-9e7d-1ee2c3b10339
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d13747f17b5f382b3a530b1f166681eeec0b9d73
ms.lasthandoff: 03/31/2017


---

# <a name="financial-reporting"></a>財務報告

このトピックでは、ダイアログ ボックスでは、Microsoft Dynamics 365の財務報告にアクセスするには、財務報告の機能の使用方法について説明します。 これは、決められた既定の財務諸表の説明を示します。

<a name="accessing-financial-reporting"></a>財務報告へのアクセス
-----------------------------

Dynamics 365 for Operationsの次の場所で**財務報告**メニューを検索できます:

-   **総勘定元帳** &gt; **照会やレポート**
-   **割り当て** &gt; ** ** **基本の割り当てを &gt; 尋ね、報告する**
-   **、[** &gt; **照会やレポート** &gt; **予算の計画**
-   **、[** &gt; **照会やレポート** &gt; **予算管理**
-   連結

法人の財務諸表を作成、生成するには、その法人に次の情報を設定する必要があります。

-   会計カレンダー
-   元帳
-   勘定科目表
-   通貨

財務報告の機能は、セキュリティ ロールによって適切な権限、職務が割り当てられたユーザーが使用できます。 次のセクションでは、関連するロールとともにこれらの権限と職務を表示します。

### <a name="duties"></a>職務権限

| 職務のラベル                            | 説明                                                             | AOT 名                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| 財務諸表のセキュリティの管理 | 財務諸表のセキュリティを管理し、管理タスクを実行します | FinancialReportsSecurityMaintain |
| 財務諸表の管理            | 財務諸表をデザインおよび管理します。                                  | FinancialReportsMaintain         |
| 財務諸表の生成            | 財務諸表を生成および更新します。                                 | FinancialReportsGenerate         |
| 財務パフォーマンスの確認          | 財務パフォーマンスを確認および分析します。                               | FinancialReportsPerfReview       |

### <a name="privileges"></a>権限

| 権限のラベル                       | 説明                                                             | AOT 名                         |
|---------------------------------------|-------------------------------------------------------------------------|----------------------------------|
| 財務諸表のセキュリティの管理 | 財務諸表のセキュリティを管理し、管理タスクを実行します | FinancialReportsSecurityMaintain |
| 財務諸表の管理            | 財務諸表をデザインおよび管理します。                                  | FinancialReportsMaintainReports  |
| 財務諸表の生成            | 財務諸表を生成および更新します。                                 | FinancialReportsGenerateReports  |
| 財務諸表の表示                | 財務諸表の表示。                                                 | FinancialReportsView             |

### <a name="roles"></a>ロール

| 権限のラベル                       | 関税                                  | ロール                                                                           |
|---------------------------------------|---------------------------------------|---------------------------------------------------------------------------------|
| 財務諸表のセキュリティの管理 | 財務諸表のセキュリティの管理 | セキュリティー管理者                                                          |
| 財務諸表の管理            | 財務諸表の管理            | アカウント マネージャ、会計監修者、財務予算管理者、マネージャ |
| 財務諸表の生成            | 財務諸表の生成            | CEO、CFOの会計士                                                            |
| 財務諸表の表示                | 財務パフォーマンスの確認          | 未割当                                                                   |

ユーザーが追加されるかロールを変更すると、ユーザーは数分以内に財務報告にアクセスできるようになります。 **注記: **のsysadminロールは、財務報告のすべてのロールに追加されます。

## <a name="default-reports"></a>既定のレポート
財務報告は 22 の既定の財務諸表を提供します。 各レポートは、Dynamics 365 for Operationsで既定の主要な勘定科目カテゴリを使用します。 このレポートは現状のまま使用するか、財務諸表のニーズに対する開始点として使用できます。 損益計算書や貸借対照表などの従来の財務諸表に加えて、これらの既定のレポートには、作成できる会計報告書のさまざまなタイプを示すレポートが含まれます。 次の表の各レポートはレポートに関するOffice Mixプレゼンテーションにリンクされます。

| 既定のレポート                                                                                         | 説明                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [12 Month Rolling Single Column Income Statement – Default](https://mix.office.com/watch/76kc7bm3wnt1) | 過去 12 か月の組織の収益性を、1 つの列で表示します。                                                                                                                                                                                                                                      |
| [12 Month Trend Income Statement – Default](https://mix.office.com/watch/12brmfge5p8r)                 | 過去 12 か月それぞれの組織の収益性を表示します。 この 12 か月は会計年度以上にまたがることができます。                                                                                                                                                                                             |
| [Actual vs Budget – Default](https://mix.office.com/watch/fi439lkwr0no)                                | 元の予算のすべての勘定の残高の詳細な情報を表示し、修正された予算を差異がある実績と比較します。                                                                                                                                                                          |
| [Audit Details – Default](https://mix.office.com/watch/1i15nzd3nwkyh)                                  | すべての勘定の残高の詳細な情報を表示します。 このレポートには、レポート通貨と国内通貨で借方と貸方残高が、ユーザー ID、データを最後に変更したユーザー、最終変更日、仕訳帳 ID などの追加トランザクション情報とともに表示されます。 |
| [Balance List – Default](https://mix.office.com/watch/1kezwu2a10fq4)                                   | すべての勘定の残高の詳細な情報を表示します。 このレポートは、開始残高と決算残高、伝票などの追加トランザクション情報とともに現在の期間と現時点の借方と貸方残高を表示します。                                                                    |
| [Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                                   | 年度の組織の財務状態を表示します。                                                                                                                                                                                                                                                             |
| [Balance Sheet and Income Statement Side by Side - Default](https://mix.office.com/watch/zkgq0u7visw9) | 年の組織の財務状態と収益性を並べて表示します。                                                                                                                                                                                                                              |
| [Cash Flow – Default](https://mix.office.com/watch/jd3go9pz6390)                                       | 組織に出入りする現金についての洞察を得ます。                                                                                                                                                                                                                                   |
| [Detailed JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)                      | すべての勘定の開始残高および活動の情報を表示します。                                                                                                                                                                                                                                                      |
| [Detailed Trial Balance - Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                         | すべての勘定の、借方と貸方残高、残高の正味金額、トランザクションの日付、伝票、仕訳帳の説明が含まれる残高情報を表示します。                                                                                                                                  |
| [Expenses Three Year Quarterly Trend – Default](https://mix.office.com/watch/gwm4zu7tmtj8)             | 過去 3 年間の 12 の四半期の経費についての洞察を得ます。                                                                                                                                                                                                                                   |
| [Financial Captions JE and TB Review – Default](https://mix.office.com/watch/1sw9fmtwgjb1f)            | 残高および資産の活動、負債、自己資本、収益、経費、利益、または損益財務キャプションを表示します。                                                                                                                                                                           |
| [Income Statement – Default](https://mix.office.com/watch/sbuhgl5hzuhi)                                | 現在の期間また年間累計の組織の収益性を表示します。                                                                                                                                                                                                                                   |
| [Ledger Transaction List – Default](https://mix.office.com/watch/19h9v2rmh48vy)                        | すべての勘定の残高の詳細な情報を表示します。 このレポートは、トランザクションの日付、仕訳帳番号、伝票、転記タイプ、追跡番号などの追加トランザクション情報とともに、借方と貸方残高を表示します。                                                                            |
| [Ratios – Default](https://mix.office.com/watch/b08hfc5h92me)                                          | 年の組織の支払能力、収益性、能率比率を表示します。                                                                                                                                                                                                                           |
| [Rolling 12 Month Expenses – Default](https://mix.office.com/watch/iywod5qmqhz7)                       | 過去 12 か月ごとの経費についての洞察を得ます。 この 12 か月は会計年度以上にまたがることができます。                                                                                                                                                                                                       |
| [Rolling Quarter Income Statement – Default](https://mix.office.com/watch/1k4yl6a6oyxqc)               | 過最後の年と年間累計のコンフィギュレーションの収益性を各季を参照してください。                                                                                                                                                                                                                   |
| [Side by Side Balance Sheet – Default](https://mix.office.com/watch/zkgq0u7visw9)                      | 年度の組織の財務状態を表示します。 このレポートには資産および負債、また株主の株主資本が並べて表示されています。                                                                                                                                                                                |
| [Summary Trial Balance – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)                          | 開始残高および決算残高、借方と貸方残高、およびそれらの正味差額が含まれるすべての勘定の残高情報を表示します。                                                                                                                                                                  |
| [Summary Trial Balance Year Over Year – Default](https://mix.office.com/watch/1ewwgbpv0iwrl)           | 現在の年と過最後の正味差異とともに開始残高と決算持つ、借方および貸方残高表示するすべての勘定の残高情報を。                                                                                                                           |
| [Weekly Sales and Discounts - Default](https://mix.office.com/watch/112ng0hy5de0j)                     | 1 か月の週単位の販売および割引についての洞察を得ます。 このレポートには、4 週間の合計が含まれます。                                                                                                                                                                                                              |
| [使用できる予算超過] -既定値 (https://mix.office.com/watch/15hcpezcbx7tv)                         | 変更された予算、実際の予算、引当、すべての勘定に使用できる予算超過比較の詳細を表示します。                                                                                                                                                                                  |

## <a name="opening-financial-reports"></a>財務諸表を開く
[**財務報告**] メニューをクリックすると、会社の既定の財務レポートの一覧が表示されます。 これにより、レポートを開くおよび変更できます。 既定のレポートの 1 つを開くには、レポートの名前を選択します。 レポートを初めて開くと、前の月のレポートが自動的に生成されます。 たとえば、2016年12月8のレポートを初めて開くと、レポートは2016年7年1月31日に生成されます。 レポートを開いた後、データの特定の部分をドリルダウンしたり、レポート オプションを変更することによりレポートの検討を開始できます。

## <a name="creating-and-modifying-financial-reports"></a>財務レポートの作成および変更
財務報告リストから、新しいレポートを作成するか、既存のレポートを変更できます。 適切なアクセス許可がある場合、新しい**クリックして**アクション ウィンドウで、[新しい財務諸表を作成できます。 レポート デザイナーの[デバイスにダウンロードします。 レポート デザイナが開始された後に、新しいレポートを作成できます。 新しいレポートは保存した後、財務報告リストに表示されます。 リストは、Dynamics 365 for Operationsで使用している会社に対して作成されたレポートのみを表示します。 Dynamics 365 for Operationsで財務諸表を作成および変更するプロセスに関する詳細については、以下を参照してくださいブログの[転記] (Dynamicsの財務報告にブログのhttps://blogs.msdn.microsoft.com/dynamics_financial_reporting/tag/learning/)です。 **注記: **レポート デザイナのクライアントをダウンロードしているコンピュータは、にインストールされているMicrosoft .NET Frameworkのバージョン4.6.2が必要です。 Microsoft .NET Frameworkのこのバージョンは、からダウンロードし、インストールできます。ここで[] (https://www.microsoft.com/en-us/download/details.aspx?id=53345)。 Chromeを使用すると、レポート デザイナのクライアントをダウンロードするにClickOnce拡張機能をインストールする必要があります。 incognitoモードで走ったら、ClickOnce拡張子をincognitoモードを有効になることを確認します。 財務報告リストに表示されるレポートは変更できます。 レポート名の周りの領域が選択されている場合、[アクション] ウィンドウの [**編集**] をクリックします。 レポート デザイナー プログラムが開始されます。

<a name="see-also"></a>参照
--------

[View financial reports](view-financial-reports.md)

[ Dynamics 財務報告ブログ](http://blogs.msdn.com/b/dynamics_financial_reporting/)


