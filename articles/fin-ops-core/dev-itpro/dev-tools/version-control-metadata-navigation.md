---
title: バージョン コントロール、メタデータ検索、およびナビゲーション
description: このチュートリアルでは、Azure DevOps をコンフィギュレーションして、モデルのソース管理を有効にします。
author: RobinARH
ms.date: 07/24/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.custom: 23401
ms.assetid: 46ed0115-6f8b-4757-b8d2-d4ccb76c733d
ms.search.region: Global
ms.author: jorisde
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51e75682a7037713b1db0eba1ad7b4d82592a9bd
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782461"
---
# <a name="version-control-metadata-search-and-navigation"></a>バージョン コントロール、メタデータ検索、およびナビゲーション

[!include [banner](../includes/banner.md)]

このチュートリアルでは、Microsoft Azure DevOps をコンフィギュレーションして、モデルのソース管理を有効にします。 これは、TODO タスクの作成および整理、メタデータおよびソース コードの検索、関連するモデル要素間の移動、モデルからのプロジェクトの作成を行う機能など、開発ツールでのその他の生産性機能について把握することにも役立ちます。

## <a name="configure-your-azure-devops-organization-and-project"></a>Azure DevOps 組織およびプロジェクトをコンフィギュレーションする

このセクションでは、Azure DevOps で新しいプロジェクトを作成します。 このプロジェクトはモデルのソース コードをホストします。 例として、フリート管理モデルを使用します。 Azure DevOps 組織をお持ちでない場合は、作成します。

### <a name="sign-up-to-azure-devops-create-an-account-and-create-a-new-project"></a>Azure DevOps への登録、アカウントの作成、および新しいプロジェクトの作成

<https://www.visualstudio.com/> に移動して Azure DevOps にサインアップします。 **サインアップ** をクリックします。 Azure DevOps アカウントを既に持っている場合は、このトピックの後半の「Azure DevOps プロジェクトの作成」セクションに移動します。

1. Microsoft アカウントでサインインします。

    > [!NOTE]
    > 組織のアカウント (Microsoft 365 ドメイン) を使用することもできます。

2. Azure DevOps 組織を作成し、アカウントの URL を選択します。 Visual Studio でソース管理を設定するときに、開発用コンピューターから接続する URL を使用します。 次の図は、アカウント URL の例です。

    ![アカウントの URL を選択します。](./media/accounturl_usingdevotools.png)

    アカウントが作成されると、アカウントのメイン ページに進むように指示され、そこで最初のプロジェクトの作成を求められます。
3. デモ **フリート管理** プロジェクトを作成します。

    ![最初のプロジェクトを作成します。](./media/firstproject_usingdevotools.png)

### <a name="create-a-azure-devops-team-project"></a>Azure DevOps チーム プロジェクトの作成

Azure DevOps 組織を既に持っている場合は、Internet Explorer を使用してアカウントに移動します。 このトピックでは、説明のために URL の例として **.visualstudio.com** を使用します。

1. <https://www.visualstudio.com/> に移動します。
2. **最近使用したプロジェクトとチーム** で **新規** をクリックして新しいプロジェクトを作成します。

   ![新しいプロジェクトを作成します。](./media/clicknew_usingdevotools.png)

3. **プロジェクト名** フィールドに、**フリート管理** と入力し、**説明** を入力してから **プロジェクトの作成** をクリックします。

### <a name="create-the-recommended-folder-structure-in-your-team-project"></a>チーム プロジェクトで推奨するフォルダー構造を作成する

Lifecycle Services (LCS) 自動化コードのアップグレード ツールを使用して以前のバージョンからコードを移行した場合、以下のフォルダ構造は、Azure DevOps チーム プロジェクトで自動的に作成されます。

![既定のフォルダー構造。](./media/vsofolders1.png)

**メタデータ** フォルダーには、パッケージとモデルによって整理されたソース XML ファイルがあり、**プロジェクト** フォルダーには Visual Studio プロジェクトが含まれています。 コードを移行せず、最初から開始している場合、開発を開始する前に、チーム プロジェクト内のサーバーに類似したフォルダ構造を作成します。

### <a name="configure-visual-studio-to-connect-to-your-team-project"></a>Visual Studio をコンフィギュレーションしてチーム プロジェクトに接続する

1. Visual Studio を起動します。 マシンに管理者としてログインしている場合は、Visual Studio を管理者として起動する必要があります。
2. **ツール &gt; オプション &gt; ソース管理 &gt; プラグインの選択** の順にクリックします。
3. 現在のソース管理プラグイン フィールドで **Visual Studio Team Foundation Server** を選択します。
4. **チーム &gt; Team Foundation Server に接続** を選択します。
5. **チーム エクスプローラー** で、**チーム プロジェクトの選択** をクリックします。
6. **Team Foundation Server の選択** ドロップダウン リストで、フリート管理プロジェクトをホストする **Azure DevOps 組織** を選択するか、メニューにない場合は **サーバー** をクリックします。
    1. **Team Foundation Server の追加および削除** ダイアログ ボックスが開いたとき、**追加** をクリックします。
    2. Azure DevOps 組織の URL を入力します。
    3. **OK** をクリックします。
    4. メッセージが表示されたら、Microsoft アカウントのユーザー名とパスワードを入力します。

7. **チーム プロジェクト** で **フリート管理** チェック ボックスをオンにし、**接続** をクリックします。

    ![Team Foundation Server に接続します。](./media/connecttfsserver_usingdevotools.png)

### <a name="map-your-azure-devops-project-to-your-local-model-store-and-projects-folder"></a>Azure DevOps プロジェクトをローカルのモデル ストアとプロジェクト フォルダーにマップ

モデル ストアのルート フォルダーには、アプリケーションの一部であるすべてのパッケージとモデルのソース ファイルが含まれています。 展開中には、複数のパッケージにまたがる複数のモデルのソース ファイルを使用するでしょう。 モデル ストアのルート フォルダーを Azure DevOps のチーム プロジェクト メタデータ フォルダーにマップすることをお勧めします。

1. Visual studio の **チーム エクスプローラー** で、このドキュメントで前に説明したようにチーム プロジェクトに接続します。
2. **ソース管理エクスプローラー** から **チーム エクスプローラー** を開きます。
3. チーム プロジェクトの **メタデータ** フォルダーを、ローカル ドライブのモデル ストアのルート フォルダー (通常は K:\\AOSService\\PackagesLocalDirectory) にマップします。例を以下の図に示します。

    > [!NOTE]
    > マシンの構成によっては、モデル ストアが I:\\AosService\\PackagesLocalDirectory または別のドライブの配下にある場合があります。

    ![ワークスペース マッピングを作成します。](./media/vsofolders21.png)

4. **マップ** をクリックし、次のダイアログ ボックスで、**No** をクリックします。
5. 同様に、**/Trunk/Main/Projects** サーバー フォルダーを、Visual Studio ソリューションとプロジェクト ファイルを保持する **ローカル プロジェクト フォルダー** にマッピングします。

## <a name="scenario-1-open-the-fleet-management-solution-and-add-it-to-azure-devops-source-control"></a>シナリオ 1: フリート管理ソリューションを開き、Azure DevOps ソース管理に追加する

このセクションでは、Azure DevOps のソース管理にソリューションを追加するために必要なステップについて説明します。 このシナリオは、新しいモデルで開発を開始し、初めてソース管理に追加する場合に関係します。 コード移行シナリオまたは他の開発者により作成された新しいモデルを同期する場合は、以下のシナリオ 2 を参照してください。

### <a name="open-the-fleetmanagement-solution"></a>FleetManagement ソリューションを開く

> [!NOTE]
> このプロジェクトは単なる一例です。 任意のプロジェクト/ソリューションを開いて、ソリューションをソース管理に追加するプロセスについて学習することができます。

1. **ファイル** メニューで、**開く** をポイントし、**プロジェクト/ソリューション** をクリックします。
2. デスクトップを参照し、**FleetManagement** フォルダーを開きます。
3. **FleetManagement** という名前のソリューション ファイルを選択します。 表示されるファイル タイプは Microsoft Visual Studio Solution です。 ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。
4. **開く** をクリックします。 ソリューションの読み込みには時間がかかる場合があります。

### <a name="add-the-fleetmanagement-solution-to-source-control"></a>ソース コントロールへの FleetManagement ソリューションの追加

1. **ソリューション エクスプローラー** で、フリート管理ソリューションを右クリックして、**ソリューションをソース管理に追加** を選択します。
2. 次のダイアログで、**Team Foundation バージョン管理** を選択し、**次へ** をクリックします。
3. **チーム プロジェクト ロケーション** にて、以下画像のように **プロジェクト** を選択します。

    > [!NOTE]
    > サーバープロジェクト フォルダ を FleetManagement ソリューションを含むローカルフォルダに既にマッピングしている場合は、手順2 と 3 を省略します。

    ![Team Foundation Server のフォルダー構造。](./media/vsofolders31.png)

4. [OK] をクリックします。
5. **チーム エクスプ ローラー &gt; 保留中の変更** に移動し、**チェックイン** をクリックして、ソリューションおよびモデル要素が Azure DevOps ソース管理にチェックインするようにします。

### <a name="add-the-model-descriptor-file-to-source-control"></a>ソース コントロールへのモデル記述子ファイルの追加

すべての Visual Studio プロジェクトはモデルに属しています。 モデルは、通常 Visual Studio プロジェクトよりも大きなスコープ内にあるソース コードの配布と配置の単位です。 前のセクションでは、ソース管理にフリート管理ソリューションの要素のファイルを追加しました。 フリート管理モデルの要素をソース管理に追加したのは初めてのため、モデル記述子ファイルをチェックインする必要があります。

1. Visual Studio 内の **チーム エクスプローラー** で,**ソース管理エクスプローラー** を開きます。
2. メタデータ フォルダー (たとえば、**\Trunk\Main\Metadata**) を右クリックし、**フォルダーへの品目の追加** をクリックします。
3. モデル記述子ファイルを選択します。 モデル記述子ファイルは、モデルの XML ファイルのマニフェストです。 これは、モデルが属するパッケージの **記述子** フォルダーにあります。 次の図は、フリート管理モデルのモデル記述子ファイルが存在する場所の例を示しています (c:\\packages\\FleetManagement\\Descriptor\\FleetManagement.xml)。

    > [!NOTE]
    > マシンの構成によっては、モデル ストアが、K:\AosService\PackagesLocalDirectory、c:\AosService\PackagesLocalDirectory、または別のドライブの下にある場合があります。

    [![ソース コントロールへの FleetManagement.xml の追加。](./media/addsourcecontrol_usingdevotools.png)](./media/addsourcecontrol_usingdevotools.png)

4. **完了** をクリックします。

    > [!NOTE]
    > ソリューションに 2 つのモデルの要素が含まれていたため、ソース管理に追加のモデル記述子ファイルを追加する必要があります: K:\\AOSService\\PackagesLocalDirectory\\FleetManagementExtension\\Descriptor\\FleetManagementExtension.xml

5. 保留中の品目をチェックインします。 これで、Azure DevOps の最新のクラウド ベースのソース コントロール システムとその他の多くのアプリケーション ライフ サイクルの機能を使用して、品目のフリート管理アプリケーションの開発をする準備が整いました。

### <a name="experiment-with-source-control"></a>ソース管理を試す

このセクションでは、**FMRental** テーブルにマイナーな変更を加え、変更内容をソース コード リポジトリ内の最新バージョンと比較します。

1. **ソリューション エクスプローラー** で、**移行されたフリート管理 &gt; データ モデル &gt; テーブル &gt; FMRental** を選択します。
2. デザイナーを開けるには、**FMRental** をダブルクリックします。
3. **フィールド** ノードを右クリックし、**新規 &gt; 整数** をクリックします。

    [![新しい整数の追加。](./media/newinteger_usingdevotools.png)](./media/newinteger_usingdevotools.png)

4. **メソッド** を右クリックして、新しいメソッドを追加します。
5. X++ コード エディターで、新たなメソッドにコメントを入力します。
6. 既存メソッドにコメントを入力します。
7. **FMRental** を保存します。
8. **チーム エクスプローラー** で、**FMRental.xml** を右クリックして **最新バージョンと比較** を選択します。

    [![バージョン間の比較。](./media/compareversions_usingdevotools.png)](./media/compareversions_usingdevotools.png)

9. **比較 (差異)** ウィンドウの違いを参照してください。
10. **ソリューション エクスプローラー** で **FMRental** テーブルを右クリックし、**ソース管理 &gt; 元に戻す &gt; 保留中の変更** を選択して変更を元に戻します。

    [![保留中の変更を元に戻す。](./media/undo_usingdevotools.png)](./media/undo_usingdevotools.png)

11. 次のダイアログで取り消しを確認し、**差異** ウィンドウを閉じます。

## <a name="scenario-2-synchronize-models-from-source-control"></a>シナリオ 2: ソース管理からモデルを同期する

このセクションでは、Azure DevOps プロジェクトから既存のモデルおよびモデル要素を同期します。 同期は以下の場合に関連します。1) 以前のバージョンのコードを LCS 経由で移行した。2) 別の開発者が新しいモデルまたは新しいモデル要素をチェックインし、それらを開発環境と同期させたい。

1. ソース管理エクスプローラーで、メタデータを右クリックして **最新バージョンの取得** を選択します。 最新バージョンを取得することにより、ローカル パッケージ フォルダーと最新のコードが同期されます。
2. 別の方法として、**詳細** メニューを使用して固有のビルド バージョンまたは変更セットを同期することができます。

    ![最新バージョンの取得。](./media/getlatest.png)

3. 同期が完了し、新しいモデルを環境に同期させる場合は、Visual Studio からメタデータを更新する必要があります。
4. **Dynamics 365 &gt; モデル管理 &gt; モデルの更新** の順に移動します。

## <a name="organize-todo-tasks-in-a-project"></a>プロジェクト内の TODO タスクの整理

このセクションでは、X++コードに埋め込まれたタスク (TODO コメント) から Visual Studio プロジェクトを作成する方法について説明します。

1. **ソリューション エクスプローラー** で、**移行されたフリート管理 &gt; コード &gt; クラス &gt; FMDataHelper** を選択してから、**FMDataHelper** をダブルクリックします。 X++ コード エディターが開きます。
2. 任意のメソッド内に、TODO コメント (//TODO: my comment) を入力します。

    [![TODO コメントの例。](./media/code_usingdevotools.png)](./media/code_usingdevotools.png)

3. 他のフリート管理のクラスやテーブルを開き、さらに TODO コメントを追加します。
4. **FleetManagement Migrated** プロジェクトをリビルドします。
5. **表示 &gt; タスク一覧** を選択し、Visual Studio **タスク一覧** ウィンドウを開きます。

    [![タスク一覧を開く。](./media/tasklist_usingdevotools.png)](./media/tasklist_usingdevotools.png)

6. ドロップダウン リストから **コメント** を選択します。

    [![コメントの表示。](./media/tasklistcomments_usingdevotools.png)](./media/tasklistcomments_usingdevotools.png)

7. すべての作業項目を選択して右クリックし、**新しいプロジェクトに追加** を選択します。

    [![TODO コメントの選択。](./media/addnewproject_usingdevotools.png)](./media/addnewproject_usingdevotools.png)

8. 品目を追加することにより、**新規プロジェクト** ダイアログが開き、すべての TODO を含む新しいプロジェクトを作成できます。
9. このプロジェクトを作業プロジェクトとして保存し、TODO リストを管理することができます。
10. 完了したら、**チーム エクスプ ローラー** ですべての保留中の変更を元に戻します。

    [![すべての変更を元に戻す。](./media/undoall_usingdevotools.png)](./media/undoall_usingdevotools.png)

11. FleetManagement ソリューションを閉じるには、**ファイル &gt; ソリューションを閉じる** をクリックします。

## <a name="use-metadata-search-and-navigation-tools-to-find-elements-and-create-projects"></a>メタデータ検索とナビゲーション ツールを使用して要素を検索し、プロジェクトを作成する

このセクションでは、アプリケーション全体でメタデータ ベースの検索を実行する方法を示します。

### <a name="use-the-metadata-search-window"></a>[メタデータ検索] ウィンドウの使用

1. **Dynamics 365 &gt; メタデータの検索** とクリックします。
2. **メタデータ検索** ウィンドウの **検索** フィールドに、次のテキストを入力して会社間クエリを含むアプリケーション スイート モデルのすべてのテーブル挿入メソッドを検索します。 `type:table,method name:insert code:"crosscompany" model:"Application Suite"`。
3. 検索が完了するまで待ちます。 これにはしばらく時間がかかる場合があります。

   ![メタデータの検索結果。](./media/metadatasearchresults_usingdevotools.png)

4. リスト内の結果をダブルクリックします。 コード エディターが開き、検索条件に一致する行にカーソルを移動します。
5. Ctrl キーを押しながら複数選択することで結果リストで複数の要素を選択し、右クリックして **新しいプロジェクトに追加** を選択します。 要素を追加することにより、選択した要素を含む新しいソリューションとプロジェクトを作成できます。

### <a name="try-other-search-examples"></a>他の検索例を試す

検索結果を操作する前に、検索が完了するのを待つ必要はありません。 いつでも結果をダブルクリックして、検索条件に一致するメタデータまたはソース コードを表示することができます。 推奨される検索例を次に示します。

- モデル アプリケーション スイートの表示モードおよび自動幅モードで定義された、垂直タブのコントロールを検索します。 

    `type:form,formtabcontrol property:arrangeMethod=Vertical,ViewEditMode=view,WidthMode=Auto model:"Application Suite"`

- プロパティ heightmode = 列で、編集できないフォームですべてのグリッド コントロールを検索します。

    `type:form,formgridcontrol:allowedit=no,heightmode=column`

- アプリケーション スイート モデル内のすべての SimpleListDetail フォームを検索します。

    `type:formdesign property:style=simplelistdetail model:"Application Suite"`

- キーワード xpNum を含むインデックス フィールド名を持つすべてのテーブルを検索します。

    `type:table,tableindexfield anem: xpNum*`

- 以前の検索条件にアクセスするには、検索バーのドロップダウン メニューを使用します。

    [![ドロップダウン メニューの使用。](./media/accessprevious_usingdevotools.png)](./media/accessprevious_usingdevotools.png)

## <a name="navigate-to-related-elements"></a>関連する要素への移動

このセクションでは、**アプリケーション エクスプローラー** または **ソリューション エクスプローラー** で関連要素を見つけることなく、ある要素から関連要素に移動する機能を紹介します。

1. **アプリケーション エクスプローラー** を開き、**モデル ビュー** に切り替えます。

    [![モデル ビューでアプリケーション エクスプローラーを開く。](./media/modelview_usingdevotool1.png)](./media/modelview_usingdevotool1.png)

2. **フリート管理** モデルで、**ユーザー インターフェイス&gt;メニュー項目&gt;メニュー項目を表示&gt;FMCustomer** をクリックします。

    [![アプリケーション エクスプローラーで FMCustomer を選択する。](./media/fmcustomerisv_usingdevotools.png)](./media/fmcustomerisv_usingdevotools.png)

3. **FMCustomer** を右クリックし、**デザイナーを開く** を選択します。
4. **FMCustomer** メニュー項目デザイナーでルート ノードを右クリックし、**フォーム FMCustomer に移動する** を選択します。

    [![アプリケーション エクスプローラーを使用したフォームへの移動。](./media/goformfmcustomer_usingdevotools.png)](./media/goformfmcustomer_usingdevotools.png)

    **FMCustomer** フォーム デザイナーが開きます。

5. **FMCustomer** フォームのデザイナーで、**データ ソース** を展開して、**FMCustomer** を右クリックしてから **テーブル FMCustomer へ移動** を選択します。

    [![アプリケーション エクスプローラーを使用したテーブルへの移動。](./media/gotablefmcustomer_usingdevotools.png)](./media/gotablefmcustomer_usingdevotools.png)

    **FMCustomer** テーブル デザイナーが開きます。

6. 同じ方法を使用すると、テーブル フィールドが参照する EDT 要素に移動できます。 **ヒント**: コンテキスト メニューを開くのではなく F9 キーを押します。 F9 キーを押すと、参照要素のデザイナーが開きます。 **ヒント**: 現在のプロジェクトに要素を追加するには、ドキュメント タブを右クリックし、**プロジェクトへの追加** を選択します。

    ![プロジェクトへの追加を使用する。](./media/addtoproject_usingdevotools.png)

## <a name="use-application-explorer-to-create-a-project-from-a-model"></a>アプリケーション エクスプローラーを使用してモデルからプロジェクトを作成

アプリケーション エクスプ ローラーを使用して、モデルのすべてまたは一部の要素を検索し、検索結果からプロジェクトを作成することができます。

1. 要素のタイプでプロジェクトを整理するためのオプションがオンになっていることを確認します。 **Dynamics 365** \> **オプション** \> **プロジェクト** の順に移動します。
2. アプリケーション エクスプローラーに移動し、目的のモデル内の要素を検索します。 たとえば、*モデル: "フリート管理"* を入力し、**入力** をクリックします。

    [![アプリケーション エクスプローラーでモデルを検索する。](./media/appexplorermodelsearch.jpg)](./media/appexplorermodelsearch.jpg)

3. 検索が完了したら、AOT ルート ノードを右クリックし、**新しいプロジェクトへの検索結果の追加** を選択します。

    [![新しいモデルに品目を追加する。](./media/addsearchresultstonewproject.jpg)](./media/addsearchresultstonewproject.jpg)

4. 新しいプロジェクト ダイアログ ボックスでプロジェクトのプロパティを指定し、**OK** をクリックしてプロジェクトを作成します。

    > [!TIP]
    > 検索結果からプロジェクトを作成するには、すべての結果が同じモデル内にある限り、任意のタイプ、名前、またはその他のフィルタを検索に追加できます。 例: *モデル:「フリート管理」 タイプ:テーブル名:^FM* は、文字 FM で始まる名前を持つフリート管理モデルで、すべてのテーブルを返します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
