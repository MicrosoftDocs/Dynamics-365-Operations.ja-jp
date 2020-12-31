---
title: ビジネス イベント と Azure イベントのハブ
description: このチュートリアルでは、 Microsoft Azure イベント ハブでビジネス イベントを機能させるために実行する必要のある手順を扱います。
author: AXnU
manager: AnnBe
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: Platform update 28
ms.dyn365.ops.version: 2019-07-31
ms.openlocfilehash: d4f3d7a690babd03ffe4e401b56ed3e51f1a7918
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688109"
---
# <a name="business-events-and-azure-event-hubs"></a><span data-ttu-id="b036a-103">ビジネス イベント と Azure イベントのハブ</span><span class="sxs-lookup"><span data-stu-id="b036a-103">Business events and Azure Event Hubs</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="b036a-104">このチュートリアルでは、 Microsoft Azure イベント ハブでビジネス イベントを機能させるために実行する必要のある手順を扱います。</span><span class="sxs-lookup"><span data-stu-id="b036a-104">This tutorial describes the steps that you must follow to make business events work with Microsoft Azure Event Hubs.</span></span>

1. <span data-ttu-id="b036a-105">Azure ポータルで、 Active Directory アプリケーションの登録を行います。</span><span class="sxs-lookup"><span data-stu-id="b036a-105">In Azure portal, create an Active Directory application registration.</span></span> <span data-ttu-id="b036a-106">アプリケーション ID をメモします。</span><span class="sxs-lookup"><span data-stu-id="b036a-106">Make a note of the application ID.</span></span>

    ![アプリケーション (クライアント) ID の値](../../media/BE_EH_aad.PNG)

2. <span data-ttu-id="b036a-108">アプリケーションに Azure Key Vault アプリケーション プログラミング インタフェース (API) の許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="b036a-108">Give the app, permission to the Azure Key Vault application programming interface (API).</span></span>

    ![アプリケーションに Azure Key Vault API の許可を付与します。](../../media/BE_EH_api.png)

3. <span data-ttu-id="b036a-110">アプリケーションの登録で、アプリケーションの秘密を作成します。</span><span class="sxs-lookup"><span data-stu-id="b036a-110">In the app registration, create an application secret.</span></span> <span data-ttu-id="b036a-111">値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b036a-111">Make a note of the value.</span></span>

    ![アプリケーションの秘密の作成](../../media/BE_EH_secret.jpg)

4. <span data-ttu-id="b036a-113">key vaultにて、新規アプリの登録に許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="b036a-113">In the key vault, give permission to the new app registration.</span></span>

    ![アプリケーションにアプリの登録の許可を付与する](../../media/BE_EH_permission.jpg)

5. <span data-ttu-id="b036a-115">key vault にて、新たな秘密を作成します。</span><span class="sxs-lookup"><span data-stu-id="b036a-115">In the key vault, create a new secret.</span></span> <span data-ttu-id="b036a-116">この秘密に格納される値は、ご利用のイベントハブへの接続文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b036a-116">The value of this secret must be the connection string to your event hub.</span></span> <span data-ttu-id="b036a-117">値をメモします。</span><span class="sxs-lookup"><span data-stu-id="b036a-117">Make a note of the value.</span></span>

    ![接続文字列](../../media/BE_EH_connectionstring.jpg)

6. <span data-ttu-id="b036a-119">イベント ハブのエンドポイント構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="b036a-119">Create an endpoint configuration for the event hub.</span></span> <span data-ttu-id="b036a-120">**システム管理 \> 設定 \> ビジネス イベント \> ビジネス イベント カタログ** へと移動し、 **エンドポイント** タブにて、 **新規** を選択して **新規エンドポイントの構成** ウィザードを起動します。</span><span class="sxs-lookup"><span data-stu-id="b036a-120">Go to **System administration \> Setup \> Business events \> Business events catalog**, and then, on the **Endpoints** tab, select **New** to open the **Configure new endpoint** wizard.</span></span>

    ![新規エンドポイントウィザードの構成をする](../../media/BE_EH_endpointconfig.jpg)

7. <span data-ttu-id="b036a-122">**エンドポイントの種類** フィールドで、 **Azure イベント ハブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b036a-122">In the **Endpoint type** field, select **Azure Event Hub**.</span></span>
8. <span data-ttu-id="b036a-123">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b036a-123">Select **Next**.</span></span>
9. <span data-ttu-id="b036a-124">**エンドポイント名称** フィールドで、エンドポイントの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-124">In the **Endpoint name** field, enter a name for the endpoint.</span></span>
10. <span data-ttu-id="b036a-125">**ハブの名称** フィールドで、イベントハブの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-125">In the **Hub name** field, enter the name of your event hub.</span></span>
11. <span data-ttu-id="b036a-126">**Azure Active Directory アプリケーション ID** フィールドで、上記で作成したアプリケーションIDを入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-126">In the **Azure Active Directory application ID** field, enter the application ID that was created earlier.</span></span>
12. <span data-ttu-id="b036a-127">**Azure アプリケーションの秘密** フィールドで、上記で作成した値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-127">In the **Azure application secret** field, enter the value that was created earlier.</span></span>
13. <span data-ttu-id="b036a-128">**Key Vault のDNS名称** フィールドで、Key Vault の ドメインネームシステム (DNS)の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-128">In the **Key Vault DNS name** field, enter the Domain Name System (DNS) name of your key vault.</span></span> <span data-ttu-id="b036a-129">この値は、Azure ポータルの key vault 設定の **概要** タブで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="b036a-129">You can find this value on the **Overview** tab of the key vault configuration in the Azure portal.</span></span>
14. <span data-ttu-id="b036a-130">**AKey Vault の秘密の名称** フィールドで、上記で作成した秘密の名称を入力します。</span><span class="sxs-lookup"><span data-stu-id="b036a-130">In the **Key Vault secret name** field, enter the name from the secret that was created earlier.</span></span>
15. <span data-ttu-id="b036a-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b036a-131">Select **OK**.</span></span>
16. <span data-ttu-id="b036a-132">以上で、このエンドポイントに送信する1つ以上のビジネス イベントを有効化することができます。</span><span class="sxs-lookup"><span data-stu-id="b036a-132">You can now activate one or more business events that should be sent to this endpoint.</span></span>
