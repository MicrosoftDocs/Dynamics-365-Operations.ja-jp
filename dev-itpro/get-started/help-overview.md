---
title: "ヘルプ概要"
description: "この記事では、Microsoft Dynamics 365 for Operations のヘルプ システム コンポーネントの概要が示されます。 また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。"
author: margoc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6f785ac8b9a8be503bf9122f21716f745b17115b
ms.openlocfilehash: f08434b4c818460009644e77da1b37ba86cc1d54
ms.contentlocale: ja-jp
ms.lasthandoff: 04/27/2017


---

# <a name="help-overview"></a>ヘルプ概要

[!include[banner](../includes/banner.md)]


この記事では、Microsoft Dynamics 365 for Operations のヘルプ システム コンポーネントの概要が示されます。 また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。 

Microsoft Dynamics 365 for Operations には、2 つの主要なコンポーネントに基づくまったく新しいヘルプ システムが含まれています。

-   ドキュメント サイト
-   タスク ガイド

次のスクリーン ショットに示すように、記事と Dynamics Online 365 for Operations の [ヘルプ] ウィンドウのタスク ガイドの両方にアクセスできます。 [![Help ウィンドウ](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) この記事は、ヘルプ システムについて説明し、組織のカスタム ドキュメントおよびトレーニング リソースの作成方法を説明します。

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.com のヘルプ
docs.microsoft.com サイト ([docs.microsoft.com/dynamics365/operations](/dynamics365/#pivot=solutions&panel=solutions_operations) が Dynamics 365 for Operations の製品ドキュメントの基本ソースです。 サイトには次のような機能が含まれています。

-   **最新のコンテンツへのアクセス** – サイトは、製品のドキュメントのより速い、より柔軟な作成、出荷、および更新方法を提供します。 したがって、最新の技術情報にアクセスできることを保証するために役立ちます。
-   **専門家が記述した内容** – サイトは Microsoft 内外のコミュニティ メンバーによって拡張できる豊富な製品ドキュメントのセットを提供します。
-   **異なるタイプのコンテンツへのアクセス** – サイトにより、Microsoft Office Mix プレゼンテーション、タスク ガイド、ビデオ、トピックなど、Dynamics 365 for Operations に関する異なる内容にすばやくアクセスできるようになります。
-   **業務プロセスをサポートするコンテンツ** – サイトには Microsoft Dynamics Lifecycle Services (LCS) のビジネス プロセス モデラー (BPM) を活用する、業務プロセス指向のコンテンツが含まれます。

以前のヘルプ Wiki から docs にすべてのコンテンツを移行しました。 新しいサイトを提供できることを嬉しく思います、ご期待ください。

### <a name="when-can-we-use-it"></a>いつ使用することができますか。

docs の内容は今すぐお読みいただけます。これは完全にパブリックで、サインインせずに検索できます。 内容の検索にはお気に入りの検索エンジンを使用できます。 サインインすることにより、必要に応じてサイトの記事にコメントできます。


## <a name="task-guides"></a>タスク ガイド
タスク ガイドは、制御された、ガイド付きでインタラクティブな方法による、タスクまたは業務プロセスの手順の説明です。 [ヘルプ] ウィンドウからタスク ガイドを開く (再生する) ことができます。 最初にタスク ガイドをクリックすると、[ヘルプ] ウィンドウには、タスクのステップ バイ ステップの手順が表示されます。 ローカライズされたタスク ガイドが利用可能になりました。 [![タスク ガイドの読み取りビュー](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) ガイド付きのインタラクティブな経験を開始するには、[ヘルプ] ページ下部の [**タスク ガイドの開始**] をクリックします。 黒のポインタが、実行する必要があるアクションを開いて、表示します。 UI に表示される指示に従い、指示されたデータを入力します。 [![タスク ガイドの手順書](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **重要:** タスク ガイドの再生時に入力したデータは実際のものです。 実稼働環境である場合、データは現在使用している会社で入力されます。

### <a name="it-all-begins-with-task-recorder"></a>すべてタスク レコーダーから始まります。

タスク ガイドは、タスク レコーダーを使用して作成されます。 タスク レコーダーを使用すると、Dynamics 365 for Operations UI で実行するアクション (メニューのクリック、設定の変更、データの入力) はすべて記録されます。 記録する手順は、[タスク記録] と呼ばれます。 前のセクションで説明したように、タスク記録は [ヘルプ] ウィンドウに表示され、タスク ガイドとして再生できます。 ただし、タスク記録を使用できるそのほかの方法があります。

-   **タスク記録を BPM に保存** – LCS の BPM ライブラリの階層の明細行にタスク記録を保存できます。 BPM にタスク記録を保存すると、フローチャートの図が生成され、記録のステップとともに表示されます。 **メモ:** Dynamics 365 for Operations の [ヘルプ] ウィンドウに表示させてタスク ガイドとして再生するには、記録を BPM ライブラリに保存します。
-   **タスク記録をWord文書として保存** – Microsoft Word文書としてタスク記録を保存すると、組織の印刷可能なトレーニング ガイドを簡単に作成できます。

タスク レコーダーの詳細については、「[Dynamics 365 for Operations のタスク レコーダー](../user-interface/task-recorder.md)」を参照してください。

### <a name="creating-customized-task-recordings"></a>カスタマイズされたタスク記録の作成

独自のタスク記録を作成するか、Microsoft の提供するタスク記録をダウンロードしてカスタマイズすることができます。 したがって、固有の Dynamics 365 for Operations の実装を反映する、組織のカスタマイズされたヘルプを作成できます。 Dynamics 365 for Operations の [ヘルプ] ウィンドウにタスク記録を表示させてタスク ガイドとして再生するには、記録を LCS の BPM ライブラリに保存します。 パートナーの場合、ライブラリを会社のライブラリに昇格してソリューションに含める場合、顧客が使用できます。 詳細な手順については、「[ドキュメントとトレーニングの作成にタスク記録を使用](../user-interface/task-recorder.md)」を参照してください。

## <a name="in-product-help"></a>製品内ヘルプ
Dynamics 365 for Operations 内のヘルプ コンテンツにアクセスするには、[**ヘルプ**] (**?**) アイコンをクリックしてからヘルプを選択するか、Ctrl + Shift + ? を押します。 どちらの場合も、[ヘルプ] ウィンドウが開きます。 [ヘルプ] ウィンドウから記事またはタスク ガイドにアクセスできます。 [![Help ウィンドウ](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>[ヘルプ] ウィンドウから記事へのアクセス

[ヘルプ] ウィンドウから、Dynamics 365 for Operations クライアントに適用する記事にアクセスできます。 最初に [ヘルプ] ウィンドウを開いてから [**Wiki**] タブをクリックすると、Dynamics 365 for Operations の現在のページに対応する記事が表示されます。 記事がない場合は、検索するキーワードを入力できます。 [ヘルプ] ウィンドウで記事をクリックすると、ブラウザで新しいタブが開いて記事を表示します。 

### <a name="accessing-task-guides-from-the-help-pane"></a>ヘルプ ウィンドウからタスク ガイドへのアクセス

[ヘルプ] ウィンドウからタスク ガイドにアクセスできるようになる前に、システム管理者が Dynamics 365 for Operations の [**システム パラメーター**] ページに進み、設定をコンフィギュレーションする必要があります。 **メモ :**

-   ヘルプを設定するには、Dynamics 365 for Operations を導入したテナントと同じテナントのアカウントを使用してサインインする必要があります。
-   ローカル仮想ハード ドライブ (VHD) で実行されている Dynamics 365 for Operations のインスタンスから、LCS ライブラリに接続することはできません。

[![システム パラメーター フォームとヘルプ設定](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) **システム パラメーター** ページで次の手順に従います。

1.  **重要:**[ヘルプ] タブを初めて開く際には、Lifecycle Services に接続する必要があります。 フォームの中程のリンクをクリックし、接続されるまで待機し、ダイアログ ボックスを閉じ、[OK] をクリックしてパラメーター フォームを取得します。[![LCS に接続](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  接続する Lifecycle Services プロジェクトを選択します。
3.  タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
4.  BPM ライブラリの表示順序を選択します。 これにより、ライブラリからのタスク記録が [ヘルプ] ウィンドウに表示される順序が決まります。

システム管理者がこれらの手順を完了したら、[**ヘルプ**] ウィンドウを開いて [タスク ガイド] タブをクリックします。 これで、Dynamics 365 for Operations の現在のページに対応するタスク ガイドを表示できます。 タスク ガイドがない場合は、検索するキーワードを入力できます。 [ヘルプ] ウィンドウでタスク ガイドをクリックした後、[ヘルプ] ウィンドウにはステップ バイ ステップの手順が表示され、タスク ガイドが再生できます。 [![タスク ガイドの読み取りビュー](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>翻訳されたタスク ガイドはどこにありますか。

翻訳されたタスク ガイドは、タイトルの「すべての言語」を持つライブラリでリリースされます。 Microsoft Dynamics 365 for Operations でローカライズされたタスク ガイドのヘルプを参照するには、適切なライブラリに接続できることを確認してください。 タスク ガイドの表示言語は、[**オプション**] &gt; [**基本設定**] の [言語の設定] でユーザーごとに制御されます。 
-   タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
-   タスク ガイドが翻訳されていない場合、それを開くと、一部のテキスト (コントロールのテキスト) のみが選択した言語で表示されます。

## <a name="additional-resources"></a>追加リソース
次の表に、Microsoft Dynamics 365 for Operations のコンテンツを提供する Web サイトを示します。 コンテンツ Web サイトは顧客のライフ サイクルをサポートするために編成されています。 各フェーズは、別の一連のサイトによってサポートされます。 名前の横にアスタリスク (\*) のあるサイトには、サービス計画と関連付けられたアカウントでサインインする必要があります。

| サイト                                                                     | 説明                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](/dynamics365/#pivot=solutions&panel=solutions_operations) | Dynamics 365 for Operations のすべての製品ドキュメントのホストまたはリンクです。                                                                                                                                                               |
| [ライフサイクル サービス](http://lcs.dynamics.com/en/)\*                      | 事前販売からの実装および工程にいたるまで Dynamics 365 for Operations のプロジェクトを管理するのに、顧客とパートナーが使用できるクラウドベースの共同ワークスペースを提供します。 このサイトは、実装のすべてのフェーズに役立ちます。 |
| [CustomerSource](http://www.customersource.com/)\*                       | 徹底したトレーニング リソースのホストであり、Dynamics 365 for Operations の主なサポート サイトです。 サイト固有のリソースにアクセスするためにサインインが必要な場合があります。                                                                      |
| [サポート ブログ](http://aka.ms/AXSupportBlog)                              | Dynamics 365 for Operations のサポート チームによって投稿されるヒントおよび秘訣を提供します。                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | 開発者向けに書き込まれた以前のリリースのコンテンツをホストします。                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | IT プロフェッショナルやアプリケーション ユーザー向けに書き込まれた以前のリリースのコンテンツをホストします。                                                                                                                                           |
| [Dynamics コミュニティ](http://community.dynamics.com/)                  | ブログ、フォーラムおよびビデオをホストします。                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | 評価と販売情報を提供します。                                                                                                                                                                                                 |



<a name="see-also"></a>参照
--------

[Dynamics 365 for Operations のヘルプ システム (ダウンロード可能なファクト シート)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Microsoft Dynamics 365 for Operations のタスク レコーダー](../user-interface/task-recorder.md)

[タスク記録を使用してドキュメントやトレーニングを作成](../user-interface/task-recorder.md)

[新規または更新されたタスク ガイド (2016 年 11 月)](new-task-guides-november-2016.md)
[新規または更新されたタスク ガイド (2016 年 8 月)](new-updated-task-guides-available-august-2016.md)
[新規または更新されたタスク ガイド (2016 年 5 月)](new-updated-task-guides-available-may-2016.md)
[新規または更新されたタスク ガイド (2016 年 2 月)](new-task-guides-available-february-2016.md)








