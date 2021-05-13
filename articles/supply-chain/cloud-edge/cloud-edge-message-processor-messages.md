---
title: メッセージ プロセッサのメッセージ
description: このトピックでは、スケール ユニット ワークロードのッセージ プロセッサ メッセージ機能に関する情報を提供します。
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938253"
---
# <a name="message-processor-messages"></a><span data-ttu-id="5f7ea-103">メッセージ プロセッサのメッセージ</span><span class="sxs-lookup"><span data-stu-id="5f7ea-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5f7ea-104">ッセージ プロセッサ メッセージは、[製造ワークロード](cloud-edge-workload-manufacturing.md)および[倉庫管理ワークロード](cloud-edge-workload-warehousing.md)に対してクラウドおよびエッジのスケール ユニットを実行している場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="5f7ea-105">ハブとスケール ユニットの展開環境間での同期を維持するために大量のデータが交換されますが、*メッセージ プロセッサ* によって処理されるデータ交換はその一部分だけです。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="5f7ea-106">**システム管理 > メッセージ プロセッサ > メッセージ プロセッサ メッセージ** から、メッセージ プロセッサによって処理されたメッセージを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="5f7ea-107">メッセージ グリッドの列およびフィルター</span><span class="sxs-lookup"><span data-stu-id="5f7ea-107">Message grid columns and filters</span></span>

<span data-ttu-id="5f7ea-108">**メッセージ プロセッサ メッセージ** ページの上部にあるフィールドを使用して、検索する特定のメッセージ を見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="5f7ea-109">これらのフィルターのほとんどは、メッセージ グリッド列のヘッダーと一致します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="5f7ea-110">次のフィルターと列のヘッダーが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="5f7ea-111">**メッセージ タイプ**: メッセージのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="5f7ea-112">**メッセージ キュー**: メッセージを処理するキューの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="5f7ea-113">次のキューが用意されています。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-113">The following queues are provided:</span></span>
  - <span data-ttu-id="5f7ea-114">*ハブに対するスケール ユニット*</span><span class="sxs-lookup"><span data-stu-id="5f7ea-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="5f7ea-115">*ハブから倉庫実行スケール ユニット*</span><span class="sxs-lookup"><span data-stu-id="5f7ea-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="5f7ea-116">*ハブから製造実行スケール ユニット*</span><span class="sxs-lookup"><span data-stu-id="5f7ea-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="5f7ea-117">**メッセージの状態** – メッセージの状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="5f7ea-118">次の状態があります。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-118">The following states exists:</span></span>
  - <span data-ttu-id="5f7ea-119">*キューに設定* – メッセージ プロセッサでメッセージを処理する準備ができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="5f7ea-120">*処理済み* – メッセージがメッセージ プロセッサで正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="5f7ea-121">*取消済* – メッセージを処理しましたが、処理に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="5f7ea-122">**メッセージ コンテンツ** – このフィルターはメッセージの内容を全文検索します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="5f7ea-123">(グリッドにメッセージ コンテンツは表示されません。) このフィルターでは、ほとんどの特殊な記号 (「-」など) をスペースとして処理し、すべての空白文字をブール OR 演算子として処理します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="5f7ea-124">T= たとえば、「USMF-123456」と等しい特定の `journalid` 値を検索すると、長いリストの場合ように、システムは「USMF」または「123456」を含むすべてのメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="5f7ea-125">したがって、「123456」と入力した方がより正確な結果が得られるでしょう。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="5f7ea-126">メッセージ タイプの例: 在庫調整財務更新の要求</span><span class="sxs-lookup"><span data-stu-id="5f7ea-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="5f7ea-127">たとえば、**メッセージ タイプ** *在庫調整財務更新の要求* は、作業者が倉庫アプリを使用してスケール ユニットの倉庫管理ワークロードの[在庫調整の登録](cloud-edge-warehouse-inventory-adjustment.md)を行う場合に、ハブ上の棚卸仕訳帳の作成および転記を行うために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="5f7ea-128">この特定のプロセスの生成元はスケール ユニットなので、**ッセージ キュー** フィールドに *スケール ユニットからハブへ* の値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="5f7ea-129">このメッセージ タイプの場合、スケール ユニットのワークロードは、メッセージを倉庫アプリの在庫調整操作の一部として記録します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="5f7ea-130">メッセージ データは、[Commerce Data Exchange アーキテクチャ](../../commerce/commerce-architecture.md)で使用されるのと同じプロセスの一部としてハブに転送されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="5f7ea-131">メッセージが更新され、**メッセージの状態** が *キューに設定* として表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="5f7ea-132">メッセージ プロセッサはメッセージの処理を試行し、成功時は *処理済* に、失敗時は *取消済* に **メッセージの状態** を更新します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="5f7ea-133">メッセージ ログ、メッセージ コンテンツ、および詳細の表示</span><span class="sxs-lookup"><span data-stu-id="5f7ea-133">View the message log, message content, and details</span></span>

<span data-ttu-id="5f7ea-134">グリッドで選択し、各処理イベントが表示されているメッセージ グリッドの下にある **ログ** または **メッセージ コンテンツ** タブを開くことによって、メッセージに関する詳細情報を検索することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="5f7ea-135">**メッセージ コンテンツ** は **メッセージ タイプ** に依存するため、テキストの長さが異なります。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="5f7ea-136">一般的なメッセージ コンテンツのテキストは、**{** で始まって **}** で終わり、その間に **:** と *USMF-123456* のような値に続いて `journalId` などのフィールド名があります。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="5f7ea-137">**ログ** タブのツールバーには次のボタンが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="5f7ea-138">**ログ** – 処理結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="5f7ea-139">これは、**処理結果** が *失敗* であるメッセージについて、処理が失敗した理由を理解するのに特に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="5f7ea-140">**バンドル** – 複数のメッセージ処理操作を同じバッチ プロセスの一部として実行することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="5f7ea-141">このボタンを選択して、この詳細データを表示します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="5f7ea-142">たとえば、システムが指定された順序で特定のメッセージを処理することが必要もなる依存関係が存在するかどうかを確認できます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="5f7ea-143">メッセージ プロセッサのバッチ ジョブ</span><span class="sxs-lookup"><span data-stu-id="5f7ea-143">Message processor batch job</span></span>

<span data-ttu-id="5f7ea-144">クラウドおよびエッジの配置を実行する場合、処理に対して新しいメッセージが作成されるとき、*メッセージ プロセッサのバッチ ジョブ* が自動的に呼び出されるので、このジョブを手動でスケジュール必要はありません。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="5f7ea-145">必要に応じて、**システム管理 > メッセージ プロセッサ > メッセージ プロセッサ** に移動して、バッチ ジョブにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="5f7ea-146">メッセージの手動処理またはキャンセル</span><span class="sxs-lookup"><span data-stu-id="5f7ea-146">Manually process or cancel a message</span></span>

<span data-ttu-id="5f7ea-147">必要な場合、現在の状態に応じて、メッセージを手動で処理またはキャンセルすることができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="5f7ea-148">そのためには、グリッドでメッセージを選択し、アクション ウィンドウで **処理** または **キャンセル** を選択します</span><span class="sxs-lookup"><span data-stu-id="5f7ea-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="5f7ea-149">失敗した処理結果に対する警告を配信するビジネス イベントの設定</span><span class="sxs-lookup"><span data-stu-id="5f7ea-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="5f7ea-150">**メッセージの状態** の値を *取消済* でフィルター処理して失敗したメッセージを照会することに加え、失敗した処理結果について警告するためにハブで[ビジネス イベント](../../fin-ops-core/dev-itpro/business-events/home-page.md)を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="5f7ea-151">そのためには、**ビジネス イベント カタログ** ページ (**システム管理 > 設定 > ビジネス イベント > ビジネス イベント カタログ**) で *メッセージ プロセッサ メッセージ処理済* と名前の付けられたビジネス イベントを有効化します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="5f7ea-152">有効化プロセスの一部として、イベントが 1 つまたはすべての法人に指定されているかどうかを指定するよう案内が表示され、最初に定義する必要がある **エンドポイント** の名前を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="5f7ea-153">**ビジネス イベントの発生時** が (*HTTPS* ではなく) *Microsoft Power Automate* に設定されている場合、**エンドポイント名** は、*Microsoft Power Automate* の設定に基づいて Supply Chain Management で自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="5f7ea-154">Microsoft Power Automate の例</span><span class="sxs-lookup"><span data-stu-id="5f7ea-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="5f7ea-155">この例では、*Microsoft Power Automate* で **ビジネス イベントの発生時** を使用して、InfoLog メッセージとハブの展開で失敗した特定のメッセージの **メッセージ プロセッサ メッセージ** を開くハイパーリンクを含む電子メールを送信します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="5f7ea-156">異なるチャネルを使用して並列で通知を送信し、イベント データに基づく受信者を制御する追加ロジックを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="5f7ea-157">[Power Automate](https://preview.flow.microsoft.com) では、次の図に示されているように、**JSON 解析** および **電子メール送信** のステップに続くフロー トリガー **ビジネス イベントの発生時 - Finance and Operations アプリ (Dynamics 365)** に対する新しい自動化クラウド フローを作成します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate 自動化クラウド フロー":::

1. <span data-ttu-id="5f7ea-159">**ビジネス イベントの発生時** のステップでは、次の図に示すように、**カテゴリ**、そして **ビジネス イベント** の *メッセージ プロセッサ メッセージ処理済* に続くハブ **インスタンス** の検索または入力を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate ビジネス イベントの発生時のステップ":::

1. <span data-ttu-id="5f7ea-161">**JSON の解析** のステップで、拡張フィールドを定義する **スキーマ** を入力します。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="5f7ea-162">Supply Chain Management の **ビジネス イベント カタログ** ページにある *スキーマのダウンロード* オプションを使用するか、または例にあるスキーマ テキストを貼り付けて開始することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="5f7ea-163">この例のテキストは、次の図の後で提供されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate JSON 解析のステップ":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="5f7ea-165">**電子メールの送信** ステップにおいて、個別のフィールドを選択するか、または電子メール本文の例を **本文** フィールドに貼り付けて開始することができます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="5f7ea-166">この例は、次の図の後で提供されます。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate 電子メール送信ステップ":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="5f7ea-168">ビジネス イベントを保存すると自動的に有効化され、Supply Chain Management の一部として使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="5f7ea-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
