---
title: "E コマース プラットフォーム SDK"
description: "このトピックでは、電子商取引プラットフォーム SDK について説明します。"
author: kfend
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 18101
ms.assetid: c0b1740b-1cbb-47c4-94e8-779cde8411af
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 5bacd7a3d02b9ee6b760ffb91b391de352636441
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="e-commerce-platform-sdk"></a>E コマース プラットフォーム SDK

[!include [banner](../includes/banner.md)]

このトピックでは、電子商取引プラットフォーム SDK について説明します。 E コマース プラットフォーム SDK は、次のコンポーネントで構成されています。

-   フレームワーク
-   コントロール
-   発行 (バージョン 1661 以上でサポートされます: [Retail サーバーでのサービス間認証のサポート](https://community.dynamics.com/ax/b/axforretail/archive/2016/09/24/support-for-service-to-service-authentication-in-retail-server))
-   サンプル ASP.net Web サイト

## <a name="use-the-sample-aspnet-website"></a>サンプル asp.net web サイトの使用
### <a name="use-the-retailsdk-to-create-the-sample-aspnet-website"></a>RetailSDKを使用して、サンプルの asp.net Web サイトを作成します。

1.  管理モードで Visual Studio 2015 を開きます。 これは、inetpub フォルダーにパブリッシュするために必要です。
2.  C:\\Microsoft Dynamics AX70\\RetailSdkOnlineStoreOnlineStore.sln を開き、すべてのフレームワーク コンポーネントを含めます。
3.  サンプルのオンライン ストアは C:\\Microsoft Dynamics AX70\\RetailSdkSampleExtensionsOnlineStore にあります。
4.  Visual Studio 内から Web ストア フロントをコンパイルし、公開します。
5.  IIS マネージャーから RetailStorefrontWebSite のパスを更新します。
    -  既定の設定によって作成された RetailStorefrontWebSite は C:\\Microsoft Dynamics AX70\\Retail Store Front\\Package を指定することに注意してください。
    -  ただし、RetailSDK から Web ストアフロントを公開すると、C:\\inetpub\\RetailWeb\\Storefront でファイルがドロップされます。
    -  したがって、RetailStorefrontWebSite の物理パスは、以前と同じポートで Web ストア フロントにアクセスする「C:\\inetpub\\RetailWeb\\Storefront」にポイントするように更新される必要があります。 もう 1 つのオプションは、新しい Web サイトを作成し inetpub 場所を指すことです。

6.  http://localhost:55080 を参照、または https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/ にアクセスし、テスト asp.net Web サイトを表示します。

### <a name="enabling-anonymous-access"></a>匿名アクセスの有効化

E コマース Web サイトでは、匿名アクセスを有効にする必要があります。 これは、アプリケーション設定で Retail Server web.config の web.config ファイルとして利用できます。 Web サイトが動作するため、これが有効であることを確認してください。 &lt;キーの追加 ="IsAnonymousEnabled" 値 ="true" /&gt;

### <a name="externally-accessing-the-aspnet-website"></a>ASP.net Web サイトに外部からアクセス

これらのいずれかが当てはまる場合は、次の設定変更が必要になります。

-   電子商取引サーバーと同梱上にはないブラウザー内から Web ストア フロントにアクセスしています。
-   電子商取引サーバーと retail サーバーが 2 つの異なるボックス上にある場合。

RetailStorefrontWebSite の web.config ファイル内の "retailServerUrl" を更新する必要があります。 ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。

- retailServerUrl=<http://localhost:35080/RetailServer/V1>
- &lt;キーの追加 ="RetailServerRoot" 値 ="<http://localhost:35080/RetailServer/V1>" /&gt;

Web ストア フロントを HTTPS 経由でアクセスする場合は、前述の Url を同等の HTTPS に更新する必要があります。

### <a name="operating-unit-or-channel-configuration"></a>作業単位またはチャンネルのコンフィギュレーション

E コマースの Web サイトは、web.configで指定された作業単位数 (チャネル) で動作します。これを変更するには、以下の OU \# を変更します。 Fabrikam はデモ データ内で「077」であることに注意してください。 RetailStorefrontWebSite の web.config 内の "retailServerUrl" を更新する必要があります。 ローカル ホストの代わりにマシン名を使用するには、次の 2 つのフィールドを更新する必要があります。

    <ecommerceControls productUrlFormat="/Pages/ProductDetails/ProductDetails.aspx?itemId={0}" retailServerUrl="http://localhost:35080/RetailServer/V1" operatingUnitNumber="068">

    <add key="OperatingUnitNumber" value="068" />

## <a name="configure-authentication-providers"></a>認証プロバイダーのコンフィギュレーション
### <a name="authentication-providers-that-you-are-using"></a>使用している認証プロバイダー

E コマース プラットフォームは、認証のためのメカニズムとして OpenID を使用します。 以下のテーブルに選択した任意の OpenID プロバイダーを登録することにより、この作業を実行することができます。 必要に応じて、テストにログインすることができます。

1.  web.config ファイルを編集し、次のように変更してください。

        redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx

    後続のステップは、追加プロバイダーを登録する場合にのみ行う必要があります。

2.  [Retail 共有パラメーター] -&gt; [ID プロバイダーを開く] フォームは、追加プロバイダーを登録するために使用できます。
3.  配送スケジュール 1110 を実行します。


