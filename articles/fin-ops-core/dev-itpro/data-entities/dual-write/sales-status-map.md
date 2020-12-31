---
title: 販売注文状態フィールドのマッピングの設定
description: このトピックでは、販売注文の状態フィールドを二重書き込み用に設定する方法について説明します。
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4454577"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a><span data-ttu-id="d235f-103">販売注文状態フィールドのマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="d235f-103">Set up the mapping for the sales order status fields</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d235f-104">販売注文の状態を示すフィールドは、Microsoft Dynamics 365 Supply Chain Management と Dynamics 365 Sales で異なる列挙値を持っています。</span><span class="sxs-lookup"><span data-stu-id="d235f-104">The fields that indicate sales order status have different enumeration values in Microsoft Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="d235f-105">これらのフィールドを二重書き込みでマップするには、追加の設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="d235f-105">Additional setup is required to map these fields in dual-write.</span></span>

## <a name="fields-in-supply-chain-management"></a><span data-ttu-id="d235f-106">Supply Chain Management のフィールド</span><span class="sxs-lookup"><span data-stu-id="d235f-106">Fields in Supply Chain Management</span></span>

<span data-ttu-id="d235f-107">Supply Chain Management では、2 つのフィールドが販売注文の状態を反映します。</span><span class="sxs-lookup"><span data-stu-id="d235f-107">In Supply Chain Management, two fields reflect the status of the sales order.</span></span> <span data-ttu-id="d235f-108">マップする必要があるフィールドは **状態** と **ドキュメントの状態** です。</span><span class="sxs-lookup"><span data-stu-id="d235f-108">The fields that you must map are **Status** and **Document Status**.</span></span>

<span data-ttu-id="d235f-109">**状態** 列挙型では、注文の全体的な状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="d235f-109">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="d235f-110">この状態は、注文ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d235f-110">This status is shown on the order header.</span></span>

<span data-ttu-id="d235f-111">**状態** 列挙型の値は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="d235f-111">The **Status** enumeration has the following values:</span></span>

- <span data-ttu-id="d235f-112">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-112">Open Order</span></span>
- <span data-ttu-id="d235f-113">配送済</span><span class="sxs-lookup"><span data-stu-id="d235f-113">Delivered</span></span>
- <span data-ttu-id="d235f-114">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-114">Invoiced</span></span>
- <span data-ttu-id="d235f-115">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-115">Cancelled</span></span>

<span data-ttu-id="d235f-116">**ドキュメントの状態** 列挙型は、注文に対して生成された最新のドキュメントを指定します。</span><span class="sxs-lookup"><span data-stu-id="d235f-116">The **Document Status** enumeration specifies the most recent document that was generated for the order.</span></span> <span data-ttu-id="d235f-117">たとえば、注文が確定された場合、このドキュメントは販売注文の確認書になります。</span><span class="sxs-lookup"><span data-stu-id="d235f-117">For example, if the order is confirmed, this document is a sales order confirmation.</span></span> <span data-ttu-id="d235f-118">販売注文が部分的に請求され、残りの明細行が確認された場合、プロセスの後で請求書が生成されるため、ドキュメントの状態は **請求書** のままになります。</span><span class="sxs-lookup"><span data-stu-id="d235f-118">If a sales order is partially invoiced, and then the remaining line is confirmed, the document status remains **Invoice**, because the invoice is generated later in the process.</span></span>

<span data-ttu-id="d235f-119">**ドキュメントの状態** 列挙型の値は次のとおりです:</span><span class="sxs-lookup"><span data-stu-id="d235f-119">The **Document Status** enumeration has the following values:</span></span>

- <span data-ttu-id="d235f-120">確認書</span><span class="sxs-lookup"><span data-stu-id="d235f-120">Confirmation</span></span>
- <span data-ttu-id="d235f-121">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="d235f-121">Picking List</span></span>
- <span data-ttu-id="d235f-122">梱包明細</span><span class="sxs-lookup"><span data-stu-id="d235f-122">Packing Slip</span></span>
- <span data-ttu-id="d235f-123">請求書</span><span class="sxs-lookup"><span data-stu-id="d235f-123">Invoice</span></span>

## <a name="fields-in-sales"></a><span data-ttu-id="d235f-124">Sales のフィールド</span><span class="sxs-lookup"><span data-stu-id="d235f-124">Fields in Sales</span></span>

<span data-ttu-id="d235f-125">Sales では、2 つのフィールドが注文の状態を示します。</span><span class="sxs-lookup"><span data-stu-id="d235f-125">In Sales, two fields indicate the status of the order.</span></span> <span data-ttu-id="d235f-126">マップする必要があるフィールドは **状態** と **処理状態** です。</span><span class="sxs-lookup"><span data-stu-id="d235f-126">The fields that you must map are **Status** and **Processing Status**.</span></span>

<span data-ttu-id="d235f-127">**状態** 列挙型では、注文の全体的な状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="d235f-127">The **Status** enumeration specifies the overall status of the order.</span></span> <span data-ttu-id="d235f-128">次の値があります:</span><span class="sxs-lookup"><span data-stu-id="d235f-128">It has the following values:</span></span>

- <span data-ttu-id="d235f-129">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-129">Active</span></span>
- <span data-ttu-id="d235f-130">提出済</span><span class="sxs-lookup"><span data-stu-id="d235f-130">Submitted</span></span>
- <span data-ttu-id="d235f-131">履行済</span><span class="sxs-lookup"><span data-stu-id="d235f-131">Fulfilled</span></span>
- <span data-ttu-id="d235f-132">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-132">Invoiced</span></span>
- <span data-ttu-id="d235f-133">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-133">Cancelled</span></span>

<span data-ttu-id="d235f-134">**処理状態** 列挙型は、状態をより正確に Supply Chain Management でマップできるように導入されました。</span><span class="sxs-lookup"><span data-stu-id="d235f-134">The **Processing Status** enumeration was introduced so that the status can be mapped more accurately with Supply Chain Management.</span></span>

<span data-ttu-id="d235f-135">次の表に、Supply Chain Management における **処理状態** のマッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="d235f-135">The following table shows the mapping of **Processing Status** in Supply Chain Management.</span></span>

| <span data-ttu-id="d235f-136">処理状態</span><span class="sxs-lookup"><span data-stu-id="d235f-136">Processing Status</span></span>   | <span data-ttu-id="d235f-137">Supply Chain Management の状態</span><span class="sxs-lookup"><span data-stu-id="d235f-137">Status in Supply Chain Management</span></span> | <span data-ttu-id="d235f-138">Supply Chain Management におけるドキュメントの状態</span><span class="sxs-lookup"><span data-stu-id="d235f-138">Document Status in Supply Chain Management</span></span> |
|---------------------|-----------------------------------|--------------------------------------------|
| <span data-ttu-id="d235f-139">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-139">Active</span></span>              | <span data-ttu-id="d235f-140">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-140">Open Order</span></span>                        | <span data-ttu-id="d235f-141">None</span><span class="sxs-lookup"><span data-stu-id="d235f-141">None</span></span>                                       |
| <span data-ttu-id="d235f-142">確定済</span><span class="sxs-lookup"><span data-stu-id="d235f-142">Confirmed</span></span>           | <span data-ttu-id="d235f-143">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-143">Open Order</span></span>                        | <span data-ttu-id="d235f-144">確認書</span><span class="sxs-lookup"><span data-stu-id="d235f-144">Confirmation</span></span>                               |
| <span data-ttu-id="d235f-145">ピッキング済</span><span class="sxs-lookup"><span data-stu-id="d235f-145">Picked</span></span>              | <span data-ttu-id="d235f-146">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-146">Open Order</span></span>                        | <span data-ttu-id="d235f-147">ピッキング リスト</span><span class="sxs-lookup"><span data-stu-id="d235f-147">Picking List</span></span>                               |
| <span data-ttu-id="d235f-148">一部出荷済</span><span class="sxs-lookup"><span data-stu-id="d235f-148">Partially Delivered</span></span> | <span data-ttu-id="d235f-149">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-149">Open Order</span></span>                        | <span data-ttu-id="d235f-150">梱包明細</span><span class="sxs-lookup"><span data-stu-id="d235f-150">Packing Slip</span></span>                               |
| <span data-ttu-id="d235f-151">配送済</span><span class="sxs-lookup"><span data-stu-id="d235f-151">Delivered</span></span>           | <span data-ttu-id="d235f-152">配送済</span><span class="sxs-lookup"><span data-stu-id="d235f-152">Delivered</span></span>                         | <span data-ttu-id="d235f-153">梱包明細</span><span class="sxs-lookup"><span data-stu-id="d235f-153">Packing Slip</span></span>                               |
| <span data-ttu-id="d235f-154">一部請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-154">Partially Invoiced</span></span>  | <span data-ttu-id="d235f-155">配送済</span><span class="sxs-lookup"><span data-stu-id="d235f-155">Delivered</span></span>                         | <span data-ttu-id="d235f-156">請求書</span><span class="sxs-lookup"><span data-stu-id="d235f-156">Invoice</span></span>                                    |
| <span data-ttu-id="d235f-157">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-157">Invoiced</span></span>            | <span data-ttu-id="d235f-158">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-158">Invoiced</span></span>                          | <span data-ttu-id="d235f-159">請求書</span><span class="sxs-lookup"><span data-stu-id="d235f-159">Invoice</span></span>                                    |
| <span data-ttu-id="d235f-160">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-160">Cancelled</span></span>           | <span data-ttu-id="d235f-161">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-161">Cancelled</span></span>                         | <span data-ttu-id="d235f-162">適用できません</span><span class="sxs-lookup"><span data-stu-id="d235f-162">Not applicable</span></span>                             |

<span data-ttu-id="d235f-163">次の表に、Sales と Supply Chain Management 間の **処理状態** のマッピングを示します。</span><span class="sxs-lookup"><span data-stu-id="d235f-163">The following table shows the mapping of **Processing Status** between Sales and Supply Chain Management.</span></span>

| <span data-ttu-id="d235f-164">処理状態</span><span class="sxs-lookup"><span data-stu-id="d235f-164">Processing Status</span></span>   | <span data-ttu-id="d235f-165">Sales の状態</span><span class="sxs-lookup"><span data-stu-id="d235f-165">Status in Sales</span></span> | <span data-ttu-id="d235f-166">Supply Chain Management の状態</span><span class="sxs-lookup"><span data-stu-id="d235f-166">Status in Supply Chain Management</span></span> |
|---------------------|-----------------|-----------------------------------|
| <span data-ttu-id="d235f-167">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-167">Active</span></span>              | <span data-ttu-id="d235f-168">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-168">Active</span></span>          | <span data-ttu-id="d235f-169">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-169">Open Order</span></span>                        |
| <span data-ttu-id="d235f-170">確定済</span><span class="sxs-lookup"><span data-stu-id="d235f-170">Confirmed</span></span>           | <span data-ttu-id="d235f-171">提出済</span><span class="sxs-lookup"><span data-stu-id="d235f-171">Submitted</span></span>       | <span data-ttu-id="d235f-172">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-172">Open Order</span></span>                        |
| <span data-ttu-id="d235f-173">ピッキング済</span><span class="sxs-lookup"><span data-stu-id="d235f-173">Picked</span></span>              | <span data-ttu-id="d235f-174">提出済</span><span class="sxs-lookup"><span data-stu-id="d235f-174">Submitted</span></span>       | <span data-ttu-id="d235f-175">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-175">Open Order</span></span>                        |
| <span data-ttu-id="d235f-176">一部出荷済</span><span class="sxs-lookup"><span data-stu-id="d235f-176">Partially Delivered</span></span> | <span data-ttu-id="d235f-177">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-177">Active</span></span>          | <span data-ttu-id="d235f-178">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-178">Open Order</span></span>                        |
| <span data-ttu-id="d235f-179">一部請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-179">Partially Invoiced</span></span>  | <span data-ttu-id="d235f-180">使用可能</span><span class="sxs-lookup"><span data-stu-id="d235f-180">Active</span></span>          | <span data-ttu-id="d235f-181">オープン注文</span><span class="sxs-lookup"><span data-stu-id="d235f-181">Open Order</span></span>                        |
| <span data-ttu-id="d235f-182">一部請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-182">Partially Invoiced</span></span>  | <span data-ttu-id="d235f-183">履行済</span><span class="sxs-lookup"><span data-stu-id="d235f-183">Fulfilled</span></span>       | <span data-ttu-id="d235f-184">配送済</span><span class="sxs-lookup"><span data-stu-id="d235f-184">Delivered</span></span>                         |
| <span data-ttu-id="d235f-185">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-185">Invoiced</span></span>            | <span data-ttu-id="d235f-186">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-186">Invoiced</span></span>        | <span data-ttu-id="d235f-187">請求済</span><span class="sxs-lookup"><span data-stu-id="d235f-187">Invoiced</span></span>                          |
| <span data-ttu-id="d235f-188">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-188">Cancelled</span></span>           | <span data-ttu-id="d235f-189">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-189">Cancelled</span></span>       | <span data-ttu-id="d235f-190">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="d235f-190">Cancelled</span></span>                         |

## <a name="setup"></a><span data-ttu-id="d235f-191">段取り</span><span class="sxs-lookup"><span data-stu-id="d235f-191">Setup</span></span>

<span data-ttu-id="d235f-192">販売注文状態フィールドのマッピングを設定するには、**IsSOPIntegrationEnabled** と **isIntegrationUser** 属性を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d235f-192">To set up the mapping for the sales order status fields, you must enable the **IsSOPIntegrationEnabled** and **isIntegrationUser** attributes.</span></span>

<span data-ttu-id="d235f-193">**IsSOPIntegrationEnabled** 属性を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d235f-193">To enable the **IsSOPIntegrationEnabled** attribute, follow these steps.</span></span>

1. <span data-ttu-id="d235f-194">ブラウザーで `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations` に移動します。</span><span class="sxs-lookup"><span data-stu-id="d235f-194">In a browser, go to `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`.</span></span> <span data-ttu-id="d235f-195">**\<test-name\>** を会社の Sales リンクに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d235f-195">Replace **\<test-name\>** with your company's link to Sales.</span></span>
2. <span data-ttu-id="d235f-196">開いたページで、**organizationid** を検索し、値をメモします。</span><span class="sxs-lookup"><span data-stu-id="d235f-196">On the page that is opened, find **organizationid**, and make a note of the value.</span></span>

    ![organizationid の検索](media/sales-map-orgid.png)

3. <span data-ttu-id="d235f-198">Sales では、ブラウザー コンソールを開き、次のスクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="d235f-198">In Sales, open the browser console, and run following script.</span></span> <span data-ttu-id="d235f-199">手順 2 の **organizationid** 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d235f-199">Use the **organizationid** value from step 2.</span></span>

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![ブラウザー コンソールの JavaScript コード](media/sales-map-script.png)

4. <span data-ttu-id="d235f-201">**IsSOPIntegrationEnabled** が **true** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d235f-201">Verify that **IsSOPIntegrationEnabled** is set to **true**.</span></span> <span data-ttu-id="d235f-202">手順 1 の URL を使用して、値を確認します。</span><span class="sxs-lookup"><span data-stu-id="d235f-202">Use the URL from step 1 to check the value.</span></span>

    ![IsSOPIntegrationEnabled を true に設定](media/sales-map-integration-enabled.png)

<span data-ttu-id="d235f-204">**isIntegrationUser** 属性を有効にするには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="d235f-204">To enable the **isIntegrationUser** attribute, follow these steps.</span></span>

1. <span data-ttu-id="d235f-205">Sales では **設定 \> カスタマイズ \> システムのカスタマイズ** に移動し、**ユーザー エンティティ** を選択して、**フォーム \> ユーザー** を開きます。</span><span class="sxs-lookup"><span data-stu-id="d235f-205">In Sales, go to **Setting \> Customization \> Customize the System**, select **User entity**, and then open **Form \> User**.</span></span>

    ![ユーザー フォームを開く](media/sales-map-user.png)

2. <span data-ttu-id="d235f-207">フィールド エクスプローラーで **統合ユーザーモード** を検索し、それをダブルクリックして、フォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="d235f-207">In Field Explorer, find **Integration user mode**, and double-click it to add it to the form.</span></span> <span data-ttu-id="d235f-208">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="d235f-208">Save your change.</span></span>

    ![統合ユーザーモード フィールドのフォームへの追加](media/sales-map-field-explorer.png)

3. <span data-ttu-id="d235f-210">Sales では、**設定 \> セキュリティ \> ユーザー** に移動し、表示を **有効なユーザー** から **アプリケーション ユーザー** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d235f-210">In Sales, go to **Setting \> Security \> Users**, and change the view from **Enabled Users** to **Application Users**.</span></span>

    ![表示を有効なユーザーからアプリケーション ユーザーに変更](media/sales-map-enabled-users.png)

4. <span data-ttu-id="d235f-212">**DualWrite IntegrationUser** の 2 つのエントリを選択します。</span><span class="sxs-lookup"><span data-stu-id="d235f-212">Select the two entries for **DualWrite IntegrationUser**.</span></span>

    ![アプリケーション ユーザーの一覧](media/sales-map-user-mode.png)

5. <span data-ttu-id="d235f-214">**統合ユーザー モード** フィールド値を **はい** に変更します。</span><span class="sxs-lookup"><span data-stu-id="d235f-214">Change the value of the **Integration user mode** field to **Yes**.</span></span>

    ![統合ユーザー モード フィールド値の変更](media/sales-map-user-mode-yes.png)

<span data-ttu-id="d235f-216">これで、販売注文がマップされました。</span><span class="sxs-lookup"><span data-stu-id="d235f-216">Your sales orders are now mapped.</span></span>
