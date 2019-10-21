---
title: コード署名証明書を使用して MPOS に署名する
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/26/2019
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
ms.openlocfilehash: efb1ba4d890cbf02296994179efd8198a306505f
ms.sourcegitcommit: 2555acfd855fc18ff3ba432ba2cf7633a8f1653c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2019
ms.locfileid: "2238561"
---
# <a name="sign-mpos-with-a-code-signing-certificate"></a>コード署名証明書を使用して MPOS に署名する

[!include [banner](../includes/banner.md)]

Windows に Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからの署名証明書を使用して MPOS アプリに署名する必要があります。 証明書を使用して MPOS アプリに署名するためのオプションが以下の場所にいくつかあります **Retail SDK\\ビルド ツール\\Customization.settings** ファイル:

- Azure DevOps ビルド ステップのセキュリティで保護されたファイル タスク部分を追加し、証明書をアップロードしてファイル タスクをセキュリティ保護し、セキュリティで保護されたファイル タスクの出力パス変数を Customization.settings ファイルのパラメータとして使用します。
    > [!NOTE] 
    > セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。 このタスクにアップロードする前にパスワードを削除する必要があります。 証明書は、Microsoft Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。 パスワードの削除についてセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。 ビルド タスクにアップロードされた証明書は、ビルド フロー中にビルド パイプラインによってのみアクセスできます。他のプロセスがアクセスすることはできません。 セキュリティで保護されたファイル タスクを使用すると、ビルド署名プロセス中にパスワード セキュリティの追加レイヤーは必要ありません。 他のシナリオの証明書のパスワードは削除しないでください。
- ファイル システムに配置された証明書を使用します。証明書をダウンロードまたは生成し、ビルドを実行しているファイル システムに配置します。 VSO エージェントまたはビルド ユーザーは、このパスとファイルにアクセスできる必要があります。
- 拇印を使用してストア内の証明書を検索し、その証明書で署名します。

## <a name="using-a-secure-file-task-is-the-recommended-approach-for-uwp-app-signing"></a>セキュリティで保護されたファイル タスクの使用は、UWP アプリの署名に推奨される方法です。

パッケージ署名については、[パッケージ署名の構成](https://docs.microsoft.com/en-us/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。 プロセスを次の図に示します。

![MPOS アプリ署名フロー](media/POSSigningFlow.png)

## <a name="steps-to-configure-the-certificate-for-signing"></a>署名のために証明書を構成する手順

### <a name="certificate-in-the-file-systemsecure-location"></a>ファイル システム / 安全な場所の証明書:

[ファイル タスクをダウンロード](https://docs.microsoft.com/en-us/visualstudio/msbuild/downloadfile-task?view=vs-2019)して、ビルド プロセスの最初の手順として追加します。 セキュア ファイル タスクを使用する利点は、ビルド中にファイルが暗号化されてディスクに配置されることであり、ビルド パイプラインが成功、失敗、またはキャンセルされたかどうかに関係なく、ファイルはビルド プロセスの完了後にダウンロード場所から削除されます。

1. Azure DevOps ビルド パイプラインの最初のステップとして、セキュア ファイル タスクをダウンロードして追加します。 セキュア ファイル タスクは、 [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。
2. 次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。
    > [!div class="mx-imgBorder"]
    > ![セキュア ファイル タスク](media/SecureFile.png)
3. **変数**タブの下の**新しい変数**ボタンをクリックして、Azure DevOps に新しい変数を作成します。
4. 値フィールド **$(MySigningCert.secureFilePath)** に、**CertFile** などの変数の名前を指定します。
5. 変数を保存します。
6. **RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateKeyFile** を Azure DevOps パイプラインで作成された変数で更新します (手順 3)。 例:
    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(CertFile</ModernPOSPackageCertificateKeyFile>
    ```

## <a name="downloaded-or-generated-certificate-to-sign-the-mpos-app"></a>MPOS アプリに署名するためにダウンロードまたは生成された証明書

ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。 例:

<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>

この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\参照**フォルダーに配置されます。

## <a name="thumbprint-to-sign-the-mpos-app"></a>MPOS アプリに署名するための拇印

拇印を使用して MPOS アプリに署名する場合、証明書をローカルにインストールし、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint** ノードの拇印の値を更新します。

ビルド ユーザーがローカル ユーザーの場合、このオプションは正常に機能しますが、Azure DevOps/VSO エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないか、ビルド マシンに証明書がインストールされない可能性があります。 この場合の回避策は、ビルド ユーザーをローカル ユーザーに変更し、このボックスに証明書をインストールすることですが、このボックスに管理者としてアクセスする権限がない場合は、このオプションは正しく機能しません。

> [!NOTE]
> .pfx ファイルまたはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** ファイルの **ModernPOSPackageCertificateThumbprint** ノードを空のままにし、拇印オプションを使用する場合は **ModernPOSPackageCertificateKeyFile** を空にします。 両方の値を更新すると、ビルドが失敗します。
