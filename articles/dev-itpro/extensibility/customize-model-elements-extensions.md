---
title: "拡張機能によってモデル要素をカスタマイズする"
description: "このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。 Dynamics AX の拡張機能を示すために、このモデルにはフリート管理アプリケーションの機能を拡張する要素が含まれています。"
author: robadawy
manager: AnnBe
ms.date: 11/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 11184
ms.assetid: 3190f6e2-698a-4cfa-9a2d-a6c57354920a
ms.search.region: Global
ms.author: robadawy
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 739033a750925d948039e3ed52eee33336d2e56e
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="customize-model-elements-through-extension"></a>拡張機能によってモデル要素をカスタマイズする

[!include [banner](../includes/banner.md)]

このチュートリアルでは、フリート管理拡張モデルを詳しく見ていきます。 このモデルには、フリート管理アプリケーションの機能を拡張する要素が含まれています。 *拡張機能* を作成することにより、モデル要素をカスタマイズすることができます。 Microsoft Dynamics AX 2012 の オーバーレイ機能とは異なり、拡張機能はベースライン モデル要素をオーバーレイしません。 代わりに、拡張機能はモデルと関連付けられているビジネス ロジックに追加またはカスタマイズする別のアセンブリとしてコンパイルされます。 テーブルにフィールドを追加、またはフォームにコントロールを追加することなどによりメタデータを拡張、およびイベント ハンドラおよびプラグイン クラスを定義することによりビジネス ロジックを拡張またはカスタマイズすることができます。 テーブル、フォーム、フォーム データ ソース、フォーム コントロール、およびその他を使用して、様々な定義済みイベントでイベント ハンドラーを作成することができるようになりました。 プラグインは、アプリケーションのビジネス ロジックを交換または拡張するできるようにする新しい機能拡張の概念でもあります。

## <a name="prerequisites"></a>前提条件
このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。

## <a name="understanding-the-fleet-management-model"></a>フリート管理モデルを理解する
フリート管理アプリケーションは、車両、顧客、および車両予約を管理するためのシステムをレンタル自動車会社に提供します。 アプリケーションは、フリート係とフリート マネージャの役割で使用されるよう設計されています。

### <a name="fleet-clerk"></a>フリート係

担当者は、顧客との対面または電話でのやり取りを処理する受付従業員です。 担当者は主に、アプリケーションに顧客情報を入力する、顧客の車両予約を作成する、車両アクセサリをオファーすることで予約をアップセルする、車両レンタルの終了時に車両の返却を処理することに関心を持っています。 担当者は、各自のニーズを予測し、楽しくて印象的なエクスペリエンスを提供しながら、顧客とやり取りすることにより、**フリート管理ワークスペース**を使用して顧客とのやり取りを準備することに大部分の時間を費やします。

### <a name="fleet-manager"></a>フリート マネージャー

マネージャーは、業務要件とプロセスの設定を処理するバック オフィス従業員です。 マネージャーは、車両の情報を入力する、使用可能な車両アクセサを定義する、車両メンテナンス、価格を決定する、および収益、アップセルの成功などのビジネス パフォーマンス測定を分析することに主に関心を持っています。 アプリケーションのビジネス ロジックは、次の 3 つの主なエンティティとそれらの間の関係を中心に展開されます。

### <a name="customers"></a>顧客

顧客は、車両の予約を行い、車両のアクセサリを選択し、車両をチェックアウトおよび返却をし、車両のレンタル料を支払うためにフリート係に連絡します。 顧客関連の情報は、**FMCustomer** というテーブルに保管されています。

### <a name="vehicles"></a>車両及び運搬具

車両は主として価格が異なり、車両の*クラス*に比例します。 車両に関する情報を格納するテーブルの名前は、「FMVehicle」で始まります。**

### <a name="reservations-and-rentals"></a>引当とレンタル

引当は、顧客および車両間の関係を処理します。 引当情報には、引当日、顧客情報、車両の選択と価格、およびアクセサリや手数料などの追加の雑費が含まれます。 引当やレンタル情報は、**FMRental** および **FMRentalCharge** テーブルに格納されます。 計算エンジンは、車両予約の価格決定に関連するトランザクションの情報を処理します。 このデータ モデルを使用すると、フリート管理アプリケーションは基本的な自動車レンタル経験を提供します。

## <a name="extending-the-fleet-management-model"></a>フリート管理モデルを拡張
基本的なフリート管理アプリケーションは、追加機能でカスタマイズされています。これらの機能によりレンタカー会社は、割引を使用して顧客に価格インセンティブを提供することができます。 これらの割引機能を使用可能にする追加のビジネス ロジックおよびデータは、フリート管理拡張モデルに格納されます。 割引機能は、3 つの主要なカスタマイズを介してフリート管理アプリケーションに価値を追加します。

### <a name="the-fleet-management-extension-data-model"></a>フリート管理拡張モデル

割引に関連する情報を格納する 2 つの新しいテーブルが追加されました。 **FEDiscounts** には、すべての割引とその料金のリストが保存されています。 **FERentalDiscountRelationTable** は割引が適用される引当を追跡します。 既存のテーブルは、価格設定スキームへの割引口座に拡張されました。 **FMRental** という特定の予約の車両料金を追跡するテーブルは、車両料金の割引に対応するように拡張されました。 **FMRentalCharge** という予約のアクセサリーを追跡しているテーブルは、アクセサリーに適用される割引に対応するために拡張されました。

### <a name="the-fleet-management-extension-calculation-engine"></a>フリート管理拡張計算エンジン

基本的な計算エンジンには、カスタマイズにより、新しい割引によって定義されたさまざまな価格決定スキーマが追加されています。 プラグイン クラスによって、基本計算エンジンの機能が置き換えられました。 車両の予約が 7 日間を超えるときは、車両フリート管理モデルが、車両の 1 日当たりの料金とより低い 1 週間あたりの料金との差に基づいて、節約を計算します。 プラグインは、同じ動作を割引を使用して実現できるため、1 週間あたりの料金の計算を削除します。

### <a name="the-fleet-management-user-interface-extensions"></a>フリート管理ユーザー インターフェイス拡張

**FMRental** という名前のフォームに組み込まれている Rental は、担当者が予約に割引を適用できるように拡張されています。 画面上の価格の概要は、予約に関連する車両およびアクセサリに適用可能な割引に関する貯蓄情報によってリアルタイムで更新されます。 次の手順では、フリート管理拡張モデルでのカスタマイズを調べて、自分でカスタマイズの一部を再実装します。

## <a name="setup"></a>段取り
前のチュートリアルでフリート管理ソリューションを開いていない場合は、以下の手順を実行します。 フリート管理ソリューション ファイルは、Dynamics AX ダウンロード可能 VM で利用できます。

1.  **デスクトップ**で、**Visual Studio** ショートカットをダブルクリックして、開発環境を開きます。
2.  **FleetManagement** ソリューションを開きます。 **ファイル**メニューで、**開く**をポイントし、**プロジェクト/ソリューション**をクリックします。
3.  デスクトップを参照し、**FleetManagement** フォルダーを開きます。 ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。
4.  **FleetManagement** という名前のソリューション ファイルを選択します。 表示されるファイル タイプは Microsoft Visual Studio Solution です。
5.  **開く** をクリックします。 ソリューションを開くには時間がかかる場合があります。



### <a name="installing-the-demo-data"></a>デモ データのインストール

デモ データを既にインストールしている場合、次のセクションに進めます。

1.  VM で、Internet Explorer を開き、アプリケーションのベース URL に移動します。
2.  サインインします。
3.  ダッシュ ボードで、ナビゲーション ウィンドウを開き、**フリート管理 &gt; 設定 &gt; フリート設定**に移動します。 [![フリート設定 > カスタマイズ モデル](./media/fleetsetup_customizemodel.png)](./media/fleetsetup_customizemodel.png)
4.  **デモ データの設定**をクリックします。 

    [![コンフィギュレーション > モデルをカスタマイズする](./media/configuration_customizemodel.png)](./media/configuration_customizemodel.png)

5.  デモ データの再読み込みを促すメッセージが表示されたら、**はい**をクリックします。
6.  データが読み込みを完了したら、**閉じる** をクリックします。
7.  ダッシュ ボードで、ナビゲーション バーを開き、**システム管理 &gt; 共通 &gt; 集計の測定を維持**に移動します。 (手順 7 ～ 9 は、新しいリリースでは適用できません)
8.  **FMAggregateMeasurements** を選択し、アクション ペインで **今すぐ更新** をクリックします。
9.  処理が完了するまで待機します。 進行中の処理は、一連の移動するドットによってページの上部に示されます。 インジケータが消えて、**前回処理時刻** フィールドが更新されると、処理が完了します。

## <a name="open-the-fmrental-form-on-the-one-box-environment"></a>1 ボックス環境で FMRental フォームを開く
1.  VM で、Internet Explorer を開き、Dynamics AX アプリケーションのベース URL に移動します。 詳細については、[Microsoft Dynamics AX インスタンスへのアクセス](../dev-tools/access-instances.md) を参照してください。
2.  求められた場合にログインします。
3.  **予約管理**タイルを検索し、予約管理ワークスペースを開くためそれをクリックします。 

    [![予約管理タイル](./media/reservationmanagementtile.jpg)](./media/reservationmanagementtile.jpg)

4.  **予約管理** ワークスペースが開いたら、**現在のレンタル** をクリックします。 

    [![現在のレンタル](./media/reservationmanagementworkspace.jpg)](./media/reservationmanagementworkspace.jpg)

5.  これにより、グリッド ビューで **レンタル** フォームが開きます。 

    [![レンタル フォーム](./media/rentalform_customizemodel.png)](./media/rentalform_customizemodel.png)

6.  **レンタル** フォームを実行した後、**オプション &gt; ビューの変更 &gt; ヘッダー** をクリックして、**ヘッダーの表示**を開きます。

    [![ヘッダーの表示](./media/headerview_customizemodel.png)](./media/headerview_customizemodel.png)

7.  **ヘッダーの表示**フォームを読み込んだら、下までスクロールし、**割引** タブを展開します。このタブはフリート管理モデルに含まれていません。 これは、**FMRental** フォームに対する拡張機能としてフリート管理拡張モデルでモデリングされています。

    [![割引](./media/discounts_customizemodel.png)](./media/discounts_customizemodel.png)

8.  割引を追加するために**追加**をクリックします。
9.  **得意先** 割引を選択し、**OK** をクリックします。 選択した割引が **割引** グリッドに追加されます。 

    [![得意先割引](./media/fcdiscount_customizemodel.png)](./media/fcdiscount_customizemodel.png)

10. FactBox を開くには、ショートカット キー **Alt+F2** を使用します。
11. 右側の**レンタル合計**情報ボックスを展開し、適用されるディスカウントの割引を表示します。 

    [![レンタル合計](./media/rentaltotal_customizemodel.png)](./media/rentaltotal_customizemodel.png)

## <a name="overview-of-the-fleet-management-discount-extension-project"></a>フリート管理割引の拡張プロジェクトの概要
このチュートリアルでは、**FleetManagementDiscounts** プロジェクトに**フリート管理拡張**という名前のモデルに属しているモデルの要素が含まれます。 ここで、プロジェクト要素について調べ、学びます。

### <a name="navigate-to-fmrentalextension-in-the-tree-designer"></a>ツリー デザイナーで FMRental.Extension に移動します。

1.  Visual Studio の**ソリューション エクスプローラー**の **FleetManagement 割引**プロジェクトで、**ユーザー インターフェイス &gt; フォーム機能拡張**と展開します。 

    [![ソリューション エクスプローラー](./media/solutionexplorer1_customizemodel.png)](./media/solutionexplorer1_customizemodel.png)

    **FMRental.Extension** 要素は、2 つの新しいデータ ソースと新しいタブ コントロールを追加することによって **FMRental** フォームの機能を拡張する拡張要素です。
2.  **ソリューション エクスプローラー**で、**FMRental.Extension** をダブルクリックしてデザイナーを開きます。 次のイメージに示します。
    -   *斜体*のテキストで示されているデータ ソースはベースライン フォームで定義されているデータ ソースです。
    -   **太字**で示されているデータ ソースは現在の拡張子で定義されています。

    デザイナーは、その拡張機能を含めて、モデル要素の統合ビューを表示します。 読み取り専用ノードは斜体で表示さえｒますが、現在の拡張機能に属するノードはカスタマイズの種類を示す他の視覚的な記号と共に太字で表示されます。 

    [![FMRentalExt\_CustomizeModel](./media/fmrentalext_customizemodel.png)](./media/fmrentalext_customizemodel.png)

3.  デザイナーの検索ボックスに、次の図に示すように「e:」と入力します。 現在のデザイナーがフィルター処理され、現在の拡張に属するノードのみが表示されます。 

    [![現在の拡張機能](./media/rentalext-e_customizemodel.png)](./media/rentalext-e_customizemodel.png)

4.  また、'e:LineViewDiscounts' と入力してデザイナーをフィルター処理し、**LineViewDiscounts** という名前と一致し現在の拡張子に属するノードを表示することができます。 

    [![LineViewDiscounts](./media/lineviewdiscounts_customizemodel.png)](./media/lineviewdiscounts_customizemodel.png)

5.  内容を確認するには、**LineViewDiscounts** ノードを展開します。 

    [![LineViewDiscounts ノードの展開](./media/expandlvdnode_customizemodel.png)](./media/expandlvdnode_customizemodel.png)

### <a name="open-the-fmrentalextension-xml-file-to-view-the-metadata"></a>FMRental.Extension XML ファイルを開いてメタデータを表示

1.  **ソリューション エクスプローラー**で、FMRental.Extension フォーム拡張子をクリックしてから**プログラムから開く**をクリックします。
2.  **プログラムから開く**ダイアログ ボックスで、**XML (テキスト) エディター**を選択してから **OK** をクリックします。
3.  デザイナーを閉じるように求めるメッセージが表示されたら、**はい** をクリックします。
4.  対応するマイナス記号をクリックすると、**制御**および**データ ソース** ノードの子ノードが折りたたまれます。 正しい結果については次の図を参照してください。 

    [![レンタル コード](./media/fmrentalcode_customizemodel.png)](./media/fmrentalcode_customizemodel.png) 

    XML ファイルには、**FMRental.Extension** 要素に関連付けられているメタデータが含まれます。 このファイルに、拡張機能の一部である 1 つのみのタブ ページ コントロールおよび 2 つのデータ ソースを説明するメタデータが含まれることがわかります。 基本フォームからのメタデータが含まれていないことを確認することもできます。

### <a name="view-other-elements-in-the-fleet-management-discount-extension-project"></a>フリート管理割引の拡張プロジェクトのその他の要素の表示

**FleetManagement Discounts** プロジェクトには 2 つの新しいテーブル **FEDiscount** および **FERentalDiscountRelationTable** と、既存のフリート管理テーブル **FMRental** および **FMRentalCharge** への 2 つの拡張が含まれています。

1.  **ソリューション エクスプローラー**の FleetManagement 割引で**データ モデル &gt; テーブル拡張機能 &gt; FMRental.Extension** をダブルクリックしてデザイナーを開きます。
2.  **フィールド**ノードを展開し、拡張子に追加されたフィールド FEVehicleRateDiscount がベース FMRental テーブルに含まれていることを確認します。 

    [![FEVehicleRateDiscount](./media/nodes_customizemodel.png)](./media/nodes_customizemodel.png)

3.  同様に、デザイナーで **FMRentalChange.Extension** 要素を開いて、その内容を調べます。

### <a name="inspect-the-data-event-handlers"></a>データ イベント ハンドラーの検査

**ソリューション エクスプローラー**の FleetManagement 割引プロジェクトで、**コード &gt; クラス &gt; FMRentalCharge\_Extension** をダブルクリックしてコード エディターを開きます。 

[![FMRentalChargeCode](./media/fmrentalchargecode_customizemodel.png)](./media/fmrentalchargecode_customizemodel.png) 

このクラスには、**FMRentalCharge** テーブルの**更新**および**挿入**イベントに登録するイベント ハンドラーの実装が含まれています。 Microsoft Dynamics AX は、テーブルおよびその他の型で発生するデータ イベントを導入しています。 基本 X++ コードをオーバーレイせずにビジネス ロジックを拡張するアプリケーションを有効にする、テーブルのデータ イベントを申し込むことができます。 このチュートリアルの後半で、簡単にテーブル イベントをサブスクライブする方法について説明します。 **注記:** このクラスが拡張クラス (\_拡張子の接尾辞によって示される) であることを確認します。 任意のクラスでイベント ハンドラーを作成することができます。このクラスは拡張クラスである必要はありません。 拡張子クラスは、拡張メソッドを作成するために必要です。 拡張メソッドの詳細については、[X++ デバッガーの機能](../dev-tools/new-x-debugger-features.md) 記事の「拡張メソッド」セクションを参照してください。

### <a name="view-the-plug-in-classes"></a>プラグイン クラスの表示

前のセクションに示された **FMRentalCharge\_Extension** クラスのイベント ハンドラー コードでは、両方のイベント ハンドラーが **FMTotalsEngineBase::GetInstance** を呼び出してフリート管理計算エンジンの現在のインスタンスを取得することに注意します。 計算エンジンは、プラグイン クラスを使用して実装されます。 クラス ファクトリは、コンフィギュレーションまたはビジネス データに基づくプラグイン クラスの適切なインスタンスを作成します。

1.  FMRentalCharge\_Extension.xpp を表示するコード エディター ウィンドウで、**GetInstance** を右クリックしてから**定義に移動**をクリックします。 これにより、抽象クラス **FMTotalsEngineBase** のコードが開きます。 この抽象クラスは**プラグインポイント**と呼ばれ、次の属性に関連付けられています: \[Microsoft.Dynamics.AX.Platform.Extensibility.ExportInterfaceAttribute()\] 

    [![定義に移動](./media/godefinition_customizemodel.png)](./media/godefinition_customizemodel.png) 

    プラグイン クラスは、抽象クラスやインターフェイスの拡張機能または実装を表します。 プラグイン クラスは、そのメタデータとプラグイン ポイントを定義する属性に関連付けられます。 この例では、**FMTotalsEngineBase** プラグイン ポイントに関連付けられている 2 つのプラグイン クラスがあります。 基本計算エンジンは、プラグイン クラス **FMTotalsEngine** によって定義されます。 プロジェクト **移行されたフリート管理 &gt; コード &gt; クラス** で見つけることができます。 

    [![FMTotalsEngineBase](./media/code1_customizemodel.png)](./media/code1_customizemodel.png) 

    割引計算エンジンは、プラグイン クラス **FEDiscountEngine** によって定義されます。 プロジェクト **フリート管理割引 &gt; コード &gt; クラス** で見つけることができます。 

    [![FEDiscountEngine](./media/code2_customizemodel.png)](./media/code2_customizemodel.png)

2.  **GetInstance** メソッドを確認します。 プラグイン ファクトリ **SysPluginFactory::Instance** を使用して、現在のプラグイン メタデータに基づいて現在の計算エンジンのインスタンスを作成します。 プラグイン メタデータは、グローバル構成テーブルの **FMParameters** で指定されます。 

    [![FMParameters](./media/code3_customizemodel.png)](./media/code3_customizemodel.png) 

    Dynamics AX は、コンフィギュレーション可能なプラグイン クラスをサポートし、プラグイン メタデータは開発時に知られず、管理者がランタイム時にコンフィギュレーション可能なクラスに関連付けられます。 これは、このチュートリアルの対象ではありません。

## <a name="create-additional-fleet-management-extensions"></a>追加のフリート管理拡張子を作成する
このセクションでは、Visual Studio tools を使用して拡張機能を作成して操作する方法を示します。

### <a name="extend-the-fmvehicle-table"></a>FMVehicle テーブルを拡張

1.  **ソリューション エクスプローラー**で、**FleetManagement 割引**プロジェクトを選択します。
2.  Visual studio の**アプリケーション エクスプローラー**で、**表示 &gt; アプリケーション エクスプローラー**をクリックして、FMVehicle という名前のテーブルを検索します。 フィルター バーに "FMVehicle type:Table" と入力し、**Enter** を押します。 

    [![FMVehicle の AppExplore 検索](./media/appexplorersmall_customizemodel.png)](./media/appexplorersmall_customizemodel.png)

3.  **FMVehicle** を右クリックし、**拡張子の作成** をクリックします。 

    [![AppExplorer 拡張機能の作成](./media/appexplorerlarge1_customizemodel.png)](./media/appexplorerlarge1_customizemodel.png)

    これにより、**FMVehicle.Extension** という名前の **FleetManagement Discounts** プロジェクトに **FMVehicle** テーブルの拡張が作成されます。 

    [![FMVehicle.Extension](./media/expanddiscountsnode2_customizemodel.png)](./media/expanddiscountsnode2_customizemodel.png)

4.  **ソリューション エクスプローラー**で、**FMVehicle.Extension** を右クリックしてから**プログラムから開く**をクリックします。 ダイアログ ボックスで **XML (テキスト) エディター**を選択してから **OK** をクリックします。 **注記**: この拡張子ファイルは、データベースの **FMVehicle** テーブルのメタデータを含まない簡単なテンプレートです。 拡張ファイルには拡張を定義するメタデータのみが常に含まれ、基本モデル要素からは何もありません。 

    [![FMVehicle](./media/code4_customizemodel.png)](./media/code4_customizemodel.png)

5.  XML エディターを閉じます。
6.  **ソリューション エクスプローラー**で、**FMVehicle.Extension** をダブルクリックしてデザイナーを開きます。
7.  **フィールド** を右クリックし、新しい整数型フィールドを追加します。 フィールドの名前を **NumberOfCylinders** に変更します。
8.  **プロパティ** ウィンドウで、新しいフィールドの**ラベル** プロパティを **NumberofCylinders** に設定します。
9.  **NumberOfCylinders** フィールドを **AutoReport** フィールド グループにドラッグ アンド ドロップし、ベース テーブルのフィールド グループに展開します。 

    [![NumberOfCylinders\_CustomizeModel](./media/numberofcylinders_customizemodel.png)](./media/numberofcylinders_customizemodel.png)

10. FMVehicle.Extension を保存します。
11. **イベント**ノードを展開します。 **イベント** ノードには、テーブルが公開するすべてのイベントが一覧表示されます。 これには、フレームワークによって定義されたイベントと、アプリケーション開発者によって定義されたデリゲート メソッドが含まれます。 

    [![イベント ノード](./media/eventsnode_customizemodel.png)](./media/eventsnode_customizemodel.png)

    **注記**: テーブルのイベント、フォームイベント、フォーム データ ソース イベント、フォーム コントロール イベントなど、異なるフレームワーク イベントが、さまざまなタイプの要素とサブ要素のデザイナーに公開されています。
12. onValidatedWrite を右クリックし、**イベント ハンドラー メソッドをコピー** を選択します。 

    [![onValidateWrite](./media/onvalidatewrite_customizemodel.png)](./media/onvalidatewrite_customizemodel.png) 

    このステップは、イベント ハンドラー メソッドのシグネチャをクリップボードにコピーします。
13. **FMVehicleEventHandlers** という名前の新しいクラスを **FleetManagement Discounts** プロジェクトに追加します。
14. **ソリューション エクスプローラー**で、**FEVehicleEventHandlers** をダブルクリックしてコード エディターを開きます。
15. 右クリックし、手順 12 にコピーしたイベント ハンドラー メソッドを貼り付けます。

        Class FMVehicleEventHandlers
        {
            /// <summary>
            ///
            /// </summary>
            /// <param name="sender"></param>
            /// <param name="e"></param>
            [DataEventHandler(tableStr(FMVehicle), DataEventType::ValidatedWrite)]
            public static void FMVehicle_onValidatedWrite(Common sender, DataEventArgs e)
            {
            }
        }



16. 次のコードを **FMVehicle\_onValidatedWrite** イベント ハンドラーに挿入します。 このコードは、シリンダの数が 8 を超えることができないことを検証します。

           [DataEventHandler(tableStr(FMVehicle), DataEventType::ValidatedWrite)]
            public static void FMVehicle_onValidatedWrite(Common sender, DataEventArgs e)
            {
                ValidateEventArgs validateArgs = e as ValidateEventArgs;
                FMVehicle vehicle = sender as FMVehicle;
                boolean result = validateArgs.parmValidateResult();

                if (vehicle.NumberOfCylinders > 8)
                {
                    result = checkFailed("Invalid number of cylinders.");
                    validateArgs.parmValidateResult(result);
                }
            }

17. FMVehicleEventHandlers クラスを保存 **ヒント**: モデルの任意のクラスで、イベント ハンドラーを貼り付けて定義できます。 クラス FMVehicleEventHandlers は、例としてのみ使用されます。

### <a name="extend-the-fmvehicle-form"></a>FMVehicle フォームを拡張

次に、**FleetManagement 割引**プロジェクトの **FMVehicle** フォーム拡張機能を追加します。 最初に、**ソリューション エクスプローラー**でこのプロジェクトを選択することを確認します。

1.  **アプリケーション エクスプローラー**を使用して **FMVehicle** という名前のフォームを検索するには、**アプリケーション エクスプローラー**のフィルタ バーに [*FMVehicle タイプ:フォーム*] を入力します。
2.  フォームを右クリックし、**拡張子の作成** をクリックします。
3.  下に示すように、**NumberOfCylinders** という名前の新しい整数コントロールを **Attributes2** グループ コントロールに追加します。 このコントロールは、**デザイン&gt; タブ &gt; TabPageDetails &gt; TabHeader &gt; DetailsDetails &gt; Attributes2** を展開すると見つけることができます。 

    [![シリンダの数](./media/numcylinteger_customizemodel.png)](./media/numcylinteger_customizemodel.png)

4.  次のように新しいコントロールをプロパティ ウィンドウの **NumberOfCylinders** データ フィールドにバインドします。 

    [![バインド コントロール](./media/datafield_customizemodel.png)](./media/datafield_customizemodel.png)

5.  FMVehicle.Extension を保存し、プロジェクトを作成します。

### <a name="test-your-extensions"></a>拡張機能をテスト

1.  **ソリューション エクスプローラー**で、**FleetManagement 割引**を右クリックしてから、**スタートアップ プロジェクトとして設定**をクリックします。
2.  同様に、FleetManagement 割引で、スタートアップ オブジェクトとして **FMVehicle.Extension** フォームを設定します。
3.  **Ctrl+F5** キーを押してデバッグなしで開始するか、**デバッグ** メニューを使用します。
4.  **車両**フォームが開いた後、車両を選択して詳細を表示します。
5.  **詳細**タブを展開し、新しい**シリンダ番号**フィールドを通知します。 

    [![シリンダー数の詳細](./media/nbofcyls.jpg)](./media/nbofcyls.jpg)

6.  アクション ウィンドウで、**編集**をクリックして**シリンダの数**フィールドの値を 12 に変更します。
7.  アクション ウィンドウで、**保存**をクリックします。
8.  検証エラーを確認します。
9.  有効なシリンダ数を 9 より小さく入力し、次に新しい値を保存します。

## <a name="experiment-with-event-handlers-on-form-controls"></a>フォーム コントロールでのイベント ハンドラーを試す
これは、既存のコントロールにイベント ハンドラー メソッドを追加する例です。

1.  **FMRental** フォーム デザイナーで **AddLine** コマンド ボタン コントロールを検索し、**OnClicked** イベントを右クリックし、次に選択**イベント ハンドラーのメソッドをコピー**を選択します。

    [![明細行 OnClicked イベントを追加します。](./media/addlineonclickedevent.jpg)](./media/addlineonclickedevent.jpg)

2.  フリート管理拡張モデルのクラスでイベント ハンドラー メソッドを貼り付け、X++ コードを追加して実装します。

<!-- -->

    /// <summary>
    ///
    /// </summary>
    /// <param name="sender"></param>
    /// <param name="e"></param>
    [FormControlEventHandler(formControlStr(FMRental, AddLine), FormControlEventType::Clicked)]
    public static void AddLine_OnClicked(FormControl sender, FormControlEventArgs e)
    {
    }

-   AddLine\_OnClicked イベント ハンドラーを実装すると、**sender** パラメーターを使用して、ボタン コントロール インスタンスにアクセスできます。

<!-- -->

    FormButtonControl button = sender as FormButtonControl;

-   親フォームや、変数のいずれかにアクセスする場合は、この例では、**FormRun** インスタンスとデータ ソースのいずれかにアクセスする方法が示されています。

<!-- -->

    FormRun fr;
    fr = sender.formRun();
    var frDs = fr.dataSource("FMRental");

## <a name="experiment-with-event-handlers-on-form-data-sources"></a>フォーム データ ソースでのイベント ハンドラーを試す
テーブル、フォーム コントロールおよびその他の要素タイプと同じように、フォーム データ ソースとフォーム データ ソース フィールドはフレームワーク レベルのイベントを提供します。 次の例は、フォーム データ ソースの ValidatingWrite イベントまたはフォーム データ ソースの検証イベントを使用して FMRental フォームのユーザー入力を検証する方法を示しています。 この機能は、Platform Update 7 以降で利用できます。

```
    /// <summary>
    /// When saving a new rental, prevent setting the start mileage on the FMRental form to a value that is equal to 1
    /// </summary>
    [FormDataSourceEventHandler(formDataSourceStr(FMRental, FMRental), FormDataSourceEventType::ValidatingWrite)]
    public static void FMRental_OnValidatingWrite(FormDataSource sender, FormDataSourceEventArgs e)
    {
        var datasource = sender as FormDataSource;
        var args = e as FormDataSourceCancelEventArgs;
        if (args != null && datasource != null)
        {
            FMRental record = datasource.cursor() as FMRental;
            if (record.recId == 0)
            {
                if(record.startmileage == 1)
                {
                    boolean doCancel = !checkFailed("Start Mileage = 1 is not allowed");
                    args.cancel(doCancel);
                }
            }
        }
    }
```
```
    /// <summary>
    /// Prevent changing the start mileage field on the FMRental form to a value that is equal to 1
    /// </summary>
    [FormDataFieldEventHandler(formDataFieldStr(FMRental, FMRental, StartMileage), FormDataFieldEventType::Validating)]
    public static void StartMileage_OnValidating(FormDataObject sender, FormDataFieldEventArgs e)
    {
        var dataObject = sender as FormDataObject;
        var args = e as FormDataFieldCancelEventArgs;
        if (args != null && dataObject != null)
        {
            var datasource = dataObject.datasource() as FormDataSource;
            if (datasource != null)
            {
                FMRental record = datasource.cursor() as FMRental;
                if (record.RecId > 0)
                {
                    if (record.StartMileage == 1 )
                    {
                        boolean doCancel = !checkFailed("Start Mileage = 1 is not allowed");
                        args.cancel(doCancel);
                    }
                }
            }
        }
    }
```
## <a name="experiment-with-table-extension-display-and-edit-methods"></a>テーブル 拡張子ディスプレイを試し、メソッドを編集
拡張メソッドを使用すると、新しい表示を作成してテーブルを拡張し、オーバーレイ X++ コード無しでテーブルのメソッドを編集します (拡張メソッドは、\_ 拡張子の接尾語という名のクラスに属する必要があります)。 たとえば、このクラスは、CupHoldersDisplay と呼ばれる拡張表示メソッドを使用して、FMVehicle テーブルを拡張する方法を表示します。

    public static class FMVehicle_Extension
    {
       public static display int CupHoldersDisplay(FMVehicle vehicle)
       {
         return 7;
       }
    }

フォームまたはフォームの拡張機能では、以下の画像に示すように、「データ ソース = FMVehicle」および「データ メソッド ="FMVehicle \_Extension::CupHoldersDisplay」を設定することによってこの表示メソッドにコントロールをバインドできます。

![拡張表示メソッド](./media/extensiondisplaymethod.jpg)

## <a name="create-a-fleet-extension-package-for-deployment"></a>展開のためのフリート拡張パッケージを作成する
拡張機能をテスト環境、運用前環境、運用環境などの別の環境に展開するには、展開パッケージを作成する必要があります。

1.  Visual Studio の **Dynamics AX** メニューで、**配置**をポイントしてから、**配置パッケージの作成**をクリックします。 

    ![配置パッケージの作成](./media/createdeploymentpackage_customizemodel.png)

2.  **フリート管理拡張** チェック ボックスをオンにします。
3.  **パッケージ ファイルの場所**テキスト ボックスに、「c:\FMLab」と入力します。
4.  **作成** をクリックします。 これにより、フリート管理拡張パッケージを含む展開パッケージが作成されます。


<a name="additional-resources"></a>その他のリソース
--------

[FMLab サンプル コードをダウンロードする](https://github.com/Microsoft/FMLab)




