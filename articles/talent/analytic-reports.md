---
title: Attract の分析レポートを使用
description: このトピックでは、Microsoft Dynamics 365 Talent - Attract でのプロセス インサイトの採用に関する分析レポートについて説明します
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: 081988e8b8cfe1e2ddb533247b678ba38a07f5f1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461787"
---
# <a name="use-analytic-reports-in-attract"></a>Attract の分析レポートを使用

[!include [banner](includes/banner.md)]

Microsoft Dynamics 365 Talent: Attract の分析レポートは、プロセス インサイトを採用するためにそのまま使用できる (OOTB) ソリューションを提供します。 利用可能な機能は次のとおりです。

- **職務分析 :** 職務申請者に関するメトリックスについては、職務内の **分析** タブをクリックします。
- **分析ハブ :** 職務間で集計されたメトリックスについては、左側のナビゲーションで **分析** をクリックしてください。
- **ユーザー固有のセキュリティ :** レポートへのアクセスは Attract [ロール](security-attract.md) および職務参加者ロールによって制御されます。
- **クロス フィルター処理 :** レポート内のビジュアルをクリックして、選択したデータによってフィルター処理された他のメトリックスを表示します。

>[!NOTE] 
>- この機能は現在[プレビュー](access-preview-feature.md)にあります。 これを実行するには、[**包括採用アドオン**](attract-comprehensive-hiring.md)が必要です。
>- すべてのパブリック プレビュー レポートは英語で表示されます。
>- レポートは 3 時間ごとに更新されます。 最新の更新時刻 (ローカル タイムゾーン) は、レポートの最上部に表示されます。 更新時刻は概算であり、地域のデータ量とリソースの負荷によって異なります。

## <a name="job-analytics"></a>職務分析

職務分析レポートは、職務の採用プロセスのスナップショットです。  主なメトリックスは次のとおりです。

- ステージごとの有効な申請者
- 申請者ソース
- 申請者のタイプ (内部と外部)

## <a name="analytics-hub"></a>分析ハブ

分析ハブは、採用プロセスにおける傾向を提示するために、職務間で集計されたデータをレポートします。 Attract には、パイプラインの概要とじょうご分析の 2 つの OOTB レポートが含まれます。

### <a name="pipeline-summary"></a>パイプラインの概要

パイプラインの概要レポートは、欠員がある職務のデータを集計します。 主なメトリックスは次のとおりです。

- ステージごとのすべての職務間の申請者
- 申請者ソース
- 勤続レベル別の欠員のある職務

### <a name="funnel-analysis"></a>じょうご分析

じょうご分析レポートでは、採用済みとして終了した職務のデータが集計されます。 主なメトリックスは次のとおりです。

- 採用する時期
- 変換メトリックス (ポイント時)
- 受入率の提示

注記 : 最も正確な時期にレポートを採用するためには、包括採用アドオンの一部として利用可能な機能である[オファー管理](offer-setup.md)を使用することをお勧めします。

>[!TIP] 
>ビジュアルの上にポインターを移動して、追加情報を確認してください。 たとえば、**有効な申請者** のビジュアルにポインターを移動すると、ステージの平均日数が表示されます。 この情報を分析することにより、採用にかかる時間を短縮し、採用担当者が各ステージで費やす時間を短縮する方法に関する重要な情報を得ることができます。

## <a name="user-specific-security"></a>ユーザー固有のセキュリティ

Attract レポートには、管理者、すべて読み取り、採用担当者、および採用マネージャー[各ロール](security-attract.md)がアクセスすることができます。 割り当てられていないユーザーは、どちらの分析レポートのページ (職務分析または分析ハブ) にもアクセスできません。

職務分析レポートには、選択した職務のデータが表示されます。 分析ハブ レポートでは、ユーザーが表示できるすべての職務のデータを集計します。 職務ページで自分の職務とすべての職務の両方を表示できるユーザーは、分析ハブでも同じビューを使用できます。

## <a name="cross-filter"></a>クロス フィルター

Power BI の優れた機能の 1 つは、レポート ページのすべてのビジュアルを連結できることです。 いずれかのビジュアルでデータ ポイントを選択すると、その選択に基づいて、そのデータを含むページ上の他のすべてのビジュアルが変更されます。 詳細については、[Power BI レポートでのビジュアルのクロス フィルター](https://docs.microsoft.com/power-bi/consumer/end-user-interactions)の例を参照してください。

## <a name="export-to-excel"></a>Excel にエクスポート

レポート データを Excel で表示するには、ビジュアル上のオプション メニュー (3 つのドット) をクリックし、**基になるデータのエクスポート** を選択します。 エクスポートされたデータは、Attract ユーザーのアクセス許可に従い、フィルタリングされ、エクスポートされます。 詳細については[視覚エフェクトからのデータのエクスポート](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data)を参照してください。
