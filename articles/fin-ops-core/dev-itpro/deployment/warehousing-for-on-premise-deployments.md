---
title: オンプレミス展開の倉庫管理アプリの構成
description: この記事では、オンプレミス展開でのウェアハウス アプリの前提条件について説明します。
author: faix
ms.date: 04/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 5ce28e20f3749d855811f0404d106f2329981dea
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867290"
---
# <a name="configure-the-warehousing-app-for-on-premises-deployments"></a>オンプレミス展開の倉庫管理アプリの構成

[!include [banner](../includes/banner.md)]

この記事では、オンプレミス配置の Dynamics 365 for Finance and Operations – Warehousing アプリの構成方法について説明します。

## <a name="prerequisites"></a>必要条件
倉庫管理アプリは Android および Windows オペレーティング システムで使用できます。 オンプレミスの展開にこのアプリを使用するには、少なくともバージョン 1.1.1.0 である必要があります。 Dynamics 365 Finance + Operations (on-premises) が次のサポートされているバージョンの 1 つである必要もあります。 ハードウェアおよびソフトウェア環境で構成がサポートされているかどうかを評価するには、次の表の情報を使用します。

| プラットフォーム               | バージョン                                                                            |
|------------------------|------------------------------------------------------------------------------------|
| Android                | 4.4 以上                                                                         |
| Windows (UWP)          | Windows 10 (すべてのバージョン)                                                          |
| アプリのバージョン            | 1.1.1.0 以上                                                                  |
| Dynamics 365 | Dynamics 365 Finance + Operations (on-premises) およびプラットフォーム更新プログラム 11 |

アプリでオンプレミス リソースにアクセスできるようにするには、AOS および Active Directory フェデレーション サービス（AD FS）の DNS レコードを作成する必要があります。 ガイダンスについては、[DNS ゾーンの作成とレコードの追加](setup-deploy-on-premises-pu12.md#setup) を参照してください。

## <a name="create-an-application-entry-in-ad-fs"></a>AD FS でアプリケーション エントリを作成する
AD FS および Finance + Operations 間で認証を正常に交換するために、AD FS アプリケーション グループの下の AD FS にアプリケーション エントリを登録する必要があります。 このアプリケーション エントリを作成するには、AD FS がインストールされているマシンで次の Windows PowerShell コマンドを実行します。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。

1.  アプリケーションのエントリを作成する Windows PowerShell コンソールに、次のコマンドを入力します。  

    ```powershell
    Add-AdfsClient -Name 'Dynamics 365 for Finance and Operations - Warehousing' -ClientId ([guid]::NewGuid()) -ClientType Confidential -GenerateClientSecret -RedirectUri '\<Resource URL\>' -ADUserPrincipalName '\<Admin user\>' 
    ```

    - \<Resource URL\> は、たとえば `https://ax.d365ffo.onprem.contoso.com` などです (`https://ax.d365ffo.onprem.contoso.com` は、Finance + Operations にアクセスするための URL です)。
    - \<Admin user\> は、AD FS マシンへの管理者アクセスを持つ任意のユーザーにすることができます。

2.  受信した値を保存します。

3.  アプリケーションへのアクセス許可を付与するには、次のコマンドを実行します。  
    
    ```powershell
    Grant-AdfsApplicationPermission -ClientRoleIdentifier '\<Client ID received in previous steps\>' -ServerRoleIdentifier '\<Resource URL\>' -ScopeNames 'openid'
    ```

## <a name="create-and-configure-a-user-account"></a>ユーザー アカウントの作成およびコンフィギュレーション

Finance + Operations で AD FS アプリケーションを使用できるようにするには、倉庫管理アプリのユーザーと同じユーザー資格情報を使用して Microsoft Dynamics 365 でユーザー アカウントを作成する必要があります:

1.  Finance + Operations でユーザーを作成し、倉庫管理モバイル デバイス ユーザー ロールをユーザーに割り当てます。

    1.  **システム管理** \> **共通** \> **ユーザー** の順に移動します。
    
    2.  新規ユーザーを作成します。
    
    3.  例のスクリーンショットに示されているように、倉庫モバイル デバイス ユーザー ロールを割り当てます。

    ![ユーザーを作成およびコンフィギュレーションします。](media/wmapp-users.png)

2.  AD FS アプリケーションと倉庫保管アプリ ユーザーを関連付けます。

    1.  Finance + Operations で、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** をクリックします。
    
    2.  新しい行を作成します。
    
    3.  AD FS でアプリケーション エントリを作成したときに取得したクライアント ID を入力します (「AD FS でのアプリケーション エントリの作成」の手順 2)。 名前を入力し、倉庫管理アプリ ユーザーを選択します。

    ![Azure Active Drectory アプリケーション。](media/azure-active-directory.png)

## <a name="certificates"></a>証明書 

アプリがインストールされているデバイスに、リソースにアクセスする適切な証明書があることを確認します。 自己署名証明書を使用している場合、コンピューター アカウント/ユーザー アカウントの信頼されているルートにスター証明書と AD FS証明書をインポートすることで、これらが各デバイスにインストールされている必要があります。 詳細については、[自己署名証明書の作成およびエクスポート](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/ff710475(v=ws.10)) を参照してください。

> [!IMPORTANT]
> 自己署名証明書のある環境には、Android デバイスからアクセスできません。 Android デバイスから環境にアクセスする必要がある場合は、AD FS および Finance + Operations に対して公開されている信頼できる証明書を使用します。 また、AD CS を使用して AD FS および Finance + Operations の証明書を生成できます。 ただし、その場合は、Android デバイスに手動で証明機関の証明書をインポートする必要があります。   

## <a name="configure-the-application"></a>アプリケーションのコンフィギュレーション

接続を設定して、AD FS アプリケーションを使用してサーバーに接続するには、デバイス上で倉庫管理アプリを設定する必要があります。 新しい接続を設定する複数の方法があります。

- ファイルから接続を追加します。
- QR コードから接続を追加します。
- 接続を手動で追加します。

### <a name="create-a-connection-settings-file-or-qr-code"></a>接続設定ファイル、またはQRコードを作成する

接続設定は、ファイルまたは QR コードからインポートできます。 いずれの方法でも、最初に JavaScript Object Notation (JSON) 形式と構文を使用した設定ファイルを作成する必要があります。 ファイルには、追加する必要のある個々の接続を含む接続のリストを含める必要があります。 次の表には、接続設定ファイルで指定する必要のあるパラメータをまとめています。

| パラメーター                  | 説明 | 
|----------------------------|-------------|
| ConnectionName             | 接続設定の名前を入力します。 最大 20 文字まで指定できます。 この値は、接続設定の固有の ID てあるため、リスト内で一意となっていることを確認してください。 デバイスに同じ名前の接続が既に存在する場合、インポートされたファイル設定によって上書きされます。 |
| ActiveDirectoryClientAppId | AD FS アプリケーションの設定時にメモしたクライアント ID を指定します。 |
| ActiveDirectoryResource    | <p>Finance + Operation (設置型) のルート URL を指定します。</p><p>**注記:**  **/namespaces/AXSF** を必ず含めてください。</p> | 
| ActiveDirectoryTenant      | AD FS サーバーの Open Authorization (OAuth) 2.0 エンドポイントを指定します。 この値は次のような形式です: `https://your-adfs-server/adfs/oauth2` 次の例を示します: `https://adfs.contoso.com/adfs/oauth2.` | 
| 会社                    | アプリケーションが接続する Finance + Operation (設置型) の法人を入力します。 | 
| ConnectionType             | <p>(オプション) 接続設定で、環境に接続する際に証明書を使用するか、クライアント シークレットを使用するかを指定します。 有効な値は、**certificate** および **clientsecret** です。 既定値は **certificate** です。</p><p>**注意 :** クライアント シークレットはインポートできません。</p> |
| IsEditable                 | (オプション) アプリのユーザーが接続設定を編集できるようにするかどうかを指定します。 有効な値は、**true** および **false** です。 既定値は **true** です。 | 
| IsDefault                  | (オプション) 接続が既定の接続であるかどうかを指定します。 既定の接続として設定されている接続は、アプリが開かれた際に自動的に設定が選択されます。 既定の接続にはひとつの接続のみを設定できます。 有効な値は、**true** および **false** です。 既定値は **false** です。 | 
| CertificateThumbprint      | (オプション) Windows デバイスでは、接続に使用する拇印の証明書を指定できます。 Android デバイスの場合、アプリのユーザーは初回の接続時に証明書を選択する必要があります。 | 

次の例では、2 つの接続を含む有効な接続設定ファイルを示しています。 こように、接続リスト (ファイル内の  connectionlist と呼ばれます) は、各接続をオブジェクトとして格納する配列を持つオブジェクトです。 各オブジェクトは、かっこ ({}) で囲み、コンマで区切る必要があります。また、配列は角かっこ ([]) で囲む必要があります。

```json
{
    "ConnectionList": [
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection1",
            "ActiveDirectoryResource": "https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF",
            "ActiveDirectoryTenant": "https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2",
            "Company": "USMF",
            "IsEditable": false,
            "IsDefaultConnection": true,
            "CertificateThumbprint": "aaaabbbbcccccdddddeeeeefffffggggghhhhiiiii",
            "ConnectionType": "certificate"
        },
        {
            "ActiveDirectoryClientAppId":"aaaaaaaa-bbbb-ccccc-dddd-eeeeeeeeeeee",
            "ConnectionName": "Connection2",
            "ActiveDirectoryResource": "https://ax2.d365ffo.onprem.contoso.com/namespaces/AXSF",
            "ActiveDirectoryTenant": "https://adfs2.d365ffo.onprem.contoso.com/adfs/oauth2",
            "Company": "USMF",
            "IsEditable": true,
            "IsDefaultConnection": false,
            "ConnectionType": "clientsecret"
        }
    ]
}
```

JSON ファイルの保存方法については、[接続設定のファイルを各デバイスに保存する](../../../supply-chain/warehousing/install-configure-warehousing-app.md#save-the-connection-settings-file-on-each-device) を参照してください。

ファイルを作成した後、インポートする必要があります。 詳細については、[接続設定をインポートする](../../../supply-chain/warehousing/install-configure-warehousing-app.md#import-the-connection-settings) を参照してください。

### <a name="manually-configure-the-application"></a>アプリケーションを手動で構成する

1. モバイル デバイスで倉庫管理アプリを起動します。
1. **接続設定** に移動します。
1. **デモ モードを使用する** オプションを **いいえ** に設定します。
1. **接続の選択** ドロップダウン コントロールをタップして、接続の詳細を手動で入力するために必要な設定を展開します。

    - **クライアント シークレットを使用する** – このオプションを **はい** に設定すると、クライアント シークレットを使用して Dynamics 365 Supply Chain Management の認証ができます。 認証に証明書を使用するには、**いいえ** に設定します。
    - **接続名称** – 新しい接続の名前を入力します。 この名前は、次に接続設定を開いたときに **接続の選択** フィールドに表示されます。 入力する名称は一意である必要があります。 (この名称は、デバイスに保存されている他のすべての接続名とは異なるものでなければなりません。)
    - **Active Directory クライアント ID** – AD FS でアプリケーション エントリを作成したときに取得したクライアント ID ([AD FS でのアプリケーション エントリの作成](#create-an-application-entry-in-ad-fs) セクションの手順 2)。
    - **Active Directory クライアント シークレット** – AD FS でアプリケーション エントリを作成したときに取得したクライアント シークレット。
    - **Active Directory リソース** – AOS インスタンスの DNS URL。 URL の末尾に **/namespaces/AXSF** を追加します。

        > [!NOTE]
        > 値の末尾には、スラッシュ (/) を入力しないでください。 たとえば、「`https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`」を入力します。

    - **Active Directory テナント** – AD FS マシンの DNS URL。 URL の末尾に **/adfs/oauth2** を追加します。 

        > [!NOTE]
        > 値の末尾には、スラッシュ (/) を入力しないでください。 たとえば、「`https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2`」を入力します。

    - **会社** – アプリケーションが接続する法人を入力します。

1. アプリケーションの右上隅にある **保存** ボタンを選択します。
1. Android デバイスを使用していて、かつ認証に証明書を使用している場合は、デバイスにで証明書の選択を促す画面が表示されます。

アプリケーションが Finance + Operations (on-premises) に接続し、倉庫作業者用のサインイン ページが表示されます。

> [!NOTE]
> 以前のリリースでは、倉庫アプリ ユーザーのテレメトリ ID がない場合、いくつかエラーが発生する可能性があります。 回避策は、Web クライアントを介して Finance + Operations (on-premises) にサインインし、テレメトリ ID を取得することです。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
