---
title: "予算計画"
description: "このラボのは、予算の計画領域のアクションの機能に、Microsoft Dynamics 365 for Operationsのガイド付きビューを表示します。 このラボの目的は、予算計画モジュールのクイック コンフィギュレーションの例、およびこのコンフィギュレーションを使用してどのように予算計画が達成されるかのショーケースを示すことです。  このラボ、予算の計画およびユーザー セキュリティの組織階層の設定]の予算の計画のシナリオ、予算の計画の[レイアウトおよびExcelテンプレートを定義する-作成および有効化の予算の計画プロセス-予算の計画のドキュメントを総勘定元帳からの現物の振出で作成されます予算の計画の編集ドキュメント データ- Excelの予算の計画のドキュメント データを編集すること。を調整するために作成するには、次の業務プロセスまたはタスクに基づく配賦を使用して、]-以前注目している。"
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 10763
ms.assetid: 0f2ba752-1f6d-4f28-b9e9-b2e97d10b6d1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 81b44aa7af3a05ebc28963f406fab98bfbbb340d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning"></a>予算計画

このラボのは、予算の計画領域のアクションの機能に、Microsoft Dynamics 365 for Operationsのガイド付きビューを表示します。 このラボの目的は、予算計画モジュールのクイック コンフィギュレーションの例、およびこのコンフィギュレーションを使用してどのように予算計画が達成されるかのショーケースを示すことです。  このラボ、予算の計画およびユーザー セキュリティの組織階層の設定]の予算の計画のシナリオ、予算の計画の[レイアウトおよびExcelテンプレートを定義する-作成および有効化の予算の計画プロセス-予算の計画のドキュメントを総勘定元帳からの現物の振出で作成されます予算の計画の編集ドキュメント データ- Excelの予算の計画のドキュメント データを編集すること。を調整するために作成するには、次の業務プロセスまたはタスクに基づく配賦を使用して、]-以前注目している。 

<a name="prerequisites"></a>必要条件 
------------------

このチュートリアルについては、それぞれのデモ データ工程の環境365 for Operationsにアクセスする必要があり、の管理者として物資が提供されます。 このラボにプライベート ブラウザ モードで使用しないでください]必要に応じてブラウザの他の勘定からが署名および工程の管理者の資格情報365 for Operationsで署名します。 Dynamics 365 for Operationsに署名する場合は、チェック ボックスに」**金額。** 「選択し、署名する情報を確認します。 これは、Excel のアプリが現在必要な永続する Cookie を作成します。 IE以外のブラウザを使用して、Dynamics 365 for Operationsに署名すると、Excelのアプリケーション内で署名するように要求されます。 Excel のアプリで「サインイン」をクリックすると、IE のポップアップ ウィンドウが開きます。「サインインしたままにする」チェック ボックスをオンにする **必要** があります。 Excel のアプリで「サインイン」をクリックしても何も表示されない場合、IE の Cookie キャッシュを削除する必要があります。

## <a name="scenario-overview"></a>**Scenario overview**
ジュリアは、ドイツ (DEMF) の Contoso Entertainment Systems の財務マネージャーとして勤務しています。 FY2016 が近づき、翌年の会社の予算を設定する業務を行う必要があります。 予算の設定は次のようになります。

1.  ジュリアは予算を作成する開始点として前年度の実績を使用します。
2.  前年度の実績に基づいて、翌年の 12 か月間の見積を作成します
3.  ジュリアは、CFO と予算を確認します。 これらが終了した後に、予算計画に必要な調整を行い、予算の設定を確定します。

次のようにシナリオの外観の計画コンフィギュレーション スキーマの割り当てします:

![Screenshot1](./media/screenshot1-300x152.png)

ジュリア、予算を準備するには、Excelテンプレートを使用します:

[![](./media/screenshot2-1024x352.png)](./media/screenshot2.png)

<a name="exercise-1-configuration"></a>練習 1: コンフィギュレーション
=========================

## <a name="task-1-create-organizational-hierarchy"></a>**タスク: 1 組織階層を作成します。**
すべての予算作成プロセスが財務部門で発生すると、ジュリアは、財務部門のみから構成される非常に単純な組織階層を作成する必要があります。 1.1。 組織階層 (コンフィギュレーション管理組織の組織 &gt; 階層) &gt; に移動し、新しいボタンをクリックします。

![Screenshot3](./media/screenshot3.png) 

1.2. 組織階層の名前を入力し、[ボタンは、目的の割り当て

[![] Screenshot4 (。/media/screenshot4.png) ] (。/media/screenshot4.png)  

1.3. [予算の計画目的、[ボタンは、新しく作成された組織階層を追加し、割り当てます: 

[![] Screenshot5 (。/media/screenshot5.png) ] (。/media/screenshot5.png) 

1.4. セキュリティの組織のために上記の手順を繰り返します。 終了した際にフォームを閉じます。

[![] Screenshot6 (。/media/screenshot6.png) ] (。/media/screenshot6.png) 

1.5. [組織階層] フォームで [表示] のボタンをクリックします。 [階層構造デザイナー] の [編集] をクリックし、[挿入] のボタンをクリックして階層を作成します。

[![] Screenshot7 (。/media/screenshot7.png) ] (。/media/screenshot7.png)  

1.6. 予算の階層の [財務部門] を選択します。 

[![] Screenshot8 (。/media/screenshot8.png) ] (。/media/screenshot8.png) 

1.7. 終了後、[公開] および [終了] のボタンをクリックします。 階層の発行の有効日として [2015 年 1 月 1 日] を選択します。

[![] Screenshot9 (。/media/screenshot9.png) ] (。/media/screenshot9.png) 

## <a name="task-2-configure-user-security"></a>タスク 2: ユーザーのセキュリティのコンフィギュレーション
予算計画は、予算計画のデータへのアクセスを構成する際に特別なセキュリティ ポリシーを使用します。 ジュリアは、自分自身に対して、財務予算計画へのアクセス権を与える必要があります。 2.1。 DEMFの法人のコンテキストに移動します: [![] Screenshot10 (。/media/screenshot10.png) ] (。/media/screenshot10.png 2.2)。 予算割り当て設定の &gt; 計画の &gt; 予算の計画 &gt; コンフィギュレーションに移動します。 パラメータでは、セキュリティ モデル値のセキュリティの組織[![] Screenshot11に基づいて設定 (。/media/screenshot11.png) ] (。/media/screenshot11.png 2.3)。 システム管理のユーザーのユーザー &gt; に移動します。 管理者 (ジュリア ファンダーバーク) の予算マネージャーのロールをユーザーに付与します。 [![] Screenshot12 (。/media/screenshot12.png) ] (。/media/screenshot12.png 2.4)。 選択したユーザー ロールと[組織[![] Screenshot13割り当てます (。/media/screenshot13.png) ] (。/media/screenshot13.png 2.5)。 「特定の組織にアクセス許可を付与」を選択します。 最初の手順で作成した [組織階層] を選択します。 財務ノードを選択し、重要な子ボタンの***とのアクセス許可をクリックします。*** *–は、組織のセキュリティとしてこのタスクを、実行可能なentity* [![] Screenshot14ごとに適用するとDEMFの法人のコンテキストにいることを確認します (。/media/screenshot14.png) ] (。/media/screenshot14.png) 

## <a name="task-3-create-scenarios"></a>タスク 3: シナリオの作成
3.1。 BudgetingSetupの予算の計画の&gt;&gt; 予算の計画 &gt; コンフィギュレーションに移動します。 シナリオのページで、このラボでさらに使用するシナリオに注意してください: 前年度の実績と予算。 *注: 必要であれば、この練習用の新しいシナリオを作成し、それらを代わりに使用します。* [![] Screenshot15 (。/media/screenshot15.png) ] (。/media/screenshot15.png) *Note: ジュリアの予算作成に正式な承認プロセスを使用していないため、このラボの作業の現在のステージと、作業の現在のステージ設定スキップ、自動–に既存の設定を承認する作業の流れを使用します。この作業の現在configuration.*については付録を表示します。

## <a name="task-4-create-budget-plan-columns"></a>タスク 4: 予算計画の列の作成
予算計画の列は、予算計画のドキュメント レイアウトに使用できる金銭情報または数量に基づく列です。 上記の例では、"前年度" の実績を表す列、および会計年度の各月を表す 12 の列を作成する必要があります。 列は単純に [追加] ボタンをクリックして値を入力するか、または "データ エンティティ" を使用して作成します。 このラボでは、値を入力するために "データ エンティティ" を使用します。 4.1。 BudgetingSetupで&gt;&gt; 計画の予算の &gt; 計画伸長列組織のページを割り当てます。 オフィス フォームのボタンを右上隅にクリックし、列 (未ろ過) [![] (Screenshot16選択します。/media/screenshot16.png) ] (。/media/screenshot16.png 4.2)。 システムは、値を入力するために使用する Excel ブックを開きます。 編集する要求された、[有効である場合、このアプリケーション[![] Screenshot18信頼 (。/media/screenshot18.png) ] (。/media/screenshot18.png![) [Screenshot17] (。/media/screenshot17.png) ] (。/media/screenshot17.png 4.3)。 ただし、複数の列の値を入力する必要があります。 グリッドに列を追加するには、右側ウィンドウでデザイン]をクリックします: [![] Screenshot19 (。/media/screenshot19.png) ] (。/media/screenshot19.png 4.4)。 [グリッド[![] Screenshot20に追加するために使用できる列を表示PlanColumnsの横の場合鉛筆ボタン (。/media/screenshot20.png) ] (。/media/screenshot20.png 4.5)。 選択したフィールドと[更新]![[Screenshot21に追加する各するフィールドをダブルクリック (。/media/screenshot21.png) ] (。/media/screenshot21.png 4.6)。 Excel の表に作成する必要があるすべての列を追加します。 Excel のオートフィル機能を使用して、明細行をすばやく追加します。 縦スクロールを使用する場合、行のテーブルの一部として、グリッド必要があります (![) [Screenshot22上の列ヘッダーを表示] (追加されていることを確認します。/media/screenshot22.png) ] (。/media/screenshot22.png 4.7)。 Dynamics 365 for Operationsの表示、ページを更新します。 発行された値は365 for Operationsで表示されます。 [![] Screenshot23 (。/media/screenshot23.png) ] (。/media/screenshot23.png) 

## <a name="task-5-create-budget-plan-document-layouts-and-templates"></a>タスク 5: 予算計画のドキュメント レイアウトおよびテンプレートの作成
レイアウトは、ユーザーが予算計画のドキュメントを開いたときに、予算計画ドキュメントの行グリッドが、どのように表示されるかを定義します。 さまざまな角度で同じデータを表示するように予算計画のドキュメントのレイアウトを切り替えることもできます。 ここでは、ジュリアが予算計画のドキュメントで使用するために定義した列があるため、ジュリアは、予算データ (このラボの「シナリオの概要」セクションを参照) 5.1 を作成するために使用する Excel の表に似た、予算計画のドキュメント レイアウトを作成する必要があります。 BudgetingSetupの予算の&gt;&gt; 計画の予算の &gt; 計画コンフィギュレーションのレイアウトのページを開きます。 月間の予算入力のために新しいレイアウトを作成します。

-   レイアウトに主勘定と業務単位を含めるために、MA+BU の分析コード セットを選択します。
-   [要素] セクションの前の手順で作成された、すべての予算計画の列を一覧表示します。 前年度の実績を除くすべてを編集可能にします。
-   どの財務分析コードをグリッドの説明に表示するかを選択するには、[説明] ボタンをクリックします。

[![] Screenshot24 (。/media/screenshot24.png) ] (。/media/screenshot24.png) 予算の計画のレイアウト定義に基づいてただし、予算データを編集する代替方法として使用するExcelテンプレートを作成できます。 Excel テンプレートは、予算計画のレイアウト定義と一致している必要があるために、Excel テンプレートの生成後に予算計画のレイアウトは編集できません。したがって、すべてのレイアウトのコンポーネントが定義された後に、このタスクは実行される必要があります。 5.2。 5.1で作成されたレイアウトを設定します。 手順、[ボタンのテンプレートが &gt; 生成されます。 警告メッセージを確認します。 テンプレートを表示するには、テンプレートのビューを &gt; クリックします。 *Note: 「保存として」を選択、編集するテンプレートが保管される場所を選択してください。ユーザーを保存しないでダイアログの「未処理」選択すると、ときにファイルへの変更は、ファイルがclosed.*場合保たれません [![] Screenshot25 (。/media/screenshot25.png) ] (。/media/screenshot25.png 5.3)。 &lt; オプションの手順が&gt;、ユーザー フレンドリー–を見させますExcelテンプレートを追加する合計フォーミュラ、ヘッダー フィールド、書式設定を変更するなど、変更を保存し、レイアウトのアップロード[![] Screenshot26クリックして計画のレイアウトを &gt; 割り当てるためのファイルをアップロードします (。/media/screenshot26.png) ] (。/media/screenshot26.png) 

## <a name="task-6-create-a-budget-planning-process"></a>タスク 6: 予算計画プロセスの作成
ジュリアは、新たな予算計画を開始するために、上記のすべての設定を組み合わせて、新しい予算計画プロセスを作成して有効化する必要があります。 予算計画プロセスは、どの予算作成の組織、ワークフロー、レイアウトおよびテンプレートが予算計画の作成に使用されるかを定義します。 6.1。 予算割り当て設定の &gt; 計画の予算の計画 &gt; プロセスに移動し、新しいレコードを作成します。

-   予算計画プロセス - DEMF FY2016 予算作成
-   予算サイクル – FY2016
-   元帳 – DEMF
-   既定の勘定構造 – 製造損益
-   組織階層 - ラボの最初に作成した階層の選択
-   予算計画のワークフロー - 自動割り当て - 財務部門のワークフローの承認
-   予算計画のステージ ルールとテンプレートでは、各ワークフローの "予算" 計画ステージが、明細行の "追加" および明細行の "変更" が許可された場合に選択されるか、またどの "レイアウト" が既定で使用されるかが選択されます。

*注: 追加のドキュメント レイアウトを作成し、それらを [代替レイアウト] ボタンをクリックして、予算計画のワークフロー ステージで使用できるように割り当てることができます。* [![] Screenshot27 (。/media/screenshot27.png) ] (。/media/screenshot27.png 6.2)。 この予算の &gt; 計画の作業現在の[![] Screenshot28有効にするには、[工程の有効化 (。/media/screenshot28.png) ] (。/media/screenshot28.png) 

<a name="exercise-2-process-simulation"></a>練習 2: プロセスのシミュレーション
==============================

## <a name="task-7-generate-initial-data-for-budget-plan-from-general-ledger"></a>タスク 7: 総勘定元帳から予算計画の初期データを生成する
7.1。 定期的な予算作成に &gt; 移動は &gt; 総勘定元帳からの予算の計画を生成します。 定期的なプロセス パラメーターを入力し、[生成] ボタンをクリックします。 [![] Screenshot29 (。/media/screenshot29.png) ] (。/media/screenshot29.png 7.2)。 予算の計画を &gt; Generateプロセスで作成された検索するための予算の予算の計画に移動します。 [![] Screenshot30 (。/media/screenshot30.png) ] (。/media/screenshot30.png 7.3)。 [文書番号] のハイパーリンクをクリックしてドキュメントの詳細を開きます。 予算の計画は、このラボ[![] Screenshot31中に作成されたレイアウトで定義されている表示されます (。/media/screenshot31.png) ] (。/media/screenshot31.png) 

## <a name="task-8-create-current-year-budget-based-on-previous-year-actuals"></a>タスク 8: 前年度の実績に基づく今年度の予算の作成
配賦方法を予算計画で使用できます。これにより、1 つのシナリオから別のシナリオに予算計画を簡単にコピーする、それらを複数の期間に分割する、または分析コードに配賦することができます。 前年度の実績からの今年度の予算を作成するために配賦を使用します。 8.1。 予算の計画のドキュメントのグリッドのすべての明細行を選択すると[ボタンは、予算[![] Screenshot32割り当てます (。/media/screenshot32.png) ] (。/media/screenshot32.png 8.2)。 配賦方法、期間キーを選択すると、ソース先および[割り当てます。 

[![] Screenshot33 (。/media/screenshot33.png) ] (。/media/screenshot33.png) 

現在の年の予算への前年度の実際の金額はコピーされ、期間間で品目を販売を使用して配賦する期間キーを曲げてします。 

[![] Screenshot34 (。/media/screenshot34.png) ] (。/media/screenshot34.png) 

## <a name="task-9-adjust-budget-plan-document-using-excel-and-finalize-the-document"></a>タスク 9: 予算計画ドキュメントを Excel を使用して調整し、ドキュメントを確定する
9.1。 Excelの開いているドキュメントのコンテンツへ]ボタンのワークシート

[![] Screenshot35 (。/media/screenshot35.png) ] (。/media/screenshot35.png) 

9.2. Excel ブックを開いて、予算計画ドキュメントで番号を調整し、[公開] ボタンをクリックします。

[![] Screenshot36 (。/media/screenshot36.png) ] (。/media/screenshot36.png) 

9.3. Dynamics 365 for Operationsの予算の計画のドキュメントを表示します。 [作業の現在、&gt; ドキュメントの自動承認を入力します

[![] Screenshot37 (。/media/screenshot37.png) ] (。/media/screenshot37.png)  

現在の作業が完了すると、予算の計画のドキュメントのステージが承認に変更されます。 [![] Screenshot38 (。/media/screenshot38.png) ] (。/media/screenshot38.png) 

<a name="appendix"></a>付録
========

### <a name="auto-approve-workflow-configuration"></a>自動承認ワークフロー コンフィギュレーション

A. 予算割り当て &gt; 設定 &gt; の計画の作業の現在は、テンプレートの予算の計画の現在の作業を使用して新しい作業の流れを作成します:

[![] Screenshot39 (。/media/screenshot39.png) ] (。/media/screenshot39.png) 

この作業の現在は、一つのタスク–のステージに遷移の予算の計画のみが含まれます 

[![] Screenshot40 (。/media/screenshot40.png) ] (。/media/screenshot40.png)  

現在の作業を保存し、有効化します。 

B. 予算割り当て設定の &gt; 計画の &gt; 予算の計画 &gt; コンフィギュレーションに移動します。 ステージで2ステージ–のイニシャルを作成し、入力 

[![] Screenshot41 (。/media/screenshot41.png) ] (。/media/screenshot41.png) 

. C 予算割り当て設定の &gt; 計画の &gt; 予算の計画 &gt; コンフィギュレーションに移動します。 作業の現在のステージ タブの関連で作業の現在のステージは自動–のイニシャルとAの手順で作成し、入れられて承認します。 

[![] Screenshot42 (。/media/screenshot42.png) ] (。/media/screenshot42.png)   


