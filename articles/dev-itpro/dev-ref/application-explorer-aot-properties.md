---
title: "アプリケーション エクスプローラーのプロパティ"
description: "このトピックでは、アプリケーション エクスプローラーの品目向けに Microsoft Visual Studio の [プロパティ] ウィンドウに表示されるプロパティについて説明します。"
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: reference
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 85213
ms.assetid: ca186dda-8a78-4969-9be0-b81be00892e5
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c6c6eaa9152652df1b78f6ad42b5025913ccec4d
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="application-explorer-properties"></a><span data-ttu-id="93299-103">アプリケーション エクスプローラーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-103">Application Explorer properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93299-104">このトピックでは、アプリケーション エクスプローラーの品目向けに Microsoft Visual Studio の [プロパティ] ウィンドウに表示されるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-104">This topic describes the properties that appear in the Properties window of Microsoft Visual Studio for items in Application Explorer.</span></span>

<span data-ttu-id="93299-105">アプリケーション エクスプローラーの多くのノードは、それに関連付けられているプロパティを持つ要素を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-105">Many nodes in Application Explorer represent elements that have properties associated with them.</span></span> <span data-ttu-id="93299-106">Microsoft Visual Studio の **プロパティ** ウィンドウで、これらのプロパティを読み取りまたは変更することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-106">You can read or modify these properties in the **Properties** window of Microsoft Visual Studio.</span></span>

## <a name="system-and-common-properties"></a><span data-ttu-id="93299-107">システムと共通プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-107">System and common properties</span></span>
<span data-ttu-id="93299-108">アプリケーション エクスプローラーのほとんどのアプリケーション オブジェクトには、システム プロパティの標準セットがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-108">Most application objects in Application Explorer have a standard set of system properties.</span></span> <span data-ttu-id="93299-109">これらのシステム プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-109">These system properties are read-only.</span></span> <span data-ttu-id="93299-110">**プロパティ** ウィンドウを使用すると、アプリケーション エクスプローラーで任意の項目のプロパティを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-110">You can use the **Properties** window to view the properties for any item in Application Explorer.</span></span> <span data-ttu-id="93299-111">**プロパティ** ウィンドウを開くには、アプリケーション エクスプローラーでノードを右クリックし、**プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93299-111">To open the **Properties** window, right-click a node in Application Explorer, and then click **Properties**.</span></span> <span data-ttu-id="93299-112">**カテゴリ**のタブの**プロパティ**ウィンドウで、多数のシステム プロパティが、**統計**ノードの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-112">On the **Categories** tab of the **Properties** window, many system properties are listed under the **Statistics** node.</span></span> <span data-ttu-id="93299-113">この記事では、すべてではないが多くのアプリケーション エクスプローラー ノードで繰り返される追加の共通プロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-113">This article lists additional common properties that are repeated on many, but not all, Application Explorer nodes.</span></span> <span data-ttu-id="93299-114">次のテーブルは、多くのアプリケーション エクスプローラー ノードで検出されるシステム プロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-114">The following table shows the system properties that are found on almost all Application Explorer nodes.</span></span> <span data-ttu-id="93299-115">これらすべてのシステム プロパティは読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-115">All these system properties are read-only.</span></span>

| <span data-ttu-id="93299-116">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-116">Property</span></span>     | <span data-ttu-id="93299-117">説明</span><span class="sxs-lookup"><span data-stu-id="93299-117">Description</span></span>                                                       |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="93299-118">ChangedBy</span><span class="sxs-lookup"><span data-stu-id="93299-118">ChangedBy</span></span>    | <span data-ttu-id="93299-119">オブジェクト (多くの場合はリリース バージョン) を最後に変更したユーザー。</span><span class="sxs-lookup"><span data-stu-id="93299-119">The user who last changed the object (often the release version).</span></span> |
| <span data-ttu-id="93299-120">ChangedDate</span><span class="sxs-lookup"><span data-stu-id="93299-120">ChangedDate</span></span>  | <span data-ttu-id="93299-121">オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="93299-121">The date when the object was last changed.</span></span>                        |
| <span data-ttu-id="93299-122">ChangedTime</span><span class="sxs-lookup"><span data-stu-id="93299-122">ChangedTime</span></span>  | <span data-ttu-id="93299-123">オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="93299-123">The time when the object was last changed.</span></span>                        |
| <span data-ttu-id="93299-124">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="93299-124">CreatedBy</span></span>    | <span data-ttu-id="93299-125">オブジェクトを作成したユーザー。</span><span class="sxs-lookup"><span data-stu-id="93299-125">The user who created the object.</span></span>                                  |
| <span data-ttu-id="93299-126">CreationDate</span><span class="sxs-lookup"><span data-stu-id="93299-126">CreationDate</span></span> | <span data-ttu-id="93299-127">オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="93299-127">The date when the object was created.</span></span>                             |
| <span data-ttu-id="93299-128">CreationTime</span><span class="sxs-lookup"><span data-stu-id="93299-128">CreationTime</span></span> | <span data-ttu-id="93299-129">オブジェクトが作成された時間。</span><span class="sxs-lookup"><span data-stu-id="93299-129">The time when the object was created.</span></span>                             |

<span data-ttu-id="93299-130">次のテーブルは、すべてではないが、多くのアプリケーション エクスプローラー ノードで検出されるその他の一般的なプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-130">The following table shows other common properties that are found on many, but not all, Application Explorer nodes.</span></span>

| <span data-ttu-id="93299-131">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-131">Property</span></span>          | <span data-ttu-id="93299-132">説明</span><span class="sxs-lookup"><span data-stu-id="93299-132">Description</span></span>                                                                                                                                                                                                                                                                                                          |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-133">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-133">ConfigurationKey</span></span>  | <span data-ttu-id="93299-134">要素へのアクセスまたは表示を制御するコンフィギュレーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-134">Specify the configuration key that controls access to or display of an element.</span></span> <span data-ttu-id="93299-135">ユーザーがコンフィギュレーション キーにアクセスできない場合は、要素は表示されません。</span><span class="sxs-lookup"><span data-stu-id="93299-135">If a user doesn't have access to the configuration key, the element isn't visible.</span></span> <span data-ttu-id="93299-136">要素には、ページ、ページのコントロール、テーブル、およびその他の要素があります。</span><span class="sxs-lookup"><span data-stu-id="93299-136">Elements include pages, controls on pages, tables, and other elements.</span></span>                                                                            |
| <span data-ttu-id="93299-137">LegacyID</span><span class="sxs-lookup"><span data-stu-id="93299-137">LegacyID</span></span>          | <span data-ttu-id="93299-138">以前のバージョンからの識別子要素です。</span><span class="sxs-lookup"><span data-stu-id="93299-138">An identifier element from an earlier version.</span></span> <span data-ttu-id="93299-139">以前のバージョンからの更新中に、古い識別子が **LegacyID** に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="93299-139">During upgrade from a previous version, the old identifier is assigned to **LegacyID**.</span></span> <span data-ttu-id="93299-140">インストール固有の識別子は割り当てられず、ビジネス ロジックは保持されます。</span><span class="sxs-lookup"><span data-stu-id="93299-140">An installation-specific identifier isn't assigned, and business logic remains intact.</span></span> <span data-ttu-id="93299-141">このプロパティは、新しい要素には使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-141">This property isn't used for new elements.</span></span>                                             |
| <span data-ttu-id="93299-142">NeededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="93299-142">NeededAccessLevel</span></span> | <span data-ttu-id="93299-143">ユーザーが必要とする最小アクセスレベル。</span><span class="sxs-lookup"><span data-stu-id="93299-143">The minimum access level that a user requires.</span></span> <span data-ttu-id="93299-144">このプロパティは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-144">This property is read-only.</span></span>                                                                                                                                                                                                                                           |
| <span data-ttu-id="93299-145">元金額</span><span class="sxs-lookup"><span data-stu-id="93299-145">Origin</span></span>            | <span data-ttu-id="93299-146">アプリケーション エクスプローラー要素のグローバル一意識別子 (GUID)。</span><span class="sxs-lookup"><span data-stu-id="93299-146">The globally unique identifier (GUID) of an Application Explorer element.</span></span> <span data-ttu-id="93299-147">このプロパティは、同期中およびアップグレード時に要素を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-147">This property is used to identify elements during synchronization and in upgrade scenarios.</span></span> <span data-ttu-id="93299-148">これは読み取り専用のプロパティで、システムが割り当てると値が変わることはありません。</span><span class="sxs-lookup"><span data-stu-id="93299-148">It's a read-only property, and the value never changes after the system assigns it.</span></span> <span data-ttu-id="93299-149">システムのどの場所にも重複する元の GUID 値はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-149">No origin GUID value is duplicated anywhere in the system.</span></span> |
| <span data-ttu-id="93299-150">SecurityKey</span><span class="sxs-lookup"><span data-stu-id="93299-150">SecurityKey</span></span>       | <span data-ttu-id="93299-151">このプロパティは廃止されましたが、以前のバージョンからアップグレードされたシステムでは参照のために保持されます。</span><span class="sxs-lookup"><span data-stu-id="93299-151">This property is obsolete but is retained for reference in systems that were upgraded from an earlier version.</span></span>                                                                                                                                                                                                       |

## <a name="base-enum-properties"></a><span data-ttu-id="93299-152">基本列挙型のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-152">Base enum properties</span></span>
<span data-ttu-id="93299-153">次のテーブルに、列挙型で使用可能なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-153">The following table describes the properties that are available for enumerations.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-154">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-154">Property</span></span></th>
<th><span data-ttu-id="93299-155">説明</span><span class="sxs-lookup"><span data-stu-id="93299-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-156">AnalysisUsage</span><span class="sxs-lookup"><span data-stu-id="93299-156">AnalysisUsage</span></span></td>
<td><span data-ttu-id="93299-157">キューブにおける列挙値の役割を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-157">Specify the role of the enumeration in a cube.</span></span> <span data-ttu-id="93299-158">この設定は、列挙を参照するすべてのテーブル フィールドに自動的に反映されます。</span><span class="sxs-lookup"><span data-stu-id="93299-158">This setting is automatically propagated to all table fields that reference the enumeration.</span></span> <span data-ttu-id="93299-159">ただし、テーブル フィールドの設定を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-159">However, you can override the setting on a table field.</span></span> <span data-ttu-id="93299-160"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-160">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-161"><strong>属性 </strong>- 列挙を参照するフィールドは、分析コードの属性です。</span><span class="sxs-lookup"><span data-stu-id="93299-161"><strong>Attribute </strong>– A field that references the enumeration is a dimension attribute.</span></span></li>
<li><span data-ttu-id="93299-162"><strong>なし </strong>- 列挙を参照するフィールドは、分析コードの属性ではありません。</span><span class="sxs-lookup"><span data-stu-id="93299-162"><strong>None </strong>– A field that references the enumeration isn&#39;t a dimension attribute.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-163">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-163">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-164">構成キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-164">Specify the configuration key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-165">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-165">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-166">ビューが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-166">Specify the codes for the countries/regions where the view is applicable or valid.</span></span> <span data-ttu-id="93299-167">このプロパティは、ISO (国際標準化機構) 国/地域コードをコンマで区切った単一の文字列のリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-167">This property is implemented as a comma-separated list of International Organization for Standardization (ISO) country/region codes in a single string.</span></span> <span data-ttu-id="93299-168">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-168">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-169">クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-169">The client framework and application might use this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-170">DisplayLength</span><span class="sxs-lookup"><span data-stu-id="93299-170">DisplayLength</span></span></td>
<td><span data-ttu-id="93299-171">表示される文字数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-171">Specify the number of characters that are shown.</span></span> <span data-ttu-id="93299-172">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-172">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-173">ヘルプ</span><span class="sxs-lookup"><span data-stu-id="93299-173">Help</span></span></td>
<td><span data-ttu-id="93299-174">フィールドのヘルプ文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-174">Create a Help string for the field.</span></span> <span data-ttu-id="93299-175">フィールドがページで使用されている場合は、ヘルプ文字列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-175">The Help string is shown when the field is used on a page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-176">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-176">Label</span></span></td>
<td><span data-ttu-id="93299-177">ページおよびレポートに表示されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-177">Specify the label that is shown on pages and reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-178">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-178">Model</span></span></td>
<td><span data-ttu-id="93299-179">テーブルがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-179">Specify the model that the table is in.</span></span> <span data-ttu-id="93299-180">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-180">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-181">要素例には、テーブルおよびクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-181">Examples of elements include a table and a class.</span></span> <span data-ttu-id="93299-182">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-182">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-183">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-183">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-184">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-184">Name</span></span></td>
<td><span data-ttu-id="93299-185">列挙名を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-185">Specify the enumeration name.</span></span> <span data-ttu-id="93299-186">列挙名は、可能な列挙値または列挙値のタイプのいずれかを示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-186">An enumeration name must indicate either the possible enumeration values or the type of the enumeration value.</span></span> <span data-ttu-id="93299-187">可能な値に従って呼ばれる列挙型の例には、<strong>InclExcl</strong> および <strong>NextPrevious</strong> があります。</span><span class="sxs-lookup"><span data-stu-id="93299-187">Examples of enumerations that are named according to the possible values are <strong>InclExcl</strong> and <strong>NextPrevious</strong>.</span></span> <span data-ttu-id="93299-188">列挙値タイプに従って呼ばれる列挙型例には、<strong>ArrivalPostingType</strong> および <strong>ListStatus</strong> があります。</span><span class="sxs-lookup"><span data-stu-id="93299-188">Examples of enumerations that are named according to the type of the enumeration value are <strong>ArrivalPostingType</strong> and <strong>ListStatus</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-189">スタイル</span><span class="sxs-lookup"><span data-stu-id="93299-189">Style</span></span></td>
<td><span data-ttu-id="93299-190">列挙型の既定の外観を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-190">Change the default appearance of the enumeration.</span></span> <span data-ttu-id="93299-191"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-191">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-192">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="93299-192">Combo box</span></span></li>
<li><span data-ttu-id="93299-193">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="93299-193">Radio button</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-194">UseEnumValue</span><span class="sxs-lookup"><span data-stu-id="93299-194">UseEnumValue</span></span></td>
<td><span data-ttu-id="93299-195"><strong>はい</strong>の値は、<strong>EnumValue</strong> プロパティの規定値が変更されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-195">A value of <strong>Yes</strong> indicates that default values of the <strong>EnumValue</strong> property were modified.</span></span> <span data-ttu-id="93299-196"><strong>いいえ</strong>の値は、<strong>EnumValue</strong> プロパティを既定値にリセットします。</span><span class="sxs-lookup"><span data-stu-id="93299-196">A value of <strong>No</strong> resets the <strong>EnumValue</strong> property to the default values.</span></span></td>
</tr>
</tbody>
</table>

## <a name="extended-data-type-properties"></a><span data-ttu-id="93299-197">拡張データ型プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-197">Extended data type properties</span></span>
<span data-ttu-id="93299-198">拡張データ型 (EDT) プロパティーは、すべての EDTs に共通であるか、または特定の基本データ型に対してのみ使用可能かに基づいて、以下のグループに分類されます。</span><span class="sxs-lookup"><span data-stu-id="93299-198">Extended data type (EDT) properties are divided into the following groups, based on whether they are common to all EDTs or available only for certain base data types.</span></span>

### <a name="properties-that-are-common-to-all-edts"></a><span data-ttu-id="93299-199">すべての EDT に共通のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-199">Properties that are common to all EDTs</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-200">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-200">Property</span></span></th>
<th><span data-ttu-id="93299-201">説明</span><span class="sxs-lookup"><span data-stu-id="93299-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-202">配置</span><span class="sxs-lookup"><span data-stu-id="93299-202">Alignment</span></span></td>
<td><span data-ttu-id="93299-203">現在のテキストの配置を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-203">Change the alignment of the text.</span></span> <span data-ttu-id="93299-204"><strong>左</strong>、<strong>右</strong>、または <strong>中央</strong> を選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-204">The available options are <strong>Left</strong>, <strong>Right</strong>, and <strong>Center</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-205">AnalysisDefaultSort</span><span class="sxs-lookup"><span data-stu-id="93299-205">AnalysisDefaultSort</span></span></td>
<td><span data-ttu-id="93299-206">この EDT を含むレポート モデルでフィールドの既定の並べ替え順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-206">Specify the default sort order for a field in a report model that has this EDT.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-207">AnalysisDefaultTotal</span><span class="sxs-lookup"><span data-stu-id="93299-207">AnalysisDefaultTotal</span></span></td>
<td><span data-ttu-id="93299-208">メジャーの集計関数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-208">Specify the aggregate function for a measure.</span></span> <span data-ttu-id="93299-209"><strong>AnalysisUsage</strong> プロパティが<strong>測定</strong>に設定されている場合、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-209">Use this property when the <strong>AnalysisUsage</strong> property is set to <strong>Measure</strong>.</span></span> <span data-ttu-id="93299-210"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-210">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-211"><strong>合計 </strong>- セット内のすべての値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-211"><strong>Sum </strong>– Return the sum of all the values in a set.</span></span></li>
<li><span data-ttu-id="93299-212"><strong>カウント</strong> - セット内の null 以外の品目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-212"><strong>Count </strong>– Return the number of non-null items in a set.</span></span></li>
<li><span data-ttu-id="93299-213"><strong>CountDistinct</strong> - セット内の特徴的な null 以外の品目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-213"><strong>CountDistinct </strong>– Return the number of distinct non-null items in a set.</span></span></li>
<li><span data-ttu-id="93299-214"><strong>最小</strong> - セット内の最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-214"><strong>Min </strong>– Return the minimum value in a set.</span></span></li>
<li><span data-ttu-id="93299-215"><strong>最大</strong> - セット内の最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-215"><strong>Max </strong>– Return the maximum value in a set.</span></span></li>
<li><span data-ttu-id="93299-216"><strong>なし</strong> - 集計関数は適用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-216"><strong>None </strong>– No aggregate function is applied.</span></span></li>
<li><span data-ttu-id="93299-217"><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-217"><strong>Auto </strong>– This option applies to derived EDTs.</span></span> <span data-ttu-id="93299-218">親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="93299-218">The value of the <strong>AnalysisUsage</strong> property for the parent EDT is used.</span></span></li>
</ul>
<span data-ttu-id="93299-219">フィールド レベルで集計関数をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-219">You can override the aggregate function at the field level.</span></span> <span data-ttu-id="93299-220">つまり、そのフィールドの <strong>AnalysisDefaultTotal</strong> プロパティを使用することで、フィールドの集計関数を変更できます。</span><span class="sxs-lookup"><span data-stu-id="93299-220">In other words, you can change the aggregate function for the field by using the <strong>AnalysisDefaultTotal</strong> property for that field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-221">AnalysisGrouping</span><span class="sxs-lookup"><span data-stu-id="93299-221">AnalysisGrouping</span></span></td>
<td><span data-ttu-id="93299-222">Microsoft SQL Server Reporting Services (SSRS) のレポート ビルダーを使用してフィールドがレポートに追加されるとき、この EDT フィールドを持つフィールドが既定でグループ化されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-222">Specify whether a field that has this EDT is grouped by default when the field is added to a report by using Report Builder for Microsoft SQL Server Reporting Services (SSRS).</span></span> <span data-ttu-id="93299-223">このプロパティは、通貨量について自動的に<strong>非推奨</strong>に設定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-223">This property is automatically set to <strong>Discouraged</strong> for currency amounts.</span></span> <span data-ttu-id="93299-224">一意であるその他のフィールドについては、このプロパティを<strong>非推奨</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-224">For other fields that are unique, you should set this property to <strong>Discouraged</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-225">AnalysisUsage</span><span class="sxs-lookup"><span data-stu-id="93299-225">AnalysisUsage</span></span></td>
<td><span data-ttu-id="93299-226">キューブにおける EDT の役割を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-226">Specify the role of the EDT in a cube.</span></span> <span data-ttu-id="93299-227">この設定は、EDT を参照するすべてのテーブル フィールドに自動的に反映されます。</span><span class="sxs-lookup"><span data-stu-id="93299-227">This setting is automatically propagated to all table fields that reference the EDT.</span></span> <span data-ttu-id="93299-228">ただし、テーブル フィールドの設定を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-228">However, you can override the setting on a table field.</span></span> <span data-ttu-id="93299-229"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-229">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-230"><strong>属性 </strong>- EDT を参照するフィールドは、分析コードの属性です。</span><span class="sxs-lookup"><span data-stu-id="93299-230"><strong>Attribute </strong>– A field that references the EDT is a dimension attribute.</span></span></li>
<li><span data-ttu-id="93299-231"><strong>測定 </strong>- EDT を参照するフィールドは測定です。</span><span class="sxs-lookup"><span data-stu-id="93299-231"><strong>Measure </strong>– A field that references the EDT is a measure.</span></span></li>
<li><span data-ttu-id="93299-232"><strong>両方 </strong>- EDT を参照するフィールドは、分析コードの属性と測定の両方です。</span><span class="sxs-lookup"><span data-stu-id="93299-232"><strong>Both </strong>– A field that references the EDT is both a dimension attribute and a measure.</span></span></li>
<li><span data-ttu-id="93299-233"><strong>なし </strong>- EDT を参照するフィールドは、分析コードの属性でも測定でもありません。</span><span class="sxs-lookup"><span data-stu-id="93299-233"><strong>None </strong>– A field that references the EDT is neither a dimension attribute nor a measure.</span></span></li>
<li><span data-ttu-id="93299-234"><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-234"><strong>Auto </strong>– This option applies to derived EDTs.</span></span> <span data-ttu-id="93299-235">親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="93299-235">The value of the <strong>AnalysisUsage</strong> property for the parent EDT is used.</span></span></li>
</ul><span data-ttu-id="93299-236">
<strong>注記:</strong> 列挙型に基づいたデータ型は、測定することができません。</span><span class="sxs-lookup"><span data-stu-id="93299-236">
<strong>Note:</strong> Data types that are based on enumerations can&#39;t be measures.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-237">ArrayLength</span><span class="sxs-lookup"><span data-stu-id="93299-237">ArrayLength</span></span></td>
<td><span data-ttu-id="93299-238">このプロパティは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-238">This property is a read-only.</span></span> <span data-ttu-id="93299-239">既定値は <strong>1</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-239">The default value is <strong>1</strong>.</span></span> <span data-ttu-id="93299-240">配列要素を EDT に追加するには、<strong>配列要素</strong> ノードを右クリックし、<strong>新規配列要素</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93299-240">To add array elements to the EDT, right-click the <strong>Array Element</strong> node, and then click <strong>New Array Element</strong>.</span></span> <span data-ttu-id="93299-241"><strong>ArrayLength</strong> プロパティの値が増加してこの変更を反映します。</span><span class="sxs-lookup"><span data-stu-id="93299-241">The value of the <strong>ArrayLength</strong> property is increased to reflect this change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-242">ButtonImage</span><span class="sxs-lookup"><span data-stu-id="93299-242">ButtonImage</span></span></td>
<td><span data-ttu-id="93299-243">ページのルックアップ ボタンに EDT が使用されるときに表示されるイメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-243">Specify the image that is shown when the EDT is used for a lookup button on a page.</span></span> <span data-ttu-id="93299-244"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-244">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-245"><strong>方向キー</strong></span><span class="sxs-lookup"><span data-stu-id="93299-245"><strong>Arrow</strong></span></span></li>
<li><span data-ttu-id="93299-246"><strong>メール</strong> - たとえば、<strong>電子メール</strong>タイプに対してこのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-246"><strong>Mail</strong> – You can select this option for the <strong>e-mail</strong> type, for example.</span></span></li>
<li><span data-ttu-id="93299-247"><strong>URL</strong> - たとえば、<strong>URL</strong> タイプに対してこのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-247"><strong>URL</strong> – You can select this option for the <strong>URL</strong> type, for example.</span></span></li>
<li><span data-ttu-id="93299-248"><strong>ThreeDots</strong> (...)</span><span class="sxs-lookup"><span data-stu-id="93299-248"><strong>ThreeDots</strong> (...)</span></span></li>
<li><span data-ttu-id="93299-249"><strong>OpenFile</strong> - たとえば、<strong>FilenameOpen</strong> および <strong>FilenameSave</strong> タイプに対してこのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-249"><strong>OpenFile</strong> – You can select this option for the <strong>FilenameOpen</strong> and <strong>FilenameSave</strong> types, for example.</span></span></li>
<li><span data-ttu-id="93299-250"><strong>カレンダー</strong> - たとえば、日付タイプに対してこのオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-250"><strong>Calendar</strong> – You can select this option for date types, for example.</span></span></li>
</ul>
<span data-ttu-id="93299-251">既定値は <strong>矢印</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-251">The default value is <strong>Arrow</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-252">CollectionLabel</span><span class="sxs-lookup"><span data-stu-id="93299-252">CollectionLabel</span></span></td>
<td><span data-ttu-id="93299-253">この EDT を持つフィールドの複数系の名前を表示するために使用するラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-253">Specify the label that is used to show the plural name of a field that has this EDT.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-254">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-254">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-255">EDT の構成キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-255">Specify the configuration key for the EDT.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-256">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-256">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-257">メニューが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-257">Specify the codes for the countries/regions where the menu is applicable or valid.</span></span> <span data-ttu-id="93299-258">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-258">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-259">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-259">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-260">クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-260">The client uses this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-261">DisplayLength</span><span class="sxs-lookup"><span data-stu-id="93299-261">DisplayLength</span></span></td>
<td><span data-ttu-id="93299-262">ページまたはレポートに表示されている文字の最大数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-262">Specify the maximum number of characters that are shown on a page or report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-263">EnumType</span><span class="sxs-lookup"><span data-stu-id="93299-263">EnumType</span></span></td>
<td><span data-ttu-id="93299-264">列挙されたデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-264">Specify an enumerated data type.</span></span> <span data-ttu-id="93299-265">このプロパティは、<strong>列挙</strong>型の EDT に対して設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-265">This property must be set for EDTs of the <strong>enum</strong> type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-266">拡張</span><span class="sxs-lookup"><span data-stu-id="93299-266">Extends</span></span></td>
<td><span data-ttu-id="93299-267">EDT を別の EDT に基づいて作成するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-267">Use this property to base the EDT on another EDT.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-268">FormHelp</span><span class="sxs-lookup"><span data-stu-id="93299-268">FormHelp</span></span></td>
<td><span data-ttu-id="93299-269">ページ上のフィールドから参照を実行するときに使用するページを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-269">Specify the page to use when you perform a lookup from a field on a page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-270">HelpText</span><span class="sxs-lookup"><span data-stu-id="93299-270">HelpText</span></span></td>
<td><span data-ttu-id="93299-271">EDT のヘルプ文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-271">Create a Help string for the EDT.</span></span> <span data-ttu-id="93299-272">型がページで使用されている場合は、ヘルプ文字列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-272">The Help string is shown when the type is used on a page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-273">ID</span><span class="sxs-lookup"><span data-stu-id="93299-273">ID</span></span></td>
<td><span data-ttu-id="93299-274">このプロパティは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-274">This property is read-only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-275">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-275">Label</span></span></td>
<td><span data-ttu-id="93299-276">ページやレポートでタイプが使用される場合にタイプに使用されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-276">Specify the label that is used for the type when the type is used on a page or report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-277">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-277">Model</span></span></td>
<td><span data-ttu-id="93299-278">テーブルがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-278">Specify the model that the table is in.</span></span> <span data-ttu-id="93299-279">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-279">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-280">要素例には、テーブルおよびクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-280">Examples of elements include a table and a class.</span></span> <span data-ttu-id="93299-281">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-281">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-282">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-282">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-283">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-283">Name</span></span></td>
<td><span data-ttu-id="93299-284">タイプの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-284">Specify the name of the type.</span></span> <span data-ttu-id="93299-285">この名前は、X++ の型を参照するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-285">The name is used to refer to the type from X++.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-286">PresenceClass</span><span class="sxs-lookup"><span data-stu-id="93299-286">PresenceClass</span></span></td>
<td><span data-ttu-id="93299-287"><strong>PresenceInfo</strong> オブジェクトのインスタンスを返すために、<strong>PresenceMethod</strong> プロパティと同時に使用する X++ クラスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-287">Specify the X++ class that is used together with the <strong>PresenceMethod</strong> property to return an instance of the <strong>PresenceInfo</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-288">PresenceIndicatorAllowed</span><span class="sxs-lookup"><span data-stu-id="93299-288">PresenceIndicatorAllowed</span></span></td>
<td><span data-ttu-id="93299-289">EDT を参照するコントロールでプレゼンスを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-289">Specify whether the control that references the EDT should use presence.</span></span> <span data-ttu-id="93299-290">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-290">The default value is <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-291">PresenceMethod</span><span class="sxs-lookup"><span data-stu-id="93299-291">PresenceMethod</span></span></td>
<td><span data-ttu-id="93299-292"><strong>PresenceClass</strong> プロパティで指定されている X++ クラスについては、コントロール データ値を使用して呼び出される必要がある X++ 静的クラス メソッドな方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-292">For the X++ class that is specified in the <strong>PresenceClass</strong> property, specify the X++ static class method that should be called by using a controls data value.</span></span> <span data-ttu-id="93299-293">このメソッドは、プレゼンス インジケータが必要とするデータを含む <strong>PresenceInfo</strong> オブジェクトのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="93299-293">This method returns an instance of the <strong>PresenceInfo</strong> object that contains the data that the Presence indicator requires.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-294">ReferenceTable</span><span class="sxs-lookup"><span data-stu-id="93299-294">ReferenceTable</span></span></td>
<td><span data-ttu-id="93299-295">この EDT で参照されているテーブルと、それが主キーであることを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-295">Specify the table that is referenced by this EDT, and that has the primary key.</span></span> <span data-ttu-id="93299-296">つまり、このプロパティは、この EDT が参照する主キー テーブルを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-296">In other words, this property indicates the primary key table that this EDT references.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-297">スタイル</span><span class="sxs-lookup"><span data-stu-id="93299-297">Style</span></span></td>
<td><span data-ttu-id="93299-298">EDT の既定の外観を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-298">Change the default appearance of the EDT.</span></span> <span data-ttu-id="93299-299"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-299">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-300">自動</span><span class="sxs-lookup"><span data-stu-id="93299-300">Auto</span></span></li>
<li><span data-ttu-id="93299-301">コンボ ボックス</span><span class="sxs-lookup"><span data-stu-id="93299-301">Combo box</span></span></li>
<li><span data-ttu-id="93299-302">オプション ボタン</span><span class="sxs-lookup"><span data-stu-id="93299-302">Radio button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="properties-that-are-available-for-only-some-base-data-types"></a><span data-ttu-id="93299-303">一部の基本データ型のみに使用できるプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-303">Properties that are available for only some base data types</span></span>

<span data-ttu-id="93299-304">次の表に別途記載がない限り、これらのプロパティはすべて **自動** に設定してください。</span><span class="sxs-lookup"><span data-stu-id="93299-304">Unless the following table specifies otherwise, you should leave all these properties set to **Auto**.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-305">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-305">Property</span></span></th>
<th><span data-ttu-id="93299-306">プロパティが存在する型を入力</span><span class="sxs-lookup"><span data-stu-id="93299-306">Type that the property exists for</span></span></th>
<th><span data-ttu-id="93299-307">説明</span><span class="sxs-lookup"><span data-stu-id="93299-307">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-308">調整</span><span class="sxs-lookup"><span data-stu-id="93299-308">Adjustment</span></span></td>
<td><span data-ttu-id="93299-309">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-309">String</span></span></td>
<td><span data-ttu-id="93299-310">固定長の文字列については、入力される文字がパディング スペースの左側または右側に格納されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-310">For strings of fixed length, specify whether the characters that are entered should be stored on the left side or the right side of the padding spaces.</span></span> <span data-ttu-id="93299-311"><strong>左</strong> または <strong>右</strong> を選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-311">The available options are <strong>Left</strong> and <strong>Right</strong>.</span></span> <span data-ttu-id="93299-312">既定値は <strong>左</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-312">The default value is <strong>Left</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-313">AllowNegative</span><span class="sxs-lookup"><span data-stu-id="93299-313">AllowNegative</span></span></td>
<td><span data-ttu-id="93299-314">IntegerInt64Real</span><span class="sxs-lookup"><span data-stu-id="93299-314">IntegerInt64Real</span></span></td>
<td><span data-ttu-id="93299-315">フィールドが負の値を受け入れることができるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-315">Specify whether the field can accept negative values.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-316">AutoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-316">AutoInsSeparator</span></span></td>
<td><span data-ttu-id="93299-317">実数</span><span class="sxs-lookup"><span data-stu-id="93299-317">Real</span></span></td>
<td><span data-ttu-id="93299-318">システムが小数桁の区切り記号を自動的に挿入する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-318">Specify whether the system should automatically insert a decimal separator.</span></span> <span data-ttu-id="93299-319">たとえば、<strong>2222</strong> を入力する場合、システムは自動で <strong>2222.00</strong> を表示します。</span><span class="sxs-lookup"><span data-stu-id="93299-319">For example, if you enter <strong>2222</strong>, the system automatically shows <strong>2222.00</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-320">ChangeCase</span><span class="sxs-lookup"><span data-stu-id="93299-320">ChangeCase</span></span></td>
<td><span data-ttu-id="93299-321">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-321">String</span></span></td>
<td><span data-ttu-id="93299-322">文字列コントロールに入力されたテキストを書式設定する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-322">Specify how text that is entered in a string control should be formatted.</span></span> <span data-ttu-id="93299-323">たとえば、テキストは全大文字として書式設定され、またはタイトルの大文字化を使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-323">For example, the text can be formatted as all uppercase letters, or it can use title capitalization.</span></span> <span data-ttu-id="93299-324"><strong>注記:</strong> このプロパティは、エンタープライズ ポータルではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="93299-324"><strong>Note:</strong> This property isn&#39;t supported for Enterprise Portal.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-325">DateDay</span><span class="sxs-lookup"><span data-stu-id="93299-325">DateDay</span></span></td>
<td><span data-ttu-id="93299-326">DateUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-326">DateUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-327">日の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-327">Specify how the day should be shown.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-328">DateFormat</span><span class="sxs-lookup"><span data-stu-id="93299-328">DateFormat</span></span></td>
<td><span data-ttu-id="93299-329">DateUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-329">DateUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-330">日付のレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-330">Specify the layout of a date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-331">DateMonth</span><span class="sxs-lookup"><span data-stu-id="93299-331">DateMonth</span></span></td>
<td><span data-ttu-id="93299-332">DateUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-332">DateUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-333">月の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-333">Specify how the month should be shown.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-334">DateSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-334">DateSeparator</span></span></td>
<td><span data-ttu-id="93299-335">DateUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-335">DateUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-336">年、月、日の間の区切り記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-336">Specify the separators between year, month, and day.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-337">DateYear</span><span class="sxs-lookup"><span data-stu-id="93299-337">DateYear</span></span></td>
<td><span data-ttu-id="93299-338">DateUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-338">DateUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-339">年の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-339">Specify how the year should be shown.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-340">DecimalSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-340">DecimalSeparator</span></span></td>
<td><span data-ttu-id="93299-341">実数</span><span class="sxs-lookup"><span data-stu-id="93299-341">Real</span></span></td>
<td><span data-ttu-id="93299-342">小数桁の区切り文字を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-342">Specify the decimal separator.</span></span> <span data-ttu-id="93299-343">既定の設定 (<strong>自動</strong>) が使用されると、システムの設定で指定されている少数桁の区切り文字が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-343">When the default setting (<strong>Auto</strong>) is used, the decimal separator that is specified in the system setup is used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-344">DisplaceNegative</span><span class="sxs-lookup"><span data-stu-id="93299-344">DisplaceNegative</span></span></td>
<td><span data-ttu-id="93299-345">IntegerInt64Real</span><span class="sxs-lookup"><span data-stu-id="93299-345">IntegerInt64Real</span></span></td>
<td><span data-ttu-id="93299-346">負の数を左に揃えるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-346">Specify whether to align negative numbers to the left.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-347">DisplayHeight</span><span class="sxs-lookup"><span data-stu-id="93299-347">DisplayHeight</span></span></td>
<td><span data-ttu-id="93299-348">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-348">String</span></span></td>
<td><span data-ttu-id="93299-349">EDT がページに表示されているときに同時に表示する行数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-349">Specify the number of lines to show at the same time when the EDT is shown on a page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-350">EnumType</span><span class="sxs-lookup"><span data-stu-id="93299-350">EnumType</span></span></td>
<td><span data-ttu-id="93299-351">列挙</span><span class="sxs-lookup"><span data-stu-id="93299-351">Enum</span></span></td>
<td><span data-ttu-id="93299-352">EDT を作成するために使用される基本列挙を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-352">Specify the base enum that is used to create the EDT.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-353">FormatMST</span><span class="sxs-lookup"><span data-stu-id="93299-353">FormatMST</span></span></td>
<td><span data-ttu-id="93299-354">実数</span><span class="sxs-lookup"><span data-stu-id="93299-354">Real</span></span></td>
<td><span data-ttu-id="93299-355">値を書式設定する必要があるマスター通貨を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-355">Specify master currency values should be formatted.</span></span> <span data-ttu-id="93299-356"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-356">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-357">自動</span><span class="sxs-lookup"><span data-stu-id="93299-357">Auto</span></span></li>
<li><span data-ttu-id="93299-358">有</span><span class="sxs-lookup"><span data-stu-id="93299-358">Yes</span></span></li>
<li><span data-ttu-id="93299-359">無</span><span class="sxs-lookup"><span data-stu-id="93299-359">No</span></span></li>
</ul>
<span data-ttu-id="93299-360">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-360">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-361">NoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="93299-361">NoOfDecimals</span></span></td>
<td><span data-ttu-id="93299-362">実数</span><span class="sxs-lookup"><span data-stu-id="93299-362">Real</span></span></td>
<td><span data-ttu-id="93299-363">値がページまたはレポートに表示されているときの小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-363">Specify the number of decimal places when a value is shown on a page or a report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-364">RotateSign</span><span class="sxs-lookup"><span data-stu-id="93299-364">RotateSign</span></span></td>
<td><span data-ttu-id="93299-365">IntegerInt64Real</span><span class="sxs-lookup"><span data-stu-id="93299-365">IntegerInt64Real</span></span></td>
<td><span data-ttu-id="93299-366">数値の符号を逆にする場合にこのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-366">Select this option to reverse the sign for the number.</span></span> <span data-ttu-id="93299-367">つまり、マイナス記号 (-) をプラス記号 (+) に、またはプラス記号をマイナス記号に変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-367">In other words, change a minus sign (–) to a plus sign (+) or a plus sign to a minus sign.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-368">ShowZero</span><span class="sxs-lookup"><span data-stu-id="93299-368">ShowZero</span></span></td>
<td><span data-ttu-id="93299-369">IntegerInt64Real</span><span class="sxs-lookup"><span data-stu-id="93299-369">IntegerInt64Real</span></span></td>
<td><span data-ttu-id="93299-370">値 0 (ゼロ) を持つのフィールドを空のフィールドとして表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-370">Specify whether to show a field that has a value of 0 (zero) as an empty field.</span></span> <span data-ttu-id="93299-371">このタイプのフィールドにある 0 の値が null であるまたは意味をなさない場合は、このプロパティを<strong>いいえ</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-371">If a value of 0 in fields of this type means null/nothing, set this property to <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-372">SignDisplay</span><span class="sxs-lookup"><span data-stu-id="93299-372">SignDisplay</span></span></td>
<td><span data-ttu-id="93299-373">IntegerInt64Real</span><span class="sxs-lookup"><span data-stu-id="93299-373">IntegerInt64Real</span></span></td>
<td><span data-ttu-id="93299-374">負の値の符号を表示するかどうかと、数値の前後に符号を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-374">Specify whether to show the sign of a negative number, and also whether the sign should appear before or after the number.</span></span> <span data-ttu-id="93299-375">通常、このプロパティは <strong>Auto</strong> に設定する必要があります。 ただし、<strong>DisplaceNegative</strong> プロパティを使用している場合は  <strong>None</strong> に設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-375">Typically, you should set this property to <strong>Auto</strong>. However, you can set it to <strong>None</strong> if the <strong>DisplaceNegative</strong> property is used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-376">StringSize</span><span class="sxs-lookup"><span data-stu-id="93299-376">StringSize</span></span></td>
<td><span data-ttu-id="93299-377">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-377">String</span></span></td>
<td><span data-ttu-id="93299-378">文字列の最大サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-378">Specify the maximum size of the string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-379">ThousandSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-379">ThousandSeparator</span></span></td>
<td><span data-ttu-id="93299-380">実数</span><span class="sxs-lookup"><span data-stu-id="93299-380">Real</span></span></td>
<td><span data-ttu-id="93299-381">1000 ごとに区切るために使用する記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-381">Specify the symbol that is used to separate thousands.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-382">TimeFormat</span><span class="sxs-lookup"><span data-stu-id="93299-382">TimeFormat</span></span></td>
<td><span data-ttu-id="93299-383">TimeUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-383">TimeUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-384">時間を書式設定する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-384">Specify how times should be formatted.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-385">TimeHours</span><span class="sxs-lookup"><span data-stu-id="93299-385">TimeHours</span></span></td>
<td><span data-ttu-id="93299-386">TimeUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-386">TimeUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-387">時間を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-387">Specify whether to include hours.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-388">TimeMinute</span><span class="sxs-lookup"><span data-stu-id="93299-388">TimeMinute</span></span></td>
<td><span data-ttu-id="93299-389">TimeUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-389">TimeUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-390">分を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-390">Specify whether to include minutes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-391">TimeSeconds</span><span class="sxs-lookup"><span data-stu-id="93299-391">TimeSeconds</span></span></td>
<td><span data-ttu-id="93299-392">TimeUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-392">TimeUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-393">秒を含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-393">Specify whether to include seconds.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-394">TimeSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-394">TimeSeparator</span></span></td>
<td><span data-ttu-id="93299-395">TimeUtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-395">TimeUtcDateTime</span></span></td>
<td><span data-ttu-id="93299-396">時間に使用される区切り記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-396">Specify the separator that is used for times.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-397">TimezonePreference</span><span class="sxs-lookup"><span data-stu-id="93299-397">TimezonePreference</span></span></td>
<td><span data-ttu-id="93299-398">UtcDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-398">UtcDateTime</span></span></td>
<td><span data-ttu-id="93299-399">協定世界時 (UTC) から値を変換するタイム ゾーンを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-399">Specify the time zone to convert the value to from Coordinated Universal Time (UTC).</span></span></td>
</tr>
</tbody>
</table>

## <a name="perspective-properties"></a><span data-ttu-id="93299-400">分析視点のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-400">Perspective properties</span></span>
<span data-ttu-id="93299-401">アプリケーション エクスプローラーの**データ ディクショナリ** ノードには、**分析視点**ノードがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-401">In Application Explorer, under the **Data Dictionary** node, there is a **Perspectives** node.</span></span> <span data-ttu-id="93299-402">分析視点は、キューブのメジャーと分析コードを含むテーブルとビューの集合です。</span><span class="sxs-lookup"><span data-stu-id="93299-402">A perspective is a collection of tables and views that contain the measures and dimensions for a cube.</span></span> <span data-ttu-id="93299-403">次のテーブルに、各分析視点に設定できるプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-403">The following table describes the properties that can be set for each perspective.</span></span> <span data-ttu-id="93299-404">分析視点で使用可能なシステム プロパティの詳細については、「システムと共通プロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-404">For information about the system properties that are available for a perspective, see the "System and common properties" section.</span></span> <span data-ttu-id="93299-405">分析視点に関連付けられているテーブルのプロパティの詳細については、「テーブルのプロパティ」および「テーブル フィールドのプロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-405">For information about the properties for tables that are associated with a perspective, see the "Table properties" and "Table field properties" sections.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-406">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-406">Property</span></span></th>
<th><span data-ttu-id="93299-407">説明</span><span class="sxs-lookup"><span data-stu-id="93299-407">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-408">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-408">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-409">分析視点に割り当てられるコンフィギュレーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-409">Specify the configuration key that is assigned to the perspective.</span></span> <span data-ttu-id="93299-410">コンフィギュレーション キーは、生成されたレポート モデルに含まれる分析視点の構成を決定します。</span><span class="sxs-lookup"><span data-stu-id="93299-410">The configuration key determines which configurations of a perspective are included for in report models that are generated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-411">HelpText</span><span class="sxs-lookup"><span data-stu-id="93299-411">HelpText</span></span></td>
<td><span data-ttu-id="93299-412">レポート モデルの分析視点の説明として使用する文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-412">Create a string to use as a description for the perspective in a report model.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-413">ID</span><span class="sxs-lookup"><span data-stu-id="93299-413">ID</span></span></td>
<td><span data-ttu-id="93299-414">分析視点の識別子を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-414">Specify the identifier of the perspective.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-415">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-415">Label</span></span></td>
<td><span data-ttu-id="93299-416">レポート モデルの分析視点に表示される名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-416">Specify the name that is shown for the perspective in a report model.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-417">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-417">Model</span></span></td>
<td><span data-ttu-id="93299-418">分析視点があるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-418">Specify the model that the perspective is in.</span></span> <span data-ttu-id="93299-419">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-419">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-420">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-420">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-421">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-421">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-422">SharedDimensionContainer</span><span class="sxs-lookup"><span data-stu-id="93299-422">SharedDimensionContainer</span></span></td>
<td><span data-ttu-id="93299-423">分析視点で項目を共有するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-423">Specify whether to share items in the perspective.</span></span> <span data-ttu-id="93299-424">このプロパティを <strong>はい</strong> に設定すると、分析視点内の品目はプロジェクト内のその他のすべての分析視点に追加され、分析視点のキューブは作成されません。</span><span class="sxs-lookup"><span data-stu-id="93299-424">When this property is set to <strong>Yes</strong>, the items in the perspective are added to all other perspectives that are in the project, and no cube is created for the perspective.</span></span> <span data-ttu-id="93299-425">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-425">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-426">用途</span><span class="sxs-lookup"><span data-stu-id="93299-426">Usage</span></span></td>
<td><span data-ttu-id="93299-427">分析視点の具体化オプションを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-427">Specify the materialization options for a perspective.</span></span> <span data-ttu-id="93299-428"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-428">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-429"><strong>AdHocReporting </strong>- 分析視点は、トランザクションの Semantic Model Definition Language (SMDL) モデルを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-429"><strong>AdHocReporting </strong>– The perspective will be used to generate a transactional Semantic Model Definition Language (SMDL) model.</span></span></li>
<li><span data-ttu-id="93299-430"><strong>OLAP</strong> - 分析視点は、Microsoft SQL Server Analysis Services (SSAS) ビジネス インテリジェンス プロジェクトでキューブを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-430"><strong>OLAP </strong>– The perspective will be used to generate a cube in a Microsoft SQL Server Analysis Services (SSAS) Business Intelligence project.</span></span></li>
<li><span data-ttu-id="93299-431"><strong>両方 </strong>- 分析視点は、SSAS Business Intelligence プロジェクトでトランザクション SDML モデルと、キューブの両方を生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-431"><strong>Both </strong>– The perspective will be used to generate both a transactional SDML model and a cube in an SSAS Business Intelligence project.</span></span></li>
<li><span data-ttu-id="93299-432"><strong>なし </strong>- 分析視点は実現されません。</span><span class="sxs-lookup"><span data-stu-id="93299-432"><strong>None </strong>– The perspective won&#39;t be materialized.</span></span></li>
</ul>
<span data-ttu-id="93299-433">既定値は <strong>なし</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-433">The default value is <strong>None</strong>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="table-properties"></a><span data-ttu-id="93299-434">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-434">Table properties</span></span>
<span data-ttu-id="93299-435">このセクションでは、アプリケーション エクスプローラーのテーブル要素の**プロパティ**ウィンドウに表示されるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-435">This section describes the properties that appear in the **Properties** window for table elements in Application Explorer.</span></span> <span data-ttu-id="93299-436">テーブル要素は、**データ ディクショナリ** &gt; **テーブル** にあります。</span><span class="sxs-lookup"><span data-stu-id="93299-436">Table elements are located under **Data Dictionary** &gt; **Tables**.</span></span>

### <a name="table-properties"></a><span data-ttu-id="93299-437">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-437">Table properties</span></span>

<span data-ttu-id="93299-438">次のテーブルは、アプリケーション エクスプローラーでのテーブル要素のプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-438">The following table describes the properties of table elements in Application Explorer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-439">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-439">Property</span></span></th>
<th><span data-ttu-id="93299-440">説明</span><span class="sxs-lookup"><span data-stu-id="93299-440">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-441">抽象</span><span class="sxs-lookup"><span data-stu-id="93299-441">Abstract</span></span></td>
<td><span data-ttu-id="93299-442">テーブルが継承をサポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-442">Specify whether the table supports inheritance.</span></span> <span data-ttu-id="93299-443">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-443">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="93299-444">値が<strong>はい</strong>に設定されている場合、テーブルが、<strong>update_recordset</strong>および<strong>select</strong> ステートメントのような X++ SQL ステートメントの直接ターゲットにはなりません。</span><span class="sxs-lookup"><span data-stu-id="93299-444">If the value is set to <strong>Yes</strong>, the table can&#39;t be a direct target of X++ SQL statements such as <strong>update_recordset</strong> and <strong>select</strong>.</span></span> <span data-ttu-id="93299-445"><strong>注記:</strong> <strong>SupportInheritance</strong> プロパティが<strong>いいえ</strong>に設定されている場合、このプロパティは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-445"><strong>Note:</strong> This property is unavailable when the <strong>SupportInheritance</strong> property is set to <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-446">AnalysisDimensionType</span><span class="sxs-lookup"><span data-stu-id="93299-446">AnalysisDimensionType</span></span></td>
<td><span data-ttu-id="93299-447"><strong>IsLookup</strong> プロパティの設定に基づいて作成される分析コードのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-447">Specify the type of dimension that is created, based on the setting of the <strong>IsLookup</strong> property.</span></span> <span data-ttu-id="93299-448"><strong>IsLookup</strong> プロパティが<strong>はい</strong>に設定されている場合、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-448">If the <strong>IsLookup</strong> property is set to <strong>Yes</strong>, the following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-449"><strong>自動 </strong>- テーブルは事実データと分析コード データの両方を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-449"><strong>Auto </strong>– The table can contain both factual and dimensional data.</span></span> <span data-ttu-id="93299-450">BI ウィザードは、分析コード データを抽出し、分析コードと属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-450">The BI Wizard will extract dimensional data, and create dimensions and attributes.</span></span> <span data-ttu-id="93299-451">事実データが抽出され、対策が作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-451">Factual data will be extracted to create measures.</span></span> <span data-ttu-id="93299-452">親テーブルから属性を持つ 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-452">One child dimension is created that has attributes from the parent table.</span></span></li>
<li><span data-ttu-id="93299-453"><strong>MasterInner</strong> - 内部 (完全) 結合を使用して、このテーブルと子テーブルの関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-453"><strong>MasterInner </strong>– An inner (full) join is used to create relationships with this table to the child table.</span></span> <span data-ttu-id="93299-454">表およびテーブルの各レコードの組み合わせは、分析コードで生成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-454">Each record combination for this table and the child table are generated in the dimension.</span></span> <span data-ttu-id="93299-455">親テーブルから属性を持つ 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-455">One child dimension is created that has attributes from the parent table.</span></span></li>
<li><span data-ttu-id="93299-456"><strong>MasterLeftOuter</strong> - 左外部結合を使用して、このテーブルと子テーブルの関係を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-456"><strong>MasterLeftOuter </strong>– A left outer join is used to create relationships with this table to the child table.</span></span> <span data-ttu-id="93299-457">分析コードには、このテーブルの値に基づいて、空の場合もある追加の属性が設定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-457">Dimensions will have additional attributes, based on values in this table that can also be empty.</span></span> <span data-ttu-id="93299-458">親テーブルから属性を持つ 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-458">One child dimension is created that has attributes from the parent table.</span></span></li>
<li><span data-ttu-id="93299-459"><strong>トランザクション </strong>- テーブルは事実データ (測定) のみを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-459"><strong>Transaction </strong>– The table should be used to generate only factual data (measures).</span></span> <span data-ttu-id="93299-460">テーブルにトランザクション データのみが含まれている場合に、このオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-460">You should use this option when a table contains only transactional data.</span></span> <span data-ttu-id="93299-461">テーブルから列挙型フィールドのみを含む 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-461">One child dimension is created that contains only enumeration fields from the table.</span></span></li>
</ul>
<span data-ttu-id="93299-462"><strong>IsLookup</strong> プロパティが<strong>いいえ</strong>に設定されている場合、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-462">If the <strong>IsLookup</strong> property is set to <strong>No</strong>, the following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-463"><strong>自動 </strong>- テーブルは事実データと分析コード データの両方を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-463"><strong>Auto </strong>– Table can contain both factual and dimensional data.</span></span> <span data-ttu-id="93299-464">BI ウィザードは、分析コード データを抽出して分析コードと属性を作成します。事実に基づくデータはメジャーを作成するために抽出されます。</span><span class="sxs-lookup"><span data-stu-id="93299-464">The BI Wizard will extract dimensional data, and create dimensions and attributes, Factual data will be extracted to create measures.</span></span> <span data-ttu-id="93299-465">1 つの親と子の分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-465">One parent and child dimension are created.</span></span></li>
<li><span data-ttu-id="93299-466"><strong>MasterInner</strong> - 適用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-466"><strong>MasterInner </strong>– Not applicable.</span></span> <span data-ttu-id="93299-467">このオプションは<strong>自動</strong>と同じです。</span><span class="sxs-lookup"><span data-stu-id="93299-467">This option is the same as <strong>Auto</strong>.</span></span></li>
<li><span data-ttu-id="93299-468"><strong>MasterLeftOuter</strong> - 適用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-468"><strong>MasterLeftOuter </strong>– Not applicable.</span></span> <span data-ttu-id="93299-469">このオプションは<strong>自動</strong>と同じです。</span><span class="sxs-lookup"><span data-stu-id="93299-469">This option is the same as <strong>Auto</strong>.</span></span></li>
<li><span data-ttu-id="93299-470"><strong>トランザクション </strong>- テーブルは事実データ (測定) のみを生成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-470"><strong>Transaction </strong>– The table should be used to generate only factual data (measures).</span></span> <span data-ttu-id="93299-471">テーブルにトランザクション データのみが含まれている場合に、このオプションを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-471">You should use this option when a table contains only transactional data.</span></span> <span data-ttu-id="93299-472">テーブルから列挙値のみを含む 1 つの子分析コードが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-472">One child dimension is created that contains only enumeration values from the table.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-473">AnalysisIdentifier</span><span class="sxs-lookup"><span data-stu-id="93299-473">AnalysisIdentifier</span></span></td>
<td><span data-ttu-id="93299-474">SSAS キューブ内の分析コードの識別子として使用するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-474">Specify the field to use as the identifier for the dimension in an SSAS cube.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-475">AOSAuthorization</span><span class="sxs-lookup"><span data-stu-id="93299-475">AOSAuthorization</span></span></td>
<td><span data-ttu-id="93299-476">ユーザーのアクセス許可に応じて、ユーザーがテーブルで実行できる操作の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-476">Specify the type of operation that a user can perform on a table, depending on the user&#39;s permissions.</span></span> <span data-ttu-id="93299-477">このプロパティを <strong>なし</strong> に設定すると、承認チェックは実行されません。</span><span class="sxs-lookup"><span data-stu-id="93299-477">When this property is set to <strong>None</strong>, no authorization check is performed.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-478">CacheLookup</span><span class="sxs-lookup"><span data-stu-id="93299-478">CacheLookup</span></span></td>
<td><span data-ttu-id="93299-479">ルックアップ操作中に取得されたレコードをキャッシュする方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-479">Specify how to cache the records that are retrieved during a lookup operation.</span></span> <span data-ttu-id="93299-480">このプロパティは、別のテーブルを継承しないテーブルにのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-480">This property exists only on tables that don&#39;t inherit from another table.</span></span> <span data-ttu-id="93299-481">継承ルート テーブルで、アプリケーション エクスプローラー<strong>プロパティ</strong> ウィンドウを使用して、このプロパティを <strong>EntireTable</strong> に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-481">On an inheritance root table, you can&#39; set this property to <strong>EntireTable</strong> by using the Application Explorer <strong>Properties</strong> window.</span></span> <span data-ttu-id="93299-482">継承ルート テーブルにこの値を割り当てるために、他の手法を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-482">You must not use other techniques to assign this value to inheritance root tables.</span></span> <span data-ttu-id="93299-483">たとえば、この値を割り当てる <strong>TreeNode</strong> クラスの <strong>AOTsetProperty</strong> メソッドを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-483">For example, don&#39;t use the <strong>AOTsetProperty</strong> method of the <strong>TreeNode</strong> class to assign this value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-484">ClusterIndex</span><span class="sxs-lookup"><span data-stu-id="93299-484">ClusterIndex</span></span></td>
<td><span data-ttu-id="93299-485">クラスター インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-485">Specify the cluster index.</span></span> <span data-ttu-id="93299-486">このプロパティは、SQL の最適化にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-486">This property is used only for SQL optimization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-487">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-487">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-488">テーブルのコンフィギュレーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-488">Specify the configuration key for the table.</span></span> <span data-ttu-id="93299-489">コンフィギュレーション キーにより、システム管理者はアプリケーションの特定の部分を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-489">Configuration keys let a system administrator enable and disable specific parts of an application.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-490">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-490">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-491">テーブルが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-491">Specify the codes for the countries/regions where the table is applicable or valid.</span></span> <span data-ttu-id="93299-492">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-492">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-493">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-493">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-494">クライアント フレームワークは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-494">The client framework uses this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-495">CountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="93299-495">CountryRegionContextField</span></span></td>
<td><span data-ttu-id="93299-496">国/地域のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-496">Specify the field that is used to identify the country/region context.</span></span> <span data-ttu-id="93299-497">このプロパティは、<strong>CountryRegionCodes</strong> プロパティに関連しています。</span><span class="sxs-lookup"><span data-stu-id="93299-497">This property is related to the <strong>CountryRegionCodes</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-498">CreatedBy</span><span class="sxs-lookup"><span data-stu-id="93299-498">CreatedBy</span></span></td>
<td><span data-ttu-id="93299-499">システムがテーブルのレコードの <strong>CreatedBy</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-499">Specify whether the system maintains the <strong>CreatedBy</strong> field for the records in a table.</span></span> <span data-ttu-id="93299-500">このフィールドには、レコードの作成者に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-500">This field contains information about the person who created a record.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-501">CreatedDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-501">CreatedDateTime</span></span></td>
<td><span data-ttu-id="93299-502">システムがテーブルのレコードの <strong>CreationDate</strong> および <strong>CreationTime</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-502">Specify whether the system maintains the <strong>CreationDate</strong> and <strong>CreationTime</strong> fields for the records in a table.</span></span> <span data-ttu-id="93299-503">このフィールドには、レコードが最後に作成された日付が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-503">This field contains the date when a record was created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-504">CreatedTransactionId</span><span class="sxs-lookup"><span data-stu-id="93299-504">CreatedTransactionId</span></span></td>
<td><span data-ttu-id="93299-505">システムがテーブルのレコードの <strong>CreatedTransactionId</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-505">Specify whether the system maintains the <strong>CreatedTransactionId</strong> field for the records in a table.</span></span> <span data-ttu-id="93299-506">このフィールドにはレコードを作成した取引に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-506">This field contains information about the transaction that created a record.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-507">CreateRecIdIndex</span><span class="sxs-lookup"><span data-stu-id="93299-507">CreateRecIdIndex</span></span></td>
<td><span data-ttu-id="93299-508"><strong>レコード ID</strong> フィールドのインデックスが作成されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-508">Specify whether an index on the <strong>Record ID</strong> field is created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-509">DeveloperDocumentation</span><span class="sxs-lookup"><span data-stu-id="93299-509">DeveloperDocumentation</span></span></td>
<td><span data-ttu-id="93299-510">テーブルの目的を説明し、プログラムでどのように使用されているかを説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-510">Describe the purpose of a table, and explain how it&#39;s used in the program.</span></span> <span data-ttu-id="93299-511">通常、説明は 5 つ以下の構文で構成され、単一の段落として書かれます。</span><span class="sxs-lookup"><span data-stu-id="93299-511">Typically, a description contains no more than five sentences and is written as a single paragraph.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-512">EntityRelationshipType</span><span class="sxs-lookup"><span data-stu-id="93299-512">EntityRelationshipType</span></span></td>
<td><span data-ttu-id="93299-513">共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってテーブルを分類します。</span><span class="sxs-lookup"><span data-stu-id="93299-513">Classify a table according to common entity relationship (ER) data model notation.</span></span> <span data-ttu-id="93299-514">テーブルは、エンティティまたはリレーションシップとして分類されます。</span><span class="sxs-lookup"><span data-stu-id="93299-514">A table is classified as either an entity or a relationship.</span></span> <span data-ttu-id="93299-515">エンティティはオブジェクトを表すのに対し、関係は 2 つのオブジェクト間の関連を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-515">An entity represents an object, whereas a relationship represents an association between two objects.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-516">拡張</span><span class="sxs-lookup"><span data-stu-id="93299-516">Extends</span></span></td>
<td><span data-ttu-id="93299-517">特定のテーブルからの派生テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-517">Derive the table from the specified table.</span></span> <span data-ttu-id="93299-518"><strong>SupportInheritance</strong> プロパティが <strong>Yes</strong> に設定されている場合、値は <strong>null</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-518">The value of this property is <strong>null</strong> when the <strong>SupportInheritance</strong> property is set to <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-519">FormRef</span><span class="sxs-lookup"><span data-stu-id="93299-519">FormRef</span></span></td>
<td><span data-ttu-id="93299-520">テーブルが参照されているときに発生する表示メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-520">Specify the display menu item that is activated when a table is referenced.</span></span> <span data-ttu-id="93299-521">表示メニュー項目は、ページに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="93299-521">A display menu item is associated with a page.</span></span> <span data-ttu-id="93299-522">レポートのプライマリ インデックス フィールドを使用するとき、このページはレポート内のリンクとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-522">When you use a primary index field on a report, this page is available as a link in the report.</span></span> <span data-ttu-id="93299-523"><strong>PrimaryIndex</strong> プロパティ使用して、プライマリ インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-523">You specify a primary index by using the <strong>PrimaryIndex</strong> property.</span></span> <span data-ttu-id="93299-524">このプロパティを空白のままにすると、システムではでテーブルと同じ名前のページを表示しようとします。</span><span class="sxs-lookup"><span data-stu-id="93299-524">If you leave this property blank, the system tries to display a page that has the same name as the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-525">ID</span><span class="sxs-lookup"><span data-stu-id="93299-525">ID</span></span></td>
<td><span data-ttu-id="93299-526">システムが生成したテーブル ID。</span><span class="sxs-lookup"><span data-stu-id="93299-526">The system-generated table ID.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-527">IsLookup</span><span class="sxs-lookup"><span data-stu-id="93299-527">IsLookup</span></span></td>
<td><span data-ttu-id="93299-528">レポート モデルについては、テーブルの情報が、レポート モデルが生成されるときに参照する他のテーブルに組み込まれているかどうかを指定するため、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-528">For report models, use this property to specify whether the table information is incorporated into other tables that reference it when a report model is generated.</span></span> <span data-ttu-id="93299-529">オンライン分析処理 (OLAP) キューブについては、このプロパティを使用して、連結分析コードまたは異なる分析コードを生成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-529">For online analytical processing (OLAP) cubes, use this property to specify whether to generate a consolidated dimension or a distinct dimension.</span></span> <span data-ttu-id="93299-530"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-530">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-531"><strong>はい </strong>- テーブルの属性は親分析コード (スター スキーマ) に連結される必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-531"><strong>Yes </strong>– Attributes from the table should be consolidated into the parent dimension (star schema).</span></span></li>
<li><span data-ttu-id="93299-532"><strong>いいえ</strong> - テーブル (スノーフレーク スキーマ) に対して個別の分析コードを生成します。</span><span class="sxs-lookup"><span data-stu-id="93299-532"><strong>No </strong>– A separate dimension should be generated for the table (snowflake schema).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-533">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-533">Label</span></span></td>
<td><span data-ttu-id="93299-534">テーブルのラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-534">Specify the label for a table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-535">ListPageRef</span><span class="sxs-lookup"><span data-stu-id="93299-535">ListPageRef</span></span></td>
<td><span data-ttu-id="93299-536">このレコードの種類の一覧を表示できるページをポイントする表示メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-536">Specify a display menu item that points to a page that can show a list of this record type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-537">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-537">Model</span></span></td>
<td><span data-ttu-id="93299-538">テーブルがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-538">Specify the model that the table is in.</span></span> <span data-ttu-id="93299-539">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-539">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-540">要素例には、テーブルおよびクラスがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-540">Examples of elements include a table and a class.</span></span> <span data-ttu-id="93299-541">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-541">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-542">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-542">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-543">ModifiedBy</span><span class="sxs-lookup"><span data-stu-id="93299-543">ModifiedBy</span></span></td>
<td><span data-ttu-id="93299-544">システムがテーブルのレコードの <strong>ModifiedBy</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-544">Specify whether the system maintains the <strong>ModifiedBy</strong> field for the records in a table.</span></span> <span data-ttu-id="93299-545">このフィールドには、レコードを最後に変更した人に関する情報が含まれます。 </span><span class="sxs-lookup"><span data-stu-id="93299-545">This field contains information about the person who last modified a record.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-546">ModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="93299-546">ModifiedDateTime</span></span></td>
<td><span data-ttu-id="93299-547">システムがテーブルのレコードの <strong>ModifiedDate</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-547">Specify whether the system maintains the <strong>ModifiedDate</strong> field for the records in a table.</span></span> <span data-ttu-id="93299-548">このフィールドには、レコードが最後に変更された日付が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-548">This field contains the date when a record was last modified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-549">ModifiedTime</span><span class="sxs-lookup"><span data-stu-id="93299-549">ModifiedTime</span></span></td>
<td><span data-ttu-id="93299-550">システムがテーブルのレコードの <strong>ModifiedDateTime</strong> フィールドを管理しているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-550">Specify whether the system maintains the <strong>ModifiedDateTime</strong> field for the records in a table.</span></span> <span data-ttu-id="93299-551">このフィールドには、レコードが最後に変更された日時が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-551">This field contains the date and time when a record was last modified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-552">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-552">Name</span></span></td>
<td><span data-ttu-id="93299-553">テーブル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-553">Specify the table name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-554">OccEnabled</span><span class="sxs-lookup"><span data-stu-id="93299-554">OccEnabled</span></span></td>
<td><span data-ttu-id="93299-555">テーブルでオプティミスティック同時実行モードを有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-555">Specify whether the optimistic concurrency mode is enabled for a table.</span></span> <span data-ttu-id="93299-556">このモードを有効にすると、データがデータベースからフェッチされるときに、データは今後の変更からロックされません。</span><span class="sxs-lookup"><span data-stu-id="93299-556">When this mode is enabled, data isn&#39;t locked from future modification when it&#39;s fetched from the database.</span></span> <span data-ttu-id="93299-557">データは、実際の更新の実行時にのみロックされます。</span><span class="sxs-lookup"><span data-stu-id="93299-557">Data is locked only when the actual update is performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-558">PreviewPartRef</span><span class="sxs-lookup"><span data-stu-id="93299-558">PreviewPartRef</span></span></td>
<td><span data-ttu-id="93299-559">拡張プレビューで使用される情報パーツまたはフォーム パーツを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-559">Specify the info part or form part to use in the enhanced preview.</span></span> <span data-ttu-id="93299-560">情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-560">An info part shows a collection of data fields from a specified query.</span></span> <span data-ttu-id="93299-561">メタデータを使用してデータの表示方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-561">It uses metadata to describe how the data appears.</span></span> <span data-ttu-id="93299-562">フォーム パーツは、ページへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="93299-562">A form part represents a pointer to a page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-563">PrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="93299-563">PrimaryIndex</span></span></td>
<td><span data-ttu-id="93299-564">プライマリ インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-564">Specify the primary index.</span></span> <span data-ttu-id="93299-565">固有のインデックスのみ選択することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-565">Only a unique index can be selected.</span></span> <span data-ttu-id="93299-566">このプロパティは、データベースの最適化と、キャッシュ キーとして使用するユニークなインデックスを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-566">This property is used for database optimization and to indicate which unique index should be used as the caching key.</span></span> <span data-ttu-id="93299-567">プライマリ インデックスを指定しない場合、最下位の ID の固有のインデックスはキャッシュ キーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-567">If you don&#39;t specify a primary index, the unique index that has the lowest ID is used as the caching key.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-568">ReplacementKey</span><span class="sxs-lookup"><span data-stu-id="93299-568">ReplacementKey</span></span></td>
<td><span data-ttu-id="93299-569">一部のページ コントロール内のデータの識別子として表示するフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-569">Specify the fields to display as the identifier for data in some page controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-570">ReportRef</span><span class="sxs-lookup"><span data-stu-id="93299-570">ReportRef</span></span></td>
<td><span data-ttu-id="93299-571">テーブルが参照されているときに発生する出力メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-571">Specify the output menu item that is activated when a table is referenced.</span></span> <span data-ttu-id="93299-572">出力メニュー項目はレポートに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="93299-572">An output menu item is associated with a report.</span></span> <span data-ttu-id="93299-573">レポートのプライマリ インデックス フィールドを使用するとき、このレポートはレポート内のリンクとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-573">When you use a primary index field on a report, this report is available as a link in the report.</span></span> <span data-ttu-id="93299-574"><strong>PrimaryIndex</strong> プロパティ使用して、プライマリ インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-574">You specify a primary index by using the <strong>PrimaryIndex</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-575">SaveDataPerCompany</span><span class="sxs-lookup"><span data-stu-id="93299-575">SaveDataPerCompany</span></span></td>
<td><span data-ttu-id="93299-576">現在の会社のデータが保存されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-576">Specify whether the data for the current company is saved.</span></span> <span data-ttu-id="93299-577">プロパティを<strong>いいえ</strong>に設定すると、データは会社識別子 (DataAreaId) なしで保存されます。</span><span class="sxs-lookup"><span data-stu-id="93299-577">If you set the property to <strong>No</strong>, data is saved without a company identifier (DataAreaId).</span></span> <span data-ttu-id="93299-578"><strong>注記: </strong>テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するページ デザインの <strong>SetCompany</strong> プロパティも<strong>はい</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-578"><strong>Note: </strong>If the <strong>SaveDataPerCompany</strong> property on a table is set to <strong>Yes</strong>, the <strong>SetCompany</strong> property on a page design that uses the table as a data source must also be set to <strong>Yes</strong>.</span></span> <span data-ttu-id="93299-579"><strong>ヒント:</strong> ステータス行は、会社の略称を表示します。</span><span class="sxs-lookup"><span data-stu-id="93299-579"><strong>Tip: </strong>The status line shows the acronym for the company.</span></span> <span data-ttu-id="93299-580">略称をダブルクリックして、会社を変更できるダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-580">Double-click the acronym to open a dialog box where you can change the company.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-581">SaveDataPerPartition</span><span class="sxs-lookup"><span data-stu-id="93299-581">SaveDataPerPartition</span></span></td>
<td><span data-ttu-id="93299-582">テーブルに<strong>パーティション</strong>という名前のシステム フィールドがあるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-582">A value that indicates whether the table has a system field that is named <strong>Partition</strong>.</span></span> <span data-ttu-id="93299-583">このプロパティは、読み取り専用になっています。</span><span class="sxs-lookup"><span data-stu-id="93299-583">This property is intended to be read-only.</span></span> <span data-ttu-id="93299-584">テーブルに<strong>パーティション</strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="93299-584">If the table has a <strong>Partition</strong> field, each record is assigned to one partition.</span></span> <span data-ttu-id="93299-585">各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されます。</span><span class="sxs-lookup"><span data-stu-id="93299-585">Each record is hidden from data access operations that are run under the context of other partitions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-586">SearchLinkRefName</span><span class="sxs-lookup"><span data-stu-id="93299-586">SearchLinkRefName</span></span></td>
<td><span data-ttu-id="93299-587">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-587">Specify the name of the menu item that links to information on a website about a table record that is listed in the Enterprise Portal search results.</span></span> <span data-ttu-id="93299-588"><strong>SearchLinkRefType</strong> プロパティが <strong>URL</strong> に設定されている場合、テーブル データが表示されている Web パーツ ページにリンクするメニュー項目を選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-588">If the <strong>SearchLinkRefType</strong> property is set to <strong>URL</strong>, select a menu item that links to a Web Part page that shows the table data.</span></span> <span data-ttu-id="93299-589">Web パーツ ページのフォームおよびレポートは、データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="93299-589">Forms and reports on Web Part pages can display data.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-590">SearchLinkRefType</span><span class="sxs-lookup"><span data-stu-id="93299-590">SearchLinkRefType</span></span></td>
<td><span data-ttu-id="93299-591">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-591">Specify the type of the menu item that links to information on a website about a table record that is listed in the Enterprise Portal search results.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-592">SingularLabel</span><span class="sxs-lookup"><span data-stu-id="93299-592">SingularLabel</span></span></td>
<td><span data-ttu-id="93299-593">テーブルに格納される品目の単数形の名前を表示するために、レポート モデルまたはキューブで使用されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-593">Specify the label that is used in a report model or a cube to show the singular name of items that are stored in the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-594">SupportInheritance</span><span class="sxs-lookup"><span data-stu-id="93299-594">SupportInheritance</span></span></td>
<td><span data-ttu-id="93299-595">このプロパティを<strong>はい</strong>に設定すると、<strong>Extends</strong> および <strong>Abstract</strong> などの、その他の継承関連のプロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-595">When you set this property to <strong>Yes</strong>, you can set a value for other inheritance-related properties, such as <strong>Extends</strong> and <strong>Abstract</strong>.</span></span> <span data-ttu-id="93299-596"><strong>注意:</strong> このプロパティを<strong>はい</strong>に設定した場合、テーブル上のフィールドはすべて削除され、再度作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-596"><strong>Caution:</strong> If you set this property to <strong>Yes</strong>, any fields on the table are dropped and must be created again.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-597">SystemTable</span><span class="sxs-lookup"><span data-stu-id="93299-597">SystemTable</span></span></td>
<td><span data-ttu-id="93299-598">テーブルをシステム テーブルとして表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-598">Indicate whether a table appears as a system table.</span></span> <span data-ttu-id="93299-599">システム テーブルとして表示されるテーブルは、エクスポートおよびインポート中にフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="93299-599">A table that appears as a system table can be filtered during export and import.</span></span> <span data-ttu-id="93299-600">システム テーブルは、サインイン時に常に同期されます。</span><span class="sxs-lookup"><span data-stu-id="93299-600">System tables are always synchronized when you sign in.</span></span> <span data-ttu-id="93299-601">したがって、このプロパティは、サインインするとすぐに使用するテーブルに便利です。</span><span class="sxs-lookup"><span data-stu-id="93299-601">Therefore, this property might be useful for tables that you use as soon as you sign in.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-602">TableContents</span><span class="sxs-lookup"><span data-stu-id="93299-602">TableContents</span></span></td>
<td><span data-ttu-id="93299-603">顧客間でセットアップ/パラメーター データを再利用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-603">Specify how setup/parameter data can be reused from one customer to another.</span></span> <span data-ttu-id="93299-604"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-604">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-605"><strong>指定なし</strong> - ほとんどのテーブルにこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-605"><strong>Not specified </strong>– Use this option for most tables.</span></span></li>
<li><span data-ttu-id="93299-606"><strong>既定のデータ</strong> - このオプションは、郵便番号、単位、時間間隔など、顧客に依存しないデータに使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-606"><strong>Default Data </strong>– Use this option for customer-independent data, such as postal codes, units, and time intervals.</span></span></li>
<li><span data-ttu-id="93299-607"><strong>基本データ </strong>- カレンダー、グループ、およびパラメータなどの顧客に依存するデータ用のこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-607"><strong>Base Data </strong>– Use this option for customer-dependent data, such as calendars, groups, and parameters.</span></span></li>
<li><span data-ttu-id="93299-608"><strong>既定 + 基本データ</strong> - このオプションは、ローカル知覚が異なるデータに対して使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-608"><strong>Default+Base data </strong>– Use this option for data where the local perception varies.</span></span> <span data-ttu-id="93299-609">たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、他のほとんどの場所では顧客に依存しています。</span><span class="sxs-lookup"><span data-stu-id="93299-609">For example, Chart of Accounts is customer-independent in Germany but is customer dependent in most other places.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-610">TableGroup</span><span class="sxs-lookup"><span data-stu-id="93299-610">TableGroup</span></span></td>
<td><span data-ttu-id="93299-611">テーブルが属するグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-611">Specify the group that the table belongs to.</span></span> <span data-ttu-id="93299-612">テーブル グループは、テーブルに含まれるデータのタイプに応じてテーブルを分類する方法を提供します。</span><span class="sxs-lookup"><span data-stu-id="93299-612">Table groups provide a method for categorizing tables according to the type of data that they contain.</span></span> <span data-ttu-id="93299-613">テーブルをデータ ソースとして使用することにより、ページ上のテーブルからデータを更新または削除するときにシステムがユーザーに確認を求めるかどうか定義するためにテーブル グループを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-613">You can use table groups to define whether the system should prompt users when they update or delete data from the table on pages by using the table as the data source.</span></span> <span data-ttu-id="93299-614">データをエクスポートするとき、テーブル グループを使用してレコードをフィルターすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-614">When you export data, you can use table groups to filter records.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-615">TableType</span><span class="sxs-lookup"><span data-stu-id="93299-615">TableType</span></span></td>
<td><span data-ttu-id="93299-616">このプロパティは、Microsoft Dynamics AX 2009 にある<strong>一時的な</strong>プロパティを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="93299-616">This property replaces the <strong>Temporary</strong> property that is found in Microsoft Dynamics AX 2009.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-617">TitleField1、TitleField2</span><span class="sxs-lookup"><span data-stu-id="93299-617">TitleField1, TitleField2</span></span></td>
<td><span data-ttu-id="93299-618">このプロパティは、次の方法で実現できます。</span><span class="sxs-lookup"><span data-stu-id="93299-618">You can use this property in the following ways:</span></span>
<ul>
<li><span data-ttu-id="93299-619">フォーム キャプションにテーブル フィールド データを追加します。</span><span class="sxs-lookup"><span data-stu-id="93299-619">Add table field data to a form caption.</span></span></li>
<li><span data-ttu-id="93299-620">参照ページで追加のフィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="93299-620">Show additional fields on a lookup page.</span></span> <span data-ttu-id="93299-621"><strong>TitleField1</strong> プロパティは、ページ上のフィールドでルックアップ リストを有効化するときにも使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-621">The <strong>TitleField1</strong> property is also used when you activate the lookup list in a field on a page.</span></span> <span data-ttu-id="93299-622"><strong>TitleField1</strong> および <strong>TitleField2</strong> プロパティに指定するフィールドは、キー値とマージできます。</span><span class="sxs-lookup"><span data-stu-id="93299-622">The fields that you specify for the <strong>TitleField1</strong> and <strong>TitleField2</strong> properties can be merged with the key value.</span></span></li>
<li><span data-ttu-id="93299-623">ツールヒントにフィールドの情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="93299-623">Show field information in a tooltip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-624">TypicalRowCount</span><span class="sxs-lookup"><span data-stu-id="93299-624">TypicalRowCount</span></span></td>
<td><span data-ttu-id="93299-625">テーブル内に通常表示されるレコード数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-625">Specify the number of records that typically appear in a table.</span></span> <span data-ttu-id="93299-626"><strong>AnalysisSelection</strong> プロパティが設定されていない場合、このプロパティにより SSRS のレポート ビルダーを使用してレコードを選択する方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-626">If the <strong>AnalysisSelection</strong> property isn&#39;t set, this property determines how records are selected by using Report Builder for SSRS.</span></span> <span data-ttu-id="93299-627">このプロパティの設定は、ドロップダウン リスト、リスト ボックス、フィルタリングされたリスト ボックスを使用してテーブル レコードを選択するかどうかに影響します。</span><span class="sxs-lookup"><span data-stu-id="93299-627">The setting of this property affects whether a drop-down list, a list box, or a filtered list box is used to select table records.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-628">ValidTimeStateFieldType</span><span class="sxs-lookup"><span data-stu-id="93299-628">ValidTimeStateFieldType</span></span></td>
<td><span data-ttu-id="93299-629">期間内のデータを追跡するときにシステムが使用する日付/時刻フィールドのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-629">Specify the type of date-time field that the system uses when it tracks data within time spans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-630">表示</span><span class="sxs-lookup"><span data-stu-id="93299-630">Visible</span></span></td>
<td><span data-ttu-id="93299-631">テーブルがページやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-631">Specify the access rights when the table is used as a data source on a page or a report.</span></span> <span data-ttu-id="93299-632">テーブルをページ内のデータ ソースとして使用する場合、ページのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-632">If the table is used as a data source on a page, the access rights on the page can&#39;t exceed the access rights that are defined for the table.</span></span></td>
</tr>
</tbody>
</table>

### <a name="tables-and-report-models"></a><span data-ttu-id="93299-633">テーブルおよびレポート モデル</span><span class="sxs-lookup"><span data-stu-id="93299-633">Tables and report models</span></span>

<span data-ttu-id="93299-634">次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。</span><span class="sxs-lookup"><span data-stu-id="93299-634">The following properties are related to report models that are used to add information to a report:</span></span>

-   <span data-ttu-id="93299-635">AnalysisSelection</span><span class="sxs-lookup"><span data-stu-id="93299-635">AnalysisSelection</span></span>
-   <span data-ttu-id="93299-636">AnalysisVisibility</span><span class="sxs-lookup"><span data-stu-id="93299-636">AnalysisVisibility</span></span>
-   <span data-ttu-id="93299-637">IsLookup</span><span class="sxs-lookup"><span data-stu-id="93299-637">IsLookup</span></span>
-   <span data-ttu-id="93299-638">SingularLabel</span><span class="sxs-lookup"><span data-stu-id="93299-638">SingularLabel</span></span>
-   <span data-ttu-id="93299-639">TypicalRowCount</span><span class="sxs-lookup"><span data-stu-id="93299-639">TypicalRowCount</span></span>

## <a name="table-field-properties"></a><span data-ttu-id="93299-640">テーブル フィールド プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-640">Table field properties</span></span>
<span data-ttu-id="93299-641">次のプロパティは、レポートに情報を追加するために使用されるレポート モデルに関連しています。</span><span class="sxs-lookup"><span data-stu-id="93299-641">The following properties are related to report models that are used to add information to a report:</span></span>

-   <span data-ttu-id="93299-642">AnalysisDefaultTotal</span><span class="sxs-lookup"><span data-stu-id="93299-642">AnalysisDefaultTotal</span></span>
-   <span data-ttu-id="93299-643">AnalysisLabel</span><span class="sxs-lookup"><span data-stu-id="93299-643">AnalysisLabel</span></span>
-   <span data-ttu-id="93299-644">AnalysisTotaling</span><span class="sxs-lookup"><span data-stu-id="93299-644">AnalysisTotaling</span></span>
-   <span data-ttu-id="93299-645">AnalysisUsage</span><span class="sxs-lookup"><span data-stu-id="93299-645">AnalysisUsage</span></span>
-   <span data-ttu-id="93299-646">AnalysisVisibility</span><span class="sxs-lookup"><span data-stu-id="93299-646">AnalysisVisibility</span></span>
-   <span data-ttu-id="93299-647">CurrencyCode</span><span class="sxs-lookup"><span data-stu-id="93299-647">CurrencyCode</span></span>
-   <span data-ttu-id="93299-648">CurrencyCodeField</span><span class="sxs-lookup"><span data-stu-id="93299-648">CurrencyCodeField</span></span>
-   <span data-ttu-id="93299-649">CurrencyCodeTable</span><span class="sxs-lookup"><span data-stu-id="93299-649">CurrencyCodeTable</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-650">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-650">Property</span></span></th>
<th><span data-ttu-id="93299-651">説明</span><span class="sxs-lookup"><span data-stu-id="93299-651">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-652">調整</span><span class="sxs-lookup"><span data-stu-id="93299-652">Adjustment</span></span></td>
<td><span data-ttu-id="93299-653">文字列フィールドがデータベースに格納されるときに左揃えか右揃えかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-653">Specify whether the string field should be left-aligned or right-aligned when it&#39;s stored in the database.</span></span> <span data-ttu-id="93299-654">たとえば、11 文字列 &quot;hello world&quot; が <strong>40</strong> の<strong>StringSize</strong> 設定を持つ右揃えのフィールドに格納される場合、29 空白文字が接頭語として格納されます。</span><span class="sxs-lookup"><span data-stu-id="93299-654">For example, if the 11-character string &quot;hello world&quot; is stored in a right-aligned field that has a <strong>StringSize</strong> setting of <strong>40</strong>, 29 space characters are stored as the prefix.</span></span> <span data-ttu-id="93299-655"><strong>注記:</strong> <strong>調整</strong> 設定は、<strong>&gt;</strong>、<strong>&lt;</strong>、<strong>&gt;=</strong>、 <strong>&lt;=</strong> リレーショナル演算子を使用してテーブルの値を検索したときの検索結果に影響します。</span><span class="sxs-lookup"><span data-stu-id="93299-655"><strong>Note:</strong> The <strong>Adjustment</strong> setting affects the search results when you search for a value in a table by using the <strong>&gt;</strong>, <strong>&lt;</strong>, <strong>&gt;=</strong>, and <strong>&lt;=</strong> relational operators.</span></span> <span data-ttu-id="93299-656"><strong>==</strong> 演算子を使用する場合、検索結果に影響を与えることはありません。</span><span class="sxs-lookup"><span data-stu-id="93299-656">It doesn&#39;t affect the search results when you use the <strong>==</strong> operator.</span></span> <span data-ttu-id="93299-657"><strong>調整</strong> 設定は、<strong>StringSize</strong> プロパティが <strong>(Memo)</strong> に設定されている場合無視されます。</span><span class="sxs-lookup"><span data-stu-id="93299-657">The <strong>Adjustment</strong> setting is ignored when the <strong>StringSize</strong> property is set to <strong>(Memo)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-658">AliasFor</span><span class="sxs-lookup"><span data-stu-id="93299-658">AliasFor</span></span></td>
<td><span data-ttu-id="93299-659">フィールドがエイリアスとなるテーブル フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-659">Specify the table field that the field is an alias for.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-660">AllowEdit</span><span class="sxs-lookup"><span data-stu-id="93299-660">AllowEdit</span></span></td>
<td><span data-ttu-id="93299-661">ユーザーがページの既存のレコードのデータを変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-661">Specify whether users are allowed to modify data in an existing record on a page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-662">AllowEditOnCreate</span><span class="sxs-lookup"><span data-stu-id="93299-662">AllowEditOnCreate</span></span></td>
<td><span data-ttu-id="93299-663">新しいレコードが作成されるときにユーザーがフィールドにデータを入力できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-663">Specify whether users are allowed to enter data in the field when a new record is created from a page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-664">AnalysisDefaultTotal</span><span class="sxs-lookup"><span data-stu-id="93299-664">AnalysisDefaultTotal</span></span></td>
<td><span data-ttu-id="93299-665">レポート モデルについては、このプロパティを使用して、テーブルの自動合計が SSRS およびレポート モデルを使用して構築されるレポートに表示されるときに、フィールド データを集計する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-665">For report models, use this property to specify how field data is aggregated when an automatic total for the table is displayed in a report that is built by using SSRS and report models.</span></span> <span data-ttu-id="93299-666">既定値は <strong>いいえ</strong> で、フィールドが自動的に合計として表示されないことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-666">The default value is <strong>No</strong>, which indicates that the field isn&#39;t automatically shown as a total.</span></span> <span data-ttu-id="93299-667">OLAP キューブで、測定の集計関数を指定するため、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-667">For OLAP cubes, use this property to specify the aggregate function for a measure.</span></span> <span data-ttu-id="93299-668"><strong>AnalysisUsage</strong> プロパティが<strong>測定</strong>に設定されている場合、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-668">Use this property when the <strong>AnalysisUsage</strong> property is set to <strong>Measure</strong>.</span></span> <span data-ttu-id="93299-669"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-669">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-670"><strong>合計 </strong>- セット内のすべての値の合計を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-670"><strong>Sum </strong>– Return the sum of all the values in a set.</span></span></li>
<li><span data-ttu-id="93299-671"><strong>カウント</strong> - セット内の null 以外の品目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-671"><strong>Count </strong>– Return the number of non-null items in a set.</span></span></li>
<li><span data-ttu-id="93299-672"><strong>CountDistinct</strong> - セット内の特徴的な null 以外の品目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-672"><strong>CountDistinct </strong>– Return the number of distinct non-null items in a set.</span></span></li>
<li><span data-ttu-id="93299-673"><strong>最小</strong> - セット内の最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-673"><strong>Min </strong>– Return the minimum value in a set.</span></span></li>
<li><span data-ttu-id="93299-674"><strong>最大</strong> - セット内の最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="93299-674"><strong>Max </strong>– Return the maximum value in a set.</span></span></li>
<li><span data-ttu-id="93299-675"><strong>なし</strong> - 集計関数は適用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-675"><strong>None </strong>– No aggregate function is applied.</span></span></li>
<li><span data-ttu-id="93299-676"><strong>自動 </strong>- このオプションは、派生 EDT に適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-676"><strong>Auto </strong>– This option applies to derived EDTs.</span></span> <span data-ttu-id="93299-677">親 EDT が使用される <strong>AnalysisUsage</strong> プロパティの値。</span><span class="sxs-lookup"><span data-stu-id="93299-677">The value of the <strong>AnalysisUsage</strong> property for the parent EDT is used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-678">AnalysisLabel</span><span class="sxs-lookup"><span data-stu-id="93299-678">AnalysisLabel</span></span></td>
<td><span data-ttu-id="93299-679">テーブル フィールドの SSAS キューブ内のキャプションとして使用するラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-679">Specify the label to use as the caption in an SSAS cube for the table field.</span></span> <span data-ttu-id="93299-680">ラベルは、分析コード属性または測定のいずれかに適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-680">The label is applied to either a dimension attribute or a measure.</span></span> <span data-ttu-id="93299-681">このプロパティは、次のいずれかの条件に該当する場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-681">This property is intended for situations where one of the following conditions is true:</span></span>
<ul>
<li><span data-ttu-id="93299-682"><strong>ラベル</strong> プロパティが定義されていません。</span><span class="sxs-lookup"><span data-stu-id="93299-682">The <strong>Label</strong> property isn&#39;t defined.</span></span></li>
<li><span data-ttu-id="93299-683"><strong>ラベル</strong> プロパティは、分析コード属性のキャプションまたは SSAS キューブのメジャーとして機能しません。</span><span class="sxs-lookup"><span data-stu-id="93299-683">The <strong>Label</strong> property doesn&#39;t work as a caption for a dimension attribute or a measure in a SSAS cube.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-684">AnalysisUsage</span><span class="sxs-lookup"><span data-stu-id="93299-684">AnalysisUsage</span></span></td>
<td><span data-ttu-id="93299-685">キューブにおけるフィールドの役割を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-685">Specify the role of the field in a cube.</span></span> <span data-ttu-id="93299-686">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-686">The following options are available</span></span>
<ul>
<li><span data-ttu-id="93299-687"><strong>属性 </strong>- このフィールドは、分析コードの属性です。</span><span class="sxs-lookup"><span data-stu-id="93299-687"><strong>Attribute </strong>– The field is a dimension attribute.</span></span></li>
<li><span data-ttu-id="93299-688"><strong>測定</strong> - このフィールドは、測定です。</span><span class="sxs-lookup"><span data-stu-id="93299-688"><strong>Measure </strong>– The field is a measure.</span></span></li>
<li><span data-ttu-id="93299-689"><strong>両方 </strong>- フィールドは、分析コードの属性と測定の両方です。</span><span class="sxs-lookup"><span data-stu-id="93299-689"><strong>Both </strong>– The field is both a dimension attribute and a measure.</span></span></li>
<li><span data-ttu-id="93299-690"><strong>なし </strong>- フィールドは、分析コードの属性でも測定でもありません。</span><span class="sxs-lookup"><span data-stu-id="93299-690"><strong>None </strong>– The field is neither a dimension attribute nor a measure.</span></span></li>
<li><span data-ttu-id="93299-691"><strong>自動 </strong>- フィールドが基づいている EDT または列挙の <strong>AnalysisUsage</strong> プロパティの値を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-691"><strong>Auto </strong>– The value of the <strong>AnalysisUsage</strong> property for the EDT or enumeration that the field is based on should be used.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-692">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-692">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-693">フィールドのコンフィギュレーション キーを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-693">Set the configuration key for the field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-694">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-694">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-695">テーブル フィールドが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-695">Specify the codes for the countries/regions where the table field is applicable or valid.</span></span> <span data-ttu-id="93299-696">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-696">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-697">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-697">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-698">クライアント フレームワークおよびアプリケーションは、このプロパティを使用して、国または地域固有の機能を有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-698">The client framework and application might use this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-699">CountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="93299-699">CountryRegionContextField</span></span></td>
<td><span data-ttu-id="93299-700">国/地域のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-700">Specify the field that is used to identify the country/region context.</span></span> <span data-ttu-id="93299-701"><strong>CountryRegionCodes</strong> プロパティの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-701">See the description of the <strong>CountryRegionCodes</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-702">ExtendedDataType</span><span class="sxs-lookup"><span data-stu-id="93299-702">ExtendedDataType</span></span></td>
<td><span data-ttu-id="93299-703">このフィールドに使用する EDT を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-703">Specify the EDT to use for this field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-704">GroupPrompt</span><span class="sxs-lookup"><span data-stu-id="93299-704">GroupPrompt</span></span></td>
<td><span data-ttu-id="93299-705">グループに表示されるときにフィールドに使用されるラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-705">Specify a label that is used for the field when it appears in a group.</span></span> <span data-ttu-id="93299-706"><strong>ヒント:</strong> このプロパティを使用して、フィールド ラベルがフィールド グループのラベルに表示されるテキストを繰り返さないようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-706"><strong>Tip:</strong> You can use this property to help guarantee that a field label doesn&#39;t repeat text that appears in the label for a field group.</span></span> <span data-ttu-id="93299-707">たとえば、ページのフィールド グループに<strong>顧客</strong>のラベルが付いている場合、フィールド グループに含まれているフィールドの <strong>GroupPrompt</strong> プロパティで、このテキストを含めないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-707">For example, if a field group on a page is labeled <strong>Customer</strong>, don&#39;t include this text in the <strong>GroupPrompt</strong> property for fields that are included in the field group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-708">HelpText</span><span class="sxs-lookup"><span data-stu-id="93299-708">HelpText</span></span></td>
<td><span data-ttu-id="93299-709">フィールドのヘルプ文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-709">Specify the Help string for the field.</span></span> <span data-ttu-id="93299-710">フィールドがページで使用されている場合は、ヘルプ文字列が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-710">The Help string is shown when the field is used on a page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-711">ID</span><span class="sxs-lookup"><span data-stu-id="93299-711">ID</span></span></td>
<td><span data-ttu-id="93299-712">システムが生成したフィールド ID。</span><span class="sxs-lookup"><span data-stu-id="93299-712">The system-generated field ID.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-713">IgnoreEDTRelation</span><span class="sxs-lookup"><span data-stu-id="93299-713">IgnoreEDTRelation</span></span></td>
<td><span data-ttu-id="93299-714">このプロパティは、EDT 関係の移行中に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-714">This property is used during the migration of EDT relations.</span></span> <span data-ttu-id="93299-715">EDT ノードからテーブル ノードにリレーションを移行するときは、任意のテーブル フィールドの無効なリレーションを省略できます。</span><span class="sxs-lookup"><span data-stu-id="93299-715">When you migrate relations from an EDT node to a table node, you can skip an invalid relation for a given table field.</span></span> <span data-ttu-id="93299-716">無効なリレーションをスキップするには、このプロパティを <strong>はい</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-716">To skip invalid relations, set this property to <strong>Yes</strong>.</span></span> <span data-ttu-id="93299-717">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-717">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-718">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-718">Label</span></span></td>
<td><span data-ttu-id="93299-719">フィールドのラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-719">Specify a label for the field.</span></span> <span data-ttu-id="93299-720">このラベルはページとレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-720">This label will appear on pages and reports.</span></span> <span data-ttu-id="93299-721">このテーブルの前のプロパティ <strong>AnalysisLabel</strong> の説明も参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-721">Also see the description of the <strong>AnalysisLabel</strong> property earlier in this table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-722">必須</span><span class="sxs-lookup"><span data-stu-id="93299-722">Mandatory</span></span></td>
<td><span data-ttu-id="93299-723">ユーザーがページ上のフィールドにデータを追加する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-723">Specify whether a user must add data to a field on a page.</span></span> <span data-ttu-id="93299-724">このプロパティを <strong>はい</strong> を設定し、各データ型の既定または初期化値がデータベースへの持続として許容できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-724">Set this property to <strong>Yes</strong> to indicate that the default or initialization value for each data type isn&#39;t acceptable for persistence into the database.</span></span> <span data-ttu-id="93299-725">次のリストは、ページの必須フィールドに使用できないいくつかの既定値を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-725">The following list shows some default values that can&#39;t be used for mandatory fields on a page:</span></span>
<ul>
<li><span data-ttu-id="93299-726">空は str (文字列) フィールドには受け入れられません。</span><span class="sxs-lookup"><span data-stu-id="93299-726">Empty isn&#39;t acceptable for a str (string) field.</span></span></li>
<li><span data-ttu-id="93299-727">date および utcdatetime などの日付/時刻フィールドでは、最小日時は受け入れられません。</span><span class="sxs-lookup"><span data-stu-id="93299-727">The minimum date-time isn&#39;t acceptable for date-time fields such as date and utcdatetime.</span></span></li>
<li><span data-ttu-id="93299-728">int、real、enum などの数値フィールドでは、0 (ゼロ) の値は受け入れられません。</span><span class="sxs-lookup"><span data-stu-id="93299-728">A value of 0 (zero) isn&#39;t acceptable for numeric fields such as int, real, and enum.</span></span></li>
</ul>
<span data-ttu-id="93299-729">Finance and Operations は、ほとんどの SQL データベース製品に標準的な <strong>Null</strong> 値に対するセマンティクスをサポートしません。</span><span class="sxs-lookup"><span data-stu-id="93299-729">Finance and Operations doesn&#39;t support the semantics for the <strong>null</strong> value that is standard in most SQL database products.</span></span> <span data-ttu-id="93299-730">フィールドはデータベースで Null にはなりません。</span><span class="sxs-lookup"><span data-stu-id="93299-730">Field can&#39;t be nulled in the database.</span></span> <span data-ttu-id="93299-731">したがって、<strong>Mandatory</strong> プロパティは、<strong>null</strong> 値の概念とは関係ありません。</span><span class="sxs-lookup"><span data-stu-id="93299-731">Therefore, the <strong>Mandatory</strong> property has nothing to do with the concept of a <strong>null</strong> value.</span></span> <span data-ttu-id="93299-732"><strong>注意:</strong> 必須テーブル フィールドは、<strong>EnumType</strong> プロパティを列挙に設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-732"><strong>Caution:</strong> A mandatory table field can have its <strong>EnumType</strong> property set to an enumeration.</span></span> <span data-ttu-id="93299-733">整数値 <strong>0</strong> を持つ品目を含む列挙型としてフィールドを定義することがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-733">You might define a field as an enum type that includes an item that has the integer value <strong>0</strong>.</span></span> <span data-ttu-id="93299-734">この場合、<strong>0</strong> はページで選択可能な項目ではありません。</span><span class="sxs-lookup"><span data-stu-id="93299-734">In this case, <strong>0</strong> isn&#39;t an item that&#39;s available for selection on the page.</span></span> <span data-ttu-id="93299-735">フォーム システムは自動的に、<strong>必須</strong> プロパティの設定を強制する <strong>validateWrite</strong> メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="93299-735">The forms system automatically calls the <strong>validateWrite</strong> method to enforce the setting of the <strong>Mandatory</strong> property.</span></span> <span data-ttu-id="93299-736">ただし、<strong>必須</strong>プロパティはテーブル フィールドの値を挿入または更新する直接の X++ SQL の動作には影響を与えません。</span><span class="sxs-lookup"><span data-stu-id="93299-736">However, the <strong>Mandatory</strong> property has no effect on the behavior of direct X++ SQL that inserts or updates the value of a table field.</span></span> <span data-ttu-id="93299-737">直接の X++ SQL では、テーブル バッファ変数に <strong>validateWrite</strong> メソッドへの呼び出しを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-737">In your direct X++ SQL, you can include calls to the <strong>validateWrite</strong> method on your table buffer variable.</span></span> <span data-ttu-id="93299-738">バッファ変数は、<strong>xRecord</strong> クラスからメソッドを継承します。</span><span class="sxs-lookup"><span data-stu-id="93299-738">Your buffer variable inherits the method from the <strong>xRecord</strong> class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-739">MinReadAccess</span><span class="sxs-lookup"><span data-stu-id="93299-739">MinReadAccess</span></span></td>
<td><span data-ttu-id="93299-740">自動承認機能のモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-740">Specify the mode of the automatic authorization feature.</span></span> <span data-ttu-id="93299-741">自動認証には代理外部キーとルックアップの 2 つの操作モードがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-741">Automatic authorization has two modes of operation: surrogate foreign key and lookup.</span></span> <span data-ttu-id="93299-742">照会内の表に代理外部キー許可のタグが付けられていて、ユーザーがその表にアクセスすることはできませんが、明示的に拒否されていない場合、表へのアクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="93299-742">If a table in a query is tagged for surrogate foreign key authorization, and the user doesn&#39;t have access to that table but hasn&#39;t been explicitly denied, view access is granted to the table.</span></span> <span data-ttu-id="93299-743">ただし、すべてのフィールドが表示されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="93299-743">However, not all fields will be visible.</span></span> <span data-ttu-id="93299-744">可視性は次の規則によって決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-744">The visibility is determined by the following rules:</span></span>
<ul>
<li><span data-ttu-id="93299-745"><strong>MinReadAccess</strong> を<strong>いいえ</strong>に設定する場合、フィールドへのアクセスは許可されません。</span><span class="sxs-lookup"><span data-stu-id="93299-745">If <strong>MinReadAccess</strong> is set to <strong>No</strong>, no access is granted to the field.</span></span></li>
<li><span data-ttu-id="93299-746"><strong>MinReadAccess</strong> が<strong>はい</strong>に設定されている場合、フィールドへのビュー アクセスは許可されません。</span><span class="sxs-lookup"><span data-stu-id="93299-746">If <strong>MinReadAccess</strong> is set to <strong>Yes</strong>, view access is granted to the field.</span></span></li>
<li><span data-ttu-id="93299-747">それ以外の場合、フィールドがナチュラル キー自動識別グループの一部である場合、タイトル フィールドである場合、またはシステム フィールドである場合は、表示アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="93299-747">Otherwise, view access is granted if the field is part of the natural key automatic identification group, if it&#39;s a title field, or if it&#39;s a system field.</span></span></li>
</ul>
<span data-ttu-id="93299-748">クエリ内のテーブルがルックアップ承認用にタグされた場合、アクセスが、次のルールによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-748">If a table in a query is tagged for lookup authorization, access is determined by the following rules:</span></span>
<ul>
<li><span data-ttu-id="93299-749"><strong>MinReadAccess</strong> を<strong>いいえ</strong>に設定する場合、フィールドへのアクセスは許可されません。</span><span class="sxs-lookup"><span data-stu-id="93299-749">If <strong>MinReadAccess</strong> is set to <strong>No</strong>, no access is granted to the field.</span></span></li>
<li><span data-ttu-id="93299-750">それ以外の場合、表示アクセスは、このフィールドに許可されます。</span><span class="sxs-lookup"><span data-stu-id="93299-750">Otherwise, view access is granted to the field.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-751">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-751">Model</span></span></td>
<td><span data-ttu-id="93299-752">テーブル フィールドがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-752">Specify the model that the table field is in.</span></span> <span data-ttu-id="93299-753">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-753">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-754">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-754">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-755">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-755">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-756">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-756">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-757">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-757">Name</span></span></td>
<td><span data-ttu-id="93299-758">フィールドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-758">Specify the name of the field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-759">関係コンテキスト</span><span class="sxs-lookup"><span data-stu-id="93299-759">RelationContext</span></span></td>
<td><span data-ttu-id="93299-760">特定のテーブル関係へのフィールドのマッピングを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-760">Specify the mapping of a field to a specific table relation.</span></span> <span data-ttu-id="93299-761">このプロパティは通常、通貨コードまたは数量に関連するデータをモデル化するために測定単位シナリオで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-761">Typically, this property is used in unit-of-measure scenarios to model data that is related to currency codes or quantities.</span></span> <span data-ttu-id="93299-762">フィールドに関連付けられた関係を使用して、通貨コードまたは数量の参照を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-762">The relation that is associated with the field can then be used to show a lookup of currency codes or quantities.</span></span> <span data-ttu-id="93299-763">既定値はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-763">There is no default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-764">SaveContents</span><span class="sxs-lookup"><span data-stu-id="93299-764">SaveContents</span></span></td>
<td><span data-ttu-id="93299-765">フィールド データがデータベースに保存されるか、仮想フィールド データとして扱われるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-765">Specify whether the field data is saved in the database or treated as virtual field data.</span></span> <span data-ttu-id="93299-766">仮想フィールドが表示されるとき、そのフィールドのデータが実行時に計算されます。</span><span class="sxs-lookup"><span data-stu-id="93299-766">Virtual field data is calculated at run time when the field is displayed.</span></span> <span data-ttu-id="93299-767">このデータはデータベースに物理的な表現はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-767">This data has no physical representation in the database.</span></span> <span data-ttu-id="93299-768"><strong>ヒント:</strong> 仮想のフィールドの代わりに、表示メソッドと編集メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-768"><strong>Tip:</strong> Instead of virtual fields, you can use display and edit methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-769">StringSize</span><span class="sxs-lookup"><span data-stu-id="93299-769">StringSize</span></span></td>
<td><span data-ttu-id="93299-770">フィールドの長さを文字数で設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-770">Set the field length, in the number of characters.</span></span> <span data-ttu-id="93299-771">最大フィールドの長さは、データベースによって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-771">The maximum field length depends on the database.</span></span> <span data-ttu-id="93299-772"><strong>(メモ)</strong> の値は、フィールドの長さが無制限であることを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-772">A value of <strong>(Memo)</strong> indicates that the field length is unlimited.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-773">種類</span><span class="sxs-lookup"><span data-stu-id="93299-773">Type</span></span></td>
<td><span data-ttu-id="93299-774">フィールドの基本データ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-774">Specify the base type of a field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-775">表示</span><span class="sxs-lookup"><span data-stu-id="93299-775">Visible</span></span></td>
<td><span data-ttu-id="93299-776">ユーザー インターフェイスにフィールドを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-776">Specify whether the field should be visible in the user interface.</span></span></td>
</tr>
</tbody>
</table>

## <a name="table-index-properties"></a><span data-ttu-id="93299-777">テーブル インデックスのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-777">Table index properties</span></span>
<span data-ttu-id="93299-778">次のテーブルに、テーブルのインデックスで使用可能なプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-778">The following table describes the properties that are available for indexes on tables.</span></span>

| <span data-ttu-id="93299-779">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-779">Property</span></span>              | <span data-ttu-id="93299-780">説明</span><span class="sxs-lookup"><span data-stu-id="93299-780">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-781">AllowDuplicates</span><span class="sxs-lookup"><span data-stu-id="93299-781">AllowDuplicates</span></span>       | <span data-ttu-id="93299-782">このプロパティを**はい**に設定すると、インデックスが非一意になる可能があります。</span><span class="sxs-lookup"><span data-stu-id="93299-782">If you set this property to **Yes**, the index can be non-unique.</span></span> <span data-ttu-id="93299-783">1 つ以上の固有のインデックスを作成しない場合、Finance and Operations では最初のインデックスと RecId を組み合わせ、固有のインデックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-783">If you don't create at least one unique index, Finance and Operations creates a unique index by combining the first index and the RecId.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="93299-784">AlternateKey</span><span class="sxs-lookup"><span data-stu-id="93299-784">AlternateKey</span></span>          | <span data-ttu-id="93299-785">このインデックスが代替キーの一部かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-785">Specify whether this index is part of an alternate key.</span></span> <span data-ttu-id="93299-786">インデックス フィールドは、すべてのレコードで一意の値を持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-786">The index field must have a unique value in every record.</span></span>                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="93299-787">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-787">ConfigurationKey</span></span>      | <span data-ttu-id="93299-788">コンフィギュレーション キーを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-788">Set the configuration key.</span></span> <span data-ttu-id="93299-789">コンフィギュレーション キーによって無効にされているインデックス フィールドはインデックスから自動的に削除されます。</span><span class="sxs-lookup"><span data-stu-id="93299-789">An index field that is disabled through a configuration key is automatically removed from the index.</span></span>                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="93299-790">有効</span><span class="sxs-lookup"><span data-stu-id="93299-790">Enabled</span></span>               | <span data-ttu-id="93299-791">このプロパティを使用すると、インデックスを無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-791">You can use this property to disable the index.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="93299-792">ID</span><span class="sxs-lookup"><span data-stu-id="93299-792">ID</span></span>                    | <span data-ttu-id="93299-793">オブジェクトの社内 ID。</span><span class="sxs-lookup"><span data-stu-id="93299-793">The internal identifier of the object.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="93299-794">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-794">Model</span></span>                 | <span data-ttu-id="93299-795">テーブル インデックスがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-795">Specify the model that the table index is in.</span></span> <span data-ttu-id="93299-796">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-796">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-797">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-797">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-798">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-798">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-799">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-799">The same element can exist in a customized version in a model that is in a higher layer.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="93299-800">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-800">Name</span></span>                  | <span data-ttu-id="93299-801">インデックス名を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-801">Specify the index name.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="93299-802">UniqueAcrossCompanies</span><span class="sxs-lookup"><span data-stu-id="93299-802">UniqueAcrossCompanies</span></span> | <span data-ttu-id="93299-803">このプロパティは、Microsoft 内部でのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-803">This property is for internal Microsoft use only.</span></span> <span data-ttu-id="93299-804">使用可能な値は、**はい** および **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="93299-804">The available values are **Yes** and **No**.</span></span> <span data-ttu-id="93299-805">既定値は **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="93299-805">The default value is **No**.</span></span> <span data-ttu-id="93299-806">**AllowDuplicates** プロパティが **No** に設定されている場合、値は無視されます。</span><span class="sxs-lookup"><span data-stu-id="93299-806">The value of this property is ignored when the **AllowDuplicates** property is set to **No**.</span></span> <span data-ttu-id="93299-807">ただし、**AllowDuplicates** が**はい**に設定されると、**UniqueAcrossCompanies** の**はい**の値は一部の会社間のクエリのパフォーマンスを向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-807">However, when **AllowDuplicates** is set to **Yes**, a value of **Yes** for **UniqueAcrossCompanies** can improve the performance of some cross-company queries.</span></span> <span data-ttu-id="93299-808">パフォーマンスの向上が、データのキャッシングを変更することによって得られます。</span><span class="sxs-lookup"><span data-stu-id="93299-808">The performance improvement is caused by changes to the caching of data.</span></span> |
| <span data-ttu-id="93299-809">ValidTimeStateKey</span><span class="sxs-lookup"><span data-stu-id="93299-809">ValidTimeStateKey</span></span>     | <span data-ttu-id="93299-810">このインデックス キーが親テーブルと有効時間状態の関係を決定するために使用されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-810">Specify whether this index key is used to determine the valid time state relationship with the parent table.</span></span> <span data-ttu-id="93299-811">既定値は **いいえ** です。</span><span class="sxs-lookup"><span data-stu-id="93299-811">The default value is **No**.</span></span> <span data-ttu-id="93299-812">**ヒント:** このプロパティを有効にするには **AllowDuplicates** プロパティを**いいえ**、**AlternateKey** プロパティを**はい**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-812">**Tip:** To enable this property, you must set the **AllowDuplicates** property to **No** and the **AlternateKey** property to **Yes**.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="93299-813">ValidTimeStateMode</span><span class="sxs-lookup"><span data-stu-id="93299-813">ValidTimeStateMode</span></span>    | <span data-ttu-id="93299-814">2 つの有効日レコードの間にギャップが許可されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-814">Specify whether gaps are allowed between two date-effective records.</span></span> <span data-ttu-id="93299-815">既定値は **NoGap** です。</span><span class="sxs-lookup"><span data-stu-id="93299-815">The default value is **NoGap**.</span></span> <span data-ttu-id="93299-816">**ヒント:** このプロパティを有効にするには、**AllowDuplicates** プロパティを**いいえ**に、**AlternateKey** プロパティを**はい**に、 **ValidTimeStateKey** プロパティを**はい**に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-816">**Tip:** To enable this property, you must set the **AllowDuplicates** property to **No**, the **AlternateKey** property to **Yes**, and the **ValidTimeStateKey** property to **Yes**.</span></span>                                                                                                                                                                        |

<span data-ttu-id="93299-817">**注記:** ページは最初のインデックスで並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="93299-817">**Note:** Pages sort on the first index.</span></span>

## <a name="table-relation-properties"></a><span data-ttu-id="93299-818">テーブル関係プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-818">Table relation properties</span></span>
### <a name="list-of-properties"></a><span data-ttu-id="93299-819">プロパティのリスト</span><span class="sxs-lookup"><span data-stu-id="93299-819">List of properties</span></span>

<span data-ttu-id="93299-820">次のテーブルは、アプリケーション エクスプローラーでのテーブル リレーションのプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-820">The following table describes the properties for a table relation in Application Explorer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-821">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-821">Property</span></span></th>
<th><span data-ttu-id="93299-822">説明</span><span class="sxs-lookup"><span data-stu-id="93299-822">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-823">基数</span><span class="sxs-lookup"><span data-stu-id="93299-823">Cardinality</span></span></td>
<td><span data-ttu-id="93299-824">参照テーブルの各主キー値が現在のテーブルの外部キー列で発生しなければならない回数。</span><span class="sxs-lookup"><span data-stu-id="93299-824">The number of times that each primary key value from the referenced table must occur in the foreign key column of the current table.</span></span> <span data-ttu-id="93299-825">たとえば、<strong>OneMore</strong> 値は、1 以上で、0 ではないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="93299-825">For example, the <strong>OneMore</strong> value means one or more, but not zero.</span></span> <span data-ttu-id="93299-826">この値は、すべての親キー値が子テーブル&#39;の外部キー列に最低 1 回現れなければならないことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-826">This value indicates that every parent key value must occur in the child table&#39;s foreign key column at least one time.</span></span> <span data-ttu-id="93299-827">ビジネス ルールが、販売された少なくとも 1 つの品目に関連する親 SalesTable テーブルのすべてのレコードを必要とする場合、SalesLine テーブルのリレーション ノードは、<strong>OneMore</strong> 値を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-827">A relation node under a SalesLine table might use the <strong>OneMore</strong> value when the business rule requires that every record in the parent SalesTable table relate to at least one item that is being sold.</span></span> <span data-ttu-id="93299-828">現在、Finance and Operations は<strong>カーディナリティ</strong> プロパティを使用しません。</span><span class="sxs-lookup"><span data-stu-id="93299-828">Currently, Finance and Operations doesn&#39;t use the <strong>Cardinality</strong> property.</span></span> <span data-ttu-id="93299-829">ただし、今後のリリースはこのプロパティおよび <strong>RelatedTableCardinality</strong> プロパティを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93299-829">However, future releases might use this property and the <strong>RelatedTableCardinality</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-830">CreateNavigationPropertyMethods</span><span class="sxs-lookup"><span data-stu-id="93299-830">CreateNavigationPropertyMethods</span></span></td>
<td><span data-ttu-id="93299-831"><strong>はい</strong>の値は、各外部キー リレーション ノードのテーブル バッファ クラスでナビゲーション メソッドを生成するシステムに指示します。</span><span class="sxs-lookup"><span data-stu-id="93299-831">A value of <strong>Yes</strong> instructs the system to generate navigation methods on the table buffer class for each foreign key relation node.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-832">EDTRelation</span><span class="sxs-lookup"><span data-stu-id="93299-832">EDTRelation</span></span></td>
<td><span data-ttu-id="93299-833">値が<strong>はい</strong>に設定されている場合、ソフトウェア ツールが古い EDT 関係からこの関係を現在の場所に移行するために使用されました。</span><span class="sxs-lookup"><span data-stu-id="93299-833">If the value is set to <strong>Yes</strong>, a software tool was used to migrate this relation to its current location from an old EDT relation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-834">EntityRelationshipRole</span><span class="sxs-lookup"><span data-stu-id="93299-834">EntityRelationshipRole</span></span></td>
<td><span data-ttu-id="93299-835">このプロパティは、テーブルに定義された関係のセマンティクスを明確にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-835">This property is used to clarify the semantics of a relationship that is defined on a table.</span></span> <span data-ttu-id="93299-836">ロール名は、名詞または名詞句のいずれかにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-836">A role name should be either a noun or a noun phrase.</span></span> <span data-ttu-id="93299-837">ロール名は、関連するオブジェクトに関連するテーブルの役割を示す必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-837">The role name should indicate the role of the associated table in relation to the associating object.</span></span> <span data-ttu-id="93299-838">あるいは、ロール名は、テーブルが関係内で果たす役割を示す現在の時制動詞で始まる短い語句でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="93299-838">Alternatively, the role name should be a short phrase that starts with a present-tense verb that indicates the role that the table plays in the relationship.</span></span> <span data-ttu-id="93299-839">ロール名は、関係があいまいではないときは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="93299-839">Role names aren&#39;t required when the relationship is unambiguous.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-840">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-840">Model</span></span></td>
<td><span data-ttu-id="93299-841">このリレーションが含まれるモデル。</span><span class="sxs-lookup"><span data-stu-id="93299-841">The model that this relation is part of.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-842">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-842">Name</span></span></td>
<td><span data-ttu-id="93299-843">関係のために選択した内容を示す名前。</span><span class="sxs-lookup"><span data-stu-id="93299-843">A descriptive name that you choose for the relation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-844">NavigationPropertyMethodNameOverride</span><span class="sxs-lookup"><span data-stu-id="93299-844">NavigationPropertyMethodNameOverride</span></span></td>
<td><span data-ttu-id="93299-845">ナビゲーション メソッドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-845">Specify the name of the navigation method.</span></span> <span data-ttu-id="93299-846">値が指定されていない場合、ナビゲーション メソッドは <strong>RelatedTableRole</strong> プロパティからの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-846">If no value is specified, the navigation method uses the value from the <strong>RelatedTableRole</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-847">RelatedTableCardinality</span><span class="sxs-lookup"><span data-stu-id="93299-847">RelatedTableCardinality</span></span></td>
<td><span data-ttu-id="93299-848">現在のテーブルの一部またはすべてのレコードにおいて、現在のテーブルの外部キー フィールドの値を <strong>null</strong> にできるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-848">Specify whether the foreign key field value in the current table can be <strong>null</strong> in some or all records of the current table.</span></span> <span data-ttu-id="93299-849"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-849">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-850"><strong>ZeroOne</strong> 0 または 1 を意味します。</span><span class="sxs-lookup"><span data-stu-id="93299-850"><strong>ZeroOne</strong> means zero or one.</span></span> <span data-ttu-id="93299-851">この値は、子レコードの外部キー フィールドが <strong>ヌル</strong> になる可能性があることを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-851">This value indicates that the foreign key field in a child record can be <strong>null</strong>.</span></span></li>
<li><span data-ttu-id="93299-852"><strong>ExactlyOne</strong> は、任意の子レコードで外部キーフィールドを <strong>null</strong> にできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-852"><strong>ExactlyOne</strong> indicates that the foreign key field can&#39;t be <strong>null</strong> in any child record.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-853">RelatedTableRole</span><span class="sxs-lookup"><span data-stu-id="93299-853">RelatedTableRole</span></span></td>
<td><span data-ttu-id="93299-854">この関係に参照される親テーブルの目的を説明するテキスト値を入力します。</span><span class="sxs-lookup"><span data-stu-id="93299-854">Enter a text value to describe the purpose of the referenced parent table in this relationship.</span></span> <span data-ttu-id="93299-855">指定された親テーブルを参照する 1 つリレーションのみがテーブルに存在するときは、親テーブルの名前を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-855">When a table has only one relation that references a given parent table, you can use the name of the parent table.</span></span> <span data-ttu-id="93299-856">場合によっては、テーブルに、指定された参照先の親テーブルとの関係が複数あります。</span><span class="sxs-lookup"><span data-stu-id="93299-856">Sometimes, a table has more than one relation to a given referenced parent table.</span></span> <span data-ttu-id="93299-857">この場合、<strong>RelatedTableRole</strong> プロパティの値は、リレーションの目的を同じ親テーブルに対する他のリレーションと区別するために、リレーションについて十分説明する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-857">this case, the value of the <strong>RelatedTableRole</strong> property should describe the relation well enough to distinguish the relation&#39;s purpose from the other relation to the same parent table.</span></span> <span data-ttu-id="93299-858">このプロパティ値は、アプリケーション エクスプローラー クエリでのデータ ソース リレーションの <strong>JoinRelation</strong> プロパティ値として使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-858">The value of this property can be used as the value of the <strong>JoinRelation</strong> property of a data source relation under an Application Explorer query.</span></span> <span data-ttu-id="93299-859">標準的に、この使用方法は正常でない部分が少なくなるためお勧めです。</span><span class="sxs-lookup"><span data-stu-id="93299-859">In standard cases, this usage is recommended, because it reduces denormalization.</span></span> <span data-ttu-id="93299-860">このプロパティは、<strong>UseDefaultRoleNames</strong> プロパティと連携します。</span><span class="sxs-lookup"><span data-stu-id="93299-860">This property interacts with the <strong>UseDefaultRoleNames</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-861">RelationshipType</span><span class="sxs-lookup"><span data-stu-id="93299-861">RelationshipType</span></span></td>
<td><span data-ttu-id="93299-862">2 つのテーブル間の微妙な関係を示す値を選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-862">Select a value that describes the subtle relationship between two tables.</span></span> <span data-ttu-id="93299-863">たとえば、<strong>構成</strong>値は、特定の親レコードに関連していない限り、子レコードが意味深く存在できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-863">For example, the <strong>Composition</strong> value indicates that the child record can&#39;t meaningfully exist unless it&#39;s related to a specific parent record.</span></span> <span data-ttu-id="93299-864">親建物テーブルのレコードを参照しない限り、フロア テーブルの 4 階のレコードは存在できません。</span><span class="sxs-lookup"><span data-stu-id="93299-864">The record for the fourth floor in the Floor table can&#39;t exist unless it references a record in the parent Building table.</span></span> <span data-ttu-id="93299-865"><strong>注記:</strong> DeleteActions は、このプロパティの設定と互換性があることが必要です。</span><span class="sxs-lookup"><span data-stu-id="93299-865"><strong>Note:</strong> The DeleteActions should be compatible with this property setting.</span></span> <span data-ttu-id="93299-866">構成の関係で、DeleteActions はカスケード動作の削除を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-866">For a Composition relationship, the DeleteActions should include delete cascade behavior.</span></span> <span data-ttu-id="93299-867">現在、Finance and Operations は <strong>RelationshipType</strong> プロパティを使用しません。</span><span class="sxs-lookup"><span data-stu-id="93299-867">Currently, Finance and Operations doesn&#39;t use the <strong>RelationshipType</strong> property.</span></span> <span data-ttu-id="93299-868">ただし、将来のリリースはこのプロパティを使用する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93299-868">However, a future release might use this property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-869">役割</span><span class="sxs-lookup"><span data-stu-id="93299-869">Role</span></span></td>
<td><span data-ttu-id="93299-870">関係の意味やロールを説明する名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-870">Specify a name that describes the meaning or role of the relation.</span></span> <span data-ttu-id="93299-871">たとえば、部門テーブルへの 1 つの関係は、従業員が現在所属する部門を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-871">For example, one relation to a Department table could track the department that the employee currently belongs to.</span></span> <span data-ttu-id="93299-872">別の関係では、従業員が移動を要求した部門を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="93299-872">Another relation could track the department that the employee has requested a transfer to.</span></span> <span data-ttu-id="93299-873">これらの関係は両方とも部門テーブルとの関係ではありますが、さまざまな異なる役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="93299-873">Although both these relations are relations to the Department table, they fill different roles.</span></span> <span data-ttu-id="93299-874">このプロパティの値として、アンダースコア (_) の文字を使用し、子テーブルと親テーブルの名前を結合することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="93299-874">As the value of this property, it&#39;s a good idea to join the names of the child table and parent table by using an underscore (_) character.</span></span> <span data-ttu-id="93299-875">たとえば、<strong>SalesTable_SalesLine</strong> を入力します。</span><span class="sxs-lookup"><span data-stu-id="93299-875">For example, enter <strong>SalesTable_SalesLine</strong>.</span></span> <span data-ttu-id="93299-876">このプロパティは、<strong>UseDefaultRoleNames</strong> プロパティと連携します。</span><span class="sxs-lookup"><span data-stu-id="93299-876">This property interacts with the <strong>UseDefaultRoleNames</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-877">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-877">Table</span></span></td>
<td><span data-ttu-id="93299-878">リレーションが参照するテーブル。</span><span class="sxs-lookup"><span data-stu-id="93299-878">The table that the relation refers to.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-879">UseDefaultRoleNames</span><span class="sxs-lookup"><span data-stu-id="93299-879">UseDefaultRoleNames</span></span></td>
<td><span data-ttu-id="93299-880"><strong>はい</strong>の値は、システムが<strong>ロール</strong>および <strong>RelatedTableRole</strong> プロパティの規定値を生成する必要があることを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-880">A value of <strong>Yes</strong> indicates that the system must generate default values for the <strong>Role</strong> and <strong>RelatedTableRole</strong> properties.</span></span> <span data-ttu-id="93299-881">プロパティが<strong>はい</strong>に設定されている場合でも、<strong>ロール</strong>および <strong>RelatedTableRole</strong> に対して生成された値は、<strong>プロパティ</strong>ウィンドウに表示されません。</span><span class="sxs-lookup"><span data-stu-id="93299-881">Even when this property is set to <strong>Yes</strong>, the values for that are generated for <strong>Role</strong> and <strong>RelatedTableRole</strong> don&#39;t appear in the <strong>Properties</strong> window.</span></span> <span data-ttu-id="93299-882">また、<strong>TreeNode</strong> クラスは、生成値を使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-882">Additionally, the <strong>TreeNode</strong> class doesn&#39;t use the generate values.</span></span> <span data-ttu-id="93299-883">ただし、<strong>DictRelation</strong> リフレクション クラスでは生成された値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-883">However, the <strong>DictRelation</strong> reflection class does use the generated values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-884">検証</span><span class="sxs-lookup"><span data-stu-id="93299-884">Validate</span></span></td>
<td><span data-ttu-id="93299-885"><strong>はい</strong>の値は、ページがレコードを子テーブルに挿入するときに、関連するレコードが参照されている親テーブルに存在しないかぎり、挿入が拒否されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-885">A value of <strong>Yes</strong> indicates that when a page inserts a record into the child table, the insertion is rejected unless the related record exists in the referenced parent table.</span></span> <span data-ttu-id="93299-886">また、ページが親テーブルからレコードを削除すると、削除は拒否されるか、子テーブルで関連するレコードに重ねて表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-886">Additionally, when a page deletes a record from the parent table, the deletion is either rejected or cascades to the related records in the child table.</span></span> <span data-ttu-id="93299-887"><strong>RelationshipType</strong> プロパティが <strong>リンク</strong> に設定されているとき、値を <strong>いいえ</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-887">Set the value to <strong>No</strong> when the <strong>RelationshipType</strong> property is set to <strong>Link</strong>.</span></span> <span data-ttu-id="93299-888">いくつかのアップグレード シナリオなどの特別な一時的なケースでは、値を <strong>いいえ</strong> に設定する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="93299-888">You might also set the value to <strong>No</strong> in special temporary cases, such as during some upgrade scenarios.</span></span> <span data-ttu-id="93299-889">値の設定を <strong>はい</strong> に戻したとき、値が <strong>いいえ</strong> の間に挿入または削除されたレコードについては検証は実行されません。</span><span class="sxs-lookup"><span data-stu-id="93299-889">When the value is set back to <strong>Yes</strong>, no validation occurs for records that were inserted or deleted while the value was <strong>No</strong>.</span></span> <span data-ttu-id="93299-890"><strong>注意:</strong> <strong>Validate</strong> プロパティの <strong>Yes</strong> の値は、直接 X++ SQL データ操作が親レコードを削除したり、外部キーデータの整合性に違反する子レコードを挿入したりすることを防ぎません。</span><span class="sxs-lookup"><span data-stu-id="93299-890"><strong>Caution:</strong> A value of <strong>Yes</strong> for the <strong>Validate</strong> property doesn&#39;t prevent direct X++ SQL data operations from deleting parent records or inserting child records that violate the integrity of foreign key data.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="93299-891">**注記:** **SaveDataPerCompany** プロパティが両方のテーブルに対して、**はい**に設定されている場合、システムは**DataAreaId** フィールドを各リレーションシップに追加します。</span><span class="sxs-lookup"><span data-stu-id="93299-891">**Note:** When the **SaveDataPerCompany** property is set to **Yes** for both tables, the system adds the **DataAreaId** field to each relationship.</span></span>

### <a name="relatedtablerole-and-query-joinrelation"></a><span data-ttu-id="93299-892">RelatedTableRole およびクエリ JoinRelation</span><span class="sxs-lookup"><span data-stu-id="93299-892">RelatedTableRole and query JoinRelation</span></span>

<span data-ttu-id="93299-893">このセクションでは、**RelatedTableRole** プロパティを使用して新しいクエリの作成を簡略化する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-893">This section describes how you can use the **RelatedTableRole** property to simplify the creation of a new query.</span></span> <span data-ttu-id="93299-894">テーブル関係上の **RelatedTableRole** プロパティの明示的な値を入力すると、その値を使用し、アプリケーション エクスプローラーにある**クエリ** &gt; **MyQuery** ノードのデータ ソースの関係の **JoinRelation** プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-894">If you enter an explicit value for the **RelatedTableRole** property on a table relation, you can use that value to populate the **JoinRelation** property on a data source relation under a **Queries** &gt; **MyQuery** node in Application Explorer.</span></span> <span data-ttu-id="93299-895">この方法を使用して、1 つの場所に結合のフィールドを指定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-895">You can use this method to specify the fields of the join in one location.</span></span> <span data-ttu-id="93299-896">結合フィールドを変更した場合は、一箇所だけ結合を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-896">If the join fields ever change, you must update the join in only one location.</span></span> <span data-ttu-id="93299-897">**JoinRelation** プロパティの値を設定する前に、**フィールド**および **RelatedField** プロパティの値を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-897">Before you can set a value for the **JoinRelation** property, you must delete the values of the **Field** and **RelatedField** properties.</span></span>

### <a name="createnavigationpropertymethods-and-relatedtablerole"></a><span data-ttu-id="93299-898">CreateNavigationPropertyMethods および RelatedTableRole</span><span class="sxs-lookup"><span data-stu-id="93299-898">CreateNavigationPropertyMethods and RelatedTableRole</span></span>

<span data-ttu-id="93299-899">テーブル リレーションで、**CreateNavigationPropertyMethods** プロパティを **はい** に設定すると、テーブル バッファ クラスのナビゲーション メソッドが生成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-899">When you set the **CreateNavigationPropertyMethods** property to **Yes** on a table relation, the system generates navigation methods for the table buffer class.</span></span> <span data-ttu-id="93299-900">ナビゲーション メソッドは、外部キーのリレーションシップを使用してテーブル バッファの 2 つのインスタンスをリンクします。</span><span class="sxs-lookup"><span data-stu-id="93299-900">A navigation method links two table buffer instances by using their foreign key relationship.</span></span> <span data-ttu-id="93299-901">**UnitOfWork** クラスは、このナビゲーション リンクが使用されている 1 つの領域です。</span><span class="sxs-lookup"><span data-stu-id="93299-901">The **UnitOfWork** class is one area where this navigation linkage is used.</span></span> <span data-ttu-id="93299-902">ナビゲーション メソッドの名前は、テーブル関連の **RelatedTableRole** プロパティの値からコピーされます。</span><span class="sxs-lookup"><span data-stu-id="93299-902">The name of a navigation method is copied from the value of the **RelatedTableRole** property on the table relation.</span></span> <span data-ttu-id="93299-903">この動作は、**RelatedTableRole** 値が **Properties** ウィンドウに明示的に設定され、**UseDefaultRoleNames** プロパティが **Yes** に設定されているため、**RelatedTableRole** 値を生成するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-903">This behavior is used when the **RelatedTableRole** value is explicitly set in the **Properties** window, and when the system generates the **RelatedTableRole** value because the **UseDefaultRoleNames** property is set to **Yes**.</span></span> <span data-ttu-id="93299-904">プロパティ値は、子 CustTable バッファで次のナビゲーション メソッドを生成します。</span><span class="sxs-lookup"><span data-stu-id="93299-904">The property values generate the following navigation method on the child CustTable buffer.</span></span> <span data-ttu-id="93299-905">ほとんど直接的に、ナビゲーション メソッドの名前は **RelatedTableRole** プロパティの値からをコピーされます。</span><span class="sxs-lookup"><span data-stu-id="93299-905">Most directly, the navigation method name is copied from the value of the **RelatedTableRole** property.</span></span>

    public final CustBankAccount BankAccounts([CustBankAccount relatedTable])

#### <a name="navigationpropertymethodnameoverride-property"></a><span data-ttu-id="93299-906">NavigationPropertyMethodNameOverride プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-906">NavigationPropertyMethodNameOverride property</span></span>

<span data-ttu-id="93299-907">次のリストでは、システムがテーブル バッファ クラスでナビゲーション メソッドに対して生成する名前を上書きする必要がある場合について説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-907">The following list describes cases where you must override the name that the system generates for a navigation method on a table buffer class:</span></span>

-   <span data-ttu-id="93299-908">テーブル クラスにはすでに **RelatedTableRole** プロパティの値と一致するメソッド名があります。</span><span class="sxs-lookup"><span data-stu-id="93299-908">The table class already has a method name that matches the values of the **RelatedTableRole** property.</span></span>
-   <span data-ttu-id="93299-909">**RelatedTableRole** プロパティの値がメソッド名に使用できる最大長を超えています。</span><span class="sxs-lookup"><span data-stu-id="93299-909">The value of the **RelatedTableRole** property exceeds the maximum length that can be used for a method name.</span></span>

<span data-ttu-id="93299-910">そのような場合、ナビゲーション メソッドの有効な名前を選択し、テーブル リレーションの **NavigationPropertyMethodNameOverride** プロパティの値としてその名前を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-910">In these cases, you must choose a valid name for the navigation method and assign that name as the value of the **NavigationPropertyMethodNameOverride** property on the table relation.</span></span>

## <a name="understanding-the-relationshiptype-enumeration"></a><span data-ttu-id="93299-911">RelationshipType の列挙型を理解する</span><span class="sxs-lookup"><span data-stu-id="93299-911">Understanding the RelationshipType enumeration</span></span>
<span data-ttu-id="93299-912">テーブル リレーションの下にノードを追加するとき、新しいリレーションの **RelationshipType** プロパティの値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-912">When you add a node under table relations, you can set the value of the **RelationshipType** property for the new relation.</span></span> <span data-ttu-id="93299-913">**RelationshipType** プロパティの可能な値のリストは、**RelationshipType** 列挙型の要素のリストです。</span><span class="sxs-lookup"><span data-stu-id="93299-913">The list of possible values for the **RelationshipType** property is the list of elements in the **RelationshipType** enumeration.</span></span> <span data-ttu-id="93299-914">このセクションでは、**RelationshipType** 列挙の各要素の意味について説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-914">This section describes the meaning of each element in the **RelationshipType** enumeration.</span></span>

### <a name="description-of-elements"></a><span data-ttu-id="93299-915">要素の説明</span><span class="sxs-lookup"><span data-stu-id="93299-915">Description of elements</span></span>

<span data-ttu-id="93299-916">次のテーブルでは、**RelationshipType** プロパティの要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-916">The following table describes the elements of the **RelationshipType** property.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-917">要素名</span><span class="sxs-lookup"><span data-stu-id="93299-917">Element name</span></span></th>
<th><span data-ttu-id="93299-918">説明</span><span class="sxs-lookup"><span data-stu-id="93299-918">Description</span></span></th>
<th><span data-ttu-id="93299-919">自動推論</span><span class="sxs-lookup"><span data-stu-id="93299-919">Automatic inference</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-920">NotSpecified</span><span class="sxs-lookup"><span data-stu-id="93299-920">NotSpecified</span></span></td>
<td><span data-ttu-id="93299-921">この要素は、多くの場合 <strong>RelationshipType</strong> プロパティの既定値です。</span><span class="sxs-lookup"><span data-stu-id="93299-921">This element is often the default value of the <strong>RelationshipType</strong> property.</span></span></td>
<td><span data-ttu-id="93299-922"><strong>RelationshipType</strong>プロパティの値が <strong>NotSpecified</strong> のとき、システムは適切な値を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-922">When the <strong>RelationshipType</strong> property has a value of <strong>NotSpecified</strong>, the system infers an appropriate value.</span></span> <span data-ttu-id="93299-923">システムは、次の順序で値を推論します。</span><span class="sxs-lookup"><span data-stu-id="93299-923">The system infers the value in the following sequence:</span></span>
<ol>
<li><span data-ttu-id="93299-924">仕様</span><span class="sxs-lookup"><span data-stu-id="93299-924">Specialization</span></span></li>
<li><span data-ttu-id="93299-925">リンク</span><span class="sxs-lookup"><span data-stu-id="93299-925">Link</span></span></li>
<li><span data-ttu-id="93299-926">構成</span><span class="sxs-lookup"><span data-stu-id="93299-926">Composition</span></span></li>
<li><span data-ttu-id="93299-927">集約</span><span class="sxs-lookup"><span data-stu-id="93299-927">Aggregation</span></span></li>
<li><span data-ttu-id="93299-928">関連</span><span class="sxs-lookup"><span data-stu-id="93299-928">Association</span></span></li>
</ol>
<span data-ttu-id="93299-929">たとえば、構成および集計の両方の基準が満たされている場合、構成が以前にリストで発生したため、システムは構成を暗示します。</span><span class="sxs-lookup"><span data-stu-id="93299-929">For example, if the criteria for both Composition and Aggregation are met, the system infers Composition, because Composition occurs earlier in the list.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-930">仕様</span><span class="sxs-lookup"><span data-stu-id="93299-930">Specialization</span></span></td>
<td><span data-ttu-id="93299-931">この要素はベース テーブルと派生テーブル関係テーブルのテーブル継承のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-931">This element applies only to table inheritance, to relationships between base and derived tables.</span></span></td>
<td><span data-ttu-id="93299-932">テーブルの継承が関係する場合は常に <strong>RelationshipType</strong> プロパティを <strong>Specialization</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-932">The system sets the <strong>RelationshipType</strong> property to <strong>Specialization</strong> whenever table inheritance is involved.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-933">リンク</span><span class="sxs-lookup"><span data-stu-id="93299-933">Link</span></span></td>
<td><span data-ttu-id="93299-934">この要素は、非リレーショナルな関係です。</span><span class="sxs-lookup"><span data-stu-id="93299-934">This element is a non-relational relationship.</span></span> <span data-ttu-id="93299-935"><strong>検証</strong>プロパティを<strong>いいえ</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-935">It requires that the <strong>Validate</strong> property be set to <strong>No</strong>.</span></span> <span data-ttu-id="93299-936">このタイプのリレーションシップは、テーブルの多くのレコードを一覧表示するページと、テーブルの 1 つのレコードの詳細フィールドを提供するページとの間でのナビゲーションをサポートします。</span><span class="sxs-lookup"><span data-stu-id="93299-936">This type of relationship supports navigation between pages that list many records from a table and pages that provide detail fields for one record from the table.</span></span></td>
<td><span data-ttu-id="93299-937">リンクは、以前のバージョンからアップグレードしている間に EDT リンクの関係の移行をサポートするためにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-937">Link is used only to support the migration of EDT link relations during upgrade from earlier versions.</span></span> <span data-ttu-id="93299-938">移行ツールはこの型の関係を作成しますが、作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-938">Migration tools create this type relationship, but you must not.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-939">構成</span><span class="sxs-lookup"><span data-stu-id="93299-939">Composition</span></span></td>
<td><span data-ttu-id="93299-940">この要素は、集約関係のより強力なタイプです。</span><span class="sxs-lookup"><span data-stu-id="93299-940">This element is a stronger type of Aggregation relation.</span></span> <span data-ttu-id="93299-941">テーブルには、複数の構成関係を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-941">A table must not have more than one Composition relation.</span></span> <span data-ttu-id="93299-942">たとえば、建物は部屋で構成され、および指定された部屋は複数の建物の中に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-942">For example, a building is composed of rooms, and a given room can&#39;t exist in more than one building.</span></span></td>
<td><span data-ttu-id="93299-943">合成の基準を満たしていますが、<strong>集計</strong>または<strong>関連</strong>の値を手動で割り当てる場合、システムではその値は<strong>集計</strong>または<strong>関連</strong>としてそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="93299-943">If the criteria for Composition are met, but you manually assign a value of <strong>Aggregation</strong> or <strong>Association</strong>, the system leaves the value as <strong>Aggregation</strong> or <strong>Association</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-944">集約</span><span class="sxs-lookup"><span data-stu-id="93299-944">Aggregation</span></span></td>
<td><span data-ttu-id="93299-945">この要素は、子テーブルが親テーブルのエンティティに従属するとみなされる場合に適しています。 </span><span class="sxs-lookup"><span data-stu-id="93299-945">This element is appropriate when the child table is considered subordinate to the entity of the parent table.</span></span></td>
<td><span data-ttu-id="93299-946">次のいずれかの条件が当てはまる場合、システムは集計を推論します。</span><span class="sxs-lookup"><span data-stu-id="93299-946">The system infers Aggregation when one of the following conditions is true:</span></span>
<ul>
<li><span data-ttu-id="93299-947">親テーブルには、このリレーション ノードを使用するために定義されている削除アクション ノードがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-947">The parent table has a delete action node that is defined to use this relation node.</span></span></li>
<li><span data-ttu-id="93299-948">子テーブル内の関係に対して外部キー フィールドでは<strong>必須</strong>プロパティが<strong>はい</strong>に設定されています。</span><span class="sxs-lookup"><span data-stu-id="93299-948">Any foreign key field for this relation in the child table has the <strong>Mandatory</strong> property set to <strong>Yes</strong>.</span></span></li>
</ul>
<span data-ttu-id="93299-949">集計の基準を満たしていますが、<strong>関連</strong>の値を手動で割り当てる場合、システムではその値は<strong>関連</strong>としてそのまま残ります。</span><span class="sxs-lookup"><span data-stu-id="93299-949">If the criteria for Aggregation are met, but you manually assign a value of <strong>Association</strong>, the system leaves the value as <strong>Association</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-950">関連</span><span class="sxs-lookup"><span data-stu-id="93299-950">Association</span></span></td>
<td><span data-ttu-id="93299-951">この要素は、標準の外部キーの概念です。</span><span class="sxs-lookup"><span data-stu-id="93299-951">This element is the concept of a standard foreign key.</span></span></td>
<td><span data-ttu-id="93299-952">プロパティ値がどんな値にも設定されず、集約と合成の両方が不適切な場合は、<strong>RelationshipType</strong> プロパティを<strong>アソシエーション</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-952">You must set the <strong>RelationshipType</strong> property to <strong>Association</strong> if the system doesn&#39;t set the value of the property to anything, and if both Aggregation and Composition are inappropriate.</span></span></td>
</tr>
</tbody>
</table>

## <a name="view-properties"></a><span data-ttu-id="93299-953">プロパティの表示</span><span class="sxs-lookup"><span data-stu-id="93299-953">View properties</span></span>
<span data-ttu-id="93299-954">ビューのプロパティは、テーブルのプロパティと同じです。</span><span class="sxs-lookup"><span data-stu-id="93299-954">The properties for views are the same as the properties for tables.</span></span> <span data-ttu-id="93299-955">ただし、ビューは読み取り専用であるため、それらのプロパティのほとんどは変更できません。</span><span class="sxs-lookup"><span data-stu-id="93299-955">However, because views are read-only, most of their properties can't be changed.</span></span> <span data-ttu-id="93299-956">これらのプロパティの一部には固定値があり、ビューを定義するクエリで使用されているデータ ソースから継承されたプロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="93299-956">Some of these properties have fixed values, and some are inherited from the data sources that are used in the query that defines the view.</span></span> <span data-ttu-id="93299-957">ビューの次のプロパティは、SSRS を使用しているときのデータ分析に関連しています。</span><span class="sxs-lookup"><span data-stu-id="93299-957">The following properties for views are related to data analysis when you're using SSRS.</span></span> <span data-ttu-id="93299-958">これらすべての既定のプロパティを変更できます。</span><span class="sxs-lookup"><span data-stu-id="93299-958">All these properties can be changed.</span></span>

-   <span data-ttu-id="93299-959">AnalysisVisibility</span><span class="sxs-lookup"><span data-stu-id="93299-959">AnalysisVisibility</span></span>
-   <span data-ttu-id="93299-960">AnalysisSelection</span><span class="sxs-lookup"><span data-stu-id="93299-960">AnalysisSelection</span></span>
-   <span data-ttu-id="93299-961">TypicalRowCount</span><span class="sxs-lookup"><span data-stu-id="93299-961">TypicalRowCount</span></span>
-   <span data-ttu-id="93299-962">IsLookup</span><span class="sxs-lookup"><span data-stu-id="93299-962">IsLookup</span></span>
-   <span data-ttu-id="93299-963">SingularLabel</span><span class="sxs-lookup"><span data-stu-id="93299-963">SingularLabel</span></span>

<span data-ttu-id="93299-964">次のテーブルに、ビューに設定できるプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-964">The following table describes the properties that can be set for a view.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-965">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-965">Property</span></span></th>
<th><span data-ttu-id="93299-966">説明</span><span class="sxs-lookup"><span data-stu-id="93299-966">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-967">AOSAuthorization</span><span class="sxs-lookup"><span data-stu-id="93299-967">AOSAuthorization</span></span></td>
<td><span data-ttu-id="93299-968">データ アクセス許可の検証が必要なデータ アクセス操作を指定するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-968">Use this property to specify which data access operations require verification of user permissions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-969">CacheLookup</span><span class="sxs-lookup"><span data-stu-id="93299-969">CacheLookup</span></span></td>
<td><span data-ttu-id="93299-970">テーブルのレコード キャッシュ レベル。</span><span class="sxs-lookup"><span data-stu-id="93299-970">The record cache level for the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-971">ClusterIndex</span><span class="sxs-lookup"><span data-stu-id="93299-971">ClusterIndex</span></span></td>
<td><span data-ttu-id="93299-972">表のクラスター インデックス (クラスター インデックスがある場合)。</span><span class="sxs-lookup"><span data-stu-id="93299-972">The cluster index of the table, if there is a cluster index.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-973">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-973">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-974">ビューのコンフィギュレーション キーを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-974">Set the configuration key for the view.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-975">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-975">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-976">メニューが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-976">Specify the codes for the countries/regions where the menu is applicable or valid.</span></span> <span data-ttu-id="93299-977">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-977">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-978">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-978">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-979">クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-979">The client uses this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-980">CountryRegionContextField</span><span class="sxs-lookup"><span data-stu-id="93299-980">CountryRegionContextField</span></span></td>
<td><span data-ttu-id="93299-981">国/地域のコンテキストを識別するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-981">Specify the field that is used to identify the country/region context.</span></span> <span data-ttu-id="93299-982"><strong>CountryRegionCodes</strong> プロパティの説明を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-982">See the description of the <strong>CountryRegionCodes</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-983">DeveloperDocumentation</span><span class="sxs-lookup"><span data-stu-id="93299-983">DeveloperDocumentation</span></span></td>
<td><span data-ttu-id="93299-984">表示の目的を説明し、プログラムでどのように使用されているかを説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-984">Describe the purpose of a view, and explain how it&#39;s used in the program.</span></span> <span data-ttu-id="93299-985">通常、説明は 5 つ以下の構文で構成され、単一の段落として書かれます。</span><span class="sxs-lookup"><span data-stu-id="93299-985">Typically, a description contains no more than five sentences and is written as a single paragraph.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-986">EntityRelationshipType</span><span class="sxs-lookup"><span data-stu-id="93299-986">EntityRelationshipType</span></span></td>
<td><span data-ttu-id="93299-987">共通エンティティ リレーションシップ (ER) データ モデルの表記法に従ってビューを分類します。</span><span class="sxs-lookup"><span data-stu-id="93299-987">Classify a view according to common entity relationship (ER) data model notation.</span></span> <span data-ttu-id="93299-988">ビューは、エンティティまたはリレーションシップとして分類されます。</span><span class="sxs-lookup"><span data-stu-id="93299-988">A view is classified as either an entity or a relationship.</span></span> <span data-ttu-id="93299-989">エンティティはオブジェクトを表すのに対し、関係は 2 つのオブジェクト間の関連を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-989">An entity represents an object, whereas a relationship represents an association between two objects.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-990">FormRef</span><span class="sxs-lookup"><span data-stu-id="93299-990">FormRef</span></span></td>
<td><span data-ttu-id="93299-991">ビューの既定のページを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-991">Specify the default page for the view.</span></span> <span data-ttu-id="93299-992">既定のページは、ユーザーがページ上のフィールドのショートカット メニューを使用してメイン テーブルにジャンプするときに表示されるページです。</span><span class="sxs-lookup"><span data-stu-id="93299-992">The default page is the page that is shown when the user activates Jump to Main Table by using the shortcut menu for a field on a page.</span></span> <span data-ttu-id="93299-993">このページは、<strong>表示</strong>タイプのメニュー項目によって参照されます。</span><span class="sxs-lookup"><span data-stu-id="93299-993">The page is referenced through a menu item of the <strong>Display</strong> type.</span></span> <span data-ttu-id="93299-994">このプロパティを空白のままにすると、MorphX はユーザーが参照しているテーブルと同じ名前のページを有効化しようとします。</span><span class="sxs-lookup"><span data-stu-id="93299-994">If you leave this property blank, MorphX tries to activate a page that has the same name as the table that you&#39;re referring to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-995">ID</span><span class="sxs-lookup"><span data-stu-id="93299-995">ID</span></span></td>
<td><span data-ttu-id="93299-996">オブジェクトの社内 ID。</span><span class="sxs-lookup"><span data-stu-id="93299-996">The internal identifier of the object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-997">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-997">Label</span></span></td>
<td><span data-ttu-id="93299-998">ビューのユーザー フレンドリ名を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-998">Specify a user-friendly name for the view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-999">ListPageRef</span><span class="sxs-lookup"><span data-stu-id="93299-999">ListPageRef</span></span></td>
<td><span data-ttu-id="93299-1000">このレコードの種類の一覧を表示できるページをポイントする表示メニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1000">Specify a display menu item that points to a page that can show a list of this record type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1001">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1001">Model</span></span></td>
<td><span data-ttu-id="93299-1002">ビューがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1002">Specify the model that the view is in.</span></span> <span data-ttu-id="93299-1003">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1003">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1004">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1004">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1005">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1005">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1006">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-1006">Name</span></span></td>
<td><span data-ttu-id="93299-1007">ビューの名前を指定します</span><span class="sxs-lookup"><span data-stu-id="93299-1007">Specify the name of the view.</span></span> <span data-ttu-id="93299-1008">この名前は、X++ 言語のビューを参照するときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1008">This name is used when you refer to the view from the X++ language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1009">PreviewPartRef</span><span class="sxs-lookup"><span data-stu-id="93299-1009">PreviewPartRef</span></span></td>
<td><span data-ttu-id="93299-1010">拡張プレビューで使用される情報パーツまたはフォーム パーツを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1010">Specify the info part or form part to use in the enhanced preview.</span></span> <span data-ttu-id="93299-1011">情報パーツは指定したクエリからデータ フィールドのコレクションを表示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-1011">An info part shows a collection of data fields from a specified query.</span></span> <span data-ttu-id="93299-1012">メタデータを使用してデータの表示方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1012">It uses metadata to describe how the data appears.</span></span> <span data-ttu-id="93299-1013">フォーム パーツは、ページへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="93299-1013">A form part represents a pointer to a page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1014">PrimaryIndex</span><span class="sxs-lookup"><span data-stu-id="93299-1014">PrimaryIndex</span></span></td>
<td><span data-ttu-id="93299-1015">ビューのプライマリ インデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1015">Specify the primary index of the view.</span></span> <span data-ttu-id="93299-1016">固有のインデックスのみ選択することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1016">Only a unique index can be selected.</span></span> <span data-ttu-id="93299-1017">このプロパティは、データベースの最適化と、キャッシュ キーとして使用するユニークなインデックスを示すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1017">This property is used for database optimization and to indicate which unique index should be used as the caching key.</span></span> <span data-ttu-id="93299-1018">プライマリ インデックスを指定しない場合、最下位の ID の固有のインデックスはキャッシュ キーとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1018">If you don&#39;t specify a primary index, the unique index that has the lowest ID is used as the caching key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1019">クエリ</span><span class="sxs-lookup"><span data-stu-id="93299-1019">Query</span></span></td>
<td><span data-ttu-id="93299-1020">ビューのデータのソースであるクエリを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1020">Specify the query that is the source of data for the view.</span></span> <span data-ttu-id="93299-1021">ビューに直接データ ソースを追加する代わりに、このプロパティを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1021">You can use this property instead of adding data sources directly to the view.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1022">ReportRef</span><span class="sxs-lookup"><span data-stu-id="93299-1022">ReportRef</span></span></td>
<td><span data-ttu-id="93299-1023">テーブルの既定のレポートの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1023">The name of the default report for the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1024">SaveDataPerCompany</span><span class="sxs-lookup"><span data-stu-id="93299-1024">SaveDataPerCompany</span></span></td>
<td><span data-ttu-id="93299-1025">会社に固有のテーブルに対してこのプロパティを <strong>はい</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1025">Set this property to <strong>Yes</strong> for company-specific tables.</span></span> <span data-ttu-id="93299-1026">データが会社間、インストール、データベース、アプリケーション エクスプ ローラー、トレース、または OLAP に関連する場合、<strong>いいえ</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1026">Set it to <strong>No</strong> if the data is related to cross-companies, installation, a database, Application Explorer, tracing, or OLAP.</span></span> <span data-ttu-id="93299-1027">たとえば、SysTraceTable または OLAPServerTable テーブルは、会社ごとの基準でデータをそのテーブルに保存するかどうか、またはデータが任意の会社への所属なしで利用できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1027">For example, the SysTraceTable or OLAPServerTable table specifies whether data should be saved for that table on a per-company basis, or whether the data should be available without any company affiliation.</span></span> <span data-ttu-id="93299-1028">テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルには、会社 id を含む <strong>DataAreaId</strong> 列が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1028">If the <strong>SaveDataPerCompany</strong> property on a table is set to <strong>Yes</strong>, that table has a <strong>DataAreaId</strong> column that contains the company identifier.</span></span> <span data-ttu-id="93299-1029">テーブルのプロパティが<strong>いいえ</strong>に設定されている場合、<strong>DataAreaId</strong> 列はテーブルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1029">If the table property is set to <strong>No</strong>, the <strong>DataAreaId</strong> column is removed from the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1030">SaveDataPerPartition</span><span class="sxs-lookup"><span data-stu-id="93299-1030">SaveDataPerPartition</span></span></td>
<td><span data-ttu-id="93299-1031">ビューに<strong>パーティション</strong>という名前のシステム フィールドがあるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-1031">A value that indicates whether the view has a system field that is named <strong>Partition</strong>.</span></span> <span data-ttu-id="93299-1032">このプロパティは、読み取り専用になっています。</span><span class="sxs-lookup"><span data-stu-id="93299-1032">This property is intended to be read-only.</span></span> <span data-ttu-id="93299-1033">ビューに<strong>パーティション</strong> フィールドがない場合、各レコードに 1 つのパーティションに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="93299-1033">If the view has a <strong>Partition</strong> field, each record is assigned to one partition.</span></span> <span data-ttu-id="93299-1034">各レコードは、他のパーティションのコンテキストで実行されるデータ アクセス操作から隠されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1034">Each record is hidden from data access operations that are run under the context of other partitions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1035">SearchLinkRefName</span><span class="sxs-lookup"><span data-stu-id="93299-1035">SearchLinkRefName</span></span></td>
<td><span data-ttu-id="93299-1036">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1036">The name of the menu item that links to information on a website about a table record that is listed in the Enterprise Portal search results.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1037">SearchLinkRefType</span><span class="sxs-lookup"><span data-stu-id="93299-1037">SearchLinkRefType</span></span></td>
<td><span data-ttu-id="93299-1038">エンタープライズ ポータルの検索結果に表示されるテーブル レコードに関する Web サイトの情報にリンクするメニュー項目のタイプ。</span><span class="sxs-lookup"><span data-stu-id="93299-1038">The type of the menu item that links to information on a website about a table record that is listed in the Enterprise Portal search results.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1039">SystemTable</span><span class="sxs-lookup"><span data-stu-id="93299-1039">SystemTable</span></span></td>
<td><span data-ttu-id="93299-1040">テーブルがシステム テーブルであるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-1040">A value that indicates whether a table is a system table.</span></span> <span data-ttu-id="93299-1041">システム テーブルは、エクスポートおよびインポート中にフィルター処理でき、ログインしたときに常に同期されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1041">System tables can be filtered during export and import, and are always synchronized when you sign in.</span></span> <span data-ttu-id="93299-1042">したがって、このプロパティは、サインインするとすぐに使用するテーブルに便利です。</span><span class="sxs-lookup"><span data-stu-id="93299-1042">Therefore, this property might be useful for tables that you use as soon as you sign in.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1043">TableContents</span><span class="sxs-lookup"><span data-stu-id="93299-1043">TableContents</span></span></td>
<td><span data-ttu-id="93299-1044">顧客間でセットアップ/パラメーター データを再利用する方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1044">Specify how setup/parameter data can be reused from one customer to another.</span></span> <span data-ttu-id="93299-1045"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1045">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1046"><strong>指定なし</strong> - ほとんどのテーブルにこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1046"><strong>Not specified</strong> – Use this option for most tables.</span></span></li>
<li><span data-ttu-id="93299-1047"><strong>既定のデータ</strong> - このオプションは、郵便番号、単位、時間間隔など、顧客に依存しないデータに使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1047"><strong>Default Data</strong> – Use this option for customer-independent data, such as postal codes, units, and time intervals.</span></span></li>
<li><span data-ttu-id="93299-1048"><strong>基本データ</strong> - カレンダー、グループ、およびパラメータなどの顧客に依存するデータ用のこのオプションを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1048"><strong>Base Data</strong> – Use this option for customer-dependent data, such as calendars, groups, and parameters.</span></span></li>
<li><span data-ttu-id="93299-1049"><strong>既定 + 基本データ</strong> - このオプションは、ローカル知覚が異なるデータに対して使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1049"><strong>Default+Base data</strong> – Use this option for data where the local perception varies.</span></span> <span data-ttu-id="93299-1050">たとえば、勘定科目表は、ドイツでは顧客に依存していませんが、他のほとんどの場所では顧客に依存しています。</span><span class="sxs-lookup"><span data-stu-id="93299-1050">For example, Chart of Accounts is customer-independent in Germany but is customer dependent in most other places.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1051">TableGroup</span><span class="sxs-lookup"><span data-stu-id="93299-1051">TableGroup</span></span></td>
<td><span data-ttu-id="93299-1052">ビューが属するグループを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1052">Specify the group that the view belongs to.</span></span> <span data-ttu-id="93299-1053">テーブル グループは、テーブルに含まれるデータのタイプに応じてテーブルとビューを分類します。</span><span class="sxs-lookup"><span data-stu-id="93299-1053">Table groups categorize tables and views according to the type of data that they contain.</span></span> <span data-ttu-id="93299-1054">ビューは、任意のテーブルと同じテーブル グループに属することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1054">Views can belong to the same table groups as a table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1055">TitleField1、TitleField2</span><span class="sxs-lookup"><span data-stu-id="93299-1055">TitleField1, TitleField2</span></span></td>
<td><span data-ttu-id="93299-1056">ビューのウィンドウ キャプションに表示される情報。</span><span class="sxs-lookup"><span data-stu-id="93299-1056">The information that is shown in the window caption for the view.</span></span> <span data-ttu-id="93299-1057">キャプションは、次の要素から構成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1057">The caption is constructed from the following elements:</span></span>
<ul>
<li><span data-ttu-id="93299-1058"><strong>TitleField1</strong> ラベル。後にコロン (:) とスペースが続きます</span><span class="sxs-lookup"><span data-stu-id="93299-1058">The <strong>TitleField1</strong> label, followed by colon (:) and a space</span></span></li>
<li><span data-ttu-id="93299-1059"><strong>TitleField1</strong> に使用する列の現在のレコードの値、後にコンマ (,) が続きます。</span><span class="sxs-lookup"><span data-stu-id="93299-1059">The value of the current record in the column that is used for <strong>TitleField1</strong>, followed by a comma (,)</span></span></li>
<li><span data-ttu-id="93299-1060"><strong>TitleField2</strong> に使用する列の現在のレコードの値。</span><span class="sxs-lookup"><span data-stu-id="93299-1060">The value of the current record in the column that is used for <strong>TitleField2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1061">ValidTimeStateEnabled</span><span class="sxs-lookup"><span data-stu-id="93299-1061">ValidTimeStateEnabled</span></span></td>
<td><span data-ttu-id="93299-1062">ビューが基になるテーブルの有効な時間状態機能をサポートしているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1062">Specify whether the view supports the valid time state feature of the underlying table.</span></span> <span data-ttu-id="93299-1063">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1063">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="93299-1064">このプロパティは、以下の両方の条件が true の場合にのみ <strong>はい</strong> に設定することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1064">You can set this property to <strong>Yes</strong> only if both the following conditions are true:</span></span>
<ul>
<li><span data-ttu-id="93299-1065">基礎になるテーブルは有効時間状態テーブルです。</span><span class="sxs-lookup"><span data-stu-id="93299-1065">The underlying table is a valid time state table.</span></span></li>
<li><span data-ttu-id="93299-1066">ビューの <strong>Fields</strong> リストには、<strong>ValidFrom</strong> および <strong>ValidTo</strong> があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1066">The view has <strong>ValidFrom</strong> and <strong>ValidTo</strong> in its <strong>Fields</strong> list.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1067">表示</span><span class="sxs-lookup"><span data-stu-id="93299-1067">Visible</span></span></td>
<td><span data-ttu-id="93299-1068">テーブルがページやレポート内のデータ ソースとして使用される場合のアクセス権を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1068">Specify the access rights when the table is used as a data source on a page or a report.</span></span> <span data-ttu-id="93299-1069">テーブルをページ内のデータ ソースとして使用する場合、ページのアクセス権は、テーブルに対して定義されているアクセス権を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1069">If the table is used as a data source on a page, the access rights on the page can&#39;t exceed the access rights that are defined for the table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="data-set-properties"></a><span data-ttu-id="93299-1070">データ セットのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1070">Data set properties</span></span>
<span data-ttu-id="93299-1071">このセクションでは、アプリケーション エクスプローラーのデータセット要素のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1071">This section contains descriptions of the properties on data set elements in Application Explorer.</span></span> <span data-ttu-id="93299-1072">**データ セット** ノードは、アプリケーション エクスプローラーの高レベル ノードです。</span><span class="sxs-lookup"><span data-stu-id="93299-1072">The **Data Sets** node is a high-level node in Application Explorer.</span></span> <span data-ttu-id="93299-1073">データ セットは、エンタープライズ ポータルのデータへのアクセスに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1073">Data sets are used to access data in Enterprise Portal.</span></span>

### <a name="description-of-properties"></a><span data-ttu-id="93299-1074">プロパティの説明</span><span class="sxs-lookup"><span data-stu-id="93299-1074">Description of properties</span></span>

<span data-ttu-id="93299-1075">次のテーブルは、アプリケーション エクスプローラーの データ セット ノードで使用可能なプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-1075">The following table describes the properties that are available on data set nodes in Application Explorer.</span></span>

| <span data-ttu-id="93299-1076">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1076">Property</span></span> | <span data-ttu-id="93299-1077">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1077">Description</span></span>                   |
|----------|-------------------------------|
| <span data-ttu-id="93299-1078">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-1078">Name</span></span>     | <span data-ttu-id="93299-1079">データ セットの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1079">Set the name of the data set.</span></span> |

### <a name="data-sources-properties"></a><span data-ttu-id="93299-1080">データ ソース プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1080">Data Sources properties</span></span>

<span data-ttu-id="93299-1081">次のテーブルでは、**データ ソース** ノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1081">The following table describes the properties for the **Data Sources** node of the data set.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1082">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1082">Property</span></span></th>
<th><span data-ttu-id="93299-1083">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1083">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1084">ChangeGroupMode</span><span class="sxs-lookup"><span data-stu-id="93299-1084">ChangeGroupMode</span></span></td>
<td><span data-ttu-id="93299-1085">データ ソースへの変更をコミットする方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1085">Specify how changes to the data sources are committed.</span></span> <span data-ttu-id="93299-1086"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1086">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1087"><strong>なし </strong>- データ セットに対するデータ ソースの変更は、他のデータ ソースの変更とは独立して行われます。</span><span class="sxs-lookup"><span data-stu-id="93299-1087"><strong>None </strong>– The changes to any data source for the data set are committed independently of changes to the other data sources.</span></span></li>
<li><span data-ttu-id="93299-1088"><strong>ImplicitInnerOuter</strong> - 内部結合または外部結合のすべてのデータ ソースが 1 つの単位として機能します。</span><span class="sxs-lookup"><span data-stu-id="93299-1088"><strong>ImplicitInnerOuter </strong>– All the data sources that are inner-joined or outer-joined work as a single unit.</span></span> <span data-ttu-id="93299-1089">すべての変更が正常に確定した場合、またはエラーが発生した場合にはこれらはロールバックします。</span><span class="sxs-lookup"><span data-stu-id="93299-1089">All changes are committed successfully, or they are rolled back if an error occurs.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="data-set-data-source-properties"></a><span data-ttu-id="93299-1090">データ セットのデータ ソース プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1090">Data set data source properties</span></span>
<span data-ttu-id="93299-1091">次のテーブルでは、データ セット データ ソースで使用可能なプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1091">The following table describes the properties that are available for data set data sources.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1092">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1092">Property</span></span></th>
<th><span data-ttu-id="93299-1093">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1093">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1094">AllowCheck</span><span class="sxs-lookup"><span data-stu-id="93299-1094">AllowCheck</span></span></td>
<td><span data-ttu-id="93299-1095">データ セットにアクセスする前にセキュリティ チェックを行うかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1095">Specify whether security checks occur before the data set is accessed.</span></span> <span data-ttu-id="93299-1096"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1096">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1097"><strong>はい </strong>- ユーザーの読み取りアクセス許可は、データ セットにアクセスする前に検証されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1097"><strong>Yes </strong>– The user&#39;s read permissions are verified before the data set is accessed.</span></span></li>
<li><span data-ttu-id="93299-1098"><strong>いいえ </strong>- ユーザーの読み取りアクセス許可は、データ セットにアクセスした後でのみが検証されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1098"><strong>No </strong>– The user&#39;s read permissions are verified only after the data set is accessed.</span></span> <span data-ttu-id="93299-1099">ユーザーが基になるデータ ソースに対して十分なアクセス許可を持っていない場合は、データは取得されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1099">No data is retrieved if the user lacks sufficient permission for the underlying data sources.</span></span></li>
</ul><span data-ttu-id="93299-1100">
<strong>はい</strong> が既定値で、通常お勧めします。</span><span class="sxs-lookup"><span data-stu-id="93299-1100">
<strong>Yes</strong> is the default value and is usually recommended.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1101">AllowCreate</span><span class="sxs-lookup"><span data-stu-id="93299-1101">AllowCreate</span></span></td>
<td><span data-ttu-id="93299-1102">ユーザーがデータ ソース内に (つまり、データ ソースのテーブルに) 新しいレコードを作成できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1102">Specify whether users can create new records in the data source (that is, in the table for the data source).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1103">AllowDelete</span><span class="sxs-lookup"><span data-stu-id="93299-1103">AllowDelete</span></span></td>
<td><span data-ttu-id="93299-1104">ユーザーがデータ ソース内の (つまり、データ ソースのテーブルの) レコードを削除できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1104">Specify whether users can delete records in the data source (that is, in the table for the data source).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1105">AllowEdit</span><span class="sxs-lookup"><span data-stu-id="93299-1105">AllowEdit</span></span></td>
<td><span data-ttu-id="93299-1106">ユーザーはデータを変更できかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1106">Specify whether users can modify the data.</span></span> <span data-ttu-id="93299-1107"><strong>ヒント:</strong> ここでは、データ ソース全体の <strong>AllowEdit</strong> プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1107"><strong>Tip:</strong> You can set the <strong>AllowEdit</strong> property for the whole data source here.</span></span> <span data-ttu-id="93299-1108">データ ソースの各フィールドにも同じプロパティが存在するため、個々のフィールドの変更を禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1108">The same property also exists on each field in the data source, so that you can prohibit modifications for individual fields.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1109">AutoNotify</span><span class="sxs-lookup"><span data-stu-id="93299-1109">AutoNotify</span></span></td>
<td><span data-ttu-id="93299-1110">このプロパティは、データ セットには使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1110">This property isn&#39;t used for data sets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1111">AutoQuery</span><span class="sxs-lookup"><span data-stu-id="93299-1111">AutoQuery</span></span></td>
<td><span data-ttu-id="93299-1112">このプロパティは、データ セットには使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1112">This property isn&#39;t used for data sets.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1113">AutoSearch</span><span class="sxs-lookup"><span data-stu-id="93299-1113">AutoSearch</span></span></td>
<td><span data-ttu-id="93299-1114">このプロパティは、データ セットには使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1114">This property isn&#39;t used for data sets.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1115">CounterField</span><span class="sxs-lookup"><span data-stu-id="93299-1115">CounterField</span></span></td>
<td><span data-ttu-id="93299-1116">データ ソース内のフィールドのいずれかをデータ セットのカウンターとして指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1116">Specify one of the fields in the data source as a counter for the data set.</span></span> <span data-ttu-id="93299-1117">フィールドは、データ ソースの基になるテーブルのインデックスでなければならず、<strong>real</strong> 型である必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1117">The field must be an index on the underlying table for the data source, and it must be of the <strong>real</strong> type.</span></span> <span data-ttu-id="93299-1118">このプロパティは、データセットに挿入されるレコードに、データの実際の連続する位置に対応する行番号があることを保証します。</span><span class="sxs-lookup"><span data-stu-id="93299-1118">This property helps guarantee that a record that is inserted in a data set has a line number that corresponds to the actual sequential position in the data.</span></span> <span data-ttu-id="93299-1119">たとえば、新しい明細行が行の 3 と 4 の間で挿入されると、新しい明細行の行番号は 3.5 になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1119">For example, if a new line is inserted between lines 3 and 4, the new line becomes line number 3.5.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1120">CrossCompanyAutoQuery</span><span class="sxs-lookup"><span data-stu-id="93299-1120">CrossCompanyAutoQuery</span></span></td>
<td><span data-ttu-id="93299-1121">データ ソースが複数の会社のデータベースからデータを取得するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1121">Specify whether the data source retrieves data from more than one company database.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1122">DelayActive</span><span class="sxs-lookup"><span data-stu-id="93299-1122">DelayActive</span></span></td>
<td><span data-ttu-id="93299-1123">データ ソースに対するアクティブ メソッドの実行を遅延させるには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1123">Use this property to delay execution of the active method for the data source.</span></span> <span data-ttu-id="93299-1124">このプロパティを<strong>はい</strong>に設定すると、有効なメソッドは 20 ミリ秒の遅延が発生した後にのみ有効になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1124">If you set this property to <strong>Yes</strong>, the active method is activated only after a delay of 20 milliseconds.</span></span> <span data-ttu-id="93299-1125">ユーザーがデータ ソースをスクロールするとき、各レコードに対して、有効なメソッドは呼ばれません。</span><span class="sxs-lookup"><span data-stu-id="93299-1125">When a user scrolls through a data source, the active method isn&#39;t called on every record.</span></span> <span data-ttu-id="93299-1126">代わりに。</span><span class="sxs-lookup"><span data-stu-id="93299-1126">Instead.</span></span> <span data-ttu-id="93299-1127">ユーザーが選択する最後のレコードに対してのみ呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1127">it&#39;s called only on the final record that the user selects.</span></span> <span data-ttu-id="93299-1128"><strong>ヒント:</strong><strong>DelayActive</strong> プロパティは、2 つのデータ ソースがリンクされている場合 (つまり <strong>LinkType</strong> プロパティが<strong>遅延</strong>に設定されている場合) に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="93299-1128"><strong>Tip:</strong> The <strong>DelayActive </strong>property is particularly useful when two data sources are linked (that is, when the <strong>LinkType</strong> property is set to <strong>Delayed</strong>).</span></span> <span data-ttu-id="93299-1129">このプロパティは、AutoJoin システムの一部です。 </span><span class="sxs-lookup"><span data-stu-id="93299-1129">This property is part of the AutoJoin system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1130">指数</span><span class="sxs-lookup"><span data-stu-id="93299-1130">Index</span></span></td>
<td><span data-ttu-id="93299-1131">並べ替え順序を指定するために使用するインデックスを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1131">Set the index that is used to specify a sorting order.</span></span> <span data-ttu-id="93299-1132">テーブル上で任意のインデックスを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1132">You can choose any of the indexes on the table.</span></span> <span data-ttu-id="93299-1133">この方法でインデックスを指定する場合、そのインデックスは、データベースへの各クエリでインデックス ヒントとして使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1133">If you specify an index in this manner, it&#39;s used as an index hint on each query to the database.</span></span> <span data-ttu-id="93299-1134">インデックスは、このデータ ソースに基づいて、データ セット内のレコードのアクセス パスとソート順の両方を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1134">The index specifies both an access path and a sort order for the records in the data set, based on this data source.</span></span> <span data-ttu-id="93299-1135">レコードの最初のソート順は、次のようにして優先順位付けされます。</span><span class="sxs-lookup"><span data-stu-id="93299-1135">The initial sort order for the records is prioritized in this manner:</span></span>
<ol>
<li><span data-ttu-id="93299-1136">データ ソース クエリには、フィールドの並べ替えを追加する場合は、並べ替えの指定が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1136">If sort fields are added to the data source query, the sort specification is used.</span></span></li>
<li><span data-ttu-id="93299-1137">インデックスがデータ ソースの<strong>インデックス</strong> プロパティで指定されている場合は、インデックスで暗黙的に指定された並べ替え順序を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1137">If an index is specified in the <strong>Index</strong> property on the data source, the sort order that is implicitly specified in that index is used.</span></span></li>
<li><span data-ttu-id="93299-1138">データ ソースが別のデータ ソースと自動結合されている場合は、システムはこの結合における最も適切なインデックスを検索し、そのインデックスに従ってデータを並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="93299-1138">If the data source is autojoined with another data source, the system finds the most appropriate index for this join and then sorts the data according to that index.</span></span></li>
<li><span data-ttu-id="93299-1139">何も指定されていない場合は、ページのデータ ソースで使用されるテーブルの最初のインデックス (最下位の ID を持つインデックス) で暗黙的に指定されている並べ替え順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1139">If nothing else is specified, the sort order that is implicitly specified in the first index (the index that has the lowest ID) on the table that is used in the page data source is used.</span></span></li>
</ol>
<span data-ttu-id="93299-1140">インデックス ヒントが指定されていないとき、データベース管理システムは適切なアクセス パスを特定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1140">When no index hints are specified, the database management system locates an applicable access path.</span></span> <span data-ttu-id="93299-1141">このアクセス パスは、提供されるクエリの情報に基づきます。</span><span class="sxs-lookup"><span data-stu-id="93299-1141">This access path is based on the information in the query that is supplied.</span></span> <span data-ttu-id="93299-1142">ユーザーは、クエリ ダイアログ ボックスを使用してページの並べ替え順序を変更できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1142">The user can change the sort order for a page by using the query dialog box.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1143">InsertAtEnd</span><span class="sxs-lookup"><span data-stu-id="93299-1143">InsertAtEnd</span></span></td>
<td><span data-ttu-id="93299-1144">ユーザーがテーブルに最後のレコードを過ぎてフォーカスを移動したときに、新しいレコードを作成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1144">Specify whether a new record is created when the user moves focus past the last record in the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1145">InsertIfEmpty</span><span class="sxs-lookup"><span data-stu-id="93299-1145">InsertIfEmpty</span></span></td>
<td><span data-ttu-id="93299-1146">テーブルにレコードが存在しない場合、空白のレコードを挿入するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1146">Specify whether a blank record is inserted if there are no records in the table.</span></span> <span data-ttu-id="93299-1147">このプロパティを<strong>いいえ</strong>に設定すると、新しいレコードを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1147">If you set this property to <strong>No</strong>, you must manually create a new record.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1148">JoinSource</span><span class="sxs-lookup"><span data-stu-id="93299-1148">JoinSource</span></span></td>
<td><span data-ttu-id="93299-1149">2 つのデータ ソースを結合するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1149">Use this property to join two data sources.</span></span> <span data-ttu-id="93299-1150">2 つ以上のテーブルがデータ ソースとして使用され、それらを結合する場合にこのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1150">Set this property when two or more tables are used as the data source, and you want to join them.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1151">LinkType</span><span class="sxs-lookup"><span data-stu-id="93299-1151">LinkType</span></span></td>
<td><span data-ttu-id="93299-1152">2 つのデータ ソース間でアクティブなリンクを管理するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1152">Use this property to maintain an active link between two data sources.</span></span> <span data-ttu-id="93299-1153">最初のデータ ソースでフォーカスが変更されると、2 番目のデータ ソース内の対応する 1 つまたは複数のレコードが選択されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1153">When focus changes in the first data source, the corresponding record or records in the second data source are selected.</span></span> <span data-ttu-id="93299-1154">たとえば、顧客テーブルおよびトランザクションのテーブルが、各顧客に対して使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1154">For example, a customer table and a table of transactions is used for each customer.</span></span> <span data-ttu-id="93299-1155">ユーザーがある顧客から次の顧客にスクロールするとき、トランザクションの一覧が自動的に更新されて、現在の顧客のトランザクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1155">When the user scroll from one customer to the next, the transaction list is automatically updated to show transactions for the current customer.</span></span> <span data-ttu-id="93299-1156">外部 (外部にリンクされた) データ ソースのこのプロパティを <strong>遅延</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1156">Set this property to <strong>Delayed</strong> for the outer (externally linked) data source.</span></span> <span data-ttu-id="93299-1157">リンクされたデータ ソースは、100 ミリ秒の遅延後にのみ更新されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1157">The linked data source is updated only after a delay of 100 milliseconds.</span></span> <span data-ttu-id="93299-1158">この遅延は、ユーザーがデータ ソースをスクロールしている間に、リンクされたデータ ソースが更新されないようにするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93299-1158">This delay helps guarantee that the linked data source isn&#39;t updated while the user is scrolling through a data source.</span></span> <span data-ttu-id="93299-1159">更新は、ユーザーが最終的にレコードにフォーカスした後にのみ発生します。</span><span class="sxs-lookup"><span data-stu-id="93299-1159">The update occurs only after the user finally focuses on a record.</span></span> <span data-ttu-id="93299-1160">このプロパティは、AutoJoin システムの一部です。 </span><span class="sxs-lookup"><span data-stu-id="93299-1160">This property is part of the AutoJoin system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1161">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-1161">Name</span></span></td>
<td><span data-ttu-id="93299-1162">データ ソースの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1162">Set the name of the data source.</span></span> <span data-ttu-id="93299-1163">この名前は基になるテーブルの名前と同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1163">This name should be the same as the name of the underlying table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1164">OnlyFetchActive</span><span class="sxs-lookup"><span data-stu-id="93299-1164">OnlyFetchActive</span></span></td>
<td><span data-ttu-id="93299-1165">データ ソース内のすべてのフィールドをフェッチするか、データ セットにより使用されるフィールドのみをフェッチするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1165">Specify whether to fetch all fields in the data source or only those fields that are used by the data set.</span></span> <span data-ttu-id="93299-1166">このプロパティを <strong>はい</strong> に設定すると、データ セットからレコードを削除できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1166">When this property is set to <strong>Yes</strong>, records can&#39;t be deleted from the data set.</span></span> <span data-ttu-id="93299-1167">この制限は、不完全なレコードに対して削除操作が行われないことを保証するために、データの整合性を維持するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93299-1167">This restriction helps preserve data integrity, because it helps guarantee that a delete operation is never tried on incomplete records.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1168">OptionalRecordMode</span><span class="sxs-lookup"><span data-stu-id="93299-1168">OptionalRecordMode</span></span></td>
<td><span data-ttu-id="93299-1169">外部結合テーブルでレコードの作成または削除動作を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1169">Specify the create and delete behavior for records on an outer-joined table.</span></span> <span data-ttu-id="93299-1170"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1170">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1171"><strong>ImplicitCreate</strong> - データベースにレコードが保存されていない場合は、親レコードがアクティブになるとすぐに外部結合レコードと結合テーブルを作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-1171"><strong>ImplicitCreate</strong> – When no record is saved in the database, create an outer-joined record and joined tables as soon as the parent record becomes active.</span></span> <span data-ttu-id="93299-1172">外部結合レコードまたは子レコードが変更されていない場合、親レコードがアクティブでなくなったときに削除されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1172">If the outer-joined record or its children aren&#39;t changed, they will be deleted when the parent record is no longer active.</span></span></li>
<li><span data-ttu-id="93299-1173"><strong>ExplicitCreate</strong> - データベースにレコードが保存されていない場合は、<strong>オプションのレコード</strong>チェックボックスを使用してユーザーが明示的に作成をトリガーするまで、このレコードを無効として扱います。</span><span class="sxs-lookup"><span data-stu-id="93299-1173"><strong>ExplicitCreate</strong> – When no record is saved in the database, treat this record as disabled until the user explicitly triggers creation by using the <strong>Optional Record</strong> check box.</span></span> <span data-ttu-id="93299-1174">このレコードが存在するときは、このチェック ボックスをオフにすると、このレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1174">When the record exists, clearing the check box will delete this record.</span></span></li>
<li><span data-ttu-id="93299-1175"><strong>なし</strong> - 外部結合レコードに対しては、特別な作成または削除の動作は発生しません。</span><span class="sxs-lookup"><span data-stu-id="93299-1175"><strong>None</strong> – No special create or delete behavior occurs for an outer-joined record.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1176">StartPosition</span><span class="sxs-lookup"><span data-stu-id="93299-1176">StartPosition</span></span></td>
<td><span data-ttu-id="93299-1177">のデータ セットにアクセスするときに最初のレコードと最後のレコードのどちらを現在のレコードにするかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1177">Specify whether the first record or the last record should be the current record when the data set is accessed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1178">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-1178">Table</span></span></td>
<td><span data-ttu-id="93299-1179">データ ソースとして使用されるテーブルを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1179">Set the table that is used as the data source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1180">ValidTimeStateAutoQuery</span><span class="sxs-lookup"><span data-stu-id="93299-1180">ValidTimeStateAutoQuery</span></span></td>
<td><span data-ttu-id="93299-1181">日付の有効性のクエリの種類を指定します (<strong>AsOfDate</strong> または <strong>DateRange</strong>)。</span><span class="sxs-lookup"><span data-stu-id="93299-1181">Specify the types of queries for date effectivity (<strong>AsOfDate</strong> or <strong>DateRange</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1182">ValidTimeStateUpdate</span><span class="sxs-lookup"><span data-stu-id="93299-1182">ValidTimeStateUpdate</span></span></td>
<td><span data-ttu-id="93299-1183">既存の日付の有効なレコードの更新の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1183">Specify the types of updates for an existing date-effective record.</span></span> <span data-ttu-id="93299-1184"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1184">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1185"><strong>CreateNewTimePeriod</strong> - 前のレコードになっているレコードでは、<strong>ValidTo</strong> 日付フィールドは、現在の日付よりも遅くない日付に設定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1185"><strong>CreateNewTimePeriod </strong>– On the record that is becoming the previous record, the <strong>ValidTo</strong> date field is set to a date that is no later than the current date.</span></span> <span data-ttu-id="93299-1186">同じトランザクションでは、新しい現在のレコードが <strong>ValidFrom</strong> フィールドを、前のレコードの <strong>ValidTo</strong> の日付の直後に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1186">In the same transaction, the new current record has its <strong>ValidFrom</strong> field set to immediately after <strong>ValidTo</strong> date of the previous record.</span></span></li>
<li><span data-ttu-id="93299-1187"><strong>修正</strong> - 既存の行の <strong>ValidFrom</strong> または <strong>ValidTo</strong> の値は、レコード セットが更新された後に日付有効データの有効期間を保持するように変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1187"><strong>Correction </strong>– The <strong>ValidFrom</strong> or <strong>ValidTo</strong> value of existing rows must be modified to keep the date-effective data valid after the record set is updated.</span></span></li>
<li><span data-ttu-id="93299-1188"><strong>EffectiveBased</strong> - 過去のレコードは編集できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1188"><strong>EffectiveBased </strong>– Records in the past can&#39;t be edited.</span></span> <span data-ttu-id="93299-1189">現在アクティブなレコードは、CreateNewTimePeriod モードに似た方法で編集されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1189">Records that are currently active are edited in a manner that resembles CreateNewTimePeriod mode.</span></span> <span data-ttu-id="93299-1190">修正モードと似た方法で、将来のレコードが編集されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1190">Future records are edited in a manner that resembles Correction mode.</span></span></li>
</ul>
<span data-ttu-id="93299-1191">既定値は <strong>CreateNewTimePeriod</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1191">The default value is <strong>CreateNewTimePeriod</strong>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="form-properties"></a><span data-ttu-id="93299-1192">フォーム プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1192">Form properties</span></span>
<span data-ttu-id="93299-1193">このセクションでは、アプリケーション エクスプローラーでフォームに設定するプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1193">This section describes the properties that you set on forms in Application Explorer.</span></span> <span data-ttu-id="93299-1194">一貫したアプリケーション インターフェイスを提供するために、多くのプロパティは**自動**値を持っています。</span><span class="sxs-lookup"><span data-stu-id="93299-1194">To provide a uniform application interface, many properties have **Auto** values.</span></span> <span data-ttu-id="93299-1195">ドラッグ アンド ドロップ操作を使用してから複数のプロパティを手動で設定することにより、フォームを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1195">You can create forms by using a drag-and-drop operation and then manually setting several properties.</span></span> <span data-ttu-id="93299-1196">フォームの名前を指定するには、フォームの **プロパティ** ウィンドウで **名前** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1196">To specify the name of a form, you set the **Name** property in the **Properties** window for the form.</span></span> <span data-ttu-id="93299-1197">フォーム最上位ノードのその他すべてのプロパティはシステム プロパティおよび読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-1197">All other properties on the top-level node for the form are system properties and are read-only.</span></span>

## <a name="form-design-properties"></a><span data-ttu-id="93299-1198">フォーム デザイン プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1198">Form design properties</span></span>
<span data-ttu-id="93299-1199">フォームの**デザイン** ノードにあるほとんどのプロパティは、個々のコントロールにも存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1199">Most properties on the **Design** node for a form also exist on the individual controls.</span></span> <span data-ttu-id="93299-1200">例には、**幅**および**高さ**プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1200">Examples include the **Width** and **Height** properties.</span></span> <span data-ttu-id="93299-1201">ただし、コントロールでプロパティを設定するのではなく、**デザイン** ノードでプロパティを設定する場合、フォーム全体に影響が生じます。</span><span class="sxs-lookup"><span data-stu-id="93299-1201">However, when you set a property on the **Design** node instead of setting it on a control, the setting affects the whole form.</span></span> <span data-ttu-id="93299-1202">いくつかのプロパティは、**デザイン**ノードにのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1202">A few properties exist only on the **Design** node.</span></span> <span data-ttu-id="93299-1203">次のテーブルにこれらのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-1203">The following table describes these properties.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1204">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1204">Property</span></span></th>
<th><span data-ttu-id="93299-1205">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1205">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1206">AlignChild</span><span class="sxs-lookup"><span data-stu-id="93299-1206">AlignChild</span></span></td>
<td><span data-ttu-id="93299-1207">グループ内のコントロールが、グループまたはフォーム デザイン全体の <strong>AlignChildren</strong> プロパティ設定に従っているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1207">Specify whether a control within a group follows the <strong>AlignChildren</strong> property setting for the group or for the overall form design.</span></span> <span data-ttu-id="93299-1208">たとえば、フォームの<strong>デザイン</strong>ノードで <strong>AlignChildren</strong> を<strong>はい</strong>に設定しても、特定のグループがその他のグループと共に配置されないようにします。</span><span class="sxs-lookup"><span data-stu-id="93299-1208">For example, <strong>AlignChildren</strong> is set to <strong>Yes</strong> on the <strong>Design</strong> node for the form, but you don&#39;t want a particular group to be arranged together with the other groups.</span></span> <span data-ttu-id="93299-1209">この場合、そのグループに対して <strong>AlignChild</strong> を<strong>いいえ</strong>に設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1209">In this case, set <strong>AlignChild</strong> to <strong>No</strong> for that group.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1210">AlignChildren</span><span class="sxs-lookup"><span data-stu-id="93299-1210">AlignChildren</span></span></td>
<td><span data-ttu-id="93299-1211">コンテナー内の子コントロールを配置します。</span><span class="sxs-lookup"><span data-stu-id="93299-1211">Align the child controls within a container.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1212">AllowDocking</span><span class="sxs-lookup"><span data-stu-id="93299-1212">AllowDocking</span></span></td>
<td><span data-ttu-id="93299-1213">クライアント ワークスペースにフォームを関連付けることができるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1213">Specify whether a form can be attached to the client workspace.</span></span> <span data-ttu-id="93299-1214">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1214">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1215">AllowFormCompanyChange</span><span class="sxs-lookup"><span data-stu-id="93299-1215">AllowFormCompanyChange</span></span></td>
<td><span data-ttu-id="93299-1216">フォームが会社間動的リンク ライブラリ (DLL) で子フォームとして使用される場合に会社の変更をサポートするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1216">Specify whether the form supports company changes when it&#39;s used as a child form with a cross-company dynamic-link library (DLL).</span></span> <span data-ttu-id="93299-1217">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1217">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1218">AllowUserSetUp</span><span class="sxs-lookup"><span data-stu-id="93299-1218">AllowUserSetUp</span></span></td>
<td><span data-ttu-id="93299-1219">ユーザーがフォーム上のコントロールを移動できるかどうかと、コントロール プロパティの値を変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1219">Specify whether a user can move controls on a form and can change the value of control properties.</span></span> <span data-ttu-id="93299-1220">このプロパティは、フォームのデザインにもあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1220">This property is also found on the design of a form.</span></span> <span data-ttu-id="93299-1221"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1221">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1222"><strong>いいえ </strong>- ユーザーはこのコンテナー内のコントロールをカスタマイズできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1222"><strong>No </strong>– Users can&#39;t customize any controls in this container.</span></span></li>
<li><span data-ttu-id="93299-1223"><strong>制限 </strong>- ユーザーは個々のコントロールのプロパティを変更できますが、コントロールを移動することはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1223"><strong>Restricted </strong>– Users can change properties of individual controls, but they can&#39;t move controls.</span></span></li>
<li><span data-ttu-id="93299-1224"><strong>はい </strong>- ユーザーの設定に制限はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-1224"><strong>Yes </strong>– There are no restrictions on the user setup.</span></span></li>
</ul>
<span data-ttu-id="93299-1225">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1225">The default value is <strong>Yes</strong>.</span></span> <span data-ttu-id="93299-1226"><strong>注意:</strong> コントロールの親コンテナのいずれかにユーザー設定レベルの制限がある場合、完全なユーザー設定は許可されません。</span><span class="sxs-lookup"><span data-stu-id="93299-1226"><strong>Caution:</strong> Full user setup isn&#39;t allowed if any of the parent containers for the control have restrictions on the user setup level.</span></span> <span data-ttu-id="93299-1227">フォーム データ ソースの <strong>AllowAdd</strong> プロパティにより、ユーザーがフォームにフィールドを追加できるかどうかが決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1227">The <strong>AllowAdd</strong> property on form data sources determines whether a user can add a field to a form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1228">AlwaysOnTop</span><span class="sxs-lookup"><span data-stu-id="93299-1228">AlwaysOnTop</span></span></td>
<td><span data-ttu-id="93299-1229">フォームが常に他のウィンドウの上に Z オーダーで表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1229">Specify whether the form always appears on top of other windows in the z-order.</span></span> <span data-ttu-id="93299-1230">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1230">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1231">ArrangeMethod</span><span class="sxs-lookup"><span data-stu-id="93299-1231">ArrangeMethod</span></span></td>
<td><span data-ttu-id="93299-1232">行または列に子フィールド グループを配置するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1232">Specify whether to arrange child field groups in columns or in rows.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1233">ArrangeWhen</span><span class="sxs-lookup"><span data-stu-id="93299-1233">ArrangeWhen</span></span></td>
<td><span data-ttu-id="93299-1234">コンテナーのコントロールを配置するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1234">Specify when the controls in the container should be arranged.</span></span> <span data-ttu-id="93299-1235"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1235">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1236">スタートアップ</span><span class="sxs-lookup"><span data-stu-id="93299-1236">Startup</span></span></li>
<li><span data-ttu-id="93299-1237">オンデマンド</span><span class="sxs-lookup"><span data-stu-id="93299-1237">On demand</span></span></li>
<li><span data-ttu-id="93299-1238">許可しない</span><span class="sxs-lookup"><span data-stu-id="93299-1238">Never</span></span></li>
<li><span data-ttu-id="93299-1239">既定</span><span class="sxs-lookup"><span data-stu-id="93299-1239">Default</span></span></li>
<li><span data-ttu-id="93299-1240">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1240">Auto</span></span></li>
</ul>
<span data-ttu-id="93299-1241">既定値は <strong>スタートアップ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1241">The default value is <strong>Startup</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1242">BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="93299-1242">BackgroundColor</span></span></td>
<td><span data-ttu-id="93299-1243">コントロールの背景に使用される色を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1243">Specify the color that is used for the background of the control.</span></span> <span data-ttu-id="93299-1244">背景を不透明または透明にするには、<strong>BackStyle</strong> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1244">To make the background opaque or transparent, use the <strong>BackStyle</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1245">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1245">BottomMargin</span></span></td>
<td><span data-ttu-id="93299-1246">ピクセル単位でフォームの下部余白を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1246">Set the bottom margin of the form in pixels.</span></span> <span data-ttu-id="93299-1247">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1247">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1248">キャプション</span><span class="sxs-lookup"><span data-stu-id="93299-1248">Caption</span></span></td>
<td><span data-ttu-id="93299-1249">グループ化されたコントロールの見出しを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1249">Specify the heading for grouped controls.</span></span> <span data-ttu-id="93299-1250">このプロパティのラベルを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1250">Use a label for this property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1251">ColorScheme</span><span class="sxs-lookup"><span data-stu-id="93299-1251">ColorScheme</span></span></td>
<td><span data-ttu-id="93299-1252">コントロールのカラー パレットを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1252">Specify the color palette for the control.</span></span> <span data-ttu-id="93299-1253">フォーム全体のカラー パレットを変更するには、最大のコンテナーの <strong>ColorScheme</strong> プロパティを設定し、個々のコントロールの規定値を保持します。</span><span class="sxs-lookup"><span data-stu-id="93299-1253">To change the color palette for the whole form, set the <strong>ColorScheme</strong> property for the largest container, and keep the default values for the individual controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1254">列</span><span class="sxs-lookup"><span data-stu-id="93299-1254">Columns</span></span></td>
<td><span data-ttu-id="93299-1255">情報が表示される列数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1255">Specify the number of columns that show the information.</span></span> <span data-ttu-id="93299-1256"><strong>注意:</strong> 基になるテーブルのフィールド グループが 1 つ以上の列に分割されることはありません。</span><span class="sxs-lookup"><span data-stu-id="93299-1256"><strong>Caution:</strong> Field groups on the underlying table are never split into more than one column.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1257">ColumnSpace</span><span class="sxs-lookup"><span data-stu-id="93299-1257">ColumnSpace</span></span></td>
<td><span data-ttu-id="93299-1258">コンテナー コントロール内の列の間にスペースの金額を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1258">Set the amount of space between columns in container controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1259">DataSource</span><span class="sxs-lookup"><span data-stu-id="93299-1259">DataSource</span></span></td>
<td><span data-ttu-id="93299-1260">コントローのデータの取得元のテーブルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1260">Specify the table that data in the control comes from.</span></span> <span data-ttu-id="93299-1261">テーブル内の特定のフィールドを設定するには、<strong>DataField</strong> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1261">To set a particular field within the table, use the <strong>DataField</strong> property.</span></span> <span data-ttu-id="93299-1262">コントロールでは、別のフォームが開き、このプロパティによって指定されたコントロールのデータ ソースと 2 番目の形式で記録するその他のフォームのヘルプ保証でデータ ソースとの関係が動的に選択されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1262">If the control opens another form, relations between the data source for the control, as specified by this property, and the data source on the other form help guarantee that records in the second form are dynamically selected.</span></span> <span data-ttu-id="93299-1263">たとえば、顧客が 1 つのフォームで選択され、コントロールは顧客トランザクションを表示するフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-1263">For example, a customer is selected in one form, and the control opens a form that shows customer transactions.</span></span> <span data-ttu-id="93299-1264">この場合、2 番目のフォームには現在の顧客に適用される顧客トランザクションの範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1264">In this case, the second form shows a range of customer transactions that apply to the current customer.</span></span> <span data-ttu-id="93299-1265"><strong>注意:</strong> <strong>DataSource</strong> と <strong>DataField</strong> プロパティを設定すると、その設定は、<strong>DataMethod</strong> または <strong>ExtendedDataType</strong> プロパティの設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="93299-1265"><strong>Caution:</strong> If you set the <strong>DataSource</strong> and <strong>DataField</strong> properties, their settings override any settings for the <strong>DataMethod</strong> or <strong>ExtendedDataType</strong> properties.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1266">フォント</span><span class="sxs-lookup"><span data-stu-id="93299-1266">Font</span></span></td>
<td><span data-ttu-id="93299-1267"><strong>フォント</strong> ダイアログ ボックスを使用して、コントロールのフォント プロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1267">Change the font properties for the control by using the <strong>Font</strong> dialog box.</span></span> <span data-ttu-id="93299-1268">ダイアログ フォントを使用して、フォント、フォント スタイル、フォント サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1268">Use the dialog font to specify the font, font style, and font size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1269">フレーム</span><span class="sxs-lookup"><span data-stu-id="93299-1269">Frame</span></span></td>
<td><span data-ttu-id="93299-1270">このフォームが使用するフレーム スタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1270">Specify the frame style that the form uses.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1271">高さ</span><span class="sxs-lookup"><span data-stu-id="93299-1271">Height</span></span></td>
<td><span data-ttu-id="93299-1272">ピクセル単位でフォームまたはコントロールの高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1272">Specify the height of the form or control in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1273">HideIfEmpty</span><span class="sxs-lookup"><span data-stu-id="93299-1273">HideIfEmpty</span></span></td>
<td><span data-ttu-id="93299-1274">コンテナー コントロールが空の場合は、このプロパティを使用してコンテナー コントロールを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1274">Use this property to hide a container control if it&#39;s empty.</span></span> <span data-ttu-id="93299-1275">この場合、コントロールのサイズが 0 (ゼロ) であるため、コンテナの<strong>幅</strong>と<strong>高さ</strong>のプロパティが<strong>自動</strong>に設定されている場合、このプロパティは影響を及ぼしません。</span><span class="sxs-lookup"><span data-stu-id="93299-1275">This property has no affect if the <strong>Width</strong> and <strong>Height</strong> properties of the container are set to <strong>Auto</strong>, because the size of the control is 0 (zero) in this case.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1276">HideToolBar</span><span class="sxs-lookup"><span data-stu-id="93299-1276">HideToolBar</span></span></td>
<td><span data-ttu-id="93299-1277">ツールバーのフォーム固有ボタンを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1277">Hide form-specific buttons on the toolbar.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1278">ImageMode</span><span class="sxs-lookup"><span data-stu-id="93299-1278">ImageMode</span></span></td>
<td><span data-ttu-id="93299-1279"><strong>ImageName</strong> プロパティで指定されたビットマップがコントロールにどのように表示されるかを定義します。</span><span class="sxs-lookup"><span data-stu-id="93299-1279">Define how the bitmap that is specified by the <strong>ImageName</strong> property appears in a control.</span></span> <span data-ttu-id="93299-1280"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1280">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1281">標準</span><span class="sxs-lookup"><span data-stu-id="93299-1281">Normal</span></span></li>
<li><span data-ttu-id="93299-1282">サイズを合わせる</span><span class="sxs-lookup"><span data-stu-id="93299-1282">Size to fit</span></span></li>
<li><span data-ttu-id="93299-1283">左右に並べて表示</span><span class="sxs-lookup"><span data-stu-id="93299-1283">Side by side</span></span></li>
<li><span data-ttu-id="93299-1284">センター</span><span class="sxs-lookup"><span data-stu-id="93299-1284">Center</span></span></li>
</ul>
<span data-ttu-id="93299-1285">既定値は <strong>通常</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1285">The default value is <strong>Normal</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1286">ImageName</span><span class="sxs-lookup"><span data-stu-id="93299-1286">ImageName</span></span></td>
<td><span data-ttu-id="93299-1287">コントロールに表示されるイメージを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1287">Specify the image that is shown for a control.</span></span> <span data-ttu-id="93299-1288">.bmp ファイルのみを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1288">You can select only .bmp files.</span></span> <span data-ttu-id="93299-1289">リソース ファイルのいずれかを使用するには、<strong>ImageResource</strong> プロパティを代わりに使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1289">To use one of the resource files, use the <strong>ImageResource</strong> property instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1290">ImageResource</span><span class="sxs-lookup"><span data-stu-id="93299-1290">ImageResource</span></span></td>
<td><span data-ttu-id="93299-1291">イメージ リソース ファイルのイメージの 1 つを、コントロールのイメージとして使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1291">Use one of the images from the image resource file as the image for a control.</span></span> <span data-ttu-id="93299-1292">イメージの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1292">Specify the ID of the image.</span></span> <span data-ttu-id="93299-1293">統合リソース ファイルからイメージのみを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1293">You can select only an image from the integrated resource file.</span></span> <span data-ttu-id="93299-1294">別のファイル タイプを使用するには、<strong>ImageName</strong> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1294">To use another file type, use the <strong>ImageName</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1295">LabelFont</span><span class="sxs-lookup"><span data-stu-id="93299-1295">LabelFont</span></span></td>
<td><span data-ttu-id="93299-1296"><strong>ラベル</strong> プロパティに含まれているテキストのフォントを変更する</span><span class="sxs-lookup"><span data-stu-id="93299-1296">Change the font for the text that is supplied in the <strong>Label</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1297">左</span><span class="sxs-lookup"><span data-stu-id="93299-1297">Left</span></span></td>
<td><span data-ttu-id="93299-1298">フォームの左上隅の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1298">Change the position of the upper-left corner of the form.</span></span> <span data-ttu-id="93299-1299">事前に定義された設定がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1299">There are several predefined settings.</span></span> <span data-ttu-id="93299-1300">また、ピクセル単位で正確な位置を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1300">You can also specify an exact position in pixels.</span></span> <span data-ttu-id="93299-1301">次の事前定義済みの設定が使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1301">The following predefined settings are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1302">自動 (左)</span><span class="sxs-lookup"><span data-stu-id="93299-1302">Auto (left)</span></span></li>
<li><span data-ttu-id="93299-1303">自動 (右)</span><span class="sxs-lookup"><span data-stu-id="93299-1303">Auto (right)</span></span></li>
<li><span data-ttu-id="93299-1304">左とじ</span><span class="sxs-lookup"><span data-stu-id="93299-1304">Left edge</span></span></li>
<li><span data-ttu-id="93299-1305">右端</span><span class="sxs-lookup"><span data-stu-id="93299-1305">Right edge</span></span></li>
<li><span data-ttu-id="93299-1306">センター</span><span class="sxs-lookup"><span data-stu-id="93299-1306">Center</span></span></li>
</ul>
<span data-ttu-id="93299-1307">既定値は <strong>自動 (左)</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1307">The default value is <strong>Auto (left)</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1308">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1308">LeftMargin</span></span></td>
<td><span data-ttu-id="93299-1309">フォームの既定の左余白を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1309">Change the default left margin of the form.</span></span> <span data-ttu-id="93299-1310">利益幅はピクセル単位で指定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1310">The margin is specified in pixels.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1311">MaximizeBox</span><span class="sxs-lookup"><span data-stu-id="93299-1311">MaximizeBox</span></span></td>
<td><span data-ttu-id="93299-1312">外側のウィンドウの右上隅に最大化ボックスを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1312">Specify whether to include the maximize box in the upper-right corner of the enclosing window.</span></span> <span data-ttu-id="93299-1313">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1313">The default value is <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1314">MinimizeBox</span><span class="sxs-lookup"><span data-stu-id="93299-1314">MinimizeBox</span></span></td>
<td><span data-ttu-id="93299-1315">外側のウィンドウの右上隅に最小化ボックスを含めるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1315">Specify whether to include the minimize box in the upper-right corner of the enclosing window.</span></span> <span data-ttu-id="93299-1316">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1316">The default value is <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1317">モード</span><span class="sxs-lookup"><span data-stu-id="93299-1317">Mode</span></span></td>
<td><span data-ttu-id="93299-1318">フォームのデータ入力モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1318">Specify the data entry mode for the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1319">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1319">Model</span></span></td>
<td><span data-ttu-id="93299-1320">フォームがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1320">Specify the model that the form is in.</span></span> <span data-ttu-id="93299-1321">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1321">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1322">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1322">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1323">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1323">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1324">RightMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1324">RightMargin</span></span></td>
<td><span data-ttu-id="93299-1325">フォームの既定の右余白を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1325">Change the default right margin of the form.</span></span> <span data-ttu-id="93299-1326">利益幅はピクセル単位で指定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1326">The margin is specified in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1327">SaveSize</span><span class="sxs-lookup"><span data-stu-id="93299-1327">SaveSize</span></span></td>
<td><span data-ttu-id="93299-1328">このプロパティを <strong>はい</strong> に設定し、フォームのサイズを保存します。</span><span class="sxs-lookup"><span data-stu-id="93299-1328">Set this property to <strong>Yes</strong> to save the size of the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1329">ScrollBars</span><span class="sxs-lookup"><span data-stu-id="93299-1329">ScrollBars</span></span></td>
<td><span data-ttu-id="93299-1330">スクロール バーがフォームで有効になっているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1330">Specify whether scroll bars are enabled in the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1331">SetCompany</span><span class="sxs-lookup"><span data-stu-id="93299-1331">SetCompany</span></span></td>
<td><span data-ttu-id="93299-1332">フォームがフォーカスを受け取ったとき、システムが会社を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1332">Cause the system to change the company when the form receives focus.</span></span> <span data-ttu-id="93299-1333"><strong>注記: </strong>テーブルの <strong>SaveDataPerCompany</strong> プロパティが<strong>はい</strong>に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong>SetCompany</strong> プロパティも<strong>はい</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1333"><strong>Note:</strong> If the <strong>SaveDataPerCompany</strong> property on a table is set to <strong>Yes</strong>, the <strong>SetCompany</strong> property on a form design that uses the table as a data source must also be set to <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1334">StatusBarStyle</span><span class="sxs-lookup"><span data-stu-id="93299-1334">StatusBarStyle</span></span></td>
<td><span data-ttu-id="93299-1335">フォーム内でのステータス バーの表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1335">Specify how the status bar appears in a form.</span></span> <span data-ttu-id="93299-1336">ステータス バーを非表示にする、ヘルプ情報のみを表示する、<strong>WindowType</strong> 設定に従ってステータス バーの要素を表示する、または常にステータス バー全部を表示する、を指定するには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1336">Use this property to hide the status bar, show only Help information, show status bar elements according to the <strong>WindowType</strong> setting, or always show the full status bar.</span></span> <span data-ttu-id="93299-1337"><strong>注記:</strong> <strong>ListPage</strong>、<strong>ContentPage</strong>、または<strong>ワークスペース</strong>の WindowType 設定を持つフォームは、このプロパティを無視します。</span><span class="sxs-lookup"><span data-stu-id="93299-1337"><strong>Note:</strong> Forms that have a WindowType setting of <strong>ListPage</strong>, <strong>ContentPage</strong>, or <strong>Workspace</strong> ignore this property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1338">スタイル</span><span class="sxs-lookup"><span data-stu-id="93299-1338">Style</span></span></td>
<td><span data-ttu-id="93299-1339">フォームのスタイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1339">Specify the style of the form.</span></span> <span data-ttu-id="93299-1340">このプロパティは、フォームで使用されているフォーム設計パターンを制御します。</span><span class="sxs-lookup"><span data-stu-id="93299-1340">This property controls the form design pattern that is used for the form.</span></span> <span data-ttu-id="93299-1341"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1341">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1342">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1342">Auto</span></span></li>
<li><span data-ttu-id="93299-1343">DetailsFormMaster</span><span class="sxs-lookup"><span data-stu-id="93299-1343">DetailsFormMaster</span></span></li>
<li><span data-ttu-id="93299-1344">DetailsFormTransaction</span><span class="sxs-lookup"><span data-stu-id="93299-1344">DetailsFormTransaction</span></span></li>
<li><span data-ttu-id="93299-1345">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="93299-1345">Dialog</span></span></li>
<li><span data-ttu-id="93299-1346">DropDialog</span><span class="sxs-lookup"><span data-stu-id="93299-1346">DropDialog</span></span></li>
<li><span data-ttu-id="93299-1347">FormPart</span><span class="sxs-lookup"><span data-stu-id="93299-1347">FormPart</span></span></li>
<li><span data-ttu-id="93299-1348">ListPage</span><span class="sxs-lookup"><span data-stu-id="93299-1348">ListPage</span></span></li>
<li><span data-ttu-id="93299-1349">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="93299-1349">Lookup</span></span></li>
<li><span data-ttu-id="93299-1350">SimpleList</span><span class="sxs-lookup"><span data-stu-id="93299-1350">SimpleList</span></span></li>
<li><span data-ttu-id="93299-1351">SimpleListDetails</span><span class="sxs-lookup"><span data-stu-id="93299-1351">SimpleListDetails</span></span></li>
<li><span data-ttu-id="93299-1352">TableOfContents</span><span class="sxs-lookup"><span data-stu-id="93299-1352">TableOfContents</span></span></li>
</ul>
<span data-ttu-id="93299-1353">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1353">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1354">TitleDataSource</span><span class="sxs-lookup"><span data-stu-id="93299-1354">TitleDataSource</span></span></td>
<td><span data-ttu-id="93299-1355">フォーム キャプションで使用するデータ ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1355">Specify the data source to use in the form caption.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1356">上</span><span class="sxs-lookup"><span data-stu-id="93299-1356">Top</span></span></td>
<td><span data-ttu-id="93299-1357">フォームの上部の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1357">Change the position of the top of the form.</span></span> <span data-ttu-id="93299-1358">事前に定義された設定がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1358">There are several predefined settings.</span></span> <span data-ttu-id="93299-1359">また、ピクセル単位で正確な位置を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1359">You can also specify an exact position in pixels.</span></span> <span data-ttu-id="93299-1360">次の事前定義済みの設定が使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1360">The following predefined settings are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1361">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1361">Auto</span></span></li>
<li><span data-ttu-id="93299-1362">トップ エッジ</span><span class="sxs-lookup"><span data-stu-id="93299-1362">Top edge</span></span></li>
<li><span data-ttu-id="93299-1363">下端</span><span class="sxs-lookup"><span data-stu-id="93299-1363">Bottom edge</span></span></li>
<li><span data-ttu-id="93299-1364">センター</span><span class="sxs-lookup"><span data-stu-id="93299-1364">Center</span></span></li>
</ul>
<span data-ttu-id="93299-1365">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1365">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1366">TopMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1366">TopMargin</span></span></td>
<td><span data-ttu-id="93299-1367">ピクセル単位でフォームの上部余白を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1367">Set the top margin of the form in pixels.</span></span> <span data-ttu-id="93299-1368">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1368">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1369">UseCaptionFromMenuItem</span><span class="sxs-lookup"><span data-stu-id="93299-1369">UseCaptionFromMenuItem</span></span></td>
<td><span data-ttu-id="93299-1370">フォーム キャプションを呼び出し元のメニュー項目のラベルで置き換えるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1370">Specify whether to replace the form caption with the label from the calling menu item.</span></span> <span data-ttu-id="93299-1371">このプロパティを使用すると、フォームを開いたときにフォームのキャプションを変更できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1371">This property enables the caption of the form to be changed when the form is opened.</span></span> <span data-ttu-id="93299-1372">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1372">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1373">ViewEditMode</span><span class="sxs-lookup"><span data-stu-id="93299-1373">ViewEditMode</span></span></td>
<td><span data-ttu-id="93299-1374">フォームが読み取り専用モードで開くか、フィールドを変更することができるフォームとして開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1374">Specify whether the form opens in read-only mode or as a form that allows you to change fields.</span></span> <span data-ttu-id="93299-1375"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1375">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1376"><strong>表示 </strong>- 読み取り専用でフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-1376"><strong>View </strong>– Open the form as read-only.</span></span></li>
<li><span data-ttu-id="93299-1377"><strong>編集</strong> - 編集モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-1377"><strong>Edit </strong>– Open the form in edit mode.</span></span></li>
<li><span data-ttu-id="93299-1378"><strong>自動 </strong>- 適切なモードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-1378"><strong>Auto </strong>– Open the form in the appropriate mode.</span></span></li>
</ul>
<span data-ttu-id="93299-1379">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1379">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1380">表示</span><span class="sxs-lookup"><span data-stu-id="93299-1380">Visible</span></span></td>
<td><span data-ttu-id="93299-1381">フォームを非表示にするには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1381">Use this property to hide the form.</span></span> <span data-ttu-id="93299-1382"><strong>注意:</strong> <strong>表示</strong>プロパティを使用してアクセス制限を実施することはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1382"><strong>Caution:</strong> You can&#39;t use the <strong>Visible</strong> property to enforce access restrictions.</span></span> <span data-ttu-id="93299-1383">ユーザーは <strong>フォームの設定</strong> ダイアログ ボックスでコントロールの表示を変更できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1383">The user can change the visibility for the controls in the <strong>Form Setup</strong> dialog box.</span></span> <span data-ttu-id="93299-1384">アクセス制限を適用するには、代わりに <strong>Enabled</strong> および <strong>NeededAccessLevel</strong> プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1384">To enforce access restrictions, use the <strong>Enabled</strong> and <strong>NeededAccessLevel</strong> properties instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1385">幅</span><span class="sxs-lookup"><span data-stu-id="93299-1385">Width</span></span></td>
<td><span data-ttu-id="93299-1386">フォームの幅をピクセル単位で変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1386">Change the width of the form in pixels.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1387">WindowResize</span><span class="sxs-lookup"><span data-stu-id="93299-1387">WindowResize</span></span></td>
<td><span data-ttu-id="93299-1388">フォームのサイズを変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1388">Specify whether the form can be resized.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1389">WindowType</span><span class="sxs-lookup"><span data-stu-id="93299-1389">WindowType</span></span></td>
<td><span data-ttu-id="93299-1390">ウィンドウのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1390">Specify the type of window.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1391">WorkflowDataSource</span><span class="sxs-lookup"><span data-stu-id="93299-1391">WorkflowDataSource</span></span></td>
<td><span data-ttu-id="93299-1392">フォーム上のワークフローのルート データ ソースを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1392">Set the root data source for the workflow on a form.</span></span> <span data-ttu-id="93299-1393">指定するルート データ ソースは、ワークフロー テンプレートの <strong>Document</strong> プロパティで使用されたクエリで指定されたルート データ ソースと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1393">The root data source that you specify should be the same root data source that is specified in the query that used for the <strong>Document</strong> property on the workflow template.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1394">WorkflowEnabled</span><span class="sxs-lookup"><span data-stu-id="93299-1394">WorkflowEnabled</span></span></td>
<td><span data-ttu-id="93299-1395">このプロパティを <strong>はい</strong> に設定し、フォームでワークフロー メニュー バーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1395">Set this property to <strong>Yes</strong> to enable the workflow menu bar on the form.</span></span> <span data-ttu-id="93299-1396">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1396">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1397">WorkflowType</span><span class="sxs-lookup"><span data-stu-id="93299-1397">WorkflowType</span></span></td>
<td><span data-ttu-id="93299-1398">以下の項目および動作を決定するワークフロー タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1398">Specify the workflow type, which determines the following items and behaviors:</span></span>
<ul>
<li><span data-ttu-id="93299-1399">使用するワークフロー ドキュメント。</span><span class="sxs-lookup"><span data-stu-id="93299-1399">The workflow document to use.</span></span> <span data-ttu-id="93299-1400">ワークフロー ドキュメントは計算フィールドを公開し、ワークフローのデータ フィールドを公開するクエリを識別します。</span><span class="sxs-lookup"><span data-stu-id="93299-1400">The workflow document exposes calculated fields and identifies the query that exposes data fields for the workflow.</span></span></li>
<li><span data-ttu-id="93299-1401">ユーザーがタスクと承認を構成できるかどうか。</span><span class="sxs-lookup"><span data-stu-id="93299-1401">Whether the user can configure tasks and approvals.</span></span></li>
<li><span data-ttu-id="93299-1402">ワークフロー タイプが特定のモジュールに割り当てられているときに使用するワークフロー カテゴリ。</span><span class="sxs-lookup"><span data-stu-id="93299-1402">The workflow categories to use when a workflow type is assigned to a specific module.</span></span></li>
<li><span data-ttu-id="93299-1403">メニュー項目およびイベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="93299-1403">Menu items and event handlers.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="help-document-set-properties"></a><span data-ttu-id="93299-1404">ヘルプ ドキュメントの設定プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1404">Help document set properties</span></span>
<span data-ttu-id="93299-1405">ドキュメント セットは、ワークスペースに関連付けられているヘルプ ドキュメントのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="93299-1405">A document set is a collection of Help documentation that is associated with a workspace.</span></span> <span data-ttu-id="93299-1406">コンテンツの要素を公開するときは、メタデータを使用して、コンテンツの要素または目次をドキュメント セットに追加します。</span><span class="sxs-lookup"><span data-stu-id="93299-1406">When you publish a content element, you use metadata to add your content element or table of contents information to a document set.</span></span> <span data-ttu-id="93299-1407">ワークスペースとドキュメント セットの関係を管理するために、Application Explorer には **Help Document Sets** という名前のノードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="93299-1407">To manage the relationship between a workspace and a document set, Application Explorer includes a node that is named **Help Document Sets**.</span></span> <span data-ttu-id="93299-1408">**Help Document Sets** ノードの各ドキュメント セットには、プロパティのコレクションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1408">Each document set in the **Help Document Sets** node includes a collection of properties.</span></span> <span data-ttu-id="93299-1409">新しいドキュメント セットを追加またはドキュメント セットとワークスペース間の関係を変更する場合には、これらのプロパティを編集します。</span><span class="sxs-lookup"><span data-stu-id="93299-1409">You edit these properties when you add a new document set or change the relationship between a document set and a workspace.</span></span> <span data-ttu-id="93299-1410">**注意:** ワークスペースは、1 つのドキュメントセットにのみ関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1410">**Caution:** A workspace can be associated with only one document set.</span></span> <span data-ttu-id="93299-1411">アプリケーション エクスプローラーで新しいドキュメント セットを追加してワークスペースに関連付けられますが、置き換えられたドキュメント セットからのドキュメントを表示することができなくなります。</span><span class="sxs-lookup"><span data-stu-id="93299-1411">Although Application Explorer lets you add a new document set and associate it with a workspace, you will no longer see documentation from the document set that you replaced.</span></span> <span data-ttu-id="93299-1412">通常、ヘルプ サーバーに公開するコンテンツ要素または目次エントリのドキュメント セットとして **UserDocumentation** を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1412">Typically, you use **UserDocumentation** as the document set for any content element or table of contents entries that you publish to the Help server.</span></span> <span data-ttu-id="93299-1413">次のテーブルでは、アプリケーション エクスプローラーの **Help Document Sets** ノードにあるドキュメント セットのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1413">The following table describes the properties for a document set in the **Help Document Sets** node of Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1414">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1414">Property</span></span></th>
<th><span data-ttu-id="93299-1415">種類</span><span class="sxs-lookup"><span data-stu-id="93299-1415">Type</span></span></th>
<th><span data-ttu-id="93299-1416">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1416">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1417">DocumentSetName</span><span class="sxs-lookup"><span data-stu-id="93299-1417">DocumentSetName</span></span></td>
<td><span data-ttu-id="93299-1418">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-1418">String</span></span></td>
<td><span data-ttu-id="93299-1419">ドキュメント セットを固有に識別する名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1419">A name that uniquely identifies the document set.</span></span> <span data-ttu-id="93299-1420">名前は 40 文字に制限されており、空白を含むことはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1420">The name is limited to 40 characters and must not contain whitespace.</span></span> <span data-ttu-id="93299-1421">コンテンツ要素または目次ファイル内の <strong>DocumentSets</strong> メタデータ要素の値を設定する場合は、このプロパティの値を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1421">Use the value of this property when you set the value of the <strong>DocumentSets</strong> metadata element in a content element or table of contents file.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1422">DocumentSetDescription</span><span class="sxs-lookup"><span data-stu-id="93299-1422">DocumentSetDescription</span></span></td>
<td><span data-ttu-id="93299-1423">文字列</span><span class="sxs-lookup"><span data-stu-id="93299-1423">String</span></span></td>
<td><span data-ttu-id="93299-1424">ドキュメント セットに表示するテキストまたはラベル。</span><span class="sxs-lookup"><span data-stu-id="93299-1424">The text or label to display for the document set.</span></span> <span data-ttu-id="93299-1425">この値は、ヘルプ ビューアの <strong>オプション</strong> メニューにある <strong>Search content from</strong> 一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1425">This value appears in the <strong>Search content from</strong> list of the <strong>Options</strong> menu of the Help viewer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1426">AddToApplicationHelpMenu</span><span class="sxs-lookup"><span data-stu-id="93299-1426">AddToApplicationHelpMenu</span></span></td>
<td><span data-ttu-id="93299-1427">ブール型</span><span class="sxs-lookup"><span data-stu-id="93299-1427">Boolean</span></span></td>
<td><span data-ttu-id="93299-1428">ドキュメントがアプリケーション ワークスペースの <strong>ヘルプ</strong> メニューに表示されるように設定する場合、このプロパティを <strong>はい</strong> にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1428">Set this property to <strong>Yes</strong> if you want the document set to appear on the <strong>Help</strong> menu of the application workspace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1429">AddToDeveloperHelpMenu</span><span class="sxs-lookup"><span data-stu-id="93299-1429">AddToDeveloperHelpMenu</span></span></td>
<td><span data-ttu-id="93299-1430">ブール型</span><span class="sxs-lookup"><span data-stu-id="93299-1430">Boolean</span></span></td>
<td><span data-ttu-id="93299-1431">ドキュメントが開発者ワークスペースの <strong>ヘルプ</strong> メニューに表示されるように設定する場合、このプロパティを <strong>はい</strong> にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1431">Set this property to <strong>Yes</strong> if you want the document set to appear on the <strong>Help</strong> menu of the developer workspace.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1432">UserDocumentSet</span><span class="sxs-lookup"><span data-stu-id="93299-1432">UserDocumentSet</span></span></td>
<td><span data-ttu-id="93299-1433">ブール型</span><span class="sxs-lookup"><span data-stu-id="93299-1433">Boolean</span></span></td>
<td><span data-ttu-id="93299-1434">このプロパティを <strong>はい</strong> に設定し、アプリケーション ワークスペースにドキュメント セットを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="93299-1434">Set this property to <strong>Yes</strong> to associate the document set with the application workspace.</span></span> <span data-ttu-id="93299-1435">このプロパティを<strong>いいえ</strong>に設定すると、Microsoft がリリースしたコンテキストに応じた (F1) ヘルプを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1435">If you set this property to <strong>No</strong>, you can&#39;t view the context-sensitive (F1) Help that was published by Microsoft.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1436">DeveloperDocumentSet</span><span class="sxs-lookup"><span data-stu-id="93299-1436">DeveloperDocumentSet</span></span></td>
<td><span data-ttu-id="93299-1437">ブール型</span><span class="sxs-lookup"><span data-stu-id="93299-1437">Boolean</span></span></td>
<td><span data-ttu-id="93299-1438">このプロパティを <strong>はい</strong> に設定し、開発ワークスペースにドキュメント セットを関連付けます。</span><span class="sxs-lookup"><span data-stu-id="93299-1438">Set this property to <strong>Yes</strong> to associate the document set with the development workspace.</span></span> <span data-ttu-id="93299-1439">このプロパティを<strong>いいえ</strong>に設定すると、Microsoft がリリースしたコンテキストに応じた (F1) ヘルプを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-1439">If you set this property to <strong>No</strong>, you can&#39;t view the context-sensitive (F1) Help that was published by Microsoft.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1440">ContentLocation</span><span class="sxs-lookup"><span data-stu-id="93299-1440">ContentLocation</span></span></td>
<td><span data-ttu-id="93299-1441">列挙</span><span class="sxs-lookup"><span data-stu-id="93299-1441">Enumeration</span></span></td>
<td><span data-ttu-id="93299-1442">ドキュメントを取得する場所を指定する列挙値です。</span><span class="sxs-lookup"><span data-stu-id="93299-1442">An enumeration value that specifies where to retrieve documentation.</span></span> <span data-ttu-id="93299-1443">次のテーブルでは、列挙型について説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1443">The following table describes the enumeration.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1444">先頭値</span><span class="sxs-lookup"><span data-stu-id="93299-1444">Value</span></span></th>
<th><span data-ttu-id="93299-1445">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-1445">Label</span></span></th>
<th><span data-ttu-id="93299-1446">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1446">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1447">1</span><span class="sxs-lookup"><span data-stu-id="93299-1447">1</span></span></td>
<td><span data-ttu-id="93299-1448">ヘルプ サーバー</span><span class="sxs-lookup"><span data-stu-id="93299-1448">Help server</span></span></td>
<td><span data-ttu-id="93299-1449">ドキュメントはヘルプ サーバーに保存されています。</span><span class="sxs-lookup"><span data-stu-id="93299-1449">The documentation is stored on the Help server.</span></span> <span data-ttu-id="93299-1450">このオプションは、<strong>UserDocumentation</strong> ドキュメント セットおよびヘルプ サーバー上でファイルが公開されているドキュメント セットとともに使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1450">This option is used together with the <strong>UserDocumentation</strong> document set and any document set that files have been published for on the Help server.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1451">2</span><span class="sxs-lookup"><span data-stu-id="93299-1451">2</span></span></td>
<td><span data-ttu-id="93299-1452">World Wide Web</span><span class="sxs-lookup"><span data-stu-id="93299-1452">World Wide Web</span></span></td>
<td><span data-ttu-id="93299-1453">ドキュメントは MSDN または類似の Web サイトに保存されています。</span><span class="sxs-lookup"><span data-stu-id="93299-1453">The documentation is stored on MSDN or a similar website.</span></span> <span data-ttu-id="93299-1454">このオプションは、<strong>DeveloperDocumentation</strong> のドキュメント セットに必要です。他のドキュメント セットでは使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-1454">This option is required for the <strong>DeveloperDocumentation</strong> documentation set and should not be used with any other document set.</span></span></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

## <a name="menu-properties"></a><span data-ttu-id="93299-1455">メニューのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1455">Menu properties</span></span>
<span data-ttu-id="93299-1456">次のテーブルは、アプリケーション エクスプローラーの **メニュー** ノードのメニューで使用可能なプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-1456">The following table describes the properties that are available for menus under the **Menus** node in Application Explorer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1457">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1457">Property</span></span></th>
<th><span data-ttu-id="93299-1458">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1458">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1459">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-1459">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-1460">メニューのコンフィギュレーション キーを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1460">Set the configuration key for the menu.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1461">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-1461">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-1462">メニューが適用されるか有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1462">Specify the codes for the countries/regions where the menu is applicable or valid.</span></span> <span data-ttu-id="93299-1463">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-1463">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-1464">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1464">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-1465">クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1465">The client uses this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1466">DisabledImage</span><span class="sxs-lookup"><span data-stu-id="93299-1466">DisabledImage</span></span></td>
<td><span data-ttu-id="93299-1467">メニューが無効になっているときに使用するボタンの画像を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1467">Specify the button image that is used when the menu is disabled.</span></span> <span data-ttu-id="93299-1468">このプロパティが設定されていない場合、システムでは <strong>NormalImage</strong> プロパティの設定が使用され、画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1468">If this property isn&#39;t set, the system uses the setting of the <strong>NormalImage</strong> property to generate an image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1469">DisabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="93299-1469">DisabledImageLocation</span></span></td>
<td><span data-ttu-id="93299-1470">無効なコントロールに使用される画像の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1470">Specify the location of the image that is used for a disabled control.</span></span> <span data-ttu-id="93299-1471">ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1471">You can use images from a file, the <strong>Resources</strong> node in Application Explorer, or an embedded resource.</span></span> <span data-ttu-id="93299-1472">このプロパティに選択した値によって、<strong>DisabledImage</strong> プロパティで使用可能な値が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1472">The value that you select for this property determines the values that are available for the <strong>DisabledImage</strong> property.</span></span> <span data-ttu-id="93299-1473">プロパティが設定されていない場合、システムでは <strong>ImageLocation</strong> プロパティの設定が使用され、画像を生成します。</span><span class="sxs-lookup"><span data-stu-id="93299-1473">If the property isn&#39;t set, the system uses the setting of the <strong>ImageLocation</strong> property to generate an image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1474">ImageLocation</span><span class="sxs-lookup"><span data-stu-id="93299-1474">ImageLocation</span></span></td>
<td><span data-ttu-id="93299-1475">使用される画像の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1475">Specify the location of the image that is used.</span></span> <span data-ttu-id="93299-1476">ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1476">You can use images from a file, the <strong>Resources</strong> node in Application Explorer, or an embedded resource.</span></span> <span data-ttu-id="93299-1477">このプロパティに選択した値によって、<strong>NormalImage</strong> プロパティで使用可能な値が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1477">The value that you select for this property determines the values that are available for the <strong>NormalImage</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1478">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-1478">Label</span></span></td>
<td><span data-ttu-id="93299-1479">ユーザーに表示されるメニューの名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1479">Set the name of the menu that is shown to the user.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1480">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="93299-1480">MenuItemName</span></span></td>
<td><span data-ttu-id="93299-1481">メニューに含めるメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1481">Specify the menu item to include on the menu.</span></span> <span data-ttu-id="93299-1482">使用可能な値は、<strong>MenuItemType</strong> プロパティの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-1482">The values that are available depend on the value of the <strong>MenuItemType</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1483">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="93299-1483">MenuItemType</span></span></td>
<td><span data-ttu-id="93299-1484">メニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1484">Specify the type of the menu item.</span></span> <span data-ttu-id="93299-1485">メニュー項目には 3 つのカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1485">There are three categories of menu items:</span></span>
<ul>
<li><span data-ttu-id="93299-1486">ディスプレイ</span><span class="sxs-lookup"><span data-stu-id="93299-1486">Display</span></span></li>
<li><span data-ttu-id="93299-1487">出力</span><span class="sxs-lookup"><span data-stu-id="93299-1487">Output</span></span></li>
<li><span data-ttu-id="93299-1488">アクション</span><span class="sxs-lookup"><span data-stu-id="93299-1488">Action</span></span></li>
</ul>
<span data-ttu-id="93299-1489">このプロパティに設定する値によって、<strong>MenuItemName</strong> プロパティのリストに表示されるメニュー項目名のリストが決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1489">The value that you set for this property determines the list of menu item names that appears in the list for the <strong>MenuItemName</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1490">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1490">Model</span></span></td>
<td><span data-ttu-id="93299-1491">メニューがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1491">Specify the model that the menu is in.</span></span> <span data-ttu-id="93299-1492">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1492">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1493">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1493">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-1494">要素は、レイヤー内の 1 つのモデルに正確に配置できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1494">An element can be located in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1495">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1495">The same element can be located in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1496">NormalImage</span><span class="sxs-lookup"><span data-stu-id="93299-1496">NormalImage</span></span></td>
<td><span data-ttu-id="93299-1497">メニューが有効になっているときに使用する画像を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1497">Specify the image that is used when the menu is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93299-1498">Parameters</span></span></td>
<td><span data-ttu-id="93299-1499">オブジェクトに渡される 1 つ以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1499">Specify one or more values that are passed to an object.</span></span> <span data-ttu-id="93299-1500">これらの値は、メソッドに渡されるパラメーターに似ています。</span><span class="sxs-lookup"><span data-stu-id="93299-1500">These values resemble the parameters that are passed to a method.</span></span> <span data-ttu-id="93299-1501">パラメーターは、タスクの実行に使用される値を提供します。</span><span class="sxs-lookup"><span data-stu-id="93299-1501">A parameter supplies a value that is then used to perform the task.</span></span> <span data-ttu-id="93299-1502">既定値はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-1502">There is no default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1503">SetCompany</span><span class="sxs-lookup"><span data-stu-id="93299-1503">SetCompany</span></span></td>
<td><span data-ttu-id="93299-1504">このプロパティを<strong>はい</strong>に設定すると、メニューを開くたびに、会社は、メニューが最初に起動したときに指定された会社に変更されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1504">If you set this property to <strong>Yes</strong>, every time that the menu is opened, the company is changed to the company that was specified when the menu was first started.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1505">ショートカット</span><span class="sxs-lookup"><span data-stu-id="93299-1505">Shortcut</span></span></td>
<td><span data-ttu-id="93299-1506">メニューを開くキーボード ショートカットを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1506">Specify the keyboard shortcut that opens the menu.</span></span> <span data-ttu-id="93299-1507">たとえば、Ctrl + F3 キーを押してメニューを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1507">For example, you can press Ctrl+F3 to open the menu.</span></span> <span data-ttu-id="93299-1508">既定値はありません。</span><span class="sxs-lookup"><span data-stu-id="93299-1508">There is no default value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1509">ShowParentModule</span><span class="sxs-lookup"><span data-stu-id="93299-1509">ShowParentModule</span></span></td>
<td><span data-ttu-id="93299-1510">メニュー項目の親モジュールに基づいてナビゲーション ウィンドウを更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1510">Specify whether to update the navigation pane, based on the parent module of the menu item.</span></span> <span data-ttu-id="93299-1511"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1511">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1512"><strong>はい </strong>- メニュー項目の親モジュールに基づいてナビゲーション ウィンドウを常に更新してください。</span><span class="sxs-lookup"><span data-stu-id="93299-1512"><strong>Yes </strong>– Always update the navigation pane, based on the parent module of the menu item.</span></span></li>
<li><span data-ttu-id="93299-1513"><strong>いいえ</strong> - メニュー項目の親モジュールが、現在のモジュールと異なる場合でもナビゲーション ウィンドウを変更せずにそのままにします。</span><span class="sxs-lookup"><span data-stu-id="93299-1513"><strong>No </strong>– Leave the navigation pane unchanged, even if the parent module of the menu item differs from the current module.</span></span></li>
</ul>
<span data-ttu-id="93299-1514">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1514">The default value is <strong>Yes</strong>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="menu-item-properties"></a><span data-ttu-id="93299-1515">メニュー項目のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1515">Menu item properties</span></span>
<span data-ttu-id="93299-1516">次のプロパティは、Web メニューに使用されるメニュー項目であっても、すべてのメニュー項目 (表示、出力、およびアクション) で使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1516">The following properties are available for all menu items (display, output, and action), even menu items that are used for web menus.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1517">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1517">Property</span></span></th>
<th><span data-ttu-id="93299-1518">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1518">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1519">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-1519">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-1520">メニュー項目を有効にするために必要なコンフィギュレーション キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1520">Select the configuration key that is required in order to enable the menu item.</span></span> <span data-ttu-id="93299-1521">オブジェクトが属しているモジュールのキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1521">Use the key for the module that the object belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1522">CopyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="93299-1522">CopyCallerQuery</span></span></td>
<td><span data-ttu-id="93299-1523">ターゲット フォームへの呼び出し元のフォームからクエリをコピーするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1523">Specify whether to copy the query from the calling form to the target form.</span></span> <span data-ttu-id="93299-1524">このプロパティを使用すると、元のフォームで表示されたものと同じデータをターゲット フォームに表示できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1524">This property enables the target form to show the same data that was viewed in the original form.</span></span> <span data-ttu-id="93299-1525">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1525">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1526">CorrectPermissions</span><span class="sxs-lookup"><span data-stu-id="93299-1526">CorrectPermissions</span></span></td>
<td><span data-ttu-id="93299-1527">メニュー項目に特権が割り当てられるときに適切なアクセス許可を選択できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1527">Specify whether correct permission should be available for selection when privileges are assigned to the menu item.</span></span> <span data-ttu-id="93299-1528"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1528">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1529"><strong>自動 </strong>- アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1529"><strong>Auto </strong>– The permission will be available for selection as a privilege on this menu item&#39;s <strong>Privileges</strong> node under the <strong>Entry Points</strong> node.</span></span></li>
<li><span data-ttu-id="93299-1530"><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1530"><strong>No </strong>– The permission won&#39;t be available for selection as a privilege on the menu item.</span></span></li>
</ul>
<span data-ttu-id="93299-1531">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1531">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1532">CountryConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-1532">CountryConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-1533">オプション: 標準のコンフィギュレーション キーに加えて、または代わりに、国/地域固有のコンフィギュレーション キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1533">Optional: Set a country/region-specific key in addition to or instead of a standard configuration key.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1534">CountryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="93299-1534">CountryRegionCodes</span></span></td>
<td><span data-ttu-id="93299-1535">メニュー項目が有効な国/地域のコードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1535">Specify the codes for the countries/regions where the menu item is valid.</span></span> <span data-ttu-id="93299-1536">このプロパティは、コンマで区切られた単一の文字列の ISO コードのリストとして実装されています。</span><span class="sxs-lookup"><span data-stu-id="93299-1536">This property is implemented as a comma-separated list of ISO country codes in a single string.</span></span> <span data-ttu-id="93299-1537">値は、グローバル アドレス帳のデータと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1537">The values must match data in the global address book.</span></span> <span data-ttu-id="93299-1538">クライアントは、このプロパティを使用して、国または地域固有の機能を有効または無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-1538">The client uses this property to enable or disable country/region-specific features.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1539">CreatePermissions</span><span class="sxs-lookup"><span data-stu-id="93299-1539">CreatePermissions</span></span></td>
<td><span data-ttu-id="93299-1540">メニュー項目に特権が割り当てられるときに作成アクセス許可を選択できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1540">Specify whether create permission should be available for selection when privileges are assigned to the menu item.</span></span> <span data-ttu-id="93299-1541"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1541">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1542"><strong>自動 </strong>- アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1542"><strong>Auto </strong>– The permission will be available for selection as a privilege on this menu item&#39;s <strong>Privileges</strong> node under the <strong>Entry Points</strong> node.</span></span></li>
<li><span data-ttu-id="93299-1543"><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1543"><strong>No </strong>– The permission won&#39;t be available for selection as a privilege on the menu item.</span></span></li>
</ul>
<span data-ttu-id="93299-1544">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1544">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1545">DeletePermissions</span><span class="sxs-lookup"><span data-stu-id="93299-1545">DeletePermissions</span></span></td>
<td><span data-ttu-id="93299-1546">メニュー項目に特権が割り当てられるときに削除アクセス許可を選択できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1546">Specify whether delete permission should be available for selection when privileges are assigned to the menu item.</span></span> <span data-ttu-id="93299-1547"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1547">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1548"><strong>自動 </strong>- アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1548"><strong>Auto </strong>– The permission will be available for selection as a privilege on this menu item&#39;s <strong>Privileges</strong> node under the <strong>Entry Points</strong> node.</span></span></li>
<li><span data-ttu-id="93299-1549"><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1549"><strong>No </strong>– The permission won&#39;t be available for selection as a privilege on the menu item.</span></span></li>
</ul>
<span data-ttu-id="93299-1550">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1550">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1551">DisabledImage</span><span class="sxs-lookup"><span data-stu-id="93299-1551">DisabledImage</span></span></td>
<td><span data-ttu-id="93299-1552">メニュー項目が無効になっているときに使用する画像を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1552">Specify the image that is used when the menu item is disabled.</span></span> <span data-ttu-id="93299-1553">このプロパティが設定されていない場合、システムでは <strong>NormalImage</strong> プロパティの設定が使用され、画像が生成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1553">If this property isn&#39;t set, the system uses the setting of the <strong>NormalImage</strong> property to generate an image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1554">DisabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="93299-1554">DisabledImageLocation</span></span></td>
<td><span data-ttu-id="93299-1555">無効なコントロールに使用される画像の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1555">Specify the location of the image that is used for a disabled control.</span></span> <span data-ttu-id="93299-1556">ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1556">You can use images from a file, the <strong>Resources</strong> node in Application Explorer, or an embedded resource.</span></span> <span data-ttu-id="93299-1557">このプロパティに選択した値によって、<strong>DisabledImage</strong> プロパティで使用可能な値が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1557">The value that you select for this property determines the values that are available for the <strong>DisabledImage</strong> property.</span></span> <span data-ttu-id="93299-1558">プロパティが設定されていない場合、システムでは <strong>ImageLocation</strong> プロパティの設定が使用され、画像を生成します。</span><span class="sxs-lookup"><span data-stu-id="93299-1558">If the property isn&#39;t set, the system uses the setting of the <strong>ImageLocation</strong> property to generate an image.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1559">EnumTypeParameter および EnumParameter</span><span class="sxs-lookup"><span data-stu-id="93299-1559">EnumTypeParameter and EnumParameter</span></span></td>
<td><span data-ttu-id="93299-1560">オプション: オブジェクトのパラメーターとして列挙型を選択し、<strong>EnumParameter</strong> プロパティの値として列挙値を選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1560">Optional: Select an enumerated type as a parameter for the object, and then select an enumeration value as the value of the <strong>EnumParameter</strong> property.</span></span> <span data-ttu-id="93299-1561">通常、これらのプロパティは、1 つのフォームが複数の状況で使用されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1561">Typically, these properties are used when one form is used in several situations.</span></span> <span data-ttu-id="93299-1562"><strong>EnumParameter</strong> 値に応じて、フォームの動作を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1562">You can change the behavior of the form, depending on the <strong>EnumParameter</strong> value.</span></span> <span data-ttu-id="93299-1563">たとえば、<strong>PriceDiscGroup</strong> フォームは 3 つの表示メニュー項目 (<strong>PriceDiscGroup_ \*</strong>) により使用され、それぞれが異なる <strong>EnumParameter</strong> 値を持ちます。</span><span class="sxs-lookup"><span data-stu-id="93299-1563">For example, the <strong>PriceDiscGroup</strong> form is used by three display menu items (<strong>PriceDiscGroup_\*</strong>), each of which has a different <strong>EnumParameter</strong> value.</span></span> <span data-ttu-id="93299-1564">フォームの <strong>init</strong> メソッドでは、switch 構造が値を検証してからフォームが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1564">In the form&#39;s <strong>init</strong> method, a switch construct validates the value, and then the form is created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1565">ExtendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="93299-1565">ExtendedDataSecurity</span></span></td>
<td><span data-ttu-id="93299-1566">メニュー項目が 1 つの会社のコンテキストでなくすべての会社の下に表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1566">Specify whether the menu item appears under all companies instead of in the context of a single company.</span></span> <span data-ttu-id="93299-1567">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1567">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1568">FormViewOption</span><span class="sxs-lookup"><span data-stu-id="93299-1568">FormViewOption</span></span></td>
<td><span data-ttu-id="93299-1569">使用するフォーム モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1569">Specify the form mode to use.</span></span> <span data-ttu-id="93299-1570"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1570">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1571">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1571">Auto</span></span></li>
<li><span data-ttu-id="93299-1572">グリッド</span><span class="sxs-lookup"><span data-stu-id="93299-1572">Grid</span></span></li>
<li><span data-ttu-id="93299-1573">細目</span><span class="sxs-lookup"><span data-stu-id="93299-1573">Details</span></span></li>
</ul>
<span data-ttu-id="93299-1574">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1574">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1575">HelpText</span><span class="sxs-lookup"><span data-stu-id="93299-1575">HelpText</span></span></td>
<td><span data-ttu-id="93299-1576">メニュー項目のヘルプ文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="93299-1576">Create a Help string for the menu item.</span></span> <span data-ttu-id="93299-1577">メニュー項目で開いたオブジェクト (フォームなど) を選択すると、ステータス バーにテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1577">The text appears on the status bar when you select the object that is opened by the menu item (for example, a form).</span></span> <span data-ttu-id="93299-1578"><strong>注記:</strong> メニュー項目のヘルプ トピックを書き込むには、アプリケーション エクスプローラーの<strong>アプリケーションのドキュメント/メニュー項目</strong>ノードで、メニュー項目と同じ名前のトピックを見つけます。</span><span class="sxs-lookup"><span data-stu-id="93299-1578"><strong>Note:</strong> To write a Help topic for the menu item, in Application Explorer, in the <strong>Application Documentation/Menu Items</strong> node, find the topic that has the same name as your menu item.</span></span> <span data-ttu-id="93299-1579">このトピックは、メニュー項目によって開かれたオブジェクトについて書かれたヘルプ トピックの代わりに表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1579">This topic will then be shown instead of any Help topic that was written about the object that is opened by the menu item.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1580">ImageLocation</span><span class="sxs-lookup"><span data-stu-id="93299-1580">ImageLocation</span></span></td>
<td><span data-ttu-id="93299-1581">コントロールに使用される画像の場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1581">Specify the location of the image that is used for a control.</span></span> <span data-ttu-id="93299-1582">ファイル、アプリケーション エクスプローラー内の <strong>リソース</strong> ノード、または埋め込みリソースからのイメージを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1582">You can use images from a file, the <strong>Resources</strong> node in Application Explorer, or an embedded resource.</span></span> <span data-ttu-id="93299-1583">このプロパティに選択した値によって、<strong>NormalImage</strong> プロパティで使用可能な値が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1583">The value that you select for this property determines the values that are available for the <strong>NormalImage</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1584">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-1584">Label</span></span></td>
<td><span data-ttu-id="93299-1585">メニューやボタンの項目に対して表示される名前として使用するラベルを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1585">Select the label to use as the name that appears for the item on menus and buttons.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1586">LinkedPermissionObject</span><span class="sxs-lookup"><span data-stu-id="93299-1586">LinkedPermissionObject</span></span></td>
<td><span data-ttu-id="93299-1587">別のオブジェクト (たとえば、フォームまたはレポートなど) のアクセス許可をメニュー項目に適用する場合は、そのオブジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1587">If the permissions of another object (for example, a form or report) should be applied to this menu item, select the object.</span></span> <span data-ttu-id="93299-1588">通常、このプロパティはアクション メニュー項目に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1588">Typically, this property is used for action menu items.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1589">LinkedPermissionType</span><span class="sxs-lookup"><span data-stu-id="93299-1589">LinkedPermissionType</span></span></td>
<td><span data-ttu-id="93299-1590"><strong>LinkedPermissionObject</strong> プロパティにより指定されるオブジェクトのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1590">Specify the type of the object that is specified by the <strong>LinkedPermissionObject</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1591">MultiSelect</span><span class="sxs-lookup"><span data-stu-id="93299-1591">MultiSelect</span></span></td>
<td><span data-ttu-id="93299-1592">メニュー項目をフォームの複数レコードに使用できるかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1592">Select whether the menu item can be used on multiple record selections in forms.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1593">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1593">Model</span></span></td>
<td><span data-ttu-id="93299-1594">テーブルがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1594">Specify the model that the table is in.</span></span> <span data-ttu-id="93299-1595">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1595">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1596">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1596">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-1597">要素は、レイヤー内の 1 つのモデルに正確に配置できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1597">An element can be located in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1598">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素を配置することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1598">The same element can be located in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1599">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-1599">Name</span></span></td>
<td><span data-ttu-id="93299-1600">メニュー項目の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1600">The name of the menu item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1601">NeededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="93299-1601">NeededAccessLevel</span></span></td>
<td><span data-ttu-id="93299-1602">メニュー項目がメニューまたはボタンに表示されるのに必要な最小アクセスを定義します。</span><span class="sxs-lookup"><span data-stu-id="93299-1602">Define the minimum access that is required for the menu item to appear on a menu or a button.</span></span> <span data-ttu-id="93299-1603">このプロパティは、異なるユーザー グループのメニュー項目へのアクセスを設定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1603">This property is used to set access to the menu item for different user groups.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1604">NeedsRecord</span><span class="sxs-lookup"><span data-stu-id="93299-1604">NeedsRecord</span></span></td>
<td><span data-ttu-id="93299-1605">レコードが存在しない場合、メニュー項目を表すボタンを有効にするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1605">Specify whether a button that represents the menu item is enabled if no record is present.</span></span> <span data-ttu-id="93299-1606">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1606">The default value is <strong>No</strong>.</span></span> <span data-ttu-id="93299-1607">アクションが完了することを保証するために、このプロパティを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1607">You can use this property to help guarantee that an action can be completed.</span></span> <span data-ttu-id="93299-1608">たとえば、詳細フォームを開くメニュー項目ボタンがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1608">For example, you have a menu item button that opens a detail form.</span></span> <span data-ttu-id="93299-1609">リスト ページにレコードが存在しない場合、ボタンを無効にする場合があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1609">You might want to disable the button if there are no records on the list page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1610">NormalImage</span><span class="sxs-lookup"><span data-stu-id="93299-1610">NormalImage</span></span></td>
<td><span data-ttu-id="93299-1611">メニュー項目が有効化されたボタン コントロールに関連付けられている場合に使用される画像を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1611">Specify the image that is used when the menu item is associated with an enabled button control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1612">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="93299-1612">Object</span></span></td>
<td><span data-ttu-id="93299-1613"><strong>Class</strong> プロパティで指定されているオブジェクト タイプのオブジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1613">Select an object of the object type that is specified in the <strong>Class</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1614">ObjectType</span><span class="sxs-lookup"><span data-stu-id="93299-1614">ObjectType</span></span></td>
<td><span data-ttu-id="93299-1615">メニュー項目が開かれるオブジェクトのタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1615">Select the type of object that the menu item opens.</span></span> <span data-ttu-id="93299-1616"><strong>注意:</strong> SSRS レポートのメニュー項目に <strong>SSRSReport</strong> を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1616"><strong>Caution:</strong> You should use <strong>SSRSReport</strong> for a menu item for an SSRS report.</span></span> <span data-ttu-id="93299-1617">新しいメニュー項目の <strong>SQLReportLibraryReport</strong> を使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-1617">Don&#39;t use <strong>SQLReportLibraryReport</strong> for new menu items.</span></span> <span data-ttu-id="93299-1618"><strong>SQLReportLibraryReport</strong> オプションは使用されてないため、今後のバージョンでは削除されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1618">The <strong>SQLReportLibraryReport</strong> option is obsolete and will be removed in a future version.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1619">OpenMode</span><span class="sxs-lookup"><span data-stu-id="93299-1619">OpenMode</span></span></td>
<td><span data-ttu-id="93299-1620">ターゲット フォームの表示モードを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1620">Specify the view mode of the target form.</span></span> <span data-ttu-id="93299-1621">このプロパティを使用して、ターゲット フォームを編集モードまたは読み取り専用モードのいずれで開くかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1621">You use this property to specify whether the target form opens in edit mode or read-only mode.</span></span> <span data-ttu-id="93299-1622"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1622">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1623">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1623">Auto</span></span></li>
<li><span data-ttu-id="93299-1624">表示</span><span class="sxs-lookup"><span data-stu-id="93299-1624">View</span></span></li>
<li><span data-ttu-id="93299-1625">編集</span><span class="sxs-lookup"><span data-stu-id="93299-1625">Edit</span></span></li>
<li><span data-ttu-id="93299-1626">新規</span><span class="sxs-lookup"><span data-stu-id="93299-1626">New</span></span></li>
</ul>
<span data-ttu-id="93299-1627">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1627">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1628">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93299-1628">Parameters</span></span></td>
<td><span data-ttu-id="93299-1629">オプション: オブジェクトに渡される引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1629">Optional: Specify the arguments that are passed to the object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1630">クエリ</span><span class="sxs-lookup"><span data-stu-id="93299-1630">Query</span></span></td>
<td><span data-ttu-id="93299-1631"><strong>InitialQuery</strong> メソッドのターゲット フォームに渡されるクエリを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1631">Select the query that is passed to the target form for the <strong>InitialQuery</strong> method.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1632">ReadPermissions</span><span class="sxs-lookup"><span data-stu-id="93299-1632">ReadPermissions</span></span></td>
<td><span data-ttu-id="93299-1633">メニュー項目に特権が割り当てられるときに読み取りアクセス許可がセクションに利用可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1633">Specify whether read permission should be available for section when privileges are assigned to the menu item.</span></span> <span data-ttu-id="93299-1634"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1634">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1635"><strong>自動 </strong>- アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限として選択可能になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1635"><strong>Auto </strong>– The permission will be available for selection as a privilege on this menu item&#39;s <strong>Privileges</strong> node under the <strong>Entry Points</strong> node.</span></span></li>
<li><span data-ttu-id="93299-1636"><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限として選択できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1636"><strong>No </strong>– The permission won&#39;t be available for selection as a privilege on the menu item.</span></span></li>
</ul>
<span data-ttu-id="93299-1637">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1637">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1638">ReportDesign</span><span class="sxs-lookup"><span data-stu-id="93299-1638">ReportDesign</span></span></td>
<td><span data-ttu-id="93299-1639">特定の SSRS レポート モデルに使用するレポート デザインを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1639">Select the report design to use for a specific SSRS report model.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1640">RunOn</span><span class="sxs-lookup"><span data-stu-id="93299-1640">RunOn</span></span></td>
<td><span data-ttu-id="93299-1641">クライアント、サーバー、または呼び出し元の場所でメニュー項目を実行するかどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1641">Select whether to run the menu item on the client, the server, or the location that it&#39;s called from.</span></span> <span data-ttu-id="93299-1642">このプロパティは、主にレポートを開くメニュー項目に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1642">This property is mainly used for menu items that open reports.</span></span> <span data-ttu-id="93299-1643">このプロパティは、オブジェクトの <strong>RunOn</strong> プロパティが<strong>呼び出し元</strong>に設定されている場合にのみ、アプリケーション オブジェクトの実行場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1643">This property determines where the application object is run from only if the <strong>RunOn</strong> property of the object is set to <strong>Called from</strong>.</span></span>
<ul>
<li><span data-ttu-id="93299-1644"><strong>FormRun</strong> クラスは常にクライアント上で実行されるため、フォームはインスタンス化されてクライアント上で実行されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1644">A form is instantiated and run on the client, because the <strong>FormRun</strong> class always runs on the client.</span></span></li>
<li><span data-ttu-id="93299-1645"><strong>ReportRun</strong> クラスは常に呼び出された場所で実行されるため、レポートは、インスタンス化され、メニュー項目の <strong>RunOn</strong> プロパティで指定されたとおりに実行されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1645">A report is instantiated and run as specified by the menu item&#39;s <strong>RunOn</strong> property, because the <strong>ReportRun</strong> class always runs where it was called from.</span></span> <span data-ttu-id="93299-1646">プロパティを<strong>呼び出し元</strong>に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1646">You should set the property to <strong>Called from</strong>.</span></span> <span data-ttu-id="93299-1647">レポートをクライアントで実行するように設定すると、レポートはバッチで実行され、レポートは失敗します。</span><span class="sxs-lookup"><span data-stu-id="93299-1647">If you set the report to run on the client, and the report is run in a batch, the report will fail.</span></span> <span data-ttu-id="93299-1648">レポートをサーバーで実行するように設定すると、レポートは画面に表示され、レポートは失敗します。</span><span class="sxs-lookup"><span data-stu-id="93299-1648">If you set the report to run on the server, and the report is shown on the screen, the report will fail.</span></span></li>
<li><span data-ttu-id="93299-1649">クラスの<strong>メイン</strong>メソッドは、モディファイアーで指定されたとおりに実行されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1649">A class&#39;s <strong>main</strong> method is run as specified by its modifier.</span></span> <span data-ttu-id="93299-1650">クラス自体は、<strong>RunOn</strong> プロパティで指定されたとおりにインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1650">The class itself is instantiated as specified by its <strong>RunOn</strong> property.</span></span> <span data-ttu-id="93299-1651">インスタンス化は、<strong>main</strong> メソッドで発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1651">The instantiation might occur in the <strong>main</strong> method.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1652">UpdatePermissions</span><span class="sxs-lookup"><span data-stu-id="93299-1652">UpdatePermissions</span></span></td>
<td><span data-ttu-id="93299-1653">メニュー項目に特権が割り当てられるときに更新アクセス許可がセクションに利用可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1653">Specify whether update permission should be available for section when privileges are assigned to the menu item.</span></span> <span data-ttu-id="93299-1654"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1654">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1655"><strong>自動 </strong>– アクセス許可が、<strong>エントリ ポイント</strong> ノードの下にある、このメニュー項目の<strong>権限</strong>ノードで、権限としてセクションで利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="93299-1655"><strong>Auto </strong>– The permission will be available for section as a privilege on this menu item&#39;s <strong>Privileges</strong> node under the <strong>Entry Points</strong> node.</span></span></li>
<li><span data-ttu-id="93299-1656"><strong>いいえ</strong> - アクセス許可は、メニュー項目の権限としてセクションで使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1656"><strong>No </strong>– The permission won&#39;t be available for section as a privilege on the menu item.</span></span></li>
</ul>
<span data-ttu-id="93299-1657">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1657">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1658">Web</span><span class="sxs-lookup"><span data-stu-id="93299-1658">Web</span></span></td>
<td><span data-ttu-id="93299-1659">メニュー項目を実行するときに開かれる URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1659">Specify the URL that is opened when you run the menu item.</span></span> <span data-ttu-id="93299-1660">このプロパティ値は使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="93299-1660">The value of this property is no longer used.</span></span> <span data-ttu-id="93299-1661">プロパティを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-1661">Don&#39;t use this property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1662">WebConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-1662">WebConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-1663">オプション: 標準のコンフィギュレーション キーだけでなく、Web 固有のコンフィギュレーション キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1663">Optional: Select a web-specific configuration key in addition to a standard configuration key.</span></span> <span data-ttu-id="93299-1664">このプロパティは、Web メニュー項目にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1664">This property applies to web menu items only.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1665">WebMenuItemName</span><span class="sxs-lookup"><span data-stu-id="93299-1665">WebMenuItemName</span></span></td>
<td><span data-ttu-id="93299-1666">Web メニューに含めるメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1666">Specify the menu item to include on a web menu.</span></span> <span data-ttu-id="93299-1667">使用可能な値は、<strong>WebMenuItemType</strong> プロパティの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-1667">The available values depend on the setting of the <strong>WebMenuItemType</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1668">WebMenuItemType</span><span class="sxs-lookup"><span data-stu-id="93299-1668">WebMenuItemType</span></span></td>
<td><span data-ttu-id="93299-1669">Web メニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1669">Specify the type of the web menu item.</span></span> <span data-ttu-id="93299-1670">Web メニュー項目には 2 つのカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1670">There are two categories of web menu items:</span></span>
<ul>
<li><span data-ttu-id="93299-1671">URL</span><span class="sxs-lookup"><span data-stu-id="93299-1671">URL</span></span></li>
<li><span data-ttu-id="93299-1672">アクション</span><span class="sxs-lookup"><span data-stu-id="93299-1672">Action</span></span></li>
</ul>
<span data-ttu-id="93299-1673">選択した値によって、<strong>WebMenuItemName</strong> プロパティで使用可能な Web メニュー項目名が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-1673">The value that you select determines the web menu item names that are available for the <strong>WebMenuItemName</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1674">WebPage</span><span class="sxs-lookup"><span data-stu-id="93299-1674">WebPage</span></span></td>
<td><span data-ttu-id="93299-1675">メニュー項目にリンクされている Web ページを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1675">Specify the webpage that is linked to the menu item.</span></span> <span data-ttu-id="93299-1676">このプロパティ値は使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="93299-1676">The value of this property is no longer used.</span></span> <span data-ttu-id="93299-1677">プロパティを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="93299-1677">Don&#39;t use this property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1678">WebSecureTransaction</span><span class="sxs-lookup"><span data-stu-id="93299-1678">WebSecureTransaction</span></span></td>
<td><span data-ttu-id="93299-1679">メニュー項目にセキュリティで保護されたトランザクション (SSL) が必要かどうかを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-1679">Select whether the menu item requires secure transactions (SSL).</span></span> <span data-ttu-id="93299-1680">このプロパティは、Web メニュー項目にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1680">This property applies to web menu items only.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="93299-1681">**注記:** **パラメーター**または **EnumParameter** を使用すると、タイプの不一致などのエラーはコンパイル時ではなく、実行時にのみ検出されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1681">**Note:** When you use the **Parameters** or **EnumParameter** property, errors such as type mismatches can be found only at run time, not at compile time.</span></span>

## <a name="query-properties"></a><span data-ttu-id="93299-1682">プロパティの照会</span><span class="sxs-lookup"><span data-stu-id="93299-1682">Query properties</span></span>
<span data-ttu-id="93299-1683">クエリ内では、クエリ自体のプロパティ、データ ソース、ソートに使用するフィールド、およびクエリの制限に使用する範囲を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1683">Within a query, you can set properties on the query itself, the data sources, the fields that are used for sorting, and the ranges that are used to delimit the query.</span></span>

### <a name="query-properties"></a><span data-ttu-id="93299-1684">プロパティの照会</span><span class="sxs-lookup"><span data-stu-id="93299-1684">Query properties</span></span>

<span data-ttu-id="93299-1685">クエリのプロパティは、クエリの全体的な動作を決定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1685">Query properties determine the overall behavior of the query.</span></span> <span data-ttu-id="93299-1686">たとえば、クエリと通信できるように、ユーザーに表示されているフォームを指定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1686">For example, you can specify the form that is shown to users so that they can interact with the query.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1687">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1687">Property</span></span></th>
<th><span data-ttu-id="93299-1688">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1688">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1689">AllowCheck</span><span class="sxs-lookup"><span data-stu-id="93299-1689">AllowCheck</span></span></td>
<td><span data-ttu-id="93299-1690">このプロパティは、クエリでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1690">This property is ignored for queries.</span></span> <span data-ttu-id="93299-1691">フォームやレポートには効果的ではありません。</span><span class="sxs-lookup"><span data-stu-id="93299-1691">It&#39;s effective on forms and reports.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1692">AllowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="93299-1692">AllowCrossCompany</span></span></td>
<td><span data-ttu-id="93299-1693">ユーザーが読み取る権限を持っているすべての会社のデータが取得されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1693">Specify whether data is retrieved for all companies that the user has authority to read from.</span></span> <span data-ttu-id="93299-1694">プロパティが、既定値である <strong>false</strong> に設定されている場合、現在のセッションの会社に対してのみデータが取得されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1694">If the property is set to <strong>false</strong>, which is the default value, data is retrieved only for the current session company.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1695">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1695">Description</span></span></td>
<td><span data-ttu-id="93299-1696">オプション: クエリについて、何を返すかなどを説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1696">Optional: Describe the query, what it returns, and so on.</span></span> <span data-ttu-id="93299-1697">このプロパティは、Microsoft Office アドイン シナリオで役立ちます。</span><span class="sxs-lookup"><span data-stu-id="93299-1697">This property is useful in Microsoft Office Add-in scenarios.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1698">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-1698">Form</span></span></td>
<td><span data-ttu-id="93299-1699">ユーザーがクエリを操作するときに MorphX が表示する必要があるクエリ フォームを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1699">Specify that query form that MorphX should show when users interact with the query.</span></span> <span data-ttu-id="93299-1700">既定値は <strong>SysQueryForm</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1700">The default value is <strong>SysQueryForm</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1701">対話型</span><span class="sxs-lookup"><span data-stu-id="93299-1701">Interactive</span></span></td>
<td><span data-ttu-id="93299-1702">ユーザーがクエリを区切る、プリンター オプションを設定するなどして、レポートを操作できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1702">Specify whether users can interact with the report by delimiting queries, setting printer options, and so on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1703">リテラル</span><span class="sxs-lookup"><span data-stu-id="93299-1703">Literals</span></span></td>
<td><span data-ttu-id="93299-1704">SQL ステートメントでリテラルがどのような方法で表示されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1704">Specify how literals are represented in SQL statements.</span></span> <span data-ttu-id="93299-1705"><strong>forceLiterals</strong> オプションは、最適化時に Microsoft SQL Server データベースに対して <strong>where</strong> 句で使用される実際値を明らかにするように、カーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="93299-1705">The <strong>forceLiterals</strong> option instructs the kernel to reveal the actual values that are used in <strong>where</strong> clauses to the Microsoft SQL Server database at the time of optimization.</span></span> <span data-ttu-id="93299-1706"><strong>forcePlaceholders</strong> オプションは、実際の値を明らかにしないようにカーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="93299-1706">The <strong>forcePlaceholders</strong> option instructs the kernel not to reveal the actual values.</span></span> <span data-ttu-id="93299-1707"><strong>注記:</strong> <strong>forceLiterals</strong> オプションは、コードを SQL インジェクション セキュリティの脅威にさらす可能性があるため、使用しないことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="93299-1707"><strong>Note:</strong> We don&#39;t recommend that you use the <strong>forceLiterals</strong> option, because it could expose code to an SQL injection security threat.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1708">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1708">Model</span></span></td>
<td><span data-ttu-id="93299-1709">クエリがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1709">Specify the model that the query is in.</span></span> <span data-ttu-id="93299-1710">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1710">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1711">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-1711">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-1712">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1712">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1713">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1713">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1714">QueryType</span><span class="sxs-lookup"><span data-stu-id="93299-1714">QueryType</span></span></td>
<td><span data-ttu-id="93299-1715">クエリのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1715">Specify the type of the query.</span></span> <span data-ttu-id="93299-1716"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1716">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1717">結合</span><span class="sxs-lookup"><span data-stu-id="93299-1717">Join</span></span></li>
<li><span data-ttu-id="93299-1718">結合</span><span class="sxs-lookup"><span data-stu-id="93299-1718">Union</span></span></li>
</ul>
<span data-ttu-id="93299-1719">既定値は <strong>結合</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1719">The default value is <strong>Join</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1720">検索可能</span><span class="sxs-lookup"><span data-stu-id="93299-1720">Searchable</span></span></td>
<td><span data-ttu-id="93299-1721">Microsoft SharePoint Business Catalog を検索するために使用できる一連のクエリの一部としてクエリを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1721">Specify whether the query can be part of a set of queries that is used to search the Microsoft SharePoint Business Catalog.</span></span> <span data-ttu-id="93299-1722">このプロパティは、エンタープライズ検索機能を使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="93299-1722">This property is useful when you use the Enterprise Search feature.</span></span> <span data-ttu-id="93299-1723">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1723">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1724">肩書き</span><span class="sxs-lookup"><span data-stu-id="93299-1724">Title</span></span></td>
<td><span data-ttu-id="93299-1725">クエリのヘッダー。</span><span class="sxs-lookup"><span data-stu-id="93299-1725">The heading for the query.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1726">UserUpdate</span><span class="sxs-lookup"><span data-stu-id="93299-1726">UserUpdate</span></span></td>
<td><span data-ttu-id="93299-1727">クエリ フォームが再度開かれたときにその状態を維持する必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1727">Specify whether the query form should retain its state when it&#39;s reopened.</span></span> <span data-ttu-id="93299-1728">このプロパティを<strong>はい</strong>に設定すると、以前の設定が復元されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1728">If you set this property to <strong>Yes</strong>, the previous settings are restored.</span></span> <span data-ttu-id="93299-1729"><strong>いいえ</strong>を設定すると、データを表示できますが、編集できない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1729">If you set it to <strong>No</strong>, the data can be viewed but not edited.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1730">バージョン</span><span class="sxs-lookup"><span data-stu-id="93299-1730">Version</span></span></td>
<td><span data-ttu-id="93299-1731">バージョンは、クエリが更新されるたびに増加します。</span><span class="sxs-lookup"><span data-stu-id="93299-1731">The version is increased every time that the query is updated.</span></span> <span data-ttu-id="93299-1732">このプロパティは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-1732">This property is read-only.</span></span></td>
</tr>
</tbody>
</table>

### <a name="data-source-properties"></a><span data-ttu-id="93299-1733">データ ソース プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1733">Data source properties</span></span>

<span data-ttu-id="93299-1734">次のプロパティは、データ ソースの特性を制御します。</span><span class="sxs-lookup"><span data-stu-id="93299-1734">The following properties control the characteristics of a data source.</span></span> <span data-ttu-id="93299-1735">追加のプロパティは、埋め込みデータ ソースとデータ ソースとの関係で使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1735">Additional properties are available on embedded data sources and relations between data sources.</span></span> <span data-ttu-id="93299-1736">また、データ ソース内のフィールドに対して 1 つのプロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="93299-1736">You can also set one property on fields in the data source.</span></span>

| <span data-ttu-id="93299-1737">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1737">Property</span></span>            | <span data-ttu-id="93299-1738">入手する場所</span><span class="sxs-lookup"><span data-stu-id="93299-1738">Where it's available</span></span>                 | <span data-ttu-id="93299-1739">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1739">Description</span></span>                                                                                                                                                                                                                                                                                                                        |
|---------------------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-1740">AllowAdd</span><span class="sxs-lookup"><span data-stu-id="93299-1740">AllowAdd</span></span>            | <span data-ttu-id="93299-1741">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1741">Data source</span></span>                          | <span data-ttu-id="93299-1742">ユーザーが実行時に並べ替えおよび範囲にフィールドを追加できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1742">Specify whether users can add fields to sorting and ranges at run time.</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="93299-1743">法人</span><span class="sxs-lookup"><span data-stu-id="93299-1743">Company</span></span>             | <span data-ttu-id="93299-1744">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1744">Data source</span></span>                          | <span data-ttu-id="93299-1745">データの取得元の会社を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1745">Specify the company to retrieve data from.</span></span>                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="93299-1746">動的</span><span class="sxs-lookup"><span data-stu-id="93299-1746">Dynamic</span></span>             | <span data-ttu-id="93299-1747">データ ソースのフィールド ノード</span><span class="sxs-lookup"><span data-stu-id="93299-1747">Fields node in a data source</span></span>         | <span data-ttu-id="93299-1748">データ ソース内のテーブルのすべてのフィールドを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1748">Specify whether all fields in the table in the data source are used.</span></span> <span data-ttu-id="93299-1749">このプロパティを**はい**に設定すると、データ ソース内のすべてのフィールドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1749">If you set this property to **Yes**, all the fields in the data source are used.</span></span> <span data-ttu-id="93299-1750">**いいえ**を設定すると、一部のフィールドを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1750">If you set it to **No**, you can remove some of the fields.</span></span> <span data-ttu-id="93299-1751">データ ソースがベース テーブルのとき、**はい** の値は、派生テーブルのすべてのフィールドが使用されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="93299-1751">When the data source is a base table, a value of **Yes** means that all fields from the derived tables are used.</span></span> |
| <span data-ttu-id="93299-1752">有効</span><span class="sxs-lookup"><span data-stu-id="93299-1752">Enabled</span></span>             | <span data-ttu-id="93299-1753">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1753">Data source</span></span>                          | <span data-ttu-id="93299-1754">このプロパティを**いいえ**に設定すると、データ ソース (およびすべての埋め込みデータ ソース) は無視されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1754">If you set this property to **No**, the data source (and all embedded data sources) are ignored.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="93299-1755">FetchMode</span><span class="sxs-lookup"><span data-stu-id="93299-1755">FetchMode</span></span>           | <span data-ttu-id="93299-1756">埋め込みデータ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1756">Embedded data source</span></span>                 | <span data-ttu-id="93299-1757">1:1 の関係または 1:n の関係を通じてデータ ソースを関連付ける必要があるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1757">Specify whether the data sources should be related through a 1:1 relation or a 1:n relation.</span></span> <span data-ttu-id="93299-1758">**注記:** レポートで使用されているデータ ソースの場合、1:1 のフェッチ モードを使用する結合関係を使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1758">**Note:** For data sources that are used on reports, use a join relation that uses 1:1 fetch mode.</span></span>                                                                                                                                    |
| <span data-ttu-id="93299-1759">フィールド、RelatedField</span><span class="sxs-lookup"><span data-stu-id="93299-1759">Field, RelatedField</span></span> | <span data-ttu-id="93299-1760">埋め込みデータソースでの関係</span><span class="sxs-lookup"><span data-stu-id="93299-1760">Relations on an embedded data source</span></span> | <span data-ttu-id="93299-1761">リレーションで使用される親データ ソースおよび関連データ ソースのフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1761">The name of the fields from the parent data source and related data source that are used in the relation.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="93299-1762">FirstFast</span><span class="sxs-lookup"><span data-stu-id="93299-1762">FirstFast</span></span>           | <span data-ttu-id="93299-1763">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1763">Data source</span></span>                          | <span data-ttu-id="93299-1764">このプロパティを**はい**に設定すると、データベースでは、クエリからの最初のレコードが、他のレコードの前に取得される必要があるというヒントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1764">If you set this property to **Yes**, the database receives a hint that the first record from the query should be retrieved before the other records.</span></span> <span data-ttu-id="93299-1765">この設定により、一部のデータベース システムでレコードの検索を最適化できるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="93299-1765">This setting enables some database systems to optimize record retrieval and therefore helps improve performance.</span></span>                                                              |
| <span data-ttu-id="93299-1766">FirstOnly</span><span class="sxs-lookup"><span data-stu-id="93299-1766">FirstOnly</span></span>           | <span data-ttu-id="93299-1767">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1767">Data source</span></span>                          | <span data-ttu-id="93299-1768">このプロパティを**はい**に設定すると、データベースでは、クエリからの最初のレコードのみが必要であるというヒントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1768">If you set this property to **Yes**, the database receives a hint that only the first record from the query is required.</span></span> <span data-ttu-id="93299-1769">この設定により、一部のデータベース システムでレコードの検索を最適化できるため、パフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="93299-1769">This setting enables some database systems to optimize record retrieval and therefore helps improve performance.</span></span>                                                                                          |
| <span data-ttu-id="93299-1770">JoinMode</span><span class="sxs-lookup"><span data-stu-id="93299-1770">JoinMode</span></span>            | <span data-ttu-id="93299-1771">埋め込みデータ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1771">Embedded data source</span></span>                 | <span data-ttu-id="93299-1772">データ ソースからの出力を結合するために使用される方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1772">Specify the strategy that is used to join the output from a data source.</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="93299-1773">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-1773">Name</span></span>                | <span data-ttu-id="93299-1774">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1774">Data source</span></span>                          | <span data-ttu-id="93299-1775">データ ソースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1775">Specify the name of the data source.</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="93299-1776">リレーション</span><span class="sxs-lookup"><span data-stu-id="93299-1776">Relations</span></span>           | <span data-ttu-id="93299-1777">埋め込みデータ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1777">Embedded data source</span></span>                 | <span data-ttu-id="93299-1778">テーブルと EDT に対して定義されている関係をクエリ システムが使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1778">Specify whether the query system should use the relations that are defined for tables and EDTs.</span></span> <span data-ttu-id="93299-1779">このプロパティを**はい**に設定すると、リレーションが変更された場合にクエリが自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1779">If you set this property to **Yes**, the query is automatically updated if a relation is changed.</span></span>                                                                                                                                  |
| <span data-ttu-id="93299-1780">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-1780">Table</span></span>               | <span data-ttu-id="93299-1781">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1781">Data source</span></span>                          | <span data-ttu-id="93299-1782">データ ソースとして使用されるテーブル、マップ、またはビューを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1782">Specify the table, map, or view that is used as a data source.</span></span> <span data-ttu-id="93299-1783">このプロパティは、並べ替え順序または範囲が定義された後は変更できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1783">This property can't be modified after a sorting order or a range has been defined.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="93299-1784">Table、RelatedTable</span><span class="sxs-lookup"><span data-stu-id="93299-1784">Table, RelatedTable</span></span> | <span data-ttu-id="93299-1785">埋め込みデータソースでの関係</span><span class="sxs-lookup"><span data-stu-id="93299-1785">Relations on an embedded data source</span></span> | <span data-ttu-id="93299-1786">親データ ソースおよび関連データ ソースの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-1786">The name of the parent data source and the related data source.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="93299-1787">UniqueId</span><span class="sxs-lookup"><span data-stu-id="93299-1787">UniqueId</span></span>            | <span data-ttu-id="93299-1788">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1788">Data source</span></span>                          | <span data-ttu-id="93299-1789">データ ソースの一意の番号。</span><span class="sxs-lookup"><span data-stu-id="93299-1789">The unique number of the data source.</span></span> <span data-ttu-id="93299-1790">このプロパティは、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="93299-1790">This property is read-only.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="93299-1791">更新</span><span class="sxs-lookup"><span data-stu-id="93299-1791">Update</span></span>              | <span data-ttu-id="93299-1792">データ ソース</span><span class="sxs-lookup"><span data-stu-id="93299-1792">Data source</span></span>                          | <span data-ttu-id="93299-1793">クエリがデータベース内のレコードを更新できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1793">Specify whether the query can update records in the database.</span></span>                                                                                                                                                                                                                                                                      |

### <a name="range-properties"></a><span data-ttu-id="93299-1794">範囲のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1794">Range properties</span></span>

<span data-ttu-id="93299-1795">次のプロパティは、範囲指定の特性を決定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1795">The following properties determine the characteristics of the range specification.</span></span> <span data-ttu-id="93299-1796">たとえば、実行時に、範囲の変更を許可されているかどうかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1796">For example, you can specify whether users are allowed to modify the range at run time.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1797">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1797">Property</span></span></th>
<th><span data-ttu-id="93299-1798">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1798">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1799">有効</span><span class="sxs-lookup"><span data-stu-id="93299-1799">Enabled</span></span></td>
<td><span data-ttu-id="93299-1800">範囲指定のフィールドを無効にするには、このプロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-1800">Use this property to disable a field in a range specification.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1801">フィールド</span><span class="sxs-lookup"><span data-stu-id="93299-1801">Field</span></span></td>
<td><span data-ttu-id="93299-1802">範囲を定義するためのフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1802">Specify the field to define a range on.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1803">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-1803">Label</span></span></td>
<td><span data-ttu-id="93299-1804">範囲のラベルを入力します。</span><span class="sxs-lookup"><span data-stu-id="93299-1804">Enter a label for the range.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1805">ステータス</span><span class="sxs-lookup"><span data-stu-id="93299-1805">Status</span></span></td>
<td><span data-ttu-id="93299-1806">ユーザーが実行時にクエリ ダイアログ ボックスで範囲の変更を許可されているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1806">Specify whether users are allowed to modify the range in the query dialog box at run time.</span></span> <span data-ttu-id="93299-1807"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1807">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1808"><strong>オープン</strong> - ユーザーは範囲を表示および編集できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1808"><strong>Open</strong> – Users can view and edit the range.</span></span></li>
<li><span data-ttu-id="93299-1809"><strong>ロック</strong> - ユーザーは、範囲のみを表示できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1809"><strong>Lock</strong> – Users can only view the range.</span></span></li>
<li><span data-ttu-id="93299-1810"><strong>非表示</strong> - ユーザーは範囲を表示または編集できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1810"><strong>Hide</strong> – Users can&#39;t view or edit the range.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1811">先頭値</span><span class="sxs-lookup"><span data-stu-id="93299-1811">Value</span></span></td>
<td><span data-ttu-id="93299-1812">取得されるレコードの範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1812">Specify the range for the records that are retrieved.</span></span> <span data-ttu-id="93299-1813">列挙型を使用する場合は、テキスト文字列を使用しません。</span><span class="sxs-lookup"><span data-stu-id="93299-1813">If you use enumerations, don&#39;t use text strings.</span></span> <span data-ttu-id="93299-1814">列挙 ID を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-1814">The enumeration ID must be used.</span></span></td>
</tr>
</tbody>
</table>

## <a name="report-properties"></a><span data-ttu-id="93299-1815">レポート プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1815">Report properties</span></span>
<span data-ttu-id="93299-1816">レポートのプロパティのほとんどは、アプリケーション エクスプローラーのデザイン、デザイン セクション、コントロール ノードに設定されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1816">Most of the properties for a report are set on the design, design section, and control nodes in Application Explorer.</span></span> <span data-ttu-id="93299-1817">レポートで使用可能なシステム プロパティの詳細については、「システムと共通プロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-1817">For information about system properties that are available on reports, see the "System and common properties" section.</span></span> <span data-ttu-id="93299-1818">次のテーブルでは、レポートのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1818">The following table describes the properties of a report.</span></span>

| <span data-ttu-id="93299-1819">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1819">Property</span></span>    | <span data-ttu-id="93299-1820">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1820">Description</span></span>                                                                                                                                                                                                                                  |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-1821">AllowCheck</span><span class="sxs-lookup"><span data-stu-id="93299-1821">AllowCheck</span></span>  | <span data-ttu-id="93299-1822">ユーザーが表示するアクセス許可を持たないレポートを実行しようとしたときにメッセージが表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1822">Specify whether a message is shown when users try to run reports that they don't have permission to view.</span></span> <span data-ttu-id="93299-1823">**はい** を選択し、メッセージが表示されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1823">Select **Yes** to specify that a message is shown.</span></span>                                                                                 |
| <span data-ttu-id="93299-1824">AutoJoin</span><span class="sxs-lookup"><span data-stu-id="93299-1824">AutoJoin</span></span>    | <span data-ttu-id="93299-1825">レポート クエリの範囲を設定するために **element.args** メソッドにより返されたレコードを使用するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1825">Specify whether a record that is returned by the **element.args** method is used to set the range on the report query.</span></span>                                                                                                                       |
| <span data-ttu-id="93299-1826">対話型</span><span class="sxs-lookup"><span data-stu-id="93299-1826">Interactive</span></span> | <span data-ttu-id="93299-1827">ユーザーがレポートに関連付けられているクエリを変更することで、表示するレコードを選択できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1827">Specify whether users can select which records to show by modifying the query that is associated with a report.</span></span>                                                                                                                              |
| <span data-ttu-id="93299-1828">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-1828">Model</span></span>       | <span data-ttu-id="93299-1829">レポートがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1829">Specify the model that the report is in.</span></span> <span data-ttu-id="93299-1830">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-1830">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-1831">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-1831">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-1832">他の層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1832">The same element can exist in a customized version in a model that is in another layer.</span></span> |

## <a name="report-control-properties"></a><span data-ttu-id="93299-1833">レポート管理プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1833">Report control properties</span></span>
<span data-ttu-id="93299-1834">次のテーブルでは、レポート コントロールのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-1834">The following table describes report control properties.</span></span> <span data-ttu-id="93299-1835">コントロールに使用される追加のプロパティの詳細については、「フォームのコントロールのプロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-1835">For information about additional properties that are available for controls, see the "Form control properties" section.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-1836">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-1836">Property</span></span></th>
<th><span data-ttu-id="93299-1837">説明</span><span class="sxs-lookup"><span data-stu-id="93299-1837">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-1838">配置</span><span class="sxs-lookup"><span data-stu-id="93299-1838">Alignment</span></span></td>
<td><span data-ttu-id="93299-1839">コントロールに表示される値の配置を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1839">Specify the alignment of a value that is shown in a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1840">AllowNegative</span><span class="sxs-lookup"><span data-stu-id="93299-1840">AllowNegative</span></span></td>
<td><span data-ttu-id="93299-1841">コントロールが負の値を受け入れるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1841">Specify whether the control accepts negative values.</span></span> <span data-ttu-id="93299-1842">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1842">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1843">ArrayIndex</span><span class="sxs-lookup"><span data-stu-id="93299-1843">ArrayIndex</span></span></td>
<td><span data-ttu-id="93299-1844">コントロールに表示される配列要素を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1844">Specify the array element that is shown in a control.</span></span> <span data-ttu-id="93299-1845">このコントロールは、配列要素を持つ拡張データ型に基づいています。</span><span class="sxs-lookup"><span data-stu-id="93299-1845">The control is based on an extended data type that has array elements.</span></span> <span data-ttu-id="93299-1846">このプロパティは、テキストおよびシェイプ コントロールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1846">This property isn&#39;t available for text and shape controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1847">AutoDeclaration</span><span class="sxs-lookup"><span data-stu-id="93299-1847">AutoDeclaration</span></span></td>
<td><span data-ttu-id="93299-1848">コントロールと同じ名前を持つ変数が作成されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1848">Specify whether a variable is created that has the same name as the control.</span></span> <span data-ttu-id="93299-1849">このプロパティを<strong>はい</strong>に設定すると、X++ コードからレポートコントロールへのアクセスが容易になり、コンパイル時にエラーを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-1849">When you set this property to <strong>Yes</strong>, it&#39;s easier to access the report controls from X++ code, and you can find errors at compile time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1850">AutoInsSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-1850">AutoInsSeparator</span></span></td>
<td><span data-ttu-id="93299-1851">小数点区切り記号が表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1851">Specify whether a decimal separator is shown.</span></span> <span data-ttu-id="93299-1852">このプロパティは、数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1852">This property is available only for real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1853">BackgroundColor</span><span class="sxs-lookup"><span data-stu-id="93299-1853">BackgroundColor</span></span></td>
<td><span data-ttu-id="93299-1854">コントロールの背景色を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1854">Specify the background color for a control.</span></span> <span data-ttu-id="93299-1855">このプロパティの設定は、<strong>BackStyle</strong> プロパティを使用して上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-1855">The setting of this property can be overridden by using the <strong>BackStyle</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1856">BackStyle</span><span class="sxs-lookup"><span data-stu-id="93299-1856">BackStyle</span></span></td>
<td><span data-ttu-id="93299-1857">コントロールの背景色が不透明であるか透明であるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1857">Specify whether the control background is opaque or transparent.</span></span> <span data-ttu-id="93299-1858">このプロパティを<strong>透明</strong>に設定すると、動作はコントロールのタイプによって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-1858">When you set this property to <strong>Transparent</strong>, the behavior depends on the type of control:</span></span>
<ul>
<li><span data-ttu-id="93299-1859">ビットマップ コントロールについては、同じ色を持つピクセル単位は透過的です。</span><span class="sxs-lookup"><span data-stu-id="93299-1859">For bitmap controls, pixels that have the same color are transparent.</span></span></li>
<li><span data-ttu-id="93299-1860">その他のすべてのコントロールについては、前景色が背景色として使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1860">For all other controls, the foreground color is used as the background color.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1861">太字</span><span class="sxs-lookup"><span data-stu-id="93299-1861">Bold</span></span></td>
<td><span data-ttu-id="93299-1862">太字のテキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1862">Specify bold text formatting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1863">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1863">BottomMargin</span></span></td>
<td><span data-ttu-id="93299-1864">コントロールの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1864">Specify the margin for a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1865">ChangeCase</span><span class="sxs-lookup"><span data-stu-id="93299-1865">ChangeCase</span></span></td>
<td><span data-ttu-id="93299-1866">ユーザーが入力したテキストが大文字か小文字かを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1866">Specify the case of text that a user enters.</span></span> <span data-ttu-id="93299-1867">このプロパティは、文字列、列挙、確認、および確認コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1867">This property is available only for string, enum, text, and prompt controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1868">ChangeLabelCase</span><span class="sxs-lookup"><span data-stu-id="93299-1868">ChangeLabelCase</span></span></td>
<td><span data-ttu-id="93299-1869">レポートを印刷するときにコントロールのラベルを変更するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1869">Specify whether the label for the control should be modified when the report is printed.</span></span> <span data-ttu-id="93299-1870"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1870">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1871">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1871">Auto</span></span></li>
<li><span data-ttu-id="93299-1872">None</span><span class="sxs-lookup"><span data-stu-id="93299-1872">None</span></span></li>
<li><span data-ttu-id="93299-1873">大文字</span><span class="sxs-lookup"><span data-stu-id="93299-1873">UPPER CASE</span></span></li>
<li><span data-ttu-id="93299-1874">lower case</span><span class="sxs-lookup"><span data-stu-id="93299-1874">lower case</span></span></li>
<li><span data-ttu-id="93299-1875">タイトル ケース</span><span class="sxs-lookup"><span data-stu-id="93299-1875">Title Case</span></span></li>
</ul>
<span data-ttu-id="93299-1876">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1876">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1877">ColorScheme</span><span class="sxs-lookup"><span data-stu-id="93299-1877">ColorScheme</span></span></td>
<td><span data-ttu-id="93299-1878">コントロールのカラー パレットを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1878">Specify the color palette for a control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1879">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-1879">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-1880">コントロールの構成キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1880">Specify a configuration key for the control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1881">CSSClass</span><span class="sxs-lookup"><span data-stu-id="93299-1881">CSSClass</span></span></td>
<td><span data-ttu-id="93299-1882">HTML での値の表示に使用するカスケード スタイル シート (CSS) を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1882">Specify the Cascading Style Sheet (CSS) to use to render the value in HTML.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1883">DataField</span><span class="sxs-lookup"><span data-stu-id="93299-1883">DataField</span></span></td>
<td><span data-ttu-id="93299-1884">コントロールのテーブル フィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1884">Specify a table field for the control.</span></span> <span data-ttu-id="93299-1885">このプロパティは、テキスト、シェイプ、ボックス、およびビットマップ コントロールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1885">This property isn&#39;t available for text, shape, box, and bitmap controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1886">DataMethod</span><span class="sxs-lookup"><span data-stu-id="93299-1886">DataMethod</span></span></td>
<td><span data-ttu-id="93299-1887">コントロールのデータを示す表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1887">Specify a display method that shows data in a control.</span></span> <span data-ttu-id="93299-1888">このプロパティは、テキスト、シェイプ、およびボックス コントロールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-1888">This property isn&#39;t available for text, shape, and box controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1889">DateDay</span><span class="sxs-lookup"><span data-stu-id="93299-1889">DateDay</span></span></td>
<td><span data-ttu-id="93299-1890">曜日の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1890">Specify the format for the day.</span></span> <span data-ttu-id="93299-1891">このプロパティは、日付コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1891">This property is available only for date controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1892">DateFormat</span><span class="sxs-lookup"><span data-stu-id="93299-1892">DateFormat</span></span></td>
<td><span data-ttu-id="93299-1893">日付の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1893">Specify the format for a date.</span></span> <span data-ttu-id="93299-1894">このプロパティは、日付コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1894">This property is available only for date controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1895">DateMonth</span><span class="sxs-lookup"><span data-stu-id="93299-1895">DateMonth</span></span></td>
<td><span data-ttu-id="93299-1896">月の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1896">Specify the format for the month.</span></span> <span data-ttu-id="93299-1897">このプロパティは、日付コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1897">This property is available only for date controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1898">DateSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-1898">DateSeparator</span></span></td>
<td><span data-ttu-id="93299-1899">月、日、年の間に表示される区切り記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1899">Specify the separator that appears between the month, day, and year.</span></span> <span data-ttu-id="93299-1900">このプロパティは、日付コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1900">This property is available only for date controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1901">DateYear</span><span class="sxs-lookup"><span data-stu-id="93299-1901">DateYear</span></span></td>
<td><span data-ttu-id="93299-1902">年の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1902">Specify the format for the year.</span></span> <span data-ttu-id="93299-1903">このプロパティは、日付コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1903">This property is available only for date controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1904">DecimalSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-1904">DecimalSeparator</span></span></td>
<td><span data-ttu-id="93299-1905">小数点以下の値を区別するために使用する記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1905">Specify the symbol that is used to separate decimal values.</span></span> <span data-ttu-id="93299-1906">このプロパティは、数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1906">This property is available only for real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1907">DisplaceNegative</span><span class="sxs-lookup"><span data-stu-id="93299-1907">DisplaceNegative</span></span></td>
<td><span data-ttu-id="93299-1908">値が負の数値の場合のグリッド コントロール内の値の新しい位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1908">Specify a new position for a value in a grid control when the value is a negative number.</span></span> <span data-ttu-id="93299-1909">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1909">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1910">DynamicHeight</span><span class="sxs-lookup"><span data-stu-id="93299-1910">DynamicHeight</span></span></td>
<td><span data-ttu-id="93299-1911">テキストの追加の行を表示するためにコントロールのサイズを変更するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1911">Specify whether the control is resized to show additional lines of text.</span></span> <span data-ttu-id="93299-1912">このプロパティを<strong>はい</strong>に設定すると、必要に応じて、ページ ヘッダー、ページ フッター、および繰り返し列見出しが自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1912">When you set this property to <strong>Yes</strong>, page headers, page footers, and repeating column headings are automatically added as required.</span></span> <span data-ttu-id="93299-1913">このプロパティは、文字列コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1913">This property is available only for string controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1914">ExtendedDataType</span><span class="sxs-lookup"><span data-stu-id="93299-1914">ExtendedDataType</span></span></td>
<td><span data-ttu-id="93299-1915">コントロールに関連付けられているフィールドを基にする EDT を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1915">Specify the EDT that the field that is associated with the control should be based on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1916">ExtraSumWidth</span><span class="sxs-lookup"><span data-stu-id="93299-1916">ExtraSumWidth</span></span></td>
<td><span data-ttu-id="93299-1917">合計に対して許可される既定の幅を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-1917">Modify the default width that is allowed for sums.</span></span> <span data-ttu-id="93299-1918">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1918">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1919">フォント</span><span class="sxs-lookup"><span data-stu-id="93299-1919">Font</span></span></td>
<td><span data-ttu-id="93299-1920">フォントを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1920">Specify the font.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1921">フォントサイズ</span><span class="sxs-lookup"><span data-stu-id="93299-1921">FontSize</span></span></td>
<td><span data-ttu-id="93299-1922">フォント サイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1922">Specify the font size.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1923">ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="93299-1923">ForegroundColor</span></span></td>
<td><span data-ttu-id="93299-1924">コントロールの前景色を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1924">Specify the foreground color for a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1925">FormatMST</span><span class="sxs-lookup"><span data-stu-id="93299-1925">FormatMST</span></span></td>
<td><span data-ttu-id="93299-1926">標準通貨形式を使用して値を書式設定するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1926">Specify whether values are formatted by using standard currency format.</span></span> <span data-ttu-id="93299-1927">このプロパティは、数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1927">This property is available only for real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1928">高さ</span><span class="sxs-lookup"><span data-stu-id="93299-1928">Height</span></span></td>
<td><span data-ttu-id="93299-1929">コントロールの高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1929">Specify the height of a control.</span></span> <span data-ttu-id="93299-1930">コントロールが EDTに関連付けられている場合、その <strong>Height</strong> プロパティは EDT の <strong>DisplayLength</strong> プロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="93299-1930">When a control is associated with an EDT, the <strong>Height</strong> property of the control overrides the <strong>DisplayLength</strong> property of the EDT.</span></span> <span data-ttu-id="93299-1931">ビットマップ コントロールの <strong>Height</strong> プロパティを<strong>自動</strong>に設定すると、コントロールのサイズは、グラフィックのサイズに基づきます。</span><span class="sxs-lookup"><span data-stu-id="93299-1931">If you set the <strong>Height</strong> property to <strong>Auto</strong> for a bitmap control, the size of the control is based on the size of the graphic.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1932">ImageName</span><span class="sxs-lookup"><span data-stu-id="93299-1932">ImageName</span></span></td>
<td><span data-ttu-id="93299-1933">画像のファイル名を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1933">Specify the file name for an image.</span></span> <span data-ttu-id="93299-1934">このプロパティは、ビットマップ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1934">This property is available only for bitmap controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1935">ImageResource</span><span class="sxs-lookup"><span data-stu-id="93299-1935">ImageResource</span></span></td>
<td><span data-ttu-id="93299-1936">表示するシステム リソースの ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1936">Specify the ID for a system resource to show.</span></span> <span data-ttu-id="93299-1937">リソース マクロは、これらの ID のリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="93299-1937">The resource macro provides a list of these IDs.</span></span> <span data-ttu-id="93299-1938">マクロは、アプリケーション エクスプローラーの<strong>マクロ</strong> ノードの下にあります。</span><span class="sxs-lookup"><span data-stu-id="93299-1938">Macros are located under the <strong>Macros</strong> node in Application Explorer.</span></span> <span data-ttu-id="93299-1939">このプロパティは、ビットマップ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1939">This property is available only for bitmap controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1940">斜体</span><span class="sxs-lookup"><span data-stu-id="93299-1940">Italic</span></span></td>
<td><span data-ttu-id="93299-1941">斜体のテキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1941">Specify italic text formatting.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1942">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-1942">Label</span></span></td>
<td><span data-ttu-id="93299-1943">コントロールのタイトルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1943">Specify a title for the control.</span></span> <span data-ttu-id="93299-1944">ラベルがここで指定されていない場合は、フィールドから継承されます。</span><span class="sxs-lookup"><span data-stu-id="93299-1944">If a label isn&#39;t specified here, it&#39;s inherited from the field.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1945">LabelBold</span><span class="sxs-lookup"><span data-stu-id="93299-1945">LabelBold</span></span></td>
<td><span data-ttu-id="93299-1946">コントロールのラベルの太字設定を示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1946">Set or return a value that indicates the bold setting for the label in the control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1947">LabelCSSClass</span><span class="sxs-lookup"><span data-stu-id="93299-1947">LabelCSSClass</span></span></td>
<td><span data-ttu-id="93299-1948">HTML でのラベルのレンダリングに使用する CSS を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1948">Specify the CSS to use to render the label in HTML.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1949">LabelFont</span><span class="sxs-lookup"><span data-stu-id="93299-1949">LabelFont</span></span></td>
<td><span data-ttu-id="93299-1950">フォーム コンボ ボックス コントロール内のラベル テキストのフォントを示す文字列データ型値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1950">Set or return a string data type value that indicates the font for the label text in a form combo box control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1951">LabelFontSize</span><span class="sxs-lookup"><span data-stu-id="93299-1951">LabelFontSize</span></span></td>
<td><span data-ttu-id="93299-1952">フォーム コンボ ボックス コントロールのラベル テキストのフォント サイズをポイント単位で設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1952">Set or return the font size, in points, for the label text in a form combo box control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1953">LabelItalic</span><span class="sxs-lookup"><span data-stu-id="93299-1953">LabelItalic</span></span></td>
<td><span data-ttu-id="93299-1954">コントロール ラベルのテキストが斜体で表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1954">Set or return a value that indicates whether the text in the control label should be italic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1955">LabelLineBelow</span><span class="sxs-lookup"><span data-stu-id="93299-1955">LabelLineBelow</span></span></td>
<td><span data-ttu-id="93299-1956">コントロール タイトルの下線の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1956">Specify the format of the underline for the control title.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1957">LabelLineThickness</span><span class="sxs-lookup"><span data-stu-id="93299-1957">LabelLineThickness</span></span></td>
<td><span data-ttu-id="93299-1958">列見出しの下の行の形式を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1958">Specify the format of the line below column headings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1959">LabelPosition</span><span class="sxs-lookup"><span data-stu-id="93299-1959">LabelPosition</span></span></td>
<td><span data-ttu-id="93299-1960">コントロールのラベルの位置を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1960">Set or return the position of the label for the control.</span></span> <span data-ttu-id="93299-1961">有効な値は <strong>Left</strong> および <strong>Above</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1961">Valid values are <strong>Left</strong> and <strong>Above</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1962">LabelTabLeader</span><span class="sxs-lookup"><span data-stu-id="93299-1962">LabelTabLeader</span></span></td>
<td><span data-ttu-id="93299-1963">ラベルを制御するために一連の点を追加するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1963">Specify whether to append a series of dots to control labels.</span></span> <span data-ttu-id="93299-1964"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1964">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-1965">自動</span><span class="sxs-lookup"><span data-stu-id="93299-1965">Auto</span></span></li>
<li><span data-ttu-id="93299-1966">追加しない</span><span class="sxs-lookup"><span data-stu-id="93299-1966">Do not append</span></span></li>
<li><span data-ttu-id="93299-1967">追記を実行</span><span class="sxs-lookup"><span data-stu-id="93299-1967">Do append</span></span></li>
</ul>
<span data-ttu-id="93299-1968">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-1968">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1969">LabelUnderline</span><span class="sxs-lookup"><span data-stu-id="93299-1969">LabelUnderline</span></span></td>
<td><span data-ttu-id="93299-1970">コントロール ラベルのテキストが下線付きで表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-1970">Set or return a value that indicates whether the text in the control label should be underlined.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1971">LabelWidth</span><span class="sxs-lookup"><span data-stu-id="93299-1971">LabelWidth</span></span></td>
<td><span data-ttu-id="93299-1972">コントロールのラベルの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1972">Specify the width of the label for the control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1973">左</span><span class="sxs-lookup"><span data-stu-id="93299-1973">Left</span></span></td>
<td><span data-ttu-id="93299-1974">コントロールの左揃えを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1974">Specify the left alignment of a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1975">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="93299-1975">LeftMargin</span></span></td>
<td><span data-ttu-id="93299-1976">コントロールの左余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1976">Specify the left margin for a control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1977">明細行</span><span class="sxs-lookup"><span data-stu-id="93299-1977">Line</span></span></td>
<td><span data-ttu-id="93299-1978">図形を形成する線の外観を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1978">Specify the appearance of the lines that form a shape.</span></span> <span data-ttu-id="93299-1979">このプロパティは、シェイプ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-1979">This property is available only for shape controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1980">LineAbove</span><span class="sxs-lookup"><span data-stu-id="93299-1980">LineAbove</span></span></td>
<td><span data-ttu-id="93299-1981">コントロールの上の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1981">Specify the type of line for the top border of a control.</span></span> <span data-ttu-id="93299-1982">レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-1982">If your report has many lines or boxes, consider using a shape control inside the individual sections.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1983">LineBelow</span><span class="sxs-lookup"><span data-stu-id="93299-1983">LineBelow</span></span></td>
<td><span data-ttu-id="93299-1984">コントロールの下の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1984">Specify the type of line for the bottom border of a control.</span></span> <span data-ttu-id="93299-1985">レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-1985">If your report has many lines or boxes, consider using a shape control inside the individual sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1986">LineLeft</span><span class="sxs-lookup"><span data-stu-id="93299-1986">LineLeft</span></span></td>
<td><span data-ttu-id="93299-1987">コントロールの左の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1987">Specify the type of line for the left border of a control.</span></span> <span data-ttu-id="93299-1988">レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-1988">If your report has many lines or boxes, consider using a shape control inside the individual sections.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1989">LineRight</span><span class="sxs-lookup"><span data-stu-id="93299-1989">LineRight</span></span></td>
<td><span data-ttu-id="93299-1990">コントロールの右の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1990">Specify the type of line for the right border of a control.</span></span> <span data-ttu-id="93299-1991">レポートに多くの明細行またはボックスがある場合は、個別のセクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-1991">If your report has many lines or boxes, consider using a shape control inside the individual sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1992">MenuItemLabel</span><span class="sxs-lookup"><span data-stu-id="93299-1992">MenuItemLabel</span></span></td>
<td><span data-ttu-id="93299-1993">メニュー項目のラベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1993">Specify the label for a menu item.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-1994">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="93299-1994">MenuItemName</span></span></td>
<td><span data-ttu-id="93299-1995">メニュー項目の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1995">Specify the name of the menu item.</span></span> <span data-ttu-id="93299-1996">使用可能なメニュー項目は、<strong>MenuItemType</strong> プロパティの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-1996">The available menu items vary, depending on the setting of the <strong>MenuItemType</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-1997">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="93299-1997">MenuItemType</span></span></td>
<td><span data-ttu-id="93299-1998">メニュー項目がアクション、表示、出力メニュー項目のどれであるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-1998">Specify whether the menu item is an action, display, or output menu item.</span></span> <span data-ttu-id="93299-1999">表示メニュー項目はフォーム用で、出力メニュー項目はレポート用です。</span><span class="sxs-lookup"><span data-stu-id="93299-1999">A display menu item is for a form, and an output menu item is for a report.</span></span> <span data-ttu-id="93299-2000">出力メニュー項目はクラス、ジョブ、またはクエリです。</span><span class="sxs-lookup"><span data-stu-id="93299-2000">An output menu item is for a class, job, or query.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2001">MinNoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="93299-2001">MinNoOfDecimals</span></span></td>
<td><span data-ttu-id="93299-2002">表示される小数点以下桁数の最小数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2002">Specify the minimum number of decimal places that are shown.</span></span> <span data-ttu-id="93299-2003">末尾のゼロは表示されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2003">Trailing zeros aren&#39;t shown.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2004">ModelFieldName</span><span class="sxs-lookup"><span data-stu-id="93299-2004">ModelFieldName</span></span></td>
<td><span data-ttu-id="93299-2005">左揃えとコントロールの幅を決定するために使用されるフィールドを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2005">Specify a field that is used to determine the left alignment and width of a control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2006">NoOfDecimals</span><span class="sxs-lookup"><span data-stu-id="93299-2006">NoOfDecimals</span></span></td>
<td><span data-ttu-id="93299-2007">表示される小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2007">Specify the number of decimal places that are shown.</span></span> <span data-ttu-id="93299-2008">既定値は <strong>20</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-2008">The default value is <strong>20</strong>.</span></span> <span data-ttu-id="93299-2009">このプロパティは、数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2009">This property is available only for real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2010">ResizeBitmap</span><span class="sxs-lookup"><span data-stu-id="93299-2010">ResizeBitmap</span></span></td>
<td><span data-ttu-id="93299-2011">コントロールのサイズに合わせてイメージのサイズを変更できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2011">Specify whether an image can be resized to fit the dimensions of a control.</span></span> <span data-ttu-id="93299-2012">このプロパティは、ビットマップ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2012">This property is available only for bitmap controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2013">RightMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2013">RightMargin</span></span></td>
<td><span data-ttu-id="93299-2014">コントロールの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2014">Specify the margin for a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2015">RotateSign</span><span class="sxs-lookup"><span data-stu-id="93299-2015">RotateSign</span></span></td>
<td><span data-ttu-id="93299-2016">コントロールの符号を反転するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2016">Specify whether the sign for the control is inverted.</span></span> <span data-ttu-id="93299-2017">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2017">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2018">ShowLabel</span><span class="sxs-lookup"><span data-stu-id="93299-2018">ShowLabel</span></span></td>
<td><span data-ttu-id="93299-2019">コントロールのラベルがフォームに表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-2019">Set or return a value that indicates whether the label for the control is shown in the form.</span></span> <span data-ttu-id="93299-2020"><strong>True</strong> の値は、ラベルが表示されることを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-2020">A value of <strong>True</strong> indicates that the label will be shown.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2021">ShowPicAsText</span><span class="sxs-lookup"><span data-stu-id="93299-2021">ShowPicAsText</span></span></td>
<td><span data-ttu-id="93299-2022">画像ではなく、画像のファイル名を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2022">Specify whether the file name for an image is shown instead of the image.</span></span> <span data-ttu-id="93299-2023">このプロパティは、ビットマップ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2023">This property is available only for bitmap controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2024">ShowZero</span><span class="sxs-lookup"><span data-stu-id="93299-2024">ShowZero</span></span></td>
<td><span data-ttu-id="93299-2025">0 (ゼロ) の値が表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2025">Specify whether a 0 (zero) value is shown.</span></span> <span data-ttu-id="93299-2026">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2026">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2027">SignDisplay</span><span class="sxs-lookup"><span data-stu-id="93299-2027">SignDisplay</span></span></td>
<td><span data-ttu-id="93299-2028">数値の符号の表示方法を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2028">Specify how the sign of a number is shown.</span></span> <span data-ttu-id="93299-2029">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2029">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2030">SumAll</span><span class="sxs-lookup"><span data-stu-id="93299-2030">SumAll</span></span></td>
<td><span data-ttu-id="93299-2031">すべての値の合計が計算されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2031">Specify whether the sum of all values is calculated.</span></span> <span data-ttu-id="93299-2032">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2032">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2033">SumNeg</span><span class="sxs-lookup"><span data-stu-id="93299-2033">SumNeg</span></span></td>
<td><span data-ttu-id="93299-2034">すべての負の値の合計が計算されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2034">Specify whether the sum of all negative values is calculated.</span></span> <span data-ttu-id="93299-2035">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2035">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2036">SumPos</span><span class="sxs-lookup"><span data-stu-id="93299-2036">SumPos</span></span></td>
<td><span data-ttu-id="93299-2037">すべての正の値の合計が計算されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2037">Specify whether the sum of all positive values is calculated.</span></span> <span data-ttu-id="93299-2038">このプロパティは、整数および実数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2038">This property is available only for integer and real controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2039">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2039">Table</span></span></td>
<td><span data-ttu-id="93299-2040">コントロールのソース タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2040">Specify a data source for the control.</span></span> <span data-ttu-id="93299-2041">このプロパティは、テキスト、シェイプ、ボックス、およびビットマップ コントロールでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="93299-2041">This property isn&#39;t available for text, shape, box, and bitmap controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2042">テキスト</span><span class="sxs-lookup"><span data-stu-id="93299-2042">Text</span></span></td>
<td><span data-ttu-id="93299-2043">コントロールに表示されるテキスト文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2043">Specify the text string that is shown in a control.</span></span> <span data-ttu-id="93299-2044">このプロパティは、テキスト コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2044">This property is available only for text controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2045">TimeFormat</span><span class="sxs-lookup"><span data-stu-id="93299-2045">TimeFormat</span></span></td>
<td><span data-ttu-id="93299-2046">時間が 24 時間制と午前/午後形式のどちらで表示されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2046">Specify whether times are shown in 24-hour format or AM/PM format.</span></span> <span data-ttu-id="93299-2047">このプロパティは、時間コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2047">This property is available only for time controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2048">TimeHours</span><span class="sxs-lookup"><span data-stu-id="93299-2048">TimeHours</span></span></td>
<td><span data-ttu-id="93299-2049">時間を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2049">Specify whether hours are shown.</span></span> <span data-ttu-id="93299-2050">このプロパティは、時間コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2050">This property is available only for time controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2051">TimeMinutes</span><span class="sxs-lookup"><span data-stu-id="93299-2051">TimeMinutes</span></span></td>
<td><span data-ttu-id="93299-2052">分を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2052">Specify whether minutes are shown.</span></span> <span data-ttu-id="93299-2053">このプロパティは、時間コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2053">This property is available only for time controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2054">TimeSeconds</span><span class="sxs-lookup"><span data-stu-id="93299-2054">TimeSeconds</span></span></td>
<td><span data-ttu-id="93299-2055">秒を表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2055">Specify whether seconds are shown.</span></span> <span data-ttu-id="93299-2056">このプロパティは、時間コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2056">This property is available only for time controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2057">TimeSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-2057">TimeSeparator</span></span></td>
<td><span data-ttu-id="93299-2058">時間、分、秒を分けるために使用される記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2058">Specify the symbol that is used to separate hours, minutes, and seconds.</span></span> <span data-ttu-id="93299-2059">このプロパティは、時間コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2059">This property is available only for time controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2060">太さ</span><span class="sxs-lookup"><span data-stu-id="93299-2060">Thickness</span></span></td>
<td><span data-ttu-id="93299-2061">コントロールの境界線の太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2061">Specify the thickness of a control border.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2062">ThousandSeparator</span><span class="sxs-lookup"><span data-stu-id="93299-2062">ThousandSeparator</span></span></td>
<td><span data-ttu-id="93299-2063">1000 ごとに区切るために使用する記号を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2063">Specify the symbol that is used to separate thousands.</span></span> <span data-ttu-id="93299-2064">このプロパティは、数コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2064">This property is available only for real controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2065">上</span><span class="sxs-lookup"><span data-stu-id="93299-2065">Top</span></span></td>
<td><span data-ttu-id="93299-2066">コントロールの上揃えを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2066">Specify the top alignment of a control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2067">TopMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2067">TopMargin</span></span></td>
<td><span data-ttu-id="93299-2068">コントロールの余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2068">Specify the margin for a control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2069">種類</span><span class="sxs-lookup"><span data-stu-id="93299-2069">Type</span></span></td>
<td><span data-ttu-id="93299-2070">表示される図形のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2070">Specify the type of shape that is shown.</span></span> <span data-ttu-id="93299-2071">このプロパティは、シェイプ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2071">This property is available only for shape controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2072">TypeHeaderPrompt</span><span class="sxs-lookup"><span data-stu-id="93299-2072">TypeHeaderPrompt</span></span></td>
<td><span data-ttu-id="93299-2073">コントロール タイトルとコントロール値の間にスペースを入力するために点線を追加するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2073">Specify whether a line of dots is added to fill the space between the control title and the control value.</span></span> <span data-ttu-id="93299-2074">このプロパティは、テキストおよび確認でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2074">This property is available only for text and prompt controls.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2075">下線</span><span class="sxs-lookup"><span data-stu-id="93299-2075">Underline</span></span></td>
<td><span data-ttu-id="93299-2076">下線付きのテキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2076">Specify underline text formatting.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2077">表示</span><span class="sxs-lookup"><span data-stu-id="93299-2077">Visible</span></span></td>
<td><span data-ttu-id="93299-2078">コントロールが表示されるかどうかを示す値を設定するか返します。</span><span class="sxs-lookup"><span data-stu-id="93299-2078">Set or return a value that indicates whether the control is visible.</span></span> <span data-ttu-id="93299-2079"><strong>True</strong> の値は、コントロールが表示されていることを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-2079">A value of <strong>True</strong> indicates that the control is visible.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2080">WarnIfMissing</span><span class="sxs-lookup"><span data-stu-id="93299-2080">WarnIfMissing</span></span></td>
<td><span data-ttu-id="93299-2081">イメージがレポートに表示されない場合にメッセージを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2081">Specify whether a message is shown if an image is missing from the report.</span></span> <span data-ttu-id="93299-2082">このプロパティは、ビットマップ コントロールでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2082">This property is available only for bitmap controls.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2083">WebMenuItemName</span><span class="sxs-lookup"><span data-stu-id="93299-2083">WebMenuItemName</span></span></td>
<td><span data-ttu-id="93299-2084">Web メニューに含めるメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2084">Specify the menu item to include on a web menu.</span></span> <span data-ttu-id="93299-2085">使用可能な値は、<strong>WebMenuItemType</strong> プロパティの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-2085">The available values depend on the setting of the <strong>WebMenuItemType</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2086">WebMenuItemType</span><span class="sxs-lookup"><span data-stu-id="93299-2086">WebMenuItemType</span></span></td>
<td><span data-ttu-id="93299-2087">メニュー項目のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2087">Specify the type of the menu item.</span></span> <span data-ttu-id="93299-2088">Web メニュー項目には 2 つのカテゴリがあります。</span><span class="sxs-lookup"><span data-stu-id="93299-2088">There are two categories of web menu items:</span></span>
<ul>
<li><span data-ttu-id="93299-2089">URL</span><span class="sxs-lookup"><span data-stu-id="93299-2089">URL</span></span></li>
<li><span data-ttu-id="93299-2090">アクション</span><span class="sxs-lookup"><span data-stu-id="93299-2090">Action</span></span></li>
</ul>
<span data-ttu-id="93299-2091">選択した値によって、<strong>WebMenuItemName</strong> プロパティで使用可能な Web メニュー項目名が決まります。</span><span class="sxs-lookup"><span data-stu-id="93299-2091">The value that you select determines the web menu item names that are available for the <strong>WebMenuItemName</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2092">WebTarget</span><span class="sxs-lookup"><span data-stu-id="93299-2092">WebTarget</span></span></td>
<td><span data-ttu-id="93299-2093">Web レポートのコントロールの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2093">Specify the location of the control on a web report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2094">幅</span><span class="sxs-lookup"><span data-stu-id="93299-2094">Width</span></span></td>
<td><span data-ttu-id="93299-2095">コントロールの幅を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2095">Specify the width of a control.</span></span> <span data-ttu-id="93299-2096">コントロールが EDTに関連付けられている場合、その <strong>Width</strong> プロパティは EDT の <strong>DisplayLength</strong> プロパティを上書きします。</span><span class="sxs-lookup"><span data-stu-id="93299-2096">When a control is associated with an EDT, the <strong>Width</strong> property of the control overrides the <strong>DisplayLength</strong> property of the EDT.</span></span> <span data-ttu-id="93299-2097">ビットマップ コントロールの <strong>Width</strong> プロパティを<strong>自動</strong>に設定すると、コントロールのサイズは、グラフィックのサイズに基づきます。</span><span class="sxs-lookup"><span data-stu-id="93299-2097">If you set the <strong>Width</strong> property to <strong>Auto</strong> for a bitmap control, the size of the control is based on the size of the graphic.</span></span></td>
</tr>
</tbody>
</table>

## <a name="report-design-properties"></a><span data-ttu-id="93299-2098">レポート設計プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2098">Report design properties</span></span>
<span data-ttu-id="93299-2099">次のテーブルでは、レポート デザイン プロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2099">The following table describes the report design properties.</span></span>

| <span data-ttu-id="93299-2100">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2100">Property</span></span>                                   | <span data-ttu-id="93299-2101">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2101">Description</span></span>                                                                                                                                                                              |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-2102">ArrangeMethod</span><span class="sxs-lookup"><span data-stu-id="93299-2102">ArrangeMethod</span></span>                              | <span data-ttu-id="93299-2103">レポート セクションのコントロールのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2103">Specify the layout for the controls in a report section.</span></span>                                                                                                                                 |
| <span data-ttu-id="93299-2104">ArrangeWhen</span><span class="sxs-lookup"><span data-stu-id="93299-2104">ArrangeWhen</span></span>                                | <span data-ttu-id="93299-2105">レポート コントロールが配置されるタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2105">Specify when report controls are arranged.</span></span>                                                                                                                                               |
| <span data-ttu-id="93299-2106">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2106">BottomMargin</span></span>                               | <span data-ttu-id="93299-2107">下部の余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2107">Specify the bottom margin.</span></span> <span data-ttu-id="93299-2108">このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2108">If you set this property to **Auto**, the default value that is stored in the system table is used.</span></span>                                                           |
| <span data-ttu-id="93299-2109">キャプション</span><span class="sxs-lookup"><span data-stu-id="93299-2109">Caption</span></span>                                    | <span data-ttu-id="93299-2110">ユーザー インターフェイスのレポートに表示される名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2110">Specify the name that is shown for the report in the user interface.</span></span>                                                                                                                     |
| <span data-ttu-id="93299-2111">ColorScheme</span><span class="sxs-lookup"><span data-stu-id="93299-2111">ColorScheme</span></span>                                | <span data-ttu-id="93299-2112">カラー パレットを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2112">Specify the color palette.</span></span>                                                                                                                                                               |
| <span data-ttu-id="93299-2113">列</span><span class="sxs-lookup"><span data-stu-id="93299-2113">Columns</span></span>                                    | <span data-ttu-id="93299-2114">列の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2114">Specify the number of columns.</span></span>                                                                                                                                                           |
| <span data-ttu-id="93299-2115">ColumnSpace</span><span class="sxs-lookup"><span data-stu-id="93299-2115">ColumnSpace</span></span>                                | <span data-ttu-id="93299-2116">列の間のスペースを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2116">Specify the space between columns.</span></span>                                                                                                                                                       |
| <span data-ttu-id="93299-2117">フォント、フォントサイズ、斜体、下線および太字</span><span class="sxs-lookup"><span data-stu-id="93299-2117">Font, FontSize, Italic, Underline and Bold</span></span> | <span data-ttu-id="93299-2118">テキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2118">Specify the text formatting.</span></span> <span data-ttu-id="93299-2119">**ツール** メニューの **Options** &gt; **Fonts** をクリックすることで、**Font** プロパティおよび **FontSize** プロパティの設定は、設定する値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2119">The settings of the **Font** and **FontSize** properties override the values that you can set by clicking **Options** &gt; **Fonts** on the **Tools** menu.</span></span> |
| <span data-ttu-id="93299-2120">ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="93299-2120">ForegroundColor</span></span>                            | <span data-ttu-id="93299-2121">前景色を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2121">Specify the foreground color.</span></span>                                                                                                                                                            |
| <span data-ttu-id="93299-2122">高さ</span><span class="sxs-lookup"><span data-stu-id="93299-2122">Height</span></span>                                     | <span data-ttu-id="93299-2123">高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2123">Specify the height.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="93299-2124">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2124">LeftMargin</span></span>                                 | <span data-ttu-id="93299-2125">左余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2125">Specify the left margin.</span></span> <span data-ttu-id="93299-2126">このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2126">If you set this property to **Auto**, the default value that is stored in the system table is used.</span></span>                                                             |
| <span data-ttu-id="93299-2127">LineAbove</span><span class="sxs-lookup"><span data-stu-id="93299-2127">LineAbove</span></span>                                  | <span data-ttu-id="93299-2128">セクションの上の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2128">Specify the type of line for the top border of a section.</span></span> <span data-ttu-id="93299-2129">レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-2129">If a report has many lines and boxes, consider using the shape control inside a section.</span></span>                                       |
| <span data-ttu-id="93299-2130">LineBelow</span><span class="sxs-lookup"><span data-stu-id="93299-2130">LineBelow</span></span>                                  | <span data-ttu-id="93299-2131">セクションの下の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2131">Specify the type of line for the bottom border of a section.</span></span> <span data-ttu-id="93299-2132">レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-2132">If a report has many lines and boxes, consider using the shape control inside a section.</span></span>                                    |
| <span data-ttu-id="93299-2133">LineLeft</span><span class="sxs-lookup"><span data-stu-id="93299-2133">LineLeft</span></span>                                   | <span data-ttu-id="93299-2134">セクションの左の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2134">Specify the type of line for the left border of a section.</span></span> <span data-ttu-id="93299-2135">レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-2135">If a report has many lines and boxes, consider using the shape control inside a section.</span></span>                                      |
| <span data-ttu-id="93299-2136">LineRight</span><span class="sxs-lookup"><span data-stu-id="93299-2136">LineRight</span></span>                                  | <span data-ttu-id="93299-2137">セクションの右の境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2137">Specify the type of line for the right border of a section.</span></span> <span data-ttu-id="93299-2138">レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-2138">If a report has many lines and boxes, consider using the shape control inside a section.</span></span>                                     |
| <span data-ttu-id="93299-2139">ResolutionX、ResolutionY</span><span class="sxs-lookup"><span data-stu-id="93299-2139">ResolutionX, ResolutionY</span></span>                   | <span data-ttu-id="93299-2140">グリッド線間の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2140">Specify the distance between gridlines.</span></span>                                                                                                                                                  |
| <span data-ttu-id="93299-2141">RightMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2141">RightMargin</span></span>                                | <span data-ttu-id="93299-2142">右余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2142">Specify the right margin.</span></span> <span data-ttu-id="93299-2143">このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2143">If you set this property to **Auto**, the default value that is stored in the system table is used.</span></span>                                                            |
| <span data-ttu-id="93299-2144">ルーラー</span><span class="sxs-lookup"><span data-stu-id="93299-2144">Ruler</span></span>                                      | <span data-ttu-id="93299-2145">デザインを編集するときに表示されるルーラーの単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2145">Specify the unit for the ruler that is shown when you edit a design.</span></span> <span data-ttu-id="93299-2146">デザインを編集するには、**AutoDesignSpecs** または**生成されたデザイン** を右クリックし、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93299-2146">To edit a design, right-click **AutoDesignSpecs** or **Generated Design**, and then click **Edit**.</span></span>                 |
| <span data-ttu-id="93299-2147">太さ</span><span class="sxs-lookup"><span data-stu-id="93299-2147">Thickness</span></span>                                  | <span data-ttu-id="93299-2148">セクションの境界線の太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2148">Specify the thickness of a section border.</span></span>                                                                                                                                               |
| <span data-ttu-id="93299-2149">TopMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2149">TopMargin</span></span>                                  | <span data-ttu-id="93299-2150">上余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2150">Specify the top margin.</span></span> <span data-ttu-id="93299-2151">このプロパティを**自動**に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2151">If you set this property to **Auto**, the default value that is stored in the system table is used.</span></span>                                                              |

## <a name="report-design-section-properties"></a><span data-ttu-id="93299-2152">レポート設計セクション プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2152">Report design section properties</span></span>
<span data-ttu-id="93299-2153">次のテーブルでは、レポート デザイン セクションのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2153">The following table describes properties for report design sections.</span></span> <span data-ttu-id="93299-2154">レポートのデザインに使用される追加のプロパティの詳細については、「レポートのデザインのプロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-2154">For information about additional properties that are available for report designs, see the "Report design properties" section.</span></span>


|                 <span data-ttu-id="93299-2155">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2155">Property</span></span>                  |                                                                                                                                                                        <span data-ttu-id="93299-2156">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2156">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|               <span data-ttu-id="93299-2157">ArrangeMethod</span><span class="sxs-lookup"><span data-stu-id="93299-2157">ArrangeMethod</span></span>               |                                                                                                                                                 <span data-ttu-id="93299-2158">レポート セクションのコントロールのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2158">Specify the layout for the controls in a report section.</span></span>                                                                                                                                                  |
|                <span data-ttu-id="93299-2159">ArrangeWhen</span><span class="sxs-lookup"><span data-stu-id="93299-2159">ArrangeWhen</span></span>                |                                                                                        <span data-ttu-id="93299-2160">コンテナーのコントロールを配置するタイミングを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2160">Specify when the controls in the container should be arranged.</span></span> <span data-ttu-id="93299-2161"><strong>スタートアップ</strong>、<strong>オンデマンド</strong>、または <strong>なし</strong> を選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2161">The available options are <strong>Startup</strong>, <strong>On demand</strong>, and <strong>Never</strong>.</span></span>                                                                                         |
|                   <span data-ttu-id="93299-2162">太字</span><span class="sxs-lookup"><span data-stu-id="93299-2162">Bold</span></span>                    |                                                                                                                                       <span data-ttu-id="93299-2163">コントロールにテキストを表示するのに使用されたフォントの重量を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2163">Get or set the weight of the font that was used to show text in the control.</span></span>                                                                                                                                        |
|                  <span data-ttu-id="93299-2164">下</span><span class="sxs-lookup"><span data-stu-id="93299-2164">Bottom</span></span>                   |                                                                                                                                                     <span data-ttu-id="93299-2165">レポートの下部の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-2165">Change the position of the bottom of the report.</span></span>                                                                                                                                                      |
|               <span data-ttu-id="93299-2166">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2166">BottomMargin</span></span>                |                                                                                                   <span data-ttu-id="93299-2167">下部の余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2167">Specify the bottom margin.</span></span> <span data-ttu-id="93299-2168">このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2168">If you set this property to <strong>Auto</strong>, the default value that is stored in the UserInfo system table is used.</span></span>                                                                                                    |
|                <span data-ttu-id="93299-2169">ColorScheme</span><span class="sxs-lookup"><span data-stu-id="93299-2169">ColorScheme</span></span>                |                                                                                                                                                                <span data-ttu-id="93299-2170">カラー パレットを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2170">Specify the color palette.</span></span>                                                                                                                                                                 |
|          <span data-ttu-id="93299-2171">ColumnHeadingsStrategy</span><span class="sxs-lookup"><span data-stu-id="93299-2171">ColumnHeadingsStrategy</span></span>           | <span data-ttu-id="93299-2172">列見出しのレイアウトを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2172">Specify the layout of column headings.</span></span> <span data-ttu-id="93299-2173">このプロパティを <strong>WordWrap</strong> と設定すると、見出しは列の最長フィールドよりも長い場合にラップします。</span><span class="sxs-lookup"><span data-stu-id="93299-2173">If you set this property to <strong>WordWrap</strong>, a heading wraps when it's longer than the longest field in the column.</span></span> <span data-ttu-id="93299-2174">ヘッダーは、最大 8 つの明細行までラップできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2174">Headings can wrap to a maximum of eight lines.</span></span> <span data-ttu-id="93299-2175">8 つの明細行より長いヘッダーは切り詰められます。</span><span class="sxs-lookup"><span data-stu-id="93299-2175">Headings that are longer than eight lines are truncated.</span></span> <span data-ttu-id="93299-2176"><strong>注記:</strong> 言語によって、ヘッダーの長さが異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-2176"><strong>Note:</strong> The heading length varies, depending on the language.</span></span> |
|                  <span data-ttu-id="93299-2177">列</span><span class="sxs-lookup"><span data-stu-id="93299-2177">Columns</span></span>                  |                                                                                                                                                              <span data-ttu-id="93299-2178">列の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2178">Specify the number of columns.</span></span>                                                                                                                                                               |
|                <span data-ttu-id="93299-2179">Columnspace</span><span class="sxs-lookup"><span data-stu-id="93299-2179">Columnspace</span></span>                |                                                                                                                                                            <span data-ttu-id="93299-2180">列の間のスペースを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2180">Specify the space between columns.</span></span>                                                                                                                                                             |
|                   <span data-ttu-id="93299-2181">フォント</span><span class="sxs-lookup"><span data-stu-id="93299-2181">Font</span></span>                    |                                                       <span data-ttu-id="93299-2182">テキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2182">Specify the text formatting.</span></span> <span data-ttu-id="93299-2183"><strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2183">The settings of the <strong>Font</strong> and <strong>FontSize</strong> properties override the values that you can set by clicking <strong>Options **&gt; **Fonts</strong> on the <strong>Tools</strong> menu.</span></span>                                                        |
|                 <span data-ttu-id="93299-2184">フォントサイズ</span><span class="sxs-lookup"><span data-stu-id="93299-2184">FontSize</span></span>                  |                                                       <span data-ttu-id="93299-2185">テキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2185">Specify the text formatting.</span></span> <span data-ttu-id="93299-2186"><strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2186">The settings of the <strong>Font</strong> and <strong>FontSize</strong> properties override the values that you can set by clicking <strong>Options **&gt; **Fonts</strong> on the <strong>Tools</strong> menu.</span></span>                                                        |
|              <span data-ttu-id="93299-2187">ForegroundColor</span><span class="sxs-lookup"><span data-stu-id="93299-2187">ForegroundColor</span></span>              |                                                                                                                                                               <span data-ttu-id="93299-2188">前景色を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2188">Specify the foreground color.</span></span>                                                                                                                                                               |
|                <span data-ttu-id="93299-2189">GrandHeader</span><span class="sxs-lookup"><span data-stu-id="93299-2189">GrandHeader</span></span>                |                                                                          <span data-ttu-id="93299-2190"><strong>HeaderText</strong> プロパティの値が表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2190">Specify whether the value of the <strong>HeaderText</strong> property is shown.</span></span> <span data-ttu-id="93299-2191"><strong>GrandHeader</strong> プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2191">The <strong>GrandHeader</strong> property is available only when a report has multiple data sources that aren't nested.</span></span>                                                                          |
|                <span data-ttu-id="93299-2192">GrandTotal</span><span class="sxs-lookup"><span data-stu-id="93299-2192">GrandTotal</span></span>                 |                                                                          <span data-ttu-id="93299-2193"><strong>FooterText</strong> プロパティの値が表示されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2193">Specify whether the value of the <strong>FooterText</strong> property is shown.</span></span> <span data-ttu-id="93299-2194"><strong>GrandTotal</strong> プロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2194">The <strong>GrandTotal</strong> property is available only when a report has multiple data sources that aren't nested.</span></span>                                                                           |
|                <span data-ttu-id="93299-2195">HeaderText</span><span class="sxs-lookup"><span data-stu-id="93299-2195">HeaderText</span></span>                 |                                                       <span data-ttu-id="93299-2196"><strong>GrandHeader</strong> プロパティが <strong>Yes</strong> に設定されているとき、セクションの最初のレコードの上に表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2196">Specify the text that is shown above the first record in a section when the <strong>GrandHeader</strong> property is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="93299-2197">このプロパティは、レポートに複数のデータ ソースがネストされていない場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2197">This property is available only when a report has multiple data sources that aren't nested.</span></span>                                                       |
|                  <span data-ttu-id="93299-2198">高さ</span><span class="sxs-lookup"><span data-stu-id="93299-2198">Height</span></span>                   |                                                                                                                                                                    <span data-ttu-id="93299-2199">高さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2199">Specify the height.</span></span>                                                                                                                                                                    |
|                  <span data-ttu-id="93299-2200">斜体</span><span class="sxs-lookup"><span data-stu-id="93299-2200">Italic</span></span>                   |                                                       <span data-ttu-id="93299-2201">テキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2201">Specify the text formatting.</span></span> <span data-ttu-id="93299-2202"><strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2202">The settings of the <strong>Font</strong> and <strong>FontSize</strong> properties override the values that you can set by clicking <strong>Options **&gt; **Fonts</strong> on the <strong>Tools</strong> menu.</span></span>                                                        |
|     <span data-ttu-id="93299-2203">LabelTopMargin、LabelBottomMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2203">LabelTopMargin, LabelBottomMargin</span></span>     |                                                                                                                                                   <span data-ttu-id="93299-2204">列見出しの上下にある余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2204">Specify the margins above and below column headings.</span></span>                                                                                                                                                    |
|                <span data-ttu-id="93299-2205">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2205">LeftMargin</span></span>                 |                                                                                                    <span data-ttu-id="93299-2206">左余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2206">Specify the left margin.</span></span> <span data-ttu-id="93299-2207">このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2207">If you set this property to <strong>Auto</strong>, the default value that is stored in the UserInfo system table is used.</span></span>                                                                                                     |
| <span data-ttu-id="93299-2208">LineAbove、LineBelow、LineLeft、LineRight</span><span class="sxs-lookup"><span data-stu-id="93299-2208">LineAbove, LineBelow, LineLeft, LineRight</span></span> |                                                                                                          <span data-ttu-id="93299-2209">セクション境界線の線のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2209">Specify the type of line for a section border.</span></span> <span data-ttu-id="93299-2210">レポートに多くの明細行とボックスがある場合は、セクション内での図形管理の使用を検討します。</span><span class="sxs-lookup"><span data-stu-id="93299-2210">If a report has many lines and boxes, consider using the shape control inside a section.</span></span>                                                                                                          |
|                    <span data-ttu-id="93299-2211">マップ</span><span class="sxs-lookup"><span data-stu-id="93299-2211">Map</span></span>                    |                                                                   <span data-ttu-id="93299-2212">データの表示に使用するマップを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2212">Specify the map to use to show data.</span></span> <span data-ttu-id="93299-2213">マップ フィールドを 1 つまたは複数のテーブル内のフィールドに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2213">You can associate a map field with a field in one or more tables.</span></span> <span data-ttu-id="93299-2214">このプロパティを使用すると、同じフィールド名を使用して、異なるテーブルの異なる名前を持つフィールドにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2214">This property lets you use the same field name to access fields that have different names in different tables.</span></span>                                                                   |
|             <span data-ttu-id="93299-2215">NoOfHeadingLines</span><span class="sxs-lookup"><span data-stu-id="93299-2215">NoOfHeadingLines</span></span>              |                                         <span data-ttu-id="93299-2216">列見出しを表示するために使用される行数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2216">Specify the number of lines that are used to show column headings.</span></span> <span data-ttu-id="93299-2217">プロパティを <strong>0</strong> (ゼロ) に設定すると、列のヘッダーは表示されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2217">If you set the property to <strong>0</strong> (zero), column headings aren't displayed.</span></span> <span data-ttu-id="93299-2218">いくつかのフィールドを含むレポートでは、すべてのフィールドが表示されていることを確認する行の数を増やします。</span><span class="sxs-lookup"><span data-stu-id="93299-2218">For reports that include several fields, increase the number of lines to make sure that all fields are shown.</span></span>                                          |
|                <span data-ttu-id="93299-2219">RightMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2219">RightMargin</span></span>                |                                                                                                    <span data-ttu-id="93299-2220">右余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2220">Specify the right margin.</span></span> <span data-ttu-id="93299-2221">このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2221">If you set this property to <strong>Auto</strong>, the default value that is stored in the UserInfo system table is used.</span></span>                                                                                                    |
|                <span data-ttu-id="93299-2222">ResolutionX</span><span class="sxs-lookup"><span data-stu-id="93299-2222">ResolutionX</span></span>                |                                                                                                                                                          <span data-ttu-id="93299-2223">グリッド線間の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2223">Specify the distance between gridlines.</span></span>                                                                                                                                                          |
|                <span data-ttu-id="93299-2224">ResolutionY</span><span class="sxs-lookup"><span data-stu-id="93299-2224">ResolutionY</span></span>                |                                                                                                                                                          <span data-ttu-id="93299-2225">グリッド線間の間隔を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2225">Specify the distance between gridlines.</span></span>                                                                                                                                                          |
|                   <span data-ttu-id="93299-2226">ルーラー</span><span class="sxs-lookup"><span data-stu-id="93299-2226">Ruler</span></span>                   |                                                                      <span data-ttu-id="93299-2227">デザインを編集するときに表示されるルーラーの単位を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2227">Specify the unit for the ruler that is shown when you edit a design.</span></span> <span data-ttu-id="93299-2228">デザインを編集するには、<strong>AutoDesignSpecs</strong> または<strong>生成された</strong>デザイン を右クリックし、<strong>編集</strong> をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93299-2228">To edit a design, right-click <strong>AutoDesignSpecs</strong> or <strong>Generated</strong> Design, and then click <strong>Edit</strong>.</span></span>                                                                      |
|                   <span data-ttu-id="93299-2229">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2229">Table</span></span>                   |                                                                                                                                                          <span data-ttu-id="93299-2230">セクションのソース タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2230">Specify the data source for a section.</span></span>                                                                                                                                                           |
|                 <span data-ttu-id="93299-2231">太さ</span><span class="sxs-lookup"><span data-stu-id="93299-2231">Thickness</span></span>                 |                                                                                                                                                        <span data-ttu-id="93299-2232">セクションの境界線の太さを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2232">Specify the thickness of a section border.</span></span>                                                                                                                                                         |
|                    <span data-ttu-id="93299-2233">上</span><span class="sxs-lookup"><span data-stu-id="93299-2233">Top</span></span>                    |                                                                                                                                                       <span data-ttu-id="93299-2234">レポートの上部の位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-2234">Change the position of the top of the report.</span></span>                                                                                                                                                       |
|                 <span data-ttu-id="93299-2235">TopMargin</span><span class="sxs-lookup"><span data-stu-id="93299-2235">TopMargin</span></span>                 |                                                                                                     <span data-ttu-id="93299-2236">上余白を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2236">Specify the top margin.</span></span> <span data-ttu-id="93299-2237">このプロパティを<strong>自動</strong>に設定すると、UserInfo システム テーブルに格納されている既定値が使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2237">If you set this property to <strong>Auto</strong>, the default value that is stored in the UserInfo system table is used.</span></span>                                                                                                     |
|                 <span data-ttu-id="93299-2238">下線</span><span class="sxs-lookup"><span data-stu-id="93299-2238">Underline</span></span>                 |                                                       <span data-ttu-id="93299-2239">テキストの書式設定を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2239">Specify the text formatting.</span></span> <span data-ttu-id="93299-2240"><strong>ツール</strong> メニューの <strong>Options **&gt;**Fonts</strong> をクリックすることで、<strong>Font</strong> プロパティおよび <strong>FontSize</strong> プロパティの設定は、設定する値を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2240">The settings of the <strong>Font</strong> and <strong>FontSize</strong> properties override the values that you can set by clicking <strong>Options **&gt; **Fonts</strong> on the <strong>Tools</strong> menu.</span></span>                                                        |

## <a name="report-query-properties"></a><span data-ttu-id="93299-2241">レポート クエリ プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2241">Report query properties</span></span>
<span data-ttu-id="93299-2242">次のテーブルでは、レポート クエリのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2242">The following table describes report query properties.</span></span> <span data-ttu-id="93299-2243">追加のレポート プロパティの詳細については、「レポート プロパティ」および「システムと共通プロパティ」セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="93299-2243">For information about additional report properties, see the "Report properties" and "System and common properties" sections.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2244">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2244">Property</span></span></th>
<th><span data-ttu-id="93299-2245">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2245">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2246">AllowCheck</span><span class="sxs-lookup"><span data-stu-id="93299-2246">AllowCheck</span></span></td>
<td><span data-ttu-id="93299-2247">チェック フラグの許可を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2247">Get or set the Allow check flag.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2248">AllowCrossCompany</span><span class="sxs-lookup"><span data-stu-id="93299-2248">AllowCrossCompany</span></span></td>
<td><span data-ttu-id="93299-2249">会社間フラグの許可を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2249">Get or set the Allow cross-company flag.</span></span> <span data-ttu-id="93299-2250">このフラグは、クエリの実行が企業間で行われるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="93299-2250">This flag indicates whether query execution will be across companies.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2251">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2251">Description</span></span></td>
<td><span data-ttu-id="93299-2252">クエリのテキストの説明。</span><span class="sxs-lookup"><span data-stu-id="93299-2252">A textual explanation of the query.</span></span> <span data-ttu-id="93299-2253">このオプションのプロパティは、Office アドイン シナリオでよく使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2253">This optional property is often used in Office Add-ins scenarios.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2254">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2254">Form</span></span></td>
<td><span data-ttu-id="93299-2255">ユーザーの操作に使用されるフォームを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2255">Specify the form that is used for user interaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2256">対話型</span><span class="sxs-lookup"><span data-stu-id="93299-2256">Interactive</span></span></td>
<td><span data-ttu-id="93299-2257">ユーザーがクエリを区切る、プリンター オプションを設定するなどして、レポートを操作できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2257">Specify whether users can interact with the report by delimiting queries, setting printer options, and so on.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2258">リテラル</span><span class="sxs-lookup"><span data-stu-id="93299-2258">Literals</span></span></td>
<td><span data-ttu-id="93299-2259">SQL ステートメントでリテラルがどのような方法で表示されるかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2259">Specify how literals are represented in SQL statements.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2260">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-2260">Model</span></span></td>
<td><span data-ttu-id="93299-2261">レポート クエリがあるモデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2261">Specify the model that the report query is in.</span></span> <span data-ttu-id="93299-2262">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-2262">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-2263">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2263">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-2264">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-2264">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-2265">他の層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2265">The same element can exist in a customized version in a model that is in another layer.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2266">QueryType</span><span class="sxs-lookup"><span data-stu-id="93299-2266">QueryType</span></span></td>
<td><span data-ttu-id="93299-2267">クエリのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2267">Specify the type of the query.</span></span> <span data-ttu-id="93299-2268"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2268">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2269">結合</span><span class="sxs-lookup"><span data-stu-id="93299-2269">Join</span></span></li>
<li><span data-ttu-id="93299-2270">結合</span><span class="sxs-lookup"><span data-stu-id="93299-2270">Union</span></span></li>
</ul>
<span data-ttu-id="93299-2271">既定値は <strong>結合</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-2271">The default value is <strong>Join</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2272">検索可能</span><span class="sxs-lookup"><span data-stu-id="93299-2272">Searchable</span></span></td>
<td><span data-ttu-id="93299-2273">SharePoint Business Catalog を検索するために使用できる一連のクエリの一部としてクエリを使用できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2273">Specify whether the query can be part of a set of queries that can be used to search the SharePoint Business Catalog.</span></span> <span data-ttu-id="93299-2274">このプロパティは、エンタープライズ検索機能を使用する場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="93299-2274">This property is useful when you use the Enterprise Search feature.</span></span> <span data-ttu-id="93299-2275">既定値は <strong>いいえ</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-2275">The default value is <strong>No</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2276">肩書き</span><span class="sxs-lookup"><span data-stu-id="93299-2276">Title</span></span></td>
<td><span data-ttu-id="93299-2277">クエリのタイトルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2277">Specify the title of the query.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2278">UserUpdate</span><span class="sxs-lookup"><span data-stu-id="93299-2278">UserUpdate</span></span></td>
<td><span data-ttu-id="93299-2279">ユーザーがクエリを更新できるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2279">Specify whether users can update a query.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2280">バージョン</span><span class="sxs-lookup"><span data-stu-id="93299-2280">Version</span></span></td>
<td><span data-ttu-id="93299-2281">これは、読み取り専用の内部プロパティです。</span><span class="sxs-lookup"><span data-stu-id="93299-2281">This is a read-only internal property.</span></span></td>
</tr>
</tbody>
</table>

## <a name="security-code-permission-properties"></a><span data-ttu-id="93299-2282">セキュリティ コードに対するアクセス許可のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2282">Security code permission properties</span></span>
<span data-ttu-id="93299-2283">コード アクセス許可は、メニュー項目またはサービス操作に関連付けられたアクセス許可のグループです。</span><span class="sxs-lookup"><span data-stu-id="93299-2283">A code permission is a group of permissions that are associated with a menu item or a service operation.</span></span> <span data-ttu-id="93299-2284">セキュリティ ロールでメニュー項目にアクセスできるときは、そのロールで、そのメニュー項目に対してコードのアクセス許可の範囲内で記載された他のアプリケーション エクスプ ローラーの品目にもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2284">When a security role has access to a menu item, it also has access to other Application Explorer items that are mentioned within the code permission for that menu item.</span></span> <span data-ttu-id="93299-2285">アクセスの程度は、コード許可ノードで定義されている特定のアクセス許可によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2285">The degree of access is controlled by the specific permissions that are defined under the code permission node.</span></span>

### <a name="securable-objects"></a><span data-ttu-id="93299-2286">セキュリティ設定が可能なオブジェクト</span><span class="sxs-lookup"><span data-stu-id="93299-2286">Securable objects</span></span>

<span data-ttu-id="93299-2287">コードに対するアクセス許可は、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2287">Code permissions are used to give access to securable objects.</span></span> <span data-ttu-id="93299-2288">次のリストは、アプリケーション エクスプローラーのコード アクセス許可の階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2288">The following list shows the hierarchy of code permission nodes in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2289">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2289">Security</span></span>
    -   <span data-ttu-id="93299-2290">コードに対するアクセス許可</span><span class="sxs-lookup"><span data-stu-id="93299-2290">Code Permissions</span></span>
        -   <span data-ttu-id="93299-2291">YourCodePermission</span><span class="sxs-lookup"><span data-stu-id="93299-2291">YourCodePermission</span></span>
            -   <span data-ttu-id="93299-2292">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2292">Tables</span></span>
            -   <span data-ttu-id="93299-2293">サーバー メソッド</span><span class="sxs-lookup"><span data-stu-id="93299-2293">Server Methods</span></span>
            -   <span data-ttu-id="93299-2294">関連付けられたオブジェクト</span><span class="sxs-lookup"><span data-stu-id="93299-2294">Associated Objects</span></span>
                -   <span data-ttu-id="93299-2295">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2295">Forms</span></span>
                -   <span data-ttu-id="93299-2296">Web コントロール</span><span class="sxs-lookup"><span data-stu-id="93299-2296">Web Controls</span></span>
                -   <span data-ttu-id="93299-2297">レポート</span><span class="sxs-lookup"><span data-stu-id="93299-2297">Reports</span></span>

<span data-ttu-id="93299-2298">コード権限は、**関連付けられたオブジェクト** ノードの下でセキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2298">Code permissions can also override the access levels to securable objects under the **Associated Objects** node.</span></span>

### <a name="code-permission-properties"></a><span data-ttu-id="93299-2299">コードに対するアクセス許可のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2299">Code permission properties</span></span>

<span data-ttu-id="93299-2300">次の表は、Application Explorer の**セキュリティ** &gt; **コード パーミッション** &gt; **YourCodePermission** のノードのプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2300">This following table describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** in Application Explorer.</span></span>

| <span data-ttu-id="93299-2301">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2301">Property</span></span> | <span data-ttu-id="93299-2302">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2302">Required</span></span> | <span data-ttu-id="93299-2303">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2303">Description</span></span>                                                                                                                        |
|----------|----------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93299-2304">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2304">Name</span></span>     | <span data-ttu-id="93299-2305">有</span><span class="sxs-lookup"><span data-stu-id="93299-2305">Yes</span></span>      | <span data-ttu-id="93299-2306">コードに対するアクセス許可の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2306">The name of the code permission.</span></span> <span data-ttu-id="93299-2307">コードのアクセス許可を使用すると、**メソッド** プロパティで指定されたクラス メソッドを実行できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2307">The code permission lets users run the class method that is specified in the **Method** property.</span></span> |
| <span data-ttu-id="93299-2308">クラス</span><span class="sxs-lookup"><span data-stu-id="93299-2308">Class</span></span>    | <span data-ttu-id="93299-2309">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2309">Optional</span></span> | <span data-ttu-id="93299-2310">このコードに対するアクセス許可に関連付けられているクラス。</span><span class="sxs-lookup"><span data-stu-id="93299-2310">The class that is associated with this code permission.</span></span>                                                                            |
| <span data-ttu-id="93299-2311">方法</span><span class="sxs-lookup"><span data-stu-id="93299-2311">Method</span></span>   | <span data-ttu-id="93299-2312">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2312">Optional</span></span> | <span data-ttu-id="93299-2313">このコードに対するアクセス許可に関連付けられているメソッド。</span><span class="sxs-lookup"><span data-stu-id="93299-2313">The method that is associated with this code permission.</span></span>                                                                           |

### <a name="table-properties"></a><span data-ttu-id="93299-2314">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2314">Table properties</span></span>

<span data-ttu-id="93299-2315">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2315">The following table describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Tables** &gt; **YourTable** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2316">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2316">Property</span></span></th>
<th><span data-ttu-id="93299-2317">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2317">Required</span></span></th>
<th><span data-ttu-id="93299-2318">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2318">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2319">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2319">Table</span></span></td>
<td><span data-ttu-id="93299-2320">有</span><span class="sxs-lookup"><span data-stu-id="93299-2320">Yes</span></span></td>
<td><span data-ttu-id="93299-2321">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2321">The name of the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2322">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2322">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2323">有</span><span class="sxs-lookup"><span data-stu-id="93299-2323">Yes</span></span></td>
<td><span data-ttu-id="93299-2324">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2324">The permission value.</span></span> <span data-ttu-id="93299-2325"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2325">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2326">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2326">Read</span></span></li>
<li><span data-ttu-id="93299-2327">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2327">Update</span></span></li>
<li><span data-ttu-id="93299-2328">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2328">Create</span></span></li>
<li><span data-ttu-id="93299-2329">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2329">Correct</span></span></li>
<li><span data-ttu-id="93299-2330">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2330">Delete</span></span></li>
<li><span data-ttu-id="93299-2331">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2331">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2332"><strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2332">The permission values for the <strong>EffectiveAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2333">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2333">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2334">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2334">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2335">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2335">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2336">アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2336">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2337">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2337">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2338">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2338">Optional</span></span></td>
<td><span data-ttu-id="93299-2339">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2339">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="server-method-properties"></a><span data-ttu-id="93299-2340">サーバー メソッド プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2340">Server method properties</span></span>

<span data-ttu-id="93299-2341">次のテーブルでは、アプリケーション エクスプローラーの **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Server Methods** &gt; **YourServerMethod** でのノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2341">The following tables describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Server Methods** &gt; **YourServerMethod** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2342">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2342">Property</span></span></th>
<th><span data-ttu-id="93299-2343">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2343">Required</span></span></th>
<th><span data-ttu-id="93299-2344">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2344">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2345">クラス</span><span class="sxs-lookup"><span data-stu-id="93299-2345">Class</span></span></td>
<td><span data-ttu-id="93299-2346">有</span><span class="sxs-lookup"><span data-stu-id="93299-2346">Yes</span></span></td>
<td><span data-ttu-id="93299-2347">サーバー クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2347">The name of the server class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2348">方法</span><span class="sxs-lookup"><span data-stu-id="93299-2348">Method</span></span></td>
<td><span data-ttu-id="93299-2349">有</span><span class="sxs-lookup"><span data-stu-id="93299-2349">Yes</span></span></td>
<td><span data-ttu-id="93299-2350"><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッド。</span><span class="sxs-lookup"><span data-stu-id="93299-2350">The secure server method that is tagged with the <strong>SysEntryPointAttribute</strong> attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2351">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2351">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2352">有</span><span class="sxs-lookup"><span data-stu-id="93299-2352">Yes</span></span></td>
<td><span data-ttu-id="93299-2353">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2353">The permission value.</span></span> <span data-ttu-id="93299-2354"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2354">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2355"><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2355"><strong>Invoke</strong> – The server method can be called.</span></span></li>
<li><span data-ttu-id="93299-2356"><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="93299-2356"><strong>NoAccess</strong> – The server method can&#39;t be called.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2357">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2357">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2358">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2358">Optional</span></span></td>
<td><span data-ttu-id="93299-2359">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2359">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a><span data-ttu-id="93299-2360">フォーム プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2360">Form properties</span></span>

<span data-ttu-id="93299-2361">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2361">The following table describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Associated Objects** &gt; **Forms** &gt; **YourForm** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2362">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2362">Property</span></span></th>
<th><span data-ttu-id="93299-2363">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2363">Required</span></span></th>
<th><span data-ttu-id="93299-2364">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2365">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2365">Form</span></span></td>
<td><span data-ttu-id="93299-2366">有</span><span class="sxs-lookup"><span data-stu-id="93299-2366">Yes</span></span></td>
<td><span data-ttu-id="93299-2367">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2367">The name of the form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2368">AccessLevel</span><span class="sxs-lookup"><span data-stu-id="93299-2368">AccessLevel</span></span></td>
<td><span data-ttu-id="93299-2369">有</span><span class="sxs-lookup"><span data-stu-id="93299-2369">Yes</span></span></td>
<td><span data-ttu-id="93299-2370">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2370">The permission value.</span></span> <span data-ttu-id="93299-2371"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2371">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2372">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2372">Read</span></span></li>
<li><span data-ttu-id="93299-2373">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2373">Update</span></span></li>
<li><span data-ttu-id="93299-2374">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2374">Create</span></span></li>
<li><span data-ttu-id="93299-2375">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2375">Correct</span></span></li>
<li><span data-ttu-id="93299-2376">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2376">Delete</span></span></li>
<li><span data-ttu-id="93299-2377">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2377">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2378"><strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2378">The permission values for the <strong>EffectiveAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2379">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2379">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2380">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2380">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2381">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2381">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2382">アクセス許可の値を <strong>NoAccess</strong> に設定すると、フォームに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2382">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2383">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2383">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2384">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2384">Optional</span></span></td>
<td><span data-ttu-id="93299-2385">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2385">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="web-control-properties"></a><span data-ttu-id="93299-2386">Web コントロールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2386">Web control properties</span></span>

<span data-ttu-id="93299-2387">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **Web コントロール** &gt; **YourWebControl** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2387">The following table describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Associated Objects** &gt; **Web Controls** &gt; **YourWebControl** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2388">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2388">Property</span></span></th>
<th><span data-ttu-id="93299-2389">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2389">Required</span></span></th>
<th><span data-ttu-id="93299-2390">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2390">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2391">WebControl</span><span class="sxs-lookup"><span data-stu-id="93299-2391">WebControl</span></span></td>
<td><span data-ttu-id="93299-2392">有</span><span class="sxs-lookup"><span data-stu-id="93299-2392">Yes</span></span></td>
<td><span data-ttu-id="93299-2393">Web コントロールの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2393">The name of the web control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2394">AccessLevel</span><span class="sxs-lookup"><span data-stu-id="93299-2394">AccessLevel</span></span></td>
<td><span data-ttu-id="93299-2395">有</span><span class="sxs-lookup"><span data-stu-id="93299-2395">Yes</span></span></td>
<td><span data-ttu-id="93299-2396">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2396">The permission value.</span></span> <span data-ttu-id="93299-2397"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2397">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2398">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2398">Read</span></span></li>
<li><span data-ttu-id="93299-2399">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2399">Update</span></span></li>
<li><span data-ttu-id="93299-2400">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2400">Create</span></span></li>
<li><span data-ttu-id="93299-2401">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2401">Correct</span></span></li>
<li><span data-ttu-id="93299-2402">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2402">Delete</span></span></li>
<li><span data-ttu-id="93299-2403">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2403">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2404"><strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2404">The permission values for the <strong>EffectiveAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2405">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2405">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2406">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2406">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2407">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2407">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2408">アクセス許可の値を <strong>NoAccess</strong> に設定すると、Web コントロールに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2408">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the web control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2409">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2409">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2410">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2410">Optional</span></span></td>
<td><span data-ttu-id="93299-2411">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2411">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="report-properties"></a><span data-ttu-id="93299-2412">レポート プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2412">Report properties</span></span>

<span data-ttu-id="93299-2413">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **コードに対するアクセス許可** &gt; **YourCodePermission** &gt; **関連付けられたオブジェクト** &gt; **レポート** &gt; **YourReport** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2413">The following table describes the properties for the node at **Security** &gt; **Code Permissions** &gt; **YourCodePermission** &gt; **Associated Objects** &gt; **Reports** &gt; **YourReport** in Application Explorer.</span></span>

| <span data-ttu-id="93299-2414">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2414">Property</span></span>  | <span data-ttu-id="93299-2415">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2415">Required</span></span> | <span data-ttu-id="93299-2416">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2416">Description</span></span>                                |
|-----------|----------|--------------------------------------------|
| <span data-ttu-id="93299-2417">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2417">Name</span></span>      | <span data-ttu-id="93299-2418">有</span><span class="sxs-lookup"><span data-stu-id="93299-2418">Yes</span></span>      | <span data-ttu-id="93299-2419">レポート デザインの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2419">The name of the report design.</span></span>             |
| <span data-ttu-id="93299-2420">レポート </span><span class="sxs-lookup"><span data-stu-id="93299-2420">Report</span></span>    | <span data-ttu-id="93299-2421">有</span><span class="sxs-lookup"><span data-stu-id="93299-2421">Yes</span></span>      | <span data-ttu-id="93299-2422">レポートのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="93299-2422">The full name of the report.</span></span>               |
| <span data-ttu-id="93299-2423">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2423">ManagedBy</span></span> | <span data-ttu-id="93299-2424">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2424">Optional</span></span> | <span data-ttu-id="93299-2425">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2425">This property is used by automation tools.</span></span> |

## <a name="security-duty-properties"></a><span data-ttu-id="93299-2426">セキュリティ職務権限のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2426">Security duty properties</span></span>
<span data-ttu-id="93299-2427">セキュリティ アクセス許可は特権に、特権は職務に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="93299-2427">Security permissions are combined into privileges, and privileges are combined into duties.</span></span> <span data-ttu-id="93299-2428">職務は、ユーザーに特定のビジネス機能へのアクセスを提供する関連特権のグループとして定義されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2428">Duties are defined as groups of related privileges that provide a user with access to a specific business function.</span></span> <span data-ttu-id="93299-2429">アプリケーション エクスプローラーでは、これらの権限は職務権限のノードにまとめられます。</span><span class="sxs-lookup"><span data-stu-id="93299-2429">In Application Explorer, these privileges are organized into the nodes of a duty.</span></span>

### <a name="best-practices"></a><span data-ttu-id="93299-2430">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="93299-2430">Best practices</span></span>

<span data-ttu-id="93299-2431">このセクションでは、職務のベスト プラクティス ルールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2431">This section describes the best practice rules for duties.</span></span>

-   <span data-ttu-id="93299-2432">すべての職務はロールに割り当てられるべきです。</span><span class="sxs-lookup"><span data-stu-id="93299-2432">All duties should be assigned to a role.</span></span>
-   <span data-ttu-id="93299-2433">すべての職務はプロセス サイクルの一部であるべきです。</span><span class="sxs-lookup"><span data-stu-id="93299-2433">All duties should be part of a process cycle.</span></span>
-   <span data-ttu-id="93299-2434">職務権限は特定のビジネス機能を表すため、職務権限の名前はほとんど変わりません。</span><span class="sxs-lookup"><span data-stu-id="93299-2434">Because a duty represents a specific business function, the name of the duty should rarely or never change.</span></span> <span data-ttu-id="93299-2435">たとえば、会社が請求の支払いをします。</span><span class="sxs-lookup"><span data-stu-id="93299-2435">For example, your company pays bills.</span></span> <span data-ttu-id="93299-2436">請求書の支払方法の詳細は変更する可能性がありますが、請求書支払いの重要な機能は変更されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2436">Although the details of how you pay bills might change, the essential function of paying bills won't change.</span></span> <span data-ttu-id="93299-2437">新しい職務を作成する代わりに、職務の権限サブノードを変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-2437">Instead of creating a new duty, you should change the privilege subnodes of the duty.</span></span>
-   <span data-ttu-id="93299-2438">プロセス サイクルの名前はほとんど変わりません。</span><span class="sxs-lookup"><span data-stu-id="93299-2438">The name of a process cycle should rarely or never change.</span></span>

### <a name="duty-hierarchy-in-application-explorer"></a><span data-ttu-id="93299-2439">アプリケーション エクスプ ローラーの職務階層</span><span class="sxs-lookup"><span data-stu-id="93299-2439">Duty hierarchy in Application Explorer</span></span>

<span data-ttu-id="93299-2440">次のリストは、アプリケーション エクスプローラーの職務権限のノードの階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2440">The following list shows the hierarchy of duty nodes in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2441">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2441">Security</span></span>
    -   <span data-ttu-id="93299-2442">職務権限</span><span class="sxs-lookup"><span data-stu-id="93299-2442">Duties</span></span>
        -   <span data-ttu-id="93299-2443">YourDuty</span><span class="sxs-lookup"><span data-stu-id="93299-2443">YourDuty</span></span>
            -   <span data-ttu-id="93299-2444">権限</span><span class="sxs-lookup"><span data-stu-id="93299-2444">Privileges</span></span>

### <a name="duty-properties"></a><span data-ttu-id="93299-2445">職務プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2445">Duty properties</span></span>

<span data-ttu-id="93299-2446">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2446">The following table describes the properties for the node at **Security** &gt; **Duties** &gt; **YourDuty** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2447">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2447">Property</span></span></th>
<th><span data-ttu-id="93299-2448">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2448">Required</span></span></th>
<th><span data-ttu-id="93299-2449">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2449">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2450">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2450">Name</span></span></td>
<td><span data-ttu-id="93299-2451">有</span><span class="sxs-lookup"><span data-stu-id="93299-2451">Yes</span></span></td>
<td><span data-ttu-id="93299-2452">職務権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2452">The name of the duty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2453">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2453">Label</span></span></td>
<td><span data-ttu-id="93299-2454">有</span><span class="sxs-lookup"><span data-stu-id="93299-2454">Yes</span></span></td>
<td><span data-ttu-id="93299-2455">ユーザー インターフェイスの職務権限で表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="93299-2455">Text that is shown for the duty in the user interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2456">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2456">Description</span></span></td>
<td><span data-ttu-id="93299-2457">有</span><span class="sxs-lookup"><span data-stu-id="93299-2457">Yes</span></span></td>
<td><span data-ttu-id="93299-2458">職務権限の説明。</span><span class="sxs-lookup"><span data-stu-id="93299-2458">A description of the duty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2459">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2459">Enabled</span></span></td>
<td><span data-ttu-id="93299-2460">有</span><span class="sxs-lookup"><span data-stu-id="93299-2460">Yes</span></span></td>
<td><span data-ttu-id="93299-2461">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2461">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2462"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2462">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2463"><strong>はい</strong> - 職務権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2463"><strong>Yes</strong> – Enable the duty.</span></span></li>
<li><span data-ttu-id="93299-2464"><strong>いいえ</strong> - 関税を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2464"><strong>No</strong> – Disable the duty.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="privilege-properties"></a><span data-ttu-id="93299-2465">権限のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2465">Privilege properties</span></span>

<span data-ttu-id="93299-2466">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **職務権限** &gt; **YourDuty** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2466">The following table describes the properties for the node at **Security** &gt; **Duties** &gt; **YourDuty** &gt; **Privileges** &gt; **YourPrivilege** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2467">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2467">Property</span></span></th>
<th><span data-ttu-id="93299-2468">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2468">Required</span></span></th>
<th><span data-ttu-id="93299-2469">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2469">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2470">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2470">Name</span></span></td>
<td><span data-ttu-id="93299-2471">有</span><span class="sxs-lookup"><span data-stu-id="93299-2471">Yes</span></span></td>
<td><span data-ttu-id="93299-2472">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2472">The name of the privilege.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2473">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2473">Enabled</span></span></td>
<td><span data-ttu-id="93299-2474">有</span><span class="sxs-lookup"><span data-stu-id="93299-2474">Yes</span></span></td>
<td><span data-ttu-id="93299-2475">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2475">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2476"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2476">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2477"><strong>はい</strong> - 権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2477"><strong>Yes</strong> – Enable the privilege.</span></span></li>
<li><span data-ttu-id="93299-2478"><strong>いいえ</strong> - 権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2478"><strong>No</strong> – Disable the privilege.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="security-privilege-properties"></a><span data-ttu-id="93299-2479">セキュリティ権限のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2479">Security privilege properties</span></span>
<span data-ttu-id="93299-2480">権限は、アクセス許可のグループです。</span><span class="sxs-lookup"><span data-stu-id="93299-2480">A privilege is a group of permissions.</span></span> <span data-ttu-id="93299-2481">各権限ノードの下にあるノードは、ユーザーがアクセスできるセキュリティ保護可能オブジェクトを識別し、各オブジェクトのアクセス レベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2481">The nodes that are below each privilege node identify the securable objects that a user can access and set the level of access for each object.</span></span>

### <a name="best-practices"></a><span data-ttu-id="93299-2482">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="93299-2482">Best practices</span></span>

<span data-ttu-id="93299-2483">このセクションでは、権限のベスト プラクティス ルールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2483">This section describes the best practice rules for privileges.</span></span>

-   <span data-ttu-id="93299-2484">特権を使用すると、ジョブを実行するために必要なアクセス特権を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2484">You can use privileges to specify the access that is required in order to perform a job.</span></span>
-   <span data-ttu-id="93299-2485">特権を使用すると、関連するセキュリティ保護可能なオブジェクトのアクセス許可をグループ化することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2485">You can use privileges to group the permissions for related securable objects.</span></span> <span data-ttu-id="93299-2486">たとえば、メニュー項目およびそのコントロールは密接に関係しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2486">For example, menu items and their controls are closely related.</span></span>
-   <span data-ttu-id="93299-2487">権限はセキュリティ ロールに直接割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2487">You can assign privileges directly to security roles.</span></span> <span data-ttu-id="93299-2488">ただし、特権ではなく職務またはプロセス サイクルを割り当てると、セキュリティ設定が管理しやすくなります。</span><span class="sxs-lookup"><span data-stu-id="93299-2488">However, security settings are easier to maintain if you assign duties or process cycles instead of privileges.</span></span>

### <a name="securable-objects"></a><span data-ttu-id="93299-2489">セキュリティ設定が可能なオブジェクト</span><span class="sxs-lookup"><span data-stu-id="93299-2489">Securable objects</span></span>

<span data-ttu-id="93299-2490">権限は、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2490">Privileges are used to give access to securable objects.</span></span> <span data-ttu-id="93299-2491">以下のリストは、アプリケーション エクスプローラーの **セキュリティ** &gt; **特権** ノードの下の階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2491">The following list shows the hierarchy under the **Security** &gt; **Privileges** node in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2492">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2492">Security</span></span>
    -   <span data-ttu-id="93299-2493">権限</span><span class="sxs-lookup"><span data-stu-id="93299-2493">Privileges</span></span>
        -   <span data-ttu-id="93299-2494">YourPrivilege</span><span class="sxs-lookup"><span data-stu-id="93299-2494">YourPrivilege</span></span>
            -   <span data-ttu-id="93299-2495">エントリ ポイント</span><span class="sxs-lookup"><span data-stu-id="93299-2495">Entry Points</span></span>
            -   <span data-ttu-id="93299-2496">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="93299-2496">Permissions</span></span>
                -   <span data-ttu-id="93299-2497">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2497">Tables</span></span>
                -   <span data-ttu-id="93299-2498">サーバー メソッド</span><span class="sxs-lookup"><span data-stu-id="93299-2498">Server Methods</span></span>
                -   <span data-ttu-id="93299-2499">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2499">Forms</span></span>

<span data-ttu-id="93299-2500">権限は、アプリケーション エクスプローラーの他の場所で定義されているとおりに、セキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2500">Privileges can also override the access levels to securable objects as they are defined elsewhere in Application Explorer.</span></span> <span data-ttu-id="93299-2501">たとえば、権限は、アプリケーション エクスプローラーの**フォーム** &gt; **YourForm** &gt; **アクセス許可** &gt; **更新** &gt; **テーブル** &gt; **YourTable** の下で、**EffectiveAccess** プロパティにより定義されるアクセス許可を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2501">For example, a privilege can override a permission that is defined by the **EffectiveAccess** property under **Forms** &gt; **YourForm** &gt; **Permissions** &gt; **Update** &gt; **Tables** &gt; **YourTable** in Application Explorer.</span></span>

### <a name="privilege-properties"></a><span data-ttu-id="93299-2502">権限のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2502">Privilege properties</span></span>

<span data-ttu-id="93299-2503">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2503">The following table describes the properties for the node at **Security** &gt; **Privileges** &gt; **YourPrivilege** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2504">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2504">Property</span></span></th>
<th><span data-ttu-id="93299-2505">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2505">Required</span></span></th>
<th><span data-ttu-id="93299-2506">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2506">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2507">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2507">Name</span></span></td>
<td><span data-ttu-id="93299-2508">有</span><span class="sxs-lookup"><span data-stu-id="93299-2508">Yes</span></span></td>
<td><span data-ttu-id="93299-2509">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2509">The name of the privilege.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2510">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2510">Label</span></span></td>
<td><span data-ttu-id="93299-2511">有</span><span class="sxs-lookup"><span data-stu-id="93299-2511">Yes</span></span></td>
<td><span data-ttu-id="93299-2512">ユーザー インターフェイスの権限で表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="93299-2512">Text that is shown for the privilege in the user interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2513">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2513">Description</span></span></td>
<td><span data-ttu-id="93299-2514">有</span><span class="sxs-lookup"><span data-stu-id="93299-2514">Yes</span></span></td>
<td><span data-ttu-id="93299-2515">権限の説明。</span><span class="sxs-lookup"><span data-stu-id="93299-2515">A description of the privilege.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2516">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2516">Enabled</span></span></td>
<td><span data-ttu-id="93299-2517">有</span><span class="sxs-lookup"><span data-stu-id="93299-2517">Yes</span></span></td>
<td><span data-ttu-id="93299-2518">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2518">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2519"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2519">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2520"><strong>はい</strong> - 権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2520"><strong>Yes</strong> – Enable the privilege.</span></span></li>
<li><span data-ttu-id="93299-2521"><strong>いいえ</strong> - 権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2521"><strong>No</strong> – Disable the privilege.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="entry-point-properties"></a><span data-ttu-id="93299-2522">エントリ ポイント プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2522">Entry point properties</span></span>

<span data-ttu-id="93299-2523">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **エントリ** **ポイント** &gt; **YourEntryPoint** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2523">The following table describes the properties for the node at **Security** &gt; **Privileges** &gt; **YourPrivilege** &gt; **Entry** **Points** &gt; **YourEntryPoint** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2524">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2524">Property</span></span></th>
<th><span data-ttu-id="93299-2525">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2525">Required</span></span></th>
<th><span data-ttu-id="93299-2526">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2526">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2527">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2527">Name</span></span></td>
<td><span data-ttu-id="93299-2528">有</span><span class="sxs-lookup"><span data-stu-id="93299-2528">Yes</span></span></td>
<td><span data-ttu-id="93299-2529">エントリ ポイントの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2529">The name of the entry point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2530">ObjectType</span><span class="sxs-lookup"><span data-stu-id="93299-2530">ObjectType</span></span></td>
<td><span data-ttu-id="93299-2531">有</span><span class="sxs-lookup"><span data-stu-id="93299-2531">Yes</span></span></td>
<td><span data-ttu-id="93299-2532">エントリ ポイントのオブジェクト タイプ。</span><span class="sxs-lookup"><span data-stu-id="93299-2532">The object type of the entry point.</span></span> <span data-ttu-id="93299-2533"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2533">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2534">MenuItemDisplay</span><span class="sxs-lookup"><span data-stu-id="93299-2534">MenuItemDisplay</span></span></li>
<li><span data-ttu-id="93299-2535">MenuItemOutput</span><span class="sxs-lookup"><span data-stu-id="93299-2535">MenuItemOutput</span></span></li>
<li><span data-ttu-id="93299-2536">MenuItemAction</span><span class="sxs-lookup"><span data-stu-id="93299-2536">MenuItemAction</span></span></li>
<li><span data-ttu-id="93299-2537">ServiceOperation</span><span class="sxs-lookup"><span data-stu-id="93299-2537">ServiceOperation</span></span></li>
<li><span data-ttu-id="93299-2538">WebActionItem</span><span class="sxs-lookup"><span data-stu-id="93299-2538">WebActionItem</span></span></li>
<li><span data-ttu-id="93299-2539">WebURLItem</span><span class="sxs-lookup"><span data-stu-id="93299-2539">WebURLItem</span></span></li>
<li><span data-ttu-id="93299-2540">WebManagedContent</span><span class="sxs-lookup"><span data-stu-id="93299-2540">WebManagedContent</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2541">ObjectName</span><span class="sxs-lookup"><span data-stu-id="93299-2541">ObjectName</span></span></td>
<td><span data-ttu-id="93299-2542">有</span><span class="sxs-lookup"><span data-stu-id="93299-2542">Yes</span></span></td>
<td><span data-ttu-id="93299-2543">エントリ ポイントのオブジェクト名。</span><span class="sxs-lookup"><span data-stu-id="93299-2543">The object name of the entry point.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2544">ObjectChildName</span><span class="sxs-lookup"><span data-stu-id="93299-2544">ObjectChildName</span></span></td>
<td><span data-ttu-id="93299-2545">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2545">Optional</span></span></td>
<td><span data-ttu-id="93299-2546">サービス メソッド名を表す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2546">A value that represents the service method name.</span></span> <span data-ttu-id="93299-2547"><strong>注記:</strong> <strong>ObjectType</strong> プロパティが <strong>ServiceOperation</strong> に設定されている場合にのみ、このプロパティの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2547"><strong>Note:</strong> Specify a value for this property only if the <strong>ObjectType</strong> property is set to <strong>ServiceOperation</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2548">AccessLevel</span><span class="sxs-lookup"><span data-stu-id="93299-2548">AccessLevel</span></span></td>
<td><span data-ttu-id="93299-2549">有</span><span class="sxs-lookup"><span data-stu-id="93299-2549">Yes</span></span></td>
<td><span data-ttu-id="93299-2550">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2550">The permission value.</span></span> <span data-ttu-id="93299-2551"><strong>ServiceOperation</strong> を除くすべてのオブジェクト タイプに関しては、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2551">For all object types except <strong>ServiceOperation</strong>, the following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2552">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2552">Read</span></span></li>
<li><span data-ttu-id="93299-2553">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2553">Update</span></span></li>
<li><span data-ttu-id="93299-2554">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2554">Create</span></span></li>
<li><span data-ttu-id="93299-2555">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2555">Correct</span></span></li>
<li><span data-ttu-id="93299-2556">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2556">Delete</span></span></li>
<li><span data-ttu-id="93299-2557">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2557">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2558"><strong>AccessLevel</strong>プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2558">The permission values for the <strong>AccessLevel</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2559">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2559">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2560">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2560">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2561">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2561">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2562">アクセス許可の値を <strong>NoAccess</strong> に設定すると、エントリ ポイントに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2562">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the entry point.</span></span> <span data-ttu-id="93299-2563">修正アクセス許可は、時間状態テーブルが関係する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2563">The Correct permission applies only when a time state table is involved.</span></span> <span data-ttu-id="93299-2564">このアクセス許可は、時間状態テーブルで更新レコードを発行する権限を与えます。</span><span class="sxs-lookup"><span data-stu-id="93299-2564">This permission authorizes you to issue update records in a time state table.</span></span> <span data-ttu-id="93299-2565"><strong>ServiceOperation</strong> オブジェクト タイプに関しては、次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2565">For the <strong>ServiceOperation</strong> object type, the following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2566"><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2566"><strong>Invoke</strong> – The server method can be called.</span></span></li>
<li><span data-ttu-id="93299-2567"><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="93299-2567"><strong>NoAccess</strong> – The server method can&#39;t be called.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="table-properties"></a><span data-ttu-id="93299-2568">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2568">Table properties</span></span>

<span data-ttu-id="93299-2569">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2569">The following table describes the properties for the node at **Security** &gt; **Privileges** &gt; **YourPrivilege** &gt; **Permissions** &gt; **Tables** &gt; **YourTable** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2570">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2570">Property</span></span></th>
<th><span data-ttu-id="93299-2571">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2571">Required</span></span></th>
<th><span data-ttu-id="93299-2572">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2572">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2573">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2573">Table</span></span></td>
<td><span data-ttu-id="93299-2574">有</span><span class="sxs-lookup"><span data-stu-id="93299-2574">Yes</span></span></td>
<td><span data-ttu-id="93299-2575">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2575">The name of the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2576">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2576">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2577">有</span><span class="sxs-lookup"><span data-stu-id="93299-2577">Yes</span></span></td>
<td><span data-ttu-id="93299-2578">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2578">The permission value.</span></span> <span data-ttu-id="93299-2579"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2579">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2580">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2580">Read</span></span></li>
<li><span data-ttu-id="93299-2581">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2581">Update</span></span></li>
<li><span data-ttu-id="93299-2582">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2582">Create</span></span></li>
<li><span data-ttu-id="93299-2583">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2583">Correct</span></span></li>
<li><span data-ttu-id="93299-2584">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2584">Delete</span></span></li>
<li><span data-ttu-id="93299-2585">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2585">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2586"><strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2586">The permission values for the <strong>EffectiveAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2587">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2587">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2588">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2588">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2589">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2589">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2590">修正アクセス許可は、時間状態テーブルが関係する場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2590">The Correct permission applies only when a time state table is involved.</span></span> <span data-ttu-id="93299-2591">このアクセス許可は、時間状態テーブルのレコードを更新する権限を与えます。</span><span class="sxs-lookup"><span data-stu-id="93299-2591">This permission authorizes you to update records in a time state table.</span></span> <span data-ttu-id="93299-2592">アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2592">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2593">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2593">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2594">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2594">Optional</span></span></td>
<td><span data-ttu-id="93299-2595">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2595">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="server-method-properties"></a><span data-ttu-id="93299-2596">サーバー メソッド プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2596">Server method properties</span></span>

<span data-ttu-id="93299-2597">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **サーバー メソッド** &gt; **YourServerMethod** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2597">The following table describes the properties for the node at **Security** &gt; **Privileges** &gt; **YourPrivilege** &gt; **Permissions** &gt; **Server Methods** &gt; **YourServerMethod** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2598">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2598">Property</span></span></th>
<th><span data-ttu-id="93299-2599">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2599">Required</span></span></th>
<th><span data-ttu-id="93299-2600">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2600">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2601">クラス</span><span class="sxs-lookup"><span data-stu-id="93299-2601">Class</span></span></td>
<td><span data-ttu-id="93299-2602">有</span><span class="sxs-lookup"><span data-stu-id="93299-2602">Yes</span></span></td>
<td><span data-ttu-id="93299-2603">サーバー クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2603">The name of the server class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2604">方法</span><span class="sxs-lookup"><span data-stu-id="93299-2604">Method</span></span></td>
<td><span data-ttu-id="93299-2605">有</span><span class="sxs-lookup"><span data-stu-id="93299-2605">Yes</span></span></td>
<td><span data-ttu-id="93299-2606"><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2606">The name of the secure server method that is tagged with the <strong>SysEntryPointAttribute</strong> attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2607">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2607">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2608">有</span><span class="sxs-lookup"><span data-stu-id="93299-2608">Yes</span></span></td>
<td><span data-ttu-id="93299-2609">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2609">The permission value.</span></span> <span data-ttu-id="93299-2610"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2610">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2611"><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2611"><strong>Invoke</strong> – The server method can be called.</span></span></li>
<li><span data-ttu-id="93299-2612"><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="93299-2612"><strong>NoAccess</strong> – The server method can&#39;t be called.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2613">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2613">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2614">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2614">Optional</span></span></td>
<td><span data-ttu-id="93299-2615">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2615">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a><span data-ttu-id="93299-2616">フォーム プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2616">Form properties</span></span>

<span data-ttu-id="93299-2617">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **権限** &gt; **YourPrivilege** &gt; **アクセス許可** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2617">The following table describes the properties for the node at **Security** &gt; **Privileges** &gt; **YourPrivilege** &gt; **Permissions** &gt; **Forms** &gt; **YourForm** in Application Explorer.</span></span>

| <span data-ttu-id="93299-2618">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2618">Property</span></span> | <span data-ttu-id="93299-2619">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2619">Required</span></span> | <span data-ttu-id="93299-2620">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2620">Description</span></span>           |
|----------|----------|-----------------------|
| <span data-ttu-id="93299-2621">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2621">Form</span></span>     | <span data-ttu-id="93299-2622">有</span><span class="sxs-lookup"><span data-stu-id="93299-2622">Yes</span></span>      | <span data-ttu-id="93299-2623">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2623">The name of the form.</span></span> |

## <a name="security-process-cycle-properties"></a><span data-ttu-id="93299-2624">セキュリティ プロセス サイクル プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2624">Security process cycle properties</span></span>
<span data-ttu-id="93299-2625">プロセス サイクルは、職務のグループです。</span><span class="sxs-lookup"><span data-stu-id="93299-2625">A process cycle is a group of duties.</span></span> <span data-ttu-id="93299-2626">プロセス サイクルは、高度なジョブ機能を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2626">A process cycle represents a high-level job function.</span></span> <span data-ttu-id="93299-2627">特定のジョブ機能を実行する詳細については時間の経過とともに変化しますが、概念とそのジョブ機能の名前はおそらく変化しません。</span><span class="sxs-lookup"><span data-stu-id="93299-2627">Although the details of how a given job function is run might change over time, the concept and name of that job function probably don't change.</span></span>

### <a name="best-practices"></a><span data-ttu-id="93299-2628">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="93299-2628">Best practices</span></span>

<span data-ttu-id="93299-2629">このセクションでは、プロセス サイクルのベスト プラクティス ルールについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2629">This section describes the best practice rules for process cycles.</span></span>

-   <span data-ttu-id="93299-2630">各職務権限は、プロセス サイクルの一部である必要があります</span><span class="sxs-lookup"><span data-stu-id="93299-2630">Each duty should be part of a process cycle.</span></span>
-   <span data-ttu-id="93299-2631">プロセス サイクルを使用して、ジョブ機能の職務のグループを編成します。</span><span class="sxs-lookup"><span data-stu-id="93299-2631">Use a process cycle to organize a group of duties for a job function.</span></span>

### <a name="process-cycle-hierarchy-in-application-explorer"></a><span data-ttu-id="93299-2632">アプリケーション エクスプローラーのプロセス サイクル</span><span class="sxs-lookup"><span data-stu-id="93299-2632">Process cycle hierarchy in Application Explorer</span></span>

<span data-ttu-id="93299-2633">次のリストは、アプリケーション エクスプローラーのプロセス サイクル ノードの階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2633">The following list shows the hierarchy of process cycles nodes in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2634">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2634">Security</span></span>
    -   <span data-ttu-id="93299-2635">プロセス サイクル</span><span class="sxs-lookup"><span data-stu-id="93299-2635">Process Cycles</span></span>
        -   <span data-ttu-id="93299-2636">YourProcessCycle</span><span class="sxs-lookup"><span data-stu-id="93299-2636">YourProcessCycle</span></span>
            -   <span data-ttu-id="93299-2637">職務権限</span><span class="sxs-lookup"><span data-stu-id="93299-2637">Duties</span></span>

### <a name="process-cycle-properties"></a><span data-ttu-id="93299-2638">サイクル プロパティの処理</span><span class="sxs-lookup"><span data-stu-id="93299-2638">Process cycle properties</span></span>

<span data-ttu-id="93299-2639">T次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **プロセス** **サイクル** &gt; **YourProcessCycle** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2639">The following table describes the properties for the node at **Security** &gt; **Process** **Cycles** &gt; **YourProcessCycle** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2640">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2640">Property</span></span></th>
<th><span data-ttu-id="93299-2641">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2641">Required</span></span></th>
<th><span data-ttu-id="93299-2642">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2642">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2643">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2643">Name</span></span></td>
<td><span data-ttu-id="93299-2644">有</span><span class="sxs-lookup"><span data-stu-id="93299-2644">Yes</span></span></td>
<td><span data-ttu-id="93299-2645">プロセス サイクルの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2645">The name of the process cycle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2646">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2646">Label</span></span></td>
<td><span data-ttu-id="93299-2647">有</span><span class="sxs-lookup"><span data-stu-id="93299-2647">Yes</span></span></td>
<td><span data-ttu-id="93299-2648">ユーザー インターフェイスのプロセス サイクルで表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="93299-2648">Text that is shown for the process cycle in the user interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2649">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2649">Description</span></span></td>
<td><span data-ttu-id="93299-2650">有</span><span class="sxs-lookup"><span data-stu-id="93299-2650">Yes</span></span></td>
<td><span data-ttu-id="93299-2651">プロセス サイクルの説明。</span><span class="sxs-lookup"><span data-stu-id="93299-2651">A description of the process cycle.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2652">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2652">Enabled</span></span></td>
<td><span data-ttu-id="93299-2653">有</span><span class="sxs-lookup"><span data-stu-id="93299-2653">Yes</span></span></td>
<td><span data-ttu-id="93299-2654">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2654">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2655"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2655">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2656"><strong>はい</strong> - プロセス サイクルを有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2656"><strong>Yes</strong> – Enable the process cycle.</span></span></li>
<li><span data-ttu-id="93299-2657"><strong>いいえ</strong> - プロセス サイクルを無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2657"><strong>No</strong> – Disable the process cycle.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="duty-properties"></a><span data-ttu-id="93299-2658">職務プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2658">Duty properties</span></span>

<span data-ttu-id="93299-2659">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **プロセス サイクル** &gt; **YourProcessCycle** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2659">The following table describes the properties for the node at **Security** &gt; **Process Cycles** &gt; **YourProcessCycle** &gt; **Duties** &gt; **YourDuty** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2660">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2660">Property</span></span></th>
<th><span data-ttu-id="93299-2661">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2661">Required</span></span></th>
<th><span data-ttu-id="93299-2662">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2662">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2663">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2663">Name</span></span></td>
<td><span data-ttu-id="93299-2664">有</span><span class="sxs-lookup"><span data-stu-id="93299-2664">Yes</span></span></td>
<td><span data-ttu-id="93299-2665">職務権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2665">The name of the duty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2666">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2666">Enabled</span></span></td>
<td><span data-ttu-id="93299-2667">有</span><span class="sxs-lookup"><span data-stu-id="93299-2667">Yes</span></span></td>
<td><span data-ttu-id="93299-2668">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2668">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2669"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2669">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2670"><strong>はい</strong> - 職務権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2670"><strong>Yes</strong> – Enable the duty.</span></span></li>
<li><span data-ttu-id="93299-2671"><strong>いいえ</strong> - 関税を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2671"><strong>No</strong> – Disable the duty.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="security-policy-properties"></a><span data-ttu-id="93299-2672">セキュリティ ポリシーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2672">Security policy properties</span></span>
<span data-ttu-id="93299-2673">開発者およびシステム管理者は、テーブル内のデータ レコードのサブセットへのアクセスを拒否するセキュリティ ポリシーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2673">Developers and system administrators can create security policies to deny access to a subset of data records in tables.</span></span>

### <a name="constrained-tables-of-a-policy"></a><span data-ttu-id="93299-2674">ポリシーの制約付きテーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2674">Constrained tables of a policy</span></span>

<span data-ttu-id="93299-2675">アプリケーション エクスプローラー内のセキュリティ ポリシーの **制限付きテーブル** ノードの下に、テーブルおよびビューを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2675">You can add tables and views under the **Constrained Tables** node of a security policy in Application Explorer.</span></span> <span data-ttu-id="93299-2676">これらのテーブルとビューは、ポリシーの **Query** プロパティに名前が付けられたクエリのデータ ソース テーブルに関連しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2676">These tables and views are related to the data source table of the query that is named in the **Query** property of the policy.</span></span> <span data-ttu-id="93299-2677">次のリストは、アプリケーション エクスプローラーのセキュリティ ポリシーの階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2677">The following list shows the hierarchy of security policy nodes in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2678">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2678">Security</span></span>
    -   <span data-ttu-id="93299-2679">ポリシー</span><span class="sxs-lookup"><span data-stu-id="93299-2679">Policies</span></span>
        -   <span data-ttu-id="93299-2680">YourPolicy</span><span class="sxs-lookup"><span data-stu-id="93299-2680">YourPolicy</span></span>
            -   <span data-ttu-id="93299-2681">制約付きテーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2681">Constrained Tables</span></span>
                -   <span data-ttu-id="93299-2682">YourConstrainedTable</span><span class="sxs-lookup"><span data-stu-id="93299-2682">YourConstrainedTable</span></span>
                    -   <span data-ttu-id="93299-2683">YourConstrainedSubTable</span><span class="sxs-lookup"><span data-stu-id="93299-2683">YourConstrainedSubTable</span></span>
                -   <span data-ttu-id="93299-2684">YourConstrainedView</span><span class="sxs-lookup"><span data-stu-id="93299-2684">YourConstrainedView</span></span>

<span data-ttu-id="93299-2685">各**制約付きテーブル**ノードは、制約されたテーブルおよびビューの任意の数を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2685">Each **Constrained Tables** node can contain any number of constrained tables and views.</span></span> <span data-ttu-id="93299-2686">また、各制約付きテーブルは、制約付きサブテーブルの任意の数を含むことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2686">Additionally, each constrained table can contain any number of constrained sub-tables.</span></span>

### <a name="security-policy-properties"></a><span data-ttu-id="93299-2687">セキュリティ ポリシーのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2687">Security policy properties</span></span>

<span data-ttu-id="93299-2688">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ポリシー** &gt; **YourPolicy** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2688">The following table describes the properties for the node at **Security** &gt; **Policies** &gt; **YourPolicy** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2689">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2689">Property</span></span></th>
<th><span data-ttu-id="93299-2690">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2690">Required</span></span></th>
<th><span data-ttu-id="93299-2691">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2691">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2692">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2692">Name</span></span></td>
<td><span data-ttu-id="93299-2693">有</span><span class="sxs-lookup"><span data-stu-id="93299-2693">Yes</span></span></td>
<td><span data-ttu-id="93299-2694">セキュリティ ポリシーの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2694">The name of the security policy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2695">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2695">Label</span></span></td>
<td><span data-ttu-id="93299-2696">有</span><span class="sxs-lookup"><span data-stu-id="93299-2696">Yes</span></span></td>
<td><span data-ttu-id="93299-2697">ユーザー インターフェイスのセキュリティ ポリシーで表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="93299-2697">The text that is shown for the security policy in the user interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2698">PrimaryTable</span><span class="sxs-lookup"><span data-stu-id="93299-2698">PrimaryTable</span></span></td>
<td><span data-ttu-id="93299-2699">有</span><span class="sxs-lookup"><span data-stu-id="93299-2699">Yes</span></span></td>
<td><span data-ttu-id="93299-2700">セキュリティ ポリシー クエリのデータ ソースで指定されているテーブル。</span><span class="sxs-lookup"><span data-stu-id="93299-2700">The table that is specified in the data source for the security policy query.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2701">クエリ</span><span class="sxs-lookup"><span data-stu-id="93299-2701">Query</span></span></td>
<td><span data-ttu-id="93299-2702">有</span><span class="sxs-lookup"><span data-stu-id="93299-2702">Yes</span></span></td>
<td><span data-ttu-id="93299-2703">ポリシーで指定された制約付きテーブルからデータをフィルタリングするためにポリシーが使用するクエリ。</span><span class="sxs-lookup"><span data-stu-id="93299-2703">The query that the policy uses to filter data from the constrained tables that are specified in the policy.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2704">UseNotExistJoin</span><span class="sxs-lookup"><span data-stu-id="93299-2704">UseNotExistJoin</span></span></td>
<td><span data-ttu-id="93299-2705">有</span><span class="sxs-lookup"><span data-stu-id="93299-2705">Yes</span></span></td>
<td><span data-ttu-id="93299-2706">セキュリティ クエリを<strong>存在しない</strong>結合または<strong>存在する</strong>結合として適用する必要があるかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2706">A value that indicates whether the security query must be applied as a <strong>not exists</strong> join or an <strong>exists</strong> join.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2707">PolicyGroup</span><span class="sxs-lookup"><span data-stu-id="93299-2707">PolicyGroup</span></span></td>
<td><span data-ttu-id="93299-2708">無</span><span class="sxs-lookup"><span data-stu-id="93299-2708">No</span></span></td>
<td><span data-ttu-id="93299-2709">管理者と開発者は、このプロパティを使用して、関連するセキュリティ ポリシーのグループをすばやく識別できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2709">Administrators and developers can use this property to quickly identify groups of related security policies.</span></span> <span data-ttu-id="93299-2710">システム管理者または開発者が作成したセキュリティ ポリシー グループの名前のいずれかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2710">The available options are the names of the security policy groups that the system administrator or developer has created.</span></span> <span data-ttu-id="93299-2711">実行時にこのプロパティは使用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2711">The system doesn&#39;t use this property at run time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2712">ConstrainedTable</span><span class="sxs-lookup"><span data-stu-id="93299-2712">ConstrainedTable</span></span></td>
<td><span data-ttu-id="93299-2713">有</span><span class="sxs-lookup"><span data-stu-id="93299-2713">Yes</span></span></td>
<td><span data-ttu-id="93299-2714">セキュリティ ポリシーが主テーブルから返されるレコードのデータ値を制限するかどうかをコントロールする値。</span><span class="sxs-lookup"><span data-stu-id="93299-2714">A value that controls whether the security policy restricts the data values in records that are returned from the primary table.</span></span> <span data-ttu-id="93299-2715"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2715">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2716"><strong>はい </strong>- セキュリティ ポリシーはプライマリ テーブルには適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2716"><strong>Yes </strong>– The security policy is enforced on the primary table.</span></span></li>
<li><span data-ttu-id="93299-2717"><strong>いいえ </strong>- セキュリティ ポリシーはプライマリ テーブルには適用されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2717"><strong>No </strong>– The security policy isn&#39;t enforced on the primary table.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2718">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2718">Enabled</span></span></td>
<td><span data-ttu-id="93299-2719">有</span><span class="sxs-lookup"><span data-stu-id="93299-2719">Yes</span></span></td>
<td><span data-ttu-id="93299-2720">システムが実行時間に、ポリシーを適用するかどうかをコントロールする値。</span><span class="sxs-lookup"><span data-stu-id="93299-2720">A value that controls whether the system enforces the policy at run time.</span></span> <span data-ttu-id="93299-2721"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2721">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2722"><strong>はい </strong>- セキュリティ ポリシーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2722"><strong>Yes </strong>– Enable the security policy.</span></span></li>
<li><span data-ttu-id="93299-2723"><strong>いいえ</strong> - セキュリティ ポリシーを無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2723"><strong>No </strong>– Disable the security policy.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2724">工程</span><span class="sxs-lookup"><span data-stu-id="93299-2724">Operation</span></span></td>
<td><span data-ttu-id="93299-2725">有</span><span class="sxs-lookup"><span data-stu-id="93299-2725">Yes</span></span></td>
<td><span data-ttu-id="93299-2726">ポリシーが適用されるデータ操作をコントロールする値。</span><span class="sxs-lookup"><span data-stu-id="93299-2726">A value that controls which data operations the policy is enforced for.</span></span> <span data-ttu-id="93299-2727"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2727">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2728">選択</span><span class="sxs-lookup"><span data-stu-id="93299-2728">Select</span></span></li>
<li><span data-ttu-id="93299-2729">挿入</span><span class="sxs-lookup"><span data-stu-id="93299-2729">Insert</span></span></li>
<li><span data-ttu-id="93299-2730">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2730">Update</span></span></li>
<li><span data-ttu-id="93299-2731">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2731">Delete</span></span></li>
<li><span data-ttu-id="93299-2732">挿入、更新、削除</span><span class="sxs-lookup"><span data-stu-id="93299-2732">Insert, Update and Delete</span></span></li>
<li><span data-ttu-id="93299-2733">すべての工程</span><span class="sxs-lookup"><span data-stu-id="93299-2733">All operations</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2734">ContextType</span><span class="sxs-lookup"><span data-stu-id="93299-2734">ContextType</span></span></td>
<td><span data-ttu-id="93299-2735">有</span><span class="sxs-lookup"><span data-stu-id="93299-2735">Yes</span></span></td>
<td><span data-ttu-id="93299-2736">セキュリティ ポリシーのコンテキスト タイプをコントロールする値。</span><span class="sxs-lookup"><span data-stu-id="93299-2736">A value that controls the context type of the security policy.</span></span> <span data-ttu-id="93299-2737"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2737">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2738"><strong>ContextString</strong> - <strong>ContextString</strong> プロパティの値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-2738"><strong>ContextString </strong>– You must specify a value for the <strong>ContextString</strong> property.</span></span> <span data-ttu-id="93299-2739">セキュリティ ポリシーは、ポリシーに特定のアプリケーション コンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-2739">The security policy uses a specific application context for the policy.</span></span></li>
<li><span data-ttu-id="93299-2740"><strong>RoleName </strong>- セキュリティ ポリシーは、<strong>RoleName</strong> の値に割り当てられているアプリケーション ユーザーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2740"><strong>RoleName </strong>– The security policy is applied only to the application user who is assigned to the value of <strong>RoleName</strong>.</span></span></li>
<li><span data-ttu-id="93299-2741"><strong>RoleProperty </strong>- この値は、<strong>ContextString</strong> と組み合わせて使用され、複数のロール コンテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2741"><strong>RoleProperty </strong>– This value is used in combination with the <strong>ContextString</strong> property to specify multiple roles context.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2742">ContextString</span><span class="sxs-lookup"><span data-stu-id="93299-2742">ContextString</span></span></td>
<td><span data-ttu-id="93299-2743">有</span><span class="sxs-lookup"><span data-stu-id="93299-2743">Yes</span></span></td>
<td><span data-ttu-id="93299-2744">このプロパティは、<strong>ContextType</strong> プロパティと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2744">This property is used in combination with <strong>ContextType</strong> property.</span></span> <span data-ttu-id="93299-2745">アプリケーションまたは複数のロール コンテキストを指定するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2745">It can be used to specify an application or multiple roles context.</span></span></td>
</tr>
</tbody>
</table>

## <a name="security-role-properties"></a><span data-ttu-id="93299-2746">セキュリティ ロールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2746">Security role properties</span></span>
<span data-ttu-id="93299-2747">ロールは、ユーザーに付与できるアクセス許可のコレクションを表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2747">Roles represent a collection of permissions that can be granted to users.</span></span> <span data-ttu-id="93299-2748">各ロール ノードの下にある入れ子になったノードは、ユーザーがアクセスできるさまざまなセキュリティ保護可能オブジェクトを識別し、各アクセス レベルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2748">The nodes that are nested below each role node identify various securable objects that a user can access and specify the level of access.</span></span>

### <a name="role-node-in-application-explorer"></a><span data-ttu-id="93299-2749">アプリケーション エクスプローラーでのロール ノード</span><span class="sxs-lookup"><span data-stu-id="93299-2749">Role node in Application Explorer</span></span>

<span data-ttu-id="93299-2750">ロールは、セキュリティ保護可能なオブジェクトへのアクセス許可の付与に使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2750">Roles are used to give access to securable objects.</span></span> <span data-ttu-id="93299-2751">次のリストは、アプリケーション エクスプローラーのロール ノードの階層を示しています。</span><span class="sxs-lookup"><span data-stu-id="93299-2751">The following list shows the hierarchy of role nodes in Application Explorer:</span></span>

-   <span data-ttu-id="93299-2752">セキュリティ</span><span class="sxs-lookup"><span data-stu-id="93299-2752">Security</span></span>
    -   <span data-ttu-id="93299-2753">ロール</span><span class="sxs-lookup"><span data-stu-id="93299-2753">Roles</span></span>
        -   <span data-ttu-id="93299-2754">YourRole</span><span class="sxs-lookup"><span data-stu-id="93299-2754">YourRole</span></span>
            -   <span data-ttu-id="93299-2755">職務権限</span><span class="sxs-lookup"><span data-stu-id="93299-2755">Duties</span></span>
            -   <span data-ttu-id="93299-2756">権限</span><span class="sxs-lookup"><span data-stu-id="93299-2756">Privileges</span></span>
            -   <span data-ttu-id="93299-2757">アクセス許可</span><span class="sxs-lookup"><span data-stu-id="93299-2757">Permissions</span></span>
                -   <span data-ttu-id="93299-2758">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2758">Tables</span></span>
                -   <span data-ttu-id="93299-2759">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2759">Forms</span></span>
                -   <span data-ttu-id="93299-2760">サーバー メソッド</span><span class="sxs-lookup"><span data-stu-id="93299-2760">Server Methods</span></span>
            -   <span data-ttu-id="93299-2761">サブロール</span><span class="sxs-lookup"><span data-stu-id="93299-2761">Sub Roles</span></span>

<span data-ttu-id="93299-2762">ロールは通常、セキュリティ税、および場合によってはセキュリティ権限に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="93299-2762">Roles are typically associated with security duties, and sometimes with security privileges.</span></span> <span data-ttu-id="93299-2763">ロール内のセキュリティ保護可能なオブジェクトへのアクセス レベルは、職務、権限、またはその両方から派生します。</span><span class="sxs-lookup"><span data-stu-id="93299-2763">Access levels to securable objects within a role are derived from the duties, privileges, or both.</span></span> <span data-ttu-id="93299-2764">ロールは、**アクセス許可** ノードの下でセキュリティ保護可能なオブジェクトへのアクセス レベルを上書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="93299-2764">Roles can also override the access levels to securable objects under the **Permissions** node.</span></span>

### <a name="role-properties"></a><span data-ttu-id="93299-2765">役割のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2765">Role properties</span></span>

<span data-ttu-id="93299-2766">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **YourRole** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2766">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **YourRole** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2767">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2767">Property</span></span></th>
<th><span data-ttu-id="93299-2768">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2768">Required</span></span></th>
<th><span data-ttu-id="93299-2769">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2769">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2770">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2770">Name</span></span></td>
<td><span data-ttu-id="93299-2771">有</span><span class="sxs-lookup"><span data-stu-id="93299-2771">Yes</span></span></td>
<td><span data-ttu-id="93299-2772">ロールの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2772">The name of the role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2773">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2773">Label</span></span></td>
<td><span data-ttu-id="93299-2774">有</span><span class="sxs-lookup"><span data-stu-id="93299-2774">Yes</span></span></td>
<td><span data-ttu-id="93299-2775">ユーザー インターフェイスのロールで表示されるテキスト。</span><span class="sxs-lookup"><span data-stu-id="93299-2775">Text that is shown for the role in the user interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2776">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2776">Description</span></span></td>
<td><span data-ttu-id="93299-2777">有</span><span class="sxs-lookup"><span data-stu-id="93299-2777">Yes</span></span></td>
<td><span data-ttu-id="93299-2778">ロールの説明。</span><span class="sxs-lookup"><span data-stu-id="93299-2778">A description of the role.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2779">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2779">Enabled</span></span></td>
<td><span data-ttu-id="93299-2780">有</span><span class="sxs-lookup"><span data-stu-id="93299-2780">Yes</span></span></td>
<td><span data-ttu-id="93299-2781">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2781">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2782"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2782">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2783"><strong>はい</strong> - ロールを有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2783"><strong>Yes</strong> – Enable the role.</span></span></li>
<li><span data-ttu-id="93299-2784"><strong>いいえ</strong> - ロールを無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2784"><strong>No</strong> – Disable the role.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2785">PastDataAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2785">PastDataAccess</span></span></td>
<td><span data-ttu-id="93299-2786">有</span><span class="sxs-lookup"><span data-stu-id="93299-2786">Yes</span></span></td>
<td><span data-ttu-id="93299-2787">有効日フィールドのあるテーブルの過去のデータ アクセス。</span><span class="sxs-lookup"><span data-stu-id="93299-2787">The past data access for the tables that have date-effective fields.</span></span> <span data-ttu-id="93299-2788"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2788">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2789">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2789">Read</span></span></li>
<li><span data-ttu-id="93299-2790">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2790">Update</span></span></li>
<li><span data-ttu-id="93299-2791">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2791">Create</span></span></li>
<li><span data-ttu-id="93299-2792">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2792">Correct</span></span></li>
<li><span data-ttu-id="93299-2793">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2793">Delete</span></span></li>
<li><span data-ttu-id="93299-2794">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2794">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2795"><strong>PastDataAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2795">The permission values for the <strong>PastDataAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2796">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2796">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2797">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2797">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2798">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2798">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2799">アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2799">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2800">CurrentDataAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2800">CurrentDataAccess</span></span></td>
<td><span data-ttu-id="93299-2801">有</span><span class="sxs-lookup"><span data-stu-id="93299-2801">Yes</span></span></td>
<td><span data-ttu-id="93299-2802">有効日フィールドのあるテーブルの現在のデータ アクセス。</span><span class="sxs-lookup"><span data-stu-id="93299-2802">The current data access for the tables that have date-effective fields.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2803">FutureDataAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2803">FutureDataAccess</span></span></td>
<td><span data-ttu-id="93299-2804">有</span><span class="sxs-lookup"><span data-stu-id="93299-2804">Yes</span></span></td>
<td><span data-ttu-id="93299-2805">有効日フィールドのあるテーブルの将来のデータ アクセス。</span><span class="sxs-lookup"><span data-stu-id="93299-2805">The future data access for the tables that have date-effective fields.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2806">ContextString</span><span class="sxs-lookup"><span data-stu-id="93299-2806">ContextString</span></span></td>
<td><span data-ttu-id="93299-2807">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2807">Optional</span></span></td>
<td><span data-ttu-id="93299-2808">セキュリティ ポリシーによって使用できるユーザー定義の文字列。</span><span class="sxs-lookup"><span data-stu-id="93299-2808">A user-defined string that can be used by security policies.</span></span></td>
</tr>
</tbody>
</table>

### <a name="duty-properties"></a><span data-ttu-id="93299-2809">職務プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2809">Duty properties</span></span>

<span data-ttu-id="93299-2810">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **職務権限** &gt; **YourDuty** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2810">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Duties** &gt; **YourDuty** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2811">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2811">Property</span></span></th>
<th><span data-ttu-id="93299-2812">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2812">Required</span></span></th>
<th><span data-ttu-id="93299-2813">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2813">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2814">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2814">Name</span></span></td>
<td><span data-ttu-id="93299-2815">有</span><span class="sxs-lookup"><span data-stu-id="93299-2815">Yes</span></span></td>
<td><span data-ttu-id="93299-2816">職務権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2816">The name of the duty.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2817">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2817">Enabled</span></span></td>
<td><span data-ttu-id="93299-2818">有</span><span class="sxs-lookup"><span data-stu-id="93299-2818">Yes</span></span></td>
<td><span data-ttu-id="93299-2819">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2819">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2820"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2820">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2821"><strong>はい</strong> - 職務権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2821"><strong>Yes</strong> – Enable the duty.</span></span></li>
<li><span data-ttu-id="93299-2822"><strong>いいえ</strong> - 関税を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2822"><strong>No</strong> – Disable the duty.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="privilege-properties"></a><span data-ttu-id="93299-2823">権限のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2823">Privilege properties</span></span>

<span data-ttu-id="93299-2824">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **YourPrivilege** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2824">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Privileges** &gt; **YourPrivilege** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2825">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2825">Property</span></span></th>
<th><span data-ttu-id="93299-2826">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2826">Required</span></span></th>
<th><span data-ttu-id="93299-2827">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2827">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2828">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2828">Name</span></span></td>
<td><span data-ttu-id="93299-2829">有</span><span class="sxs-lookup"><span data-stu-id="93299-2829">Yes</span></span></td>
<td><span data-ttu-id="93299-2830">権限の名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2830">The name of the privilege.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2831">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2831">Enabled</span></span></td>
<td><span data-ttu-id="93299-2832">有</span><span class="sxs-lookup"><span data-stu-id="93299-2832">Yes</span></span></td>
<td><span data-ttu-id="93299-2833">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2833">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2834"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2834">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2835"><strong>はい</strong> - 権限を有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2835"><strong>Yes</strong> – Enable the privilege.</span></span></li>
<li><span data-ttu-id="93299-2836"><strong>いいえ</strong> - 権限を無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2836"><strong>No</strong> – Disable the privilege.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="table-properties"></a><span data-ttu-id="93299-2837">表のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2837">Table properties</span></span>

<span data-ttu-id="93299-2838">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **テーブル** &gt; **YourTable** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2838">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Permissions** &gt; **Tables** &gt; **YourTable** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2839">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2839">Property</span></span></th>
<th><span data-ttu-id="93299-2840">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2840">Required</span></span></th>
<th><span data-ttu-id="93299-2841">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2841">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2842">テーブル</span><span class="sxs-lookup"><span data-stu-id="93299-2842">Table</span></span></td>
<td><span data-ttu-id="93299-2843">有</span><span class="sxs-lookup"><span data-stu-id="93299-2843">Yes</span></span></td>
<td><span data-ttu-id="93299-2844">テーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2844">The name of the table.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2845">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2845">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2846">有</span><span class="sxs-lookup"><span data-stu-id="93299-2846">Yes</span></span></td>
<td><span data-ttu-id="93299-2847">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2847">The permission value.</span></span> <span data-ttu-id="93299-2848"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2848">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2849">既読</span><span class="sxs-lookup"><span data-stu-id="93299-2849">Read</span></span></li>
<li><span data-ttu-id="93299-2850">更新</span><span class="sxs-lookup"><span data-stu-id="93299-2850">Update</span></span></li>
<li><span data-ttu-id="93299-2851">新規</span><span class="sxs-lookup"><span data-stu-id="93299-2851">Create</span></span></li>
<li><span data-ttu-id="93299-2852">修正</span><span class="sxs-lookup"><span data-stu-id="93299-2852">Correct</span></span></li>
<li><span data-ttu-id="93299-2853">消去</span><span class="sxs-lookup"><span data-stu-id="93299-2853">Delete</span></span></li>
<li><span data-ttu-id="93299-2854">NoAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2854">NoAccess</span></span></li>
</ul>
<span data-ttu-id="93299-2855"><strong>EffectiveAccess</strong> プロパティのアクセス許可の値は階層を表します。</span><span class="sxs-lookup"><span data-stu-id="93299-2855">The permission values for the <strong>EffectiveAccess</strong> property represent a hierarchy.</span></span> <span data-ttu-id="93299-2856">読み取りは最も低いアクセス許可であり、削除は最も強いアクセス許可です。</span><span class="sxs-lookup"><span data-stu-id="93299-2856">Read is the weakest permission, and Delete is the strongest.</span></span> <span data-ttu-id="93299-2857">削除のアクセス許可には他のすべての権限が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2857">Delete permission includes every other permission.</span></span> <span data-ttu-id="93299-2858">アクセス許可には、更新と読み取りが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2858">Create permission includes Update and Read.</span></span> <span data-ttu-id="93299-2859">アクセス許可の値を <strong>NoAccess</strong> に設定すると、テーブルに対するすべてのアクセスを禁止することができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2859">You can set the permission value to <strong>NoAccess</strong> to prevent all access to the table.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2860">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2860">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2861">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2861">Optional</span></span></td>
<td><span data-ttu-id="93299-2862">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2862">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="form-properties"></a><span data-ttu-id="93299-2863">フォーム プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2863">Form properties</span></span>

<span data-ttu-id="93299-2864">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **フォーム** &gt; **YourForm** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2864">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Permissions** &gt; **Form** &gt; **YourForm** in Application Explorer.</span></span>

| <span data-ttu-id="93299-2865">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2865">Property</span></span> | <span data-ttu-id="93299-2866">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2866">Required</span></span> | <span data-ttu-id="93299-2867">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2867">Description</span></span>           |
|----------|----------|-----------------------|
| <span data-ttu-id="93299-2868">フォーム</span><span class="sxs-lookup"><span data-stu-id="93299-2868">Form</span></span>     | <span data-ttu-id="93299-2869">有</span><span class="sxs-lookup"><span data-stu-id="93299-2869">Yes</span></span>      | <span data-ttu-id="93299-2870">フォームの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2870">The name of the form.</span></span> |

### <a name="server-method-properties"></a><span data-ttu-id="93299-2871">サーバー メソッド プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2871">Server method properties</span></span>

<span data-ttu-id="93299-2872">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **権限** &gt; **サーバー メソッド** &gt; **YourServerMethod** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2872">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Permissions** &gt; **Server Methods** &gt; **YourServerMethod** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2873">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2873">Property</span></span></th>
<th><span data-ttu-id="93299-2874">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2874">Required</span></span></th>
<th><span data-ttu-id="93299-2875">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2875">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2876">クラス</span><span class="sxs-lookup"><span data-stu-id="93299-2876">Class</span></span></td>
<td><span data-ttu-id="93299-2877">有</span><span class="sxs-lookup"><span data-stu-id="93299-2877">Yes</span></span></td>
<td><span data-ttu-id="93299-2878">サーバー クラスの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2878">The name of the server class.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2879">方法</span><span class="sxs-lookup"><span data-stu-id="93299-2879">Method</span></span></td>
<td><span data-ttu-id="93299-2880">有</span><span class="sxs-lookup"><span data-stu-id="93299-2880">Yes</span></span></td>
<td><span data-ttu-id="93299-2881"><strong>SysEntryPointAttribute</strong> 属性でタグ付けされた安全なサーバー メソッドの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2881">The name of the secure server method that is tagged with the <strong>SysEntryPointAttribute</strong> attribute.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2882">EffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="93299-2882">EffectiveAccess</span></span></td>
<td><span data-ttu-id="93299-2883">有</span><span class="sxs-lookup"><span data-stu-id="93299-2883">Yes</span></span></td>
<td><span data-ttu-id="93299-2884">アクセス許可の値。</span><span class="sxs-lookup"><span data-stu-id="93299-2884">The permission value.</span></span> <span data-ttu-id="93299-2885"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2885">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2886"><strong>呼び出し</strong> - サーバー メソッドを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="93299-2886"><strong>Invoke</strong> – The server method can be called.</span></span></li>
<li><span data-ttu-id="93299-2887"><strong>NoAccess</strong> - サーバー メソッドを呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="93299-2887"><strong>NoAccess</strong> – The server method can&#39;t be called.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2888">ManagedBy</span><span class="sxs-lookup"><span data-stu-id="93299-2888">ManagedBy</span></span></td>
<td><span data-ttu-id="93299-2889">オプション</span><span class="sxs-lookup"><span data-stu-id="93299-2889">Optional</span></span></td>
<td><span data-ttu-id="93299-2890">このプロパティは、自動化ツールで使用されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2890">This property is used by automation tools.</span></span></td>
</tr>
</tbody>
</table>

### <a name="subrole-properties"></a><span data-ttu-id="93299-2891">サブロールのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2891">Subrole properties</span></span>

<span data-ttu-id="93299-2892">次のテーブルでは、アプリケーション エクスプローラーの **セキュリティ** &gt; **ロール** &gt; **サブロール** &gt; **YourSubRole** のノードのプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2892">The following table describes the properties for the node at **Security** &gt; **Roles** &gt; **Sub Roles** &gt; **YourSubRole** in Application Explorer.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2893">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2893">Property</span></span></th>
<th><span data-ttu-id="93299-2894">要求済み</span><span class="sxs-lookup"><span data-stu-id="93299-2894">Required</span></span></th>
<th><span data-ttu-id="93299-2895">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2895">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2896">氏名</span><span class="sxs-lookup"><span data-stu-id="93299-2896">Name</span></span></td>
<td><span data-ttu-id="93299-2897">有</span><span class="sxs-lookup"><span data-stu-id="93299-2897">Yes</span></span></td>
<td><span data-ttu-id="93299-2898">サブロールの名前。</span><span class="sxs-lookup"><span data-stu-id="93299-2898">The name of the subrole.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2899">有効</span><span class="sxs-lookup"><span data-stu-id="93299-2899">Enabled</span></span></td>
<td><span data-ttu-id="93299-2900">有</span><span class="sxs-lookup"><span data-stu-id="93299-2900">Yes</span></span></td>
<td><span data-ttu-id="93299-2901">職務権限が有効かどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="93299-2901">A value that indicates whether the duty is enabled.</span></span> <span data-ttu-id="93299-2902"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2902">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2903"><strong>はい</strong> - サブロールを有効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2903"><strong>Yes</strong> – Enable the subrole</span></span></li>
<li><span data-ttu-id="93299-2904"><strong>いいえ</strong> - サブロールを無効にします。</span><span class="sxs-lookup"><span data-stu-id="93299-2904"><strong>No</strong> – Disable the subrole.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="web-menu-properties"></a><span data-ttu-id="93299-2905">Web メニューのプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2905">Web menu properties</span></span>
<span data-ttu-id="93299-2906">次のデーブルでは、Web メニューとサブメニューに固有のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2906">The following table describes the properties that are specific to web menus and submenus.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2907">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2907">Property</span></span></th>
<th><span data-ttu-id="93299-2908">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2908">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2909">ConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-2909">ConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-2910">このメニューの表示の制御に使用されるコンフィギュレーション キーを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2910">Specify the configuration key that is used to control display of this menu.</span></span> <span data-ttu-id="93299-2911">ユーザーがコンフィギュレーション キーにアクセスできない場合は、メニューは表示されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2911">If a user doesn&#39;t have access to the configuration key, the menu won&#39;t be visible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2912">HighlightSelected</span><span class="sxs-lookup"><span data-stu-id="93299-2912">HighlightSelected</span></span></td>
<td><span data-ttu-id="93299-2913">このプロパティは、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="93299-2913">This property isn&#39;t supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2914">ラベル</span><span class="sxs-lookup"><span data-stu-id="93299-2914">Label</span></span></td>
<td><span data-ttu-id="93299-2915">Web メニューまたはサブメニューの最上位レベル ノードに表示されるテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2915">Specify the text that is shown for the top-level node of the web menu or submenu.</span></span> <span data-ttu-id="93299-2916">値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="93299-2916">The value can&#39;t exceed 250 characters.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2917">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="93299-2917">MenuItemName</span></span></td>
<td><span data-ttu-id="93299-2918">メニューまたはサブメニューの最上位ノードをクリックしたときにアクセスするメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2918">Specify the menu item to access when the top-level node for the menu or submenu is clicked.</span></span> <span data-ttu-id="93299-2919">使用可能なオプションは、<strong>MenuItemType</strong> プロパティの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="93299-2919">The options that are available depend on the setting of the <strong>MenuItemType</strong> property.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2920">MenuItemType</span><span class="sxs-lookup"><span data-stu-id="93299-2920">MenuItemType</span></span></td>
<td><span data-ttu-id="93299-2921">メニューまたはサブメニューの最上位ノードによりアクセスされるメニュー項目の種類を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2921">Specify the type of menu item that is accessed by the top-level node of the menu or submenu.</span></span> <span data-ttu-id="93299-2922"><strong>アクション</strong> または <strong>URL</strong> を選択できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2922">The available options are <strong>Action</strong> and <strong>URL</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2923">モデル</span><span class="sxs-lookup"><span data-stu-id="93299-2923">Model</span></span></td>
<td><span data-ttu-id="93299-2924">モデルを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2924">Specify the model.</span></span> <span data-ttu-id="93299-2925">モデルは、レイヤー内の要素の論理グループです。</span><span class="sxs-lookup"><span data-stu-id="93299-2925">A model is a logical grouping of elements in a layer.</span></span> <span data-ttu-id="93299-2926">要素例には、テーブルまたはクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="93299-2926">Examples of elements include a table or class.</span></span> <span data-ttu-id="93299-2927">要素は、レイヤー内の 1 つのモデルに正確に存在します。</span><span class="sxs-lookup"><span data-stu-id="93299-2927">An element can exist in exactly one model in a layer.</span></span> <span data-ttu-id="93299-2928">上位層にあるモデルのカスタマイズされたバージョンに、同じ要素が存在できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2928">The same element can exist in a customized version in a model that is in a higher layer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2929">SetCompany</span><span class="sxs-lookup"><span data-stu-id="93299-2929">SetCompany</span></span></td>
<td><span data-ttu-id="93299-2930">このプロパティは、フォームがフォーカスを受け取ったときにシステムを変更します。</span><span class="sxs-lookup"><span data-stu-id="93299-2930">This property causes the system to change the company when the form receives focus.</span></span> <span data-ttu-id="93299-2931"><strong>SaveDataPerCompany</strong> プロパティが <strong>はい</strong> に設定されている場合、テーブルをデータ ソースとして使用するフォーム デザインの <strong>SetCompany</strong> プロパティも <strong>はい</strong> に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-2931">If the <strong>SaveDataPerCompany</strong> property on a table is set to <strong>Yes</strong>, the <strong>SetCompany</strong> property on a form design that uses the table as a data source must also be set to <strong>Yes</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2932">ShowParentModule</span><span class="sxs-lookup"><span data-stu-id="93299-2932">ShowParentModule</span></span></td>
<td><span data-ttu-id="93299-2933">メニュー項目の親モジュールに基づいて QuickLaunch を更新するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2933">Specify whether to update the QuickLaunch, based on the parent module of the menu item.</span></span> <span data-ttu-id="93299-2934"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2934">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2935"><strong>はい </strong>- メニュー項目の親モジュールに基づいて QuickLaunch を常に更新してください。</span><span class="sxs-lookup"><span data-stu-id="93299-2935"><strong>Yes </strong>– Always update the QuickLaunch, based on the parent module of the menu item.</span></span></li>
<li><span data-ttu-id="93299-2936"><strong>いいえ</strong> - メニュー項目の親モジュールが、現在のモジュールと異なる場合でも QuickLaunch を変更せずにそのままにします。</span><span class="sxs-lookup"><span data-stu-id="93299-2936"><strong>No </strong>– Leave the QuickLaunch unchanged, even if the parent module of the menu item differs from the current module.</span></span></li>
</ul>
<span data-ttu-id="93299-2937">既定値は <strong>はい</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-2937">The default value is <strong>Yes</strong>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="web-menu-item-properties"></a><span data-ttu-id="93299-2938">Web メニュー項目のプロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2938">Web menu item properties</span></span>
<span data-ttu-id="93299-2939">次のデーブルでは、Web メニュー項目に固有のプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="93299-2939">The following table describes the properties that are specific to web menu items.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93299-2940">プロパティ</span><span class="sxs-lookup"><span data-stu-id="93299-2940">Property</span></span></th>
<th><span data-ttu-id="93299-2941">説明</span><span class="sxs-lookup"><span data-stu-id="93299-2941">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="93299-2942">ビッグ</span><span class="sxs-lookup"><span data-stu-id="93299-2942">Big</span></span></td>
<td><span data-ttu-id="93299-2943">アクション ウィンドウに使用されるボタンのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2943">Specify the size of the button when it&#39;s used on an Action Pane.</span></span> <span data-ttu-id="93299-2944"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2944">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2945"><strong>はい </strong>- ボタンはフル サイズで表示され、グループの先頭に位置します。</span><span class="sxs-lookup"><span data-stu-id="93299-2945"><strong>Yes </strong>– The button is shown at full size and is located at the start of the group.</span></span></li>
<li><span data-ttu-id="93299-2946"><strong>いいえ</strong> - ボタンは小さいサイズで表示され、グループの右側にあります。</span><span class="sxs-lookup"><span data-stu-id="93299-2946"><strong>No </strong>– The button is shown at the smaller size and is located on the right side of the group.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2947">CloseDialogBehavior</span><span class="sxs-lookup"><span data-stu-id="93299-2947">CloseDialogBehavior</span></span></td>
<td><span data-ttu-id="93299-2948">ダイアログ ボックスが閉じるときに親ウィンドウで実行されるアクションを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2948">Specify the action that is performed on the parent window when the dialog box closes.</span></span> <span data-ttu-id="93299-2949"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2949">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2950"><strong>自動 </strong>- ダイアログ ボックスの使用方法に応じて、適切な更新アクションが、ダイアログ ボックスが閉じたときに実行されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2950"><strong>Auto </strong>– Depending on how the dialog box was used, the appropriate update actions are performed when the dialog box is closed.</span></span></li>
<li><span data-ttu-id="93299-2951"><strong>RefreshDataSource </strong>- 親フォーム上の読み取り専用データ ソースは更新されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2951"><strong>RefreshDataSource </strong>– The read-only data source on the parent form is updated.</span></span> <span data-ttu-id="93299-2952">このオプションは、現在の選択を保存し、データソースに対して <strong>Research()</strong> 操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="93299-2952">This option preserves the current selection and performs a <strong>Research()</strong> operation on the data source.</span></span></li>
<li><span data-ttu-id="93299-2953"><strong>RefreshPage </strong>- ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="93299-2953"><strong>RefreshPage </strong>– Refresh the page.</span></span></li>
<li><span data-ttu-id="93299-2954"><strong>送信 </strong>- 親ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="93299-2954"><strong>Submit </strong>– Refresh the parent page.</span></span></li>
<li><span data-ttu-id="93299-2955"><strong>なし </strong>- アクションは実行されません。</span><span class="sxs-lookup"><span data-stu-id="93299-2955"><strong>None </strong>– No action is performed.</span></span></li>
</ul>
<span data-ttu-id="93299-2956">既定値は <strong>自動</strong> です。</span><span class="sxs-lookup"><span data-stu-id="93299-2956">The default value is <strong>Auto</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2957">HideActionPane</span><span class="sxs-lookup"><span data-stu-id="93299-2957">HideActionPane</span></span></td>
<td><span data-ttu-id="93299-2958">開いているページにアクション ウィンドウを表示するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2958">Specify whether the Action Pane is visible on the page that is being opened.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2959">ホームページ</span><span class="sxs-lookup"><span data-stu-id="93299-2959">HomePage</span></span></td>
<td><span data-ttu-id="93299-2960">ページがロール センター ページであり、メイン エンタープライズ ポータル サイトに配置されるかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2960">Specify whether the page is a Role Center page and is deployed to the main Enterprise Portal site.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2961">NeedsRecord</span><span class="sxs-lookup"><span data-stu-id="93299-2961">NeedsRecord</span></span></td>
<td><span data-ttu-id="93299-2962">このプロパティを<strong>はい</strong>に設定すると、データ セットにレコードがないとき、メニュー項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2962">When you set this property to <strong>Yes</strong>, the menu item is shown when there are no records in the data set.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2963">PageDefinition</span><span class="sxs-lookup"><span data-stu-id="93299-2963">PageDefinition</span></span></td>
<td><span data-ttu-id="93299-2964">Web メニュー項目が指し示すページ。</span><span class="sxs-lookup"><span data-stu-id="93299-2964">The page that the web menu item points to.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2965">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93299-2965">Parameters</span></span></td>
<td><span data-ttu-id="93299-2966">開いているページに渡される引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2966">Specify the arguments that are passed to the page that is being opened.</span></span> <span data-ttu-id="93299-2967">各パラメーターは以下のフォーム<em>名前</em>=<em>値</em>を必要とします。また複数のパラメーターを渡す場合、次の例に示すように、アンパサンド (&amp;) で区切らなくてはなりません。例: mode=2&amp;category=1</span><span class="sxs-lookup"><span data-stu-id="93299-2967">Each parameter must have the following form: <em>name</em>=<em>value</em> If multiple parameters must be passed, they must be separated by an ampersand (&amp;), as shown in the following example: mode=2&amp;category=1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2968">URL</span><span class="sxs-lookup"><span data-stu-id="93299-2968">URL</span></span></td>
<td><span data-ttu-id="93299-2969">移動先の URL を指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2969">Specify the URL to navigate to.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2970">WebConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="93299-2970">WebConfigurationKey</span></span></td>
<td><span data-ttu-id="93299-2971">Web メニュー項目を有効にするために必要なコンフィギュレーション キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="93299-2971">Select the configuration key that is required in order to enable the web menu item.</span></span> <span data-ttu-id="93299-2972">オブジェクトが属しているモジュールのキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="93299-2972">Use the key for the module that the object belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2973">WindowMode</span><span class="sxs-lookup"><span data-stu-id="93299-2973">WindowMode</span></span></td>
<td><span data-ttu-id="93299-2974">開いているページに使用するウィンドウのタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2974">Specify the type of window to use for the page that is being opened.</span></span> <span data-ttu-id="93299-2975"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2975">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2976"><strong>インライン</strong> - 開いているページは、ブラウザの既存の内容に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="93299-2976"><strong>Inline </strong>– The page that is being opened will replace the existing content in the browser.</span></span> <span data-ttu-id="93299-2977">Web メニュー項目にダイアログ ボックスからアクセスしている場合、新しいブラウザー ウィンドウで開くページが開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-2977">If the web menu item is being accessed from a dialog box, the page that is being opened will open in a new browser window.</span></span></li>
<li><span data-ttu-id="93299-2978"><strong>モーダル</strong> - 開いているダイアログ ボックスがない場合は、新しいダイアログ ボックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="93299-2978"><strong>Modal </strong>– If no dialog box is open, a new dialog box will be created.</span></span> <span data-ttu-id="93299-2979">Web メニュー項目にダイアログ ボックスからアクセスしている場合、現在のダイアログ ボックスのコンテンツが開いているページに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="93299-2979">If the web menu item is being accessed from a dialog box, the page that is being opened will replace the content of the current dialog box.</span></span></li>
<li><span data-ttu-id="93299-2980"><strong>NewModal</strong> - 開いているページは常に新しいダイアログ ボックスで開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-2980"><strong>NewModal </strong>– The page that is being opened will always open in a new dialog box.</span></span></li>
<li><span data-ttu-id="93299-2981"><strong>NewWindow</strong> - 開いているページは新しいブラウザー ウィンドウで開きます。</span><span class="sxs-lookup"><span data-stu-id="93299-2981"><strong>NewWindow </strong>– The page that is being opened will open in a new browser window.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="93299-2982">WindowParameters</span><span class="sxs-lookup"><span data-stu-id="93299-2982">WindowParameters</span></span></td>
<td><span data-ttu-id="93299-2983">SharePoint ダイアログ ボックスの外観を制御する追加のパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2983">Specify additional parameters to control the appearance of the SharePoint dialog box.</span></span> <span data-ttu-id="93299-2984">パラメータは、かっこ ({}) で囲み、コンマで区切る必要があります。</span><span class="sxs-lookup"><span data-stu-id="93299-2984">The parameters must be enclosed in braces ({}) and separated by commas.</span></span> <span data-ttu-id="93299-2985">次の例は、ダイアログボックスのサイズが 400 × 300 ピクセルになり、<strong>閉じる</strong> ボタンまたは <strong>最大化</strong> ボタンが表示されるように <strong>WindowParameters</strong> プロパティを設定する方法を示しています。{幅: 400、高さ: 300、showClose: false、allowMaximize: false}</span><span class="sxs-lookup"><span data-stu-id="93299-2985">The following example shows how to set the <strong>WindowParameters</strong> property so that the dialog box has a size of 400 × 300 pixels, and so that it has no <strong>Close</strong> or <strong>Maximize</strong> button: {width:400, height:300, showClose:false, allowMaximize:false}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="93299-2986">WindowSize</span><span class="sxs-lookup"><span data-stu-id="93299-2986">WindowSize</span></span></td>
<td><span data-ttu-id="93299-2987">開いているページに使用するウィンドウのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="93299-2987">Specify the size of the window to use for the page that is being opened.</span></span> <span data-ttu-id="93299-2988"> 次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="93299-2988">The following options are available:</span></span>
<ul>
<li><span data-ttu-id="93299-2989"><strong>最小 </strong>- 330 × 200 ピクセル</span><span class="sxs-lookup"><span data-stu-id="93299-2989"><strong>Smallest </strong>– 330 × 200 pixels</span></span></li>
<li><span data-ttu-id="93299-2990"><strong>小 </strong>- 550 × 450 ピクセル</span><span class="sxs-lookup"><span data-stu-id="93299-2990"><strong>Small </strong>– 550 × 450 pixels</span></span></li>
<li><span data-ttu-id="93299-2991"><strong>中</strong> - 800 × 630 ピクセル</span><span class="sxs-lookup"><span data-stu-id="93299-2991"><strong>Medium </strong>– 800 × 630 pixels</span></span></li>
<li><span data-ttu-id="93299-2992"><strong>大</strong> - 930 × 630 ピクセル</span><span class="sxs-lookup"><span data-stu-id="93299-2992"><strong>Large </strong>– 930 × 630 pixels</span></span></li>
<li><span data-ttu-id="93299-2993"><strong>最大</strong> - メインのブラウザー ウィンドウの境界内に収まる最大のサイズ</span><span class="sxs-lookup"><span data-stu-id="93299-2993"><strong>Maximum </strong>– The largest size that will fit in the boundaries of the main browser window</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





