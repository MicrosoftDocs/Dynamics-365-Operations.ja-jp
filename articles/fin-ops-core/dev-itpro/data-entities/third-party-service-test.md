---
title: サード パーティ ユーティリティを使用したテスト サービス
description: このトピックでは、サービスをテストするサード パーティのユーティリティを設定する方法について説明します。
author: peakerbl
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24841
ms.assetid: 7137b0a0-1473-4134-b769-ede5e07fd6f5
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab26c16984f24e75ce603543bd4ad7ce3257dfe7
ms.sourcegitcommit: 7aa7d756e1e98a53da62e03c608a9597ef9893ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2021
ms.locfileid: "7404188"
---
# <a name="test-services-by-using-third-party-utilities"></a>サード パーティ ユーティリティを使用したテスト サービス

[!include [banner](../includes/banner.md)]

<https://github.com/Microsoft/Dynamics-AX-Integration> で、Microsoft はサービスを使用するためのサンプル コードを提供します。 ただし、統合でのその他のエンドポイントは Microsoft スタックを使用しない可能性があるという多くのシナリオがあります。 他のエンドポイントが、たとえば Microsoft が利用できるオープン データ プロトコル (OData) クライアント コードを使用している場合でも、次の操作を実行すると便利です。

- インタラクションのメッセージがどのように構築されているかを調べ、分析します。
- 既知の要求へのサービスの応答をテストします。
- 他のエンドポイントに例外がどのように表示されるかを決定します。

頻繁に使用される多くのツールを使用でき、これらのアクションを実行するのに役立ちます。 このトピックでは、どんなツールも推奨しません。 頻繁に使用されるいくつかのソフトウェア ユーティリティの使用例を示していますが、原則は他の同様のツールに広く適用されるべきです。

## <a name="prerequisites"></a>前提条件

外部アプリケーションを使用してサービスをテストする前に、Microsoft Azure、および Finance and Operations にアプリケーションを登録する必要があります。

詳細については、以下を参照してください。

- [AAD にアプリケーションを登録する](services-home-page.md#register-a-web-application-with-aad)
- [外部アプリケーションの登録](services-home-page.md#register-your-external-application)

## <a name="query-odata-by-using-postman"></a>Postman を使用した OData のクエリ

Postman (<https://www.getpostman.com/postman>) は、アプリケーション プログラミング インターフェイス (API) の開発とテストが関係するシナリオで RESTful サービス (OData など) の操作によく使用されるツールです。 このステップは Postman の推奨ではなく、他の類似のツールも利用できます。 ただし、Azure AD で認証する OAuth を使用する際に含まれる概念およびメッセージについて説明し、OData 要求を作成し、アプリケーションからの応答を受け取るのに Postman を使用しています。

1. Postman を起動します。
2. 右上隅にある歯車ボタンを選択してから、**環境の管理** を選択して環境を作成または更新します。
3. 環境名を入力し、**一括編集** をクリックします。
4. 次の表に示すとおり、キーと値のペアを入力します。 行ごとに 1 つのペアを入力し、コロン (:) を使用してキーと値を区切ります。

    | キー            | 先頭値                                                                                               |
    |----------------|-----------------------------------------------------------------------------------------------------|
    | tenant\_id     | 前提条件のセットアップ中に参照した Azure テナント ID                            |
    | client\_id     | 前提条件のセットアップ中に登録した Azure AD アプリケーション ID                   |
    | client\_secret | 前提条件の設定中のアプリケーション登録中に生成した秘密キー |
    | grant\_type    | client\_credentials                                                                                 |
    | リソース       | 末尾の '/' を除いたインスタンスのベース URL                                                 |

5. キーと値のペアが正しく解析できることを確認するには、**キー-値の編集** を選択し、結果を確認します。
6. 環境ページを閉じます。
7. 歯車と目のボタンの左側にあるフィールドで、新しいまたは更新した環境を選択します。
8. Azure AD トークンを取得するには、`https://login.microsoftonline.com/[tenant ID]/oauth2/token` の形式の URL を持つ POST 要求を作成します。

    `https://login.microsoftonline.com/:tenant_id/oauth2/token` などの、**tenant\_id** 環境変数を参照する URL パラメーターを使用することができます。

    ![Azure AD トークンを取得します。](./media/postman6.png)

9. **本文** タブで、前に作成した環境変数を参照する要求パラメーターとして、本文要素を追加します。 **一括編集** を選択して、上記の表のキーを入力し、コロン (:) を入力してからキーの名前を再入力しますが、二重中かっこ ({{}}) で囲みます。 行ごとに 1 つの要求パラメーターを入力します。 たとえば、**交付\_タイプ:{{交付\_タイプ}}** を入力します。 次に例を示します。

    ![本文要素。](./media/postman8.png)

10. **テスト** タブで、応答が妥当であることを検証し、環境変数で返される認証トークンを格納するテストを作成します。 次に例を示します。

    ```csharp
    var json = JSON.parse(responseBody);
    tests["Get Azure AD Token"] = !json.error && responseBody !== '' && responseBody !== '{}' && json.access_token !== '';
    postman.setEnvironmentVariable("bearerToken", json.access_token);
    ```

11. **保存** を選択し、要求の名前とコレクションを入力して、**保存** を再度選択します。
12. **送信** を選択して承認要求を行います。 **本文** タブには、その他の応答の詳細と共に、Azure AD トークンが含まれるようになりました。

    ![Azure AD トークン。](./media/postman11.png)

13. テスト コードのため、トークンは環境変数にあります。 **環境クイック表示** ボタン (目のボタン) を選択すると、トークンが環境変数であることがわかります。

    ![環境クイック表示。](./media/postman12.png)

14. OData サービスを介して、目的のデータ エンティティに対して作成、読み取り、更新、または削除 (CRUD) 操作を実行する要求を作成します。 必要に応じて URL を作成します。 詳細については、[データ プロトコル (OData) を開く](odata.md) を参照してください。 前に示したように、環境に格納されている変数を使用して、要求をパラメーター化することが便利であることがわかる場合があります。 次の GET クエリの例では、**Customer Account** パラメーターが使用されています。 クエリは、環境変数で指定された顧客アカウントの名前とアドレスの詳細を返します。 特殊文字は、URL に正しくエンコードされる必要があることに注意してください。

    ```Console
    https://[Finance and Operations instance URL]/data/Customers?$format=json&$filter=CustomerAccount%20eq%20%27{{custAccount}}%27&$select=CustomerAccount,Name,AddressDescription,FullPrimaryAddress
    ```

15. 以前に取得され、**bearerToken** 環境変数に格納された認証トークンを参照する認証ヘッダーを追加します。 トークンは、ヘッダーの先頭に **Bearer** を付ける必要があります。

    ![ベアラー トークン。](./media/postman13.png)

16. 応答を検証するためのテストを作成します。 次の例では、空でない JSON 形式のデータが応答本文に返されるかどうかをテストします。

    ```csharp
    var json = JSON.parse(responseBody);
    tests["Get customer info"] = !json.error && responseBody !== '' && responseBody !== '{}';
    ```

17. 要求を保存および送信し、結果を確認します。 使用するユーザー アカウントが、データを持つ既定の会社に対して設定されていることを確認する必要があります。 または、OData 要求のクエリ パラメーターとして、クロス会社 =true を指定することもできます。

    ![結果。](./media/postman15.png)

ここでは、正常に認証されてから、OData サービスを使用して、顧客レコードを読み取っています。

## <a name="query-the-soap-custom-service-in-your-application-by-using-soapui"></a>SoapUI を使用して、アプリケーションで SOAP カスタム サービスのクエリを実行

SoapUI (<https://www.soapui.org/>) は、API の開発とテストが関係するシナリオで SOAP および REST Web サービスを操作するために多くの場合使用されるツールです。 このステップは SoapUI を推奨するものではなく、他の類似のツールも使用できます。 ただし、Azure AD で認証する OAuth を使用する際に含まれる概念およびメッセージについて説明するのに SoapUI を使用しており、SOAP 要求を作成して応答を受け取ることができます。

1. SoapUI を起動し、**SOAP** ボタンを選択してプロジェクトを作成します。
2. プロジェクトの情報を記入してください:

    - **プロジェクト名** フィールドに、プロジェクトの名前を入力します。
    - **初期 WSDL** フィールドに、サービス アドレスを入力し、接尾語 **?wsdl** を追加します。 (サービスの住所は \[Finance and Operations インスタンスのベース URL\]/soap/services/ \[サービス グループ名\] の形式である必要があります。) 詳細については、[サービスのホーム ページ](services-home-page.md) を参照してください。

        たとえば、URL `https://[Finance and Operations base URL]/soap/services/UserSessionService?wsdl` でユーザー セッション サービスについて問い合わせます。

    - **すべての工程でサンプル依頼を作成しますか?** チェック ボックスをオンにします。

        サンプル要求の作成を選択したため、利用可能なサービス操作ごとに 1 つのサンプル要求が作成されます。

        ![サンプル要求。](./media/soapui3.png)

3. 新しいプロジェクトを右クリックし、**新しいテスト スイート** を選択してテスト スイートを作成します。 このテスト スイートは、Azure AD 認証トークンに対する POST 要求を生成します。
4. テスト スイートを右クリックし、**新しいテスト ケース** を選択します。
5. テスト ケースを展開し、**テスト ステップ** を右クリックして **ステップの追加** を選び、次に **HTTP 要求** を選択します。
6. 要求名を入力し、**OK** を選択します。
7. テスト ステップ名を入力します。 POST 要求に使用する必要のあるエンドポイントは、`[https://login.microsoftonline.com/[tenant_id]/oauth2/token](https://login.microsoftonline.com/%5btenant_id%5d/oauth2/token)` です。
8. **パラメーター** の横にある [プラス記号 (**+**)] ボタンを使用して、次の値を追加します。

    | パラメーター      | 先頭値                                                           |
    |----------------|-----------------------------------------------------------------|
    | grant\_type    | client\_credentials                                             |
    | client\_id     | Azure AD アプリケーション登録のアプリケーション ID   |
    | client\_secret | Azure AD アプリケーション登録の秘密キーの値 |
    | リソース       | 末尾の '/' を除いたインスタンスの URL                 |

9. パラメーターが POST 本体にあることを確認するには、**Post QueryString** を選択し、**再生** を選択します。 アクセス トークンは応答ウィンドウに戻す必要があります。 **JSON 応答** タブを使用すると、値が最も読みやすくなります。アクセス トークンをコピーして、後続の要求の認証ヘッダーで使用できるようにします。
10. **GetUserSessionInfo** SOAP サンプル要求で、最初の要求ノードに戻ります。 左側の要求ウィンドウで、プラス記号 (**+**) ボタンを選択して、**認証** というヘッダーを追加します。 アクセストークンを **Value** フィールドに貼り付け、プレフィックス **Bearer** を追加します。
11. SoapUI が作成するサンプル リクエストは、変更しない限り動作しません。 行なおうとしていることのスキーマに対応できるように、呼び出しコンテキストと本文を編集する必要があります。

    単純なシナリオでは、null 値になるように、オプションの呼び出しコンテキスト要素を編集できます。 開始タグで大なり記号 (&gt;) の前にフォワード スラッシュ (/) を挿入します。 コメントの開始と終了を区切るには、標準の &lt;!--...--&gt; 構文を使用して疑問符 (?) と終了タグをコメント アウトします。 (疑問符は XML スキーマの有効なコンテンツではありません。) または、疑問符 (?) を削除して、コンテキスト要素が空になるようにすることもできます。

12. SOAP 要求の準備が整いました。 **再生** を選択し、右側の結果を検証します。

    ![結果を検証します。](./media/soapui8.png)

ここでは、正常に認証されてから、SOAP を介して UserSessionService を照会しています。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
