---
title: メンテナンス モード
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードに関する情報を提供します。 メンテナンス モードは、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できるシステム全体に適用される設定です。
author: manalidongre
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysConfiguration
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 70292
ms.assetid: c11a35e8-40bb-4005-adf3-cfd998a418fc
ms.search.region: Global
ms.author: manado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b1ced105f238b6cd97d17c114478128cc9ea6b1
ms.sourcegitcommit: 980cf8280538f37d64c477576a67f66bb00252d3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/05/2019
ms.locfileid: "776910"
---
# <a name="maintenance-mode"></a><span data-ttu-id="aa1e6-104">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="aa1e6-104">Maintenance mode</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="aa1e6-105">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のメンテナンス モードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-105">This topic provides information about maintenance mode in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="aa1e6-106">メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-106">When maintenance mode is turned on, it provides a safe way for system administrators to make system changes that might affect system functionality.</span></span> <span data-ttu-id="aa1e6-107">たとえば、コンフィギュレーション キーは、有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-107">For example, configuration keys can be enabled or disabled.</span></span> <span data-ttu-id="aa1e6-108">メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-108">While maintenance mode is on, only system administrators and users who have the **Maintenance mode user** role can sign in to the system.</span></span> <span data-ttu-id="aa1e6-109">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-109">By default, maintenance mode is turned off.</span></span> <span data-ttu-id="aa1e6-110">メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-110">When maintenance mode is off, you can't edit the **License configuration** page.</span></span>

## <a name="turn-maintenance-mode-on-and-off-on-sandbox-and-production-environments-through-lifecycle-services"></a><span data-ttu-id="aa1e6-111">Lifecycle Services を通じてサンドボックスおよび運用環境でメンテナンス モードを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="aa1e6-111">Turn maintenance mode on and off on sandbox and production environments through Lifecycle Services</span></span> 
<span data-ttu-id="aa1e6-112">サンドボックスおよび運用環境で、Lifecycle Services (LCS) を通じて直接メンテナンス モードを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-112">You can now turn maintenance mode on and off directly through Lifecycle Services (LCS) on your sandbox and production environments.</span></span> <span data-ttu-id="aa1e6-113">これを行うには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-113">Refer to the following steps to do this:</span></span>

1. <span data-ttu-id="aa1e6-114">環境の詳細ページに移動し、**メンテナンス** メニューで **メンテナンス モードの構成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-114">Go to the environment details page and on the **Maintain** menu and click **Configure Maintenance Mode**.</span></span> <span data-ttu-id="aa1e6-115">プレビューに追加された顧客に対してこのメニュー項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-115">This menu item will display for customers added to the preview.</span></span>
2. <span data-ttu-id="aa1e6-116">スライダーで、環境の **メンテナンス モードを有効にする** を設定し、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-116">In the slider, set **Turn maintenance mode on** for the environment and select **Confirm**.</span></span>
3. <span data-ttu-id="aa1e6-117">サービス工程が開始され、システムがメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-117">A servicing operation will begin and your system  will go into maintenance mode.</span></span>
4. <span data-ttu-id="aa1e6-118">完了時、環境の状態が **メンテナンス中** になります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-118">On completion, the environment state will be **In Maintenance**.</span></span> <span data-ttu-id="aa1e6-119">この時点では、システム管理者だけが環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-119">At this point, only the system administrator will have access to the environment.</span></span>
5. <span data-ttu-id="aa1e6-120">システム全体にわたる変更を完了した後、環境更新セクションで **メンテナンス モードの無効化** をクリックすることで、メンテナンス モードをオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-120">After you are done making system-wide changes, you can turn off maintenance mode by clicking **Disable Maintenance Mode** in the environment updates section.</span></span>
6. <span data-ttu-id="aa1e6-121">これにより、環境のメンテナンス モードを終了するサービス操作が開始されます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-121">This will start a servicing operation that takes your environment out of maintenance mode.</span></span> <span data-ttu-id="aa1e6-122">環境の詳細ページで、工程の進捗状況を確認できます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-122">You can see the progress of the operation in the environment details page.</span></span>
7. <span data-ttu-id="aa1e6-123">これが完了すると、環境が **配置中** 状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-123">After this is complete, your environment goes back to the **Deployed** state.</span></span> <span data-ttu-id="aa1e6-124">すべてのユーザーが環境にログオンできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-124">Now all users can sign in to the environment.</span></span>
8. <span data-ttu-id="aa1e6-125">メンテナンス モードが有効または無効かを環境の履歴ページで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-125">You can check the environment history page to see when the maintenance mode was turned on or turned off.</span></span> <span data-ttu-id="aa1e6-126">環境履歴ページに移動するには環境の詳細ページで **履歴** および **環境の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-126">To get to the environment history page, select **History** and **Environment changes** on the environment details page.</span></span>

<span data-ttu-id="aa1e6-127">サンドボックスおよび運用環境のメンテナンス モードをオン/オフにする操作と、サービス操作にとても似ています。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-127">Turning maintenance mode on and off for your sandbox and production environment is very similar to a servicing operation.</span></span> <span data-ttu-id="aa1e6-128">メンテナンス モードのオンまたはオフに失敗した場合は、**再開**、**ロールバック**、および **中止** などのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-128">If turning maintenance mode on or off fails, you will see options such as **Resume**, **Rollback**, and **Abort**.</span></span> <span data-ttu-id="aa1e6-129">操作に失敗した理由をトラブルシューティングするために**ログをダウンロード**するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-129">You also have the option to **download the logs** to troubleshoot why the operation failed.</span></span>

## <a name="turn-maintenance-mode-on-and-off-in-devtestdemo-environments-and-vhd-based-hosted-environments"></a><span data-ttu-id="aa1e6-130">DevTest/デモ環境およびVHD ベースのホストされている環境でメンテナンス モードのオンとオフを切り替える</span><span class="sxs-lookup"><span data-stu-id="aa1e6-130">Turn maintenance mode on and off in DevTest/Demo environments and VHD-based hosted environments</span></span>

<span data-ttu-id="aa1e6-131">次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-131">You can turn on maintenance mode locally by running the following command.</span></span> 

> [!Note]
> <span data-ttu-id="aa1e6-132">一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-132">On some virtual machines (VMs), the exact location of the Deployment.Setup.exe tool might differ.</span></span> <span data-ttu-id="aa1e6-133">AosServiceWebRootbin を確認してください。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-133">Check AosServiceWebRootbin.</span></span>

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true

<span data-ttu-id="aa1e6-134">次のテーブルに、このコマンドで使用されるパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-134">The following table describes the parameters that are used in this command.</span></span>

| <span data-ttu-id="aa1e6-135">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="aa1e6-135">Parameter name</span></span>              | <span data-ttu-id="aa1e6-136">説明</span><span class="sxs-lookup"><span data-stu-id="aa1e6-136">Description</span></span>  |
|-----------------------------|------|
| <span data-ttu-id="aa1e6-137">--setupmode maintenancemode</span><span class="sxs-lookup"><span data-stu-id="aa1e6-137">--setupmode maintenancemode</span></span> | <span data-ttu-id="aa1e6-138">システムをメンテナンス モードにするかメンテナンス モードを解除するかをセットアップ ツールに通知するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-138">Use this parameter to inform the setup tool that the system will be put into or taken out of maintenance mode.</span></span>    |
| <span data-ttu-id="aa1e6-139">--metadatadir</span><span class="sxs-lookup"><span data-stu-id="aa1e6-139">--metadatadir</span></span>               | <span data-ttu-id="aa1e6-140">メタデータ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-140">Use this parameter to specify the metadata directory.</span></span> <span data-ttu-id="aa1e6-141">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-141">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="aa1e6-142">--bindir</span><span class="sxs-lookup"><span data-stu-id="aa1e6-142">--bindir</span></span>                    | <span data-ttu-id="aa1e6-143">バイナリ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-143">Use this parameter to specify the binaries directory.</span></span> <span data-ttu-id="aa1e6-144">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-144">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="aa1e6-145">--sqlserver</span><span class="sxs-lookup"><span data-stu-id="aa1e6-145">--sqlserver</span></span>                 | <span data-ttu-id="aa1e6-146">このパラメーターを使用して Microsoft SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-146">Use this parameter to specify the Microsoft SQL Server.</span></span> <span data-ttu-id="aa1e6-147">1 ボックス環境では、ピリオド (**.**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-147">For one-box environments, use a period (**.**).</span></span>           |
| <span data-ttu-id="aa1e6-148">--sqluser</span><span class="sxs-lookup"><span data-stu-id="aa1e6-148">--sqluser</span></span>                   | <span data-ttu-id="aa1e6-149">SQL Server のユーザーを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-149">Use this parameter to specify the SQL Server user.</span></span> <span data-ttu-id="aa1e6-150">**AOSUser** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-150">You should use **AOSUser**.</span></span>                                    |
| <span data-ttu-id="aa1e6-151">--sqlpwd</span><span class="sxs-lookup"><span data-stu-id="aa1e6-151">--sqlpwd</span></span>                    | <span data-ttu-id="aa1e6-152">SQL Server のパスワードを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-152">Use this parameter to specify the SQL Server password.</span></span>                                                            |
| <span data-ttu-id="aa1e6-153">--isinmaintenancemode</span><span class="sxs-lookup"><span data-stu-id="aa1e6-153">--isinmaintenancemode</span></span>       | <span data-ttu-id="aa1e6-154">構成モードを有効または無効にするには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-154">Use this parameter to turn configuration mode on or off.</span></span> <span data-ttu-id="aa1e6-155">オンにするには **true** とし、オフにするには **false** にします。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-155">Use **true** to turn it on and **false** to turn it off.</span></span> |

<span data-ttu-id="aa1e6-156">Finance and Operations の Application Object Server (AOS) のインスタンスを再起動すると、システムはメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-156">After the instance of Finance and Operations Application Object Server (AOS) is restarted, the system will be in maintenance mode.</span></span> <span data-ttu-id="aa1e6-157">次のスクリーンショットに示すように、構成キーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-157">You can then enable configuration keys, as shown in the following screenshot.</span></span> 

<span data-ttu-id="aa1e6-158">[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span><span class="sxs-lookup"><span data-stu-id="aa1e6-158">[![license-configuration-page-when-not-in-maintenance-mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span></span> 

<span data-ttu-id="aa1e6-159">システムがメンテナンス モードになっているときに、システム管理者または**メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-159">If you try to access Finance and Operations while the system is in maintenance mode, but you aren't a system administrator or a user who has the **Maintenance mode user** role, you may receive an error message.</span></span> 

<span data-ttu-id="aa1e6-160">次のコマンドを実行して、メンテナンス モードをオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="aa1e6-160">You can turn off maintenance mode by running the following command.</span></span>

    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false

