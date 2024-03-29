---
title: ブローカー契約管理
description: この記事では、構成する管理タスクを自動化することによるブローカー契約管理について説明します。
author: t-benebo
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRBrokerContractManagement, MCRCustCategory, MCRCustCategoryHierarchy, PdsRebateAgreementLineInfoPart, MCRRoyaltyTable
audience: IT Pro
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 775136fc036818ab04194a3d5737756866548e45
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879757"
---
# <a name="broker-contract-management"></a>ブローカー契約管理

[!include [banner](../includes/banner.md)]

ブローカー契約管理により、企業は、ブローカーに支払う手数料の管理、追跡、支払に関連するタスクを自動化することにより、仲介契約を効率的に管理できます。

この記事では、ブローカー手数料を処理するための標準的なプロセスの概要を説明します:

- 取り決めブローカー契約の詳細を登録する
- 継続的な販売を通して交渉された契約を実行し、ブローカー請求を生成する
- 生成された請求を承認し、支払のために買掛金勘定 (A/P) に渡せるようにする
- 部分請求承認と差分会計の状況を処理する

## <a name="audience-and-purpose"></a>対象者および目的

この記事の情報は、以下の触接を持つ、セールス マネージャー、会計マネージャー、A/P マネージャーなどの立場にいる、エンタープライズの会社での業務の意思決定者を対象としています。

- ブローカーとの契約を交渉する
- ブローカー請求を処理し、手数料の支払を行うスタッフの管理

これらのロールのユーザーは、以下の目標を達成する方法を求めています:

- ブローカー契約とその状況の各種の定義に柔軟に対応します。
- 管理の負担、およびブローカー請求の追跡と処理に関連付けられるエラーを減らします。
- 将来の買掛金の見越計上によりキャッシュフロー予測の精度を高めます。

## <a name="broker-contract"></a>ブローカー契約

ブローカー契約は、ブローカーとの契約のレコードです。 事前に設定された売上目標の達成と引き換えに仲介企業が金銭的報酬を受け取るすることを認める交渉済み条件を指定します。

ブローカー契約は、**ブローカー契約** ページで登録されます。 **ブローカー契約** ページを開くには、**買掛金勘定** \> **ブローカーおよびロイヤルティ** \> **ブローカー契約** を選びます。


![ブローカー請求ページ。](./media/broker-contract-management-contract-page.png "ブローカー請求ページ")

契約には、ブローカー手数料を支払う当事者 (製品を購入する顧客または販売会社) に関する取り決め条件が含まれています。 この条件は、**諸費用コード** ページで設定されます。

**契約の詳細** セクションには、仲介の対象となる条件と品目が示されます。 売上目標の達成に対してブローカーが受け取る金銭的報酬は、**分割** に表示されます。

**ブローカー手数料** 請求金額の設定は、顧客がブローカー サービスの手数料を負担しないことを示します。 代わりに、販売会社が販売経費としてブローカー手数料を負担します。


> [!NOTE]
> 契約に、顧客がブローカー サービスの手数料を負担すると規定されている場合、**借方** セクションの **タイプ** フィールドが **顧客/仕入先** に設定されるように、関連付けられている雑費を設定する必要があります。 この場合は、会社はまず、顧客から手数料の支払を受け取り、ブローカーに負債を支払います。 販売の経費としてブローカー手数料を負担する販売会社である場合、**借方** および **貸方** セクションの両方の **タイプ** フィールドが **勘定科目** に設定されるように、関連付けられている雑費を設定する必要があります。 

借方勘定は、損益計算書の中間経費を受け取ります。貸方勘定は、請求金額が転記されたときからブローカー請求が承認され、請求書の転記の結果として実際の買掛金に移動されたときまで請求金額 (手数料) をホストする中間負債勘定です。

ブローカー契約の **契約の詳細** セクションには、仲介の対象となる条件と品目が示されます。 売上目標の達成に対してブローカーが受け取る金銭的報酬は、**分割** に表示されます。

条件に一致する販売注文に適用するには、契約の **ステータス** が **承認済** でなければなりません。

## <a name="sell-products-that-qualify-for-a-broker-commission-and-generate-a-claim"></a>ブローカー コミッションの対象となり、請求を生成する製品を販売します。

ブローカー契約の条件を満たす明細行を持つ販売注文を作成する場合、**販売注文** ページで **販売注文明細行** \> **表示** \> **ブローカー コミッション** の順に選択して関連する情報を表示します。

ブローカー手数料の見越計上は費用として処理されるため、販売注文から標準雑費ページを開いてブローカー コミッションにアクセスすることもできます。 注文明細行を選択し、**販売注文明細行**\>**財務**\>**雑費の管理** を選択します。

販売注文の請求書を転記するとき、通常の売上請求書のトランザクションだけでなく、次の転記が行われます。

- 請求明細行のブローカー請求が生成されます。
- ブローカー手数料を表す未収費用は、必要に応じて、中間負債および経費勘定に転記されます。

売上請求書仕訳帳に関連付けられている伝票トランザクションで、未収ブローカー手数料の転記を表示できます。

## <a name="review-and-process-claims"></a>請求を確認および処理する

請求が完全または部分的に承認されると、転記が A/P ポリシーによりサポートされている場合、仕入先請求書が作成されて天気されます。 これにより、仕入先請求の貸方は、通常の買掛金の処理に渡されます。

すべての請求は、**ブローカー請求** ページで表示できます。 手数料ごとに、**修飾** フィールドは、承認された後に仲介サービスのベンダーに支払われる手数料の金額を指定します。

![ブローカー請求ページ。](./media/broker-contract-management-contract-page.png "ブローカー請求ページ")

ページの下部セクションのフィールドは、請求書番号、請求書明細行の正味金額、および関連付けられている顧客トランザクションなど、発生元となる販売の請求書に関する詳細を指定することに注意してください。

請求を承認するには、**マーク** 列で、明細行のチェック ボックスを選択します。 アクション ウィンドウで、**承認** を選択します。

承認の結果として、次のイベントが発生します。

- 経費計上仕訳帳の転記が、見越負債勘定および見越経費勘定の両方の以前の中間納付を取り消します。
- 承認済ブローカー手数料の金額のブローカー要求 (仕入先) の請求書が作成されています。

    > [!NOTE]
    > 請求書承認プロセスの一部として自動的に、または手動で、ブローカー請求書の請求書を転記できます。 **買掛金勘定パラメーター** ページの **ブローカーとロイヤリティ** タブの **手動転記** フィールドは、転記の動作を制御するポリシーを指定します。

- ブローカー請求請求の転記の結果として、経費勘定が借方に転記されており、仕入先の買掛金勘定が貸方に転記されています。

    > [!NOTE]
    > 発注書の経費転記の購買支出が設定されている場合に、調達カテゴリの経費勘定番号が指定されます。 調達カテゴリ自体は、**買掛金勘定パラメーター** ページの **ブローカーとロイヤリティ** タブで定義されます。
    
**ブローカー請求** ページで、請求書に関連付けれている転記とドキュメント、ブローカーに作成された仕入先請求書番号を確認できます。 仕入先請求書が転記された場合 (自動または手動で) **請求書** タブの **日付** および **トランザクション通貨での金額** 適切な値が含まれます。 請求書がまだ保留中の場合は、これらのフィールドは空白になります。    

請求明細行の **承認済** フィールドに **見込み** フィールドと同じ金額が含まれていて、**差額** フィールドに 0 が含まれる場合、請求が未決済の問題がないため、閉じることができることを意味します。

## <a name="partially-process-claims"></a>請求の部分処理

顧客が販売注文の一部の単位を返品した場合、ブローカーは返品された数量に関連する手数料を得る資格を失った可能性があります。 この場合、一部の金額の 2 つ目の請求を承認する必要があります。 **買掛金管理** \> **ブローカーおよびロイヤリティ** \> **ブローカー請求** を選択し、請求を選択します。 **承認** フィールドに、合計数量から返品単位を引いた数を入力します。 アクション ウィンドウで、**承認** を選択します。

![請求の部分処理。](./media/broker-contract-management-process-claim.png "請求の部分処理")

**承認済** フィールドの値と **修飾** フィールドの値の間に違いがある場合、**差額** フィールドに記録されます。 これらの値は、請求がまだ未決済であることと、請求が終了と見なされる前に差額を処理する必要があることを示しています。

差額は、未決済の請求明細行を選択し、アクション ウィンドウで **終了** をクリックして処理される必要があります。

システムは、請求にはまだ未払単位の数があることを識別し、差額を説明する理由コードを入力するようにユーザーに求めます。

請求を閉じた後は、次のイベントが発生します。

- 経費計上仕訳帳の転記が、見越経費勘定の以前の中間納付を取り消します。
- 同じ転記が、見越負債勘定の以前の中間納付を取り消します。

**差異** タブの下の明細行は、支払いの承認が取り消されたブローカー手数料の金額を示しています。

顧客ではなく会社がブローカー手数料を支払うシナリオの場合、手数料の過剰支払または過少支払に関連付けられている利益または損失を損益計算書で考慮する必要はありません。 この場は、差額仕訳は差額の明細行に関連付けられません。 

顧客がブローカー手数料を支払う手数料シナリオで差額を処理する場合、システムが請求決算で差分仕訳を転記されることがわかります。 この仕訳は、ブローカー手数料損金処理勘定を借方/貸方に登録し、中間負債勘定を借方/貸方に登録します。 

> [!NOTE]
> 損金処理経費勘定番号は、**差異の理由** ページの **主勘定** フィールドで、特定の理由コードにより指定されます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
