---
title: 優先順位に基づく調整
description: このトピックでは、Odata およびカスタム サービス ベース統合の優先順位に基づく調整に関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 09/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: 5ff7fd93-1bb8-4883-9cca-c8c42ddc1746
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Platform update 37
ms.openlocfilehash: 091d909c3e7fbfc075980b6f71b4acbf86043965
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893379"
---
# <a name="priority-based-throttling"></a><span data-ttu-id="f90db-103">優先順位に基づく調整</span><span class="sxs-lookup"><span data-stu-id="f90db-103">Priority-based throttling</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="f90db-104">このトピックに記載されている機能は、プレビュー リリースの一部として使用可能です。</span><span class="sxs-lookup"><span data-stu-id="f90db-104">The functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="f90db-105">コンテンツおよび機能は、変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="f90db-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="f90db-106">この機能をテストするには、**調整優先順位マッピング** ページで統合優先順位をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="f90db-106">To test this capability, configure integration priorities on the **Throttling priority mapping** page.</span></span>  


<span data-ttu-id="f90db-107">優先順位に基づく調整により、リソースの過剰使用率を回避してシステムの応答性を維持し、Dynamics 365 Finance and Operations アプリケーションを実行する環境において一貫した可用性とパフォーマンスを確保できます。</span><span class="sxs-lookup"><span data-stu-id="f90db-107">Priority-based throttling prevents the over-utilization of resources to preserve the system's responsiveness and ensure consistent availability and performance for environments running Dynamics 365 Finance and Operations apps.</span></span>

- <span data-ttu-id="f90db-108">統合には、ビジネスで重要なニーズに基づいて優先順位を付けられます。</span><span class="sxs-lookup"><span data-stu-id="f90db-108">Integrations can be prioritized based on business-critical needs.</span></span> <span data-ttu-id="f90db-109">調整では、これらの優先順位を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="f90db-109">Throttling honors these priorities.</span></span> 
- <span data-ttu-id="f90db-110">OData とカスタム サービス要求では、429 エラー「要求過多」が発生します。</span><span class="sxs-lookup"><span data-stu-id="f90db-110">For OData and custom service requests, a 429 error "Too many requests", will occur.</span></span> 
- <span data-ttu-id="f90db-111">**Lifecycle Services (LCS) の監視** ページで調整イベントを照会できます。</span><span class="sxs-lookup"><span data-stu-id="f90db-111">You can query throttling events on the **Lifecycle Services Monitoring** page.</span></span>  

<span data-ttu-id="f90db-112">優先順位に基づく調整では、ビジネスにとって重要な統合の必要性に応じて、OData とカスタム サービス ベース統合の優先順位を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f90db-112">Priority-based throttling provides the ability to set priorities for OData and custom service-based integrations, depending on the business-critical need of integrations.</span></span>

<span data-ttu-id="f90db-113">**統合優先順位** ページでは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f90db-113">The **Integration priority** page is used to assign priorities for integrations so that priorities can be honored when requests are throttled.</span></span> 

<span data-ttu-id="f90db-114">適切な優先順位を設定することにより、統合に基づいて優先順位の低い統合を、優先順位の高い統合の前に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="f90db-114">Setting appropriate priorities ensures that low-priority integrations will be throttled before high-priority integrations, based on the integration.</span></span> <span data-ttu-id="f90db-115">統合の設定方法の詳細については、[外部サービスとの接続を有効にする](https://docs.microsoft.com/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f90db-115">For more information about how to set up integration, see [Enable connectivity with external services](https://docs.microsoft.com/learn/modules/integrate-azure-finance-operations/7-connect-external).</span></span> 

<span data-ttu-id="f90db-116">Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f90db-116">There are two kinds of applications are supported in Microsoft Azure Active Directory (Azure AD):</span></span>

- <span data-ttu-id="f90db-117">ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="f90db-117">User based - This flow uses a username and password for authentication and authorization.</span></span> 
- <span data-ttu-id="f90db-118">Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。</span><span class="sxs-lookup"><span data-stu-id="f90db-118">Azure AD app based - A confidential client is an application that can keep a client password confidential.</span></span> <span data-ttu-id="f90db-119">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="f90db-119">The authorization server assigned this client password to the client application.</span></span> 

<span data-ttu-id="f90db-120">詳細については、[認証](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f90db-120">For more information, see [Authentication](services-home-page.md).</span></span>
 
## <a name="configure-priorities-for-integrations"></a><span data-ttu-id="f90db-121">統合優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="f90db-121">Configure priorities for integrations</span></span> 

<span data-ttu-id="f90db-122">サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。</span><span class="sxs-lookup"><span data-stu-id="f90db-122">After you have registered your service in Azure AD and in your Finance and Operations apps, you can set up priorities for integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="f90db-123">設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f90db-123">You must be assigned the System administrator or Integration priority manager role to complete the set up.</span></span> 

1. <span data-ttu-id="f90db-124">Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f90db-124">In Finance and Operations apps, go to  **System administration** > **Setup** > **Throttling priority mapping**.</span></span> 
2. <span data-ttu-id="f90db-125"> *\*新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-125">Select **New**.</span></span> 
3. <span data-ttu-id="f90db-126"> *\*認証タイプ** フィールドで、統合シナリオに基づいて *\*ユーザー** または *\*Azure AD アプリケーション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-126">In the  **Authentication type** field, select **User** or **Azure AD application** based on your integration scenario.</span></span>
4. <span data-ttu-id="f90db-127">**Azure AD アプリケーション タイプ** を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-127">If **Azure AD application type** is selected, in the **Client ID** field select the application that you registered in the Azure Active Directory application.</span></span>
5. <span data-ttu-id="f90db-128">**ユーザー タイプ** が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-128">If **User type** is selected, in the **User ID** field select an appropriate service account user ID.</span></span>
6. <span data-ttu-id="f90db-129">適切な優先順位を割り当て、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-129">Assign the appropriate priority and then select **Save**.</span></span>

## <a name="retry-operations"></a><span data-ttu-id="f90db-130">再試行操作</span><span class="sxs-lookup"><span data-stu-id="f90db-130">Retry operations</span></span> 

<span data-ttu-id="f90db-131">要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="f90db-131">When a request is throttled, the system provides a value indicating the duration before any new requests from the user can be processed.</span></span> <span data-ttu-id="f90db-132">要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行** 間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f90db-132">When a request is throttled and a 429 error occurs, the response header will include a **Retry-After** interval, which can be used to retry the request after a specific number of seconds.</span></span> <span data-ttu-id="f90db-133">次の例は、この操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="f90db-133">The following example shows this operation.</span></span> 

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


## <a name="monitoring"></a><span data-ttu-id="f90db-134">監視</span><span class="sxs-lookup"><span data-stu-id="f90db-134">Monitoring</span></span>

<span data-ttu-id="f90db-135">調整機能でオンボード エクスペリエンスを成功させるには、Odata およびカスタム サービス統合パターンも監視できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f90db-135">To have a successful onboarding experience with the throttling capability, you must also be able to monitor your Odata and custom service integration patterns.</span></span> <span data-ttu-id="f90db-136">管理センターである Microsoft Dynamics Lifecycle Services (LCS) には、管理している環境を正確に表示できることを保証する監視および診断ツールのコレクションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f90db-136">Microsoft Dynamics Lifecycle Services (LCS), which is the administration center, contains a collection of monitoring and diagnostics tools that can help ensure that you have an accurate view of the environments you manage.</span></span> <span data-ttu-id="f90db-137">詳細については、[Lifecycle Services (LCS) の監視および診断ツール](../lifecycle-services/monitoring-diagnostics.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f90db-137">For more details, see [Monitoring and diagnostics tools in Lifecycle Services (LCS)](../lifecycle-services/monitoring-diagnostics.md).</span></span>

<span data-ttu-id="f90db-138">一連の定義済クエリを使用して、問題の未加工ログを取得することができます。</span><span class="sxs-lookup"><span data-stu-id="f90db-138">You can use a set of predefined queries to get raw logs for an issue.</span></span> <span data-ttu-id="f90db-139">さらに高度な分析を行うためにログをエクスポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="f90db-139">You can then export the logs for a more advanced analysis.</span></span> <span data-ttu-id="f90db-140">以下のタイプのクエリを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f90db-140">The following types of queries are available:</span></span>

- <span data-ttu-id="f90db-141">すべての調整イベント</span><span class="sxs-lookup"><span data-stu-id="f90db-141">All throttling events</span></span>
- <span data-ttu-id="f90db-142">調整済みの要求</span><span class="sxs-lookup"><span data-stu-id="f90db-142">Requests throttled</span></span>

## <a name="access-the-monitoring-and-diagnostics-portal"></a><span data-ttu-id="f90db-143">監視および診断ポータルへのアクセス</span><span class="sxs-lookup"><span data-stu-id="f90db-143">Access the Monitoring and diagnostics portal</span></span>

1. <span data-ttu-id="f90db-144">LCS で、適切なプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f90db-144">In LCS, open the appropriate project.</span></span>
2. <span data-ttu-id="f90db-145">**環境** セクションで、表示する環境を選択してから **完全な詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-145">In the **Environments** section, select the environment to view, and then select **Full details**.</span></span>
3. <span data-ttu-id="f90db-146">**環境の詳細** ページで、**環境の監視** を選択して、監視および診断ポータルを開きます。</span><span class="sxs-lookup"><span data-stu-id="f90db-146">On the **Environment details** page, select **Environment monitoring** to open the Monitoring and diagnostics portal.</span></span> 
4. <span data-ttu-id="f90db-147">**環境の監視** ページで、**活動** タブを選択して、**未加工ログ** ページを表示します。</span><span class="sxs-lookup"><span data-stu-id="f90db-147">On the **Environment monitoring** page, select the **Activity** tab to view the **Raw logs** page.</span></span> 
5. <span data-ttu-id="f90db-148">**クエリ名** を選択し、すべての Odata およびカスタム サービス活動の **すべての調整イベント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-148">Select the **Query name**, and then select **All throttling events** for all Odata and custom services activities.</span></span>
6. <span data-ttu-id="f90db-149">**クエリ名** を選択し、調整されたすべての Odata およびカスタム サービス要求の **調整された要求** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f90db-149">Select the **Query name**, and then select **Requests throttled** for all Odata and custom services requests that have been throttled.</span></span>
