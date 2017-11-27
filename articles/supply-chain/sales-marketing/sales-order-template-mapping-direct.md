---
title: "販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期"
description: "このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="df8a8-103">販売注文ヘッダーおよび明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="df8a8-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="df8a8-104">このトピックでは、Microsoft Dynamics 365 for Finance and Operations, Enterprise edition から Microsoft Dynamics 365 for Sales に対して、販売注文ヘッダーと明細行を直接同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="df8a8-105">見込み客の現金化へのデータフロー</span><span class="sxs-lookup"><span data-stu-id="df8a8-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="df8a8-106">見込み客の現金化ソリューションは、Finance and Operations と Sales のインスタンス間でデータを同期するため、データの統合機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="df8a8-107">データ統合機能で利用可能な見込み顧客を現金化するテンプレートは、Finance and Operations と Sales 間での勘定、連絡先、製品および販売見積、販売注文、および売上請求書データの流れを可能にします。</span><span class="sxs-lookup"><span data-stu-id="df8a8-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="df8a8-108">次の図は、Finance and Operations と Sales の間でデータを同期させる方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="df8a8-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="df8a8-109">[![見込み客の現金化へのデータフロー](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="df8a8-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="df8a8-110">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="df8a8-110">Templates and tasks</span></span>

<span data-ttu-id="df8a8-111">利用可能なテンプレートにアクセスするには、[PowerApps 管理者センター](https://preview.admin.powerapps.com/dataintegration) を開きます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="df8a8-112">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="df8a8-113">Finance and Operations から Sales への販売注文ヘッダーと明細行の同期には、以下のテンプレートと基本的なタスクが使用されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="df8a8-114">**データ統合における テンプレートの名前** 販売注文 (Sales から Finance and Operations )- 直接</span><span class="sxs-lookup"><span data-stu-id="df8a8-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="df8a8-115">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="df8a8-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="df8a8-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="df8a8-116">OrderHeader</span></span>
    - <span data-ttu-id="df8a8-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="df8a8-117">OrderLine</span></span>

<span data-ttu-id="df8a8-118">販売請求書ヘッダーと明細行を同期させるには、次の同期タスクが必要です。</span><span class="sxs-lookup"><span data-stu-id="df8a8-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="df8a8-119">製品 (Finance and Operations から Sales) - 直接</span><span class="sxs-lookup"><span data-stu-id="df8a8-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="df8a8-120">勘定 (Sales から Finance and Operations) - 直接(使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="df8a8-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="df8a8-121">顧客への連絡先 (Sales から Finance and Operations) - ダイレクト (使用されている場合)</span><span class="sxs-lookup"><span data-stu-id="df8a8-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="df8a8-122">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="df8a8-122">Entity set</span></span>

| <span data-ttu-id="df8a8-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="df8a8-123">Finance and Operations</span></span>  | <span data-ttu-id="df8a8-124">売上</span><span class="sxs-lookup"><span data-stu-id="df8a8-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="df8a8-125">CDS 販売注文ヘッダー</span><span class="sxs-lookup"><span data-stu-id="df8a8-125">CDS sales order headers</span></span> | <span data-ttu-id="df8a8-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="df8a8-126">SalesOrders</span></span>       |
| <span data-ttu-id="df8a8-127">CDS 販売注文明細行</span><span class="sxs-lookup"><span data-stu-id="df8a8-127">CDS sales order lines</span></span>   | <span data-ttu-id="df8a8-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="df8a8-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="df8a8-129">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="df8a8-129">Entity flow</span></span>

<span data-ttu-id="df8a8-130">販売注文が Finance and Operations で作成され Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="df8a8-131">テンプレートのフィルタは、関連する受注のみが同期に含まれることを保証します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="df8a8-132">受注では、Sales から生成される発注元の顧客と販売担当者の両方が同期に含まれます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="df8a8-133">Finance and Operations で、[**OrderingCustomerIsExternallyMaintained**] および [**InvoiceCustomerIsExternallyMaintained**] フィールドは、データ エンティティの同期を追跡するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="df8a8-134">Finance and Operations で [販売注文] を確定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8a8-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="df8a8-135">[**出荷済**] や [**請求済**] など、確認済の販売注文または処理ステータスの高い販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="df8a8-136">販売注文を作成または変更した後、Finance and Operations で [**販売合計の計算**] のバッチ ジョブを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8a8-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="df8a8-137">販売合計が計算された販売注文のみが Sales に同期されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="df8a8-138">現在、販売注文ヘッダの料金に関連する税金は、Finance and Operations から Sales までの同期には含まれていません。</span><span class="sxs-lookup"><span data-stu-id="df8a8-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="df8a8-139">これは Sales がヘッダー レベルでの税金情報をサポートしていないためです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="df8a8-140">ただし、同期の明細行レベルでの税に関連する費用が含まれます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="df8a8-141">売上の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="df8a8-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="df8a8-142">新しいフィールドが [**注文**] エンティティに追加され、ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="df8a8-143">[**外部で管理**] - 注文が Finance and Operations から来る場合、このオプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="df8a8-144">[**処理状態**] - このフィールドには、Finance and Operations の注文の処理状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="df8a8-145">使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-145">The following values are available:</span></span>

    - <span data-ttu-id="df8a8-146">使用可能</span><span class="sxs-lookup"><span data-stu-id="df8a8-146">Active</span></span>
    - <span data-ttu-id="df8a8-147">確認済</span><span class="sxs-lookup"><span data-stu-id="df8a8-147">Confirmed</span></span>
    - <span data-ttu-id="df8a8-148">梱包明細</span><span class="sxs-lookup"><span data-stu-id="df8a8-148">Packing Slip</span></span>
    - <span data-ttu-id="df8a8-149">請求済</span><span class="sxs-lookup"><span data-stu-id="df8a8-149">Invoiced</span></span>
    - <span data-ttu-id="df8a8-150">ピッキング済</span><span class="sxs-lookup"><span data-stu-id="df8a8-150">Picked</span></span>
    - <span data-ttu-id="df8a8-151">一部ピック済</span><span class="sxs-lookup"><span data-stu-id="df8a8-151">Partially Picked</span></span>
    - <span data-ttu-id="df8a8-152">一部ピック済</span><span class="sxs-lookup"><span data-stu-id="df8a8-152">Partially Packed</span></span>
    - <span data-ttu-id="df8a8-153">出荷済</span><span class="sxs-lookup"><span data-stu-id="df8a8-153">Shipped</span></span>
    - <span data-ttu-id="df8a8-154">一部出荷済</span><span class="sxs-lookup"><span data-stu-id="df8a8-154">Partially Shipped</span></span>
    - <span data-ttu-id="df8a8-155">一部請求済</span><span class="sxs-lookup"><span data-stu-id="df8a8-155">Partially Invoiced</span></span>
    - <span data-ttu-id="df8a8-156">キャンセル済</span><span class="sxs-lookup"><span data-stu-id="df8a8-156">Cancelled</span></span>

<span data-ttu-id="df8a8-157">[外部で管理される製品のみ] 設定は、別の販売注文のシナリオ (例えば、Sales から Finance and Operation への同期) で使用され、販売注文が完全に外部管理製品から構成されているかどうか一貫して追跡されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="df8a8-158">受注が外部から管理された製品で完全に構成されている場合、製品は Finance and Operations で管理されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="df8a8-159">この設定は、Finance and Operations に不明な製品を含む受注明細行を同期させないことを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="df8a8-160">[**販売注文**] ページで、[**請求書の作成**]、[**注文のキャンセル**]、[**再計算**]、[**製品の取得**] および [**ルックアップ アドレス**] ボタンは外部で管理される注文用に非表示となります。それは Finance and Operations で請求書が作成され Sales に同期されるためです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="df8a8-161">注文ページは編集できません。販売注文情報は Finance and Operations から同期されるためです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="df8a8-162">受注状況は、Finance and Operations からの変更が Sales の受注に流れることを保証するために、**有効**のままになります。</span><span class="sxs-lookup"><span data-stu-id="df8a8-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="df8a8-163">この動作を制御するためには、データ統合プロジェクトで、既定の [**Statecode\[状態\]**] を [**有効**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="df8a8-164">前提条件とマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="df8a8-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="df8a8-165">販売注文を同期する前に、システムで以下の設定を更新することが重要です。</span><span class="sxs-lookup"><span data-stu-id="df8a8-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="df8a8-166">Sales での設定</span><span class="sxs-lookup"><span data-stu-id="df8a8-166">Setup in Sales</span></span>

- <span data-ttu-id="df8a8-167">Sales で設定された接続のユーザーが割り当てられているチームのアクセス許可として設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="df8a8-168">デモデータを使用している場合、通常、ユーザーは管理者権限を持っていますが、チームには管理者権限がありません。</span><span class="sxs-lookup"><span data-stu-id="df8a8-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="df8a8-169">チームがデータ統合からプロジェクトを実行するとき、管理者権限がない場合、主要なチームがないというエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="df8a8-170">**設定** > **セキュリティ** > **チーム**で、関連チームを選択し、**ロール管理**をクリックして**システム管理者**などの必要なアクセス許可を持つロールを選択します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="df8a8-171">**設定** > **管理** > **システムの設定** > **Sales**の順にクリックし、次の設定を使用することを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="df8a8-172">[**システム プライジング計算システムの使用**] オプションが、[**はい**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="df8a8-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="df8a8-173">[**割引の計算方法**] フィールドが、[**明細行品目**] に設定されている。</span><span class="sxs-lookup"><span data-stu-id="df8a8-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="df8a8-174">Finance and Operations での設定</span><span class="sxs-lookup"><span data-stu-id="df8a8-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="df8a8-175">**販売およびマーケティング** > **定期処理タスク** > **販売合計を計算する**の順にクリックし、バッチ ジョブとして実行されるようにタスクを設定します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="df8a8-176">**販売注文合計を計算する**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="df8a8-177">販売合計が計算された販売注文のみが Sales に同期されるため、このステップは重要です。</span><span class="sxs-lookup"><span data-stu-id="df8a8-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="df8a8-178">バッチジョブの頻度は、販売注文同期の頻度と一致させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8a8-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="df8a8-179">データ統合プロジェクトでの設定</span><span class="sxs-lookup"><span data-stu-id="df8a8-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="df8a8-180">SalesHeader タスク</span><span class="sxs-lookup"><span data-stu-id="df8a8-180">SalesHeader task</span></span>

- <span data-ttu-id="df8a8-181">必要なマッピングが **InvoiceCountryRegionId** から **BillingAddress\_Country** に、また **DeliveryCountryRegionId** から **DeliveryAddress\_Country** に存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="df8a8-182">テンプレートの値は、複数の国または地域がマップされている値マップです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="df8a8-183">価格リストは、Sales で注文を作成するために必要です。</span><span class="sxs-lookup"><span data-stu-id="df8a8-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="df8a8-184">Sales で通貨ごとに使用される価格リストへの [**pricelevelid.name \[価格リスト名\]**] の値マップを更新します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="df8a8-185">1つの通貨に対する既定の価格リストを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="df8a8-186">または、複数の通貨で価格リストがある場合、値マップを使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="df8a8-187">**pricelevelid.name \[価格リスト名\]** の既定テンプレート値は **CRM サービス USA (サンプル)** です。</span><span class="sxs-lookup"><span data-stu-id="df8a8-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="df8a8-188">SalesLine タスク</span><span class="sxs-lookup"><span data-stu-id="df8a8-188">SalesLine task</span></span>

- <span data-ttu-id="df8a8-189">**DeliveryCountryRegionId** から **DeliveryAddress\_Country** に必要なマッピングが存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="df8a8-190">テンプレートの値は、複数の国または地域がマップされている値マップです。</span><span class="sxs-lookup"><span data-stu-id="df8a8-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="df8a8-191">Finance and Operation で [**SalesUnitSymbol**] 用の必要な値マップを確認します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="df8a8-192">[**SalesUnitSymbol**] から [**Quantity\_** UMO] に対して値マップを持つテンプレート値が定義されます。</span><span class="sxs-lookup"><span data-stu-id="df8a8-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="df8a8-193">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="df8a8-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="df8a8-194">[**支払条件**]、[**運賃条件**]、[**配送条件**]、[**送付方法**]、および [**配送モード**] フィールドは、既定のマッピングには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="df8a8-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="df8a8-195">これらのフィールドをマップするには、エンティティ間で同期される組織内のデータに固有の値マッピングを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8a8-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="df8a8-196">次の図は、データ統合のテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="df8a8-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="df8a8-197">マッピングは、Sales から Finance and Operations にどのフィールド情報を同期するかを表示します。</span><span class="sxs-lookup"><span data-stu-id="df8a8-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="df8a8-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="df8a8-198">OrderHeader</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="df8a8-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="df8a8-200">OrderLine</span></span>

![データ インテグレーターのテンプレートのマッピング](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="df8a8-202">関連トピック</span><span class="sxs-lookup"><span data-stu-id="df8a8-202">Related topics</span></span>

[<span data-ttu-id="df8a8-203">見込顧客を現金化</span><span class="sxs-lookup"><span data-stu-id="df8a8-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="df8a8-204">Sales から Finance and Operations の顧客への勘定の直接同期</span><span class="sxs-lookup"><span data-stu-id="df8a8-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="df8a8-205">Sales 製品への Finance and Operations 製品の直接同期</span><span class="sxs-lookup"><span data-stu-id="df8a8-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="df8a8-206">Sales から Finance and Operations の連絡先または顧客への連絡先の直接同期</span><span class="sxs-lookup"><span data-stu-id="df8a8-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="df8a8-207">売上請求書ヘッダーおよび直接明細行の Finance and Operations から Sales への直接同期</span><span class="sxs-lookup"><span data-stu-id="df8a8-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




