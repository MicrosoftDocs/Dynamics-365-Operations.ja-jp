<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="prepare-migration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>prepare-migration.a904f9.04eb3ba177d9151bc34ce13e67564864e3e01563.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>04eb3ba177d9151bc34ce13e67564864e3e01563</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\prepare-migration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Prepare to migrate code to Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations へのコードの移行の準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this topic, we will describe the LCS code upgrade service and Visual Studio tools that help you migrate your code and metadata from Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、LCS コード アップグレード サービスと、コードとデータを Dynamics AX 2012 R3 から Microsoft Dynamics 365 for Finance and Operations に移行するのに役立つ Visual Studio ツールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>Most of these steps also apply to code migration between two major versions of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順のほとんどは、Finance and Operations の 2 つのメジャー バージョンの間でのコードの移行にも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Prepare to migrate code to Finance and Operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations へのコードの移行の準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this topic, we will describe the Lifecycle Services (LCS) Code upgrade service and Visual Studio tools that help you migrate your code and metadata from Dynamics AX 2012 R3 to Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Lifecycle Services (LCS) コード アップグレード サービスと、コードとデータを Dynamics AX 2012 R3 から Microsoft Dynamics 365 for Finance and Operations に移行するのに役立つ Visual Studio ツールについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Most of these steps also apply to code migration between two major versions of Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順のほとんどは、Finance and Operations の 2 つのメジャー バージョンの間でのコードの移行にも適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You will need access to a Finance and Operations development environment using Remote Desktop, and be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リモート デスクトップを使用して Finance and Operations 開発環境にアクセスし、このインスタンスの管理者としてプロビジョニングされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>We recommend you become familiar with some of the Dynamics 365 for Operation development, customization and user interface concepts before you upgrade your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをアップグレードする前に、Dynamics 365 for Operation の開発、カスタマイズ、およびユーザー インターフェイスの概念の幾つかをよく理解しておくことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Here are some references.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にいくつかの参照を挙げます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">[</bpt>Development tools<ept id="p1">](../dev-tools/developer-home-page.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>開発ツール<ept id="p1">](../dev-tools/developer-home-page.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt>Models and packages<ept id="p1">](../dev-tools/models.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>モデルとパッケージ<ept id="p1">](../dev-tools/models.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">[</bpt>X++ programming language<ept id="p1">](../dev-ref/xpp-language-reference.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>X++ プログラミング言語<ept id="p1">](../dev-ref/xpp-language-reference.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">[</bpt>Extensions and Overlayering<ept id="p1">](../extensibility/extensibility-home-page.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張機能およびオーバーレイ<ept id="p1">](../extensibility/extensibility-home-page.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source><bpt id="p1">[</bpt>User interface development<ept id="p1">](../user-interface/user-interface-development-home-page.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>ユーザー インターフェイス開発<ept id="p1">](../user-interface/user-interface-development-home-page.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Overview of the code migration process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード移行プロセスの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Model split</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分割されたモデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The Finance and Operations application is split into several packages, or assemblies: Platform Packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations アプリケーションは、いくつかのパッケージ、つまりアセンブリに分割されます (プラットフォーム パッケージ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Application Platform</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション プラットフォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Application Foundation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション基準</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Test Essentials</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Test Essentials</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Application Packages</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Application Suite</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Suite</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Other application packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のアプリケーション パッケージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>ISV and customer code that is migrated from Dynamics AX 2012 R3 will be re-baselined into the correct package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV および Dynamics AX 2012 R3 から移行された顧客コードは、正しいパッケージに再ベースラインされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Auto-migration using the LCS Code Upgrade service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS コードのアップグレード サービスを使用して自動移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The LCS code upgrade service takes a Dynamics AX 2012 R3 model store as input and completes the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS コードのアップグレード サービスは、Dynamics AX 2012 R3 モデル ストアを入力として受け取り、次の作業を完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Converts metadata into the latest format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータを最新の形式に変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Re-baselines metadata, by moving and merging, into the right model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なモデルに移動およびマージすることで、メタデータのベースラインを再度設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Provides an estimation to understand the effort required to upgrade the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションのアップグレードに必要な作業を理解する見積を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Runs migration rules that auto-migrate parts of a solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの一部を自動移行する移行ルールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Runs migration rules that inform developers what to manually fix by using TODOs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TODO を使って手動で修正する内容を開発者に知らせる移行ルールを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Automatically checks-in the upgraded solution into your Azure DevOps project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップグレードされたソリューションを Azure DevOps プロジェクトに自動的にチェックインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>To configure and run the code upgrade service, see <bpt id="p1">[</bpt>Configure and execute the code upgrade service in Lifecycle Services<ept id="p1">](../lifecycle-services/configure-execute-code-upgrade.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード サービスを設定および実行する方法については、[<bpt id="p1">[</bpt>Lifecycle Services でコード アップグレード サービスを構成および実行する<ept id="p1">](../lifecycle-services/configure-execute-code-upgrade.md)</ept>] を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Manual migration steps</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動での移行の手順</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>After you upgrade your code using the LCS code upgrade service configure your developer VM and Azure DevOps to connect to the upgraded code branch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">LCS コード アップグレード サービス構成のコードをアップグレードした後、開発者の VM と Azure DevOps にアップグレードされたコード ブランチに接続します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">[</bpt>Configure your developer VM<ept id="p1">](../dev-tools/configure-developer-vm.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>開発者向け VM を構成する<ept id="p1">](../dev-tools/configure-developer-vm.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">[</bpt>Configure Azure DevOps<ept id="p1">](configure-vso-solution.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Azure DevOps のコンフィギュレーション<ept id="p1">](configure-vso-solution.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The code upgrade service will provide with Visual Studio solutions that you can open to compile your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのアップグレード サービスは、コードをコンパイルするために開くことができる Visual Studio ソリューションを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>A <bpt id="p1">**</bpt>code merge<ept id="p1">**</ept> solution for all elements that contain conflicts and an <bpt id="p2">**</bpt>upgraded<ept id="p2">**</ept> solutions for all your upgraded elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">競合を含むすべての要素向けの<bpt id="p1">**</bpt>コード マージ<ept id="p1">**</ept>ソリューションと、すべてのアップグレードされた要素向けの<bpt id="p2">**</bpt>アップグレード<ept id="p2">**</ept>ソリューション。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Typically, you can compile the application by fixing compilation errors in the order shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、以下の順序でコンパイル エラーを修正して、アプリケーションをコンパイルできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The order is determined based on the package dependencies graph, start with the lowest package in the graph.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">順序はパッケージの依存関係のグラフに基づいて決定され、グラフの中で最も低いパッケージから開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>To determine package dependencies, see <bpt id="p1">[</bpt>Models<ept id="p1">](../dev-tools/models.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パッケージの依存関係を調べるには、[<bpt id="p1">[</bpt>モデル<ept id="p1">](../dev-tools/models.md)</ept>] を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A typical order is Application Platform, Application Foundation, Directory, ...etc., Application Suite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準的な注文は、Application Platform、Application Foundation、Directory など、Application Suite です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>For each of your upgraded models:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各アップグレードされたモデル対象:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Fix merge conflicts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マージの競合を修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Fix compilation errors related to a model split (references across packages).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの分割 (パッケージ全体の参照) に関連するコンパイル エラーを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Typical error messages are:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的なエラー メッセージは次のとおりです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><ph id="ph1">&amp;lt;</ph>Element Type<ph id="ph2">&amp;gt;</ph> X refers to <ph id="ph3">&amp;lt;</ph>Element Type<ph id="ph4">&amp;gt;</ph> Y which does not exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>要素タイプ<ph id="ph2">&amp;gt;</ph> X は、存在しない <ph id="ph3">&amp;lt;</ph>要素タイプ<ph id="ph4">&amp;gt;</ph> Y を参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The name <ph id="ph1">&amp;lt;</ph>Name<ph id="ph2">&amp;gt;</ph> does not denote a class, a table or an extended data type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前 <ph id="ph1">&amp;lt;</ph>Name<ph id="ph2">&amp;gt;</ph> はクラス、テーブル、または拡張データ型を示すものではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For example, your overlayering customizations may be referencing elements or code that are higher in the package dependency graph:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、オーバーレイされたカスタマイズは、パッケージの依存関係グラフの上位にある要素またはコードを参照している場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>A method in the Directory model is referencing a table in the Application Suite package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクトリ モデル内のメソッドは、アプリケーション スイート パッケージ内のテーブルを参照しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>A form in the Directory package is referencing a data source in the Application Suite package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ディレクトリ パッケージ内のフォームは、アプリケーション スイート パッケージ内のデータ ソースを参照しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>You will have to refactor your code to address these dependencies by moving model elements or business logic to higher level packages.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル要素またはビジネス ロジックを上位のパッケージに移動することによって、これらの依存関係に対応するようにコードをリファクターする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">[</bpt>Delegates for Migration<ept id="p1">](delegates-migration.md)</ept> describes how to use delegates to solve some of these issues.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>移行の委任<ept id="p1">](delegates-migration.md)</ept> は、委任を使用してこれらの問題のいくつかを解決する方法を説明しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Fix compilation errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル エラーを修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>After you have resolved all of the compilation errors, all packages will compile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのコンパイル エラーを解決した後は、すべてのパッケージがコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Next, you must complete the following tasks:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、次のタスクを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Address guided code upgrade TODOs and code upgrade-specific best practice warnings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガイド付きコード アップグレード TODO とコード アップグレード固有のベスト プラクティス警告に対処します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Some examples and details are in the sections below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかの例と詳細を以下のセクションに示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Replace deprecated controls, for example, ActiveX or find an alternative.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ActiveX や代替の検索など、非推奨のコントロールを置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Apply form patterns and sub patterns to all forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのフォームにフォーム パターンとサブ パターンを適用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Validate that all scenarios work in multiple browsers with different sizes for custom patterns.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのシナリオが、カスタム パターンに対して異なるサイズで、複数のブラウザーで動作することを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Write and run tests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記述してテストを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Best practice setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>In the Best Practice framework, there is a subset of Best Practice warnings that need to be resolved to complete migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス フレームワークには、移行を完了するために解決する必要があるベスト プラクティス警告のサブセットがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>This applies if you are migrating from Dynamics AX 2012 R3 or earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、Dynamics AX 2012 R3 またはそれ以前から移行する場合に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>In Visual Studio, click <bpt id="p1">**</bpt>Dynamics 365 <ph id="ph1">&amp;gt;</ph> Options <ph id="ph2">&amp;gt;</ph> Best Practices<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>Dynamics 365 <ph id="ph1">&amp;gt;</ph> オプション <ph id="ph2">&amp;gt;</ph> ベスト プラクティス<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>In the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> drop-down menu, select <bpt id="p2">**</bpt>Application Suite<ept id="p2">**</ept> (Repeat with all models you are working on)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept> ドロップダウン メニューで、<bpt id="p2">**</bpt>アプリケーション スイート<ept id="p2">**</ept>を選択します (作業しているすべてのモデルで繰り返します)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>These rules should be set to “ON” while migrating your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのルールは、ソリューションの移行中に「オン」に設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The setting is driven by an XML file in the AxRuleSet folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定は、AxRuleSet フォルダー内の XML ファイルによって実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>For example, see the Application Suite xml file, BPRules.xml, located under C:<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>ApplicationSuite<ph id="ph3">\\</ph>Foundation<ph id="ph4">\\</ph>AxRuleSet.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、C:<ph id="ph1">\\</ph>Packages<ph id="ph2">\\</ph>ApplicationSuite<ph id="ph3">\\</ph>Foundation<ph id="ph4">\\</ph>AxRuleSet の下にある、アプリケーション スイート xml ファイル、BPRules.xml を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>bpupgraderules<ept id="p1">](./media/bpupgraderules.png)](./media/bpupgraderules.png)</ept> To complete the migration, you need to fix all migration-specific Best Practice rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>bpupgraderules<ept id="p1">](./media/bpupgraderules.png)](./media/bpupgraderules.png)</ept> 移行を完了するには、すべての移行固有のベストプラクティスルールを修正する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The errors will show up in the error list as warnings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラーは警告としてエラー リストに表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>In the error list, you will see compiler warnings and best practice errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エラー一覧には、コンパイラの警告やベスト プラクティスのエラーが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Best Practice errors are prefixed with the text <bpt id="p1">**</bpt>BP<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティスのエラーには接頭語として <bpt id="p1">**</bpt>BP<ept id="p1">**</ept> のテキストが付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>For example, <bpt id="p1">**</bpt>BPErrorFormControlPatternUnspecified<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>BPErrorFormControlPatternUnspecified<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Debugging</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>By default, Finance and Operations optimizes the debugging experience for the files that you are working on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、Finance and Operations は作業中のファイルのデバッグ環境を最適化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>As a result, when you step into a file (F11) that is not in your project, the PDBs are not loaded and you can’t debug the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果として、プロジェクトに含まれていないファイル (F11) にステップ インすると、 PDB が読み込まれず、コードをデバッグできなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>To work around this, change the project debugging setting by clicking <bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **<ph id="ph1">&amp;gt;</ph> **Options<ept id="p1">&lt;/strong&gt;</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p2">&lt;strong&gt;</bpt>Debugging<ept id="p2">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この問題を回避するには、<bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **<ph id="ph1">&amp;gt;</ph>**オプション<ept id="p1">&lt;/strong&gt;</ept><ph id="ph2">&amp;gt;</ph><bpt id="p2">&lt;strong&gt;</bpt>デバッグ<ept id="p2">&lt;/strong&gt;</ept> をクリックしてプロジェクトのデバッグ設定を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Verify that the <bpt id="p1">&lt;strong&gt;</bpt>Load symbols only for items in the solution<ept id="p1">&lt;/strong&gt;</ept> check box is not selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>ソリューション内の項目に対してのみシンボルを読み込む<ept id="p1">&lt;/strong&gt;</ept> チェックボックスが選択されていないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This option is selected by default because it improves the debugger speed significantly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、デバッガの速度を大幅に向上させるため、既定で選択されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Another debugging setting that you may want to turn off is Intellitrace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intellitrace をオフにしたい場合、別のデバッグ設定をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Intellitrace collects the complete execution history of an application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intellitrace はアプリケーションの完全な実行履歴を収集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>It creates a lot of noise in the IDE when debugging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグ時に IDE で多くのノイズが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>To turn off Intellitrace, click <bpt id="p1">&lt;strong&gt;</bpt>Options<ept id="p1">&lt;/strong&gt;</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">&lt;strong&gt;</bpt>IntelliTrace<ept id="p2">&lt;/strong&gt;</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">&lt;strong&gt;</bpt>Enable IntelliTrace<ept id="p3">&lt;/strong&gt;</ept>, clear the check box, and then click <bpt id="p4">&lt;strong&gt;</bpt>OK<ept id="p4">&lt;/strong&gt;</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intellitrace をオフにするには、<bpt id="p1">&lt;strong&gt;</bpt>オプション<ept id="p1">&lt;/strong&gt;</ept><ph id="ph1">&amp;gt;</ph><bpt id="p2">&lt;strong&gt;</bpt>IntelliTrace<ept id="p2">&lt;/strong&gt;</ept><ph id="ph2">&amp;gt;</ph><bpt id="p3">&lt;strong&gt;</bpt>IntelliTrace を有効にする<ept id="p3">&lt;/strong&gt;</ept> をクリックしてチェック ボックスをオフにし、<bpt id="p4">&lt;strong&gt;</bpt>OK<ept id="p4">&lt;/strong&gt;</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Note that Intellitrace is only available in the Enterprise version of Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Intellitrace は Visual Studio の Enterprise 版でのみ使用できることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Address code migration tasks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アドレス コード移行タスク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>When metadata is migrated to Finance and Operations, multiple auto-upgrade scripts are run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータを Finance and Operations に移行するとき、複数の自動アップグレード スクリプトが実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In the case where developers need to complete manual migration tasks, TO DOs and Best Practices (BP) have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者が手動で移行タスクを完了する必要がある場合、行う内容とベスト プラクティス (BP) が追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>TO DOs are prefixed with <bpt id="p1">*</bpt><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (Code Upgrade)<ept id="p1">*</ept>, and need to be fixed as a part of code migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TO DO には <bpt id="p1">*</bpt><ph id="ph1">/</ph><ph id="ph2">\*</ph> TODO: (コード アップグレード)<ept id="p1">*</ept> の接頭語が付いており、コード移行の一部として修正する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>BP migration specific rules also need to be fixed as part of code migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">BP 移行固有のルールはコード移行の一環として修正される必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>This example below uses the <bpt id="p1">**</bpt>PurchCommitment<ph id="ph1">\_</ph>PSN<ept id="p1">**</ept> form to walk you through the migration task of fixing navigation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のこの例では、<bpt id="p1">**</bpt>PurchCommitment<ph id="ph1">\_</ph>PSN<ept id="p1">**</ept> フォームを使用して、ナビゲーションを修正する移行タスクについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>Specifically, you will see examples of duplicate buttons and Action Pane TODOs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">具体的には、重複するボタンおよびアクション ウィンドウ TODO などの例が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>In Visual Studio, open <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept>, and search for the form, PurchCommitment<ph id="ph1">\_</ph>PSN.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>を開き、フォーム PurchCommitment<ph id="ph1">\_</ph>PSN を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Right-click the project and select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>In the Model property, select <bpt id="p1">**</bpt>Application Suite<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル プロパティで<bpt id="p1">**</bpt>アプリケーション スイート<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>In the Company property, select FRSI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社プロパティで、FRSI を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Note: The form is located in the French demo data company FRSI.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注記: このフォームは、フランスのデモ データ会社 FRSI に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5 to<ept id="p1">**</ept> see the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してフォームを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>While the form looks complete, there are still code migration tasks necessary to be migration-complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームは完成しているように見えますが、移行を完了するために必要なコード移行タスクがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>i<ept id="p1">](./media/i1.png)](./media/i1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>i<ept id="p1">](./media/i1.png)](./media/i1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Navigation migration tasks</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ナビゲーション移行タスク</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>In Visual Studio, build the project, and then on the toolbar, click <bpt id="p1">**</bpt>View<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Task List<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、プロジェクトをビルドし、ツール バーで<bpt id="p1">**</bpt>表示<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>タスク一覧<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Click the <bpt id="p1">**</bpt>Comments<ept id="p1">**</ept> drop-down list to view the TO DO: (Code Upgrade) tasks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>コメント<ept id="p1">**</ept> ドロップダウン リストをクリックして、TO DO: (コード アップグレード) タスクを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In the list, find the ActionPane TODOs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧で、ActionPane TODO を検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>j<ept id="p1">](./media/j1.png)](./media/j1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>j<ept id="p1">](./media/j1.png)](./media/j1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Code upgrade rule - Action Pane</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード アップグレード ルール - アクション ウィンドウ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In Finance and Operations, the following core actions are provided as system-defined buttons:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、次の主要なアクションはシステム定義ボタンとして提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>New</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新規</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>Delete</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">消去</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Edit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Export</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">輸出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>As part of the auto-migration, the Action Pane rule is run to identify redundant buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動移行の一環として、アクション ペイン ルールは冗長ボタンを識別するために実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>To complete this part of migration, you need to manually:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この移行の部分を完了するには、手動で行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Remove or move the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを削除するか移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Delete redundant controls in the application code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション コード内の冗長なコントロールを削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: In the section below, we will provide examples of how to migrate and modify the code on modeled buttons that replicate system-defined buttons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: 以下のセクションでは、システム定義ボタンを複製するモデル化されたボタンのコードを移行および変更する方法の例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>However, in practice, before making changes similar to those made in this article, the code must first be evaluated with respect to the scenario to determine if it is still needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、実際には、この記事で行われたのと同様の変更を加える前に、シナリオに関してコードをまず評価して、それがまだ必要かどうかを決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>First, fix the TODO for the DeleteCmdButton, which duplicates the system-defined Delete button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、システム定義の削除ボタンと重複する、DeleteCmdButton に対する TODO を修正します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>In Visual Studio, find the TODO shown below, and then double-click the TODO.<bpt id="p1">[</bpt><ph id="ph1">![</ph>k<ept id="p1">](./media/k1.png)](./media/k1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、次に示す "TODO" を検索して、"TODO.<bpt id="p1">[</bpt><ph id="ph1">![</ph>k<ept id="p1">](./media/k1.png)](./media/k1.png)</ept>" をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Replace the TODO and the line of code as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下に示すように、TODO とコード行を置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>The state of the system-defined <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept> button is controlled by the AllowDelete property on the firstmaster datasource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム定義の <bpt id="p1">**</bpt>削除<ept id="p1">**</ept> ボタンの状態は、firstmaster データソースの AllowDelete プロパティによって制御されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>By setting AllowDelete to false, the delete task is kept from executing when the keyboard shortcut is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AllowDelete を false に設定することにより、キーボード ショートカットが使用されている場合に削除タスクは実行されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>In the editor, find and remove DeleteCmdButton from the form design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エディターで、DeleteCmdButton を探してフォーム デザインから削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>l<ept id="p1">](./media/l1.png)](./media/l1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>l<ept id="p1">](./media/l1.png)](./media/l1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S to<ept id="p1">**</ept> save the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押してフォームを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Next, we will focus on the EditCmdButton that duplicates the system Edit button, handing the two TODOs associated with this button as well as removing this button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、システム編集ボタンと重複する EditCmdButton に焦点を当てて、このボタンに関連付けられた 2 つの "仕事" の処理とこのボタンの削除を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>In Visual Studio, find the TODO shown below, and then double-click the TODO.<bpt id="p1">[</bpt><ph id="ph1">![</ph>m<ept id="p1">](./media/m1.png)](./media/m1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、次に示す "TODO" を検索して、"TODO.<bpt id="p1">[</bpt><ph id="ph1">![</ph>m<ept id="p1">](./media/m1.png)](./media/m1.png)</ept>" をダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Because the visibility of the <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button is controlled by the View/Edit mode of the form, you will need to modify this code so it sets that property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタンの表示はフォームの表示/編集モードで制御されるため、このコードを変更してプロパティを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Replace the TODO and the line of code as shown in the following graphic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図に示すように、TODO とコード行を置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Double-click the other TODO for this button.<bpt id="p1">[</bpt><ph id="ph1">![</ph>n<ept id="p1">](./media/n1.png)](./media/n1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ボタンの他の TODO をダブルクリックします。<bpt id="p1">[</bpt><ph id="ph1">![</ph>n<ept id="p1">](./media/n1.png)](./media/n1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Inspect the code on the modeled <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル化された<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>ボタンでコードを検査します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>This logic will need to be moved to the form’s task() method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このロジックは、フォームの task() メソッドに移動する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>On the left side of the Visual Studio designer, right-click <bpt id="p1">**</bpt>Methods<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Override<ept id="p2">**</ept>, and select <bpt id="p3">**</bpt>Task<ept id="p3">**</ept>, to add an override for the form’s Task method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio デザイナーの左側で、<bpt id="p1">**</bpt>メソッド<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>上書き<ept id="p2">**</ept>を右クリックし、<bpt id="p3">**</bpt>タスク<ept id="p3">**</ept>を選択して、フォームのタスク メソッドの上書きを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Update the task method as shown below so that the code from above is triggered when the system-defined <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept> button is clicked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システム定義の <bpt id="p1">**</bpt>編集<ept id="p1">**</ept> ボタンをクリックしたときに上記のコードがトリガーされるように、以下に示すようにタスク メソッドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>In the Editor, find and remove the <bpt id="p1">**</bpt>EditCmdButton<ept id="p1">**</ept> from the form design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エディターで、<bpt id="p1">**</bpt>EditCmdButton<ept id="p1">**</ept> を探してフォーム デザインから削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>o<ept id="p1">](./media/o1.png)](./media/o1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>o<ept id="p1">](./media/o1.png)](./media/o1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Press <bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> to save the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+S<ept id="p1">**</ept> キーを押してフォームを保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to view the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してフォームを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Notice the <bpt id="p1">**</bpt>Delete<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept> buttons in the <bpt id="p3">**</bpt>Commitment<ept id="p3">**</ept> tab have been removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p3">**</bpt>確約<ept id="p3">**</ept>タブの<bpt id="p1">**</bpt>削除<ept id="p1">**</ept>および<bpt id="p2">**</bpt>編集<ept id="p2">**</ept>ボタンが削除されたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Resolve casting exceptions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャスト例外を解決</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>In Finance and Operations, X++ is completely intermediate-language (IL) based and therefore has a stricter runtime type behavior than the interpreted Dynamics AX2 012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、X++ は完全に中間言語 (IL) ベースであるため、解釈された Dynamics <ph id="1">AX</ph> 2012 よりも厳密なランタイム タイプ動作を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This stricter runtime type behavior can generate exceptions in migrated Dynamics AX 2012 R3 metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この厳しいランタイム タイプの動作により、移行された Dynamics AX 2012 R3 メタデータの例外を生成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>It is likely you will encounter these exceptions during your migration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行中にこれらの例外が発生することがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>The casting exceptions can be raised in different runtime scenarios, such as down-casting, casting runtime to design time objects, and side-casting.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャスト例外は、ダウンキャスト、タイム オブジェクトを設計するためのキャスト ランタイム、サイド キャストなど、さまざまな実行時シナリオで発生させることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>In the section below, we will walk through an example where a form, CosJournalName, is generating controls at runtime, and has a type mismatch which causes a .NET exception because it is strongly typed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のセクションで、フォーム CosJournalName が実行時にコントロールを生成し、強い型付けのために .NET 例外を発生させる型の不一致がある例について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Example: Side-casting exception</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例: サイドキャストの例外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>In Visual Studio, select and right-click <bpt id="p1">**</bpt>Project Properties<ept id="p1">**</ept>, and verify that USMF is the default company.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">**</bpt>プロジェクト プロパティ<ept id="p1">**</ept>を選択して右クリックし、USMF が既定の会社であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>Add the display menu item CosJournalName to your project, and set the menu item as your Startup object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メニュー項目に CosJournalName を追加し、スタートアップ オブジェクトとしてメニュー項目を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Add the CosJournalName form to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトに CosJournalName フォームを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Add the cosDimCheckBoxController class to your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトに cosDimCheckBoxController クラスを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>Rebuild your project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトのリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to run the form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してフォームを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>Note that you will get an exception, similar to the following, when running the form.<bpt id="p1">[</bpt><ph id="ph1">![</ph>u<ept id="p1">](./media/u1.png)](./media/u1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームを実行するときに、次のような例外が発生することに注意してください。<bpt id="p1">[</bpt><ph id="ph1">![</ph>u<ept id="p1">](./media/u1.png)](./media/u1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Right-click the class, cosDimCheckBoxController, and then select <bpt id="p1">**</bpt>View Code<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">cosDimCheckBoxController クラスを右クリックし、<bpt id="p1">**</bpt>コードの表示<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Set a breakpoint on the cosDimCheckBoxController::getBuildControl().</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">cosDimCheckBoxController::getBuildControl() にブレークポイントを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Press <bpt id="p1">**</bpt>F5<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>F5<ept id="p1">**</ept> キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The breakpoint will be hit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブレークポイントをヒットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>This is where the casting error occurs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これがキャスティング エラーが発生する場所です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The reason for the casting error is because we are trying to return a control of type: FormBuildCheckboxControl and the object is expecting FormBuildStringControl.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャスト エラーの理由は、型のコントロールを返そうとしているためです。FormBuildCheckboxControl とオブジェクトは FormBuildStringControl を想定しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Hover over the buildcontrol to see the type and notice the differences.<bpt id="p1">[</bpt><ph id="ph1">![</ph>v<ept id="p1">](./media/v1.png)](./media/v1.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">buildcontrol をポイントしてタイプを表示し、相違点に注目します。<bpt id="p1">[</bpt><ph id="ph1">![</ph>v<ept id="p1">](./media/v1.png)](./media/v1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Press <bpt id="p1">**</bpt>F10<ept id="p1">**</ept> to hit the exception.<bpt id="p2">[</bpt><ph id="ph1">![</ph>w<ept id="p2">](./media/w2.png)](./media/w2.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>F10<ept id="p1">**</ept> キーを押して例外をヒットします。<bpt id="p2">[</bpt><ph id="ph1">![</ph>w<ept id="p2">](./media/w2.png)](./media/w2.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Stop debugging.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッグを停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>To fix the exception, change the method declaration from FormBuildStringControl to FormBuildCheckBoxControl.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外を修正するには、メソッド宣言を FormBuildStringControl から FormBuildCheckBoxControl に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>Rebuild the project, and press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをリビルドして、<bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The form should open successfully because the casting error is resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">キャスト エラーが解決されたため、フォームが正常に開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>a<ept id="p1">](./media/a-1024x576.png)](./media/a.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>a<ept id="p1">](./media/a-1024x576.png)](./media/a.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>Migrating context menus and mouse double-click code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューとマウス ダブルクリック コードの移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Refer to these topics to migrate code Dynamics AX 2012 that deals with context menus and mouse double-click actions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテキスト メニューとマウスのダブルクリック アクションを処理する Dynamics AX 2012 コードを移行するには、このトピックを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source><bpt id="p1">[</bpt>Context menus<ept id="p1">](code-migration-context-menus.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>コンテキスト メニュー<ept id="p1">](code-migration-context-menus.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source><bpt id="p1">[</bpt>Mouse double-click<ept id="p1">](code-migration-double-click.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>マウスをダブルクリックします<ept id="p1">](code-migration-double-click.md)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>