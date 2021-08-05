---
title: サービス認証問題のトラブルシューティング
description: このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。
author: nimakms
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 195943
ms.assetid: 0c22fad3-be0a-4111-97c0-2f3fadfd5f6b
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f47cddcf9898a275cd0e6f054a99197a1509c41e
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359351"
---
# <a name="troubleshoot-service-authentication-issues"></a>サービス認証問題のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。

サービス認証の問題をトラブルシューティングする場合、もっともよく発生する問題の解決に役立ついくつかの基本的な共通の手順があります。 また、これらの手順では、認証メカニズムの仕組みを実際に実演します。 このトピックでは手順を説明し、これまでに生じたいくつかの一般的な問題を一覧表示しています。

## <a name="inspect-the-jwt"></a>JWT を検査します。
### <a name="capture-the-jwt-from-an-http-request"></a>HTTP 要求から JWT をキャプチャします。

1. Fiddler を <https://www.telerik.com/fiddler> からダウンロードします。
2. クライアントから HTTPS トラフィックを監視するには、HTTPS キャプチャを設定します。
3. 未処理認証 (OAuth) JSON Web トークン (JWT) を検索します。 これは、「ベアラー」セグメントのない HTTP「認証」ヘッダーの値です。

### <a name="use-a-deserializer-tool-to-look-at-the-token-contents"></a>逆シリアル化ツールを使用してトークンの内容を確認

1. <https://jwt.io> に移動し、入力パネルに JWT を貼り付けます。
2. 名前と値の組でコンテンツを表示します。 次の例を参照してください。
3. 次の情報が正しいことを確認します。

    - **"aud"** - 値は、Microsoft Azure Active Directory (Azure AD) リソースという概念に対応します。 「aud」を含む典型的な問題を以下に示します。

        - JWT の **"aud"** セグメントには、末尾にスラッシュを持つ URI が含まれています。
        - JWT の **"aud"** セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれています。 URI は、すべて小文字であることが必要です。

    - **"appid"** - 値は Azure AD ネイティブ クライアント アプリ ID (またはサービス アプリ ID) に対応します。
    - **"upn"** - 値はネイティブ クライアント アプリケーションを通じて認証されているユーザーに対応します。

次の図は、JWT のコンテンツの例を示します。

[![JWT の例。](./media/serviceauthenticationtroubleshooting01.png)](./media/serviceauthenticationtroubleshooting01.png)

## <a name="review-the-event-logs"></a>イベント ログを確認
また、仮想マシン (VM) に対するアクセス権限がある場合、インスタンス マシンのイベント ログを確認することができます。

1. **実行** ウィンドウから **eventvwr** コマンドを実行してイベント ビューアーを起動します。
2. 次のチャンネルに移動します。

    - アプリケーションとサービス ログ &gt; Microsoft &gt; Dynamics &gt; AX-IntegrationServices &gt; Channel:Operational (Microsoft-Dynamics-AX-IntegrationServices/運用)
    - アプリケーションとサービス ログ &gt; Microsoft &gt; Dynamics &gt; AX-SystemRuntime &gt; Channel:Operational (Microsoft-Dynamics-AX-SystemRuntime/運用)

## <a name="other-approaches"></a>その他の方法
- OAuth がコンフィギュレーションされる方法の詳細については、[サービス エンドポイント概要](services-home-page.md) を参照してください。
- また、自分自身のクライアント コードを使用して、並列でサービスの呼び出しを試みることができます。 公開されたサンプル コードは <https://github.com/Microsoft/Dynamics-AX-Integration> で入手できます。
- 2 番目のメソッドが動作する場合は、それぞれのメソッドで JWT を比較できます。

## <a name="known-issues"></a>既知の問題
### <a name="aadsts65001-the-user-or-administrator-hasnt-consented-to-use-the-application"></a>AADSTS65001: ユーザーまたは管理者がアプリケーションの使用に同意していない

- JWT の **"aud"** セグメントには、末尾にスラッシュを持つ URI が含まれている可能性があります。 スラッシュを削除する必要があります。
- JWT の **"aud"** セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれている可能性があります。 URI は、すべて小文字であることが必要です。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]