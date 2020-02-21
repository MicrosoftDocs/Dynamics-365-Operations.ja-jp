---
title: システム診断のインストールと実行
description: Microsoft Dynamics Lifecycle Services では、Microsoft Dynamics AX 環境を検出してデータを収集するサービスが使用できるようになる前にインストールする必要があるオンプレミス コンポーネントがシステム診断に含まれています。
author: manalidongre
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 18861
ms.assetid: 075b4e28-162f-47ae-8713-392d711bdaff
ms.search.region: Global
ms.author: manado
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 92a6a47c3d39c23dead7e28f905d871d7a3574c4
ms.sourcegitcommit: 759325234a763e14071348a6f5399999a92f8264
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/25/2020
ms.locfileid: "2983605"
---
# <a name="install-and-run-system-diagnostics"></a><span data-ttu-id="326d5-103">システム診断のインストールと実行</span><span class="sxs-lookup"><span data-stu-id="326d5-103">Install and run System diagnostics</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="326d5-104">Microsoft Dynamics Lifecycle Services では、Microsoft Dynamics AX 環境を検出してデータを収集するサービスが使用できるようになる前にインストールする必要があるオンプレミス コンポーネントがシステム診断に含まれています。</span><span class="sxs-lookup"><span data-stu-id="326d5-104">In Microsoft Dynamics Lifecycle Services, System diagnostics includes an on-premises component that must be installed before you can use the service to discover Microsoft Dynamics AX environments and collect data.</span></span>

<a name="install-the-system-diagnostics-on-premises-component"></a><span data-ttu-id="326d5-105">システム診断オンプレミス コンポーネントのインストール</span><span class="sxs-lookup"><span data-stu-id="326d5-105">Install the System diagnostics on-premises component</span></span>
----------------------------------------------------

<span data-ttu-id="326d5-106">システム診断オンプレミス コンポーネントをインストールするには、以下が必要です。</span><span class="sxs-lookup"><span data-stu-id="326d5-106">To install the System diagnostics on-premises component, the following is required:</span></span>

-   <span data-ttu-id="326d5-107">ローカル コンピューターと Microsoft Dynamics AX ビジネス データベースに特定のアクセス許可を持つサービス アカウント。</span><span class="sxs-lookup"><span data-stu-id="326d5-107">A service account with specific permissions on the local computer and the Microsoft Dynamics AX business database.</span></span>
-   <span data-ttu-id="326d5-108">X509 証明書です。</span><span class="sxs-lookup"><span data-stu-id="326d5-108">An X509 certificate .</span></span> <span data-ttu-id="326d5-109">既存の証明書を使用するか、インストーラーにより作成することができます。</span><span class="sxs-lookup"><span data-stu-id="326d5-109">You can either use an existing certificate, or have the installer create one for you.</span></span> <span data-ttu-id="326d5-110">各 X509 証明書は、単一プロジェクトに関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="326d5-110">Each X509 certificate is associated with a single project.</span></span> <span data-ttu-id="326d5-111">環境からの診断は、1 つのプロジェクトにのみアップロードできます。</span><span class="sxs-lookup"><span data-stu-id="326d5-111">Diagnostics from an environment can be uploaded to only one project.</span></span>
-   <span data-ttu-id="326d5-112">Microsoft .NET 4.5 または 4.5.1</span><span class="sxs-lookup"><span data-stu-id="326d5-112">Microsoft .NET 4.5 or 4.5.1</span></span>

### <a name="configure-the-service-account-for-system-diagnostics"></a><span data-ttu-id="326d5-113">システム診断用のサービス アカウントをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="326d5-113">Configure the service account for System diagnostics</span></span>

<span data-ttu-id="326d5-114">このセクションでは、Lifecycle Services 診断サービス (LCSDiagFXService.exe) が実行されるサービス アカウントに必要なアクセス許可について説明します。</span><span class="sxs-lookup"><span data-stu-id="326d5-114">This section describes the permissions that are required for the service account that the Lifecycle Services Diagnostic Service (LCSDiagFXService.exe) runs as.</span></span>

-   <span data-ttu-id="326d5-115">サービス アカウントは、Microsoft Dynamics AX のユーザーで、**BusinessConnector** ロールのメンバーであるドメイン アカウントである必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-115">The service account must be a domain account that is a user in Microsoft Dynamics AX and a member of the **BusinessConnector** role.</span></span> <span data-ttu-id="326d5-116">可能な場合、アカウントは、.NET Business Connector プロキシに使用する同じアカウントを使用することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="326d5-116">We strongly recommend that, if possible, the account be the same account used for the .NET Business Connector proxy.</span></span> <span data-ttu-id="326d5-117">詳細については、[.NET Business Connector プロキシ アカウントを指定](https://technet.microsoft.com/library/3e46dc0a-2ff4-4a06-ae61-041e52dcc774(AX.60).aspx) および [セキュリティ ロールにユーザーを割り当てる](https://technet.microsoft.com/library/214ee45b-5b99-4ea8-9454-f4297f68e38c(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-117">For more information, see [Specify the .NET Business Connector proxy account](https://technet.microsoft.com/library/3e46dc0a-2ff4-4a06-ae61-041e52dcc774(AX.60).aspx) and [Assign users to security roles](https://technet.microsoft.com/library/214ee45b-5b99-4ea8-9454-f4297f68e38c(AX.60).aspx).</span></span>

    | <span data-ttu-id="326d5-118">**メモ**</span><span class="sxs-lookup"><span data-stu-id="326d5-118">**Note**</span></span>                                                                                                                     |
    |------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="326d5-119">.NET Business Connector プロキシ アカウントを再利用する場合は、引き続きそれを **BusinessConnector** ロールのメンバーとして追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-119">If you reuse the .NET Business connector proxy account, you must still add it as a member of the **BusinessConnector** role.</span></span> |

-   <span data-ttu-id="326d5-120">Lifecycle Services 診断サービスがデータを収集できるよう、サービス アカウントには、AOS インスタンスを実行し、Microsoft Dynamics AX ビジネス データベースをホストするすべてのコンピューター上の HKEY\_LOCAL\_MACHINE ハイブ内の特定のレジストリ キーへの読み取りアクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="326d5-120">The service account must have read access to specific registry keys in the HKEY\_LOCAL\_MACHINE hive on all of the computers that run AOS instances and host Microsoft Dynamics AX business databases, so that the Lifecycle Services Diagnostic Service can discover environments and collect data.</span></span>
-   <span data-ttu-id="326d5-121">サービス アカウントは、Lifecycle Services 診断サービスが Windows イベントログを読み取れるように、環境内の各サーバー上の**イベント ログ リーダー**のローカル グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-121">The service account must be a member of the **Event Log Readers** local group on each server in the environment, so that the Lifecycle Services Diagnostic Service can read the Windows event logs.</span></span>
-   <span data-ttu-id="326d5-122">Lifecycle Services 診断サービスが SQL Server で既定の動的管理ビューを実行できるよう、サービス アカウントには、Microsoft Dynamics AX ビジネス データベース (**db\_datareader**) への読み取りアクセスと、SQL Server インスタンスに対して VIEW SERVER STATE 権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="326d5-122">The service account must have read access to the Microsoft Dynamics AX business database (**db\_datareader**), and must have VIEW SERVER STATE permission for the SQL Server instance, so that Lifecycle Services Diagnostic Service can run default dynamic management views in SQL Server.</span></span>

#### <a name="configure-read-permissions-to-the-registry"></a><span data-ttu-id="326d5-123">レジストリへの読み取りアクセス許可をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="326d5-123">Configure read permissions to the registry</span></span>

<span data-ttu-id="326d5-124">AOS インスタンスまたは Microsoft Dynamics AX SQL Server ビジネス データベースをホストする環境内の各サーバーで、HKEY\_LOCAL\_MACHINE ハイブ内のレジストリ キーに対する読み取りアクセス権を、システム診断のサービス アカウントに付与する必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-124">On each server in your environment that hosts an AOS instance or Microsoft Dynamics AX SQL Server business database, you must grant read access to a registry key in the HKEY\_LOCAL\_MACHINE hive to the service account for the System diagnostics.</span></span>

| <span data-ttu-id="326d5-125">**注意**</span><span class="sxs-lookup"><span data-stu-id="326d5-125">**Caution**</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="326d5-126">次の手順には、Windows レジストリの編集が含まれます。</span><span class="sxs-lookup"><span data-stu-id="326d5-126">The following procedure includes editing the Windows Registry.</span></span> <span data-ttu-id="326d5-127">レジストリを誤って編集すると深刻な問題が発生し、Windows の再インストールが必要になることがあります。</span><span class="sxs-lookup"><span data-stu-id="326d5-127">Editing the registry incorrectly can cause serious problems that may require you to reinstall Windows.</span></span> <span data-ttu-id="326d5-128">Microsoft は、レジストリの編集によって発生した問題の解決については保証できません。</span><span class="sxs-lookup"><span data-stu-id="326d5-128">Microsoft cannot guarantee that problems resulting from incorrectly editing the registry can be solved.</span></span> <span data-ttu-id="326d5-129">解決済み。</span><span class="sxs-lookup"><span data-stu-id="326d5-129">solved.</span></span> <span data-ttu-id="326d5-130">レジストリを編集する前に、レジストリ ファイル (System.dat と User.dat) のバックアップを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-130">You should make a backup copy of the registry files (System.dat and User.dat) before you edit the registry.</span></span> |

<span data-ttu-id="326d5-131">SQL Server ビジネス データベースをホストするサーバー上の Windows レジストリからデータを収集するためのアクセスを許可するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="326d5-131">To grant access to collect data from the Windows registry on the server that hosts the SQL Server business database:</span></span>
1.  <span data-ttu-id="326d5-132">**開始**、**実行**をクリックし、**regedit** と入力し、次に **Enter** を押します。</span><span class="sxs-lookup"><span data-stu-id="326d5-132">Click **Start**, click **Run**, type **regedit**, and then press **Enter**.</span></span>
2.  <span data-ttu-id="326d5-133">**HKEY\_LOCAL\_MACHINE** を展開し、サブキー **System\CurrentControlSet\Control\PriorityControl** で移動し、右クリックおよび**アクセス許可**を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-133">Expand **HKEY\_LOCAL\_MACHINE**, navigate to the subkey **System\CurrentControlSet\Control\PriorityControl**, right-click it and select **Permissions**.</span></span>
3.  <span data-ttu-id="326d5-134">Lifecycle Services 診断サービスに関連付ける必要のあるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-134">Add the user that you want to associate with the Lifecycle Services Diagnostic Service.</span></span>
4.  <span data-ttu-id="326d5-135">追加したユーザーを選択し、読み取りアクセス許可を許可します。</span><span class="sxs-lookup"><span data-stu-id="326d5-135">Select the user that you added, and then allow read permissions.</span></span>
5.  <span data-ttu-id="326d5-136">**セキュリティの詳細設定**をクリックし、アクセス許可が子オブジェクトによって継承されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="326d5-136">Click **Advanced Security Settings**, and then ensure that the permissions are inherited by the child objects.</span></span>

<span data-ttu-id="326d5-137">1 つ以上の AOS インスタンスをホストするサーバー上の Windows レジストリからデータを収集するためのアクセスを許可するには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="326d5-137">To grant access to collect data from the Windows registry on a server that hosts one or more AOS instances:</span></span>
1.  <span data-ttu-id="326d5-138">**開始**、**実行**をクリックし、**regedit** と入力し **Enter** を押します。</span><span class="sxs-lookup"><span data-stu-id="326d5-138">Click **Start**, click **Run**, type **regedit**, and press **Enter**.</span></span>
2.  <span data-ttu-id="326d5-139">**HKEY\_LOCAL\_MACHINE** を展開し、サブキー **System\CurrentControlSet\Services\Dynamics Server\6.0** で移動し、右クリックおよび**アクセス許可**を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-139">Expand **HKEY\_LOCAL\_MACHINE**, navigate to the subkey **System\CurrentControlSet\Services\Dynamics Server\6.0**, right-click it and select **Permissions**.</span></span>
3.  <span data-ttu-id="326d5-140">Lifecycle Services 診断サービスに関連付ける必要のあるユーザーを追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-140">Add the user that you want to associate with the Lifecycle Services Diagnostic Service.</span></span>
4.  <span data-ttu-id="326d5-141">追加したユーザーを選択し、読み取りアクセス許可を許可します。</span><span class="sxs-lookup"><span data-stu-id="326d5-141">Select the user that you added, and then allow read permissions.</span></span>
5.  <span data-ttu-id="326d5-142">**セキュリティの詳細設定**をクリックし、アクセス許可が子オブジェクトによって継承されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="326d5-142">Click **Advanced Security Settings**, and then ensure that the permissions are inherited by the child objects.</span></span>
6.  <span data-ttu-id="326d5-143">データの収集元にする各環境でのすべての AOS インスタンスを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="326d5-143">Repeat for all AOS instances in each environment that you want to collect data from.</span></span>

<table>
<colgroup>
<col width="100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="326d5-144"><strong>重要</strong></span><span class="sxs-lookup"><span data-stu-id="326d5-144"><strong>Important</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="326d5-145">レジストリで権限を設定するには、既に存在しているアクセス特権を削減することはできません。</span><span class="sxs-lookup"><span data-stu-id="326d5-145">As you are configuring rights in the registry, do not reduce account privileges that already exist.</span></span> <span data-ttu-id="326d5-146">セキュリティの詳細設定については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-146">For more information about Advanced security settings, see:</span></span>
<ul>
<li><span data-ttu-id="326d5-147"><a href="https://technet.microsoft.com/library/jj134043.aspx">Windows Server 2012 アクセス制御と承認の概要</a></span><span class="sxs-lookup"><span data-stu-id="326d5-147"><a href="https://technet.microsoft.com/library/jj134043.aspx">Windows Server 2012 Access Control and Authorization Overview</a></span></span></li>
<li><span data-ttu-id="326d5-148"><a href="https://technet.microsoft.com/library/cc730772.aspx">Windows Server 2008 R2 セキュリティの詳細設定のプロパティ ページ - アクセス許可タブ</a></span><span class="sxs-lookup"><span data-stu-id="326d5-148"><a href="https://technet.microsoft.com/library/cc730772.aspx">Windows Server 2008 R2 Advanced Security Settings Properties Page - Permissions Tab</a></span></span></li>
</ul></td>
</tr>
</tbody>
</table>

#### <a name="edit-the-group-policy-on-the-aos"></a><span data-ttu-id="326d5-149">AOS のグループ ポリシーを編集</span><span class="sxs-lookup"><span data-stu-id="326d5-149">Edit the Group Policy on the AOS</span></span>

<span data-ttu-id="326d5-150">Group Policy では、AOS のサービスをリモートで利用できるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="326d5-150">You must make the services of the AOS remotely accessible in Group Policy.</span></span>

1.  <span data-ttu-id="326d5-151">AOS インスタンスを実行するコンピューターで、**開始** &gt; **実行**をクリックして、**gpedit.msc** を入力し、**Enter** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="326d5-151">On the computer running the AOS instance, click **Start** &gt; **Run**, type **gpedit.msc**, and then press **Enter**.</span></span>
2.  <span data-ttu-id="326d5-152">左ウィンドウで、**コンピューターの構成** &gt; **Windows の設定** &gt; **セキュリティ設定** &gt; **ローカル ポリシー** &gt; **セキュリティ オプション**を展開します。</span><span class="sxs-lookup"><span data-stu-id="326d5-152">In the left pane, expand **Computer Configuration** &gt; **Windows settings** &gt; **Security settings** &gt; **Local policies** &gt; **Security options**.</span></span>
3.  <span data-ttu-id="326d5-153">右ウィンドウで、**ネットワーク アクセス: リモートからアクセスできるレジストリ パスおよびサブ パス**をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-153">In the right pane, double-click **Network access: Remotely accessible registry paths and sub-paths**.</span></span>
4.  <span data-ttu-id="326d5-154">次のパスがリストにない場合は、リストの最後にそれを追加し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-154">If the following paths are not in the list, add them to the end of the list and then click **OK**.</span></span>
    -   <span data-ttu-id="326d5-155">System\CurrentControlSet\Control\PriorityControl</span><span class="sxs-lookup"><span data-stu-id="326d5-155">System\CurrentControlSet\Control\PriorityControl</span></span>
    -   <span data-ttu-id="326d5-156">System\CurrentControlSet\services\Dynamics Server\6.0</span><span class="sxs-lookup"><span data-stu-id="326d5-156">System\CurrentControlSet\services\Dynamics Server\6.0</span></span>

#### <a name="configure-windows-event-log-and-wmi-permissions"></a><span data-ttu-id="326d5-157">Windows イベント ログおよび WMI のアクセス許可をコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="326d5-157">Configure Windows event log and WMI permissions</span></span>

<span data-ttu-id="326d5-158">サービス アカウントは、環境内の各サーバー上の Windows イベント ログを読み取ることができ、リモートで Windows Management Instrumentation 接続を監視できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-158">The service account must be able to read the Windows event logs on each server in the environment, and must be able to monitor remote Windows Management Instrumentation connections.</span></span> <span data-ttu-id="326d5-159">詳細については、「[ローカル グループへのメンバーの追加](https://technet.microsoft.com/library/cc772524(v=WS.10).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-159">For more information, see [Add a member to a local group](https://technet.microsoft.com/library/cc772524(v=WS.10).aspx).</span></span>

-   <span data-ttu-id="326d5-160">環境内の各サーバーでは、サービス アカウントを**イベント ログ リーダー**ローカル グループ、**配分 COM ユーザー**ローカル グループ、および**パフォーマンス ユーザーの監視** ローカル グループに追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-160">On each server in the environment, add the service account to the **Event Log Readers** local group, the **Distributed COM Users** local group and the **Performance Monitor Users** local group.</span></span>

#### <a name="secure-the-remote-windows-management-instrumentation-connections"></a><span data-ttu-id="326d5-161">Windows Management Instrumentation リモート接続をセキュリティで保護</span><span class="sxs-lookup"><span data-stu-id="326d5-161">Secure the remote Windows Management Instrumentation connections</span></span>

<span data-ttu-id="326d5-162">AOS インスタンスまたは Microsoft Dynamics AX SQL Server ビジネス データベースをホストする環境内の各サーバーで、リモート Windows Management Instrumentation(WMI) 接続をセキュリティで保護されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="326d5-162">On each server in your environment that hosts an AOS instance or Microsoft Dynamics AX SQL Server business database, ensure that you secure the remote Windows Management Instrumentation (WMI) connection.</span></span>

1.  <span data-ttu-id="326d5-163">**開始** &gt; **実行**の順にクリックし、**DCOMCNFG** と入力し **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-163">Click **Start** &gt; **Run**, type **DCOMCNFG**, and then click **OK**.</span></span>
2.  <span data-ttu-id="326d5-164">**コンポーネント サービス** ダイアログ ボックスで、**コンポーネント サービス**を展開し、**コンピューター**を展開してから、**マイ コンピューター**を右クリックして**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-164">In the **Component Services** dialog box, expand **Component Services**, expand **Computers**, and then right-click **My Computer** and click **Properties**.</span></span>
3.  <span data-ttu-id="326d5-165">**マイ コンピューターのプロパティ** ダイアログ ボックスで、**COM セキュリティ** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-165">In the **My Computer Properties** dialog box, click the **COM Security** tab.</span></span>
4.  <span data-ttu-id="326d5-166">**起動とアクティベーションのアクセス許可** で、**制限の編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-166">Under **Launch and Activation Permissions**, click **Edit Limits**.</span></span>
5.  <span data-ttu-id="326d5-167">**起動アクセス許可**ダイアログ ボックスで、名前またはグループが**グループまたはユーザー名**一覧に表示されない場合は次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="326d5-167">In the **Launch Permission** dialog box, follow these steps if your name or your group does not appear in the **Groups or user names** list:</span></span>
    1.  <span data-ttu-id="326d5-168">**起動アクセス許可**ダイアログ ボックスで、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-168">In the **Launch Permission** dialog box, click **Add**.</span></span>
    2.  <span data-ttu-id="326d5-169">**ユーザー、コンピュータ、またはグループの選択**ダイアログ ボックスの**選択するオブジェクト名を入力してください**ボックスに**配分 COM ユーザー**と入力して、**名前の確認**をクリックしてから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-169">In the **Select Users, Computers, or Groups** dialog box, in the **Enter the object names to select** box, type **Distributed COM Users**, click **Check Names**, and then click **OK**.</span></span>
    3.  <span data-ttu-id="326d5-170">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-170">Click **Add**.</span></span>
    4.  <span data-ttu-id="326d5-171">**選択するオブジェクト名を入力してください**ボックスに、**パフォーマンス モニター ユーザー**と入力し、**名前の確認**をクリックしてから、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-171">In the **Enter the object names to select** box, type **Performance Monitor Users**, click **Check Names**, and then click **OK**.</span></span>
    5.  <span data-ttu-id="326d5-172">各グループの各アクセス許可 (ローカル起動、リモート起動、ローカルの有効化、リモートの有効化) について **許可** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-172">Select **Allow** for each of the permissions (Local Launch, Remote Launch, Local Activation, Remote Activation) for each of these groups, and then click **OK**.</span></span>

6.  <span data-ttu-id="326d5-173">すべての名前空間に WMI コントロールのセキュリティ設定を適用します。</span><span class="sxs-lookup"><span data-stu-id="326d5-173">Apply the WMI control security settings to all namespaces:</span></span>
    1.  <span data-ttu-id="326d5-174">**開始** &gt; **実行**の順にクリックし、**wmimgmt.msc** と入力し **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-174">Click **Start** &gt; **Run**, type **wmimgmt.msc**, and then click **OK**.</span></span>
    2.  <span data-ttu-id="326d5-175">**WMI コントロール (ローカル)** を右クリックし、**プロパティ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-175">Right-click **WMI Control (Local)**, and then click **Properties**.</span></span>
    3.  <span data-ttu-id="326d5-176">**セキュリティ**タブで、**ルート**をクリックし、**セキュリティ**をクリックして、**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-176">On the **Security** tab, click **Root**, click **Security**, and then click **Add**.</span></span>
    4.  <span data-ttu-id="326d5-177">**選択するオブジェクト名の入力** で Distributed COM ユーザーを入力し、**名前の確認** をクリックしてから **OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-177">Under **Enter the object names to select**, type Distributed COM users, click **Check Names**, and then click **OK**.</span></span>
    5.  <span data-ttu-id="326d5-178">**詳細**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-178">Click **Advanced**.</span></span>
    6.  <span data-ttu-id="326d5-179">**配布される COM ユーザー** を選択し、**編集** をクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="326d5-179">Select **Distributed COM Users** and then click **Edit**.</span></span>
    7.  <span data-ttu-id="326d5-180">**この名前空間とサブ名前空間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-180">Select **This namespace and subnamespaces**.</span></span>
    8.  <span data-ttu-id="326d5-181">メソッドの実行、アカウントの有効化、リモートの有効化のアクセス許可について **許可** を選択し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-181">Select **Allow** for the following permissions: Execute Methods, Enable Account, and Remote Enable, and then click **OK**.</span></span>

7.  <span data-ttu-id="326d5-182">パフォーマンス モニター ユーザー グループで手順 6 を繰り返し、すべてのウィンドウを閉じます。</span><span class="sxs-lookup"><span data-stu-id="326d5-182">Repeat step 6 for the Performance Monitor Users group, and then close all windows.</span></span>

<span data-ttu-id="326d5-183">詳細については、「[リモート WMI 接続の保護](https://msdn.microsoft.com/library/windows/desktop/aa393266(v=vs.85).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-183">For more information, see [Securing a Remote WMI Connection](https://msdn.microsoft.com/library/windows/desktop/aa393266(v=vs.85).aspx).</span></span>

#### <a name="configure-sql-server-permissions"></a><span data-ttu-id="326d5-184">SQL Server のアクセス許可をコンフィギュレーションします</span><span class="sxs-lookup"><span data-stu-id="326d5-184">Configure SQL Server permissions</span></span>

<span data-ttu-id="326d5-185">サービス アカウントは、Microsoft Dynamics AX ビジネス データベースのデータを読み取ることができ、SQL Server の既定の動的管理ビューにアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-185">The service account must be able to read the data in the Microsoft Dynamics AX business database and must have access to the default dynamic management views in SQL Server.</span></span>

1.  <span data-ttu-id="326d5-186">Microsoft Dynamics AX ビジネス データベースがインストールされている SQL Server インスタンスに、ログインとしてサービス アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-186">Add the service account as a login to the SQL Server instance where the Microsoft Dynamics AX business database is installed.</span></span> <span data-ttu-id="326d5-187">このステップを実行する方法の詳細については、「[ログインの作成](https://msdn.microsoft.com/library/aa337562.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-187">For information about how to perform this step, see [Create a Login](https://msdn.microsoft.com/library/aa337562.aspx).</span></span>
2.  <span data-ttu-id="326d5-188">ビジネス データベースのユーザーとしてアカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-188">Add the account as a user of the business database.</span></span> <span data-ttu-id="326d5-189">このステップを実行する方法の詳細については、「[方法: データベース ユーザーの作成](https://msdn.microsoft.com/library/aa337545.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-189">For information about how to perform this step, see [How to: Create a Database User](https://msdn.microsoft.com/library/aa337545.aspx).</span></span>
3.  <span data-ttu-id="326d5-190">ビジネス データベースの db\_datareader ロールにサービス アカウントを追加します。</span><span class="sxs-lookup"><span data-stu-id="326d5-190">Add the service account to the db\_datareader role in the business database.</span></span> <span data-ttu-id="326d5-191">このステップを実行する方法の詳細については、「[ロールに参加](https://msdn.microsoft.com/library/ff877886.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-191">For information about how to perform this step, see [Join a Role](https://msdn.microsoft.com/library/ff877886.aspx).</span></span>
4.  <span data-ttu-id="326d5-192">サービス アカウントに SQL Server インスタンスの VIEW SERVER STATE 権限を付与します。</span><span class="sxs-lookup"><span data-stu-id="326d5-192">Grant the service account the VIEW SERVER STATE permission in the SQL Server instance.</span></span>
    1.  <span data-ttu-id="326d5-193">SQL Server Management Studio で、**データベース**を展開し、**Microsoft Dynamics AX** データベースを右クリックし、**プロパティ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-193">In SQL Server Management Studio, expand **Databases**, right-click the **Microsoft Dynamics AX** database, and then click **Properties**.</span></span>
    2.  <span data-ttu-id="326d5-194">**アクセス許可**をクリックし、次に**サーバーのアクセス許可を表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-194">Click **Permissions**, and then click **View server permissions**.</span></span>
    3.  <span data-ttu-id="326d5-195">**ログインまたはロール**一覧で、アクセス許可を付与するユーザーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-195">In the **Logins or Roles** list, click the user to whom you want to grant the permission.</span></span>
    4.  <span data-ttu-id="326d5-196">**ユーザーの明示的なアクセス許可**リストで、**サーバー状態のアクセス許可を表示**の隣にある**付与**チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="326d5-196">In the **Explicit permissions for user** list, select the **Grant** check box next to **View server state permission**.</span></span>

### <a name="verify-that-the-net-business-connector-service-is-running-in-the-environment"></a><span data-ttu-id="326d5-197">この環境で .NET Business connector サービスが実行されていることを確認する</span><span class="sxs-lookup"><span data-stu-id="326d5-197">Verify that the .NET Business connector service is running in the environment</span></span>

<span data-ttu-id="326d5-198">Business Connector サービスは、Lifecycle Services 診断サービスがインストールされているホストで実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-198">The Business Connector service must be running on the host where the Lifecycle Services Diagnostic Service is installed.</span></span> <span data-ttu-id="326d5-199">1 つ以上の環境が見つかると、.Ne ビジネス コネクタ プロキシ アカウントは、Microsoft Dynamics AX Application Object Server (AOS) インスタンスを実行している各サーバーと同じものである必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-199">If more than one environment is to be discovered, the .Net Business Connector proxy account must be the same for each server that is running a Microsoft Dynamics AX Application Object Server (AOS) instance.</span></span> <span data-ttu-id="326d5-200">詳細については、[.NET Business Connector のインストール](https://technet.microsoft.com/library/c67944e8-73c5-4434-94d6-84484c810333(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="326d5-200">For more information, see [Install the .NET Business Connector](https://technet.microsoft.com/library/c67944e8-73c5-4434-94d6-84484c810333(AX.60).aspx).</span></span>

### <a name="install-the-microsoft-dynamics-lifecycle-services-system-diagnostics"></a><span data-ttu-id="326d5-201">Microsoft Dynamics Lifecycle Services システム診断のインストール</span><span class="sxs-lookup"><span data-stu-id="326d5-201">Install the Microsoft Dynamics Lifecycle Services System diagnostics</span></span>

<span data-ttu-id="326d5-202">システム診断プログラムのオンプレミス コンポーネントをインストールするには、ローカル コンピューターの Administrator グループのメンバーである必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-202">To install the on-premises component of System diagnostics, you must be a member of the Administrator group on the local computer.</span></span>

1.  <span data-ttu-id="326d5-203">[Lifecycle Services に移動](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="326d5-203">[Go to Lifecycle Services](https://lcs.dynamics.com).</span></span>
2.  <span data-ttu-id="326d5-204">プロジェクトを開いて、**システム診断**タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-204">Open a project and click the **System diagnostics** tile.</span></span>
3.  <span data-ttu-id="326d5-205">**管理者**ページで、圧縮インストーラーをダウンロードします (**LCSDiagFX\_x64.zip.**)。</span><span class="sxs-lookup"><span data-stu-id="326d5-205">On the **Admin** page, download the compressed installer (**LCSDiagFX\_x64.zip.**).</span></span>
4.  <span data-ttu-id="326d5-206">Microsoft Dynamics AX クライアントを実行しているコンピュータにインストーラーを抽出します。</span><span class="sxs-lookup"><span data-stu-id="326d5-206">Extract the installer to a computer that is running a Microsoft Dynamics AX client.</span></span> <span data-ttu-id="326d5-207">コンピューターが環境内の他のすべてのサーバーにネットワーク アクセスできる必要があります。.Net Business Connector プロキシ アカウントをサービス アカウントとして使用している場合は、.NET Business Connector を実行している必要があります。</span><span class="sxs-lookup"><span data-stu-id="326d5-207">The computer must have network access to all other servers in the environment, and must be running the .NET Business Connector if you are using the NET Business Connector proxy account as a service account.</span></span>

    | <span data-ttu-id="326d5-208">**重要**</span><span class="sxs-lookup"><span data-stu-id="326d5-208">**Important**</span></span>                                                                                                                                                                                                      |
    |--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="326d5-209">実稼働環境では、AOS インスタンスまたは SQL Server インスタンスも実行しているコンピューターではなく、クライアントのみ実行しているコンピューターにオンプレミス コンポーネントをインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="326d5-209">In a production environment, we recommend that you install the on-premises component on a computer that is running only a client, not on computers that are also running an AOS instance or a SQL Server instance.</span></span> |

5.  <span data-ttu-id="326d5-210">**Setup.exe** を実行します。</span><span class="sxs-lookup"><span data-stu-id="326d5-210">Run **Setup.exe**.</span></span>

    | <span data-ttu-id="326d5-211">**メモ**</span><span class="sxs-lookup"><span data-stu-id="326d5-211">**Note**</span></span>                           |
    |------------------------------------|
    | <span data-ttu-id="326d5-212">直接 MSI ファイルを実行しないでください。</span><span class="sxs-lookup"><span data-stu-id="326d5-212">Do not run the .msi file directly.</span></span> |

6.  <span data-ttu-id="326d5-213">ライセンス条項に同意します。</span><span class="sxs-lookup"><span data-stu-id="326d5-213">Accept the license terms.</span></span>
7.  <span data-ttu-id="326d5-214">既存のローカル X509 証明書をお持ちの場合は、**証明書タイプを選択** ページで、**既存のものを使用**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-214">If you have an existing local X509 certificate, on the **Select the certificate type** page, click **Use existing**.</span></span> <span data-ttu-id="326d5-215">X509 証明書がない場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="326d5-215">If you do not have an X509 certificate, perform the following steps:</span></span>
    1.  <span data-ttu-id="326d5-216">**証明書タイプの選択**ページで、**新規作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-216">On the **Select the certificate type** page, click **Create new**.</span></span>
    2.  <span data-ttu-id="326d5-217">証明書の名前で使用される接頭語を入力します。</span><span class="sxs-lookup"><span data-stu-id="326d5-217">Enter a prefix to be used in the certificate name.</span></span>
    3.  <span data-ttu-id="326d5-218">**次へ**をクリックして証明書を作成します。</span><span class="sxs-lookup"><span data-stu-id="326d5-218">Click **Next** to create the certificate.</span></span>
    4.  <span data-ttu-id="326d5-219">指定した場所に新しい証明書が作成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="326d5-219">Verify that the new certificate has been created in the specified location.</span></span>

8.  <span data-ttu-id="326d5-220">**システム診断** ページに戻り、証明書の場所を参照して **アップロード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-220">Return to the **System diagnostics** page, browse to the location of the certificate, and click **Upload**.</span></span>
9.  <span data-ttu-id="326d5-221">**Microsoft Dynamics Lifecycle Services 診断サービス セットアップ ウィザード**の **新しい証明書のアップロード** ページに戻り、**証明書ファイルがアップロードされました**を選択して**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-221">Return to the **Upload the new certificate** page of the **Microsoft Dynamics Lifecycle Services Diagnostic Service Setup Wizard**, select **Certificate file has been uploaded**, and click **Next**.</span></span>
10. <span data-ttu-id="326d5-222">**プライベート証明書の選択**ページで、証明書の名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="326d5-222">On the **Select private certificate** page, the name of the certificate is displayed.</span></span> <span data-ttu-id="326d5-223">**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-223">Click **Next**.</span></span>
11. <span data-ttu-id="326d5-224">**サービス アカウントの指定**ページで、サービス アカウントとパスワードを入力し、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-224">On the **Specify service account** page, enter the service account and password, and then click **Next**.</span></span>
12. <span data-ttu-id="326d5-225">**変更先フォルダ**ページで、システム診断によって収集されたログを保管する場所を入力し、**次**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-225">On the **Change destination folder** page, enter the location where you want to store the logs that were collected by the System diagnostics, and then click **Next**.</span></span>
13. <span data-ttu-id="326d5-226">**OK** クリックして、システム診断をインストールおよび開始し、次に**完了**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-226">Click **OK** to install and start the System diagnostics, and then click **Finish**.</span></span>

<span data-ttu-id="326d5-227">2 つの実行可能プログラム、LCSDiagFXDiscovery.exe と LCSDiagFXCollector.exe がインストールされています。</span><span class="sxs-lookup"><span data-stu-id="326d5-227">Two executable programs are installed: LCSDiagFXDiscovery.exe and LCSDiagFXCollector.exe.</span></span>

## <a name="discover-environments"></a><span data-ttu-id="326d5-228">環境を検出</span><span class="sxs-lookup"><span data-stu-id="326d5-228">Discover environments</span></span>
1.  <span data-ttu-id="326d5-229">**開始**、**Microsoft Dynamics AX Lifecycle Services 診断サービス検索**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-229">Click **Start**, and then click **Microsoft Dynamics AX Lifecycle Services Diagnostic Service Discovery.**</span></span>
2.  <span data-ttu-id="326d5-230">**環境の検出**ウィンドウに、環境の名前と SQL Server のインスタンスとデータベースの完全修飾名を入力してから、**検出**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-230">In the **Environment Discovery** window, enter a name for the environment, the fully-qualified name of the SQL Server instance and database, and then click **Discover**.</span></span>
3.  <span data-ttu-id="326d5-231">ウィンドウの一番下にある**テストアクセス許可**ボタンをクリックします。![システム診断用のテストアクセス許可ボタン](./media/testpermissions.jpg) ページの下部にあります。</span><span class="sxs-lookup"><span data-stu-id="326d5-231">At the bottom of the Window, click the **Test permissions** button ![Test permissions button for System diagnostics](./media/testpermissions.jpg) at the bottom of the page.</span></span>
4.  <span data-ttu-id="326d5-232">**変更先フォルダ**ページで、システム診断によって収集されたログを保管する場所を入力し、**次**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-232">On the **Change destination folder** page, enter the location where you want to store the logs that were collected by the System diagnostics, and then click **Next**.</span></span>

## <a name="collect-data"></a><span data-ttu-id="326d5-233">データを収集</span><span class="sxs-lookup"><span data-stu-id="326d5-233">Collect data</span></span>
<span data-ttu-id="326d5-234">必要に応じて **環境の検出** ウィンドウからデータを収集することができます。</span><span class="sxs-lookup"><span data-stu-id="326d5-234">You can collect data on demand from the **Environment Discovery** window.</span></span> <span data-ttu-id="326d5-235">定期的にデータを収集するジョブをスケジュールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="326d5-235">We recommend that you schedule a job to collect data regularly.</span></span> <span data-ttu-id="326d5-236">データ収集は、通常、5 ~ 15 分かかります。</span><span class="sxs-lookup"><span data-stu-id="326d5-236">Data collection typically takes between 5 and 15 minutes.</span></span> <span data-ttu-id="326d5-237">データ収集中に発生したエラーは、Windows アプリケーション イベント ログと、インストール中に指定した場所のログ ファイルに記録されます。</span><span class="sxs-lookup"><span data-stu-id="326d5-237">Errors that are encountered during data collection are logged in the Windows Application event log, as well as in a log file in the location that you specified during installation.</span></span>

1.  <span data-ttu-id="326d5-238">**環境の検出** ウィンドウで初期データ収集を実行するには、**今すぐ収集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-238">To run an initial data collection in the **Environment Discovery** window, click **Collect now**.</span></span> <span data-ttu-id="326d5-239">初めて環境を検出した直後に最初のコレクションを実行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="326d5-239">We recommend that you run an initial collection immediately after discovering an environment for the first time.</span></span>
2.  <span data-ttu-id="326d5-240">コレクション ジョブのスケジューリングに使用できるコレクション コマンドを生成するするには、**コレクション コマンドを生成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-240">To generate a collection command that you can use to schedule collection jobs, click **Generate collection command**.</span></span>
3.  <span data-ttu-id="326d5-241">生成されたコマンドをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="326d5-241">Copy the generated command to the clipboard.</span></span>
4.  <span data-ttu-id="326d5-242">**Windows タスク スケジューラ**などのスケジュール エンジンを使用して実行するコマンドをスケジュール設定します。</span><span class="sxs-lookup"><span data-stu-id="326d5-242">Schedule the command to run by using a scheduling engine, such as **Windows Task Scheduler**.</span></span> <span data-ttu-id="326d5-243">**タスク スケジューラ**の使用の詳細については、[タスクのスケジュール](https://technet.microsoft.com/library/cc766428.aspx) を参照してください</span><span class="sxs-lookup"><span data-stu-id="326d5-243">For more information about using **Task Scheduler**, see [Schedule a task](https://technet.microsoft.com/library/cc766428.aspx).</span></span>

## <a name="use-same-x509-certificate-for-all-environments"></a><span data-ttu-id="326d5-244">すべての環境で同じ X509 証明書を使用する</span><span class="sxs-lookup"><span data-stu-id="326d5-244">Use same X509 certificate for all environments</span></span>

1.  <span data-ttu-id="326d5-245">当初期間は、証明書を生成する設定を従来どおりにします</span><span class="sxs-lookup"><span data-stu-id="326d5-245">First time let setup generate certificate as usual</span></span>
2.  <span data-ttu-id="326d5-246">MMC (Microsoft管理コンソール) を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="326d5-246">Run MMC (Microsoft management console) as admin</span></span>
3.  <span data-ttu-id="326d5-247">ファイル -&gt; **スナップインの追加または削除**</span><span class="sxs-lookup"><span data-stu-id="326d5-247">File -&gt; "**Add or Remove Snap-ins**"</span></span>
4.  <span data-ttu-id="326d5-248">**証明書**項目をダブルクリックし、コンピューター アカウントと next-&gt;finish-&gt;ok を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-248">Double click **Certificates** item and choose computer account then next-&gt;finish-&gt;ok</span></span>
5.  <span data-ttu-id="326d5-249">証明書 (ローカル コンピューター)-&gt;**個人**-&gt; 証明書を展開します。</span><span class="sxs-lookup"><span data-stu-id="326d5-249">Expand Certificates (Local Computer)-&gt;**Personal**-&gt;Certificates:</span></span>
6.  <span data-ttu-id="326d5-250">最初の手順 - &gt; すべてのタスク -&gt; エクスポート -&gt; 次へ -&gt; "**はい、プライベート キーをエクスポートします**" で生成された証明書を右クリックします。</span><span class="sxs-lookup"><span data-stu-id="326d5-250">Right click on certificate generated on first step -&gt; All tasks -&gt; Export -&gt; Next -&gt; Choose "**Yes, export the private key**"</span></span>
7.  <span data-ttu-id="326d5-251">\*.pfx エクスポート設定で既定値のままにする</span><span class="sxs-lookup"><span data-stu-id="326d5-251">Leave default values in \*.pfx export setup</span></span>
8.  <span data-ttu-id="326d5-252">セキュリティ ステップでは、エクスポートしたファイルを保護するためにドメイン アカウントまたはパスワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="326d5-252">In security step Use domain account or password for securing your exported file</span></span>
9.  <span data-ttu-id="326d5-253">次の手順でファイルをエキスポート</span><span class="sxs-lookup"><span data-stu-id="326d5-253">Export files in next steps</span></span>
10. <span data-ttu-id="326d5-254">エクスポートしたファイルを新しい環境にコピーし、クリックして、**PFX のインストール**を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-254">Copy exported file to new environment click it and choose **Install PFX**</span></span>
11. <span data-ttu-id="326d5-255">**ローカル コンピューター**を選択します。</span><span class="sxs-lookup"><span data-stu-id="326d5-255">Choose **Local Machine**</span></span>
12. <span data-ttu-id="326d5-256">次へ -&gt; をクリックし、次の画面で、**このキーをエクスポート可能としてマーク**が設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="326d5-256">Click next -&gt; And in following screen make sure that **Mark this key as exportable** is set.</span></span> <span data-ttu-id="326d5-257">次へをクリックして終了</span><span class="sxs-lookup"><span data-stu-id="326d5-257">Click next and finish</span></span>
13. <span data-ttu-id="326d5-258">ここで、Lifecycle Services システム診断セットアップを実行している場合、新しい環境を選択して既存の証明書を使用します。</span><span class="sxs-lookup"><span data-stu-id="326d5-258">Now when running Lifecycle services system diagnostics setup choose on new environment use an existing certificate</span></span>
14. <span data-ttu-id="326d5-259">最初の手順で生成された証明書は、クライアント証明書のルックアップに含まれており、それを選択して通常どおりに続行する必要があります:</span><span class="sxs-lookup"><span data-stu-id="326d5-259">Certificate generated in first step should be present in client certificates lookup choose it and continue as usual:</span></span>





