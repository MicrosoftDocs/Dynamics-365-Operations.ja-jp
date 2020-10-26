---
title: トレーニング用の更新
description: このトピックでは、Microsoft Dynamics 365 Finance の汎用データベースの更新シナリオについて説明します。
author: LaneSwenka
manager: AnnBe
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 3e5f778cd713c968028d8496f6ad7c238d2cf6a9
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982781"
---
# <a name="refresh-for-training-purposes"></a><span data-ttu-id="42545-103">トレーニング用の更新</span><span class="sxs-lookup"><span data-stu-id="42545-103">Refresh for training purposes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42545-104">データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。</span><span class="sxs-lookup"><span data-stu-id="42545-104">Database movement operations are a suite of self-service actions that can be used as part of data application lifecycle management (DataALM).</span></span> <span data-ttu-id="42545-105">このチュートリアルでは、トレーニング シナリオでデータベース更新操作の使用方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="42545-105">This tutorial shows how to use the refresh database operation in a training scenario.</span></span>

<span data-ttu-id="42545-106">このチュートリアルでは、次の方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="42545-106">In this tutorial, you will learn how to:</span></span>

> [!div class="checklist"]
> * <span data-ttu-id="42545-107">ターゲット環境を準備します。</span><span class="sxs-lookup"><span data-stu-id="42545-107">Prepare the target environment.</span></span>
> * <span data-ttu-id="42545-108">更新を実行します。</span><span class="sxs-lookup"><span data-stu-id="42545-108">Run the refresh.</span></span>
> * <span data-ttu-id="42545-109">ターゲット環境を再構成します。</span><span class="sxs-lookup"><span data-stu-id="42545-109">Reconfigure the target environment.</span></span>
> * <span data-ttu-id="42545-110">選択したユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="42545-110">Enable selected users.</span></span>

<span data-ttu-id="42545-111">このシナリオの例として、アプリケーションを既に稼働している顧客が、ユーザー受け入れテスト (UAT) 環境に生産トランザクションの最新のコピーを読み込むということがあります。</span><span class="sxs-lookup"><span data-stu-id="42545-111">As an example of this scenario, a customer who has already gone live with the application wants to load a recent copy of production transactions into the user acceptance testing (UAT) environment.</span></span> <span data-ttu-id="42545-112">このようにして、顧客は、新しい従業員のトレーニングをサポートし、実際の環境に影響を与えずに構成の変更を評価できます。</span><span class="sxs-lookup"><span data-stu-id="42545-112">In this way, the customer can support training of new employees and evaluate configuration changes without affecting the live environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="42545-113">必要条件</span><span class="sxs-lookup"><span data-stu-id="42545-113">Prerequisites</span></span>

<span data-ttu-id="42545-114">データベース更新操作を行うには、実稼働環境を配置する必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="42545-114">To do a refresh database operation, your production environment must be deployed, or you must have a minimum of two standard UAT environments.</span></span>

## <a name="notify-users-about-the-pending-downtime"></a><span data-ttu-id="42545-115">保留中のダウンタイムについてユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="42545-115">Notify users about the pending downtime</span></span>

<span data-ttu-id="42545-116">作業の大部分を開始する前に、環境が一定期間オフラインになる対象となる環境についてユーザーに通知します。</span><span class="sxs-lookup"><span data-stu-id="42545-116">Before you start the bulk of the work, notify users of the target environment that the environment will be offline for a period.</span></span> <span data-ttu-id="42545-117">Microsoft Dynamics Lifecycle Services (LCS) から手動で、または RESTful アプリケーション プログラミング インターフェイス (API) 呼び出しを使用してプログラムによりユーザーに通知できます。</span><span class="sxs-lookup"><span data-stu-id="42545-117">You can notify users either manually via Microsoft Dynamics Lifecycle Services (LCS) or programmatically by using RESTful application programming interface (API) calls.</span></span>

### <a name="manually-send-a-broadcast-message"></a><span data-ttu-id="42545-118">手動でブロードキャスト メッセージを送信</span><span class="sxs-lookup"><span data-stu-id="42545-118">Manually send a broadcast message</span></span>

<span data-ttu-id="42545-119">LCS を通して手動でユーザーに通知するには、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="42545-119">To notify users manually via LCS, follow these steps.</span></span>

1. <span data-ttu-id="42545-120">LCS で、ターゲット環境の **環境の詳細** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="42545-120">In LCS, open the **Environment details** page for the target environment.</span></span>
2. <span data-ttu-id="42545-121">**管理**\>**オンライン ユーザーにメッセージ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42545-121">Select **Maintain** \> **Message online users**.</span></span>
3. <span data-ttu-id="42545-122">**ダウンタイムに関する新しいメッセージの配信**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42545-122">Select **Broadcast a new message for downtime**.</span></span>
4. <span data-ttu-id="42545-123">ローカル タイム ゾーンで有効開始/有効終了の時刻を選択します。</span><span class="sxs-lookup"><span data-stu-id="42545-123">Select the valid from/valid to times in your local time zone.</span></span>
5. <span data-ttu-id="42545-124">**投稿**を選択します。</span><span class="sxs-lookup"><span data-stu-id="42545-124">Select **Post**.</span></span>

### <a name="programmatically-send-a-broadcast-message"></a><span data-ttu-id="42545-125">プログラムによりブロードキャスト メッセージを送信</span><span class="sxs-lookup"><span data-stu-id="42545-125">Programmatically send a broadcast message</span></span>

<span data-ttu-id="42545-126">次のサンプル コードをコンソール アプリケーションに示されたとおりに使用するか、Microsoft Azure の機能など、オンデマンドで呼び出せる他のサービスと連携するように変更できます。</span><span class="sxs-lookup"><span data-stu-id="42545-126">The following sample code can be used as shown in a console application, or it can be modified to make it work with other services that can be called on demand, such as Microsoft Azure Functions.</span></span> <span data-ttu-id="42545-127">このサンプル コードが動作するには、 [サービス エンドポイントの概要](../data-entities/services-home-page.md)に記載の説明に従ってアプリケーション登録を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42545-127">Before this sample code will work, you must set up your application registration as described in [Service endpoints overview](../data-entities/services-home-page.md).</span></span>

```csharp
[Serializable]
public class SysAddBroadcastMessageDataContract
{
    public SysAddBroadcastMessageRequest request { get; set; }
}
[Serializable]
public class SysAddBroadcastMessageRequest
{
    public DateTime FromDateTime { get; set; }
    public DateTime ToDateTime { get; set; }
}
public class Program
{
    public static AuthenticationResult getResult(AuthenticationContext ctx, string url)
    {
        return ctx.AcquireTokenAsync(url, "YOUR_APP_REGISTRATION_ID", new Uri("YOUR_REPLY_URL"), new PlatformParameters(PromptBehavior.Always)).Result;
    }
    static void Main(string[] args)
    {
        SysAddBroadcastMessageRequest request = new SysAddBroadcastMessageRequest();
        request.FromDateTime = DateTime.UtcNow;
        request.ToDateTime = DateTime.UtcNow.AddHours(12);

        SysAddBroadcastMessageDataContract dc = new SysAddBroadcastMessageDataContract();
        dc.request = request;

        AuthenticationContext ctx = new AuthenticationContext("https://login.microsoftonline.com/YOUR_TENANT.COM");
        AuthenticationResult res = getResult(ctx, "https://YOUR_SANDBOX_UAT.sandbox.operations.dynamics.com");

        HttpClient restfulCli = new HttpClient();
        restfulCli.DefaultRequestHeaders.Clear();
        restfulCli.BaseAddress = new Uri("https://YOUR_SANDBOX_UAT.sandbox.operations.dynamics.com/");
        restfulCli.DefaultRequestHeaders.Add("Authorization", res.CreateAuthorizationHeader());
        restfulCli.DefaultRequestHeaders.Accept.Add(new MediaTypeWithQualityHeaderValue("application/json"));

        HttpRequestMessage requestMsg = new HttpRequestMessage(HttpMethod.Post, string.Format("api/services/SysBroadcastMessageServices/SysBroadcastMessageService/AddMessage"));
        requestMsg.Content = new StringContent(JsonConvert.SerializeObject(dc));

        HttpResponseMessage responseMsg = restfulCli.SendAsync(requestMsg).Result;
        if(responseMsg.IsSuccessStatusCode)
        {
            Console.WriteLine("Wow I just notified the users programmatically!");
        }
    }
```

<span data-ttu-id="42545-128">どちらの方法でも (LCS 経由の手動、RESTful API 呼び出しでプログラムにより)、ダウンタイムの期間が保留中であることがユーザーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="42545-128">Both approaches, manual via LCS and programmatic via RESTful API calls, will show users that a period of downtime is pending.</span></span>

<img src="media/BroadcastMessage.png" width="400px" alt="Broadcast message of downtime" />

## <a name="begin-the-refresh"></a><span data-ttu-id="42545-129">更新の開始</span><span class="sxs-lookup"><span data-stu-id="42545-129">Begin the refresh</span></span>

<span data-ttu-id="42545-130">ソース環境の規模によっては、即座に更新プロセスを開始することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42545-130">Depending on the size of your source environment, it might make sense to begin the refresh process immediately.</span></span> <span data-ttu-id="42545-131">ソース データベースが大きいほど、ターゲット Azure SQL データベース インスタンスへのコピーに時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="42545-131">The larger the source database, the longer it will take to copy to your target Azure SQL Database instance.</span></span> <span data-ttu-id="42545-132">コピーの進行中も、対象となる環境はオンラインになります。</span><span class="sxs-lookup"><span data-stu-id="42545-132">While the copy is in progress, the target environment will still be online.</span></span> <span data-ttu-id="42545-133">コピーが完了した後、ダウンタイムが開始されます。</span><span class="sxs-lookup"><span data-stu-id="42545-133">The downtime will start after the copy is completed.</span></span>

<span data-ttu-id="42545-134">このプロセスは、LCS 経由で手動で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="42545-134">This process can be done manually via LCS.</span></span> <span data-ttu-id="42545-135">最新の手順については、 [データベースの更新](database-refresh.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="42545-135">For the latest steps, see [Refresh database](database-refresh.md).</span></span> <span data-ttu-id="42545-136">LCS の将来のリリースでは、RESTful API 経由でこのプロセスがトリガーすることもできるようになります。</span><span class="sxs-lookup"><span data-stu-id="42545-136">In a future release of LCS, you will also be able to trigger this process via a RESTful API.</span></span>

## <a name="reconfigure-environment-specific-settings"></a><span data-ttu-id="42545-137">環境の固有の設定を変更</span><span class="sxs-lookup"><span data-stu-id="42545-137">Reconfigure environment specific settings</span></span>

<span data-ttu-id="42545-138">更新が完了した後、LCS で**サインオフ** ボタンを使用し、操作を閉じます。</span><span class="sxs-lookup"><span data-stu-id="42545-138">After the refresh is completed, use the **Sign off** button in LCS to close out of the operation.</span></span> <span data-ttu-id="42545-139">その後、環境固有の設定のコンフィギュレーションを開始できます。</span><span class="sxs-lookup"><span data-stu-id="42545-139">You can then start to configure the environment-specific settings.</span></span>

<span data-ttu-id="42545-140">まず、環境にログインします。LCS の**環境の詳細**ページにある管理者アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="42545-140">First, sign in to the environment by using the admin account that can be found on the **Environment details** page in LCS.</span></span> <span data-ttu-id="42545-141">再設定の標準的な領域を次に示します。</span><span class="sxs-lookup"><span data-stu-id="42545-141">Here are typical areas of reconfiguration.</span></span> <span data-ttu-id="42545-142">設定およびインストールされている独立系ソフトウェア ベンダー (ISV) ソリューションによっては、追加の再設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="42545-142">You might require additional reconfiguration, based on your setup and the independent software vendor (ISV) solutions that are installed.</span></span>

* <span data-ttu-id="42545-143">**システム管理**\>**設定**\>**バッチ グループ:** 必要なバッチ サーバー グループにさまざまなアプリケーション おぶじぇくと サーバー (AOS) インスタンスを追加します。</span><span class="sxs-lookup"><span data-stu-id="42545-143">**System administration** \> **Setup** \> **Batch groups:** Add the various Application Object Server (AOS) instances to the batch server groups that you require.</span></span>
* <span data-ttu-id="42545-144">**システム管理**\>**設定**\>**エンティティ店舗:** Microsoft Power BI レポートに必要なさまざまなエンティティを更新します。</span><span class="sxs-lookup"><span data-stu-id="42545-144">**System administration** \> **Setup** \> **Entity Store:** Refresh the various entities that you require for Microsoft Power BI reporting.</span></span>
* <span data-ttu-id="42545-145">**システム管理**\>**設定**\>**システム パラメーター:** タスク ガイドの LCS ヘルプ コンフィギュレーションに環境を再接続します。</span><span class="sxs-lookup"><span data-stu-id="42545-145">**System administration** \> **Setup** \> **System parameters:** Reconnect the environment to the LCS Help configuration for task guides.</span></span>
* <span data-ttu-id="42545-146">**システム管理**\>**設定**\>**電子メール**\>**パラメータを電子メールで送信:** UAT 環境内で電子メールを使用する場合は、簡易メール転送プロトコル (SMTP) の設定を入力します。</span><span class="sxs-lookup"><span data-stu-id="42545-146">**System administration** \> **Setup** \> **Email** \> **Email parameters:** Enter the Simple Mail Transfer Protocol (SMTP) settings if you use email in your UAT environment.</span></span>
* <span data-ttu-id="42545-147">**システム管理**\>**照会**\>**バッチ ジョブ:** UAT 環境で実行するジョブを選択し、ステータスを **待機中** に更新します。</span><span class="sxs-lookup"><span data-stu-id="42545-147">**System administration** \> **Inquiries** \> **Batch jobs:** Select the jobs that you want to run in your UAT environment, and update the status to **Waiting**.</span></span>

<span data-ttu-id="42545-148">この再設定をより迅速に完了するには、更新が完了した後に必要に応じて呼び出すことができるカスタム Web サービス エンドポイントを構築することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="42545-148">To complete this reconfiguration more quickly, we recommend that you build a custom web service endpoint that can be called on demand after the refresh is completed.</span></span> <span data-ttu-id="42545-149">この種類の Web サービスの例は、このトピックの将来の更新で追加されます。</span><span class="sxs-lookup"><span data-stu-id="42545-149">An example of this type of web service will be added in a future update of this topic.</span></span>

## <a name="open-the-environment-to-users"></a><span data-ttu-id="42545-150">ユーザーに環境を開く</span><span class="sxs-lookup"><span data-stu-id="42545-150">Open the environment to users</span></span>

<span data-ttu-id="42545-151">必要に応じて、システムを構成する場合は、選択したユーザーが環境にアクセスできるようにできます。</span><span class="sxs-lookup"><span data-stu-id="42545-151">When the system is configured as you require, you can enable selected users to let them access the environment.</span></span> <span data-ttu-id="42545-152">デフォルトでは、管理者と Microsoft サービス アカウントを除くすべてのユーザーが無効になります。</span><span class="sxs-lookup"><span data-stu-id="42545-152">By default, all users except the admin and Microsoft service accounts are disabled.</span></span>

<span data-ttu-id="42545-153">**システム管理**\>**ユーザー**\>**ユーザー** に移動し、UAT 環境へのアクセスが必要なユーザーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="42545-153">Go to **System administration** \> **Users** \> **Users**, and enable the users that should have access to the UAT environment.</span></span> <span data-ttu-id="42545-154">多くのユーザーを有効にする必要がある場合、[Microsoft Excel アドイン](../office-integration/use-excel-add-in.md)を使用してこのタスクをすばやく完了できます。</span><span class="sxs-lookup"><span data-stu-id="42545-154">If many users must be enabled, you can complete this task more quickly by using the [Microsoft Excel Add-In](../office-integration/use-excel-add-in.md).</span></span>
