---
title: トレーニング用の更新
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations の汎用データベース更新シナリオについて説明します。
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
ms.author: laneswenka
ms.search.validFrom: 2019-01-31
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 356e91d9a095531fb9b16ec475d0a160ed5add61
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537093"
---
# <a name="refresh-for-training-purposes"></a>トレーニング用の更新

[!include [banner](../includes/banner.md)]

データベース移動操作は、データ アプリケーション ライフ サイクル管理 (DataALM) の一部として使用できる一連のセルフ サービスのアクションです。 このチュートリアルでは、トレーニング シナリオでデータベース更新操作の使用方法を説明します。

このチュートリアルでは、次の方法について説明します。

> [!div class="checklist"]
> * ターゲット環境を準備します。
> * 更新を実行します。
> * ターゲット環境を再構成します。
> * 選択したユーザーを有効にします。

このシナリオの例として、Microsoft Dynamics 365 for Finance and Operations を既に稼働している顧客が、ユーザー受け入れテスト (UAT) 環境に生産トランザクションの最新のコピーを読み込もうとしています。 このようにして、顧客は、新しい従業員のトレーニングをサポートし、実際の環境に影響を与えずに構成の変更を評価できます。

## <a name="prerequisites"></a>必要条件

データベース更新操作を行うには、実稼働環境を配置する必要があります。または標準的な UAT 環境を 2 つ以上持つ必要があります。

## <a name="notify-users-about-the-pending-downtime"></a>保留中のダウンタイムについてユーザーに通知します。

作業の大部分を開始する前に、環境が一定期間オフラインになる対象となる環境についてユーザーに通知します。 Microsoft Dynamics Lifecycle Services (LCS) から手動で、または RESTful アプリケーション プログラミング インターフェイス (API) 呼び出しを使用してプログラムによりユーザーに通知できます。

### <a name="manually-send-a-broadcast-message"></a>手動でブロードキャスト メッセージを送信

LCS を通して手動でユーザーに通知するには、以下の手順を実行します。

1. LCS で、ターゲット環境の **環境の詳細** ページを開きます。
2. **管理**\>**オンライン ユーザーにメッセージ**を選択します。
3. **ダウンタイムに関する新しいメッセージの配信**を選択します。
4. ローカル タイム ゾーンで有効開始/有効終了の時刻を選択します。
5. **投稿**を選択します。

### <a name="programmatically-send-a-broadcast-message"></a>プログラムによりブロードキャスト メッセージを送信

次のサンプル コードをコンソール アプリケーションに示されたとおりに使用するか、Microsoft Azure の機能など、オンデマンドで呼び出せる他のサービスと連携するように変更できます。 このサンプル コードが動作するには、[カスタム サービスの認証方法](../data-entities/services-home-page.md)の説明に従ってアプリケーション登録を設定する必要があります。

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

どちらの方法でも (LCS 経由の手動、RESTful API 呼び出しでプログラムにより)、ダウンタイムの期間が保留中であることがユーザーに表示されます。

<img src="media/BroadcastMessage.png" width="400px" alt="Broadcast message of downtime" />

## <a name="begin-the-refresh"></a>更新の開始

ソース環境の規模によっては、即座に更新プロセスを開始することをお勧めします。 ソース データベースが大きいほど、ターゲット Azure SQL データベース インスタンスへのコピーに時間がかかります。 コピーの進行中も、対象となる環境はオンラインになります。 コピーが完了した後、ダウンタイムが開始されます。

このプロセスは、LCS 経由で手動で行うことができます。 最新の手順については、[データベースの更新クイックスタート](database-refresh.md)を参照してください。 LCS の将来のリリースでは、RESTful API 経由でこのプロセスがトリガーすることもできるようになります。

## <a name="reconfigure-environment-specific-settings"></a>環境の固有の設定を変更

更新が完了した後、LCS で**サインオフ** ボタンを使用し、操作を閉じます。 その後、環境固有の設定のコンフィギュレーションを開始できます。

まず、環境にログインします。LCS の**環境の詳細**ページにある管理者アカウントを使用します。 再設定の標準的な領域を次に示します。 設定およびインストールされている独立系ソフトウェア ベンダー (ISV) ソリューションによっては、追加の再設定が必要です。

* **システム管理**\>**設定**\>**バッチ グループ:** 必要なバッチ サーバー グループにさまざまなアプリケーション おぶじぇくと サーバー (AOS) インスタンスを追加します。
* **システム管理**\>**設定**\>**エンティティ店舗:** Microsoft Power BI レポートに必要なさまざまなエンティティを更新します。
* **システム管理**\>**設定**\>**システム パラメーター:** タスク ガイドの LCS ヘルプ コンフィギュレーションに環境を再接続します。
* **システム管理**\>**設定**\>**電子メール**\>**パラメータを電子メールで送信:** UAT 環境内で電子メールを使用する場合は、簡易メール転送プロトコル (SMTP) の設定を入力します。
* **システム管理**\>**照会**\>**バッチ ジョブ:** UAT 環境で実行するジョブを選択し、ステータスを **待機中** に更新します。

この再設定をより迅速に完了するには、更新が完了した後に必要に応じて呼び出すことができるカスタム Web サービス エンドポイントを構築することをお勧めします。 この種類の Web サービスの例は、このトピックの将来の更新で追加されます。

## <a name="open-the-environment-to-users"></a>ユーザーに環境を開く

必要に応じて、システムを構成する場合は、選択したユーザーが環境にアクセスできるようにできます。 デフォルトでは、管理者と Microsoft サービス アカウントを除くすべてのユーザーが無効になります。

**システム管理**\>**ユーザー**\>**ユーザー** に移動し、UAT 環境へのアクセスが必要なユーザーを有効にします。 多くのユーザーを有効にする必要がある場合、[Microsoft Excel アドイン](../office-integration/use-excel-add-in.md)を使用してこのタスクをすばやく完了できます。
