---
title: IoT インテリジェンスの Azure resources を設定する
description: このトピックでは、IoT インテリジェンスに必要となる Microsoft Azure リソースの作成と構成方法について説明します。
author: ''
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: ''
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ea1083a65efb25699b9237c72c081f50e1fb476c
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802776"
---
# <a name="set-up-azure-resources-for-iot-intelligence"></a>IoT インテリジェンスの Azure resources を設定する

[!include [banner](../../includes/banner.md)]

このトピックでは、IoT インテリジェンスに必要となる Microsoft Azure リソースの作成と構成方法について説明します。

## <a name="create-azure-resources"></a>Azure リソースの作成

次の手順に従って、Microsoft  Dynamics 365 Supply Chain Management からアクセスできる IoT hub、Redis キャッシュ、キーボルトを作成します。

### <a name="verify-that-the-microsoft-dynamics-erp-microservices-first-party-app-id-is-in-your-tenant"></a>Microsoft Dynamics ERP Microservices ファースト パーティ アプリの ID がテナントに含まれていることを確認する

Microsoft Dynamics ERP Microservices のファースト パーティ アプリのアプリ ID がテナントに含まれていることを確認するには、次の手順に従ってください。

1. <https://portal.azure.com>で Azure ポータルにログインします。
2. **Azure Active Directory** に移動します。
3. **エンタープライズ アプリケーション**に移動します。
4. **アプリケーション タイプ** フィールドで、**Microsoft アプリケーション** を選択します。
5. 検索フィールドで、**Microsoft Dynamics ERP Microservices** と入力します。
6. **Microsoft Dynamics ERP Microservices**が一覧に表示されていることを確認します。 その他のアプリケーションにも同様の名前があります。 そのため、適切なアプリを見つけるようにしてください。 アプリの ID は **0cdb527f-a8d1-4bf8-9436-b352c68682b2** です。

    アプリケーションが一覧に含まれていない場合は、テナントに追加する必要があります:

    1. Azure portal のツールバーで、ボタンを選択して Azure Cloud Shell を開きます。
    2. コマンド **Install-Module AzureAD** を実行します。 モジュールをインストールするには、**Y**と入力します。
    3. コマンド**Get-InstalledModule -Name "AzureAD"** を実行して、モジュールがインストールされていることを確認してください。
    4. コマンド **Connect-AzureAD -Confirm** を実行し、認証を行います。
    5. **New-AzureADServicePrincipal -AppId 0cdb527f-a8d1-4bf8-9436-b352c68682b2** を実行します。

    手順 1 ～ 6 を繰り返して、アプリの ID がご利用のテナントに含まれていることを確認できます。

### <a name="create-a-key-vault-resource"></a>Key Vault のリソースを作成する

Key Vault のリソースを作成するには、次の手順に従います。

1. Azure ポータルで、リソース グループに移動する、またはリソース グループを作成します。
2. **追加**を選択します。
3. **新しい**ページの [検索] フィールドに、**キーボルト** を入力します。 次に**作成** を選択します。
4. **Key Vault の作成** ページで、**Key Vault の名称** フィールドに名前を入力します。
5. 既定の値を確認し、**確認 + 作成** を選択します。
6. **作成**を選択します。

Key Vault がバックグラウンドで作成されます。

### <a name="create-an-iot-hub-resource"></a>IoT ハブ リソースの作成

IoT ハブのリソース ファイルを作成するには、次の手順に従います。

1. リソース グループに移動、またはリソース グループを作成する。
2. **追加**を選択します。
3. **新規**ページの [検索] フィールドに、**Iot ハブ** を入力します。 次に**作成** を選択します。
4. **IoT ハブの名称**フィールドに名前を入力します。
5. 既定の値を確認し、**確認 + 作成** を選択します。
6. **作成**を選択します。

IoT ハブ がバックグラウンドで作成されます。

> [!NOTE]
> 環境ごとに 1 つの IoT ハブ リソースを作成することを推奨します。

### <a name="create-a-redis-cache-resource"></a>Redis キャッシュ リソースの作成

Redis キャッシュ のリソースを作成するには、次の手順に従います。

1. リソース グループに移動、またはリソース グループを作成する。
2. **追加**を選択します。
3. **新規**ページの [検索] フィールドに、**Azure Cache for Redis** を入力します。 次に**作成** を選択します。
4. **DNS 名称**フィールドに、名前を入力します。
5. 既定の値を確認し、**作成** を選択します。

Redis キャッシュがバックグラウンドで作成されます。

> [!NOTE]
> 環境ごとに 1 つの Redis キャッシュを作成することを推奨します。

以上で、すべてのリソースが作成されました。

## <a name="configure-the-azure-resources"></a>Azure リソースの構成

### <a name="configure-the-iot-hub"></a>IoT ハブの構成

IoT ハブを構成するには、次の手順に従います。

1. ご利用のリソースで、IoT ハブのリソースを選択します。
2. 左側のナビゲーション ウィンドウで、**組み込み型エンドポイント** を選択します。
3. **コンシューマー グループ**で、次のコンシューマー グループを貼り付けます。 これらのコンシューマー グループは、既成のシナリオに対応しています。

    + microsoft.dynamics.iotintelligence-1
    + microsoft.dynamics.iotintelligence-2
    + microsoft.dynamics.iotintelligence-3

### <a name="configure-the-key-vault"></a>Key Vault の構成

Key Vault を構成するには、次の手順に従います。

1. ご利用のリソースで、Key Vault のリソースを選択します。
2. 左側のナビゲーション ウィンドウで、**アクセス ポリシー**を選択します。
3. **アクセス ポリシーの追加** を選択します。
4. **アクセス ポリシーの追加** ページの **シークレットの アクセス許可** フィールドで、**取得** と **一覧** を選択し ます。
5. **プリンシパルの選択**をクリックします。
6. **プリンシパル** ダイアログ ボックスで、**Microsoft Dynamics ERP Microservices** を検索して選択します。 **選択する** を選択します。
7. **追加**を選択します。
8. **保存** を選択します。

以上で、アプリが Key Vault のシークレットにアクセスできるようになります。

### <a name="save-the-iot-hub-connection-string-secret"></a>IoT ハブの接続文字列シークレットを保存します

IoT ハブの接続文字列のシークレットを保存するには、次の手順に従います。

1. ご利用のリソースで、IoT ハブのリソースを選択します。
2. 左側のナビゲーション ウィンドウで、**組み込み型エンドポイント** を選択します。
3. **イベントハブ互換エンドポイント** フィールドの値をコピー します。
4. Key Vault のリソースに移動します。
5. 左側のナビゲーション ウィンドウで、**シークレット**を選択します。
6. **生成/インポート** を選択します。
7. **名前**フィールドに、名前を入力します。
8. **値** フィールドに、前述の手順でコピーした エンドポイントの値を貼り付けます。
9. **作成**を選択します。

### <a name="save-the-redis-cache-connection-string-secret"></a>Redis キャッシュの接続文字列のシークレットを保存する

Redis キャッシュの接続文字列のシークレットを保存するには、次の手順に従います。

1. ご利用のリソースで、Redis キャッシュのリソースを選択します。
2. **アクセス キー**を選択します。
3. **ライマリ接続文字列** フィールドの値をコピーします。
4. Key Vault のリソースに移動します。
5. 左側のナビゲーション ウィンドウで、**シークレット**を選択します。
6. **生成/インポート** を選択します。
7. **名前**フィールドに、名前を入力します。
8. **値** フィールドに、前述の手順でコピーした接続文字列を貼り付けます。
9. **作成**を選択します。

> [!NOTE]
> いずれかの接続文字列を更新する場合は、常にこのシークレットの値も更新する必要があります。

以上で、必要な Azure リソースのプロビジョニングが完了しました。 次の手順では、[Microsoft Dynamics Lifecycle Services (LCS) に、IoT インテリジェンスをインストール](iot-lcs-setup.md) します。
