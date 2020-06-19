---
title: プロジェクト見積の確認、更新、送信
description: このトピックでは、顧客に見積書を送信して確認し、フィードバックに基づいて修正し、見積書を再送信する流れについて説明します。
author: kfend
manager: AnnBe
ms.date: 05/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 7c2f7435ed63702dafb52b0eff57c0f174ff829e
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410240"
---
# <a name="confirm-update-and-send-a-project-quotation"></a><span data-ttu-id="fd31e-103">プロジェクト見積の確認、更新、送信</span><span class="sxs-lookup"><span data-stu-id="fd31e-103">Confirm, update, and send a project quotation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd31e-104">プロジェクトの見積を作成して顧客に送信した後は、見積のステータスを **送信済** に更新する前に顧客から確認を受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd31e-104">After you create and send a project quotation to a customer, you must get confirmation from the customer before you update the quotation status to **Sent**.</span></span> <span data-ttu-id="fd31e-105">顧客から要望のあった修正は、見積書の中で更新することができます。</span><span class="sxs-lookup"><span data-stu-id="fd31e-105">Any modifications requested by the customer can be updated in the quotation.</span></span> <span data-ttu-id="fd31e-106">見積のステータスを **送信済** に更新した後は、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="fd31e-106">After you update the quotation status to **Sent**, you can’t modify it.</span></span> <span data-ttu-id="fd31e-107">以下の手順では、見積書を送信して確認し、フィードバックに基づいた更新を行い、見積書を再送信する流れで使用するオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-107">The following procedure describes the options to send a quotation for confirmation, make updates based on feedback, and then send the quotation.</span></span>

## <a name="send-a-project-quotation-confirmation"></a><span data-ttu-id="fd31e-108">プロジェクト見積の確認を送信する</span><span class="sxs-lookup"><span data-stu-id="fd31e-108">Send a project quotation confirmation</span></span>  

<span data-ttu-id="fd31e-109">確認をする目的で、既存のプロジェクトの見積書を電子メールで送信するか、印刷したコピーとして送信することができます。</span><span class="sxs-lookup"><span data-stu-id="fd31e-109">You can send an existing project quotation for confirmation through email or as a printed copy.</span></span> 

1. <span data-ttu-id="fd31e-110">**プロジェクト管理と会計** > **見積書** > **プロジェクト見積** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-110">Go to **Project management and accounting** > **Quotations** > **Project quotation.**</span></span> 
2. <span data-ttu-id="fd31e-111">**プロジェクト見積** ページで、確認をする目的で送信する見積を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-111">On the **Project quotation** page, select the quotation you want to send for confirmation.</span></span> 
3. <span data-ttu-id="fd31e-112">**生成**グループの、**フォローアップ**タブで、 **確認**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-112">On the **Follow up** tab, in the **Generate** group, select **Confirm**.</span></span> 
4. <span data-ttu-id="fd31e-113">**見積の確認** ページで、必要なパラメータを設定します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-113">On the **Confirm quotation** page, set the required parameters.</span></span> <span data-ttu-id="fd31e-114">たとえば、確認を印刷するには、**印刷**オプションで**印刷の確認**をオンにして、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-114">For example, to print the confirmation, under **Print** options, turn on **Print confirmation**, and then select **OK**.</span></span>
5. <span data-ttu-id="fd31e-115">**見積書の送信**ページで、**オプション**を選択し、**印刷先の設定**ページで、見積もりの送信先として**画面**、**電子メール**、**ファイル**、**印刷アーカイブ**、**印刷**を選択し、続いて**設計**エリアで見積書のルーティングの調整を行います。</span><span class="sxs-lookup"><span data-stu-id="fd31e-115">On the **Send quotation** page, select **Options**, and on the **Print destination settings** page, select whether you want the quotation sent to **Screen**, **E-mail**, **File**, **Print archive**, or **Printer**, and then make any adjustments that you want in the **Specification** area to route the quotation.</span></span>
6. <span data-ttu-id="fd31e-116">**印刷先の設定** ページで、**OK**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-116">On the **Print destination settings** page, select **OK**.</span></span>  

## <a name="update-a-project-quotation"></a><span data-ttu-id="fd31e-117">プロジェクトの見積を更新する</span><span class="sxs-lookup"><span data-stu-id="fd31e-117">Update a project quotation</span></span>

<span data-ttu-id="fd31e-118">既存のプロジェクトの見積を変更するには、見積のステータスを**作成する**必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd31e-118">To modify an existing project quotation, the quotation status must be **Created**.</span></span> <span data-ttu-id="fd31e-119">既存の見積を更新するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-119">Complete the following steps to update an existing quotation.</span></span> 

1. <span data-ttu-id="fd31e-120">**プロジェクト管理と会計** > **見積書** > **プロジェクト見積** に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-120">Go to **Project management and accounting** > **Quotations** > **Project quotations**.</span></span>
2. <span data-ttu-id="fd31e-121">**プロジェクトの見積** ページで、更新する見積を選択し、アクションウィンドウで **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-121">On the **Project quotations** page, select the quotation you want to update and on the Action Pane, select **Edit**.</span></span>
3. <span data-ttu-id="fd31e-122">必要なフィールドの情報を更新し、アクション ウィンドウで **保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-122">Update the necessary field information, and on the Action Pane, select **Save**.</span></span>  

## <a name="send-a-project-quotation-to-a-customer"></a><span data-ttu-id="fd31e-123">プロジェクトの見積を顧客に送信する</span><span class="sxs-lookup"><span data-stu-id="fd31e-123">Send a project quotation to a customer</span></span> 

1. <span data-ttu-id="fd31e-124">**プロジェクト管理と会計** > **見積書** > **プロジェクト見積**に移動し、送信するプロジェクトの見積を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-124">Go to **Project management and accounting** > **Quotations** > **Project quotations**, and select the project quotation that you want to send.</span></span>
2. <span data-ttu-id="fd31e-125">**見積**タブの **プロジェクト見積** ページで、**プロセス**グループにて、**見積書の送付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd31e-125">On the **Project quotations** page, on the **Quote** tab, in the **Process** group, select **Send quotation**.</span></span> <span data-ttu-id="fd31e-126">見積のステータスが**送信済**に更新されます。</span><span class="sxs-lookup"><span data-stu-id="fd31e-126">The quotation status updates to **Sent**.</span></span>

> [!NOTE]
> <span data-ttu-id="fd31e-127">ステータスを **送信済** に変更した後は、プロジェクトの見積を変更できません 。</span><span class="sxs-lookup"><span data-stu-id="fd31e-127">You can’t modify a project quotation after the status is changed to **Sent**.</span></span>
