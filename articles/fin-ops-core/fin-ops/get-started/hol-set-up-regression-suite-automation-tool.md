---
title: Regression Suite Automation Tool の設定およびインストール チュートリアル
description: このトピックは、Regression Suite Automation Tool (RSAT) の設定およびインストール方法を説明するチュートリアルです。
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 4757d506239e309dcbc3e181469b17e3286cc111
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4695118"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="72efa-103">Regression Suite Automation Tool の設定およびインストール チュートリアル</span><span class="sxs-lookup"><span data-stu-id="72efa-103">Set up and install Regression suite automation tool tutorial</span></span>
<span data-ttu-id="72efa-104">このトピックは、RSAT および RSAT の使用に関連したツールをセットアップして開始するのに役立つチュートリアルです。</span><span class="sxs-lookup"><span data-stu-id="72efa-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span> 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="72efa-105">インターネット ブラウザー ツールを使用して、このページを PDF 形式でダウンロードして保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-105">Use your internet browser tools to download and save this page in PDF format.</span></span> 

## <a name="key-concepts"></a><span data-ttu-id="72efa-106">重要な概念</span><span class="sxs-lookup"><span data-stu-id="72efa-106">Key concepts</span></span>

- <span data-ttu-id="72efa-107">Regression Suite Automation Tool (RSAT) をサポートするさまざまなアプリケーションに必要なインストールと前提条件の設定について理解してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="72efa-108">タスク レコーダー機能と、 Microsoft Dynamics Lifecycle Services (LCS) および Microsoft Azure DevOps を組み合わせて使用することで、テスト ケースの作成、構成、実行、調査、および報告が可能になります。</span><span class="sxs-lookup"><span data-stu-id="72efa-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="72efa-109">機能ユーザーがタスク レコーダーを使用してビジネス タスクを記録し、ソース コードを作成しなくてもタスク記録を一連の自動テストに変換できるようにします。</span><span class="sxs-lookup"><span data-stu-id="72efa-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="72efa-110">準備</span><span class="sxs-lookup"><span data-stu-id="72efa-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="72efa-111">必要条件</span><span class="sxs-lookup"><span data-stu-id="72efa-111">Prerequisites</span></span>

- <span data-ttu-id="72efa-112">このチュートリアルでは、Microsoft Dynamics 365 for Finance and Operations バージョン 10.0 (2019 年 4 月) またはそれ以降を実行する環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="72efa-113">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 7.3、プラットフォーム更新プログラム 20 (PU20) またはそれ以降を使用している場合もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="72efa-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="72efa-114">ユーザーは、環境に対して管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="72efa-115">顧客テナント LCS および Azure DevOps (以前は Microsoft Visual Studio Team Services \[VSTS\]と呼ばれていた) にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="72efa-116">テスト スイートを作成および管理しているユーザーは、Azure DevOps テスト計画またはテスト管理者ライセンスを持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="72efa-117">次のライセンスを使用してテスト計画にアクセスすることもできます。</span><span class="sxs-lookup"><span data-stu-id="72efa-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="72efa-118">Visual Studio エンタープライズ ライセンス</span><span class="sxs-lookup"><span data-stu-id="72efa-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="72efa-119">Visual Studio Test Professional ライセンス</span><span class="sxs-lookup"><span data-stu-id="72efa-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="72efa-120">MSDN プラットフォームのサブスクライバー ライセンス</span><span class="sxs-lookup"><span data-stu-id="72efa-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="72efa-121">RSAT は、テスト環境に Web ブラウザーを介してアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="72efa-122">テスト パラメーターを作成および編集するには、Microsoft Excel をインストールしておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="72efa-123">Azure DevOps のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72efa-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="72efa-124">ユーザーの適格性</span><span class="sxs-lookup"><span data-stu-id="72efa-124">User eligibility</span></span>

<span data-ttu-id="72efa-125">ユーザーが Azure DevOps に作成されていること、および Azure テスト計画へのアクセスを提供するサブスクリプション レベルを持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="72efa-126">Azure DevOps テスト計画ライセンスは、ユーザーがテスト ケースを作成および管理する場合にのみ必要です (つまり、すべての RSAT ユーザーがこのライセンスを必要とするわけではありません)。</span><span class="sxs-lookup"><span data-stu-id="72efa-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="72efa-127">ライセンスの要件については、[ライセンス要件](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-127">For information about the license requirements, see [License requirements](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="72efa-128">新しい Azure DevOps プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="72efa-128">Create a new Azure DevOps project</span></span>
<span data-ttu-id="72efa-129">RSATは、テスト ケースとテスト スイートの管理、レポート作成、およびテスト実行結果の調査に Azure Devops を使用します。</span><span class="sxs-lookup"><span data-stu-id="72efa-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span> 

> [!NOTE]
> <span data-ttu-id="72efa-130">既存の Azure DevOps のプロジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="72efa-131">ただし、既存の Azure DevOps のプロジェクトがカスタム テンプレートを持つように設定されている場合は、ビジネス プロセス モデラー (BPM) から Azure DevOps にテスト ケースを同期するときに「VSTSの同期エラー」というエラーが表示されます ([BPM から Azure DevOps への同期をテストする](#test-the-synchronization-from-bpm-to-azure-devops) セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="72efa-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="72efa-132">カスタム テンプレートに対して次のようなベスト プラクティスに従っている場合は、テストケースを Azure DevOps に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="72efa-133">(これらのベスト プラクティスは、エラー メッセージに一覧表示されています)。</span><span class="sxs-lookup"><span data-stu-id="72efa-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="72efa-134">作業項目タイプや標準フィールドは削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="72efa-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="72efa-135">作業項目タイプの状態は削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="72efa-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="72efa-136">必須フィールドを作業項目タイプに追加しないでください。</span><span class="sxs-lookup"><span data-stu-id="72efa-136">Do not add any required fields to a work item type.</span></span>

![ベスト プラクティスの一覧に表示されるエラー メッセージ](./media/setup_rsa_tool_02.png)

<span data-ttu-id="72efa-138">それ以外の場合は、このチュートリアルでは新しい Azure DevOps プロジェクトを作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72efa-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="72efa-139">詳細については、[カスタム Azure DevOps (VSTS) プロセス テンプレートを使用して BPM に同期するときの問題](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="72efa-140">Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`) を開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="72efa-141">Azure DevOps ページの右上隅にある **プロジェクトを作成する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![プロジェクト ボタンを作成する](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="72efa-143">次のフィールドに入力し、**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="72efa-144">**プロジェクト名**</span><span class="sxs-lookup"><span data-stu-id="72efa-144">**Project name**</span></span>
    - <span data-ttu-id="72efa-145">**バージョン管理** ー **Team Foundation バージョン管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="72efa-146">既定のオプションでは **Git** はサポートされていないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="72efa-147">**作業項目プロセス**</span><span class="sxs-lookup"><span data-stu-id="72efa-147">**Work item process**</span></span>

    ![新しいプロジェクト ダイアログ ボックスを作成する](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="72efa-149">個人用アクセス トークンを作成する</span><span class="sxs-lookup"><span data-stu-id="72efa-149">Create a personal access token</span></span>

<span data-ttu-id="72efa-150">このチュートリアルでは、LCS ビジネス プロセス モデラー (BPM) を使用してテスト ケース ライブラリを作成し、テスト ケースと Azure DevOps の同期を行います。</span><span class="sxs-lookup"><span data-stu-id="72efa-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="72efa-151">BPM を Azure DevOps と同期するには、個人用アクセス トークンが必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="72efa-152">Azure DevOps プロジェクトのページの右上隅にある プロファイル アイコンを選択し、**セキュリティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![セキュリティ コマンド](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="72efa-154">左ウィンドウの **セキュリティ** で、**個人用アクセス トークン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="72efa-155">**新しいトークン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-155">Then select **New Token**.</span></span>

    ![ユーザー設定の個人用アクセス トークン タブの新しいトークン ボタン](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="72efa-157">次のフィールドに入力し、**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="72efa-158">**氏名**</span><span class="sxs-lookup"><span data-stu-id="72efa-158">**Name**</span></span>
    - <span data-ttu-id="72efa-159">**有効期限 (UTC)** ー **カスタム定義** を選択し、日付の選択を使用して、使用可能な最後の日付を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="72efa-160">**スコープ** ー **フル アクセス** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-160">**Scopes** – Select the **Full access** option.</span></span>

    ![新しい個人用アクセス トークン ダイアログ ボックスを作成する](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-162">作成された個人用アクセス トークンをメモします。</span><span class="sxs-lookup"><span data-stu-id="72efa-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="72efa-163">これは、RSAT の構成を設定するときに必要になります。</span><span class="sxs-lookup"><span data-stu-id="72efa-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![個人用アクセス トークン](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="72efa-165">LCS プロジェクトを構成する</span><span class="sxs-lookup"><span data-stu-id="72efa-165">Configure the LCS project</span></span>

<span data-ttu-id="72efa-166">マスター テスト ライブラリ用の Lifecycle Services (LCS) プロジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="72efa-167">LCS ビジネス プロセス モデラー (BPM) は、テスト ケースのマスター ライブラリとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="72efa-168">BPM は、LCS プロジェクト間でテスト ライブラリを管理および配布するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="72efa-169">たとえば、Microsoft のパートナーまたはテスト ライブラリを構築している独立系ソフトウェア仕入先 (ISV) は、BPM ライブラリの形式でテスト ケースをリリースします。</span><span class="sxs-lookup"><span data-stu-id="72efa-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="72efa-170">BPM では、テスト ケースは業務プロセスごとにまとめられています。</span><span class="sxs-lookup"><span data-stu-id="72efa-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="72efa-171">BPM では、テスト パスの実行順序や頻度は定義されません。</span><span class="sxs-lookup"><span data-stu-id="72efa-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="72efa-172">このトピックで後述するように、これらの詳細は Azure DevOps で管理されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="72efa-173">LCS プロジェクトでは、既存の顧客実装またはパートナー プロジェクトを使用できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="72efa-174">LCS 言語を更新する</span><span class="sxs-lookup"><span data-stu-id="72efa-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-175">ユーザー インターフェイス (UI) で業務プロセスを正しく表示するには、LCS 優先言語を **英語 (米国)** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="72efa-176">LCS 実装プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="72efa-177">ページの右上隅にある **設定** ボタン (ギヤ記号) を選択して、**言語の基本設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![設定メニューのコマンド](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="72efa-179">**優先言語** フィールドで **英語 (米国)** を選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![ユーザー設定の言語の基本設定タブ](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="72efa-181">LCS プロジェクトを構成して Azure DevOps プロジェクトに接続する</span><span class="sxs-lookup"><span data-stu-id="72efa-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="72efa-182">以前に新しい Azure DevOps プロジェクトを作成した場合は、それに接続するように LCS プロジェクトを構成します。</span><span class="sxs-lookup"><span data-stu-id="72efa-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="72efa-183">LCS プロジェクトが既に Azure DevOps プロジェクトに接続されている場合は、次のセクションに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="72efa-184">LCS 実装プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="72efa-185">**メニュー** ボタンを選択し、**プロジェクトの設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![プロジェクト設定コマンド](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="72efa-187">左ウィンドウで、**Visual Studio Team Services** を選択し、**Visual Studio Team Services の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![プロジェクト設定の Visual Studio Team Services タブ](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="72efa-189">**Azure DevOps サイト URL** フィールドに、Azure DevOps サイトの URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="72efa-190">**個人用アクセス トークン** フィールドに、先ほど作成した個人用アクセス トークンを入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-191">VSTS は現在、Azure DevOps と呼ばれていますが、LCS を Azure DevOps プロジェクトに接続するためには、古い URL を使用します。</span><span class="sxs-lookup"><span data-stu-id="72efa-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="72efa-192">たとえば、このチュートリアルで使用する Azure DevOps URL は `https://dev.azure.com/D365FOFastTrack/` です。</span><span class="sxs-lookup"><span data-stu-id="72efa-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="72efa-193">ただし、次の図では、`https://D365FOFastTrack.visualstudio.com/` と入力されています。</span><span class="sxs-lookup"><span data-stu-id="72efa-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Visual Studio Team Services のステップ 1](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="72efa-195">**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-195">Select **Continue**.</span></span>
6. <span data-ttu-id="72efa-196">**Visual Studio Team Services プロジェクト** フィールドで、選択したサイトの VSTS プロジェクトを選択して、LCS プロジェクトにリンクさせます。</span><span class="sxs-lookup"><span data-stu-id="72efa-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="72efa-197">**プロセス テンプレート** フィールドは、既定で **アジャイル** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="72efa-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="72efa-198">カスタム テンプレートの場合は、[新しい Azure DevOps プロジェクトを作成する](#create-a-new-azure-devops-project) セクションのベスト プラクティスのガイダンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="72efa-199">その後 **続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-199">Then select **Continue**.</span></span>

    ![Visual Studio Team Services のステップ 2](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="72efa-201">設定を確認し、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-201">Review your settings, and then select **Save**.</span></span>

    ![Visual Studio Team Services のステップ 3](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="72efa-203">**承認** を選択すると、構成された Azure DevOps サイトに代理でアクセスし、VSTS と統合する機能を有効にすることを LCS に承認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![承認ボタン](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="72efa-205">「Lifecycle Services がユーザーに代わって Visual Studio Team Services に接続することを承認するために、外部サイトにリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="72efa-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="72efa-206">続行しますか?」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-206">Proceed?"</span></span> <span data-ttu-id="72efa-207">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-207">Select **Yes**.</span></span>

    ![メッセージ ボックス](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="72efa-209">**受け入れる** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-209">Select **Accept**.</span></span>

    ![アクセスを承認する](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="72efa-211">ユーザーとして承認されている場合、UI は LCS プロジェクト設定ページに戻る必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![承認されたユーザー](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="72efa-213">新しい BPM ライブラリの作成</span><span class="sxs-lookup"><span data-stu-id="72efa-213">Create a new BPM library</span></span>

1. <span data-ttu-id="72efa-214">LCS 実装プロジェクトに移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="72efa-215">**メニュー** ボタンを選択し、**ビジネス プロセス モデラー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![ビジネス プロセス モデラー コマンド](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="72efa-217">**新しいライブラリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-217">Select **New library**.</span></span>

    ![新しいライブラリ ボタン](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="72efa-219">**ライブラリの名前** フィールドで、名前を入力し、**作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="72efa-220">このチュートリアルでは、BPM ライブラリに **RSAT** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="72efa-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![新しいライブラリ ダイアログ ボックスを作成する](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="72efa-222">新しい **RSAT** BPM ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="72efa-223">**サンプル コア業務プロセス** プロセスを選択し、右側で **編集モード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![編集モード ボタン](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="72efa-225">**名前** フィールドと **説明** フィールドの両方の値を、**製品の作成** に変更します。</span><span class="sxs-lookup"><span data-stu-id="72efa-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="72efa-226">その後、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-226">Then select **Save**.</span></span>

    ![名前と説明フィールド](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="72efa-228">環境</span><span class="sxs-lookup"><span data-stu-id="72efa-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="72efa-229">バージョン要求</span><span class="sxs-lookup"><span data-stu-id="72efa-229">Version requirement</span></span>

<span data-ttu-id="72efa-230">バージョン 10 を実行するテスト環境またはサンドボックス環境が必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="72efa-231">バージョン 7.3、プラットフォーム更新プログラム 20 またはそれ以降を使用している場合もサポートされます。</span><span class="sxs-lookup"><span data-stu-id="72efa-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-232">RSAT は、Web ブラウザーを介してテスト環境にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="72efa-233">ユーザーの条件</span><span class="sxs-lookup"><span data-stu-id="72efa-233">User criteria</span></span>

<span data-ttu-id="72efa-234">ユーザーは、この環境に対して管理者権限を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="72efa-235">ヘルプ設定をセットアップして LCS に接続する</span><span class="sxs-lookup"><span data-stu-id="72efa-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="72efa-236">このステップは、クライアントを介して LCS の適切な BPM ライブラリにタスクの記録を保存できるように LCS と接続するために必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="72efa-237">クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-237">Open the client.</span></span>
2. <span data-ttu-id="72efa-238">**システム管理 \> 設定 \> システム パラメーター** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="72efa-239">**ヘルプ** タブの **Lifecycle Services ヘルプの構成** フィールドで、該当する LCS プロジェクト (このチュートリアルでは **RSAT**) を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![ヘルプ タブの Lifecycle Services ヘルプの構成フィールド](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="72efa-241">適切な LCS プロジェクトの下に、BPM ライブラリが入力されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="72efa-242">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-242">Select **Save**.</span></span>
5. <span data-ttu-id="72efa-243">更新されたヘルプの内容を表示するには、ブラウザーを更新する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![ブラウザーの更新に関する通知](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="72efa-245">タスクの記録</span><span class="sxs-lookup"><span data-stu-id="72efa-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-246">すべてのタスクの記録が、メイン ダッシュボードから開始していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="72efa-247">個々の記録を短くし、販売注文の作成など、1 つのビジネス タスクに注目します。</span><span class="sxs-lookup"><span data-stu-id="72efa-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="72efa-248">タスク記録を作成して BPM ライブラリに保存する</span><span class="sxs-lookup"><span data-stu-id="72efa-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="72efa-249">対応するタスク記録を作成します。これにより、新しい BPM ライブラリで作成された単純な業務プロセスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="72efa-250">クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-250">Open the client.</span></span>
2. <span data-ttu-id="72efa-251">メイン ダッシュボードで、**設定** ボタン (ギヤ記号) を選択し、**タスク レコーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![設定メニューのコマンド](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="72efa-253">**記録の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-253">Select **Create recording**.</span></span>

    ![記録ボタンの作成](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="72efa-255">**記録の名前** フィールドと **記録の説明** フィールドに入力し、**開始** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![記録の名前と記録の説明フィールド](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="72efa-257">製品を作成するステップを記録します。</span><span class="sxs-lookup"><span data-stu-id="72efa-257">Record the steps for creating a product.</span></span> <span data-ttu-id="72efa-258">完了したら、**停止** を選択して記録を停止します。</span><span class="sxs-lookup"><span data-stu-id="72efa-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![製品を作成するステップ](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="72efa-260">**Lifecycle Services に保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-260">Select **Save to Lifecycle Services**.</span></span>

    ![保存オプション](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="72efa-262">ライブラリ情報が LCS から読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="72efa-262">Library information is loaded from LCS.</span></span>

    ![進捗状況インジケーター](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="72efa-264">タスク記録に関連付ける BPM ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="72efa-265">このチュートリアルでは、先ほど作成した **RSAT** BPM ライブラリとその下にある **製品の作成** 業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="72efa-266">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-266">Then select **OK**.</span></span>

    ![タスク記録を BPM ライブラリと業務プロセスに関連付ける](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="72efa-268">「Lifecycle Services への保存が成功しました。」というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![LCS への保存に成功したことを示すメッセージ](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="72efa-270">タスク記録をローカルに保存してから LCS を介して BPM にアップロードする場合は、次のステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="72efa-271">記録が完了したら、**この PC に保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![保存オプション](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="72efa-273">ブラウザーの通知バーで、**保存** または **名前を付けて保存** を選択して、ローカル コンピューターにファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![通知バー](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="72efa-275">**RSAT** BPM ライブラリに移動し、タスク記録を保存する業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="72efa-276">**概要** タブで、**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-276">On the **Overview** tab, select **Upload**.</span></span>

        ![アップロード ボタン](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="72efa-278">**参照** をクリックし、先ほど保存した .axtr ファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="72efa-279">**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-279">Then select **Upload**.</span></span>

        ![アップロードする .axtr ファイルを選択する](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="72efa-281">BPMから Azure DevOps への同期をテストする</span><span class="sxs-lookup"><span data-stu-id="72efa-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="72efa-282">タスク記録が業務プロセスに関連付けられたので、LCS の VSTS 同期機能を使用して、業務プロセスとそれに関連するタスク記録を機能とテスト ケースとしてそれぞれ Azure DevOps に同期できることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-283">Azure DevOps で作成された対応する作業項目タイプは、[新しい Azure DevOps プロジェクトの作成](#create-a-new-azure-devops-project) セクションで説明されているように、Azure DevOps で LCS プロジェクトを構成したときに選択したプロセス テンプレートによって異なります。</span><span class="sxs-lookup"><span data-stu-id="72efa-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="72efa-284">BPM ライブラリに移動し、先ほど作成した **RSAT** ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="72efa-285">省略記号ボタン (**...**) を選択し、**VSTS 同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![省略記号メニューの VSTS 同期コマンド](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="72efa-287">VSTS の同期が完了すると、左側に **要件** タブが表示され、対応する Azure DevOps 作業項目が含まれます。</span><span class="sxs-lookup"><span data-stu-id="72efa-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-288">Azure DevOps で作成された作業項目には、タイトルの接頭語として BPM ライブラリ名が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="72efa-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![要件タブ](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="72efa-290">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="72efa-290">Refresh the page.</span></span>
4. <span data-ttu-id="72efa-291">省略記号ボタン (**...**) を選択すると、追加のオプションである **テスト ケースの同期** が表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="72efa-292">このオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-292">Select this option.</span></span>

    ![省略記号メニューのテスト ケースの同期コマンド](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-294">ページを更新した後で **テスト ケースの同期** オプションを使用できない場合は、BPMのメイン ページに移動し、ライブラリ自体の **テスト ケースの同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="72efa-295">このようにして、ライブラリ全体を効果的に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    > 
    > ![ライブラリ全体のテスト ケースの同期を選択する](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="72efa-297">テスト ケースの同期が完了すると、**要件** タブに新しいテスト ケースが作成されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![要求タブの新しいテスト ケース](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="72efa-299">Azure DevOps プロジェクトに移動し、**ボード\>作業項目** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![ボードの作業項目コマンド](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="72efa-301">BPM 同期によって作成した作業項目とテスト ケースが存在することを検証します。</span><span class="sxs-lookup"><span data-stu-id="72efa-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![作業項目とテスト ケース](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="72efa-303">RSAT のインストールと構成</span><span class="sxs-lookup"><span data-stu-id="72efa-303">Install and Configure RSAT</span></span>

<span data-ttu-id="72efa-304">RSAT は、Windows 10 を実行していて、Web ブラウザー (Internet Explorer または Google Chrome) を介して環境に接続できるすべてのコンピューターにインストールできます。</span><span class="sxs-lookup"><span data-stu-id="72efa-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-305">ツールの新しいバージョンをインストールする前に、以前のバージョンをアンインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72efa-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="72efa-306">認証証明書をインストールする</span><span class="sxs-lookup"><span data-stu-id="72efa-306">Install an authentication certificate</span></span>

<span data-ttu-id="72efa-307">認証を有効にするには、RSAT が実行されているのと同じコンピューターで証明書を生成してインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="72efa-308">証明書を生成する</span><span class="sxs-lookup"><span data-stu-id="72efa-308">Generate a certificate</span></span>

1. <span data-ttu-id="72efa-309">証明書ファイルを生成するには、管理者として Microsoft Windows PowerShell ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="72efa-310">**実行** ダイアログ ボックスに **certlm.msc** と入力して証明書マネージャーを開いて、**D365 自動テスト証明書** の証明書が **個人\>証明書** の下に作成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-311">証明書はローカル コンピューターに格納されているので、**certmgr.msc** ではなく、**certlm.msc** と入力してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 自動テスト証明書の証明書](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="72efa-313">証明書を右クリックし、**コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="72efa-314">**信頼済ルート証明機関 \> 証明書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![信頼済ルート証明機関フォルダの下の証明書フォルダ](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="72efa-316">**アクション** メニューの **貼り付け** を選択して、証明書を **信頼済ルート証明機関** にコピーします。</span><span class="sxs-lookup"><span data-stu-id="72efa-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![アクション メニューの貼り付けコマンド](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="72efa-318">インストールされている証明書の拇印を取得するには、スペースや特殊文字を使用しないで、管理者として Windows PowerShell ウィンドウを開き、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="72efa-319">後で Application Object Server (AOS) の .wif ファイルを更新し、RSAT 構成を設定するときに必要になるため、拇印を保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="72efa-320">接続を信頼するように AOS コンピューターを構成する</span><span class="sxs-lookup"><span data-stu-id="72efa-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="72efa-321">環境がレベル 2 以上である場合は、証明書の拇印は環境内の **すべての** AOS コンピューターの wif.config ファイルで更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="72efa-322">AOS コンピューターへのリモート デスクトップ プロトコル (RDP) 接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="72efa-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="72efa-323">サインインの詳細については、LCS の環境の詳細ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="72efa-324">Microsoft インターネット インフォメーション サービス (IIS) を開いて、サイトの一覧にある **AOSService** を検索します。</span><span class="sxs-lookup"><span data-stu-id="72efa-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![サイトの一覧にあるAOSService](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="72efa-326">**エクスプローラー** を右クリックして **\<Drive\>: \\AosService\\WebRoot** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="72efa-327">**wif.config** ファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="72efa-327">Find the **wif.config** file.</span></span>

    ![WebRoot フォルダーの Wif.config ファイル](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="72efa-329">次の例に示すように、証明書と機関名に対応する新しい機関のエントリを追加して、**wif.config** ファイルを更新します。</span><span class="sxs-lookup"><span data-stu-id="72efa-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="72efa-330">複数のユーザーが同一のアプリケーションを使用している場合は、各ユーザーが個別のサムプリントを生成する必要があり、それぞれのサムプリントは **\<keys\>** セクションで追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="72efa-331">複数の AOS コンピュータがある場合は、追加の各コンピュータに対してステップ 3 ~ 4 を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="72efa-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-332">従来のレベル 2 の環境とは異なり、新しいレベル 2 の環境は 2 つの AOS インスタンスを使用して配置されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="72efa-333">すべての AOS コンピューターで **iisreset** を実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-334">レベル 1 のコンピューターで **iisreset** を実行するための管理者権限を持っていない場合は、LCS の環境の詳細ページで、メンテナス > サービスの再起動を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="72efa-335">レベル 2 以上の環境</span><span class="sxs-lookup"><span data-stu-id="72efa-335">Tier 2+ environment</span></span>

<span data-ttu-id="72efa-336">レベル 2 以上 (スタンダード承認テスト サンドボックスまたはそれ以上) の環境を使用している場合は、RSAT がインストールされているコンピューターで次のレジストリ設定を確認または設定します。</span><span class="sxs-lookup"><span data-stu-id="72efa-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="72efa-337">認証または RSAT 接続エラーを回避するのに役立つため、このステップを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="72efa-338">RSAT をインストールする</span><span class="sxs-lookup"><span data-stu-id="72efa-338">Install RSAT</span></span>

1. <span data-ttu-id="72efa-339"><https://www.microsoft.com/download/details.aspx?id=57357> に移動して、**ダウンロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="72efa-340">すべてのファイルを選択し、**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-340">Select all the files, and then select **Next**.</span></span>

    ![すべてのファイルを選択する](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="72efa-342">.msi パッケージをダブルクリックして、インストーラーを実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="72efa-343">インストールが完了したら、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT インストーラー ファイル](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="72efa-345">Selenium およびブラウザー ドライバーをインストールする</span><span class="sxs-lookup"><span data-stu-id="72efa-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="72efa-346">以前のバージョンの RSAT では、Selenium とブラウザー ドライバーをインストールする必要がありました。</span><span class="sxs-lookup"><span data-stu-id="72efa-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="72efa-347">これらのドライバーは自動的にインストールされるため、インストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="72efa-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="72efa-348">RSAT を初めて開くときに、Selenium を自動的にダウンロードしてインストールするかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="72efa-349">詳細については、[RSAT を構成する](#configure-rsat) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="72efa-350">テスト ケースを実行する前に、RSAT の構成で選択されている既定のブラウザーに対応するブラウザー ドライバーを自動的にダウンロードしてインストールするかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="72efa-351">詳細については、[テスト ケースの読み込みと実行](#load-and-run-test-cases) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="72efa-352">RSAT の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="72efa-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="72efa-353">テスト計画およびテスト スイートを作成する</span><span class="sxs-lookup"><span data-stu-id="72efa-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="72efa-354">Azure DevOps プロジェクトに移動して、**テスト計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![テスト計画コマンド](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="72efa-356">**新しいテスト計画** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-356">Select **New Test Plan**.</span></span>

    ![新しいテスト計画ボタン](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="72efa-358">**名前** フィールドに入力し、**作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="72efa-359">このチュートリアルでは、テスト計画に **RSAT テスト計画** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="72efa-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![新しいテスト計画ダイアログ ボックス](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="72efa-361">プラス記号 (**+**) を選択し、**静的スイート** を選択して、新しいテスト計画の下に静的スイートを作成します。</span><span class="sxs-lookup"><span data-stu-id="72efa-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="72efa-362">新しいテスト スイートに **T01 ー 製造から在庫** という名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="72efa-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-363">BPM の新しいテスト ケースを自動的に RSAT テスト スイートに取り込む必要がある場合は、クエリ ベースのスイートを作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="72efa-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![静的スイートの作成](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="72efa-365">テスト ケースをテスト スイートに関連付ける</span><span class="sxs-lookup"><span data-stu-id="72efa-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="72efa-366">テスト スイートに既存のテスト ケースを追加するには、右側の **既存の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![既存の追加ボタン](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="72efa-368">**スイートにテスト ケースを追加** ページで **クエリの実行** を選択し、テスト スイートに追加するテスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="72efa-369">このチュートリアルでは、**新しい製品の作成** テスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="72efa-370">次に、ページの右下隅にある **テスト ケースの追加** を選択します (このボタンは次の図には示されていません)。</span><span class="sxs-lookup"><span data-stu-id="72efa-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![クエリの実行ボタン](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="72efa-372">**T01-製造から在庫** テスト スイートにテスト ケースが追加されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![テスト スイートに追加されたテスト ケース](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="72efa-374">RSAT のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="72efa-374">Configure RSAT</span></span>

1. <span data-ttu-id="72efa-375">RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-375">Open RSAT.</span></span>

    ![RSAT アイコン](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="72efa-377">「Regression Suite Automation Tool には Seleniumが必要です。今すぐ自動的にダウンロードしてインストールしますか?」という警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="72efa-378">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-378">Select **Yes**.</span></span>

    ![警告メッセージ](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="72efa-380">右上隅にある **設定** ボタン (ギヤ記号) を選択し、表示されるダイアログ ボックスで、次のフィールドに情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="72efa-381">**Azure DevOpsURL** ー Azure DevOps プロジェクトの URL (`https://yourAzureDevOpsUrlHere.visualStudio.com` など) を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="72efa-382">**アクセス トークン** ー ツールが Azure DevOps に接続できるアクセス トークンを入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="72efa-383">このチュートリアルで先ほど作成した個人用アクセス トークンを使用します。</span><span class="sxs-lookup"><span data-stu-id="72efa-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="72efa-384">詳細については、[個人用アクセス トークンを使用したアクセスの認証](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="72efa-385">**プロジェクトの名前** ー Azure DevOps プロジェクトの名前を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="72efa-386">**テスト計画** ー テスト ケースが含まれている Azure DevOps テスト計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="72efa-387">詳細については[テスト計画およびテスト スイートの作成](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="72efa-388">テスト計画を選択した後に **接続のテスト** を選択して Azure DevOps への接続をテストします。</span><span class="sxs-lookup"><span data-stu-id="72efa-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="72efa-389">**ホスト名** – **\<myaos\>.cloudax.dynamics.com** などのテスト環境のホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="72efa-390">**https://** または **http://** の接頭語を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="72efa-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="72efa-391">**SOAP ホスト名** ー テスト環境の SOAP ホスト名を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="72efa-392">通常、SOAP ホスト名はホスト名と同じですが、**soap** の接尾語が付いています。</span><span class="sxs-lookup"><span data-stu-id="72efa-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="72efa-393">次に例を示します: **\<myaos\>soap.cloudax.dynamics.com**。</span><span class="sxs-lookup"><span data-stu-id="72efa-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="72efa-394">**https://** または **http://** の接頭語を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="72efa-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="72efa-395">ホスト名と SOAP ホスト名を検索するには、IIS マネージャーを開き、**サイト \> AOSService** を右クリックして、**バインディングの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="72efa-396">**ホスト名** 列の値によって、ホスト名と SOAP ホスト名が指定されます (SOAP ホスト名の URL には接尾語 **soap** が使用されています)。</span><span class="sxs-lookup"><span data-stu-id="72efa-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![ホスト名列のホスト名と SOAP ホスト名](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="72efa-398">**管理者ユーザー名** ー テスト環境の管理者ユーザーの電子メール アドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="72efa-399">**拇印** ー このチュートリアルの前の説明に従って、認証証明書の拇印を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="72efa-400">**作業ディレクトリ** ー Excel テスト データ ファイルなどのテスト自動化ファイルを格納するフォルダの場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="72efa-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="72efa-401">たとえば、**C:\\Temp\\RegressionTool** と入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="72efa-402">フォルダの名前にスペースが含まれている場合は、フォルダが見つからないために実行が失敗します。</span><span class="sxs-lookup"><span data-stu-id="72efa-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="72efa-403">この問題は既知の問題であり、ツールの最新バージョンで修正する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="72efa-404">**既定のブラウザー** – **Internet Explorer** または **Google Chrome** のいずれかを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="72efa-405">適切なブラウザー ドライバーがインストールされていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="72efa-406">**テストの実行タイムアウト** – テストの実行のタイムアウト期間を分単位で指定します。</span><span class="sxs-lookup"><span data-stu-id="72efa-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="72efa-407">タイムアウト期間が経過すると、すべてのアクティブなウィンドウが閉じられ、保留中のテスト ケースは終了します。</span><span class="sxs-lookup"><span data-stu-id="72efa-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="72efa-408">**テスト アクション タイムアウト** ー このフィールドは Finance and Operation 環境のサーバー要求のタイムアウト期間を分単位で制御します。</span><span class="sxs-lookup"><span data-stu-id="72efa-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="72efa-409">通常は、既定値 (2 分) で十分です。</span><span class="sxs-lookup"><span data-stu-id="72efa-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="72efa-410">ただし、低速な環境では、タイムアウトに関連するエラーが発生する場合、値を増やすことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72efa-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="72efa-411">**会社名** ー Excel パラメーター ファイルを作成するときに、既定の会社として使用する会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="72efa-412">後で Excel パラメーター ファイルを編集して会社を変更できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![設定ダイアログ ボックス](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="72efa-414">**適用** を選択して、設定を適用または保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="72efa-415">使用しているコンピューターの構成ファイルに現在の設定を保存するには、**名前を付けて保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="72efa-416">使用しているコンピューターの構成ファイルから設定を復元するには、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="72efa-417">**閉じる** を選択して、ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="72efa-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="72efa-418">テスト ケースの読み込みと実行</span><span class="sxs-lookup"><span data-stu-id="72efa-418">Load and run test cases</span></span>

1. <span data-ttu-id="72efa-419">Azure DevOps プロジェクトから **RSAT テスト計画** のテスト計画を読み込むには、**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![読み込みボタン](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="72efa-421">テスト スイートから **新しい製品の作成** テスト ケースを選択し、**新規 \> テスト実行とパラメーター ファイルの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![新しいメニューにテスト実行とパラメーター ファイルを生成する](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="72efa-423">Excel パラメーター ファイルは RSAT 構成 (たとえば、**C:\\Temp\\RegressionTool**) で指定したローカル フォルダーに作成されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![作成された Excel パラメーター ファイル](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="72efa-425">パラメーター ファイルを保存する場合は、**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="72efa-426">選択したすべてのテスト ケースのテスト自動化ファイルは、将来使用するために Azure DevOps にアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="72efa-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="72efa-427">(これらのファイルには、Excel テスト パラメーター ファイルが含まれています。)</span><span class="sxs-lookup"><span data-stu-id="72efa-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="72efa-428">このようにして、**読み込み** を選択して、パラメーター ファイル (および自動化ファイル) をテストケースから直接 Azure DevOps から読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="72efa-429">パラメーター ファイルを再生成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="72efa-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="72efa-430">この方法は、後でパラメーター ファイルに変更を保持し、それらを上書きしたくない場合に重要になります。</span><span class="sxs-lookup"><span data-stu-id="72efa-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="72efa-431">自動化ファイルおよびパラメーター ファイルが Azure DevOps に保存されていることを確認するには、Azure DevOps プロジェクトに移動して、**ボード  \> 作業項目** を選択し、**新しい製品の作成** テスト ケースを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="72efa-432">**添付ファイル** タブには、次の 4 つのファイルが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="72efa-433">**.cs** – C\# 自動化ファイル</span><span class="sxs-lookup"><span data-stu-id="72efa-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="72efa-434">**.dll** ー アセンブリとしてコンパイルされた自動化ファイル</span><span class="sxs-lookup"><span data-stu-id="72efa-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="72efa-435">**.xlsx** – Excel パラメーター ファイル</span><span class="sxs-lookup"><span data-stu-id="72efa-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="72efa-436">**.xml** – 記録ファイル</span><span class="sxs-lookup"><span data-stu-id="72efa-436">**.xml** – Recording file</span></span>

    ![添付ファイル タブのファイル](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="72efa-438">実行するテスト ケースを選択し、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-439">テスト ケースを実行する前に、ブラウザーとして Internet Explorer を使用している場合は、**Windows のディスプレイ設定 \> 拡大縮小とレイアウト** でデスクトップの解像度が **100%** に設定されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="72efa-440">仮想マシン (VM) でこの設定を変更できない場合は、VM にアクセスしようとしているクライアント (ラップトップ) で変更します。</span><span class="sxs-lookup"><span data-stu-id="72efa-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="72efa-441">解像度の設定は、VM の表示設定に継承されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![100% に設定されたデスクトップの解像度](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="72efa-443">ブラウザー ドライバーがシステムにインストールされていない場合は、次のような警告メッセージが表示されます: "この操作には \<browser name\> ドライバーが必要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="72efa-444">今すぐ自動的にダウンロードしてインストールしますか?」という警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="72efa-445">**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-445">Select **Yes**.</span></span>

    ![Internet Explorer の警告メッセージ](./media/setup_rsa_tool_69.png)

    ![Chrome の警告メッセージ](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-448">ブラウザーとして Chrome を使用していて、Chrome バージョンが正しくないためにセッションが作成されなかったことを示すエラー メッセージが表示された場合は、最新の Chrome を<http://chromedriver.chromium.org/downloads> から **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** フォルダーにダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="72efa-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Chrome のエラー メッセージ](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="72efa-450">テスト ケースが実行され、**結果** フィールドが更新されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-450">The test case is run, and the **Result** field is updated.</span></span>

    ![進捗状況インジケーター](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="72efa-452">このチュートリアルに従っている場合は、製品を作成するためのタスク記録で製品名をハードコーディングされた値として保存しているので、**新しい製品の作成** テスト ケースは失敗します。</span><span class="sxs-lookup"><span data-stu-id="72efa-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="72efa-453">同じテスト ケースを再実行すると、製品が既に存在するため、エラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![失敗に設定された結果フィールド](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="72efa-455">テスト結果の表示</span><span class="sxs-lookup"><span data-stu-id="72efa-455">View the test results</span></span>

1. <span data-ttu-id="72efa-456">失敗したテスト ケースをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="72efa-457">エラー メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="72efa-457">You receive an error message.</span></span>

    ![エラー メッセージ](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="72efa-459">**詳細** を選択すると、エラー メッセージの全体が表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-459">Select **Details** to view the whole error message.</span></span>

    ![エラー メッセージの全体](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="72efa-461">Azure DevOps で詳細なバージョンのエラー メッセージを表示するには、**Azure DevOps で開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="72efa-462">Azure DevOps では、テスト ケースと詳細なエラー メッセージの状態を表示できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Azure DevOps の詳細なエラー メッセージ](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="72efa-464">Azure DevOps プロジェクトでテスト結果を直接表示するには、**テスト計画\>テスト計画\>実行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="72efa-465">詳細を表示するテストの実行をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="72efa-465">Double-click the test run that you want to see more details for.</span></span>

    ![Azure DevOps でのテストの実行の一覧](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="72efa-467">**実行の概要** タブには、テスト ケースが失敗したことが示されますが、実際のエラー メッセージは表示されません。</span><span class="sxs-lookup"><span data-stu-id="72efa-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="72efa-468">詳細なエラー メッセージを表示するには、**テスト結果** タブを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![実行の概要タブ](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="72efa-470">**テスト結果** タブには、テスト ケースの情報と共に、結果とエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![テスト結果タブ](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="72efa-472">関連するレコードをダブルクリックして、詳細なエラー メッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="72efa-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![詳細なエラー メッセージ](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-474">すべてのエラー メッセージは、**C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt** でローカルでも利用可能です。</span><span class="sxs-lookup"><span data-stu-id="72efa-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="72efa-475">**エクスポート** を選択して、テスト計画レベルでテストの実行の結果をエクスポートすることもできます。</span><span class="sxs-lookup"><span data-stu-id="72efa-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![テスト計画のエクスポート](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="72efa-477">Excel パラメーター ファイルの変更</span><span class="sxs-lookup"><span data-stu-id="72efa-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="72efa-478">RSAT を開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-478">Open RSAT.</span></span>
2. <span data-ttu-id="72efa-479">テスト ケースを選択し、**編集** を選択して Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="72efa-480">**EcoResProductCreate** シートで、**製品番号** フィールドの値がハードコーディングされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="72efa-481">テスト ケースを再度実行する前に、このフィールドを新しい製品番号に更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="72efa-482">Excel パラメーター ファイルを再度開いて製品番号を毎回手動で更新することなく、実行ごとに一意の製品番号を生成するには、次の Excel の式を使用します。</span><span class="sxs-lookup"><span data-stu-id="72efa-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="72efa-483">**一般** タブに加えて、Excel パラメーター ファイルには、テスト ケースがアクセスするすべてのフォーム ページのデータ タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="72efa-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![製品番号フィールド](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="72efa-485">**保存** を選択して、Excel ブックを閉じます。</span><span class="sxs-lookup"><span data-stu-id="72efa-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="72efa-486">**アップロード** を選択して Excel パラメーター ファイルを Azure DevOps に保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![ファイルのアップロードに成功したことを示すメッセージ](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-488">特定のユーザー コンテキストでテスト ケースを実行するには、Excel パラメーター ファイルの **一般** タブの **テスト ユーザー** フィールドにユーザーの電子メール ID を入力します。</span><span class="sxs-lookup"><span data-stu-id="72efa-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="72efa-489">最新バージョンの RSAT では、Excel パラメーター ファイルのフィールドのレイアウトは更新されていますが、概念は同じです。</span><span class="sxs-lookup"><span data-stu-id="72efa-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![テスト ユーザー フィールド](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="72efa-491">結果の検証</span><span class="sxs-lookup"><span data-stu-id="72efa-491">Validate the results</span></span>

- <span data-ttu-id="72efa-492">**実行** を選択してテスト ケースを再実行し、テスト ケースが成功したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="72efa-493">テスト結果は、[テスト結果の表示](#view-the-test-results) セクションの説明に従って表示できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![成功に設定された結果フィールド](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="72efa-495">テスト ケースの連鎖</span><span class="sxs-lookup"><span data-stu-id="72efa-495">Chaining of test cases</span></span>

<span data-ttu-id="72efa-496">RSAT の主要な機能の 1 つとして、テスト ケースの連鎖 (つまり、テストが他のテストに値を渡す機能) があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="72efa-497">テスト ケースは、Azure DevOps テスト計画で定義された順序に従って実行されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="72efa-498">(この順序は、テスト ツール自体で更新することもできます)。したがって、あるテスト ケースから別のテスト ケースに変数を渡す場合は、テストが正しい順序であることが非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="72efa-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="72efa-499">このセクションでは、最初のテスト ケースで保存された変数を作成し、2 番目のテスト ケースを作成して、保存された変数を最初のテスト ケースから 2 番目のテスト ケースに渡します。</span><span class="sxs-lookup"><span data-stu-id="72efa-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="72efa-500">その後、テスト ケースを連鎖したテスト ケースとして RSAT で実行します。</span><span class="sxs-lookup"><span data-stu-id="72efa-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="72efa-501">既存のタスク記録を変更して保存された変数を作成する</span><span class="sxs-lookup"><span data-stu-id="72efa-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="72efa-502">クライアントを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-502">Open the client.</span></span>
2. <span data-ttu-id="72efa-503">**設定** ボタン (ギヤ記号) を選択し、**タスク レコーダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="72efa-504">**記録の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-504">Select **Edit Recording**.</span></span>

    ![記録の編集ボタン](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="72efa-506">**Lifecycle Services から開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-506">Select **Open from Lifecycle Services**.</span></span>

    ![Lifecycle Services から開くボタン](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="72efa-508">**Lifecycle Services ライブラリを選択する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Lifecycle Services ライブラリの選択ボタン](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="72efa-510">BPM ライブラリが LCS から読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="72efa-510">BPM libraries are loaded from LCS.</span></span>

    ![進捗状況インジケーター](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="72efa-512">BPM ライブラリが LCS から読み込まれたら、**RSAT** BPM ライブラリと、タスク記録が関連付けられていた **新しい製品の作成** 業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="72efa-513">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-513">Then select **OK**.</span></span>

    ![BPM ライブラリと業務プロセスの選択](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="72efa-515">適切なタスク記録の名前が **記録の名前** フィールドに入力されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="72efa-516">**スタート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-516">Select **Start**.</span></span>

    ![記録の名前フィールド内のタスク記録の名前](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="72efa-518">**製品情報管理\>製品** に移動し、**新規** を選択すると、元のタスク記録や **製品の作成** などが記録されたページが開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="72efa-519">**ステップの挿入** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-520">新しいステップは、ウィンドウで選択したステップの **後に** 挿入されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![ステップの挿入ボタン](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="72efa-522">**製品番号** フィールドを右クリックし、**タスク レコーダー \> コピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![コピー コマンド](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="72efa-524">新しいステップがウィンドウに追加されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-524">A new step is added in the pane.</span></span> <span data-ttu-id="72efa-525">後で必要になるため、**製品番号** フィールドの値をメモしておきます。</span><span class="sxs-lookup"><span data-stu-id="72efa-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![追加された新しいステップ](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="72efa-527">**編集の完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="72efa-528">**Lifecycle Services に保存** を選択し、新しいタスク記録を、元のタスク記録が関連付けられていたのと同じ BPM ライブラリおよび業務プロセスに関連付けます。</span><span class="sxs-lookup"><span data-stu-id="72efa-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="72efa-529">詳細については、[タスクの記録の作成と BPM ライブラリへの保存](#create-a-task-recording-and-save-it-to-the-bpm-library) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="72efa-530">BPM ライブラリに移動し、[BPM から Azure DevOps への同期のテスト](#test-the-synchronization-from-bpm-to-azure-devops) セクションで説明しているように、**テスト ケースの同期** を選択して、Azure DevOps のテス トケースに関連付けられているタスク記録を上書きします。</span><span class="sxs-lookup"><span data-stu-id="72efa-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="72efa-531">RSAT を開き、**読み込み** を選択して、テスト スイート内のすべてのテスト ケースを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="72efa-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="72efa-532">[テスト ケースの読み込みと実行](#load-and-run-test-cases) セクションの説明に従って、テスト ケースを選択し、**新規 \> テストの実行とパラメーター ファイルの生成** を選択することによって、適切なテスト ケースの自動化ファイルとパラメーター ファイルを再生成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-533">Excel パラメーター ファイルを開いたままにしておくと、再生成に失敗します。</span><span class="sxs-lookup"><span data-stu-id="72efa-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="72efa-534">したがって、新しい Excel パラメーター ファイルを生成する前に、テスト ケースの Excel パラメーター ファイルが閉じられていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="72efa-535">**編集** を選択して新しい Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="72efa-536">新しい **保存された変数** のエントリが、行 9 に表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="72efa-537">この変数 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** はタスク記録の XML ファイルに保存され、後続のテストで使用できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![保存された変数エントリ](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="72efa-539">新しいテスト ケースの作成</span><span class="sxs-lookup"><span data-stu-id="72efa-539">Create a new test case</span></span>

1. <span data-ttu-id="72efa-540">**RSAT** BPM ライブラリに移動します。</span><span class="sxs-lookup"><span data-stu-id="72efa-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="72efa-541">**サンプル サポート業務プロセス** プロセスを選択し、右側で **編集モード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="72efa-542">**名前** フィールドと **説明** フィールドの両方の値を、**製品のリリース** に変更します。</span><span class="sxs-lookup"><span data-stu-id="72efa-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="72efa-543">その後、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-543">Then select **Save**.</span></span>

    ![製品のリリースに変更された名前と説明](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="72efa-545">検証機能を持つ新しいタスク記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="72efa-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="72efa-546">先ほど作成した製品を USRT 法人にリリースするためのタスクの記録を作成します。</span><span class="sxs-lookup"><span data-stu-id="72efa-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="72efa-547">詳細については、[タスクの記録の作成と BPM ライブラリへの保存](#create-a-task-recording-and-save-it-to-the-bpm-library) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="72efa-548">連鎖したテスト ケースでは、*フィールドの値を手動で入力する* ことによって、必要なレコードを検出またはフィルター処理することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72efa-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="72efa-549">このようにして、ツールは、後続のテスト ケースでアクションを実行する必要があるレコードを決定できます。</span><span class="sxs-lookup"><span data-stu-id="72efa-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![検証機能を持つ新しいタスク記録](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="72efa-551">上の図に示されているように、クイック フィルターを使用して製品を検出した後、**製品のリリース** を選択する前に、**製品番号** フィールドの値を検証して、製品 ID が以前に作成された製品 ID であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="72efa-552">値を検証するには、**製品番号** フィールドを右クリックして、**タスク レコーダー \> 検証 \> 現在の値** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![現在の値の検証](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="72efa-554">タスク記録を BPM に保存する</span><span class="sxs-lookup"><span data-stu-id="72efa-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="72efa-555">タスク記録が完了したら、**Lifecycle Services に保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![保存オプション](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="72efa-557">ライブラリ情報が LCS から読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="72efa-557">Library information is loaded from LCS.</span></span>

    ![進捗状況インジケーター](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="72efa-559">タスク記録に関連付ける BPM ライブラリを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="72efa-560">このチュートリアルでは、先ほど作成した **RSAT** BPM ライブラリとその下にある **製品のリリース** 業務プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="72efa-561">その後、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="72efa-562">BPM を Azure DevOps に同期する</span><span class="sxs-lookup"><span data-stu-id="72efa-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="72efa-563">BPM ライブラリに移動して、**RSAT** ライブラリを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="72efa-564">**VSTS 同期** を選択し、**テスト ケースを同期** します。</span><span class="sxs-lookup"><span data-stu-id="72efa-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="72efa-565">詳細については、[BPM から Azure DevOps への同期をテストする](#test-the-synchronization-from-bpm-to-azure-devops) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72efa-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="72efa-566">同期が完了したら、新しい作業項目と、**製品のリリース** 業務プロセスの対応するテスト ケースが、**ボード \> 作業項目** の Azure DevOps に表示されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="72efa-567">既存のテスト スイートに新しいテスト ケースを追加する</span><span class="sxs-lookup"><span data-stu-id="72efa-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="72efa-568">**テスト計画 \> テスト計画** に移動し、**RSAT テスト計画** 計画を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="72efa-569">**既存の追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="72efa-570">**スイートにテスト ケースを追加** ページで、**クエリの実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="72efa-571">**製品のリリース** に対して作成された新しいテスト ケースを選択し、ページの右下隅にある **テスト ケースの追加** を選択します (このボタンは次の図には示されていません)。</span><span class="sxs-lookup"><span data-stu-id="72efa-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![スイートにテスト ケースを追加ページ](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="72efa-573">テスト スイートには、2 つのテスト ケースが含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="72efa-573">The test suite now has two test cases.</span></span>

    ![テスト スイートの 2 つのテスト ケース](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="72efa-575">テストケースの RSAT への読み込み</span><span class="sxs-lookup"><span data-stu-id="72efa-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="72efa-576">RSAT を開き、**読み込み** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="72efa-577">テスト ケースが読み込まれ、「このアクションは Excel のテスト データ ファイルを上書きします」という警告が表示され、ローカルの変更が失われます。</span><span class="sxs-lookup"><span data-stu-id="72efa-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="72efa-578">続行しますか?</span><span class="sxs-lookup"><span data-stu-id="72efa-578">Do you want to proceed?"</span></span> <span data-ttu-id="72efa-579">**はい** を選択すると、Azure DevOps にアップロードされた Excel パラメーター ファイルではなく、ローカル システムの Excel パラメーター ファイルが更新されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![警告メッセージ](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="72efa-581">両方のテスト ケースが、最初のテスト ケースの Excel パラメーター ファイルと共に読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="72efa-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="72efa-582">前回の実行で **アップロード** を選択したため、パラメーター ファイルが Azure DevOps から引き出されます。</span><span class="sxs-lookup"><span data-stu-id="72efa-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![読み込まれたテスト ケース](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="72efa-584">2 番目のテスト ケースのみを選択して、**新規 \> テスト実行とパラメーター ファイルの生成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="72efa-585">Excel パラメーター ファイルの編集</span><span class="sxs-lookup"><span data-stu-id="72efa-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="72efa-586">2 番目のテスト ケースのみを選択し、**編集** を選択して対応する Excel パラメーター ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="72efa-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="72efa-587">保存された変数 **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** を最初のテスト ケースから製品番号が使用されているすべてのフィールドへコピーします ([既存のタスク記録を変更して保存された変数を作成する](#modify-an-existing-task-recording-to-create-a-saved-variable) セクションを参照してください)。</span><span class="sxs-lookup"><span data-stu-id="72efa-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="72efa-588">この場合、変数を **EcoResProductListPage** シートの **製品番号** フィールドと **製品番号の検証** フィールドにコピーします。</span><span class="sxs-lookup"><span data-stu-id="72efa-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![製品番号と製品番号の検証フィールド](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="72efa-590">変数は、同じテストの実行中にのみテスト間で受け渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="72efa-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="72efa-591">変数の名前は完全に一致している必要があります。</span><span class="sxs-lookup"><span data-stu-id="72efa-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="72efa-592">**保存** を選択して、Excel ブックを閉じます。</span><span class="sxs-lookup"><span data-stu-id="72efa-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="72efa-593">**アップロード** を選択して、Excel パラメーター ファイルに加えた変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="72efa-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="72efa-594">連鎖したテスト ケースの実行</span><span class="sxs-lookup"><span data-stu-id="72efa-594">Run the chained test cases</span></span>

1. <span data-ttu-id="72efa-595">両方のテスト ケースを選択し、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="72efa-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="72efa-596">両方のテスト ケースが成功していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="72efa-596">Verify that both test cases have passed.</span></span>

    ![両方のテスト ケースに対して成功に設定された結果フィールド](./media/setup_rsa_tool_105.png)
