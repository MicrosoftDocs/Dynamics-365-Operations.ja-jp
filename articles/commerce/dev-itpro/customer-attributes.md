---
title: 顧客属性
description: このトピックでは、顧客属性に関する情報を提供し、構成を使用して顧客のマスター レコードに新しいフィールドを追加する方法について説明します。
author: mugunthanm
manager: AnnBe
ms.date: 10/12/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: a86308c160c1b624c4129e6d551454dcd581aeec
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683349"
---
# <a name="customer-attributes"></a><span data-ttu-id="42300-103">顧客属性</span><span class="sxs-lookup"><span data-stu-id="42300-103">Customer attributes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="42300-104">顧客、顧客の注文、現金売りトランザクション、およびコール センター注文の属性をサポートするために、バックオフィスの属性フレームワークを拡張しました。</span><span class="sxs-lookup"><span data-stu-id="42300-104">We extended the attribute framework in Headquarters to support attributes for customers, customer orders, cash-and-carry transactions, and call center orders.</span></span>

> [!NOTE]
> <span data-ttu-id="42300-105">属性は読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="42300-105">The attributes are read-only.</span></span> <span data-ttu-id="42300-106">ただし、顧客や注文属性の場合は、個々の顧客または注文のレベルで値を編集および設定できます。</span><span class="sxs-lookup"><span data-stu-id="42300-106">However, in the case of customer or order attributes, you can edit and set values at the level of the individual customer or order.</span></span>

<span data-ttu-id="42300-107">新しい顧客属性フレームワークでは、コンフィギュレーションを使用して顧客マスター レコードに新しい項目を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="42300-107">The new customer attribute framework lets you use configurations to add new fields to the customer master record.</span></span> <span data-ttu-id="42300-108">これらのフィールドは販売時点管理 (POS) またはバックオフィスの **顧客の追加/編集** または **顧客の詳細** 画面に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="42300-108">Those fields then automatically appear on the **Customer add/edit** or **Customer details** screen in Point of Sale (POS) or Headquarters.</span></span> <span data-ttu-id="42300-109">コマース パラメーターの顧客属性グループを構成すると、POS とバックオフィスは自動的に新しい属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="42300-109">After you configure the customer attribute group in the Commerce parameters, POS and Headquarters automatically show the new attribute.</span></span> <span data-ttu-id="42300-110">コードの変更またはカスタマイズは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="42300-110">No code change or customization is required.</span></span> <span data-ttu-id="42300-111">また、画面レイアウト デザイナーを使用して、POS トランザクション画面に顧客の属性が表示されるように顧客カードを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="42300-111">You can also use the screen layout designer to configure the customer card on the POS transaction screen so that it shows the customer attributes.</span></span>

## <a name="why-and-when-you-should-configure-customer-attributes"></a><span data-ttu-id="42300-112">顧客属性の構成が必要な理由および場合</span><span class="sxs-lookup"><span data-stu-id="42300-112">Why and when you should configure customer attributes</span></span>

<span data-ttu-id="42300-113">顧客のマスター レコードに新しいフィールドを追加して、POS またはバック オフィスで情報を取得する場合は、この機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="42300-113">If you want to add new fields to the customer master record, and capture the information in POS or Headquarters, you can use this feature.</span></span> <span data-ttu-id="42300-114">以前は、顧客マスター レコードに新しいフィールドを追加して POS およびバックオフィスに表示するには、バックオフィスおよびチャネル データベースで新しい拡張テーブルを作成し、Commerce runtime (CRT) および POS コードでインライン変更を加える必要がありました。</span><span class="sxs-lookup"><span data-stu-id="42300-114">Previously, to add a new field to the customer master record and show it in POS and Headquarters, you had to create a new extension table in Headquarters and the channel database, and make inline modifications to Commerce runtime (CRT) and POS code.</span></span> <span data-ttu-id="42300-115">拡張フィールドへの読み取り/書き込みを行い POS で表示するには、CRT および POS でコードを記述する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="42300-115">You had to write code in CRT and POS to read/write to the extension fields and show them in POS.</span></span> <span data-ttu-id="42300-116">**顧客の詳細** 画面およびトランザクション画面の **顧客** パネルなど、さまざまな POS ビューやシナリオでこれを処理する必要がありました。</span><span class="sxs-lookup"><span data-stu-id="42300-116">You had to handle this in various POS views and scenarios, such as the **Customer details** screen and the **Customer** panel on the transaction screen.</span></span> <span data-ttu-id="42300-117">さらに、CRT で、挿入、選択、および更新のすべての操作を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42300-117">In addition, in CRT, you had to handle all insert, select, and update operations.</span></span> <span data-ttu-id="42300-118">ただし、新しい機能によりこれらのすべての手順をコンフィギュレーションによって完了できるため、コードを記述またはカスタム拡張機能テーブルを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="42300-118">However, the new functionality lets you complete all these steps through configuration so you don't have to write any code or create custom extension tables.</span></span>

<span data-ttu-id="42300-119">この機能の最初のバージョンは、**datetime** および **reference** 属性タイプをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="42300-119">The first version of this functionality doesn't support **datetime** and **reference** attribute types.</span></span> <span data-ttu-id="42300-120">それらの属性タイプについては、POS に詳細を表示するのに、拡張機能プロパティおよびカスタム コントロールを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42300-120">For those attribute types, you should use extension properties and custom controls to show the details in POS.</span></span>

## <a name="configure-customer-attributes-in-pos-and-headquarters"></a><span data-ttu-id="42300-121">POS およびバックオフィスで顧客属性をコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="42300-121">Configure customer attributes in POS and Headquarters</span></span>

### <a name="define-attribute-types"></a><span data-ttu-id="42300-122">属性タイプを定義</span><span class="sxs-lookup"><span data-stu-id="42300-122">Define attribute types</span></span>

1. <span data-ttu-id="42300-123">**製品情報管理** > **設定** &gt; **カテゴリと属性** > **属性タイプ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-123">Select **Product information management** > **Setup** &gt; **Categories and attributes** > **Attribute types**.</span></span>
2. <span data-ttu-id="42300-124">**属性タイプ** ページで、**新規** を選択し、新しい属性タイプを追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-124">On the **Attribute types** page, select **New** to add a new attribute type.</span></span>
3. <span data-ttu-id="42300-125">階層タイプ名を入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-125">Enter a name for the attribute type.</span></span>
4. <span data-ttu-id="42300-126">**一般** クイック タブの、**タイプ** フィールドで、このデータ型に割り当てられている属性に入力できるデータのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-126">On the **General** FastTab, in the **Type** field, select the type of data that can be entered for attributes that are assigned to this data type.</span></span>
5. <span data-ttu-id="42300-127">属性タイプが **少数点** または **整数** の場合、測定単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-127">If the attribute type is **Decimal** or **Integer**, select a unit of measure.</span></span>
6. <span data-ttu-id="42300-128">属属性タイプの固定値リストを定義するには、**固定値リスト** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="42300-128">To define a fixed list of values for the attribute type, select the **Fixed list** check box.</span></span> <span data-ttu-id="42300-129">次に、**値** クイックタブで、値のリストを追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-129">Then, on the **Values** FastTab, add the list of values.</span></span>

    > [!NOTE]
    > <span data-ttu-id="42300-130">**固定リスト** チェック ボックスは、**テキスト** 属性タイプでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="42300-130">The **Fixed list** check box is available only for the **Text** attribute type.</span></span>

    <span data-ttu-id="42300-131">または、属性タイプに有効な値の範囲を定義するには **値の範囲** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-131">Alternatively, to define a range of valid values for the attribute type, select the **Value range** check box.</span></span> <span data-ttu-id="42300-132">次に、**範囲** クイックタブで、値の有効範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-132">Then, on the **Range** FastTab, enter the valid range of values.</span></span>

### <a name="define-attributes"></a><span data-ttu-id="42300-133">属性の定義</span><span class="sxs-lookup"><span data-stu-id="42300-133">Define attributes</span></span>

1. <span data-ttu-id="42300-134">**製品情報管理** > **設定** > **カテゴリと属性** > **属性** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-134">Select **Product information management** > **Setup** > **Categories and attributes** > **Attributes**.</span></span>
2. <span data-ttu-id="42300-135">**属性** ページで、**新規** を選択し、新しい属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-135">On the **Attributes** page, select **New** to add a new attribute.</span></span>
3. <span data-ttu-id="42300-136">属性にユーザーを表示する必要がある名前、フレンドリ名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-136">Enter the name, friendly name, description, and any Help text that should be shown to the user for the attribute.</span></span>
4. <span data-ttu-id="42300-137">**属性タイプ** フィールドで、属性に割り当てる属性タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-137">In the **Attribute type** field, select the attribute type to assign to the attribute.</span></span>
5. <span data-ttu-id="42300-138">属性タイプに応じて、**既定値** フィールドに、この属性が顧客に割り当てられたときに既定で表示される値または値の範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-138">Depending on the attribute type, in the **Default value** field, enter the value or the range of values that is shown by default when this attribute is assigned to a customer.</span></span>
6. <span data-ttu-id="42300-139">**翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性の名前、説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="42300-139">Select **Translate** to open the **Text translation** page, where you can enter the name, description, friendly name, and Help text for the attribute in additional languages.</span></span>
7. <span data-ttu-id="42300-140">ステップ 2 ～ 6 を繰り返してさらに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-140">Repeat steps 2 through 6 to add more attributes.</span></span>

### <a name="define-an-attribute-group"></a><span data-ttu-id="42300-141">属性グループの定義</span><span class="sxs-lookup"><span data-stu-id="42300-141">Define an attribute group</span></span>

1. <span data-ttu-id="42300-142">**製品情報管理** > **設定** > **カテゴリと属性** > **属性グループ** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-142">Select **Product information management** > **Setup** > **Categories and attributes** > **Attribute groups**.</span></span>
2. <span data-ttu-id="42300-143">**属性グループ** ページで、**新規** を選択し、新しい属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-143">On the **Attribute groups** page, select **New** to add a new attribute group.</span></span>
3. <span data-ttu-id="42300-144">名前を入力し、次に **一般** FastTab で、属性グループのフレンドり名、説明、およびヘルプ テキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-144">Enter the name, and then, on the **General** FastTab, enter the friendly name, description, and any Help text for the attribute group.</span></span>
4. <span data-ttu-id="42300-145">**属性** クイック タブで、**追加** を選択して、属性グループに属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-145">On the **Attributes** FastTab, select **Add** to add attributes to the attribute group.</span></span> <span data-ttu-id="42300-146">**既定値** フィールドでは、選択した属性の既定値を入力できます。</span><span class="sxs-lookup"><span data-stu-id="42300-146">In the **Default value** field, you can enter a default value for the selected attributes.</span></span>
5. <span data-ttu-id="42300-147">**翻訳** を選択して **テキスト翻訳** ページ を開き、追加の言語で属性グループの説明、フレンドリ名、およびヘルプ テキストを入力できます。</span><span class="sxs-lookup"><span data-stu-id="42300-147">Select **Translate** to open the **Text translation** page, where you can enter the description, friendly name, and Help text for the attribute group in additional languages.</span></span>

### <a name="link-the-attribute-group-to-the-customers"></a><span data-ttu-id="42300-148">属性グループの顧客へのリンク</span><span class="sxs-lookup"><span data-stu-id="42300-148">Link the attribute group to the customers</span></span>

1. <span data-ttu-id="42300-149">**Retail とコマース** > **バックオフィス設定** > **パラメーター** > **コマース パラメーター** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-149">Select **Retail and Commerce** > **Headquarters setup** > **Parameters** > **Commerce parameters**.</span></span>
2. <span data-ttu-id="42300-150">**一般** タブの、**顧客属性グループ** フィールドに、属性グループ POS に表示する必要がある属性グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-150">On the **General** tab, in the **Customer attribute group** field, select the attribute group that should be shown in POS.</span></span>

### <a name="run-the-distribution-jobs"></a><span data-ttu-id="42300-151">配送ジョブを実行</span><span class="sxs-lookup"><span data-stu-id="42300-151">Run the distribution jobs</span></span>

1. <span data-ttu-id="42300-152">**Retail とコマース** > **Retail と コマース IT** > **配送スケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-152">Select **Retail and Commerce** > **Retail and Commerce IT** > **Distribution schedule**.</span></span>
2. <span data-ttu-id="42300-153">**顧客** ジョブ (1010) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-153">Select the **Customers** job (1010), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="42300-154">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-154">When you're prompted, select **Yes**.</span></span>
3. <span data-ttu-id="42300-155">**グローバル構成** ジョブ (1110) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-155">Select the **Global configuration** job (1110), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="42300-156">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-156">When you're prompted, select **Yes**.</span></span>

### <a name="view-customer-attributes"></a><span data-ttu-id="42300-157">顧客属性の表示</span><span class="sxs-lookup"><span data-stu-id="42300-157">View customer attributes</span></span>

#### <a name="headquarters"></a><span data-ttu-id="42300-158">バックオフィス</span><span class="sxs-lookup"><span data-stu-id="42300-158">Headquarters</span></span>

1. <span data-ttu-id="42300-159">**Retail とコマース** > **顧客** > **すべての顧客** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-159">Select **Retail and Commerce** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="42300-160">アクション ウィンドウの **Retail とコマース** にある、**属性** セクションで、**小売属性** を選択して属性値を表示または編集します。</span><span class="sxs-lookup"><span data-stu-id="42300-160">On the Action Pane, in **Retail and Commerce**, in the **Attribute** section, select **Retail attributes** to view or edit the attribute values.</span></span>

#### <a name="pos"></a><span data-ttu-id="42300-161">POS</span><span class="sxs-lookup"><span data-stu-id="42300-161">POS</span></span>

- <span data-ttu-id="42300-162">POS を起動し、**顧客の追加/編集** 画面を開いて顧客の属性値を設定または更新するか、**顧客の詳細** 画面を開いて構成されている属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="42300-162">Start POS, and then either open the **Customer Add/Edit** screen to set or update the attribute values for the customer, or open the **Customer details** screen to view the configured attributes.</span></span>

### <a name="show-customer-attributes-in-the-pos-transaction-screen"></a><span data-ttu-id="42300-163">POS トランザクション画面に顧客属性を表示</span><span class="sxs-lookup"><span data-stu-id="42300-163">Show customer attributes in the POS transaction screen</span></span>

#### <a name="headquarters"></a><span data-ttu-id="42300-164">バックオフィス</span><span class="sxs-lookup"><span data-stu-id="42300-164">Headquarters</span></span>

1. <span data-ttu-id="42300-165">**Retail と Commerce** > **チャネル設定** > **POS 設定** > **POS** > **画面レイアウト** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-165">Select **Retail and Commerce** > **Channel setup** > **POS Setup** > **POS** > **Screen layouts**.</span></span>
2. <span data-ttu-id="42300-166">**画面レイアウト** ページで、**新規** を選択し新しい画面レイアウトを作成するか、既存の画面レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-166">On the **screen layout** page, select **New** to create a new screen layout, or select an existing screen layout.</span></span>
3. <span data-ttu-id="42300-167">スクリーン レイアウトの名前と ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="42300-167">Enter the ID and name for the screen layout.</span></span>
4. <span data-ttu-id="42300-168">**レイアウト サイズ** クイック タブで、**追加** ボタン選択して、POS の新しいレイアウト サイズを追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-168">On the **Layout sizes** FastTab, select the **Add** button to add new layout sizes for the POS.</span></span>
5. <span data-ttu-id="42300-169">**名前** フィールドで POS 画面の解像度を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-169">In the **Name** field, select the POS screen resolution.</span></span>
6. <span data-ttu-id="42300-170">**レイアウト サイズ** クイック タブで、**レイアウト デザイナー** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-170">On the **Layout sized** FastTab, select the **Layout designer** button.</span></span>
7. <span data-ttu-id="42300-171">プロンプトが表示されたら、**インストール/実行** ボタンを使用して Retail Designer Host をダウンロードしてインストールするには、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-171">If you're prompted, select **Yes** to download and install the Retail Designer Host by using the **Install/Run** button.</span></span>
8. <span data-ttu-id="42300-172">入力を求めるメッセージが表示されたら、Microsoft Dynamics 365 のユーザー名とパスワードを入力して、デザイナーを起動します。</span><span class="sxs-lookup"><span data-stu-id="42300-172">When you're prompted, enter the Microsoft Dynamics 365 user name and password to start the designer.</span></span>
9. <span data-ttu-id="42300-173">デザイナーが開始された後、**顧客** カードを画面レイアウト デザイナーの任意の場所にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="42300-173">After the designer is started, drag the **Customer** card anywhere in the screen layout designer.</span></span>
10. <span data-ttu-id="42300-174">**顧客** カードを右クリックし、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-174">Right-click the **Customer** card, and then select **Customize**.</span></span>
11. <span data-ttu-id="42300-175">**カスタマイズ - 顧客** カードのページが表示されたら、**利用可能な列** セクションで必要な属性を選択してから、右矢印ボタン (**>**) を選択して 、それらを **選択された列** セクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="42300-175">When the page for the **Customization - Customer** card appears, select the required attributes in the **Available columns** section, and then select the right arrow button (**>**) to move them to the **Selected columns** section.</span></span> <span data-ttu-id="42300-176">**上** または **下** ボタンを選択することにより、属性を上または下に移動することができます。</span><span class="sxs-lookup"><span data-stu-id="42300-176">You can move the attributes up or down by selecting the **Up** or **Down** buttons.</span></span>
12. <span data-ttu-id="42300-177">完了したら、**OK** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="42300-177">When you've finished, select **OK** to save your changes.</span></span>
13. <span data-ttu-id="42300-178">右上隅の **閉じる** ボタン (**X**) を選択し、画面レイアウト デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="42300-178">Close the screen layout designer by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="42300-179">メッセージが表示されたら、**はい** を選択して、変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="42300-179">When you're prompted, select **Yes** to save your changes.</span></span>
14. <span data-ttu-id="42300-180">**Retail とコマース** &gt; **Retail とコマース IT** &gt; **配送スケジュール** の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-180">Select **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedule**.</span></span>
15. <span data-ttu-id="42300-181">**レジスター** ジョブ (1090) を選択し、アクション ペインで **今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-181">Select the **Registers** job (1090), and then, on the Action Pane, select **Run now**.</span></span> <span data-ttu-id="42300-182">メッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="42300-182">When you're prompted, select **Yes**.</span></span>

#### <a name="pos"></a><span data-ttu-id="42300-183">POS</span><span class="sxs-lookup"><span data-stu-id="42300-183">POS</span></span>

1. <span data-ttu-id="42300-184">POS を起動し、顧客をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="42300-184">Start POS, and add a customer to a transaction.</span></span>
2. <span data-ttu-id="42300-185">トランザクション画面を開いて、追加された属性を表示します。</span><span class="sxs-lookup"><span data-stu-id="42300-185">Open the transaction screen to view the attributes that have been added.</span></span>
