---
title: RFQ を使用する要求の作成
description: このトピックでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法について説明します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05ff98b5fd95fa345d344e54d9116c73434e5de5
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018899"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a>RFQ を使用する要求の作成

[!include [banner](../../includes/banner.md)]

このトピックでは、価格および仕入先情報を RFQ プロセスから購買要求へ追加する方法について説明します。 このガイドで表示される例は USMF のデモ データ会社で使用でき、すべての手順を完了するためには管理者としてログインする必要があります。 このガイドのタスクは、調達担当者によって通常実行されます。


## <a name="create-a-requisition"></a>要求の作成
1. ナビゲーション ウィンドウで、**モジュール > 調達 > 購買要求 > 自分自身が作成した購買要求** の順に移動します。
2. **新規** を選択します。
3. **名前** フィールドに値を入力します。
4. **要求日** フィールドに日付を入力します。
5. **会計日** フィールドに日付を入力します。
6. **OK** を選択します。
7. **理由** フィールドで、値を入力または選択します。
8. **明細行の追加** を選択します。
9. **調達カテゴリ** フィールドで、ツリーのカテゴリーを選択し、**OK** を選択します。
10. **製品名** フィールドに値を入力します。
11. **数量** フィールドに、数値を入力します。
12. **単位** フィールドで、値を入力または選択します。
13. **保存** を選択します。
14. **ワークフロー** を選択して、ドロップ ダイアログを開きます。
15. **送信** を選択します。
16. ページを閉じます。
17. **送信** を選択します。

## <a name="reassign-a-workflow-task"></a>ワークフロー タスクの再割り当て
次のタスクは、RFQ を作成し、製品の仕入先から入札を取得します。 USMF のデモ データでは、要求ワークフローとルールが共に設定されているため、仕入先が選択されていない場合、または単価が明細行に対して 0 の場合でも、RFQ を作成する特定の作業者にタスクが割り当てられます。 このガイドで続行するには、別のユーザー (自分自身) にそのタスクを再度割り当てる必要があります。 自分が管理者としてログインしている場合にのみこれを行うことができます。  

1. **ワークフロー** を選択して、ドロップ ダイアログを開きます。
2. **履歴の表示** を選択します。
3. ページを更新します。
4. **追跡の詳細** セクションを展開します。
5. ツリーで、“行のワークフローが有効化された“ から始まる行を選択します。
6. **ワークフローの詳細を表示** を選択します。
7. **作業項目** セクションを展開します。
8. **再割り当て** を選択します。
9. **ユーザー** フィールドで、**管理者** を選択します。
10. **再割り当て** を選択します。
11. 2 つのページを閉じます。

## <a name="create-an-rfq"></a>RFQ の作成

1. ページを更新します。
2. **見積依頼** を選択します。
3. **購買組織** フィールドで、**USMF** を選択します。 要求明細行と同じ法人を選択する必要があります。  
4. 一覧で、選択された行をマークします。 自分の購買要求に複数の明細行がある場合は、RFQ に追加するすべての明細行を選択します。  
5. **OK** を選択します。
6. ページを更新します。
7. 情報ボックスが開いていることを確認し、**関連ドキュメント** のセクションを展開します。
8. **見積依頼** フィールドのリンクを選択し、先ほど作成した RFQ を開きます。
9. **ヘッダー** を選択します。
10. **追加** を選択します。
11. **仕入先** フィールドで、値を入力または選択します。
12. **追加** を選択します。
13. **仕入先** フィールドで、値を入力または選択します。
14. **送信** を選択します。
15. **OK** を選択します。
16. **回答の入力** を選択します。
17. アクション ペインで、**返信** を選択します。
18. **データを返信にコピー** を選択します。 これにより、数量や日付などのデータが RFQ から返信へコピーされます。  
19. **単価** フィールドに数値を入力します。 これは、仕入先から受け取った価格です。 仕入先からの追加情報を入力することもできます。  
20. **受け入れる** を選択します。
21. **OK** を選択します。

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a>仕入先および価格が請求に転送されていることを確認します。
1. ページを閉じます。
2. **明細行** を選択します。
3. **関連情報** を選択します。
4. **購買要求** を選択します。
5. RFQ の移動明細行を選択します。 価格および仕入先が要求書にコピーされていることを確認します。  
6. **ワークフロー** を選択して、ドロップ ダイアログを開きます。
7. [完了] を選択します。
8. ページを選択します。
9. [完了] を選択します。

