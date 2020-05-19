---
title: 実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する
description: このトピックでは、構成されたデータ フローと変換をよりよく理解するために、実行された ER 形式のデータ ソースをデバッグする方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 5b51c4beac0ddf1e2b53fe300e10c0f608e5d1e1
ms.sourcegitcommit: 153bb33722c02501bf7bcfd56ac887602d5dfbd3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2020
ms.locfileid: "3318669"
---
# <a name="debug-data-sources-of-an-executed-er-format-to-analyze-data-flow-and-transformation"></a>実行された ER 形式のデータソースをデバッグして、データ フローや変換を解析する

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/preview-banner.md)]

電子レポート（ER）ソリューションを [構成](tasks/er-format-configuration-2016-11.md) してアウトバウンド文書を生成する場合、アプリケーションからデータを取得し、生成される出力にデータを入力するために使用する方法を定義します。 ER ソリューションのライフ サイクル サポートをより効率的には、ご利用のソリューションを、ER [データモデル](general-electronic-reporting.md#DataModelComponent) とその [マッピング](general-electronic-reporting.md#ModelMappingComponent) コンポーネント、および [ER](general-electronic-reporting.md#FormatComponentOutbound)フォーマットとそのマッピング コンポーネントで構成する必要があります。モデル マッピングがアプリケーション固有のものであるのに対し、他のコンポーネントはアプリケーションに依存しないようにしてください。 したがって、一部の ER コンポーネントは、生成された出力にデータを入力するプロセスに [影響を与える](general-electronic-reporting.md#FormatComponentOutbound) 場合があります。

生成された出力のデータは、アプリケーション データベースの同じデータとは異なる場合があります。 そのような場合は、どの ER コンポーネントがデータ変換を担当しているかを特定する必要があります。 ER データソース デバッガー機能を実行すると、この調査に必要な時間と費用を大幅に削減できます。 ER 形式の実行を中断して、データソース デバッガ インターフェイスを開くことができます。 この機能では、使用可能なデータソースを参照し、実行する個別のデータソースを選択できます。 この手動実行では、ER 形式の実稼働中にデータソースの実行をシミュレートします。 結果は、受信したデータを分析するページに表示されます。

データソースのデバッグ機能を有効にするには、ER ユーザー パラメーターで、**形式実行時にデータのデバッグを有効にする** オプションを **はい** に設定します。 その後、ER 形式を実行してアウトバウンド ドキュメントを生成する際に、データソースのデバッグを開始できます。 **デバッグを開始する** オプションを使用して、[ER オペレーション デザイナー](./tasks/er-format-configuration-2016-11.md#design-the-format-of-an-electronic-document) で構成された ER 形式のデータソースのデバッグを開始することもできます。

このトピックでは、実行された ER 形式のデータソース デバッグを開始するためのガイドラインを示します。 ここでは、データフローとデータ変換を理解する上で、どのような情報が役立つのかを解説しています。 このトピックでは、仕入先支払処理の業務プロセスを例として使用します。

## <a name="limitations"></a>制限

データソースデバッガーを使用すると、送信ドキュメントの生成時に実行する ER 形式のデータソース内のデータにアクセスできます。 インバウンド ドキュメントの解析に使用する ER 形式のデータソースのデバッグには使用できません。

次の ER 形式の設定は、現在データソース デバッグでは使用できません。

- 形式の変換
- 形式とマッピングの検証ルール
- 式を有効にする
- イン メモリ データ コレクションの詳細

## <a name="prerequisites"></a>必要条件

- このトピックの例を完了するには、次のいずれかの [ロール](../sysadmin/tasks/assign-users-security-roles.md) にアクセスできる必要があります：

    - 電子申告開発者
    - 電子申告機能コンサルタント
    - システム管理者

- この会社は、**DEMF** に設定する必要があります。

- このトピックの [付録1](#appendix1) の手順に従って、仕入先支払の処理に必要となる Microsoft ER ソリューションのコンポーネントをダウンロードします。
- 本トピックの [付録2](#appendix2) に記載の手順に従って、ダウンロードした ER ソリューションを使用して、ベンダーの支払い処理のための買掛金を準備してください。

## <a name="process-a-vendor-payment-to-get-a-payment-file"></a>仕入先の支払いを処理して支払いファイルを取得する

1. 本トピックの [付録3](#appendix3) に記載の手順に従って、仕入先の支払いを処理します。

    ![仕入先の支払い処理中](./media/er-data-debugger-process-payment.png)

2. ZIP ファイルをご利用のコンピューターにダウンロード し、保存します。
3. ZIP ファイルから **ISO20022 Credit transfer.xml** 支払ファイルを抽出します。
4. XML ファイル ビューアーを使用して、抽出した支払ファイルを開きます。

    支払ファイルでは、仕入先の銀行口座の国際銀行口座番号 (IBAN) コードにスペースが含まれていません。 したがって、**銀行口座**ページで [入力](#enteredIBANcode) した値とは異なります。

    ![空白のない IBAN コード](./media/er-data-debugger-payment-file.png)

    ER データソースデバッガーを使用して、ER ソリューションのどのコンポーネントが IBAN コードのスペースの切り捨てに使用されているかを説明します。

## <a name="turn-on-data-source-debugging"></a>データソースのデバッグを有効にする

1. **組織管理** \> **電子申告** \> **構成**の順に移動します。
2. **構成**ページ、アクション ウィンドウ、**構成**タブ、**詳細設定**グループで、**ユーザー パラメーター**を選択します。
3. **形式実行時にデータのデバッグを有効にする**オプションを **はい** に設定します。

    > [!NOTE]
    > このパラメーターはユーザーに固有のものまたは会社固有のものであることに注意してください。

    ![ユーザー パラメーター ダイアログ ボックス](./media/er-data-debugger-user-parameters.png)

## <a name="process-a-vendor-payment-for-debugging"></a>仕入先支払の処理のデバッグ

1. 本トピックの [付録3](#appendix3) に記載の手順に従って、仕入先の支払いを処理します。
2. メッセージ ボックスで、**はい** を選択して、仕支入の支払い処理を中断し、代わりに**デバッグ データソース** のページでデータ ソースのデバッグを開始することを確認します。

    ![確認用メッセージボックス](./media/er-data-debugger-start-debugging.png)

## <a name="debug-data-sources-that-are-used-in-payment-processing"></a>支払処理に使用されるデバッグ データ ソース

### <a name="debug-the-model-mapping"></a>モデル マッピングのデバッグ

1. アクション ウィンドウの **デバッグ データソース** で、**モデル マッピング** を選択してこの ER コンポーネントからデバッグを開始します。
2. 左側の [データソース] ウィンドウで、**\$notSentTransactions** データソースを選択し、**すべてのレコードの読み取り** を選択します。

    **1 レコードの読み取り**、**10 レコードの読み取り**、**100 レコードの読み取り**、または**すべてのレコードの読み取り** を選択して、選択したデータ ソースから適切な数のレコードを強制的に読み取ることができます。 このように、実行中の ER 形式からデータソースへのアクセスをシミュレートすることができます。

3. 右のデータ ウィンドウで、**すべて展開する** を選択します。

    **レコード リスト** タイプの選択されたデータソースに 1 つのレコードが含まれていることがわかります。

4. **\$notSentTransactions** データソースを展開し、入れ子になった **vendBankAccountInTransactionCompany()** メソッドを選択します。
5. **vendBankAccountInTransactionCompany()** メソッドを展開し、入れ子になった **IBAN** フィールドを選択します。
6. **値の取得** を選択します。

    **値の取得**  を選択すると、選択したデータソースの選択したフィールドの値を読み取ることができます。 このように、実行中の ER 形式からこのフィールドへのアクセスをシミュレートすることができます。

7. **すべて展開**を選択します。

    ![モデル マッピングの IBAN フィールドの値](./media/er-data-debugger-debugging-model-mapping.png)

    このように、仕入先の銀行口座に対して返される IBAN コードにスペースが含まれているため、モデル マッピングではスペースが切り捨てられることはありません。 したがって、データ ソースのデバッグを続行する必要があります。

### <a name="debug-the-format-mapping"></a>形式マッピングのデバッグ

1. アクション ウィンドウの **デバッグ データソース** で、**形式のマッピング** を選択してこの ER コンポーネントからデバッグを継続します。
2. **\$PaymentByDebtor** データソースを選択し、**すべてのレコードの読み取り** を選択します。
3. **\$PaymentByDebtor** を展開します。
4. **\$PaymentByDebtor.Lines** を展開し 、**すべてのレコードの読み取り** を選択します。
5. **\$PaymentByDebtor.Lines.CreditorAccount** を展開します。
6. **\$PaymentByDebtor.Lines.CreditorAccount.Identification** を展開し、**\$PaymentByDebtor.Lines.CreditorAccount.Identification.IBAN** を選択します。
7. **値の取得** を選択します。
8. **すべて展開**を選択します。

    ![形式マッピングの IBAN フィールドの値](./media/er-data-debugger-debugging-format-mapping.png)

    このように、仕入先の銀行口座に返されるIBANコードにはスペースが含まれているため、形式マッピングのデータソースはスペースの切り捨てに責任を負いません。 したがって、データ ソースのデバッグを続行する必要があります。

### <a name="debug-the-format"></a>形式のデバッグ

1. アクション ウィンドウの **デバッグ データソース** で、**形式** を選択してこの ER コンポーネントからデバッグを継続します。
2. 形式の要素を展開して **20022** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** を選択し、**すべてのレコードの読み取り** を選択します。
3. 形式の要素を展開して **ISO20022CTReports** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** を選択し、**すべてのレコードの読み取り** を選択します。
4. 形式の要素を展開して **ISO20022CTReports** \> **XMLHeader** \> **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** を選択し、**値を取得する** を選択します。
5. **すべて展開**を選択します。

    ![形式の IBAN フィールドの値](./media/er-data-debugger-debugging-format.png)

   このように、仕入先の銀行口座に対して返される IBAN コードにスペースが含まれているため、形式のバインドではスペースが切り捨てられることはありません。 したがって、**BankIBAN**要素は、スペースを切り捨てる形式変換を使用するように構成されます。

6. データ ソース デバッガーを閉じます。

### <a name="review-the-format-transformations"></a>形式の変換を確認する

1. **組織管理** \> **電子申告** \> **構成**の順に移動します。
2. **構成** ページで、**支払モデル** \> **ISO20022 クレジット転送** を選択します。
3. **デザイナー** を選択し、続いて要素を展開して **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** を選択します。

    ![形式デザイナー ページの BankIBAN 要素](./media/er-data-debugger-referred-transformation.png)

    このように、**BankIBAN** 要素は、**英数字以外を削除** するように構成されています。

4. **変換** タブを選択します。

    ![BankIBAN 要素が使用する変換タブ](./media/er-data-debugger-transformation.png)

    このように、**英数字以外の** 変換は、提供されたテキスト文字列からスペースを切り捨てる式を使用するように構成されています。

## <a name="start-to-debug-in-the-operation-designer"></a>操作デザイナーでデバッグを開始する

ER 形式の下書きバージョンを操作デザイナーから直接実行できるように構成した場合は、アクション ウィンドウで **デバッグの開始** を選択することにより、データソース デバッガーにアクセスできます。

![形式デザイナー ページのデバッグ開始ボタン](./media/er-data-debugger-run-from-designer.png)

編集中の ER 形式の形式マッピングと形式コンポーネントのデバッグが可能です。

## <a name="start-to-debug-in-the-model-mapping-designer"></a>モデル マッピング デザイナーでデバッグを開始する

**モデル マッピング** ページから実行できる ER モデル マッピングを構成した場合、アクション ウィンドウで **デバッグの開始** を選択すると、データ ソース デバッガーにアクセスできます。

![モデル マッピング デザイナー ページのデバッグ開始ボタン](./media/er-data-debugger-run-from-designer-mapping.png)

編集中の ER マッピングのモデル マッピング コンポーネントは、デバッグが可能です。

## <a name="appendix-1-get-an-er-solution"></a><a name="appendix1"></a>付録 1：ER ソリューションを入手する

### <a name="download-an-er-solution"></a>ER ソリューションをダウンロードする

ER ソリューションを使用して、処理された仕入先決済の電子決済ファイルをする場合は、 Microsoft Dynamics Lifecycle Services (LCS) の共有アセット ライブラリまたはグローバル リポジトリから入手可能な **ISO20022 クレジット転送** ER 決済フォーマットを [ダウンロード](download-electronic-reporting-configuration-lcs.md) することができます。

![構成リポジトリ ページの ER 決済形式のインポート](./media/er-data-debugger-import-from-repo.png)

選択された ER 形式に加えて、**ISO20022 クレジット転送** ER ソリューションの一環として、以下の[構成](general-electronic-reporting.md#Configuration) を Microsoft Dynamics 365 Finance インスタンスに自動的にインポートする必要があります：

- **支払モデル** [ER データ モデル 構成](general-electronic-reporting.md#DataModelComponent)
- **ISO20022 クレジット連想** [ER 形式の構成](general-electronic-reporting.md#FormatComponentOutbound)
- **支払 モデル マッピング 1611** [ER モデル マッピングの構成](general-electronic-reporting.md#ModelMappingComponent)
- **支払 モデルのマッピング先 SO20022** ER モデル マッピングの構成

これらの構成は、ER フレームワークの **構成** ページ（**組織管理** \> **電子レポート** \> **構成**）で確認できます。

![構成ページでインポートされた ER 構成](./media/er-data-debugger-configurations.png)

上記のいずれかの構成が構成ツリーに表示されない場合は、**ISO20022 クレジット転送**ER 支払形式と同じ方法でダウンロードし、LCS 共有アセットライブラリから手動でダウンロードする必要があります。

### <a name="analyze-the-downloaded-er-solution"></a>ダウンロードした ER ソリューションの分析

#### <a name="review-the-model-mapping"></a>モデル マッピングを確認する

1. **組織管理** \> **電子申告** \> **構成**の順に移動します。
2. **支払モデル** \> **支払モデルのマッピング 1611** を選択します。
3. **デザイナー** をクリックします。
4. マッピング レコード **支払モデル マッピング ISO20022 CT** を選択します。
5. **デザイナー** を選択し、開いているモデル マッピングを確認します。

    データモデルの **支払** フィールドは、処理中のベンダーの支払いラインのリストを返す **\$notSentTransactions** データ ソースにバインドされていることに注意してください。

    ![モデル マッピング デザイナー ページの支払フィールド](./media/er-data-debugger-model-mapping.png)

#### <a name="review-the-format-mapping"></a>形式マッピングを確認する

1. **組織管理** \> **電子申告** \> **構成**の順に移動します。
2. **支払モデル** \> **ISO20022 クレジット転送** を選択します。
3. **デザイナー** をクリックします。
4. **マッピング** タブで、開いている形式のマッピングを確認します。

    **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** element of the **ISO20022CTReports** \> **XMLHeader** のファイルは **\$PaymentByDebtor** データ ソースにバインドされており。このデータ ソースは、データ モデルの **支払い** フィールドのレコードをグループ化するように構成されていることを留意してください。

    ![形式デザイナー ページの PmtInf 要素](./media/er-data-debugger-format-mapping.png)

#### <a name="review-the-format"></a>形式を確認する

1. **組織管理** \> **電子申告** \> **構成**の順に移動します。
2. **支払モデル** \> **ISO20022 クレジット転送** を選択します。
3. **デザイナー** を選択し、開いている形式を確認します。

    **ドキュメント** \> **CstmrCdtTrfInitn** \> **PmtInf** \> **CdtTrfTxInf** \> **CdtrAcct** \> **Id** \> **IBAN** \> **BankIBAN** が、支払いファイルに仕入先アカウントの IBAN コードを入力するように設定されていることを留意してください。

    ![形式デザイナー ページの BankIBAN 要素](./media/er-data-debugger-format.png)

## <a name="appendix-2-configure-accounts-payable"></a><a name="appendix2"></a>付録 2：買掛金勘定を構成する

### <a name="modify-a-vendor-property"></a>仕入先プロパティの変更

1. **買掛金勘定** \> **仕入先** \> **すべての仕入先** に移動します。
2. アクション ウィンドウで、仕入先に **DE-01002** を選択し、**設定** グループの **仕入先** タブで、**銀行口座** を選択します。
3. **ID** クイックタブの **IBAN** フィールド に、<a name="enteredIBANcode"> </a>**GB33 BUKB 2020 1555 5555 55** を入力します。
4. **保存** を選択します。

![仕入先の銀行口座ページで設定された IBAN フィールド](./media/er-data-debugger-iban.png)

### <a name="set-up-a-method-of-payment"></a>支払方法の設定

1. **買掛金勘定** \> **支払設定** \> **支払方法** に移動します。
2. 支払方法 **SEPA CT** を選択します。
3. **ファイル形式** セクションの **ファイル形式** クイック タブで、 **一般的なエクスポート形式** のオプションを **はい** に設定します。
4. **形式の構成のエクスポート** フィールドで、ER 形式に **ISO20022 クレジット転送** を選択します。
5. **保存** を選択します。

![支払方法ページにおけるファイル形式の設定](./media/er-data-debugger-payment-method.png)

### <a name="add-a-vendor-payment"></a>仕入先の支払を追加する

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. 新しい支払仕訳帳を追加します。
3. **明細行** を選択し、新しい支払明細行を追加します。
4. **口座** フィールドで、仕入先に **DE-01002** を選択します。
5. **Debit**フィールドに値を入力します。
6. **支払方法**フィールドで、**SEPA CT**を選択します。
7. **保存** を選択します。

![仕入先支払ページに追加された仕入先の支払](./media/er-data-debugger-payment-journal.png)

## <a name="appendix-3-process-a-vendor-payment"></a><a name="appendix3"></a>付録 3：仕入先の支払いを処理する

1. **買掛金勘定** \> **支払** \> **仕入先支払仕訳帳** に移動します。
2. **仕入先支払仕訳帳** ページで、上記手順で作成した 支払仕訳帳を選択し、**明細行**を選択し ます。
3. 支払明細行を選択し、**支払ステータス** \> **なし** を選択します。
4. **支払の生成**を選択します。
5. **支払方法**フィールドで、**SEPA CT**を選択します。
6. **銀行口座** フィールドで、 **DEMF OPER** を選択します。
7. **支払いの生成** ダイアログ ボックスで、**OK** を選択します。
8. **電子レポート パラメーター** ダイアログ ボックスで、**OK**を選択します。
