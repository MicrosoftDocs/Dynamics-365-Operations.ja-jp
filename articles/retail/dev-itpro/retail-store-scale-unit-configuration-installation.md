<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="retail-store-scale-unit-configuration-installation.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>retail-store-scale-unit-configuration-installation.2a1b8c.639b7c4af0614ee5f0a292c8823390edbd4eea9d.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>639b7c4af0614ee5f0a292c8823390edbd4eea9d</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\dev-itpro\retail-store-scale-unit-configuration-installation.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Configure and install Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のコンフィギュレーションとインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how you can use self-service to configure Retail Store Scale Unit in Retail headquarters, download it, and install it on one or more computers in a brick-and-mortar store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、セルフ サービスを使用して、小売用バックオフィスで Retail Store Scale Unit を構成し、ダウンロードして、実店舗の 1 台以上のコンピューターにインストールする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Configure and install Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のコンフィギュレーションとインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how you can use self-service to configure Retail Store Scale Unit in Microsoft Dynamics 365 for Retail headquarters, download it, and install it on one or more computers in a brick-and-mortar store.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、セルフ サービスを使用して、Microsoft Dynamics 365 for Retail バックオフィスで Retail Store Scale Unit を構成し、ダウンロードして、実店舗の 1 台以上のコンピューターにインストールする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Retail Store Scale Unit combines the Retail channel database, Retail Async Client, Retail Server, and Retail Cloud point of sale (POS) components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit は、Retail チャネル データベース、Retail Async Client、Retail Server、Retail Cloud 販売時点管理 (POS) コンポーネントを組み合わせます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>A Microsoft Dynamics 365 for Retail environment already provides these components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Retail 環境では、これらのコンポーネントが既に提供されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>However, you can now configure them so that they work locally in a store, in either a single-computer setup (the default option) or a multiple-computer setup.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、単一コンピューターのセットアップ (既定のオプション) または複数コンピューターのセットアップのいずれかで、ストア内でローカルに動作するように構成できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>This topic also explains how to uninstall and troubleshoot Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックは、Retail Store Scale Unit のアンインストールとトラブルシューティングの方法についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Before you begin</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">準備</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>To help maintain a high level of security across the company, we strongly recommend that you create a new application ID (client ID) and key (secret) for each retail store that is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">会社全体で高いレベルのセキュリティを維持するために、作成する小売店舗ごとに新しいアプリケーション ID (クライアント ID) とキー (シークレット) を作成することを強くお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>This step requires a new Web app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップでは、新しい Web アプリが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Generate a Microsoft Azure Active Directory (Azure AD) app registration to create an application ID (client ID) and key (secret).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ID (クライアント ID) とキー (シークレット) を作成する Microsoft Azure Active Directory (Azure AD) アプリ登録を生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>For instructions, see <bpt id="p1">[</bpt>Create an Azure Active Directory application<ept id="p1">](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手順については、<bpt id="p1">[</bpt>Azure Active Directory アプリケーションを作成する<ept id="p1">](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This topic reviews Azure user permissions and requirements, and explains how to generate an app registration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Azure ユーザーのアクセス許可と要件を確認し、アプリ登録を生成する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>If you are installing Retail Store Scale Unit for use with an on-premises environment using Active Directory Federation Services, instead of Azure, follow the instructions in the Retail installation document for on-premises environments.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure ではなく Active Directory フェデレーション サービスを使用する設置環境で使用する Retail Store Scale Unit をインストールする場合は、設置環境の Retail インストール ドキュメントの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>For more information, see <bpt id="p1">[</bpt>Installation steps for Retail channel components in an on-premises environment<ept id="p1">](../../dev-itpro/deployment/deploy-retail-onprem.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>オンプレミス環境での小売チャネルのコンポーネントのインストール手順<ept id="p1">](../../dev-itpro/deployment/deploy-retail-onprem.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>After an application ID (client ID) and key are created for Retail Store Scale Unit, the client ID must be accepted in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のアプリケーション ID (クライアント ID) とキーが作成された後、クライアント ID を、小売で受け入れる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory applications<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory アプリケーション<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Enter the application ID (client ID) in the <bpt id="p1">**</bpt>Client ID<ept id="p1">**</ept> column, enter descriptive text in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> column, and enter <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> in the <bpt id="p4">**</bpt>User ID<ept id="p4">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ID (クライアントID) を<bpt id="p1">**</bpt>クライアント ID<ept id="p1">**</ept> 列に入力し、説明のテキストを<bpt id="p2">**</bpt>名<ept id="p2">**</ept>列に入力および <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> を<bpt id="p4">**</bpt>ユーザー ID<ept id="p4">**</ept> 列に入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Configure a new Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい Retail Store Scale Unit のコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>To create a functioning Retail Store Scale Unit, complete the procedures in all sections of this topic through the "Run the Retail Store Scale Unit installer" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">機能する Retail Store Scale Unit を作成するには、「Retail Store Scale Unit インストーラーの実行」の手順に従ってこのトピックのすべてのセクションの手順を実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>To complete the configuration and installation, you must first do the initial configuration in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">構成とインストールを完了するには、まず小売用バックオフィスで初期構成を行う必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Next, you must complete the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、インストールを完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Finally, you must return to Retail headquarters to finish the configuration, so that Retail Store Scale Unit works correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、Retail Store Scale Unit が正しく動作するよう、コンフィギュレーションを完了する小売用バック オフィスを返す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>For on-premises deployments, perform the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">設置配置では、次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Channel database group<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>チャンネル データベース グループ<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>On the Action pane, select <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>新規<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>Default<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept> フィールドに、<bpt id="p2">**</bpt>既定<ept id="p2">**</ept>と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Enter a description in the <bpt id="p1">**</bpt>Description<ept id="p1">**</ept> field, if needed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要に応じて、<bpt id="p1">**</bpt>説明<ept id="p1">**</ept> フィールドに説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In the <bpt id="p1">**</bpt>Retail channel schema<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>AX7<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Retail チャネル スキーマ<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>AX7<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>In the <bpt id="p1">**</bpt>Working folders<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>File storage<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作業フォルダー<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>ファイル ストレージ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>In Retail headquarters, go to  <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Channel database<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、<bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>チャネル データベース<ept id="p4">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>On the <bpt id="p1">**</bpt>Channel database<ept id="p1">**</ept> page, on the Action Pane, select <bpt id="p2">**</bpt>New<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル データベース<ept id="p1">**</ept>ページの、アクション ウィンドウで、<bpt id="p2">**</bpt>新規<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In the <bpt id="p1">**</bpt>Channel database ID<ept id="p1">**</ept> field, enter a unique value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャネル データベース ID<ept id="p1">**</ept> フィールドに、固有の値を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>In the <bpt id="p1">**</bpt>Channel data group<ept id="p1">**</ept> field, select the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>チャンル データ グループ<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>既定<ept id="p2">**</ept>オプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Select any option that has been created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成されている任意のオプションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>For on-premises deployments, this value will be the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> value that was previously described in this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置では、この値が前にこのトピックで説明した<bpt id="p1">**</bpt>既定<ept id="p1">**</ept>値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> field, leave the default value (<bpt id="p2">**</bpt>Channel database<ept id="p2">**</ept>) selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイプ<ept id="p1">**</ept> フィールドで、既定値 (<bpt id="p2">**</bpt>チャネル データベース<ept id="p2">**</ept>) を選択したままにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>You can leave the <bpt id="p1">**</bpt>Data sync interval<ept id="p1">**</ept> field blank.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ同期間隔<ept id="p1">**</ept> フィールドは空白のままにすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Alternatively, you can select a value in this field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">あるいは、このフィールドで値を選択することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>For example, in the demo data, the value <bpt id="p1">**</bpt>D60-U15<ept id="p1">**</ept> specifies a 15-minute synchronization interval.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デモ データでは、<bpt id="p1">**</bpt>D60-U15<ept id="p1">**</ept> の値が 15 分の同期間隔を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The <bpt id="p1">**</bpt>Data sync interval<ept id="p1">**</ept> value determines how often the data is synchronized between the channel database (Retail Store Scale Unit) and retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データの同期間隔<ept id="p1">**</ept> 値は、チャネル データベース (Retail Store Scale Unit) および小売用バックオフィス間でデータを同期する頻度を決定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>If no value is entered, the default interval that is set up in Retail Store Scale Unit is used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">値が入力されていない場合は、Retail Store Scale Unit で設定されている既定の間隔が使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>This default interval is three minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この既定の間隔は、3 分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>On the <bpt id="p1">**</bpt>Retail channel<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and then, in the <bpt id="p3">**</bpt>Channel<ept id="p3">**</ept> field, select the appropriate Retail store channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売チャネル<ept id="p1">**</ept>のクイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択し、<bpt id="p3">**</bpt>チャネル フィールド<ept id="p3">**</ept>で、適切な小売店舗のチャンネルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Repeat this step to add all the channels that should use this database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースを使用するすべてのチャンネルを追加するには、この手順を繰り返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>You can also add channels that don't use this database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、このデータベースを使用しないチャンネルを追加することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>In this way, you keep the data for those channels in the Retail Store Scale Unit channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、Retail Store Scale Unit のチャネル データベースのチャネルのデータを保持します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The Retail store channels that actively use this database can then access that data locally.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータベースを頻繁に使用する Retail 店舗チャネルは、ローカルでそのデータにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>For on-premises deployments, select the <bpt id="p1">**</bpt>Download<ept id="p1">**</ept> button on the Action pane and select <bpt id="p2">**</bpt>Retail Store Scale Unit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置では、アクション ウィンドウの <bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept> ボタンを選択し、<bpt id="p2">**</bpt>Retail Store Scale Unit<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>This will cause a known error and initiate the upload logic so that the following step in this document can be correctly completed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、既知のエラーが発生し、このドキュメントの次の手順を正しく完了できるように、アップロード ロジックが開始されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Allow for one minute while the upload logic completes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アップロード ロジックが完了するまで 1 分待ってください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>On the <bpt id="p1">**</bpt>Store Scale Unit package<ept id="p1">**</ept> FastTab, in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> field, select the appropriate Retail Store Scale Unit package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>店舗スケール ユニット パッケージ<ept id="p1">**</ept>クイック タブの、<bpt id="p2">**</bpt>名前<ept id="p2">**</ept>フィールドで、適切な Retail Store Scale Unit パッケージを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Each environment generates a base Retail Store Scale Unit package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各環境では、基本な Retail Store Scale Unit パッケージを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Therefore, this field always contains at least one option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このフィールドには常に少なくとも 1 つのオプションが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel profiles<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャンネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>チャンネル プロファイル<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>New<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>新規<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> field, enter a unique name for the channel profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>フィールドに、チャネル プロセスの一意な名前を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>For on-premises deployments, use the value <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> in this field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置では、このフィールドで<bpt id="p1">**</bpt>既定<ept id="p1">**</ept>値を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>On the <bpt id="p1">**</bpt>Profile properties<ept id="p1">**</ept> FastTab for the new channel profile, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャネル プロファイルの<bpt id="p1">**</bpt>プロファイルのプロパティ<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In the <bpt id="p1">**</bpt>Property key<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Retail server URL<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ キー<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>Retail サーバー URL<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>In the <bpt id="p1">**</bpt>Property value<ept id="p1">**</ept> field, enter the URL of the Retail Server that should be installed for Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ値<ept id="p1">**</ept>フィールドに、Retail Store Scale Unit にインストールする必要のある Retail サーバーの URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The standard format for the URL of Retail Server is <bpt id="p1">**</bpt>https://<ph id="ph1">&amp;lt;</ph>Computer Name<ph id="ph2">&amp;gt;</ph>:<ph id="ph3">&amp;lt;</ph>Port<ph id="ph4">&amp;gt;</ph>/RetailServer/Commerce<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーの URL の標準形式は、<bpt id="p1">**</bpt>https://<ph id="ph1">&amp;lt;</ph>コンピューター名<ph id="ph2">&amp;gt;</ph>:<ph id="ph3">&amp;lt;</ph>ポート<ph id="ph4">&amp;gt;</ph>/RetailServer/Commerce<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In this format, <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Computer Name<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> is either the fully qualified domain name (FQDN) of the computer where Retail Store Scale Unit is installed or, for systems that aren't joined to a domain, the full computer name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この形式で、<bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>コンピューター名<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> は Retail Store Scale Unit がインストールされているコンピューター、またはドメイン、フル コンピューター名に結合されていないシステムの完全修飾ドメイン名 (FQDN) のどちらかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Port<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> is the port number that should be used in the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>ポート<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept>はインストールに使用するポート番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The port number must be a value between 1 and 65535.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポート番号は、 1 ～ 65535 の範囲の値である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>If you're using the default HTTPS port (443), you don't have to specify the port number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の HTTPS ポート (443) を使用している場合、ポート番号を指定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>On the <bpt id="p1">**</bpt>Profile properties<ept id="p1">**</ept> FastTab for the new channel profile, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャネル プロファイルの<bpt id="p1">**</bpt>プロファイルのプロパティ<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In the <bpt id="p1">**</bpt>Property key<ept id="p1">**</ept> field, select <bpt id="p2">**</bpt>Cloud POS URL<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ キー<ept id="p1">**</ept> フィールドで、<bpt id="p2">**</bpt>クラウド POS URL<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In the <bpt id="p1">**</bpt>Property value<ept id="p1">**</ept> field, enter the URL of the Retail Cloud POS instance that should be installed for Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ値<ept id="p1">**</ept>フィールドに、Retail Store Scale Unit にインストールする必要のある Retail Cloud POS インスタンスの URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The standard format for the URL of Cloud POS is <bpt id="p1">**</bpt>https://<ph id="ph1">&amp;lt;</ph>Computer Name<ph id="ph2">&amp;gt;</ph>:<ph id="ph3">&amp;lt;</ph>Port<ph id="ph4">&amp;gt;</ph>/POS<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラウド POS の URL の標準形式は、<bpt id="p1">**</bpt>https://<ph id="ph1">&amp;lt;</ph>コンピューター名<ph id="ph2">&amp;gt;</ph>:<ph id="ph3">&amp;lt;</ph>ポート<ph id="ph4">&amp;gt;</ph>/POS<ept id="p1">**</ept> です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>In this format, <bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Computer Name<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> is either the FQDN of the computer where Retail Store Scale Unit is installed or, for systems that aren't joined to a domain, the full computer name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この形式で、<bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>コンピューター名<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> は Retail Store Scale Unit がインストールされているコンピューター、またはドメイン、フル コンピューター名に結合されていないシステムの FQDN のどちらかです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>Port<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept> is the port number that should be used in the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt><ph id="ph1">&amp;lt;</ph>ポート<ph id="ph2">&amp;gt;</ph><ept id="p1">**</ept>はインストールに使用するポート番号です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>The port number must be a value between 1 and 65535.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ポート番号は、 1 ～ 65535 の範囲の値である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If you're using the default HTTPS port (443), you don't have to specify the port number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定の HTTPS ポート (443) を使用している場合、ポート番号を指定する必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>If media is commonly used, it will be necessary to generate a <bpt id="p1">**</bpt>Media Server Base URL<ept id="p1">**</ept> for the profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メディアがよく使用される場合、プロファイルの <bpt id="p1">**</bpt>メディア サーバー ベース URL<ept id="p1">**</ept> を生成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For testing and simplicity, the URL that exists for the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> Channel profile can be reused.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テストとわかりやすくするために、<bpt id="p1">**</bpt>既定の<ept id="p1">**</ept>チャネル プロファイルに存在する URL を再利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>For on-premises deployments, the <bpt id="p1">**</bpt>Media Server Base URL<ept id="p1">**</ept> will be where all media is stored for POS devices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置では、<bpt id="p1">**</bpt>メディア サーバー ベースの URL<ept id="p1">**</ept> は、POS デバイスのすべてのメディアが格納されている場所になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channels<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail stores<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>All retail stores<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャンネル<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売店舗<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>すべての小売店舗<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Select the Retail channel ID for the retail store that will use the new channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャネル データベースを使用する小売店の小売チャネル ID を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>On the details page for the selected store, on the Action Pane, select <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したストアの詳細ページにある、アクション ウィンドウで、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>On the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> FastTab for the store, in the <bpt id="p2">**</bpt>Live channel database<ept id="p2">**</ept> field, select the channel database that you created in step 3.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗の<bpt id="p1">**</bpt>一般<ept id="p1">**</ept>クイック タブの、<bpt id="p2">**</bpt>ライブ チャネル データベース<ept id="p2">**</ept>フィールドで、手順 3 で作成したチャネル データベースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>On the <bpt id="p1">**</bpt>General<ept id="p1">**</ept> FastTab for the store, in the <bpt id="p2">**</bpt>Channel profile<ept id="p2">**</ept> field, select the channel profile that you created in step 12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗の<bpt id="p1">**</bpt>一般<ept id="p1">**</ept>クイック タブの、<bpt id="p2">**</bpt>チャネル プロファイル<ept id="p2">**</ept>フィールドで、手順 12 で作成したチャネル プロファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Channel data group<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>チャンネル データ グループ<ept id="p4">**</ept>の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Select the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> data group, and then, on the Action Pane, select <bpt id="p2">**</bpt>Full data sync<ept id="p2">**</ept>. In the <bpt id="p3">**</bpt>Select a distribution schedule<ept id="p3">**</ept> field, select job <bpt id="p4">**</bpt>9999<ept id="p4">**</ept>, and then select <bpt id="p5">**</bpt>OK<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>既定<ept id="p1">**</ept> データ グループを選択した後、アクション ウィンドウで、<bpt id="p2">**</bpt>完全データ同期<ept id="p2">**</ept> を選択します。<bpt id="p3">**</bpt>配送スケジュールの選択<ept id="p3">**</ept> のフィールドで、ジョブ <bpt id="p4">**</bpt>9999<ept id="p4">**</ept> を選択し、<bpt id="p5">**</bpt>OK<ept id="p5">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In the dialog box that appears, select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept> to confirm the full synchronization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるダイアログ ボックスで、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択して完全同期を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>All the data in the channel database is prepared for download.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル データベース内のすべてのデータはダウンロードの準備をします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>After the first Retail Store Scale Unit is created, it requires less data generation to perform a full data sync from the Channel database instead of the Channel data group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初の Retail Store Scale Unit を作成したら、チャネル データ グループではなくチャンネル データベースからの完全なデータ同期を実行するために必要なデータ生成が少なくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Download the Retail Store Scale Unit installer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>In Retail headquarters, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Channel database<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、<bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>チャネル データベース<ept id="p4">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>In the list of channel databases on the left, select the channel database that you created earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">左のチャネル データベースの一覧で、以前に作成したチャネル データベースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Download<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the drop-down menu, select <bpt id="p1">**</bpt>Configuration file<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドロップダウン メニューで、<bpt id="p1">**</bpt>コンフィギュレーション ファイル<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>To help ensure that the Retail Store Scale Unit installer correctly uses the configuration file (XML file), you must save the configuration file to the same location as the installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーが構成ファイル (XML ファイル) を正しく使用するためには、構成ファイルをインストーラと同じ場所に保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>For on-premises deployments, the configuration file (at this time) requires manual editing:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス配置では、構成ファイル (この時点で) を手動で編集する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>StoreSystemAosUrl should have the value used to access headquarters (AX).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">StoreSystemAosUrl には、Headquarters (AX) へのアクセスに使用される値が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>It is critical to keep a trailing slash at the end of this URL (for example, <bpt id="p1">**</bpt><ph id="ph1">https://myContosoURL.com/namespaces/AXSF/</ph><ept id="p1">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この URL の末尾にスラッシュを保持することが重要です (たとえば、<bpt id="p1">**</bpt><ph id="ph1">https://myContosoURL.com/namespaces/AXSF/</ph><ept id="p1">**</ept>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>AADTokenIssuerPrefix should have the value <bpt id="p1">**</bpt><ph id="ph1">https://NOTUSED.microsoft.com</ph><ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AADTokenIssuerPrefix には値 <bpt id="p1">**</bpt><ph id="ph1">https://NOTUSED.microsoft.com</ph><ept id="p1">**</ept> が必要です</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>TransactionServiceAzureAuthority should have the value <bpt id="p1">**</bpt>https://&lt;ADFS FQDN including .com&gt;/adfs<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransactionServiceAzureAuthority には値 <bpt id="p1">**</bpt>https://&lt;ADFS FQDN (.com を含む)&gt;/adfs<ept id="p1">**</ept> が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>TransactionServiceAzureResource should have the same value as the <bpt id="p1">**</bpt>StoreSystemAosUrl<ept id="p1">**</ept> listed in the same configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TransactionServiceAzureResource には、同じ構成ファイルにリストされた <bpt id="p1">**</bpt>StoreSystemAosUrl<ept id="p1">**</ept> と同じ値が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>On the Notification bar that appears at the bottom of the Internet Explorer window, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer ウィンドウの下部に表示される通知バーで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>(The Notification bar might appear in a different place in other browsers.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Browsers might block the download pop-up that is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーは、生成されたダウンロード ポップアップをブロックする可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Select either <bpt id="p1">**</bpt>Allow once<ept id="p1">**</ept> or <bpt id="p2">**</bpt>Options for this site<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Always allow<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 回許可<ept id="p1">**</ept> または <bpt id="p2">**</bpt>このサイトのオプション<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>常に許可<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Then select <bpt id="p1">**</bpt>Download<ept id="p1">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、再度 <bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Download<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>ダウンロード<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>On the drop-down menu, select <bpt id="p1">**</bpt>Retail Store Scale Unit package<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドロップダウン メニューで、<bpt id="p1">**</bpt>Retail Store Scale Unit パッケージ<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>On the Notification bar that appears at the bottom of the Internet Explorer window, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer ウィンドウの下部に表示される通知バーで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>(The Notification bar might appear in a different place in other browsers.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(通知バーは、他のブラウザでは別の場所に表示される場合があります。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The correct installation package is automatically selected for download, based on the Retail Store Scale Unit package on the selected channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択したチャネル データベースの Retail Store Scale Unit パッケージに基づいて、適切なパッケージがダウンロード用に自動的に選択されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>After the setup installer has been saved, on the Notification bar, select <bpt id="p1">**</bpt>Run<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップ インストーラが保存されたら、通知バーの、<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>(This step might differ, depending on the type of browser.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この手順はブラウザの種類によって異なる場合があります。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Run the Retail Store Scale Unit installer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーを実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>If you will install and use Retail Cloud POS, you must initialize the configuration the first time that you run the installer, as described in the following procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS をインストールし、使用する場合は、次の手順に従って、インストーラーを初めて実行するときに構成を初期化する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Before you run the Retail Store Scale Unit installer, make sure that all <bpt id="p1">[</bpt>system requirements<ept id="p1">](../../fin-and-ops/get-started/system-requirements.md)</ept> are met.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーを実行する前に、すべての <bpt id="p1">[</bpt>システム要件<ept id="p1">](../../fin-and-ops/get-started/system-requirements.md)</ept> が満たされていることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>If you are installing Retail Store Scale Unit for use with an on-premises environment, you must start it from a command line using administrator privileges as follows: StoreSystemSetup.exe -UseAdfsAuthentication</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境で使用する Retail Store Scale Unit をインストールする場合は、次のように、管理者権限を使用して、コマンド ラインから起動する必要があります: StoreSystemSetup.exe -UseAdfsAuthentication</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>The Retail Store Scale Unit installer first extracts the associated files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーが最初に関連付けられているファイルを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>It then begins the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the first page of the installer, select the components to install.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーの最初のページで、インストールするコンポーネントを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>You can install the following components:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコンポーネントをインストールすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Retail channel database together with Async Client</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売チャンネル データベースと非同期クライアント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Retail Server</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Retail Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売クラウド POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>To install Retail Cloud POS, you must also select and install Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS をインストールするには、Retail Server も選択してインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>If you will use only Retail Modern POS in the store, clear the <bpt id="p1">**</bpt>Retail Cloud POS<ept id="p1">**</ept> check box, and continue with installation process as it's described here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">店舗内で Retail Modern POS のみを使用する場合は、<bpt id="p1">**</bpt>Retail Cloud POS<ept id="p1">**</ept> チェック ボックスをオフにして、ここで説明されているようにインストール プロセスを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>By default, the installer installs all components on one computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、インストーラーはすべてのコンポーネントを 1 台のコンピュータにインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>To install the components across multiple computers, you must complete additional manual steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のコンピューターにコンポーネントをインストールするには、追加の手動手順を完了する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>For more information, see the "Multiple-computer installation" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「複数のコンピューターのインストール」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>After you've selected all the components to install, select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールするすべてのコンポーネントを選択した後、<bpt id="p1">**</bpt>次<ept id="p1">**</ept>を選択して続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>The installer validates that all prerequisites are met.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーは、すべての前提条件が満たされていることを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>If a valid version of Microsoft SQL Server isn't found, the installer downloads and installs Microsoft SQL Server 2014 Express with Service Pack 2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server の有効なバージョンが見つからない場合は、インストーラーが、Microsoft SQL Server 2014 with Service Pack 2 をダウンロードし、インストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>To meet the prerequisites, SQL Server must have full-text search, and it must support, at a minimum, Transport Layer Security (TLS) 1.2.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この前提条件を満たすためには、SQL Server に全文検索機能を搭載し、最低限トランスポート層セキュリティ (TLS) 1.2 がサポートされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>For Microsoft SQL Server 2012, Service Pack 3 must be installed, at a minimum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2012 では、最低でも、Service Pack 3 がインストールされる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>For Microsoft SQL Server 2014, Service Pack 2 must be installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft SQL Server 2014 では、Service Pack 2 がインストールされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>If a system restart is required, the installer will prompt the user.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムの再起動が必要な場合、インストーラーはユーザーにプロンプトを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>This prompt is based upon a Windows system registry key that tells all applications if a restart is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この確認は、再起動が必要かどうかをすべてのアプリケーションに通知する Windows システム レジストリ キーに基づいています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>While it is recommended to restart prior to continuing the installation, a restart is not mandatory and the installer can continue without restarting the computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールを続行する前に再起動することをお勧めしますが、再起動は必須ではなく、インストーラーはコンピュータを再起動せずに続行することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Verify the URL for Application Object Server (AOS), and then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS) の URL を確認し、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>(The AOS URL is the URL that is used to access Retail headquarters.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(AOS URL とは、小売用バックオフィスにアクセスするために使用される URL のことです。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>The Retail Server URL is automatically entered from the configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Server URL は、構成ファイルから自動的に入力されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>Select a valid Secure Sockets Layer (SSL) certificate to use for HTTPS communication.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HTTPS 通信に使用する、有効な Secure Sockets Layer (SSL) 証明書を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>The certificate must use private key storage, and server authentication must be listed in the enhanced key usage property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">証明書は秘密キー ストレージを使用する必要があり、サーバー認証は拡張キー使用プロパティにリストされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Additionally, the certificate must be trusted locally, and it can't be expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、証明書はローカルに信頼される必要があり、期限切れにすることはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>It must be stored in the personal certificate store location on the local computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ローカル コンピューターの個人用証明書格納場所に保存する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>If a specific user is required, enter the user name and password that the application pool should run under.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">特定のユーザーが必要な場合は、アプリケーション プールを実行するために必要なユーザー名とパスワードを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>By default, the installer automatically generates a service account to use.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、インストーラーは自動的に使用するサービス アカウントを生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>This approach is more secure and is recommended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、安全性がより向上するためお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>It is important to note that service accounts, out of box, still function under the same password policy that is defined for all other accounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初から用意されているサービス アカウントは、他のすべてのアカウントに定義されているのと同じパスワード ポリシー下で引き続き機能する点に留意することは重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>This means that the minimum password age policy still applies to the Retail Store Scale Unit service account and must be updated when necessary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">つまり、最小限のパスワード有効期間ポリシーが引き続き Retail Store Scale Unit サービス アカウントに適用されるため、必要な場合に更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>By default, on Windows Server 2012 R2, this is typically 42 days.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、Windows Server 2012 R2 では通常 42 日です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>If the password does expire on a used service account, the Retail Server will fail to continue functioning until the issue is resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されるサービス アカウントのパスワードが期限切れの場合、問題が解決されるまで Retail サーバーが機能しなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>On the next page, enter the user account and password for the Retail Server application pool and Async Client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、小売サーバー アプリケーション プールと Async Client のユーザー アカウントとパスワードを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>By default, this account is automatically generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、このアカウントは自動的に生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>However, you can manually enter the user account and password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、ユーザー アカウントとパスワードを手動で入力できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Enter the HTTPS port to use, and verify that the host name of the computer is correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用する HTTPS ポートを入力し、コンピューターのホスト名が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>Then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択して続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>The installer automatically enters the host name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーは自動的にホスト名を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>If, for any reason, the host name must be changed for the installation, change it here.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">何らかの理由で、インストールのためにホスト名を変更する必要がある場合は、ここで変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>The host name must be the FQDN of the system, and it must be entered in the <bpt id="p1">**</bpt>Host name<ept id="p1">**</ept> field for the selected Store system entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ホスト名はシステムの FQDN でなければなりません。また、選択した Store システム エントリの <bpt id="p1">**</bpt>ホスト名<ept id="p1">**</ept>フィールドに入力する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Enter the application ID (client ID) and key (secret) that are associated with this Retail Store Scale Unit installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ID (クライアント ID) および Retail Store Scale Unit インストールと関連するキー (シークレット) を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>Additionally, verify the channel database ID, which is automatically entered from the configuration file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、コンフィギュレーション ファイルから自動的に入力されるチャネル データベース ID を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Then select <bpt id="p1">**</bpt>Install<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>インストール<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>If you will use Retail Cloud POS, make sure that the <bpt id="p1">**</bpt>Configure Retail Cloud POS<ept id="p1">**</ept> check box at the bottom of the page is selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS を使用する場合は、ページの下部にある <bpt id="p1">**</bpt>Retail Cloud POS のコンフィギュレーション<ept id="p1">**</ept> チェック ボックスが選択されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>This configuration requests Azure AD sign-in and automatically generates all required information in Azure, so that Retail Cloud POS can be used on-premises.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この構成では Azure AD サインインが要求され、必要なすべての情報が Azure で自動的に生成され、Retail Cloud POS をオンプレミスで使用できるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>If you are installing Retail Store Scale Unit for use with an on-premises environment, you must clear this option.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境で使用する Retail Store Scale Unit をインストールする場合、このオプションをオフにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>For information about how to create web applications in Azure, see <bpt id="p1">[</bpt>Create an Azure Active Directory application<ept id="p1">](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure で Web アプリケーションを作成する方法については、<bpt id="p1">[</bpt>Azure Active Directory アプリケーションを作成する<ept id="p1">](/azure/azure-resource-manager/resource-group-create-service-principal-portal#create-an-azure-active-directory-application)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>When installing Retail Store Scale Unit for use with an on-premises environment, Retail Cloud POS does not require an Azure or AD FS application to be configured, so it is important to unmark <bpt id="p1">**</bpt>Configure Retail Cloud POS<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プレミス環境で使用する Retail Store Scale Unit をインストールするとき、Retail クラウド POS は Azure または AD FS アプリケーションの構成を要求しないため、<bpt id="p1">**</bpt>Retail クラウド POS のコンフィギュレーション<ept id="p1">**</ept> のマークを解除することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>When installing Retail Store Scale Unit for use with an on-premises environment, the Client ID (Application ID) and Secret (Key) used will be the values generated by the PowerShell script performed in the configuration steps performed in steps 6-8 in the <bpt id="p1">[</bpt>Installation steps for Retail channel components in an on-premises environment<ept id="p1">](../../dev-itpro/deployment/deploy-retail-onprem.md)</ept> topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オンプレミス環境で使用する Retail Store Scale Unit をインストールするとき、使用されるクライアント ID (アプリケーション ID) およびシークレット (キー) は、<bpt id="p1">[</bpt>オンプレミス環境の Retail チャネル コンポーネントのインストール手順<ept id="p1">](../../dev-itpro/deployment/deploy-retail-onprem.md)</ept>トピックの手順6 ～ 8 で実行される構成手順で実行される PowerShell スクリプトによって生成される値になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>(Step 6 creates the Client ID and step 8 resets the Secret to be copied.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(手順 6 ではクライアント ID を作成し、手順 8 ではコピーされるシークレットをリセットします)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>When you create the Web App, the initial URI and URL don't have to be any specific value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web アプリを作成するとき、最初の URI と URL は特定の値である必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>Only the application ID (client ID) and key (secret) that are created are important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成されるアプリケーション ID (クライアント ID) とキー (シークレット) のみ重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>After the application ID (client ID) and key (secret) are created for Retail Store Scale Unit, the application ID (client ID) must be accepted in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit にアプリケーション ID (クライアント ID) とキー (シークレット) が作成され、アプリケーション ID (クライアント ID) は、小売で受け入れる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>Follow the next procedure to finish the configuration in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスでコンフィギュレーションを完了する次の手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>After the installation is complete, the final health page appears.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールが完了すると、最終正常性ページが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>This page shows whether the installation was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページには、インストールが成功したかどうかが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>It also shows the health of each component, based on basic connection tests, and the location of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、基本的な接続テストに基づいた各コンポーネントの正常性と、このトピックの場所について示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>If the installation wasn't successful, the page shows the location of the log files.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールに失敗した場合は、ページにログ ファイルの場所が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>We recommend that you keep this final health page open until you've completed the configuration of Retail Store Scale Unit and all components are working correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のコンフィギュレーションを完了して、すべてのコンポーネントが正しく動作するまで、この最終正常性ページを開いたままにしておくことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Finish the Retail Store Scale Unit configuration in headquarters</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Headquarters で Retail Store Scale Unit のコンフィギュレーションを完了する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>The last steps require validation and verification that the Azure application ID (client ID) and key (secret) are correctly accepted in Retail headquarters, so that connections can be made between the environment and the new Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後のステップでは、Azure アプリケーション ID (クライアント ID) とキー (シークレット) が小売用バックオフィスで正しく受け入れられ、環境と新しい Retail Store Scale Unit との接続が可能であることを検証し、確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>After the application ID (client ID) and key (secret) are created for Retail Store Scale Unit and entered in the installer, the application ID (client ID) must be accepted in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit にアプリケーション ID (クライアント ID) とキー (シークレット) が作成され、インストーラーに入力された後、アプリケーション ID (クライアント ID) は、小売用バック オフィスで受け入れる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>In Retail headquarters, go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory applications<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、<bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>セットアップ<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory アプリケーション<ept id="p3">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>Enter the application ID (client ID) in the <bpt id="p1">**</bpt>Client ID<ept id="p1">**</ept> column, enter descriptive text in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> column, and enter <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> in the <bpt id="p4">**</bpt>User ID<ept id="p4">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション ID (クライアントID) を<bpt id="p1">**</bpt>クライアント ID<ept id="p1">**</ept> 列に入力し、説明のテキストを<bpt id="p2">**</bpt>名<ept id="p2">**</ept>列に入力および <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> を<bpt id="p4">**</bpt>ユーザー ID<ept id="p4">**</ept> 列に入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>If Retail Cloud POS is configured for use, a client ID is shown at the end of the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS を使用するように設定されている場合、インストールの最後にクライアント ID が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>You must add this client ID to the <bpt id="p1">**</bpt>Retail shared parameters<ept id="p1">**</ept> page in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクライアント ID を小売の <bpt id="p1">**</bpt>小売共有パラメーター<ept id="p1">**</ept> ページに追加する必要があります、</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>In Retail headquarters, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Parameters<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail shared parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>パラメーター<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売共有パラメーター<ept id="p4">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source>Select <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>On the <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept> FastTab, select the provider that begins with <ph id="ph1">`HTTPS://sts.windows.net/`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> クイック タブで、<ph id="ph1">`HTTPS://sts.windows.net/`</ph> で始まるプロバイダーを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source>The values on the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab are set, based on your selection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択に基づいて、<bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept> FastTab の値が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>On the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>Enter the client ID that is listed on the final health page of the Retail Store Scale Unit installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーの最終正常性ページに表示されているクライアント ID を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Set the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> and the <bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Type<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> に、<bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> フィールドを <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Then, on the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[アクション] ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>Select the new relying party, and then, on the <bpt id="p1">**</bpt>Server resource IDs<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい依存する関係者を選択し、<bpt id="p1">**</bpt>サーバー リソース ID<ept id="p1">**</ept> クイック タブで <bpt id="p2">**</bpt>追加<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>In the <bpt id="p1">**</bpt>Server Resource ID<ept id="p1">**</ept> column, enter <ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サーバー リソース ID<ept id="p1">**</ept> 列に、<ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>In Retail headquarters, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Parameters<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail shared parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスで、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>パラメーター<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売共有パラメーター<ept id="p4">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Select <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>On the <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>In the new <bpt id="p1">**</bpt>Issuer<ept id="p1">**</ept> row, enter the Retail Server URL of the newly installed Retail Store Scale Unit.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい<bpt id="p1">**</bpt>発行者<ept id="p1">**</ept>行に、新たにインストールした Retail Store Scale Unit の Retail サーバー URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source>At the end of the URL, add <bpt id="p1">**</bpt>/auth<ept id="p1">**</ept>. The URL will resemble <ph id="ph1">`https://&lt;My Case-Sensitive Computer Name&gt;:&lt;Port Number&gt;/RetailServer/auth`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL の末尾に <bpt id="p1">**</bpt>/auth<ept id="p1">**</ept> を追加します。URL は <ph id="ph1">`https://&lt;My Case-Sensitive Computer Name&gt;:&lt;Port Number&gt;/RetailServer/auth`</ph> のようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source>The URL described above is case sensitive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記 URL では、大文字と小文字を区別します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>There will be a new identity provider line for each Retail Store Scale Unit that is installed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールされている各 Retail Store Scale Unit に新しい ID プロバイダー行があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source>Each Retail Store Scale Unit will have a URL that resembles this URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 Retail Store Scale Unit では、この URL に似た URL が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>In the <bpt id="p1">**</bpt>Name<ept id="p1">**</ept> column, enter a description for the store that the URL belongs to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>名前<ept id="p1">**</ept>列に、URL が属する店舗の説明を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>In the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> column, select <bpt id="p2">**</bpt>Open ID Connect<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>タイプ<ept id="p1">**</ept>列で、<bpt id="p2">**</bpt>OpenID 接続<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>This new row must be duplicated for every Retail Store Scale Unit installation (that is, for every unique URL).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この新しい行は、すべての Retail Store Scale Unit のインストール (つまり、一意の URL ごと) ごとに複製する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>On the <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept> FastTab, select the newly created line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept>クイック タブで、新しく作成された明細行を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>The values on the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab are set, based on your selection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択に基づいて、<bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept> FastTab の値が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>On the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>, and add the following two entries:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択し、次の 2 つのエントリを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>In the <bpt id="p1">**</bpt>ClientId<ept id="p1">**</ept> column, enter <bpt id="p2">**</bpt>Cloud POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ClientId<ept id="p1">**</ept> 列に、<bpt id="p2">**</bpt>クラウド POS<ept id="p2">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Set the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> and the <bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Type<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> に、<bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> フィールドを <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>In the <bpt id="p1">**</bpt>ClientId<ept id="p1">**</ept> column, enter <bpt id="p2">**</bpt>Modern POS<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ClientId<ept id="p1">**</ept> 列に、<bpt id="p2">**</bpt>Modern POS<ept id="p2">**</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>Set the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> and the <bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Type<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> に、<bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> フィールドを <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>In Retail, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution Schedule<ept id="p3">**</ept>, and run CDX Job <bpt id="p4">**</bpt>1110<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail では、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept>へ移動し、CDX ジョブ <bpt id="p4">**</bpt>1110<ept id="p4">**</ept> を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>When you've finished, return to the installer, and select <bpt id="p1">**</bpt>Finish<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したら、インストーラーに戻り、<bpt id="p1">**</bpt>完了<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>The final page of the installer includes valuable information that you can use to test and validate that all components work correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーの最後のページには、すべてのコンポーネントが正しく動作することをテストして検証するために使用できる貴重な情報が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source>Keep this page open until you've completed the validation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このページは、検証が完了する段階まで開いたままにしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>If the installer doesn't show a check mark for Retail Server, Async Client, or any other component, wait 10 minutes, so that any cached values can be updated in the cloud.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストーラーが Retail Server、Async Client、またはその他のコンポーネントのチェック マークを表示しない場合は、10 分待って、キャッシュされた値をクラウドで更新できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source>Then check again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">再び確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>If the installer still isn't fully successful, run a full synchronization on the new channel database that this installation uses.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それでもインストーラーが完全に成功しない場合は、このインストールを使用する新しいチャンネル データベースで完全同期を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>If you followed all the steps correctly, your configuration should have these characteristics:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべての手順を正しく実行する場合、構成には次の特性が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>In Azure, two web applications have been automatically generated through the installer:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure では、2 つの Web アプリケーションはインストーラー経由で自動的に生成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Retail Store Scale Unit Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unitクラウド POS</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Retail Store Scale Unit Retail Server for Cloud POS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit Cloud POS 用 Retail サーバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>In Azure, a web application (that is, an App registration in the new Azure portal) has been manually created for each Retail Store Scale Unit installation (for example, RetailStoreScaleUnitHouston).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure では、Web アプリケーション (つまり、新しい Azure ポータルでのアプリ登録) は各 Retail Store Scale Unit インストールに対して手動で作成されています (たとえば、RetailStoreScaleUnitHouston)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>A key (secret) has been created that can be used in the installer, as described earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作成されたキー (シークレット) は、前述のようにインストーラーで使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source>The application ID (client ID) of the manually created web application has been added to the <bpt id="p1">**</bpt>Azure Active Directory applications<ept id="p1">**</ept> page in Retail, as explained in step 1 of the preceding procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">手動で作成した Web アプリケーションのアプリケーション ID (クライアント ID) は、前の手順のステップ 1 で説明したように、Retail の <bpt id="p1">**</bpt>Azure Active Directory アプリケーション<ept id="p1">**</ept> ページに追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>The Retail Cloud POS application ID (client ID) that was shown at the end of the Retail Store Scale Unit installer has been added on the <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept> FastTab, as explained in the final steps of the "Run the Retail Store Scale Unit installer" section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーの最後に表示される Retail Cloud POS アプリケーション ID (クライアント ID) は、「Retail Store Scale Unit インストーラーを実行」セクションの最後の手順で説明されているように、<bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> クイック タブに追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>Multiple-computer installation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">複数のコンピューターのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Only advanced users should install Retail Store Scale Unit across multiple computers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上級者のみ、複数のコンピュータに Retail Store Scale Unit をインストールする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>The following set of procedures explains how to install the Retail channel database and Async Client on one computer, and Retail Server and Retail Cloud POS on a second computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の一連の手順では、1 台のコンピューターに Retail チャネル データベースと Async Client、2 台目のコンピューターに Retail Server と Retail Cloud POS をインストールする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>The instructions assume that both systems are on the same domain, and that users for the services that will be installed have already been created on both systems.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指示では、両方のシステムが同じドメイン上にあり、インストールされるサービスのユーザーが両方のシステムで既に作成されていることが前提です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>It's important that you do all configuration in Retail headquarters.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">小売用バックオフィスですべてのコンフィギュレーションを行うことが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Installation on the first computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のコンピューターへのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source>On the first computer, run the Retail Store Scale Unit self-service installer as described earlier in this topic, but make the following changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のコンピューターで、このトピックの前のところで説明したように、Retail Store Scale Unit セルフ サービス インストーラーを実行しますが、次の変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Select only Retail channel database and Async Client as the components to install.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールするコンポーネントとして Retail チャネル データベースと非同期クライアントのみを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>Then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to continue with the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後 <bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択して、インストールを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>You can use a generated service account for Async Client, because Async Client won't be accessed outside the computer that it's installed on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Async Client はインストールされたコンピューターの外部からアクセスすることができないため、Async Client のために生成されたサービス アカウントを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Enter the client ID and key (secret).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント ID およびキー (シークレット) を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Keep these details available, so that you can use them again on the second computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 台目のコンピューターで再度使用できるように、これらの詳細情報を使用可能な状態にしておきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>After a client ID and key (secret) are created for Retail Store Scale Unit, the client ID must be accepted in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のクライアント ID と キー (シークレット) が作成された後、クライアント ID を、小売で受け入れる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>Go to <bpt id="p1">**</bpt>System administration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory applications<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>システム管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Azure Active Directory アプリケーション<ept id="p3">**</ept> の順に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Enter the client ID in the <bpt id="p1">**</bpt>Client ID<ept id="p1">**</ept> column, enter descriptive text in the <bpt id="p2">**</bpt>Name<ept id="p2">**</ept> column, and enter <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> in the <bpt id="p4">**</bpt>User ID<ept id="p4">**</ept> column.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クライアント ID を<bpt id="p1">**</bpt>クライアント ID<ept id="p1">**</ept> 列に入力し、説明のテキストを<bpt id="p2">**</bpt>名<ept id="p2">**</ept>列に入力および <bpt id="p3">**</bpt>RetailServiceAccount<ept id="p3">**</ept> を<bpt id="p4">**</bpt>ユーザー ID<ept id="p4">**</ept> 列に入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>When setup is successful, start SQL Server Configuration Manager.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップが正常に行われたときは、SQL Server 構成マネージャーを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>Go to <bpt id="p1">**</bpt>SQL Server Network Configuration<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Protocols<ept id="p2">**</ept> for the SQL Server instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server インスタンスの <bpt id="p1">**</bpt>SQL Server ネットワークの構成<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>プロトコル<ept id="p2">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>Right-click, and then select <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、<bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>In the <bpt id="p1">**</bpt>Flags<ept id="p1">**</ept> section, change the value of <bpt id="p2">**</bpt>Set Force Encryption<ept id="p2">**</ept> to <bpt id="p3">**</bpt>Yes<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フラグ<ept id="p1">**</ept> セクションで、<bpt id="p2">**</bpt>強制暗号化の設定<ept id="p2">**</ept>の値を<bpt id="p3">**</bpt>はい<ept id="p3">**</ept>に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>In the <bpt id="p1">**</bpt>Certificate<ept id="p1">**</ept> section, select the SSL certificate on the drop-down menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>証明書<ept id="p1">**</ept>セクションで、ドロップダウン メニューから SSL 証明書を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>This SQL Server SSL certificate is the same certificate that is used in the installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この SQL Server SSL 証明書は、インストーラーで使用されているのと同じ証明書です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Go back to <bpt id="p1">**</bpt>Protocols<ept id="p1">**</ept> in SQL Server Configuration Manager, and enable the following protocols:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server 構成マネージャで<bpt id="p1">**</bpt>プロトコル<ept id="p1">**</ept>に戻り、次のプロトコルを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Named Pipes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">名前付きパイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>TCP/IP</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TCP/IP</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Right-click the <bpt id="p1">**</bpt>TCP/IP<ept id="p1">**</ept> protocol, and then select <bpt id="p2">**</bpt>Properties<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TCP/IP<ept id="p1">**</ept> プロトコルを右クリックし、<bpt id="p2">**</bpt>プロパティ<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>In the <bpt id="p1">**</bpt>IP Address<ept id="p1">**</ept> section, scroll down the list to <bpt id="p2">**</bpt>IPALL<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>IP アドレス<ept id="p1">**</ept> セクションで、一覧を <bpt id="p2">**</bpt>IPALL<ept id="p2">**</ept> まで下方向にスクロールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Enter <bpt id="p1">**</bpt>TCPPort = 1433<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>TCPPort = 1433<ept id="p1">**</ept> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source>Select <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="366">
          <source>Start Microsoft Windows Firewall with Advanced Security.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">高度なセキュリティの Microsoft Windows ファイアウォールを起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="367">
          <source>In Windows Firewall, create an inbound rule to open TCP port 1433.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ファイアウォールで、TCP ポート 1433 を開放する受信ルールを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="368">
          <source>For detailed information about SQL Server and Windows Firewall, see <bpt id="p1">[</bpt>Configure a Windows Firewall for Database Engine Access<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175043.aspx)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL Server および Windows ファイアウォールに関する詳細については、<bpt id="p1">[</bpt>データベース エンジンへ アクセス用の Windows ファイアウォールをコンフィギュレーションする<ept id="p1">](https://msdn.microsoft.com/en-us/library/ms175043.aspx)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="369">
          <source>Installation on the second computer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 台目のコンピューターへのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="370">
          <source>On the second computer, run the Retail Store Scale Unit Self-service installer as described earlier in this topic, but make the following changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 台目のコンピューターで、このトピックの前のところで説明したように、Retail Store Scale Unit セルフ サービス インストーラーを実行しますが、次の変更を行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="371">
          <source>Select only Retail Server and Retail Cloud POS as the components to install.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インストールするコンポーネントとして Retail Server と Retail Cloud POS のみを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="372">
          <source>If only Retail Server must to be installed, don't select Retail Cloud POS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーをインストールする必要がある場合は、Retail クラウド POS を選択できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="373">
          <source>Then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept> to continue with the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後 <bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択して、インストールを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="374">
          <source>Enter the domain user credentials (user name and password) that have permission to access SQL Server on the first computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のコンピュータで、SQL Server にアクセスする権限を持つドメイン ユーザーの資格情報 (ユーザー名およびパスワード) を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="375">
          <source>Then select <bpt id="p1">**</bpt>Next<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その後、<bpt id="p1">**</bpt>次へ<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="376">
          <source>A generated service account can't be used, because Retail Server requires access to the SQL database on the first computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail サーバーでは、最初のコンピューター上の SQL データベースへのアクセスが必要なため、生成されたサービス アカウントは使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="377">
          <source>You must use a domain account.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ドメイン アカウントを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="378">
          <source>Enter the same client ID and key (secret) that are used on the first computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のコンピューターで使用される同じクライアント ID およびキー (シークレット) を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="379">
          <source>It's critical that you add this client ID to Retail as described earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前述のように Retail にこのクライアント ID を追加することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="380">
          <source>Select <bpt id="p1">**</bpt>Configure Cloud POS<ept id="p1">**</ept>, and then enter Azure AD credentials that have the correct permissions to create Azure Web Apps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラウド POS のコンフィギュレーション<ept id="p1">**</ept> を選択し、Azure Web アプリケーションを作成するための適切なアクセス許可を持つ Azure AD 資格情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="381">
          <source>For more information about Azure Web Apps, how to create them, and how to generate a new key (secret), see <bpt id="p1">[</bpt>Use portal to create an Azure Active Directory application and service principal that can access resources<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/resource-group-create-service-principal-portal/)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Azure Web アプリ、それを作成する方法、および新しいキー (シークレット) を生成する方法の詳細については、<bpt id="p1">[</bpt>リソースにアクセスできる Azure Active Directory アプリケーションおよびサービス プリンシパルを作成するポータルの使用<ept id="p1">](https://azure.microsoft.com/en-us/documentation/articles/resource-group-create-service-principal-portal/)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="382">
          <source>Note that the sign-in URL and the App ID URI are not important.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインイン URL やアプリ ID URI は重要ではないことに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="383">
          <source>When setup is successful, don't exit the installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">セットアップが正常に行われたときは、インストーラーを終了しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="384">
          <source>At first, the health check ping won't be successful, because the database isn't yet set up correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初は、データベースがまだ正しく設定されていないため、ヘルスチェック ping は成功しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="385">
          <source>After you've completed the remaining steps of this procedure, you can test the health check again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この手順の残りのステップを完了した後は、再度稼働状況チェックをテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="386">
          <source>Start <bpt id="p1">**</bpt>Microsoft Internet Information Services (IIS)<ept id="p1">**</ept>, select the <bpt id="p2">**</bpt>Retail Store Scale Unit<ept id="p2">**</ept> website, and select the <bpt id="p3">**</bpt>Retail Server<ept id="p3">**</ept> web application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft インターネット インフォメーション サービス (IIS)<ept id="p1">**</ept> を起動し、<bpt id="p2">**</bpt>Retail Store Scale Unit<ept id="p2">**</ept> Web サイトを選択して <bpt id="p3">**</bpt>Retail Server<ept id="p3">**</ept> Web アプリケーションを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="387">
          <source>Explore the working directory.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業ディレクトリを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="388">
          <source>Open the Web.config file, and then, in the <bpt id="p1">**</bpt>connectionStrings<ept id="p1">**</ept> section, add <bpt id="p2">**</bpt>Server name<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web.config ファイルを開いて、<bpt id="p1">**</bpt>connectionStrings<ept id="p1">**</ept> セクションで、<bpt id="p2">**</bpt>サーバー名<ept id="p2">**</ept>を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="389">
          <source><bpt id="p1">**</bpt>Server name<ept id="p1">**</ept> is the name of the first computer where you installed components.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サーバー名<ept id="p1">**</ept> はユーザーがコンポーネントをインストールした最初のコンピュータの名前です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="390">
          <source>Save the file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="391">
          <source>If the certificate that is used isn't a valid, trusted certificate from a trusted authority, open CERTMGR.MSC, and follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用されている証明書が信頼できる機関の有効な信頼できる証明書でない場合は、CERTMGR.MSC を開いて次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="392">
          <source>Import the SQL Server SSL certificate that you created earlier, and add it to Trusted Root.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前に作成した SQL Server SSL 証明書をインポートし、信頼されたルートに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="393">
          <source>Open a <bpt id="p1">**</bpt>Command Prompt<ept id="p1">**</ept> window as an administrator, type <bpt id="p2">**</bpt>IISRESET<ept id="p2">**</ept>, and then press Enter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">管理者として<bpt id="p1">**</bpt>コマンド プロンプト<ept id="p1">**</ept> ウィンドウを開き、<bpt id="p2">**</bpt>IISRESET<ept id="p2">**</ept> と入力し、Enter キーを押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="394">
          <source>If Retail Cloud POS is configured for use, a client ID is shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Cloud POS を使用するように設定されている場合は、クライアント ID が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="395">
          <source>You must add this client ID to the <bpt id="p1">**</bpt>Retail shared parameters<ept id="p1">**</ept> page in Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクライアント ID を小売の <bpt id="p1">**</bpt>小売共有パラメーター<ept id="p1">**</ept> ページに追加する必要があります、</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="396">
          <source>In Retail, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Parameters<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Retail shared parameters<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail で、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>パラメーター<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>小売共有パラメーター<ept id="p4">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="397">
          <source>Select <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="398">
          <source>On the <bpt id="p1">**</bpt>Identity providers<ept id="p1">**</ept> FastTab, select the provider that begins with <ph id="ph1">`HTTPS://sts.windows.net/`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ID プロバイダー<ept id="p1">**</ept> クイック タブで、<ph id="ph1">`HTTPS://sts.windows.net/`</ph> で始まるプロバイダーを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="399">
          <source>The values on the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab are set, based on your selection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択に基づいて、<bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept> FastTab の値が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="400">
          <source>On the <bpt id="p1">**</bpt>Relying parties<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>依存する関係者<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>追加<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="401">
          <source>Enter the client ID that is listed in the Retail Store Scale Unit installer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit インストーラーに表示されているクライアント ID を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="402">
          <source>Set the <bpt id="p1">**</bpt>Type<ept id="p1">**</ept> field to <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> and the <bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> field to <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Type<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>Public<ept id="p2">**</ept> に、<bpt id="p3">**</bpt>UserType<ept id="p3">**</ept> フィールドを <bpt id="p4">**</bpt>Worker<ept id="p4">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="403">
          <source>Then, on the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">[アクション] ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="404">
          <source>Select the new relying party, and then, on the <bpt id="p1">**</bpt>Server resource IDs<ept id="p1">**</ept> FastTab, select <bpt id="p2">**</bpt>Add<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい依存する関係者を選択し、<bpt id="p1">**</bpt>サーバー リソース ID<ept id="p1">**</ept> クイック タブで <bpt id="p2">**</bpt>追加<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="405">
          <source>In the <bpt id="p1">**</bpt>Server Resource ID<ept id="p1">**</ept> column, enter <ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サーバー リソース ID<ept id="p1">**</ept> 列に、<ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph> と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="406">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="407">
          <source>In Retail, go to <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Headquarters setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Retail scheduler<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>Channel database<ept id="p4">**</ept>, and follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail で、<bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>本社の設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>小売用スケジューラ<ept id="p3">**</ept> <ph id="ph3">&amp;gt;</ph> <bpt id="p4">**</bpt>チャネル データベース<ept id="p4">**</ept>に移動し、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="408">
          <source>Select the channel database that you created at the beginning of this topic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックの先頭に作成したチャネルのデータベースを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="409">
          <source>On the Action Pane, select <bpt id="p1">**</bpt>Full Sync<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Job 9999<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>完全な同期<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>ジョブ 9999<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="410">
          <source>Full synchronization might require several minutes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全な同期には数分間かかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="411">
          <source>In the Retail Store Scale Unit installer, retest to verify that all functionality is working correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のインストーラーで、すべての機能が正常に機能していることを確認するために再テストします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="412">
          <source>Start Retail Cloud POS from the computer that you're using for POS operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">POS 操作を使用しているコンピューターから Retail Cloud POS を起動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="413">
          <source>(This computer is a third computer that is separate from the Retail Store Scale Unit systems.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(このコンピューターは、Retail Store Scale Unit システムとは別の 3 台目のコンピューターです。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="414">
          <source>Activate the Retail Cloud POS device that you're using for this computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコンピューターを使用している Retail Cloud POS デバイスを有効化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="415">
          <source>Do a simple sale to verify full end-to-end functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なエンド ツー エンドの機能を確認する簡易販売を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="416">
          <source>Help secure Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のセキュリティを強化する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="417">
          <source>According to current security standards, the following options should be set in a production environment:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のセキュリティ基準によると、実稼動環境で次のオプションを設定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="418">
          <source>You should completely disable SSL (v2 and v3) on the computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンピューターの SSL (v2およびv3) を完全に無効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="419">
          <source>You should enable and use only TLS version 1.2 (or the current highest version).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS バージョン 1.2 (または、現時点で最も新しいバージョン) のみを有効にし、使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="420">
          <source>By default, SSL and all versions of TLS except TLS 1.2 are disabled.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、SSL および TLS 1.2 を除くすべてのバージョンの TLS は無効です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="421">
          <source>To edit or enable these settings, follow these steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの設定を編集または有効にするには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="422">
          <source>Press the Windows logo key+R to open a <bpt id="p1">**</bpt>Run<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ロゴキーと R キーを同時に押して、<bpt id="p1">**</bpt>実行<ept id="p1">**</ept>ウィンドウを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="423">
          <source>In the <bpt id="p1">**</bpt>Open<ept id="p1">**</ept> field, enter <bpt id="p2">**</bpt>Regedit<ept id="p2">**</ept>, and then select <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept>フィールドに、<bpt id="p2">**</bpt>Regedit<ept id="p2">**</ept> と入力してから <bpt id="p3">**</bpt>OK<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="424">
          <source>In the <bpt id="p1">**</bpt>User Account Control<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>Yes<ept id="p2">**</ept> (if this step is required), and then, in the new <bpt id="p3">**</bpt>Registry Editor<ept id="p3">**</ept> window, go to <bpt id="p4">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>System<ph id="ph4">\\</ph>CurrentControlSet<ph id="ph5">\\</ph>SecurityProviders<ph id="ph6">\\</ph>SCHANNEL<ph id="ph7">\\</ph>Protocols<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ユーザー アカウント制御<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>はい<ept id="p2">**</ept> (この手順が必要である場合) を選択してから、新しい<bpt id="p3">**</bpt>レジストリ エディター<ept id="p3">**</ept> ウィンドウで <bpt id="p4">**</bpt>HKEY<ph id="ph1">\_</ph>LOCAL<ph id="ph2">\_</ph>MACHINE<ph id="ph3">\\</ph>System<ph id="ph4">\\</ph>CurrentControlSet<ph id="ph5">\\</ph>SecurityProviders<ph id="ph6">\\</ph>SCHANNEL<ph id="ph7">\\</ph>Protocols<ept id="p4">**</ept> に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="425">
          <source>The following keys have been automatically entered to enable only TLS 1.2:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のキーは自動的に入力され、TLS 1.2 のみが有効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="426">
          <source>TLS 1.2<ph id="ph1">\\</ph>Server:Enabled=1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.2<ph id="ph1">\\</ph>Server:Enabled=1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="427">
          <source>TLS 1.2<ph id="ph1">\\</ph>Server:DisabledByDefault=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.2<ph id="ph1">\\</ph>Server:DisabledByDefault=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="428">
          <source>TLS 1.2<ph id="ph1">\\</ph>Client:Enabled=1</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.2<ph id="ph1">\\</ph>Client:Enabled=1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="429">
          <source>TLS 1.2<ph id="ph1">\\</ph>Client:DisabledByDefault=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.2<ph id="ph1">\\</ph>Client:DisabledByDefault=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="430">
          <source>TLS 1.1<ph id="ph1">\\</ph>Server:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.1<ph id="ph1">\\</ph>Server:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="431">
          <source>TLS 1.1<ph id="ph1">\\</ph>Client:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.1<ph id="ph1">\\</ph>Client:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="432">
          <source>TLS 1.0<ph id="ph1">\\</ph>Server:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.0<ph id="ph1">\\</ph>Server:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="433">
          <source>TLS 1.0<ph id="ph1">\\</ph>Client:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">TLS 1.0<ph id="ph1">\\</ph>Client:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="434">
          <source>SSL 3.0<ph id="ph1">\\</ph>Server:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSL 3.0<ph id="ph1">\\</ph>Server:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="435">
          <source>SSL 3.0<ph id="ph1">\\</ph>Client:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSL 3.0<ph id="ph1">\\</ph>Client:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="436">
          <source>SSL 2.0<ph id="ph1">\\</ph>Server:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSL 2.0<ph id="ph1">\\</ph>Server:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="437">
          <source>SSL 2.0<ph id="ph1">\\</ph>Client:Enabled=0</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SSL 2.0<ph id="ph1">\\</ph>Client:Enabled=0</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="438">
          <source>No additional network ports should be open, unless they are required for known, specified reasons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">知られている特定の理由で必要とされない限り、追加のネットワーク ポートを開かないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="439">
          <source>You must disable cross-origin resource sharing, and you must specify the allowed origins that are accepted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クロスオリジンのリソース共有を無効にし、許可され承認されたオリジンを指定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="440">
          <source>You should use only trusted certificate authorities to obtain certificates that will be used on Store system computers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Store システムのコンピューターで使用する証明書の取得には、信頼された証明機関のみを活用してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="441">
          <source>It's critical that you review security guidelines for IIS and the Payment Card Industry (PCI) requirements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IIS と Payment Card Industry (PCI) の要件向けのセキュリティ ガイドラインを確認することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="442">
          <source>Troubleshoot Retail Store Scale Unit</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit のトラブルシューティング</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="443">
          <source>Here is a checklist of things to verify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">確認する項目のチェックリストを次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="444">
          <source>In Retail, on the <bpt id="p1">**</bpt>Retail shared parameters<ept id="p1">**</ept> page, verify that the correct client ID has been added to the <bpt id="p2">**</bpt>Relying parties<ept id="p2">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail の<bpt id="p1">**</bpt>小売共有パラメーター<ept id="p1">**</ept> ページで、適切なクライアント ID が<bpt id="p2">**</bpt>依存する関係者<ept id="p2">**</ept>クイック タブに追加されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="445">
          <source>Additionally, verify that the correct <ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph> entry has been added to the <bpt id="p1">**</bpt>Server resource IDs<ept id="p1">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、正しい <ph id="ph1">`https://retailstorescaleunit.retailserver.com`</ph> エントリが <bpt id="p1">**</bpt>サーバー リソース ID<ept id="p1">**</ept> クイック タブに追加されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="446">
          <source>In Retail, verify that every client ID that was generated for each retail store exists on the <bpt id="p1">**</bpt>Azure Active Directory applications<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail で、各小売店舗に生成されたすべてのクライアント ID が <bpt id="p1">**</bpt>Azure Active Directory アプリケーション<ept id="p1">**</ept> ページに存在することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="447">
          <source>In Retail, on the <bpt id="p1">**</bpt>Channel profile<ept id="p1">**</ept> page, verify that the URLs are correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail の<bpt id="p1">**</bpt>チャネル プロファイル<ept id="p1">**</ept> ページで、URL が正しいことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="448">
          <source>(In other words, verify that the computer name in each URL is correct, the URL is correctly formatted, and so on.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(つまり、各 URL のコンピュータ名が正しいこと、URL が正しく書式設定されていることなどを確認します。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="449">
          <source>In Retail, on the <bpt id="p1">**</bpt>Channel database<ept id="p1">**</ept> page, verify that full synchronization correctly occurred for the new channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail の<bpt id="p1">**</bpt>チャネル データベース<ept id="p1">**</ept> ページで、新しいチャネル データベースに完全同期が正しく発生したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="450">
          <source>Verify that the retail store is correctly configured to use the new channel database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいチャネル データベースを使用するように小売店舗が正しく構成されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="451">
          <source>If the Retail Store Scale Unit stops functioning after a period of time, there are two simple things to verify:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store Scale Unit が一定時間の後に停止した場合、確認すべき 2 つの簡単なことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="452">
          <source>Verify if the password policy requires the service account that was generated to change the password (password expiration).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パスワード ポリシーにより、パスワード (パスワードの有効期限) を変更するために生成されたサービス アカウントが求められているかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="453">
          <source>Re-run the same installer over the current installation (idempotent), which will update a service account's password or allow the user to update the selected account's password.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のインストール (非べき等) で同一のインストーラーを再実行します。これにより、サービス アカウントのパスワードが更新されるか、選択したアカウントのパスワードの更新が許可されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="454">
          <source>Uninstall Retail Store system</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Store システムのアンインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="455">
          <source>Use Control Panel in Microsoft Windows to uninstall Retail Store system.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Windows でコントロール パネルを使用して Retail Store システムをアンインストールします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="456">
          <source>Press the Windows logo key, and then enter <bpt id="p1">**</bpt>Control Panel<ept id="p1">**</ept> in the search box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Windows ロゴ キーを押し、検索ボックスに<bpt id="p1">**</bpt>コントロール パネル<ept id="p1">**</ept>と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="457">
          <source>In the search results, select <bpt id="p1">**</bpt>Control Panel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索結果で、<bpt id="p1">**</bpt>コントロール パネル<ept id="p1">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="458">
          <source>In Control Panel, select <bpt id="p1">**</bpt>Programs<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Uninstall a program<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コントロール パネルで、<bpt id="p1">**</bpt>プログラム<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>プログラムのアンインストール<ept id="p2">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="459">
          <source>In the <bpt id="p1">**</bpt>Programs and Features<ept id="p1">**</ept> window, select <bpt id="p2">**</bpt>Microsoft Dynamics 365 for Retail Store system<ept id="p2">**</ept>, and then, above the list of programs, select <bpt id="p3">**</bpt>Uninstall<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プログラムと機能<ept id="p1">**</ept>ウィンドウで、<bpt id="p2">**</bpt>Microsoft Dynamics 365 for Retail ストア システム<ept id="p2">**</ept>を選択してから、プログラムの一覧で<bpt id="p3">**</bpt>アンインストール<ept id="p3">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="460">
          <source>Wait for the uninstaller to finish removing the program.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アンインストールがプログラムの削除を完了するまで待ちます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>