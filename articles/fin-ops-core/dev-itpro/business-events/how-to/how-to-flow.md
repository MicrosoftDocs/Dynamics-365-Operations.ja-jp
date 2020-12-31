---
title: ビジネス イベントと Microsoft Power Automate
description: このトピックでは、コネクタを使い Microsoft Power Automate で使用可能なビジネス イベントに関する情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 11/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 27
ms.dyn365.ops.version: 2019-6-30
ms.openlocfilehash: 27d935ecd9e676a19a3bce2470878ad2b435b8ee
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688107"
---
# <a name="business-events-and-microsoft-power-automate"></a><span data-ttu-id="373eb-103">ビジネス イベントと Microsoft Power Automate</span><span class="sxs-lookup"><span data-stu-id="373eb-103">Business events and Microsoft Power Automate</span></span>

[!include[banner](../../includes/banner.md)]

<span data-ttu-id="373eb-104">このトピックでは、Power Automate エンドポイントからビジネスイ ベントを設定および使用する手順を示します。</span><span class="sxs-lookup"><span data-stu-id="373eb-104">This topic provides steps detailing how to configure and consume a business event from a Power Automate endpoint.</span></span>

<span data-ttu-id="373eb-105">このトピックでは、以下のタスクを実行する方法について説明します:</span><span class="sxs-lookup"><span data-stu-id="373eb-105">This topic shows how to perform the following tasks:</span></span>

-   <span data-ttu-id="373eb-106">Power Automate で、新しいフローを作成します。</span><span class="sxs-lookup"><span data-stu-id="373eb-106">Create a new flow in Power Automate.</span></span>
-   <span data-ttu-id="373eb-107">ビジネス イベントのトリガー</span><span class="sxs-lookup"><span data-stu-id="373eb-107">Trigger a business event.</span></span>

## <a name="create-a-new-flow-in-power-automate"></a><span data-ttu-id="373eb-108">Power Automate で、新しいフローを作成する</span><span class="sxs-lookup"><span data-stu-id="373eb-108">Create a new flow in Power Automate</span></span>

1.  <span data-ttu-id="373eb-109">Power Automate portal にサインインします。</span><span class="sxs-lookup"><span data-stu-id="373eb-109">Sign in to Power Automate portal.</span></span>

2.  <span data-ttu-id="373eb-110">Power Automate リソースを作成するために必要なアクセス許可のある既存の環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-110">Select an existing environment where you have the permissions needed to create a Power Automate resource.</span></span> <span data-ttu-id="373eb-111">既定の環境は、すべての会社に対して開かれています。</span><span class="sxs-lookup"><span data-stu-id="373eb-111">The default environment is open to all companies.</span></span>

3.  <span data-ttu-id="373eb-112">**空白から新規 \> を作成する** 選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-112">Select **New \> Create from blank**.</span></span>

4.  <span data-ttu-id="373eb-113">**Dynamics 365 for Finance and Operations** を検索して、コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-113">Search for **Dynamics 365 for Finance and Operations** and select the connector.</span></span>
     
5.  <span data-ttu-id="373eb-114">**ビジネス イベントが発生した場合** という名称のトリガーを確認できます。</span><span class="sxs-lookup"><span data-stu-id="373eb-114">You will notice a trigger named **When a Business Event occurs**.</span></span> <span data-ttu-id="373eb-115">このトリガーを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-115">Select this trigger.</span></span>

6.  <span data-ttu-id="373eb-116">環境インスタンス、カテゴリ、イベント名称、法的エンティティを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-116">Select your environment instance, category, event name, and legal entity.</span></span> 
    > [!TIP]
    > <span data-ttu-id="373eb-117">環境インスタンス URL の一部またはイベント名の一部のみを入力することで Power Automate が提供するオート コンプリート機能を利用できます。</span><span class="sxs-lookup"><span data-stu-id="373eb-117">Take advantage of the auto-complete that Power Automate provides by entering only part of the environment instance URL or part of the event name.</span></span>

    <img alt="Microsoft Power Automate buisness event trigger" src="../../media/BEF-Howto-Flow-04.png" width="50%">

7.  <span data-ttu-id="373eb-118">**新規ステップ** ボタンを選択して新しいアクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="373eb-118">Select the **New Step** button to add a new action.</span></span>

8.  <span data-ttu-id="373eb-119">**JSON解析** データ処理を検索します。</span><span class="sxs-lookup"><span data-stu-id="373eb-119">Search for the **Parse JSON** data operation.</span></span> <span data-ttu-id="373eb-120">この手順は、データ コントラクトのスキーマを使用して、メッセージを解析するために必要となります。</span><span class="sxs-lookup"><span data-stu-id="373eb-120">This step is needed to parse the message with the schema of the data contract.</span></span>

    <img alt="Parse JSON action " src="../../media/BEF-Howto-Flow-06.png" width="50%">

9.  <span data-ttu-id="373eb-121">**Jsonの解析** アクションの コンテンツ フィールドを選択すると、前のステップの **Body** がオプションとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="373eb-121">Select the content field of **Parse Json** action, then the **Body** output from the previous step should appear as an option.</span></span> <span data-ttu-id="373eb-122">**Body** を選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-122">Select **Body**.</span></span>

    <img alt="Parse JSON input " src="../../media/BEF-Howto-Flow-07.png" width="50%">

10. <span data-ttu-id="373eb-123">コントラクトのスキーマを入力します。</span><span class="sxs-lookup"><span data-stu-id="373eb-123">Enter the schema of the contract.</span></span> <span data-ttu-id="373eb-124">アプリでは、サンプルのペイロードしか提供されないため、ペイロードからスキーマを生成する Power Automate の機能を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="373eb-124">Because the app provides only a sample payload you can use the Power Automate capability to generate a schema from a payload.</span></span> <span data-ttu-id="373eb-125">カタログ内のイベントを選択し (例えば、顧客の支払)、**スキーマのダウンロード** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-125">Select an event in the catalog (for example, Customer Payment) and select the **Download schema** link.</span></span> <span data-ttu-id="373eb-126">テキストファイルがダウンロードされます。</span><span class="sxs-lookup"><span data-stu-id="373eb-126">This will download a text file.</span></span> <span data-ttu-id="373eb-127">テキストファイルを開き、内容をコピーします。</span><span class="sxs-lookup"><span data-stu-id="373eb-127">Open the text file and copy the content.</span></span>

    <img alt="Event payload" src="../../media/BEF-Howto-Flow-08.png" width="50%">

11. <span data-ttu-id="373eb-128">Power Automate に戻り、 **サンプル ペイロードを使用してスキーマを生成する** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-128">Go Back to Power Automate and select the **Use sample payload to generate schema** link.</span></span> <span data-ttu-id="373eb-129">テキストファイルの内容を貼り付け、 **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-129">Paste your text file content and select **Done**.</span></span>

    <img alt="Parse JSON schema input " src="../../media/BEF-Howto-Flow-09.png" width="70%">

12. <span data-ttu-id="373eb-130">サンプル ペイロードの品質により、ジェネレーターは整数と実数を区別できません。</span><span class="sxs-lookup"><span data-stu-id="373eb-130">Depending on the quality of your sample payload, your generator will not be able to distinguish between an integer and a real number.</span></span> <span data-ttu-id="373eb-131">これは、サンプル ペイロードに実数が整数として提供される場合に該当します。</span><span class="sxs-lookup"><span data-stu-id="373eb-131">This is true if the real number is provided as a whole number in the sample payload.</span></span> <span data-ttu-id="373eb-132">生成されたスキーマを確認し、「整数」を「数値」に変更する必要があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="373eb-132">Review your generated schema and check if you need to change an “integer” into “number”.</span></span> <span data-ttu-id="373eb-133">(JSONでは、"数値" データ型は実数値を意味します)。</span><span class="sxs-lookup"><span data-stu-id="373eb-133">(In JSON, a “number” data type means real number).</span></span>

    <img alt="JSON data types " src="../../media/BEF-Howto-Flow-10.png" width="100%">

13.  <span data-ttu-id="373eb-134">ビジネス イベント コンテンツを使用するための最終アクションを選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-134">Choose another final action to consume the business event content.</span></span> <span data-ttu-id="373eb-135">たとえば、電子メールで (または、テキストメッセージをチームに共有する) 支払の詳細を顧客に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="373eb-135">For instance, you can send an email (or post a text message to Teams) to notify the customer about payment details.</span></span> <span data-ttu-id="373eb-136">**電子メールの送信** アクションを検索し、自分の Microsoft 365 アカウントにサインインします。</span><span class="sxs-lookup"><span data-stu-id="373eb-136">Search for the **Send email** action, then sign in to your Microsoft 365 account.</span></span>

14.  <span data-ttu-id="373eb-137">メッセージの本文および、必須項目を入力します。</span><span class="sxs-lookup"><span data-stu-id="373eb-137">Fill in the message with the required fields.</span></span>

     <img alt="Microsoft Power Automate send email action " src="../../media/BEF-Howto-Flow-12.png" width="70%">

15. <span data-ttu-id="373eb-138">フローを保存します。</span><span class="sxs-lookup"><span data-stu-id="373eb-138">Save the flow.</span></span>

## <a name="trigger-a-business-event"></a><span data-ttu-id="373eb-139">ビジネス イベント の トリガー</span><span class="sxs-lookup"><span data-stu-id="373eb-139">Trigger a Business Event</span></span>

<span data-ttu-id="373eb-140">Power Automate では、アプリケーションを自動的にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="373eb-140">Power Automate can configure the application automatically for you.</span></span> <span data-ttu-id="373eb-141">フローを保存すると、エンドポイントが作成され、ビジネス イベントが有効となります。</span><span class="sxs-lookup"><span data-stu-id="373eb-141">After you save your flow, it creates an endpoint, then it activates the business event for you.</span></span> <span data-ttu-id="373eb-142">イベントを起動する前に、エンドポイントが正しく構成されていることを確認する以外に、必要とされる構成手順はありません。</span><span class="sxs-lookup"><span data-stu-id="373eb-142">There is no remaining configuration step apart from verifying that the endpoint has been correctly configured before triggering an event.</span></span>

1. <span data-ttu-id="373eb-143">クライアントにサイン インします。</span><span class="sxs-lookup"><span data-stu-id="373eb-143">Sign in to the client.</span></span>

2.  <span data-ttu-id="373eb-144">**システム管理 \> 設定 \> ビジネス イベント** に移動します。</span><span class="sxs-lookup"><span data-stu-id="373eb-144">Go to **System Administration \> Setup \> Business Events**.</span></span>

3.  <span data-ttu-id="373eb-145">**エンドポイント** を選択します。</span><span class="sxs-lookup"><span data-stu-id="373eb-145">Select **Endpoints**.</span></span>

4.  <span data-ttu-id="373eb-146">新たなエンドポイントが作成され、名称にGUIDが追加されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="373eb-146">Verify that a new endpoint has been created with a GUID appended in the name.</span></span>

    <img alt="Microsoft Power Automate buiness event GUID" src="../../media/BEF-Howto-Flow-13.png" width="100%">

5.  <span data-ttu-id="373eb-147">**有効なイベント** タブをオンにした場合は、法的エンティティGBSIに対し **支払転記済** が有効化されていることも確認することができます。</span><span class="sxs-lookup"><span data-stu-id="373eb-147">If you check the **Active events** tab you can also verify that “**Payment Posted**” is activated for legal entity GBSI.</span></span>

    <img alt="Active business events " src="../../media/BEF-Howto-Flow-14.png" width="100%">

6.  <span data-ttu-id="373eb-148">最後の手順では、転記された顧客支払のビジネス イベントをトリガーし、フローの実行と顧客の支払詳細を含む電子メールを受信するかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="373eb-148">The final step is to trigger the business event of a posted customer payment and check whether the flow runs and you receive an email with customer payment details.</span></span>

## <a name="troubleshooting-a-flow"></a><span data-ttu-id="373eb-149">フローのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="373eb-149">Troubleshooting a flow</span></span>
<span data-ttu-id="373eb-150">トラブルシューティングの推奨事項を次に示します。</span><span class="sxs-lookup"><span data-stu-id="373eb-150">Here are some troubleshooting suggestions:</span></span>
- <span data-ttu-id="373eb-151">Power Automate では、失敗したフローの問題点を特定するのに役立つ、実行の完全な履歴を提供しています。</span><span class="sxs-lookup"><span data-stu-id="373eb-151">Power Automate provides a full history of runs to help determine what might be wrong with a failing flow.</span></span>
- <span data-ttu-id="373eb-152">失敗した実行を確認する場合は、トリガーおよびアクション ブロックの入力と出力を慎重に確認してください。</span><span class="sxs-lookup"><span data-stu-id="373eb-152">When reviewing a failed run, carefully review the inputs and outputs of trigger and action blocks.</span></span> 
- <span data-ttu-id="373eb-153">フローに変更が加えられたら、最新の実行または特定の実行に移動し、入力を **再送信** して、フローを再度実行します。</span><span class="sxs-lookup"><span data-stu-id="373eb-153">After changes have been made to the flow, go to the latest run or a particular run, and **Resubmit** the inputs to run the flow again.</span></span>
