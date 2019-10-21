---
title: Azure 上での AX 2012 R3 配置のトラブルシューティング
description: このトピックでは、一般的な問題を解決するための方法、および Azure で Microsoft Dynamics AX 2012 R3 環境の支援を受ける方法について説明します。
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18691
ms.assetid: cc7c6dd5-b715-4734-9918-c25df4187c6e
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: b014e4d9f1036bf393a1dae0115fbabf370d8a77
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183228"
---
# <a name="troubleshoot-ax-2012-r3-deployments-on-azure"></a><span data-ttu-id="6b428-103">Azure 上での AX 2012 R3 配置のトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="6b428-103">Troubleshoot AX 2012 R3 deployments on Azure</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b428-104">このトピックでは、一般的な問題を解決するための方法、および Azure で Microsoft Dynamics AX 2012 R3 環境の支援を受ける方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="6b428-104">This topic explains how to resolve common issues and how to get assistance with your Microsoft Dynamics AX 2012 R3 environment on Azure.</span></span>

<a name="how-do-i-renew-the-windows-license-on-a-demo-virtual-machine"></a><span data-ttu-id="6b428-105">デモ仮想マシンで Windows ライセンスを更新するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="6b428-105">How do I renew the Windows license on a demo virtual machine?</span></span>
-------------------------------------------------------------

<span data-ttu-id="6b428-106">Windows のデモ環境で仮想マシンに試用版のライセンスを更新する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b428-106">If you need to renew the trial license for Windows on the virtual machine in a demo environment, complete the following steps.</span></span>

1.  <span data-ttu-id="6b428-107">**クラウド ホスト環境**ページで、デモ環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b428-107">On the **Cloud-hosted environments** page, select the demo environment.</span></span>
2.  <span data-ttu-id="6b428-108">環境に関する詳細を表示するためにページの右側にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="6b428-108">Scroll to the right side of the page to view details about the environment.</span></span>
3.  <span data-ttu-id="6b428-109">**DEMO-&lt;GUID&gt;** リンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b428-109">Click the **DEMO-&lt;GUID&gt;** link.</span></span>
4.  <span data-ttu-id="6b428-110">ページの下部にある**開く**をクリックして、.rdp ファイルを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b428-110">At the bottom of the page, click **Open** to open the .rdp file.</span></span>
5.  <span data-ttu-id="6b428-111">資格情報を求めるメッセージが表示されたら、 この環境の **クラウドによってホストされた環境** ページにある、適切なユーザー名とパスワードを入力します。</span><span class="sxs-lookup"><span data-stu-id="6b428-111">When prompted for credentials, enter the user name and password found on the **Cloud-hosted environments** page for this environment.</span></span>
6.  <span data-ttu-id="6b428-112">仮想マシンのデスクトップが表示されたとき、c:\\DemoFiles\\StartupScripts の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="6b428-112">When the virtual machine’s desktop is displayed, go to the following location: C:\\DemoFiles\\StartupScripts</span></span>
7.  <span data-ttu-id="6b428-113">**rearm.cmd** を右クリックして**管理者として実行** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b428-113">Right-click **rearm.cmd**, and then click **Run as administrator**.</span></span>

<span data-ttu-id="6b428-114">コマンド プロンプト ウィンドウが短く表示され、仮想マシンが再起動します。</span><span class="sxs-lookup"><span data-stu-id="6b428-114">A command prompt window will be displayed briefly, and then the virtual machine will restart.</span></span> <span data-ttu-id="6b428-115">ライセンスは現在 180 日間有効です。</span><span class="sxs-lookup"><span data-stu-id="6b428-115">The license is now good for 180 days.</span></span> <span data-ttu-id="6b428-116">この手順は 3 回完了することができます。</span><span class="sxs-lookup"><span data-stu-id="6b428-116">You can complete this procedure 3 times.</span></span>

## <a name="how-do-i-renew-the-microsoft-dynamics-ax-license-on-a-demo-virtual-machine"></a><span data-ttu-id="6b428-117">デモ仮想マシンで Microsoft Dynamics AX ライセンスを更新するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="6b428-117">How do I renew the Microsoft Dynamics AX license on a demo virtual machine?</span></span>
<span data-ttu-id="6b428-118">Microsoft Dynamics AX のデモ環境で仮想マシンのライセンスを更新する必要がある場合、[CustomerSource](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/service-packs/AX2012DemoToolsMaterials#DemoVirtualMachineLicenses) または [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898) から試用版のライセンス ファイルをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="6b428-118">If you need to renew the license for Microsoft Dynamics AX on the virtual machine in a demo environment, please download the trial license files from [CustomerSource](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/service-packs/AX2012DemoToolsMaterials#DemoVirtualMachineLicenses) or [MSDN](https://msdn.microsoft.com/subscriptions/securedownloads/hh442898).</span></span> <span data-ttu-id="6b428-119">「[ライセンス情報の指定](https://technet.microsoft.com/library/aa496447.aspx)」に記載の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="6b428-119">Then, follow the steps listed in [Provide license information](https://technet.microsoft.com/library/aa496447.aspx).</span></span>

## <a name="how-do-i-activate-windows-on-the-virtual-machines-in-my-non-demo-environment"></a><span data-ttu-id="6b428-120">非デモ環境で仮想マシンの Windows をアクティブにするにはどうしたらいいですか。</span><span class="sxs-lookup"><span data-stu-id="6b428-120">How do I activate Windows on the virtual machines in my non-demo environment?</span></span>
<span data-ttu-id="6b428-121">Windows は非デモ環境に含まれている仮想マシン上で自動的に有効化されます。</span><span class="sxs-lookup"><span data-stu-id="6b428-121">Windows is automatically activated on the virtual machines that are included with non-demo environments.</span></span> <span data-ttu-id="6b428-122">ただし、有効化には完了までに 4 日間かかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b428-122">However, the activation may take up to 4 days to complete.</span></span> <span data-ttu-id="6b428-123">4 日間後に Windows を有効化するように求めるメッセージが続けて表示される場合は、Azure サポート チームに問い合わせます。</span><span class="sxs-lookup"><span data-stu-id="6b428-123">If you continue to see messages that prompt you to activate Windows after 4 days, contact the Azure support team.</span></span> <span data-ttu-id="6b428-124">Azure サポート チームに連絡する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b428-124">For information on how to contact the Azure support team, see the following section.</span></span>

## <a name="how-do-i-resolve-the-following-error-scriptid-installdatabase-failed-execution-on-vm-instance"></a><span data-ttu-id="6b428-125">次のエラーを解決するには: VMインスタンスで ScriptId 「InstallDatabase」 実行の失敗</span><span class="sxs-lookup"><span data-stu-id="6b428-125">How do I resolve the following error: ScriptId 'InstallDatabase' failed execution on VM instance</span></span>
<span data-ttu-id="6b428-126">SQL Server AlwaysOn クラスターをインストールすると、プライマリ SQL Server インスタンスがセカンダリ インスタンスにフェール オーバーする場合、そのインストールは上記のエラーで失敗します。</span><span class="sxs-lookup"><span data-stu-id="6b428-126">When installing a SQL Server AlwaysOn cluster, if the primary SQL Server instance fails over to the secondary instance, then the installation will fail with the above error.</span></span> <span data-ttu-id="6b428-127">仮想マシンがオンラインになると、すぐに失敗することは異常です。</span><span class="sxs-lookup"><span data-stu-id="6b428-127">It is unusual for a virtual machine that has just been brought online to fail immediately.</span></span> <span data-ttu-id="6b428-128">配置されているトポロジを削除し、再配置することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="6b428-128">We recommend that you delete the deployed topology and redeploy.</span></span>

## <a name="how-do-i-resolve-the-following-error-script-createazurefailoverclusterhasql1-failed-execution"></a><span data-ttu-id="6b428-129">次のエラーを解決するには: スクリプト 「CreateAzureFailoverCluster:HASQL1」 実行の失敗</span><span class="sxs-lookup"><span data-stu-id="6b428-129">How do I resolve the following error: Script 'CreateAzureFailoverCluster:HASQL1' failed execution</span></span>
<span data-ttu-id="6b428-130">既存のネットワークと Active Directory に展開した場合 (トポロジー内の VM の名前もカスタマイズしている場合)、Azure の DNS サーバーを変更せずに同じ名前のカスタマイズを再展開することはできません。</span><span class="sxs-lookup"><span data-stu-id="6b428-130">If you have deployed to an existing network and Active Directory—while also customizing the names of the VMs in the topology—you cannot redeploy that same name customization without altering the DNS server in Azure.</span></span> <span data-ttu-id="6b428-131">このシナリオでは、DNS サーバーに同じ名前を持つ前の VM の IP アドレスがあり、その結果、配置に失敗します。</span><span class="sxs-lookup"><span data-stu-id="6b428-131">In this scenario, the DNS server will have the IP addresses of the previous VMs with the same names, and as a result, the deployment will fail.</span></span> <span data-ttu-id="6b428-132">この問題を解決するには、再配置する前にそれらの VM の DNS サーバー エントリを削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b428-132">To resolve this issue, you must delete the DNS server entries for those VMs before redeploying.</span></span>

## <a name="the-dynamics-ax-client-crashes-on-first-use--how-do-i-resolve-this"></a><span data-ttu-id="6b428-133">Dynamics AX クライアントは、初回の使用時にクラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6b428-133">The Dynamics AX client crashes on first use.</span></span>  <span data-ttu-id="6b428-134">これをどのように解決しますか。</span><span class="sxs-lookup"><span data-stu-id="6b428-134">How do I resolve this?</span></span>
<span data-ttu-id="6b428-135">Dynamics AX クライアントは、再起動後または最初のログイン後にクラッシュする可能性があります。</span><span class="sxs-lookup"><span data-stu-id="6b428-135">Dynamics AX clients may crash upon first login after a restart or after a period of inactivity.</span></span> <span data-ttu-id="6b428-136">これは、カーネル 6.3.3000.287 で修正された RemoteApp の問題が原因です。</span><span class="sxs-lookup"><span data-stu-id="6b428-136">This is due to a RemoteApp issue that has been fixed in kernel 6.3.3000.287.</span></span>  <span data-ttu-id="6b428-137">高可用性環境またはテスト環境を配置した場合、RemoteApp を使用している場合があります。</span><span class="sxs-lookup"><span data-stu-id="6b428-137">If you've deployed a high availability environment or a test environment, you may be using RemoteApp.</span></span> <span data-ttu-id="6b428-138">この問題を解決するには、次のいずれかの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="6b428-138">To resolve this issue, complete one of the following procedures:</span></span>

### <a name="disable-the-status-bar"></a><span data-ttu-id="6b428-139">ステータス バーを無効にする</span><span class="sxs-lookup"><span data-stu-id="6b428-139">Disable the status bar</span></span>

1.  <span data-ttu-id="6b428-140">Dynamics AX クライアントで、**オプション** フォーム (**ファイル** &gt; **ツール** &gt; **オプション**) を開きます。</span><span class="sxs-lookup"><span data-stu-id="6b428-140">In the Dynamics AX client, open the **Options** form (**File** &gt; **Tools** &gt; **Options**)</span></span>
2.  <span data-ttu-id="6b428-141">**ステータス バー** オプションをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6b428-141">Click the **Status bar** option.</span></span>
3.  <span data-ttu-id="6b428-142">**ステータス バーの表示** フィールドで**なし**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6b428-142">In the **Show status bar** field, select **None**.</span></span>

### <a name="install-kernel-633000287-or-later"></a><span data-ttu-id="6b428-143">カーネル 6.3.3000.287 以降のインストール</span><span class="sxs-lookup"><span data-stu-id="6b428-143">Install kernel 6.3.3000.287 or later</span></span>

<span data-ttu-id="6b428-144">カーネルは累積型であるため、最新のカーネルはこちらを参照してください。<https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/></span><span class="sxs-lookup"><span data-stu-id="6b428-144">Kernels are cumulative and the most recent kernel can be found here: <https://blogs.msdn.microsoft.com/axsupport/2012/03/29/overview-of-microsoft-dynamics-ax-build-numbers/></span></span>

## <a name="how-do-i-monitor-for-storage-account-throttling"></a><span data-ttu-id="6b428-145">ストレージ アカウントのスロットルを監視するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="6b428-145">How do I monitor for storage account throttling?</span></span>
<span data-ttu-id="6b428-146">ストレージ アカウントのスロットルを監視するには、[[ストレージ アカウントのスロットルを監視する方法](https://blogs.msdn.microsoft.com/mast/2014/08/02/how-to-monitor-for-storage-account-throttling/)] を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b428-146">To monitor storage account throttling, see [How to Monitor for Storage Account Throttling](https://blogs.msdn.microsoft.com/mast/2014/08/02/how-to-monitor-for-storage-account-throttling/).</span></span> <span data-ttu-id="6b428-147">ストレージが制限されているときに通知するには、警告および通知を利用できます。</span><span class="sxs-lookup"><span data-stu-id="6b428-147">Alerts and notifications can be utilized to notify you when storage is being throttled.</span></span> <span data-ttu-id="6b428-148">これが発生している場合、複数の Azure コネクタや LCS プロジェクトの活用に関する情報については、[Azure で Microsoft Dynamics AX 2012 R3 の展開を計画](plan-2012-r3-deployment-azure.md) というトピックを参照します。</span><span class="sxs-lookup"><span data-stu-id="6b428-148">If this is happening, see the [Plan your Microsoft Dynamics AX 2012 R3 deployment on Azure](plan-2012-r3-deployment-azure.md) topic for information about leveraging multiple Azure Connectors and/or LCS projects.</span></span>

## <a name="how-do-i-contact-support"></a><span data-ttu-id="6b428-149">サポートに連絡するにはどうすればよいですか。</span><span class="sxs-lookup"><span data-stu-id="6b428-149">How do I contact Support?</span></span>
<span data-ttu-id="6b428-150">ライセンスまたは技術的な質問で Microsoft に連絡する必要がある場合は、最初にどのサポート チームに連絡するかを決める必要があります。</span><span class="sxs-lookup"><span data-stu-id="6b428-150">If you need to contact Microsoft with licensing or technical questions, you must first determine which support team to contact.</span></span> <span data-ttu-id="6b428-151">以下の情報を参考にして、最良の担当サポート チームを見つけてください。</span><span class="sxs-lookup"><span data-stu-id="6b428-151">Use the information below to best identify which support team to contact.</span></span>

### <a name="azure-support"></a><span data-ttu-id="6b428-152">Azure サポート</span><span class="sxs-lookup"><span data-stu-id="6b428-152">Azure support</span></span>

<span data-ttu-id="6b428-153">Azure のサポートを得るには、次の表に示すリソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b428-153">To obtain support for Azure, use the resources listed in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b428-154"><strong>タスク</strong></span><span class="sxs-lookup"><span data-stu-id="6b428-154"><strong>Task</strong></span></span></td>
<td><span data-ttu-id="6b428-155"><strong>詳細情報</strong></span><span class="sxs-lookup"><span data-stu-id="6b428-155"><strong>More information</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b428-156">請求書に関連する質問について援助を受けます</span><span class="sxs-lookup"><span data-stu-id="6b428-156">Get assistance with billing-related questions</span></span></td>
<td><span data-ttu-id="6b428-157">サンプル請求書、および現在の請求期間に対する毎日の使用データをダウンロードする方法に関する情報にリンクする Azure 請求プロセスの概要を確認するには、<a href="http://azure.microsoft.com/support/understand-your-bill/">請求書を理解する</a>ページに移動してください。</span><span class="sxs-lookup"><span data-stu-id="6b428-157">Go to the <a href="http://azure.microsoft.com/support/understand-your-bill/">Understand your bill</a> page to get an overview of the Azure billing process, links to sample invoices, and information about how to download daily usage data for the current billing period.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b428-158">コミュニティに質問する</span><span class="sxs-lookup"><span data-stu-id="6b428-158">Ask the community</span></span></td>
<td><span data-ttu-id="6b428-159"><a href="http://www.windowsazure.com/support/forums/">Azure フォーラム</a>ページに移動し、Azure コミュニティからの質問のヘルプを入手します。</span><span class="sxs-lookup"><span data-stu-id="6b428-159">Go to the <a href="http://www.windowsazure.com/support/forums/">Azure forums</a> page to get help with your questions from the Azure community.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b428-160">Azure サービス ダッシュ ボードの使用</span><span class="sxs-lookup"><span data-stu-id="6b428-160">Use the Azure services dashboard</span></span></td>
<td><span data-ttu-id="6b428-161"><a href="http://www.windowsazure.com/support/service-dashboard/">Azure サービス ダッシュ ボード</a>ページに移動して、Azure プラットフォームおよびサービスの現在のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6b428-161">Go to the <a href="http://www.windowsazure.com/support/service-dashboard/">Azure services dashboard</a> page to get the current status of the Azure platform and services.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b428-162">Azure サポート チームとのサポート チケットを入力します。</span><span class="sxs-lookup"><span data-stu-id="6b428-162">Enter a support ticket with the Azure support team</span></span></td>
<td><span data-ttu-id="6b428-163"><a href="http://www.windowsazure.com/support/options/">Azure サポート オプション</a>ページに移動し、サポートを受けるをクリックしてサポート チケットを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b428-163">Go to the <a href="http://www.windowsazure.com/support/options/">Azure support options</a> page, and click Get Support to open a support ticket.</span></span> <span data-ttu-id="6b428-164">Azure サポート チームは、以下に関連する問題の解決をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6b428-164">The Azure support team can help you resolve issues related to:</span></span>
<ul>
<li><span data-ttu-id="6b428-165">Azure サブスクリプションのサイズを大きくする要求</span><span class="sxs-lookup"><span data-stu-id="6b428-165">Requests to increase the size of your Azure subscription</span></span></li>
<li><span data-ttu-id="6b428-166">Azure 管理ポータルの使用時のエラー</span><span class="sxs-lookup"><span data-stu-id="6b428-166">Errors when using the Azure management portal</span></span></li>
<li><span data-ttu-id="6b428-167">仮想ネットワークを構成する際の問題</span><span class="sxs-lookup"><span data-stu-id="6b428-167">Issues when configuring a virtual network</span></span></li>
<li><span data-ttu-id="6b428-168">仮想ネットワーク ゲートウェイを構成する際の問題</span><span class="sxs-lookup"><span data-stu-id="6b428-168">Issues when configuring a virtual network gateway</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### 

### <a name="microsoft-dynamics-ax-support"></a><span data-ttu-id="6b428-169">Microsoft Dynamics AX のサポート</span><span class="sxs-lookup"><span data-stu-id="6b428-169">Microsoft Dynamics AX support</span></span>

<span data-ttu-id="6b428-170">Microsoft Dynamics AX のサポートを得るには、次の表に示すリソースを使用します。</span><span class="sxs-lookup"><span data-stu-id="6b428-170">To obtain support for Microsoft Dynamics AX, use the resources listed in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b428-171"><strong>タスク</strong></span><span class="sxs-lookup"><span data-stu-id="6b428-171"><strong>Task</strong></span></span></td>
<td><span data-ttu-id="6b428-172"><strong>詳細</strong></span><span class="sxs-lookup"><span data-stu-id="6b428-172"><strong>More information</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b428-173">Microsoft Dynamics AX のライセンスに関する質問について援助を受けます。</span><span class="sxs-lookup"><span data-stu-id="6b428-173">Get assistance with Microsoft Dynamics AX licensing questions</span></span></td>
<td><span data-ttu-id="6b428-174">次の PartnerSource のリンクをクリックして、Microsoft Dynamics Regional Operations Center にお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="6b428-174">Contact Microsoft Dynamics Regional Operations Centers by clicking the following PartnerSource links:</span></span>
<ul>
<li><span data-ttu-id="6b428-175"><a href="https://mbs.microsoft.com/partnersource/northamerica/pricing-ordering">価格決定と注文</a></span><span class="sxs-lookup"><span data-stu-id="6b428-175"><a href="https://mbs.microsoft.com/partnersource/northamerica/pricing-ordering">Pricing and ordering</a></span></span></li>
<li><span data-ttu-id="6b428-176"><a href="https://mbs.microsoft.com/partnersource/northamerica/help/help/GlobalOperationsSupportPage">工程のサポート</a></span><span class="sxs-lookup"><span data-stu-id="6b428-176"><a href="https://mbs.microsoft.com/partnersource/northamerica/help/help/GlobalOperationsSupportPage">Operations support</a></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b428-177">コミュニティに質問する</span><span class="sxs-lookup"><span data-stu-id="6b428-177">Ask the community</span></span></td>
<td><span data-ttu-id="6b428-178"><a href="http://go.microsoft.com/fwlink/?LinkId=221068">Microsoft Dynamics AX フォーラム</a>ページに移動し、Microsoft Dynamics AX コミュニティからの質問のヘルプを入手します。</span><span class="sxs-lookup"><span data-stu-id="6b428-178">Go to the <a href="http://go.microsoft.com/fwlink/?LinkId=221068">Microsoft Dynamics AX forum</a> page to get help with your questions from the Microsoft Dynamics AX community.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b428-179">クラウドを利用したサポート ツールの使用</span><span class="sxs-lookup"><span data-stu-id="6b428-179">Use the Cloud-powered support tool</span></span></td>
<td><span data-ttu-id="6b428-180"><a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a> で、クラウドを利用したサポートはサポート インシデントを管理するためのツールです。</span><span class="sxs-lookup"><span data-stu-id="6b428-180">In <a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a>, Cloud-powered support is a tool that helps you manage support incidents.</span></span> <span data-ttu-id="6b428-181">クラウドを利用したサポートにより、ローカル環境と同じ修正プログラムがインストールされた Azure に仮想マシンを作成できます。</span><span class="sxs-lookup"><span data-stu-id="6b428-181">Cloud-powered support lets you create a virtual machine in Azure that has the same hotfixes installed as your local environment.</span></span> <span data-ttu-id="6b428-182">仮想マシン上でインシデントを再生成して記録し、仮想マシンをサポート チームに送信することができます。</span><span class="sxs-lookup"><span data-stu-id="6b428-182">You can reproduce and record the incident on the virtual machine, and then submit the virtual machine to our support team.</span></span> <span data-ttu-id="6b428-183">サポート チームは、インシデントを調査し、仮想マシンの修正をテストすることによってフォローアップします。</span><span class="sxs-lookup"><span data-stu-id="6b428-183">The support team follows up by investigating the incident and testing a fix on the virtual machine.</span></span> <span data-ttu-id="6b428-184">修正プログラムが見つかった場合、仮想マシンと修正プログラムを確認のために送信します。</span><span class="sxs-lookup"><span data-stu-id="6b428-184">If a fix is found, they send the virtual machine and the fix back to you for verification.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b428-185">問題検索ツールの使用</span><span class="sxs-lookup"><span data-stu-id="6b428-185">Use the Issue search tool</span></span></td>
<td><span data-ttu-id="6b428-186"><a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a> で、問題検索は、サポート技術情報記事、修正プログラム、および Microsoft Dynamics AX で報告された問題の回避策をすぐに検索できる検索エンジンです。</span><span class="sxs-lookup"><span data-stu-id="6b428-186">In <a href="https://lifecycleservices.dynamics.com/en/">Microsoft Dynamics Lifecycle Services</a>, Issue search is a search engine that you can use to quickly search for KB articles, hotfixes, and workarounds for reported issues in Microsoft Dynamics AX.</span></span> <span data-ttu-id="6b428-187">どのレポート済みの問題が修正処理中であるか表示され、Microsoft Dynamics AX で特定の機能領域の修正プログラムがリリースされるときに通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6b428-187">You can see which reported issues are in the process of being fixed and see notifications when a hotfix is released for a specific functional area in Microsoft Dynamics AX.</span></span> <span data-ttu-id="6b428-188">リリース済の修正プログラムをダウンロードして、どのコード オブジェクトが影響を受けるか確認し、修正プログラムで導入されたコード変更を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="6b428-188">You can download released hotfixes, see which code objects are affected, and see the code changes introduced by the hotfix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b428-189">Microsoft Dynamics AX サポート チームとのサポート チケットを入力します。</span><span class="sxs-lookup"><span data-stu-id="6b428-189">Enter a support ticket with the Microsoft Dynamics AX support team</span></span></td>
<td><span data-ttu-id="6b428-190"><a href="https://community.dynamics.com/ax/p/support.aspx">Microsoft Dynamics AX のサポート</a>ページに移動して、サポート チケットを開きます。</span><span class="sxs-lookup"><span data-stu-id="6b428-190">Go to the <a href="https://community.dynamics.com/ax/p/support.aspx">Support for Microsoft Dynamics AX</a> page to open a support ticket.</span></span> <span data-ttu-id="6b428-191">Microsoft Dynamics AX サポート チームは、以下に関連する技術的な問題の解決をサポートします。</span><span class="sxs-lookup"><span data-stu-id="6b428-191">The Microsoft Dynamics AX support team can help you resolve technical issues related to:</span></span>
<ul>
<li><span data-ttu-id="6b428-192">Lifecycle Services の使用時のエラー</span><span class="sxs-lookup"><span data-stu-id="6b428-192">Errors when using Lifecycle Services</span></span></li>
<li><span data-ttu-id="6b428-193">Microsoft Dynamics AX の使用時のエラー</span><span class="sxs-lookup"><span data-stu-id="6b428-193">Errors when using Microsoft Dynamics AX</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





