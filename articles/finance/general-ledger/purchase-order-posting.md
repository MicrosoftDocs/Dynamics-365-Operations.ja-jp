---
title: 発注書転記
description: この記事では、在庫転記プロファイル ページの [発注書] タブに関する情報について説明します。
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 38a9e2740232b18255109ba867fcdddd5b890774
ms.sourcegitcommit: 9310c943ac76896663e5604209034da9f8d6139c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151035"
---
# <a name="purchase-order-posting"></a>発注書転記

**在庫転記プロファイル** ページにある **発注書** タブは、発注書が一般会計へ転記する方法をコントロールするために使用されます。 発注書の一般会計には、次の 2 つの主要な活動が転記されます。 

- 製品受領書
- 請求書

現物トランザクション (製品受領) を発注書の一般会計に転記するには、次のチェックボックスをオンにする必要があります。

- **在庫および倉庫管理パラメーター** ページの **元帳で製品受領を転記する** チェックボックス。
- **品目モデル グループ** ページの **現物在庫の転記** および **見越計上負債** チェックボックス。

**在庫転記プロファイル** ページの主勘定は、次の転記タイプに対して指定する必要があります。

- 受領済の購入材料の原価
- 購買支出、未請求
- 購買、見越計上

財務トランザクション (請求書) が発注書の一般会計に転記するには、次の条件を満たしている必要があります。

- 発注書行で選択した項目の **品目モデル グループ** ページにある **資産在庫の転記** チェックボックスをオンにする必要があります。
- **在庫転記プロファイル** ページの主勘定は、次の転記タイプに対して指定する必要があります。
  - 請求済の購入材料の原価
  - 製品の購買支出
  - 支出の購買支出
  - 割引 (オプション)

## <a name="fixed-receipt-price-posting"></a>固定入庫価格の転記

品目の **品目モデル グループ** ページにある **在庫モデル** フィールドで **標準原価** オプションを選択する代わりに、固定入庫価格を製品の標準原価として使用できます。 **固定入庫価格** を使用する場合の主な違いは、在庫受領が転記される際に、現在の原価価格が品目に使用される点です。 **固定入庫価格** に対する原価の再評価プロセスはありません。財務的な更新を転記すると、転記時に現在の原価価格が使用されます。 受入時に使用される原価価格と請求書が異なる場合は、差異が固定入庫価格損益勘定に転記されます。

製品に固定入庫価格を使用するには、次を構成する必要があります。

- **品目モデル グループ** ページで、**現物在庫の転記** および **固定入庫価格** チェックボックスを選択します。 
- **在庫および倉庫管理パラメーター** ページで、**元帳で梱包明細を転記する** チェックボックスをオンにする必要があります。
- **在庫転記プロファイル** ページで、次の転記タイプに対して主勘定を指定します。
  - 固定入庫価格差益
  - 固定入庫価格損失
  - 固定入庫価格相殺

詳細については、[固定入庫価格](/supply-chain/cost-management/fixed-receipt-price.md) へアクセスしてください。

## <a name="purchase-charges-and-stock-variation-posting"></a>購買請求および在庫変動の転記

購買請求と在庫変動を考慮に入れる場合は、次を実行します。

- **請求書** タブの **買掛金勘定パラメーター** ページで、**元帳の請求勘定に転記** チェックボックスをオンにします。
- 発注書行で選択された品目の **品目モデル グループ** で、**現物在庫の転記**、**資産在庫の転記**、**製品入庫の見越計上負債** チェックボックスをオンにします。
- **調達パラメーター** ページで、**製品入庫の費用を生成する** チェックボックスをオンにします。
- **在庫および倉庫管理パラメーター** ページで、**元帳で梱包明細を転記する** チェックボックスをオンにする必要があります。

**在庫転記プロファイル** ページでは、次の転記タイプに対して主勘定を指定する必要があります。

- 購買支出、未請求
- 製品の購買支出
- 在庫変動

> [!NOTE]
> **請求金額** 転記タイプは、**元帳で掛売勘定に転記する** パラメーターが選択されている場合は使用されません。

詳細に関しては、[掛売勘定の会計原則に転記する](/supply-chain/cost-management/post-to-charge-account-accounting-principle.md) へアクセスしてください。

## <a name="sample-posting-profile-configuration"></a>転記プロファイル構成のサンプル

次の表では、主勘定のサンプルと説明を含む既定の転記タイプの例を表示しています。

- **決済勘定** 列は、転記タイプが決済勘定の場合を示します。 このアカウントに転記された金額は、後でトランザクションが転記された場合に自動的に取り消されます。 
- **P/F** 列は、現物転記の場合は **P**、財務転記の場合は **F** を表しています。 
- **次の** 列は、特定の転記タイプの主勘定が別の転記タイプと同じかどうかを表しています。 列の値は、通常使用される転記のタイプを表しています。

> [!NOTE]
> この主勘定および主勘定名は推奨にすぎません。 会計士と話し合い、<!--note from editor: Via Writing Style Guide.--> ビジネス ニーズに最適な構成を決定することをお勧めします。


| 転記タイプ | 主勘定の例 | 主勘定の名前の例 | 勘定タイプ | 借方か貸方か | 清算勘定 | P/F | 継承 | Description |
|--------------|---------------------|-------------------------|----------------|----------------|--------------------|----|----------|-----------|
| 受領済の購入材料の原価 | 140100</br>140101 | 材料在庫</br>出荷済未請求の材料 | 資産 | 借方 | 有効 | P | 請求済の購入材料の原価 | 発注書の製品入庫が転記されるときに使用され、勘定に対する相殺は、未請求の購買支出です。 この勘定の金額は、発注書の請求書が転記されたときに取り消されます。 |
| 購買支出、未請求 | 600180 | 材料受領 | 経費 | 借方 | 有効 | P | |発注書の製品受領書が転記されたときに使用します。 標準原価が使用された場合に購買価格の差異を追跡するために、入庫用の伝票が 2 つ作成されます。 最初の伝票の勘定に対する相殺は購買見越計上です。 2 番目の伝票上の相殺は、入庫した購入材料の原価と購買価格差異勘定の合計です。 この勘定に転記された金額は、発注書の請求書が転記されたときに取り消されます。 |
| 請求済の購入材料の原価 | 140100 | 材料在庫 | 資産 | 借方 | 無効 | 金  |受領済の購入材料の原価 | 発注書の請求書を転記するときに使用します。 この勘定に対する相殺は、製品の購買支出です。 この勘定は貸借対照表の在庫を表します。 通常、使用する勘定は、配送される単位原価、および販売注文に対して請求される単位原価で使用する勘定と同じです。 |
| 製品の購買支出 | 600180 | 材料受領 | 経費 | 貸方 | 有効 | 金  | |発注書の請求書を転記するときに使用します。 標準原価が使用された場合に購買価格の差異を追跡するために、請求書用の伝票が 2 つ作成されます。 この勘定に対する相殺は、領収書の転記で使用され、請求書の転記中に取り消される未請求の勘定の購買支出です。 貸借対照表の在庫勘定に反映されていない、請求時に購入した在庫のコストを表します。 これは、標準コスト品目購入で最も一般的に見られる購買価格差異の損益の転記です。|
| 固定入庫価格利益 (購入、固定入庫価格利益*) | 510310 | 購買価格差異 | 経費 | 貸方 | 無効 | 金 | 固定入庫価格損失 | 発注書の請求書を転記する際に使用され、品目の請求価格と既定の原価との間に差異があります。 差額が大きい場合は、この勘定が使用されます。 この勘定への相殺は、固定入庫価格相殺です。 |
| 固定入庫価格損失 (購入、固定入庫価格損失*) | 510310 | 購買価格差異 | 経費 | 借方 | 無効 | 金 | 固定入庫価格差益 | 発注書の請求書を転記する際に使用され、品目の請求価格と既定の原価との間に差異があります。 差額が小さい場合は、この勘定が使用されます。 この勘定への相殺は、固定入庫価格相殺です。 |
| 固定入庫価格相殺 (購入、固定入庫価格相殺*) | 140900 | 在庫変動 | 資産 | 両方 | 無効 | 金  | |発注書の請求書を転記する際に使用され、品目の請求価格と既定の原価との間に差異があります。 この勘定は、固定入庫価格利益と損失への相殺です。 |
| 請求金額 | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | 該当なし | この勘定はもう使用されていません。 代わりに在庫変動を使用します。 |
| 在庫変動 | 600170 | 在庫変動 | 経費 | 貸方 | 無効 | 両方 | | この勘定は、次の場合に使用します。 <ul><li>製品の入庫と請求書の間で単価に差異があります。</li><li>品目に対して請求費用が転記されます。</li><li>間接原価は<!--note from editor: Edit okay?--> 購入品目に追加されています。 </li><li>この勘定に対する相殺は、未請求の勘定の購買支出です。</li></ul> |
| 購買、見越計上 | 200140 | 未収購買 | 負債 | 貸方 | Y | P | |発注書の製品入庫が転記され、購買金額を見越計上するオプションが有効になっている場合に使用します。 |
| 入庫時の未収消費税 | 250500 | 未収消費税 | 負債 | 貸方 | Y | 両方  | |この勘定は、**在庫と倉庫管理パラメーター** で **現物税の転記** オプションを選択し、税金が設定された発注書がある場合に使用します。 この金額は、発注書を物理的に更新すると転記され (製品入庫)、発注書を財務的に転記する (請求書) と取り消されます。 |
| 固定資産入庫 (固定資産借方*) | 180100 | 有形固定資産 | 資産 | 借方 | 無 | 両方 | 両方 | この勘定は、固定資産の発注書行でオプションを選択するときに使用されます。 発注書の統合は、製品の入庫時または請求時に固定資産を取得するように構成されています。 固定資産の発注書の統合に関する詳細については、[調達による資産の取得](/fixed-assets/acquire-assets-procurement) へアクセスしてください。 |
| 支出の購買支出 | 618900 | 雑費 | 経費 | 借方 | 無 | 両方 | |品目の在庫が少ないときか、調達カテゴリが使用される発注書の製品入庫または製品の請求書を転記するときに使用します。 |
| 前払 | 132190 | 前払経費 | 資産 | 借方 | 無 | 両方 | | 発注書に対する前払請求書を処理するときに使用します。 |


\*括弧で示された値は、**伝票トランザクション** ページの **転記タイプ** フィールドで使用されている値を表しています。 **全般** タブの **伝票トランザクション** ページに、**転記タイプ** が表示されます。

## <a name="fixed-asset-posting-with-purchase-orders"></a>発注書を使用した固定資産の転記

**固定資産** モジュールを使用して発注書から固定資産の購入を計画する場合、**在庫転記プロファイル** ページの **発注書** タブにある **固定資産受領** の転記タイプを構成する必要があります。 詳細については、[固定資産の統合](/fixed-assets/fixed-asset-integration.md) および [買掛金勘定から資産を作成し取得する](/fixed-assets/tasks/create-acquire-assets-accounts-payable.md) へアクセスしてください。

## <a name="prepayment-purchase-order-invoice-posting"></a>発注書の前払請求書を転記する

発注書に対して **前払い請求書** 機能を使用する場合、**在庫転記プロファイル** ページの **発注書** タブで、**前払い** 転記タイプを選択する必要があります。 詳細については、[前払い請求書と前払いの違い](/accounts-payable/prepayments-invoices-vs-prepayments.md) へアクセスしてください。

## <a name="purchase-requisition-and-purchase-order-confirmation-posting"></a>購買要求と発注書の確認の転記

購買要求および発注書の確認では、事前債務および債務を一般会計に転記するように構成することもできます。 これらの転記は、転記の定義によってコントロールされます。 詳細については、[発注書の債務について](/dynamicsax-2012/appuser-itpro/about-purchase-order-encumbrances) にアクセスしてください。

## <a name="procurement-category-posting"></a>調達カテゴリの転記

すべての品目、品目グループ、または 1 つの品目に対する在庫の転記を設定する代わりに、カテゴリを設定し、調達カテゴリ別に元帳の転記をコントロールできます。 カテゴリの設定および製品への割り当てに関する詳細は、この記事にある [プロファイル構成のサンプル転記](#sample-posting-profile-configuration) へアクセスしてください

発注書または仕入先請求書とカテゴリを使用する場合、カテゴリ階層を **カテゴリ階層ロールの割り当て** ページにある **調達カテゴリ階層** タイプに割り当てる必要があります。

### <a name="vendor-invoices-with-procurement-categories"></a>調達カテゴリを含む仕入先請求書

組織で特定の購入にのみ発注書を使用する場合は、発注書以外に関連した請求書をさまざまな方法で処理できます。 たとえば、**買掛金勘定** で仕訳帳を使用したり、発注書の請求書を生成するために使用する **保留中の仕入先請求書** ページを使用したりして処理できます。 発注書以外に関連した請求書を作成する場合は、経費の種類ごとに調達カテゴリを作成する必要があります。 **在庫転記プロファイル** ページで、カテゴリを適切な経費勘定にマップする必要があります。

カテゴリの正確な数は、請求書を転記するときに使用する経費勘定の数によって異なります。 発注書以外の請求書の経費を処理する主勘定ごとに少なくとも 1 つの調達カテゴリが必要です。 1 つの主勘定に複数のカテゴリを使用できます。 これにより、使用する経費タイプの使用、検索、および報告が簡単になります。

### <a name="benefits-of-using-procurement-categories-for-vendor-invoices"></a>仕入先請求書に調達カテゴリを使用する利点

仕入先請求書に調達カテゴリを使用する利点は次のとおりです。

- 一貫したユーザー エクスペリエンス: 発注書以外のすべての関連経費に対して調達カテゴリを構成する場合、ユーザーは **保留中の仕入先請求書** ページを使用して、1 つの請求プロセスをトレーニングすることができます。
- 改善されたレポート エクスペリエンス: すべての品目と発注書以外のすべての関連経費の調達カテゴリを構成する場合、調達支出レポートは、仕入先、カテゴリなどごとに支出を分析します。
- 一貫したワークフロー: **保留中の仕入先請求書** を使用してすべての請求書を処理する場合は、ワークフローを 1 つ使用して、一貫したワークフローと承認プロセスを作成することができます。

## <a name="consignment-inventory-posting"></a>委託販売在庫の転記

委託販売在庫では、他の購入品目と同じ元帳の転記を使用します。 重要な違いは、在庫を受け取ったときに元帳トランザクションが記録されないという点です。 **在庫所有権の変更** 仕訳帳が転記されたときに所有権を組織に転送するために、品目の原価を記録する伝票が生成されます。 詳細については、[委託販売の設定](/supply-chain/inventory/consignment.md) へアクセスしてください。
