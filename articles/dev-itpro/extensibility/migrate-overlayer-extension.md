<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="migrate-overlayer-extension.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>migrate-overlayer-extension.2333a7.0dd2629923209dc1d10a3cb52a3bc2c70f536bfd.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>0dd2629923209dc1d10a3cb52a3bc2c70f536bfd</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\migrate-overlayer-extension.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Migrate from overlayering to extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイから拡張機能への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about migration from customizations that are based on overlayered code to customizations that are based on extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能の基準となるカスタマイズoverlayeredコードに基づいていますカスタマイズからの移行について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Migrate from overlayering to extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイから拡張機能への移行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Introduction</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">はじめに</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>When Microsoft Dynamics 365 for Finance and Operations was first released, we strongly recommended that extensions be used instead of overlayering for customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics 365 for Finance and Operations の最初のリリース時に、カスタマイズのオーバーレイの代わりに拡張機能を使用することを強くお勧めしました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Overlayering-based customizations have been migrated from release to release through code migrations, and many customizations of application code are still based on the overlayering of code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイヤーに基づくカスタマイズは、コードの移行を通じてリリースごとに移行され、アプリケーション コードの多くのカスタマイズは引き続きコードのオーバーレイヤーがベースとなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>For most partners, at least some of their solution is still based on overlaying, and some partners will have lots of overlayering across their solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのパートナーについては、少なくともソリューションの一部が引き続きオーバーレイに基づいており、および一部のパートナーはソリューション間でたくさんのオーバーレイを持ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The amount of work that is required to change an implementation from overlayered code to extensions depends on the code itself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイ コードから拡張への実装を変更するために必要な作業の金額は、そのコード自体によって異なります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Some overlayered code can be changed relatively seamlessly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのオーバーレイヤーされたコードは、比較的シームレスに変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>However, for some changes, you must rethink the customization to find an appropriate way to accomplish it through extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、いくつかの変更については、拡張機能によりそれを達成できるよう適切な方法を見つけるためのカスタマイズを再考する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>Therefore, it can be a major undertaking to change complete solutions where multiple places have overlayered code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、複数の場所にコードが重複している場合、完全なソリューションを変更することが大きな課題になる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Such an undertaking requires an investment in the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このような仕事には、ソリューションへの投資が必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>The upside of this investment is a more seamless upgrade process, because customization is now based on application programming interfaces (APIs) through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズは現在、拡張を介したアプリケーション プログラミング インターフェイス (API) に基づいているため、この投資のメリットはよりシームレスなアップグレード プロセスにあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>Additionally, a lengthy code upgrade process is no longer required as it was for overlayered code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、オーバーレイ コードの場合と同様に、長いコード アップグレード プロセスは不要になりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>More importantly, daily servicing of a running environment offers many benefits.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに重要なことに、実行中の環境を日々保守すると多くの利点があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The core application and extensions no longer have to be compiled together, and patching can be done by deploying precompiled assemblies.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コア アプリケーションと拡張機能をまとめてコンパイルする必要がなくなり、プリ コンパイルされたアセンブリをデプロイすることでパッチを適用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Therefore, customers can apply patches to their system in a relatively seamless manner, and the amount of downtime is minimized.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、顧客は比較的シームレスにシステムにパッチを適用することができ、ダウンタイムの量は最小限に抑えられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>However, there is work that must be done before this result can be achieved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、この結果が得られる前に行う必要がある作業があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>Although there are multiple ways to approach this task, we have gained experience through our close work with independent software vendors (ISVs) and value-added resellers (VARs) that have already started to migrate from overlayering to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このタスクには複数の方法がありますが、既にオーバーレイから拡張機能に移行を開始した独立系ソフトウェア ベンダー (ISV) および付加価値再販業者 (VAR) との緊密な連携を通じて経験を積んでいます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>In this topic, we share some of this experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックではこの体験の一部を共有します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>First things first</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要なものから順番に</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The task ahead is substantial, and we want to make sure that our shared investment pays dividends.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後の課題はかなりあり、私たちは共有投資が配当を支払うことを確実にしたいと考えています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Keep the goal in mind as you work through your customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズを通じて作業するため、目標に注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>When customization is done correctly, your solution has these qualities:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズが正しく完了したとき、ソリューションには次の品質が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>It has no intrusive customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">侵入的なカスタマイズはありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>It supports side-by-side deployment with other ISV solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他の ISV ソリューションと横に並べる配置をサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>It's resilient to changes in Microsoft code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft コードでの変更に対して復元力があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>It's resilient to changes in other ISV solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他の ISV ソリューションでの変更に対して復元力があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>It can be upgraded automatically to future versions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後のバージョンに自動的にアップグレードすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>This type of customization represents a fundamental shift of approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この種のカスタマイズは、アプローチが根本的に変化することを表しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Previously, the primary objective was to implement the functional requirements on the current version.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、主な目的は、現在のバージョンで機能の要件を実装するためのものでした。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>This objective was acceptable, because we knew that manual work was required in order to upgrade the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションをアップグレードするために手動作業が必要であることがわかっていたため、この目標は受け入れられました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Previously, great engineers minimized the manual upgrade cost.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">以前は、優れたエンジニアは、手動アップグレード コストを最小化していました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Now, <bpt id="p1">*</bpt>every<ept id="p1">*</ept> engineer must implement solutions that require <bpt id="p2">*</bpt>zero effort<ept id="p2">*</ept> to upgrade.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在は、<bpt id="p1">*</bpt>各<ept id="p1">*</ept>エンジニアがアップグレードの<bpt id="p2">*</bpt>労力をゼロ<ept id="p2">*</ept>にするソリューションを実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Staying on the right path</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">適切なパスに残る</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Cars are designed to be safe.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">自動車は安全であるように設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>However, they can't yet prevent accidents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、まだ事故を防ぐことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Accident prevention remains the driver's responsibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">事故防止は、ドライバーの責任です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Similarly, the development toolset is designed for extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、拡張機能用に開発ツールセットが設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>However, the toolset can't yet prevent every type of intrusive customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、侵入的なカスタマイズのすべてのタイプを防ぐことは、ツールセットにはまだできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>As an engineer, it's your responsibility to avoid intrusive customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">エンジニアとして、侵入的なカスタマイズを回避することは職責です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>Sometimes, you might find that you can reach your functional goal only by implementing intrusive customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、煩雑なカスタマイズを実装することによってのみ、機能の目標に到達できることがわかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>In this case, you should reach out to Microsoft to find a correct solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、正しい解決策を見つけるために Microsoft に問い合わせる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>You should not force your way forward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ご自分のやり方で進めないようにしてください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>Otherwise, customers who, for example, experience an outage of their service after an automated upgrade might realize that your solution isn't future-proof after all.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それ以外の場合、たとえば、自動アップグレード後にサービスの停止が発生した顧客が、ソリューションに結局将来性がないことに気づく可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Because a future-proof solution represents a competitive advantage, it's worth the extra effort to do it correctly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来性のあるソリューションは競合の利点を表しているため、それを正しく行うための特別な努力は価値があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>Obtain an overview of your code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの概要の取得</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>When you create an overview of your code, first consider analyzing each of your solutions independently instead of analyzing them all together.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの概要を作成するときは、ソリューションをまとめて分析するのではなく、各ソリューションの分析をまず検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>This approach might be practical even if different teams work on the individual solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法は、さまざまなチームが個々のソリューションで作業している場合でも実用的な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>By choosing one team that you will engage before the other teams, you can gain some experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">他のチームよりも前に関与するチームを 1 つ選択することで、いくらか経験を積むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>Experience is valuable, because it not only helps you analyze and plan the work, but also helps the team ramp up and become familiar with the extensibility model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">経験は、作業を分析し計画するのに役立つだけでなく、チームがランプアップして拡張性モデルに慣れることにも役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>Therefore, the experience that you and your team gain can become valuable "lessons learned" that you can apply to later solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、あなたとあなたのチームが得た経験は、後のソリューションにも適用できる貴重な「教訓」となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>We have gained practical experience both with ISVs that take each ISV solution in turn, and with ISVs that work as VARs and take customer solutions later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各 ISV ソリューションを順番に実行する ISVと、VAR として機能して顧客のソリューションを後で実行する ISV の両方について、実際的な経験を得ました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>No matter how the work is pieced together in solutions, you can use the <bpt id="p1">[</bpt>Customization Analysis Report (CAR)<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept> to get information about what has been overlayered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">どのような形で作業がソリューションにまとめられていても、<bpt id="p1">[</bpt>カスタマイズ分析のレポート (CAR)<ept id="p1">](../dev-tools/customization-analysis-report.md)</ept> を使用してオーバーレイされたものに関する情報を取得できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>This report is generated when you submit your solutions to the Code Migration tool on Microsoft Dynamics Lifecycle Services (LCS).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このレポートは、Microsoft Dynamics Lifecycle Services (LCS) のコード移行ツールにソリューションを提出すると生成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The report is in Microsoft Excel format and includes a list of all the places that have overlayered code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートは Microsoft Excel 形式で、重複したコードを持つすべての場所の一覧が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>You can use the report to both analyze and categorize all overlayered instances in your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポートを使用すると、ソリューションのすべてのオーバーレイ インスタンスの分析と分類の両方をすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>To obtain an overview, you might find it helpful to categorize each overlayered instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">概要を得るには、オーバーレイヤーされたそれぞれのインスタンスを分類すると便利です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The category that you apply to an overlayered instance should represent the approximate effort that is required in order to change the customization to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイされたインスタンスに適用するカテゴリは、カスタマイズを拡張に変更するために必要なおよその労力を表す必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Some customizations will be easily changed to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのカスタマイズは、拡張機能に簡単に変更されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>However, for other customizations, the change will be more difficult.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、その他のカスタマイズについては、変更がより難しくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>From our experience working with numerous ISVs, we have found that the following categories are a good starting point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さまざまな ISV を操作する経験から、次のカテゴリが良い出発点であることがわかりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Category</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カテゴリ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Description</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">説明</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Extensible enums</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張可能な列挙</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>You can add new enum values by using extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を使用して新しい列挙値を追加することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>For more information, see <bpt id="p1">[</bpt>Add an enum value<ept id="p1">](add-enum-value.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>列挙値の追加<ept id="p1">](add-enum-value.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Construct with throw</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">throw による構築</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Most construct methods are simple and can be extended by using post-event handlers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ほとんどのコンストラクト メソッドは単純で、ポストイベント ハンドラーを使用して拡張することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>However, some construct methods are more complex and throw an exception when no class is created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、一部の construct メソッドはより複雑であり、クラスを作成していないとき例外をスローします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Exposing members</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メンバーを公開</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>Member variables that have the <bpt id="p1">**</bpt>private<ept id="p1">**</ept> access modifier in their definition can't be accessed through extensions unless they become exposed through public methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">定義に<bpt id="p1">**</bpt>プライベート<ept id="p1">**</ept>のアクセス修飾子があるメンバー変数は、パブリック メソッドを通じて公開されない限り、拡張機能を通じてアクセスできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>You can request that we add access to members through extensions that currently have not been exposed for this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このために現在公開されていない拡張を通じて、メンバーに対するアクセス許可の追加を要求することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>Note that access to protected members is generally enabled through extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">保護されたメンバーへのアクセスは通常、拡張クラスを通じて有効になることに注意してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Data manipulation methods that don't raise DataEvents</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">DataEvents を発生させないデータ操作メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>In some places in the application, data methods such as <bpt id="p1">**</bpt>insert()<ept id="p1">**</ept> and <bpt id="p2">**</bpt>update()<ept id="p2">**</ept> don't call <bpt id="p3">**</bpt>super()<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションの一部の場所では、<bpt id="p1">**</bpt>insert()<ept id="p1">**</ept> および <bpt id="p2">**</bpt>update()<ept id="p2">**</ept> などのデータ メソッドは <bpt id="p3">**</bpt>super()<ept id="p3">**</ept> を呼び出しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>Therefore, the methods don't raise DataEvents to add extensions to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">したがって、これらのメソッドは、拡張機能を追加する DataEvents を生成しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>Microsoft plans to refactor the standard application so that it includes additional methods that enable extensions in these places.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、これらの場所で拡張機能を有効にする追加のメソッドが含まれるように、標準のアプリケーションのリファクターを計画しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>If you submit a request for Microsoft to add this, add any of the affected methods that you must currently overlayer, if those methods haven't already been accounted for.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを追加するために Microsoft の要求を送信する場合は、それらのメソッドがまだ転記されていない場合は、現在オーバーレイする必要がある影響を受けるメソッドのいずれかを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Extract method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの抽出</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>This category is for code changes in the middle of methods, which can't be made through chain of command.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカテゴリは、コマンドの連鎖ではできないメソッドの途中でのコード変更用です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>When you request a method extraction, be sure to specify which lines of a method to extract, and what the signature of the new method must be.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドの抽出を要求するときは、抽出するメソッドの行と、新規メソッドの署名を何にする必要があるかをかならず指定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>SQL statement operations</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL ステートメント操作</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>SQL statements that are written directly in the application code don't enable extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション コードで直接記述されている SQL ステートメントは、拡張機能を有効にしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>When you make a request to extend these SQL statements, be sure to explicitly specify what you must extend, such as a field list, <bpt id="p1">**</bpt>where<ept id="p1">**</ept> clauses, or ordering.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの SQL ステートメントの拡張を要求するときは、フィールド一覧、<bpt id="p1">**</bpt>WHERE<ept id="p1">**</ept> 句、または注文などの、拡張を必要とする内容を明示的に指定していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Metadata overlayering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータのオーバーレイ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Provide the Application Object Tree (AOT) path of the element where you believe the metadata (property value) must be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータ (プロパティ値) を変更する必要があると思われる要素のアプリケーション オブジェクト ツリー (AOT) のパスを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>Metadata changes can't be made through the current extension capabilities.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータの変更は、現在の拡張機能を通じて行うことはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Method overlayering</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッドのオーバーレイ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>This category is for customizations where a method is overlayered.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカテゴリは、メソッドがオーバーレイされているカスタマイズのためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>You should consider converting the overlayed method to an extension, so that changes are clean by extension not substitution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代替機能ではなく拡張機能ごとに変更がクリーンになるように、オーバーレイ メソッドを拡張機能に変換することを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Method signature changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド シグネチャの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>The capability to change method signatures through overlayering will be discontinued.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバレイによるメソッド シグネチャの変更機能は廃止されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>Other patterns for achieving similar results are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様の結果を実現するための他のパターンが必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>You can request changes to the standard signature to support extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張性をサポートするために、標準シグネチャへの変更を要求することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Be sure to include information about additional parameters that are required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な追加パラメーターについての情報が含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>Inventory dimensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫分析コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>You can no longer add dimensions by editing the macro and recompiling the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マクロを編集および標準アプリケーションのコンパイルでは、分析コードを追加することができなくなりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>Another approach will be offered that involves predefined dimensions that are deployed at runtime.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行時に配置される定義済分析コードに関連する別の方法が提供されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>This approach drives changes to existing customizations where new dimensions are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法では、新しいディメンションが追加される既存のカスタマイズに対する変更が行われます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Extensibility platform</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張性プラットフォーム</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Some customizations might not be possible through extensions unless new platform features are added.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのカスタマイズは、新しいプラットフォーム機能が追加されない限り、拡張機能から使用できない場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>If you determine that customizations can't currently be done through extensions, open an extensibility request that explains the scenario and what is required.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズが拡張機能を通じて現在実行できないと判断した場合は、シナリオと必要な内容を説明する拡張依頼を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>Reports</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Customizations of report designs have limited support for extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート デザインのカスタマイズでは、拡張性のサポートが限られています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>In general, a new report must be created.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般に、新しいレポートを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>Data provider classes can also be customized so that they include additional information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ プロバイダー クラスは、追加情報を含むようにカスタマイズすることもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>In some places, the standard application must be changed to enable this type of customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部の場所では、標準のアプリケーションを変更して、このタイプのカスタマイズを有効にする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>Other</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">外</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>This category is for overlayering instances that don't fit into any other category.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このカテゴリは、他のカテゴリに収まらないインスタンスをオーバーレイするためのものです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>By categorizing all overlaying code, you gain an overview of what must be changed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">オーバーレイするすべてのコードを分類することによって、変更が必要な対象の概要を得ることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Analyzing for impact and estimating work</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">影響の分析と作業の見積もり</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>In a typical approach to assessing work impact, you break down tasks into something tangible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">作業の影響を評価する標準的なアプローチでは、タスクを具体的なものに分割します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>This approach also applies to this work.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この方法はこの作業にも当てはまります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>The categories that were discussed in the previous section help frame similar customizations, and a first pass on estimates can be built by coming up with an overall estimate for each of these categories and similar categories that make up your solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションで説明したカテゴリは、同様のカスタマイズをフレームするのに役立ちます。また、これらのカテゴリおよびソリューションを構成する同様のカテゴリの全体的な見積もりを作成することで、見積もりの最初のパスを構築できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The group of customizations in a given category often has a few extremes that stand out, and it might be appropriate to establish estimates for these customizations individually.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したカテゴリのカスタマイズ グループには、いくつかの点で優れていることが多く、これらのカスタマイズの見積もりを個別に確立することが適切な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Consider that some customizations will require either a request to Microsoft to enable extensibility or significant refactoring of the customization so that it can be done through extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一部のカスタマイズでは、拡張性を有効にするために Microsoft への要求、または拡張性を介して行うことができるようにカスタマイズの大幅なリファクタリングが必要になることを考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>Both of these scenarios will increase the estimates for migrating the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの両方のシナリオはソリューションを移行するための見積を増加させます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>Customization that drives what are referred to as intrusive changes is often more complex to convert to extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">侵入的な変更を実行するカスタマイズは、拡張機能に変換する場合、より複雑な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>For these changes, you must consider what is the correct way to approach the customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更については、カスタマイズにアプローチする正しい方法を考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>Here are some examples of these changes:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの変更の例を次に示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>Customizations that request inline delegates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インライン デリゲートを要求するカスタマイズ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>Customizations of complex classes or methods such as <bpt id="p1">**</bpt>SalesLinetype<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>SalesLinetype<ept id="p1">**</ept> のような、複雑なクラスまたはメソッドのカスタマイズ。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>Changes to method signatures.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド シグネチャの変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Additions of inventory dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">在庫分析コードの追加。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Changes to report definitions and report data provider classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レポート定義およびレポート データ プロバイダー クラスの変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Intrusive changes to forms.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームへの侵入的な変更。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>For changes that require different approaches to make the customizations extension-based, you might have to log requests to Microsoft to enable extensibility.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズを拡張ベースにするための異なるアプローチが必要な変更については、拡張機能を有効にするため Microsoft にログ要求をする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>When creating your migration schedule, you'll need to take into account the delay of waiting for updates from Microsoft.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行スケジュールを作成するとき、Microsoft からの更新プログラム待ちの遅延を考慮する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>What is supported, and what requires an extensibility request?</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">何がサポートされるか、また何が拡張機能を必要とするか ?</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>When you review a customization, be sure to consider different options for converting it to an extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">カスタマイズを確認するときは、カスタマイズを拡張機能へ変換するための各種オプションをかならず考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>Be sure to consider whether a method is hookable, or whether it can be a class extension or form event.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フック可能なメソッドかどうか、またはクラス拡張かフォーム イベントかどうかを必ず考慮してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Review most of the currently available application code that is available to you.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">使用できる現在使用可能なアプリケーション コードの大部分を確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>You might conclude that a change to the standard application is required in order to enable the required extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な拡張子を有効にするために、標準アプリケーションへの変更が必要であると結論付ける可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>In this case, you must <bpt id="p1">[</bpt>log an extensibility request<ept id="p1">](extensibility-requests.md)</ept>  The request is then put into the backlog at Microsoft so that it can be addressed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、<bpt id="p1">[</bpt>拡張機能の要求を記録<ept id="p1">](extensibility-requests.md)</ept>する必要があります。この要求は対処できるように Microsoft のバックログに配置されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>Don't log extensibility requests by opening a request for a hotfix, because Microsoft doesn't release extensibility requests as hotfixes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は修正プログラムの機能拡張要求を解放しないので、修正プログラムの要求を開いて、拡張機能の要求をログないでください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>Be sure to supply enough contextual information in your extensibility requests.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能の要求には十分なコンテキスト情報を供給してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>For example, a request for an inline delegate might come from the current customization approach.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、インライン デリゲートの要求が、現在のカスタマイズ アプローチから来る可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>However, to better accommodate extension, the requirement that led to this customization might be better served by a structural change to the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ただし、より適切な拡張を行うため、このカスタマイズにつながなる要求は、標準アプリケーションへの構造的な変更によってより効果的になる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>We appreciate suggestions of this type, because they help move the application toward a better platform for building different customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この種のご提案は、アプリケーションをさまざまなカスタマイズを構築するためのより良いプラットフォームに近づけることに役に立ちますのでよろしくお願い致します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>Planning the migration</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">移行の計画</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Be sure to start planning the migration of your solutions early.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">早期にソリューションの移行を計画開始してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>This planning is important because it helps you make sure that you have room in your schedules to identify and log extensibility requests, and that you have room for the time delay before these requests become available in product releases.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この計画は、機能拡張要求を識別してログに記録するためのスケジュールに余裕があること、およびこれらの要求が製品リリースで利用可能になるまでの時間の余地があることを確認するのに役立つので重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Additionally, acknowledge that your developers might have to build new skills, and make sure that you cater to any required learning as part of the migration plan.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、開発者は、新しいスキルをビルドする可能性があることに同意し、移行計画の一部として必要な学習に対応するかどうかを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Your solution might contain intrusive customizations that aren't easily accommodated through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションに、拡張機能を通じて簡単に対応できない侵入的なカスタマイズが含まれていることがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>You should consider whether the business value of these customizations outweighs the effort of building them through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このようなカスタマイズの業務の値が拡張機能を通じて構築する手間を上回るかどうかを検討してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>In some cases, partners have decided to discontinue parts of their solutions, because they found that it was impractical to rebuild those parts through extensions, and those parts weren't critical to the solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">場合によっては、パートナーが拡張機能を通じてパーツを再構築することが困難で、それらのパーツはソリューションにとって重要ではないため、ソリューションのパーツを中止することを決定しました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>Some smaller fixes that you're customizing across the application might not be core for your solution, but they are important for the customers that you engage with.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション全体でカスタマイズする小規模な修正プログラムの一部は、ソリューションのコアでない場合がありますが、関係するユーザーにとって重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>In these cases, you must decide whether you prefer to ask Microsoft to implement similar capabilities in the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">そのような場合、標準アプリケーションに類似の機能を実装するよう Microsoft に依頼するほうがよいかどうかを決定する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can enter an extensibility request for this purpose.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この目的のために拡張性要求を入力することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>For example, if customers want to simplify standard business processes in the system, you might suggest that we add options for disabling steps of the process in the standard application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、顧客がシステムでの標準の業務プロセスを簡略化する場合、標準のアプリケーションでプロセスの手順を無効にするためのオプションを追加するよう、提案する可能性があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>