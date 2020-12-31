---
title: RCS で ER コンフィギュレーションを作成し、グローバル リポジトリにアップロードする
description: このトピックでは、Microsoft Regulatory Configuration Service (RCS) の電子レポート (ER) の構成を作成する方法と、グローバル レポジトリにアップロードする方法ついて説明します。
author: JaneA07
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace, RCS
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 5b2b8f35b9931f8fd1824c20e9045da68af33ad5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4445246"
---
# <a name="create-er-configurations-in-regulatory-configuration-services-rcs-and-upload-them-to-the-global-repository"></a><span data-ttu-id="3db69-103">Regulatory Configuration Services (RCS) で ER の構成を作成し、グローバル リポジトリにアップロードする</span><span class="sxs-lookup"><span data-stu-id="3db69-103">Create ER configurations in Regulatory Configuration Services (RCS) and upload them to the Global repository</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3db69-104">Microsoft Regulatory Configuration Service (RCS) を使用して電子レポート (ER) の構成を設計し、組織内で使えるように公開することができます。</span><span class="sxs-lookup"><span data-stu-id="3db69-104">You can use Microsoft Regulatory Configuration Services (RCS) to design Electronic reporting (ER) configurations and publish them so that they can be used in your organization.</span></span>

<span data-ttu-id="3db69-105">以下の手順では、システム管理者 または電子レポートの開発者ロールを持つユーザーが、RCS インスタンスで構成された ER 構成の派生バージョンを作成し、派生する構成をグローバル リポジトリにアップロードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="3db69-105">The following procedures explain how a user in the System Administrator or Electronic Reporting Developer role can create a derived version of an ER configuration that has been configured in an RCS instance, and then upload the derived configuration to the Global repository.</span></span> 

<span data-ttu-id="3db69-106">この手順を完了する前に、まず以下の手順を完了する必要があります:</span><span class="sxs-lookup"><span data-stu-id="3db69-106">Before you can complete those procedures, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="3db69-107">RCS インスタンスへのアクセス権。</span><span class="sxs-lookup"><span data-stu-id="3db69-107">Access an RCS instance.</span></span>
- <span data-ttu-id="3db69-108">有効な構成プロバイダーを作成する。</span><span class="sxs-lookup"><span data-stu-id="3db69-108">Create an active configuration provider.</span></span> <span data-ttu-id="3db69-109">詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3db69-109">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="3db69-110">また、RCS 環境がプロビジョニングされていることを確認しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db69-110">You must also make sure that an RCS environment is provisioned for your company.</span></span>

1. <span data-ttu-id="3db69-111">Finance and Operations アプリで、**組織管理** \> **ワークスペース** \> **電子レポート** に移動します。</span><span class="sxs-lookup"><span data-stu-id="3db69-111">In a Finance and Operations app, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="3db69-112">RCS 環境がご利用の会社にプロビジョニングされていない場合は、**Regulatory services – 外部の構成** を選択し、続いてプロビジョニングの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="3db69-112">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration external**, and then follow the instructions to provision one.</span></span>

<span data-ttu-id="3db69-113">RCS 環境が既にプロビジョニングされている場合は、[サインイン] オプションを選択して、ページの URL を使用してこの機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="3db69-113">If an RCS environment has been already provisioned for your company, use the page URL to access it by selecting the sign-in option.</span></span>

## <a name="create-a-derived-version-of-a-configuration-in-rcs"></a><span data-ttu-id="3db69-114">RCS で構成の派生バージョンを作成する</span><span class="sxs-lookup"><span data-stu-id="3db69-114">Create a derived version of a configuration in RCS</span></span>

1. <span data-ttu-id="3db69-115">**電子レポート** ワークスペースで、ご利用の組織に対して有効な構成プロバイダーがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3db69-115">In the **Electronic reporting** workspace, verify that you have an active configuration provider for your organization.</span></span> 
2. <span data-ttu-id="3db69-116">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-116">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="3db69-117">新しいバージョンを派生させる構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-117">Select the configuration that you want to derive a new version from.</span></span> <span data-ttu-id="3db69-118">ツリーの上にあるフィルターフィールドを使用して検索を絞り込むことができます。</span><span class="sxs-lookup"><span data-stu-id="3db69-118">You can use the filter field above the tree to narrow your search.</span></span>
4. <span data-ttu-id="3db69-119">**構成の作成** \> **名前から派生する** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-119">Select **Create configuration** \> **Derive from Name**.</span></span>
5. <span data-ttu-id="3db69-120">名前と説明を入力し、**構成の作成** を選択して、新たな派生バージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="3db69-120">Enter a name and description, and then select **Create configuration** to create a new derived version.</span></span>
6. <span data-ttu-id="3db69-121">新たに派生した構成を選択し、バージョンの説明を追加して、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-121">Select the newly derived configuration, add a description of the version, and then select **OK**.</span></span> <span data-ttu-id="3db69-122">構成先のステータスが **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="3db69-122">The status of the configuration to is changed to **Completed**.</span></span>

![RCS における新たな構成のバージョン](media/RCS_CompleteConfig.JPG)

> [!NOTE]
> <span data-ttu-id="3db69-124">構成のステータスが変更されると、接続されているアプリケーションに関連した検証のエラーメッセージが表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3db69-124">When the configuration status is changed, you might receive a validation error message that is related to the connected applications.</span></span> <span data-ttu-id="3db69-125">検証を無効にするには、**構成** タブのアクション ウィンドウで、**ユーザーパラメーター** を選択し、**設定のステータス変更時に検証をスキップしてリベースする** オプションを **はい** に設定します</span><span class="sxs-lookup"><span data-stu-id="3db69-125">To turn off the validation, on the Action Pane on the **Configurations** tab, select **User parameters**, and then set the **Skip validation at configuration's status change and rebase** option to **Yes**</span></span> 

## <a name="upload-a-configuration-to-the-global-repository"></a><span data-ttu-id="3db69-126">グローバル リポジトリに構成をアップロードする</span><span class="sxs-lookup"><span data-stu-id="3db69-126">Upload a configuration to the Global repository</span></span>

<span data-ttu-id="3db69-127">新たな構成や派生した構成を組織と共有するには、グローバル リポジトリにアップロードします。</span><span class="sxs-lookup"><span data-stu-id="3db69-127">To share a new or derived configuration with your organization, you can upload it to the Global repository.</span></span>

1. <span data-ttu-id="3db69-128">構成の完成バージョンを選択し、**リポジトリにアップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-128">Select the completed version of the configuration, and then select **Upload into repository**.</span></span>
2. <span data-ttu-id="3db69-129">**グローバル (Microsoft)** オプションを選択し、**アップロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-129">Select the **Global (Microsoft)** option, and then select **Upload**.</span></span>

    ![リポジトリ オプションへのアップロード](media/RCS_Upload_to_GlobalRepo_options.JPG)

3. <span data-ttu-id="3db69-131">確認のメッセージ ボックスで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-131">In the confirmation message box, select **Yes**.</span></span> 
4. <span data-ttu-id="3db69-132">必要に応じてバージョンの説明を更新し、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-132">Update the description of the version as required, and then select **OK**.</span></span> 

<span data-ttu-id="3db69-133">構成のステータスが **共有** に更新され、構成がグローバル リポジトリにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="3db69-133">The status of the configuration is updated to **Share**, and the configuration is uploaded to the Global repository.</span></span> <span data-ttu-id="3db69-134">そこからは、次の方法で作業することができます:</span><span class="sxs-lookup"><span data-stu-id="3db69-134">From there, you can work with it in the following ways:</span></span>

- <span data-ttu-id="3db69-135">Dynamics 365 のインスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="3db69-135">Import it into your Dynamics 365 instance.</span></span> <span data-ttu-id="3db69-136">詳細については、[(ER) RCS から構成をインポートする](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3db69-136">For more information, see [(ER) Import configurations from RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md).</span></span>
- <span data-ttu-id="3db69-137">サード パーティや外部の組織と共有する場合は、[RCS 電子レポート (ER) の構成を外部組織と共有する](rcs-global-repo-share-configuration.md)を参照してください</span><span class="sxs-lookup"><span data-stu-id="3db69-137">Share it with a third party or an external organization, see [RCS Share Electronic reporting (ER) configurations with external organizations](rcs-global-repo-share-configuration.md)</span></span>

    ![グローバル リポジトリの イントラスタット Contoso の構成バージョンが派生されました](media/RCS_Config_upload_GlobalRepo.JPG)

## <a name="delete-a-configuration-from-the-global-repository"></a><span data-ttu-id="3db69-139">グローバル リポジトリから構成を削除する</span><span class="sxs-lookup"><span data-stu-id="3db69-139">Delete a configuration from the Global repository</span></span>
<span data-ttu-id="3db69-140">組織で作成した構成を削除するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="3db69-140">Complete the following steps to delete a configuration that your organization has created.</span></span>

1. <span data-ttu-id="3db69-141">**電子申告** ワークスペースで、構成プロバイダーが **アクティブ** であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3db69-141">In the **Electronic reporting** workspace, verify that your configuration provider is **Active**.</span></span> <span data-ttu-id="3db69-142">詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3db69-142">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
2. <span data-ttu-id="3db69-143">アクティブな構成プロバイダーで **リポジトリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-143">On your active configuration provider, select **repository**.</span></span>
3. <span data-ttu-id="3db69-144">リポジトリ タイプ **グローバル** を選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-144">Select the repository type **Global**, and select **Open**.</span></span>
4. <span data-ttu-id="3db69-145">**フィルター** クイック タブで、**フィルター** 機能を使用して削除する構成を見つけます。</span><span class="sxs-lookup"><span data-stu-id="3db69-145">On the **Filter** FastTab, find the configuration that you want to delete by using the **Filter** functionality.</span></span>
5. <span data-ttu-id="3db69-146">**バージョン** クイック タブで、削除する構成のバージョンを選択し、**削除** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-146">On the **Version** FastTab, select the version of the configuration that you want to delete, and then select **Delete**:</span></span>

    ![グローバル リポジトリから構成を削除する](media/RCS_Delete_from_GlobalRepo.JPG)

6. <span data-ttu-id="3db69-148">確認のメッセージ ボックスで、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="3db69-148">In the confirmation message box, select **Yes**.</span></span>

    ![構成バージョン確認メッセージの削除](media/RCS_Delete_from_GlobalRepo_Msg.JPG)
 
<span data-ttu-id="3db69-150">構成バージョンが削除され、確認メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3db69-150">The configuration version is deleted, and confirmation message is shown.</span></span> 

> [!NOTE]
> <span data-ttu-id="3db69-151">構成は、作成した構成プロバイダーによってのみ削除できます。</span><span class="sxs-lookup"><span data-stu-id="3db69-151">Configurations can only be deleted by the Configuration provider that created them.</span></span> <span data-ttu-id="3db69-152">構成が別の組織と共有されている場合、削除する前に構成の共有を解除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3db69-152">If the configuration has been shared with another organization, the configuration will need to be unshared before you delete it.</span></span>
 
