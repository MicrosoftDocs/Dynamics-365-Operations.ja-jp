---
title: 国/地域コンテキストの適用
description: このトピックでは、ローカライズおよび翻訳要件を満たすために国/地域コンテキストを適用する方法に関する情報を提供します。 このトピックで、国コンテキスト プロパティを使用する方法と、どのようなアプリケーション オブジェクトがユーザー インターフェイス要素を制御するかに関する情報を確認できます。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom: 21681
ms.assetid: d02eee15-bbeb-4e0f-a59f-0313da9334da
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1dbeb11e639f1b4c496d90498d6e24bc5a43b47d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685071"
---
# <a name="apply-countryregion-context"></a><span data-ttu-id="5e9c6-104">国/地域コンテキストの適用</span><span class="sxs-lookup"><span data-stu-id="5e9c6-104">Apply country/region context</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e9c6-105">ローカライズおよび翻訳向け LCS ソリューション要件の一部として、ローカライズ ISV ソリューション プロバイダーは国/地域コンテキストによって制御できるように、すべての国または地域固有の機能を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-105">As part of the requirements for LCS solutions for localization and translation, localization ISV solution providers must implement all country-specific or region-specific functionality so that it can be controlled by country/region context.</span></span> <span data-ttu-id="5e9c6-106">この記事では、これらの要件を満たすために、国/地域コンテキストを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-106">This article describes how to apply country/region context to meet these requirements.</span></span> <span data-ttu-id="5e9c6-107">この記事では、国コンテキスト プロパティを使用する方法と、どのようなアプリケーション オブジェクトがユーザー インターフェイス要素を制御するのかに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-107">In this article you can find information how you should use country context property and what application objects control user interface elements.</span></span>

## <a name="countryregion-specific-functionality"></a><span data-ttu-id="5e9c6-108">国/地域固有の機能</span><span class="sxs-lookup"><span data-stu-id="5e9c6-108">Country/region-specific functionality</span></span>

<span data-ttu-id="5e9c6-109">個々の地域の法律、規制、ビジネス要件への対応を容易にするために、国/地域に固有の機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-109">You use country/region-specific functionality to help meet the legal, regulatory, and business requirements of individual geographies.</span></span> <span data-ttu-id="5e9c6-110">地理は、国際標準化機構 (ISO) の国/地域コードで識別されている任意の国または地域です。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-110">A geography is any country or region that is identified by an International Organization for Standardization (ISO) country or region code.</span></span> <span data-ttu-id="5e9c6-111">次のテーブルでは、国/地域固有の機能をコンフィギュレーションするために使用する主要な要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-111">The following table highlights the main elements that you use to configure country/region-specific functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5e9c6-112">要素</span><span class="sxs-lookup"><span data-stu-id="5e9c6-112">Element</span></span></th>
<th><span data-ttu-id="5e9c6-113">説明</span><span class="sxs-lookup"><span data-stu-id="5e9c6-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5e9c6-114">制御されたエンティティ</span><span class="sxs-lookup"><span data-stu-id="5e9c6-114">Controlled entity</span></span></td>
<td><span data-ttu-id="5e9c6-115">制御されたエンティティは、その国/地域のコンテキストが制御エンティティの国/地域のコンテキストと一致するかどうかによって、非表示または表示される UI 要素です。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-115">The controlled entity is a UI element that is hidden or shown, depending on whether its country/region context matches the country/region context of the controlling entity.</span></span> <span data-ttu-id="5e9c6-116">国/地域のコンテキストに基づくメニュー、メニュー項目、フォーム コントロールを非表示にするために、一部の要素で、コントロールされたエンティティに <strong>CountryRegionCodes</strong> プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-116">To enable menus, menu items, and form controls that are based on country/region context to be hidden, a controlled entity includes a <strong>CountryRegionCodes</strong> property on some elements.</span></span> <span data-ttu-id="5e9c6-117">このプロパティを使用して、要素が表示される国または地域を指定します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-117">You use this property to specify the country or region where the element is shown.</span></span> <span data-ttu-id="5e9c6-118">次のアプリケーション オブジェクト ツリー (AOT) 要素で <strong>CountryRegionCodes</strong> プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-118">You find the <strong>CountryRegionCodes</strong> property on the following Application Object Tree (AOT) elements:</span></span>
<ul>
<li><span data-ttu-id="5e9c6-119">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="5e9c6-119">Extended data type</span></span></li>
<li><span data-ttu-id="5e9c6-120">メニューとメニュー項目</span><span class="sxs-lookup"><span data-stu-id="5e9c6-120">Menu and menu items</span></span></li>
<li><span data-ttu-id="5e9c6-121">列挙と列挙値</span><span class="sxs-lookup"><span data-stu-id="5e9c6-121">Enum and enum value</span></span></li>
<li><span data-ttu-id="5e9c6-122">テーブルとテーブル フィールド</span><span class="sxs-lookup"><span data-stu-id="5e9c6-122">Table and table field</span></span></li>
<li><span data-ttu-id="5e9c6-123">データ エンティティとデータ エンティティ フィールド</span><span class="sxs-lookup"><span data-stu-id="5e9c6-123">Data entity and data entity field</span></span></li>
<li><span data-ttu-id="5e9c6-124">表示と表示フィールド</span><span class="sxs-lookup"><span data-stu-id="5e9c6-124">View and view field</span></span></li>
<li><span data-ttu-id="5e9c6-125">マップおよびマップ フィールド</span><span class="sxs-lookup"><span data-stu-id="5e9c6-125">Map and map field</span></span></li>
<li><span data-ttu-id="5e9c6-126">フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="5e9c6-126">Form control</span></span></li>
<li><span data-ttu-id="5e9c6-127">タイル</span><span class="sxs-lookup"><span data-stu-id="5e9c6-127">Tile</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5e9c6-128">制御関係者</span><span class="sxs-lookup"><span data-stu-id="5e9c6-128">Controlling party</span></span></td>
<td><span data-ttu-id="5e9c6-129">制御関係者の役割は、国/地域固有の機能または UI 要素が有効かどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-129">The controlling party’s role is used to determine whether country/region-specific functionality or UI elements are enabled.</span></span> <span data-ttu-id="5e9c6-130">制御関係者は、組織モデルによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-130">The controlling party is defined by the Organization model.</span></span> <span data-ttu-id="5e9c6-131">例には、法人、顧客、仕入先、銀行、または作業者が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-131">Examples include legal entity, customer, vendor, bank, or worker.</span></span> <span data-ttu-id="5e9c6-132">既定では、法人が管理関係者として使用されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-132">By default, the legal entity is used as the controlling party.</span></span> <span data-ttu-id="5e9c6-133">制御の関係者の国/地域のコンテキストでは、コントロールのエンティティの国/地域コンテキストが一致すると、機能または UI 要素が有効になります。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-133">If the country/region context of the controlling party matches the country/region context of the controlled entity, the functionality or UI elements are enabled.</span></span> <span data-ttu-id="5e9c6-134">制御関係者の国/地域コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-134">You set the country/region context of the controlling party.</span></span> <span data-ttu-id="5e9c6-135">一致する国/地域のコンテキストを持つ制御されたエンティティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-135">Any controlled entities that have a matching country/region context are shown.</span></span></td>
</tr>
</tbody>
</table>

## <a name="using-the-countryregioncodes-property"></a><span data-ttu-id="5e9c6-136">CountryRegionCodes プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="5e9c6-136">Using the CountryRegionCodes property</span></span>
<span data-ttu-id="5e9c6-137">制御されたエンティティで国/地域コンテキストを作成するには、**CountryRegionCodes** プロパティで ISO コード値の設定します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-137">You create country/region context on a controlled entity by setting the ISO code value on the **CountryRegionCodes** property.</span></span> <span data-ttu-id="5e9c6-138">ISO の国および地域コードの一覧は [ISO の Web サイト](https://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm) にあります。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-138">You can find the list of ISO country and region codes on the [ISO website](https://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm).</span></span> <span data-ttu-id="5e9c6-139">**CountryRegionCodes** プロパティの値を管理関係者の国/地域コンテキストと比較します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-139">The values of the **CountryRegionCodes** property are compared to the country/region context of the controlling party.</span></span> <span data-ttu-id="5e9c6-140">値が一致した場合は、要素が表示されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-140">If the values match, the element is shown.</span></span> <span data-ttu-id="5e9c6-141">それ以外の場合、表示されません。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-141">Otherwise, it's hidden.</span></span>

> [!TIP]
> <span data-ttu-id="5e9c6-142">**CountryRegionCodes** プロパティに複数の ISO 国および地域コードを追加するには、コンマ区切りのリストを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-142">To add more than one ISO country and region code to the **CountryRegionCodes** property, use a comma-separated list.</span></span>

## <a name="using-the-legal-entity-as-the-controlling-party"></a><span data-ttu-id="5e9c6-143">法人を管理関係者として使用</span><span class="sxs-lookup"><span data-stu-id="5e9c6-143">Using the legal entity as the controlling party</span></span>
<span data-ttu-id="5e9c6-144">法人のプライマリ住所の **国/地域** 値により、制御側関係者の国/地域コンテキストが決定されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-144">The **Country/region** value in the primary address of the legal entity determines the country/region context of the controlling party.</span></span> <span data-ttu-id="5e9c6-145">**国/地域** フィールドの既定値は、システムのロケールです。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-145">The default value of the **Country/region** field is the locale of the system.</span></span> <span data-ttu-id="5e9c6-146">次の図は、法人の基本住所を設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-146">The following illustration shows how to set the primary address of the legal entity.</span></span> <span data-ttu-id="5e9c6-147">[![LE\_Edit\_address](./media/le_edit_address-1024x570.jpg)](./media/le_edit_address.jpg)</span><span class="sxs-lookup"><span data-stu-id="5e9c6-147">[![LE\_Edit\_address](./media/le_edit_address-1024x570.jpg)](./media/le_edit_address.jpg)</span></span>

## <a name="setting-another-party-as-the-controlling-party"></a><span data-ttu-id="5e9c6-148">別の当事者を管理側の関係者として設定</span><span class="sxs-lookup"><span data-stu-id="5e9c6-148">Setting another party as the controlling party</span></span>
<span data-ttu-id="5e9c6-149">顧客、銀行、または仕入先などの、別の関係者を制御関係者として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-149">You can use another party, such as a customer, bank, or vendor, as a controlling party.</span></span> <span data-ttu-id="5e9c6-150">たとえば、特定の国/地域の顧客に対して対象となる機能を有効化する、または特定の国/地域から仕入先の固有の検証を必要とすることができます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-150">For example, you can enable targeted functionality for customers of a specific country/region or require specific validation of vendors from a specific country/region.</span></span> <span data-ttu-id="5e9c6-151">管理者を設定するには、フォーム、コントロール、またはその他の要素の **CountryRegionContextField** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-151">To set the controlling party, use the **CountryRegionContextField** property of the form, control, or other element.</span></span> <span data-ttu-id="5e9c6-152">このプロパティを使用すると、管理関係者であるエンティティを選択できます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-152">This property lets you select the entity that is the controlling party.</span></span> <span data-ttu-id="5e9c6-153">既定値は法人です。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-153">The default value is the legal entity.</span></span> <span data-ttu-id="5e9c6-154">次の図は、フィールドに **CountryRegionContextField** プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-154">The following illustration shows how to set the **CountryRegionContextField** property for a field.</span></span> 
<span data-ttu-id="5e9c6-155">[![DE\_CountryRegionContextField](./media/de_countryregioncontextfield.jpg)](./media/de_countryregioncontextfield.jpg)</span><span class="sxs-lookup"><span data-stu-id="5e9c6-155">[![DE\_CountryRegionContextField](./media/de_countryregioncontextfield.jpg)](./media/de_countryregioncontextfield.jpg)</span></span> 

<span data-ttu-id="5e9c6-156">この例では、顧客が制御エンティティになります。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-156">In this example, the customer becomes the controlling entity.</span></span> <span data-ttu-id="5e9c6-157">顧客の住所が **CountryRegionCodes** フィールドの値と比較され、**GermanSpecifcSetting** フィールドが表示されているかどうかが判別されます。</span><span class="sxs-lookup"><span data-stu-id="5e9c6-157">The customer's address is compared with the value of the **CountryRegionCodes** field to determine whether the **GermanSpecifcSetting** field is displayed.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5e9c6-158">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="5e9c6-158">Additional resources</span></span>
--------

[<span data-ttu-id="5e9c6-159">ISO コード</span><span class="sxs-lookup"><span data-stu-id="5e9c6-159">ISO codes</span></span>](https://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm)



