---
title: "与信および回収管理 Power BI コンテンツ"
description: "このトピックでは、与信および回収管理 Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations. Core
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5f08df6cb8549e87e123b10c5a771ae1c60ff39c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="credit-and-collections-management-power-bi-content"></a>与信および回収管理 Power BI コンテンツ

このトピックでは、**与信および回収管理** Microsoft Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**与信および回収管理** Power BI コンテンツは、与信および回収マネージャー、そして回収係のために作成されています。 売掛債権回転日数、延滞残高、クレジット エクスポージャ、与信限度額を超えた顧客など、主要な与信および回収のメトリックスを提供します。 トランザクション データを使用し、すべての会社の与信および回収の集計ビューを提供します。 会社、顧客グループ、および顧客ごとの内訳も提供します。

この Power BI コンテンツは、10 のレポート ページで構成されます。

- 2 つの概要ページ (与信の概要に 1 ページと回収の概要に 1 ページ)
- さまざまな分析コードで解析された与信および回収のメトリックスの詳細を提供する 8 つの詳細ページ

すべての金額はシステム通貨で表示されます。 システム通貨は、[**システム パラメーター**] ページで設定できます。

既定では、現在の会社の与信および回収のデータが表示されます。 すべての会社のデータを表示するには、**CustCollectionsBICrossCompany** 職務権限をロールに割り当てます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition (2017 年 7 月) を使用している場合、**与信および回収管理** Power BI コンテンツは**顧客の与信および回収**ワークスペースで表示されます。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート

**CustCollectionsBICrossCompany** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれています。 これらのメトリックスはグラフ、タイル、表として視覚化されます。 次の表に、**CustCollectionsBICrossCompany** Power BI コンテンツの表示の概要を示します。

| レポート ページ                 | 視覚化 |
|-----------------------------|---------------|
| 回収の概要        | <ul><li>期日が経過した顧客</li><li>与信限度額を超えた顧客</li><li>DSO 30 日間</li><li>オープンなケース</li><li>ケースがクローズするまでの平均日数</li><li>オープンな活動</li><li>活動をクローズするまでの平均日数</li><li>利子計算書を開く</li><li>督促状を開く</li><li>顧客保留</li><li>販売保留</li><li>指定の期間に達している残高</li><li>回収状態の金額</li><li>回収コードの金額</li><li>理由ごとの損金処理</li><li>地域ごとの未払い残高</li><li>支払予定</li></ul> |
| 与信の概要             | <ul><li>期日が経過した顧客</li><li>与信限度額と未払い残高</li><li>与信限度額グリッドを超えた顧客</li><li>会社ごとの与信限度額を超えた顧客</li><li>使用されたクレジットと与信限度額合計</li><li>与信限度額と地域ごとの使用されたクレジット</li><li>信用格付けごとの顧客</li></ul> |
| 与信限度額                | <ul><li>与信限度額</li><li>与信限度額詳細</li><li>顧客ごとの与信限度額</li><li>顧客グループごとの与信限度額</li><li>会社ごと、信用格付けごとの与信限度額</li><li>与信限度額と地域で使用されたクレジット</li></ul> |
| 与信限度額を超えた顧客 | <ul><li>与信限度額を超えた顧客</li><li>与信限度額を超えた顧客の詳細</li><li>会社ごとの与信限度額を超えた顧客</li><li>顧客グループごとの与信限度額を超えた顧客</li><li>地域ごとの与信限度額を超えた顧客</li></ul> |
| 期日が経過した顧客          | <ul><li>期日が経過した顧客</li><li>期日が経過した顧客の詳細</li><li>会社ごとの期日が経過した顧客</li><li>顧客グループごとの期日が経過した顧客</li><li>地域ごとの期日が経過した顧客</li></ul> |
| 指定の期間に達している残高               | <ul><li>指定の期間に達している残高</li><li>指定の期間に達している残高の詳細</li><li>会社ごとの指定の期間に達している残高</li><li>顧客グループごとの指定の期間に達している残高</li></ul> |
| 支払予定           | <ul><li>支払予定</li><li>支払予定の詳細</li><li>会社ごとの予期される支払い</li><li>顧客グループごとの予期される支払い</li><li>地域ごとの予期される支払い</li></ul> |
| 損金処理                  | <ul><li>地域による損金処理</li><li>損金処理の詳細</li><li>主勘定による損金処理</li><li>会社ごとの損金処理</li><li>顧客グループごとの損金処理</li><li>地域による損金処理</li></ul> |
| 回収状態          | <ul><li>争議中</li><li>支払の約束が破棄されました</li><li>支払約束</li><li>回収状態の詳細</li><li>回収状態の金額</li><li>オープンなケース</li><li>オープンな活動</li></ul> |
| 督促状         | <ul><li>督促状コードの金額</li><li>回収コードの量の詳細</li><li>会社別の督促状の量</li><li>顧客グループ別の督促状の量</li><li>地域ごとの督促状の量</li></ul> |

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/) を参照してください。 また、基になるデータのエクスポート機能を使用して、視覚化で要約されている基になるデータをエクスポートすることができます。

## <a name="extending-the-power-bi-content"></a>Power BI コンテンツの拡張
Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Finance and Operations にログインしない人々に関する優れた分析ができます。 ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。

LCS の共有資産ライブラリに **与信および回収管理** Power BI コンテンツがあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](../../dev-itpro/analytics/power-bi-content-microsoft-partners.md)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

ご使用のバージョンの Finance and Operations に適用する **与信および回収管理** Power BI コンテンツをダウンロードしてください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

次のデータは、**与信および回収管理** Power BI コンテンツのレポートに入力するために使用されます。 このデータは、エンティティ ストアで実施される集計の測定として表されます。 エンティティ ストアは、分析に最適化された Microsoft SQL Server データベースです。 詳細については、「[エンティティ ストアとの Power BI の統合](../../dev-itpro/analytics/power-bi-integration-entity-store.md)」を参照してください。

| エンティティ                                      | キー集計の測定           | データ ソース                                 | フィールド                                                      | 説明 |
|---------------------------------------------|--------------------------------------|---------------------------------------------|------------------------------------------------------------|-------------|
| CustCollectionsBIActivitiesAverageCloseTime | NumOfActivities, AveragecClosedTime  | smmActivities                               | AverageOfChildren(AverageClosedTime) Count(ActivityNumber) | 終了した活動の数およびそれらの活動を終了する平均時間。 |
| CustCollectionsBIActivitiesOpen             | ActivityNumber                       | smmActivities                               | Count(ActivityNumber)                                      | オープンな活動の数。 |
| CustCollectionsBIAgedBalances               | AgedBalances                         | CustCollectionsBIAgedBalancesView           | Sum(SystemCurrencyBalance)                                 | 指定の期間に達している残高の合計。 |
| CustCollectionsBIBalancesDue                | SystemCurrencyAmount                 | CustCollectionsBIBalanceDueView             | Sum(SystemCurrencyAmount)                                  | 期限切れの金額。 |
| CustCollectionsBICaseAverageCloseTIme       | NumOfCases, CaseAverageClosedTime    | CustCollectionsCaseDetail                   | AverageOfChildren(CaseAverageClosedTime) Count(NumOfCases) | 終了したケースの数およびそれらのケースを終了する平均時間。 |
| CustCollectionsBICasesOpen                  | CaseId                               | CustCollectionsCaseDetail                   | Count(CaseId)                                              | オープンなケースの数。 |
| CustCollectionsBICollectionLetter           | CollectionLetterNum                  | CustCollectionLetterJour                    | Count(CollectionLetterNum)                                 | オープンな督促状の数。 |
| CustCollectionsBICollectionLetterAmount     | CollectionLetterAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | 転記済督促状の残高。 |
| CustCollectionsBICollectionStatus           | CollectionStatusAmounts              | CustCollectionsBIAccountsReceivables        | Sum(SystemCurrencyAmount)                                  | 回収状態のトランザクションの残高。 |
| CustCollectionsBICredit                     | CreditExposed, AmountOverCreditLimit | CustCollectionsBICreditView                 | Sum(CreditExposed), Sum(AmountOverCreditLimit)             | クレジット エクスポージャおよび顧客が与信限度額を超えている金額の合計値。 |
| CustCollectionsBICustOnHold                 | ブロック                              | CustCollectionsBICustTable                  | Count(Blocked)                                             | 保留中の顧客の数。 |
| CustCollectionsBIDSO                        | DSO30                                | CustCollectionsBIDSOView                    | AverageOfChildren(DSO30)                                   | 30 日の売掛債権回転日数 |
| CustCollectionsBIExpectedPayment            | ExpectedPayment                      | CustCollectionsBIExpectedPaymentView        | Sum(SystemCurrencyAmounts)                                 | 翌年度内の予期される支払いの合計。 |
| CustCollectionsBIInterestNote               | InterestNote                         | CustInterestJour                            | Count(InterestNote)                                        | 作成済の利子計算書の数。 |
| CustCollectionsBISalesOnHold                | SalesId                              | SalesTable                                  | Count(SalesId)                                             | 保留中の販売注文の合計数。 |
| CustCollectionsBIWriteOff                   | WriteOffAmount                       | CustCollectionsBIWriteOffView               | Sum(SystemCurrencyAmount)                                  | 損金処理済のトランザクションの合計。 |

