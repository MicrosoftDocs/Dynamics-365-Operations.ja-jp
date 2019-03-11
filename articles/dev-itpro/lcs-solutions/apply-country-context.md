---
title: 国/地域コンテキストの適用
description: ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは国/地域コンテキストによって制御できるように、すべての国固有または地域固有の機能を実装する必要があります。 この記事では、これらの要件を満たすために、国/地域コンテキストを適用する方法について説明します。 この記事では、国コンテキスト プロパティを使用する方法と、どのようなアプリケーション オブジェクトがユーザー インターフェイス要素を制御するのかに関する情報を確認できます。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 21681
ms.assetid: d02eee15-bbeb-4e0f-a59f-0313da9334da
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62dc6a69f859963b69907cde175d94f2b852a656
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368461"
---
# <a name="apply-countryregion-context"></a><span data-ttu-id="9342f-105">国/地域コンテキストの適用</span><span class="sxs-lookup"><span data-stu-id="9342f-105">Apply country/region context</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9342f-106">ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは国/地域コンテキストによって制御できるように、すべての国固有または地域固有の機能を実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9342f-106">As part of the requirements for LCS solutions for localization &amp; translation, localization ISV solution providers must implement all country-specific or region-specific functionality so that it can be controlled by country/region context.</span></span> <span data-ttu-id="9342f-107">この記事では、これらの要件を満たすために、国/地域コンテキストを適用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9342f-107">This article describes how to apply country/region context to meet these requirements.</span></span> <span data-ttu-id="9342f-108">この記事では、国コンテキスト プロパティを使用する方法と、どのようなアプリケーション オブジェクトがユーザー インターフェイス要素を制御するのかに関する情報を確認できます。</span><span class="sxs-lookup"><span data-stu-id="9342f-108">In this article you can find information how you should use country context property and what application objects control user interface elements.</span></span>

## <a name="countryregion-specific-functionality"></a><span data-ttu-id="9342f-109">国/地域固有の機能</span><span class="sxs-lookup"><span data-stu-id="9342f-109">Country/region-specific functionality</span></span>

<span data-ttu-id="9342f-110">個々の地域の法律、規制、ビジネス要件への対応を容易にするために、国/地域に固有の機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="9342f-110">You use country/region-specific functionality to help meet the legal, regulatory, and business requirements of individual geographies.</span></span> <span data-ttu-id="9342f-111">地理は、国際標準化機構 (ISO) の国/地域コードで識別されている任意の国または地域です。</span><span class="sxs-lookup"><span data-stu-id="9342f-111">A geography is any country or region that is identified by an International Organization for Standardization (ISO) country or region code.</span></span> <span data-ttu-id="9342f-112">Microsoft Dynamics 365 for Finance and Operations では、国/地域のコンテキストを使用します。</span><span class="sxs-lookup"><span data-stu-id="9342f-112">In Microsoft Dynamics 365 for Finance and Operations, you use country/region context.</span></span> <span data-ttu-id="9342f-113">次のテーブルでは、国/地域固有の機能をコンフィギュレーションするために使用する主要な要素について説明します。</span><span class="sxs-lookup"><span data-stu-id="9342f-113">The following table highlights the main elements that you use to configure country/region-specific functionality.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9342f-114">要素</span><span class="sxs-lookup"><span data-stu-id="9342f-114">Element</span></span></th>
<th><span data-ttu-id="9342f-115">説明</span><span class="sxs-lookup"><span data-stu-id="9342f-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9342f-116">制御されたエンティティ</span><span class="sxs-lookup"><span data-stu-id="9342f-116">Controlled entity</span></span></td>
<td><span data-ttu-id="9342f-117">制御されたエンティティは、その国/地域のコンテキストが制御エンティティの国/地域のコンテキストと一致するかどうかによって、非表示または表示される UI 要素です。</span><span class="sxs-lookup"><span data-stu-id="9342f-117">The controlled entity is a UI element that is hidden or shown, depending on whether its country/region context matches the country/region context of the controlling entity.</span></span> <span data-ttu-id="9342f-118">国/地域のコンテキストに基づくメニュー、メニュー項目、フォーム コントロールを非表示にするために、一部の要素で、コントロールされたエンティティに <strong>CountryRegionCodes</strong> プロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9342f-118">To enable menus, menu items, and form controls that are based on country/region context to be hidden, a controlled entity includes a <strong>CountryRegionCodes</strong> property on some elements.</span></span> <span data-ttu-id="9342f-119">このプロパティを使用して、要素が表示される国または地域を指定します。</span><span class="sxs-lookup"><span data-stu-id="9342f-119">You use this property to specify the country or region where the element is shown.</span></span> <span data-ttu-id="9342f-120">次のアプリケーション オブジェクト ツリー (AOT) 要素で <strong>CountryRegionCodes</strong> プロパティを検索します。</span><span class="sxs-lookup"><span data-stu-id="9342f-120">You find the <strong>CountryRegionCodes</strong> property on the following Application Object Tree (AOT) elements:</span></span>
<ul>
<li><span data-ttu-id="9342f-121">拡張データ型</span><span class="sxs-lookup"><span data-stu-id="9342f-121">Extended data type</span></span></li>
<li><span data-ttu-id="9342f-122">メニューとメニュー項目</span><span class="sxs-lookup"><span data-stu-id="9342f-122">Menu and menu items</span></span></li>
<li><span data-ttu-id="9342f-123">列挙と列挙値</span><span class="sxs-lookup"><span data-stu-id="9342f-123">Enum and enum value</span></span></li>
<li><span data-ttu-id="9342f-124">テーブルとテーブル フィールド</span><span class="sxs-lookup"><span data-stu-id="9342f-124">Table and table field</span></span></li>
<li><span data-ttu-id="9342f-125">データ エンティティとデータ エンティティ フィールド</span><span class="sxs-lookup"><span data-stu-id="9342f-125">Data entity and data entity field</span></span></li>
<li><span data-ttu-id="9342f-126">表示と表示フィールド</span><span class="sxs-lookup"><span data-stu-id="9342f-126">View and view field</span></span></li>
<li><span data-ttu-id="9342f-127">マップおよびマップ フィールド</span><span class="sxs-lookup"><span data-stu-id="9342f-127">Map and map field</span></span></li>
<li><span data-ttu-id="9342f-128">フォーム コントロール</span><span class="sxs-lookup"><span data-stu-id="9342f-128">Form control</span></span></li>
<li><span data-ttu-id="9342f-129">タイル</span><span class="sxs-lookup"><span data-stu-id="9342f-129">Tile</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9342f-130">制御関係者</span><span class="sxs-lookup"><span data-stu-id="9342f-130">Controlling party</span></span></td>
<td><span data-ttu-id="9342f-131">制御関係者の役割は、国/地域固有の機能または UI 要素が有効かどうかを判断するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-131">The controlling party’s role is used to determine whether country/region-specific functionality or UI elements are enabled.</span></span> <span data-ttu-id="9342f-132">制御関係者は、Finance and Operations の組織モデルによって定義されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-132">The controlling party is defined by the Organization model in Finance and Operations.</span></span> <span data-ttu-id="9342f-133">例には、法人、顧客、仕入先、銀行、または作業者が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9342f-133">Examples include legal entity, customer, vendor, bank, or worker.</span></span> <span data-ttu-id="9342f-134">既定では、法人が管理関係者として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-134">By default, the legal entity is used as the controlling party.</span></span> <span data-ttu-id="9342f-135">制御の関係者の国/地域のコンテキストでは、コントロールのエンティティの国/地域コンテキストが一致すると、機能または UI 要素が有効になります。</span><span class="sxs-lookup"><span data-stu-id="9342f-135">If the country/region context of the controlling party matches the country/region context of the controlled entity, the functionality or UI elements are enabled.</span></span> <span data-ttu-id="9342f-136">制御関係者の国/地域コンテキストを設定します。</span><span class="sxs-lookup"><span data-stu-id="9342f-136">You set the country/region context of the controlling party.</span></span> <span data-ttu-id="9342f-137">一致する国/地域のコンテキストを持つ制御されたエンティティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-137">Any controlled entities that have a matching country/region context are shown.</span></span></td>
</tr>
</tbody>
</table>

## <a name="using-the-countryregioncodes-property"></a><span data-ttu-id="9342f-138">CountryRegionCodes プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="9342f-138">Using the CountryRegionCodes property</span></span>
<span data-ttu-id="9342f-139">制御されたエンティティで国/地域コンテキストを作成するには、**CountryRegionCodes** プロパティで ISO コード値の設定します。</span><span class="sxs-lookup"><span data-stu-id="9342f-139">You create country/region context on a controlled entity by setting the ISO code value on the **CountryRegionCodes** property.</span></span> <span data-ttu-id="9342f-140">ISO 国および地域コードの一覧は [ここ](http://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm) で見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="9342f-140">You can find the list of ISO country and region codes [here](http://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm).</span></span> <span data-ttu-id="9342f-141">Microsoft Dynamics 365 for Finance and Operations は、**CountryRegionCodes** プロパティの値を管理関係者の国/地域コンテキストと比較します。</span><span class="sxs-lookup"><span data-stu-id="9342f-141">Microsoft Dynamics 365 for Finance and Operations compares the values of the **CountryRegionCodes** property to the country/region context of the controlling party.</span></span> <span data-ttu-id="9342f-142">値が一致した場合は、要素が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-142">If the values match, the element is shown.</span></span> <span data-ttu-id="9342f-143">それ以外の場合、表示されません。</span><span class="sxs-lookup"><span data-stu-id="9342f-143">Otherwise, it's hidden.</span></span> <span data-ttu-id="9342f-144">**ヒント:** **CountryRegionCodes** プロパティに複数の ISO 国および地域コードを追加するには、コンマ区切りのリストを使用します。</span><span class="sxs-lookup"><span data-stu-id="9342f-144">**Tip:** To add more than one ISO country and region code to the **CountryRegionCodes** property, use a comma-separated list.</span></span>

## <a name="using-the-legal-entity-as-the-controlling-party"></a><span data-ttu-id="9342f-145">法人を管理関係者として使用</span><span class="sxs-lookup"><span data-stu-id="9342f-145">Using the legal entity as the controlling party</span></span>
<span data-ttu-id="9342f-146">法人のプライマリ住所の **国/地域** 値により、制御側関係者の国/地域コンテキストが決定されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-146">The **Country/region** value in the primary address of the legal entity determines the country/region context of the controlling party.</span></span> <span data-ttu-id="9342f-147">**国/地域** フィールドの既定値は、Finance and Operations クライアントのロケールです。</span><span class="sxs-lookup"><span data-stu-id="9342f-147">The default value of the **Country/region** field is the locale of the Finance and Operations client.</span></span> <span data-ttu-id="9342f-148">次の図は、法人の基本住所を設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9342f-148">The following illustration shows how to set the primary address of the legal entity.</span></span> <span data-ttu-id="9342f-149">[![LE\_Edit\_address](./media/le_edit_address-1024x570.jpg)](./media/le_edit_address.jpg)</span><span class="sxs-lookup"><span data-stu-id="9342f-149">[![LE\_Edit\_address](./media/le_edit_address-1024x570.jpg)](./media/le_edit_address.jpg)</span></span>

## <a name="setting-another-party-as-the-controlling-party"></a><span data-ttu-id="9342f-150">別の当事者を管理側の関係者として設定</span><span class="sxs-lookup"><span data-stu-id="9342f-150">Setting another party as the controlling party</span></span>
<span data-ttu-id="9342f-151">顧客、銀行、または仕入先などの、別の関係者を制御関係者として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9342f-151">You can use another party, such as a customer, bank, or vendor, as a controlling party.</span></span> <span data-ttu-id="9342f-152">たとえば、特定の国/地域の顧客に対して対象となる機能を有効化する、または特定の国/地域から仕入先の固有の検証を必要とすることができます。</span><span class="sxs-lookup"><span data-stu-id="9342f-152">For example, you can enable targeted functionality for customers of a specific country/region or require specific validation of vendors from a specific country/region.</span></span> <span data-ttu-id="9342f-153">管理者を設定するには、フォーム、コントロール、またはその他の要素の **CountryRegionContextField** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="9342f-153">To set the controlling party, use the **CountryRegionContextField** property of the form, control, or other element.</span></span> <span data-ttu-id="9342f-154">このプロパティを使用すると、管理関係者であるエンティティを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9342f-154">This property lets you select the entity that is the controlling party.</span></span> <span data-ttu-id="9342f-155">既定値は法人です。</span><span class="sxs-lookup"><span data-stu-id="9342f-155">The default value is the legal entity.</span></span> <span data-ttu-id="9342f-156">次の図は、フィールドに **CountryRegionContextField** プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="9342f-156">The following illustration shows how to set the **CountryRegionContextField** property for a field.</span></span> 
<span data-ttu-id="9342f-157">[![DE\_CountryRegionContextField](./media/de_countryregioncontextfield.jpg)](./media/de_countryregioncontextfield.jpg)</span><span class="sxs-lookup"><span data-stu-id="9342f-157">[![DE\_CountryRegionContextField](./media/de_countryregioncontextfield.jpg)](./media/de_countryregioncontextfield.jpg)</span></span> 

<span data-ttu-id="9342f-158">この例では、顧客が制御エンティティになります。</span><span class="sxs-lookup"><span data-stu-id="9342f-158">In this example, the customer becomes the controlling entity.</span></span> <span data-ttu-id="9342f-159">顧客の住所が **CountryRegionCodes** フィールドの値と比較され、**GermanSpecifcSetting** フィールドが表示されているかどうかが判別されます。</span><span class="sxs-lookup"><span data-stu-id="9342f-159">The customer's address is compared with the value of the **CountryRegionCodes** field to determine whether the **GermanSpecifcSetting** field is displayed.</span></span>

<a name="additional-resources"></a><span data-ttu-id="9342f-160">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9342f-160">Additional resources</span></span>
--------

[<span data-ttu-id="9342f-161">ISO コード</span><span class="sxs-lookup"><span data-stu-id="9342f-161">ISO codes</span></span>](http://www.iso.org/iso/country_codes/iso_3166_code_lists/country_names_and_code_elements.htm)



