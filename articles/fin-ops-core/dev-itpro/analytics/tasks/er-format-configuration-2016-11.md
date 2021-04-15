---
title: ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)
description: このトピックでは、電子申告 (ER) 用の形式コンフィギュレーションを作成する方法について説明します。
author: NickSelin
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46686b9e4f6197f565a324a9d03cbb695b6a933b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749072"
---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="e4b3b-103">ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="e4b3b-103">ER Create a format configuration (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e4b3b-104">このトピックでは、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER)の形式コンフィギュレーション作成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="e4b3b-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="e4b3b-106">この例では、サンプル会社 Litware、Inc. のフォーマット構成を作成します。この手順を完了するには、まず「選択したデータソースへのモデルのマッピング」に記載の手順のを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Map model to selected datasources" procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e4b3b-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="e4b3b-107">Create a new format configuration</span></span>
1. <span data-ttu-id="e4b3b-108">**組織管理 > ワークスペース > 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-108">Go to **Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="e4b3b-109">**コンフィギュレーションをレポートする** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-109">Click **Reporting configurations**.</span></span>
3. <span data-ttu-id="e4b3b-110">ツリーで、**支払 (単純化モデル)** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-110">In the tree, select **Payments (simplified model)**.</span></span>
4. <span data-ttu-id="e4b3b-111">**コンフィギュレーションの作成** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-111">Click **Create configuration** to open the drop dialog.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e4b3b-112">**コンフィギュレーションの作成** が表示されない場合は、**電子申告のパラメーター** ページでデザイン モードを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-112">If you don't see **Create configuration**, you must enable design mode on the **Electronic reporting parameters** page.</span></span> 
 
5. <span data-ttu-id="e4b3b-113">**新規** フィールドで、**PaymentModel データ モデルに基づいた書式** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-113">In the **New** field, enter **Format based on data model PaymentModel**.</span></span>
6. <span data-ttu-id="e4b3b-114">**名前** フィールドに、**BACS (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-114">In the **Name** field, type **BACS (UK fictitious)**.</span></span>
7. <span data-ttu-id="e4b3b-115">**説明** フィールドに、**BACS 仕入先支払形式 (英国企業)** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-115">In the **Description** field, type **BACS vendor payment format (UK fictitious)**.</span></span>
    * <span data-ttu-id="e4b3b-116">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-116">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="e4b3b-117">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-117">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="e4b3b-118">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-118">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="e4b3b-119">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-119">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="e4b3b-120">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-120">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="e4b3b-121">**データ モデル定義** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-121">In the **Data model definition** field, enter or select a value.</span></span>
9. <span data-ttu-id="e4b3b-122">**コンフィギュレーションの作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-122">Click **Create configuration**.</span></span> <span data-ttu-id="e4b3b-123">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-123">A new configuration has been created.</span></span> <span data-ttu-id="e4b3b-124">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-124">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-the-format-of-an-electronic-document"></a><span data-ttu-id="e4b3b-125">電子ドキュメントの形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="e4b3b-125">Design the format of an electronic document</span></span>
1. <span data-ttu-id="e4b3b-126">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-126">Click **Designer**.</span></span>
2. <span data-ttu-id="e4b3b-127">**ルートの追加** をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-127">Click **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="e4b3b-128">ツリーで、**Common\File** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-128">In the tree, select **Common\File**.</span></span>
4. <span data-ttu-id="e4b3b-129">**名前** フィールドに、**Xml** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-129">In the **Name** field, type **Xml**.</span></span>
5. <span data-ttu-id="e4b3b-130">**エンコード** フィールドに、**UTF-8** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-130">In the **Encoding** field, type **UTF-8**.</span></span>
6. <span data-ttu-id="e4b3b-131">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-131">Click **OK**.</span></span>
7. <span data-ttu-id="e4b3b-132">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-132">Click **Add**.</span></span>
8. <span data-ttu-id="e4b3b-133">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-133">In the tree, select **XML\Element**.</span></span>
9. <span data-ttu-id="e4b3b-134">**名前** フィールドに、**メッセージ** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-134">In the **Name** field, type **Message**.</span></span>
10. <span data-ttu-id="e4b3b-135">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-135">Click **OK**.</span></span>
11. <span data-ttu-id="e4b3b-136">ツリーで、**Xml\Message** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-136">In the tree, select **Xml\Message**.</span></span>
12. <span data-ttu-id="e4b3b-137">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-137">Click **Add Element**.</span></span>
13. <span data-ttu-id="e4b3b-138">**名前** フィールドに、**ProcessingDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-138">In the **Name** field, type **ProcessingDate**.</span></span>
14. <span data-ttu-id="e4b3b-139">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-139">Click **OK**.</span></span>
15. <span data-ttu-id="e4b3b-140">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-140">Click **Add Element**.</span></span>
16. <span data-ttu-id="e4b3b-141">名前フィールドに、**MessageId** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-141">In the Name field, type **MessageId**.</span></span>
17. <span data-ttu-id="e4b3b-142">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-142">Click **OK**.</span></span>
18. <span data-ttu-id="e4b3b-143">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-143">Click **Add Element**.</span></span>
19. <span data-ttu-id="e4b3b-144">**名前** フィールドに、**支払** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-144">In the **Name** field, type **Payments**.</span></span>
20. <span data-ttu-id="e4b3b-145">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-145">Click **OK**.</span></span>
21. <span data-ttu-id="e4b3b-146">ツリーで、**Xml\Message\Payments** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-146">In the tree, select **Xml\Message\Payments**.</span></span>
22. <span data-ttu-id="e4b3b-147">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-147">Click **Add Element**.</span></span>
23. <span data-ttu-id="e4b3b-148">**名前** フィールドに、**品目** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-148">In the **Name** field, type **Item**.</span></span>
24. <span data-ttu-id="e4b3b-149">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-149">Click **OK**.</span></span>
25. <span data-ttu-id="e4b3b-150">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-150">In the tree, select **Xml\Message\Payments\Item**.</span></span>
26. <span data-ttu-id="e4b3b-151">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-151">Click **Add**.</span></span>
27. <span data-ttu-id="e4b3b-152">ツリーで、**XML\Attribute** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-152">In the tree, select **XML\Attribute**.</span></span>
28. <span data-ttu-id="e4b3b-153">名前フィールドに、**Id** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-153">In the Name field, type **Id**.</span></span>
29. <span data-ttu-id="e4b3b-154">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-154">Click **OK**.</span></span>
30. <span data-ttu-id="e4b3b-155">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-155">Click **Add**.</span></span>
31. <span data-ttu-id="e4b3b-156">ツリーで、**XML\Element** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-156">In the tree, select **XML\Element**.</span></span>
32. <span data-ttu-id="e4b3b-157">名前フィールドに、**仕入先** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-157">In the Name field, type **Vendor**.</span></span>
33. <span data-ttu-id="e4b3b-158">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-158">Click **OK**.</span></span>
34. <span data-ttu-id="e4b3b-159">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-159">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
35. <span data-ttu-id="e4b3b-160">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-160">Click **Add Element**.</span></span>
36. <span data-ttu-id="e4b3b-161">名前フィールドに、**名前** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-161">In the Name field, type **Name**.</span></span>
37. <span data-ttu-id="e4b3b-162">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-162">Click **OK**.</span></span>
38. <span data-ttu-id="e4b3b-163">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-163">Click **Add Element**.</span></span>
39. <span data-ttu-id="e4b3b-164">**名前** フィールドに、**銀行** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-164">In the **Name** field, type **Bank**.</span></span>
40. <span data-ttu-id="e4b3b-165">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-165">Click **OK**.</span></span>
41. <span data-ttu-id="e4b3b-166">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-166">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank**.</span></span>
42. <span data-ttu-id="e4b3b-167">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-167">Click **Add Element**.</span></span>
43. <span data-ttu-id="e4b3b-168">**名前** フィールドに、**RoutingNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-168">In the **Name** field, type **RoutingNumber**.</span></span>
44. <span data-ttu-id="e4b3b-169">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-169">Click **OK**.</span></span>
45. <span data-ttu-id="e4b3b-170">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-170">Click **Add Element**.</span></span>
46. <span data-ttu-id="e4b3b-171">**名前** フィールドに、**AccountNumber** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-171">In the **Name** field, type **AccountNumber**.</span></span>
47. <span data-ttu-id="e4b3b-172">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-172">Click **OK**.</span></span>
48. <span data-ttu-id="e4b3b-173">ツリーで、**Xml\Message\Payments\Item\Vendor** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-173">In the tree, select **Xml\Message\Payments\Item\Vendor**.</span></span>
49. <span data-ttu-id="e4b3b-174">**コピー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-174">Click **Copy**.</span></span>
50. <span data-ttu-id="e4b3b-175">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-175">In the tree, select **Xml\Message\Payments\Item**.</span></span>
51. <span data-ttu-id="e4b3b-176">**ペースト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-176">Click **Paste**.</span></span>
52. <span data-ttu-id="e4b3b-177">**名前** フィールドに、**支払人** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-177">In the **Name** field, type **Payer**.</span></span>
53. <span data-ttu-id="e4b3b-178">ツリーで、**Xml\Message\Payments\Item** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-178">In the tree, select **Xml\Message\Payments\Item**.</span></span>
54. <span data-ttu-id="e4b3b-179">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-179">Click **Add Element**.</span></span>
55. <span data-ttu-id="e4b3b-180">**名前** フィールドに、**通貨** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-180">In the **Name** field, type **Currency**.</span></span>
56. <span data-ttu-id="e4b3b-181">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-181">Click **OK**.</span></span>
57. <span data-ttu-id="e4b3b-182">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-182">Click **Add Element**.</span></span>
58. <span data-ttu-id="e4b3b-183">**名前** フィールドに、**説明** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-183">In the **Name** field, type **Description**.</span></span>
59. <span data-ttu-id="e4b3b-184">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-184">Click **OK**.</span></span>
60. <span data-ttu-id="e4b3b-185">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-185">Click **Add Element**.</span></span>
61. <span data-ttu-id="e4b3b-186">名前フィールドに、**TransDate** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-186">In the Name field, type **TransDate**.</span></span>
62. <span data-ttu-id="e4b3b-187">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-187">Click **OK**.</span></span>
63. <span data-ttu-id="e4b3b-188">**要素の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-188">Click **Add Element**.</span></span>
64. <span data-ttu-id="e4b3b-189">名前フィールドに、**Amount** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-189">In the Name field, type **Amount**.</span></span>
65. <span data-ttu-id="e4b3b-190">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-190">Click **OK**.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="e4b3b-191">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-191">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="e4b3b-192">ツリーで、**Xml\Message\ProcessingDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-192">In the tree, select **Xml\Message\ProcessingDate**.</span></span>
2. <span data-ttu-id="e4b3b-193">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-193">Click **Add** to open the drop dialog.</span></span>
3. <span data-ttu-id="e4b3b-194">ツリーで、**Text\DateTime** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-194">In the tree, select **Text\DateTime**.</span></span>
4. <span data-ttu-id="e4b3b-195">**形式** フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-195">In the **Format** field, type **yyyy-MM-dd**.</span></span>
5. <span data-ttu-id="e4b3b-196">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-196">Click **OK**.</span></span>
6. <span data-ttu-id="e4b3b-197">ツリーで、**Xml\Message\Payments\Item\TransDate** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-197">In the tree, select **Xml\Message\Payments\Item\TransDate**.</span></span>
7. <span data-ttu-id="e4b3b-198">**日時を追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-198">Click **Add DateTime**.</span></span>
8. <span data-ttu-id="e4b3b-199">**形式** フィールドに、**yyyy-MM-dd** と入力します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-199">In the **Format** field, type **yyyy-MM-dd**.</span></span>
9. <span data-ttu-id="e4b3b-200">**DateTime** 型フィールドで、**日付** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-200">In the **DateTime** type field, select **Date**.</span></span>
10. <span data-ttu-id="e4b3b-201">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-201">Click **OK**.</span></span>
11. <span data-ttu-id="e4b3b-202">ツリーで、**Xml\Message\MessageId** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-202">In the tree, select **Xml\Message\MessageId**.</span></span>
12. <span data-ttu-id="e4b3b-203">**追加** をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-203">Click **Add** to open the drop dialog.</span></span>
13. <span data-ttu-id="e4b3b-204">ツリーで、**Text\String** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-204">In the tree, select **Text\String**.</span></span>
14. <span data-ttu-id="e4b3b-205">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-205">Click **OK**.</span></span>
15. <span data-ttu-id="e4b3b-206">ツリーで、**Xml\Message\Payments\Item\Vendor\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-206">In the tree, select **Xml\Message\Payments\Item\Vendor\Name**.</span></span>
16. <span data-ttu-id="e4b3b-207">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-207">Click **Add String**.</span></span>
17. <span data-ttu-id="e4b3b-208">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-208">Click **OK**.</span></span>
18. <span data-ttu-id="e4b3b-209">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-209">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber**.</span></span>
19. <span data-ttu-id="e4b3b-210">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-210">Click **Add String**.</span></span>
20. <span data-ttu-id="e4b3b-211">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-211">Click **OK**.</span></span>
21. <span data-ttu-id="e4b3b-212">ツリーで、**Xml\Message\Payments\Item\Vendor\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-212">In the tree, select **Xml\Message\Payments\Item\Vendor\Bank\AccountNumber**.</span></span>
22. <span data-ttu-id="e4b3b-213">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-213">Click **Add String**.</span></span>
23. <span data-ttu-id="e4b3b-214">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-214">Click **OK**.</span></span>
24. <span data-ttu-id="e4b3b-215">ツリーで、**Xml\Message\Payments\Item\Payer\Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-215">In the tree, select **Xml\Message\Payments\Item\Payer\Name**.</span></span>
25. <span data-ttu-id="e4b3b-216">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-216">Click **Add String**.</span></span>
26. <span data-ttu-id="e4b3b-217">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-217">Click **OK**.</span></span>
27. <span data-ttu-id="e4b3b-218">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\RoutingNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-218">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\RoutingNumber**.</span></span>
28. <span data-ttu-id="e4b3b-219">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-219">Click **Add String**.</span></span>
29. <span data-ttu-id="e4b3b-220">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-220">Click **OK**.</span></span>
30. <span data-ttu-id="e4b3b-221">ツリーで、**Xml\Message\Payments\Item\Payer\Bank\AccountNumber** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-221">In the tree, select **Xml\Message\Payments\Item\Payer\Bank\AccountNumber**.</span></span>
31. <span data-ttu-id="e4b3b-222">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-222">Click **Add String**.</span></span>
32. <span data-ttu-id="e4b3b-223">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-223">Click **OK**.</span></span>
33. <span data-ttu-id="e4b3b-224">ツリーで、**Xml\Message\Payments\Item\Currency** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-224">In the tree, select **Xml\Message\Payments\Item\Currency**.</span></span>
34. <span data-ttu-id="e4b3b-225">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-225">Click **Add String**.</span></span>
35. <span data-ttu-id="e4b3b-226">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-226">Click **OK**.</span></span>
36. <span data-ttu-id="e4b3b-227">ツリーで、**Xml\Message\Payments\Item\Description** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-227">In the tree, select **Xml\Message\Payments\Item\Description**.</span></span>
37. <span data-ttu-id="e4b3b-228">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-228">Click **Add String**.</span></span>
38. <span data-ttu-id="e4b3b-229">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-229">Click **OK**.</span></span>
39. <span data-ttu-id="e4b3b-230">ツリーで、**Xml\Message\Payments\Item\Amount** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-230">In the tree, select **Xml\Message\Payments\Item\Amount**.</span></span>
40. <span data-ttu-id="e4b3b-231">**文字列の追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-231">Click **Add String**.</span></span>
41. <span data-ttu-id="e4b3b-232">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-232">Click **OK**.</span></span>
42. <span data-ttu-id="e4b3b-233">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-233">Click **Save**.</span></span>
43. <span data-ttu-id="e4b3b-234">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="e4b3b-234">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]