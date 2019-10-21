---
title: Retail 有効化アカウントの管理とデバイスの検証
description: このトピックでは、小売業者がModern POS デバイスまたはクラウド POS デバイスを有効にするために Retail アクティベーション アカウント を IT Pro で設定する方法について説明します。
author: athinesh99
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: HcmWorker, RetailDeviceActivationValidation, RetailPositionPosPermission
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 20471
ms.assetid: 5394e10c-539c-4e26-a097-504c6950cd56
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 6d0a42f5d85473721a666281b3656a560f6a65fc
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024903"
---
# <a name="manage-retail-activation-accounts-and-validate-devices"></a><span data-ttu-id="7e50b-103">Retail 有効化アカウントの管理とデバイスの検証</span><span class="sxs-lookup"><span data-stu-id="7e50b-103">Manage Retail activation accounts and validate devices</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7e50b-104">このトピックでは、小売業者がModern POS デバイスまたはクラウド POS デバイスを有効にするために Retail アクティベーション アカウント を IT Pro で設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-104">This topic explains how an IT Pro can set up Retail activation accounts for retail workers to activate Modern POS or Cloud POS devices.</span></span>

## <a name="setting-up-a-device-activation-account-for-a-single-worker"></a><span data-ttu-id="7e50b-105">1 人の作業者のデバイス有効化アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="7e50b-105">Setting up a device activation account for a single worker</span></span>

<span data-ttu-id="7e50b-106">この手順は、クラウド POS を有効化する前に完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-106">This procedure should be completed before you activate Cloud POS.</span></span>

1. <span data-ttu-id="7e50b-107">Retail では、**作業者**ページから、作業者の**作業者の詳細**ページを開き、AAD 有効化権限を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-107">In Retail, from the **Workers** page, open the **Worker details** page for the worker to assign AAD device activation privileges to.</span></span> <span data-ttu-id="7e50b-108">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-108">Click **Edit**.</span></span>
2. <span data-ttu-id="7e50b-109">**小売**タブで、**POS アクセス許可**リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-109">On the **Retail** tab, click the **POS permissions** link.</span></span> <span data-ttu-id="7e50b-110">作業者がマネージャー アクセス許可グループにあるか、**デバイスの管理**が作業者に対して**はい**に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-110">Make sure that the worker is in the Manager Permission group, or that **Manage Devices** is set to **Yes** for the worker.</span></span>
3. <span data-ttu-id="7e50b-111">**小売**タブの、**外部 ID** で、次のフィールドの値を更新します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-111">On the **Retail** tab, under **External identity**, update the values for the following fields:</span></span>

    - <span data-ttu-id="7e50b-112">エイリアス</span><span class="sxs-lookup"><span data-stu-id="7e50b-112">Alias</span></span>
    - <span data-ttu-id="7e50b-113">UPN</span><span class="sxs-lookup"><span data-stu-id="7e50b-113">UPN</span></span>
    - <span data-ttu-id="7e50b-114">外部識別子</span><span class="sxs-lookup"><span data-stu-id="7e50b-114">External identifier</span></span>

4. <span data-ttu-id="7e50b-115">既存の AAD アカウントを使用するか、または新しい AAD アカウントを作成して、**外部 ID** フィールドを更新することができます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-115">You can update the **External identity** fields by using an existing AAD account or creating a new AAD account.</span></span> <span data-ttu-id="7e50b-116">フィールドを更新するには、**小売**メイン メニュー (**小売**&gt;**既存の ID を関連付ける**または**小売**&gt;**新しい ID を作成する**) から **外部 ID** オプションをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-116">To update the fields, access the **External identity** options from the **Retail** main menu (**Retail** &gt; **Associate existing identity** or **Retail** &gt; **Create new identity**).</span></span>
5. <span data-ttu-id="7e50b-117">既存の AAD アカウントを使用するには、**小売**&gt;**既存の ID を関連付ける** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-117">To use an existing AAD account, select **Retail** &gt; **Associate existing identity**.</span></span> <span data-ttu-id="7e50b-118">スライダーで、正確な名前を持つ AAD アカウントをクリックしてから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-118">In the slider, click the AAD account that has the correct name, and then click **OK**.</span></span> <span data-ttu-id="7e50b-119">その名前とエイリアスに関連付けられている AAD アカウントは、Modern POS のユーザーの有効化アカウントです。</span><span class="sxs-lookup"><span data-stu-id="7e50b-119">The AAD account that is associated with that name and alias is the user's Activation account for Modern POS.</span></span>
6. <span data-ttu-id="7e50b-120">完了し、変更を**作業者**ページに保存し、ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-120">Complete and save the changes on the **Workers** page, and then refresh the page.</span></span> <span data-ttu-id="7e50b-121">外部 ID 情報を含むセクションは、新しい情報で更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-121">The section that contains external identity information should be updated with the new information.</span></span> <span data-ttu-id="7e50b-122">マッピングされた AAD アカウントは、Cloud POS と Modern POS のユーザーの有効化アカウントになりました。</span><span class="sxs-lookup"><span data-stu-id="7e50b-122">The mapped AAD account is now your Activation account for Cloud POS and Modern POS.</span></span> <span data-ttu-id="7e50b-123">このアカウントは、POS アクセス許可が必要な作業者にマップされます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-123">This account is mapped to a worker for the required POS permissions.</span></span> <span data-ttu-id="7e50b-124">Modern POS または POS の有効化に、この AAD アカウントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-124">You can use this AAD account for Modern POS or Cloud POS activation.</span></span>
7. <span data-ttu-id="7e50b-125">外部 ID 作成機能は、入力したエイリアスを使用することにより新しい AAD アカウントを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-125">The Create external identity feature creates a new AAD account for you by using the alias that you enter.</span></span> <span data-ttu-id="7e50b-126">フィールドを更新するには、 **小売**メイン メニュー (**小売** &gt; **新しい ID を作成する**) から **外部 ID**  オプションをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-126">To update the fields, access the **External identity** options from the **Retail** main menu (**Retail** &gt; **Create new identity**).</span></span>
8. <span data-ttu-id="7e50b-127">生成するエイリアスを手動で入力するか、**既定値にリセット** ボタンを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-127">You can either manually enter the alias to generate or use the **Reset to default** button.</span></span> <span data-ttu-id="7e50b-128">その後強力なパスワードを手動で入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-128">Then manually enter a strong password, and click **OK**.</span></span>
9. <span data-ttu-id="7e50b-129">作業者が正常に作成された場合、**作業者**ページにメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-129">If the worker is created successfully, you receive a message on the **Workers** page.</span></span> <span data-ttu-id="7e50b-130">マッピングされた AAD アカウントは、Cloud POS と Modern POS のユーザーの有効化アカウントになりました。</span><span class="sxs-lookup"><span data-stu-id="7e50b-130">The mapped AAD account is now the user's Activation account for Cloud POS and Modern POS.</span></span> <span data-ttu-id="7e50b-131">このアカウントは、POS アクセス許可が必要な作業者にマップされます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-131">This account is mapped to a worker for the required POS permissions.</span></span> <span data-ttu-id="7e50b-132">Modern POS または POS の有効化に、この AAD アカウントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-132">You can use this AAD account for Modern POS or Cloud POS activation.</span></span>

## <a name="setting-up-device-activation-accounts-for-multiple-workers"></a><span data-ttu-id="7e50b-133">複数の作業者のデバイス有効化アカウントの設定</span><span class="sxs-lookup"><span data-stu-id="7e50b-133">Setting up device activation accounts for multiple workers</span></span>

<span data-ttu-id="7e50b-134">複数の作業者のアクティベーション アカウントをバルクで設定することができます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-134">You can set up activation accounts for multiple workers in bulk.</span></span> <span data-ttu-id="7e50b-135">ただし、この機能は ID を関連付けるのでなく、新しい外部 ID を作成する場合にのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-135">However, this functionality is supported only if you're creating new external identities, not if you're associating identities.</span></span>

1. <span data-ttu-id="7e50b-136">作業者フォームで、有効化アカウントを設定する作業者の一覧を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-136">In the workers form, select the list of workers to set the activation account for.</span></span>
2. <span data-ttu-id="7e50b-137">フィールドを更新するには、**小売** &gt; **外部 ID を作成**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-137">Click **Retail** &gt; **Create external identity** to update the fields.</span></span> <span data-ttu-id="7e50b-138">作業者に関連付けられているすべての AAD アカウントはこのウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-138">Any AAD accounts that are associated with the workers appear in this pane.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7e50b-139">これらのアカウントは、外部 ID フロー オプションを使用してマップするまで、デバイスのアクティベーション アカウントではありません。</span><span class="sxs-lookup"><span data-stu-id="7e50b-139">These accounts aren't device activation accounts until you map them by using the external identity flow options.</span></span>

3. <span data-ttu-id="7e50b-140">既存の AAD アカウントを有効化アカウントとして使用する場合は、バルクでマップできません。</span><span class="sxs-lookup"><span data-stu-id="7e50b-140">If you want to use the existing AAD accounts as activation accounts, you can't map them in bulk.</span></span> <span data-ttu-id="7e50b-141">これらの作業者の選択をキャンセルし、**既存の外部 ID の使用**を使用して個別にマップします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-141">Cancel the selection of those workers, and then map them individually by using **Use existing external identity**.</span></span>
4. <span data-ttu-id="7e50b-142">新しい AAD アカウントを作成し、作業者に関連付けてアクティベーション アカウントとして使用できるようにするには、**エイリアス** と **パスワード** フィールドを更新し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-142">To create new AAD accounts and associate them with the workers, so that they can be used as activation accounts, update the **Alias** and **Password** fields, and then click **OK**.</span></span> <span data-ttu-id="7e50b-143">メイン作業者フォームでは、アクティベーション アカウントが作業者ごとに作成されるとメッセージを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-143">In the main worker form, you receive a message as activation accounts are created for each worker.</span></span>

## <a name="run-the-validate-devices-for-activation-check-at-headquarters"></a><span data-ttu-id="7e50b-144">本社で有効化チェックのためにデバイス検証を実行</span><span class="sxs-lookup"><span data-stu-id="7e50b-144">Run the Validate Devices for Activation check at headquarters</span></span>

<span data-ttu-id="7e50b-145">有効化アカウントを作業者に手渡す前に、IT プロフェッショナルは作業者に割り当てられたデバイスのためにデバイスを検証チェックを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-145">Before handing an activation account to a worker, an IT Pro must run the Validate devices check for the devices assigned to the worker.</span></span> <span data-ttu-id="7e50b-146">これは、事前にデバイス動作の潜在的な障害を特定し、それを作業者に通知する前に修正するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-146">This will help identify any potential failures of device activation in advance and fix it before it is given to the worker.</span></span>

1. <span data-ttu-id="7e50b-147">**デバイス** ページを HQ (**小売りとコマース** &gt; **チャンネル設定** &gt; **POS 設定** &gt; **デバイス**)で開きます。</span><span class="sxs-lookup"><span data-stu-id="7e50b-147">Open the **Device** page in HQ (**Retail and commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **Devices**).</span></span>
2. <span data-ttu-id="7e50b-148">デバイスの有効化を検証するデバイスを選択し、**デバイスで有効化を検証する** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-148">Select the device to validate for device activation, and then click **Validate devices for activation**.</span></span> <span data-ttu-id="7e50b-149">たとえば、デバイスの **HOUSTON-2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-149">For example, select device **HOUSTON-2**.</span></span>
3. <span data-ttu-id="7e50b-150">表示されるダイアログ ボックスで、デバイスを検証する作業者 (前の手順で AAD アカウントにマップされた作業者) を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-150">In the dialog box that appears, select the worker to validate the device for (that is, the worker that you mapped to the AAD account in the previous procedure).</span></span> <span data-ttu-id="7e50b-151">たとえば、作業者の **000160** を選択します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-151">For example, select worker **000160**.</span></span>
4. <span data-ttu-id="7e50b-152">**OK** をクリックし、次のようなメッセージが表示されることを確認します。「デバイス HOUSTON-2 とスタッフ 000160 の有効化前の検証が完了しました。</span><span class="sxs-lookup"><span data-stu-id="7e50b-152">Click **OK**, and make sure that you receive a message similar to the following: "Pre-Activation validation completed for Device HOUSTON-2 and Staff 000160.</span></span> <span data-ttu-id="7e50b-153">検証: 成功</span><span class="sxs-lookup"><span data-stu-id="7e50b-153">Validation: Passed"</span></span>

## <a name="checklist-to-follow-before-activation"></a><span data-ttu-id="7e50b-154">起動前のチェックリスト</span><span class="sxs-lookup"><span data-stu-id="7e50b-154">Checklist to follow before activation</span></span>

1. <span data-ttu-id="7e50b-155">HQ で**有効化のためにデバイスを検証**チェックを完了し、デバイスが検証をパスしたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-155">Complete the **Validate devices for activation** check in HQ, and make sure that the device passes validation.</span></span>
2. <span data-ttu-id="7e50b-156">デバイスを有効化しているクライアント マシンで、Retail サーバー URL 正常性チェックにアクセスし、正常性チェックが承認されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-156">On the client machine where you're activating the device, access the Retail Server URL health check, and make sure that the health check is passed.</span></span> <span data-ttu-id="7e50b-157">次の形式を使用します: `https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping`</span><span class="sxs-lookup"><span data-stu-id="7e50b-157">Use the following format: `https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping`</span></span>
3. <span data-ttu-id="7e50b-158">作業者は、AAD アカウント (**外部 ID** 下) にマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-158">The worker must be mapped to an AAD account (under **External identity**).</span></span>
4. <span data-ttu-id="7e50b-159">マッピングする AAD アカウントは、同じテナントに属している必要があります。</span><span class="sxs-lookup"><span data-stu-id="7e50b-159">The AAD account to map must belong to the same tenant.</span></span>
5. <span data-ttu-id="7e50b-160">作業者を AAD アカウントにマップするには、Microsoft Dynamics Lifecycle Services (LCS) の管理者アカウントを使用して HQ に サインインします。</span><span class="sxs-lookup"><span data-stu-id="7e50b-160">To map the worker to the AAD account, sign in to HQ by using the Admin account for Microsoft Dynamics Lifecycle Services (LCS).</span></span>
6. <span data-ttu-id="7e50b-161">作業者がマネージャー ロール内の Retail ユーザーとして設定されていることを確認します (検証でチェックされます)。</span><span class="sxs-lookup"><span data-stu-id="7e50b-161">Make sure that the worker is set up as a Retail user in the Manager role (checked by validation).</span></span>
7. <span data-ttu-id="7e50b-162">チャネル データがチャネル データベースに存在することを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-162">Make sure that the channel data is present in the channel database.</span></span>
8. <span data-ttu-id="7e50b-163">**登録** &gt; **登録** (検証によって確認) でハードウェア プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-163">Set up the hardware profile under **Registers** &gt; **Register** (checked by validation).</span></span>
9. <span data-ttu-id="7e50b-164">レジスターおよび店舗に画面レイアウトがあることを確認します (検証でチェックされます)。</span><span class="sxs-lookup"><span data-stu-id="7e50b-164">Make sure that the register and store have a screen layout (checked by validation).</span></span>
10. <span data-ttu-id="7e50b-165">基本住所が法人に対して設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-165">Make sure that a primary address is set up for the legal entity.</span></span>
11. <span data-ttu-id="7e50b-166">電子決済 (EFT) のコンフィギュレーションの値があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="7e50b-166">Make sure that the electronic funds transfer (EFT) configuration value is present.</span></span>
