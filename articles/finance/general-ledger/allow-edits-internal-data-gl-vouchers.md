---
title: 総勘定元帳伝票の内部データの編集を許可する
description: この記事では、総勘定元帳伝票の内部データを編集する方法に関する情報を提供します。
author: kweekley
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 6e346c6ff881d3a33743196b45247493fd19ed1d
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573254"
---
# <a name="allow-edits-to-internal-data-on-general-ledger-vouchers"></a>総勘定元帳伝票の内部データの編集を許可する

[!include[banner](../includes/banner.md)]


会計入力を総勘定元帳に転記する場合、**説明** フィールドは多くの場合、社内ノートやドキュメントを格納するために使用されます。 情報が正しくない場合、混乱が発生し、期間終了の決算が困難になる可能性があります。 この機能により、総勘定元帳の転記された伝票の **説明** フィールドを編集して、会計マネージャまたは会計監修者が誤りを修正できます。

総勘定元帳の転記伝票に対する変更は、内部的なデータに限定されます。 この機能では、金額、転記日付、勘定科目、トランザクション通貨などのデータを編集することはできません。 このデータを変更すると財務諸表の外部レポートに影響が生じ、新しい総勘定元帳の伝票からのみ行う必要があります。

> [!NOTE]
> Dynamics 365 Finance バージョン 10.0.29 の場合、この機能は **説明** フィールドの編集に限定されます。

## <a name="edit-internal-data-on-general-ledger-vouchers"></a>総勘定元帳伝票の内部データの編集

総勘定元帳伝票の内部データを編集する前に、**機能管理** ワークスペースの **総勘定元帳伝票の内部データの編集を許可する** を有効にする必要があります。
機能を有効にした後、転記された伝票を編集するユーザーを、会計マネージャまたは会計監修者ロールに割り当てる必要があります。 セキュリティ ロールをカスタマイズすると、他のロールにもアクセス許可を追加できます。

編集プロセスは、伝票トランザクション ページからのみ許可されます。

1. **総勘定元帳** > **照会およびレポート** > **伝票トランザクション** の順に移動します。
2. **SysQuery** ダイアログ ボックスで、伝票を選択する検索基準を入力します。
3. 編集する伝票の明細行を選択し、**伝票の編集** > **内部伝票データの編集** を選択します。

    [![伝票トランザクション ページ](./media/voucher-transactions-page.png)](./media/voucher-transactions-page.png)
    
**内部伝票データの編集** ページでは、選択した各行に次のデータが表示されます。
  
  - 勘定科目
  - アカウント名
  - 伝票
  - 現在の説明
  - 新しい説明

    [![仕訳伝票。](./media/edit-internal-voucher-data.png)](./media/edit-internal-voucher-data.png)
    
> [!NOTE]
> **新しい説明** フィールドのみ編集できます。 既定では、この値は **現在の説明** フィールドの値に一致します。この値により、説明に小さな誤りをすばやく修正できます。

4. 各行の **新しい説明** フィールドを変更するか、各行から説明を削除します。

   同じ値で複数の行を更新する必要がある場合は、次の手順に従います。

      1. 編集する行を選択し、**選択したレコードの一括更新** を選択します。
      2. **編集するフィールド** フィールドで、編集するフィールドを選択します。 現在、ルックアップには **新しい説明** フィールド だけが含まれます。
      3. **新規の値** フィールドで、新しい説明を入力します。
      4. **更新プログラム** を選択します。 選択したレコードはすべて新しい値で更新されます。

      [![レコードを選択した一括更新ダイアログボックス](./media/bulk-update-selected-records.png)](./media/bulk-update-selected-records.png)
    
5. **編集の理由** フィールドに、編集が行われた理由を説明する注記を入力します。 このメモは、**伝票編集ページの監査証跡** に表示されます。

   同じ伝票に対して複数の編集を行い、各編集を追跡します。

## <a name="audit-trail-of-voucher-edits"></a>伝票の編集の監査証跡

監査証跡は、この機能を通じて行われた変更を追跡するために特別に管理されます。 伝票編集の監査証跡にアクセスするには、次の 2 つの方法があります。

  - **総勘定元帳** > **照会およびレポート** > **伝票トランザクション** の順に移動します。 **伝票照会** ページで、**伝票の編集** > **伝票の編集の監査証跡** を選択します。 選択した伝票レコードについてのみ監査証跡が表示されます。 
   
    この方法で照会を開始することにより、1 つの伝票レコードに対して行われたすべての編集に焦点を合わせできます。
  
  - **総勘定元帳** > **定期処理タスク** > **伝票編集の監査証跡** に移動します。 ダイアログ ボックスで、編集の監査証跡を表示する伝票を指定する基準を入力します。 すべての伝票の監査証跡を表示するには、条件を空白のままにして、**OK** を選択します。 
    
    この方法で照会を開始することにより、特定の日付または特定のユーザーによって行われた編集をフィルタ処理できます。

**編集の監査証跡** ページには、次の情報が表示されます。

- **作成日時** - 編集の日時。
- **編集の理由** - ユーザーが編集用に入力した理由。
- **作成者** - 編集を作成したユーザー。

各監査証跡の詳細を表示するには、**作成日時** の値をドリルダウンします。 **編集された伝票プロパティの表示** ページには、前の説明や更新された説明など、元の編集ページと同じ情報が表示されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
