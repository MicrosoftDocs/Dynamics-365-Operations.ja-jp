---
title: Finance および Supply Chain Management で電子請求書を発行する
description: このトピックでは、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management で電子請求書のアドオンを使用して電子請求書を発行する方法について説明します。
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 187f5a20d088b4fcd7af2a6576357a69c2efc2c6
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104404"
---
# <a name="issue-electronic-invoices-in-finance-and-supply-chain-management"></a><span data-ttu-id="18c83-103">Finance および Supply Chain Management で電子請求書を発行する</span><span class="sxs-lookup"><span data-stu-id="18c83-103">Issue electronic invoices in Finance and Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="18c83-104">このトピックでは、Microsoft Dynamics 365 Finance と Dynamics 365 Supply Chain Management で電子請求書のアドオンを使用して電子請求書を発行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="18c83-104">This topic explains how to issue electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management through the Electronic invoicing add-on.</span></span>


## <a name="feature-activation"></a><span data-ttu-id="18c83-105">機能の有効化</span><span class="sxs-lookup"><span data-stu-id="18c83-105">Feature activation</span></span>

<span data-ttu-id="18c83-106">電子請求書アドオンで電子請求書の発行を開始するには、Finance および Supply Chain Management の機能参照を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="18c83-106">To start issuing electronic invoices through the Electronic invoicing add-on, it is necessary to activate the Feature reference in Finance and Supply Chain Management.</span></span>

<span data-ttu-id="18c83-107">各機能参照は、国/地域の電子請求書発行の要件に準拠した特定の電子請求書発行機能に対応しています。</span><span class="sxs-lookup"><span data-stu-id="18c83-107">Each Feature reference corresponds to a specific electronic invoicing feature that complies to the electronic invoicing requirements from a country/region.</span></span>

<span data-ttu-id="18c83-108">次の表に、電子請求書アドオンに対応する機能参照の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="18c83-108">The following table shows the list of feature References that the Electronic invoicing add-on supports.</span></span>

| <span data-ttu-id="18c83-109">機能リファレンス</span><span class="sxs-lookup"><span data-stu-id="18c83-109">Feature reference</span></span> | <span data-ttu-id="18c83-110">氏名</span><span class="sxs-lookup"><span data-stu-id="18c83-110">Name</span></span>                                              | <span data-ttu-id="18c83-111">国/地域</span><span class="sxs-lookup"><span data-stu-id="18c83-111">Country/region</span></span> |
|-------------------|---------------------------------------------------|----------------|
| <span data-ttu-id="18c83-112">BR-00053</span><span class="sxs-lookup"><span data-stu-id="18c83-112">BR-00053</span></span>          | <span data-ttu-id="18c83-113">NF-e Federal - ブラジル電子請求書</span><span class="sxs-lookup"><span data-stu-id="18c83-113">NF-e Federal - Brazilian electronic invoice</span></span>       | <span data-ttu-id="18c83-114">ブラジル</span><span class="sxs-lookup"><span data-stu-id="18c83-114">Brazil</span></span>         |
| <span data-ttu-id="18c83-115">BR-00095</span><span class="sxs-lookup"><span data-stu-id="18c83-115">BR-00095</span></span>          | <span data-ttu-id="18c83-116">NFS-e ブラジル電子請求書</span><span class="sxs-lookup"><span data-stu-id="18c83-116">NFS-e Brazilian electronic invoices</span></span>               | <span data-ttu-id="18c83-117">ブラジル</span><span class="sxs-lookup"><span data-stu-id="18c83-117">Brazil</span></span>         |
| <span data-ttu-id="18c83-118">DK-00001</span><span class="sxs-lookup"><span data-stu-id="18c83-118">DK-00001</span></span>          | <span data-ttu-id="18c83-119">公的機関への電子請求書 (OIOUBL) – DK</span><span class="sxs-lookup"><span data-stu-id="18c83-119">E-invoicing to the public sector (OIOUBL) – DK</span></span>    | <span data-ttu-id="18c83-120">デンマーク</span><span class="sxs-lookup"><span data-stu-id="18c83-120">Denmark</span></span>        |
| <span data-ttu-id="18c83-121">EG-00008</span><span class="sxs-lookup"><span data-stu-id="18c83-121">EG-00008</span></span>          | <span data-ttu-id="18c83-122">エジプトの電子請求</span><span class="sxs-lookup"><span data-stu-id="18c83-122">E-invoicing for Egypt</span></span>                             | <span data-ttu-id="18c83-123">エジプト</span><span class="sxs-lookup"><span data-stu-id="18c83-123">Egypt</span></span>          |
| <span data-ttu-id="18c83-124">ES-00025</span><span class="sxs-lookup"><span data-stu-id="18c83-124">ES-00025</span></span>          | <span data-ttu-id="18c83-125">公的部門向けの電子請求書</span><span class="sxs-lookup"><span data-stu-id="18c83-125">Electronic Invoice to the public sector</span></span>           | <span data-ttu-id="18c83-126">スペイン</span><span class="sxs-lookup"><span data-stu-id="18c83-126">Spain</span></span>          |
| <span data-ttu-id="18c83-127">EUR-00023</span><span class="sxs-lookup"><span data-stu-id="18c83-127">EUR-00023</span></span>         | <span data-ttu-id="18c83-128">欧州連合の公共部門向けの電子請求書</span><span class="sxs-lookup"><span data-stu-id="18c83-128">European Union E-invoicing to Public sector</span></span>       | <span data-ttu-id="18c83-129">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="18c83-129">Europe</span></span>         |
| <span data-ttu-id="18c83-130">ITA-00036</span><span class="sxs-lookup"><span data-stu-id="18c83-130">ITA-00036</span></span>         | <span data-ttu-id="18c83-131">IT - 公的機関に電子請求 (FatturaPA)</span><span class="sxs-lookup"><span data-stu-id="18c83-131">IT - E-invoicing to the public sector (FatturaPA)</span></span> | <span data-ttu-id="18c83-132">イタリア</span><span class="sxs-lookup"><span data-stu-id="18c83-132">Italy</span></span>          |
| <span data-ttu-id="18c83-133">MX-00010</span><span class="sxs-lookup"><span data-stu-id="18c83-133">MX-00010</span></span>          | <span data-ttu-id="18c83-134">CFDI の電子請求</span><span class="sxs-lookup"><span data-stu-id="18c83-134">E-invoicing CFDI</span></span>                                  | <span data-ttu-id="18c83-135">メキシコ</span><span class="sxs-lookup"><span data-stu-id="18c83-135">Mexico</span></span>         |
| <span data-ttu-id="18c83-136">MX-00016</span><span class="sxs-lookup"><span data-stu-id="18c83-136">MX-00016</span></span>          | <span data-ttu-id="18c83-137">電子請求 CFDI - キャンセル プロセス</span><span class="sxs-lookup"><span data-stu-id="18c83-137">E-invoicing CFDI - cancellation process</span></span>           | <span data-ttu-id="18c83-138">メキシコ</span><span class="sxs-lookup"><span data-stu-id="18c83-138">Mexico</span></span>         |

<span data-ttu-id="18c83-139">当該国のローカライズのスコープに対応しているレガシーな電子請求書発行機能がある場合には、機能参照をアクティブ化することで、電子請求書発行アドオンを介して電子請求書の発行が可能になり、以前の機能がオフになります。</span><span class="sxs-lookup"><span data-stu-id="18c83-139">In the cases where there is a legacy electronic invoicing feature, supported the country localizations scope, the activation of the Feature reference enables the issuing of electronic invoices through the Electronic invoicing add-on and turns-off the former feature.</span></span>

## <a name="submit-electronic-documents"></a><span data-ttu-id="18c83-140">電子ドキュメントの送信</span><span class="sxs-lookup"><span data-stu-id="18c83-140">Submit electronic documents</span></span>

<span data-ttu-id="18c83-141">電子文書を提出するプロセスは、Finance および Supply Chain Management 管理と電子請求書アドオンとの間の単一のコミュニケーションポイントを表しています。</span><span class="sxs-lookup"><span data-stu-id="18c83-141">The process of submitting electronic documents represents the single point of communication between Finance and Supply Chain Management and the Electronic invoicing add-on.</span></span> <span data-ttu-id="18c83-142">各送信イベントで、両方向に通信が流れます。</span><span class="sxs-lookup"><span data-stu-id="18c83-142">During each submission event, the communication flows in both directions:</span></span>

- <span data-ttu-id="18c83-143">**Finance および Supply Chain Management から電子請求アドオンへ** – Finance および Supply Chain Management は、抽象請求書を電子請求 アドオンに送信します。</span><span class="sxs-lookup"><span data-stu-id="18c83-143">**From Finance and Supply Chain Management to the Electronic invoicing add-on** – Finance and Supply Chain Management send the abstract invoices to the Electronic invoicing add-on.</span></span> <span data-ttu-id="18c83-144">必要に応じて、電子請求書機能の一部として構成された変数の内容も送信されます。</span><span class="sxs-lookup"><span data-stu-id="18c83-144">As required, they also send the contents of variables that were configured as part of the electronic invoicing features.</span></span>
- <span data-ttu-id="18c83-145">**電子請求アドオンから財務およびサプライ チェーン マネジメントへ** - 電子請求書の機能に応じて、Finance および Supply Chain Management 管理は、電子請求書アドオンから、以前に提出された請求書の処理結果に関する更新情報を受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="18c83-145">**From the Electronic invoicing add-on to Finance and Supply Chain Management** – Depending on the electronic invoicing feature, Finance and Supply Chain Management receive updates from the Electronic invoicing add-on about the processing results of invoices that were previously submitted.</span></span> <span data-ttu-id="18c83-146">また、電子請求書作成機能の一部として設定された変数の内容も受信します。</span><span class="sxs-lookup"><span data-stu-id="18c83-146">They also receive the contents of variables that were configured as part of the electronic invoicing features.</span></span>

<span data-ttu-id="18c83-147">Finance および Supply Chain Management で電子請求書アドオンに電子ドキュメントを送信するには、**組織管理 &gt; 定期処理 &gt; 電子ドキュメント &gt; 電子ドキュメントの送信** に移動してください。</span><span class="sxs-lookup"><span data-stu-id="18c83-147">To submit electronic documents to the Electronic invoicing add-on, in Finance and Supply Chain Management, go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Submit electronic documents**.</span></span>

<span data-ttu-id="18c83-148">開始点は転記された請求書です。</span><span class="sxs-lookup"><span data-stu-id="18c83-148">The starting point is a posted invoice.</span></span> <span data-ttu-id="18c83-149">この請求書は、販売注文、プロジェクト請求書、自由形式の請求書など、さまざまな発生元から作成できます。</span><span class="sxs-lookup"><span data-stu-id="18c83-149">This invoice can come from different origins, such as sales orders, project invoices, or free text invoices.</span></span>

<span data-ttu-id="18c83-150">送信のプロセスは、手動またはバックグラウンドで実行できます。</span><span class="sxs-lookup"><span data-stu-id="18c83-150">The submission process can be run manually or in the background.</span></span>

- <span data-ttu-id="18c83-151">**手動実行** - 手動で実行するには、**フィルタ** オプションを使用して、送信する必要があるドキュメントの範囲を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18c83-151">**Manual execution** – For manual execution, you must use the **Filter** option to define the range of documents that must be submitted.</span></span> <span data-ttu-id="18c83-152">**フィルター** ページで、独自のクエリを構成して、送信する必要がある転記済請求書を選択できます。</span><span class="sxs-lookup"><span data-stu-id="18c83-152">On the **Filters** page, you can configure your own query to select the posted invoices that must be submitted.</span></span> <span data-ttu-id="18c83-153">選択した後、手動で処理の実行を開始し、実行が完了するまで待つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="18c83-153">After the selection is made, you must manually start execution of the processing and wait for it to finish running.</span></span> <span data-ttu-id="18c83-154">処理が完了すると、アクション センターのメッセージに、正常に送信された電子ドキュメントの数が表示されます。</span><span class="sxs-lookup"><span data-stu-id="18c83-154">When the processing is completed, a message in the Action center shows the number of electronic documents that have been successfully submitted.</span></span>
- <span data-ttu-id="18c83-155">**バックグラウンド実行** - バックグラウンドでの実行は、ログインや送信ダイアログ ボックスを開いていなくても実行されます。</span><span class="sxs-lookup"><span data-stu-id="18c83-155">**Background execution** – Background execution runs without requiring that you be signed in or keep the submission dialog box open.</span></span> <span data-ttu-id="18c83-156">プロセスの実行をスケジュールし、実行頻度を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="18c83-156">You can schedule the process to run and define the frequency of execution.</span></span>

## <a name="view-the-submission-logs"></a><span data-ttu-id="18c83-157">送信ログを表示する</span><span class="sxs-lookup"><span data-stu-id="18c83-157">View the submission logs</span></span>

<span data-ttu-id="18c83-158">Finance および Supply Chain Management では、送信ログを使用して電子請求書アドオンへの送信結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="18c83-158">In Finance and Supply Chain Management, you can use the submission logs to view the results of processing the submission to the Electronic invoicing add-on.</span></span> <span data-ttu-id="18c83-159">**組織管理 &gt; 定期処理 &gt; 電子ドキュメント &gt; 電子ドキュメントの送信** に移動し、**ドキュメント タイプ** フィールドで、ログに表示される請求書の種類をフィルタ処理する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="18c83-159">Go to **Organization administration &gt; Periodic &gt; Electronic documents &gt; Electronic document submission**, and then, in the **Document type** field, select a value to filter the type of invoices that the logs show.</span></span>

<span data-ttu-id="18c83-160">送信状態には次の3つがあります。</span><span class="sxs-lookup"><span data-stu-id="18c83-160">There are three possible submission statuses:</span></span>

- <span data-ttu-id="18c83-161">**スケジュール済** - 電子請求書アドオンは Finance と Supply Chain Management からの送信を受信し、電子請求書機能の処理を行っています。</span><span class="sxs-lookup"><span data-stu-id="18c83-161">**Scheduled** – The Electronic invoicing add-on received the submission from Finance and Supply Chain Management, and processing of the electronic invoicing feature is in progress.</span></span>
- <span data-ttu-id="18c83-162">**完了** - 電子請求書作成アドオンが電子請求書機能の実行をするように設定されているため、正常に処理されました。</span><span class="sxs-lookup"><span data-stu-id="18c83-162">**Completed** – The Electronic invoicing add-on successfully processed the electronic invoicing feature as it was configured to run it.</span></span>
- <span data-ttu-id="18c83-163">**失敗** - 電子請求書機能の処理中に、電子請求書アドオンでエラーが発生したか、例外により停止しました。</span><span class="sxs-lookup"><span data-stu-id="18c83-163">**Failed** – The Electronic invoicing add-on encountered an error or was stopped by an exception during processing of the electronic invoicing feature.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="18c83-164">送信の状態は、電子請求書アドオンが電子請求書機能に対して実行する処理の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="18c83-164">The submission status refers to the status of the processing that the Electronic invoicing add-on does on the electronic invoicing feature.</span></span> <span data-ttu-id="18c83-165">電子請求書の最終的な状態を指しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="18c83-165">It doesn't refer to the final status of the electronic invoice itself.</span></span>
>
> <span data-ttu-id="18c83-166">たとえば、電子請求書を外部の Web サービスに提出して承認を得る必要がある場合、送信の状態は **完了** となっていても、電子請求書の状態は **否認** である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="18c83-166">For example, if an electronic invoice must be submitted to an external web service for approval, the submission status might be **Completed**, but the status of the electronic invoice might be **Rejected**.</span></span> <span data-ttu-id="18c83-167">この場合、 電子請求書作成アドオンは、電子請求書作成機能を処理するように設定されているため、正常に処理することができています。</span><span class="sxs-lookup"><span data-stu-id="18c83-167">In this case, the Electronic invoicing add-on was able to successfully process the electronic invoicing feature as it's configured to process that feature.</span></span> <span data-ttu-id="18c83-168">しかし、電子請求書は、We bサービスが請求書承認に設定した基準を満たしていなかったため、否認されていました。</span><span class="sxs-lookup"><span data-stu-id="18c83-168">However, the electronic invoice was rejected because it didn't meet the criteria that the web service established for invoice approval.</span></span>

<span data-ttu-id="18c83-169">送信ログには、次の追加機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="18c83-169">The submission logs include the following additional functions:</span></span>

- <span data-ttu-id="18c83-170">**送信の詳細** - 主要な送信の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="18c83-170">**Submission details** – View the details of the main submission.</span></span> <span data-ttu-id="18c83-171">視覚化では、電子請求書作成機能で設定されたアクションの完全な実行ログが表示されます。</span><span class="sxs-lookup"><span data-stu-id="18c83-171">The visualization shows the complete execution log of the actions that are configured in the electronic invoicing feature.</span></span> <span data-ttu-id="18c83-172">また、ユーザーは、処理の間に作成されたファイルをダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="18c83-172">It also lets users download the files that are created during the processing.</span></span> <span data-ttu-id="18c83-173">請求書が外部 Web サービスによって承認される必要がある場合は、請求書の状態をユーザーが確認できます。</span><span class="sxs-lookup"><span data-stu-id="18c83-173">In scenarios where the invoice must be approved by an external web service, it lets users view the status of the invoice.</span></span>
- <span data-ttu-id="18c83-174">**関連する送信** - 子送信の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="18c83-174">**Related submissions** – View the details of child submissions.</span></span>
- <span data-ttu-id="18c83-175">**送信のキャンセル** - この機能により、外部 Web サービスによって電子請求書を承認する必要がある場合に、特別な送信プロセスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="18c83-175">**Cancel submissions** – This function enables a special submission process in scenarios where the electronic invoice must be approved by an external web service.</span></span> <span data-ttu-id="18c83-176">これは、Web サービス データベース内の承認済み電子請求書の状態をキャンセルする特定のメッセージを Web サービスに送信するよう、電子請求書アドオンに指示します。</span><span class="sxs-lookup"><span data-stu-id="18c83-176">It instructs the Electronic invoicing add-on to send the web service a specific message that is intended to cancel the status of an approved electronic invoice in the web service database.</span></span>
- <span data-ttu-id="18c83-177">**ドキュメントの再送信** - 電子請求アドオンに既に送信されている電子ドキュメント を再送信します。</span><span class="sxs-lookup"><span data-stu-id="18c83-177">**Resubmit document** – Resubmit an electronic document that has already been submitted to the Electronic invoicing add-on.</span></span> <span data-ttu-id="18c83-178">**送信の詳細** ページに、全く新しいログが作成されます。</span><span class="sxs-lookup"><span data-stu-id="18c83-178">A whole new log is created on the **Submission details** page.</span></span>
- <span data-ttu-id="18c83-179">**関連する送信を送信**</span><span class="sxs-lookup"><span data-stu-id="18c83-179">**Send related submission**</span></span>
