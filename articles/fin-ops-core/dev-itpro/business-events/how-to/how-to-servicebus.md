---
title: ビジネス イベントおよび Azure Service Bus
description: このトピックでは、Microsoft Azure Service Bus エンドポイントを構成する方法と、Service Bus からビジネス イベントを消費する方法を説明します。
author: ibenbouzid
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 30412ba27efce40ee1f10eeb69a6cc06c3e1d8c0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191550"
---
# <a name="business-events-and-azure-service-bus"></a><span data-ttu-id="6f944-103">ビジネス イベントおよび Azure Service Bus</span><span class="sxs-lookup"><span data-stu-id="6f944-103">Business events and Azure Service Bus</span></span>
[!include[banner](../../includes/banner.md)]

<span data-ttu-id="6f944-104">このトピックでは、Microsoft Azure Service Bus エンドポイントを構成する方法と、Service Bus からビジネス イベントを消費する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="6f944-104">This topic explains how to configure a Microsoft Azure Service Bus endpoint and how to consume a business event from Service Bus.</span></span>

## <a name="scenario-overview"></a><span data-ttu-id="6f944-105">シナリオの概要</span><span class="sxs-lookup"><span data-stu-id="6f944-105">Scenario overview</span></span>

<span data-ttu-id="6f944-106">セキュリティのベスト プラクティスでは、接続文字列をアプリケーション外の Azure Key Vault ドライブに保存し、アプリケーションに対して Key Vault キー、シークレット、証明書の適切なアクセス権を付与することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6f944-106">Security best practices recommend that you store connection strings outside applications, in an Azure Key Vault drive, and that you give applications the correct access to the key vault keys, secrets, or certificates.</span></span>

<span data-ttu-id="6f944-107">このアプローチの多くの利点のうち 2 つを次に示します。</span><span class="sxs-lookup"><span data-stu-id="6f944-107">Here are two of the many benefits of this approach:</span></span>

- <span data-ttu-id="6f944-108">アプリケーション データベースにアクセスできるユーザーは、サードパーティの接続文字列を取得できません。</span><span class="sxs-lookup"><span data-stu-id="6f944-108">Someone who gets access to the application database won't be able to get the third-party connection string.</span></span>
- <span data-ttu-id="6f944-109">特に複数のアプリケーションが同じリソースにアクセスする場合、更新する必要がある接続文字列が 1 か所だけなのでメンテナンスが簡単です。</span><span class="sxs-lookup"><span data-stu-id="6f944-109">Maintenance is easier, especially when multiple applications access the same resources, because you must update connection strings in only one place.</span></span>

<span data-ttu-id="6f944-110">完了する必要がある手順の概要を次に示します。</span><span class="sxs-lookup"><span data-stu-id="6f944-110">Here is an overview of the procedures that you must complete:</span></span>

1. <span data-ttu-id="6f944-111">新しい Service Bus の名前空間を作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-111">Create a new Service Bus namespace.</span></span>
2. <span data-ttu-id="6f944-112">新しい Service Bus のトピックとサブスクリプションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-112">Create a new Service Bus topic and subscription.</span></span>
3. <span data-ttu-id="6f944-113">Service Bus キーを格納する新しい Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-113">Create a new key vault to store the Service Bus key.</span></span>
4. <span data-ttu-id="6f944-114">Key Vault にアクセスするためのアクセス許可が与えられている Azure アプリを登録します。</span><span class="sxs-lookup"><span data-stu-id="6f944-114">Register an Azure app that has permission to access the key vault.</span></span>
5. <span data-ttu-id="6f944-115">ビジネス イベント エンドポイントをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="6f944-115">Configure a Business Events endpoint.</span></span>
6. <span data-ttu-id="6f944-116">ビジネス イベントを消費します。</span><span class="sxs-lookup"><span data-stu-id="6f944-116">Consume the business event.</span></span>

## <a name="create-a-new-service-bus-namespace"></a><span data-ttu-id="6f944-117">新しい Service Bus の名前空間を作成する</span><span class="sxs-lookup"><span data-stu-id="6f944-117">Create a new Service Bus namespace</span></span>

1. <span data-ttu-id="6f944-118">Azure ポータルにサインインします。</span><span class="sxs-lookup"><span data-stu-id="6f944-118">Sign in to the Azure portal.</span></span>
2. <span data-ttu-id="6f944-119">**すべてのサービス \> 統合 \> Service Bus** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-119">Select **All services \> Integration \> Service Bus**.</span></span>
3. <span data-ttu-id="6f944-120">**追加** を選択して新しい Service Bus の名前空間を作成し、パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f944-120">Select **Add** to create a new Service Bus namespace, and set the parameters.</span></span> <span data-ttu-id="6f944-121">**標準** の価格レベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-121">Select the **Standard** pricing tier.</span></span> <span data-ttu-id="6f944-122">ラボのコンテナーとして新しいリソース グループを作成するか、または既存のリソース グループを使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f944-122">You can create a new resource group as a container for your lab, or you can use an existing resource group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f944-123">**基本** 価格レベルを選択した場合、作成できるのはキューのみです。</span><span class="sxs-lookup"><span data-stu-id="6f944-123">If you select the **Basic** pricing tier, you can create only queues.</span></span> <span data-ttu-id="6f944-124">トピックを作成するには **標準** 価格帯を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-124">To create topics, you must select the **Standard** pricing tier.</span></span>

4. <span data-ttu-id="6f944-125">すべてのパラメーターの設定が終了したら **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-125">When you've finished setting all the parameters, select **Create**.</span></span>

## <a name="create-a-new-service-bus-topic-and-subscription"></a><span data-ttu-id="6f944-126">新しい Service Bus のトピックとサブスクリプションを作成</span><span class="sxs-lookup"><span data-stu-id="6f944-126">Create a new Service Bus topic and subscription</span></span>

1. <span data-ttu-id="6f944-127">Azure ポータルで、作成した Service Bus を選択して新しいトピックを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-127">In the Azure portal, select the Service Bus that you just created, and then create a new topic.</span></span>

   <img alt="Service Bus Topic" src="../../media/BEF-Howto-servicebus-03.png" width="70%">

2. <span data-ttu-id="6f944-128">新しいトピックを選択して **BE-USMF** という名前の新しいサブスクリプションを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-128">Select the new topic, and then create a new subscription that is named **BE-USMF**.</span></span>

    <img alt="Service Bus subscription" src="../../media/BEF-Howto-servicebus-04.png" width="70%">

3. <span data-ttu-id="6f944-129">Service Bus のブレードに戻り、イベントを送信する新しい共有アクセス ポリシーを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-129">Go back to the blade for your Service Bus, and create a new shared access policy to send events.</span></span> <span data-ttu-id="6f944-130">Service Bus のトピックにイベントを送信するには **送信** ポリシーのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f944-130">Only the **Send** policy is required to send events to the Service Bus topic.</span></span>

    <img alt="Service Bus Shared access policy" src="../../media/BEF-Howto-servicebus-05.png" width="70%">

4. <span data-ttu-id="6f944-131">新しい **送信** ポリシーを選択して **プライマリ接続文字列** 値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-131">Select the new **Send** policy, and then copy and save the **Primary Connection String** value.</span></span> <span data-ttu-id="6f944-132">この値は後で使用します。</span><span class="sxs-lookup"><span data-stu-id="6f944-132">You will use this value later.</span></span>

    <img alt="Service Bus connection string" src="../../media/BEF-Howto-servicebus-06.png" width="70%">

## <a name="create-a-new-key-vault"></a><span data-ttu-id="6f944-133">新しい Key Vault の作成</span><span class="sxs-lookup"><span data-stu-id="6f944-133">Create a new key vault</span></span>

<span data-ttu-id="6f944-134">この手順では、前の手順でコピーしたキーを保存する Key Vault を作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-134">In this procedure, you will create a key vault to store the key that you copied in the previous procedure.</span></span> <span data-ttu-id="6f944-135">Key Vault は、キー、シークレット、証明書を保存するために使用する安全なドライブです。</span><span class="sxs-lookup"><span data-stu-id="6f944-135">A key vault is a secure drive that is used to store keys, secrets, and certificates.</span></span> <span data-ttu-id="6f944-136">接続文字列を保存する代わりに、より一般的で安全なアプローチは Key Vault に保存することです。</span><span class="sxs-lookup"><span data-stu-id="6f944-136">Instead of storing the connection string, a more typical and more secure approach is to store it in a key vault.</span></span> <span data-ttu-id="6f944-137">その後、新しいアプリケーションを Azure Active Directory (Azure AD) に登録し、Key Vault からシークレットを取得する権限を付与できます。</span><span class="sxs-lookup"><span data-stu-id="6f944-137">You can then register a new application with Azure Active Directory (Azure AD) and grant it the right to retrieve the secret from the key vault.</span></span>

1. <span data-ttu-id="6f944-138">Azure ポータルで **すべてのサービス \> セキュリティ \> Key Vaults** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-138">In the Azure portal, select **All services \> Security \> Key vaults**.</span></span>
2. <span data-ttu-id="6f944-139">リソース グループに新しい Key Vault を作成し、デフォルトのパラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f944-139">Create a new key vault in your resource group and set the default parameters.</span></span>

    <img alt="New Key Vault" src="../../media/BEF-Howto-Keyvault-02.png" width="50%">

3. <span data-ttu-id="6f944-140">**概要** を選択し、Key Vault の **DNS 名** 値をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-140">Select **Overview**, then copy and save the **DNS Name** value for the key vault.</span></span> <span data-ttu-id="6f944-141">この値は後で使用します。</span><span class="sxs-lookup"><span data-stu-id="6f944-141">You will use this value later.</span></span>

    <img alt="Key vault DNS name" src="../../media/BEF-Howto-Keyvault-03.png" width="70%">

4. <span data-ttu-id="6f944-142">**BE-Key Vault \> シークレット \> 生成/インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-142">Select **BE-key vault \> Secrets \> Generate/Import**.</span></span> <span data-ttu-id="6f944-143">シークレットの名前を入力し、先に保存した Service Bus 接続文字列を貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="6f944-143">Enter a name for your secret, and paste the Service Bus connection string that you saved earlier.</span></span>

    <img alt="Key vault secret " src="../../media/BEF-Howto-Keyvault-04.png" width="70%">

5. <span data-ttu-id="6f944-144">**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-144">Select **Create**.</span></span>

## <a name="register-a-new-application"></a><span data-ttu-id="6f944-145">新しいアプリケーションの登録</span><span class="sxs-lookup"><span data-stu-id="6f944-145">Register a new application</span></span>

<span data-ttu-id="6f944-146">この手順では、新しいアプリケーションを Azure AD に登録して、Key Vault のシークレットの読み取りと取得アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="6f944-146">In this procedure, you will register a new application with Azure AD, and give it read and retrieve access to key vault secrets.</span></span> <span data-ttu-id="6f944-147">すると Finance and Operations はこのアプリケーションを使用して Service Bus シークレットを取得します。</span><span class="sxs-lookup"><span data-stu-id="6f944-147">Finance and Operations will then use this application to retrieve Service Bus secrets.</span></span>

1. <span data-ttu-id="6f944-148">Azure ポータルで **すべてのサービス \> セキュリティ \> Azure Active Directory** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-148">In the Azure portal, select **All services \> Security \> Azure Active Directory**.</span></span>
2. <span data-ttu-id="6f944-149">**アプリ登録 (プレビュー) \> 新しい登録** を選択し、アプリケーションの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f944-149">Select **App registrations (preview) \> New registration**, and enter a name for your application.</span></span>
3. <span data-ttu-id="6f944-150">**登録** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-150">Select **Register**.</span></span>
4. <span data-ttu-id="6f944-151">新しいアプリケーションを選択してから **証明書とシークレット \> 新しいクライアント シークレット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-151">Select the new application, and then select **Certificates & secrets \> New client secret**.</span></span> <span data-ttu-id="6f944-152">シークレットの名前を入力し、有効期限が切れないようにシークレットを設定します。</span><span class="sxs-lookup"><span data-stu-id="6f944-152">Enter a name for your secret, and set the secret so that it never expires.</span></span> <span data-ttu-id="6f944-153">その後 **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-153">Then select **Add**.</span></span>

    <img alt="Azure App secret " src="../../media/BEF-Howto-Keyvault-07.png" width="50%">

5. <span data-ttu-id="6f944-154">新しいシークレットをコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-154">Copy and save your new secret.</span></span> <span data-ttu-id="6f944-155">これは後で使用します。</span><span class="sxs-lookup"><span data-stu-id="6f944-155">You will use it later.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="6f944-156">シークレットは一度だけ表示されます。</span><span class="sxs-lookup"><span data-stu-id="6f944-156">Secrets are visible only one time.</span></span> <span data-ttu-id="6f944-157">シークレットをコピーし忘れた場合は、削除してから新しいシークレットを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-157">If you forget to copy the secret, you will have to delete it and create a new secret.</span></span>

    <img alt="Copy App secret " src="../../media/BEF-Howto-Keyvault-08.png" width="70%">

6. <span data-ttu-id="6f944-158">**概要** を選択し、アプリケーション ID をコピーして保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-158">Select **Overview**, and copy and save the application ID.</span></span> <span data-ttu-id="6f944-159">この値は後で使用します。</span><span class="sxs-lookup"><span data-stu-id="6f944-159">You will use this value later.</span></span>

    <img alt="Copy App ID " src="../../media/BEF-Howto-Keyvault-09.png" width="70%">

7. <span data-ttu-id="6f944-160">**すべてのサービス \> セキュリティ \> Key Vaults** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-160">Select **All services \> Security \> Key vaults**.</span></span>
8. <span data-ttu-id="6f944-161">前に作成した Key Vault を選択してから **アクセスポリシー \> 新規追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-161">Select the key vault that you created earlier, and then select **Access policies \> Add new**.</span></span>
9. <span data-ttu-id="6f944-162">**プリンシパル** ブレードで、新しい登録済みアプリケーションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-162">On the **Principal** blade, select your new registered application.</span></span> <span data-ttu-id="6f944-163">Key Vault のシークレットを取得するには、**Get** と **List** シークレット アクセス許可のチェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-163">Select the check boxes for the **Get** and **List** secret permissions to retrieve key vault secrets.</span></span>

    <img alt="Key Vault access policy " src="../../media/BEF-Howto-Keyvault-12.png" width="50%">

10. <span data-ttu-id="6f944-164">新しいアクセス ポリシーを保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-164">Save your new access policy.</span></span>

## <a name="configure-a-business-events-endpoint"></a><span data-ttu-id="6f944-165">ビジネス イベント エンドポイントのをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6f944-165">Configure a Business Events endpoint</span></span> 

1. <span data-ttu-id="6f944-166">アプリケーションにサイン インし、**システム管理** \> **設定** \> **ビジネス イベント**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f944-166">Sign in to the application and go to **System administration** \> **Setup** \> **Business events**.</span></span>
2. <span data-ttu-id="6f944-167">**エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-167">Select **Endpoints**.</span></span>
3. <span data-ttu-id="6f944-168">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-168">Select **New**.</span></span>
4. <span data-ttu-id="6f944-169">**Azure Service Bus のトピック** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-169">Select **Azure Service Bus Topic**.</span></span>
5. <span data-ttu-id="6f944-170">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-170">Select **Next**.</span></span>
6. <span data-ttu-id="6f944-171">必要なパラメーター値を設定します。</span><span class="sxs-lookup"><span data-stu-id="6f944-171">Set the required parameter values.</span></span>

    <img alt="Service Bus dndpoint" src="../../media/BEF-Howto-servicebus-08.png" width="70%">

7. <span data-ttu-id="6f944-172">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-172">Select **OK**.</span></span>

## <a name="consume-a-business-event"></a><span data-ttu-id="6f944-173">ビジネス イベントの消費</span><span class="sxs-lookup"><span data-stu-id="6f944-173">Consume a business event</span></span>

<span data-ttu-id="6f944-174">ビジネス シナリオは USMF 企業の顧客の支払いが転記されるたびに、電子メールやメッセージをチーム チャネルに送信します。</span><span class="sxs-lookup"><span data-stu-id="6f944-174">The business scenario involves sending an email or a message to a team channel whenever a customer payment is posted for the USMF company.</span></span> <span data-ttu-id="6f944-175">顧客アカウント番号、顧客名、支払い額などの詳細がメッセージ\`に含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-175">The message must contain details such as the customer account number, the customer name, and the amount of the payment.</span></span>

1. <span data-ttu-id="6f944-176">ビジネス イベント カタログを選択し、**顧客の支払が転記されました**ビジネス イベントを探します</span><span class="sxs-lookup"><span data-stu-id="6f944-176">Select the business event catalog and look for **customer payment posted** business event</span></span>
2. <span data-ttu-id="6f944-177">USMF 会社のビジネス イベントを有効化します。</span><span class="sxs-lookup"><span data-stu-id="6f944-177">Activate the business event for USMF company.</span></span>

    <img alt="Activate business event " src="../../media/BEF-Howto-servicebus-09.png" width="30%">

    <span data-ttu-id="6f944-178">新しい Service Bus エンドポイントを使用するビジネス イベントを有効化した後、アプリケーションはテスト メッセージを送信してコンフィギュレーションが正確であることを確認し、接続をキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="6f944-178">After you activate a business event that uses the new Service Bus endpoint, the application sends a test message to verify that the configuration is accurate and to cache the connection.</span></span>

3. <span data-ttu-id="6f944-179">テスト メッセージが受信されたことを確認するには Azure ポータルで **BE-Topic** Service Bus トピックを選択して、そして以前に作成した **BE-USMF** Service Bus サブスクリプションに入ります。</span><span class="sxs-lookup"><span data-stu-id="6f944-179">To verify that the test message has been received, in the Azure portal, select your **BE-Topic** Service Bus topic, and then go into the **BE-USMF** Service Bus subscription that you created earlier.</span></span> <span data-ttu-id="6f944-180">サブスクリプションのメッセージ数が少なくとも **1** の値を示していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f944-180">Verify that the message count for the subscription shows a value of at least **1**.</span></span> <span data-ttu-id="6f944-181">そうでない場合は、バッチジョブがメッセージを受信するまで待ちます。</span><span class="sxs-lookup"><span data-stu-id="6f944-181">If it doesn't, wait for the batch job to pick up your message.</span></span>

    <img alt="Service Bus message count" src="../../media/BEF-Howto-servicebus-10.png" width="70%">

3. <span data-ttu-id="6f944-182">**すべてのサービス \> 統合 \> ロジック アプリ** を順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-182">Select **All services \> Integration \> Logic Apps**.</span></span>

    <img alt="Logic apps" src="../../media/BEF-Howto-servicebus-11.png" width="70%">

4. <span data-ttu-id="6f944-183">リソース グループに新しいロジック アプリを作成します。</span><span class="sxs-lookup"><span data-stu-id="6f944-183">Create a new logic app in your resource group.</span></span>
5. <span data-ttu-id="6f944-184">ロジック アプリ リソースを作成したら、空のロジック アプリを作成するオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-184">After your Logic Apps resource has been created, select the option to create a blank logic app.</span></span>
6. <span data-ttu-id="6f944-185">**サービス バス** を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-185">Search for **Service Bus**, and select it.</span></span>
7. <span data-ttu-id="6f944-186">**トピック サブスクリプションでメッセージを受信した場合 (オート コンプリート)** という名前のトリガーを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-186">Select the trigger that is named **When a message is received in a topic subscription (auto-complete)**.</span></span>

    > [!NOTE] 
    > <span data-ttu-id="6f944-187">オート コンプリートとは、メッセージが取得された後にサブスクリプション キューから削除されることを意味します。</span><span class="sxs-lookup"><span data-stu-id="6f944-187">Auto-complete means that the message is deleted from the subscription queue after it's retrieved.</span></span> <span data-ttu-id="6f944-188">ピーク ロックは同時実行消費者を許可します。</span><span class="sxs-lookup"><span data-stu-id="6f944-188">Peek-lock authorizes concurrent consumers.</span></span> <span data-ttu-id="6f944-189">メッセージを削除するには、Service Bus アプリケーション プログラミング インターフェイス (API) の **完了** コマンドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-189">It requires a call to the **complete** command of the Service Bus application programming interface (API) in order to delete the message.</span></span>

    <span data-ttu-id="6f944-190">ロジック アプリは初めて Service Bus にアクセスするために新しい接続を要求します。</span><span class="sxs-lookup"><span data-stu-id="6f944-190">Because Logic Apps is accessing your Service Bus for the first time, it asks for a new connection.</span></span> <span data-ttu-id="6f944-191">この接続は、接続の詳細を Service Bus 名前空間の URL と資格情報としてキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="6f944-191">This connection will cache connection details as a Service Bus namespace URL and credential.</span></span>

8. <span data-ttu-id="6f944-192">Service Bus 名前空間を選択して新しい接続の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f944-192">Select your Service Bus namespace, and enter a name for the new connection.</span></span>
9. <span data-ttu-id="6f944-193">ロジック アプリの **RootManageSharedAccessKey** ポリシーを選択して **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-193">Select the **RootManageSharedAccessKey** policy for your logic app, and then select **Create**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f944-194">メッセージを送信するのではなく*取得* する必要があるため **送信** ポリシーをここで使用できません。</span><span class="sxs-lookup"><span data-stu-id="6f944-194">The **Send** policy can't be used here, because you want to *retrieve* messages, not send them.</span></span> <span data-ttu-id="6f944-195">ベスト プラクティスとして、このユース ケースに新しいポリシーを作成して **リッスン** アクセス許可のみを付与できます。</span><span class="sxs-lookup"><span data-stu-id="6f944-195">As a best practice, you could have created a new policy for this use case and given it **Listen** permission only.</span></span>

    <img alt="Service bus listen policy " src="../../media/BEF-Howto-servicebus-16.png" width="70%">

10. <span data-ttu-id="6f944-196">トリガー パラメーターを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-196">Select your trigger parameters.</span></span> <span data-ttu-id="6f944-197">作成したトピックとサブスクリプションに必ず正しい名前を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f944-197">Be sure to use the correct names for the topic and subscription that you created.</span></span>

    <span data-ttu-id="6f944-198">この API はコンフィギュレーション可能な頻度で、新しいメッセージの Service Bus をポーリングします (既定は 3 分ごと)。</span><span class="sxs-lookup"><span data-stu-id="6f944-198">This API polls Service Bus for new messages at a configurable recurrence (by default, every three minutes).</span></span> <span data-ttu-id="6f944-199">ロジック アプリはトリガーの呼び出しとアクションの実行ごとに課金されるため、メッセージの量が少ない場合に API は不要なトリガーのコストに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="6f944-199">If the volume of messages is low, the API will have a cost impact for unnecessary triggers, because Logic Apps is priced per trigger call and action run.</span></span> <span data-ttu-id="6f944-200">ただし、途中で Azure Event Grid を使用するプッシュ アーキテクチャを実装できます。</span><span class="sxs-lookup"><span data-stu-id="6f944-200">However, you can implement a push architecture that uses Azure Event Grid in the middle.</span></span> <span data-ttu-id="6f944-201">キューやサブスクリプションにメッセージがある場合、Service Bus はイベントをイベント グリッドにプッシュできます。</span><span class="sxs-lookup"><span data-stu-id="6f944-201">Service Bus can then push events to Event Grid when there are messages in a queue or a subscription.</span></span> <span data-ttu-id="6f944-202">詳細については [Azure Service Bus からイベント グリッドへの統合の概要](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-to-event-grid-integration-concept) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f944-202">For more information, see [Azure Service Bus to Event Grid integration overview](https://docs.microsoft.com/azure/service-bus-messaging/service-bus-to-event-grid-integration-concept).</span></span>

    <img alt="Logic apps trigger " src="../../media/BEF-Howto-servicebus-17.png" width="70%">

11. <span data-ttu-id="6f944-203">**新規ステップ** を選択して新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="6f944-203">Select **New step** to add a new action.</span></span>
12. <span data-ttu-id="6f944-204">**JSON の解析** データ処理を検索します。</span><span class="sxs-lookup"><span data-stu-id="6f944-204">Search for the **Parse Json** data operation.</span></span> <span data-ttu-id="6f944-205">このステップは、データ コントラクトのスキーマを使用してメッセージを解析するために必要です。</span><span class="sxs-lookup"><span data-stu-id="6f944-205">This step is required so that the message can be parsed by using the schema of the data contract.</span></span>

    <span data-ttu-id="6f944-206">Service Bus から受信した本文コンテンツは base64 形式にエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="6f944-206">The body content that is received from the Service Bus is encoded into base64 format.</span></span> <span data-ttu-id="6f944-207">したがって、JavaScript Object Notation (JSON) ペイロードを解析する前に文字列形式に変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-207">Therefore, you must transform it to string format before the JavaScript Object Notation (JSON) payload can be parsed.</span></span> 

13. <span data-ttu-id="6f944-208">**コンテンツ** フィールドをクリックし、表示されたウィンドウの **式** タブに次の式を入力します: **Base64ToString()**</span><span class="sxs-lookup"><span data-stu-id="6f944-208">Click in the **Content** field, and then, in the pane that appears, on the **Expression** tab, enter the following expression: **Base64ToString()**</span></span>

    <img alt="base64ToString " src="../../media/BEF-Howto-servicebus-19.png" width="70%">

14. <span data-ttu-id="6f944-209">式の括弧の間にカーソルを置き、**動的コンテンツ** タブで前の Service Bus トリガーから **メッセージのコンテンツ** コンテンツを見つけて選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-209">Put the cursor between the parentheses in the expression, and then, on the **Dynamic content** tab, find and select the **Content of the message** content from the previous Service Bus trigger.</span></span> <span data-ttu-id="6f944-210">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-210">Then select **OK**.</span></span>

    <img alt="Service Bus message body " src="../../media/BEF-Howto-servicebus-20.png" width="50%">

    <span data-ttu-id="6f944-211">次に、アプリケーションから受け取った契約のスキーマを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f944-211">Next, you must enter the schema of the contract that is received from the application.</span></span> <span data-ttu-id="6f944-212">アプリケーションでは、サンプル ペイロードのみ提供します。</span><span class="sxs-lookup"><span data-stu-id="6f944-212">The application only provides a sample payload.</span></span> <span data-ttu-id="6f944-213">ただし、Azure ロジック アプリの機能を使用してペイロードからスキーマを生成できます。</span><span class="sxs-lookup"><span data-stu-id="6f944-213">However, you can use a capability of Azure Logic Apps to generate a schema from a payload.</span></span>

15. <span data-ttu-id="6f944-214">ビジネス イベント カタログのイベントを選択し、**スキーマのダウンロード**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-214">Select your event in the business event catalog, and then select the **Download schema** link.</span></span> <span data-ttu-id="6f944-215">ダウンロードしたテキスト ファイルを開いて内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="6f944-215">Open the text file that is downloaded, and copy the contents.</span></span>
16. <span data-ttu-id="6f944-216">ロジック アプリに戻って **サンプル ペイロードを使用してスキーマを生成** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-216">Go back to your Logic Apps, and select the **Use sample payload to generate schema** link.</span></span> <span data-ttu-id="6f944-217">テキスト ファイルの内容を貼り付けて **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-217">Paste the contents of the text file, and then select **Done**.</span></span>

    <img alt="Message schema " src="../../media/BEF-Howto-servicebus-22.png" width="70%">

17. <span data-ttu-id="6f944-218">サンプル ペイロードの品質により、特に実値がサンプル ペイロードで整数として与えられた場合、ジェネレーターは整数と実値を区別しません。</span><span class="sxs-lookup"><span data-stu-id="6f944-218">Depending on the quality of your sample payload, your generator won't be able to distinguish between an integer and a real value, especially if the real value is provided as a whole number in the sample payload.</span></span> <span data-ttu-id="6f944-219">生成されたスキーマを確認して **整数** データ型のフィールドを **数値** データ型に変更する必要があるか判断します。</span><span class="sxs-lookup"><span data-stu-id="6f944-219">Review the schema that is generated, and determine whether you must change a field of the **integer** data type to the **number** data type.</span></span> <span data-ttu-id="6f944-220">(JSON で **数値** データ型は実値を表します。)</span><span class="sxs-lookup"><span data-stu-id="6f944-220">(In JSON, the **number** data type represents real values.)</span></span>

    <img alt="JSON data types " src="../../media/BEF-Howto-servicebus-23.png" width="70%">

    <span data-ttu-id="6f944-221">次に、顧客の支払いの詳細を含む通知電子メールの送信など、最終的なアクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f944-221">Next, you will select a final action, such as sending a notification email that includes customer payment details.</span></span>

18. <span data-ttu-id="6f944-222">**電子メールの送信** アクションを検索し、自分の Microsoft Office 365 アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="6f944-222">Search for the **send email** action, and then sign in to your Microsoft Office 365 account.</span></span>
19. <span data-ttu-id="6f944-223">メッセージの本文および、必須項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f944-223">Fill in the message with the required fields.</span></span>

    <img alt="Logic apps action send email " src="../../media/BEF-Howto-servicebus-25.png" width="70%">

20. <span data-ttu-id="6f944-224">ロジック アプリを保存します。</span><span class="sxs-lookup"><span data-stu-id="6f944-224">Save your logic app.</span></span>
21. <span data-ttu-id="6f944-225">顧客の支払いを転記して、ビジネス イベントをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="6f944-225">Trigger the business event by posting a customer payment.</span></span> <span data-ttu-id="6f944-226">そして、ロジック アプリが実行されていること、顧客の支払いの詳細が記載された電子メールを受信することを確認します。</span><span class="sxs-lookup"><span data-stu-id="6f944-226">Then verify that the logic app runs, and that you receive an email that includes customer payment details.</span></span>
