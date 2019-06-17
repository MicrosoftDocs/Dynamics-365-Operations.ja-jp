<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="trigger-example-return-policy.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>trigger-example-return-policy.8371ba.2d32ee27ca157dcaaf12abbff297a6f84e8a8dbd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>2d32ee27ca157dcaaf12abbff297a6f84e8a8dbd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\trigger-example-return-policy.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Implement a return policy by using triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを使用して返品ポリシーを実装してください</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic has two examples which show how you can implement a new policy using a trigger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トリガーを使用して新しいポリシーを実装する方法の例を 2 つ示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Implement a return policy by using triggers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガーを使用して返品ポリシーを実装してください</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic is applicable for Dynamics 365 for Finance and Operations version 7.1 and earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Dynamics 365 for Finance and Operations バージョン 7.1 およびそれ以前のバージョンに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This implementation is not supported for versions 7.2 and higher.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バージョン 7.2 およびそれ以上の場合は、この実装はサポートされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For those versions, follow the extension model without overlayering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのバージョンでは、オーバーレイせずに拡張モデルに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This topic has two examples that show how you can implement a new policy using a trigger.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、トリガーを使用して新しいポリシーを実装する方法の例を 2 つ示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The examples in this topic assume that you have a new return policy.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの例では、新しい返品ポリシーがあることを前提としています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The maximum time period for returning an item is 30 days and no item may be returned more than 30 days after the date of purchase.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">返品の最長期間は 30 日間で、購入日から 30 日を超えて返品することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Additionally, the cashier or manager is not allowed to void more than three items in a single transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、レジ担当者またはマネージャーは、1 回のトランザクションで 3 つ以上の品目を無効にすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Extend the MPOS trigger</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS トリガーを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Open Visual Studio as an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio を管理者としてオープンします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Open the Modern POS solution from K:<ph id="ph1">\\</ph>RainMainStab<ph id="ph2">\\</ph>7.0.1265.3014<ph id="ph3">\\</ph>retail<ph id="ph4">\\</ph>Services<ph id="ph5">\\</ph>RetailSDK<ph id="ph6">\\</ph>Code<ph id="ph7">\\</ph>POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS ソリューションを K:<ph id="ph1">\\</ph>RainMainStab<ph id="ph2">\\</ph>7.0.1265.3014<ph id="ph3">\\</ph>小売<ph id="ph4">\\</ph>サービス<ph id="ph5">\\</ph>RetailSDK<ph id="ph6">\\</ph>コード<ph id="ph7">\\</ph>POS から開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Add new a TypeScript file in the POS.Core project, under the <bpt id="p1">**</bpt>Triggers<ept id="p1">**</ept> folder, and name it ExtensionTrigger.ts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>トリガー<ept id="p1">**</ept> フォルダーの下の POS.Core プロジェクトに新しい TypeScript ファイルを追加し、ExtensionTrigger.ts という名前をつけます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Add reference to the triggers interface and create a new module for the code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">トリガー インターフェイスへの参照を追加し、コードの新しいモジュールを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the ExtensionTrigger.ts file, add the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ExtensionTrigger.ts ファイルに次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Scenario 1: 30day return policy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ 1: 30 日返品ポリシー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>To implement the 30-day return policy, extend the IPreConfrimReturnTransactionTrigger by creating a new class and implementing the IPreConfirmReturnTransactionTrigger interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">30日間の返品ポリシーを実装するには、新しいクラスを作成し、IPreConfirmReturnTransactionTrigger インターフェイスを実装して、IPreConfrimReturnTransactionTrigger を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>This trigger will be invoked before returning any item from the transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトリガーは、トランザクションから項目を返す前に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Create a new class that implements IPreConfirmReturnTransactionTrigger in the module Commerce.Triggers.Samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール Commerce.Triggers.Samples で IPreConfirmReturnTransactionTrigger を実装する新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Name it PreConfirmReturnTransactionTrigger, as shown in the following code example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードの例に示すように、PreConfirmReturnTransactionTrigger と名前を付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Implement the <bpt id="p1">**</bpt>execute<ept id="p1">**</ept> method from the interface and add code to validate the return condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスから<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>メソッドを実装して、返品条件を検証するコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Scenario 2: Limit of three returns per transaction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ 2: トランザクションごとに返品 3 回の制限</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>To implement the three-time limit, create a new class and implement the IPreVoidProductsTrigger interface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 回限りの制限を実装するには、新しいクラスを作成し、IPreVoidProductsTrigger インターフェイスを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>This trigger will be invoked before voiding any item in a transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトリガーは、トランザクション内の項目を無効にする前に呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Create a new class named PreVoidProductsTrigger that implements the IPreVoidProductsTrigger interface in the module Commerce.Triggers.Samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モジュール Commerce.Triggers.Samples で IPreVoidProductsTrigger インターフェイスを実装する PreVoidProductsTrigger という名前の新しいクラスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Make sure this code is outside of the PreConfirmReturnTransactionTrigger class that you created in the previous step.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、前の手順で作成した PreConfirmReturnTransactionTrigger クラスの外にあることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Implement the <bpt id="p1">**</bpt>execute<ept id="p1">**</ept> method from the interface and add the code to validate the void condition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インターフェイスから<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>メソッドを実装して、無効条件を検証するコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Register the two triggers after the MPOS logon.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS ログオン後に 2 つのトリガーを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Copy the following code to the same file after the two classes that you created in the previous steps but within the same module Commerce.Triggers.Samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記の手順で作成した 2 つのクラスの後、同じモジュールの Commerce.Triggers.Samples 内にある同じファイルに、次のコードをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Register the PostLogon trigger during the DOMCOntentLoaded event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DOMCOntentLoaded イベント中に PostLogon トリガーを登録します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Copy the following code outside of all the classes but within the module Commerce.Triggers.Samples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Commerce.Triggers.Samples モジュール内のすべてのクラスの外に、次のコードをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Build the project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトの構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Compile and rebuild the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトをコンパイル、およびリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Deploy the MPOS in Local Machine by clicking the <bpt id="p1">**</bpt>Deploy<ept id="p1">**</ept> button in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で<bpt id="p1">**</bpt>配置ボタン<ept id="p1">**</ept>をクリックして、ローカル コンピューターに MPOS を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>If you get an error which states that “The project POS.App needs to be deployed before it can be started.”, then follow the steps below to resolve the error and try again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">"プロジェクトの POS.App を開始できる前に展開する必要があります" というエラー メッセージが表示された場合、下記の手順に従い、エラーを解決し、再試行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Right-click the ModernPOS solution in Visual Studio and click <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で ModernPOS ソリューションを右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In the <bpt id="p1">**</bpt>Property<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>Configuration<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、<bpt id="p2">**</bpt>コンフィギュレーション<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Select the <bpt id="p1">**</bpt>Deploy<ept id="p1">**</ept> check box for the Pos.App project and click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Pos.App プロジェクトの <bpt id="p1">**</bpt>展開<ept id="p1">**</ept> チェック ボックスを選択し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Validate the customization</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズの検証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Log in to MPOS using 000160 as the operator ID and 123 as the password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オペレーター ID に 000160、パスワードに 123 を使用して MPOS にログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Complete a sales transaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">販売トランザクションを比較します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Click <bpt id="p1">**</bpt>Show Journal<ept id="p1">**</ept> and try to return the merchandise.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>仕訳帳の表示<ept id="p1">**</ept>をクリックし、商品を返送してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You will get the error message “Cannot return, you are past return date”.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「返却できません。返却日を過ぎています」というエラー メッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Create another new transaction and add four different items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">別の新しいトランザクションを作成し、4 つの異なるアイテムを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Try to return all four items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 つのアイテムすべてを返すようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>You will get an error for the fourth item with the message, "Void is not allowed anymore.”</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4番目の項目に関してエラーが発生し、「無効はこれ以上許されません」 というメッセージが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>In the sample code, the return the time period is configured as 100 ms, so that you can test your code immediately.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプルコードでは、期間を 100 ミリ秒として返すので、すぐにコードをテストすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>You should change the configuration as needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、コンフィギュレーションを変更する必要があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>