<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="inventory-dimensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>inventory-dimensions.8405aa.c7351337f64fdf62c6206aed174f203df3bfef17.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>c7351337f64fdf62c6206aed174f203df3bfef17</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\inventory-dimensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Add new inventory dimensions through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を通じた新しい在庫分析コードの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic describes how to add new inventory dimensions through extensions in Microsoft Dynamics 365 for Finance and Operations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、Microsoft Dynamics 365 for Finance and Operations の拡張機能を通じて新しい在庫分析コードを追加する方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Add new inventory dimensions through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能を通じた新しい在庫分析コードの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>This topic provides a high-level overview of how to add new inventory dimensions through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、拡張機能を使用して新しい在庫分析コードを追加する方法の概要を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>It also includes information about how to access a sample application that contains an actual implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、実際の実装を含むサンプル アプリケーションへのアクセス方法に関する情報も含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>Solution overview</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>The cornerstone in this solution is that multiple roles participate in the life cycle of adding new inventory dimensions through extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このソリューションで重要なことは、複数のロールが、拡張機能を介して新しい在庫分析コードを追加するライフサイクルに参加することです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>The following description simplifies and generalizes this solution, however, in real life there is overlap between the roles, and sometimes it might even be the same person filling several roles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の説明では、このソリューションを簡略化して一般化していますが、現実にはロールの重複があり、時には同じ人が複数のロールを果たす場合もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Microsoft's role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft のロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Microsoft provides a finite set of unused dimension fields.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、使用されていない分析コード フィールドの限定的なセットを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>In addition to the 15 existing dimensions, Microsoft supports 10 generic dimensions:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">15 の既存の分析コードに加えて、Microsoft は 10 の一般的な分析コードをサポートします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>8 string-based</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">8 つの文字列ベース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>1 real-based</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">リアルベース 1 つ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>1 utcdatetime-based</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">utcdatetime ベース 1 つ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>This brings the total number of inventory dimensions in the standard application to 25:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、標準アプリケーションのインベントリ ディメンションの合計数が 25 になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>4 product dimensions: Color, Size, Style, and Config</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">4 製品分析コード: 色、サイズ、スタイル、およびコンフィギュレーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>5 tracking dimensions: Serial, Batch, Owner, Profile (Russia only), and GTD (Russia only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">5 つの追跡用分析コード: シリアル、バッチ、所有者、プロファイル (ロシアのみ)、および GTD (ロシアのみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>6 storage dimensions: Site, Warehouse, Location, Status, License Plate, and Pallet (for upgrade and migration only)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">6. 保管分析コード: サイト、倉庫、場所、ステータス、ライセンス プレートおよびパレット (アップグレードと移行のみ)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>10 unassigned generic dimensions: InventDimension1 to InventDimension10</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">10 個の未割り当ての一般的な分析コード: InventDimension10 から InventDimension1</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Microsoft provides the physical schema.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft は、物理スキーマを提供しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>ISV role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV 役割</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>The ISV adds new inventory dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV は、新規在庫分析コードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The ISV solution provides all the specific functionality for the dimension - it must be strong-typed, maintainable, testable, and performant.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV ソリューションは、分析コードの特定のすべての機能を提供します。強力な種類で、管理、テストしやすく、パフォーマンスの高いものでなければなりません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>In addition, the solution must be agnostic to other ISV's solutions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">さらに、ソリューションは、その他の ISV のソリューションに依存しないようにする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The ISV builds a solution that doesn't reference the physical schema directly, but goes through an indirection, which can be done seamlessly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV は、物理スキーマを直接参照せず、シームレスに行うことができる間接参照を通過するソリューションを構築します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>The ISV provides the logical implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV は、論理実装を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>VAR role</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VAR ロール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>The VAR must be able to deliver a fully functional system to a customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VAR は、完全に機能するシステムを顧客に出荷できる必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>The system can contain solutions from multiple ISV's - each potentially containing new inventory dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">システムには、複数の ISV のソリューションを含めることができます。それぞれに新しい在庫分析コードが含まれる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>In total, up to 10 ISV dimension fields are supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">合計で最大 10 個の ISV 分析コード フィールドがサポートされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The VAR provides the binding between the physical data model and logical implementation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VAR により、物理的データ モデルと論理的実装が結合されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Details</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">細目</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>The first half of the solution is straight forward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの前半はシンプルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>A new class hierarchy is introduced.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいクラス階層が導入されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Each new dimension must be implemented in a new class deriving from either InventProductDimension or InventTrackingDimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それぞれの新しい分析コードは、InventProductDimension または InventTrackingDimension のいずれかから派生する新しいクラスに実装する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Currently, there is no support for storage dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在、保管分析コードのサポートがされていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>With this, ISVs can introduce new dimensions without having to change any of the logic on the InventDim table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを使用すると、ISV は InventDim テーブルのロジックを変更せずに新しい分析コードを導入することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>InventDimensionClassHierarchy</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDimensionClassHierarchy</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>To reference the new dimension in a strongly-typed fashion, the ISV introduces a table extension class to the InventDim table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">厳密に型指定された新しい分析コードを参照するために、ISV では InventDim テーブルにテーブル拡張クラスが導入されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The extension classes for Style, Color, and Size can be used as templates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">スタイル、色、サイズの拡張クラスをテンプレートとして使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Example: InventDimStyle_Extension<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>例: InventDimStyle_Extension<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The dimensions can be referenced like this.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分析コードは、次のように参照することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>The ISV can now build logic, including the data model and user interface for maintaining the list of dimension values, for the new inventory dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV は、新しい在庫分析コードの分析コード値のリストを保持するために、データ モデルおよびユーザー インターフェイスなどのロジックを構築できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>The second half of the solution is the data model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの後半はデータ モデルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>The standard application will contain the following for each new dimension:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">標準アプリケーションには、新しい分析コードごとに次の内容が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>A label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベル ファイル。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>A configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キー。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>Two extended data types (EDTs) (for the field on InventDim and for the flag on InventDimParm).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">2 つの拡張データ型 (EDT) (InventDim のフィールド用と InventDimParm のフラグ用) です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>One field on InventDim table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDim テーブルの 1 つのフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>One field on InventDimParm table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDimParm テーブルの 1 つのフィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>One field on InventDimFieldMap map and one field on each of the tables (approximately 30) mapped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDimFieldMap マップの 1 つのフィールドと、各テーブルの 1 つのフィールド (約 30) がマップされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>The VAR's job is to wire the ISV solutions to the available dimension fields on InventDim for a given customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VAR の職務は、特定の顧客の InventDim の分析コード フィールドに ISV ソリューションを書き込むことです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>To minimize this work, it currently includes the following:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この作業を最小にするために、現在以下が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Implement the binding mapping.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">バインディング マッピングを実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>This is accomplished by extending the method InventDimFieldBinding.className2FieldName().</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、メソッド InventDimFieldBinding.className2FieldName() メソッドを拡張するよって行います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>Enable the configuration key.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンフィギュレーション キーを有効にします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Extend the EDT to specify the right string size.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右側の文字列のサイズを指定するには、EDT を拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Extend the Label file, such as copy the ISV-provided labels into the correct label file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV 製ラベルを正しいラベル ファイルにコピーするなど、ラベル ファイルを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>Extend the ProductDimensions or TrackingDimensions field groups on InventDim, and a few other tables, depending on the type of dimension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDim の ProductDimensions または TrackingDimensions フィールド グループおよび分析コードのタイプに応じていくつかの他のテーブルを拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Extend relations and index as needed on InventDim.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">関係およびインデックスを必要に応じて、InventDim で拡張します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>InventDimensionISVVARExtensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDimensionISVVARExtensions</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Known issues</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既知の問題</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>There are some technical limitations influencing the design of the solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの設計に影響を与えるいくつかの技術的な制限があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>The most significant is the SQL statements throughout the application that contain where-clauses on InventDim.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最も重要なのは、InventDim のWhere 句を含むアプリケーション全体の SQL 文です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Most of these are implemented using macros, which doesn't change the fact that SQL statements are not extensible.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのほとんどはマクロを使用して実装され、SQL ステートメントが拡張可能ではないという事実を変更しません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Many of the SQL statements could be rewritten to use query objects to make them extensible, however many delete_from and update_recordset would remain.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">SQL ステートメントの多くは書き換えることができ、クエリ オブジェクトを使用して拡張できますが、多くの delete_from および update_recordset は残ります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>A viable solution cannot require changes to these SQL statements when adding new dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行可能なソリューションは、新しい分析コードを追加するときに、これらの SQL ステートメントへの変更を要求することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Another technical limitation is the amount of inventory dimensions that can be supported.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">もう 1 つの技術的な制限は、サポートできる在庫分析コードの量です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Each adds a small overhead, and the InventDimFixed EDT sets an upper limit at 32.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">それぞれが小さなオーバーヘッドを追加し、InventDimFixed EDT は上限を 32 に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>This EDT contains a bit mask for each dimension, and because the EDT is an integer, the limit is 32.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この EDT には各分析コードのビットマスクが含まれており、EDT は整数であるため制限は 32 です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>The provided solution stays within the limit of 32.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定されたソリューションは 32 の制限内で保持されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>If required in the future, InventDimFixed could be changed to be an Int64, a container, or it could be removed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">将来に必要になる場合、InventDimFixed を Int64、コンテナーに変更するまたは削除することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Sample application</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル アプリケーション</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>A sample application called "Product flavor dimension sample app" can be found on <bpt id="p1">[</bpt>GitHub<ept id="p1">](https://github.com/Microsoft/Product-flavor-dimension-sample-app)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">「製品フレーバーの分析コード サンプル アプリケーション」と呼ばれるサンプル アプリケーションは、<bpt id="p1">[</bpt>GitHub<ept id="p1">](https://github.com/Microsoft/Product-flavor-dimension-sample-app)</ept> で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>This sample consists of three models:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例は 3 つのモデルで構成されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>ISV production code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV の生産コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source>ISV test code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ISV テスト コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>VAR integration code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VAR 統合コード</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>Together these models provide a great starting point for implementing new inventory dimensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらのモデルを組み合わせると、新しい在庫分析コードを実装するための出発点となります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>The sample application introduces a new product dimension: Flavor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サンプル アプリケーションでは、Flavor という新しい製品ディメンションが導入されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>The application supports many end-to-end business scenarios, for example creating, buying, and selling items with various flavors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションでは、さまざまなフレーバーの品目の製造、購入、販売などの多くのエンド ツー エンドのビジネス シナリオがサポートされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>If needed, please log issues directly in GitHub, and feel free to contribute to the sample application to provide additional coverage.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要な場合は、問題を GitHub に直接記録し、追加の補充を提供するサンプル アプリケーションへ自由に投稿してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>InventDimensionFlavorScreenshot</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">InventDimensionFlavorScreenshot</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>