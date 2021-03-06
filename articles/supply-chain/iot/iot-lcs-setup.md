---
title: LCS で IoT インテリジェンスをインストールする
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストールする手順を説明します。
author: robinarh
ms.date: 07/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2d1cc9a7535be05a3e466c27e53047d694cf0160
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826446"
---
# <a name="install-the-iot-intelligence-add-in-in-lcs"></a>LCS で IoT インテリジェンスをインストールする

[!include [banner](../../includes/banner.md)]

このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストールする手順を説明します。 アドインはデモ/試用環境にはインストールできないことに注意してください。 アドインをインストールするには、事前に[Azure リソースを作成する ](iot-azure-setup.md)必要があります。

## <a name="set-up-the-lcs-environment"></a>LCS 環境の設定

1. LCS を開いて、Microsoft Dynamics 365 Supply Chain Management 環境に移動します。
2. **環境アドイン** セクションまでスクロールします。
3. **新規アドインをインストールする** を選択して、環境に対して有効になっているアドインの一覧を表示します。
4. **インストールするアドインの選択** ダイアログボックスで、**IoT インテリジェンス** を選択します。
5. **セットアップ アドイン** ダイアログ ボックスで、IoT ハブと Redis キャッシュの詳細を入力します。 必要となる値は、[Azureリソースの作成](iot-azure-setup.md) で作成した Key Vault で確認でき ます。

    + **テナント ID** – Azure ポータルで、Key Vault に移動し、左側のナビゲーションウィンドウで **概要** を選択して、**ディレクトリ ID** の値をコピーします。 コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。
    + **IoT イベントハブ - 互換エンドポイント Key Vault の URI** – Key Vault に移動し、続いて左側のナビゲーションウィンドウで **概要** を選択し、**DNS 名称** の値をコピーします。 コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。
    + **IoT イベント ハブ - 互換エンドポイントのシークレット名** – Key Vault に移動し、左側のナビゲーションウィンドウで **シークレット** を選択し、 IoT ハブが使用するイベント ハブの接続文字列が格納されているシークレット名をコピーします。 コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。
    + **Redis キャッシュ Key Vault の URI** – Key Vault に移動し、続いて左側のナビゲーションウィンドウで **概要** を選択し、**DNS 名称** の値をコピーします。 コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。
    + **Redis キャッシュ エンドポイントのシークレット名** – Key Vault に移動し、左側のナビゲーションウィンドウで **シークレット** を選択し、 Redis キャッシュが使用する接続文字列が格納されているシークレット名をコピーします。 コピーした値を **セットアップ アドイン** のダイアログ ボックスに貼り付けます。

6. 条件に同意するには、このチェック ボックスをオンにします。
7. **インストール** を選択します。
8. "アドインのインストールが正常に開始されました" というメッセージ ボックスが表示されます。 **OK** を選択します。

以上で、LCS の設定が完了しました。 次の手順では、[シナリオを設定](iot-scenario-setup.md)します。

## <a name="uninstall-the-add-in"></a><a id="uninstall-addin"></a>アドインのアンインストール

1. Supply Chain Management で [シナリオを無効にします](iot-scenario-setup.md#disable-a-scenario)。
2. LCS で、Supply Chain Management 環境の詳細に移動します。
3. **環境アドイン** セクションまでスクロールします。
4. IoT インテリジェンス アドインの **アンインストール** を選択します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]