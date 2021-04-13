---
title: セルフサービス配置に関する既知の問題
description: このトピックでは、セルフ サービス配置を使用する場合に発生する可能性がある既知の問題を一覧表示します。
author: rashmansur
manager: AnnBe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: e1efada0dd3f3d012ba3d96978a62eb05ac276c5
ms.sourcegitcommit: 3f2bcb8745e826efcf3d82194e1cb2a41e7e0bf2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5770148"
---
# <a name="known-issues-with-self-service-deployment"></a><span data-ttu-id="f67e8-103">セルフサービス配置に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="f67e8-103">Known issues with self-service deployment</span></span>

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="f67e8-104">このトピックでは、[セルフ サービス配置](infrastructure-stack.md)の既知の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="f67e8-104">This topic describes the known issues with [self-service deployment](infrastructure-stack.md).</span></span>

## <a name="lifecycle-services-lcs"></a><span data-ttu-id="f67e8-105">Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="f67e8-105">Lifecycle Services (LCS)</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="f67e8-106">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="f67e8-106">Features not intended to be implemented</span></span>
<span data-ttu-id="f67e8-107">次の LCS 機能は、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-107">The following LCS features will not be implemented in self-service deployment.</span></span>

- <span data-ttu-id="f67e8-108">**システム診断** - 現在のシステム診断によって提供されるすべてのデータと機能は、製品と LCS のその他の機能を通じて使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-108">**System diagnostics** - All data and functionality provided by system diagnostics today will be available through other features in the product and LCS.</span></span> 
 - <span data-ttu-id="f67e8-109">**サービス要求** - サービス要求は、セルフ サービス アクションに置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f67e8-109">**Service requests** - Service requests are being replaced with self-service actions.</span></span> 

### <a name="known-issues-in-this-release"></a><span data-ttu-id="f67e8-110">このリリースの既知の問題</span><span class="sxs-lookup"><span data-stu-id="f67e8-110">Known issues in this release</span></span>
<span data-ttu-id="f67e8-111">既知の問題は、将来のリリースで解決されるバグです。</span><span class="sxs-lookup"><span data-stu-id="f67e8-111">Know issues are bugs that will be addressed in upcoming releases.</span></span> <span data-ttu-id="f67e8-112">2 週間おきに LCS の新しいリリースがあります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-112">Every 2 weeks there is a new release of LCS.</span></span>

## <a name="finance-and-operations-apps"></a><span data-ttu-id="f67e8-113">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="f67e8-113">Finance and Operations apps</span></span> 

> [!NOTE]
> <span data-ttu-id="f67e8-114">Dynamics 365 Commerce は、10.0.10 リリースを使用した最新の配置エクスペリエンスに実装されています。</span><span class="sxs-lookup"><span data-stu-id="f67e8-114">Dynamics 365 Commerce is implemented in the modern deployment experience with the 10.0.10 release.</span></span> <span data-ttu-id="f67e8-115">詳細については、[セルフサービス配置でのアプリケーション エクスプローラー用支払パッケージの作成](../../../commerce/dev-itpro/payment-connector-package.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-115">For more information, see [Create payment packaging for Application Explorer for self-service deployment](../../../commerce/dev-itpro/payment-connector-package.md).</span></span>

### <a name="features-not-intended-to-be-implemented"></a><span data-ttu-id="f67e8-116">実装が意図されていない機能</span><span class="sxs-lookup"><span data-stu-id="f67e8-116">Features not intended to be implemented</span></span>
<span data-ttu-id="f67e8-117">次の機能は、セルフ サービス配置では実装されません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-117">The following feature will not be implemented in self-service deployment.</span></span>

- <span data-ttu-id="f67e8-118">**カスタム フォント** - カスタム フォントはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-118">**Custom fonts** - Custom fonts are not supported.</span></span> <span data-ttu-id="f67e8-119">詳細については、[Dynamics 365 アプリケーションのドキュメント レポート サービス](../analytics/reporting-experience-iias-environments.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-119">For more information, see [Document Reporting Service in Dynamics 365 applications](../analytics/reporting-experience-iias-environments.md).</span></span>
- <span data-ttu-id="f67e8-120">**セルフサービスのユーザー インターフェイス (UI) コンポーネントに関連したカスタマイズ** - Finance and Operations アプリで標準の Financial Reporting または SQL Server Reporting Services (SSRS) を使用しないカスタマイズは、多くの場合、AOS が実行されているオペレーティング システムの UI コンポーネントに依存します。</span><span class="sxs-lookup"><span data-stu-id="f67e8-120">**Customizations related to user interface (UI) components on self service** - Customizations that do not use the standard Financial Reporting or SQL Server Reporting Services (SSRS) in Finance and Operations apps often take a dependency on UI components of the operating system where the AOS runs.</span></span> <span data-ttu-id="f67e8-121">依存関係の例としては、Windows フォント、Internet Explorer などの Web ブラウザー、またはカスタム PDF レンダリングなどがあります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-121">Example dependencies include Windows fonts, web browsers such as Internet Explorer, or custom PDF rendering.</span></span> <span data-ttu-id="f67e8-122">ホスト オペレーティング システムに、フォント インフラストラクチャ、Web ブラウザー、または一般的な UI コンポーネントのサポートが含まれることを保証するものではありません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-122">We do not ensure the host operating system will include any support for font infrastructure, web browsers, or any general UI components.</span></span> <span data-ttu-id="f67e8-123">セルフサービス インフラストラクチャに移行すると、ホスト オペレーティング システムが変更されます。</span><span class="sxs-lookup"><span data-stu-id="f67e8-123">The host operating system will change when migrating to self-service infrastructure.</span></span> <span data-ttu-id="f67e8-124">このような依存関係があり他にご質問がある場合は、Microsoft サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-124">If you have such dependencies and have additional questions, please contact Microsoft Support.</span></span>

### <a name="features-no-longer-supported"></a><span data-ttu-id="f67e8-125">サポートされなくなった機能</span><span class="sxs-lookup"><span data-stu-id="f67e8-125">Features no longer supported</span></span>
<span data-ttu-id="f67e8-126">次の機能は、セルフ サービス配置ではサポートされなくなりました。</span><span class="sxs-lookup"><span data-stu-id="f67e8-126">The following feature is no longer supported with self-service deployment.</span></span>

#### <a name="ftp"></a><span data-ttu-id="f67e8-127">FTP</span><span class="sxs-lookup"><span data-stu-id="f67e8-127">FTP</span></span>
<span data-ttu-id="f67e8-128">FTP に依存するカスタマイズは、セルフサービスの配置ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-128">Customizations relying on FTP are not supported with self-service deployment.</span></span> <span data-ttu-id="f67e8-129">次の情報を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-129">You should consider the following information:</span></span>

- <span data-ttu-id="f67e8-130">Application Object Server (AOS) からの送信要求すべてが静的 IP アドレス上にあることを保証するものではありません。</span><span class="sxs-lookup"><span data-stu-id="f67e8-130">We do not ensure that all outbound requests from an Application Object Server (AOS) are on a static IP address.</span></span> 

- <span data-ttu-id="f67e8-131">2021 年 6 月まで、特定の AOS セッション中のすべての発信要求が同じ IP アドレスに設定されます。</span><span class="sxs-lookup"><span data-stu-id="f67e8-131">Until June 2021, we will ensure that all outbound requests during a particular AOS session will be on the same IP address.</span></span> <span data-ttu-id="f67e8-132">これは、FTP などの一部のプロセスに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-132">This can have implications for some processes, such as FTP.</span></span> <span data-ttu-id="f67e8-133">Power Apps を使用してファイルを引き出し、Finance and Operations アプリに API 呼び出しを実行して、データ統合フレームワークを使用してファイルをインポートすることにより、FTP の使用を除去することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f67e8-133">We recommend removing the use of FTP by using Power Apps to pull the files in and make API calls into Finance and Operations apps to import the files using the Data Integration framework.</span></span> <span data-ttu-id="f67e8-134">詳細については、[データ エンティティ統合の概要](../data-entities/integration-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-134">For more information, see [Data entities integration overview](../data-entities/integration-overview.md).</span></span> <span data-ttu-id="f67e8-135">特定の例には以下が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f67e8-135">Some specific examples include:</span></span>

  - <span data-ttu-id="f67e8-136">([Azure Logic App での SFTP ファイルの監視、作成、および管理で説明されているように](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp))、ネイティブの SFTP コネクタを使用します。そのために、オン プレミス サービスを呼び出すためにファイアウォールでいくつかのポートを開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="f67e8-136">Use the native SFTP connector (as described in [Monitor, create, and manage SFTP files in Azure Logic Apps](https://docs.microsoft.com/azure/connectors/connectors-create-api-sftp)), which still requires some port opening on the firewall to call the on-premises service.</span></span> <span data-ttu-id="f67e8-137">Logic Apps の場合、IP のリストは、全体の[地域の許可リスト ](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound)および [Power Automate での制限と構成](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps)よりもはるかに短いことを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-137">Consider that for Logic Apps, the list of IPs is much shorter than the entire [region allowlist](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) and the [limits and configuration in Power Automate](https://docs.microsoft.com/power-automate/limits-and-config#logic-apps).</span></span>

  - <span data-ttu-id="f67e8-138">[発信 IP アドレス](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound) の説明に従って、オンプレミスのデータ ゲートウェイと組み合わせて、「ローカル ファイルシステム」コネクタを使用します。</span><span class="sxs-lookup"><span data-stu-id="f67e8-138">Use the “Local Filesystem” connector, as described in [Outbound IP addresses](https://docs.microsoft.com/azure/logic-apps/logic-apps-limits-and-config#outbound), in combination with the on-premises data gateway.</span></span> <span data-ttu-id="f67e8-139">詳細については、[Azure Logic Apps のオンプレミス データ ゲートウェイのインストール](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-139">For more information, see [Install on-premises data gateway for Azure Logic Apps](https://docs.microsoft.com/azure/logic-apps/logic-apps-gateway-install).</span></span> <span data-ttu-id="f67e8-140">このソリューションでは、非常に高いセキュリティ レベルを維持しながら、セルフサービス配置では非推奨の IP 許可リストの必要性を完全に排除します。</span><span class="sxs-lookup"><span data-stu-id="f67e8-140">This solution completely removes the need for the IP allowlist, which is deprecated in self-service deployment, while keeping a very high-level of security.</span></span>

  - <span data-ttu-id="f67e8-141">セルフサービス機能: セルフサービス機能への移行後に FTP シナリオが失敗した場合は、FTP サーバーのコンフィギュレーションを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-141">Self-service capabilities:  If FTP scenarios are failing after migrating to self-service capabilities, review the configuration at the FTP server.</span></span> <span data-ttu-id="f67e8-142">最も一般的なシナリオは、許可された [IP リスト](deploymentFAQ.md#for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment)をセルフサービス環境の範囲で更新する必要があることです。</span><span class="sxs-lookup"><span data-stu-id="f67e8-142">The most common scenario is the need to update the allowed [IP list](deploymentFAQ.md#for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment) with the ranges for self-service environments.</span></span>

> [!NOTE]
> <span data-ttu-id="f67e8-143">非推奨機能の詳細については、[削除済みまたは非推奨のプラットフォーム機能](../get-started/removed-deprecated-features-platform-updates.md)および[以前のリリースの削除済みまたは非推奨の機能](../migration-upgrade/deprecated-features.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f67e8-143">For more information about deprecated features, see [Removed or deprecated platform features](../get-started/removed-deprecated-features-platform-updates.md) and [Removed or deprecated features from previous releases](../migration-upgrade/deprecated-features.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
