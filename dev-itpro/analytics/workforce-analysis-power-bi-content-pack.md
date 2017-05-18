---
title: "Workforce Metrics Power BI コンテンツ"
description: "このトピックでは Dynamics 365 for Operations - Workforce Metrics Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 351306857ae62496fb28e9bb55dcbb11e7c3fd00
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="workforce-metrics-power-bi-content"></a>Workforce Metrics Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは Dynamics 365 for Operations - Workforce Metrics Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

<a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
--------------------------

Workforce Metrics コンテンツ パックは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリにあります。 コンテンツ パックのダウンロード方法および Microsoft Dynamics 365 for Operations データに接続する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックを Dynamics 365 for Operations データに接続した後に、レポートに組織のデータが表示されます。 Microsoft Power BI を以前に使用したことがない場合は、詳細については「[Power BI のガイド付きの学習](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート                                            | コンテンツ                                                                                                                                                                                                            |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 会社、部門、場所人数分析 | 会社別の人数、部門別の人数、場所別の人数、および総人数                                                                                                                           |
| 職務、ステップ、管理者人数分析            | 職務別の人数、ステップ別の人数、管理者別の人数、および総人数                                                                                                                                      |
| 人数傾向分析                         | 会社別の今年対去年の人数、および過去 12 か月のローリング人数                                                                                                                        |
| 従業員の人口統計                           | 年齢と性別ごとの人数、出身民族別の人数、ベテラン状態別の人数、配偶者の有無別の人数、フルタイム学生の数、平均勤続期間、平均年齢、男性従業員に対する女性の比率 |
| 職位分析                                | 部門別の空いている職位、欠員から採用済みになった職位、有効から無効になった職位、部門別の職位                                                                                                   |
| 縮小分析                               | 今年対去年の縮小、縮小、退職人員の平均勤続期間、退職人員の平均年齢、および理由があって退職する従業員                                                                   |
| 部署ごとの人員                             | 部門別の従業員の個人番号、職位、および割り当て開始日と終了日                                                                                                                       |
| 勤続分析                               | 会社と勤続リスト別の平均勤続年数                                                                                                                                                              |
| 記念日および勤続年数               | 勤続年数、記念日別の従業員                                                                                                                                                                    |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Dynamics 365 for Operations のデータを使用して、従業員メトリックス コンテンツ パックに情報を入力します。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                            | コンテンツ                                                                                                   | 他のエンティティとの関係                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | レポートをスライスするカレンダーのオフセット                                                                          | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workorce\_WorkerTrend Workforce\_TerminatedWorker                                                                                                                                                                                                                     |
| Workforce\_Company                | レポートをフィルター処理する会社                                                                             | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_Compensation           | 時間経過に伴う支払レートと頻度                                                                           | Workforce\_CurrentCompensation Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                        |
| Workforce\_CurrentCompensation    | 現在の日付時点の支払レートと頻度                                                              | Workforce\_Company Workforce\_Compensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | 現在の日付時点での職位、フルタイム相当 (FTE)、空いている職位、欠員から採用済みになった職位 | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                                               |
| Workforce\_CurrentWorker          | 現在の日付時点での作業者、期日経過日数、人員                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position Workforce\_WorkerBenefit                                            |
| Workforce\_Date                   | 日、週、月、年                                                                             | Workforce\_PastPositionAssignment Workforce\_PositionTrend Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                     |
| Workforce\_Demographics           | 生年月日、性別、出身民族、配偶者の有無                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Employment             | 開始日、終了日、移行日                                                                  | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_GeographicLocation     | 市町村、市区郡、郵便番号、都道府県                                                           | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Job                    | 職務、タイプ、役職                                                                                  | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_JobPerferredSkill      |                                                                                                            |                                                                                                                                                                                                                                                                                                                                  |
| Workforce\_PastPositionAssignment | 割り当て理由、開始日、終了日、職務                                                           | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_Performance            | 評価、説明、評価モデル                                                                      | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_PersonSkill            | レベルおよびスキル                                                                                            | Workforce\_Skill                                                                                                                                                                                                                                                                                                                 |
| Workforce\_PersonSkillAnalysis    | 認定済みレベルおよびスキル                                                                                | Workforce\_Skill Workforce\_WorkerName                                                                                                                                                                                                                                                                                           |
| Workforce\_Position               | 部門、FTE、職位、職位のタイプ、役職                                                        | Workforce\_CurrentPosition Workforce\_CurrentWorker                                                                                                                                                                                                                                                                              |
| Workforce\_PositionTrend          | 時間経過に伴う職位、FTE、職務                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                     |
| Workforce\_ReportsToWorkerName    | 名、姓、フルネーム                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_Skill                  | スキル、スキル タイプおよび評価                                                                              | Workforce\_PersonSkill Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                                                                            |
| Workforce\_TerminatedWorker       | 退職済作業者、退職日、役職、職位、職務                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position Workforce\_WorkerBenefit |
| Workforce\_WorkerBenefit          | 有効日、福利厚生オプション、福利厚生計画、福利厚生タイプ                                             | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workforce\_WorkerName             | 名、姓、フルネーム                                                                       | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend Workforce\_PersonSkillAnalysis                                                                                                                                                                                                                        |
| Workforce\_WorkerTitle            | 役職と勤続日数                                                                                   | Workforce\_CurrentWorker Workforce\_TerminatedWorker Workorce\_WorkerTrend                                                                                                                                                                                                                                                       |
| Workorce\_WorkerTrend             | 時間経過に伴う作業者、人員、会社、職位                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_WorkerBenefit                     |

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、主要業績評価指標 (KPI) およびコンテンツ パックで使用するためのレポートを計算するために使用されます。 レポートおよびダッシュボードに追加の計算を含める場合は、LCS から CompensationandBenefits.pbix ファイルをダウンロードして変更することができます。 このファイルはコンテンツ パックを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





