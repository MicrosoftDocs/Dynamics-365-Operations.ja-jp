---
title: Regulatory Configuration Service
description: このトピックでは、Regulatory Configuration Service (RCS) の機能の概要を示し、サービスにアクセスする方法について説明します。
author: JaneA07
manager: AnnBe
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: ec7e0fe07d979b85109605949b6ba33ab6d99b51
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890803"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="9f996-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="9f996-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f996-104">Regulatory Configuration Service (RCS) は、コードなし/ロー コードのグローバリゼーション機能のための、スタンドアロン デザイナーおよびライフサイクル管理サービスです。</span><span class="sxs-lookup"><span data-stu-id="9f996-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="9f996-105">RCS を使用すると、グローバリゼーションの関係者は、開発者を関与させることなく、税、電子請求、規制に関する報告、銀行、およびビジネス ドキュメントの主要なグローバリゼーション領域を拡張およびカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="9f996-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="9f996-106">このコードなし/ロー コードのグローバリゼーション アプローチにより、グローバリゼーションの作成または拡張がより簡単に、より迅速に、よりコスト効率が高くなります。</span><span class="sxs-lookup"><span data-stu-id="9f996-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="9f996-107">RCS は次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="9f996-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="9f996-108">電子レポート (ER) によって提供されるすべての機能のサポート。</span><span class="sxs-lookup"><span data-stu-id="9f996-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="9f996-109">新しいグローバリゼーション マイクロサービスを構成する前提条件。</span><span class="sxs-lookup"><span data-stu-id="9f996-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="9f996-110">電子請求のサポート。</span><span class="sxs-lookup"><span data-stu-id="9f996-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="9f996-111">詳細については、[電子請求](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f996-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="9f996-112">税計算のサポート。</span><span class="sxs-lookup"><span data-stu-id="9f996-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="9f996-113">詳細については、[税サービス](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f996-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="9f996-114">マルチコンポーネント機能のライフサイクル管理を簡素化し、アクションを構成し、機能パラメーターを設定するための追加機能を提供する、新しいグローバリゼーション機能のサポート。</span><span class="sxs-lookup"><span data-stu-id="9f996-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="9f996-115">詳細については、[Regulatory Configuration Service – グローバリゼーション サービスに対する簡素化されたグローバリゼーション機能の管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f996-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="9f996-116">Microsoft Dynamics Lifecycle Services (LCS) を使用せずに構成管理を簡素化するための、グローバル リポジトリでのカスタム構成の集中公開、保存、および共有のサポート。</span><span class="sxs-lookup"><span data-stu-id="9f996-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="9f996-117">アクセス RCS</span><span class="sxs-lookup"><span data-stu-id="9f996-117">Access RCS</span></span>

<span data-ttu-id="9f996-118">[Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/) から RCS に登録またはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="9f996-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RSC 登録/サインイン](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="9f996-120">**Regulatory Configuration Service** ページで、サービスの使用に関する追加の条件を確認して承認し、次のいずれかのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="9f996-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="9f996-121">初めてサービスを利用するユーザーで、組織にサービス環境をプロビジョニングするためにビジネス メール アドレスを使用している場合に **登録** する</span><span class="sxs-lookup"><span data-stu-id="9f996-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="9f996-122">サービスに以前にサインアップした、組織環境にアクセスしたい場合に **サインイン** する</span><span class="sxs-lookup"><span data-stu-id="9f996-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="9f996-123">地域の可用性</span><span class="sxs-lookup"><span data-stu-id="9f996-123">Regional availability</span></span>

<span data-ttu-id="9f996-124">通常、RCS は次の地域で使用できます。</span><span class="sxs-lookup"><span data-stu-id="9f996-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="9f996-125">米国</span><span class="sxs-lookup"><span data-stu-id="9f996-125">United States</span></span>
- <span data-ttu-id="9f996-126">インド</span><span class="sxs-lookup"><span data-stu-id="9f996-126">India</span></span>
- <span data-ttu-id="9f996-127">フランス</span><span class="sxs-lookup"><span data-stu-id="9f996-127">France</span></span>
- <span data-ttu-id="9f996-128">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="9f996-128">Europe</span></span>

<span data-ttu-id="9f996-129">地域の完全な一覧については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズ](https://aka.ms/dynamics_365_international_availability_deck) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f996-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="9f996-130">関連する RCS ドキュメント</span><span class="sxs-lookup"><span data-stu-id="9f996-130">Related RCS documentation</span></span>

<span data-ttu-id="9f996-131">関連コンポーネントの詳細については、次のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9f996-131">For more information about related components, see the following documentation:</span></span>

- <span data-ttu-id="9f996-132">**グローバル リポジトリ:**</span><span class="sxs-lookup"><span data-stu-id="9f996-132">**Global repository:**</span></span>

    - [<span data-ttu-id="9f996-133">ER コンフィギュレーションの作成 & グローバル リポジトリへのアップロード</span><span class="sxs-lookup"><span data-stu-id="9f996-133">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="9f996-134">グローバル リポジトリ でのコンフィギュレーションの共有</span><span class="sxs-lookup"><span data-stu-id="9f996-134">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="9f996-135">グローバル レポジトリの拡張フィルター処理</span><span class="sxs-lookup"><span data-stu-id="9f996-135">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="9f996-136">ER コンフィギュレーションをグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="9f996-136">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="9f996-137">グローバル リポジトリのコンフィギュレーションを中止する</span><span class="sxs-lookup"><span data-stu-id="9f996-137">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)

- <span data-ttu-id="9f996-138">**グローバリゼーション機能:**</span><span class="sxs-lookup"><span data-stu-id="9f996-138">**Globalization feature:**</span></span>

    - [<span data-ttu-id="9f996-139">Regulatory Configuration Service (RCS) - グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="9f996-139">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)