---
title: サブスクリプション請求管理における収益と経費の繰延
description: この記事では、サブスクリプション請求管理で収益と経費の繰延を設定する方法について説明します。
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 209afd08c0c7e3cbd63ed95613b1d1dec94856f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908099"
---
# <a name="revenue-and-expense-deferrals-in-subscription-billing"></a>サブスクリプション請求管理における収益と経費の繰延

この記事では、サブスクリプション請求管理で収益と経費の繰延を設定して使用する方法について説明します。 繰延スケジュールは、基になるドキュメントまたは請求スケジュールに常に基づいて設定されます。 これらは既定値に基づいて作成されるため、個別に入力したり作成することはできません。

収益および経費の繰延を設定および使用するプロセスは、複数のページで行われます:

- **収益および経費の繰延パラメーター** ページで、会社の基本設定を定義できます。
- **延期の既定値**  ページでは、繰延スケジュールに使用される既定の勘定、およびテンプレートを設定できます。
- **延期テンプレート** および **イベント ベースの延期テンプレート** ページで、延期スケジュールに使用するテンプレートを定義できます。
- **すべての繰延スケジュール** ページで、延期スケジュールを表示および編集できます。

収益および経費の繰延は、繰り返し契約の請求と組み合わせて使用できます。

## <a name="revenue-and-expense-deferral-parameters"></a>収益および経費の繰延パラメーター

**収益および経費の繰延パラメータ** ページには、次のフィールドが表示されます。

| フィールド | Description |
|---|---| 
| **スケジュール** タブ | |
| 期間ごとに等しい | <p>延期スケジュールの期間ごとの金額を計算する際には、期間の日数を使用するかどうかを指定します:</p><ul><li>**はい** - 期間の日数に関係なく、各期間の金額が同じになります。 一部期間 (繰延スケジュールの最初や最後の期間など) が分割されます。</li><li>**いいえ** – この金額は各期間の日数に応じて算出されます。</li></ul><p>この設定はトランザクション レベルで上書きできます。</p> |
| 販売割引繰延オプション | <p>割引額と受注額について別々の繰延スケジュールを作成するかどうかを指定します:</p><ul><li>**割引の個別のスケジュール** : 割引金額は、収益金額とは別の方法で保持されます。<p>この場合、販売注文を作成して転記すると、2 つの繰延スケジュールが作成されます。 割引金額と収益金額は、異なる繰延勘定に転記されます。</p></li><li>**収益と割引を マージ**: 割引金額と収益金額が組み合わされます。 繰延スケジュールが 1 つ作成され、割引額と収益額は同じ繰延べ勘定に計上されます。<p>この場合、販売注文を作成して転記すると、1 つの繰延スケジュールが作成されます。 割引額と収益額の両方が同じ繰延べ勘定に計上されます。</p></li></ul><p>**注:** 未請求収益機能を使用する項目に割引を適用するには、**割引のためのスケジュールを別にする** オプションを選択します。 あた、未請求収益機能を使用しているかどうかにかかわらず、すべての項目に割引を適用することができます。 **収益に割引をマージする** オプションが選択されている場合、未結合の収益機能を使用する品目に割引を適用することはできません。</p> |
| 購買割引繰延オプション | <p>割引額と発注額について別々の繰り延べ表を作成するかどうかを選択します。</p><ul><li>**割引の個別のスケジュール** : 割引金額は、経費金額とは別の方法で保持されます。<p>この場合、発注を作成して転記すると、2 つの繰延スケジュールが作成されます。 割引金額と経費は、異なる繰延勘定に転記されます。</p></li><li>**収益と割引を マージ**: 割引金額と経費金額が組み合わされます。 繰延スケジュールが 1 つ作成され、割引額と経費額は同じ繰延べ勘定に計上されます。<p>この場合、発注を作成して転記すると、1 つの繰延スケジュールが作成されます。 割引額と経費額の両方が同じ繰延べ勘定に計上されます。</p></li></ul> |
| 前期間を連結 | <p>前の期間の繰延スケジュール行を連結するかどうかを指定します。</p><ul><li>**はい** - 繰延開始日がトランザクション日付より前の期間の場合、トランザクション日付の期間を通じてのすべての金額が、1つの延期スケジュール行に結合されます。</li><li>**いいえ** - すべての期間の金額が別々の繰延スケジュール行に保持されます。<p>繰延開始日がトランザクション日付と同じ期間以降の期間である場合、このオプションは無効です。</p></li></ul><p>この設定は、トランザクション レベルで更新できます。</p> |
| 既定の繰延開始日 | <p>繰延スケジュールの開始日を決定するために使用するルールを選択します。</p><ul><li>**トランザクションの日付** – トランザクション日付を開始日として使用します。</li><li>**現在の月の始まり** - 現在の月の最初の日付を開始日として使用します。 トランザクション日付が任意の月の最初の日付である場合、当月の最初の日付は開始日です。</li><li>**次の月の始まり** - 翌月の最初の日付を開始日として使用します。 トランザクション日付が最初の日付である場合は、トランザクションの日付が使用されます。 それ以外の場合は、翌月の初日が使用されます。</li><li>**ルール15** - トランザクションの日付が 1 日目から 15 日目の場合は、当月の最初の日付を開始日として使用します。 トランザクション日付が 16 日目以降の場合は、翌月の 1 日が起算日となります。</li></ul><p>この設定は、トランザクション レベルで更新することができます。</p> |
| 短期繰延方法 | <p>短期の繰延方法を選択します (**なし**、**ローリング期間**、**固定年**)。</p><p>|
| 繰延転記方法 | <p>繰延トランザクションの作成方法を選択します:</p><ul><li>**貸借対照表** - 繰延トランザクションを作成するには、貸借対照表転記方法を使用します。</li><li>**損益計算書** - 繰延取引の作成には、損益計算書方式を使用します。 トランザクションが計上されると、請求書伝票を確認し、初期認識額と認識オフセット額のバランスをとるための追加項目を確認することができます。</li></ul> |
| 貸方の損益の取消 | <p>**メモ:** – このフィールドは、**繰延の計上方法** フィールドが **損益** に設定されている場合にのみ利用可能です。</p><p>請求スケジュールまたは販売注文に取消、終了、または払戻しを適用する際に、損益の金額を取り消すかどうかを指定します。</p><ul><li>**はい** - 損益の金額を取り消し、繰延スケジュールに貸方調整額を適用します。<p>請求期間の途中で取消が発生した場合、金額が計算されます。</p></li><li>**いいえ** – 請求予定表や販売注文に戻入、解約、返金が適用された場合、損益に戻入取引は発生しません。</li></ul> |
| **認識** タブ | |
| 一般仕訳帳の自動転記 | <p>収益および経費の繰延によって作成された仕訳帳エントリを自動的に転記するかどうかを指定します。</p><ul><li>**はい** – 収益や費用の繰り延べによって発生する仕訳を自動的に転記することができます。<p>**ヒント:** **はい** を選択することで、伝票の手動変更に起因する会計上の不整合を防止することができます。</p></li><li>**いいえ** – 収益や費用の繰り延べによって作成された仕訳は、自動的に計上されません。 仕訳帳はかならず手動で転記する必要があります。</li></ul> |
| 認識仕訳帳の集計 | <p>認識票を既定で連結するかどうかを指定します。</p><ul><li>**はい** - 日付が同じであるすべての認識明細行に対し、単一の伝票を作成する。 同じ勘定を持つ伝票内のすべての明細行が 1 つの明細行に連結されます。</li><li>**いいえ** - 各認識明細行に対して伝票を作成します。</li></ul><p>この設定は、**認識処理** ページ で更新できます。</p> |
| 既定の仕訳帳名 | 認識処理など、収益・費用の繰り延べ処理から作成される仕訳帳の名称を選択します。 |
| 認識仕訳帳明細行の説明 | <p>仕訳帳の伝票行の説明に表示される説明を選択します。</p><ul><li>**スケジュール明細行の日付** - 仕訳帳の行の説明にスケジュール行の日付を表示します。</li><li>**発生元トランザクションの詳細** - 仕訳帳行の説明に元のトランザクション情報を表示します。<p>**例 :** USMF-0001、CIV-00839、ソフトウェア収益</p></li></ul> |
| **番号順序** タブ | リース番号順序の既定値を設定するには、このタブを使用します。 番号列生成ウィザードは、番号列を自動的に生成して割り当てるために使用します。 生成される番号順序に手動で変更を加える場合を選択しない限り、番号順序を変更する必要があります。 |
| スケジュール番号 | 繰延スケジュールに使用されるシーケンス番号です。 |

## <a name="deferral-templates"></a>繰延テンプレート

**繰延テンプレート** ページを使用 して、繰延スケジュールに使用する直線テンプレートを定義します。

テンプレートを使用する利点を次に示します:

* 繰延の長さは自動的に計算されます。
* 認識をスキップする期間がある繰延スケジュールを許可します。
* 繰延を自動化するには、テンプレートを製品、製品グループ、製品カテゴリ、顧客、または顧客グループに割り当てる必要があります。 テンプレートの割り当ては **繰延の既定値** ページから行われます。

テンプレートには、日次、月次、会計年度期間など、複数の期間頻度を使用できます。

テンプレート行は、タイプ (**認識** または **スキップ**) と期間の長さで構成されます。 スキップされた明細行の繰延スケジュール行の金額は 0 (ゼロ) です。 この動作は、すべての期間で収益を認識しない場合に便利です。

### <a name="create-a-deferral-template"></a>繰延のテンプレートを作成する

繰延のテンプレートを作成するには、次の手順に従います。

1. **繰延のテンプレート** ページで、**新規** を選択します。
2. **テンプレート** フィールドに名前を入力します。
3. **説明** フィールドに説明を入力します。
4. **期間頻度** フィールドで、期間頻度を選択します。
5. 行のリストの一番上に行を追加する場合は **追加** を、リストの一番下に行を追加する場合は **アペンド** を選択します。
6. **タイプ** フィールドで、期間のタイプを選択します。
7. **期間** フィールドで、期間の長さを指定します。
8. 必要となる明細行ごとに手順 5 から 7 を繰り返します。
9. **保存** を選択します。

## <a name="deferral-defaults"></a>繰延の既定値

**延期の既定値** ページでは、品目の既定の繰延勘定を設定し、既定のテンプレートを繰延可能品目に割り当てる必要があります。 また、費用の繰延勘定を設定し、繰延費用にテンプレートを割り当てすることもできます。

**品目別の繰延**

品目があるトランザクション (販売注文など) の場合は、特定の品目および顧客に勘定とテンプレートを割り当てできます。 これらの設定は、トランザクションが延期される際の既定値として使用されます。 既定でトランザクションを繰延可能にする場合は、**繰延可能品目** ページで品目を設定する必要があります。

**勘定ごとの延期**

品目のないトランザクション (一般仕訳帳など) の場合は、繰延勘定を指定できます。 これらの勘定がトランザクション行で使用される場合、そのトランザクションは自動的に繰延としてマークされます。 トランザクションの明細行に対応するテンプレートと認識勘定が割り当てられます。

**すべてのトランザクション タイプ (販売注文、購買、一般仕訳帳のタブなど)**

ページ上の勘定には、財務分析コードを持つ主要勘定はありません。 認識勘定の財務分析コードは、組織に基づく顧客、または品目から由来します。

各テンプレートの明細行には、直線テンプレートまたはイベント ベースのテンプレートが必要です。 その両方を含めることができます。

### <a name="for-sales-orders"></a>販売注文用

販売注文の繰延既定値を指定するには、次の手順に従います。

1. **販売注文** タブで、繰延のタイプを選択します。
2. **追加** を選択して明細行を追加します。
3. **品目コード** フィールドで、品目コードを選択します。 品目コードにより、繰延の既定値の適用方法が決まれます。
4. 品目コードの適用方法を指定します:

    * **項目コード** フィールドが **テーブル** または **グループ** の場合、**商品関係** フィールドで項目関係を選択します。
    * **品目コード** フィールドが **カテゴリ** に設定 されている場合は、**カテゴリ関係** でカテゴリの関係性を選択します。
    * **品目コード** フィールドが **すべて** に設定されている場合、既定値は該当するすべてのレコードに適用されます。

5. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** フィールドでアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウントはすべてのレコードに適用されます。

6. **主勘定** フィールドで、繰延する主勘定を選択します。
7. **繰延転記方法** フィールドが **損益** に設定されている場合は、**初期収益勘定** フィールドで最初の収益勘定を選択し、**収益相手勘定** フィールドで収益相手勘定を選択します。
8. **短期繰延方法** フィールドが **ローリング期間s** または **固定年** に設定されている場合は、**短期繰延勘定** フィールドで短期繰延勘定を選択します。
9. テンプレートの場合、**追加** を選択して明細行を追加できます。
10. **品目コード** フィールドで、品目コードを選択します。
11. 品目コードの適用方法を指定します:

    * **項目コード** フィールドが **テーブル** または **グループ** の場合、**商品関係** フィールドで項目関係を選択します。
    * **品目コード** フィールドが **カテゴリ** に設定 されている場合は、**カテゴリ関係** フィールドでカテゴリの関係性を選択します。
    * **品目コード** フィールドが **すべて** に設定されている場合、既定値は該当するすべてのレコードに適用されます。

12. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** フィールドでアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウントはすべての該当するレコードに適用されます。
    * **直線テンプレート** フィールドで直線 テンプレートを選択するか、**イベント ベースのテンプレート** フィールドでイベント ベースのテンプレートを選択します。

13. **保存** を選択します。

### <a name="for-purchase-orders"></a>発注書用

発注書の繰延既定値を指定するには、次の手順に従います。

1. **発注** タブで、繰延のタイプを選択します。
2. **追加** を選択して明細行を追加します。
3. **品目コード** フィールドで、品目コードを選択します。
4. 品目コードの適用方法を指定します:

    * **項目コード** フィールドが **テーブル** または **グループ** の場合、**商品関係** フィールドで項目関係を選択します。
    * **品目コード** フィールドが **カテゴリ** に設定 されている場合は、**カテゴリ関係** フィールドでカテゴリの関係性を選択します。
    * **品目コード** フィールドが **すべて** に設定されている場合、既定値は該当するすべてのレコードに適用されます。

5. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** フィールドでアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウントはすべての該当するレコードに適用されます。

6. **主勘定** フィールドで、繰延する主勘定を選択します。
7. **繰延転記方法** フィールドが **損益** に設定されている場合は、**初期収益勘定** フィールドで最初の収益勘定を選択し、**収益相手勘定** フィールドで収益相手勘定を選択します。
8. **短期繰延方法** フィールドが **ローリング期間s** または **固定年** に設定されている場合は、**短期繰延勘定** フィールドで短期繰延勘定を選択します。
9. テンプレートの場合、**追加** を選択して明細行を追加できます。 
10. **品目コード** フィールドで、品目コードを選択します。
11. 品目コードの適用方法を指定します:

    * **項目コード** フィールドが **テーブル** または **グループ** の場合、**商品関係** フィールドで項目関係を選択します。
    * **品目コード** フィールドが **カテゴリ** に設定 されている場合は、**カテゴリ関係** フィールドでカテゴリの関係性を選択します。
    * **品目コード** フィールドが **すべて** に設定されている場合、既定値は該当するすべてのレコードに適用されます。

12. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** でアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウントはすべての該当するレコードに適用されます。
    * **直線テンプレート** フィールドで直線 テンプレートを選択するか、**イベント ベースのテンプレート** フィールドでイベント ベースのテンプレートを選択します。

13. **保存** を選択します。

### <a name="for-general-journals"></a>一般仕訳帳

一般仕訳帳の繰延既定値を指定するには、次の手順に従います。

1. **一般仕訳帳** タブを選択します。
2. 繰延の場合、**追加** を選択して明細行を追加できます。
3. **短期繰延方法** フィールドが **ローリング期間s** または **固定年** に設定されている場合は、**短期繰延勘定** フィールドで短期繰延勘定を選択します。
4. **繰延アカウント** フィールドで繰延アカウントを選択します。
5. **認知アカウント** フィールドで認知アカウントを選択します。
6. **繰延転記方法** フィールドが **損益** に設定されている場合は、**初期収益勘定** フィールドで最初の収益勘定を選択し、**収益相手勘定** フィールドで収益相手勘定を選択します。
7. **直線テンプレート** フィールドで直線 テンプレートを選択するか、**イベント ベースのテンプレート** フィールドでイベント ベースのテンプレートを選択します。
8. **保存** を選択します。

### <a name="for-free-text-invoices"></a>自由書式の請求書

自由書式の請求書の繰延既定値を指定するには、次の手順に従います。

1. **自由書式の請求書** タブを選択します。
2. 繰延の場合、**追加** を選択して明細行を追加できます。
3. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** フィールドでアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウント コーはすべての該当するレコードに適用されます。

4. **繰延アカウント** フィールドで繰延アカウントを選択します。
5. **短期繰延方法** フィールドが **ローリング期間s** または **固定年** に設定されている場合は、**短期繰延勘定** フィールドで短期繰延勘定を選択します。
6. **認知アカウント** フィールドで認知アカウントを選択します。
7. **繰延転記方法** フィールドが **損益** に設定されている場合は、**初期収益勘定** フィールドで最初の収益勘定を選択し、**収益相手勘定** フィールドで収益相手勘定を選択します。
8. **直線テンプレート** フィールドで直線 テンプレートを選択するか、**イベント ベースのテンプレート** フィールドでイベント ベースのテンプレートを選択します。
9. **保存** を選択します。

### <a name="for-invoice-journals"></a>請求書仕訳帳

請求書仕訳帳の繰延既定値を指定するには、次の手順に従います。

1. **請求書仕訳帳** タブを選択します。
2. 繰延の場合、**追加** を選択して明細行を追加できます。
3. アカウント コードの適用方法を指定します:

    * **アカウント コード** フィールドが **テーブル** または **グループ** の場合、**アカウント関係** フィールドでアカウントの関係を選択します。
    * **アカウント コード** フィールドが **すべて** に設定されている場合、アカウント コーはすべての該当するレコードに適用されます。

4. **繰延アカウント** フィールドで繰延アカウントを選択します。
5. **短期繰延方法** フィールドが **ローリング期間s** または **固定年** に設定されている場合は、**短期繰延勘定** フィールドで短期繰延勘定を選択します。
6. **認知アカウント** フィールドで認知アカウントを選択します。
7. **繰延転記方法** フィールドが **損益** に設定されている場合は、**初期収益勘定** フィールドで最初の収益勘定を選択し、**収益相手勘定** フィールドで収益相手勘定を選択します。
8. **直線テンプレート** フィールドで直線 テンプレートを選択するか、**イベント ベースのテンプレート** フィールドでイベント ベースのテンプレートを選択します。
9. **保存** を選択します。

### <a name="items-that-are-deferred-by-default"></a>既定で繰延される品目

**既定で繰延される品目** のページを使用して、既定で延期される品目を定義します。 品目を繰延するトランザクションのタイプを設定できます。 1 つの品目を繰延するか、品目グループまたはカテゴリ全体を指定することができます。

品目を繰延として設定する場合は、**繰延の既定値** ページで既定 の勘定およびテンプレートを選択します。 勘定とテンプレートを選択しない場合、それらの品目が入力されたトランザクション明細行は繰延されません。

関連付けられている販売カテゴリまたは購買カテゴリに基づいて繰延される品目の場合、繰延設定はカテゴリに基づいて設定されます。 ただし、**カテゴリ関係** フィールドでカテゴリの項目が選択されていない場合は、ランクが上位のカテゴリの繰延設定が使用されます。 たとえば、**ホーム ビデオ** 販売カテゴリを追加するが、**テレビ** 販売カテゴリは追加しません。 **テレビ** カテゴリに関連付けられている繰延品目を追加すると、その品目に対して **ホーム ビデオ** の繰延設定が使用されます。

### <a name="set-up-deferred-items"></a>繰延品目を設定します

デフォルトで繰延される項目を設定するには、次の手順に従います。

1. **既定で延期された品目** のページで、目的のタブ (**販売注文** または **購買**) を選択します。
2. **追加** を選択して明細行を追加します。
3. **品目コード** フィールドで、品目コードを選択します。
4. 品目コードの適用方法を指定します:

    * **項目コード** フィールドが **グループ** または **テーブル** の場合、**商品関係** フィールドで項目関係を選択します。
    * **品目コード** フィールドが **カテゴリ** に設定 されている場合は、**カテゴリ関係** フィールドでカテゴリの関係性を選択します。

5. 必要となる明細行ごとに手順 2 から 4 を繰り返します。
6. **保存** を選択します。

## <a name="deferred-charges"></a>繰延費用

**繰延費用** ページでは、既定で延期される請求額を定義します。

> [!NOTE]
> * 現在、繰延費用は販売注文にのみ使用できます。
> * 課金は明細行でのみ繰延が可能です。 販売注文のヘッダー レベルで請求を延期するには、販売注文の別の行に繰延品目として設定することができます。
> * 自由形式の請求書の料金を繰延するには、別の繰延請求書の明細行として料金を入力する必要があります。
> * この機能は、サポート費用および収益分割機能には使用できません。

### <a name="set-up-deferred-charges"></a>繰延料金の設定

繰延の課金を設定するには、以下の手順で行います。

1. **繰延費用** ページで、**追加** を選択して明細行を追加します。
2. **請求金額コード** フィールドで、請求金額のコードを選択します。
3. **請求金額リレーション** フィールドで、請求金額のリレーションを選択します。
4. 必要となる明細行ごとに手順 1 から 3 を繰り返します。
5. **保存** を選択します。

## <a name="event-based-deferral-templates"></a>イベント ベースの繰延テンプレート

**イベント ベースの延期テンプレート** ページを使用して、繰延トランザクションで使用できるイベント ベースの延期テンプレートを定義し、**延期の既定値** ページで割り当てできます。

### <a name="create-an-event-based-template"></a>イベント ベーステンプレートの作成

イベント ベースのテンプレートを作成するには、次の手順に従います。

1. **イベント ベースの繰延テンプレート** ページで、**新規** を選択します。
2. **テンプレート** フィールドにテンプレート グループの固有の名前を入力します。
3. **説明** フィールドに説明を入力します。
4. **配賦タイプ** フィールドで、配賦のタイプを選択します。

    * **変動金額** : 入力した各行に特定の金額を割り当てます。
    * **等しい金額** : 入力した各行に同じ金額を割り当てます。 
    * **割合** - 各枚際行に対して入力した割合の値に基づく金額を割り当てます。
    * **完了率** – 入力された各行に対して累積完了値を割り当てます。
    * **変動数** : 入力した各行に特定の数量を割り当てます。

5. 請求書トランザクションの各イベント行を単位数で等分する場合は、**単位ごとに個別のイベントを作成** オプションを **はい** に設定します。 イベント明細行を分割しない場合は **いいえ** に設定します。
6. **有効期限アカウント** フィールドで有効期限アカウントを選択します。
7. 行のリストの一番上に行を追加する場合は **追加** を、リストの一番下に行を追加する場合は **アペンド** を選択します。
8. **説明** フィールドに、イベントの説明を入力します。
9. **配賦の種類** のフィールドが **割合** の場合、 **配賦の割合** フィールドに配賦の割合を指定します。 割合は 0 (ゼロ) から 100 の間である必要があります。 **配賦割合** フィールドを空白のままにした場合、割合は 0 と見なされます。 すべてのパーセンテージの合計は、ページ下部の **合計割合** フィールドに表示され、100 に等しくなければなりません。
10. **月の終了日** フィールド で、イベントの有効期間を月数で指定します。 トランザクションの繰延の有効期限は、この値に基づいて自動的に入力されます。
11. トランザクションの転記時に収益を自動的に認識するには、**転記時に認識** チェック ボックスをオンにします。 このチェック ボックスをオフのままにした場合は、収益を手動で認識する必要があります。
12. **認識アカウント** フィールドで、イベントで延期スケジュール全体とは異なる勘定を使用する場合に、イベントの認識勘定を選択します。 このフィールドは、**転記時に認識** チェック ボックスと共に使用されます。
13. 必要となる明細行ごとに手順 7 から 12 を繰り返します。
14. **保存** を選択します。
