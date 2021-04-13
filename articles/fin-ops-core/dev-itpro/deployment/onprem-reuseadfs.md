---
title: 複数の環境への同じ AD FS インスタンスの再利用
description: このトピックでは、複数の Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。
author: faix
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: osfaixat
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 183750e10c985e7e0c9206cc9c8586c2d0c43227
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745323"
---
# <a name="reuse-the-same-ad-fs-instance-for-multiple-environments"></a><span data-ttu-id="6cbca-103">複数の環境への同じ AD FS インスタンスの再利用</span><span class="sxs-lookup"><span data-stu-id="6cbca-103">Reuse the same AD FS instance for multiple environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cbca-104">このトピックでは、複数の Microsoft Dynamics 365 Finance + Operations (オンプレミス) 環境で Active Directory フェデレーション サービス (AD FS) の同じインスタンスを使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-104">This topic explains how to use the same instance of Active Directory Federation Services (AD FS) in multiple Microsoft Dynamics 365 Finance + Operations (on-premises) environments.</span></span>

## <a name="setup"></a><span data-ttu-id="6cbca-105">段取り</span><span class="sxs-lookup"><span data-stu-id="6cbca-105">Setup</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6cbca-106">この手順では、[オンプレミス環境コンテンツの設定および展開](./setup-deploy-on-premises-environments.md) コンテンツの手順に従って 1 つの環境に対して以前に AD FS が既に構成されていることを前提にしています。</span><span class="sxs-lookup"><span data-stu-id="6cbca-106">This procedure assumes that you've previously configured AD FS for one environment by following the instructions in the [Set up and deploy on-premises environments](./setup-deploy-on-premises-environments.md) content.</span></span> <span data-ttu-id="6cbca-107">また、環境が問題なく実行されていることも前提としています。</span><span class="sxs-lookup"><span data-stu-id="6cbca-107">It also assumes that that environment is running without any issues.</span></span>

1. <span data-ttu-id="6cbca-108">AD FS マネージャーで、**AD FS** \> **アプリケーション グループ** に移動し、**Microsoft Dynamics 365 for Operations オンプレミス** を開きます。</span><span class="sxs-lookup"><span data-stu-id="6cbca-108">In AD FS Manager, go to **AD FS** \> **Application groups**, and open **Microsoft Dynamics 365 for Operations On-premises**.</span></span>
2. <span data-ttu-id="6cbca-109">**ネイティブ アプリケーション** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-109">In the **Native application** section, follow these steps:</span></span>

    1. <span data-ttu-id="6cbca-110">**Microsoft Dynamics 365 for Operations オンプレミス - ネイティブ アプリケーション** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF`) を追加します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-110">Open **Microsoft Dynamics 365 for Operations On-premises - Native application**, and add the redirect URI of the new environment (`https://ax.contoso.com/namespaces/AXSF`).</span></span>
    2. <span data-ttu-id="6cbca-111">**Microsoft Dynamics 365 for Operations オンプレミス - Financial Reporting - ネイティブ アプリケーション** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/FinancialReporting/ApplicationService/soap/`) を追加します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-111">Open **Microsoft Dynamics 365 for Operations On-premises - Financial Reporting - Native application**, and add the redirect URI of the new environment (`https://ax.contoso.com/FinancialReporting/ApplicationService/soap/`).</span></span>

3. <span data-ttu-id="6cbca-112">**Web API** セクションで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-112">In the **Web API** section, follow these steps:</span></span>

    1. <span data-ttu-id="6cbca-113">**Microsoft Dynamics 365 for Operations オンプレミス-Web API** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF` および `https://ax.contoso.com`) のエントリを 2 つ追加します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-113">Open **Microsoft Dynamics 365 for Operations On-premises - Web API**, and add two entries for the redirect URI of the new environment (`https://ax.contoso.com/namespaces/AXSF` and `https://ax.contoso.com`).</span></span>
    2. <span data-ttu-id="6cbca-114">**Microsoft Dynamics 365 for Operations オンプレミス - Financial Reporting Web API** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/FinancialReporting`) のエントリを 2 つ追加します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-114">Open **Microsoft Dynamics 365 for Operations On-premises - Financial Reporting Web API**, and add the redirect URI of the new environment (`https://ax.contoso.com/FinancialReporting`).</span></span>

4. <span data-ttu-id="6cbca-115">オプション : **サーバー** セクションで、**Microsoft Dynamics 365 for Operations オンプレミス - Retail** を開き、新しい環境のリダイレクト URI (`https://ax.contoso.com/namespaces/AXSF/`) を追加します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-115">Optional: In the **Server** section, open **Microsoft Dynamics 365 for Operations On-premises - Retail**, and add the redirect URI of the new environment (`https://ax.contoso.com/namespaces/AXSF/`).</span></span>
5. <span data-ttu-id="6cbca-116">オプション: 新しい環境向けの Warehouse Mobile App を、[オンプレミスでの Warehousing アプリのコンフィグレーション](./warehousing-for-on-premise-deployments.md) で次の手順に従って構成します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-116">Optional: Configure the warehouse mobile app for the new environment by following the instructions in [Configure the Warehousing app for on-premises deployments](./warehousing-for-on-premise-deployments.md) again.</span></span> <span data-ttu-id="6cbca-117">新しい環境 (`https://ax.contoso.com`) の URI を **リソース URL** 値として使用することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6cbca-117">Remember to use the URI of the new environment (`https://ax.contoso.com`) as the **Resource URL** value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6cbca-118">ワークフローおよびリテール デザイナー アプリケーションには、追加の構成は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="6cbca-118">No additional configuration is required for the workflow and retail designer applications.</span></span>

6. <span data-ttu-id="6cbca-119">新しい環境で、OpenID メタデータ エンドポイント (`https://<adfs-dns-name>/adfs/.well-known/openid-configuration`) に **AOS** ノードおよび **MR** ノードからアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6cbca-119">Verify that you can reach the OpenID metadata endpoint (`https://<adfs-dns-name>/adfs/.well-known/openid-configuration`) from the **AOS** and **MR** nodes in your new environment.</span></span> <span data-ttu-id="6cbca-120">自己署名付き証明書を使用している場合は、AD FS Secure Sockets Layer (SSL) 証明書を各ノードの信頼済みルート証明機関ストアにインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="6cbca-120">If you're using self-signed certificates, you might have to import the AD FS Secure Sockets Layer (SSL) certificate into the Trusted Root Certification Authorities store of each node.</span></span>
7. <span data-ttu-id="6cbca-121">Microsoft Dynamics Lifecycle Services (LCS) から新しい環境を配置し、配置構成を指定する場合は、以前の環境に対して指定したのと同じ AD FS OpenID メタデータ エンドポイントと AD FS OpenID 接続クライアント ID を使用していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="6cbca-121">When you deploy the new environment from Microsoft Dynamics Lifecycle Services (LCS) and are specifying the deployment configuration, make sure that you use the same AD FS OpenID metadata endpoint and AD FS OpenID connect client IDs that you specified for the previous environment.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]