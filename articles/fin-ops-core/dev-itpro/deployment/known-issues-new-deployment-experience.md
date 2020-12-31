---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: f9345aa54995608e496cf53b8bd21f20edbd9d36
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679284"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="d657b-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="d657b-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="d657b-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="d657b-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="d657b-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="d657b-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="d657b-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="d657b-106">Features not intended to be implemented</span></span>
<span data-ttu-id="d657b-107">次の LCS 機能は、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="d657b-107">The following LCS features will not be implemented in self-service deployment.</span></span>

- <span data-ttu-id="d657b-108">**システム診断** - 現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="d657b-108">**System diagnostics** - All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> 
 - <span data-ttu-id="d657b-109">**サービス要求** - サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="d657b-109">**Service requests** - Service requests are being replaced with self-service actions.</span></span> 

### <a name="known-issues-in-this-release"></a><span data-ttu-id="d657b-110">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="d657b-110">Known issues in this release</span></span>
<span data-ttu-id="d657b-111">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="d657b-111">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="d657b-112">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="d657b-112">Every 2 weeks there is a new release of LCS.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="d657b-113">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="d657b-113">Finance and Operations apps</span></span> 

> [!NOTE]
> <span data-ttu-id="d657b-114">Dynamics 365 Commerce は、10.0.10 リリースを使用した最新の配置エクスペリエンスに実装されています。</span><span class="sxs-lookup"><span data-stu-id="d657b-114">Dynamics 365 Commerce is implemented in the modern deployment experience with the 10.0.10 release.</span></span> <span data-ttu-id="d657b-115">詳細については、[セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-115">For more information, see [Create payment packaging for Application Explorer for self-service deployment](../../../commerce/dev-itpro/payment-connector-package.md).</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="d657b-116">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="d657b-116">Features not intended to be implemented</span></span>
<span data-ttu-id="d657b-117">次の機能は、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="d657b-117">The following feature will not be implemented in self-service deployment.</span></span>

- <span data-ttu-id="d657b-118">**カスタム フォント** - カスタム フォントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d657b-118">**Custom fonts** - Custom fonts are not supported.</span></span> <span data-ttu-id="d657b-119">詳細については、[Dynamics 365 アプリケーションのドキュメント レポート サービス](../analytics/reporting-experience-iias-environments.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-119">For more information, see [Document Reporting Service in Dynamics 365 applications](../analytics/reporting-experience-iias-environments.md).</span></span>
- <span data-ttu-id="d657b-120">**セルフサービスの UI コンポーネントに関連したカスタマイズ** - Finance and Operations アプリで標準の Financial Reporting または SQL Server Reporting Services (SSRS) を使用しないカスタマイズは、多くの場合、AOS が実行されているオペレーティング システムの UI コンポーネントに依存します。</span><span class="sxs-lookup"><span data-stu-id="d657b-120">**Customizations related to UI components on self service** - Customizations that do not use the standard Financial Reporting or SQL Server Reporting Services (SSRS) in Finance and Operations apps often take a dependency on UI components of the operating system where the AOS runs.</span></span> <span data-ttu-id="d657b-121">依存関係の例としては、Windows フォント、Internet Explorer などの Web ブラウザー、またはカスタム PDF レンダリングなどがあります。</span><span class="sxs-lookup"><span data-stu-id="d657b-121">Example dependencies include Windows fonts, web browsers such as Internet Explorer, or custom PDF rendering.</span></span> <span data-ttu-id="d657b-122">ホスト オペレーティング システムに、フォント インフラストラクチャ、Web ブラウザー、または一般的な UI コンポーネントのサポートが含まれることを保証するものではありません。</span><span class="sxs-lookup"><span data-stu-id="d657b-122">We do not ensure the host operating system will include any support for font infrastructure, web browsers, or any general UI components.</span></span> <span data-ttu-id="d657b-123">セルフサービス インフラストラクチャに移行すると、ホスト オペレーティング システムが変更されます。</span><span class="sxs-lookup"><span data-stu-id="d657b-123">The host operating system will change when migrating to self-service infrastructure.</span></span> <span data-ttu-id="d657b-124">このような依存関係があり他にご質問がある場合は、Microsoft サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="d657b-124">If you have such dependencies and have additional questions, please contact Microsoft support.</span></span>

### <a name="features-no-longer-supported"></a><span data-ttu-id="d657b-125">サポートされなくなった機能</span><span class="sxs-lookup"><span data-stu-id="d657b-125">Features no longer supported</span></span>
<span data-ttu-id="d657b-126">次の機能は、セルフ サービス配置ではサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d657b-126">The following feature is no longer supported with self-service deployment.</span></span>

#### <a name="ftp"></a><span data-ttu-id="d657b-127">FTP</span><span class="sxs-lookup"><span data-stu-id="d657b-127">FTP</span></span>
<span data-ttu-id="d657b-128">FTP に依存するカスタマイズは、セルフ サービス配置ではサポートされず、次のアクションを検討する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d657b-128">Customizations relying on FTP are not supported with self-service deployment and should consider the following actions.</span></span>

- <span data-ttu-id="d657b-129">**再試行の追加** - これは、短期から中期のオプションと見なす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d657b-129">**Add retries** - This should be viewed as a short to medium term option.</span></span> <span data-ttu-id="d657b-130">現在のインフラストラクチャ デザインによって、コントロールとデータ呼び出しに一致する IP が許可されます。</span><span class="sxs-lookup"><span data-stu-id="d657b-130">The current infrastructure design allows control and data calls to occasionally have matching IP.</span></span> <span data-ttu-id="d657b-131">このデザインは変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d657b-131">This design is subject to change.</span></span> 
- <span data-ttu-id="d657b-132">**コントロールおよび同じ IP からのデータに対する FTP 要求を無効にする** - この場合は、状況に応じてセキュリティの影響を慎重に評価します。</span><span class="sxs-lookup"><span data-stu-id="d657b-132">**Disabling the FTP requirement for control and data that is from the same IP** - Carefully evaluate the security implications for your situation in this case.</span></span>
- <span data-ttu-id="d657b-133">**FTP の使用を削除** - たとえば、Power Apps を使用してファイルを引き出し、Finance and Operations にアプリに API 呼び出しを実行して、データ統合フレームワークを使用してファイルをインポートします。</span><span class="sxs-lookup"><span data-stu-id="d657b-133">**Remove the use of FTP** - For example, use Power Apps to pull the files in and make API calls into Finance and Operations apps to import the files using the Data Integration framework.</span></span> <span data-ttu-id="d657b-134">詳細については、[データ統合戦略の選択](../data-entities/integration-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-134">For more information, see [Choose a data integration strategy](../data-entities/integration-overview.md).</span></span>
- <span data-ttu-id="d657b-135">**SFTP 使用** - 静的な発信 IP アドレスを使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="d657b-135">**Use SFTP** - We do not recommend using static outbound IP addresses.</span></span> <span data-ttu-id="d657b-136">詳細については、[Finance and Operations 静的 IP アドレス](https://community.dynamics.com/ax/b/axinthefield/posts/dynamics-365-for-finance-and-operations-static-ip-addresses) ブログの投稿を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-136">For more information, see the [Finance and Operations Static IP Addresses](https://community.dynamics.com/ax/b/axinthefield/posts/dynamics-365-for-finance-and-operations-static-ip-addresses) blog post.</span></span>

<span data-ttu-id="d657b-137">一般には、FTP の使用を解除することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="d657b-137">Our general recommendation is to remove the use of FTP.</span></span> <span data-ttu-id="d657b-138">Dynamics 365 から SFTP への直接接続は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="d657b-138">Do not use a direct connection from Dynamics 365 to an SFTP.</span></span> <span data-ttu-id="d657b-139">代わりに、2 つの間の Logic App を使用します。</span><span class="sxs-lookup"><span data-stu-id="d657b-139">Instead, use a Logic App in between the two.</span></span> <span data-ttu-id="d657b-140">Logic App では、次の 2 つのオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="d657b-140">With the Logic App you have two options:</span></span>

- <span data-ttu-id="d657b-141">([Azure Logic App での SFTP ファイルの監視、作成、および管理で説明されているように](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp))、ネイティブの SFTP コネクタを使用します。そのために、オン プレミス サービスを呼び出すためにファイアウォールでいくつかのポートを開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="d657b-141">Use the native SFTP connector (as described in [Monitor, create, and manage SFTP files in Azure Logic Apps](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp)), which still requires some port opening on the firewall to call the on-premises service.</span></span> <span data-ttu-id="d657b-142">Logic Apps の場合、IP のリスト、全体の[地域の許可リスト ](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) および [Power Automate での制限と構成](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps) よりもはるかに短いことを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-142">Consider that for Logic Apps, the list of IPs is much shorter than the entire [region allow list](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) and the [limits and configuration in Power Automate](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps).</span></span>

- <span data-ttu-id="d657b-143">[発信 IP アドレス](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) の説明に従って、オンプレミスのデータ ゲートウェイと組み合わせて、「ローカル ファイルシステム」コネクタを使用します。</span><span class="sxs-lookup"><span data-stu-id="d657b-143">Use the “Local Filesystem” connector, as described in [Outbound IP addresses](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound), in combination with the on-premises data gateway.</span></span> <span data-ttu-id="d657b-144">詳細については、[Azure Logic Apps のオンプレミス データ ゲートウェイのインストール](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-144">For more information, see [Install on-premises data gateway for Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install).</span></span> <span data-ttu-id="d657b-145">このソリューションでは、非常に高いレベルのセキュリティを維持しながら、セルフ サービス配置では非推奨の IP 許可リストは、完全に削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d657b-145">This solution completely removes the need for the IP allow list, which is deprecated in self-service deployment, while keeping a very high-level of security.</span></span>

> [!NOTE]
> <span data-ttu-id="d657b-146">非推奨の機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)、[以前のリリースからの削除済みおよび非推奨の機能](../migration-upgrade/deprecated-features.md)、[以前のリリースの削除済みおよび非推奨の機能](../get-started/removed-deprecated-features-platform-updates.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d657b-146">For more information about deprecated features, see [Removed or deprecated platform features](../get-started/removed-deprecated-features-platform-updates.md) and [Removed or deprecated features from previous releases](../migration-upgrade/deprecated-features.md) and [Removed or deprecated features in previous releases](../get-started/removed-deprecated-features-platform-updates.md).</span></span>
