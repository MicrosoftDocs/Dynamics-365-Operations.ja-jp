---
title: ER データ モデル要素に作成された形式のコンポーネントのマップ (2016 年 11 月)
description: 次の手順では、システム管理者ロールまたは電子申告開発者ロールのいずれかのユーザーが、支払いビジネス ドメインの電子ドキュメント書式を定義する電子レポート (ER) のコンポーネントにデータ モデルをマッピングする様子を示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e77de79113e3f44da1d7f92f17a446df86f6852e
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143033"
---
# <a name="er-map-components-of-the-created-format-to-data-model-elements-november-2016"></a><span data-ttu-id="03fe8-103">ER データ モデル要素に作成された形式のコンポーネントのマップ (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="03fe8-103">ER Map components of the created format to data model elements (November 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03fe8-104">次の手順では、システム管理者ロールまたは電子申告開発者ロールのいずれかのユーザーが、支払いビジネス ドメインの電子ドキュメント書式を定義する電子レポート (ER) のコンポーネントにデータ モデルをマッピングする様子を示します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-104">The following procedure shows how a user in either the System administrator or Electronic reporting developer role can map data model elements to components of the created Electronic reporting (ER) configuration, which defines an electronic document format for the payments business domain.</span></span> <span data-ttu-id="03fe8-105">この書式は、支払を処理するための電子ドキュメントを生成するために後で使用します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-105">This format will be used later to generate electronic documents for processing payments.</span></span> <span data-ttu-id="03fe8-106">この例では、サンプル会社 'Litware、Inc.' の構成のフォーマットを作成します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-106">In this example, you will create a format configuration for the sample company, 'Litware, Inc.'.</span></span> <span data-ttu-id="03fe8-107">ER コンフィギュレーションはすべての会社用に共有されるため、これらのステップはどの会社でも実行できます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-107">These steps can be performed in any company as ER configurations are shared for all companies.</span></span> <span data-ttu-id="03fe8-108">これらの手順を完了するには、まず 「構成のフォーマットを作成する」 タスク ガイドに記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="03fe8-108">To complete these steps, you must first complete the steps in the "Create a format configuration" task guide.</span></span>


## <a name="select-a-format-configuration"></a><span data-ttu-id="03fe8-109">書式コンフィギュレーションの選択</span><span class="sxs-lookup"><span data-stu-id="03fe8-109">Select a format configuration</span></span>
1. <span data-ttu-id="03fe8-110">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="03fe8-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="03fe8-112">ツリーで、「支払 (単純化モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-112">In the tree, expand 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="03fe8-113">ツリーで、「支払 (単純化モデル)」 \BACS (英国の企業) を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-113">In the tree, select 'Payments (simplified model)\BACS (UK fictitious)'.</span></span>
5. <span data-ttu-id="03fe8-114">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-114">Click Designer.</span></span>

## <a name="map-format-components-to-data-model-elements"></a><span data-ttu-id="03fe8-115">データ モデルの要素への形式のコンポーネントのマッピング</span><span class="sxs-lookup"><span data-stu-id="03fe8-115">Map format components to data model elements</span></span>
1. <span data-ttu-id="03fe8-116">[展開] / [折りたたみ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-116">Click Expand/collapse.</span></span>
2. <span data-ttu-id="03fe8-117">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-117">Click the Mapping tab.</span></span>
3. <span data-ttu-id="03fe8-118">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-118">In the tree, expand 'model'.</span></span>
4. <span data-ttu-id="03fe8-119">ツリーで、[Xml\Message\ProcessingDate\DateTime] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-119">In the tree, select 'Xml\Message\ProcessingDate\DateTime'.</span></span>
5. <span data-ttu-id="03fe8-120">ツリーで、[model\ProcessingDateTime] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-120">In the tree, select 'model\ProcessingDateTime'.</span></span>
6. <span data-ttu-id="03fe8-121">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-121">Click Bind.</span></span>
7. <span data-ttu-id="03fe8-122">ツリーで、[Xml\Message\MessageId\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-122">In the tree, select 'Xml\Message\MessageId\String'.</span></span>
8. <span data-ttu-id="03fe8-123">ツリーで、[model\MessageIdentification] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-123">In the tree, select 'model\MessageIdentification'.</span></span>
9. <span data-ttu-id="03fe8-124">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-124">Click Bind.</span></span>
10. <span data-ttu-id="03fe8-125">ツリーで、「model\Payments」を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-125">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="03fe8-126">ツリーで、[Xml\Message\Payments\Item\Amount\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-126">In the tree, select 'Xml\Message\Payments\Item\Amount\String'.</span></span>
12. <span data-ttu-id="03fe8-127">ツリーで、[model\Payments\InstructedAmount] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-127">In the tree, select 'model\Payments\InstructedAmount'.</span></span>
13. <span data-ttu-id="03fe8-128">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-128">Click Bind.</span></span>
14. <span data-ttu-id="03fe8-129">ツリーで、[Xml\Message\Payments\Item\TransDate\DateTime] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-129">In the tree, select 'Xml\Message\Payments\Item\TransDate\DateTime'.</span></span>
15. <span data-ttu-id="03fe8-130">ツリーで、[model\Payments\TransactionDate] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-130">In the tree, select 'model\Payments\TransactionDate'.</span></span>
16. <span data-ttu-id="03fe8-131">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-131">Click Bind.</span></span>
17. <span data-ttu-id="03fe8-132">ツリーで、[Xml\Message\Payments\Item\Description\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-132">In the tree, select 'Xml\Message\Payments\Item\Description\String'.</span></span>
18. <span data-ttu-id="03fe8-133">ツリーで、[model\Payments\Description] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-133">In the tree, select 'model\Payments\Description'.</span></span>
19. <span data-ttu-id="03fe8-134">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-134">Click Bind.</span></span>
20. <span data-ttu-id="03fe8-135">ツリーで、[Xml\Message\Payments\Item\Currency\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-135">In the tree, select 'Xml\Message\Payments\Item\Currency\String'.</span></span>
21. <span data-ttu-id="03fe8-136">ツリーで、「model\Payments\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-136">In the tree, select 'model\Payments\Currency'.</span></span>
22. <span data-ttu-id="03fe8-137">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-137">Click Bind.</span></span>
23. <span data-ttu-id="03fe8-138">ツリーで、[Xml\Message\Payments\Item\Id] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-138">In the tree, select 'Xml\Message\Payments\Item\Id'.</span></span>
24. <span data-ttu-id="03fe8-139">ツリーで、[model\Payments\End2EndID] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-139">In the tree, select 'model\Payments\End2EndID'.</span></span>
25. <span data-ttu-id="03fe8-140">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-140">Click Bind.</span></span>
26. <span data-ttu-id="03fe8-141">ツリーで、[model\Payments\Creditor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-141">In the tree, expand 'model\Payments\Creditor'.</span></span>
27. <span data-ttu-id="03fe8-142">ツリーで、[model\Payments\Creditor\Account] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-142">In the tree, expand 'model\Payments\Creditor\Account'.</span></span>
28. <span data-ttu-id="03fe8-143">ツリーで、[model\Payments\Creditor\Agent] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-143">In the tree, expand 'model\Payments\Creditor\Agent'.</span></span>
29. <span data-ttu-id="03fe8-144">ツリーで、「Xml\Message\Payments\Item\Vendor\Name\String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-144">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name\String'.</span></span>
30. <span data-ttu-id="03fe8-145">ツリーで、[model\Payments\Creditor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-145">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
31. <span data-ttu-id="03fe8-146">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-146">Click Bind.</span></span>
32. <span data-ttu-id="03fe8-147">ツリーで、[Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-147">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber\String'.</span></span>
33. <span data-ttu-id="03fe8-148">ツリーで、[model\Payments\Creditor\Agent\RoutingNumber] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-148">In the tree, select 'model\Payments\Creditor\Agent\RoutingNumber'.</span></span>
34. <span data-ttu-id="03fe8-149">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-149">Click Bind.</span></span>
35. <span data-ttu-id="03fe8-150">ツリーで、[Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-150">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber\String'.</span></span>
36. <span data-ttu-id="03fe8-151">ツリーで、[model\Payments\Creditor\Account\Number] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-151">In the tree, select 'model\Payments\Creditor\Account\Number'.</span></span>
37. <span data-ttu-id="03fe8-152">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-152">Click Bind.</span></span>
38. <span data-ttu-id="03fe8-153">ツリーで、[Xml\Message\Payments\Item\Payer\Name\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-153">In the tree, select 'Xml\Message\Payments\Item\Payer\Name\String'.</span></span>
39. <span data-ttu-id="03fe8-154">ツリーで、[model\Payments\Debtor] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-154">In the tree, expand 'model\Payments\Debtor'.</span></span>
40. <span data-ttu-id="03fe8-155">ツリーで、[model\Payments\Debtor\Account] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-155">In the tree, expand 'model\Payments\Debtor\Account'.</span></span>
41. <span data-ttu-id="03fe8-156">ツリーで、[model\Payments\Debtor\Agent] を展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-156">In the tree, expand 'model\Payments\Debtor\Agent'.</span></span>
42. <span data-ttu-id="03fe8-157">ツリーで、[model\Payments\Debtor\Name] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-157">In the tree, select 'model\Payments\Debtor\Name'.</span></span>
43. <span data-ttu-id="03fe8-158">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-158">Click Bind.</span></span>
44. <span data-ttu-id="03fe8-159">ツリーで、[Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-159">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber\String'.</span></span>
45. <span data-ttu-id="03fe8-160">ツリーで、[model\Payments\Debtor\Agent\RoutingNumber] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-160">In the tree, select 'model\Payments\Debtor\Agent\RoutingNumber'.</span></span>
46. <span data-ttu-id="03fe8-161">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-161">Click Bind.</span></span>
47. <span data-ttu-id="03fe8-162">ツリーで、[Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-162">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber\String'.</span></span>
48. <span data-ttu-id="03fe8-163">ツリーで、[model\Payments\Debtor\Account\Number] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-163">In the tree, select 'model\Payments\Debtor\Account\Number'.</span></span>
49. <span data-ttu-id="03fe8-164">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-164">Click Bind.</span></span>
50. <span data-ttu-id="03fe8-165">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-165">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="03fe8-166">ツリーで、[model\Payments] を選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-166">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="03fe8-167">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-167">Click Bind.</span></span>
53. <span data-ttu-id="03fe8-168">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-168">Click Save.</span></span>

## <a name="validate-format-mapping"></a><span data-ttu-id="03fe8-169">書式マッピングの検証</span><span class="sxs-lookup"><span data-stu-id="03fe8-169">Validate format mapping</span></span>
1. <span data-ttu-id="03fe8-170">[検証] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-170">Click Validate.</span></span>
    * <span data-ttu-id="03fe8-171">新しいマッピングを検証し、すべてのバインディングが要件を満たしていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-171">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="03fe8-172">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-172">Close the page.</span></span>

## <a name="change-status-of-the-current-version-of-format-configuration"></a><span data-ttu-id="03fe8-173">コンフィギュレーションの書式設定の現在のバージョンのステータスの変更</span><span class="sxs-lookup"><span data-stu-id="03fe8-173">Change status of the current version of format configuration</span></span>
<span data-ttu-id="03fe8-174">次の手順では、フォーマット構成のステータスを 「下書き」 から 「完了」 に変更して、支払書類の作成に利用できるように設定します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-174">In the next steps, you'll change the status of the format configuration from Draft to Completed to make it available for payment document generation.</span></span>  
1. <span data-ttu-id="03fe8-175">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-175">Click Change status.</span></span>
2. <span data-ttu-id="03fe8-176">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-176">Click Complete.</span></span>
3. <span data-ttu-id="03fe8-177">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-177">In the Description field, type a value.</span></span>
    * <span data-ttu-id="03fe8-178">例えば、「バージョン 1」。</span><span class="sxs-lookup"><span data-stu-id="03fe8-178">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="03fe8-179">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="03fe8-179">Click OK.</span></span>
5. <span data-ttu-id="03fe8-180">現在のコンフィギュレーションの完了したバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-180">Select completed version of the current configuration.</span></span>
    * <span data-ttu-id="03fe8-181">コンフィギュレーションの設定が完了したバージョン 1.1 として保存されることに注意してください。これはデータ モデルのバージョン 1 に基づく書式のバージョン 1 です。</span><span class="sxs-lookup"><span data-stu-id="03fe8-181">Note that the configuration is saved as completed version 1.1: version 1 of the format based on the version 1 of the data model.</span></span>  

## <a name="define-effective-date-for-completed-version-of-format"></a><span data-ttu-id="03fe8-182">形式の完了したバージョンの有効期間の定義</span><span class="sxs-lookup"><span data-stu-id="03fe8-182">Define effective date for completed version of format</span></span>
<span data-ttu-id="03fe8-183">各書式のバージョンは、特定の日付をから使用開始するように設定できます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-183">Each format version can be configured as available for usage starting from a certain date.</span></span> <span data-ttu-id="03fe8-184">複数の書式のバージョンを特定の日付に有効にする場合は、最新書式 (バージョン番号に基づく) を使用できるように選択します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-184">When more than one format version is active on a certain date, the latest format (based on version number) will be selected for usage.</span></span> <span data-ttu-id="03fe8-185">セッション日付値は、適切なバージョンの選択に使用されます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-185">The session date value is used for proper version selection.</span></span>  

## <a name="restrict-access-to-created-format-from-companies"></a><span data-ttu-id="03fe8-186">会社から作成した形式へのアクセスの制限</span><span class="sxs-lookup"><span data-stu-id="03fe8-186">Restrict access to created format from companies</span></span>
1. <span data-ttu-id="03fe8-187">[ISO 国/地域コード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="03fe8-187">Expand the ISO Country/region codes section.</span></span>
    * <span data-ttu-id="03fe8-188">各書式へのアクセスは、書式が適用される特定の国/地域の ID によって制限することができます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-188">Each format access can be restricted by identifying particular countries/regions in which a format is applicable.</span></span> <span data-ttu-id="03fe8-189">特定の書式の国/地域のリストが空の場合、この書式は任意の会社で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-189">When the list of countries/regions for particular format is empty, this format can be used in any company.</span></span> <span data-ttu-id="03fe8-190">一部の ISO 国/地域コードがその国/地域のリストに挿入された場合、この書式は基本住所がその国/地域にある場合にのみ会社で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="03fe8-190">When some ISO country/region codes are inserted in the list of countries/regions, the format can only be use in companies if the primary address is in the country/region.</span></span>  

