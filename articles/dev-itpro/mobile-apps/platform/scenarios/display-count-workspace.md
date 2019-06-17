<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="display-count-workspace.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>display-count-workspace.fa8eeb.c73c504301945cf371dd10e5508a44222724a8fc.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c73c504301945cf371dd10e5508a44222724a8fc</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\mobile-apps\platform\scenarios\display-count-workspace.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Show counts in fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに数を表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how to calculate a count that is correct and that appears quickly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、正確で、迅速に表示される数を計算する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Show counts in fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドに数を表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Although a <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control can be used to show counts (totals), it can be slow, because it must load the target page before it counts the number of rows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールを使用してカウント (合計) を表示することができますが、行数をカウントする前にターゲット ページが読み込まれるため遅くなることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Additionally, the count that is calculated can be incorrect, because there is a limit on the number of rows that are retrieved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、取得される行の数に制限があるため、計算される数は正しくない可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Workspace with tiles that show counts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カウントを表示するタイルを持つワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>If you want to make mobile workspaces work more quickly, we recommended that you use a regular field to show the count and then model the field as a <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control in the mobile client.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モバイル ワークスペースをより迅速に動作させる場合は、通常のフィールドを使用してカウントを表示し、そのフィールドをモバイル クライアントの <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールとしてモデル化することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following example uses the Fleet Management app.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例では、フリート管理アプリを使用しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In the Fleet Management app, the workspace shows the total number of customers, reservations, and vehicles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理アプリでは、ワークスペースに顧客、予約、および車両の合計数が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Previously, these counts came from a <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control that had AllCustomers, AllReservations, and AllVehicles as targets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、これらのカウントはターゲットとして AllCustomers、AllReservations、および AllVehicles を持っていた <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールに起因していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control loaded the rows and did the count.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールは行を読み込み、カウントを実行しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>(This approach isn't the recommended approach.)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(この方法は、推奨される方法ではありません。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Follow these steps to configure the workspace page to use the recommended approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">推奨される方法を使用するようワークスペース ページをコンフィギュレーションするには、これらの手順に従います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>On the server, create a new form to contain fields that are also on the server.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サーバーで、サーバー上のフィールドを含む新しいフォームを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>(You can also add the new fields to an existing form).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(既存のフォームに新しいフィールドを追加することもできます。)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>In the following illustration, a new <bpt id="p1">**</bpt>FMMobSummary<ept id="p1">**</ept> form is created that has three fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図では、3 つのフィールドがある新しい <bpt id="p1">**</bpt>FMMobSummary<ept id="p1">**</ept> フォームが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Form that has three fields</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">3 つのフィールドを含むフォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Create a page by using the mobile app designer for the <bpt id="p1">**</bpt>FMMobSummary<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMMobSummary<ept id="p1">**</ept> フォームのモバイル アプリ デザイナーを使用してページを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>New page in the designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーでの新しいページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Update the business logic to transform the fields into a <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドを <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールに変換する業務ロジックを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Use the <bpt id="p1">**</bpt>configureControl<ept id="p1">**</ept> method to add a navigation target to the fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドにナビゲーション ターゲットを追加するには <bpt id="p1">**</bpt>configureControl<ept id="p1">**</ept> メソッドを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The fields are then configured as <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドは、次に <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールとして設定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The arguments for the <bpt id="p1">**</bpt>configureControl<ept id="p1">**</ept> method are the page name, the control name, and an object of properties that must be updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>configureControl<ept id="p1">**</ept> メソッドの引数は、ページ名、コントロール名、および更新が必要なプロパティのオブジェクトです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Update the workspace design.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースのデザインを更新します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Embed the summary page as a part in the workspace page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペース ページの一部として概要ページを埋め込みします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Reference the fields that are now configured as <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールとして構成されるようになったフィールドを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Provide a style, and set the <bpt id="p1">**</bpt>showCount:true<ept id="p1">**</ept> property, so that the count is shown on the <bpt id="p2">**</bpt>pageLink<ept id="p2">**</ept> control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタイルを提供して <bpt id="p1">**</bpt>showCount:true<ept id="p1">**</ept> プロパティを設定し、カウントが <bpt id="p2">**</bpt>pageLink<ept id="p2">**</ept> コントロールに表示されるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Changes to the business logic</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビジネス ロジックの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>By using this approach, you also get the localized labels for <bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法を使用することにより、<bpt id="p1">**</bpt>pageLink<ept id="p1">**</ept> コントロールのローカライズされたラベルも取得します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The result is a much faster experience when workspaces are loaded.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ワークスペースが読み込まれると、結果ははるかに高速になります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>