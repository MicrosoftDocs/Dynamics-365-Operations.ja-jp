---
title: 電子請求書アドオンのサービス管理を使用する
description: このトピックでは、電子請求書アドオンの使用を開始する方法について解説します。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 111ec65aa826795125d4a9ce835f72e1a0f41b7b
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104403"
---
# <a name="get-started-with-electronic-invoicing-add-on-service-administration"></a>電子請求書アドオンのサービス管理を使用する

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="prerequisites"></a>必要条件

このトピックの手順を完了する前に、以下の前提条件を満たす必要があります :

- Microsoft Dynamics Lifecycle Services (LCS) アカウントにアクセスできる必要があります。
- バージョン 10.0.13 以降の Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management。 さらに、これらのアプリケーションは、次のいずれかの Azure 地域にデプロイされている必要があります。

    - 米国東部
    - 米国西部
    - 北ヨーロッパ
    - 西ヨーロッパ

- Dynamics 365 Regulatory Configuration Services (RCS) アカウントにアクセスする必要があります。
- 機能管理で RCS アカウントのグローバル化機能を有効にする必要があります。 詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。
- Azure のストレージ アカウントと Key Vault リソースを作成する必要があります。 詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。

## <a name="install-the-add-on-for-microservices-in-lifecycle-services"></a>Lifecycle Services のマイクロサービス用アドオンをインストールする

1. LCS アカウントにサインインします。
2. **プレビュー機能管理** タイルを選択します。
3. **パブリックプレビュー機能** セクションで、**電子請求書サービス** を選択します。
4. **プレビュー機能の有効化** オプションが **はい** に設定されていることを確認します。

## <a name="set-up-the-parameters-for-rcs-integration-with-the-electronic-invoicing-add-on"></a>電子請求書アドオンを使用した RCS 統合に使用するパラメーターを設定する

1. RCS アカウントにサインインします。
2. **関連リンク** セクションの **電子申告** ワークスペースで、**電子申告パラメーター** を選択します。
3. **電子請求書作成サービス** タブの **サービス エンドポイントURI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。

    | Azure geography データ センター | サービス エンドポイント URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 米国東部                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | 米国西部                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | 北ヨーロッパ                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | 西ヨーロッパ                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

4. **アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。 この値は固定値です。
5. **LCS 環境 ID** フィールドに、LCS のサブスクリプション アカウントの ID を入力します。
6. **保存** を選択し、ページを閉じます。

## <a name="create-key-vault-secret"></a>Key Vault シークレットの作成

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境** セクションで、**電子請求書** タイルを選択します。
3. **環境の設定**  ページのアクション ウィンドウで、**サービス環境** を選択し、**Key Vault パラメーター** を選択します。
4. **新規** を 選択すると、主要な key vault のシークレットを作成できます。
5. **名前** フィールドに、Key Vault のシークレットを入力します。 **説明** フィールドに説明を入力します。
6. **Key Vault URI** フィールドに、Azure Key Vault のからコピーしたシークレットを貼り付けます。
7. **保存** を選択します。

## <a name="create-storage-account-secret"></a>ストレージ アカウントのシークレットを作成する

1. **Key vault パラメーター** ページの **証明書** セクションで、**追加** を選択します。
2. **名前** フィールドに、Key Vault のシークレットを入力します。 **説明** フィールドに説明を入力します。
3. **タイプ** フィールドで、**証明書** を選択します。
4. **保存** を選択し、ページを閉じます。

## <a name="create-an-electronic-invoicing-add-on-environment"></a>電子請求書アドオン環境を作成する

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境** セクションで、**電子請求書** タイルを選択します。

## <a name="create-a-service-environment"></a>サービス環境の作成

1. **環境の設定** ページ のアクション ウィンドウで、**サービス環境** を選択します。
2. **新規** を選択して、新しいサービス環境を作成します。
3. **名前** フィールドに、電子請求書環境の名前を入力します。 **説明** フィールドに説明を入力します。
4. **Storage SAS トークンのシークレット**  フィールドで、記憶域アカウントへのアクセスの認証に使用する証明書の名前を選択します。
5. **ユーザー** セクションで、**追加** を選択し、環境を通じて電子請求書を送信し、記憶域アカウントに接続できるユーザーを追加します。
6. **ユーザーID** フィールドに、ユーザーのエイリアスを入力します。 **メール** フィールドに、ユーザーのメール アドレスを入力します。
7. **保存** を選択します。
8. 国や地域固有の請求書でデジタル署名を適用するにあたって一連の証明書が必要な場合は、アクション ウィンドウで **Key Vault パラメーター** を選択し、**証明書チェーン** を選択し、次の手順に従います。

    1. **新規** を選択して、一連の証明書を作成します。
    2. **名称** フィールドに、一連の証明書の名前を入力します。 **説明** フィールドに説明を入力します。
    3. **証明書** セクションで、**追加** を択してチェーンに証明書を追加します。
    4. **上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。
    5. **保存** を選択し、ページを閉じます。
    6. ページを閉じます。
9. **サービス環境** ページの、アクション ペインで、 **公開** を選択してクラウドに環境を公開します。 **状態** フィールドの値が **公開済** に変更されます。

## <a name="create-a-connected-application"></a>接続されたアプリケーションを作成する

1. **環境の設定** ページ のアクション ウィンドウで、**接続されたアプリケーション** を選択します。
2. **新規** を選択して、接続されたアプリケーションを作成します。
3. **名前** フィールドに、接続するアプリケーションの名前を入力します。
4. **アプリケーション** フィールドに、接続する Finance と Supply Chain Management 環境の URL を入力します。
4. **テナント** フィールドに、接続する Finance と Supply Chain Management 環境のテナントを入力します。
5. **保存** を選択します。
6. アクション ウィンドウで、**接続の確認** を 選択して環境との接続をテストします。 テスト後、ページを閉じます。

## <a name="link-connected-applications-to-environments"></a>接続されたアプリケーションと環境の関連付け

1. **環境の設定** ページで **新規** を選択し、接続されたアプリケーションを環境に割り当てます。
2. **接続されたアプリケーション**  フィールドで、接続されたアプリケーションを選択します。
3. **サービス環境** フィールドで、サービスの環境を選択します。
4. **保存** を選択し、ページを閉じます。

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance-and-supply-chain-management"></a>Finance および Supply Chain Management で電子請求書のアドオン統合を設定する

### <a name="turn-on-the-electronic-invoicing-add-on-integration-feature"></a>電子請求書アドオンの統合を有効化する

1. Finance または Supply Chain Management インスタンスにサインインします。
2. **機能の管理** ワークスペースで、 **電子請求書アドオンの統合** 機能を検索します。 この機能がページに表示されない場合は、**更新を確認する** を選択します。
3. 機能を選択し、**直ちに有効化** を選択します。

### <a name="set-up-the-service-endpoint-url"></a>サービス エンドポイント URL を設定する

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **送信サービス** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。

    | Azure geography データ センター | サービス エンドポイント URL                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 米国東部                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
    | 米国西部                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
    | 北ヨーロッパ                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
    | 西ヨーロッパ                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

3. **環境** フィールドに、電子請求書のアドオン環境の名前を入力します。
4. **保存** を選択し、ページを閉じます。
