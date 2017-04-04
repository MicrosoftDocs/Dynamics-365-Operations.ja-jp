---
title: Organizational Training Power BI content
description: "このトピックでは、]Power BI組織のトレーニングの内容365 for Operationsについて説明します。 コンテンツ パックへのアクセス方法を説明しコンテンツ パックを作成するのに使用されたエンティティとデータ モデルについて説明します。"
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 263874
ms.assetid: 45dbba14-aba6-4571-be0d-5d1aba3515d9
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 104164f8ffd0d2bc3a64bf15d2fb5213234046ce
ms.lasthandoff: 03/31/2017


---

# <a name="organizational-training-power-bi-content"></a>Organizational Training Power BI content

このトピックでは、]Power BI組織のトレーニングの内容365 for Operationsについて説明します。 コンテンツ パックへのアクセス方法を説明しコンテンツ パックを作成するのに使用されたエンティティとデータ モデルについて説明します。

<a name="accessing-the-content-pack"></a>コンテンツPackのアクセス
--------------------------

Microsoft Dynamics Lifecycle Services (LCS)の共有資産のライブラリの組織のトレーニングの内容Packを検索できます。 コンテンツ パックをダウンロードし、データのMicrosoft Dynamics 365に接続する方法の詳細については、" "を参照してください]、[Microsoftパートナー (能力Bi内容Microsoft partners.md) のLCSのPower BIの内容。

## <a name="reports-that-are-included-in-the-content-pack"></a>コンテンツ パックに含まれるレポート
工程365 for OperationsデータにコンテンツPack接続されたら、レポートは、組織のデータが表示されます。 は、Microsoft Power BIの前に使用していない場合は、そのコンフィギュレーションに関する情報を入手ことができます。[導かれるPower BI説明します] (https://powerbi.microsoft.com/en-us/guided-learning/?WT.mc_id=PBIService_GetData)のページを。 コンテンツ パックに含まれるレポートに追加情報を含むテーブルの両方とグラフがあります。 次の表にレポートを示します。

| レポート           | コンテンツ                                                                    |
|-----------------|-----------------------------------------------------------------------------|
| コースの分析 | 場所ごとに登録、ステータス別コースの出席者、および登録リスト |
| コース タイプ    | スキル別コース タイプ                                                       |

これらのレポートのグラフとタイルをフィルタ処理しダッシュボードにとグラフをタイルでそのPIN。 Power BIにフィルタPINでな方法の詳細について表示する[ダッシュボード作成してコンフィギュレーション] (https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)を。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
工程365 for Operationsデータが組織のトレーニングの内容パックのレポートの情報も使用されます。 次の表に、コンテンツ パックが基づいているエンティティに示します。

| エンティティ                    | コンテンツ                                                         | 他のエンティティとの関係                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| トレーニング\_CalendarOffset  | スライス レポートへのカレンダーの相殺                                | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニングの\_の会社         | レポートをフィルタ処理する会社                                   | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニング コース\_          | コース、説明、講師名、場所、スペース、ステータス | \_CourseSkillを実施する\_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                             |
| トレーニング\_CourseAgenda    | コース日程、および開始時刻と終了時刻                          | \_コースを実施する\_日付を実施する\_CalendarOffsetを実施するトレーニングの\_会社                                                                                                                         |
| トレーニング\_CourseAttendees | 名前、ステータス、ジョブ、および登録日付                         | \_トレーニングの\_位置を実施する\_WorkerTitleを実施する\_WorkerNameを実施する\_コースを実施する\_雇用を実施する\_人口統計を実施する\_日付を実施する\_CalendarOffsetを実施するトレーニングの\_会社 |
| トレーニング\_CourseSkill     | スキル、スキル タイプとレベル                                     | トレーニング コース\_                                                                                                                                                                                   |
| トレーニングの\_の日付            | 日、週、月、年                                   | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニング\_人口統計    | 、性別、種族的出身と配偶者の有無誕生日         | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニングの\_の雇用      | 開始日、終了日、および遷移の日付                        | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニングの\_ジョブ             | 職務、および職位タイプ                                        | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニングの\_の位置        | 職位、タイトルと完全に同等の(FTE)                  | \_CourseAttendeesを実施するトレーニング\_CourseAgenda                                                                                                                                                   |
| トレーニング\_WorkerName      | 名]ボックスに、完全名                             | トレーニング\_CourseAttendees                                                                                                                                                                          |
| トレーニング\_WorkerTitle     | タイトルと上級の日付                                         | トレーニング\_CourseAttendees                                                                                                                                                                          |

これらのエンティティがデータ モデルの計算メジャーを作成するのに使用されます。 これらの計算メジャーは、コンテンツ パックで使用されるレポートおよび主要業績評価指標(KPIs)を計算するために使用します。 レポートおよびダッシュボードの追加の計算を含める場合は、LCSからのTraining.pbixファイルのダウンロードを変更できます。 このファイルはコンテンツ パックを作成するのに使用される既定のデータ モデルです。 変更をすると、追加した情報を含むダッシュボードと組織のコンテンツ パックを作成できます。

## <a name="additional-resources"></a>追加リソース
エンティティと建物 Power BI の内容に関連する役立つリンクを次に示します:

-   [データ エンティティ](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/)
-   [組織のコンテンツ パックの作成](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Power BI を使用したデータのモデル化](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Power BI タイルをワークスペースへ追加する](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/07/06/pinning-power-bi-reports-to-dynamics-ax-client/)



