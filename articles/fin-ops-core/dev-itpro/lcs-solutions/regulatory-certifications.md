---
title: 機能タイトルの規制証明情報
description: このトピックでは、機能のタイトルで認証に関する情報を使用する方法について説明します。
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.custom: 27581
ms.assetid: d0b8286a-b2c1-4fa2-905a-3383b1d34d56
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 004b2ef6aabc3cf116ec31c9980aa4efe483a69e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752270"
---
# <a name="regulatory-certification-information-in-feature-titles"></a><span data-ttu-id="4c5ac-103">機能タイトルの規制認証情報</span><span class="sxs-lookup"><span data-stu-id="4c5ac-103">Regulatory certification information in feature titles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c5ac-104">ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは意図したマーケットでの販売を、法律に準拠したものにするために。ソリューションが必要とする規制認証に関する詳細を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-104">As part of the requirements for LCS solutions for localization &amp; translation, localization ISV solution providers must include details about any regulatory certifications that the solution requires in order to be legally compliant for sale in the intended market.</span></span> <span data-ttu-id="4c5ac-105">この記事では、機能のタイトルに認証に関する情報をどのように使用しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-105">This article shows how information about certifications is used in the title of the feature.</span></span>

<span data-ttu-id="4c5ac-106">規制証明には、データ プライバシーから特定の規制に準拠する認定まで。さまざまな形式があります。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-106">Regulatory certification can take various forms, from data privacy to certification of compliance with specific regulations.</span></span> <span data-ttu-id="4c5ac-107">ただし、すべての規制認証にある共通の 1 つの点は、実施するの国/地域の法令や規制によって要求されるということです。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-107">However, one thing that all regulatory certifications have in common is that they are required by the laws and regulations of the country/region of operation.</span></span> <span data-ttu-id="4c5ac-108">これらの認定は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-108">These certifications are enforced, and non-adherence can lead to severe consequences for an organization that does business in that country/region.</span></span> <span data-ttu-id="4c5ac-109">業務プロセス ライブラリが構築されたとき、規制認証は、ローカライズ ソリューション機能のタイトルによって、Microsoft Dynamics Lifecycle Services (LCS) の業務プロセス モデラー (BPM) ライブラリの規制に関する要件として識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-109">When the business process library is constructed, regulatory certifications must be identified as regulatory requirements in the Microsoft Dynamics Lifecycle Services (LCS) Business process modeler (BPM) library through the title of the localization solution feature.</span></span> <span data-ttu-id="4c5ac-110">このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および認証タイプを示す次の命名規則に準拠します。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-110">The label for this title will conform to the following naming convention that indicates the country/region and certification type through prefixes, as shown in the following table.</span></span>

| <span data-ttu-id="4c5ac-111">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="4c5ac-111">Feature type</span></span> | <span data-ttu-id="4c5ac-112">書式設定</span><span class="sxs-lookup"><span data-stu-id="4c5ac-112">Format</span></span>                      | <span data-ttu-id="4c5ac-113">例</span><span class="sxs-lookup"><span data-stu-id="4c5ac-113">Example</span></span>                                  |
|--------------|-----------------------------|------------------------------------------|
| <span data-ttu-id="4c5ac-114">規制</span><span class="sxs-lookup"><span data-stu-id="4c5ac-114">Regulatory</span></span>   | <span data-ttu-id="4c5ac-115">xx 用 XX-REG-Certification</span><span class="sxs-lookup"><span data-stu-id="4c5ac-115">XX-REG-Certification for xx</span></span> | <span data-ttu-id="4c5ac-116">PT-REG-会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="4c5ac-116">PT-REG-Certification for Fiscal printers</span></span> |

<span data-ttu-id="4c5ac-117">次のテーブルに、名前付け規則のコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-117">The following table explains the components of the naming convention.</span></span>

| <span data-ttu-id="4c5ac-118">コンポーネント名</span><span class="sxs-lookup"><span data-stu-id="4c5ac-118">Component name</span></span>      |  <span data-ttu-id="4c5ac-119">書式設定</span><span class="sxs-lookup"><span data-stu-id="4c5ac-119">Format</span></span> | <span data-ttu-id="4c5ac-120">説明</span><span class="sxs-lookup"><span data-stu-id="4c5ac-120">Description</span></span>                                                                                                                   | <span data-ttu-id="4c5ac-121">例</span><span class="sxs-lookup"><span data-stu-id="4c5ac-121">Example</span></span>                           |
|---------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="4c5ac-122">国/地域コード</span><span class="sxs-lookup"><span data-stu-id="4c5ac-122">Country/region code</span></span> | <span data-ttu-id="4c5ac-123">XX</span><span class="sxs-lookup"><span data-stu-id="4c5ac-123">XX</span></span>      | <span data-ttu-id="4c5ac-124">2 文字の ISO 国/地域コード ([ISO 3166 規格](https://www.iso.org/iso/country_names_and_code_elements))</span><span class="sxs-lookup"><span data-stu-id="4c5ac-124">The two-letter ISO country/region code (from the [ISO 3166 standard](https://www.iso.org/iso/country_names_and_code_elements))</span></span> | <span data-ttu-id="4c5ac-125">PT (= ポルトガル)</span><span class="sxs-lookup"><span data-stu-id="4c5ac-125">PT (= Portugal)</span></span>                   |
| <span data-ttu-id="4c5ac-126">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="4c5ac-126">Feature type</span></span>        | <span data-ttu-id="4c5ac-127">REG</span><span class="sxs-lookup"><span data-stu-id="4c5ac-127">REG</span></span>     | <span data-ttu-id="4c5ac-128">機能のタイプ</span><span class="sxs-lookup"><span data-stu-id="4c5ac-128">The type of feature</span></span>                                                                                                           | <span data-ttu-id="4c5ac-129">REG</span><span class="sxs-lookup"><span data-stu-id="4c5ac-129">REG</span></span>                               |
| <span data-ttu-id="4c5ac-130">証明の名前</span><span class="sxs-lookup"><span data-stu-id="4c5ac-130">Certification name</span></span>  | <span data-ttu-id="4c5ac-131">テキスト</span><span class="sxs-lookup"><span data-stu-id="4c5ac-131">Text</span></span>    | <span data-ttu-id="4c5ac-132">証明書とそのアプリケーションを説明する短いタイトル</span><span class="sxs-lookup"><span data-stu-id="4c5ac-132">A short title that describes the certification and its application</span></span>                                                            | <span data-ttu-id="4c5ac-133">会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="4c5ac-133">Certification for Fiscal printers</span></span> |

<span data-ttu-id="4c5ac-134">BPM の業務プロセス ライブラリでは、**APQC レベル 8.0 財務リソースの管理 (10009)** に認証を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-134">In the BPM business process library, certifications should be located under **APQC level 8.0 Manage Financial Resources (10009)**.</span></span> 

<span data-ttu-id="4c5ac-135">**例**</span><span class="sxs-lookup"><span data-stu-id="4c5ac-135">**Example**</span></span>

-   <span data-ttu-id="4c5ac-136">APQC レベル 8.0 財務リソースの管理 (10009)</span><span class="sxs-lookup"><span data-stu-id="4c5ac-136">APQC level 8.0 Manage Financial Resources (10009)</span></span>
    -   <span data-ttu-id="4c5ac-137">PT-REG-会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="4c5ac-137">PT-REG-Certification for Fiscal printers</span></span>

<span data-ttu-id="4c5ac-138">BPM の詳細については、[ビジネス プロセス モデラー (BPM) のフローチャート](../lifecycle-services/flowcharts-business-process-modeler.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4c5ac-138">For more information about BPM, see [Flowcharts in Business process modeler (BPM)](../lifecycle-services/flowcharts-business-process-modeler.md).</span></span>





[!INCLUDE[footer-include](../../../includes/footer-banner.md)]