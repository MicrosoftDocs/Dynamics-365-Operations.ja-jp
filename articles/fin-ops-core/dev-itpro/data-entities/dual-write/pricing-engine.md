---
title: Dynamics 365 Supply Chain Management の価格決定エンジンとのオンデマンド同期
description: このトピックでは、Dynamics 365 Sales からの Microsoft Dynamics 365 Supply Chain Management の価格決定エンジンを使用する方法について説明します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: ef4465144155130087b078f9f96911df38b62c41
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173180"
---
# <a name="sync-with-the-dynamics-365-supply-chain-management-pricing-engine-on-demand"></a>Dynamics 365 Supply Chain Management の価格決定エンジンとのオンデマンド同期

[!include [banner](../../includes/banner.md)]



Microsoft Dynamics 365 Supply Chain Managementには、売買契約、価格リスト、顧客ロイヤルティ プログラム、プロモーション、および割引を処理する価格決定エンジンが含まれています。 価格決定エンジンでは、複雑なルールを使用して、特定の見積または注文に対して最適な価格を決定します。 デュアル書き込みを使用する場合は、Dynamics 365 Sales の 見積書 と 注文 ページで、Dynamics 365 Supply Chain Management からの静的な価格決定または価格決定エンジンのいずれかを使用します。

## <a name="use-the-pricing-engine-from-supply-chain-management-in-sales"></a>Sales の Supply Chain Management からの価格決定エンジンを使用する

1. Sales で、**販売\>注文** に移動します。
2. 新規注文を作成するには **新規** を選択するか、**自分の注文** リストから既存の注文を選択します。
3. 新しい注文明細行を追加します。
4. 新しい注文を作成する場合は、アクション ウィンドウで **注文の価格** を選択します。 既存の注文を更新する場合は、アクション ウィンドウで **再計算** を選択します。

    以下のフィールドは、自動入力されます。

    + 詳細金額
    + 割引率
    + 割引
    + 送料を差し引いた金額
    + 送料
    + 税合計
    + 合計金額

## <a name="how-it-works"></a>この機能の動作

Sales で **注文の価格** を選択すると、Supply Chain Management の **販売注文 \> 表示** タブの **合計** 機能が、関連付けられている販売注文に対して呼び出されます。 Sales の注文合計の値は、Supply Chain Management の対応フィールドへの入力に使用されます。

Supply Chain Management で販売注文の合計が計算されるとき、顧客や販売注文に一覧表示されている製品の既存の売買契約と販売契約書がこの計算で評価されます。 この情報は、合計の計算に使用されます。 **注文の価格** が選択された場合、Supply Chain Management で行われたすべての設定が販売によって自動的に反映されます。

## <a name="limitations"></a>制限

Sales のフィールドが入力されている場合は、次の制限事項が適用されます。

+ Supply Chain Management での請求金額と請求金額配賦の設定は、Sales ではレプリケートされません。
+ 価格決定では、Supply Chain Management の販売注文行ページの **小売チャネル** フィールドで指定された特別な小売価格は考慮しません。
+ Supply Chain Management の **取引手当管理** セクションで定義されている割引は考慮されません。
