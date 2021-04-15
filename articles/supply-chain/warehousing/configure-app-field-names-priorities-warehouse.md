---
title: 倉庫管理モバイル アプリのフィールドを構成する
description: このトピックでは、倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法について説明します。
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField, WHSMobileAppFieldPriority
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269434
ms.assetid: 6cf3d7da-29bb-4d3d-aaf5-544ca9cc2980
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mafoge
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6ed726536085b836f4014c59ea8df4755577ab5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808825"
---
# <a name="configure-fields-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="35c1b-103">倉庫管理モバイル アプリのフィールドを構成する</span><span class="sxs-lookup"><span data-stu-id="35c1b-103">Configure fields for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35c1b-104">このトピックでは、倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-104">This topic describes how to define and configure names and priorities of fields shown in the Warehouse Management mobile app.</span></span>

> [!NOTE]
> <span data-ttu-id="35c1b-105">このトピックは、倉庫管理の機能に適用されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-105">This topic applies to features in Warehouse management.</span></span> <span data-ttu-id="35c1b-106">在庫管理の機能には適用しません。</span><span class="sxs-lookup"><span data-stu-id="35c1b-106">It doesn’t apply to features in Inventory management.</span></span> <span data-ttu-id="35c1b-107">倉庫管理モバイル アプリは、倉庫タスクの実行に使用できるアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="35c1b-107">The Warehouse Management mobile app is an application that you can use to perform warehouse tasks.</span></span> <span data-ttu-id="35c1b-108">アプリで使用されるフィールド名を定義してコンフィギュレーションし、フィールド名に割り当てる優先順位をフィールド名をコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-108">You can define and configure the field names that are used in the app, as well as configure the priority to which the field names should be assigned.</span></span> <span data-ttu-id="35c1b-109">このトピックでは、これらの倉庫管理モバイル アプリのフィールド名と優先順位の定義および構成方法と使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-109">This topic explains how to define and configure these Warehouse Management mobile app field names and priorities, and how they are used.</span></span>

## <a name="configure-warehouse-app-field-names"></a><span data-ttu-id="35c1b-110">倉庫アプリ フィールド名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="35c1b-110">Configure warehouse app field names</span></span>

<span data-ttu-id="35c1b-111">Warehousing をモバイル デバイスで使用するときに、**倉庫アプリ フィールド名** ページでお使いのデバイスにメタデータをどのように表示するかをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-111">When you use Warehousing on your mobile device, you can configure how metadata should be displayed on your device on the **Warehouse app field names** page.</span></span> <span data-ttu-id="35c1b-112">新しい会社で、**既定の設定の作成** をクリックして倉庫モバイル デバイス ワークフローで使用されるすべてのフィールド名を生成してから、優先される入力モードと入力タイプを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-112">In a new company, select **Create default setup** to generate all field names that will be used in the warehouse mobile device workflows, and then assign a preferred input mode and input type to them.</span></span> <span data-ttu-id="35c1b-113">すべてのフィールド名を生成すると、次の入力オプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-113">After you have generated all field names, you can select the following input options.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35c1b-114">オプション</span><span class="sxs-lookup"><span data-stu-id="35c1b-114">Option</span></span></th>
<th><span data-ttu-id="35c1b-115">説明</span><span class="sxs-lookup"><span data-stu-id="35c1b-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35c1b-116">優先入力モード</span><span class="sxs-lookup"><span data-stu-id="35c1b-116">Preferred input mode</span></span></td>
<td><span data-ttu-id="35c1b-117">このオプションは、スキャン フィールドまたは手動入力フィールドを選択したフィールド名に表示するかどうかを定義します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-117">This option defines whether a scanning field or a manual entry input field should be shown for the selected field name.</span></span> <span data-ttu-id="35c1b-118">これは、バーコードがフィールドに使用されるかどうかによって、フィールドを区別する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-118">This is useful to distinguish fields depending on if barcodes are used for the field.</span></span> <span data-ttu-id="35c1b-119"><strong>注記:</strong> 優先入力モードを <strong>スキャン</strong> に設定したフィールド名では、バーコードが読み取れない場合や破損している場合に手動で情報を入力できます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-119"><strong>Note:</strong> For field names with preferred input mode set to <strong>Scanning</strong>, you can enter information manually if the barcode is unreadable or damaged.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35c1b-120">入力タイプ</span><span class="sxs-lookup"><span data-stu-id="35c1b-120">Input type</span></span></td>
<td><span data-ttu-id="35c1b-121">このオプションは、どの入力タイプを選択したフィールド名に使用するかを定義します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-121">This option defines what input type should be used for the selected field name.</span></span> <span data-ttu-id="35c1b-122">次の 4 つのオプションが使用可能です。</span><span class="sxs-lookup"><span data-stu-id="35c1b-122">Four options are available:</span></span>
<ul>
<li><span data-ttu-id="35c1b-123"><strong>選択</strong> - 選択するオプションの一覧を含みます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-123"><strong>Selection</strong> - Contains a list of options to choose from.</span></span> <span data-ttu-id="35c1b-124">このオプションのフィールド名は編集できません。</span><span class="sxs-lookup"><span data-stu-id="35c1b-124">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="35c1b-125"><strong>日付</strong> - 日付として指定されたフィールド名がラベルとともに日付形式で表示されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-125"><strong>Date</strong> - Field names specified as date will show a date format with the label.</span></span> <span data-ttu-id="35c1b-126">これは、倉庫作業者が日付を入力する形式を確認するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-126">This helps warehouse workers see in which format to enter the date.</span></span> <span data-ttu-id="35c1b-127">このオプションのフィールド名は編集できません。</span><span class="sxs-lookup"><span data-stu-id="35c1b-127">Field names with this option are not editable.</span></span></li>
<li><span data-ttu-id="35c1b-128"><strong>アルファ</strong> - 選択されている場合、アプリに手動で情報を入力する際にデバイス キーボードを使用します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-128"><strong>Alpha</strong> - If selected, the device keyboard will be used when entering information manually in the app.</span></span> <span data-ttu-id="35c1b-129">使用するデバイスに応じて、キーボード エクスペリエンスを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-129">The keyboard experience can be changed depending on which device is used.</span></span></li>
<li><span data-ttu-id="35c1b-130"><strong>数値</strong> - 数値入力のみを使用するフィールド名では、このオプションを選択してデバイス キーボードではなくカスタムのテンキーを入力フィールドとともに表示できます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-130"><strong>Numeric</strong> - For field names that use numeric input only, you can select this option to display a custom numeric keypad with the input field instead of the device keyboard.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configure-warehouse-app-field-priority"></a><span data-ttu-id="35c1b-131">倉庫アプリ フィールドの優先順位のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="35c1b-131">Configure warehouse app field priority</span></span>

<span data-ttu-id="35c1b-132">**倉庫アプリ フィールドの優先順位** ページで、フィールド名を異なる優先順位グループに配置できます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-132">On the **Warehouse app field priority** page, you can put field names into different priority groups.</span></span> <span data-ttu-id="35c1b-133">これにより、倉庫作業者がアプリを使用してタスクを実行する際に、どの情報を主要なタスク ページに表示すべきかを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-133">This makes it possible to decide what information should be displayed on the main task page when warehouse workers perform tasks using the app.</span></span> <span data-ttu-id="35c1b-134">**既定の設定の作成** をクリックすると、優先順位グループの既定の設定が生成されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-134">If you click **Create default setup**, a default set of priority groups will be generated.</span></span> <span data-ttu-id="35c1b-135">必要な数だけ優先順位グループを作成することもできますが、3 つの優先順位グループだけがタスク ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-135">It is possible to create as many priority groups as needed, but only three priority groups will be shown on the task page.</span></span> <span data-ttu-id="35c1b-136">システムはアプリにメタデータを送信する際に、優先順位グループに応じて各フィールドに相対的な優先順位を割り当てて、アプリはメタデータを含む上位 3 つの優先順位グループをタスク ページに表示します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-136">When the system sends metadata to the app, it will assign each field a relative priority depending on its priority group, and the app will display the first three priority groups contained in the metadata on the task page.</span></span> <span data-ttu-id="35c1b-137">オーバーフローしているメタデータの残りは、2 番目の詳細ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-137">The rest of the overflowing metadata will be displayed on a secondary details page.</span></span> <span data-ttu-id="35c1b-138">次の表に、5 つの優先順位グループの例を示します。</span><span class="sxs-lookup"><span data-stu-id="35c1b-138">The following table shows an example of five priority groups.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="35c1b-139">優先順位グループ</span><span class="sxs-lookup"><span data-stu-id="35c1b-139">Priority group</span></span></th>
<th><span data-ttu-id="35c1b-140">割り当て済フィールド</span><span class="sxs-lookup"><span data-stu-id="35c1b-140">Assigned fields</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td> <span data-ttu-id="35c1b-141">優先順位 10</span><span class="sxs-lookup"><span data-stu-id="35c1b-141">Priority 10</span></span></td>
<td><ul>
<li><span data-ttu-id="35c1b-142">項目</span><span class="sxs-lookup"><span data-stu-id="35c1b-142">Item</span></span></li>
<li><span data-ttu-id="35c1b-143">件数</span><span class="sxs-lookup"><span data-stu-id="35c1b-143">Quantity</span></span></li>
<li><span data-ttu-id="35c1b-144">計量単位</span><span class="sxs-lookup"><span data-stu-id="35c1b-144">Unit of measure</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="35c1b-145">優先順位 20</span><span class="sxs-lookup"><span data-stu-id="35c1b-145">Priority 20</span></span></td>
<td><ul>
<li><span data-ttu-id="35c1b-146">クラスター位置</span><span class="sxs-lookup"><span data-stu-id="35c1b-146">Cluster position</span></span></li>
<li><span data-ttu-id="35c1b-147">クラスター</span><span class="sxs-lookup"><span data-stu-id="35c1b-147">Cluster</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="35c1b-148">優先順位 30</span><span class="sxs-lookup"><span data-stu-id="35c1b-148">Priority 30</span></span></td>
<td><ul>
<li><span data-ttu-id="35c1b-149">品目の説明</span><span class="sxs-lookup"><span data-stu-id="35c1b-149">Item description</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td> <span data-ttu-id="35c1b-150">優先順位 40</span><span class="sxs-lookup"><span data-stu-id="35c1b-150">Priority 40</span></span></td>
<td><ul>
<li><span data-ttu-id="35c1b-151">構成</span><span class="sxs-lookup"><span data-stu-id="35c1b-151">Configuration</span></span></li>
<li><span data-ttu-id="35c1b-152">色</span><span class="sxs-lookup"><span data-stu-id="35c1b-152">Color</span></span></li>
<li><span data-ttu-id="35c1b-153">サイズ</span><span class="sxs-lookup"><span data-stu-id="35c1b-153">Size</span></span></li>
<li><span data-ttu-id="35c1b-154">スタイル</span><span class="sxs-lookup"><span data-stu-id="35c1b-154">Style</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td> <span data-ttu-id="35c1b-155">優先順位 50</span><span class="sxs-lookup"><span data-stu-id="35c1b-155">Priority 50</span></span></td>
<td><ul>
<li><span data-ttu-id="35c1b-156">保管場所</span><span class="sxs-lookup"><span data-stu-id="35c1b-156">Location</span></span></li>
<li><span data-ttu-id="35c1b-157">ライセンス プレート</span><span class="sxs-lookup"><span data-stu-id="35c1b-157">License plate</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="35c1b-158">たとえば、倉庫作業者がモバイル デバイスのタスクを実行しているときに、アプリケーションに表示されるメタデータが次のフィールドで構成されている場合 :</span><span class="sxs-lookup"><span data-stu-id="35c1b-158">For example, when a warehouse worker is performing a task on a mobile device, if the metadata that will be displayed in the app consists of the following fields:</span></span>

-   <span data-ttu-id="35c1b-159">項目</span><span class="sxs-lookup"><span data-stu-id="35c1b-159">Item</span></span>
-   <span data-ttu-id="35c1b-160">件数</span><span class="sxs-lookup"><span data-stu-id="35c1b-160">Quantity</span></span>
-   <span data-ttu-id="35c1b-161">計量単位</span><span class="sxs-lookup"><span data-stu-id="35c1b-161">Unit of measure</span></span>
-   <span data-ttu-id="35c1b-162">品目の説明</span><span class="sxs-lookup"><span data-stu-id="35c1b-162">Item description</span></span>
-   <span data-ttu-id="35c1b-163">サイズと場所</span><span class="sxs-lookup"><span data-stu-id="35c1b-163">Size and Location</span></span>

<span data-ttu-id="35c1b-164">上の表で設定されている倉庫アプリ フィールドの優先順位に基づいて、情報の次の 3 行は、タスク ページに表示されます :</span><span class="sxs-lookup"><span data-stu-id="35c1b-164">Based on the warehouse app field priority set up in the table above, the following 3 rows of information will be displayed on the task page:</span></span>

-   <span data-ttu-id="35c1b-165">行 1: 品目、数量、測定単位</span><span class="sxs-lookup"><span data-stu-id="35c1b-165">Row 1: Item, Quantity, Unit of measure</span></span>
-   <span data-ttu-id="35c1b-166">行 2: 品目の説明</span><span class="sxs-lookup"><span data-stu-id="35c1b-166">Row 2: Item description</span></span>
-   <span data-ttu-id="35c1b-167">行 3 : サイズ</span><span class="sxs-lookup"><span data-stu-id="35c1b-167">Row 3: Size</span></span>

<span data-ttu-id="35c1b-168">場所などの残りのメタデータは、タスク ページに表示されませんが、詳細ページに表示されます。</span><span class="sxs-lookup"><span data-stu-id="35c1b-168">The remaining metadata, for example, Location, will not be displayed on the task page, but will be displayed on a details page.</span></span> <span data-ttu-id="35c1b-169">ユーザー インターフェイスの詳細や例については、ブログ投稿 [Finance and Operations - Warehousing の発表](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35c1b-169">To learn more and see examples of the user interface, refer to the blog post [Announcing Finance and Operations - Warehousing](https://blogs.msdn.microsoft.com/dynamicsaxscm/2017/01/20/announcing-dynamics-365-for-operations-warehousing/).</span></span>

<a name="additional-resources"></a><span data-ttu-id="35c1b-170">追加リソース</span><span class="sxs-lookup"><span data-stu-id="35c1b-170">Additional resources</span></span>
--------

[<span data-ttu-id="35c1b-171">倉庫管理モバイル アプリのインストールと接続</span><span class="sxs-lookup"><span data-stu-id="35c1b-171">Install and connect the Warehouse Management mobile app</span></span>](../warehousing/install-configure-warehouse-management-app.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]