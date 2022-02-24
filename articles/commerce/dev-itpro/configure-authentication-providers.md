---
title: 認証プロバイダーのコンフィギュレーション
description: このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。
author: kfend
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 31241
ms.assetid: fef883f3-981a-4bba-9a41-d9dde63b0cd0
ms.search.region: Global
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7949eb77abddd7749d8fb5642419a24ebb25bfe8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683369"
---
# <a name="configure-authentication-providers"></a>認証プロバイダーのコンフィギュレーション

[!include [banner](../includes/banner.md)]

このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。

E コマース プラットフォームは、認証のためのメカニズムとして業界標準の [OpenID Connect](https://openid.net/connect/) を使用します。 この記事では、オンライン ストアで使用される OpenID プロバイダーを登録するために使用するページについて説明します。 Commerce Scale Unit は、認証された顧客をサポートするメカニズムとして OpenID Connect を使用します。 OpenID 接続は、シンプルで発展した ID プロバイダーとして、OAuth 2.0 に加えて広く受け入れられている標準です。 Commerce Scale Unit は、Microsoft Azure アクセス制御サービスを通じてすぐに使用できる OpenID プロバイダー、およびその他の個別に使用可能なプロバイダーの両方と統合することができます。 さらに、OpenID 接続をサポートするカスタム プロバイダーを統合および登録できます。 次の図は、Commerce Scale Unit と電子商取引のフロント エンド サーバーの間で発生し、後続の呼び出しで認証トークンを渡すステップ バイ ステップのハンドシェイクを示しています。 

[![OpenId](./media/openid-1024x540.png)](./media/openid.png) 

Commerce Scale Unit で使用できるようにするため、OpenID プロバイダーを登録するプロセスのチュートリアルを次に示します。

1.  Retail and Commerce IT ワークスペースから、**コマース共有パラメーター** &gt; **OpenID プロバイダー** に移動します。 **OpenID プロバイダー** ページを使用すると追加プロバイダーを登録することができます。 サポートする各プロバイダーについては、OpenID プロバイダーの詳細および依存する関係者の詳細を入力します。 Commerce Scale Unit は、この情報を使用し、認証トークンを要求して後続の呼び出しに使用します。
2.  配送スケジュール 1110 を実行します。
3.  テスト オンライン ストアについては、次の例に示すように、正しいリダイレクト URL とドメインを指定できるように web.config ファイルを編集します。 第三者のオンライン ストアを使用している場合、この情報を必要に応じて保存できます。

    ```xml
    redirectUrl=https://usnconeboxax1ecom.cloud.onebox.dynamics.com/en/Pages/OauthV2Redirect/OauthV2Redirect.aspx
    ```
