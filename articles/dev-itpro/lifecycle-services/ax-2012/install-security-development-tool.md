---
title: セキュリティ開発ツールをインストールする
description: このトピックでは、セキュリティ開発ツールのインストール方法について説明します。
author: kfend
manager: AnnBe
ms.date: 07/26/2018
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 18391
ms.assetid: f62f5636-4d63-473e-b326-277ea500c540
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: 53865c47b9a66c6fa292b14590d962721bdde0db
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544083"
---
# <a name="install-the-security-development-tool"></a><span data-ttu-id="a9873-103">セキュリティ開発ツールをインストールする</span><span class="sxs-lookup"><span data-stu-id="a9873-103">Install the Security Development Tool</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE] 

> <span data-ttu-id="a9873-104">これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a9873-104">This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="a9873-105">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="a9873-105">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span> <span data-ttu-id="a9873-106">セキュリティ開発ツールをインストールする前に、次の前提条件を満たしていることを仮定します。</span><span class="sxs-lookup"><span data-stu-id="a9873-106">Before you install the Security Development Tool, be aware that we assume that you meet the following prerequisites:</span></span>

-   <span data-ttu-id="a9873-107">Microsoft Dynamics AX 2012 の開発環境を使い慣れています。</span><span class="sxs-lookup"><span data-stu-id="a9873-107">You are familiar with the development environment in Microsoft Dynamics AX 2012.</span></span>
-   <span data-ttu-id="a9873-108">Microsoft Dynamics AX 2012 のセキュリティ モデルを使い慣れています。</span><span class="sxs-lookup"><span data-stu-id="a9873-108">You are familiar with the security model in Microsoft Dynamics AX 2012.</span></span>
-   <span data-ttu-id="a9873-109">Microsoft Dynamics AX の開発者権限を持っている場合、アプリケーション オブジェクト ツリー (AOT) からツールを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a9873-109">You have developer privileges in Microsoft Dynamics AX, so that you can run the tool from the Application Object Tree (AOT).</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="a9873-110">セキュリティ開発ツールの一部のオプション機能では、フレームワーク クラスを変更したり、その追跡を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9873-110">Some optional features of the Security Development Tool require that changes be made to framework classes, or that tracing be enabled.</span></span> <span data-ttu-id="a9873-111">これらの変更は、Microsoft Dynamics AX システムの全体的なパフォーマンスに影響する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a9873-111">These changes can affect the overall performance of your Microsoft Dynamics AX system.</span></span> <span data-ttu-id="a9873-112">したがって、このツールは開発環境またはテスト環境でのみ使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9873-112">Therefore, we recommend that you use this tool only in development or test environments.</span></span>

## <a name="procedures"></a><span data-ttu-id="a9873-113">手順</span><span class="sxs-lookup"><span data-stu-id="a9873-113">Procedures</span></span>
<span data-ttu-id="a9873-114">このセクションでは、セキュリティ開発ツールのインストールと設定に必要なステップを示します。</span><span class="sxs-lookup"><span data-stu-id="a9873-114">This section lists the procedures required to install and configure the Security Development Tool.</span></span>

### <a name="install-the-tool"></a><span data-ttu-id="a9873-115">ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="a9873-115">Install the tool</span></span>

1.  <span data-ttu-id="a9873-116">SecurityDevelopmentTool.msi フォームを「[Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com)」の Downloadable ツールからダウンロードします (Microsoft のアカウントでログインする場合のみ Downloadable ツールはアクセス可能です。組織アカウントでサインインすると表示されませんので注意してください)</span><span class="sxs-lookup"><span data-stu-id="a9873-116">Download the SecurityDevelopmentTool.msi from the Downloadable tools of [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (note that the Downloadable tools is only accessible if you log in to LCS with a Microsoft account; it will not be shown if you sign in with an organizational account)</span></span>
2.  <span data-ttu-id="a9873-117">**SecurityDevelopmentTool.msi** を実行して**インストール ウィザード**を開きます。</span><span class="sxs-lookup"><span data-stu-id="a9873-117">Run **SecurityDevelopmentTool.msi** to open the **Installation Wizard**.</span></span>
3.  <span data-ttu-id="a9873-118">Microsoft ソフトウェア ライセンス条件に同意し、**インストール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9873-118">Accept the Microsoft Software License Terms, and then click **Install**.</span></span>
4.  <span data-ttu-id="a9873-119">ツールが正常にインストールされたことを示すメッセージが表示されたら、**完了** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9873-119">When a message indicates that the tool has been successfully installed, click **Finish**.</span></span> <span data-ttu-id="a9873-120">**インストール** **ウィザード**の実行が完了すると、ファイルは次の場所で使用できます。</span><span class="sxs-lookup"><span data-stu-id="a9873-120">After the **Installation** **Wizard** has finished running, the files are available at the following locations:</span></span>
    -   <span data-ttu-id="a9873-121">64 ビット システム用: %ProgramFiles (x86)%Microsoft%Security 開発ツール</span><span class="sxs-lookup"><span data-stu-id="a9873-121">For 64-bit systems: %ProgramFiles (x86)%Microsoft%Security Development Tool</span></span>
    -   <span data-ttu-id="a9873-122">32 ビット システム用: %ProgramFiles%Microsoft%Security 開発ツール</span><span class="sxs-lookup"><span data-stu-id="a9873-122">For 32-bit systems: %ProgramFiles%Microsoft%Security Development Tool</span></span>

### <a name="import-and-compile-the-tool"></a><span data-ttu-id="a9873-123">ツールのインポートおよびコンパイル</span><span class="sxs-lookup"><span data-stu-id="a9873-123">Import and compile the tool</span></span>

1.  <span data-ttu-id="a9873-124">使用している Application Object Server (AOS) のインスタンスからクライアント接続を排除します。</span><span class="sxs-lookup"><span data-stu-id="a9873-124">Drain the client connections from the instance of Application Object Server (AOS) that you are working with.</span></span> <span data-ttu-id="a9873-125">詳細については、[AOS からユーザーを排除](http://technet.microsoft.com/en-us/library/hh433538.aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9873-125">For more information, see [Drain users from an AOS](http://technet.microsoft.com/en-us/library/hh433538.aspx).</span></span>
2.  <span data-ttu-id="a9873-126">**管理ツール**に移動し、**サービス**をクリックし、**Microsoft Dynamics AX Object Server 6.0** サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="a9873-126">Go to **Administrative Tools**, click **Services**, and stop the **Microsoft Dynamics AX Object Server 6.0** service.</span></span>
3.  <span data-ttu-id="a9873-127">Windows PowerShell または AXUtil を使用して、**SecurityDevelopmentTool.axmodel** モデルを Microsoft Dynamics AX AOT にインポートします。</span><span class="sxs-lookup"><span data-stu-id="a9873-127">Use Windows PowerShell or AXUtil to import the **SecurityDevelopmentTool.axmodel** model into the Microsoft Dynamics AX AOT.</span></span>
    1.  <span data-ttu-id="a9873-128">スタートメニューで、**すべてのプログラム**をポイントし、**管理ツール**をポイントして、**Microsoft Dynamics AX 管理シェル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9873-128">On the Start menu, point to **All Programs**, point to **Administrative Tools**, and then click **Microsoft Dynamics AX Management Shell**.</span></span>
    2.  <span data-ttu-id="a9873-129">Windows PowerShell コマンド プロンプト PS C:&gt; で、次のコマンドを入力して Enter キーを押します。</span><span class="sxs-lookup"><span data-stu-id="a9873-129">At the Windows PowerShell command prompt, PS C:&gt;, type the following command, and then press Enter.</span></span>

            Install-AXModel -File “C:\Program Files (x86)\Microsoft\Security Development Tool\SecurityDevelopmentTool.axmodel”

        <span data-ttu-id="a9873-130">詳細については、「[方法: モデルのエクスポートとインポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a9873-130">For more information, see [How to: Export and Import a Model](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx).</span></span>

4.  <span data-ttu-id="a9873-131">Microsoft Dynamics AX Object Server 6.0 サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="a9873-131">Start the Microsoft Dynamics AX Object Server 6.0 service.</span></span>
5.  <span data-ttu-id="a9873-132">Microsoft Dynamics AX クライアントを起動します。</span><span class="sxs-lookup"><span data-stu-id="a9873-132">Start the Microsoft Dynamics AX client.</span></span> <span data-ttu-id="a9873-133">モデル ストアが変更されました。ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="a9873-133">The Model store has been modified dialog box opens.</span></span>
6.  <span data-ttu-id="a9873-134">**コンパイルして同期**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a9873-134">Click **Compile and Synchronize**.</span></span>
7.  <span data-ttu-id="a9873-135">同期が完了したときに、**Ctrl+Shift+W** を押して、開発ワークスペースを開きます。</span><span class="sxs-lookup"><span data-stu-id="a9873-135">When synchronization is completed, press **Ctrl+Shift+W** to open a Development workspace.</span></span>
8.  <span data-ttu-id="a9873-136">**SysSecEntryPointManagerSetup** クラスを実行して以下のメニュー項目を標準  Microsoft Dynamics AX メニューに追加します。</span><span class="sxs-lookup"><span data-stu-id="a9873-136">Run the **SysSecEntryPointManagerSetup** class to add the following menu items to the standard Microsoft Dynamics AX menus.</span></span>

    | <span data-ttu-id="a9873-137">メニュー項目</span><span class="sxs-lookup"><span data-stu-id="a9873-137">Menu item</span></span>                     | <span data-ttu-id="a9873-138">メニュー</span><span class="sxs-lookup"><span data-stu-id="a9873-138">Menu</span></span>                               |
    |-------------------------------|------------------------------------|
    | <span data-ttu-id="a9873-139">SysSecRoleEntryPointDeveloper</span><span class="sxs-lookup"><span data-stu-id="a9873-139">SysSecRoleEntryPointDeveloper</span></span> | <span data-ttu-id="a9873-140">SysContextMenu (AOT アドイン)</span><span class="sxs-lookup"><span data-stu-id="a9873-140">SysContextMenu (AOT Add-Ins)</span></span>       |
    | <span data-ttu-id="a9873-141">SysSecRoleEntryPoint</span><span class="sxs-lookup"><span data-stu-id="a9873-141">SysSecRoleEntryPoint</span></span>          | <span data-ttu-id="a9873-142">システム管理設定セキュリティ</span><span class="sxs-lookup"><span data-stu-id="a9873-142">System AdministrationSetupSecurity</span></span> |
