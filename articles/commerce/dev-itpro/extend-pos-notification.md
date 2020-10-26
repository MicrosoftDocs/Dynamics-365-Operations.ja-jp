---
title: POS でカスタム通知を表示する
description: このトピックでは、販売時点管理 (POS) でカスタマイズした通知を追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 28021
ms.assetid: ''
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 90be8691950e5a29737dacbf4043b72c7a31a355
ms.sourcegitcommit: 9c694772e1484df10afd72ea1a717fda0861627e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/14/2020
ms.locfileid: "3813872"
---
# <a name="show-custom-notifications-in-the-pos"></a><span data-ttu-id="d52d0-103">POS でカスタム通知を表示する</span><span class="sxs-lookup"><span data-stu-id="d52d0-103">Show custom notifications in the POS</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d52d0-104">このトピックでは、販売時点管理 (POS) でカスタマイズした通知を追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-104">This topic explains how to add custom notifications in the point of sale (POS).</span></span> <span data-ttu-id="d52d0-105">このトピックは、最新のバイナリ修正がある Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 および Dynamics 365 for Retail 7.3 とそれ以降のバージョンに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-105">This topic applies to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 and Dynamics 365 for Retail 7.3, and later versions that have the latest binary fix.</span></span>

<span data-ttu-id="d52d0-106">次のシナリオで、POS 通知フレームワークを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-106">You can extend the POS notification framework for these scenarios:</span></span>

- <span data-ttu-id="d52d0-107">カスタム通知を表示して、店舗の関連付けが通知に基づいて必要なアクションを実行したり、カスタム ロジックを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-107">Show a custom notification so that a store associate can either perform a required action, based on that notification, or perform custom logic.</span></span>
- <span data-ttu-id="d52d0-108">定期的に、バックグラウンドで操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-108">Periodically perform some operation in the background.</span></span> <span data-ttu-id="d52d0-109">ただし、パフォーマンスの問題が発生する可能性があるため、このシナリオはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d52d0-109">However, this scenario isn't recommended, because it might cause performance issues.</span></span>

## <a name="how-custom-notifications-work"></a><span data-ttu-id="d52d0-110">カスタム通知の仕組み</span><span class="sxs-lookup"><span data-stu-id="d52d0-110">How custom notifications work</span></span>

<span data-ttu-id="d52d0-111">POS の通知フレームワークは、Retail Headquarters で構成されている操作に対して定期的に実行されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-111">The notification framework in the POS periodically runs for the configured operation in Retail headquarters.</span></span> <span data-ttu-id="d52d0-112">(定期処理の実行頻度をコンフィギュレーションできます。) また、Commerce runtime (CRT) および Retail Headquarters のリアルタイム サービスで通知サービスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-112">(The frequency of the periodic runs can be configured.) It calls the notification service in the Commerce runtime (CRT) and Real time service in Retail headquarters.</span></span> <span data-ttu-id="d52d0-113">POS が CRT で通知サービスに対する呼び出しを行うと、CRT はビジネス ロジックを実行し、操作に対して POS に送信される通知があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-113">When the POS makes the call to the notification service in CRT, CRT runs the business logic and determines whether any notification must be sent to the POS for the operation.</span></span> <span data-ttu-id="d52d0-114">操作 ID は、要求にパラメータとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-114">The operation ID is passed to the request as a parameter.</span></span> <span data-ttu-id="d52d0-115">CRT 通知サービスは操作 ID をチェックし、通知の詳細を返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-115">The CRT notification service checks the operation ID and returns the notification details.</span></span>

<span data-ttu-id="d52d0-116">通知が存在する場合、CRT は POS に利用可能な通知があることを報告する応答を返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-116">If the notification exists, CRT returns the response to the POS and reports that a notification is available.</span></span> <span data-ttu-id="d52d0-117">この通知は、POS によって解析され、ユーザー インターフェース (UI) に表示されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-117">POS parses this notification and shows it in the user interface (UI).</span></span> <span data-ttu-id="d52d0-118">POS ユーザーが通知を選択すると、POS の関連する操作が実行されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-118">When the POS user selects the notification, the relevant operation in POS is run.</span></span> <span data-ttu-id="d52d0-119">通知は、操作にリンクされています。</span><span class="sxs-lookup"><span data-stu-id="d52d0-119">Notifications are linked to an operation.</span></span> <span data-ttu-id="d52d0-120">操作ハンドラー内で、実行する必要があるビジネス ロジックを書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-120">Inside the operation handler, you write the business logic that must be performed.</span></span>

<span data-ttu-id="d52d0-121">CRT が通知に対する応答を返すと、通知、メッセージ、およびアクション パラメーターの数が返されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-121">When CRT returns the response for the notification, it returns the number of notifications, messages, and action parameters.</span></span> <span data-ttu-id="d52d0-122">POS フレームワークには、応答を解析して POS 操作 ID を取得し、ユーザーが通知を選択したときにそれを呼び出す組み込みロジックがあります。</span><span class="sxs-lookup"><span data-stu-id="d52d0-122">The POS framework has built-in logic to parse the response to get the POS operation ID and call it when the user selects the notification.</span></span>

<span data-ttu-id="d52d0-123">操作内で、POS ユーザーが通知を選択したときに行われる特定の動作について、カスタム ロジックに書き込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-123">Inside the operation, you can write custom logic to specify what should happen when the POS user selects the notification.</span></span> <span data-ttu-id="d52d0-124">アクション プロパティを使用して、追加のパラメータを CRT から POS に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-124">Additional parameters can be sent from CRT to the POS by using the action property.</span></span> <span data-ttu-id="d52d0-125">その後、これらのパラメータは、POS の操作要求内で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="d52d0-125">Those parameters will then be available inside the operation request in the POS.</span></span>

### <a name="example"></a><span data-ttu-id="d52d0-126">例</span><span class="sxs-lookup"><span data-stu-id="d52d0-126">Example</span></span>

<span data-ttu-id="d52d0-127">集荷の注文を準備するよう POS ユーザーに通知するために、CRT に集荷の注文があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-127">To notify the POS user to prepare orders for pickup, inside CRT, check whether there is an order for pickup.</span></span> <span data-ttu-id="d52d0-128">ある場合、関連するパラメーターを使用して通知応答を更新します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-128">If there is, update the notification response with the relevant parameters.</span></span> <span data-ttu-id="d52d0-129">POS が応答を解析し、通知を表示します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-129">The POS parses the response and shows the notification.</span></span> <span data-ttu-id="d52d0-130">POS ユーザーが通知を選択すると、POS は通知からのパラメータを使用して操作を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-130">When the POS user selects the notification, the POS calls the operation by using the parameter from the notification.</span></span> <span data-ttu-id="d52d0-131">(拡張ロジックは、パラメータを送信する必要があるかどうかを決定します。) 操作内で、POS が集荷の保留中の注文をすべて読み取り、POS ユーザーがさらにアクションを実行できるように、注文を UI に表示します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-131">(The extension logic determines whether parameters should be sent.) Inside the operation, the POS reads all the pending orders for pickup and shows the orders in the UI so that the POS user can take further action.</span></span>

## <a name="required-steps-to-make-notifications-available-for-a-custom-operation"></a><span data-ttu-id="d52d0-132">カスタム操作の通知を使用可能にするための必要な手順</span><span class="sxs-lookup"><span data-stu-id="d52d0-132">Required steps to make notifications available for a custom operation</span></span>

1. <span data-ttu-id="d52d0-133">Retail Headquarters で **Retail と Commerce \> チャネル設定 \> POS 設定 \> POS \> POS 操作**に移動し、操作を作成します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-133">In Retail headquarters, go to **Retail and Commerce \> Channel Setup \> POS Setup \> POS \> POS operations**, and create an operation.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d52d0-134">カスタム操作に 5000 以上の操作 ID を使用します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-134">For custom operations, use an operation ID that is above 5000.</span></span>

2. <span data-ttu-id="d52d0-135">通知サービスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-135">Extend the notification service.</span></span> <span data-ttu-id="d52d0-136">通知サービスのスケジューラが実行されると、通知メッセージを取得するために、CRT とリアルタイム トランザクション サービス拡張コードの両方の拡張コードが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-136">When the scheduler for the notification service runs, it calls the extension code for both CRT and the Real time transaction service to get the notification message.</span></span>
3. <span data-ttu-id="d52d0-137">POS を拡張します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-137">Extend the POS.</span></span> <span data-ttu-id="d52d0-138">POS で、POS ユーザーが通知を選択したときに行われる特定の動作について、POS 操作内のロジックに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-138">In the POS, write logic inside the POS operation to specify what should happen when the POS user selects the notification.</span></span> <span data-ttu-id="d52d0-139">POS 操作の作成方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](add-pos-operations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d52d0-139">For information about how to create a POS operation, see [Add POS operations to POS layouts by using Button grid designer](add-pos-operations.md).</span></span>
4. <span data-ttu-id="d52d0-140">Retail Headquarters で、カスタム操作の通知サービスを構成します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-140">In Retail headquarters, configure the notification service with the custom operation.</span></span> <span data-ttu-id="d52d0-141">その後、スケジューラが通知サービスを実行すると、カスタム操作が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-141">Then, when the scheduler runs the notification service, it includes the custom operation.</span></span> <span data-ttu-id="d52d0-142">POS で通知を構成する方法については、[ボタン グリッド デザイナーを使用して POS 操作を POS レイアウトに追加](../notifications-pos.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d52d0-142">For information about how to configure notifications in the POS, see [Add POS operations to POS layouts by using Button grid designer](../notifications-pos.md).</span></span>

    <span data-ttu-id="d52d0-143">POS ユーザーが通知を選択すると、CRT から返された応答に基づいて、フレームワークは適切な操作を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-143">When the POS user selects the notification, the framework calls the correct operation, based on the response that is returned from CRT.</span></span> <span data-ttu-id="d52d0-144">Retail Headquarters で構成されているすべての通知に対して通知サービスが実行され、操作 ID と通知の詳細を含む応答が返されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-144">The notification service runs for all the notifications that are configured in Retail headquarters, and it returns the response that includes the operation ID and notification details.</span></span> <span data-ttu-id="d52d0-145">そのため、POS は操作 ID のコンテキストを持つことになり、フレームワークはこのコンテキストを使用してオペレーションの実装を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-145">Therefore, the POS will have the context of the operation ID, and the framework will use this context to call the operation implementation.</span></span>

> [!NOTE]
> <span data-ttu-id="d52d0-146">通知スケジューラは、CRT と Retail Headquarters の両方で、新しい通知を確認します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-146">The notification scheduler checks both CRT and Retail headquarters for new notifications.</span></span> <span data-ttu-id="d52d0-147">シナリオに応じて、Retail Headquarters または CRT のみのリアルタイム トランザクション サービスを拡張できます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-147">Depending on the scenario, you can extend the Real time transaction service in Retail headquarters or only in CRT.</span></span> <span data-ttu-id="d52d0-148">通知にリアルタイム処理が必要なシナリオでは、Retail Headquarters でリアルタイム トランザクション サービスを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-148">In scenarios where real-time processing is required for notifications, extend the Real-time transaction service method in Retail headquarters.</span></span> <span data-ttu-id="d52d0-149">リアルタイム処理を必要としない場合は、CRT のみを拡張します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-149">If real-time processing isn't required, extend only CRT.</span></span>

## <a name="extend-the-notification-service-in-crt"></a><span data-ttu-id="d52d0-150">CRT の通知サービスの拡張</span><span class="sxs-lookup"><span data-stu-id="d52d0-150">Extend the notification service in CRT</span></span>

<span data-ttu-id="d52d0-151">CRT の通知サービスを拡張するには、**GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-151">To extend the notification service in CRT, override **GetNotificationsExtensionServiceRequest**, and return **GetNotificationsExtensionServiceResponse**.</span></span>

<span data-ttu-id="d52d0-152">Retail ソフトウェア開発キット (SDK) には、通知サービス (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**) を拡張する方法を示すサンプルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d52d0-152">The Retail software development kit (SDK) includes a sample that shows how to extend the notification service (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**).</span></span>

+ <span data-ttu-id="d52d0-153">**GetNotificationsExtensionServiceRequest** – このクラスには、操作 ID、スタッフ、およびチャネルが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-153">**GetNotificationsExtensionServiceRequest** – This class contains the operation ID, staff, and channel.</span></span> <span data-ttu-id="d52d0-154">Retail Headquarters の構成に基づいて、POS は構成された各操作に対して通知スケジューラを実行します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-154">Based on the configuration of Retail headquarters, the POS runs the notification scheduler for each configured operation.</span></span>
+ <span data-ttu-id="d52d0-155">**GetNotificationsExtensionServiceResponse** – 応答で、通知の詳細エンティティ (**NotificationDetailCollection**) を返し、**GetNotificationsExtensionServiceResponse** を更新して、すべての通知を返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-155">**GetNotificationsExtensionServiceResponse** – In the response, return the notification detail entity (**NotificationDetailCollection**), update **GetNotificationsExtensionServiceResponse**, and return all the notifications.</span></span> <span data-ttu-id="d52d0-156">応答はコレクションなので、複数の通知を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-156">Because the response is a collection, multiple notifications can be returned.</span></span>

## <a name="properties-of-the-notification-detail-entity"></a><span data-ttu-id="d52d0-157">通知の詳細エンティティのプロパティ</span><span class="sxs-lookup"><span data-stu-id="d52d0-157">Properties of the notification detail entity</span></span>

<span data-ttu-id="d52d0-158">通知の詳細エンティティには、次のプロパティがあります。</span><span class="sxs-lookup"><span data-stu-id="d52d0-158">The notification detail entity has the following properties.</span></span>

| <span data-ttu-id="d52d0-159">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d52d0-159">Property</span></span>               | <span data-ttu-id="d52d0-160">データ型</span><span class="sxs-lookup"><span data-stu-id="d52d0-160">Data type</span></span>      | <span data-ttu-id="d52d0-161">説明</span><span class="sxs-lookup"><span data-stu-id="d52d0-161">Description</span></span>                                                                            |
|------------------------|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d52d0-162">ActionProperty</span><span class="sxs-lookup"><span data-stu-id="d52d0-162">ActionProperty</span></span>         | <span data-ttu-id="d52d0-163">文字列</span><span class="sxs-lookup"><span data-stu-id="d52d0-163">string</span></span>         | <span data-ttu-id="d52d0-164">POS 操作に送信するカスタム プロパティ。</span><span class="sxs-lookup"><span data-stu-id="d52d0-164">A custom property to send to the POS operation.</span></span>                                        |
| <span data-ttu-id="d52d0-165">DisplayText</span><span class="sxs-lookup"><span data-stu-id="d52d0-165">DisplayText</span></span>            | <span data-ttu-id="d52d0-166">文字列</span><span class="sxs-lookup"><span data-stu-id="d52d0-166">string</span></span>         | <span data-ttu-id="d52d0-167">通知の表示テキスト。</span><span class="sxs-lookup"><span data-stu-id="d52d0-167">The display text of the notification.</span></span>                                                  |
| <span data-ttu-id="d52d0-168">IsLiveContentOnly</span><span class="sxs-lookup"><span data-stu-id="d52d0-168">IsLiveContentOnly</span></span>      | <span data-ttu-id="d52d0-169">ブール</span><span class="sxs-lookup"><span data-stu-id="d52d0-169">bool</span></span>           | <span data-ttu-id="d52d0-170">通知がライブ コンテンツのみを対象とするかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d52d0-170">A value that indicates whether the notification is only for live content.</span></span>              |
| <span data-ttu-id="d52d0-171">IsNew</span><span class="sxs-lookup"><span data-stu-id="d52d0-171">IsNew</span></span>                  | <span data-ttu-id="d52d0-172">ブール</span><span class="sxs-lookup"><span data-stu-id="d52d0-172">bool</span></span>           | <span data-ttu-id="d52d0-173">通知が新しいかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d52d0-173">A value that indicates whether the notification is new.</span></span>                                |
| <span data-ttu-id="d52d0-174">IsSuccess</span><span class="sxs-lookup"><span data-stu-id="d52d0-174">IsSuccess</span></span>              | <span data-ttu-id="d52d0-175">ブール</span><span class="sxs-lookup"><span data-stu-id="d52d0-175">bool</span></span>           | <span data-ttu-id="d52d0-176">通知が成功したかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="d52d0-176">A value that indicates whether the notification was successful.</span></span>                        |
| <span data-ttu-id="d52d0-177">ItemCount</span><span class="sxs-lookup"><span data-stu-id="d52d0-177">ItemCount</span></span>              | <span data-ttu-id="d52d0-178">long</span><span class="sxs-lookup"><span data-stu-id="d52d0-178">long</span></span>           | <span data-ttu-id="d52d0-179">通知の数。</span><span class="sxs-lookup"><span data-stu-id="d52d0-179">The number of notifications.</span></span>                                                           |
| <span data-ttu-id="d52d0-180">LastUpdatedDateTime</span><span class="sxs-lookup"><span data-stu-id="d52d0-180">LastUpdatedDateTime</span></span>    | <span data-ttu-id="d52d0-181">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d52d0-181">DateTimeOffset</span></span> | <span data-ttu-id="d52d0-182">アクション プロパティの項目が最後に更新された日時。</span><span class="sxs-lookup"><span data-stu-id="d52d0-182">The date/time when the item in the action property was last updated.</span></span>                   |
| <span data-ttu-id="d52d0-183">LastUpdatedDateTimeStr</span><span class="sxs-lookup"><span data-stu-id="d52d0-183">LastUpdatedDateTimeStr</span></span> | <span data-ttu-id="d52d0-184">文字列</span><span class="sxs-lookup"><span data-stu-id="d52d0-184">string</span></span>         | <span data-ttu-id="d52d0-185">文字列形式のアクション プロパティの項目が最後に更新された日時。</span><span class="sxs-lookup"><span data-stu-id="d52d0-185">The date/time when the item in the action property was last updated, in string format.</span></span> |

## <a name="detailed-steps"></a><span data-ttu-id="d52d0-186">詳細な手順</span><span class="sxs-lookup"><span data-stu-id="d52d0-186">Detailed steps</span></span>

1. <span data-ttu-id="d52d0-187">Retail SDK から **Runtime.Extensions.NotificationSample.proj** を開きます (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**)。</span><span class="sxs-lookup"><span data-stu-id="d52d0-187">Open **Runtime.Extensions.NotificationSample.proj** from the Retail SDK (**RetailSDK\\SampleExtensions\\CommerceRuntime\\Extensions.NotificationSample**).</span></span>
2. <span data-ttu-id="d52d0-188">標準の名前付け規則に従ってプロジェクトの名前を変更します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-188">Rename the project according to the standard naming convention.</span></span>
3. <span data-ttu-id="d52d0-189">プロジェクト内には、**NotificationExtensionService.cs** という名前のクラス ファイルがあります。</span><span class="sxs-lookup"><span data-stu-id="d52d0-189">Inside the project, there is a class file that is named **NotificationExtensionService.cs**.</span></span> <span data-ttu-id="d52d0-190">このファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-190">Open this file.</span></span>
4. <span data-ttu-id="d52d0-191">**GetNotificationsExtensionServiceRequest** クラスは、カスタム通知を追加するために上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-191">The **GetNotificationsExtensionServiceRequest** class is overridden to add a custom notification.</span></span> <span data-ttu-id="d52d0-192">**GetNotificationsExtensionServiceRequest** を上書きし、**GetNotificationsExtensionServiceResponse** を返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-192">Override **GetNotificationsExtensionServiceRequest**, and return **GetNotificationsExtensionServiceResponse**.</span></span>
5. <span data-ttu-id="d52d0-193">新しいクラスを作成して、**GetNotificationsExtensionServiceRequest** を上書きするか、サンプル テンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-193">Either create a new class and override **GetNotificationsExtensionServiceRequest**, or use the sample template.</span></span> 
6. <span data-ttu-id="d52d0-194">**NotificationExtensionService** クラスには、**Process** という名前のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="d52d0-194">In the **NotificationExtensionService** class, there is a method that is named **Process**.</span></span> <span data-ttu-id="d52d0-195">このコードは、メソッド内で操作 ID を確認し、操作 ID に基づいて通知の詳細オブジェクトを作成し、通知を追加します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-195">The code inside that method checks the operation ID and then, based on the operation ID, creates a notification details object and adds any notifications.</span></span> <span data-ttu-id="d52d0-196">カスタム操作 ID かどうかを確認し、通知があるかどうかを確認するロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-196">Check whether the operation ID is custom operation ID, and then write logic to check whether there are any notifications.</span></span> <span data-ttu-id="d52d0-197">通知がある場合は、詳細を含む通知オブジェクトを作成し、応答と共に返します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-197">If there are, create a notification object that contains the details, and return it together with the response.</span></span> <span data-ttu-id="d52d0-198">その後、POS が応答を解析し、通知を表示します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-198">The POS will then parse the response and show the notification.</span></span> <span data-ttu-id="d52d0-199">テンプレートに基づくコード例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-199">The following code example is based on the template.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d52d0-200">プロセス メソッド内のサンプル実装を削除します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-200">Remove the sample implementation inside the process method.</span></span> <span data-ttu-id="d52d0-201">カスタム ロジックのみを保持します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-201">Keep only the custom logic.</span></span>

    ```csharp
    namespace Contoso
    {
        namespace Commerce.Runtime.NotificationSample
        {
            using System;
            using Microsoft.Dynamics.Commerce.Runtime;
            using Microsoft.Dynamics.Commerce.Runtime.DataModel;
            using Microsoft.Dynamics.Commerce.Runtime.Services.Messages;
            /// <summary>
            /// Service class responsible executing the service requests.
            /// </summary>
            public class NotificationExtensionService : SingleRequestHandler<GetNotificationsExtensionServiceRequest, GetNotificationsExtensionServiceResponse>
            {
                /// <summary>
                /// The handler for the <c>GetNotificationsExtensionServiceRequest</c> request.
                /// </summary>
                /// <param name="request">The request with the operation.</param>
                /// <returns>The notification details for the operation.</returns>
                protected override GetNotificationsExtensionServiceResponse Process(GetNotificationsExtensionServiceRequest request)
                {
                    ThrowIf.Null(request, "request");
                    NotificationDetailCollection details = new NotificationDetailCollection();
                    DateTimeOffset lastNotificationDateTime = DateTimeOffset.Now;
                    string myOperationId = "5000";
                    // do the actual work here
                    if ((request.SubscribedOperation).ToString() == myOperationId)
                    {
                        NotificationDetail detail = new NotificationDetail()
                        {
                        // Text which will display for the notification detail in the POS notification center
                        DisplayText = "Custom notification",
                        // Number of notifications found
                        ItemCount = 1,
                        // Timestamp of creation of latest notification item (Used to determine whether notification is new)
                        LastUpdatedDateTime = lastNotificationDateTime,
                        // Boolean value representing whether the attempt to get notifications for the given operation was successful
                        IsSuccess = true,
                        // If you would like POS to navigate to a specific action property for the given operation
                        // when the notification tile is selected, define the action property as well.
                        ActionProperty = "1"
                        };
                    details.Add(detail);
                    }
                    var serviceResponse = new GetNotificationsExtensionServiceResponse(details);
                    return serviceResponse;
                }
            }
        }
    }
    ```

7. <span data-ttu-id="d52d0-202">変更が完了したら、プロジェクトをビルドし、出力ライブラリを **\\RetailServer\\webroot\\bin\\Ext** にドロップします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-202">After you've completed your changes, build the project, and drop the output library into **\\RetailServer\\webroot\\bin\\Ext**.</span></span>
8. <span data-ttu-id="d52d0-203">**CommerceRuntime.Ext.config** ファイルに出力ライブラリを登録します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-203">Register the output library in the **CommerceRuntime.Ext.config** file.</span></span>
9. <span data-ttu-id="d52d0-204">POS で、CRT 拡張機能で使用されているのと同じ操作 ID を使用して、新しい操作を作成します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-204">In the POS, create a new operation that has the same operation ID that is used in the CRT extension.</span></span> <span data-ttu-id="d52d0-205">この例では、操作 ID は **5000** です。</span><span class="sxs-lookup"><span data-stu-id="d52d0-205">In this example, the operation ID is **5000**.</span></span> <span data-ttu-id="d52d0-206">5000 以上の任意の操作 ID を使用できます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-206">You can use any operation ID that is above 5000.</span></span>
10. <span data-ttu-id="d52d0-207">POS ユーザーが通知タイルを選択すると、POS フレームワークは使用される操作 ID の操作ハンドラーを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-207">When the POS user selects the notification tile, the POS framework calls the operation handler for the operation ID that is used.</span></span> <span data-ttu-id="d52d0-208">ハンドラー内で、POS ユーザーが通知を選択したときに行われる特定の動作について、必要なロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-208">Inside the handler, add the required logic to specify what should happen when the POS user selects the notification.</span></span> <span data-ttu-id="d52d0-209">POS 操作要求、応答、およびハンドラーの作成方法については、 [販売時点管理 (POS) での注文通知の表示](add-POS-operations.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d52d0-209">For information about how to create a POS operation request, response, and handler, see [Show order notifications in the point of sale (POS)](add-POS-operations.md).</span></span>

    > [!NOTE]
    > <span data-ttu-id="d52d0-210">通知の詳細エンティティのアクション プロパティが POS 操作要求に送信されます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-210">The action property in the Notification detail entity will be sent to the POS operation request.</span></span> <span data-ttu-id="d52d0-211">このアクション プロパティを使用すると、通知サービス から POS にカスタム情報を渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-211">Use that action property to pass any custom information from the notification service to the POS.</span></span>

11. <span data-ttu-id="d52d0-212">[販売時点管理 (POS) での注文通知の表示](../notifications-pos.md) の指示に従って、通知スケジューラをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-212">Configure the notification scheduler according to the instructions in [Show order notifications in the point of sale (POS)](../notifications-pos.md).</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="d52d0-213">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="d52d0-213">Validate the customization</span></span>

1. <span data-ttu-id="d52d0-214">拡張 Cloud POS または Modern POS アプリケーションを開きます。</span><span class="sxs-lookup"><span data-stu-id="d52d0-214">Open the extended Cloud POS or Modern POS application.</span></span>

    <span data-ttu-id="d52d0-215">POS は、通知スケジューラのコンフィギュレーションに基づいて通知サービスをトリガーします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-215">The POS triggers the notification service, based on your notification scheduler configuration.</span></span>

3. <span data-ttu-id="d52d0-216">CRT プロジェクトを w3wp.exe にアタッチして、CRT コードをデバッグします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-216">Debug the CRT code by attaching the CRT project to w3wp.exe.</span></span> <span data-ttu-id="d52d0-217">このブレークポイントは、通知サービスが POS から呼び出されたときに必ずヒットします。</span><span class="sxs-lookup"><span data-stu-id="d52d0-217">The breakpoint should be hit whenever the notification service is called from the POS.</span></span>
4. <span data-ttu-id="d52d0-218">POS で通知を受信したら、通知をクリック選択します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-218">When the notification is received in the POS, select it.</span></span> <span data-ttu-id="d52d0-219">POS 操作ハンドラーを呼び出し、ハンドラー内に記述されたカスタム ロジックを実行します。</span><span class="sxs-lookup"><span data-stu-id="d52d0-219">The notification should call the POS operation handler and run the custom logic that is written inside it.</span></span>
