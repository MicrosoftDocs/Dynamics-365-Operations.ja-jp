---
title: ビジネス イベントおよび Azure Event Grid
description: このトピックでは、Microsoft Azure イベント グリッド エンドポイントを構成する方法と、イベント グリッドからビジネス イベントを消費する方法について説明します。
author: ibenbouzid
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 6ab7c0081fec1688cdd57cdbfea10040813b5f51
ms.sourcegitcommit: b6ecc60e33deef76b7248466c5747ac6f20d30ee
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/30/2019
ms.locfileid: "2691549"
---
# <a name="business-events-and-azure-event-grid"></a><span data-ttu-id="3b8aa-103">ビジネス イベントおよび Azure Event Grid</span><span class="sxs-lookup"><span data-stu-id="3b8aa-103">Business events and Azure Event Grid</span></span>
[!include[banner](../../includes/banner.md)]

<span data-ttu-id="3b8aa-104">このトピックでは、Microsoft Azure イベント グリッド エンドポイントを構成する方法と、イベント グリッドからビジネス イベントを消費する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-104">This topic explains how to configure a Microsoft Azure Event Grid endpoint, and how to consume a business event from Event Grid.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="3b8aa-105">シナリオの概要</span><span class="sxs-lookup"><span data-stu-id="3b8aa-105">Scenario overview</span></span>

<span data-ttu-id="3b8aa-106">セキュリティのベスト プラクティスでは、接続文字列をアプリケーション外の Azure Key Vault ドライブに保存し、アプリケーションに対して Key Vault キー、シークレット、証明書の適切なアクセス権を付与することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-106">Security best practices recommend that you store connection strings outside applications, in an Azure Key Vault drive, and that you give applications the correct access to the key vault keys, secrets, or certificates.</span></span>

<span data-ttu-id="3b8aa-107">このアプローチの多くの利点のうち 2 つを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-107">Here are two of the many benefits of this approach:</span></span>

- <span data-ttu-id="3b8aa-108">アプリケーション データベースにアクセスできるユーザーは、サードパーティの接続文字列を取得できません。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-108">Someone who gets access to the application database won't be able to get the third-party connection string.</span></span>
- <span data-ttu-id="3b8aa-109">特に複数のアプリケーションが同じリソースにアクセスする場合、更新する必要がある接続文字列が 1 か所だけなのでメンテナンスが簡単です。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-109">Maintenance is easier, especially when multiple applications access the same resources, because you must update connection strings in only one place.</span></span>

<span data-ttu-id="3b8aa-110">完了する必要がある手順の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-110">Here is an overview of the procedures that you must complete:</span></span>

1. <span data-ttu-id="3b8aa-111">新しいイベント グリッド トピックを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-111">Create a new event grid topic.</span></span>
2. <span data-ttu-id="3b8aa-112">イベント グリッド トピックのキーを格納する新しいキー コンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-112">Create a new key vault to store the key for the event grid topic.</span></span>
3. <span data-ttu-id="3b8aa-113">Key Vault にアクセスするためのアクセス許可が与えられている Azure アプリを登録します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-113">Register an Azure app that has permission to access the key vault.</span></span>
4. <span data-ttu-id="3b8aa-114">エンドポイントのパラメーターをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-114">Configure the parameters of the endpoint.</span></span>
5. <span data-ttu-id="3b8aa-115">ビジネス イベントを消費します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-115">Consume the business event.</span></span>

## <a name="procedure-1-create-a-new-event-grid-topic"></a><span data-ttu-id="3b8aa-116">手順 1: 新しいイベント グリッド トピックを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-116">Procedure 1: Create a new event grid topic</span></span>

1. <span data-ttu-id="3b8aa-117">Azure ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-117">Sign in to the Azure portal.</span></span>
2. <span data-ttu-id="3b8aa-118">**すべてのサービス \> 統合 \> イベント グリッド トピック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-118">Select **All services \> Integration \> Event Grid Topics**.</span></span>
3. <span data-ttu-id="3b8aa-119">**追加** を選択して新しいイベント グリッド トピックを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-119">Select **Add** to create a new event grid topic.</span></span> <span data-ttu-id="3b8aa-120">パラメーターを設定してから **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-120">Set the parameters, and then select **Create**.</span></span> <span data-ttu-id="3b8aa-121">ラボのコンテナーとして新しいリソース グループを作成するか、または既存のリソース グループを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-121">You can create a new resource group as a container for your lab, or you can use an existing resource group.</span></span>
4. <span data-ttu-id="3b8aa-122">配置が完了したら、新しいイベント グリッドを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-122">After deployment is completed, select the new event grid.</span></span> <span data-ttu-id="3b8aa-123">プロパティ ブレードで **概要** を選択し、**トピック エンドポイント** 値をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-123">On the property blade, select **Overview**, and make a note of the **Topic Endpoint** value.</span></span> <span data-ttu-id="3b8aa-124">後に、この値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-124">You will need this value later.</span></span>

    <img alt="Event grid topic" src="../../media/BEF-Howto-EventGrid-03.png" width="70%">

5. <span data-ttu-id="3b8aa-125">プロパティ ブレードに戻って **アクセス キー** を選択して **キー 1** の値をコピーします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-125">Back on the property blade, select **Access keys**, and copy the **Key 1** value.</span></span> <span data-ttu-id="3b8aa-126">次の手順でキー コンテナーを構成するときに、この値が必要になります。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-126">You will need this value when you configure the key vault in the next procedure.</span></span>

    <img alt="Event grid access key" src="../../media/BEF-Howto-EventGrid-04.png" width="70%">

## <a name="procedure-2-create-a-key-vault"></a><span data-ttu-id="3b8aa-127">手順 2: 新しいキー コンテナーの作成</span><span class="sxs-lookup"><span data-stu-id="3b8aa-127">Procedure 2: Create a key vault</span></span>

<span data-ttu-id="3b8aa-128">この手順では、前の手順でコピーしたキーを保存する Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-128">In this procedure, you will create a key vault to store the key that you copied in the previous procedure.</span></span> <span data-ttu-id="3b8aa-129">Key Vault は、キー、シークレット、証明書を保存するために使用する安全なドライブです。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-129">A key vault is a secure drive that is used to store keys, secrets, and certificates.</span></span> <span data-ttu-id="3b8aa-130">接続文字列を保存する代わりに、より一般的で安全なアプローチは Key Vault に保存することです。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-130">Instead of storing the connection string, a more typical and more secure approach is to store it in a key vault.</span></span> <span data-ttu-id="3b8aa-131">その後、新しいアプリケーションを Azure Active Directory (Azure AD) に登録し、Key Vault からシークレットを取得する権限を付与できます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-131">You can then register a new application with Azure Active Directory (Azure AD) and grant it the right to retrieve the secret from the key vault.</span></span>

1. <span data-ttu-id="3b8aa-132">Azure ポータルで **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-132">In the Azure portal, select **All services \> Security \> Key vaults**.</span></span>
2. <span data-ttu-id="3b8aa-133">リソース グループに新しい Key Vault を作成し、デフォルトのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-133">Create a new key vault in your resource group and set the default parameters.</span></span>

    <img alt="New Key Vault" src="../../media/BEF-Howto-Keyvault-02.png" width="50%">

3. <span data-ttu-id="3b8aa-134">**概要** を選択し、Key Vault の **DNS 名** 値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-134">Select **Overview**, then copy and save the **DNS Name** value for the key vault.</span></span> <span data-ttu-id="3b8aa-135">この値は後で使用します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-135">You will use this value later.</span></span>

    <img alt="Key vault DNS name" src="../../media/BEF-Howto-Keyvault-03.png" width="70%">

4. <span data-ttu-id="3b8aa-136">**BE-Key Vault \> シークレット \> 生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-136">Select **BE-key vault \> Secrets \> Generate/Import**.</span></span> <span data-ttu-id="3b8aa-137">シークレットの名前を入力し、先に保存したイベント グリッド接続文字列を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-137">Enter a name for your secret, and paste the event grid connection string that you saved earlier.</span></span>

    <img alt="Key vault secret " src="../../media/BEF-Howto-Keyvault-04.png" width="70%">

5. <span data-ttu-id="3b8aa-138">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-138">Select **Create**.</span></span>

## <a name="procedure-3-register-a-new-application"></a><span data-ttu-id="3b8aa-139">手順 3: 新しいアプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="3b8aa-139">Procedure 3: Register a new application</span></span>

<span data-ttu-id="3b8aa-140">この手順では、新しいアプリケーションを Azure AD に登録して、Key Vault のシークレットの読み取りと取得アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-140">In this procedure, you will register a new application with Azure AD, and give it read and retrieve access to key vault secrets.</span></span> <span data-ttu-id="3b8aa-141">アプリケーションを使用してイベント グリッドのシークレットを取得します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-141">The application will then use this application to retrieve event grid secrets.</span></span>

1. <span data-ttu-id="3b8aa-142">Azure ポータルで **すべてのサービス \> セキュリティ \> Azure Active Directory** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-142">In the Azure portal, select **All services \> Security \> Azure Active Directory**.</span></span>
2. <span data-ttu-id="3b8aa-143">**アプリ登録 (プレビュー) \> 新しい登録** を選択し、次にアプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-143">Select **App registrations (preview) \> New registration**, and then enter a name for your application.</span></span>
3. <span data-ttu-id="3b8aa-144">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-144">Select **Register**.</span></span>
4. <span data-ttu-id="3b8aa-145">新しいアプリケーションを選択して **証明書とシークレット \> 新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-145">Select your new application, and then select **Certificates & secrets \> New client secret**.</span></span> <span data-ttu-id="3b8aa-146">シークレットの名前を入力し、有効期限が切れないようにシークレットを設定します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-146">Enter a name for your secret, and set the secret so that it never expires.</span></span> <span data-ttu-id="3b8aa-147">その後 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-147">Then select **Add**.</span></span>

    <img alt="Azure App secret " src="../../media/BEF-Howto-Keyvault-07.png" width="50%">

5. <span data-ttu-id="3b8aa-148">新しいシークレットをコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-148">Copy and save your new secret.</span></span> <span data-ttu-id="3b8aa-149">これは後で使用します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-149">You will use it later.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="3b8aa-150">シークレットは一度だけ表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-150">Secrets are visible only one time.</span></span> <span data-ttu-id="3b8aa-151">シークレットをコピーし忘れた場合は、削除してから新しいシークレットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-151">If you forget to copy the secret, you will have to delete it and create a new secret.</span></span>

    <img alt="Copy App secret " src="../../media/BEF-Howto-Keyvault-08.png" width="70%">

6. <span data-ttu-id="3b8aa-152">**概要** を選択し、アプリケーション ID をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-152">Select **Overview**, and copy and save the application ID.</span></span> <span data-ttu-id="3b8aa-153">この値は後で使用します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-153">You will use this value later.</span></span>

    <img alt="Copy App Id " src="../../media/BEF-Howto-Keyvault-09.png" width="70%">

7. <span data-ttu-id="3b8aa-154">**すべてのサービス \> セキュリティ \> Key Vaults** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-154">Select **All services \> Security \> Key vaults**.</span></span>
8. <span data-ttu-id="3b8aa-155">前に作成した Key Vault を選択してから **アクセスポリシー \> 新規追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-155">Select the key vault that you created earlier, and then select **Access policies \> Add new**.</span></span>
9. <span data-ttu-id="3b8aa-156">**プリンシパル** ブレードで、新しい登録済みアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-156">On the **Principal** blade, select your new registered application.</span></span> <span data-ttu-id="3b8aa-157">Key Vault のシークレットを取得するには、**Get** と **List** シークレット アクセス許可のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-157">Select the check boxes for the **Get** and **List** secret permissions to retrieve key vault secrets.</span></span>

    <img alt="Key Vault access policy " src="../../media/BEF-Howto-Keyvault-12.png" width="50%">

10. <span data-ttu-id="3b8aa-158">新しいアクセス ポリシーを保存します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-158">Save your new access policy.</span></span>

## <a name="procedure-4-configure-a-business-events-endpoint"></a><span data-ttu-id="3b8aa-159">手順 4: ビジネス イベント エンドポイントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="3b8aa-159">Procedure 4: Configure a Business Events endpoint</span></span>

1. <span data-ttu-id="3b8aa-160">アプリケーションにサイン インし、**システム管理 \> 設定 \> ビジネス イベント**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-160">Sign in to the application and go to **System administration \> Setup \> Business events**.</span></span>
2. <span data-ttu-id="3b8aa-161">**エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-161">Select **Endpoints**.</span></span>
3. <span data-ttu-id="3b8aa-162">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-162">Select **New**.</span></span>
4. <span data-ttu-id="3b8aa-163">**Azure Event Grid** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-163">Select **Azure Event Grid**.</span></span>
5. <span data-ttu-id="3b8aa-164">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-164">Select **Next**.</span></span>
6. <span data-ttu-id="3b8aa-165">必要なパラメーター値を設定します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-165">Set the required parameter values.</span></span>

    <img alt="Event grid endpoint" src="../../media/BEF-Howto-EventGrid-06.png" width="50%">

7. <span data-ttu-id="3b8aa-166">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-166">Select **OK**.</span></span>

## <a name="procedure-5-consume-a-business-event"></a><span data-ttu-id="3b8aa-167">手順 5: ビジネス イベントの消費</span><span class="sxs-lookup"><span data-stu-id="3b8aa-167">Procedure 5: Consume a business event</span></span>

<span data-ttu-id="3b8aa-168">ビジネス シナリオでは、USMF 会社に自由書式の請求書が転記されるたびに電子メール メッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-168">The business scenario involves sending an email message whenever a free text invoice is posted for the USMF company.</span></span> <span data-ttu-id="3b8aa-169">顧客アカウント番号、顧客名、請求書の合計金額など、詳細がメッセージ\`に含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-169">The message must contain details such as the customer account number, the customer name, and the total amount of the invoice.</span></span>

1. <span data-ttu-id="3b8aa-170">ビジネス イベント カタログを選択し、**自由書式の請求書が転記されました**ビジネス イベントを探します</span><span class="sxs-lookup"><span data-stu-id="3b8aa-170">Select the business event catalog and look for **free text invoice posted** business event.</span></span>
2. <span data-ttu-id="3b8aa-171">次に USMF 会社のビジネス イベントを有効化します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-171">Then activate the business event for USMF company.</span></span> <span data-ttu-id="3b8aa-172">一度有効になると、テスト メッセージは送信され、構成を検証し、接続をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-172">Once activated, a test message is sent to validate the configuration and cache the connection.</span></span>
3. <span data-ttu-id="3b8aa-173">テスト メッセージが受信されたことを確認するには、Azure ポータルでイベント グリッド トピックを選択して **メトリック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-173">To verify that the test message has been received, in the Azure portal, select your event grid topic, and then select **Metrics**.</span></span> <span data-ttu-id="3b8aa-174">**公開されたイベント** メトリックと **一致しないイベント** メトリックの両方が少なくとも **1** の値を示していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-174">Verify that both the **Published Events** metric and the **Unmatched Events** metric show a value of at least **1**.</span></span> <span data-ttu-id="3b8aa-175">そうでない場合は、バッチ ジョブがメッセージを受信するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-175">If they don't, wait for the batch job to pick up your message.</span></span>

    <img alt="Event grid metrics" src="../../media/BEF-Howto-EventGrid-08.png" width="70%">

    <span data-ttu-id="3b8aa-176">両方のメトリックの値が少なくとも **1** の場合、イベント グリッド トピックをサブスクライブする新しいロジック アプリを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-176">When both metrics have a value of at least **1**, you will create a new logic app to subscribe to your event grid topic.</span></span>

4. <span data-ttu-id="3b8aa-177">**すべてのサービス \> 統合 \> ロジック アプリ** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-177">Select **All services \> Integration \> Logic Apps**.</span></span>
5. <span data-ttu-id="3b8aa-178">リソース グループに新しいロジック アプリを作成します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-178">Create a new logic app in your resource group.</span></span>

    <img alt="New logic apps" src="../../media/BEF-Howto-EventGrid-10.png" width="50%">

6. <span data-ttu-id="3b8aa-179">ロジック アプリ リソースを作成したら、空のロジック アプリを作成するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-179">After your logic app resource has been created, select the option to create a blank logic app.</span></span>
7. <span data-ttu-id="3b8aa-180">**イベント グリッド** を検索して **リソース イベントが発生した場合 (プレビュー)** トリガーを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-180">Search for **Event Grid**, and select the **When a resource event occurs (preview)** trigger.</span></span>

    <img alt="Event grid trigger" src="../../media/BEF-Howto-EventGrid-11.png" width="50%">

8. <span data-ttu-id="3b8aa-181">サブスクリプションを選択し、リソース タイプとして **Microsoft.EventGrid.Topics** を選択し、手順 1 で作成したイベント グリッド トピックの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-181">Select your subscription, select **Microsoft.EventGrid.Topics** as the resource type, and select the name of the event grid topic that you created in procedure 1.</span></span>

    <img alt="Event grid trigger parameters" src="../../media/BEF-Howto-EventGrid-12.png" width="50%">

9. <span data-ttu-id="3b8aa-182">**新規ステップ** を選択して新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-182">Select **New Step** to add a new action.</span></span>
10. <span data-ttu-id="3b8aa-183">**JSON の解析** データ処理を検索します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-183">Search for the **Parse Json** data operation.</span></span> <span data-ttu-id="3b8aa-184">このステップは、データ コントラクトの指定されたスキーマを使用してメッセージを解析するために必要です。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-184">This step is required so that the message can be parsed by using the provided schema for the data contract.</span></span>
11. <span data-ttu-id="3b8aa-185">**Json 解析** アクションの **コンテンツ** フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-185">Click in the **Content** field of the **Parse Json** action.</span></span> <span data-ttu-id="3b8aa-186">表示されるウィンドウには前のトリガーからのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-186">The pane that appears gives you the option form the previous trigger.</span></span> <span data-ttu-id="3b8aa-187">Finance and Operations で送信されるペイロードを含むイベント グリッド メッセージの **データ オブジェクト** フィールドを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-187">You must select the **Data object** field of the event grid message that contains the payload that is transmitted by Finance and Operations.</span></span>

    <img alt="Logic appas parse JSON " src="../../media/BEF-Howto-EventGrid-14.png" width="50%">

    <span data-ttu-id="3b8aa-188">次に、契約の指定されたスキーマを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-188">Next, you must enter the provided schema for the contract.</span></span> <span data-ttu-id="3b8aa-189">これは、ただのサンプル ペイロードです。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-189">This is only a sample payload.</span></span> <span data-ttu-id="3b8aa-190">ただし、Azure ロジック アプリの機能を使用してペイロードからスキーマを生成できます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-190">However, you can use a capability of Azure Logic Apps to generate a schema from a payload.</span></span>

12. <span data-ttu-id="3b8aa-191">ビジネス イベント カタログのイベントを選択し、**スキーマのダウンロード**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-191">Select your event in the business event catalog, and then select the **Download schema** link.</span></span> <span data-ttu-id="3b8aa-192">テキスト ファイルがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-192">A text file is downloaded.</span></span> <span data-ttu-id="3b8aa-193">テキストファイルを開いて内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-193">Open the text file, and copy the contents.</span></span>
13. <span data-ttu-id="3b8aa-194">ロジック アプリに戻って **サンプル ペイロードを使用してスキーマを生成** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-194">Go back to Logic Apps, and select the **Use sample payload to generate schema** link.</span></span> <span data-ttu-id="3b8aa-195">テキスト ファイルの内容を貼り付けて **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-195">Paste the contents of the text file, and then select **Done**.</span></span>

    <img alt="Event schema " src="../../media/BEF-Howto-EventGrid-16.png" width="70%">

14. <span data-ttu-id="3b8aa-196">サンプル ペイロードの品質により、特に実値がサンプル ペイロードで整数として与えられた場合、ジェネレーターは整数と実値を区別しません。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-196">Depending on the quality of your sample payload, your generator won't be able to distinguish between an integer and a real value, especially if the real value is provided as a whole number in the sample payload.</span></span> <span data-ttu-id="3b8aa-197">生成されたスキーマを確認して **整数** データ型のフィールドを **数値** データ型に変更する必要があるか判断します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-197">Review the schema that is generated, and determine whether you must change a field of the **integer** data type to the **number** data type.</span></span> <span data-ttu-id="3b8aa-198">(JavaScript Object Notation \[JSON\] で **数値** データ型は実数値を表します。)</span><span class="sxs-lookup"><span data-stu-id="3b8aa-198">(In JavaScript Object Notation \[JSON\], the **number** data type represents real values.)</span></span>

    <img alt="JSON data types " src="../../media/BEF-Howto-EventGrid-17.png" width="100%">

    <span data-ttu-id="3b8aa-199">次に、顧客の支払いの詳細を含む通知電子メールの送信など、最終的なアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-199">Next, you will select a final action, such as sending a notification email that includes customer payment details.</span></span>

15. <span data-ttu-id="3b8aa-200">**電子メールの送信** アクションを検索し、自分の Microsoft Office 365 アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-200">Search for the **send email** action, and then sign in to your Microsoft Office 365 account.</span></span>
16. <span data-ttu-id="3b8aa-201">メッセージの本文および、必須項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-201">Fill in the message with the required fields.</span></span>
17. <span data-ttu-id="3b8aa-202">ロジック アプリを保存します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-202">Save your logic app.</span></span>
18. <span data-ttu-id="3b8aa-203">顧客の支払いを転記して、ビジネス イベントをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-203">Trigger the business event by posting a customer payment.</span></span> <span data-ttu-id="3b8aa-204">そして、ロジック アプリが実行されていること、顧客の支払いの詳細が記載された電子メールを受信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="3b8aa-204">Then verify that the logic app runs, and that you receive an email that includes customer payment details.</span></span>
