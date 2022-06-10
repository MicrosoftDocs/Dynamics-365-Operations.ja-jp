---
title: コード署名証明書を使用した MPOS .appx ファイルの署名
description: このトピックでは、コード署名証明書を使用して MPOS に署名する方法について説明します。
author: mugunthanm
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: 38c094de6f94381a809fdb68d2e76d410e406934
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811088"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>コード署名証明書を使用した MPOS .appx ファイルの署名

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Modern POS (MPOS) をインストールするには、信頼されたプロバイダーからのコード署名証明書を使用して MPOS アプリに署名し、現在のユーザーの信頼されたルート フォルダーの下に MPOS がインストールされているすべてのコンピューターに同じ証明書をインストールする必要があります。

証明書を使用して MPOS アプリに署名するために、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルにあるオプションのいずれかを使用します。

- Azure DevOps ビルド ステップのセキュア ファイル タスク部分を追加して、証明書をアップロードしてファイル タスクを保護します。 セキュア ファイル タスクの出力パス変数を Customization.settings ファイルのパラメーターとして使用します。

    > [!NOTE]
    > セキュリティで保護されたファイル タスクは、パスワードで保護された証明書をサポートしていません。 このタスクをアップロードする前にパスワードを削除する必要があります。 証明書は、Azure のセキュリティで保護されたファイル システム タスクにアップロードされるため、このステップのパスワードのみを削除することができます。 ただし、パスワードの削除についてはセキュリティの専門家と話し合って、これがプロジェクトにとって正しいアクションであるかどうかを判断する必要があります。 他のシナリオの証明書のパスワードは削除しないでください。
- ファイル システムにある証明書を使用してください。 これを行うには、証明書をダウンロードまたは生成し、ビルドが実行されているファイル システムに配置します。 Microsoft にホストされるエージェントまたはビルド ユーザーは、このパスとファイルへのアクセスが必要です。
- 拇印を使用してストア内の証明書を検索し、その証明書でサインインします。

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Universal Windows Platform アプリの署名にセキュリティで保護されたファイル タスクを使用する

> [!NOTE]
> Azure Key Vault を使用して証明書を格納し、Azure 署名ツールを使用して Modern POS .appx ファイルおよびセルフサービス インストーラーに署名することもできます。 サンプルのパイプライン スクリプトと追加情報については、[Azure DevOps でビルド パイプラインを設定して Retail セルフサービス パッケージを生成する](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages)を参照してください。

セキュリティで保護されたファイル タスクの使用は、Universal Windows Platform (UWP) アプリの署名に推奨される方法です。 パッケージ署名の詳細については、[パッケージ署名の構成](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing)を参照してください。 このプロセスを次の図に示します。

![MPOS アプリ署名フロー。](media/POSSigningFlow.png)

> [!NOTE]
> 現在 OOB パッケージでは、.appx ファイルの署名のみがサポートされており、MPOIS、RSSU、HWS などのセルフ サービスの他のインストーラーは、このプロセスによって署名されません。 SignTool またはその他の署名ツールを使用して、手動で署名する必要があります。 .appx ファイルの署名に使用する証明書は、Modern POS がインストールされているマシンにインストールする必要があります。

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Azure Pipelines にサインインするための証明書を構成する手順

### <a name="certificate-in-the-file-systemsecure-location"></a>ファイル システム / 安全な場所の証明書

[ダウンロードファイル タスク](/visualstudio/msbuild/downloadfile-task)をダウンロードして、ビルド プロセスの最初の手順として追加します。 セキュリティで保護されたファイルのタスクを使用する利点は、ビルド パイプラインが成功したか、失敗したか、またはキャンセルされたかに関係なく、ビルド時にファイルが暗号化されてディスクに格納されることです。 このファイルは、ビルド プロセスの完了後にダウンロード場所から削除されます。

1. 最初のステップとして、Azure ビルド パイプラインでセキュア ファイル タスクをダウンロードして追加します。 セキュア ファイル タスクは、[DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile) からダウンロードできます。
1. 次の図に示すように、証明書をセキュア ファイル タスクにアップロードし、出力変数で参照名を設定します。
    > [!div class="mx-imgBorder"]
    > ![セキュア ファイル タスク。](media/SecureFile.png)
1. **変数** タブの下の **新しい変数** を選択して、Azure Pipelines に新しい変数を作成します。
1. 値フィールドに変数の名前を入力します (例: **MySigningCert**)。
1. 変数を保存します。
1. **RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、パイプラインで作成された変数名で **ModernPOSPackageCertificateKeyFile** を更新します (手順 3)。 例:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    証明書がパスワードで保護されていない場合は、この手順を実行する必要があります。 証明書がパスワードで保護されている場合は、次の手順に進みます。
    
1. 証明書で署名する際に MPOS .appx ファイルにタイムスタンプを付ける場合は、**Retail SDK\\ビルド ツール\\Customization.settings** ファイルを開き、タイムスタンプ プロバイダーで **ModernPOSPackageCertificateTimestamp** 変数を更新します (例: `http://timestamp.digicert.com`)。
1. パイプラインの **変数** タブで、セキュリティで保護された新しいテキスト変数を追加します。 名前を **MySigningCert.secret** に設定し、証明書のパスワードの値を設定します。 変数を保護するには、ロック アイコンを選択します。
1. **Powershell スクリプト** タスクをパイプラインに追加します (セキュリティで保護されたファイルのダウンロード後、およびビルド ステップの前)。 **表示** 名を指定し、タイプを **インライン** として設定します。 以下をコピーしてスクリプト セクションに貼り付けます。

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. **RetailSDK\\BuildTools** から **Customization.settings** ファイルを開き、**ModernPOSPackageCertificateThumbprint** を証明書の拇印の値で更新します。

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
証明書の拇印を取得する方法の詳細については、[証明書の印刷を取得する](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint)を参照してください。 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>SDK の msbuild を使用して手動で MPOS アプリに署名する証明書をダウンロードまたは生成する

ダウンロードまたは生成された証明書を使用して MPOS アプリに署名する場合、**BuildTools\\Customization.settings** ファイルの **ModernPOSPackageCertificateKeyFile** ノードを更新して、pfx ファイルの場所 (**$(SdkReferencesPath)\\appxsignkey.pfx**) を指すようにします。 例:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

この場合、証明書ファイル名は **appxsignkey.pfx** であり、**Retail SDK\\ 参照** フォルダーに配置されます。

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>拇印を使用して MPOS アプリに署名する

拇印を使用して MPOS アプリに署名する場合は、証明書をローカルにインストールします。 **BuildTools\\Customization.settings** ファイルにある **ModernPOSPackageCertificateThumbprint** ノードで、拇印の値を更新します。

このオプションは、ビルド ユーザーがローカル ユーザーの場合に機能します。 ただし、Azure DevOps エージェントを使用してビルドを生成している場合、エージェントは証明書ストアにアクセスして署名に証明書を使用する権限を持たないので、ビルド マシンに証明書がインストールされない可能性があります。　 この場合、ビルド ユーザーをローカル ユーザーに変更し、そのボックスに証明書をインストールすることをお勧めします。 ただし、ボックスへの管理者アクセス権限がない場合は、このオプションは使用できません。

> [!NOTE]
> pfx file またはセキュア ファイル タスク オプションを使用してアプリに署名する場合は、**Customization.settings** の **ModernPOSPackageCertificateThumbprint** ノードを空のままにします。 拇印オプションが使用されている場合、**ModernPOSPackageCertificateKeyFile** を空のままにします。 両方の値を更新すると、ビルドが失敗します。

### <a name="certification-renewal"></a>証明書の更新

### <a name="renew-a-certificate-from-trusted-ca"></a>信頼される CA から証明書を更新する

証明書の更新プロセスについては、証明機関 (CA) に問い合わせてください。 信頼される証明書については、MPOS 側でアクションを実行する必要はありません。

### <a name="renew-a-self-signed-certificate"></a>自己署名証明書を更新する

実稼働用の Retail SDK で使用可能なサンプル証明書は使用しないでください。 開発の目的にのみ使用できます。 サンプルの Contoso の証明書は更新することができず、10.0.16 またはそれ以前のバージョンの Retail SDK に含まれているサンプルの証明書は、2020 年 12 月 31 日に有効期限が切れます。 カスタマイズされた Modern POS に署名するためにこの証明書または自己署名証明書を使用した場合、この日付の後は Modern POS が正しく機能しなくなる可能性が大いにあります。
 
### <a name="impact"></a>影響
 
上記の場合、2020 年 12 月 31 日以降はインストーラーを実行できないという問題が発生します。 使用している会社の IT ポリシーによっては、Modern POS が機能しない場合があります。 組織への影響を判断するために、日付を一時的に未来の日付に変更してテストすることが重要です。
 
### <a name="steps-to-determine-the-issue"></a>問題を特定する手順
 
1.  Windows の設定を使用して、コンピュータの日時を 2021 年の時刻に変更します。
2.  Modern POS を開くことができることを確認し、サインインを実行すると、トランザクションを完了することができます。
3.  Modern POS のセルフ サービス インストーラーが実行可能であることを確認します。実行可能な場合、インストールは正常に完了します。
4.  Windows の日時設定を正しい時刻に戻します。
 
これらの手順すべてを問題なく完了できる場合、現在の証明書で 2020 年 12 月 31 日までの操作が可能になります。  
 
### <a name="steps-going-forward"></a>今後の手順 

以前に使用していた証明書を更新することを強くお勧めします。 新しい証明書を取得することを強くお勧めします。 これを実行するには、次のアクションのいずれかを実行する必要があります。
 
- **優先** - 信頼される証明機関からコード署名証明書を取得します。

- **非優先** - 使用する自己署名のコード署名証明書を生成します。 これは通常、ドメイン内の開発目的でのみ使用され、本番に対して推奨されません。 

- **一時的なソリューションとして利用可能** - 更新された Contoso のコード署名証明書を使用します。 通常、これはテスト目的で使用されるため、運用環境に配置することはお勧めできません。
 
次に、上記のいずれかのアクションから取得した証明書を使用して署名された、新しくカスタマイズされた Modern POS のパッケージを生成します。 証明書に応じて、次のいずれかの手順を実行します。
 
- 新しい信頼される証明書 (または新しい自己署名の証明書) を使用する場合、すべてのデバイスに新しい証明書をインストールする必要があります。 その後、新しく作成された Modern POS のパッケージ (インストーラー) を使用して、既存のアプリケーションをアンインストールし、新しい Modern POS パッケージを再インストールする必要があります。 すべてのデバイスで Modern POS のデバイスの有効化を実行する必要があります。

- 更新された Contoso 証明書を使用する場合、すべてのデバイスに新しい証明書をインストールして、Modern POS パッケージ (インストーラー) をインストールする必要があります。 アンインストールする必要はありませんが、デバイスに再インストールする必要があります。 Modern POS のデバイスの有効化は必須ではないことに注意してください。 このオプションは一時的なソリューションです。 新しい信頼される証明書を取得する前にこのオプションを使用するだけで最有効化を回避し、問題を解決することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
