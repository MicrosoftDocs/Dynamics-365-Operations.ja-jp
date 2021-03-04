---
title: タイル、リスト、およびデータ キャッシュを使用してワークスペースを変更する
description: このチュートリアルでは、ワークスペースの概要に新しいタイルを作成し、新しいリストを構築して、リストのデータ キャッシュを作成します。
author: jasongre
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 10794
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 883746ee194b452a3aca45cddd54cf85c5301b77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092352"
---
# <a name="modify-a-workspace-with-a-tile-list-and-data-cache"></a>タイル、リスト、およびデータ キャッシュを使用してワークスペースを変更する

[!include [banner](../includes/banner.md)]

このチュートリアルでは、新しいタイルを作成し、ワークスペースの概要にそれを含め、ワークスペースの新しいリストを構築して、ワークスペースにリストのデータ キャッシュを作成します。

## <a name="prerequisites"></a>必要条件

このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。 詳細については、トピック [開発環境の配置とアクセス](../dev-tools/access-instances.md) を参照してください。

## <a name="key-concepts"></a>重要な概念

- ワークスペースに関連付けられているフォーム パターンについて学んで使用します。
- 新しいタイルを作成し、それをワークスペースの **集計** セクションに含めます。
- ワークスペースの新しいリストをビルドします。
- リストのデータ キャッシュをワークスペースに作成します。

## <a name="setup"></a>段取り

### <a name="import-the-tutorial-project-and-transactional-data"></a>チュートリアル プロジェクトおよびトランザクション データのインポート

Microsoft Visual Studio を使用してチュートリアル プロジェクトをインポートします。 チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。 Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。 フリート管理チュートリアルのデータを読み込むために、**FMTDataHelper** クラスを使用します。 これが作業する最初のチュートリアルである場合は、[開発環境の配置とアクセス](../dev-tools/access-instances.md) をレビューして、ローカル仮想マシン (VM)で作業している場合に、管理者ユーザーをプロビジョニングすることを確認します。

1. Microsoft Dynamics Lifecycle Services (LCS) の手法から **FMTutorialDataModel.axpp** ファイルをダウンロードして、VM の **Downloads** フォルダーにコピーします。
2. デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。
3. **Dynamics 365** メニューで、**プロジェクトのインポート** をクリックします。
4. **プロジェクトのインポート** ダイアログ ボックスで、**ファイル名** フィールドの隣にある、省略記号 (**...**) ボタンをクリックします。
5. **インポートするファイルの選択** ダイアログ ボックスで、**ダウンロード** フォルダーを参照して **FMTutorialDataModel.axpp** をクリックしてから **開く** をクリックします。
6. **要素の上書き** チェック ボックスをオンにし、**現在のソリューション** オプションをオンにします。 次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。

    ![完了したプロジェクトのインポート ダイアログ ボックス](media/importproject1.png)

7. **OK** をクリックします。
8. ソリューション エクスプローラーで **クラス** を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
9. **ビルド** メニューで、**ソリューションの再構築** をクリックします。 タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。 **出力** ウィンドウでビルドの進行状況を表示できます。
10. ビルドが完了した後、**Ctrl + F5** を押してプロジェクトを実行します。 ブラウザーが開き、データをインポートするクラスが実行されます。

### <a name="open-the-fmtutorial-project"></a>FMTutorial プロジェクトを開く

Visual Studio を使用して FMTutorial プロジェクトを開きます。 Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。

1. デスクトップ環境がまだ開かれていない場合は、Visual Studio ショートカットをデスクトップ上でダブルクリックして、開発環境を開きます。
2. **ファイル** メニューで、**開く** \> **プロジェクト/ソリューション** をクリックします。
3. **プロジェクトを開く** ダイアログ ボックスで、**ドキュメント** \> **Visual Studio 15.0** \> **プロジェクト** の順に参照して、**FMTutorial** ソリューションを選択してから、**開く** をクリックします。
4. FMTutorial プロジェクトがソリューション エクスプローラーに表示されます。

## <a name="exercise-1-understand-the-operational-workspace-pattern"></a>手順 1: 運用ワークスペースのパターンを理解

**FmtClerkWorkspace** フォームを調整する前に、フォームの現在の状態を確認して既に存在するコンテンツと、その内容が運用ワークスペース パターンにどのように適合するかを理解してください。

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。
2. **デザイン** ノードをクリックします。
3. **パターン** タブをクリックします。運用ワークスペースにはオプションのアクション ウィンドウとオプションのフィルター グループがあります (これらのノードの左に 0..1 の表記で示されています)。 ただし、このパターンによってパノラマ スタイル タブが必要になります。 **パターン** タブでは、PanoramaBody コントロールがパターンで必要なタブと一致していることを示しますが、このパターンのレベルでオプションの項目に対応するコントロールはありません。

    ![稼働中のワークスペース パターン](./media/workspacepattern1.png)

4. **PanoramaBody** をクリックします。

    ![パターン タブ、PanoramaBody](./media/workspacepattern2.png)

All すべてのワークスペースに必要な 3 つのセクションがあります。

- **集計セクション** – このセクションは、カードまたはグラフに対応するタイルまたはフォーム パーツを含むことを意図しています。
- **タブ付きリスト** – このセクションでは、ユーザーの作業に関連するデータの 1 つまたは複数のリストで構成されています。 一度に 1 つだけ一覧が表示され、各一覧はローカル フィルターとアクションを含めることもできます。 個別のリストは、フォーム パーツ コントロール内でモデル化されます。
- **関連リンク** – このセクションは、この活動またはペルソナの、重要なリンクまたは一般的に使用されるリンクで構成されています。

運用ワークスペースは、最大 2 つのグラフ (セクション グラフのタブ ページ) を含むパノラマ セクションと Power BI セクションを必要に応じて含めることができます。

### <a name="view-the-workspace"></a>ワークスペースの表示

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
2. **Ctrl+F5** キーを押して、フォームをビルドおよび実行します。 Internet Explorer でフォームが開きます。

    ![フォームを開く](./media/fmtworkspaceinitial.png)

## <a name="exercise-2-create-a-new-tile-for-the-workspace"></a>手順 2: ワークスペースの新しいタイルを作成

ワークスペースのコンテンツ構造がわかったので、ワークスペースにコンテンツを追加する方法を見てみます。 たとえば、このワークスペースに対する 1 つの重要な情報は、現在進行中であるレンタル数である可能性があります。 このセクションでは、**FmtClerkWorkspace** フォームの **概要** セクションに新しいタイルを追加してこの情報を表示するために必要なメタデータを追加します。 このタイルを正しく機能させるには、クエリ、メニュー項目、タイル、タイル ボタンの 4 つのメタデータ アーティファクトを追加する必要があります。

### <a name="add-a-query-that-retrieves-current-rentals"></a>現在のレンタルを取得するクエリの追加

すべてのタイルは、正しい情報を取得するバッキング クエリが必要です。

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **データ モデル** \> **クエリ** の順にクリックします。 **名前** プロパティについては、**FMTRental\_Current** を入力します。
3. **追加** をクリックします。
4. 新しい **FMTRental\_Current** クエリーがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. デザイナーで、**データ ソース** を右クリックしてから **新しいデータ ソース** をクリックします。
6. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ        | 先頭値     |
    |-----------------|-----------|
    | テーブル           | FMTRental |
    | Dynamics フィールド | 有       |

7. **範囲** を右クリックし、**新しい範囲** をクリックします。
8. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ | 先頭値      |
    |----------|------------|
    | フィールド    | 行政単位 (区画)      |
    | 先頭値    | InProgress |

9. **並べ替え** を右クリックし、**新しいフィールド** をクリックします。
10. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ    | 先頭値      |
    |-------------|------------|
    | 方向   | 降順 |
    | データ ソース | FMTRental  |
    | フィールド       | StartDate  |

11. **Ctrl+S** キーを押して保存します。

### <a name="add-the-corresponding-menu-item"></a>対応するメニュー項目の追加

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**メニュー項目** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **ユーザー インターフェイス** \> **表示メニュー項目** の順にクリックします。 **Name** プロパティを **FMTRental\_Current** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTRental\_Current** メニュー項目がデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. **プロパティ** ウィンドウで、次のプロパティを設定します。

   | プロパティ |                                    先頭値                                    |
   |----------|-----------------------------------------------------------------------------|
   |  ラベル   | @FMT197 この値は “現在のレンタル” に対応します。 |
   |  オブジェクト  | FMTRental                                  |
   |  クエリ   | FMTRental\_Current                              |

6. **Ctrl+S** キーを押して保存します。

### <a name="add-a-tile"></a>タイルの追加

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**タイル** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **ユーザー インターフェイス** \> **タイル** の順にクリックします。 **Name** プロパティを **FMTCurrentRentalsTile** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTRental\_Current** タイルがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ       | 先頭値              |
    |----------------|--------------------|
    | サイズ           | ShortWide          |
    | メニュー項目名 | FMTRental\_Current |
    | 種類           | COUNT              |

6. **Ctrl+S** キーを押して保存します。

タイルには、タイルのカウントが自動的に更新される頻度を制御するリフレッシュ頻度プロパティもあります。 このプロパティに設定されている値は、ボリューム データに対するクエリの実行速度とともに、更新されたカウントの要求に基づいている必要があります。 このプロパティを設定する方法の指針については、[ワークスペースのタイルおよびリストのキャッシュ](tile-list-caching-workspaces.md) を参照してください。 このラボでは、10 分の既定値で十分です。

### <a name="add-a-tile-button-to-the-workspace-form"></a>ワークスペースのフォームへのタイル ボタンの追加

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。
2. **デザイン** \> **PanoramaBody** \> **TileContainer** を右クリックして **新規** をポイントし、**ボタンを並べて表示** をクリックします。
3. **Alt+上方向キー** を 4 回押して、タイル ボタンを TileContainer の上部に移動します。
4. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ | 先頭値                 |
    |----------|-----------------------|
    | 氏名     | FMTCurrentRentalsTile |
    | タイル     | FMTCurrentRentalsTile |

5. **Ctrl+S** キーを押して保存します。

### <a name="view-the-new-tile-on-the-workspace"></a>ワークスペース上の新規タイルの表示

Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
2. **Ctrl+F5** キーを押して、フォームをビルドおよび実行します。 Internet Explorer でフォームが開きます。

    [![レンタル タイル](./media/currentrentalstile.png)](./media/currentrentalstile.png)

3. **現在のレンタル** タイルをクリックします。 **レンタル** ページに移動し、それは 3 つの現在のレンタルにフィルター処理する必要があります。
4. **戻る** ボタン、または **閉じる** ボタンをクリックし、ワークスペースに戻ります。
5. **現在のレンタル** タイルの右上隅にある小さな **i** ボタンをクリックします。 並べて表示されたデータに関する情報が、どの程度新しいかが確認できます。 また、更新されたデータを表示するためのタイルを手動で更新するために使用できるリンクが指定されます。

### <a name="view-tile-data-cache-values-at-run-time"></a>実行時のタイル データ キャッシュ値の表示

システム管理者は、実行時に **タイル データ キャッシュ コンフィギュレーション** ページを使用して、タイル キャッシュ パラメーターを変更できます。

1. ナビゲーション バーのナビゲーション検索フィールドをクリックします。
2. **タイル データ** を入力し、検索結果の **タイル データ キャッシュ構成** をクリックします。
3. **FMTCurrentRentalsTile** レコードを検索します。

    ![タイル キャッシュ パラメーター](./media/tilecacheparams.png)

このページから、システム管理者はタイル キャッシュにいくつかのランタイム変更を実行できます。 たとえば、システム管理者は、データ キャッシュの有効化/無効化、更新頻度の変更、およびカウント タイルを手動で更新する機能の有効化/無効化をすることができます。 タイル キャッシュは、タイルのあるフォームが最初に開かれたときに登録されることに注意してください。 したがって、ご使用の環境に表示されているタイルのリストが、上の図のリストと異なる場合があります。

## <a name="exercise-3-create-a-new-tabbed-list-in-the-workspace"></a>手順 3: ワークスペースに新しいタブ リストを作成

次に、ワークスペースに追加のリストを含める方法を確認します。 このセクションでは、フォームを作成する際の経験を紹介し、フォーム パターンも公開します。 利用可能な車両を選択することによって新しいレンタルを開始できるように、利用可能な車両の一覧を追加します。 このセクションでは、新しいワークスペースに新しいリストを追加するだけで、レンタルを開始するアクションは追加しません。 このリストを追加するには、次のタスクを完了する必要があります。

1. ワークスペースに新しいタブ ページを追加します。
2. リストの内容を持つ新しいフォームを追加します。
3. 新しいフォームを示す新しいメニュー項目を追加します。
4. 車両を使用可能な車両に限定する新しいクエリを追加します。

### <a name="add-space-in-the-workspace-for-a-new-list"></a>新しいリストのワークスペースへのスペースの追加

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。
2. **デザイン** \> **PanoramaBody** \> **TabbedListSection** \> **TabbedLists** を右クリックし、**新しいタブ ページ** をクリックします。
3. **プロパティ** ウィンドウで、次のプロパティを設定します。

   | プロパティ | 先頭値 |
   |----------|-------|
   | 氏名     | AvailableVehiclesContainer                           |
   | キャプション  | @FMT199 この値は “使用可能な車両” に対応します。 |

4. **AvailableVehiclesContainer** を右クリックし、**新規** をポイントして、**パーツから** をクリックします。 **フォーム パート** は運用ワークスペースのパターンにより、ここで唯一許可されるコントロール タイプです。 このコントロールは、このセクションのコンテンツを保持するためにビルドするフォームにリンクするために使用されます。

   ![セクションを追加](./media/addsection1.png)

5. **プロパティ** ウィンドウで、**名前** プロパティを **AvailableVehiclesPart** に設定します。
6. **Ctrl+S** キーを押して保存します。

### <a name="add-a-new-form-that-has-the-new-workspace-content"></a>新しいワークスペースの内容を持つ新しいフォームを追加します。

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**フォーム** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **ユーザー インターフェイス** \> **フォーム** の順にクリックします。 **Name** プロパティを **FMTAvailableVehicles** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTAvailableVehicles** フォームがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. フォームのデータ ソースとして **FmtVehicle** テーブルを追加します。
    1. **データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。
    2. 新しいデータ ソース ノードをクリックします。 **プロパティ** ウィンドウで、次のプロパティを設定します。

        | プロパティ | 先頭値                                                                                                                                                      |
        |----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
        | テーブル    | FMTVehicle                                                                                                                                                 |
        | 氏名     | FMTVehicle **注記:** 最初に **Table** プロパティの値を指定してください。 このプロパティは、同じ値を使用するように自動的に更新されます。 |

6. フォームの 2 番目のデータ ソースとして **FmtVehicleModel** テーブルを追加します。
    1. **データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。
    2. 新しいデータ ソース ノードをクリックします。 **プロパティ** ウィンドウで、次のプロパティを設定します。

        | プロパティ    | 先頭値                                                                                                                                                           |
        |-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
        | テーブル       | FMTVehicleModel                                                                                                                                                 |
        | 氏名        | FMTVehicleModel **注記:** 最初に **Table** プロパティの値を指定してください。 このプロパティは、同じ値を使用するように自動的に更新されます。 |
        | ソースの結合 | FMTVehicle                                                                                                                                                      |
        | リンク タイプ   | 内部結合                                                                                                                                                      |

7. **パターン: \<select\>** の記法が **フォーム デザイン** の横にあることに注目してください。 これは、このノードに必要なパターンを示します。 **デザイン** を右クリックして **パターンの適用** をポイントし、**フォーム パターン セクション リスト** をクリックします。 このフォーム パターンは通常、ワークスペースのリストで使用されます。
8. このパターンの予想されるコンテンツを表示するには、**パターン** タブをクリックします。 この情報は、フォームのコンテンツを作成する際に役立ちます。 **注記:** 今後は、選択したフォーム パターンに基づいて自動的にフォーム構造を作成するメカニズムを提供する予定です。

    [![セクション リスト](./media/formpartsectionlist.png)](./media/formpartsectionlist.png)

    特に、このパターンは次の要素を検索します。
    - ワークスペース リストに必要なすべてのフィルターおよびアクションを含むオプションのヘッダー グループです。
    - 必要なグリッド。 前の図の赤い枠線が示すように、パターン エンジンは現在この要素を見つけることができません。
    - オプションの既定アクションは、グリッド内の個々のレコードのバッキング フォームへのナビゲーションを提供できます。
    - オプション ボタンで、このセクションの品目の完全なリストを表示するバッキング フォームへユーザーを移動させます。

9. **デザイン** を右クリックして **新規** をクリックし、**グリッド** をクリックします。
10. **プロパティ** ウィンドウで、次のプロパティを設定します。 **注記:** 構築中のグリッドには複数のカードが含まれ、カード 2 枚の幅になります。

    | プロパティ             | 先頭値       |
    |----------------------|-------------|
    | ExtendedStyle        | cardList    |
    | 複数選択         | 無          |
    | スタイル                | リスト        |
    | データ ソース          | FMTVehicle  |
    | 氏名                 | VehicleList |
    | 表示されている列のモード | 開始日固定       |
    | 表示されている列      | 2           |

11. **VehicleList** グリッドを右クリックして **新規** をクリックし、**Group** をクリックします。
12. **プロパティ** ウィンドウで、**名前** プロパティを **VehicleCard** に設定します。
13. **VehicleCard** グループを右クリックして **パターンの適用** をポイントし、**ビジネス カード – 3 つのフィールド** をクリックします。
14. **VehicleCard** グループを右クリックして **新規** をクリックし、**Image** をクリックします。
15. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ    | 先頭値           |
    |-------------|-----------------|
    | データ ソース | FMTVehicleModel |
    | データ メソッド | vehicleImage    |

16. **データ ソース** \> **FMTVehicle** \> **フィールド** を展開します。
17. **VehicleId** および **DisplayRelationType** フィールドを **VehicleCard** グループにドラッグします。
18. **デザイン** を右クリックして **新規** をクリックし、**グループ** をクリックします。 新しいグループの **Name** プロパティを **HeaderGroup** に更新します。
19. 新しい HeaderGroup 要素にはサブパターンが必要です。これは、これらのセクションのフィルターとアクションの配置に 2 つのバリアントがあるためです。 **HeaderGroup** を右クリックして **パターンの適用** をポイントし、**フィルターとツール バー - インライン** をクリックします。
20. **HeaderGroup** を右クリックして **新規** をクリックし、**グループ** をクリックします。 新しいグループの **Name** プロパティを **FilterGroup** に更新します。
21. **FilterGroup** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。
22. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ       | 金額              |
    |----------------|--------------------|
    | 氏名           | VehicleQuickFilter |
    | ターゲット コントロール | VehicleList        |

23. **Ctrl+S** キーを押して保存します。

### <a name="add-a-new-query-that-limits-the-data-to-available-vehicles"></a>データを使用可能な車両に限定する新しいクエリの追加

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **データ モデル** \> **クエリ** の順にクリックします。 **Name** プロパティを **FMTAvailableVehicles** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTAvailableVehicles** クエリがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. デザイナーで、**データ ソース** を右クリックしてから **新しいデータ ソース** をクリックします。
6. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ        | 金額       |
    |-----------------|-------------|
    | テーブル           | FMTVehicle  |
    | Dynamics フィールド | はい         |

7. **範囲** を右クリックし、**新しい範囲** をクリックします。
8. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ | 先頭値     |
    |----------|-----------|
    | フィールド    | ステータス    |
    | 先頭値    | 取得可能 |

9. **Ctrl+S** キーを押して保存します。

### <a name="add-a-new-menu-item-that-references-the-new-form"></a>新しいフォームを参照する新しいメニュー項目の追加

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**メニュー項目** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **ユーザー インターフェイス** \> **表示メニュー項目** の順にクリックします。 **Name** プロパティを **FMTAvailableVehicles** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTAvailableVehicles** メニュー項目がデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ       | 金額                |
    |----------------|----------------------|
    | オブジェクト         | FMTAvailableVehicles |
    | クエリ          | FMTAvailableVehicles |

6. **Ctrl+S** キーを押して保存します。

### <a name="link-the-new-list-to-the-workspace"></a>新しいリストのワークスペースへのリンク

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。
2. **デザイン** \> **PanoramaBody** \> **TabbedListSection** \> **TabbedLists** \> **AvailableVehiclesContainer** \> **AvailableVehiclesPart** の順にクリックします。
3. **プロパティ** ウィンドウで、**メニュー項目名** プロパティを **FmtAvailableVehicles** に設定します。

### <a name="view-the-new-menu-item"></a>メニュー項目を表示する

Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
2. **Ctrl+F5** キーを押して、フォームをビルドおよび実行します。 Internet Explorer でフォームが開きます。

    ![使用可能なリスト](./media/availablelist.png)

3. **使用可能な車両** タブをクリックし、新しいリストを表示します。
4. QuickFilter をクリックして **Lit** と入力し、**Enter** を押して利用可能な Litware モデルの車両に絞り込みます。

## <a name="exercise-4-create-a-backing-data-cache-for-a-list"></a>手順 4: リストのバック データ キャッシュを作成

価値が高いクエリのリスト、同じワークスペースから複数のユーザーが使用し作業する場合があるリストについては、パフォーマンスを向上させるためにリストのキャッシュを考慮してください。 このセクションでは、一覧のデータ キャッシュを作成するために必要なコンポーネントを追加します。 これらのコンポーネントには、フィールドをキャッシュにマップするクエリ、キャッシュを保持するテーブル、クエリとテーブルの間のマッピングを提供するクラスが含まれます。 次に、ワークスペース内のいずれかのタブ付きリストにこのキャッシュを取り込みます。

### <a name="add-a-query-that-maps-fields-to-the-data-cache"></a>フィールドをデータ キャッシュにマップするクエリの追加

最初のステップでは、キャッシュ テーブルを作成するために使用されるクエリをビルドします。 このクエリには、キャッシュ データを取得するすべてのテーブルが含まれている必要があります。また、結果をキャッシュするレコード/列に限定する必要があります。

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **データ モデル** \> **クエリ** の順にクリックします。 **Name** プロパティを **FMTPickupAndReturnQuery** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTPickupAndReturnQuery** クエリがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. デザイナーで、**データ ソース** を右クリックしてから **新しいデータ ソース** をクリックします。
6. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ        | 先頭値     |
    |-----------------|-----------|
    | テーブル           | FMTRental |
    | Dynamics フィールド | 無        |

7. FMTRental データ ソースに、次の 5 つのフィールドを追加します。 各フィールドについては、**フィールド** を右クリックし、**新規** を指し、次に **フィールド** をクリックします。 **プロパティ** ウィンドウで、必要に応じて **フィールド** プロパティを設定します。
    - StartDate
    - EndDate
    - 車両
    - 行政単位 (区画)
    - RentalId

8. **範囲** を右クリックし、**新しい範囲** をクリックします。
9. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ | 先頭値                                                                                  |
    |----------|----------------------------------------------------------------------------------------|
    | フィールド    | 行政単位 (区画)                                                                                  |
    | 先頭値    | 1..2 **注記:** この値は受取準備完了または処理中のレンタルをキャッシュします。 |

10. **FMTRental** で **データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。
11. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ        | 先頭値       |
    |-----------------|-------------|
    | テーブル           | FMTCustomer |
    | Dynamics フィールド | 無          |

12. FMTCustomer データ ソースに、次の 3 つのフィールドを追加します。 各フィールドについては、**フィールド** を右クリックし、**新規** を指し、次に **フィールド** をクリックします。 **プロパティ** ウィンドウで、必要に応じて **フィールド** プロパティを設定します。
    - 名
    - 姓
    - 画像

13. **関係** を右クリックし、 **新しい関係** をクリックします。
14. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ         | 先頭値     |
    |------------------|-----------|
    | データ ソースの結合 | FMTRental |
    | フィールド            | 顧客  |
    | 関連フィールド    | RecID     |

    作成したクエリは、次の図と一致する必要があります。

    ![キャッシュ クエリ](./media/cachequery.png)

15. **Ctrl+S** キーを押して保存します。

### <a name="add-a-cache-table"></a>キャッシュ テーブルの追加

2 番目のステップでは、キャッシュ クエリから返されるフィールドを持つテーブルを定義します。 キャッシュ行をベース フレームワーク キャッシュ テーブルにマップするために使用される **SysDataCacheContextId** フィールドを追加することも必要です。 また、このテーブルと他のテーブルとの間に必要な関係を定義する必要もあり、関係するキャッシュされたフィールドを必要とするデータ メソッドも必要です。

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**テーブル** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **データ モデル** \> **テーブル** の順にクリックします。 **Name** プロパティを **FMTPickupAndReturnTableCache** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTPickupAndReturnTableCache** テーブルがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. デザイナーで、**フィールド** を右クリックしてから、次のフィールドを追加します。 各フィールドについては、次の表は、データ型および拡張データ型 (EDT) または列挙型を表示します。

    | フィールド タイプ    | フィールド名            | EDT/ 列挙型タイプ               |
    |---------------|-----------------------|-----------------------------|
    | 文字列        | 名             | FirstName (EDT)             |
    | 文字列        | 姓              | LastName (EDT)              |
    | コンテナー     | 画像                 | ビットマップ (EDT)                |
    | Int64         | 車両               | FMTVehicleRecId (EDT)       |
    | UTC 日時 | StartDate             | StartDateTime (EDT)         |
    | UTC 日時 | EndDate               | EndDateTime (EDT)           |
    | Int64         | SysDataCacheContextId | SysDataCacheContextId (EDT) |
    | 列挙          | 行政単位 (区画)                 | FMTReservationState (Enum)  |
    | 文字列        | RentalId              | FMTRentalId (EDT)           |

6. デザイナーで、**リレーション** を右クリックし、**新規** をポイントしてから **リレーション** をクリックします。
7. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ      | 先頭値     |
    |---------------|-----------|
    | 氏名          | FMTRental |
    | 関連テーブル | FMTRental |

8. **FMTRental** 関係を右クリックし、**新規** をポイントして **標準** をクリックします。
9. **プロパティ** ウィンドウで、次のプロパティを設定します。

    | プロパティ      | 先頭値    |
    |---------------|----------|
    | フィールド         | RentalId |
    | 関連フィールド | RentalId |

10. デザイナーで、**マッピング** を右クリックしてから **新規** をクリックします。
11. **プロパティ** ウィンドウで、**マップ** プロパティを **SysDataSetCacheTableMap** に設定します。
12. **ID** をクリックします。 **プロパティ** ウィンドウで、**フィールドのマップ** プロパティを **RecId** に設定します。
13. **SysDataCacheContextId** をクリックします。 **プロパティ** ウィンドウで、**フィールドのマップ** プロパティを **SysDataCacheContextId** に設定します。 **注記:** フィールドが一覧に表示されない場合は、**Ctrl+S** キーを押してテーブルを保存しなければならない場合があります。
14. **F7** キーを押して、テーブルのコードを表示します。 または、**FMTReturnAndPickupTableCache** を右クリックし、その後 **コードの表示** をクリックします。
15. テーブルに、次の表示メソッドを追加します。 フォームは後でこれらのメソッドを使用します。

    ```xpp
    public display FMTName fullName()
    {
        return this.FirstName + ' ' + this.LastName;
    }
    public display container customerImage()
    {
        ImageReference imgRef;
        container imgContainer = this.Image;
        if(imgContainer == connull())
            {
                imgRef = ImageReference::constructForSymbol("Person");
                imgContainer = imgRef.pack();
            }
            return imgContainer;
    }
    public display str rentalVehicle()
    {
        FMTVehicle vehicle;
        str value;
        if(this.Vehicle == 0)
        {
            value = "No vehicle assigned";
        }
        else
        {
            select vehicle where vehicle.RecId == this.Vehicle;
            value = vehicle.Description;
        }
        return value;
    }
    ```

16. **Ctrl+S** キーを押して保存します。

### <a name="adding-a-cache-class-that-links-the-query-and-table"></a>クエリとテーブルをリンクするキャッシュ クラスの追加

3 番目のステップは、キャッシュ クエリとキャッシュ テーブルの間のリレーションシップを定義するクラスを作成することです。

1. ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クラス** フォルダーを右クリックし、**追加** をポイントしてから **新しい項目** をクリックします。
2. **Dynamics 365 品目** \> **コード** \> **クラス** の順にクリックします。 **Name** プロパティを **FMTPickupAndReturnClass** に置き換えます。
3. **追加** をクリックします。
4. 新しい **FMTPickupAndReturnClass** クラスがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。
5. クラスに次のコードを追加します。

    ```xpp
    [SysDataSetExtension(classStr(FMTPickupAndReturnClass)), // The name of this class
    SysDataSetCacheTableExtension(tableStr(FMTPickupAndReturnTableCache))] // The name of the cache table
    class FMTPickupAndReturnClass extends SysDataSetQuery implements SysIDataSet
    {
        public SysDataCacheRefreshFrequency parmRefreshFrequency()
        {
            return 600; // Cache refresh frequency, in seconds.
        }
        public SysQueryableIdentifier parmQueryableIdentifier()
        {
            return queryStr(FMTPickupAndReturnQuery); // The name of the query.
        }
        public SysDataCacheTypeId parmCacheTypeId()
        {
            return tableNum(FMTPickupAndReturnTableCache); // The name of the table.
        }
        public static FMTPickupAndReturnClass construct()
        {
            return new FMTPickupAndReturnClass();
        }
    }
    ```

6. **Ctrl+S** キーを押して保存します。

### <a name="uptake-the-data-cache-on-a-list-in-the-workspace-and-table"></a>ワークスペースとテーブルの一覧にあるデータ キャッシュを読み込む

データ キャッシュを設定した後、フォーム内でキャッシュの使用を開始することができます。 このセクションでは、データ キャッシュを使用するようワークスペース リストのいずれかを更新します。

1. ソリューション エクスプローラーで、**FMTReturningTodayPart** フォームをダブルクリックしてデザイナーで開きます。
2. **データ ソース** ノードを展開します。
3. **FMTCustomer** データソースを削除します。
4. **FMTRental** データ ソースをクリックします。 **プロパティ** ウィンドウで、**テーブル** プロパティを **FMTPickupAndReturnTableCache** に設定します。
5. **デザイン** \> **ReturningTodayGrid** とクリックします。 **プロパティ** ウィンドウで、**データ ソース** プロパティを **FMTPickupAndReturnTableCache** に設定します。
6. **ReturningTodayGrid** 内で、**CustomerImage** をクリックします。 **データ ソース** プロパティを **FMTPickupAndReturnTableCache** に、**データ メソッド** プロパティを **customerImage** に更新します。
7. **ReturningTodayGrid** 内で、**FirstNameCopy1** をクリックします。 **データ ソース** プロパティを **FMTPickupAndReturnTableCache** に、**データ メソッド** プロパティを **fullName** に更新します。
8. **F7** キーを押して、フォームのコードを表示します。
9. 次のコードに示すように、データ キャッシュに対処できることができるようフォームをインストルメント化します。

    ```xpp
    [Form]
    public class FMTReturningTodayPart extends FormRun implements SysIDataSetConsumerForm
    {
        public void registerDatasourceOnQueryingEvent()
        {
            FMTPickupAndReturnTableCache_DS.OnQueryExecuting +=
                eventhandler(this.parmDataSetFormQueryEventHandler().prepareDataSet);
        }
    }
    ```

10. **Ctrl+S** キーを押して保存します。

### <a name="update-the-action-above-the-list-so-that-it-works-with-the-cache-table"></a>キャッシュ テーブルで動作するようにリストにあるアクションを更新する

ワークスペースから実行されるアクションは、ベース テーブルからのレコードが必要とするかもしれません。 したがって、これらのアクションを更新してキャッシュ テーブルと連携させる必要があります。 この例では、**FmtCompleteRecord** は **FMTRental** レコードをコンテキストとして期待しています。 したがって、このフォームを更新して、ベース レンタル レコードまたはキャッシュ テーブル レコードのいずれかで正しく動作するようにする必要があります。

1. ソリューション エクスプローラーで、**FmtCompleteRental** フォームをダブルクリックしてデザイナーで開きます。
2. **F7** キーを押して、フォームのコードを表示します。

    ```xpp
    public void init()
    {
        //If this form was opened with a Rental as context
        if(element.args() != null && element.args().record() != null && element.args().record().TableId == tablenum(FMTRental))
        {
            //Get the Rental context
            rentalDS = FormDataUtil::getFormDataSource(element.args().record());
            rental = element.args().record();
            if(rental != null)
            {
                select firstonly forupdate vehicle where vehicle.RecId == rental.Vehicle;
            }
        }
        super();
    }
    ```

3. **init()** メソッドを次のコードと一致するように更新します。

    ```xpp
    public void init()
    {
        //If this form was opened with a record context
        if(element.args() != null && element.args().record() != null))
        {
            //Get that context
            rentalDS = FormDataUtil::getFormDataSource(element.args().record());
            if(element.args().record().TableId == tableNum(FMTPickupAndReturnTableCache))
            {
                FMTPickupAndReturnTableCache cacheRecord = element.args().record();
                select firstonly forupdate rental where rental.RentalId == cacheRecord.RentalId;
            }
            else if(element.args().record().TableId == tableNum(FMTRental))
            {
                rental = element.args().record();
            }
            if(rental != null)
            {
                select firstonly forupdate vehicle where vehicle.RecId == rental.Vehicle;
            }
        }
        super();
    }
    ```

4. **Ctrl+S** キーを押して保存します。

### <a name="update-the-returning-today-query-so-that-it-works-with-the-cache-table"></a>キャッシュ テーブルで動作するように Returning today クエリ を更新する

1. ソリューション エクスプローラーで、**FmtRental\_ReturningToday** クエリをダブルクリックしてデザイナーで開きます。
2. **データ ソース** ノードを展開し、**FMTRental** をクリックします。
3. **プロパティ** ウィンドウで、**テーブル** プロパティを **FMTPickupAndReturnTableCache** に更新します。 **注記:** **名前** プロパティは、自動的に同じ値に更新されます。
4. **Ctrl+S** キーを押して保存します。

### <a name="view-the-updated-query"></a>更新されたクエリの表示

Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
2. **Ctrl+F5** キーを押して、フォームをビルドおよび実行します。 Internet Explorer でフォームが開きます。
3. **今日を返す** 垂直タブをクリックします。
4. リストの 2 番目のレコードに対する **完全レンタル** をクリックします。
5. **終了マイレージ** を **200** に設定し、**OK** をクリックします。 返却されたレンタルがまだ一覧に表示されていることを確認します。

### <a name="make-sure-that-your-workspace-is-responsive"></a>ワークスペースが応答可能であることを確認します。

一覧からレコードを削除する (例えばユーザーがレンタルを完了させる) アクションをユーザーが行った後は、ご自分の一覧を最新に保つようにしてください。 このセクションでは、ワークスペースが適切に反応することを保証するために、そのアクションをインストルメント化します。

1. ソリューション エクスプローラーで、**FmtCompleteRental** フォームをダブルクリックしてデザイナーで開きます。
2. **F7** キーを押して、フォームのコードを表示します。
3. **OKButton** の **clicked()** コードを検索します。 呼び出しフォームでのデータ ソースの調査呼び出しは、このメソッドの最後の方です。 そのコード行の直前に、次の **if** ステートメントを追加してキャッシュ テーブルから処理済のレンタルを削除します。

    ```xpp
    . . .
    if(rentalDS.table() == tableNum(FMTPickupAndReturnTableCache))
    {
        //Delete updated record from backing cache
        FMTPickupAndReturnTableCache cacheRecord = element.args().record();
        cacheRecord.delete();
    }
    rentalDS.research(true);
    }
    ```

4. **Ctrl+S** キーを押して保存します。

### <a name="view-the-updated-form"></a>更新されたフォームの表示

Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。

1. ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。
2. **Ctrl+F5** キーを押して、フォームをビルドおよび実行します。 Internet Explorer でフォームが開きます。
3. **今日を返す** 垂直タブをクリックします。
4. リストの 2 番目のレコードに対する **完全レンタル** をクリックします。
5. **終了マイレージ** を **100** に設定し、**OK** をクリックします。 返却されたレンタルが一覧に表示されなくなったことを確認します。

## <a name="related-tutorials"></a>関連するチュートリアル

- [顧客フォームの作成](build-customer-form.md) – フォーム パターンを公開する場合は、このチュートリアルを参照してください。 このチュートリアルでは、詳細マスター パターンをフォームに適用するプロセスについて説明します。
- [ナビゲーションの構築](build-navigation.md) – メニュー構造にワークスペースを追加する方法については、このチュートリアルを参照してください。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]