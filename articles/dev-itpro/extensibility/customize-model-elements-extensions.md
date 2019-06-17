<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="customize-model-elements-extensions.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>customize-model-elements-extensions.2e271a.739033a750925d948039e3ed52eee33336d2e56e.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>739033a750925d948039e3ed52eee33336d2e56e</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\extensibility\customize-model-elements-extensions.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Customize model elements through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能によってモデル要素をカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you’ll become familiar with the Fleet Management Extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>To demonstrate the extension capabilities of Dynamics AX, this model contains elements that extend the functionality of the Fleet Management application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX の拡張機能を示すために、このモデルにはフリート管理アプリケーションの機能を拡張する要素が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Customize model elements through extension</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能によってモデル要素をカスタマイズする</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this tutorial, you’ll become familiar with the Fleet Management Extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>This model contains elements that extend the functionality of the Fleet Management application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このモデルには、フリート管理アプリケーションの機能を拡張する要素が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>You can customize model elements by creating <bpt id="p1">*</bpt>extensions<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>拡張機能<ept id="p1">*</ept> を作成することにより、モデル要素をカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Unlike the overlayering capabilities of Microsoft Dynamics AX 2012, extensions don’t overlay the baseline model elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX 2012 の オーバーレイ機能とは異なり、拡張機能はベースライン モデル要素をオーバーレイしません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>Instead, extensions are compiled as a separate assembly that adds to or customizes the model and the associated business logic.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代わりに、拡張機能はモデルと関連付けられているビジネス ロジックに追加またはカスタマイズする別のアセンブリとしてコンパイルされます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>You can extend metadata, for example, by adding a field to a table or adding a control to a form, and also extend or customize business logic by defining event handlers and plug-in classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブルにフィールドを追加、またはフォームにコントロールを追加することなどによりメタデータを拡張、およびイベント ハンドラおよびプラグイン クラスを定義することによりビジネス ロジックを拡張またはカスタマイズすることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>You can now author event handlers on several pre-defined events on tables, forms, form data sources, form controls, and others.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、フォーム、フォーム データ ソース、フォーム コントロール、およびその他を使用して、様々な定義済みイベントでイベント ハンドラーを作成することができるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>Plug-ins are also a new extensibility concept that enables replacing or extending the business logic of the application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグインは、アプリケーションのビジネス ロジックを交換または拡張するできるようにする新しい機能拡張の概念でもあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前提条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>This tutorial requires you to access the environment using Remote Desktop, and that you be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Understanding the Fleet Management model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理モデルを理解する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>The Fleet Management application provides a rental car company a system for managing vehicles, customers and vehicle reservations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理アプリケーションは、車両、顧客、および車両予約を管理するためのシステムをレンタル自動車会社に提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>The application is designed for use by the Fleet Clerk and Fleet Manager personas.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションは、フリート係とフリート マネージャの役割で使用されるよう設計されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>Fleet Clerk</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート係</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>The Clerk is the front desk employee who handles the face-to-face and over-the-phone interactions with customers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">担当者は、顧客との対面または電話でのやり取りを処理する受付従業員です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>The Clerk is primarily concerned with entering customer information into the application, creating vehicle reservations for customers, upselling the reservation by offering vehicle accessories, and processing vehicle returns upon completion of a vehicle rental.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">担当者は主に、アプリケーションに顧客情報を入力する、顧客の車両予約を作成する、車両アクセサリをオファーすることで予約をアップセルする、車両レンタルの終了時に車両の返却を処理することに関心を持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>The Clerk spends the vast majority of their time using the <bpt id="p1">**</bpt>Fleet Management Workspace<ept id="p1">**</ept> to prepare for interactions with customers by anticipating their needs and providing a pleasant and memorable experience, while interacting with the customer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">担当者は、各自のニーズを予測し、楽しくて印象的なエクスペリエンスを提供しながら、顧客とやり取りすることにより、<bpt id="p1">**</bpt>フリート管理ワークスペース<ept id="p1">**</ept>を使用して顧客とのやり取りを準備することに大部分の時間を費やします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Fleet Manager</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート マネージャー</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>The Manager is the back office employee who handles setting business requirements and processes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マネージャーは、業務要件とプロセスの設定を処理するバック オフィス従業員です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>The Manager is primarily concerned with entering vehicle information, defining the available vehicle accessories, vehicle maintenance, determining pricing, and analyzing business performance measures such as revenue, upsell success, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">マネージャーは、車両の情報を入力する、使用可能な車両アクセサを定義する、車両メンテナンス、価格を決定する、および収益、アップセルの成功などのビジネス パフォーマンス測定を分析することに主に関心を持っています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>The application's business logic revolves around the following three primary entities and the relationships between them.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アプリケーションのビジネス ロジックは、次の 3 つの主なエンティティとそれらの間の関係を中心に展開されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>Customers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Customers contact the Fleet Clerk to make vehicle reservations, choose vehicle accessories, check out and return vehicles, and pay for vehicle rentals.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客は、車両の予約を行い、車両のアクセサリを選択し、車両をチェックアウトおよび返却をし、車両のレンタル料を支払うためにフリート係に連絡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>Customer-related information is stored in the table named <bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">顧客関連の情報は、<bpt id="p1">**</bpt>FMCustomer<ept id="p1">**</ept> というテーブルに保管されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Vehicles</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">車両及び運搬具</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>Vehicles vary primarily in their price, which is proportional to the vehicle <bpt id="p1">*</bpt>class<ept id="p1">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">車両は主として価格が異なり、車両の<bpt id="p1">*</bpt>クラス<ept id="p1">*</ept>に比例します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>The names of tables that store information about vehicles begin with "FMVehicle".**</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">車両に関する情報を格納するテーブルの名前は、「FMVehicle」で始まります。**</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Reservations and rentals</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引当とレンタル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Reservations handle the relationship between customers and vehicles.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引当は、顧客および車両間の関係を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>Reservation information includes reservation dates, customer information, vehicle selection and price, and additional charges such as accessories or fees.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引当情報には、引当日、顧客情報、車両の選択と価格、およびアクセサリや手数料などの追加の雑費が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>Reservation and rental information is stored in the <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> and <bpt id="p2">**</bpt>FMRentalCharge<ept id="p2">**</ept> tables.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">引当やレンタル情報は、<bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> および <bpt id="p2">**</bpt>FMRentalCharge<ept id="p2">**</ept> テーブルに格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>A calculation engine handles the transactional information related to the pricing of vehicle reservations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算エンジンは、車両予約の価格決定に関連するトランザクションの情報を処理します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Using this data model the Fleet Management application provides a basic car rental experience.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデータ モデルを使用すると、フリート管理アプリケーションは基本的な自動車レンタル経験を提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Extending the Fleet Management model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理モデルを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>The basic Fleet Management application has been customized with additional capabilities that enable a rental car company to provide pricing incentives to its customers through discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本的なフリート管理アプリケーションは、追加機能でカスタマイズされています。これらの機能によりレンタカー会社は、割引を使用して顧客に価格インセンティブを提供することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>The additional business logic and data that enables these discount capabilities is stored in the Fleet Management Extension model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの割引機能を使用可能にする追加のビジネス ロジックおよびデータは、フリート管理拡張モデルに格納されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>The discount capabilities add value to the Fleet management application through three primary customizations.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引機能は、3 つの主要なカスタマイズを介してフリート管理アプリケーションに価値を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>The Fleet Management Extension data model</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理拡張モデル</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Two new tables have been added that store discount-related information.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引に関連する情報を格納する 2 つの新しいテーブルが追加されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source><bpt id="p1">**</bpt>FEDiscounts<ept id="p1">**</ept> stores the list of all discounts and their rates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FEDiscounts<ept id="p1">**</ept> には、すべての割引とその料金のリストが保存されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source><bpt id="p1">**</bpt>FERentalDiscountRelationTable<ept id="p1">**</ept> keeps track of the reservations that the discounts are applied to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FERentalDiscountRelationTable<ept id="p1">**</ept> は割引が適用される引当を追跡します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>Existing tables have been extended to account for the addition of discounts to the pricing scheme.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のテーブルは、価格設定スキームへの割引口座に拡張されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source>The table that keeps track of the vehicle rate for a particular reservation, named <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept>, has been extended to accommodate discounts to the vehicle rate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> という特定の予約の車両料金を追跡するテーブルは、車両料金の割引に対応するように拡張されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>The table that keeps track of the accessories for a reservation, named <bpt id="p1">**</bpt>FMRentalCharge<ept id="p1">**</ept>, has been extended to accommodate discounts applied to accessories.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRentalCharge<ept id="p1">**</ept> という予約のアクセサリーを追跡しているテーブルは、アクセサリーに適用される割引に対応するために拡張されました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>The Fleet Management Extension Calculation Engine</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理拡張計算エンジン</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The basic calculation engine has been customized to add the various pricing schemes defined by the new discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本的な計算エンジンには、カスタマイズにより、新しい割引によって定義されたさまざまな価格決定スキーマが追加されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>A plug-in class has replaced the functionality of the base calculation engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン クラスによって、基本計算エンジンの機能が置き換えられました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>When a vehicle is reserved for more than 7 days, the vehicle Fleet Management model calculates savings based on the difference between a vehicle's daily rate and a lower weekly rate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">車両の予約が 7 日間を超えるときは、車両フリート管理モデルが、車両の 1 日当たりの料金とより低い 1 週間あたりの料金との差に基づいて、節約を計算します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>The plug-in removes the weekly-rate calculation because this same behavior can be accomplished by using discounts.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグインは、同じ動作を割引を使用して実現できるため、1 週間あたりの料金の計算を削除します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>The Fleet Management User Interface Extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理ユーザー インターフェイス拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>The Rental, which is contained by the form named <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept>, has been extended to enable the Clerk to apply discounts to a reservation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> という名前のフォームに組み込まれている Rental は、担当者が予約に割引を適用できるように拡張されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>The on-screen price summary is updated in real time with savings information related to discounts that can be applied to vehicles and accessories related to the reservation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">画面上の価格の概要は、予約に関連する車両およびアクセサリに適用可能な割引に関する貯蓄情報によってリアルタイムで更新されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source>In the following steps, you'll explore the customizations that have been made in the Fleet management Extension model, as well as re-implement a portion of the customizations for yourself.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の手順では、フリート管理拡張モデルでのカスタマイズを調べて、自分でカスタマイズの一部を再実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>Setup</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">段取り</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>If you haven't opened the Fleet Management Solution in a previous tutorial, follow these steps.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のチュートリアルでフリート管理ソリューションを開いていない場合は、以下の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>The fleet management solution file is available on the Dynamics AX downloadable VM.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理ソリューション ファイルは、Dynamics AX のダウンロード可能な VM で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>On the <bpt id="p1">**</bpt>Desktop<ept id="p1">**</ept>, double-click the <bpt id="p2">**</bpt>Visual Studio<ept id="p2">**</ept> shortcut to open the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デスクトップ<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>Visual Studio<ept id="p2">**</ept> ショートカットをダブルクリックして、開発環境を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>Open the <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> ソリューションを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Browse to the desktop and open the <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップを参照し、<bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> フォルダーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>If the solution file is not on your computer, the steps to create it are listed in <bpt id="p1">[</bpt>Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション ファイルがコンピュータにない場合は、作成手順が「<bpt id="p1">[</bpt>チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)</ept>」に記載されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>Select the solution file named <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> という名前のソリューション ファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>The file type listed is Microsoft Visual Studio Solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるファイル タイプは Microsoft Visual Studio Solution です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>Click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>The solution may take some time to open.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションを開くには時間がかかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>Installing the demo data</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データのインストール</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>If you've already installed the demo data, you can skip to the next section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データを既にインストールしている場合、次のセクションに進めます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>In the VM, open Internet Explorer and navigate to the application's base URL.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM で、Internet Explorer を開き、アプリケーションのベース URL に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Sign in.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">サインインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source>On the dashboard, open the navigation pane and navigate to <bpt id="p1">**</bpt>Fleet Management <ph id="ph1">&amp;gt;</ph> Setup <ph id="ph2">&amp;gt;</ph> Fleet Setup<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュ ボードで、ナビゲーション ウィンドウを開き、<bpt id="p1">**</bpt>フリート管理 <ph id="ph1">&amp;gt;</ph> 設定 <ph id="ph2">&amp;gt;</ph> フリート設定<ept id="p1">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Fleet setup &gt; Customize model<ept id="p1">](./media/fleetsetup_customizemodel.png)](./media/fleetsetup_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>フリート設定 &gt; カスタマイズ モデル<ept id="p1">](./media/fleetsetup_customizemodel.png)](./media/fleetsetup_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>Click <bpt id="p1">**</bpt>Setup Demo Data<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デモ データの設定<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Configuration &gt; Customize Model<ept id="p1">](./media/configuration_customizemodel.png)](./media/configuration_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>コンフィギュレーション &gt; モデルをカスタマイズする<ept id="p1">](./media/configuration_customizemodel.png)](./media/configuration_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>If you're prompted to reload the demo data, click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デモ データの再読み込みを促すメッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>When the data is finished loading, click <bpt id="p1">**</bpt>Close<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データが読み込みを完了したら、<bpt id="p1">**</bpt>閉じる<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>On the dashboard, open the navigation bar and navigate to <bpt id="p1">**</bpt>System Administration <ph id="ph1">&amp;gt;</ph> Common <ph id="ph2">&amp;gt;</ph> Maintain aggregate measurements<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダッシュ ボードで、ナビゲーション バーを開き、<bpt id="p1">**</bpt>システム管理 <ph id="ph1">&amp;gt;</ph> 共通 <ph id="ph2">&amp;gt;</ph> 集計の測定を維持<ept id="p1">**</ept>に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>(Steps 7 to 9 are not applicable on newer releases)</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">(手順 7 ～ 9 は、新しいリリースでは適用できません)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source>Select <bpt id="p1">**</bpt>FMAggregateMeasurements<ept id="p1">**</ept>, and on the Action Pane, click <bpt id="p2">**</bpt>Refresh now<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMAggregateMeasurements<ept id="p1">**</ept> を選択し、アクション ペインで <bpt id="p2">**</bpt>今すぐ更新<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>Wait until the processing completes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">処理が完了するまで待機します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The ongoing processing is indicated at the top of the page by a series of moving dots.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">進行中の処理は、一連の移動するドットによってページの上部に示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>The processing is completed when the indicator disappears and the <bpt id="p1">**</bpt>Time Last Processed<ept id="p1">**</ept> field is updated.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インジケータが消えて、<bpt id="p1">**</bpt>前回処理時刻<ept id="p1">**</ept> フィールドが更新されると、処理が完了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>Open the FMRental form on the one-box environment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">1 ボックス環境で FMRental フォームを開く</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>In the VM, open Internet Explorer and navigate to the base URL of your Dynamics AX application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">VM で、Internet Explorer を開き、Dynamics AX アプリケーションのベース URL に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source>For more information, see <bpt id="p1">[</bpt>Access Microsoft Dynamics AX Instances<ept id="p1">](../dev-tools/access-instances.md)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">詳細については、「<bpt id="p1">[</bpt>Microsoft Dynamics AX インスタンスにアクセス <ept id="p1">](../dev-tools/access-instances.md)</ept>」を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Sign in, if prompted.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">求められた場合にログインします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Find the <bpt id="p1">**</bpt>Reservation Management<ept id="p1">**</ept> tile and click to open the Reservation Management workspace.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予約管理<ept id="p1">**</ept>タイルを検索し、予約管理ワークスペースを開くためそれをクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Reservation management tile<ept id="p1">](./media/reservationmanagementtile.jpg)](./media/reservationmanagementtile.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>予約管理タイル<ept id="p1">](./media/reservationmanagementtile.jpg)](./media/reservationmanagementtile.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>When the <bpt id="p1">**</bpt>Reservation Management<ept id="p1">**</ept> workspace opens, click <bpt id="p2">**</bpt>Current rentals<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>予約管理<ept id="p1">**</ept> ワークスペースが開いたら、<bpt id="p2">**</bpt>現在のレンタル<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Current rentals<ept id="p1">](./media/reservationmanagementworkspace.jpg)](./media/reservationmanagementworkspace.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>現在のレンタル<ept id="p1">](./media/reservationmanagementworkspace.jpg)](./media/reservationmanagementworkspace.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>This will open the <bpt id="p1">**</bpt>Rental<ept id="p1">**</ept> form in grid view.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、グリッド ビューで <bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept> フォームが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Rental form<ept id="p1">](./media/rentalform_customizemodel.png)](./media/rentalform_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>レンタル フォーム<ept id="p1">](./media/rentalform_customizemodel.png)](./media/rentalform_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>After the <bpt id="p1">**</bpt>Rental<ept id="p1">**</ept> form loads, click <bpt id="p2">**</bpt>Options <ph id="ph1">&amp;gt;</ph> Change view <ph id="ph2">&amp;gt;</ph> Header<ept id="p2">**</ept> to open the <bpt id="p3">**</bpt>Header view<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>レンタル<ept id="p1">**</ept> フォームを実行した後、<bpt id="p2">**</bpt>オプション <ph id="ph1">&amp;gt;</ph> ビューの変更 <ph id="ph2">&amp;gt;</ph> ヘッダー<ept id="p2">**</ept> をクリックして、<bpt id="p3">**</bpt>ヘッダーの表示<ept id="p3">**</ept>を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Header view<ept id="p1">](./media/headerview_customizemodel.png)](./media/headerview_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ヘッダーの表示<ept id="p1">](./media/headerview_customizemodel.png)](./media/headerview_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>When the <bpt id="p1">**</bpt>Header view<ept id="p1">**</ept> form loads, scroll to the bottom and expand the <bpt id="p2">**</bpt>Discounts<ept id="p2">**</ept> tab. This tab isn't part of the Fleet Management model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ヘッダーの表示<ept id="p1">**</ept>フォームを読み込んだら、下までスクロールし、<bpt id="p2">**</bpt>割引<ept id="p2">**</ept> タブを展開します。このタブはフリート管理モデルに含まれていません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>It has been modeled in the Fleet Management Extension Model as an extension to the <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、<bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> フォームに対する拡張機能としてフリート管理拡張モデルでモデリングされています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Discounts<ept id="p1">](./media/discounts_customizemodel.png)](./media/discounts_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>割引<ept id="p1">](./media/discounts_customizemodel.png)](./media/discounts_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Click <bpt id="p1">**</bpt>Add<ept id="p1">**</ept> to add a discount.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引を追加するために<bpt id="p1">**</bpt>追加<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>Select the <bpt id="p1">**</bpt>Frequent Customer<ept id="p1">**</ept> discount, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>得意先<ept id="p1">**</ept> 割引を選択し、<bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The selected discount is added to the <bpt id="p1">**</bpt>Discounts<ept id="p1">**</ept> grid.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択した割引が <bpt id="p1">**</bpt>割引<ept id="p1">**</ept> グリッドに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Frequent customer discount<ept id="p1">](./media/fcdiscount_customizemodel.png)](./media/fcdiscount_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>得意先割引<ept id="p1">](./media/fcdiscount_customizemodel.png)](./media/fcdiscount_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>Use the shortcut key, <bpt id="p1">**</bpt>Alt+F2<ept id="p1">**</ept> to open the FactBox.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FactBox を開くには、ショートカット キー <bpt id="p1">**</bpt>Alt+F2<ept id="p1">**</ept> を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>Expand the <bpt id="p1">**</bpt>Rental total<ept id="p1">**</ept> FactBox on the right and view the discount savings that are applied.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右側の<bpt id="p1">**</bpt>レンタル合計<ept id="p1">**</ept>情報ボックスを展開し、適用されるディスカウントの割引を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Rental total<ept id="p1">](./media/rentaltotal_customizemodel.png)](./media/rentaltotal_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>レンタル合計<ept id="p1">](./media/rentaltotal_customizemodel.png)](./media/rentaltotal_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>Overview of the Fleet management discount extension project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理割引の拡張プロジェクトの概要</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>In this tutorial, the <bpt id="p1">**</bpt>FleetManagementDiscounts<ept id="p1">**</ept> Project contains the model elements that belong to the model named <bpt id="p2">**</bpt>Fleet Management Extension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、<bpt id="p1">**</bpt>FleetManagementDiscounts<ept id="p1">**</ept> プロジェクトに<bpt id="p2">**</bpt>フリート管理拡張<ept id="p2">**</ept>という名前のモデルに属しているモデルの要素が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Here, you'll explore and learn about the project elements.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、プロジェクト要素について調べ、学びます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Navigate to FMRental.Extension in the Tree Designer</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツリー デザイナーで FMRental.Extension に移動します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>In the Visual Studio, in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, in the <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> project, expand <bpt id="p3">**</bpt>User Interface <ph id="ph1">&amp;gt;</ph> Form Extensions<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の <bpt id="p2">**</bpt>FleetManagement 割引<ept id="p2">**</ept>プロジェクトで、<bpt id="p3">**</bpt>ユーザー インターフェイス <ph id="ph1">&amp;gt;</ph> フォーム機能拡張<ept id="p3">**</ept>と展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Solution explorer<ept id="p1">](./media/solutionexplorer1_customizemodel.png)](./media/solutionexplorer1_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ソリューション エクスプローラー<ept id="p1">](./media/solutionexplorer1_customizemodel.png)](./media/solutionexplorer1_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>The <bpt id="p1">**</bpt>FMRental.Extension<ept id="p1">**</ept> element is an extension element that extends the functionality of the <bpt id="p2">**</bpt>FMRental<ept id="p2">**</ept> form by adding two new data sources and a new tab control.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRental.Extension<ept id="p1">**</ept> 要素は、2 つの新しいデータ ソースと新しいタブ コントロールを追加することによって <bpt id="p2">**</bpt>FMRental<ept id="p2">**</ept> フォームの機能を拡張する拡張要素です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>FMRental.Extension<ept id="p2">**</ept> to open the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMRental.Extension<ept id="p2">**</ept> をダブルクリックしてデザイナーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>As the following image shows:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のイメージに示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>The data sources shown in <bpt id="p1">*</bpt>italic<ept id="p1">*</ept> text are data sources defined in the baseline form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">*</bpt>斜体<ept id="p1">*</ept>のテキストで示されているデータ ソースはベースライン フォームで定義されているデータ ソースです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>The data sources shown in <bpt id="p1">**</bpt>bold<ept id="p1">**</ept> are the ones defined in the current extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>太字<ept id="p1">**</ept>で示されているデータ ソースは現在の拡張子で定義されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>The designer presents an integrated view of the model element, including its extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーは、その拡張機能を含めて、モデル要素の統合ビューを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>Read-only nodes are shown in italic text, while nodes that belong to the current extension are shown in bold, with other visual cues that indicate the type of customization.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み取り専用ノードは斜体で表示さえｒますが、現在の拡張機能に属するノードはカスタマイズの種類を示す他の視覚的な記号と共に太字で表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalExt<ph id="ph2">\_</ph>CustomizeModel<ept id="p1">](./media/fmrentalext_customizemodel.png)](./media/fmrentalext_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalExt<ph id="ph2">\_</ph>CustomizeModel<ept id="p1">](./media/fmrentalext_customizemodel.png)](./media/fmrentalext_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>In the designer's search box, type 'e:' as shown in the image below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーの検索ボックスに、次の図に示すように「e:」と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>This filters the current designer to only show nodes that belong to the current extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">現在のデザイナーがフィルター処理され、現在の拡張に属するノードのみが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Current extension<ept id="p1">](./media/rentalext-e_customizemodel.png)](./media/rentalext-e_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>現在の拡張機能<ept id="p1">](./media/rentalext-e_customizemodel.png)](./media/rentalext-e_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>You can also type 'e:LineViewDiscounts' to filter the designer to show nodes that match the name <bpt id="p1">**</bpt>LineViewDiscounts<ept id="p1">**</ept> and that belong to the current extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、'e:LineViewDiscounts' と入力してデザイナーをフィルター処理し、<bpt id="p1">**</bpt>LineViewDiscounts<ept id="p1">**</ept> という名前と一致し現在の拡張子に属するノードを表示することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>LineViewDiscounts<ept id="p1">](./media/lineviewdiscounts_customizemodel.png)](./media/lineviewdiscounts_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LineViewDiscounts<ept id="p1">](./media/lineviewdiscounts_customizemodel.png)](./media/lineviewdiscounts_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Expand the <bpt id="p1">**</bpt>LineViewDiscounts<ept id="p1">**</ept> node to see its contents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">内容を確認するには、<bpt id="p1">**</bpt>LineViewDiscounts<ept id="p1">**</ept> ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Expand LineViewDiscounts node<ept id="p1">](./media/expandlvdnode_customizemodel.png)](./media/expandlvdnode_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>LineViewDiscounts ノードの展開<ept id="p1">](./media/expandlvdnode_customizemodel.png)](./media/expandlvdnode_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>Open the FMRental.Extension XML file to view the metadata</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMRental.Extension XML ファイルを開いてメタデータを表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>In the <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click FMRental.Extension form extension, and then click <bpt id="p2">**</bpt>Open with<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、FMRental.Extension フォーム拡張子をクリックしてから<bpt id="p2">**</bpt>プログラムから開く<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>In the <bpt id="p1">**</bpt>Open with<ept id="p1">**</ept> dialog box, select <bpt id="p2">**</bpt>XML (Text) Editor<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>OK<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プログラムから開く<ept id="p1">**</ept>ダイアログ ボックスで、<bpt id="p2">**</bpt>XML (テキスト) エディター<ept id="p2">**</ept>を選択してから <bpt id="p3">**</bpt>OK<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source>When prompted to close the designer, click <bpt id="p1">**</bpt>Yes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デザイナーを閉じるように求めるメッセージが表示されたら、<bpt id="p1">**</bpt>はい<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>Click the corresponding minus signs to collapse the child nodes of the <bpt id="p1">**</bpt>Controls<ept id="p1">**</ept> and <bpt id="p2">**</bpt>DataSources<ept id="p2">**</ept> nodes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">対応するマイナス記号をクリックすると、<bpt id="p1">**</bpt>制御<ept id="p1">**</ept>および<bpt id="p2">**</bpt>データ ソース<ept id="p2">**</ept> ノードの子ノードが折りたたまれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>Refer to the following image for the correct result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">正しい結果については次の図を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Rental code<ept id="p1">](./media/fmrentalcode_customizemodel.png)](./media/fmrentalcode_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>レンタル コード<ept id="p1">](./media/fmrentalcode_customizemodel.png)](./media/fmrentalcode_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>The XML file contains the metadata associated with the <bpt id="p1">**</bpt>FMRental.Extension<ept id="p1">**</ept> element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML ファイルには、<bpt id="p1">**</bpt>FMRental.Extension<ept id="p1">**</ept> 要素に関連付けられているメタデータが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>You can see that this file contains metadata that describes only one tab page control and two data sources that are part of the extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このファイルに、拡張機能の一部である 1 つのみのタブ ページ コントロールおよび 2 つのデータ ソースを説明するメタデータが含まれることがわかります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>You can also see that it doesn't contain any metadata from the base form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本フォームからのメタデータが含まれていないことを確認することもできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>View other elements in the Fleet Management discount extension project</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理割引の拡張プロジェクトのその他の要素の表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>The <bpt id="p1">**</bpt>FleetManagement Discounts<ept id="p1">**</ept> project contains two new tables, <bpt id="p2">**</bpt>FEDiscount<ept id="p2">**</ept> and <bpt id="p3">**</bpt>FERentalDiscountRelationTable<ept id="p3">**</ept>, and two extensions to existing Fleet Management tables, <bpt id="p4">**</bpt>FMRental<ept id="p4">**</ept> and <bpt id="p5">**</bpt>FMRentalCharge<ept id="p5">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetManagement Discounts<ept id="p1">**</ept> プロジェクトには 2 つの新しいテーブル <bpt id="p2">**</bpt>FEDiscount<ept id="p2">**</ept> および <bpt id="p3">**</bpt>FERentalDiscountRelationTable<ept id="p3">**</ept> と、既存のフリート管理テーブル <bpt id="p4">**</bpt>FMRental<ept id="p4">**</ept> および <bpt id="p5">**</bpt>FMRentalCharge<ept id="p5">**</ept> への 2 つの拡張が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, in FleetManagement Discounts, double-click <bpt id="p2">**</bpt>Data Model <ph id="ph1">&amp;gt;</ph> Table Extensions <ph id="ph2">&amp;gt;</ph> FMRental.Extension<ept id="p2">**</ept> to open the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の FleetManagement 割引で<bpt id="p2">**</bpt>データ モデル <ph id="ph1">&amp;gt;</ph> テーブル拡張機能 <ph id="ph2">&amp;gt;</ph> FMRental.Extension<ept id="p2">**</ept> をダブルクリックしてデザイナーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Expand the <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> node to see that this extension contains one added field, FEVehicleRateDiscount, to the base FMRental table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept>ノードを展開し、拡張子に追加されたフィールド FEVehicleRateDiscount がベース FMRental テーブルに含まれていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FEVehicleRateDiscount<ept id="p1">](./media/nodes_customizemodel.png)](./media/nodes_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FEVehicleRateDiscount<ept id="p1">](./media/nodes_customizemodel.png)](./media/nodes_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>Similarly, open the <bpt id="p1">**</bpt>FMRentalChange.Extension<ept id="p1">**</ept> element in the designer to explore its contents.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、デザイナーで <bpt id="p1">**</bpt>FMRentalChange.Extension<ept id="p1">**</ept> 要素を開いて、その内容を調べます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Inspect the data event handlers</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">データ イベント ハンドラーの検査</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, in the FleetManagement Discounts project, double-click <bpt id="p2">**</bpt>Code <ph id="ph1">&amp;gt;</ph> Classes <ph id="ph2">&amp;gt;</ph> FMRentalCharge<ph id="ph3">\_</ph>Extension<ept id="p2">**</ept> to open the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>の FleetManagement 割引プロジェクトで、<bpt id="p2">**</bpt>コード <ph id="ph1">&amp;gt;</ph> クラス <ph id="ph2">&amp;gt;</ph> FMRentalCharge<ph id="ph3">\_</ph>Extension<ept id="p2">**</ept> をダブルクリックしてコード エディターを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalChargeCode<ept id="p1">](./media/fmrentalchargecode_customizemodel.png)](./media/fmrentalchargecode_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMRentalChargeCode<ept id="p1">](./media/fmrentalchargecode_customizemodel.png)](./media/fmrentalchargecode_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>This class contains event handler implementations that subscribe to the <bpt id="p1">**</bpt>Updating<ept id="p1">**</ept> and <bpt id="p2">**</bpt>Inserting<ept id="p2">**</ept> events of the <bpt id="p3">**</bpt>FMRentalCharge<ept id="p3">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスには、<bpt id="p3">**</bpt>FMRentalCharge<ept id="p3">**</ept> テーブルの<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>および<bpt id="p2">**</bpt>挿入<ept id="p2">**</ept>イベントに登録するイベント ハンドラーの実装が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>Microsoft Dynamics AX introduces data events that can occur on tables and other types.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Microsoft Dynamics AX では、テーブルおよび他の種類で発生する可能性のあるデータ イベントが導入されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>You can subscribe to data events of a table, enabling your application to extend business logic without overlayering base X++ code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本 X++ コードをオーバーレイせずにビジネス ロジックを拡張するアプリケーションを有効にする、テーブルのデータ イベントを申し込むことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>Later in this tutorial, you'll see how easy it is to subscribe to table events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルの後半で、簡単にテーブル イベントをサブスクライブする方法について説明します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source><bpt id="p1">**</bpt>Note:<ept id="p1">**</ept> Notice that this class is an extension class (indicated by the <ph id="ph1">\_</ph>Extension suffix).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記:<ept id="p1">**</ept> このクラスが拡張クラス (<ph id="ph1">\_</ph>拡張子の接尾辞によって示される) であることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>You can author event handlers in any class, this class does not need to be an extension class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">任意のクラスでイベント ハンドラーを作成することができます。このクラスは拡張クラスである必要はありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>Extension classes are needed in order to create extension methods.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張子クラスは、拡張メソッドを作成するために必要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>For more details on extension methods, refer to the "Extension methods" section of the <bpt id="p1">[</bpt>X++ debugger features<ept id="p1">](../dev-tools/new-x-debugger-features.md)</ept> article.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドの詳細については、<bpt id="p1">[</bpt>X++ デバッガーの機能<ept id="p1">](../dev-tools/new-x-debugger-features.md)</ept> 記事の「拡張メソッド」セクションを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>View the plug-in classes</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン クラスの表示</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>In the event handler code of the <bpt id="p1">**</bpt>FMRentalCharge<ph id="ph1">\_</ph>Extension<ept id="p1">**</ept> class shown in the previous section, notice that both event handlers call <bpt id="p2">**</bpt>FMTotalsEngineBase::GetInstance<ept id="p2">**</ept> to retrieve the current instance of the Fleet Management calculation engine.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションに示された <bpt id="p1">**</bpt>FMRentalCharge<ph id="ph1">\_</ph>Extension<ept id="p1">**</ept> クラスのイベント ハンドラー コードでは、両方のイベント ハンドラーが <bpt id="p2">**</bpt>FMTotalsEngineBase::GetInstance<ept id="p2">**</ept> を呼び出してフリート管理計算エンジンの現在のインスタンスを取得することを確認してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>The calculation engines are implemented by using plug-in classes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">計算エンジンは、プラグイン クラスを使用して実装されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>A class factory creates the appropriate instances of a plug-in class based on configuration or business data.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス ファクトリは、コンフィギュレーションまたはビジネス データに基づくプラグイン クラスの適切なインスタンスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>In the code editor window that displays FMRentalCharge<ph id="ph1">\_</ph>Extension.xpp, right-click <bpt id="p1">**</bpt>GetInstance<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Go To Definition<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMRentalCharge<ph id="ph1">\_</ph>Extension.xpp を表示するコード エディター ウィンドウで、<bpt id="p1">**</bpt>GetInstance<ept id="p1">**</ept> を右クリックしてから<bpt id="p2">**</bpt>定義に移動<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>This will open the code of the abstract class <bpt id="p1">**</bpt>FMTotalsEngineBase<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、抽象クラス <bpt id="p1">**</bpt>FMTotalsEngineBase<ept id="p1">**</ept> のコードが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>This abstract class is called a <bpt id="p1">**</bpt>plugin point<ept id="p1">**</ept> and it's associated with the following attribute: <ph id="ph1">\[</ph>Microsoft.Dynamics.AX.Platform.Extensibility.ExportInterfaceAttribute()<ph id="ph2">\]</ph></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この抽象クラスは<bpt id="p1">**</bpt>プラグインポイント<ept id="p1">**</ept>と呼ばれ、属性 <ph id="ph1">\[</ph>Microsoft.Dynamics.AX.Platform.Extensibility.ExportInterfaceAttribute()<ph id="ph2">\]</ph> に関連付けられています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Go to Definition<ept id="p1">](./media/godefinition_customizemodel.png)](./media/godefinition_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>定義に移動<ept id="p1">](./media/godefinition_customizemodel.png)](./media/godefinition_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>Plug-in classes represent extensions or implementations of abstract classes or interfaces.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン クラスは、抽象クラスやインターフェイスの拡張機能または実装を表します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="265">
          <source>Plug-in classes are associated with attributes defining their metadata and the plug-in point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン クラスは、そのメタデータとプラグイン ポイントを定義する属性に関連付けられます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="266">
          <source>In this example, there are two plug-in classes associated with the <bpt id="p1">**</bpt>FMTotalsEngineBase<ept id="p1">**</ept> plug-in point.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この例では、<bpt id="p1">**</bpt>FMTotalsEngineBase<ept id="p1">**</ept> プラグイン ポイントに関連付けられている 2 つのプラグイン クラスがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="267">
          <source>The base calculation engine is defined by the plug-in class <bpt id="p1">**</bpt>FMTotalsEngine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">基本計算エンジンは、プラグイン クラス <bpt id="p1">**</bpt>FMTotalsEngine<ept id="p1">**</ept> によって定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="268">
          <source>You can find it in the project <bpt id="p1">**</bpt>FleetManagement Migrated <ph id="ph1">&amp;gt;</ph> Code <ph id="ph2">&amp;gt;</ph> Classes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト <bpt id="p1">**</bpt>移行されたフリート管理 <ph id="ph1">&amp;gt;</ph> コード <ph id="ph2">&amp;gt;</ph> クラス<ept id="p1">**</ept> で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="269">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTotalsEngineBase<ept id="p1">](./media/code1_customizemodel.png)](./media/code1_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMTotalsEngineBase<ept id="p1">](./media/code1_customizemodel.png)](./media/code1_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="270">
          <source>The discount calculation engine is defined by the plug-in class <bpt id="p1">**</bpt>FEDiscountEngine<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">割引計算エンジンは、プラグイン クラス <bpt id="p1">**</bpt>FEDiscountEngine<ept id="p1">**</ept> によって定義されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="271">
          <source>You can find it in the project <bpt id="p1">**</bpt>FleetManagement Discounts <ph id="ph1">&amp;gt;</ph> Code <ph id="ph2">&amp;gt;</ph> Classes<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト <bpt id="p1">**</bpt>フリート管理割引 <ph id="ph1">&amp;gt;</ph> コード <ph id="ph2">&amp;gt;</ph> クラス<ept id="p1">**</ept> で見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="272">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FEDiscountEngine<ept id="p1">](./media/code2_customizemodel.png)](./media/code2_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FEDiscountEngine<ept id="p1">](./media/code2_customizemodel.png)](./media/code2_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="273">
          <source>Look at the <bpt id="p1">**</bpt>GetInstance<ept id="p1">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>GetInstance<ept id="p1">**</ept> メソッドを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="274">
          <source>It uses the plug-in factory <bpt id="p1">**</bpt>SysPluginFactory::Instance<ept id="p1">**</ept> to instantiate the current calculation engine based on current plug-in metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、プラグイン ファクトリ <bpt id="p1">**</bpt>SysPluginFactory::Instance<ept id="p1">**</ept> を使用して、現在のプラグイン メタデータに基づいて現在の計算エンジンのインスタンスを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="275">
          <source>The plug-in metadata is specified in the global configuration table, <bpt id="p1">**</bpt>FMParameters<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プラグイン メタデータは、グローバル構成テーブルの <bpt id="p1">**</bpt>FMParameters<ept id="p1">**</ept> で指定されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="276">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMParameters<ept id="p1">](./media/code3_customizemodel.png)](./media/code3_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMParameters<ept id="p1">](./media/code3_customizemodel.png)](./media/code3_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="277">
          <source>Dynamics AX also supports configurable plug-in classes where the plug-in metadata associate with the class isn't known at development time and is configurable at runtime by an administrator.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Dynamics AX は、コンフィギュレーション可能なプラグイン クラスもサポートします。このクラスでは、クラスに関連付けられているプラグイン メタデータは開発時は未知であり、管理者がランタイム時にコンフィギュレーション可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="278">
          <source>This isn't in the scope of this tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、このチュートリアルの対象ではありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="279">
          <source>Create additional Fleet Management extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">追加のフリート管理拡張子を作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="280">
          <source>This section shows how you can use the Visual Studio tools to create and interact with extensions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このセクションでは、Visual Studio ツールを使用して拡張機能を作成して操作する方法を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="281">
          <source>Extend the FMVehicle Table</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMVehicle テーブルを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="282">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, select the <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FleetManagement 割引<ept id="p2">**</ept>プロジェクトを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="283">
          <source>In Visual studio, in <bpt id="p1">**</bpt>Application Explorer,<ept id="p1">**</ept> click <bpt id="p2">**</bpt>View <ph id="ph1">&amp;gt;</ph> Application Explorer<ept id="p2">**</ept>, and search for the table named FMVehicle.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual studio の<bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>表示 <ph id="ph1">&amp;gt;</ph> アプリケーション エクスプローラー<ept id="p2">**</ept>をクリックして、FMVehicle という名前のテーブルを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="284">
          <source>Type "FMVehicle type:Table" in the filter bar and press <bpt id="p1">**</bpt>Enter<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィルター バーに "FMVehicle type:Table" と入力し、<bpt id="p1">**</bpt>Enter<ept id="p1">**</ept> を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="285">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>AppExplorer search for FMVehicle<ept id="p1">](./media/appexplorersmall_customizemodel.png)](./media/appexplorersmall_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicle の AppExplore 検索<ept id="p1">](./media/appexplorersmall_customizemodel.png)](./media/appexplorersmall_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="286">
          <source>Right-click <bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>Create extension<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept> を右クリックし、<bpt id="p2">**</bpt>拡張子の作成<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="287">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>AppExplorer Create extension<ept id="p1">](./media/appexplorerlarge1_customizemodel.png)](./media/appexplorerlarge1_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>AppExplorer 拡張機能の作成<ept id="p1">](./media/appexplorerlarge1_customizemodel.png)](./media/appexplorerlarge1_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="288">
          <source>This will create an extension of the <bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept> table in the <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> project named <bpt id="p3">**</bpt>FMVehicle.Extension<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、<bpt id="p3">**</bpt>FMVehicle.Extension<ept id="p3">**</ept> という名前の <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> プロジェクトに <bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept> テーブルの拡張が作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="289">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicle.Extension<ept id="p1">](./media/expanddiscountsnode2_customizemodel.png)](./media/expanddiscountsnode2_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicle.Extension<ept id="p1">](./media/expanddiscountsnode2_customizemodel.png)](./media/expanddiscountsnode2_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="290">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FMVehicle.Extension<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Open with<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMVehicle.Extension<ept id="p2">**</ept> を右クリックしてから<bpt id="p3">**</bpt>プログラムから開く<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="291">
          <source>In the dialog box, select <bpt id="p1">**</bpt>XML (Text) Editor<ept id="p1">**</ept>, and then click <bpt id="p2">**</bpt>OK<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ダイアログ ボックスで <bpt id="p1">**</bpt>XML (テキスト) エディター<ept id="p1">**</ept>を選択してから <bpt id="p2">**</bpt>OK<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="292">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: This extension file is simply a template that doesn't contain metadata from the base <bpt id="p2">**</bpt>FMVehicle<ept id="p2">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: この拡張子ファイルは、データベースの <bpt id="p2">**</bpt>FMVehicle<ept id="p2">**</ept> テーブルのメタデータを含まない簡単なテンプレートです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="293">
          <source>An extension file will always contain only the metadata that defines the extension and nothing from the base model element.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張ファイルには拡張を定義するメタデータのみが常に含まれ、基本モデル要素からは何もありません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="294">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicle<ept id="p1">](./media/code4_customizemodel.png)](./media/code4_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>FMVehicle<ept id="p1">](./media/code4_customizemodel.png)](./media/code4_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="295">
          <source>Close the XML editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">XML エディターを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="296">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>FMVehicle.Extension<ept id="p2">**</ept> to open the designer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FMVehicle.Extension<ept id="p2">**</ept> をダブルクリックしてデザイナーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="297">
          <source>Right-click <bpt id="p1">**</bpt>Fields<ept id="p1">**</ept> and add a new integer field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フィールド<ept id="p1">**</ept> を右クリックし、新しい整数型フィールドを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="298">
          <source>Change the name of the field to <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フィールドの名前を <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="299">
          <source>In the <bpt id="p1">**</bpt>Properties<ept id="p1">**</ept> window, set the <bpt id="p2">**</bpt>Label<ept id="p2">**</ept> property of the new field to <bpt id="p3">**</bpt>NumberofCylinders<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>プロパティ<ept id="p1">**</ept> ウィンドウで、新しいフィールドの<bpt id="p2">**</bpt>ラベル<ept id="p2">**</ept> プロパティを <bpt id="p3">**</bpt>NumberofCylinders<ept id="p3">**</ept> に設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="300">
          <source>Drag-and-drop the <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> field into the <bpt id="p2">**</bpt>AutoReport<ept id="p2">**</ept> field group to extend the field group of the base table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> フィールドを <bpt id="p2">**</bpt>AutoReport<ept id="p2">**</ept> フィールド グループにドラッグ アンド ドロップし、ベース テーブルのフィールド グループに展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="301">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>NumberOfCylinders<ph id="ph2">\_</ph>CustomizeModel<ept id="p1">](./media/numberofcylinders_customizemodel.png)](./media/numberofcylinders_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>NumberOfCylinders<ph id="ph2">\_</ph>CustomizeModel<ept id="p1">](./media/numberofcylinders_customizemodel.png)](./media/numberofcylinders_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="302">
          <source>Save FMVehicle.Extension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMVehicle.Extension を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="303">
          <source>Expand the <bpt id="p1">**</bpt>Events<ept id="p1">**</ept> node.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イベント<ept id="p1">**</ept>ノードを展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="304">
          <source>The <bpt id="p1">**</bpt>Events<ept id="p1">**</ept> node lists all events that the table exposes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>イベント<ept id="p1">**</ept> ノードには、テーブルが公開するすべてのイベントが一覧表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="305">
          <source>This includes events that are defined by the framework, and delegate methods that are defined by application developers.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これには、フレームワークによって定義されたイベントと、アプリケーション開発者によって定義されたデリゲート メソッドが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="306">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Events node<ept id="p1">](./media/eventsnode_customizemodel.png)](./media/eventsnode_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>イベント ノード<ept id="p1">](./media/eventsnode_customizemodel.png)](./media/eventsnode_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="307">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: Different framework events are exposed on the designers of many types of element and sub-elements, like table events, form events, form data source events, and form control events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: テーブルのイベント、フォームイベント、フォーム データ ソース イベント、フォーム コントロール イベントなど、異なるフレームワーク イベントが、さまざまなタイプの要素とサブ要素のデザイナーに公開されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="308">
          <source>Right-click onValidatedWrite, and then select <bpt id="p1">**</bpt>Copy event handler method<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">onValidatedWrite を右クリックし、<bpt id="p1">**</bpt>イベント ハンドラー メソッドをコピー<ept id="p1">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="309">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>onValidateWrite<ept id="p1">](./media/onvalidatewrite_customizemodel.png)](./media/onvalidatewrite_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>onValidateWrite<ept id="p1">](./media/onvalidatewrite_customizemodel.png)](./media/onvalidatewrite_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="310">
          <source>This step copies the event handler method signature to the clipboard.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップは、イベント ハンドラー メソッドのシグネチャをクリップボードにコピーします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="311">
          <source>Add a new class named <bpt id="p1">**</bpt>FMVehicleEventHandlers<ept id="p1">**</ept> to the <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMVehicleEventHandlers<ept id="p1">**</ept> という名前の新しいクラスを <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> プロジェクトに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="312">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click <bpt id="p2">**</bpt>FEVehicleEventHandlers<ept id="p2">**</ept> to open the code editor.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FEVehicleEventHandlers<ept id="p2">**</ept> をダブルクリックしてコード エディターを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="313">
          <source>Right-click and paste the event handler method that you copied in step 12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">右クリックし、手順 12 にコピーしたイベント ハンドラー メソッドを貼り付けます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="314">
          <source>Insert the following code into the <bpt id="p1">**</bpt>FMVehicle<ph id="ph1">\_</ph>onValidatedWrite<ept id="p1">**</ept> event handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のコードを <bpt id="p1">**</bpt>FMVehicle<ph id="ph1">\_</ph>onValidatedWrite<ept id="p1">**</ept> イベント ハンドラーに挿入します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="315">
          <source>This code validates that the number of cylinders can't be greater than 8.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコードは、シリンダの数が 8 を超えることができないことを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="316">
          <source>Save FMVehicleEventHandlers class <bpt id="p1">**</bpt>Tip<ept id="p1">**</ept>: You can paste and define your event handlers in any class of your model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMVehicleEventHandlers クラスを保存 <bpt id="p1">**</bpt>ヒント<ept id="p1">**</ept>: モデルの任意のクラスで、イベント ハンドラーを貼り付けて定義できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="317">
          <source>The class FMVehicleEventHandlers is used only as an example.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス FMVehicleEventHandlers は、例としてのみ使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="318">
          <source>Extend the FMVehicle Form</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMVehicle フォームを拡張</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="319">
          <source>Next, add an extension to the <bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept> form in the <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept> project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次に、<bpt id="p2">**</bpt>FleetManagement 割引<ept id="p2">**</ept>プロジェクトの <bpt id="p1">**</bpt>FMVehicle<ept id="p1">**</ept> フォーム拡張機能を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="320">
          <source>First, be sure to select this project in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初に、<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>でこのプロジェクトを選択することを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="321">
          <source>Use <bpt id="p1">**</bpt>Application Explorer<ept id="p1">**</ept> to find the form named <bpt id="p2">**</bpt>FMVehicle<ept id="p2">**</ept>, and in the <bpt id="p3">**</bpt>Application Explorer<ept id="p3">**</ept> filter bar, enter the <bpt id="p4">*</bpt>FMVehicle type:form<ept id="p4">*</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>アプリケーション エクスプローラー<ept id="p1">**</ept>を使用して <bpt id="p2">**</bpt>FMVehicle<ept id="p2">**</ept> という名前のフォームを検索するには、<bpt id="p3">**</bpt>アプリケーション エクスプローラー<ept id="p3">**</ept>のフィルタ バーに <bpt id="p4">*</bpt>FMVehicle タイプ:フォーム<ept id="p4">*</ept> を入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="322">
          <source>Right-click the form, and then click <bpt id="p1">**</bpt>Create extension<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームを右クリックし、<bpt id="p1">**</bpt>拡張子の作成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="323">
          <source>Add a new integer control named <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> to the <bpt id="p2">**</bpt>Attributes2<ept id="p2">**</ept> group control as shown below.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">下に示すように、<bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> という名前の新しい整数コントロールを <bpt id="p2">**</bpt>Attributes2<ept id="p2">**</ept> グループ コントロールに追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="324">
          <source>You can find this control by expanding <bpt id="p1">**</bpt>Design <ph id="ph1">&amp;gt;</ph> Tab <ph id="ph2">&amp;gt;</ph> TabPageDetails <ph id="ph3">&amp;gt;</ph> TabHeader <ph id="ph4">&amp;gt;</ph> DetailsDetails <ph id="ph5">&amp;gt;</ph> Attributes2<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このコントロールは、<bpt id="p1">**</bpt>デザイン<ph id="ph1">&amp;gt;</ph> タブ <ph id="ph2">&amp;gt;</ph> TabPageDetails <ph id="ph3">&amp;gt;</ph> TabHeader <ph id="ph4">&amp;gt;</ph> DetailsDetails <ph id="ph5">&amp;gt;</ph> Attributes2<ept id="p1">**</ept> を展開すると見つけることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="325">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Number of Cylinders<ept id="p1">](./media/numcylinteger_customizemodel.png)](./media/numcylinteger_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>シリンダの数<ept id="p1">](./media/numcylinteger_customizemodel.png)](./media/numcylinteger_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="326">
          <source>Bind the new control to the <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> data field in the properties window as follows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のように新しいコントロールをプロパティ ウィンドウの <bpt id="p1">**</bpt>NumberOfCylinders<ept id="p1">**</ept> データ フィールドにバインドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="327">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Bind control<ept id="p1">](./media/datafield_customizemodel.png)](./media/datafield_customizemodel.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>バインド コントロール<ept id="p1">](./media/datafield_customizemodel.png)](./media/datafield_customizemodel.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="328">
          <source>Save FMVehicle.Extension and build the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMVehicle.Extension を保存し、プロジェクトを作成します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="329">
          <source>Test your extensions</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能をテスト</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="330">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click <bpt id="p2">**</bpt>FleetManagement Discounts<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Set as StartUp project<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept>で、<bpt id="p2">**</bpt>FleetManagement 割引<ept id="p2">**</ept>を右クリックしてから、<bpt id="p3">**</bpt>スタートアップ プロジェクトとして設定<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="331">
          <source>Similarly, in FleetManagement Discounts, set the <bpt id="p1">**</bpt>FMVehicle.Extension<ept id="p1">**</ept> form as the startup object.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同様に、FleetManagement 割引で、スタートアップ オブジェクトとして <bpt id="p1">**</bpt>FMVehicle.Extension<ept id="p1">**</ept> フォームを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="332">
          <source>Press <bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> to start without debugging, or use the <bpt id="p2">**</bpt>Debug<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Ctrl+F5<ept id="p1">**</ept> キーを押してデバッグなしで開始するか、<bpt id="p2">**</bpt>デバッグ<ept id="p2">**</ept> メニューを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="333">
          <source>After the <bpt id="p1">**</bpt>Vehicles<ept id="p1">**</ept> form opens, select a vehicle to view its details.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>車両<ept id="p1">**</ept>フォームが開いた後、車両を選択して詳細を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="334">
          <source>Expand the <bpt id="p1">**</bpt>Details<ept id="p1">**</ept> tab and notice the new <bpt id="p2">**</bpt>Number of Cylinders<ept id="p2">**</ept> field.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>詳細<ept id="p1">**</ept>タブを展開し、新しい<bpt id="p2">**</bpt>シリンダ番号<ept id="p2">**</ept>フィールドを通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="335">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Details with number of cylinders<ept id="p1">](./media/nbofcyls.jpg)](./media/nbofcyls.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>シリンダー数の詳細<ept id="p1">](./media/nbofcyls.jpg)](./media/nbofcyls.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="336">
          <source>In the Action Pane, click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and change the value in the <bpt id="p2">**</bpt>Number of cylinders<ept id="p2">**</ept> field to 12.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>をクリックして<bpt id="p2">**</bpt>シリンダの数<ept id="p2">**</ept>フィールドの値を 12 に変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="337">
          <source>In the Action Pane, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="338">
          <source>Notice the validation error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証エラーを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="339">
          <source>Enter a valid number of cylinders, less than 9, and then save the new value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">有効なシリンダ数を 9 より小さく入力し、次に新しい値を保存します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="340">
          <source>Experiment with event handlers on form controls</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム コントロールでのイベント ハンドラーを試す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="341">
          <source>This is an example of adding event handler methods on existing controls.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、既存のコントロールにイベント ハンドラー メソッドを追加する例です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="342">
          <source>Find the <bpt id="p1">**</bpt>AddLine<ept id="p1">**</ept> command button control in the <bpt id="p2">**</bpt>FMRental<ept id="p2">**</ept> form designer, right-click the <bpt id="p3">**</bpt>OnClicked<ept id="p3">**</ept> event, and select <bpt id="p4">**</bpt>Copy event handler method<ept id="p4">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>FMRental<ept id="p2">**</ept> フォーム デザイナーで <bpt id="p1">**</bpt>AddLine<ept id="p1">**</ept> コマンド ボタン コントロールを検索し、<bpt id="p3">**</bpt>OnClicked<ept id="p3">**</ept> イベントを右クリックし、次に選択<bpt id="p4">**</bpt>イベント ハンドラーのメソッドをコピー<ept id="p4">**</ept>を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="343">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Add line OnClicked event<ept id="p1">](./media/addlineonclickedevent.jpg)](./media/addlineonclickedevent.jpg)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>明細行 OnClicked イベントを追加します。<ept id="p1">](./media/addlineonclickedevent.jpg)](./media/addlineonclickedevent.jpg)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="344">
          <source>Paste the event handler method in a class of the Fleet Management Extension model and add X++ code to implement it.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フリート管理拡張モデルのクラスでイベント ハンドラー メソッドを貼り付け、X++ コードを追加して実装します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="345">
          <source>When implementing the AddLine<ph id="ph1">\_</ph>OnClicked event handler, you can access the button control instance using the <bpt id="p1">**</bpt>sender<ept id="p1">**</ept> parameter.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">AddLine<ph id="ph1">\_</ph>OnClicked イベント ハンドラーを実装すると、<bpt id="p1">**</bpt>sender<ept id="p1">**</ept> パラメーターを使用して、ボタン コントロール インスタンスにアクセスできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="346">
          <source>If you need to access the parent form or any of its variables, this example shows how to access the <bpt id="p1">**</bpt>FormRun<ept id="p1">**</ept> instance and one of its data sources.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">親フォームや、変数のいずれかにアクセスする場合は、この例では、<bpt id="p1">**</bpt>FormRun<ept id="p1">**</ept> インスタンスとデータ ソースのいずれかにアクセスする方法が示されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="347">
          <source>Experiment with event handlers on form data sources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォーム データ ソースでのイベント ハンドラーを試す</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="348">
          <source>Just like tables, form controls and other element types, form data sources and form data source fields provide framework-level events.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル、フォーム コントロールおよびその他の要素タイプと同じように、フォーム データ ソースとフォーム データ ソース フィールドはフレームワーク レベルのイベントを提供します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="349">
          <source>The following example shows how you can use the ValidatingWrite event on a form data source or the Validating event on a form data source field to validate user input on the FMRental form.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の例は、フォーム データ ソースの ValidatingWrite イベントまたはフォーム データ ソースの検証イベントを使用して FMRental フォームのユーザー入力を検証する方法を示しています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="350">
          <source>This functionality is available as of Platform Update 7.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この機能は、Platform Update 7 以降で利用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="351">
          <source>Experiment with table extension display and edit methods</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">テーブル 拡張子ディスプレイを試し、メソッドを編集</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="352">
          <source>Extension methods enable you to extend tables by creating new display and edit methods on these tables without over-layering X++ code (Extension method must belong to a class named with an <ph id="ph1">\_</ph>Extension suffix).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張メソッドを使用すると、新しい表示を作成してテーブルを拡張し、オーバーレイ X++ コード無しでテーブルのメソッドを編集します (拡張メソッドは、<ph id="ph1">\_</ph> 拡張子の接尾語という名のクラスに属する必要があります)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="353">
          <source>For example, this class shows how you can extend the FMVehicle table with an extension display method named CupHoldersDisplay.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、このクラスは、CupHoldersDisplay と呼ばれる拡張表示メソッドを使用して、FMVehicle テーブルを拡張する方法を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="354">
          <source>On a form or form extension, you can bind a control to this display method by setting "Data Source = FMVehicle" and "Data method = "FMVehicle<ph id="ph1">\_</ph>Extension::CupHoldersDisplay" as the image below shows.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">フォームまたはフォームの拡張機能では、以下の画像に示すように、「Data Source = FMVehicle」および「Data method ="FMVehicle<ph id="ph1">\_</ph>Extension::CupHoldersDisplay」を設定することによってこの表示メソッドにコントロールをバインドできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="355">
          <source>Extension display method</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張表示メソッド</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="356">
          <source>Create a Fleet extension package for deployment</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">展開のためのフリート拡張パッケージを作成する</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="357">
          <source>To deploy your extension to another environment, for example, a test, pre-production or production environment, you must create a deployment package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">拡張機能をテスト環境、運用前環境、運用環境などの別の環境に展開するには、展開パッケージを作成する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="358">
          <source>In Visual Studio, on the <bpt id="p1">**</bpt>Dynamics AX<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Deploy<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Create Deployment Package<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の <bpt id="p1">**</bpt>Dynamics AX<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>配置<ept id="p2">**</ept>をポイントしてから、<bpt id="p3">**</bpt>配置パッケージの作成<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="359">
          <source>Create deployment package</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">配置パッケージの作成</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="360">
          <source>Select the <bpt id="p1">**</bpt>Fleet Management Extension<ept id="p1">**</ept> check box.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>フリート管理拡張<ept id="p1">**</ept> チェック ボックスをオンにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="361">
          <source>In the <bpt id="p1">**</bpt>Package file location<ept id="p1">**</ept> text box, enter "c:\FMLab".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>パッケージ ファイルの場所<ept id="p1">**</ept>テキスト ボックスに、「c:\FMLab」と入力します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="362">
          <source>Click <bpt id="p1">**</bpt>Create<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>作成<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="363">
          <source>This will create a deployment package that contains the Fleet management Extension package.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、フリート管理拡張パッケージを含む展開パッケージが作成されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="364">
          <source>Additional resources</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その他のリソース</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="365">
          <source><bpt id="p1">[</bpt>Download FMLab sample code<ept id="p1">](https://github.com/Microsoft/FMLab)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt>FMLab サンプル コードをダウンロードする<ept id="p1">](https://github.com/Microsoft/FMLab)</ept></target></trans-unit>
      </group>
    </body>
  </file>
</xliff>