---
title: 定期契約請求の定期処理
description: この記事では、定期契約請求で使用できる定期処理について説明します。
author: JodiChristiansen
ms.date: 04/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: d834d1d7aa34448b4ef21606974538eb294b5d7d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904791"
---
# <a name="periodic-tasks-in-recurring-contract-billing"></a>定期契約請求の定期処理

この記事では、定期契約請求で使用できる定期処理について説明します。

## <a name="generate-invoice"></a>請求書の生成

**請求書の生成** ページで、**すべての請求スケジュール** および **請求の詳細を表示する** ページで設定した情報から大量の月次定期請求書を作成します。 請求書が作成されると、販売注文処理行の品目説明が、請求されるスケジュール行の品目説明および請求開始日と終了日で更新されます。

## <a name="generate-invoice-batch-processing"></a>請求書バッチ処理の生成

**請求書バッチ処理の生成** ページを使用して、定期的なバッチ プロセスにより定期請求書を作成します。 使用できるパラメータは、**請求書の生成** ページのパラメーターと同じですが、複数回実行できるバッチ プロセスに保存できます。

## <a name="price-update"></a>価格の更新

1 つのアクションで複数の請求スケジュールに対して複数の品目の価格を更新するには、価格更新ユーティリティを使用します。 価格は、指定された割合または金額に基づいて更新できます。 行の一覧には、品目の現在の単価だけが表示されます。 価格の更新後に価格は表示されません。

価格の更新ユーティリティについて次の点に注意してください。

- 特定の年の販売注文が既に作成されている場合 (品目を請求済みの場合)、行品目の価格には影響しません。
- 価格の更新ユーティリティは、状態が **アクティブ** または **保留中** の行品目に対して使用できます。 保留されている品目の場合は、保留中に **スケジュールを調節する** オプションが **いいえ** に設定されている必要があります。
- 価格の更新ユーティリティは、使用品目である行品目、エスカレーション、マイルストーン請求、または収益分解を使用する行品目には使用できません。

### <a name="price-update-example"></a>価格更新の例

請求スケジュールが作成され、更新された品目が追加されます。 単価は USD750 です。 品目の初年度の支払いは 2021 年 12 月 15 日です。 請求スケジュールは、2022 年 1 月から 12 月 31 日の期間に対して作成されます。

更新時に **請求書の生成** プロセスにより、2022 年度の販売注文が作成されます。 価格の更新ユーティリティを実行すると、価格が USD750 から USD800 に更新されます。

2022 年の販売注文と請求書スケジュールは影響を受けておらず、2022 年の請求スケジュールは既に請求済なので、単価は USD750 のままです。 2023 年度の請求スケジュールはまだ請求されていないため、2023 年度の請求スケジュール行と行の詳細は USD800 に更新されます。

### <a name="update-prices--flat-pricing-method"></a>価格の更新 – 一律の価格決定方法

一律の価格決定方法を使用する品目の価格を更新する場合は、割合または金額を指定して価格を引き上げることができます。

一律の価格決定方法を使用する品目に対して価格更新ユーティリティを実行するには、次の手順に従います。

1. **価格更新** ユーティリティ ページで、**一律** 価格決定方法を選択します。
2. **増加方法** フィールドで、品目の価格の更新に使用する増加方法を選択します。
3. 選択した増加方法に応じて、**割合** フィールドで割合を指定するか、**金額** フィールドで金額を指定します。
4. **含めるレコード** FastTab で、**フィルター** ボタンを使用してデータ フィルターを追加します。
5. **プレビューの表示** を選択してレコードの範囲を表示します。
6. 処理しない行がある場合、それをマークしてから **削除** を選択します。
7.  **OK** を選択します。

### <a name="update-prices--standard-pricing-method"></a>価格の更新 – 標準価格決定方法

品目レコードで品目の価格が変更された場合、その品目が標準価格決定方法を使用していると、品目をすべての請求スケジュール行に対して更新できます。

1. **価格更新** ユーティリティ ページで、**標準** 価格決定方法を選択します。
2. **含めるレコード** FastTab で、**フィルター** ボタンを使用してデータ フィルターを追加します。
3. **プレビューの表示** を選択してレコードの範囲を表示します。
4. 処理しない行がある場合、それをマークしてから **削除** を選択します。
5.  **OK** を選択します。

## <a name="mass-hold-processing"></a>一括保留処理

同時に **一括保留** ページを使用して、保留オプションを請求スケジュールに適用します。

1 つの請求スケジュール、または 1 つの請求スケジュール行を保留にするには、**すべての請求スケジュール** ページを開いて **保留に設定する** を選択します。 保留を削除するには、**保留の削除** ページを使用します。

### <a name="put-billing-schedules-on-hold"></a>請求スケジュールを保留にする

複数の請求スケジュールを保留するには、次の手順を実行します。

1. **一括保留** ページで、**オプションの処理** フィールドを **保留を適用する** に設定します。
2. **理由コード** フィールドで、新しい理由コードを選択します。
3. **スケジュールの調節** オプションを設定します。

    - **はい** – オプションを **はい** に設定した場合は、**保留日** フィールドで保留日を指定します。 保留日より後の請求スケジュール行が削除されます。
    - **いいえ** – 請求スケジュール行は変更されません。 状態のみが変更されます。 **保留中** に更新されます。

4. **含めるレコード** FastTab で、**フィルター** ボタンを使用してデータ フィルターを追加します。
5. **プレビューの表示** を選択してレコードの範囲を表示します。
6. 処理しない行がある場合、それをマークしてから **削除** を選択します。
7.  **OK** を選択します。

請求スケジュールの一覧に戻って、請求スケジュールの状態が **保留中** に変更されているのを確認する必要があります。

### <a name="remove-a-hold-from-several-billing-schedules"></a>複数の請求スケジュールから保留を削除する

1. **一括保留** ページで、**オプションの処理** フィールドを **保留を削除する** に設定します。
2. **理由コード** フィールドで、新しい理由コードを入力します。
3. **日付の削除** フィールドで、保留を削除する日付を選択します。
4. 必要に応 じて **再開日** フィールドおよび **繰延日** フィールドを設定します。 繰延日付は、繰延可能なすべての行に追加されます。
5. **含めるレコード** FastTab で、**フィルター** ボタンを使用してデータ フィルターを追加します。
6. **プレビューの表示** を選択してレコードの範囲を表示します。
7. 処理しない行がある場合、それをマークしてから **削除** を選択します。
8.  **OK** を選択します。

> [!NOTE]
> 保留を解除するには、**定期契約の請求パラメーター** ページで **保留ユーザー グループ オーバーライドの削除** の値を設定します。

たとえば、請求行の開始日が 2022 年 2 月 1 日で、終了日が 2022 年 2 月 28 日です。 請求金額は USD200 です。 **保留日** フィールドは、2022 年 2 月 10 日に設定されています。 したがって、2 月の期間は 2 月 10 日以後の日付を除外するよう調整されます。 新しい期間は 2 月 1 日から 2 月 9 日までで、金額は USD64.29 (毎日比例配分) です。 2 月 10 日以降のすべての請求スケジュール行が削除されます。

**保留の削除** プロセスが完了して **日付の削除** フィールドが 2022 年 2 月 10 日に設定されている場合は、2 つの請求期間が表示されます。 最初の請求期間は 2 月 1 日から 2 月 9 日までで、金額は USD64.29 です。 2 回目の請求期間は 2 月 10 日から 2 月 28 日までで、金額は USD135.71 です。

## <a name="mass-termination-processing"></a>一括終了処理

**一括終了** ページを使用して、指定している終了日が現在表示されている請求スケジュール行を終了します。

収益および経費繰延を使用している場合、**終了日** フィールドが **すべての請求スケジュール** ページで **スケジュールの調節** に設定されている請求スケジュールが払戻しの対象となります。

複数の要素配賦 (MEA) 機能を使用する請求スケジュールは、**一括終了** ページに表示されません。 その場合でも、請求スケジュールの終了機能を使用して個別の請求スケジュールを終了できます。

> [!NOTE]
> 現在 **請求書の生成** バッチに含まれる請求スケジュール行は、このプロセスでは使用できません。

各フィールドおよびプロセスの詳細については、[請求スケジュールの終了](terminate-billing-schedule.md) を参照してください。

## <a name="mass-archive-process"></a>一括アーカイブ プロセス

**一括アーカイブ** ページを使用して、複数の請求スケジュールをアーカイブします。 終了した請求スケジュールのみをアーカイブできます。

請求スケジュールがアーカイブされた後に、次のイベントが発生します。

- 状態が **アーカイブ済み** に変わります。
- 請求スケジュールは永久的にロックされます。
- 照会ページで請求スケジュール行を使用できなくなりました。

> [!NOTE]
> 請求スケジュールのアーカイブは永続的なアクションであり、取り消すことはできません。

請求スケジュールをアーカイブするには、次の手順に従います。

1. **一括アーカイブ** ページの **請求終了日** フィールドで、請求の終了日を指定します。 終了したすべての請求スケジュールを表示するには、このフィールドを空白のままにします。
2. **対象に含めるレコード** FastTab で、**フィルター** ボタンを使用して表示されたレコードを制限します。
3. **プレビューの表示** を選択します。
4. アーカイブしないレコ―ドがある場合、それをマークしてから **削除** を選択します。
5. **OK** を選択すると、ページにレコードがアーカイブされます。

## <a name="mass-stubbing-process"></a>一括スタブ プロセス

**一括スタブ** ページを使用して、選択したすべての請求スケジュール行を請求済 (スタブ) または未請求 (スタブの取消) にマークします。 スタブまたはスタブの取消は、多くの場合、以前に別のシステムで請求されインポートされた請求スケジュール行で実行されます。 スタブ済みの請求スケジュール行は、スタブ済みとして表示され、顧客の請求書は作成されません。

### <a name="stub-records"></a>スタブ レコード

1. **一括スタブ** ページの **プロセス オプション** フィールドで、**スタブ** を選択します。
2. **締日** フィールドで、プロセスを適用する行を指定する締日を設定します。 指定した締日以前に請求の開始日が設定されているレコードだけが表示されます。
3. **プレビューを表示** を選択して、スタブを行う行を表示します。
4. プロセスから行を除外するには、その行をマークしてから **削除** を選択します。
5. **プロセス** を選択し、行をスタブします。

### <a name="reverse-stub-records"></a>スタブ レコードの取消

1. **一括スタブ** ページの **プロセス オプション** フィールドで、**スタブの取消** を選択します。
2. **締日** フィールドで、プロセスを適用する行を指定する締日を設定します。 指定した締日以前に請求の開始日が設定されているレコードだけが表示されます。
3. **プレビューを表示** を選択して、スタブを取り消す行を表示します。
4. プロセスから行を除外するには、その行をマークしてから **削除** を選択します。
5. **プロセス** を選択し、行のスタブ取消します。

## <a name="update-completion-date-process"></a>完了日の更新プロセス

**完了日を更新する** ページを使用して、複数の請求スケジュールまたはユーザーに対する特定のマイルストーン品目の完了日を更新します。 **完了した率** 方法を使用するマイルストーン テンプレートで、品目の完了率を更新します。

1. **完了日の更新** ページで、**マイルストーン処理** に移動して **完了率を更新する** を選択します。
2. **合計の割合** フィールドで、完了した合計の割合を入力します。
3. マイルストーン テンプレートに関連する行の数を選択します。
4. **含めるレコード** FastTab で、**フィルター** を選択して特定の **エンド ユーザー アカウント**、**請求スケジュール数**、または **品目数** 値をフィルター条件として選択します。
5. **OK** を選択し、変更を処理します。 処理が完了すると、マイルストーン配賦に新しい行が追加されます。 この行は、マイルストーン テンプレートに対して完了した割合を表します。

## <a name="unbilled-revenue-mass-processing"></a>未請求収益一括処理

**未請求収益の一括処理** ページから、未請求の収益仕訳入力を作成したり、選択した 1 つ以上の請求スケジュールまたは請求書の詳細行に対して仕訳入力をスタブしたりできます。

- **仕訳入力の作成** – 複数の請求スケジュール行に対して未請求の収益仕訳入力を作成します。 **含めるレコード** FastTab にある **フィルター** ボタンを使用して、一覧に表示されるレコードの範囲を選択します。 未請求の収益仕訳入力が作成されていない請求スケジュール行だけが表示されます。 最初の仕訳入力が作成されます。 繰延品目については、繰延スケジュールも作成されます。
- **"仕訳入力のスタブ** – 未請求の仕訳入力が既に作成されている請求スケジュール行をマークします。 未請求の仕訳入力が既に別のシステムに転記されている場合は、このオプションが使用されます。 未請求の収益仕訳をスタブ済みとしてマークし、トランザクションを一般会計に転記しません。
- **スタブの仕訳入力の取消** – 処理されたスタブの仕訳入力を取り消します。 **スタブの仕訳入力** のプロセスでエラーが発生した場合、このオプションが請求スケジュール行の **スタブ済み** チェックボックスをオフにします。
- **スタブ請求の詳細行** – 未請求の収益を外部システムで処理した場合と、一部の請求詳細行がすでに請求されている場合にこのプロセスを使用します。 このプロセスにより、未請求の収益勘定に正しい金額が表示されます。
- **スタブ請求の詳細行の取消** – 任意の **スタブ請求の詳細行** アクションを取り消します。

**仕訳名** フィールドは、**仕訳入力の作成** を一般会計に転記するために使用されます。

> [!NOTE]
> スタブ プロセスでは、一般会計に金額を転記しません。 **仕訳名** フィールドは、一部のスタブ プロセスおよびスタブの取消プロセスでは使用できません。

### <a name="unbilled-revenue-stub-example"></a>未請求の収益スタブの例

請求スケジュールは、2021 年 10 月から 2022 年 9 月までの 1 年間に設定されます。 未請求の収益は外部システムで既に処理されています。 9 か月分の請求スケジュールが既に請求されています。 各請求期間の金額は、USD250 です。 年初に、未請求の収益に転記された合計金額は USD3,000 です。 9 か月後、USD2,250 はすでに請求され、未請求の収益として USD750 が残ります。

未請求の収益が 3 か月分しか残っていない請求スケジュールを設定するには、次の手順に従います。

1. **請求詳細の表示** ページで、2021 年 10 月から 2022 年 9 月までの期間の請求スケジュール、品目番号 S0001、月あたりの金額 USD250 を作成します。
2. 請求スケジュールの **仕訳入力の作成** を選択します。 USD 3,000 が未請求の収益に転記されます。
3. **スタブ請求の詳細行** 選択し、トランザクションの日付 2022 年 6 月 (9 か月) を指定します。 請求スケジュール行はプレビューに表示されません。 影響を受ける行はトランザクションの日付に基づいて表示されます。
4.  **OK** を選択します。

請求された最初の 9 か月はスタブされます。

[![請求詳細行スタブを表示する](./media/01_View-billing-detail-stub.png)](./media/01_View-billing-detail-stub.png)

未請求の収益から USD3,000 から取り消され、残された未請求の収益 USD750 が転記されます。 未請求の収益の転記を表示するには、行詳細ページの **更新** タブにある **未請求の収益仕訳入力監査** を選択します。

[![未請求収益仕訳入力の監査。](./media/02_Unbilled-rev-journal-audit.png)](./media/02_Unbilled-rev-journal-audit.png)

> [!NOTE]
> 前期間のすべての請求詳細行が請求済みの場合、未請求の収益仕訳入力は、任意の更新期間に対して作成できます。 たとえば、請求スケジュール行の 12 か月間 (2021 年 1 月から 12 月まで) の請求頻度は月 1 回です。 この行には、第 1 期間、第 2 期間 (2022 年 1 月から 12 月まで) と第 3 期間 (2023 年 1 月から 12 月まで) の 3 つの期間があります。 2021 年の最初の 12 か月以降のすべての請求詳細行に対する請求書が作成された後、未請求の収益の仕訳入力を第 2 期間に作成できます。
>
> 未請求の収益機能を使用する繰延品目については、請求行および割引行が処理されます。 これらの品目については、未請求の収益仕訳入力と、請求行と割引行の繰延スケジュールが作成されます。
>
> 繰延が可能でない品目、および繰延可能品目に対して作成された仕訳入力は、他の収益勘定の貸方に転記します。
