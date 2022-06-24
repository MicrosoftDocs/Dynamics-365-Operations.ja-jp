---
title: Recruiting Power BI コンテンツ
description: この記事では、Recruiting Power BI コンテンツについて説明します。
author: jcart1106
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmRecruitmentWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 263934
ms.assetid: 38e6827b-0819-473c-bc47-821a1ec482b8
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d3240b92993986b32a739b7a6e5c7f7c2df3ed71
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890099"
---
# <a name="recruiting-power-bi-content"></a>Recruiting Power BI コンテンツ

[!include [banner](../includes/banner.md)]

この記事では、**Recruiting** Microsoft Power BI コンテンツについて説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
**Recruiting** Power BI コンテンツが **採用管理** ワークスペースで表示されます。

## <a name="reports-and-visuals-in-the-recruitment-management-workspace"></a>採用管理ワークスペースでのレポートおよびビジュアル
**採用管理** ワークスペースは、**分析** タブを含みます。このタブには、採用のための埋め込み Power BI コンテンツが含まれています。 このコンテンツには、[概要] タブと詳細が含まれる追加のタブがあります。 次の表に各タブのレポートを示します。

| レポート                | コンテンツ |
|----------------------|----------|
| 採用の概要 | 他のレポートの集計 |
| 申請者の分析   | 申請者の総数、ジョブ別申請者、申請者ソース、男性申請者に対する女性申請者、場所別申請者 |
| 申請者のステータス     | タイプおよびステータス別申請者および申請者のステータス |
| 採用分析  | 正味採用率、平均雇用日数、悪い雇用者の割合、採用にかかる費用、採用プロジェクト数、申請者に対する雇用者数、採用プロジェクトによる申請者数と空き状況 |

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解
これらのレポートのグラフとタイルをフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成およびコンフィギュレーション](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards) を参照してください。

次の表に、**Recruiting** Power BI コンテンツが基づいているエンティティを示します。

| エンティティ               | コンテンツ                                                         | 他のエンティティとの関係 |
|----------------------|------------------------------------------------------------------|-----------------------------------|
| 申請者            | 応募者、雇用申請者、正味雇用率、および費用          | 申請者名、会社、カレンダーのオフセット、日付、地理的な場所、人口統計、ジョブ、メディア、採用プロジェクト |
| 申請者名       | 申請者の名、姓、フルネーム                   | 申請者、採用済申請者、退職済申請者 |
| カレンダーのオフセット      | レポートをスライスするカレンダーのオフセット                                | 申請者、採用済申請者、退職済申請者 |
| 法人              | レポートをフィルター処理する会社                                   | 申請者、採用済申請者、退職済申請者 |
| 日                 | 日、週、月、年                                   | 申請者、採用済申請者、退職済申請者 |
| 顧客情報         | 生年月日、性別、出身民族、配偶者の有無         | 申請者、採用済申請者、退職済申請者 |
| 採用済申請者   | 申請者、パフォーマンス、開始日、および申請者のタイプ           | 会社、カレンダーのオフセット、日付、地理的な場所、申請者名、雇用、パフォーマンス、ジョブ、メディア、採用プロジェクト |
| 雇用           | 開始日、終了日、移行日                        | 申請者、採用済申請者、退職済申請者 |
| 地理的な場所  | 市町村、市区郡、郵便番号、都道府県                 | 申請者、採用済申請者、退職済申請者 |
| ジョブ                  | 職務、タイプ、役職                                        | 申請者、採用済申請者、退職済申請者 |
| メディア                | 申請者のソース                                             | 申請者、採用済申請者、退職済申請者 |
| パフォーマンス          | 評価、説明、評価モデル                            | 申請者、採用済申請者、退職済申請者 |
| 採用プロジェクト  | プロジェクト説明、プロジェクト ステータス、空き状況                | 申請者、採用済申請者、退職済申請者 |
| 退職済申請者 | 退職済申請者、理由、パフォーマンス、終了日 | 会社、カレンダーのオフセット、日付、地理的な場所、パフォーマンス、人口統計、雇用、メディア、採用プロジェクト、申請者名 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]