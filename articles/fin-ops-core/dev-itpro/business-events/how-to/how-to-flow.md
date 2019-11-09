---
title: ビジネス イベントおよび Microsoft Flow
description: このトピックでは、コネクタを使い Microsoft Flow で使用可能なビジネス イベントに関する情報を提供します。
author: ibenbouzid
manager: AnnBe
ms.date: 08/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: imbenbou
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 0d7572b29f55f160609d4841933317a309854fc5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183442"
---
# <a name="business-events-and-microsoft-flow"></a><span data-ttu-id="186cd-103">ビジネス イベントおよび Microsoft Flow</span><span class="sxs-lookup"><span data-stu-id="186cd-103">Business events and Microsoft Flow</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="186cd-104">このトピックでは、Microsoft Flow エンドポイントからビジネスイ ベントを設定および使用する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="186cd-104">This topic provides steps detailing how to configure and consume a business event from a Microsoft Flow endpoint.</span></span>

<span data-ttu-id="186cd-105">このトピックでは、以下のタスクを実行する方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="186cd-105">This topic shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="186cd-106">新規 Microsoft Flow の作成</span><span class="sxs-lookup"><span data-stu-id="186cd-106">Create a new Microsoft Flow.</span></span>
-   <span data-ttu-id="186cd-107">ビジネス イベントのトリガー</span><span class="sxs-lookup"><span data-stu-id="186cd-107">Trigger a business event.</span></span>

## <a name="create-a-new-microsoft-flow"></a><span data-ttu-id="186cd-108">新しい Microsoft Flow の作成</span><span class="sxs-lookup"><span data-stu-id="186cd-108">Create a new Microsoft Flow</span></span>

1.  <span data-ttu-id="186cd-109">Microsoft Flow portal にサインインします。</span><span class="sxs-lookup"><span data-stu-id="186cd-109">Sign in to Microsoft Flow portal.</span></span>

2.  <span data-ttu-id="186cd-110">フローリソースを作成するために必要なアクセス権限のある既存の環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-110">Select an existing environment where you have the permissions needed to create a flow resource.</span></span> <span data-ttu-id="186cd-111">既定の環境は、すべての会社に対して開かれています。</span><span class="sxs-lookup"><span data-stu-id="186cd-111">The default environment is open to all companies.</span></span>

3.  <span data-ttu-id="186cd-112">**空白から新規 \> を作成する**選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-112">Select **New \> Create from blank**.</span></span>

4.  <span data-ttu-id="186cd-113">**Dynamics 365 for Finance and Operations** を検索して、コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-113">Search for **Dynamics 365 for Finance and Operations** and select the connector.</span></span>
     
5.  <span data-ttu-id="186cd-114">**ビジネス イベントが発生した場合**という名称のトリガーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="186cd-114">You will notice a trigger named **When a Business Event occurs**.</span></span> <span data-ttu-id="186cd-115">このトリガーを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-115">Select this trigger.</span></span>

6.  <span data-ttu-id="186cd-116">環境インスタンス、カテゴリ、イベント名称、法的エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-116">Select your environment instance, category, event name, and legal entity.</span></span> 
    > [!TIP]
    > <span data-ttu-id="186cd-117">環境インスタンス URL の一部またはイベント名の一部のみを入力することによって、フローのオート コンプリート機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="186cd-117">Take advantage of the auto-complete that Flow provides by entering only part of the environment instance URL or part of the event name.</span></span>

    <img alt="Microsoft Flow buisness event trigger" src="../../media/BEF-Howto-Flow-04.png" width="50%">

7.  <span data-ttu-id="186cd-118">**新規ステップ** ボタンを選択して新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="186cd-118">Select the **New Step** button to add a new action.</span></span>

8.  <span data-ttu-id="186cd-119">**JSON解析** データ処理を検索します。</span><span class="sxs-lookup"><span data-stu-id="186cd-119">Search for the **Parse JSON** data operation.</span></span> <span data-ttu-id="186cd-120">この手順は、データ コントラクトのスキーマを使用して、メッセージを解析するために必要となります。</span><span class="sxs-lookup"><span data-stu-id="186cd-120">This step is needed to parse the message with the schema of the data contract.</span></span>

    <img alt="Parse JSON action " src="../../media/BEF-Howto-Flow-06.png" width="50%">

9.  <span data-ttu-id="186cd-121">**Jsonの解析** アクションの コンテンツ フィールドを選択すると、前のステップの **Body** がオプションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="186cd-121">Select the content field of **Parse Json** action, then the **Body** output from the previous step should appear as an option.</span></span> <span data-ttu-id="186cd-122">**Body** を選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-122">Select **Body**.</span></span>

    <img alt="Parse JSON input " src="../../media/BEF-Howto-Flow-07.png" width="50%">

10. <span data-ttu-id="186cd-123">コントラクトのスキーマを入力します。</span><span class="sxs-lookup"><span data-stu-id="186cd-123">Enter the schema of the contract.</span></span> <span data-ttu-id="186cd-124">アプリでは、サンプルのペイロードしか提供されないため、ペイロードからスキーマを生成する Microsoft Flow の機能を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="186cd-124">Because the app provides only a sample payload you can use the Microsoft Flow capability to generate a schema from a payload.</span></span> <span data-ttu-id="186cd-125">カタログ内のイベントを選択し (例えば、顧客の支払)、**スキーマのダウンロード**リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-125">Select an event in the catalog (for example, Customer Payment) and select the **Download schema** link.</span></span> <span data-ttu-id="186cd-126">テキストファイルがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="186cd-126">This will download a text file.</span></span> <span data-ttu-id="186cd-127">テキストファイルを開き、内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="186cd-127">Open the text file and copy the content.</span></span>

    <img alt="Event payload" src="../../media/BEF-Howto-Flow-08.png" width="50%">

11. <span data-ttu-id="186cd-128">Microsoft Flow に戻り、 **サンプル ペイロードを使用してスキーマを生成する** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-128">Go Back to Microsoft Flow and select the **Use sample payload to generate schema** link.</span></span> <span data-ttu-id="186cd-129">テキストファイルの内容を貼り付け、 **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-129">Paste your text file content and select **Done**.</span></span>

    <img alt="Parse JSON schema input " src="../../media/BEF-Howto-Flow-09.png" width="70%">

12. <span data-ttu-id="186cd-130">サンプル ペイロードの品質により、ジェネレーターは整数と実数を区別できません。</span><span class="sxs-lookup"><span data-stu-id="186cd-130">Depending on the quality of your sample payload, your generator will not be able to distinguish between an integer and a real number.</span></span> <span data-ttu-id="186cd-131">これは、サンプル ペイロードに実数が整数として提供される場合に該当します。</span><span class="sxs-lookup"><span data-stu-id="186cd-131">This is true if the real number is provided as a whole number in the sample payload.</span></span> <span data-ttu-id="186cd-132">生成されたスキーマを確認し、「整数」を「数値」に変更する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="186cd-132">Review your generated schema and check if you need to change an “integer” into “number”.</span></span> <span data-ttu-id="186cd-133">(JSONでは、"数値" データ型は実数値を意味します)。</span><span class="sxs-lookup"><span data-stu-id="186cd-133">(In JSON, a “number” data type means real number).</span></span>

    <img alt="JSON data types " src="../../media/BEF-Howto-Flow-10.png" width="100%">

13.  <span data-ttu-id="186cd-134">ビジネス イベント コンテンツを使用するための最終アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-134">Choose another final action to consume the business event content.</span></span> <span data-ttu-id="186cd-135">たとえば、電子メールで (または、テキストメッセージをチームに共有する) 支払の詳細を顧客に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="186cd-135">For instance, you can send an email (or post a text message to Teams) to notify the customer about payment details.</span></span> <span data-ttu-id="186cd-136">**電子メールの送信** アクションを検索し、自分の Office 365 アカウントにログインします。</span><span class="sxs-lookup"><span data-stu-id="186cd-136">Search for the **Send email** action, then sign in to your Office 365 account.</span></span>

14.  <span data-ttu-id="186cd-137">メッセージの本文および、必須項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="186cd-137">Fill in the message with the required fields.</span></span>

   <img alt="Microsoft Flow send email action " src="../../media/BEF-Howto-Flow-12.png" width="70%">

15. <span data-ttu-id="186cd-138">フローを保存します。</span><span class="sxs-lookup"><span data-stu-id="186cd-138">Save Flow.</span></span>

## <a name="trigger-a-business-event"></a><span data-ttu-id="186cd-139">ビジネス イベント の トリガー</span><span class="sxs-lookup"><span data-stu-id="186cd-139">Trigger a Business Event</span></span>

<span data-ttu-id="186cd-140">Microsoft Flow では、アプリケーションを自動的にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="186cd-140">Microsoft Flow can configure the application automatically for you.</span></span> <span data-ttu-id="186cd-141">フローを保存すると、エンドポイントが作成され、ビジネス イベントが有効となります。</span><span class="sxs-lookup"><span data-stu-id="186cd-141">After you save your Flow it creates an endpoint, then it activates the business event for you.</span></span> <span data-ttu-id="186cd-142">イベントを起動する前に、エンドポイントが正しく構成されていることを確認する以外に、必要とされる構成手順はありません。</span><span class="sxs-lookup"><span data-stu-id="186cd-142">There is no remaining configuration step apart from verifying that the endpoint has been correctly configured before triggering an event.</span></span>

1. <span data-ttu-id="186cd-143">クライアントにサイン インします。</span><span class="sxs-lookup"><span data-stu-id="186cd-143">Sign in to the client.</span></span>

2.  <span data-ttu-id="186cd-144">**システム管理 \> 設定 \> ビジネス イベント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="186cd-144">Go to **System Administration \> Setup \> Business Events**.</span></span>

3.  <span data-ttu-id="186cd-145">**エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="186cd-145">Select **Endpoints**.</span></span>

4.  <span data-ttu-id="186cd-146">新たなエンドポイントが作成され、名称にGUIDが追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="186cd-146">Verify that a new endpoint has been created with a GUID appended in the name.</span></span>

    <img alt="Microsoft Flow buiness event GUID" src="../../media/BEF-Howto-Flow-13.png" width="100%">

5.  <span data-ttu-id="186cd-147">**有効なイベント** タブをオンにした場合は、法的エンティティGBSIに対し **支払転記済** が有効化されていることも確認することができます。</span><span class="sxs-lookup"><span data-stu-id="186cd-147">If you check the **Active events** tab you can also verify that “**Payment Posted**” is activated for legal entity GBSI.</span></span>

    <img alt="Active business events " src="../../media/BEF-Howto-Flow-14.png" width="100%">

6.  <span data-ttu-id="186cd-148">最後の手順では、転記された顧客支払のビジネス イベントをトリガーし、フローの実行と顧客の支払詳細を含む電子メールを受信するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="186cd-148">The final step is to trigger the business event of a posted customer payment and check whether the Flow runs and you receive an email with customer payment details.</span></span>

## <a name="troubleshooting-a-flow"></a><span data-ttu-id="186cd-149">フローのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="186cd-149">Troubleshooting a Flow</span></span>
<span data-ttu-id="186cd-150">トラブルシューティングの推奨事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="186cd-150">Here are some troubleshooting suggestions:</span></span>
- <span data-ttu-id="186cd-151">Microsoft Flow は、実行の完全な履歴を表示します。この情報を確認することにより、失敗しているフローについてどのような問題があるかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="186cd-151">Microsoft Flow provides a full history of runs so can review this information to determine what might be wrong with a failing Flow.</span></span>
- <span data-ttu-id="186cd-152">失敗した実行を確認する場合は、トリガーおよびアクション ブロックの入力と出力を慎重に確認してください。</span><span class="sxs-lookup"><span data-stu-id="186cd-152">When reviewing a failed run, carefully review the inputs and outputs of trigger and action blocks.</span></span> 
- <span data-ttu-id="186cd-153">フローに変更が加えられたら、最後の実行または特定の実行に移動し、入力を**再送信**してフローを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="186cd-153">After changes have been made to Flow, go to the latest run or a particular run, and **Resubmit** the inputs to run the Flow again.</span></span>