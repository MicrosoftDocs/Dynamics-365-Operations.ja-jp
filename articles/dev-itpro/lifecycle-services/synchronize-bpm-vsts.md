<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="synchronize-bpm-vsts.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>synchronize-bpm-vsts.a8d603.911a8983baa8df0fd3e21c86abb527e93b9c4978.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>911a8983baa8df0fd3e21c86abb527e93b9c4978</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\synchronize-bpm-vsts.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Synchronize BPM libraries with Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ライブラリと Azure DevOps の同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to synchronize a BPM library in LCS with Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、LCS の BPM ライブラリを Azure DevOps と同期させる方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Synchronize BPM libraries with Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ライブラリと Azure DevOps の同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>You start the implementation stage of a project by synchronizing a Business process modeler (BPM) library with your project in Microsoft Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの実装のステージを開始するには、Microsoft Azure DevOps で、ビジネス プロセス モデラー (BPM) とお客様のプロジェクトを同期します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this way, you can review processes and associate requirements with business processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、プロセスを確認し、要件を業務プロセスと関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>By synchronizing a BPM library with a Azure DevOps project, you can also track the progress of your implementation project in Azure DevOps, and can associate various work items with requirements and business processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ライブラリを Azure DevOps プロジェクトと同期させることにより、Azure DevOps での実装プロジェクトの進捗状況を追跡したり、さまざまな作業項目を要件や業務プロセスに関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>These work items include bugs, tasks, backlog items, tests, and documents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの作業項目には、バグ、タスク、バックログ項目、テスト、ドキュメントが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Currently, BPM-Azure DevOps synchronization doesn't support custom work item types or synchronizing business processes with custom work item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、BPM Azure DevOps 同期では、カスタム作業項目または業務プロセスとの同期をサポートしていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>If you try either of these, you will receive a warning.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのいずれかを試みると、警告が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>If you choose to ignore the warning and attempt a Azure DevOps sync with a custom template, you can avoid synchronization issues by verifying the following for the template:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">警告を無視して、カスタム テンプレートとの Azure DevOps 同期を試みる場合は、テンプレートの次の内容を確認することで同期の問題を回避できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Does not delete any work item type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業品目タイプの状態を削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Does not delete any state of a work item type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業品目タイプの状態を削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Does not add any required fields to a work item type</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須フィールドを作業項目の種類に追加しない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>To learn more about Azure DevOps, go to <bpt id="p1">[</bpt>www.visualstudio.com/team-services<ept id="p1">](https://www.visualstudio.com/team-services)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps の詳細については、<bpt id="p1">[</bpt>www.visualstudio.com/team-services<ept id="p1">](https://www.visualstudio.com/team-services)</ept> をご覧ください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>LCS project settings: Set up Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクト設定: Azure DevOps の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>If you've already set up Azure DevOps from Microsoft Dynamics Lifecycle Services (LCS), you can skip the procedures in this section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に Microsoft Dynamics Lifecycle Services (LCS) から Azure DevOps を設定している場合、このセクションの手順を省略できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create a personal access token</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個人用アクセス トークンを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>To connect to a Azure DevOps project, LCS is authenticated by using a personal access token.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Follow these steps to create a personal access token in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で個人用アクセス トークンを作成するには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Go to <ph id="ph1">&lt;https://www.visualstudio.com&gt;</ph>, sign in, and find your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&lt;https://www.visualstudio.com&gt;</ph> に移動し、サインイン、および Azure DevOps プロジェクトを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>In the upper-right corner, hold the pointer over your name, and then, on the menu that appears, select <bpt id="p1">**</bpt>Security<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅で、自分の名前にポインターを置き、表示されるメニューで<bpt id="p1">**</bpt>セキュリティ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Select <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to create a new personal access token.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept> を選択し、新しい個人用アクセス トークンを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Enter a name for the token, and then specify how long the token should last.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トークン名を入力し、トークンの持続時間を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Select <bpt id="p1">**</bpt>Create Token<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トークンの作成<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Copy the token to your clipboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トークンをクリップボードにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>You won't be able to find the token details again after you complete this step and move away from the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップを完了してこのページから移動すると、トークンの詳細を再度検索することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Therefore, make sure that you've copied the token before you move away from the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ページから移動する前にトークンをコピーしたことを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Configure your LCS project to connect to Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトをコンフィギュレーションして Azure DevOps に接続する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>In your LCS project, select the <bpt id="p1">**</bpt>Project settings<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトで、<bpt id="p1">**</bpt>プロジェクト設定<ept id="p1">**</ept>タイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Select <bpt id="p1">**</bpt>Azure DevOps<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Setup Azure DevOps<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Azure DevOps<ept id="p1">**</ept> を選択し、<bpt id="p2">**</bpt>Azure DevOps の設定<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>This configuration is required by many LCS tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成は多くの LCS ツールで必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>If you've already configured LCS to connect to your Azure DevOps project, you can either skip this procedure or select <bpt id="p1">**</bpt>Change<ept id="p1">**</ept> to change the existing configuration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に LCS を構成して Azure DevOps プロジェクトに接続している場合、この手順を省略するか、<bpt id="p1">**</bpt>変更<ept id="p1">**</ept>を選択して既存のコンフィギュレーションを変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Enter the root URL for your Azure DevOps account, and the personal access token that you created earlier, and then select <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps アカウントのルート URL および以前に作成した個人用アクセス トークンを入力し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Select your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Specify the mapping between LCS/BPM items and the associated Azure DevOps work item types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS/BPM 項目と関連付けられている Azure DevOps 作業項目の種類の間のマッピングを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Work item type mappings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目タイプ マッピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Select <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>, review your changes, and then select <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>続行<ept id="p1">**</ept> を選択して変更内容を確認し、<bpt id="p2">**</bpt>保存<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Synchronize a BPM library with a Azure DevOps project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトと BPM ライブラリの同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>After you've set up the connection between the LCS project and a Azure DevOps project, you can synchronize a BPM library with the Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトおよび Azure DevOps プロジェクト間の接続を設定した後は、Azure DevOps プロジェクトに BPM ライブラリを同期することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>When you synchronize a BPM library with a Azure DevOps project, a Azure DevOps work item is created for each business process line in the BPM library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ライブラリを Azure DevOps プロジェクトと同期させると、BPM ライブラリ内の各業務プロセスの明細行に対して Azure DevOps 作業項目が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In addition, the hierarchy of business processes in BPM is reflected in the hierarchy of work items in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、BPM の業務プロセスの階層は、Azure DevOps の作業項目の階層に反映されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The type of work items that are created in Azure DevOps depends on the settings of your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で作成される作業項目のタイプは、LCS プロジェクトの設定によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>This synchronization is a one-way synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この同期は一方向の同期です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Changes in LCS are reflected in Azure DevOps, but changes in Azure DevOps aren't reflected in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の変更は Azure DevOps に反映されますが、Azure DevOps の変更は LCS に反映されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The following information is synchronized:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の情報が同期されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Business process names</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスの名前</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Business process descriptions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスの説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Keywords (as tags)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キーワード (タグとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Countries or regions (as tags)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">国または地域 (タグとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Industries (as tags)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業界 (タグとして)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>To synchronize a BPM library with a Azure DevOps project, on the <bpt id="p1">**</bpt>Business process libraries<ept id="p1">**</ept> page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select <bpt id="p2">**</bpt>Azure DevOps sync<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ライブラリを Azure DevOps プロジェクトと同期させるには、<bpt id="p1">**</bpt>業務プロセス ライブラリ<ept id="p1">**</ept>ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、<bpt id="p2">**</bpt>Azure DevOps 同期<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Starting Azure DevOps synchronization from the tile for a library</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライブラリのタイルから Azure DevOps 同期を開始</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>You can also start Azure DevOps synchronization from the toolbar in a BPM library.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、BPM ライブラリ内のツールバーから Azure DevOps 同期を開始することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Select the ellipsis button (…), and then select <bpt id="p1">**</bpt>Azure DevOps sync<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">省略記号ボタン (...) を選択し、<bpt id="p1">**</bpt>Azure DevOps の同期<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Starting Azure DevOps synchronization from the toolbar in a library</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ライブラリのツール バーから Azure DevOps 同期を開始</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>BPM localization is not supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM ローカライズはサポートされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>If you edit in the new BPM client in any language other than EN-US, your changes will only display when you view the BPM in the language in which the changes were made.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To view any changes made in EN-US, you must synchronize with Visual Studio Team Server before the changes will display.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Turn off synchronization of BPM with Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM と Azure DevOps の同期の停止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>To turn off synchronization, on the <bpt id="p1">**</bpt>Business process libraries<ept id="p1">**</ept> page, select the library that you want to stop synchronizing, select the ellipsis button (…), and then unselect <bpt id="p2">**</bpt>Azure DevOps sync<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期をオフにするには、<bpt id="p1">**</bpt>業務プロセス ライブラリ<ept id="p1">**</ept> ページで同期を停止するライブラリを選択し、省略記号ボタン (...) を選択してから <bpt id="p2">**</bpt>Azure DevOps 同期<ept id="p2">**</ept> を選択解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Review processes and add requirements</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスを確認し、要件を追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>During the project phase where you're gathering requirements, you can use the BPM library to review business processes and tasks, and to identify requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要件を収集しているプロジェクトのフェーズ中に、BPM ライブラリを使用して、ビジネス プロセスおよびタスクをレビューし、要件を特定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>In BPM, you can mark business processes as reviewed to track the review process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM で、業務プロセスを確認済みとマークして、確認プロセスを追跡することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To mark a process or one of its child processes as reviewed, select the process in BPM, and then, in the right pane, on the <bpt id="p1">**</bpt>Overview<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Mark as reviewed<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロセスまたはその子プロセスの 1 つをレビューとしてマークするには、BPMでプロセスを選択し、右ウィンドウの <bpt id="p1">**</bpt>概要<ept id="p1">**</ept> タブで <bpt id="p2">**</bpt>レビューとしてマーク<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>When a business process is marked as reviewed, the <bpt id="p1">**</bpt>Reviewed<ept id="p1">**</ept> column is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">業務プロセスを確認済みとしてマークすると、<bpt id="p1">**</bpt>確認済<ept id="p1">**</ept> 列が更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>This column shows the following information:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この列には、次の情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>A fraction indicates how many direct child processes have been reviewed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分数では、直接の子プロセスの確認された数を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A symbol indicates how completely the process and its child processes have been reviewed:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記号は、プロセスとその子プロセスがどれだけ完全にレビューされたかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">**</bpt>Green check mark<ept id="p1">**</ept> – The process and all its child processes have been fully reviewed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>緑のチェック マーク<ept id="p1">**</ept> – プロセスとそのすべての子プロセスは完全に確認済です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">**</bpt>Yellow circle<ept id="p1">**</ept> – The process and its child processes have been partially reviewed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>黄色の円<ept id="p1">**</ept> – プロセスおよびその子プロセスは部分的に確認されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">**</bpt>Red dash<ept id="p1">**</ept> – The process and its child processes haven't been reviewed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>赤いダッシュ<ept id="p1">**</ept> – プロセスとその子プロセスは確認されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Example of a Review column</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レビュー列の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>While you're reviewing a business process that is connected to Azure DevOps, you can add a requirement directly to your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps に接続されている業務プロセスを確認するとき、Azure DevOps プロジェクトに要求を直接追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Select a business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス プロセスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>In the right pane, on the <bpt id="p1">**</bpt>Requirements<ept id="p1">**</ept> tab, select <bpt id="p2">**</bpt>Add requirement<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右ウィンドウの<bpt id="p1">**</bpt>要件<ept id="p1">**</ept>タブで、<bpt id="p2">**</bpt>要件を追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Enter a name, description, and type, and then select <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前、説明、およびタイプを入力し、次に<bpt id="p1">**</bpt>作成<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>In Azure DevOps, a requirement work item is created that is associated with the current business process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps では、現在の業務プロセスに関連付けられている要求作業項目が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>To go to the Azure DevOps work items that are associated with the current business process, on the <bpt id="p1">**</bpt>Requirements<ept id="p1">**</ept> tab, select the appropriate links.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在の業務プロセスに関連付けられている Azure DevOps 作業項目に移動するには、<bpt id="p1">**</bpt>要件<ept id="p1">**</ept> タブで適切なリンクを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Common syncing errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な同期エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If the BPM to Azure DevOps synchronization fails, you will see the failed process name, work item type, and an error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM から Azure DevOps への同期が失敗した場合、失敗したプロセス名、作業項目の種類、およびエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>BPM sync error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BPM 同期エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Here are some common causes and suggested actions to resolve the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここでいくつか一般的な原因と、エラーを解決するために推奨するアクションを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">**</bpt>Possible cause<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>考えられる原因<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">**</bpt>Error message<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>エラー メッセージ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">**</bpt>Suggested solution<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>推奨される解決策<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Required field added</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須フィールドが追加されました</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Failed to create work item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の作成に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>A required field has been added to this work item type, which is not supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須フィールドがこの作業項目の種類に追加されましたが、サポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Remove this requirement or provide a default value in the process template to unblock the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この要件を削除するか、プロセス テンプレートで既定値を提供して、操作をブロック解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Remove the required field or provide a default value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必須フィールドを削除するか、既定値を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Work item type disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の種類が無効です</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Failed to create work item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の作成に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The work item type has been disabled in the process template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の種類がプロセス テンプレートで無効になっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Enable the work item type to unblock the operation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の種類を有効にして、操作をブロック解除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Enable the work item type in the process template</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の種類をプロセス テンプレートで有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Couldn't find work item to update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新する作業項目が見つかりませんでした</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Failed to update work item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目の更新に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The work item does not exist, or you do not have permissions to read it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業項目が存在しないか、読み取るためのアクセス許可がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Check the PAT configuration in the project settings or restore the work item if it has been deleted directly from the DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト設定で PAT コンフィギュレーションを確認するか、作業項目が DevOps プロジェクトから直接削除されている場合は作業項目を復元します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Restore the work item from the recycle bin if it was deleted, or create a new Personal Access Token (PAT) and make sure that it has full permissions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">削除された場合はごみ箱から作業項目を復元するか、新しい個人用アクセス トークン (PAT) を作成して完全なアクセス許可があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Personal Access Token is expired</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">個人用アクセス トークンの期限が切れています</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Failed to sync with Visual Studio Team Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio Team Services との同期に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The request response is: Unauthorized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求応答は次のとおりです: 無許可。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Please check that the PAT is setup correctly and still valid, try again and contact support if the error persists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Create a new Personal Access Token (PAT) from Azure DevOps and update the PAT value in your LCS Project settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps から新しい個人用アクセス トークン (PAT) を作成し、LCS プロジェクト設定で PAT 値を更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Generic error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Failed to sync with Visual Studio Team Services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio Team Services との同期に失敗しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The request response is: <ph id="ph1">{0}</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">要求応答は次のとおりです: <ph id="ph1">{0}</ph>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Please check that the PAT is setup correctly and still valid, try again and contact support if the error persists.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Contact customer support with the request response that caused the syncing error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同期エラーの原因となった要求応答で、顧客サポートに問い合わせてください。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>