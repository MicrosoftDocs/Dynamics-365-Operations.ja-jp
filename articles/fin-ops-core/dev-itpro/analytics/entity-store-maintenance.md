---
title: エンティティ ストアのメンテナンス後に問題を解決
description: この記事では、エンティティ ストアのメンテナンス後に完了する必要のある手順について説明します。
author: MilindaV2
ms.date: 04/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region:
- Global for most topics. Set Country/Region name for localizations
ms.author: milindav
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 70887a520fbc9b267fd1a3952e1099430a975cd7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897170"
---
# <a name="resolve-issues-after-entity-store-maintenance"></a>エンティティ ストアのメンテナンス後に問題を解決

[!include[banner](../includes/banner.md)]

エンティティ格納に対してメンテナンスが実行されるとき、それは次のコンポーネントに影響します。

- アプリケーション分析ワークスペース。
- PowerBI.com に配備されたエンティティ格納ベースのレポート。

これらのコンポーネントで問題を解決するには、この記事の手順を実行します。

> [!NOTE]
> アプリケーションの通常の動作には **影響しません**。

## <a name="if-you-are-using-application-analytical-workspaces"></a>アプリケーション分析ワークスペースを使用している場合

アプリケーション分析ワークスペースおよびレポートは、特定の保守操作が完了した後データを表示しない可能性があります。 次のスクリーン ショットはその例です。

![分析レポートは空白です。](media/blank-powerbi.png)

この問題を解決するには、次のようにします。

1. アプリケーションにログインします。
2. **システム管理** > **照会** > **バッチ ジョブ** の順に移動します。
3. **バッチ ジョブ** ページで、エンティティ格納に関連付けられているすべての保留中のバッチ ジョブを削除します。 これらのバッチ ジョブには次がふくまれます。

    - **待機中** の状態になります。
    - 通常は、**測定の配置**、**完全なリセット**、**差分更新** の説明があります。

    > [!NOTE]
    > 既定の説明は、以前のバージョンでは **測定の配置**、新しいバージョンでは **完全なリセット** です。 **Data Lake のトリクル更新** オプションを使用して Data Lake の統合を有効にすると、**差分更新** という説明のバッチ ジョブが作成されます。 説明がカスタマイズされている場合は、クラス名を参照して、バッチ ジョブがエンティティの店舗に関連付けられているかどうかを確認できます。 エンティティ格納に関連付けられているバッチ ジョブのクラス名は **BIMeasurementDeployManagementEntityBatchJob**、**BIMeasurementProcessorFull** または **BIMeasurementProcessorIncremental** になります。

4. **エンティティ格納** ページ (**システム管理 \> 設定 \> エンティティ格納**) に移動します。
5. 更新する必要があるすべての測定を選択します。
6. **更新** をクリックし、**OK** をクリックします。

リフレッシュが完了すると、アプリケーション分析ワークスペースおよびレポートはデータを表示します。

## <a name="if-you-have-deployed-entity-store-based-reports-to-powerbicom-and-are-using-the-reports-within-powerbicom"></a>エンティティ格納ベースのレポートを PowerBI.com に展開し、PowerBI.com 内のレポートを使用している場合

エンティティ格納 (前述) を更新した後、**システム管理** \> **設定** \> **Power BI ファイルを配置** を選択して、**Power BI レポート ファイルを配置** のページを使用してレポートを再配置します。

> [!NOTE]
> 以前に PowerBI.com に展開されたレポートは、エラーを発生させることがあります。 これが発生した場合、保守活動が終了したあとに、レポートと関連するデータセットを削除し再配置する必要がある場合があります。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
