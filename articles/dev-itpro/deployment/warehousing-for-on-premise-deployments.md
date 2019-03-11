---
title: オンプレミス配置の倉庫管理アプリを構成
description: このトピックでは、オンプレミス展開でのウェアハウス アプリの前提条件について説明します。
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 24861
ms.assetid: 63e43066-76c7-400b-be7d-d14785e7985d
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 820a557dc77f259c9503f02c7eac9eadfa8f9512
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369023"
---
# <a name="configure-the-warehousing-app-for-on-premises-deployments"></a>オンプレミス配置の倉庫管理アプリを構成

[!include [banner](../includes/banner.md)]

このトピックでは、オンプレミス配置の Microsoft Dynamics 365 for Finance and Operations - Warehousing の構成方法について説明します。

## <a name="prerequisites"></a>必要条件
倉庫管理アプリは Android および Windows オペレーティング システムで使用できます。 オンプレミスの展開にこのアプリを使用するには、少なくともバージョン 1.1.1.0 である必要があります。 Microsoft Dynamics 365 for Finance and Operations が次のサポートされているバージョンの 1 つである必要もあります。 ハードウェアおよびソフトウェア環境で構成がサポートされているかどうかを評価するには、次の表の情報を使用します。

| プラットフォーム               | バージョン                                                                            |
|------------------------|------------------------------------------------------------------------------------|
| Android                | 4.4 以上                                                                         |
| Windows (UWP)          | Windows 10 (すべてのバージョン)                                                          |
| アプリのバージョン            | 1.1.1.0 以上                                                                  |
| Microsoft Dynamics 365 | Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 11 (オンプレミス) |

アプリでオンプレミス リソースにアクセスできるようにするには、AOS および Active Directory フェデレーション サービス（AD FS）の DNS レコードを作成する必要があります。 ガイダンスについては、[DNS ゾーンの作成とレコードの追加](setup-deploy-on-premises-pu12.md#setup) を参照してください。

## <a name="create-an-application-entry-in-ad-fs"></a>AD FS でアプリケーション エントリを作成する
AD FS およびFinance and Operations 間で認証を正常に交換するために、AD FS アプリケーション グループの下の AD FS にアプリケーション エントリを登録する必要があります。 このアプリケーション エントリを作成するには、AD FS がインストールされているマシンで次の Windows PowerShell コマンドを実行します。 ユーザー アカウントには、AD FS を管理するための十分なアクセス許可が必要です。

1.  アプリケーションのエントリを作成する Windows PowerShell コンソールに、次のコマンドを入力します。  
    
        Add-AdfsClient -Name 'Dynamics 365 for Finance and Operations - Warehousing' -ClientId ([guid]::NewGuid()) -ClientType Confidential -GenerateClientSecret -RedirectUri '\<Resource URL\>' -ADUserPrincipalName '\<Admin user\>' 

    - \<リソース URL\> は、たとえば `https://ax.d365ffo.onprem.contoso.com` などです (`https://ax.d365ffo.onprem.contoso.com` は、Finance and Operations にアクセスするための URL です)。
    - \<管理者ユーザー\> は、AD FS コンピューターへの管理者のアクセス権を持つ任意のユーザーにすることができます。

2.  受信した値を保存します。

3.  アプリケーションへのアクセス許可を付与するには、次のコマンドを実行します。  
    
        Grant-AdfsApplicationPermission -ClientRoleIdentifier '\<Client ID received in previous steps\>' -ServerRoleIdentifier '\<Resource URL\>' -ScopeNames 'openid'

## <a name="create-and-configure-a-user-account"></a>ユーザー アカウントの作成およびコンフィギュレーション

Dynamics 365 for Finance and Operations で AD FS アプリケーションを使用できるようにするには、倉庫管理アプリのユーザーと同じユーザー資格情報を使用して Microsoft Dynamics 365 でユーザー アカウントを作成する必要があります:

1.  Finance and Operations でユーザーを作成し、倉庫管理モバイル デバイス ユーザー ロールをユーザーに割り当てます。

    a.  **システム管理** \> **共通** \> **ユーザー**の順に移動します。
    
    b.  新規ユーザーを作成します。
    
    c.  例のスクリーンショットに示されているように、倉庫モバイル デバイス ユーザー ロールを割り当てます。

    ![ユーザーの作成およびコンフィギュレーション](media/wmapp-users.png)

2.  AD FS アプリケーションと倉庫保管アプリ ユーザーを関連付けます。

    a.  Finance and Operations で、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション**をクリックします。
    
    b.  新しい行を作成します。
    
    c.  AD FS でアプリケーション エントリを作成したときに取得したクライアント ID を入力します (「AD FS でのアプリケーション エントリの作成」の手順 2)。 名前を入力し、倉庫管理アプリ ユーザーを選択します。

    ![Azure Active Drectory アプリケーション ](media/azure-active-directory.png)

## <a name="certificates"></a>証明書 

アプリがインストールされているデバイスに、リソースにアクセスする適切な証明書があることを確認します。 自己署名証明書を使用している場合、コンピューター アカウント/ユーザー アカウントの信頼されているルートに star(AX) と AD FS をインポートすることで、これらが各デバイスにインストールされている必要があります。 詳細については、[自己署名証明書の作成およびエクスポート](https://technet.microsoft.com/en-us/library/ff710475(v=ws.10).aspx) を参照してください。

## <a name="configure-the-application"></a>アプリケーションのコンフィギュレーション

AD FS アプリケーションを使用して Finance and Operations サーバーに接続するには、デバイス上で倉庫管理アプリを設定する必要があります。

1.  アプリで**接続設定**を開きます。
2.  次の情報を入力します。

    a.  **Active Directory クライアント ID** - AD FS でアプリケーション エントリを作成したときに取得したクライアント ID (「AD FS でのアプリケーション エントリの作成」の手順 2)。

    b.  **Active Directory クライアント シークレット** - AD FS でアプリケーション エントリを作成したときに取得したクライアント シークレット。

    c.  **Active Directory リソース** - Finance and Operations AOS の DNS URL。 URL に「/namespaces/AXSF」を追加します。 
        例: `https://ax.d365ffo.onprem.contoso.com/namespaces/AXSF`

    d.  **Active Directory テナント** - Finance and Operations AD FS マシンの DNS URL。 URL に「/adfs/oauth2」を追加します。 
        例: `https://adfs.d365ffo.onprem.contoso.com/adfs/oauth2` ADFS マシン (例では CNAME は `https://adfs.d365ffo.onprem.contoso.com` です) の CNAME を使用していることを確認します

3.  **会社** - Finance and Operations にアプリケーションが接続する法的エンティティを入力します。
4.  アプリケーションの左上隅にある **戻る** ボタンを選択します。

    アプリケーションは Finance and Operations サーバーに接続し、倉庫ワーカーのログイン画面が表示されます。
