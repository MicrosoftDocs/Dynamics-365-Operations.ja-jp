---
title: "顧客属性"
description: "このトピックでは、顧客属性に関する情報を提供し、構成を使用して顧客のマスター レコードに新しいフィールドを追加する方法について説明します。"
author: mugunthanm
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations, Retail
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dc2e5c36e8e750c0100c546ad01dfbb2e87afa38
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="customer-attributes"></a><span data-ttu-id="bdb61-103">顧客属性</span><span class="sxs-lookup"><span data-stu-id="bdb61-103">Customer attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdb61-104">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、小売用バックオフィスの属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="bdb61-104">We extended the attribute framework in Retail headquarters to support attributes for customers, customer orders, cash-and-carry transactions, and call center orders.</span></span>

> [!NOTE]
> <span data-ttu-id="bdb61-105">属性は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="bdb61-105">The attributes are read-only.</span></span> <span data-ttu-id="bdb61-106">ただし、顧客や注文属性の場合は、個々の顧客または注文のレベルで値を編集および設定できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-106">However, in the case of customer or order attributes, you can edit and set values at the level of the individual customer or order.</span></span>

<span data-ttu-id="bdb61-107">新しい顧客属性フレームワークでは、コンフィギュレーションを使用して顧客マスター レコードに新しい項目を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-107">The new customer attribute framework lets you use configurations to add new fields to the customer master record.</span></span> <span data-ttu-id="bdb61-108">これらのフィールドは販売時点管理 (POS) または小売用バックオフィスの **顧客の追加/編集** または **顧客の詳細** 画面に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-108">Those fields then automatically appear on the **Customer add/edit** or **Customer details** screen in Point of Sale (POS) or Retail headquarters.</span></span> <span data-ttu-id="bdb61-109">小売パラメーターの顧客属性グループを構成すると、POS と小売用バックオフィスは自動的に新しい属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-109">After you configure the customer attribute group in the Retail parameters, POS and Retail headquarters automatically show the new attribute.</span></span> <span data-ttu-id="bdb61-110">コードの変更またはカスタマイズは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="bdb61-110">No code change or customization is required.</span></span> <span data-ttu-id="bdb61-111">また、画面レイアウト デザイナーを使用して、POS トランザクション画面に顧客の属性が表示されるように顧客カードを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-111">You can also use the screen layout designer to configure the customer card on the POS transaction screen so that it shows the customer attributes.</span></span>

## <a name="why-and-when-you-should-configure-customer-attributes"></a><span data-ttu-id="bdb61-112">顧客属性の構成が必要な理由および場合</span><span class="sxs-lookup"><span data-stu-id="bdb61-112">Why and when you should configure customer attributes</span></span>

<span data-ttu-id="bdb61-113">顧客のマスター レコードに新しいフィールドを追加して、POS または小売用バック オフィスで情報を取得する場合は、この機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-113">If you want to add new fields to the customer master record, and capture the information in POS or Retail headquarters, you can use this feature.</span></span> <span data-ttu-id="bdb61-114">以前は、顧客マスター レコードをに新しいフィールドを追加して POS および小売用バックオフィスに表示するには、小売用バックオフィスおよびチャネル データベースで新しい拡張テーブルを作成し、Commerce Runtime (CRT) および POS コードでインライン変更を加える必要がありました。</span><span class="sxs-lookup"><span data-stu-id="bdb61-114">Previously, to add a new field to the customer master record and show it in POS and Retail headquarters, you had to create a new extension table in Retail headquarters and the channel database, and make inline modifications to Commerce runtime (CRT) and POS code.</span></span> <span data-ttu-id="bdb61-115">拡張フィールドへの読み取り/書き込みを行い POS で表示するには、CRT および POS でコードを記述する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="bdb61-115">You had to write code in CRT and POS to read/write to the extension fields and show them in POS.</span></span> <span data-ttu-id="bdb61-116">**顧客の詳細** 画面およびトランザクション画面の **顧客** パネルなど、さまざまな POS ビューやシナリオでこれを処理する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="bdb61-116">You had to handle this in various POS views and scenarios, such as the **Customer details** screen and the **Customer** panel on the transaction screen.</span></span> <span data-ttu-id="bdb61-117">さらに、CRT で、挿入、選択、および更新のすべての操作を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdb61-117">In addition, in CRT, you had to handle all insert, select, and update operations.</span></span> <span data-ttu-id="bdb61-118">ただし、新しい機能では、コンフィギュレーションを通してこれらすべての手順を完了することができます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-118">However, the new functionality lets you complete all these steps through configuration.</span></span> <span data-ttu-id="bdb61-119">小売用バック オフィスまたはチャンネル データベースでコードを記述またはカスタム拡張機能テーブルを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="bdb61-119">You don't have to write any code or create custom extension tables in Retail headquarters or the channel database.</span></span>

<span data-ttu-id="bdb61-120">この機能の最初のバージョンは、**datetime** および **reference** 属性タイプをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="bdb61-120">The first version of this functionality doesn't support **datetime** and **reference** attribute types.</span></span> <span data-ttu-id="bdb61-121">それらの属性タイプについては、POS に詳細を表示するのに、拡張機能プロパティおよびカスタム コントロールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdb61-121">For those attribute types, you should use extension properties and custom controls to show the details in POS.</span></span>

## <a name="configure-customer-attributes-in-pos-and-retail-headquarters"></a><span data-ttu-id="bdb61-122">POS および小売用バックオフィスで顧客属性をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="bdb61-122">Configure customer attributes in POS and Retail headquarters</span></span>

### <a name="define-attribute-types"></a><span data-ttu-id="bdb61-123">属性タイプを定義</span><span class="sxs-lookup"><span data-stu-id="bdb61-123">Define attribute types</span></span>

1. <span data-ttu-id="bdb61-124">**製品情報管理** > **設定** &gt; **カテゴリと属性** > **属性タイプ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-124">Select **Product information management** > **Setup** &gt; **Categories and attributes** > **Attribute types**.</span></span>
2. <span data-ttu-id="bdb61-125">**属性タイプ**ページで、**新規**を選択し、新しい属性タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-125">On the **Attribute types** page, select **New** to add a new attribute type.</span></span>
3. <span data-ttu-id="bdb61-126">階層タイプ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-126">Enter a name for the attribute type.</span></span>
4. <span data-ttu-id="bdb61-127">**一般**クイック タブの、**タイプ**フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-127">On the **General** FastTab, in the **Type** field, select the type of data that can be entered for attributes that are assigned to this data type.</span></span>
5. <span data-ttu-id="bdb61-128">属性タイプが**少数点**または**整数**の場合、測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-128">If the attribute type is **Decimal** or **Integer**, select a unit of measure.</span></span>
6. <span data-ttu-id="bdb61-129">属属性タイプの固定値リストを定義するには、**固定値リスト** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bdb61-129">To define a fixed list of values for the attribute type, select the **Fixed list** check box.</span></span> <span data-ttu-id="bdb61-130">次に、**値** クイックタブで、値のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-130">Then, on the **Values** FastTab, add the list of values.</span></span>

    > [!NOTE]
    > <span data-ttu-id="bdb61-131">**固定リスト** チェック ボックスは、**テキスト** 属性タイプでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-131">The **Fixed list** check box is available only for the **Text** attribute type.</span></span>

    <span data-ttu-id="bdb61-132">または、属性タイプに有効な値の範囲を定義するには**値の範囲**チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-132">Alternatively, to define a range of valid values for the attribute type, select the **Value range** check box.</span></span> <span data-ttu-id="bdb61-133">次に、**範囲** クイックタブで、値の有効範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-133">Then, on the **Range** FastTab, enter the valid range of values.</span></span>

### <a name="define-attributes"></a><span data-ttu-id="bdb61-134">属性の定義</span><span class="sxs-lookup"><span data-stu-id="bdb61-134">Define attributes</span></span>

1. <span data-ttu-id="bdb61-135">**製品情報管理** > **設定** > **カテゴリと属性** > **属性**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-135">Select **Product information management** > **Setup** > **Categories and attributes** > **Attributes**.</span></span>
2. <span data-ttu-id="bdb61-136">**属性**ページで、**新規**を選択し、新しい属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-136">On the **Attributes** page, select **New** to add a new attribute.</span></span>
3. <span data-ttu-id="bdb61-137">属性にユーザーを表示する必要がある名前、フレンドリ名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-137">Enter the name, friendly name, description, and any Help text that should be shown to the user for the attribute.</span></span>
4. <span data-ttu-id="bdb61-138">**属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-138">In the **Attribute type** field, select the attribute type to assign to the attribute.</span></span>
5. <span data-ttu-id="bdb61-139">属性タイプに応じて、**既定値**フィールドに、この属性が顧客に割り当てられたときに既定で表示される値または値の範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-139">Depending on the attribute type, in the **Default value** field, enter the value or the range of values that is shown by default when this attribute is assigned to a customer.</span></span>
6. <span data-ttu-id="bdb61-140">**翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-140">Select **Translate** to open the **Text translation** page, where you can enter the name, description, friendly name, and Help text for the attribute in additional languages.</span></span>
7. <span data-ttu-id="bdb61-141">ステップ 2 ～ 6 を繰り返してさらに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-141">Repeat steps 2 through 6 to add more attributes.</span></span>

### <a name="define-an-attribute-group"></a><span data-ttu-id="bdb61-142">属性グループの定義</span><span class="sxs-lookup"><span data-stu-id="bdb61-142">Define an attribute group</span></span>

1. <span data-ttu-id="bdb61-143">**製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ**の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-143">Select **Product information management** > **Setup** > **Categories and attributes** > **Attribute groups**.</span></span>
2. <span data-ttu-id="bdb61-144">**属性グループ**ページで、**新規**を選択し、新しい属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-144">On the **Attribute groups** page, select **New** to add a new attribute group.</span></span>
3. <span data-ttu-id="bdb61-145">名前を入力し、次に**一般** FastTab で、属性グループのフレンドり名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-145">Enter the name, and then, on the **General** FastTab, enter the friendly name, description, and any Help text for the attribute group.</span></span>
4. <span data-ttu-id="bdb61-146">**属性**クイック タブで、**追加**を選択して、属性グループに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-146">On the **Attributes** FastTab, select **Add** to add attributes to the attribute group.</span></span> <span data-ttu-id="bdb61-147">**既定値**フィールドでは、選択した属性の既定値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-147">In the **Default value** field, you can enter a default value for the selected attributes.</span></span>
5. <span data-ttu-id="bdb61-148">**翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-148">Select **Translate** to open the **Text translation** page, where you can enter the description, friendly name, and Help text for the attribute group in additional languages.</span></span>

### <a name="link-the-attribute-group-to-the-customers-in-the-retail-parameters"></a><span data-ttu-id="bdb61-149">Retail パラメーターでの属性グループの顧客へのリンク</span><span class="sxs-lookup"><span data-stu-id="bdb61-149">Link the attribute group to the customers in the Retail parameters</span></span>

1. <span data-ttu-id="bdb61-150">**小売** > **本社の設定** > **パラメーター** > **小売パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-150">Select **Retail** > **Headquarters setup** > **Parameters** > **Retail parameters**.</span></span>
2. <span data-ttu-id="bdb61-151">**一般**タブの、**顧客属性グループ**フィールドに、属性グループ POS に表示する必要がある属性グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-151">On the **General** tab, in the **Customer attribute group** field, select the attribute group that should be shown in POS.</span></span>

### <a name="run-the-distribution-jobs"></a><span data-ttu-id="bdb61-152">配送ジョブを実行</span><span class="sxs-lookup"><span data-stu-id="bdb61-152">Run the distribution jobs</span></span>

1. <span data-ttu-id="bdb61-153">**小売** > **小売 IT** > **配送スケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-153">Select **Retail** > **Retail IT** > **Distribution schedule**.</span></span>
2. <span data-ttu-id="bdb61-154">**顧客** ジョブ (1010) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-154">Select the **Customers** job (1010), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="bdb61-155">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-155">When you're prompted, select **Yes**.</span></span>
3. <span data-ttu-id="bdb61-156">**グローバル構成** ジョブ (1110) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-156">Select the **Global configuration** job (1110), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="bdb61-157">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-157">When you're prompted, select **Yes**.</span></span>

### <a name="view-customer-attributes"></a><span data-ttu-id="bdb61-158">顧客属性の表示</span><span class="sxs-lookup"><span data-stu-id="bdb61-158">View customer attributes</span></span>

#### <a name="retail-headquarters"></a><span data-ttu-id="bdb61-159">小売用バックオフィス</span><span class="sxs-lookup"><span data-stu-id="bdb61-159">Retail headquarters</span></span>

1. <span data-ttu-id="bdb61-160">**小売** > **顧客** > **すべての顧客** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-160">Select **Retail** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="bdb61-161">アクション ウィンドウの**小売**にある、**属性**セクションで、**小売属性**を選択し属性値を表示または編集します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-161">On the Action Pane, on the **Retail**, in the **Attribute** section, select **Retail attributes** to view or edit the attribute values.</span></span>

#### <a name="pos"></a><span data-ttu-id="bdb61-162">POS</span><span class="sxs-lookup"><span data-stu-id="bdb61-162">POS</span></span>

- <span data-ttu-id="bdb61-163">POS を起動し、**顧客の追加/編集** 画面を開いて顧客の属性値を設定または更新するか、**顧客の詳細** 画面を開いて構成されている属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-163">Start POS, and then either open the **Customer Add/Edit** screen to set or update the attribute values for the customer, or open the **Customer details** screen to view the configured attributes.</span></span>

### <a name="show-customer-attributes-in-the-pos-transaction-screen"></a><span data-ttu-id="bdb61-164">POS トランザクション画面に顧客属性を表示</span><span class="sxs-lookup"><span data-stu-id="bdb61-164">Show customer attributes in the POS transaction screen</span></span>

#### <a name="retail-headquarters"></a><span data-ttu-id="bdb61-165">小売用バックオフィス</span><span class="sxs-lookup"><span data-stu-id="bdb61-165">Retail headquarters</span></span>

1. <span data-ttu-id="bdb61-166">**Retail** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト**と選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-166">Select **Retail** > **Channel setup** > **POS Setup** > **POS** > **Screen layouts**.</span></span>
2. <span data-ttu-id="bdb61-167">**画面レイアウト**ページで、**新規**を選択し新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-167">On the **screen layout** page, select **New** to create a new screen layout, or select an existing screen layout.</span></span>
3. <span data-ttu-id="bdb61-168">スクリーン レイアウトの名前と ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-168">Enter the ID and name for the screen layout.</span></span>
4. <span data-ttu-id="bdb61-169">**レイアウト サイズ**クイック タブで、**追加**ボタン選択して、POS の新しいレイアウト サイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-169">On the **Layout sizes** FastTab, select the **Add** button to add new layout sizes for the POS.</span></span>
5. <span data-ttu-id="bdb61-170">**名前**フィールドで POS 画面の解像度を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-170">In the **Name** field, select the POS screen resolution.</span></span>
6. <span data-ttu-id="bdb61-171">**レイアウト サイズ**クイック タブで、**レイアウト デザイナー**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-171">On the **Layout sized** FastTab, select the **Layout designer** button.</span></span>
7. <span data-ttu-id="bdb61-172">プロンプトが表示されたら、**インストール/実行**ボタンを使用して Retail Designer Host をダウンロードしてインストールするには、**はい**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-172">If you're prompted, select **Yes** to download and install the Retail Designer Host by using the **Install/Run** button.</span></span>
8. <span data-ttu-id="bdb61-173">メッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-173">When you're prompted, enter the Microsoft Dynamics 365 user name and password to start the designer.</span></span>
9. <span data-ttu-id="bdb61-174">デザイナーが開始された後、**顧客**カードを画面レイアウト デザイナーの任意の場所にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="bdb61-174">After the designer is started, drag the **Customer** card anywhere in the screen layout designer.</span></span>
10. <span data-ttu-id="bdb61-175">**顧客** カードを右クリックし、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-175">Right-click the **Customer** card, and then select **Customize**.</span></span>
11. <span data-ttu-id="bdb61-176">**カスタマイズ - 顧客** カードのページが表示されたら、**利用可能な列** セクションで必要な属性を選択してから、右矢印ボタン (**>**) を選択して 、それらを **選択された列** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-176">When the page for the **Customization - Customer** card appears, select the required attributes in the **Available columns** section, and then select the right arrow button (**>**) to move them to the **Selected columns** section.</span></span> <span data-ttu-id="bdb61-177">**上** または **下** ボタンを選択することにより、属性を上または下に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-177">You can move the attributes up or down by selecting the **Up** or **Down** buttons.</span></span>
12. <span data-ttu-id="bdb61-178">完了したら、**OK** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-178">When you've finished, select **OK** to save your changes.</span></span>
13. <span data-ttu-id="bdb61-179">右上隅の**閉じる**ボタン (**X**) を選択し、画面レイアウト デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="bdb61-179">Close the screen layout designer by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="bdb61-180">メッセージが表示されたら、**はい** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-180">When you're prompted, select **Yes** to save your changes.</span></span>
14. <span data-ttu-id="bdb61-181">**小売** &gt; **小売 IT** &gt; **配送スケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-181">Select **Retail** &gt; **Retail IT** &gt; **Distribution schedule**.</span></span>
15. <span data-ttu-id="bdb61-182">**レジスター** ジョブ (1090) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-182">Select the **Registers** job (1090), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="bdb61-183">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-183">When you're prompted, select **Yes**.</span></span>

#### <a name="pos"></a><span data-ttu-id="bdb61-184">POS</span><span class="sxs-lookup"><span data-stu-id="bdb61-184">POS</span></span>

1. <span data-ttu-id="bdb61-185">POS を起動し、顧客をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-185">Start POS, and add a customer to a transaction.</span></span>
2. <span data-ttu-id="bdb61-186">トランザクション画面を開いて、追加された属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="bdb61-186">Open the transaction screen to view the attributes that have been added.</span></span>

