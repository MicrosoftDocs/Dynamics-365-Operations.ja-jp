---
title: コンテンツ配信ネットワークの実装オプション
description: このトピックでは、Microsoft Dynamics 365 Commerce 環境で使用できるコンテンツ配信ネットワーク (CDN) の実装に関するさまざまなオプションを確認します。 オプションには、Azure Front Door のコマース提供のインスタンスおよび Azure Front Door の顧客所有のインスタンスであるネイティブが含まれます。
author: BrianShook
manager: AnnBe
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: ae0769b7e19f80244186c51454444c499c5e497f
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582806"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="a7b89-104">コンテンツ配信ネットワークの実装オプション</span><span class="sxs-lookup"><span data-stu-id="a7b89-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7b89-105">このトピックでは、Microsoft Dynamics 365 Commerce 環境で使用できるコンテンツ配信ネットワーク (CDN) の実装に関するさまざまなオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="a7b89-106">オプションには、Azure Front Door のコマース提供のインスタンスおよび Azure Front Door の顧客所有のインスタンスであるネイティブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="a7b89-107">コマースの顧客は、コマース環境でどの CDN サービスを使用するか検討する際、いくつかのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="a7b89-108">コマースは、基本的なホストとカスタム ドメインの要件をカバーする基本的な Azure Front Door サポートとともにリリースされます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="a7b89-109">Web アプリケーション ファイアウォール (WAF) など、より詳細な制御機能とより具体的なセキュリティ能力を必要とする会社では、最良なオプションは Azure Front Door の顧客所有のインスタンスまたは外部の CDN サービスのいずれかを使用することです。</span><span class="sxs-lookup"><span data-stu-id="a7b89-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="a7b89-110">次の 3 つの CDN 実装オプションがコマース環境で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="a7b89-111">Azure Front Door のコマース提供インスタンス</span><span class="sxs-lookup"><span data-stu-id="a7b89-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="a7b89-112">Azure Front Door の顧客所有インスタンス (制御強化と追加セキュリティ機能に向け)</span><span class="sxs-lookup"><span data-stu-id="a7b89-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="a7b89-113">外部 CDN サービス</span><span class="sxs-lookup"><span data-stu-id="a7b89-113">An external CDN service</span></span>

<span data-ttu-id="a7b89-114">3 つすべての CDN 実装オプションは、カスタム ドメインからの動的な HTML コンテンツのみを提供します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="a7b89-115">コマースでは自動的に全ての JavaScript、Cascading Style Sheets (CSS)、画像、動画、そして Microsoft 管理の CDN を使った他の静的コンテンツを管理します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="a7b89-116">選択するオプションによって、運用能力、制御機能、および追加のセキュリティ機能が決まります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="a7b89-117">次の図では、コマース アーキテクチャの概要を表示します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![コマース アーキテクチャの概要](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="a7b89-119">コマース サイトの Azure Front Door インスタンスを設定する方法については、[CDN サポートを追加](add-cdn-support.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7b89-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="a7b89-120">コマース提供 Azure Front Door インスタンスの使用</span><span class="sxs-lookup"><span data-stu-id="a7b89-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="a7b89-121">次の表では、コンテンツ エンドポイントを管理するための Azure Fron Door のコマース提供インスタンスを使うことの長所と短所が示されています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="a7b89-122">プロ</span><span class="sxs-lookup"><span data-stu-id="a7b89-122">Pros</span></span> | <span data-ttu-id="a7b89-123">短所</span><span class="sxs-lookup"><span data-stu-id="a7b89-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="a7b89-124">このインスタンスは、コマースの原価に含まれます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="a7b89-125">このインスタンスはコマース チームによって管理されているため、メンテナンスの必要量を減らし、共有のセットアップ手順があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="a7b89-126">Azure でホストされたインフラストラクチャは、スケーラブル、セキュリティ、および信頼性があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="a7b89-127">Secure Sockets Layer (SSL) 証明書は、1 回の設定が必要で、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="a7b89-128">このインスタンスでは、コマース チームがエラーや変更を監視します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="a7b89-129">WAF はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a7b89-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="a7b89-130">具体的なカスタマイズや設定調整はありません。</span><span class="sxs-lookup"><span data-stu-id="a7b89-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="a7b89-131">このインスタンスは、コマース チームによって更新や変更が異なります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="a7b89-132">apex ドメインには別の Azure Front Door インスタンスが必要であり、Azure DNS の統合 apex ドメインには追加の作業が必要です。</span><span class="sxs-lookup"><span data-stu-id="a7b89-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="a7b89-133">顧客には、1 秒あたりの応答 (RPS) やエラー率に関する製品利用統計情報は提供されません。</span><span class="sxs-lookup"><span data-stu-id="a7b89-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="a7b89-134">次の図は、コマースが提供する Azure Front Door インスタンスのアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![コマース提供 Azure Front Door インスタンス](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="a7b89-136">顧客所有 Azure Front Door インスタンスの使用</span><span class="sxs-lookup"><span data-stu-id="a7b89-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="a7b89-137">次の表では、コンテンツ エンドポイントを管理するための Azure Fron Door の顧客所有インスタンスを使うことの長所と短所が示されています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="a7b89-138">プロ</span><span class="sxs-lookup"><span data-stu-id="a7b89-138">Pros</span></span> | <span data-ttu-id="a7b89-139">短所</span><span class="sxs-lookup"><span data-stu-id="a7b89-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="a7b89-140">設定はセキュリティで保護され、管理が容易です。</span><span class="sxs-lookup"><span data-stu-id="a7b89-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="a7b89-141">Azure でホストされたインフラストラクチャは、スケーラブル、セキュリティ、および信頼性があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="a7b89-142">このインスタンスでは、使用しているサイト向けに特別に調整されているより細かい等級のセキュリティに対して、WAF 統合およびきめ細かいルール制御が許可されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="a7b89-143">このインスタンスでは、SSL 証明書 (顧客所有と Azure Front Door 管理の両方) およびドメイン リンクの詳細な制御が可能です。</span><span class="sxs-lookup"><span data-stu-id="a7b89-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="a7b89-144">このインスタンスは、Azure DNS に直接使用される場合、ドメイン ソリューションを提供します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="a7b89-145">製品利用統計情報および警告機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="a7b89-146">SSL 証明書は、1 回の設定が必要で、自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="a7b89-147">インスタンスはセルフ管理されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="a7b89-148">初期知識のランプ アップが必要です。</span><span class="sxs-lookup"><span data-stu-id="a7b89-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="a7b89-149">次の図は、顧客所有 Azure Front Door インスタンスを含むコマース インフラストラクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![顧客所有 Azure Front Door インスタンスを含むコマース インフラストラクチャ](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="a7b89-151">外部 CDN サービスの使用</span><span class="sxs-lookup"><span data-stu-id="a7b89-151">Use an external CDN service</span></span>

<span data-ttu-id="a7b89-152">次の表に、コンテンツ エンドポイントを管理するにあたり、外部 CDN サービスを使用の長所と短所を示します。</span><span class="sxs-lookup"><span data-stu-id="a7b89-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="a7b89-153">プロ</span><span class="sxs-lookup"><span data-stu-id="a7b89-153">Pros</span></span> | <span data-ttu-id="a7b89-154">短所</span><span class="sxs-lookup"><span data-stu-id="a7b89-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="a7b89-155">このオプションは、既存のドメインが既に外部 CDN でホストされている場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a7b89-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="a7b89-156">競合他社 CDN (たとえば、Akamai) は、WAF 機能を持つ場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="a7b89-157">別途契約を作成し、追加の原価設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="a7b89-158">SSL は追加費用が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="a7b89-159">サービスは Azure クラウド構造とは別ので、追加のインフラストラクチャを管理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="a7b89-160">サービスでは、エンドポイントおよびセキュリティの設定に要する時間が長くなる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7b89-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="a7b89-161">サービスはセルフ管理されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-161">The service is self-managed.</span></span></li><li><span data-ttu-id="a7b89-162">サービスはセルフ監視されます。</span><span class="sxs-lookup"><span data-stu-id="a7b89-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="a7b89-163">次の図は、外部の CDN サービスを含むコマース インフラストラクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="a7b89-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![外部の CDN サービスを含むコマース インフラストラクチャ](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="a7b89-165">追加リソース</span><span class="sxs-lookup"><span data-stu-id="a7b89-165">Additional resources</span></span>

[<span data-ttu-id="a7b89-166">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="a7b89-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
