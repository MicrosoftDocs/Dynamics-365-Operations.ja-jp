---
title: Dynamics 365 Supply Chain Management の顧客ポータルの概要
description: このトピックでは、顧客ポータルの概要とその使用方法および機能について説明します。
author: dasani-madipalli
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 50c9ac9106487fe04ccf704907c59b9a414b6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840752"
---
# <a name="customer-portal-for-dynamics-365-supply-chain-management-overview"></a><span data-ttu-id="e52a1-103">Dynamics 365 Supply Chain Management の顧客ポータルの概要</span><span class="sxs-lookup"><span data-stu-id="e52a1-103">Customer portal for Dynamics 365 Supply Chain Management overview</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="what-is-the-customer-portal"></a><span data-ttu-id="e52a1-104">顧客のポータルの概要</span><span class="sxs-lookup"><span data-stu-id="e52a1-104">What is the Customer portal?</span></span>

<span data-ttu-id="e52a1-105">最新のサプライ チェーンシステムは統合と依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-105">Modern supply chain systems rely on integration.</span></span> <span data-ttu-id="e52a1-106">そのためには、在庫、顧客需要、販売部門を個別の格納するのではなく統合する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-106">They require that inventory, customer demand, and sales departments be integrated instead of residing in separate silos.</span></span> <span data-ttu-id="e52a1-107">顧客ポータルを使用することで、Microsoft Dynamics 365 Supply Chain Management を実行している組織がこの統合を促進し、顧客に情報をより効果的に提供することができます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-107">The Customer portal helps organizations that run Microsoft Dynamics 365 Supply Chain Management enhance this integration and more effectively keep their customers informed.</span></span>

<span data-ttu-id="e52a1-108">顧客ポータルは、[Power Apps ポータル](https://docs.microsoft.com/powerapps/maker/portals/overview)のテンプレートを指し、販売注文の処理に関連するシナリオに対して、外部と接する企業間 (B2B) の Web サイトを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-108">The Customer portal is a [Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) template that lets companies create an externally facing business-to-business (B2B) website for scenarios that are related to sales order processing.</span></span> <span data-ttu-id="e52a1-109">このテンプレートでは、[デュアル書き込み ](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)、Supply Chain Management、Power Apps ポータルを使用して、外部企業の顧客が Dynamics 365 環境からデータを表示および作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-109">The template uses [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), Supply Chain Management, and Power Apps portals to enable external enterprise customers to view and create data from the company's Dynamics 365 environment.</span></span>

<span data-ttu-id="e52a1-110">顧客ポータル テンプレートには、Power Apps ポータル機能のすべてのカスタマイズ機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="e52a1-110">The Customer portal template has all the customization capabilities that the portals feature of Power Apps offers.</span></span> <span data-ttu-id="e52a1-111">テンプレートの変更は簡単に行うことができ、企業のブランドを表わす、機能の強化、ユーザー エクスペリエンスの変更をすることができます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-111">The template can easily be modified to represent the company's brand, add increased functionality, and change the user experience.</span></span> <span data-ttu-id="e52a1-112">テンプレートが提供するすべての機能は必要に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-112">All the functionality that the template offers out of the box can be modified as desired.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e52a1-113">テンプレートそのものが、完全に機能するとは限りません。</span><span class="sxs-lookup"><span data-stu-id="e52a1-113">By itself, the template isn't expected to be completely functional.</span></span> <span data-ttu-id="e52a1-114">企業の顧客が Supply Chain Management のデータにアクセスできるよう、外部向けの Web サイトを作成したいと考えている顧客のためのイネーブラーとしての役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="e52a1-114">It just serves as an enabler for customers who want to create an externally facing website so that enterprise customers can engage with data from Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="e52a1-115">顧客ポータルのドキュメントは、Supply Chain Management の顧客ポータルをインストールや設定を行う管理者、カスタマイザー、システム インテグレーターに向けられています。</span><span class="sxs-lookup"><span data-stu-id="e52a1-115">The Customer portal documentation is directed at admins, customizers, and system integrators who will set up the Customer portal for a Supply Chain Management installation.</span></span> <span data-ttu-id="e52a1-116">Supply Chain Management を運用している組織の顧客や、最終的なポータルの利用者は、_顧客_ と _ユーザー_ という用語で表わされます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-116">It uses the terms _customer_ and _user_ to describe people who are customers of the organization that is running Supply Chain Management, and who will use the final portal itself.</span></span>

## <a name="video"></a><span data-ttu-id="e52a1-117">ビデオ</span><span class="sxs-lookup"><span data-stu-id="e52a1-117">Video</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE4ylwW]

<span data-ttu-id="e52a1-118">[Dynamics 365 Supply Chain Management の顧客ポータル テンプレート](https://youtu.be/nPrqoLuHfV8) ビデオ (上記参照) は、YouTube で利用可能な [Finance and Operations 再生リスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="e52a1-118">The [Overview of the Customer portal template in Dynamics 365 Supply Chain Management](https://youtu.be/nPrqoLuHfV8) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="who-should-use-it"></a><span data-ttu-id="e52a1-119">対象となるユーザー</span><span class="sxs-lookup"><span data-stu-id="e52a1-119">Who should use it?</span></span>

<span data-ttu-id="e52a1-120">顧客ポータルは、Supply Chain Managementを実行し、次の特性を持つ企業に向けて設計されています :</span><span class="sxs-lookup"><span data-stu-id="e52a1-120">The Customer portal is designed for companies that run Supply Chain Management and have these characteristics:</span></span>

- <span data-ttu-id="e52a1-121">こうした企業は、注文処理情報 (注文状況やアカウント情報など) を、Supply Chain Management システムから企業の顧客に直接連絡する、外部に向けた Webサイトの構築を目的としています。</span><span class="sxs-lookup"><span data-stu-id="e52a1-121">They want to build an externally facing website that communicates order processing information (such as order status or account information) directly from their Supply Chain Management system to their enterprise customers.</span></span>
- <span data-ttu-id="e52a1-122">Dynamics AX 2012 から Supply Chain Management へと移行しており、以前は [AX 2012 Customer self-service portal](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal) を使用していました。</span><span class="sxs-lookup"><span data-stu-id="e52a1-122">They are transitioning from Dynamics AX 2012 to Supply Chain Management and previously used the [AX 2012 Customer self-service portal](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/about-the-customer-self-service-portal).</span></span>

<span data-ttu-id="e52a1-123">次のようなタイプの組織は、顧客ポータルの実装には **向いていない** でしょう :</span><span class="sxs-lookup"><span data-stu-id="e52a1-123">The following types of organizations are **not** good candidates for implementing the Customer portal:</span></span>

- <span data-ttu-id="e52a1-124">エンタープライズ以外の顧客に向けて Web サイトを構築する企業。</span><span class="sxs-lookup"><span data-stu-id="e52a1-124">Companies that want to build a website for non-enterprise customers.</span></span> <span data-ttu-id="e52a1-125">こうした企業は、[Dynamics 365 Commerce e-コマースの Web サイト](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site) 作成を検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-125">These companies should consider creating a [Dynamics 365 Commerce e-commerce website](https://docs.microsoft.com/dynamics365/commerce/create-ecommerce-site).</span></span>
- <span data-ttu-id="e52a1-126">既存の Power Apps Web サイトを同様の目的で使用している企業。</span><span class="sxs-lookup"><span data-stu-id="e52a1-126">Companies that are already using an existing Power Apps portals website for a similar purpose.</span></span> <span data-ttu-id="e52a1-127">このような企業には、顧客ポータルをしようしてもさらなる恩恵を得ることはないでしょう。</span><span class="sxs-lookup"><span data-stu-id="e52a1-127">These companies won't receive any additional benefits from the Customer portal.</span></span> <span data-ttu-id="e52a1-128">顧客ポータルは、デュアル書き込み、Supply Chain Management、Power Apps ポータル間の「点と点をつなげる」ことを希望する顧客に向けたガイドとなるテンプレートとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-128">The Customer portal is delivered as a template that acts as a guide and a starting point for customers who want to "connect the dots" between dual-write, Supply Chain Management, and Power Apps portals.</span></span> <span data-ttu-id="e52a1-129">この目的を果たす Web サイトを既に設定している場合は、顧客ポータル テンプレートを使用して Web サイトの再プロビジョニングを行っても多くの恩恵を得られない場合があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-129">If you've already set up a website that serves this purpose, you might not gain much value from using the Customer portal template to re-provision that website.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="e52a1-130"> どのような仕組みですか?</span><span class="sxs-lookup"><span data-stu-id="e52a1-130">How does it work?</span></span>

<span data-ttu-id="e52a1-131">顧客 ポータルは、Power Apps ポータルのテンプレートとして提供されます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-131">The Customer portal is provided as a Power Apps portals template.</span></span> <span data-ttu-id="e52a1-132">これは、Power Apps ポータルとデュアル書き込みに対して依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-132">It depends on Power Apps portals and dual-write.</span></span>

<span data-ttu-id="e52a1-133">[Power Appsポータル](https://docs.microsoft.com/powerapps/maker/portals/overview)を使用することで、組織の外部のユーザーがログインできる外部向けの Web サイトをユーザーが作成できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-133">[Power Apps portals](https://docs.microsoft.com/powerapps/maker/portals/overview) is a feature that lets users create an externally facing website that people from outside the organization can sign in to.</span></span> <span data-ttu-id="e52a1-134">ポータルの作成には、コードの記述がほとんど必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e52a1-134">Little to no coding is required to make portals.</span></span> <span data-ttu-id="e52a1-135">顧客ポータルは、Microsoft から入手可能な、多くの [Dynamics 365 ポータルテンプレート](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) の1つです。</span><span class="sxs-lookup"><span data-stu-id="e52a1-135">The Customer portal is one of many [Dynamics 365 portal templates](https://docs.microsoft.com/powerapps/maker/portals/portal-templates#environment-with-model-driven-apps-in-dynamics-365) that are available from Microsoft.</span></span>

<span data-ttu-id="e52a1-136">[デュアル書き込み](https://docs.microsoft.com/powerapps/maker/portals/overview) は、Customer Engagement アプリと Finance and Operations アプリの間の、ほぼリアルタイムの対話を提供する既成のインフラストラクチャ製品です。</span><span class="sxs-lookup"><span data-stu-id="e52a1-136">[Dual-write](https://docs.microsoft.com/powerapps/maker/portals/overview) is an out-of-box infrastructure product that provides near-real-time interaction between customer engagements apps and Finance and Operations apps.</span></span> <span data-ttu-id="e52a1-137">デュアル書き込みは、Finance and Operations アプリと Microsoft Dataverse の間で密に結合された双方向の統合を可能とします。</span><span class="sxs-lookup"><span data-stu-id="e52a1-137">Dual-write provides bidirectional integration between Finance and Operations apps and Microsoft Dataverse.</span></span> <span data-ttu-id="e52a1-138">そのため、アプリを横断して統合されたユーザー エクスペリエンスを実現します。</span><span class="sxs-lookup"><span data-stu-id="e52a1-138">Therefore, it provides an integrated user experience across the apps.</span></span> <span data-ttu-id="e52a1-139">顧客ポータルは、デュアル書き込みと同期されているテーブルに依存関係があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-139">The Customer portal depends on tables that are synced with dual-write.</span></span> <span data-ttu-id="e52a1-140">Supply Chain Management からのデータを顧客ポータルで表示する前に、デュアル書き込みをすべての適切なテーブルに対して有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e52a1-140">Before data from Supply Chain Management can be surfaced in the Customer portal, dual-write must be enabled for all the appropriate tables.</span></span>

<span data-ttu-id="e52a1-141">![顧客ポータルの依存関係](media/customer-portal-elements.png "顧客ポータルの依存関係")</span><span class="sxs-lookup"><span data-stu-id="e52a1-141">![Customer portal dependencies](media/customer-portal-elements.png "Customer portal dependencies")</span></span>

<span data-ttu-id="e52a1-142">顧客ポータルは、 Power Apps ポータルを使用して Supply Chain Management のインストール データを使用した外部向けの Web サイトを構築したいと考えている組織にとっての出発点としての役割を果たします。</span><span class="sxs-lookup"><span data-stu-id="e52a1-142">The Customer portal acts as a starting point for organizations that want to use Power Apps portals to build an externally facing website that uses data from their Supply Chain Management installation.</span></span> <span data-ttu-id="e52a1-143">これにより、組織は、デュアル書き込み、Supply Chain Management、Power Apps ポータルを接続することができます。</span><span class="sxs-lookup"><span data-stu-id="e52a1-143">It helps organizations connect dual-write, Supply Chain Management, and Power Apps portals.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]