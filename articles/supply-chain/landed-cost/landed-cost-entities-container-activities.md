---
title: コンテナー活動エンティティ
description: この記事では、出荷コンテナーの進捗状況を追跡するために使用されるコンテナー活動について説明します。
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 6a518003f8624ef05ac86be1b963c3f916420278
ms.sourcegitcommit: 5b34b41ae74269ba639e2876bc5862ef468da1cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2022
ms.locfileid: "9167576"
---
# <a name="container-activities-entity"></a>コンテナー活動エンティティ

[!include [banner](../includes/banner.md)]

コンテナー活動は、出荷コンテナーの進捗状況を追跡するために使用されます。 出荷コンテナーの作成時に選択された輸送テンプレートに割り当てられた各区画にレコードが作成されます。 レコードは、出荷コンテナーがデータ エンティティで作成された場合にも作成されます。

輸送中の出荷コンテナーの進捗状況に関する情報は、多くの場合、外部ソースから取得されます。 コンテナー活動エンティティでは、配送業者などの外部ソースがレコードを直接更新できます。 そのため、データを手動で更新する必要はありません。

## <a name="container-activities-itmcontaineractivityentity"></a>コンテナー活動 (ITMContainerActivityEntity)

コンテナ活動エンティティ (`ITMContainerActivityEntity`) を使用して、追加の活動レコードを作成できます。 または、配送業者は確認済みの **実際の終了日** の値に更新を渡すことができます。

| Name | マッピング | データ型 | キー | 必須 |
|---|---|---|---|---|
| 実際の終了日 | ITMContainerActivityTable.ActualEndDate | 日時 | 無効 | 無効 |
| 配送方法 | ITMContainerActivityTable.DlvModeId | Nvarchar(10) | 無効 | 無効 |
| 見積終了日 | ITMContainerActivityTable.EsimatedDate | 日時 | 無効 | 無効 |
| 行番号 | ITMContainerActivityTable.LineNum | Numeric(32, 16) | **有** | 無効 |
| 摘要 | ITMContainerActivityTable.Notes | nvarchar(MAX) | 無効 | 無効 |
| 活動 | ITMContainerActivityTable.ShipActivityId | Nvarchar(10) | 無効 | **有** |
| 出荷コンテナー | ITMContainerActivityTable.ShipContainerId | Nvarchar(20) | **有** | **有** |
| 航海 | ITMContainerActivityTable.ShipId | Nvarchar(20) | **有** | **有** |
| 区間 | ITMContainerActivityTable.ShipLegId | Nvarchar(20) | 無効 | **有** |
| サービス プロバイダー | ITMContainerActivityTable.ShipServiceProvider | Nvarchar(20) | 無効 | 無効 |
| 温度 | ITMContainerActivityTable.ShipTemperature | Numeric(32, 6) | 無効 | 無効 |
| 船舶 | ITMContainerActivityTable.ShipVesselId | Nvarchar(20) | 無効 | 無効 |
| 開始日 | ITMContainerActivityTable.StartDate | 日時 | 無効 | 無効 |

## <a name="tracking-control"></a>追跡管理

追跡管理センターを使用すると、指定したソース フィールドの更新が、指定されたターゲット フィールドの更新によってトリガーされます。 ソース フィールドの値とターゲット フィールドの値の両方がコンテナー活動エンティティを使用して更新された場合、ターゲット フィールドにはエンティティ値が表示されます。 この動作は、*リード タイム* の **作成タイプ** 値を持つ追跡管理レコードに関連しています。

**作成タイプ** の値が *状態更新* または *空白* (ユーザー定義の値) の原価領域では、システムが追跡管理の構成に従って航海状態またはターゲット フィールドを更新します。

## <a name="calculated-fields"></a>計算済フィールド

コンテナー活動レコードの次のフィールドの値は、他のフィールドの値に基づいて計算されます。 これらの計算フィールドはデータ エンティティには含まれませんが、計算の基になるフィールドが指定されている場合は設定されます。

- **見積日数** = **見積終了日** – **開始日**
- **実際の日数** = **実際の終了日** – **開始日**
