---
title: テスト用にシミュレーションされたセンサーを設定する
description: この記事では、物理的なセンサーを設置せずに Sensor Data Intelligence をテストするために使用できるシミュレーターを設定する方法を説明します。
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f12d6e1d417a260477b1eb4e027b850d1862f51f
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689807"
---
# <a name="set-up-a-simulated-sensor-for-testing"></a>テスト用にシミュレーションされたセンサーを設定する

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

物理的なセンサーをインストールせずに、Sensor Data Intelligence をテストする場合、*Raspberry PI Azure IoT Online Simulator* サービスを使用してセンサー信号をエミュレートし、Microsoft Azure のモノのインターネット (IoT) ソリューションに送信することができます。 シミュレーターの詳細については、[Raspberry Pi online シミュレーターを Azure IoT ハブ (node.js) に接続する](/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)を参照してください。

## <a name="video-instructions"></a>ビデオの指示

次のビデオでは、テスト用のシミュレーション センサーを設定する方法を説明します。 この記事の残りのセクションでは、テキスト ベースの形式で同じ手順を示します。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE588g6]

## <a name="create-a-device-in-azure-iot-hub"></a>Azure IoT でデバイスを作成する

最初にデバイスを設定して、Azure IoT Hub に対する信号を認証する必要があります。

1. Azure で、Sensor Data Intelligence と併用するために作成したそのリソース グループのリソース リストに移動します。 (詳細については、[ IoT ソリューションを Azure に配置する](sdi-deploy-iot-solution-on-azure.md)を参照してください。)
1. リソース の一覧で、**タイプ** フィールドが *IoT Hub* に設定されているレコードを検索します。 **名前** 列で、名前を選択して、リリースの詳細ページを開きます。
1. 左側のナビゲーション ウィンドウで、**デバイス** を選択します。
1. **デバイス** ページで、**デバイスの追加** を選択します。
1. **デバイスの作成** ページで、次のフィールドを設定します :

    - **デバイス ID** - 新しいデバイスの名前 (*My-IoT-Device* など) を入力します。
    - **認証タイプ** - *キーの選択* を選択します。
    - **キーの自動生成** - このチェック ボックスをオンにします。
    - **このデバイスを IoT ファイルに接続する** - *有効* を選択します。

1. **保存** を選択して **デバイス** ページに戻ります。
1. 新しいデバイスをリストから検索します。 **デバイス ID** 列で、名前を選択して、デバイスの詳細ページを開きます。 新しいデバイスがリストに表示される場合は、ページを更新します。
1. **プライマリ接続文字列** 値をコピーします (**クリップボードにコピー** ボタンを選択する場合など)。 この値は、Raspberry Pi IoT シミュレーターを設定してセンサー信号をエミュレートする際に必要となります。 したがって、このファイルをテキスト ファイルに貼り付けることを検討してください。

## <a name="add-the-azure-connection-string-to-the-raspberry-pi-iot-simulator"></a>Azure 接続文字列を Raspberry Pi IoT シミュレーターに追加します

次の手順に従って、Azure IoT 内のデバイスの接続文字列を、Raspberry サービスのスクリプトに追加します。

1. [Raspberry Pi IoT シミュレーター](https://azure-samples.github.io/raspberry-pi-web-simulator/)を開きます。
1. コード エディタ ウィンドウで、次のコマンドを含む行を検索します。

    `const connectionString = '[Your IoT hub device connection string]';`

1. かっこを含むヘルプ テキストを、前のセクションでコピーした **プライマリー接続文字列** の値と置き換えます。 結果は次の例のようになります。

    `const connectionString = 'HostName=XXX;DeviceId=YYY;SharedAccessKey=ZZZ';`

## <a name="add-sensor-ids-and-values-to-the-payload-in-the-raspberry-pi-iot-simulator"></a>センサー ID と値を Raspberry Pi IoT シミュレーターのペイロードに追加する

次に、Raspberry Pi IoT シミュレーターを、シミュレーションされたセンサーとペイロードとして送信する値を使って設定する必要があります。

- Raspberry Pi IoT シミュレーターのコードエディターで、`getMessage` 関数を見つけて、次のコードと一致するように編集します。 (センサーは `cb()` 行で設定 されます。)

    ```cpp
    function getMessage(cb) {
        messageId++;
        sensor.readSensorData()
        .then(function (data) {
            cb(JSON.stringify({ value: 1, sensorId: 'MachineStatus' }), false);
            cb(JSON.stringify({ value: 70, sensorId: 'Quality' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'AssetMaintenance' }), false);
            cb(JSON.stringify({ value: 1, sensorId: 'ProductionDelay' }), false);
            cb(JSON.stringify({ value: 20, sensorId: 'AssetDowntime' }), false);
        })
        .catch(function (err) {
            console.error('Failed to read out sensor data: ' + err);
        });
    }
    ```

    > [!IMPORTANT]
    > Raspberry Pi IoT シミュレーターのコード エディターで定義するセンサー ID は、後で Supply Chain Management のシナリオに指定するセンサー ID と同一である必要があります。 前の例コードでは、読み取り可能なセンサー ID を使用します。 ただし実際のシナリオでは、センサー ID はセンサー製造元から提供される グローバル一意識別子 (GUID) 値となります。 このコードの例で使用されるユーザーが読み取り可能な接続図の ID は、[製品の品質シナリオ](sdi-scenario-product-quality.md)、[資産メンテナンス シナリオ](sdi-scenario-asset-maintenance.md)、[生産の遅延のシナリオ](sdi-scenario-production-delays.md)、および[マシン状態のシナリオ](sdi-scenario-equipment-downtime.md) の例でも使用されています。 したがって、これらのシナリオを実行する場合は、このコードを使用します。

## <a name="edit-the-interval-for-sending-sensor-signals"></a>センサー信号を送信する間隔を編集します

ここで、Raspberry Pi IoT シミュレーターがエミュレートしたセンサー信号を送信する間隔を設定する必要があります。

1. Raspberry Pi IoT シミュレーターのコード エディターで、次の関数の呼び出しを見つけます。

    `setInterval(sendMessage, 2000);`

2. 既定では、Raspberry Pi IoT シミュレーターでは、2,000 ミリ秒 (2 秒) ごとにセンサー信号が送信されます。 必要に応じて値を調整することができます。

## <a name="run-the-raspberry-pi-iot-simulator"></a>Raspberry Pi IoT シミュレーターを実行します

- **実行** を選択してシミュレーターを開始し、シミュレーションされたセンサー データの送信を開始します。
