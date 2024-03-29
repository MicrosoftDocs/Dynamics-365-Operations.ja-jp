---
title: 元帳決済
description: この記事では、元帳決済 ページを使用して元帳トランザクションを決済する、および決済を取り消す方法について説明します。
author: kweekley
ms.date: 11/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 6357629f83873437eb62a4839fafd8efd98fffc1
ms.sourcegitcommit: 9041fa6e00ecbdf1a1880659d9bdfff4d888f20e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/22/2022
ms.locfileid: "9800634"
---
# <a name="ledger-settlements"></a>元帳決済

[!include [banner](../includes/banner.md)]

元帳決済は、一般会計の借方および貸方トランザクションを照合するプロセスです。 借方額と貸方額の決済を使用して、勘定科目の残高と、その残高を構成する詳細トランザクションとの間で調整します。

決済済みトランザクションは照会やレポートから除外できます。 これにより、勘定科目の残高を構成するオープン元帳トランザクションの分析が容易になります。

> [!IMPORTANT] 
> 買掛金勘定 (AP) および売掛金勘定 (AR) モジュールは、請求書および支払の決済も含みます。 AR および AP の補助元帳で決済が行われると、対応する元帳エントリは自動的に決済されません。

## <a name="ledger-settlement-features"></a>元帳決済機能
Microsoft Dynamics 365 Finance バージョン 10.0.21 で、**高度な元帳決済を有効にする** オプションは **一般会計パラメーター** ページから削除されました。 高度な元帳決済が常に有効になりました。
Finance バージョン10.0.25 では、**元帳決済から年度末決済までの認識** 機能が導入されました。 この機能により、元帳決済と一般会計の年度末決済の基本的な機能が変更されます。 **機能管理** ワークスペースでこの機能を有効にする前に、[元帳決済から年度末決算までの認識](awareness-between-ledger-settlement-year-end-close.md) を参照してください。

## <a name="set-up-ledger-settlement"></a>勘定科目の設定
元帳決済を行う主勘定を選択する必要があります。 これらの主勘定を選択する方法は 2 種類あります。

1. **一般会計** > **元帳の設定** > **一般会計のパラメーター** の順に移動します。
2. **元帳決済** タブで、勘定科目表を選択し、そこから主勘定を選択します。
3. 元帳決済を行う主勘定を選択します。 勘定科目表はグローバルなので、選択した勘定科目表が割り当てられているすべての会社の主勘定は、元帳決済に対して選択した主勘定と同じです。

  または

1. **一般会計** > **定期処理タスク** > **元帳決済** の順に移動します。
2. **元帳決済勘定** を選択します。
3. ダイアログ ボックスで、元帳決済を実行する勘定科目表と主勘定を選択します。 このダイアログ ボックスはショートカットです。 ここに追加する主勘定はどれも、**一般会計パラメーター** ページに反映されます。

同じ基本的な手順を使用して、主勘定をいつでも元帳決済から削除できます。 主勘定を削除した場合、以前の元帳決済には影響しません。 ただし、主勘定およびトランザクションは **元帳決済** ページに表示されなくなります。

## <a name="settle-transactions"></a><a name="settle-transactions"></a>トランザクションの決済
元帳トランザクションを決済するには、次の手順に従います。

1. **一般会計** > **定期処理タスク** > **元帳決済** の順に移動します。
2. ページの上部にあるフィルターを設定します:

    - 日付範囲を選択します。 または、日付範囲を選択、または日付範囲コードを日付範囲に自動的に入力するように選択します。 会計年度のトランザクションに対して元帳決済の実行はお勧めしません。
    - 必要に応じて転記階層を変更します。 異なる転記階層のトランザクションは決済できません。
    - 主勘定および分析コードを個別に表示するためには、財務分析コード セットを選択します。

3. **トランザクションを表示** を選択すると、設定したフィルターと一致するすべてのトランザクションと、前のセクションで勘定科目表の設定時に指定した勘定の一覧が表示されます。

    - フィルターまたは分析コード セットのいずれかを変更する場合は、**トランザクションを表示** を再度選択する必要があります。
    - トランザクションを個々の主勘定にフィルター処理するには、**勘定科目** フィールドでフィルターを使用します。 別の主勘定に転記されるトランザクションに対する元帳決済の実行はお勧めしません。

4. 決済に使用する明細行を選択します。 ページの上部にある **選択済金額** フィールドの値は、選択した明細行の合計金額を反映して増減します。
5. トランザクションの選択が完了した後は、**選択済としてマークする** を選択します。 選択した各トランザクションの **マーク済** 列にチェック マークが表示されます。 また、グリッドの上にある **マークされた金額** フィールドの値は、マークした明細行の合計金額を反映して増減します。
6. **マークされた金額** フィールドの値が **0** (ゼロ) の場合は、**マークされたトランザクションの決済** を選択します。 マークされたトランザクションのステータスは **決済済** に更新されます。

    > [!IMPORTANT]
    > フィルターを適用したため、アクティブな法人の決済としてマークされたトランザクションはすべて、現時点で元帳決済ページに表示されていない場合でも決済されます。

## <a name="make-transactions-easier-to-find"></a>トランザクションを見つけやすくする
**元帳決済** ページには、決算に必要な取引を簡単に表示する機能があります。

- **マーク済** フィルターを使用して、**マーク済** チェックボックスが選択されているかどうかに基づいてトランザクションをフィルター処理します。
- **状態** フィルータを使用して、トランザクションの状態に基づいてフィルター処理できます。
- **絶対額で並べ替え** を選択して、金額を絶対値で並べ替えます。 これにより、同じ金額を持つ借方と貸方をグループ化できます。

## <a name="reverse-a-settlement"></a>決済を取り消す
誤って行われた決済を取り消すことができます。

1. [トランザクションの決済](#settle-transactions)セクションの手順1 から 3 に従って、必要なトランザクションを表示します。
2. **ステータス** フィルターで **決済済** を選択します。
3. 取消処理に使用する明細行を選択します。
4. **取消をマークしたトランザクション** を選択します。 決済 ID が同じすべてのトランザクションのステータスが **未決済** に更新されます。

    > [!IMPORTANT]
    > 決済 ID が同じトランザクションは、変更を適用していない場合でも取り消されます。 たとえば、4 つの明細行がマークされ、決済されています。 4 つの明細行の決済 ID はすべて同じです。 この 4 つの明細行のいずれかをマークし、**マークされたトランザクションの取り消し** を選択すると、4 つの明細行すべてが取り消されます。

## <a name="unmark-for-selected-users"></a>選択されたユーザー用のマーク解除
**選択されたユーザー用のマーク解除** を選択し、ユーザー ID ですべての法人の元帳決済トランザクションのマークを解除します。 たとえば、これにより、会計マネージャーは、決済を完了する前に休暇に出かけた、または組織を離れたユーザーのトランザクションのマークを解除することができます。 このアクションにより、トランザクションを他のユーザーが決済用にマークすることができます。


## <a name="unmark-all-transactions"></a>すべてのトランザクションのマークを解除
**すべてのトランザクションのマークを解除** を選択し、すべてのユーザーおよびすべての法人の元帳決済トランザクションすべてのマークを解除します。 このアクションは管理者ロールで使用できます。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
