<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="set-up-manage-images-retail-mpos.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>set-up-manage-images-retail-mpos.3cc4ad.c256569135a00ea98a5c059b9dd12a07a000ee6a.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c256569135a00ea98a5c059b9dd12a07a000ee6a</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>e2fb0846fcc6298050a0ec82c302e5eb5254e0b5</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/27/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\retail\set-up-manage-images-retail-mpos.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) のイメージの設定および管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事は、Retail Modern POS (MPOS) に表示されるさまざまなエンティティの設定および画像の管理に関連する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Set up and manage images for Retail Modern POS (MPOS)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) のイメージの設定および管理</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This article explains the steps that are involved in setting up and managing images for the various entities that appear in Retail Modern POS (MPOS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この記事は、Retail Modern POS (MPOS) に表示されるさまざまなエンティティの設定および画像の管理に関連する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Setting up the media base URL and defining media templates to configure the format for image URLs</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像 URL 形式をコンフィギュレーションするメディア ベースの URL およびメディアのテンプレートの定義を設定します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The images that appear in Retail Modern POS (MPOS) must be hosted externally, outside Microsoft Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Retail Modern POS (MPOS) に表示される画像は Microsoft Dynamics 365 for Retail の外部でホストされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Typically, they are hosted in a content management system, content delivery network (CDN), or media server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常は、コンテンツ管理システム、コンテンツ配信ネットワーク (CDN)、またはメディア サーバーでホストされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>MPOS then fetches and displays the images for the appropriate entities, such as products and catalogs, by accessing the target URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品およびカタログなど、適切なエンティティの画像は、MPOS がターゲット URL にアクセスし、フェッチして表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>To fetch these externally hosted images, MPOS requires the correct URL format for the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS が、これらの外部でホストされている画像をフェッチするには、画像の正しい URL 形式が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can configure the required URL format for the images by setting up the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> value in the channel profile and using the <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> functionality for each entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネル プロファイルの<bpt id="p1">**</bpt>メディア基準 URL<ept id="p1">**</ept>の値を設定、および各エンティティの<bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept>機能の設定により、画像の URL 形式をコンフィギュレーションできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can also overwrite the standard URL format for a subset of entities by using the <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept> functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、エンティティのサブセットに対して標準 URL 形式を <bpt id="p1">**</bpt>Excel で編集<ept id="p1">**</ept>機能を使用して上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>In the current version of Dynamics 365 for Retail, you can no longer set up the URL format by using the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute XML for MPOS in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail の現在のバージョンでは、エンティティの<bpt id="p2">**</bpt>既定<ept id="p2">**</ept>属性グループで MPOS の<bpt id="p1">**</bpt>画像<ept id="p1">**</ept>属性 XML を使用して URL フォーマットを設定することはできなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>If you're familiar with Microsoft Dynamics AX 2012 R3 and are now using the current version of Dynamics 365 for Retail, make sure that you always use the new <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality to set up images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 R3 を使い慣れていて、Dynamics 365 for Retail の現在のバージョンを使用している場合は、イメージの設定に、新しい<bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>機能を常に使用していることを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Don't use or modify the <bpt id="p1">**</bpt>Image<ept id="p1">**</ept> attribute in the <bpt id="p2">**</bpt>Default<ept id="p2">**</ept> attribute group for any entities, including products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品を含む、エンティティ グループの<bpt id="p2">**</bpt>既定<ept id="p2">**</ept>属性で、<bpt id="p1">**</bpt>画像<ept id="p1">**</ept>属性を使用、または変更しないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Changes that you make directly in the <bpt id="p1">**</bpt>Default<ept id="p1">**</ept> attribute group for images won't be reflected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像グループの<bpt id="p1">**</bpt>既定<ept id="p1">**</ept>属性での直接の変更は反映されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This option will be disabled in a future release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションは、将来のリリースでは無効になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>In the following procedures, images are set up for the Catalog entity as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順では、例として画像はカタログ エンティティに設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>These procedures will help guarantee that the correct image destination path is set implicitly for all catalog images that use a common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの手順で、正しい画像先のパスが共通のパスを使用するすべてのカタログ画像に対して暗黙的に設定されていることを保証するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>For example, if you've set up a media server or CDN externally, and want the images to appear in MPOS for a given store, the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> functionality helps you the set the path where MPOS can look up and retrieve the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、外部のメディアサーバーあるいは CDN を設定し、特定の店舗の MPOS に表示する画像を必要とする場合は、<bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>機能が、MPOS が検索したり、画像を取得できるパスを設定するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For this demo data example, the media server is deployed on the Retail Server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデモ データの例では、メディア サーバーは、Retail サーバーに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>However, you can have it anywhere outside Dynamics 365 for Retail.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Dynamics 365 for Retail の外部の任意の場所で配置できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Set up the media base URL for a channel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネルにメディアベース URL を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Open the Dynamics 365 for Retail HQ portal.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail HQ ポータルを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Channel setup<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Channel profiles<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売りとコマース<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>チャンネル設定<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>チャンネル プロファイル<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Navigation<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ナビゲーション<ept id="p1">](./media/channel-profile1.png)](./media/channel-profile1.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>In the channel profile that your store uses for MPOS, update the <bpt id="p1">**</bpt>Media base URL<ept id="p1">**</ept> field with the base URL of your media server or CDN.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">店舗で MPOS に使用するチャンネル プロファイルで、メディアサーバーあるいは CDN の基準 URLの<bpt id="p1">**</bpt>メディア基準 URL<ept id="p1">**</ept> フィールドを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>The base URL is the first part of the URL that is shared by all image folders of different entities.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ベース URL は別のエンティティのすべての画像のフォルダにより共有される URL の最初の部分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Channel profiles page<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></source><target logoport:matchpercent="79" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>チャネル プロファイル ページ<ept id="p1">](./media/channel-profile2.png)](./media/channel-profile2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Define the media template for an entity</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エンティティのメディアのテンプレートを定義します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>カタログ管理<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>カタログ画像<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, on the Action Pane, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログ画像<ept id="p1">**</ept>ページの、アクション ウィンドウで、<bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected by default.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>エンティティ<ept id="p2">**</ept>フィールドの、<bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>ダイアログボックスで、<bpt id="p3">**</bpt>カタログ<ept id="p3">**</ept>が既定でオンになっている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, enter the remaining path of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メディア パス<ept id="p1">**</ept>クイック タブで、画像の場所の残りのパスを入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>The media path supports <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> as a variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メディア パスは、<bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> を変数としてサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>For example, for the demo data, you can create a <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> folder for all catalog images under the media base URL for your media server (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デモ データについては、メディア サーバーのメディア基準 URL 以下のすべてのカタログ画像に<bpt id="p1">**</bpt>カタログ<ept id="p1">**</ept> フォルダを作成できます (<ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`</ph>)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>You can then have a folder for each language, such as en-US or fr-FR, and copy the appropriate images under each folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各言語のフォルダが、en-US または fr-FR などである場合、各フォルダで適切な画像をコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>If you don't have different images for the various languages, you can omit the <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> variable from your folder structure and point directly to the Catalogs folder that contains the catalog images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな言語のための、さまざまな画像を所有していない場合、フォルダ構造から <bpt id="p1">**</bpt>LanguageID<ept id="p1">**</ept> 変数を省略でき、カタログ画像を含むカタログフォルダを直接設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>The current version of Dynamics 365 for Retail supports the <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> token for Catalog, Product, and Category entities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail の現在のバージョンでは、カタログ、製品、およびカテゴリ エンティティの <bpt id="p1">**</bpt>{LanguageId}<ept id="p1">**</ept> トークンがサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>(The <bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> token isn't supported for Customer and Worker entities, according to the existing standard that has been effective since Microsoft Dynamics AX 6.x.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(<bpt id="p1">**</bpt>{LanguageID}<ept id="p1">**</ept> トークンは、Microsoft Dynamics AX 6.x. 以降有効な既存の標準に従って、顧客および作業者の場合はサポートされません)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>For images, the file name format is hard-coded to the catalog name and can't be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像では、ファイル名の形式は、カタログ名にハードコーディングされ、変更することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Therefore, rename your images so that they have appropriate catalog names, to help guarantee that MPOS handles them correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">従って、MPOS がそれらを正しく処理できるようにするため、適切なカタログ名となるように画像の名前を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>In the <bpt id="p1">**</bpt>File Extension<ept id="p1">**</ept> field, select the expected file name extension, depending on the type of images that you have.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル拡張子<ept id="p1">**</ept>フィールドで、画像のタイプに基いて必要なファイル拡張子を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>For example, for the demo data, the catalog images are set to the .jpg extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デモ データに対しては、カタログの画像に .jpg の拡張子が設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>(The image files are also renamed so that they have catalog names.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(画像ファイルは、カタログ名を持つように名前を変更されます)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>To validate that the media template for images has been saved correctly, on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept> again.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像のメディアのテンプレートが、<bpt id="p1">**</bpt>カタログ画像<ept id="p1">**</ept>ページで、適切に保存されていることを確認するには、<bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept>をもう一度クリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>To validate the template without closing the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, you can use the <bpt id="p2">**</bpt>Generate Image URLs for Excel<ept id="p2">**</ept> FastTab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>ダイアログ ボックスを閉めないでテンプレートを検証するには、<bpt id="p2">**</bpt>Excel 用の画像 URL の生成<ept id="p2">**</ept>クイック タブを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Check the appearance of the image URL, and verify that the URL complies with the template standard that was mentioned earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像 URL の外観を確認し、URL が上記のテンプレートの標準に準拠していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box has now set the image path implicitly for all catalog images that use this common URL path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>ダイアログ ボックスにより、この URL 共通のパスを使用するすべてのカタログ画像に画像のパスが暗黙的に配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>This URL path applies to all catalog images unless they are overwritten.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上書きされない場合、この URL パスは、すべてのカタログ画像に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The first part of the image path is taken from the media base URL that you defined in the channel profile.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像のパスの最初の部分は、チャンネルのプロファイルで定義したメディアの基準 URL から取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The remaining part of the path is taken from the path that you defined in the media template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">パスに関する残りの部分は、メディアのテンプレートで定義したパスから取得されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The two parts are concatenated to provide the full URL of the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像の場所の URL 全体を提供するために 2 つの部分が連結されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>For example, a catalog in the demo data is named Fabrikam Base Catalog.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、デモ データのカタログでは、Fabrikam の基本カタログが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Therefore, the image name must be Fabrikam Base Catalog.jpg so that it uses the catalog name and the .jpg file name extension that is configured in the template.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、テンプレートでコンフィギュレーションされているカタログ名、および .jpg ファイル名拡張子を使用するため、画像の名前は Catalog.jpg Fabrikam である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>In this case, after concatenation, the URL will be <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、連結後の URL は <ph id="ph1">`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`</ph> になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Run the synchronization jobs to push the new template to the channel database, so that MPOS can use the template to access the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージにアクセスする場合に MPOS がテンプレートを使用するように、チャンネルのデータベースに新しいテンプレートをプッシュするため、同期ジョブを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To update the media template for catalog images on the channel side, be sure to run <bpt id="p1">**</bpt>Catalog Job 1150<ept id="p1">**</ept> from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">チャネル側のカタログ画像のメディア テンプレートを更新するには、<bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept>から<bpt id="p1">**</bpt>カタログ ジョブ 1150<ept id="p1">**</ept> を実行してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>メディア テンプレートの定義ダイアログ ボックス<ept id="p1">](./media/catalog1.png)](./media/catalog1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Previewing an image from the entity level</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">エンティティ レベルからの画像のプレビュー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>From the page for the entity item in HQ, you can preview the image that uses the image URL that is derived from the media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">HQ のエンティティの品目のページで、メディアのテンプレートから派生した画像 URL を使用する画像をプレビューできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>For this example, go to the appropriate catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、適切なカタログに移動し、アクション ウィンドウで、<bpt id="p1">**</bpt>メディア<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>画像<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Use the drop-down list to select different stores that might have different channel profiles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チャンネルのさまざまなプロファイルがある異なる店舗を選択する場合でも、ドロップダウン リストを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To edit or remove the implicit media template, you must return to the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box for the <bpt id="p2">**</bpt>Catalog images<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗黙的なメディア テンプレートを編集、または削除するには、<bpt id="p2">**</bpt>カタログ画像<ept id="p2">**</ept>ページの<bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>ダイアログ ボックスに戻る必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>You can use the <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Remove<ept id="p2">**</ept> buttons to manually change the path that is based on the implicit template and used for a specific image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">暗黙的なテンプレートに基づき、特定の画像に使用されるパスを手動で変更するために、<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>および<bpt id="p2">**</bpt>削除<ept id="p2">**</ept>ボタンを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>For more information, see the <bpt id="p1">[</bpt>Overwriting the media template for entity items<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept> section later in this article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、この記事で後述する<bpt id="p1">[</bpt>エンティティ アイテムのメディア テンプレートの上書き<ept id="p1">](#overwriting-the-media-template-for-entity-items)</ept>セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>After you've finished previewing an image and making any changes that you require, start the MPOS instance for the appropriate store, and see whether the catalog images are shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">画像をプレビューし、必要な変更を加えることを完了したら、適切な店舗の MPOS のインスタンスを起動し、カタログの画像を表示するかどうかを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Images dialog box<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></source><target logoport:matchpercent="68" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ダイアログ ボックスの画像<ept id="p1">](./media/catalog4.png)](./media/catalog4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>You can use the same procedure for all the five entities that are supported: Worker, Customer, Catalog, Category, and Products.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">サポートされている 5 つのエンティティ、作業者、顧客、カタログ、カテゴリ、および製品で同じ手順を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>"Catalog Products" (products that are set at the catalog level) and "Channel Products" (products that are set at the channel level) use the media template that is set for the Products entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「カタログ製品」 (カタログ レベルで設定された製品) および「チャンネル製品」 (チャンネル レベルで設定された製品) は、製品 エンティティで設定されたメディア テンプレートを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>For the Products media template, you can select the number of product images to show per product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品のメディア テンプレートでは、製品ごとに表示する製品画像の数を選択できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>You can also set the default image for a given product.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、特定の製品に既定の画像を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>In this way, you can prevent blank images in MPOS and help to control which image is used as the default image for a product item.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、MPOS の空白の画像をなくしたり、画像を製品品目の既定の画像として使用するかどうかを制御できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>In the following example, each product has five images, and the first image is set as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、各製品に 5 つの画像があり、最初の画像は、既定の画像として設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Variant products are treated the same way as master products.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バリアント製品はマスターの製品と同じ方法で処理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>The file name of the image file should be based on the product number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ ファイルのファイル名は製品番号に基づく必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Some characters are also escaped while the file name is generated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル名の生成中、一部の文字がエスケープします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Therefore, it's a good to verify the file name by using the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> section.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">したがって、<bpt id="p1">**</bpt>Excel 用の画像 URL の生成<ept id="p1">**</ept>セクションを使用してファイル名を確認することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Define media template dialog box<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></source><target logoport:matchpercent="100" state="translated" state-qualifier="exact-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>メディア テンプレートの定義ダイアログ ボックス<ept id="p1">](./media/prods.png)](./media/prods.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Synchronization jobs to send a media template to the channel side</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">チャンネル側にメディアのテンプレートを送信するジョブを同期</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>For all the five supported entities (Worker, Customer, Catalog, Category, and Products), whenever you update the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog to set up an image, make sure that you run the Catalog job (1150) from <bpt id="p2">**</bpt>Retail IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>Distribution schedule<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サポートされている 5 つのエンティティすべて (作業者、顧客、カタログ、カテゴリ、および製品) で、画像を設定するために <bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept> ダイアログを更新する場合は常に、<bpt id="p2">**</bpt>小売 IT<ept id="p2">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p3">**</bpt>配送スケジュール<ept id="p3">**</ept> から、カタログジョブ (1150) の実行を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>This job will enable the updated media template to be synced to the channel and used by MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このジョブは、チャンネルに同期された更新されたメディア テンプレートを有効にし、MPOS で使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Run the Catalog job (1150) after you make any of the following changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のような変更を行った後、カタログジョブ (1150) を実行します:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>You update the Catalog image media template from <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログ画像<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept> からカタログ画像メディア テンプレートを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>You update the Employee image media template from <bpt id="p1">**</bpt>Employee images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>従業員の画像<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept> から従業員の画像メディア テンプレートを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>You update the Customer image media template from <bpt id="p1">**</bpt>Customer image<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客画像<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept> から顧客画像メディア テンプレートを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>You update the Product image media template from <bpt id="p1">**</bpt>Product images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品画像<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept> から製品画像メディア テンプレートを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>You update the Category image media template from <bpt id="p1">**</bpt>Category images<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カテゴリ画像<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept> からカテゴリ画像メディア テンプレートを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>You must also publish the channel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、チャンネルを公開する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Overwriting the media template for entity items</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ品目のメディア テンプレートを上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>As you learned in the previous section, the media template for a given entity supports only one common path.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションで学んだように、特定のエンティティのメディア テンプレートは、一つの共通のパスのみサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>This path is based on the media base URL that is configured and the media path that is defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このパスは、コンフィギュレーションされた基準 URL、および定義されたメディアのパスに基づきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>However, in many cases, a retailer wants to be able to use images from different sources for a subset of items in an entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、多くの場合、小売業者はエンティティの品目のサブセットに対してさまざまなソースから画像が使用できることを希望します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>For example, a store uses the self-hosted media server for one set of catalog images but uses CDN URLs for another set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、店舗は、自己ホストのメディア サーバーを 1 つのセットのカタログ画像に使用しますが、別のセットには CDN の URL を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>To overwrite image URLs that are based on a media template for entity images at the entity level, you can use the Edit in Excel and Manual edit functionality from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ レベルのエンティティ 画像のメディア テンプレートに基づく画像 URL を上書きするには、<bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept>ページの Excel および手動で編集機能を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Overwrite by using Edit in Excel</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で編集を使用して上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Click <bpt id="p1">**</bpt>Retail<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Catalog management<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Catalog images<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>小売<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>カタログ管理<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>カタログ画像<ept id="p3">**</ept> の順にクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>On the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> page, click <bpt id="p2">**</bpt>Define media template<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログ画像<ept id="p1">**</ept>ページで、<bpt id="p2">**</bpt>メディア テンプレートの定義<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>In the <bpt id="p1">**</bpt>Define media template<ept id="p1">**</ept> dialog box, in the <bpt id="p2">**</bpt>Entity<ept id="p2">**</ept> field, <bpt id="p3">**</bpt>Catalog<ept id="p3">**</ept> should be selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>エンティティ<ept id="p2">**</ept>フィールドの、<bpt id="p1">**</bpt>メディア テンプレートの定義<ept id="p1">**</ept>ダイアログボックスで、<bpt id="p3">**</bpt>カタログ<ept id="p3">**</ept>がオンになっている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>On the <bpt id="p1">**</bpt>Media path<ept id="p1">**</ept> FastTab, notice the image location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メディア パス<ept id="p1">**</ept>クイック タブで、画像の場所を通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>On the <bpt id="p1">**</bpt>Generate Image URLs for Excel<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Generate<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Excel 用の画像 URL の生成<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>生成<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Whenever the media template is changed, you must click <bpt id="p1">**</bpt>Generate<ept id="p1">**</ept> before you can use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">メディア テンプレートが変更された場合、Excel で編集機能を使用する前に、<bpt id="p1">**</bpt>生成<ept id="p1">**</ept>をクリックする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Excel 用の画像 URL の生成クイック タブ<ept id="p1">](./media/excel1.jpg)](./media/excel1.jpg)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>You now see a preview of the image URLs that were generated based on the last saved media template.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">最後に保存したメディア テンプレートに基づいて生成された、画像 URL がプレビュー表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Generate Image URLs for Excel FastTab after Generate is selected<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>生成が選択された後の Excel 用の画像 URL の生成クイック タブ<ept id="p1">](./media/excel2.png)](./media/excel2.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>The URLs that are generated for Excel use the path and conventions of the media template that is defined.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">Excel 用に生成された URL は、定義されているメディア テンプレートのパスと方式を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>These conventions include the conventions for file names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの方式には、ファイル名の方式も含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>The expectation is that you've set up the physical images outside Dynamics 365 for Retail, and the images can be retrieved from the URLs that are derived from the media template that you defined earlier.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics 365 for Retail の外部で現物画像を設定することが期待されており、画像は、先に定義したメディア テンプレートから派生する URL から取得することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>You can overwrite these derived URLs by using the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で編集の機能を使用すると、これらの派生 URL を上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Click <bpt id="p1">**</bpt>Edit in Excel<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Excel で編集<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>After the Microsoft Excel worksheet is opened, click <bpt id="p1">**</bpt>Enable edit<ept id="p1">**</ept> when you're prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Excel ワークシートを開き、メッセージが表示されたら、<bpt id="p1">**</bpt>編集の有効化<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>When you're prompted, click <bpt id="p1">**</bpt>Trust this add-in<ept id="p1">**</ept> in the right pane, and wait for the add-in to complete the installation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メッセージが表示されたら、<bpt id="p1">**</bpt>このアドインを信頼します<ept id="p1">**</ept>を右ウィンドウでクリックし、インストールを完了するためにアドインを待機します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Trust this add-in<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>このアドインを信頼します<ept id="p1">](./media/excel4.jpg)](./media/excel4.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you're prompted to sign in, enter the credentials that you used to sign in to HQ.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインするメッセージが表示されると、HQ のサインインに使用する資格情報を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Sign-in prompt<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>サインイン プロンプト<ept id="p1">](./media/excel5.png)](./media/excel5.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>After you sign in, you should be able to see the list of image URLs for the various catalog entries.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインした後、さまざまなカタログ エントリについて画像 URL の一覧を確認できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>You edit, add, and remove the image URLs for various entity items.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまなエンティティ品目の画像 URL を編集、追加、および削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>For all entities except Products, you can overwrite the image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品を除くすべてのエンティティに、画像 URL を上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Modify the existing image URL, so that it uses the new destination URL of the image, and update the file name with the new file name for the image file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像の新しい配送先 URL を使用し、ファイル名を画像ファイルの新しいファイル名に更新するために、既存の画像 URL を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>The file name must be unique to help guarantee that the record is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコードが一意であることを保証するために、ファイル名は一意である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Overwrite the image URLs in Excel<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Excel で画像 URL を上書き<ept id="p1">](./media/excel6.jpg)](./media/excel6.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>When you overwrite image URLs for Products entities by using the Edit in Excel functionality or the entity item page, MPOS always shows all the media template image URLs together with the overwritten image URLs.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で編集の機能またはエンティティ品目ページを使用して製品エンティティの画像 URL を上書きすると、MPOS は上書きされた画像 URL とともに、すべてのメディア テンプレートの画像 URL を常に表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>After you've finished making your changes, click <bpt id="p1">**</bpt>Publish in Excel<ept id="p1">**</ept> to create a new explicit association entry.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更を加えることを完了した後、<bpt id="p1">**</bpt>Excel で公開<ept id="p1">**</ept>をクリックすると、新しい明示的 アソシエーション エントリが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Return to HQ, and click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">HQ に戻り、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Run the appropriate synchronization jobs for the entity, and check the preview on the entity page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティの適切な同期ジョブを実行し、エンティティ ページ、あるいは MPOS のプレビューを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Creating new records</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい記録の作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>You can create new records in Excel.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel の新しいレコードを作成できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>However, make sure that you provide the correct information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、正しい情報を入力したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>For example, to create a new entry for a catalog, make sure that the catalog ID and catalog name are correct, and also provide a unique file name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、カタログの新しいエントリを作成する場合、カタログ ID、およびカタログの名前が正しいことを確認し、一意のファイル名を入力してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>The unique file name is very important, because the uniqueness of records in Excel is validated during publishing.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">固有のファイル名は、Excel のレコードの独自性が発行中に検証されるために非常に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>First copy the details from the catalog that you want to create a new record for, and copy the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、新しいレコードを作成するカタログから詳細をコピーし、レコードをコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>You just have to update the file name and URL, because the rest of the information will be same.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の情報が同じであるため、ファイル名、URL を更新する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To create new records for Product entity items, you use the same basic procedure.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品エンティティの品目に新しいレコードを作成するには、同じ基本的な手順を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>From the Excel worksheet, copy an existing record for the product that you to create a new record for, and then replace the image URL and filename.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel ワークシートから、新しいレコードを作成する製品に既存のレコードをコピーし、画像 URL およびファイル名を置き換えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Make sure that the file name is unique.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイル名は一意であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Deleting an existing record</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のレコードの削除</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Only the overwritten image URL records can be deleted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上書きした画像 URL のレコードのみ削除できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>After an image is deleted and synchronization is completed, the image will no longer appear on the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page or in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像が削除され、同期が完了した後、画像は<bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept>ページ、または MPOS に表示されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Image URL records that are derived from the media template can't be deleted, because these records are always derived from the media template every time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">毎回これらのレコードはメディア テンプレートから常に派生するため、メディア テンプレートから派生した画像 URL レコードは削除できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Overwrite from the entity-level Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンティティ レベル プレビュー ページを上書き</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>For all entities except Products, you can overwrite the image URL for a given entity item at the entity item level from the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品を除くすべてのエンティティは、<bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept>ページからのエンティティ レベルで、一部のエンティティ品目の画像 URL を上書きできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>For Products, you can use the "Catalog Products" entity page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">製品については、「カタログ製品」エンティティ ページを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This example shows how to overwrite a catalog image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、カタログ画像を上書きする方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Click <bpt id="p1">**</bpt>Catalogs<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Media<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Images<ept id="p3">**</ept>, and select the catalog image to update.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>カタログ<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>メディア<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>画像<ept id="p3">**</ept> をクリックし、更新するカタログ画像を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and enter the image URL to overwrite the media template URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックし、メディア テンプレート URL に上書きする画像 URL を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>If you want this image to be shown in MPOS for the catalog, you can set it as the default image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この画像を MPOS でカタログに表示する場合、既定の画像として設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>The image URL is updated for this catalog image, and a preview is shown.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">画像 URL は、このカタログ画像に更新され、プレビューが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>URL updated in the New image dialog box<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新しい画像ダイアログ ボックスで更新された URL<ept id="p1">](./media/preview3.png)](./media/preview3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can also see the image preview for all overwritten image URLs on the <bpt id="p1">**</bpt>Catalog images<ept id="p1">**</ept> gallery page.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">すべてを上書きした画像 URL は、画像のプレビューを<bpt id="p1">**</bpt>カタログ画像<ept id="p1">**</ept>ギャラリー ページで表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Catalog images gallery page<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></source><target logoport:matchpercent="0" state="translated"><bpt id="p1">[</bpt><ph id="ph1">![</ph>カタログ画像ギャラリー ページ<ept id="p1">](./media/preview-4.png)](./media/preview-4.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Currently, the gallery doesn't show image previews for media template image URLs.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">現在のところ、ギャラリーはメディア テンプレートの画像 URL の画像のプレビューを表示しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>For Catalog, Worker, Customer, and Category entities, if the user explicitly provides a URL through this page, we recommend that you indicate which image is the default image, because Retail Server clients show only one image per Catalog, Customer, Worker, and Category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログ、作業者、顧客、およびカテゴリエンティティに、ユーザーがこのページで明示的に URL を指定すると、Retail サーバーのクライアントがカタログ、顧客、作業者、およびカテゴリごとに一つの画像のみを参照するため、既定の画像を指定することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>If the user doesn't specify a default image, the system determines the default image and send it to the Retail service caller (MPOS or Ecommerce).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ユーザーが既定の画像を指定しないと、システムは既定の画像を確認し、小売サービスの呼び出し元に送信します (MPOS または e コマース)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>Overwrite the image URL for catalog product images from the Preview page</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プレビュー ページからカタログ製品画像の画像 URL を上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>To overwrite image URLs for catalog product images, you must use the <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログ製品画像の画像 URL を上書きするために、<bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept>ページを使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>You can't use the Edit in Excel functionality.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Excel で編集の機能を使用できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>To overwrite product images at a catalog level, select a catalog, and then select the product to overwrite the image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログのレベルで製品画像を上書きするには、カタログを選択し、画像を上書きする製品を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>Click <bpt id="p1">**</bpt>Attributes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>属性<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>On the next page, select <bpt id="p1">**</bpt>Image<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Edit<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のページで、<bpt id="p1">**</bpt>画像<ept id="p1">**</ept>を選択し、<bpt id="p2">**</bpt>編集<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>The <bpt id="p1">**</bpt>Preview<ept id="p1">**</ept> page opens as a slider dialog box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プレビュー<ept id="p1">**</ept> ページがスライダーのダイアログ ボックスとして開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept>, and overwrite the image URL with a new URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックし、画像 URL を新しい URL で上書きします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>You now see the preview of the new image and can set it as the default image.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">これで、新しい画像をプレビュー表示し、既定の画像として設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Image preview in the New image dialog box<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></source><target logoport:matchpercent="75" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>新しい画像ダイアログ ボックスの画像プレビュー<ept id="p1">](./media/cat3.png)](./media/cat3.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>After category image association, you must publish the channel and run the Channel job to help guarantee that the changes are published to the channel database.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">カテゴリ画像のアソシエーションの後、チャネルを発行し、チャネル データベースへの変更を公開することを保証するチャネル ジョブを実行する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>Setting up images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS のオフライン モードで表示されるイメージの設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>MPOS can run in Online mode (when MPOS connected to Retail Server) or Offline mode (when there is no Retail Server or network connectivity, and transactions are stored in a local offline database).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS はオンライン モード (MPOS が Retail サーバーに接続される時)、またはオフライン モード (Retail サーバー、またはネットワーク接続がない、およびトランザクションがローカル オフライン データベースに保存されている時) で実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source>When MPOS runs in Offline mode, it can't get images from the external image server to display from Retail Server, because Retail Server connectivity has been lost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS をオフライン モードで実行すると、Retail サーバー接続が失われるため、外部ファイル サーバーから、Retail サーバーからの表示のための画像を取得することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>However, you can still set up images so that they are shown when MPOS runs in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、MPOS がオフライン モードの実行時に表示するように、まだ画像を設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>Set up product images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS のオフライン モードで表示される製品画像の設定</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source>The product images that must be used in Offline mode can be set up by uploading the required physical image into the base product image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードで使用する製品画像は、基本製品画像に必要な現物画像をアップロードすることで設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Click <bpt id="p1">**</bpt>Product information management<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Products<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>Products<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品情報管理<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>製品<ept id="p2">**</ept> <ph id="ph2">&amp;gt;</ph> <bpt id="p3">**</bpt>製品<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>Select the product to set the offline image for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン画像に設定する製品を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>Click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and then click the arrow in the right corner to show the right pane.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>編集<ept id="p1">**</ept>をクリックし、右ウィンドウを表示するために角の右矢印をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source>On the <bpt id="p1">**</bpt>Product image<ept id="p1">**</ept> FastTab, click <bpt id="p2">**</bpt>Change image<ept id="p2">**</ept>, and upload the physical image to use for the selected product in Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>製品画像<ept id="p1">**</ept>クイック タブで、<bpt id="p2">**</bpt>イメージの変更<ept id="p2">**</ept>をクリックし、オフライン モードで選択した製品に使用する、現物画像をアップロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Save and close the page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページを保存して閉じる。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>While MPOS is in Online mode, run the Catalog job in HQ, to make sure that the data is sent at least one time to the offline database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">MPOS がオンライン モードの間に、データがオフライン データベースに 1 回以上の送信を行うかどうか確認するため、HQ でカタログジョブを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Put MPOS into Offline mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードに MPOS を挿入します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>You should see the image that you uploaded for the specific product in HQ.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">HQ の特定の製品にアップロードする画像を確認する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Product image in Offline mode<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt><ph id="ph1">![</ph>オフライン モードの製品画像<ept id="p1">](./media/offline1.png)](./media/offline1.png)</ept></target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>Set up catalog, category, employee, and customer images to appear in Offline mode for MPOS</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">MPOS のオフライン モードで表示するカタログ、カテゴリ、従業員、および顧客の画像を設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>The catalog, category, employee, and customer images that must be used in Offline mode can be set up by adding the required image's destination link to the gallery and setting the image as the default image for the selected entity.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オフライン モードで使用するカタログ、カテゴリ、従業員、および顧客の画像は、必要な画像のリンク先をギャラリーに追加し、選択したエンティティの既定の画像として画像を設定することで設定できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Go to the catalog, and then, on the Action Pane, click <bpt id="p1">**</bpt>Media<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>Images<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログに移動してから、アクション ウィンドウで、<bpt id="p1">**</bpt>メディア<ept id="p1">**</ept> <ph id="ph1">&amp;gt;</ph> <bpt id="p2">**</bpt>画像<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source>Follow the steps in the <bpt id="p1">[</bpt>Overwrite from the entity-level Preview page<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept> section to add the external image URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部 URL 画像を追加するには、<bpt id="p1">[</bpt>エンティティ レベル プレビュー ページを上書き<ept id="p1">](#overwrite-from-the-entity-level-preview-page)</ept>セクションの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Mark this image as the default image for the catalog by selecting the check box against the Image listed in the grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">チェック ボックスをオンにして、グリッドに表示する画像に対し、この画像をカタログの既定の画像としてマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source>Run the Catalog job.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カタログジョブを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>This image will now be used as the Offline image for that catalog in MPOS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この画像は MPOS でカタログのオフラインの画像としてすぐに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source>Follow a similar process for other entities, such as Category, Employee, and Customer.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">カテゴリ、従業員、および顧客など、他のエンティティの類似したプロセスに従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Offline image<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></source><target logoport:matchpercent="70" state="translated" state-qualifier="fuzzy-match"><bpt id="p1">[</bpt><ph id="ph1">![</ph>オフライン画像<ept id="p1">](./media/offline2.png)](./media/offline2.png)</ept></target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>