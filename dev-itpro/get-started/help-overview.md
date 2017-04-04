---
title: "ヘルプの概要"
description: "この記事では、Microsoft Dynamics 365 for Operations のヘルプ システム コンポーネントの概要が示されます。 また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。"
author: margoc
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>ヘルプの概要

この記事では、Microsoft Dynamics 365 for Operations のヘルプ システム コンポーネントの概要が示されます。 また、組織の独自のドキュメントやトレーニングを提供する方法について説明します。 

Microsoft Dynamics 365 for Operations には、2 つの主要なコンポーネントに基づくまったく新しいヘルプ システムが含まれています。

-   ドキュメントのサイト
-   タスク ガイド

次のスクリーン ショットに示すように、Dynamics 365 for Operationsのヘルプ ウィンドウから記事や作業ガイドにもアクセスできます。 [![ヘルプ ウィンドウ] (。/media/helpウィンドウopsタスク ガイド1024x741.png) ] (。/media/helpウィンドウopsタスクguides.pngは、この記事では、ヘルプ システムについて、組織にカスタム ドキュメントとトレーニング リソースを作成する方法を説明します。

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.comのヘルプ
docs.microsoft.comのサイト (docs.microsoft.com/dynamics365/operations [] (https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations)は、Dynamics 365 for Operationsの製品ドキュメントの基本ソースです。 サイトは次の機能があります:

-   **最新のコンテンツへのアクセス– **は、サイトによってための、製品ドキュメントを作成および表示および更新できます。詳細に柔軟を示します。 したがって、最新の技術情報にアクセスできることを保証するために役立ちます。
-    **満足照合します。こうしたエキスパートによって作成された** –は、Microsoftサイトの内側と外部の両方に会員地域によって高めることができる製品ドキュメントの豊富な設定を提供します。
-   **内容のタイプへのアクセス– **は、サイトMicrosoft Officeの両方のプレゼンテーション、タスク、およびビデオ ヘルプWiki記事では、Dynamics 365 for Operationsに関する内容のタイプにアクセスすることをすぐに有効にします。
-    **満足照合します業務プロセスをサポートする** –サイトはMicrosoft Dynamics Lifecycle Services (LCS)の業務プロセスのModelerを使用する(BPM)ビジネスprocess–focusedコンテンツが含まれています。

Microsoft、Microsoftの前のヘルプWikiのドキュメントの内容すべての移行しました。 Microsoft、Microsoftのサイトについてよく興奮、があることを望みます。

### <a name="when-can-we-use-it"></a>いつ使用することができますか。

ドキュメントのコンテンツをすぐにを読み取ることができます。。これはサインインが必要なしないで完全にパブリックと捜せます。 内容の検索にはお気に入りの検索エンジンを使用できます。 選択したサイトの技術情報についてGitHubの勘定に署名で、コメントできます。


## <a name="task-guides"></a>タスク ガイド
このガイドでは、タスクの手順について説明します、または業務プロセスとして制御された、ガイド付き、対話型の経験。  (演劇) ヘルプ ウィンドウのタスク ガイド"を開くことができます。 最初にタスク ガイドをクリックすると、ヘルプ ウィンドウはタスクの手順を示します。 集中するタスク ガイドはなりました。 [!["タスクの読み取りの表示] (。/media/taskガイドOps 1024x742.png) ] (。ガイド付き、対話型の経験、[を**ガイド タスクを開始します。**ヘルプ ウィンドウの下では開始/media/taskガイドops.png)。 黒のポインタが、実行する必要があるアクションを開いて、表示します。 UI に表示される指示に従い、指示されたデータを入力します。 [タスク]!["の手順 (。/media/task "手順1 ops.png) ] (。重要な/media/task "手順1 ops.png) **: **このガイドのするときに入力されたデータは実際になります。 実稼働環境である場合、データは現在使用している会社で入力されます。

### <a name="it-all-begins-with-task-recorder"></a>すべてタスク レコーダーから始まります。

タスク ガイドは、タスク レコーダーを使用して作成されます。 タスク レコーダーを使用すると、Dynamics 365 for Operations UI で実行するアクション (メニューのクリック、設定の変更、データの入力) はすべて記録されます。 記録する手順は、[タスク記録] と呼ばれます。 前のセクションで説明したように、タスク記録は [ヘルプ] ウィンドウに表示され、タスク ガイドとして再生できます。 ただし、タスク記録を使用できるそのほかの方法があります。

-   **タスク記録を BPM に保存** – LCS の BPM ライブラリの階層の明細行にタスク記録を保存できます。 BPM にタスク記録を保存すると、フローチャートの図が生成され、記録のステップとともに表示されます。 **メモ:** Dynamics 365 for Operations の [ヘルプ] ウィンドウに表示させてタスク ガイドとして再生するには、記録を BPM ライブラリに保存します。
-   **タスク記録をWord文書として保存** – Microsoft Word文書としてタスク記録を保存すると、組織の印刷可能なトレーニング ガイドを簡単に作成できます。

タスク レコーダに関する詳細については、" [Dynamics 365 for Operationsのタスク レコーダ] (。/user-interface/task-recorder.md)。

### <a name="creating-customized-task-recordings"></a>カスタマイズされたタスク記録の作成

独自のタスク記録を作成するか、Microsoft の提供するタスク記録をダウンロードしてカスタマイズすることができます。 したがって、固有の Dynamics 365 for Operations の実装を反映する、組織のカスタマイズされたヘルプを作成できます。 Dynamics 365 for Operationsのタスク記録を表示するには、ウィンドウを確認し、タスク ガイドとして、LCSのBPMのライブラリに記録を保存する必要がありますします。 パートナーになり、会社のライブラリにライブラリを促進およびソリューションに含めれば、顧客が使用できます。 詳細な手順については、" "を参照してください[ドキュメントやトレーニングを作成するタスク記録を使用して] (。/user-interface/task-recorder.md)。

## <a name="in-product-help"></a>製品内ヘルプ
Dynamics 365 for Operations内のヘルプ コンテンツにアクセスするには、** **ヘルプ ([**か。** [) は、ヘルプ アイコンを選択するか、またはCtrl+Shift+を押して、または。 どちらの場合も、[ヘルプ] ウィンドウが開きます。 ヘルプ ウィンドウで、記事や作業ガイドにアクセスできます。 [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>ヘルプ ウィンドウのアクセスの記事

ヘルプ ウィンドウで、工程のクライアント365 for Operationsに適用される技術情報にアクセスできます。 最初にヘルプ ウィンドウを開き、** Wiki **タブをクリックすると、Dynamics 365 for Operationsで現在処理されていることページに適用される技術情報が表示されます。 技術情報がない場合、検索条件を調整するキーワードを入力できます。 ヘルプ ウィンドウの記事をクリックすると、新しいタブは、ブラウザで開き、技術情報を表示します。 

### <a name="accessing-task-guides-from-the-help-pane"></a>ヘルプ ウィンドウからアクセス タスク ガイド

ヘルプ ウィンドウからタスク ガイドにアクセスできるようにシステム管理者はにDynamics 365 for Operationsで**システム パラメータ**]ページで、コンフィギュレーションする設定のステージがあります。 **メモ :**

-   ヘルプを設定するには、Dynamics 365 for Operations を導入したテナントと同じテナントのアカウントを使用してサインインする必要があります。
-   ローカル仮想ハード ドライブ (VHD) で実行されている Dynamics 365 for Operations のインスタンスから、LCS ライブラリに接続することはできません。

[![システム![設定では、ヘルプ"] (。/media/system-parameters_ops-1024x437.png) ] (。**システム パラメータ**ページでは、/media/system-parameters_ops.png、次の手順に従います。:

1.  **重要: **[ヘルプ] タブを初めて開く際には、Lifecycle Services に接続する必要があります。 フォームの途中でリンクをクリックするしてくださいい接続、決算のダイアログ ボックス待ち、[パラメーターに取得するOK]をクリックします。[![はLCSに接続します] (。/media/connectにlcs穀物1024x365.png) ] (。/media/connectにlcscrop.png) 
2.  接続する Lifecycle Services プロジェクトを選択します。
3.  タスク記録を取得する BPM ライブラリ (選択したプロジェクト内) を選択します。
4.  BPM ライブラリの表示順序を選択します。 これにより、ライブラリからのタスク記録が [ヘルプ] ウィンドウに表示される順序が決まります。

システム管理者がこれらの手順を完了したら、[**ヘルプ**] ウィンドウを開いて [タスク ガイド] タブをクリックします。 これで、Dynamics 365 for Operationsで現在処理されていることページに適用するタスク ガイド"を参照してください。 タスク ガイドがない場合、検索条件を調整するキーワードを入力できます。 ヘルプ ウィンドウのタスク ガイドをクリックすると、ヘルプ ウィンドウは手順と、タスク ガイドを行うことができます。 [!["タスクの読み取りの表示] (。/media/taskガイドOps 1024x742.png) ] (。/media/taskガイドops.png) 

### <a name="where-are-the-translated-task-guides"></a>変換されたタスク ガイドでは、どの位置にあるか。

変換されたタスクはタイトル ガイドの「すべての言語」ライブラリでリリースされます。 Dynamics 365 for Operationsで、apppropriateのライブラリに接続していることを一括するタスク ガイドの"ヘルプを表示するには、確認してください。 このガイドは、な言語は**オプション** **ユーザー設定での言語設定で、ユーザーに &gt; 対してアクセスを制御します。**。 
-   このガイドでは、選択した言語でタスク ガイドのすべてのテキスト表示されます。このガイドは変換された、開いたとき。
-   タスク ガイドがまだ変換されていない場合は、それを開くと、テキスト (制御のテキスト) の一部のみが選択した言語で表示されます。

## <a name="additional-resources"></a>追加リソース
次の表に、Microsoft Dynamics 365 for Operations のコンテンツを提供する Web サイトを示します。 コンテンツ Web サイトは顧客のライフ サイクルをサポートするために編成されています。 各フェーズは、別の一連のサイトによってサポートされます。 名前の横にアスタリスク (\*) を持つサイトは、サービス計画に関連付けられるアカウントの使用によって署名する必要があります。

| サイト                                                                     | 説明                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com] (https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Dynamics 365 for Operations のすべての製品ドキュメントのホストまたはリンクです。                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | 事前販売からの実装および工程にいたるまで Dynamics 365 for Operations のプロジェクトを管理するのに、顧客とパートナーが使用できるクラウドベースの共同ワークスペースを提供します。 このサイトは、実装のすべてのフェーズに役立ちます。 |
| [CustomerSource] (http://www.customersource.com/)\*                       | 徹底したトレーニング リソースのホストであり、Dynamics 365 for Operations の主なサポート サイトです。 サイト固有のリソースにアクセスするためにサインインが必要な場合があります。                                                                      |
| [サポート ブログ] (http://aka.ms/AXSupportBlog)                              | Dynamics 365 for Operations のサポート チームによって投稿されるヒントおよび秘訣を提供します。                                                                                                                                                  |
| [方法] (http://aka.ms/AXMSDN)                                             | 開発者向けに書き込まれた以前のリリースのコンテンツをホストします。                                                                                                                                                                       |
| [TechNet] (http://aka.ms/TechNet)                                         | IT プロフェッショナルやアプリケーション ユーザー向けに書き込まれた以前のリリースのコンテンツをホストします。                                                                                                                                           |
| [Dynamicsコミュニティ] (http://community.dynamics.com/en/)                  | ブログ、フォーラムおよびビデオをホストします。                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/] (http://www.microsoft.com/dynamics/)                 | 評価と販売情報を提供します。                                                                                                                                                                                                 |



<a name="see-also"></a>参照
--------

[アクションのヘルプ システム (ダウンロードできるにファクト シート) ] 365 for Operations (https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[、Microsoft Dynamics 365のタスク レコーダ] (。/user-interface/task-recorder.md) 

[タスク記録を使用してドキュメントやトレーニングを作成](../user-interface/task-recorder.md)

[新規または更新タスク ガイド (2016年12月11) ]新しいタスク (ガイド月11 2016.md) 
[新規または更新タスク ガイド (2016年12月8) ] ([更新タスク ガイド使用できます尊厳な2016.md) 
[新規または更新タスク ガイド (2016年12月5) ] ([更新タスク ガイド使用している場合2016.md) 
[新しいタスク ガイド (2016年12月2) ]新しいタスク (ガイド使用して2年2016.md) 






