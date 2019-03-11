---
title: オンプレミス環境の再配置
description: このトピックでは、オンプレミス環境の再展開について説明します。
author: sarvanisathish
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: aa187dc35edb11428052df8c917458956f4d1db2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369976"
---
# <a name="redeploy-on-premises-environments"></a>オンプレミス環境の再配置

[!include [banner](../includes/banner.md)]

ある時点で、オンプレミス環境を再配置する必要があります。 これは、新しいプラットフォームの更新または実装の変更や問題がある場合に適用できます。 現在使用している環境を削除する前に、再配置する際に使用するコンフィギュレーション設定情報を保存する必要があります。 このトピックでは、構成設定を保存する方法と、環境を再配置する方法について説明します。 

## <a name="save-your-configuration"></a>コンフィギュレーションの保存
更新する予定の環境を削除する前に、次の手順に従って構成を保存してください。 
1. LCS で、**プロジェクト設定** > **オンプレミス コネクタ**に移動します。
2. 環境へのコネクタを選択し、**編集** をクリックします。
3. **コネクタの編集**タブで、**エージェントの構成** > **コンフィギュレーションの入力**の順に移動します。
4. **コンフィギュレーション設定**セクションのダウンロード Fileshare 場所の値をコピーします。 これは後で必要になります。
5. オンプレミス環境ファイル共有マシンにログインして、**\agent\wp<environment name>\StandaloneSetup\config.json** をコピーします。 この json ファイルで構成設定を使用すると、環境を再配置することができます。

### <a name="configuration-settings"></a>コンフィギュレーション設定
次のテーブルに、コンフィギュレーション設定に関する情報を示します。 前の手順で保存した .json ファイルの**構成設定**値を使用します。

**Active Directory フェデレーション サービス設定**


|                                                                  <strong>フィールド</strong>                                                                  |                          <strong>コンフィギュレーション設定</strong>                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
|                         最初の管理者になるユーザーの電子メール アドレス (たとえば、adminuser@yourdomain.com)                          |            components.(AOS).parameters.provisioning.adminPrincipleName.value             |
| Dynamics 365 アプリケーション グループの ADFS OpenID メタデータ エンドポイント。 (https://[federation-service-name]/adfs/.well-known/openid-configuration など) |              components.(AOS).parameters.activeDirectory.adfsMetadata.value              |
|                                               AOS アプリケーション グループの ADFS OpenID 接続クライアント ID                                                |              components.(AOS).parameters.activeDirectory.adfsClientId.value              |
|                                       Financial Reporting アプリケーション グループの ADFS OpenID 接続クライアント ID                                        | components.(FinancialReporting).parameters.aad.nativeClientAuthentication.clientId.value |

**SQL データベース コンフィギュレーション**

| **フィールド**                        | **コンフィギュレーション設定**                                                              |
|------------------------------|------------------------------------------------------------------------------------|
| SQL Server                   | components.(AOS).parameters.database.dbServer.value          |
| AX データベース                  | components.(AOS).parameters.database.dbName.value            |
| FINANCIAL REPORTING DATABASE | components.(FinancialReporting).parameters.mrdb.dbName.value |

**ファイル共有設定**

| **フィールド**                                                                                                                              | **コンフィギュレーション設定**                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Dynamics 365 インスタンスのファイル共有パス。 この共有は、ユーザーがアップロードしたファイルのドキュメント ストアとして使用されます。 | components.(AOS).parameters.storage.fileSharePath.value          |
| Microsoft Dynamics 365 インスタンスのファイル共有証明書の拇印。                                                      | components.(AOS).parameters.storage.sharedAccessThumbprint.value |

   > [!NOTE]
   > ファイル パス コンフィギュレーション値を .json ファイルから LCS UI にコピーするときは、余分な円記号をかならず削除してください。 たとえば、.json ファイルからのコンフィギュレーション値 **\\\\DC1\\D365FFOStorage** は LCS UI で **\\DC1\D365FFOStorage** である必要があります。

**SSRS コンフィギュレーション設定**

| **フィールド**                                                                      | **コンフィギュレーション設定**                                                                                      |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| SSRS インスタンスの IP アドレス。                                        | components.(AOS).parameters.biReporting.persistentVirtualMachineIPAddressSSRS.value  |
| SSRS アプリケーションが AX サービスと通信するために使用するサムプリント。 | components.(ReportingServices).parameters.reportingClientCertificateThumbprint.value |

**サービスの設定のコンフィギュレーション**

| **フィールド**                                                                                                                                      | **コンフィギュレーション設定**                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Dynamics 365 DNS 情報 - Microsoft Dynamics 365 インスタンスの DNS ホスト名 (ax.d365ffo.onprem.contoso.com など)。           | components.(AOS).parameters.infrastructure.hostName                                            |
| AOS SERVICE PRINCIPAL USER SETTINGS - yourdomain\axserviceuser など、AX サービスを実行するドメイン ユーザー アカウント。                         | components.(AOS).parameters.infrastructure.principalUserAccountName *                          |
| MR サービス プリンシパル ユーザー設定 - yourdomain\Svc-FRAS$ などの MR アプリケーション サービスを実行するためのグループ管理サービス アカウント (gMSA) です。 | components.(FinancialReporting).parameters.ApplicationServicePrincipalUser.accountName.value * |
| yourdomain\Svc-FRPS$ などの MR プロセス サービスを実行するためのグループ管理サービス アカウント (gMSA) です。                                          | components.(FinancialReporting).parameters.ProcessServicePrincipalUser.accountName.value *     |
| yourdomain\Svc-FRCO$ などのクリックワンス サービスを実行するためのグループ管理サービス アカウント (gMSA) です。                                       | components.(FinancialReporting).parameters.ClickOnceServicePrincipalUser.accountName.value *   |

> [!NOTE]
> LCS ユーザー インターフェイスで入力する前に、.json ファイルのプリンシパル ユーザー名構成値から余分な円記号を削除します。 たとえば、contoso\\AXServiceUser は LCS で contoso\AXServiceUser として入力される必要があります。

**アプリケーション証明書の設定**

| **フィールド**                                                                         | **コンフィギュレーション設定**                                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| データ暗号化証明書のサムプリント。                             | components.(AOS).parameters.database.dataEncryptionCertificateThumbprint.value              |
| データ署名証明書のサムプリント。                                | components.(AOS).parameters.database.dataSigningCertificateThumbprint.value                 |
| セッション認証証明書のサムプリント。                      | components.(FinancialReporting).parameters.sessionAuthenticationCertificateThumbprint.value |
| WCF / SOAP サポートに使用される SSL 証明書のサムプリント。               | components.(AOS).parameters.infrastructure.sslCertificateThumbprint.value                   |
| Management Reporter が AX サービスと通信するために使用するサムプリント。 | components.(FinancialReporting).parameters.tokenSpec.certThumbprint.value                   |



## <a name="redeploy-your-environment"></a>環境の再配置
次の手順では、環境を新しいプラットフォームまたはトポロジで更新または再配置する方法について説明します。
1. LCS で、オンプレミスのプロジェクトの**環境**ブレードに移動します。
2. 環境を削除するには、**削除**をクリックします。 

    > [!NOTE]
    > 環境を削除しても、データベース、インフラストラクチャ、またはローカル エージェントは削除されません。 Service Fabric アプリケーションのみ削除されます。

3. しばらく待ってから、配置が削除されたことを確認します。 展開が削除されたことを確認するには、オンプレミス環境にログインし、[Service Fabric Explorer] に移動します。

    次のアプリケーションを削除する必要があります。
   - AXBootstapperAppType
   - AXSFType
   - FinancialReportingType
   - RTGatewayAppType
   - ReportingService

     次のオンプレミス サービス ファブリック エージェント アプリケーションは削除しないでください。
   - LocalAgentType
   - MonitoringAgentAppType

4. 手順 3 でアプリケーションがすべて削除された後、LCS に戻り、**コンフィギュレーション**をクリックします。
5. プラットフォームの新しいトポロジを選択します。
6. 環境名を入力します。 同じ名前を使用したり、新しい名前を入力することができます。
7. **詳細設定**をクリックします。
   環境を構成するために保存した .json ファイルから、関連する構成を使用することができるようになりました。



