---
title: 実績対予算 Power BI コンテンツ
description: このトピックでは、実績対予算 Power BI コンテンツについて説明します。 レポートへのアクセス方法およびデータ モデルに関する情報を提供します。
author: panolte
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9cc52f4cdab3084c9ac43078b0b0d534119ab514
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744242"
---
# <a name="actual-vs-budget-power-bi-content"></a>実績対予算 Power BI コンテンツ

[!include [banner](../includes/banner.md)]

このトピックでは、**実績対予算** Microsoft Power BI コンテンツについて説明します。 Power BI レポートにアクセスする方法を説明し、コンテンツを作成するために使用したデータ モデルおよびエンティティについての情報を提供します。

## <a name="overview"></a>概要

**実績対予算** Power BI コンテンツは、組織内で実績対予算パフォーマンスの監視を担当する各個人に対して作成されました。 **実績対予算** Power BI コンテンツは、予算差異の可視性を提供します。 勘定カテゴリ、予算コード、主勘定、主勘定の説明、または差異の原因をより良く理解するための会計年度期間ごとに、今年度の予算を分析できます。

## <a name="accessing-the-power-bi-content"></a>Power BI コンテンツへのアクセス
**実績対予算** Power BI コンテンツからのレポートは、**元帳予算と予測**、および **CFO** ワークスペースで表示されます。

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Power BI コンテンツに含まれるレポート
次の表は、**実績対予算** Power BI コンテンツの各レポート ページに表示されるメトリックスの詳細について説明しています。

| レポート                       | メトリックス                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| 経費 - 実績対予算 | <ul><li>今年度の経費合計</li><li>今年度の合計経費予算</li></ul>  |
| 収益 - 実績対予算  | <ul><li>今年度の総収益</li><li>今年度の予算の総収益</li><ul>     |
| 支出                     | <ul><li>今年度の経費合計</li><li>予算に基づく経費目標</li><ul> |
| 収益                     | <ul><li>今年度の総収益</li><li>予算に基づく収益目標</li><ul>   |
| 純利益                  | <ul><li>今年度の純利益</li><li>予算に基づく目標純利益</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>データ モデルおよびエンティティの理解

| エンティティ                    | コンテンツ                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| 総勘定元帳アクティビティ | 総勘定元帳のトランザクション金額                                       |
| 予算アクティビティ         | 予算登録のトランザクション金額                                      |
| 主勘定             | レポートをフィルター処理する主勘定                                               |
| 会計カレンダー          | レポートをフィルター処理する会計カレンダー                                            |
| 元帳                   | 現在の元帳へのレポートをフィルター処理するために使用される元帳              |
| 予算コード              | レポートをフィルター処理する予算コード                                                |
| 法人            | 現在の法人へのレポートをフィルター処理するために使用される法人 |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]