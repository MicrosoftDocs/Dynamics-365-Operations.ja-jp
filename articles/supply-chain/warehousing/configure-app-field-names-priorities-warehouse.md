---
title: "倉庫アプリのアプリ フィールド名のコンフィギュレーション"
description: "このトピックでは、Finance and Operations の倉庫アプリ フィールド名と優先順位の定義およびコンフィギュレーション方法について説明します。"
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0162014189ed6bffb17e6718a67eecfd55c334a5
ms.contentlocale: ja-jp
ms.lasthandoff: 08/07/2018

---

# <a name="configure-app-field-names-in-warehousing-app"></a><span data-ttu-id="006d4-103">倉庫アプリのアプリ フィールド名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="006d4-103">Configure app field names in Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="006d4-104">このトピックでは、Finance and Operations の倉庫アプリ フィールド名と優先順位の定義およびコンフィギュレーション方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="006d4-104">This topic describes how to define and configure warehouse app field names and priorities in Finance and Operations.</span></span> 

<span data-ttu-id="006d4-105">**注記:** このトピックは、倉庫管理の機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-105">**Note:** This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="006d4-106">在庫管理の機能には適用しません。</span><span class="sxs-lookup"><span data-stu-id="006d4-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="006d4-107">Finance and Operations - Warehousing は倉庫作業の実行に使用できるアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="006d4-107">Finance and Operations - Warehousing is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="006d4-108">アプリで使用されるフィールド名を定義してコンフィギュレーションし、フィールド名に割り当てる優先順位をフィールド名をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="006d4-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="006d4-109">このトピックでは、これらの倉庫アプリ フィールド名と優先順位の定義およびコンフィギュレーション方法、および Finance and Operations - Warehousing での使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="006d4-109">This topic explains how to define and configure these warehouse app field names and priorities, and how they are used in Finance and Operations - Warehousing.</span></span> <span data-ttu-id="006d4-110">Finance and Operations - Warehousing への接続をコンフィギュレーションする方法の詳細については、チュートリアル「[Finance and Operations – Warehousing のインストールと構成](install-configure-warehousing-app.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="006d4-110">For detailed information about how to configure the connection to Finance and Operations  - Warehousing, refer to the tutorial [Install and configure Finance and Operations - Warehousing](install-configure-warehousing-app.md).</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="006d4-111">倉庫アプリ フィールド名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="006d4-111">Configure warehouse app field names</span></span>

<span data-ttu-id="006d4-112">Finance and Operations - Warehousing をモバイル デバイスで使用するときに、**倉庫アプリ フィールド名**ページでお使いのデバイスにメタデータをどのように表示するかをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="006d4-112">When you use Finance and Operations - Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="006d4-113">Finance and Operations の新しい会社で、**既定の設定の作成**をクリックして倉庫モバイル デバイス ワークフローで使用されるすべてのフィールド名を生成してから、優先される入力モードと入力タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="006d4-113">In a new company in Finance and Operations, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="006d4-114">すべてのフィールド名を生成すると、次の入力オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="006d4-114">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="006d4-115">オプション</span><span class="sxs-lookup"><span data-stu-id="006d4-115">Option</span></span></th>
<th><span data-ttu-id="006d4-116">説明</span><span class="sxs-lookup"><span data-stu-id="006d4-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="006d4-117">優先入力モード</span><span class="sxs-lookup"><span data-stu-id="006d4-117">Preferred input mode</span></span></td>
<td><span data-ttu-id="006d4-118">このオプションは、スキャン フィールドまたは手動入力フィールドを選択したフィールド名に表示するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="006d4-118">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="006d4-119">これは、バーコードがフィールドに使用されるかどうかによって、フィールドを区別する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="006d4-119">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="006d4-120"><strong>注記:</strong> 優先入力モードを <strong>スキャン</strong> に設定したフィールド名では、バーコードが読み取れない場合や破損している場合に手動で情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="006d4-120"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="006d4-121">入力タイプ</span><span class="sxs-lookup"><span data-stu-id="006d4-121">Input type</span></span></td>
<td><span data-ttu-id="006d4-122">このオプションは、どの入力タイプを選択したフィールド名に使用するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="006d4-122">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="006d4-123">次の 4 つのオプションが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="006d4-123">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="006d4-124"><strong>選択</strong> - 選択するオプションの一覧を含みます。</span><span class="sxs-lookup"><span data-stu-id="006d4-124"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="006d4-125">このオプションのフィールド名は編集できません。</span><span class="sxs-lookup"><span data-stu-id="006d4-125">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="006d4-126"><strong>日付</strong> - 日付として指定されたフィールド名がラベルとともに日付形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-126"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="006d4-127">これは、倉庫作業者が日付を入力する形式を確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="006d4-127">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="006d4-128">このオプションのフィールド名は編集できません。</span><span class="sxs-lookup"><span data-stu-id="006d4-128">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="006d4-129"><strong>アルファ</strong> - 選択されている場合、アプリに手動で情報を入力する際にデバイス キーボードを使用します。</span><span class="sxs-lookup"><span data-stu-id="006d4-129"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="006d4-130">使用するデバイスに応じて、キーボード エクスペリエンスを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="006d4-130">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="006d4-131"><strong>数値</strong> - 数値入力のみを使用するフィールド名では、このオプションを選択してデバイス キーボードではなくカスタムのテンキーを入力フィールドとともに表示できます。</span><span class="sxs-lookup"><span data-stu-id="006d4-131"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="006d4-132">倉庫アプリ フィールドの優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="006d4-132">Configure warehouse app field priority</span></span>

<span data-ttu-id="006d4-133">**倉庫アプリ フィールドの優先順位**ページで、フィールド名を異なる優先順位グループに配置できます。</span><span class="sxs-lookup"><span data-stu-id="006d4-133">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="006d4-134">これにより、倉庫作業者がアプリを使用してタスクを実行する際に、どの情報を主要なタスク ページに表示すべきかを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="006d4-134">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="006d4-135">**既定の設定の作成**をクリックすると、優先順位グループの既定の設定が生成されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-135">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="006d4-136">必要な数だけ優先順位グループを作成することもできますが、3 つの優先順位グループだけがタスク ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-136">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="006d4-137">Finance and Operations はアプリにメタデータを送信する際に、優先順位グループに応じて各フィールドに相対的な優先順位を割り当てて、アプリはメタデータを含む上位 3 つの優先順位グループをタスク ページに表示します。</span><span class="sxs-lookup"><span data-stu-id="006d4-137">When Finance and Operations sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="006d4-138">オーバーフローしているメタデータの残りは、2 番目の詳細ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-138">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="006d4-139">次の表に、5 つの優先順位グループの例を示します。</span><span class="sxs-lookup"><span data-stu-id="006d4-139">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="006d4-140">優先順位グループ</span><span class="sxs-lookup"><span data-stu-id="006d4-140">Priority group</span></span></th>
<th><span data-ttu-id="006d4-141">割り当て済フィールド</span><span class="sxs-lookup"><span data-stu-id="006d4-141">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="006d4-142">優先順位 10</span><span class="sxs-lookup"><span data-stu-id="006d4-142">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="006d4-143">項目</span><span class="sxs-lookup"><span data-stu-id="006d4-143">Item</span></span></li>
<li><span data-ttu-id="006d4-144">件数</span><span class="sxs-lookup"><span data-stu-id="006d4-144">Quantity</span></span></li>
<li><span data-ttu-id="006d4-145">計量単位</span><span class="sxs-lookup"><span data-stu-id="006d4-145">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="006d4-146">優先順位 20</span><span class="sxs-lookup"><span data-stu-id="006d4-146">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="006d4-147">クラスター位置</span><span class="sxs-lookup"><span data-stu-id="006d4-147">Cluster position</span></span></li>
<li><span data-ttu-id="006d4-148">クラスター</span><span class="sxs-lookup"><span data-stu-id="006d4-148">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="006d4-149">優先順位 30</span><span class="sxs-lookup"><span data-stu-id="006d4-149">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="006d4-150">品目の説明</span><span class="sxs-lookup"><span data-stu-id="006d4-150">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="006d4-151">優先順位 40</span><span class="sxs-lookup"><span data-stu-id="006d4-151">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="006d4-152">構成</span><span class="sxs-lookup"><span data-stu-id="006d4-152">Configuration</span></span></li>
<li><span data-ttu-id="006d4-153">色</span><span class="sxs-lookup"><span data-stu-id="006d4-153">Color</span></span></li>
<li><span data-ttu-id="006d4-154">サイズ</span><span class="sxs-lookup"><span data-stu-id="006d4-154">Size</span></span></li>
<li><span data-ttu-id="006d4-155">スタイル</span><span class="sxs-lookup"><span data-stu-id="006d4-155">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="006d4-156">優先順位 50</span><span class="sxs-lookup"><span data-stu-id="006d4-156">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="006d4-157">保管場所</span><span class="sxs-lookup"><span data-stu-id="006d4-157">Location</span></span></li>
<li><span data-ttu-id="006d4-158">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="006d4-158">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="006d4-159">たとえば、倉庫作業者がモバイル デバイスのタスクを実行しているときに、アプリケーションに表示されるメタデータが次のフィールドで構成されている場合 :</span><span class="sxs-lookup"><span data-stu-id="006d4-159">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="006d4-160">項目</span><span class="sxs-lookup"><span data-stu-id="006d4-160">Item</span></span>
-   <span data-ttu-id="006d4-161">件数</span><span class="sxs-lookup"><span data-stu-id="006d4-161">Quantity</span></span>
-   <span data-ttu-id="006d4-162">計量単位</span><span class="sxs-lookup"><span data-stu-id="006d4-162">Unit of measure</span></span>
-   <span data-ttu-id="006d4-163">品目の説明</span><span class="sxs-lookup"><span data-stu-id="006d4-163">Item description</span></span>
-   <span data-ttu-id="006d4-164">サイズと場所</span><span class="sxs-lookup"><span data-stu-id="006d4-164">Size and Location</span></span>

<span data-ttu-id="006d4-165">上の表で設定されている倉庫アプリ フィールドの優先順位に基づいて、情報の次の 3 行は、タスク ページに表示されます :</span><span class="sxs-lookup"><span data-stu-id="006d4-165">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="006d4-166">行 1: 品目、数量、測定単位</span><span class="sxs-lookup"><span data-stu-id="006d4-166">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="006d4-167">行 2: 品目の説明</span><span class="sxs-lookup"><span data-stu-id="006d4-167">Row 2: Item description</span></span>
-   <span data-ttu-id="006d4-168">行 3 : サイズ</span><span class="sxs-lookup"><span data-stu-id="006d4-168">Row 3: Size</span></span>

<span data-ttu-id="006d4-169">場所などの残りのメタデータは、タスク ページに表示されませんが、詳細ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="006d4-169">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="006d4-170">ユーザー インターフェイスの詳細や例については、ブログ投稿「[Finance and Operations - Warehousing の発表](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="006d4-170">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="006d4-171">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="006d4-171">Additional resources</span></span>
--------

[<span data-ttu-id="006d4-172">Microsoft Dynamics 365 for Finance and Operations – Warehousing のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="006d4-172">Install and configure Microsoft Dynamics 365 for Finance and Operations – Warehousing</span></span>](install-configure-warehousing-app.md)




