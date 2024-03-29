---
title: 財務と運用アプリの Data Lake にエクスポートする
description: この記事では、財務と運用アプリ環境でデータを選択して、Data Lake でデータの使用を可能にする方法について説明します。
author: MilindaV2
ms.date: 10/5/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 96283
ms.assetid: ''
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Platform Update 34
ms.openlocfilehash: f7669acd1d43845f2fb5fcce8e2304116a63c813
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631472"
---
# <a name="export-to-data-lake-in-finance-and-operations-apps"></a>財務と運用アプリの Data Lake にエクスポートする 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> **Data Lake へのエクスポート** 機能は通常、米国、カナダ、英国、ヨーロッパ、東南アジア、東アジア、オーストラリア、インド、ラテン アメリカ、および日本の地域で使用できます。 財務と運用環境がそれらの地域にある場合は、そこに **Data Lake にエクスポート** アドインをインストールできます。 将来的に Microsoft はその他の地域へもこの機能を追加していきます。 [Project Como Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=32768909312&view=all)に参加すると、連絡を取り合ったり、機能や今後の改善点を理解するのに役立つ質問をすることができます。

**Data Lake へのエクスポート** 機能を使用すると、財務と運用アプリから自分の Data Lake にデータをコピーできます (Azure Data Lake Storage Gen2)。 このシステムでは、含めるテーブルやエンティティを選択できます。 必要なデータを選択した後、システムが初期コピーを行います。 システムは、変更、削除、追加を適用することで、選択したデータを最新の状態に保ちます。 財務と運用アプリのインスタンスのデータを変更後、Data Lake でデータが使用可能になるまでには数分を要する場合があります。

## <a name="enable-the-export-to-data-lake-feature"></a>Data Lake へのエクスポート機能を有効にする
この機能を使用する前に、[Azure Data Lake アドインへのエクスポートをインストールする](configure-export-data-lake.md)を参照してください。

## <a name="select-data"></a>データの選択

> [!NOTE]
> この機能 **Azure Data Lake へのエクスポート** がご利用中の環境内の **機能管理** モジュールで使用できない場合、環境にサインインし、ブラウザのアドレスに以下の URL を追加してください: &mi=DataFeedsDefinitionWorkspace たとえば、`https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=DataFeedsDefinitionWorkspace`。

Data Lake にステージングする必要のあるテーブルとエンティティを選択することができます。

1. ご利用の環境で、**システム管理** \> **設定** \> **Data Lake にエクスポートする** へと移動します。

    ナビゲーション バーの検索フィールドを使用して、**Data Lake にエクスポート** ページを開くこともできます。 検索フィールドで、**構成** と入力します。 検索結果にはページへのリンクが含まれる必要があります。

2. **Data Lake へのエクスポート** ページの **テーブルの選択** タブで、Data Lake にステージングするデータ テーブルを選択します。 テーブルは、表示名またはシステム名のいずれかで検索できます。 テーブルが既に同期されているかどうかを確認することもできます。 
3. 完了後に、**テーブルの追加** を選択し、選択したテーブルを Data Lake に追加します。

    ![テーブルの選択。](./media/Export-Table-to-Data-lake-Tables-Running-state.png)

4. **データフィードの有効化** を選択し 、**OK** を選択します。 テーブルを追加すると、システムのステータスが **初期化** として表示される場合があります。 この状態は、データの初期コピーを作成していることを示します。 初期コピーが完了すると、状態が **実行中** に変更されます。

    エラーが発生した場合は、状態が **無効** として表示されます。

    状態が **実行中** の場合、Data Lake でデータを消費できます。 **初期化** または **無効化** 状態の間に Data Lake でデータを使用している場合は、一部のデータが表示されないことがあります。 

    必要な特定のテーブルについて詳しくない場合は、エンティティを使用してテーブルを選択することができます。 エンティティはデータの抽象度が高く、複数のテーブルを含む場合があります。 エンティティを選択することで、それを構成するテーブルも選択することになります。

    > [!NOTE]
    > **エンティティを使用して選択** タブを初めて開いた場合、ページのエンティティの一覧が空白である場合があります。 システムは、エンティティの一覧に入力するのに時間がかかる場合があります。 アクション ウィンドウで **管理 \> データ フィード カタログの再構築** を選択すると、リストを強制的に更新できます。 

5. **使用するエンティティの選択** タブでエンティティを選択し、**エンティティを使用してテーブルを追加する** を選択します。

    ![エンティティを使用したテーブルの選択。](./media/Export-Table-to-Data-lake-Entities-Running-state.png)

    テーブルを選択する方法を問わず、テーブルは Data Lake にステージングされます。

## <a name="monitor-the-tables-in-the-data-lake"></a>Data Lake のテーブルを監視する

システムが Data Lake でデータの更新をし続けるため、データのエクスポートの監視や、スケジュールを設定する必要はありません。 **Data Lake へのエクスポート** ページの **状態** 列で、進行中のデータ エクスポートの状態を確認することができます。 

データを選択すると、Azure Data Lake へのエクスポート サービスは、Data Lake 内のデータの初期コピーを作成します。 複数のテーブルを選択する場合、システムは一度に 10 個のテーブルを取得して初期コピーを作成します。 データのサイズやテーブル内のレコード数によっては、このプロセスに数分または数時間かかる場合があります。 エクスポートの進行状況が画面に表示されます。

初期コピーが作成された後、財務と運用アプリで変更が行われると、システムによってデータが継続的に更新されます。 レコードの挿入、更新、または削除を行う場合、Data Lake 内のデータ レコードは、それに応じて挿入、更新、または削除されます。

オプションのほぼリアルタイムの変更機能 (現在プレビュー中) を使用すると、財務と運用環境の変更から数分以内に Data Lake 内のデータは更新されます。 それ以外の場合は、財務と運用環境内の変更から数時間以内に Data Lake 内のデータは更新されます。

財務と運用環境にある Data Lake へのエクスポートのページは、Data Lake 内のデータが最後に更新された時のタイム スタンプを表示します。 システムは、Data Lake 内のデータが更新された時刻を識別するのに役立つデータ フィールドも追加します。 ダウンストリーム プロセスでは、タイム スタンプを使用して、Data Lake 内で変化するデータを検出して処理できます。

## <a name="troubleshooting-common-issues-and-errors"></a>一般的な問題とエラーに対するトラブルシューティング

### <a name="export-to-data-lake-feature-is-not-available-in-your-region-andor-your-environment-at-this-time"></a>Data Lake へのエクスポート機能が表示されない場合は、この機能がご利用の環境や地域で対応していないことを意味します
この機能は、Tier 1 (開発者) 環境では使用できません。 バージョン 10.0.13、またはそれ以上のプラットフォーム更新プログラムを含むサンドボックス環境 (Tier 2 またはそれ以降) が必要です。

この機能は、財務と運用アプリが利用可能なすべての Azure リージョンで利用できない場合や、ご使用の環境によっては利用できない場合があります。 今後のプレビューに参加する場合は、[アンケートを完了します](https://aka.ms/FnODataLakePreviewSurvey)。 参加の準備ができ次第、ご連絡いたします。 アンケートを完了すると、Yammer グループに参加することもできます。 Yammer グループを使用して、機能を理解するのに役立つ質問をお伝えすることができます。 この機能をご利用頂けるよう対応いたします。

### <a name="export-to-data-lake-feature-is-currently-being-installed-for-your-environment-please-check-back-later"></a>Data Lake へのエクスポート機能は、ご利用の環境にインストールされています。 後でもう一度ご確認ください。
この機能を使用する前に、Data Lake へのエクスポートを構成する必要があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-add-in-is-not-installed"></a>Data Lake アドインへのエクスポート機能がインストールされていません。 
Dynamics Lifecycle Services (LCS) を使用してこのアドインをインストールする場合は、管理者に問い合わせてください。 この機能を使用する前に、Data Lake へのエクスポートを構成する必要があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-feature-failed-to-install-in-dynamics-life-cycle-services-lcs"></a>Data Lake へのエクスポート機能は、Dynamics Life Cycle Services (LCS) へのインストールに失敗しました。 
Data Lake アドインへのエクスポート機能を再インストールするには、管理者に問い合わせてください。 問題が解消しない場合は、サポートにお問い合わせください。 Data Lake へのエクスポート機能を構成した際に、エラーが表示される場合があります。 または、ご利用の環境の変更がされている場合は、構成後に Data Lake にアクセスした際にエラーが発生する場合があります。 詳細については、[Azure Data Lake へのエクスポートの構成](configure-export-data-lake.md)を参照してください。

### <a name="export-to-data-lake-feature-is-temporarily-unavailable-please-check-back-later"></a>Data Lake へのエクスポート機能は、一時的に使用できなくなります。 後でもう一度ご確認ください。
このエラーが長時間継続するする場合は、サポートに連絡してください。  

### <a name="memo-fields-are-missing-in-the-data-lake"></a>Data Lake にメモ フィールドがない
システムは、メモ タイプ、nVarchar(max)、VarBinary、または Blob タイプのフィールドを Data Lake にエクスポートしません。 これらのタイプのフィールドを含むテーブルを選択した場合、システムはそれらのフィールドを無視し、他のフィールドをエクスポートします。 将来そのような特殊なフィールドも可能になるように取り組んでいます。 製品チームと連絡を取り合い、更新機能について知りたい場合は [Project Como Yammer グループ](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=32768909312&view=all)に参加することができます。

### <a name="status-codes-with-extended-errors"></a>拡張エラーを含むステータス コード
Data Lake へのエクスポートに追加したテーブルでエラーが発生すると、ステータス列にエラー コードが表示される場合があります。 次のエラー コードは、エラーの原因と問題の修正方法を示します。

#### <a name="error-status-codes-4xx-indicate-an-issue-with-the-table"></a>エラー ステータス コード 4xx は、テーブルに関する問題を示します

| エラー コード | 出庫                                                                  | 次のステップ                                                                                                                                                                                                                                                                                                                                                                     |
|------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 400        | 追加したテーブルには RecID フィールドが含まれていません。                   | RecID フィールドは、システムによりテーブル データをインデックス化するために使用されます。 RecID フィールドを含まないテーブルは、Data Lake に追加できません。 この問題が財務と運用アプリのテーブルからの問題である場合は、Microsoft サポートにお問い合わせください。 このテーブルがパートナーまたは ISV によって開発された場合は、RecID フィールドを含めるよう、開発者にお問い合わせください。                                  |
| 401        | 追加したテーブルがデータベースにありません。 | 追加したテーブルがデータベースで使用できなくなり、システムはレイクでデータの更新を続行できません。 ソフトウェアまたはデータベースの更新が原因で、このテーブルが削除された可能性があります。 この問題を解決するには、データベース管理者または開発者にお問い合わせください。 このテーブルがパートナーまたは ISV によって開発された場合は、開発者にお問い合わせください。  <br><br> この問題は、DirPerson テーブルなどの「派生テーブル」を追加する場合にも発生する可能性があります。 現在、このサービスでは、派生テーブルはサポートされていません。 派生テーブルを選択するには、ベース テーブルを選択する必要があります。 将来のリリースで派生テーブルのサポートが追加される予定です。               |
| 402        | RecID フィールドがインデックス化されません。                                            | システムにより、テーブルに含まれる RecID フィールドがインデックスの一部ではないか、インデックスの最初のフィールドではないことが検出されました。 これにより Data Lake の更新でのパフォーマンスが低下し、更新が Data Lake に反映されるのに時間がかかる可能性があります。 この問題を解決するために、インデックスに RecID フィールドを含めることができます。 この問題が財務と運用アプリのテーブルからの問題である場合は、Microsoft サポートにお問い合わせください。 このテーブルがパートナーまたは ISV によって開発された場合は、開発者にお問い合わせください。 |
| 409        | アクセス許可が原因で、ストレージ アカウントにアクセスできません。 ストレージ アカウントのコンフィギュレーションを確認します。      | システムはストレージ アカウントにアクセスして書き込むことができません。 階層の名前空間 (HNS) が有効になっていることを確認し、アクセス ロールを検証してください。 詳細については、[Azure Data Lake へのエクスポートのコンフィギュレーション - アクセス権の付与](configure-export-data-lake.md#grantaccess)を参照してください。 この問題を解決するには、システムを構成したシステム管理者または LCS 管理者に連絡してください。 |
| 410        | Data Lake にアクセスするためのアプリケーション ID の検出に失敗しました。 指定されたアプリケーション ID が正しくない、または見つかりません。      | Key Vault で指定されたアプリケーション ID が Azure Active Directory で見つかりません。 [Azure Data Lake へのエクスポートのコンフィギュレーション - 申請書の作成](configure-export-data-lake.md#createapplication)に記載の手順に従って、Key Vault で指定されたアプリケーション ID を検証します。 |
| 411        | 指定されたアプリケーション ID とアプリケーション シークレットで Data Lake にアクセスできませんでした。 | 指定されたアプリケーション ID (app-id) とアプリケーション シークレット (app-secret) は、ストレージ アカウントへのアクセスには使用できません。 [Azure Data Lake へのエクスポートのコンフィギュレーション - 申請書の作成](configure-export-data-lake.md#createapplication)に記載の手順に従って、アプリケーション ID とアプリケーション シークレットが有効であることを確認します。 <br><br> 次に、ストレージ アカウントに必要なアクセス権を持っているかどうかを確認します。 詳細については、[Azure Data Lake へのエクスポートのコンフィギュレーション - アクセス権の付与](configure-export-data-lake.md#grantaccess)を参照してください。 システムを構成したシステム管理者または LCS 管理者に連絡する必要があります。 | 
| 412        | 選択したテーブルがサポートされていないか、RecID インデックスがありません。 | 一部の内部テーブルおよびシステム テーブルは、Data Lake へのエクスポート機能でサポートされていません。 このエラーが表示された場合は、許可されないテーブルを選択した可能性があります。 将来的に、選択フォームにそのようなテーブルが表示されなくなる可能性があります。 サポートされているテーブルを使用して同じ情報を抽出するように計画する必要があります。 <br><br> 選択したテーブルに多数の行 (100 万以上) が含まれていて、必要な RecID インデックスが存在しない場合にも、このエラーが発生する可能性があります。 システムでは、RecID がインデックスの最初のフィールドであるインデックスを格納するために、より大きなテーブルが必要です。 このエラーを解決するために、テーブル拡張子として RecID インデックスを作成することができます。 | 
| 415        | Key Vault で指定されているストレージ名を使用してストレージ アカウントにアクセスできませんでした。 | Key Vault で指定されているストレージ アカウントが見つからない、または無効です。 [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](configure-export-data-lake.md#addsecrets)に記載の手順に従って、正しいストレージ アカウント名が Key Vault に入力されていることを確認します。 <br><br> [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](configure-export-data-lake.md#addsecrets)に記載の手順に従って、ストレージ アカウントに正しいシークレット名が指定されていることを確認します。 | 
| 420        | Key Vault または Key Vault のシークレットにアクセスできませんでした。 | サービスは、Key Vault または Key Vault のシークレットにアクセスできません。  Azure サブスクリプションの有効期限が切れていないことを確認します。 <br> <br> [Azure Data Lake へのエクスポートのコンフィギュレーション - サービス プリンシパルの作成](configure-export-data-lake.md#createServicePrincipal)に記載の手順に従って、サービス プリンシパルが作成されていることを確認します。 <br> <br> [Azure Data Lake へのエクスポートのコンフィギュレーション - シークレットの追加](configure-export-data-lake.md#addsecrets)に記載の手順に従って、Key Vault に必要なシークレットがすべて含まれていることを確認します。 <br><br> [Azure Data Lake へのエクスポートのコンフィギュレーション - アドインのインストール](configure-export-data-lake.md#installaddin)の構成手順で、正しい Key Vault URI が指定されていることを確認します。 | 
| 425        | 環境の Azure テナント ID の検索に失敗しました。 | [Azure Data Lake へのエクスポートのコンフィギュレーション - アドインのインストール](configure-export-data-lake.md#installaddin)に記載の手順に従って、正しい Azure テナント ID が指定されていることを確認します。  | 
| 430        | 環境にアクセスできませんでした。 | 環境が使用可能で、削除されているまたは無効な状態でないことを確認します。  |
| 435        | レイク内のファイルが破損している、または無効です。 | システムにより、Data Lake 内で破損したファイルまたは無効なフォルダー構造が検出されました。 システムは、コンフィギュレーションで指定されたレイク内のファイルとフォルダーを管理します。 Data Lake 内のファイルやフォルダー構造を自分で変更しないでください。 ユーザーまたはプロセスがレイク内のファイルまたはフォルダーを変更していないことを確認します。 テーブルを再有効化して、問題が解決されているかどうか確認することができます。 問題が解決しない場合は、Data Lake アドインへのエクスポート機能をアンインストールしてから再インストールしてください。  |
| 439        | 選択したテーブルに対する拡張メタデータを、システムが見つけられません | 財務と運用のバージョンを 10.0.28 (PU52) に更新し、**管理 > メタデータの再発行** オプションを使用してメタデータを手動で更新する必要があります。 このオプションの後、数分間待って、問題が解決されたかどうかを確認する必要があります。      |
| 440        | この環境で拡張メタデータをシステムが見つけられません | "拡張メタデータの強化" 機能を選択した場合、このエラーが表示されます。 この場合、システムが拡張メタデータを見つけられません。 この問題を解決するには、財務と運用のバージョン 10.0.28 (PU52) 以降がインストールされていることを確認してください。 適切なバージョンを使用している場合は、**管理 > メタデータの再発行** オプションを使用してメタデータを手動で更新することもできます。 このオプションの後、数分間待って、問題が解決されたかどうかを確認する必要があります。  |


#### <a name="error-status-codes-5xx-indicate-a-system-error-encountered-while-exporting-data"></a>エラー ステータス コード 5xx は、データのエクスポート中にシステム エラーが発生することを示します
エラーが原因で、システムによるデータのエクスポートが一時停止しました – レイクに存在するデータは、エラーが解決されるまで更新されません。 テーブルを無効化および有効化して、これにより問題が解決されるかどうか確認してください。 テーブルを無効化および有効化すると、システムが完全なコピーを取ってレイク内のデータが再初期化される場合があることに注意してください。 それでも問題が解消しない場合は、テーブル名とエラー コードを手元に用意して Microsoft サポートにお問い合わせください。

#### <a name="error-status-codes-8xx-indicates-an-issue-with-finance-and-operations-apps-database"></a>エラー状態コード 8xx は、財務と運用アプリのデータベースの問題を示します 
Microsoft Azure Data Lake 機能へのエクスポートは、財務と運用アプリ データベースの変更データ キャプチャ機能を使用します。 エラー 8xx は、財務と運用アプリ データベースの変更データ キャプチャ機能の問題を示します。 これの原因は、データベース保守操作の結果、またはデータベース操作に影響を与える別の問題である可能性があります。 この問題の解決にサービス管理チームが積極的に取り組んでおり、お客様のアクションは必要ありません。 問題が解決しない場合は、Microsoft サポートに更新プログラムを依頼してください。 

#### <a name="error-status-codes-9xx-indicate-an-issue-with-finance-and-operations-environment"></a>エラー状態コード 9xx は、財務と運用環境の問題を示します
エラー コード 9xx は、財務と運用環境にともなうシステム構成の問題を示します。 この問題の解決にサービス管理チームが積極的に取り組んでおり、お客様のアクションは必要ありません。 問題が解決しない場合は、Microsoft サポートに更新プログラムを依頼してください。
                                                                                                                                                                    |

> [!NOTE]
> テーブルを無効化および有効化すると、システムが完全なコピーを作成してレイク内のデータが再初期化される場合があります。 これが大きなテーブルの場合、初期化プロセスに時間がかかる可能性があります。 今後システムは、テーブル構造の変更を反映するため、レイク内のデータの更新を自動的に行う可能性があります。 



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

