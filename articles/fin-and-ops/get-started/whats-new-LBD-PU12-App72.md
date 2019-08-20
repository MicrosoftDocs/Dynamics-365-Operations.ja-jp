---
title: プラットフォーム更新プログラム 12 による Dynamics 365 for Finance and Operations, Enterprise Edition 7.2 のオンプレミス配置 (2018 年 3 月)
description: このトピックでは、プラットフォーム更新プログラム 12 による Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.2 の新機能または変更された機能について説明します。 この展開オプションは、2018 年 3 月に使用できるようになりました。
author: sericks007
manager: AnnBe
ms.date: 03/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.custom: ''
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: 8624f9f7eb3aa32a2d855d0c9e2ef4887dd441df
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863549"
---
# <a name="whats-new-or-changed-in-on-premises-deployments-of-dynamics-365-for-finance-and-operations-enterprise-edition-72-with-platform-update-12-march-2018"></a><span data-ttu-id="2b1b1-104">プラットフォーム更新プログラム 12 による Dynamics 365 for Finance and Operations, Enterprise Edition 7.2 のオンプレミス配置 (2018 年 3 月)</span><span class="sxs-lookup"><span data-stu-id="2b1b1-104">What's new or changed in on-premises deployments of Dynamics 365 for Finance and Operations, Enterprise edition 7.2 with platform update 12 (March 2018)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b1b1-105">このトピックでは、プラットフォーム更新プログラム 12 による Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.2 の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-105">This topic describes features that are either new or changed in on-premises deployments of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.2 with platform update 12.</span></span> <span data-ttu-id="2b1b1-106">この展開オプションは、2018 年 3 月に使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-106">This deployment option became available in March 2018.</span></span>

<span data-ttu-id="2b1b1-107">プラットフォーム更新プログラム 12 の詳細については、[Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 の新機能または変更された機能について](whats-new-platform-update-12.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-107">For more information about platform update 12, see [What's new or changed in Dynamics 365 for Finance and Operations, Enterprise edition platform update 12](whats-new-platform-update-12.md).</span></span>

<span data-ttu-id="2b1b1-108">オンプレミス配置のリソースについては、[オンプレミス配置のホーム ページ](../../dev-itpro/deployment/on-premises-deployment-landing-page.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-108">For more resources about on-premises deployments, see [On-premises deployment home page](../../dev-itpro/deployment/on-premises-deployment-landing-page.md).</span></span>

## <a name="setup-and-deployment"></a><span data-ttu-id="2b1b1-109">設定と配置</span><span class="sxs-lookup"><span data-stu-id="2b1b1-109">Setup and deployment</span></span>

<span data-ttu-id="2b1b1-110">セットアップおよび配置プロセスが強化されました。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-110">Improvements have been made to the setup and deployment process.</span></span> <span data-ttu-id="2b1b1-111">これらの改良により、展開に必要な時間が大幅に短縮されます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-111">These improvements significantly reduce the time that is required for deployment.</span></span> <span data-ttu-id="2b1b1-112">信頼性を向上させるために、自動処理の強化および複数の前提条件の検証も追加されました。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-112">Increased automation and multiple prerequisite validations have also been added to improve reliability.</span></span> <span data-ttu-id="2b1b1-113">詳細については、[オンプレミス環境の設定と配置 (プラットフォーム更新プログラム 12)](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-113">For more information, see [Set up and deploy on-premises environments (Platform update 12)](../../dev-itpro/deployment/setup-deploy-on-premises-pu12.md).</span></span>

## <a name="servicing"></a><span data-ttu-id="2b1b1-114">サービス</span><span class="sxs-lookup"><span data-stu-id="2b1b1-114">Servicing</span></span>

<span data-ttu-id="2b1b1-115">オンプレミス環境が配置されると、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft からリリースされたプラットフォームおよびアプリケーションの更新プログラムを適用できます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-115">After your on-premises environment is deployed, you can now use Microsoft Dynamics Lifecycle Services (LCS) to apply platform and application updates that Microsoft releases.</span></span> <span data-ttu-id="2b1b1-116">また、コードのカスタマイズを適用することもできます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-116">You can also apply code customizations.</span></span> <span data-ttu-id="2b1b1-117">したがって、顧客は最新の修正プログラムを最新の状態に保ち、既存の環境を再構成したり、オンプレミス環境を再配置することなく、新しいカスタマイズを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-117">Therefore, customers can stay current with the latest set of fixes and take up new customizations without having to reconfigure an existing environment or redeploy the on-premises environment.</span></span> <span data-ttu-id="2b1b1-118">また、パッケージが正常に適用されなかった場合に、コード変更をロール バックできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-118">Additionally, you can now roll back code changes if packages aren't successfully applied.</span></span> <span data-ttu-id="2b1b1-119">詳細については、[オンプレミス配置への更新プログラムの適用](../../dev-itpro/deployment/apply-updates-on-premises.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-119">For more information, see [Apply updates to an on-premises deployment](../../dev-itpro/deployment/apply-updates-on-premises.md).</span></span>

<span data-ttu-id="2b1b1-120">[再構成機能](../../dev-itpro/lifecycle-services/reconfigure-environment.md)は、プラットフォーム更新プログラム 12 以前のバージョンで配置された環境でも使用可能であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-120">Note that the [Reconfigure feature](../../dev-itpro/lifecycle-services/reconfigure-environment.md) will remain available for environments that were deployed with platform update versions that are earlier than Platform update 12.</span></span>

## <a name="hotfixes"></a><span data-ttu-id="2b1b1-121">修正プログラム</span><span class="sxs-lookup"><span data-stu-id="2b1b1-121">Hotfixes</span></span>

<span data-ttu-id="2b1b1-122">LCS からダウンロードできる修正プログラムは、プラットフォーム更新プログラム 12 のオンプレミス配置に関する追加の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-122">Hotfixes that you can download from LCS provide additional features for your on-premises deployments of Platform update 12.</span></span> <span data-ttu-id="2b1b1-123">次の修正プログラムを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-123">Be sure to apply the following hotfixes:</span></span>

- <span data-ttu-id="2b1b1-124">**[KB 4091763 - 管理者がクライアントの接続と Skype プレゼンスを切り替える](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=fd949f8a204ceeedaa0a586ca8a1bfdbd6535b35225da98506d688e093d086f6):** この修正プログラムにより、管理者はクライアント マシンのインターネット接続に依存するエクスペリエンスを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-124">**[KB 4091763 - Admin toggles for Client connectivity and Skype presence](https://fix.lcs.dynamics.com/Issue/Details?kb=4091763&bugId=3934773&qc=fd949f8a204ceeedaa0a586ca8a1bfdbd6535b35225da98506d688e093d086f6):** This hotfix enables administrators to disable experiences that depend on internet connectivity on client machines.</span></span> <span data-ttu-id="2b1b1-125">詳細については、「[クライアント インターネット接続](../../dev-itpro/user-interface/client-disconnected.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-125">For more information, see [Client internet connection](../../dev-itpro/user-interface/client-disconnected.md).</span></span>
- <span data-ttu-id="2b1b1-126">**[KB 4093454 - オンプレミスの ISV ライセンス サポート](https://fix.lcs.dynamics.com/Issue/Details?kb=4093454&bugId=3936799&qc=766427475435463a174e287b531401ab8cc8f1aeedf12bf2c2d4f8d1a1774592):** プラットフォーム更新プログラム 12 から開始するオンプレミス環境を配置する場合、テナント GUID は LCS からオンプレミス環境に自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-126">**[KB 4093454 - ISV license support for on-premises](https://fix.lcs.dynamics.com/Issue/Details?kb=4093454&bugId=3936799&qc=766427475435463a174e287b531401ab8cc8f1aeedf12bf2c2d4f8d1a1774592):** When deploying an on-premises environment starting from platform update 12, the tenant GUID is automatically populated from LCS to the on-prem environment.</span></span> <span data-ttu-id="2b1b1-127">ライセンス供与の検証では次の値を読み取り、正常にライセンスを検証できます。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-127">Licensing validation can read this value and successfully validate the licenses.</span></span> <span data-ttu-id="2b1b1-128">詳細については、[ISV ライセンス (オンプレミス)](../../dev-itpro/dev-tools/isv-licensing-on-prem.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2b1b1-128">For more information, see [ISV licensing (on-premises)](../../dev-itpro/dev-tools/isv-licensing-on-prem.md).</span></span>
