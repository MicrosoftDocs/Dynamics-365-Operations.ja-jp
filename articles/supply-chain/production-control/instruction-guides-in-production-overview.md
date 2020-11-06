---
title: 生産での作業者への Mixed-reality ガイドの提供
description: このトピックでは、Dynamics 365 Guides を使用した Microsoft Dynamics 365 Supply Chain Management での生産管理モジュールを統合する方法について説明します。
author: cabeln
manager: tfehr
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkGuidesManufacturing
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 61943
ms.assetid: a3847f07-fca4-4140-a26f-d83c6ac68dde
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: cabeln
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 14645f592275d07a6b633146bb6da35b89c1bf77
ms.sourcegitcommit: 6d2fc497c8a7f49c48e7662995e27b5f8cc10296
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000981"
---
# <a name="provide-mixed-reality-guides-for-workers-in-production"></a><span data-ttu-id="b3f74-103">生産での作業者への Mixed-reality ガイドの提供</span><span class="sxs-lookup"><span data-stu-id="b3f74-103">Provide mixed-reality Guides for workers in production</span></span>

<span data-ttu-id="b3f74-104">生産プロセスの作業者は、作業の流れの中で適切な時に提供される関連する指示は大きな助けになります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-104">Workers in production processes will benefit from relevant instructions that are provided at the right time in the context of their work.</span></span> <span data-ttu-id="b3f74-105">*手順* は、組み立て、サービス、行程、認定、および安全など、複数の作業ドメインで適用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-105">*Instructions* apply in several domains of work, including: assembly, service, operations, certification, and safety.</span></span> <span data-ttu-id="b3f74-106">これらのコアビジネス機能には、継続的なトレーニング手順が用意されており、作業者が労働力を向上させることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-106">Across all of these core business functions, ongoing training instructions can help empower workers to achieve more and work better.</span></span>

## <a name="introduction"></a><span data-ttu-id="b3f74-107">はじめに</span><span class="sxs-lookup"><span data-stu-id="b3f74-107">Introduction</span></span>

<span data-ttu-id="b3f74-108">手順は、さまざまな方法で提供できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-108">You can provide instructions in different ways.</span></span> <span data-ttu-id="b3f74-109">すぐに利用できる効率的なシステムの 1 つは、[Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/) を使用します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-109">One efficient system that ships out of the box uses [Dynamics 365 Guides](https://dynamics.microsoft.com/mixed-reality/guides/).</span></span>

<span data-ttu-id="b3f74-110">Dynamics 365 Guides は、実践的な学習によって従業員を支援することができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-110">Dynamics 365 Guides can help empower your employees with hands-on learning.</span></span> <span data-ttu-id="b3f74-111">ステップ バイ ステップの標準化されたプロセスを定義して、必要なツールや部品を従業員に紹介し、そのツールを実際の作業状況で使用する方法を示すことができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-111">You can define standardized processes with step-by-step instructions that guide your employees to the tools and parts they need and show employees how to use these tools in real work situations.</span></span>

<span data-ttu-id="b3f74-112">次のように、生産管理のさまざまな側面にガイドを付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-112">You can attach guides to various aspects of production control including:</span></span>

- [<span data-ttu-id="b3f74-113">リソース</span><span class="sxs-lookup"><span data-stu-id="b3f74-113">Resources</span></span>](#resources)
- [<span data-ttu-id="b3f74-114">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="b3f74-114">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="b3f74-115">リリースされた製品</span><span class="sxs-lookup"><span data-stu-id="b3f74-115">Released products</span></span>](#released-products)
- [<span data-ttu-id="b3f74-116">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="b3f74-116">Formulas</span></span>](#formulas)
- [<span data-ttu-id="b3f74-117">フォーミュラ バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-117">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="b3f74-118">部品表 (BOM)</span><span class="sxs-lookup"><span data-stu-id="b3f74-118">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="b3f74-119">BOM バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-119">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="b3f74-120">工順</span><span class="sxs-lookup"><span data-stu-id="b3f74-120">Routes</span></span>](#routes)
- [<span data-ttu-id="b3f74-121">工順バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-121">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="b3f74-122">工順工程関連</span><span class="sxs-lookup"><span data-stu-id="b3f74-122">Route operation relations</span></span>](#route-operation-relations)

> [!NOTE]
> <span data-ttu-id="b3f74-123">また、資産管理でガイドを関連付けることもできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-123">You can also attach Guides with Asset Management.</span></span> <span data-ttu-id="b3f74-124">このオプションの詳細については、[Dynamics 365 Guides を使用した Dynamics 365 Supply Chain Management (資産管理) の統合](../asset-management/asset-management-guides-integration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b3f74-124">For more information about that option, see [Integrate Dynamics 365 Supply Chain Management (Asset Management) with Dynamics 365 Guides](../asset-management/asset-management-guides-integration.md).</span></span>

<span data-ttu-id="b3f74-125">最前線で働く作業者が Supply Chain Management を通じて作業現場の職務を選択すると、作業者はジョブカードで[関連するガイド](#logic) を参照できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-125">When a first-line worker chooses a job on the shop floor through Supply Chain Management, the worker can see [the relevant guides](#logic) on the job card.</span></span> <span data-ttu-id="b3f74-126">作業者が特定のガイドを選択すると、このガイドの QR コードが画面に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-126">When the worker chooses a specific guide, a QR code for that guide is shown on the screen.</span></span> <span data-ttu-id="b3f74-127">作業者は、HoloLens を使用して QR コードをスキャンします。そうすると、ガイドが起動し必要な手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-127">The worker then uses their HoloLens to scan the QR code, which launches Guides and shows the required instructions.</span></span>

<span data-ttu-id="b3f74-128">次のサブセクションでは、ガイドを使用して製造に関する手順を表示する場合に、業界全体の企業が最大の価値を見出すことができるいくつかのシナリオについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-128">The following subsections describe a few selected scenarios where companies across industries can see the biggest value when using Guides to present instructions for manufacturing.</span></span>

### <a name="assembly"></a><span data-ttu-id="b3f74-129">組み立て</span><span class="sxs-lookup"><span data-stu-id="b3f74-129">Assembly</span></span>

<span data-ttu-id="b3f74-130">![アセンブリ タスクのガイドの使用](media/instruction-guides-hero-assembly.png "サービス タスクのガイドの使用")</span><span class="sxs-lookup"><span data-stu-id="b3f74-130">![Use Guides in assembly tasks](media/instruction-guides-hero-assembly.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="b3f74-131">組み立て操作の手順では、作業者が必要なツールとパーツ、および実際の作業状況での使用方法が示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-131">Instructions in assembly operations show workers the tools and parts they need and how to use them in real work situations.</span></span>

<span data-ttu-id="b3f74-132">生産管理者は、たとえば、[生産工順](routes-operations.md)、[関連工程](routes-operations.md#operation-relations)、[部品表](bill-of-material-bom.md)などのガイドを作成し、割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-132">Production managers can create and assign Guides, for example, for [production routes](routes-operations.md), [operation relations](routes-operations.md#operation-relations), or [bills of material](bill-of-material-bom.md).</span></span> <span data-ttu-id="b3f74-133">作業者には、作業現場でそれぞれの工程経験に関連する手順が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-133">Workers will find the relevant instructions on the respective operation experience on the shop floor.</span></span>

### <a name="service"></a><span data-ttu-id="b3f74-134">サービス</span><span class="sxs-lookup"><span data-stu-id="b3f74-134">Service</span></span>

<span data-ttu-id="b3f74-135">![サービス タスクのガイドの使用](media/instruction-guides-hero-service.png "サービス タスクのガイドの使用")</span><span class="sxs-lookup"><span data-stu-id="b3f74-135">![Use Guides in service tasks](media/instruction-guides-hero-service.png "Use Guides in service tasks")</span></span>

<span data-ttu-id="b3f74-136">技術者には、現場でのガイド付き指示事項が提供されるため、追加の訪問をスケジュールする必要がありません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-136">Equip technicians with guided instructions at the job site, eliminating the need to schedule additional visits.</span></span>

<span data-ttu-id="b3f74-137">サービス マネージャーは、たとえば品質評価のルーチンを説明する特定の[製品](../../commerce/product.md)にガイドを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-137">Service managers can assign Guides, for example, to specific [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="quality"></a><span data-ttu-id="b3f74-138">品質</span><span class="sxs-lookup"><span data-stu-id="b3f74-138">Quality</span></span>

<span data-ttu-id="b3f74-139">![品質保証タスクでのガイドの使用](media/instruction-guides-hero-quality.png "品質保証タスクのガイドの使用")</span><span class="sxs-lookup"><span data-stu-id="b3f74-139">![Use Guides in quality assurance tasks](media/instruction-guides-hero-quality.png "Use Guides in quality assurance tasks")</span></span>

<span data-ttu-id="b3f74-140">従業員の知識を反復可能なツールに変えることにより、新しいプロセスをロールアウトし、一貫性を高めることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-140">Rollout new processes and ensure increased consistency by turning employee knowledge into a repeatable tool.</span></span>

<span data-ttu-id="b3f74-141">品質保証マネージャーは、たとえば品質評価のルーチンを説明する[製品](../../commerce/product.md)にガイドを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-141">Quality assurance managers can assign guides, for example, to [products](../../commerce/product.md) that walk through routines of quality assessment.</span></span>

### <a name="certifications"></a><span data-ttu-id="b3f74-142">証明書</span><span class="sxs-lookup"><span data-stu-id="b3f74-142">Certifications</span></span>

<span data-ttu-id="b3f74-143">![認定に関連したタスクのガイドを使用](media/instruction-guides-hero-certification.png "認定に関連したタスクのガイドの使用")</span><span class="sxs-lookup"><span data-stu-id="b3f74-143">![Use Guides for certification related tasks](media/instruction-guides-hero-certification.png "Use Guides for certification related tasks")</span></span>

<span data-ttu-id="b3f74-144">支援を必要とする人物をすばやく特定して、すべての従業員が高い基準を満たすようにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-144">Ensure every employee meets high standards by quickly identifying who needs help and where.</span></span>

### <a name="safety"></a><span data-ttu-id="b3f74-145">安全</span><span class="sxs-lookup"><span data-stu-id="b3f74-145">Safety</span></span>

<span data-ttu-id="b3f74-146">![作業安全手順のガイドの使用](media/instruction-guides-hero-safety.png "作業安全手順のガイドの使用")</span><span class="sxs-lookup"><span data-stu-id="b3f74-146">![Use Guides in work safety instructions](media/instruction-guides-hero-safety.png "Use Guides in work safety instructions")</span></span>

<span data-ttu-id="b3f74-147">物理環境で試みる前に、危険な手順を仮想的に実行する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-147">Provide instructions that walk through dangerous procedures virtually before attempting in the physical environment.</span></span> <span data-ttu-id="b3f74-148">Mixed reality アプローチでは、作業者が危険な手順を仮想的に経験できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-148">With a mixed reality approach, workers can experience dangerous procedures virtually.</span></span>

<span data-ttu-id="b3f74-149">生産管理者は、[製品品目](../../commerce/product.md)、[工順](routes-operations.md)、および[工程](routes-operations.md#operation-relations)に手順を割り当てることにより、有害な材料取り扱いまたは繊細な処理手順に関する専用の手順を提供できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-149">Production managers can provide dedicated handling instructions for hazardous material handling or delicate handling procedures by assigning instructions to [product items](../../commerce/product.md), [routes](routes-operations.md), and [operations](routes-operations.md#operation-relations).</span></span>

## <a name="get-started-with-instructions-and-guides"></a><span data-ttu-id="b3f74-150">手順とガイドの使用開始</span><span class="sxs-lookup"><span data-stu-id="b3f74-150">Get started with instructions and Guides</span></span>

<span data-ttu-id="b3f74-151">生産プロセスで手順を有効にするために、Supply Chain Management には、Dynamics 365 Guides にすぐ使用できる統合機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="b3f74-151">To enable instructions in production processes, Supply Chain Management provides an out-of-the-box integration with Dynamics 365 Guides.</span></span> <span data-ttu-id="b3f74-152">Guides のライセンスおよびインストールされたアプリケーション インスタンスは、生産資産と作業に Mixed Reality の手順を作成、管理、および割り当てるために必要です。</span><span class="sxs-lookup"><span data-stu-id="b3f74-152">A licensed and installed application instance of Guides is required to build, maintain, and assign mixed reality instructions to production assets and work.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="b3f74-153">必要条件</span><span class="sxs-lookup"><span data-stu-id="b3f74-153">Prerequisites</span></span>

<span data-ttu-id="b3f74-154">この機能を使用するには、システムに次のものが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-154">To use this feature, your system must include the following:</span></span>

- <span data-ttu-id="b3f74-155">Dynamics 365 Supply Chain Management バージョン 10.0.15 以降</span><span class="sxs-lookup"><span data-stu-id="b3f74-155">Dynamics 365 Supply Chain Management version 10.0.15 or later</span></span>
- <span data-ttu-id="b3f74-156">Supply Chain Management アプリに対する[二重書き込み](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write)。</span><span class="sxs-lookup"><span data-stu-id="b3f74-156">[Dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write) for Supply Chain Management apps.</span></span>
- <span data-ttu-id="b3f74-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution)バージョン 400.0.1.48、またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="b3f74-157">[Dynamics 365 Guides](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) version 400.0.1.48 or later</span></span>

### <a name="turn-on-the-feature"></a><span data-ttu-id="b3f74-158">機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="b3f74-158">Turn on the feature</span></span>

<span data-ttu-id="b3f74-159">この機能をシステムで使用できるようにするには、その構成キーを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-159">To make the feature available on your system, you must enable its configuration keys.</span></span> <span data-ttu-id="b3f74-160">これを行う必要があるのは 1 回だけです。</span><span class="sxs-lookup"><span data-stu-id="b3f74-160">You only need to do this once.</span></span> <span data-ttu-id="b3f74-161">これを行うには、管理者が次の操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-161">To do this, an administrator must do the following:</span></span>

1. <span data-ttu-id="b3f74-162">[メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、システムをメンテナンス モードにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-162">Place your system into maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="b3f74-163">**システム管理 \> 設定 \> ライセンス コンフィギュレーション** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-163">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="b3f74-164">**Mixed reality** セクションを展開し、 **Mixed reality ガイド** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-164">Expand the **Mixed reality** section and then select the **Mixed reality guide** check box.</span></span>
1. <span data-ttu-id="b3f74-165">**製品管理** セクションを展開し、 **生産指示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-165">Expand the **Production management** section and then select the **Production instructions** check box.</span></span>
1. <span data-ttu-id="b3f74-166">[メンテナンス モード](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md)の説明に従って、メンテナンス モードをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-166">Turn off maintenance mode as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
  
## <a name="configure-how-guides-appear-on-the-shop-floor"></a><span data-ttu-id="b3f74-167">作業現場でのガイド表示方法の構成</span><span class="sxs-lookup"><span data-stu-id="b3f74-167">Configure how Guides appear on the shop floor</span></span>

<span data-ttu-id="b3f74-168">作業現場でのガイドの表示方法を構成するには、 **Mixed Reality \> Dynamics 365 Guides \> 構成ガイドの統合** へ移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-168">To configure how Guides appear on the shop floor, go to **Mixed Reality \> Dynamics 365 Guides \> Configure Guides integration**.</span></span>

<span data-ttu-id="b3f74-169">![製造用構成ガイドの統合](media/instruction-guides-configure-integration.png "製造用ガイド統合の構成")</span><span class="sxs-lookup"><span data-stu-id="b3f74-169">![Configure Guide integration for manufacturing](media/instruction-guides-configure-integration.png "Configure Guide integration for manufacturing")</span></span>

<span data-ttu-id="b3f74-170">次のフィールドを設定します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-170">Set the following fields:</span></span>

- <span data-ttu-id="b3f74-171">**Common Data Service サブドメイン** - このフィールドには、すでに値が表示されているはずです。</span><span class="sxs-lookup"><span data-stu-id="b3f74-171">**Common Data Service subdomain** - This field should already show a value.</span></span> <span data-ttu-id="b3f74-172">このフィールドには、ガイドを作成する Common Data Service 環境のサブドメインが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3f74-172">This field holds the subdomain for the Common Data Service environment where you create your Guides.</span></span> <span data-ttu-id="b3f74-173">サブドメインは URL の最初の部分であり、通常は組織の後に名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-173">The subdomain is the first part of the URL and is typically named after your organization.</span></span> <span data-ttu-id="b3f74-174">たとえば、Common Data Service URL が "contoso.crm4.dynamics.com" の場合、ここで *contoso* を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-174">For example, if your Common Data Service URL is "contoso.crm4.dynamics.com", you should enter *contoso* here.</span></span> <span data-ttu-id="b3f74-175">この値は、ガイドのアドレスを作成するために使用され、QR コードにエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-175">This value is used to compose addresses for your guides and will be encoded into the QR codes.</span></span>
- <span data-ttu-id="b3f74-176">**QR コード サイズ** - レンダリングされた QR コードのサイズを設定します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-176">**QR code size** - Set the size of the rendered QR code.</span></span> <span data-ttu-id="b3f74-177">表示画面の大部分を占めるサイズを選択することをお勧めしますが、それ以上にはしないでください。</span><span class="sxs-lookup"><span data-stu-id="b3f74-177">We recommend choosing a size that will fill most of your display screen, but not more.</span></span> <span data-ttu-id="b3f74-178">通常、 *15* が適切な値です。</span><span class="sxs-lookup"><span data-stu-id="b3f74-178">Typically, *15* is a good value.</span></span>
- <span data-ttu-id="b3f74-179">**QR コード エラー訂正レベル** - QR コードの粒度を設定します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-179">**QR code error correction level** - Set the granularity of the QR code.</span></span> <span data-ttu-id="b3f74-180">粒度を高くすると、コードの信頼性を高めることができますが、 **QR コードのサイズ** は選択した修正レベルに必要な詳細レベルをサポートするために、十分な大きさにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-180">Higher granularity can help increase the code's reliability, but your **QR code size** must be large enough to support the level of detail required by your selected correction level.</span></span>


> [!TIP]
> - <span data-ttu-id="b3f74-181">QR コードのサイズが大きすぎてディスプレイに表示できない場合は、表示に時間がかかります。表示に合わせて縮小する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-181">QR codes sizes that are too large for your display will take a bit longer to render and then be scaled down to fit your display.</span></span> <span data-ttu-id="b3f74-182">これらにはメリットがありません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-182">These do not provide a benefit.</span></span>
> - <span data-ttu-id="b3f74-183">QR コードのサイズが小さすぎると、一部の環境で HoloLens がコードを適切に読み取る能力が低下する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-183">QR code sizes that are too small may decrease the ability of HoloLens to read the code properly in some environments.</span></span>
> - <span data-ttu-id="b3f74-184">HoloLens ユーザー向けに、QR コードを表示する各デバイスの設定をテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-184">We recommend that you test the settings for each device that will display QR codes for HoloLens users.</span></span> <span data-ttu-id="b3f74-185">作業現場の環境で読みやすさを確保できる設定を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-185">Choose settings that provide sufficient readability in your shop floor environment.</span></span>  

## <a name="get-an-overview-of-all-guide-assignments"></a><span data-ttu-id="b3f74-186">すべてのガイド割り当ての概要を取得する</span><span class="sxs-lookup"><span data-stu-id="b3f74-186">Get an overview of all Guide assignments</span></span>

<span data-ttu-id="b3f74-187">**すべてのガイド** ページを使用すると、組織で使用可能なすべてのガイドの一覧を表示したり、生産プロセスやリソースに対するすべての割り当てを表示したりできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-187">Use the **All Guides** page to see the list of all available Guides in your organization and all assignments to your production processes and resources.</span></span> <span data-ttu-id="b3f74-188">これを開くには、 **Mixed reality \> ガイド \> すべてのガイド** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-188">To open it, go to **Mixed reality \> Guides \> All Guides**.</span></span> <span data-ttu-id="b3f74-189">上部の一覧には使用可能なすべてのガイドが表示され、ここでフィールドを使用して一覧をフィルタリングできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-189">The list at the top shows all the available Guides and you can use the field here to filter the list.</span></span> <span data-ttu-id="b3f74-190">下部の一覧には、すべてのガイドの割り当てが表示され、それらを管理するためのツールバーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-190">The list at the bottom shows all Guide assignments and provides a toolbar for managing them.</span></span>

<span data-ttu-id="b3f74-191">![ガイドの管理](media/instruction-guides-allguides.png "ガイドの管理")</span><span class="sxs-lookup"><span data-stu-id="b3f74-191">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

<span data-ttu-id="b3f74-192">次のセクションでは、ガイドを割り当てることができるオブジェクトのタイプについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-192">The following sections describe the types of objects that you can assign Guides to.</span></span> <span data-ttu-id="b3f74-193">各割り当てガイドには、それぞれの生産ジョブに自動的に関連付けられた手順が表示され、作業現場で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-193">Each assigned guide provides instructions that are automatically attached to the respective production jobs and will be available on the shop floor.</span></span>

## <a name="associate-a-guide-to-a-resource"></a><a name="resources"></a><span data-ttu-id="b3f74-194">リソースへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-194">Associate a Guide to a resource</span></span>

<span data-ttu-id="b3f74-195">[リソース](operations-resources.md)にガイドを追加して、関連する生産ジョブのコンテキストでガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-195">Add a Guide to a [resource](operations-resources.md) to offer the Guide in the context of relevant production jobs.</span></span>

### <a name="typical-scenario-using-resources"></a><span data-ttu-id="b3f74-196">リソースを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-196">Typical scenario using resources</span></span>

<span data-ttu-id="b3f74-197">たとえば、マシンの一般的なセキュリティに関するガイドや、マシン タイプのリソースへの手順を処理するガイドを関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-197">For example, you could attach a Guide with general machine security or handling instructions to a resource of type machine.</span></span> <span data-ttu-id="b3f74-198">その後、このガイドはマシンで実行されるすべてのジョブで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-198">Then, the Guide will be available on every job that is performed on the machine.</span></span>

### <a name="add-a-guide-to-a-resource"></a><span data-ttu-id="b3f74-199">リソースへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-199">Add a Guide to a resource</span></span>

<span data-ttu-id="b3f74-200">リソースへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-200">To add a Guide to a resource:</span></span>

1. <span data-ttu-id="b3f74-201">**生産管理 \> 設定 \> リソース \> リソース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-201">Go to **Production control \> Setup \> Resources \> Resources**.</span></span>
1. <span data-ttu-id="b3f74-202">一覧ペインから、ガイドを割り当てるリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-202">From the list pane, select the resource you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-203">**関連するガイド** のクイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-203">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="b3f74-204">**関連するガイド** ツールバーから **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-204">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="b3f74-205">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-205">A new line is added to the grid.</span></span>
1. <span data-ttu-id="b3f74-206">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-206">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="b3f74-207">ガイドの数が多い場合は、一覧をフィルタリングして目的のガイドを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-207">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="b3f74-208">![ガイドの管理](media/instruction-guides-allguides.png "ガイドの管理")</span><span class="sxs-lookup"><span data-stu-id="b3f74-208">![Manage Guides](media/instruction-guides-allguides.png "Manage Guides")</span></span>

## <a name="associate-a-guide-to-a-resource-group"></a><a name="resource-groups"></a><span data-ttu-id="b3f74-209">リソース グループへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-209">Associate a Guide to a resource group</span></span>

<span data-ttu-id="b3f74-210">リソース グループを使用してマシンのグループ、生産ライン、または作業セルを管理する場合、[リソース グループ](tasks/define-discrete-manufacturing-resource-group.md)にガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-210">You can add a guide to [resource groups](tasks/define-discrete-manufacturing-resource-group.md) if you use them to manage groups of machines, production lines, or work cells.</span></span>

### <a name="typical-scenarios-using-resource-groups"></a><span data-ttu-id="b3f74-211">リソース グループを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-211">Typical scenarios using resource groups</span></span>

<span data-ttu-id="b3f74-212">**例 1:** 同じモデルの複数のマシンに対してリソース グループを定義している場合。</span><span class="sxs-lookup"><span data-stu-id="b3f74-212">**Example 1:** You have defined a resource group for several machines of the same model.</span></span> <span data-ttu-id="b3f74-213">マシン モデルに関連する取扱説明ガイドを関連するすべてのリソースに割り当てる代わりに、そのマシン モデルを反映するリソース グループにガイドを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-213">Instead of assigning the relevant handling instruction guide for the machine model to every relevant resource, you could instead assign the Guide to the resource group that reflects that machine model.</span></span>

<span data-ttu-id="b3f74-214">**例 2:** 異なるマシンを含む作業セルにリソース グループを定義している場合、作業セルを管理するための一般的な手順を提供するガイドがあります。</span><span class="sxs-lookup"><span data-stu-id="b3f74-214">**Example 2:** You have defined a resource group for a work cell that contains different machines and you have a Guide that provides general instructions for how to maintain the work cell.</span></span> <span data-ttu-id="b3f74-215">このガイドは、この作業セルのすべての生産活動に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-215">The Guide applies to any production activity in this work cell.</span></span>

### <a name="add-a-guide-to-a-resource-group"></a><span data-ttu-id="b3f74-216">リソース グループへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-216">Add a Guide to a resource group</span></span>

<span data-ttu-id="b3f74-217">リソース グループへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-217">To add a Guide to a resource group:</span></span>

1. <span data-ttu-id="b3f74-218">**生産管理 \> 設定 \> リソース \> リソース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-218">Go to **Production control \> Setup \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="b3f74-219">一覧ペインから、ガイドを割り当てるリソース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-219">From the list pane, select the resource group you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-220">**関連するガイド** のクイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-220">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="b3f74-221">**関連するガイド** ツールバーから **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-221">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="b3f74-222">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-222">A new line is added to the grid.</span></span>
1. <span data-ttu-id="b3f74-223">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-223">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="b3f74-224">ガイドの数が多い場合は、一覧をフィルタリングして目的のガイドを見つけることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-224">If you have a large number of Guides, then you can filter the list to find the one you are looking for.</span></span>
    <span data-ttu-id="b3f74-225">![リソース グループへのガイドの追加](media/instruction-guides-resourcegroup.png "リソース グループへガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-225">![Adding a Guide to a resource group](media/instruction-guides-resourcegroup.png "Adding a Guide to a resource group")</span></span>

## <a name="associate-a-guide-to-a-released-product"></a><a name="released-products"></a><span data-ttu-id="b3f74-226">リリース済製品へのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-226">Associate a Guide to a released product</span></span>

<span data-ttu-id="b3f74-227">[リリース済製品](../pim/tasks/create-released-product-single-company.md)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-227">You can add a guide to any [released product](../pim/tasks/create-released-product-single-company.md).</span></span>

### <a name="typical-scenario-using-released-products"></a><span data-ttu-id="b3f74-228">リリース済製品を使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-228">Typical scenario using released products</span></span>

<span data-ttu-id="b3f74-229">製品レベルのガイドでは、特定のリリース済製品または品目の運用または処理に関する手順が作業現場の作業者に提供されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-229">Product-level Guides help shop floor workers with instructions relevant to operating or handling a specific released product or item.</span></span>

### <a name="add-a-guide-to-a-released-product"></a><span data-ttu-id="b3f74-230">リリース済製品へのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-230">Add a Guide to a released product</span></span>

<span data-ttu-id="b3f74-231">リリース済製品へガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-231">To add a Guide to a released product:</span></span>

1. <span data-ttu-id="b3f74-232">**生産情報管理 \> 製品 \> リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-232">Go to **Production information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="b3f74-233">ガイドを割り当てる製品を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-233">Open the product you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-234">アクション ウィンドウで、 **エンジニア** タブを開き、 **表示** グループから、 **関連するガイド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-234">On the Action Pane, open the **Engineer** tab and from the **View** group, select **Associated Guides**.</span></span>
1. <span data-ttu-id="b3f74-235">選択したプロダクトの **関連ガイド** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-235">The **Associated Guides** page opens for your selected product.</span></span>
1. <span data-ttu-id="b3f74-236">アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-236">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="b3f74-237">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-237">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-238">![リリース済製品へガイドを追加する](media/instruction-guides-ReleasedProduct-AddGuides.png "リリース済製品へガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-238">![Adding a Guide to a released product](media/instruction-guides-ReleasedProduct-AddGuides.png "Adding a Guide to a released product")</span></span>

## <a name="associate-a-guide-to-a-formula"></a><a name="formulas"></a><span data-ttu-id="b3f74-239">フォーミュラへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-239">Associate a Guide to a formula</span></span>

<span data-ttu-id="b3f74-240">[フォーミュラ](bill-of-material-bom.md#formulas-co-products-and-by-products)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-240">You can add a guide to any [formula](bill-of-material-bom.md#formulas-co-products-and-by-products).</span></span>

### <a name="typical-scenario-using-formulas"></a><span data-ttu-id="b3f74-241">フォーミュラを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-241">Typical scenario using formulas</span></span>
  
<span data-ttu-id="b3f74-242">フォーミュラ レベル ガイドは、フォーミュラまたはレシピのコンテキストでのガイド付き処理手順が作業現場の作業者に用意されています。</span><span class="sxs-lookup"><span data-stu-id="b3f74-242">Formula-level Guides provide shop floor workers with guided handling instructions in the context of a formula or recipe.</span></span> <span data-ttu-id="b3f74-243">また、フォーミュラのバージョンにガイドを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-243">Guides can also be assigned to versions of a formula.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f74-244">生産プロセスに関連するガイダンスは、工順、工順バージョン、または工順工程関連に対するフォーミュラに基づいて割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-244">You can assign guidance relevant for production processes based on a formula to a route, route version, or route operation relations.</span></span>  

> <span data-ttu-id="b3f74-245">現在、個々のフォーミュラ行にガイドを関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-245">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula"></a><span data-ttu-id="b3f74-246">フォーミュラへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-246">Add a Guide to a formula</span></span>

<span data-ttu-id="b3f74-247">フォーミュラへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-247">To add a Guide to a formula:</span></span>

1. <span data-ttu-id="b3f74-248">**生産情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-248">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="b3f74-249">ガイドを割り当てるフォーミュラを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-249">Open the formula you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-250">上部クイックタブの上にある **ヘッダー** タブを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-250">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="b3f74-251">**関連するガイド** のクイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-251">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="b3f74-252">**関連するガイド** ツールバーから **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-252">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="b3f74-253">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-253">A new line is added to the grid.</span></span>
1. <span data-ttu-id="b3f74-254">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-254">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-255">![フォーミュラへガイドを追加する](media/instruction-guides-Formula.png "フォーミュラへガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-255">![Adding a Guide to a formula](media/instruction-guides-Formula.png "Adding a Guide to a formula")</span></span>

## <a name="associate-a-guide-to-a-formula-version"></a><a name="formula-versions"></a><span data-ttu-id="b3f74-256">フォーミュラ バージョンへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-256">Associate a Guide to a formula version</span></span>

<span data-ttu-id="b3f74-257">[フォーミュラ バージョン](bill-of-material-bom.md#bom-and-formula-versions)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-257">You can add a guide to any [formula version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-formula-versions"></a><span data-ttu-id="b3f74-258">フォーミュラ バージョンを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-258">Typical scenario using formula versions</span></span>

<span data-ttu-id="b3f74-259">フォーミュラの個々のバージョンに関連付けられたガイドは、そのバージョンのフォーミュラ レシピの生産についての手順を作業現場の作業者に提供します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-259">Guides attached to an individual version of a formula provide shop floor workers with instructions that walk through the production of that version of the formula recipe.</span></span>

> [!TIP]
> <span data-ttu-id="b3f74-260">生産プロセスに関連するガイダンスは、工順、工順バージョン、または工順工程関連に対するこのフォーミュラ バージョンに基づいて割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-260">You can assign guidance relevant for production processes based on this formula version to a route, route version, or route operation relations.</span></span>  

> [!NOTE]
> <span data-ttu-id="b3f74-261">現在、個々のフォーミュラ行にガイドを関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-261">Guides can't currently be attached to individual formula lines.</span></span>

### <a name="add-a-guide-to-a-formula-version"></a><span data-ttu-id="b3f74-262">フォーミュラ バージョンへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-262">Add a Guide to a formula version</span></span>

<span data-ttu-id="b3f74-263">フォーミュラ バージョンへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-263">To add a Guide to a formula version:</span></span>

1. <span data-ttu-id="b3f74-264">**生産情報管理 \> 部品表およびフォーミュラ \> フォーミュラ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-264">Go to **Production information management \> Bills of materials and formulas \> Formulas**.</span></span>
1. <span data-ttu-id="b3f74-265">ガイドを割り当てるバージョンを含むフォーミュラを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-265">Open the formula that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-266">上部クイックタブの上にある **ヘッダー** タブを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-266">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="b3f74-267">**フォーミュラ バージョン** クイックタブで、ガイドを割り当てるバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-267">On the **Formula versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-268">**フォーミュラ バージョン** ツールバーで、 **関連するガイド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-268">On the **Formula versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="b3f74-269">![選択したフォーミュラ バージョンに関連付けられているガイドの表示](media/instruction-guides-FormulaVersion.png "選択したフォーミュラ バージョンに関連付けられているガイドの表示")</span><span class="sxs-lookup"><span data-stu-id="b3f74-269">![Open the Guides associated with a selected formula version](media/instruction-guides-FormulaVersion.png "Open the Guides associated with a selected formula version")</span></span>
1. <span data-ttu-id="b3f74-270">フォーミュラ バージョンの **関連ガイド** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-270">The **Associated Guides** page opens for your formula version.</span></span>
1. <span data-ttu-id="b3f74-271">アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-271">Select **Add** on the Action Pane to add a new line to the grid.</span></span> 
1. <span data-ttu-id="b3f74-272">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-272">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-273">![フォーミュラ バージョンへガイドを追加する](media/instruction-guides-FormulaVersionAddGuide.png "フォーミュラ バージョンへガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-273">![Adding a Guide to a formula version](media/instruction-guides-FormulaVersionAddGuide.png "Adding a Guide to a formula version")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials"></a><a name="bom"></a><span data-ttu-id="b3f74-274">部品表へのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-274">Associate a Guide to a bill of materials</span></span>

<span data-ttu-id="b3f74-275">すべての[部品表](bill-of-material-bom.md) (BOM) にガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-275">You can add a guide to any [bill of materials](bill-of-material-bom.md) (BOM).</span></span>

### <a name="typical-scenario-using-bills-of-materials"></a><span data-ttu-id="b3f74-276">部品表を使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-276">Typical scenario using bills of materials</span></span>

<span data-ttu-id="b3f74-277">BOM に関連付けられているガイドには、BOM から材料を準備および処理する方法を説明する手順が作業現場の作業者に用意されています。</span><span class="sxs-lookup"><span data-stu-id="b3f74-277">Guides attached to a BOM provide shop floor workers with instructions that explain how to prepare and handle material from a BOM.</span></span> <span data-ttu-id="b3f74-278">また、BOM のバージョンにガイドを割り当てることもできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-278">Guides can also be assigned to versions of a BOM.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f74-279">現在、個々の BOM 行にガイドを関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-279">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials"></a><span data-ttu-id="b3f74-280">部品表へのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-280">Add a Guide to a bill of materials</span></span>

<span data-ttu-id="b3f74-281">部品表へガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-281">To add a Guide to a bill of material:</span></span>

1. <span data-ttu-id="b3f74-282">**生産情報管理 \> 部品表およびフォーミュラ \> 部品表** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-282">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="b3f74-283">ガイドを割り当てる部品表を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-283">Open the bill of materials that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-284">上部クイックタブの上にある **ヘッダー** タブを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-284">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="b3f74-285">**関連するガイド** のクイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-285">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="b3f74-286">**関連するガイド** ツールバーから **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-286">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="b3f74-287">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-287">A new line is added to the grid.</span></span>
1. <span data-ttu-id="b3f74-288">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-288">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-289">![BOM へガイドを追加する](media/instruction-guides-BOM.png "BOM へガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-289">![Adding a Guide to a BOM](media/instruction-guides-BOM.png "Adding a Guide to a BOM")</span></span>

## <a name="associate-a-guide-to-a-bill-of-materials-version"></a><a name="bom-versions"></a><span data-ttu-id="b3f74-290">部品表バージョンへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-290">Associate a Guide to a bill of materials version</span></span>

<span data-ttu-id="b3f74-291">すべての[部品表バージョン](bill-of-material-bom.md#bom-and-formula-versions)にガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-291">You can add a guide to any [bill of materials version](bill-of-material-bom.md#bom-and-formula-versions).</span></span>

### <a name="typical-scenario-using-bill-of-materials-versions"></a><span data-ttu-id="b3f74-292">部品表バージョンを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-292">Typical scenario using bill of materials versions</span></span>

<span data-ttu-id="b3f74-293">個々の BOM バージョンに関連付けられたガイドでは、ジェネリック BOM またはその他のバージョンとは異なるバージョンの BOM の材料を準備および処理する方法を説明する手順が作業現場の作業者に用意されています。</span><span class="sxs-lookup"><span data-stu-id="b3f74-293">Guides attached to an individual BOM version provide shop floor workers with instructions that explain how to prepare and handle material for a version of a BOM that is different from the generic BOM or other versions of it.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f74-294">現在、個々の BOM 行にガイドを関連付けることはできません。</span><span class="sxs-lookup"><span data-stu-id="b3f74-294">Guides can't currently be attached to individual BOM lines.</span></span>

### <a name="add-a-guide-to-a-bill-of-materials-version"></a><span data-ttu-id="b3f74-295">部品表バージョンへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-295">Add a Guide to a bill of materials version</span></span>

<span data-ttu-id="b3f74-296">部品表バージョンへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-296">To add a Guide to a bill of materials version:</span></span>

1. <span data-ttu-id="b3f74-297">**生産情報管理 \> 部品表およびフォーミュラ \> 部品表** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-297">Go to **Production information management \> Bills of materials and formulas \> Bills of materials**.</span></span>
1. <span data-ttu-id="b3f74-298">ガイドを割り当てるバージョンを含む BOM を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-298">Open the BOM that includes a version that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-299">上部クイックタブの上にある **ヘッダー** タブを開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-299">Open the **Header** tab above the top FastTab.</span></span>
1. <span data-ttu-id="b3f74-300">**BOM バージョン** クイックタブで、ガイドを割り当てるバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-300">On the **BOM versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-301">**BOM バージョン** ツールバーで、 **関連するガイド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-301">On the **BOM versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="b3f74-302">![選択した BOM バージョンに関連付けられているガイドの表示](media/instruction-guides-BOMVersion.png "選択した BOM バージョンに関連付けられているガイドの表示")</span><span class="sxs-lookup"><span data-stu-id="b3f74-302">![Open the Guides associated with a selected BOM version](media/instruction-guides-BOMVersion.png "Open the Guides associated with a selected BOM version")</span></span>
1. <span data-ttu-id="b3f74-303">BOM バージョンの **関連ガイド** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-303">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="b3f74-304">アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-304">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="b3f74-305">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-305">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-306">![BOM バージョンへガイドを追加する](media/instruction-guides-BOMVersionAddGuide.png "BOM バージョンへガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-306">![Adding a Guide to a BOM version](media/instruction-guides-BOMVersionAddGuide.png "Adding a Guide to a BOM version")</span></span>

## <a name="associate-a-guide-to-a-route"></a><a name="routes"></a><span data-ttu-id="b3f74-307">工順へのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-307">Associate a Guide to a route</span></span>

<span data-ttu-id="b3f74-308">[工順](routes-operations.md)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-308">You can add a guide to any [route](routes-operations.md).</span></span>

### <a name="typical-scenario-using-routes"></a><span data-ttu-id="b3f74-309">工順を使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-309">Typical scenario using routes</span></span>

<span data-ttu-id="b3f74-310">通常、工順は、BOM または BOM バージョンに基づいて、一連のリソースまたはリソース グループを使用して、特定のリリース製品をどのように生産するかを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-310">Routes are typically used to specify how a certain released product shall be produced based on a BOM or BOM version and with a set of resources or resource groups.</span></span>

<span data-ttu-id="b3f74-311">工順にガイドを割り当てることにより、それぞれの生産プロセスに関する手順を説明します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-311">Assign a Guide to a route to provide step-by-step instructions for the respective production process.</span></span>

### <a name="add-a-guide-to-a-route"></a><span data-ttu-id="b3f74-312">工順へのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-312">Add a Guide to a route</span></span>

<span data-ttu-id="b3f74-313">工順へガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-313">To add a Guide to a route:</span></span>

1. <span data-ttu-id="b3f74-314">**生産管理 \> すべての工順** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-314">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="b3f74-315">ガイドを割り当てる工順を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-315">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-316">**関連するガイド** のクイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-316">Expand the **Associated Guides** FastTab.</span></span>
1. <span data-ttu-id="b3f74-317">**関連するガイド** ツールバーから **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-317">Select **Add** from the **Associated Guides** toolbar.</span></span> <span data-ttu-id="b3f74-318">新しい行がグリッドに追加されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-318">A new line is added to the grid.</span></span>
1. <span data-ttu-id="b3f74-319">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-319">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-320">![工順へガイドを追加する](media/instruction-guides-Route.png "工順へガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-320">![Adding a Guide to a route](media/instruction-guides-Route.png "Adding a Guide to a route")</span></span>

## <a name="associate-a-guide-to-a-route-version"></a><a name="route-versions"></a><span data-ttu-id="b3f74-321">工順バージョンへのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-321">Associate a Guide to a route version</span></span>

<span data-ttu-id="b3f74-322">[工順バージョン](routes-operations.md#route-versions)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-322">You can add a guide to any [route version](routes-operations.md#route-versions).</span></span>

### <a name="typical-scenario-using-route-versions"></a><span data-ttu-id="b3f74-323">工順バージョンを使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-323">Typical scenario using route versions</span></span>

<span data-ttu-id="b3f74-324">工順バージョンは、通常、既存の工順に基づいて生産プロセスのバリアントを指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-324">Routes versions are typically used to specify variants of production processes based on an existing route.</span></span> <span data-ttu-id="b3f74-325">各工順バージョンには、さまざまなガイドを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-325">You can assign different Guides to each route version.</span></span>

### <a name="add-a-guide-to-a-route-version"></a><span data-ttu-id="b3f74-326">工順バージョンへのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-326">Add a Guide to a route version</span></span>

<span data-ttu-id="b3f74-327">工順バージョンへガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-327">To add a Guide to a route version:</span></span>

1. <span data-ttu-id="b3f74-328">**生産管理 \> すべての工順** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-328">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="b3f74-329">ガイドを割り当てる工順を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-329">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-330">**バージョン** クイック タブで、ガイドを割り当てるバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-330">On the **Versions** FastTab, select the version you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-331">**バージョン** ツールバーで、 **関連するガイド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-331">On the **Versions** toolbar, select **Associated Guides**.</span></span>
    <span data-ttu-id="b3f74-332">![選択した工順バージョンに関連付けられているガイドの表示](media/instruction-guides-RouteVersion.png "選択した工順バージョンに関連付けられているガイドの表示")</span><span class="sxs-lookup"><span data-stu-id="b3f74-332">![Open the Guides associated with a selected route version](media/instruction-guides-RouteVersion.png "Open the Guides associated with a selected route version")</span></span>
1. <span data-ttu-id="b3f74-333">BOM バージョンの **関連ガイド** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-333">The **Associated Guides** page opens for your BOM version.</span></span>
1. <span data-ttu-id="b3f74-334">アクション ウィンドウで **追加** を選択して、新しい行をグリッドに追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-334">Select **Add** on the Action Pane to add a new line to the grid.</span></span>
1. <span data-ttu-id="b3f74-335">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-335">For the new line, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span>
    <span data-ttu-id="b3f74-336">![工順バージョンへガイドを追加する](media/instruction-guides-RouteVersionAddGuide.png "工順バージョンへガイドを追加する")</span><span class="sxs-lookup"><span data-stu-id="b3f74-336">![Adding a Guide to a route version](media/instruction-guides-RouteVersionAddGuide.png "Adding a Guide to a route version")</span></span>

## <a name="associate-a-guide-to-a-route-operation-relation"></a><a name="route-operation-relations"></a><span data-ttu-id="b3f74-337">工順工程関連へのガイドの関連付け</span><span class="sxs-lookup"><span data-stu-id="b3f74-337">Associate a Guide to a route operation relation</span></span>

<span data-ttu-id="b3f74-338">[工順工程関連](routes-operations.md#operation-relations)にはガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-338">You can add a guide to any [route operation relation](routes-operations.md#operation-relations).</span></span>

### <a name="typical-scenario-using-route-operation-relations"></a><span data-ttu-id="b3f74-339">工順工程関連を使用する一般的なシナリオ</span><span class="sxs-lookup"><span data-stu-id="b3f74-339">Typical scenario using route operation relations</span></span>

<span data-ttu-id="b3f74-340">関連する工程は、製品プロセスや関連工程に対してガイダンスを追加するための最も具体的な方法です。</span><span class="sxs-lookup"><span data-stu-id="b3f74-340">Operation relations are the most specific way to add guidance to a product process and its related operations.</span></span> <span data-ttu-id="b3f74-341">工順の各工程についてのガイダンスを指定したり、特定の品目や構成など工順に指定された関係コンテキストのタイプに対してさまざまなガイダンスを指定したりできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-341">You can specify guidance for each operation in a route and specify different guidance for any type of relation context specified for a route, such as for specific items, configurations, and more.</span></span> <span data-ttu-id="b3f74-342">また、ガイダンスが適用される工程のステージ (設定、キュー、プロセス、配送など) を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-342">You can also specify to which stages in the operation the guidance applies (such as setup, queueing, process, or transport).</span></span>

> [!NOTE]
> <span data-ttu-id="b3f74-343">このようなガイドで、工順の複数の工程に関連するガイドを指定した場合、生成されたジョブの作業現場には、最も具体的な関係のあるガイドのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-343">If you specify guides for several operation relations of a route, among those guides, only the guide from the most specific relation will be show on the shop floor for the generated job.</span></span>

### <a name="add-a-guide-to-a-route-operation-relation"></a><span data-ttu-id="b3f74-344">工順工程関連へのガイドの追加</span><span class="sxs-lookup"><span data-stu-id="b3f74-344">Add a Guide to a route operation relation</span></span>

<span data-ttu-id="b3f74-345">工順工程関連へガイドを追加するには:</span><span class="sxs-lookup"><span data-stu-id="b3f74-345">To add a Guide to a route operation relation:</span></span>

1. <span data-ttu-id="b3f74-346">**生産管理 \> すべての工順** に移動します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-346">Go to **Production control \> All routes**.</span></span>
1. <span data-ttu-id="b3f74-347">ガイドを割り当てる工順を開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-347">Open the route that you want to assign a Guide to.</span></span>
1. <span data-ttu-id="b3f74-348">アクション ウィンドウで、 **工順** タブを開き、 **管理** グループから、 **工順の詳細** を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-348">On the Action Pane, open the **Route** tab and from the **Maintain** group, select **Route details**.</span></span>
1. <span data-ttu-id="b3f74-349">選択した工順の **工順の詳細** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-349">The **Route details** page opens for your selected rout.</span></span>
1. <span data-ttu-id="b3f74-350">上部グリッドで、ガイダンスを提供する工程を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-350">In the top grid, select the operation you want to provide guidance for.</span></span>
1. <span data-ttu-id="b3f74-351">下部グリッドで、特定の関係 (汎用的な **すべて** の関係) を選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-351">In the bottom grid, select a specific relation (or the generic **All** relation).</span></span>
    <span data-ttu-id="b3f74-352">![工程を選択してから、関係を選択](media/instruction-guides-RouteOperationRelation.png "工程を選択してから、関係を選択")</span><span class="sxs-lookup"><span data-stu-id="b3f74-352">![Select an operation and then a relation](media/instruction-guides-RouteOperationRelation.png "Select an operation and then a relation")</span></span>
1. <span data-ttu-id="b3f74-353">下段の上にある **関連するガイド** タブを開きます。![関連するガイド タブ](media/instruction-guides-RouteOperationRelation-AddGuide.png "関連するガイド タブ")</span><span class="sxs-lookup"><span data-stu-id="b3f74-353">Above the bottom gird, open the **Associated Guides** tab.  ![The Associated Guides tab](media/instruction-guides-RouteOperationRelation-AddGuide.png "The Associated Guides tab")</span></span>
1. <span data-ttu-id="b3f74-354">下部のグリッドの一番上にあるツールバーの **追加** を選択して、グリッドに新しい行を追加します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-354">Select **Add** from the toolbar at the top of the bottom grid to add a new line to the grid.</span></span>
1. <span data-ttu-id="b3f74-355">新しい行の場合は、 **名前** 列のドロップダウン リストを使用して、割り当てるガイドを選択します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-355">For the new row, use the drop-down list in the **Name** column to choose the Guide you want to assign.</span></span> <span data-ttu-id="b3f74-356">行の残りの部分で、選択したガイドを使用できるようにする各コンテキストのチェックボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-356">In the rest of the row, select the check box for each context where the selected Guide should be available.</span></span>

> [!NOTE]
> <span data-ttu-id="b3f74-357">各工程のステージごとに 1 つ以上のガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-357">You can add one or more guides for each stage of each operation.</span></span>

## <a name="select-guides-from-the-shop-floor-execution-interface"></a><span data-ttu-id="b3f74-358">作業現場の実行インターフェイスからのガイドの選択</span><span class="sxs-lookup"><span data-stu-id="b3f74-358">Select guides from the shop floor execution interface</span></span>

<span data-ttu-id="b3f74-359">作業者が作業現場の実行インターフェイスでジョブリストを開くと、Supply Chain Management によって表示されているジョブに関連するガイドが検出されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-359">When a worker opens a job list on the shop floor execution interface, Supply Chain Management finds the relevant guides for the jobs shown.</span></span> <span data-ttu-id="b3f74-360">**ガイド** ボタンを使用して、関連するガイドを表示します。</span><span class="sxs-lookup"><span data-stu-id="b3f74-360">Use the **Guides** button to view the relevant guides.</span></span>

<span data-ttu-id="b3f74-361">![作業現場の実行インターフェイスでのガイド ボタン](media/instruction-guides-Shopfloor1.png "作業現場の実行インターフェイスでのガイド ボタン")</span><span class="sxs-lookup"><span data-stu-id="b3f74-361">![Guides button in the shop floor execution interface](media/instruction-guides-Shopfloor1.png "Guides button in the shop floor execution interface")</span></span>

<span data-ttu-id="b3f74-362">次に、HoloLens を装着し、QR コードを確認してそれぞれのガイドを有効化することによりガイドにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="b3f74-362">Then put on a HoloLens and access the respective guide by glancing at the QR code and activating the respective Guide.</span></span>

<span data-ttu-id="b3f74-363">![QR コードで HoloLens を使用してガイドにアクセスする](media/instruction-guides-Shopfloor2.png "QR コードで HoloLens を使用してガイドにアクセスする")</span><span class="sxs-lookup"><span data-stu-id="b3f74-363">![QR code to access guides using a HoloLens](media/instruction-guides-Shopfloor2.png "QR code to access guides using a HoloLens")</span></span>

## <a name="resolving-the-logic-for-selecting-guides"></a><a name="logic"></a><span data-ttu-id="b3f74-364">ガイドを選択するためのロジックを解決する</span><span class="sxs-lookup"><span data-stu-id="b3f74-364">Resolving the logic for selecting Guides</span></span>

<span data-ttu-id="b3f74-365">次の生産データにガイドを追加できます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-365">You can add Guides to the following production data:</span></span>

- [<span data-ttu-id="b3f74-366">リソース</span><span class="sxs-lookup"><span data-stu-id="b3f74-366">Resources</span></span>](#resources)
- [<span data-ttu-id="b3f74-367">リソース グループ</span><span class="sxs-lookup"><span data-stu-id="b3f74-367">Resource groups</span></span>](#resource-groups)
- [<span data-ttu-id="b3f74-368">リリースされた製品</span><span class="sxs-lookup"><span data-stu-id="b3f74-368">Released products</span></span>](#released-products)
- [<span data-ttu-id="b3f74-369">フォーミュラ</span><span class="sxs-lookup"><span data-stu-id="b3f74-369">Formulas</span></span>](#formulas)
- [<span data-ttu-id="b3f74-370">フォーミュラ バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-370">Formula versions</span></span>](#formula-versions)
- [<span data-ttu-id="b3f74-371">部品表 (BOM)</span><span class="sxs-lookup"><span data-stu-id="b3f74-371">Bills of material (BOMs)</span></span>](#bom)
- [<span data-ttu-id="b3f74-372">BOM バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-372">BOM versions</span></span>](#bom-versions)
- [<span data-ttu-id="b3f74-373">工順</span><span class="sxs-lookup"><span data-stu-id="b3f74-373">Routes</span></span>](#routes)
- [<span data-ttu-id="b3f74-374">工順バージョン</span><span class="sxs-lookup"><span data-stu-id="b3f74-374">Route versions</span></span>](#route-versions)
- [<span data-ttu-id="b3f74-375">工順工程関連</span><span class="sxs-lookup"><span data-stu-id="b3f74-375">Route operation relations</span></span>](#route-operation-relations)

<span data-ttu-id="b3f74-376">Supply Chain Management では、生産フロアのジョブを生成すると、それらのソースから関連するガイドが収集されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-376">When Supply Chain Management generates the jobs for the production floor, it will collect the relevant Guides from those sources.</span></span> <span data-ttu-id="b3f74-377">次の重要なルールに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b3f74-377">Take note of the following important rules.</span></span>

- <span data-ttu-id="b3f74-378">BOM バージョンまたはフォーミュラ バージョンを工順または製造オーダーに関連付けた場合、そのバージョンに関連付けられているすべてのガイドと、そのバージョンの親 BOM またはフォーミュラに関連付けられているガイドもジョブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-378">If you attach a BOM version or formula version to a route or production order, then any Guides attached to this version, and also the Guides attached to the parent BOM or formula of that version, will be shown on the job.</span></span>
- <span data-ttu-id="b3f74-379">工順 バージョンを製造オーダーに関連付けた場合、そのバージョンに関連付けられているすべてのガイドと、そのバージョンの親工順に関連付けられているガイドもジョブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-379">If you attach a route version to a production order, then any Guides attached to this version, and also the Guides attached to the parent route of that version, will be shown on the job.</span></span>
- <span data-ttu-id="b3f74-380">*すべて* の関係を含む工順工程関係を定義し、それらの関係にガイドを割り当てると、ジョブには最も具体的な関係のあるガイドのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="b3f74-380">If you define several route operation relations that include the *All* relation and assign Guides to those, only the Guides from the most specific relation will be shown for the job.</span></span>  

<span data-ttu-id="b3f74-381">![関連するガイドを解決する図](media/instruction-guides-Resolve.png "関連するガイドを解決する図")</span><span class="sxs-lookup"><span data-stu-id="b3f74-381">![Diagram on resolving the relevant Guides](media/instruction-guides-Resolve.png "Diagram on resolving the relevant Guides")</span></span>
