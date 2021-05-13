---
title: データベース移動 API - 認証
description: このトピックでは、データベース移動のアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。
author: laneswenka
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: c9e610f203c120f841b5929c28c3e1def6381a85
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5940896"
---
# <a name="database-movement-api---authentication"></a>データベース移動 API - 認証

[!include [banner](../../includes/banner.md)]

このトピックでは、データベース移動のアプリケーション プログラミング インターフェイス (API) を使用した認証方法についての概要を示します。

## <a name="fundamentals"></a>基本

データベース移動 API を呼び出すには、アプリケーションが Microsoft ID プラットフォームからアクセス トークンを取得する必要があります。 アクセス トークンには、アプリケーションに関する情報と、Microsoft Dynamics Lifecycle Services (LCS) のリソースを呼び出すために必要なアクセス許可が含まれています。

### <a name="access-token"></a>アクセス トークン

Microsoft ID プラットフォームにより発行されるアクセス トークンは、base64 エンコードされた JavaScript Object Notation (JSON) Web トークン (JWT) です。 これにはデータベース移動 API および Microsoft ID プラットフォームによって保護されるその他の Web API が呼び出し元を検証し、呼び出し元が要求している操作を実行するための適切なアクセス許可を持っていることを確認するのに使用する情報 (クレーム) が含まれています。 呼び出し中に、アクセス トークンを不透明として扱うことができます。 アクセス トークンは、常に Transport Layer Security (TLS) や Hypertext Transfer Protocol Secure (HTTPS) などのセキュリティで保護されたチャネルを介して送信する必要があります。

Microsoft ID プラットフォームによって発行されるアクセス トークンの例を次に示します。

```jwt
EwAoA8l6BAAU7p9QDpi/D7xJLwsTgCg3TskyTaQAAXu71AU9f4aS4rOK5xoO/SU5HZKSXtCsDe0Pj7uSc5Ug008qTI+a9M1tBeKoTs7tHzhJNSKgk7pm5e8d3oGWXX5shyOG3cKSqgfwuNDnmmPDNDivwmi9kmKqWIC9OQRf8InpYXH7NdUYNwN+jljffvNTewdZz42VPrvqoMH7hSxiG7A1h8leOv4F3Ek/oeJX6U8nnL9nJ5pHLVuPWD0aNnTPTJD8Y4oQTp5zLhDIIfaJCaGcQperULVF7K6yX8MhHxIBwek418rKIp11om0SWBXOYSGOM0rNNN59qNiKwLNK+MPUf7ObcRBN5I5vg8jB7IMoz66jrNmT2uiWCyI8MmYDZgAACPoaZ9REyqke+AE1/x1ZX0w7OamUexKF8YGZiw+cDpT/BP1GsONnwI4a8M7HsBtDgZPRd6/Hfqlq3HE2xLuhYX8bAc1MUr0gP9KuH6HDQNlIV4KaRZWxyRo1wmKHOF5G5wTHrtxg8tnXylMc1PKOtaXIU4JJZ1l4x/7FwhPmg9M86PBPWr5zwUj2CVXC7wWlL/6M89Mlh8yXESMO3AIuAmEMKjqauPrgi9hAdI2oqnLZWCRL9gcHBida1y0DTXQhcwMv1ORrk65VFHtVgYAegrxu3NDoJiDyVaPZxDwTYRGjPII3va8GALAMVy5xou2ikzRvJjW7Gm3XoaqJCTCExN4m5i/Dqc81Gr4uT7OaeypYTUjnwCh7aMhsOTDJehefzjXhlkn//2eik+NivKx/BTJBEdT6MR97Wh/ns/VcK7QTmbjwbU2cwLngT7Ylq+uzhx54R9JMaSLhnw+/nIrcVkG77Hi3neShKeZmnl5DC9PuwIbtNvVge3Q+V0ws2zsL3z7ndz4tTMYFdvR/XbrnbEErTDLWrV6Lc3JHQMs0bYUyTBg5dThwCiuZ1evaT6BlMMLuSCVxdBGzXTBcvGwihFzZbyNoX+52DS5x+RbIEvd6KWOpQ6Ni+1GAawHDdNUiQTQFXRxLSHfc9fh7hE4qcD7PqHGsykYj7A0XqHCjbKKgWSkcAg==
```

データベース移動 API を呼び出すには、アクセス トークンを HTTP 要求の承認ヘッダーにベアラー トークンとして関連付けます。 次に例を示します。

```HTTP
HTTP/1.1
Authorization: Bearer EwAoA8l6BAAU ... 7PqHGsykYj7A0XqHCjbKKgWSkcAg==
Host: lcsapi.lcs.dynamics.com
GET https://lcsapi.lcs.dynamics.com/databasemovement/v1/databases
```

## <a name="register-a-new-application-by-using-the-azure-portal"></a>Azure ポータルを使用して新しいアプリケーションを登録する

1. 勤務先または学校アカウント、または Microsoft アカウントを使用して、[Microsoft Azure ポータル](https://portal.azure.com) にサインインします。
2. アカウントで複数のテナントにアクセスが許可されている場合は、右上隅でアカウントを選択し、ポータル セッションを目的の Azure Active Directory (Azure AD) テナントに設定します。
3. 左ウィンドウで、**Azure Active Directory** サービスを選択し、**アプリ登録 \> 新規登録** を選択します。
4. **アプリケーションの登録** ページが表示されたら、アプリケーションの登録情報を入力します。

    - **名前** – アプリのユーザーに表示される、意味のあるアプリケーション名を入力します。
    - **サポートされる勘定タイプ** – アプリがサポートする必要がある勘定タイプを選択します。

        | サポートされる勘定タイプ | 説明 |
        |-------------------------|-------------|
        | この組織ディレクトリのみでの勘定 | 基幹業務アプリを構築している場合は、このオプションを選択します。 このオプションは、アプリをディレクトリに登録していない限り使用できません。<p>このオプションは、**Azure AD のみの単一テナント** にマップされます。</p><p>このオプションは、アプリをディレクトリの外部に登録していない限り、既定のオプションです。 この場合、既定のオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** です。</p> |
        | 任意の組織ディレクトリでのアカウント | このオプションを選択して、すべてのビジネスおよび教育機関の顧客を対象にします。<p>このオプションは、**Azure AD のみのマルチ テナント** にマップされます。</p><p>アプリを **Azure AD のみの単一テナント** として登録した場合は、**認証** ブレードを使用して **Azure AD のみのマルチ テナント** に更新してから、**Azure AD のみの単一テナント** に戻ります。</p> |
        | 任意の組織ディレクトリおよび個人の Microsoft アカウントでのアカウント | このオプションを選択して、最も幅広い顧客を対象にします。<p>このオプションは **Azure AD マルチ テナントと個人の Microsoft アカウント** にマップされます。</p><p>アプリを **Azure AD マルチ テナントと個人の Microsoft アカウント** として登録した場合、ユーザー インターフェイス (UI) でこの設定を変更することはできません。 代わりに、アプリケーション マニフェスト エディターを使用してサポートされているアカウント タイプを変更する必要があります。</p> |

    - **リダイレクト URI (オプション)** – 構築しているアプリのタイプを選択します: **Web** または **パブリック クライアント (モバイル & デスクトップ)**。 次に、アプリのリダイレクト URI (または返信 URL) を入力します。

        - Web アプリに関しては、アプリのベース URL を指定します。 たとえば、`http://localhost:31544` はローカル コンピューターで実行する Web アプリの URL である可能性があります。 ユーザーは、この URL を使用して Web クライアント アプリにサインインします。
        - パブリック クライアント アプリに関しては、Azure AD を使用してトークン応答を返すための URI を指定します。 `myapp://auth` などの、アプリに固有の値を入力します。

        Web アプリまたはネイティブ アプリの特定の例を表示するには、[Azure AD からのクイック スタート ガイド](/azure/active-directory/develop/#quickstarts) を参照してください。

5. **API アクセス許可** で、**アクセス許可の追加** を選択します。 次に、**自分の組織が使用する API** タブで、**Dynamics Lifecycle services** サービスを検索し、アプリに **ユーザー\_偽装** のアクセス許可を追加します。
6. **登録** を選択します。

[![Azure ポータルで新しいアプリに登録する](../media/new-app-registration-expanded.png)](../media/new-app-registration-expanded.png#lightbox)

Azure AD は、アプリに固有のアプリケーション ID (クライアント ID) を割り当て、アプリの **概要** ページが表示されます。 アプリに複数の機能を追加するには、他のコンフィギュレーション オプション (ブランド化のオプションや証明書とシークレットのオプションなど) を選択できます。


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]