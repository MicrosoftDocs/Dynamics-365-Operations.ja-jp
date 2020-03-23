---
title: Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) でオンプレミス プロジェクトを設定するプロセスについて説明します。
author: PeterRFriis
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 60373
ms.assetid: ''
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f37c0c1b4a558e0178c2b35039f4848e4a29184
ms.sourcegitcommit: 66eae22cd99e53fe8e4c6c94945ad8061b69a442
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/11/2020
ms.locfileid: "3117412"
---
# <a name="set-up-on-premises-projects-in-lifecycle-services-lcs"></a><span data-ttu-id="f4143-103">Lifecycle Services (LCS) でのオンプレミス プロジェクトの設定</span><span class="sxs-lookup"><span data-stu-id="f4143-103">Set up on-premises projects in Lifecycle Services (LCS)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4143-104">Microsoft Dynamics Lifecycle Services (LCS) を使用して、Dynamics 365 Finance + Operations (オンプレミス) のインスタンスを配置し更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4143-104">You must use Microsoft Dynamics Lifecycle Services (LCS) to deploy and update an instance of Dynamics 365 Finance + Operations (on-premises).</span></span> <span data-ttu-id="f4143-105">ボリューム ライセンス フローまたは Dynamics 価格リスト フローを通じてサーバーとユーザーのライセンスを購入した後は、 [Finance + Operations (オンプレミス) の購入](../../fin-ops/get-started/purchase-on-premises.md) を参照して、 Azure AD アカウントを作成、または既存の Azure AD アカウントを使用して、すべてのサインアップ手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="f4143-105">After you purchase a server and user license through the Volume Licensing flow or the Dynamics Price List flow, see the topic, [Buy Finance + Operations (on-premises)](../../fin-ops/get-started/purchase-on-premises.md), to create an Azure AD account or use an existing Azure AD account, and then complete all the sign-up steps.</span></span> <span data-ttu-id="f4143-106">ユーザーは LCS へリダイレクトされ、そこでオンプレミス実装プロジェクトがプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="f4143-106">You will be redirected to LCS, where an on-premises implementation project will be provisioned for you.</span></span>

 <span data-ttu-id="f4143-107">[![On-premises 実装プロジェクト](./media/lbd-proejcts-01.png)](./media/lbd-proejcts-01.png)</span><span class="sxs-lookup"><span data-stu-id="f4143-107">[![On-premises implementation project](./media/lbd-proejcts-01.png)](./media/lbd-proejcts-01.png)</span></span>

<span data-ttu-id="f4143-108">オンプレミス プロジェクトには、オンプレミス ソリューションの実装、保守、および運用に必要なすべてのツールがあります。</span><span class="sxs-lookup"><span data-stu-id="f4143-108">The on-premises project has all the tools that you require in order to implement, maintain, and operate an on-premises solution.</span></span> <span data-ttu-id="f4143-109">オンプレミス プロジェクトで使用可能なツールの一部を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f4143-109">Here are some of the tools that are available in the on-premises project:</span></span>

- <span data-ttu-id="f4143-110">**方法** – オンプレミスの方法は、顧客がオンプレミス プロジェクトを実装および管理するのに役立つベスト プラクティスを提供しています。</span><span class="sxs-lookup"><span data-stu-id="f4143-110">**Methodology** – The on-premises methodology provides best practices that will help customers implement and manage on-premises projects.</span></span>
- <span data-ttu-id="f4143-111">**ビジネス プロセス モデラー** - ビジネス プロセス モデラー (BPM) は、要件をキャプチャし、ギャップ分析に適合するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4143-111">**Business process modeler** – Business process modeler (BPM) is used to capture requirements and do fit gap analysis.</span></span>
- <span data-ttu-id="f4143-112">**クラウド ホスト環境** - クラウドホスト環境は、開発者の配置とトポロジの構築、およびオンプレミス ソリューションのための Dev Application Lifecycle Management(ALM) の完成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f4143-112">**Cloud-hosted environments** – Cloud-hosted environments are used to deploy developer and build topologies, and to complete Dev Application Lifecycle Management (ALM) for on-premises solutions.</span></span>
- <span data-ttu-id="f4143-113">**コードのアップグレード** - これらのツールを使用して、コードを新しいバージョンにアップグレードできます。</span><span class="sxs-lookup"><span data-stu-id="f4143-113">**Code upgrade** – These tools will help you upgrade code to a newer release.</span></span>
- <span data-ttu-id="f4143-114">**問題検索** – アプリケーションとプラットフォームの問題に関連する公開済の KB を検索します。</span><span class="sxs-lookup"><span data-stu-id="f4143-114">**Issue search** – Search for published KBs that are related to application and platform issues.</span></span>
- <span data-ttu-id="f4143-115">**ローカライズおよび翻訳** – 資産のローカライズおよび翻訳。</span><span class="sxs-lookup"><span data-stu-id="f4143-115">**Localization and translation** – Localize and translate assets.</span></span>
- <span data-ttu-id="f4143-116">**サポート** – ファイルおよびトラック がインシデントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="f4143-116">**Support** – File and track support incidents.</span></span>
- <span data-ttu-id="f4143-117">**プロジェクト ユーザー** – プロジェクトにユーザーを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f4143-117">**Project users** – Assign users to a project.</span></span>
- <span data-ttu-id="f4143-118">**プロジェクト設定** – コネクタ、プロジェクト名、組織ユーザー、ライセンス番号などのプロジェクトレベルの設定を編集します。</span><span class="sxs-lookup"><span data-stu-id="f4143-118">**Project settings** – Edit project-level settings, such as connectors, the project name, organization users, and the license number.</span></span>
- <span data-ttu-id="f4143-119">**アセット ライブラリ** - アセット ライブラリは、パッケージなどのさまざまなアセットのライブラリです。</span><span class="sxs-lookup"><span data-stu-id="f4143-119">**Asset library** – The Asset library is a library for various assets, such as packages.</span></span>
- <span data-ttu-id="f4143-120">**SharePoint のオンライン ライブラリ** – オンラインの Microsoft SharePoint ライブラリに接続します。</span><span class="sxs-lookup"><span data-stu-id="f4143-120">**SharePoint online library** – Connect to an online Microsoft SharePoint library.</span></span>

<span data-ttu-id="f4143-121">オンプレミス実装を開始するには、プロジェクトを正しくセットアップし、開発者とビルド環境を展開してから、サンドボックス環境と実稼働環境を展開する方法の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4143-121">To start your on-premises implementation, you must follow the steps in the methodology to correctly set up the project, deploy the developer and build environments, and then deploy sandbox and production environments.</span></span> <span data-ttu-id="f4143-122">展開に役立つように、2 つの環境スロットがオンプレミス プロジェクトにあらかじめ割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="f4143-122">To help you with deployments, two environment slots are pre-allocated to the on-premises project.</span></span> <span data-ttu-id="f4143-123">一方のスロットはサンドボックス環境用で、もう一方のスロットは実稼働環境用です。</span><span class="sxs-lookup"><span data-stu-id="f4143-123">One slot is for a sandbox environment, and the other slot is for a production environment.</span></span> <span data-ttu-id="f4143-124">これらのスロットは、サービス フロー中に使用され、パッケージが実稼働環境で適用される前にサンドボックス環境でテストされることを保証します。</span><span class="sxs-lookup"><span data-stu-id="f4143-124">These slots will be used during the Servicing flow to help guarantee that packages are tested in the sandbox environment before they are applied in the production environment.</span></span>
