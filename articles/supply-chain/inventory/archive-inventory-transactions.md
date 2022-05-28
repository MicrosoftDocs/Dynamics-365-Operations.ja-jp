---
title: 在庫トランザクションをアーカイブする
description: このトピックでは、システムのパフォーマンスを向上させるために在庫トランザクション データをアーカイブする方法について説明します。
author: yufeihuang
ms.date: 05/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8b766d306f31fc531f33aa29e1f96048bbd90085
ms.sourcegitcommit: e18ea2458ae042b7d83f5102ed40140d1067301a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/10/2022
ms.locfileid: "8736064"
---
# <a name="archive-inventory-transactions"></a>在庫トランザクションをアーカイブする

[!include [banner](../../includes/banner.md)]

時間の経過と共に、在庫トランザクション テーブル (`InventTrans`) は拡大し、データベース容量を消費します。 したがって、テーブルに対して実行されるクエリの速度は徐々に低下します。 このトピックでは、システム パフォーマンスを向上させるために、*在庫トランザクション アーカイブ* 機能を使用して在庫トランザクションに関するデータをアーカイブする方法について説明します。

> [!NOTE]
> 選択した決算済元帳期間にアーカイブできるのは、財務更新済の在庫トランザクションのみです。 アーカイブするには、財務更新済の出荷在庫トランザクションの払出ステータスが *売却済* で、入庫在庫トランザクションの受入ステータスが *購買済* である必要があります。

在庫トランザクションをアーカイブすると、関連のすべてのトランザクションが `InventTransArchive` テーブルに移動されます。 在庫払出トランザクションと在庫受入トランザクションは、品目ID (`itemId`) と在庫分析コード ID (`inventDimId`) の組み合わせに基づいて個別にアーカイブされ、集計された払出トランザクションと受入トランザクションに転記されます。

`itemId` と `inventDimId` の組み合わせに払出トランザクションまたは受入トランザクションが 1 つだけ含まれている場合、トランザクションはアーカイブされません。

## <a name="turn-on-the-feature-in-your-system"></a>システムで機能を有効化する

このトピックで説明する機能がシステムにまだ含まれていない場合は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) に移動して、*在庫トランザクション アーカイブ* 機能を有効にします。 この機能は、いったん有効にすると無効にできません。

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a>在庫トランザクションをアーカイブする前に考慮する点

在庫トランザクションをアーカイブする前に、次の業務シナリオを考慮する必要があります。これらは操作の影響を受けるためです。

- 発注書明細行などの関連ドキュメントから在庫トランザクションを監査する場合、在庫トランザクションはアーカイブ済として表示されます。 アーカイブされたトランザクションを確認するには、**在庫管理 \> 定期処理タスク \> クリーンアップ \> 在庫トランザクション アーカイブ** の順に移動する必要があります。
- アーカイブされた期間の在庫決算はキャンセルできます。 在庫決算をキャンセルするには、まず関連する期間の在庫トランザクション アーカイブを取り消す必要があります。
- アーカイブされた期間に対して標準原価換算は行えません。 標準原価換算を行うには、まず関連する期間の在庫トランザクション アーカイブを取り消す必要があります。
- 在庫トランザクションをアーカイブすると、在庫トランザクションから取得された在庫レポートが影響を受ける可能性があります。 これらのレポートには、在庫エイジング レポートおよび在庫金額レポートが含まれます。
- 在庫予測は、アーカイブされた期間の期間中に実行されると影響を受ける場合があります。

## <a name="prerequisites"></a>必要条件

在庫トランザクションは、次の条件が満たされた期間にのみアーカイブできます。

- 元帳期間は決済されている必要があります。
- 在庫決算は、アーカイブの終了日以降に実行する必要があります。
- 期間は、アーカイブの開始日の 1 年以上前の日付である必要があります。
- 既存の在庫再計算が作成されていない必要があります。

## <a name="archive-inventory-transactions"></a>在庫トランザクションをアーカイブする

在庫トランザクションをアーカイブするには、以下の手順に従います。

1. **在庫管理** \> **定期処理タスク** \> **クリーンアップ** \> **在庫トランザクション アーカイブ** の順に移動します。

    **在庫トランザクション アーカイブ** ページが表示され、アーカイブされているプロセス レコードの一覧が表示されます。

    ![在庫トランザクション アーカイブ ページ。](media/archive-inventory-empty.png "在庫トランザクション アーカイブ ページ")

1. アクション ウィンドウで、**在庫トランザクション アーカイブ** を選択して、在庫トランザクション アーカイブを作成します。
1. **在庫トランザクション アーカイブ** ダイアログ ボックスの **パラメーター** クイック タブで、次のフィールドを設定します。

    - **元帳の決算済期間の開始日** – アーカイブに含める最も早いトランザクションの日付を選択します。
    - **元帳の決算済期間の終了日** – アーカイブに含める最も遅いトランザクションの日付を選択します。

    ![在庫トランザクション ダイアログ ボックス。](media/archive-inventory-dates.png "在庫トランザクション ダイアログ ボックス")

    > [!NOTE]
    > [前提条件](#prerequisites) を満たす期間のみを選択できます。

1. **バックグラウンドで実行** クイック タブで、必要に応じてバッチ処理の詳細を設定します。 Microsoft Dynamics 365 Supply Chain Management のバッチ ジョブの通常の手順に従います 。
1. **OK** を選択します。
1. 続行を確認するメッセージが表示されます。 メッセージを慎重に読み、続行する場合は **はい** を選択します。

    在庫トランザクション アーカイブ ジョブがバッチ キューに追加されたというメッセージが表示されます。 選択した期間の在庫トランザクションのアーカイブがジョブによって開始されます。

## <a name="view-archived-inventory-transactions"></a>アーカイブされた在庫トランザクションの表示

**在庫トランザクション アーカイブ** ページには、完全なアーカイブ履歴が表示されます。 グリッドの各行には、アーカイブが作成された日付、作成したユーザー、ステータスなどの情報が表示されます。

![在庫トランザクション アーカイブの履歴をアーカイブします。](media/archive-inventory-full.png "在庫トランザクション アーカイブの履歴をアーカイブする")

ページの上部にあるドロップダウン リストで、次のいずれかの値を選択して、グリッドに表示されるアーカイブをフィルター処理します。

- **有効** – 有効なアーカイブのみ表示し、取り消されたアーカイブは表示しません。
- **すべて** – 有効なアーカイブと取り消されたアーカイブの両方を表示します。

グリッド内のアーカイブごとに、次の情報が提供されます。

- **有効** – チェック マークは、アーカイブが有効かどうかを示します。
- **開始日** – アーカイブに含まれる最も古いトランザクションの日付。
- **終了日** – アーカイブに含まれる最も新しいトランザクションの日付。
- **スケジュール作成者** – アーカイブを作成したユーザー アカウント。
- **実行日** – アーカイブが作成された日時。
- **取り消し** – チェック マークは、アーカイブが取り消し済かどうかを示します。
- **現在の更新の停止** – チェック マークは、アーカイブが進行中で、一時停止中であることを示します。
- **状態** – アーカイブの処理ステータス。 このフィールドの値は、*待機中*、*進行中*、および *完了済* です。

グリッドの上にあるツール バーには、選択したアーカイブを操作する場合に使用できる次のボタンが表示されます。

- **アーカイブされたトランザクション** – 選択したアーカイブの詳細を表示します。 **アーカイブされたトランザクション** ページには、アーカイブ内のすべてのトランザクションが表示されます。

    ![アーカイブされたトランザクション ページ。](media/archive-inventory-transactions.png "アーカイブされたトランザクション ページ")

    **アーカイブされたトランザクション** ページで特定のトランザクションに関する詳細情報を表示するには、グリッドで特定のトランザクションを選択し、アクション ウィンドウで **アーカイブされたトランザクションの詳細** を選択します。 表示される **アーカイブされたトランザクションの詳細** ページには、元帳転記、関連する補助元帳参照、財務分析コードなどの情報が表示されます。

- **アーカイブの一時停止** – 現在処理されている選択したアーカイブを一時停止します。 一時停止は、アーカイブ タスクが生成された後にのみ有効になります。 そのため、一時停止が有効になる前に、短い遅延が発生する場合があります。 アーカイブが一時停止されている場合は、**現在の更新の停止** フィールドにチェック マークが表示されます。
- **アーカイブの再開** – 現在一時停止されている選択したアーカイブを再開します。
- **取り消し** – 選択したアーカイブを取り消します。 アーカイブを取り消しできるのは、アーカイブの **状態** フィールドが *完了* に設定されている場合のみです。 アーカイブが取り消されている場合は、**取り消し** フィールドにチェック マークが表示されます。

## <a name="extend-your-code-to-support-custom-fields"></a>カスタム フィールドをサポートするためにコードを拡張する

`InventTrans` テーブルに 1 つ以上のカスタム フィールドが含まれている場合は、名前の付け方に応じて、サポートするようにコードを拡張する必要がある場合があります。

- `InventTrans` テーブルのカスタム フィールドが `InventtransArchive` テーブルと同じフィールド名である場合は、1:1 でマップされていることを意味します。 したがって、カスタム フィールドを `inventTrans` テーブルの `InventoryArchiveFields` フィールド グループに入力するだけで済みます。
- `InventTrans` テーブルのカスタム フィールド名が `InventtransArchive` テーブルのフィールド名と一致しない場合は、マップするコードを追加する必要があります。 たとえば、`InventTrans.CreatedDateTime` というシステム フィールドがある場合、次のサンプル コードに示すように、別の名前 (`InventtransArchive.InventTransCreatedDateTime` など) で `InventTransArchive` テーブルのフィールドを作成し、`InventTransArchiveProcessTask` と `InventTransArchiveSqlStatementHelper` のクラスに拡張子を追加する必要があります。

次のサンプル コードは、必要な拡張機能を `InventTransArchiveProcessTask` に追加する方法の例を示しています。

```xpp
[ExtensionOf(classStr(InventTransArchiveProcessTask))]
Final class InventTransArchiveProcessTask_Extension
{

    protected void addInventTransFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTrans, ModifiedBy))
            .add(fieldStr(InventTrans, CreatedBy)).add(fieldStr(InventTrans, CreatedDateTime));

        next addInventTransFields(_selectionObject);
    }


    protected void addInventTransArchiveFields(SysDaSelection _selectionObject)
    {
        _selectionObject.add(fieldStr(InventTransArchive, InventTransModifiedBy))
            .add(fieldStr(InventTransArchive, InventTransCreatedBy)).add(fieldStr(InventTransArchive, InventTransCreatedDateTime));

        next addInventTransArchiveFields(_selectionObject);
    }
}
```

次のサンプル コードは、必要な拡張機能を `InventTransArchiveSqlStatementHelper` に追加する方法の例を示しています。

```xpp
[ExtensionOf(classStr(InventTransArchiveSqlStatementHelper))]
final class InventTransArchiveSqlStatementHelper_Extension
{
    private str     inventTransModifiedBy;  
    private str     inventTransCreatedBy;
    private str     inventTransCreatedDateTime;

    protected void initialize()
    {
        next initialize();
        inventTransModifiedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, ModifiedBy)).name(DbBackend::Sql);
        inventTransCreatedDateTime = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedDateTime)).name(DbBackend::Sql);
        inventTransCreatedBy = new SysDictField(tablenum(InventTrans), fieldNum(InventTrans, CreatedBy)).name(DbBackend::Sql);
    }

    protected str buildInventTransArchiveSelectionFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransArchiveSelectionFieldsStatement();
        
        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransModifiedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedBy)).name(DbBackend::Sql));
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1',  new SysDictField(tablenum(InventTransArchive), fieldNum(InventTransArchive, InventTransCreatedDateTime)).name(DbBackend::Sql));
        }

        return ret;
    }

    protected str buildInventTransTargetFieldsStatement()
    {
        str     ret;

        ret = next buildInventTransTargetFieldsStatement();

        if (inventTransModifiedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransModifiedBy);
        }

        if (inventTransCreatedBy)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedBy);
        }

        if (inventTransCreatedDateTime)
        {
            ret += ',';
            ret += strFmt('%1', inventTransCreatedDateTime);
        }

        return ret;
    }
}
```
