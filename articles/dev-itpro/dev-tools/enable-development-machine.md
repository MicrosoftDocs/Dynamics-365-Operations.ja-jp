---
title: "開発マシンでの新しいユーザーの作成"
description: "環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。 この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。"
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 31621
ms.assetid: c56d5cdf-3c01-4730-bda5-bb5f8f79e375
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 7f520439afe7b30c02e293803072649bccf69eec
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="create-a-new-user-on-a-development-machine"></a><span data-ttu-id="c1739-104">開発マシンでの新しいユーザーの作成</span><span class="sxs-lookup"><span data-stu-id="c1739-104">Create a new user on a development machine</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1739-105">この記事では、開発者が開発 VM に別のユーザー アカウントを有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="c1739-105">This article explains how to enable another user account as a developer on a development VM.</span></span>

<span data-ttu-id="c1739-106">環境が最初に配置されるとき、1 つのユーザー アカウントのみが仮想マシン (VM)上で開発者として有効になります。</span><span class="sxs-lookup"><span data-stu-id="c1739-106">When an environment is first deployed, only one user account is enabled as a developer on the virtual machine (VM).</span></span> <span data-ttu-id="c1739-107">このユーザーは、Microsoft Dynamics Lifecycle Services (LCS) によって事前設定するか、ダウンロードした仮想ハードディスク (VHD) のローカル管理者のアカウントです。</span><span class="sxs-lookup"><span data-stu-id="c1739-107">This user is preconfigured by Microsoft Dynamics Lifecycle Services (LCS) or is the local administrator account on downloaded virtual hard disks (VHDs).</span></span> <span data-ttu-id="c1739-108">ただし、新しいユーザー アカウントを VM で開発できます。</span><span class="sxs-lookup"><span data-stu-id="c1739-108">However, you can enable a new user account to develop on the VM.</span></span> <span data-ttu-id="c1739-109">新しいアカウントを有効にした後でも、同じ VM/アプリケーションで一度に開発できる開発者は 1 人だけです。</span><span class="sxs-lookup"><span data-stu-id="c1739-109">Even after you enable a new account, only one developer can develop at a time on the same VM/application.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c1739-110">前提条件</span><span class="sxs-lookup"><span data-stu-id="c1739-110">Prerequisites</span></span>
<span data-ttu-id="c1739-111">新しいユーザー アカウントが VM で開発できるようにするには、ユーザー アカウントが VM の管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1739-111">To enable a new user account to develop on the VM, the user account must be an administrator on the VM.</span></span> <span data-ttu-id="c1739-112">また、既定の開発者アカウントの資格情報を使用して VM にログオンする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1739-112">Additionally, you must log on to the VM by using the credentials of the default developer account.</span></span> <span data-ttu-id="c1739-113">VM が Microsoft Azure VM である場合は、この勘定の情報は LCS の環境のページで使用できます。</span><span class="sxs-lookup"><span data-stu-id="c1739-113">If the VM is a Microsoft Azure VM, the account information is available on the environment page in LCS.</span></span> <span data-ttu-id="c1739-114">VM がダウンロードした VHD 上で実行されるローカル VM である場合は、ローカル管理者アカウントを使用します。</span><span class="sxs-lookup"><span data-stu-id="c1739-114">If the VM is a local VM that runs on the downloaded VHD, use the local administrator account.</span></span> <span data-ttu-id="c1739-115">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1739-115">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="steps"></a><span data-ttu-id="c1739-116">ステップ</span><span class="sxs-lookup"><span data-stu-id="c1739-116">Steps</span></span>
1.  <span data-ttu-id="c1739-117">スクリプト ProvisionAxDeveloper.ps1 をダウンロードしてください。スクリプトは、<https://github.com/Microsoft/Dynamics-AX-Scripts> で利用可能です。</span><span class="sxs-lookup"><span data-stu-id="c1739-117">Download the following script: ProvisionAxDeveloper.ps1, the script is available at <https://github.com/Microsoft/Dynamics-AX-Scripts>.</span></span>
2.  <span data-ttu-id="c1739-118">Microsoft Windows **PowerShell コマンド プロンプト** ウィンドウを管理者として開きます。</span><span class="sxs-lookup"><span data-stu-id="c1739-118">Open a Microsoft Windows **PowerShell Command Prompt** window as an administrator.</span></span>
3.  <span data-ttu-id="c1739-119">ProvisionAxDeveloper.ps1 スクリプトを実行します。</span><span class="sxs-lookup"><span data-stu-id="c1739-119">Run the ProvisionAxDeveloper.ps1 script.</span></span> <span data-ttu-id="c1739-120">次のパラメーターを指定します。</span><span class="sxs-lookup"><span data-stu-id="c1739-120">Specify the following parameters:</span></span>

    -   <span data-ttu-id="c1739-121">**DatabaseServerName** - 通常、これは、コンピューター名です。</span><span class="sxs-lookup"><span data-stu-id="c1739-121">**DatabaseServerName** – Typically, this is the machine name.</span></span>
    -   <span data-ttu-id="c1739-122">**ユーザー** – 次の形式を使用します: &lt;ドメインまたはコンピューター名&gt;\\ユーザー 1、…</span><span class="sxs-lookup"><span data-stu-id="c1739-122">**Users** – Use the following format: &lt;domain or machine name&gt;\\user1, …</span></span> <span data-ttu-id="c1739-123">&lt;ドメインまたはコンピューター名&gt;\\ユーザー n</span><span class="sxs-lookup"><span data-stu-id="c1739-123">&lt;domain or machine name&gt;\\user n</span></span>

    <span data-ttu-id="c1739-124">**例**</span><span class="sxs-lookup"><span data-stu-id="c1739-124">**Examples**</span></span>

        > ProvisionAxDeveloper.ps1 RDXP00DB20RAINM RDXP00DB20RAINM\username1

        > ProvisionAxDeveloper.ps1 -databaseservername RDXP00DB20RAINM -users RDXP00DB20RAINM\username1,RDXP00DB20RAINM\username2

4.  <span data-ttu-id="c1739-125">1 つ以上のユーザー アカウントが同じバージョン管理ワークスペース上で開発されている場合、ワークスペースをパブリックにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1739-125">If more than one user account will be developing on the same version control workspace, you need to make the workspace public.</span></span>
    1.  <span data-ttu-id="c1739-126">Visual Studio で、**ソース管理エクスプローラー**を開き、ワークスペース ドロップダウンを選択し、**ワークスペースの管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="c1739-126">In Visual Studio, open **Source Control Explorer**, select the workspace dropdown and select **Manage workspaces**.</span></span>
    2.  <span data-ttu-id="c1739-127">アプリケーション ワークスペースを選択して、**編集** をクリックし、**詳細** をクリックしてワークスペースを **パブリック ワークスペース**.[![publicworkspace](./media/publicworkspace.png)](./media/publicworkspace.png) にせっていします</span><span class="sxs-lookup"><span data-stu-id="c1739-127">Select the application workspace, click **Edit,** then click **Advanced** and set the workspace to **Public workspace**.[![publicworkspace](./media/publicworkspace.png)](./media/publicworkspace.png)</span></span>






