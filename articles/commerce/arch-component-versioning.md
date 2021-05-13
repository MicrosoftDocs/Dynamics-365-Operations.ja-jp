---
title: Dynamics 365 Commerceコンポーネント バージョンの管理要件
description: このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。
author: rezaassadi
ms.date: 04/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailITWorkspace
audience: Developer, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 6e9f81ec574b80ab60d4a643e6bee54ee672de74
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936958"
---
# <a name="dynamics-365-commerce-component-versioning-requirements"></a><span data-ttu-id="60f3d-103">Dynamics 365 Commerceコンポーネント バージョンの管理要件</span><span class="sxs-lookup"><span data-stu-id="60f3d-103">Dynamics 365 Commerce component versioning requirements</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="60f3d-104">このトピックでは、Microsoft Dynamics 365 Commerce エコシステムのすべてのコンポーネントに対する、コンポーネント バージョン要件および依存関係の概要について説明します。</span><span class="sxs-lookup"><span data-stu-id="60f3d-104">This topic provides an overview of the component versioning requirements and dependencies for all components in the Microsoft Dynamics 365 Commerce ecosystem.</span></span>

<span data-ttu-id="60f3d-105">次の図は、Dynamics 365 Commerce コンポーネントの概要、それに対応するバージョン要件および依存関係を示しています。</span><span class="sxs-lookup"><span data-stu-id="60f3d-105">The following illustration shows an overview of Dynamics 365 Commerce components and corresponding versioning requirements and dependencies.</span></span>

<span data-ttu-id="60f3d-106"><a href="/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce コンポーネント バージョン要件および依存関係](./media/commerce-component-versioning.jpg)</a></span><span class="sxs-lookup"><span data-stu-id="60f3d-106"><a href="/dynamics365/commerce/media/commerce-component-versioning.jpg" target="_blank">![Dynamics 365 Commerce Component versioning requirements and dependencies](./media/commerce-component-versioning.jpg)</a></span></span>

## <a name="component-dependencies"></a><span data-ttu-id="60f3d-107">コンポーネントの依存関係</span><span class="sxs-lookup"><span data-stu-id="60f3d-107">Component dependencies</span></span>

### <a name="service-updates"></a><span data-ttu-id="60f3d-108">サービスの更新</span><span class="sxs-lookup"><span data-stu-id="60f3d-108">Service updates</span></span>

<span data-ttu-id="60f3d-109">顧客およびパートナーがサービスおよび配置を行うすべてのコマース コンポーネントとの互換性を確保するには、更新サービス中にいくつかのバージョン依存関係に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-109">To ensure compatibility between all Commerce components that are serviced and deployed by customers and partners, you must follow several versioning dependencies during servicing updates.</span></span> <span data-ttu-id="60f3d-110">次のリストは、これらの依存関係をすべて示しています。</span><span class="sxs-lookup"><span data-stu-id="60f3d-110">The following list describes all these dependencies.</span></span>

- <span data-ttu-id="60f3d-111">**コマースの本部と Finance and Operations アプリは、Commerce Scale Unit (クラウドと自己ホスト型の両方) と同じバージョンか、それよりも新しいバージョンになっている必要があります。**</span><span class="sxs-lookup"><span data-stu-id="60f3d-111">**Commerce headquarters and Finance and Operations apps must be on the same version as, or a newer version than, Commerce Scale Unit (both cloud and self-hosted).**</span></span>

    <span data-ttu-id="60f3d-112">たとえば、Commerce 本社および Finance and Operations アプリがバージョン 10.0.18 である場合、Commerce Scale Unit はバージョン 10.0.18 またはそれ以前 (たとえば、10.0.17 または 10.0.16) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-112">For example, if Commerce headquarters and Finance and Operations apps are on version 10.0.18, Commerce Scale Unit must be on version 10.0.18 or earlier (for example, 10.0.17 or 10.0.16).</span></span>

- <span data-ttu-id="60f3d-113">**Commerce Scale Unit は、Modern Point of Sale (POS)、Hardware Station、コマース ソフトウェア キット (SDK) と同じバージョンかそれより新しいバージョン、および関連するローカル サイト コンフィギュレーション (モジュール、データ アクション、テーマなど) でなくてはなりません。**</span><span class="sxs-lookup"><span data-stu-id="60f3d-113">**Commerce Scale Unit must be on the same version as, or a newer version than, Modern Point of Sale (POS), Hardware Station, and the Commerce software development kit (SDK) and associated local site configurations (such as modules, data actions, and themes).**</span></span>

    <span data-ttu-id="60f3d-114">たとえば、Commerce Scale Unit がバージョン 10.0.18 である場合、Modern POS、Hardware Station、およびコマース ストアフロントはバージョン 10.0.18 またはそれ以前 (たとえば、10.0.17 または 10.0.16) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-114">For example, if Commerce Scale Unit is on version 10.0.18, Modern POS, Hardware Station, and the Commerce storefront must be on version 10.0.18 or earlier (for example, 10.0.17 or 10.0.16).</span></span>

- <span data-ttu-id="60f3d-115">**拡張機能パッケージは、拡張機能が適用されるターゲット コンポーネントと同じバージョン、またはそれより新しいバージョンに対してコンパイルする必要があります。**</span><span class="sxs-lookup"><span data-stu-id="60f3d-115">**Extension packages must be compiled against the same version as, or a newer version than, the target component that the extension applies to.**</span></span>

    <span data-ttu-id="60f3d-116">たとえば、展開された Commerce Scale Unit がバージョン 10.0.18 である場合、対応する拡張パッケージをバージョン 10.0.18 またはそれ以前 (たとえば、10.0.17 または 10.0.16) に対してコンパイルする必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-116">For example, if the deployed Commerce Scale Unit is on version 10.0.18, the corresponding extension packages must be compiled against version 10.0.18 or earlier (for example, 10.0.17 or 10.0.16).</span></span>

### <a name="quality-updates"></a><span data-ttu-id="60f3d-117">品質更新プログラム</span><span class="sxs-lookup"><span data-stu-id="60f3d-117">Quality updates</span></span>

<span data-ttu-id="60f3d-118">品質更新プログラム中、サービス更新プログラムに必要なもの以外に、各コマース コンポーネントに対して特定のバージョン管理要件に従う必要はありません。</span><span class="sxs-lookup"><span data-stu-id="60f3d-118">During quality updates, no specific versioning requirements must be followed for each Commerce component, besides what is required for service updates.</span></span>

## <a name="current-supported-versions"></a><span data-ttu-id="60f3d-119">現在サポートされているバージョン</span><span class="sxs-lookup"><span data-stu-id="60f3d-119">Current supported versions</span></span>

<span data-ttu-id="60f3d-120">次の表では、**2021 年 4 月 16 日** 時点での各種コマース コンポーネントの現在のサポートされているバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="60f3d-120">The following table describes the current supported versions of various Commerce components as of **April 16, 2021**.</span></span>

| <span data-ttu-id="60f3d-121">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="60f3d-121">Component</span></span> | <span data-ttu-id="60f3d-122">利用可能な最新リリース (サンドボックス内の最初のリリース)</span><span class="sxs-lookup"><span data-stu-id="60f3d-122">Latest available release (first release available in Sandbox)</span></span> | <span data-ttu-id="60f3d-123">利用可能な最新のコンポーネント バージョン番号 (サンドボックス内の最初のリリース)</span><span class="sxs-lookup"><span data-stu-id="60f3d-123">Latest available component version number (first release available in Sandbox)</span></span> | <span data-ttu-id="60f3d-124">サポートされている最も古いリリース</span><span class="sxs-lookup"><span data-stu-id="60f3d-124">Earliest supported release</span></span> | <span data-ttu-id="60f3d-125">サポートされている最も古いコンポーネントのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="60f3d-125">Earliest supported component version number</span></span> |
|---|---|---|---|---|
| <span data-ttu-id="60f3d-126">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="60f3d-126">Finance and Operations apps</span></span> | <span data-ttu-id="60f3d-127">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-127">10.0.18</span></span> | <span data-ttu-id="60f3d-128">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-128">10.0.18</span></span> | <span data-ttu-id="60f3d-129">10.0.14</span><span class="sxs-lookup"><span data-stu-id="60f3d-129">10.0.14</span></span> | <span data-ttu-id="60f3d-130">10.0.14</span><span class="sxs-lookup"><span data-stu-id="60f3d-130">10.0.14</span></span> |
| <span data-ttu-id="60f3d-131">Commerce Scale Unit (クラウド自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="60f3d-131">Commerce Scale Unit (cloud-hosted)</span></span> | <span data-ttu-id="60f3d-132">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-132">10.0.18</span></span> | <span data-ttu-id="60f3d-133">9.28</span><span class="sxs-lookup"><span data-stu-id="60f3d-133">9.28</span></span> | <span data-ttu-id="60f3d-134">10.0.14</span><span class="sxs-lookup"><span data-stu-id="60f3d-134">10.0.14</span></span> | <span data-ttu-id="60f3d-135">9.24</span><span class="sxs-lookup"><span data-stu-id="60f3d-135">9.24</span></span> |
| <span data-ttu-id="60f3d-136">Commerce モジュール ライブラリ</span><span class="sxs-lookup"><span data-stu-id="60f3d-136">Commerce module library</span></span> | <span data-ttu-id="60f3d-137">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-137">10.0.18</span></span> | <span data-ttu-id="60f3d-138">9.28</span><span class="sxs-lookup"><span data-stu-id="60f3d-138">9.28</span></span> | <span data-ttu-id="60f3d-139">10.0.14</span><span class="sxs-lookup"><span data-stu-id="60f3d-139">10.0.14</span></span> | <span data-ttu-id="60f3d-140">9.24</span><span class="sxs-lookup"><span data-stu-id="60f3d-140">9.24</span></span> |
| <span data-ttu-id="60f3d-141">Commerce Scale Unit (自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="60f3d-141">Commerce Scale Unit (self-hosted)</span></span> | <span data-ttu-id="60f3d-142">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-142">10.0.18</span></span> | <span data-ttu-id="60f3d-143">9.28</span><span class="sxs-lookup"><span data-stu-id="60f3d-143">9.28</span></span> | <span data-ttu-id="60f3d-144">10.0.10</span><span class="sxs-lookup"><span data-stu-id="60f3d-144">10.0.10</span></span> | <span data-ttu-id="60f3d-145">9.20</span><span class="sxs-lookup"><span data-stu-id="60f3d-145">9.20</span></span> |
| <span data-ttu-id="60f3d-146">Modern POS</span><span class="sxs-lookup"><span data-stu-id="60f3d-146">Modern POS</span></span> | <span data-ttu-id="60f3d-147">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-147">10.0.18</span></span> | <span data-ttu-id="60f3d-148">9.28</span><span class="sxs-lookup"><span data-stu-id="60f3d-148">9.28</span></span> | <span data-ttu-id="60f3d-149">10.0.10</span><span class="sxs-lookup"><span data-stu-id="60f3d-149">10.0.10</span></span> | <span data-ttu-id="60f3d-150">9.20</span><span class="sxs-lookup"><span data-stu-id="60f3d-150">9.20</span></span> |
| <span data-ttu-id="60f3d-151">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="60f3d-151">Hardware Station</span></span> | <span data-ttu-id="60f3d-152">10.0.18</span><span class="sxs-lookup"><span data-stu-id="60f3d-152">10.0.18</span></span> | <span data-ttu-id="60f3d-153">9.28</span><span class="sxs-lookup"><span data-stu-id="60f3d-153">9.28</span></span> | <span data-ttu-id="60f3d-154">10.0.10</span><span class="sxs-lookup"><span data-stu-id="60f3d-154">10.0.10</span></span> | <span data-ttu-id="60f3d-155">9.20</span><span class="sxs-lookup"><span data-stu-id="60f3d-155">9.20</span></span> |

## <a name="one-version-requirements"></a><span data-ttu-id="60f3d-156">1 つのバージョン要求</span><span class="sxs-lookup"><span data-stu-id="60f3d-156">One Version requirements</span></span>

<span data-ttu-id="60f3d-157">コマース コンポーネントは、2018 年 7 月に発表された同じ [1 つのバージョン サービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)、およびその後 2019 年 6 月に発表され公開された [Finance and Operations アプリの柔軟なサービスの更新プログラム](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/) も追従しています。</span><span class="sxs-lookup"><span data-stu-id="60f3d-157">Commerce components follow the same [One Version service updates](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/) that were announced in July 2018, and also the subsequently published [flexible service updates for Finance and Operations apps](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/) that were announced in June 2019.</span></span> <span data-ttu-id="60f3d-158">詳細については、[1 つのバージョン サービスに関してよく寄せられる質問](../fin-ops-core/fin-ops/get-started/one-version.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60f3d-158">For more information, see [One Version service updates FAQ](../fin-ops-core/fin-ops/get-started/one-version.md).</span></span>

### <a name="cloud-components"></a><span data-ttu-id="60f3d-159">クラウド コンポーネント</span><span class="sxs-lookup"><span data-stu-id="60f3d-159">Cloud components</span></span>

<span data-ttu-id="60f3d-160">顧客は、次のコンポーネントに対して最大で 3 回連続して更新の一時停止が可能です。</span><span class="sxs-lookup"><span data-stu-id="60f3d-160">Customers can pause up to three consecutive updates across the following components.</span></span> <span data-ttu-id="60f3d-161">(3 回の更新は、約 6 磨月に対応しています。)</span><span class="sxs-lookup"><span data-stu-id="60f3d-161">(Three updates correspond to approximately six calendar months.)</span></span>

- <span data-ttu-id="60f3d-162">コマースの本部および Finance and Operationsアプリ</span><span class="sxs-lookup"><span data-stu-id="60f3d-162">Commerce headquarters and Finance and Operations apps</span></span>
- <span data-ttu-id="60f3d-163">Commerce Scale Unit (クラウド自己ホスト)</span><span class="sxs-lookup"><span data-stu-id="60f3d-163">Commerce Scale Unit (cloud-hosted)</span></span>
- <span data-ttu-id="60f3d-164">Commerce SDK および関連するローカル サイト コンフィギュレーション (モジュール、データア クション、テーマなど)</span><span class="sxs-lookup"><span data-stu-id="60f3d-164">Commerce SDK and associated local site configurations (such as modules, data actions, and themes)</span></span>

<span data-ttu-id="60f3d-165">たとえば、現在バージョン 10.0.15 を使用している顧客は、バージョン10.0.16、10.0.17、および 10.0.18 に対する更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="60f3d-165">For example, customers who are currently on version 10.0.15 can pause updates to versions 10.0.16, 10.0.17, and 10.0.18.</span></span> <span data-ttu-id="60f3d-166">ただし、バージョン 10.0.19 に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-166">However, they must then update to version 10.0.19.</span></span> <span data-ttu-id="60f3d-167">このシナリオでは、バージョン 10.0.20 が使用可能になると、バージョン 10.0.15 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-167">In this scenario, after version 10.0.20 becomes available, version 10.0.15 is no longer supported.</span></span>

### <a name="in-store-components"></a><span data-ttu-id="60f3d-168">ストア内のコンポーネント</span><span class="sxs-lookup"><span data-stu-id="60f3d-168">In-store components</span></span>

<span data-ttu-id="60f3d-169">顧客は、次のコンポーネントに対して最大で 7 回連続して更新の一時停止が可能です。</span><span class="sxs-lookup"><span data-stu-id="60f3d-169">Customers can pause up to seven consecutive updates across the following components.</span></span> <span data-ttu-id="60f3d-170">(7 回の更新は、約 12 磨月に対応しています。)</span><span class="sxs-lookup"><span data-stu-id="60f3d-170">(Seven updates correspond to approximately twelve calendar months.)</span></span>

- <span data-ttu-id="60f3d-171">Commerce Scale Unit (ストア内でホスト)</span><span class="sxs-lookup"><span data-stu-id="60f3d-171">Commerce Scale Unit (in-store hosted)</span></span>
- <span data-ttu-id="60f3d-172">Modern POS</span><span class="sxs-lookup"><span data-stu-id="60f3d-172">Modern POS</span></span>
- <span data-ttu-id="60f3d-173">Hardware Station</span><span class="sxs-lookup"><span data-stu-id="60f3d-173">Hardware Station</span></span>

<span data-ttu-id="60f3d-174">たとえば、現在バージョン 10.0.15 を使用している顧客は、バージョン10.0.6、10.0.17、および 10.0.18 に対する更新を一時停止できます。</span><span class="sxs-lookup"><span data-stu-id="60f3d-174">For example, customers who are currently on version 10.0.15 can pause updates to versions 10.0.6, 10.0.17, and 10.0.18.</span></span> <span data-ttu-id="60f3d-175">ただし、バージョン 10.0.19 に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-175">However, they must then update to version 10.0.19.</span></span> <span data-ttu-id="60f3d-176">このシナリオでは、バージョン 10.0.120 が使用可能になると、バージョン 10.0.15 はサポートされなくなります。</span><span class="sxs-lookup"><span data-stu-id="60f3d-176">In this scenario, after version 10.0.120 becomes available, version 10.0.15 is no longer supported.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60f3d-177">追加リソース</span><span class="sxs-lookup"><span data-stu-id="60f3d-177">Additional resources</span></span>

### <a name="one-version-service-updates"></a><span data-ttu-id="60f3d-178">One Version のサービス更新</span><span class="sxs-lookup"><span data-stu-id="60f3d-178">One Version service updates</span></span>

<span data-ttu-id="60f3d-179">1 つのバージョン サービスの更新詳細は、次のリソースをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="60f3d-179">For more information about One Version service updates, see the following resources:</span></span>

- [<span data-ttu-id="60f3d-180">1 つのバージョンのサービス更新に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="60f3d-180">One Version service updates FAQ</span></span>](../fin-ops-core/fin-ops/get-started/one-version.md)
- [<span data-ttu-id="60f3d-181">Dynamics 365 の更新方法を近代化</span><span class="sxs-lookup"><span data-stu-id="60f3d-181">Modernizing the way we update Dynamics 365</span></span>](https://cloudblogs.microsoft.com/dynamics365/bdm/2018/07/06/modernizing-the-way-we-update-dynamics-365/)
- [<span data-ttu-id="60f3d-182">Finance and Operations アプリの新しい柔軟なサービスを更新</span><span class="sxs-lookup"><span data-stu-id="60f3d-182">New flexible service updates for Finance and Operations apps</span></span>](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/06/03/new-flexible-service-updates-for-dynamics-365-for-finance-and-operations/)

### <a name="component-selection"></a><span data-ttu-id="60f3d-183">コンポーネントの選択</span><span class="sxs-lookup"><span data-stu-id="60f3d-183">Component selection</span></span>

<span data-ttu-id="60f3d-184">ニーズに合った適切なコンポーネントを選択する方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="60f3d-184">For more information about how to select the correct components to meet your needs, see the following topics:</span></span>

- [<span data-ttu-id="60f3d-185">ストア内トポロジの選択</span><span class="sxs-lookup"><span data-stu-id="60f3d-185">Select an in-store topology</span></span>](./dev-itpro/retail-in-store-topology.md)
- [<span data-ttu-id="60f3d-186">Modern POS (MPOS) か Cloud POS (CPOS) かの選択</span><span class="sxs-lookup"><span data-stu-id="60f3d-186">Choose between Modern POS (MPOS) and Cloud POS (CPOS)</span></span>](mpos-or-cpos.md)

### <a name="servicing-instructions"></a><span data-ttu-id="60f3d-187">サービスの手順</span><span class="sxs-lookup"><span data-stu-id="60f3d-187">Servicing instructions</span></span>

<span data-ttu-id="60f3d-188">このトピックで説明されている個々のコンポーネントをサービスする方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="60f3d-188">For more information about how to service individual components that are described in this topic, see the following topics:</span></span>

- [<span data-ttu-id="60f3d-189">Commerce Scale Unit のコンフィギュレーションとインストール</span><span class="sxs-lookup"><span data-stu-id="60f3d-189">Configure and install Commerce Scale Unit</span></span>](./dev-itpro/retail-store-scale-unit-configuration-installation.md)
- [<span data-ttu-id="60f3d-190">更新プログラムの適用および Retail Cloud Scale Unit への拡張機能</span><span class="sxs-lookup"><span data-stu-id="60f3d-190">Apply updates and extensions to Retail Cloud Scale Unit</span></span>](../fin-ops-core/dev-itpro/deployment/update-retail-channel.md)
- [<span data-ttu-id="60f3d-191">Modern POS (MPOS) のコンフィギュレーション、インストール、および有効にする</span><span class="sxs-lookup"><span data-stu-id="60f3d-191">Configure, install, and active Modern POS (MPOS)</span></span>](retail-modern-pos-device-activation.md)
- [<span data-ttu-id="60f3d-192">Retail Hardware Station のコンフィギュレーションおよびインストール</span><span class="sxs-lookup"><span data-stu-id="60f3d-192">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md)
- [<span data-ttu-id="60f3d-193">パッケージ コンフィギュレーションとオンライン チャネルへの配置</span><span class="sxs-lookup"><span data-stu-id="60f3d-193">Package configurations and deploy them to an online channel</span></span>](./e-commerce-extensibility/package-deploy.md)

### <a name="extensibility-and-packing"></a><span data-ttu-id="60f3d-194">拡張性および梱包</span><span class="sxs-lookup"><span data-stu-id="60f3d-194">Extensibility and packing</span></span>

<span data-ttu-id="60f3d-195">拡張機能の保守機能については、[配置可能なパッケージの作成](./dev-itpro/retail-sdk/retail-sdk-packaging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60f3d-195">For more information about serviceability for extensions, see [Create deployable packages](./dev-itpro/retail-sdk/retail-sdk-packaging.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]