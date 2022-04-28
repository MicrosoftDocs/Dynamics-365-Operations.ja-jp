---
title: メキシコ用電子請求の使用を開始する
description: このトピックでは、メキシコ向けの電子請求の使用を開始するにあたっての情報を提供します。
author: gionoder
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6fc8a9eaf6c6e4c82719e7c1ebccd4272548e73f
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566002"
---
# <a name="get-started-with-electronic-invoicing-for-mexico"></a>メキシコ用電子請求の使用を開始する

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> メキシコ向けの電子請求は、現在のところ、Comprobante Fiscal Digital por Internet (CFDI) 文書で利用できるすべての機能、および Microsoft Dynamics 365 Finance や Dynamics 365 Supply Chain Management に組み込まれている関連する統合で利用できるすべての機能のすべてには対応していない場合があります。

このトピックでは、メキシコ向けの電子請求の使用を開始するにあたっての情報を提供します。 このガイドでは、Regulatory Configuration Services (RCS) 、財務における、国ごとに異なる構成手順について説明します。 また、サービスを介して CFDI の請求書を提出するために金融機関で行う必要のある手順や、処理結果や CFDI の請求書の状況を確認する方法についても説明します。

## <a name="prerequisites"></a>必要条件

このトピックの手順を実行する前に、[電子請求書発行サービスの運用を開始する](e-invoicing-get-started-service-administration.md)と[電子請求書を始める](e-invoicing-get-started.md)に記載の手順を完了する必要があります。

## <a name="set-up-the-cadena-xslt"></a>Cadena XSLT の設定

CFDI 処理のグローバル化機能に Cadena XSLT スキーマを追加するには、次の手順を実行します。

1. [SAT Web サイト](http://www.sat.gob.mx/sitio_internet/cfd/3/cadenaoriginal_3_3/cadenaoriginal_3_3.xslt)から スキーマをダウンロードします。
2. スキーマを ZIP ファイルに圧縮します。
3. 新しいコンテナ用にサービス環境に設定した Azure Storage アカウントに xslt ファイルを保存します。

## <a name="rcs-setup"></a>RCS の設定

RCS の設定を行う際には、次の作業を実行します :

1. CFDI の請求書を処理するための電子請求書機能をインポートします。
2. CFDI 請求書の作成、提出、回答の受け取り、取消の提出、回答の受け取りに必要なフォーマットの構成を確認します。
3. CFDI 請求書の提出シナリオに対応したイベントを構成します。
4. CFDI の請求書を処理するための電子請求書機能を公開します。

> [!NOTE]
> "電子請求機能" は、電子請求書のアドオン サーバーを使用するように構成および公開されたリソースの総称です。 この場合、CFDI 請求書 (MX) は、これから設定する電子請求書機能です。

## <a name="import-the-e-invoicing-feature"></a>電子請求書機能をインポートする

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求書** タイルを選択します。
3. **電子請求書機能** ページで、 **インポート** を選択して、グローバル レポジトリから **CFDI 請求書 (MX)** の機能をインポートします。

    > [!NOTE]
    > 機能が一覧に表示されない場合は、**同期** を選択し、手順3 を繰り返します。

![CFDI 請求書 (MX) 機能をインポートします。](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

グローバル レポジトリから **CFDI 請求書 (MX)** 機能をインポートすると、構成やアクションを含むすべての機能設定もインポートされます。

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a>CFDI請求書エクスポート (MX) 機能の新しいバージョンを作成する

たとえば、URL を更新する必要がある場合は、新しいバージョンを作成できます。 詳細については、[電子請求書 CFDI](tasks/mx-00010-e-invoicing-cfdi.md) を参照してください。

- **電子請求機能** ページの **バージョン** タブで、**新規** を選択します。

![新しい電子請求書機能のバージョンを追加します。](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a>構成のバージョンを更新する

1. **電子請求機能** ページの **構成** タブで、**追加** または **削除** を選択して、構成のバージョン (ER ファイル形式の構成) を管理します。

    ![電子請求書機能の構成を管理します。](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    新しいバージョンを作成すると、すべての構成が最後に発行されたバージョンから継承されます。 CFDI 請求書を処理するには、次のコ構成が必要となります :

    - CFDI 請求書 (BusinessDocumentService)
    - CFDI 応答メッセージのインポート
    - CFDI エラー ログのインポート
    - CFDI 取消申請 (MX) (BusinessDocumentService)
    - CFDI 請求書 (BusinessDocumentService)

2. 一覧で構成バージョンを選択し、**編集** または **表示** を選択すると、**形式デザイナ** ページが表示されます。このページで、構成の編集や表示をすることができます。

    ![形式デザイナー ページを開きます。](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. **形式デザイナー** ページを使用して、ER 形式ファイルの構成を編集、確認します。 詳細については、[電子ドキュメントのコンフィギュレーションの作成](../../fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration.md) を参照してください。

    ![形式デザイナー ページです。](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>電子請求書機能の設定を管理する

- **電子請求機能**  ページの **設定** タブで、**追加** や **削除**、**編集** を選択して、電子請求機能の設定を管理します。

![電子請求書機能の設定を管理します。](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

認証に使用する CFDI 請求書を送信するには (XML ファイルを生成し、XML ファイルを送信して応答を処理する) 、**売上請求書** 機能の設定が必要となります。

CFDI 請求書の取り消しを送信するには、**取り消し** 機能と **取り消し機能の設定** が必要です。

### <a name="configure-the-sales-invoice-feature-setup"></a>売上請求書機能の設定を構成する

1. **電子請求機能** ページ上の **設定** タブで、**機能の設定** 列で、**売上請求書** を選択します。
2. **編集** を選択し、アクションや適用ルール、変数を構成します。

    ![電子請求書機能の設定を編集します。](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. **機能のバージョン設定** ページで、**アクション** タブを選択してアクションの一覧を管理します。 アクションは、イベントを完全に実行するために、順番に従って実行する必要がある操作の一覧を定義します。

    ![アクション タブ。](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | アクション ID | 操作                   | アクション名                                  | アクション説明                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | 1         | ドキュメントを変換する       | CFDI デジタル署名を含まない電子請求書を生成する | CFDI 請求書を生成します。                                |
    | 2         | ドキュメントに署名            | デジタル署名                                 | 提出に使用する電子請求書にデジタル署名をします。                |
    | 3         | メキシコ PAC サービスの呼び出し | CFDI 電子請求書を送信する                        | Windows Communication Foundation (WCF) クライアントは、CFDI 電子請求書を送信します。 |
    | 4         | 応答の処理         | Web サービスの応答を分析する                 | Web サービスの応答を分析し、エラーログを返します。 |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a>Mexican PAC webサービスの URL を設定する 

1. **機能のバージョン設定**  ページで、**アクション** タブの  **アクション** クイックタブで、**メキシコ向け PAC サービスの呼び出し** を選択します。
2. **パラメーター** クイックタブの **URL アドレス パラメーター**  フィールドに、CFDI 電子請求書の提出に使用する webサービスの URL を入力します。

> [!NOTE]
> **取り消し** と **取り消し申請** 機能設定で使用する **メキシコ向け PAC サービス アクションの呼び出し** の URL を更新するには、同じ手順を使用します。

### <a name="set-up-the-path-for-the-cadena-xlst-schema"></a>Cadena XLST スキーマのパスを設定する

1. **機能バージョン設定** ページの **変数** タブで、変数名 **DigitalSignatureXSLT** を選択します。
2. **値** フィールド: {"containerUrl":"https://&lt;AccountStorageName&gt;.blob.core.windows.net/&lt;ContainerName&gt;","path":"&lt;RelativePath&gt;"}
   
    場所: \<RelativePath\> = フォルダ\\フォルダ\\ファイル名とダブル バックスラッシュ、ContainerName はサービスに使用されるコンテナを表す必要があります。
   
    変数の例は次のようになります:
    
    {"path":"xxxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx\\dev\\cadena_xslt","containerUrl":https://yyyyyyyyyy.blob.core.windows.net/containername}

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a>電子請求書の環境に下書きのバージョンを割り当てる

1. **電子請求書機能** ページの **環境** タブで、**有効化** を選択します。
2. **環境** フィールドで、環境を選択します。
3. **有効開始** フィールドで、環境が有効になる日付を選択します。
3. **有効化** を選択します。

![電子請求書の環境を有効化します。](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a>バージョンの状態を完了に変更する

1. **電子請求書機能** ページの **バージョン** タブで、状態が **下書き** となっている電子請求書機能のバージョンを選択します。
2. **ステータスの変更 \> 完了** を選択します。

## <a name="change-the-version-status-to-published"></a>バージョンの状態を公開済みに変更する

- **電子請求機能**  ページの **バージョン** タブで、**状態の変更 \> 公開** を選択します。

## <a name="publish-the-e-invoicing-feature"></a>電子請求書の機能を公開する

1. **電子請求書機能**  ページで、 **バージョン** タブを選択して、**CFDI 請求書 (MX)** 機能の状態を管理します。
2. **状態の変更** を選択して、機能の状態を変更します。

![電子請求書機能の状態を変更します。](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing--integration-in-finance"></a>財務における電子請求統合を設定する

財務で電子請求を設定するには、次の作業を行う必要があります :

1. ER データ モデル、ER データ モデル マッピング、および CFDI 請求書で必要となる形式をインポートします。
2. CFDI 請求書の更新に使用する応答タイプを構成します。 これらの応答タイプは、認定証明書プロバイダー (PAC) サーバーからの応答に使用されます。

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a>ER データ モデル、ERデータ モデル マッピング、CFDI 請求書で使用するコンテキスト構成をインポートする

1. 財務にログインします。
2. **電子レポート** ワークスペースの、**構成プロバイダー** セクションで、**Microsoft** タイトルを選択します。 この構成プロバイダーが **有効** に設定されていることを確認してください。 プロバイダーを **有効化** を設定する方法については、[構成プロバイダーを作成して有効化としてマークする](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md)を参照してください。
3. **リポジトリ** を選択します。
4. **グローバル リソース \>  開く** を選択します。
5. **請求書モデル**、**請求書モデル マッピング**、**CFDI 請求書形式 (MX)**、**CFDI 請求書の取消申請の形式 (MX)**、**CFDI 請求書の取消形式 (MX)** をインポートします。

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a>CFDI の請求書の処理に使用する機能を有効にする

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **機能** タブで、**MX-00010** と **MX-00016** の機能参照のそれぞれの行の **有効** チェック ボックスをオンにします。

![CFDI の請求書の処理に使用する機能を有効にします。](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a>ER の構成をインポートして CFDI 請求書の更新に使用する応答タイプを設定する

#### <a name="import-er-configurations"></a>ER コンフィギュレーションをインポートする

1. **電子レポート** ワークスペースの、**構成プロバイダー** セクションで、**Microsoft** タイトルを選択します。
3. **リポジトリ** を選択します。
4. **グローバル リソース \>  開く** を選択します。
5. **応答メッセージのインポート モデル**、**CFDI エラー ログ インポート (MX)**、**CFDI 応答メッセージのインポート (MX)** をインポートします。

#### <a name="set-up-the-response-types"></a>応答タイプを設定する

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **電子ドキュメント** タブで、**追加** を選択します。
3. 顧客請求書仕訳帳を入力し、**テーブル名** フィールドでプロジェクト請求書を選択します。
4. 各テーブルについて、関連するドキュメントのコンテキストを定義します :

    - **顧客請求書仕訳帳** に、**顧客請求書のコンテキスト** を入力します。
    - **プロジェクト請求書** に、**プロジェクト請求書のコンテキスト** を入力します。

4. **応答タイプ** を選択して、電子請求から返され、顧客の請求書仕訳帳やプロジェクトの請求書に含まれる応答タイプを構成します。
5. **新規** を選択し、続いて **応答タイプ** フィールドで、**応答** を選択します。
6. **提出の状態** フィールドで **保留** を選択します。
7. **モデル マッピング** フィールドで、**応答メッセージのインポート形式 - 応答メッセージからモデル マッピング** を選択します。
8. **保存** を選択します。
9. **新規** を選択し、続いて **応答タイプ** フィールドで、**ResponseData** を選択します。
10. **提出の状態** フィールドで **保留** を選択します。
11. **モデル マッピング** フィールドで、**CFDI 応答データのインポート形式 (詳細) - 応答データインポート** を選択します。
12. **保存** を選択します。

## <a name="process-electronic-invoices-in-finance"></a>財務での電子請求書の処理 

財務における CFDI 請求書の処理中には、電子請求を使用して次のタスクを実行できます :

- CFDI 請求書を送信します。
- 送信の実行ログを表示する。
- CFDI 請求書の取り消しを送信する。

### <a name="submit-cfdi-invoices"></a>CFDI 請求書の送信

**構成可能な電子請求の統合** 機能を有効化すると、CFDI 請求書の提出に使用する **電子請求書のエクスポート/インポート** 処理 (**売掛金勘定 \> 請求書 \> 電子請求書**) は使用できなくなります。 これは、**電子ドキュメントの送信** という名前の新しいプロセスによって置き換えられ ます。

> [!NOTE]
> 新しい **電子ドキュメントの送信** プロセスを使用する前に、メキシコ向けの電子請求書に必要な設定が完了していることを確認してください。 詳細については、[CFDI レイアウト バージョン 3.3](./latam-mex-cfdi-3-3.md) を参照してください。

1. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの送信** に移動します。
2. ドキュメントを初めて送信する場合は、必ず **ドキュメントの再送信** オプションを **いいえ** に設定してください。 サービスを使用してドキュメントを再送信する必要がある場合は、このオプションを **はい** に設定します。
3. **含めるレコード** クイックタブで、**フィルター** を選択して **照会** ダイアログ ボックスを開きます。ここでは送信するドキュメントを選択するクエリを作成できます。

![CFDI ドキュメントを送信します。](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> このサービスを利用して初めて書類を提出する際は、電子請求との接続を確認するように促されます。 **ここをクリックして電子ドキュメント送信サービスに接続する** を選択します。

### <a name="view-submission-logs"></a>送信ログの表示

すべての提出書類の提出ログ、または提出された提出書類のみのログを確認できます。

#### <a name="view-all-submission-logs"></a>すべての提出ログを表示する

**構成可能な電子請求の統合** 機能を有効にすると、ドキュメントの提出プロセスをフォローする新しいページが利用可能となります。 このページを使用して全ての提出書類の提出ログを確認することができます。

1. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。
2. **ドキュメント タイプ**  フィールドで、**顧客請求書仕訳帳** を選択して必要な電子ドキュメントをフィルター処理します。

    ![提出書類のログを表示するドキュメント タイプを選択します。](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。

    ![提出書類ログの詳細を表示します。](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

提出書類ログの情報は、次の3つのクイック タブに分かれています :

- **処理中のアクション** - このクイックタブでは、RCS で設定された機能のバージョンで構成されているアクションの実行ログが表示されます。 **状態** 列には、アクションが正常に実行されたかどうかが表示されます。
- **アクション ファイル** - こクイックタブでは、アクションの実行中に生成された中間ファイルが表示されます。 **表示** を選択する と、ファイルをダウンロードして表示できます。
- **アクション ログの処理** - このクイックタブには、電子請求とターゲットの web サービスの間の通信結果が表示されます。 また、web サービスからの処理によって返された内容が表示されます。 **エラーコード** 列には、web サービスの認証で返されたリターン コードが表示されます。

送信された CFDI 請求書が承認されると、その状態が **承認済** に更新されます。

#### <a name="view-submission-logs-from-cfdi-invoices"></a>CFDI 請求書から送信ログを表示する

**構成可能な電子請求の統合** 機能を有効にすると、CFDI 請求書から提出書類のログを表示することも可能です。

1. **売掛金勘定 \> 照会およびレポート\> CFDI (電子請求書)** の順に移動します。
2. **設定可能な電子請求の統合** 機能が有効にした後に送信された CFDI 請求書を選択します。
3. アクション ウィンドウの **履歴** タブで、**電子ドキュメント ログ** を選択します。

![CFDI 請求書から送信ログを表示します。](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> **構成可能な電子請求の統合** 機能が有効になる前に送信された請求書の場合は、**履歴** ボタンを使用できます。 **構成可能な電子請求の統合** 機能が有効になった後に送信された請求書の場合は、**履歴** ボタンは使用できません。

### <a name="submit-cancellation-of-cfdi-invoices"></a>CFDI 請求書の取り消しを送信する

**構成可能な電子請求の統合** 機能を有効化すると、CFDI 請求書の取り消しに使用する従来のプロセスが使用できなくなります。 **電子ドキュメントの送信ログ** ページに埋め込まれた新しい取り消しプロセスに置き換えられます。

1. **売掛金勘定 \> 照会およびレポート\> CFDI (電子請求書)** の順に移動します。
2. CFDI 請求書の状態が **承認済** の場合は、**機能 \> CFDI の取り消し** を選択します。
3. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。
4. CFDI 請求書を選択し、**機能 \> 関連する提出書類を送信する** を選択します。
5. 提出に関する説明を入力し、**OK** を選択します。

#### <a name="view-cancellation-submission-logs"></a>すべての取り消し提出ログを表示する

1. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。
2. **ドキュメント タイプ**  フィールドで、**顧客請求書仕訳帳** を選択し、顧客請求書仕訳帳ドキュメントをフィルター処理します。
3. CFDI 請求書を選択し、アクション ウィンドウで、**照会 \> 関連する提出書類** を選択します。

    **関連する提出書類** ページには、特定の CFDI 請求書に関連する提出書類とその提出書類の状態が表示されます。 次の図では、最初の行は、CFDI 請求書の承認を要求する提出書類を表します。 2 行目は、その CFDI 請求書を取り消しした提出書類を表します。

    ![取り消し提出ログを表示します。](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。

    ![提出書類の取り消しログの詳細を表示します。](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a>プライバシー通知
**CFDI メキシコの電子請求 (MX)** 機能を有効にするには、組織の税務登録 ID を含む一部のデータの送信が必要となる場合があります。 これは、政府の web サービスとの統合に必要な所定の形式で、この税務当局に電子請求書を送信する目的で、税務当局から権限を与えられた第三者機関に送信されます。 管理者は、**組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動して、**CFDI メキシコの電子請求 (MX)** 機能を有効または無効にすることができます。 **機能** タブを選択し、**CFDI メキシコの電子請求 (MX)** 機能を含む行を選択して、適切な選択を行います。 これらの外部システムから Dynamics 365 のオンライン サービスにインポートされたデータは、当社の [プライバシー ステートメント](https://go.microsoft.com/fwlink/?LinkId=512132) の対象となります。 詳細については、各国固有の機能説明書のプライバシーに関する注意事項を参照してください。

## <a name="additional-resources"></a>追加リソース

- [電子請求の概要](e-invoicing-service-overview.md)
- [電子請求の使用を開始する](e-invoicing-get-started.md)
- [電子請求の設定](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
