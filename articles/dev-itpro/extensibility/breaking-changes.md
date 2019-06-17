<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="breaking-changes.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>breaking-changes.e1297f.06bde311e2d272e20b0e088b28f7e3c01932809c.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>06bde311e2d272e20b0e088b28f7e3c01932809c</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\breaking-changes.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Breaking changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更の分割</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>This topic provides information about breaking changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、分割変更について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103">
          <source>Breaking changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">変更の分割</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>When you make your solution extensible, you also help guarantee that you won't break the extension points later.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションを拡張可能にすると、後で拡張ポイントを壊さずに済むことにもなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>A breaking change is any change that can break a consumer of your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">分割変更は、コードのユーザーを分割できる任意の変更です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This topic lists some of the types of changes that can break your code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このトピックでは、コードを分割できる変更のタイプを一覧表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>This list isn't exhaustive.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このリストは、包括的ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Other types of changes that aren't listed here could also be breaking changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここに登録されていない他のタイプの変更が分割変更となることもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Data model changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ モデルの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>General</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">一般</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>If any data model change requires that a data upgrade script be run, consumers might no longer be able to synchronize their data model, or they might lose access to data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ モデルの変更で、データ アップグレード スクリプトを実行する必要がある場合は、ユーザーがデータ モデルを同期できなくなったり、データにアクセスできなくなる可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Data types</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ型</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source><bpt id="p1">**</bpt>Changing an enumeration (enum) from extensible to non-extensible<ept id="p1">**</ept> – Consumers might have extensions to the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙を拡張可能から拡張不可に変更する<ept id="p1">**</ept>: ユーザーは、列挙の拡張を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source><bpt id="p1">**</bpt>Changing an enum from non-extensible to extensible<ept id="p1">**</ept> – Consumers might be using the enums in comparisons.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙を拡張不可から拡張可能に変更する<ept id="p1">**</ept>: ユーザーは、比較で列挙を使用している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>For more details, see <bpt id="p1">[</bpt>Write extensible enums<ept id="p1">](extensible-enums.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、<bpt id="p1">[</bpt>拡張可能な列挙の記述<ept id="p1">](extensible-enums.md)</ept>を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source><bpt id="p1">**</bpt>Decreasing the decimal precision of an extended data type (EDT) of the real type<ept id="p1">**</ept> – Consumers might have dependencies on the ability to enter data that uses the precision.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>実数型の拡張データ型 (EDT) の小数点以下の精度を下げる<ept id="p1">**</ept>: ユーザーは、精度を使用するデータを入力する機能に依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source><bpt id="p1">**</bpt>Decreasing the size of an EDT of the string type<ept id="p1">**</ept> – Consumers might have dependencies on the size of the string.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>文字列型の EDT のサイズを小さく<ept id="p1">**</ept>: ユーザーは文字列のサイズに依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source><bpt id="p1">**</bpt>Specializing the EDT by making it extend another EDT<ept id="p1">**</ept> – Consumers might have string length or decimal precision extensions to the EDT.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>別の EDT を拡張することにより EDT を特殊化する<ept id="p1">**</ept>: ユーザーは、文字列の長さ、または EDT への小数点以下の精度の拡張を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source><bpt id="p1">**</bpt>Changing the enum type of an EDT of the enum type when the enum is extensible<ept id="p1">**</ept> – Consumers might have extensions to the enum.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>列挙が拡張可能な場合に、列挙型の EDT の列挙型を変更する<ept id="p1">**</ept>: ユーザーは、列挙の拡張を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>Data model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source><bpt id="p1">**</bpt>Making a table obsolete and stopping information from being entered in the table<ept id="p1">**</ept> – Consumers might have a dependency on the table that information is entered in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブルを古い形式にし、情報がテーブルで入力されないようにする<ept id="p1">**</ept>: ユーザーは、情報が入力されるテーブルで依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source><bpt id="p1">**</bpt>Making a table field obsolete and stopping information from being entered in the field<ept id="p1">**</ept> – Consumers might have a dependency on the field that information is entered in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールドを古い形式にし、情報がフィールドで入力されないようにする<ept id="p1">**</ept>: ユーザーは、情報が入力されるフィールドで依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source><bpt id="p1">**</bpt>Renaming a field group<ept id="p1">**</ept> – Consumers might have extensions to field group, or code or metadata dependencies to it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド グループの名前を変更する<ept id="p1">**</ept>: ユーザーは、フィールド グループへの拡張、またはコードまたはメタデータの依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source><bpt id="p1">**</bpt>Changing constraints or indexes<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>制約またはインデックスの変更<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source><bpt id="p1">**</bpt>Making a table map obsolete and stopping the table map from being used<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル マップを古い形式にし、テーブル マップが使用されないようにする<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source><bpt id="p1">**</bpt>Make a table map field obsolete<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル マップ フィールドを古い形式にする<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source><bpt id="p1">**</bpt>Adding a table map field<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル マップ フィールドを追加する<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source><bpt id="p1">**</bpt>Removing a table map field mapping<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>テーブル マップ フィールド マッピングを削除する<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source><bpt id="p1">**</bpt>Making a data entity obsolete<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ エンティティを古い形式にする<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source><bpt id="p1">**</bpt>Making a data entity field obsolete<ept id="p1">**</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>データ エンティティ フィールドを古い形式にする<ept id="p1">**</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Code changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Class members</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス メンバー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source><bpt id="p1">**</bpt>Deleting or renaming public or protected class-level members<ept id="p1">**</ept> – Consumers might be using these members in the extension classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パブリックまたは保護されたクラス レベルのメンバーを削除するか名前を変更する<ept id="p1">**</ept>: ユーザーは、拡張クラスでこれらのメンバーを使用している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source><bpt id="p1">**</bpt>Changing a class member from public or protected to protected or private<ept id="p1">**</ept> – Consumers might have queried or assigned values to the field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラス メンバーをパブリックまたは保護から保護またはプライベートに変更する<ept id="p1">**</ept>: ユーザーは、フィールドに値をクエリ済みまたは割り当て済みの可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Classes and interfaces</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスおよびインターフェイス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source><bpt id="p1">**</bpt>Adding an abstract method to a class<ept id="p1">**</ept> – Consumers might have created a derived type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスに抽象メソッドを追加する<ept id="p1">**</ept>: ユーザーは、派生タイプを作成した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source><bpt id="p1">**</bpt>Adding final to a class<ept id="p1">**</ept> – Consumers might have created a derived type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>クラスに最終を追加する<ept id="p1">**</ept>: ユーザーは、派生タイプを作成した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source><bpt id="p1">**</bpt>Adding a method to an interface<ept id="p1">**</ept> – Consumers might have implemented the interface on their own type.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドをインターフェイスに追加する<ept id="p1">**</ept>: 消費者は、独自の種類でインターフェイスを実装した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source><bpt id="p1">**</bpt>Making a public class obsolete and stopping instantiation of the class<ept id="p1">**</ept> – Consumers might have overridden, wrapped, or subscribed to the instance methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パブリック クラスを古い形式にし、クラスのインスタンス化を停止する<ept id="p1">**</ept>: ユーザーは、インスタンス メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>Methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source><bpt id="p1">**</bpt>Changing the access modifier from protected or public to another access modifier<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アクセス修飾子を保護またはパブリックから別のアクセス修飾子に変更する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source><bpt id="p1">**</bpt>Making a concrete public or protected method abstract<ept id="p1">**</ept> – Consumers might have subclasses to the class, and those subclasses might not have implemented the method, or they might even call super.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>具体的なパブリックまたは保護されているメソッドを抽象的にする<ept id="p1">**</ept>: ユーザーは、クラスへのサブクラスを持っており、それらのサブクラスがメソッドを実装していないか、上位を呼び出す可能性もあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source><bpt id="p1">**</bpt>Renaming method parameters<ept id="p1">**</ept> – Consumers might have dependencies on parameters by name (via arguments or externally from C<ph id="ph1">\#</ph>, for example).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッド パラメーターの名前を変更する<ept id="p1">**</ept>: ユーザーは、名前によるパラメーターの依存関係を持っている可能性があります (引数または C<ph id="ph1">\#</ph> から外部でなど)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>Adding, removing, or changing the type of a method parameter on a protected or public method<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護またはパブリック メソッドでメソッド パラメーターのタイプを追加、削除、または変更する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>Adding or removing a default method parameter on a protected or public method<ept id="p1">**</ept> – Consumers might have wrapped or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護またはパブリック メソッドで既定のメソッド パラメーターを追加または削除する<ept id="p1">**</ept>: ユーザーは、メソッドを折り返しまたはサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source><bpt id="p1">**</bpt>Changing the return type of a method<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドの戻り値の型を変更する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">**</bpt>Adding Hookable(false) to a protected or public method<ept id="p1">**</ept> – Consumers might have wrapped or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護またはパブリック メソッドに Hookable(false) を追加する<ept id="p1">**</ept>: ユーザーは、メソッドを折り返しまたはサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source><bpt id="p1">**</bpt>Adding Wrappable(false) to a protected or public method<ept id="p1">**</ept> – Consumers might have wrapped the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護またはパブリック メソッドに Wrappable(false) を追加する<ept id="p1">**</ept>: ユーザーは、メソッドを折り返した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source><bpt id="p1">**</bpt>Removing Hookable(true) from a private or protected method<ept id="p1">**</ept> – Consumers might have subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライベートまたは保護メソッドから Hookable(true) を削除する<ept id="p1">**</ept>: ユーザーは、メソッドをサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source><bpt id="p1">**</bpt>Removing Wrappable(true) from a private method<ept id="p1">**</ept> – Consumers might have wrapped the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プライベートまたは保護メソッドから Wrappable(true) を削除する<ept id="p1">**</ept>: ユーザーは、メソッドを折り返した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source><bpt id="p1">**</bpt>Removing Replaceable(true) from a method<ept id="p1">**</ept> – Consumers might have conditionally wrapped the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドから Replaceable(true) を削除する<ept id="p1">**</ept>: ユーザーは、条件付きでメソッドを折り返した可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source><bpt id="p1">**</bpt>Adding final to a protected or public method<ept id="p1">**</ept> – Consumers might have overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>保護またはパブリック メソッドに最終を追加する<ept id="p1">**</ept>: ユーザーは、メソッドをオーバーライド、折り返し、またはサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source><bpt id="p1">**</bpt>Changing a method from instance to static or from static to instance<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>インスタンスから静的または静的からインスタンスにメソッドを変更する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、サブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source><bpt id="p1">**</bpt>Making a method obsolete and stopping invocation of the method<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドを古い形式にし、メソッドの呼び出しを停止する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブしている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source><bpt id="p1">**</bpt>Changing the responsibility of a method<ept id="p1">**</ept> – Consumers might have called, overridden, wrapped, or subscribed to the method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドの責任を変更する<ept id="p1">**</ept>: ユーザーは、メソッドを呼び出し、オーバーライド、折り返し、またはサブスクライブした可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source><bpt id="p1">**</bpt>Removing the reference to a method<ept id="p1">**</ept> – Consumers might have overridden, wrapped, or subscribed to the method, and they might expect their logic to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メソッドへの参照を削除する<ept id="p1">**</ept>: ユーザーは、メソッドをオーバーライド、折り返し、またはサブスクライブしている可能性があり、ロジックが実行されることを期待している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>Delegates</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">委任</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source><bpt id="p1">**</bpt>Making any change in signature<ept id="p1">**</ept> – Consumers might have subscribed dynamically.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>シグネチャで変更を行う<ept id="p1">**</ept>: ユーザーは、動的にサブスクライブしている場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source><bpt id="p1">**</bpt>Removing the reference to a delegate<ept id="p1">**</ept> – Consumers might have subscribed, and they might expect their logic to run.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デリゲートへの参照を削除する<ept id="p1">**</ept>: ユーザーは、サブスクライブしている可能性があり、ロジックが実行されることを期待している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>Label changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラベルの変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source><bpt id="p1">**</bpt>Modifying or deleting a label<ept id="p1">**</ept> – Consumers might be using the label in the current context of the label text and the parameters that were passed, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ラベルを変更または削除する<ept id="p1">**</ept>: ユーザーは、ラベル テキストの現在のコンテキストにあるラベルと渡されたパラメーターなどを使用している可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>We recommend that, going forward, you add new labels in the event of a label change.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今後は、ラベルの変更が発生した場合は新しいラベルを追加することをお勧めします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>Application element changes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーション要素の変更</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source><bpt id="p1">**</bpt>Removing any element<ept id="p1">**</ept> – Consumers might have a compile time dependency on the existence of the element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>要素を削除する<ept id="p1">**</ept>: ユーザーは、要素の存在にコンパイル時間の依存関係を持っている可能性があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>Metadata extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">メタデータの拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source><bpt id="p1">**</bpt>Not following the naming guidelines for metadata or augmentation classes<ept id="p1">**</ept> – Consumers might have elements that have the same name.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>メタデータまたは拡張クラスの名前付けガイドラインに従わない<ept id="p1">**</ept>: ユーザーは、同じ名前を持つ要素を持っている可能性があります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>