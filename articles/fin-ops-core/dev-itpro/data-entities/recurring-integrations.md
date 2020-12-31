---
title: 定期統合
description: このトピックでは、定期的な統合について説明します。 データ移行のプロセスや、エンタープライズ システムの内外への移動は、どのプラットフォームでもサポートする必要がある重要な要素です。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 24821
ms.assetid: 70a4f748-b0bd-44b1-a118-56aacb91481c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1223870603885ce82ffc9d7a52317e04667a9c67
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685472"
---
# <a name="recurring-integrations"></a><span data-ttu-id="8b970-104">定期統合</span><span class="sxs-lookup"><span data-stu-id="8b970-104">Recurring integrations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8b970-105">移行を繰り返し行うと以下の処理が行われます:</span><span class="sxs-lookup"><span data-stu-id="8b970-105">Recurring integration does the following things:</span></span>

- <span data-ttu-id="8b970-106">これは、データ エンティティとデータ管理フレームワークで構築されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-106">It builds on data entities and the Data management framework.</span></span>
- <span data-ttu-id="8b970-107">Finance and Operations とあらゆるサード パーティ製アプリケーションやサービスで、ドキュメントまたはファイルの交換を可能にします。</span><span class="sxs-lookup"><span data-stu-id="8b970-107">It enables the exchange of documents or files between Finance and Operations and any third-party application or service.</span></span>
- <span data-ttu-id="8b970-108">複数のドキュメント形式、ソース マッピング、XSLT (Extensible Stylesheet Language Transformations)、およびフィルターをサポートします。</span><span class="sxs-lookup"><span data-stu-id="8b970-108">It supports several document formats, source mapping, Extensible Stylesheet Language Transformations (XSLT), and filters.</span></span>

    ![複数の文書形式のドキュメントまたはファイルを交換](./media/recurring-integrations.png)

- <span data-ttu-id="8b970-110">セキュリティで保護された REST のアプリケーション プログラミング インターフェイス (API) と認証メカニズムを使用して、統合システムからデータを受信し、データを送り返します。</span><span class="sxs-lookup"><span data-stu-id="8b970-110">It uses secure REST application programming interfaces (APIs) and authorization mechanisms to receive data from, and send data back to, integration systems.</span></span>

    ![繰り返し実行される統合を設定](./media/set-up-recurring.png)

## <a name="authorization-for-the-integration-rest-api"></a><span data-ttu-id="8b970-112">REST API 統合の承認</span><span class="sxs-lookup"><span data-stu-id="8b970-112">Authorization for the integration REST API</span></span>
<span data-ttu-id="8b970-113">REST API の統合は、その他の サービス エンドポイント と同じ OAuth 2.0 認証モデルを使用しています。</span><span class="sxs-lookup"><span data-stu-id="8b970-113">The integration REST API uses the same OAuth 2.0 authentication model as the other service endpoints.</span></span> <span data-ttu-id="8b970-114">統合クライアント アプリケーションがこのエンドポイントを使用する前に、Microsoft Azure Active Directory (Azure AD) にアプリケーション ID を作成し、アプリケーションに適切なアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b970-114">Before the integrating client application can consume this endpoint, you must create an application ID in Microsoft Azure Active Directory (Azure AD) and give it appropriate permission to the application.</span></span> <span data-ttu-id="8b970-115">定期的なジョブを作成して有効にするとき、その定期的なジョブとやり取りする Azure AD アプリケーション ID を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="8b970-115">When you create and enable a recurring job, you're prompted to enter the Azure AD application ID that will interact with that recurring job.</span></span> <span data-ttu-id="8b970-116">したがって、アプリケーション ID をメモしておいてください。</span><span class="sxs-lookup"><span data-stu-id="8b970-116">Therefore, be sure to make a note of the application ID.</span></span>

> [!NOTE]
> <span data-ttu-id="8b970-117">この機能は、オンプレミス バージョンの Dynamics 365 Finance + Operations (オンプレミス) ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8b970-117">This feature is not supported with Dynamics 365 Finance + Operations (on-premises).</span></span>

## <a name="set-up-a-data-project-and-recurring-data-jobs"></a><span data-ttu-id="8b970-118">データ プロジェクトと定期的なデータ ジョブを設定</span><span class="sxs-lookup"><span data-stu-id="8b970-118">Set up a data project and recurring data jobs</span></span>
### <a name="create-a-data-project"></a><span data-ttu-id="8b970-119">データ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="8b970-119">Create a data project</span></span>

1. <span data-ttu-id="8b970-120">主要なダッシュ ボードで、**データ管理** タイルを選択し **データ管理** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="8b970-120">On the main dashboard, select the **Data management** tile to open the **Data management** workspace.</span></span>
2. <span data-ttu-id="8b970-121">**インポート** または **エクスポート** タイルを選択し、新しいデータ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="8b970-121">Select the **Import** or **Export** tile to create a new data project.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b970-122">既存のデータ プロジェクトを使用する場合は、**データ プロジェクト** タブにあるデータ プロジェクトのカードで **プロジェクトを読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b970-122">If you have an existing data project, select **Load project** on the card for any data project on the **Data projects** tab.</span></span>

3. <span data-ttu-id="8b970-123">有効なジョブ名、データ ソース、およびエンティティ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b970-123">Enter a valid job name, data source, and entity name.</span></span>
4. <span data-ttu-id="8b970-124">1 つ以上のエンティティのデータ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="8b970-124">Upload a data file for one or more entities.</span></span> <span data-ttu-id="8b970-125">各エンティティが追加されており、エラーが発生していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="8b970-125">Make sure that each entity is added, and that no errors occur.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b970-126">フィールド マップを設定、レビュー、または修正し、受信データに適用する必要がある XSLT ベースの変換を設定するため、各エンティティ データ カードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-126">You can select each entity data card to set up, review, or modify field maps, and to set up XSLT-based transforms that must be applied to inbound data.</span></span> <span data-ttu-id="8b970-127">データ プロジェクトのエクスポートについては、エンティティ カードはフィルター リンクも表示し、フィルター データにフィルターを設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="8b970-127">For export data projects, the entity card also shows a filter link, so that you can set up filters to filter data.</span></span> <span data-ttu-id="8b970-128">現在、データ プロジェクトのすべての定期的なデータ ジョブは、同じフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="8b970-128">Currently, all recurring data jobs in a data project use the same filter.</span></span>

5. <span data-ttu-id="8b970-129">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b970-129">Select **Save**.</span></span>

### <a name="create-a-recurring-data-job"></a><span data-ttu-id="8b970-130">定期的なデータ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="8b970-130">Create a recurring data job</span></span>

1. <span data-ttu-id="8b970-131">**データ プロジェクト** ページで、**定期的なデータ ジョブの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b970-131">On the **Data project** page, select **Create recurring data job**.</span></span>
2. <span data-ttu-id="8b970-132">定期的なデータ ジョブの有効な名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8b970-132">Enter a valid name and a description for the recurring data job.</span></span>
3. <span data-ttu-id="8b970-133">**承認ポリシーの設定** タブに、アプリケーションが生成されているアプリケーション ID を入力し、それを有効になっているとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="8b970-133">On the **Set up authorization policy** tab, enter the application ID that was generated for your application, and mark it as enabled.</span></span>
4. <span data-ttu-id="8b970-134">**詳細オプション** タブを展開し、**ファイル** または **データ パッケージ** のどちらかを指定します。</span><span class="sxs-lookup"><span data-stu-id="8b970-134">Expand **Advanced options** tab, and specify either **File** or **Data package**.</span></span>

    - <span data-ttu-id="8b970-135">**ファイル** – 外部統合によって個々のファイルがプッシュされ、この定期的なデータジョブによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-135">**File** – Your external integration will push individual files so that they can be processed via this recurring data job.</span></span> <span data-ttu-id="8b970-136">この場合、予想されるファイルの形式は、エンティティがデータ プロジェクトに追加されたときに指定された形式と同じです。</span><span class="sxs-lookup"><span data-stu-id="8b970-136">In this case, the format of the file that is expected is the same as the format that was specified when the entity was added to the data project.</span></span>
    - <span data-ttu-id="8b970-137">**データ パッケージ** - 処理のためのデータ パッケージ ファイルのみをプッシュできます。</span><span class="sxs-lookup"><span data-stu-id="8b970-137">**Data package** – You can push only data package files for processing.</span></span> <span data-ttu-id="8b970-138">データ パッケージは、統合ジョブで使用できる 1 つの単位として複数のデータ ファイルを送信できる新しい形式です。</span><span class="sxs-lookup"><span data-stu-id="8b970-138">A data package is a new format that lets you submit multiple data files as a single unit that can be used in integration jobs.</span></span>
    - <span data-ttu-id="8b970-139">**順に処理されるメッセージ** – このオプションを有効にすると、インポート シナリオで受信ファイルを強制的に処理することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-139">**Process messages in order** – You can enable this option to force sequential processing of incoming files in an import scenario.</span></span> <span data-ttu-id="8b970-140">このオプションはファイルにのみ適用され、データ パッケージには適用されません。</span><span class="sxs-lookup"><span data-stu-id="8b970-140">This option is only applicable to files and not data packages.</span></span>

5. <span data-ttu-id="8b970-141">**処理の繰り返しを設定** を選択し、**定期的なアイテムの定義** ダイアログ ボックスで、データ ジョブの有効な繰り返しを設定します。</span><span class="sxs-lookup"><span data-stu-id="8b970-141">Select **Set processing recurrence**, and then, in the **Define recurrence** dialog box, set up a valid recurrence for your data job.</span></span>
6. <span data-ttu-id="8b970-142">オプション: **定期的なアイテムの監視を設定** を選択し、定期的なアイテムの監視を設定します。</span><span class="sxs-lookup"><span data-stu-id="8b970-142">Optional: Select **Set monitoring recurrence**, and set up a monitoring recurrence.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8b970-143">現在のところ、監視の繰り返しは、定期的なデータ ジョブのキューでのみ負荷監視を有効にします。</span><span class="sxs-lookup"><span data-stu-id="8b970-143">Currently, monitoring recurrence enables load monitoring only on the queue for your recurring data job.</span></span> <span data-ttu-id="8b970-144">このサービスを使用してサポートされる追加のポリシーはありません。</span><span class="sxs-lookup"><span data-stu-id="8b970-144">No additional policies are supported via this service.</span></span> <span data-ttu-id="8b970-145">この機能を使用すると、積荷需要が必要な場合に処理の繰り返しを微調整することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-145">You can use this feature to fine-tune the processing recurrence as the load demand requires.</span></span>

7. <span data-ttu-id="8b970-146">**OK** を選択し、確認メッセージ ボックスで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="8b970-146">Select **OK**, and then select **Yes** in the confirmation message box.</span></span>

## <a name="manage-recurring-data-jobs"></a><span data-ttu-id="8b970-147">定期的なデータ ジョブの管理</span><span class="sxs-lookup"><span data-stu-id="8b970-147">Manage recurring data jobs</span></span>
1. <span data-ttu-id="8b970-148">**システム管理** ワークスペース (**システム管理** モジュールではない) で、**データ管理 IT** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="8b970-148">In the **System administration** workspace (not the **System administration** module), select the **Data Management IT** workspace.</span></span>
2. <span data-ttu-id="8b970-149">ワークスペースの **定期的なデータ ジョブ** タブで、定期的なジョブを選択して詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="8b970-149">In the workspace, on the **Recurring data job** tab, select the recurring job to view the details.</span></span> <span data-ttu-id="8b970-150">**スケジュールされたデータ ジョブを管理** ページには、キューに待機しているすべてのメッセージを一覧表示するグリッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8b970-150">The **Manage scheduled data jobs** page contains a grid that lists any messages that are waiting in the queue.</span></span> <span data-ttu-id="8b970-151">したがって、メッセージと処理ステータスを監視できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-151">Therefore, you can monitor messages and the processing status.</span></span>

    ![スケジュール済みデータ ジョブの管理](./media/image013.jpg)

## <a name="submitting-data-to-recurring-data-jobs"></a><span data-ttu-id="8b970-153">定期的なデータ ジョブにデータを送信</span><span class="sxs-lookup"><span data-stu-id="8b970-153">Submitting data to recurring data jobs</span></span>
<span data-ttu-id="8b970-154">統合 REST エンドポイントを使用して、クライアントと統合、ドキュメントの送信 (インポート)、またはダウンロードに使用可能なドキュメントのポーリング (エクスポート) を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-154">You can use integration REST endpoints to integrate with the client, submit documents (import), or poll available documents for download (export).</span></span> <span data-ttu-id="8b970-155">これらのエンドポイントは OAuth をサポートします。</span><span class="sxs-lookup"><span data-stu-id="8b970-155">These endpoints support OAuth.</span></span>

## <a name="integration-rest-apis"></a><span data-ttu-id="8b970-156">REST API の統合</span><span class="sxs-lookup"><span data-stu-id="8b970-156">Integration REST APIs</span></span>
<span data-ttu-id="8b970-157">次の API セットは、統合クライアントとアプリケーション間でデータを交換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-157">The following set of APIs is used to exchange data between the integration client and the application.</span></span>

### <a name="api-for-import-enqueue"></a><span data-ttu-id="8b970-158">インポート (エンキュー) の API</span><span class="sxs-lookup"><span data-stu-id="8b970-158">API for import (enqueue)</span></span>
<span data-ttu-id="8b970-159">次の URL に対して HTTP POST 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="8b970-159">Make an HTTP POST call against the following URL.</span></span>

```Console
https://<base URL>/api/connector/enqueue/<activity ID>?entity=<entity name>
```

<span data-ttu-id="8b970-160">メッセージ本文では、データをメモリ ストリームとして渡せます。</span><span class="sxs-lookup"><span data-stu-id="8b970-160">In the message body, you can the pass the data as a memory stream.</span></span>

<span data-ttu-id="8b970-161">**例**</span><span class="sxs-lookup"><span data-stu-id="8b970-161">**Example**</span></span>

```Console
POST https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/enqueue/%7B6D31E09F-0249-459F-94F0-AAD9C2C47B64%7D?entity=Customer%20Groups
```

<span data-ttu-id="8b970-162">アクティビティ ID を取得するには、**スケジュールされたデータ ジョブの管理** ページの **ID** フィールドで、グローバルで一意の識別子 (GUID) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="8b970-162">To get the activity ID, on the **Manage scheduled data jobs** page, in the **ID** field, copy the globally unique identifier (GUID).</span></span>

![スケジュール済みデータ ジョブ ページの管理での GUID](./media/image015.jpg)

### <a name="api-for-export-dequeue"></a><span data-ttu-id="8b970-164">エクスポート (デキュー) のAPI</span><span class="sxs-lookup"><span data-stu-id="8b970-164">API for export (dequeue)</span></span>
<span data-ttu-id="8b970-165">データ プロジェクトで定義されたすべてのデータ エンティティを含むデータ パッケージを返し、クライアント アプリケーションで解凍して使用できるようにするには、次の構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b970-165">To return a data package that contains all the data entities that were defined in the data project, and that the client application can unzip and consume, use the following structure.</span></span>

```Console
https://<base URL>/api/connector/dequeue/<activity ID>
```

<span data-ttu-id="8b970-166">**例**</span><span class="sxs-lookup"><span data-stu-id="8b970-166">**Example**</span></span>

```Console
GET https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/dequeue/%7BC03BB937-09ED-46DE-86EE-4520D7D7E373%7D
```

<span data-ttu-id="8b970-167">クライアントがデータをダウンロードした後、データを受領したものとしてマークすることができるように、受信確認はアプリケーションに送り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b970-167">After the client downloads the data, an acknowledgment must be sent back to the application, so that you can mark the data as received.</span></span>

<span data-ttu-id="8b970-168">blob にアップロードされたファイルがない場合、デキュー API はそのことを示す応答を返します。</span><span class="sxs-lookup"><span data-stu-id="8b970-168">In cases when there was no file uploaded to the blob, the dequeue API will return a response indicating as such.</span></span>

### <a name="api-for-acknowledgment"></a><span data-ttu-id="8b970-169">確認の API</span><span class="sxs-lookup"><span data-stu-id="8b970-169">API for acknowledgment</span></span>
<span data-ttu-id="8b970-170">次 の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="8b970-170">Use the following API.</span></span>

> [!NOTE]
> <span data-ttu-id="8b970-171">**/dequeue** の要求本文は、 **/ack** POST 要求の本文で送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b970-171">The body of the response of **/dequeue** must be sent in the body of the **/ack** POST request.</span></span>

```Console
https://<base URL>/api/connector/ack/<activity ID>
```

<span data-ttu-id="8b970-172">**例**</span><span class="sxs-lookup"><span data-stu-id="8b970-172">**Example**</span></span>

```Console
POST https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/ack/%7BC03BB937-09ED-46DE-86EE-4520D7D7E373%7D
```
> [!NOTE] 
> <span data-ttu-id="8b970-173">メッセージの受信確認が成功するまで、同じメッセージが 30 分ごとにキューから削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="8b970-173">Until a message is successfully acknowledged, the same message will become available to dequeue every 30 minutes.</span></span> <span data-ttu-id="8b970-174">メッセージが複数回キューから削除されている場合、デキューの応答は、最後にデキューされた日時を送信します。</span><span class="sxs-lookup"><span data-stu-id="8b970-174">In cases when a message is being dequeued more than one time, the dequeue response will send the last dequeued date time.</span></span> <span data-ttu-id="8b970-175">これはメッセージの最初のデキューに対して、空白になります。</span><span class="sxs-lookup"><span data-stu-id="8b970-175">This will be blank for the first dequeue of a message.</span></span> <span data-ttu-id="8b970-176">メッセージの受信確認をして、同じメッセージを繰り返しダウンロードされないようにすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="8b970-176">It is important to ensure that a message is successfully acknowledged to prevent a repeated download of the same message.</span></span> <span data-ttu-id="8b970-177">確認に失敗した場合に、失敗を確認できるよう再試行ロジックを導入することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b970-177">When an acknowledgement fails, having re-try logic to acknowledge the failure is recommended.</span></span>

### <a name="api-for-getting-message-status"></a><span data-ttu-id="8b970-178">メッセージ状態を取得中の API</span><span class="sxs-lookup"><span data-stu-id="8b970-178">API for getting message status</span></span>
<span data-ttu-id="8b970-179">メッセージのステータスを取得する API は、Platform update 12 の修正プログラム KB4058074 として入手できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-179">The API to get the status of a message is available as of hotfix KB 4058074 for Platform update 12.</span></span> <span data-ttu-id="8b970-180">この API は、インポートシナリオでメッセージが正常に処理されたかどうかを判断する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="8b970-180">This API is particularly useful in import scenarios to determine if a message has been successfully processed.</span></span> <span data-ttu-id="8b970-181">エンキュープロセスの完了時に、メッセージが作成されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-181">A message is created when the enqueue process is completed.</span></span> <span data-ttu-id="8b970-182">メッセージから障害状況が返される場合、統合アプリを設定し再実行するか、別のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-182">If the message returns a failed status, you can set your integration app to retry or take another action.</span></span>

<span data-ttu-id="8b970-183">**例**</span><span class="sxs-lookup"><span data-stu-id="8b970-183">**Example**</span></span>

```Console
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetMessageStatus
BODY
{
    "messageId":"<string>"
}
```

<span data-ttu-id="8b970-184">次のテーブルに、使用可能なステータス値を示します。</span><span class="sxs-lookup"><span data-stu-id="8b970-184">The following table lists the possible status values.</span></span>

| <span data-ttu-id="8b970-185">先頭値</span><span class="sxs-lookup"><span data-stu-id="8b970-185">Value</span></span>                | <span data-ttu-id="8b970-186">意味</span><span class="sxs-lookup"><span data-stu-id="8b970-186">Meaning</span></span>                                                                              |
|----------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8b970-187">エンキュー化</span><span class="sxs-lookup"><span data-stu-id="8b970-187">Enqueued</span></span>             | <span data-ttu-id="8b970-188">ファイルは blob ストレージのキューに正常に追加されました</span><span class="sxs-lookup"><span data-stu-id="8b970-188">The file has been successfully enqueued to blob storage</span></span>                              |
| <span data-ttu-id="8b970-189">キューから削除</span><span class="sxs-lookup"><span data-stu-id="8b970-189">Dequeued</span></span>             | <span data-ttu-id="8b970-190">ファイルは blob ストレージのキューから正常に削除されました</span><span class="sxs-lookup"><span data-stu-id="8b970-190">The file has been successfully dequeued from blob storage</span></span>                            |
| <span data-ttu-id="8b970-191">Acked</span><span class="sxs-lookup"><span data-stu-id="8b970-191">Acked</span></span>                | <span data-ttu-id="8b970-192">エクスポートされたファイルは、外部アプリケーションによってダウンロードされることが確認されています</span><span class="sxs-lookup"><span data-stu-id="8b970-192">The exported file has been acknowledged to be downloaded by the external application</span></span> |
| <span data-ttu-id="8b970-193">前処理中</span><span class="sxs-lookup"><span data-stu-id="8b970-193">Preprocessing</span></span>        | <span data-ttu-id="8b970-194">インポート/エクスポート操作は要求を前処理しています</span><span class="sxs-lookup"><span data-stu-id="8b970-194">The import/export operation is pre-processing the request</span></span>                            |
| <span data-ttu-id="8b970-195">処理中</span><span class="sxs-lookup"><span data-stu-id="8b970-195">Processing</span></span>           | <span data-ttu-id="8b970-196">インポート/エクスポート操作が処理中です</span><span class="sxs-lookup"><span data-stu-id="8b970-196">The import/export operation is in process</span></span>                                            |
| <span data-ttu-id="8b970-197">処理済</span><span class="sxs-lookup"><span data-stu-id="8b970-197">Processed</span></span>            | <span data-ttu-id="8b970-198">インポート/エクスポート操作は正常に完了しました</span><span class="sxs-lookup"><span data-stu-id="8b970-198">The import/export operation completed successfully</span></span>                                   |
| <span data-ttu-id="8b970-199">PreProcessingError</span><span class="sxs-lookup"><span data-stu-id="8b970-199">PreProcessingError</span></span>   | <span data-ttu-id="8b970-200">インポート/エクスポート操作はポスト前処理ステージで失敗しました</span><span class="sxs-lookup"><span data-stu-id="8b970-200">The import/export operation failed in the pre-processing stage</span></span>                       |
| <span data-ttu-id="8b970-201">ProcessedWithErrors</span><span class="sxs-lookup"><span data-stu-id="8b970-201">ProcessedWithErrors</span></span>  | <span data-ttu-id="8b970-202">インポート/エクスポート操作は完了しましたが、エラーが発生しました</span><span class="sxs-lookup"><span data-stu-id="8b970-202">The import/export operation completed with errors</span></span>                                    |
| <span data-ttu-id="8b970-203">PostProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="8b970-203">PostProcessingFailed</span></span> | <span data-ttu-id="8b970-204">インポート/エクスポート操作はポスト処理中に失敗しました</span><span class="sxs-lookup"><span data-stu-id="8b970-204">the import/export operation failed during post-processing</span></span>                            |

> [!NOTE]
> <span data-ttu-id="8b970-205">BLOB ストレージ内のファイルは、ストレージに 7 日間残ります。その後、自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-205">The file in the blob storage will remain in the storage for seven days, after which it will be automatically deleted.</span></span>

### <a name="api-to-get-the-list-of-execution-errors"></a><span data-ttu-id="8b970-206">実行エラーの一覧を取得する API</span><span class="sxs-lookup"><span data-stu-id="8b970-206">API to get the list of execution errors</span></span>
<span data-ttu-id="8b970-207">GetExecutionErrors は、ジョブ実行のエラーのリストを取得するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-207">GetExecutionErrors can be used to get the list of errors in a job execution.</span></span> <span data-ttu-id="8b970-208">API は、Execution ID をパラメーターとして取り、JSON リストでエラー メッセージのセットを返します。</span><span class="sxs-lookup"><span data-stu-id="8b970-208">The API takes the Execution ID as the parameter, and returns a set of error messages in a JSON list.</span></span>

```Console
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionErrors
BODY
{"executionId":"<executionId>"}
```

## <a name="tips-and-tricks"></a><span data-ttu-id="8b970-209">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="8b970-209">Tips and tricks</span></span>
### <a name="viewing-the-batch-job-status-for-recurring-integrations-from-the-data-management-workspace"></a><span data-ttu-id="8b970-210">データ管理ワークスペースからの定期的な統合バッチ ジョブのステータスの表示</span><span class="sxs-lookup"><span data-stu-id="8b970-210">Viewing the batch job status for recurring integrations from the Data management workspace</span></span>
<span data-ttu-id="8b970-211">定期的な統合データ ジョブは、バッチ モードで実行されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-211">Recurring integration data jobs run in batch mode.</span></span> <span data-ttu-id="8b970-212">繰り返しジョブが失敗した場合は、トラブルシューティング プロセスの一環としてバッチ ジョブのインスタンスを調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8b970-212">If a recurring job fails, you must investigate the instance of the batch job as part of the troubleshooting process.</span></span> <span data-ttu-id="8b970-213">これを簡単に調べるには、**メッセージの管理** をクリックして **定期データ ジョブのプロセス状態** ページに進ます。そうすると、バッチ ジョブの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-213">To make this investigation easier, click **Manage messages** to get to the **Process status for recurring data job** page, which now shows the status of the batch job.</span></span>

<span data-ttu-id="8b970-214">バッチ ジョブの状態は、指定した繰り返しデータ ジョブのバッチ フレームワークから非同期で取得されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-214">The batch job status is retrieved asynchronously from the batch framework for the specified recurring data job.</span></span> <span data-ttu-id="8b970-215">最新のバッチ ジョブの状態を表示するには、**バッチの状態を表示する** を選択し、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="8b970-215">To see the most up-to-date batch job status, select **Get batch status**, and then refresh the page.</span></span>

> [!NOTE]
> <span data-ttu-id="8b970-216">バッチ履歴のレコードが削除された場合、**定期的なデータ ジョブの処理ステータス** ページにあるバッチ ジョブのステータスは空白になります。</span><span class="sxs-lookup"><span data-stu-id="8b970-216">If the record for the batch history is deleted, the status for the batch job on the **Processing status for recurring data job** page will be blank.</span></span>

![バッチ ジョブ ステータス](./media/show-batch-status.png)

### <a name="preventing-uploads-when-there-are-no-records"></a><span data-ttu-id="8b970-218">レコードがない場合は、アップロードを禁止する</span><span class="sxs-lookup"><span data-stu-id="8b970-218">Preventing uploads when there are no records</span></span>
<span data-ttu-id="8b970-219">定期的なエクスポートを使用するとき、そのファイルまたはパッケージ内の合計のレコード数が 0 (ゼロ) である場合、生成されるファイルまたはパッケージをアップロードしないように選択できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-219">When you use recurring exports you can choose not to upload a generated file or package if the total record count in that file or package is 0 (zero).</span></span>

<span data-ttu-id="8b970-220">**レコード数が 0 の場合にアップロードしない** オプションは、定期的なエクスポート ジョブを構成するとき、またはジョブが作成済みのいずれかの場合に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-220">You can set the **Prevent upload when zero records** option either when you configure a recurring export job or after a job has been created.</span></span> <span data-ttu-id="8b970-221">このオプションは、データ ソースとしてファイルまたはパッケージを使用する場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-221">This option is available only when you use files or packages as data sources.</span></span>

![レコード数が 0 の場合にアップロードしない](./media/prevent-file-upload.png)

<span data-ttu-id="8b970-223">実装に、ファイルまたはパッケージをアップロードした、定期的なジョブの実行が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8b970-223">Your implementation might include runs of recurring jobs where files or packages were uploaded.</span></span> <span data-ttu-id="8b970-224">ご使用の実装には、アップロードするものがないため、ファイルまたはパッケージがアップロードされなかった実行が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="8b970-224">Your implementation might also include runs where no files or packages were uploaded, because there was nothing to upload.</span></span> <span data-ttu-id="8b970-225">アップロードする必要のあるファイルがアップロードされていない、またはアップロードする必要がないファイルがアップロードされていた場合は、定期的なエクスポート ジョブに対して **メッセージの管理** ページを使用して、デバッグ プロセスを支援することができます。</span><span class="sxs-lookup"><span data-stu-id="8b970-225">If you suspect that a file that should have been uploaded wasn't uploaded, or that a file that should not have been uploaded was uploaded, you can use the **Manage messages** page for the recurring export job to help with the debugging process.</span></span>

> [!NOTE]
> <span data-ttu-id="8b970-226">これらの機能が、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition プラットフォーム更新プログラム 12 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="8b970-226">These features were added in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition platform update 12.</span></span> <span data-ttu-id="8b970-227">プラットフォーム更新 12 にアップグレードする前に実行されたジョブは、次の列に値を持ちません。</span><span class="sxs-lookup"><span data-stu-id="8b970-227">Jobs that were run before you upgraded to Platform update 12 won't have values in the following columns.</span></span>

<span data-ttu-id="8b970-228">**エクスポートされたレコードの合計** 列には、エクスポートされたレコードの合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="8b970-228">The **Total records exported** column shows the total count of records that were exported.</span></span> <span data-ttu-id="8b970-229">**0** (ゼロ) の値は、ファイルにエクスポートされたまたはパッケージに含まれていたレコードがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="8b970-229">A value of **0** (zero) indicates that no records were exported to the file or included in the package.</span></span>

<span data-ttu-id="8b970-230">**ファイルが正常にアップロードされました** 列には、ファイルまたはパッケージが正常にアップロードされた場合にチェック マークが含まれます。</span><span class="sxs-lookup"><span data-stu-id="8b970-230">The **File uploaded successfully** column contains a check mark if the file or the package was uploaded successfully.</span></span> <span data-ttu-id="8b970-231">エラーが発生したまたはレコードがないことが原因でファイルがアップロードされなかった場合、列は空白になります。</span><span class="sxs-lookup"><span data-stu-id="8b970-231">If the file wasn't uploaded because of an error, or because there were no records, the column will be blank.</span></span>

### <a name="http-vs-https"></a><span data-ttu-id="8b970-232">Http 対 Https</span><span class="sxs-lookup"><span data-stu-id="8b970-232">Http vs Https</span></span>
<span data-ttu-id="8b970-233">デキュー API は、HTTPS ではなく HTTP を返します。</span><span class="sxs-lookup"><span data-stu-id="8b970-233">The dequeue API returns HTTP instead of HTTPS.</span></span> <span data-ttu-id="8b970-234">この動作は、運用環境などのロード バランサーを使用するアプリケーション環境で確認できます。</span><span class="sxs-lookup"><span data-stu-id="8b970-234">This behavior can be seen in application environments that use a load balancer, such as production environments.</span></span> <span data-ttu-id="8b970-235">(1 つのボックス環境で動作を表示ことはできません)。</span><span class="sxs-lookup"><span data-stu-id="8b970-235">(You cannot see the behavior in one box environments).</span></span> <span data-ttu-id="8b970-236">アプリケーションからキューから削除しようとするミドルウェア アプリケーションで、URI スキームを HTTPS に変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8b970-236">We recommend that you change the URI scheme to HTTPS in the middleware application that is trying to dequeue from the application.</span></span>

![バッチ ジョブの状態](./media/show-batch-status.png)
