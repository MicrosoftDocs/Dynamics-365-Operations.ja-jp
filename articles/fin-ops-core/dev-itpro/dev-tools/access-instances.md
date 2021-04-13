---
title: 開発環境の配置とアクセス
description: このトピックでは、開発インスタンスへのアクセス、ローカル開発 VM の構成、および開発者と管理者のための構成設定を見つける方法について説明します。
author: laneswenka
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10031
ms.assetid: 4be8b7a1-9632-4368-af41-6811cd100a37
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4170bcb8ae4d8d460c6fe66de2725603f6c2171
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750950"
---
# <a name="deploy-and-access-development-environments"></a><span data-ttu-id="a7e05-103">開発環境の配置とアクセス</span><span class="sxs-lookup"><span data-stu-id="a7e05-103">Deploy and access development environments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7e05-104">このトピックでは、開発インスタンスへのアクセス、ローカル開発仮想マシン (VM) の構成、および開発者と管理者にとって重要な構成設定を見つける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-104">This topic describes how to access development instances, configure local development virtual machines (VMs), and find important configurations settings for developers and administrators.</span></span>

## <a name="definitions"></a><span data-ttu-id="a7e05-105">定義</span><span class="sxs-lookup"><span data-stu-id="a7e05-105">Definitions</span></span>

| <span data-ttu-id="a7e05-106">期間</span><span class="sxs-lookup"><span data-stu-id="a7e05-106">Term</span></span>      | <span data-ttu-id="a7e05-107">定義</span><span class="sxs-lookup"><span data-stu-id="a7e05-107">Definition</span></span>                             |
|-----------|----------------------------------------|
| <span data-ttu-id="a7e05-108">エンド ユーザー</span><span class="sxs-lookup"><span data-stu-id="a7e05-108">End user</span></span>  | <span data-ttu-id="a7e05-109">Web クライアントを使用してインスタンスにアクセスするユーザー。</span><span class="sxs-lookup"><span data-stu-id="a7e05-109">A user who accesses an instance through the web client.</span></span> <span data-ttu-id="a7e05-110">エンド ユーザーは、インスタンスにアクセスするには Microsoft Azure Active Directory (Azure AD) の資格情報が必要で、そのインスタンスのユーザーとしてプロビジョニングまたは追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-110">The end user must have Microsoft Azure Active Directory (Azure AD) credentials to access an instance and must be provisioned/added as a user of that instance.</span></span> |
| <span data-ttu-id="a7e05-111">開発者</span><span class="sxs-lookup"><span data-stu-id="a7e05-111">Developer</span></span> | <span data-ttu-id="a7e05-112">Microsoft Visual Studio 環境でコードを開発するユーザー。</span><span class="sxs-lookup"><span data-stu-id="a7e05-112">A user who will develop code through the Microsoft Visual Studio environment.</span></span> <span data-ttu-id="a7e05-113">開発者は、開発環境 (VM) へのリモート デスクトップ アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-113">A developer requires Remote Desktop access to development environment (VM).</span></span> <span data-ttu-id="a7e05-114">開発者アカウントは、VM の管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-114">The developer account must be an administrator on the VM.</span></span>      |


## <a name="deploying-cloud-development-environments"></a><span data-ttu-id="a7e05-115">クラウド開発環境の配置</span><span class="sxs-lookup"><span data-stu-id="a7e05-115">Deploying cloud development environments</span></span>

<span data-ttu-id="a7e05-116">クラウド ホスト環境を展開するプロセスは、Lifecycle Services (LCS) トライアルまたはパートナー プロジェクトと、LCS 顧客実装プロジェクトで異なります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-116">The process of deploying cloud hosted environments differs for Lifecycle Services (LCS) trial or partner projects and LCS customer implementation projects.</span></span>

<span data-ttu-id="a7e05-117">**試用版** または **パートナー** プロジェクト用:</span><span class="sxs-lookup"><span data-stu-id="a7e05-117">For a **Trial** or **Partner** project:</span></span>

1. <span data-ttu-id="a7e05-118">LCS プロジェクトと Azure サブスクリプションの間に接続を作成します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-118">Create a connection between an LCS project and your Azure subscription.</span></span> <span data-ttu-id="a7e05-119">Azure サブスクリプション ID が必要であり、サブスクリプションの使用を承認します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-119">You will need your Azure subscription ID and authorize the use of the subscription.</span></span>
2. <span data-ttu-id="a7e05-120">配置する **環境** の下で **+** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-120">Select **+** under **Environments** to deploy.</span></span>

    ![LCS Onboard の方法](media/access-instances-5.jpeg)
    
3. <span data-ttu-id="a7e05-122">アプリケーションとプラットフォーム バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-122">Select an application and platform version.</span></span>
4. <span data-ttu-id="a7e05-123">環境のトポロジを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-123">Select an environment topology.</span></span> <span data-ttu-id="a7e05-124">詳細については、[プレビュー サブスクリプションのサインアップ](sign-up-preview-subscription.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-124">For more information, see [Sign up for preview subscriptions](sign-up-preview-subscription.md).</span></span>
    
5. <span data-ttu-id="a7e05-125">クラウドでホストされている環境を選択した場合は、使用する Azure コネクタを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-125">If you chose a cloud-hosted environment, select which Azure connector you want to use.</span></span> <span data-ttu-id="a7e05-126">**配置** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-126">Then select **Deploy**.</span></span>

    ![環境の配置](media/access-instances-3.jpeg)
    
6. <span data-ttu-id="a7e05-128">クラウド ホスト環境を選択しなかった場合は、ダウンロードする VHD を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-128">If you did not choose a cloud-hosted environment, select a VHD to download.</span></span>

<span data-ttu-id="a7e05-129">**顧客実装** プロジェクト用:</span><span class="sxs-lookup"><span data-stu-id="a7e05-129">For a **Customer Implementation** project:</span></span>
1. <span data-ttu-id="a7e05-130">LCS 実装プロジェクトにサインインします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-130">Sign in to your LCS Implementation project.</span></span>
2. <span data-ttu-id="a7e05-131">**構成** を選択して配置します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-131">Select **Configure** to deploy.</span></span>

    ![開発、テスト、およびコンフィギュレーション](media/access-instances-6.jpeg)
    
3. <span data-ttu-id="a7e05-133">アプリケーションとプラットフォーム バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-133">Select an application and platform version.</span></span>
4. <span data-ttu-id="a7e05-134">設定を指定し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-134">Specify the settings and select **Save**.</span></span>

    ![配置設定](media/access-instances-7.jpeg)

<span data-ttu-id="a7e05-136">顧客には、Microsoft の Azure サブスクリプションでホストされている無料の「開発とテスト」環境が 1 つ提供されます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-136">Customers are provided with one free "develop and test" environment hosted in Microsoft's Azure subscription.</span></span> <span data-ttu-id="a7e05-137">「開発およびテスト」には、**開発** と **ビルドおよびテスト** の 2 種類の環境があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-137">Under "Develop and test", there are two types of environments, **Develop** and **Build and Test**.</span></span> <span data-ttu-id="a7e05-138">開発およびカスタマイズ活動については、**開発** 環境をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-138">For development and customization activities, configure a **Develop** environment.</span></span> <span data-ttu-id="a7e05-139">**ビルドおよびテスト** 標準的な開発活動では環境はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="a7e05-139">**Build and Test** environments are not supported for standard development activities.</span></span> <span data-ttu-id="a7e05-140">代わりに、日単位ビルドおよびテストの自動化に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-140">Instead, they are used for daily build and test automation.</span></span> <span data-ttu-id="a7e05-141">詳細については、[継続的なビルドとテストの自動化をサポートする環境を配置して使用する](../perf-test/continuous-build-test-automation.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-141">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>  

<span data-ttu-id="a7e05-142">追加の開発とビルド環境は、ユーザー自身の Azure サブスクリプションで購入またはホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-142">Additional develop and build environments can either be purchased or hosted in your own Azure subscription.</span></span> <span data-ttu-id="a7e05-143">独自のサブスクリプションに環境を展開するには、**クラウド ホスト環境** ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-143">To deploy an environment in your own subscription, go to the **Cloud-hosted environment** page.</span></span>

![クラウド ホスト インスタンス](media/CloudHostedPicture.jpg)

## <a name="cloud-environment-that-is-provisioned-through-lcs"></a><span data-ttu-id="a7e05-145">LCS を通じてプロビジョニングされるクラウド環境</span><span class="sxs-lookup"><span data-stu-id="a7e05-145">Cloud environment that is provisioned through LCS</span></span>

<span data-ttu-id="a7e05-146">クラウド環境が LCS を通じてプロビジョニングされると、次の操作が行われます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-146">When a cloud environment is provisioned through LCS:</span></span>
+ <span data-ttu-id="a7e05-147">クラウド環境を要求するユーザーは、その環境内の管理者としてプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-147">The user who requests the cloud environment is provisioned as the administrator in that environment.</span></span>
+ <span data-ttu-id="a7e05-148">ユーザー アカウントは開発用 VM にプロビジョニングされ、リモート デスクトップを使用して環境へのアクセスを許可します。これらの資格情報は LCS の環境ページからアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-148">User accounts are provisioned on the development VM to allow access to the environment using Remote Desktop, these credentials are accessible on the environment page in LCS.</span></span>

### <a name="accessing-an-instance-through-a-url"></a><span data-ttu-id="a7e05-149">URL を試用したインスタンスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a7e05-149">Accessing an instance through a URL</span></span>

<span data-ttu-id="a7e05-150">エンド ユーザーはシステムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-150">The system can be accessed by end users.</span></span> <span data-ttu-id="a7e05-151">管理者は、インスタンスの **ユーザー** ページを使用して、このシステムにユーザーを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-151">The administrator can add users to this system by using the **Users** page in the instance.</span></span> <span data-ttu-id="a7e05-152">これらの追加のユーザーは LCS 内のユーザーである必要はないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-152">Note that these additional users don't have to be users in LCS.</span></span> <span data-ttu-id="a7e05-153">LCS プロジェクト サイトからは、クラウド環境のベース URL を取得します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-153">You obtain the base URL for the cloud environment from your LCS project site.</span></span>

1. <span data-ttu-id="a7e05-154">LCS プロジェクト ページに移動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-154">Go to your LCS project page.</span></span>
2. <span data-ttu-id="a7e05-155">**環境** セクションで、配置された環境をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-155">In the **Environments** section, click the deployed environment.</span></span>
3. <span data-ttu-id="a7e05-156">環境ページが開くと、右上隅で、**ログイン** &gt; **Finance and Operations にログオン** をクリックして、アプリケーションにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-156">When the environment page opens, you can access the application by clicking **Login** &gt; **Log on to Finance and Operations** in the upper-right corner.</span></span>
4. <span data-ttu-id="a7e05-157">有効なエンド ユーザー資格情報を使用して、アプリケーションにサインインします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-157">Use valid end user credentials to sign in to the application.</span></span> <span data-ttu-id="a7e05-158">現在の LCS ユーザーが最初に環境を展開したユーザーである場合は、そのユーザーは有効な終了ユーザーおよびアプリケーションの管理者である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-158">If the current LCS user is the user who originally deployed the environment, that user is probably a valid end user and the administrator of the application.</span></span>
5. <span data-ttu-id="a7e05-159">ブラウザーで、サインインした後にベース URL を記録します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-159">In your browser, make a note of the base URL after you sign in.</span></span> <span data-ttu-id="a7e05-160">たとえば、ベース URL は、`https://dynamicsAx7aosContoso.cloud.dynamics.com` である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-160">For example, the base URL might be `https://dynamicsAx7aosContoso.cloud.dynamics.com`.</span></span>

### <a name="accessing-the-cloud-instance-through-remote-desktop"></a><span data-ttu-id="a7e05-161">リモート デスクトップを使用したクラウド インスタンスへのアクセス</span><span class="sxs-lookup"><span data-stu-id="a7e05-161">Accessing the cloud instance through Remote Desktop</span></span>

<span data-ttu-id="a7e05-162">クラウド環境は、エンド ユーザーおよび開発者の両方としてアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-162">Cloud environments can be accessed both as an end user and as a developer.</span></span> <span data-ttu-id="a7e05-163">開発者は、リモート デスクトップの資格情報を使用してシステムにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-163">The developer gets access to the system through Remote Desktop credentials.</span></span> <span data-ttu-id="a7e05-164">リモート デスクトップの資格情報は、LCS プロジェクト サイトの環境ページから取得されます (このトピックの前の図を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="a7e05-164">The Remote Desktop credentials are obtained from the environment page on the LCS project site (see the illustration earlier in this topic).</span></span>

![制限された管理者アクセス](media/restricted-admin.png)

<span data-ttu-id="a7e05-166">配置された **プラットフォーム更新プログラム 12 以前** の環境の対象:</span><span class="sxs-lookup"><span data-stu-id="a7e05-166">For environments deployed **before Platform update 12**:</span></span>
1.  <span data-ttu-id="a7e05-167">VM 名をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-167">Click the VM name.</span></span>
2.  <span data-ttu-id="a7e05-168">表示されているローカル管理者のユーザー名とパスワードを使用して、リモート デスクトップ経由でクラウド VM に接続します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-168">Use the local administrator user name and password that are shown to connect to the cloud VM through Remote Desktop.</span></span> <span data-ttu-id="a7e05-169">パスワードの表示アイコンを選択してパスワードを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-169">You can reveal the password by selecting the show password icon.</span></span>

<span data-ttu-id="a7e05-170">配置された **プラットフォーム更新プログラム 12 以降** の任意の環境については、特徴的アカウント、開発者アカウントおよび管理者アカウントがあります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-170">For any environments deployed **on or after Platform update 12** , there are distinct accounts, a developer account and an admin account.</span></span> <span data-ttu-id="a7e05-171">顧客が、Microsoft サブスクリプションで実行されている開発環境またはビルド環境の仮想マシン管理者アカウントにアクセスすることはできません。</span><span class="sxs-lookup"><span data-stu-id="a7e05-171">Customers will not have access to virtual machine admin accounts on development or build environments that are running in Microsoft subscriptions.</span></span> <span data-ttu-id="a7e05-172">したがって、環境が Azure サブスクリプションで実行されていない限り、管理者アカウントは非表示になります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-172">Thus, the admin account will be hidden unless the environment is running in their Azure subscription.</span></span> <span data-ttu-id="a7e05-173">詳細については、[管理者アクセスを許可しない開発用 VM および ビルド用 VM に関するよく寄せられる質問](../sysadmin/VMs-no-admin-access.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-173">For more information, see [Development and build VMs that don't allow admin access FAQ](../sysadmin/VMs-no-admin-access.md).</span></span> 

<span data-ttu-id="a7e05-174">リモート デスクトップを通じて環境にサインインした後、ブラウザーからローカル アプリケーションにアクセスできるようにする場合、リモート コンピューターからアプリケーションにアクセスするために使用するのと同じベース URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-174">After you sign in to the environment through Remote Desktop, if you want to access the local application from the browser, use the same base URL that you use to access the application from a remote computer.</span></span> <span data-ttu-id="a7e05-175">上記のセクションは、このベース URL を LCS から取得する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-175">The previous section explains how to obtain this base URL from LCS.</span></span>

## <a name="vm-that-is-running-locally"></a><span data-ttu-id="a7e05-176">ローカルで実行されている VM</span><span class="sxs-lookup"><span data-stu-id="a7e05-176">VM that is running locally</span></span>
<span data-ttu-id="a7e05-177">仮想ハード ディスク (VHD) は LCS からダウンロードができるようになり、ローカル コンピューター上に設定可能です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-177">A virtual hard disk (VHD) is made available for download from LCS, so that you can set it up on a local machine.</span></span> <span data-ttu-id="a7e05-178">このシステムは、開発者によるアクセスを目的としており、Finance and Operations アプリの事前構成済みワンボックス開発環境です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-178">This system is intended to be accessed by a developer and is a pre-configured one-box development environment of Finance and Operations apps.</span></span> <span data-ttu-id="a7e05-179">VHD は、資産タイプの **ダウンロード可能な VHD** の下で、LCS の共有アセットライブラリで使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-179">The VHD is available in the Shared Asset library of LCS under the asset type **Downloadable VHD**.</span></span>

1. <span data-ttu-id="a7e05-180">LCS のメイン ページに移動して **共有アセット ライブラリ** を選択するか、または [共有アセット ライブラリ](https://lcs.dynamics.com/V2/SharedAssetLibrary) に移動します。 </span><span class="sxs-lookup"><span data-stu-id="a7e05-180">Go to the LCS main page and select **Shared asset library** or go to [Shared Asset Library](https://lcs.dynamics.com/V2/SharedAssetLibrary).</span></span>
2. <span data-ttu-id="a7e05-181">資産タイプの **ダウンロード可能な VHD** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-181">Select the asset type **Downloadable VHD**.</span></span>
3. <span data-ttu-id="a7e05-182">目的の Finance and Operation バージョンに基づいて、探している VHD を検索します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-182">Find the VHD you are looking for based on the desired Finance and Operation version.</span></span> <span data-ttu-id="a7e05-183">VHD は、ダウンロードする必要がある複数のファイル パーツに分割されています。</span><span class="sxs-lookup"><span data-stu-id="a7e05-183">The VHD is divided into multiple file parts that you need to download.</span></span> <span data-ttu-id="a7e05-184">たとえば、 "VHD - 10.0.5" で始まる資産ファイルは、バージョン 10.0.5 をインストールするために必要な別のファイルです。</span><span class="sxs-lookup"><span data-stu-id="a7e05-184">For example, the asset files that start with "VHD - 10.0.5" are the different files you need in order to install version 10.0.5.</span></span>
4. <span data-ttu-id="a7e05-185">目的の VHD に関連付けられているすべてのファイル (パーツ) をローカル フォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-185">Download all files (parts) associated with the desired VHD to a local folder.</span></span>
5. <span data-ttu-id="a7e05-186">ダウンロードが完了したら、ダウンロードした実行可能ファイルを実行して、ソフトウェア使用許諾契約に同意し、VHD を抽出するファイル パスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-186">After the download is complete, run the executable file that you downloaded, accept the software license agreement, and choose a file path to extract the VHD to.</span></span>
6. <span data-ttu-id="a7e05-187">これにより、ローカルの仮想マシンを実行するのに使用できるローカル VHD ファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-187">This creates a local VHD file that you can use to run a local virtual machine.</span></span>

### <a name="commerce-configuration"></a><span data-ttu-id="a7e05-188">コマースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7e05-188">Commerce configuration</span></span>

<span data-ttu-id="a7e05-189">コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a7e05-189">Follow the steps in this section if you are also configuring for Commerce.</span></span>

<span data-ttu-id="a7e05-190">ダウンロード可能な VHD を POS のカスタマイズに使用するには、次の手順も実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-190">To use the downloadable VHD for POS customizations, you must also follow this step.</span></span>

-   <span data-ttu-id="a7e05-191">ホスト コンピューターで、入れ子になった VM サポートを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-191">On the host computer, enable Nested VM support.</span></span> <span data-ttu-id="a7e05-192">詳細については、[入れ子仮想化の仮想マシンで Hyper-v を実行](https://msdn.microsoft.com/virtualization/hyperv_on_windows/user_guide/nesting) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-192">For more information, see [Run Hyper-V in a Virtual Machine with Nested Virtualization](https://msdn.microsoft.com/virtualization/hyperv_on_windows/user_guide/nesting).</span></span>

### <a name="running-the-virtual-machine-locally"></a><span data-ttu-id="a7e05-193">仮想マシンをローカルで実行</span><span class="sxs-lookup"><span data-stu-id="a7e05-193">Running the virtual machine locally</span></span>

<span data-ttu-id="a7e05-194">Hyper-V マネージャーから VM を実行するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a7e05-194">Follow these steps to run the VM from Hyper-V Manager.</span></span>

1. <span data-ttu-id="a7e05-195">VM を起動するには、**開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-195">To start the VM, select **Start**.</span></span>
2. <span data-ttu-id="a7e05-196">ウィンドウで VM を開くには、**接続** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-196">To open the VM in a window, select **Connect**.</span></span>
3. <span data-ttu-id="a7e05-197">ツール バーで **Ctrl + Alt + Delete** ボタンを選択してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-197">Select the **Ctrl+Alt+Delete** button on the toolbar.</span></span> <span data-ttu-id="a7e05-198">VM は、ほとんどのキーボード コマンドを受け取りますが、その中に Ctrl + Alt + Del は含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a7e05-198">The VM receives most keyboard commands, but Ctrl+Alt+Delete isn't one of them.</span></span> <span data-ttu-id="a7e05-199">したがって、ボタンまたはメニュー コマンドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-199">Therefore, you must use the button or a menu command.</span></span>
4. <span data-ttu-id="a7e05-200">次の資格情報を使用して VM にログインします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-200">Sign in to the VM by using the following credentials:</span></span>
   - <span data-ttu-id="a7e05-201">ユーザー名: **管理者**</span><span class="sxs-lookup"><span data-stu-id="a7e05-201">User name: **Administrator**</span></span>
   - <span data-ttu-id="a7e05-202">パスワード: <strong>pass@word1</strong></span><span class="sxs-lookup"><span data-stu-id="a7e05-202">Password: <strong>pass@word1</strong></span></span>

    > [!TIP]
    > <span data-ttu-id="a7e05-203">画面解像度を変更することにより、VM ウィンドウのサイズを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-203">You can resize the VM window by changing the screen resolution.</span></span> <span data-ttu-id="a7e05-204">VM でデスクトップを右クリックし、**画面の解像度** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-204">Right-click the desktop on the VM, and then click **Screen resolution**.</span></span> <span data-ttu-id="a7e05-205">ディスプレイに適した解像度を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-205">Select a resolution that works well for your display.</span></span>
   
5. <span data-ttu-id="a7e05-206">管理者ユーザーを準備します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-206">Provision the administrator user.</span></span> <span data-ttu-id="a7e05-207">詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-207">For more information, see the next section.</span></span>
6. <span data-ttu-id="a7e05-208">バッチ マネージャー サービスを起動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-208">Start the Batch Manager Service.</span></span> <span data-ttu-id="a7e05-209">このステップは、バッチ ジョブまたはワークフローを実行している場合に必要です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-209">This step is required if you're running batch jobs or workflows.</span></span>
   1.  <span data-ttu-id="a7e05-210">管理者として **コマンド プロンプト** ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-210">Open a **Command Prompt** window as an administrator.</span></span>
   2.  <span data-ttu-id="a7e05-211">**net start DynamicsAxBatch** と入力し、Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-211">Type **net start DynamicsAxBatch**, and then press Enter.</span></span>

   <span data-ttu-id="a7e05-212">また、サービスを **サービス** ウィンドウから開始することができます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-212">You can also start the service from the **Services** window.</span></span>

7. <span data-ttu-id="a7e05-213">必要に応じて [更新プログラムを適用](../migration-upgrade/upgrade-latest-platform-update.md#apply-a-platform-update-to-environments-that-are-not-connected-to-lcs) します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-213">[Apply updates](../migration-upgrade/upgrade-latest-platform-update.md#apply-a-platform-update-to-environments-that-are-not-connected-to-lcs) as needed.</span></span>

#### <a name="commerce-configuration"></a><span data-ttu-id="a7e05-214">コマースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7e05-214">Commerce configuration</span></span>

<span data-ttu-id="a7e05-215">POS カスタマイズで、ゲスト VM でもこれらの手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-215">For POS customizations, you must also follow these steps on the guest VM.</span></span>

1.  <span data-ttu-id="a7e05-216">[Microsoft Emulator for Windows 10 Mobile Anniversary Update](https://www.microsoft.com/download/details.aspx?id=53424) をダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-216">Download and install [Microsoft Emulator for Windows 10 Mobile Anniversary Update](https://www.microsoft.com/download/details.aspx?id=53424).</span></span>
2.  <span data-ttu-id="a7e05-217">Hyper-V ホスト サービスを起動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-217">Start the Hyper-V host service.</span></span> <span data-ttu-id="a7e05-218">詳細については、[Hyper-V: Hyper-V 仮想マシン管理サービスを実行している必要があります](https://technet.microsoft.com/library/ee956894(v=ws.10).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-218">For more information, see [Hyper-V: The Hyper-V Virtual Machine Management service must be running](https://technet.microsoft.com/library/ee956894(v=ws.10).aspx).</span></span> <span data-ttu-id="a7e05-219">起動中にエラーが発生した場合は、ゲスト VM で Hyper-V ロールをアンインストールし、再インストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-219">If errors occur during startup, you can also try to uninstall and reinstall the Hyper-V role on the guest VM.</span></span>

### <a name="provisioning-the-administrator-user"></a><span data-ttu-id="a7e05-220">管理者ユーザーを準備</span><span class="sxs-lookup"><span data-stu-id="a7e05-220">Provisioning the administrator user</span></span>

<span data-ttu-id="a7e05-221">開発者がアクセスするには、インスタンスで管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-221">For developer access, you must be an administrator on the instance.</span></span> <span data-ttu-id="a7e05-222">管理者としての資格情報をプロビジョニングするには、デスクトップにある管理者プロビジョニング ツールを実行し、ツールにメール アドレス (Azure AD 資格情報) を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-222">To provision your own credentials as an administrator, run the admin user provisioning tool that is provided on the desktop, and provide your email address (Azure AD credentials) in the tool.</span></span>

1.  <span data-ttu-id="a7e05-223">デスクトップから、管理者として管理者ユーザーのプロビジョニング ツールを実行します (アイコンを右クリックし、**管理者として実行** をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="a7e05-223">From the desktop, run the admin user provisioning tool as an administrator (right-click the icon, and then click **Run as administrator**).</span></span>
2.  <span data-ttu-id="a7e05-224">電子メール アドレスを入力し、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-224">Enter your email address, and then select **Submit**.</span></span>

### <a name="commerce-configuration"></a><span data-ttu-id="a7e05-225">コマースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7e05-225">Commerce configuration</span></span>

<span data-ttu-id="a7e05-226">コマースもコンフィギュレーションしている場合は、このセクションの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a7e05-226">Follow the steps in this section if you are also configuring for Commerce.</span></span>

#### <a name="for-dynamics-365-for-operations-version-1611"></a><span data-ttu-id="a7e05-227">Dynamics 365 for Operations の場合、バージョン 1611</span><span class="sxs-lookup"><span data-stu-id="a7e05-227">For Dynamics 365 for Operations, Version 1611</span></span>

1.  <span data-ttu-id="a7e05-228">RetailTenantUpdateTool を実行します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-228">Run the RetailTenantUpdateTool.</span></span>
    -   <span data-ttu-id="a7e05-229">このツールのアイコンは、デスクトップ上で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-229">The icon for this tool is available on the desktop.</span></span>
    -   <span data-ttu-id="a7e05-230">このツールは、次の場所から使用することもできます: C:\windows\System32\WindowsPowerShell\v1.0\PowerShell.exe -File C:\RetailSDK\Tools\RetailTenantUpdateTool.ps1</span><span class="sxs-lookup"><span data-stu-id="a7e05-230">This tool is also available at the following location: C:\windows\System32\WindowsPowerShell\v1.0\PowerShell.exe -File C:\RetailSDK\Tools\RetailTenantUpdateTool.ps1</span></span>

2.  <span data-ttu-id="a7e05-231">このツールを開始するには、アイコンをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-231">Double-click the icon to start this tool.</span></span> <span data-ttu-id="a7e05-232">自身の Azure AD 資格情報を求められます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-232">You will be prompted for your Azure AD credentials.</span></span> <span data-ttu-id="a7e05-233">管理者ユーザーのプロビジョニング ツールで以前使用したものと同じ資格情報を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-233">You must use the same credentials that you used in the admin user provisioning tool earlier.</span></span>

#### <a name="for-dynamics-365-for-operations-70"></a><span data-ttu-id="a7e05-234">Dynamics 365 for Operations 7.0 の場合</span><span class="sxs-lookup"><span data-stu-id="a7e05-234">For Dynamics 365 for Operations 7.0</span></span>

1.  <span data-ttu-id="a7e05-235">[IT プロフェッショナル用 Microsoft Online Services サインイン アシスタント RTW](https://go.microsoft.com/fwlink/?LinkID=286152) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-235">Install [Microsoft Online Services Sign-In Assistant for IT Professionals RTW](https://go.microsoft.com/fwlink/?LinkID=286152).</span></span>
2.  <span data-ttu-id="a7e05-236">[Windows PowerShell (64-ビット バージョン) 用 Azure Active Directory モジュール](https://go.microsoft.com/fwlink/p/?linkid=236297) をインストールします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-236">Install [Azure Active Directory Module for Windows PowerShell (64-bit version)](https://go.microsoft.com/fwlink/p/?linkid=236297).</span></span>
3.  <span data-ttu-id="a7e05-237">テナントとユーザー ID の Azure AD を照会します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-237">Query Azure AD for your tenant and user ID.</span></span> <span data-ttu-id="a7e05-238">Windows PowerShell 統合スクリプト環境 (ISE) ウィンドウを管理者権限で開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-238">Open a Windows PowerShell Integrated Scripting Environment (ISE) window with administrative privileges, and run the following command.</span></span> <span data-ttu-id="a7e05-239">Azure AD 資格情報を求められます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-239">You will be prompted for Azure AD credentials.</span></span> <span data-ttu-id="a7e05-240">以前に管理者プロビジョニング ツールで使用したのと同じユーザー アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-240">Use the same user account that you used in the admin user provisioning tool earlier.</span></span>

    ```powershell
    $msocred = Get-Credential 
    Connect-MsolService -Credential $msocred 
    $company = Get-MsolCompanyInformation 
    Write-Host "TenantID: $($company.ObjectId)" 
    $msocred.UserName 
    $users = Get-MsolUser -SearchString "$($msocred.username)" 
    foreach($u in $users) 
    { 
        if($u.SignInName -eq $msocred.UserName) 
        { 
            Write-Host "SignInName:$($u.SignInName) UserId: $($u.ObjectId)" 
        } 
    }
    ```
        
    <span data-ttu-id="a7e05-241">[![Windows PowerShell ISE ウィンドウのコマンド](./media/retailconfig02-1024x529.png)](./media/retailconfig02.png)</span><span class="sxs-lookup"><span data-stu-id="a7e05-241">[![Command in the Windows PowerShell ISE window](./media/retailconfig02-1024x529.png)](./media/retailconfig02.png)</span></span>

4.  <span data-ttu-id="a7e05-242">次の SQL スクリプトを更新し、その環境の AXDB で実行します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-242">Update the following SQL script, and run it in on AXDB for that environment.</span></span> <span data-ttu-id="a7e05-243">上記の Windows PowerShell スクリプト出力から次のパラメーターの値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-243">Supply values for the following parameters from the preceding Windows PowerShell script output:</span></span>

    -   <span data-ttu-id="a7e05-244">**TenantID** – たとえば、c83429a6-782b-4275-85cf-60ebe81250ee</span><span class="sxs-lookup"><span data-stu-id="a7e05-244">**TenantID** – For example, c83429a6-782b-4275-85cf-60ebe81250ee</span></span>
    -   <span data-ttu-id="a7e05-245">**UserId** – たとえば、a036b5d8-bc8c-4abe-8eec-17516ea913ec</span><span class="sxs-lookup"><span data-stu-id="a7e05-245">**UserId** – For example, a036b5d8-bc8c-4abe-8eec-17516ea913ec</span></span>

    <!-- -->
    ```sql
    DECLARE @TenantId NVARCHAR(1024)         DECLARE @UserId NVARCHAR(1024) 
    SET @TenantId = ‘‘ 
    SET @UserId = ‘‘ 
    IF(LEN(@TenantId) > 0 AND LEN(@UserId) > 0) 
        BEGIN 
        UPDATE AxDBRAIN.dbo.SYSSERVICECONFIGURATIONSETTING SET [VALUE] = @TenantId WHERE [NAME] = ‘TENANTID’ 
        UPDATE RetailHoustonStore.ax.SYSSERVICECONFIGURATIONSETTING SET [VALUE] = @TenantId WHERE [NAME] = ‘TENANTID’ 
        UPDATE AxDBRAIN.dbo.RETAILSTAFFTABLE SET EXTERNALIDENTITYID = @TenantId, EXTERNALIDENTITYSUBID = @UserId WHERE STAFFID = ‘000160’
        END 
    ELSE 
        BEGIN 
        RAISERROR (15600, -1, -1, ‘TenantId and UserId must be set before running this script’) 
        END
    ```

5.  <span data-ttu-id="a7e05-246">管理者特権の **コマンド プロンプト** ウィンドウで **IISRESET** を実行することにより、インターネット インフォメーション サービス (IIS) をリセットします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-246">Reset Internet Information Services (IIS) by running **IISRESET** in an elevated **Command Prompt** window.</span></span>
6.  <span data-ttu-id="a7e05-247">新しい管理者ユーザーを使用するようにリアルタイム サービス プロファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-247">Update the Real-time service profile to use the new admin user.</span></span>
    1.  <span data-ttu-id="a7e05-248">**小売とコマース** &gt; **本社の設定** &gt; **コマース スケジューラ** &gt; **リアルタイム サービス プロファイル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-248">Go to **Retail and Commerce** &gt; **Headquarters setup** &gt; **Commerce scheduler** &gt; **Real-time service profiles**.</span></span>
    3.  <span data-ttu-id="a7e05-249">以前に使用したユーザーを使用するように JBB レコードを編集します (たとえば、`administrator@contosoax7.onmicrosoft.com`)。</span><span class="sxs-lookup"><span data-stu-id="a7e05-249">Edit the JBB record so that it uses the user that you used earlier (for example, `administrator@contosoax7.onmicrosoft.com`).</span></span>
    4.  <span data-ttu-id="a7e05-250">既定のチャネル データベースの CDX ジョブ 1070 (スタッフ) を実行します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-250">Run CDX Job 1070 (Staff) for the default channel database.</span></span>
    5.  <span data-ttu-id="a7e05-251">クライアント上の **ダウンロード セッション** ページを表示して、ジョブが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-251">Verify that the job succeeded by viewing the **Download Sessions** page on the client.</span></span>

### <a name="base-url-of-the-local-application"></a><span data-ttu-id="a7e05-252">ローカル アプリケーションの基本 URL</span><span class="sxs-lookup"><span data-stu-id="a7e05-252">Base URL of the local application</span></span>

<span data-ttu-id="a7e05-253">ユーザーが管理者としてプロビジョニングされた後、ユーザーは次のベース URL に移動してコンピュータ上のインスタンスにアクセスできます: `https://usnconeboxax1aos.cloud.onebox.dynamics.com`。</span><span class="sxs-lookup"><span data-stu-id="a7e05-253">After the user is provisioned as an administrator, that user can access the instance on the computer by navigating to the following base URL: `https://usnconeboxax1aos.cloud.onebox.dynamics.com`.</span></span> <span data-ttu-id="a7e05-254">バージョン管理を使用しており、複数の開発 VMs を同じ Azure DevOps プロジェクトに接続する予定がある場合は、ローカル VM 名を変更してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-254">If you're using version control and plan to connect multiple development VMs to the same Azure DevOps project, rename your local VM.</span></span> <span data-ttu-id="a7e05-255">手順については、[ローカル開発 (VHD) 環境の名前変更](../migration-upgrade/vso-machine-renaming.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-255">For instructions, see [Rename a local development (VHD) environment](../migration-upgrade/vso-machine-renaming.md).</span></span>

#### <a name="commerce-configuration"></a><span data-ttu-id="a7e05-256">コマースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7e05-256">Commerce configuration</span></span>

<span data-ttu-id="a7e05-257">POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com/`です。　</span><span class="sxs-lookup"><span data-stu-id="a7e05-257">The URL of the POS app is `https://usnconeboxax1pos.cloud.onebox.dynamics.com/`.</span></span> 

<span data-ttu-id="a7e05-258">クラウド POS アプリケーションの URL は `https://usnconeboxax1pos.cloud.onebox.dynamics.com` です。　</span><span class="sxs-lookup"><span data-stu-id="a7e05-258">The URL of the Cloud POS app is `https://usnconeboxax1pos.cloud.onebox.dynamics.com`.</span></span> <span data-ttu-id="a7e05-259">構成手順を完了すると、この VM には Azure AD テナントがプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-259">After you complete the configuration steps, this VM is provisioned with your Azure AD tenant.</span></span> <span data-ttu-id="a7e05-260">Azure AD 管理者アカウントは、デモ データ内のレジ担当者アカウントにマップされます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-260">Your Azure AD admin account is mapped to a cashier worker account in demo data.</span></span> <span data-ttu-id="a7e05-261">この環境の POS デバイスを簡単にアクティブにするには、このレジ担当者アカウントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-261">You can use this cashier account to easily activate a POS device in this environment.</span></span>

-   <span data-ttu-id="a7e05-262">出納係ユーザー ID: **000160**</span><span class="sxs-lookup"><span data-stu-id="a7e05-262">Cashier user ID: **000160**</span></span>
-   <span data-ttu-id="a7e05-263">出納係パスワード: **123**</span><span class="sxs-lookup"><span data-stu-id="a7e05-263">Cashier password: **123**</span></span>
-   <span data-ttu-id="a7e05-264">出納係 LE: **USRT**</span><span class="sxs-lookup"><span data-stu-id="a7e05-264">Cashier LE: **USRT**</span></span>
-   <span data-ttu-id="a7e05-265">出納係ストア: **ヒューストン**</span><span class="sxs-lookup"><span data-stu-id="a7e05-265">Cashier store: **Houston**</span></span>

## <a name="location-of-packages-source-code-and-other-aos-configurations"></a><span data-ttu-id="a7e05-266">パッケージ、ソース コード、およびその他の AOS コンフィギュレーションの場所</span><span class="sxs-lookup"><span data-stu-id="a7e05-266">Location of packages, source code, and other AOS configurations</span></span>
<span data-ttu-id="a7e05-267">VM で、AOSWebApplication の web.config file を開くことによって、ほとんどのアプリケーション コンフィギュレーションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-267">On a VM, you can find most of the application configuration by opening the web.config file of AOSWebApplication.</span></span>

1.  <span data-ttu-id="a7e05-268">IIS を起動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-268">Start IIS.</span></span>
2.  <span data-ttu-id="a7e05-269">**サイト** &gt; **AOSWebApplication** に移動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-269">Go to **Sites** &gt; **AOSWebApplication**.</span></span>
3.  <span data-ttu-id="a7e05-270">右クリックしてから、**エクスプローラー** をクリックしてエクスプローラーを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-270">Right-click, and then click **Explore** to open File Explorer.</span></span>
4.  <span data-ttu-id="a7e05-271">メモ帳や他のテキスト エディターで web.config ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7e05-271">Open the web.config file in Notepad or another text editor.</span></span> <span data-ttu-id="a7e05-272">多くの開発者や管理者にとって、次のキーが重要です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-272">The following keys are of interest to many developers and administrators:</span></span>
    -   <span data-ttu-id="a7e05-273">**Aos.MetadataDirectory** - このキーは、プラットフォームとアプリケーションのバイナリを含むパッケージ フォルダの場所、およびソースコードをポイントします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-273">**Aos.MetadataDirectory** – This key points to the location of the packages folder that contains platform and application binaries, and also source code.</span></span> <span data-ttu-id="a7e05-274">(ソース コードは、開発環境でのみ使用できます。) 一般的な値は、c:\packages、c:\AosServicePackagesLocalDirectory、および J:AosServicePackagesLocalDirectory です。</span><span class="sxs-lookup"><span data-stu-id="a7e05-274">(Source code is available only in development environments.) Typical values are: c:\packages, c:\AosServicePackagesLocalDirectory, and J:AosServicePackagesLocalDirectory.</span></span>
    -   <span data-ttu-id="a7e05-275">**DataAccess.Database** - このキーは、データベースの名前を保持します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-275">**DataAccess.Database** – This key holds the name of the database.</span></span>
    -   <span data-ttu-id="a7e05-276">**Aos.AppRoot** - このキーは、Application Object Server (AOS) Web アプリケーションのルート フォルダーをポイントします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-276">**Aos.AppRoot** – This key points to the root folder of the Application Object Server (AOS) web application.</span></span>

### <a name="commerce-configuration"></a><span data-ttu-id="a7e05-277">コマースのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="a7e05-277">Commerce configuration</span></span>

<span data-ttu-id="a7e05-278">ソフトウェア開発キット (SDK) は、C:\RetailSDK にあります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-278">The software development kit (SDK) is available at C:\RetailSDK.</span></span> <span data-ttu-id="a7e05-279">アプリケーションの使用およびカスタマイズ方法の詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7e05-279">For more information about how to use and customize applications, see the following topics:</span></span>
-   [<span data-ttu-id="a7e05-280">Retail ソフトウェア開発キット (SDK) アーキテクチャ</span><span class="sxs-lookup"><span data-stu-id="a7e05-280">Retail software development kit (SDK) architecture</span></span>](../../../retail/dev-itpro/retail-sdk/retail-sdk-overview.md)
-   [<span data-ttu-id="a7e05-281">販売時点管理 (POS) デバイスのライセンス認証</span><span class="sxs-lookup"><span data-stu-id="a7e05-281">Point of sale (POS) device activation</span></span>](../../../retail/dev-itpro/retail-device-activation.md)

## <a name="redeploying-or-restarting-the-runtime-on-the-vm"></a><span data-ttu-id="a7e05-282">VM でのランタイムの再配置または再起動</span><span class="sxs-lookup"><span data-stu-id="a7e05-282">Redeploying or restarting the runtime on the VM</span></span>
<span data-ttu-id="a7e05-283">ローカルのランタイムを再起動して、すべてのパッケージを再配置するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-283">To restart the local runtime and redeploy all the packages, follow these steps.</span></span>

1.  <span data-ttu-id="a7e05-284">ファイル エクスプローラーを開き、C:\CustomerServiceUnit に移動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-284">Open File Explorer, and go to C:\CustomerServiceUnit.</span></span>
2.  <span data-ttu-id="a7e05-285">**AOSDeploy.cmd** を右クリックして **管理者として実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7e05-285">Right-click **AOSDeploy.cmd**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="a7e05-286">このプロセス時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7e05-286">This process might take a while.</span></span> <span data-ttu-id="a7e05-287">cmd.exe ウィンドウが終了すると、プロセスが完了します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-287">The process is completed when the cmd.exe window closes.</span></span> <span data-ttu-id="a7e05-288">ランタイムを再配置せずに AOS を再起動するのみの場合は、管理者の **Command Prompt** ウィンドウから **iisreset** を実行するか、IIS から AOSWebApplication を再起動します。</span><span class="sxs-lookup"><span data-stu-id="a7e05-288">If you just want to restart AOS (without redeploying the runtime), run **iisreset** from an administrator **Command Prompt** window, or restart AOSWebApplication from IIS.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]