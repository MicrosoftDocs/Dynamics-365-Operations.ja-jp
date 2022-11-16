---
title: 計画ジョブのキャンセル
description: この記事では、計画の最適化機能を使用する有効な計画ジョブを取り消す方法について説明します。
author: t-benebo
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741179"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]