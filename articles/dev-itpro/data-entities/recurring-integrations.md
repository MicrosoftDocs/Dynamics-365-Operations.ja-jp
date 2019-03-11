---
title: 定期統合
description: このトピックでは、定期的な統合について説明します。 データ移行のプロセスや、エンタープライズ システムの内外への移動は、どのプラットフォームでもサポートする必要がある重要な要素です。
author: Sunil-Garg
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 24821
ms.assetid: 70a4f748-b0bd-44b1-a118-56aacb91481c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a5c8e4844b575732bf5be7753ef0535fe0822b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368476"
---
# <a name="recurring-integrations"></a><span data-ttu-id="ac8cb-104">定期統合</span><span class="sxs-lookup"><span data-stu-id="ac8cb-104">Recurring integrations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ac8cb-105">データ移行のプロセスや、エンタープライズ システムの内外への移動は、どのプラットフォームでもサポートする必要がある重要な要素です。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-105">The process of data migration, and movement into and out of any enterprise system, are critical pieces that any platform must support.</span></span> <span data-ttu-id="ac8cb-106">多くの労力と計画によって、Microsoft Dynamics 365 for Finance and Operations など企業の業種 (LOB) システムとさまざまなソース システムでのサード パーティ統合が構築されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-106">Lots of effort and planning go into building third-party integrations between an enterprise line of business (LOB) system, such as Microsoft Dynamics 365 for Finance and Operations, and various source systems.</span></span> <span data-ttu-id="ac8cb-107">Microsoft Dynamics AX 2012 では、アプリケーション統合フレームワーク (AIF) を通じてこのようなシナリオを可能にします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-107">Microsoft Dynamics AX 2012 enables these scenarios through Application Integration Framework (AIF).</span></span> <span data-ttu-id="ac8cb-108">Finance and Operations では、統合ソリューション ビルダーから顧客ユーザーに含まれるすべての関係者に対して、このプロセスの簡略化に努めました。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-108">For Finance and Operations, we have tried to simplify this process for all parties who are involved, from integration solution builders to customer users.</span></span>

## <a name="architecture"></a><span data-ttu-id="ac8cb-109">アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="ac8cb-109">Architecture</span></span>
<span data-ttu-id="ac8cb-110">統合では、次の操作が行われます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-110">Integration does the following things:</span></span>

- <span data-ttu-id="ac8cb-111">これは、データ エンティティとデータ管理フレームワークで構築されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-111">It builds on data entities and the Data management framework.</span></span>
- <span data-ttu-id="ac8cb-112">Finance and Operations とあらゆるサード パーティ製アプリケーションやサービスで、ドキュメントまたはファイルの交換を可能にします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-112">It enables the exchange of documents or files between Finance and Operations and any third-party application or service.</span></span>
- <span data-ttu-id="ac8cb-113">複数のドキュメント形式、ソース マッピング、XSLT (Extensible Stylesheet Language Transformations)、およびフィルターをサポートします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-113">It supports several document formats, source mapping, Extensible Stylesheet Language Transformations (XSLT), and filters.</span></span>

    ![複数の文書形式のドキュメントまたはファイルを交換](./media/recurring-integrations.png)

- <span data-ttu-id="ac8cb-115">セキュリティで保護された REST のアプリケーション プログラミング インターフェイス (API) と認証メカニズムを使用して、統合システムからデータを受信し、データを送り返します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-115">It uses secure REST application programming interfaces (APIs) and authorization mechanisms to receive data from, and send data back to, integration systems.</span></span>

    ![繰り返し実行される統合を設定](./media/set-up-recurring.png)

## <a name="authorization-for-the-integration-rest-api"></a><span data-ttu-id="ac8cb-117">統合 REST API の承認</span><span class="sxs-lookup"><span data-stu-id="ac8cb-117">Authorization for the integration REST API</span></span>
<span data-ttu-id="ac8cb-118">統合 REST API は、他のサービス エンドポイントと同じ OAuth 2.0 認証モデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-118">The integration REST API uses the same OAuth 2.0 authentication model as the other service endpoints.</span></span> <span data-ttu-id="ac8cb-119">統合クライアント アプリケーションがこのエンドポイントを使用する前に、Microsoft Azure Active Directory (Azure AD) にアプリケーション ID を作成し、Finance and Operations に適切なアクセス許可を付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-119">Before the integrating client application can consume this endpoint, you must create an application ID in Microsoft Azure Active Directory (Azure AD) and give it appropriate permission to Finance and Operations.</span></span> <span data-ttu-id="ac8cb-120">定期的なジョブを作成して有効にするとき、その定期的なジョブとやり取りする Azure AD アプリケーション ID を入力するように求められます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-120">When you create and enable a recurring job, you're prompted to enter the Azure AD application ID that will interact with that recurring job.</span></span> <span data-ttu-id="ac8cb-121">したがって、アプリケーション ID をメモしておいてください。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-121">Therefore, be sure to make a note of the application ID.</span></span>

## <a name="set-up-a-data-project-and-recurring-data-jobs"></a><span data-ttu-id="ac8cb-122">データ プロジェクトと定期的なデータ ジョブを設定</span><span class="sxs-lookup"><span data-stu-id="ac8cb-122">Set up a data project and recurring data jobs</span></span>
### <a name="create-a-data-project"></a><span data-ttu-id="ac8cb-123">データ プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="ac8cb-123">Create a data project</span></span>

1. <span data-ttu-id="ac8cb-124">主要なダッシュ ボードで、**データ管理**タイルを選択し**データ管理**ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-124">On the main dashboard, select the **Data management** tile to open the **Data management** workspace.</span></span>
2. <span data-ttu-id="ac8cb-125">**インポートまたはエクスポート** タイルを選択し、新しいデータ プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-125">Select the **Import or Export** tile to create a new data project.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac8cb-126">既存のデータ プロジェクトを使用する場合は、**データ プロジェクト** タブにあるデータ プロジェクトのカードで**プロジェクトを読み込む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-126">If you have an existing data project, select **Load project** on the card for any data project on the **Data projects** tab.</span></span>

3. <span data-ttu-id="ac8cb-127">有効なジョブ名、データ ソース、およびエンティティ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-127">Enter a valid job name, data source, and entity name.</span></span>
4. <span data-ttu-id="ac8cb-128">1 つ以上のエンティティのデータ ファイルをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-128">Upload a data file for one or more entities.</span></span> <span data-ttu-id="ac8cb-129">各エンティティが追加されており、エラーが発生していないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-129">Make sure that each entity is added, and that no errors occur.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac8cb-130">フィールド マップを設定、レビュー、または修正し、受信データに適用する必要がある XSLT ベースの変換を設定するため、各エンティティ データ カードを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-130">You can select each entity data card to set up, review, or modify field maps, and to set up XSLT-based transforms that must be applied to inbound data.</span></span> <span data-ttu-id="ac8cb-131">データ プロジェクトのエクスポートについては、エンティティ カードはフィルター リンクも表示し、フィルター データにフィルターを設定できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-131">For export data projects, the entity card also shows a filter link, so that you can set up filters to filter data.</span></span> <span data-ttu-id="ac8cb-132">現在、データ プロジェクトのすべての定期的なデータ ジョブは、同じフィルターを使用します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-132">Currently, all recurring data jobs in a data project use the same filter.</span></span>

5. <span data-ttu-id="ac8cb-133">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-133">Select **Save**.</span></span>

### <a name="create-a-recurring-data-job"></a><span data-ttu-id="ac8cb-134">定期的なデータ ジョブの作成</span><span class="sxs-lookup"><span data-stu-id="ac8cb-134">Create a recurring data job</span></span>

1. <span data-ttu-id="ac8cb-135">**データ プロジェクト**ページで、**定期的なデータ ジョブの作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-135">On the **Data project** page, select **Create recurring data job**.</span></span>
2. <span data-ttu-id="ac8cb-136">定期的なデータ ジョブの有効な名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-136">Enter a valid name and a description for the recurring data job.</span></span>
3. <span data-ttu-id="ac8cb-137">**承認ポリシーの設定**タブに、アプリケーションが生成されているアプリケーション ID を入力し、それを有効になっているとしてマークします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-137">On the **Set up authorization policy** tab, enter the application ID that was generated for your application, and mark it as enabled.</span></span>
4. <span data-ttu-id="ac8cb-138">**詳細オプション**タブを展開し、**ファイル**または**データ パッケージ**のどちらかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-138">Expand **Advanced options** tab, and specify either **File** or **Data package**.</span></span>

    - <span data-ttu-id="ac8cb-139">**ファイル** – 外部統合によって個々のファイルがプッシュされ、この定期的なデータジョブによって処理されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-139">**File** – Your external integration will push individual files so that they can be processed via this recurring data job.</span></span> <span data-ttu-id="ac8cb-140">この場合、予想されるファイルの形式は、エンティティがデータ プロジェクトに追加されたときに指定された形式と同じです。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-140">In this case, the format of the file that is expected is the same as the format that was specified when the entity was added to the data project.</span></span>
    - <span data-ttu-id="ac8cb-141">**データ パッケージ** - 処理のためのデータ パッケージ ファイルのみをプッシュできます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-141">**Data package** – You can push only data package files for processing.</span></span> <span data-ttu-id="ac8cb-142">データ パッケージは、統合ジョブで使用できる 1 つの単位として複数のデータ ファイルを送信できる新しい形式です。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-142">A data package is a new format that lets you submit multiple data files as a single unit that can be used in integration jobs.</span></span>
    - <span data-ttu-id="ac8cb-143">**順に処理されるメッセージ** – このオプションを有効にすると、インポート シナリオで受信ファイルを強制的に処理することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-143">**Process messages in order** – You can enable this option to force sequential processing of incoming files in an import scenario.</span></span> <span data-ttu-id="ac8cb-144">このオプションはファイルにのみ適用され、データ パッケージには適用されません。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-144">This option is only applicable to files and not data packages.</span></span>

5. <span data-ttu-id="ac8cb-145">**処理の繰り返しを設定** を選択し、**定期的なアイテムの定義** ダイアログ ボックスで、データ ジョブの有効な繰り返しを設定します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-145">Select **Set processing recurrence**, and then, in the **Define recurrence** dialog box, set up a valid recurrence for your data job.</span></span>
6. <span data-ttu-id="ac8cb-146">オプション: **定期的なアイテムの監視を設定** を選択し、定期的なアイテムの監視を設定します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-146">Optional: Select **Set monitoring recurrence**, and set up a monitoring recurrence.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac8cb-147">現在のところ、監視の繰り返しは、定期的なデータ ジョブのキューでのみ負荷監視を有効にします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-147">Currently, monitoring recurrence enables load monitoring only on the queue for your recurring data job.</span></span> <span data-ttu-id="ac8cb-148">このサービスを使用してサポートされる追加のポリシーはありません。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-148">No additional policies are supported via this service.</span></span> <span data-ttu-id="ac8cb-149">この機能を使用すると、積荷需要が必要な場合に処理の繰り返しを微調整することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-149">You can use this feature to fine-tune the processing recurrence as the load demand requires.</span></span>

7. <span data-ttu-id="ac8cb-150">**OK** を選択し、確認メッセージ ボックスで **はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-150">Select **OK**, and then select **Yes** in the confirmation message box.</span></span>

## <a name="manage-recurring-data-jobs"></a><span data-ttu-id="ac8cb-151">定期的なデータ ジョブの管理</span><span class="sxs-lookup"><span data-stu-id="ac8cb-151">Manage recurring data jobs</span></span>
1. <span data-ttu-id="ac8cb-152">**システム管理**ワークスペース (**システム管理**モジュールではない) で、**データ管理 IT** ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-152">In the **System administration** workspace (not the **System administration** module), select the **Data Management IT** workspace.</span></span>
2. <span data-ttu-id="ac8cb-153">ワークスペースの**定期的なデータ ジョブ** タブで、定期的なジョブを選択して詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-153">In the workspace, on the **Recurring data job** tab, select the recurring job to view the details.</span></span> <span data-ttu-id="ac8cb-154">**スケジュールされたデータ ジョブを管理** ページには、キューに待機しているすべてのメッセージを一覧表示するグリッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-154">The **Manage scheduled data jobs** page contains a grid that lists any messages that are waiting in the queue.</span></span> <span data-ttu-id="ac8cb-155">したがって、メッセージと処理ステータスを監視できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-155">Therefore, you can monitor messages and the processing status.</span></span>

    ![スケジュール済みデータ ジョブの管理](./media/image013.jpg)

## <a name="submitting-data-to-recurring-data-jobs"></a><span data-ttu-id="ac8cb-157">定期的なデータ ジョブにデータを送信</span><span class="sxs-lookup"><span data-stu-id="ac8cb-157">Submitting data to recurring data jobs</span></span>
<span data-ttu-id="ac8cb-158">統合 REST エンドポイントを使用して、クライアントと統合、ドキュメントの送信 (インポート)、またはダウンロードに使用可能なドキュメントのポーリング (エクスポート) を実行することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-158">You can use integration REST endpoints to integrate with the client, submit documents (import), or poll available documents for download (export).</span></span> <span data-ttu-id="ac8cb-159">これらのエンドポイントは OAuth をサポートします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-159">These endpoints support OAuth.</span></span>

## <a name="integration-rest-apis"></a><span data-ttu-id="ac8cb-160">REST API 統合</span><span class="sxs-lookup"><span data-stu-id="ac8cb-160">Integration REST APIs</span></span>
<span data-ttu-id="ac8cb-161">次の API セットは、統合クライアントと Finance and Operations の間でデータを交換するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-161">The following set of APIs is used to exchange data between the integration client and Finance and Operations.</span></span>

### <a name="api-for-import-enqueue"></a><span data-ttu-id="ac8cb-162">インポート (エンキュー) の API</span><span class="sxs-lookup"><span data-stu-id="ac8cb-162">API for import (enqueue)</span></span>
<span data-ttu-id="ac8cb-163">次の URL に対して HTTP POST 呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-163">Make an HTTP POST call against the following URL.</span></span>

```
https://<base URL>/api/connector/enqueue/<activity ID>?entity=<entity name>
```

<span data-ttu-id="ac8cb-164">メッセージ本文では、データをメモリ ストリームとして渡せます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-164">In the message body, you can the pass the data as a memory stream.</span></span>

<span data-ttu-id="ac8cb-165">**例**</span><span class="sxs-lookup"><span data-stu-id="ac8cb-165">**Example**</span></span>

```
POST https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/enqueue/%7B6D31E09F-0249-459F-94F0-AAD9C2C47B64%7D?entity=Customer%20Groups
```

<span data-ttu-id="ac8cb-166">アクティビティ ID を取得するには、**スケジュールされたデータ ジョブの管理** ページの **ID** フィールドで、グローバルで一意の識別子 (GUID) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-166">To get the activity ID, on the **Manage scheduled data jobs** page, in the **ID** field, copy the globally unique identifier (GUID).</span></span>

![スケジュール済みデータ ジョブ ページの管理での GUID](./media/image015.jpg)

### <a name="api-for-export-dequeue"></a><span data-ttu-id="ac8cb-168">エクスポート (デキュー) のAPI</span><span class="sxs-lookup"><span data-stu-id="ac8cb-168">API for export (dequeue)</span></span>
<span data-ttu-id="ac8cb-169">データ プロジェクトで定義されたすべてのデータ エンティティを含むデータ パッケージを返し、クライアント アプリケーションで解凍して使用できるようにするには、次の構造を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-169">To return a data package that contains all the data entities that were defined in the data project, and that the client application can unzip and consume, use the following structure.</span></span>

```
https://<base URL>/api/connector/dequeue/<activity ID>
```

<span data-ttu-id="ac8cb-170">**例**</span><span class="sxs-lookup"><span data-stu-id="ac8cb-170">**Example**</span></span>

```
GET https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/dequeue/%7BC03BB937-09ED-46DE-86EE-4520D7D7E373%7D
```

<span data-ttu-id="ac8cb-171">クライアントがデータをダウンロードした後、データを受領したものとしてマークすることができるように、受信確認は Finance and Operations に送り返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-171">After the client downloads the data, an acknowledgment must be sent back to Finance and Operations, so that you can mark the data as received.</span></span>

<span data-ttu-id="ac8cb-172">blob にアップロードされたファイルがない場合、デキュー API はそのことを示す応答を返します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-172">In cases when there was no file uploaded to the blob, the dequeue API will return a response indicating as such.</span></span>

### <a name="api-for-acknowledgment"></a><span data-ttu-id="ac8cb-173">確認の API</span><span class="sxs-lookup"><span data-stu-id="ac8cb-173">API for acknowledgment</span></span>
<span data-ttu-id="ac8cb-174">次 の API を使用します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-174">Use the following API.</span></span>

> [!NOTE]
> <span data-ttu-id="ac8cb-175">**/enqueue** の応答の本文は、**/ack** 転記要求の本文で送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-175">The body of the response of **/enqueue** must be sent in the body of the **/ack** POST request.</span></span>

```
https://<base URL>/api/connector/ack/<activity ID>
```

<span data-ttu-id="ac8cb-176">**例**</span><span class="sxs-lookup"><span data-stu-id="ac8cb-176">**Example**</span></span>

```
POST https://usncax1aos.cloud.onebox.dynamics.com/en/api/connector/ack/%7BC03BB937-09ED-46DE-86EE-4520D7D7E373%7D
```

### <a name="api-for-getting-message-status"></a><span data-ttu-id="ac8cb-177">メッセージ状態を取得中の API</span><span class="sxs-lookup"><span data-stu-id="ac8cb-177">API for getting message status</span></span>
<span data-ttu-id="ac8cb-178">メッセージのステータスを取得する API は、Platform update 12 の修正プログラム KB4058074 として入手できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-178">The API to get the status of a message is available as of hotfix KB 4058074 for Platform update 12.</span></span> <span data-ttu-id="ac8cb-179">この API は、インポートシナリオでメッセージが正常に処理されたかどうかを判断する場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-179">This API is particularly useful in import scenarios to determine if a message has been successfully processed.</span></span> <span data-ttu-id="ac8cb-180">エンキュープロセスの完了時に、メッセージが作成されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-180">A message is created when the enqueue process is completed.</span></span> <span data-ttu-id="ac8cb-181">メッセージから障害状況が返される場合、統合アプリを設定し再実行するか、別のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-181">If the message returns a failed status, you can set your integration app to retry or take another action.</span></span>

<span data-ttu-id="ac8cb-182">**例**</span><span class="sxs-lookup"><span data-stu-id="ac8cb-182">**Example**</span></span>

```
POST /data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetMessageStatus
BODY
{
    "messageId":"<string>"
}
```

<span data-ttu-id="ac8cb-183">次のテーブルに、使用可能なステータス値を示します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-183">The following table lists the possible status values.</span></span>

| <span data-ttu-id="ac8cb-184">先頭値</span><span class="sxs-lookup"><span data-stu-id="ac8cb-184">Value</span></span>                | <span data-ttu-id="ac8cb-185">意味</span><span class="sxs-lookup"><span data-stu-id="ac8cb-185">Meaning</span></span>                                                                              |
|----------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ac8cb-186">エンキュー化</span><span class="sxs-lookup"><span data-stu-id="ac8cb-186">Enqueued</span></span>             | <span data-ttu-id="ac8cb-187">ファイルは blob ストレージのキューに正常に追加されました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-187">The file has been successfully enqueued to blob storage</span></span>                              |
| <span data-ttu-id="ac8cb-188">キューから削除</span><span class="sxs-lookup"><span data-stu-id="ac8cb-188">Dequeued</span></span>             | <span data-ttu-id="ac8cb-189">ファイルは blob ストレージのキューから正常に削除されました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-189">The file has been successfully dequeued from blob storage</span></span>                            |
| <span data-ttu-id="ac8cb-190">Acked</span><span class="sxs-lookup"><span data-stu-id="ac8cb-190">Acked</span></span>                | <span data-ttu-id="ac8cb-191">エクスポートされたファイルは、外部アプリケーションによってダウンロードされることが確認されています</span><span class="sxs-lookup"><span data-stu-id="ac8cb-191">The exported file has been acknowledged to be downloaded by the external application</span></span> |
| <span data-ttu-id="ac8cb-192">前処理中</span><span class="sxs-lookup"><span data-stu-id="ac8cb-192">Preprocessing</span></span>        | <span data-ttu-id="ac8cb-193">インポート/エクスポート操作は要求を前処理しています</span><span class="sxs-lookup"><span data-stu-id="ac8cb-193">The import/export operation is pre-processing the request</span></span>                            |
| <span data-ttu-id="ac8cb-194">処理中</span><span class="sxs-lookup"><span data-stu-id="ac8cb-194">Processing</span></span>           | <span data-ttu-id="ac8cb-195">インポート/エクスポート操作が処理中です</span><span class="sxs-lookup"><span data-stu-id="ac8cb-195">The import/export operation is in process</span></span>                                            |
| <span data-ttu-id="ac8cb-196">処理済</span><span class="sxs-lookup"><span data-stu-id="ac8cb-196">Processed</span></span>            | <span data-ttu-id="ac8cb-197">インポート/エクスポート操作は正常に完了しました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-197">The import/export operation completed successfully</span></span>                                   |
| <span data-ttu-id="ac8cb-198">PreProcessingError</span><span class="sxs-lookup"><span data-stu-id="ac8cb-198">PreProcessingError</span></span>   | <span data-ttu-id="ac8cb-199">インポート/エクスポート操作はポスト前処理ステージで失敗しました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-199">The import/export operation failed in the pre-processing stage</span></span>                       |
| <span data-ttu-id="ac8cb-200">ProcessedWithErrors</span><span class="sxs-lookup"><span data-stu-id="ac8cb-200">ProcessedWithErrors</span></span>  | <span data-ttu-id="ac8cb-201">インポート/エクスポート操作は完了しましたが、エラーが発生しました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-201">The import/export operation completed with errors</span></span>                                    |
| <span data-ttu-id="ac8cb-202">PostProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="ac8cb-202">PostProcessingFailed</span></span> | <span data-ttu-id="ac8cb-203">インポート/エクスポート操作はポスト処理中に失敗しました</span><span class="sxs-lookup"><span data-stu-id="ac8cb-203">the import/export operation failed during post-processing</span></span>                            |

> [!NOTE]
> <span data-ttu-id="ac8cb-204">BLOB ストレージ内のファイルは、ストレージに 7 日間残ります。その後、自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-204">The file in the blob storage will remain in the storage for seven days, after which it will be automatically deleted.</span></span>

## <a name="tips-and-tricks"></a><span data-ttu-id="ac8cb-205">ヒントや秘訣</span><span class="sxs-lookup"><span data-stu-id="ac8cb-205">Tips and tricks</span></span>
### <a name="viewing-the-batch-job-status-for-recurring-integrations-from-the-data-management-workspace"></a><span data-ttu-id="ac8cb-206">データ管理ワークスペースからの定期的な統合バッチ ジョブのステータスの表示</span><span class="sxs-lookup"><span data-stu-id="ac8cb-206">Viewing the batch job status for recurring integrations from the Data management workspace</span></span>
<span data-ttu-id="ac8cb-207">定期的な統合データ ジョブは、バッチ モードで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-207">Recurring integration data jobs run in batch mode.</span></span> <span data-ttu-id="ac8cb-208">繰り返しジョブが失敗した場合は、トラブルシューティング プロセスの一環としてバッチ ジョブのインスタンスを調査する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-208">If a recurring job fails, you must investigate the instance of the batch job as part of the troubleshooting process.</span></span> <span data-ttu-id="ac8cb-209">これを簡単に調べるには、**メッセージの管理** をクリックして **定期データ ジョブのプロセス状態** ページに進ます。そうすると、バッチ ジョブの状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-209">To make this investigation easier, click **Manage messages** to get to the **Process status for recurring data job** page, which now shows the status of the batch job.</span></span>

<span data-ttu-id="ac8cb-210">バッチ ジョブの状態は、指定した繰り返しデータ ジョブのバッチ フレームワークから非同期で取得されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-210">The batch job status is retrieved asynchronously from the batch framework for the specified recurring data job.</span></span> <span data-ttu-id="ac8cb-211">最新のバッチ ジョブの状態を表示するには、**バッチの状態を表示する** を選択し、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-211">To see the most up-to-date batch job status, select **Get batch status**, and then refresh the page.</span></span>

> [!NOTE]
> <span data-ttu-id="ac8cb-212">バッチ履歴のレコードが削除された場合、**定期的なデータ ジョブの処理ステータス** ページにあるバッチ ジョブのステータスは空白になります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-212">If the record for the batch history is deleted, the status for the batch job on the **Processing status for recurring data job** page will be blank.</span></span>

![バッチ ジョブ ステータス](./media/show-batch-status.png)

### <a name="preventing-uploads-when-there-are-no-records"></a><span data-ttu-id="ac8cb-214">レコードがない場合は、アップロードを禁止する</span><span class="sxs-lookup"><span data-stu-id="ac8cb-214">Preventing uploads when there are no records</span></span>
<span data-ttu-id="ac8cb-215">Finance and Operations で定期的なエクスポートを使用するとき、そのファイルまたはパッケージ内の合計のレコード数が 0 (ゼロ) である場合、生成されるファイルまたはパッケージをアップロードしないように選択できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-215">When you use recurring exports in Finance and Operations, you can choose not to upload a generated file or package if the total record count in that file or package is 0 (zero).</span></span>

<span data-ttu-id="ac8cb-216">**レコード数が 0 の場合にアップロードしない** オプションは、定期的なエクスポート ジョブを構成するとき、またはジョブが作成済みのいずれかの場合に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-216">You can set the **Prevent upload when zero records** option either when you configure a recurring export job or after a job has been created.</span></span> <span data-ttu-id="ac8cb-217">このオプションは、データ ソースとしてファイルまたはパッケージを使用する場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-217">This option is available only when you use files or packages as data sources.</span></span>

![レコード数が 0 の場合にアップロードしない](./media/prevent-file-upload.png)

<span data-ttu-id="ac8cb-219">実装に、ファイルまたはパッケージをアップロードした、定期的なジョブの実行が含まれている可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-219">Your implementation might include runs of recurring jobs where files or packages were uploaded.</span></span> <span data-ttu-id="ac8cb-220">ご使用の実装には、アップロードするものがないため、ファイルまたはパッケージがアップロードされなかった実行が含まれていることがあります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-220">Your implementation might also include runs where no files or packages were uploaded, because there was nothing to upload.</span></span> <span data-ttu-id="ac8cb-221">アップロードする必要のあるファイルがアップロードされていない、またはアップロードする必要がないファイルがアップロードされていた場合は、定期的なエクスポート ジョブに対して**メッセージの管理**ページを使用して、デバッグ プロセスを支援することができます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-221">If you suspect that a file that should have been uploaded wasn't uploaded, or that a file that should not have been uploaded was uploaded, you can use the **Manage messages** page for the recurring export job to help with the debugging process.</span></span>

> [!NOTE]
> <span data-ttu-id="ac8cb-222">これらの機能は、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition のプラットフォーム更新プログラム 12 に追加されました。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-222">These features were added in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition platform update 12.</span></span> <span data-ttu-id="ac8cb-223">プラットフォーム更新 12 にアップグレードする前に実行されたジョブは、次の列に値を持ちません。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-223">Jobs that were run before you upgraded to Platform update 12 won't have values in the following columns.</span></span>

<span data-ttu-id="ac8cb-224">**エクスポートされたレコードの合計** 列には、エクスポートされたレコードの合計数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-224">The **Total records exported** column shows the total count of records that were exported.</span></span> <span data-ttu-id="ac8cb-225">**0** (ゼロ) の値は、ファイルにエクスポートされたまたはパッケージに含まれていたレコードがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-225">A value of **0** (zero) indicates that no records were exported to the file or included in the package.</span></span>

<span data-ttu-id="ac8cb-226">**ファイルが正常にアップロードされました** 列には、ファイルまたはパッケージが正常にアップロードされた場合にチェック マークが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-226">The **File uploaded successfully** column contains a check mark if the file or the package was uploaded successfully.</span></span> <span data-ttu-id="ac8cb-227">エラーが発生したまたはレコードがないことが原因でファイルがアップロードされなかった場合、列は空白になります。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-227">If the file wasn't uploaded because of an error, or because there were no records, the column will be blank.</span></span>

### <a name="http-vs-https"></a><span data-ttu-id="ac8cb-228">Http 対 Https</span><span class="sxs-lookup"><span data-stu-id="ac8cb-228">Http vs Https</span></span>
<span data-ttu-id="ac8cb-229">デキュー API は、HTTPS ではなく HTTP を返します。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-229">The dequeue API returns HTTP instead of HTTPS.</span></span> <span data-ttu-id="ac8cb-230">この動作は、運用環境などのロード バランサーを使用する Finance and Operations 環境で確認できます。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-230">This behavior can be seen in Finance and Operations environments that use a load balancer, such as production environments.</span></span> <span data-ttu-id="ac8cb-231">(1 つのボックス環境で動作を表示ことはできません)。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-231">(You cannot see the behavior in one box environments).</span></span> <span data-ttu-id="ac8cb-232">Finance and Operations からキューから削除しようとするミドルウェア アプリケーションで、URI スキームを HTTPS に変更することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ac8cb-232">We recommend that you change the URI scheme to HTTPS in the middleware application that is trying to dequeue from Finance and Operations.</span></span>

![バッチ ジョブ ステータス](./media/show-batch-status.png)
