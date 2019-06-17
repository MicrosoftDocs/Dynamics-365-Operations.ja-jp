<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="create-localizable-labels-client.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>create-localizable-labels-client.5d0f67.4bcd9580d5417780c409ef29d0214f8df9575764.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>4bcd9580d5417780c409ef29d0214f8df9575764</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\create-localizable-labels-client.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Create localizable labels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカライズ可能なラベルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains how to create localizable labels for client components and HTML/JavaScript controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Create localizable labels</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカライズ可能なラベルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains how to create localizable labels for client components and HTML/JavaScript controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、クライアント コンポーネントと HTML/JavaScript コントロールのローカライズ可能なラベルを作成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This article details the process for creating <bpt id="p1">**</bpt>localizable<ept id="p1">**</ept> labels for client components and HTML/JavaScript controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、クライアント コンポーネントと HTML/JavaScript コントロールの<bpt id="p1">**</bpt>ローカライズ可能な<ept id="p1">**</ept>ラベルを作成するプロセスについて詳しく説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This process uses the existing localization tools and process for labels to bring localization support to client components and HMTL/JavaScript controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロセスでは、既存のローカライズ ツールとラベル用のプロセスを使用して、クライアント コンポーネントと HMTL/JavaScript コントロールのローカライズ  サポートを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The following process relies on the label resource controller that can serialize label files into their JavaScript equivalents so that the labels can be used by the client components and HTML/JavaScript controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のプロセスでは、クライアント コンポーネントと HTML/JavaScript コントロールでラベルを使用できるように、ラベル ファイルを JavaScript に相当するものにシリアル化できるラベル リソース コントローラーが使用されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The label resource controller is deployed automatically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル リソース コントローラーは自動的に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>It is an MVC service that is located at the /Resources/Labels endpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">/Resources/Labels エンドポイントに配置されている MVC サービスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>1. Create a label file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1. ラベル ファイルの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Use the developer tools to create a new label file for your control's area, or use an existing label file for your control's area.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツールを使用して、コントロールの領域に新しいラベル ファイルを作成するか、コントロールの領域に既存のラベル ファイルを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>A control's area is determined by the owning team.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの領域は、チームによって決定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For extensible controls, your goal should be to create one label file for each HTM resource file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコントロールについては、目標として、HTM リソース ファイルごとに 1 つのラベル ファイルを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>If multiple HTM resources share the same set of labels, only one label file should be required for the set of HTM resource files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数の HTM リソースは、同じラベルのセットを共有している場合、1 つだけのラベル ファイルが HTM リソース ファイルのセットに対して必要となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For client controls and components, in general, controls that share a lot of the same functionality (for example, the Input controls: StringEdit, ComboBox, CheckBox, and so on) should also share the same label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント コントロールおよびコンポーネントでは、一般に、多くの同じ機能 (たとえば、入力コントロール: StringEdit、コンボボックス、チェックボックスなど) を共有するコントロールは、同じラベル ファイルも共有する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">*</bpt>Don't use a label file that also contains labels that are only used in X++.<ept id="p1">*</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>X ++ のみで使用されるラベルを含めて、ラベル ファイルは使用しないでください。<ept id="p1">*</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The whole label file is serialized when it’s loaded by the client, so be sure to keep the labels that aren't required by the client components/controls in a separate label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル ファイル全体がクライアントによってロードされると、シリアル化されるため、クライアント コンポーネント/コントロールで必要とされないラベルを別のラベル ファイルに保存してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>2. Add label strings to the label file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2. ラベル ファイルにラベル文字列を追加する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Use the developer tools to add label strings to the label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者ツールを使用して、ラベル文字列をラベル ファイルに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Example for extensible controls:<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張可能なコントロールの例:<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Label file name:<ept id="p1">**</ept> ClockControl</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ファイル名:<ept id="p1">**</ept> ClockControl</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Label ID:<ept id="p1">**</ept> Seconds</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル ID:<ept id="p1">**</ept> Seconds</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Label string:<ept id="p1">**</ept> seconds</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベル文字列:<ept id="p1">**</ept> seconds</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>3. Request the label file as a JavaScript file by using Resource manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3. リソース マネージャーを使用して、ラベル ファイルを JavaScript ファイルとして要求する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Use the script loading tag to load the JavaScript file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">タグ読み込みスクリプトを使用して、JavaScript ファイルを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The loading tag should reference the label file from /Resources/Labels, because the label resource controller is located there.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローディング タグは、ラベル リソース コントローラーがそこにあるため、/Resources/Labels のラベル ファイルを参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> For extensible controls, the controller automatically appends the label file name to the beginning of the label identifier in JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 拡張可能なコントロールの場合、コントローラーは自動的にラベル ファイル名を JavaScript のラベル ID の先頭に追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The JavaScript file that is returned will contain code that resembles the following example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返される JavaScript ファイルには、次の例のようなコードが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The culture information is injected automatically, based on the current user's culture.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カルチャ情報は、現在のユーザーのカルチャに基づいて自動的に挿入されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>No action is required on the part of the control to set, modify, or read the user's culture.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロールの部分でユーザーのカルチャの設定、変更、読み取りに必要なアクションはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The preceding code adds each of your label strings to the jQuery Globalize label storage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のコードは、jQuery Globalize ラベル記憶域に各ラベル文字列を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>You can then reference your labels throughout your HTML and JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML と JavaScript 全体でラベルを参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The JavaScript code in the script file is run the moment that the file is loaded by the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト ファイルにある JavaScript コードは、ブラウザーによってファイルが読み込まれた時点で実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Therefore, your labels are immediately ready for use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、ラベルはすぐに使用できる状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Be sure to add the label script loading tag <bpt id="p1">**</bpt>after<ept id="p1">**</ept> any other script loading tags in your HTML.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML に他のスクリプト読み込みタグの<bpt id="p1">**</bpt>後<ept id="p1">**</ept>、ラベルスクリプトの読み込みタグを必ず追加してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>The script loading tags are processed in order, from top to bottom.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スクリプト読み込みタグは、上から順に処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>By loading the label script last, you help guarantee that no other scripts cause conflicts or override the labels that are set in the script label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後にラベル スクリプトを読み込むことによって、他のスクリプトが競合を起こさないようにするか、スクリプト ラベル ファイルに設定されているラベルを上書きすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>4. Use localizable labels in HTML and JavaScript</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4. HTML と JavaScript でローカライズ可能なラベルを使用する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The following framework application programming interface (API) can be used in HTML (inside <bpt id="p1">**</bpt>data-dyn-bind<ept id="p1">**</ept>) or in JavaScript to access the labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のフレームワーク アプリケーション プログラミング インターフェイス (API) は、HTML (内部 <bpt id="p1">**</bpt>data-dyn-bind<ept id="p1">**</ept>) または JavaScript でラベルにアクセスするために使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source><bpt id="p1">**</bpt>HTML<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HTML<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>JavaScript<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>JavaScript<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>You can also pass the label ID via a variable in HTML or JavaScript.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTML または JavaScript の変数を介してラベル ID を渡すこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>HTML<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>HTML<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>JavaScript<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>JavaScript<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The <bpt id="p1">**</bpt>$dyn.label<ept id="p1">**</ept> API will find the appropriately named label and return the string that can be used to display text to the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>$dyn.label<ept id="p1">**</ept> API は、適切な名前のラベルを検索し、ユーザーにテキストを表示するために使用する文字列を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>This API will automatically select the label, based on the current user's culture.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この API は、現在のユーザーのカルチャに基づいてラベルを自動的に選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Troubleshooting</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you have correctly created a label file, and the label has been deployed, you should be able to load the JavaScript version of the label file directly from the browser.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル ファイルが正しく作成され、そのラベルが展開されている場合は、ブラウザから直接、ラベルファイルの JavaScript バージョンを読み込むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>You can access the JavaScript label file by navigating to the home page in the client and appending the following path to the URL: <bpt id="p1">**</bpt>/Resources/Labels/MyLabelFile.js<ept id="p1">**</ept>, where <bpt id="p2">**</bpt>MyLabelFile<ept id="p2">**</ept> is the name of the label file without the language suffix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JavaScript のラベル ファイルには、クライアントのホーム ページに移動して、URL にパス <bpt id="p1">**</bpt>/Resources/Labels/MyLabelFile.js<ept id="p1">**</ept> を加えてアクセスすることができます。ここで <bpt id="p2">**</bpt>MyLabelFile<ept id="p2">**</ept> は言語の接尾語なしのラベル ファイル名です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>For a deployed label file that is named MyLabelFile.en-us, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MyLabelFile.en-us という名前の配置されたラベル ファイルのについては、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Navigate to the home page, and sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ホーム ページに移動して、サインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>(On one-box deployments, the URL of the home page is <ph id="ph1">&lt;https://usncax1aos.cloud.onebox.dynamics.com/en/&gt;</ph>.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ワン ボックス配置では、ホーム ページの URL は<ph id="ph1">&lt;https://usncax1aos.cloud.onebox.dynamics.com/en/&gt;</ph> です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Make sure that the desired language has been set by going to <bpt id="p1">**</bpt>Options<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Language and Region<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">目的の言語が<bpt id="p1">**</bpt>オプション<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>言語および地域<ept id="p2">**</ept>で設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>(You don't have to change the language if it's already set to the language that you want.) Now that the user's language has been set in the current session, the label resource controller will know what language to use when the label file is loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(目的の言語に設定されている場合は言語を変更する必要はありません。) ユーザーの言語が現在のセッションで設定されたので、ラベル リソース コントローラーは、ラベル ファイルが読み込まれるときに使用する言語を認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>To load the JavaScript version of the label file, navigate to the label file by adding <bpt id="p1">&lt;strong&gt;</bpt>Resources/Labels/MyLabelFile.js<ept id="p1">&lt;/strong&gt;</ept> to the URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">JavaScript バージョンのラベル ファイルを読み込むには、<bpt id="p1">&lt;strong&gt;</bpt>Resources/Labels/MyLabelFile.js<ept id="p1">&lt;/strong&gt;</ept> を URL に追加してラベル ファイルに移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>(On one-box deployments, the whole URL is <ph id="ph1">&lt;https://usncax1aos.cloud.onebox.dynamics.com/en/Resources/Labels/MyLabelFile.js&gt;</ph>.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(ワン ボックス配置では、全体の URL は<ph id="ph1">&lt;https://usncax1aos.cloud.onebox.dynamics.com/en/Resources/Labels/MyLabelFile.js&gt;</ph> です。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>The corresponding label file will be JSON-serialized, and the browser will either show the text on the current tab or prompt you to download the .js file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対応するラベル ファイルは JSON シリアル化され、ブラウザーは現在のタブにテキストを表示するか、.js ファイルのダウンロードを促すメッセージを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>If you download the file, you can then open it locally to inspect it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルをダウンロードする場合、ローカルでそれを開き、検査できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If the browser doesn't find the file, you might have mistyped the name of the label, or you might not have deployed the label correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーにファイルが見つからない場合は、ラベルの名前を誤って入力した、またはラベルを正しく展開しなかった可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>There is never a physical .js file for the label in the web folder /Resources/Labels.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web フォルダー/リソース/ラベルのラベルに物理的な .js ファイルはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>The .js file is dynamically generated by the label resource controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.js ファイルは、ラベル リソース コントローラーによって動的に生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Microsoft Visual Studio form previewer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studioフォーム プレビューアー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>The form previewer isn't currently configured to load labels via the label resource controller.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム プレビューアーは、ラベル リソース コントローラー経由でラベルを読み込むようには現在設定されていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The form previewer will load only labels that are defined directly in the .js file for the code behind (located at /Resources/Scripts).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム プレビューアーは、コード ビハインド (/Resources/Scripts にあります) の .js ファイルに直接定義されているラベルのみを読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Until the form previewer is updated so that it can load .js files from the label resource controller, make sure that you also define the labels in the .js file for the code behind of the control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム プレビューアを更新して、ラベル リソース コントローラから .js ファイルをロードできるようになるまでは、コントロールのコード ビハインドの .js ファイルにもラベルを定義するようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The dependency on these labels will be removed in a future update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのラベルへの依存関係は、将来の更新で削除されます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>