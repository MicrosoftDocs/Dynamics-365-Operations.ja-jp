--- 
title: "ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 11/27/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 13469aad7fdcefb3a1706eec0527f29968e007eb
ms.openlocfilehash: 10511fe5b936135471b522fc7152a54686a3be87
ms.contentlocale: ja-jp
ms.lasthandoff: 12/18/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="50b42-103">ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="50b42-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50b42-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="50b42-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="50b42-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="50b42-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="50b42-106">この例では、サンプル会社 Litware、Inc. の形式コンフィギュレーションを作成します。これらの手順を完了するには、先に「選択したデータソースへのモデルのマッピング」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="50b42-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="50b42-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="50b42-107">Create a new format configuration</span></span>
1. <span data-ttu-id="50b42-108">**組織管理 > ワークスペース > 電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="50b42-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="50b42-109">**コンフィギュレーションをレポートする**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="50b42-110">ツリーで、**支払 (単純化モデル)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="50b42-111">**コンフィギュレーションの作成**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="50b42-111">Click **Create configuration** to open the drop dialog.</span></span>
 > [!NOTE]
 > <span data-ttu-id="50b42-112">**コンフィギュレーションの作成**が表示されない場合は、**電子申告のパラメーター**ページでデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50b42-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
5. <span data-ttu-id="50b42-113">**新規**フィールドで、**PaymentModel データ モデルに基づいた書式**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="50b42-114">**名前**フィールドに、**BACS (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="50b42-115">**説明**フィールドに、**BACS 仕入先支払形式 (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="50b42-116">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="50b42-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="50b42-117">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="50b42-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="50b42-118">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="50b42-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="50b42-119">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="50b42-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="50b42-120">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="50b42-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="50b42-121">**データ モデル定義**フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="50b42-122">**コンフィギュレーションの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-122">Click **Create configuration**.</span></span> <span data-ttu-id="50b42-123">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="50b42-123">A new configuration has been created.</span></span> <span data-ttu-id="50b42-124">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="50b42-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  
 > [!NOTE]
 > <span data-ttu-id="50b42-125">**コンフィギュレーションの作成**が表示されない場合は、**電子申告のパラメーター**ページでデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="50b42-125">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span>


## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="50b42-126">電子ドキュメントの形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="50b42-126">Design the format of an electronic document</span></span>
1. <span data-ttu-id="50b42-127">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-127">Click **Designer**.</span></span>
2. <span data-ttu-id="50b42-128">**ルートの追加**をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="50b42-128">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="50b42-129">ツリーで、**Common\File** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-129">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="50b42-130">**名前**フィールドに、**Xml** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-130">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="50b42-131">**エンコード**フィールドに、**UTF-8** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-131">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="50b42-132">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-132">Click **OK**.</span></span>
7. <span data-ttu-id="50b42-133">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-133">Click **Add**.</span></span>
8. <span data-ttu-id="50b42-134">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-134">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="50b42-135">**名前**フィールドに、**メッセージ**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-135">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="50b42-136">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-136">Click **OK**.</span></span>
11. <span data-ttu-id="50b42-137">ツリーで、**Xml\Message** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-137">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="50b42-138">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-138">Click **Add Element**.</span></span>
13. <span data-ttu-id="50b42-139">**名前**フィールドに、**ProcessingDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-139">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="50b42-140">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-140">Click **OK**.</span></span>
15. <span data-ttu-id="50b42-141">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-141">Click **Add Element**.</span></span>
16. <span data-ttu-id="50b42-142">名前フィールドに、**MessageId** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-142">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="50b42-143">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-143">Click **OK**.</span></span>
18. <span data-ttu-id="50b42-144">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-144">Click **Add Element**.</span></span>
19. <span data-ttu-id="50b42-145">**名前**フィールドに、**支払**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-145">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="50b42-146">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-146">Click **OK**.</span></span>
21. <span data-ttu-id="50b42-147">ツリーで、**Xml\Message\Payments** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-147">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="50b42-148">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-148">Click **Add Element**.</span></span>
23. <span data-ttu-id="50b42-149">**名前**フィールドに、**品目**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-149">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="50b42-150">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-150">Click **OK**.</span></span>
25. <span data-ttu-id="50b42-151">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-151">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="50b42-152">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-152">Click **Add**.</span></span>
27. <span data-ttu-id="50b42-153">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-153">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="50b42-154">名前フィールドに、**Id** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-154">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="50b42-155">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-155">Click **OK**.</span></span>
30. <span data-ttu-id="50b42-156">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-156">Click **Add**.</span></span>
31. <span data-ttu-id="50b42-157">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-157">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="50b42-158">名前フィールドに、**仕入先**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-158">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="50b42-159">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-159">Click **OK**.</span></span>
34. <span data-ttu-id="50b42-160">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-160">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="50b42-161">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-161">Click **Add Element**.</span></span>
36. <span data-ttu-id="50b42-162">名前フィールドに、**名前**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-162">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="50b42-163">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-163">Click **OK**.</span></span>
38. <span data-ttu-id="50b42-164">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-164">Click **Add Element**.</span></span>
39. <span data-ttu-id="50b42-165">**名前**フィールドに、**銀行**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-165">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="50b42-166">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-166">Click **OK**.</span></span>
41. <span data-ttu-id="50b42-167">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-167">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="50b42-168">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-168">Click **Add Element**.</span></span>
43. <span data-ttu-id="50b42-169">**名前**フィールドに、**RoutingNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-169">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="50b42-170">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-170">Click **OK**.</span></span>
45. <span data-ttu-id="50b42-171">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-171">Click **Add Element**.</span></span>
46. <span data-ttu-id="50b42-172">**名前**フィールドに、**AccountNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-172">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="50b42-173">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-173">Click **OK**.</span></span>
48. <span data-ttu-id="50b42-174">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-174">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="50b42-175">**コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-175">Click **Copy**.</span></span>
50. <span data-ttu-id="50b42-176">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-176">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="50b42-177">**ペースト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-177">Click **Paste**.</span></span>
52. <span data-ttu-id="50b42-178">**名前**フィールドに、**支払人**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-178">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="50b42-179">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-179">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="50b42-180">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-180">Click **Add Element**.</span></span>
55. <span data-ttu-id="50b42-181">**名前**フィールドに、**通貨**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-181">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="50b42-182">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-182">Click **OK**.</span></span>
57. <span data-ttu-id="50b42-183">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-183">Click **Add Element**.</span></span>
58. <span data-ttu-id="50b42-184">**名前**フィールドに、**説明**と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-184">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="50b42-185">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-185">Click **OK**.</span></span>
60. <span data-ttu-id="50b42-186">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-186">Click **Add Element**.</span></span>
61. <span data-ttu-id="50b42-187">名前フィールドに、**TransDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-187">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="50b42-188">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-188">Click **OK**.</span></span>
63. <span data-ttu-id="50b42-189">**要素の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-189">Click **Add Element**.</span></span>
64. <span data-ttu-id="50b42-190">名前フィールドに、**Amount** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-190">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="50b42-191">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-191">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="50b42-192">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="50b42-192">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="50b42-193">ツリーで、**Xml\Message\ProcessingDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-193">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="50b42-194">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="50b42-194">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="50b42-195">ツリーで、**Text\DateTime** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-195">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="50b42-196">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-196">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="50b42-197">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-197">Click **OK**.</span></span>
6. <span data-ttu-id="50b42-198">ツリーで、**Xml\Message\Payments\Item\TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-198">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="50b42-199">**日時を追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-199">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="50b42-200">**形式**フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="50b42-200">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="50b42-201">**DateTime** 型フィールドで、**日付**を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-201">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="50b42-202">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-202">Click **OK**.</span></span>
11. <span data-ttu-id="50b42-203">ツリーで、**Xml\Message\MessageId** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-203">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="50b42-204">**追加**をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="50b42-204">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="50b42-205">ツリーで、**Text\String** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-205">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="50b42-206">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-206">Click **OK**.</span></span>
15. <span data-ttu-id="50b42-207">ツリーで、**Xml\Message\Payments\Item\Vendor\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-207">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="50b42-208">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-208">Click **Add String**.</span></span>
17. <span data-ttu-id="50b42-209">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-209">Click **OK**.</span></span>
18. <span data-ttu-id="50b42-210">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-210">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="50b42-211">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-211">Click **Add String**.</span></span>
20. <span data-ttu-id="50b42-212">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-212">Click **OK**.</span></span>
21. <span data-ttu-id="50b42-213">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-213">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="50b42-214">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-214">Click **Add String**.</span></span>
23. <span data-ttu-id="50b42-215">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-215">Click **OK**.</span></span>
24. <span data-ttu-id="50b42-216">ツリーで、**Xml\Message\Payments\Item\Payer\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-216">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="50b42-217">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-217">Click **Add String**.</span></span>
26. <span data-ttu-id="50b42-218">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-218">Click **OK**.</span></span>
27. <span data-ttu-id="50b42-219">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-219">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="50b42-220">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-220">Click **Add String**.</span></span>
29. <span data-ttu-id="50b42-221">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-221">Click **OK**.</span></span>
30. <span data-ttu-id="50b42-222">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-222">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="50b42-223">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-223">Click **Add String**.</span></span>
32. <span data-ttu-id="50b42-224">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-224">Click **OK**.</span></span>
33. <span data-ttu-id="50b42-225">ツリーで、**Xml\Message\Payments\Item\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-225">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="50b42-226">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-226">Click **Add String**.</span></span>
35. <span data-ttu-id="50b42-227">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-227">Click **OK**.</span></span>
36. <span data-ttu-id="50b42-228">ツリーで、**Xml\Message\Payments\Item\Description** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-228">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="50b42-229">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-229">Click **Add String**.</span></span>
38. <span data-ttu-id="50b42-230">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-230">Click **OK**.</span></span>
39. <span data-ttu-id="50b42-231">ツリーで、**Xml\Message\Payments\Item\Amount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50b42-231">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="50b42-232">**文字列の追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-232">Click **Add String**.</span></span>
41. <span data-ttu-id="50b42-233">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-233">Click **OK**.</span></span>
42. <span data-ttu-id="50b42-234">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="50b42-234">Click **Save**.</span></span>
43. <span data-ttu-id="50b42-235">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="50b42-235">Close the page.</span></span>


