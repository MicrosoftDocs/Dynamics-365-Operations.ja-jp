---
title: Retail Modern POS (MPOS) および Cloud POS のタスク レコーダーとヘルプ
description: このトピックでは、Retail Modern POS および Cloud POS のタスク レコーダーを使用する方法を説明します。
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTerminalTable, SystemParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.search.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 0ab8456d81fbe2dca495b65b932395572242a25c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413814"
---
# <a name="task-recorder-and-help-for-retail-modern-pos-mpos-and-cloud-pos"></a>Retail Modern POS (MPOS) および Cloud POS のタスク レコーダーとヘルプ

[!include [banner](includes/banner.md)]

このトピックでは、Retail Modern POS および Cloud POS のタスク レコーダーを使用する方法を説明します。

## <a name="overview"></a>概要

Retail Modern POS またはクラウド POS のタスク レコーダーは、高い応答性に焦点を合わせて構築された新しいソリューションです。 業務プロセスを記録する消費者向けに、拡張性とシームレスな統合のための柔軟なアプリケーション プログラミング インターフェイス (API) を提供します。 さらに、Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) で業務プロセス モデル (BPM) ツールと統合されたタスク レコーダーが公開されました。 そのため、ユーザーは、引き続き記録からリッチな業務プロセス ダイアグラムを作成してアプリケーションを分析、設計できます。

## <a name="architecture"></a>アーキテクチャ

タスク レコーダーは、正確な再現性でクライアントでのユーザー アクションを記録できます。 各コントロールが計測され、ユーザー アクションの実行についてタスク レコーダーに通知されます。 コントロールは、イベントが発生したことをタスク レコーダーを通知し、該当するユーザー アクションに関するすべての関連情報をリアルタイムで渡します。 タスク レコーダーは、この情報からユーザー アクションのタイプ (ボタンのクリック、値の入力、ナビゲーションなど) と、ユーザー アクションに関連するデータ (入力データの値とタイプ、フォーム コンテキスト、レコード コンテキストなど) をキャプチャできます。 タスク レコーダーは、記録の再生で、記録されたアクションをユーザーが実行したとおりに実行できることを保証するために役立つ十分な詳細とともに、情報を保持します  (再生機能はまだ Retail modern POS またはクラウド POS で実装されていません)。

## <a name="basic-configuration"></a>基本コンフィギュレーション

POS でタスク記録を有効化するには、次の手順に従います。

1. **Retail とコマース** &gt; **チャネル設定** &gt; **POS 設定** &gt; **レジスター** の順にクリックします。
2. レジスターをクリックしてタスクの記録を有効にします。
3. **登録** タブの **全般** クイック タブで、**タスク記録の有効化** オプションを **はい** に設定します。
4. **保存** をクリックします。
5. **Retail と Commerce** &gt; **Retail と Commerce IT** &gt; **配送スケジュール** の順に移動します。
6. **1090 レジスター** ジョブを選択し、**今すぐ実行** をクリックします。

## <a name="create-a-recording"></a>記録の作成

次の手順に従い、タスク レコーダーを使用して新しい記録を作成します。

1. Retail Modern POS または Cloud POS を起動し、サインインします。
2. **設定** ページの **タスク レコーダー** セクションで、**タスク レコーダーを開く** をクリックします。 **タスク レコーダー** ウィンドウが表示されます。 右上隅の **閉じる** ボタン (**X**) をクリックして **タスク レコーダー** ウィンドウを閉じてから、新しい記録を開始します。 ウィンドウをもう一度開くには、手順 2 を繰り返します。

    [![[タスク レコーダー] ウィンドウ](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3. 記録の名前と説明を入力し、**開始** をクリックします。 **開始** をクリックするとすぐに記録セッションが開始されます。

    > [!NOTE]
    > 記録中に右上隅の **閉じる** ボタン (**X**) をクリックすると、**タスク レコーダー** ウィンドウが閉じられますが、記録セッションは終了されません。 [タスク レコーダー] ウィンドウを再度開くには、画面の上部にある **ヘルプ** ボタン (疑問符) をクリックします。
    >
    > [![疑問符](./media/help.jpg)](./media/help.jpg)

4. **開始** をクリックすると、タスク レコーダーは記録モードになります。 **タスク レコーダー** ウィンドウには、記録プロセスに関連付けられている情報とコントロールが表示されます。
5. Retail Modern POS または Cloud POS ユーザー インターフェイス (UI) で、目的のアクションを実行します。
6. 記録セッションを終了するには、**停止** をクリックします。

## <a name="download-options"></a>ダウンロード オプション

記録セッションを終了すると、いくつかのオプションが表示され、記録をダウンロードできます。

[![ダウンロード オプション](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>この PC に保存

記録パッケージを使用して、タスク ガイドの再生、記録の管理、または記録の注釈の編集を行うことができます  (この機能はまだ Retail Modern POS および Cloud POS で実装されていません。)

### <a name="export-as-word-document"></a>Word ドキュメントとしてエクスポート

記録を Microsoft Word 文書として保存できます。 このドキュメントには、記録されたステップとキャプチャされたスクリーンショットが含まれます。

### <a name="save-as-developer-recording"></a>開発者の記録として保存

未加工の記録ファイルは、テスト コードの生成などの開発者シナリオに役立ちます  (この機能はまだ実装されていません)。

## <a name="recording-controls"></a>記録コントロール

[![記録コントロール](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>停止

記録セッションを終了するには、**停止** をクリックします。 終了後にセッションを再起動することはできません。 そのため、記録が完了したことを確認してから終了してください。

### <a name="pause"></a>一時停止

**一時停止** をクリックして記録セッションを一時的に中止 (一時停止) し、操作を続行します。 **一時停止** をクリックした後で実行するステップは記録されません。

### <a name="continue"></a>続行

一時停止後に記録セッションを再開するには、**続行** をクリックします。

### <a name="capture-screenshots"></a>スクリーンショットのキャプチャ

タスク レコーダーは、業務プロセスを記録するときに Retail Modern POS UI のスクリーンショットをキャプチャできます。 スクリーンショットのキャプチャ機能を有効にするには、**スクリーンショットをキャプチャ** オプションを **はい** に設定し、記録します。 一度記録が完了すると、**停止** をクリックし Word 文書をダウンロードします。 ドキュメントには、該当するスクリーン ショットの手順が含まれます。

> [!NOTE]
> クラウド POS ではスクリーンショットのキャプチャ機能はサポートされていません。

### <a name="start-task-and-end-task"></a>タスクの開始と終了

You can specify the beginning and end of a set of grouped steps by using the **タスクの開始** と **タスクの** **終了** ボタンを使用して、グループ化されたステップの開始と終了を指定できます。 **タスクの開始** をクリックして「タスクの開始」ステップを追加し、グループに含めるステップを実行します。 グループのステップの実行を終了したら、**タスクの終了** をクリックします。 タスクは手順を整理するのに役立ちます。 タスクはその他のタスク内で入れ子にすることができます。 この方法を使用すると、非常に長く複雑な業務プロセスをさらに上手に整理できます。

## <a name="adding-annotations"></a>注釈の追加

注釈は、記録でステップに追加するテキストです。 たとえば、注釈を使用して、詳細なコンテキストや指示をユーザーに与えることができます。 注釈はステップの前後に追加できます。 ステップの右側にある **編集** ボタン (鉛筆のアイコン) をクリックして、任意のステップに注釈を追加できます。

[![ステップの [編集] ボタン](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>テキストとメモ

**テキスト** および **メモ** フィールドを使用して、タスク ガイドのステップに関連付けるテキストを追加できます。

[![[テキスト] および [メモ] フィールド](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>テキスト

**テキスト** フィールドに入力するテキストは、タスク ガイドのステップのテキストの *上* に表示されます。 この場所は、ステップを完了する前にユーザーに読んでもらいたいテキストに適しています。

#### <a name="notes"></a>摘要

**メモ** フィールドに入力するテキストは、タスク ガイドのステップのテキストの *下* に表示されます。 メモのテキストを読み取るには、ユーザーはポップアップ ウィンドウでステップのテキストを展開する必要があります。 この場所は、ユーザーにとって役立つ可能性があるが、アクションを完了するために必要とはしない、オプションの参考資料またはその他の情報に適しています。

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Retail Modern POS および Cloud POS のヘルプ

独自のタスク記録をテキストとして表示するために、Retail Modern POS および Cloud POS のヘルプ ウィンドウに表示するには、タスク記録を BPM ライブラリに保存して、ヘルプ システム パラメーターを BPM ライブラリにポイントするように更新します。 詳細については、「[ヘルプ システムの接続](../fin-and-ops/get-started/help-connect.md)」を参照してください。 Retail Modern POS および Cloud POS のヘルプでは、リアルタイムで LCS を検索します。 コマースのヘルプ システムのパラメーターで選択されているすべての BPM ライブラリを検索し、関連する結果を示します。 **ヘルプ** メニューにアクセスするには、画面の上部にある **ヘルプ** ボタン (疑問符) をクリックし、検索ボックスにプロセス名を入力して、検索ボタンをクリックします。

[![ヘルプ ボタン](./media/help.jpg)](./media/help.jpg)

検索結果でタスク ガイドをクリックするときは、ヘルプ トピックとしてステップを表示するか、Word 文書にステップをエクスポートできます。

> [!NOTE]
> Retail Modern POS および Cloud POS のヘルプ システムでは、使用しているフォームまたは行っている操作によるタスク ガイドは表示されません。 検索ボックスにプロセス名を入力して **検索** ボタンをクリックする必要があります。
