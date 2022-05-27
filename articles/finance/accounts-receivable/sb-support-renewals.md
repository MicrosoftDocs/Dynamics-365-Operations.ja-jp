---
title: サポートと更新
description: このトピックでは、販売注文のサポート プロセスとプログラム変更プロセスを設定して使用して、変更を伴う品目の請求スケジュールを作成する方法について説明します。
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
ms.openlocfilehash: 7de74f2b12e8e7201663ba78d936131b301b1ff9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685773"
---
# <a name="support-and-renewals"></a>サポートと更新 

このトピックでは、販売注文の入力時にサポート品目またはオブジェクト名を入力する方法について説明します。 これらの項目は、元のサポート契約や定期購読の請求書作成で請求スケジュールを作成するときに使用される総額の計算に使用されます。 たとえば、会社で顧客にサーバーを販売している場合、最初の年にデータ バックアップ定期売買を提供し、その定期売買を毎年更新するオプションを提供します。 *サポート品目* は最初の年の *定期購読* で、1 年おきに適用される付け替え項目は年ごとに適用されます。

サポート契約、契約契約、または両方の情報を入力できます。 サポート契約情報を入力すると、サポート品目だけが販売注文に追加されます。 付け替え契約の情報を入力すると、案内アイテムを使用して請求書作成スケジュールが作成されます。

## <a name="support-and-renewal-setup"></a>サポートと更新設定

**サポートとレベルの変更** ページでは、サポート品目および変更項目に対してさまざまなサポート レベルを設定できます。 サポートまたは変更は、元の品目金額の割合に対する割合にするか、標準金額にすることができます。

既定のサポート レベルを、**定期契約の請求書作成パラメータ** ページで選択できます。

たとえば、会社で次のようなサポート レベルとレベルを提供している場合があります。

| サポート レベル | サポート率 | 更新率 |
|---|---|---|
| 無制限 | 40% | 30% |
| 金 | 25% | 18% |
| 銀 | 20% | 14% |
| 銅 | 15% | 10% |

サポート レベルまたはプログラムレベルを作成するには、次の手順に従います。

1. **サポートと更新レベル** ページで、**新規** を選択します。
2. **サポート レベル** フィールドに一意の名前を入力します。
3. **説明** フィールドに説明を入力します。
4. **サポートの計算方法** フィールド で、サポートの計算方法を選択します。 **割合** を 選択した場合、**サポート割合** フィールドにサポート割合を入力します。
5. **計算方法の更新** フィールド で、サポートの計算方法を更新します。 **割合** を 選択した場合、**割合の更新** フィールドに割合を更新します。
6. **保存** を選択します。

### <a name="fields"></a>フィールド

**サポートおよび更新レベル** ページには、次のフィールドが表示されます。

| フィールド | Description |
|---|---|
| サポート レベル | サポート レベルまたはプログラムレベル ( **Gold** や **Silver**) の一意識別子。 |
| Description | サポートまたは更新レベルの説明。 |
| サポート計算方法 | レベル: **割合** または **標準金額** のサポート計算方法を選択します。 |
| サポート率 | サポート計算方法として **パーセンテージ** を選択した場合に、サポート品目の価格の計算に使用する割合を指定します。 計算方法として **標準金額** を選択した場合、金額はトランザクションの作成時に指定されます。 |
| 更新計算方法 | レベル: **割合** または **標準金額** の更新計算方法を選択します。 |
| 更新率 | 更新計算方法として **割合** を選択した場合に、更新品目の価格の計算に使用する割合を指定します。 計算方法として **標準金額** を選択した場合、金額はトランザクションの作成時に指定されます。 |

## <a name="support-and-renewal-process"></a>サポートおよび更新プロセス

サポートと更新の機能は、さまざまなサポート レベルを品目に適用し、サブスクリプション請求管理の更新情報を更新することができます。

サポートと更新機能を使用する前に、次のタスクを完了する必要があります。

1. **サポートと更新レベル** ページで、少なくとも 1 つのサポートまたは更新レベルを作成します。
2. **品目の設定** ページで、品目をサポート品目と更新項目に関連付します。 このタスクが必要になるのは、サポート品目や変更項目に対する既定値を設定する場合のみです。
3. **定期契約の請求パラメータ** ページで、新しい請求スケジュールの既定のサポートと更新設定を指定します。

品目にさまざまなサポート レベルを適用し、修正プログラムの情報を更新するには、次の手順に従います。

1. **すべての販売注文** ページで、販売注文を作成します。
2. **販売注文行** クイック タブで、品目を追加します。
3. **請求書** タブで、**サポートおよび更新 \> サポートと更新を追加** を選択します。
4. **サポートと移動可能なプロセス** ページのヘッダー セクションは、**定期契約の請求パラメータ** ページの設定で更新されます。 これらの値は、すべてのサポート品目および項目項目に適用されます。 (たとえば、請求頻度が **年に 1回** に設定されている場合、変更後の品目を作成した販売明細行には、年に 1 回の頻度が設定されます)。販売注文を既存の請求スケジュールに関連付ける場合は、**請求スケジュール番号** フィールドで値を選択します。
5. サポートまたはプログラムの開始日を変更するには、**開始日の上書き** オプションを **はい** に設定します。
6. サポート品目を追加または編集するには、**サポート** チェック ボックスをオンにし、**サポート品目** フィールドにサポート品目を入力します。 この品目が既存の販売注文に追加されます。
7. 更新品目を追加または編集するには、**更新** チェック ボックスをオンにし、**更新品目** フィールドに更新品目を入力します。 販売注文の請求時に、品目を含む請求スケジュールが作成されます。
8.  **OK** を選択します。
9. **生成** タブで、**請求書** を選択します。 販売注文が転記された時に、請求スケジュールが作成されます。 請求スケジュール情報を含む通知がメッセージの詳細に表示されます。
10. **すべて/アクティブな請求スケジュール** リスト ページで、請求スケジュール番号を選択して、**請求スケジュール** ページで請求スケジュールの詳細をレビューします。
11. **請求書作成スケジュール行** クイック タブで、作成された明細行の詳細をレビューするために **サポートと更新** を選択します。

> [!NOTE]
> 請求スケジュール行の更新を開始する必要がある場合は、**請求スケジュール** ページで行の **開始日** の値を編集できます。 その行の **請求の詳細の表示** ページを開いた場合、**請求開始日** フィールドが新しい日付で更新されます。 **請求終了日** の値は、請求頻度に基づいて再計算されます。 変更計画の開始日は、変更前の請求スケジュールの最初の請求書が作成および転記されていない場合にのみ更新できます。 最初の請求書を作成して転記した後は、開始日を編集できません。

サポート プロセスと部下プロセスは、販売注文でのみ使用できます。 販売注文に更新品目および項目を変更した場合は、新しい請求スケジュールを作成するか、その変更後の品目を既存の請求スケジュールに追加できます。

## <a name="support-and-renewal-audit"></a>サポートと更新の監査

**サポートと更新後の監査** ページで、販売注文のその変更項目から作成された請求スケジュール行の詳細を確認できます。 このオプションは、請求スケジュール行の品目が更新品目の場合にのみ使用できます。

請求スケジュール行のサポートと更新情報を編集するには、次の手順に従います。

1. **すべての請求スケジュール** ページで、請求スケジュール番号を選択します。
2. **請求スケジュール明細行** セクションで、明細行を選択して、**サポートおよび更新** を選択します。
3. サポートまたは更新品目に関する情報を確認します。
4. 必要に応じてサポート レベル、または更新割合、または金額を変更し、**変更の理由** フィールドに値を入力します。
5. **プロセス** を選択します。

### <a name="fields"></a>フィールド

**サポートおよび更新監査** ページには、次のフィールドが表示されます。

| フィールド | Description |
|-------|-------------|
| 品目番号 | 請求スケジュール明細行の品目番号です。 |
| 製品名 | 製品名。 |
| サポート計画レベル | 更新品目のサポート レベルを表示または変更します。 |
| 更新率 | 請求スケジュールで更新品目の単価を計算する際に使用する更新比率を入力します。 |
| 更新金額 | 請求スケジュールで更新品目の単価を計算する際に使用する更新がk額を入力します。 |
| 変更理由 | サポートおよび更新の情報を変更した理由を入力します。 **更新の割合**、**更新額**、または **サポート プラン レベル** 値を変更した際の理由を入力します。 |
| 元の販売品目 | 販売注文からの元の販売品目番号。 |
| 元の正味金額 | その品目の元の正味金額。 |
| 元のサポート レベル | その品目の元のサポート レベル。 |
| 元の更新率 | その品目の元の更新の割合。 |
| 元の更新金額 | その品目の元の更新額。 |
| **グリッド** | |
| 元のサポート レベル | 以前のサポート レベル。 |
| 元の更新率 | 以前の更新の割合。 |
| 元の更新金額 | 以前の更新額。 |
| 変更者 | 変更をおこなったユーザーの名前。 |
| 変更日時 | 変更が発生した時の日時。 |
| 理由 | 変更の理由。 |