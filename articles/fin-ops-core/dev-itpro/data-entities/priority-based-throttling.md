---
title: 優先順位に基づく調整
description: このトピックでは、OData およびカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。
author: hasaid
ms.date: 05/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 42255f78a8596523ba4989b3fe217b7a6b01d07e
ms.sourcegitcommit: 905a8c7a0c1bc06ada2acfba913dfe5f7b44ea16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/14/2021
ms.locfileid: "6039753"
---
# <a name="priority-based-throttling"></a><span data-ttu-id="d92f3-103">優先順位に基づく調整</span><span class="sxs-lookup"><span data-stu-id="d92f3-103">Priority-based throttling</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="d92f3-104">優先順位に基づく調整は、Dynamics 365 Finance バージョン 10.0.19 から既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="d92f3-104">Priority-based throttling is enabled by default starting in Dynamics 365 Finance version 10.0.19.</span></span> <span data-ttu-id="d92f3-105">バージョン 10.0.19 に更新する前に環境を準備する方法については [FAQ ドキュメント](throttling-faq.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d92f3-105">To learn about how you can prepare your environment prior to updating to  version 10.0.19, see [FAQ document](throttling-faq.md).</span></span> <span data-ttu-id="d92f3-106">この機能をテストするには、**調整優先順位マッピング** ページで統合優先順位をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="d92f3-106">To test this capability, configure the integration priorities on the **Throttling priority mapping** page.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="d92f3-107">[KB 4615823](https://fix.lcs.dynamics.com/Issue/Details?kb=4615823&bugId=560394&dbType=3&qc=bdc60364311159f2509ed641a0d858a46b5c57effbae2ffe778cd41f2109f7e9) には優先順位に基づく調整エクスペリエンスに直接影響する 2 つの重要な修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d92f3-107">[KB 4615823](https://fix.lcs.dynamics.com/Issue/Details?kb=4615823&bugId=560394&dbType=3&qc=bdc60364311159f2509ed641a0d858a46b5c57effbae2ffe778cd41f2109f7e9) includes two important fixes that directly impact the priority-based throttling experience.</span></span> 
> 
> <span data-ttu-id="d92f3-108">この修正により、環境内で調整イベントが発生した場合に 429 HTTP メッセージが送信され、そのイベントが環境に対する正しいしきい値の計算を反映するようにします。</span><span class="sxs-lookup"><span data-stu-id="d92f3-108">This fix ensures that 429 HTTP messages are sent when a throttling event occurs in your environment and that the events reflect the correct threshold calculations for your environment.</span></span> 
>
> <span data-ttu-id="d92f3-109">この修正は、品質更新プログラム 10.0.17 の一部として利用できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-109">The fix is available as part of the quality update for 10.0.17.</span></span> <span data-ttu-id="d92f3-110">このバージョンをインストールして、環境に対して優先順位に基づく調整を行う準備ができていることを確認するようお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d92f3-110">We recommend you install this version to ensure that your environment is ready for priority-based throttling.</span></span>

<span data-ttu-id="d92f3-111">優先順位に基づく調整により、サービス保護設定を導入し、リソースの過剰使用率を回避してシステムの応答性を維持し、Finance and Operations アプリを実行する環境において一貫した可用性とパフォーマンスを確保できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-111">Priority-based throttling introduces service protection settings that prevent the over-utilization of resources to preserve the system's responsiveness and ensure consistent availability and performance for environments running Finance and Operations apps.</span></span>


<span data-ttu-id="d92f3-112">優先順位に基づく調整では、ビジネスにとって重要なこれらの統合の必要性に応じて、OData とカスタム サービス ベース統合の相対的な優先順位を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-112">You have the ability to set relative priority for the OData and custom service-based integrations, depending on your business-critical need for these integrations.</span></span> <span data-ttu-id="d92f3-113">調整マネージャーは、これらの要求に対して設定されたこれらの優先順位を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-113">The throttling manager will then honor these priorities set for these requests.</span></span>

- <span data-ttu-id="d92f3-114">OData およびカスタム サービス要求では、システムの正常性とパフォーマンスが影響を受けると、「要求過多」 を示すエラーが送信されます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-114">For OData and custom service requests, an error which states "Too many requests" will be sent when system health and performance are affected.</span></span> 
- <span data-ttu-id="d92f3-115">**Lifecycle Services (LCS) の監視** ページで調整イベントを照会できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-115">You can query throttling events on the **Lifecycle Services Monitoring** page.</span></span>  

<span data-ttu-id="d92f3-116">**調整優先順位マッピング** ページは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-116">The **Throttling Priority Mapping** page is used to assign priorities for integrations so that priorities can be honored when requests are throttled.</span></span> 

<span data-ttu-id="d92f3-117">適切な優先順位を設定することにより、優先順位の低い統合を優先順位の高い統合の前に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-117">Setting appropriate priorities ensures that low-priority integrations will be throttled before high-priority integrations.</span></span> <span data-ttu-id="d92f3-118">統合の設定方法の詳細については、[外部サービスとの接続を有効にする](/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d92f3-118">For more information about how to set up integration, see [Enable connectivity with external services](/learn/modules/integrate-azure-finance-operations/7-connect-external).</span></span> 

<span data-ttu-id="d92f3-119">Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d92f3-119">There are two kinds of applications are supported in Microsoft Azure Active Directory (Azure AD):</span></span>

- <span data-ttu-id="d92f3-120">ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-120">User based - This flow uses a username and password for authentication and authorization.</span></span> 
- <span data-ttu-id="d92f3-121">Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。</span><span class="sxs-lookup"><span data-stu-id="d92f3-121">Azure AD app based - A confidential client is an application that can keep a client password confidential.</span></span> <span data-ttu-id="d92f3-122">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="d92f3-122">The authorization server assigned this client password to the client application.</span></span> 

<span data-ttu-id="d92f3-123">詳細については、[認証](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d92f3-123">For more information, see [Authentication](services-home-page.md).</span></span>
 
## <a name="configure-priorities-for-integrations"></a><span data-ttu-id="d92f3-124">統合優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d92f3-124">Configure priorities for integrations</span></span> 

<span data-ttu-id="d92f3-125">サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-125">After you have registered your service in Azure AD and in your Finance and Operations apps, you can set up priorities for integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="d92f3-126">設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d92f3-126">You must be assigned the System administrator or Integration priority manager role to complete the set up.</span></span> 

1. <span data-ttu-id="d92f3-127">Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-127">In Finance and Operations apps, go to  **System administration** > **Setup** > **Throttling priority mapping**.</span></span> 
2. <span data-ttu-id="d92f3-128"> *\*新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-128">Select **New**.</span></span> 
3. <span data-ttu-id="d92f3-129"> *\*認証タイプ** フィールドで、統合シナリオに基づいて *\*ユーザー** または *\*Azure AD アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-129">In the  **Authentication type** field, select **User** or **Azure AD application** based on your integration scenario.</span></span>
4. <span data-ttu-id="d92f3-130">**Azure AD アプリケーション タイプ** を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-130">If **Azure AD application type** is selected, in the **Client ID** field select the application that you registered in the Azure Active Directory application.</span></span>
5. <span data-ttu-id="d92f3-131">**ユーザー タイプ** が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-131">If **User type** is selected, in the **User ID** field select an appropriate service account user ID.</span></span>
6. <span data-ttu-id="d92f3-132">適切な優先順位を割り当て、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-132">Assign the appropriate priority and then select **Save**.</span></span>

## <a name="retry-operations"></a><span data-ttu-id="d92f3-133">再試行操作</span><span class="sxs-lookup"><span data-stu-id="d92f3-133">Retry operations</span></span> 

<span data-ttu-id="d92f3-134">要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-134">When a request is throttled, the system provides a value indicating the duration before any new requests from the user can be processed.</span></span> <span data-ttu-id="d92f3-135">要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行** 間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-135">When a request is throttled and a 429 error occurs, the response header will include a **Retry-After** interval, which can be used to retry the request after a specific number of seconds.</span></span> <span data-ttu-id="d92f3-136">次の例は、この操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="d92f3-136">The following example shows this operation.</span></span> 

```C#
    if (!response.IsSuccessStatusCode) 
            { 
                if ((int)response.StatusCode == 429) 
                { 
                    int seconds = 30; 
                    //Try to use the Retry-After header value if it is returned. 
                    if (response.Headers.Contains("Retry-After")) 
                    { 
                        seconds = int.Parse(response.Headers.GetValues("Retry-After").FirstOrDefault()); 
                    } 
                    Thread.Sleep(TimeSpan.FromSeconds(seconds)); 



                    // Retry sending the request.
                } 
            } 
```


## <a name="monitoring"></a><span data-ttu-id="d92f3-137">監視</span><span class="sxs-lookup"><span data-stu-id="d92f3-137">Monitoring</span></span>

<span data-ttu-id="d92f3-138">調整機能でオンボード エクスペリエンスを成功させるには、OData およびカスタム サービス統合パターンも監視できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d92f3-138">To have a successful onboarding experience with the throttling capability, you must also be able to monitor your OData and custom service integration patterns.</span></span> <span data-ttu-id="d92f3-139">管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d92f3-139">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center, contains a collection of monitoring and diagnostics tools that can help ensure that you have an accurate view of the environments you manage.</span></span> <span data-ttu-id="d92f3-140">詳細については、 [Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d92f3-140">For more information, see [Monitoring and diagnostics tools in Lifecycle Services (LCS)](../lifecycle-services/monitoring-diagnostics.md).</span></span>

<span data-ttu-id="d92f3-141">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-141">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="d92f3-142">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-142">You can then export the logs for a more advanced analysis.</span></span> <span data-ttu-id="d92f3-143">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-143">The following types of queries are available:</span></span>

- <span data-ttu-id="d92f3-144">すべての調整イベント</span><span class="sxs-lookup"><span data-stu-id="d92f3-144">All throttling events</span></span>
- <span data-ttu-id="d92f3-145">調整済みの要求</span><span class="sxs-lookup"><span data-stu-id="d92f3-145">Requests throttled</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="d92f3-146">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="d92f3-146">Access the Monitoring and diagnostics portal</span></span>

1. <span data-ttu-id="d92f3-147">LCS で、適切なプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-147">In LCS, open the appropriate project.</span></span>
2. <span data-ttu-id="d92f3-148">**環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-148">In the **Environments** section, select the environment to view, and then select **Full details**.</span></span>
3. <span data-ttu-id="d92f3-149">**環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d92f3-149">On the **Environment details** page, select **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> 
4. <span data-ttu-id="d92f3-150">**環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-150">On the **Environment monitoring** page, select the **Activity** tab to view the **Raw logs** page.</span></span> 
5. <span data-ttu-id="d92f3-151">**クエリ名** を選択し、すべての OData およびカスタム サービス活動の **すべての調整イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-151">Select the **Query name**, and then select **All throttling events** for all OData and custom services activities.</span></span>
6. <span data-ttu-id="d92f3-152">**クエリ名** を選択し、調整されたすべての Odata およびカスタム サービス要求の **調整済みの要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d92f3-152">Select the **Query name**, and then select **Requests throttled** for all OData and custom services requests that have been throttled.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
