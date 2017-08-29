---
title: "学習 Power BI コンテンツ"
description: "このトピックでは、学習 Power BI コンテンツについて説明します。 レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: jcart1106
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations, Talent, Core
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a3f28d21a7e73d3ad462c5cc37198dd2b6f5f8af
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="learning-power-bi-content"></a>学習 Power BI コンテンツ

[!include[banner](../includes/banner.md)]

このトピックでは、[**学習**] Microsoft Power BI コンテンツについて説明します。 コンテンツにアクセスする方法、およびコンテンツを構築するために使用されたデータ モデルとエンティティについて説明します。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

Microsoft Dynamics 365 for Finance および Operations、Enterprise Edition 2017 年 7 月の更新プログラムを使用している場合は、[**学習**] Power BI コンテンツは Microsoft Dynamics Lifecycle Services (LCS) 内の共有アセットライブラリにあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート

[**学習**] Power BI コンテンツに含まれるレポートには、追加情報を含むグラフとテーブルの両方があります。 次の表にレポートを示します。

| レポート                 | コンテンツ |
|-----------------------|----------|
| 学習の概要     | 他のレポートの集計 |
| コースの分析       | 場所による登録、ステータスによる出席者、コース、会社ごとのタイプによるコース、およびジョブによるコースの出席 |
| 登録分析 | 登録リスト |
| コースのタイプ          | スキル別コース タイプ |
| 講師分析   | 講師に対してコースの比率、講師の数、講師によるコース、講師あたりのコース、および講師によるコース議題 |
| 提供されているコース       | コースの一覧 |
| コースのデザイン        | コースの議題 |

これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、「[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards)」を参照してください。

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

次のデータを使用して、[**学習**] Power BI コンテンツのレポートを入力します。 この表に、コンテンツが基づいているエンティティを示します。

| エンティティ           | コンテンツ                                                         | 他のエンティティとの関係 |
|------------------|------------------------------------------------------------------|-----------------------------------|
| カレンダーのオフセット  | レポートをスライスするカレンダーのオフセット                                | コース議題、コース参加者 |
| 法人          | レポートをフィルター処理する会社                                   | コース議題、コース参加者 |
| コース           | コース、説明、講師名、場所、部屋、およびステータス | コース議題、コース参加者、コース スキル |
| コース議題    | 議題、コース、および開始時間と終了時間                          | 会社、カレンダーのオフセット、日付、コース |
| コース出席者 | 名前、ステータス、ジョブ、および登録日付                         | 会社、カレンダーのオフセット、日付、コース、従業員層、雇用、コース、従業員名、従業員の肩書き、職務、職位 |
| コース スキル     | スキル、スキル タイプ、およびレベル                                     | コース |
| 日             | 日、週、月、年                                   | コース議題、コース参加者 |
| 顧客情報     | 生年月日、性別、出身民族、配偶者の有無         | コース議題、コース参加者 |
| 雇用       | 開始日、終了日、移行日                        | コース議題、コース参加者 |
| ジョブ              | 職務、タイプ、役職                                        | コース議題、コース参加者 |
| 配置         | 職位、タイトル、およびフルタイム相当額 (FTE)                  | コース議題、コース参加者 |
| 従業員名    | 名、姓、フルネーム                             | コース出席者 |
| 従業員の肩書き   | 役職と勤続日数                                         | コース出席者 |

これらのエンティティは、データ モデルの計算メジャーを作成するために使用されました。 これらの計算メジャーは、主要業績評価指標 (KPI) およびコンテンツで使用するためのレポートを計算するために使用されます。 レポートおよびダッシュボードに追加の計算を含める場合は、LCS から .pbix ファイルをダウンロードして変更することができます。 このファイルはコンテンツを作成するために使用された既定のデータ モデルです。 変更後に、追加した情報を含む組織のコンテンツ パックとダッシュボードを作成できます。

