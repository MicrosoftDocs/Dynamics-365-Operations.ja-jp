<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="troubleshoot-service-authentication.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>troubleshoot-service-authentication.a2d9d0.bb112cf5e4502e9c0566c0e9739ff64ae8dca303.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>bb112cf5e4502e9c0566c0e9739ff64ae8dca303</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\data-entities\troubleshoot-service-authentication.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Troubleshoot service authentication issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス認証問題のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides some tips for troubleshooting issues that involve service authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Troubleshoot service authentication issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス認証問題のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides some tips for troubleshooting issues that involve service authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、サービス認証に関する問題を解決するためのヒントをいくつか示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When you troubleshoot service authentication issues, there are a few basic and common procedures that can help resolve the issues that are most often encountered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サービス認証の問題をトラブルシューティングする場合、もっともよく発生する問題の解決に役立ついくつかの基本的な共通の手順があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>These procedures also provide a hands-on demonstration of how the authentication mechanism works.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、これらの手順では、認証メカニズムの仕組みを実際に実演します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic includes instructions and also lists a few common issues that users have encountered so far.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは手順を説明し、これまでに生じたいくつかの一般的な問題を一覧表示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Inspect the JWT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JWT を検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Capture the JWT from an HTTP request</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTTP 要求から JWT をキャプチャします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Download Fiddler from <ph id="ph1">&lt;https://www.telerik.com/fiddler&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Fiddler を <ph id="ph1">&lt;https://www.telerik.com/fiddler&gt;</ph> からダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Set up HTTPS capture to watch the HTTPS traffic from the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアントから HTTPS トラフィックを監視するには、HTTPS キャプチャを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Find the Open Authorization (OAuth) JSON Web Token (JWT).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">未処理認証 (OAuth) JSON Web トークン (JWT) を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>It's the value of the HTTP "Authorization" header without the "bearer" segment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、「ベアラー」セグメントのない HTTP「認証」ヘッダーの値です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Use a deserializer tool to look at the token contents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">逆シリアル化ツールを使用してトークンの内容を確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Go to <ph id="ph1">&lt;https://jwt.io&gt;</ph>, and paste the JWT into the input panel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&lt;https://jwt.io&gt;</ph> に移動し、入力パネルに JWT を貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>View the contents in the form of name-value pairs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前と値の組でコンテンツを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>See the example that follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Verify that the following information is correct:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の情報が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> – The value corresponds to the Microsoft Azure Active Directory (Azure AD) resource concept.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> - 値は、Microsoft Azure Active Directory (Azure AD) リソースという概念に対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Here are some typical issues that involve "aud":</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「aud」を含む典型的な問題を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> segment of the JWT contains a URI that has a trailing slash.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JWT の <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> セグメントには、末尾にスラッシュを持つ URI が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> segment of the JWT contains a URI that uses an incorrect capitalization style.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JWT の <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The URI must be all lowercase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URI は、すべて小文字であることが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>"appid"<ept id="p1">**</ept> – The value corresponds to the Azure AD Native Client App ID (or Service App ID).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>"appid"<ept id="p1">**</ept> - 値は Azure AD ネイティブ クライアント アプリ ID (またはサービス アプリ ID) に対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>"upn"<ept id="p1">**</ept> – The value corresponds to the user who is being authenticated through a Native Client App.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>"upn"<ept id="p1">**</ept> - 値はネイティブ クライアント アプリケーションを通じて認証されているユーザーに対応します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The following illustration shows an example of the contents of the JWT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、JWT のコンテンツの例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Example of a JWT<ept id="p1">](./media/serviceauthenticationtroubleshooting01.png)](./media/serviceauthenticationtroubleshooting01.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>JWT の例<ept id="p1">](./media/serviceauthenticationtroubleshooting01.png)](./media/serviceauthenticationtroubleshooting01.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Review the event logs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ログを確認</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>You can also look at the event logs of the instance machine, if you have access to the virtual machine (VM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、仮想マシン (VM) に対するアクセス権限がある場合、インスタンス マシンのイベント ログを確認することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Start Event Viewer by running the <bpt id="p1">**</bpt>eventvwr<ept id="p1">**</ept> command from the <bpt id="p2">**</bpt>Run<ept id="p2">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>実行<ept id="p2">**</ept> ウィンドウから <bpt id="p1">**</bpt>eventvwr<ept id="p1">**</ept> コマンドを実行してイベント ビューアーを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Go to the following channels:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のチャンネルに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Application and Services Logs <ph id="ph1">&amp;gt;</ph> Microsoft <ph id="ph2">&amp;gt;</ph> Dynamics <ph id="ph3">&amp;gt;</ph> AX-IntegrationServices <ph id="ph4">&amp;gt;</ph> Channel:Operational (Microsoft-Dynamics-AX-IntegrationServices/Operational)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションとサービス ログ <ph id="ph1">&amp;gt;</ph> Microsoft <ph id="ph2">&amp;gt;</ph> Dynamics <ph id="ph3">&amp;gt;</ph> AX-IntegrationServices <ph id="ph4">&amp;gt;</ph> Channel:Operational (Microsoft-Dynamics-AX-IntegrationServices/運用)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Application and Services Logs <ph id="ph1">&amp;gt;</ph> Microsoft <ph id="ph2">&amp;gt;</ph> Dynamics <ph id="ph3">&amp;gt;</ph> AX-SystemRuntime <ph id="ph4">&amp;gt;</ph> Channel:Operational (Microsoft-Dynamics-AX-SystemRuntime/Operational)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションとサービス ログ <ph id="ph1">&amp;gt;</ph> Microsoft <ph id="ph2">&amp;gt;</ph> Dynamics <ph id="ph3">&amp;gt;</ph> AX-SystemRuntime <ph id="ph4">&amp;gt;</ph> Channel:Operational (Microsoft-Dynamics-AX-SystemRuntime/運用)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Other approaches</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For more information about how OAuth is configured, see <bpt id="p1">[</bpt>Service endpoints<ept id="p1">](services-home-page.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OAuth がコンフィギュレーションされる方法の詳細については、<bpt id="p1">[</bpt>サービス エンドポイント<ept id="p1">](services-home-page.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can also try to call the service in parallel by using your own client code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、自分自身のクライアント コードを使用して、並列でサービスの呼び出しを試みることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>The sample code that we published is available at <ph id="ph1">&lt;https://github.com/Microsoft/Dynamics-AX-Integration&gt;</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">公開されたサンプル コードは <ph id="ph1">&lt;https://github.com/Microsoft/Dynamics-AX-Integration&gt;</ph> で入手できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>If the second method works, you can compare the JWTs from each method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 番目のメソッドが動作する場合は、それぞれのメソッドで JWT を比較できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>AADSTS65001: The user or administrator hasn't consented to use the application</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AADSTS65001: ユーザーまたは管理者がアプリケーションの使用に同意していない</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> segment of the JWT might contain a URI that has a trailing slash.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JWT の <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> セグメントには、末尾にスラッシュを持つ URI が含まれている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The slash must be removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スラッシュを削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> segment of the JWT might contain a URI that uses an incorrect capitalization style.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JWT の <bpt id="p1">**</bpt>"aud"<ept id="p1">**</ept> セグメントには、大文字と小文字の間違ったスタイルを使用する URI が含まれている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The URI must be all lowercase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URI は、すべて小文字であることが必要です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>