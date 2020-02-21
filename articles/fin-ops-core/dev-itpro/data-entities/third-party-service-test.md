---
title: サード パーティ ユーティリティを使用したテスト サービス
description: このトピックでは、サービスをテストするサード パーティのユーティリティを設定する方法について説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 24841
ms.assetid: 7137b0a0-1473-4134-b769-ede5e07fd6f5
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b4a1067e7f0457632b0fafa149a4e0104f89afe
ms.sourcegitcommit: 9f90b194c0fc751d866d3d24d57ecf1b3c5053a1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/07/2020
ms.locfileid: "3033006"
---
# <a name="test-services-by-using-third-party-utilities"></a><span data-ttu-id="5cc6a-103">サード パーティ ユーティリティを使用したテスト サービス</span><span class="sxs-lookup"><span data-stu-id="5cc6a-103">Test services by using third-party utilities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cc6a-104"><https://github.com/Microsoft/Dynamics-AX-Integration> で、Microsoft はサービスを使用するためのサンプル コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-104">At <https://github.com/Microsoft/Dynamics-AX-Integration>, Microsoft provides sample code for consuming services.</span></span> <span data-ttu-id="5cc6a-105">ただし、統合でのその他のエンドポイントは Microsoft スタックを使用しない可能性があるという多くのシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-105">However, there are many scenarios where the other endpoint in an integration might not use a Microsoft stack.</span></span> <span data-ttu-id="5cc6a-106">他のエンドポイントが、たとえば Microsoft が利用できるオープン データ プロトコル (OData) クライアント コードを使用している場合でも、次の操作を実行すると便利です。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-106">Even when the other endpoint does use, for example, the Open Data Protocol (OData) client code that Microsoft makes available, you might find it useful to perform the following actions:</span></span>

- <span data-ttu-id="5cc6a-107">インタラクションのメッセージがどのように構築されているかを調べ、分析します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-107">Explore and analyze how an interaction's messages are constructed.</span></span>
- <span data-ttu-id="5cc6a-108">既知の要求へのサービスの応答をテストします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-108">Test the response of a service to a well-known request.</span></span>
- <span data-ttu-id="5cc6a-109">他のエンドポイントに例外がどのように表示されるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-109">Determine how exceptions will appear to the other endpoint.</span></span>

<span data-ttu-id="5cc6a-110">頻繁に使用される多くのツールを使用でき、これらのアクションを実行するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-110">Many frequently used tools that will help you perform these actions are available.</span></span> <span data-ttu-id="5cc6a-111">このトピックでは、どんなツールも推奨しません。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-111">This topic isn't an endorsement of any tool.</span></span> <span data-ttu-id="5cc6a-112">頻繁に使用されるいくつかのソフトウェア ユーティリティの使用例を示していますが、原則は他の同様のツールに広く適用されるべきです。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-112">Although it provides examples that use some frequently used software utilities, the principles should broadly apply to other, similar tools.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5cc6a-113">前提条件</span><span class="sxs-lookup"><span data-stu-id="5cc6a-113">Prerequisites</span></span>

<span data-ttu-id="5cc6a-114">外部アプリケーションを使用してサービスをテストする前に、Microsoft Azure、および Finance and Operations にアプリケーションを登録する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-114">Before you can test a service by using an external application, you must register the application in Microsoft Azure, and in Finance and Operations.</span></span>

<span data-ttu-id="5cc6a-115">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-115">For details, see:</span></span>

- [<span data-ttu-id="5cc6a-116">AAD にアプリケーションを登録する</span><span class="sxs-lookup"><span data-stu-id="5cc6a-116">Register an application with AAD</span></span>](services-home-page.md#register-a-web-application-with-aad)
- [<span data-ttu-id="5cc6a-117">外部アプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="5cc6a-117">Register your external application</span></span>](services-home-page.md#register-your-external-application)

## <a name="query-odata-by-using-postman"></a><span data-ttu-id="5cc6a-118">Postman を使用した OData のクエリ</span><span class="sxs-lookup"><span data-stu-id="5cc6a-118">Query OData by using Postman</span></span>

<span data-ttu-id="5cc6a-119">Postman (<https://www.getpostman.com/postman>) は、アプリケーション プログラミング インターフェイス (API) の開発とテストが関係するシナリオで RESTful サービス (OData など) の操作によく使用されるツールです。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-119">Postman (<https://www.getpostman.com/postman>) is a tool that is often used to interact with RESTful services (such as OData) in scenarios that involve the development and testing of application programming interfaces (APIs).</span></span> <span data-ttu-id="5cc6a-120">このステップは Postman の推奨ではなく、他の類似のツールも利用できます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-120">This procedure isn't an endorsement of Postman, and other similar tools are available.</span></span> <span data-ttu-id="5cc6a-121">ただし、Azure AD で認証する OAuth を使用する際に含まれる概念およびメッセージについて説明し、OData 要求を作成し、アプリケーションからの応答を受け取るのに Postman を使用しています。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-121">However, we are using Postman to illustrate the concepts and messages that are involved when you use OAuth to authenticate with Azure AD, and then make OData requests to and receive responses from the application.</span></span>

1. <span data-ttu-id="5cc6a-122">Postman を起動します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-122">Start Postman.</span></span>
2. <span data-ttu-id="5cc6a-123">右上隅にある歯車ボタンを選択してから、**環境の管理**を選択して環境を作成または更新します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-123">In the upper-right corner, select the gear button, and then select **Manage environments** to create or update an environment.</span></span>
3. <span data-ttu-id="5cc6a-124">環境名を入力し、**一括編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-124">Enter a name for the environment, and then select **Bulk Edit**.</span></span>
4. <span data-ttu-id="5cc6a-125">次の表に示すとおり、キーと値のペアを入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-125">Enter key-value pairs as shown in the following table.</span></span> <span data-ttu-id="5cc6a-126">行ごとに 1 つのペアを入力し、コロン (:) を使用してキーと値を区切ります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-126">Enter one pair per line, and separate the key and value by using a colon (:).</span></span>

    | <span data-ttu-id="5cc6a-127">キー</span><span class="sxs-lookup"><span data-stu-id="5cc6a-127">Key</span></span>            | <span data-ttu-id="5cc6a-128">先頭値</span><span class="sxs-lookup"><span data-stu-id="5cc6a-128">Value</span></span>                                                                                               |
    |----------------|-----------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="5cc6a-129">tenant\_id</span><span class="sxs-lookup"><span data-stu-id="5cc6a-129">tenant\_id</span></span>     | <span data-ttu-id="5cc6a-130">前提条件のセットアップ中に参照した Azure テナント ID</span><span class="sxs-lookup"><span data-stu-id="5cc6a-130">The Azure tenant ID that you looked up during the setup of prerequisites</span></span>                            |
    | <span data-ttu-id="5cc6a-131">client\_id</span><span class="sxs-lookup"><span data-stu-id="5cc6a-131">client\_id</span></span>     | <span data-ttu-id="5cc6a-132">前提条件のセットアップ中に登録した Azure AD アプリケーション ID</span><span class="sxs-lookup"><span data-stu-id="5cc6a-132">The Azure AD application ID that you registered during the setup of prerequisites</span></span>                   |
    | <span data-ttu-id="5cc6a-133">client\_secret</span><span class="sxs-lookup"><span data-stu-id="5cc6a-133">client\_secret</span></span> | <span data-ttu-id="5cc6a-134">前提条件の設定中のアプリケーション登録中に生成した秘密キー</span><span class="sxs-lookup"><span data-stu-id="5cc6a-134">The secret key that you generated during application registration during the setup of prerequisites</span></span> |
    | <span data-ttu-id="5cc6a-135">grant\_type</span><span class="sxs-lookup"><span data-stu-id="5cc6a-135">grant\_type</span></span>    | <span data-ttu-id="5cc6a-136">client\_credentials</span><span class="sxs-lookup"><span data-stu-id="5cc6a-136">client\_credentials</span></span>                                                                                 |
    | <span data-ttu-id="5cc6a-137">リソース</span><span class="sxs-lookup"><span data-stu-id="5cc6a-137">resource</span></span>       | <span data-ttu-id="5cc6a-138">末尾の '/' を除いたインスタンスのベース URL</span><span class="sxs-lookup"><span data-stu-id="5cc6a-138">The base URL of the instance without the trailing '/'</span></span>                                                 |

5. <span data-ttu-id="5cc6a-139">キーと値のペアが正しく解析できることを確認するには、**キー-値の編集** を選択し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-139">To verify that the key-value pairs can be parsed correctly, select **Key-Value Edit**, and review the results.</span></span>
6. <span data-ttu-id="5cc6a-140">環境ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-140">Close the environment page.</span></span>
7. <span data-ttu-id="5cc6a-141">歯車と目のボタンの左側にあるフィールドで、新しいまたは更新した環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-141">In the field to the left of the gear and eye buttons, select the new or updated environment.</span></span>
8. <span data-ttu-id="5cc6a-142">Azure AD トークンを取得するには、`https://login.microsoftonline.com/[tenant ID]/oauth2/token` の形式の URL を持つ POST 要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-142">To retrieve an Azure AD token, create a POST request that has a URL in the format `https://login.microsoftonline.com/[tenant ID]/oauth2/token`.</span></span>

    <span data-ttu-id="5cc6a-143">`https://login.microsoftonline.com/:tenant_id/oauth2/token` などの、**tenant\_id** 環境変数を参照する URL パラメーターを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-143">You can use a URL parameter that refers to the **tenant\_id** environment variable, such as `https://login.microsoftonline.com/:tenant_id/oauth2/token`.</span></span>

    ![Azure AD トークンの取得](./media/postman6.png)

9. <span data-ttu-id="5cc6a-145">**本文**タブで、前に作成した環境変数を参照する要求パラメーターとして、本文要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-145">On the **Body** tab, add body elements as request parameters that refer to the environment variables that you created earlier.</span></span> <span data-ttu-id="5cc6a-146">**一括編集** を選択して、上記の表のキーを入力し、コロン (:) を入力してからキーの名前を再入力しますが、二重中かっこ ({{}}) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-146">Select **Bulk Edit**, enter the keys from the previous table, enter a colon (:), and then enter the key name again but enclose it in double braces ({{}}).</span></span> <span data-ttu-id="5cc6a-147">行ごとに 1 つの要求パラメーターを入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-147">Enter one request parameter per line.</span></span> <span data-ttu-id="5cc6a-148">たとえば、**交付\_タイプ:{{交付\_タイプ}}** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-148">For example, enter **grant\_type:{{grant\_type}}**.</span></span> <span data-ttu-id="5cc6a-149">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-149">Here is an example.</span></span>

    ![本文要素](./media/postman8.png)

10. <span data-ttu-id="5cc6a-151">**テスト**タブで、応答が妥当であることを検証し、環境変数で返される認証トークンを格納するテストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-151">On the **Tests** tab, create a test that validates that the response is reasonable, and that stores the returned authorization token in an environment variable.</span></span> <span data-ttu-id="5cc6a-152">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-152">Here is an example.</span></span>

    ```csharp
    var json = JSON.parse(responseBody);
    tests["Get Azure AD Token"] = !json.error && responseBody !== '' && responseBody !== '{}' && json.access_token !== '';
    postman.setEnvironmentVariable("bearerToken", json.access_token);
    ```

11. <span data-ttu-id="5cc6a-153">**保存** を選択し、要求の名前とコレクションを入力して、**保存** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-153">Select **Save**, enter a name and collection for the request, and then select **Save** again.</span></span>
12. <span data-ttu-id="5cc6a-154">**送信** を選択して承認要求を行います。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-154">Select **Send** to make the authorization request.</span></span> <span data-ttu-id="5cc6a-155">**本文** タブには、その他の応答の詳細と共に、Azure AD トークンが含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-155">The **Body** tab should now contain an Azure AD token together with other response details.</span></span>

    ![Azure ADトークン](./media/postman11.png)

13. <span data-ttu-id="5cc6a-157">テスト コードのため、トークンは環境変数にあります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-157">Because of the test code, the token is now in an environment variable.</span></span> <span data-ttu-id="5cc6a-158">**環境クイック表示** ボタン (目のボタン) を選択すると、トークンが環境変数であることがわかります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-158">You can see that the token is an environment variable by selecting the **Environment quick look** button (the eye button).</span></span>

    ![環境クイック表示](./media/postman12.png)

14. <span data-ttu-id="5cc6a-160">OData サービスを介して、目的のデータ エンティティに対して作成、読み取り、更新、または削除 (CRUD) 操作を実行する要求を作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-160">Create a request to perform create, read, update, or delete (CRUD) operations on the desired data entity via the OData service.</span></span> <span data-ttu-id="5cc6a-161">必要に応じて URL を作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-161">Create the URL according to your requirements.</span></span> <span data-ttu-id="5cc6a-162">詳細については、[データ プロトコル (OData) を開く](odata.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-162">For more information, see [Open Data Protocol (OData)](odata.md).</span></span> <span data-ttu-id="5cc6a-163">前に示したように、環境に格納されている変数を使用して、要求をパラメーター化することが便利であることがわかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-163">You might find it useful to parameterize the request by using a variable that is stored in the environment, as shown earlier.</span></span> <span data-ttu-id="5cc6a-164">次の GET クエリの例では、**Customer Account** パラメーターが使用されています。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-164">The following example of a GET query uses a **Customer Account** parameter.</span></span> <span data-ttu-id="5cc6a-165">クエリは、環境変数で指定された顧客アカウントの名前とアドレスの詳細を返します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-165">The query returns name and address details for the customer account that is specified in the environment variable.</span></span> <span data-ttu-id="5cc6a-166">特殊文字は、URL に正しくエンコードされる必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-166">Note that special characters must be correctly URL-encoded.</span></span>

    ```Console
    https://[Finance and Operations instance URL]/data/Customers?$format=json&$filter=CustomerAccount%20eq%20%27{{custAccount}}%27&$select=CustomerAccount,Name,AddressDescription,FullPrimaryAddress
    ```

15. <span data-ttu-id="5cc6a-167">以前に取得され、**bearerToken** 環境変数に格納された認証トークンを参照する認証ヘッダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-167">Add an Authorization header that refers to the authorization token that was retrieved earlier and stored in the **bearerToken** environment variable.</span></span> <span data-ttu-id="5cc6a-168">トークンは、ヘッダーの先頭に **Bearer** を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-168">The token must be prefixed by **Bearer** in the header.</span></span>

    ![ベアラー トークン](./media/postman13.png)

16. <span data-ttu-id="5cc6a-170">応答を検証するためのテストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-170">Create a test to help validate the response.</span></span> <span data-ttu-id="5cc6a-171">次の例では、空でない JSON 形式のデータが応答本文に返されるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-171">The following example tests that non-empty, JSON-formatted data is returned in the response body.</span></span>

    ```csharp
    var json = JSON.parse(responseBody);
    tests["Get customer info"] = !json.error && responseBody !== '' && responseBody !== '{}';
    ```

17. <span data-ttu-id="5cc6a-172">要求を保存および送信し、結果を確認します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-172">Save and send the request, and then verify the result.</span></span> <span data-ttu-id="5cc6a-173">使用するユーザー アカウントが、データを持つ既定の会社に対して設定されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-173">You must ensure that the user account being used is set to a default company that has data.</span></span> <span data-ttu-id="5cc6a-174">または、OData 要求のクエリ パラメーターとして、クロス会社 =true を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-174">Alternatively, you can also specify cross-company=true as the query parameter in the OData request.</span></span>

    ![結果](./media/postman15.png)

<span data-ttu-id="5cc6a-176">ここでは、正常に認証されてから、OData サービスを使用して、顧客レコードを読み取っています。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-176">In our example, we have now successfully authenticated and then used the OData service to read a customer record.</span></span>

## <a name="query-the-soap-custom-service-in-your-application-by-using-soapui"></a><span data-ttu-id="5cc6a-177">SoapUI を使用して、アプリケーションで SOAP カスタム サービスのクエリを実行</span><span class="sxs-lookup"><span data-stu-id="5cc6a-177">Query the SOAP custom service in your application by using SoapUI</span></span>

<span data-ttu-id="5cc6a-178">SoapUI (<https://www.soapui.org/>) は、API の開発とテストが関係するシナリオで SOAP および REST Web サービスを操作するために多くの場合使用されるツールです。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-178">SoapUI (<https://www.soapui.org/>) is a tool that is often used to interact with SOAP and REST web services in scenarios that involve API development and testing.</span></span> <span data-ttu-id="5cc6a-179">このステップは SoapUI を推奨するものではなく、他の類似のツールも使用できます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-179">This procedure isn't an endorsement of SoapUI, and other similar tools are available.</span></span> <span data-ttu-id="5cc6a-180">ただし、Azure AD で認証する OAuth を使用する際に含まれる概念およびメッセージについて説明するのに SoapUI を使用しており、SOAP 要求を作成して応答を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-180">However, we are using SoapUI to illustrate the concepts and messages that are involved when you use OAuth to authenticate with Azure AD, and then make SOAP requests to and receive responses.</span></span>

1. <span data-ttu-id="5cc6a-181">SoapUI を起動し、**SOAP** ボタンを選択してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-181">Start SoapUI, and select the **SOAP** button to create a project.</span></span>
2. <span data-ttu-id="5cc6a-182">プロジェクトの情報を記入してください:</span><span class="sxs-lookup"><span data-stu-id="5cc6a-182">Complete the information for the project:</span></span>

    - <span data-ttu-id="5cc6a-183">**プロジェクト名**フィールドに、プロジェクトの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-183">In the **Project Name** field, enter a name for the project.</span></span>
    - <span data-ttu-id="5cc6a-184">**初期 WSDL** フィールドに、サービス アドレスを入力し、接尾語 **?wsdl** を追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-184">In the **Initial WSDL** field, enter the service address, and add the suffix **?wsdl**.</span></span> <span data-ttu-id="5cc6a-185">(サービスの住所は \[Finance and Operations インスタンスのベース URL\]/soap/services/ \[サービス グループ名\] の形式である必要があります。) 詳細については、[サービスのホーム ページ](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-185">(The service address should be in the format \[Finance and Operations instance base URL\]/soap/services/\[service group name\].) For more information, see the [Services home page](services-home-page.md).</span></span>

        <span data-ttu-id="5cc6a-186">たとえば、URL `https://[Finance and Operations base URL]/soap/services/UserSessionService?wsdl` でユーザー セッション サービスについて問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-186">For example, we are querying the user session service at the URL `https://[Finance and Operations base URL]/soap/services/UserSessionService?wsdl`.</span></span>

    - <span data-ttu-id="5cc6a-187">**すべての工程でサンプル依頼を作成しますか?** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-187">Select the **Create sample requests for all operations?** check box.</span></span>

        <span data-ttu-id="5cc6a-188">サンプル要求の作成を選択したため、利用可能なサービス操作ごとに 1 つのサンプル要求が作成されます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-188">Because you selected to create sample requests, one sample request is created for each service operation that is available.</span></span>

        ![サンプル要求](./media/soapui3.png)

3. <span data-ttu-id="5cc6a-190">新しいプロジェクトを右クリックし、**新しいテスト スイート** を選択してテスト スイートを作成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-190">Right-click the new project, and then select **New TestSuite** to create a test suite.</span></span> <span data-ttu-id="5cc6a-191">このテスト スイートは、Azure AD 認証トークンに対する POST 要求を生成します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-191">This test suite will generate a POST request for an Azure AD authorization token.</span></span>
4. <span data-ttu-id="5cc6a-192">テスト スイートを右クリックし、**新しいテスト ケース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-192">Right-click the test suite, and then select **New TestCase**.</span></span>
5. <span data-ttu-id="5cc6a-193">テスト ケースを展開し、**テスト ステップ**を右クリックして**ステップの追加**を選び、次に **HTTP 要求**を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-193">Expand the test case, right-click **Test Steps**, select **Add Step**, and then select **HTTP Request**.</span></span>
6. <span data-ttu-id="5cc6a-194">要求名を入力し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-194">Enter a name for the request, and then select **OK**.</span></span>
7. <span data-ttu-id="5cc6a-195">テスト ステップ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-195">Enter a name for the test step.</span></span> <span data-ttu-id="5cc6a-196">POST 要求に使用する必要のあるエンドポイントは、`[https://login.microsoftonline.com/[tenant_id]/oauth2/token](https://login.microsoftonline.com/%5btenant_id%5d/oauth2/token)` です。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-196">The endpoint that you should use for the POST request is `[https://login.microsoftonline.com/[tenant_id]/oauth2/token](https://login.microsoftonline.com/%5btenant_id%5d/oauth2/token)`.</span></span>
8. <span data-ttu-id="5cc6a-197">**パラメーター** の横にある [プラス記号 (**+**)] ボタンを使用して、次の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-197">Use the plus sign (**+**) button next to **Parameters** to add the following values.</span></span>

    | <span data-ttu-id="5cc6a-198">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5cc6a-198">Parameter</span></span>      | <span data-ttu-id="5cc6a-199">先頭値</span><span class="sxs-lookup"><span data-stu-id="5cc6a-199">Value</span></span>                                                           |
    |----------------|-----------------------------------------------------------------|
    | <span data-ttu-id="5cc6a-200">grant\_type</span><span class="sxs-lookup"><span data-stu-id="5cc6a-200">grant\_type</span></span>    | <span data-ttu-id="5cc6a-201">client\_credentials</span><span class="sxs-lookup"><span data-stu-id="5cc6a-201">client\_credentials</span></span>                                             |
    | <span data-ttu-id="5cc6a-202">client\_id</span><span class="sxs-lookup"><span data-stu-id="5cc6a-202">client\_id</span></span>     | <span data-ttu-id="5cc6a-203">Azure AD アプリケーション登録のアプリケーション ID</span><span class="sxs-lookup"><span data-stu-id="5cc6a-203">The application ID from the Azure AD application registration</span></span>   |
    | <span data-ttu-id="5cc6a-204">client\_secret</span><span class="sxs-lookup"><span data-stu-id="5cc6a-204">client\_secret</span></span> | <span data-ttu-id="5cc6a-205">Azure AD アプリケーション登録の秘密キーの値</span><span class="sxs-lookup"><span data-stu-id="5cc6a-205">The secret key value from the Azure AD application registration</span></span> |
    | <span data-ttu-id="5cc6a-206">リソース</span><span class="sxs-lookup"><span data-stu-id="5cc6a-206">resource</span></span>       | <span data-ttu-id="5cc6a-207">末尾の '/' を除いたインスタンスの URL</span><span class="sxs-lookup"><span data-stu-id="5cc6a-207">The URL of the instance without the trailing '/'</span></span>                 |

9. <span data-ttu-id="5cc6a-208">パラメーターが POST 本体にあることを確認するには、**Post QueryString** を選択し、**再生** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-208">To make sure that the parameters are in the POST body, select **Post QueryString**, and then select **Play**.</span></span> <span data-ttu-id="5cc6a-209">アクセス トークンは応答ウィンドウに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-209">An access token should be returned in the response pane.</span></span> <span data-ttu-id="5cc6a-210">**JSON 応答** タブを使用すると、値が最も読みやすくなります。アクセス トークンをコピーして、後続の要求の認証ヘッダーで使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-210">The values will be most readable if you use the **JSON response** tab. Copy the access token so that you can use it in the authorization header of subsequent requests.</span></span>
10. <span data-ttu-id="5cc6a-211">**GetUserSessionInfo**SOAP サンプル要求で、最初の要求ノードに戻ります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-211">Go back to the first request node under the **GetUserSessionInfo** SOAP sample request.</span></span> <span data-ttu-id="5cc6a-212">左側の要求ウィンドウで、プラス記号 (**+**) ボタンを選択して、**認証**というヘッダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-212">In the request pane on the left, select the plus sign (**+**) button to add a header that is named **Authorization**.</span></span> <span data-ttu-id="5cc6a-213">アクセストークンを **Value** フィールドに貼り付け、プレフィックス **Bearer** を追加します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-213">Paste the access token into the **Value** field, and add the prefix **Bearer**.</span></span>
11. <span data-ttu-id="5cc6a-214">SoapUI が作成するサンプル リクエストは、変更しない限り動作しません。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-214">The sample requests that SoapUI creates won't work unless you modify them.</span></span> <span data-ttu-id="5cc6a-215">行なおうとしていることのスキーマに対応できるように、呼び出しコンテキストと本文を編集する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-215">You must edit the call context and body so that they are consistent with the schema for what you're trying to do.</span></span>

    <span data-ttu-id="5cc6a-216">単純なシナリオでは、null 値になるように、オプションの呼び出しコンテキスト要素を編集できます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-216">For our simple scenario, you can edit the optional call context elements so that they are null-valued.</span></span> <span data-ttu-id="5cc6a-217">開始タグで大なり記号 (&gt;) の前にフォワード スラッシュ (/) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-217">Insert a forward slash (/) before the greater than sign (&gt;) in the opening tags.</span></span> <span data-ttu-id="5cc6a-218">コメントの開始と終了を区切るには、標準の &lt;!--...--&gt; 構文を使用して疑問符 (?) と終了タグをコメント アウトします。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-218">Then comment out the question marks (?) and the closing tags by using the standard &lt;!--...--&gt; syntax to delimit the start and end of the comments.</span></span> <span data-ttu-id="5cc6a-219">(疑問符は XML スキーマの有効なコンテンツではありません。) または、疑問符 (?) を削除して、コンテキスト要素が空になるようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-219">(Question marks aren't valid content for the XML schema.) Alternatively, you can just delete the question marks (?) so that the context elements are empty.</span></span>

12. <span data-ttu-id="5cc6a-220">SOAP 要求の準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-220">The SOAP request is now ready.</span></span> <span data-ttu-id="5cc6a-221">**再生** を選択し、右側の結果を検証します。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-221">Select **Play**, and validate the result on the right.</span></span>

    ![結果の検証](./media/soapui8.png)

<span data-ttu-id="5cc6a-223">ここでは、正常に認証されてから、SOAP を介して UserSessionService を照会しています。</span><span class="sxs-lookup"><span data-stu-id="5cc6a-223">In our example, we have now successfully authenticated and then queried UserSessionService via SOAP.</span></span>
