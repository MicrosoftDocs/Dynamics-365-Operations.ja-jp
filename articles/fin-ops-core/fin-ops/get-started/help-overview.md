---
title: ヘルプ システム (動画を含む)
description: この記事では、財務と運用アプリのヘルプ システムの概要を説明します。
author: edupont04
ms.date: 08/16/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: edupont
ms.search.region: Global
ms.author: edupont
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 16381,  ""intro-internal
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.form: SystemParameters
ms.openlocfilehash: f9095db85e38598ac03b4c77c3fa3be9f450ec02
ms.sourcegitcommit: 78d41eeef0a8a8e94ed502bd89778414231a31ae
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/17/2022
ms.locfileid: "9305227"
---
# <a name="help-system"></a>ヘルプ システム

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

以下のアプリのユーザーは、同じヘルプ システムをベースにした状況依存型のヘルプ、またはその他のコンテンツにアクセスできます。

- Dynamics 365 Commerce
- Dynamics 365 Finance
- Dynamics 365 Human Resources
- Dynamics 365 Supply Chain Management

これらすべてのアプリでは、**ヘルプ** ウィンドウから製品固有のヘルプにアクセスできます。

![ヘルプ ウィンドウ。](./media/help-pane-ops-help.png)

## <a name="help-on-docsmicrosoftcom"></a>docs.microsoft.com のヘルプ

docs.microsoft.com サイト ([docs.microsoft.com/dynamics365/](/dynamics365/)) が前述のアプリの製品ドキュメントの既定のソースです。 このサイトには次のような機能が含まれています:

- **最新コンテンツへのアクセス** – このサイトは、製品ドキュメントの作成、納品、更新をより迅速かつ柔軟に行うことができます。 最新の技術情へのアクセスに役立てることができます。
- **専門家が記述したコンテンツ** – このサイトのコンテンツは、Microsoft 内外のコミュニティメンバーによる投稿を受け付けています。

docs.microsoft.com のコンテンツは、任意の検索エンジンを使用して検索できます。 最適な結果を得るには、次のようなサイト検索を使用することをお勧めします: **site:docs.microsoft.com dynamics 365 "検索する語句"**。

## <a name="get-notified-about-changes-through-an-rss-feed"></a>RSS フィードを通じて変更の通知を受け取る

財務と運用アプリ全体で docs.microsoft.com のコンテンツに加えられたすべての更新の RSS フィードを購読するには、次のリンクを使用します。

[RSS フィード](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finops%27)&locale=en-us)

> [!NOTE]
> RSS フィードは、最新更新された 100 トピックの一覧が返されます。 一覧は日付順に並べ替されますが、最新の更新記事によってリストが作成される前には最大 1 週間かかる場合があります。  

また、アプリケーションで RSS フィードを購読することもできます。

- [Commerce](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-commerce%27)&locale=en-us)  
- [Finance](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-finance%27)&locale=en-us)  
- [Human Resources](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-hr%27)&locale=en-us)  
- [サプライ チェーン](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-supplychain%27)&locale=en-us)  
- [人材](/api/search/rss?$filter=scopes%2fany(t%3A%20t%20eq%20%27dynamics365-talent%27)&locale=en-us)  

### <a name="leave-us-feedback"></a>フィードバックをお送りください

フィードバックまたは記事に関するご質問がある場合は、ページ下部にコメントを記入してください。

1. **フィードバック** をクリックして、ページ下部のコメントに移動します。 次に、**製品フィードバック** 、または **サインインしてドキュメントのフィードバックを提供する** を選択します。

2. コメントを入力して、**フィードバックを送信する** を選択します。

    ![コメントを投稿。](./media/feedback.png)

> [!NOTE]
> ドキュメントのフィードバックを送信する場合は、GitHub アカウントを使用してログインする必要があります。 詳細については、[GitHub プロファイルの設定と管理](https://help.github.com/github/setting-up-and-managing-your-github-profile)を参照してください 。

## <a name="contribute-to-the-documentation"></a>ドキュメントに寄稿する

ドキュメントを寄稿し、編集することができます。 開始するには、記事の **編集** ボタン (鉛筆記号) を選択します。 次のビデオでは、ドキュメントに寄稿する方法を示します。

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE36liB]

[Microsoft Dynamics 365 のドキュメントへの投稿方法](https://youtu.be/m5djioozRbg)ビデオ (上記参照) は YouTube の Microsoft Dynamics 365 チャンネルに含まれています。

詳細については、docs.microsoft.com サイトを構築したチームが公開した [Docs 共同作成者ガイド](/contribute)を参照してください。

> [!NOTE]
> 現時点では英語のコンテンツへの寄稿のみを受け付けています。

## <a name="task-guides"></a>タスク ガイド

タスク ガイドは、制御された、ガイド付きでインタラクティブな方法による、タスクまたは業務プロセスの手順の説明です。 **ヘルプ** ウィンドウからタスク ガイドを開く (再生する) ことができます。 最初にタスク ガイドを選択すると、**ヘルプ** ウィンドウには、タスクのステップ バイ ステップの手順が表示されます。 ローカライズされたタスク ガイドが利用可能となりました。

Microsoft は、2017 年 12 月の Dynamics 365 財務と運用のリリースを介して製品バージョンのタスク ガイド ライブラリをリリースしました。 この記事の [ヘルプ ウィンドウからタスク ガイドにアクセスする](#accessing-task-guides-from-the-help-pane) セクションでは、製品の正しいタスク ガイドを検索する方法について説明します。

![タスク ガイドの読み取りビュー。](./media/task-guide-ops.png)

ガイドのあるインタラクティブな経験を開始するには、**ヘルプ** ウィンドウ下部の **タスク ガイドの開始** を選択します。 進むべき箇所が黒いポインターで示されます。 ユーザー インターフェース (UI) に表示される指示に従い、指示されたデータを入力します。

![タスク ガイドの手順書。](./media/task-guide-step-1-ops.png)

> [!IMPORTANT]
> タスク ガイドの再生時には、実際のデータを入力します。 運用環境である場合、データは現在使用している会社で入力されます。

タスク レコーダーを使用して、独自のカスタム タスク ガイドを作成することができます。 詳細については、[タスク レコーダーを使用したドキュメントやトレーニングの作成](../../dev-itpro/user-interface/task-recorder-training-docs.md) を参照してください。

## <a name="in-product-help"></a>製品内ヘルプ

一部のフィールドには、フィールドに格納されているデータに不明点がある場合に備えて、ユーザーがブロックを解除できるようにフィールドの説明が用意されています。 また、製品内 **ヘルプ** ウィンドウを使用すると、コンテキストに応じたコンテンツへのアクセスが可能となり、ユーザーの使用開始、ブロック解除、詳細情報の取得が容易になります。

ヘルプ コンテンツにアクセスするには、 **ヘルプ** ボタン ( **?**) を選択し、 **ヘルプ** を選択します。 または、**Ctrl+Shift+?** を押します。 どちらの場合も、**ヘルプ** ウィンドウが表示されます。 **ヘルプ** ウィンドウから 、現在使用している製品の領域に関連する概念的なトピックやタスクガイドにアクセスすることができます。

![ヘルプ ウィンドウ。](./media/help-pane-ops-help.png)

### <a name="accessing-help-topics-from-the-help-pane"></a>ヘルプ ウィンドウからヘルプ トピックにアクセスする

**ヘルプ** ウィンドウから、クライアントに適用するトピックにアクセスできます。 最初に **ヘルプ** ウィンドウを開いてから **ヘルプ** タブをクリックすると、現在のページに対応するトピックが表示されます。 トピックが見つからない場合は、検索するキーワードを入力できます。 **ヘルプ** ウィンドウで記事を選択すると 、ブラウザーの新しいタブに表示されます。

> [!IMPORTANT]
> このセクションは Dynamics 365 Human Resources には適用されません。 人事管理 のヘルプ システムは、製品のタスク ガイドに自動的に関連付けられます。 また、人事管理 のタスク ガイドをカスタマイズすることはできません。

### <a name="accessing-task-guides-from-the-help-pane"></a>ヘルプ ウィンドウからタスク ガイドへのアクセス

**ヘルプ** ウィンドウからタスク ガイドにアクセスできるようにするには、システム管理者が、Finance、Supply Chain Management、 Commerce の **システム パラメーター** ページにて、いくつかの設定を構成する必要があります。 詳細については、[タスク ガイドの追加](help-connect.md#adding-task-guides)を参照してください。

<!-- > [!NOTE]
> - In order to configure Help, you must be signed in with an account in the same tenant as the tenant in which the app is deployed.
> - It is not possible to connect to an LCS library from an instance of the app running in a local virtual hard drive (VHD).

![System Parameters form with Help settings.](./media/system-parameters_ops-1024x437.png)

On the **System parameters** page, follow these steps:

1. **Important:** The first time that you open the Help tab, you must connect to Lifecycle Services. Be sure to select the link in the middle of the form, wait for the connection, close the dialog box, and then select **OK** to get to the parameters form.

    ![Connect to LCS.](./media/connect-to-lcs-crop-1024x365.png)

2. Select the Lifecycle Services project to connect to.
3. Select BPM libraries (within the selected project) to retrieve task recordings from.
4. Set the display order of the BPM libraries. This setting determines the order in which task recordings from the libraries will appear in the Help pane.-->

システム管理者がこれらの手順を完了すると、**ヘルプ** ウィンドウを開いて **タスク ガイド** タブをクリックすることができます。そして現在表示しているページに対応したタスク ガイドが表示されるようになります。 タスク ガイドがない場合は、検索するキーワードを入力できます。 **ヘルプ** ウィンドウでタスク ガイドをクリックした後は、**ヘルプ** ウィンドウに段階を追った指示が表示され、タスク ガイドを再生できます。

![タスク ガイドの読み取りビュー。](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides-for-microsoft-libraries"></a>Microsoft ライブラリの翻訳されたタスク ガイドはどこにありますか？

翻訳されたタスク ガイドは、タイトルに「すべての言語」を持つライブラリでリリースされます。 ローカライズされたタスク ガイドのヘルプを参照する前提として、適切なライブラリに接続できている必要があります。 タスク ガイドの表示言語は、**オプション** &gt; **基本設定** の言語の設定で変更することができます。

- タスク ガイドが翻訳されている場合、そのタスク ガイドを開くと、タスク ガイドのすべてのテキストは選択した言語で表示されます。
- タスク ガイドが翻訳されていない場合、それを開くと、一部のテキストのみが選択した言語で表示されます。

## <a name="creating-custom-help"></a>ユーザー定義のヘルプの作成

ユーザー定義のタスク ガイドを作成することで、ユーザー向けのヘルプを作成したり、自分の Web サイトを **ヘルプ** ウィンドウに接続することができます。 詳細については、次のトピックを参照してください。

- [タスク レコーダー リソース](../../dev-itpro/user-interface/task-recorder.md)
- [カスタム ヘルプの概要](../../dev-itpro/help/custom-help-overview.md)

## <a name="additional-resources"></a>追加リソース

次の表に Web サイトの一覧を示します。 名前の横にアスタリスク (\*) のあるサイトには、サービス計画と関連付けられたアカウントでサインインする必要があります。

| サイト | 説明 |
|------|-------------|
| [Docs.microsoft.com](/dynamics365/) | このサイトでは、Dynamics 365 のすべての製品ドキュメントをホスト、またはリンクしています。 |
| [Microsoft Learn](/learn/) | このサイトは、無償で提供されている Microsoft eラーニング サイトです。 |
| [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/)\* | このサイトでは、顧客やパートナーがプリ セールスから導入、運用までのプロジェクトを管理できるクラウド ベースの共同ワークスペースを提供しています。 このサイトは、実装におけるすべてのフェーズに活用できます。 |
| [サポート ブログ](https://aka.ms/AXSupportBlog) | サポート チームが投稿するコツやヒントを参照できます。 |
| [Docs.microsoft.com/previous versions](/previous-versions/dynamics/) | 古いリリースのコンテンツをホストします。 |
| [Dynamics コミュニティ](https://community.dynamics.com/) | ブログ、フォーラム、ビデオをホストします。 |
| [Microsoft.com/dynamics365](https://www.microsoft.com/dynamics365/home) | 評価と販売情報を提供します。 |




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

