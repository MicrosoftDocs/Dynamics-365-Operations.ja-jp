---
title: Dynamics 365 Commerce の評価環境に関するよく寄せられる質問
description: このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e42618a522f5ad551f608605300c30b5ffb8e299
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795934"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a><span data-ttu-id="e5962-103">Dynamics 365 Commerce 評価環境に関してよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="e5962-103">Dynamics 365 Commerce evaluation environment FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5962-104">このトピックでは、Microsoft Dynamics 365 Commerce の評価環境についてよく寄せられる質問に対する回答を示します。</span><span class="sxs-lookup"><span data-stu-id="e5962-104">This topic provides answers to frequently asked questions about the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="e5962-105">**現在 Retail を実装する顧客に対して、コマースの評価環境を eコマース店舗として使用できますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-105">**Can we use the Commerce evaluation environment as an e-Commerce storefront for customers that currently implement Retail?**</span></span>

<span data-ttu-id="e5962-106">No.</span><span class="sxs-lookup"><span data-stu-id="e5962-106">No.</span></span> <span data-ttu-id="e5962-107">コマースの評価環境は評価用にのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="e5962-107">The Commerce evaluation environment is only for evaluation.</span></span> <span data-ttu-id="e5962-108">Retail を実装する顧客に環境が必要な場合は、Microsoft にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="e5962-108">If you require an environment for a customer that implements Retail, contact Microsoft.</span></span>

<span data-ttu-id="e5962-109">**コマースの評価環境を使用して、Retail を実装する既存のアプリケーション/環境の上に eコマース機能をプロビジョニングできますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-109">**Can the Commerce evaluation environment be used to provision the e-Commerce features on top of an existing application/environment that implements Retail?**</span></span>

<span data-ttu-id="e5962-110">できません (多くの場合)。</span><span class="sxs-lookup"><span data-stu-id="e5962-110">No (mostly).</span></span> <span data-ttu-id="e5962-111">コマースの評価コンポーネントは、前提条件とプロビジョニング ガイドで指定されている構成に一致する環境でのみ利用できます。</span><span class="sxs-lookup"><span data-stu-id="e5962-111">The Commerce evaluation components are available only to environments that match the configurations that are specified in the prerequisites and provisioning guide.</span></span> <span data-ttu-id="e5962-112">また、10.0.8 以前の初期リリース版でデプロイされた環境では、必要となる基本デモ データは利用できません。</span><span class="sxs-lookup"><span data-stu-id="e5962-112">Additionally, the required base demo data won't be available in environments that were deployed with an initial release that is earlier than 10.0.8.</span></span> 

<span data-ttu-id="e5962-113">**Microsoft Dynamics Lifecycle Services (LCS) を介して Microsoft Azure で コマースの評価環境をデプロイするには、どのような費用がかかりますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-113">**What costs are involved in deploying the Commerce evaluation environment on Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?**</span></span>

<span data-ttu-id="e5962-114">従来の Dynamics 365 Finance / Dynamics 365 Supply Chain Management / Dynamics 365 Commerce 本部のデモ環境 (仮想マシン \[VM \]) は、Azure サブスクリプションでホストされます。</span><span class="sxs-lookup"><span data-stu-id="e5962-114">A traditional Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce headquarters demo environment (virtual machine \[VM\]) will be hosted in your Azure subscription.</span></span> <span data-ttu-id="e5962-115">[Azure 価格計算ツール](https://azure.microsoft.com/pricing/calculator/) を使用してこのコストを見積もることができます。</span><span class="sxs-lookup"><span data-stu-id="e5962-115">You can use the [Azure pricing calculator](https://azure.microsoft.com/pricing/calculator/) to estimate this cost.</span></span>

<span data-ttu-id="e5962-116">Commerce Scale Unit、コマース サイト ビルダー、eコマース サイトなどのコンポーネントは、software as a service (SaaS) として提供され、Microsoft がホストしています。</span><span class="sxs-lookup"><span data-stu-id="e5962-116">Other components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site will be available as software as a service (SaaS) and hosted by Microsoft.</span></span>

<span data-ttu-id="e5962-117">**コマースの評価環境で現在サポートされている Azure 地域はどこですか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-117">**Which Azure geographies are currently supported for the Commerce evaluation environment?**</span></span>

<span data-ttu-id="e5962-118">コマースの評価環境は、北米地域でのみデプロイ可能です。</span><span class="sxs-lookup"><span data-stu-id="e5962-118">The Commerce evaluation environment can be deployed only in the North America geography.</span></span>

<span data-ttu-id="e5962-119">**完全な OneBox 仮想マシン (VM) オプションを含む、ダウンロード可能な仮想ハード ディスク (VHD) はありますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-119">**Is there a downloadable virtual hard disk (VHD) that has the complete OneBox virtual machine (VM) option?**</span></span>

<span data-ttu-id="e5962-120">Dynamics 365 Commerce と Commerce Scale Unit は、完全に software as a service (SaaS) であり、クラウドでホストされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5962-120">Dynamics 365 Commerce and Commerce Scale Unit are completely software as a service (SaaS) and must be cloud-hosted.</span></span>

<span data-ttu-id="e5962-121">**コマースの評価環境は、どのくらいの期間使用できますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-121">**How long can the Commerce evaluation environment be used?**</span></span>

<span data-ttu-id="e5962-122">コマースの評価環境には、Commerce Scale Unit、コマース サイト ビルダーなどの SaaS コンポーネントが提供された日から30日間の期間制限が設定されています。</span><span class="sxs-lookup"><span data-stu-id="e5962-122">The Commerce evaluation environment has a 30-day time limit from the date when SaaS components such as Commerce Scale Unit, Commerce site builder, and your e-Commerce site are provisioned.</span></span>

<span data-ttu-id="e5962-123">**コマースの評価環境の期限設定は延長できますか ?**</span><span class="sxs-lookup"><span data-stu-id="e5962-123">**Can I extend the time limit for my Commerce evaluation environment?**</span></span>

<span data-ttu-id="e5962-124">制限時間の延長は例外対応となり、状況に応じて考慮されます。</span><span class="sxs-lookup"><span data-stu-id="e5962-124">Extension of the time limit is an exception to the norm and is considered on a case-by-case basis.</span></span> <span data-ttu-id="e5962-125">Microsoft パートナーの連絡先にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="e5962-125">You should reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5962-126">追加リソース</span><span class="sxs-lookup"><span data-stu-id="e5962-126">Additional resources</span></span>

[<span data-ttu-id="e5962-127">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="e5962-127">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e5962-128">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="e5962-128">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e5962-129">Dynamics 365 Commerce の評価環境を構成する</span><span class="sxs-lookup"><span data-stu-id="e5962-129">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e5962-130">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="e5962-130">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e5962-131">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="e5962-131">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]