---
title: AX 2012 の個人データ要求への対応
description: このトピックは、Microsoft Dynamics AX 2012 を使用する企業、実装パートナー、および独立系ソフトウェア ベンダー (ISV) が、EUデータ保護規則 (GDPR) の下にある個人データに関する、データ主体からの要求に準拠するのに役立つでしょう。
author: ryanc
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10031
ms.search.region: Global
ms.author: ryanc
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b735ea552180fb3d262ab62a7ed185949a4df53
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750934"
---
# <a name="respond-to-requests-for-personal-data-in-ax-2012"></a><span data-ttu-id="6f8bd-103">AX 2012 の個人データ要求への対応</span><span class="sxs-lookup"><span data-stu-id="6f8bd-103">Respond to requests for personal data in AX 2012</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f8bd-104">このトピックは、Microsoft Dynamics AX 2012 を使用する企業、実装パートナー、および独立系ソフトウェア ベンダー (ISV) が、EUデータ保護規則 (GDPR) の下にある個人データに関する、データ主体からの要求に準拠するのに役立つでしょう。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-104">This topic can help businesses that use Microsoft Dynamics AX 2012, implementation partners, and independent software vendors (ISVs) comply with requests from a data subject concerning their personal data under the European Union’s General Data Protection Regulation (GDPR).</span></span> <span data-ttu-id="6f8bd-105">GDPR および Microsoft が提供する関連するリソースの詳細については、[一般データ保護規則の概要](./gdpr-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-105">For more information about the GDPR and the related resources that Microsoft provides, see the [General Data Protection Regulation overview](./gdpr-guide.md).</span></span> <span data-ttu-id="6f8bd-106">「Finance and Operations のための GDPR ガイド」は、Finance and Operations アプリのために書かれたものですが、GDPR の下でのデータ主体の権利は Dynamics AX 2012 を使用している組織にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-106">Although the "Guide to the GDPR for Finance and Operations" was written for Finance and Operations apps, the rights that a data subject has under the GDPR apply to organizations using Dynamics AX 2012.</span></span> <span data-ttu-id="6f8bd-107">「Finance and Operations のための GDPR ガイド」に記載されている手順は、個人データの要求に応答する組織により使用され、Dynamics AX 2012 を使用する組織にも適していますが、Dynamics AX 2012 では **人物検索** レポートは利用できません。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-107">The steps listed in the "Guide to the GDPR for Finance and Operations" can be used by an organization responding to a request for personal data and are also appropriate for organizations using Dynamics AX 2012, with the exception of the **Person search** report, which is not available for Dynamics AX 2012.</span></span> <span data-ttu-id="6f8bd-108">このトピックでは、Dynamics AX 2012 に固有の追加項目を一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-108">This topic lists additional points that are specific to Dynamics AX 2012.</span></span> 

## <a name="applicable-product-updates-for-dynamics-ax-2012"></a><span data-ttu-id="6f8bd-109">Dynamics AX 2012 の適用可能製品更新プログラム</span><span class="sxs-lookup"><span data-stu-id="6f8bd-109">Applicable product updates for Dynamics AX 2012</span></span>

<span data-ttu-id="6f8bd-110">AX 2012 に固有の追加の製品更新と GDPR に関連する情報は、[Microsoft Dynamics Lifecycle Services (LCS)](https://fix.lcs.dynamics.com/Issue/Results?q=3909273) から入手できます。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-110">Additional product updates and information related to GDPR that's specific to AX 2012 are available from [Microsoft Dynamics Lifecycle Services](https://fix.lcs.dynamics.com/Issue/Results?q=3909273) (LCS).</span></span> <span data-ttu-id="6f8bd-111">LCS へのアクセスには、サインインが必要です。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-111">Sign-in is required for access to LCS.</span></span> 

<span data-ttu-id="6f8bd-112">次に示す、AX 2012 で使用可能な照会およびレポートのいくつかの例は、個人データを検索およびレポートするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-112">Here are some example inquiries and reports that are available in AX 2012 that might help you find and report personal data:</span></span>

+ <span data-ttu-id="6f8bd-113">**ホーム** &gt; **一般的な** &gt; **グローバル アドレス帳**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-113">**Home** &gt; **Common** &gt; **Global address book**</span></span>

    <span data-ttu-id="6f8bd-114">照会ウィンドウで、検索ボックスに担当者の名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-114">In the inquiry window, enter a person's name in the search box.</span></span>

+ <span data-ttu-id="6f8bd-115">**買掛金勘定**&gt;**共通**&gt;**仕入先**&gt;**すべての仕入先**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-115">**Accounts payable** &gt; **Common** &gt; **Vendor** &gt; **All vendors**</span></span>
+ <span data-ttu-id="6f8bd-116">**売掛金勘定**&gt;**共通**&gt;**顧客**&gt;**すべての顧客**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-116">**Accounts receivable** &gt; **Common** &gt; **Customer** &gt; **All Customers**</span></span>
+ <span data-ttu-id="6f8bd-117">**人事管理** &gt; **共通** &gt; **作業者**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-117">**Human resources** &gt; **Common** &gt; **Workers**</span></span>
+ <span data-ttu-id="6f8bd-118">**販売とマーケティング** &gt; **共通** > **顧客**、**見込顧客**、**潜在顧客**、または **連絡先**</span><span class="sxs-lookup"><span data-stu-id="6f8bd-118">**Sales and marketing** &gt; **Common** > **Customers**, **Prospects**, **Leads**, or **Contacts**</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f8bd-119">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="6f8bd-119">Additional resources</span></span>
<span data-ttu-id="6f8bd-120">GDPR の詳細については、[欧州連合の Web サイト](https://europa.eu/) および [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-120">You can learn more about the GDPR on the [European Union's website](https://europa.eu/) and on the [Microsoft Trust Center](https://www.microsoft.com/TrustCenter/Privacy/gdpr/default.aspx).</span></span>

### <a name="disclaimer"></a><span data-ttu-id="6f8bd-121">免責事項</span><span class="sxs-lookup"><span data-stu-id="6f8bd-121">Disclaimer</span></span>
<span data-ttu-id="6f8bd-122">(c)2018 Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-122">(c)2018 Microsoft Corporation.</span></span> <span data-ttu-id="6f8bd-123">All rights reserved.</span><span class="sxs-lookup"><span data-stu-id="6f8bd-123">All rights reserved.</span></span> <span data-ttu-id="6f8bd-124">このドキュメントは、"現状のまま" 提供されます。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-124">This document is provided "as-is."</span></span> <span data-ttu-id="6f8bd-125">URL およびその他のインターネット Web サイトの参照を含む、このドキュメントの情報および見解は、予告なしに変更することがあります。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-125">Information and views expressed in this document, including URL and other Internet Web site references, may change without notice.</span></span> <span data-ttu-id="6f8bd-126">このドキュメントの使用上のリスクは、すべてユーザーが負うものとします。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-126">You bear the risk of using it.</span></span> <span data-ttu-id="6f8bd-127">このドキュメントは、Microsoft の製品に含まれる知的財産に対する法律上の権利をお客様に付与するものではありません。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-127">This document does not provide you with any legal rights to any intellectual property in any Microsoft product.</span></span> <span data-ttu-id="6f8bd-128">内部での参照を目的とする場合、このドキュメントをコピーして使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f8bd-128">You may copy and use this document for your internal, reference purposes.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]