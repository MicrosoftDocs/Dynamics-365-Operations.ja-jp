<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="support-experience.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>support-experience.57e1f5.a8d48d190beb7433ae4fc09ef7431181f85752dd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>a8d48d190beb7433ae4fc09ef7431181f85752dd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\support-experience.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up technical support for Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の技術サポートの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about the support experience for cloud and on-premises deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、クラウドおよびオンプレミスの展開のサポートについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>It describes the setup that is required and explains how to create and work with support issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な設定およびサポートの問題を作成して対応する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Set up technical support for Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations の技術サポートの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Before you can set up technical support, you must acquire a Microsoft Azure Active Directory (Azure AD) account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テクニカル サポートの設定をする前に、Microsoft Azure Active Directory (Azure AD) アカウントを取得する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This account is created during the subscription setup for Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このアカウントは、Microsoft Dynamics 365 for Finance and Operations のサブスクリプション設定時に作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Create an Azure DevOps project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile in a Lifecycle Services (LCS) project uses Azure DevOps to store issues that are submitted through the client and issues that are manually created from the<bpt id="p2"> **</bpt>Support<ept id="p2">**</ept> tile in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) プロジェクトの<bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルは、Azure DevOps を使用し、クライアントを通じて送信された問題と、LCS の<bpt id="p2"> **</bpt>サポート<ept id="p2">**</ept> タイルから手動で作成された問題を格納します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This functionality requires that a Azure DevOps project be configured in the LCS project that you want to use for support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用するには、サポートに使用する LCS プロジェクトで Azure DevOps プロジェクトを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>All users who need to use the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile to submit an issue must have access to the Azure DevOps project, and must authorize LCS to access Azure DevOps on their own behalf.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルを使用して問題を提出する必要があるすべてのユーザーは、Azure DevOps プロジェクトにアクセスできる必要があり、LCS が Azure DevOps に自身が代わってアクセスできるようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Most users don't have access to LCS or Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのユーザーは、LCS または Azure DevOps へのアクセス権がありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Therefore, in the Azure DevOps project, you should create a special system account that can be used to submit issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、Azure DevOps プロジェクトでは、問題を提出するために使用できる特別なシステム アカウントを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Create a new Azure DevOps project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Azure DevOps プロジェクトの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Go to <ph id="ph1">&lt;https://www.visualstudio.com/&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&lt;https://www.visualstudio.com/&gt;</ph> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Click <bpt id="p1">**</bpt>Sign in<ept id="p1">**</ept> in the upper-right corner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅にある<bpt id="p1">**</bpt>サインイン<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Sign in by using an AAD account that is in the tenant that your subscription is linked to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サブスクリプションがリンクされているテナントに含まれる AAD アカウントを使用してサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>If the browser already has your credentials, you won't see the sign-in page and should instead click your name in the upper-right corner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーにすでに資格情報が割り当てられている場合は、サインイン ページは表示されず、右上隅にあるユーザーの名前をクリックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>On the right side of the page, under <bpt id="p1">**</bpt>Accounts<ept id="p1">**</ept>, click <bpt id="p2">**</bpt>Create a free account now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページの右側の、<bpt id="p1">**</bpt>アカウント<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>今すぐ無料のアカウントを作成<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Specify an account URL, and then click <bpt id="p1">**</bpt>Create Account<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アカウント URL を指定し、<bpt id="p1">**</bpt>アカウントの作成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Name your project, and specify a process template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトに名前を付け、プロセス テンプレートを指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Your project should now be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、プロジェクトが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Add users to the Azure DevOps project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps プロジェクトへのユーザーの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In the upper-left corner, click <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左上にある <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>On the <bpt id="p1">**</bpt>Users<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and invite users who will use the Support experience to the Azure DevOps account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー<ept id="p1">**</ept> タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックし、サポート エクスペリエンスを使用するユーザーを Azure DevOps アカウントに招待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For each user that you invite, select either <bpt id="p1">**</bpt>Basic<ept id="p1">**</ept><ph id="ph1"> </ph>or <bpt id="p2">**</bpt>Stakeholder<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">招待する各ユーザーについては、<bpt id="p1">**</bpt>基本<ept id="p1">**</ept><ph id="ph1"> </ph>または<bpt id="p2">**</bpt>利害関係者<ept id="p2">**</ept>のいずれかを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In the upper-left corner, click <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左上にある <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Click <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept>, and browse to the project that you created in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept>をクリックし、以前の手順で作成されたプロジェクトを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>In the <bpt id="p1">**</bpt>Members<ept id="p1">**</ept><ph id="ph1"> </ph>section of the project home page, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and add the users that you invited in step 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトのホーム ページの<bpt id="p1">**</bpt>メンバー<ept id="p1">**</ept><ph id="ph1"> </ph> セクションで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックして手順 2 で招待したユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Create the Support system user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート システム ユーザーを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Create a new user in your Azure AD tenant, and enter a descriptive name, such as <bpt id="p1">**</bpt>LcsCpsSystemAccount<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure AD テナントで新しいユーザーを作成し、<bpt id="p1">**</bpt>LcsCpsSystemAccount<ept id="p1">**</ept> などの内容を説明する名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the upper-left corner, click <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左上にある <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the <bpt id="p1">**</bpt>Users<ept id="p1">**</ept> tab, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and invite the system user that you created in step 1.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー<ept id="p1">**</ept> タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックし、手順 1 で作成したシステム ユーザーを招待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For this user, select<bpt id="p1"> **</bpt>Stakeholder<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このユーザーについては、<bpt id="p1"> **</bpt>利害関係者<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In the upper-left corner, click <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左上にある <bpt id="p1">**</bpt>Team Services<ept id="p1">**</ept> を再度クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Click <bpt id="p1">**</bpt>Browse<ept id="p1">**</ept>, and browse to the project that you created earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>参照<ept id="p1">**</ept>をクリックし、以前に作成したプロジェクトを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In the <bpt id="p1">**</bpt>Members<ept id="p1">**</ept><ph id="ph1"> </ph>section of the project home page, click <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and add the system user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトのホーム ページの<bpt id="p1">**</bpt>メンバー<ept id="p1">**</ept><ph id="ph1"> </ph> セクションで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>をクリックしてシステム ユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Retrieve the personal access token for the Support system user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート システム ユーザーの個人アクセス トークンを取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Sign out of Team Services by clicking the user name in the upper-right corner and then clicking <bpt id="p1">**</bpt>Sign out<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅でユーザー名をクリックして<bpt id="p1">**</bpt>サインアウト<ept id="p1">**</ept>をクリックすることで、Team Services からサインアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Sign in to Team Services by using the Support system account that you created in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の手順で作成したサポート システム アカウントを使用して Team Services にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>In the upper-right corner, click the user name, and then click <bpt id="p1">**</bpt>My profile<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右上隅でユーザー名をクリックしてから、<bpt id="p1">**</bpt>自分のプロファイル<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>On the<bpt id="p1"> **</bpt>Security<ept id="p1">**</ept> tab, on the <bpt id="p2">**</bpt>Personal access tokens<ept id="p2">**</ept> tab, click <bpt id="p3">**</bpt>Add<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1"> **</bpt>セキュリティ<ept id="p1">**</ept> タブの、<bpt id="p2">**</bpt>個人用アクセス トークン<ept id="p2">**</ept> タブで、<bpt id="p3">**</bpt>追加<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Enter a description, such as <bpt id="p1">**</bpt>LCS Support system account<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>LCS サポート システム アカウント<ept id="p1">**</ept>のような説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Select an expiration date of one year.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 年の有効期限を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>Selected scopes<ept id="p1">**</ept>, and the select <bpt id="p2">**</bpt>Work items (read and write)<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択されているスコープ<ept id="p1">**</ept>をクリックし、<bpt id="p2">**</bpt>作業項目 (読み取り/書き込み)<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Click <bpt id="p1">**</bpt>Create token<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トークンの作成<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Copy the token and paste it in a safe location because it won't be accessible after you move away from the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページから移動した後にアクセスできなくするため、トークンをコピーして、安全な場所に貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Configure LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Sign in to LCS by using an account that has the <bpt id="p1">**</bpt>Owner<ept id="p1">**</ept> role for the LCS project that Finance and Operations is deployed in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations が配置された LCS プロジェクトの <bpt id="p1">**</bpt>所有者<ept id="p1">**</ept> ロールを持っているアカウントを使用して、LCS にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Open the project in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS でプロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Click <bpt id="p1">**</bpt>Project settings<ept id="p1">**</ept>, and then click the<bpt id="p2"> **</bpt>Azure DevOps<ept id="p2">**</ept><ph id="ph1"> </ph>link.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト設定<ept id="p1">**</ept>をクリックし、<bpt id="p2"> **</bpt>Azure DevOps<ept id="p2">**</ept><ph id="ph1"> </ph> リンクをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-Project-Tiles<ept id="p1">](./media/lcs-project-tiles-237x300.png)](./media/lcs-project-tiles.png)</ept><ph id="ph2">
</ph><bpt id="p2">[</bpt><ph id="ph3">![</ph>LCS-Project-Settings-VSO<ept id="p2">](./media/lcs-project-settings-vso-1024x320.png)](./media/lcs-project-settings-vso.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-Project-Tiles<ept id="p1">](./media/lcs-project-tiles-237x300.png)](./media/lcs-project-tiles.png)</ept><ph id="ph2">
</ph><bpt id="p2">[</bpt><ph id="ph3">![</ph>LCS-Project-Settings-VSO<ept id="p2">](./media/lcs-project-settings-vso-1024x320.png)](./media/lcs-project-settings-vso.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Click <bpt id="p1">**</bpt>Setup Azure DevOps<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Azure DevOps の設定<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In the <bpt id="p1">**</bpt>Azure DevOps site URL<ept id="p1">**</ept> field, enter the URL of the Azure DevOps project that you created in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Azure DevOps サイトの URL<ept id="p1">**</ept> フィールドに、前のセクションで作成した Azure DevOps プロジェクトの URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In the <bpt id="p1">**</bpt>Personal access token<ept id="p1">**</ept><ph id="ph1"> </ph>field, enter the personal access token that you created in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>個人用アクセス トークン<ept id="p1">**</ept><ph id="ph1"> </ph> フィールドに、前のセクションで作成した個人用アクセス トークンを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-Project-Settings-VSO-Setup-1<ept id="p1">](./media/lcs-project-settings-vso-setup-1.png)](./media/lcs-project-settings-vso-setup-1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-Project-Settings-VSO-Setup-1<ept id="p1">](./media/lcs-project-settings-vso-setup-1.png)](./media/lcs-project-settings-vso-setup-1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Select the VSO project to use, and then click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用する VSO プロジェクトを選択し、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Click <bpt id="p1">**</bpt>Authorize<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>承認<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the confirmation message box, click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">確認メッセージ ボックスで、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Sign in to Visual Studio Online.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio Online へサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Click <bpt id="p1">**</bpt>Accept<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>承認<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Create an issue in the Finance and Operations client (Microsoft Dynamics AX 7.0, Dynamics AX platform update 1 or update 2, or Finance and Operations platform update 3)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のクライアント (Microsoft Dynamics AX 7.0、Dynamics AX プラットフォーム更新プログラム 1 または更新プログラム 2、または Finance and Operations プラットフォーム更新プログラム 3) に問題を作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>If you are on Finance and Operations platform update 4, or if you have consumed KB 4010473 for platform update 3, skip to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations プラットフォーム更新プログラム 4 を使用している場合、またはプラットフォーム更新プログラム 3 の KB 4010473 を消費した場合、次のセクションをスキップします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>If you have an on-premises deployment of Finance and Operations, the option to search for existing issues and submit a support incident from the Dynamics 365 for Finance and Operations on-premises client to your Azure DevOps project is not available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations をオンプレミスで配置している場合、既存の問題を検索して Dynamics 365 for Finance and Operations オンプレミス クライアントから Azure DevOps プロジェクトにサポート インシデントを送信することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the client, click the <bpt id="p1">**</bpt>Help<ept id="p1">**</ept> menu, or question mark icon, in the upper-right corner.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントで、右上隅の<bpt id="p1">**</bpt>ヘルプ<ept id="p1">**</ept> メニューまたは疑問符アイコンをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>AX7-help-Contact<ph id="ph2">\_</ph>Your<ph id="ph3">\_</ph>Support<ept id="p1">](./media/ax7-help-contact_your_support1.png)](./media/ax7-help-contact_your_support1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>AX7-help-Contact<ph id="ph2">\_</ph>Your<ph id="ph3">\_</ph>Support<ept id="p1">](./media/ax7-help-contact_your_support1.png)](./media/ax7-help-contact_your_support1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Click <bpt id="p1">**</bpt>Contact your support team<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サポート チームに連絡してください<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Enter information in the <bpt id="p1">**</bpt>Issue<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Description<ept id="p2">**</ept> fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題<ept id="p1">**</ept>および<bpt id="p2">**</bpt>説明<ept id="p2">**</ept>フィールドに情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Optional: Enter the time when the issue occurred (Platform update 3 feature).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: 問題が発生した時刻を入力します (プラットフォーム アップデート 3 の機能)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Optional: Set the <bpt id="p1">**</bpt>Work stoppage<ept id="p1">**</ept> fields to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: <bpt id="p1">**</bpt>作業の中断<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Optional: Upload a task recording.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オプション: 作業記録をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Set the option to share your email address with LCS to <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS を使用して電子メール アドレスを共有するオプションを <bpt id="p1">**</bpt>はい<ept id="p1">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>The <bpt id="p1">**</bpt>Submit<ept id="p1">**</ept> button won't be available unless you share your email address.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子メール アドレスを共有しない限り、<bpt id="p1">**</bpt>送信<ept id="p1">**</ept> ボタンは使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Click <bpt id="p1">**</bpt>Submit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>送信<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Contact Support<ept id="p1">](./media/contact-support.png)](./media/contact-support.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>サポートへの問い合わせ<ept id="p1">](./media/contact-support.png)](./media/contact-support.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>You should receive a confirmation message that states that the issue has been submitted to LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS に問題が送信されたことを示す確認メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Users who are in the <bpt id="p1">**</bpt>Operations users<ept id="p1">**</ept> role are notified that a new issue has been submitted to LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オペレーション ユーザー<ept id="p1">**</ept> ロールのユーザーに、新しい案件が LCS に送信されたことが通知されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>To view the issue that was submitted, click the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile in the associated LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">提出された問題を表示するには、関連する LCS プロジェクトの <bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Create an issue in the Finance and Operations client (Finance and Operations platform update 4 and platform update 3 KB 4010473)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のクライアントで問題を作成する (Finance and Operations プラットフォームのアップデート 4 およびプラットフォームのアップデート 3 KB 4010473)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If you have not taken platform update 4 for Finance and Operations, or if you have not consumed KB 4010473 for platform update 3, complete the procedure in the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のプラットフォーム更新プログラム 4 を使用しない場合、またはプラットフォーム更新プログラム 3 の KB 4010473 を消費していない場合は、前のセクションの手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The Support experience has been updated to show updates that are published by Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft によって公開されている更新プログラムを表示するため、サポート エクスペリエンスが更新されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>In the client, on the top bar, click<bpt id="p1"> **</bpt>?<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Support<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントの上部バーで、<bpt id="p1"> **</bpt>?<ept id="p1">**</ept> をクリックしてから<bpt id="p2">**</bpt>サポート<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>If you have an on-premises deployment of Finance and Operations, the option to search for existing issues and submit a support incident from the Dynamics 365 for Finance and Operations on-premises client to your Azure DevOps project is not available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations をオンプレミスで配置している場合、既存の問題を検索して Dynamics 365 for Finance and Operations オンプレミス クライアントから Azure DevOps プロジェクトにサポート インシデントを送信することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>wiki1<ept id="p1">](./media/wiki1-1024x518.png)](./media/wiki1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>wiki1<ept id="p1">](./media/wiki1-1024x518.png)](./media/wiki1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>If you haven’t already connected to Lifecycle Services (LCS), a dialog box will display where you can connect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) にまだ接続していない場合は、ダイアログ ボックスに接続できる場所が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Click the link to connect before proceeding.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">続行する前に、接続するリンクをクリックしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>wiki2<ept id="p1">](./media/wiki2.png)](./media/wiki2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>wiki2<ept id="p1">](./media/wiki2.png)](./media/wiki2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Search for a fix</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正プログラムの検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>After you connect to LCS, you can search for existing Microsoft published updates and fixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS に接続した後は、既存の Microsoft 更新プログラムおよび修正を検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Enter your issue in the <bpt id="p1">**</bpt>Search<ept id="p1">**</ept> box and press <bpt id="p2">**</bpt>Enter<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>検索<ept id="p1">**</ept>ボックスに問題を入力し、<bpt id="p2">**</bpt>入力<ept id="p2">**</ept>を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>If you don't want the functionality to search for existing fixes enabled for all users, you can remove the <bpt id="p1">**</bpt>SearchExistingFixes<ept id="p1">**</ept><ph id="ph1"> </ph>duty from the System user role and add it to only those roles which you want to have this functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのユーザーに対して有効な既存の修正プログラムを検索する機能を使用しない場合は、<bpt id="p1">**</bpt>SearchExistingFixes<ept id="p1">**</ept><ph id="ph1"> </ph>の職務をシステム ユーザー ロールから削除し、この機能を追加するロールにのみ追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Search results are based on the Microsoft Issue Search data that is relevant to your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果は、環境に関連する Microsoft 問題検索データに基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Fixes that you have already installed will not be included in your search results.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既にインストールした修正は、検索結果には含まれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>To view a specific result, click the link to view the details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定の結果を表示するには、リンクをクリックして詳細を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Based on the duties assigned to you, you will see either the <bpt id="p1">**</bpt>Download view<ept id="p1">**</ept> or the<bpt id="p2"> **</bpt>Request view<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割り当てられた職務に基づいて、<bpt id="p1">**</bpt>ダウンロード表示<ept id="p1">**</ept>または<bpt id="p2"> **</bpt>要求表示<ept id="p2">**</ept>が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><bpt id="p1">**</bpt>Download view<ept id="p1">**</ept> - By default, this view is only available to system administrators.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ダウンロード表示<ept id="p1">**</ept> - 既定では、この表示はシステム管理者のみが利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>From this view, you can directly download the hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このビューから、直接修正プログラムをダウンロードできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>The duty <bpt id="p1">**</bpt>DownloadHotfix<ept id="p1">**</ept><ph id="ph1"> </ph>controls the ability to directly download fixes from LCS rather than requesting them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">職務 <bpt id="p1">**</bpt>DownloadHotfix<ept id="p1">**</ept><ph id="ph1"> </ph>は、修正プログラムを要求するのではなく、LCS から直接ダウンロードする機能を制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Only system administrators will have access to it by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、システム管理者のみそのアクセス権があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>If you want to assign this duty to users other than system administrators, you can do so by adding the duty to the selected roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この職務権限をシステム管理者以外のユーザーに割り当てる場合は、職務権限を選択したロールに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">**</bpt>Request view<ept id="p1">**</ept><ph id="ph1"> </ph>- By default, this view is available to all users who are not system administrators.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要求表示<ept id="p1">**</ept><ph id="ph1"> </ph> - 既定では、システム管理者ではないすべてのユーザーがこのビューを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>From this view, you can make a request to download the hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このビューから、修正プログラムのダウンロードを要求できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>After you submit your request to download the hotfix, a work item will be created in the Azure DevOps project that is associated to your LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">修正プログラムをダウンロードする要求を送信した後は、LCS プロジェクトに関連付けられている Azure DevOps プロジェクトに作業項目が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The customer IT admin can view all requested hotfixes by clicking the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile in LCS and then clicking the <bpt id="p2">**</bpt>Hotfix requests<ept id="p2">**</ept> tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客の IT 管理者は、LCS の<bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルをクリックし、<bpt id="p2">**</bpt>修正プログラムの要求<ept id="p2">**</ept>タブをクリックして、要求したすべての修正プログラムを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Search for project work items in Azure DevOps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で、プロジェクトの作業項目を検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The Azure DevOps administrator can publish project work items to your organization users by tagging the work items with <bpt id="p1">**</bpt>#SearchableInFinanceAndOperations<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps 管理者は、<bpt id="p1">**</bpt>#SearchableInFinanceAndOperations<ept id="p1">**</ept> を作業項目にタグ付けすることによって、プロジェクトの作業項目を組織のユーザーに発行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>The tagged work items will be searchable for users from the client support search box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タグ付けされた作業項目は、クライアント サポート検索ボックスからユーザーに対して検索可能になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>The search result will include tagged Azure DevOps work items in addition to Microsoft published updates and fixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果には、Microsoft が公開した更新プログラムや修正プログラムに加えて、タグ付きの Azure DevOps 作業項目が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The following graphic shows a tagged Azure DevOps work item for publishing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のグラフィックは、公開用のタグ付きの Azure DevOps 作業項目を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>vstsTag<ept id="p1">](./media/VSTS%20Tagging.png)](./media/VSTS%20Tagging.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>vstsTag<ept id="p1">](./media/VSTS%20Tagging.png)](./media/VSTS%20Tagging.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>When you search for published Azure DevOps work items using the support search box, search results show the work item's type, title, state, and description in a new browser tab with <bpt id="p1">**</bpt>view<ept id="p1">**</ept> mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート検索ボックスを使用して公開済みの Azure DevOps 作業項目を検索するとき、検索結果は、新しいブラウザー タブに <bpt id="p1">**</bpt>表示<ept id="p1">**</ept> モードで、作業項目のタイプ、タイトル、状態、および説明が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Users with proper permissions can edit the work item in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なアクセス許可を持つユーザーが、Azure DevOps の作業項目を編集できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The following graphic shows the search result of a published Azure DevOps work item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のグラフィックは、公開された Azure DevOps 作業項目の検索結果を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ViewVSTS<ept id="p1">](./media/ViewVSTSItem.png)](./media/ViewVSTSItem.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ViewVSTS<ept id="p1">](./media/ViewVSTSItem.png)](./media/ViewVSTSItem.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The published Azure DevOps work items are only visible to your organization's users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">発行済みの Azure DevOps 作業項目は、組織のユーザーにのみ表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Create and submit a new issue</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい問題の作成および送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If you don’t see a fix in the search results, you can create a new issue by clicking <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果から修正プログラムが見つからない場合は、<bpt id="p1">**</bpt>作成<ept id="p1">**</ept>をクリックし、新しい問題を作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>This is the same functionality that is available for previous releases and is documented in earlier procedures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは以前のリリースで使用できる機能と同じで、以前の手順で説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Work with issues in LCS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS での問題についての作業</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>View issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>In the LCS<bpt id="p1"> **</bpt>Support<ept id="p1">**</ept> tile, issues are stored as work items in the Azure DevOps project that is associated with the LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS <bpt id="p1"> **</bpt>サポート<ept id="p1">**</ept> タイルでは、問題が LCS プロジェクトに関連付けられている Azure DevOps プロジェクトで作業項目として保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Specifically, issues are stored as work items of the <bpt id="p1">**</bpt>Issue<ept id="p1">**</ept><ph id="ph1"> </ph>or <bpt id="p2">**</bpt>Impediment<ept id="p2">**</ept> type, depending on the type of Azure DevOps project, in the <bpt id="p3">**</bpt>AxAndLcsGeneratedIssues<ept id="p3">**</ept> area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、問題は、Azure DevOps プロジェクトのタイプに応じて<bpt id="p1">**</bpt>問題<ept id="p1">**</ept><ph id="ph1"> </ph>または<bpt id="p2">**</bpt>懸案事項<ept id="p2">**</ept>の作業項目として <bpt id="p3">**</bpt>AxAndLcsGeneratedIssues<ept id="p3">**</ept> 領域に保存されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Every work item of one of those types in that area will be included in the list of issues in the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その地域にあるタイプの作業項目のすべてが、<bpt id="p1">**</bpt>サポート<ept id="p1">**</ept>タイルの問題リストに含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>If an issue is modified in Azure DevOps, the changes will be reflected in Support issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps で問題点が変更されると、サポート案件で変更内容が反映されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Issues can be assigned to any user in the Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題は、Azure DevOps プロジェクト内のユーザーに割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Users don't need to have access to LCS to work with issues in Azure DevOps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、Azure DevOps で案件を取り扱うために、LCS にアクセスする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Go to <bpt id="p1">[</bpt>lcs.dynamics.com,<ept id="p1">](https://lcs.dynamics.com/en/)</ept> and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>lcs.dynamics.com,<ept id="p1">](https://lcs.dynamics.com/en/)</ept> に移動しサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Open the LCS project that is associated with the environment that you want to view issues for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">払出を表示する環境に関連付けられている LCS プロジェクトを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Click the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>A list of the issues that have been created appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成された問題の一覧を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-CPS-list<ept id="p1">](./media/lcs-cps-list-1024x243.png)](./media/lcs-cps-list.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-CPS-list<ept id="p1">](./media/lcs-cps-list-1024x243.png)](./media/lcs-cps-list.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Edit issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">項目を編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>In the <bpt id="p1">**</bpt>Issues<ept id="p1">**</ept> grid, click the title of an issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題<ept id="p1">**</ept>グリッドで、問題のタイトルをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If necessary, sign in to Azure DevOps by using an account that has access to the Azure DevOps project that you set up in the first section of this topic, <bpt id="p1">**</bpt>Create an Azure DevOps project<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの最初のセクションで設定した Azure DevOps プロジェクトへのアクセス権を持つアカウントを使用して、Azure DevOps へログインし、<bpt id="p1">**</bpt>Azure DevOps プロジェクトを作成<ept id="p1">**</ept>します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>There is an issue in Azure DevOps, where the link to edit work items doesn't work correctly if sign-in is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps には、サインインが必要な場合に作業項目を編集するためのリンクが正しく機能しないという問題があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>If you see the <bpt id="p1">**</bpt>Assigned to me<ept id="p1">**</ept><ph id="ph1"> </ph>query after you sign in to Azure DevOps, go back to LCS, and click the title of the issue in the issue grid again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps にサインインした後に<bpt id="p1">**</bpt>自分自身に割り当て<ept id="p1">**</ept><ph id="ph1"> </ph>クエリが表示された場合、LCS に戻って、問題グリッドで問題のタイトルをもう一度クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>The Azure DevOps editor opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure DevOps エディターが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Edit the issue, and then save your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題点を編集し、変更を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>The changes will be reflected in the <bpt id="p1">**</bpt>Support<ept id="p1">**</ept> tile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更は<bpt id="p1">**</bpt>サポート<ept id="p1">**</ept> タイルに反映されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Troubleshoot issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>The information in this section is not applicable to on-premises deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションの情報は、オンプレミスの配置には適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Issues that are created through the client contain metadata about the environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントを使用して作成される問題には、環境に関するメタデータが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>When those issues are selected in the <bpt id="p1">**</bpt>Issue<ept id="p1">**</ept> grid, the <bpt id="p2">**</bpt>Troubleshoot<ept id="p2">**</ept> button becomes available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題<ept id="p1">**</ept> グリッドでこれらの問題が選択されると、<bpt id="p2">**</bpt>トラブルシューティング<ept id="p2">**</ept> ボタンが使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>When you click <bpt id="p1">**</bpt>Troubleshoot<ept id="p1">**</ept>, the <bpt id="p2">**</bpt>Event monitoring<ept id="p2">**</ept><ph id="ph1"> </ph>page opens.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トラブルシューティング<ept id="p1">**</ept>をクリックすると、<bpt id="p2">**</bpt>イベント監視<ept id="p2">**</ept><ph id="ph1"> </ph>ページが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This page lets you access events and logs that are related to the issue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページでは、問題に関連するイベントやログにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The page shows activities, error messages, and other information that has occurred within the last two hours since an issue was reported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページには、活動、エラー メッセージ、および問題点が報告されてからこの 2 時間以内に発生したその他の情報が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-CPS-list-troubleshoot-1024x331<ept id="p1">](./media/lcs-cps-list-troubleshoot-1024x3311-1024x331.png)](./media/lcs-cps-list-troubleshoot-1024x3311.png)</ept><ph id="ph2"> 
</ph><bpt id="p2">[</bpt><ph id="ph3">![</ph>LCS-Monitoring-1024x419<ept id="p2">](./media/lcs-monitoring-1024x4191-1024x419.png)](./media/lcs-monitoring-1024x4191.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LCS-CPS-list-troubleshoot-1024x331<ept id="p1">](./media/lcs-cps-list-troubleshoot-1024x3311-1024x331.png)](./media/lcs-cps-list-troubleshoot-1024x3311.png)</ept><ph id="ph2"> 
</ph><bpt id="p2">[</bpt><ph id="ph3">![</ph>LCS-Monitoring-1024x419<ept id="p2">](./media/lcs-monitoring-1024x4191-1024x419.png)](./media/lcs-monitoring-1024x4191.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Submit an issue to Microsoft</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft に問題を送信</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>You can submit issues to Microsoft support.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft サポートに問題を送信することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>When you submit an issue to Microsoft, the information and attachments in the issue can be included in the Microsoft support incident.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft に問題点を送信すると、問題に関する情報と添付ファイルを Microsoft サポート インシデントに含めることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>** ** LCS users must have a valid Microsoft support plan to submit issues to Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">** ** Microsoft に問題を送信するためには、LCS ユーザーに有効な Microsoft サポート プランが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If you have trouble submitting issues to Microsoft, work with your administrator to make sure that your LCS credentials are added to or associated with your organization's support plan with Microsoft Partner Source Business Center.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft に問題を報告する上で問題が発生している場合は、管理者と連携して、LCS 資格情報が、Microsoft Partner Source Business Center との組織のサポート計画に追加されている、または関連付けられているかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>In the <bpt id="p1">**</bpt>Issue<ept id="p1">**</ept> grid, select the issue to submit to Microsoft, and then click <bpt id="p2">**</bpt>Submit to Microsoft<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題<ept id="p1">**</ept>グリッドで、Microsoft に送信する問題を選択して、<bpt id="p2">**</bpt>Microsoft に送信<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>If your account is associated with multiple support organizations, select the organization to use to create the Microsoft support incident.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アカウントが複数のサポート組織に関連付けられている場合、使用する組織を選択して Microsoft サポート インシデントを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Use <bpt id="p1">**</bpt>Issue search<ept id="p1">**</ept> to verify that your issue hasn't already been solved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題検索<ept id="p1">**</ept>を使用して、問題がまだ解決されていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>If <bpt id="p1">**</bpt>Issue search<ept id="p1">**</ept> doesn't provide a solution to your issue, click <bpt id="p2">**</bpt>Create incident<ept id="p2">**</ept><ph id="ph1"> </ph>at the bottom of the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>問題検索<ept id="p1">**</ept>により問題が解決されない場合、ページの下部にある<bpt id="p2">**</bpt>作成インシデント<ept id="p2">**</ept><ph id="ph1"> </ph>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Share diagnostic data with the Microsoft support team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft サポート チームに診断データを共有します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>By providing version information, your issues can be resolved more quickly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン情報を提供することによって、問題をより迅速に解決できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Describe your issue, provide your contact information, and then click <bpt id="p1">**</bpt>Submit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題を説明し、連絡先情報を入力してから、<bpt id="p1">**</bpt>送信<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Support settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>The information in this section is not applicable to on-premises deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションの情報は、オンプレミスの配置には適用されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>When you deploy Finance and Operations from Lifecycle Services, no configuration is required, because the Support tool automatically saves any issues to the same LCS project that Finance and Operations was deployed from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations を Lifecycle Services から配置するとき、構成は必要ありません。それは、サポート ツールが、配置された Finance and Operations の供給元の同じ LCS プロジェクトに問題を自動的に保存するためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>To verify the LCS project that Support uses, go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Setup<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>System parameters<ept id="p3">**</ept>, and then click <bpt id="p4">**</bpt>Help<ept id="p4">**</ept><ph id="ph3"> &gt; </ph><bpt id="p5">**</bpt>Support Contact<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされている LCS プロジェクトを確認するには、<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>設定<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>システム パラメーター<ept id="p3">**</ept> に移動し、<bpt id="p4">**</bpt>ヘルプ<ept id="p4">**</ept><ph id="ph3"> &gt; </ph><bpt id="p5">**</bpt>サポートの連絡先<ept id="p5">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configure Contact support<ept id="p1">](./media/configure-contact-support.jpg)](./media/configure-contact-support.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>連絡先の構成サポート<ept id="p1">](./media/configure-contact-support.jpg)](./media/configure-contact-support.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Support plans (on-premises only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート計画 (オンプレミスのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>The following customer and partner support plans are available for on-premises deployments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミスの配置では、次の顧客およびパートナーのサポート計画を利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">**</bpt>Customer<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>Software assurance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソフトウェア保証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Advantage/Advantage Plus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドバンテージ/アドバンテージ プラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Premier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プレミア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source><bpt id="p1">**</bpt>Partner<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パートナー<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Partner Advantage/Partner Advantage Plus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Partner Advantage/Partner Advantage Plus</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Advanced Support for Partners</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パートナー様向け Advanced サポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Premier</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プレミア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Prevent users from creating issues from the client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが、クライアントからの問題を作成できなようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>By default, the System user role has the privilege,<bpt id="p1"> *</bpt>SysLCSCPSIssueEntry<ept id="p1">*</ept> assigned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、システム ユーザー ロールに <bpt id="p1"> *</bpt>SysLCSCPSIssueEntry<ept id="p1">*</ept> という権限が割り当てられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>This privilege controls access to the <bpt id="p1">**</bpt>Contact your support team<ept id="p1">**</ept> menu item on the Help menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この権限は、[ヘルプ] メニューの <bpt id="p1">**</bpt>サポート チームに連絡<ept id="p1">**</ept> メニュー項目へのアクセスを制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>If you want to prevent users from being able to create and submit issues from the client, remove this privilege from the System user role.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがクライアントからの問題を作成して送信できないようにするには、システム ユーザー ロールからこの権限を削除します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>