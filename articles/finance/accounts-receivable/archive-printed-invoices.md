---
title: 印刷された顧客請求書にハッシュ番号を付けてアーカイブする
description: このトピックでは、ハッシュ番号付きの印刷された顧客請求書を保存するアーカイブを有効にする方法について説明します。
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5b0305381ee709ce52b18d171a1ea274e2126cce
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827701"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="1d14d-103">印刷された顧客請求書にハッシュ番号を付けてアーカイブする</span><span class="sxs-lookup"><span data-stu-id="1d14d-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="1d14d-104">一部の国では、一部のドキュメントの印刷と共に計算されたハッシュ番号をシステムに保存する法的要件があります。</span><span class="sxs-lookup"><span data-stu-id="1d14d-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="1d14d-105">ハッシュ番号は、関係機関への報告や監査時に使用できます。</span><span class="sxs-lookup"><span data-stu-id="1d14d-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="1d14d-106">このトピックでは、ハッシュ番号付きの印刷された顧客請求書を保存するアーカイブを設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d14d-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1d14d-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="1d14d-107">Prerequisites</span></span>

- <span data-ttu-id="1d14d-108">**機能管理** ワークスペースで、機能を有効にし、**印刷された顧客請求書をハッシュ番号でアーカイブします**。</span><span class="sxs-lookup"><span data-stu-id="1d14d-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="1d14d-109">詳細については [機能管理の概要](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1d14d-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="1d14d-110">**印刷管理** で必要なドキュメントの印刷可能な形式を説明します。</span><span class="sxs-lookup"><span data-stu-id="1d14d-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="1d14d-111">この機能は次のドキュメントに適用できます。</span><span class="sxs-lookup"><span data-stu-id="1d14d-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="1d14d-112">**売掛金勘定**</span><span class="sxs-lookup"><span data-stu-id="1d14d-112">**Accounts receivable**</span></span>
- <span data-ttu-id="1d14d-113">顧客請求書</span><span class="sxs-lookup"><span data-stu-id="1d14d-113">Customer invoice</span></span>
- <span data-ttu-id="1d14d-114">顧客訂正票</span><span class="sxs-lookup"><span data-stu-id="1d14d-114">Customer credit note</span></span>
- <span data-ttu-id="1d14d-115">自由書式の請求書</span><span class="sxs-lookup"><span data-stu-id="1d14d-115">Free text invoice</span></span>
- <span data-ttu-id="1d14d-116">自由書式の訂正票</span><span class="sxs-lookup"><span data-stu-id="1d14d-116">Free text credit note</span></span>

<span data-ttu-id="1d14d-117">**プロジェクト管理および会計**</span><span class="sxs-lookup"><span data-stu-id="1d14d-117">**Project management and accounting**</span></span>
- <span data-ttu-id="1d14d-118">プロジェクト請求書</span><span class="sxs-lookup"><span data-stu-id="1d14d-118">Project invoice</span></span>
- <span data-ttu-id="1d14d-119">プロジェクト訂正票</span><span class="sxs-lookup"><span data-stu-id="1d14d-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="1d14d-120">顧客マスター データの構成</span><span class="sxs-lookup"><span data-stu-id="1d14d-120">Configure customer master data</span></span>
<span data-ttu-id="1d14d-121">顧客データを構成し、印刷した請求書を添付ファイルとして自動的に保存する機能を有効にする場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="1d14d-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="1d14d-122">**売掛金勘定** > **すべての顧客** に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d14d-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="1d14d-123">顧客を選択し、**eInvoice の添付ファイル** フィールドの **E-INVOCE** セクションで、**請求書と出荷** FastTab から、**はい** を選びます。</span><span class="sxs-lookup"><span data-stu-id="1d14d-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="1d14d-124">請求書の印刷</span><span class="sxs-lookup"><span data-stu-id="1d14d-124">Print invoices</span></span>
<span data-ttu-id="1d14d-125">前の手順で設定した顧客の自由形式、顧客、およびプロジェクト請求書または貸方伝票を転記および印刷できます。</span><span class="sxs-lookup"><span data-stu-id="1d14d-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="1d14d-126">印刷された請求書の **添付ファイル** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="1d14d-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="1d14d-127">**ドキュメント ハッシュ番号** フィールドの **追加の詳細** フィールド グループから、**添付ファイル** FastTab で、印刷済み請求書の計算された保存済ハッシュ番号を探します。</span><span class="sxs-lookup"><span data-stu-id="1d14d-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![添付ファイル のハッシュ番号](media/attach-hash-num.jpg)

