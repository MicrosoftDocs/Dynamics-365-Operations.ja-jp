---
title: データベース移動 API - 認証
description: この記事では、データベース移動のアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。
author: laneswenka
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: fa31bcf57cd88c376aa6c05d767ccf8642a16c3e
ms.sourcegitcommit: e14648b01549bdc17998ffdef6cde273d4e78560
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/09/2022
ms.locfileid: "9242966"
---
# <a name="database-movement-api---authentication"></a>データベース移動 API - 認証

[!include [banner](../../includes/banner.md)]

この記事では、Database Movement API を含む Lifecycle Services API を呼び出すための Azure Active Directory (Azure AD) 設定の概要を提供します。  API Azure AD を使用して利用できるリソースにアクセスするには、各要求の一覧から証証を取得し、ヘッダーとして送信する必要があります。  このトークンを取得する手順は次のとおりです。

正しいアクセス許可を持つ持ち主トークンを取得するには、次の手順が必要です。

1. Azure AD テナントでアプリケーションの登録を作成する
2. API のアクセス許可の構成
3. パブリック クライアントの構成 
4. アクセス トークンの要求

## <a name="step-1-create-an-application-registration"></a>手順 1 アプリケーション登録を作成する
[Azure AD アプリケーションの登録](https://go.microsoft.com/fwlink/?linkid=2083908) ページに移動し、新しい登録を作成します。  アプリケーションに名前を付け、**シングル テナント** オプションが選択されている必要があります。  リダイレクト URI の設定をスキップすることができます。

## <a name="step-2-configure-api-permissions"></a>手順 2 API のアクセス許可の構成
新規アプリケーション登録内で、**管理 - API のアクセス許可** タブに移動します。**アクセス許可の構成** セクションで、**アクセス許可の追加** を選択します。  開いたダイアログ ウィンドウで、**自分の組織が使用する API** タブで、**Dynamics Lifecycle services** を検索します。  このような名前のエントリがいくつか表示される場合は、必ず GUID **913c6de4-2a4a-4a61-a9ce-945d2b2ce2e0** を持つものを使ってください。  

> [!NOTE]
> これらの API では、委任されたアクセス許可を現時点でのみ使用します。  ユーザー コンテキストで実行するアプリケーションの場合は、**user_impersonation** の **スコープ** パラメーターを使用して、委任されたアクセス許可を要求します。  これらのアクセス許可は、アプリケーションにサインイン ユーザーの特権を委任し、API エンドポイントを呼び出す際のユーザーの機能を許可します。
>
> アプリケーションが独自の ID または管理 ID を使用して API を呼び出すサービス プリンシパル認証はサポートされていません。  

必要なアクセス許可をアプリケーションに追加したら、設定を完了するために **管理者に同意する** を選択します。  これは、対話型の同意エクスペリエンスを必要とするのではなく、ユーザーがアプリケーションに近い位置でアクセスを許可する場合に必要です。 対話型の同意をサポートできる場合は、[Microsoft ID プラットフォームおよび OAuth 2.0 認証コード フロー](/azure/active-directory/develop/v2-oauth2-auth-code-flow) に従することをお勧めします。

## <a name="step-3-configure-public-client"></a>手順 3 パブリック クライアントの構成
ユーザーの代わりにリソースの読み取りおよび書き込みを開始するには、**パブリック クライアント** 設定を有効にする 必要 があります。  これは、Azure AD がトークン要求の本文でユーザー名とパスワードのプロパティを受け入れる唯一の方法です。  この機能を使用する予定の場合は、多要素認証が有効な勘定には使用できません。  

有効にするには、**管理 - 認証** タブに移動します。**詳細設定** セクションで、**パブリック クライアント** スイッチを **はい** に設定します。 

## <a name="step-4-request-an-access-token"></a>手順 4 アクセス トークンの要求
ユーザー名とパスワードの証しトークンを要求するには、次の手順に従います。  

### <a name="username-and-password-flow"></a>ユーザー名とパスワードのフロー
上記の [パブリック クライアント](dbmovement-api-authentication.md#step-3-configure-public-client) セクションを参照してください。  その後、POST リクエストを HTTP 経由でユーザー名とパスワードのペイロードを持った Azure AD に送信します。

```HTTP
Content-Type: application/x-www-form-urlencoded
Host: login.microsoftonline.com
Accept: application/json
POST https://login.microsoftonline.com/YOUR_TENANT.COM/oauth2/v2.0/token
BODY:
client_id={CLIENT_ID_FROM_AZURE_CLIENT_APP}&scope=https://lcsapi.lcs.dynamics.com//.default&username={USER_EMAIL_ADDRESS}&password={PASSWORD}&grant_type=password
```
前の例には、Azure Active Directory でクライアント アプリケーションから取得できるプレースホルダが含まれているとします 。  後続の Power Platform API 呼び出しに使用できる応答が返されます。

```JSON
{
  "token_type": "Bearer",
  "scope": "https://lcsapi.lcs.dynamics.com//user_impersonation https://lcsapi.lcs.dynamics.com//.default",
  "expires_in": 4228,
  "ext_expires_in": 4228,
  "access_token": "eyJ0eXAiOiJKV1Qi..."
}
```

以降の通話で **access_token** 値を、**認証** HTTP ヘッダーを持った Lifecycle Services API またはデータベース移動 API に対して使用します。

> [!NOTE]
> Lifecycle Services のローカル インスタンスや最新のクラウドを使用している場合は、スコープのパラメータに別の URL 形式が必要な場合があります。  たとえば、LCS の EU インスタンスにアクセスする場合は、スコープのパラメータ として `https://lcsapi.eu.lcs.dynamics.com//.default` を使用できます。  これは、ホスト名のために API に対する後続の呼び出しにも適用されます。

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
