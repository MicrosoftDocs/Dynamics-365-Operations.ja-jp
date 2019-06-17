<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="extend-commerce-data-exchange.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>extend-commerce-data-exchange.b1c6f1.dbf138d5f60c5b72689460c4477f957b464d71f9.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>dbf138d5f60c5b72689460c4477f957b464d71f9</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\extend-commerce-data-exchange.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Extend Commerce Data Exchange - Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange の拡張 - リアルタイム サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can extend Commerce Data Exchange -  Real-time service by adding extension methods to the RetailTransactionServiceEx class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange - リアルタイム サービスを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Extend Commerce Data Exchange - Real-time Service</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange の拡張 - リアルタイム サービス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how you can extend Commerce Data Exchange (CDX) - Real-time service by adding extension methods to the RetailTransactionServiceEx class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、RetailTransactionServiceEx クラスに拡張メソッドを追加して、Commerce Data Exchange (CDX) - リアルタイム サービスを拡張する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Real-time Service enables retail clients to interact with retail functionality in real time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム サービスは、Retail クライアントがリアルタイムで小売機能を操作できるようします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>To extend Commerce Data Exchange - Real-time Service, you create a new method in the <bpt id="p1">**</bpt>RetailTransactionServiceEx<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce Data Exchange - リアルタイム サービスを拡張するには、<bpt id="p1">**</bpt>RetailTransactionServiceEx<ept id="p1">**</ept> クラスで新しいメソッドを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This method must meet the following criteria:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、次の基準を満たしている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The method must be a public static method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、パブリック静的メソッドでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The return value must be a container that has a length of 2 or more.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">戻り値は、長さが 2 以上のコンテナーである必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The first element must be a Boolean value that indicates whether the method call was successful, and a string value that you can use for a comment or error message.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の要素は、メソッド呼び出しが成功したかどうかを示すブール値と、コメントまたはエラー メッセージに使用できる文字列値でなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The other items in the container can be of any type, and they can even be nested containers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー内の他の項目は任意の型になることができ、入れ子になったコンテナーにもなれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The method parameters must be one of the following primitive types:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのパラメーターは、次のプリミティブ型のいずれかでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Boolean</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブール型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>date</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">日付</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>int</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">int</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>int64</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">int64</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>str</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">str</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>guid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">guid</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Real</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実績</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create and call a new extension method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい拡張メソッドの作成と呼び出し</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Start Microsoft Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Visual Studio を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Model management &gt; Create model<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>モデル管理 &gt; モデルの作成<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>In the <bpt id="p1">**</bpt>Create model<ept id="p1">**</ept> dialog box, enter the following details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの作成<ept id="p1">**</ept>ダイアログ ボックスに、次の詳細を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Model name<ept id="p1">**</ept> - Contoso</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル名<ept id="p1">**</ept> - Contoso</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Model publisher<ept id="p1">**</ept> - Contoso</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル発行元<ept id="p1">**</ept> - Contoso</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Layer<ept id="p1">**</ept> - USR (Select the relevant layer)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レイヤー<ept id="p1">**</ept> - USR (関連するレイヤーを選択)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Version<ept id="p1">**</ept> - 1.0.0.0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>バージョン<ept id="p1">**</ept> - 1.0.0.0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Model display name<ept id="p1">**</ept> - Contoso</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデルの表示名<ept id="p1">**</ept> - Contoso</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In the dialog box, select <bpt id="p1">**</bpt>Select existing package<ept id="p1">**</ept>, and then select <bpt id="p2">**</bpt>Application Suite<ept id="p2">**</ept> in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで、<bpt id="p1">**</bpt>既存のパッケージを選択<ept id="p1">**</ept>を選択してから、一覧で<bpt id="p2">**</bpt>アプリケーション スイート<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Click <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>完了<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>In the <bpt id="p1">**</bpt>New project<ept id="p1">**</ept> dialog box, enter <bpt id="p2">**</bpt>ContosoRetailTransactionServiceEx<ept id="p2">**</ept> as the project name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しいプロジェクト<ept id="p1">**</ept> ダイアログ ボックスに、<bpt id="p2">**</bpt>ContosoRetailTransactionServiceEx<ept id="p2">**</ept> というプロジェクト名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Right-click the project and select <bpt id="p1">**</bpt>Add &gt; New item<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトを右クリックし、<bpt id="p1">**</bpt>追加 &gt; 新しい項目<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the <bpt id="p1">**</bpt>Add New Item<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>Class<ept id="p2">**</ept> and enter the name of the class as <bpt id="p3">**</bpt>ContosoRetailTransactionServiceSample<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>新しい項目の追加<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>クラス<ept id="p2">**</ept> を選択し、<bpt id="p3">**</bpt>ContosoRetailTransactionServiceSample<ept id="p3">**</ept> としてクラスの名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>To consume the CDX method in Commerce runtime (CRT) you must add the ExtensionOf attribute to your class, such as ExtensionOf(classStr(RetailTransactionServiceEx).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) で CDX メソッドを使用するには、ExtensionOf(classStr(RetailTransactionServiceEx) など、ExtensionOf 属性をクラスに追加する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>This means that the class is extending from the RetailTransactionServiceEx.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、RetailTransactionServiceEx からクラスが拡張されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the code editor, add the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コード エディターで、次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Inside the class, add a new method to do your custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス内部で、カスタム ロジックを実行する新しいメソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>This is the method that you will call from CRT to do the custom logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、カスタム ロジックを実行するために CRT から呼び出すメソッドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In Solution Explorer, right-click the project, and then click <bpt id="p1">**</bpt>Build<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション エクスプローラーで、プロジェクトを右クリックしてから<bpt id="p1">**</bpt>ビルド<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>After you've finished building your new extension methods, the project will be deployed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい拡張メソッドを作成した後は、プロジェクトが展開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>Call the new method from the CRT</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CRT から新しいメソッドを呼び出す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In your commerce runtime (CRT), add a reference to the Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll, if it hasn't already been added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="1">Commerce Runtime</ph> (<ph id="2">CRT</ph>) で、Microsoft.Dynamics.Commerce.Runtime.TransactionService.dll への参照が追加されていない場合は追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Use the following sample code to call the new method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいメソッドを呼び出すには、次のサンプル コードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>In case of an exception in headquarters there is HeadquarterTransactionServiceException, which captures an exception and shows a user-friendly message in POS based on your scenario.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">本社で例外が発生した場合、HeadquarterTransactionServiceException が発生します。これは、例外をキャプチャし、シナリオに基づいて POS にわかりやすいメッセージを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>If you want to log the exception, use the RetailLogger.Log class object to log the events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">例外をログに記録する場合は、RetailLogger.Log クラス オブジェクトを使用してイベントを記録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>From the results object, you can read the response values from Real-time Service.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">results オブジェクトからは、リアルタイム サービスからの応答値を読み取ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The <bpt id="p1">**</bpt>InvokeExtensionMethod<ept id="p1">**</ept> method takes two parameters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>InvokeExtensionMethod<ept id="p1">**</ept> メソッドは 2 つのパラメーターを取ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>One parameter is the Real-time Service method name, and the other is the list of parameters that should be used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 つのパラメ ーターはリアルタイム サービス メソッド名であり、その他はパラメータの一覧を使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The method name that is passed should be the same as the method name that you created in the <bpt id="p1">**</bpt>ContosoRetailTransactionServiceSample<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">渡されるメソッド名は、<bpt id="p1">**</bpt>ContosoRetailTransactionServiceSample<ept id="p1">**</ept> クラスで作成したメソッド名と同じにする必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>