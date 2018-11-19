---
title: "オンプレミス環境での小売チャネルのコンポーネントのインストール手順"
description: "このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。"
author: aamirallaqaband
manager: AnnBe
ms.date: 11/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: b8fb8c963e2bba2e6fe7cb31e71a38232f1e8a54
ms.openlocfilehash: 5b7edf0d9beb50480f2c75a591a83ea1030055af
ms.contentlocale: ja-jp
ms.lasthandoff: 11/02/2018

---

# <a name="installation-steps-for-retail-channel-components-in-an-on-premises-environment"></a><span data-ttu-id="c4348-103">オンプレミス環境での小売チャネルのコンポーネントのインストール手順</span><span class="sxs-lookup"><span data-stu-id="c4348-103">Installation steps for Retail channel components in an on-premises environment</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c4348-104">このトピックでは、オンプレミス環境での小売チャネルのコンポーネントのインストール手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="c4348-104">This topic covers the installation steps for Retail channel components in an on-premises environment.</span></span>

## <a name="overview"></a><span data-ttu-id="c4348-105">概要</span><span class="sxs-lookup"><span data-stu-id="c4348-105">Overview</span></span>

<span data-ttu-id="c4348-106">オンプレミス環境では、小売チャネル機能は Retail Store Scale Unit の使用により排他的に有効になります。</span><span class="sxs-lookup"><span data-stu-id="c4348-106">Retail channel functionality, in an on-premises environment, is enabled exclusively via use of Retail Store Scale Unit.</span></span> <span data-ttu-id="c4348-107">Retail Store Scale Unit の概要については、[Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4348-107">For an overview of Retail Store Scale Unit, see [Retail Store Scale Unit](../../retail/dev-itpro/retail-store-system-begin.md).</span></span> 

<span data-ttu-id="c4348-108">クラウド展開とは異なり、オンプレミス環境では Lifecycle Services (LCS) 経由で小売チャネル コンポーネントのシームレスで可用性の高い展開は有効になりません。</span><span class="sxs-lookup"><span data-stu-id="c4348-108">Unlike a cloud deployment, an on-premises environment does not enable seamless, high-availability deployment of Retail channel components via Lifecycle Services (LCS).</span></span> <span data-ttu-id="c4348-109">Retail Store Scale Unit をインストールすることによってのみ、小売チャネル コンポーネントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4348-109">The only way to use Retail channel components is by installing Retail Store Scale Unit.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c4348-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="c4348-110">Prerequisites</span></span> 

<span data-ttu-id="c4348-111">小売チャネル コンポーネントのインストールを開始する前に、まずオンプレミス環境のすべての事前インストール手順を完了してください。</span><span class="sxs-lookup"><span data-stu-id="c4348-111">Before you can start installation of Retail channel components, you must first complete all prior installation steps for an on-premises environment.</span></span> <span data-ttu-id="c4348-112">この手順は、[オンプレミス環境の設定と配置 (Platform update 12 以降)](setup-deploy-on-premises-pu12.md)で説明されています。</span><span class="sxs-lookup"><span data-stu-id="c4348-112">These steps are listed in [Set up and deploy on-premises environments (Platform update 12 and later)](setup-deploy-on-premises-pu12.md).</span></span>

<span data-ttu-id="c4348-113">必ず、セキュリティで保護されたネットワークを使用して、Retail Store Scale Unit (RSSU) を、パブリックにアクセスできない小売用バック オフィスに接続するようにもしてください。</span><span class="sxs-lookup"><span data-stu-id="c4348-113">You must also ensure that you use a secure network to connect Retail Store Scale Unit (RSSU) to Retail headquarters that is not publicly  accessible.</span></span> <span data-ttu-id="c4348-114">さらに、小売用バックオフィスへのネットワーク アクセスを、ネットワーク フィルタリングやその他の方法を介した既知の RSSU デバイスのみに制限してください。</span><span class="sxs-lookup"><span data-stu-id="c4348-114">You must also restrict network access to Retail headquarters only to known RSSU devices via network filtering or other means.</span></span>

## <a name="installation-steps"></a><span data-ttu-id="c4348-115">インストール手順</span><span class="sxs-lookup"><span data-stu-id="c4348-115">Installation steps</span></span>

1.  <span data-ttu-id="c4348-116">以前に作成したファイル共有で、**RetailSelfServicePackages** と呼ばれる新しいフォルダーを作成します。</span><span class="sxs-lookup"><span data-stu-id="c4348-116">On the previously created file share, create a new folder called **RetailSelfServicePackages**.</span></span>
2.  <span data-ttu-id="c4348-117">各 AOS コンピューターで、次の PowerShell スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="c4348-117">On each AOS computer, run the following PowerShell script:</span></span>

```powershell
.\RetailUpdateDatabase.ps1 -DatabaseServer '<Database server name for AOS database -DatabaseName 'Database name for AOS database ' -envName '<Environment name>' -RetailSelfServicePackages '<Local path of Retail self-service packages>’ -SendProductSupportTelemetryToMicrosoft <True/False>
```
  
3.  <span data-ttu-id="c4348-118">LCS からバイナリ更新プログラムをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="c4348-118">Download the binary update from LCS.</span></span> <span data-ttu-id="c4348-119">手順については、[Lifecycle Services (LCS) から更新プログラムを入手](../migration-upgrade/download-hotfix-lcs.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4348-119">For instructions, see [Get updates from Lifecycle Services (LCS)](../migration-upgrade/download-hotfix-lcs.md).</span></span>
4.  <span data-ttu-id="c4348-120">zip ファイルを展開し、上記のファイル共有の場所に作成した RetailSelfServicePackages フォルダーにある ModenPOSSetup.exe および StoreSystemSetup.exe をコピーします。</span><span class="sxs-lookup"><span data-stu-id="c4348-120">Extract the zip file and copy ModenPOSSetup.exe and StoreSystemSetup.exe found in the RetailSelfServicePackages folder that was created in the file share location above.</span></span>
5.  <span data-ttu-id="c4348-121">Retail Store Scale Unit をインストールするためのインストール手順に従います。</span><span class="sxs-lookup"><span data-stu-id="c4348-121">Follow the installation steps for installing the Retail Store Scale Unit.</span></span> <span data-ttu-id="c4348-122">手順については、[Retail Store Scale Unit のコンフィギュレーションとインストール](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c4348-122">For instructions, see [Configure and install Retail Store Scale Unit](../../retail/dev-itpro/retail-store-scale-unit-configuration-installation.md).</span></span>


