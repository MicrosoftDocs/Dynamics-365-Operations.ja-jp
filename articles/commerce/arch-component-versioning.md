---
title: Dynamics 365 Commerceコンポーネント バージョンの管理要件
description: このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。
author: rezaassadi
manager: AnnBe
ms.date: 07/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 02cb1bf662983edb74ad5173e2c494a0edfe8d3f
ms.sourcegitcommit: 267498fbc4c54adf83b15854ecea6a93e200164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2020
ms.locfileid: "3549337"
---
# <a name="dynamics-365-commerce-component-versioning-requirements"></a><span data-ttu-id="99315-103">Dynamics 365 Commerceコンポーネント バージョンの管理要件</span><span class="sxs-lookup"><span data-stu-id="99315-103">Dynamics 365 Commerce component versioning requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="99315-104">このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="99315-104">This topic provides an overview of the component versioning requirements and dependencies for all components in the Microsoft Dynamics 365 Commerce ecosystem.</span></span>

## <a name="overview"></a><span data-ttu-id="99315-105">概要</span><span class="sxs-lookup"><span data-stu-id="99315-105">Overview</span></span>

<span data-ttu-id="99315-106">次の図は、Dynamics 365 Commerce コンポーネントの概要、それに対応するバージョン要件および依存関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="99315-106">The following illustration shows an overview of Dynamics 365 Commerce components and corresponding versioning requirements and dependencies.</span></span>

<span data-ttu-id="99315-107"><a href="https://docs.microsoft.com/en-us/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce コンポーネント バージョン要件および依存関係](./media/commerce-component-versioning.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="99315-107"><a href="https://docs.microsoft.com/en-us/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce Component versioning requirements and dependencies](./media/commerce-component-versioning.jpg)</a></span></span>

## <a name="component-dependencies"></a><span data-ttu-id="99315-108">コンポーネントの依存関係</span><span class="sxs-lookup"><span data-stu-id="99315-108">Component dependencies</span></span>

### <a name="service-updates"></a><span data-ttu-id="99315-109">サービスの更新</span><span class="sxs-lookup"><span data-stu-id="99315-109">Service updates</span></span>

<span data-ttu-id="99315-110">顧客およびパートナーがサービスおよび配置を行うすべてのコマース コンポーネントとの互換性を確保するには、更新サービス中にいくつかのバージョン依存関係に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-110">To ensure compatibility between all Commerce components that are serviced and deployed by customers and partners, you must follow several versioning dependencies during servicing updates.</span></span> <span data-ttu-id="99315-111">次のリストは、これらの依存関係をすべて示しています。</span><span class="sxs-lookup"><span data-stu-id="99315-111">The following list describes all these dependencies.</span></span>

- <span data-ttu-id="99315-112">**コマースの本部と Finance and Operations アプリは、Commerce Scale Unit (クラウドと自己ホスト型の両方) と同じバージョンか、それよりも新しいバージョンになっている必要があります。**</span><span class="sxs-lookup"><span data-stu-id="99315-112">**Commerce headquarters and Finance and Operations apps must be on the same version as, or a newer version than, Commerce Scale Unit (both cloud and self-hosted).**</span></span>

    <span data-ttu-id="99315-113">たとえば、コマースの本部と Finance and Operations アプリがバージョン 10.0.10 である場合、Commerce Scale Unit はバージョン 10.0.10 またはそれ以前 (たとえば、10.0.9 または 10.0.8) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-113">For example, if Commerce headquarters and Finance and Operations apps are on version 10.0.10, Commerce Scale Unit must be on version 10.0.10 or earlier (for example, 10.0.9 or 10.0.8).</span></span>

- <span data-ttu-id="99315-114">**Commerce Scale Unit は、Modern Point of Sale (POS)、Hardware Station、コマース ソフトウェア キット (SDK) と同じバージョンかそれより新しいバージョン、および関連するローカル サイト コンフィギュレーション (モジュール、データ アクション、テーマなど) でなくてはなりません。**</span><span class="sxs-lookup"><span data-stu-id="99315-114">**Commerce Scale Unit must be on the same version as, or a newer version than, Modern Point of Sale (POS), Hardware Station, and the Commerce software development kit (SDK) and associated local site configurations (such as modules, data actions, and themes).**</span></span>

    <span data-ttu-id="99315-115">たとえば、Commerce Scale Unit がバージョン 10.0.10 である場合、Modern POS、Hardware Station、およびコマース ストアフロントはバージョン 10.0.10 またはそれ以前 (たとえば、10.0.9 または 10.0.8) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-115">For example, if Commerce Scale Unit is on version 10.0.10, Modern POS, Hardware Station, and the Commerce storefront must be on version 10.0.10 or earlier (for example, 10.0.9 or 10.0.8).</span></span>

- <span data-ttu-id="99315-116">**拡張機能パッケージは、拡張機能が適用されるターゲット コンポーネントと同じバージョン、またはそれより新しいバージョンに対してコンパイルする必要があります。**</span><span class="sxs-lookup"><span data-stu-id="99315-116">**Extension packages must be compiled against the same version as, or a newer version than, the target component that the extension applies to.**</span></span>

    <span data-ttu-id="99315-117">たとえば、展開された Commerce Scale Unit がバージョン 10.0.10 である場合、対応する拡張パッケージをバージョン 10.0.10 またはそれ以前のバージョン (たとえば、10.0.10 または 10.0.9) に対してコンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-117">For example, if the deployed Commerce Scale Unit is on version 10.0.10, the corresponding extension packages must be compiled against version 10.0.10 or earlier (for example, 10.0.10 or 10.0.9).</span></span>

### <a name="quality-updates"></a><span data-ttu-id="99315-118">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="99315-118">Quality updates</span></span>

<span data-ttu-id="99315-119">品質更新プログラム中、サービス更新プログラムに必要なもの以外に、各コマース コンポーネントに対して特定のバージョン管理要件に従う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="99315-119">During quality updates, no specific versioning requirements must be followed for each Commerce component, besides what is required for service updates.</span></span>

## <a name="current-supported-versions"></a><span data-ttu-id="99315-120">現在サポートされているバージョン</span><span class="sxs-lookup"><span data-stu-id="99315-120">Current supported versions</span></span>

<span data-ttu-id="99315-121">次の表では、**2020 年 7 月 1 日**時点での各種コマース コンポーネントの現在のサポートされているバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="99315-121">The following table describes the current supported versions of various Commerce components as of **July 1, 2020**.</span></span>

| <span data-ttu-id="99315-122">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="99315-122">Component</span></span> | <span data-ttu-id="99315-123">最新の利用可能なリリース</span><span class="sxs-lookup"><span data-stu-id="99315-123">Latest available release</span></span> | <span data-ttu-id="99315-124">最新の使用可能なコンポーネントのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="99315-124">Latest available component version number</span></span> | <span data-ttu-id="99315-125">サポートされている最も古いリリース</span><span class="sxs-lookup"><span data-stu-id="99315-125">Earliest supported release</span></span> | <span data-ttu-id="99315-126">サポートされている最も古いコンポーネントのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="99315-126">Earliest supported component version number</span></span> |
|---|---|---|---|---|
| <span data-ttu-id="99315-127">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="99315-127">Finance and Operations apps</span></span> | <span data-ttu-id="99315-128">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-128">10.0.12</span></span> | <span data-ttu-id="99315-129">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-129">10.0.12</span></span> | <span data-ttu-id="99315-130">10.0.9</span><span class="sxs-lookup"><span data-stu-id="99315-130">10.0.9</span></span> | <span data-ttu-id="99315-131">10.0.9</span><span class="sxs-lookup"><span data-stu-id="99315-131">10.0.9</span></span> |
| <span data-ttu-id="99315-132">Commerce Scale Unit (クラウド自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="99315-132">Commerce Scale Unit (cloud-hosted)</span></span> | <span data-ttu-id="99315-133">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-133">10.0.12</span></span> | <span data-ttu-id="99315-134">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-134">9.22</span></span> | <span data-ttu-id="99315-135">10.0.9</span><span class="sxs-lookup"><span data-stu-id="99315-135">10.0.9</span></span> | <span data-ttu-id="99315-136">9.19</span><span class="sxs-lookup"><span data-stu-id="99315-136">9.19</span></span> |
| <span data-ttu-id="99315-137">Commerce ストア スターター キット (SSK)</span><span class="sxs-lookup"><span data-stu-id="99315-137">Commerce Store Starter Kit (SSK)</span></span> | <span data-ttu-id="99315-138">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-138">10.0.12</span></span> | <span data-ttu-id="99315-139">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-139">9.22</span></span> | <span data-ttu-id="99315-140">10.0.9</span><span class="sxs-lookup"><span data-stu-id="99315-140">10.0.9</span></span> | <span data-ttu-id="99315-141">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-141">9.22</span></span> |
| <span data-ttu-id="99315-142">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="99315-142">Commerce Scale Unit (self-hosted)</span></span> | <span data-ttu-id="99315-143">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-143">10.0.12</span></span> | <span data-ttu-id="99315-144">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-144">9.22</span></span> | <span data-ttu-id="99315-145">10.0.5</span><span class="sxs-lookup"><span data-stu-id="99315-145">10.0.5</span></span> | <span data-ttu-id="99315-146">9.15</span><span class="sxs-lookup"><span data-stu-id="99315-146">9.15</span></span> |
| <span data-ttu-id="99315-147">Modern POS</span><span class="sxs-lookup"><span data-stu-id="99315-147">Modern POS</span></span> | <span data-ttu-id="99315-148">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-148">10.0.12</span></span> | <span data-ttu-id="99315-149">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-149">9.22</span></span> | <span data-ttu-id="99315-150">10.0.5</span><span class="sxs-lookup"><span data-stu-id="99315-150">10.0.5</span></span> | <span data-ttu-id="99315-151">9.15</span><span class="sxs-lookup"><span data-stu-id="99315-151">9.15</span></span> |
| <span data-ttu-id="99315-152">ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="99315-152">Hardware Station</span></span> | <span data-ttu-id="99315-153">10.0.12</span><span class="sxs-lookup"><span data-stu-id="99315-153">10.0.12</span></span> | <span data-ttu-id="99315-154">9.22</span><span class="sxs-lookup"><span data-stu-id="99315-154">9.22</span></span> | <span data-ttu-id="99315-155">10.0.5</span><span class="sxs-lookup"><span data-stu-id="99315-155">10.0.5</span></span> | <span data-ttu-id="99315-156">9.15</span><span class="sxs-lookup"><span data-stu-id="99315-156">9.15</span></span> |

## <a name="one-version-requirements"></a><span data-ttu-id="99315-157">1 つのバージョン要求</span><span class="sxs-lookup"><span data-stu-id="99315-157">One Version requirements</span></span>

<span data-ttu-id="99315-158">コマース コンポーネントは、2018 年 7 月に発表された同じ [1 つのバージョン サービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)、およびその後 2019 年 6 月に発表され公開された [Finance and Operations アプリの柔軟なサービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/) も追従しています。</span><span class="sxs-lookup"><span data-stu-id="99315-158">Commerce components follow the same [One Version service updates](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/) that were announced in July 2018, and also the subsequently published [flexible service updates for Finance and Operations apps](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/) that were announced in June 2019.</span></span> <span data-ttu-id="99315-159">詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99315-159">For more information, see [One Version service updates FAQ](../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

### <a name="cloud-components"></a><span data-ttu-id="99315-160">クラウド コンポーネント</span><span class="sxs-lookup"><span data-stu-id="99315-160">Cloud components</span></span>

<span data-ttu-id="99315-161">顧客は、次のコンポーネントに対して最大で 3 回連続して更新の一時停止が可能です。</span><span class="sxs-lookup"><span data-stu-id="99315-161">Customers can pause up to three consecutive updates across the following components.</span></span> <span data-ttu-id="99315-162">(3 回の更新は、約 6 磨月に対応しています。)</span><span class="sxs-lookup"><span data-stu-id="99315-162">(Three updates correspond to approximately six calendar months.)</span></span>

- <span data-ttu-id="99315-163">コマースの本部および Finance and Operationsアプリ</span><span class="sxs-lookup"><span data-stu-id="99315-163">Commerce headquarters and Finance and Operations apps</span></span>
- <span data-ttu-id="99315-164">Commerce Scale Unit (クラウド自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="99315-164">Commerce Scale Unit (cloud-hosted)</span></span>
- <span data-ttu-id="99315-165">Commerce SDK および関連するローカル サイト コンフィギュレーション (モジュール、データア クション、テーマなど)</span><span class="sxs-lookup"><span data-stu-id="99315-165">Commerce SDK and associated local site configurations (such as modules, data actions, and themes)</span></span>

<span data-ttu-id="99315-166">たとえば、現在バージョン 10.0.2 を使用している顧客は、バージョン10.0.3、10.0.4、および 10.0.5 に対する更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="99315-166">For example, customers who are currently on version 10.0.2 can pause updates to versions 10.0.3, 10.0.4, and 10.0.5.</span></span> <span data-ttu-id="99315-167">ただし、バージョン 10.0.6 に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-167">However, they must then update to version 10.0.6.</span></span> <span data-ttu-id="99315-168">このシナリオでは、バージョン 10.0.7 が使用可能になると、バージョン 10.0.2 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="99315-168">In this scenario, after version 10.0.7 becomes available, version 10.0.2 is no longer supported.</span></span>

### <a name="in-store-components"></a><span data-ttu-id="99315-169">ストア内のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="99315-169">In-store components</span></span>

<span data-ttu-id="99315-170">顧客は、次のコンポーネントに対して最大で 7 回連続して更新の一時停止が可能です。</span><span class="sxs-lookup"><span data-stu-id="99315-170">Customers can pause up to seven consecutive updates across the following components.</span></span> <span data-ttu-id="99315-171">(7 回の更新は、約 12 磨月に対応しています。)</span><span class="sxs-lookup"><span data-stu-id="99315-171">(Seven updates correspond to approximately twelve calendar months.)</span></span>

- <span data-ttu-id="99315-172">Commerce Scale Unit (ストア内でホスト)</span><span class="sxs-lookup"><span data-stu-id="99315-172">Commerce Scale Unit (in-store hosted)</span></span>
- <span data-ttu-id="99315-173">Modern POS</span><span class="sxs-lookup"><span data-stu-id="99315-173">Modern POS</span></span>
- <span data-ttu-id="99315-174">ハードウェア ステーション</span><span class="sxs-lookup"><span data-stu-id="99315-174">Hardware Station</span></span>

<span data-ttu-id="99315-175">たとえば、現在バージョン 10.0.2 を使用している顧客は、バージョン10.0.3 から 10.0.9 に対する更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="99315-175">For example, customers who are currently on version 10.0.2 can pause updates to versions 10.0.3 through 10.0.9.</span></span> <span data-ttu-id="99315-176">ただし、バージョン 10.0.10 に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99315-176">However, they must then update to version 10.0.10.</span></span> <span data-ttu-id="99315-177">このシナリオでは、バージョン 10.0.11 が使用可能になると、バージョン 10.0.2 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="99315-177">In this scenario, after version 10.0.11 becomes available, version 10.0.2 is no longer supported.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99315-178">追加リソース</span><span class="sxs-lookup"><span data-stu-id="99315-178">Additional resources</span></span>

### <a name="one-version-service-updates"></a><span data-ttu-id="99315-179">One Version のサービス更新</span><span class="sxs-lookup"><span data-stu-id="99315-179">One Version service updates</span></span>

<span data-ttu-id="99315-180">1 つのバージョン サービスの更新詳細は、次のリソースをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="99315-180">For more information about One Version service updates, see the following resources:</span></span>

- [<span data-ttu-id="99315-181">1 つのバージョンのサービス更新に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="99315-181">One Version service updates FAQ</span></span>](../fin-ops-core/fin-ops/get-started/one-version.md)
- [<span data-ttu-id="99315-182">Dynamics 365 の更新方法を近代化</span><span class="sxs-lookup"><span data-stu-id="99315-182">Modernizing the way we update Dynamics 365</span></span>](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)
- [<span data-ttu-id="99315-183">Finance and Operations アプリの新しい柔軟なサービスを更新</span><span class="sxs-lookup"><span data-stu-id="99315-183">New flexible service updates for Finance and Operations apps</span></span>](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/)

### <a name="component-selection"></a><span data-ttu-id="99315-184">コンポーネントの選択</span><span class="sxs-lookup"><span data-stu-id="99315-184">Component selection</span></span>

<span data-ttu-id="99315-185">ニーズに合った適切なコンポーネントを選択する方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="99315-185">For more information about how to select the correct components to meet your needs, see the following topics:</span></span>

- [<span data-ttu-id="99315-186">ストア内トポロジの選択</span><span class="sxs-lookup"><span data-stu-id="99315-186">Select an in-store topology</span></span>](./dev-itpro/retail-in-store-topology.md)
- [<span data-ttu-id="99315-187">Modern POS (MPOS) か Cloud POS (CPOS) かの選択</span><span class="sxs-lookup"><span data-stu-id="99315-187">Choose between Modern POS (MPOS) and Cloud POS (CPOS)</span></span>](mpos-or-cpos.md)

### <a name="servicing-instructions"></a><span data-ttu-id="99315-188">サービスの手順</span><span class="sxs-lookup"><span data-stu-id="99315-188">Servicing instructions</span></span>

<span data-ttu-id="99315-189">このトピックで説明されている個々のコンポーネントをサービスする方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="99315-189">For more information about how to service individual components that are described in this topic, see the following topics:</span></span>

- [<span data-ttu-id="99315-190">Commerce Scale Unit のコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="99315-190">Configure and install Commerce Scale Unit</span></span>](./dev-itpro/retail-store-scale-unit-configuration-installation.md)
- [<span data-ttu-id="99315-191">更新プログラムの適用および Retail Cloud Scale Unit への拡張機能</span><span class="sxs-lookup"><span data-stu-id="99315-191">Apply updates and extensions to Retail Cloud Scale Unit</span></span>](../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)
- [<span data-ttu-id="99315-192">Modern POS (MPOS) のコンフィギュレーション、インストール、および有効にする</span><span class="sxs-lookup"><span data-stu-id="99315-192">Configure, install, and active Modern POS (MPOS)</span></span>](retail-modern-pos-device-activation.md)
- [<span data-ttu-id="99315-193">Retail Hardware Station のコンフィギュレーションおよびインストール</span><span class="sxs-lookup"><span data-stu-id="99315-193">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md)
- [<span data-ttu-id="99315-194">パッケージ コンフィギュレーションとオンライン チャネルへの配置</span><span class="sxs-lookup"><span data-stu-id="99315-194">Package configurations and deploy them to an online channel</span></span>](./e-commerce-extensibility/package-deploy.md)

### <a name="extensibility-and-packing"></a><span data-ttu-id="99315-195">拡張性および梱包</span><span class="sxs-lookup"><span data-stu-id="99315-195">Extensibility and packing</span></span>

<span data-ttu-id="99315-196">拡張機能の保守機能については、[配置可能なパッケージの作成](./dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99315-196">For more information about serviceability for extensions, see [Create deployable packages](./dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>
