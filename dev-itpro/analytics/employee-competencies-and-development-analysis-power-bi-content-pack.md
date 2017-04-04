---
title: "従業員の能力や開発のPower BIの内容"
description: "このトピックでは、Dynamics 365 for Operationsの従業員の能力や開発のPower BIの内容について説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。"
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
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1fd6f978b6a871f9f7d3d5e91ab3e0aac789ae88
ms.lasthandoff: 03/31/2017


---

# <a name="employee-competencies-and-development-power-bi-content"></a>従業員の能力や開発のPower BIの内容

このトピックでは、Dynamics 365 for Operationsの従業員の能力や開発のPower BIの内容について説明します。 コンテンツ パックに含まれる説明し、コンテンツ パックを作成するのに使用されたエンティティとデータ モデルに関する情報を提供するレポートにアクセスする方法。

<a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
--------------------------

Pack、Microsoft Dynamics Lifecycle Services (LCS)の共有資産のライブラリの従業員の能力や開発の内容の検索できます。 コンテンツ パックをダウンロードし、データのMicrosoft Dynamics 365に接続する方法の詳細については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
工程365 for OperationsデータにコンテンツPack接続されたら、レポートは、組織のデータが表示されます。 は、Microsoft Power BIの前に使用していない場合は、そのコンフィギュレーションに関する情報を入手ことができます。[導かれるPower BI説明します] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)のページを。 コンテンツ パックに含まれるレポートに追加情報を含むテーブルの両方とグラフがあります。 次の表にレポートを示します。

| レポート                             | コンテンツ                                               |
|-----------------------------------|--------------------------------------------------------|
| 能力と開発の分析 | タイプ別にチーム メンバのスキル タイプとチーム メンバのスキル |
| スキル プロファイル                     | 選択した従業員のスキル プロファイル                |
| スキルの分析                    | タイプおよび評価別のスキル                              |

これらのレポートのグラフとタイルをフィルタ処理しダッシュボードにとグラフをタイルでそのPIN。 Power BIにフィルタPINでな方法の詳細について表示する[ダッシュボード作成してコンフィギュレーション] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)を。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for Operationsデータが従業員の能力や開発の内容のレポートの情報もパック使用されます。 次の表に、コンテンツ パックが基づいているエンティティに示します。

| エンティティ                            | コンテンツ                                                                                                   | 他のエンティティとの関係                                                                                                                                                                                                                                                                       |
|-----------------------------------|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 全従業員\_CalendarOffset         | スライス レポートへのカレンダーの相殺                                                                          |                                                                                                                                                                                                                                                                                                         |
| 従業員の\_会社                | レポートをフィルタ処理する会社                                                                             |                                                                                                                                                                                                                                                                                                         |
| 従業員の\_           | 支払レートと頻度の条件に従って                                                                           |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_CurrentCompensation    | 現在の日付の支払レートと頻度                                                              | 従業員の\_会社の従業員の\_CurrentCompensationに、従業員\_人口統計の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                            |
| 全従業員\_CurrentPosition        | 現在の日付、フルタイムに同等の(FTE)、開職位、オープンに満ちた職位現在の職位 | 従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                                                                      |
| 全従業員\_CurrentWorker          | 現在の日付、期間、人員現在の労働災害                                                         | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_PersonSkillの従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_ジョブ、従業員の\_の\_の従業員の\_位置                     |
| 従業員の\_日付                   | 日、週、月、年                                                                             |                                                                                                                                                                                                                                                                                                         |
| 従業員の\_人口統計           | 、性別、種族的出身と配偶者の有無誕生日                                                   |                                                                                                                                                                                                                                                                                                         |
| 従業員の雇用\_             | 開始日、終了日、および遷移の日付                                                                  |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_GeographicLocation     | 市町村、郵便番号、市区郡、都道府県または地域                                                           |                                                                                                                                                                                                                                                                                                         |
| 従業員の\_ジョブ                    | 職務、および職位タイプ                                                                                  |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_JobPreferredSkill      | 他の評価、スキル、スキル レベル                                                                 | 従業員の\_のスキルの従業員の\_ジョブ                                                                                                                                                                                                                                                                         |
| 全従業員\_PastPositionAssignment | 割り当て理由、開始日、終了日、およびジョブ                                                           | 従業員の\_ClaendarOffsetの従業員の\_日付の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                            |
| 従業員の業績\_            | 評価、説明、および評価モデル                                                                      |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_PersonSkill            | レベル、およびスキル レベルな日付                                                                               | 従業員の\_スキル                                                                                                                                                                                                                                                                                        |
| 全従業員\_PersonSkillAnalysis    | 認定、レベルで、[な日付およびスキル                                                                    | 従業員の\_WorkerNameの従業員の\_スキル                                                                                                                                                                                                                                                                  |
| 従業員の\_位置               | 部門、FTE、職位、および職位のタイプ。                                                        |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_PositionTrend          | 職位の条件に従って、およびジョブFTE                                                                          | 従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_ジョブ、従業員の\_位置                                                                                                                                                                                                                            |
| 全従業員\_ReportsToWorkerName    | 名]ボックスに、完全名                                                                       |                                                                                                                                                                                                                                                                                                         |
| 従業員の\_スキル                  | スキル、スキル タイプおよび評価                                                                              |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_TerminatedWorker       | 完成したため、終了日、タイトル、職位、およびジョブ                                             | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_の\_の従業員の\_ジョブ、従業員の\_位置 |
| 全従業員\_WorkerName             | 名]ボックスに、完全名                                                                       |                                                                                                                                                                                                                                                                                                         |
| 全従業員\_WorkerTitle            | タイトルと上級の日付                                                                                   |                                                                                                                                                                                                                                                                                                         |
| Workorce\_WorkerTrend             | ための条件に従って、人員、会社と職位                                                        | 従業員の\_会社の従業員の\_の従業員の\_GeographicLocationの従業員の\_パフォーマンス、従業員の\_WorkerNameの従業員の\_ReportsToWorkerNameの従業員の\_CalendarOffsetの従業員の\_日付の従業員の\_WorkerTitleに、従業員\_人口統計の従業員の\_の\_の従業員の\_ジョブ                     |

これらのエンティティがデータ モデルの計算メジャーを作成するのに使用されます。 これらの計算メジャーは、コンテンツ パックで使用されるレポートおよび主要業績評価指標(KPIs)を計算するために使用します。 レポートおよびダッシュボードの追加の計算を含める場合は、LCSからのCompetenciesandDevelopment.pbixファイルのダウンロードを変更できます。 このファイルはコンテンツ パックを作成するのに使用される既定のデータ モデルです。 変更をすると、追加した情報を含むダッシュボードと組織のコンテンツ パックを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



