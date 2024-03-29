---
title: 請求スケジュールを終了する
description: この記事では、サブスクリプション請求管理の請求スケジュールおよび請求スケジュール明細行を終了する方法について説明します。
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
ms.openlocfilehash: 4fce23f3cf35ef8c388ce13fc422f268a2bd8e32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872560"
---
# <a name="terminate-billing-schedules"></a>請求スケジュールを終了する

[!include [banner](../includes/banner.md)]

この記事では、サブスクリプション請求管理の請求スケジュールおよび請求スケジュール明細行を終了する方法について説明します。 請求スケジュールを終了する場合は、**アクティブ** ステータスが必要です。 ステータスは **保留** に設定できません。 同様に、請求スケジュール明細行を終了する場合は、**アクティブ** ステータスが必要です。 請求スケジュール行を終了すると、請求書作成スケジュールのヘッダー セクションは影響を受けません。

請求スケジュールまたは請求スケジュール行を終了するには、次のいずれかの場所に移動します。

- **すべて/有効な請求スケジュール** リスト ページ
- **すべての請求スケジュール** ページの特定の請求スケジュール
- **すべての請求スケジュール** ページの特定の請求スケジュール明細行

> [!NOTE]
> 複数の請求スケジュールを同時に終了する場合は、**一括終了処理** ページを使用します。

## <a name="terminate-a-billing-schedule-or-line"></a>請求スケジュールまたは明細行を終了する

請求スケジュールまたは請求スケジュール明細行を終了するには、次のステップに従います。

1. 請求スケジュールまたは請求スケジュール明細行を選択し、**終了** を選択します。 
2. **終了日**、**終了タイプ**、および **理由コード** の各フィールドを設定 します。
3. **クレジット オプション** フィールドを **クレジットの発行** に設定します。
4. **終了** を選択します。

請求スケジュールのステータスは、選択した終了タイプに基づいて変更されます。 終了タイプとして **残数請求** を選択した場合、請求スケジュールのすべての明細行のステータスは **最終請求** になります。 請求スケジュールのステータスは、最後の請求書が処理されるまで **アクティブ** のままです。 最後の請求書が処理された後で、ステータスが **終了** に更新されます。 終了タイプとして **スケジュールの調整** を選択した場合、請求スケジュールのすべての明細行のステータスはただちに **終了** に更新されます。

## <a name="terminate-a-billing-schedule-or-line-and-apply-a-refund"></a>請求スケジュールまたは請求明細の終了と払戻の適用

請求スケジュールまたは請求スケジュール明細行を終了して、払戻を適用するには、次のステップに従います。

1. 請求スケジュールまたは請求スケジュール明細行を選択し、**終了** を選択します。
2. **終了日**、**終了タイプ**、および **理由コード**、および **クレジット オプション** の各フィールドを設定します。
3. **払戻で終了** を選択します。 **一括終了処理** ページが表示され、請求スケジュールを示すようにフィルタ処理されます。
4. **プレビューの表示** を選択して、請求スケジュール明細行を表示してから、**プロセス** を選択します。

クレジットが処理された後、**請求詳細の表示** ページを開き、請求スケジュールに適用されたクレジットを確認します。 クレジット金額が 0 より多い場合は、すべての将来の未請求の明細行が削除され、請求スケジュールに適用されたクレジットの負の金額を表示する請求詳細行に置き換えます。

### <a name="view-example"></a>例を表示

請求スケジュールには次の情報があります。

- 開始日は 2020 年 1 月 1 日です。
- 終了日は 2020 年 12 月 31 日です。
- 請求期間の金額は月当たり 100.00 になります。
- 1 月から 7 月の請求期間に対して請求書が作成されました。
- 契約の終了日は 2020 年 6 月 15 日です。

クレジット調整が処理されると、**請求詳細の表示** ページから将来のすべての請求期間 (8~12 月) が削除 されます。 クレジット調整行は、7月の請求期間後に追加されます。

- 6 月 16 日～7 月 31 日、クレジット金額は 150.00

未定収益機能を使用すると、**未定収益仕訳帳エントリ監査** ページが終了エントリで更新されます。

## <a name="terminate-a-billing-schedule-or-line-without-applying-a-credit"></a>クレジットを適用せずに請求スケジュールまたは請求明細を終了する

クレジットを適用せずに請求スケジュールまたは請求明細を終了するには、次のステップに従います。

1. 請求スケジュールまたは請求スケジュール明細行を選択し、**終了** を選択します。
2. **終了日** フィールドを設定します。
3. **終了タイプ** フィールドを **調整なし** に設定します。 **クレジット オプション** フィールドが自動的に **クレジットなし** に設定されます。
3. **理由コード** フィールドを設定します。
4. **終了メモ** フィールドに、必要な追加のメモを入力します。
5. **終了** を選択します。 

終了が処理されると、終了日付後のすべての請求詳細行が削除されます。 これらの明細行には、終了日付を含む明細行が含まれます。終了した明細行に対して請求書を作成することはできません。 終了が削除されると、すべての終了明細行が **請求詳細の表示** ページに追加され、請求が可能になります。

## <a name="fields"></a>フィールド

**請求詳細の表示** ページには、次のフィールドが含まれます。

| フィールド | Description |
|-------|-------------| 
| 退職日 | 請求スケジュールまたは請求スケジュール明細行を終了する日付を選択します。 |
| 終了タイプ | <p>終了タイプを選択します。</p><ul><li>**スケジュールの調整** – 終了日に行の請求期間をカットし、その行のステータスを **最終請求** に変更します。 品目の繰延スケジュールが存在する場合は、認識されなくなる必要がある金額を逆にすることで調整されます。 請求開始日が終了日より後の場合は、残りの請求期間が削除されます。</li><li>**残数請求** – 請求期間の残額を終了期間に追加し、行のステータスを **最終請求** に変更します。 品目の繰延スケジュールが存在する場合は、延期の終了日が更新されます。 請求開始日が終了日付より後の場合は、すべての残りの請求期間の合計金額が請求期間に追加され、残りの請求期間は削除されます。</li><li>**調整なし** – 指定された終了日に明細行の請求期間を終了します。 調整はされません。 この終了タイプを選択すると、**クレジット オプション** フィールドが **クレジットなし** に設定され、**日割払い** フィールドが **いいえ** に設定されます。 これらのフィールドはどちらも読み取り専用になり、変更できません。</li></ul> |
| 与信オプション | <p>請求スケジュール行を終了する際にクレジットが適用される方法を選択します。</p><ul><li>**クレジット調整** – 明細行が終了すると、請求スケジュールのクレジット調整を作成します。 クレジット調整は、請求スケジュールの将来の請求期間に表示されます。 また、次の請求期間の請求金額は、クレジットが請求スケジュールに適用されるまで自動的に調整されます。</li><li>**クレジットの発行** – 請求スケジュールまたは請求スケジュール明細行が終了したら、訂正票を作成します。</li><li>**クレジットなし** – 請求スケジュールまたは請求スケジュール明細行が終了しても、クレジット調整または訂正票を作成しません。 このオプションは、**調整なし** タイプの終了を使用して請求スケジュールを終了する場合にのみ使用できます。</li></ul><p>既定値は、**経常契約の請求書作成パラメータ** ページから取得されます。</p> |
| 理由コード | 終了の理由コードを選択します。 |
| 理由の説明 | 理由コードの説明。 |
| 終了通知 | 終了に関する注記を入力します。 |

<!--## Additional information-->
