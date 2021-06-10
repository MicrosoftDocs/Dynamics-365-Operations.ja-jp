---
title: Field Service の契約の請求書と Supply Chain Management の自由書式の請求書との同期
description: このトピックでは、Dynamics 365 Field Service の契約請求書を Dynamics 365 Supply Chain Management の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102737"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="c0136-103">Field Service の契約の請求書と Supply Chain Management の自由書式の請求書との同期</span><span class="sxs-lookup"><span data-stu-id="c0136-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c0136-104">このトピックでは、Dynamics 365 Field Service の契約請求書を Dynamics 365 Supply Chain Management の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="c0136-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="c0136-105">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="c0136-105">Templates and tasks</span></span>

<span data-ttu-id="c0136-106">次のテンプレートと基本的なタスクは、Field Service の契約請求書と Supply Chain Management の自由書式の請求書との同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="c0136-107">**データ統合でのテンプレートの名前**</span><span class="sxs-lookup"><span data-stu-id="c0136-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="c0136-108">契約請求書 (Field Service から Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="c0136-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="c0136-109">**データ統合プロジェクトのタスク名**</span><span class="sxs-lookup"><span data-stu-id="c0136-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="c0136-110">請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c0136-110">Invoice headers</span></span>
- <span data-ttu-id="c0136-111">請求明細行</span><span class="sxs-lookup"><span data-stu-id="c0136-111">Invoice lines</span></span>

<span data-ttu-id="c0136-112">契約請求書の同期が処理される前に、次の同期が必要です。</span><span class="sxs-lookup"><span data-stu-id="c0136-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="c0136-113">アカウント (Sales から Supply Chain Management) - 直接</span><span class="sxs-lookup"><span data-stu-id="c0136-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="c0136-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="c0136-114">Entity set</span></span>

| <span data-ttu-id="c0136-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="c0136-115">Field Service</span></span>  | <span data-ttu-id="c0136-116">サプライ チェーン マネジメント</span><span class="sxs-lookup"><span data-stu-id="c0136-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="c0136-117">請求書</span><span class="sxs-lookup"><span data-stu-id="c0136-117">invoices</span></span>       | <span data-ttu-id="c0136-118">Dataverse 顧客の自由書式請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c0136-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="c0136-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="c0136-119">invoicedetails</span></span> | <span data-ttu-id="c0136-120">Dataverse 顧客の自由書式請求書明細行</span><span class="sxs-lookup"><span data-stu-id="c0136-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="c0136-121">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="c0136-121">Entity flow</span></span>

<span data-ttu-id="c0136-122">Field Service の契約から作成された請求書は、Microsoft Dataverse データの統合プロジェクトを通して Supply Chain Management に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="c0136-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="c0136-123">自由書式の請求書の会計ステータスが **処理中** の場合、これらの請求書の更新は Supply Chain Management の自由書式の請求書に同期されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="c0136-124">自由書式の請求書が Supply Chain Management に転記済で、会計ステータスが **完了** に更新されると、Field Service から更新を同期することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="c0136-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="c0136-125">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="c0136-125">Field Service CRM solution</span></span>

<span data-ttu-id="c0136-126">**契約元の行を有する** 列が **請求書** テーブルに追加されました。</span><span class="sxs-lookup"><span data-stu-id="c0136-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="c0136-127">この列は、契約書から作成された請求書のみが同期されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c0136-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c0136-128">契約書に基づく請求明細行が少なくとも 1 つ含まれている場合、値は **true** です。</span><span class="sxs-lookup"><span data-stu-id="c0136-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="c0136-129">**契約元の行を有する** 列が **請求明細行** テーブルに追加されました。</span><span class="sxs-lookup"><span data-stu-id="c0136-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="c0136-130">この列は、契約書から作成された請求明細行のみが同期されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="c0136-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="c0136-131">請求明細行が契約書に基づいている場合、値は **true** です。</span><span class="sxs-lookup"><span data-stu-id="c0136-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="c0136-132">**請求日** は、Supply Chain Management の必須フィールドです。</span><span class="sxs-lookup"><span data-stu-id="c0136-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="c0136-133">したがって、この列は同期が発生する前に Field Service に値が必要です。</span><span class="sxs-lookup"><span data-stu-id="c0136-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="c0136-134">この要件を満たすためには、次のロジックが追加されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="c0136-135">**請求日** 列の **請求書** テーブルが空白の場合 (つまり、値が存在しない場合)、契約に基づく請求明細行が追加された現在の日付が設定されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="c0136-136">ユーザーは **請求日** 列を変更できます。</span><span class="sxs-lookup"><span data-stu-id="c0136-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="c0136-137">しかし、契約に基づく請求書を保存しようとすると、請求書の **請求日** 列が空白の場合、ビジネス プロセス エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c0136-137">However, when the user tries to save an invoice that originates from an agreement, they receive a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="c0136-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="c0136-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="c0136-139">Supply Chain Management 内</span><span class="sxs-lookup"><span data-stu-id="c0136-139">In Supply Chain Management</span></span>

<span data-ttu-id="c0136-140">Field Service の契約請求書から作成された Supply Chain Management の自由書式の請求書を区別するために、統合に対して請求書発生元を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c0136-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="c0136-141">請求書が **契約請求書統合** タイプの請求書発生元を含んでいる場合、**外部請求書番号** フィールドが **売上請求書** ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="c0136-142">請求書ヘッダーでの表示に加えて、Field Service 契約請求書から作成された請求書が Supply Chain Management から Field Service への販売注文同期の間に除外されることを保証するために **外部請求書番号** 情報は使用されます。</span><span class="sxs-lookup"><span data-stu-id="c0136-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="c0136-143">**売掛金勘定** \> **設定** \> **請求書発生元コード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="c0136-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="c0136-144">**新規** を選択し、新しい請求書発生元を作成します。</span><span class="sxs-lookup"><span data-stu-id="c0136-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="c0136-145">**販売元** フィールドに、**FS** のような請求書発生元の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0136-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="c0136-146">**説明** フィールドに、**Field Service契約請求書** のような説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="c0136-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="c0136-147">**発生元タイプの割り当て** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="c0136-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="c0136-148">**請求書発生元** フィールドを **契約請求書統合** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c0136-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="c0136-149">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="c0136-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="c0136-150">データ統合プロジェクト内</span><span class="sxs-lookup"><span data-stu-id="c0136-150">In the Data Integration project</span></span>

<span data-ttu-id="c0136-151">タスク: **請求明細行**</span><span class="sxs-lookup"><span data-stu-id="c0136-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="c0136-152">Supply Chain Management フィールド **主勘定表示値** に対する既定の値が、希望する値と一致するように更新されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="c0136-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="c0136-153">既定のテンプレートの値は **401100** です。</span><span class="sxs-lookup"><span data-stu-id="c0136-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c0136-154">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="c0136-154">Template mapping in Data integration</span></span>

<span data-ttu-id="c0136-155">次の図は、データ統合のテンプレート マッピングを示しています。</span><span class="sxs-lookup"><span data-stu-id="c0136-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="c0136-156">契約請求書 (Field Service から Supply Chain Management) : 請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="c0136-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="c0136-157">[![請求書ヘッダーのデータ統合でのテンプレート マッピング](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="c0136-157">[![Template mapping in Data integration for invoice headers](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="c0136-158">契約請求書 (Field Service から Supply Chain Management) : 請求明細行</span><span class="sxs-lookup"><span data-stu-id="c0136-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="c0136-159">[![請求書ヘッダーのデータ統合でのテンプレート マッピング](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="c0136-159">[![Template mapping in Data integration for invoice lines](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]