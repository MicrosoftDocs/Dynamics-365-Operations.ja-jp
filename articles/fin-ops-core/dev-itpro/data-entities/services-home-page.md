---
title: サービス エンドポイント 概要
description: このトピックでは、使用できるサービス エンドポイントについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f76298d621e3d74dfbf1ad85b43b4e2b97fe27e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685235"
---
# <a name="service-endpoints-overview"></a>サービス エンドポイント 概要

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Finance で使用できるサービス エンドポイントについて説明します。 また、Microsoft Dynamics AX 2012 で使用できるエンドポイントと比較します。

## <a name="list-of-services"></a>サービスのリスト
次のテーブルでは、すべてのサービス エンドポイントを一覧表示し、アプリケーション、および AX 2012 で使用可能なエンドポイントを比較しています。

| サービス エンドポイント            | AX 2012 | Finance and Operations         |
|-----------------------------|---------|--------------------------------|
| ドキュメント サービス (AXDs)    | はい     | いいえ – データ エンティティに置き換えられます |
| SOAP ベースのメタデータ サービス | 有     | いいえ – REST メタデータに置き換えられます |
| SOAP ベースのクエリ サービス    | 有     | いいえ – OData に置き換えられます         |
| OData クエリ サービス         | 有     | いいえ – OData に置き換えられます         |
| SOAP ベース カスタム サービス   | 有     | 有                            |
| JSON ベース カスタム サービス   | 無      | 有                            |
| OData サービス               | 無      | 有                            |
| REST メタデータ サービス       | 無      | 有                            |

このトピックは、サービスと、REST メタデータ サービスの認証について説明します。 次のリンクでは、以下のための詳細なドキュメントを提供します。

- [カスタム サービスの開発](custom-services.md)
- [データ プロトコル (OData) を開く](odata.md)

## <a name="authentication"></a>認証
OData サービス、JSON ベース カスタム サービス、および REST メタデータ サービスは、標準の OAuth 2.0 認証をサポートします。

現在のところ、[承認コード付与フロー](https://msdn.microsoft.com/library/azure/dn645542.aspx)と[クライアントの資格情報 (共有シークレットまたは証明書) を使用したサービス間の呼び出し](https://docs.microsoft.com/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service)の両方をサポートしています。

Microsoft Azure Active Directory (AAD) では、次の 2 種類のアプリケーションがサポートされています。

- **ネイティブ クライアント アプリケーション** – このフローでは、認証と承認にユーザー名とパスワードを使用します。
- **Web アプリケーション (機密クライアント)** – 機密クライアントとは、クライアントのパスワードを世界に対して秘密にするアプリケーションです。 承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。

詳細については、以下を参照してください。

- [OAuth 2.0 および Azure Active Directory を使用して web アプリケーションへのアクセスを許可する](https://msdn.microsoft.com/library/azure/dn645545.aspx)
- [サービス認証問題のトラブルシューティング](troubleshoot-service-authentication.md)

次の図は、認証コードの付与フローに対して認証を設定する方法について説明します。

![認証コードの付与フロー](./media/services-authentication.png)

以下の図では、クライアントの資格情報 (共有秘密または証明書) を使用したサービス間の呼び出し承認の仕組みを説明します。

![クライアントの資格情報を使用したサービス間呼び出し](./media/S2SAuth.jpg)

### <a name="register-a-web-application-with-aad"></a>AAD に Web アプリケーションを登録する

> [!NOTE]
> これらの手順は、組織内のすべての人が完了する必要はありません。 Azure サービスの管理者ユーザーのみがアプリケーションを追加し、その開発者とクライアント ID を共有することができます。

**前提条件:** Azure サブスクリプションと Azure Active Directory (Azure AD) への管理者権限が必要です。

クライアントがサービスと通信する前に、(Azure AD) に登録する必要があります。 これらの手順を使用すると、(Azure AD) でアプリケーションに登録できます。 この手順については、[Azure アプリ登録のトレーニングガイド](https://docs.microsoft.com/azure/active-directory/develop/app-registrations-training-guide-for-app-registrations-legacy-users)を参照してください。 このプロセスでの固有の構成には、コンテキストで次の追加情報を使用する必要があります。

**Microsoft DynamicsERP (Microsoft.ERP)** を選択します。 **API を選択** 内の検索フィールドで **Microsoft Dynamics ERP** を検索する場合、使用できないように見えることがあります。 その場合は、上に示したようにフルネームを検索してください。
**委任アクセス権** で、少なくとも次のオプションを選択する必要があります。

- Dynamics AX カスタム サービスへのアクセス
- Dynamics AX データへのアクセス
- 組織ユーザーとしての Dynamics AX オンラインへのアクセス

 > [!IMPORTANT]
 > このキーは再度表示されないため、コピーしてください。 OAuth 認証を完了して Azure AD トークンを受け取るには、この秘密のキーを知っておく必要があります。

### <a name="register-your-external-application"></a>外部アプリケーションの登録 

1. Finance and Operations アプリで、**システム管理** \> **設定** \> **Azure Active Directory アプリケーション** の順に移動します。
2. **新規** を選択します。
3. 新しいレコード用のフィールドに入力します。

    - **クライアント ID** フィールドで、Azure AD に登録したアプリケーション ID を入力します。
    - **名前** フィールドに、アプリケーションの名前を入力します。
    - **ユーザー ID** フィールドで、適切なサービス アカウントのユーザー ID を選択します。 この例では、**管理者** ユーザーを選択しました。 ただし、実行する必要がある操作に対して適切なアクセス許可を持つ、専用のサービス アカウントをプロビジョニングすることをお勧めします。

    完了したら、**保存** を選択します。

これで、前提条件の設定を完了しました。 外部のアプリケーションが Azure AD Authentication トークンを取得した後、認証 HTTP ヘッダーのトークンを使用して、OData や SOAP などの後続のサービスの呼び出しを行うことができるようになりました。

### <a name="client-sample-code"></a>クライアント サンプル コード

次は、AAD からトークンを取得するための C\# サンプル コードです。 このフローで、同意フォーム (テナント間アプリケーション用) およびサインイン フォームがユーザーに表示されます。

```csharp
UriBuilder uri = new UriBuilder ("https://login.windows.net/contoso2ax.onmicrosoft.com");

AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

//request token for the resource - which is the URI for your organization. NOTE: Important do not add a trailing slash at the end of the URI
AuthenticationResult authenticationResult = authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, redirectURI);

//this gets the authorization token, which needs to be passed in the Header of the HTTP Requests
string authenticationHeader = authenticationResult.CreateAuthorizationHeader();
```

ポップアップを表示せずにユーザー名とパスワードを渡すには、**AcquireToken** の次のオーバーロードを使用します。

```csharp
UserCredential userCred = new UserCredential (username, password);
authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, userCred);
```

## <a name="rest-metadata-service"></a>REST メタデータ サービス
REST メタデータ サービスは、読み取り専用サービスです。 つまり、ユーザーは GET 要求のみ生成できます。 このエンドポイントの主な目的は、要素のメタデータ情報を提供することです。 OData 実装です。

このエンドポイントは、`http://\[baseURI\]/Metadata` でホストされています。

現在、このエンドポイントは、次の要素のメタデータを提供します。

- **ラベル** – システムからラベルを返します。 ラベルには言語と ID のデュアル ペア キーがあり、ラベルの値を取得できます。

    **例:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`

- **データ エンティティ** - システム内のすべてのデータ エンティティの JSON 形式の一覧を返します。

    **例:** `https://[baseURI\]/Metadata/DataEntities`


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]