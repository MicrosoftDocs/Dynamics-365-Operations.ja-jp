---
title: Regulatory Configuration Service (RCS) - グローバリゼーション機能
description: このトピックでは、Microsoft Regulatory Configuration Service (RCS) とグローバル レポジトリを使用して、グローバリゼーション機能を作成および使用する方法ついて説明します。
author: JaneA07
manager: AnnBe
ms.date: 06/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCS, RCSWorkspace, e-Invoicing service
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: ae46dab5250fbe8096f43e420cb7ef33a5862af0
ms.sourcegitcommit: 97206552616b248f88e516fea08b3f059257e8d1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3432050"
---
# <a name="regulatory-configuration-services-rcs---globalization-features"></a><span data-ttu-id="4ae30-103">Regulatory Configuration Service (RCS) - グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="4ae30-103">Regulatory Configuration Services (RCS) - Globalization features</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ae30-104">Microsoft Regulatory Configuration Services (RCS) を使用すると、電子請求サービスなどのグローバリゼーション サービスで使用できるグローバリゼーション機能を作成できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-104">You can use Microsoft Regulatory Configuration Services (RCS) to create a Globalization feature that can be used in Globalization services, such as an e-invoicing service.</span></span> <span data-ttu-id="4ae30-105">RCS を使用すると、次のタスクを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-105">RCS lets you perform these tasks:</span></span>

- <span data-ttu-id="4ae30-106">機能の関連コンポーネントを定義します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-106">Define related components of a feature.</span></span>
- <span data-ttu-id="4ae30-107">機能のステータスを通じて機能のライフサイクルを管理します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-107">Manage the feature lifecycle through a feature's status.</span></span>
- <span data-ttu-id="4ae30-108">定義された環境で機能を使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4ae30-108">Make a feature available for defined environments.</span></span>
- <span data-ttu-id="4ae30-109">機能をその他の組織と共有します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-109">Share a feature with other organizations.</span></span>

<span data-ttu-id="4ae30-110">次の手順では、RCS のユーザーがグローバリゼーション機能および関連コンポーネントを追加する方法、その機能のステータスを更新する方法、およびグローバリゼーション サービスで使用できるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-110">The following procedures explain how a user in RCS can add a Globalization feature and related components, update the feature's status, and make the feature available so that it can be used in Globalization services.</span></span>

<span data-ttu-id="4ae30-111">手順を実行する前に、次の作業に関連する手順を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-111">Before you complete the procedures, you must complete the steps that are related to the following tasks:</span></span>

- <span data-ttu-id="4ae30-112">RCS インスタンスへのアクセス。</span><span class="sxs-lookup"><span data-stu-id="4ae30-112">Accessing an RCS instance.</span></span>
- <span data-ttu-id="4ae30-113">構成プロバイダーを作成して有効化します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-113">Creating and activating a configuration provider.</span></span> <span data-ttu-id="4ae30-114">詳細については、[構成プロバイダーを作成して、有効としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ae30-114">For more information, see [Create configuration providers and mark them as active](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

<span data-ttu-id="4ae30-115">Finance and Operations アプリ インスタンスで、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-115">In your Finance and Operations apps instance, follow these steps.</span></span>

1. <span data-ttu-id="4ae30-116">**組織管理** \> **ワークスペース** \> **電子申告**の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-116">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="4ae30-117">RCS 環境が貴社にプロビジョニングされていない場合は、**Regulatory services – 構成** を選択し、続いてプロビジョニングの指示に従います。</span><span class="sxs-lookup"><span data-stu-id="4ae30-117">If no RCS environment is provisioned for your company, select **Regulatory services – Configuration**, and follow the instructions to provision one.</span></span>

> [!NOTE]
> <span data-ttu-id="4ae30-118">RCS 環境が既にプロビジョニングされている場合は、サインインのオプションを選択して、ページの URL を使用してこの環境にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4ae30-118">If an RCS environment has already been provisioned for your company, use the page URL to access the environment by selecting the sign-in option.</span></span>

## <a name="turn-on-the-globalization-features"></a><span data-ttu-id="4ae30-119">グローバリゼーション機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="4ae30-119">Turn on the Globalization features</span></span>

1. <span data-ttu-id="4ae30-120">RCS インスタンスで、**機能管理** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-120">In your RCS instance, select the **Feature management** tile.</span></span>
2. <span data-ttu-id="4ae30-121">**機能の管理** ワークスペースで、一覧から **グローバリゼーション** 機能を選択し、**今すぐ有効にする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-121">In the **Feature management** workspace, select **Globalization features** in the list, and then select **Enable now**.</span></span>

    ![機能管理のグローバリゼーション機能](./media/RCS_GlobalF_1%20Feature%20mgmt.JPG)

## <a name="globalization-features"></a><span data-ttu-id="4ae30-123">グローバリゼーション機能</span><span class="sxs-lookup"><span data-stu-id="4ae30-123">Globalization features</span></span>

<span data-ttu-id="4ae30-124">グローバリゼーション機能を使用するには、まずグローバル リポジトリからファイルをインポートし、それを独自のバージョンで作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-124">To use a Globalization feature, you must first import it from the the Global repository and create your own version of it.</span></span> <span data-ttu-id="4ae30-125">グローバリゼーション機能を追加するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-125">There are two ways to add Globalization features:</span></span>

- <span data-ttu-id="4ae30-126">発行または共有されている既存の機能に基づく派生フィーチャーを追加します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-126">Add a derived feature that is based on an existing feature that has been published or shared.</span></span>
- <span data-ttu-id="4ae30-127">作成した新しい機能を最初から追加します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-127">Add a new feature that you've created from scratch.</span></span>

## <a name="access-globalization-features"></a><span data-ttu-id="4ae30-128">グローバリゼーション機能にアクセスする</span><span class="sxs-lookup"><span data-stu-id="4ae30-128">Access Globalization features</span></span>

1. <span data-ttu-id="4ae30-129">このトピックで既に説明したように、機能の管理については、**グローバリゼーション機能** 機能が有効になっていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="4ae30-129">Make sure that the **Globalization features** feature is turned on in Feature management, as described earlier in this topic.</span></span>
2. <span data-ttu-id="4ae30-130">新しい **グローバリゼーション機能** ワークスペースを開き、**機能** で、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-130">Open the new **Globalization Features** workspace, and then, under **Features**, select the **e-Invoicing** tile.</span></span>

    ![グローバル機能ワークスペース](./media/RCS_GlobalF_2%20Feature%20wrkspace.JPG)

    <span data-ttu-id="4ae30-132">**電子請求機能** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-132">The **e-Invoicing Features** page is opened.</span></span>

    ![電子請求機能ページ](./media/RCS_GlobalF_3%20Feature%20form.JPG)

## <a name="add-a-derived-globalization-feature"></a><span data-ttu-id="4ae30-134">派生グローバリゼーション機能の追加</span><span class="sxs-lookup"><span data-stu-id="4ae30-134">Add a derived Globalization feature</span></span>

<span data-ttu-id="4ae30-135">発行または共有されている既存の機能から新しいグローバリゼーション機能を派生することによって追加できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-135">You can add a new Globalization feature by deriving it from an existing feature that has been published or shared.</span></span>

1. <span data-ttu-id="4ae30-136">**インポート** を選択すると、**グローバル リポジトリからのインポート機能** ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-136">Select **Import** to open the **Import feature from Global repository** page.</span></span>

    ![グローバルリポジトリ ページから機能をインポートする](./media/RCS_GlobalF_4%20Feature%20import%20form%20GR.JPG)

2. <span data-ttu-id="4ae30-138">**同期** を選択して、最新の機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-138">Select **Synchronize** to get the latest features.</span></span>

    <span data-ttu-id="4ae30-139">同期されたリストには、Microsoft によって発行されたもの、または他の構成プロバイダーによって共有されたものによって、使用できる機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4ae30-139">The synced list includes features that are available to you either because they were published by Microsoft or because they were shared with you by another configuration provider.</span></span>

    ![機能の同期リスト](./media/RCS_GlobalF_5%20Feature%20GR%20sync.JPG)

3. <span data-ttu-id="4ae30-141">一覧でインポートする機能を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-141">In the list, select the features to import, and then select **Import**.</span></span> <span data-ttu-id="4ae30-142">選択した機能が正常にインポートされた場合は、メッセージを受信します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-142">You receive a message when the selected features have been successfully imported.</span></span>

    ![ファイルのインポートに成功したことを示すメッセージ](./media/RCS_GlobalF_6%20Feature%20GR%20import%20success.JPG)

4. <span data-ttu-id="4ae30-144">**追加** をクリックし、ドロップダウン ダイアログボックスで、**既存のバージョンに基づく** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-144">Select **Add**, and then, in the drop-down dialog box, select the **Based on existing version** option.</span></span>
5. <span data-ttu-id="4ae30-145">機能の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-145">Enter a name and description for the feature.</span></span>
6. <span data-ttu-id="4ae30-146">使用可能な機能の一覧で、機能の基本バージョンを選択し、**機能の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-146">In the list of available features, select the base version of the feature, and then select **Create feature**.</span></span>

    ![派生機能の追加](./media/RCS_GlobalF_7%20Feature%20create%20derived.JPG)

    <span data-ttu-id="4ae30-148">追加した機能が作成され、ステータスが **ドラフト** になります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-148">The feature that you added is created and has a status of **Draft**.</span></span>

    ![ドラフト ステータスのある派生機能](./media/RCS_GlobalF_8%20Feature%20draft%20create.JPG)

7. <span data-ttu-id="4ae30-150">機能コンポーネントを確認して、更新が必要かどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-150">Review the feature components to determine whether updates are required:</span></span>

    - <span data-ttu-id="4ae30-151">電子レポート (ER) 形式と、その機能バージョンの形式マッピングを使用してバインドをカスタマイズする必要がある場合に備えて、構成を確認します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-151">Review the configurations, in case you need to customize the Electronic reporting (ER) formats and their binding with format mappings for the feature version.</span></span>
    - <span data-ttu-id="4ae30-152">機能バージョンの **アクション** タブ、**適用ルール** タブ、または **変数** タブをカスタマイズする必要がある場合に備えて、設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-152">Review the setup, in case you need to customize the **Actions** tab, **Applicability rules** tab, or **Variables** tab for the feature version.</span></span>

8. <span data-ttu-id="4ae30-153">**バージョン** タブで、**有効期限の開始** の日付を選択肢、**説明** フィールドが空白の場合は説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-153">On the **Versions** tab, select an **Effective from** date, and enter a description if the **Description** field is blank.</span></span>
9. <span data-ttu-id="4ae30-154">機能を完了するには、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-154">Select **Change status** to complete the feature.</span></span> <span data-ttu-id="4ae30-155">完成した機能は、特定の環境に対して使用できるようにするため、グローバリゼーション サービスで使用できる、または、グローバル リポジトリに発行することができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-155">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="4ae30-156">**公開済み** の **機能バージョンステータス** の値を持つ機能は、外部組織と共有できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-156">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="add-a-new-globalization-feature"></a><span data-ttu-id="4ae30-157">新規グローバリゼーション機能の追加</span><span class="sxs-lookup"><span data-stu-id="4ae30-157">Add a new Globalization feature</span></span>

<span data-ttu-id="4ae30-158">新規グローバリゼーション機能を追加するには、最初から作成します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-158">You can add a new Globalization feature by creating it from scratch.</span></span>

1. <span data-ttu-id="4ae30-159">**グローバル リポジトリからのインポート機能** ページで、**追加** を選択し、ドロップダウン ダイアログボックスで、**新機能** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-159">On the **Import feature from Global repository** page, select **Add**, and then, in the drop-down dialog box, select the **New feature** option.</span></span>
2. <span data-ttu-id="4ae30-160">機能の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-160">Enter a name and description for the feature.</span></span>
3. <span data-ttu-id="4ae30-161">**機能の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-161">Select **Create feature**.</span></span>

    ![新機能の追加](./media/RCS_GlobalF_9%20Feature%20create%20new.JPG)

4. <span data-ttu-id="4ae30-163">**バージョン** タブで、**有効期間** を選択し、**ステータスの変更** を選択して機能を完了します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-163">On the **Versions** tab, select an **Effective from** date, and then select **Change status** to complete the feature.</span></span> <span data-ttu-id="4ae30-164">完成した機能は、特定の環境に対して使用できるようにするため、グローバリゼーション サービスで使用できる、または、グローバル リポジトリに発行することができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-164">Completed features can be made available for a specific environment so that they can be used in Globalization services, or they can be published to the Global repository.</span></span>

> [!NOTE]
> <span data-ttu-id="4ae30-165">**公開済み** の **機能バージョンステータス** の値を持つ機能は、外部組織と共有できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-165">Features that have a **Feature version status** value of **Published** can be shared with external organizations.</span></span>

## <a name="feature-component-overview"></a><span data-ttu-id="4ae30-166">機能コンポーネントの概要</span><span class="sxs-lookup"><span data-stu-id="4ae30-166">Feature component overview</span></span>

<span data-ttu-id="4ae30-167">グローバリゼーション機能には、いくつかのコンポーネントがあります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-167">Globalization features have several components:</span></span>

- <span data-ttu-id="4ae30-168">**バージョン** - このコンポーネントは、機能ライフサイクル管理をサポートし、ユーザーが機能のさまざまなバージョンのステータスを管理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4ae30-168">**Version** – This component supports feature lifecycle management and lets users manage the status for different versions of the feature.</span></span>
- <span data-ttu-id="4ae30-169">**構成** - このコンポーネントを使用すると、ユーザーは関連する ER 形式と形式マッピングを管理、表示、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-169">**Configurations** – This component lets users manage, view, and edit related ER formats and format mappings.</span></span>
- <span data-ttu-id="4ae30-170">**セットアップ** - このコンポーネントを使用すると、電子請求サービスなどのグローバリゼーション サービスのユーザーは、関連する機能バージョンの設定を管理できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-170">**Setups** – This component lets users of Globalization services, such as an e-invoicing service, manage the setup of the related feature version.</span></span> <span data-ttu-id="4ae30-171">したがって、通信ルールと応答ルールの柔軟な構築がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-171">Therefore, it supports the flexible construction of communication and responses rules.</span></span>
- <span data-ttu-id="4ae30-172">**環境** - このコンポーネントを使用すると、電子請求サービスなどのグローバリゼーション サービスのユーザーは、機能バージョンの設定が使用されている環境を管理し、それにアクセスできるユーザーに認証を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-172">**Environment** – This component lets users of Globalization services, such as an e-invoicing service, manage the environment where the feature version setup is used and grant authorization to the users who will have access to it.</span></span>
- <span data-ttu-id="4ae30-173">**組織** - このコンポーネントを使用すると、ユーザーは外部組織と機能を共有できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-173">**Organizations** – This component lets users to share the feature with external organizations.</span></span>

## <a name="configuring-feature-components"></a><span data-ttu-id="4ae30-174">機能コンポーネントの構成</span><span class="sxs-lookup"><span data-stu-id="4ae30-174">Configuring feature components</span></span>

### <a name="version-and-status"></a><span data-ttu-id="4ae30-175">バージョンとステータス</span><span class="sxs-lookup"><span data-stu-id="4ae30-175">Version and status</span></span>

<span data-ttu-id="4ae30-176">このバージョンは、グローバリゼーション機能のライフサイクルを管理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-176">The version is used to manage the Globalization feature lifecycle.</span></span>

<span data-ttu-id="4ae30-177">ステータスは、**バージョン** タブの **ステータス** フィールドで変更できます。次のステータスを使用できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-177">The status can be changed in the **Status** field on the **Version** tab. The following statuses are available:</span></span>

- <span data-ttu-id="4ae30-178">**下書き** - この機能は、このステータスになっている場合にのみ編集できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-178">**Draft** – The feature can be edited only when it's in this status.</span></span>
- <span data-ttu-id="4ae30-179">**完了** - 機能とそれに関連するすべてのコンポーネントがファイナライズ (完了) されており、編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="4ae30-179">**Complete** – The feature and all related components have been finalized (completed) and can't be edited.</span></span>
- <span data-ttu-id="4ae30-180">**発行済** - 機能とすべての関連コンポーネントがグローバル リポジトリに公開されています。</span><span class="sxs-lookup"><span data-stu-id="4ae30-180">**Published** – The feature and all related components have been published to the Global repository.</span></span>
- <span data-ttu-id="4ae30-181">**共有** - 機能とすべての関連コンポーネントが外部組織と共有されています。</span><span class="sxs-lookup"><span data-stu-id="4ae30-181">**Shared** – The feature and all related components have been shared with external organizations.</span></span>
- <span data-ttu-id="4ae30-182">**有効** - 電子請求サービスなどのグローバリゼーション サービスで使用できる機能とすべての関連コンポーネントが有効になります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-182">**Enabled** – The feature and all related components have been enabled for use in a Globalization service, such as an e-invoicing service.</span></span>

> [!NOTE]
> <span data-ttu-id="4ae30-183">機能は、これらのステータスの一部に順番に移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-183">Features must move sequentially through some of these statuses.</span></span> <span data-ttu-id="4ae30-184">したがって、すべてのステータスをライフサイクルのすべての段階で利用できるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="4ae30-184">Therefore, not every status might be available at every lifecycle stage.</span></span>

### <a name="configurations"></a><span data-ttu-id="4ae30-185">コンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4ae30-185">Configurations</span></span>

<span data-ttu-id="4ae30-186">以下のアクションは、構成に利用できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-186">The following actions are available for configurations:</span></span>

- <span data-ttu-id="4ae30-187">**表示** - 更新を必要としない基本機能構成を表示します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-187">**View** – View the underlying feature configurations that don't require any update.</span></span>
- <span data-ttu-id="4ae30-188">**編集** - 選択した構成の下書きバージョンを作成することで、書式デザイナーで形式または形式のマッピングを編集できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-188">**Edit** – Create a draft version of a selected configuration so that you can edit the format or format mapping in the Format designer.</span></span>
- <span data-ttu-id="4ae30-189">**削除** - 選択した構成を機能から削除します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-189">**Delete** – Delete a selected configuration from the feature.</span></span>
- <span data-ttu-id="4ae30-190">**リベース** - 機能をリベースします。</span><span class="sxs-lookup"><span data-stu-id="4ae30-190">**Rebase** – Rebase the feature.</span></span> <span data-ttu-id="4ae30-191">詳細については、このトピックの後半の [派生したグローバリゼーション機能をリベースする](#rebase) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ae30-191">For more information, see the [Rebase derived Globalization features](#rebase) section later in this topic.</span></span>

### <a name="setups"></a><span data-ttu-id="4ae30-192">設定</span><span class="sxs-lookup"><span data-stu-id="4ae30-192">Setups</span></span>

<span data-ttu-id="4ae30-193">以下のアクションは、次の機能設定に利用できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-193">The following actions are available for feature setups:</span></span>

- <span data-ttu-id="4ae30-194">**追加** – 新機能の設定を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-194">**Add** – Create a new feature setup.</span></span> <span data-ttu-id="4ae30-195">この機能の設定は、既存の機能設定から派生するか、または最初から作成することができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-195">This feature setup can be derived from an existing feature setup or created from scratch.</span></span>
- <span data-ttu-id="4ae30-196">**削除** - 選択した機能の設定を削除します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-196">**Delete** – Delete a selected feature setup.</span></span>
- <span data-ttu-id="4ae30-197">**表示** – 変更を必要としない基本機能の設定を表示します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-197">**View** – View an underlying feature setup that doesn't require any changes.</span></span>
- <span data-ttu-id="4ae30-198">**編集** - フィーチャー設定の 3 つの主要なコンポーネントの属性を作成、削除、または変更します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-198">**Edit** – Create, delete, or modify the attributes of the three main components of a feature setup:</span></span>

    - <span data-ttu-id="4ae30-199">アクションとそのパラメータ</span><span class="sxs-lookup"><span data-stu-id="4ae30-199">Actions and their parameters</span></span>
    - <span data-ttu-id="4ae30-200">適合性ルール</span><span class="sxs-lookup"><span data-stu-id="4ae30-200">Applicability rules</span></span>
    - <span data-ttu-id="4ae30-201">変数</span><span class="sxs-lookup"><span data-stu-id="4ae30-201">Variables</span></span>

![機能バージョン設定ページ](./media/RCS_GlobalF_10%20Feature%20set%20up.JPG)

### <a name="environments"></a><span data-ttu-id="4ae30-203">環境</span><span class="sxs-lookup"><span data-stu-id="4ae30-203">Environments</span></span>

<span data-ttu-id="4ae30-204">以下のアクションは、環境に利用できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-204">The following actions are available for environments:</span></span>

- <span data-ttu-id="4ae30-205">**有効化** - 選択した機能バージョンについて、発行済の環境を選択し、使用可能な場合に **有効開始** 日を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-205">**Enable** – For a selected feature version, select a published environment, and select an **Effective from** date when it should be available.</span></span> <span data-ttu-id="4ae30-206">詳細については、このトピックの後半の [有効化のための環境を構成する](#configureenvironment) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4ae30-206">For more information, see the [Configure environments for enablement](#configureenvironment) section later in this topic.</span></span>
- <span data-ttu-id="4ae30-207">**キャンセル** - 機能の設定に対して環境を削除します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-207">**Cancel** – Remove an environment for a feature setup.</span></span>

### <a name="organizations"></a><span data-ttu-id="4ae30-208">組織</span><span class="sxs-lookup"><span data-stu-id="4ae30-208">Organizations</span></span>

<span data-ttu-id="4ae30-209">外部組織とのグローバリゼーション機能を共有するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4ae30-209">Follow these steps to share a Globalization feature with an external organization.</span></span>

1. <span data-ttu-id="4ae30-210">**電子請求機能** ページで、共有する機能と機能バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-210">On the **e-Invoicing features** page, select the feature and the feature version to share.</span></span>
2. <span data-ttu-id="4ae30-211">**組織** タブで、**共有** を選択し、ドロップダウン ダイアログボックスで組織のドメイン名を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-211">On the **Organizations** tab, select **Share with**, and then, in the drop-down dialog box, enter the organization's domain name.</span></span>
3. <span data-ttu-id="4ae30-212">**共有** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-212">Select **Share**.</span></span>

    ![機能をその他の組織と共有する](./media/RCS_GlobalF_20%20Feature%20orgn_share%20with.JPG)

<span data-ttu-id="4ae30-214">機能が選択した組織と共有され、その組織ではグローバル リポジトリで利用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4ae30-214">The feature is shared with the selected organization and is available for that organization in the Global repository.</span></span> <span data-ttu-id="4ae30-215">この機能は、組織の RCS のインスタンス、または Dynamics 365 Finance にインポートしたり、使用できるようにしたりすることができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-215">From there, the feature can be imported into the organization's instance of RCS or Dynamics 365 Finance so that it can be used.</span></span>

## <a name="rebase-derived-globalization-features"></a><a name="rebase"></a><span data-ttu-id="4ae30-216">派生グローバリゼーション機能のリベース</span><span class="sxs-lookup"><span data-stu-id="4ae30-216">Rebase derived Globalization features</span></span>

<span data-ttu-id="4ae30-217">新しい基本機能バージョンまたは更新された基本機能バージョンに、派生したグローバリゼーション機能をリベースできます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-217">You can rebase a derived Globalization feature to the new or updated base feature version.</span></span> <span data-ttu-id="4ae30-218">これにより、基本バージョンで発生した変更が自動的に更新されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-218">In this way, changes that have occurred in the base version can be automatically updated.</span></span> <span data-ttu-id="4ae30-219">更新された基本機能バージョンは、元の構成プロバイダーによって作成された後、発行または共有されます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-219">The updated base feature version is created by the originating configuration provider, and it's then published or shared.</span></span>

![更新された基本機能バージョン](./media/RCS_GlobalF_12%20Feature%20new%20version.JPG)

<span data-ttu-id="4ae30-221">たとえば、作成した機能の派生バージョンをリベースする場合は、最初にグローバル リポジトリからその機能をインポートして最新バージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-221">For example, if you want to rebase the derived version of a feature that you created, you first get the latest version of the feature by importing it from the Global repository.</span></span>

1. <span data-ttu-id="4ae30-222">**電子請求機能** ページで、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-222">On the **e-Invoicing features** page, select **Import**.</span></span>
2. <span data-ttu-id="4ae30-223">**同期** を選択して、最新の機能を取得します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-223">Select **Synchronize** to get the latest features.</span></span>
3. <span data-ttu-id="4ae30-224">機能の一覧で、インポートする機能を選択し、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-224">In the list of features, select the features to import, and then select **Import**.</span></span>

    ![機能の最新バージョンのインポート](./media/RCS_GlobalF_13%20Feature%20new%20version%20import.JPG)

4. <span data-ttu-id="4ae30-226">機能の一覧で、リベースする機能を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-226">In the list of features, select the feature to rebase.</span></span>
5. <span data-ttu-id="4ae30-227">**バージョン** タブで、**新規** を選択して、下書きバージョンを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-227">On the **Version** tab, select **New** to create a draft version.</span></span>

    ![新規下書きバージョンが作成されました](./media/RCS_GlobalF_14%20Feature%20new%20base%20version.JPG)

6. <span data-ttu-id="4ae30-229">**リベース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-229">Select **Rebase**.</span></span>
7. <span data-ttu-id="4ae30-230">**リベース** ダイアログボックスで、リベース先となる機能の最新バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-230">In the **Rebase** dialog box, select the latest version of the feature to rebase to.</span></span>

    ![ダイアログ ボックスのリベース](./media/RCS_GlobalF_15%20Feature%20rebase%20version.JPG)

8. <span data-ttu-id="4ae30-232">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-232">Select **OK**.</span></span>
9. <span data-ttu-id="4ae30-233">機能コンポーネントを確認し、必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="4ae30-233">Review the feature components, and make any changes that are required.</span></span>
10. <span data-ttu-id="4ae30-234">リベースされた機能を完了するには、**ステータスの変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-234">Select **Change status** to complete the rebased feature.</span></span> <span data-ttu-id="4ae30-235">リベースが完了したら、追加のアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-235">When the rebase is completed, you can perform additional actions.</span></span> <span data-ttu-id="4ae30-236">たとえば、機能を公開して、グローバリゼーション サービスで使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-236">For example, you can publish the feature and make it available for use in Globalization services.</span></span>

    ![機能のステータスが完了に更新されました](./media/RCS_GlobalF_16%20Feature%20rebase%20version%20complete.JPG)

## <a name="configure-environments-for-globalization-features"></a><a name="configureenvironment"></a><span data-ttu-id="4ae30-238">グローバリゼーション機能のための環境の構成</span><span class="sxs-lookup"><span data-stu-id="4ae30-238">Configure environments for Globalization features</span></span>

<span data-ttu-id="4ae30-239">グローバリゼーション サービスのユーザーは、環境を管理して、グローバリゼーション機能を設定し、それにアクセスできる他のユーザーに承認を付与することができます。</span><span class="sxs-lookup"><span data-stu-id="4ae30-239">Users of Globalization services can manage the environment to set up a Globalization feature and grant authorization to other users who will have access to it.</span></span>

1. <span data-ttu-id="4ae30-240">**グローバリゼーション機能** ワークスペースで、**環境** から、**電子請求** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-240">In the **Globalization Features** workspace, under **Environments**, select the **e-Invoicing** tile.</span></span>

    ![グローバリゼーション機能ワークスペース](./media/RCS_GlobalF_17%20Feature%20environment.JPG)

2. <span data-ttu-id="4ae30-242">**Key Vault パラメータ** を選択し、**新規** を選択して、Azure Key Vault シークレットを作成します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-242">Select **Key Vault parameters**, and then select **New** to create an Azure Key Vault secret.</span></span>
3. <span data-ttu-id="4ae30-243">Key Vaultの名前と説明を入力し、**Key Vault の URI** フィールドに Azure での Key Vault リソースを識別する URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-243">Enter a name and description for the key vault, and then, in the **Key Vault URI** field, enter the URL that identifies the Key Vault resource in Azure.</span></span>
4. <span data-ttu-id="4ae30-244">**証明書** クイックタブで、**追加** をクリックして証明書を追加し、各証明書の名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-244">On the **Certificates** FastTab, select **Add** to add the certificate, and enter a name and description for each certificate.</span></span>

    ![追加された証明書](./media/RCS_GlobalF_18%20Feature%20envn%20key%20vault%20parameter.JPG)

5. <span data-ttu-id="4ae30-246">**新規** を選択して、新しい環境を作成します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-246">Select **New** to create a new environment.</span></span>
6. <span data-ttu-id="4ae30-247">ストレージに必要な名前、説明、および共有アクセス署名トークンのシークレットを入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-247">Enter a name, a description, and the shared access signature token secret required for the storage.</span></span>
7. <span data-ttu-id="4ae30-248">**ユーザー** クイックタブで、**新規** を選択し、この環境にアクセスするためのアクセス許可を持つユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-248">On the **Users** FastTab, select **New** to add a user who will have permission to access this environment.</span></span>
8. <span data-ttu-id="4ae30-249">ユーザーのユーザー ID とメールアドレスを入力します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-249">Enter the user's user ID and email address.</span></span>
9. <span data-ttu-id="4ae30-250">さらにユーザーを追加するには、手順 7. と 8. を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-250">Repeat steps 7 and 8 to add more users.</span></span>
10. <span data-ttu-id="4ae30-251">**公開** を選択して、環境を公開します。</span><span class="sxs-lookup"><span data-stu-id="4ae30-251">Select **Publish** to publish the environment.</span></span>

    ![公開された環境](./media/RCS_GlobalF_19%20Feature%20envn%20publishing.JPG)
