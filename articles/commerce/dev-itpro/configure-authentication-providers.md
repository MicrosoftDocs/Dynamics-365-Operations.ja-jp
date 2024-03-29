---
title: 認証プロバイダーの構成
description: この記事では、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。
author: josaw1
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.custom: 31241
ms.assetid: fef883f3-981a-4bba-9a41-d9dde63b0cd0
ms.openlocfilehash: 93e895aaaa985b0dbff6c1bd7aeaca75fb7fb196
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270023"
---
# <a name="configure-authentication-providers"></a>認証プロバイダーの構成

[!include [banner](../includes/banner.md)]

この記事では、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。

E コマース プラットフォームは、認証のためのメカニズムとして業界標準の [OpenID Connect](https://openid.net/connect/) を使用します。 この記事では、オンライン ストアで使用される OpenID プロバイダーを登録するために使用するページについて説明します。 Commerce Scale Unit は、認証された顧客をサポートするメカニズムとして OpenID Connect を使用します。 OpenID 接続は、シンプルで発展した ID プロバイダーとして、OAuth 2.0 に加えて広く受け入れられている標準です。 Commerce Scale Unit は、Microsoft Azure アクセス制御サービスを通じてすぐに使用できる OpenID プロバイダー、およびその他の個別に使用可能なプロバイダーの両方と統合することができます。 さらに、OpenID 接続をサポートするカスタム プロバイダーを統合および登録できます。 次の図は、Commerce Scale Unit と電子商取引のフロント エンド サーバーの間で発生し、後続の呼び出しで認証トークンを渡すステップ バイ ステップのハンドシェイクを示しています。 

[![OpenId。](./media/openid-1024x540.png)](./media/openid.png) 

Commerce Scale Unit で使用できるようにするため、OpenID プロバイダーを登録するプロセスのチュートリアルを次に示します。

1.  Retail and Commerce IT ワークスペースから、**コマース共有パラメーター** &gt; **OpenID プロバイダー** に移動します。 **OpenID プロバイダー** ページを使用すると追加プロバイダーを登録することができます。 サポートする各プロバイダーについては、OpenID プロバイダーの詳細および依存する関係者の詳細を入力します。 Commerce Scale Unit は、この情報を使用し、認証トークンを要求して後続の呼び出しに使用します。
2.  配送スケジュール 1110 を実行します。
3.  テスト オンライン ストアについては、次の例に示すように、正しいリダイレクト URL とドメインを指定できるように web.config ファイルを編集します。 第三者のオンライン ストアを使用している場合、この情報を必要に応じて保存できます。

    ```xml
    redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx
    ```


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
