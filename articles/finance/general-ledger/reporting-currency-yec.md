---
title: 年度末決算時の残高が不足しているレポート通貨
description: この記事では、年度末決算の実行時にレポート通貨がどのように残高不足になっているかについて説明します。
author: kweekley
ms.date: 12/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 31f79791330e076d4fbd7b604ba9f9c6cd9b9195
ms.sourcegitcommit: 44f0b4ef8d74c86b5c5040be37981e32eb43e1a8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2022
ms.locfileid: "9850262"
---
# <a name="reporting-currency-out-of-balance-when-the-year-end-close-is-run"></a>年度末決算時の残高が不足しているレポート通貨

**元帳決済と年度末決算の認識** 機能 (**認識** 機能) を有効にした後で、決済済の元帳トランザクションは、一般会計年度末決算が実行された次の会計年度の期首残高には含まれません。 決済された元帳トランザクションの除外は、元帳に対してレポート通貨が定義されている場合、年末の決済時に顧客に対する変更を示す場合があります。

元帳決済は、会計通貨についてのみ行われます。 元帳トランザクションが決済される際には、会計通貨借方と会計通貨貸方との間の貸方だけが検証によって確認されます。 これらの元帳トランザクションの報告通貨金額は検証されていないので、借方は貸方と等しくない場合があります。 また、元帳決済ではレポート通貨での利益/損失は自動的に計算および転記されません。

これらの制限のために、元帳決済を行う場合は、損益トランザクションがレポート通貨で存在する必要があります。 元帳決済に利益/損失が含まれていない場合は、年度末の決算を実行するときに残高からのメッセージが表示されます。

次の例では、年度末の終了の終了を実行する前に、この問題に対処するための手順を実行します。

## <a name="example-setup"></a>設定例

この例を設定するには、**認識** 機能を有効にし、元帳決済に対して勘定科目 110180 を設定します。 次の図は、DEIM 法人に転記された元帳トランザクションを示しています。 DE EUR の会計通貨は米国ドル (USD) で、報告通貨はユーロ (EUR) です。

![レポート通貨での転記された元帳トランザクション。](./media/reporting-currency-1.png)

**元帳決済** ページには、主要勘定 110180 の元帳トランザクションが示されます。 グリッドでを選択したまま (または右クリック)、**列を挿入** を選択します。 **レポート通貨の金額** 列 を追加して、トランザクション通貨、会計通貨、レポート通貨金額すべてが表示されるようにします。

![元帳決済ページに追加されたレポート通貨列の金額。](./media/Ledger-settlement2.png)

元帳の最初の 2 つの 100.00 EUR は 1 つのグループとして決済され、次の 2 つの元帳トランザクションは別の 200.00 EUR として決済されます。 (2 つのトランザクションには、決済 ID が異なります)。この設定は、組織が、異なる時間に決済され、決済日が異なる複数の元帳トランザクション のグループを持つことを示しています。 決済が完了すると、ステータスが **決済済** のトランザクションを表示するフィルタが実行される際に、**元帳決済** ページに次の情報が表示されます。

![元帳決済のページの決済済トランザクション。](./media/Settled-trans-filtered3.png)

**元帳決済** ページで 、**金額** 列のオンと保持 (または右クリック) し、**この列の合計** を選択します。 **レポート通貨列の金額** に対してこの手順を繰り返します。 決済を実行するには、会計通貨の差額が 0 (ゼロ) である必要があります。 ただし、レポート通貨の決済金額の検証はありません。 次の図は、レポート通貨の -27.79 USD の差を示しています。

![レポート通貨の差分。](./media/Difference4.png)

## <a name="year-end-close"></a>年度末決算

年度末の終了が 2022 年に対して実行された場合、プロセスは残高に関するエラーで終了します。 このエラーは、レポート通貨の元帳決済金額が 0 (ゼロ) に対して正味ではないという状態が原因で直接発生します。

![元帳決済金額に 0 (ゼロ) を示すエラー メッセージ。](./media/YEC5.png)

## <a name="posting-reporting-currency-gainloss"></a>レポート通貨での利益/損失を転記する

年度末決算を正常に実行するために、レポート通貨金額の差額を通常は利益または損失として、元帳決済に含める必要があります。 レポート通貨の利益/損失は、次に示す複数の方法で転記できます。

- 主要勘定が買掛金勘定または売掛金勘定である場合、これらのドキュメントの AR/AP 決済によって必要な利益/損失が生成されます。 請求書、支払、貸方表などからの対応する元帳トランザクションを決済する場合、その会計エントリを元帳決済に含める必要があります。
- 主要勘定が買掛金勘定または売掛金勘定に加え勘定である場合は、利益/損失を手動で入力する必要があります。 利益/損失を転記すると、会計エントリの詳細レベルは組織によって決定されます。
- 各主要勘定について、転記する必要があるレポート通貨の利益/損失の金額を識別します。

先ほど説明したように、この転記は **元帳決済** ページで実行できます。

1. 利益/損失を転記する日付範囲をフィルタ処理します。 月ごとの利益/損失を転記する場合は、各月をフィルター処理します。 会計年度ごとに利益/損失を転記する予定の場合は、年度全体をフィルター処理します。
2. 主勘定のフィルター。
3. ステータスをフィルタ処理して、**決済済** トランザクションのみを表示します。
4. **報告通貨の金額** 列に合計を追加します。
5. 利益/損失をより細かい粒度で転記する場合は、決済IDや財務分析コードでフィルタ処理を追加することができます。 **レポート通貨の金額** 列 の合計金額は、利益/損失が転記される金額を表します。
6. **一般会計 \> 仕訳入力 \> レポート通貨調節元帳** に移動します。
7. 利益/損失のトランザクション金額を入力します。 この仕訳帳では、調整はレポート通貨でのみ転記されます。 転記されるトランザクション通貨および会計通貨の金額は、常に0 (ゼロ) です。 この仕訳帳が以前     に使用されたことがない場合は、**総勘定仕訳 \> 元帳の設定 \> 仕訳帳名** で **レポート通貨調整** の仕訳帳タイプを持つ仕訳帳名を作成する必要があります。
8. メイン 勘定で手動入力が許可されている場合、この調整は転記されません。 したがって、**メイン アカウント** ページで **手動で入力できない** パラメータを一時的にオフにする必要がある場合があります。

![仕訳伝票ページの手動入力。](./media/Manual-entry6.png)

調整仕訳帳を転記して **元帳決済** ページに戻り、利益/損失を転記した主要勘定を選択します。 利益/損失調整は、元帳決済に含める必要があります。 報告通貨金額は0 (ゼロ) に正味を設定する必要はないので、以前のトランザクションを決済し、再度決済できますが、今回は利益/損失を含めることができます。 元帳決済の利益/損失の転記と、その利益/損失の決済の詳細は組織によってどのように正確に行う必要があります。

次の図は、トランザクションのトランザクション200 EUR 決済として再びマークされています。 この時刻には、利益/損失調整が含まれます。

![元帳決済ページでの利益/損失調整。](./media/gain-loss7.png)

トランザクションが決済された後に **ステータス** フィルタを 変更 し、ページに **決済済** トランザクションが表示されます。 **レポート通貨列の金額** の合計は 0 (ゼロ) になります。 年度末の終了処理を正常に実行できます。

![正常に終了した年度末決算。](./media/Zero-settled8.png)
