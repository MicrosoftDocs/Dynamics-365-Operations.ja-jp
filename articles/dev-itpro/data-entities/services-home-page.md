---
title: "サービス エンドポイント"
description: "このトピックでは、使用できるサービス エンドポイントについて説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 11/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cf531c3a8f3bdb17314d1de436b98249169f82a3
ms.openlocfilehash: c743a86cccb0de04c6f059aa1a653a684e0c23f7
ms.contentlocale: ja-jp
ms.lasthandoff: 05/22/2018

---

# <a name="service-endpoints"></a>サービス エンドポイント

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 for Finance and Operations で使用できるサービス エンドポイントについて説明します。 また、Microsoft Dynamics AX 2012 で使用できるエンドポイントと比較します。 

## <a name="list-of-services"></a>サービスのリスト
次のテーブルでは、すべてのサービス エンドポイントを一覧表示し、Finance and Operations、および AX 2012 で使用可能なエンドポイントを比較しています。

| サービス エンドポイント            | AX 2012 | Finance and Operations     |
|-----------------------------|------------------|--------------------------------|
| ドキュメント サービス (AXDs)    | 有              | いいえ – データ エンティティに置き換えられます |
| SOAP ベースのメタデータ サービス | 有              | いいえ – REST メタデータに置き換えられます |
| SOAP ベースのクエリ サービス    | 有              | いいえ – OData に置き換えられます         |
| OData クエリ サービス         | 有              | いいえ – OData に置き換えられます         |
| SOAP ベース顧客サービス   | 有              | 有                            |
| JSON ベース顧客サービス   | 無               | 有                   |
| OData サービス               | 無               | 有                   |
| REST メタデータ サービス       | 無               | 有                   |

このトピックは、サービスと、REST メタデータ サービスの認証について説明します。 次のリンクでは、以下のための詳細なドキュメントを提供します。 
- [顧客サービス](custom-services.md)
- [OData サービス](odata.md)

## <a name="authentication"></a>認証
OData サービス、JSON ベース顧客サービス、および REST メタデータ サービスは、標準の OAuth 2.0 認証をサポートします。 

現在のところ、[承認コード付与フロー](https://msdn.microsoft.com/en-us/library/azure/dn645542.aspx)と[クライアントの資格情報 (共有シークレットまたは証明書) を使用したサービス間の呼び出し](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-protocols-oauth-service-to-service)の両方をサポートしています。 

Microsoft Azure Active Directory (AAD) では、次の 2 種類のアプリケーションがサポートされています。

-   **ネイティブ クライアント アプリケーション** – このフローでは、認証と承認にユーザー名とパスワードを使用します。
-   **Web アプリケーション (機密クライアント)** – 機密クライアントとは、クライアントのパスワードを世界に対して秘密にするアプリケーションです。 承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。 

詳細については、以下を参照してください。 
- [OAuth 2.0 および Azure Active Directory を使用して web アプリケーションへのアクセスを許可する](https://msdn.microsoft.com/en-us/library/azure/dn645545.aspx)
- [サービス認証のトラブルシューティング](troubleshoot-service-authentication.md)

次の図は、認証コードの付与フローに対して認証を設定する方法について説明します。 

![認証コードの付与フロー](./media/services-authentication.png)


以下の図では、クライアントの資格情報 (共有秘密または証明書) を使用したサービス間の呼び出し承認の仕組みを説明します。

![クライアント資格情報を使用したサービス間呼び出し](./media/S2SAuth.jpg)

### <a name="register-a-native-application-with-aad"></a>AAD にネイティブ アプリケーションを登録する

クライアントがサービスと通信するには、事前に AAD に登録する必要があります。 これらの手順を使用すると、AAD でアプリケーションに登録できます。 

> [!NOTE]
> これらの手順は、組織内のすべての人が完了する必要はありません。 Azure サービスの管理者ユーザーのみがアプリケーションを追加し、その開発者とクライアント ID を共有することができます。 **前提条件:** Azure サブスクリプションと Active Directory への管理者権限が必要です。

1. Microsoft Dynamics Lifecycle Services (LCS) の適切なプロジェクトから Azure ポータルを開きます。

    ![Azure ポータルを開きます](./media/odata_azure1.png)

2. Azure ポータルの **Azure Active Directory** タブで、**プロパティ**を選択して**ディレクトリ ID** フィールドのテナント ID を記録します。 Azure Active Directory (Azure AD) 認証トークンを取得するには、後で、テナント ID が必要です。
3. **Azure Active Directory** タブで、**アプリの登録**を選択し、**新しいアプリケーションの登録**を選択します。
4. 登録している外部アプリケーションを識別する名前を入力します。 共有機密情報を使用して認証するアプリケーションについては、**Web アプリ/API** を選択します。 このコンテキストでは、サインオン URL は関係ありません。 したがって、**localhost** を使用します。
5. 新しいアプリケーションを選択し、アプリケーション ID をコピーします。 Azure AD 認証トークンを要求するには、後で、アプリケーション ID が必要です。 **必要なアクセス許可** を選択します。
6. **追加** を選択し、**API を選択** を選択します。
7. **Microsoft Dynamics ERP (Microsoft.ERP)** を選択します。 **API を選択**の検索フィールドで **Microsoft Dynamics ERP** を検索すると、グレーで表示されることがあります。その場合は、上記のように完全名で検索することを確認してください。

8. **委任アクセス権** で、少なくとも次のオプションを選択する必要があります。

    - Dynamics AX カスタム サービスへのアクセス
    - Dynamics AX データへのアクセス
    - 組織ユーザーとしての Dynamics AX オンラインへのアクセス

9. **完了** を選択します。
10. **キー** を選択します。 表示されるダイアログ ボックスで、説明を入力し、**有効期限**の値を**無期限**に設定してから**保存**を選択します。

    新しいキーを保存した後、**値**列に値が示されます。

    > [!IMPORTANT]
    > 再度、表示することはないため、必ずこの値をコピーします。OAuth 認証を完了し、Azure AD トークンを受け取るには、この秘密キーが必要になります。

### <a name="register-your-external-application-in-finance-and-operations"></a>Finance and Operations で外部のアプリケーションを登録する

1. Finance and Operations で、**システム管理** &gt; **セットアップ** &gt; **Azure Active Directory アプリケーション** に移動します。
2. **新規**を選択します。
3. 新しいレコード用のフィールドに入力します。

   - **クライアント Id** フィールドで、Azure AD に登録したアプリケーション ID を入力します。
   - **名前**フィールドに、アプリケーションの名前を入力します。
   - **ユーザー ID** フィールドで、適切なサービス アカウントのユーザー ID を選択します。 この例では、**管理者**ユーザーを選択しました。 ただし、実行する必要がある操作に対して適切なアクセス許可を持つ、専用のサービス アカウントをプロビジョニングすることをお勧めします。
    
     完了したら、**保存** を選択します。

これで、前提条件の設定を完了しました。 外部のアプリケーションが Azure AD Authentication トークンを取得した後、認証 HTTP ヘッダーのトークンを使用して、OData や SOAP などの後続のサービスの呼び出しを行うことができるようになりました。


### <a name="client-sample-code"></a>クライアント サンプル コード

次は、AAD からトークンを取得するための C# サンプル コードです。 このフローで、同意フォーム (テナント間アプリケーション用) およびサインイン フォームがユーザーに表示されます。

```
 UriBuilder uri = new UriBuilder ("https://login.windows.net/contoso2ax.onmicrosoft.com");
               
    AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

    //request token for the resource - which is the URI for your organization. NOTE: Important do not add a trailing slash at the end of the URI
    AuthenticationResult authenticationResult = authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, redirectURI);
                
    //this gets the authorization token, which needs to be passed in the Header of the HTTP Requests
    string authenticationHeader = authenticationResult.CreateAuthorizationHeader();
```

ポップアップを表示せずにユーザー名とパスワードを渡すには、**AcquireToken** の次のオーバーロードを使用します。

```
    UserCredential userCred = new UserCredential (username, password);
    authenticationContext.AcquireToken("https://axdynamics1001aos.cloud.dynamics.com", clientId, userCred);
```

## <a name="rest-metadata-service"></a>REST メタデータ サービス
REST メタデータ サービスは、読み取り専用サービスです。 つまり、ユーザーは GET 要求のみ生成できます。 このエンドポイントの主な目的は、要素のメタデータ情報を提供することです。 OData 実装です。 

このエンドポイントは、`http://\[baseURI\]/Metadata` でホストされています。

現在、このエンドポイントは、次の要素のメタデータを提供します。

-   **ラベル** – システムからラベルを返します。 ラベルには言語と ID のデュアル ペア キーがあり、ラベルの値を取得できます。 

    **例:** `https://[baseURI\]/metadata/Labels(Id='@SVC\_ODataLabelFile:Label1',Language='en-us')`

-   **データ エンティティ** - システム内のすべてのデータ エンティティの JSON 形式の一覧を返します。 

    **例:** `https://[baseURI\]/Metadata/DataEntities`

