---
title: IoT インテリジェンスの監視と管理
description: この記事では、IoT インテリジェンスを監視、管理する方法について説明します。
author: johanhoffmann
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a640b523adac619377e19d670f932d4d85cfb6a9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852421"
---
# <a name="monitor-and-manage-iot-intelligence"></a>IoT インテリジェンスの監視と管理

[!include [banner](../../includes/banner.md)]

この記事では、IoT インテリジェンスを監視、管理する方法について説明します。

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a>Microsoft Dynamics 365 Supply Chain Management のシナリオを監視する

IoT インテリジェンスが行う処理は、複数の場所から監視できます:

+ **モジュール \> 生産管理 \> 照会とレポート \> IoT インテリジェンス \> 通知** – 未解決の通知の一覧を表示します。
+ **モジュール \> 生産管理 \> 照会とレポート \> IoT インテリジェンス \> 確認済みの通知** – 対応済み、または無視した通知の一覧を表示します。
+ **モジュール \> 生産管理 \> 照会とレポート \> IoTインテリジェンス \>メトリック キー** – **リソース ステータス** の時系列グラフのメトリック キーを表示し ます。
+ **モジュール \> 生産管理 \> 製造の実行 \> リソース ステータス** – **構成** ダイアログ ボックスを使用して特定のメトリックを追跡します。 シナリオで例外が検出された場合は、例外の詳細が通知されます。
+ **ワークスペース \> 生産現場管理 \> 通知** – 未解決の通知の一覧を表示します。

## <a name="modify-a-running-iot-intelligence-scenario"></a>実行中の IoT インテリジェンス シナリオの変更

シナリオが実行されている場合は、以下の変更を行うことができます:

+ 新たなセンサー スキーマの定義を追加する。
+ 新たなシグナル データ値を選択する。
+ 既存のシグナル データ値の選択をキャンセルする。
+ 新たなシグナル データ値を追加・マッピングする。
+ しきい値を更新する。

シナリオが実行されている場合は、以下の変更はできません:

+ 有効なシナリオが現在消費しているスキーマ定義の削除・変更。
+ 有効なシナリオの選択したスキーマのパスを変更する。

## <a name="simulation-options"></a>シミュレーション オプション

工場のマシンの信号をシミュレートすることができます。 詳細については、以下の記事を参照してください。

+ [IoT DevKit AZ3166 を Azure IoT ハブに接続する](/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [Raspberry Pi online シミュレーターを Azure IoT ハブ (node.js) に接続する](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
