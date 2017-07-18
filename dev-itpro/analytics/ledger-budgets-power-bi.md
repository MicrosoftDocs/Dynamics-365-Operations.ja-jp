---
title: "実績対予算 Power BI コンテンツ"
description: "このトピックでは、実績対予算 Power BI コンテンツについて説明します。 コンテンツに含まれているレポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。"
author: ryansandness
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 5d52cce3cccb16f0645d9de1832ebeffbfaf3a09
ms.contentlocale: ja-jp
ms.lasthandoff: 06/13/2017

---

# <a name="actual-vs-budget-power-bi-content"></a>実績対予算 Power BI コンテンツ

[!include[banner](../includes/banner.md)]


このトピックでは、[**実績対予算**] Microsoft Power BI コンテンツについて説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。 

# <a name="overview"></a>概要

[**実績対予算**] Power BI コンテンツは、組織内で実績対予算パフォーマンスの監視を担当する各個人に対して作成されました。 [**実績対予算**] Power BI コンテンツは、予算差異の可視性を提供します。 勘定カテゴリ、予算コード、主勘定、主勘定の説明、または差異の原因をより良く理解するための会計年度期間ごとに、今年度の予算を分析できます。 

# <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 7 月の更新プログラムを使用している場合、[**実績対予算**] Power BI コンテンツからのレポートは [**元帳予算および予測**] および [**CFO**] ワークスペースで表示されます。

# <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート
次の表は、[**実績対予算**] Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート                       | メトリックス |
|-----------------------------|---------|
| 経費 - 実績対予算 | <ul><li>今年度の経費合計</li><li>今年度の合計経費予算</li></ul> |
| 収益 - 実績対予算  | <ul><li>今年度の総収益</li><li>今年度の予算の総収益</li><ul> |
| 支出                     | <ul><li>今年度の経費合計</li><li>予算に基づく経費目標 </li><ul> |
| 収益                     | <ul><li>今年度の総収益</li><li>予算に基づく収益目標 </li><ul> |
| 純利益                  | <ul><li>今年度の純利益</li><li>予算に基づく目標純利益 </li><ul> |

## <a name="extending-the-power-bi-content"></a>Power BI コンテンツの拡張
Microsoft Dynamics Lifecycle Services (LCS) で利用できるコンテンツ パックを使用すると、Microsoft Dynamics 365 にログインしない人々に関する優れた分析ができます。 ほかのレポートまたはビジュアルを含めるよう、これらのコンテンツ パックを変更できます。次いで分析のためにコンテンツ パックを Power BI.com テナントに発行します。 

LCS の共有資産ライブラリに [**実績対予算**] Power BI コンテンツがあります。 コンテンツのダウンロード方法および組織で実装する方法の詳細については、「[Microsoft およびパートナーからの LCS での Power BI コンテンツ](power-bi-content-microsoft-partners.md)」を参照してください。 Power BI コンテンツの実装方法を示すデモを視聴するには、「[Microsoft の Power BI コンテンツおよび Dynamics Lifecycle Services のパートナー](https://mix.office.com/watch/9puyb1b2xs1w)」の Office Mix を参照してください。

# <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

| エンティティ                    | コンテンツ |
|---------------------------|----------|
| 総勘定元帳アクティビティ | 総勘定元帳のトランザクション金額 |
| 予算アクティビティ         | 予算登録のトランザクション金額 |
| 主勘定             | レポートをフィルター処理する主勘定 |
| 会計カレンダー          | レポートをフィルター処理する会計カレンダー |
| 元帳                   | 現在の元帳へのレポートをフィルター処理するために使用される元帳 |
| 予算コード              | レポートをフィルター処理する予算コード |
| 法人            | 現在の法人へのレポートをフィルター処理するために使用される法人 |

