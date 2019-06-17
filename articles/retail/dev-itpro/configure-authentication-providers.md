<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="configure-authentication-providers.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>configure-authentication-providers.b6cdaf.f5fe5ec83b0e2a89932eaef7f7c4243c22f6050d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>f5fe5ec83b0e2a89932eaef7f7c4243c22f6050d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\configure-authentication-providers.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure authentication providers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証プロバイダーのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides an overview of the process for configuring a new OpenID authentication provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure authentication providers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">認証プロバイダーのコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides an overview of the process for configuring a new OpenID authentication provider.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、新しい OpenID 認証プロバイダを構成するためのプロセスの概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>The E-Commerce platform uses industry-standard <bpt id="p1">[</bpt>OpenID Connect<ept id="p1">](https://openid.net/connect/)</ept> as the mechanism for authentication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">E コマース プラットフォームは、認証のためのメカニズムとして業界標準の <bpt id="p1">[</bpt>OpenID Connect<ept id="p1">](https://openid.net/connect/)</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This article covers the pages that you use to register the OpenID providers that are used in an online store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、オンライン ストアで使用される OpenID プロバイダーを登録するために使用するページについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Retail Server uses OpenID Connect as the mechanism to support authenticated customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーは、認証された顧客をサポートするメカニズムとして OpenID Connect を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>OpenID Connect is a universally accepted standard that acts as simple and evolved identity provider on top of OAuth 2.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">OpenID 接続は、シンプルで発展した ID プロバイダーとして、OAuth 2.0 に加えて広く受け入れられている標準です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Retail Server can be integrated with both ready-to-use OpenID providers through the Microsoft Azure Access Control service and other independently available providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーは、Microsoft Azure アクセス制御サービスを通じてすぐに使用できる OpenID プロバイダー、およびその他の個別に使用可能なプロバイダーの両方と統合することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>In addition, any custom providers that support OpenID connect can be integrated and registered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、OpenID 接続をサポートするカスタム プロバイダーを統合および登録できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The following illustration shows the step-by-step handshake that occurs between the Retail Server and the E-Commerce front-end server to pass the authentication token for subsequent calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図は、Retail サーバーと電子商取引のフロントエンド サーバーの間で発生し、後続の呼び出しで認証トークンを渡すステップ バイ ステップのハンドシェイクを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>OpenId<ept id="p1">](./media/openid-1024x540.png)](./media/openid.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>OpenId<ept id="p1">](./media/openid-1024x540.png)](./media/openid.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Here is a walkthrough of the process for registering OpenID providers so that they can be used in Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーで使用できるようにするため、OpenID プロバイダーを登録するプロセスのチュートリアルを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>From the Retail IT workspace, go to <bpt id="p1">**</bpt>Retail shared parameters<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>OpenID providers<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売 IT ワークスペースから、<bpt id="p1">**</bpt>小売共有パラメーター<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>OpenID プロバイダー<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>You can use the <bpt id="p1">**</bpt>OpenID providers<ept id="p1">**</ept> page to register additional providers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OpenID プロバイダー<ept id="p1">**</ept> ページを使用すると追加プロバイダーを登録することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For every provider that you support, enter the details of the OpenID provider and the details of the relying parties.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートする各プロバイダーについては、OpenID プロバイダーの詳細および依存する関係者の詳細を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Retail Server uses this information to request and use an authentication token for subsequent calls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーは、この情報を使用し、認証トークンを要求して後続の呼び出しに使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Run distribution schedule 1110.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配送スケジュール 1110 を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For the test online store, edit the web.config file so that it specifies the correct redirect URL and domain, as shown in the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テスト オンライン ストアについては、次の例に示すように、正しいリダイレクト URL とドメインを指定できるように web.config ファイルを編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>If you're using a third-party online store, this information can be stored as required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">第三者のオンライン ストアを使用している場合、この情報を必要に応じて保存できます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>