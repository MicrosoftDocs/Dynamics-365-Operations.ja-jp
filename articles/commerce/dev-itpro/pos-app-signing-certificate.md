---
title: コード署名証明書を使用して MPOS に署名する
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 9a90f1226c9932ea92c3bc21763f0b466ec1f4ee
ms.sourcegitcommit: 440b0a446f2c65135fde1be122ac714ba30ed71b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686225"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a>コード署名証明書を使用した MPOS appx の署名

[!include [banner](../includes/banner.md)]

Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからの署名証明書を使用して MPOS アプリに署名する必要があります。 証明書を使用して MPOS アプリに署名するために、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルにあるオプションのいずれかを使用します。

- Azure DevOps ビルド ステップのセキュア ファイル タスク部分を追加して、証明書をアップロードしてファイル タスクを保護します。 セキュア ファイル タスクの出力パス変数を Customization.settings ファイルのパラメーターとして使用します。

    > [!NOTE] 
    > セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。 このタスクをアップロードする前にパスワードを削除する必要があります。 証明書は、Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。 ただし、パスワードの削除についてはセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。 他のシナリオの証明書のパスワードは削除しないでください。
- ファイル システムにある証明書を使用してください。 これを行うには、証明書をダウンロードまたは生成し、ビルドが実行されているファイル システムに配置します。 Microsoft にホストされるエージェントまたはビルド ユーザーは、このパスとファイルへのアクセスが必要です。
- 拇印を使用してストア内の証明書を検索し、その証明書でサインインします。

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Universal Windows Platform アプリの署名にセキュリティで保護されたファイル タスクを使用する

セキュリティで保護されたファイル タスクの使用は、Universal Windows Platform (UWP) アプリの署名に推奨される方法です。 パッケージ署名の詳細については、[パッケージ署名の構成](https://docs.microsoft.com/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。 このプロセスを次の図に示します。

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

> [!NOTE] 
> 現在 OOB パッケージでは、appx ファイルの署名のみがサポートされており、MPOIS、RSSU、HWSなどのセルフ サービスの他のインストーラーは、このプロセスによって署名されません。 SignTool またはその他の署名ツールを使用して、手動で署名する必要があります。 appx ファイルの署名に使用する証明書は、Modern POS がインストールされているマシンにインストールする必要があります。

## <a name="steps-to-configure-the-certificate-for-signing"></a>署名のために証明書を構成する手順

### <a name="certificate-in-the-file-systemsecure-location"></a>ファイル システム / 安全な場所の証明書

[ダウンロードファイル タスク](https://docs.microsoft.com/visualstudio/msbuild/downloadfile-task?view=vs-2019)をダウンロードして、ビルド プロセスの最初の手順として追加します。 セキュリティで保護されたファイルのタスクを使用する利点は、ビルド パイプラインが成功したか、失敗したか、またはキャンセルされたかに関係なく、ビルド時にファイルが暗号化されてディスクに格納されることです。 このファイルは、ビルド プロセスの完了後にダウンロード場所から削除されます。

1. Azure DevOps ビルド パイプラインの最初のステップとして、セキュア ファイル タスクをダウンロードして追加します。 セキュア ファイル タスクは、[DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。
2. 次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。
    > [!div class="mx-imgBorder"]
    > ![セキュア ファイル タスク](media/SecureFile.png)
3. **変数**タブの下の**新しい変数**をクリックして、Azure DevOps パイプラインに新しい変数を作成します。
4. 値フィールド **$(MySigningCert.secureFilePath)** に、**CertFile** などの変数の名前を指定します。
5. 変数を保存します。
6. **RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateKeyFile** を Azure DevOps パイプラインで作成された変数で更新します (手順 3)。 例:
    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(CertFile)</ModernPOSPackageCertificateKeyFile>
    ```

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app"></a>MPOS アプリに署名するために証明書をダウンロードまたは生成する

ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。 例:

<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>

この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\ 参照**フォルダーに配置されます。

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>拇印を使用して MPOS アプリに署名する

拇印を使用して MPOS アプリに署名する場合は、証明書をローカルにインストールします。 **BuildTools\\Customization.settings** ファイルにある **ModernPOSPackageCertificateThumbprint** ノードで、拇印の値を更新します。

このオプションは、ビルド ユーザーがローカル ユーザーの場合に機能します。 ただし、Azure DevOps エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないので、ビルド マシンに証明書がインストールされない可能性があります。　 この場合、ビルド ユーザーをローカル ユーザーに変更し、そのボックスに証明書をインストールすることをお勧めします。 ただし、ボックスへの管理者アクセス権限がない場合は、このオプションは使用できません。

> [!NOTE]
> pfx file またはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint** ノードを空のままにします。 拇印オプションが使用されている場合、**ModernPOSPackageCertificateKeyFile** を空のままにします。 両方の値を更新すると、ビルドが失敗します。
