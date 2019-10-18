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
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184948"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="d961e-103">ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="d961e-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d961e-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER)の形式コンフィギュレーション作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="d961e-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="d961e-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="d961e-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="d961e-106">この例では、サンプル会社 Litware、Inc. の形式コンフィギュレーションを作成します。これらの手順を完了するには、先に「選択したデータソースへのモデルのマッピング」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d961e-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="d961e-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="d961e-107">Create a new format configuration</span></span>
1. <span data-ttu-id="d961e-108">**組織管理 > ワークスペース > 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="d961e-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="d961e-109">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="d961e-110">ツリーで、**支払 (単純化モデル)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="d961e-111">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d961e-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="d961e-112">**コンフィギュレーションの作成**が表示されない場合は、**電子申告のパラメーター**ページでデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d961e-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="d961e-113">**新規**フィールドで、**PaymentModel データ モデルに基づいた書式**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="d961e-114">**名前**フィールドに、**BACS (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="d961e-115">**説明**フィールドに、**BACS 仕入先支払形式 (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="d961e-116">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="d961e-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="d961e-117">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="d961e-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="d961e-118">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="d961e-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="d961e-119">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="d961e-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="d961e-120">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="d961e-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="d961e-121">**データ モデル定義**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="d961e-122">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-122">Click **Create configuration**.</span></span> <span data-ttu-id="d961e-123">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="d961e-123">A new configuration has been created.</span></span> <span data-ttu-id="d961e-124">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d961e-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="d961e-125">電子ドキュメントの形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="d961e-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="d961e-126">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-126">Click **Designer**.</span></span>
2. <span data-ttu-id="d961e-127">**ルートの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d961e-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="d961e-128">ツリーで、**Common\File** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="d961e-129">**名前**フィールドに、**Xml** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="d961e-130">**エンコード**フィールドに、**UTF-8** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="d961e-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-131">Click **OK**.</span></span>
7. <span data-ttu-id="d961e-132">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-132">Click **Add**.</span></span>
8. <span data-ttu-id="d961e-133">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="d961e-134">**名前**フィールドに、**メッセージ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="d961e-135">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-135">Click **OK**.</span></span>
11. <span data-ttu-id="d961e-136">ツリーで、**Xml\Message** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="d961e-137">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="d961e-138">**名前**フィールドに、**ProcessingDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="d961e-139">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-139">Click **OK**.</span></span>
15. <span data-ttu-id="d961e-140">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="d961e-141">名前フィールドに、**MessageId** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="d961e-142">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-142">Click **OK**.</span></span>
18. <span data-ttu-id="d961e-143">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="d961e-144">**名前**フィールドに、**支払**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="d961e-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-145">Click **OK**.</span></span>
21. <span data-ttu-id="d961e-146">ツリーで、**Xml\Message\Payments** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="d961e-147">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="d961e-148">**名前**フィールドに、**品目**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="d961e-149">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-149">Click **OK**.</span></span>
25. <span data-ttu-id="d961e-150">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="d961e-151">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-151">Click **Add**.</span></span>
27. <span data-ttu-id="d961e-152">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="d961e-153">名前フィールドに、**Id** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="d961e-154">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-154">Click **OK**.</span></span>
30. <span data-ttu-id="d961e-155">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-155">Click **Add**.</span></span>
31. <span data-ttu-id="d961e-156">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="d961e-157">名前フィールドに、**仕入先**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="d961e-158">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-158">Click **OK**.</span></span>
34. <span data-ttu-id="d961e-159">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="d961e-160">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="d961e-161">名前フィールドに、**名前**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="d961e-162">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-162">Click **OK**.</span></span>
38. <span data-ttu-id="d961e-163">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="d961e-164">**名前**フィールドに、**銀行**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="d961e-165">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-165">Click **OK**.</span></span>
41. <span data-ttu-id="d961e-166">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="d961e-167">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="d961e-168">**名前**フィールドに、**RoutingNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="d961e-169">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-169">Click **OK**.</span></span>
45. <span data-ttu-id="d961e-170">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="d961e-171">**名前**フィールドに、**AccountNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="d961e-172">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-172">Click **OK**.</span></span>
48. <span data-ttu-id="d961e-173">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="d961e-174">**コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-174">Click **Copy**.</span></span>
50. <span data-ttu-id="d961e-175">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="d961e-176">**ペースト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-176">Click **Paste**.</span></span>
52. <span data-ttu-id="d961e-177">**名前**フィールドに、**支払人**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="d961e-178">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="d961e-179">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="d961e-180">**名前**フィールドに、**通貨**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="d961e-181">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-181">Click **OK**.</span></span>
57. <span data-ttu-id="d961e-182">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="d961e-183">**名前**フィールドに、**説明**と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="d961e-184">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-184">Click **OK**.</span></span>
60. <span data-ttu-id="d961e-185">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="d961e-186">名前フィールドに、**TransDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="d961e-187">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-187">Click **OK**.</span></span>
63. <span data-ttu-id="d961e-188">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="d961e-189">名前フィールドに、**Amount** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="d961e-190">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="d961e-191">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="d961e-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="d961e-192">ツリーで、**Xml\Message\ProcessingDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="d961e-193">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d961e-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="d961e-194">ツリーで、**Text\DateTime** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="d961e-195">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="d961e-196">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-196">Click **OK**.</span></span>
6. <span data-ttu-id="d961e-197">ツリーで、**Xml\Message\Payments\Item\TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="d961e-198">**日時を追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="d961e-199">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="d961e-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="d961e-200">**DateTime** 型フィールドで、**日付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="d961e-201">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-201">Click **OK**.</span></span>
11. <span data-ttu-id="d961e-202">ツリーで、**Xml\Message\MessageId** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="d961e-203">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="d961e-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="d961e-204">ツリーで、**Text\String** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="d961e-205">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-205">Click **OK**.</span></span>
15. <span data-ttu-id="d961e-206">ツリーで、**Xml\Message\Payments\Item\Vendor\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="d961e-207">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-207">Click **Add String**.</span></span>
17. <span data-ttu-id="d961e-208">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-208">Click **OK**.</span></span>
18. <span data-ttu-id="d961e-209">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="d961e-210">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-210">Click **Add String**.</span></span>
20. <span data-ttu-id="d961e-211">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-211">Click **OK**.</span></span>
21. <span data-ttu-id="d961e-212">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="d961e-213">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-213">Click **Add String**.</span></span>
23. <span data-ttu-id="d961e-214">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-214">Click **OK**.</span></span>
24. <span data-ttu-id="d961e-215">ツリーで、**Xml\Message\Payments\Item\Payer\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="d961e-216">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-216">Click **Add String**.</span></span>
26. <span data-ttu-id="d961e-217">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-217">Click **OK**.</span></span>
27. <span data-ttu-id="d961e-218">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="d961e-219">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-219">Click **Add String**.</span></span>
29. <span data-ttu-id="d961e-220">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-220">Click **OK**.</span></span>
30. <span data-ttu-id="d961e-221">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="d961e-222">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-222">Click **Add String**.</span></span>
32. <span data-ttu-id="d961e-223">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-223">Click **OK**.</span></span>
33. <span data-ttu-id="d961e-224">ツリーで、**Xml\Message\Payments\Item\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="d961e-225">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-225">Click **Add String**.</span></span>
35. <span data-ttu-id="d961e-226">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-226">Click **OK**.</span></span>
36. <span data-ttu-id="d961e-227">ツリーで、**Xml\Message\Payments\Item\Description** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="d961e-228">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-228">Click **Add String**.</span></span>
38. <span data-ttu-id="d961e-229">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-229">Click **OK**.</span></span>
39. <span data-ttu-id="d961e-230">ツリーで、**Xml\Message\Payments\Item\Amount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="d961e-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="d961e-231">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-231">Click **Add String**.</span></span>
41. <span data-ttu-id="d961e-232">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-232">Click **OK**.</span></span>
42. <span data-ttu-id="d961e-233">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="d961e-233">Click **Save**.</span></span>
43. <span data-ttu-id="d961e-234">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d961e-234">Close the page.</span></span>

