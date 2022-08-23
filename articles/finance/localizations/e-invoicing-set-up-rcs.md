---
title: Regulatory Configuration Service (RCS) を設定する
description: この記事では、Regulatory Configuration Service (RCS) を設定する方法について説明します。
author: gionoder
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 63a4f77d6e80133947dff678cef3885167ec55be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285790"
---
# <a name="set-up-regulatory-configuration-service-rcs"></a>Regulatory Configuration Service (RCS) を設定する

[!include [banner](../includes/banner.md)]

この記事では、Regulatory Configuration Service (RCS) を設定する方法について説明します。

## <a name="turn-on-globalization-features"></a>グローバリゼーション機能を有効にする

1. RCS アカウントにサインインします。
2. **機能管理** タイルを選択します。
3. **機能の管理** ワークスペースで、一覧から **グローバリゼーション** 機能を選択し、**今すぐ有効にする** を選択します。

これで、**グローバリゼーション機能** ワークスペースのウィンドウがメインの RCS ダッシュボードに表示されます。

## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>電子請求と RCS 統合のパラメーターを設定する

1. **関連する設定** セクションの **グローバリゼーション** ワークスペースで、**電子申告パラメーター** を選択します。
2. **電子請求** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Microsoft Azure の地域に対応するサービス エンドポイントを入力します。

    | Azure geography データ センター | サービス エンドポイント URI |
    |----------------------------|----------------------|
    | 米国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ヨーロッパ                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | イギリス             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | アジア                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 日本                      | <p>`https://gw.jp-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | スイス                | <p>`https://gw.ch-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ブラジル                     | <p>`https://gw.br-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.br-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | アラブ首長国連邦       | <p>`https://gw.ae-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | オーストラリア                  | <p>`https://gw.au-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.au-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | カナダ                     | <p>`https://gw.ca-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> <p>`https://gw.ca-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | フランス                     | <p>`https://gw.fr-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | インド                      | <p>`https://gw.in-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. **アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。 この値は固定値です。 グローバル一意識別子 (GUID) のみを入力し、値にスペース、コンマ、期間、引用符などの他の記号が含まれるのを確認します。
4. **LCS 環境 ID** フィールドに、Microsoft Dynamics Lifecycle Services (LCS) 環境の ID を入力してください。 この値は、電子請求サービスで使用する財務または  Supply Chain Management 環境への参照です。 ID を取得するには、[LCS](https://lcs.dynamics.com/) にサインインして、自分のプロジェクトを開き、**環境の管理** タブの **環境の詳細** セクションで **環境ID** フィールドを参照します。

    > [!IMPORTANT]
    > LCS の複数の Finance または Supply Chain Management 環境に電子請求アドインがインストールされている場合は、常にインストールされた最新環境の環境 ID を使用します。 電子請求機能の設定と使用の後で新しい環境にアドインをインストールする場合は、RCSの **LCS 環境 ID** フィールドを最新の値に更新します。

5. **保存** を選択し、ページを閉じます。

## <a name="configuration-providers"></a>コンフィギュレーション提供者

構成プロバイダーを使用すると、電子請求プロセスで使用される電子レポート (ER) 構成の所有者と、所有者のグローバリゼーション機能を区別できます。 Microsoft が提供し、グローバル リポジトリで公開しているグローバリゼーション機能に対して、構成プロバイダーは **Microsoft** (`http://microsoft.com`) に設定されます。

有効な構成プロバイダーに属する ER 構成およびグローバリゼーション機能のみを調整できます。 これらの構成および機能をテンプレートとして使用して、有効な構成プロバイダーに属する構成および機能を作成して調整することができます。

まず、構成プロバイダーを作成します。 次に、その 1 つを有効として設定します。 **Microsoft** 構成プロバイダーを有効に設定できない。

### <a name="create-a-configuration-provider"></a>構成プロバイダーを作成する

1. **電子レポート** ワークスペースの、**関連するリンク** セクションで、**構成プロバイダー** を選択します。
2. **新規** を選択します。
3. **名前** フィールドに、構成プロバイダーの固有の名前を入力します。
4. **インターネット アドレス** フィールドに、構成プロバイダーの固有の URL を入力します。
5. **保存** を選択し、ページを閉じます。

### <a name="select-a-configuration-provider-as-active"></a>有効な構成プロバイダーを有効として選択します

1. 構成プロバイダーの一覧で、有効として設定する構成プロバイダーを選択します。
2. **有効に設定** を選択します。

## <a name="import-er-configurations-from-the-global-repository"></a>ER 構成をグローバル リポジトリからインポートする

1. **電子レポート** ワークスペースの、**関連するリンク** セクションで、**構成プロバイダー** を選択します。
2. 構成プロバイダーのリストで、**Microsoft** を選択して、**リポジトリ** を選択します。
3. **グローバル** を選択して、アクション ウィンドウで **開く** を選びます。
4. 次の ER モデルをインポートします。

    - **顧客請求書コンテクスト モデル**
    - **請求書モデル**
    - **会計ドキュメント** (必要に応じて、ブラジルのシナリオ)
    - **応答メッセージ モデル**

5. **請求書モデル マッピング** が自動的にインポートされていない場合は、それをインポートします。
6. ページを閉じます。
