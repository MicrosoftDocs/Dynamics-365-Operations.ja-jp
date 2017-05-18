---
title: "従業員のコンピテンシーと開発 Power BI コンテンツ"
description: "このトピックでは、Dynamics 365 for Operations - 従業員のコンピテンシーと開発 Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263894
ms.assetid: 7d375d8a-b2de-4bec-b575-93d1d4521b79
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 48a12a32fd6a0d95f50b98e6533173265b9867ab
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>従業員のコンピテンシーと開発 Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは、Dynamics 365 for Operations - 従業員のコンピテンシーと開発 Power BI コンテンツについて説明します。 コンテンツ パックに含まれているレポートにアクセスする方法を説明し、コンテンツ パックを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

<a name="accessing-the-content-pack"></a>コンテンツ パックへのアクセス
--------------------------

従業員のコンピテンシーと開発コンテンツ パックは、Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリにあります。 コンテンツ パックのダウンロード方法および Microsoft Dynamics 365 for Operations データに接続する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
コンテンツ パックを Dynamics 365 for Operations データに接続した後に、レポートに組織のデータが表示されます。 Microsoft Power BI を以前に使用したことがない場合は、詳細については「[Power BI のガイド付きの学習](https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)」を参照してください。 コンテンツ パックに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート                             | コンテンツ                                               |
|-----------------------------------|--------------------------------------------------------|
| コンピテンシーと開発の分析 | チーム メンバーのスキル タイプとタイプ別のチーム メンバーのスキル |
| スキル プロファイル                     | 選択された従業員のスキル プロファイル                |
| スキル分析                    | タイプ別スキルおよび評価                              |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
Dynamics 365 for Operations データを使用して、従業員のコンピテンシーと開発コンテンツ パックにレポートを入力します。 次の表に、コンテンツ パックが基づいているエンティティを示します。

| エンティティ                            | コンテンツ                                                                                                   | 他のエンティティとの関係                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Workforce\_CalendarOffset         | レポートをスライスするカレンダーのオフセット                                                                          |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Company                | レポートをフィルター処理する会社                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Compensation           | 時間経過に伴う支払レートと頻度                                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_CurrentCompensation    | 現在の日付時点の支払レートと頻度                                                              | Workforce\_Company Workforce\_CurrentCompensation Workforce\_Demographics Workforce\_Job Workforce\_Position                                                                                                                                                                                            |
| Workforce\_CurrentPosition        | 現在の日付時点での職位、フルタイム相当 (FTE)、空いている職位、欠員から採用済みになった職位 | Workforce\_Job Workforce\_Position                                                                                                                                                                                                                                                                      |
| Workforce\_CurrentWorker          | 現在の日付時点での作業者、期日経過日数、人員                                                         | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_PersonSkill Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Job Workforce\_Employment Workforce\_Position                     |
| Workforce\_Date                   | 日、週、月、年                                                                             |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Demographics           | 生年月日、性別、出身民族、配偶者の有無                                                   |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Employment             | 開始日、終了日、移行日                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_GeographicLocation     | 市町村、市区郡、郵便番号、都道府県                                                           |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Job                    | 職務、タイプ、役職                                                                                  |                                                                                                                                                                                                                                                                                                         |
| Workforce\_JobPreferredSkill      | 重要性、評価、スキル、スキル レベル                                                                 | Workforce\_Skill Workforce\_Job                                                                                                                                                                                                                                                                         |
| Workforce\_PastPositionAssignment | 割り当て理由、開始日、終了日、職務                                                           | Workforce\_ClaendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_Performance            | 評価、説明、評価モデル                                                                      |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PersonSkill            | レベル、取得日、スキル                                                                               | Workforce\_Skill                                                                                                                                                                                                                                                                                        |
| Workforce\_PersonSkillAnalysis    | 証明済、レベル、取得日、スキル                                                                    | Workforce\_WorkerName Workforce\_Skill                                                                                                                                                                                                                                                                  |
| Workforce\_Position               | 部門、FTE、職位、職位のタイプ、役職                                                        |                                                                                                                                                                                                                                                                                                         |
| Workforce\_PositionTrend          | 時間経過に伴う職位、FTE、職務                                                                          | Workforce\_CalendarOffset Workforce\_Date Workforce\_Job Workforce\_Position                                                                                                                                                                                                                            |
| Workforce\_ReportsToWorkerName    | 名、姓、フルネーム                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_Skill                  | スキル、スキル タイプおよび評価                                                                              |                                                                                                                                                                                                                                                                                                         |
| Workforce\_TerminatedWorker       | 退職済作業者、退職日、役職、職位、職務                                             | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job Workforce\_Position |
| Workforce\_WorkerName             | 名、姓、フルネーム                                                                       |                                                                                                                                                                                                                                                                                                         |
| Workforce\_WorkerTitle            | 役職と勤続日数                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | 時間経過に伴う作業者、人員、会社、職位                                                        | Workforce\_Company Workforce\_Compensation Workforce\_GeographicLocation Workforce\_Performance Workforce\_WorkerName Workforce\_ReportsToWorkerName Workforce\_CalendarOffset Workforces\_Date Workforce\_WorkerTitle Workforce\_Demographics Workforce\_Employment Workforce\_Job                     |

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、主要業績評価指標 (KPI) およびコンテンツ パックで使用するためのレポートを計算するために使用されます。 レポートおよびダッシュボードに追加の計算を含める場合は、LCS から CompetenciesandDevelopment.pbix ファイルをダウンロードして変更することができます。 このファイルはコンテンツ パックを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)





