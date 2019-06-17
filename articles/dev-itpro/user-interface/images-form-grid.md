<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="images-form-grid.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>images-form-grid.9158c5.43257e6ed0c8a7ca74a7cddc685e6113352a1c03.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>43257e6ed0c8a7ca74a7cddc685e6113352a1c03</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\images-form-grid.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Images on a page or in a grid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ上またはグリッド内の画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes the steps for displaying images on a page or in a grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、画像をページまたはグリッドに表示する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>The topic also provides background about some of the ways that images can be used, and the APIs that are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Images on a page or in a grid</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ上またはグリッド内の画像</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>This topic describes the steps for displaying images on a page or in a grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、画像をページまたはグリッドに表示する手順について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>The topic also provides background about some of the ways that images can be used, and the APIs that are used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、イメージの使用方法のいくつかについての背景と、使用される API についても説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> For accessibility, when you use an image to indicate status or show data, the image must be accompanied by a tooltip, enhanced preview, label, or other textual representation that describes the value or status that the image represents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> アクセシビリティのために、画像を使用して状態を示したり、データを表示するときには、その画像が表す値または状態を説明するツールヒント、拡張プレビュー、ラベル、またはその他のテキスト形式表記が添付されていなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Unlike Microsoft Dynamics AX 2012, Microsoft Dynamics 365 for Finance and Operations doesn’t use embedded resources for images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 とは異なり、Microsoft Dynamics 365 for Finance and Operations ではイメージに埋め込みリソースを使用しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Instead, it uses lightweight symbols.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、ライトウェイト記号を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>The coding pattern has changed slightly to support the new image control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいイメージ コントロールをサポートするために、コーディング パターンがわずかに変更されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>For ImageList uses, the runtime accepts the old <bpt id="p1">**</bpt>ImageID<ept id="p1">**</ept> value and maps it to a symbol, so that existing code continues to work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ImageList 使用により、ランタイムは古い <bpt id="p1">**</bpt>ImageID<ept id="p1">**</ept> 値を受け入れて記号にマップし、既存のコードは引き続き動作できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> In some cases, there is no image even after runtime mapping, and this behavior is intentional.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> 場合によっては、ランタイム マッピング後もイメージが存在せず、この動作は意図的です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>AX 2012 displays images in a grid column to indicate status.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 は、ステータスを示すためにグリッド列で画像を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>These images were sometimes retrieved from embedded resources that are no longer available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの画像は、利用できなくなった埋め込みリソースから取得されることがありました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>AX 2012 offers the following storage options for images:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012は、画像の次の記憶域オプションが用意されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>An embedded resource where images are offered as part of the kernel itself</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像がカーネル自体の一部として提供される埋め込みリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>An Application Object Server (AOS) resource where developers or independent software vendors (ISVs) can add their own image resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Object Server (AOS) リソースは開発者または独立系ソフトウェア ベンダー (ISV) が独自のイメージ リソースを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>A file location where developers or ISVs can load images at run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に開発者または ISV が画像を読み込むファイルの場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>A database field that is stored as a bitmap</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビットマップとして保存されているデータベース フィールド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Finance and Operations offers the following storage options for images:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations は、画像用に次の記憶域オプションを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>An AOS resource where developers or ISVs can add their own image resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS リソースは開発者や ISV が独自のイメージ リソースを追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>A URL location where developers or ISVs can load images at run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に開発者または ISVs が画像を読み込む URL の場所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>A database field that is stored as a container.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーとして保存されているデータベース フィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>A symbol font, where images are rendered by name from the font</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像がフォントの名前でレンダリングされる記号フォント</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>In Finance and Operations, embedded resources (kernel resources) have been retired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Finance and Operations では、埋め込みリソース (カーネル リソース) が破棄されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Images that are stored as AOS resources allow for the use of an image that isn't categorized as user data, and can be used with your application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AOS リソースとして保存されるイメージは、ユーザー データに分類されていないイメージを使用でき、お使いのアプリケーションと共に使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> If there are legacy embedded resource images that UX has approved for use, those embedded images can be manually transferred to an AOS resource and used.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> UX が使用を承認したレガシ埋め込みリソース イメージがある場合、それらの埋め込みイメージを手動で AOS リソースに転送して使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>A typical web application maintains a collection of images on an Internet Information Services (IIS) server and just provides a URL to the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般的な Web アプリケーションは、Internet Information Services (IIS) サーバー上の画像のコレクションを管理し、画像の URL を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Although this approach is supported, we don't expect that it will be used very much.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法はサポートされていますが、非常に多く使用されるとは考えていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Instead, we expect that the symbol font will be used as an image source.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、記号フォントをイメージ ソースとして使用することを期待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Of course, application logic will store an image in a database to allow for strong employee photos, product images, and so on, and this approach is a first-class experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もちろん、アプリケーション ロジックは、許可された厳密な従業員の写真、製品画像など、データベースに画像を保管し、この方法は、ファースト クラスの経験です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>A symbol font is the most performant and scalable image format.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記号フォントは、最もパフォーマンスが高く、スケーラブルな画像形式です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>We expect that characters from the symbol font will be used for most application use cases (grid row by row status, button images, and so on).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのアプリケーションのユース ケース (グリッドの行ごとのステータスやボタンの画像など) に記号フォントの文字の使用を考えています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>For the list of symbols that are available in the symbol font, see <bpt id="p1">[</bpt>Symbol font<ept id="p1">](symbol-font.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">記号フォントで利用できる記号の一覧については、<bpt id="p1">[</bpt>記号フォント<ept id="p1">](symbol-font.md)</ept> を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Image type: Symbol</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージの種類: シンボル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Pros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">短所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Usually, the symbol font is the smallest payload to send to the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、記号フォントは、クライアントに送られる最小のペイロードです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>You can easily customize the images by using Cascading Style Sheets (CSS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスケード スタイル シート (CSS) を使用することにより、画像を簡単にカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The symbol font should already be cached on the user's computer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シンボル フォントは、すでにユーザーのコンピューターにキャッシュされている必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Therefore, no extra bandwidth is used, and there are no additional network requests that might slow down page loads.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、余分な帯域幅が使用されず、追加のネットワーク要求がないためにページの読み込みが遅くなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Colors can be controlled by themes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">色はテーマで制御できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The images are automatically scaled on high-DPI displays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージは高 DPI ディスプレイで自動的に拡大/縮小されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>A limited number of framework-defined symbols is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">限られた数のフレームワーク定義の記号を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Design time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Image location:<ept id="p1">&lt;/strong&gt;</ept> Symbol <bpt id="p2">&lt;strong&gt;</bpt>Typical image:<ept id="p2">&lt;/strong&gt;</ept> <ph id="ph1">&amp;quot;</ph>Person<ph id="ph2">&amp;quot;</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>イメージの場所:<ept id="p1">&lt;/strong&gt;</ept> 記号<bpt id="p2">&lt;strong&gt;</bpt>一般的な画像:<ept id="p2">&lt;/strong&gt;</ept> <ph id="ph1">&amp;quot;</ph>個人<ph id="ph2">&amp;quot;</ph></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Sometimes, you don't have an image for a particular record in a grid, but you don't want an empty space where the image should be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The following example shows how you can use a display method to check for an image value, and then substitute a placeholder image instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、表示メソッドを使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Image type: AOT Resource</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージの種類: AOT リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Pros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">短所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In addition to the pros of using URL images (see the next section), AOT resources are modeled and managed by the development tools.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL イメージ (次のセクションを参照) を使用するプロに加えて、AOT リソースが開発ツールでモデル化および管理されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>A   limited number of framework-defined images is available.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">限られた数のフレームワーク定義の画像が使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>Design time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>| You just create a new resource and then save the image into the Application Object Tree (AOT) resource.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">| 新しいリソースを作成してからイメージをアプリケーション オブジェクト ツリー (AOT) リソースに保存するだけです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>When you model your image control on a page, you specify the resource name, not the image name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページ上でイメージ コントロールをモデル化するときは、イメージ名ではなく、リソース名を指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>This approach is typically used for legacy images (icons) that don’t have equivalents in the symbol font.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、通常、シンボル フォントに同等のものがないレガシ イメージ (アイコン) に使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Image location:<ept id="p1">&lt;/strong&gt;</ept> AOTResource <bpt id="p2">&lt;strong&gt;</bpt>Typical image:<ept id="p2">&lt;/strong&gt;</ept> <ph id="ph1">&amp;quot;</ph>ResourceMicrosoft Dynamics AX<ph id="ph2">&amp;quot;</ph> (a .jpg is added to resources) |</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>イメージの場所:<ept id="p1">&lt;/strong&gt;</ept> AOTResource <bpt id="p2">&lt;strong&gt;</bpt>一般的な画像:<ept id="p2">&lt;/strong&gt;</ept> <ph id="ph1">&amp;quot;</ph>ResourceMicrosoft Dynamics AX<ph id="ph2">&amp;quot;</ph> (.jpg をリソースに追加) |</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>Image type: URL Image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージの種類: URL イメージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Pros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">短所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>This approach provides an easy way to reference any image anywhere on web.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、web 上の任意の画像を参照する簡単な方法を説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This approach supports full-color images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、フル カラー画像をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The web browser can cache the image, based on the settings of the server that hosts the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Web ブラウザーは、画像をホストするサーバーの設定に基づいて、画像をキャッシュできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The transfer size isn’t as small as it is for symbols, but it's reasonable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">転送サイズはシンボルほど小さいわけではありませんが、妥当です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>The URL is sent as a string for each control that uses the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL は、画像を使用する各コントロールの文字列として送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The browser then downloads the image from the URL, and from that point, standard browser caching rules apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブラウザーは URL からイメージをダウンロードし、その時点から標準のブラウザー キャッシュ ルールが適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>You can’t easily theme the images by using CSS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSS を使用してもイメージのテーマを簡単に提示することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Unless the URL points to a Scalable Vector Graphics (SVG) file, the image isn't automatically scaled on high-DPI displays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">URL がスケーラブル ベクター グラフィックス (SVG) ファイルを指していない場合、イメージは高 DPI ディスプレイでは自動的にスケーリングされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Design time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>The following example shows an image that uses a URL that is contained in a string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、文字列に含まれる URL を使用するイメージを示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>This code sends a small JavaScript Object Notation (JSON) message to the control on the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、小さな JavaScript Object Notation (JSON) メッセージをクライアントのコントロールに送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>This message instructs the control to treat the image as a URL and let the browser do the work of downloading the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>No download occurs on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバーで発生しているダウンロードはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Storing an image URL in a database table<ept id="p1">&lt;/strong&gt;</ept> You can also have a container field for the image column on your table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>データベース テーブルに画像 URL を格納する<ept id="p1">&lt;/strong&gt;</ept>テーブル上にイメージ列のためのコンテナ フィールドを持つこともできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>You can then use code that resembles the following example to store the <bpt id="p1">&lt;strong&gt;</bpt>ImageReference<ept id="p1">&lt;/strong&gt;</ept> pack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の例を表すコードを使用して、<bpt id="p1">&lt;strong&gt;</bpt>ImageReference<ept id="p1">&lt;/strong&gt;</ept> パックを保存することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>This code causes the user’s browser to download the image from the specified URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードにより、ユーザーのブラウザーは指定された URL からイメージをダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The use of ImageReference involves some overhead, but this approach lets you use a single application programming interface (API) to handle images that are created from binary data, URLs, AOT resources, or symbols.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ImageReference の使用には間接費が発生しますが、このアプローチでは、バイナリデータ、URL、AOT リソース、シンボルから作成されたイメージを処理するために、単一のアプリケーション プログラミング インターフェイス (API) を使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>You can even mix and match image types between rows of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの行間でイメージの種類を組み合わせることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Image type: Binary Image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージの種類: バイナリ イメージ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>Pros</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Cons</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">短所</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Usually, this approach offers the easiest migration if the <bpt id="p1">&lt;strong&gt;</bpt>Image<ept id="p1">&lt;/strong&gt;</ept> class in X++ was already used, or if binary images were previously stored in the database.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ の <bpt id="p1">&lt;strong&gt;</bpt>イメージ<ept id="p1">&lt;/strong&gt;</ept> クラスが既に使用された場合、またはバイナリ イメージがデータベースに先に保存された場合、通常、この方法で移行が最も簡単に行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>This approach involves the largest transfer size, because the binary image is encoded as a string and sent to the client as part of the interaction.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バイナリ イメージは文字列としてエンコードされ、相互作用の一部としてクライアントに送信されるため、この方法では転送サイズが最大になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>The browser can't cache the images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このブラウザーは、画像をキャッシュできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>For a grid, the binary-encoded image is sent for every row, even if multiple rows use the same image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドについては、複数の行が同じイメージを使用していても、バイナリ エンコード イメージがすべての行に対して送信されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Therefore, this approach can lead to very large transfer sizes in the interactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、このアプローチは、相互作用において非常に大きな転送サイズにつながる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You can't easily theme the images by using CSS.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">CSS を使用してもイメージのテーマを簡単に提示することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>The images aren't automatically scaled on high-DPI displays.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージは高 DPI ディスプレイで自動的に拡大/縮小されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Design time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイン時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Run time</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時間</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">&lt;strong&gt;</bpt>Using a database field<ept id="p1">&lt;/strong&gt;</ept> This approach is typically used to display data, such as employee pictures and product images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">&lt;strong&gt;</bpt>データベース フィールドを使用<ept id="p1">&lt;/strong&gt;</ept>この方法は、通常、従業員の写真や製品画像などのデータを表示するために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>You can bind directly to a field, or you can use a display method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに直接バインドするか、表示メソッドを使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Data Source Data Field Data Method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ ソース データ フィールドのデータ メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>Typically, the images are loaded from database, and no additional code is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、イメージはデータベースから読み込まれ、追加のコードは必要ありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>For cases where the image is managed in a data method, see the data method examples.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ メソッドで画像が管理されるケースでは、データ メソッドの例を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Display methods and images (three return types)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドとイメージを表示 (3 つの戻り値の型)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>When you use a display method for an image type to show an image in a grid, three return types are understood by the image control that works with the framework.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像タイプの表示メソッドを使用してグリッドに画像を表示するとき、フレームワークと連携する画像コントロールによって、次の 3 つの戻り値の型が認識されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>All three return types can be used to display an image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つの戻り値の型すべてを使用して画像を表示できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>Int (imagelist array index)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Int (imagelist 配列インデックス)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Container (image instance)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナー (イメージ インスタンス)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>ResID (which is mapped to a symbol)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ResID (記号にマッピングされます)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> ResID and Int are the same return types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> ResID および Int は、同じ戻り値の型です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>If the <bpt id="p1">**</bpt>imageList<ept id="p1">**</ept> property of the image control instance has been assigned an instance value, the display method return value is considered an array index into the imagelist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像コントロール インスタンスの<bpt id="p1">**</bpt>イメージ リスト<ept id="p1">**</ept> プロパティにインスタンス値が割り当てられている場合、表示メソッドの戻り値はイメージ リストへの配列インデックスと見なされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>If the <bpt id="p1">**</bpt>imageList<ept id="p1">**</ept> property is <bpt id="p2">**</bpt>null<ept id="p2">**</ept>, the return value is used to map a legacy ResID to a symbol.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>imageList<ept id="p1">**</ept> プロパティが <bpt id="p2">**</bpt>null<ept id="p2">**</ept> である場合、戻り値は、記号をレガシー ResID をマップするために使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Images in a grid and the legacy ImageList collection</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッドのイメージと旧式 ImageList コレクション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>In AX 2012 and earlier versions, a common use pattern for displaying images is to store an image as a resource or use a kernel-supplied image resource, and then at run time, extract that image and place it in a reusable collection that is known as an ImageList.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AX 2012 およびそれ以前のバージョンにおいて、イメージを表示するための共通の使用パターンでは、リソースとしてイメージを格納、またはカーネルによって提供されるイメージ リソースを使用してから、実行時にそのイメージを抽出して、ImageList と呼ばれる再利用可能なコレクションに配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>The guidance is to use lighter-weight symbol images.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このガイダンスでは軽量の記号画像を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>You should rewrite all legacy code so that it uses symbols directly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">すべてのレガシ コードは、記号を直接使用するように書き換える必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>You should also replace all code that uses the ImageList collection.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ImageList コレクションを使用するすべてのコードを置換する必要もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>If you don't make these changes, the legacy ImageList collection won't display images, because use of this collection relies on embedded (kernel) resources that no longer exist.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更を行わない場合は、旧式 ImageList コレクションを使用すると、もはや存在しない埋め込み (カーネル) のリソースに依存するため、イメージが表示されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Therefore, to support legacy code until it can be updated, the ImageList collection maps the ResID for an embedded resource to a new font-based symbol to help guarantee that any code that uses the ImageList collection will continue to run and provide an image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、更新されるまでレガシー コードをサポートするために、ImageList コレクションは埋め込みリソースの ResID を新しいフォント ベースのシンボルにマップし、ImageList コレクションを使用するコードが引き続き実行され、イメージが提供されるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>Using the imageList property for backward compatibility</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下位互換性のための imageList プロパティの使用</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>An image control has a property that is named <bpt id="p1">**</bpt>imageList<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ コントロールには <bpt id="p1">**</bpt>imageList<ept id="p1">**</ept> という名前のプロパティがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>You pass in an instance of the ImageList collection to this property.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティに ImageList コレクションのインスタンスに渡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>In this way, the image is an array of images that you select via the array number.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法で、イメージは配列番号で選択したイメージの配列です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Display method that returns an ImageRes (legacy image resource ID)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ImageRes を返すメソッドを表示 (レガシ イメージ リソース ID)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Display method that returns a container</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンテナーを返すメソッドを表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Obtaining and displaying an image from the user by using file upload</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ファイルのアップロードを使用して、ユーザーからの画像を取得し表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Model a page that has an image control and a <bpt id="p1">**</bpt>FileUpload<ept id="p1">**</ept> button.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ コントロールと <bpt id="p1">**</bpt>FileUpload<ept id="p1">**</ept> ボタンがあるページをモデル化します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Example of in-memory bitmap manipulation</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メモリ内ビットマップ操作の例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>In this example, an image is created from scratch.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、最初からイメージが作成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>However, developers can also load a bitmap from an alternative source and then manipulate the image as desired (for example, by cropping, stretching, or resizing, or by changing the opacity).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、開発者は代替ソースからビットマップを読み込むこともでき、必要に応じて画像を操作します (たとえば、クロッピング、ストレッチ、またはサイズ変更により、または透過度を変更することにより)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>After any manipulation is completed, the developers can display the image by using the image control, or they can assign it to a data source field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意の操作が完了した後、開発者はイメージ コントロールを使用して画像を表示したり、データ ソース フィールドを割り当てることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Additional examples (URL, binary, and symbol)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加の例 (URL、バイナリ、記号)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>The following table explains two concepts: Image Class and FormImageControl.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のテーブルでは、イメージ クラスと FormImageControl の 2 つの概念について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Image Class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イメージ クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>This class is a run-time representation of an image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスは、画像の実行時表示です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Four constructors:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 つのコンストラクター:</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Image::ConstructBinary(INT64Encode);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Image::ConstructBinary(INT64Encode);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Image::ConstructSymbol(SymbolName);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Image::ConstructSymbol(SymbolName);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Image::ConstructURL(URL);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Image::ConstructURL(URL);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Image::Construct(ResourceName);</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Image::Construct(ResourceName);</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>FormImageControl</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FormImageControl</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>This control is used to add an image at run time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントロールを使用して、実行時に画像を追加できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>.image(new image());</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">.image(new image());</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Using a display method to show an image from a URL string</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メソッドを使用して URL 文字列から画像を表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In this example, a display method is used to translate a string that contains a URL to the format that the image control expects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、表示メソッドを使用してイメージ コントロールが期待している形式に URL を含む文字列を変換します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>This code sends a small JSON message to the control on the client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、小さな JSON メッセージをクライアントのコントロールに送信します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This message instructs the control to treat the image as a URL and let the browser do the work of downloading the image.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメッセージは、コントロールに画像を URL として扱い、ブラウザーに画像のダウンロード作業をさせるように指示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>No download occurs on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバーで発生しているダウンロードはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Using a display method to show a blank image</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示メソッドを使用して空白の画像を表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>There might be times when you have no image for a particular record in a grid, but you don't want an empty space where the image should be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">グリッド内の特定のレコードのイメージがない場合もありますが、イメージを配置する場所は空ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>This example shows how you can use a display method to check for an image value and then substitute a placeholder image instead.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、表示方法を使用してイメージ値をチェックし、代わりにプレースホルダー イメージを置換する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Taking an image URL and storing the image in table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画像の URL を取得し、テーブルに画像を格納</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>You can have a container field for the image column on your table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル上にはイメージ列のためのコンテナ フィールドがある場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can then use code that resembles the following example to store the <bpt id="p1">**</bpt>ImageReference<ept id="p1">**</ept> pack.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の例を表すコードを使用して、<bpt id="p1">**</bpt>ImageReference<ept id="p1">**</ept> パックを保存することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Like the display method that is described in the "Using a display method to show an image from a URL string" section, this code causes the user's browser to download the image from the specified URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「表示メソッドを使用して URL 文字列から画像を表示」のセクションに記載されている表示メソッドと同様に、このコードを使用するとユーザーのブラウザーは指定した URL から画像をダウンロードします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>Although this approach involves some overhead, you can use a single API to handle images that are created from binary data, URLs, AOT resources, or symbols.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法はいくらかの間接費を伴いますが、バイナリ データ、URL、AOT リソースまたは記号から作成された画像を処理するために単一の API を使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>You can even mix and match image types between rows of data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データの行間でイメージの種類を組み合わせることもできます。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>