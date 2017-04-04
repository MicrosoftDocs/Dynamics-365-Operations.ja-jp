---
title: "従業員のメトリックスのPower BIの内容"
description: "このトピックでは、-従業員のメトリックスのPower BIの内容365 for Operationsについて説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 264084
ms.assetid: 8e700583-3a7d-4f5f-9ac8-58c4feed1a02
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: d03692e39c51cc4eb0fe23ba263e52de2bf3c3da
ms.lasthandoff: 03/31/2017


---

# <a name="workforce-metrics-power-bi-content"></a>従業員のメトリックスのPower BIの内容

このトピックでは、-従業員のメトリックスのPower BIの内容365 for Operationsについて説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。

<a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
--------------------------

Microsoft Dynamics Lifecycle Services (LCS)の共有資産のライブラリの従業員のメトリックスの内容Packを検索できます。 コンテンツ パックをダウンロードし、データのMicrosoft Dynamics 365に接続する方法の詳細については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
工程365 for OperationsデータにコンテンツPack接続されたら、レポートは、組織のデータが表示されます。 は、Microsoft Power BIの前に使用していない場合は、そのコンフィギュレーションに関する情報を入手ことができます。[導かれるPower BI説明します] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)のページを。 コンテンツ パックに含まれるレポートに追加情報を含むテーブルの両方とグラフがあります。 次の表にレポートを示します。

| レポート                                            | コンテンツ                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Analysis Headcount "会社"の部門、場所 | 会社による人員、部門別人員、場所別の人数、および合計人員                                                                                                                           |
| 人員の分析ジョブ、手順は、マネージャー            | ジョブの人員、ステップ別の人員、マネージャ別の人数、および合計人員                                                                                                                                      |
| 人員の傾向分析                         | 会社による最後対人数最後の12か月の今年度、ローリングの人員                                                                                                                        |
| 従業員の人口統計                           | 期間と性別別の人員、種族出身的による人員、情報のステータス別人員、配偶者の有無による人員、フルタイムのバージョン番号、オスの従業員に女性の平均勤続、平均期間となります。 |
| 分析を設定します。                                | 部門別開職位、部門別に未処理満ちた職位、有効に無効な職位、および職位                                                                                                   |
| 摩擦の分析                               | 最後の対象摩擦理由によって去って従業員の個人の今年度、摩擦、去っての平均期間去って平均および従業員の勤続                                                                   |
| 部署ごとの人員                             | 部門別個人の従業員番号、職位、および代入の開始日と終了日                                                                                                                       |
| 勤続年数の分析                               | 会社と上級別の平均勤続年数を示します。                                                                                                                                                              |
| 記念日および勤続年数               | 勤続年数で従業員、および記念日                                                                                                                                                                    |

これらのレポートのグラフとタイルをフィルタ処理しダッシュボードにとグラフをタイルでそのPIN。 Power BIにフィルタPINでな方法の詳細について表示する[ダッシュボード作成してコンフィギュレーション] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)を。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for Operationsデータが従業員のメトリックスの内容パックのレポートの情報も使用されます。 次の表に、コンテンツ パックが基づいているエンティティに示します。

| エンティティ                            | コンテンツ                                                                                                   | 他のエンティティとの関係                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 全従業員\_CalendarOffset         | スライス レポートへのカレンダーの相殺                                                                          | 従業員の\_PastPositionAssignmentの従業員の\_PositionTrend Workorce\_WorkerTrendに、従業員\_TerminatedWorker                                                                                                                                                                                                                     |
| 従業員の\_会社                | レポートをフィルタ処理する会社                                                                             | 従業員の\_CurrentCompensationの従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| 従業員の\_           | 支払レートと頻度の条件に従って                                                                           | 従業員の\_CurrentCompensationの従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| 全従業員\_CurrentCompensation    | 現在の日付の支払レートと頻度                                                              | 従業員の\_会社の従業員の\_に、従業員\_人口統計の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                            |
| 全従業員\_CurrentPosition        | 現在の日付、フルタイムに同等の(FTE)、開職位、オープンに満ちた職位現在の職位 | 従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                                                                                               |
| 全従業員\_CurrentWorker          | 現在の日付、期間、人員現在の労働災害                                                         | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_ジョブ、従業員の\_の\_の従業員の\_職位に、従業員\_WorkerBenefit                                            |
| 従業員の\_日付                   | 日、週、月、年                                                                             | 従業員の\_PastPositionAssignmentの従業員の\_PositionTrendに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| 従業員の\_人口統計           | 、性別、種族的出身と配偶者の有無誕生日                                                   | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 従業員の雇用\_             | 開始日、終了日、および遷移の日付                                                                  | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 全従業員\_GeographicLocation     | 市町村、郵便番号、市区郡、都道府県または地域                                                           | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 従業員の\_ジョブ                    | 職務、および職位タイプ                                                                                  | 従業員の\_CurrentPositionに、従業員\_CurrentWorker                                                                                                                                                                                                                                                                              |
| 全従業員\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| 全従業員\_PastPositionAssignment | 割り当て理由、開始日、終了日、およびジョブ                                                           | 従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                                                     |
| 従業員の業績\_            | 評価、説明、および評価モデル                                                                      | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 全従業員\_PersonSkill            | スキル レベルと                                                                                            | 従業員の\_スキル                                                                                                                                                                                                                                                                                                                 |
| 全従業員\_PersonSkillAnalysis    | されるして、スキル、証明書                                                                                | 従業員の\_スキルに、従業員\_WorkerName                                                                                                                                                                                                                                                                                           |
| 従業員の\_位置               | 部門、FTE、職位、および職位のタイプ。                                                        | 従業員の\_CurrentPositionに、従業員\_CurrentWorker                                                                                                                                                                                                                                                                              |
| 全従業員\_PositionTrend          | 職位の条件に従って、およびジョブFTE                                                                          | 従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                                                     |
| 全従業員\_ReportsToWorkerName    | 名]ボックスに、完全名                                                                       | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 従業員の\_スキル                  | スキル、スキル タイプおよび評価                                                                              | 従業員の\_PersonSkillに、従業員\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| 全従業員\_TerminatedWorker       | 完成したため、終了日、タイトル、職位、およびジョブ                                             | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_の\_の従業員の\_ジョブ、従業員の\_職位に、従業員\_WorkerBenefit |
| 全従業員\_WorkerBenefit          | 有効日、福利厚生オプション、福利プラン、福利厚生タイプ                                             | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| 全従業員\_WorkerName             | 名]ボックスに、完全名                                                                       | 従業員の\_CurrentWorkerの従業員の\_TerminatedWorker Workorce\_WorkerTrendに、従業員\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| 全従業員\_WorkerTitle            | タイトルと上級の日付                                                                                   | 従業員の\_CurrentWorkerに、従業員\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | ための条件に従って、人員、会社と職位                                                        | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_の\_の従業員の\_ジョブ、従業員\_WorkerBenefit                     |

これらのエンティティがデータ モデルの計算メジャーを作成するのに使用されます。 これらの計算メジャーは、コンテンツ パックで使用されるレポートおよび主要業績評価指標(KPIs)を計算するために使用します。 レポートおよびダッシュボードの追加の計算を含める場合は、LCSからのCompensationandBenefits.pbixファイルのダウンロードを変更できます。 このファイルはコンテンツ パックを作成するのに使用される既定のデータ モデルです。 変更をすると、追加した情報を含むダッシュボードと組織のコンテンツ パックを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



