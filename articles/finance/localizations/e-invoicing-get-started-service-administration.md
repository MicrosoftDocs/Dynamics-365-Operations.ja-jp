---
title: 電子請求サービスの管理を開始する
description: このトピックでは、電子請求を開始する方法について説明します。
author: gionoder
ms.date: 08/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f77c8fd1696b74f852d04cc0a696d4816ef9af1f
ms.sourcegitcommit: 5033d42a2aac852916d726e40bd98a164d1a837d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/23/2022
ms.locfileid: "7984831"
---
# <a name="get-started-with-electronic-invoicing-service-administration"></a>電子請求サービスの管理を開始する

[!include [banner](../includes/banner.md)]

## <a name="prerequisites"></a>必要条件

このトピックの手順を完了する前に、以下の前提条件を満たす必要があります :

- Microsoft Dynamics Lifecycle Services (LCS) アカウントにアクセスできる必要があります。
- バージョン 10.0.17 以降の Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management を含む LCS プロジェクトが必要です。 さらに、これらのアプリケーションは、次のいずれかの Azure 地域にデプロイされている必要があります。

    - 米国
    - ヨーロッパ
    - 英国
    - アジア

- Dynamics 365 Regulatory Configuration Services (RCS) アカウントにアクセスする必要があります。
- 機能管理で RCS アカウントのグローバル化機能を有効にする必要があります。 詳細については、[Regulatory Configuration Services (RCS) - グローバリゼーション機能](rcs-globalization-feature.md)を参照してください。
- Azure のストレージ アカウントと Key Vault リソースを作成する必要があります。 詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。

## <a name="install-the-add-in-for-microservices-in-lifecycle-services"></a>Lifecycle Services にマイクロサービス向けのアドインをインストールします

1. LCS アカウントにサインインし、LCS プロジェクトのダッシュボードで、LCS プロジェクトを選択します。
2. プロジェクトの **環境** ダッシュボードで、配置された環境を選択します。 選択する環境は実行中である必要があります。
3. **Power Platform 統合** タブの **環境アドイン** フィールド グループで、**新しいアドインをインストールする** を選択します 。
4. **電子請求** を選択します。
5. **AAD アプリケーション ID** フィールドに、**091c98b0-a1c9-4b02-b62c-7753395ccabe** を入力します。 この値は固定値です。
6. **AAD のテナント ID** フィールドに、Azure のサブスクリプション アカウントのテナント ID を入力します。 指定する Azure Active Directory (Azure AD) テナントは、RCS に使用するテナントと同じである必要があります。
7. 条件を確認して、このチェック ボックスをオンにします。
8. **インストール** を選択します。 インストールには数分かかります。


## <a name="set-up-the-parameters-for-rcs-integration-with-electronic-invoicing"></a>電子請求と RCS 統合のパラメーターを設定する

1. RCS アカウントにサインインします。
2. **関連する設定** セクションの **グローバリゼーション** ワークスペースで、**電子申告パラメーター** を選択します。
3. **電子請求** タブの **サービス エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。

    | Azure geography データ センター | サービス エンドポイント URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 米国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ヨーロッパ                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 英国             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | アジア                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

4. **アプリケーション ID** フィールドが、**0cdb527f-a8d1-4bf8-9436-b352c68682b2** に設定されていることを確認します。 この値は固定値です。
5. **LCS 環境 ID** フィールドに、LCS 環境の ID を入力してください。
6. **保存** を選択し、ページを閉じます。

## <a name="create-key-vault-references"></a>Key Vault 参照を作成する

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。
3. **環境設定** ページのアクション ウィンドウで、**サービス環境** を選択してから **Key Vault パラメーター** を選択します。
4. **新規** を選択して、新しい Key Vault 参照を作成します。
5. **名前** フィールドに、key vault 参照の名前を入力します。 **説明** フィールドに説明を入力します。
6. **Key Vault URI** フィールドで、Azure Key Vault からの Key Vault シークレットをペーストします。 詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。
7. **保存** を選択します。

## <a name="create-storage-account-secret"></a>ストレージ アカウントのシークレットを作成する

1. **環境設定** ページの [アクション] ペインで、**サービス環境** > **Key Vault パラメーター** を選択します。
2. **Key Vault 参照** を選択し、**証明書** セクションで **追加** を選択します。
3. **名前** フィールドに、ストレージ アカウント シークレットの名前を入力します。 詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。
4. **説明** フィールドに説明を入力します。
5. **タイプ** フィールドで、**シークレット** を選択します。
6. **保存** を選択し、ページを閉じます。

## <a name="create-a-digital-certificate-secret"></a>デジタル証明書シークレットを作成する

1. **環境設定** ページのアクション ウィンドウで、**サービス環境** を選択してから **Key Vault パラメーター** を選択します。
2. **Key Vault 参照** を選択してから、**証明書** セクションで **追加** を選択します。
3. **名前** フィールドに、デジタル証明書シークレットの名前を入力します。 詳細については、[Azure ストレージ アカウント Key Vault リソースの作成](e-invoicing-create-azure-storage-account-key-vault.md) を参照してください。
4. **説明** フィールドに説明を入力します。
5. **タイプ** フィールドで、**証明書** を選択します。
6. **保存** を選択し、ページを閉じます。

## <a name="create-a-service-environment"></a>サービス環境の作成

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **環境t** セクションで、**電子請求** タイルを選択します。
3. **環境の設定** ページのアクション ウィンドウで、**サービス環境** を選択します。
4. **新規** を選択して、新しいサービス環境を作成します。
5. **名前** フィールドに、電子請求書環境の名前を入力します。 **説明** フィールドに説明を入力します。
6. **ストレージ SAS トークンのシークレット** フィールドで、ストレージ アカウントへのアクセス認証に使用する必要のあるストレージ アカウント シークレットの名前を選択します。
7. **ユーザー** セクションで、**追加** を選択し、環境を通じて電子請求書を送信し、記憶域アカウントに接続できるユーザーを追加します。
8. **ユーザーID** フィールドに、ユーザーのエイリアスを入力します。 **メール** フィールドに、ユーザーのメール アドレスを入力します。
9. **保存** を選択します。
10. 国や地域固有の請求書でデジタル署名を適用するにあたって一連の証明書が必要な場合は、アクション ウィンドウで **Key Vault パラメーター** を選択し、**証明書チェーン** を選択し、次の手順に従います。

    1. **新規** を選択して、一連の証明書を作成します。
    2. **名称** フィールドに、一連の証明書の名前を入力します。 **説明** フィールドに説明を入力します。
    3. **証明書** セクションで、**追加** を択してチェーンに証明書を追加します。
    4. **上** ボタン、または **下** ボタンを使用して、証明書チェーンの位置を変更します。
    5. **保存** を選択し、ページを閉じます。
    6. ページを閉じます。

11. **サービス環境** ページの、アクション ペインで、 **公開** を選択してクラウドに環境を公開します。 **状態** フィールドの値が **公開済** に変更されます。

## <a name="create-a-connected-application"></a>接続されたアプリケーションを作成する

1. **環境の設定** ページのアクション ウィンドウで、**接続されたアプリケーション** を選択します。
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

## <a name="set-up-electronic-invoicing-integration-in-finance-and-supply-chain-management"></a>Finance または Supply Chain Management に電子請求統合を設定する

### <a name="turn-on-the-electronic-invoicing-integration-feature"></a>電子請求統合機能をオンにする

1. Finance または Supply Chain Management インスタンスにサインインします。
2. **機能管理** ワークスペースで、**電子請求統合** 機能を検索します。 この機能がページに表示されない場合は、**更新を確認する** を選択します。
3. 機能を選択し、**直ちに有効化** を選択します。

### <a name="set-up-the-service-endpoint-url"></a>サービス エンドポイント URL を設定する

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **電子請求** タブの **エンドポイント URI** フィールドに、次の表に示すように、Azure の地域に対応するサービス エンドポイントを入力します。

    | Azure geography データ センター | サービス エンドポイント URI                                                       |
    |----------------------------|----------------------------------------------------------------------------|
    | 米国              | <p>`https://gw.us-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.us-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | ヨーロッパ                     | <p>`https://gw.eu-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il103.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il104.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il105.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il106.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il107.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il108.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il109.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.eu-il110.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | 英国             | <p>`https://gw.uk-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.uk-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |
    | アジア                       | <p>`https://gw.as-il101.gateway.prod.island.powerapps.com/electronicinvoicing/`</p><p>`https://gw.as-il102.gateway.prod.island.powerapps.com/electronicinvoicing/`</p> |

3. **環境** フィールドで、 電子請求に公開されたサービス環境の名前を入力します。
4. **保存** を選択し、ページを閉じます。

### <a name="enable-flighting-keys-for-finance-or-supply-chain-management-version-10017"></a>Finance または Supply Chain Management バージョン 10.0.17 のフライト キーを有効にする

1. 次の SQL コマンドを実行してください :

    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BusinessDocumentSubmissionServiceEnabled', 1)
    
    INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('ElectronicInvoicingServiceIntegrationFeature', 1)

2. すべての AOS に IISreset コマンドを実行します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
