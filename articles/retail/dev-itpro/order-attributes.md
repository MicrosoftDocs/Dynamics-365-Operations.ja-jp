---
title: "注文属性"
description: "このトピックでは、小売用バックオフィス、POS、および CRT でオーダーの属性値を直接編集および設定する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-24
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 46360c5707e51d77d95f7d6e2b8d10109ad77bcc
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="order-attributes"></a><span data-ttu-id="2a8a5-103">注文属性</span><span class="sxs-lookup"><span data-stu-id="2a8a5-103">Order attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2a8a5-104">以前は、属性フレームワークは、オンライン注文でのみ属性をサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-104">Previously, the attribute framework supported attributes only in online orders.</span></span> <span data-ttu-id="2a8a5-105">ただし、フレームワークが拡張されたため、現金売りトランザクション、顧客の注文、およびコール センター注文の属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-105">However, the framework has been extended so that it now supports attributes in cash-and-carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="2a8a5-106">この機能拡張により、小売用バックオフィス、販売時点管理 (POS)、および Commerce Runtime (CRT) でオーダーの属性値を直接編集および設定できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-106">This enhancement lets you edit and set attribute values for orders directly in Retail headquarters, the point of sale (POS), and the Commerce runtime (CRT).</span></span> <span data-ttu-id="2a8a5-107">小売用バック オフィスには、属性の値を編集したり更新するためのページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-107">Retail headquarters now includes pages for editing and updating attribute values.</span></span> <span data-ttu-id="2a8a5-108">たがって、コール センター注文の値は、小売用バックオフィスで設定できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-108">Therefore, you can set the values for call center orders in Retail headquarters.</span></span> <span data-ttu-id="2a8a5-109">POS で使用できる属性値を設定するためのユーザー インターフェイス (UI) がありませんが、新しい UI を追加する POS を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-109">Although no out-of-box user interface (UI) for setting attribute values is available in the POS, you can extend the POS to add a new UI.</span></span> <span data-ttu-id="2a8a5-110">UI を必要とせず、ビジネス ロジックを追加するだけの場合、ビジネス ロジックを CRT に直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-110">If you don't require a UI and just want to add business logic, you can add the business logic directly in CRT.</span></span> <span data-ttu-id="2a8a5-111">小売り用バックオフィス構成を使用することにより、新しい属性を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-111">You can create new attributes by using the Retail headquarters configurations.</span></span> <span data-ttu-id="2a8a5-112">データベースの変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-112">No database changes are required.</span></span> <span data-ttu-id="2a8a5-113">以前は、小売用バックオフィスとチャンネル データベースで新しいテーブルを作成するには、それらのテーブルを変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-113">Previously, you had to create new tables in Retail headquarters and the channel database, and then modify those tables.</span></span>

## <a name="why-and-when-you-should-customer-attributes"></a><span data-ttu-id="2a8a5-114">顧客属性が必要な理由および場合</span><span class="sxs-lookup"><span data-stu-id="2a8a5-114">Why and when you should customer attributes</span></span>

<span data-ttu-id="2a8a5-115">現金売りトランザクション、顧客注文、またはコールセンターの注文に新しいフィールドを追加し、POS または小売の本社で情報をキャプチャする場合は、顧客属性を使用します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-115">If you want to add new fields to cash-and-carry transactions, customer orders, or call center orders, and if you want to capture the information in the POS or Retail headquarters, use customer attributes.</span></span> <span data-ttu-id="2a8a5-116">以前は、現金売りトランザクション (トランザクション ヘッダーまたは行) または POS の顧客注文に新しいフィールドを追加するには、小売用バックオフィスとチャネル データベースで新しい拡張テーブルを作成し、CRT および POS コードにインライン変更を加えて各種画面および操作を処理する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-116">Previously, to add a new field to a cash-and-carry transaction (transaction header or lines) or a customer order in the POS, you had to create a new extension table in Retail headquarters and the channel database, and then make inline changes to CRT and POS code to handle the various screens and operations.</span></span> <span data-ttu-id="2a8a5-117">また、チャネル データベースと小売用バックオフィス間でデータを同期するように Commerce Data Exchange を構成する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-117">You also had to configure Commerce Data Exchange to synchronize the data between the channel database and Retail headquarters.</span></span> <span data-ttu-id="2a8a5-118">ただし、顧客属性はコンフィギュレーションを通してこれらすべてのアクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-118">However, customer attributes now let you complete all these actions through configuration.</span></span> <span data-ttu-id="2a8a5-119">コードを記述またはカスタム拡張機能テーブルを作成する必要はありませんが、主要なビジネス ロジックおよび POS UI を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-119">You don't have to write any code or create custom extension tables, but you still need to create the core business logic and the POS UI.</span></span>

<span data-ttu-id="2a8a5-120">この最初のバージョンは **String** 属性タイプのみをサポートしますが、将来のバージョンは他の属性タイプをサポートします。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-120">This first version supports only the **String** attribute type, but future versions will support other attribute types.</span></span> <span data-ttu-id="2a8a5-121">データをマスター テーブルから取得し、そのデータに X++ の複雑な検索ロジックとコア ビジネス ロジックが必要な場合は、拡張プロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-121">If you want the data to come from the master table, and that data involves complex search logic and core business logic in X++, you should use extension properties.</span></span>

## <a name="define-attribute-types"></a><span data-ttu-id="2a8a5-122">属性タイプを定義</span><span class="sxs-lookup"><span data-stu-id="2a8a5-122">Define attribute types</span></span>

<span data-ttu-id="2a8a5-123">最初に、属性タイプを定義し、それに有効な範囲を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-123">First, you must define the attribute types and assign valid ranges to them.</span></span>

1. <span data-ttu-id="2a8a5-124">**製品情報管理** > **設定** > **カテゴリと属性** > **属性タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-124">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attribute types**.</span></span>
2. <span data-ttu-id="2a8a5-125">**属性タイプ**ページで、**新規**を選択し、新しい属性タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-125">On the **Attribute types** page, select **New** to add a new attribute type.</span></span>
3. <span data-ttu-id="2a8a5-126">階層タイプ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-126">Enter a name for the attribute type.</span></span>
4. <span data-ttu-id="2a8a5-127">**一般**クイック タブの、**タイプ**フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-127">On the **General** FastTab, in the **Type** field, select the type of data that can be entered for attributes that are assigned to this data type.</span></span>
5. <span data-ttu-id="2a8a5-128">属性タイプが**少数点**または**整数**の場合、測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-128">If the attribute type is **Decimal** or **Integer**, select a unit of measure.</span></span>
6. <span data-ttu-id="2a8a5-129">属性の型が**テキスト**である場合は、それを固定値の一覧を定義できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-129">If the attribute type is **Text**, you can define a fixed list of values for it.</span></span> <span data-ttu-id="2a8a5-130">**固定リスト** チェック ボックスをオンにし、**値** クイック タブで、値の一覧を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-130">Select the **Fixed list** check box, and then, on the **Values** FastTab, enter the list of values.</span></span>
7. <span data-ttu-id="2a8a5-131">属性タイプに有効な値の範囲を定義するには、**値の範囲** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-131">To define a range of valid values for the attribute type, select the **Value range** check box.</span></span> <span data-ttu-id="2a8a5-132">次に、**範囲** クイックタブで、値の有効範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-132">Then, on the **Range** FastTab, enter the valid range of values.</span></span>

## <a name="define-the-attributes"></a><span data-ttu-id="2a8a5-133">属性の定義</span><span class="sxs-lookup"><span data-stu-id="2a8a5-133">Define the attributes</span></span> 

<span data-ttu-id="2a8a5-134">次に、属性を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-134">Next, you must define the attributes.</span></span> <span data-ttu-id="2a8a5-135">定義する各属性に対して、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-135">Follow these steps for each attribute that you want to define.</span></span>

1. <span data-ttu-id="2a8a5-136">**製品情報管理** > **設定** > **カテゴリと属性** > **属性**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-136">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attributes**.</span></span>
2. <span data-ttu-id="2a8a5-137">**属性**ページで、**新規**を選択し、新しい属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-137">On the **Attributes** page, select **New** to add a new attribute.</span></span>
3. <span data-ttu-id="2a8a5-138">属性の名前、フレンドリ名、および説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-138">Enter a name, friendly name, and description for the attribute.</span></span> <span data-ttu-id="2a8a5-139">また、属性にユーザーを表示する必要があるヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-139">Additionally, enter any Help text that should be shown to the user for the attribute.</span></span>
4. <span data-ttu-id="2a8a5-140">**属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-140">In the **Attribute type** field, select the attribute type to assign to the attribute.</span></span>
5. <span data-ttu-id="2a8a5-141">属性タイプに応じて、**既定値**フィールドに、属性が顧客に割り当てられたときに既定で表示される値または値の範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-141">Depending on the attribute type, in the **Default value** field, enter the value or range of values that is shown by default when the attribute is assigned to a customer.</span></span>
6. <span data-ttu-id="2a8a5-142">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-142">Select **Translate**.</span></span> <span data-ttu-id="2a8a5-143">その後、**テキストの翻訳** ページで、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-143">Then, on the **Text translation** page, enter the name, description, friendly name, and Help text for the attribute in additional languages.</span></span>

## <a name="define-attribute-groups"></a><span data-ttu-id="2a8a5-144">属性グループの定義</span><span class="sxs-lookup"><span data-stu-id="2a8a5-144">Define attribute groups</span></span>

1. <span data-ttu-id="2a8a5-145">**製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-145">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attribute groups**.</span></span>
2. <span data-ttu-id="2a8a5-146">**属性グループ**ページで、**新規**を選択し、新しい属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-146">On the **Attribute groups** page, select **New** to add a new attribute group.</span></span>
3. <span data-ttu-id="2a8a5-147">属性グループ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-147">Enter a name for the attribute group.</span></span> <span data-ttu-id="2a8a5-148">その後、**全般** クイックタブで、属性グループのフレンドリ名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-148">Then, on the **General** FastTab, enter a friendly name, a description, and any Help text for the attribute group.</span></span>
4. <span data-ttu-id="2a8a5-149">**属性**クイック タブで、**追加**を選択して、属性グループに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-149">On the **Attributes** FastTab, select **Add** to add attributes to the attribute group.</span></span> <span data-ttu-id="2a8a5-150">**既定値**フィールドでは、選択した属性の既定値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-150">In the **Default value** field, you can enter a default value for the selected attributes.</span></span>
5. <span data-ttu-id="2a8a5-151">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-151">Select **Translate**.</span></span> <span data-ttu-id="2a8a5-152">その後、**テキストの翻訳** ページで、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-152">Then, on the **Text translation** page, enter the description, friendly name, and Help text for the attribute group in additional languages.</span></span>

## <a name="link-the-attribute-group-to-the-channel"></a><span data-ttu-id="2a8a5-153">属性グループのチャネルへのリンク</span><span class="sxs-lookup"><span data-stu-id="2a8a5-153">Link the attribute group to the channel</span></span>

1. <span data-ttu-id="2a8a5-154">**小売** > **チャンネル** > **小売店舗** > **すべての小売店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-154">Go to **Retail** > **Channels** > **Retail stores** > **All retail stores**.</span></span>
2. <span data-ttu-id="2a8a5-155">**チャネル** ページの属性をリンクする必要があるチャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-155">Select the channel that the attributes on the **Channel** page should be linked to.</span></span>
3. <span data-ttu-id="2a8a5-156">**設定**タブで、**属性グループ**の**販売注文属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-156">On the **Set up** tab, select **Sales order attributes** under **Attribute group**.</span></span>
4. <span data-ttu-id="2a8a5-157">**販売注文属性グループ**ページで、**新規**を選択し、属性グループをチャネルにリンクします。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-157">On the **Sales order attribute groups** page, select **New** to link the attribute group to the channel.</span></span>
5. <span data-ttu-id="2a8a5-158">**名前**フィールドで属性グループを選択してチャネルにリンクします。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-158">In the **Name** field, select the attribute group to link to the channel.</span></span>
6. <span data-ttu-id="2a8a5-159">**属性の適用先**フィールドで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-159">In the **Apply attributes to** field, select one of the following options:</span></span>

    - <span data-ttu-id="2a8a5-160">**ヘッダー** – 属性は、トランザクション ヘッダーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-160">**Header** – The attributes will apply only to the transaction header.</span></span>
    - <span data-ttu-id="2a8a5-161">**明細行** – 属性は、トランザクション明細行にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-161">**Lines** – The attribute will apply only to the transaction lines.</span></span>
    - <span data-ttu-id="2a8a5-162">**既定** - 属性は、トランザクション ヘッダーとトランザクション明細行の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-162">**Default** – The attribute will apply to both the transaction header and the transaction lines.</span></span>

7. <span data-ttu-id="2a8a5-163">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-163">Select **Save**.</span></span>

## <a name="run-the-distribution-jobs"></a><span data-ttu-id="2a8a5-164">配送ジョブを実行</span><span class="sxs-lookup"><span data-stu-id="2a8a5-164">Run the distribution jobs</span></span>

1. <span data-ttu-id="2a8a5-165">**小売** > **小売 IT** > **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-165">Go to **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
2. <span data-ttu-id="2a8a5-166">**製品 (1040)** を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-166">Select **Products (1040)**, and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="2a8a5-167">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-167">When you're prompted, select **Yes**.</span></span> <span data-ttu-id="2a8a5-168">このステップは、新しい属性、属性タイプ、または属性グループを追加した場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-168">This step is required only if you added any new attributes, attribute types, or attribute groups.</span></span>
3. <span data-ttu-id="2a8a5-169">**チャネル コンフィギュレーション ジョブ (1070)** を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-169">Select **Channel configuration job (1070)**, and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="2a8a5-170">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-170">When you're prompted, select **Yes**.</span></span>

## <a name="set-attribute-values-for-call-center-orders"></a><span data-ttu-id="2a8a5-171">コール センターの注文の属性値を設定</span><span class="sxs-lookup"><span data-stu-id="2a8a5-171">Set attribute values for call center orders</span></span>

<span data-ttu-id="2a8a5-172">チャンネルの注文属性を構成した後、**顧客サービス**または**すべての販売注文**、およびコール センターの新しい注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-172">After you configure the order attributes for the channel, go to **Customer service** or **All Sales orders**, and create a new call center order.</span></span>

1. <span data-ttu-id="2a8a5-173">顧客注文の作成後または作成中に、トランザクション ヘッダーの属性値を設定する場合は、アクション ウィンドウの**小売**タブで、**小売属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-173">After or during the creation of a customer order, if you want to set an attribute value for the transaction header, on the Action Pane, on the **Retail** tab, select **Retail Attributes**.</span></span>
2. <span data-ttu-id="2a8a5-174">**販売注文属性値**ページで、属性値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-174">On the **Sales order attributes values** page, you can set the values for the attributes.</span></span> <span data-ttu-id="2a8a5-175">このページの属性のリストは、チャネル用にコンフィギュレーションした属性グループに基づいています。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-175">The list of attributes on this page is based on the attribute group that you configured for the channel.</span></span>
3. <span data-ttu-id="2a8a5-176">行レベルで属性値を設定するには、**販売注文** ページで **行** ビューを選択し、属性値を設定する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-176">To set attribute values at the line level, on the **Sales order** page, select the **Lines** view, and then select the line to set the attribute value for.</span></span> <span data-ttu-id="2a8a5-177">**販売注文明細行グループ** で **小売** > **小売属性** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-177">Under **Sales order lines group**, select **Retail** > **Retail attributes**.</span></span>
4. <span data-ttu-id="2a8a5-178">値を設定するすべての販売明細行に対して手順 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-178">Repeat step 3 for all the sales lines that you want to set the values for.</span></span>

## <a name="view-the-attributes-values-for-cash-and-carry-transactions-in-retail-headquarters"></a><span data-ttu-id="2a8a5-179">小売用バック オフィスでの現金売りトランザクションの属性値の表示</span><span class="sxs-lookup"><span data-stu-id="2a8a5-179">View the attributes values for cash-and-carry transactions in Retail headquarters</span></span>

<span data-ttu-id="2a8a5-180">配送ジョブを実行し小売用バックオフィスに現金売りトランザクションを収集した後、トランザクションの属性値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-180">After you've run the distribution job and pulled a cash-and-carry transaction into Retail headquarters, you can view the attribute values for that transaction.</span></span> <span data-ttu-id="2a8a5-181">POS は、注文の属性を表示するための UI を提供しません。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-181">The POS doesn't provide a UI for viewing order attributes.</span></span> <span data-ttu-id="2a8a5-182">したがって、注文の属性値を表示するには、POS を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-182">Therefore, to view the order attribute values, you must extend the POS.</span></span>

1. <span data-ttu-id="2a8a5-183">**小売** > **照会およびレポート** > **小売店舗のトランザクション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-183">Go to **Retail** > **Inquires and reports** > **Retail store transactions**.</span></span>
2. <span data-ttu-id="2a8a5-184">トランザクション ヘッダー属性を表示するには、アクション ウィンドウで **小売属性** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-184">To view the transaction header attributes, on the Action Pane, select **Retail attributes**.</span></span>
3. <span data-ttu-id="2a8a5-185">トランザクション ヘッダー行の属性を表示するには、アクション ウィンドウで **トランザクション** > **販売トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-185">To view the transaction lines attributes, on the Action Pane, select **Transaction** > **Sales transaction**.</span></span>
4. <span data-ttu-id="2a8a5-186">**販売トランザクション**ページで、すべての明細行を選択し、アクション ウィンドウで、**小売属性**を選択して、明細行の属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-186">On the **Sales transactions** page, select any line, and then, on the Action Pane, select **Retail attributes** to view the line attributes.</span></span>

> [!NOTE]
> <span data-ttu-id="2a8a5-187">あなたの属性グループの一部として構成され、チャンネルにリンクされている属性のみ、Retail headquarters UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-187">Only the attributes that are configured as part of your attribute group and linked to the channel will appear in the Retail headquarters UI.</span></span>

## <a name="extend-attributes-to-add-business-logic-in-crt"></a><span data-ttu-id="2a8a5-188">CRT でビジネス ロジックを追加するには、属性を拡張します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-188">Extend attributes to add business logic in CRT</span></span>

<span data-ttu-id="2a8a5-189">Retail SDK に追加された新しいサンプルでは、CRT の注文属性のビジネス ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-189">A new sample that has been added to the Retail SDK adds business logic for order attributes in CRT.</span></span> <span data-ttu-id="2a8a5-190">この例には、ビジネス ロジックのコードのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-190">This sample includes code only for the business logic.</span></span> <span data-ttu-id="2a8a5-191">属性に対する読み取りおよび書き込み処理は自動化されているため、属性を保存したり読み取ったりする方法は示しません。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-191">It doesn't show how to save or read the attributes, because read and write operations for attributes are automated.</span></span>

<span data-ttu-id="2a8a5-192">このサンプルでは、次のシナリオを実装しています。カートを中断するときはいつでも、属性値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-192">The sample implements the following scenario: Whenever you suspend a cart, you set set an attribute value.</span></span> <span data-ttu-id="2a8a5-193">カートを再開するとき、その値を消去します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-193">When you resume the cart, you want to clear that value.</span></span> <span data-ttu-id="2a8a5-194">事前トリガーが **SuspendCartRequest** に追加され、ビジネス ロジックが記述されました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-194">A pre-trigger was added for **SuspendCartRequest**, and the business logic was written.</span></span> <span data-ttu-id="2a8a5-195">CRT で任意のトリガーを拡張または任意の要求をオーバーライドして、シナリオに基づきロジックをセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-195">You can extend any trigger or override any request in CRT to set the logic, based on your scenario.</span></span>

<span data-ttu-id="2a8a5-196">完全なサンプル コードは Retail SDK\\SampleExtensions\\CommerceRuntime\\Extensions.TransactionAttributesSample の Retail SDK で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-196">You can find the full sample code in the Retail SDK at Retail SDK\\SampleExtensions\\CommerceRuntime\\Extensions.TransactionAttributesSample.</span></span>

- <span data-ttu-id="2a8a5-197">新しい C# ポータブル クラス ライブラリ プロジェクトを作成し、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-197">Create a new C# portable class library project, and paste in the following code.</span></span>

    ```C#
    public class CustomSuspendCartTrigger : IRequestTrigger
    {
        // summary
        // Gets the list of supported request types.
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new [ ] { typeof(SuspendCartRequest)};
            }
         }

        // Pre-trigger code.

        // summary
        // param name="request" The request param
        public void OnExecuting(Request request)
        {
            ThrowIf.Null(request, "request");
            Type requestedType = request.GetType();
            if (requestedType == typeof(SuspendCartRequest))
            {
                SuspendCartRequest suspendCartRequest = request as SuspendCartRequest;
                // Get the cart.
                var getCartServiceRequest = new GetCartServiceRequest(
                    new CartSearchCriteria(suspendCartRequest.CartId), QueryResultSettings.SingleRecord);
                Cart cart = request.RequestContext.Execute<GetCartServiceResponse>(getCartServiceRequest).Carts.Single();
                // Update the transaction header attribute for customer order.
                if (cart.CartType == CartType.CustomerOrder)
                {
                    bool cartUpdated = CustomCartHelper.CreateUpdateTransactionHeaderAttribute(
                        cart, reserveNow: false, updateAttribute: true);
                    if (cartUpdated)
                    {
                        // Save the cart after updating the header attribute.
                        var saveCartRequest = new SaveCartRequest(cart);
                        request.RequestContext.Execute<SaveCartResponse>(saveCartRequest);
                    } 
                } 
            } 
        }

        // Post-trigger code.

        // summary
        // param name="request" The request param
        // param name="response" The response param
        public void OnExecuted(Request request, Response response)
        {
        }
    ```

## <a name="extend-attributes-to-do-some-business-logic-in-the-pos"></a><span data-ttu-id="2a8a5-198">POS でビジネス ロジックを行うには、属性を拡張します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-198">Extend attributes to do some business logic in the POS</span></span>

<span data-ttu-id="2a8a5-199">Retail SDK に追加された新しいサンプルでは、POS の注文属性のビジネス ロジックを設定します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-199">A new sample that has been added to the Retail SDK sets the business logic for order attributes in the POS.</span></span> <span data-ttu-id="2a8a5-200">この例には、ビジネス ロジックのコードのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-200">This sample includes code only for the business logic.</span></span> <span data-ttu-id="2a8a5-201">属性に対する読み取りおよび書き込み処理は自動化されているため、属性の値を保存したり読み取ったりする方法は示しません。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-201">It doesn't show how to save or read attribute values, because read and write operations for attributes are automated.</span></span> <span data-ttu-id="2a8a5-202">属性の値は、シナリオに基づき、CRT または POS のいずれかで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-202">You can set the values for attributes in either CRT or the POS, based on your scenario.</span></span> <span data-ttu-id="2a8a5-203">値が顧客の入力に基づいている場合、POS クライアントで設定します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-203">If your values are based on customer input, set them in the POS client.</span></span> <span data-ttu-id="2a8a5-204">一部のビジネス ロジックが含まれている場合は、CRT で値を設定します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-204">If some business logic is involved, set the values in CRT.</span></span>

<span data-ttu-id="2a8a5-205">このサンプルでは、次のシナリオを実装しています。企業間 (B2B) 注文を作成し、 顧客からのフィードバックに基づいて B2B 属性の値を設定する場合 (**Yes** または **No**)。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-205">The sample implements the following scenario: You create a business-to-business (B2B) order and want to set the B2B attribute value (**Yes** or **No**), based on customer input.</span></span> <span data-ttu-id="2a8a5-206">**PreEndTransactionTrigger** は値を設定するために POS で拡張されました。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-206">**PreEndTransactionTrigger** was extended in the POS to set the values.</span></span> <span data-ttu-id="2a8a5-207">必要に応じて任意の POS トリガーを拡張、または要求をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-207">You can extend any POS trigger or override the request as appropriate.</span></span>

<span data-ttu-id="2a8a5-208">完全なサンプル コードは Retail SDK\\POS\\Extensions\\B2BSample の Retail SDK で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-208">You can find the full sample code in the Retail SDK at Retail SDK\\POS\\Extensions\\B2BSample.</span></span>

> [!NOTE]
> <span data-ttu-id="2a8a5-209">そのコードに属性と属性値を設定または追加した場合でも、構成された属性のみ Retail headquarters UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-209">Only the configured attributes will appear in the Retail headquarters UI, even if you set or add attributes and attribute values in the code.</span></span> <span data-ttu-id="2a8a5-210">属性が、チャンネルにリンクされている属性グループに属さない場合は、小売用バックオフィス UI に反映されません。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-210">If an attribute isn't part of the attribute group that you linked to the channel, it won't appear in the Retail headquarters UI.</span></span>

1. <span data-ttu-id="2a8a5-211">Retail SDK から **ModernPOS.sln\\CloudPos.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-211">From the Retail SDK, open **ModernPOS.sln\\CloudPos.sln**.</span></span>
2. <span data-ttu-id="2a8a5-212">Retail SDK で、**POS.Extension** プロジェクトに新しい拡張フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-212">In the Retail SDK, create a new extension folder under the **POS.Extension** project.</span></span>
3. <span data-ttu-id="2a8a5-213">新しい拡張フォルダーに、新しい **manifest.json** ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-213">In the new extension folder, add a new **manifest.json** file.</span></span>
4. <span data-ttu-id="2a8a5-214">次のコードに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-214">Paste in the following code.</span></span>

    ```typescript
    {
        "$schema": "..manifestSchema.json",
        "name": "Pos_Extensibility_B2BSample",
        "publisher": "Microsoft",
        "version": "7.2.0",
        "minimumPosVersion": "7.2.0.0",
        "components": {
        "resources": {
        "supportedUICultures": [ "en-US" ],
        "fallbackUICulture": "en-US",
        "culturesDirectoryPath": "Resources/Strings",
        "stringResourcesFileName": "resources.resjson" 
    },
    "extend": {
        "triggers": [
        {
            "triggerType": "PreEndTransaction",
            "modulePath": "TriggerHandlers/PreEndTransactionTrigger"
        }  
        ]
    } } }
    ```
5.  <span data-ttu-id="2a8a5-215">新しい TypeScript ファイルを作成して **PreEndTransactionTrigger** を実装し、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="2a8a5-215">Create a new TypeScript file to implement **PreEndTransactionTrigger**, and add the following code.</span></span>

    ```typescript
    /**
     * Executes the trigger functionality.
     * @param {Triggers.IPreEndTransactionTriggerOptions} options The options provided to the trigger.
     */

    public execute(options: Triggers.IPreEndTransactionTriggerOptions): Promise<ClientEntities.ICancelable {
        console.log("Executing PreEndTransactionTrigger with options " + JSON.stringify(options) + ".");
        let currentCart: ProxyEntities.Cart;
        return this.context.runtime.executeAsync<GetCurrentCartClientResponse>(new GetCurrentCartClientRequest())
    then((getCurrentCartClientResponse: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>> => {
            currentCart = getCurrentCartClientResponse.data.result;
            // Gets the current customer.
            let result: Promise<ClientEntities.ICancelableDataResult<GetCustomerClientResponse>>;
            if (!ObjectExtensions.isNullOrUndefined(currentCart) && !ObjectExtensions.isNullOrUndefined(currentCart.CustomerId)) {
                let getCurrentCustomerClientRequest: GetCustomerClientRequest<GetCustomerClientResponse =
                    new GetCustomerClientRequest(currentCart.CustomerId);
                result = this.context.runtime.executeAsync<GetCustomerClientResponse>(getCurrentCustomerClientRequest);
            } else {
                result = Promise.resolve({ canceled: false, data: new GetCustomerClientResponse(null) });
            }
            return result;
        })
     .then((getCurrentCustomerClientResponse: ClientEntities.ICancelableDataResult<GetCustomerClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>> => {
        let currentCustomer: ProxyEntities.Customer = getCurrentCustomerClientResponse.data.result;
        // If the cart is a customer order with a B2B customer, then we display a dialog to determine if the order should be B2B.
        let result: Promise<ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse>>;
        if (!ObjectExtensions.isNullOrUndefined(currentCart)
            && currentCart.CustomerOrderModeValue === ProxyEntities.CustomerOrderMode.CustomerOrderCreateOrEdit
            && !ObjectExtensions.isNullOrUndefined(currentCustomer)
            && this.isCustomerB2B(currentCustomer)) {
            let yesButton: ClientEntities.Dialogs.IDialogResultButton = {
                id: PreEndTransactionTrigger.DIALOG_YES_BUTTON_ID,
                label: this.context.resources.getString("string_0"),  "Yes"
                result: PreEndTransactionTrigger.DIALOG_RESULT_YES
            };
            let noButton: ClientEntities.Dialogs.IDialogResultButton = {
                id: PreEndTransactionTrigger.DIALOG_NO_BUTTON_ID,
                label: this.context.resources.getString("string_1"),  "No"
                result: PreEndTransactionTrigger.DIALOG_RESULT_NO
            };
            let showMessageDialogClientRequestOptions: ClientEntities.Dialogs.IMessageDialogOptions = {
                title: this.context.resources.getString("string_2"),  "B2B Order"
                subTitle: StringExtensions.EMPTY,
                message: this.context.resources.getString("string_3"),  "Do you want to mark this order as a B2B order?"
                button1: yesButton,
                button2: noButton
            };
            let showMessageDialogClientRequest: ShowMessageDialogClientRequest<ShowMessageDialogClientResponse> =
                new ShowMessageDialogClientRequest(showMessageDialogClientRequestOptions);
            result = this.context.runtime.executeAsync<ShowMessageDialogClientResponse>(showMessageDialogClientRequest);
        } else {
            result = Promise.resolve({ canceled: false, data: new ShowMessageDialogClientResponse(null) });
        }
        return result;
    })
    .then((showMessageDialogClientResponse: ClientEntities.ICancelableDataResult<ShowMessageDialogClientResponse):
        Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>> => {
        // Save the B2B attribute value depending on the dialog result.
        let messageDialogResult: ClientEntities.Dialogs.IMessageDialogResult = showMessageDialogClientResponse.data.result;
        let result: Promise<ClientEntities.ICancelableDataResult<SaveAttributesOnCartClientResponse>>;
        if (!ObjectExtensions.isNullOrUndefined(messageDialogResult)) {
            let attributeValue: ProxyEntities.AttributeTextValue = new ProxyEntities.AttributeTextValueClass();
            attributeValue.Name = PreEndTransactionTrigger.B2B_CART_ATTRIBUTE_NAME;
            attributeValue.TextValue = messageDialogResult.dialogResult === PreEndTransactionTrigger.DIALOG_RESULT_YES?
            PreEndTransactionTrigger.B2B_ATTRIBUTE_VALUE_TRUE : PreEndTransactionTrigger.B2B_ATTRIBUTE_VALUE_FALSE;
            let attributeValues: ProxyEntities.AttributeValueBase[] = [attributeValue];
            let saveAttributesOnCartRequest: SaveAttributesOnCartClientRequest<SaveAttributesOnCartClientResponse> =
            new SaveAttributesOnCartClientRequest(attributeValues);
            result = this.context.runtime.executeAsync(saveAttributesOnCartRequest);
        } else {
            result = Promise.resolve({ canceled: false, data: new SaveAttributesOnCartClientResponse(null) });
        }
        return result;
    });
    }
    /**
    * Returns whether or not the given customer is a B2B customer.
    * @param {ProxyEntities.Customer} customer The customer.
    * @returns {boolean} Whether or not the given customer is a B2B customer.
    */
    private isCustomerB2B(customer: ProxyEntities.Customer): boolean {
        let isB2B: boolean = false;
        if (!ObjectExtensions.isNullOrUndefined(customer.Attributes)) {
            for (let i: number = 0; i < customer.Attributes.length; i++) {
                let currentAttribute: ProxyEntities.CustomerAttribute = customer.Attributes[i];
                if (currentAttribute.Name === PreEndTransactionTrigger.B2B_CUSTOMER_ATTRIBUTE_NAME) {
                    if (!ObjectExtensions.isNullOrUndefined(currentAttribute.AttributeValue.BooleanValue)) {
                        isB2B = currentAttribute.AttributeValue.BooleanValue;
                    }
                    break;
                }
            }  
        }
        return isB2B;
    } } } }
    ```

