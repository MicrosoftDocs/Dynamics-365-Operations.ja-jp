---
title: 販売時点管理 (POS) Totals パネルへカスタム フィールドを追加
description: このトピックでは、画面レイアウト デザイナーを使用して、POS トランザクション画面の合計パネルに新しいカスタム フィールドを追加する方法について説明します。
author: mugunthanm
ms.date: 05/23/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 6cdafd4243b8e093addb95446d52eae1dd41845f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795673"
---
# <a name="add-custom-fields-to-the-point-of-sale-pos-totals-panel"></a><span data-ttu-id="2b2a8-103">販売時点管理 (POS) Totals パネルへカスタム フィールドを追加</span><span class="sxs-lookup"><span data-stu-id="2b2a8-103">Add custom fields to the point of sale (POS) Totals panel</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b2a8-104">このトピックでは、画面レイアウト デザイナーを使用して、POS トランザクション画面の **合計** パネルに新しいカスタム フィールドを追加する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-104">This topic explains how to add a new custom field to the **Totals** panel on the POS transaction screen by using the screen layout designer.</span></span> <span data-ttu-id="2b2a8-105">このトピックは、Microsoft Dynamics 365 for Finance and Operations 7.3 およびそれ以降と、Microsoft Dynamics 365 Retail 7.3 およびそれ以降に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-105">This topic is applicable to Microsoft Dynamics 365 for Finance and Operations 7.3 and later, and to Microsoft Dynamics 365 Retail 7.3 and later.</span></span>

<span data-ttu-id="2b2a8-106">**カスタム フィールド** ページの **合計** パネルに追加するカスタム フィールドが、デザイナーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-106">Custom fields that you add for the **Totals** panel on the **Custom fields** page will appear in the designer.</span></span> <span data-ttu-id="2b2a8-107">次に、左右の列にあるカスタム フィールドを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-107">You can then select which custom fields should be in the left and right columns.</span></span> <span data-ttu-id="2b2a8-108">カスタム フィールドのロジックは、販売時点管理 (POS) 拡張機能でコーディングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-108">The logic for the custom fields should be coded in the point of sale (POS) extensions.</span></span>

## <a name="scenariobusiness-problem"></a><span data-ttu-id="2b2a8-109">シナリオ/ビジネスの問題</span><span class="sxs-lookup"><span data-stu-id="2b2a8-109">Scenario/business problem</span></span>

<span data-ttu-id="2b2a8-110"><span id="_Toc446093285" class="anchor"></span>画面レイアウト デザイナーを使用して、POS トランザクション画面の **合計** パネルにカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-110"><span id="_Toc446093285" class="anchor"></span>You will add a custom field to the **Totals** panel on the POS transaction screen by using the screen layout designer.</span></span> <span data-ttu-id="2b2a8-111">また、POS 拡張のカスタム項目のビジネス ロジックをコード化します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-111">You will also code the business logic for the custom field in the POS extensions.</span></span>

## <a name="overview-of-the-required-steps"></a><span data-ttu-id="2b2a8-112">必要な手順の概要</span><span class="sxs-lookup"><span data-stu-id="2b2a8-112">Overview of the required steps</span></span>

<span data-ttu-id="2b2a8-113">まず、バックオフィスをコンフィギュレーションするには、これらの手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-113">First, you must complete these steps to configure Headquarters.</span></span>

1. <span data-ttu-id="2b2a8-114">**言語テキスト** ページで、カスタム フィールドの言語テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-114">On the **Language text** page, add the language text for the custom field.</span></span>
2. <span data-ttu-id="2b2a8-115">**カスタム フィールド** ページで、新しいカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-115">On the **Custom fields** page, add the new custom field.</span></span>
3. <span data-ttu-id="2b2a8-116">画面レイアウト デザイナーで、**合計** パネルに新しいカスタム フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-116">In the screen layout designer, add the new custom field to the **Totals** panel.</span></span>
4. <span data-ttu-id="2b2a8-117">**レジスター** (**1090**) ジョブを実行します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-117">Run the **Registers** (**1090**) job.</span></span>

<span data-ttu-id="2b2a8-118">POS の拡張機能プロジェクトでは、この手順を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-118">You must then complete this step in the POS extension project.</span></span>

- <span data-ttu-id="2b2a8-119">ビジネス ロジックをカスタム フィールドへ追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-119">Add the business logic for the custom field.</span></span>

## <a name="configure-headquarters"></a><span data-ttu-id="2b2a8-120">バックオフィスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="2b2a8-120">Configure Headquarters</span></span>

1. <span data-ttu-id="2b2a8-121">コマースにサインインします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-121">Sign in to Commerce.</span></span>
2. <span data-ttu-id="2b2a8-122">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> 言語テキスト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-122">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Language text**.</span></span>
3. <span data-ttu-id="2b2a8-123">**POS** タブで、**追加** を選択して新しい POS 言語テキストを追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-123">On the **POS** tab, select **Add** to add a new POS language text.</span></span>

    <span data-ttu-id="2b2a8-124">**合計** パネルに表示されるテキストはローカライズすることができます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-124">The text that appears in the **Totals** panel can be localized.</span></span> <span data-ttu-id="2b2a8-125">したがって、同じテキスト ID の異なる言語で複数のテキストを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-125">Therefore, you can create multiple texts in different languages for the same text ID.</span></span> <span data-ttu-id="2b2a8-126">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-126">Here is an example.</span></span>

    | <span data-ttu-id="2b2a8-127">言語 ID</span><span class="sxs-lookup"><span data-stu-id="2b2a8-127">Language ID</span></span> | <span data-ttu-id="2b2a8-128">テキスト ID</span><span class="sxs-lookup"><span data-stu-id="2b2a8-128">Text ID</span></span> | <span data-ttu-id="2b2a8-129">テキスト</span><span class="sxs-lookup"><span data-stu-id="2b2a8-129">Text</span></span>   |
    |-------------|---------|--------|
    | <span data-ttu-id="2b2a8-130">ja</span><span class="sxs-lookup"><span data-stu-id="2b2a8-130">en-US</span></span>       | <span data-ttu-id="2b2a8-131">1</span><span class="sxs-lookup"><span data-stu-id="2b2a8-131">1</span></span>       | <span data-ttu-id="2b2a8-132">サンプル</span><span class="sxs-lookup"><span data-stu-id="2b2a8-132">Sample</span></span> |
    | <span data-ttu-id="2b2a8-133">en-UK</span><span class="sxs-lookup"><span data-stu-id="2b2a8-133">en-UK</span></span>       | <span data-ttu-id="2b2a8-134">1</span><span class="sxs-lookup"><span data-stu-id="2b2a8-134">1</span></span>       | <span data-ttu-id="2b2a8-135">デモ</span><span class="sxs-lookup"><span data-stu-id="2b2a8-135">Demo</span></span>   |

4. <span data-ttu-id="2b2a8-136">アクション ウィンドウで、**保存** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-136">On the Action Pane, select **Save** to save your changes.</span></span>
5. <span data-ttu-id="2b2a8-137">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS プロファイル \> カスタム フィールド** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-137">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Custom fields**.</span></span>
6. <span data-ttu-id="2b2a8-138">アクション ウィンドウで、**新規** を選択して新しいカスタム フィールドを追加し、次の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-138">On the Action Pane, select **New** to add a new custom field, and specify the following information:</span></span> 

    1. <span data-ttu-id="2b2a8-139">**名前** フィールドに、カスタム フィールドの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-139">In the **Name** field, enter the name of the custom field.</span></span>
    2. <span data-ttu-id="2b2a8-140">**タイプ** フィールドで、**合計エリア** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-140">In the **Type** field, select **Totals area**.</span></span>
    3. <span data-ttu-id="2b2a8-141">**キャプション テキスト ID** フィールドで、手順 3 で使用したテキスト ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-141">In the **Caption text ID** field, specify the text ID that you used in step 3.</span></span>

    <span data-ttu-id="2b2a8-142">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-142">Here is an example.</span></span>

    | <span data-ttu-id="2b2a8-143">氏名</span><span class="sxs-lookup"><span data-stu-id="2b2a8-143">Name</span></span>   | <span data-ttu-id="2b2a8-144">種類</span><span class="sxs-lookup"><span data-stu-id="2b2a8-144">Type</span></span>        | <span data-ttu-id="2b2a8-145">キャプション テキスト ID</span><span class="sxs-lookup"><span data-stu-id="2b2a8-145">Caption text ID</span></span> |
    |--------|-------------|-----------------|
    | <span data-ttu-id="2b2a8-146">サンプル</span><span class="sxs-lookup"><span data-stu-id="2b2a8-146">Sample</span></span> | <span data-ttu-id="2b2a8-147">合計エリア</span><span class="sxs-lookup"><span data-stu-id="2b2a8-147">Totals area</span></span> | <span data-ttu-id="2b2a8-148">1</span><span class="sxs-lookup"><span data-stu-id="2b2a8-148">1</span></span>               |


7. <span data-ttu-id="2b2a8-149">アクション ウィンドウで、**保存** を選択して変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-149">On the Action Pane, select **Save** to save your changes.</span></span>
8. <span data-ttu-id="2b2a8-150">**Retail とコマース \> チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-150">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS \> Screen layouts**.</span></span>
9. <span data-ttu-id="2b2a8-151">**F3MGR** 画面レイアウト ID を選択した後、アクション ウィンドウで **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-151">Select the **F3MGR** screen layout ID, and then, on the Action Pane, select **Designer**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b2a8-152">既存のレイアウトを選択するか、新しいレイアウトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-152">You can select any existing layout or create a new layout.</span></span> <span data-ttu-id="2b2a8-153">**F3MGR** 画面レイアウト ID は、デモ データを使用している場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-153">The **F3MGR** screen layout ID is available only if you're using demo data.</span></span>

10. <span data-ttu-id="2b2a8-154">**1440x960 – フル** レイアウト サイズを選択し、**レイアウト デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-154">Select the **1440x960 – Full** layout size, and then select **Layout designer**.</span></span>
11. <span data-ttu-id="2b2a8-155">アプリケーションを開いて確認するよう求めるメッセージが表示されたら、**開く** を選択して、インストールの指示に従ってください。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-155">If you're prompted to confirm that you want to open the application, select **Open**, and then follow the installation instructions.</span></span>
12. <span data-ttu-id="2b2a8-156">デザイナーをインストールすると、Azure Active Directory (Azure AD) の資格情報を要求されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-156">After the designer is installed, you're asked for Azure Active Directory (Azure AD) credentials.</span></span> <span data-ttu-id="2b2a8-157">デザイナーを開始するための情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-157">Enter the information to start the designer.</span></span>
13. <span data-ttu-id="2b2a8-158">デザイナーで、左ウィンドウから画面レイアウトへ **合計パネル** コントロールをドラッグします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-158">In the designer, drag the **Totals panel** control from the left pane to the screen layout.</span></span> <span data-ttu-id="2b2a8-159">レイアウトに既に **合計** パネルが含まれている場合、コントロールは左ウィンドウに淡色表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-159">If the layout already includes a **Totals** panel, the control appears dimmed in the left pane.</span></span>
14. <span data-ttu-id="2b2a8-160">画面レイアウトで、**合計パネル** を右クリックし、**カスタマイズ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-160">In the screen layout, right-click the **Totals panel**, and then select **Customize**.</span></span>
15. <span data-ttu-id="2b2a8-161">**カスタマイズ - 合計パネル** ダイアログ ボックスで、**SAMPLE** カスタム フィールドが **利用可能なフィールド** リストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-161">In the **Customization - Totals panel** dialog box, the **SAMPLE** custom field should appear in the **Available fields** list.</span></span> <span data-ttu-id="2b2a8-162">矢印ボタンを使用して左列または右列のいずれかに移動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-162">Move it to either the left column or the right column by using the arrow buttons.</span></span>
16. <span data-ttu-id="2b2a8-163">カスタム フィールドを上下に移動するには、**アップ** および **ダウン** ボタンを使用します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-163">To move the custom field up or down, use the **Up** and **Down** buttons.</span></span>
17. <span data-ttu-id="2b2a8-164">**OK** を選択して変更を保存し、**カスタマイズ - 合計パネル** ダイアログ ボックスを終了します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-164">Select **OK** to save your changes and close the **Customization - Totals panel** dialog box.</span></span>
18. <span data-ttu-id="2b2a8-165">右上隅の **閉じる** ボタン (**X**) を選択して、デザイナーを閉じます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-165">Select the **Close** button (**X**) in the upper-right corner to close the designer.</span></span>
19. <span data-ttu-id="2b2a8-166">変更の保存を求められたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-166">When you're prompted to save your changes, select **Yes**.</span></span> <span data-ttu-id="2b2a8-167">**いいえ** を選択した場合、変更は保存されません。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-167">If you select **No**, your changes aren't saved.</span></span>
20. <span data-ttu-id="2b2a8-168">**Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-168">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
21. <span data-ttu-id="2b2a8-169">**レジスター** (**1090**) ジョブを選択し、**今すぐ実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-169">Select the **Registers** (**1090**) job, and then select **Run now**.</span></span>

## <a name="add-business-logic-to-the-custom-field"></a><span data-ttu-id="2b2a8-170">ビジネス ロジックをカスタム フィールドへ追加</span><span class="sxs-lookup"><span data-stu-id="2b2a8-170">Add business logic to the custom field</span></span>

<span data-ttu-id="2b2a8-171">同様のサンプルコードは、\\RetailSDK\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\Cart\\TipsCustomField.ts の Retail ソフトウェア開発キット (SDK) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-171">You can find similar sample code in the Retail software development kit (SDK), at …\\RetailSDK\\POS\\Extensions\\SampleExtensions\\ViewExtensions\\Cart\\TipsCustomField.ts.</span></span>

1. <span data-ttu-id="2b2a8-172">Microsoft Visual Studio 2015 を管理者モードで起動します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-172">Start Microsoft Visual Studio 2015 in administrator mode.</span></span>
2. <span data-ttu-id="2b2a8-173">**ModernPOS** ソリューションを **…\\RetailSDK\\POS** から開きます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-173">Open the **ModernPOS** solution from **…\\RetailSDK\\POS**.</span></span>
3. <span data-ttu-id="2b2a8-174">**POS.Extensions** プロジェクトで、**CustomFieldExtensions** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-174">Under the **POS.Extensions** project, create a folder that is named **CustomFieldExtensions**.</span></span>
4. <span data-ttu-id="2b2a8-175">**CustomFieldExtensions** フォルダーで、**Cart** というフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-175">Under the **CustomFieldExtensions** folder, create a folder that is named **Cart**.</span></span>
5. <span data-ttu-id="2b2a8-176">**カート** フォルダーで、**SampleCustomField.ts** という .ts (typescript) ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-176">In the **Cart** folder, create a .ts (typescript) file that is named **SampleCustomField.ts**.</span></span>
6. <span data-ttu-id="2b2a8-177">**SampleCustomField.ts** ファイルで、次の **import** ステートメントを追加して関連するエンティティおよびコンテキストをインポートします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-177">In the **SampleCustomField.ts** file, add the following **import** statement to import the relevant entities and context.</span></span>

    ```typescript
    import { CartViewTotalsPanelCustomFieldBase } from "PosApi/Extend/Views/CartView";
    import { ProxyEntities } from "PosApi/Entities";
    ```

7. <span data-ttu-id="2b2a8-178">**SampleCustomField** という名前のクラスを作成し、**CartViewTotalsPanelCustomFieldBase** クラスから拡張します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-178">Create a class that is named **SampleCustomField**, and extend it from the **CartViewTotalsPanelCustomFieldBase** class.</span></span> <span data-ttu-id="2b2a8-179">この方法で、基本クラスからの **computeValue** メソッドでは、カスタム フィールドの任意のカスタム ロジックが実行されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-179">In this way, the **computeValue** method from the base class will do any custom logic for the custom field.</span></span>

    ```typescript
    export default class SampleCustomField extends CartViewTotalsPanelCustomFieldBase {

    }
    ```

8. <span data-ttu-id="2b2a8-180">**SampleCustomField** クラス内で、カスタム フィールドのロジックを設定するため **computeValue** 抽象メソッドを実装します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-180">Inside the **SampleCustomField** class, implement the abstract **computeValue** method to set the logic for the custom field.</span></span>

    ```typescript
    public computeValue(cart: ProxyEntities.Cart): string {

        // Let's show 10% of total amount in the custom field.

        if (isNaN(cart.TotalAmount) || cart.TotalAmount <= 0) {
            return "$0.00";
        }
        return "$" + (cart.TotalAmount * 0.1).toFixed(2).toString();
    }
    ```

    <span data-ttu-id="2b2a8-181">全体的なクラスは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-181">The overall class should look like this.</span></span>

    ```typescript
    import { CartViewTotalsPanelCustomFieldBase } from "PosApi/Extend/Views/CartView";
    import { ProxyEntities } from "PosApi/Entities";

    export default class SampleCustomField extends CartViewTotalsPanelCustomFieldBase {
        public computeValue(cart: ProxyEntities.Cart): string {

            // Let's show 10% of total amount in the custom field.
            if (isNaN(cart.TotalAmount) || cart.TotalAmount <= 0) {
                return "$0.00";
            }
            return "$" + (cart.TotalAmount * 0.1).toFixed(2).toString();
        }
    }
    ```

9. <span data-ttu-id="2b2a8-182">**CustomFieldExtensions** フォルダーで、**manifest.json** という .json ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-182">In the **CustomFieldExtensions** folder, create a .json file that is named **manifest.json**.</span></span>
10. <span data-ttu-id="2b2a8-183">**manifest.json** ファイルに、以下のコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-183">In the **manifest.json** file, paste the below code.</span></span>

    ```typescript
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Contoso",
        "version": "7.3.0",
        "minimumPosVersion": "7.3.0.0",
        "components": {
            "extend": {
                "views": {
                    "CartView": {
                        "totalsPanel": {
                            "customFields": [
                                {
                                    "fieldName": "Sample",
                                    "modulePath": "Cart/SampleCustomField"
                                }
                            ]
                    } }
            }  }
    } }
    ```

    <span data-ttu-id="2b2a8-184">マニフェストでは、**customFields** セクションの **fieldName** 値が、バックオフィスで追加されたカスタム フィールドの名前、および "バックオフィスのコンフィギュレーション" 手順のステップ 6 のカスタム フィールドで指定した名前と一致している必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-184">In the manifest, note that the **fieldName** value in the **customFields** section should match the name of the custom field added in the Headquarters, the name you specified for the custom field in step 6 of the "Configure Headquarters" procedure.</span></span> <span data-ttu-id="2b2a8-185">**modulePath** は、実装ファイルの名前です。その実装ファイル名は、"ビジネス ロジックをカスタム フィールドへ追加" 手順のステップ 5 で作成したファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-185">**modulePath** is the name of the implementation file, the implementation file name is the name of the file that you created in step 5 of "Add business logic to the custom field" procedure.</span></span>
    
    <span data-ttu-id="2b2a8-186">複数のカスタム フィールドを追加する場合は、複数の実装ファイルを追加し、custonFileds セクションの情報を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-186">If you add multiple custom fields, you should add multiple implementation files and update the information under the custonFileds section.</span></span>

    <span data-ttu-id="2b2a8-187">たとえば、2 つのカスタム フィールド、**サンプル 1** と **サンプル 2** を追加する場合、同じ基本クラスの **CartViewTotalsPanelCustomFieldBase** から拡張された 2 つの実装ファイルが必要になります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-187">For example, if you add two custom fields, **Sample1** and **Sample2**, you should have two implementation files that extend from the same base class, **CartViewTotalsPanelCustomFieldBase**.</span></span>

    <span data-ttu-id="2b2a8-188">この場合、マニフェストは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-188">In this case, the manifest should look like this.</span></span>

    ```typescript
    "customFields": [
        {
            "fieldName": "Sample1",
            "modulePath": "Cart/SampleCustomField1"
        },
        {
            "fieldName": "Sample2",
            "modulePath": "Cart/SampleCustomField2"
        }
    ]
    ```
    
    <span data-ttu-id="2b2a8-189">この例では、**SampleCustomField1** と **SampleCustomField2** は、ビジネス ロジックを実行する typescript ファイルの名前になります。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-189">In this example, **SampleCustomField1** and **SampleCustomField2** are the names of the typescript files where you will do the business logic.</span></span>

11. <span data-ttu-id="2b2a8-190">**extensions.json** ファイルを **POS.Extensions** プロジェクトで開いて、**CustomFieldExtensions** サンプルで更新し、実行時に POS にこの拡張機能を読み込むようにします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-190">Open the **extensions.json** file under the **POS.Extensions** project, and update it with the **CustomFieldExtensions** samples, so that POS will load this extension at runtime.</span></span>

    ```typescript
    {
        "extensionPackages": [
            { 
                "baseUrl": "SampleExtensions2" 
            }, 
            {
                "baseUrl": "CustomFieldExtensions"
            }
        ]
    }
    ```

12. <span data-ttu-id="2b2a8-191">**tsconfig.json** ファイルを開き、拡張子フォルダ名 **CustomFieldExtensions** を追加し **除外** リストで拡張子フォルダをコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-191">Open the **tsconfig.json** file, and add the extension folder name **CustomFieldExtensions** and comment out the extension folder in the **exclude** list.</span></span> <span data-ttu-id="2b2a8-192">POS では、このファイルを使用して、拡張機能を追加または除外します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-192">POS will use this file to include or exclude the extension.</span></span> <span data-ttu-id="2b2a8-193">既定では、**除外** リストには除外されたすべての拡張リストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-193">By default, the **exclude** list contains all the excluded extensions.</span></span> <span data-ttu-id="2b2a8-194">拡張機能を POS の一部として含めるには、次に示すように、拡張フォルダーの名前を追加し、**拡張** リストの拡張をコメントアウトします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-194">To include an extension as part of the POS, you must add the extension folder name and comment out the extension in the **extension** list, as shown here.</span></span>

    ```typescript
    "exclude": [
        "SampleExtensions",
        //"SampleExtensions2",
        //"CustomFieldExtensions"
    ],
    ```

13. <span data-ttu-id="2b2a8-195">プロジェクトをコンパイル、およびリビルドします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-195">Compile and rebuild the project.</span></span>
14. <span data-ttu-id="2b2a8-196">**ローカル コンピューター** ボタンをクリックすることで、Retail Modern POS (MPOS) のカスタマイズされたバージョンを配置します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-196">Deploy the customized version of Retail Modern POS (MPOS) by selecting the **Local Machine** button.</span></span> <span data-ttu-id="2b2a8-197">ソリューション プラットフォームが x86 であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-197">Make sure that the solution platform is x86.</span></span> <span data-ttu-id="2b2a8-198">または、配置可能パッケージの作成およびパッケージから MPOS のインストールが可能です。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-198">Alternatively, you can create a deployable package and install MPOS from it.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2b2a8-199">このトピックで MPOS を使用しても、MPOS またはクラウド POS のいずれかを使用できます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-199">Although MPOS is used in this topic, you can use either MPOS or Cloud POS.</span></span>

## <a name="validate-the-customization"></a><span data-ttu-id="2b2a8-200">カスタマイズの検証</span><span class="sxs-lookup"><span data-stu-id="2b2a8-200">Validate the customization</span></span>

1. <span data-ttu-id="2b2a8-201">オペレーター ID に **000160**、パスワードに **123** を使用して MPOS にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-201">Sign in to MPOS by using **000160** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="2b2a8-202">ようこそ画面で、**現在のトランザクション** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-202">On the welcome screen, select the **Current transaction** button.</span></span>
3. <span data-ttu-id="2b2a8-203">品目をトランザクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-203">Add any item to the transaction.</span></span>

<span data-ttu-id="2b2a8-204">カスタム フィールドが **合計** パネルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2b2a8-204">The custom field should appear in the **Totals** panel.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]