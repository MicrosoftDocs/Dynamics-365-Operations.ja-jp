---
title: ローカリゼーション機能の分類
description: このトピックでは、規制機能と競合機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 27601
ms.assetid: 7e2031b4-a092-482e-a76d-1e582edecd86
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7904f11cbd4a2578c1d4789b8efcb441376f7dd5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749277"
---
# <a name="classification-of-localization-features"></a><span data-ttu-id="b1026-103">ローカライズ機能の分類</span><span class="sxs-lookup"><span data-stu-id="b1026-103">Classification of localization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1026-104">ローカライズおよび翻訳向け LCS ソリューションの要件の一部として、ローカライズ機能は Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制または競合として分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1026-104">As part of the requirements for LCS solutions for localization and translation, localization features must be classified as either regulatory or competitive in the business process modeler (BPM) library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b1026-105">この記事では、これらの 2 つのタイプの機能の違いについて説明し、その機能のタイトルにどのように機能タイプが使用されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="b1026-105">This article explains the difference between these two types of feature and shows how the feature type is used in the title of the feature.</span></span>

<span data-ttu-id="b1026-106">ローカライズ機能は、Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) ライブラリで規制または競合として分類される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1026-106">Localization features must be classified as either regulatory or competitive in the Business process modeler (BPM) library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="b1026-107">次の定義は、2 つのタイプの機能を区別するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b1026-107">The following definitions will help you distinguish the two types of features:</span></span>

-   <span data-ttu-id="b1026-108">**規制機能** – 特定の国/地域で業務を行う組織は、日々の業務トランザクションや工程に関して、国/地域固有の法律や規制を遵守する必要があり、その国/地域で実施される活動についての法的義務を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1026-108">**Regulatory features** – Organizations that do business in a particular country/region must comply with country/region-specific laws and regulations as they handle their daily business transactions and operations, and meet their legal obligations for activities that are conducted in that country/region.</span></span> <span data-ttu-id="b1026-109">これらの法律および規制は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b1026-109">These laws and regulations are enforced, and non-adherence can lead to severe consequences for an organization that does business in that country/region.</span></span>
-   <span data-ttu-id="b1026-110">**競合機能** - このカテゴリには、前述の定義に従って規制機能とは見なされないその他のすべての機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b1026-110">**Competitive features** – This category includes all other features that aren't considered regulatory features according to the preceding definition.</span></span>

<span data-ttu-id="b1026-111">BPM ライブラリが構築されているときは、ローカライズ ソリューションの機能のタイトルで、各機能のタイプを区別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1026-111">When the BPM library is constructed, the various feature types should be distinguished through the title of the localization solution feature.</span></span> <span data-ttu-id="b1026-112">このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および機能タイプを示す次の命名規則に準拠します。</span><span class="sxs-lookup"><span data-stu-id="b1026-112">The label for this title will conform to the following naming convention that indicates the country/region and feature type through prefixes, as shown in the following table.</span></span>

| <span data-ttu-id="b1026-113">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="b1026-113">Feature type</span></span> | <span data-ttu-id="b1026-114">書式設定</span><span class="sxs-lookup"><span data-stu-id="b1026-114">Format</span></span>                | <span data-ttu-id="b1026-115">例</span><span class="sxs-lookup"><span data-stu-id="b1026-115">Example</span></span>                             |
|--------------|-----------------------|-------------------------------------|
| <span data-ttu-id="b1026-116">規制</span><span class="sxs-lookup"><span data-stu-id="b1026-116">Regulatory</span></span>   | <span data-ttu-id="b1026-117">XX-REG-Feature タイトル</span><span class="sxs-lookup"><span data-stu-id="b1026-117">XX-REG-Feature title</span></span>  | <span data-ttu-id="b1026-118">PT-REG-直接売上税レポート</span><span class="sxs-lookup"><span data-stu-id="b1026-118">PT-REG-Direct sales Tax report</span></span>      |
| <span data-ttu-id="b1026-119">競合</span><span class="sxs-lookup"><span data-stu-id="b1026-119">Competitive</span></span>  | <span data-ttu-id="b1026-120">XX-COMP-Feature タイトル</span><span class="sxs-lookup"><span data-stu-id="b1026-120">XX-COMP-Feature title</span></span> | <span data-ttu-id="b1026-121">PT-COMP-国内銀行支払形式</span><span class="sxs-lookup"><span data-stu-id="b1026-121">PT-COMP-Country bank payment format</span></span> |

<span data-ttu-id="b1026-122">次のテーブルに、名前付け規則のコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="b1026-122">The following table explains the components of the naming convention.</span></span>

| <span data-ttu-id="b1026-123">コンポーネント名</span><span class="sxs-lookup"><span data-stu-id="b1026-123">Component name</span></span>      | <span data-ttu-id="b1026-124">書式設定</span><span class="sxs-lookup"><span data-stu-id="b1026-124">Format</span></span>      | <span data-ttu-id="b1026-125">説明</span><span class="sxs-lookup"><span data-stu-id="b1026-125">Description</span></span>                                                                                                                   | <span data-ttu-id="b1026-126">例</span><span class="sxs-lookup"><span data-stu-id="b1026-126">Example</span></span>                 |
|---------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span data-ttu-id="b1026-127">国/地域コード</span><span class="sxs-lookup"><span data-stu-id="b1026-127">Country/region code</span></span> | <span data-ttu-id="b1026-128">XX</span><span class="sxs-lookup"><span data-stu-id="b1026-128">XX</span></span>          | <span data-ttu-id="b1026-129">2 文字の ISO 国/地域コード ([ISO 3166 規格](https://www.iso.org/iso/country_names_and_code_elements))</span><span class="sxs-lookup"><span data-stu-id="b1026-129">The two-letter ISO country/region code (from the [ISO 3166 standard](https://www.iso.org/iso/country_names_and_code_elements))</span></span> | <span data-ttu-id="b1026-130">PT (= ポルトガル)</span><span class="sxs-lookup"><span data-stu-id="b1026-130">PT (= Portugal)</span></span>         |
| <span data-ttu-id="b1026-131">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="b1026-131">Feature type</span></span>        | <span data-ttu-id="b1026-132">REG または COMP</span><span class="sxs-lookup"><span data-stu-id="b1026-132">REG or COMP</span></span> | <span data-ttu-id="b1026-133">機能のタイプ</span><span class="sxs-lookup"><span data-stu-id="b1026-133">The type of feature</span></span>                                                                                                           | <span data-ttu-id="b1026-134">REG</span><span class="sxs-lookup"><span data-stu-id="b1026-134">REG</span></span>                     |
| <span data-ttu-id="b1026-135">フィーチャー名</span><span class="sxs-lookup"><span data-stu-id="b1026-135">Feature name</span></span>        | <span data-ttu-id="b1026-136">テキスト</span><span class="sxs-lookup"><span data-stu-id="b1026-136">Text</span></span>        | <span data-ttu-id="b1026-137">機能がどのように使用されているかを説明する短い機能タイトル</span><span class="sxs-lookup"><span data-stu-id="b1026-137">A short feature title that describes what the feature is used for</span></span>                                                             | <span data-ttu-id="b1026-138">直接売上税レポート</span><span class="sxs-lookup"><span data-stu-id="b1026-138">Direct sales tax report</span></span> |

<span data-ttu-id="b1026-139">BPMの詳細については、 [ユーザー定義の業務プロセスをビジネス プロセス モデラー (BPM) にアップロードする](../lifecycle-services/upload-business-processes-bpm-task-recorder.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b1026-139">For more information about BPM, see [Upload custom business processes to Business process modeler (BPM)](../lifecycle-services/upload-business-processes-bpm-task-recorder.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1026-140">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b1026-140">Additional resources</span></span>

- [<span data-ttu-id="b1026-141">グローバリゼーション リソース</span><span class="sxs-lookup"><span data-stu-id="b1026-141">Globalization resources</span></span>](country-region.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]