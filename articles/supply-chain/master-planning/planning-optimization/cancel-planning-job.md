---
title: 計画ジョブのキャンセル
description: このトピックでは、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 7cee11e6d9e8bc2fe83f5369554ae9ff9ee2b741
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008219"
---
# <a name="cancel-a-planning-job"></a>計画ジョブのキャンセル

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。 計画最適化ジョブがユーザー インターフェイス (バックグラウンドではなく) から直接トリガーされた際、ダイアログ ボックスで **キャンセル** を選択すると、計画最適化ジョブはキャンセルされません。 「処理が取り消されました」などの警告が表示された場合でも、計画最適化で計画ジョブをキャンセルするには、次の手順を使用する必要があります。


有効な計画ジョブをキャンセルするには、次の手順を実行します。 

> [!NOTE]
> 有効なジョブのみキャンセルすることができます。

1. **マスタープラン \> 設定 \> 計画** に移動します。
2. 計画実行に適切な計画を選択します。
3. **履歴** を選択します。
4. キャンセルする計画ジョブの選択
5. **キャンセル** を選択します。

ジョブ状態は、計画の最適化サービスがジョブのキャンセルを確認するまで **キャンセル中** になります。 その後、状態は **キャンセル済** に変更されます。

> [!NOTE]
> 状態の変更を確認するには、**更新** ボタンを選択してページを更新する必要があります。

## <a name="additional-resources"></a>追加リソース

[計画最適化の概要](planning-optimization-overview.md)

[計画最適化の開始](get-started.md)

[計画の最適化フィット分析](planning-optimization-fit-analysis.md)

[計画の履歴と計画ログの表示](plan-history-logs.md)

[プランへのフィルターの適用](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]