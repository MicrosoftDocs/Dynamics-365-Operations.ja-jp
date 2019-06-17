<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="refactoring-over-layering.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>refactoring-over-layering.310249.ab532f76f8c9287e25f0fcf7f8141e79a37f731f.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>ab532f76f8c9287e25f0fcf7f8141e79a37f731f</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\refactoring-over-layering.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Relax model restrictions to refactor overlayering into extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能にオーバーレイをリファクタリングするモデルの制限を緩和</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about relaxing model restrictions to enable the refactoring of over-layering into extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、オーバーレイを拡張機能にリファクタリングできるように、モデルの制限を緩和する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>This is needed because the models are sealed in Microsoft Dynamics 365 for Finance and Operations 8.0.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、モデルが Microsoft Dynamics 365 for Finance and Operations 8.0 にシールされているために、必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Relax model restrictions to refactor overlayering into extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバレイを拡張機能にリファクタリングするため、モデルの制限を緩和する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Dynamics 365 for Finance and Operations 8.0, and all subsequent releases, will not allow Microsoft’s code to be customized by using over-layering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations 8.0 およびこれ以降のすべてのリリースでは、Microsoft のコードをカスタマイズすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Instead, extension capabilities should be used to modify and add behavior.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">動作の変更や追加には、拡張機能を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The "no over-layering" restriction is a key part of the evolution of the product toward providing customers with a cloud ERP service that is simple to update and always running the most recent version possible to allow all customers to receive the benefits of the latest features and fixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「オーバーレイを使用しない」という制限は、すべてのお客様が最新の機能と修正プログラムを利用できるように、シンプルで更新しやすく、常に最新のバージョンが実行されるクラウド ERP サービスをお客様に提供するための製品の展開において、重要な要素です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>After you upgrade code to 8.0 or later, when you compile, any customizations that still use over-layering will cause errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを 8.0 以降にアップグレードした後、コンパイルを行うと、オーバーレイを使用するカスタマイズが残っている場合、エラーが発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To refactor the code, the over-layering restriction can be temporarily relaxed in the model descriptor file of the model that is being over-layered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードのリファクタリングを行うには、オーバーレイされているモデルのモデル記述子ファイルで一時的にオーバーレイの制限を緩和できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>This temporary relaxation only works on development and demo environments and cannot be deployed on runtime environments like Standard Acceptance Test (or higher) sandbox or production environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この一時的な緩和は、開発環境およびデモ環境でのみ利用できます。スタンダード承認テスト以上のサンドボックス環境や実稼働環境などのランタイム環境には適用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Relaxing the descriptor restriction will enable the code to be gradually refactored to extensions, compiled, run, and then tested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記述子の制限を緩和することで、段階的にコードを拡張機能へとリファクタリングし、コンパイル、実行、テストを行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Detailed process</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細なプロセス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Complete the following steps to relax model restrictions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの制限を緩和するには、以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This procedure can be completed on a cloud environment or a local virtual machine (VM).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順は、クラウド環境で実行することも、ローカルの仮想マシン (VM) で実行することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Deploy a Dynamics 365 for Finance and Operations 8.0 development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Finance and Operations 8.0 開発環境を配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Run the Lifecycle Services (LCS) code upgrade service to upgrade the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Lifecycle Services (LCS) のコード アップグレード サービスを実行して、ソリューションをアップグレードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Temporarily allow over-layering in Microsoft models as needed to enable compilation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイルできるように、必要に応じて Microsoft のモデルでのオーバーレイを一時的に許可します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>a.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">a.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Locate the desired model within the C:\AOSService\PackagesLocalDirectory folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">C:\AOSService\PackagesLocalDirectory フォルダーで目的のモデルを見つけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>b.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">b.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Navigate to the descriptor folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記述子のフォルダーに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>For example, \Currency\Descriptor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、\Currency\Descriptor フォルダーなどです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>c.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">c.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open the XML file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML ファイルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For example, Currency.xml.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、Currency.xml ファイルなどです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>d.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">d.</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add a <bpt id="p1">**</bpt>Customization<ept id="p1">**</ept> metadata element inside the <bpt id="p2">**</bpt>AxModelInfo<ept id="p2">**</ept> metadata element to indicate <bpt id="p3">**</bpt>AllowAndWarn<ept id="p3">**</ept> so that the start of the file now looks like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Customization<ept id="p1">**</ept> メタデータ要素を <bpt id="p2">**</bpt>AxModelInfo<ept id="p2">**</ept> メタデータ要素の内側に追加して、<bpt id="p3">**</bpt>AllowAndWarn<ept id="p3">**</ept> を指定します。ファイルの冒頭はこのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Refactor over-layering to extensions and test.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイをリファクタリングして拡張機能にし、テストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Make use of extension capabilities to eliminate over-layering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">​オーバーレイを削除できるように、拡張機能を利用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>If needed, make extensibility requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合には、拡張機能の要求を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Revert the temporary changes to Microsoft models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft のモデルに対する一時的な変更を元に戻します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The deployment of a model that uses over-layering will not be possible, so it's important to ensure that the descriptor file is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイを使用するモデルの展開はできなくなるため、記述子ファイルを更新することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Prototyping extensibility requests</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の要求のプロトタイピング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>As a solution gradually migrates toward extensions, there will be places where an extensibility request is required to unblock the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用するようにソリューションを徐々に移行していく中で、ソリューションにおける課題を解消するために拡張機能の要求が必要になることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>To fully understand what is needed to unblock a solution and smooth the migration process toward extensions, extension capabilities can be prototyped in a separate model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの課題を解消し、拡張機能を使用するための移行プロセスをスムーズに進めるために何が必要なのかを十分に把握するために、拡張機能のプロトタイプを別のモデルとして作成することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Identify the need for an extension capability to refactor some over-layering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイをリファクタリングするために必要な拡張機能を特定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Add a prototype of extension capabilities into an extension prototype model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能のプロトタイプを拡張機能プロトタイプ モデルに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>For enumeration extensibility, put a copy of the enumeration into the extension prototype model and mark it as extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">列挙型の拡張については、対象の列挙型のコピーを拡張機能プロトタイプ モデルに追加して、拡張可能の設定を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>For extract method extensibility, prototype the extracted method and the overlayered original in the extension prototype model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">抽出メソッドの拡張については、抽出されたメソッドとオーバーレイされたオリジナルのプロトタイプを拡張機能プロトタイプ モデルに作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Use the prototype extension capability.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロトタイプの拡張機能を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>If the prototype extension capability is sufficient, create a matching request.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロトタイプの拡張機能で問題がなければ、対応する要求を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>When the extension capability has been implemented in the platform or application, the prototype extension capability and any associated over-layering should be removed from the extension prototype model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その拡張機能をプラットフォームやアプリケーションに実装する際には、プロトタイプの拡張機能および関連するオーバーレイはすべて、拡張機能プロトタイプ モデルから削除する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>After the solution has all over-layering refactored to extensions and the extension prototype model is empty, the solution refactoring is complete.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションのすべてのオーバーレイが拡張機能にリファクタリングされ、拡張機能プロトタイプ モデルが空になったら、ソリューションのリファクタリングは完了です。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>