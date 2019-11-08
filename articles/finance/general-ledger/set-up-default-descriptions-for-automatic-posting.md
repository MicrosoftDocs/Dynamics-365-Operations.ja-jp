---
title: 自動転記の既定の説明を設定する
description: このトピックは、一般会計に自動的に転記される、会計項目の説明に使用される既定のテキストの設定方法を説明します。 自由書式のテキストを使用するか、固定変数を選択することによって、既定の説明テキストを設定することができます。
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622692"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="9aa88-104">自動転記の既定の説明を設定する</span><span class="sxs-lookup"><span data-stu-id="9aa88-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="9aa88-105">このトピックは、一般会計に自動的に転記される、会計項目の説明に使用される既定のテキストの設定方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="9aa88-106">自由書式のテキストを使用するか、固定変数を選択することによって、既定の説明テキストを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="9aa88-107">一部のトランザクション タイプに対し、一部の国または地域では、これらのトランザクション タイプに関連する、Microsoft Dynamics AX データベースのフィールドからのテキストを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="9aa88-108">トランザクション タイプ、および国と地域のリストについては、このトピックで後述する [オプション: 既定の説明に他のテキストを追加する](#optional-add-other-text-to-default-descriptions) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9aa88-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="9aa88-109">既定の説明を設定</span><span class="sxs-lookup"><span data-stu-id="9aa88-109">Set up default descriptions</span></span>

1. <span data-ttu-id="9aa88-110">**組織管理** \> **設定** \> **既定の説明**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="9aa88-111">アクション ウィンドウで、**新規**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="9aa88-112">**説明**フィールドで、既定の説明を作成するトランザクションのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="9aa88-113">**言語**フィールドで、この説明が適用される言語を選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="9aa88-114">**テキスト** フィールドに、既定の説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="9aa88-115">フィールドにテキストを入力するか、次の自由書式の 1 つ以上の変数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="9aa88-116">**%1** – トランザクション日付を追加します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="9aa88-117">**%2** – 一般会計に転記されるドキュメント タイプに対応する ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="9aa88-118">たとえば、請求書に関連するトランザクション タイプの場合、**%2** 変数によって請求書番号が追加されます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="9aa88-119">**%3** – 一般会計に転記されるドキュメント タイプに対応する ID を追加します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="9aa88-120">たとえば、請求書に関連するトランザクション タイプの場合、**%3** 変数によって顧客 ID 番号が追加されます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="9aa88-121">オプション: 既定の説明に他のテキストを追加する</span><span class="sxs-lookup"><span data-stu-id="9aa88-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="9aa88-122">一部のトランザクション タイプに対し、一部の国または地域では、これらのトランザクション タイプに関連するデータのフィールドから取られたテキストを既定の説明に含めることができます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="9aa88-123">次のリストは、このオプションが使用可能なトランザクション タイプ、および国と地域を示します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="9aa88-124">**トランザクション タイプ**</span><span class="sxs-lookup"><span data-stu-id="9aa88-124">**Transaction types**</span></span>

<span data-ttu-id="9aa88-125">次のドキュメント タイプに関連付けられているトランザクション タイプの既定の説明に、他のテキストを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="9aa88-126">顧客請求書</span><span class="sxs-lookup"><span data-stu-id="9aa88-126">Customer invoices</span></span>
- <span data-ttu-id="9aa88-127">顧客訂正票</span><span class="sxs-lookup"><span data-stu-id="9aa88-127">Customer credit notes</span></span>
- <span data-ttu-id="9aa88-128">顧客現金払い</span><span class="sxs-lookup"><span data-stu-id="9aa88-128">Customer cash payments</span></span>
- <span data-ttu-id="9aa88-129">仕入先支払</span><span class="sxs-lookup"><span data-stu-id="9aa88-129">Vendor payments</span></span>
- <span data-ttu-id="9aa88-130">販売注文</span><span class="sxs-lookup"><span data-stu-id="9aa88-130">Sales orders</span></span>
- <span data-ttu-id="9aa88-131">発注書</span><span class="sxs-lookup"><span data-stu-id="9aa88-131">Purchase orders</span></span>
- <span data-ttu-id="9aa88-132">在庫仕訳帳</span><span class="sxs-lookup"><span data-stu-id="9aa88-132">Inventory journals</span></span>
- <span data-ttu-id="9aa88-133">マスター プラン (MRP)</span><span class="sxs-lookup"><span data-stu-id="9aa88-133">Master planning (MRP)</span></span>
- <span data-ttu-id="9aa88-134">固定資産</span><span class="sxs-lookup"><span data-stu-id="9aa88-134">Fixed assets</span></span>

<span data-ttu-id="9aa88-135">**国と地域**</span><span class="sxs-lookup"><span data-stu-id="9aa88-135">**Countries and regions**</span></span>

<span data-ttu-id="9aa88-136">このオプションは、次の国および地域に対して使用できます。</span><span class="sxs-lookup"><span data-stu-id="9aa88-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="9aa88-137">ブラジル</span><span class="sxs-lookup"><span data-stu-id="9aa88-137">Brazil</span></span>
- <span data-ttu-id="9aa88-138">中国</span><span class="sxs-lookup"><span data-stu-id="9aa88-138">China</span></span>
- <span data-ttu-id="9aa88-139">チェコ共和国</span><span class="sxs-lookup"><span data-stu-id="9aa88-139">Czech Republic</span></span>
- <span data-ttu-id="9aa88-140">東ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="9aa88-140">Eastern Europe</span></span>
- <span data-ttu-id="9aa88-141">ハンガリー</span><span class="sxs-lookup"><span data-stu-id="9aa88-141">Hungary</span></span>
- <span data-ttu-id="9aa88-142">インド</span><span class="sxs-lookup"><span data-stu-id="9aa88-142">India</span></span>
- <span data-ttu-id="9aa88-143">日本</span><span class="sxs-lookup"><span data-stu-id="9aa88-143">Japan</span></span>
- <span data-ttu-id="9aa88-144">リトアニア</span><span class="sxs-lookup"><span data-stu-id="9aa88-144">Lithuania</span></span>
- <span data-ttu-id="9aa88-145">ラトビア</span><span class="sxs-lookup"><span data-stu-id="9aa88-145">Latvia</span></span>
- <span data-ttu-id="9aa88-146">ポーランド</span><span class="sxs-lookup"><span data-stu-id="9aa88-146">Poland</span></span>
- <span data-ttu-id="9aa88-147">ロシア</span><span class="sxs-lookup"><span data-stu-id="9aa88-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="9aa88-148">既定の説明にテキストを追加する</span><span class="sxs-lookup"><span data-stu-id="9aa88-148">Add text to default descriptions</span></span>

<span data-ttu-id="9aa88-149">このトピックの前半の [既定の説明の設定](#set-up-default-descriptions) セクションの手順を完了した後、次の手順に従い、既定の説明に他のテキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="9aa88-150">**パラメーター** クイック タブで、**追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="9aa88-151">**参照テーブル** フィールドで、パラメーター データを説明に追加するデータベース テーブルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="9aa88-152">**参照フィールド** フィールドで、説明にパラメーター データを追加するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="9aa88-153">手順 1. ～ 3. を繰り返してパラメーターを追加します。</span><span class="sxs-lookup"><span data-stu-id="9aa88-153">Repeat steps 1 through 3 to add more parameters.</span></span>
