---
title: 優先順位に基づく調整
description: このトピックでは、OData およびカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。
author: hasaid
ms.date: 09/25/2020
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
ms.openlocfilehash: 900c7c1f36bed1a5f46cc8c5048bc0b231f7177a
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941214"
---
# <a name="priority-based-throttling"></a><span data-ttu-id="5d053-103">優先順位に基づく調整</span><span class="sxs-lookup"><span data-stu-id="5d053-103">Priority-based throttling</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5d053-104">優先順位に基づく調整は、Dynamics 365 Finance バージョン 10.0.19 から既定で有効になります。</span><span class="sxs-lookup"><span data-stu-id="5d053-104">Priority-based throttling is enabled by default starting in Dynamics 365 Finance version 10.0.19.</span></span> <span data-ttu-id="5d053-105">バージョン 10.0.19 に更新する前に環境を準備する方法については [FAQ ドキュメント](throttling-faq.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d053-105">To learn about how you can prepare your environment prior to updating to  version 10.0.19, see [FAQ document](throttling-faq.md).</span></span> <span data-ttu-id="5d053-106">この機能をテストするには、**調整優先順位マッピング** ページで統合優先順位をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="5d053-106">To test this capability, configure the integration priorities on the **Throttling priority mapping** page.</span></span>

<span data-ttu-id="5d053-107">優先順位に基づく調整により、サービス保護設定を導入し、リソースの過剰使用率を回避してシステムの応答性を維持し、Finance and Operations アプリを実行する環境において一貫した可用性とパフォーマンスを確保できます。</span><span class="sxs-lookup"><span data-stu-id="5d053-107">Priority-based throttling introduces service protection settings that prevent the over-utilization of resources to preserve the system's responsiveness and ensure consistent availability and performance for environments running Finance and Operations apps.</span></span>

<span data-ttu-id="5d053-108">優先順位に基づく調整では、ビジネスにとって重要なこれらの統合の必要性に応じて、OData とカスタム サービス ベース統合の相対的な優先順位を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5d053-108">You have the ability to set relative priority for the OData and custom service-based integrations, depending on your business-critical need for these integrations.</span></span> <span data-ttu-id="5d053-109">調整マネージャーは、これらの要求に対して設定されたこれらの優先順位を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="5d053-109">The throttling manager will then honor these priorities set for these requests.</span></span>

- <span data-ttu-id="5d053-110">OData およびカスタム サービス要求では、システムの正常性とパフォーマンスが影響を受けると、「要求過多」 を示すエラーが送信されます。</span><span class="sxs-lookup"><span data-stu-id="5d053-110">For OData and custom service requests, an error which states "Too many requests" will be sent when system health and performance are affected.</span></span> 
- <span data-ttu-id="5d053-111">**Lifecycle Services (LCS) の監視** ページで調整イベントを照会できます。</span><span class="sxs-lookup"><span data-stu-id="5d053-111">You can query throttling events on the **Lifecycle Services Monitoring** page.</span></span>  

<span data-ttu-id="5d053-112">**調整優先順位マッピング** ページは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5d053-112">The **Throttling Priority Mapping** page is used to assign priorities for integrations so that priorities can be honored when requests are throttled.</span></span> 

<span data-ttu-id="5d053-113">適切な優先順位を設定することにより、優先順位の低い統合を優先順位の高い統合の前に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="5d053-113">Setting appropriate priorities ensures that low-priority integrations will be throttled before high-priority integrations.</span></span> <span data-ttu-id="5d053-114">統合の設定方法の詳細については、[外部サービスとの接続を有効にする](/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d053-114">For more information about how to set up integration, see [Enable connectivity with external services](/learn/modules/integrate-azure-finance-operations/7-connect-external).</span></span> 

<span data-ttu-id="5d053-115">Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="5d053-115">There are two kinds of applications are supported in Microsoft Azure Active Directory (Azure AD):</span></span>

- <span data-ttu-id="5d053-116">ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="5d053-116">User based - This flow uses a username and password for authentication and authorization.</span></span> 
- <span data-ttu-id="5d053-117">Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。</span><span class="sxs-lookup"><span data-stu-id="5d053-117">Azure AD app based - A confidential client is an application that can keep a client password confidential.</span></span> <span data-ttu-id="5d053-118">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="5d053-118">The authorization server assigned this client password to the client application.</span></span> 

<span data-ttu-id="5d053-119">詳細については、[認証](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d053-119">For more information, see [Authentication](services-home-page.md).</span></span>
 
## <a name="configure-priorities-for-integrations"></a><span data-ttu-id="5d053-120">統合優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="5d053-120">Configure priorities for integrations</span></span> 

<span data-ttu-id="5d053-121">サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。</span><span class="sxs-lookup"><span data-stu-id="5d053-121">After you have registered your service in Azure AD and in your Finance and Operations apps, you can set up priorities for integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="5d053-122">設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d053-122">You must be assigned the System administrator or Integration priority manager role to complete the set up.</span></span> 

1. <span data-ttu-id="5d053-123">Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="5d053-123">In Finance and Operations apps, go to  **System administration** > **Setup** > **Throttling priority mapping**.</span></span> 
2. <span data-ttu-id="5d053-124"> *\*新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-124">Select **New**.</span></span> 
3. <span data-ttu-id="5d053-125"> *\*認証タイプ** フィールドで、統合シナリオに基づいて *\*ユーザー** または *\*Azure AD アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-125">In the  **Authentication type** field, select **User** or **Azure AD application** based on your integration scenario.</span></span>
4. <span data-ttu-id="5d053-126">**Azure AD アプリケーション タイプ** を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-126">If **Azure AD application type** is selected, in the **Client ID** field select the application that you registered in the Azure Active Directory application.</span></span>
5. <span data-ttu-id="5d053-127">**ユーザー タイプ** が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-127">If **User type** is selected, in the **User ID** field select an appropriate service account user ID.</span></span>
6. <span data-ttu-id="5d053-128">適切な優先順位を割り当て、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-128">Assign the appropriate priority and then select **Save**.</span></span>

## <a name="retry-operations"></a><span data-ttu-id="5d053-129">再試行操作</span><span class="sxs-lookup"><span data-stu-id="5d053-129">Retry operations</span></span> 

<span data-ttu-id="5d053-130">要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="5d053-130">When a request is throttled, the system provides a value indicating the duration before any new requests from the user can be processed.</span></span> <span data-ttu-id="5d053-131">要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行** 間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d053-131">When a request is throttled and a 429 error occurs, the response header will include a **Retry-After** interval, which can be used to retry the request after a specific number of seconds.</span></span> <span data-ttu-id="5d053-132">次の例は、この操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="5d053-132">The following example shows this operation.</span></span> 

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


## <a name="monitoring"></a><span data-ttu-id="5d053-133">監視</span><span class="sxs-lookup"><span data-stu-id="5d053-133">Monitoring</span></span>

<span data-ttu-id="5d053-134">調整機能でオンボード エクスペリエンスを成功させるには、OData およびカスタム サービス統合パターンも監視できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5d053-134">To have a successful onboarding experience with the throttling capability, you must also be able to monitor your OData and custom service integration patterns.</span></span> <span data-ttu-id="5d053-135">管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5d053-135">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center, contains a collection of monitoring and diagnostics tools that can help ensure that you have an accurate view of the environments you manage.</span></span> <span data-ttu-id="5d053-136">詳細については、 [Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5d053-136">For more information, see [Monitoring and diagnostics tools in Lifecycle Services (LCS)](../lifecycle-services/monitoring-diagnostics.md).</span></span>

<span data-ttu-id="5d053-137">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="5d053-137">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="5d053-138">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="5d053-138">You can then export the logs for a more advanced analysis.</span></span> <span data-ttu-id="5d053-139">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="5d053-139">The following types of queries are available:</span></span>

- <span data-ttu-id="5d053-140">すべての調整イベント</span><span class="sxs-lookup"><span data-stu-id="5d053-140">All throttling events</span></span>
- <span data-ttu-id="5d053-141">調整済みの要求</span><span class="sxs-lookup"><span data-stu-id="5d053-141">Requests throttled</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="5d053-142">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="5d053-142">Access the Monitoring and diagnostics portal</span></span>

1. <span data-ttu-id="5d053-143">LCS で、適切なプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="5d053-143">In LCS, open the appropriate project.</span></span>
2. <span data-ttu-id="5d053-144">**環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-144">In the **Environments** section, select the environment to view, and then select **Full details**.</span></span>
3. <span data-ttu-id="5d053-145">**環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="5d053-145">On the **Environment details** page, select **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> 
4. <span data-ttu-id="5d053-146">**環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="5d053-146">On the **Environment monitoring** page, select the **Activity** tab to view the **Raw logs** page.</span></span> 
5. <span data-ttu-id="5d053-147">**クエリ名** を選択し、すべての OData およびカスタム サービス活動の **すべての調整イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-147">Select the **Query name**, and then select **All throttling events** for all OData and custom services activities.</span></span>
6. <span data-ttu-id="5d053-148">**クエリ名** を選択し、調整されたすべての Odata およびカスタム サービス要求の **調整済みの要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="5d053-148">Select the **Query name**, and then select **Requests throttled** for all OData and custom services requests that have been throttled.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
