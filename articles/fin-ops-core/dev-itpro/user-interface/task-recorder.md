---
title: タスク レコーダー リソース
description: この記事では、タスク レコーダーを使用して、業務プロセスを記録する方法について説明します。
author: jasongre
ms.date: 09/11/2020
ms.topic: article
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.search.form: SysTaskRecorderPane
ms.openlocfilehash: 07c43d2cd8aa3796a3730997b4b2976ee9cefb47
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292422"
---
# <a name="task-recorder-resources"></a>タスク レコーダー リソース

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

この記事では、タスク レコーダーを使用して、業務プロセスを記録する方法について説明します。

## <a name="overview"></a>概要

### <a name="task-recorder"></a>タスク レコーダー

財務と運用アプリのタスク レコーダーは、ユーザーが複数の異なるユース ケースの業務プロセスを記録できるユーティリティです。 次にいくつか例を挙げます。 
- アプリケーション自体に含まれる特定の業務プロセスのステップ バイ ステップ ガイド付きツアー 
- オプションでスクリーンショットを含めることができる Microsoft Word ドキュメントとしての業務プロセスのドキュメント
- 業務プロセスの回帰テスト
- アプリケーションでの業務プロセスの自動再生

財務と運用アプリのタスク レコーダーは、高い応答性、フレキシブルなアプリケーション プログラミング インターフェイス (API)、および業務プロセス記録の消費者とのシームレスな統合を備えています。 また、タスク レコーダーは、Microsoft Dynamics Lifecycle Services (LCS) の [ビジネス プロセス モデラー (BPM)](https://bpm.lcs.dynamics.com) ツールとも統合されているため、ユーザーは引き続き記録を整理ができます。 ただし、ユーザーは、記録から業務プロセス ダイアグラムを生成できなくなりました。

タスク レコーダーでは、業務プロセスの記録からアプリケーションの回帰テストを自動的に生成し、既に記録されたプロセスを再生することができます。 これらの新機能には、ユーザーがタスク レコーダーを最大限に活用できるテスト固有のジェスチャも含まれます。

### <a name="architecture"></a>アーキテクチャ

各コントロールが計測され、ユーザー アクションの実行についてタスク レコーダーに通知されるため、タスク レコーダーは、正確な再現性でクライアントでのユーザー アクションを記録できます。 コントロールは、イベントが発生したことをタスク レコーダーに通知し、対応するユーザー アクションに関するすべての関連情報をリアルタイムで渡します。 タスク レコーダーは、この情報からユーザー アクションのタイプ (たとえば、ボタンのクリック、値の入力、またはナビゲーション) と、ユーザー アクションに関連するデータ (たとえば、入力データの値とタイプ、フォーム コンテキスト、またはレコード コンテキスト) を取得できます。 タスク レコーダーは、記録されたアクションをユーザーが実行したとおりに記録の再生で実行できるように、十分な詳細情報を保持します。

### <a name="basic-configuration"></a>基本コンフィギュレーション

タスク レコーダーはすべての財務と運用アプリに含まれており、ユーザーが初めてクライアントを開いた直後に業務プロセスの記録を開始できます。

> [!IMPORTANT]
> **タスク ガイド** タブは、現在のところ、コマースおよび人事管理では使用できません。 将来のリリースではこの機能を有効にするよう、作業が進行中です。 人事管理でのはじめにの経験タスク ガイドは、基本的機能をカバーするために引き続き使用可能です。 Commerce および Human Resources の両方に関する[財務と運用アプリケーション ドキュメント](../../fin-ops/index.md)で手順を追ったヘルプも利用できます。

## <a name="start-a-new-recording"></a>新しい記録を開始する
次のステップでは、タスク レコーダーを使用して新しい記録を開始する方法を示します。

1.  製品を開いて、サインインします。 毎回新しく記録する前に、ブラウザーを更新することをお勧めします。 更新すると、新しいユーザー セッションが作成され、タスク レコーダーが再起動します。 したがって、最も安定したレコーディング エクスペリエンスが提供されます。
2.  記録中に使用する会社を選択します。 タスク レコーダーを初めて使用する場合は、このチュートリアルでフリート管理の業務プロセスに基づいてサンプル レコードを作成して、この手順を進めることができます。 以下に従って、フリート デモ データを読み込む必要があります。
    1.  **ダッシュ ボード &gt; フリート管理 &gt; フリート設定** の順に移動します。
    2.  **デモ データの読み込み** をクリックします。
    3.  データが読み込みを完了したら、**閉じる** をクリックします。
    4.  ナビゲーション バーの製品名をクリックして **ダッシュ ボード** に戻ります。

3.  **設定 &gt; タスク レコーダー** に移動します。
    
4.  **タスク レコーダー** ウィンドウが開きます。 右上隅の **閉じる** ボタン (**X**) をクリックして **タスク レコーダー** ウィンドウを閉じてから、新しい記録を開始します。 前のステップに従って、ウィンドウを再度開くことができます。
        
5.  **記録の作成** をクリックします。
6.  記録名を入力し、**開始** をクリックします。 記録は、**開始** がクリックされると開始されます。 このチュートリアルのフリート例については、名前「新しいレンタル予約の作成」を使用します。

    記録中に右上隅にある **終了** ボタン (**X**) をクリックすると、記録を停止せずに **タスク レコーダー** ウィンドウを非表示にできます。 ページ上部に表示される **タスク レコーダー** ボタンをクリックして、ウィンドウを再度開くことができます。 このボタンは、記録中にのみ表示されます。 

    > [!NOTE]
    > **[保存されているビュー](../../fin-ops/get-started/saved-views.md)** 機能が有効になっている場合、公開済みのビューまたは標準ビューのいずれかを使用して記録を作成し、記録がユーザーにとって確実に機能するようにします。 

7.  タスク レコーダーが **記録モード** になります。 このウィンドウには、記録プロセスに関連する情報とコントロールが表示されます。

これで、タスク レコーダーを使用して業務プロセスを記録する準備が整いました。 初回のユーザーとしてこのガイドに従っている場合は、次のようなフリート管理のシナリオを例として完成させることができます。 それ以外の場合、独自のアプリケーション シナリオを記録することができます。

### <a name="record-a-fleet-management-scenario"></a>フリート管理シナリオの記録
1.  **タスク レコーダー** ウィンドウで、**サブ タスクの開始** をクリックします。
2.  **名前** を [新しい顧客でレンタルの作成] に設定します。 **コメント** フィールドは空白のままにします。
3.  **OK** をクリックします。 タスクはステップ リストに追加されます。 
5.  **ダッシュ ボード &gt; フリート管理 &gt; 予約管理** の順に移動します。
6.  **集計** タブで **すべての顧客** に移動します。
7.  アクション ウィンドウで、**新規** をクリックします。
8.  顧客の名と姓を入力します。
9.  **保存** をクリックします。
10. **タスク レコーダー** ウィンドウで、**サブ タスクの終了** をクリックします。 
11. ブラウザーの戻るボタンを 2 回クリックして **引当管理** ワークスペースに戻ります。
12. **タスク レコーダー** ウィンドウで、**サブ タスクの開始** をクリックします。 タスクに 「新規顧客に車両をレンタル」 と名前を付けます。 **OK** をクリックします。
13. **集計** の下の (**+**) **レンタル** をクリックします。
14. **情報** で、車両として "1975 Litware McKinley" を選択します。
15. **情報** で、いま作成した顧客を設定します。
16. **割引** セクションを展開します。
17. **割引** の下にある **追加** をクリックし、顧客割引の頻度を追加します。 **OK** をクリックします。
18. アクション ウィンドウで **レンタル開始** をクリックします。
19. 返却日を将来の日付に設定します。
20. **OK** をクリックします。
21. **タスク レコーダー** ウィンドウで、**サブ タスクの終了** をクリックします。
22. ページ最上部にある **停止** をクリックします。

## <a name="recording-a-business-process"></a>業務プロセスの記録
記録を開始すると、Web クライアントを使用して通常実行するのと同様の方法で業務プロセスを実行できます。 製品を操作すると、新しいステップが **タスク レコーダー** ウィンドウのステップ リストに追加されます。 このセクションでは、タスク レコーダーの機能を最大限に活用するために、業務プロセスの記録中に実行できる他のアクションについて説明します。 

### <a name="stop"></a>停止

**停止** は記録セッションを終了するのに使用します。 この操作は元に戻せないため、**停止** をクリックする前に、記録が完了していることを確認します。 **停止** をクリックすると、ダウンロード オプション画面に移動します。

[![コントロールの停止。](./media/taskrecorderguide-taskrecordertoolbarstop.png)](./media/taskrecorderguide-taskrecordertoolbarstop.png)

### <a name="startend-sub-task"></a>サブ タスクの開始/終了

**サブ タスクの開始/終了** により、ユーザーは、記録のグループ化された一連のステップの開始および終了を指定できます。 **サブ タスクの開始** ボタンをクリックして、記録されたステップの現在のリストの最後に 「サブ タスク」 ステップを追加します。 サブ タスクには、この時点から **サブ タスクの終了** ボタンをクリックするまで実行するすべてのステップが含まれます。 **サブ タスクの終了** ボタンをクリックすると、「サブ タスクの終了」 ステップも記録されたステップ リストに追加されます。

> [!NOTE]
> タスクに追加するステップを実行/記録する前に、サブ タスクを開始する必要があります。 次に、タスクに含めるステップのすべてを実行/記録した後、サブ タスクを終了する必要があります。

サブ タスクは純粋に組織のツールであり、業務プロセスの記録の消費者は、作業グループを有用な方法で解釈できます。 タスクはその他のタスク内で入れ子にすることができるため、非常に長く複雑な業務プロセスを柔軟に整理できます。 

### <a name="deleterestore-step"></a>削除/復元ステップ

**削除/復元ステップ** により、ユーザーは記録から手順を削除したり、記録からの手順の削除を元に戻したりすることができます。 まずステップ リストからステップを選択し、その後 **削除/復元ステップ** ボタンをクリックしてください。

> [!NOTE]
> 記録を再生すると、**削除** ボタンの動作が変わります。 再生モードでは、削除されたステップを実行するポイントを再生が過ぎると、削除されたステップを元に戻すことはできません。 たとえば、3 つのステップを含む記録を読み込み、再生を開始する前にステップ 2 を削除します。 再生がステップ 3 を実行していない場合に限り、ステップ 2 を復元できます。 再生を開始し、再生がステップ 2 を「スキップ」 (削除したため) し、ステップ 3 を実行した後、ステップ 2 を復元することはできません。 ステップ 2 が実行されておらず、記録されていないため、前の位置の記録に遡って追加することはできません。 


### <a name="add-developer-placeholder"></a>開発者プレースホルダーの追加

**開発者プレースホルダーの追加** により、ユーザーは記録されたステップ リストにプレースホルダー ステップを追加できます。 このプレースホルダーのステップは、タスク ガイドを表示したときには表示されません。また、記録のメンテナンス中に実行されることもありません。 この機能は、[Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md)、またはタスク記録から X++ テストを作成できるようにする X++ コードジェネレーターでのみ使用されます。 コードジェネレーターで X++ テストが作成されると、生成されたコードにメソッド スタブが自動的に追加されます。 開発者は、このメソッド スタブに X++ コードを追加できます。 自動化コードは、このプレースホルダーが追加された記録のポイントで生成されたテストが実行されると、検証を呼び出します。

## <a name="enriching-steps-in-a-recording"></a>記録のステップの拡充

記録のステップを拡充するためのさまざまなオプションがあります。 たとえば、ステップに関連付けられているテキストを調整し、特定のステップに関する情報を追加できます。 このセクションでは、利用可能なステップ拡充機能について説明します。 これらのオプションにアクセスするには、記録の特定のステップで **ステップの編集** ボタンをクリックします。 

### <a name="step-instruction"></a>ステップの指示

**ステップ命令** は、タスク ガイドのこの手順に表示される主要テキストです。 通常、ステップの指示には 2 ～ 3 つの代替オプションがあり、コメントを編集するときには次の順序で表示されます。

[![この画像は、ステップの指示を変更するための注釈オプションを示しています。](./media/taskrecorderguide-annotationlabels.png)](./media/taskrecorderguide-annotationlabels.png) 

このイメージは、手順を変更するための注釈オプションを示しています。
- **優先値指示** このタイプの指示は、ステップが記録されたときに使用されたものと同じデータを入力するようにユーザに指示します。 *例*: 名フィールドに「John」を入力します。
- **サンプル値ラベル** このタイプの指示は、ステップを記録したときに使用されたデータが *サンプル* データのみであったことを示す、独自のデータの入力をユーザーに指示します。 *例*: 名フィールドに値を入力します。

   記録をタスク ガイドとして再生するときに、このステップで **詳細情報** ボタンをクリックすると、ステップが記録されたときに使用されたデータを表示できます。 この記録されたデータ値は、*例* データ値としてラベル付けされます。 
   > [!NOTE]
   > ボタンをクリックする、フォームを開く、ルックアップからレコードを選択するなどの、フィールドに関連しない手順では、注記するときに *サンプル値ラベル* をオプションとして設定しません。
   
- **ユーザーが指定した値のラベル** このステップ指示には、作成者が独自のテキストで記入できるプレースホルダー テキストが含まれています。 **サンプル値ラベル** オプションのある手順については、プレースホルダーが通常入力するデータを指定するテキストを置き換えます。 これは、**優先値ラベル** も **サンプル値ラベル** も、このステップで使用する必要のあるデータを十分に表現できないシナリオに役立ちます。
  -   *ラベル例*: 名前フィールドに *{テキストの例}* を入力します。
  -   *プレースホルダー表示後のラベル例*: 名前フィールドで、顧客名を入力します。

  **サンプル値ラベル** オプションのない手順では、プレースホルダーがすべてのラベル テキストを置き換えることができます。 たとえば、ボタンに関連付けられている手順には **サンプル値ラベル** がないため、独自のテキストでラベル テキスト全体を置換する可能性があります。
  -   *交換前のラベル例*: 転記をクリックします。
  -   *交換した後のラベル例*: 注文を転記するには、転記をクリックします。

### <a name="titles-and-notes"></a>タイトルとメモ

タイトルとメモは、ユーザー指定のテキストをタスク ガイドのステップに関連付けるための場所を提供します。
- **タイトル** – このタイトルにより、タスク ガイドのこのステップのステップの指示の上に表示されるテキストを指定できます。 タイトルは、ステップの指示で示されるアクションを完了する前にユーザーに読んでほしいテキストを配置するのに適しています。
- **注記** – 注記を使用して、タスク ガイドでこのステップの展開可能なポップ アップ セクションに表示されるテキストを指定できます。 注記は、オプションの参考資料またはユーザーにとって有益なその他の情報を配置するのに適していますが、ステップの指示で示されるアクションを完了するために読む必要はありません。

### <a name="change-recorded-values"></a>記録された値の変更

バージョン 10.0.12 では、基本的な入力コントロール (たとえば、単純なテキスト、数値、日付、および 候補リストの各フィールド) に記録される値を調整して、手順を再記録することはできません。 検索コントロールと参照グループは現在サポートされていないことに注意してください。  

### <a name="hide-from-task-guide"></a>タスク ガイドから非表示にします。

**このステップを非表示** オプションを使用すると、作成者は特定のステップをタスク ガイドに表示しないようにすることができます。 このオプションは、タスクの記録を再生モードで実行するために必要だが、ユーザーには表示されないステップを非表示にする場合に役立ちます。 これらのステップの例には、コピー ステップ、システム生成ステップ、データ クリーンアップ ステップなどが含まれます。 サブ タスクを非表示にすると、そのサブ タスク内に記録されているステップもすべて非表示になります。

## <a name="using-control-gestures"></a>コントロール ジェスチャの使用

基本的な記録機能を使用すると、プロセスにオーバーヘッドを追加することなく、タスク レコーダーを使用してエンド ツー エンドの業務プロセスを記録できます。 状況によっては、より高度な記録機能を使用して、さらに豊富な業務プロセスの記録を作成できます。 次の各ジェスチャは、コントロールのショートカット メニュー (右クリック メニューまたはコンテキスト メニューとも呼ばれます) の **タスク レコーダー** オプションの下にあり、ステップを記録に追加します。 ジェスチャがコントロールでサポートされていない場合、そのコントロールのショートカット メニューには表示されません。

### <a name="copy"></a>コピー

**コピー** ジェスチャを使用すると、現在のコントロールの値をタスク レコーダーの 「クリップボード」 にコピーできます。 その値は、後で **貼り付け** または **検証** ジェスチャの一部として使用できます。 複数のコントロールからの値を貼り付ける必要があるため、タスク レコーダーの 「クリップボード」 には、記録にコピーされたすべてのコントロール値の一覧を保持します。

### <a name="paste"></a>貼り付け

**貼り付け** ジェスチャを使用すると、同じ記録内の前の **コピー** ジェスチャから値を貼り付けることができます。 タスク レコーダー 貼り付け機能は、ユーザーが使い慣れた標準の貼り付け機能と同じように動作し、記録時に使用するとさらにメリットがあります。 タスク レコーダーは、再生中に記録された **コピー** と **貼り付け** コマンドを再生するため、コピーされたコントロールの値が記録中の値と異なる場合、コピーされたコントロールの記録中の値ではなく、現在の値をタスク レコーダーは貼り付けます。 この機能は、コピーされたコントロールに環境間で変更できる値 (例えば、recID値または数値シーケンス) があるシナリオで役立ちます。

テスト コードが生成されるときに、**コピー** と **貼り付け** を使用すると、さらに便利です。 **貼り付け** コマンドを使用して値が設定されるコントロールについては、タスク レコーダーは、他のコントロールの値に基づいて設定されるため、そのコントロールの値に対するパラメーター化された入力変数を作成する必要はありません。 この機能は、顧客などのエンティティが作成され、そのエンティティの識別子が記録中に頻繁に入力されるシナリオで非常に便利です。 シナリオ全体で手動で顧客名または ID を再入力して、タスク レコーダーに各エントリのパラメーター化された入力変数を生成させるのではなく、ユーザーは顧客名または ID を一度コピーして、繰り返し貼り付けることができます。 この場合、タスク レコーダーは、顧客名または ID を表すために、単一のパラメーター化された入力変数を生成します。 この機能により、生成されたテストの入力データをより簡単に変更できます。

###  <a name="validate"></a>検証

**検証** ジェスチャを使用すると、ターゲット コントロールの値を検証するステップを挿入できます。 このジェスチャは、常に等式を用いて、コントロールの値を検証します。 *現在、記録の再生中には検証は実行しません。* 代わりに、生成されたテスト コードが実行されたときにのみ実行されます。 利用できる検証は 2 種類あります。

-   **現在の値の検証** は、記録時にターゲット コントロールの値をキャプチャし、それを使用してテスト コードでアサーションを生成します。 ショートカット メニューの検証オプションの一覧では、**現在の値** が常に先頭に来ます。
-   **参照値の検証** は、テスト コードでアサーションを生成するときに、以前にコピーしたコントロールの値を使用します。 これにより、値がテスト コードにハードコードされていないため、データの変更に対して弾力性のあるアサーションを作成できます。 ショートカット メニューの検証オプションの一覧で、**参照値の検証** は \[コピーしたコントロールの AOT 名: 現在のコピーされた値\] に従います。

追加のオプションはバージョン 10.0.13 またはそれ以降で使用できます。 次にいくつか例を挙げます。

- **有効**/**無効** では、対象となるコントロールの状態が有効 (または無効) になったことが検証され、その検証ステップを使用してテスト コードにアサーションが生成されます。
- **読み取り専用**/**編集可能** では、対象となるコントロールの状態が読み取り専用 (または編集可能) になったことが検証され、その検証ステップを使用してテスト コードにアサーションが生成されます。

### <a name="add-info-step"></a>参考ステップの追加

**情報ステップの追加** ジェスチャを使用すると、ステップを挿入して、テキストを入力できます。 この機能は、主にタスク ガイドの作成に役立ちます。 **情報ステップ** はステップの指示テキストがユーザー指定のタスク ガイド ステップです。 情報ステップは、シナリオの一部であるアクションを説明するのに役立ちますが、クライアントの外部で発生する必要があります。 たとえば、あるシナリオでは、ユーザーが品目在庫を検索したり、電子メールで情報を確認したりする必要があります。

ユーザーは、タスク ガイドに情報ステップが表示される場所を指定できます。 情報ステップは、ステップがコントロールに関連付けられている場合、ページ上のコントロールをポイントできます。 または、ステップがクライアントの外部にある、またはページ全体に適用される説明である場合は、情報ステップはページの右上に表示できます。

> [!NOTE]
> 情報ステップは手動で指定されたステップで、ユーザーがコントロールに対してアクションを取ったときにタスク レコーダーによって自動的に記録されないため、情報ステップにはユーザーがタスク ガイドでステップを完了したときに、自動的に処理する機能はありません。 情報ステップはクライアントでアクションを実行することに関連付けられていないため、タスク ガイドがユーザーが完了したことを検出して自動的に次のステップに進むためのアクションはありません。

## <a name="options-after-a-recording-is-completed"></a>記録完了後のオプション
**停止** をクリックして記録セッションを終了すると、いくつかのオプションが、完了した記録に関連するファイルを保存するために表示されます。 **この PC に保存** をクリックし、タスク記録パッケージをデスクトップに保存します。 このファイルは後で使用します。

[![記録が終了した後に、記録をダウンロードまたは保存するためのオプション。](./media/taskrecorderguide-taskrecorderdownloadoptions.png)](./media/taskrecorderguide-taskrecorderdownloadoptions.png)

### <a name="save-to-this-pc"></a>この PC に保存

記録を完了した後の 1 つのオプションは、タスクの記録パッケージ (.axtr ファイル) をコンピュータにダウンロードすることです。 このファイルは後で **タスク レコーダー** ウィンドウから読み込んで、記録をタスク ガイドとして再生したり編集したりできます。

### <a name="save-to-lifecycle-services-lcs"></a>Lifecycle Services (LCS) に保存 

LCS ライブラリに記録を保存すると、BPM ライブラリの指定された業務プロセスで公開されます。 選択されている LCS ライブラリがヘルプ ライブラリとして設定されている場合、**ヘルプ** メニューを検索することにより、この記録に関するタスク ガイドを検索することができます。 

> [!NOTE]
> LCS ライブラリに記録を保存できるようにするには、ユーザーは環境を配置した Azure Active Directory (Azure AD) テナントにいる必要があります。  

### <a name="export-as-word-document"></a>Word ドキュメントとしてエクスポート

記録の Microsoft Word 文書には、記録されたステップとキャプチャされたすべてのスクリーンショットが含まれます。

### <a name="save-as-developer-recording"></a>開発者の記録として保存

未加工の記録ファイル (開発者用の記録) は、テスト コードの生成や [RSAT](../perf-test/rsat/rsat-overview.md) が使用されているシナリオなどの開発に役立ちます。

## <a name="playing-back-a-recording"></a>記録の再生 
タスク レコーダーの **再生** 機能は、最初に記録されたページと値を使用して、既存の記録のステップを自動的に実行できます。 再生モードは、基になるアプリケーションに変更が加えられ、その変更によってシナリオに必要な業務プロセス ステップが変更された場合に、既存の記録を更新するために使用できます。 このモードでは、タスク レコーダーがステップを同時に再記録して再生することに注意してください。 再生が完了すると、既存の記録から実行されたステップと、ユーザーが手動で実行した新しいステップの両方を反映する新しい記録が生成されます。 ユーザーまたはタスク レコーダーによって自動的に実行されないステップは、この新しい記録には含まれません。 

既存の記録を再生するには、次のステップを実行します。
1. ブラウザー タブを更新します。 
    > [!NOTE]
    > 毎回新しく記録する前に、ブラウザーを更新することをお勧めします。
    
2. **タスク レコーダー** ウィンドウを開きます。
3. **記録の再生** をクリックします。
4. **この PC から開く** をクリックすると、以前にダウンロードしたタスク レコーダ パッケージ (.axtr ファイル) から記録を読み込むことができます。
   -   このガイドを初めて読む場合、以前ダウンロードした「新しいレンタル予約を作成する」を選択します。

5. **開始** をクリックします。

記録を再生すると、追加のアクションが **タスク レコーダー** ウィンドウで使用できます。
### <a name="play-next-pending-step"></a>次の保留中のステップの再生 

**次の保留中のステップの再生** は、記録の次のステップを実行します。 このアクションは、1 つのステップの効果を分析するときに、再生速度をより詳細に制御できるので便利です。 このアクションには、注意が必要な副作用があります。 **次の保留中のステップの再生** をクリックすると、開いているルックアップ、ドロップダウン ダイアログ ボックス、またはアクション ウィンドウ タブは、このアクションがこれらの要素からフォーカスを移動するため、閉じる場合があります。 このような状況のため、代わりに **保留中のすべてのステップの再生** を使用することをお勧めします。

### <a name="play-all-pending-steps"></a>保留中のすべてのステップの再生

**保留中のすべてのステップの再生** は、記録内の残りのステップの順次実行を開始し、再生が一時停止されるか、すべてのステップが実行されるまで継続します。 再生中、**保留中のすべてのステップの再生** ボタンは、再生を一時停止するために使用できる **一時停止** ボタンになります。 再生が何らかの理由 (例えば、名前が変更されたボタンが見つからないなど) で、ステップを正常に実行できない場合、タスク レコーダーはそのステップをスキップし、再生は自動的に一時停止されます。 このようにして、クライアントで新しいステップを完了することで、ユーザーは、古いステップを置き換えることができます。 タスク レコーダーは、新しい手順を記録し、スキップされたステップを無視します。 ユーザーは **保留中のすべてのステップの再生** をクリックして、残りのステップの再生を継続できます。 記録が完了した後、ユーザーは更新された記録をダウンロードできます。 この記録には、元の記録のすべてのステップが含まれますが、スキップされたステップは除外され、新しいステップが含まれます。

### <a name="play-to-selected-step"></a>選択したステップまで再生

**選択したステップまで再生** は、**保留中のすべてのステップの再生** のように動作しますが、すべてのステップではなく、ステップのサブセットのみを再生できます。 リストで、再生を停止するステップを選択し、**選択したステップまで再生** をクリックします。 タスク レコーダーはリスト内のステップの実行を開始し、選択したステップを実行すると停止します。

## <a name="editing-a-recording"></a>記録の編集
再生機能を使用して記録を編集できますが、記録全体を再生せずに、記録を簡単に編集できるモードもあります。 この機能にアクセスするには、**タスク レコーダー** ウィンドウを開いた後、**記録の編集** をクリックします。 この機能を使用して、次の編集を行うことができます:
- ファイル全体を再記録することなく、記録にステップを挿入します。
- ファイル全体を再記録せずにサブ タスクの下にステップを移動します。
- 記録の名前と説明を調整します。

### <a name="insert-steps-without-re-recording-the-entire-file"></a>ファイル全体を再記録せずにステップを挿入する

ファイル全体を再生または再記録せずに、タスク記録の任意の場所にステップを追加できます。

1.  新しいステップを挿入する後のステップを選択します。 ステップが強調表示されているかを確認します。
 
    タスク レコーダーがステップを挿入するには、正しいページを開いておく必要があります。 新しいステップが発生するページが正しいページです。 タスク レコーダーには、アクティブなページが何であるかを判断するメカニズムがあり、正しいページが開かれていない場合は、機能が無効になります。 

    [![ステップ機能を挿入。](./media/taskguide1.png)](./media/taskguide1.png)

    正しいページを開いている場合は、**ステップの挿入** が利用可能になります。

    [![適切なページに使用可能なステップを挿入する。](./media/taskguide2-231x300.png)](./media/taskguide2.png)

2.  **ステップの挿入** をクリックします。

    **ステップの挿入** をクリックすると、タスク レコーダーが記録モードに切り替わります。 ユーザー インターフェイス (UI) で実行されたアクションは記録され、ステップとして記録に挿入されます。
    
3.  **停止** をクリックします。

    記録モードが停止し、、記録の編集を続行できます。 たとえば、このプロセスを繰り返して、記録の別の場所にステップを挿入したり、次のセクションで説明されているようにサブ タスクを移動したりできます。

4.  タスク記録の編集が完了したら、**編集の完了** をクリックし、記録の保存または公開オプションの 1 つを選択します。

### <a name="move-steps-under-a-sub-task-without-re-recording-the-entire-file"></a>全体のファイルを再記録せずにサブタスクでのステップの移動

ファイル全体を再生または再記録せずにサブタスクでステップを移動できます。 既存のステップをグループ化する場合は、サブタスク ステップまたはエンド サブタスク ステップを移動することもできます。

1.  移動するステップまたはサブタスク ステップを選択します。 ステップが強調表示されていることを確認します。

2.  **ステップを後に移動** をクリックします。 このコマンドにアクセスするには、省略符号 (**...**) ボタンを選択する必要がある場合があります。

    [![ステップを後に移動の例。](./media/taskguide3.png)](./media/taskguide3.png)

3.  ステップまたはサブタスク ステップを移動した後に移動するステップまたはサブタスク ステップを選択します。 タスク レコーダーはステップを移動します。

4.  サブ タスクの終了ステップを移動するには、それを選択し、**ステップを後に移動** をクリックしてから、サブ タスクの終了ステップの後に配置するステップを選択します。

    タスク ガイドの 1 番目のステップをサブタスク内に配置する場合は、サブタスクのステップを 2 番目のステップとして作成し、それに 1 番目のステップを移動します。 必要な数のステップまたはサブタスクを追加、または移動できます。

5.  タスク記録の編集が完了したら、**編集の完了** をクリックし、記録の保存または公開オプションの 1 つを選択します。

### <a name="adjust-the-recording-name-and-description"></a>記録の名前と説明の調整

**記録の名前** と **記録の説明** フィールドの値を調整できます。 さらにステップをタスク レコーダー編集ウィンドウに表示する場合は、記録の名前と説明を表示するセクションを折りたたむこともできます。

[![記録の名前と説明の展開と折りたたみ。](./media/taskguide4-300x252.png)](./media/taskguide4.png)

## <a name="playing-a-task-guide"></a>タスク ガイドの再生

**タスク ガイド** はユーザー向けのエクスペリエンスであり、ユーザーは、タスク記録を使用してビジネス シナリオを完了させるための一連のガイド付きステップ バイ ステップ手順を使用することができます。 ユーザーは、ページ全体を移動し、ユーザーが操作する必要がある UI 要素をポイントするアニメーション化されたポップアップ プロンプトを通じて各ステップを完了するよう指示されます。 プロンプトでは、要素の操作方法もユーザーに知らせます。 たとえば、「ここをクリック」 や 「このフィールドにデータを入力する」 と表示されます。 ユーザーが完了するように指示される各ステップは、タスク記録に最初に記録されたステップに基づいています。 タスク記録ファイルには、最初に記録されたステップを説明するデータが含まれているため、タスク ガイドはユーザーが期待どおりにステップを完了したことを自動的に判断できます。 その後、自動的に次のステップに進みます。 

> [!NOTE]
> ユーザーがステップを完了したとタスク ガイドが判断する 1 つの方法は、フィールドの値がいつ変更されたかを検出することです。 タスク ガイドでは特定の値を設定する必要はありませんが、ステップが完了したことを確認するために、フィールド値を変更する必要があります。 ユーザーはフィールド値を変更してから、**タブ** キーを押すか、UI 要素の外側の領域をクリックする必要があります。 その時点でのみ、クライアントはフィールド値が変更されたことを検出し、必要なアプリケーション検証またはビジネス ロジックの実行に進むことができます。 したがって、タスク ガイドは、ステップがユーザーにより完了したと判断する前に、フィールド値が変更されたことを検出するためクライアントに依存します。

### <a name="what-can-a-task-guide-allow-a-user-to-do"></a>タスク ガイドを使用してユーザーができることは何ですか?

ユーザーがタスク ガイドに記入しているとき、クライアントは、ユーザーがタスク ガイドに記入していないときと同様に、同じ方法で、同じデータ、セキュリティ、および検証ルールを使用して動作します。 ユーザーがタスク ガイドを完了していないときには実行できないアクションを実行できるようにする、クライアントでの動作には違いはありません。 ユーザーがタスク ガイドに記入しているとき、以下の操作が行われます。
-   ユーザーが入力するデータは、タスク ガイドを再生していないときと同じデータ検証ルールの対象となります。
-   ユーザが入力したすべてのデータは保存され、タスク ガイドを再生しないときと同じ制限やルールに従ってデータを変更することができます。
-   ユーザーが検出するすべてのセキュリティ メカニズムは、ユーザーがタスク ガイドを再生しない場合と同じように動作します。
-   ユーザーがアクセスするフォームまたはコントロールは、ユーザーがタスク ガイドを再生していないときと同じセキュリティおよびアクセス メカニズムの影響を受けます。

### <a name="the-on-rails-feature-of-task-guides"></a>タスク ガイドの「オンレール」機能

既定では、ユーザーがタスク ガイドを開始すると、それらは「オンレール」に配置されます。 これらの「レール」は、タスク ガイドが指している要素以外の要素を *クリックする* ことを防止します。 ユーザーがタスク ガイドが指し示す UI 要素以外のものをクリックしようとすると、タスク ガイド ポップアップは、アニメーションによって、タスク ガイドの現在のステップを完了するまで前に進めないことを、ユーザーに知らせます。 

ユーザーが他の要素の *クリック* を禁止されているときでも、そのユーザーはフォーム上の他のコントロールを介してタブ移動することができ、そのユーザーはキーボード ショートカットを使用することができます。 これは、アプリケーションに慣れるにつれて、主にマウスを使用することが期待される初めてのユーザーを対象とした、「オンレール」機能が設計されているためです。 

さらに高度または経験豊富なユーザーは、タスク ガイドの完了時に、「オンレール」 機能を無効にできます。 タスク ガイドのどのポイントでも、ページ上部のタスク レコーダー ツールバーに表示される **ロック解除** ボタンをクリックすると、「レール」 を解除できます。 このボタンは、タスク ガイド中の任意のポイントで 「レール」 を復元するためにも使用できます。 状況によっては、タスク ガイドが 「オンレール」 機能を自動的にオフにする場合があります。 「レール」 をオフにすると、ユーザーはタスク ガイドが実行されていないときと同様に UI 要素をクリックできます。 「オンレール」 機能は、次の状況で自動的に停止する場合があります:

-   ユーザーは、ナビゲーション ウィンドウまたはナビゲーション検索を使用してページに移動するように指示されています。
    -   ユーザーはいずれかのエントリ ポイントを使用できるため、タスク ガイドは特定のエントリ ポイントを指定することはなく、ユーザーがどちらのエントリ ポイントを使用してもかまいません。
-   タスク ガイドが、エラー状態になります (エラー状態の一覧については次のセクションを参照してください)。
-   タスク ガイドには、情報ステップが表示されます。

### <a name="error-detection"></a>エラー検出

*エラー状態* は UI 要素が画面上に表示しないのでタスク ガイドが現在のステップに関連付けられている UI 要素をポイントすることができない場合に発生します。 タスク ガイドが、非表示の UI 要素とユーザーが対話することを現在のステップが必要としていることを検出すると、タスク ガイド ポップアップが画面の右上に移動します。 これらのエラー状態の原因は、2 つのカテゴリに単純化することができます。

#### <a name="the-control-is-not-visible-on-the-form"></a>コントロールがフォーム上に表示されていません

*このエラー状態は通常、ユーザーが誤ったタブ、クイック タブ、折りたたみ可能なセクション、情報ボックス、またはポップアップ メニューを開いたり閉じたりしたときに発生します。*

現在のステップで必要な UI 要素は現在のフォームのどこかにありますが、画面上には表示されないため、ユーザーが実行すべきアクションを通知する同じ指示の表示中にタスクガイドのポップアップは画面の右上に移動します。

タスク ガイドは、画面上で UI 要素を見つけることができないため、ユーザーは UI要素 が非表示になっている原因を手動で特定し、要素を画面に表示する必要があります。 タスク ガイド ポップアップは、UI 要素が表示されていることを自動的に検出し、現在表示されている要素をポイントしするように位置変更します。

#### <a name="the-control-is-not-on-the-form"></a>コントロールがフォーム上にありません

*このエラー状態は通常、ユーザーが間違ったフォームに移動するか、正しいフォームから離れることによって、間違ったフォームに移動したときに発生します。*

UI 要素が画面上に表示されないために、タスク ガイドのポップアップは画面の右上側に移動します。 さらに、タスク ガイドによってユーザーが間違ったフォーム上にいることを検出すると、タスク ガイドのポップアップ テキストが変更され、移動すべきフォームをユーザーに通知します。

場合によっては、タスク ガイドのポップアップではフォームが名前で示されません。 これは、ユーザーが動的フォームに移動する必要があるためです。 動的なフォームは、モデル化されていない、頻繁にランタイムに生成されるフォームと呼ばれるフォームです。 このようなフォームでは、正確な名前はありません。 ランタイムによって生成されるフォームの例には、単純なルックアップとカスタム ルックアップなどがあります。 ユーザーがルックアップ フォームに移動する方法は、ルックアップを再度開くことです。

### <a name="next-step-and-previous-step"></a>次および前のステップ

**次のステップ** と **前のステップ** ボタンは、タスク ガイドのポップアップに表示され、ユーザーがタスク ガイドのフローを手動で制御できるようにします。 これらのボタンをクリックすると、タスク ガイドが次または前のステップに進みます。 タスク ガイドは、ユーザーが次または前のステップに進む前に、ステップを完了したかどうか確認しません。 

**次のステップ** および **前のステップ** ボタンが使用されている場合でも、タスク ガイドは、ユーザーのステップを自動的に完了する **ことはありません**。 これらのボタンを使用すると、前のステップまたは次のステップが現在のページにない UI 要素を参照する場合、エラー状態が発生します。 ユーザーが情報ステップを完了したとき、続行する唯一の方法は、**次のステップ** ボタンを使用することです。 このアクションが必要なのは、情報ステップが任意の UI 要素に記録されたアクションを表していないためです。 タスクの記録にアクションが記録されていないため、タスク ガイドには、ユーザーが完了する必要のあるアクションを決定するために必要な情報がありません。

### <a name="the-see-more-button"></a>[詳細情報] ボタン

**詳細情報** ボタンをクリックすると、タスク ガイドのポップアップが展開され、ステップに関連する追加情報が表示されます。 追加情報は多くの場合、オプションの参考資料であり、ステップを完了するために必要ではありません。 次の情報が含まれる場合があります:

-   **例** の値
    -   Example 値は、タスク記録が作成されたときに使用されていた値です。
    -   値の例は、非ルックアップ フィールドを使用するステップにのみ表示されます。 これらのフィールドには、テキスト フィールド、数値フィールド、日付フィールド、コンボ ボックス、およびチェック ボックスが含まれます。
-   **注記**
    -   注記には、タスク ガイドの現在のステップについて、ユーザーにコンテキストを提供するのに役立つシナリオ固有の情報が含まれている場合があります。

## <a name="taking-screenshots-in-task-recorder"></a>タスク レコーダーでのスクリーンショットの撮影

新しい (Chromium ベースの) Microsoft Edge ブラウザーと Google Chrome の両方で機能する **プレリリース** の Chromium ブラウザー拡張機能を使用することにより、タスク レコーダーは、ユーザーが業務プロセスを記録するときにブラウザーのスクリーンショットを撮影することができます。 ユーザーが記録を完了すると、タスク レコーダーはこれらのスクリーンショットを使用して Microsoft Word ドキュメントを生成できます。 この機能を有効にするには、次の手順に従って、プレリリースの Chromium 拡張機能をインストールして、記録中にタスク レコーダーがスクリーンショットを撮影できるようにします。

1.  <https://github.com/Microsoft/FMLab> で、GitHub から拡張機能を含む **FMLabTaskRecorderScreenshot** フォルダをダウンロードします。
2.  **オンプレミス配置のみ:** 次のコードと一致するように、拡張機能のマニフェストを調整します。 \<hostname\> を環境のベース URL に置き換えます。

    ```json
    ...
    "content_scripts": [
        {
            "matches": ["https://*.dynamics.com/*", "<hostname>"],
            "js": ["screenshot.js"]
        }
        ...
    ```

3.  **[中国の 21Vianet](../deployment/china-local-deployment.md) 配置のみ:** 次のコードと一致するように、拡張機能のマニフェストを調整します。 **.com** を **.cn** に置き換えます
    ```json
    ...
    "content_scripts": [
        {
            "matches": ["https://*.dynamics.cn/*"],
            "js": ["screenshot.js"]
        }
        ...
    ```
4.  **[米国政府機関向けコミュニティ クラウド (GCC)](../deployment/us-gcc-deployment.md) 配置のみ:** 次のコードと一致するように、拡張機能のマニフェストを調整します。 **dynamics.com** を **microsoftdynamics.us** に置き換える
    ```json
    ...
    "content_scripts": [
        {
            "matches": ["https://*.microsoftdynamics.us/*"],
            "js": ["screenshot.js"]
        }
        ...
    ```
4.  **複数の配置:** matches 句に文字列値を追加し、コンマで区切ります。
    ```json
    ...
    "content_scripts": [
        {
            "matches": ["https://*.dynamics.com/*", "https://*.microsoftdynamics.us/*"],
            "js": ["screenshot.js"]
        }
        ...
    ```
6.  最新の Microsoft Edge ブラウザーまたは Google Chrome を開きます。
7.  Microsoft Edge で **設定とその他 &gt; 拡張機能** (または Google Chrome で **Google Chrome のカスタマイズと制御 &gt; その他のツール &gt; 拡張機能**) を選択します。
8.  **開発者モード** を選択します。
9.  **展開された拡張子の読み込み** をクリックします。
10.  パス **FMLab-master \> FMLab \> TaskRecorderScreenshot** を使用してタスク レコーダー拡張子を含むフォルダーを参照してから、**フォルダーの選択** を選択します。
11.  拡張機能が有効になるように、**有効** が選択されていることを確認します。
12.  ブラウザーを再起動します。

タスク レコーダーは、クライアントが実行しているタブのスクリーンショットを撮影します。 必要に応じて、タスク記録をもう一度再生して、スクリーンショットを再生成できます。

タスク レコーダーは、他のタブまたはユーザーのデスクトップからスクリーンショットを取得 **しない** 点に注意してください。

## <a name="generating-tests-from-a-recording"></a>記録からのテストの生成

タスク レコーダーを使用して業務プロセスの記録を完了したら、開発者は未加工の開発者記録ファイル (.xml ファイル) を Visual Studio にインポートして、X++ テストを作成できます。 Import Tool は、記録から人間が判読可読な X++ テストを生成し、コントロール ジェスチャ、検証、またはタスクを適切なテスト コードに変換します。 

### <a name="import-a-recorded-test"></a>記録されたテストのインポート

1.  財務と運用の開発ツールを使い、Visual Studio を開きます。
2.  **Dynamics 365 &gt; アドイン &gt; タスク記録のインポート** に移動します。
3.  **タスクの記録をインポート** メニューで、**参照** ボタンを使用して以前にダウンロードした記録ファイルを検索します。
4.  必要に応じて、生成されたテスト コードをスタートアップ プロジェクトに追加することを選択します。 これには、プロジェクトを含むソリューションがスタートアップ プロジェクトとして設定されている必要があります。 これにより、生成された X++ テストがプロジェクトと同じモデルになります。
5.  新しいプロジェクトの作成時に、プロジェクトのモデルを選択します。 生成された X++ テストがこのモデルに配置されます。 モデルは、生成されたテストを正常にビルトするには、モデルには **TestEssentials** モデルへの参照が必要です。
6.  **インポート** をクリックします。

    [![インポート タスク記録ダイアログ ボックス。](./media/importnewproject_taskrecorderguide.png)](./media/importnewproject_taskrecorderguide.png)

7.  **新しいプロジェクト** ダイアログ ボックスで、プロジェクトの名前を指定します。
8.  プロジェクトが作成されると、ユーザーは生成されたコードを開き検査することができます。
9.  テストを実行するには、プロジェクトをビルドします。
10. **テスト &gt; ウィンドウ &gt;テスト エクスプ ローラー** の順にテスト移動します。

## <a name="appendix"></a>付録

### <a name="controls-that-are-known-to-have-incomplete-support-for-task-recorder"></a>タスク レコーダの未完了なサポートがあることが知られているコントロール

-   テーブル
-   フィルター ウィンドウは、左側から表示されるフィルターです
    -   フィルターをフィルター ウィンドウに追加すると、その手順に遅延が発生します。 フィルター ウィンドウでユーザーが [適用] をクリックするまで、ステップは記録されません。
-   拡張プレビュー
    -   拡張プレビュー内でのジェスチャーの記録に関するサポートは計画されていません。 記録中は、拡張プレビューは無効になります。
-   セグメント化されたエントリを除いて、拡張可能なコントロールはそのまま使用できません。
    -   拡張可能なコントロールの所有者は、タスク レコーダーのサポートを個別にビルドする必要があります。

### <a name="controls-that-can-be-recorded-but-have-limited-support-for-the-copypastevalidate-gestures"></a>記録できますが、コピー/貼り付け/検証ジェスチャーのサポートが制限されているコントロール

-   日時
    -   値として「なし」のコピーまたは貼り付けをサポートしないでください。
-   画像
    -   イメージ値をコピー/貼り付け/検証する機能はありません。
-   フィルター ウィンドウ
    -   コピー/貼り付けは機能しますが、貼り付けられたデータは UI に表示されません。 正しく貼り付けられたかのように続行することができます。
-   メッセージ ボックス
    -   メッセージ ボックスのテキストを検証することはできません。

### <a name="controls-that-are-known-to-have-incomplete-support-for-being-used-in-a-task-guide"></a>タスク ガイドで使用するための未完了なサポートがあることが知られているコントロール

- リストの上部に表示されるフィルター コントロールであるクイック フィルター
  -   タスク ガイド中の「一般的な値」の表示をサポートしないでください。 現在、録音中に使用された値が表示されます。
- フィルター ウィンドウは、左側から表示されるフィルターです
  -   タスク ガイドは、クリックする必要があるフィルタ ウィンドウ内の各要素を指定しません。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

