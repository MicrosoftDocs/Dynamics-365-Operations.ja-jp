<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="delegates-migration.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>delegates-migration.1459e1.8ddd1527bfa0fc162e62bcf044ab999d5c441c5b.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>8ddd1527bfa0fc162e62bcf044ab999d5c441c5b</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>574d4dda83dcab94728a3d35fc53ee7e2b90feb0</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/22/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\migration-upgrade\delegates-migration.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Solve dependencies among models by using delegates during code migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの移行中にデリゲートを使用してモデル間の依存関係の解決</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic explains how delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Solve dependencies among models by using delegates during code migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの移行中にデリゲートを使用してモデル間の依存関係の解決</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic explains how delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、デリゲート インスタンスとデリゲート ハンドラ間でコントラクトを定義する手段としてデリゲート メソッドがどのように機能するかについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>Overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Microsoft Dynamics 365 for Finance and Operations is split into more several models, with each model in separate package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations は、各モデルが個別のパッケージにある、複数のモデルに分割されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The principal 3 models are Application Platform, Application Foundation, and Application Suite (See <bpt id="p1">[</bpt>Models<ept id="p1">](../dev-tools/models.md)</ept> to learn about models and packages).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">主要な 3 つのモデルは、アプリケーション プラットフォーム、アプリケーション基盤、およびアプリケーション スイートです (モデルとパッケージについては、<bpt id="p1">[</bpt>モデル<ept id="p1">](../dev-tools/models.md)</ept>を参照してください)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>With the model split, a hierarchy has been created where a higher model can take dependencies and access elements in the models below, but not in models above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデル分割を使用して、階層が作成されました。ここで上位のモデルは依存関係を持つことができ、下位のモデル内の要素にアクセスできますが、上位のモデルにはアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>In this setup, Application Suite has full access to its elements, Application Foundation’s elements, and Application Platform’s elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この設定では、アプリケーション スイートはその要素、アプリケーション基準の要素およびアプリケーション プラットフォームの要素にフル アクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Application Foundation can access its own elements and those of Application Platform.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション基準は、独自の要素とアプリケーション プラットフォームの要素にアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Finally, Application Platform can only access its own elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、アプリケーション プラットフォームは独自の要素にのみアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del1<ept id="p1">](./media/del1.jpg)](./media/del1.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del1<ept id="p1">](./media/del1.jpg)](./media/del1.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>While the model split provides many benefits, it creates a problem when trying to access elements defined in higher models.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">モデルの分割には多くの利点がありますが、上位モデルで定義された要素にアクセスするとき問題が発生します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Delegates are the recommended method for accessing elements in higher models from a lower model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上位モデルの要素に下位モデルからアクセスするに、デリゲートが推奨されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Delegates are very similar to events in that when a delegate instance is invoked, a handler with compatible signature code is executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは、デリゲート インスタンスが呼び出されると、互換性のある署名コードを持つハンドラーが実行されるという点で、イベントと非常によく似ています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>This permits higher layer code, the handler, to be called by lower layer code, the delegate instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、ハンドラーである上位レイヤーコードが、デリゲート インスタンスである下位レイヤーコード (デリゲート インスタンス) によって呼び出されるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Create delegates and handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任およびハンドラーを作成します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>A delegate declaration must have three things:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートの宣言には、次の 3 つが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The delegate keyword</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任キーワード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Type void</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">無効タイプ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Empty method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">空のメソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Delegate methods serve as a means for defining a contract between the delegate instance and the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート メソッドは、デリゲート インスタンスとデリゲート ハンドラー間のコントラクトを定義する手段として機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>A delegate takes no action itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートは、アクション自体を行ないません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>This is enforced by having a void type and having no code in the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、void 型を持ち、メソッドにコードがないことによって適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Adding the <bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> keyword to a method creates a static delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドに <bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> キーワードを追加して、静的委任ハンドラーを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> requires the class name of the delegate, and the string name of the delegate method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> にはデリゲートのクラス名、およびデリゲート メソッドの文字列名が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>In order for a delegate to be properly handled, the delegate method declaration, the delegate instance, and the delegate handler must have the <bpt id="p1">*</bpt>same<ept id="p1">*</ept> method signature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートが適切に処理されるには、デリゲート メソッドの宣言、デリゲート インスタンスおよびデリゲート ハンドラーに<bpt id="p1">*</bpt>同じ<ept id="p1">*</ept>メソッドの署名が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>For example, the delegate instance below takes two inputs, a real number and an EventHandlerResult, matching the delegate declaration and handler signatures above.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、次に示すデリゲート インスタンスには、2 つの入力が必要です。実数および EventHandlerResult で、上記のデリゲート宣言およびハンドラー署名と一致するものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>static delegate handler</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">static delegate ハンドラー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Due to the fact that delegates do not have a return value, an EventHandlerResult is passed as a parameter to provide access to the needed result value after the delegate has returned.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートに戻り値がないため、EventHandlerResult がパラメーターとして渡され、デリゲートが返された後に必要な結果値にアクセスできるようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>This topic focuses on static delegate handlers using the SubscribesTo.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、SubscribesTo を使用する静的委任ハンドラーについて説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>The delegate functionality from Dynamics AX 2012 remains.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 からのデリゲート機能が保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">[</bpt>How to use X++ Delegates in Dynamics AX 2012<ept id="p1">](https://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx)</ept> is a great blog post on MSDN by Microsoft developer Marcos Calderon on delegate concepts in Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Dynamics AX 2012 で X++ デリゲートを使用する方法<ept id="p1">](https://blogs.msdn.com/b/x/archive/2011/08/02/how-to-use-x-delegates-in-dynamics-ax-2012.aspx)</ept> は Dynamics AX 2012 のデリゲートの概念について、Microsoft の開発者 Marcos Calderon が MSDN に投稿した素晴らしいブログです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>These concepts still apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの概念が引き続き適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Example scenarios</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ例</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Overlaying an existing delegate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存の委任のオーバーレイ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>In many cases where delegates are needed, the code that was formerly overlayed has already been moved to a delegate handler by Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートが必要な多くの場合、以前にオーバーレイされたコードは既に Microsoft によってデリゲート ハンドラーに移動されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>In these instances, Microsoft created delegates that can be leveraged and the code can be overlayed in a similar manner in the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのインスタンスで、Microsoft は利用できるデリゲートを作成し、デリゲート ハンドラーで同様の方法でコードをオーバーレイできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>In this scenario, an Independent Software Vendor (ISV) is migrating code from Dynamics  AX 2012 R3 where they have overlayed the showSalesTax() method in the LogisticsEntityPostalAddressFormHandler class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、独立系ソフトウェア ベンダー (ISV) が、LogisticsEntityPostalAddressFormHandler クラスで showSalesTax() メソッドをオーバーレイした Dynamics AX 2012 R3 からコードを移行しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>After migration, the CodeUpgrade project will contain the LogisticsEntityPostalAddressFormHandler with the <bpt id="p1">*</bpt>Your Solution<ept id="p1">*</ept>, <bpt id="p2">*</bpt>Microsoft AX 2012,<ept id="p2">*</ept> and <bpt id="p3">*</bpt>Microsoft AX<ept id="p3">*</ept> sections to resolve for the showSalesTax() method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行後に、CodeUpgrade プロジェクトは、<bpt id="p1">*</bpt>Your Solution<ept id="p1">*</ept>、<bpt id="p2">*</bpt>Microsoft AX 2012<ept id="p2">*</ept>、<bpt id="p3">*</bpt>Microsoft AX<ept id="p3">*</ept> セクションを使用する LogisticsEntityPostalAddressFormHandler が含まれ、showSalesTax() メソッドを解決します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The commented Your Solution section shows that the showSalesTax() method was overlayed by adding an additional table to approve showing sales tax from.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コメントされた Your Solution セクションには、売上税の表示を承認するための追加のテーブルを追加することによって、showSalesTax() メソッドがオーバーレイされたことが示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This overlay is shown between the <ph id="ph1">&amp;lt;</ph>isv<ph id="ph2">&amp;gt;</ph> tags circled in red below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオーバーレイは、赤で丸で囲まれた <ph id="ph1">&amp;lt;</ph>isv<ph id="ph2">&amp;gt;</ph> タグの間に表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>4<ept id="p1">](./media/41.png)](./media/41.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>4<ept id="p1">](./media/41.png)](./media/41.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>When comparing this overlay with the code from Dynamics AX 2012, this is a simple change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオーバーレイを Dynamics AX 2012 のコードと比較するとき、これは単純な変更です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The overlay has added an additional table to the switch statement.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイによって、switch ステートメントに追加のテーブルが追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>5<ept id="p1">](./media/51.png)](./media/51.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>5<ept id="p1">](./media/51.png)](./media/51.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>However, the Finance and Operations section does not appear to resemble either of the Dynamics AX 2012 code snippets.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、Finance and Operations セクションでは、Dynamics AX 2012 コード スニペットのいずれかと同じようには表示されません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>6<ept id="p1">](./media/61.png)](./media/61.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>6<ept id="p1">](./media/61.png)](./media/61.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>Upon deeper inspection, the code is calling a delegate method, showSalesTax<ph id="ph1">\_</ph>delegate().</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細な点検を行う際、コードはデリゲート メソッド showSalesTax<ph id="ph1">\_</ph>delegate() を呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>this.showSalesTax<ph id="ph2">\_</ph>delegate(this.getCallerRecord().TableId, result);<ept id="p1">](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>this.showSalesTax<ph id="ph2">\_</ph>delegate(this.getCallerRecord().TableId, result);<ept id="p1">](./media/showsalestax_delegate.png)](./media/showsalestax_delegate.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>The use of a delegate implies that code has been moved to another location.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートの使用は、コードが別の場所に移動されたことを意味します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The showSalesTax<ph id="ph1">\_</ph>delegate() has been declared in the Application Foundation and handled in the Application Suite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">showSalesTax<ph id="ph1">\_</ph>delegate() は、アプリケーション基準で宣言され、Application Suite で処理されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>To view the code that has been moved, find the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移動されたコードを表示するには、デリゲート ハンドラを探します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The <bpt id="p1">**</bpt>Finding Delegates and Handlers<ept id="p1">**</ept> section contains methods to locate delegates and handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デリゲートとハンドラーの検索<ept id="p1">**</ept> セクションには、デリゲートとハンドラーを検索するメソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>After finding the delegate handler method in the Application Suite, we see the code that has been moved from the showSalesTax() method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション スイートでデリゲート ハンドラー メソッドを検索した後、showSalesTax() メソッドからから移動されたコードを参照します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The same overlayered changes applied in Dynamics AX 2012 can be applied in the delegate handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX 2012 で適用されているオーバーレイされた同じ変更を、デリゲート ハンドラーに適用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Finding delegates and handlers code sample<ept id="p1">](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>委任とハンドラーのコード サンプルの検索<ept id="p1">](./media/findingdelegatesandhandles.png)](./media/findingdelegatesandhandles.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>After adding the new table to the switch statement in the delegate handler, the code will function as it did in Dynamics AX 2012.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラーで switch ステートメントに新しいテーブルを追加した後、コードは Dynamics AX 2012 の場合と同じように機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ShowSalesTax method code<ept id="p1">](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ShowSalesTax メソッド コード<ept id="p1">](./media/showsalestaxmethod.png)](./media/showsalestaxmethod.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Adding a new delegate</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい委任の追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In this scenario, we will modify an existing tax calculation method that resides in the Application Foundation to account for discounts created in the Application Suite.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このシナリオでは、アプリケーション スイートで作成された割引を考慮するために、アプリケーション基準に存在する既存の税計算方法を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>The following class in the Foundation layer calculates the tax based on the gross total.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Foundation レイヤーの次のクラスは、総額に基づいて税金を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>SimpleTax class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SimpleTax クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>In the Application Suite, we have introduced the notion of discounts by adding a ProductDiscount class that contains the current discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション スイートでは、現在の割引を含む ProductDiscount クラスを追加することで割引の概念を導入しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>11<ept id="p1">](./media/112.png)](./media/112.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>11<ept id="p1">](./media/112.png)](./media/112.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The TaxCalculator class, in the lower Foundation layer, does not have access to the DiscountRate in the Suite layer and must use a delegate to update receipt total to use in the tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Foundation レイヤー下部にある TaxCalculator クラスには、Suite レイヤーの DiscountRate へのアクセス権がないため、委任を使用して受領合計を更新し、税計算に使用する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the SimpleTax class, we create a delegate method, applyDiscountDelegate, with the state information that is needed by the handler in the signature.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SimpleTax クラスでは、署名のハンドラーによって必要な状態情報とともにデリゲート メソッド applyDiscountDelegate を作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>A delegate method is always empty because its only purpose is to define the contract between the delegate instance and the handler.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">デリゲート メソッドは、デリゲート インスタンスとハンドラー間のコントラクトを定義することが唯一の目的のため、常に空です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The signature for the delegate declaration, the delegate instance, and the delegate handler must match.</source><target logoport:matchpercent="95" state="translated" state-qualifier="fuzzy-match">デリゲートの宣言、デリゲート インスタンスおよびデリゲート ハンドラーの署名は一致する必要があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>We now have to create an instance of the delegate at the point in the code where we would like the delegate handler to be run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲート ハンドラーを実行するコード内の箇所に、デリゲートのインスタンスを作成することが必要になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The changes in between the <ph id="ph1">&amp;lt;</ph>isv<ph id="ph2">&amp;gt;</ph> tags represent the added code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><ph id="ph1">&amp;lt;</ph>isv<ph id="ph2">&amp;gt;</ph> タグ間での変更は追加されたコードを表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>calculateTotalTax method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">calculateTotalTax method</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>With the delegate in place, we now add a handler method in the Application Suite layer that has access to the discount information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートの環境が整い、割引情報へのアクセス権を持つアプリケーション スイート レイヤーに、ハンドラー メソッドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>applyDiscountDelegateHandler method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">applyDiscountDelegateHandler メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Using the SubscribesTo keyword, we tie the applyDiscountDelegateHandler method as a handler to the applyDiscountDelegate delegate.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">SubscribesTo キーワードを使用して、applyDiscountDelegateHandler メソッドを applyDiscountDelegate デリゲートにハンドラーとして結合します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>There can be more than one handler per delegate.</source><target logoport:matchpercent="90" state="translated" state-qualifier="fuzzy-match">デリゲートごとに複数のハンドラーが存在する可能性があります。</target>
        </trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>There is <bpt id="p1">**</bpt>not<ept id="p1">**</ept> a defined order in the processing of handler methods.</source>
        <target logoport:matchpercent="100" state="translated" state-qualifier="leveraged-tm">ハンドラー メソッドの処理には、定義された順序は<bpt id="p1">**</bpt>ありません<ept id="p1">**</ept>。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If order is important, delegate handler pairs should be chained together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">注文が重要な場合は、代行ハンドラーのペアは一緒に連鎖する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>With the final classes below, when the calculateTotalTax() method is run, the applyDiscountDelegate is fired and handled, updating the receiptTotal to provide an accurate tax calculation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下の最終クラスでは、calculateTotalTax() メソッドが実行されるとき、applyDiscountDelegate が起動および処理され、receiptTotal が更新されて正確な税計算が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Full Code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完全なコード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>SimpleTax class in the Application Foundation Layer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Application Foundation Layer の SimpleTax クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>SimpleTax class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SimpleTax クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>ProductDiscount class in the Application Suite layer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション スイート レイヤーの ProductDiscount クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>ProductDiscount class</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ProductDiscount クラス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>Find delegates and handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任およびハンドラーを検索します</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>There are three key ways to find delegates and handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートとハンドラーを見つける主要な 3 つの方法があります</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Metadata search</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ検索</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Class references</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>SubscribesTo references</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubscribesTo 参照</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>The Metadata search tool, described on the <bpt id="p1">[</bpt>Metadata search in Visual Studio<ept id="p1">](../dev-tools/metadata-search-visual-studio.md)</ept> page, is the best way to find either delegates or their handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>メタデータ検索と Visual Studio<ept id="p1">](../dev-tools/metadata-search-visual-studio.md)</ept> ページで説明されているメタデータ検索ツールは、デリゲート、またはそのハンドラーを検索するための優れた方法です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>In Visual Studio, go to <bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **<ph id="ph1">&amp;gt;</ph> **Metadata Search<ept id="p1">&lt;/strong&gt;</ept> to open the metadata search tool.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio で、<bpt id="p1">&lt;strong&gt;</bpt>Dynamics 365 **<ph id="ph1">&amp;gt;</ph> **メタデータ検索<ept id="p1">&lt;/strong&gt;</ept>に移動してメタデータ検索ツールを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del15<ept id="p1">](./media/del15.png)](./media/del15.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del15<ept id="p1">](./media/del15.png)](./media/del15.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>In the search field, type “code:<ph id="ph1">&amp;lt;</ph>delegate name<ph id="ph2">&amp;gt;</ph>” which will restrict the search to code and find any use of the delegate name, returning both the delegate and handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索フィールドに、「code:<ph id="ph1">&amp;lt;</ph>デリゲート名<ph id="ph2">&amp;gt;</ph>」を入力して検索をコードに制限し、デリゲート名の使用を見つけると、デリゲートとハンドラーの両方を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Metadata search will search the entire code base and may take some time to complete, but will return any use of the search term in code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ検索は全体のコード ベースを検索し、完了に時間がかかる場合がありますが、コードにあるすべての検索用語の使用を返します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del16<ept id="p1">](./media/del16.png)](./media/del16.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del16<ept id="p1">](./media/del16.png)](./media/del16.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Methods two and three can be used in parallel to the metadata search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド 2 および 3 はメタデータ検索に並行して使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>The class where a delegate is defined can also serve as a means to narrow down the search for a delegate or handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートが定義されているクラスは、デリゲートまたはハンドラーの検索を絞り込む手段としても機能します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>The SubscribesTo keyword requires the class name where the delegate was defined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SubscribesTo キーワードには、デリゲートが定義されているクラス名が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Visual Studio’s find references (right-click the class name <ph id="ph1">&amp;gt;</ph> find references) will return a list of files that reference the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の 参照の検索 (クラス名の右クリック <ph id="ph1">&amp;gt;</ph> 参照の検索) により、クラスを参照するファイルの一覧が返されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This list will include both the class definition where the delegate is declared and the handler referencing the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストには、デリゲートが宣言されているクラス定義とそのクラスを参照するハンドラーの両方が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Finding class references is not a perfect method and will require some manual searching through class references.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス参照の検索は完全な方法ではなく、クラス参照によるいくつかの手動検索を必要とします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>However, it produces a smaller subset of files and can be faster than a metadata search.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、少さいサブセットのファイルが生成され、メタデータ検索よりも早くなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del17<ept id="p1">](./media/del17-1024x300.png)](./media/del17.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del17<ept id="p1">](./media/del17-1024x300.png)](./media/del17.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Similar to finding class references, finding all references can be done on the SubscribesTo keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス参照の検索と同様、すべての参照の検索は、SubscribesTo キーワードで行うことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>The resulting list will include all static delegate handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">結果リストには、すべての静的デリゲート ハンドラーが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Manually going through this list provides another means for finding static delegate handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この一覧を手動で移動することで、静的デリゲート ハンドラーを検索できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>This will not return dynamically declared delegate handlers that do not use the SubscribesTo keyword.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、SubscribesTo キーワードを使用しない動的に宣言された代理ハンドラを返しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del18<ept id="p1">](./media/del18-1024x328.png)](./media/del18.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Del18<ept id="p1">](./media/del18-1024x328.png)](./media/del18.png)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>