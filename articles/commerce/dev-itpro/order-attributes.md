---
title: 注文属性の定義と設定をする
description: このトピックでは、コマース バックオフィス、POS、および CRT でオーダーの属性値を直接編集および設定する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: 83892
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-10-24
ms.dyn365.ops.version: AX 7.0.0, Retail September 2017 update
ms.openlocfilehash: 4cfa896ae8d0f60267f62668bf301ff6e88be8cd
ms.sourcegitcommit: 3227127dd20c43cedaa8912e74aaf6120a1dcbb9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/28/2020
ms.locfileid: "3628391"
---
# <a name="define-and-set-order-attributes"></a><span data-ttu-id="527f5-103">注文属性の定義および設定</span><span class="sxs-lookup"><span data-stu-id="527f5-103">Define and set order attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="527f5-104">以前は、属性フレームワークは、オンライン注文でのみ属性をサポートしていました。</span><span class="sxs-lookup"><span data-stu-id="527f5-104">Previously, the attribute framework supported attributes only in online orders.</span></span> <span data-ttu-id="527f5-105">ただし、フレームワークが拡張されたため、現金売りトランザクション、顧客の注文、およびコール センター注文の属性がサポートされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="527f5-105">However, the framework has been extended so that it now supports attributes in cash-and-carry transactions, customer orders, and call center orders.</span></span> <span data-ttu-id="527f5-106">この機能拡張により、バックオフィス、販売時点管理 (POS)、および Commerce runtime (CRT) でオーダーの属性値を直接編集および設定できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-106">This enhancement lets you edit and set attribute values for orders directly in Commerce Headquarters, the point of sale (POS), and the Commerce runtime (CRT).</span></span> 

<span data-ttu-id="527f5-107">バックオフィスには、属性の値を編集したり更新するためのページが含まれています。</span><span class="sxs-lookup"><span data-stu-id="527f5-107">Headquarters now includes pages for editing and updating attribute values.</span></span> <span data-ttu-id="527f5-108">たがって、コール センター注文の値は、バックオフィスで設定できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-108">Therefore, you can set the values for call center orders in Headquarters.</span></span> <span data-ttu-id="527f5-109">POS で使用できる属性値を設定するためのユーザー インターフェイス (UI) がありませんが、新しい UI を追加する POS を拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-109">Although no out-of-box user interface (UI) for setting attribute values is available in the POS, you can extend the POS to add a new UI.</span></span> <span data-ttu-id="527f5-110">UI を必要とせず、ビジネス ロジックを追加するだけの場合、ビジネス ロジックを CRT に直接追加できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-110">If you don't require a UI and just want to add business logic, you can add the business logic directly in CRT.</span></span> <span data-ttu-id="527f5-111">バックオフィス コンフィギュレーションを使用することにより、新しい属性を作成することができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-111">You can create new attributes by using the Headquarters configurations.</span></span> <span data-ttu-id="527f5-112">データベースの変更は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="527f5-112">No database changes are required.</span></span> <span data-ttu-id="527f5-113">以前は、バックオフィスとチャンネル データベースで新しいテーブルを作成するには、それらのテーブルを変更する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="527f5-113">Previously, you had to create new tables in Headquarters and the channel database, and then modify those tables.</span></span>

## <a name="why-and-when-you-should-order-attributes"></a><span data-ttu-id="527f5-114">注文属性が必要な理由および場合</span><span class="sxs-lookup"><span data-stu-id="527f5-114">Why and when you should order attributes</span></span>

<span data-ttu-id="527f5-115">現金売りトランザクション、顧客注文、またはコールセンターの注文に新しいフィールドを追加し、POS またはバックオフィスで情報をキャプチャする場合は、注文属性を使用します。</span><span class="sxs-lookup"><span data-stu-id="527f5-115">If you want to add new fields to cash-and-carry transactions, customer orders, or call center orders, and if you want to capture the information in the POS or Headquarters, use order attributes.</span></span> <span data-ttu-id="527f5-116">以前は、現金売りトランザクション (トランザクション ヘッダーまたは行) または POS の顧客注文に新しいフィールドを追加するには、バックオフィスとチャネル データベースで新しい拡張テーブルを作成し、CRT および POS コードにインライン変更を加えて各種画面および操作を処理する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="527f5-116">Previously, to add a new field to a cash-and-carry transaction (transaction header or lines) or a customer order in the POS, you had to create a new extension table in Headquarters and the channel database, and then make inline changes to CRT and POS code to handle the various screens and operations.</span></span> <span data-ttu-id="527f5-117">また、チャネル データベースとバックオフィス間でデータを同期するように Commerce Data Exchange を構成する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="527f5-117">You also had to configure Commerce Data Exchange to synchronize the data between the channel database and Headquarters.</span></span> <span data-ttu-id="527f5-118">ただし、注文属性はコンフィギュレーションを通してこれらすべてのアクションを完了できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-118">However, order attributes now let you complete all these actions through configuration.</span></span> <span data-ttu-id="527f5-119">コードを記述またはカスタム拡張機能テーブルを作成する必要はありませんが、主要なビジネス ロジックおよび POS UI を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="527f5-119">You don't have to write any code or create custom extension tables, but you still need to create the core business logic and the POS UI.</span></span>

<span data-ttu-id="527f5-120">この最初のバージョンは **String** 属性タイプのみをサポートしますが、将来のバージョンは他の属性タイプをサポートします。</span><span class="sxs-lookup"><span data-stu-id="527f5-120">This first version supports only the **String** attribute type, but future versions will support other attribute types.</span></span> <span data-ttu-id="527f5-121">データをマスター テーブルから取得し、そのデータに X++ の複雑な検索ロジックとコア ビジネス ロジックが必要な場合は、拡張プロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="527f5-121">If you want the data to come from the master table, and that data involves complex search logic and core business logic in X++, you should use extension properties.</span></span>

> [!NOTE]
> <span data-ttu-id="527f5-122">顧客注文および現金店頭払いのトランザクションでのみ属性がサポートされます。他のトランザクション タイプはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="527f5-122">We only support attributes on customer orders and cash-and-carry transactions, no other transaction types are supported.</span></span>

## <a name="define-attribute-types"></a><span data-ttu-id="527f5-123">属性タイプを定義</span><span class="sxs-lookup"><span data-stu-id="527f5-123">Define attribute types</span></span>

<span data-ttu-id="527f5-124">最初に、属性タイプを定義し、それに有効な範囲を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="527f5-124">First, you must define the attribute types and assign valid ranges to them.</span></span>

1. <span data-ttu-id="527f5-125">**製品情報管理** > **設定** > **カテゴリと属性** > **属性タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-125">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attribute types**.</span></span>
2. <span data-ttu-id="527f5-126">**属性タイプ**ページで、**新規**を選択し、新しい属性タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-126">On the **Attribute types** page, select **New** to add a new attribute type.</span></span>
3. <span data-ttu-id="527f5-127">階層タイプ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-127">Enter a name for the attribute type.</span></span>
4. <span data-ttu-id="527f5-128">**一般**クイック タブの、**タイプ**フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-128">On the **General** FastTab, in the **Type** field, select the type of data that can be entered for attributes that are assigned to this data type.</span></span>
5. <span data-ttu-id="527f5-129">属性タイプが**少数点**または**整数**の場合、測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-129">If the attribute type is **Decimal** or **Integer**, select a unit of measure.</span></span>
6. <span data-ttu-id="527f5-130">属性の型が**テキスト**である場合は、それを固定値の一覧を定義できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-130">If the attribute type is **Text**, you can define a fixed list of values for it.</span></span> <span data-ttu-id="527f5-131">**固定リスト** チェック ボックスをオンにし、**値**クイック タブで、値の一覧を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-131">Select the **Fixed list** check box, and then, on the **Values** FastTab, enter the list of values.</span></span>
7. <span data-ttu-id="527f5-132">属性タイプに有効な値の範囲を定義するには、**値の範囲**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="527f5-132">To define a range of valid values for the attribute type, select the **Value range** check box.</span></span> <span data-ttu-id="527f5-133">次に、**範囲**クイックタブで、値の有効範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-133">Then, on the **Range** FastTab, enter the valid range of values.</span></span>

## <a name="define-the-attributes"></a><span data-ttu-id="527f5-134">属性の定義</span><span class="sxs-lookup"><span data-stu-id="527f5-134">Define the attributes</span></span> 

<span data-ttu-id="527f5-135">次に、属性を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="527f5-135">Next, you must define the attributes.</span></span> <span data-ttu-id="527f5-136">定義する各属性に対して、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="527f5-136">Follow these steps for each attribute that you want to define.</span></span>

1. <span data-ttu-id="527f5-137">**製品情報管理** > **設定** > **カテゴリと属性** > **属性**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-137">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attributes**.</span></span>
2. <span data-ttu-id="527f5-138">**属性**ページで、**新規**を選択し、新しい属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-138">On the **Attributes** page, select **New** to add a new attribute.</span></span>
3. <span data-ttu-id="527f5-139">属性の名前、フレンドリ名、および説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-139">Enter a name, friendly name, and description for the attribute.</span></span> <span data-ttu-id="527f5-140">また、属性にユーザーを表示する必要があるヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-140">Additionally, enter any Help text that should be shown to the user for the attribute.</span></span>
4. <span data-ttu-id="527f5-141">**属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-141">In the **Attribute type** field, select the attribute type to assign to the attribute.</span></span>
5. <span data-ttu-id="527f5-142">属性タイプに応じて、**既定値**フィールドに、属性がチャネルに割り当てられたときに既定で表示される値または値の範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-142">Depending on the attribute type, in the **Default value** field, enter the value or range of values that is shown by default when the attribute is assigned to a channel.</span></span>
6. <span data-ttu-id="527f5-143">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-143">Select **Translate**.</span></span> <span data-ttu-id="527f5-144">その後、**テキストの翻訳**ページで、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-144">Then, on the **Text translation** page, enter the name, description, friendly name, and Help text for the attribute in additional languages.</span></span>

## <a name="define-attribute-groups"></a><span data-ttu-id="527f5-145">属性グループの定義</span><span class="sxs-lookup"><span data-stu-id="527f5-145">Define attribute groups</span></span>

1. <span data-ttu-id="527f5-146">**製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-146">Go to **Product information management** > **Setup** > **Categories and attributes** > **Attribute groups**.</span></span>
2. <span data-ttu-id="527f5-147">**属性グループ**ページで、**新規**を選択し、新しい属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-147">On the **Attribute groups** page, select **New** to add a new attribute group.</span></span>
3. <span data-ttu-id="527f5-148">属性グループ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-148">Enter a name for the attribute group.</span></span> <span data-ttu-id="527f5-149">その後、**全般**クイックタブで、属性グループのフレンドリ名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-149">Then, on the **General** FastTab, enter a friendly name, a description, and any Help text for the attribute group.</span></span>
4. <span data-ttu-id="527f5-150">**属性**クイック タブで、**追加**を選択して、属性グループに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-150">On the **Attributes** FastTab, select **Add** to add attributes to the attribute group.</span></span> <span data-ttu-id="527f5-151">**既定値**フィールドでは、選択した属性の既定値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-151">In the **Default value** field, you can enter a default value for the selected attributes.</span></span>
5. <span data-ttu-id="527f5-152">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-152">Select **Translate**.</span></span> <span data-ttu-id="527f5-153">その後、**テキストの翻訳**ページで、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-153">Then, on the **Text translation** page, enter the description, friendly name, and Help text for the attribute group in additional languages.</span></span>

## <a name="link-the-attribute-group-to-the-channel"></a><span data-ttu-id="527f5-154">属性グループのチャネルへのリンク</span><span class="sxs-lookup"><span data-stu-id="527f5-154">Link the attribute group to the channel</span></span>

1. <span data-ttu-id="527f5-155">**Retail とコマース** > **チャネル** > **店舗** > **すべての店舗**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-155">Go to **Retail and Commerce** > **Channels** > **Stores** > **All stores**.</span></span>
2. <span data-ttu-id="527f5-156">**チャネル** ページの属性をリンクする必要があるチャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-156">Select the channel that the attributes on the **Channel** page should be linked to.</span></span>
3. <span data-ttu-id="527f5-157">**設定**タブで、**属性グループ**の**販売注文属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-157">On the **Set up** tab, select **Sales order attributes** under **Attribute group**.</span></span>
4. <span data-ttu-id="527f5-158">**販売注文属性グループ**ページで、**新規**を選択し、属性グループをチャネルにリンクします。</span><span class="sxs-lookup"><span data-stu-id="527f5-158">On the **Sales order attribute groups** page, select **New** to link the attribute group to the channel.</span></span>
5. <span data-ttu-id="527f5-159">**名前**フィールドで属性グループを選択してチャネルにリンクします。</span><span class="sxs-lookup"><span data-stu-id="527f5-159">In the **Name** field, select the attribute group to link to the channel.</span></span>
6. <span data-ttu-id="527f5-160">**属性の適用先**フィールドで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-160">In the **Apply attributes to** field, select one of the following options:</span></span>

    - <span data-ttu-id="527f5-161">**ヘッダー** – 属性は、トランザクション ヘッダーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-161">**Header** – The attributes will apply only to the transaction header.</span></span>
    - <span data-ttu-id="527f5-162">**明細行** – 属性は、トランザクション明細行にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-162">**Lines** – The attribute will apply only to the transaction lines.</span></span>
    - <span data-ttu-id="527f5-163">**既定** - 属性は、トランザクション ヘッダーとトランザクション明細行の両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-163">**Default** – The attribute will apply to both the transaction header and the transaction lines.</span></span>

7. <span data-ttu-id="527f5-164">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-164">Select **Save**.</span></span>

## <a name="run-the-distribution-jobs"></a><span data-ttu-id="527f5-165">配送ジョブを実行</span><span class="sxs-lookup"><span data-stu-id="527f5-165">Run the distribution jobs</span></span>

1. <span data-ttu-id="527f5-166">**Retail とコマース** > **Retail とコマース IT** > **配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-166">Go to **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
2. <span data-ttu-id="527f5-167">**製品 (1040)** を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-167">Select **Products (1040)**, and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="527f5-168">メッセージが表示されたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-168">When you're prompted, select **Yes**.</span></span> <span data-ttu-id="527f5-169">このステップは、新しい属性、属性タイプ、または属性グループを追加した場合にのみ必要です。</span><span class="sxs-lookup"><span data-stu-id="527f5-169">This step is required only if you added any new attributes, attribute types, or attribute groups.</span></span>
3. <span data-ttu-id="527f5-170">**チャネル コンフィギュレーション ジョブ (1070)** を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-170">Select **Channel configuration job (1070)**, and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="527f5-171">メッセージが表示されたら、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-171">When you're prompted, select **Yes**.</span></span>

## <a name="show-order-attributes-in-the-pos-transaction-screen-using-the-attribute-control-this-feature-is-available-in-version-813-and-later"></a><span data-ttu-id="527f5-172">属性コントロールを使用して POS トランザクション画面に注文属性を表示します (この機能はバージョン 8.1.3 以降で使用できます)。</span><span class="sxs-lookup"><span data-stu-id="527f5-172">Show order attributes in the POS transaction screen using the Attribute control (this feature is available in version 8.1.3 and later)</span></span>

### <a name="headquarters"></a><span data-ttu-id="527f5-173">バックオフィス</span><span class="sxs-lookup"><span data-stu-id="527f5-173">Headquarters</span></span>

1. <span data-ttu-id="527f5-174">**Retail とコマース > チャネル設定 > POS 設定 > POS > 画面レイアウト**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-174">Select **Retail and Commerce > Channel setup > POS Setup > POS > Screen layouts**.</span></span>
2. <span data-ttu-id="527f5-175">画面レイアウトページで、**新規**をクリックして新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-175">On the screen layout page, click **New** to create a new screen layout, or select an existing screen layout.</span></span>
3. <span data-ttu-id="527f5-176">スクリーン レイアウトの名前と ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="527f5-176">Enter the ID and name for the screen layout.</span></span>
4. <span data-ttu-id="527f5-177">**レイアウト サイズ** クイック タブで、**追加**ボタン選択して、POS の新しいレイアウト サイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-177">On the **Layout sizes** FastTab, select the **Add** button to add new layout sizes for the POS.</span></span>
5. <span data-ttu-id="527f5-178">**名前**フィールドで POS 画面の解像度を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-178">In the **Name** field, select the POS screen resolution.</span></span>
6. <span data-ttu-id="527f5-179">**レイアウト サイズ** クイック タブで、**レイアウト デザイナー** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="527f5-179">On the **Layout sizes** FastTab, click the **Layout designer** button.</span></span>
7. <span data-ttu-id="527f5-180">プロンプトが表示されたら、**はい**を選択して、**インストール/実行**ボタンを使用してデザイナー ホストをダウンロードおよびインストールします。</span><span class="sxs-lookup"><span data-stu-id="527f5-180">If you're prompted, select **Yes** to download and install the Designer Host by using the **Install/Run** button.</span></span>
8. <span data-ttu-id="527f5-181">入力を求めるメッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-181">When you're prompted, enter the Microsoft Dynamics 365 user name and password to start the designer.</span></span>
9. <span data-ttu-id="527f5-182">デザイナーが開始されたら、属性パネルを画面レイアウト デザイナー内の任意の場所にドラッグし、画面の幅に従ってサイズを調整します。</span><span class="sxs-lookup"><span data-stu-id="527f5-182">After the designer is started, drag the Attributes panel anywhere in the screen layout designer and adjust the size according to your screen width.</span></span>
10. <span data-ttu-id="527f5-183">完了したら、**OK**を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="527f5-183">When you've finished, select **OK** to save your changes.</span></span>
11. <span data-ttu-id="527f5-184">右上隅の **閉じる** ボタン (X) をクリックし、画面レイアウト デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="527f5-184">Close the screen layout designer by clicking the **Close** button (X) in the upper-right corner.</span></span> <span data-ttu-id="527f5-185">メッセージが表示されたら、**はい**を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="527f5-185">When you're prompted, select **Yes** to save your changes.</span></span>
12. <span data-ttu-id="527f5-186">**Retail とコマース > Retail とコマース IT > 配送スケジュール**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-186">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule**.</span></span>
13. <span data-ttu-id="527f5-187">レジスター ジョブ (1090) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-187">Select the Registers job (1090), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="527f5-188">メッセージが表示されたら、はい を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-188">When you're prompted, select Yes.</span></span>

### <a name="pos"></a><span data-ttu-id="527f5-189">POS</span><span class="sxs-lookup"><span data-stu-id="527f5-189">POS</span></span>

1. <span data-ttu-id="527f5-190">POS を起動し、任意の品目をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-190">Start POS, and add any item to a transaction.</span></span> <span data-ttu-id="527f5-191">ヘッダーと明細行の両方のコンフィギュレーション済の属性と共に、トランザクション画面に属性パネルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-191">You should see the Attribute panel in the transaction screen with the configured attributes both for header and lines.</span></span>
2. <span data-ttu-id="527f5-192">属性パネルで **編集** アイコンをクリックして、属性の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="527f5-192">Click the **Edit** icon in the attribute panel to update the attribute value.</span></span>
3. <span data-ttu-id="527f5-193">属性パネルでヘッダーまたは明細行タブをクリックして、ヘッダーまたは明細行の属性パネルを表示します。</span><span class="sxs-lookup"><span data-stu-id="527f5-193">Click the header or lines tab in the attribute panel to view the header or lines attribute.</span></span> 
4. <span data-ttu-id="527f5-194">明細行の属性は、トランザクションで選択した明細行に基づいて自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-194">The lines attribute will refresh automatically based on the lines selected in the transaction.</span></span>

## <a name="set-attribute-values-for-call-center-orders"></a><span data-ttu-id="527f5-195">コール センターの注文の属性値を設定</span><span class="sxs-lookup"><span data-stu-id="527f5-195">Set attribute values for call center orders</span></span>

<span data-ttu-id="527f5-196">チャンネルの注文属性を構成した後、**顧客サービス**または**すべての販売注文**、およびコール センターの新しい注文を作成します。</span><span class="sxs-lookup"><span data-stu-id="527f5-196">After you configure the order attributes for the channel, go to **Customer service** or **All Sales orders**, and create a new call center order.</span></span>

1. <span data-ttu-id="527f5-197">顧客注文の作成後または作成中に、トランザクション ヘッダーの属性値を設定する場合は、アクション ウィンドウで、**コマース** タブに移動し、**小売属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-197">After or during the creation of a customer order, if you want to set an attribute value for the transaction header, on the Action Pane, go to the **Commerce** tab, select **Attributes**.</span></span>
2. <span data-ttu-id="527f5-198">**販売注文属性値**ページで、属性値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-198">On the **Sales order attributes values** page, you can set the values for the attributes.</span></span> <span data-ttu-id="527f5-199">このページの属性のリストは、チャネル用にコンフィギュレーションした属性グループに基づいています。</span><span class="sxs-lookup"><span data-stu-id="527f5-199">The list of attributes on this page is based on the attribute group that you configured for the channel.</span></span>
3. <span data-ttu-id="527f5-200">行レベルで属性値を設定するには、**販売注文**ページで **行**ビューを選択し、属性値を設定する行を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-200">To set attribute values at the line level, on the **Sales order** page, select the **Lines** view, and then select the line to set the attribute value for.</span></span> <span data-ttu-id="527f5-201">**販売注文明細行グループ**で、**Retail とコマース** > **属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-201">Under **Sales order lines group**, select **Retail and Commerce** > **Attributes**.</span></span>
4. <span data-ttu-id="527f5-202">値を設定するすべての販売明細行に対して手順 3 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="527f5-202">Repeat step 3 for all the sales lines that you want to set the values for.</span></span>

## <a name="view-the-attributes-values-for-cash-and-carry-transactions-in-headquarters"></a><span data-ttu-id="527f5-203">バックオフィスでの現金売りトランザクションの属性値の表示</span><span class="sxs-lookup"><span data-stu-id="527f5-203">View the attributes values for cash-and-carry transactions in Headquarters</span></span>

<span data-ttu-id="527f5-204">配送ジョブを実行し、バックオフィスに現金売りトランザクションを収集した後、トランザクションの属性値を表示できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-204">After you've run the distribution job and pulled a cash-and-carry transaction into Headquarters, you can view the attribute values for that transaction.</span></span> <span data-ttu-id="527f5-205">POS は、注文の属性を表示するための UI を提供しません。</span><span class="sxs-lookup"><span data-stu-id="527f5-205">The POS doesn't provide a UI for viewing order attributes.</span></span> <span data-ttu-id="527f5-206">したがって、注文の属性値を表示するには、POS を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="527f5-206">Therefore, to view the order attribute values, you must extend the POS.</span></span>

1. <span data-ttu-id="527f5-207">**Retail とコマース** > **照会およびレポート** > **店舗のトランザクション**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="527f5-207">Go to **Retail and Commerce** > **Inquires and reports** > **Store transactions**.</span></span>
2. <span data-ttu-id="527f5-208">トランザクション ヘッダー属性を表示するには、アクション ウィンドウで**属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-208">To view the transaction header attributes, on the Action Pane, select **Attributes**.</span></span>
3. <span data-ttu-id="527f5-209">トランザクション ヘッダー行の属性を表示するには、アクション ウィンドウで **トランザクション** > **販売トランザクション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="527f5-209">To view the transaction lines attributes, on the Action Pane, select **Transaction** > **Sales transaction**.</span></span>
4. <span data-ttu-id="527f5-210">**販売トランザクション**ページで、すべての明細行を選択し、アクション ウィンドウで、**属性**を選択して、明細行の属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="527f5-210">On the **Sales transactions** page, select any line, and then, on the Action Pane, select **Attributes** to view the line attributes.</span></span>

> [!NOTE]
> <span data-ttu-id="527f5-211">あなたの属性グループの一部として構成され、チャンネルにリンクされている属性のみ、バックオフィス UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-211">Only the attributes that are configured as part of your attribute group and linked to the channel will appear in the Headquarters UI.</span></span>

## <a name="extend-attributes-to-add-business-logic-in-crt"></a><span data-ttu-id="527f5-212">CRT でビジネス ロジックを追加するには、属性を拡張します。</span><span class="sxs-lookup"><span data-stu-id="527f5-212">Extend attributes to add business logic in CRT</span></span>

<span data-ttu-id="527f5-213">Retail SDK に追加された新しいサンプルでは、CRT の注文属性のビジネス ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-213">A new sample that has been added to the Retail SDK adds business logic for order attributes in CRT.</span></span> <span data-ttu-id="527f5-214">この例には、ビジネス ロジックのコードのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="527f5-214">This sample includes code only for the business logic.</span></span> <span data-ttu-id="527f5-215">属性に対する読み取りおよび書き込み処理は自動化されているため、属性を保存したり読み取ったりする方法は示しません。</span><span class="sxs-lookup"><span data-stu-id="527f5-215">It doesn't show how to save or read the attributes, because read and write operations for attributes are automated.</span></span>

<span data-ttu-id="527f5-216">このサンプルでは、次のシナリオを実装しています。カートを中断するには、属性値を設定します。</span><span class="sxs-lookup"><span data-stu-id="527f5-216">The sample implements the following scenario: When you suspend a cart, you set an attribute value.</span></span> <span data-ttu-id="527f5-217">カートを再開するとき、その値を消去します。</span><span class="sxs-lookup"><span data-stu-id="527f5-217">When you resume the cart, you want to clear that value.</span></span> <span data-ttu-id="527f5-218">事前トリガーが **SuspendCartRequest** に追加され、ビジネス ロジックが記述されました。</span><span class="sxs-lookup"><span data-stu-id="527f5-218">A pre-trigger was added for **SuspendCartRequest**, and the business logic was written.</span></span> <span data-ttu-id="527f5-219">CRT で任意のトリガーを拡張または任意の要求をオーバーライドして、シナリオに基づきロジックをセットすることができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-219">You can extend any trigger or override any request in CRT to set the logic, based on your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="527f5-220">カートに属性を追加する前に、カートまたはカート行にその属性が既に存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="527f5-220">Before adding attribute to the cart, check whether the attribute already exists in the cart or cartline.</span></span> <span data-ttu-id="527f5-221">属性が既に存在する場合は、その属性を再度追加するのではなく、更新します。</span><span class="sxs-lookup"><span data-stu-id="527f5-221">If the attribute already exists, then don’t add the attribute again, instead update it.</span></span> <span data-ttu-id="527f5-222">カートまたはカート行に重複属性を追加すると、CRT にランタイム エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-222">If a duplicate attribute is added to the cart or cartline, then CRT will display a runtime error.</span></span> <span data-ttu-id="527f5-223">このシナリオのサンプル コードは、次のサンプル コード セクションで参照できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-223">Sample code for this scenario can be found in sample code section below.</span></span>


<span data-ttu-id="527f5-224">完全なサンプル コードは Retail SDK\\SampleExtensions\\CommerceRuntime\\Extensions.TransactionAttributesSample の Retail SDK で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-224">You can find the full sample code in the Retail SDK at Retail SDK\\SampleExtensions\\CommerceRuntime\\Extensions.TransactionAttributesSample.</span></span>

- <span data-ttu-id="527f5-225">新しい C# ポータブル クラス ライブラリ プロジェクトを作成し、次のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="527f5-225">Create a new C# portable class library project, and paste in the following code.</span></span>

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
        // Sample code to check for the duplicate attribute, before adding attributes to the cart check whether the attribute already exists if so then don’t add the attribute again, instead update it.
        
        public static class CustomCartHelper
        {
            /// <summary>
            /// Updates the transaction header attribute.
            /// </summary>
            /// <param name="cart">The cart.</param>
            /// <param name="reserveNow">The value of the transaction header attribute.</param>
            /// <param name="updateAttribute">A flag indicating whether or not to override an existing attribute value.</param>
            /// <returns>A flag indication whether or not the cart was updated.</returns>
            public static bool CreateUpdateTransactionHeaderAttribute(Cart cart, bool reserveNow, bool updateAttribute)
            {
                ThrowIf.Null(cart, "cart");
                bool cartUpdated = false;
                IList<AttributeValueBase> transactionAttributes = cart.AttributeValues;
                string reserveNowAttributeName = "Reserve now";
                string reserveNowAttributeValue = reserveNow ? "Yes" : "No";
                AttributeValueBase reserveNowAttribute = transactionAttributes.SingleOrDefault(attribute => attribute.Name.Equals(reserveNowAttributeName));

                if (reserveNowAttribute == null)
                {
                    transactionAttributes.Add(new AttributeTextValue() { Name = reserveNowAttributeName, TextValue = reserveNowAttributeValue });
                    cartUpdated = true;
                }
                else if (updateAttribute && !((AttributeTextValue)reserveNowAttribute).TextValue.Equals(reserveNowAttributeValue))
                {
                    ((AttributeTextValue)reserveNowAttribute).TextValue = reserveNowAttributeValue;
                    cartUpdated = true;
                }

                return cartUpdated;
            }
        }
```

## <a name="extend-attributes-to-do-some-business-logic-in-the-pos"></a><span data-ttu-id="527f5-226">POS でビジネス ロジックを行うには、属性を拡張します。</span><span class="sxs-lookup"><span data-stu-id="527f5-226">Extend attributes to do some business logic in the POS</span></span>

> [!NOTE]
> <span data-ttu-id="527f5-227">バージョン 8.1.2 以降でアプリケーションを実行している場合にのみ、次の変更が必要です。</span><span class="sxs-lookup"><span data-stu-id="527f5-227">The following changes are required only if you are running the application with version 8.1.2 or earlier.</span></span> <span data-ttu-id="527f5-228">8.1.3 以降は、新しい属性パネルを使用して、POS で属性の値を設定または更新できます。</span><span class="sxs-lookup"><span data-stu-id="527f5-228">Starting in 8.1.3, you can use the new Attributes panel to set or update the attribute value in POS.</span></span> <span data-ttu-id="527f5-229">このコントロールでは、POS で属性値を設定するために追加のコードを記述したり、UI を作成したりする必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="527f5-229">With this control you no longer  need to write any additional code or create UI to set the attribute value in POS.</span></span> <span data-ttu-id="527f5-230">属性値を設定または更新するための属性コントロール UI が追加されました。</span><span class="sxs-lookup"><span data-stu-id="527f5-230">In the attribute control UI has been added to set or update the attribute value.</span></span> <span data-ttu-id="527f5-231">詳細については、このドキュメントの**属性コントロールを使用して POS トランザクション画面で注文属性を表示する**セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="527f5-231">Refer to the **Show Order attributes in the POS transaction screen using the Attribute control** section in this document for more details.</span></span>

<span data-ttu-id="527f5-232">Retail SDK に追加された新しいサンプルでは、POS の注文属性のビジネス ロジックを設定します。</span><span class="sxs-lookup"><span data-stu-id="527f5-232">A new sample that has been added to the Retail SDK sets the business logic for order attributes in the POS.</span></span> <span data-ttu-id="527f5-233">この例には、ビジネス ロジックのコードのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="527f5-233">This sample includes code only for the business logic.</span></span> <span data-ttu-id="527f5-234">属性に対する読み取りおよび書き込み処理は自動化されているため、属性の値を保存したり読み取ったりする方法は示しません。</span><span class="sxs-lookup"><span data-stu-id="527f5-234">It doesn't show how to save or read attribute values, because read and write operations for attributes are automated.</span></span> <span data-ttu-id="527f5-235">属性の値は、シナリオに基づき、CRT または POS のいずれかで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-235">You can set the values for attributes in either CRT or the POS, based on your scenario.</span></span> <span data-ttu-id="527f5-236">値が顧客の入力に基づいている場合、POS クライアントで設定します。</span><span class="sxs-lookup"><span data-stu-id="527f5-236">If your values are based on customer input, set them in the POS client.</span></span> <span data-ttu-id="527f5-237">一部のビジネス ロジックが含まれている場合は、CRT で値を設定します。</span><span class="sxs-lookup"><span data-stu-id="527f5-237">If some business logic is involved, set the values in CRT.</span></span>

<span data-ttu-id="527f5-238">このサンプルでは、次のシナリオを実装しています。企業間 (B2B) 注文を作成し、 顧客からのフィードバックに基づいて B2B 属性の値を設定する場合 (**Yes** または **No**)。</span><span class="sxs-lookup"><span data-stu-id="527f5-238">The sample implements the following scenario: You create a business-to-business (B2B) order and want to set the B2B attribute value (**Yes** or **No**), based on customer input.</span></span> <span data-ttu-id="527f5-239">**PreEndTransactionTrigger** は値を設定するために POS で拡張されました。</span><span class="sxs-lookup"><span data-stu-id="527f5-239">**PreEndTransactionTrigger** was extended in the POS to set the values.</span></span> <span data-ttu-id="527f5-240">必要に応じて任意の POS トリガーを拡張、または要求をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-240">You can extend any POS trigger or override the request as appropriate.</span></span>

<span data-ttu-id="527f5-241">完全なサンプル コードは Retail SDK\\POS\\Extensions\\B2BSample の Retail SDK で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="527f5-241">You can find the full sample code in the Retail SDK at Retail SDK\\POS\\Extensions\\B2BSample.</span></span>

> [!NOTE]
> <span data-ttu-id="527f5-242">そのコードに属性と属性値を設定または追加した場合でも、構成された属性のみバックオフィス UI に表示されます。</span><span class="sxs-lookup"><span data-stu-id="527f5-242">Only the configured attributes will appear in the Headquarters UI, even if you set or add attributes and attribute values in the code.</span></span> <span data-ttu-id="527f5-243">属性が、チャンネルにリンクされている属性グループに属さない場合は、バックオフィス UI に反映されません。</span><span class="sxs-lookup"><span data-stu-id="527f5-243">If an attribute isn't part of the attribute group that you linked to the channel, it won't appear in the Headquarters UI.</span></span>

1. <span data-ttu-id="527f5-244">Retail SDK から **ModernPOS.sln\\CloudPos.sln** を開きます。</span><span class="sxs-lookup"><span data-stu-id="527f5-244">From the Retail SDK, open **ModernPOS.sln\\CloudPos.sln**.</span></span>
2. <span data-ttu-id="527f5-245">Retail SDK で、**POS.Extension** プロジェクトに新しい拡張フォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="527f5-245">In the Retail SDK, create a new extension folder under the **POS.Extension** project.</span></span>
3. <span data-ttu-id="527f5-246">新しい拡張フォルダーに、新しい **manifest.json** ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-246">In the new extension folder, add a new **manifest.json** file.</span></span>
4. <span data-ttu-id="527f5-247">次のコードに貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="527f5-247">Paste in the following code.</span></span>

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
5.  <span data-ttu-id="527f5-248">新しい TypeScript ファイルを作成して **PreEndTransactionTrigger** を実装し、次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="527f5-248">Create a new TypeScript file to implement **PreEndTransactionTrigger**, and add the following code.</span></span>

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
