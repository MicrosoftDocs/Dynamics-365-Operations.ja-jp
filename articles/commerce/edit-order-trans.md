---
title: オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査
description: このトピックでは、Microsoft Dynamics 365 Commerce でオンライン注文トランザクションと非同期顧客注文トランザクションを編集および監査する方法について説明します。
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 0fee5ef7ad61e9581e7b2797bb1bd26b1a48ddbd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5221777"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="6efeb-103">オンライン注文トランザクションと非同期顧客注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="6efeb-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6efeb-104">このトピックでは、Microsoft Dynamics 365 Commerce でオンライン注文トランザクションと非同期顧客注文トランザクションを編集および監査する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6efeb-105">概要</span><span class="sxs-lookup"><span data-stu-id="6efeb-105">Overview</span></span>

<span data-ttu-id="6efeb-106">Commerce バージョン 10.0.5 と 10.0.6 では、現金売りトランザクション (売上や返品など) と現金管理トランザクション (釣銭入力や支払/入金の削除など) の編集のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="6efeb-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="6efeb-107">Commerce バージョン 10.0.7 では、オンライン注文トランザクションと非同期顧客注文トランザクションの編集のサポートが追加されました。</span><span class="sxs-lookup"><span data-stu-id="6efeb-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="6efeb-108">注文トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="6efeb-108">Edit and audit order transactions</span></span>

<span data-ttu-id="6efeb-109">Commerce 本社でトランザクションの編集と監査を行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6efeb-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="6efeb-110">[Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="6efeb-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="6efeb-111">**小売パラメーター** ページの **顧客注文** タブの **注文** クイックタブで、**注文の同期エラーの保留コード** に保留コードを指定します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="6efeb-112">**店舗の財務** ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="6efeb-113">**オンライン注文の同期エラー** タイルと **顧客注文の同期エラー** タイルに、小売トランザクションの事前にフィルターされたビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="6efeb-114">それぞれに、対応する注文タイプについて同期に失敗したトランザクション レコードが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="6efeb-115">**オンライン注文の同期エラー** ページまたは **顧客注文の同期エラー** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="6efeb-116">レコードを選択して、同期エラーの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="6efeb-117">**同期の状態** クイック タブに、次のエラーの詳細が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="6efeb-118">保留中の注文のステータス</span><span class="sxs-lookup"><span data-stu-id="6efeb-118">Pending order status</span></span>
    - <span data-ttu-id="6efeb-119">注文エラーの詳細</span><span class="sxs-lookup"><span data-stu-id="6efeb-119">Order error details</span></span>
    - <span data-ttu-id="6efeb-120">変更日時</span><span class="sxs-lookup"><span data-stu-id="6efeb-120">Modified date and time</span></span>
    - <span data-ttu-id="6efeb-121">再試行回数</span><span class="sxs-lookup"><span data-stu-id="6efeb-121">Retry count</span></span>

1. <span data-ttu-id="6efeb-122">エラーの詳細にレコードの修正が必要である旨が示された場合は、**Office アドイン**、**選択したトランザクションの編集** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="6efeb-123">選択したトランザクションの詳細を示す Excel ファイルが開きます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="6efeb-124">編集中のトランザクションがオンライン注文トランザクションの場合、Excel ファイルに次のワークシートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="6efeb-125">**トランザクション** – このワークシートには、トランザクションのヘッダーに関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-126">**販売トランザクション** – このワークシートには、トランザクションの明細書に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-127">**支払トランザクション** – このワークシートには、トランザクションの支払行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="6efeb-128">**割引トランザクション** – このワークシートには、トランザクションの割引に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-129">**税金トランザクション** – このワークシートには、トランザクションの税金に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-130">**諸費用トランザクション** – このワークシートには、トランザクションの諸費用に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="6efeb-131">編集中のトランザクションが非同期顧客トランザクションの場合、Excel ファイルに次のワークシートが含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="6efeb-132">**明細行** – このワークシートには、トランザクションのヘッダーと明細行に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-133">**支払** – このワークシートには、トランザクションの支払明細行の詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="6efeb-134">**割引** – このワークシートには、トランザクションの割引に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-135">**税金** – このワークシートには、トランザクションの税金に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="6efeb-136">**諸費用** – このワークシートには、トランザクションの諸費用に関する詳細が含まれます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="6efeb-137">Excel ファイルの **保留中の注文のステータス** フィールドに **編集** と入力し、変更を公開します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="6efeb-138">このようにして、バッチ モードで実行している **同期注文** ジョブが、処理中にこのレコードをスキップするのを防ぐことができます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="6efeb-139">Excel ファイルで適切なフィールドを変更してから、Dynamics Excel アドインの公開機能を使用してデータをアップロードして Commerce 本社に戻します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="6efeb-140">データの公開後、変更がシステムに反映されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="6efeb-141">公開時には、ユーザーが行った変更に対する検証は行われません。</span><span class="sxs-lookup"><span data-stu-id="6efeb-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="6efeb-142">変更の完全な監査証跡を表示するには、ヘッダーレベル変更用の **小売トランザクション** ヘッダー、および適切なトランザクション ページの該当するセクションやレコードにある **監査追跡の表示** を選択します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="6efeb-143">たとえば、販売明細行に関連するすべての変更は、**販売トランザクション** ページに表示され、支 に関連するすべての変更は、**支払トランザクション** ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="6efeb-144">変更については、次の監査の詳細が維持されます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="6efeb-145">変更日時</span><span class="sxs-lookup"><span data-stu-id="6efeb-145">Modified date and time</span></span>
    - <span data-ttu-id="6efeb-146">フィールド</span><span class="sxs-lookup"><span data-stu-id="6efeb-146">Field</span></span>
    - <span data-ttu-id="6efeb-147">元の値</span><span class="sxs-lookup"><span data-stu-id="6efeb-147">Old value</span></span>
    - <span data-ttu-id="6efeb-148">新しい値</span><span class="sxs-lookup"><span data-stu-id="6efeb-148">New value</span></span>
    - <span data-ttu-id="6efeb-149">変更者</span><span class="sxs-lookup"><span data-stu-id="6efeb-149">Modified by</span></span>

1. <span data-ttu-id="6efeb-150">変更を作成して公開したら、**同期注文** を選択して同期プロセスを直ちに開始します。</span><span class="sxs-lookup"><span data-stu-id="6efeb-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="6efeb-151">または、バッチ モードで実行中の同期プロセスがトランザクションを処理するまで待機することができます。</span><span class="sxs-lookup"><span data-stu-id="6efeb-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="6efeb-152">既定では、注文が正常に同期された後、その注文は、Commerce パラメーターで定義されている保留コードに基づいて保留状態になります。</span><span class="sxs-lookup"><span data-stu-id="6efeb-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="6efeb-153">フルフィルメントやその他の操作のために注文をさらに処理するには、保留された注文を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6efeb-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6efeb-154">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6efeb-154">Additional resources</span></span>

[<span data-ttu-id="6efeb-155">現金売りトランザクションと現金管理トランザクションの編集と監査</span><span class="sxs-lookup"><span data-stu-id="6efeb-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="6efeb-156">小売トランザクションの財務分析コードの編集</span><span class="sxs-lookup"><span data-stu-id="6efeb-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="6efeb-157">小売トランザクションを編集するために Excel ブックを作成する</span><span class="sxs-lookup"><span data-stu-id="6efeb-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="6efeb-158">小売トランザクションを編集するために Excel ブックにフィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="6efeb-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]