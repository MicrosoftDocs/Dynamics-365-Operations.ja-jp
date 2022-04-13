---
title: 認証
description: この記事では、Microsoft Dynamics 365 Human Resources データのアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。
author: twheeloc
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f09e9f9e19c5a59918e2801f6d25f72bee090a2b
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2022
ms.locfileid: "8534192"
---
# <a name="authentication"></a>認証


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、Microsoft Dynamics 365 Human Resources データのアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。

## <a name="overview"></a>概要

人事管理のデータ API は OData 実装です。 詳細については、[データ プロトコル (OData) を開く](../fin-ops-core/dev-itpro/data-entities/odata.md) を参照してください。

API がアプリケーションからのサービス要求を処理する前に、アプリケーションは承認された呼び出し元として認証される必要があります。

## <a name="fundamentals"></a>基本

データ API を呼び出すには、アプリケーションが Microsoft ID プラットフォームからアクセス トークンを取得する必要があります。 アクセス トークンには、アプリケーションに関する情報と、人事管理のリソースを呼び出すために必要なアクセス許可が含まれています。

### <a name="access-token"></a>アクセス トークン

Microsoft ID プラットフォームにより発行されるアクセス トークンは、base64 エンコードされた JavaScript Object Notation (JSON) Web トークン (JWT) です。 これにはデータ API (および Microsoft ID プラットフォームによって保護されるその他の Web API) が呼び出し元を検証し、呼び出し元が要求している操作を実行するための適切なアクセス許可を持っていることを確認するのに使用する情報 (クレーム) が含まれています。 呼び出し中に、アクセス トークンを不透明として扱うことができます。 アクセス トークンは、常に Transport Layer Security (TLS) や Hypertext Transfer Protocol Secure (HTTPS) などのセキュリティで保護されたチャネルを介して送信する必要があります。

Microsoft ID プラットフォームによって発行されるアクセス トークンの例を次に示します。

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

データ API を呼び出すには、アクセス トークンを HTTP 要求の承認ヘッダーにベアラー トークンとして関連付けます。 次に例を示します。

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: https://{cluster}.hr.talent.dynamics.com
GET https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/JobTypes
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Azure ポータルを使用して新しいアプリケーションを登録する

1. 勤務先または学校のアカウント、または個人の Microsoft アカウントを使用して、[Microsoft Azure ポータル](https://portal.azure.com) にサインインします。

2. アカウントで複数のテナントにアクセスが許可されている場合は、右上隅でアカウントを選択し、ポータル セッションを目的の Azure Active Directory (Azure AD) テナントに設定します。

3. 左ウィンドウで、**Azure Active Directory** サービスを選択し、**アプリ登録 \> 新規登録** を選択します。

4. **アプリケーションの登録** ページが表示されたら、アプリケーションの登録情報を入力します。

    - **名前**: アプリのユーザーに表示される、意味のあるアプリケーション名を入力します。
    - **サポートされる勘定タイプ**: アプリがサポートする必要がある勘定タイプを選択します。

        | サポートされる勘定タイプ | 説明 |
        |-------------------------|-------------|
        | この組織ディレクトリのみでの勘定 | 基幹業務アプリを構築している場合は、このオプションを選択します。 このオプションは、アプリをディレクトリに登録していない限り使用できません。<p>このオプションは、**Azure AD のみの単一テナント** にマップされます。</p><p>このオプションは、アプリをディレクトリの外部に登録していない限り、既定のオプションです。 この場合、既定のオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** です。</p> |
        | 任意の組織ディレクトリでのアカウント | このオプションを選択して、すべてのビジネスおよび教育機関の顧客を対象にします。<p>このオプションは、**Azure AD のみのマルチ テナント** にマップされます。</p><p>アプリを **Azure AD のみの単一テナント** として登録した場合は、**認証** ブレードを使用して **Azure AD のみのマルチ テナント** に更新してから、**Azure AD のみの単一テナント** に戻ります。</p> |
        | 任意の組織ディレクトリおよび個人の Microsoft アカウントでのアカウント | このオプションを選択して、最も幅広い顧客を対象にします。<p>このオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** にマップされます。</p><p>アプリを **Azure AD マルチ テナントと個人の Microsoft アカウント** として登録した場合、ユーザー インターフェイス (UI) でこの設定を変更することはできません。 代わりに、アプリケーション マニフェスト エディターを使用してサポートされているアカウント タイプを変更する必要があります。</p> |

    - **リダイレクト URI (オプション)** – 構築しているアプリのタイプを選択します: **Web** または **パブリック クライアント (モバイル & デスクトップ)**。 次に、アプリのリダイレクト URI (または返信 URL) を入力します。

        - Web アプリに関しては、アプリのベース URL を指定します。 たとえば、`http://localhost:31544` はローカル コンピューターで実行する Web アプリの URL である可能性があります。 ユーザーは、この URL を使用して Web クライアント アプリにサインインします。
        - パブリック クライアント アプリに関しては、Azure AD を使用してトークン応答を返すための URI を指定します。 `myapp://auth` などの、アプリに固有の値を入力します。

        Web アプリまたはネイティブ アプリの特定の例を表示するには、[Microsoft ID プラットフォーム (旧「開発者向けAzure Active Directory」)](/azure/active-directory/develop/#quickstarts)のクイックスタートを参照してください。

5. **API アクセス許可** で、**アクセス許可の追加** を選択します。 次に、**自分の組織が使用する API** タブで **Dynamics 365 Human Resources** サービスを検索し、アプリに **user\_impersonation** のアクセス許可を追加します。 人事管理のアプリケーション ID は f9be0c49-aa22-4ec6-911a-c5da515226ff です。 この ID を使用して、正しいアプリケーションが選択されていることを確認します。

6. **登録** を選択します。

   [![Azure ポータルで新しいアプリに登録する。](media/api-new-app-registration-expanded.png)](media/api-new-app-registration-expanded.png#lightbox)

Azure AD は、アプリに固有のアプリケーション ID (クライアント ID) を割り当て、アプリの **概要** ページへと移動します。 アプリに複数の機能を追加するには、他のコンフィギュレーション オプション (ブランド化のオプションや証明書とシークレットのオプションなど) を選択できます。

## <a name="retrieving-an-access-token"></a>アクセス トークンの取得

人事管理データ API を呼び出すためのアクセス トークンを取得する方法の詳細は、クライアント アプリケーションの開発に使用しているテクノロジーによって異なります。 たとえば、[サード パーティー ユーティリティのテスト](../fin-ops-core/dev-itpro/data-entities/third-party-service-test.md) (Postman など)、C# コンソール アプリケーションや Web サービスの開発、または javascript/TypeScript クライアントのビルドを行っている場合です。

C# クライアント アプリケーションの例:
```C#
using System;
using System.Net.Http;
using System.Threading.Tasks;

// requires appropriate NuGet package references in the project
using Microsoft.IdentityModel.Clients.ActiveDirectory;

namespace TalentODataPoC
{
    class Program
    {
        // prereq: This client app must be registered in Azure Active Directory. The app must be
        // registered as requiring permission to the Dynamics 365 for Talent API (with the Dynamics
        // HCM Workload delegated permission).
        static string clientId = "4fc703ef-672c-4e2c-813f-2f9d29d726db"; // This value should be obtained from AAD and must match your registered app
        static string talentNamespaceUri = "";

        public static async Task CallTalentODataService()
        {
            // authority URI
            UriBuilder uri = new UriBuilder("https://login.microsoftonline.com/common");
            AuthenticationContext authenticationContext = new AuthenticationContext(uri.ToString());

            // request token for the resource we want to access (Human Resources). This will authenticate
            // the user and return an access token containing claims for the authenticated user.
            var authResult = await authenticationContext.AcquireTokenAsync(
                "http://hr.talent.dynamics.com", /*Talent app id or resource URI*/
                clientId, /*registered client app id*/
                new Uri("https://localhost"), /*redirect URI, as registered in your AAD app*/
                new PlatformParameters(PromptBehavior.SelectAccount));

            // create the authorization header, which needs to be passed in the Header of the HTTP Requests to Talent
            string authHeader = authResult.CreateAuthorizationHeader();

            // HINT: paste the JWT into https://jwt.ms to decode and view it
            Console.Write("authHeader: ");
            Console.WriteLine(authHeader);
            Console.WriteLine();

            HttpClient client = new HttpClient();
            client.DefaultRequestHeaders.Add("Authorization", authHeader);

            string s;

            Console.Write("Talent Namespace URI: ");
            Console.WriteLine(talentNamespaceUri);
            Console.WriteLine();

            // call the OData service to get JobType data from Talent
            var resultOdata = await client.GetAsync(talentNamespaceUri + "data/JobTypes");
            s = await resultOdata.Content.ReadAsStringAsync();
            Console.WriteLine(s);
            Console.WriteLine();
        }

        static void Main(string[] args)
        {
            Console.WriteLine();

            // if the user passes in a single parameter, assume it is the namespaceUri for Talent
            if (args.Length == 1)
            {
                talentNamespaceUri = args[0];
            } else if (args.Length == 0)
            {
                Console.WriteLine("Enter Talent URL including namespace.");
                Console.WriteLine("Example: https://aos-rts-sf-21454f9d830-prod-westus2.hr.talent.dynamics.com/namespaces/2328af1a-2d45-4c6a-99e3-12a4c3867dcf/");
                Console.Write("> ");
                talentNamespaceUri = Console.ReadLine();
                if (!talentNamespaceUri.EndsWith("/"))
                {
                    talentNamespaceUri = talentNamespaceUri + "/";
                }
            } else
            {
                Console.WriteLine("Unexpected Arguments");
                System.Environment.Exit(1);
            }

            Task t = Program.CallTalentODataService();
            t.Wait();
        }
    }
}
```

アクセス トークンを取得したら、上記のように、データ API に送信する各要求でベアラー トークンとして認証ヘッダーでトークンを渡します。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
