---
title: 属性および属性グループ
description: このトピックでは、ユーザー定義フィールドを通して製品およびその特性を説明する方法を提供する、属性の使用方法について説明します。
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 76b78a898a619f1bc7faa4749e5380a0ccfef527
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552720"
---
# <a name="attributes-and-attribute-groups"></a><span data-ttu-id="52eae-103">属性および属性グループ</span><span class="sxs-lookup"><span data-stu-id="52eae-103">Attributes and attribute groups</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="52eae-104">*属性*は、製品とユーザー定義フィールドによる特性をさらに記述する方法を提供 (たとえば、**メモリ サイズ**、**ハード ディスク能力**、**エネルギー スター対応**など)。</span><span class="sxs-lookup"><span data-stu-id="52eae-104">*Attributes* provide a way to further describe a product and its characteristics through user-defined fields (such as **Memory size**, **Hard disk capacity**, **Is Energy star compliant**, and so on).</span></span> <span data-ttu-id="52eae-105">Microsoft Dynamics 365 for Finance and Operations にて、属性は製品カテゴリ、小売チャンネルなどのさまざまな小売エンティティに関連付けられており、それらに対して既定値を設定できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-105">In Microsoft Dynamics 365 for Finance and Operations, attributes can be associated with various Retail entities, such as product categories and retail channels, and default values can be set for them.</span></span> <span data-ttu-id="52eae-106">製品は、製品カテゴリまたは小売チャンネルに関連付けられる場合、その属性と既定値を継承します。</span><span class="sxs-lookup"><span data-stu-id="52eae-106">Products then inherit the attributes and the default values when they are associated with the product categories or retail channels.</span></span> <span data-ttu-id="52eae-107">既定値は、個々の製品レベルや小売チャンネル レベル、または小売カタログで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-107">The default values can be overridden at the individual product level, at the retail channel level, or in a retail catalog.</span></span>

<span data-ttu-id="52eae-108">例えば、典型的なテレビ番組は、以下の属性を有することがあります。</span><span class="sxs-lookup"><span data-stu-id="52eae-108">For example, a typical television product might have the following attributes.</span></span>

| <span data-ttu-id="52eae-109">カテゴリ</span><span class="sxs-lookup"><span data-stu-id="52eae-109">Category</span></span>   | <span data-ttu-id="52eae-110">属性</span><span class="sxs-lookup"><span data-stu-id="52eae-110">Attribute</span></span>                | <span data-ttu-id="52eae-111">許容値</span><span class="sxs-lookup"><span data-stu-id="52eae-111">Permissible values</span></span>          | <span data-ttu-id="52eae-112">既定値</span><span class="sxs-lookup"><span data-stu-id="52eae-112">Default value</span></span> |
|------------|--------------------------|-----------------------------|---------------|
| <span data-ttu-id="52eae-113">テレビ & ビデオ</span><span class="sxs-lookup"><span data-stu-id="52eae-113">TV & Video</span></span> | <span data-ttu-id="52eae-114">ブランド</span><span class="sxs-lookup"><span data-stu-id="52eae-114">Brand</span></span>                    | <span data-ttu-id="52eae-115">有効なブランド値</span><span class="sxs-lookup"><span data-stu-id="52eae-115">Any valid brand value</span></span>       | <span data-ttu-id="52eae-116">None</span><span class="sxs-lookup"><span data-stu-id="52eae-116">None</span></span>          |
| <span data-ttu-id="52eae-117">テレビ</span><span class="sxs-lookup"><span data-stu-id="52eae-117">TV</span></span>         | <span data-ttu-id="52eae-118">スクリーン サイズ</span><span class="sxs-lookup"><span data-stu-id="52eae-118">Screen Size</span></span>              | <span data-ttu-id="52eae-119">20–80 インチ</span><span class="sxs-lookup"><span data-stu-id="52eae-119">20–80 inches</span></span>                | <span data-ttu-id="52eae-120">None</span><span class="sxs-lookup"><span data-stu-id="52eae-120">None</span></span>          |
|            | <span data-ttu-id="52eae-121">[垂直解像度]</span><span class="sxs-lookup"><span data-stu-id="52eae-121">Vertical Resolution</span></span>      | <span data-ttu-id="52eae-122">480i、720p、1080i、または 1080p</span><span class="sxs-lookup"><span data-stu-id="52eae-122">480i, 720p, 1080i, or 1080p</span></span> | <span data-ttu-id="52eae-123">1080p</span><span class="sxs-lookup"><span data-stu-id="52eae-123">1080p</span></span>         |
|            | <span data-ttu-id="52eae-124">画面の更新頻度</span><span class="sxs-lookup"><span data-stu-id="52eae-124">Screen Refresh Rate</span></span>      | <span data-ttu-id="52eae-125">60hz、120hz、または 240hz</span><span class="sxs-lookup"><span data-stu-id="52eae-125">60hz, 120hz, or 240hz</span></span>       | <span data-ttu-id="52eae-126">60hz</span><span class="sxs-lookup"><span data-stu-id="52eae-126">60hz</span></span>          |
|            | <span data-ttu-id="52eae-127">[HDMI 入力]</span><span class="sxs-lookup"><span data-stu-id="52eae-127">HDMI Inputs</span></span>              | <span data-ttu-id="52eae-128">0–10</span><span class="sxs-lookup"><span data-stu-id="52eae-128">0–10</span></span>                        | <span data-ttu-id="52eae-129">3</span><span class="sxs-lookup"><span data-stu-id="52eae-129">3</span></span>             |
|            | <span data-ttu-id="52eae-130">[DVI 入力]</span><span class="sxs-lookup"><span data-stu-id="52eae-130">DVI Inputs</span></span>               | <span data-ttu-id="52eae-131">0–10</span><span class="sxs-lookup"><span data-stu-id="52eae-131">0–10</span></span>                        | <span data-ttu-id="52eae-132">1</span><span class="sxs-lookup"><span data-stu-id="52eae-132">1</span></span>             |
|            | <span data-ttu-id="52eae-133">[複合の入力]</span><span class="sxs-lookup"><span data-stu-id="52eae-133">Composite Inputs</span></span>         | <span data-ttu-id="52eae-134">0–10</span><span class="sxs-lookup"><span data-stu-id="52eae-134">0–10</span></span>                        | <span data-ttu-id="52eae-135">2</span><span class="sxs-lookup"><span data-stu-id="52eae-135">2</span></span>             |
|            | <span data-ttu-id="52eae-136">[コンポーネントの入力]</span><span class="sxs-lookup"><span data-stu-id="52eae-136">Component Inputs</span></span>         | <span data-ttu-id="52eae-137">0–10</span><span class="sxs-lookup"><span data-stu-id="52eae-137">0–10</span></span>                        | <span data-ttu-id="52eae-138">1</span><span class="sxs-lookup"><span data-stu-id="52eae-138">1</span></span>             |
| <span data-ttu-id="52eae-139">LCD</span><span class="sxs-lookup"><span data-stu-id="52eae-139">LCD</span></span>        | <span data-ttu-id="52eae-140">[3D 準備完了]</span><span class="sxs-lookup"><span data-stu-id="52eae-140">3D Ready</span></span>                 | <span data-ttu-id="52eae-141">[はい] または [いいえ]</span><span class="sxs-lookup"><span data-stu-id="52eae-141">Yes or No</span></span>                   | <span data-ttu-id="52eae-142">有</span><span class="sxs-lookup"><span data-stu-id="52eae-142">Yes</span></span>           |
|            | <span data-ttu-id="52eae-143">[3D 有効]</span><span class="sxs-lookup"><span data-stu-id="52eae-143">3D Enabled</span></span>               | <span data-ttu-id="52eae-144">[はい] または [いいえ]</span><span class="sxs-lookup"><span data-stu-id="52eae-144">Yes or No</span></span>                   | <span data-ttu-id="52eae-145">無</span><span class="sxs-lookup"><span data-stu-id="52eae-145">No</span></span>            |
| <span data-ttu-id="52eae-146">プラズマ</span><span class="sxs-lookup"><span data-stu-id="52eae-146">Plasma</span></span>     | <span data-ttu-id="52eae-147">[作業開始の温度]</span><span class="sxs-lookup"><span data-stu-id="52eae-147">Operating Temp From</span></span>      | <span data-ttu-id="52eae-148">32–110 度</span><span class="sxs-lookup"><span data-stu-id="52eae-148">32–110 degrees</span></span>              | <span data-ttu-id="52eae-149">32</span><span class="sxs-lookup"><span data-stu-id="52eae-149">32</span></span>            |
|            | <span data-ttu-id="52eae-150">[作業終了の温度]</span><span class="sxs-lookup"><span data-stu-id="52eae-150">Operating Temp To</span></span>        | <span data-ttu-id="52eae-151">32–110 度</span><span class="sxs-lookup"><span data-stu-id="52eae-151">32–110 degrees</span></span>              | <span data-ttu-id="52eae-152">100</span><span class="sxs-lookup"><span data-stu-id="52eae-152">100</span></span>           |
| <span data-ttu-id="52eae-153">プロジェクション</span><span class="sxs-lookup"><span data-stu-id="52eae-153">Projection</span></span> | <span data-ttu-id="52eae-154">プロジェクションの管の保証</span><span class="sxs-lookup"><span data-stu-id="52eae-154">Projection Tube Warranty</span></span> | <span data-ttu-id="52eae-155">6、12、または 18 か月</span><span class="sxs-lookup"><span data-stu-id="52eae-155">6, 12, or 18 months</span></span>         | <span data-ttu-id="52eae-156">12</span><span class="sxs-lookup"><span data-stu-id="52eae-156">12</span></span>            |
|            | <span data-ttu-id="52eae-157">プロジェクションの管の \#</span><span class="sxs-lookup"><span data-stu-id="52eae-157">\# of Projection Tubes</span></span>   | <span data-ttu-id="52eae-158">1–5</span><span class="sxs-lookup"><span data-stu-id="52eae-158">1–5</span></span>                         | <span data-ttu-id="52eae-159">3</span><span class="sxs-lookup"><span data-stu-id="52eae-159">3</span></span>             |

## <a name="attributes-and-attribute-types"></a><span data-ttu-id="52eae-160">属性と属性タイプ</span><span class="sxs-lookup"><span data-stu-id="52eae-160">Attributes and attribute types</span></span>

<span data-ttu-id="52eae-161">属性は *属性タイプ* をベースにしています。</span><span class="sxs-lookup"><span data-stu-id="52eae-161">Attributes are based on *attribute types*.</span></span> <span data-ttu-id="52eae-162">属性タイプは、特定の属性に入力できるデータのタイプを示します。</span><span class="sxs-lookup"><span data-stu-id="52eae-162">The attribute type identifies the type of data that can be entered for a specific attribute.</span></span> <span data-ttu-id="52eae-163">Finance and Operations は、現在次の属性タイプをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="52eae-163">Finance and Operations currently supports the following attribute types:</span></span>

- <span data-ttu-id="52eae-164">**通貨** – このタイプは、通過の値をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-164">**Currency** – This type supports a currency value.</span></span> <span data-ttu-id="52eae-165">これはバインドできますし (値の範囲をサポートできる) 開いたままにもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-165">It can be bounded (that is, it can support a range of values), or it can be left open.</span></span>
- <span data-ttu-id="52eae-166">**日時** – このタイプは、日付と時刻の値をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-166">**DateTime** – This type supports a date and time value.</span></span> <span data-ttu-id="52eae-167">それはバインドできますし、開いたままにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-167">It can be bounded or left open.</span></span>
- <span data-ttu-id="52eae-168">**小数点** – このタイプは、小数点以下を含む数値をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-168">**Decimal** – This type supports a numerical value that includes decimal places.</span></span> <span data-ttu-id="52eae-169">また、測定単位もサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-169">It also supports a unit of measure.</span></span> <span data-ttu-id="52eae-170">それはバインドできますし、開いたままにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-170">It can be bounded or left open.</span></span>
- <span data-ttu-id="52eae-171">**整数** – このタイプは、数値をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-171">**Integer** – This type supports a numerical value.</span></span> <span data-ttu-id="52eae-172">また、測定単位もサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-172">It also supports a unit of measure.</span></span> <span data-ttu-id="52eae-173">それはバインドできますし、開いたままにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-173">It can be bounded or left open.</span></span>
- <span data-ttu-id="52eae-174">**テキスト** – このタイプは、テキストの値をサポートします。</span><span class="sxs-lookup"><span data-stu-id="52eae-174">**Text** – This type supports a text value.</span></span> <span data-ttu-id="52eae-175">また、事前定義された一連の使用可能な値 (*列挙型* である) がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="52eae-175">It also supports a predefined set of possible values (that is, an *enumeration*).</span></span>
- <span data-ttu-id="52eae-176">**ブール値** – このタイプは、バイナリ値をサポートします (**true** または **false**)。</span><span class="sxs-lookup"><span data-stu-id="52eae-176">**Boolean** – This type supports a binary value (**true** or **false**).</span></span>
- <span data-ttu-id="52eae-177">**参照** – このタイプは、他の属性を参照します。</span><span class="sxs-lookup"><span data-stu-id="52eae-177">**Reference** – This type references other attributes.</span></span>

### <a name="set-up-attribute-types-in-finance-and-operations"></a><span data-ttu-id="52eae-178">Finance and Operations で属性タイプを設定</span><span class="sxs-lookup"><span data-stu-id="52eae-178">Set up attribute types in Finance and Operations</span></span>

1. <span data-ttu-id="52eae-179">小売販売促進マネージャーとして、Finance and Operations のバック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-179">Sign in to the Finance and Operations back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-180">**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性タイプ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-180">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute types**.</span></span>
3. <span data-ttu-id="52eae-181">**テキスト**タイプの 2 つの属性タイプを作成し、**固定リスト**オプションを**はい**に設定し、値の一覧を追加します。</span><span class="sxs-lookup"><span data-stu-id="52eae-181">Create two attribute types of the **Text** type, set the **Fixed list** option to **Yes**, and then add a list of values:</span></span>

    - <span data-ttu-id="52eae-182">1 つの属性タイプを**レンズ図形**と名付け、**楕円** と **四角**、そして **長方形** の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="52eae-182">Name one attribute type **Lens shape**, and add the following values: **Oval**, **Square**, and **Rectangle**.</span></span>
    - <span data-ttu-id="52eae-183">その他の属性の型の名前を**サングラス ブランド**とし、**Ray ban** と **Aviator**、そして **Oakley** の値を追加します。</span><span class="sxs-lookup"><span data-stu-id="52eae-183">Name the other attribute type **Sunglass brand**, and add the following values: **Ray ban**, **Aviator**, and **Oakley**.</span></span>

![属性タイプ](media/AttributeType.png)

### <a name="set-up-an-attribute-in-finance-and-operations"></a><span data-ttu-id="52eae-185">Finance and Operations で属性を設定</span><span class="sxs-lookup"><span data-stu-id="52eae-185">Set up an attribute in Finance and Operations</span></span>

1. <span data-ttu-id="52eae-186">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-186">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-187">**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-187">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attributes**.</span></span>
3. <span data-ttu-id="52eae-188">**レンズ**と名付けられた属性を作成します。</span><span class="sxs-lookup"><span data-stu-id="52eae-188">Create an attribute that is named **Lens**.</span></span>
4. <span data-ttu-id="52eae-189">**属性タイプ**フィールドを**レンズ図形**に設定します。</span><span class="sxs-lookup"><span data-stu-id="52eae-189">Set the **Attribute type** field to **Lens shape**.</span></span>

![属性](media/Attribute.png)

## <a name="attribute-metadata"></a><span data-ttu-id="52eae-191">属性メタデータ</span><span class="sxs-lookup"><span data-stu-id="52eae-191">Attribute metadata</span></span>

<span data-ttu-id="52eae-192">*属性のメタデータ* では、各製品の属性がどのように動作するかを指定するオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-192">*Attribute metadata* lets you select options to specify how the attributes for each product should behave.</span></span> <span data-ttu-id="52eae-193">たとえば、属性が必要か、検索で属性を使用できるか、フィルターとして属性を使用できるか特定することができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-193">For example, you can specify whether attributes are required, whether they can be used for searches, and whether they can be used as a filter.</span></span>

<span data-ttu-id="52eae-194">小売製品では、属性メタデータの設定はチャネル レベルで上書きできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-194">For retail products, the attribute metadata settings can be overridden at the channel level.</span></span> <span data-ttu-id="52eae-195">この機能は、このトピックの後半で説明されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-195">This capability will be discussed later in this topic.</span></span>

<span data-ttu-id="52eae-196">ご存知のように、**属性**ページには、属性メタデータに関連するオプションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52eae-196">As you might notice, the **Attributes** page includes options that are related to attribute metadata.</span></span> <span data-ttu-id="52eae-197">**POS の属性メタデータ**のもと、**絞り込み可能**と名付けられたオプションは、システムがこれらの属性値を処理する方法または販売時点管理 (POS) での属性値の動作に影響します。</span><span class="sxs-lookup"><span data-stu-id="52eae-197">Under **Attribute metadata for POS**, one option that is named **Can be refined** affects the behavior of the attribute values in the retail point of sale (POS) or the way that the system handles those attribute values.</span></span> <span data-ttu-id="52eae-198">**絞り込み可能**オプションから**はい**に設定できる属性のみ、Retail POS での製品の洗練またはフィルター処理のために表示されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-198">Only attributes for which you may set the **Can be refined** option to **Yes**, will show up for refinement or filtering of products in the retail POS.</span></span>

<span data-ttu-id="52eae-199">ここでは、**属性**ページで、残りの属性メタデータ オプションをお見せします。</span><span class="sxs-lookup"><span data-stu-id="52eae-199">Here are the remaining attribute metadata options on the **Attributes** page:</span></span>

- <span data-ttu-id="52eae-200">検索可能</span><span class="sxs-lookup"><span data-stu-id="52eae-200">Searchable</span></span>
- <span data-ttu-id="52eae-201">取得可能</span><span class="sxs-lookup"><span data-stu-id="52eae-201">Retrievable</span></span>
- <span data-ttu-id="52eae-202">照会可能</span><span class="sxs-lookup"><span data-stu-id="52eae-202">Can be queried</span></span>
- <span data-ttu-id="52eae-203">並べ替え可能</span><span class="sxs-lookup"><span data-stu-id="52eae-203">Sortable</span></span>
- <span data-ttu-id="52eae-204">複数の値を許可</span><span class="sxs-lookup"><span data-stu-id="52eae-204">Allow multiple values</span></span>
- <span data-ttu-id="52eae-205">大文字と小文字および形式を無視</span><span class="sxs-lookup"><span data-stu-id="52eae-205">Ignore case and format</span></span>
- <span data-ttu-id="52eae-206">完全一致</span><span class="sxs-lookup"><span data-stu-id="52eae-206">Complete match</span></span>

<span data-ttu-id="52eae-207">これらのオプションは、もともとオンライン店舗の検索機能を向上させることを意図していました。</span><span class="sxs-lookup"><span data-stu-id="52eae-207">These options were originally intended to improve the search functionality for the online storefront.</span></span> <span data-ttu-id="52eae-208">Finance and Operations には、すぐに使えるオンライン店舗が含まれていませんが、電子商取引発行ソフトウェア開発キット (SDK) は含まれています。</span><span class="sxs-lookup"><span data-stu-id="52eae-208">Although Finance and Operations doesn't include the online storefront out of the box, it does include the eCommerce Publishing Software Development Kit (SDK).</span></span> <span data-ttu-id="52eae-209">顧客は、この SDK を使用して任意の検索インデックスに製品を配置することが可能です。</span><span class="sxs-lookup"><span data-stu-id="52eae-209">Customers can use this SDK to put products into a search index of their choice.</span></span> <span data-ttu-id="52eae-210">製品データはインポートされますが、顧客は引き続き検索可能なデータ、クエリ可能なデータなどを区別することができるはずです。</span><span class="sxs-lookup"><span data-stu-id="52eae-210">Although the product data is imported, customers should still be able to distinguish searchable data, data that can be queried, and so on.</span></span> <span data-ttu-id="52eae-211">この方法により、最適なインデックスを作成して、*これらの意見で* がインデックスされる属性のみをインデックス化できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-211">In that way, they can build an optimal index to make sure that they index only attributes that, *in their opinion*, should be indexed.</span></span>

<span data-ttu-id="52eae-212">これらの残りのオプションの目的については、[SharePoint Server 2013 の検索スキーマの概要](https://technet.microsoft.com/library/jj219669.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52eae-212">For information about the purpose of these remaining options, see [Overview of the search schema in SharePoint Server 2013](https://technet.microsoft.com/library/jj219669.aspx).</span></span>

## <a name="filter-settings-for-attributes"></a><span data-ttu-id="52eae-213">属性のためのフィルター設定</span><span class="sxs-lookup"><span data-stu-id="52eae-213">Filter settings for attributes</span></span>

<span data-ttu-id="52eae-214">属性のフィルター設定を使用して、属性のフィルターを小売 POS に表示する方法を定義できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-214">Filter settings for attributes let you define how the filters for attributes are shown in the retail POS.</span></span> <span data-ttu-id="52eae-215">属性のフィルター設定へアクセスするには、Finance and Operations の**属性**ページで、属性を選択し、アクション ペインで**フィルター設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-215">To access the filter settings for an attribute, on the **Attributes** page in Finance and Operations, select the attribute, and then, on the Action Pane, select **Filter settings**.</span></span>

<span data-ttu-id="52eae-216">**フィルターの表示設定**ページでは、次のフィールドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52eae-216">The **Filter display preferences** page includes the following fields:</span></span>

- <span data-ttu-id="52eae-217">**名前** – 既定では、このフィールドは属性の名前を設定します。</span><span class="sxs-lookup"><span data-stu-id="52eae-217">**Name** – By default, this field is set to the name of the attribute.</span></span> <span data-ttu-id="52eae-218">ただし、その値は変更できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-218">However, you can change the value.</span></span>
- <span data-ttu-id="52eae-219">**オプションを表示** – 次のオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-219">**Display option** – The following options are available:</span></span>

    - <span data-ttu-id="52eae-220">**単一の値** – このオプションでは、次の属性タイプを選択できます。**ブール値**、**通貨**、**10 進数**、**整数**、そして**テキスト**。</span><span class="sxs-lookup"><span data-stu-id="52eae-220">**Single value** – This option is available for the following attribute types: **Boolean**, **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="52eae-221">このオプションは、調整のクライアントで、これらの属性の単一の値の選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="52eae-221">This option enables single value selection for these attributes in the client for refinement.</span></span>
    - <span data-ttu-id="52eae-222">**複数の値** – このオプションでは、次の属性タイプを選択できます。**通貨**、**10 進数**、**整数**、**テキスト**。</span><span class="sxs-lookup"><span data-stu-id="52eae-222">**Multi value** – This option is available for the following attribute types: **Currency**, **Decimal**, **Integer**, and **Text**.</span></span> <span data-ttu-id="52eae-223">このオプションは、調整のクライアントで、この属性の多値の選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="52eae-223">This option enables multi-value selection for this attribute in the client for refinement.</span></span>

- <span data-ttu-id="52eae-224">**表示制御** – 次のオプションを選択できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-224">**Display control** – The following options are available:</span></span>

    - <span data-ttu-id="52eae-225">**リスト** – このオプションは、全ての属性タイプで使用できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-225">**List** – This option is available for the all attribute types.</span></span>
    - <span data-ttu-id="52eae-226">**範囲** – このオプションでは、次の属性タイプを選択できます。**通貨**、**10 進数**、そして**整数**。</span><span class="sxs-lookup"><span data-stu-id="52eae-226">**Range** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>
    - <span data-ttu-id="52eae-227">**スライダー** – このオプションでは、次の属性タイプを選択できます。**通貨**、**10 進数**、そして**整数**。</span><span class="sxs-lookup"><span data-stu-id="52eae-227">**Slider** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>
    - <span data-ttu-id="52eae-228">**バー付きスライダー** – このオプションでは、次の属性タイプを選択できます。**通貨**、**10 進数**、そして**整数**。</span><span class="sxs-lookup"><span data-stu-id="52eae-228">**Slider with bars** – This option is available for the following attribute types: **Currency**, **Decimal**, and **Integer**.</span></span>

- <span data-ttu-id="52eae-229">**しきい値** – 表示制御タイプで**範囲**を選択した場合、この設定が必要です。</span><span class="sxs-lookup"><span data-stu-id="52eae-229">**Threshold value** – This setting is required if you selected **Range** as the display control type.</span></span> <span data-ttu-id="52eae-230">セミコロン (;) を区切り記号として使用し、値を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-230">You can define values by using a semicolon (;) as a delimiter.</span></span>

    <span data-ttu-id="52eae-231">例えば**バッグ数量**のようなフィルターに、しきい値を **10、20、50、100、200、500、1000、5000** とすることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-231">For example, for the filter like **Bag Volume**, a threshold value can be **10; 20; 50; 100; 200; 500; 1000; 5000**.</span></span> <span data-ttu-id="52eae-232">この場合、その小売 POS では次の範囲が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-232">In this case, the retail POS will show the following ranges.</span></span> <span data-ttu-id="52eae-233">結果セット内に商品を持たない範囲はすべてグレー表示になります。</span><span class="sxs-lookup"><span data-stu-id="52eae-233">Any ranges that don't have any products in the result set will appear dimmed.</span></span>

    - <span data-ttu-id="52eae-234">10 未満</span><span class="sxs-lookup"><span data-stu-id="52eae-234">Less than 10</span></span>
    - <span data-ttu-id="52eae-235">10 – 20</span><span class="sxs-lookup"><span data-stu-id="52eae-235">10 – 20</span></span>
    - <span data-ttu-id="52eae-236">20 – 50</span><span class="sxs-lookup"><span data-stu-id="52eae-236">20 – 50</span></span>
    - <span data-ttu-id="52eae-237">50 – 100</span><span class="sxs-lookup"><span data-stu-id="52eae-237">50 – 100</span></span>
    - <span data-ttu-id="52eae-238">100 – 200</span><span class="sxs-lookup"><span data-stu-id="52eae-238">100 – 200</span></span>
    - <span data-ttu-id="52eae-239">200 – 500</span><span class="sxs-lookup"><span data-stu-id="52eae-239">200 – 500</span></span>
    - <span data-ttu-id="52eae-240">500 回以上</span><span class="sxs-lookup"><span data-stu-id="52eae-240">500 or more</span></span>

![属性のフィルター設定](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a><span data-ttu-id="52eae-242">属性グループ</span><span class="sxs-lookup"><span data-stu-id="52eae-242">Attribute groups</span></span>

<span data-ttu-id="52eae-243">属性を定義した後は、属性グループに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-243">After attributes have been defined, they can be assigned to attribute groups.</span></span> <span data-ttu-id="52eae-244">*属性グループ* は、製品コンフィギュレーション モデルのコンポーネントまたはサブコンポーネントの個々の属性をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-244">An *attribute group* is used to group the individual attributes for a component or subcomponent in a product configuration model.</span></span> <span data-ttu-id="52eae-245">属性は、複数の属性グループに含めることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-245">An attribute can be included in more than one attribute group.</span></span> <span data-ttu-id="52eae-246">属性グループは、各種の選択が特定のコンテキストで並べられるため、ユーザーが製品を構成する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="52eae-246">Attribute groups can help users configure products, because the various selections are arranged in a specific context.</span></span> <span data-ttu-id="52eae-247">属性グループを小売カテゴリまたは小売チャンネルに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-247">Attribute groups can be assigned to retail categories or retail channels.</span></span>

<span data-ttu-id="52eae-248">属性グループに含まれている属性の既定値を設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-248">You can also set default values for attributes that are included in an attribute group.</span></span> <span data-ttu-id="52eae-249">例えば、属性グループに色の属性を追加し、既定の属性値として**青色**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-249">For example, you add an attribute for color to an attribute group and select **Blue** as the default attribute value.</span></span> <span data-ttu-id="52eae-250">この場合、その属性グループの 1 つを含む小売製品に属性グループが追加されると、各製品の既定の色として**青色**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-250">In this case, when the attribute group is added to a retail product that includes color as one of its attributes, **Blue** appears as the default color for that product.</span></span>

![属性グループ](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a><span data-ttu-id="52eae-252">属性グループの作成</span><span class="sxs-lookup"><span data-stu-id="52eae-252">Create an attribute group</span></span>

1. <span data-ttu-id="52eae-253">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-253">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-254">**製品情報管理** &gt; **設定** &gt; **カテゴリと属性** &gt; **属性グループ**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-254">Go to **Product information management** &gt; **Setup** &gt; **Categories and attributes** &gt; **Attribute groups**.</span></span>
3. <span data-ttu-id="52eae-255">**ファッション サングラス**という名の属性グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="52eae-255">Create an attribute group that is named **Fashion Sunglasses**.</span></span>
4. <span data-ttu-id="52eae-256">次の属性を追加します。**レンズ図形**と**サングラス ブランド**。</span><span class="sxs-lookup"><span data-stu-id="52eae-256">Add the following attributes: **Lens shape** and **Sunglass brand**.</span></span>

### <a name="assign-attribute-groups-to-retail-categories"></a><span data-ttu-id="52eae-257">小売カテゴリへ属性グループを割り当て</span><span class="sxs-lookup"><span data-stu-id="52eae-257">Assign attribute groups to retail categories</span></span>

<span data-ttu-id="52eae-258">1 つまたは複数の属性グループは、次のタイプの小売カテゴリ階層内のカテゴリ ノードを関連付けることができます。小売カテゴリ階層、チャネル ナビゲーション カテゴリ階層、および補助製品カテゴリ階層。</span><span class="sxs-lookup"><span data-stu-id="52eae-258">One or more attribute groups can be associated with category nodes in the following types of retail category hierarchies: Retail product hierarchy, Channel navigation category hierarchy, and Supplemental product category hierarchy.</span></span> <span data-ttu-id="52eae-259">そして、製品を分類されると、属性グループに含まれる属性を継承します。</span><span class="sxs-lookup"><span data-stu-id="52eae-259">Then, when products are categorized, they inherit the attributes that are included in the attribute groups.</span></span>

![小売製品階層 – 製品属性グループ](media/AGRetailProdHierarchy.PNG)

<span data-ttu-id="52eae-261">この手順では、属性グループを小売製品階層内のカテゴリに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="52eae-261">Follow these steps to assign attribute groups to categories in the Retail product hierarchy.</span></span>

1. <span data-ttu-id="52eae-262">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-262">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-263">**小売** &gt; **カテゴリおよび製品の管理** &gt; **小売製品階層**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-263">Go to **Retail** &gt; **Category and product management** &gt; **Retail product hierarchy**.</span></span>
3. <span data-ttu-id="52eae-264">**ファッション ナビゲーション階層**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-264">Select **Fashion navigation hierarchy**.</span></span>
4. <span data-ttu-id="52eae-265">**紳士服**で、**パンツ**カテゴリを選び、**製品属性グループ**クイック タブ上で**男性用ベルト**という名の属性グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="52eae-265">Under **Menswear**, select the **Pants** category, and then, on the **Product attribute groups** FastTab, add an attribute group that is named **Men's belt**.</span></span>
5. <span data-ttu-id="52eae-266">**ファッション サングラス**カテゴリを選択し、**属性の表示**を選び**ファッション サングラス**属性グループで新しい属性を確認します。</span><span class="sxs-lookup"><span data-stu-id="52eae-266">Select the **Fashion sunglasses** category, and verify the new attributes in the **Fashion Sunglasses** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="52eae-267">属性グループに新しい**レンズ図形**と**サングラス ブランド**属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-267">The attribute group should show the new **Lens shape** and **Sunglass brand** attributes.</span></span>

6. <span data-ttu-id="52eae-268">**紳士服**で、**パンツ**カテゴリを選択し、**属性の表示**を選び**男性用ベルト**の属性グループを確認します。</span><span class="sxs-lookup"><span data-stu-id="52eae-268">Under **Menswear**, select the **Pants** category, and verify the attributes for the **Men's belt** attribute group by selecting **View attributes**.</span></span>

    <span data-ttu-id="52eae-269">属性グループに、**男性用ベルト ブランド**と**ベルト ファブリック**、**ベルト サイズ**の属性が表示されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-269">The attribute group should show the **Men's belt brand**, **Belt fabric**, and **Belt size** attributes.</span></span>

> [!NOTE]
> <span data-ttu-id="52eae-270">この手順を使用して、チャンネル ナビゲーション カテゴリ階層と補助製品カテゴリ階層内のカテゴリに属性グループを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-270">This procedure can also be used to assign attribute groups to categories in the Channel navigation category hierarchy and the Supplemental product category hierarchy.</span></span> <span data-ttu-id="52eae-271">手順 2 では、次のナビゲーション パスを使用します。</span><span class="sxs-lookup"><span data-stu-id="52eae-271">In step 2, use the following navigation paths:</span></span>
>
> - <span data-ttu-id="52eae-272">**小売** &gt; **カテゴリおよび製品の管理** &gt; **チャネル ナビゲーション カテゴリ**</span><span class="sxs-lookup"><span data-stu-id="52eae-272">**Retail** &gt; **Category and product management** &gt; **Channel navigation categories**</span></span>
> - <span data-ttu-id="52eae-273">**小売** &gt; **カテゴリおよび製品の管理** &gt; **補助製品カテゴリ**</span><span class="sxs-lookup"><span data-stu-id="52eae-273">**Retail** &gt; **Category and product management** &gt; **Supplemental product categories**</span></span>

### <a name="assign-attribute-groups-to-retail-stores"></a><span data-ttu-id="52eae-274">小売店舗へ属性グループを割り当て</span><span class="sxs-lookup"><span data-stu-id="52eae-274">Assign attribute groups to retail stores</span></span>

<span data-ttu-id="52eae-275">1 つ以上の属性グループを小売店舗階層の 1 つ以上の小売店舗に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-275">One or more attribute groups can be associated with one or more retail stores in the retail store hierarchy.</span></span> <span data-ttu-id="52eae-276">そして、製品が特定の小売店舗に対して強化されると、属性グループに含まれる属性を継承します。</span><span class="sxs-lookup"><span data-stu-id="52eae-276">Then, when products are enriched for specific retail stores, they inherit the attributes that are included in the attribute groups.</span></span>

1. <span data-ttu-id="52eae-277">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-277">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-278">**小売** &gt; **チャネル設定** &gt; **チャネル カテゴリと製品属性**に移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-278">Go to **Retail** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="52eae-279">ヒューストン チャネルに属性グループを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="52eae-279">Assign attribute groups to the Houston channel:</span></span>

    1. <span data-ttu-id="52eae-280">**ヒューストン**チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-280">Select the **Houston** channel.</span></span>
    2. <span data-ttu-id="52eae-281">**属性グループ**クイック タブで、**追加**を選び、**名前**フィールドで **SharePointProvisionedProductAttributeGroup** を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-281">On the **Attribute group** FastTab, select **Add**, and then, in the **Name** field, select **SharePointProvisionedProductAttributeGroup**.</span></span>
    3. <span data-ttu-id="52eae-282">もう一度**追加**を選び、**名前**フィールドで**男性用ベルト**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-282">Select **Add** again, and then, in the **Name** field, select **Men's belt**.</span></span>
    4. <span data-ttu-id="52eae-283">もう一度**追加**を選び、**名前**フィールドで**ファッション サングラス**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-283">Select **Add** again, and then, in the **Name** field, select **Fashion Sunglasses**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="52eae-284">オプションを使用すると、このチャネルが階層内で、親チャネルから属性グループを継承するよう指定できます。</span><span class="sxs-lookup"><span data-stu-id="52eae-284">An option lets you specify that this channel should inherit the attribute groups from its parent channel in the hierarchy.</span></span> <span data-ttu-id="52eae-285">**継承**オプションを**はい**に設定すると、子チャネル ノードは、すべての属性グループとそれらの属性グループ内のすべての属性を継承します。</span><span class="sxs-lookup"><span data-stu-id="52eae-285">If you set the **Inherit** option to **Yes**, the child channel node inherits all the attribute groups and all the attributes in those attribute groups.</span></span>

4. <span data-ttu-id="52eae-286">これらはヒューストン チャネルで使用できるように属性を有効にします。</span><span class="sxs-lookup"><span data-stu-id="52eae-286">Enable the attributes so that they are available in the Houston channel:</span></span>

    1. <span data-ttu-id="52eae-287">アクション ペインで、**属性メタデータの設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-287">On the Action Pane, select **Set attribute metadata**.</span></span>
    2. <span data-ttu-id="52eae-288">**ファッション**カテゴリ ノードを選び、**チャネル製品属性**クイック タブ で各属性の**属性を含む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-288">Select the **Fashion** category node, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    3. <span data-ttu-id="52eae-289">**ファッション アクセサリー**カテゴリ ノードを選び、**ファッション サングラス**カテゴリを選択し、**チャンネル製品属性**クイック タブで各属性の**属性を含む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-289">Select the **Fashion Accessories** category node, select the **Fashion Sunglasses** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>
    4. <span data-ttu-id="52eae-290">**紳士服**カテゴリ ノードを選び、**パンツ**カテゴリを選択し、**チャネル製品属性**クイック タブで各属性の**属性を含む**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-290">Select the **Menswear** category node, select the **Pants** category, and then, on the **Channel product attributes** FastTab, select **Include attribute** for each attribute.</span></span>

![チャネル カテゴリと製品属性 – 属性グループ](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a><span data-ttu-id="52eae-292">属性値の上書き</span><span class="sxs-lookup"><span data-stu-id="52eae-292">Overriding attribute values</span></span>

<span data-ttu-id="52eae-293">属性の既定値は、製品レベルで各製品に対して上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="52eae-293">The default values of attributes can be overridden for individual products at the product level.</span></span> <span data-ttu-id="52eae-294">特定の小売チャネルを対象とする特定のカタログの個々の製品について、既定値を上書きすることもできます。</span><span class="sxs-lookup"><span data-stu-id="52eae-294">Default values can also be overridden for individual products in specific catalogs that are targeted at specific retail channels.</span></span>

### <a name="override-the-attribute-values-of-an-individual-product"></a><span data-ttu-id="52eae-295">個々の製品の属性値を上書き</span><span class="sxs-lookup"><span data-stu-id="52eae-295">Override the attribute values of an individual product</span></span>

1. <span data-ttu-id="52eae-296">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-296">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-297">**小売** &gt; **カテゴリおよび製品の管理** &gt; **カテゴリ別リリース済製品**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-297">Go to **Retail** &gt; **Category and product management** &gt; **Released products by category**.</span></span>
3. <span data-ttu-id="52eae-298">**ファッション** &gt; **ファッション アクセサリ** &gt; **ファッション サングラス**カテゴリ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-298">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
4. <span data-ttu-id="52eae-299">グリッドで必要な製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-299">Select the required product in the grid.</span></span> <span data-ttu-id="52eae-300">そして、アクション ペイン、**製品**タブの、**設定**グループで、**製品属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-300">Then, on the Action Pane, on the **Product** tab, in the **Set up** group, select **Product attributes**.</span></span>
5. <span data-ttu-id="52eae-301">左側のペインで属性を選択し、右側のペインでその値を更新します。</span><span class="sxs-lookup"><span data-stu-id="52eae-301">Select an attribute in the left pane, and then update its value in the right pane.</span></span>

![製品詳細ページ – 製品属性グループ](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a><span data-ttu-id="52eae-303">カタログ内の製品属性値を上書き</span><span class="sxs-lookup"><span data-stu-id="52eae-303">Override the attribute values of products in a catalog</span></span>

1. <span data-ttu-id="52eae-304">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-304">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-305">**小売** &gt; **カタログ管理** &gt; **すべてのカタログ**へ移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-305">Go to **Retail** &gt; **Catalog management** &gt; **All catalogs**.</span></span>
3. <span data-ttu-id="52eae-306">**Fabrikam 基本カタログ**カタログを選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-306">Select the **Fabrikam Base Catalog** catalog.</span></span>
4. <span data-ttu-id="52eae-307">**ファッション** &gt; **ファッション アクセサリ** &gt; **ファッション サングラス**カテゴリ ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-307">Select the **Fashion** &gt; **Fashion Accessories** &gt; **Fashion Sunglasses** category node.</span></span>
5. <span data-ttu-id="52eae-308">**製品**クイック タブで、必要な製品を選び、製品グリッドの上部で**属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-308">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>
6. <span data-ttu-id="52eae-309">次のクイック タブで、必要な属性の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="52eae-309">On the following FastTabs, update the values of the required attributes:</span></span>

    - <span data-ttu-id="52eae-310">共有製品メディア</span><span class="sxs-lookup"><span data-stu-id="52eae-310">Shared product media</span></span>
    - <span data-ttu-id="52eae-311">共有の製品属性</span><span class="sxs-lookup"><span data-stu-id="52eae-311">Shared product attributes</span></span>
    - <span data-ttu-id="52eae-312">チャネル メディア</span><span class="sxs-lookup"><span data-stu-id="52eae-312">Channel media</span></span>
    - <span data-ttu-id="52eae-313">チャネル製品属性</span><span class="sxs-lookup"><span data-stu-id="52eae-313">Channel product attributes</span></span>

    > [!NOTE]
    > <span data-ttu-id="52eae-314">共有製品メディアと共有製品属性が Finance and Operations で作成される場合、それらはすべての小売製品に適用されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-314">If shared product media and shared product attributes are created in Finance and Operations, they apply to all the retail products.</span></span>

![カタログ製品属性グループ](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a><span data-ttu-id="52eae-316">チャネル内の製品属性値を上書き</span><span class="sxs-lookup"><span data-stu-id="52eae-316">Override the attribute values of products in a channel</span></span>

1. <span data-ttu-id="52eae-317">小売販売促進マネージャーとして、バック オフィス クライアントにログインします。</span><span class="sxs-lookup"><span data-stu-id="52eae-317">Sign in to the back-office client as a retail merchandising manager.</span></span>
2. <span data-ttu-id="52eae-318">**小売** &gt; **チャネル設定** &gt; **チャネル カテゴリと製品属性**に移動します。</span><span class="sxs-lookup"><span data-stu-id="52eae-318">Go to **Retail** &gt; **Channel setup** &gt; **Channel categories and product attributes**.</span></span>
3. <span data-ttu-id="52eae-319">**ヒューストン**チャネルを選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-319">Select the **Houston** channel.</span></span>
4. <span data-ttu-id="52eae-320">**製品**クイック タブで、必要な製品を選び、製品グリッドの上部で**属性**を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-320">On the **Products** FastTab, select the required product, and then select **Attributes** above the product grid.</span></span>

    > [!NOTE]
    > <span data-ttu-id="52eae-321">製品がない場合は、**製品**クイック タブで**追加**を選択して製品を追加し、**製品を追加**ダイアログ ボックスで必要な製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="52eae-321">If no products are available, add products by selecting **Add** on the **Products** FastTab and then selecting the required products in the **Add products** dialog box.</span></span>

5. <span data-ttu-id="52eae-322">次のクイック タブで、必要な属性の値を更新します。</span><span class="sxs-lookup"><span data-stu-id="52eae-322">On the following FastTabs, update the values of the required attributes:</span></span>

    - <span data-ttu-id="52eae-323">共有製品メディア</span><span class="sxs-lookup"><span data-stu-id="52eae-323">Shared product media</span></span>
    - <span data-ttu-id="52eae-324">共有の製品属性</span><span class="sxs-lookup"><span data-stu-id="52eae-324">Shared product attributes</span></span>
    - <span data-ttu-id="52eae-325">チャネル メディア</span><span class="sxs-lookup"><span data-stu-id="52eae-325">Channel media</span></span>
    - <span data-ttu-id="52eae-326">チャネル製品属性</span><span class="sxs-lookup"><span data-stu-id="52eae-326">Channel product attributes</span></span>

    > [!NOTE]
    > <span data-ttu-id="52eae-327">共有製品メディアと共有製品属性が Finance and Operations で作成される場合、それらはすべての小売製品に適用されます。</span><span class="sxs-lookup"><span data-stu-id="52eae-327">If shared product media and shared product attributes are created in Finance and Operations, they apply to all the retail products.</span></span>
