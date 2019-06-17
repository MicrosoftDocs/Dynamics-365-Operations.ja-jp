<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="writing-extensible-code.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>writing-extensible-code.83f7dc.d9c2e4772fce96ffcc302794df69bf556b4d6849.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>d9c2e4772fce96ffcc302794df69bf556b4d6849</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\writing-extensible-code.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Write extensible code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコードの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about how to write extensible code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張可能コードを書き込む方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Write extensible code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能なコードの書き込み</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>X++ and the metadata model provide a powerful foundation for building business solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ およびメタデータ モデルは、ビジネス ソリューションを構築するため強力な基礎を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>One of the design pillars is to automate as many technical concerns as possible, so that the engineer can focus on the business domain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザインの柱の 1 つは、エンジニアがビジネス ドメインに焦点を当てることができるように、できるだけ多くの技術的な問題を自動化することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>For example, if you put all the text resources in label files, one technical concern that you don't have to worry about is the localization of text resources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ラベル ファイルにすべてのテキスト リソースを配置した場合、心配しなくてもよい 1 つの技術的な問題はテキスト リソースのローカライズです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Extensibility is another technical concern.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張性は、別の技術的な問題です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>You want other people to be able to extend your solution in a safe, robust, and maintainable way.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のユーザーが安全かつ堅牢で管理可能な方法でソリューションを拡張できるようにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>By default, your solution is highly extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既定では、ソリューションの拡張性は高くなっています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, there are a few guidelines that you should follow to help guarantee completeness.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、完全性を保証するために従う必要のある、いくつかのガイドラインがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Responsibilities</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">職責</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Any Microsoft Dynamics 365 for Finance and Operations environment runs a business solution that includes components from many sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どの Microsoft Dynamics 365 for Finance and Operations 環境でも、さまざまなソースからのコンポーネントを含むビジネス ソリューションが実行されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Typically, each solution has code from Microsoft, independent software vendors (ISVs) and partners, and also internally developed code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常、各ソリューションにはマイクロソフト、独立系ソフトウェア ベンダー (ISV)、パートナーのコード、さらに内部開発のコードも含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Each contributor is responsible for its own contribution to the solution and for the way that its contribution interacts with other contributions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各コントリビューターは、ソリューションへの自分の貢献と、自分の貢献が他のユーザーの貢献と関わる方法に責任を負っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>When you write extensible code, you invite other people to interact with your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能コードを作成するとき、ソリューションを操作するよう他のユーザーを招待します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>Your responsibility is to enable other people to be good guests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自分の責任は、他のユーザーを適切なゲストにすることです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Here is how you meet this responsibility:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この責任を果たす方法を以下に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Make robust extension points<ept id="p1">**</ept> – Extension points are the foundation of extenders' solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>信頼性の高い拡張ポイントを作成する<ept id="p1">**</ept>: 拡張ポイントは拡張担当者のソリューションの土台部分です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>They must be well-defined and robust from release to release.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切に定義されていて、リリースごと堅牢である必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source><bpt id="p1">**</bpt>Invite side-by-side customizations<ept id="p1">**</ept> – Recognize that multiple extenders might use the same extension point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>サイド バイ サイド カスタマイズを招待<ept id="p1">**</ept>: 複数の拡張担当者が同じ拡張ポイントを使用する場合があることを認識します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>Enable 1:n (one-to-many) interactions instead of 1:1 (one-to-one) interactions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1:1 (1 対 1) のやり取りではなく、1: n (1 対多) のやり取りを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Trust that extenders will be well-behaved<ept id="p1">**</ept> – All responsible parties share the same goal: to create great, lasting solutions for the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張担当者が適切に行動することを信頼<ept id="p1">**</ept>: すべての責任者は、長続きする優れた顧客向けソリューションを作成するという同じ目標を共有します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>When you create extension points, you give up control and share the responsibility with other people.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張ポイントを作成するときは、コントロールを引き渡し、他のユーザーと責任を共有します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>Assume that extenders will be cautious and use your extension points as they were intended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張担当者は慎重であり、意図した拡張ポイントを使用しているとみなします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Proven principles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実績のある原則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>All the good engineering practices that you're already using still apply.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既に使用している優れたエンジニアリングの手法がすべて適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Everything that you've learned still applies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">学習したことすべても適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>You don't have to learn new principles or unlearn old practices.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しい原則を習得したり、古い手法を忘れる必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>This topic is just highlighting three principles of software craftmanship that have been sought and taught for decades.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、何十年もの間求められ、教えられ続けてきた、ソフトウェア作成者が守るべき 3 つの原則だけ強調します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>These principles not only make your code easier to read, maintain, test, review, and refactor, but also make your code easier to extend.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの原則により、コードが読み取り、管理、テスト、確認、リファクタリングしやすくなるだけでなく、コードを簡単に拡張できるようにもなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Apply and advocate these principles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの原則を適用して推奨します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Extend code by using the SOLID principles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOLID を使用してコードを拡張する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>SOLID is an acronym for five principles that you can use to make your code easier to extend:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SOLID は、コードを簡単に拡張できるようにするために使用できる 5 つの原則の頭字語です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Single responsibility<ept id="p1">**</ept> – Classes and method should have a single responsibility and should not have side-effects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>1 つの責任<ept id="p1">**</ept>: クラスおよびメソッドには責任が 1 つでなければならず、副作用があってはなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>By following this principle, you help guarantee that extension points that are automatically created on public and protected methods will be great extension points.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則に従うと、パブリックな保護された方法で自動的に作成される拡張ポイントが優れた拡張ポイントになることを保証することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Open/closed<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>オープン/クローズ<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Open for extension<ept id="p1">**</ept> – Open your solution for extensions by designing and considering the extension surface.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>拡張に対してオープン<ept id="p1">**</ept>: 拡張サーフェイスをデザインして検討することにより、拡張のソリューションを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>After an extension point is made available, you're responsible for maintaining it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張ポイントが使用可能になったら、管理を担当します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>This responsibility adds significant restrictions to future development.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この責任は、今後の開発に重要な制限を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>It's often preferable to open a solution up for extension by demand.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">多くの場合、需要に応じて拡張に対してソリューションを開くことをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>For example, use internal methods over public methods or private methods over protected methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、パブリック メソッドより内部メソッドを使用したり、保護されたメソッドよりプライベート メソッドを使用したりします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Closed for modification<ept id="p1">**</ept> – Make your properties private, and make your methods either private or final-protected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>変更に対して閉じている<ept id="p1">**</ept>: プロパティをプライベートにし、メソッドをプライベートまたは最終保護にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In this way, no one can take advantage of a dependency on your logic, either through inheritance or extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法により、継承または拡張を通じて、ロジックで依存関係を活用できる人はいません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Liskov substitution<ept id="p1">**</ept> – Derived classes must be able to be substituted for their base classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>リスコフ置き換え<ept id="p1">**</ept>: 派生クラスは、基本クラスの代わりに使用できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>For example, this substitution can be done by providing factories, by using SysExtension, and by using simple construct methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、この置き換えは、ファクトリを指定する、SysExtension を使用する、および単純なコンストラクト メソッドを使用することにより実行できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Interface segregation<ept id="p1">**</ept> – Create concise interfaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インターフェイスの分離<ept id="p1">**</ept>: 簡単なインターフェイスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>This principle lets extenders provide replacement implementations and is particularly valuable when it's used together with the next SOLID principle, dependency inversion.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則により、拡張担当者は置き換えの実装を提供します。次の SOLID 原則である依存関係の反転と組み合わせて使用する場合は、特に重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Dependency inversion<ept id="p1">**</ept> – Depend on abstractions, not concretions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>依存関係の反転<ept id="p1">**</ept>: 具体化ではなく抽象化に依存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This principle enables decoupling and lets extenders provide concrete instances that conform to the abstraction that your logic depends on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則により切り離しが可能になり、拡張担当者は、ロジックが依存している抽象化に準拠している具体的なインスタンスを提供できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>Write clean code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリーンなコードの記述</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Clean code can be read like an article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリーンなコードは、記事のように読むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The name of a method provides the heading of the article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの名前は、記事の見出しを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The body of the method comes next and really consists of just a few lines of summary.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次にメソッドの本文があり、概要はわずか数行で構成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>This summary calls a few other methods that have good descriptive names.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この概要は、適切な内容を示す名前を持つ他のいくつかのメソッドを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>In this way, the reader can keep exploring details and can also stop at any time without missing any conceptual information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、読み手は、詳細を閲覧し続け、概念に関する情報を見逃すことなくいつでも停止することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>When code is written like in this manner, methods are short, often less than 5 to 10 code lines.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法でコードが記述されると、メソッドは短く (多くの場合 5 ～ 10 コード行未満) なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Additionally, the number of parameters is low, often less than two, and the conditions and blocks of code are always a single code line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、パラメーターの数が少なくなり (通常は 2 未満)、コードの条件およびブロックが常に 1 つのコード行になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Here is an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に例を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>In X++, every protected and public method is an extension point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ では、すべての保護されたパブリック メソッドが拡張ポイントです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>By writing clean code, you automatically produce extensible code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クリーンなコードを記述することで、拡張可能コードを自動的に生成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the previous example, an extender can change how approval, confirmation, and rejection are implemented.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前の例では、拡張担当者が、承認、確認、および否認を実装する方法を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If the implementations had been inline, the code would not be extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装がインラインである場合、コードは拡張できません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Don't repeat yourself (DRY)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DRY 原則</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>To help prevent misalignment of implementations, avoid redundancy in your logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実装の不整合を防ぐため、ロジックで冗長性を避けてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>This principle is especially important in the case of extensible code, because the extender might not extend all required pieces and might therefore unintentionally leave the solution broken.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この原則は、拡張可能コードの場合は特に重要です。拡張担当者は、必要な部分をすべて拡張するとは限らないため、意図せずソリューションが壊れたままにする可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Best practices to create an extensible solution in X++</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">X++ で拡張可能ソリューションを作成するためのベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The following best practices can help you create extensible solutions in X++, so that consumers of your code can extend your solution:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以下のベスト プラクティスは、コードのユーザーがソリューションを拡張できるように、X++ で拡張可能なソリューションを作成するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source><bpt id="p1">[</bpt>Classes<ept id="p1">](extensible-classes.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>クラス<ept id="p1">](extensible-classes.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source><bpt id="p1">[</bpt>Methods<ept id="p1">](extensible-methods.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>方法<ept id="p1">](extensible-methods.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source><bpt id="p1">[</bpt>Forms<ept id="p1">](extensible-forms.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>フォーム<ept id="p1">](extensible-forms.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source><bpt id="p1">[</bpt>Extended data types<ept id="p1">](extensible-edts.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張データ型<ept id="p1">](extensible-edts.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source><bpt id="p1">[</bpt>Extensible enums<ept id="p1">](extensible-enums.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>拡張可能な列挙<ept id="p1">](extensible-enums.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source><bpt id="p1">[</bpt>Delegates<ept id="p1">](extensible-code-delegates.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>委任<ept id="p1">](extensible-code-delegates.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">[</bpt>Tables<ept id="p1">](extensible-tables.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>テーブル<ept id="p1">](extensible-tables.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt>Extensibility attributes for methods<ept id="p1">](extensibility-attributes.md)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>メソッドの拡張属性<ept id="p1">](extensibility-attributes.md)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Breaking changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重大な変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>When you make your solution extensible, you also help guarantee that you won't break extension points later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>For more information, see <bpt id="p1">[</bpt>Breaking changes<ept id="p1">](breaking-changes.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>重大な変更<ept id="p1">](breaking-changes.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>External resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外部リソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The following external resources can help you make sure that you're writing clean code:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の外部リソースは、クリーンなコードを作成しているかどうかを確認するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source><bpt id="p1">[</bpt>SOLID Principles<ept id="p1">](https://en.wikipedia.org/wiki/SOLID)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>SOLID の原則<ept id="p1">](https://en.wikipedia.org/wiki/SOLID)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><bpt id="p1">[</bpt>Pluralsight - Clean Code: Writing Code for Humans<ept id="p1">](https://www.pluralsight.com/courses/writing-clean-code-humans)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Pluralsight - クリーンなコード: 人間に適したコードの記述<ept id="p1">](https://www.pluralsight.com/courses/writing-clean-code-humans)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source><bpt id="p1">[</bpt>Clean Code: A Handbook of Agile Software Craftsmanship<ept id="p1">](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>クリーンなコード: アジャイル ソフトウェア作成者が守るべき事柄のハンドブック<ept id="p1">](https://www.amazon.com/Clean-Code-Handbook-Software-Craftsmanship/dp/0132350882)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source><bpt id="p1">[</bpt>Clean Coders<ept id="p1">](https://cleancoders.com/)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>Clean Coders<ept id="p1">](https://cleancoders.com/)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source><bpt id="p1">[</bpt>Don't repeat yourself<ept id="p1">](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>DRY 原則<ept id="p1">](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>