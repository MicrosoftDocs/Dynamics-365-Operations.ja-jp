---
title: IoT インテリジェンスの指標の設定
description: このトピックでは、IoT インテリジェンスの指標を設定する方法について説明します。
author: robinarh
ms.date: 04/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-25
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9ddc9f47d17782ef77f5c9c05253835a5b79748ac836f8b5bd33c2328cea427
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736807"
---
# <a name="set-up-metrics-for-iot-intelligence"></a>IoT インテリジェンスの指標の設定

[!include [banner](../../includes/banner.md)]

## <a name="configure-metrics"></a>指標のコンフィギュレーション

Microsoft Dynamics 365 Supply Chain Management でメッセージのタイム シリーズ チャートを表示する場合は、次の手順に従って指標を設定する必要があります。

1. Redis キャッシュの接続文字列をコピーします:

    1. Azure portal で、Redis キャッシュに移動します。
    2. **設定** \> **アクセス キー** に移動します。
    3. **ライマリ接続文字列** フィールドの値をコピーします。

2. Supply Chain Management では、**生産管理 \> 設定 \> IoT インテリジェンス \> シナリオ パラメータ** に移動します。
3. **シナリオ パラメータ** ページの **タイム シリーズ** タブの **Redis メトリック ストア接続文字列** フィールドに、前の手順でコピーした接続文字列を貼り付けます。 この手順により、Azure IoT Hub からの指標を Supply Chain Management で視覚化できます。 フィールドに値を貼り付けると、**\*\*\*\*\*\*** と表示されます。

    > [!NOTE]
    > Redis キャッシュ接続文字列を更新する場合はいつでも、このフィールドも更新する必要があります。

4. **生産管理 \> 照会とレポート \> IoT インテリジェンス \> 指標キー** に移動します。
5. **指標キー** ページで、**更新** を選択します。
6. **指標キーの更新** ダイアログ ボックスで、フィールドで **バックグラウンドで実行** が選択されていることに注意してください。 **OK** を選択します。

Redis キャッシュ内のすべての指標キーが取得され、**指標キー** 一覧に追加されます。 指標値は、[シナリオを有効にする](iot-scenario-setup.md) まで表示されません。

## <a name="configure-the-resource-status-time-series"></a>リソース ステータス タイム シリーズのコンフィギュレーション

**リソース ステータス** タイム シリーズをコンフィギュレーションするには、次の手順を実行します。

1. Supply Chain Management で、**生産管理 \> 製造実行 \> リソース ステータス** に移動します。
2. **リソース ステータス** ページで、**コンフィギュレーション** を選択します。
2. **コンフィギュレーション** ダイアログ ボックスの **リソース** 一覧で、監視する項目を選択します。
3. **タイム シリーズ 1** の **編集** ボタンを選択します。
4. **タイム シリーズの選択** ダイアログ ボックスで、グリッドの指標を選択します。 (**指標キーの更新** リンクを使用して、このダイアログ ボックスから指標キーを更新します。)
5. **OK** を選択し て、**コンフィギュレーション** ダイアログ ボックスに戻ります。
6. 表示名を入力します。
7. **データの表示元** フィールドで、タイム フレームを選択します。
8. **OK** を選択します。

グラフが表示されます。

## <a name="delete-a-metric-key"></a>指標キーの削除

1. Supply Chain Management で、**生産管理 \> 照会とレポート \> IoT インテリジェンス \> 指標キー** に移動します。
2. **指標キー** ページで、削除する指標キーを選択します。
3. **削除** を選択します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]