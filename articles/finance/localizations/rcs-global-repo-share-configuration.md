---
title: 外部組織で RCS/グローバル レポジトリの ER 構成を共有する
description: このトピックでは、Microsoft Regulatory Configuration Service (RCS) 、またはグローバル レポジトリの電子レポート (ER) の構成を外部組織と直接共有する方法について説明します。
author: JaneA07
manager: AnnBe
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: e7ec24ddc532ee3b87108d076d5103538be903be
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218833"
---
# <a name="share-electronic-reporting-er-configurations-in-regulatory-configuration-services-rcs-global-repository-with-external-organizations"></a><span data-ttu-id="50243-103">Microsoft Regulatory Configuration Service (RCS) のグローバル レポジトリの電子レポート (ER) の構成を外部組織と共有する</span><span class="sxs-lookup"><span data-stu-id="50243-103">Share Electronic reporting (ER) configurations in Regulatory Configuration Services (RCS) Global repository with external organizations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50243-104">Microsoft Regulatory Configuration Service (RCS) を使用すると、電子レポート (ER) の構成を共有して外部組織に公開することができます。</span><span class="sxs-lookup"><span data-stu-id="50243-104">You can use Microsoft Regulatory Configuration Services (RCS) to share Electronic reporting (ER) configurations and then publish them to external organizations.</span></span>

<span data-ttu-id="50243-105">次の手順では、RCS のユーザーが RCS インスタンスで設定された ER 構成のバージョンを外部組織と共有する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="50243-105">The following procedures explain how an RCS user can share a version of an ER configuration that has been configured in an RCS instance with an external organization.</span></span> <span data-ttu-id="50243-106">この手順を完了する前に、まず以下の手順を完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="50243-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="50243-107">RCS インスタンスへのアクセス権。</span><span class="sxs-lookup"><span data-stu-id="50243-107">Access an RCS instance.</span></span>
- <span data-ttu-id="50243-108">有効な構成プロバイダーを作成する。</span><span class="sxs-lookup"><span data-stu-id="50243-108">Create an active configuration provider.</span></span> <span data-ttu-id="50243-109">詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50243-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
- <span data-ttu-id="50243-110">ER 構成の新しいバージョンを作成してアップロードします。</span><span class="sxs-lookup"><span data-stu-id="50243-110">Create and upload a new version of an ER configuration.</span></span> <span data-ttu-id="50243-111">詳細については、[新しいバージョンの電子レポート (ER) 構成の作成とアップロード](rcs-global-repo-upload.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50243-111">For more information, see [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

<span data-ttu-id="50243-112">また、RCS 環境がプロビジョニングされていることを確認しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="50243-112">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="50243-113">Finance and Operations アプリで、**組織管理** \> **ワークスペース** \> **電子レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="50243-113">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="50243-114">RCS 環境がご利用の会社にプロビジョニングされていない場合は、**Regulatory services – 外部の構成** を選択し、続いてプロビジョニングの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="50243-114">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="50243-115">RCS 環境が既にプロビジョニングされている場合は、[サインイン] オプションを選択して、ページの URL を使用してこの機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="50243-115">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="verify-the-configuration-that-you-want-to-share"></a><span data-ttu-id="50243-116">共有する構成を確認する</span><span class="sxs-lookup"><span data-stu-id="50243-116">Verify the configuration that you want to share</span></span>

<span data-ttu-id="50243-117">共有する構成が既にグローバル リポジトリにアップロードされていることを確認するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="50243-117">Follow these steps to verify that the configuration that you want to share has already been uploaded to the Global repository.</span></span>

1. <span data-ttu-id="50243-118">**電子レポート** ワークスペースで、超す営プロバイダーの **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-118">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>

    ![コンフィギュレーション プロバイダー](media/1_RCS_Repo_for_config_provider.JPG)

2. <span data-ttu-id="50243-120">**グローバル リポジトリ** \>**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-120">Select **Global repository** \> **Open**.</span></span>
3. <span data-ttu-id="50243-121">共有する構成を検索します。</span><span class="sxs-lookup"><span data-stu-id="50243-121">Search for the configuration that you want to share.</span></span> <span data-ttu-id="50243-122">フィルターのフィールドを使用して検索を絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="50243-122">You can use the filter field to narrow your search.</span></span> <span data-ttu-id="50243-123">グローバル リポジトリに構成が見つからない場合は、[新しいバージョンの電子レポート (ER) 構成の作成とアップロード](rcs-global-repo-upload.md)に記載の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="50243-123">If you can't find the configuration in the Global repository, follow the steps in [Create and upload a new version of an Electronic reporting (ER) configuration](rcs-global-repo-upload.md).</span></span>

## <a name="share-er-configurations-with-external-organizations"></a><span data-ttu-id="50243-124">ER の構成を外部の組織と共有する</span><span class="sxs-lookup"><span data-stu-id="50243-124">Share ER configurations with external organizations</span></span>

<span data-ttu-id="50243-125">構成プロバイダーの配下に構成が作成された後は、**グローバル構成リポジトリ** ページの **共有** クイックタブを使用して外部組織と直接共有することができます。</span><span class="sxs-lookup"><span data-stu-id="50243-125">After a configuration has been created under your configuration provider, you can share it directly with external organizations by using the **Shared with** FastTab on the **Global configuration repository** page.</span></span>

1. <span data-ttu-id="50243-126">**電子レポート** ワークスペースで、超す営プロバイダーの **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-126">In the **Electronic reporting** workspace, select **Repositories** for your configuration provider.</span></span>
2. <span data-ttu-id="50243-127">**グローバル リポジトリ** \>**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-127">Select **Global repository** \> **Open**.</span></span> 
3. <span data-ttu-id="50243-128">共有する構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-128">Select the configuration that you want to share.</span></span>
4. <span data-ttu-id="50243-129">**共有** クイック タブで、**組織** を選択します。</span><span class="sxs-lookup"><span data-stu-id="50243-129">On the **Shared with** FastTab, select **Organization**.</span></span>

    ![クイック タブで共有する](media/1_RCS_Repo_for_Share_with_org.JPG)

5. <span data-ttu-id="50243-131">ダイアログ ボックスで、外部組織のドメイン名を入力し、**OK** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="50243-131">In the dialog box, enter the domain name for the external organization, and then select **OK**.</span></span>

    ![外部組織との構成バージョンを共有するダイアログボックス](media/1_RCS_Repo_for_Share_with_form.JPG)

<span data-ttu-id="50243-133">構成が外部組織と共有され、その組織ではグローバルリポジトリで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="50243-133">The configuration is shared with the external organization and is available to that organization in the Global repository.</span></span> <span data-ttu-id="50243-134">そこから RCS の組織のインスタンスにインポートをする、または組織の Finance and Operations アプリのインスタンスにインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="50243-134">From there, it can be imported into the organization's instance of RCS or into its instances of Finance and Operations apps.</span></span>

6. <span data-ttu-id="50243-135">外部組織と既に共有されている構成の共有を解除するには、構成を選択して **共有解除** をクリックし、**OK** をクリックします</span><span class="sxs-lookup"><span data-stu-id="50243-135">To unshare a configuration that has been previously shared with an external organization, select the configuration and click **Unshare**, and then select **OK**</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]