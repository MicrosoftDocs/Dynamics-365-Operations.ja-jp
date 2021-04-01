---
title: ワークフロー システムに請求書を送信し、製品受領書行を照合
description: このトピックでは、仕入先請求書をワークフロー システムに送信し、転記された製品受領書明細行を仕入先請求書に自動的に照合するプロセスについて説明します。
author: abruer
manager: AnnBe
ms.date: 09/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2017-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 534b5dbc54a516fea0b3f7090042d247c1076737
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231545"
---
# <a name="submit-invoices-to-the-workflow-system-and-match-product-receipt-lines"></a><span data-ttu-id="5a1fc-103">ワークフロー システムに請求書を送信し、製品受領書行を照合</span><span class="sxs-lookup"><span data-stu-id="5a1fc-103">Submit invoices to the workflow system and match product receipt lines</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a1fc-104">このトピックでは、仕入先請求書をワークフロー システムに送信し、転記された製品受領書明細行を仕入先請求書に自動的に照合するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-104">This topic explains the process of submitting vendor invoices to the workflow system and automatically matching posted product receipt lines to vendor invoices.</span></span>

## <a name="submitting-imported-vendor-invoices-to-the-workflow-system-and-matching-posted-product-receipt-lines-to-pending-vendor-invoice-lines"></a><span data-ttu-id="5a1fc-105">インポートされた仕入先請求書をワークフロー システムに送信し、転記された製品受領書明細行を保留中の仕入先請求書明細行と照合する</span><span class="sxs-lookup"><span data-stu-id="5a1fc-105">Submitting imported vendor invoices to the workflow system and matching posted product receipt lines to pending vendor invoice lines</span></span>

<span data-ttu-id="5a1fc-106">継続的な買掛金勘定請求プロセスの一部として、インポートした請求書をシステムが自動的にワークフロー システムに送信するようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-106">As part of a touchless Accounts payable invoicing process, you can have the system automatically submit an imported invoice to the workflow system.</span></span> <span data-ttu-id="5a1fc-107">インポートされた請求書をワークフロー システムに送信するプロセスは、**買掛金パラメーター** ページの **仕入先請求書の自動化** タブで構成できます (**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター**)。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-107">You can configure the process of submitting imported invoices to the workflow system on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span> <span data-ttu-id="5a1fc-108">ワークフローへの送信プロセスは、指定した頻度 (毎時間または毎日) でバックグラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-108">The submit-to-workflow process will run in the background, at a frequency that you specify (either hourly or daily).</span></span>

<span data-ttu-id="5a1fc-109">請求書をワークフロー システムに自動的に送信する場合は、インポートされた請求書から開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-109">When you automatically submit invoices to the workflow system, you must begin with an imported invoice.</span></span> <span data-ttu-id="5a1fc-110">手動操作なしで請求書を開始から終了まで処理できるようにするには、自動化された転記タスクをワークフロー コンフィギュレーションに含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-110">To ensure that the invoice can be processed from start to finish without manual intervention, you must include an automated posting task in the workflow configuration.</span></span> <span data-ttu-id="5a1fc-111">発注書 (PO) に関連付けられている請求書、および発注書以外の調達カテゴリと非在庫明細行が含まれている請求書は、ワークフロー システムに自動的に送信できます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-111">Invoices that are related to purchase orders (POs), and invoices that contain a non-PO procurement category and non-stocked lines, can automatically be submitted to the workflow system.</span></span> <span data-ttu-id="5a1fc-112">手動で入力された請求書は、ワークフロー システムに手動で送信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-112">Invoices that are manually entered must be manually submitted to the workflow system.</span></span>

<span data-ttu-id="5a1fc-113">ワークフローの **送信者** の値は、**プロセスの自動化** ページの **仕入先請求書をワークフローに送信** バックグラウンド タスクに入力されたユーザー ID です。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-113">The **Submitted by** value in the workflow is the user ID that was entered for the **Submit vendor invoices to workflow** background task on the **Process automation** page.</span></span> <span data-ttu-id="5a1fc-114">そのユーザー ID を持つユーザーは、必要に応じてワークフロー システムから請求書を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-114">The user who has that user ID will be able to recall the invoice from the workflow system as required.</span></span>

## <a name="matching-posted-product-receipts-to-invoice-lines-that-have-a-three-way-matching-policy"></a><span data-ttu-id="5a1fc-115">転記された製品受領書とスリーウェイ マッチング ポリシーが適用された請求書明細行を照合する</span><span class="sxs-lookup"><span data-stu-id="5a1fc-115">Matching posted product receipts to invoice lines that have a three-way matching policy</span></span>

<span data-ttu-id="5a1fc-116">継続的な買掛金勘定請求プロセスの一部として、システムは、転記された製品受領書を請求書明細行に自動的に照合できます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-116">As part of a touchless Accounts payable invoicing process, the system can automatically match posted product receipts to invoice lines.</span></span> <span data-ttu-id="5a1fc-117">このタスクには、スリーウェイ マッチングポリシーを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-117">A three-way matching policy must be defined for this task.</span></span> <span data-ttu-id="5a1fc-118">この機能は、**機能の管理** ページで **仕入先請求書の自動化** 機能が有効になっている場合に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-118">This feature is available if the **Vendor invoice automation** feature has been enabled on the **Feature management** page.</span></span>

<span data-ttu-id="5a1fc-119">プロセスは、照合した製品受領書の数量と請求書の数量が等しくなるまで実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-119">The process will run until the matched product receipt quantity equals the invoice quantity.</span></span> <span data-ttu-id="5a1fc-120">このプロセスの一部として、プロセスが失敗して終了するまでに、システムが製品受領書を請求明細行と照合する最大回数を指定できます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-120">As part of this process, you can specify the maximum number of times that the system should try to match product receipts to an invoice line before it concludes that the process failed.</span></span> <span data-ttu-id="5a1fc-121">プロセスは、毎時間または毎日、バックグラウンドで実行されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-121">The process will run in the background, either hourly or daily.</span></span> <span data-ttu-id="5a1fc-122">自動照合プロセスは、ワークフロー システムに請求書を送信するプロセスの一部として実行できます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-122">You can run the automated matching process as part of the process for submitting invoices to the workflow system.</span></span> <span data-ttu-id="5a1fc-123">または、スタンドアロン プロセスとして実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-123">Alternatively, you can run it as a standalone process.</span></span> <span data-ttu-id="5a1fc-124">製品受領書と請求書明細行の照合プロセスの設定は、**買掛金パラメーター** ページの **仕入先請求書の自動化** タブで構成されます (**買掛金勘定 \> 設定 \> 買掛金勘定パラメーター**)。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-124">The settings for the match-product-receipts-to-invoice-lines process are configured on the **Vendor invoice automation** tab of the **Accounts payable parameters** page (**Accounts payable \> Setup \> Accounts payable parameters**).</span></span>

<span data-ttu-id="5a1fc-125">照合された受領書の数量が請求書の数量より少ない、スリーウェイ マッチングポリシーを持つ請求書明細行は、自動化された製品受領書との照合プロセスに含まれます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-125">Invoice lines that have a three-way matching policy, where the matched receipt quantity is less than the invoice quantity, will be included in the automated match-to-product-receipt process.</span></span>

<span data-ttu-id="5a1fc-126">自動化されたワークフローへの送信プロセスに含まれていない請求書の **最新の照合** 状態を表示するには、**仕入先請求書** ページから請求書を開きます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-126">To view the **Last match** status for invoices that aren't part of the automated submit-to-workflow process, open the invoice from the **Vendor invoices** page.</span></span> <span data-ttu-id="5a1fc-127">請求書を表示すると、照合検証情報が更新されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-127">When you view the invoice, the matching validation information is updated.</span></span> <span data-ttu-id="5a1fc-128">**請求書照合の検証** のバックグラウンド タスクを使用して、**最終一致** ステータス が自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-128">The **Last match** status can be updated automatically using the **Validate invoice matching** background task.</span></span> <span data-ttu-id="5a1fc-129">**プロセスの自動化** ページの **バックグラウンド プロセス** タブ (**システム管理者\>設定\>プロセス自動化**) で、**最終一致** ステータスを自動的に更新するプロセスを構成できます 。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-129">You can configure the process of automatically updating the **Last match** status on the **Background processes** tab of the **Process automations** page (**System adminstration\> Setup\> Process automations**).</span></span>

<span data-ttu-id="5a1fc-130">請求書明細行は、次のいずれかの条件が満たされた場合に自動処理から除外されます。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-130">An invoice line will be excluded from the automated processing if any of the following conditions are met:</span></span>

- <span data-ttu-id="5a1fc-131">請求書明細行の **自動受領書照合状態** 値は、**失敗** です。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-131">The **Automated receipt match status** value of the invoice line is **Failed**.</span></span>
- <span data-ttu-id="5a1fc-132">請求書が使用されています。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-132">The invoice is being used.</span></span>
- <span data-ttu-id="5a1fc-133">請求書はワークフロー システムにあります。</span><span class="sxs-lookup"><span data-stu-id="5a1fc-133">The invoice is in the workflow system.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]