---
title: 在庫操作のトラブルシューティング
description: このトピックでは、在庫操作で作業をする際に発生する可能性がある問題の修正方法について説明します。
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832061"
---
# <a name="troubleshoot-inventory-operations"></a>在庫操作のトラブルシューティング

[!include [banner](../includes/banner.md)]

このトピックでは、在庫操作で作業をする際に発生する可能性がある問題の修正方法について説明します。

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a>在庫仕訳帳の "ワークフロー" ドロップダウン ダイアログ ボックスが見つらない。

### <a name="issue-description"></a>問題の説明

仕訳帳ページには **ワークフロー** ドロップダウン ダイアログ ボックスが表示されないか、関連するワークフロー操作を選択できません。

この問題は、次のサブセクションで説明するように、3 つの理由で発生する可能性があります。

### <a name="issue-resolution-1"></a>問題の解決 1

すべてのユーザーに問題が適用される場合は、承認ワークフローが仕訳帳名に割り当てられていないため、問題が発生している可能性があります。 問題を解決するには、次の手順に従います。

1. **在庫管理 &gt; 設定 &gt; 仕訳帳名 &gt; 在庫** に移動します。
1. リスト ペイン列から仕訳帳名を選択して、設定ページを開きます。
1. **一般** クイック タブで、**承認ワークフロー** オプションを *はい* に設定します。 変更の確認を求められたら、**はい** を選択します。
1. **ワークフロー** フィールドで、選択した仕訳帳名にに使用するワークフローを選択します。

### <a name="issue-resolution-2"></a>問題の解決 2

ワークフローでカスタマイズされたコードを使用している場合、システムをアップグレードすると問題が発生することがあります。 たとえば、仕訳帳ワークフローで **送信** ボタンはグレー表示され、送信を承認するために選択できない場合があります。

**送信** ボタンがグレー表示されている場合、ワークフローはカスタマイズされている場合があります (つまり、ワークフローの方法。`FormDataUtil` の `canSubmitToWorkflow()` は拡張されています)。 この問題を修正するには、次の例で構造を使用する `canSubmitToWorkflow()` の方法を拡張する方法を変更します。

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a>問題の解決 3

特定のユーザーにのみ問題が適用される場合、そのユーザーには、在庫仕訳帳に対するワークフロー操作の実行に必要なセキュリティ特権が付与されていない可能性があります。 影響を受ける各ユーザーに *在庫仕訳帳ワークフロー の維持* のセキュリティ特権が付与されているかを確認します。 既定では、この特権は同じ名前の関税に割り当てされ、その関税は *倉庫作業者* と *倉庫マネージャ* のロールに適用されます。

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a>在庫仕訳帳の状態がシステム ロック状態のままで、ワークフロー バッチ ジョブが機能しない。

### <a name="issue-description"></a>問題の説明

使用している在庫仕訳帳の 1 つが、ある操作によってロックされ、変更後はリリースされません。 たとえば、転記中に不明なエラーが発生した場合 (システム ロック操作)、仕訳帳はシステム ロック状態のままです。 この場合、ワークフロー作業項目ハンドラーは検証をロックしている間にエラーを修正します。

### <a name="issue-resolution"></a>問題の解決

Supply Chain Management の SQL Server インスタンスにログインし、**InventJournalTable.SystemBlocked** が *1* に設定されているかどうかを確認します。 その場合は、仕訳帳がロックの状態ではない事を確認してから、**InventJournalTable.SystemBlocked** を *0* にリセットしてください。

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a>自分の在庫仕訳帳ワークフローは完了したことがなく、仕訳帳を編集したり転記したりできません。

### <a name="issue-description"></a>問題の説明

仕訳帳承認ワークフローを送信すると、ワークフロー処理の応答が停止され、仕訳帳を編集または処理できます。

### <a name="issue-resolution"></a>問題の解決

ワークフロー処理が完了しないのはいくつかの理由があります。 次の問題を確認してください。

- **在庫管理 &gt; 設定 &gt; 在庫管理ワークフロー** に移動し、影響を受けるワークフローの構成を確認します。 詳細については、[仕訳帳承認ワークフロー](inventory-journal-workflow.md) を参照してください。
- ワークフローに例外またはエラーが発生する可能性があります。 影響を受けるワークフローの作業項目履歴を確認して、ワークフローを終了する申請エラーが含まれるかどうかを確認します。
- 在庫仕訳帳は、承認されている場合にのみ更新または編集できます。 リコールが有効な場合は、仕訳帳を取り消してみてください。 ワークフロー バッチ ジョブの実行が複数の理由で中断される場合があります。 このような理由の一部は、ワークフロー フレームワークの問題が原因である可能性があります。

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a>在庫仕訳帳ワークフロー条件は、行レベルではなく仕訳帳レベルでのみ適用されます。

### <a name="issue-description"></a>問題の説明

たとえば、原価金額に対して在庫仕訳帳のワークフロー条件を設定しようとする場合に、この問題が発生する可能性があります。 この条件を設定して、原価金額が 100 未満の場合にのみ手順 1 が実行されます。 その後他の条件を設定して、原価金額が 100 以上の場合にのみ手順 2 が実行されます。 その後、ワークフローを実行するとワークフロー履歴に表示される行は 1 行のみです。送信された値に関係なく、常に最初の条件が *真* として評価されます。

### <a name="issue-workaround"></a>問題の回避策

現在のリリースでは、在庫ワークフロー条件は、行レベルではなく仕訳帳レベルでのみ適用されます。 この動作は仕様です。 条件基準は、仕訳帳レベルの属性に対してだけ設定することをお勧めします。

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a>手持在庫リスト ページのフィルター ペインでは、期待した通りの結果のフィルタ処理は行されません。

### <a name="issue-description"></a>問題の説明

**手持在庫リスト**  ページのフィルター ペインにあるフィルタ―では、期待した通りの結果のフィルタ処理は行されません。

### <a name="issue-resolution"></a>問題の解決

この動作は仕様です。

 **手持在庫リスト**  ページは、使用可能なすべての分析コードを含む詳細な手持在庫テーブルから構成されています。 ただし、このページの一覧には概要情報が表示されます。 そのため、表示される分析コードに応じて値を集計することで、ソース テーブルからの行を結合することができます。

フィルターペインで設定したフィルターは、集計リストではなく、ソース テーブルに適用されます。 [これらの例](inventory-on-hand-list.md#examples) で示すように、この動作によって予期しない結果が生成される場合があります。

ただし、 [グリッドで指定されているフィルタ](inventory-on-hand-list.md#grid-filters) は集計リストに適用され  *ません* 。 これらのフィルターには、グリッドの上部にクイック フィルターが含まれており、各列のヘッダーに対してフィルターが適用されます。

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a>在庫仕訳帳で単位数量と単位数量が正しく機能しない。

### <a name="issue-description"></a>問題の説明

在庫仕訳帳の単位と数量を使用すると、次のいずれかの問題が発生する場合があります。

- リリースされた製品に換算単位が設定されている間は、在庫仕訳帳に単位数量または単位数量は表示されません。また、在庫仕訳帳で単位を変更したりは変更できます。
- 在庫仕訳帳には **数量** フィールドと **単位** フィールドが表示されますが、**単位数量** フィールド は表示されます。 単位を変更して数量を入力して仕訳帳を転記すると、仕訳帳には引き続きその数量の元の測定単位が表示されます。

### <a name="issue-resolution"></a>問題の解決

この問題を解決するには、次の手順に従います。

1. **機能管理** ワークスペースで、*在庫仕訳帳の測定単位と単位数量の使用* 機能が有効になっていることを確認します。 この機能により、**単位** と **単位数量** フィールドが仕訳帳に追加されます。
1. 機能が有効になった後は、次の方法で **数量**、**単位数量**、**単位** フィールドを使用します。

    - **数量** - リリースされた製品に対して定義されている既定の単位を使用して数量を指定します。 ただし、既定の単位自体は、ここには表示されません。 既定の単位と **単位** フィールドで選択した単位の間に換算が設定されている場合、**数量** フィールドは、**単位数量** フィールドと **単位** フィールドでの選択内容に基づいて自動的に更新されます。
    - **単位数量** – **単位** フィールドで選択された単位を使った数量を指定します。
    - **単位** - **単位数量** フィールドの値に適用する単位を選択します。

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a>"最小在庫管理単位の最大小数点以下桁数は 0 です" というエラー メッセージが表示されます。

### <a name="issue-description"></a>問題の説明

在庫トランザクションや在庫予約を転記しようとする場合、"最小在庫管理単位の最大小数点以下の桁数は 0 です" というエラー メッセージが表示されます。

この問題は、在庫トランザクションの数量が、フィールドでサポートされる精度レベルを下回る小数の値として指定されている場合に発生します。 たとえば、在庫トランザクションに対して数量 *0.5* が指定されている一方で、サポートされているのは整数数量のみです。 したがって、値は *0.5* の代わりに *1* にする必要があります。

### <a name="issue-resolution"></a>問題の解決

1. 在庫トランザクションの数量を丸めるには、SQL Server インスタンスで次のスクリプトを実行します。 このスクリプトは **inventTrans** テーブルの値を修正します。

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. **修正エラー** オプションが有効になっているという一貫性の確認を実行します。 このチェックは、**inventSum** テーブルの値を修正します。

> [!IMPORTANT]
> 実稼働環境でスクリプトを実行する前に、必要に応じてスクリプトを入念に編集し、テスト環境でテストしてから、結果のデータを確認することを強く推奨します。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]