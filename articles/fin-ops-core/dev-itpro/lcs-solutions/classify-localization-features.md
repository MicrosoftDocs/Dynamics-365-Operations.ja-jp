---
title: ローカライズ機能の分類
description: ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制、または競合のいずれかに分類される必要があります。 この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 27601
ms.assetid: 7e2031b4-a092-482e-a76d-1e582edecd86
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b883d9246f35539e3bae14b0a9171e49c7534c73
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183280"
---
# <a name="classification-of-localization-features"></a><span data-ttu-id="40b08-104">ローカライズ機能の分類</span><span class="sxs-lookup"><span data-stu-id="40b08-104">Classification of localization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="40b08-105">ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制、または競合のいずれかに分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b08-105">As part of the requirements for LCS solutions for localization &amp; translation, localization features must be classified as either regulatory or competitive in the business process modeler (BPM) library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="40b08-106">この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="40b08-106">This article explains the difference between these two types of feature and shows how the feature type is used in the title of the feature.</span></span>

<span data-ttu-id="40b08-107">ローカライズ機能は、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制または競合として分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b08-107">Localization features must be classified as either regulatory or competitive in the Business process modeler (BPM) library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="40b08-108">次の定義は、2 つのタイプの機能を区別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="40b08-108">The following definitions will help you distinguish the two types of features:</span></span>

-   <span data-ttu-id="40b08-109">**規制機能** – 特定の国/地域で業務を行う組織は、日々の業務トランザクションや工程に関して、国/地域固有の法律や規制を遵守する必要があり、その国/地域で実施される活動についての法的義務を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b08-109">**Regulatory features** – Organizations that do business in a particular country/region must comply with country/region-specific laws and regulations as they handle their daily business transactions and operations, and meet their legal obligations for activities that are conducted in that country/region.</span></span> <span data-ttu-id="40b08-110">これらの法律および規制は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="40b08-110">These laws and regulations are enforced, and non-adherence can lead to severe consequences for an organization that does business in that country/region.</span></span>
-   <span data-ttu-id="40b08-111">**競合機能** - このカテゴリには、前述の定義に従って規制機能とは見なされないその他のすべての機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="40b08-111">**Competitive features** – This category includes all other features that aren't considered regulatory features according to the preceding definition.</span></span>

<span data-ttu-id="40b08-112">BPM ライブラリが構築されているときは、ローカライズ ソリューションの機能のタイトルで、各機能のタイプを区別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="40b08-112">When the BPM library is constructed, the various feature types should be distinguished through the title of the localization solution feature.</span></span> <span data-ttu-id="40b08-113">このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および機能タイプを示す次の命名規則に準拠します。</span><span class="sxs-lookup"><span data-stu-id="40b08-113">The label for this title will conform to the following naming convention that indicates the country/region and feature type through prefixes, as shown in the following table.</span></span>

| <span data-ttu-id="40b08-114">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="40b08-114">Feature type</span></span> | <span data-ttu-id="40b08-115">書式設定</span><span class="sxs-lookup"><span data-stu-id="40b08-115">Format</span></span>                | <span data-ttu-id="40b08-116">例</span><span class="sxs-lookup"><span data-stu-id="40b08-116">Example</span></span>                             |
|--------------|-----------------------|-------------------------------------|
| <span data-ttu-id="40b08-117">規制</span><span class="sxs-lookup"><span data-stu-id="40b08-117">Regulatory</span></span>   | <span data-ttu-id="40b08-118">XX-REG-Feature タイトル</span><span class="sxs-lookup"><span data-stu-id="40b08-118">XX-REG-Feature title</span></span>  | <span data-ttu-id="40b08-119">PT-REG-直接売上税レポート</span><span class="sxs-lookup"><span data-stu-id="40b08-119">PT-REG-Direct sales Tax report</span></span>      |
| <span data-ttu-id="40b08-120">競合</span><span class="sxs-lookup"><span data-stu-id="40b08-120">Competitive</span></span>  | <span data-ttu-id="40b08-121">XX-COMP-Feature タイトル</span><span class="sxs-lookup"><span data-stu-id="40b08-121">XX-COMP-Feature title</span></span> | <span data-ttu-id="40b08-122">PT-COMP-国内銀行支払形式</span><span class="sxs-lookup"><span data-stu-id="40b08-122">PT-COMP-Country bank payment format</span></span> |

<span data-ttu-id="40b08-123">次のテーブルに、名前付け規則のコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="40b08-123">The following table explains the components of the naming convention.</span></span>

| <span data-ttu-id="40b08-124">コンポーネント名</span><span class="sxs-lookup"><span data-stu-id="40b08-124">Component name</span></span>      | <span data-ttu-id="40b08-125">書式設定</span><span class="sxs-lookup"><span data-stu-id="40b08-125">Format</span></span>      | <span data-ttu-id="40b08-126">説明</span><span class="sxs-lookup"><span data-stu-id="40b08-126">Description</span></span>                                                                                                                   | <span data-ttu-id="40b08-127">例</span><span class="sxs-lookup"><span data-stu-id="40b08-127">Example</span></span>                 |
|---------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="40b08-128">国/地域コード</span><span class="sxs-lookup"><span data-stu-id="40b08-128">Country/region code</span></span> | <span data-ttu-id="40b08-129">XX</span><span class="sxs-lookup"><span data-stu-id="40b08-129">XX</span></span>          | <span data-ttu-id="40b08-130">2 文字の ISO 国/地域コード ([ISO 3166 規格](https://www.iso.org/iso/country_names_and_code_elements))</span><span class="sxs-lookup"><span data-stu-id="40b08-130">The two-letter ISO country/region code (from the [ISO 3166 standard](https://www.iso.org/iso/country_names_and_code_elements))</span></span> | <span data-ttu-id="40b08-131">PT (= ポルトガル)</span><span class="sxs-lookup"><span data-stu-id="40b08-131">PT (= Portugal)</span></span>         |
| <span data-ttu-id="40b08-132">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="40b08-132">Feature type</span></span>        | <span data-ttu-id="40b08-133">REG または COMP</span><span class="sxs-lookup"><span data-stu-id="40b08-133">REG or COMP</span></span> | <span data-ttu-id="40b08-134">機能のタイプ</span><span class="sxs-lookup"><span data-stu-id="40b08-134">The type of feature</span></span>                                                                                                           | <span data-ttu-id="40b08-135">REG</span><span class="sxs-lookup"><span data-stu-id="40b08-135">REG</span></span>                     |
| <span data-ttu-id="40b08-136">フィーチャー名</span><span class="sxs-lookup"><span data-stu-id="40b08-136">Feature name</span></span>        | <span data-ttu-id="40b08-137">テキスト</span><span class="sxs-lookup"><span data-stu-id="40b08-137">Text</span></span>        | <span data-ttu-id="40b08-138">機能がどのように使用されているかを説明する短い機能タイトル</span><span class="sxs-lookup"><span data-stu-id="40b08-138">A short feature title that describes what the feature is used for</span></span>                                                             | <span data-ttu-id="40b08-139">直接売上税レポート</span><span class="sxs-lookup"><span data-stu-id="40b08-139">Direct sales tax report</span></span> |

<span data-ttu-id="40b08-140">BPM の詳細については、[BPM に業務プロセスをアップロード](../lifecycle-services/upload-business-processes-bpm-task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40b08-140">For more information about BPM, see [Upload business processes to BPM](../lifecycle-services/upload-business-processes-bpm-task-recorder.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40b08-141">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="40b08-141">Additional resources</span></span>

- [<span data-ttu-id="40b08-142">ローカライズと規制の機能</span><span class="sxs-lookup"><span data-stu-id="40b08-142">Localization and regulatory features</span></span>](country-region.md)

