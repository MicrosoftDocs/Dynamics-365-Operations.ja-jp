---
title: デバイスのジョブ カードのコンフィギュレーション
description: このトピックでは、ジョブ カード デバイスの構成に使用するさまざまなオプションについて説明します。
author: johanhoffmann
manager: tfehr
ms.date: 05/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: fc698ac7e0cfc8d6b196abf35658688ad1bc8bc7
ms.sourcegitcommit: 6319a07ee6c36ebb28acaf205bc79d2fd8f7dd5d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/30/2020
ms.locfileid: "3413173"
---
# <a name="configure-job-card-for-devices"></a><span data-ttu-id="6c818-103">デバイスのジョブ カードのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="6c818-103">Configure job card for devices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c818-104">ジョブ カード デバイスは、ジョブが開始されたとき、ジョブについてのフィードバックを報告するとき、間接活動を登録するとき、休暇を報告するときなど、作業現場労働者が日々の作業を登録する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-104">The job card device is used by the shop floor workers to register their daily work, such as when jobs are started, reporting feedback on jobs, registering indirect activities, and reporting absence.</span></span> <span data-ttu-id="6c818-105">これらの登録は、製造オーダーの進捗と原価を追跡し、従業員の給与の基準を計算する基準として使用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-105">These registrations are the basis for tracking progress and cost on production orders and for calculating the basis for the workers' pay.</span></span> <span data-ttu-id="6c818-106">このトピックでは、ジョブ カード デバイスの構成に使用するさまざまなオプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6c818-106">This topic describes the various options for configuring job card devices.</span></span>

## <a name="enable-new-features-in-feature-management"></a><span data-ttu-id="6c818-107">機能管理で新しい機能を有効化する</span><span class="sxs-lookup"><span data-stu-id="6c818-107">Enable new features in feature management</span></span>

<span data-ttu-id="6c818-108">このトピックで説明するいくつかの設定は、使用する前にシステムで有効化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c818-108">A few of the settings described in this topic must be enabled on your system before they will be available to you.</span></span> <span data-ttu-id="6c818-109">[機能管理 ](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ページを使用して、必要に応じて次の機能のいずれか、またはすべてを有効にします。</span><span class="sxs-lookup"><span data-stu-id="6c818-109">Use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) page to enable any or all of the following features as required.</span></span>

### <a name="generate-license-plate"></a><span data-ttu-id="6c818-110">ライセンス プレートの生成</span><span class="sxs-lookup"><span data-stu-id="6c818-110">Generate license plate</span></span>

<span data-ttu-id="6c818-111">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で次の機能を順に有効化します :</span><span class="sxs-lookup"><span data-stu-id="6c818-111">To make this feature available, enable the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in order):</span></span>

1. <span data-ttu-id="6c818-112">完了報告用ライセンス プレートをジョブ カード デバイスに追加</span><span class="sxs-lookup"><span data-stu-id="6c818-112">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="6c818-113">ジョブ カード デバイスでの完了報告時に、ライセンス プレート番号の自動生成を有効にする</span><span class="sxs-lookup"><span data-stu-id="6c818-113">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>

### <a name="print-label"></a><span data-ttu-id="6c818-114">ラベルの印刷</span><span class="sxs-lookup"><span data-stu-id="6c818-114">Print label</span></span>

<span data-ttu-id="6c818-115">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で次の機能を順に有効化します :</span><span class="sxs-lookup"><span data-stu-id="6c818-115">To make this feature available, enable the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in order):</span></span>

1. <span data-ttu-id="6c818-116">完了報告用ライセンス プレートをジョブ カード デバイスに追加</span><span class="sxs-lookup"><span data-stu-id="6c818-116">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="6c818-117">ジョブ カード デバイスからラベルを印刷</span><span class="sxs-lookup"><span data-stu-id="6c818-117">Print label from Job Card Device</span></span>

### <a name="allow-locking-of-touch-screen"></a><span data-ttu-id="6c818-118">タッチ スクリーンのロックを許可する</span><span class="sxs-lookup"><span data-stu-id="6c818-118">Allow locking of touch screen</span></span>

<span data-ttu-id="6c818-119">この機能を使用できるようにするには、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)で次の機能を有効化します :</span><span class="sxs-lookup"><span data-stu-id="6c818-119">To make this feature available, enable the following feature in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="6c818-120">(プレビュー) 画面ジョブカード デバイスとジョブ カード 端末を除菌できるようにロックする機能です</span><span class="sxs-lookup"><span data-stu-id="6c818-120">(Preview) Feature for locking job card device and job card terminal so that they can be sanitized</span></span>

## <a name="manage-your-device-configurations"></a><span data-ttu-id="6c818-121">デバイスの構成を管理する</span><span class="sxs-lookup"><span data-stu-id="6c818-121">Manage your device configurations</span></span>

<span data-ttu-id="6c818-122">デバイスを構成するには、**生産産管理 > 設定 > 製造の実行 > デバイスで使用するジョブ カードの構成**に移動します。</span><span class="sxs-lookup"><span data-stu-id="6c818-122">To set up your device configurations, go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span> <span data-ttu-id="6c818-123">**ジョブ カードのデバイス構成** ページが開きます。このページには、既存の構成の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-123">The **Configure job card for devices** page opens, which shows a list of existing configurations.</span></span> <span data-ttu-id="6c818-124">ここでは、以下の操作を実行できます :</span><span class="sxs-lookup"><span data-stu-id="6c818-124">From here, you can do the following:</span></span> 

- <span data-ttu-id="6c818-125">左の列に一覧表示されているデバイスの構成を選択して、表示や編集を行います。</span><span class="sxs-lookup"><span data-stu-id="6c818-125">Select any device configuration listed in the left column to view and edit it.</span></span>
- <span data-ttu-id="6c818-126">アクションウィンドウで **新規** を選択し、新たなデバイスの構成を一覧に追加します。</span><span class="sxs-lookup"><span data-stu-id="6c818-126">Select **New** on the Action Pane to add a new device configuration to the list.</span></span> <span data-ttu-id="6c818-127">**構成**フィールドにはこの新しい構成を見分けられるような名前を入力してください。</span><span class="sxs-lookup"><span data-stu-id="6c818-127">Then enter a name in the **Configuration** field to identify the new configuration.</span></span> <span data-ttu-id="6c818-128">ここで入力する値は、すべてのデバイスコンの構成間で一意となっている必要があり、後で編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="6c818-128">The value you enter here must be unique among all device configurations, and you won't be able to edit it later.</span></span>

<span data-ttu-id="6c818-129">ジョブ カード デバイスを構成する各設定の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c818-129">Refer to following sections for details about each of the settings for configuring job card devices.</span></span>

## <a name="general-settings"></a><span data-ttu-id="6c818-130">一般設定</span><span class="sxs-lookup"><span data-stu-id="6c818-130">General settings</span></span>

<span data-ttu-id="6c818-131">**全般** クイックタブでは、選択したデバイスの構成で使用できる各種のオプションを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-131">The **General** FastTab lets you configure each of the various options available for the selected device configuration.</span></span> <span data-ttu-id="6c818-132">次の設定を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6c818-132">The following settings are available:</span></span>

- <span data-ttu-id="6c818-133">**退勤時のレポート数量** - この設定を **はい** に設定すると、作業者は退勤時に進行中のジョブに関するフィードバックを報告するように指示されます。これを**いいえ** を設定すると 、作業者にはこのメッセージが表示されません。</span><span class="sxs-lookup"><span data-stu-id="6c818-133">**Report quantity at clock-out** - Set this to **Yes** to prompt workers to report feedback on jobs in progress when clocking out. When set to **No**, workers won't not be prompted.</span></span>
- <span data-ttu-id="6c818-134">**従業員のロック** - このオプションが **いいえ** に設定されている場合 、各作業者は登録を作成 (新しいジョブなど) した直後にログアウトされ、デバイスはログインページへと戻ります。</span><span class="sxs-lookup"><span data-stu-id="6c818-134">**Lock employee** -  When this option is set to **No**, each worker will be logged out immediately after they make a registration (such as a new job), and then the device will return to the log-in page.</span></span> <span data-ttu-id="6c818-135">このオプションが  **はい** に設定されている場合、各作業者はジョブ カードのデバイスにログインしたままとなります。</span><span class="sxs-lookup"><span data-stu-id="6c818-135">When this option is set to **Yes**, each worker will stay logged in to the job card device.</span></span> <span data-ttu-id="6c818-136">ただし、ジョブ カードのデバイスが同じシステム ユーザー アカウントの下で実行されている間、別の作業者がログインできるように手動でログアウトすることができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-136">However, the worker will still be able to log out manually to allow another worker to log in while the job card device remains running under the same system user account.</span></span> <span data-ttu-id="6c818-137">これらタイプのアカウントの詳細については、[割り当てられたユーザー](#assigned-users)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c818-137">For more information about these types of accounts, see [Assigned users](#assigned-users).</span></span>
- <span data-ttu-id="6c818-138">**バーコードスキャナー** - ジョブ カードのデバイスでこのオプションを **はい** に設定すると、バーコードをスキャンして新たなジョブの開始を登録できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c818-138">**Barcode scanner** - Set this to **Yes** to provide an option on the job card device that allows workers register the start of a new job by scanning a bar code.</span></span>
- <span data-ttu-id="6c818-139">**登録の実際時間を使用する** - この値を **はい** に設定すると、各新規登録の時間が、作業者が登録した正確な時間と等しくなるように設定されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-139">**Use the actual time of registration** - Set this to **Yes** to set the time for each new registration to be equal to the exact time that registration was submitted by a worker.</span></span> <span data-ttu-id="6c818-140">ログイン時刻を代わりに使用するには、**いいえ**に設定 します。</span><span class="sxs-lookup"><span data-stu-id="6c818-140">Set to **No** to use the log-in time instead.</span></span> <span data-ttu-id="6c818-141">**従業員のロック**および/または**単一の作業者**のオプションを有効にしている場合は、これを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c818-141">You'll usually want to set this to **Yes** if you have enabled the **Lock employee** and/or **Single worker** options, where workers often remain logged in for longer periods.</span></span>
- <span data-ttu-id="6c818-142">**単一の作業者** - この構成がアクティブな各ジョブ カードのデバイスを使用する作業者が 1 人だけの場合、このオプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="6c818-142">**Single worker** - Set this option to **Yes** if only one worker uses each job card device where this configuration is active.</span></span> <span data-ttu-id="6c818-143">このオプションを選択すると、**従業員のロック** オプションが自動的に **はい** に設定され ます。</span><span class="sxs-lookup"><span data-stu-id="6c818-143">When this option is selected, the **Lock employee** option is automatically set to **Yes**.</span></span> <span data-ttu-id="6c818-144">さらに、このオプションは、作業者がバッジ ID (または類似するもの) を使用してログインする際の要件 (および機能) を削除します。</span><span class="sxs-lookup"><span data-stu-id="6c818-144">In addition, this option removes the requirement (and ability) for the worker to log in using a badge ID (or similar).</span></span> <span data-ttu-id="6c818-145">その代わりに、*時間登録された作業者* (*作業者* テーブルに由来) にリンクされたシステム ユーザー アカウントを使用して Supply Chain Management にサインインし、同時にその作業者としてジョブ カードのデバイスにログインします。</span><span class="sxs-lookup"><span data-stu-id="6c818-145">Instead the worker signs in to Supply Chain Management using a system user account linked to a *time registered worker* (from the *workers* table) and gets logged in to the job card device as that worker at the same time.</span></span>  <span data-ttu-id="6c818-146">これらタイプのアカウントの詳細については、[割り当てられたユーザー](#assigned-users)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6c818-146">For more information about these types of accounts, see [Assigned users](#assigned-users).</span></span>
- <span data-ttu-id="6c818-147">**個人用フィルターの設定を作業者に許可する** - このオプションを**はい**に設定すると、ユーザーはデバイスで表示されるジョブをフィルター処理できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c818-147">**Allow workers to set personal filters** - Set this option to **Yes** to allow workers to filter the jobs shown to them on the device.</span></span> <span data-ttu-id="6c818-148">作業者は、**生産単位**、**リソース グループ**、 **リソース**の 3 つのフィルタ条件のいずれかの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6c818-148">The worker can modify values for any of the three filter criteria: **Production unit**, **Resource group** and **Resource**.</span></span> <span data-ttu-id="6c818-149">選択したフィルター基準に一致するリソースでスケジュールされているジョブのみがデバイスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-149">Only jobs that are scheduled on resources matching the selected filter criteria will be shown on the device.</span></span> <span data-ttu-id="6c818-150">また、これらの基準のいずれか、またはすべてに対して既定値を割り当てることもでき、このオプションが選択されていない場合でも、既定値が適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-150">You can also assign default values for any or all of these criteria, and those will apply even with this option is not selected.</span></span>
- <span data-ttu-id="6c818-151">**タッチスクリーンのロックを許可する** - このオプションを**はい**に設定すると、作業者はジョブ カードのデバイスのタッチスクリーンをロックして、衛生的に保つことができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-151">**Allow locking the touchscreen** - Set this option to **Yes** to allow workers to lock the job card device touchscreen so they can sanitize it.</span></span> <span data-ttu-id="6c818-152">有効にすると、**除菌用の画面ロック**ボタンがデバイスのログイン ページに追加されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-152">When enabled, a **Lock screen for sanitizing** button is added to the device log-in page.</span></span> <span data-ttu-id="6c818-153">作業者がこのボタンを選択すると、タッチ スクリーンが一時的にロックされ、意図しない入力やカウント ダウン タイマーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-153">When a worker selects this button, the touchscreen temporarily locks to prevent unintended input and a countdown timer is shown.</span></span> <span data-ttu-id="6c818-154">作業者はデバイスと画面を清潔に保つことができるようになります。</span><span class="sxs-lookup"><span data-stu-id="6c818-154">The worker can now safely clean the device and the screen.</span></span> <span data-ttu-id="6c818-155">カウント ダウンが完了すると、タッチスクリーンは自動的にロック解除されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-155">When the countdown completes, the touchscreen automatically unlocks again.</span></span>
- <span data-ttu-id="6c818-156">**画面のロック期間** - **タッチスクリーンのロックを許可する**オプションが有効になっている場合は、このオプションを使用して、タッチスクリーンをロックして除菌する秒数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6c818-156">**Screen lock duration** - When the **Allow locking touchscreen** option is enabled, use this option so specify number of seconds the touchscreen should be locked for sanitizing.</span></span> <span data-ttu-id="6c818-157">ここには 5 秒から 120 秒を表わす数値を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c818-157">The duration must be between 5 and 120 seconds.</span></span>
- <span data-ttu-id="6c818-158">**生産単位** - 各作業者に対して表示されるジョブの一覧については、既定のフィルタ条件として適用する生産単位を選択します。</span><span class="sxs-lookup"><span data-stu-id="6c818-158">**Production unit** - Select a production unit to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6c818-159">デバイスで最初に表示されジョブは、選択した生産単位の下にグループ化されたリソースでスケジュールされているジョブのみです。</span><span class="sxs-lookup"><span data-stu-id="6c818-159">Only jobs that are scheduled on resources grouped under the selected production unit will initially be displayed by the device.</span></span> <span data-ttu-id="6c818-160">**作業者に個人フィルターの設定を許可する** が有効になっている場合は、作業者がこの値を編集できます。それ以外の場合、このデバイスの構成が有効な場合は、このフィルターが常に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-160">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6c818-161">**リソース グループ** - 各作業者に表示されるジョブのリストで使用する既定のフィルター基準として適用するリソースグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c818-161">**Resource group** - Select a resource group to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6c818-162">デバイスで最初に表示されるジョブは、選択したリソース グループの配下にグループ化されたリソースでスケジュールされているジョブのみです。</span><span class="sxs-lookup"><span data-stu-id="6c818-162">Only jobs that are scheduled on resources grouped under the selected resource group will initially be displayed by the device.</span></span> <span data-ttu-id="6c818-163">**作業者に個人フィルターの設定を許可する** が有効になっている場合は、作業者がこの値を編集できます。それ以外の場合、このデバイスの構成が有効な場合は、このフィルターが常に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-163">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6c818-164">**リソース グループ** - 各作業者に表示されるジョブのリストで使用する既定のフィルター基準として適用するリソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="6c818-164">**Resource** - Select a resource to be applied as a default filter criterion for the list of jobs shown to each worker.</span></span> <span data-ttu-id="6c818-165">デバイスに初期表示されるジョブは、選択したリソースでスケジュールされているジョブのみです。</span><span class="sxs-lookup"><span data-stu-id="6c818-165">Only jobs that are scheduled on the selected resource will initially be displayed by the device.</span></span> <span data-ttu-id="6c818-166">**作業者に個人フィルターの設定を許可する** が有効になっている場合は、作業者がこの値を編集できます。それ以外の場合、このデバイスの構成が有効な場合は、このフィルターが常に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-166">If **Allow workers to set personal filters** is enabled, workers will be able to edit this value, otherwise this filter will always apply when this device configuration is active.</span></span>
- <span data-ttu-id="6c818-167">**ライセンス プレートの生成** - このオプションを **はい** に設定すると、作業者がジョブ カード デバイスを使用するたびに新しいライセンス プレートを生成し、作業の完了報告することができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-167">**Generate license plate** - Set this option to **Yes** to generate a new license plate each time a worker uses the job card device to report as finished.</span></span> <span data-ttu-id="6c818-168">ライセンス プレート番号は、**倉庫管理パラメータ** ページで設定された番号の順序に従って生成されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-168">The license plate number is generated from a number sequence set up on the **Warehouse management parameters** page.</span></span> <span data-ttu-id="6c818-169">**いいえ** に設定すると、作業者は完了報告時に既存のライセンス プレートを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c818-169">When set to **No**, workers must specify an existing license plate when reporting as finished.</span></span>
- <span data-ttu-id="6c818-170">**印刷ラベル** - このオプションを**はい**に設定すると、作業員がジョブカード デバイスを使用して完了報告する際に、ライセンス プレートのラベルを印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-170">**Print label** - Set this option to **Yes** to print a license plate label when a worker uses the job card device to report as finished.</span></span> <span data-ttu-id="6c818-171">ラベルの構成は、ドキュメントのルーティングに設定されており、[ライセンス プレートのラベルに使用するドキュメント ルーティング レイアウト](../warehousing/document-routing-layout-for-license-plates.md)に記載されています。</span><span class="sxs-lookup"><span data-stu-id="6c818-171">The configuration of the label is set up in document routing, as described in [Document routing layout for license plate labels](../warehousing/document-routing-layout-for-license-plates.md).</span></span>

<a name="assigned-users"></a>

## <a name="assigned-users"></a><span data-ttu-id="6c818-172">割り当て済ユーザー</span><span class="sxs-lookup"><span data-stu-id="6c818-172">Assigned users</span></span>

<span data-ttu-id="6c818-173">**割り当てられたユーザー** のクイックタブを使用して、1つ以上のシステム ユーザーを現在のデバイスの構成に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="6c818-173">Use the **Assigned users** FastTab to associate one or more system users with the current device configuration.</span></span> <span data-ttu-id="6c818-174">各システムユーザーには、1つのジョブのデバイス構成のみを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-174">Each system user can only be assigned one job device configuration.</span></span>

<span data-ttu-id="6c818-175">通常、IT 作業者はデバイスを設定する際に、システム ユーザーのアカウントを使用して Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="6c818-175">When setting up a device, an IT worker typically signs in to Supply Chain Management using a system user account.</span></span> <span data-ttu-id="6c818-176">その後、そのシステ ムユーザがサインインしている間、そのシステム ユーザーに関連付けられたジョブ デバイスの構成を適用します。</span><span class="sxs-lookup"><span data-stu-id="6c818-176">Thereafter, the job device configuration associated with that system user applies for as long as that system user remains signed in.</span></span> <span data-ttu-id="6c818-177">通常、これらのシステム ユーザーのアカウントは、ジョブ カード デバイスのページに対してのみアクセスを許可し、Supply Chain Management のその他の部分に対しては許可しないように制限されます。</span><span class="sxs-lookup"><span data-stu-id="6c818-177">These system user accounts are typically limited to allow access only to the job card device page and no other part of Supply Chain Management.</span></span>

<span data-ttu-id="6c818-178">システム ユーザーがログインしてジョブ デバイスの構成が読み込まれた後、作業者は (自身のバッジに記されたバーコードをスキャンして) *時間登録労働者*のアカウントでジョブ カード デバイスにログオンし、新しいジョブを開始したり、その他種類の登録を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="6c818-178">After the system user is signed in and the job device configuration is loaded, workers can then log in to the job card device using their *time registered worker* account (for example, by scanning a bar code on their badge) so they can start new jobs and make other kinds of registrations.</span></span> <span data-ttu-id="6c818-179">一日の間で様々な作業者がにログイン/ログアウトすることができますが、システムユーザがその日の間、Supply Chain Management にサイン インしたままであるため、そのマシンでは同じデバイス構成が有効になっています。</span><span class="sxs-lookup"><span data-stu-id="6c818-179">Various workers can log in and out during the day, while the same device configuration remains in effect on that machine because the system user remains signed in to Supply Chain Management for the day.</span></span>

<span data-ttu-id="6c818-180">**単一の作業者**オプションでデバイスの構成を使用する場合、作業者自身は通常、自身の*時間登録された労働者* のアカウントにリンクされたシステム ユーザーを使用して Supply Chain Management にサインインするため、デバイスの構成をロードすると同時にジョブ カード デバイス上の労働者としてログインします。</span><span class="sxs-lookup"><span data-stu-id="6c818-180">However, as mentioned previously, when you use a device configuration with the **Single worker** option, workers themselves typically sign in to Supply Chain Management using a system user linked to their own *time registered worker* account, so they load the device configuration and log in as a worker on the job card device at the same time.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c818-181">追加リソース</span><span class="sxs-lookup"><span data-stu-id="6c818-181">Additional resources</span></span>

[<span data-ttu-id="6c818-182">ジョブ カード デバイスから完了報告をする</span><span class="sxs-lookup"><span data-stu-id="6c818-182">Report as finished from the job card device</span></span>](report-finished-job-device.md)