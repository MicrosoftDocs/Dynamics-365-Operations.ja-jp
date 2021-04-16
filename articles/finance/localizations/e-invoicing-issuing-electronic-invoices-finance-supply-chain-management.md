---
title: Finance および Supply Chain Management で電子請求書を発行する
description: このトピックでは、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management で電子請求を使用して電子請求書を発行する方法について説明します。
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 8d6ef59b64a96e13bdc2e5ddf299ef7ab98e105c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840079"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a><span data-ttu-id="64475-103">Finance および Supply Chain Management での電子請求書の発行</span><span class="sxs-lookup"><span data-stu-id="64475-103">Issue electronic invoices in Finance and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="64475-104">このトピックでは、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management で電子請求を使用して電子請求書を発行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64475-104">This topic explains how to issue electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management through Electronic invoicing.</span></span>


## <a name="feature-activation"></a><span data-ttu-id="64475-105">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="64475-105">Feature activation</span></span>

<span data-ttu-id="64475-106">電子請求で電子請求書を発行するには、Finance および Supply Chain Management の機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="64475-106">To issue electronic invoices through Electronic invoicing, you must activate the Feature in Finance and Supply Chain Management.</span></span>

<span data-ttu-id="64475-107">各機能は、国/地域の電子請求書発行の要件に準拠した特定の電子請求書発行機能に対応しています。</span><span class="sxs-lookup"><span data-stu-id="64475-107">Each feature corresponds to a specific electronic invoicing feature that complies with the electronic invoicing requirements for a country/region.</span></span>

<span data-ttu-id="64475-108">次の表に、電子請求に対応する機能の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="64475-108">The following table shows the list of features that Electronic invoicing may support.</span></span>

| <span data-ttu-id="64475-109">氏名</span><span class="sxs-lookup"><span data-stu-id="64475-109">Name</span></span>                                              | <span data-ttu-id="64475-110">国/地域</span><span class="sxs-lookup"><span data-stu-id="64475-110">Country/region</span></span> |
|---------------------------------------------------|----------------|
|<span data-ttu-id="64475-111">オーストラリアの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-111">Austrian electronic invoice</span></span>                        |<span data-ttu-id="64475-112">オーストリア</span><span class="sxs-lookup"><span data-stu-id="64475-112">Austria</span></span>         |
|<span data-ttu-id="64475-113">ベルギーの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-113">Belgian electronic invoice</span></span>                         |<span data-ttu-id="64475-114">ベルギー</span><span class="sxs-lookup"><span data-stu-id="64475-114">Belgium</span></span>         |
|<span data-ttu-id="64475-115">NF-e 連邦政府 - ブラジル電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-115">NF-e  Federal - Brazilian electronic invoice</span></span>       |<span data-ttu-id="64475-116">ブラジル</span><span class="sxs-lookup"><span data-stu-id="64475-116">Brazil</span></span>          |
|<span data-ttu-id="64475-117">NFS-e - ブラジルのサービス (市区町) 電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-117">NFS-e - Brazilian service (city) electronic invoice</span></span>|<span data-ttu-id="64475-118">ブラジル</span><span class="sxs-lookup"><span data-stu-id="64475-118">Brazil</span></span>          |
|<span data-ttu-id="64475-119">デンマークの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-119">Danish electronic invoice</span></span>                          |<span data-ttu-id="64475-120">デンマーク</span><span class="sxs-lookup"><span data-stu-id="64475-120">Denmark</span></span>         |
|<span data-ttu-id="64475-121">エジプトの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-121">Egyptian electronic invoice</span></span>                        |<span data-ttu-id="64475-122">エジプト</span><span class="sxs-lookup"><span data-stu-id="64475-122">Egypt</span></span>           |
|<span data-ttu-id="64475-123">エストニアの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-123">Estonian electronic invoice</span></span>                        |<span data-ttu-id="64475-124">エストニア</span><span class="sxs-lookup"><span data-stu-id="64475-124">Estonia</span></span>         |
|<span data-ttu-id="64475-125">フィンランドの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-125">Finnish electronic invoice</span></span>                         |<span data-ttu-id="64475-126">フィンランド</span><span class="sxs-lookup"><span data-stu-id="64475-126">Finland</span></span>         |
|<span data-ttu-id="64475-127">フランスの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-127">French electronic invoice</span></span>                          |<span data-ttu-id="64475-128">フランス</span><span class="sxs-lookup"><span data-stu-id="64475-128">France</span></span>          |
|<span data-ttu-id="64475-129">ドイツの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-129">German electronic invoice</span></span>                          |<span data-ttu-id="64475-130">ドイツ</span><span class="sxs-lookup"><span data-stu-id="64475-130">Germany</span></span>         |
|<span data-ttu-id="64475-131">PEPPOL - グローバル電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-131">PEPPOL - Global electronic invoice</span></span>                 |<span data-ttu-id="64475-132">グローバル</span><span class="sxs-lookup"><span data-stu-id="64475-132">Global</span></span>          |
|<span data-ttu-id="64475-133">イタリアの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-133">Italian electronic invoice</span></span>                         |<span data-ttu-id="64475-134">イタリア</span><span class="sxs-lookup"><span data-stu-id="64475-134">Italy</span></span>           |
|<span data-ttu-id="64475-135">CFDI - メキシコの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-135">CFDI - Mexican electronic invoice</span></span>                  |<span data-ttu-id="64475-136">メキシコ</span><span class="sxs-lookup"><span data-stu-id="64475-136">Mexico</span></span>          |
|<span data-ttu-id="64475-137">オランダの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-137">Dutch electronic invoice</span></span>                           |<span data-ttu-id="64475-138">オランダ</span><span class="sxs-lookup"><span data-stu-id="64475-138">Netherlands</span></span>     |
|<span data-ttu-id="64475-139">ノルウェーの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-139">Norwegian electronic invoice</span></span>                       |<span data-ttu-id="64475-140">ノルウェー</span><span class="sxs-lookup"><span data-stu-id="64475-140">Norway</span></span>          |
|<span data-ttu-id="64475-141">スペインの電子請求書</span><span class="sxs-lookup"><span data-stu-id="64475-141">Spanish electronic invoice</span></span>                         |<span data-ttu-id="64475-142">スペイン</span><span class="sxs-lookup"><span data-stu-id="64475-142">Spain</span></span>           |

<span data-ttu-id="64475-143">国/地域のローカライズのスコープに対応している従来の電子請求書発行機能がある場合、これらの機能のひとつを有効にすると、従来の機能がオフになり、電子請求を介して電子請求書を発行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="64475-143">When there is a legacy Electronic invoicing feature that is supported in a country/region's localizations scope, activating one of these features turns off the legacy feature and enables electronic invoices to be issued through Electronic invoicing.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64475-144">電子請求の統合機能が有効になると、新しい電子請求エクスペリエンスが既定で無効になります。</span><span class="sxs-lookup"><span data-stu-id="64475-144">After the Electronic invoicing integration feature is enabled, the new Electronic invoicing experience is turned off by default.</span></span> <span data-ttu-id="64475-145">この機能の概念を使用すると、国/地域固有の機能を使用して、法人に対する新しいエクスペリエンスを選択的に有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="64475-145">You can use the feature concept to selectively enable new experiences for legal entities using country/region-specific functionality.</span></span> <span data-ttu-id="64475-146">**グローバル** オプションは、表に具体的にリストされていない残りの国/地域の新しいエクスペリエンスを制御します。</span><span class="sxs-lookup"><span data-stu-id="64475-146">The **Global** option controls the new experience for the remaining county/regions that aren't specifically listed in the table.</span></span>

## <a name="submit-electronic-documents"></a><span data-ttu-id="64475-147">電子ドキュメントの送信</span><span class="sxs-lookup"><span data-stu-id="64475-147">Submit electronic documents</span></span>

<span data-ttu-id="64475-148">電子文書を提出するプロセスは、Finance および Supply Chain Management 管理と電子請求との間の単一のコミュニケーションポイントを表しています。</span><span class="sxs-lookup"><span data-stu-id="64475-148">The process of submitting electronic documents represents the single point of communication between Finance and Supply Chain Management and Electronic invoicing.</span></span> <span data-ttu-id="64475-149">各送信イベントで、両方向に通信が流れます。</span><span class="sxs-lookup"><span data-stu-id="64475-149">During each submission event, the communication flows in both directions:</span></span>

- <span data-ttu-id="64475-150">**Finance および Supply Chain Management から電子請求へ** – Finance および Supply Chain Management は、抽象請求書を電子請求に送信します。</span><span class="sxs-lookup"><span data-stu-id="64475-150">**From Finance and Supply Chain Management to the Electronic invoicing** – Finance and Supply Chain Management send the abstract invoices to Electronic invoicing.</span></span> <span data-ttu-id="64475-151">必要に応じて、電子請求書機能の一部として構成された変数の内容も送信されます。</span><span class="sxs-lookup"><span data-stu-id="64475-151">As required, they also send the contents of variables that were configured as part of the electronic invoicing features.</span></span>
- <span data-ttu-id="64475-152">**電子請求から財務およびサプライ チェーン マネジメントへ** - 電子請求書の機能に応じて、Finance および Supply Chain Management 管理は、電子請求から、以前に提出された請求書の処理結果に関する更新情報を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="64475-152">**From the Electronic invoicing to Finance and Supply Chain Management** – Depending on the electronic invoicing feature, Finance and Supply Chain Management receive updates from Electronic invoicing about the processing results of invoices that were previously submitted.</span></span> <span data-ttu-id="64475-153">また、電子請求書作成機能の一部として設定された変数の内容も受信します。</span><span class="sxs-lookup"><span data-stu-id="64475-153">They also receive the contents of variables that were configured as part of the electronic invoicing features.</span></span>

<span data-ttu-id="64475-154">Finance および Supply Chain Management で電子請求に電子ドキュメントを送信するには、**組織管理 &gt; 定期処理 &gt; 電子ドキュメント &gt; 電子ドキュメントの送信** に移動してください。</span><span class="sxs-lookup"><span data-stu-id="64475-154">To submit electronic documents to Electronic invoicing, in Finance and Supply Chain Management, go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Submit electronic documents**.</span></span>

<span data-ttu-id="64475-155">開始点は転記された請求書です。</span><span class="sxs-lookup"><span data-stu-id="64475-155">The starting point is a posted invoice.</span></span> <span data-ttu-id="64475-156">この請求書は、販売注文、プロジェクト請求書、自由形式の請求書など、さまざまな発生元から作成できます。</span><span class="sxs-lookup"><span data-stu-id="64475-156">This invoice can come from different origins, such as sales orders, project invoices, or free text invoices.</span></span>

<span data-ttu-id="64475-157">送信のプロセスは、手動またはバックグラウンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="64475-157">The submission process can be run manually or in the background.</span></span>

- <span data-ttu-id="64475-158">**手動実行** - 手動で実行するには、**フィルタ** オプションを使用して、送信する必要があるドキュメントの範囲を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64475-158">**Manual execution** – For manual execution, you must use the **Filter** option to define the range of documents that must be submitted.</span></span> <span data-ttu-id="64475-159">**フィルター** ページで、独自のクエリを構成して、送信する必要がある転記済請求書を選択できます。</span><span class="sxs-lookup"><span data-stu-id="64475-159">On the **Filters** page, you can configure your own query to select the posted invoices that must be submitted.</span></span> <span data-ttu-id="64475-160">選択した後、手動で処理の実行を開始し、実行が完了するまで待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="64475-160">After the selection is made, you must manually start execution of the processing and wait for it to finish running.</span></span> <span data-ttu-id="64475-161">処理が完了すると、アクション センターのメッセージに、正常に送信された電子ドキュメントの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="64475-161">When the processing is completed, a message in the Action center shows the number of electronic documents that have been successfully submitted.</span></span>
- <span data-ttu-id="64475-162">**バックグラウンド実行** - バックグラウンドでの実行は、ログインや送信ダイアログ ボックスを開いていなくても実行されます。</span><span class="sxs-lookup"><span data-stu-id="64475-162">**Background execution** – Background execution runs without requiring that you be signed in or keep the submission dialog box open.</span></span> <span data-ttu-id="64475-163">プロセスの実行をスケジュールし、実行頻度を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="64475-163">You can schedule the process to run and define the frequency of execution.</span></span>

## <a name="view-the-submission-logs"></a><span data-ttu-id="64475-164">送信ログを表示する</span><span class="sxs-lookup"><span data-stu-id="64475-164">View the submission logs</span></span>

<span data-ttu-id="64475-165">Finance および Supply Chain Management では、送信ログを使用して電子請求への送信結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="64475-165">In Finance and Supply Chain Management, you can use the submission logs to view the results of processing the submission to Electronic invoicing.</span></span> <span data-ttu-id="64475-166">**組織管理 &gt; 定期処理 &gt; 電子ドキュメント &gt; 電子ドキュメントの送信** に移動し、**ドキュメント タイプ** フィールドで、ログに表示される請求書の種類をフィルタ処理する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="64475-166">Go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Electronic document submission**, and then, in the **Document type** field, select a value to filter the type of invoices that the logs show.</span></span>

<span data-ttu-id="64475-167">送信状態には次の3つがあります。</span><span class="sxs-lookup"><span data-stu-id="64475-167">There are three possible submission statuses:</span></span>

- <span data-ttu-id="64475-168">**スケジュール済** - 電子請求は Finance と Supply Chain Management からの送信を受信し、電子請求書機能の処理を行っています。</span><span class="sxs-lookup"><span data-stu-id="64475-168">**Scheduled** – Electronic invoicing received the submission from Finance and Supply Chain Management, and processing of the electronic invoicing feature is in progress.</span></span>
- <span data-ttu-id="64475-169">**完了** - 電子請求が電子請求書機能の実行をするように設定されているため、正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="64475-169">**Completed** – Electronic invoicing successfully processed the electronic invoicing feature as it was configured to run it.</span></span>
- <span data-ttu-id="64475-170">**失敗** - 電子請求書機能の処理中に、電子請求でエラーが発生したか、例外により停止しました。</span><span class="sxs-lookup"><span data-stu-id="64475-170">**Failed** – Electronic invoicing encountered an error or was stopped by an exception during processing of the electronic invoicing feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="64475-171">送信の状態は、電子請求が電子請求機能に対して実行する処理の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="64475-171">The submission status refers to the status of the processing that Electronic invoicing does on the electronic invoicing feature.</span></span> <span data-ttu-id="64475-172">電子請求書の最終的な状態を指しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="64475-172">It doesn't refer to the final status of the electronic invoice itself.</span></span>
>
> <span data-ttu-id="64475-173">たとえば、電子請求書を外部の Web サービスに提出して承認を得る必要がある場合、送信の状態は **完了** となっていても、電子請求書の状態は **否認** である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="64475-173">For example, if an electronic invoice must be submitted to an external web service for approval, the submission status might be **Completed**, but the status of the electronic invoice might be **Rejected**.</span></span> <span data-ttu-id="64475-174">この場合、 電子請求は、電子請求書作成機能を処理するように設定されているため、正常に処理することができています。</span><span class="sxs-lookup"><span data-stu-id="64475-174">In this case, Electronic invoicing was able to successfully process the electronic invoicing feature as it's configured to process that feature.</span></span> <span data-ttu-id="64475-175">しかし、電子請求書は、We bサービスが請求書承認に設定した基準を満たしていなかったため、否認されていました。</span><span class="sxs-lookup"><span data-stu-id="64475-175">However, the electronic invoice was rejected because it didn't meet the criteria that the web service established for invoice approval.</span></span>

<span data-ttu-id="64475-176">送信ログには、次の追加機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="64475-176">The submission logs include the following additional functions:</span></span>

- <span data-ttu-id="64475-177">**送信の詳細** - 主要な送信の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="64475-177">**Submission details** – View the details of the main submission.</span></span> <span data-ttu-id="64475-178">視覚化では、電子請求書作成機能で設定されたアクションの完全な実行ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64475-178">The visualization shows the complete execution log of the actions that are configured in the electronic invoicing feature.</span></span> <span data-ttu-id="64475-179">また、ユーザーは、処理の間に作成されたファイルをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="64475-179">It also lets users download the files that are created during the processing.</span></span> <span data-ttu-id="64475-180">請求書が外部 Web サービスによって承認される必要がある場合は、請求書の状態をユーザーが確認できます。</span><span class="sxs-lookup"><span data-stu-id="64475-180">In scenarios where the invoice must be approved by an external web service, it lets users view the status of the invoice.</span></span>
- <span data-ttu-id="64475-181">**関連する送信** - 子送信の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="64475-181">**Related submissions** – View the details of child submissions.</span></span>
- <span data-ttu-id="64475-182">**送信のキャンセル** - この機能により、外部 Web サービスによって電子請求書を承認する必要がある場合に、特別な送信プロセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="64475-182">**Cancel submissions** – This function enables a special submission process in scenarios where the electronic invoice must be approved by an external web service.</span></span> <span data-ttu-id="64475-183">これは、Web サービス データベース内の承認済み電子請求書の状態をキャンセルする特定のメッセージを Web サービスに送信するよう、電子請求に指示します。</span><span class="sxs-lookup"><span data-stu-id="64475-183">It instructs Electronic invoicing to send the web service a specific message that is intended to cancel the status of an approved electronic invoice in the web service database.</span></span>
- <span data-ttu-id="64475-184">**ドキュメントの再送信** - 電子請求に既に送信されている電子ドキュメント を再送信します。</span><span class="sxs-lookup"><span data-stu-id="64475-184">**Resubmit document** – Resubmit an electronic document that has already been submitted to Electronic invoicing.</span></span> <span data-ttu-id="64475-185">**送信の詳細** ページに、新しいログが作成されます。</span><span class="sxs-lookup"><span data-stu-id="64475-185">A new log is created on the **Submission details** page.</span></span>
- <span data-ttu-id="64475-186">**関連する送信を送信**</span><span class="sxs-lookup"><span data-stu-id="64475-186">**Send related submission**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
