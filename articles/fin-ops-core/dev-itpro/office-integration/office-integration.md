---
title: オフィス統合の概要
description: この記事では、Microsoft Office の統合の概念と機能について説明します。
author: jasongre
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.custom:
- "25511"
- intro-internal
ms.assetid: 36ba2da0-ee9b-4f84-b705-751303ccec33
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e5cd5d5651c734d73d57290ceef37d9e67220738
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108619"
---
# <a name="office-integration-overview"></a>オフィス統合の概要

[!include [applies to](../includes/applies-to-commerce-finance-scm.md)]

[!include [banner](../includes/banner.md)]

この記事では、Microsoft Office の統合の概念と機能について説明します。 統合はいくつかの技術に依存します。

-   Microsoft Azure での作業
-   Azure Active Directory (Azure AD) での作業
-   複数のブラウザーで Web クライアントを実行

Microsoft Office の統合機能は、生産的環境を提供し、Office 製品を使用して作業を遂行するユーザーを支援します。

## <a name="excel-data-connector-add-in"></a>Excel Data Connector アドイン
Microsoft Excel は、データを変更してすばやく分析することができます。 Excel Data Connector アプリは、公開されたデータ エンティティに作成された Excel ブックおよび OData サービスとやり取りします。 Excel Data Connector アドインを使用すると、Excel がユーザー エクスペリエンスのシームレスな部分となることができます。 Excel Data Connector アドインは、Office Web アドイン フレームワークを使用して構築されます。 アドインは作業ウィンドウで実行されます。 Office Web アドインは、埋め込み Internet Explorer ブラウザー ウィンドウ内で実行される Web アプリケーションです。 

[![Excel データ コネクタ アプリのスクリーンショット。](./media/1_office.png)](./media/1_office.png)

### <a name="dynamics-ax-2012-architecture-vs-finance-and-operations-architecture"></a>Dynamics AX 2012 アーキテクチャ対財務と運用アーキテクチャ

バージョン間にはいくつかの違いがあります。 両方で、Excel で実行する軽量のアドインを構築し、アプリケーションに接続するサービスを使用します。

#### <a name="dynamics-ax-2012"></a>Dynamics AX 2012

Excel &gt; VSTO (.NET) Add-in &gt; Windows Communication foundation (WCF) &gt; AOS &gt; AX Services and Tables &gt; AX クエリ エンジン &gt; Database の Active Directory (AD) &gt; AIF SOAP サービスによる認証

#### <a name="finance-and-operations"></a>財務と運用

Excel &gt; Office Web Add-in (JS + HTML) &gt; JavaScript OData API (Olingo) &gt; AOS &gt; AX Entities &gt; AX LINQ プロバイダー &gt; AX Database の Azure Active Directory (AAD) &gt; AX OData サービスによる認証

### <a name="office-add-in-explained"></a>Office アドインの説明

Excel Data Connector アプリケーションは、ブックの右側にある作業ウィンドウに配置されます。 [![テーブルに対応する番号付き要素を含む Excel データ コネクタ アプリの場所を示すスクリーン ショット。](./media/2_office.png)](./media/2_office.png) 次の表では、アドインの各部について説明します。 数値は、前のスクリーンショットの数値に対応しています。

| 数値 | 氏名                             | 説明                                                                                                                                                                                                                                                                          |
|--------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1      | アドイン プライマリ タイトル             | Office Web アドイン フレームワークに提供されるアドインのタイトル。                                                                                                                                                                                                        |
| 2      | アドイン セカンダリ タイトル           | アドインによって提供されるアドインのタイトル。                                                                                                                                                                                                                              |
| 3      | 求人者名                      | 選択したデータ テーブルのデータを提供するエンティティのラベル。 ラベルの上にマウス ポインターを移動すると、対応する名前を表示することができます。                                                                                                                                                  |
| 4      | フィールド名                       | 選択したデータ テーブル列のデータを提供するエンティティのフィールド。 ラベルの上にマウス ポインターを移動すると、対応する名前とタイプを表示することができます。                                                                                                                                   |
| 5      | [更新] ボタン                   | ブックのデータを更新します。                                                                                                                                                                                                                                                    |
| 6      | 公開ボタン                   | ブック内のデータの変更を発行します。                                                                                                                                                                                                                                            |
| 7      | デザイン ボタン                    | デザイン時エクスペリエンスを開きます。                                                                                                                                                                                                                                                     |
| 8      | ステータス バー                       | ステータス バーには、一時的な情報のアラートが表示されます。 ステータス バーで表示される情報は、**メッセージ** ダイアログ ボックスでも表示されます。                                                                                                                               |
| 9      | オプション ボタン                   | **オプション** ダイアログ ボックスを開きます。                                                                                                                                                                                                                                                     |
| 10     | メッセージ ボタン                  | プログラムがユーザーに提供する情報メッセージ、警告、およびエラーを表示している **メッセージ** ダイアログ ボックスを開きます。 ユーザーが関心を持つ可能性がある警告またはエラーの数を提供するために、**メッセージ** ボタンの横に番号が表示される場合があります。 |
| 11     | データを含む Excel データ テーブル | この列ヘッダーのフィルターとソート コントロールをこのデータで使用できます。 データの変更が公開される前にフィルターを削除する必要があります。                                                                                                                                         |
| 12     | Office Web アドイン メニュー          | Office Web アドイン メニュー ボタンでは、いくつかの標準的なリンクが提供されます。 最も重要なリンクは、アドインをリロードするために使用されます。 アドインは、再度読み込まれると、アドインに関連付けられているテーブルに格納されているブックのすべてのデータを更新します。             |

### <a name="authentication"></a>認証

OData は、サーバーと同じ認証スタック上に配置されます。 アドインは、OAuth を使用して認証を容易にします。

### <a name="lookups-and-drop-down-lists"></a>ルックアップおよびドロップダウン リスト

表のセルをクリックすると、そのセルに関連付けられているルックアップ、列挙ドロップダウン リスト、または日付の選択が、ソースおよびフィールドの情報の下にあるアドイン内に表示されます。 アドイン内で選択した値は、現在選択したテーブル セルに配置されます。

### <a name="adding-and-deleting-records"></a>レコードの追加と削除

レコードを追加するには、テーブルのすぐ下の行に入力するか、Tab キーを使用してテーブルの最後の行の最後のセルから移動します。 レコードを削除するには、行ラベル (1、2、3、など) をクリックして行を選択し、その行のすべてのセルを削除します。 変更を発行するには、**発行** をクリックします。 **メッセージ** ダイアログ ボックスには、追加、編集、および削除されたレコード数が表示されます。

## <a name="workbook-designer"></a>ブック デザイナー
**ブック デザイナー** ページを使用すると、エンティティおよび一連のフィールドを含む、編集可能なカスタム エクスポート ブックを設計することができます。 **ブックブック デザイナー** (**ExportToExcelWorkbookDesigner**) ページを開くには、**Common&gt;Common&gt;Office統合&gt;Excel ワークブック デザイナー** をクリックします。 データ編集を公開する前に、エンティティのすべてのキー フィールドは Excel テーブルに存在する必要があります。 キー フィールドには、それらの横に鍵の記号があります。 レコードを正常に作成または更新するには、Excel テーブルにすべての必須フィールドがなければなりません。 必須フィールドには、その横にアスタリスク (\*) があります。 

[![必須項目の一覧を示すスクリーン ショット。](./media/3_office.png)](./media/3_office.png) 

ブックを作成するには、アプリ バーの **ブックの作成** をクリックします。 

エンティティが公開するデータを表示するには、**関連するフォームの表示** をクリックします。 このボタンは、**FormRef** プロパティ値を持つエンティティでのみ有効です。

## <a name="document-management"></a>ドキュメント管理
ドキュメントの管理は、Azure Blob storage および SharePoint Online でレコードの添付ファイルの保存をサポートします。 データベースの記憶域は非推奨です。 ドキュメントはアプリケーションを介してのみアクセスでき、データベースのパフォーマンスに悪影響を及ぼさないストレージを提供できるという利点があるため Azure Blob ストレージは、データベースのストレージと同等です。 Azure blob storage は既定でありすぐに動作します。 SharePoint テナントは自動的に検出されるため、O365 ライセンスを持っている場合 SharePoint の記憶域がすぐに機能します。例: TenantA.onmicrosoft.com O365/AAD テナントのユーザーは SharePoint サイトとして TenantA.sharepoint.com を取得します。 ユーザーがドキュメントの管理が無効になっている場合、それを有効にするには、**オプション &gt; 一般 &gt; その他** をクリックし、**ドキュメント処理の有効オプション** を **はい** に設定します。 

[![Yes に設定されたドキュメント処理の有効オプションを示すスクリーン ショット。](./media/4_office.png)](./media/4_office.png) 

データを持つページでは、**添付** ボタンが右上隅に表示されます。 

[![添付ボタンを表示するスクリーン ショット。](./media/5_office.png)](./media/5_office.png) 

**添付ファイル** ページには、前のページで選択したレコードに関連付けられている添付ファイル (ドキュメント) のビューが表示されます。 アプリ バーの **新規** ボタン (**+**) をクリックすると、レコードに新しいアタッチメントを追加することができます。 **ファイル** および **画像** ドキュメント タイプについては、関連ファイルを提供するように求められます。

### <a name="document-preview"></a>ドキュメントのプレビュー

サポート対象のファイルの種類のプレビューは、**プレビュー** クイック タブで提供されます。 PNG イメージやテキスト ファイルなどの基本的なドキュメント タイプは、既定でサポートされています。 Microsoft Word、Excel、および PowerPoint ファイルなどの Office ドキュメント タイプは、実稼動 Office Web Apps サーバーを使用する必要があり、OneBox コンフィギュレーションを利用できない場合もあます。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="office-licensing"></a>Office ライセンス

#### <a name="what-microsoft-365-licenses-are-available"></a>どのような Microsoft 365 ライセンスがありますか ?

「[Microsoft 365 ライセンス オプション](https://products.office.com/business/compare-office-365-for-business-plans)」が多数あります。 所属されている組織にとって、意味のあるライセンスを選択する必要があります。

#### <a name="after-purchasing-a-microsoft-365-license-what-needs-to-be-done-to-set-up-sharepoint-storage-for-attachments"></a>Microsoft 365 ライセンスを購入した後、添付ファイル用に SharePoint ストレージを設定するために何を行う必要がありますか?

ドキュメント パラメーター フォームを開いて、SharePoint サーバーが自動的に検出および設定されていることを確認してください。 ここで、ドキュメント タイプを開くか作成し、"SharePoint" へのドキュメント タイプの場所を設定し、ファイルを保存する必要があるフォルダーを選択します。

## <a name="additional-resources"></a>追加リソース

[Office 統合のチュートリアル](office-integration-tutorial.md)

[Office 統合のトラブルシューティング](office-integration-troubleshooting.md)

[アプリケーション スタックおよびサーバーのアーキテクチャ](../dev-tools/application-stack-server-architecture.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
