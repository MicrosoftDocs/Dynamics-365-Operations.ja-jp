---
title: 優先順位に基づく調整
description: このトピックでは、Odata とカスタム サービス ベース統合に関する優先順位に基づく調整に関する情報を提供します。
author: hasaid
manager: AnnBe
ms.date: 07/20/2020
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
ms.openlocfilehash: 640f52d01ec41ec370f6d4cf887c72741abdd2d6
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652203"
---
# <a name="priority-based-throttling"></a><span data-ttu-id="01229-103">優先順位に基づく調整</span><span class="sxs-lookup"><span data-stu-id="01229-103">Priority-based throttling</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="01229-104">優先順位に基づく調整により、リソースの過剰使用率を回避してシステムの応答性を維持し、Dynamics 365 Finance and Operations アプリケーションを実行する環境において一貫した可用性とパフォーマンスを確保できます。</span><span class="sxs-lookup"><span data-stu-id="01229-104">Priority-based throttling prevents the over-utilization of resources to preserve the system's responsiveness and ensure consistent availability and performance for environments running Dynamics 365 Finance and Operations apps.</span></span>

- <span data-ttu-id="01229-105">統合には、ビジネスで重要なニーズに基づいて優先順位を付けられます。</span><span class="sxs-lookup"><span data-stu-id="01229-105">Integrations can be prioritized based on business-critical needs.</span></span> <span data-ttu-id="01229-106">調整では、これらの優先順位を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="01229-106">Throttling honors these priorities.</span></span> 
- <span data-ttu-id="01229-107">OData とカスタム サービス要求では、429 エラー「要求過多」が発生します。</span><span class="sxs-lookup"><span data-stu-id="01229-107">For OData and custom service requests, a 429 error "Too many requests", will occur.</span></span> 
- <span data-ttu-id="01229-108">**Lifecycle Services (LCS) の監視**ページで調整イベントを照会できます。</span><span class="sxs-lookup"><span data-stu-id="01229-108">You can query throttling events on the **Lifecycle Services Monitoring** page.</span></span>  

<span data-ttu-id="01229-109">優先順位に基づく調整では、ビジネスにとって重要な統合の必要性に応じて、OData とカスタムのサービス ベース統合の優先順位を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="01229-109">Priority-based throttling provides the ability to set priorities for OData and custom service-based integrations, depending on the business-critical need of integrations.</span></span>

<span data-ttu-id="01229-110">**統合優先順位**ページでは、要求が調整された場合、優先順位が受け入れられるように統合の優先順位を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="01229-110">The **Integration priority** page is used to assign priorities for integrations so that priorities can be honored when requests are throttled.</span></span> 

<span data-ttu-id="01229-111">適切な優先順位を設定することにより、統合に基づいて優先順位の低い統合を、優先順位の高い統合の前に調整することができます。</span><span class="sxs-lookup"><span data-stu-id="01229-111">Setting appropriate priorities ensures that low-priority integrations will be throttled before high-priority integrations, based on the the integration.</span></span> <span data-ttu-id="01229-112">統合の設定方法の詳細については、[外部サービスとの接続を有効にする](https://docs.microsoft.com/learn/modules/integrate-azure-finance-operations/7-connect-external) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01229-112">For more information about how to set up integration, see [Enable connectivity with external services](https://docs.microsoft.com/learn/modules/integrate-azure-finance-operations/7-connect-external).</span></span> 

<span data-ttu-id="01229-113">Microsoft Azure Active Directory (Azure AD) では、次の 2 種類のアプリケーションがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="01229-113">There are two kinds of applications are supported in Microsoft Azure Active Directory (Azure AD):</span></span>

- <span data-ttu-id="01229-114">ユーザー ベース - このフローでは、認証と承認にユーザー名とパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="01229-114">User based - This flow uses a username and password for authentication and authorization.</span></span> 
- <span data-ttu-id="01229-115">Azure AD アプリケーション ベース - 機密クライアントとは、クライアント パスワードを機密保持できるアプリケーションのことです。</span><span class="sxs-lookup"><span data-stu-id="01229-115">Azure AD app based - A confidential client is an application that can keep a client password confidential.</span></span> <span data-ttu-id="01229-116">承認サーバーは、このクライアント パスワードをクライアント アプリケーションに割り当てています。</span><span class="sxs-lookup"><span data-stu-id="01229-116">The authorization server assigned this client password to the client application.</span></span> 

<span data-ttu-id="01229-117">詳細については、[認証](services-home-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="01229-117">For more information, see [Authentication](services-home-page.md).</span></span>
 
## <a name="configure-priorities-for-integrations"></a><span data-ttu-id="01229-118">統合優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="01229-118">Configure priorities for integrations</span></span> 

<span data-ttu-id="01229-119">サービスを Azure AD および Finance and Operations アプリに登録すると、統合優先順位を設定できます。</span><span class="sxs-lookup"><span data-stu-id="01229-119">After you have registered your service in Azure AD and in your Finance and Operations apps, you can set up priorities for integrations.</span></span>

> [!NOTE]
> <span data-ttu-id="01229-120">設定を完了するには、システム管理者または統合優先順位マネージャー ロールを割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="01229-120">You must be assigned the System administrator or Integration priority manager role to complete the set up.</span></span> 

1. <span data-ttu-id="01229-121">Finance and Operations アプリで、 **システム管理** > **設定** > **調整優先順位マッピング**に移動します。</span><span class="sxs-lookup"><span data-stu-id="01229-121">In Finance and Operations apps, go to **System administration** > **Setup** > **Throttling priority mapping**.</span></span> 
2. <span data-ttu-id="01229-122"> *\*新規*\*を選択します。</span><span class="sxs-lookup"><span data-stu-id="01229-122">Select **New**.</span></span> 
3. <span data-ttu-id="01229-123"> *\*認証タイプ** フィールドで、統合シナリオに基づいて*\*ユーザー*\*または *\*Azure AD アプリケーション*\*を選択します。</span><span class="sxs-lookup"><span data-stu-id="01229-123">In the **Authentication type** field, select **User** or **Azure AD application** based on your integration scenario.</span></span>
4. <span data-ttu-id="01229-124">**Azure AD アプリケーション タイプ**を選択した場合、Azure Active Directory アプリケーションで登録したアプリケ―ションを **クライアント ID** フィールドで選択します。</span><span class="sxs-lookup"><span data-stu-id="01229-124">If **Azure AD application type** is selected, in the **Client ID** field select the application that you registered in the Azure Active Directory application.</span></span>
5. <span data-ttu-id="01229-125">**ユーザー タイプ**が選択されている場合は、 **ユーザー ID** フィールドで適切なサービス アカウント ユーザー ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="01229-125">If **User type** is selected, in the **User ID** field select an appropriate service account user ID.</span></span>
6. <span data-ttu-id="01229-126">適切な優先順位を割り当て、**保存**を選択します。</span><span class="sxs-lookup"><span data-stu-id="01229-126">Assign the appropriate priority and then select **Save**.</span></span>

## <a name="retry-operations"></a><span data-ttu-id="01229-127">再試行操作</span><span class="sxs-lookup"><span data-stu-id="01229-127">Retry operations</span></span> 

<span data-ttu-id="01229-128">要求が調整されると、ユーザーからの新しい要求を処理できるようになるまでの期間を示す値がシステムによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="01229-128">When a request is throttled, the system provides a value indicating the duration before any new requests from the user can be processed.</span></span> <span data-ttu-id="01229-129">要求が調整され、429 エラーが発生した場合、応答ヘッダーは **再試行**間隔を含み、指定された秒数の経過後に要求を再試行するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="01229-129">When a request is throttled and a 429 error occurs, the response header will include a **Retry-After** interval, which can be used to retry the request after a specific number of seconds.</span></span> <span data-ttu-id="01229-130">次の例は、この操作を示しています。</span><span class="sxs-lookup"><span data-stu-id="01229-130">The following example shows this operation.</span></span> 

```x++
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
