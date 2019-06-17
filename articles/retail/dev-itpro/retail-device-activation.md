<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-device-activation.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-device-activation.d89f05.c51d363be4e6da9d0a181cd528e54a55d8045a47.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c51d363be4e6da9d0a181cd528e54a55d8045a47</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-device-activation.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Retail point of sale (POS) device activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売販売時点管理 (POS) デバイスのライセンス認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains the new guided device activation for Retail Cloud POS and Retail Modern POS, and explains the client simplifications that help users easily activate devices without having to manually enter register and device ID information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Retail Cloud POS および Retail Modern POS の新しいガイド付きデバイスの有効化について説明し、ユーザーが手動で登録およびデバイスID情報を入力しなくても簡単にデバイスをアクティブ化できるクライアントの簡略化について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Retail point of sale (POS) device activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売販売時点管理 (POS) デバイスのライセンス認証</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains the new guided device activation for Retail Cloud POS and Retail Modern POS, and explains the client simplifications that help users easily activate devices without having to manually enter register and device ID information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事では、Retail Cloud POS および Retail Modern POS の新しいガイド付きデバイスの有効化について説明し、ユーザーが手動で登録およびデバイスID情報を入力しなくても簡単にデバイスをアクティブ化できるクライアントの簡略化について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Checklist to follow before activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">起動前のチェックリスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Complete the <bpt id="p1">**</bpt>Validate devices for activation<ept id="p1">**</ept> check in HQ, and make sure that the device passes validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HQ で<bpt id="p1">**</bpt>有効化のためにデバイスを検証<ept id="p1">**</ept>チェックを完了し、デバイスが検証をパスしたことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>On the client machine where you're activating the device, access the Retail Server URL health check, and make sure that the health check is passed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスを有効化しているクライアント マシンで、Retail サーバー URL 正常性チェックにアクセスし、正常性チェックが承認されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Use the following format: <ph id="ph1">https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の形式を使用します: <ph id="ph1">https://clxtestax404ret.cloud.test.dynamics.com/en/healthcheck?testname=ping</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>The worker must be mapped to a Microsoft Azure Active Directory (AAD) account (under <bpt id="p1">**</bpt>External identity<ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者は、Microsoft Azure Active Directory (AAD) アカウント (<bpt id="p1">**</bpt>外部 ID 下<ept id="p1">**</ept>) にマップする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The AAD account to map must belong to the same tenant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マッピングする AAD アカウントは、同じテナントに属している必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>To map the worker to the AAD account, sign in to HQ by using the Admin account for Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者を AAD アカウントにマップするには、Microsoft Dynamics Lifecycle Services (LCS) の管理者アカウントを使用して HQ に サインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Make sure that the worker is set up as a user in the Manager role (checked by validation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業者がマネージャー ロール内のユーザーとして設定されていることを確認します (検証でチェックされます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Make sure that the channel is published (checked by validation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネルが公開されていることを確認します (検証でチェックされます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Make sure that the channel database has the synced data from HQ, and that download jobs are running.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャネル データベースに本社から同期したデータが含まれており、ダウンロード ジョブが実行されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>To check this, run the following command in the channel database for the store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを確認するには、ストアのチャネル データベースで次のコマンドを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Make sure that data is returned, and that the result isn't empty.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データが返され、結果が空ではないことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Set up the hardware profile under <bpt id="p1">**</bpt>Register<ept id="p1">**</ept> (checked by validation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>登録<ept id="p1">**</ept> (検証によって確認) でハードウェア プロファイルを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Make sure that the register and store have a screen layout (checked by validation).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスターおよび店舗に画面レイアウトがあることを確認します (検証でチェックされます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Make sure that a primary address is set up for the legal entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本住所が法人に対して設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Make sure that the language is set up for the Commerce Data Exchange: Real-time Service user profile (JBB in the demo data).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">言語が Commerce Data Exchange: Real-time Service ユーザー プロファイル (デモ データでの JBB) に設定されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Make sure that the Real-time Service profile has the correct access.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルタイム サービス プロファイルに適切なアクセス許可があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Make sure that the electronic funds transfer (EFT) configuration value is present.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">電子決済 (EFT) のコンフィギュレーションの値があることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Activate a Modern POS or Cloud POS device by using guided activation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ガイド付きの有効化を使用して、Modern POS または Cloud POS デバイスを有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Open the initial device activation page for Modern POS or Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS またはクラウド POS 用の初期デバイスの有効化ページを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>You're prompted to sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインするように求められます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>On the <bpt id="p1">**</bpt>Before you start<ept id="p1">**</ept> page, follow the instructions, and then click <bpt id="p2">**</bpt>Next<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>始める前に<ept id="p1">**</ept>ページで、指示に従い、<bpt id="p2">**</bpt>次へ<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>p24</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">p24</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Start Cloud POS or Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Cloud POS または Modern POS を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Use your AAD credentials to sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AAD 資格情報を使用してサインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The AAD account must already be mapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AAD アカウントが既にマッピングされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>For instructions, see <bpt id="p1">[</bpt>Retail Modern POS self-service and device activation<ept id="p1">](../retail-modern-pos-device-activation.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順については、<bpt id="p1">[</bpt>Retail Modern POS セルフ サービスとデバイスのライセンス認証<ept id="p1">](../retail-modern-pos-device-activation.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>For Cloud POS, the server URL is automatically entered in the address bar.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS で、サーバー URL は、アドレス バーに自動的に入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>For Modern POS, you must copy and paste the server URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS で、サーバー URL をコピーし貼り付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>p18<ept id="p1">](./media/p18.png)](./media/p18.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>p18<ept id="p1">](./media/p18.png)](./media/p18.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Click <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to populate the list of stores.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗のリストを入力するには、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Select the correct store in the list.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一覧で適切な店舗を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>p20<ept id="p1">](./media/p20.png)](./media/p20.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>p20<ept id="p1">](./media/p20.png)](./media/p20.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Select the correct register and device.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なレジスターとデバイスを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> The device can be <bpt id="p2">**</bpt>Pending<ept id="p2">**</ept>, <bpt id="p3">**</bpt>De-activated<ept id="p3">**</ept>, or <bpt id="p4">**</bpt>Activated<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このデバイスは<bpt id="p2">**</bpt>保留中<ept id="p2">**</ept>、<bpt id="p3">**</bpt>非有効化<ept id="p3">**</ept>、または<bpt id="p4">**</bpt>有効化<ept id="p4">**</ept>とすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Alternatively, if you turned on the Retail HQ <bpt id="p1">**</bpt>Allow devices to be associated to registers from store<ept id="p1">**</ept> setting, you might see a list of registers that have no device associated with them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、Retail HQ <bpt id="p1">**</bpt>デバイスをストアからレジスターに関連付ける<ept id="p1">**</ept>設定を有効にする場合は、関連付けられているデバイスを持たないレジスターの一覧を表示する可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>p22<ept id="p1">](./media/p22.png)](./media/p22.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>p22<ept id="p1">](./media/p22.png)](./media/p22.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Click <bpt id="p1">**</bpt>Activate<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効化<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The device should be activated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバイスを有効化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>p23<ept id="p1">](./media/p23.png)](./media/p23.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>p23<ept id="p1">](./media/p23.png)](./media/p23.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Create a device ID from Modern POS and Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モダン POS とクラウド POS からデバイス ID を作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>We have added features to create a device (that is, automatically generate a device ID) from Modern POS or Cloud POS, so that the device can be associated with a register that doesn't yet have devices mapped to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS または Cloud POS からデバイスを作成する (すなわち、自動的にデバイス ID を生成する) 機能を追加しました。これにより、デバイスがまだマップされていないレジスターにデバイスを関連付けることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>This functionality can be used in Modern POS only if you set the HQ settings as follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、HQ の設定を次のように設定した場合にのみ Modern POS で使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Parameters<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail shared parameters<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>General<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>パラメータ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売共有パラメーター<ept id="p4">**</ept> <ph id="ph4">&amp;gt;</ph> <bpt id="p5">**</bpt>一般<ept id="p5">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Under <bpt id="p1">**</bpt>Devices,<ept id="p1">**</ept> set <bpt id="p2">**</bpt>Allow register association from device<ept id="p2">**</ept> to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept> で <bpt id="p2">**</bpt>デバイスからの登録を許可する<ept id="p2">**</ept> を <bpt id="p3">**</bpt>はい<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>In the Modern POS client, you can now add a device when you select a register that is listed as <bpt id="p1">**</bpt>No associated devices<ept id="p1">**</ept> in the guided activation flow.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS クライアントで、ガイド付きの有効化フローの<bpt id="p1">**</bpt>関連付けられているデバイスがありません<ept id="p1">**</ept>とリストされているレジスターを選択するときにデバイスを追加できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>After you select the register, you can either select a device that doesn't have register mapping or use the <bpt id="p1">**</bpt>Or, Add a Device<ept id="p1">**</ept> link.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レジスターを選択した後に、レジスター マッピングを持たないデバイスを選択するか、<bpt id="p1">**</bpt>またはデバイスを追加<ept id="p1">**</ept>リンクを使用するかのいずれかを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Click the <bpt id="p1">**</bpt>Or, Add a Device<ept id="p1">**</ept> link, and then either enter the new device ID or select <bpt id="p2">**</bpt>Automatically create a new device ID for me<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>またはデバイスを追加<ept id="p1">**</ept>リンクをクリックし、新しいデバイス ID を入力するか、または<bpt id="p2">**</bpt>新しいデバイス ID を自動的に作成する<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Click <bpt id="p1">**</bpt>Activate<ept id="p1">**</ept> to create a new device ID, associate it with the selected register, and complete the activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>有効化<ept id="p1">**</ept>をクリックして新しいデバイス ID を作成し、選択したレジスタへの関連付け、および有効化が完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Activate the device for Modern POS by using a configuration file</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルを使用して Modern POS のデバイスを有効化</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>IT Pros can now easily configure device activation for Modern POS by using a configuration file that can be downloaded together with Modern POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IT プロフェッショナルは、Modern POS と一緒にダウンロードできるコンフィギュレーション ファイルを使用して、Modern POS のデバイス アクティベーションを簡単に設定できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>This file is now available on the <bpt id="p1">**</bpt>Devices<ept id="p1">**</ept> page for the appropriate Modern POS device (<bpt id="p2">**</bpt>Retail<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel setup<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>POS setup<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>Devices<ept id="p5">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルは、適切な Modern POS デバイス (<bpt id="p2">**</bpt>Retail<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>チャネル設定<ept id="p3">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p4">**</bpt>POS 設定<ept id="p4">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p5">**</bpt>デバイス<ept id="p5">**</ept>) の<bpt id="p1">**</bpt>デバイス<ept id="p1">**</ept>ページで利用できます。   </target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configuration file download<ept id="p1">](./media/p16_11_16-1024x481.png)](./media/p16_11_16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>構成ファイルのダウンロード<ept id="p1">](./media/p16_11_16-1024x481.png)](./media/p16_11_16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>The configuration file is used to enter the Retail Server URL, device ID, and register number for device activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション ファイルは、Retail サーバー URL、デバイス ID、およびデバイスの有効化のためのレジスター番号を入力するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>During installation, the installer selects this file and populates the values for device activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストール時に、インストーラーはファイルを選択し、デバイスのライセンチ値を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source><bpt id="p1">**</bpt>Important:<ept id="p1">**</ept> The user must put the file in the same folder as the Modern POS self-service package and run the .exe file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>重要:<ept id="p1">**</ept> ユーザーは Modern POS セルフサービス パッケージと同じフォルダにファイルを置いて、.exe ファイルを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configuration file<ept id="p1">](./media/p17_11_16-1024x532.png)](./media/p17_11_16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>構成ファイル<ept id="p1">](./media/p17_11_16-1024x532.png)](./media/p17_11_16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Modern POS starts in Manual entry mode, and the Retail Server URL, device ID, and register ID are pre-populated for activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Modern POS は手動入力モードで起動し、Retail サーバー URL、デバイス ID、およびレジスター ID は、有効化のために事前設定されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Activate the device for Cloud POS by using syntactic sugar</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">糖衣構文を使用して Cloud POS のデバイスを有効化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>IT Pros can now configure device activation for Cloud POS by providing the device ID and register ID as the part of the Cloud POS URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IT プロフェッショナルは、Cloud POS URL の一部として、デバイス ID とレジスター ID を提供することで、Cloud POS のデバイス アクティベーションを設定できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>The link is available in the <bpt id="p1">**</bpt>Cloud POS URL<ept id="p1">**</ept> field on the <bpt id="p2">**</bpt>Devices<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>デバイス<ept id="p2">**</ept> ページの <bpt id="p1">**</bpt>クラウド POS URL<ept id="p1">**</ept> フィールドにリンクがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>(<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS setup<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Devices<ept id="p4">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>POS 設定<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>デバイス<ept id="p4">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Cloud POS URL field<ept id="p1">](./media/p15_11_16.png)](./media/p15_11_16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>クラウド POS URL フィールド<ept id="p1">](./media/p15_11_16.png)](./media/p15_11_16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Cloud POS starts in Manual entry mode, and the Retail Server URL, device ID, and register ID are pre-populated for activation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS は手動入力モードで起動し、Retail サーバー URL、デバイス ID、およびレジスター IDは、有効化のために事前設定されています。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>