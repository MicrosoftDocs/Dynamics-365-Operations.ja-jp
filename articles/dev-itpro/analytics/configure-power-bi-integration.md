<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-power-bi-integration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-power-bi-integration.83728c.15d259d26ece872925290b64c0d7e17063cb1524.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>15d259d26ece872925290b64c0d7e17063cb1524</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\analytics\configure-power-bi-integration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure Power BI integration for workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの Power BI 統合のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to configure a new Microsoft Dynamics 365 for Finance and Operations environment to support integration with PowerBI.com.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、PowerBI.com との統合をサポートする新しい Microsoft Dynamics 365 for Finance and Operations 環境を構成する方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This configuration enables workspaces to show the Power BI control and lets users pin visualizations to a workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンフィギュレーションにより、ワークスペースに Power BI コントロールが表示され、ユーザーはワークスペースに視覚エフェクトをピン留めすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Configure Power BI integration for workspaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースの Power BI 統合のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Microsoft Dynamics 365 for Finance and Operations lets users pin tiles, dashboards, and reports from their own PowerBI.com account to workspaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations では、ユーザー自身の PowerBI.com アカウントからワークスペースに、タイル、ダッシュ ボード、およびレポートをピン留めすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This functionality requires a one-time configuration of your environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能を使用するには、構成を一度設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>An administrator must do this step to enable Finance and Operations and Microsoft Power BI to communicate and authenticate correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者は、Finance and Operations および Microsoft Power BI が正しく通信して認証できるようにするには、この手順を実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Both Finance and Operations and PowerBI.com are cloud-based services.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations と PowerBI.com の両方はクラウドベースのサービスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>For a Finance and Operations workspace to show a Power BI tile, the Finance and Operations server must contact the Power BI service on behalf of a user and access the visualization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations ワークスペースに Power BI タイルを表示するには、Finance and Operations サーバーはユーザーの代理として Power BI サービスに連絡し、視覚エフェクトにアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>It must then redraw the visualization in the Finance and Operations workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そして、Finance and Operations ワークスペースで視覚化を再描画する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The fact that the Finance and Operations server contacts the Power BI service "on behalf of a user" is important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations サーバーが Power BI サービスに「ユーザーの代わりに」連絡するということが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>When a user, such as <ph id="ph1">`D365User@contoso.com`</ph>, contacts the PowerBI.com service, Power BI should show only tiles and reports from the user's PowerBI.com subscription.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">`D365User@contoso.com`</ph> などのユーザーが BI PowerBI.com サービスに連絡するとき、Power BI は、ユーザーの PowerBI.com サブスクリプションからタイルとレポートのみを表示するはずです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>By completing this configuration step, you enable Finance and Operations to contact the PowerBI.com service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成ステップが完了すると、Finance and Operations が PowerBI.com サービスに連絡できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Things you must know before you start</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開始前に知っておく必要事項</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>You must be a system administrator in Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations のシステム管理者である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>This option is available on the <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept>メニューで利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>You must have a PowerBI.com account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com のアカウントが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You can create a trial account if you don't have an account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アカウントを持っていない場合は、試用版アカウントを作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>(A Pro license isn't required for this configuration step.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(プロ ライセンスは、この構成ステップでは必要ありません。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>You must have at least one dashboard and one report in your Power BI account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自分の Power BI アカウントに、少なくとも 1 つのダッシュボードと 1 つのレポートがあることが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Although the dashboard and report aren't required for this configuration step, you might not be able to validate the configuration if you don't have any content in your PowerBI.com account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成ステップでは、ダッシュボードやレポートは必要ではありませんが、PowerBI.com アカウントにコンテンツが含まれていない場合コンフィギュレーションを検証することができないかもしれません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>You must be an administrator for your Microsoft Azure Active Directory (Azure AD) account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure Active Directory (Azure AD) アカウントの管理者である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>If you aren't the administrator, an administrative user must perform this configuration step for you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者ではない場合は、管理者ユーザーはこのコンフィギュレーションの手順をユーザーのために実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The Azure AD domain that is configured for Finance and Operations must be the same domain that you used for your PowerBI.com account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations 用に構成されている Azure AD ドメインは、自分の PowerBI.com アカウントに使用したドメインと同じにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>For example, if you provisioned Finance and Operations in the Contoso.com domain, you must have Power BI accounts in that domain, such as <ph id="ph1">`Tim@ContosoAX7.onmicrosoft.com`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、Contoso.com ドメインで Finance and Operations をプロビジョニングした場合、そのドメイン内に <ph id="ph1">`Tim@ContosoAX7.onmicrosoft.com`</ph> などの Power BI アカウントを持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Registration process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">登録プロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Sign in to <ph id="ph1">https://portal.azure.com/</ph> using an Azure tenant admin account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure テナント管理者アカウントを使用して <ph id="ph1">https://portal.azure.com/</ph> にログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The user who completes this procedure must have Admin rights for the tenant to register applications.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順を完了したユーザーは、アプリケーションを登録するテナントの管理者権限を持っている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Go to <bpt id="p1">**</bpt>Azure Active Directory<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>App registrations<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>New application registration<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Azure Active Directory<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>アプリの登録<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>新しいアプリケーションの登録<ept id="p3">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><ph id="ph1">![</ph>Azure Portal App Registration<ph id="ph2">](media/Azure-Portal-AppRegistration.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>Azure ポータル アプリケーションの登録<ph id="ph2">](media/Azure-Portal-AppRegistration.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Enter the following values:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Name<ept id="p1">**</ept> - Your app name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept> - アプリの名前。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Application type<ept id="p1">**</ept> - Web app/API</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション タイプ<ept id="p1">**</ept> - Web アプリ/API</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source><bpt id="p1">**</bpt>Sign-on URL<ept id="p1">**</ept> - The base URL of your Finance and Operations client and the OAuth suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サインオン URL<ept id="p1">**</ept> - Finance and Operations クライアントと OAuth 接尾語のベース URL。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>For example, <ph id="ph1">http://contosoax7.cloud.dynamics.com/oauth</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<ph id="ph1">http://contosoax7.cloud.dynamics.com/oauth</ph>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Click <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Copy the <bpt id="p1">**</bpt>Application ID<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション ID<ept id="p1">**</ept> をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>This will be used in Finance and Operations to connect to the PowerBI.com service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、PowerBI.com サービスに接続するために Finance and Operations で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Click <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Required permissions<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>Add<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>Select an API<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>Power BI Service (Power BI)<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>必要なアクセス許可<ept id="p2">**</ept><ph id="ph2"> &gt; </ph><bpt id="p3">**</bpt>追加<ept id="p3">**</ept><ph id="ph3"> &gt; </ph><bpt id="p4">**</bpt>API の選択<ept id="p4">**</ept><ph id="ph4"> &gt; </ph><bpt id="p5">**</bpt>Power BI サービス (Power BI)<ept id="p5">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Click <bpt id="p1">**</bpt>Select<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>選択<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Enable Access and click <bpt id="p1">**</bpt>Select<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクセスを有効にして <bpt id="p1">**</bpt>選択<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><ph id="ph1">![</ph>Azure Portal App Permissions<ph id="ph2">](media/Azure-Portal-AppPermissions.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>Azure ポータル アプリのアクセス許可<ph id="ph2">](media/Azure-Portal-AppPermissions.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Click <bpt id="p1">**</bpt>Done<ept id="p1">**</ept> and then click <bpt id="p2">**</bpt>Grant Permissions<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックし、<bpt id="p2">**</bpt>アクセス許可の付与<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>Settings<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>Keys<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>設定<ept id="p1">**</ept><ph id="ph1"> &gt; </ph><bpt id="p2">**</bpt>キー<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Enter a value for <bpt id="p1">**</bpt>Key description<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Expires<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Save<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>キーの説明<ept id="p1">**</ept> および <bpt id="p2">**</bpt>期限切れ日時<ept id="p2">**</ept> に値を入力し、<bpt id="p3">**</bpt>保存<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Make a note of the <bpt id="p1">**</bpt>Application ID<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Application Key<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション ID<ept id="p1">**</ept> および <bpt id="p2">**</bpt>アプリケーション キー<ept id="p2">**</ept> を書き留めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>You will use these values in the next procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順で、これらの値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Specify Power BI settings in Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations での Power BI の設定の指定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In the Finance and Operations client, open the <bpt id="p1">**</bpt>Power BI configuration<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations クライアントで、<bpt id="p1">**</bpt>Power BI の設定<ept id="p1">**</ept>ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><ph id="ph1">![</ph>Power BI configuration dialog<ph id="ph2">](./media/D365-PBI-Configuration.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>Power BIコンフィギュレーション ダイアログ<ph id="ph2">](./media/D365-PBI-Configuration.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Set the <bpt id="p1">**</bpt>Enabled<ept id="p1">**</ept> option to <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効<ept id="p1">**</ept> オプションを <bpt id="p2">**</bpt>はい<ept id="p2">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>In the <bpt id="p1">**</bpt>Application ID<ept id="p1">**</ept> field, enter the <bpt id="p2">**</bpt>Application ID<ept id="p2">**</ept> value that you got from Power BI in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション ID<ept id="p1">**</ept> フィールドで、前の手順で Power BI から取得した<bpt id="p2">**</bpt>アプリケーション ID<ept id="p2">**</ept> の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In the <bpt id="p1">**</bpt>Application Key<ept id="p1">**</ept> field, enter the <bpt id="p2">**</bpt>Application Key<ept id="p2">**</ept> value that you got from Power BI in the previous procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション キー<ept id="p1">**</ept> フィールドで、前の手順で Power BI から取得した<bpt id="p2">**</bpt>アプリケーション キー<ept id="p2">**</ept> の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>You can apply the company filter only if your Power BI content has a table that is named <bpt id="p1">**</bpt>Company<ept id="p1">**</ept> and a column that is named <bpt id="p2">**</bpt>ID<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI のコンテンツに<bpt id="p1">**</bpt>会社<ept id="p1">**</ept>という名前のテーブルおよび <bpt id="p2">**</bpt>ID<ept id="p2">**</ept> という名前の列がある場合にのみ、会社フィルターを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Ready-made Power BI content that is released with Finance and Operations uses this convention.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations によってリリースされた既存の Power BI コンテンツでは、この規約が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Complete the steps in the next section to verify the changes and enable PowerBI.com integrations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のセクションの手順を実行して変更を確認し、PowerBI.com の統合を有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Pin tiles to a workspace</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースにタイルを固定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>To validate the PowerBI.com configuration, click <bpt id="p1">**</bpt>Get started<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com コンフィギュレーションを検証するには、<bpt id="p1">**</bpt>開始する<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>You may need to refresh the browser to apply the changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を適用するにはブラウザーを更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source><ph id="ph1">![</ph>Authorize Power BI<ph id="ph2">](./media/D365-PBI-GetStarted.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>Power BI の承認<ph id="ph2">](./media/D365-PBI-GetStarted.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>If you're starting Power BI from Finance and Operations for the first time, you're prompted to authorize sign-in to Power BI from the Finance and Operations client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations から Power BI をはじめて起動する場合は、Finance and Operations クライアントから、Power BI へのサインインを承認するように求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Select <bpt id="p1">**</bpt>Click here to provide authorization to Power BI<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ここをクリックして Power BI に承認を与える<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Users must complete this step the first time they pin Power BI content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーは、初めて Power BI コンテンツをピン留めするとき、このステップを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The Azure AD consent page asks for your consent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure AD の同意ページが、お客様の同意を求めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>User consent is required for Finance and Operations to access PowerBI.com on behalf of the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations がユーザーに代わって PowerBI.com にアクセスするには、ユーザーの同意が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Select <bpt id="p1">**</bpt>Accept<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>受け入れる<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Because you're already signed in to Azure AD in Finance and Operations, you don't have to enter your credentials again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations で Azure AD に既にサインインしているので、再度資格情報を入力する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>A new tab appears, where you're prompted to authorize the connection between Finance and Operations and Power BI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタブが表示され、Finance and Operations と Power BI の間の接続を承認するように求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Authorize the connection, and then return to the original tab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続を承認し元のタブに戻ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>A list of tiles from your PowerBI.com account appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com アカウントのタイルの一覧が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Select one or more tiles to pin to the selected workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つまたは複数のタイルを選択し、選択したワークスペースにピン留めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><ph id="ph1">![</ph>Validate Power BI integration<ph id="ph2">](./media/D365-PBI-Validation.png)</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">![</ph>Power BI 統合の検証<ph id="ph2">](./media/D365-PBI-Validation.png)</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Troubleshooting common errors</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なエラーのトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>In the procedure above, after you click <bpt id="p1">**</bpt>Accept<ept id="p1">**</ept>, you might receive the following error message if the process is unsuccessful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上の手順で <bpt id="p1">**</bpt>承諾<ept id="p1">**</ept> をクリックした後、プロセスが失敗した場合、次のエラー メッセージが表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Note that the details of the error appear at the bottom of the message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーの詳細がメッセージの下部に表示されていることに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Additional technical information provides clues that can help you determine what went wrong.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の技術情報は、原因を特定するのに役立つヒントを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Some common issues and the resolution steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な問題および解決手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>Error</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Resolution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">解像度</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>The Power BI service is unavailable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI サービスを使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>This issue doesn't occur very often, but the Power BI service might sometimes be unreachable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題は頻繁には発生しませんが、Power BI サービスに到達できないことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You don't have to re-register.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再登録する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Try to pin a tile to a workspace later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">後でタイルをワークスペースに固定してみてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You can't access the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションにアクセスすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You probably didn't select all the check boxes under <bpt id="p1">**</bpt>Step 3 Choose APIs to access<ept id="p1">**</ept> during the registration process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">登録プロセス中に、<bpt id="p1">**</bpt>手順 3 アクセスする API<ept id="p1">**</ept> の下のすべてのチェック ボックスが選択されなかった可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Start Power BI, and re-run the registration process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI を起動し、登録プロセスを再実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The Power BI tiles page is empty (no content is shown).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI タイル ページが空です (コンテンツが表示されません)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Your PowerBI.com account might not have a dashboard or any tiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">PowerBI.com アカウントに、ダッシュ ボードまたはタイルがない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Add a dashboard, such as a sample dashboard, and try to pin a tile again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル ダッシュ ボードなどのダッシュボードを追加して、もう一度をタイルをピン留めしてみてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Error when authorizing Power BI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Power BI の承認時にエラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>On the Azure Admin dashboard, under <bpt id="p1">**</bpt>Users and Groups <ph id="ph1">\&gt;</ph> User settings<ept id="p1">**</ept>, make sure that the <bpt id="p2">**</bpt>Users can consent to apps accessing company data on their behalf<ept id="p2">**</ept> option is set to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure 管理者ダッシュボードの、<bpt id="p1">**</bpt>ユーザーおよびグループ <ph id="ph1">\&gt;</ph> ユーザー設定<ept id="p1">**</ept> の下で、<bpt id="p2">**</bpt>ユーザーはアプリが会社のデータにアクセスすることに同意できる<ept id="p2">**</ept> オプションが <bpt id="p3">**</bpt>はい<ept id="p3">**</ept> に設定されていることを確認します。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>