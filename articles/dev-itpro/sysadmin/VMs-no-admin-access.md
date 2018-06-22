---
title: "管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問"
description: "このトピックでは、管理者アクセスを許可しない仮想マシンに関するよくある質問 (FAQ) への回答を示します。"
author: yukonpeegs
manager: AnnBe
ms.date: 03/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform
ms.custom: 
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2017-11-30
ms.dyn365.ops.version: Platform update 12
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 8124081c061b11fe391811be1979567cf2012206
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="virtual-machines-that-dont-allow-administrator-access-faq"></a><span data-ttu-id="d283e-103">管理者のアクセスを許可しない仮想マシンに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="d283e-103">Virtual machines that don't allow administrator access FAQ</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="d283e-104">このトピックでは、管理者アクセスを許可しない仮想マシン (VM) に関するよくある質問 (FAQ) への回答を示します。</span><span class="sxs-lookup"><span data-stu-id="d283e-104">This topic provides answers to frequently asked questions (FAQ) about virtual machines (VMs) that don't allow administrator access.</span></span> <span data-ttu-id="d283e-105">具体的には、このトピックの情報は、Platform update 12 以降を実行する Tier 1 VM に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d283e-105">Specifically, the information in this topic applies to Tier 1 VMs that run Platform update 12 and later.</span></span>

## <a name="how-can-i-install-a-deployable-package"></a><span data-ttu-id="d283e-106">どのように配置可能パッケージをインストールできますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-106">How can I install a deployable package?</span></span>
<span data-ttu-id="d283e-107">可能な限り、Microsoft Dynamics Lifecyle Services (LCS) を使用して、配置可能なパッケージをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d283e-107">Whenever possible, use Microsoft Dynamics Lifecyle Services (LCS) to install a deployable package.</span></span> <span data-ttu-id="d283e-108">**-devinstall** オプションを使用して、展開可能なパッケージをインストールすることができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-108">You can install a deployable package by using the **-devinstall** option.</span></span> <span data-ttu-id="d283e-109">このオプションには手動データベース同期が必要な点に留意してください。</span><span class="sxs-lookup"><span data-stu-id="d283e-109">Remember that this option requires manual database synchronization.</span></span>

<span data-ttu-id="d283e-110">配置可能パッケージをインストールする方法の詳細については、[配置可能パッケージのインストール](../deployment/install-deployable-package.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d283e-110">For more information about how to install a deployable package, see [Install a deployable package](../deployment/install-deployable-package.md).</span></span>

## <a name="is-the-finance-and-operations-website-accessible-when-visual-studio-isnt-running"></a><span data-ttu-id="d283e-111">Visual Studio が実行されていないときに Finance and Operations の Web サイトはアクセス可能ですか。</span><span class="sxs-lookup"><span data-stu-id="d283e-111">Is the Finance and Operations website accessible when Visual Studio isn't running?</span></span>
<span data-ttu-id="d283e-112">はい、Microsoft Visual Studio が実行されていない場合、Microsoft Dynamics 365 for Finance and Operations Web サイトにアクセスすることができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-112">Yes, you can access the Microsoft Dynamics 365 for Finance and Operations website when Microsoft Visual Studio isn't running.</span></span> <span data-ttu-id="d283e-113">Microsoft Internet Information Services (IIS) Express は、ユーザーとして実行する .exe ファイルです。</span><span class="sxs-lookup"><span data-stu-id="d283e-113">Microsoft Internet Information Services (IIS) Express is an .exe file that runs as the user.</span></span> <span data-ttu-id="d283e-114">ただし、Visual Studio を終了すると、XPPC エージェントが終了する前に通常の IIS (IIS Express ではなく) が起動します。</span><span class="sxs-lookup"><span data-stu-id="d283e-114">However, when you close Visual Studio, the XPPC agent starts regular IIS (not IIS Express) before it closes.</span></span> <span data-ttu-id="d283e-115">この動作により、サインアウトした場合やマシンを再起動した場合でも、Application Object Server (AOS) インスタンスとFinance and Operations Web サイトにリモートでアクセスできるようになります。</span><span class="sxs-lookup"><span data-stu-id="d283e-115">This behavior helps guarantee that you can remotely access the Application Object Server (AOS) instance and the Finance and Operations website, even when you sign out or the machine is restarted.</span></span> <span data-ttu-id="d283e-116">多くのユーザーがこのような開発者用マシンをテスト用マシンとして使用してていること、また彼らが常に AOS インスタンスが実行されていることを期待していることを認識しています。</span><span class="sxs-lookup"><span data-stu-id="d283e-116">We recognize that many people use these developer machines as test machines, and that they expect the AOS instance always to be running.</span></span> <span data-ttu-id="d283e-117">ただし、IIS Express は、この動作をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="d283e-117">However, IIS Express doesn't support this behavior.</span></span>

## <a name="what-about-the-other-services"></a><span data-ttu-id="d283e-118">他のサービスはどうなのですか ?</span><span class="sxs-lookup"><span data-stu-id="d283e-118">What about the other services?</span></span>
<span data-ttu-id="d283e-119">Microsoft SQL Server、SQL Server Reporting Services (SSRS)、SQL Server Integration Services (SSIS)、SQL Server Analysis Services (SSAS)、Batch、Financial reporting (旧 Management Reporter)、および IIS などの Microsoft Windows サービスを再起動することができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-119">You can restart Microsoft Windows services such as Microsoft SQL Server, SQL Server Reporting Services (SSRS), SQL Server Integration Services (SSIS), SQL Server Analysis Services (SSAS), Batch, Financial reporting (formerly Management Reporter), and IIS.</span></span> <span data-ttu-id="d283e-120">(IIS の場合は、iisreset.exe を使用できないため、World Wide Web 発行サービスを再起動する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="d283e-120">(For IIS, you must restart the World Wide Web Publishing Service service because you can't use iisreset.exe.)</span></span>

## <a name="can-i-clean-up-the-service-volume-drive"></a><span data-ttu-id="d283e-121">サービス ボリューム ドライブをクリーンアップできますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-121">Can I clean up the service volume drive?</span></span>
<span data-ttu-id="d283e-122">はい、サービス ボリューム ドライブに対する完全なアクセス権があります。</span><span class="sxs-lookup"><span data-stu-id="d283e-122">Yes, you have full access to the service volume drive.</span></span> <span data-ttu-id="d283e-123">したがって、監視データをクリーンアップすることができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-123">Therefore, you can clean up the monitoring data, and so on.</span></span>

## <a name="what-are-the-alternatives-to-vms-that-dont-allow-administrator-access"></a><span data-ttu-id="d283e-124">管理者アクセスを許可しない VM に代わる方法とは</span><span class="sxs-lookup"><span data-stu-id="d283e-124">What are the alternatives to VMs that don't allow administrator access?</span></span>
<span data-ttu-id="d283e-125">プライベート Azure サブスクリプションの Microsoft Azure VM とローカル仮想ハード ディスク (VHD) の両方は管理者アクセスを許可します。</span><span class="sxs-lookup"><span data-stu-id="d283e-125">Both a Microsoft Azure VM on a private Azure subscription and a local virtual hard disk (VHD) allow administrator access.</span></span> <span data-ttu-id="d283e-126">ただし、Visual Studio を管理者として実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d283e-126">However, you must run Visual Studio as an administrator.</span></span> <span data-ttu-id="d283e-127">管理者は明示的にではなく、**管理者**グループを介してのみこれらの代替手段にアクセスできるため、この要件が適用されます。</span><span class="sxs-lookup"><span data-stu-id="d283e-127">This requirement applies because the administrator has access to these alternatives only through the **administrator** group, not explicitly.</span></span>

## <a name="can-i-run-visual-studio-as-an-administrator"></a><span data-ttu-id="d283e-128">Visual Studio を管理者として実行できますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-128">Can I run Visual Studio as an administrator?</span></span>
<span data-ttu-id="d283e-129">Platform update 12 以降、Visual Studio を管理者として実行する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d283e-129">Starting with Platform update 12, you're no longer required to run Visual Studio as an administrator.</span></span> <span data-ttu-id="d283e-130">Microsoft 所有の Azure サブスクリプションである VM に対して、リモート デスクトップ プロトコル (RDP) を使用して管理者として接続することはできなくなりました。</span><span class="sxs-lookup"><span data-stu-id="d283e-130">You can no longer use the Remote Desktop Protocol (RDP) to connect as an administrator to VMs that are under a Microsoft-owned Azure subscription.</span></span> <span data-ttu-id="d283e-131">これらの VM には、サブスクリプションおよび Tier 1 アドオン VM に含まれる Tier 1 VM が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d283e-131">These VMs include the Tier 1 VM that is included in the subscription and Tier 1 add-on VMs.</span></span> <span data-ttu-id="d283e-132">ただし、管理者として Microsoft 所有のサブスクリプションの下にはない VM に接続する場合、管理者として引き続き Visual Studio を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d283e-132">However, if you're connecting as an administrator to a VM that isn't under a Microsoft-owned subscription, you must still run Visual Studio as an administrator.</span></span>

## <a name="a-get-latest-operation-in-visual-studio-failed-because-files-are-blocked-by-the-aos-instance-how-do-i-start-and-stop-iis"></a><span data-ttu-id="d283e-133">ファイルが AOS インスタンスによってブロックされているため、Visual Studio での「最新の取得」操作が失敗しました。</span><span class="sxs-lookup"><span data-stu-id="d283e-133">A "get latest" operation in Visual Studio failed because files are blocked by the AOS instance.</span></span> <span data-ttu-id="d283e-134">IIS を開始または停止するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="d283e-134">How do I start and stop IIS?</span></span>
<span data-ttu-id="d283e-135">IIS Express を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d283e-135">You must use IIS Express.</span></span> <span data-ttu-id="d283e-136">詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d283e-136">See the next question for more information.</span></span>

## <a name="what-are-the-instructions-for-using-iis-express"></a><span data-ttu-id="d283e-137">IIS Express の使用方法は ?</span><span class="sxs-lookup"><span data-stu-id="d283e-137">What are the instructions for using IIS Express?</span></span>
<span data-ttu-id="d283e-138">IIS Express が起動されると、通知領域 (時計の近くにある) にアイコンが表示されます。</span><span class="sxs-lookup"><span data-stu-id="d283e-138">When IIS Express is started, an icon appears in the notification area (near the clock).</span></span> <span data-ttu-id="d283e-139">IIS Express アイコンを右クリックすると、実行中のすべてのサイトが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="d283e-139">When you right-click on the IIS Express icon, all the running sites are listed.</span></span> <span data-ttu-id="d283e-140">そのメニューから IIS Express を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-140">You can stop IIS Express from that menu.</span></span> <span data-ttu-id="d283e-141">Visual Studio でのいくつかのアクションによって IIS Express が起動しますが、**Dynamics 365** メニューで **IIS Express の再起動** を選択することで、Visual Studio から明示的に IIS Express を起動することもできます。</span><span class="sxs-lookup"><span data-stu-id="d283e-141">Some actions in Visual Studio cause IIS Express to be started, but you can also explicitly start IIS Express from Visual Studio by selecting **Restart IIS Express** on the **Dynamics 365** menu.</span></span>

## <a name="how-can-i-apply-a-partner-visual-studio-license-that-isnt-linked-to-the-visual-studio-sign-in-account-that-is-likely-to-be-used-in-the-customer-azure-ad-or-domain"></a><span data-ttu-id="d283e-142">顧客の Azure AD またはドメインで使用される可能性のある、Visual Studio サインイン アカウントにリンクされていない、パートナーの Visual Studio ライセンスはどのように適用できますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-142">How can I apply a partner Visual Studio license that isn't linked to the Visual Studio sign-in account that is likely to be used in the customer Azure AD or domain?</span></span>
<span data-ttu-id="d283e-143">この機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d283e-143">This functionality isn't supported.</span></span> <span data-ttu-id="d283e-144">パートナーの Visual Studio ライセンスは、顧客の Azure Active Directory (Azure AD) またはドメインで使用されている Visual Studio サインイン アカウントにリンクされない限り、適用することはできません。</span><span class="sxs-lookup"><span data-stu-id="d283e-144">You can't apply a partner Visual Studio license unless it's linked to the Visual Studio sign-in account that is used in the customer Azure Active Directory (Azure AD) or domain.</span></span>

## <a name="can-i-install-additional-development-tools-such-as-fiddler-and-pepper"></a><span data-ttu-id="d283e-145">追加の開発ツール (Fiddler や Pepper など) をインストールすることはできますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-145">Can I install additional development tools (such as Fiddler and Pepper)?</span></span>
<span data-ttu-id="d283e-146">いいえ、追加の開発ツールをインストールすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d283e-146">No, you can't install additional development tools.</span></span>

## <a name="is-there-a-way-to-run-windows-powershell-and-command-prompt-commands-as-an-administrator"></a><span data-ttu-id="d283e-147">管理者として Windows PowerShell およびコマンド プロンプトのコマンドを実行する方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-147">Is there a way to run Windows PowerShell and command prompt commands as an administrator?</span></span>
<span data-ttu-id="d283e-148">いいえ、管理者として Windows PowerShell コマンドおよびコマンド プロンプトのコマンドを実行できません。</span><span class="sxs-lookup"><span data-stu-id="d283e-148">No, you can't run Windows PowerShell commands and commands at a prompt command as an administrator.</span></span>

## <a name="is-the-trace-parser-supported"></a><span data-ttu-id="d283e-149">Trace Parser はサポートされていますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-149">Is the Trace Parser supported?</span></span>
<span data-ttu-id="d283e-150">Trace Parser は現在サポートされていませんが、間もなく再度そのサポートを追加する予定です。</span><span class="sxs-lookup"><span data-stu-id="d283e-150">Although the Trace Parser isn't currently supported, we plan to add support for it again soon.</span></span>

## <a name="can-the-system-be-put-into-maintenance-mode"></a><span data-ttu-id="d283e-151">システムをメンテナンス モードにすることはできますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-151">Can the system be put into maintenance mode?</span></span>
<span data-ttu-id="d283e-152">システムをメンテナンス モードにしてライセンス コンフィギュレーションを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-152">You can put the system into maintenance mode to change the license configuration.</span></span> <span data-ttu-id="d283e-153">ただし、[メンテナンス モード](maintenance-mode.md) に記載されている手順はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d283e-153">However, the procedure that is described in [Maintenance mode](maintenance-mode.md) isn't supported.</span></span> <span data-ttu-id="d283e-154">すべての環境におけるメンテナンス モードのセルフ サービス サポートが将来 LCS に追加されます。</span><span class="sxs-lookup"><span data-stu-id="d283e-154">Self-service support for maintenance mode in all environments will be added to LCS in the future.</span></span> <span data-ttu-id="d283e-155">このサポートが LCS で利用可能になるまで、以下の手順に従ってシステムをメンテナンス モードにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d283e-155">Until this support is available in LCS, you can follow these steps to put a system into maintenance mode.</span></span>

1. <span data-ttu-id="d283e-156">開発者のマシンに RDP の接続を確立します。</span><span class="sxs-lookup"><span data-stu-id="d283e-156">Establish an RDP connection to the developer machine.</span></span>
2. <span data-ttu-id="d283e-157">開発者のマシンで、LCS から axdbadmin ユーザーの資格情報を使用して SQL Server にサインインします。</span><span class="sxs-lookup"><span data-stu-id="d283e-157">On the developer machine, sign in to SQL Server by using the credentials for the axdbadmin user from LCS.</span></span> <span data-ttu-id="d283e-158">次に、AXDB データベースに切り替えて、次のコマンドを実行します。</span><span class="sxs-lookup"><span data-stu-id="d283e-158">Then switch to the AXDB database, and run the following command.</span></span>

    ```
    update SQLSYSTEMVARIABLES SET VALUE = 1 where PARM = 'CONFIGURATIONMODE'
    ```

3. <span data-ttu-id="d283e-159">**World Wide Web 公開サービス** サービスを再起動して IIS をリセットします。</span><span class="sxs-lookup"><span data-stu-id="d283e-159">Restart the **World Wide Web Publishing Service** service to reset IIS.</span></span>

    <span data-ttu-id="d283e-160">サービスが再起動されると、システムはメンテナンス モードになります。</span><span class="sxs-lookup"><span data-stu-id="d283e-160">After the service is restarted, the system will be in maintenance mode.</span></span>

4. <span data-ttu-id="d283e-161">メンテナンス モードの活動を完了したら、ステップ 2 および 3 を繰り返しますが、値はステップ 2 で **0** に設定します。</span><span class="sxs-lookup"><span data-stu-id="d283e-161">When you've completed your maintenance mode activities, repeat steps 2 and 3, but set the value to **0** in step 2.</span></span>

## <a name="can-i-install-a-license-deployable-package"></a><span data-ttu-id="d283e-162">ライセンス配置可能パッケージをインストールできますか。</span><span class="sxs-lookup"><span data-stu-id="d283e-162">Can I install a license deployable package?</span></span>
<span data-ttu-id="d283e-163">**- devinstall** オプションを使用して、ライセンスが配置可能なパッケージをインストールできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="d283e-163">You should be able to use the **-devinstall** option to install license deployable packages.</span></span> <span data-ttu-id="d283e-164">ただし、このシナリオで問題が検出されました。</span><span class="sxs-lookup"><span data-stu-id="d283e-164">However, an issue was found with this scenario.</span></span> <span data-ttu-id="d283e-165">問題の解決に取り組んでいます。</span><span class="sxs-lookup"><span data-stu-id="d283e-165">We are working to resolve the issue.</span></span>
