---
title: 新しい ER ソリューションを設計して ZPL ラベルを印刷する
description: この記事では、新しい電子レポート (ER) を設計して Zebra プログラミング言語 (ZPL) ラベルを印刷する方法について説明します。
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: f861fe63c6d7d00d0a9f84d33c0d1b1b23735b61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845718"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>新しい ER ソリューションを設計して ZPL ラベルを印刷する

[!include [banner](../includes/banner.md)]


この記事では、システム管理者、電子レポートの開発者、電子レポート業務コンサルタントの役割にあるユーザーが、[電子レポート (ER)](general-electronic-reporting.md) のフレーム ワークを構成し、求められる新しい ER ソリューションの ER [構成](general-electronic-reporting.md#Configuration)を設計して、倉庫管理システムのデータにアクセスし、Zebra プログラミング言語 (ZPL) II 形式でカスタムレポートを生成する方法について説明します。 これらの設定を **USRT** 社を使用して説明します。

## <a name="business-scenario"></a>ビジネス シナリオ

Microsoft Dynamics 365 Finance で倉庫管理を実装した会社を表します。 すべての倉庫の場所には、バー コードを含むセルフ ラベルを付する必要があります。 倉庫作業員は、同僚のバーコード リーダーを使用してバーコードをスキャンします。

すべての倉庫の場所には、移動前活動の範囲でラベルが付けされています。 ただし、既存のラベルが破損したり、倉庫の棚付けが展開された場合に、需要時に倉庫の場所のラベルを印刷することもできます。 最近リリースされたER機能を使用すると、倉庫の監修者がラベルを直接ラベルプリンターに印刷できる新しい ER ソリューションを構成できます。

## <a name="configure-the-er-framework"></a> ER フレームワークを構成する

[ER フレームワークの構成](er-quick-start2-customize-report.md#ConfigureFramework)に記載の手順に従って、 ER パラメーターの最小限のセットを構成します。 新しい ER ソリューションを使用して ER モデル マッピングを設計する前に、この設定を完了する必要があります。

## <a name="design-a-domain-specific-data-model"></a>ドメイン固有のデータ モデルを設計する

倉庫管理ドメインの [データ モデル](er-overview-components.md#data-model-component) コンポーネントを含む、新たな ER 構成を作成します。 このデータ モデルは後で、ER フォーマットを設計して倉庫一ラベルを生成する際に、データ ソースとして使用されます。

### <a name="import-a-data-model-configuration"></a>データ モデル構成のインポート

次の手順に従って、Microsoft が提供する XML ファイルから必要なデータ モデルをインポートします。 次のセクションの説明に従って独自のデータ モデルを作成する方法も指定できます。

1. [倉庫モデル.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. アクション ウィンドウの **構成** ページで、**交換** \> **XML ファイルを読込む** を選択します。
5. **参照する** を選択し、**倉庫モデル.version.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

![構成ページのインポートされた ER データ モデル構成。](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>データ モデル構成の作成

Microsoft が提供するデータ モデル ファイルをインポートする代わりに、データ モデルを最初から作成することができます。 このタスクの完了方法を示す例については、[新しいデータ モデル構成の作成](er-quick-start1-new-solution.md#DesignDataModel) を参照してください。

### <a name="review-the-data-model"></a>インポートされたデータ モデルをレビューする

構成済データ モデルの編集可能なバージョンは、**データ モデル デザイナー** ページで確認できます。

![データ モデル デザイナー ページ上の ER データ モデルの構造。](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>構成済みのデータモデルで使用するモデル マッピングをデザインする

電子レポート開発者のロールにあるユーザーは、 倉庫データ モデルの [モデル マッピング](er-overview-components.md#model-mapping-component) コンポーネントを含む、新たな ER 構成を作成する必要があります。 このコンポーネントは、Dynamics 365 Finance に特化して構成されたデータモデルを実装しています。 構成済みのデータモデルの実行時にアプリケーション データの入力に使用する必要があるアプリケーション オブジェクトを指定するには、モデルマッピング コンポーネントを構成する必要があります。 このタスクを完了するには、財務における倉庫管理事業ドメインのデータ構造の実装方法について理解しておく必要があります。

### <a name="import-a-model-mapping-configuration"></a>新しいモデル マッピング構成をインポートする

次の手順に従って、Microsoft が提供する XML ファイルから必要なデータ モデル マッピングをインポートします。 次のセクションの説明に従って独自のデータ モデル マッピングを作成する方法も指定できます。

1. [倉庫モデル mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. アクション ウィンドウの **構成** ページで、**交換** \> **XML ファイルを読込む** を選択します。
5. **参照する** を選択し、**倉庫モデル mapping.version.1.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

![構成ページのインポートされた ER データ モデル構成。](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>モデル マッピング構成を作成する

Microsoft が提供するデータ モデル マッピング ファイルをインポートする代わりに、データ モデル マッピングを最初から作成することができます。 このタスクの完了方法を示す例については、[新しいデータ モデル マッピング構成の作成](er-quick-start1-new-solution.md#CreateModelMapping) を参照してください。

### <a name="review-the-model-mapping"></a>モデル マッピングを確認する

構成済データ モデル マッピングの編集可能なバージョンは、**モデル マッピング デザイナー** ページで確認できます。

![モデル マッピング デザイナー ページ上の ER モデル マッピングの構造。](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>形式のデザイン

電子レポート機能コンサルタントのロールが付与されているユーザーは、[フォーマット](er-overview-components.md#format-component) コンポーネントを含む新しい ER 構成を作成する必要があります。 このコンポーネントを構成するには、ZPL II コードを使用して倉庫の場所ラベルのレイアウトを指定します。

### <a name="import-a-format-configuration"></a>形式構成のインポート

次の手順に従って、Microsoft が提供する XML ファイルから必要な形式をインポートします。 次のセクションの説明に従って独自の形式を作成する方法も指定できます。

1. [倉庫場所 labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml) ファイルをダウンロードし、ご利用のコンピューターに保存してください。
2. **組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。
3. **電子レポート** ワークスペースで、**レポートの構成** を選択します。
4. アクション ウィンドウの **構成** ページで、**交換** \> **XML ファイルを読込む** を選択します。
5. **参照する** を選択し、**倉庫場所 labels.version.1.1.xml** ファイルを検索して、選択します。
6. **OK** を選択し、構成をインポートします。

![構成ページのインポートされた ER 形式構成。](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>形式コンフィギュレーションを作成する

Microsoft が提供する形式ファイルをインポートする代わりに、形式を最初から作成することができます。 このタスクの完了方法を示す例については、[新しい形式構成の作成](er-quick-start1-new-solution.md#FormatCreate) を参照してください。

### <a name="review-the-format"></a>形式を確認する

構成済形式の編集可能なバージョンは、**形式デザイナー** ページで確認できます。

![形式デザイナー ページで ER 形式の構造。](./media/er-design-zpl-labels-format.png)

この形式の `model.Location.Label` データ ソースは、次の情報を含むラベルを生成するように構成されます。

- テキストとしての倉庫のタイトル
- バー コードとしての倉庫のタイトル
- 場所タイトル
- チェック ディジット

データ ソース の **フォーミュラ デザイナー** ページで、ラベルの生成に使用されるER 式には、目的のレイアウトの情報を結合する `CONCATENATE` 機能が含まれます。

![フォーミュラ デザイナー ページでモデル データ ソースの式。](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> ラベル レイアウトは、場所のタイトルとチェック ディジットがラベルの中央に位置合わせするように設計されています。 ただし、ZPL II はバーコードのセンター配置をサポートしています。 したがって、`model.Location.Warehouse.Alignment` データ ソースのフォーミュラを使用して、ラベルの中央でバー コードを位置合わせします。 このフォーミュラは、倉庫タイトルの文字数に基づいて、バー コードのオフセットを計算します。

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>生成されたラベルをプレビュー表示する環境の準備

次の例では、ZPL ラベル用にプリンタを使用して生成されたラベルを画面にプレビュー表示します。 これらの手順に従って、このオプションを有効にします。

1. **倉庫の場所ラベル** ER 形式の [プリンター](er-destination-type-print.md) ER の出力先を追加し、それを構成して財務から [ドキュメント ルート指定エージェント (DRA)](install-document-routing-agent.md) に生成されたラベルを送信します。
2. 生成されたラベルを現在のワークステーションからアクセスできるローカル プリンタに財務からルーティングする DRA をインストールおよび構成します。
3. 現在のワークステーション用のローカル プリンタを追加し、DRA からプリンタ アプリケーションに生成されたラベルを渡す方法で構成します。
4. Chrome Web ブラウザの拡張機能としてプリンタの接続アプリケーションをインストールし、ローカル プリンタから生成されたラベルを Web サービスに渡して、生成されたラベルを表示してプレビュー用にプリンター画面に戻す構成を行います。

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER レポート</p>
<p>プリンター出力先</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>ドキュメント ルート指定エージェント</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>ローカル プリンター</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>プリンター エミュレーター</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>レンダリング Web サービス</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>プリンター接続アプリケーションのインストールおよび構成

ZPL レンダリング エンジン用のプリンター エミュレーターのアプリケーションを Chrome Web ブラウザに追加します。 この例では、[Labelary ZPL web サービス](http://labelary.com/service.html) に基づいた [ZPL プリンター](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) エミュレーターを使用します。 このプリンター エミュレーター アプリケーションは、生成されたラベルを ZPL 形式でローカル プリンターから Web サービスに渡し、プレビュー用に PDF または PNG ファイルとしてラベルを返します。

1. Chrome Web ストアで、使用するプリンター アプリケーションを探して選択します。 その後、**Chromeに追加** を 選択して、Chrome Web ブラウザに追加します。

    ![Chrome Web ストアから Chrome Web ブラウザにプリンターを接続するアプリケーションを追加する。](./media/er-design-zpl-labels-add-app.png)

2. Chrome Web ブラウザーからプリンター エミュレーター アプリケーションを実行するには、**アプリケーションを起動** を選択します。

    ![Chrome Web ブラウザーからプリンター エミュレーター アプリケーションを実行します。](./media/er-design-zpl-labels-run-app.png)

3. アプリケーションの実行を構成する

    1. アプリケーションをオフにします。
    2. プリンター設定で、ホストを **127.0.0.1** に設定します。
    3. ポートを **9100** に設定します。

        ![プリンターを接続するアプリケーションを構成します。](./media/er-design-zpl-labels-configure-app.png)

    4. アプリケーションを再度オンにします。 指定したホストおよびポートでプリンタが開始されたというメッセージが表示されます。

        ![プリンター エミュレーター アプリケーションがオンに戻りました。](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> この例で使用するプリンターの接続アプリケーションは、ラベルを表示する Web サービスに依存します。セキュリティ設定でサービスと通信を行えるようになっていることを確認してください。 そうでない場合は、表示されたラベルがアプリケーションに送信され、プレビューも表示されません。

### <a name="add-and-configure-a-local-printer"></a>ローカル プリンターの追加および構成

現在のデバイスが使用して DRA からプリンター エミュレーター アプリケーションに生成されたラベルを渡す　[新しいローカル プリンターを追加します](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b)。

1. Windows で、**開始** \> **設定** \> **デバイス** \> **プリンター \& スキャナー** を選択します。
2. **プリンター \& スキャナー 設定** を選択します。
3. **プリンターまたはスキャナーを追加** の場合、**デバイスの追加** を選択します。
4. **希望のプリンターが表示されていなかった** 場合は、**手動で追加** を選択します。
5. **その他のオプションを使用してプリンターを検索** フィールドで、**手動設定を使用してローカル プリンターまたはネットワーク プリンターを追加する** を選択します。
6. **プリンター ポートの選択** フィールドで、**新しいポートの作成** を選択し、次の手順に従います。

    1. **ポートのタイプ** フィールドで、**標準 TCP/IP ポート** を選択します。
    2. **ホスト名か IP アドレス** フィールドに、**127.0.0.1** と入力します。
    3. **ポート名** フィールドに、**ZPL** と入力します。
    4. **TCP/IP ポートの検出** 操作が完了するまで待ちます。
    5. **デバイスタイプ** フィールドで **カスタム** を選択し、**設定** を選択します。
    6. 次のポート設定が指定されている必要があります。

        - **ポート名:** ZPL
        - **プリンタ名または IP アドレス:** 127.0.0.1
        - **プロトコル:** 生
        - **ポート番号:** 9100

7. **プリンタ ドライバのインストール** フィールドで、**一般 / テキストのみ** を選択します。
8. **プリンター名** フィールドに **ZebraPrinter** と入力します。

![現在のデバイスにローカル プリンターを追加する。](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>DRA の構成とインストール

生成されたラベルを財務から構成済のローカル プリンターに渡す DRA を準備します。

1. [DRA のインストール](install-document-routing-agent.md#install-the-document-routing-agent)。
2. [DRA の構成](install-document-routing-agent.md#configure-the-document-routing-agent).
3. DRA で [ローカル プリンターを登録します](install-document-routing-agent.md#register-network-printers)。
4. 財務環境で [ローカル プリンターを有効にします](install-document-routing-agent.md#administer-network-printers)。

![生成されたラベルを印刷するための DRA の準備をします。](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>ER 送信先のコンフィギュレーション

生成されたラベルを財務から DRA を準備します。

1. **組織管理** \> **電子レポート** \> **電子レポートの送信先** に移動します。
2. **電子報告の送信先** ページで、アクション ウィンドウで、**新規** を選択します。
3. **参照** フィールドで、**倉庫の場所ラベル** を選択します。
4. **ファイルの送信先** クイックタブで **新規** を選択します。
5. **名前** フィールドに、**ラベル** と入力します。
6. **ファイル コンポーネント名** フィールドで、**レポート** を選択します。
7. **設定** を選択します。
8. **デスティネーション設定** ダイアログ ボックスの **プリンター** タブで、**有効化済み** オプションを **はい** に設定します。
9. **プリンター名** フィールドで **ZebraPrinter** を選択します。
10. **ドキュメント ルーティング タイプ** フィールドで、**ZPL** を選択します。
11.  **OK** を選択します。

![電子レポートのデスティネーション ページで、倉庫場所ラベル形式の ER デスティネーションを構成します。](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>倉庫の場所のレビュー

1. **倉庫管理** \> **設定** \> **倉庫** \> **場所** に移動します。
2. **場所** ページで、**チェック ディジット** フィールドに値が設定されている場所だけを 表示するフィルターが適用されます。

![場所ページで倉庫の場所を確認します。](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>倉庫の場所ラベルの印刷

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **構成** ページの構成ツリーで、**倉庫モデル** を展開し、**倉庫場所ラベル** を選択します。
3. アクション ウィンドウで、**実行** を選択します。
4. **電気レポート パラメータ** ダイアログ ボックスの **含めるレコード** タブで、**フィルター** を選択します。
5. **範囲** タブで、**テーブル** フィールドが **場所** に設定されていて、**フィールド** フィールドが **場所** に設定されている行を検索します。 **基準** フィールドに、**LPEnabled** を入力します。
6.  **OK** を選択します。
7.  **OK** を選択します。 ラベルが生成され、プリンター エミュレーター アプリケーションのプレビュー ページに表示されます。

![Zpl プリンター アプリケーションのプレビュー ページで生成されたラベルをレビューします。](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>ラベルのレイアウトを変更する

倉庫の場所ラベルの現在のレイアウトを変更できます。 次の例では、生成されたラベルに場所プロファイル ID が含まれるレイアウトを変更する方法を示します。

1. **組織管理** \> **電子申告** \> **構成** の順に移動します。
2. **ドラフト状態でデスティネーションを使用する** [ER ユーザー パラメータ](electronic-reporting-destinations.md#applicability) を **はい** に設定します。
3. **構成** ページの構成ツリーで、**倉庫モデル** を展開し、**倉庫場所ラベル** を選択します。
4. **デザイナー** をクリックします。
5. **形式デザイナー** ページの **マッピング** タブで、`model.Location.Label` データソースを選択します。
6. **データ ソース プロパティ** ダイアログ ボックスで、**編集** \> **フォーミュラの編集** を選択します。
7. **フォーミュラ デザイナー** ページの **フォーミュラ** フィールドで、ラベルを生成するために使用される ER 式を確認します。

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. フォーミュラを更新して、生成されたラベルに場所プロファイル ID を追加します。

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. **保存** を選択します。
10.  **OK** を選択します。
11. アクション ウィンドウで、**実行** を選択します。
12. **電気レポート パラメータ** ダイアログ ボックスの **含めるレコード** タブで、**フィルター** を選択します。
13. **範囲** タブで、**テーブル** フィールドが **場所** に設定されていて、**フィールド** フィールドが **場所** に設定されている行を検索します。 **基準** フィールドに、**Bay** と入力します。
14.  **OK** を選択します。
15.  **OK** を選択します。 ラベルが生成され、プリンター エミュレーター アプリケーションのプレビュー ページに表示されます。

![Zpl プリンターのエミュレーター アプリケーションのプレビュー ページで、場所プロファイル ID を含む生成されたラベルを確認する。](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>暗号化

> [!NOTE]
> 編集可能な ER 形式の **共通\\ファイル**  コンポーネントのエンコード設定と、デザインされたラベルの適切な設定を同期する必要があります。 **共通\\ファイル** コンポーネントの **[エンコーディング](er-suppress-bom-characters.md)** フィールドの値は、ラベルのエンコードを制御するために使用される ZPL コマンド (`^CI` コマンドなど) と相反しない必要があります。 ER は、これらの設定が同期化される検証を行わないとします。

## <a name="additional-resources"></a>追加リソース

[プリンター出力先](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
