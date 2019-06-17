<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="understanding-saved-views.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-d915bc8" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>understanding-saved-views.25946d.0a98f7cc39c835f37585402350227787870fe45e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>0a98f7cc39c835f37585402350227787870fe45e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>fcae2e7938d7dbd94b76b0948b084d90d5fc919c</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>06/05/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\user-interface\understanding-saved-views.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build forms that fully optimize saved views</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">保存されたビューを十分に最適化するフォームの作成</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains some of the technical aspects of saved views and describes considerations with form development to ensure forms work well with saved views.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">このトピックでは、保存されたビューの技術的な側面について説明します。また、保存されたビューを使用したフォームがうまく機能するよう、フォーム開発に関する考察を記載します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Build forms that fully optimize saved views</source>
        <target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-inherited">保存されたビューを十分に最適化するフォームの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Saved views are an important expansion of personalization capabilities in Dynamics 365 for Finance and Operations.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">保存されたビューは、 Dynamics 365 for Finance and Operations におけるパーソナライズ機能の中でも重要な拡張機能です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>While the <bpt id="p1">[</bpt>Saved views<ept id="p1">](../../fin-and-ops/get-started/saved-views.md)</ept> topic provides general details about this feature, this topic focuses on the more technical elements of saved views as well as aspects of form development that may be impacted by views.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">[</bpt>保存されたビュー<ept id="p1">](../../fin-and-ops/get-started/saved-views.md)</ept> のトピックでは、この機能の総合的な詳細情報を提供します。ここでは、保存されているビューの技術的な要素のみでなく、ビューの影響を受ける可能性のあるフォーム開発の側面も対象とします。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>“User-perceived” pages</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">「ユーザー視点」のページ</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Traditionally, a set of personalizations has a 1:1 link to a modeled form.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">従来、パーソナライゼーションには、1セットにつきモデル化されたフォームに対する 1:1 のリンクが含まれています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>For many pages, this makes sense to the user, as the user’s perception of the page matches the way in which the form is modeled.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">多くのページでは、これはユーザーにとっては理にかなっています。ユーザーが知覚するページと、フォームをモデル化した方法と合致するためです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>However, in some cases the 1:1 link of a modeled form to a set of personalizations is not intuitive or obvious because users do not see or care about the boundaries between modeled forms.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ただし、場合によっては 1:1のリンクとモデル化されたフォームが、パーソナライゼーションに対して直感的ではなく、わかりにくい場合があります。これはユーザーがモデル化されたフォーム間の境界に対して注意を払っていないためです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Saved views tries to eliminate this confusion by allowing users to create views on “user-perceived” pages, which eliminates the need to understand how forms are modeled to understand how and when personalizations are applied.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">保存されたビューは、このような混乱を解消するべく 「ユーザー視点」 ページ上でビューを作成できる機能がついています。これにより、パーソナライゼーションがいつ、どのように適用されるかを理解するために、フォームがどのようにモデル化されているかを理解する必要がなくなります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Consider the following two scenarios:</source><target logoport:matchpercent="73" state="translated" state-qualifier="fuzzy-match">たとえば、次の2つのシナリオを考えてみます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">**</bpt>More than one “user-perceived” page in a single modeled form<ept id="p1">**</ept>: The standard modeling of Master Details and Transaction Details forms (like the <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> and <bpt id="p3">**</bpt>PurchTable<ept id="p3">**</ept> forms, respectively) consist of more than one “user-perceived” page: a grid page and a details page.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt"><bpt id="p1">**</bpt>一つのモデル化されたフォームに複数の「ユーザー視点」ページ<ept id="p1">**</ept>: マスタの詳細 と トランザクションの詳細 フォーム ( たとえば <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> や <bpt id="p3">**</bpt>PurchTable<ept id="p3">**</ept> フォームなど) は一般的に、グリッドページと詳細ページからなる複数の「ユーザー視点」ページで構成されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Because users are not aware when this transition from list to details crosses a form boundary (nor do they need to know this), view support in Details forms is handled differently to allow views to be defined separately for the grid and details portions.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">これはユーザーはリストから詳細への切り替えることによってフォームの境界を超えていることに気づかない (気づく必要もないのですが) ためです。詳細フォームでのビューのサポートは、グリッド部分と詳細部分で別々にビューを定義できるように、異なる方法で処理されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This means that the view selector for the “grid” and “details” can show different sets of available views.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">つまり、「グリッド」と「詳細」のビューセレクタでは、使用可能なビューの異なるセットを表示できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>The special casing of view support on these forms also allows the “grid” views to allow filters in their view definitions, whereas the “details” view only need personalizations.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">これらのフォームで対応している特殊なケースのビューを使用することで、「グリッド」ビューにてビュー定義にフィルタを適用できます。その一方で「詳細」ビューではパーソナライゼーションのみが必要です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>More than one modeled form in a single “user-perceived” page<ept id="p1">**</ept>: The ability to embed subforms into modeled forms (via FactBoxes or form parts) leads to situations where more than one modeled form corresponds to a single “user-perceived” page.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match"><bpt id="p1">**</bpt>1つの 「ユーザー視点」 ページに複数のモデル化されたフォーム<ept id="p1">**</ept>: モデル化されたフォーム (FactBoxまたはフォームパーツ) にサブフォームを埋め込む機能により、複数のモデル化されたフォームが単一の「ユーザー視点」ページに割り当てられている場合があります</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>For example, consider the details portion of the <bpt id="p1">**</bpt>All customers<ept id="p1">**</ept> page, which has a number of FactBoxes and two FastTabs whose contents come from form parts.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">たとえば、 <bpt id="p1">**</bpt>すべての顧客<ept id="p1">**</ept> ページの詳細の部分には、情報ボックスの数と、フォームパーツの内容情報を取得する2つのファストタブがあります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>With traditional personalization, contrary to a user’s expectations, exporting the personalizations for the <bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> form would not include personalizations on any FactBox or any personalizations done inside the <bpt id="p2">**</bpt>Addresses<ept id="p2">**</ept> or <bpt id="p3">**</bpt>Contact information<ept id="p3">**</ept> FastTabs.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">従来のパーソナリゼーションではユーザーの期待に反して、 <bpt id="p1">**</bpt>CustTable<ept id="p1">**</ept> フォームにおけるパーソナリゼーションのエクスポートには、FactBoxのパーソナリゼーションも <bpt id="p2">**</bpt>住所<ept id="p2">**</ept> 、 <bpt id="p3">**</bpt>連絡先情報<ept id="p3">**</ept> のファストタブ内で行われたパーソナリゼーションも含まれていませんでした。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Equally unexpected for users, any personalizations done on these subforms would also be reflected in other parts of the application where these form parts are used.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">これと同様にユーザーが予期しないこととして、これらのサブフォームで行われたパーソナライゼーションはすべて、該当するフォームパーツが使用されているアプリケーションの他の部分にも反映されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>For example, changes to the <bpt id="p1">**</bpt>Addresses<ept id="p1">**</ept> FastTab in the <bpt id="p2">**</bpt>All customers<ept id="p2">**</ept> page would also result in the same changes appearing in the <bpt id="p3">**</bpt>Addresses<ept id="p3">**</ept> FastTab in the <bpt id="p4">**</bpt>All vendors<ept id="p4">**</ept> page.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">例えば <bpt id="p2">**</bpt>すべての顧客<ept id="p2">**</ept> ページ内の <bpt id="p1">**</bpt>住所<ept id="p1">**</ept> ファストタブに変更を加えると、変更した内容が <bpt id="p4">**</bpt>すべての仕入先<ept id="p4">**</ept> ページの <bpt id="p3">**</bpt>住所<ept id="p3">**</ept> ファストタブにも反映されます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>With views, the personalization scope of form parts has been modified to match user expectations.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ビューでは、フォームパーツのパーソナライゼーションの範囲が、ユーザーの期待に合うように変更されています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>In particular, subform personalizations are now tied to the base form where they are made.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">特にサブフォームのパーソナライゼーションは、作成された基本フォームに関連付けられるようになっています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>This means that exporting a view on the <bpt id="p1">**</bpt>All customers<ept id="p1">**</ept> details page will include personalizations from the base <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> form as well as any personalizations in FactBoxes or form parts modeled in that portion of the form.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">つまり、 <bpt id="p1">**</bpt>すべての顧客<ept id="p1">**</ept> の詳細ページからビューをエクスポートすると、元となっている <bpt id="p2">**</bpt>CustTable<ept id="p2">**</ept> フォームのパーソナライゼーションと、FactBox またはフォーム上の該当部分でモデル化されたフォームパーツからの個人設定が含まれます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Similarly, any personalizations done on the <bpt id="p1">**</bpt>Addresses<ept id="p1">**</ept> FastTab (form part) on the <bpt id="p2">**</bpt>All customers<ept id="p2">**</ept> page will not be reflected in other forms where that form part is used.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">同様に、 <bpt id="p2">**</bpt>すべての顧客<ept id="p2">**</ept> ページ内の <bpt id="p1">**</bpt>住所<ept id="p1">**</ept> ファストタブ (フォームパーツ) で行ったパーソナライゼーションは、そのフォームパーツを使用している他のフォームには反映されません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>These are highly technical modifications to the personalization subsystem that are only available when view is enabled.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">これらはパーソナライゼーション・サブシステムに対する高度な技術的変更であり、ビューが使用可能となっている場合にのみ利用できます。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>These modifications are very important for ensuring that users have a predictable and understandable experience with views.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">これらの変更は、ユーザーがビューに関して予測可能で理解しやすい運用を行うにあたって非常に重要となります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>View support</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ビューのサポート</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The style of a form determines the level of support for views.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">フォームのスタイルは、ビューのサポートレベルによって決まります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Views include queries for forms, such as:</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ビューには、以下のようなフォームに対するクエリが含まれています</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>List pages</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">リスト ページ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Simple lists</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">簡易リスト</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Grid portions of Master Details and Transaction Details forms</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">[マスタの詳細] フォーム と [トランザクションの詳細] フォーム のグリッド部分</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Views do not include queries, such as:</source><target logoport:matchpercent="74" state="translated" state-qualifier="fuzzy-match">以下のようなクエリは、ビューには含まれていません</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Any other full-page form</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">その他形式のフルページのフォーム</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Details portions of Master Details and Transaction Details forms</source><target logoport:matchpercent="87" state="translated" state-qualifier="fuzzy-match">[マスタの詳細] フォーム と [トランザクションの詳細] フォーム の詳細</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Views that are not currently supported include:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">以下のビューについては現在対応していません</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Dashboards</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm"> ダッシュボード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Workspaces</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ワークスペース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Dialogs</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ダイアログ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Secondary forms like drop-down dialogs, lookups, and enhanced previews</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ドロップダウンダイアログ、ルックアップ、強化されたプレビューなどの、副次的なフォーム</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>Modifying forms to fully utilize views</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">フォームを変更してビューを完全に活用する</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>While most forms will work well with saved views, there are some areas that may require changes to form logic so that views work as expected on these forms without causing confusion.</source><target logoport:matchpercent="101" state="translated" state-qualifier="id-match">ほとんどのフォームは保存されたビューで十分に機能しますが、フォー上でビューが問題なく想定どおりに機能するためには、フォームロジックへの変更が必要となる部分も存在します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Here are some key items to keep in mind during development of new forms.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">以下は、新しいフォームを開発する際に留意すべき重要な項目です。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>X++ code late in the form startup cycle can interfere with views working as users expect.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">フォームのスタートアップサイクルにてX++コードの遅延が発生すると、ビューが想定どおりに機能しない可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>In particular, be aware of the following:</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">特に、以下の点にご注意ください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Modifications of the query post super() of executeQuery() or post super() of run() can cause the query aspect of a view to be ignored.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">executeQuery() 内の super()または、run() 内の super() のクエリに対する変更を行うと、ビューからのクエリが無視される可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Form changes post super() of run() can result in some user personalizations not applying correctly.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">run() 内の super() に対するフォーム変更を行うと、ユーザーのパーソナライゼーションが正しく適用されない可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Extra work may be required to ensure the values of custom filters always align to the current view or query.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">カスタムフィルタの値を常に現在のビュー、またはクエリに合わせるには、追加の作業が必要となる場合があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Forms may need to be instrumented to ensure the values of custom filters update based on the current query and aren’t just initialized to the same default value with each form load.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在のクエリに基づいてカスタムフィルタの値を更新し、フォームの読み込みごとに同じ既定値に初期化されないようにするには、フォームを計測する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Looking forward, in the long-term, views are meant to replace modeled secondary list pages.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">長期的に見ると、ビューはモデル化されたセカンダリ リストページに取って代わるものです。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Typically, secondary list pages, such as Customers on hold, are menu items that point at the same form but have a different query.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">通常、保留中の得意先などのセカンダリ リスト ページは、同じフォームを指定するメニュー項目ですが、異なるクエリを持っています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Because menu items that pass in queries will override any query defined on the default view, these entry points can create confusion for users.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">クエリを渡すメニュー項目は、既定のビューで定義されているすべてのクエリを上書きするため、こうしたエントリ ポイントはユーザーを混乱させる可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>Long-term, the current plan is to deprecate secondary list pages and move them to views.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">長期的には、セカンダリ リストページを廃止して、それらをビューに移動する計画となっています。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>To avoid user confusion between form caption (such as “All customers”) and view name (such as “My customers”), consider renaming form captions to simply be the name of the corresponding entity.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">ユーザがフォームキャプション (「すべての顧客」など) とビュー名 (「お客様」など) を混同しないように、フォームキャプションを対応するエンティティの名前に変更することを検討してください。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>For example, instead of a form caption of “All customers” or “All sales orders”, the form caption would be modified to “Customers” and “Sales orders”.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">たとえば、フォームキャプションに 「すべての顧客」 や 「すべての受注」 と表示していたものを、 「顧客」 や 「受注」 へと変更します。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Known issues</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Publishing views that contain personalizations on subforms (FactBoxes or form parts) will currently not publish the subform portion of the view.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在、サブフォームにパーソナライゼーションを含む発行ビュー(FactBoxe または フォームパーツ)では、ビューのサブフォーム部分を発行できません。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>While re-publishing the current view, an update of the name of the view creates a second view instead of replacing the original one.</source><target logoport:matchpercent="70" state="translated" state-qualifier="leveraged-mt">現在のビューを再発行するときに、ビューの名前を更新すると、元のビューを置き換えるのではなく、2番目のビューが作成されます。</target>
        </trans-unit>
      </group>
    </body>
  </file>
</xliff>