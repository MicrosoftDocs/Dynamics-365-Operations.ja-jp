---
title: Office 統合のトラブルシューティング
description: この記事では、Microsoft Office 統合の機能に関する質問、ヒント、およびトラブルシューティング情報についての回答を示します。
author: jasongre
ms.date: 04/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OfficeAppParameters, SysEmailParameters
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 72263
ms.assetid: 89588fed-b47f-4f01-9328-325518f016d6
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdda4c02bb97c2816107671b744a2c4ba5d134d0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862175"
---
# <a name="troubleshoot-the-office-integration"></a>Office 統合のトラブルシューティング

[!include [applies to](../includes/applies-to-commerce-finance-hr-scm.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]


この記事では、Microsoft Office 統合の機能に関する質問、ヒント、およびトラブルシューティング情報についての回答を示します。 説明されている質問と問題は、ユーザー、管理、および開発のシナリオにわたっています。

## <a name="frequently-asked-questions"></a>よく寄せられる質問

### <a name="what-platforms-do-the-office-add-ins-support"></a>Office アドインはどのようなプットフォームをサポートしますか ?

Microsoft Excel アドインと Microsoft Word アドインは、Office Web/JavaScript アドイン フレームワークを使用して構築されます。 このフレームワークは最初は Microsoft Office 2013 用にリリースされましたが、Microsoft Office 2016 では重要な更新が行われました。 詳細については、[Office アドイン ホストおよびプラットフォームの可用性](/office/dev/add-ins/overview/office-add-in-availability) を参照してください。 Excel アドインには ExcelAPI 1.2 が必要です。 したがって、Excel アドインをサポートするプラットフォームを判断するには、[[Office アドイン ホストおよびプラットフォームの可用性](/office/dev/add-ins/overview/office-add-in-availability)] マトリックスを使用します。 多くのユーザーにとって、語句「Excel 2016 と最新の更新」で十分です。

### <a name="are-the-office-add-ins-safe"></a>Office アドインは安全ですか。

マルウェア、完全な接続、およびコンプライアンス リスクがあるうちは、完全に安全なものはありません。 ただし、他の Web サイトと同様、Web アドインは基本的に、制限のあるアプリケーション プログラミング インターフェイス (API) 経由で Office クライアント製品と対話する Web アプリケーションです。 詳細については、 [Office アドイン プラットフォームの概要](/office/dev/add-ins/overview/office-add-ins) を参照してください。

### <a name="does-the-excel-add-in-support-office-for-mac"></a>Excel アドインは Mac のために Office をサポートしますか。

いいえ。 Office JavaScript (JS) API は、特に認証に関しては、Apple Safari と Microsoft Edge/Internet Explorer で動作が異なります。 Office JS API のプラットフォーム サポートの詳細については、[Office アドイン ホストおよびプラットフォームの可用性](/office/dev/add-ins/overview/office-add-in-availability) を参照してください。

### <a name="what-version-of-office-is-required-for-the-excel-add-in-to-support-ad-fs"></a>Excel アドインが AD FS をサポートするために必要な Office のバージョンとは

詳細については、この記事で後述する「問題のトラブルシューティング」 セクションを参照してください。

### <a name="how-can-i-force-an-update-of-office"></a>どのように Office の更新を強制できますか。

Office ビルドが更新されない場合、遅延したトラックにある場合があります ([Microsoft 365 アプリ更新チャネルの概要](/deployoffice/overview-update-channels)). この場合、[Office 配置ツールを使用して現在のチャネルに移動する](/deployoffice/overview-office-deployment-tool?f=255&MSPPError=-2147217396) を使用するか、最新の更新プログラムがあることを保証するために [Office Insider プログラム](https://products.office.com/office-insider) にサインアップできます。 最も簡単な方法は、Office 配置ツールを使用して現在のチャネルに切り替えることです。 この場合、最新の更新プログラムはすぐにインストールされます。

### <a name="why-cant-you-tell-me-what-version-of-office-or-excel-a-particular-issue-is-fixed-in"></a>どのバージョンの Office または Excel で特定の問題が修正されたか知ることができないのはなぜですか。

Office には、多くのリリースがあります。 これらのリリースは、さまざまな時刻にアップデートを受け取り、対応しないさまざまなバージョン番号を持ちます。 頻繁に使用されるいくつかのバージョンの Office および更新メソッドは、Click to Run (C2R) Current channel、C2R Deferred、C2R First Update Deferred、Office Insider Fast、Office Insider Slow、MSI/MSO (DVD からインストール) です。 Office バージョンの詳細については、[Microsoft 365 アプリの更新に関するリリース情報 ](/officeupdates/release-notes-microsoft365-apps?f=255&MSPPError=-2147217396) を参照してください。

### <a name="why-am-i-having-trouble-signing-into-the-excel-add-in"></a>Excel アドインへのサインインに問題が生じるのはなぜですか。

Excel アドイン (または Office アドイン) を認証するために使用されるブラウザは、Office と操作システムのバージョンに依存します。 コンフィギュレーションへのサインインに使用される特定のブラウザーの詳細については、[Office アドインで使用されるブラウザー](/office/dev/add-ins/concepts/browsers-used-by-office-web-add-ins)。既定では、Excel アドインは、ブラウザーから格納されている資格情報を取得し、格納されている資格情報がない場合は、ブラウザーが現在の Microsoft Windows 資格情報を提供します。 適切な資格情報を使用してサインインしていることを確認します。 Excel アドインで、明示的にサインアウトしてから、適切な資格情報が使用されていることを確認するためにサインインします。

### <a name="the-excel-add-in-seems-to-be-slow-when-it-publishes-records-how-can-i-learn-more-about-what-is-occurring"></a>レコードを発行するとき、Excel アドインが遅くなったように見えます。 何が起こっているかについてもっと知るにはどうすればいいですか。

Excel アドインが実行する作業のほとんどは、サーバーで発生させる必要があります。 時間が費やされている場所を知るには、[[Fiddler (無償ダウンロード)](https://www.telerik.com/fiddler)] を使用して Excel アドインが期待通りに機能することを確認してください。

Excel アドインは、公開されているレコードを要求として送信します。 これらのレコードが処理されると、サーバーから応答が送信されます。 次に、Excel アドインは公開するレコードの次のセットを含む別のメッセージを作成し、その要求を送信します。 Excel アドインでは、サーバーからの以前の応答から、サーバーへの次の要求の間での処理時間に 5 から 10 秒を要します。

Excel アドインとサーバー/サービスの処理時間の関係を確認するには、次の手順を実行します。

1. [Fiddler](https://www.telerik.com/fiddler) を起動します。 
2. プロセスをテストするいくつかのレコードを公開します。
3. Fiddler でその要求と応答を表示できることを確認します ([HTTPS トラフィックが復号化されていることを確認します](https://docs.telerik.com/fiddler/Configure-Fiddler/Tasks/DecryptHTTPS))。
4. 多数のレコードを公開します。 
5. Fiddler では、要求から応答までに必要な時間と、応答から次の要求までに必要な時間を監視します。

    - 要求から応答までの時間が長い場合、ボトルネックはサーバー/サービスです。
    - 次の要求への応答時間が大きい場合は、ボトルネックは Excel アドイン (つまり、クライアント) です。

### <a name="is-export-to-excel-the-best-way-to-get-data-out-of-the-system"></a>システムからデータを取得するには、Excel にエクスポートするのが最善の方法ですか?

エンド ユーザーがシステムからデータを取得する最善の方法は、Excel アドインを使用することです。 アドインは、Open Data Protocol (OData) サービスに依存してデータを取得し、データ エンティティが提供するセキュリティを活用します。 データ管理フレームワーク (DMF) およびデータ インポート/エクスポート フレームワーク (DIXF) のインポートおよびエクスポート機能も使用できます。 ただし、DMF と DIXF は、多くの場合管理者に限定されます。 また、製品で使用可能な[レポートと分析機能](../analytics/bi-reporting-home-page.md)を検討してください。

前述のオプションを使用できない場合は、計算列 (表示メソッド)、フォーマットされた値を持つ列、および一時テーブルからのデータからデータを取得するのに役立つ、Excel へのエクスポート機能を検討することをお勧めします。 エクスポート プロセスでは有効なフォームのデータを使用してデータが取得されるため、Excel にエクスポートするとグリッドに表示されているとおりにデータが返されます。 また、現在のフィルターのセットに一致するデータだけが返されます。

Excel にエクスポートするには独自の一式の制限があります。 第一に、このメカニズムは、OData サービスを通過するオプションよりもエクスポートに時間がかかり、大規模なエクスポートではかなりの時間がかかる場合があります。 第二に、Excel へのデータのエクスポートはメモリを大量に消費するプロセスであり、特に組織がエクスポート行を既定値を超えた場合に、メモリ不足エラーが発生し、サーバーが応答を停止する可能性があります。 監査目的で Excel にエクスポートしません。 非常に大規模なデータセットをシステムからエクスポートする必要がある場合は、データ管理を推奨します。

> [!WARNING]
> 組織では、既定の Excel にエクスポートする行の制限 (50,000 レコード) を増やすことができますが、この制限を 100,000 レコード以上に引き上げ **ない** ことを **強くお勧めします**。 環境の特性やエクスポートされる特定のグリッドによっては、制限が大きすぎるとメモリの問題が発生する場合があります。

Excel からエクスポートするには時間がかかることがあるため、自動ダウンロード オプションを有効にした Chrome または Edge ブラウザーを使用して行うことをお勧めします。 自動ダウンロード オプションを使用すれば、15 分の時間制限内にダウンロード リンクが使用されるように、ブラウザーはエクスポートが完了するとすぐにファイルをダウンロードします。

### <a name="why-is-the-publish-button-in-the-excel-add-in-unavailable"></a>Excel アドインで公開ボタンが利用できないのはなぜですか。 

**発行** ボタンをポイントし、現在公開がサポートされていない理由に関する詳細を取得します。 通常、これが発生するのは、エンティティにデータを公開し返すためにすべてのキー フィールドと必須フィールドが存在する必要があるためです。この場合、デザイナを開いて、すべてのキー フィールドがバインドされている必要があります。  

### <a name="why-are-the-excel-add-in-the-word-add-in-and-the-open-in-excel-options-only-available-when-the-internet-is-available"></a>Excel アドイン、Word アドイン、および Excel で開くオプションは、インターネットが利用可能な場合にのみ利用できます。

オンプレミスを含むすべての環境で、Excel と Word のアドインとライブラリは複数のインターネット地点からロードされます。したがってインターネットが使用可能な場合にのみ実行します。 オンプレミス環境では、インターネットが利用できない場合、コンテンツ配信ネットワーク (CDN) にアクセスできず Excel アドインが実行されないため、Excel で開くオプションは非表示になります。 

### <a name="can-the-excel-add-in-and-word-add-in-be-made-available-to-users-using-centralized-deployment"></a>一元化配置を使用して、Excel アドインと Word アドインをユーザーが利用できるようにできますか。

はい、一元化配置はサポートされています。 詳細については、「[一元化配置](/office/dev/add-ins/publish/centralized-deployment)」を参照してください。 

一元化配置を使用するには、**Office アプリのパラメーター** ページの **アプリのパラメーター** タブで **アプリ ID**、**ストア**、**ストア タイプ** を変更します:

- **アプリ ID**: 61bcc63f-b860-4280-8280-3e4fb5ea7726
- **ストア**: EXCatalog
- **ストア タイプ**: 一元化配置

Office ストアへの戻しが必要な場合、標準値は次のとおりです:
- **アプリ ID**: WA104379629
- **ストア**: en-US
- **ストア タイプ**: Office ストア

> [!NOTE]
>- **名前**、**バージョン**、および **メモ** は情報を提供する値ですが、Excel アドインを実行するために必要ではありません。
>- これらの値は、ドキュメント テンプレートのフォームから実行されるときに Word アドインに対しても使用されます。

一部のユーザーに一元化配置で問題が発生した場合は、次のいずれかの問題が考えられます:
-   グループの 1 人以上のユーザーが、他よりも制限が厳しいメンバー
-   参照されたユーザーが別の Microsoft 365 アカウント (個人アカウントなど) にある

### <a name="what-is-the-cell-limit-for-the-excel-add-in"></a>Excel アドインのセル制限は何ですか。

既定の Excel アドインのセル制限は、Excel アドインが適度に高速なマシン上で処理できる上限の約半分になります。 マシンの速度は制限です。 問題が発生した場合は、セル制限を小さくし、そして / または、フィルターを調整してデータ セットを小さくする必要があります。 一般的な回避策として、フィルターを使用してデータを一度にもっと小さく管理することができます。

### <a name="how-do-i-make-an-entity-available-in-the-excel-add-in-andor-as-an-open-in-excel-option"></a>エンティティを Excel アドインまたは Excel で開くオプションとして使用できるようにするにはどうすればよいですか?

エンティティが "IsPublic = Yes" としてマークされており、固有の PublicEntityName と PublicCollectionName の値がある場合は、ODataサービス経由で使用できるようになります。 (できればGoogle Chromeで) 環境の $metadata フィード を調べることによって、同じ PublicEntityName と PublicCollectionName の値を持つ既存のエンティティがないことを確認します: https://*SomeFullEnvironmentURL*.dynamics.com/data/$metadata

### <a name="why-are-date-and-time-values-in-utc-in-the-excel-add-in"></a>Excel アドインで日付と時刻の値がUTCに設定されるのはなぜですか？

Excelアドイン、データ管理 フレームワーク、 Power BI レポートはすべて、データベース レベル で データと直接やり取りするように設計されています。 ユーザーのタイムゾーンに合わせて日付と時刻のデータを調整するクライアントが存在しないため、日付と時刻の値はすべて UTC となります。

### <a name="when-is-skype-integration-supported"></a>Skype 統合はいつサポートされますか?

Skype 統合は、パブリック クラウドの環境で利用できます。 オンプレミス環境を含む、パブリック クラウド外部の環境では、Skype 統合は現在サポートされていません。 

## <a name="troubleshooting-issues"></a>問題のトラブルシューティング

### <a name="issue-the-excel-add-in-loads-but-instead-of-showing-data-it-displays-load-applets-in-the-task-pane"></a>問題: Excel アドインを読み込むが、データが表示される代わりに、作業ウィンドウに「アプレットの読み込み」と表示される 

**問題:** Excel アドインを読み込みますが、データが表示される代わりに、作業ウィンドウに「アプレットの読み込み」と表示されます。 

**説明:** この問題は、通常、次のいずれかの理由によって発生します。

-   サインインが正しくない
-   環境でアドインの登録データが初期化されていない
-   OData の問題 

**固定:** 
-  **サインインが正しくない**: この問題の原因として最も考えられるのは、ユーザーが間違ったユーザーとしてサインインしている可能性があります。 これは、ユーザーが複数のアカウントを使用し、ブラウザーが間違ったユーザー コンテキストを使用している場合に発生する可能性があります。 他の修正を試す前に、右上隅のユーザー メニューを使用してアドインからサインアウトしてから、アドインに再度サインインします。 問題が引き続き発生する場合は、次の修正に記載されているように、登録データが適切に初期化されていることを確認してください。 

-  **登録データが初期化されない**: アドインに再度サインインしても問題が解決されなかった場合、別の潜在的な原因は、環境でアドイン データがまだ初期化されていないことです。 これを確認するために、管理者は **Office アプリ パラメーター** ページに移動できます。 そのページの各 **アプリ パラメータ**、**登録アプレット**、および **登録リソース** タブについて、各タブにデータが入力されていることを確認します。いずれかのタブに空のグリッドがある場合は、そのタブで適切な **初期化** ボタンを選択します。 

-  **OData の問題**: 前の 2 つの修正を試みても問題が解決しない場合、この問題の最終的な原因は、アドインが Finance and Operations と通信する OData サービスが、登録データをアドインに返すことができないことである可能性があります。 そのデータがない場合、アドインは、アプレットの読み込みに失敗します。 この段階で、失敗したセッションの Excel アドインの **アプリケーション相関関係 ID** からの情報を Microsoft サポートに連絡する必要があります。 このフィールドは **オプション** で見つけることができます。

### <a name="issue-during-sign-in-to-the-excel-add-in-users-receive-an-error-message-saying-they-cannot-access-the-application-2bc50526-cdc3-4e36-a970-c284c34cbd6e-in-that-tenant"></a>問題: Excel アドインへのサインイン中、ユーザーに「テナントのアプリケーション 2bc50526-cdc3-4e36-a970-c284c34cbd6e にアクセスできません」というエラー メッセージが表示される

**問題:** Excel アドインへのサインイン中、ユーザーに次のようなエラーが表示される。 
-  「AADSTS50020: ID プロバイダー https://sts.windows.net/XXX のユーザー アカウント 'XXX' はテナント 'XXX' に存在しないため、テナントのアプリケーション 2bc50526-cdc3-4e36-a970-c284c34cbd6e (Microsoft Business Office のアドイン) にアクセスできません。」
-  「選択したユーザー アカウントはテナント 'XXX' に存在しないため、テナントのアプリケーション 2bc50526-cdc3-4e36-a970-c284c34cbd6e にアクセスできません。」

**説明:** この問題は、外部ユーザーに関して 2021 年 4 月に Azure Active Directory (Azure AD) に行われた変更により発生します。 この変更は財務と運用アプリに対して行われたものではないので、すべてのバージョンのプラットフォームまたはアプリケーションの顧客に影響を与える可能性があります。  

**修正:** すべての外部ユーザーは、 Azure AD を通してテナントに招待される必要があります。 詳細については、[Azure Active Directory B2B コラボレーションを使用してユーザーを招待する](/power-platform/admin/invite-users-azure-active-directory-b2b-collaboration) を参照してください。

### <a name="fixed-issue-during-sign-in-to-the-excel-add-in-i-receive-the-following-error-message-aadsts65001-the-user-or-administrator-has-not-consented-to-use-the-application-with-id-xyz"></a>\[固定\] 問題: Excel アドインへのサインイン中に、次のエラー メッセージが表示されます: 「AADSTS65001: ユーザーまたは管理者が ID XYZ のアプリケーションを使用することに同意していません」

**問題:** Excel アドインへのサインイン中に、次のエラー メッセージが表示されます。「AADSTS65001: ユーザーまたは管理者が ID XYZ でアプリケーションを使用することに同意しませんでした」。

**説明:** 通常、この問題は、Microsoft Azure Active Directory (Azure AD) が Excel アドインを表す Azure AD アプリケーションを検出できないために発生します。 この問題は、[Microsoft Power BI のコンフィギュレーション](../analytics/configure-power-bi-integration.md)中に、アプリ ID URI が環境 URL に設定された Azure AD アプリケーションが追加されたために発生します。 

**修正**: Azure AD アプリケーションのアプリケーション ID URI が環境 URL に設定されていないことを確認します。 アプリ ID URI は、`https://contosoAXPowerBI` などの固有の URI で作成する必要があります。

### <a name="fixed-issue-during-sign-in-to-the-excel-add-in-i-receive-the-following-error-message-aadsts50001-the-application-named-abc-was-not-found-in-the-tenant-named-xyz"></a>\[固定\] 問題: Excel アドインへのサインイン中に、次のエラー メッセージが表示されます: 「AADSTS50001: ABC という名前のアプリケーションが XYZ という名前のテナントに見つかりませんでした」

**問題:** Excel アドインへのサインイン中に、次のエラー メッセージが表示されます。「AADSTS50001: XYZ という名前のテナントに ABC という名前のアプリケーションが見つかりませんでした」。

**説明:** この問題は、配置システムのエラーにより、環境がテナントのサービス プリンシパルのコンフィギュレーション済の一覧に追加されていない URL を取得したために発生している可能性があります。 

**修正:** 環境に関するサポート問題を提出し、問題を調査し、コンフィギュレーションを調整できるようにします。

### <a name="fixed-issue-after-the-excel-add-in-starts-and-updates-data-i-receive-the-following-error-message-an-error-occurred-while-writing-to-the-data-cache"></a>\[固定\] 問題: Excel アドインが起動してデータを更新した後、次のエラー メッセージが表示されます: 「データ キャッシュへの書き込み中にエラーが発生しました」

**問題:** Excel アドインを開始してデータを更新すると、次のエラー メッセージが表示されます。「データ キャッシュに書き込み中にエラーが発生しました」。 エラー状態の詳細は次の通りです。「引数が無効または不足している、またはフォーマットが正しくありません」 

**説明**: クライアントを Internet Explorer で開いていて、ユーザーが **Excel で開く** オプションを選択した直後に、**開く** をクリックすると、このエラー メッセージが表示されます。 Internet Explorer が一時的なインターネット ファイルを処理する方法は、Excel で問題を引き起こします。 この問題は、API 呼び出しの失敗の原因となります。 

**回避策:** Microsoft Edge または別の最新のブラウザを使用することをお勧めします。 これらのブラウザは、既定でファイルをダウンロード フォルダーに保存する傾向があるため、問題が軽減されます。 現在非推奨となっている Internet Explorer を使用している場合は、ブックを開くときに、最初に **保存** を選択してから、**開く** を選択します。 ファイルはダウンロード フォルダーから開かれます。  

**長期的な修正プログラム:** Office チームと協力してこの問題を理解し、Excel で解決できるようにしています。

### <a name="issue-vpn-users-see-a-blank-authentication-screen-when-trying-to-sign-into-the-excel-add-in"></a>問題: Excel アドインにサインインしようとする場合、VPN ユーザーに空白の認証画面が表示される

**問題**: 仮想プライベート ネットワーク (VPN) を使用しているユーザーは、認証ダイアログが空白で表示されるか、テキストが表示されないので、アドインにサインインできません。  

**修正**: VPN で実行しているときの VPN ソフトウェアまたはブラウザの設定により、マシンがリソースを取得したり、それらのリソースを正しく解釈したりできないため、この問題は顧客側から解決する必要があります。

VPN に関する一般的な解決策を次に示します。
-  ユーザーが次の場所にアクセスできることを確認します: [問題: Excel アドインが正しく実行されないか、サインインが有効にならない](#fixed-issue-the-excel-add-in-doesnt-correctly-run-or-enable-sign-in)。
-  ブラウザが Microsoft Edge (または Internet Explorer 11) の「互換性表示でイントラネット サイトを表示する」に設定されていないことを確認します。 これは組織ポリシーによって構成できます。 
-  影響を受けるユーザーに、VPN および Edge/IE ブラウザーの設定を影響を受けていない他のユーザーと比較してもらいます。

### <a name="fixed-issue-the-excel-add-in-doesnt-correctly-run-or-enable-sign-in"></a>\[固定\] 問題: Excel アドインが正しく実行されず、サインインが有効にならない

**問題:** ユーザーが Excel アドインにサインインしようとすると、認証ページの代わりに空白の認証ダイアログボックスが表示されるか、エラー メッセージが表示されます。 ユーザーがログインできません。 

**説明**: Excel アドインは、Office Web JS アドイン プラットフォームを依存し、認証に Azure AD を使用します。 プロキシを使用する場合、ユーザーが Excel アドインを実行してサインインするには、いくつかの URL にアクセスできる必要があります。 また、AD FS が使用される場合は、AD FS URL が HTTPS を使用する必要があります。 

**ソリューション:** この問題は顧客固有のネットワーク問題であるため、顧客固有の解決策が必要です。 AD FS が使用される場合は、AD FS URL が HTTPS を使用していることを確認します。 また、次のすべての URL がユーザーのコンピューターからアクセスできることを確認してください。

読み込みのために次の URL にアクセスします。

- `https://az689774.vo.msecnd.net:443`
- `https://az689774.vo.msecnd.net`
- `https://appsforoffice.microsoft.com:443`
- `https://appsforoffice.microsoft.com`
- `https://secure.aadcdn.microsoftonline-p.com:443`
- `https://secure.aadcdn.microsoftonline-p.com`
- `https://az416426.vo.msecnd.net:443`
- `https://az416426.vo.msecnd.net`
- `https://telemetryservice.firstpartyapps.oaspapps.com:443`
- `https://telemetryservice.firstpartyapps.oaspapps.com`
- `https://nexus.officeapps.live.com:443`
- `https://nexus.officeapps.live.com`
- `https://browser.pipe.aria.microsoft.com:443`
- `https://browser.pipe.aria.microsoft.com`
- `http://schemas.microsoft.com`

認証のために次の URL にアクセスします。

- `https://login.windows.net:443`
- `https://login.windows.net`
- `https://login.microsoftonline.com:443`
- `https://login.microsoftonline.com`


**代替ソリューション:** ユーザーが Windows 10 の古いバージョン (バージョン 1909 より前) を実行している場合は、Windows 10 をバージョン 1909 以降にアップグレードしてください。 バージョン 1909 では、KB5003635 が必要となる場合があります。 詳細については、[2021 年 5 月に解決された問題](/windows/release-health/resolved-issues-windows-10-1909#1610msgdesc)を参照してください。 

### <a name="issue-the-excel-add-in-needs-an-explicit-sign-out-after-encountering-an-aadsts50058-silent-sign-in-failed-error"></a>問題: AADSTS50058 "サイレント サインインが失敗しました" エラーが発生した後に、Excelアドインで明示的にサインアウトする必要がある。

**問題:** ユーザーが、一定期間操作が行われなかった後にExcelアドインにログインしようとすると、AADSTS50058 "サイレント サインインが失敗しました" というエラーが発生し、強制的にサインアウトが要求されます。

**説明:** Excelアドインは認証に Azure AD を使用します。 認証が行われると、ユーザーにトークンが作成されます。 このトークンには有効期限があります。 トークンの有効期限が切れると、AADSTS50058エラーが発生し "サイレントログインに失敗しました" という内容のが表示されます。

**解決策** : ユーザーは一度サインアウトしてから、再度サインインする必要があります。 この挙動については来的には改善をする予定です。自動的にユーザーをログアウトさせることで、より迅速なログインを実現します。

### <a name="issue-when-trying-to-use-a-document-template-with-open-in-excel-a-record-for-id-guid-not-found-error-displays"></a>問題: ドキュメント テンプレートを Excel で開いて使用しようとすると「ID GUID のレコードが見つかりません」エラーが表示される

**問題:** ある環境から別の環境にデータベースをコピーすると「ID GUIDのレコードが見つかりません」エラーが表示される場合があります。 

**説明:** データベースのコピーは Azure Blob Storage に保存されたドキュメント テンプレート、レコードの添付ファイル、その他のファイルに対して問題があります。 データベースをある環境から別の環境にコピーすると、ファイルはレコードとともにコピーされないため、アプリケーションがアクセスしようとするファイルが見つかりません。 

**解決策** : ドキュメント テンプレートの場合の解決策は、必要なテンプレートを特定してそのテンプレート ファイルのコピーをターゲット環境にロードすることです。

## <a name="additional-resources"></a>追加リソース

[Office 統合](office-integration.md)

[Office 統合のチュートリアル](office-integration-tutorial.md)

[Power BI 統合のコンフィギュレーション](../analytics/configure-power-bi-integration.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
