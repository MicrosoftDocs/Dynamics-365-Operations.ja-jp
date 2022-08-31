---
title: E コマース プラットフォーム ソフトウェア開発キット (SDK)
description: この記事では、電子商取引プラットフォーム SDK について説明します。
author: josaw1
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 18101
ms.assetid: c0b1740b-1cbb-47c4-94e8-779cde8411af
ms.openlocfilehash: a0e0d8f6df8736b8900e9c99912247ba9796b2bf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282853"
---
#  <a name="e-commerce-platform-software-development-kit-sdk"></a>E コマース プラットフォーム ソフトウェア開発キット (SDK)

[!include [banner](../includes/banner.md)]

この記事では、電子商取引プラットフォーム SDK について説明します。 E コマース プラットフォーム ソフトウェア開発キット (SDK) は、次のコンポーネントで構成されています。

-   フレームワーク
-   コントロール
-   発行 (バージョン 1661 以上でサポートされます: [Retail サーバーでのサービス間認証のサポート](https://community.dynamics.com/ax/b/axforretail/archive/2016/09/24/support-for-service-to-service-authentication-in-retail-server))
-   サンプル ASP.NET Web サイト

## <a name="use-the-sample-aspnet-website"></a>サンプル ASP.NET Web サイトの使用


### <a name="download-the-retail-sdk"></a>Retail SDK をダウンロード

Retail SDK は、開発環境と、Retail SDK フォルダーにある修正プログラム パッケージで使用できます。

- 開発インスタンスから SDK を取得すると、構成および使用の準備がすぐに整います。 詳細については、「[アクセス インスタンス](../../fin-ops-core/dev-itpro/dev-tools/access-instances.md)」を参照してください。 
- 修正プログラムから SDK を取得する場合は、修正プログラムのパッケージでは圧縮フォルダとして含まれています。 修正プログラムは累積的であり、その他のすべての修正プログラムが含まれています。 

Visual Studio Online などのソース管理システムに SDK を配置することをお勧めします。

### <a name="use-the-retail-sdk-to-create-the-sample-aspnet-website"></a>Retail SDK を使用して、サンプル ASP.NET Web サイトを作成する
1.  管理者モードで Visual Studio を開きます。 この手順は、inetpub フォルダーにパブリッシュするために必要です。
2.  C:\\Microsoft Dynamics AX70\\RetailSdkOnlineStoreOnlineStore.sln を開き、すべてのフレームワーク コンポーネントを含めます。
3.  サンプルのオンライン ストアは C:\\Microsoft Dynamics AX70\\RetailSdkSampleExtensionsOnlineStore にあります。
4.  Visual Studio 内から Web ストア フロントをコンパイルし、公開します。
5.  IIS マネージャーから RetailStorefrontWebSite のパスを更新します。
    -  既定の設定によって作成された RetailStorefrontWebSite は C:\\Microsoft Dynamics AX70\\Retail Store Front\\Package を指定することに注意してください。
    -  ただし、RetailSDK から Web ストアフロントを公開すると、C:\\inetpub\\RetailWeb\\Storefront でファイルがドロップされます。
    -  したがって、RetailStorefrontWebSite の物理パスは、以前と同じポートで Web ストア フロントにアクセスする「C:\\inetpub\\RetailWeb\\Storefront」にポイントするように更新される必要があります。 もう 1 つのオプションは、新しい Web サイトを作成し inetpub 場所を指すことです。

6.  `http://localhost:55080` を参照、または `https://usnconeboxax1ecom.cloud.onebox.dynamics.com/` にアクセスして、テスト ASP.NET Web サイトを表示します。

### <a name="enable-anonymous-access"></a>匿名アクセスの有効化

E コマース Web サイトでは、匿名アクセスが正常に機能するように許可する必要があります。 アプリケーション設定にある Commerce Scale Unit web.config ファイルに次のキーを追加して、匿名アクセスが有効であることを確認にします。

`
add key="IsAnonymousEnabled" value="true"
`

### <a name="externally-accessing-the-aspnet-website"></a>ASP.NET Web サイトに外部からアクセス

これらのいずれかが当てはまる場合は、次の構成の変更が必要になります。

-   E コマース サーバーと同じボックス上にはないブラウザー内から Web ストア フロントにアクセスしています。
-   E コマース サーバーおよび Commerce Scale Unit は 2 つの異なるボックス上にあります。

RetailStorefrontWebSite の web.config ファイル内の "retailServerUrl" を更新する必要があります。 ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。

```xml
retailServerUrl=<http://localhost:35080/RetailServer/V1>
<add key="RetailServerRoot" value="<http://localhost:35080/RetailServer/V1>" />
```

Web ストア フロントを HTTPS 経由でアクセスする場合は、前述の Url を同等の HTTPS に更新する必要があります。

### <a name="operating-unit-or-channel-configuration"></a>作業単位またはチャンネルのコンフィギュレーション

E コマースの Web サイトは、web.configで指定された作業単位数 (チャネル) で動作します。これを変更するには、以下の OU \# を変更します。 Fabrikam はデモ データ内で「077」であることに注意してください。 RetailStorefrontWebSite の web.config 内の "retailServerUrl" を更新する必要があります。 ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。

```xml
<ecommerceControls productUrlFormat="/Pages/ProductDetails/ProductDetails.aspx?itemId={0}" retailServerUrl="http://localhost:35080/RetailServer/V1" operatingUnitNumber="068">
<add key="OperatingUnitNumber" value="068" />
```

## <a name="configure-authentication-providers"></a>認証プロバイダーのコンフィギュレーション
### <a name="authentication-providers-that-you-are-using"></a>使用している認証プロバイダー

E コマース プラットフォームは、認証のためのメカニズムとして OpenID を使用します。 以下のテーブルに選択した任意の OpenID プロバイダーを登録することにより、この作業を実行することができます。 必要に応じて、テストにログインすることができます。

1.  web.config ファイルを編集し、次のように変更してください。

    ```xml
    redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx
    ```
    
    後続のステップは、追加プロバイダーを登録する場合にのみ行う必要があります。

2.  **Retail 共有パラメーター -&gt; ID プロバイダーを開く** フォームは、追加プロバイダーを登録するために使用できます。
3.  配送スケジュール 1110 を実行します。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
