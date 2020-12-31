---
title: エンティティ ストアのメンテナンス後に問題を解決
description: このトピックでは、エンティティ ストアのメンテナンス後に完了する必要のある手順について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region:
- Global for most topics. Set Country/Region name for localizations
ms.author: sarvanis
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 6dd95f2a73829e3703722673d6c0113cb916ddf7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687090"
---
# <a name="resolve-issues-after-entity-store-maintenance"></a>エンティティ ストアのメンテナンス後に問題を解決

[!include[banner](../includes/banner.md)]

エンティティ格納に対してメンテナンスが実行されるとき、それは次のコンポーネントに影響します。

- アプリケーション分析ワークスペース。
- PowerBI.com に配備されたエンティティ格納ベースのレポート。

これらのコンポーネントで問題を解決するには、このトピックの手順を実行します。

> [!NOTE]
> アプリケーションの通常の動作には **影響しません**。

## <a name="if-you-are-using-application-analytical-workspaces"></a>アプリケーション分析ワークスペースを使用している場合

アプリケーション分析ワークスペースおよびレポートは、特定の保守操作が完了した後データを表示しない可能性があります。 次のスクリーン ショットはその例です。

![分析レポートは空白](media/blank-powerbi.png)

この問題を解決するには、次のようにします。

1. アプリケーションにログインします。
2. **バッチ ジョブ** ページ (**システム管理 \> 照会 \> バッチ ジョブ**) に移動します。
3. エンティティ格納に関連付けられているすべての保留中のバッチ ジョブを削除します。 これらのバッチ ジョブには次がふくまれます。

    - **待機中** の状態になります。
    - 通常は **測定の配置** の説明があります。

    > [!NOTE]
    > 既定の説明は、**測定の配置** です。 説明がカスタマイズされている場合は、クラス名を参照して、バッチ ジョブがエンティティの店舗に関連付けられているかどうかを確認できます。 エンティティ格納に関連付けられているバッチ ジョブのクラス名は **BIMeasurementDeployManagementEntityBatchJob** になります。

4. **エンティティ格納** ページ (**システム管理 \> 設定 \> エンティティ格納**) に移動します。
5. 更新する必要があるすべての測定を選択します。
6. **更新** をクリックし、**OK** をクリックします。

リフレッシュが完了すると、アプリケーション分析ワークスペースおよびレポートはデータを表示します。

## <a name="if-you-have-deployed-entity-store-based-reports-to-powerbicom-and-are-using-the-reports-within-powerbicom"></a>エンティティ格納ベースのレポートを PowerBI.com に展開し、PowerBI.com 内のレポートを使用している場合

エンティティ格納 (前述) を更新した後、**システム管理** \> **設定** \> **Power BI ファイルを配置** を選択して、**Power BI レポート ファイルを配置** のページを使用してレポートを再配置します。

> [!NOTE]
> 以前に PowerBI.com に展開されたレポートは、エラーを発生させることがあります。 これが発生した場合、保守活動が終了したあとにレポートを削除し再配置する必要がある場合があります。
