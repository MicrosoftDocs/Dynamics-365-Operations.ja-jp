<?xml version="1.0" encoding="UTF-8"?>
<xliff xmlns:logoport="urn:logoport:xliffeditor:xliff-extras:1.0" xmlns:tilt="urn:logoport:xliffeditor:tilt-non-translatables:1.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="urn:oasis:names:tc:xliff:document:1.2" xmlns:xliffext="urn:microsoft:content:schema:xliffextensions" version="1.2" xsi:schemaLocation="urn:oasis:names:tc:xliff:document:1.2 xliff-core-1.2-transitional.xsd">
  <file datatype="xml" source-language="en-US" original="build-debug-project.md" target-language="ja-JP">
    <header>
      <tool tool-company="Microsoft" tool-version="1.0-7889195" tool-name="mdxliff" tool-id="mdxliff"/>
      <xliffext:skl_file_name>build-debug-project.30eb5a.5b842c4704b8505b07502eb3e87af85f7239a660.skl</xliffext:skl_file_name>
      <xliffext:version>1.2</xliffext:version>
      <xliffext:ms.openlocfilehash>5b842c4704b8505b07502eb3e87af85f7239a660</xliffext:ms.openlocfilehash>
      <xliffext:ms.sourcegitcommit>9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b</xliffext:ms.sourcegitcommit>
      <xliffext:ms.lasthandoff>05/15/2019</xliffext:ms.lasthandoff>
      <xliffext:ms.openlocfilepath>articles\dev-itpro\dev-tools\build-debug-project.md</xliffext:ms.openlocfilepath>
    </header>
    <body>
      <group extype="content" id="content">
        <trans-unit xml:space="preserve" translate="yes" id="101" restype="x-metadata">
          <source>Build and debug projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトのビルドおよびデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="102" restype="x-metadata">
          <source>In this tutorial, you’ll learn about using the tools in Visual Studio to analyze and debug code in the Fleet Management application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="103" restype="x-metadata">
          <source>You’ll go through a simple developer scenario in which you will set breakpoints, modify some code, and build the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="104">
          <source>Build and debug projects</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクトのビルドおよびデバッグ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="105">
          <source>In this tutorial, you’ll learn about using the tools in Visual Studio to analyze and debug code in the Fleet Management application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="106">
          <source>You’ll go through a simple developer scenario in which you will set breakpoints, modify some code, and build the result.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="107">
          <source>Prerequisites</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">必要条件</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="108">
          <source>Previous experience with code and Visual Studio is helpful to get the full benefit of this tutorial.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードおよび Visual Studio の以前の経験は、このチュートリアルを完全に活用するのに役立ちます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="109">
          <source>This tutorial requires you to access the environment using Remote Desktop and that you be provisioned as an administrator on the instance.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="110">
          <source>Key concepts</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">重要な概念</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="111">
          <source>The debugger in Visual Studio is used to analyze and debug code for your projects.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio のデバッガーは、プロジェクトのコードの分析とデバッグに使用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="112">
          <source>The standard features of the Visual Studio debugger are available to use when you're examining the running application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio デバッガーの標準機能は、実行中のアプリケーションを調べているときに使用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="113">
          <source>These features include modifying values of variables, setting breakpoints, and so on.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの機能には、変数の値の変更、ブレークポイントの設定などが含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="114">
          <source>IntelliSense and other features of Visual Studio are vital to efficient code editing and comprehension.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">IntelliSense および Visual Studio の他の機能は、効率的なコード編集および理解に不可欠です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="115">
          <source>Development is an iterative process.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発は反復的なプロセスです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="116">
          <source>After making modifications to the code, the project will be built, and changes can be tested.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードを変更すると、プロジェクトが作成され、変更をテストできます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="117">
          <source>Scenario</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">シナリオ</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="118">
          <source>The rental company has had unfortunate events when customers rent cars using credit cards that are past the expiration dates.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル会社は、顧客が有効期限を過ぎているクレジット カードを使用して車を借りているときに、不幸な出来事に見舞われました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="119">
          <source>You, the developer, are tasked with revising the application to help prevent this situation.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">開発者は、この状況の阻止を支援するために、アプリケーションを修正する責任を負います。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="120">
          <source>You’ll identify the problem by using the debugger in Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio のデバッガーを使用して、問題を特定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="121">
          <source>After the problem is identified, you’ll edit some code to implement a fix.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">問題識別された後は、修正を実装するためにいくつかのコードを編集します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="122">
          <source>Finally, you’ll build the project and validate that the fix was successful.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最後に、プロジェクトを構築し、修正プログラムが成功したことを検証します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="123">
          <source>Run to a breakpoint</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブレークポイントまで実行</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="124">
          <source>On the desktop, double-click the Visual Studio shortcut to open the development environment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="125">
          <source>Open the FleetManagement solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FleetManagement ソリューションを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="126">
          <source>On the <bpt id="p1">**</bpt>File<ept id="p1">**</ept> menu, point to <bpt id="p2">**</bpt>Open<ept id="p2">**</ept>, and then click <bpt id="p3">**</bpt>Project/Solution<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ファイル<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>開く<ept id="p2">**</ept>をポイントし、<bpt id="p3">**</bpt>プロジェクト/ソリューション<ept id="p3">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="127">
          <source>Browse to the desktop, and then open the <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> folder.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デスクトップを参照し、次に <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> フォルダーを開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="128">
          <source>If the solution file is not on your computer, the steps to create it are listed in <bpt id="p1">[</bpt>Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューション ファイルがコンピュータにない場合は、作成手順が「<bpt id="p1">[</bpt>チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する<ept id="p1">](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)</ept>」に記載されています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="129">
          <source>Select the file named <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> という名前のファイルを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="130">
          <source>The file type listed is SLN File.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">表示されるファイル タイプは SLN ファイルです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="131">
          <source>Click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="132">
          <source>Loading the solution may take some time.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ソリューションの読み込みには時間がかかる場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="133">
          <source>Make the <bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> project the startup project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FleetManagement<ept id="p1">**</ept> プロジェクトをスタートアップ プロジェクトにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="134">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click the <bpt id="p2">**</bpt>Fleet Management<ept id="p2">**</ept> project, and choose <bpt id="p3">**</bpt>Set as StartUp Project<ept id="p3">**</ept> in the context menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>フリート管理<ept id="p2">**</ept> プロジェクトを右クリックして、コンテキスト メニューで <bpt id="p3">**</bpt>スタートアップ プロジェクトとして設定<ept id="p3">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="135">
          <source>In <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, double-click the <bpt id="p2">**</bpt>Fleet Management<ept id="p2">**</ept> project to display its content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>フリート管理<ept id="p2">**</ept> プロジェクトをダブルクリックして内容を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="136">
          <source>Double-click the <bpt id="p1">**</bpt>Code<ept id="p1">**</ept> folder, and then double click the <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept> folder of the Fleet Management project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Code<ept id="p1">**</ept> フォルダーをダブルクリックしてから、フリート管理プロジェクトの <bpt id="p2">**</bpt>Classes<ept id="p2">**</ept> フォルダーをダブルクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="137">
          <source>Locate the <bpt id="p1">**</bpt>FMRentailCheckoutProcessor<ept id="p1">**</ept> class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FMRentailCheckoutProcessor<ept id="p1">**</ept> クラスを検索します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="138">
          <source>Right-click this class, and then click <bpt id="p1">**</bpt>Open<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスを右クリックしてから、<bpt id="p1">**</bpt>開く<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="139">
          <source>Alternatively, you can use the solution explorer search bar at the top of the solution explorer window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">または、ソリューション エクスプローラー ウィンドウの上部にあるソリューション エクスプローラーの検索バーを使用できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="140">
          <source>As you enter the name in the search bar, you'll see the corresponding artifacts selected in the solution explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検索バーに名前を入力すると、ソリューション エクスプローラーで選択された対応するコンポーネントが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="141">
          <source>You can now see the X++ code for the class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラスで X++ コードを表示できるようになりました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="142">
          <source>This class has a method named <bpt id="p1">**</bpt>FinalizeRentalCheckout<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このクラスには <bpt id="p1">**</bpt>FinalizeRentalCheckout<ept id="p1">**</ept> という名前のメソッドがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="143">
          <source>Place a breakpoint in this method on the line following the first comment.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">最初のコメントの次の行にあるこのメソッドにブレークポイントを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="144">
          <source>To do this, click in the margin to the left of the line of code where you want the debugger to pause execution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、デバッガで実行を一時停止するコード行の左側の余白をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="145">
          <source>You can also click anywhere in the line of code, and then press F9.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">また、コード行の任意の場所をクリックして、F9 を押すことができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="146">
          <source>The following illustration shows a breakpoint, which is displayed as a red-filled circle in the margin.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次の図はブレークポイントを示しています。ブレークポイントは余白に赤で塗りつぶされた円として表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="147">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>RedCircleMargin<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</ept> The FinalizeRentalCheckout method is called when a rental transaction is saved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>RedCircleMargin<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</ept>FinalizeRentalCheckout メソッドは、レンタルトランザクションが保存されるときに呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="148">
          <source>This method calls the delegate named RentalTransactionAboutTobeFinalizedEvent.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、RentalTransactionAboutTobeFinalizedEvent という名前のデリゲートを呼び出します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="149">
          <source>You can implement an event handler method, which is called by this delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このデリゲートで呼び出される、イベント ハンドラー メソッドを実装することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="150">
          <source>The method that calls the delegate passes a parameter, named RentalConfirmation, which contains a value that indicates whether the rental should be allowed or blocked.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デリゲートを呼び出すメソッドは、RentalConfirmation という名前のパラメーターを渡します。このパラメーターには、レンタルを許可するかブロックするかを示す値が含まれています。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="151">
          <source>If the rental is allowed, the value contains "true"; if it's blocked, the value contains "false".</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタルが許可されている場合、値に true が含まれ、ブロックされている場合は、値に false が含まれます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="152">
          <source>An event handler can change this value, based on any test the developer chooses to implement in code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラーは、開発者がコード内で実装するために選択するテストに基づいてこの値を変更できます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="153">
          <source>In this case, we'll modify the code to test the expiration date of the credit card.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">この場合、クレジット カードの有効期限をテストするコードを変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="154">
          <source>Press F5 to start the application for debugging, or, on the <bpt id="p1">**</bpt>Debug<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Start Debugging<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 を押してアプリケーションをデバッグのために起動するか、<bpt id="p1">**</bpt>デバッグ<ept id="p1">**</ept> メニューで <bpt id="p2">**</bpt>デバッグ開始<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="155">
          <source>It's important that you start the application in one of these ways.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの方法のいずれかでアプリケーションを開始することが重要です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="156">
          <source>If you don't, the Visual Studio debugger won't start, so you won't hit any of the breakpoints you've set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">しない場合は、Visual Studio デバッガーは起動されないため、設定されたブレークポイントのいずれかはヒットされません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="157">
          <source><bpt id="p1">**</bpt>Note<ept id="p1">**</ept>: The debugger needs to relate code position to source positions.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>注記<ept id="p1">**</ept>: デバッガーは、コードの位置をソースの位置に関連付ける必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="158">
          <source>It does this through consuming PDB files produced alongside the assemblies and net modules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アセンブリおよび net モジュールに沿って生成された PDB ファイルの消費を通じて実行されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="159">
          <source>The debugger will load symbols from the PDB files as described in the settings in the global tools settings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガーは、グローバル ツール設定の設定に示すように、PDBファイルから記号を読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="160">
          <source>To open the options page containing the setting that controls which symbols load, go to the <bpt id="p1">**</bpt>Tools<ept id="p1">**</ept> menu and choose <bpt id="p2">**</bpt>Options<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">読み込むシンボルを制御する設定を含むオプション ページを開くには、<bpt id="p1">**</bpt>ツール<ept id="p1">**</ept> メニューで <bpt id="p2">**</bpt>オプション<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="161">
          <source>In the <bpt id="p1">**</bpt>Microsoft Dynamics 365 for Finance and Operations<ept id="p1">**</ept> group, select the <bpt id="p2">**</bpt>Debugging<ept id="p2">**</ept> page.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Microsoft Dynamics 365 for Finance and Operations<ept id="p1">**</ept> グループで、<bpt id="p2">**</bpt>デバッグ<ept id="p2">**</ept> ページを選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="162">
          <source>If this option is selected, the system will load symbols from only the PDB files related to the artifacts in the current solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションが選択されている場合、システムは、現在のソリューションのコンポーネントに関連する PDB ファイルのみから記号を読み込みます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="163">
          <source>This reduces the startup time significantly, so be sure it’s selected for this lab.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより起動時間が大幅に短縮されるため、このラボでは必ずそれを選択してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="164">
          <source>Be aware that when this option is selected, it won’t be possible to see source code from entities outside of the current solution.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このオプションを選択すると、現在のソリューションの外部にあるエンティティからソース コードを確認することはできません。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="165">
          <source>After a few moments, the browser will start and display the startup object that was selected in the project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">数分後、ブラウザーが起動し、プロジェクトで選択されたスタートアップ オブジェクトを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="166">
          <source>The <bpt id="p1">**</bpt>Current Rentals<ept id="p1">**</ept> page will open.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>現在のレンタル<ept id="p1">**</ept> ページが開きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="167">
          <source>In the Action Pane, click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">アクション ウィンドウで、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="168">
          <source>When the page is displayed, click <bpt id="p1">**</bpt>Show list<ept id="p1">**</ept> in the <bpt id="p2">**</bpt>Show/Hide<ept id="p2">**</ept> list (or press <bpt id="p3">**</bpt>Ctrl+F8<ept id="p3">**</ept>).</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ページが表示されたら、<bpt id="p2">**</bpt>表示/非表示<ept id="p2">**</ept> リストで <bpt id="p1">**</bpt>リストの表示<ept id="p1">**</ept> をクリックします (または <bpt id="p3">**</bpt>Ctrl+F8<ept id="p3">**</ept> を押します)。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="169">
          <source>Make a change to any existing rental.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のレンタルに変更を加えます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="170">
          <source>For example, click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>, and change the time that the rental period started.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept>をクリックして、レンタル期間が開始した時刻を変更します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="171">
          <source>Click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept> to force a validation of the rental record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レンタル レコードを強制的に検証するには、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="172">
          <source>The method in which you placed a breakpoint is called.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ブレークポイントを配置するメソッドが呼び出されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="173">
          <source>Execution pauses at the line of code that contains the breakpoint.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行は、ブレークポイントを含むコード行で一時停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="174">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>ForceValidation<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</ept> While the application is paused at a breakpoint, you can examine the application state.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ForceValidation<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</ept> アプリケーションがブレークポイントで一時停止している間に、アプリケーションの状態を調べることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="175">
          <source>Use the same techniques that you typically would for any application developed with Visual Studio.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">通常 Visual Studio で開発するアプリケーションと同じ方法を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="176">
          <source>For example, place the cursor over a variable or a parameter to see its value in a tooltip.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、ツールヒントでその値を表示する変数またはパラメーターにカーソルを置きます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="177">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Tooltip<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>Tooltip<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="178">
          <source>The other debugging tools in Visual Studio are available as well.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の他のデバッグ ツールも利用することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="179">
          <source>For example, the <bpt id="p1">**</bpt>Locals<ept id="p1">**</ept> window shows all of the local variables for the location where execution has stopped.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>ローカル<ept id="p1">**</ept>ウィンドウは、実行が停止した場所のすべてのローカル変数を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="180">
          <source>Click the <bpt id="p1">**</bpt>Locals<ept id="p1">**</ept> tab at the bottom of Visual Studio, and expand the <bpt id="p2">**</bpt>fmrentalrecord<ept id="p2">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio の下部にある <bpt id="p1">**</bpt>ローカル<ept id="p1">**</ept> タブをクリックし、<bpt id="p2">**</bpt>fmrentalrecord<ept id="p2">**</ept> 変数を展開します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="181">
          <source>You will see the internal state of the record, showing the values of all the fields in the record.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">レコード内のすべてのフィールドの値を示す、レコードの内部状態が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="182">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>InternalState<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</ept> Notice the value of the <bpt id="p2">**</bpt>Vehicle<ept id="p2">**</ept> property of the <bpt id="p3">**</bpt>fmrentalrecord<ept id="p3">**</ept> variable.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>InternalState<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</ept> <bpt id="p3">**</bpt>fmrentalrecord<ept id="p3">**</ept> 変数の<bpt id="p2">**</bpt>車両<ept id="p2">**</ept>プロパティの値に注目してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="183">
          <source>This property is a foreign key field in the <bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このプロパティは、<bpt id="p1">**</bpt>FMRental<ept id="p1">**</ept> テーブルの外部キー フィールドです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="184">
          <source>The debugger allows us to peek into the related record in the FMVehicle table.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">デバッガーを使用すると、FMVehicle テーブルの関連するレコードを調べることができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="185">
          <source>It shows values that belong to the <bpt id="p1">**</bpt>AutoIdentification<ept id="p1">**</ept> field group.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>AutoIdentification<ept id="p1">**</ept> フィールド グループに属する値を示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="186">
          <source>The <bpt id="p1">**</bpt>Breakpoints<ept id="p1">**</ept> window lists all of the breakpoints that have been set.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブレークポイント<ept id="p1">**</ept> ウィンドウには、設定されているすべてのブレークポイントが一覧表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="187">
          <source>Click the <bpt id="p1">**</bpt>Breakpoints<ept id="p1">**</ept> tab to see its content.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ブレークポイント<ept id="p1">**</ept> タブをクリックし、コンテンツを表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="188">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>Breakpoint<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>ブレークポイント<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="189">
          <source>Press F10 a few times to step through the code, line-by-line, and use the full complement of debugger features.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F10 キーを数回押してコードを 1 行ずつ実行し、デバッガー機能の完全な補完を使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="190">
          <source>Notice that the <bpt id="p1">**</bpt>Locals<ept id="p1">**</ept> window updates the values of variables immediately with each statement that's executed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>ローカル<ept id="p1">**</ept> ウィンドウが、実行される各ステートメントですぐに変数の値を更新することに注意します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="191">
          <source>On the toolbar, click <bpt id="p1">**</bpt>Continue<ept id="p1">**</ept>, or press F5</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ツール バーで、<bpt id="p1">**</bpt>続行<ept id="p1">**</ept>をクリックするか、F5 を押します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="192">
          <source>Close Internet Explorer to close the <bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> application.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を閉じ、<bpt id="p1">**</bpt>Fleet Management<ept id="p1">**</ept> アプリケーションを閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="193">
          <source>Visual Studio will exit the debugging mode.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio はデバッグ モードを終了します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="194">
          <source>An alternative is to choose <bpt id="p1">**</bpt>Stop Debugging<ept id="p1">**</ept> from the <bpt id="p2">**</bpt>Debug<ept id="p2">**</ept> menu.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">代替は<bpt id="p1">**</bpt>デバッグの停止<ept id="p1">**</ept>を<bpt id="p2">**</bpt>デバッグ<ept id="p2">**</ept>メニューから選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="195">
          <source>This will leave Internet Explorer open, allowing the next debugging session to start faster.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これにより、Internet Explorer は開いたままになり、次のデバッグ セッションをより早く開始することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="196">
          <source>Add the validation code</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">検証コードの追加</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="197">
          <source>In the <bpt id="p1">**</bpt>FinalizeRentalCheckout<ept id="p1">**</ept> method, you saw that the developer added code to call the delegate that’s used to determine the validity of the rental.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>FinalizeRentalCheckout<ept id="p1">**</ept> メソッドでは、開発者がコードを追加してレンタルの有効性を決定するために使用されるデリゲートを呼び出したことを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="198">
          <source>To solve the problem of expired credit cards, you’ll add an event handler, which you’ll use to verify that that the credit card isn’t expired.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">期限切れのクレジット カードの問題を解決するには、クレジット カードが期限切れではないことを確認するために使用するイベント ハンドラを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="199">
          <source>To simplify the lab, the handler will be added in the same file that contains the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ラボを簡素化するために、ハンドラはデリゲートを含む同じファイルに追加されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="200">
          <source>Use the following code as inspiration.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">インスピレーションとして、次のコードを使用します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="201">
          <source>Rather than copying and pasting the code, type it in manually to see the IntelliSense features in action.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードをコピーして貼り付けるのではなく、手動で入力して IntelliSense 機能の動作を参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="202">
          <source>These features add to the high level of productivity that Visual Studio users expect.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの機能により、Visual Studio ユーザーは高い生産性を期待することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="203">
          <source>The preceding code is straightforward.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">上記のコードはわかりやすいです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="204">
          <source>The method is marked as handler for the relevant delegate by using the <bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> attribute, as shown.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このメソッドは、<bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> 属性を使用して、関連するデリゲートのハンドラーとしてマークされています (図参照)</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="205">
          <source>In the code, the customer record is retrieved, and then the credit card date is compared to today's date.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードでは、顧客レコードが取得されてから、クレジット カードの日付が今日の日付と比較されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="206">
          <source>If the expiration date of the credit card is in the past, the event handler sets a value in the <bpt id="p1">**</bpt>RentalConfirmation<ept id="p1">**</ept> structure to signal that the customer isn't eligible to rent a vehicle.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クレジット カードの有効期限が過ぎている場合は、<bpt id="p1">**</bpt>RentalConfirmation<ept id="p1">**</ept> 構造でイベント ハンドラーの値を設定し、顧客が車両の貸し出しの対象ではないことを通知します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="207">
          <source>The idea is that any number of handlers can subscribe to the delegate.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これは、任意の数のハンドラーがデリゲートにサブスクライブできるようにするためです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="208">
          <source>If any handler determines that a rental should not proceed, it sets the <bpt id="p1">**</bpt>OkToRent<ept id="p1">**</ept> flag to false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラーでレンタルを続行しないと決定した場合、<bpt id="p1">**</bpt>OkToRent<ept id="p1">**</ept> フラグを設定します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="209">
          <source>A superior implementation might refrain from doing any analysis if it determines that the <bpt id="p1">**</bpt>OkToRent<ept id="p1">**</ept> flag has already been set to false.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">優れた実装では、<bpt id="p1">**</bpt>OkToRent<ept id="p1">**</ept> フラグがすでに false に設定されていると判断した場合、分析を行わないことがあります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="210">
          <source>Be sure that you're working in the FMRentalCheckoutProcessor.xpp file.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">FMRentalCheckoutProcessor.xpp ファイルで作業していることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="211">
          <source>Begin by adding the new event handler definition to the FMRentalCheckoutProcessor class.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">新しいイベント ハンドラー定義を FMRentalCheckoutProcessor クラスに追加することによって開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="212">
          <source>Add the following code on an empty line just above the brace (}) that marks the end of the class definition.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">クラス定義の終了を示す波括弧 (}) のすぐ上の空の明細行に次のコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="213">
          <source>Add the attributes to the beginning of the event handler.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">イベント ハンドラーの先頭に、属性を追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="214">
          <source>These attributes indicate which delegate the event handler is subscribing to.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらの属性は、イベントハンドラーがどのデリゲートに加入しているかを示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="215">
          <source>Now, add the code that checks the credit card expiration value.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ここで、クレジット カードの有効期限の値を確認するコードを追加します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="216">
          <source>The completed method should look similar to the following code.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">完了したメソッドは、次のコードのようになります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="217">
          <source>Make sure the handler and the delegate are separated by exactly one blank line.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ハンドラーとデリゲートが 1 行の空白行で区切られていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="218">
          <source>On the toolbar in Visual Studio, click <bpt id="p1">**</bpt>Save<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Visual Studio のツールバーで、<bpt id="p1">**</bpt>保存<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="219">
          <source>After you're satisfied with the code, build the code for the Fleet Management project.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードに問題がなければ、フリート管理プロジェクトのコードをビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="220">
          <source>To do this, in <bpt id="p1">**</bpt>Solution Explorer<ept id="p1">**</ept>, right-click the <bpt id="p2">**</bpt>FleetManagement<ept id="p2">**</ept> project name, and then click <bpt id="p3">**</bpt>Build<ept id="p3">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを行うには、<bpt id="p1">**</bpt>ソリューション エクスプローラー<ept id="p1">**</ept> で、<bpt id="p2">**</bpt>FleetManagement<ept id="p2">**</ept> プロジェクト名を右クリックし、<bpt id="p3">**</bpt>Build<ept id="p3">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="221">
          <source>You may see errors or warnings if the code isn't correct.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コードが正しくない場合は、エラーまたは警告が表示される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="222">
          <source>If so, correct the code, and build again until all warnings and errors have been resolved.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その場合は、コードを修正し、再度ビルド警告やエラーが解決されるまでビルドを続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="223">
          <source>You're now ready to validate that the revision works as intended.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これで、リビジョンが意図したとおりに動作することを確認する準備が整いました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="224">
          <source>On the <bpt id="p1">**</bpt>Debug<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Delete All Breakpoints<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>デバッグ<ept id="p1">**</ept>メニューをクリックして、<bpt id="p2">**</bpt>すべてのブレークポイントを削除<ept id="p2">**</ept>します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="225">
          <source>Place a new breakpoint in the event-handler method at the line that contains the following statement:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">次のステートメントを含む明細行にあるイベント ハンドラー メソッドに新しいブレークポイントを配置します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="226">
          <source>Start the Fleet Management sample with debugging active by pressing F5.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押してデバッグをアクティブにし、フリート管理サンプルを開始します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="227">
          <source>Browse to the <bpt id="p1">**</bpt>Current rentals<ept id="p1">**</ept> page, as described starting in step 11 of the previous section.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">前のセクションのステップ 11 で説明されているように<bpt id="p1">**</bpt>現在のレンタル<ept id="p1">**</ept> ページを参照してください。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="228">
          <source>Select one of the reservations, and click <bpt id="p1">**</bpt>Edit<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いずれかの予約を選択し、<bpt id="p1">**</bpt>編集<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="229">
          <source>In the <bpt id="p1">**</bpt>Customer<ept id="p1">**</ept> drop-down list, select Adrian Lannin from the list, and then click <bpt id="p2">**</bpt>Save<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>顧客<ept id="p1">**</ept>ドロップダウン リストで、一覧から Adrian Lannin を選択して<bpt id="p2">**</bpt>保存<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="230">
          <source>Execution pauses at the breakpoint that you set in the event-handler method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">実行は、イベントハンドラー メソッドで設定したブレークポイントで一時停止します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="231">
          <source>Press F10 three times to step through the code block.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F10 キーを 3 回押して、コード ブロックを実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="232">
          <source><bpt id="p1">[</bpt><ph id="ph1">![</ph>StepCodeBlock<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</ept></source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">[</bpt><ph id="ph1">![</ph>StepCodeBlock<ph id="ph2">\_</ph>BuildDebugProj<ept id="p1">](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</ept></target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="233">
          <source>To see the code map for the call stacks, right-click in the code editor, and then click <bpt id="p1">**</bpt>Show Call Stack on Code Map<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コール スタックのコード マップを表示するには、コード エディターを右クリックし、<bpt id="p1">**</bpt>コード マップにコール スタックを表示<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="234">
          <source>You may want to add a comment to the call stack, step through the code, and watch as the code map changes accordingly.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">呼び出し履歴にコメントを追加し、コードを進め、それに応じたコード マップの変更としてウォッチすることが必要な場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="235">
          <source>Press F5 to continue.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">F5 キーを押して続行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="236">
          <source>You'll see that the customer has been disallowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">その顧客が許可されていないことが表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="237">
          <source>In the same rental, change the customer name to Phil Spencer, and then click <bpt id="p1">**</bpt>Update<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">同じレンタルで、顧客名を Phil Spencer に変更してから<bpt id="p1">**</bpt>更新<ept id="p1">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="238">
          <source>This time, the transaction is allowed.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">今回は、トランザクションが可能です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="239">
          <source>Close Internet Explorer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">Internet Explorer を閉じます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="240">
          <source>Comment out the <bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> attribute on the <bpt id="p2">**</bpt>RentalFinalizedEventHandler<ept id="p2">**</ept> method.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p2">**</bpt>RentalFinalizedEventHandler<ept id="p2">**</ept> メソッドで <bpt id="p1">**</bpt>SubscribesTo<ept id="p1">**</ept> をコメントにします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="241">
          <source>This step ensures that the credit card test will no longer run as you work on the remaining tutorials.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このステップでは、残りのチュートリアルで作業してもクレジット カード テストが実行されなくなります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="242">
          <source>Best practices</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="243">
          <source>Earlier in this tutorial, you had the opportunity to add code to the project and build the solution with your changes.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このチュートリアルの前半では、プロジェクトにコードを追加し、変更を加えてソリューションをビルドする営業案件を得ました。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="244">
          <source>The build process may not have been successful, requiring you to refer to the error window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ビルド プロセスが成功しなかったため、エラー ウィンドウを参照する必要があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="245">
          <source>Using this window, you can get to the error by clicking on the line that describes the error.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このウィンドウを使用しているとき、エラーを説明する明細行をクリックすると、エラー状態になります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="246">
          <source>You may have noticed some diagnostic messages that don’t represent compilation errors.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">コンパイル エラーを表していないいくつかの診断メッセージが通知される場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="247">
          <source>These are diagnostics from the <bpt id="p1">**</bpt>Best Practice<ept id="p1">**</ept> checker.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これらは、<bpt id="p1">**</bpt>ベスト プラクティス<ept id="p1">**</ept> チェッカーからの診断です。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="248">
          <source>This tool will check for instances where the developer has violated a known best practice, and display a warning when one is found.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">このツールは、開発者が既知のベスト プラクティスに違反したインスタンスをチェックして、違反が見つかったときに警告を表示します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="249">
          <source>The Best Practice rules apply to both code constructs and metadata.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス ルールは、コードの構成要素とメタデータの両方に適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="250">
          <source>Each software development organization is likely to have its own set of best practices that they enforce.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">各ソフトウェアの開発組織は、実施するベスト プラクティスのセットを持つ可能性が高いです。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="251">
          <source>They may want to disregard some of the existing best practice checks.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">既存のベスト プラクティス チェックの一部を無視する場合があります。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="252">
          <source>To support this, the set of reported best practice diagnostics can be modified by the individual developer.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これをサポートするために、報告されたベスト プラクティスの診断セットを個々の開発者が変更することができます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="253">
          <source>To demonstrate this, complete the following steps:</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">これを実証するには、次の手順を実行します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="254">
          <source>On the <bpt id="p1">**</bpt>View<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Error List<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>表示<ept id="p1">**</ept>メニューで、<bpt id="p2">**</bpt>エラー リスト<ept id="p2">**</ept>をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="255">
          <source>You should see a small number of best practice warnings.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">いくつかのベスト プラクティス警告が表示されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="256">
          <source>On the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> menu, click <bpt id="p2">**</bpt>Options<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> メニューで、<bpt id="p2">**</bpt>オプション<ept id="p2">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="257">
          <source>In the <bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> group, choose <bpt id="p2">**</bpt>Best Practices<ept id="p2">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>Dynamics 365<ept id="p1">**</ept> グループで、<bpt id="p2">**</bpt>ベスト プラクティス<ept id="p2">**</ept> を選択します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="258">
          <source>In the <bpt id="p1">**</bpt>Model<ept id="p1">**</ept> drop-down list, make sure that the <bpt id="p2">**</bpt>Fleet Management<ept id="p2">**</ept> model is selected.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm"><bpt id="p1">**</bpt>モデル<ept id="p1">**</ept> ドロップダウン リストで、<bpt id="p2">**</bpt>フリート管理<ept id="p2">**</ept>モデルが選択されていることを確認します。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="259">
          <source>The best practice rules apply to a particular model.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス ルールは、特定のモデルに適用されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="260">
          <source>Mark the selections for some of the sets of Best Practice rules.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">ベスト プラクティス ルールのセットの一部に対する選択内容をマークします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="261">
          <source>For example, if you select the entry for <bpt id="p1">**</bpt>CodeStyleRules<ept id="p1">**</ept>, best practice guidelines for variables will be examined.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">たとえば、<bpt id="p1">**</bpt>CodeStyleRules<ept id="p1">**</ept> のエントリを選択する場合、変数のベスト プラクティスのガイドラインが検査されます。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="262">
          <source>After you've updated the selections, click <bpt id="p1">**</bpt>OK<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">選択を更新した後、<bpt id="p1">**</bpt>OK<ept id="p1">**</ept> をクリックします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="263">
          <source>Rebuild the Fleet Management project by right-clicking the project name and then clicking <bpt id="p1">**</bpt>Rebuild<ept id="p1">**</ept>.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">プロジェクト名を右クリックして <bpt id="p1">**</bpt>リビルド<ept id="p1">**</ept> をクリックすることにより、フリート管理プロジェクトをリビルドします。</target></trans-unit>
        <trans-unit xml:space="preserve" translate="yes" id="264">
          <source>You'll notice that the violations of the best practice rules that you specified appear in the <bpt id="p1">**</bpt>Error list<ept id="p1">**</ept> window.</source>
        <target logoport:matchpercent="101" state="translated" state-qualifier="leveraged-tm">指定したベスト プラクティス ルールの違反が <bpt id="p1">**</bpt>エラー一覧<ept id="p1">**</ept> ウィンドウに表示されることがわかります。</target></trans-unit>
      </group>
    </body>
  </file>
</xliff>