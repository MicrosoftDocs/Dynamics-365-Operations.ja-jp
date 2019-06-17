<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-lcs-security.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-lcs-security.1e17db.082d9003a5b1afba67273ffb22a3e6973e68b561.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>082d9003a5b1afba67273ffb22a3e6973e68b561</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\lifecycle-services\configure-lcs-security.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure Lifecycle Services (LCS) security</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) のセキュリティの構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Security in Microsoft Dynamics Lifecycle Services (LCS) is controlled at both the organization level and the project level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>Not all members of an organization have access to all projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104" restype="x-metadata">
          <source>Additionally, the members of a project might not all be members of the same organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Configure Lifecycle Services (LCS) security</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) のセキュリティの構成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Security in Microsoft Dynamics Lifecycle Services (LCS) is controlled at both the organization level and the project level.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics Lifecycle Services (LCS) のセキュリティは、組織レベルとプロジェクト レベルの両方で制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Not all members of an organization have access to all projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織のすべてのメンバーが、すべてのプロジェクトへのアクセス権を持っているわけではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Additionally, the members of a project might not all be members of the same organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、プロジェクトのメンバーは、すべて同じ組織のメンバーではない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>For the current version of Microsoft Dynamics 365 for Finance and Operations, users can sign in by using the Microsoft Azure Active Directory (Azure AD) credentials that they created in the <bpt id="p1">[</bpt>Microsoft Office 365 portal<ept id="p1">](https://go.microsoft.com/fwlink/?LinkID=324287)</ept> when they signed up.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations の現在のバージョンでは、サインアップ時に <bpt id="p1">[</bpt>Microsoft Office 365 ポータル<ept id="p1">](https://go.microsoft.com/fwlink/?LinkID=324287)</ept>で作成した Microsoft Azure Active Directory(Azure AD) 資格情報を使用してサインインできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Users who are administrators for their organization in Azure AD will be administrators in Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure AD の組織の管理者になっているユーザーは、Microsoft Dynamics Lifecycle Services (LCS) の管理者になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For Microsoft Dynamics AX 2012, organization-level access to LCS is controlled by the association of a person’s Microsoft ID with an organization in CustomerSource or PartnerSource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 では、LCS への組織レベルのアクセスは、個人の Microsoft ID と CustomerSource または PartnerSource の組織との関連付けによって制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Therefore, users of CustomerSource or PartnerSource automatically have access to their organization’s workspace in LCS, and can view all projects that they have been invited to participate in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、CustomerSource または PartnerSource のユーザーは、LCS の組織のワークスペースに自動的にアクセスし、参加するように招待されたすべてのプロジェクトを表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Users who are administrators for their organization in CustomerSource and PartnerSource will be administrators in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource および PartnerSource の組織の管理者になっているユーザーは LCS の管理者になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Although an administrator can invite people who don’t have CustomerSource or PartnerSource credentials to be members of an organization in LCS, we don't recommend this approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は CustomerSource または PartnerSource の資格情報を持っていないユーザーを LCS の組織のメンバーに招待できますが、この方法はお勧めしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>People who are invited to be members of an LCS organization aren't provided with credentials in CustomerSource or PartnerSource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 組織のメンバーとなるよう招待されたユーザーには、CustomerSource または PartnerSource での資格情報が提供されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Project-level access to LCS is by invitation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS へのプロジェクト レベル アクセスは、招待によって行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>You can invite members of your organization to be project owners and team members.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの所有者およびチーム メンバーとして組織のメンバーを招待することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Additionally, you can invite users who aren't part of your organization, and who don't have accounts in Azure AD or CustomerSource or PartnerSource, to be team members.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">また、組織のメンバーではなく、Azure AD、CustomerSource、または PartnerSource のアカンウントを持たないユーザーをチーム メンバーに招待できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>We strongly recommend that you manage all users within your company at the organization level.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">会社内のすべてのユーザーを組織レベルで管理することを強くお勧めします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In that way, you help guarantee that their relationship with your organization is correct in CustomerSource, PartnerSource, and Azure AD.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、組織との関係が CustomerSource、PartnerSource、および Azure AD で正しいことを保証できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Additionally, you help guarantee that users can access the benefits that are available to your organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、ユーザーが組織で利用できる福利厚生にアクセスできることを保証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Manage LCS organization users</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS 組織のユーザーの管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Only an administrator can manage users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者のみユーザーを管理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In CustomerSource, PartnerSource, or Azure AD, associate all the users in your organization who require access to LCS with your organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource、PartnerSource、または Azure AD で、LCS へのアクセスを必要とする組織内のすべてのユーザーを組織と関連付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Users might have to wait up to two business days before they can sign in to LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、LCS にログインできるようになるまでに、2 営業日待機することが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add your users to the appropriate projects in LCS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS の適切なプロジェクトに、ユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Invite a user to an LCS project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS プロジェクトへのユーザーの招待</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Sign in to <bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>LCS<ept id="p1">](https://lcs.dynamics.com/)</ept> にサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click the project to add the user to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをクリックしてユーザーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Click the <bpt id="p1">**</bpt>Project users<ept id="p1">**</ept> tile, and then, on the <bpt id="p2">**</bpt>Project users<ept id="p2">**</ept> page, click the plus sign (<bpt id="p3">**</bpt><ph id="ph1">+</ph><ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロジェクト ユーザー<ept id="p1">**</ept> タイルをクリックし、<bpt id="p2">**</bpt>プロジェクト ユーザー<ept id="p2">**</ept> ページで、プラス記号 (<bpt id="p3">**</bpt><ph id="ph1">+</ph><ept id="p3">**</ept>) をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Enter the user’s email address, select the correct security role, and then click <bpt id="p1">**</bpt>Invite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの電子メール アドレスを入力し、次に正しいセキュリティ ロールを選択して、<bpt id="p1">**</bpt>招待<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Working with CustomerSource and PartnerSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource および PartnerSource での作業</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The information in this section is intended to help you access CustomerSource or PartnerSource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションの情報は、CustomerSource または PartnerSource へのアクセスを支援することを目的としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Signing in to CustomerSource or PartnerSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource または PartnerSource へのサインイン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Visit the <bpt id="p1">[</bpt>CustomerSource sign-in page<ept id="p1">](https://mbs.microsoft.com/customersource/)</ept>, and enter the user name and password for your Microsoft account (previously known as Windows Live ID) to access the site.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>CustomerSource サインイン ページ<ept id="p1">](https://mbs.microsoft.com/customersource/)</ept>に移動し、Microsoft アカウント (以前は Windows Live ID と呼ばれる) のユーザー名とパスワードを入力してサイトにアクセスします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have access to your organization’s CustomerSource account, follow the steps on the <bpt id="p1">[</bpt>How to sign in to CustomerSource<ept id="p1">](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource)</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">組織の CustomerSource 勘定へのアクセスがない場合、「<bpt id="p1">[</bpt>CustomerSource<ept id="p1">](https://mbs.microsoft.com/customersource/northamerica/news-events/news-events/news/NeedAccesstoCustomerSource)</ept> にログインする方法」ページに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Determining the administrator for your organization in CustomerSource or PartnerSource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource または PartnerSource で組織の管理者を決定する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>If you don’t know your CustomerSource administrator, or if your organization doesn’t have a CustomerSource administrator, send an email message to <bpt id="p1">[</bpt>itmbssup@microsoft.com<ept id="p1">](mailto:itmbssup@microsoft.com)</ept> for help.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CustomerSource の管理者がわからない場合、または組織に CustomerSource 管理者がいない場合は、電子メール メッセージを <bpt id="p1">[</bpt>itmbssup@microsoft.com<ept id="p1">](mailto:itmbssup@microsoft.com)</ept> に送信してお問い合わせください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Configuring project security</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト セキュリティのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>You can invite users from inside or outside your organization to join your project as users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトにユーザーとして参加するように、組織の内外からユーザーを招待することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The following table describes the roles that are available for users.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、ユーザーが使用可能なロールを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">役割</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Project owner</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト所有者</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Members of this role have access to all tools in LCS, can add other users in any role, and can delete the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロールのメンバーは LCS のすべてのツールにアクセスでき、他のユーザーを任意のロールに追加することや、プロジェクトを削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Environment manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">環境マネージャー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Members of this role have access to all tools in LCS and can manage cloud-hosted environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロールのメンバーは LCS のすべてのツールにアクセスでき、クラウド ホスト環境を管理できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Project team member</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト チーム メンバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Members of this role have access to all tools in LCS but can&amp;#39;t manage cloud-hosted environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロールのメンバーは LCS のすべてのツールにアクセスできますが、クラウド ホスト環境を管理できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Project team member (prospect)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト チーム メンバー (見込顧客)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Members of this role have limited access to all tools in an LCS project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロールのメンバーは LCS プロジェクトのすべてのツールに制限付きでアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Prospects are users who have been added to a project, but who don&amp;#39;t have an account in VOICE or an Azure AD account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">見込顧客は、プロジェクトに追加されましたが、VOICE または <ph id="1">Azure AD</ph> にアカウントを持っていないユーザーです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You can identify that a user is a prospect, because <bpt id="p1">&lt;strong&gt;</bpt>prospect<ept id="p1">&lt;/strong&gt;</ept> is listed as his or her organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>見込み顧客<ept id="p1">&lt;/strong&gt;</ept> がユーザーの組織として一覧表示されるため、ユーザーが見込み顧客であることを識別することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Operations user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーション ユーザー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Members of this role have access to the following tools in LCS:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロールのメンバーは LCS の次のツールにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>System diagnostics</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム診断</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Issue search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Cloud-powered support</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウドを利用したサポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Updates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">更新</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Cloud-hosted environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド ホスト環境</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>After you've configured security for one project, you can import the users to another project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのプロジェクトのセキュリティをコンフィギュレーションした後は、別のプロジェクトにユーザーをインポートできます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>