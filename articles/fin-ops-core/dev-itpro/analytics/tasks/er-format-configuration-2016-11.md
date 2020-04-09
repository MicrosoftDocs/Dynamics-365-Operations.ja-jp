---
title: ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)
description: このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER)の形式コンフィギュレーション作成方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af2899da843967bfaaa8f3c66906fc8e3765b573
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142504"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="fc623-103">ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="fc623-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc623-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER)の形式コンフィギュレーション作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fc623-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="fc623-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="fc623-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="fc623-106">この例では、サンプル会社 Litware、Inc. のフォーマット構成を作成します。この手順を完了するには、まず「選択したデータソースへのモデルのマッピング」に記載の手順のを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc623-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="fc623-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="fc623-107">Create a new format configuration</span></span>
1. <span data-ttu-id="fc623-108">**組織管理 > ワークスペース > 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fc623-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="fc623-109">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="fc623-110">ツリーで、**支払 (単純化モデル)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="fc623-111">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc623-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="fc623-112">**コンフィギュレーションの作成**が表示されない場合は、**電子申告のパラメーター**ページでデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc623-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="fc623-113">**新規**フィールドで、**PaymentModel データ モデルに基づいた書式**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="fc623-114">**名前**フィールドに、**BACS (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="fc623-115">**説明**フィールドに、**BACS 仕入先支払形式 (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="fc623-116">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="fc623-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="fc623-117">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="fc623-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="fc623-118">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="fc623-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="fc623-119">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="fc623-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="fc623-120">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="fc623-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="fc623-121">**データ モデル定義**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="fc623-122">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-122">Click **Create configuration**.</span></span> <span data-ttu-id="fc623-123">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="fc623-123">A new configuration has been created.</span></span> <span data-ttu-id="fc623-124">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="fc623-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="fc623-125">電子ドキュメントの形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="fc623-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="fc623-126">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-126">Click **Designer**.</span></span>
2. <span data-ttu-id="fc623-127">**ルートの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc623-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="fc623-128">ツリーで、**Common\File** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="fc623-129">**名前**フィールドに、**Xml** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="fc623-130">**エンコード**フィールドに、**UTF-8** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="fc623-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-131">Click **OK**.</span></span>
7. <span data-ttu-id="fc623-132">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-132">Click **Add**.</span></span>
8. <span data-ttu-id="fc623-133">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="fc623-134">**名前**フィールドに、**メッセージ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="fc623-135">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-135">Click **OK**.</span></span>
11. <span data-ttu-id="fc623-136">ツリーで、**Xml\Message** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="fc623-137">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="fc623-138">**名前**フィールドに、**ProcessingDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="fc623-139">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-139">Click **OK**.</span></span>
15. <span data-ttu-id="fc623-140">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="fc623-141">名前フィールドに、**MessageId** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="fc623-142">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-142">Click **OK**.</span></span>
18. <span data-ttu-id="fc623-143">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="fc623-144">**名前**フィールドに、**支払**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="fc623-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-145">Click **OK**.</span></span>
21. <span data-ttu-id="fc623-146">ツリーで、**Xml\Message\Payments** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="fc623-147">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="fc623-148">**名前**フィールドに、**品目**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="fc623-149">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-149">Click **OK**.</span></span>
25. <span data-ttu-id="fc623-150">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="fc623-151">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-151">Click **Add**.</span></span>
27. <span data-ttu-id="fc623-152">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="fc623-153">名前フィールドに、**Id** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="fc623-154">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-154">Click **OK**.</span></span>
30. <span data-ttu-id="fc623-155">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-155">Click **Add**.</span></span>
31. <span data-ttu-id="fc623-156">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="fc623-157">名前フィールドに、**仕入先**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="fc623-158">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-158">Click **OK**.</span></span>
34. <span data-ttu-id="fc623-159">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="fc623-160">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="fc623-161">名前フィールドに、**名前**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="fc623-162">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-162">Click **OK**.</span></span>
38. <span data-ttu-id="fc623-163">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="fc623-164">**名前**フィールドに、**銀行**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="fc623-165">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-165">Click **OK**.</span></span>
41. <span data-ttu-id="fc623-166">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="fc623-167">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="fc623-168">**名前**フィールドに、**RoutingNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="fc623-169">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-169">Click **OK**.</span></span>
45. <span data-ttu-id="fc623-170">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="fc623-171">**名前**フィールドに、**AccountNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="fc623-172">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-172">Click **OK**.</span></span>
48. <span data-ttu-id="fc623-173">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="fc623-174">**コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-174">Click **Copy**.</span></span>
50. <span data-ttu-id="fc623-175">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="fc623-176">**ペースト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-176">Click **Paste**.</span></span>
52. <span data-ttu-id="fc623-177">**名前**フィールドに、**支払人**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="fc623-178">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="fc623-179">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="fc623-180">**名前**フィールドに、**通貨**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="fc623-181">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-181">Click **OK**.</span></span>
57. <span data-ttu-id="fc623-182">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="fc623-183">**名前**フィールドに、**説明**と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="fc623-184">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-184">Click **OK**.</span></span>
60. <span data-ttu-id="fc623-185">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="fc623-186">名前フィールドに、**TransDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="fc623-187">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-187">Click **OK**.</span></span>
63. <span data-ttu-id="fc623-188">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="fc623-189">名前フィールドに、**Amount** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="fc623-190">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="fc623-191">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="fc623-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="fc623-192">ツリーで、**Xml\Message\ProcessingDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="fc623-193">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc623-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="fc623-194">ツリーで、**Text\DateTime** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="fc623-195">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="fc623-196">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-196">Click **OK**.</span></span>
6. <span data-ttu-id="fc623-197">ツリーで、**Xml\Message\Payments\Item\TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="fc623-198">**日時を追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="fc623-199">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="fc623-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="fc623-200">**DateTime** 型フィールドで、**日付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="fc623-201">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-201">Click **OK**.</span></span>
11. <span data-ttu-id="fc623-202">ツリーで、**Xml\Message\MessageId** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="fc623-203">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fc623-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="fc623-204">ツリーで、**Text\String** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="fc623-205">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-205">Click **OK**.</span></span>
15. <span data-ttu-id="fc623-206">ツリーで、**Xml\Message\Payments\Item\Vendor\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="fc623-207">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-207">Click **Add String**.</span></span>
17. <span data-ttu-id="fc623-208">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-208">Click **OK**.</span></span>
18. <span data-ttu-id="fc623-209">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="fc623-210">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-210">Click **Add String**.</span></span>
20. <span data-ttu-id="fc623-211">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-211">Click **OK**.</span></span>
21. <span data-ttu-id="fc623-212">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="fc623-213">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-213">Click **Add String**.</span></span>
23. <span data-ttu-id="fc623-214">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-214">Click **OK**.</span></span>
24. <span data-ttu-id="fc623-215">ツリーで、**Xml\Message\Payments\Item\Payer\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="fc623-216">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-216">Click **Add String**.</span></span>
26. <span data-ttu-id="fc623-217">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-217">Click **OK**.</span></span>
27. <span data-ttu-id="fc623-218">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="fc623-219">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-219">Click **Add String**.</span></span>
29. <span data-ttu-id="fc623-220">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-220">Click **OK**.</span></span>
30. <span data-ttu-id="fc623-221">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="fc623-222">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-222">Click **Add String**.</span></span>
32. <span data-ttu-id="fc623-223">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-223">Click **OK**.</span></span>
33. <span data-ttu-id="fc623-224">ツリーで、**Xml\Message\Payments\Item\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="fc623-225">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-225">Click **Add String**.</span></span>
35. <span data-ttu-id="fc623-226">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-226">Click **OK**.</span></span>
36. <span data-ttu-id="fc623-227">ツリーで、**Xml\Message\Payments\Item\Description** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="fc623-228">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-228">Click **Add String**.</span></span>
38. <span data-ttu-id="fc623-229">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-229">Click **OK**.</span></span>
39. <span data-ttu-id="fc623-230">ツリーで、**Xml\Message\Payments\Item\Amount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="fc623-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="fc623-231">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-231">Click **Add String**.</span></span>
41. <span data-ttu-id="fc623-232">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-232">Click **OK**.</span></span>
42. <span data-ttu-id="fc623-233">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fc623-233">Click **Save**.</span></span>
43. <span data-ttu-id="fc623-234">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fc623-234">Close the page.</span></span>

