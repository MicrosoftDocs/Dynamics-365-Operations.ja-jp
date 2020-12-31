---
title: オンプレミス環境でのネットワーク プリンター デバイスのインストール
description: このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。
author: TJVass
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCorpNetPrinterList
audience: IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 5407963653b758e131d6e858d53787d113e6cd25
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685288"
---
# <a name="install-network-printer-devices-in-on-premises-environments"></a><span data-ttu-id="095af-103">オンプレミス環境でのネットワーク プリンター デバイスのインストール</span><span class="sxs-lookup"><span data-stu-id="095af-103">Install network printer devices in on-premises environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="095af-104">このトピックでは、Microsoft Dynamics 365 Finance + Operations (オンプレミス) のオンプレミス展開を既存のネットワーク プリンター デバイスに接続する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="095af-104">This topic explains how to connect an on-premises deployment of Microsoft Dynamics 365 Finance + Operations (on-premises) to existing network printer devices.</span></span> <span data-ttu-id="095af-105">オンプレミス アプリケーションでのネットワーク印刷は、Microsoft Windows Server 2016 の「[印刷およびドキュメント サービス](https://technet.microsoft.com/library/hh831468(v=ws.11).aspx)」機能でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="095af-105">Network printing in the on-premises application is supported by the [Print and Document Services](https://technet.microsoft.com/library/hh831468(v=ws.11).aspx) feature in Microsoft Windows Server 2016.</span></span> <span data-ttu-id="095af-106">この機能を使用すると、プリンター管理に関連するタスクを集中管理できます。</span><span class="sxs-lookup"><span data-stu-id="095af-106">This feature lets you centralize tasks that are related to printer management.</span></span> <span data-ttu-id="095af-107">印刷およびドキュメント サービスをインストールして構成するには、Application Object Server (AOS) のプライマリー インスタンスをホストするサーバーへの管理アクセス権が必要です。</span><span class="sxs-lookup"><span data-stu-id="095af-107">To install and configure Print and Document Services, you must have administrative access to the server that hosts the primary instance of Application Object Server (AOS).</span></span>

<span data-ttu-id="095af-108">ネットワーク印刷サービスの構成には、次の 2 つの役割があります。</span><span class="sxs-lookup"><span data-stu-id="095af-108">Two roles are associated with the configuration of network printing services:</span></span>

- <span data-ttu-id="095af-109">**サービス管理者** – この役割を持つ担当者は、インストールやプラットフォーム インフラストラクチャのコンポーネントのコンフィギュレーションを担当します。</span><span class="sxs-lookup"><span data-stu-id="095af-109">**Service Administrator** – The person who has this role is responsible for installing and configuring components of the platform infrastructure.</span></span> <span data-ttu-id="095af-110">従来、この役割は昇格したドメイン権限を持った Active Directory アカウントです。</span><span class="sxs-lookup"><span data-stu-id="095af-110">Traditionally, this role is an Active Directory account that has elevated domain privileges.</span></span> <span data-ttu-id="095af-111">Microsoft Windows Server のコンポーネントのインストールに必要な権限があります。</span><span class="sxs-lookup"><span data-stu-id="095af-111">It has enough privileges to install components of Microsoft Windows Server.</span></span>
- <span data-ttu-id="095af-112">**組織の管理者** – このロールを持つユーザーはアプリケーション セキュリティ権限を管理します。</span><span class="sxs-lookup"><span data-stu-id="095af-112">**Organization Administrator** – The person who has this role manages application security privileges.</span></span> <span data-ttu-id="095af-113">この Active Directory アカウントは、**システム管理者** ロールに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="095af-113">This Active Directory account is assigned to the **System Administrator** role.</span></span>

<span data-ttu-id="095af-114">組織の管理者がネットワーク プリンターの追加を開始する前に、サービス管理者はプライマリ AOS インスタンスをホストするサーバーに印刷およびドキュメント サービスをインストールして構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="095af-114">Before the organization administrator can begin to add network printers, the service administrator must install and configure Print and Document Services on the server that hosts the primary AOS instance.</span></span> <span data-ttu-id="095af-115">組織の管理者は、組み込みツールを使用してネットワーク プリンター デバイスの設定を開始できます。</span><span class="sxs-lookup"><span data-stu-id="095af-115">The organization administrator can then begin to use built-in tools to configure network printer devices.</span></span>

## <a name="install-and-configure-print-and-document-services"></a><span data-ttu-id="095af-116">印刷およびドキュメント サービスのインストールと構成</span><span class="sxs-lookup"><span data-stu-id="095af-116">Install and configure Print and Document Services</span></span>

<span data-ttu-id="095af-117">環境管理者は、このセクションの情報を使用してネットワーク印刷サービスを有効にします。</span><span class="sxs-lookup"><span data-stu-id="095af-117">The environment administrator uses the information in this section to enable network printing services.</span></span>

1. <span data-ttu-id="095af-118">[印刷およびドキュメント サービスのインストール](https://technet.microsoft.com/library/jj134159(v=ws.11).aspx)の手順に従って印刷およびドキュメント サービスをインストールします。</span><span class="sxs-lookup"><span data-stu-id="095af-118">Install Print and Document Services by following the instructions in [Install Print and Document Services](https://technet.microsoft.com/library/jj134159(v=ws.11).aspx).</span></span>
2. <span data-ttu-id="095af-119">次の手順に従って印刷およびドキュメント サービスをコンフィギュレーションします [印刷およびドキュメント サービスのコンフィギュレーション](https://technet.microsoft.com/library/jj134163(v=ws.11).aspx)。</span><span class="sxs-lookup"><span data-stu-id="095af-119">Configure Print and Document Services by following the instructions in [Configure Print and Document Services](https://technet.microsoft.com/library/jj134163(v=ws.11).aspx).</span></span>
3. <span data-ttu-id="095af-120">AXService アプリケーションをホストするために使用する各サーバーに対して、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="095af-120">Follow these steps for each server that is used to host the AXService application:</span></span>

    1. <span data-ttu-id="095af-121">ローカル サーバーで、**ローカル ユーザーとグループ** マネージャーを開始します。</span><span class="sxs-lookup"><span data-stu-id="095af-121">On the local server, start the **Local Users and Groups** manager.</span></span>
    2. <span data-ttu-id="095af-122">**グループ** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="095af-122">Select the **Groups** node.</span></span>
    3. <span data-ttu-id="095af-123">**出力演算子** を右クリックし、**グループへの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="095af-123">Right-click **Print Operators**, and then select **Add to Group**.</span></span>
    4. <span data-ttu-id="095af-124">グループに AXService アプリケーションを実行するために使用されるネットワーク Active Directory アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="095af-124">Add the network Active Directory account that is used to run the AXService application to the group.</span></span>
    5. <span data-ttu-id="095af-125">AXService ユーザー アカウントを使用してネットワーク プリンターをインストールします。</span><span class="sxs-lookup"><span data-stu-id="095af-125">Install network printers by using the AXService user account.</span></span> <span data-ttu-id="095af-126">このステップにより、プリンター ドライバーが AXService ユーザー アカウントで使用できることが保証されます。</span><span class="sxs-lookup"><span data-stu-id="095af-126">This step helps guarantee that the printer driver is available to the AXService user account.</span></span>
    6. <span data-ttu-id="095af-127">すべての接続が正しく構成されていることを確認するため、インストールされているプリンターのテスト ページを印刷します。</span><span class="sxs-lookup"><span data-stu-id="095af-127">Print a test page on the installed printers to make sure that all the connections are correctly configured.</span></span>
    7. <span data-ttu-id="095af-128">ユーザーのプロファイルが正しく読み込まれることを保証し、プリンターを参照できるようにするために、AXService アプリケーションを再起動します。</span><span class="sxs-lookup"><span data-stu-id="095af-128">Restart the AXService application to help guarantee that the user's profile is correctly loaded so that it can look up the printer driver.</span></span>

## <a name="manage-network-printers"></a><span data-ttu-id="095af-129">ネットワーク プリンターの管理</span><span class="sxs-lookup"><span data-stu-id="095af-129">Manage network printers</span></span>

<span data-ttu-id="095af-130">システム管理者は、このセクションの情報を使用してネットワーク プリンターを定義します。</span><span class="sxs-lookup"><span data-stu-id="095af-130">The system administrator uses the information in this section to define network printers.</span></span>

1. <span data-ttu-id="095af-131">**組織管理** \> **設定** \> **ネットワーク プリンター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="095af-131">Go to **Organization administration** \> **Setup** \> **Network printers**.</span></span>
2. <span data-ttu-id="095af-132">**ネットワーク プリンター** ページで、新しいプリンターを追加します。</span><span class="sxs-lookup"><span data-stu-id="095af-132">On the **Network printers** page, add new printers.</span></span> <span data-ttu-id="095af-133">各プリンターで、名前、説明、パス、およびステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="095af-133">For each printer, specify a name, description, path, and status.</span></span> <span data-ttu-id="095af-134">プリンター パスがインストールされているプリンターのネットワーク パスと一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="095af-134">Make sure that the printer path matches the network path of the installed printer.</span></span>

<span data-ttu-id="095af-135">**有効** とマークされている項目は、すぐにアプリケーションのユーザーによって利用できるようになるので、ネットワーク プリンター デバイスで文書スタイル レポートの印刷を開始できます。</span><span class="sxs-lookup"><span data-stu-id="095af-135">Items that are marked **Active** immediately become available to application users, so that they can begin to print document-style reports on network printer devices.</span></span>
