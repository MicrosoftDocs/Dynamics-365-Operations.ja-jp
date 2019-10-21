---
title: 与信および回収管理 Power BI コンテンツ
description: このトピックでは、与信および回収管理 Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用するデータ モデルおよびエンティティについての情報を提供します。
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustomerCollectionManagerWorkspace
audience: Application User, IT Pro
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5ac47ee086569cdaaa3c30f76435432e64f8fac6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189111"
---
# <a name="credit-and-collections-management-power-bi-content"></a>与信および回収管理 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

このトピックでは、**与信および回収管理** Microsoft Power BI コンテンツの内容について説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**与信および回収管理** Power BI コンテンツは、与信および回収マネージャー、そして回収係のために作成されています。 売掛債権回転日数、延滞残高、クレジット エクスポージャ、与信限度額を超えた顧客など、主要な与信および回収のメトリックスを提供します。 トランザクション データを使用し、すべての会社の与信および回収の集計ビューを提供します。 会社、顧客グループ、および顧客ごとの内訳も提供します。

この Power BI コンテンツは、10 のレポート ページで構成されます:

- 2 つの概要ページ (与信の概要に 1 ページと回収の概要に 1 ページ)
- さまざまな分析コードで解析された与信および回収のメトリックスの詳細を提供する 8 つの詳細ページ

すべての金額はシステム通貨で表示されます。 システム通貨は、**システム パラメーター** ページで設定できます。

既定では、現在の会社の与信および回収のデータが表示されます。 すべての会社のデータを表示するには、**CustCollectionsBICrossCompany** 職務権限をロールに割り当てます。

## <a name="setup-needed-to-view-power-bi-content"></a>Power BI コンテンツを表示するための設定

データを**顧客の与信および回収** Power BI ビジュアルに表示するには、次の設定を完了する必要があります。

1. **システム管理 > 設定 > システム パラメーター**に移動して、**システム通貨**および**システム為替レート**を設定します。
2. **総勘定元帳 > 設定 > 元帳**に移動して、**会計通貨**および**為替レート タイプ**を設定します。
3. トランザクション通貨と会計通貨、会計通貨とシステム通貨の間の為替レートを定義します。 これを行うには、**総勘定元帳 > 通貨 > 通貨の為替レート**に移動します。
4. **システム管理 > 設定 > エンティティ格納**に移動して、**CustCollectionsBIMeasurements** 集計測定を更新します。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス

**与信および回収管理** Power BI コンテンツは**顧客の与信および回収**ワークスペースに表示されます。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート

**CustCollectionsBICrossCompany** Power BI コンテンツには、一連のメトリックスで構成されるレポートが含まれています。 これらのメトリックスはグラフ、タイル、表として視覚化されます。 次の表に、**CustCollectionsBICrossCompany** Power BI コンテンツの視覚化の概要を示します。

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

これらすべてのレポートのグラフとタイルはフィルター処理し、ダッシュボードに固定することができます。 Power BI のフィルター処理と固定方法の詳細については、[ダッシュボードの作成および構成](https://powerbi.microsoft.com/guided-learning/powerbi-learning-4-2-create-configure-dashboards/) を参照してください。 また、基になるデータのエクスポート機能を使用して、視覚化で要約されている基になるデータをエクスポートすることができます。
