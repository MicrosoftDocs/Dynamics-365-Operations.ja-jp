---
title: イタリア用電子請求の使用を開始する
description: このトピックでは、イタリア向けの電子請求の使用を開始するにあたっての情報を提供します。
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 23cb0523b6d6d065ad19f6c3bddf881b0dc82a7d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840103"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a>イタリア用電子請求の使用を開始する

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> イタリア向けの電子請求は、現時点では Microsoft Dynamics 365 Finance および Dynamics 365 Supply Chain Management の電子請求書で利用できるすべての機能に対応していない可能性があります。 

このトピックでは、イタリア向けの電子請求の使用を開始するにあたっての情報を提供します。 このガイドでは、Regulatory Configuration Services (RCS) 、財務における、国ごとに異なる構成手順について説明します。 また、サービスを介してイタリア固有の **FatturaPA** 形式で生成された電子請求書を送信するための手順、および処理の結果を確認する方法についても説明します。

## <a name="prerequisites"></a>必要条件

このトピックの手順を実行する前に、 [電子請求の使用を開始する](e-invoicing-get-started.md)に記載の手順を完了する必要があります。

## <a name="rcs-setup"></a>RCS の設定

RCS の設定を行う際には、次の作業を実行します :

1. **FatturaPA** 形式で顧客の電子請求書をエクスポートする際に使用する電子請求書の機能をインポートします。
2. 電子請求書の作成、提出、回答の受信に必要な形式の構成を確認します。
3. 電子請求書の提出シナリオに対応したイベントを構成します。
4. 電子請求書機能を公開する。

> [!NOTE]
> "電子請求機能" は、電子請求書のアドオン サーバーを使用するように構成および公開されたリソースの総称です。 この場合は、顧客の電子請求書のエクスポートは、これから設定を行う電子請求書の機能となります。

## <a name="import-the-e-invoicing-feature"></a>電子請求書機能をインポートする

1. RCS アカウントにサインインします。
2. **グローバリゼーション機能** ワークスペースの **機能** セクションで、**電子請求書** タイルを選択します。
3. **電子請求書機能** ページで、**インポート** を選択して、グローバル レポジトリから電子請求書の機能をインポートします。

    > [!NOTE]
    > 利用可能な機能の一覧が表示されない場合は、**同期** を選択します。 

4. **電子請求書のエクスポート (IT)** 機能を選択し、**インポート** を選択し ます。

![電子請求書エクスポート (IT) 機能のインポート](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

**電子請求書エクスポート (IT)** 機能をグローバル レポジトリからインポートすると、次のセクションで説明されているすべての設定もインポートされます。

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a>電子請求書エクスポート (IT) 機能の新しいバージョンを作成する

1. **電子請求機能** ページの **バージョン** タブで、**新規** を選択します。 

    ![新しい電子請求書機能のバージョンを追加する](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    次に、電子請求書の機能に関連付けられている電子レポート (ER) の形式を構成します。

2. **構成** タブで、**追加** を選択して構成のバージョンを管理します。

    ![電子請求書機能の構成バージョンを管理する](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    この手順では、イタリアの電子請求書のエクスポートに使用されるさまざまなファイルの ER 形式を追加、構成します。 イタリアの FatturaPA 電子請求書では、次の標準的な構成を使用するか、電子請求書に使用する実際のカスタム構成を使用してください。

    - 売上請求書 (IT)
    - プロジェクト請求書 (IT)

    別の電子請求書機能から派生した電子請求機能を作成する場合、すべての ER 形式は元の機能から継承されます。

3. 特定の ER 形式ファイルの構成を選択します。
4. **編集** または **表示** を選択して **形式デザイナ** ページを開きます。

    ![形式デザイナー ページを開く](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. **形式デザイナー** ページを使用して、ER 形式ファイルの構成を編集、確認します。

    ![形式デザイナーのページ](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a>電子請求書機能の設定を管理する

- **電子請求機能**  ページの **設定** タブで、**追加** や **削除**、**編集** を選択して、電子請求機能の設定を管理します。

![電子請求書機能の設定を管理する](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

この手順では、電子請求書に適用するイベントを構成します。これには、**FatturaPA** 形式やデジタル署名 (必要な場合) における XML 出力ファイルの生成が含まれます。

### <a name="configure-the-sales-invoice-feature-setup"></a>売上請求書機能の設定を構成する

1. **電子請求機能** ページ上の **設定** タブで、**機能の設定** 列で、**売上請求書** を選択します。
2. **編集** を選択します。
3. **機能のバージョン設定** ページで、**アクション** タブを選択してアクションの一覧を管理します。 アクションは、イベントを完全に実行するために、順番に従って実行する必要がある操作の一覧を定義します。

    ![アクション タブ](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | アクション ID | アクション名        | アクション説明                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | 1         | ドキュメントの変換 | 電子請求書の XML ファイルを **FatturaPA** 形式で作成します。 |
    | 2         | ドキュメントに署名      | XML ファイルにデジタル署名を適用します。             |

4. 適用のルールを表示、管理するには、**適用ルール** タブを選択します。 適用ルールは、アクションが実行されるコンテキストを定義します。

    ![適合性ルール タブ](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. 変数を表示、管理するには、**変数** タブを選択します。

    ![変数タブ](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. アクションの実行に必要となるパブリック変数を定義します。

### <a name="configure-the-project-invoice-feature-setup"></a>プロジェクトの請求書機能の設定を構成する 

**プロジェクト請求書** 機能の設定の構成に必要な手順と設定は、**販売請求書** 機能の設定手順と設定方法と共通しています。 プロジェクト請求書を使用する場合は、売上請求書の手順を参照してください。

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a>環境にの電子請求書機能を割り当てる

1. **電子請求書機能** ページの **環境** タブで、**有効化** を選択します。
2. **環境** フィールドで、環境を選択します。
3. **有効開始** フィールドで、環境が有効になる日付を選択します。
4. **有効化** を選択します。 

![電子請求書環境を有効化する](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a>電子請求書の機能を公開する

電子請求書機能を公開するには、バージョンの状態を **完了**、または **公開済** に変更します。

### <a name="change-the-version-status-to-completed"></a>バージョンの状態を完了に変更する

1. **電子請求書機能** ページの **バージョン** タブで、状態が **下書き** となっている電子請求書機能のバージョンを選択します。
2. **ステータスの変更 \> 完了** を選択します。 

### <a name="change-the-version-status-to-published"></a>バージョンの状態を公開済みに変更する 

1. **電子請求書機能** ページの **バージョン** タブで、状態が **完了** となっている電子請求書機能のバージョンを選択します。
2. **状態の変更 \> 公開** を選択します。

![電子請求書機能の状態を変更する](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a>財務における電子請求統合を設定する

財務の設定を行う際には、次の作業を実行します :

1. ER データ モデル、ERデータ モデル マッピング、および FatturaPA 請求書のコンテキスト構成をインポートします。
2. イタリアの電子請求書にデジタル署名をするために必要となる証明書を構成します。

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a>ER データ モデル、データ モデル マッピング、形式をインポートする

1. **電子レポート** ワークスペースで、**ビジネス ドキュメント サービス** 構成プロバイダーが **有効** に設定されていることを確認します。
2. **リポジトリ** を選択します。
3. **グローバル リソース \>  開く** を選択します。
4. **請求書モデル**、**請求書モデルマッピング**、**顧客請求書コンテキスト モデル** をインポートします。

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a>イタリア向け顧客電子請求書のエクスポートを有効化する

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **機能** タブで、機能参照 **IT00036** 行の **有効** チェック ボックスをオンにします。

![FatturaPA 機能を有効にする](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a>電子ドキュメントを構成する

1. **組織管理 \> 設定 \> 電子ドキュメント パラメーター** に移動します。
2. **電子ドキュメント** タブで、**追加** を選択し、イタリア向けの電子請求書の生成に必要となるテーブルを入力します。

    - **テーブル名 :** 顧客請求書仕訳帳
    - **テーブル名 :** プロジェクト請求書

3. 各テーブルについて、関連するドキュメントのコンテキストを定義します :

    - **顧客請求書仕訳帳** で、**顧客請求書のコンテキスト** を選択します。
    - **プロジェクト請求書** で、**プロジェクト請求書のコンテキスト** を選択します。

![応答タイプを設定する](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a>電子請求書の処理

財務の処置を行う際には、次の作業を実行します :

1. 電子請求を介してイタリア向けの電子請求書を生成する
2. 実行ログを表示し、処理結果を確認する

### <a name="generate-electronic-invoices"></a>一般的な電子請求書

**構成可能な電子請求の統合** 機能を有効にして、**IT00036** 機能を有効にすると、イタリア向けの電子請求書を生成する従来の財務プロセスは使用できなくなります。 これは、**電子ドキュメントの送信** という名前の新しいプロセスによって置き換えられ ます。

電子請求書ドキュメントの要求に基づいてドキュメントを手動で送信することができます。

> [!NOTE]
> 続行する前に、イタリア向けの電子請求書に必要な設定が完了していることを確認してください。 詳細については、[顧客の電子請求書の作成](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices)を参照してください。 電子請求を有効化することで、そのトピックで説明されている一部の設定手順が使用できなくなる可能性があることに注意してください。

1. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの送信** に移動します。
2. ドキュメントを初めて送信する場合は、**ドキュメントの再送信** オプションを **いいえ** に設定します。 サービスを使用してドキュメントを再送信する必要がある場合は、このオプションを **はい** に設定します。
3. **含めるレコード** クイックタブで、**フィルター** を選択して **照会** ダイアログ ボックスを開きます。ここでは送信するドキュメントを選択するクエリを作成できます。

![電子ドキュメント ダイアログ ボックスの送信](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a>フィルター クエリ

1. **照会** ダイアログ ボックスで、売上請求書とプロジェクト請求書の両方のフィルター条件を構成する、または条件を空白のままにして未提出のすべての請求書をすべて含めるようにします。

    ![送信フィルター条件を設定する](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. **OK** を選択して **照会** ダイアログ ボックスを閉じます。
3. **OK** を選択し、選択したドキュメントを送信します。

> ![注記] このサービスを利用して初めて書類を提出する際は、電子請求との接続を確認するように促されます。 **ここをクリックして電子ドキュメント送信サービスに接続する** を選択します。

#### <a name="view-submission-logs"></a>送信ログの表示

全ての提出書類の提出ログを見ることができます。

1. **組織管理 \> 定期的 \> 電子ドキュメント  \> 電子ドキュメントの提出ログ** に移動します。
2. **ドキュメント タイプ** フィールドで、必要な電子ドキュメントをフィルタ処理する **顧客請求書仕訳帳**、または **プロジェクト請求書** を選択します。

    ![提出書類のログを表示するドキュメント タイプの選択](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    **提出状態** 列に表示される値は、提出プロセスの状態を表します。 これは、プロセスが構成通りに実行されたかどうか、追加のアクションが必要かどうかを示します。

3. アクション ウィンドウで、**照会\> 提出の詳細** を選択して、提出実行ログの詳細を表示します。

    ![提出書類ログの詳細を表示する](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. **処理中のアクション** クイックタブで、RCS で設定された機能のバージョンで構成されているアクションの実行ログを表示できます。 **状態** 列には、アクションが正常に実行されたかどうかが表示されます。
5. **アクション ファイル** のクイックタブでは、アクションの実行中に生成された中間ファイルを表示できます。 **表示** を選択すると、出力XMLファイルが **FatturaPA** 形式でダウンロードされ、その内容が表示されます。

## <a name="related-topics"></a>関連トピック

- [電子請求の概要](e-invoicing-service-overview.md)
- [電子請求の使用を開始する](e-invoicing-get-started.md)
- [電子請求の設定](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
