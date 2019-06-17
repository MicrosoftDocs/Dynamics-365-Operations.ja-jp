<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="security-architecture.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>security-architecture.2bd582.1e1b8b42c4df43554fd4464909db071e687b58e5.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>1e1b8b42c4df43554fd4464909db071e687b58e5</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\sysadmin\security-architecture.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Security architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ アークテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides an overview of the security architecture of Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations のセキュリティ アーキテクチャの概要を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Security architecture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ アーキテクチャ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides an overview of the security architecture of Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Dynamics 365 for Finance and Operations のセキュリティ アーキテクチャの概要を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When you understand the security architecture of Finance and Operations, you can more easily customize security to fit the requirements of your business.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のセキュリティ アーキテクチャを理解すると、業務の要件に合わせてセキュリティを容易にカスタマイズできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The following diagram provides a high-level overview of the security architecture.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、セキュリティ アーキテクチャの高レベルな概要を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>security-architecture<ept id="p1">](./media/security-architecture.png)](./media/security-architecture.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>security-architecture<ept id="p1">](./media/security-architecture.png)](./media/security-architecture.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Authentication</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>By default, only authenticated users who have user rights in Finance and Operations can establish a connection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、Finance and Operations でユーザー権利を持つ認証済みユーザーのみが接続を確立できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Finance and Operations uses Microsoft Azure Active Directory (AAD) as a primary identity provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、主要な ID プロバイダーとして Microsoft Azure Active Directory (AAD) を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To access the system, users must be provisioned into a Finance and Operations instance and should have a valid AAD account in an authorized tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムにアクセスするには、ユーザーは Finance and Operations インスタンスにプロビジョニングされ、認可されたテナントに有効な AAD アカウントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Authorization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Authorization is the control of access to the Finance and Operations program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">承認は Finance and Operations プログラムへのアクセスをコントロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Security permissions are used to control access to individual elements of the program: menus, menu items, action and command buttons, reports, service operations, web URL menu items, web controls, and fields in the Finance and Operations client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ アクセス許可は、プログラムの個々の要素へのアクセスを制御するために使用されます: メニュー、メニュー項目、アクションおよびコマンド ボタン、レポート、サービス操作、Web URL のメニュー項目、Web コントロール、および Finance and Operations クライアントのフィールド。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>In Finance and Operations, individual security permissions are combined into privileges, and privileges are combined into duties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、個々 のセキュリティ アクセス許可は特権に、特権は職務に組み込まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The administrator grants security roles access to the program by assigning duties and privileges to those roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、セキュリティ ロールに職務権限と権限を割り当てることにより、これらのセキュリティ ロールへのアクセス許可をプログラムに付与します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Finance and Operations uses context-based security to determine access to securable objects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、セキュリティ保護可能なオブジェクトへのアクセスを決定するため、コンテキスト ベースのセキュリティを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>When a privilege is associated with an entry point (such as a menu item or a service operation), a level of access, such as <bpt id="p1">**</bpt>Read<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Delete<ept id="p2">**</ept>, is specified.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特権がエントリ ポイント (メニュー項目またはサービス操作など) に関連付けられているとき、<bpt id="p1">**</bpt>読み取り<ept id="p1">**</ept> または <bpt id="p2">**</bpt>削除<ept id="p2">**</ept> などのアクセス レベルが指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The Finance and Operations authorization subsystem detects the access at run time, when that entry point is accessed, and applies the specified level of access to the securable object that the entry point leads to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations 承認サブシステムは、そのエントリ ポイントにアクセスがあると実行時にアクセスを検出し、エントリ ポイントが導かれるセキュリティ保護可能なオブジェクトに指定したレベルのアクセスを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>This functionality helps to ensure that there is no over-permissioning, and the developer gets the access that he or she intended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、過剰なアクセス権がないことを保証し、開発者が意図したアクセス権を得るのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>For more information about role-based security in Finance and Operations, see <bpt id="p1">[</bpt>Role-based security<ept id="p1">](role-based-security.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations でのロール ベース セキュリティの詳細については、<bpt id="p1">[</bpt>ロール ベース セキュリティ<ept id="p1">](role-based-security.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Data security</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ セキュリティ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Authorization is used to grant access to elements of the program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">承認はプログラムの要素へのアクセスを許可するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>By contrast, data security is used to deny access to tables, fields, and rows in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対照的に、データ セキュリティはデータベース内のテーブル、フィールド、および行へのアクセスを拒否するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use the extensible data security framework to control access to transactional data by assigning data security policies to security roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なデータ セキュリティ フレームワークを使用して、データ セキュリティ ポリシーをセキュリティ ロールに割り当てることにより、トランザクション データへのアクセスを制御します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Data security policies can restrict access to data, based on either the effective date or user data, such as the sales territory or organization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ セキュリティ ポリシーは、有効な日付または営業担当地域や組織などのユーザー データに基づいて、データへのアクセスを制限することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Record-level security, which was a mechanism for securing data in Dynamics AX 2012 and earlier versions, is obsolete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコード レベル セキュリティ (Dynamics AX 2012 以前のバージョンのデータを保護するためのメカニズム) が古くなっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Extensible data security is the recommended mechanism for securing or filtering data in the program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラム内のデータを保護またはフィルター処理するには、拡張可能なデータ セキュリティが推奨されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Additionally, the Table Permissions Framework helps protect some data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、テーブル アクセス許可フレームワークは、一部のデータを保護するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Data security for specific tables is enforced by Application Object Server (AOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のテーブルのデータ セキュリティは、Application Object Server (AOS) によって適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Auditing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">監査</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Auditing of user sign in and sign out is now enabled in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーのログインとサインアウトの監査が Finance and Operations で有効になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The system logs when a user signs in or out of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがアプリケーションにサインインまたはサインアウトすると、システムログが記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>A sign out is logged even if the user's session expires or ends.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーのセッションが期限切れまたは終了する場合でも、サインアウトが記録されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>A system administrator or security administrator can access the audit logs by going to  the <bpt id="p1">**</bpt>User log<ept id="p1">**</ept> page (<bpt id="p2">**</bpt>System administration<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>Inquiries<ept id="p3">**</ept><ph id="ph2"> &gt; </ph><bpt id="p4">**</bpt>User log<ept id="p4">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム管理者またはセキュリティー管理者は、<bpt id="p1">**</bpt>ユーザー ログ<ept id="p1">**</ept> ページ (<bpt id="p2">**</bpt>システム管理<ept id="p2">**</ept><ph id="ph1"> &gt; </ph><bpt id="p3">**</bpt>照会<ept id="p3">**</ept><ph id="ph2"> &gt; </ph><bpt id="p4">**</bpt>ユーザー ログ<ept id="p4">**</ept>) に移動して監査ログにアクセスできます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>