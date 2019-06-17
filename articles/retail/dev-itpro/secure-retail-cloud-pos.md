<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="secure-retail-cloud-pos.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>secure-retail-cloud-pos.045409.ee7e400ea5878ceb1cc84b10c87d0baf3ae4ec90.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ee7e400ea5878ceb1cc84b10c87d0baf3ae4ec90</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\secure-retail-cloud-pos.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Security best practices for Cloud POS in shared environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有環境におけるクラウド POS のセキュリティ ベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>Retail Cloud POS is a web application that runs in the context of a browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS は、ブラウザーのコンテキストで動作する Web アプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This topic provides recommendations that can help secure Retail Cloud POS in a shared environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、共有環境で Retail Cloud POS をセキュリティ保護するための推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Security best practices for Cloud POS in shared environments</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有環境におけるクラウド POS のセキュリティ ベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Retail Cloud POS is a web application that runs in the context of a browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS は、ブラウザーのコンテキストで動作する Web アプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic provides recommendations that can help secure Retail Cloud POS in a shared environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、共有環境で Retail Cloud POS をセキュリティ保護するための推奨事項について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バックグラウンド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Retail Cloud POS is a web application that runs in the context of a web browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS は、Web ブラウザーのコンテキストで動作する Web アプリケーションです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Therefore, it's vulnerable to attack when a user can run any script in the context of the web application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ユーザーが Web アプリケーションのコンテキストで任意のスクリプトを実行できるときに攻撃するのは脆弱です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>One requirement for such attacks is that the user must have physical access to the computer, either in person or by using Remote Desktop Connection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような攻撃の要件の 1 つは、個人またはリモート デスクトップ接続を使用して、ユーザーがコンピューターへ物理的にアクセスすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Vulnerability to attack is an existing issue in most browsers that provide developer tools, and that enable scripts to be run without sufficient privilege control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">攻撃に対する脆弱性は、開発者ツールを提供するほとんどのブラウザーの、また権限の十分な制御なしで実行されるスクリプトを有効にするほとんどのブラウザーの既存の問題です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Because the web application will have little influence over its hosting environment, one way to mitigate security issues is to add defense-in-depth.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web アプリケーションはホスティング環境にほとんど影響力をもたないため、セキュリティの問題を軽減する方法の 1 つは多層防御を追加することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The defense-in-depth can be built by taking advantage of the restrictive policies of both the browser and the operating system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーおよびオペレーティング システムの両方の制限の厳しい強いポリシーを活用して、多層防御を構築できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Hardening instructions for a Retail Cloud POS computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS コンピュータの強化手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Here are some of the defense-in-depth recommendations for the operating system and/or browser that will have an activated instance of Retail Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS のアクティブ化されたインスタンスを持つオペレーティング システムまたはブラウザーの多層防御の推奨事項を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The settings should be enabled or set by a high-privileged account for the operating system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定は、オペレーティング システムの権限の高いアカウントによって有効にするか、設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Retail Cloud POS should be used by a low-privileged account that can't override those settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS は、これらの設定を上書きすることができない低い特権のアカウントで使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>We recommend that you enable all the following settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のすべての設定を有効にすることをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Otherwise, you could create a security loophole that will be prone to security exploitation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、セキュリティを悪用されやすくなるセキュリティ ループホールができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Required<ept id="p1">**</ept> - Disable script execution in the browser's address bar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必須<ept id="p1">**</ept> - ブラウザーのアドレス バーでスクリプトの実行を無効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Required<ept id="p1">**</ept> - Disable the browser's developer console.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必須<ept id="p1">**</ept> - ブラウザーの開発者コンソールを無効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Required<ept id="p1">**</ept> - Retail Cloud POS should be accessed by a low-privileged user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必須<ept id="p1">**</ept> - 権限の低いユーザーが Retail Cloud POS にアクセスする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Required<ept id="p1">**</ept> - Set up group policies to enable a kiosk session.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>必須<ept id="p1">**</ept> - キオスク セッションを有効にするグループ ポリシーを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Recommended<ept id="p1">**</ept> - Set up a proxy to access only whitelisted websites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>推奨<ept id="p1">**</ept> - ホワイトリストに登録されたウェブサイトのみにアクセスするプロキシを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Disable script execution in the address bar of the browser that runs Retail Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS を実行するブラウザのアドレスバーでスクリプトの実行を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>There is no option to disable script execution in the address bar in Internet Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer のアドレス バーでスクリプトの実行を無効にするオプションはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>One alternative is to hide the address bar itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つの方法は、アドレス バー自体を非表示にすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Create a shortcut for the Retail Cloud POS URL, and copy it to each store worker's Microsoft Windows desktop.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS URL のショートカットを作成し、各作業者の Microsoft Windows デスクトップにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Run <bpt id="p1">**</bpt>regedit.exe<ept id="p1">**</ept> to change the registry to disable the Internet Explorer address bar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>regedit.exe<ept id="p1">**</ept> を実行し、Internet Explorer アドレス バーを無効にするレジストリを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source><ph id="ph1">\[</ph>HKEY<ph id="ph2">\_</ph>LOCAL<ph id="ph3">\_</ph>MACHINE<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Policies<ph id="ph6">\\</ph>Microsoft<ph id="ph7">\\</ph>Internet Explorer<ph id="ph8">\\</ph>ToolBars<ph id="ph9">\\</ph>Restrictions<ph id="ph10">\]</ph> "NoNavBar"=dword:00000001</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>HKEY<ph id="ph2">\_</ph>LOCAL<ph id="ph3">\_</ph>MACHINE<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Policies<ph id="ph6">\\</ph>Microsoft<ph id="ph7">\\</ph>Internet Explorer<ph id="ph8">\\</ph>ToolBars<ph id="ph9">\\</ph>Restrictions<ph id="ph10">\]</ph> "NoNavBar"=dword:00000001</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Microsoft Edge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Edge</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>By design, Microsoft Edge prevents script execution in the address bar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">意図的に、Microsoft Edge はアドレス バーでのスクリプトの実行を防ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Therefore, no action is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、何もする必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Disable the developer console in the browser that runs Retail Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS を実行するブラウザーで開発者コンソールを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Use Group Policy Editor to enable the following group policy to disable the Internet Explorer developer console: <ph id="ph1">\\</ph>Administrative Templates<ph id="ph2">\\</ph>Windows Components<ph id="ph3">\\</ph>Internet Explorer<ph id="ph4">\\</ph>Toolbars<ph id="ph5">\\</ph>Turn off Developer Tools="Enabled"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グループ ポリシー エディターを使用し、次のグループ ポリシーを有効にして Internet Explorer の開発者コンソールを無効にします。<ph id="ph1">\\</ph>管理用テンプレート<ph id="ph2">\\</ph>Windows コンポーネント<ph id="ph3">\\</ph>Internet Explorer<ph id="ph4">\\</ph>ツール バー<ph id="ph5">\\</ph>開発者ツール="有効" を無効。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Microsoft Edge</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Edge</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Run <bpt id="p1">**</bpt>regedit.exe<ept id="p1">**</ept> to change the registry to disable the developer console.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>regedit.exe<ept id="p1">**</ept> を実行し、開発者コンソールを無効にするレジストリを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><ph id="ph1">\[</ph>HKEY<ph id="ph2">\_</ph>LOCAL<ph id="ph3">\_</ph>MACHINE<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Policies<ph id="ph6">\\</ph>Microsoft<ph id="ph7">\\</ph>MicrosoftEdge<ph id="ph8">\\</ph>F12<ph id="ph9">\]</ph> "AllowDeveloperTools"=dword:00000000</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\[</ph>HKEY<ph id="ph2">\_</ph>LOCAL<ph id="ph3">\_</ph>MACHINE<ph id="ph4">\\</ph>SOFTWARE<ph id="ph5">\\</ph>Policies<ph id="ph6">\\</ph>Microsoft<ph id="ph7">\\</ph>MicrosoftEdge<ph id="ph8">\\</ph>F12<ph id="ph9">\]</ph> "AllowDeveloperTools"=dword:00000000</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Retail Cloud POS should be accessed by a low-privileged user</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">権限の低いユーザーが Retail Cloud POS にアクセスする必要があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>A point of sale (POS) user must be a non-administrative account that doesn't have privileges to change applied policies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) ユーザーは、適用されたポリシーを変更する権限を持たない管理者以外のアカウントである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Set up group policies to enable a kiosk session</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キオスク セッションを有効にするグループ ポリシーを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>We recommend that you apply the following restrictions for Retail Cloud POS users:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS ユーザーに次の制限を適用することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Restrict access to the file system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル システムへのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Restrict access to Control Panel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール パネルへのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Restrict access to removable drives.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リムーバブル ドライブへのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Restrict access to shells that run commands.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンドを実行するシェルへのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Restrict access to the registry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリへのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Restrict access to application management.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション管理へのアクセスを制限します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The following table lists the group policies to enable kiosk mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルに、キオスク モードを有効にするグループ ポリシーを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The set of policies requires that you start your browser at the sign-in script.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一連のポリシーでは、ログイン スクリプトでブラウザーを起動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>These policies can be adjusted to your requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのポリシーは要件に合わせて調整できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You should always assess any security implications or talk to a specialist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">常に、セキュリティへの影響を評価するか、専門家に相談する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Setting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>State</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">行政単位 (区画)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Comment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コメント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Path</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Enable screen saver</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリーン セーバーの有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Allow DFS roots to be published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DFS ルートの公開をできるように許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><ph id="ph1">\\</ph>Shared Folders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>共有フォルダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>Allow shared folders to be published</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">共有フォルダーの公開を許可</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><ph id="ph1">\\</ph>Shared Folders</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>共有フォルダー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Add Search Internet link to Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューに検索インターネット リンクを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Show Quick Launch on Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーにサイド リンク バーを表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Show the Apps view automatically when the user goes to Start</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが [スタート] に移動したときにアプリケーションのビューを自動的に表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Show "Run as different user" command on Start</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">起動時に [別のユーザーとして実行] コマンドを表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Add the Run command to the Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューへの実行コマンドの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>Show Start on the display the user is using when they press the Windows logo key</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ロゴ キーを押すと、ユーザーが使用しているディスプレイに [スタート] を表示する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Show Windows Store apps on the taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ストア アプリをタスク バーを表示する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Turn off shell protocol protected mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シェル プロトコルの保護モードをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Turn on menu bar by default</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定でメニュー バーをオンにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Turn on Script Execution</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト実行をオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Disabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Windows PowerShell</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Windows PowerShell</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Hide the "Add a program from CD-ROM or floppy disk" option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「CD-ROM またはフロッピーディスクからプログラムの追加」オプションの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Hide the "Add programs from Microsoft" option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「Microsoft からプログラムの追加」オプションの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Hide the "Add programs from your network" option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「ネットワークからプログラムの追加」オプションの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Hide Add New Programs page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいプログラムの追加ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Remove Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムの追加と削除を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Hide the Set Program Access and Defaults page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラム アクセスおよび既定の設定ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Hide Change or Remove Programs page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムの変更または削除ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Go directly to Components Wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンポーネント ウィザードに直接移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Remove Support Information</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポート情報を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Hide Add/Remove Windows Components page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows コンポーネントの追加と削除の非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Add or Remove Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラムの追加と削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Disable the Display Control Panel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール パネルの表示を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Display</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Hide Settings tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設定タブの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Display</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Prevent changing color scheme</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変化する配色を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Prevent changing theme</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーマの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Prevent changing visual style for windows and buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows およびボタンの視覚スタイルの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Prohibit selection of visual style font size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォント サイズの表示スタイルの選択を禁止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Prevent changing color and appearance</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">色や外観の変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Prevent changing desktop background</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップ背景の変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>Prevent changing desktop icons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップ アイコンの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Prevent changing mouse pointers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マウス ポインターの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>Prevent changing screen saver</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリーン セーバーの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Prevent changing sounds</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サウンドの変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Prevent addition of printers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリンターの追加を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Printers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プリンター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Prevent deletion of printers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プリンターの削除を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Printers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プリンター</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>Hide "Set Program Access and Computer Defaults" page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「プログラム アクセスおよびコンピューター既定の設定」ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Hide "Get Programs" page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「プログラムの取得」ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>Hide "Installed Updates" page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「インストールされた更新プログラム」ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Hide "Programs and Features" page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「プログラムと機能」ページの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Hide the Programs Control Panel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムのコントロール パネルの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Hide "Windows Features"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「Windows の機能」の非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Hide "Windows Marketplace"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「Windows マーケットプレース」の非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Programs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>プログラム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>Turn off automatic learning</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動学習をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Regional and Language Options<ph id="ph3">\\</ph>Handwriting personalization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>地域と言語のオプション<ph id="ph3">\\</ph>手書きの個人用設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Hide Regional and Language Options administrative options</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">地域と言語オプションの管理オプションの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source><ph id="ph1">\\</ph>Control Panel<ph id="ph2">\\</ph>Regional and Language Options</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>コントロール パネル<ph id="ph2">\\</ph>地域と言語のオプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>Hide and disable all items on the desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップ上のすべての項目の非表示および無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Remove the Desktop Cleanup Wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップ クリーンアップ ウィザードを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Hide Internet Explorer icon on desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップでの Internet Explorer アイコンの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Remove Computer icon on the desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップのコンピューター アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Remove My Documents icon on the desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップのマイ ドキュメント アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>Hide Network Locations icon on desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップでネットワークの場所のアイコンの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>Remove Properties from the Computer icon context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピュータ アイコン コンテキスト メニューからプロパティを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Remove Properties from the Documents icon context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドキュメント アイコン コンテキスト メニューからプロパティを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Do not add shares of recently opened documents to Network Locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最近開いたドキュメントの共有をネットワークの場所に追加しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>Remove Recycle Bin icon from desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップから [ごみ箱] アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>Remove Properties from the Recycle Bin context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ごみ箱コンテキスト メニューからプロパティを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Do not save settings at exit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">終了時に、設定を保存しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>Turn off Aero Shake window minimizing mouse gesture</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マウス ジェスチャーを最小化する Aero Shake ウィンドウをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>Prevent adding, dragging dropping and closing the Taskbar's toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーのツールバーの追加、ドラッグ アンド ドロップ、終了を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Prohibit adjusting desktop toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーの調整を禁止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source><ph id="ph1">\\</ph>Desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>デスクトップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Force Start to be either full screen size or menu size</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全画面のサイズまたはメニュー サイズのいずれかで強制スタート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>Go to the desktop instead of Start when signing in</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン時に、開始ではなくデスクトップに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>Turn off personalized menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パーソナライズされたメニューをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>Lock the Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーのロック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>Turn off notification area cleanup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通知領域のクリーンアップをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>Remove Balloon Tips on Start Menu items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[スタート] メニューの項目のバルーン ヒントを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>Prevent users from customizing their Start Screen</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが開始画面をカスタマイズできないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>Remove common program groups from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[スタート] メニューから共通プログラム グループを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>Remove Favorites menu from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから [お気に入り] メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>Remove Search link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから検索リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>Remove frequent programs list from the Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからよく使うプログラムの一覧を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Remove Games link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからゲーム リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>Remove Help menu from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから [ヘルプ] メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Turn off user tracking</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーの追跡をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>Remove All Programs list from the Start menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからすべてのプログラムの一覧を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="461">
          <source>Remove Network Connections from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからネットワーク接続を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="462">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="463">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="464">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="465">
          <source>Remove pinned programs list from the Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからピン留めされたプログラムの一覧を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="466">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="467">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="468">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="469">
          <source>Do not keep history of recently opened documents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最近使用したファイルの履歴を保存しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="470">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="471">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="472">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="473">
          <source>Remove Recent Items menu from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから [最近使った項目] メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="474">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="475">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="476">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="477">
          <source>Do not use the search-based method when resolving shell shortcuts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シェルのショートカットを解決する際は、検索に基づくメソッドを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="478">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="479">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="480">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="481">
          <source>Do not use the tracking-based method when resolving shell shortcuts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シェルのショートカットを解決する際は、追跡に基づくメソッドを使用しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="482">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="483">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="484">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="485">
          <source>Remove Run menu from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから [ファイル名を指定して実行] メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="486">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="487">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="488">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="489">
          <source>Remove Default Programs link from the Start menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから既定のプログラム リンクを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="490">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="491">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="492">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="493">
          <source>Remove Documents icon from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからドキュメント アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="494">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="495">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="496">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="497">
          <source>Remove Music icon from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからミュージック アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="498">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="499">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="500">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="501">
          <source>Remove Network icon from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからネットワーク アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="502">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="503">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="504">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="505">
          <source>Remove Pictures icon from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからピクチャ アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="506">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="507">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="508">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="509">
          <source>Do not search communications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コミュニケーションを検索しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="510">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="511">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="512">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="513">
          <source>Remove Search Computer link</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターを検索リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="514">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="515">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="516">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="517">
          <source>Remove See More Results / Search Everywhere link</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに結果を表示/すべての場所の検索リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="518">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="519">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="520">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="521">
          <source>Do not search for files</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルを検索しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="522">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="523">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="524">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="525">
          <source>Do not search Internet</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネットを検索しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="526">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="527">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="528">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="529">
          <source>Do not search programs and Control Panel items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムやコントロール パネルの項目を検索しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="530">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="531">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="532">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="533">
          <source>Remove programs on Settings menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[設定] メニューのプログラムを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="534">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="535">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="536">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="537">
          <source>Prevent changes to Taskbar and Start Menu Settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーとスタート メニューの設定を変更できないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="538">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="539">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="540">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="541">
          <source>Remove Downloads link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからダウンロード リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="542">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="543">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="544">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="545">
          <source>Remove Homegroup link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからホームグループ リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="546">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="547">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="548">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="549">
          <source>Remove Recorded TV link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから録画された TV リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="550">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="551">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="552">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="553">
          <source>Remove user's folders from the Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからユーザーのフォルダーを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="554">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="555">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="556">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="557">
          <source>Remove Videos link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからビデオ リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="558">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="559">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="560">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="561">
          <source>Force classic Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従来のスタート メニューの強制</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="562">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="563">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="564">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="565">
          <source>Remove Clock from the system notification area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム通知領域から時計を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="566">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="567">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="568">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="569">
          <source>Prevent grouping of taskbar items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バー項目のグループ化を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="570">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="571">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="572">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="573">
          <source>Do not display any custom toolbars in the taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーで顧客ツールバーを表示しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="574">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="575">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="576">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="577">
          <source>Remove access to the context menus for the taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーのコンテキスト メニューへのアクセス許可を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="578">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="579">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="580">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="581">
          <source>Hide the notification area</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通知領域の非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="582">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="583">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="584">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="585">
          <source>Prevent users from uninstalling applications from Start</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが [スタート] からアプリケーションをアンインストールできないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="586">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="587">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="588">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="589">
          <source>Remove user folder link from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからユーザー フォルダー リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="590">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="591">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="592">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="593">
          <source>Remove user name from Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューからユーザー名を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="594">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="595">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="596">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="597">
          <source>Remove links and access to Windows Update</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Update へのリンクおよびアクセスを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="598">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="599">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="600">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="601">
          <source>Remove the "Undock PC" button from the Start Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタート メニューから [PC の固定解除] ボタンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="602">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="603">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="604">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="605">
          <source>Remove Notifications and Action Center</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通知とアクション センターを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="606">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="607">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="608">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="609">
          <source>Disable showing balloon notifications as toasts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バルーン通知をトーストとして表示しないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="610">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="611">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="612">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="613">
          <source>Remove the Security and Maintenance icon</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティと保守アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="614">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="615">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="616">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="617">
          <source>Remove the networking icon</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワーク アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="618">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="619">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="620">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="621">
          <source>Remove the battery meter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バッテリ メーターを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="622">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="623">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="624">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="625">
          <source>Remove the volume control icon</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">音量コントロール アイコンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="626">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="627">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="628">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="629">
          <source>Turn off feature advertisement balloon notifications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィーチャー広告バルーン通知をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="630">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="631">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="632">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="633">
          <source>Do not allow pinning Store app to the Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ストア アプリをタスクバーに固定することを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="634">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="635">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="636">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="637">
          <source>Do not allow pinning items in Jump Lists</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">項目をジャンプ リストに固定することを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="638">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="639">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="640">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="641">
          <source>Do not allow pinning programs to the Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラムをタスクバーに固定することを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="642">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="643">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="644">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="645">
          <source>Do not display or track items in Jump Lists from remote locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">遠隔拠点からジャンプ リストの品目を表示または追跡しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="646">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="647">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="648">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="649">
          <source>Turn off automatic promotion of notification icons to the taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスクバーへの通知アイコンの自動プロモーションをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="650">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="651">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="652">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="653">
          <source>Lock all taskbar settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのタスク バー設定のロック</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="654">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="655">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="656">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="657">
          <source>Prevent users from adding or removing toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがツールバーの追加または削除できないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="658">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="659">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="660">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="661">
          <source>Prevent users from rearranging toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがツールバーの配置を変更できないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="662">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="663">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="664">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="665">
          <source>Do not allow taskbars on more than one display</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つ以上のディスプレイにタスク バーを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="666">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="667">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="668">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="669">
          <source>Turn off all balloon notifications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのバルーン通知をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="670">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="671">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="672">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="673">
          <source>Remove pinned programs from the Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク バーからピン留めされたプログラムを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="674">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="675">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="676">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="677">
          <source>Prevent users from moving taskbar to another screen dock location</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがタスク バーを別の画面ドックの場所に移動することを防ぐ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="678">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="679">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="680">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="681">
          <source>Prevent users from resizing the taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがタスク バーのサイズを変更できないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="682">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="683">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="684">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="685">
          <source>Turn off taskbar thumbnails</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスクバーのサムネイルをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="686">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="687">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="688">
          <source><ph id="ph1">\\</ph>Start Menu and Taskbar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>スタート メニューとタスクバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="689">
          <source>Remove Task Manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タスク マネージャーの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="690">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="691">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="692">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Ctrl+Alt+Del Options</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>Ctrl+Alt+Del オプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="693">
          <source>Code signing for device drivers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイス ドライバーのコード署名</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="694">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="695">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="696">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Driver Installation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>ドライバーのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="697">
          <source>Turn off Windows Update device driver search prompt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows Update デバイス ドライバーの検索プロンプトをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="698">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="699">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="700">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Driver Installation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>ドライバーのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="701">
          <source>Disallow selection of Custom Locales</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタム ロケールの選択を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="702">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="703">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="704">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Locale Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>ロケール サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="705">
          <source>Disallow changing of geographic location</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">地理的位置の変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="706">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="707">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="708">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Locale Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>ロケール サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="709">
          <source>Disallow user override of locale settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ロケール設定のユーザーによる上書きを禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="710">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="711">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="712">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Locale Services</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>ロケール サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="713">
          <source>CD and DVD: Deny read access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CD および DVD: 読み取りアクセス権を拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="714">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="715">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="716">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="717">
          <source>CD and DVD: Deny write access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CD および DVD: 書き込みアクセス権を拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="718">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="719">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="720">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="721">
          <source>Floppy Drives: Deny read access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フロッピー ドライブ: 読み取りアクセスを拒否します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="722">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="723">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="724">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="725">
          <source>Floppy Drives: Deny write access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フロッピー ドライブ: 書き込みアクセスを拒否します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="726">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="727">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="728">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="729">
          <source>Removable Disks: Deny read access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リムーバブル ディスク: 読み取りアクセスを拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="730">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="731">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="732">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="733">
          <source>Removable Disks: Deny write access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リムーバブル ディスク: 書き込みアクセスを拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="734">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="735">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="736">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="737">
          <source>All Removable Storage classes: Deny all access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのリムーバブル ストレージ クラス: すべてのアクセスを拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="738">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="739">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="740">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="741">
          <source>Tape Drives: Deny read access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テープ ドライブ: 読み取りアクセスを拒否します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="742">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="743">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="744">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="745">
          <source>Tape Drives: Deny write access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テープ ドライブ: 書き込みアクセスを拒否します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="746">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="747">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="748">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="749">
          <source>WPD Devices: Deny read access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WPD デバイス: 読み取りアクセスを拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="750">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="751">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="752">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="753">
          <source>WPD Devices: Deny write access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">WPD デバイス: 書き込みアクセスを拒否</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="754">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="755">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="756">
          <source><ph id="ph1">\\</ph>System<ph id="ph2">\\</ph>Removable Storage Access</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>システム<ph id="ph2">\\</ph>リムーバル ストレージ アクセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="757">
          <source>Prevent access to the command prompt</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド プロンプトへのアクセスを禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="758">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="759">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="760">
          <source><ph id="ph1">\\</ph>System</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>System</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="761">
          <source>Prevent access to registry editing tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジストリ編集ツールへのアクセスを禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="762">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="763">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="764">
          <source><ph id="ph1">\\</ph>System</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>System</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="765">
          <source>Prevent the wizard from running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ウィザードが実行されないようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="766">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="767">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="768">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Add features to Windows 10</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Windows 10 への機能の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="769">
          <source>Turn off Program Compatibility Assistant</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プログラム互換性アシスタントをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="770">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="771">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="772">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Application Compatibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>アプリケーションの互換性</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="773">
          <source>Search, Share, Start, Devices and Settings don't appear when the mouse is pointing to the upper-right corner of the screen</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マウスが画面の右上隅をポイントしたとき、検索、共有、開始、デバイスおよび設定は表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="774">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="775">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="776">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="777">
          <source>Disable help tips</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ ヒントを無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="778">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="779">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="780">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="781">
          <source>Turn off tracking of app usage</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの使用状況の追跡をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="782">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="783">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="784">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="785">
          <source>Do not show recent apps when the mouse is pointing to the upper-left corner of the screen</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面の左上にマウスをポイントした際は、最新のアプリケーションを表示しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="786">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="787">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="788">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="789">
          <source>Prevent users from replacing the Command Prompt with Windows PowerShell in the menu they see when they right-click the lower-left corner or press the Windows logo key+X</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが、左下隅を右クリックするか、Windows ロゴ キーを押しながら X キーを押したときに表示される Windows PowerShell にコマンド プロンプトを置き換えることができないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="790">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="791">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="792">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="793">
          <source>Turn off switching between recent apps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最近アプリの切り替えをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="794">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="795">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="796">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Edge UI</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Edge UI</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="797">
          <source>Turn on or off details pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細ウィンドウのオン/オフを切り替え</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="798">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="799">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="800">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer<ph id="ph3">\\</ph>Explorer Frame Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー<ph id="ph3">\\</ph>エクスプローラー フレーム ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="801">
          <source>Turn off Preview Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[プレビュー] ウィンドウをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="802">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="803">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="804">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer<ph id="ph3">\\</ph>Explorer Frame Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー<ph id="ph3">\\</ph>エクスプローラー フレーム ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="805">
          <source>Do not display the Welcome Center at user logon</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーのログオン時に、ウェルカム センターを表示しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="806">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="807">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="808">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="809">
          <source>Turn on Classic Shell</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラシック シェルにオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="810">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="811">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="812">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="813">
          <source>Remove CD Burning features</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CD 作成機能を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="814">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="815">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="816">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="817">
          <source>Remove DFS tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DFS タブの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="818">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="819">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="820">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="821">
          <source>Hide these specified drives in My Computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイ コンピュータで指定したこれらのドライブの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="822">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="823">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="824">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="825">
          <source>No Entire Network in Network Locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワークの場所でネットワーク全体がありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="826">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="827">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="828">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="829">
          <source>Remove File menu from File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスプローラーから [ファイル] メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="830">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="831">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="832">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="833">
          <source>Do not allow Folder Options to be opened from the Options button on the View tab of the ribbon</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォルダー オプションを、リボンの表示タブ上のオプション ボタンから開くことを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="834">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="835">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="836">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="837">
          <source>Remove Hardware tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[ハードウェア] タブの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="838">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="839">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="840">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="841">
          <source>Hide the Manage item on the File Explorer context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル エクスプ ローラーのコンテキスト メニューで管理項目の非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="842">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="843">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="844">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="845">
          <source>Remove Shared Documents from My Computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイ コンピューターから共有ドキュメントを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="846">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="847">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="848">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="849">
          <source>Remove "Map Network Drive" and "Disconnect Network Drive"</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「ネットワーク ドライブの割り当て」および「ネットワーク ドライブの切断」を削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="850">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="851">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="852">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="853">
          <source>Remove the Search the Internet "Search again" link</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット検索の「再度検索」リンクを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="854">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="855">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="856">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="857">
          <source>Remove Security tab</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[セキュリティ] タブを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="858">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="859">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="860">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="861">
          <source>Remove Search button from File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスプローラーから検索ボタンを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="862">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="863">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="864">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="865">
          <source>Remove File Explorer's default context menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エクスプローラーの既定のコンテキスト メニューを削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="866">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="867">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="868">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="869">
          <source>Prevent access to drives from My Computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マイ コンピューターからドライブへのアクセスを禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="870">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="871">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="872">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="873">
          <source>Turn off Windows+X hotkeys</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows+X のホットキーをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="874">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="875">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="876">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="877">
          <source>No Computers Near Me in Network Locations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワークの場所で近くにコンピューターがありません</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="878">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="879">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="880">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="881">
          <source>Request credentials for network installations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ネットワークのインストールの資格情報を要求</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="882">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="883">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="884">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="885">
          <source>Prevent users from adding files to the root of their Users Files folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが、ユーザー ファイル フォルダーのルートにファイルを追加するを防ぎます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="886">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="887">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="888">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>File Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ファイル エクスプローラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="889">
          <source>Turn off Accelerators</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクセラレータをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="890">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="891">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="892">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Accelerators</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>アクセラレータ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="893">
          <source>File menu: Disable closing the browser and Explorer windows</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル メニュー: ブラウザーおよびエクスプ ローラー ウィンドウを閉じるを無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="894">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="895">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="896">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="897">
          <source>File menu: Disable Save As... menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル メニュー: ... メニュー オプションとして保存を無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="898">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="899">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="900">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="901">
          <source>File menu: Disable Save As Web Page Complete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル メニュー: Web ページの完了として保存を無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="902">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="903">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="904">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="905">
          <source>File menu: Disable New menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル メニュー: 新しいメニュー オプションを無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="906">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="907">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="908">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="909">
          <source>File menu: Disable Open menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル メニュー: オープン メニュー オプションを無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="910">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="911">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="912">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="913">
          <source>Help menu: Remove 'Send Feedback' menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ メニュー: 「フィードバックの送信」メニュー オプションを削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="914">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="915">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="916">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="917">
          <source>Help menu: Remove 'For Netscape Users' menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ メニュー: 「ネットスケープ ユーザー用」メニュー オプションを削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="918">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="919">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="920">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="921">
          <source>Help menu: Remove 'Tip of the Day' menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ メニュー: 「今日のヒント」メニュー オプションを削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="922">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="923">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="924">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="925">
          <source>Help menu: Remove 'Tour' menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ヘルプ メニュー: 「ツアー」メニュー オプションを削除します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="926">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="927">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="928">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="929">
          <source>Turn off Shortcut Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[ショートカット] メニューをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="930">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="931">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="932">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="933">
          <source>Hide Favorites menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">お気に入りメニューの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="934">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="935">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="936">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="937">
          <source>Disable Open in New Window menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいウィンドウ メニュー オプションで開くを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="938">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="939">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="940">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="941">
          <source>Turn off Print Menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[印刷] メニューをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="942">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="943">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="944">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="945">
          <source>Turn off the ability to launch report site problems using a menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メニュー オプションを使用してレポート サイトの問題を起動する機能をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="946">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="947">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="948">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="949">
          <source>Disable Save this program to disk option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプログラムをディスクに保存するオプションを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="950">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="951">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="952">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="953">
          <source>Tools menu: Disable Internet Options... menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[ツール] メニュー: インターネット オプションを無効にする...メニュー オプション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="954">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="955">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="956">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="957">
          <source>View menu: Disable Full Screen menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メニュー: 全画面表示メニューのオプションの無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="958">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="959">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="960">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="961">
          <source>View menu: Disable Source menu option</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メニュー: ソース メニュー オプションの無効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="962">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="963">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="964">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Browser menus</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ブラウザー メニュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="965">
          <source>Turn off Developer Tools</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツールをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="966">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="967">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="968">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="969">
          <source>Turn off toolbar upgrade tool</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツールバーのアップグレード ツールをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="970">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="971">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="972">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="973">
          <source>Hide the Command bar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コマンド バーの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="974">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="975">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="976">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="977">
          <source>Hide the status bar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ステータス バーの非表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="978">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="979">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="980">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="981">
          <source>Disable customizing browser toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザー ツールバーのカスタマイズを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="982">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="983">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="984">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="985">
          <source>Disable customizing browser toolbar buttons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザー ツールバーのカスタマイズ ボタンを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="986">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="987">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="988">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>Toolbars</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer<ph id="ph3">\\</ph>ツールバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="989">
          <source>Turn off add-on performance notifications</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドオンのパフォーマンス通知をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="990">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="991">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="992">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="993">
          <source>Do not allow users to enable or disable add-ons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーに有効または無効アドオンを許可しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="994">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="995">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="996">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="997">
          <source>Disable changing Advanced page settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高度なページ設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="998">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="999">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1000">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1001">
          <source>Turn off Favorites bar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">お気に入りバーをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1002">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1003">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1004">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1005">
          <source>Prevent per-user installation of ActiveX controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ActiveX コントロールのユーザー単位のインストールを禁止しする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1006">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1007">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1008">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1009">
          <source>Turn off Reopen Last Browsing Session</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最終閲覧セッションの再開をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1010">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1011">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1012">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1013">
          <source>Turn off Tab Grouping</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タブのグループ化をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1014">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1015">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1016">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1017">
          <source>Prevent managing the phishing filter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィッシング フィルターの管理を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1018">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1019">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1020">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1021">
          <source>Turn off Managing SmartScreen Filter for Internet Explorer 8</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer 8 で SmartScreen フィルターの管理をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1022">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1023">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1024">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1025">
          <source>Prevent managing SmartScreen Filter</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SmartScreen フィルターの管理を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1026">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1027">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1028">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1029">
          <source>Turn off the Security Settings Check feature</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セキュリティ設定のチェック機能をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1030">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1031">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1032">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1033">
          <source>Enforce full-screen mode</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フルスクリーン モードの実施</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1034">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1035">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1036">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1037">
          <source>Disable Import/Export Settings wizard</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インポート/エクスポート設定ウィザードを無効にします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1038">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1039">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1040">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1041">
          <source>Prevent Internet Explorer Search box from appearing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer 検索ボックスが表示されないようにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1042">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1043">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1044">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1045">
          <source>Turn off Quick Tabs functionality</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クイック タブの機能をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1046">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1047">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1048">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1049">
          <source>Turn off tabbed browsing</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タブ ブラウズをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1050">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1051">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1052">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1053">
          <source>Disable changing Automatic Configuration settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動構成設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1054">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1055">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1056">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1057">
          <source>Disable changing Temporary Internet files settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターネット一時ファイル設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1058">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1059">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1060">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1061">
          <source>Disable changing Calendar and Contact settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">予定表と連絡先の設定を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1062">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1063">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1064">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1065">
          <source>Disable changing certificate settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1066">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1067">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1068">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1069">
          <source>Disable changing default browser check</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定のブラウザー チェックを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1070">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1071">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1072">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1073">
          <source>Disable changing color settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カラー設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1074">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1075">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1076">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1077">
          <source>Disable changing connection settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">接続設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1078">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1079">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1080">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1081">
          <source>Disable changing font settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォント設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1082">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1083">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1084">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1085">
          <source>Disable changing language settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">言語設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1086">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1087">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1088">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1089">
          <source>Disable changing link color settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リンク カラー設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1090">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1091">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1092">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1093">
          <source>Disable changing Messaging settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージ設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1094">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1095">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1096">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1097">
          <source>Prevent managing pop-up exception list</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポップアップ例外一覧の管理を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1098">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1099">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1100">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1101">
          <source>Turn off pop-up management</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポップアップ管理をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1102">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1103">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1104">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1105">
          <source>Disable changing Profile Assistant settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロファイル アシスタント設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1106">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1107">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1108">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1109">
          <source>Prevent changing proxy settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロキシ設定の変更を禁止する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1110">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1111">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1112">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1113">
          <source>Disable changing ratings settings</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">評価設定の変更を無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1114">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1115">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1116">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1117">
          <source>Turn off the auto-complete feature for web addresses</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web アドレスの自動補完機能をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1118">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1119">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1120">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1121">
          <source>Turn off suggestions for all user-installed providers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーがインストールしたすべてのプロバイダの推奨事項をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1122">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1123">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1124">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1125">
          <source>Turn off the quick pick menu</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[クイック ピック] メニューをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1126">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1127">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1128">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1129">
          <source>Search: Disable Find Files via F3 within the browser</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索: ブラウザー内で F3 キーを使用したファイルの検索を無効化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1130">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1131">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1132">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1133">
          <source>Search: Disable Search Customization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索: 検索のカスタマイズを無効にする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1134">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1135">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1136">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1137">
          <source>Turn off ability to pin sites in Internet Explorer on the desktop</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップの Internet Explorer でサイトをピン留めする機能をオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1138">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1139">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1140">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Internet Explorer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>Internet Explorer</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1141">
          <source>Turn off the offer to update to the latest version of Windows</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows の最新バージョンに更新するオファーをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1142">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1143">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1144">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ストア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1145">
          <source>Turn off the Store application</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗アプリケーションをオフにする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1146">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1147">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1148">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Store</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>ストア</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1149">
          <source>Prohibit New Task Creation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいタスクの作成を禁止</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1150">
          <source>Enabled</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1151">
          <source>No</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1152">
          <source><ph id="ph1">\\</ph>Windows Components<ph id="ph2">\\</ph>Task Scheduler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">\\</ph>Windows コンポーネント<ph id="ph2">\\</ph>タスク スケジューラ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1153">
          <source>Set up a proxy to access only whitelisted websites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ホワイトリストに登録されたウェブサイトのみにアクセスするプロキシを設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1154">
          <source>You can define a list of websites that a store worker (cashier) requires for normal operations, and set up an administrator-controlled proxy that has access only to these websites.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日常業務で店員 (レジ担当者) が必要とする Web サイトの一覧を定義し、これらの Web サイトにのみアクセス権を持つ管理者制御のプロキシを設定することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1155">
          <source>Retail Cloud POS requires access to the following websites:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS には、次の Web サイトへのアクセスが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1156">
          <source>Retail Cloud POS website</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS Web サイト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1157">
          <source>Microsoft Azure Active Directory sign-in page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Azure Active Directory のサインイン ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1158">
          <source>Retail Server website</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー Web サイト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1159">
          <source>Bing Maps resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Bing Maps リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1160">
          <source>Media resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メディア リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="1161">
          <source>Credit Card Payment acceptance page (optional)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クレジット カード支払引受ページ (オプション)</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>