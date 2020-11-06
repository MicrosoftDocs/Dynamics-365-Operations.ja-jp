---
title: 生産現場の実行インターフェースを実行するデバイスを設定する
description: 生産現場の実行インターフェイスは、生産現場のすべてのデバイスに対して設定されます。 通常、会社では、デバイスのサービスの目的に応じて、各デバイスの設定を変えることができます。 たとえば、ある会社では、作業者が出勤時間および退勤時間を記録する受付エリアに 1 台のデバイスがあり、作業者が作業を管理する作業現場に別のデバイスがあるとします。
author: johanhoffmann
manager: tfehr
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 57f09bf907407e19ae0e693de64510f7f4efbf0b
ms.sourcegitcommit: 9dd2d38e76d4d93171315ec319e6ce7d51d4e6c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2020
ms.locfileid: "4012490"
---
# <a name="set-up-a-device-to-run-the-production-floor-execution-interface"></a><span data-ttu-id="2d194-105">生産現場の実行インターフェースを実行するデバイスを設定する</span><span class="sxs-lookup"><span data-stu-id="2d194-105">Set up a device to run the production floor execution interface</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="2d194-106">生産現場の実行インターフェイスは、生産現場のすべてのデバイスに対して設定されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-106">The production floor execution interface is set up for every device on the production floor.</span></span> <span data-ttu-id="2d194-107">通常、会社では、デバイスのサービスの目的に応じて、各デバイスの設定を変えることができます。</span><span class="sxs-lookup"><span data-stu-id="2d194-107">Companies typically set up each device differently, depending on the purpose that the device serves.</span></span> <span data-ttu-id="2d194-108">たとえば、ある会社では、作業者が出勤時間および退勤時間を記録する受付エリアに 1 台のデバイスがあり、作業者が作業を管理する作業現場に別のデバイスがあるとします。</span><span class="sxs-lookup"><span data-stu-id="2d194-108">For example, a company might have one device in the reception area, where workers clock in and clock out, and another on the shop floor, where workers manage their jobs.</span></span>

## <a name="set-the-configuration-and-filters-for-a-specific-device"></a><span data-ttu-id="2d194-109">特定のデバイスの構成とフィルタの設定</span><span class="sxs-lookup"><span data-stu-id="2d194-109">Set the configuration and filters for a specific device</span></span>

<span data-ttu-id="2d194-110">デバイスの構成とジョブ フィルターを設定するには、 *時間スーパーバイザーの管理* 権限を含むセキュリティ ロールを持つアカウントを使用して、 **生産現場の実行** ページにサインインします。</span><span class="sxs-lookup"><span data-stu-id="2d194-110">To set the configuration and job filters for a device, sign in to the **Production floor execution** page by using an account that has a security role that includes the *Maintain time supervisor* duty.</span></span> <span data-ttu-id="2d194-111">(最初から用意されているセキュリティ ロールの中で、 *作業現場の監督* だけがこの権限を持ちます。) 次に、以下の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="2d194-111">(Among the out-of-box security roles, only *Shop floor supervisor* has this duty.) Then follow these steps.</span></span>

1. <span data-ttu-id="2d194-112">設定するデバイスに移動して、作業現場監督として Microsoft Dynamics 365 Supply Chain Management にサインインします。</span><span class="sxs-lookup"><span data-stu-id="2d194-112">Go to the device that you want to set up, and sign in to Microsoft Dynamics 365 Supply Chain Management as a shop floor supervisor.</span></span> <span data-ttu-id="2d194-113">( *時間スーパーバイザーの管理* 権限を含むアカウントを使用します。)</span><span class="sxs-lookup"><span data-stu-id="2d194-113">(Use an account that includes the *Maintain time supervisor* duty.)</span></span>
1. <span data-ttu-id="2d194-114">設定するデバイスの構成が使用可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2d194-114">Make sure that a configuration is available for the device that you're setting up.</span></span> <span data-ttu-id="2d194-115">構成がまだ存在しない場合は、既定の構成が提供されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-115">If no configuration already exists, a default configuration is provided.</span></span> <span data-ttu-id="2d194-116">構成の設定方法については、[生産現場の実行インターフェースを構成する](production-floor-execution-configure.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2d194-116">For more information about how to set up a configuration, see [Configure the production floor execution interface](production-floor-execution-configure.md).</span></span>
1. <span data-ttu-id="2d194-117">**生産管理 \> 製造実行 \> 生産現場の実行** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d194-117">Go to **Production control \> Manufacturing execution \> Production floor execution**.</span></span>

    <span data-ttu-id="2d194-118">生産現場の実行インターフェイスが、現在のデバイスで少なくとも 1 回、既に構成されている場合は、サインイン ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-118">If the production floor execution interface has already been configured at least one time on the current device, a sign-in page appears.</span></span> <span data-ttu-id="2d194-119">それ以外の場合は、ウェルカム ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-119">Otherwise, a welcome page appears.</span></span>

1. <span data-ttu-id="2d194-120">サインイン ページまたはウェルカム ページで、 **構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-120">On either the sign-in page or the welcome page, select **Configure**.</span></span>
1. <span data-ttu-id="2d194-121">一覧で構成を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-121">Select a configuration in the list.</span></span>
1. <span data-ttu-id="2d194-122">**次へ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-122">Select **Next**.</span></span>
1. <span data-ttu-id="2d194-123">現在のデバイスに適用する 1 つ以上のフィルターを選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-123">Select one or more filters to apply to the current device.</span></span> <span data-ttu-id="2d194-124">これらのフィルターを使用すると、関連するジョブのみをデバイスに表示することができます。</span><span class="sxs-lookup"><span data-stu-id="2d194-124">These filters will help ensure that only relevant jobs are shown on the device.</span></span> <span data-ttu-id="2d194-125">フィルターを設定するには、フィルター タイプを選択して値の一覧を開き、フィルター処理する値を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-125">To set a filter, select the filter type to open a list of values, and then select the value to filter on.</span></span> <span data-ttu-id="2d194-126">次のフィルターを使用できます:</span><span class="sxs-lookup"><span data-stu-id="2d194-126">The following filters are available:</span></span>

    - <span data-ttu-id="2d194-127">**生産単位** : このフィルターは最上位レベルのフィルターです。</span><span class="sxs-lookup"><span data-stu-id="2d194-127">**Production unit** – This filter is the highest-level filter.</span></span> <span data-ttu-id="2d194-128">通常は、複数のリソース グループと個別のリソースを含む大きな作業領域を指します。</span><span class="sxs-lookup"><span data-stu-id="2d194-128">It typically refers to a large work area that has several resource groups and individual resources in it.</span></span>
    - <span data-ttu-id="2d194-129">**リソース グループ** – このフィルターは中間レベルのフィルターです。</span><span class="sxs-lookup"><span data-stu-id="2d194-129">**Resource group** – This filter is a mid-level filter.</span></span> <span data-ttu-id="2d194-130">通常は、ワークスペースの限られた領域にある関連リソースのコレクションを指します。</span><span class="sxs-lookup"><span data-stu-id="2d194-130">It typically refers to a collection of related resources in a limited area of the workspace.</span></span> <span data-ttu-id="2d194-131">最初に **生産単位** フィルターを選択すると、リソース グループの一覧には、その単位からグループのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-131">If you select a **Production unit** filter first, the list of resource groups shows only groups from that unit.</span></span> <span data-ttu-id="2d194-132">それ以外の場合は、使用可能なすべてのリソース グループが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-132">Otherwise, it shows all available resource groups.</span></span>
    - <span data-ttu-id="2d194-133">**リソース** : このフィルタは、最も限定的なフィルターです。</span><span class="sxs-lookup"><span data-stu-id="2d194-133">**Resource** – This filter is the most specific filter.</span></span> <span data-ttu-id="2d194-134">通常、特定のマシンまたはその他の単一のリソースを指します。</span><span class="sxs-lookup"><span data-stu-id="2d194-134">It typically refers to a specific machine or other single resource.</span></span> <span data-ttu-id="2d194-135">最初に **リソース グループ** および/または **生産単位** フィルターを選択すると、リソースの一覧には、そのグループおよび/または単位からリソースのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-135">If you select a **Resource group** and/or **Production unit** filter first, the list of resources shows only resources from that group and/or unit.</span></span> <span data-ttu-id="2d194-136">それ以外の場合は、使用可能なすべてのリソースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-136">Otherwise, it shows all available resources.</span></span>

1. <span data-ttu-id="2d194-137">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="2d194-137">Select **OK**.</span></span>
1. <span data-ttu-id="2d194-138">サインイン ページが表示され、デバイスを使用できる状態になります。</span><span class="sxs-lookup"><span data-stu-id="2d194-138">The sign-in page appears, and your device is ready for use.</span></span>

## <a name="allow-a-worker-to-override-the-default-filters"></a><span data-ttu-id="2d194-139">作業者が既定のフィルターを上書きできるようにする</span><span class="sxs-lookup"><span data-stu-id="2d194-139">Allow a worker to override the default filters</span></span>

<span data-ttu-id="2d194-140">特定の作業者に、使用するデバイスのフィルター設定を変更するアクセス許可を与えることができます。</span><span class="sxs-lookup"><span data-stu-id="2d194-140">You can give specific workers permission to change the filter settings on any device that they use.</span></span> <span data-ttu-id="2d194-141">このアクセス許可を持つ作業者の場合、生産現場の実行インターフェイスの **すべてのジョブ** ページと **有効なジョブ** ページに **フィルター** ボタンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-141">For workers who have this permission, the production floor execution interface provides a **Filter** button on the **All jobs** and **Active job** pages.</span></span>

> [!NOTE]
> <span data-ttu-id="2d194-142">作業者がフィルターを変更すると、その時点から、デバイスにサインインするユーザーすべてに、新しいフィルターが適用されます。</span><span class="sxs-lookup"><span data-stu-id="2d194-142">If a worker changes a filter, the new filter applies from that point forward, for all users who sign in to the device.</span></span>

<span data-ttu-id="2d194-143">デバイスに対して設定されている既定のジョブ フィルターを作業者が上書きできるようにするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="2d194-143">To allow a worker to override the default job filters that have been set up for a device, follow these steps.</span></span>

1. <span data-ttu-id="2d194-144">**時刻と出勤 \> 設定 \> 時間登録作業者** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d194-144">Go to **Time and attendance \> Setup \> Time registration workers**.</span></span>
1. <span data-ttu-id="2d194-145">一覧で作業者を選択して、その作業者の **時間登録作業者** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="2d194-145">Select a worker in the list to open that worker's **Time registration workers** page.</span></span>
1. <span data-ttu-id="2d194-146">**時間登録** タブで、 **フィルターの設定** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="2d194-146">On the **Time registration** tab, set the **Set filters** option to *Yes*.</span></span>

## <a name="run-the-interface-in-full-screen-mode"></a><span data-ttu-id="2d194-147">インターフェイスを全画面表示モードで実行する</span><span class="sxs-lookup"><span data-stu-id="2d194-147">Run the interface in full-screen mode</span></span>

<span data-ttu-id="2d194-148">多くの場合、生産現場の実行インターフェイスを、その目的専用に使用されるデバイス上で実行します。</span><span class="sxs-lookup"><span data-stu-id="2d194-148">Often, you will run the production floor execution interface on a device that is used exclusively for that purpose.</span></span> <span data-ttu-id="2d194-149">したがって、ナビゲーションおよび/またはブラウザー Chrome を表示せずに、インターフェイスを全画面モードで実行することは理にかなっている場合があります。</span><span class="sxs-lookup"><span data-stu-id="2d194-149">Therefore, it might make sense to run the interface in full-screen mode, without showing any navigation and/or browser chrome.</span></span>

- <span data-ttu-id="2d194-150">Supply Chain Management に表示されるナビゲーション ウィンドウを非表示にするには、ブラウザーのアドレス バー: `\&limitednav=true` で、次のテキストを URL の末尾に追加します。</span><span class="sxs-lookup"><span data-stu-id="2d194-150">To hide the navigation pane that is shown in Supply Chain Management, add the following text to the end of the URL in the browser's address bar: `\&limitednav=true`.</span></span>
- <span data-ttu-id="2d194-151">ブラウザーのアドレス バーも非表示にするには、ブラウザーのネイティブ全画面モードを使用します。</span><span class="sxs-lookup"><span data-stu-id="2d194-151">To also hide the browser's address bar, use the browser's native full-screen mode.</span></span> <span data-ttu-id="2d194-152">(手順については、ブラウザー ドキュメントを参照してください。)</span><span class="sxs-lookup"><span data-stu-id="2d194-152">(For instructions, see your browser's documentation.)</span></span>

<span data-ttu-id="2d194-153">次の図の上部には、インターフェイスが既定でどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="2d194-153">The upper part of the following illustration shows how the interface looks by default.</span></span> <span data-ttu-id="2d194-154">下の部分は、ナビゲーション ウィンドウが非表示の場合、全画面モードでどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="2d194-154">The lower part shows how it looks in full-screen mode when the navigation pane is hidden.</span></span>

<span data-ttu-id="2d194-155">![標準対全画面表示インターフェイス](media/pfei-full-screen.png "標準対全画面表示インターフェイス")</span><span class="sxs-lookup"><span data-stu-id="2d194-155">![Standard vs. full-screen interface](media/pfei-full-screen.png "Standard vs. full-screen interface")</span></span>

## <a name="extend-the-session-past-12-hours"></a><span data-ttu-id="2d194-156">12 時間経過したセッションを延長する</span><span class="sxs-lookup"><span data-stu-id="2d194-156">Extend the session past 12 hours</span></span>

<span data-ttu-id="2d194-157">既定では、生産現場の実行インターフェースは、12 時間誰も使用しない場合、自動的にサインアウトします。</span><span class="sxs-lookup"><span data-stu-id="2d194-157">By default, the production floor execution interface automatically signs out if nobody uses it for 12 hours.</span></span> <span data-ttu-id="2d194-158">Supply Chain Management ユーザーは、再度サインインする必要があります。</span><span class="sxs-lookup"><span data-stu-id="2d194-158">A Supply Chain Management user must then sign in again.</span></span> <span data-ttu-id="2d194-159">ただし、タイムアウト制限を最大 90 日まで延長できます。</span><span class="sxs-lookup"><span data-stu-id="2d194-159">However, you can extend the time-out limit to up to 90 days.</span></span>

<span data-ttu-id="2d194-160">タイムアウト制限を延長するには、Supply Chain Management にサインインし、 **システム管理 \> ユーザー \> セッション拡張機能** に移動します。</span><span class="sxs-lookup"><span data-stu-id="2d194-160">To extend the time-out limit, sign in to Supply Chain Management, and go to **System administration \> Users \> Session extensions**.</span></span> <span data-ttu-id="2d194-161">デバイスへのサインインに使用する Supply Chain Management のユーザー アカウントと、セッションをアクティブにしておく時間数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2d194-161">Specify the Supply Chain Management user account that is used to sign in to the device, and the number of hours that the session should stay active for.</span></span>
