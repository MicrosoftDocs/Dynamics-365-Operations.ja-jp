---
title: 機能タイトルの規制認証情報
description: ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは意図したマーケットでの販売を、法律に準拠したものにするために。ソリューションが必要とする規制認証に関する詳細を含める必要があります。 この記事では、機能のタイトルに認証に関する情報をどのように使用しているかを示します。
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: shylaw
ms.search.scope: Operations
ms.custom: 27581
ms.assetid: d0b8286a-b2c1-4fa2-905a-3383b1d34d56
ms.search.region: global
ms.author: janeaug
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 67dc99d11df923416e8890a3ab22a6fe74990ebc
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537248"
---
# <a name="regulatory-certification-information-in-feature-titles"></a><span data-ttu-id="859ed-104">機能タイトルの規制認証情報</span><span class="sxs-lookup"><span data-stu-id="859ed-104">Regulatory certification information in feature titles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="859ed-105">ローカライズ &amp; 翻訳向け LCS ソリューションの要件の一部として、ローカライズ ISV ソリューション プロバイダーは意図したマーケットでの販売を、法律に準拠したものにするために。ソリューションが必要とする規制認証に関する詳細を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="859ed-105">As part of the requirements for LCS solutions for localization &amp; translation, localization ISV solution providers must include details about any regulatory certifications that the solution requires in order to be legally compliant for sale in the intended market.</span></span> <span data-ttu-id="859ed-106">この記事では、機能のタイトルに認証に関する情報をどのように使用しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="859ed-106">This article shows how information about certifications is used in the title of the feature.</span></span>

<span data-ttu-id="859ed-107">規制証明には、データ プライバシーから特定の規制に準拠する認定まで。さまざまな形式があります。</span><span class="sxs-lookup"><span data-stu-id="859ed-107">Regulatory certification can take various forms, from data privacy to certification of compliance with specific regulations.</span></span> <span data-ttu-id="859ed-108">ただし、すべての規制認証にある共通の 1 つの点は、実施するの国/地域の法令や規制によって要求されるということです。</span><span class="sxs-lookup"><span data-stu-id="859ed-108">However, one thing that all regulatory certifications have in common is that they are required by the laws and regulations of the country/region of operation.</span></span> <span data-ttu-id="859ed-109">これらの認定は強制され、遵守しない場合、その国/地域で事業を行う組織にとって深刻な結果につながる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="859ed-109">These certifications are enforced, and non-adherence can lead to severe consequences for an organization that does business in that country/region.</span></span> <span data-ttu-id="859ed-110">業務プロセス ライブラリが構築されたとき、規制認証は、ローカライズ ソリューション機能のタイトルによって、Microsoft Dynamics Lifecycle Services (LCS) の業務プロセス モデラー (BPM) ライブラリの規制に関する要件として識別する必要があります。</span><span class="sxs-lookup"><span data-stu-id="859ed-110">When the business process library is constructed, regulatory certifications must be identified as regulatory requirements in the Microsoft Dynamics Lifecycle Services (LCS) Business process modeler (BPM) library through the title of the localization solution feature.</span></span> <span data-ttu-id="859ed-111">このタイトルのラベルは、次のテーブルに示すように、接頭辞による国/地域および認証タイプを示す次の命名規則に準拠します。</span><span class="sxs-lookup"><span data-stu-id="859ed-111">The label for this title will conform to the following naming convention that indicates the country/region and certification type through prefixes, as shown in the following table.</span></span>

| <span data-ttu-id="859ed-112">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="859ed-112">Feature type</span></span> | <span data-ttu-id="859ed-113">書式設定</span><span class="sxs-lookup"><span data-stu-id="859ed-113">Format</span></span>                      | <span data-ttu-id="859ed-114">例</span><span class="sxs-lookup"><span data-stu-id="859ed-114">Example</span></span>                                  |
|--------------|-----------------------------|------------------------------------------|
| <span data-ttu-id="859ed-115">規制</span><span class="sxs-lookup"><span data-stu-id="859ed-115">Regulatory</span></span>   | <span data-ttu-id="859ed-116">xx 用 XX-REG-Certification</span><span class="sxs-lookup"><span data-stu-id="859ed-116">XX-REG-Certification for xx</span></span> | <span data-ttu-id="859ed-117">PT-REG-会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="859ed-117">PT-REG-Certification for Fiscal printers</span></span> |

<span data-ttu-id="859ed-118">次のテーブルに、名前付け規則のコンポーネントを示します。</span><span class="sxs-lookup"><span data-stu-id="859ed-118">The following table explains the components of the naming convention.</span></span>

| <span data-ttu-id="859ed-119">コンポーネント名</span><span class="sxs-lookup"><span data-stu-id="859ed-119">Component name</span></span>      |  <span data-ttu-id="859ed-120">書式設定</span><span class="sxs-lookup"><span data-stu-id="859ed-120">Format</span></span> | <span data-ttu-id="859ed-121">説明</span><span class="sxs-lookup"><span data-stu-id="859ed-121">Description</span></span>                                                                                                                   | <span data-ttu-id="859ed-122">例</span><span class="sxs-lookup"><span data-stu-id="859ed-122">Example</span></span>                           |
|---------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span data-ttu-id="859ed-123">国/地域コード</span><span class="sxs-lookup"><span data-stu-id="859ed-123">Country/region code</span></span> | <span data-ttu-id="859ed-124">XX</span><span class="sxs-lookup"><span data-stu-id="859ed-124">XX</span></span>      | <span data-ttu-id="859ed-125">2 文字の ISO 国/地域コード ([ISO 3166 規格](http://www.iso.org/iso/country_names_and_code_elements))</span><span class="sxs-lookup"><span data-stu-id="859ed-125">The two-letter ISO country/region code (from the [ISO 3166 standard](http://www.iso.org/iso/country_names_and_code_elements))</span></span> | <span data-ttu-id="859ed-126">PT (= ポルトガル)</span><span class="sxs-lookup"><span data-stu-id="859ed-126">PT (= Portugal)</span></span>                   |
| <span data-ttu-id="859ed-127">フィーチャー タイプ</span><span class="sxs-lookup"><span data-stu-id="859ed-127">Feature type</span></span>        | <span data-ttu-id="859ed-128">REG</span><span class="sxs-lookup"><span data-stu-id="859ed-128">REG</span></span>     | <span data-ttu-id="859ed-129">機能のタイプ</span><span class="sxs-lookup"><span data-stu-id="859ed-129">The type of feature</span></span>                                                                                                           | <span data-ttu-id="859ed-130">REG</span><span class="sxs-lookup"><span data-stu-id="859ed-130">REG</span></span>                               |
| <span data-ttu-id="859ed-131">証明の名前</span><span class="sxs-lookup"><span data-stu-id="859ed-131">Certification name</span></span>  | <span data-ttu-id="859ed-132">テキスト</span><span class="sxs-lookup"><span data-stu-id="859ed-132">Text</span></span>    | <span data-ttu-id="859ed-133">証明書とそのアプリケーションを説明する短いタイトル</span><span class="sxs-lookup"><span data-stu-id="859ed-133">A short title that describes the certification and its application</span></span>                                                            | <span data-ttu-id="859ed-134">会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="859ed-134">Certification for Fiscal printers</span></span> |

<span data-ttu-id="859ed-135">BPM の業務プロセス ライブラリでは、**APQC レベル 8.0 財務リソースの管理 (10009)** に認証を配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="859ed-135">In the BPM business process library, certifications should be located under **APQC level 8.0 Manage Financial Resources (10009)**.</span></span> <span data-ttu-id="859ed-136">**例**</span><span class="sxs-lookup"><span data-stu-id="859ed-136">**Example**</span></span>

-   <span data-ttu-id="859ed-137">APQC レベル 8.0 財務リソースの管理 (10009)</span><span class="sxs-lookup"><span data-stu-id="859ed-137">APQC level 8.0 Manage Financial Resources (10009)</span></span>
    -   <span data-ttu-id="859ed-138">PT-REG-会計プリンターの証明</span><span class="sxs-lookup"><span data-stu-id="859ed-138">PT-REG-Certification for Fiscal printers</span></span>

<span data-ttu-id="859ed-139">BPM の詳細については、[BPM フローチャート](../lifecycle-services/flowcharts-business-process-modeler.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="859ed-139">For more information about BPM, see [BPM flowcharts](../lifecycle-services/flowcharts-business-process-modeler.md).</span></span>



