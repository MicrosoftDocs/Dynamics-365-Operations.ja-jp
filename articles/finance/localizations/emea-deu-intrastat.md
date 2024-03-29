---
title: ドイツのイントラスタット
description: この記事には、ドイツでのイントラスタット申告に関する情報が含まれています。
author: AdamTrukawka
ms.date: 09/09/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: ae978b28098d92d84415c29bbe76157144f862d8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269437"
---
# <a name="german-intrastat"></a>ドイツのイントラスタット

[!include [banner](../includes/banner.md)]

**イントラスタット** ページは、欧州連合 (EU) の加盟国での取引に関するレポート情報を生成するために使用されます。 ドイツのイントラスタット申告には、報告用の商品の取引に関する情報が含まれています。 レポートは、[6.2 INSTAT/XML フォーマットのファイル宣言](https://www-idev.destatis.de/idev/doc/intra_en/hilfe6_2.html)ページで紹介されているドイツ当局のガイドラインに従ってフォーマットされています。

次の表は、ドイツのイントラスタット申告に含まれるフィールドを示しています。

| フィールド | 出荷 | 着荷 |
|-------------------------|-------------------------|-------------------------|
| 参照期間 | X | X |
| 方向コード | X | X |
| イントラスタット申告の通貨</br>**注 :** この通貨は<em>会計通貨</em>です。 | X | X |
| 商品コード | X | X |
| 商品名 | X | X |
| 補足単位コード | X | X |
| 委託 / 仕向地の加盟国 | X | X |
| 正味質量 | X | X |
| 補足単位の数量 | X | X |
| 原産国 |  | X |
| 請求金額 | X |  |
| 統計値 | X | X |
| トランザクションの種類 | X | X |
| 転送モード | X | X |
| 地域コード</br>**注記:**</br><ul></br><li>原産国または地域がドイツで、請求書が発送用の場合、原産国のイントラスタット コードが表示されます。</li></br><li>原産国または地域がドイツに例を示し、請求書が発送用である場合は、コード **99** が表示されます。</li></br><li>請求書が着荷の場合は、州のイントラスタット コードが表示されます。</li></br></ul> | X | X |
| 港/空港/内陸港コード | X | X |
| 配送条件 | X | X |


## <a name="set-up-intrastat"></a>イントラスタットの設定

1. 会社のコードを設定します。

    1. **組織管理** > **組織** > **法人** の順に移動します。
    2. **対外貿易およびロジスティクス** クイックタブの、**識別** セクションの、**DVR** フィールドにインターチェンジ契約 ID を入力します。 この ID は、レポートに含まれます。
    3. **VAT 控除番号のエクスポート** フィールドに、エクスポートする会社の付加価値税 (VAT) 番号を入力します。
    4. **VAT 控除番号のインポート** フィールドに、インポートする会社の VAT 番号を入力します。
    5. **イントラスタット コード** フィールドに、法人に割り当てられているイントラスタット コードを入力します。
    6. **税登録** クイックタブの **税登録番号** フィールドに、自分の会社の税登録番号を入力します。

    > [!NOTE]
    > 関連会社のイントラスタット レポートを生成する場合は、**税登録番号** フィールドに親会社の税登録番号を入力します。

2. [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index) の共有アセット ライブラリで、イントラスタット申告用に次の電子申告 (ER) コンフィギュレーションの最新バージョンをダウンロードします。

    - イントラスタット モデル
    - イントラスタット レポート
    - INSTAT XML
    - INSTAT XML (DE)

3. 対外貿易パラメーターの設定 :

    1. Dynamics 365 Finance で、**税** > **設定** > **対外貿易パラメーター** の順に移動します。
    2. **イントラスタット** タブの、**電子申告** クイックタブの **ファイル形式のマッピング** フィールドで、**イントラスタット XML (DE)** を選択します。
    3. **レポート形式のマッピング** フィールドで **イントラスタット レポート** を選択します。
    4. **商品コード階層** クイック タブの **カテゴリ階層** フィールドで、**イントラスタット** を選択します。
    5. **トランザクション コード** フィールドで、プロパティ転送のトランザクション コードを選択します。 このコードは、補償 (金銭的またはその他) に対する資産の実際のまたは計画された譲渡を生み出すトランザクションに使用します。 また、修正に対して使用します。
    6. **訂正票** フィールドで商品の返品用のトランザクション コードを選択します。
    7. **作業者** フィールドで、イントラスタット レポートの連絡担当者を選択します。 **連絡先** タブで、**名前**、**電話**、**FAX**、**電子メール**、**インターネット アドレス** の各フィールドに値を入力します。 これらのフィールドはレポートに含まれています。
    8. **所轄官庁** フィールドで、イントラスタット所轄官庁を選択します。
    9. **税** > **間接税** > **売上税** > **売上税所轄官庁** および前のステップで選択したイントラスタット権限について次の情報を入力します。

       - 当局 ID
       - 住所
       - 連絡先情報

    10. **国/地域のプロパティ** タブの、**国/地域** フィールドで、会社が事業を行っているすべての国または地域を一覧表示します。 国または地域ごとに、**国/地域のタイプ** フィールドで **EU** を選択して、国または地域をイントラスタット レポートに表示します。

4. リージョン コードの設定。

    1. **組織管理** > **グローバル アドレス帳** > **アドレス** > **アドレスの設定** の順に移動します。
    2. **都道府県** タブの、**国/地域** フィールドで、**DEU** を選択し、**フィルターの適用** を選択します。
    3. グリッドで、状態を選択します。 次に、**イントラスタット コード** フィールドに、一意のイントラスタット コードを入力します。

5. 製品の原産国住所を設定します。

    1. **製品情報管理** > **製品** > **リリースされた製品** の順に移動します。
    2. グリッドで製品を選択します。
    3. **対外貿易クイックタブ** の **イントラスタット** セクションにある **原産国** フィールドで、**DEU** を選択します。

6. **税** > **設定** > **対外貿易** > **イントラスタットの圧縮** に移動し、イントラスタット情報が集計されたとき比較するフィールドを選択します。 ドイツのイントラスタットの場合、次のフィールドを選択します。

    - 商品
    - 国/地域
    - 訂正
    - 方向
    - 配送条件
    - 請求書
    - 原産国/地域
    - 港
    - 送信者の国/地域
    - 送信者の都道府県
    - 集計手順
    - トランザクション コード
    - 輸送
    - 課税控除番号

### <a name="intrastat-transfer"></a>イントラスタットの転送

**イントラスタット** ページの操作ウィンドウで、**転送** を選択し、販売注文、自由書式の請求書、発注書、仕入先請求書、仕入れ先製品受領書 **、** プロジェクト請求書、および転送オーダーから EU 内での貿易についての情報が自動的に転送されます。 EU 加盟国が宛先の国または地域 (発送用) または委託 (着荷用) として扱っているドキュメントのみ転送されます。

また、アクション ウィンドウで **新規** を選択することで、トランザクションを手動で入力することもできます。

### <a name="generate-an-intrastat-report"></a>イントラスタット レポートの生成

1. **税** > **申告** > **対外貿易** > **イントラスタット** の順に移動します。
2. アクション ウィンドウで、**出力** > **レポート** を選択します。
3. **イントラスタット レポート** ダイアログ ボックスで、次のフィールドを設定します。

    | フィールド | 説明 |
    |-------------------------|-------------------------|
    | 自 | レポートの開始日を選択します。 |
    | 最終日 | レポートの終了日を選択します。 |
    | ファイルの生成 | .txt ファイルを生成するには、このオプションを **はい** に設定します。 |
    | ファイル名 | このフィールドは空白のままにします。 ファイル名は自動的に生成され、**&lt;envelopeId&gt;** XML タグの値とファイル拡張子 **.xml** で構成されます。</br>**&lt;envelopeId&gt;** 値は、次の要素を連結した順序で表されます。</br><ol type="1"></br><li>**&lt;interchangeAgreementId&gt;** タグの値</li></br><li>ハイフン (-)</li></br><li>**&lt;YYYYMM の referencePeriod&gt;** タグの値</li></br><li>ハイフン (-)</li></br><li>**&lt;YYYYMMDD の封筒/日時/日付&gt;** タグの値</li></br><li>ハイフン (-)</li></br><li>**&lt;hhmm の封筒/日時/時間&gt;** タグの値</li></br></ol> |
    | 方向 | <ul></br><li>コミュニティ内の着荷についてレポートするには **着荷** を選択します。</li></br><li>コミュニティ内発送に関してレポートするには **発送** を選択します。</li></br><li>着荷と発送の両方についてレポートするには **両方** を選択します。</li></br></ul> |
    | 税務登録番号 | 法人の税登録番号と異なる場合は、送信者の識別コードを生成するために使用する登録番号を入力します。 |


## <a name="example"></a>例

この例は、イントラスタットの着荷と発送を投稿する方法を示しています。 **DEMF** 法人を使用します。

1. [LCS](https://lcs.dynamics.com/Logon/Index) の共有アセット ライブラリで、イントラスタット申告の形式については、以下の ER 構成の最新バージョンをダウンロードしてください。

    - イントラスタット モデル
    - イントラスタット レポート
    - イントラスタット XML
    - イントラスタット XML (DE)

2. トランザクション コードを作成します。

    1. **税** > **設定** > **対外貿易** > **トランザクション コード** の順に移動します。
    2. アクション ウィンドウで、**新規** を選択します。
    3. **トランザクション** **コード** フィールドに、**21** を入力します。
    4. **名前** フィールドに、**返品** と入力します。
    5. アクション ウィンドウで、**保存** を選択します。

3. 所轄官庁識別番号を設定します。

    1. **税** > **間接税** > **売上税** > **売上税所轄官庁** に移動します。
    2. 一覧で、**TA** を選択します。
    3. **所轄官庁** フィールドで、**123** と入力します。

4. リージョン コードの設定。

    1. **組織管理** > **グローバル アドレス帳** > **アドレス** > **アドレスの設定** の順に移動します。
    2. **都道府県** タブの、**国/地域** フィールドで、**DEU** を選択し、**フィルターの適用** を選択します。
    3. グリッドで **BE** を選択し、**イントラスタット コード** フィールドに **11** と入力します。
    4. アクション ウィンドウで、**保存** を選択します。

5. 対外貿易パラメーターの設定。

    1. **税** > **設定** > **対外貿易** > **対外貿易パラメーター** の順に移動します。
    2. **イントラスタット** タブの **一般** クイックタブにある **トランザクション** **コード** フィールドで、**11** を選択します。
    3. **訂正票** フィールドで、**21** を選択します。
    4. **所轄官庁** フィールドで、**TA** を選択します。
    5. **電子申告** クイックタブの **ファイル形式のマッピング** フィールドで、**INSTAT XML (DE)** を選択します。
    6. **レポート形式のマッピング** フィールドで **イントラスタット レポート** を選択します。
    7. **商品コード階層** クイック タブの **カテゴリ階層** フィールドで、**イントラスタット** が選択されていることを確認します。
    8. **国/地域のプロパティ** タブで、**新規** を選択します。
    9. **関係者国/地域** フィールド で、**FRA** を選択します。
    10. **国/地域のタイプ** フィールドで、**EU** を選択します。

6. 商品に商品コードを割り当て、商品の原産地を設定します。 **商品コード**、**原産国/地域**、および **原産地** フィールドは、製品を選択したときに自動的に受注と発注書に設定されます。

    1. **製品情報管理** > **製品** > **リリースされた製品** の順に移動します。
    2. グリッドで、**D0001** を選択します。
    3. **対外貿易クイックタブ** の **イントラスタット** セクションにある **商品** フィールドで、**920 20 34** を選択します。
    4. **発生元** セクションの **国/地域** フィールドで **DEU** を選択します。
    5. **在庫管理** クイックタブの、**重量測定** セクションの、**正味重量** フィールドに、**12** と入力します。
    6. アクション ウィンドウで、**保存** を選択します。

7. 配送を配信モードに割り当てます。 配送コードは、配送モードを選択すると注文時に自動的に設定されます。

    1. **調達** > **設定** > **配布** > **配送モード** に順に移動します。
    2. 一覧で、**10** を選択します。
    3. **対外貿易** クイックタブの **配送** フィールドで、**01** を選択します。

8. EU 顧客との販売注文を作成します。

    1. **売掛金勘定** > **注文** > **すべての販売注文** の順に移動します。
    2. アクション ウィンドウで、**新規** を選択します。
    3. **作成販売注文** ダイアログ ボックスの **顧客** クイックタブにある **顧客** セクションの、**顧客アカウント** フィールドで、**DE-012** を選択します。
    4. **一般** クイック タブの **保管分析コード** セクションの **サイト** フィールドで、**1** を選択します。
    5. **倉庫** フィールドで、**11** を選択します。
    6. **OK** を選択します。
    7. **ヘッダー** タブの **対外貿易** クイックタブの、**港** フィールドで、**53** を選択します。
    8. **集計手順** フィールドで、**31710** を選択します。
    9.  **行** タブの、**販売注文** **明細行** クイックタブにある、**品目番号** フィールドで、**D0001** を選択します。 その後、**数量** フィールドに **10** と入力します。
    10. **行の詳細** クイックタブの **対外貿易** タブで、**トランザクション コード**、**転送**、**商品**、および **原産国/地域** の各フィールドが自動的に設定されます。
    11. アクション ウィンドウで、**保存** を選択します。
    12. アクション ペインの、**請求書** タブで、**生成** セクションから **請求書** を選択します。
    13. **請求の転記** ダイアログ ボックスの **パラメーター** クイックタブにある、**パラメーター** セクションの **数量** フィールドで、**すべて** を選択します。
    14. **OK** を選択して、請求書を転記します。

9.  トランザクションをイントラスタット仕訳帳に転送し、結果を確認します。

    1. **税** > **申告** > **対外貿易** > **イントラスタット** の順に移動します。
    2. アクション ペインで、**転送** を選択します。
    3. **イントラスタット (転送)** ダイアログ ボックスの **パラメーター** セクションで、**顧客請求書** オプションを **はい** に設定します。
    4. **フィルター** を選択します。
    5. **イントラスタット フィルター** ダイアログ ボックスの **範囲** タブで、1 行目の行を選択し、**フィールド** フィールドが **日付** に設定されている必要があります。
    6. **基準** フィールドで、現在の日付を選択します。
    7. **OK** を選択して **イントラスタット フィルター** ダイアログ ボックスを閉じます。
    8. **OK** を選択し、**イントラスタット (転送)** ダイアログ ボックスを閉じて、結果をレビューします。 この線は、前に作成した受注を表します。

        ![イントラスタット ページの販売注文を表す線](media/intrastat_deu_1.png)

10. トランザクション行を選択し、**一般** タブを選択して詳細を表示します。

    ![イントラスタット ページの全般タブにある販売注文の詳細](media/intrastat_deu_2.png)

11. 販売注文を使用して訂正票を作成します。

    1. **売掛金勘定** > **注文** > **すべての販売注文** の順に移動します。
    2. アクション ウィンドウで、**新規** を選択します。
    3. **作成販売注文** ダイアログ ボックスの **顧客** クイックタブにある **顧客** セクションの、**顧客アカウント** フィールドで、**DE-012** を選択します。
    4. **一般** クイック タブの **保管分析コード** セクションの **サイト** フィールドで、**1** を選択します。
    5. **倉庫** フィールドで、**11** を選択します。
    6. **ヘッダー** タブの **対外貿易** クイックタブの、**港** フィールドで、**53** を選択します。
    7. **集計手順** フィールドで、**31710** を選択します。
    8. **行** タブの、**販売注文** **明細行** クイックタブにある、**品目番号** フィールドで、**D0001** を選択します。 その後、**数量** フィールドに **-2** と入力します。
    9. **明細行の詳細** クイックタブの **対外貿易** タブにある **トランザクション コード** フィールドで、**21** を選択します。
    10. **輸送**、**商品** および **原産国/地域** の各フィールドが自動的に設定されます。
    11. アクション ウィンドウで、**保存** を選択します。
    12. アクション ペインの、**請求書** タブで、**生成** セクションから **請求書** を選択します。
    13. **請求の転記** ダイアログ ボックスの **パラメーター** クイックタブにある、**パラメーター** セクションの **数量** フィールドで、**すべて** を選択します。
    14. **OK** を選択して、請求書を転記します。

12. トランザクションをイントラスタット仕訳帳に転送し、結果を確認します。

    1. **税** > **申告** > **対外貿易** > **イントラスタット** の順に移動します。
    2. アクション ペインで、**転送** を選択します。
    3. **イントラスタット (転送)** ダイアログ ボックスの **パラメーター** セクションで、**顧客請求書** オプションを **はい** に設定します。
    4. **OK** を選択し、**イントラスタット (転送)** ダイアログ ボックスを閉じて、結果をレビューします。 **方向** フィールドが **着荷** にされている新しい行が追加されました。            
        この行は、商品の物理的な返品を表します。

        ![イントラスタット ページの商品の物理的返品の行](media/intrastat_deu_3.png)

13. トランザクション行を選択し、**一般** タブを選択して詳細を表示します。

    ![イントラスタット ページの全般タブでの商品の物理的返品の詳細](media/intrastat_deu_4.png)

14. 販売注文を使用して修正を作成します。

    1. **売掛金勘定** > **注文** > **すべての販売注文** の順に移動します。
    2. アクション ウィンドウで、**新規** を選択します。
    3. **作成販売注文** ダイアログ ボックスの **顧客** クイックタブにある **顧客** セクションの、**顧客アカウント** フィールドで、**DE-012** を選択します。
    4. **一般** クイック タブの **保管分析コード** セクションの **サイト** フィールドで、**1** を選択します。
    5. **倉庫** フィールドで、**11** を選択します。
    6. **ヘッダー** タブの **対外貿易** クイックタブの、**港** フィールドで、**53** を選択します。
    7. **集計手順** フィールドで、**31710** を選択します。
    8. **行** タブの、**販売注文** **明細行** クイックタブにある、**品目番号** フィールドで、**D0001** を選択します。 その後、**数量** フィールドに **-3** と入力します。
    9. **明細行の詳細** クイックタブの **対外貿易** タブにある **トランザクション コード** フィールドで、**11** を選択します。
    10. **輸送**、**商品** および **原産国/地域** の各フィールドが自動的に設定されます。
    11. アクション ウィンドウで、**保存** を選択します。
    12. **トランザクション コード** フィールドが 11 に設定されていることを確認してください。
    13. アクション ペインの、**請求書** タブで、**生成** セクションから **請求書** を選択します。
    14. **請求の転記** ダイアログ ボックスの **パラメーター** クイックタブにある、**パラメーター** セクションの **数量** フィールドで、**すべて** を選択します。
    15. **OK** を選択して、請求書を転記します。

15. トランザクションをイントラスタット仕訳帳に転送し、結果を確認します。

    1. **税** > **申告** > **対外貿易** > **イントラスタット** の順に移動します。
    2. アクション ペインで、**転送** を選択します。
    3. **イントラスタット (転送)** ダイアログ ボックスの **パラメーター** セクションで、**顧客請求書** オプションを **はい** に設定します。
    4. **OK** を選択し、**イントラスタット (転送)** ダイアログ ボックスを閉じて、結果をレビューします。 **修正** 列にチェック マークが表示される新しい行が追加されました。

        ![イントラスタット ページの修正の行](media/intrastat_deu_5.png)

16. トランザクション行を選択し、**一般** タブを選択して詳細を表示します。

    ![イントラスタット ページの全般タブにある修正の詳細](media/intrastat_deu_6.png)

17. アクション ウィンドウで、**出力** > **レポート** を選択します。
18. **イントラスタット レポート** ダイアログ ボックスの **パラメーター** クイックタブにある **日付** セクションで、作成した販売注文の月を選択します。
19. **エクスポート** **オプション** セクションで、**ファイルの生成** オプションを **はい** に設定します。
20. **ファイル名** フィールドに、必要なファイル名を入力します。
21. **OK** を選択し、生成されたレポートを確認します。 次の表に、サンプル レポートの値を示します。

    | **氏名**                  | **売上請求書**  |   **訂正**   | **訂正票** |
    |---------------------------|--------------------|--------------------|-----------------|
    | declarationId             | 2021-07-D          | 2021-07-A          |                 |
    | referencePeriod           | 2021-07            | 2021-07            |                 |
    | PSIId                     | 11203/118/12345000 | 11203/118/12345000 |                 |
    | functionCode              | O                  | O                  |                 |
    | flowCode                  | 借方                  | A                  |                 |
    | CurrencyCode              | EUR                | EUR                |                 |
    | itemNumber                | 0000362            | 0000362            | 0000361         |
    | CN8Code                   | 9202034            | 9202034            | 9202034         |
    | goodsDescription          | スピーカー            | スピーカー            | スピーカー         |
    | MSConsDestCode            | FR                 | FR                 | FR              |
    | countryOfOriginCode       | \-                 | \-                 | DE              |
    | netMass                   | 120                | -36                | 24              |
    | invoicedAmount            | 3290               | -987               | \-              |
    | StatisticalValue          | 3290               | -987               | 658             |
    | natureOfTransactionACode  | 1                  | 1                  | 2               |
    | natureOfTransactionBCode  | 1                  | 1                  | 1               |
    | modeOfTransportCode       | 01                 | 01                 | 01              |
    | regionCode                | 11                 | 11                 | 11              |
    | portAirportInlandportCode | 53                 | 53                 | 53              |

