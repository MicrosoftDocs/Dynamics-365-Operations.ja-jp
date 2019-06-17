<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="pos-api-extension.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>pos-api-extension.4ab022.3c59fcb1e2ec2593ff9b4a09f4c163f45e78f97c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>3c59fcb1e2ec2593ff9b4a09f4c163f45e78f97c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\pos-api-extension.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Call point of sale (POS) APIs or operations from POS extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) API または POS 拡張からの工程を呼び出す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>The Retail POS APIs help you to build extensions or add new features to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS API を使用すると、拡張機能を構築したり、POS に新しい機能を追加したりすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Call point of sale (POS) APIs or operations from POS extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売時点管理 (POS) API または POS 拡張からの工程を呼び出す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>The Retail POS APIs help you to build extensions or add new features to POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail POS API を使用すると、拡張機能を構築したり、POS に新しい機能を追加したりすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>For example, if you wanted to add new features that would retrieve product details, change a price, or add an item to a cart, you would call the POS APIs to do that work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、製品の詳細を取得し、価格を変更し、またはカートに品目を追加する新しい機能を追加する場合は、その作業を行うための POS API を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The POS APIs simplify the extension pattern and provide continuous support to build the extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API は、拡張子パターンを合理化し、拡張機能を構築するために継続的なサポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source> The extension patterns for Commerce Runtime (RT), POS, and Hardware Station now all use the request/response pattern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Runtime (RT)、POS、およびハードウェア ステーションの拡張パターンはすべて、要求/応答パターンを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This topic applies to Dynamics 365 for Finance and Operations and Dynamics 365 for Retail with Platform update 8 and Retail Application update 4 hotfix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは Dynamics 365 for Finance and Operations および Dynamics 365 for Retail プラットフォーム更新 8 と Retail アプリケーション更新プログラム 4 修正プログラムが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The POS APIs are categorized into three different scenarios.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS API は、3 つのさまざまなシナリオに分類されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source><bpt id="p1">**</bpt>Consume<ept id="p1">**</ept> - Consume the public APIs in your extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>消費<ept id="p1">**</ept> - 拡張機能のパブリック API を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Extend<ept id="p1">**</ept> - Extend the public APIs to do some additional logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張<ept id="p1">**</ept> - 一部の追加ロジックを実行するパブリック API を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Create<ept id="p1">**</ept> - Create new APIs using the POS interface, which can then be used across your extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> - POS インターフェイスを使用して新しい API を作成します。それは拡張機能全体で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Consume POS APIs in extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で POS API を使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Because the APIs are exposed using a request/response pattern, you can make an external web service call to implement your business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API は要求/応答パターンを使用して公開されるため、ビジネス ロジックを実装するための外部 Web サービス呼び出しを行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For example, is you wanted to change the price of an item, you would call <bpt id="p1">**</bpt>PriceOverrideOperationRequest<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえばが、品目の価格を変更する場合、<bpt id="p1">**</bpt>PriceOverrideOperationRequest<ept id="p1">**</ept> を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The APIs are subcategorized by modules such as CRT, peripherals, and store operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">API は、CRT、周辺機器、保存操作などのモジュールによりサブカテゴリ化されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Many new APIs have been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの新しい API が追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You can find a list of all the APIs in the file <bpt id="p1">**</bpt>…Retail SDK<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>Extensions<ph id="ph3">\\</ph>Pos.Api.d.ts<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての API のリストは <bpt id="p1">**</bpt>…Retail SDK<ph id="ph1">\\</ph>POS<ph id="ph2">\\</ph>Extensions<ph id="ph3">\\</ph>Pos.Api.d.ts<ept id="p1">**</ept> ファイルで探すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>How to consume an API in an extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で API を使用する方法</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To consume APIs in an extension, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能で  API を使用するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Open Visual Studio 2015 in administrator mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者モードで Visual Studio 2015 を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the <bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> solution from <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ModernPOS<ept id="p1">**</ept> ソリューションを <bpt id="p2">**</bpt>…<ph id="ph1">\\</ph>RetailSDK<ph id="ph2">\\</ph>POS<ept id="p2">**</ept> から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Under the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project create a new folder named <bpt id="p2">**</bpt>POSAPIExtension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> プロジェクトで、<bpt id="p2">**</bpt>POSAPIExtension<ept id="p2">**</ept> という名前の新しいフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Under <bpt id="p1">**</bpt>POSAPIExtension<ept id="p1">**</ept>, create a new folder named <bpt id="p2">**</bpt>TriggersHandlers<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POSAPIExtension<ept id="p1">**</ept> の下で <bpt id="p2">**</bpt>TriggersHandlers<ept id="p2">**</ept> という名前の新しいフォルダーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the <bpt id="p1">**</bpt>TriggersHandlers<ept id="p1">**</ept> folder, add a new Typescript file and name it <bpt id="p2">**</bpt>PreEndTransactionTrigger.ts<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TriggersHandlers<ept id="p1">**</ept> フォルダーに、新しい Typescript ファイルを追加し、<bpt id="p2">**</bpt>PreEndTransactionTrigger.ts<ept id="p2">**</ept> と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Add the following <bpt id="p1">**</bpt>import<ept id="p1">**</ept> statements to import the relevant entities and context.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の <bpt id="p1">**</bpt>import<ept id="p1">**</ept> 明細書を追加して、関連するエンティティおよびコンテキストをインポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Create a new class called <bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept> and extend it from <bpt id="p2">**</bpt>PreEndTransactionTrigger<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>PreEndTransactionTrigger<ept id="p1">**</ept> と呼ばれる新しいクラスを作成し、<bpt id="p2">**</bpt>PreEndTransactionTrigger<ept id="p2">**</ept> から拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Inside the class declare the following variables for the attributes names and sample values.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス内で、属性名と値の例に対して次の変数を宣言します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Implement the trigger <bpt id="p1">**</bpt>execute<ept id="p1">**</ept> method and call the existing POS APIs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>メソッドを実装し、既存の POS API を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The <bpt id="p1">**</bpt>execute<ept id="p1">**</ept> method calls APIs to get the current cart and customer, and then saves the attributes on the cart.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>execute<ept id="p1">**</ept> メソッドは、API を呼び出して現在の買い物カゴと顧客を取得し、買い物カゴに属性を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The overall code should look like the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">全体的なコードは次の例のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Create a new json file under the POSAPIExtension folder and name it manifest.json.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい json ファイルを POSAPIExtension フォルダーの下に作成し、manifest.json という名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In the manifest.json file, copy and paste the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">manifest.json ファイルに、次のコードをコピーして貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Delete the default generated code before copying this code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードをコピーする前に、既定で生成されたコードを削除してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Open the <bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept> file under the <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> project and update it with the <bpt id="p3">**</bpt>POSAPIExtension<ept id="p3">**</ept> samples, so that POS during runtime will include this extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>extensions.json<ept id="p1">**</ept> ファイルを <bpt id="p2">**</bpt>POS.Extensions<ept id="p2">**</ept> プロジェクトで開いて、<bpt id="p3">**</bpt>POSAPIExtension<ept id="p3">**</ept> サンプルで更新し、実行時に POS にこの拡張機能が含まれるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The extension.json file must contain at least two extensions folder names so don’t remove the <bpt id="p2">**</bpt>SampleExtensions<ept id="p2">**</ept> folder name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> extension.json ファイルには少なくとも 2 つの拡張子フォルダ名が含まれている必要があるため、<bpt id="p2">**</bpt>SampleExtensions<ept id="p2">**</ept> フォルダ名は削除しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Open <bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> and comment out the extension package folders from the exclude list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>tsconfig.json<ept id="p1">**</ept> を開き、拡張パッケージ フォルダーを除外リストからコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>POS will use this file to include or exclude the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS では、このファイルを使用して、拡張機能を追加または除外します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>By default, the list contains all the excluded extensions, if you want to include any extensions that are part of the POS, then you need add the extension folder name and comment out the extension from the extension list as shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、リストに除外されているすべての拡張子が含まれています。POS の一部である拡張子を含める場合は、拡張フォルダー名を追加し、示されている拡張リストから拡張子をコメント アウトする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept> Comment out both SampleExtensions2 and POSAPIExtension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> SampleExtensions2 と POSAPIExtension の両方をコメントアウトします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Select the <bpt id="p1">**</bpt>POS.Extensions<ept id="p1">**</ept> project and click <bpt id="p2">**</bpt>Show all Files<ept id="p2">**</ept> in Solution Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>POS 拡張機能<ept id="p1">**</ept> プロジェクトを選択し、ソリューション エクスプローラーで <bpt id="p2">**</bpt>ファイルをすべて表示<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Right-click and include the <bpt id="p1">**</bpt>SampleExtensions2<ept id="p1">**</ept> folder in the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、プロジェクトに <bpt id="p1">**</bpt>SampleExtensions2<ept id="p1">**</ept> フォルダーを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Test the extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張のテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Press F5 and deploy the POS to test your customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押し、POS を展開してカスタマイズをテストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Sign in to POS and add any item to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS にログインし、任意の品目をトランザクションに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Add any customer to a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トランザクションに顧客を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Click the <bpt id="p1">**</bpt>Pay<ept id="p1">**</ept> button and commit the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>支払<ept id="p1">**</ept>ボタンをクリックし、トランザクションをコミットします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>A dialog box should display asking if you want to save the attribute.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">属性を保存するかどうかをたずねるダイアログ ボックスが表示されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>