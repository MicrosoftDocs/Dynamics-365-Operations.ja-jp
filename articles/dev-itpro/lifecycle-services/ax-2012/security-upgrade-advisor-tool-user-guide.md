---
title: "セキュリティ アップグレード アドバイザー ツールのユーザー ガイド"
description: "Microsoft Dynamics AX Security Upgrade Advisor Tool を使用すると、以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 にセキュリティ設定をアップグレードするプロセスを簡略化できます。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: 
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012
ms.custom: 30061
ms.assetid: fda4d8e9-79a2-4ee2-831e-a90a9df2d980
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 6d5545580168dcd8fb335b6ebd4ac7ace11d83e2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="security-upgrade-advisor-tool-user-guide"></a><span data-ttu-id="98308-103">セキュリティ アップグレード アドバイザー ツールのユーザー ガイド</span><span class="sxs-lookup"><span data-stu-id="98308-103">Security Upgrade Advisor Tool user guide</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98308-104">Microsoft Dynamics AX Security Upgrade Advisor Tool を使用すると、以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 にセキュリティ設定をアップグレードするプロセスを簡略化できます。</span><span class="sxs-lookup"><span data-stu-id="98308-104">The Microsoft Dynamics AX Security Upgrade Advisor Tool is intended to help simplify the process of upgrading security settings from earlier versions of Microsoft Dynamics AX to Microsoft Dynamics AX 2012.</span></span> 

> [!NOTE]
> <span data-ttu-id="98308-105">これは、予備的なプレリリース ドキュメントで、予告なしに変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="98308-105">This is pre-release documentation of a preliminary nature and is subject to change at any time without notice.</span></span> <span data-ttu-id="98308-106">ここで提供されている情報の正確さは保障されていません。</span><span class="sxs-lookup"><span data-stu-id="98308-106">Microsoft cannot guarantee the accuracy of any information provided herein.</span></span>

<span data-ttu-id="98308-107">セキュリティ アップグレード アドバイザー ツールは、システム間でエントリ ポイントとアクセス許可を比較し、特定のロールのために使用できる一致する特権の一覧を生成します。</span><span class="sxs-lookup"><span data-stu-id="98308-107">The Security Upgrade Advisor Tool compares entry points and permissions between systems, and generates a list of matching privileges that can be used for a particular role.</span></span> <span data-ttu-id="98308-108">ロールから権限へのマッピングは、以前のバージョンの Microsoft Dynamics AX システムでの、ユーザー グループからアクセスへの正しいマッピングに基づいています。</span><span class="sxs-lookup"><span data-stu-id="98308-108">The role-to-privilege mapping is based on the user group–to–access right mapping in earlier versions of Microsoft Dynamics AX systems.</span></span> <span data-ttu-id="98308-109">このツールは、セキュリティ設定をアップグレードするためのもので、ワンクリック ソリューションではありません。</span><span class="sxs-lookup"><span data-stu-id="98308-109">The tool is designed as an aid for upgrading security settings and is not a one-click solution.</span></span> <span data-ttu-id="98308-110">開発者は、変更を行う前に各提案を慎重に検討することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-110">Developers are advised to review each suggestion carefully before making any changes.</span></span> <span data-ttu-id="98308-111">生成される提案のリストは、次の基準に基づいています。</span><span class="sxs-lookup"><span data-stu-id="98308-111">The list of suggestions generated is based on the following criteria:</span></span>

1.  <span data-ttu-id="98308-112">エントリ ポイントの名前、タイプ、アクセス権は、以前のバージョンの Microsoft Dynamics AX と Microsoft Dynamics AX 2012 との間で正確に一致します。</span><span class="sxs-lookup"><span data-stu-id="98308-112">The entry point name, type, and access right are exactly matched between earlier versions of Microsoft Dynamics AX and Microsoft Dynamics AX 2012.</span></span>
2.  <span data-ttu-id="98308-113">エントリ ポイントの名前とタイプは完全に一致しています。</span><span class="sxs-lookup"><span data-stu-id="98308-113">The entry point name and type are exactly matched.</span></span> <span data-ttu-id="98308-114">ただし、アクセス権に関しては、完全な一致が見つからない場合、類似した一致候補が生成されます。</span><span class="sxs-lookup"><span data-stu-id="98308-114">However, for an access right, if an exact match is not found, a similar match suggestion is generated.</span></span> <span data-ttu-id="98308-115">以前のバージョンの Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の両方でビューよりも大きいアクセス権は、潜在的な一致とみなされます。</span><span class="sxs-lookup"><span data-stu-id="98308-115">Any access right that is greater than View in both the earlier versions of Microsoft Dynamics AX and Microsoft Dynamics AX 2012 is considered a potential match.</span></span>

## <a name="assumptions"></a><span data-ttu-id="98308-116">前提</span><span class="sxs-lookup"><span data-stu-id="98308-116">Assumptions</span></span>
<span data-ttu-id="98308-117">このツールを使用する前に、次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-117">Before you use the tool, we assume that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="98308-118">Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の以前のバージョンの開発環境を使い慣れています。</span><span class="sxs-lookup"><span data-stu-id="98308-118">You are familiar with development environments in earlier versions of Microsoft Dynamics AX and Microsoft Dynamics AX 2012.</span></span>
-   <span data-ttu-id="98308-119">Microsoft Dynamics AX および Microsoft Dynamics AX 2012 の以前のバージョンのセキュリティ モデルを使い慣れています。</span><span class="sxs-lookup"><span data-stu-id="98308-119">You are familiar with the security model in earlier versions of Microsoft Dynamics AX and Microsoft Dynamics AX 2012.</span></span>
-   <span data-ttu-id="98308-120">Microsoft Dynamics AX の開発者権限を持っている場合、アプリケーション オブジェクト ツリー (AOT) からツールを実行できるようにします。</span><span class="sxs-lookup"><span data-stu-id="98308-120">You have developer privileges in Microsoft Dynamics AX, so that you can run the tool from the Application Object Tree (AOT).</span></span>
-   <span data-ttu-id="98308-121">コードのアップグレードおよびデータのアップグレードが完了しました。</span><span class="sxs-lookup"><span data-stu-id="98308-121">You have completed the code upgrade and data upgrade.</span></span> <span data-ttu-id="98308-122">セキュリティ アップグレード アドバイザー ツールはいつでも実行できますが、コード アップグレードの後に実行すると、コンポーネントを以前のバージョンの Microsoft Dynamics AX から持ち越すことができます。</span><span class="sxs-lookup"><span data-stu-id="98308-122">The Security Upgrade Advisor Tool can be run at any time, but running it after a code upgrade enables artifacts to be carried over from earlier versions of Microsoft Dynamics AX.</span></span>

## <a name="install-the-tool"></a><span data-ttu-id="98308-123">ツールのインストール</span><span class="sxs-lookup"><span data-stu-id="98308-123">Install the tool</span></span>
1.  <span data-ttu-id="98308-124">**SecurityUpgradeAdvisorTool.msi** を実行して**インストール ウィザード**を開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-124">Run **SecurityUpgradeAdvisorTool.msi** to open the **Installation Wizard**.</span></span>
2.  <span data-ttu-id="98308-125">使用許諾契約書に同意し、**インストール**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98308-125">Accept the License Agreement, and then click **Install**.</span></span>
3.  <span data-ttu-id="98308-126">**完了**をクリックしてインストールを完了します。</span><span class="sxs-lookup"><span data-stu-id="98308-126">Click **Finish** to complete the installation.</span></span> <span data-ttu-id="98308-127">**インストール ウィザード**の実行が完了すると、ファイルは、x64 システム - %ProgramFiles(x86)%MicrosoftSecurity アップグレード アドバイザー Toolx32 システム - %ProgramFiles%MicrosoftSecurity アップグレード アドバイザー ツールで使用可能です</span><span class="sxs-lookup"><span data-stu-id="98308-127">After the **Installation Wizard** has finished running, the files are available at: x64 systems - %ProgramFiles(x86)%MicrosoftSecurity Upgrade Advisor Toolx32 systems - %ProgramFiles%MicrosoftSecurity Upgrade Advisor Tool</span></span>

## <a name="before-running-the-tool"></a><span data-ttu-id="98308-128">ツールを実行する前に</span><span class="sxs-lookup"><span data-stu-id="98308-128">Before running the tool</span></span>
<span data-ttu-id="98308-129">このツールを実行する前に、以下の点を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-129">Before you run the tool, here are few things that you should consider:</span></span>

-   <span data-ttu-id="98308-130">ソース管理: ソース管理が有効な場合、ツールはロールと特権の生成をサポートしません。</span><span class="sxs-lookup"><span data-stu-id="98308-130">Source Control: The tool does not support generating roles and privileges when source control is enabled.</span></span>
-   <span data-ttu-id="98308-131">モデル: モデルですべてのセキュリティ アップグレード タスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="98308-131">Model: Perform all security upgrade tasks in a model.</span></span> <span data-ttu-id="98308-132">これにより、新しく生成された設定を新しい環境に柔軟にエクスポートできます。</span><span class="sxs-lookup"><span data-stu-id="98308-132">This provides the flexibility to export your newly generated settings to new environments.</span></span> <span data-ttu-id="98308-133">また、これにより、設定をクリーンアップおよび再生成する必要がある場合に、全体の設定を削除することもできます。</span><span class="sxs-lookup"><span data-stu-id="98308-133">It also lets you delete the whole setting if you have to clean up and regenerate settings.</span></span>
-   <span data-ttu-id="98308-134">テスト: ツールは、Microsoft Dynamics AX の以前のバージョンからのセキュリティ設定に基づいてセキュリティ コンポーネントを生成します。</span><span class="sxs-lookup"><span data-stu-id="98308-134">Testing: The tool generates security artifacts based on security settings from earlier versions of Microsoft Dynamics AX.</span></span> <span data-ttu-id="98308-135">各設定の確認、調整、およびテストを繰り返して、生成された設定が目的の設定になっていることを確認することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-135">We recommend that you iteratively review, fine-tune, and test each setting to make sure that the generated settings are the ones intended.</span></span>

## <a name="running-the-tool"></a><span data-ttu-id="98308-136">ツールを実行中</span><span class="sxs-lookup"><span data-stu-id="98308-136">Running the tool</span></span>
<span data-ttu-id="98308-137">次の手順では、セキュリティ アップグレード アドバイザー ツールの実行時に従う必要があるプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="98308-137">The following procedures describe the process you should follow when running the Security Upgrade Advisor Tool.</span></span>

### <a name="export-security-settings-from-an-environment-running-an-earlier-version-of-microsoft-dynamics-ax"></a><span data-ttu-id="98308-138">Microsoft Dynamics AX の以前のバージョンを実行している環境から、セキュリティ設定をエクスポート</span><span class="sxs-lookup"><span data-stu-id="98308-138">Export security settings from an environment running an earlier version of Microsoft Dynamics AX</span></span>

1.  <span data-ttu-id="98308-139">Microsoft Dynamics AX の以前のバージョンを実行している環境で、次の XPO をインポートします: **Job\_ExportSecuritySettingsBulk.xpo**。</span><span class="sxs-lookup"><span data-stu-id="98308-139">In the environment that is running an earlier version of Microsoft Dynamics AX, import the following XPO: **Job\_ExportSecuritySettingsBulk.xpo**.</span></span>
2.  <span data-ttu-id="98308-140">X++ ジョブ **ExportSecuritySettingsBuild** を実行します。</span><span class="sxs-lookup"><span data-stu-id="98308-140">Execute the X++ job **ExportSecuritySettingsBuild**.</span></span>
3.  <span data-ttu-id="98308-141">メッセージが表示されたら、保存するファイルの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="98308-141">When prompted, enter the name of the file to save.</span></span>
4.  <span data-ttu-id="98308-142">ファイルを既知の場所にエクスポートして、後で取得します。</span><span class="sxs-lookup"><span data-stu-id="98308-142">Export the file to a known location for later retrieval.</span></span>

### <a name="run-the-security-upgrade-wizard-in-microsoft-dynamics-ax-2012"></a><span data-ttu-id="98308-143">Microsoft Dynamics AX 2012 でセキュリティ アップグレード ウィザードを実行</span><span class="sxs-lookup"><span data-stu-id="98308-143">Run the Security Upgrade Wizard in Microsoft Dynamics AX 2012</span></span>

<span data-ttu-id="98308-144">ウィザードの出力は、指定した接頭語で名前が付けられた AOT のカスタム ロールです。</span><span class="sxs-lookup"><span data-stu-id="98308-144">The outputs of the wizard are custom roles in the AOT, named with a prefix that you specify.</span></span> <span data-ttu-id="98308-145">ユーザーはこれらのロールに自動的に割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="98308-145">No users are assigned to these roles automatically.</span></span> <span data-ttu-id="98308-146">ロールが生成されると、各ユーザーにロールを手動で割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-146">After roles are generated, you must manually assign roles to each user.</span></span> <span data-ttu-id="98308-147">**次へ**をクリックすると、ウィザードの各ステップを実行します。</span><span class="sxs-lookup"><span data-stu-id="98308-147">Clicking **Next** runs each step of the wizard.</span></span> <span data-ttu-id="98308-148">**キャンセル**をクリックすると、ウィザードが閉じます。</span><span class="sxs-lookup"><span data-stu-id="98308-148">Clicking **Cancel** closes the wizard.</span></span>

1. <span data-ttu-id="98308-149">使用している Application Object Server (AOS) のインスタンスに接続されているクライアント接続を排除します。</span><span class="sxs-lookup"><span data-stu-id="98308-149">Drain the client connections that are connected to the instance of Application Object Server (AOS) that you are working with.</span></span> <span data-ttu-id="98308-150">詳細については、[AOS からユーザーを排除](http://technet.microsoft.com/library/d19bd816-cd9e-423a-94c7-aceb946baa30(AX.60).aspx) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98308-150">For more information, see [Drain users from an AOS](http://technet.microsoft.com/library/d19bd816-cd9e-423a-94c7-aceb946baa30(AX.60).aspx).</span></span>
2. <span data-ttu-id="98308-151">**管理ツール** &gt; **サービス**で、**Microsoft Dynamics AX Object Server 6.0** サービスを停止します。</span><span class="sxs-lookup"><span data-stu-id="98308-151">In **Administrative Tools** &gt; **Services**, stop the **Microsoft Dynamics AX Object Server 6.0** service.</span></span>
3. <span data-ttu-id="98308-152">Windows PowerShell または AXUtil を使用して、**SecurityUpgradeAdvisorTool.axmodel** モデルを Microsoft Dynamics AX 2012 AOT にインポートします。</span><span class="sxs-lookup"><span data-stu-id="98308-152">Use Windows PowerShell or AXUtil to import the model **SecurityUpgradeAdvisorTool.axmodel** into the Microsoft Dynamics AX 2012 AOT.</span></span>

       Install-AXModel -File SecurityUpgradeAdvisorTool.axmodel -Details

   <span data-ttu-id="98308-153">詳細については、「[方法: モデルのエクスポートとインポート](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="98308-153">For more information, see [How to: Export and Import a Model](http://msdn.microsoft.com/library/c2449a03-7574-4b9d-8518-9005b560209f(AX.60).aspx).</span></span>

4. <span data-ttu-id="98308-154">**Microsoft Dynamics AX Object Server 6.0** サービスを開始します。</span><span class="sxs-lookup"><span data-stu-id="98308-154">Start the **Microsoft Dynamics AX Object Server 6.0** service.</span></span>
5. <span data-ttu-id="98308-155">Security Upgrade Advisor プロジェクトを開いて、<strong>フォーム</strong>&gt;<strong>SecurityUpgradeWizard</strong> フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-155">Open the Security Upgrade Advisor project, and open the <strong>Forms</strong> &gt; <strong>SecurityUpgradeWizard</strong> form.</span></span>
  > [!IMPORTANT]
  > <span data-ttu-id="98308-156">プロジェクトをコンパイルして、AOT の オブジェクト グループ **UpgradeAdvisorTool** および **PrivelegeGenerationTool** にあるすべてのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="98308-156">Compile the project and synchronize all tables in the object groups **UpgradeAdvisorTool** and **PrivelegeGenerationTool** in the AOT.</span></span>
6. <span data-ttu-id="98308-157">**次へ**をクリックし、**ステップ１インポートの設定**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-157">Click **Next** to open the **Step 1 Import Settings** page.</span></span> <span data-ttu-id="98308-158">このステップでは、以前のバージョンの Microsoft Dynamics AX からエクスポートされたセキュリティ情報の .xml ファイルを Microsoft Dynamics AX 2012 の一時テーブルにインポートします。</span><span class="sxs-lookup"><span data-stu-id="98308-158">This step imports the .xml file of security information exported from an earlier version of Microsoft Dynamics AX into temp tables in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="98308-159">このステップでは、前のセクションで生成されたファイルを使用します。</span><span class="sxs-lookup"><span data-stu-id="98308-159">This step uses the file generated in the previous section.</span></span>
7. <span data-ttu-id="98308-160">**次へ**をクリックし、**ステップ 2 権限の一致を検索**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-160">Click **Next** to open the **Step 2 Find Privilege Matches** page.</span></span> <span data-ttu-id="98308-161">このステップでは、既存のセキュリティ設定を繰り返し、Microsoft Dynamics AX 2012 で一致するエントリ ポイントとアクセス許可を検出します。</span><span class="sxs-lookup"><span data-stu-id="98308-161">This step iterates through the existing security settings, and finds matching entry points and permissions in Microsoft Dynamics AX 2012.</span></span>
8. <span data-ttu-id="98308-162">**次へ**をクリックし、**ステップ 3 ユーザー グループをカスタムロールにマップ** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-162">Click **Next** to open the **Step 3 Map User Groups to Custom Roles** page.</span></span> <span data-ttu-id="98308-163">このステップでは、検出された権限の新しいカスタム ロール マッピングが生成されます。</span><span class="sxs-lookup"><span data-stu-id="98308-163">This step generates new custom role mappings for the privileges that were found.</span></span>
9. <span data-ttu-id="98308-164">**次へ**をクリックし、**ステップ 4 セキュリティ アップグレード提案のエクスポート** ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-164">Click **Next** to open the **Step 4 Export Security Upgrade Suggestions** page.</span></span> <span data-ttu-id="98308-165">このステップは、すべてのマッピングを一時テーブルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="98308-165">This step exports all the mappings to a temporary table.</span></span>
10. <span data-ttu-id="98308-166">**次へ**をクリックし、**ステップ 5 セキュリティ アップグレード提案**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-166">Click **Next** to open the **Step 5 Security Upgrade Suggestions** page.</span></span> <span data-ttu-id="98308-167">このウィザードのページには推奨されるセキュリティ マッピングが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98308-167">This page of the wizard displays the suggested security mappings.</span></span> 
  > [!IMPORTANT]
  > <span data-ttu-id="98308-168">追加の分析のアップグレードの提案をエクスポートすることを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-168">We strongly recommend that you export the upgrade suggestions for additional analysis.</span></span> <span data-ttu-id="98308-169">Ctrl + T を押すことで、追加分析のためにデータを Microsoft Excel にコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="98308-169">You can copy and paste the data into Microsoft Excel for additional analysis by pressing Ctrl+T.</span></span> <span data-ttu-id="98308-170">推奨される設定を分析する方法の詳細については、次のセクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98308-170">For more information about how to analyze the suggested settings, see the next section.</span></span>
11. <span data-ttu-id="98308-171">セキュリティ アップグレード提案の解析中に **NoMatchingPrivilege** ステータスを持つ複数の品目がある場合、権限生成ツールを実行できます。</span><span class="sxs-lookup"><span data-stu-id="98308-171">If, during your analysis of the security upgrade suggestions, you notice multiple items that have the **NoMatchingPrivilege** status, you may want to run the Privilege Generation Tool.</span></span> <span data-ttu-id="98308-172">**特権の生成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98308-172">Click **Generate Privileges**.</span></span>
12. <span data-ttu-id="98308-173">**次へ**をクリックし、**ステップ 6 カスタム ロール生成オプションの指定**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-173">Click **Next** to open the **Step 6 Specify Custom Role Generation Options** page.</span></span> <span data-ttu-id="98308-174">この手順では、AOT 内でのロールを生成するためのオプションを指定できます。</span><span class="sxs-lookup"><span data-stu-id="98308-174">In this step, you can specify options for generating roles in the AOT:</span></span>
    -   <span data-ttu-id="98308-175">**類似**ステータスに一致する特権を使用し、カスタム ロールに追加するには、カスタム ロールで**類似する一致を含める**を選択します。</span><span class="sxs-lookup"><span data-stu-id="98308-175">Select **Include similar matches** in the custom role to use privileges that match with **Similar** status, and to add them to the custom role.</span></span>
    -   <span data-ttu-id="98308-176">**カスタム ロール名の省略可能な接頭語**フィールドに、新しいロールの接頭語を入力します。</span><span class="sxs-lookup"><span data-stu-id="98308-176">In the **Optional prefix for custom role name** field, enter a prefix for the new role.</span></span> <span data-ttu-id="98308-177">AOT でのロールを後で簡単に識別するのに役立つ接頭語を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-177">We recommend that you use a prefix that helps you easily identify roles in the AOT later.</span></span> <span data-ttu-id="98308-178">Microsoft Dynamics AX 2009 システムにドメインがある場合は、別のドメインにある類似したユーザー グループの名前を区別するために、ロールの前にドメイン名を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="98308-178">If your Microsoft Dynamics AX 2009 system had domains, you can prefix the domain name to the role to distinguish between similar user group names in different domains.</span></span>

13. <span data-ttu-id="98308-179">**完了**をクリックし、ウィザードを終了します。</span><span class="sxs-lookup"><span data-stu-id="98308-179">Click **Finish** to exit the wizard.</span></span>

<span data-ttu-id="98308-180">ウィザードの実行が完了したら、推奨されるセキュリティ マッピングに基づいたカスタムのロールを AOT 内で使用できます。</span><span class="sxs-lookup"><span data-stu-id="98308-180">When the wizard has finished running, custom roles based on the suggested security mappings are available in the AOT.</span></span> <span data-ttu-id="98308-181">生成されたのカスタム ロールを確認し、反復テストと調整プロセスに従ってセキュリティ設定を微調整することを強くお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-181">We strongly recommend that you review the generated custom roles, and follow an iterative testing and refinement process to fine-tune your security settings.</span></span>

## <a name="analyzing-upgrade-suggestions"></a><span data-ttu-id="98308-182">アップグレード提案の分析</span><span class="sxs-lookup"><span data-stu-id="98308-182">Analyzing upgrade suggestions</span></span>
<span data-ttu-id="98308-183">セキュリティ アップグレード アドバイザー ツールの手順 5 で生成される結果は、すべてのロール、エントリポイント、権限、一致する権限の一覧です。</span><span class="sxs-lookup"><span data-stu-id="98308-183">The result generated by step 5 of the Security Upgrade Advisor Tool is a list of all roles, entry points, permissions, and matching privileges.</span></span> <span data-ttu-id="98308-184">これは次の列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="98308-184">It contains the following columns.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98308-185">列</span><span class="sxs-lookup"><span data-stu-id="98308-185">Columns</span></span></th>
<th><span data-ttu-id="98308-186">説明</span><span class="sxs-lookup"><span data-stu-id="98308-186">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98308-187"><span class="ui">ドメイン</span></span><span class="sxs-lookup"><span data-stu-id="98308-187"><span class="ui">Domain</span></span></span></td>
<td><span data-ttu-id="98308-188">Microsoft Dynamics AX 2009 からインポートされたドメイン名。</span><span class="sxs-lookup"><span data-stu-id="98308-188">The domain names imported from Microsoft Dynamics AX 2009.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-189"><span class="ui">役割</span></span><span class="sxs-lookup"><span data-stu-id="98308-189"><span class="ui">Role</span></span></span></td>
<td><span data-ttu-id="98308-190">Microsoft Dynamics AX 2009 からインポートされたユーザー グループ名。</span><span class="sxs-lookup"><span data-stu-id="98308-190">The user group names imported from Microsoft Dynamics AX 2009.</span></span> <span data-ttu-id="98308-191">列内のデータは、特殊文字を削除するようにフォーマットされています。</span><span class="sxs-lookup"><span data-stu-id="98308-191">Data in the column has been formatted to remove any special characters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-192"><span class="ui">権限</span></span><span class="sxs-lookup"><span data-stu-id="98308-192"><span class="ui">Privilege</span></span></span></td>
<td><span data-ttu-id="98308-193">Microsoft Dynamics AX 2012 での一致する権限。</span><span class="sxs-lookup"><span data-stu-id="98308-193">The matching privileges in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="98308-194">この列には、<strong><span class="ui">ステータス</span></strong>列の値が<strong><span class="ui">完全一致</span></strong>または<strong><span class="ui">類似</span></strong>の場合にのみ値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98308-194">This column contains values only if the value in the <strong><span class="ui">Status</span></strong> column is <strong><span class="ui">Exact</span></strong> or <strong><span class="ui">Similar</span></strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-195"><span class="ui">エントリ ポイント 名</span></span><span class="sxs-lookup"><span data-stu-id="98308-195"><span class="ui">Entry Point Name</span></span></span></td>
<td><span data-ttu-id="98308-196">Microsoft Dynamics AX 2009 からインポートされたエントリ ポイント名。</span><span class="sxs-lookup"><span data-stu-id="98308-196">The entry point names imported from Microsoft Dynamics AX 2009.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-197"><span class="ui">新規エントリ ポイント名</span></span><span class="sxs-lookup"><span data-stu-id="98308-197"><span class="ui">New Entry Point Name</span></span></span></td>
<td><span data-ttu-id="98308-198">エントリ ポイントが以前のバージョンの Microsoft Dynamics AX から Microsoft Dynamics AX 2012 に変更されている場合、スクリプトは、自動的に、新しいエントリ ポイント名に基づく特権をマップし、新しい名前でこの列に値を設定します。</span><span class="sxs-lookup"><span data-stu-id="98308-198">If entry points were renamed from earlier versions of Microsoft Dynamics AX to Microsoft Dynamics AX 2012, the script automatically maps privileges based on the new entry point names, and populates this column with the new name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-199"><span class="ui">エントリ ポイント タイプ</span></span><span class="sxs-lookup"><span data-stu-id="98308-199"><span class="ui">Entry Point Type</span></span></span></td>
<td><span data-ttu-id="98308-200">エントリ ポイントのタイプ</span><span class="sxs-lookup"><span data-stu-id="98308-200">The entry point types.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-201"><span class="ui">エントリ ポイント アクセス権限</span></span><span class="sxs-lookup"><span data-stu-id="98308-201"><span class="ui">Entry Point Access Rights</span></span></span></td>
<td><span data-ttu-id="98308-202">Microsoft Dynamics AX 2012 で一致するエントリ ポイントのアクセス許可。</span><span class="sxs-lookup"><span data-stu-id="98308-202">The matching entry point permissions in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="98308-203">この列には、<strong><span class="ui">ステータス</span></strong>列の値が<strong><span class="ui">完全一致</span></strong>または<strong><span class="ui">類似</span></strong>の場合にのみ値が含まれます。</span><span class="sxs-lookup"><span data-stu-id="98308-203">This column contains values only if the value in the <strong><span class="ui">Status</span></strong> column is <strong><span class="ui">Exact</span></strong> or <strong><span class="ui">Similar</span></strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-204"><span class="ui">エントリ ポイント 旧アクセス権限</span></span><span class="sxs-lookup"><span data-stu-id="98308-204"><span class="ui">Entry Point Old Access Rights</span></span></span></td>
<td><span data-ttu-id="98308-205">Microsoft Dynamics AX 2009 で設定されたエントリポイントの権限。</span><span class="sxs-lookup"><span data-stu-id="98308-205">The entry point rights that were configured in Microsoft Dynamics AX 2009.</span></span> <span data-ttu-id="98308-206">この列は参照用に追加されています。</span><span class="sxs-lookup"><span data-stu-id="98308-206">This column is added for reference.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-207"><span class="ui">ステータス</span></span><span class="sxs-lookup"><span data-stu-id="98308-207"><span class="ui">Status</span></span></span></td>
<td><span data-ttu-id="98308-208">各エントリ ポイントの状態が一致します。</span><span class="sxs-lookup"><span data-stu-id="98308-208">The status for each entry point match.</span></span> <span data-ttu-id="98308-209">このツールでは、次のステータスが生成されます。</span><span class="sxs-lookup"><span data-stu-id="98308-209">The following statuses are generated by the tool:</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98308-210"><span class="ui">正確</span></span><span class="sxs-lookup"><span data-stu-id="98308-210"><span class="ui">Exact</span></span></span></td>
<td><span data-ttu-id="98308-211">エントリポイント、タイプ、アクセス権は、Microsoft Dynamics AX 2012 の権限と完全に一致します。</span><span class="sxs-lookup"><span data-stu-id="98308-211">The entry point, type, and access right exactly match a privilege in Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="98308-212">提案された特権は、Microsoft Dynamics AX 2012 の同様のセキュリティ設定の指定された役割で使用できます。</span><span class="sxs-lookup"><span data-stu-id="98308-212">The suggested privilege can be used in the specified role for similar security settings in Microsoft Dynamics AX 2012.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-213"><span class="ui">類似</span></span><span class="sxs-lookup"><span data-stu-id="98308-213"><span class="ui">Similar</span></span></span></td>
<td><span data-ttu-id="98308-214">エントリ ポイントとタイプは正確に一致しますが、アクセス権の完全一致は見つかりませんでした。</span><span class="sxs-lookup"><span data-stu-id="98308-214">The entry point and type match exactly, but no exact match for an access right was found.</span></span> <span data-ttu-id="98308-215">ただし、古いアクセス権および新しいアクセス権の両方に<strong>表示</strong>より大きいアクセス許可があるため、一致する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="98308-215">However, there is a potential match, because both the old and new access rights have permissions greater than <strong>View</strong>.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="98308-216"><strong>重要</strong></span><span class="sxs-lookup"><span data-stu-id="98308-216"><strong>Important</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="98308-217">開発者と管理者はこれらの行を確認し、提案された権限が目的のセキュリティ結果と一致することを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-217">The developer and administrator should review these rows, and make sure that the suggested privileges match the intended security outcome.</span></span></td>
</tr>
</tbody>
</table></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-218"><span class="ui">NoEntryPoint</span></span><span class="sxs-lookup"><span data-stu-id="98308-218"><span class="ui">NoEntryPoint</span></span></span></td>
<td><span data-ttu-id="98308-219">以前のバージョンの Microsoft Dynamics AX と Microsoft Dynamics AX 2012 には、一致するエントリ ポイントとタイプがありませんでした。</span><span class="sxs-lookup"><span data-stu-id="98308-219">There were no matching entry point and type between earlier versions of Microsoft Dynamics AX and Microsoft Dynamics AX 2012.</span></span> <span data-ttu-id="98308-220">見つからない品目には、マッピングの手動エントリ ポイントを実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-220">A manual entry point mapping must be performed for items that are not found.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="98308-221"><span class="ui">NoMatchingPrivilege</span></span><span class="sxs-lookup"><span data-stu-id="98308-221"><span class="ui">NoMatchingPrivilege</span></span></span></td>
<td><span data-ttu-id="98308-222">Microsoft Dynamics AX 2012 にてエントリ ポイントが見つかった場合でも、アクセス権に任意の条件が一致しませんでした。</span><span class="sxs-lookup"><span data-stu-id="98308-222">Even though an entry point was found in Microsoft Dynamics AX 2012, the access right did not match any criteria.</span></span> <span data-ttu-id="98308-223">アクセス権限の手動マッピングが必要になるか、権限生成ツールを使用して権限を生成することができます。</span><span class="sxs-lookup"><span data-stu-id="98308-223">A manual access right mapping might be required, or it may be possible to generate a privilege by using the Privilege Generation Tool.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="98308-224"><span class="ui">非推奨</span></span><span class="sxs-lookup"><span data-stu-id="98308-224"><span class="ui">Deprecated</span></span></span></td>
<td><span data-ttu-id="98308-225">Microsoft Dynamics AX 2012 からエントリ ポイントが削除されました。</span><span class="sxs-lookup"><span data-stu-id="98308-225">The entry point has been removed from Microsoft Dynamics AX 2012.</span></span></td>
</tr>
</tbody>
</table></td>
</tr>
</tbody>
</table>

## <a name="privilege-generation-tool"></a><span data-ttu-id="98308-226">特権生成ツール</span><span class="sxs-lookup"><span data-stu-id="98308-226">Privilege Generation Tool</span></span>
<span data-ttu-id="98308-227">特権生成ツールは、セキュリティ アップグレード アドバイザー ツールに組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="98308-227">The Privilege Generation Tool is included as part of the Security Upgrade Advisor Tool.</span></span> <span data-ttu-id="98308-228">カスタム エントリ ポイントに特権がなく、関連するアクセス権が定義されていないシナリオが多数あります。</span><span class="sxs-lookup"><span data-stu-id="98308-228">There are many scenarios where custom entry points may not have a privilege and associated access right defined.</span></span> <span data-ttu-id="98308-229">ベスト プラクティスは、権限をエントリ ポイントに関連付けることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-229">As a best practice, we recommend that a privilege be associated with an entry point.</span></span> <span data-ttu-id="98308-230">権限が事前に定義されていない場合、権限生成ツールはアップグレード プロセス中に自動的に権限を生成します。</span><span class="sxs-lookup"><span data-stu-id="98308-230">In cases where a privilege is not predefined, the Privilege Generation Tool can automatically generate privileges during the upgrade process.</span></span> <span data-ttu-id="98308-231">状態が **NoMatchingPrivilege** のすべてのエントリ ポイントに対して権限を生成するには、次の手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="98308-231">Use the following procedure to generate privileges for all entry points with a status of **NoMatchingPrivilege**.</span></span>

1.  <span data-ttu-id="98308-232">セキュリティ アップグレード ツールから、**手順 5 セキュリティ アップグレード提案ページで、権限の生成をクリックします**</span><span class="sxs-lookup"><span data-stu-id="98308-232">From the Security Upgrade Tool, on the **Step 5 Security Upgrade Suggestions page, click Generate Privileges**</span></span> 

       <span data-ttu-id="98308-233">- または -</span><span class="sxs-lookup"><span data-stu-id="98308-233">–or–</span></span>

       <span data-ttu-id="98308-234">AOT からの特権生成ツール フォームを、**PrivilegeGenerationTool** &gt; **フォーム** &gt; **SecurityUpgradePrivilegeGenerator** で開きます。</span><span class="sxs-lookup"><span data-stu-id="98308-234">Open the Privilege Generation Tool form from the AOT, under **PrivilegeGenerationTool** &gt; **Forms** &gt; **SecurityUpgradePrivilegeGenerator**.</span></span>
       
2.  <span data-ttu-id="98308-235">**ステップ １: 特権生成ウィザード**ページで、**次へ**をクリックし、ウィザードを開始します。</span><span class="sxs-lookup"><span data-stu-id="98308-235">On the **Step 1: Privilege Generation Wizard** page, click **Next** to start the wizard.</span></span>
3.  <span data-ttu-id="98308-236">手順 2 では、追加する省略可能な接頭語を指定し、生成された権限の名前に追加してから、**次へ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98308-236">In step 2, specify an optional prefix to add to the names of the generated privileges, and then click **Next**.</span></span>
4.  <span data-ttu-id="98308-237">手順 3 では、生成できるすべての特権が一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="98308-237">Step 3 lists all the privileges that can be generated.</span></span> <span data-ttu-id="98308-238">生成する特権ごとに **作成** を選択し、**次へ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98308-238">Select **Create** for each privilege that you want to generate, and then click **Next**.</span></span>
5.  <span data-ttu-id="98308-239">権限の生成が完了した後に、**完了**をクリックしてウィザードを閉じます。</span><span class="sxs-lookup"><span data-stu-id="98308-239">After privilege generation is completed, click **Finish** to close the wizard.</span></span>
6.  <span data-ttu-id="98308-240">AOT で、**セキュリティ**&gt;**権限**を確認して権限が正常に生成されたことを確認します。</span><span class="sxs-lookup"><span data-stu-id="98308-240">In the AOT, verify that the privileges were generated successfully by looking under **Security** &gt; **Privileges**.</span></span>
7.  <span data-ttu-id="98308-241">新しい権限を表示するように AOT を更新し、コンパイルして正しく生成されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="98308-241">Update the AOT to display the new privileges, and then compile them to make sure that they have been generated correctly.</span></span>
8.  <span data-ttu-id="98308-242">セキュリティ アップグレード アドバイザー ツールをもう一度実行します。</span><span class="sxs-lookup"><span data-stu-id="98308-242">Run the Security Upgrade Advisor Tool again.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98308-243">Microsoft Dynamics AX の以前のバージョンに **SysUtilElementsLog** メニュー項目がある場合は、特権が生成されると、コンパイル エラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98308-243">If you have the **SysUtilElementsLog** menu item from an earlier version of Microsoft Dynamics AX, it shows compile errors after privileges are generated.</span></span> <span data-ttu-id="98308-244">**SysUtilElementsLog** メニュー項目のタイプが Microsoft Dynamics AX 2012 での表示に変更されました。</span><span class="sxs-lookup"><span data-stu-id="98308-244">The type of the **SysUtilElementsLog** menu item has changed to Display in Microsoft Dynamics AX 2012.</span></span> 
> <span data-ttu-id="98308-245">**回避策:** この問題を回避するには、タイプを**表示**に変更し、権限に名前を再割り当てしてください。</span><span class="sxs-lookup"><span data-stu-id="98308-245">**Work Around:** To work around this issue, change the type to **Display**, and reassign the name to the privilege.</span></span> |

## <a name="frequently-asked-questions"></a><span data-ttu-id="98308-246">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="98308-246">Frequently asked questions</span></span>
### <a name="can-you-automatically-generate-role-definitions-from-excel"></a><span data-ttu-id="98308-247">Excel からロール定義を自動的に生成できますか。</span><span class="sxs-lookup"><span data-stu-id="98308-247">Can you automatically generate role definitions from Excel?</span></span>

<span data-ttu-id="98308-248">一連番号</span><span class="sxs-lookup"><span data-stu-id="98308-248">No.</span></span> <span data-ttu-id="98308-249">Excel のスプレッドシートを変更し、それらの設定を使用してロールを生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="98308-249">You cannot modify a spreadsheet in Excel and use those settings to generate roles.</span></span> <span data-ttu-id="98308-250">ただし、ツールを使用して、カスタム ロールおよび特権を生成できます。</span><span class="sxs-lookup"><span data-stu-id="98308-250">However, you can generate custom roles and privileges by using the tool.</span></span>

### <a name="what-happens-to-the-custom-menu-items-that-were-used-in-the-earlier-versions-of-microsoft-dynamics-ax"></a><span data-ttu-id="98308-251">Microsoft Dynamics AX の以前のバージョンで使用されていたカスタム メニュー項目はどうなったでしょうか ?</span><span class="sxs-lookup"><span data-stu-id="98308-251">What happens to the custom menu items that were used in the earlier versions of Microsoft Dynamics AX?</span></span>

<span data-ttu-id="98308-252">コードのアップグレードが完了したシステムでこのツールを実行するとき、Microsoft Dynamics AX 2012 システムでメニュー項目と一致するものを検索します。</span><span class="sxs-lookup"><span data-stu-id="98308-252">When you run this tool on a system that has finished a code upgrade, you find a match for the menu items in the Microsoft Dynamics AX 2012 system.</span></span> <span data-ttu-id="98308-253">ただし、それらに対する権限はありません。</span><span class="sxs-lookup"><span data-stu-id="98308-253">However, there are no privileges for them.</span></span> <span data-ttu-id="98308-254">適用可能と思われる場合は、新しい権限を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-254">You must create new privileges if you believe that they are applicable.</span></span>

### <a name="does-the-tool-consider-other-artifacts-such-as-tables-and-forms"></a><span data-ttu-id="98308-255">ツールは、テーブルやフォームなどの他のコンポーネントを考慮しますか。</span><span class="sxs-lookup"><span data-stu-id="98308-255">Does the tool consider other artifacts, such as tables and forms?</span></span>

<span data-ttu-id="98308-256">いいえ、このツールでは、メニュー項目などのエントリ ポイントのみが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="98308-256">No, the tool only considers entry points, such as menu items.</span></span> <span data-ttu-id="98308-257">Microsoft Dynamics AX 2012 のセキュリティ モデルでは、権限がアーティファクトへのアクセスを維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="98308-257">In the Microsoft Dynamics AX 2012 security model, privileges are used to maintain access to the artifacts.</span></span>

### <a name="are-the-user-groups-mapped-for-all-the-domains"></a><span data-ttu-id="98308-258">ユーザー グループは、すべてのドメインにマップされていますか。</span><span class="sxs-lookup"><span data-stu-id="98308-258">Are the user groups mapped for all the domains?</span></span>

<span data-ttu-id="98308-259">はい。</span><span class="sxs-lookup"><span data-stu-id="98308-259">Yes.</span></span> <span data-ttu-id="98308-260">結果は各ドメインとユーザーグループです。</span><span class="sxs-lookup"><span data-stu-id="98308-260">The results are for each domain and user group.</span></span> <span data-ttu-id="98308-261">Microsoft Dynamics AX 2012 の組織構造に基づいて、Microsoft Dynamics AX 2012 でロールを作成するユーザー グループとドメインの組み合わせを決定します。</span><span class="sxs-lookup"><span data-stu-id="98308-261">Based on your organizational structure in Microsoft Dynamics AX 2012, decide which user group/domain combinations you want to create roles for in Microsoft Dynamics AX 2012.</span></span>

### <a name="are-users-moved-as-part-of-the-security-upgrade"></a><span data-ttu-id="98308-262">ユーザーはセキュリティ アップグレードの一部として移動しますか。</span><span class="sxs-lookup"><span data-stu-id="98308-262">Are users moved as part of the security upgrade?</span></span>

<span data-ttu-id="98308-263">ユーザー情報は保存または移動されません。</span><span class="sxs-lookup"><span data-stu-id="98308-263">No user information is stored or moved.</span></span> <span data-ttu-id="98308-264">Microsoft Dynamics AX 2012 でロールを作成した後、ユーザー ロール マッピングを手動で作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98308-264">After the roles have been created in Microsoft Dynamics AX 2012, the user role mapping must be created manually.</span></span>

### <a name="are-record-level-security-settings-moved-as-part-of-the-security-upgrade"></a><span data-ttu-id="98308-265">レコード レベルのセキュリティ設定はセキュリティ アップグレードの一部として移動しますか。</span><span class="sxs-lookup"><span data-stu-id="98308-265">Are Record Level Security settings moved as part of the security upgrade?</span></span>

<span data-ttu-id="98308-266">アップグレードされるレコード レベルのセキュリティ (RLS) ルールはありません。</span><span class="sxs-lookup"><span data-stu-id="98308-266">No Record Level Security (RLS) rules are upgraded.</span></span> <span data-ttu-id="98308-267">Microsoft Dynamics AX 2012 には、拡張可能なデータ セキュリティ (XDS) と呼ばれる新しくより豊富なデータのセキュリティ メカニズムがあります。</span><span class="sxs-lookup"><span data-stu-id="98308-267">In Microsoft Dynamics AX 2012, there is a new and richer data security mechanism called Extensible Data Security (XDS).</span></span> <span data-ttu-id="98308-268">新しい XDS ポリシーを業務要件に基づいて作成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="98308-268">We recommend that you create new XDS policies based on your business requirements.</span></span>

### <a name="what-are-the-next-steps-to-complete-the-security-upgrade"></a><span data-ttu-id="98308-269">セキュリティのアップグレードを完了するための次の手順</span><span class="sxs-lookup"><span data-stu-id="98308-269">What are the next steps to complete the security upgrade?</span></span>

<span data-ttu-id="98308-270">結果を使用して Excel スプレッドシートが生成された後は、ツールでロール生成と権限生成の機能を使用して、ロールと権限を自動的に作成することができます。</span><span class="sxs-lookup"><span data-stu-id="98308-270">After the Excel spreadsheet with the results is generated, you can use the role generation and privilege generation functionality in the tool to create roles and privileges automatically.</span></span> <span data-ttu-id="98308-271">次に、ユーザーをそれらの役割に割り当ててシステムをテストし、アクセス権と公開されている機能が正確であることを検証します。</span><span class="sxs-lookup"><span data-stu-id="98308-271">Then, test the system by assigning users to those roles, and validating that they have access and the exposed functionality is accurate.</span></span>




