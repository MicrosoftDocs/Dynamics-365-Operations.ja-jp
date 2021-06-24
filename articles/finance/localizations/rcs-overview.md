---
title: Regulatory Configuration Service
description: このトピックでは、Regulatory Configuration Service (RCS) の機能の概要を示し、サービスにアクセスする方法について説明します。
author: JaneA07
ms.date: 06/04/2021
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
ms.openlocfilehash: 7f946988f124c814452e1774c700d5c7354f39b0
ms.sourcegitcommit: 60afcd85b3b5b9e5e8981ebbb57c0161cf05e54b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2021
ms.locfileid: "6216565"
---
# <a name="regulatory-configuration-service"></a><span data-ttu-id="d01db-103">Regulatory Configuration Service</span><span class="sxs-lookup"><span data-stu-id="d01db-103">Regulatory Configuration Service</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d01db-104">Regulatory Configuration Service (RCS) は、コードなし/ロー コードのグローバリゼーション機能のための、スタンドアロン デザイナーおよびライフサイクル管理サービスです。</span><span class="sxs-lookup"><span data-stu-id="d01db-104">Regulatory Configuration Service (RCS) is a standalone designer and lifecycle management service for no-code/low-code globalization functionality.</span></span> <span data-ttu-id="d01db-105">RCS を使用すると、グローバリゼーションの関係者は、開発者を関与させることなく、税、電子請求、規制に関する報告、銀行、およびビジネス ドキュメントの主要なグローバリゼーション領域を拡張およびカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="d01db-105">RCS lets globalization stakeholders extend and customize key globalization areas of tax, e-invoicing, regulatory reporting, banking, and business documents without having to involve developers.</span></span> <span data-ttu-id="d01db-106">このコードなし/ロー コードのグローバリゼーション アプローチにより、グローバリゼーションの作成または拡張がより簡単に、より迅速に、よりコスト効率が高くなります。</span><span class="sxs-lookup"><span data-stu-id="d01db-106">This no-code/low-code globalization approach makes globalization easier, faster, and more cost effective to create or extend.</span></span>

<span data-ttu-id="d01db-107">RCS は次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="d01db-107">RCS provides the following capabilities:</span></span>

- <span data-ttu-id="d01db-108">電子レポート (ER) によって提供されるすべての機能のサポート。</span><span class="sxs-lookup"><span data-stu-id="d01db-108">Support for all functionality that is provided by Electronic reporting (ER).</span></span>
- <span data-ttu-id="d01db-109">新しいグローバリゼーション マイクロサービスを構成する前提条件。</span><span class="sxs-lookup"><span data-stu-id="d01db-109">A prerequisite to configure new globalization microservices.</span></span>
- <span data-ttu-id="d01db-110">電子請求のサポート。</span><span class="sxs-lookup"><span data-stu-id="d01db-110">Support for Electronic Invoicing.</span></span> <span data-ttu-id="d01db-111">詳細については、[電子請求](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-111">For more information, see [Electronic Invoicing](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/electronic-invoicing-add-on-dynamics-365-ga).</span></span>
- <span data-ttu-id="d01db-112">税計算のサポート。</span><span class="sxs-lookup"><span data-stu-id="d01db-112">Supports for Tax Calculation.</span></span> <span data-ttu-id="d01db-113">詳細については、[税サービス](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-113">For more information, see [Tax service](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/tax-service-preview).</span></span>
- <span data-ttu-id="d01db-114">マルチコンポーネント機能のライフサイクル管理を簡素化し、アクションを構成し、機能パラメーターを設定するための追加機能を提供する、新しいグローバリゼーション機能のサポート。</span><span class="sxs-lookup"><span data-stu-id="d01db-114">Support for new globalization feature functionality that simplifies the lifecycle management of multi-component features and provides extra capability to configure actions and set up feature parameters.</span></span> <span data-ttu-id="d01db-115">詳細については、[Regulatory Configuration Service – グローバリゼーション サービスに対する簡素化されたグローバリゼーション機能の管理](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-115">For more information, see [Regulatory Configuration Service – simplified globalization feature management for globalization services](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services).</span></span>
- <span data-ttu-id="d01db-116">Microsoft Dynamics Lifecycle Services (LCS) を使用せずに構成管理を簡素化するための、グローバル リポジトリでのカスタム構成の集中公開、保存、および共有のサポート。</span><span class="sxs-lookup"><span data-stu-id="d01db-116">Support for centralized publication, storage, and sharing of custom configurations in the Global repository to simplify configuration management without requiring the use of Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="access-rcs"></a><span data-ttu-id="d01db-117">アクセス RCS</span><span class="sxs-lookup"><span data-stu-id="d01db-117">Access RCS</span></span>

<span data-ttu-id="d01db-118">[Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/) から RCS に登録またはサインインできます。</span><span class="sxs-lookup"><span data-stu-id="d01db-118">You can sign up for or sign in to RCS from the [Regulatory Configuration Service page](https://marketing.configure.global.dynamics.com/).</span></span>

![RSC 登録/サインイン](media/202103_RCS%20Marketing%20page_updated_1.jpg)

<span data-ttu-id="d01db-120">**Regulatory Configuration Service** ページで、サービスの使用に関する追加の条件を確認して承認し、次のいずれかのボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="d01db-120">On the **Regulatory Configuration Service** page, review and accept the supplemental terms and conditions for use of the service, and then select one of the following buttons:</span></span>

- <span data-ttu-id="d01db-121">初めてサービスを利用するユーザーで、組織にサービス環境をプロビジョニングするためにビジネス メール アドレスを使用している場合に **登録** する</span><span class="sxs-lookup"><span data-stu-id="d01db-121">**Sign up** if you're a first-time user of the service, and you're using a business email address to provision your organization a service environment</span></span>
- <span data-ttu-id="d01db-122">サービスに以前にサインアップした、組織環境にアクセスしたい場合に **サインイン** する</span><span class="sxs-lookup"><span data-stu-id="d01db-122">**Sign in** if you've previously signed up for the service, and you want to access your organization environment</span></span>

## <a name="regional-availability"></a><span data-ttu-id="d01db-123">地域の可用性</span><span class="sxs-lookup"><span data-stu-id="d01db-123">Regional availability</span></span>

<span data-ttu-id="d01db-124">通常、RCS は次の地域で使用できます。</span><span class="sxs-lookup"><span data-stu-id="d01db-124">RCS is generally available in the following regions:</span></span>

- <span data-ttu-id="d01db-125">米国</span><span class="sxs-lookup"><span data-stu-id="d01db-125">United States</span></span>
- <span data-ttu-id="d01db-126">インド</span><span class="sxs-lookup"><span data-stu-id="d01db-126">India</span></span>
- <span data-ttu-id="d01db-127">フランス</span><span class="sxs-lookup"><span data-stu-id="d01db-127">France</span></span>
- <span data-ttu-id="d01db-128">ヨーロッパ</span><span class="sxs-lookup"><span data-stu-id="d01db-128">Europe</span></span>

<span data-ttu-id="d01db-129">地域の完全な一覧については [Dynamics 365 および Power Platform: 使用可能性、データの場所、言語、およびローカライズ](https://aka.ms/dynamics_365_international_availability_deck) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-129">For a complete list of regions, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/dynamics_365_international_availability_deck).</span></span>

## <a name="rcs-default-company"></a><span data-ttu-id="d01db-130">RCS 既定会社</span><span class="sxs-lookup"><span data-stu-id="d01db-130">RCS default company</span></span>

<span data-ttu-id="d01db-131">RCS で使用される設計時間機能は、すべての会社間で共有されます。</span><span class="sxs-lookup"><span data-stu-id="d01db-131">Design time functionality that is used in RCS is shared across all companies.</span></span> <span data-ttu-id="d01db-132">会社固有の機能はありません。</span><span class="sxs-lookup"><span data-stu-id="d01db-132">There is no company-specific functionality.</span></span> <span data-ttu-id="d01db-133">したがって、RCS 環境では 1 つの会社 **DAT** を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d01db-133">Therefore, we recommend that you use one company, **DAT**, with your RCS environment.</span></span>

<span data-ttu-id="d01db-134">ただし、場合によっては、ER 形式で特定の法人に関連するパラメーターを使用することが推奨されます。</span><span class="sxs-lookup"><span data-stu-id="d01db-134">However, in some scenarios, you might want to make ER formats use parameters that are related to a specific legal entity.</span></span> <span data-ttu-id="d01db-135">これらのシナリオでのみ、既定の会社の切り替え機能を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d01db-135">In these scenarios only, you should use the default company switcher.</span></span> <span data-ttu-id="d01db-136">例については、[法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-136">For an example, see [Configure ER format to use parameters that are specified per legal entity](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-configure-format.md).</span></span>

## <a name="related-rcs-documentation"></a><span data-ttu-id="d01db-137">関連する RCS ドキュメント</span><span class="sxs-lookup"><span data-stu-id="d01db-137">Related RCS documentation</span></span>

<span data-ttu-id="d01db-138">関連コンポーネントの詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-138">For more information about related components, see the following topics:</span></span>

- <span data-ttu-id="d01db-139">**RCS:**</span><span class="sxs-lookup"><span data-stu-id="d01db-139">**RCS:**</span></span>

    - [<span data-ttu-id="d01db-140">RCS で ER コンフィギュレーションを作成し、グローバル リポジトリにアップロードする</span><span class="sxs-lookup"><span data-stu-id="d01db-140">Create ER configurations in RCS and upload them to the Global repository</span></span>](rcs-global-repo-upload.md)

- <span data-ttu-id="d01db-141">**グローバル リポジトリ:**</span><span class="sxs-lookup"><span data-stu-id="d01db-141">**Global repository:**</span></span>

    - [<span data-ttu-id="d01db-142">ER コンフィギュレーションの作成 & グローバル リポジトリへのアップロード</span><span class="sxs-lookup"><span data-stu-id="d01db-142">Create ER configuration & upload to Global repo</span></span>](rcs-global-repo-upload.md)
    - [<span data-ttu-id="d01db-143">グローバル リポジトリ でのコンフィギュレーションの共有</span><span class="sxs-lookup"><span data-stu-id="d01db-143">Share configuration in Global repo</span></span>](rcs-global-repo-share-configuration.md)
    - [<span data-ttu-id="d01db-144">グローバル レポジトリの拡張フィルター処理</span><span class="sxs-lookup"><span data-stu-id="d01db-144">Enhanced filtering in Global repo</span></span>](enhanced-filtering-global-repo.md)
    - [<span data-ttu-id="d01db-145">ER コンフィギュレーションをグローバル リポジトリからダウンロードする</span><span class="sxs-lookup"><span data-stu-id="d01db-145">Download ER configurations from the Global repository</span></span>](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md)
    - [<span data-ttu-id="d01db-146">グローバル リポジトリのコンフィギュレーションを中止する</span><span class="sxs-lookup"><span data-stu-id="d01db-146">Discontinuing configurations in Global repo</span></span>](discontinuing-configurations-rcs-global-repo.md)
    - [<span data-ttu-id="d01db-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) 記憶域の廃止</span><span class="sxs-lookup"><span data-stu-id="d01db-147">Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation</span></span>](rcs-lcs-repo-dep-faq.md)

- <span data-ttu-id="d01db-148">**グローバリゼーション機能:**</span><span class="sxs-lookup"><span data-stu-id="d01db-148">**Globalization feature:**</span></span>

    - [<span data-ttu-id="d01db-149">Regulatory Configuration Service (RCS) - グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="d01db-149">Regulatory Configuration Service (RCS) - Globalization feature</span></span>](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-finance/regulatory-configuration-service-simplified-globalization-feature-management-globalization-services)


## <a name="troubleshooting-rcs-sign-up"></a><span data-ttu-id="d01db-150">RCS サインアップのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="d01db-150">Troubleshooting RCS sign-up</span></span>

<span data-ttu-id="d01db-151">サービス ページから RCS にサインアップすると、Azure Active Directory (Azure AD) に関連した問題が発生する 場合があります。</span><span class="sxs-lookup"><span data-stu-id="d01db-151">When you sign up for RCS from the service page, you might encounter an issue that is related to Azure Active Directory (Azure AD).</span></span> <span data-ttu-id="d01db-152">表示されるエラー メッセージは、RCS のサインアップが現在オフであり、サインアップ プロセスを完了する前に有効になっていることを示します。</span><span class="sxs-lookup"><span data-stu-id="d01db-152">The error message that you receive indicates that sign-up for RCS is currently turned off and must be turned on before you can complete the sign-up process.</span></span>

![RCS サインアップのエラー メッセージ](media/01_RCSSignUpError.jpg)

<span data-ttu-id="d01db-154">問題が発生するのは、アドホック サブスクリプションへのサインアップがブロックされ、`AllowAdHocSubscriptions` プロパティがテナントで有効になっている必要があるためです。</span><span class="sxs-lookup"><span data-stu-id="d01db-154">The issue occurs because you're blocked from signing up for ad-hoc subscriptions, and the `AllowAdHocSubscriptions` property must be enabled in your tenant.</span></span> 

- <span data-ttu-id="d01db-155">組織の Azure テナントを IT 部門が管理している場合は、その部門に問題を報告してください。</span><span class="sxs-lookup"><span data-stu-id="d01db-155">If your IT department manages your organization's Azure tenants, contact that department to report the issue.</span></span>
- <span data-ttu-id="d01db-156">ご自身が Azure テナントの管理を担当している場合は、[Azure Active Directory のセルフサービス登録とは](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings)の手順に従って問題を修正できます。</span><span class="sxs-lookup"><span data-stu-id="d01db-156">If you're responsible for managing your Azure tenants, you can fix the issues by following the steps in [What is self-service sign-up for Azure Active Directory](/azure/active-directory/enterprise-users/directory-self-service-signup#how-do-i-control-self-service-settings).</span></span>
