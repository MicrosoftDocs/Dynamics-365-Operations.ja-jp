---
title: "Field Service の契約請求書を Finance and Operations の自由書式の請求書に同期します"
description: "このトピックでは、Microsoft Dynamics 365 for Field Service の契約請求書を Microsoft Dynamics 365 for Finance and Operations の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。"
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: ja-jp
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="d845f-103">Field Service の契約請求書を Finance and Operations の自由書式の請求書に同期します</span><span class="sxs-lookup"><span data-stu-id="d845f-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d845f-104">このトピックでは、Microsoft Dynamics 365 for Field Service の契約請求書を Microsoft Dynamics 365 for Finance and Operations の自由書式の請求書に同期するために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d845f-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d845f-105">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="d845f-105">Templates and tasks</span></span>

<span data-ttu-id="d845f-106">次のテンプレートと基本的なタスクは、Field Service の契約請求書と Finance and Operations の自由書式の請求書との同期を実行するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="d845f-107">**データ統合でのテンプレートの名前:**</span><span class="sxs-lookup"><span data-stu-id="d845f-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="d845f-108">契約請求書 (Field Service から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d845f-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="d845f-109">**データ統合プロジェクトのタスク名:**</span><span class="sxs-lookup"><span data-stu-id="d845f-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="d845f-110">請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d845f-110">Invoice headers</span></span>
- <span data-ttu-id="d845f-111">請求明細行</span><span class="sxs-lookup"><span data-stu-id="d845f-111">Invoice lines</span></span>

<span data-ttu-id="d845f-112">契約請求書の同期が処理される前に、次の同期が必要です。</span><span class="sxs-lookup"><span data-stu-id="d845f-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="d845f-113">勘定 (Sales から Finance and Operations) – 直接</span><span class="sxs-lookup"><span data-stu-id="d845f-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="d845f-114">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="d845f-114">Entity set</span></span>

| <span data-ttu-id="d845f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="d845f-115">Field Service</span></span>  | <span data-ttu-id="d845f-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d845f-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="d845f-117">請求書</span><span class="sxs-lookup"><span data-stu-id="d845f-117">invoices</span></span>       | <span data-ttu-id="d845f-118">CDS 顧客の自由書式請求書ヘッダー</span><span class="sxs-lookup"><span data-stu-id="d845f-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="d845f-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="d845f-119">invoicedetails</span></span> | <span data-ttu-id="d845f-120">CDS 顧客の自由書式請求書明細行</span><span class="sxs-lookup"><span data-stu-id="d845f-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="d845f-121">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="d845f-121">Entity flow</span></span>

<span data-ttu-id="d845f-122">Field Service の契約から作成された請求書は、Common Data Service (CDS) データの統合プロジェクトを通して Finance and Operations に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="d845f-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="d845f-123">自由書式の請求書の会計ステータスが**処理中**の場合、これらの請求書の更新は Finance and Operations の自由書式の請求書に同期されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="d845f-124">自由書式の請求書が Finance and Operations に転記済で、会計ステータスが**完了**に更新されると、Field Service から更新を同期することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="d845f-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d845f-125">Field Service CRM ソリューション</span><span class="sxs-lookup"><span data-stu-id="d845f-125">Field Service CRM solution</span></span>

<span data-ttu-id="d845f-126">[**契約元の行を有する**] フィールドが**請求書**エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="d845f-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="d845f-127">このフィールドは、契約書から作成された請求書のみが同期されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d845f-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="d845f-128">契約書に基づく請求明細行が少なくとも 1 つ含まれている場合、値は **true** です。</span><span class="sxs-lookup"><span data-stu-id="d845f-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="d845f-129">[**契約元を有する**] フィールドが**請求明細行**エンティティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="d845f-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="d845f-130">このフィールドは、契約書から作成された請求明細行のみが同期されることを保証するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d845f-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="d845f-131">請求明細行が契約書に基づいている場合、値は **true** です。</span><span class="sxs-lookup"><span data-stu-id="d845f-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="d845f-132">[**請求日**] は、Finance and Operations の必須フィールドです。</span><span class="sxs-lookup"><span data-stu-id="d845f-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="d845f-133">したがって、このフィールドは同期が発生する前に Field Service に値が必要です。</span><span class="sxs-lookup"><span data-stu-id="d845f-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="d845f-134">この要件を満たすためには、次のロジックが追加されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="d845f-135">[**請求日**] フィールドの**請求書**エンティティが空白の場合 (つまり、値が存在しない) 場合、契約に基づく請求明細行が追加された現在の日付が設定されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="d845f-136">ユーザーは [**請求日**] フィールドを変更できます。</span><span class="sxs-lookup"><span data-stu-id="d845f-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="d845f-137">ただし、ユーザーが契約に基づいた請求書を保存する際に、[**請求日**] フィールドの請求書が空白の場合、ユーザーは業務プロセス エラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d845f-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d845f-138">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="d845f-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="d845f-139">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d845f-139">In Finance and Operations</span></span>

<span data-ttu-id="d845f-140">Field Service の契約請求書から作成された Finance and Operations の自由書式の請求書を区別するために、統合に対して請求書発生元を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d845f-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="d845f-141">請求書が**契約請求書統合**タイプの請求書発生元を含んでいる場合、[**外部請求書番号**] フィールドが**売上請求書**ヘッダーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="d845f-142">請求書ヘッダーでの表示に加えて、Field Service 契約請求書から作成された請求書が Finance and Operations から Field Service への販売注文同期の間に除外されることを保証するために**外部請求書番号**情報は使用されます。</span><span class="sxs-lookup"><span data-stu-id="d845f-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="d845f-143">[**売掛金勘定**] \> [**設定**] \> [**請求書発生元コード**] に移動します。</span><span class="sxs-lookup"><span data-stu-id="d845f-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="d845f-144">**新規**を選択し、新しい請求書発生元を作成します。</span><span class="sxs-lookup"><span data-stu-id="d845f-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="d845f-145">[**販売元**] フィールドに、**FS** のような請求書発生元の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="d845f-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="d845f-146">[**説明**] フィールドに、**Field Service契約請求書**のような説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="d845f-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="d845f-147">[**発生元タイプの割り当て**] チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="d845f-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="d845f-148">[**請求書発生元**] フィールドを**契約請求書統合**に設定します。</span><span class="sxs-lookup"><span data-stu-id="d845f-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="d845f-149">[**保存**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="d845f-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="d845f-150">データ統合プロジェクト内</span><span class="sxs-lookup"><span data-stu-id="d845f-150">In the Data Integration project</span></span>

<span data-ttu-id="d845f-151">タスク: **請求明細行**</span><span class="sxs-lookup"><span data-stu-id="d845f-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="d845f-152">Finance and Operations フィールド**主勘定表示値**に対する既定の値が、希望する値と一致するように更新されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="d845f-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="d845f-153">既定のテンプレートの値は **401100** です。</span><span class="sxs-lookup"><span data-stu-id="d845f-153">The default template value is **401100**.</span></span>

