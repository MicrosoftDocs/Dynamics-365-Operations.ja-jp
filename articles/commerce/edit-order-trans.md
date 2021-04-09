---
title: オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン注文トランザクションと非同期顧客注文トランザクションを編集および監査する方法について説明します。
author: josaw1
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5113f7ac0d308076ebaa9daeca0929eb537e94ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792684"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="a8d4b-103">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="a8d4b-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8d4b-104">このトピックでは、Microsoft Dynamics 365 Commerce でオンライン注文トランザクションと非同期顧客注文トランザクションを編集および監査する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a8d4b-105">概要</span><span class="sxs-lookup"><span data-stu-id="a8d4b-105">Overview</span></span>

<span data-ttu-id="a8d4b-106">Commerce バージョン 10.0.5 と 10.0.6 では、現金売りトランザクション (売上や返品など) と現金管理トランザクション (釣銭入力や支払/入金の削除など) の編集のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="a8d4b-107">Commerce バージョン 10.0.7 では、オンライン注文トランザクションと非同期顧客注文トランザクションの編集のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="a8d4b-108">注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="a8d4b-108">Edit and audit order transactions</span></span>

<span data-ttu-id="a8d4b-109">Commerce 本社でトランザクションの編集と監査を行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a8d4b-110">[Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="a8d4b-111">**小売パラメーター** ページの **顧客注文** タブの **注文** クイックタブで、**注文の同期エラーの保留コード** に保留コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="a8d4b-112">**店舗の財務** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="a8d4b-113">**オンライン注文の同期エラー** タイルと **顧客注文の同期エラー** タイルに、小売トランザクションの事前にフィルターされたビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="a8d4b-114">それぞれに、対応する注文タイプについて同期に失敗したトランザクション レコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="a8d4b-115">**オンライン注文の同期エラー** ページまたは **顧客注文の同期エラー** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="a8d4b-116">レコードを選択して、同期エラーの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="a8d4b-117">**同期の状態** クイック タブに、次のエラーの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="a8d4b-118">保留中の注文のステータス</span><span class="sxs-lookup"><span data-stu-id="a8d4b-118">Pending order status</span></span>
    - <span data-ttu-id="a8d4b-119">注文エラーの詳細</span><span class="sxs-lookup"><span data-stu-id="a8d4b-119">Order error details</span></span>
    - <span data-ttu-id="a8d4b-120">変更日時</span><span class="sxs-lookup"><span data-stu-id="a8d4b-120">Modified date and time</span></span>
    - <span data-ttu-id="a8d4b-121">再試行回数</span><span class="sxs-lookup"><span data-stu-id="a8d4b-121">Retry count</span></span>

1. <span data-ttu-id="a8d4b-122">エラーの詳細にレコードの修正が必要である旨が示された場合は、**Office アドイン**、**選択したトランザクションの編集** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="a8d4b-123">選択したトランザクションの詳細を示す Excel ファイルが開きます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="a8d4b-124">編集中のトランザクションがオンライン注文トランザクションの場合、Excel ファイルに次のワークシートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="a8d4b-125">**トランザクション** – このワークシートには、トランザクションのヘッダーに関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-126">**販売トランザクション** – このワークシートには、トランザクションの明細書に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-127">**支払トランザクション** – このワークシートには、トランザクションの支払行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-128">**割引トランザクション** – このワークシートには、トランザクションの割引に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-129">**税金トランザクション** – このワークシートには、トランザクションの税金に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-130">**諸費用トランザクション** – このワークシートには、トランザクションの諸費用に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="a8d4b-131">編集中のトランザクションが非同期顧客トランザクションの場合、Excel ファイルに次のワークシートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="a8d4b-132">**明細行** – このワークシートには、トランザクションのヘッダーと明細行に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-133">**支払** – このワークシートには、トランザクションの支払明細行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-134">**割引** – このワークシートには、トランザクションの割引に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-135">**税金** – このワークシートには、トランザクションの税金に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="a8d4b-136">**諸費用** – このワークシートには、トランザクションの諸費用に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="a8d4b-137">Excel ファイルの **保留中の注文のステータス** フィールドに **編集** と入力し、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="a8d4b-138">このようにして、バッチ モードで実行している **同期注文** ジョブが、処理中にこのレコードをスキップするのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="a8d4b-139">Excel ファイルで適切なフィールドを変更してから、Dynamics Excel アドインの公開機能を使用してデータをアップロードして Commerce 本社に戻します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="a8d4b-140">データの公開後、変更がシステムに反映されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="a8d4b-141">公開時には、ユーザーが行った変更に対する検証は行われません。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="a8d4b-142">変更の完全な監査証跡を表示するには、ヘッダーレベル変更用の **小売トランザクション** ヘッダー、および適切なトランザクション ページの該当するセクションやレコードにある **監査追跡の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="a8d4b-143">たとえば、販売明細行に関連するすべての変更は、**販売トランザクション** ページに表示され、支 に関連するすべての変更は、**支払トランザクション** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="a8d4b-144">変更については、次の監査の詳細が維持されます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="a8d4b-145">変更日時</span><span class="sxs-lookup"><span data-stu-id="a8d4b-145">Modified date and time</span></span>
    - <span data-ttu-id="a8d4b-146">フィールド</span><span class="sxs-lookup"><span data-stu-id="a8d4b-146">Field</span></span>
    - <span data-ttu-id="a8d4b-147">元の値</span><span class="sxs-lookup"><span data-stu-id="a8d4b-147">Old value</span></span>
    - <span data-ttu-id="a8d4b-148">新しい値</span><span class="sxs-lookup"><span data-stu-id="a8d4b-148">New value</span></span>
    - <span data-ttu-id="a8d4b-149">変更者</span><span class="sxs-lookup"><span data-stu-id="a8d4b-149">Modified by</span></span>

1. <span data-ttu-id="a8d4b-150">変更を作成して公開したら、**同期注文** を選択して同期プロセスを直ちに開始します。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="a8d4b-151">または、バッチ モードで実行中の同期プロセスがトランザクションを処理するまで待機することができます。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="a8d4b-152">既定では、注文が正常に同期された後、その注文は、Commerce パラメーターで定義されている保留コードに基づいて保留状態になります。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="a8d4b-153">フルフィルメントやその他の操作のために注文をさらに処理するには、保留された注文を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8d4b-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8d4b-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a8d4b-154">Additional resources</span></span>

[<span data-ttu-id="a8d4b-155">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="a8d4b-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="a8d4b-156">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="a8d4b-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="a8d4b-157">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="a8d4b-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="a8d4b-158">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="a8d4b-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]