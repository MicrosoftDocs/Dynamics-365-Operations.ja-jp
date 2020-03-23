---
title: メンテナンス モード
description: このトピックでは、メンテナンス モードに関する情報を提供しています。システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行できるシステム全体に適用される設定です。
author: laneswenka
manager: AnnBe
ms.date: 05/10/2019
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
ms.author: laswenka
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ede4d8b0eb45693f15afe3e26ae9bc4e7c7c71a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096935"
---
# <a name="maintenance-mode"></a><span data-ttu-id="04710-103">メンテナンス モード</span><span class="sxs-lookup"><span data-stu-id="04710-103">Maintenance mode</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/limited-availability.md)]

<span data-ttu-id="04710-104">このトピックでは、Finance and Operations のメンテナンス モードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="04710-104">This topic provides information about maintenance mode in Finance and Operations.</span></span> <span data-ttu-id="04710-105">メンテナンス モードを有効にすると、システム機能に影響を与える可能性のあるシステム変更を、システム管理者が安全に実行する方法が提供されます。</span><span class="sxs-lookup"><span data-stu-id="04710-105">When maintenance mode is turned on, it provides a safe way for system administrators to make system changes that might affect system functionality.</span></span> <span data-ttu-id="04710-106">たとえば、コンフィギュレーション キーは、有効または無効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-106">For example, configuration keys can be enabled or disabled.</span></span> <span data-ttu-id="04710-107">メンテナンス モードがオンのとき、システム管理者および **メンテナンス モード ユーザー** ロールを持つユーザーのみがシステムにサインインすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-107">While maintenance mode is on, only system administrators and users who have the **Maintenance mode user** role can sign in to the system.</span></span> <span data-ttu-id="04710-108">既定では、メンテナンス モードがオフになっています。</span><span class="sxs-lookup"><span data-stu-id="04710-108">By default, maintenance mode is turned off.</span></span> <span data-ttu-id="04710-109">メンテナンス モードがオフのとき、**ライセンス コンフィギュレーション** ページを編集することはできません。</span><span class="sxs-lookup"><span data-stu-id="04710-109">When maintenance mode is off, you can't edit the **License configuration** page.</span></span>

## <a name="turn-maintenance-mode-on-and-off-on-sandbox-and-production-environments-through-lifecycle-services"></a><span data-ttu-id="04710-110">Lifecycle Services を通じてサンドボックスおよび運用環境でメンテナンス モードを有効または無効にする</span><span class="sxs-lookup"><span data-stu-id="04710-110">Turn maintenance mode on and off on sandbox and production environments through Lifecycle Services</span></span> 
<span data-ttu-id="04710-111">サンドボックスおよび運用環境で、Lifecycle Services (LCS) を通じて直接メンテナンス モードを有効または無効にできます。</span><span class="sxs-lookup"><span data-stu-id="04710-111">You can now turn maintenance mode on and off directly through Lifecycle Services (LCS) on your sandbox and production environments.</span></span> <span data-ttu-id="04710-112">これを行うには、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="04710-112">Refer to the following steps to do this:</span></span>

1. <span data-ttu-id="04710-113">環境の詳細ページに移動し、 **メンテナンス** メニューで **メンテナンス モードの有効化** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="04710-113">Go to the environment details page and on the **Maintain** menu, click **Enable Maintenance Mode**.</span></span> 
2. <span data-ttu-id="04710-114">スライダーで、環境の **メンテナンス モードを有効にする** を設定し、**確認** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04710-114">In the slider, set **Turn maintenance mode on** for the environment and select **Confirm**.</span></span>
3. <span data-ttu-id="04710-115">サービス工程が開始され、システムがメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="04710-115">A servicing operation will begin and your system  will go into maintenance mode.</span></span>
4. <span data-ttu-id="04710-116">完了時、環境の状態が **メンテナンス中** になります。</span><span class="sxs-lookup"><span data-stu-id="04710-116">On completion, the environment state will be **In Maintenance**.</span></span> <span data-ttu-id="04710-117">この時点では、システム管理者だけが環境にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="04710-117">At this point, only the system administrator will have access to the environment.</span></span>
5. <span data-ttu-id="04710-118">システム全体の変更を完了後、 **メンテナンス** メニューの **メンテナンスモードの無効化** をクリックすることで、メンテナンス モードをオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-118">After you are done making system-wide changes, you can turn off maintenance mode by clicking **Disable Maintenance Mode** under the **Maintain** menu.</span></span>
6. <span data-ttu-id="04710-119">これにより、環境のメンテナンス モードを終了するサービス操作が開始されます。</span><span class="sxs-lookup"><span data-stu-id="04710-119">This will start a servicing operation that takes your environment out of maintenance mode.</span></span> <span data-ttu-id="04710-120">環境の詳細ページで、工程の進捗状況を確認できます。</span><span class="sxs-lookup"><span data-stu-id="04710-120">You can see the progress of the operation in the environment details page.</span></span>
7. <span data-ttu-id="04710-121">これが完了すると、環境が **配置中** 状態に戻ります。</span><span class="sxs-lookup"><span data-stu-id="04710-121">After this is complete, your environment goes back to the **Deployed** state.</span></span> <span data-ttu-id="04710-122">すべてのユーザーが環境にログオンできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="04710-122">Now all users can sign in to the environment.</span></span>
8. <span data-ttu-id="04710-123">メンテナンス モードが有効または無効かを環境の履歴ページで確認することができます。</span><span class="sxs-lookup"><span data-stu-id="04710-123">You can check the environment history page to see when the maintenance mode was turned on or turned off.</span></span> <span data-ttu-id="04710-124">環境履歴ページに移動するには環境の詳細ページで **履歴** および **環境の変更** を選択します。</span><span class="sxs-lookup"><span data-stu-id="04710-124">To get to the environment history page, select **History** and **Environment changes** on the environment details page.</span></span>

<span data-ttu-id="04710-125">サンドボックスおよび運用環境のメンテナンス モードをオン/オフにする操作と、サービス操作にとても似ています。</span><span class="sxs-lookup"><span data-stu-id="04710-125">Turning maintenance mode on and off for your sandbox and production environment is very similar to a servicing operation.</span></span> <span data-ttu-id="04710-126">メンテナンス モードのオンまたはオフに失敗した場合は、**再開**、**ロールバック**、および **中止** などのオプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="04710-126">If turning maintenance mode on or off fails, you will see options such as **Resume**, **Rollback**, and **Abort**.</span></span> <span data-ttu-id="04710-127">操作に失敗した理由をトラブルシューティングするために**ログをダウンロード**するオプションもあります。</span><span class="sxs-lookup"><span data-stu-id="04710-127">You also have the option to **download the logs** to troubleshoot why the operation failed.</span></span>

## <a name="turn-maintenance-mode-on-and-off-in-devtestdemo-environments-hosted-in-a-microsoft-subscription"></a><span data-ttu-id="04710-128">Microsoft サブスクリプションで動作している開発テスト環境またはデモ環境にてメンテナンス モードをオンにする/オフにする。</span><span class="sxs-lookup"><span data-stu-id="04710-128">Turn maintenance mode on and off in DevTest/Demo environments hosted in a Microsoft subscription</span></span>
1. <span data-ttu-id="04710-129">開発者のマシンに RDP の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="04710-129">Establish an RDP connection to the developer machine.</span></span>
2. <span data-ttu-id="04710-130">開発者のマシンで、LCS から axdbadmin ユーザーの資格情報を使用して SQL Server にサインインします。</span><span class="sxs-lookup"><span data-stu-id="04710-130">On the developer machine, sign in to SQL Server by using the credentials for the axdbadmin user from LCS.</span></span> <span data-ttu-id="04710-131">次に、AXDB データベースに切り替えて、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="04710-131">Then switch to the AXDB database, and run the following command.</span></span>

    ```Console
    update SQLSYSTEMVARIABLES SET VALUE = 1 where PARM = 'CONFIGURATIONMODE'
    ```

3. <span data-ttu-id="04710-132">**World Wide Web 公開サービス** を再起動して IIS をリセットします。</span><span class="sxs-lookup"><span data-stu-id="04710-132">Restart the **World Wide Web Publishing Service** to reset IIS.</span></span>
4. <span data-ttu-id="04710-133">サービスが再起動されると、システムはメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="04710-133">After the service is restarted, the system will be in maintenance mode.</span></span>
5. <span data-ttu-id="04710-134">メンテナンス モードの活動を完了したら、ステップ 2 および 3 を繰り返しますが、値はステップ 2 で 0 に設定します。</span><span class="sxs-lookup"><span data-stu-id="04710-134">When you've completed your maintenance mode activities, repeat steps 2 and 3, but set the value to 0 in step 2.</span></span>

## <a name="turn-maintenance-mode-on-and-off-in-devtestdemo-environments-and-vhd-based-environments-hosted-in-customers-subscription"></a><span data-ttu-id="04710-135">サブスクリプションで動作しているVHDベースの環境あるいは、開発テスト環境またはデモ環境にて、メンテナンス モードをオンにする/オフにする。</span><span class="sxs-lookup"><span data-stu-id="04710-135">Turn maintenance mode on and off in DevTest/Demo environments and VHD-based environments hosted in customers' subscription</span></span>

<span data-ttu-id="04710-136">次のコマンドを実行して、メンテナンス モードをローカルでオンにすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-136">You can turn on maintenance mode locally by running the following command.</span></span> 

> [!Note]
> <span data-ttu-id="04710-137">一部の仮想マシン (VM) では、Deployment.Setup.exe ツールの正確な場所が異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="04710-137">On some virtual machines (VMs), the exact location of the Deployment.Setup.exe tool might differ.</span></span> <span data-ttu-id="04710-138">AosServiceWebRootbin を確認してください。</span><span class="sxs-lookup"><span data-stu-id="04710-138">Check AosServiceWebRootbin.</span></span>
>
>
>    ```Console
>    J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir 
>    J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode true
>    ```

<span data-ttu-id="04710-139">次のテーブルに、このコマンドで使用されるパラメーターを示します。</span><span class="sxs-lookup"><span data-stu-id="04710-139">The following table describes the parameters that are used in this command.</span></span>

| <span data-ttu-id="04710-140">パラメーター名</span><span class="sxs-lookup"><span data-stu-id="04710-140">Parameter name</span></span>              | <span data-ttu-id="04710-141">説明</span><span class="sxs-lookup"><span data-stu-id="04710-141">Description</span></span>  |
|-----------------------------|------|
| <span data-ttu-id="04710-142">--setupmode maintenancemode</span><span class="sxs-lookup"><span data-stu-id="04710-142">--setupmode maintenancemode</span></span> | <span data-ttu-id="04710-143">システムをメンテナンス モードにするかメンテナンス モードを解除するかをセットアップ ツールに通知するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-143">Use this parameter to inform the setup tool that the system will be put into or taken out of maintenance mode.</span></span>    |
| <span data-ttu-id="04710-144">--metadatadir</span><span class="sxs-lookup"><span data-stu-id="04710-144">--metadatadir</span></span>               | <span data-ttu-id="04710-145">メタデータ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-145">Use this parameter to specify the metadata directory.</span></span> <span data-ttu-id="04710-146">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04710-146">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="04710-147">--bindir</span><span class="sxs-lookup"><span data-stu-id="04710-147">--bindir</span></span>                    | <span data-ttu-id="04710-148">バイナリ ディレクトリ を指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-148">Use this parameter to specify the binaries directory.</span></span> <span data-ttu-id="04710-149">既定のパッケージ ディレクトリを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04710-149">You should use the default packages directory.</span></span>              |
| <span data-ttu-id="04710-150">--sqlserver</span><span class="sxs-lookup"><span data-stu-id="04710-150">--sqlserver</span></span>                 | <span data-ttu-id="04710-151">このパラメーターを使用して Microsoft SQL Server を指定します。</span><span class="sxs-lookup"><span data-stu-id="04710-151">Use this parameter to specify the Microsoft SQL Server.</span></span> <span data-ttu-id="04710-152">1 ボックス環境では、ピリオド (**.**) を使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-152">For one-box environments, use a period (**.**).</span></span>           |
| <span data-ttu-id="04710-153">--sqluser</span><span class="sxs-lookup"><span data-stu-id="04710-153">--sqluser</span></span>                   | <span data-ttu-id="04710-154">SQL Server のユーザーを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-154">Use this parameter to specify the SQL Server user.</span></span> <span data-ttu-id="04710-155">**AOSUser** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04710-155">You should use **AOSUser**.</span></span>                                    |
| <span data-ttu-id="04710-156">--sqlpwd</span><span class="sxs-lookup"><span data-stu-id="04710-156">--sqlpwd</span></span>                    | <span data-ttu-id="04710-157">SQL Server のパスワードを指定するには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-157">Use this parameter to specify the SQL Server password.</span></span>                                                            |
| <span data-ttu-id="04710-158">--isinmaintenancemode</span><span class="sxs-lookup"><span data-stu-id="04710-158">--isinmaintenancemode</span></span>       | <span data-ttu-id="04710-159">構成モードを有効または無効にするには、このパラメーターを使用します。</span><span class="sxs-lookup"><span data-stu-id="04710-159">Use this parameter to turn configuration mode on or off.</span></span> <span data-ttu-id="04710-160">オンにするには **true** とし、オフにするには **false** にします。</span><span class="sxs-lookup"><span data-stu-id="04710-160">Use **true** to turn it on and **false** to turn it off.</span></span> |

## <a name="enable-or-disable-configuration-keys"></a><span data-ttu-id="04710-161">コンフィギュレーション キーの有効化 (または無効化)</span><span class="sxs-lookup"><span data-stu-id="04710-161">Enable (or disable) configuration keys</span></span>

<span data-ttu-id="04710-162">Application Object Server (AOS) のインスタンスを再起動すると、システムはメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="04710-162">After the instance of Application Object Server (AOS) is restarted, the system will be in maintenance mode.</span></span> <span data-ttu-id="04710-163">次のスクリーンショットに示すように、構成キーを有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-163">You can then enable configuration keys, as shown in the following screenshot.</span></span> 

<span data-ttu-id="04710-164">[![メンテナンス モード以外のライセンス コンフィギュレーション ページ](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span><span class="sxs-lookup"><span data-stu-id="04710-164">[![License configuration page when not in maintenance mode](./media/license-configuration-page-when-not-in-maintenance-mode.png)](./media/license-configuration-page-when-not-in-maintenance-mode.png)</span></span> 

<span data-ttu-id="04710-165">メンテナンス モードになっている際にシステムへアクセスしようとすると、システム管理者または**メンテナンス モード ユーザー** ロールを持つユーザーではない人が、Finance and Operations にアクセスしようとすると、エラー メッセージが表示されることがあります。</span><span class="sxs-lookup"><span data-stu-id="04710-165">If you try to access the system while in maintenance mode, but you aren't a system administrator or a user who has the **Maintenance mode user** role, you may receive an error message.</span></span> 

<span data-ttu-id="04710-166">次のコマンドを実行して、メンテナンス モードをオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="04710-166">You can turn off maintenance mode by running the following command.</span></span>

```Console
J:\AosService\PackagesLocalDirectory\Bin\Microsoft.Dynamics.AX.Deployment.Setup.exe --metadatadir J:\AosService\PackagesLocalDirectory --bindir J:\AosService\PackagesLocalDirectory\Bin --sqlserver . --sqldatabase axdb --sqluser axdbadmin --sqlpwd ********* --setupmode maintenancemode --isinmaintenancemode false
```

