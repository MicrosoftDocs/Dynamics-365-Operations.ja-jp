---
title: 販売注文の収益認識
description: この記事では、販売注文と請求書の収益を認識するための基本的な機能について説明します。 収益認識は、販売注文と、販売注文から作成された対応する請求書で使用できます。
author: bking
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: bb031b41c07aaff06b41830fb0c322503e9f27ec
ms.sourcegitcommit: 1909d18a74cef85aad020a6a7473281e451f58c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348241"
---
# <a name="revenue-recognition-on-sales-orders"></a>販売注文の収益認識

[!include [banner](../includes/banner.md)]

> [!NOTE]
> 収益認識機能は、機能管理を使用して有効にすることはできません。 現時点では、コンフィギュレーション キーを使用して有効にする必要があります。

この記事では、販売注文と請求書の収益を認識するための基本的な機能について説明します。 収益認識は、販売注文と、販売注文から作成された対応する請求書で使用できます。 時間/実費払プロジェクトを使用して販売注文を作成することもできます。

> [!NOTE]
> この記事の図では、列が非表示になっているか、グリッドに追加されており、概念をより詳しく示しています。 したがって、図中のページとデータが、製品に表示されるものと異なる場合があります。

## <a name="enter-a-sales-order"></a>販売注文の入力

次の販売注文が入力され、収益認識のために設定された 3 つの品目が含まれます。

[![販売注文の入力。](./media/revenue-recognition-so-basic-sales-order-header.png)](./media/revenue-recognition-so-basic-sales-order-header.png)

収益認識の 2 つの概念を次に示します。

- **収益額を決定します。** 収益額は、リリースされた製品の設定に基づいて計算されます。 収益額は顧客に表示されませんが、販売注文請求書の会計にのみ使用されます。 販売の一部として印刷される販売注文明細行および伝票は、引き続き単位/定価を表示します。
- **収益認識がいつ発生するかを決定します。** 収益スケジュールは、収益をどのように認識するかを決定するために使用されます。

    この例では、最初の品目 S0001 が **1O** (1回限り) の収益スケジュールに割り当てられています。 この明細行は、将来インストールが行われた後に収益が認識されるマイルストーン タイプのシナリオを表します。 したがって、収益はインストールが完了するまで延期されます。

    2 番目の項目である S0008 は、契約の事後サポート (PCS) 品目として設定されたサービス品目です。 継続的なエンジニアリング サービスは、12 か月間にわたって顧客に提供されます。 したがって、既定では、**12M** の収益スケジュールが製品に割り当てられます。 この品目は PCS 品目なので、契約の開始日と終了日を定義する必要があります。 既定では、契約の開始日と終了日は品目の詳細の設定タブにあります。収益スケジュールでは、**12M** の設定が定義されており、次の図に示すように契約条件が自動的に入力されます。

    [![収益スケジュール。](./media/revenue-recognition-so-basic-revenue-schedules.png)](./media/revenue-recognition-so-basic-revenue-schedules.png)

    3 番目の項目である S0012 はハードウェアであり、既定では収益スケジュールが割り当てられていません。 ハードウェアの収益は、品目が請求されるとすぐに認識されます。

## <a name="confirm-the-sales-order"></a>販売注文の確認

収益額と収益スケジュールに関する追加情報を表示するには、販売注文の操作ウィンドウの **管理** タブにある **収益認識** グループのボタンを使用します。 この時点では販売注文が確定されていないため、収益認識に使用されるボタンは使用できません。 これらのボタンは、販売注文がフルフィルメントを実行するステージを通じて進行するため、使用可能または使用不可になります。

[![販売注文ヘッダー。](./media/revenue-recognition-so-basic-sales-order-header-02.png)](./media/revenue-recognition-so-basic-sales-order-header-02.png)

最初の 3 つのボタンを使用して、収益認識の設定での品目の収益額の詳細を表示します。

- **収益額の配賦** - このボタンは、販売注文が確認された後または請求書が転記された後に使用できるようになります。 販売注文の確認および請求書の転記の両方で、収益を計算して、勘定項目で認識または繰延される価格を認識する必要があります。 設定によっては、計算される収益額が顧客に表示される単価と異なる場合があります。
- **新しい注文明細行で価格を再配賦** - このボタンは、販売注文が確認された後または請求書が転記された後に使用できるようになります。 再配賦プロセスは、現在の販売注文、請求後、または新しい販売注文に新しい明細行を追加した後に認識される必要がある収益を再計算するために使用されます。 どちらの場合も、新しい品目を追加すると契約が変更されます。 したがって、収益額を再配賦する必要があります。
- **収益額配賦の更新** - このボタンは、販売注文が確定した後で使用できますが、販売注文が請求された後は使用できなくなります。 この更新は、販売注文を確認することなく収益額の配賦を再実行するために使用されます。 販売注文が請求された後、収益額を再計算することはできません。

最後の 2 つのボタンを使用すると、収益スケジュールを持つ販売注文の品目の収益スケジュールに関する詳細が表示されます。

- **予定収益認識スケジュール** - このボタンは、販売注文が確定した後で使用できますが、販売注文が請求された後は使用できなくなります。 予定収益スケジュールを示すページが開きます。 最終スケジュールは、指定された出荷日を使用するのに対し、最終スケジュールでは実際の出荷日を使用するため、最終スケジュールは変更される場合があります。
- **収益認識のスケジュール** - このボタンは、販売注文が請求された後に使用できるようになります。 確認が行われるとき、または梱包明細が作成されるときは、最終の収益認識のスケジュールは作成されません。 販売注文が請求された場合にのみ作成されます。

次の例では、販売注文が確認されたときに収益額の配賦が発生しています。 収益額の配賦が異なる場合でも、**認識する収益** フィールドの合計金額は、顧客に請求される販売注文明細行の合計と同じである必要があることに注意してください。 たとえば、税を除く販売注文明細行の合計は、1,499 ドルになります。 したがって、**認識する収益** の合計も 1,499 ドルである必要があります。

[![収益額の配賦。](./media/revenue-recognition-so-basic-revenue-price-allocation.png)](./media/revenue-recognition-so-basic-revenue-price-allocation.png)

予定の収益認識スケジュールも作成されます。 収益スケジュールでは、**認識する収益** の値を繰り延べる金額として認識します。 品目 S0001 は 300 ドルではなく 321.21 ドルに繰り延べられ、品目 S0008 は 100 ドルではなく 160.61 ドルに繰り延べられます。 収益が繰り延べられていないため、品目 S0012 は予定スケジュールには表示されません。 転記が発生すると、品目 S0012 は収益勘定科目に直接 1,017.18 ドルで転記されます。

[![予定収益認識スケジュール。](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)](./media/revenue-recognition-so-basic-expected-rev-rec-schedule.png)

## <a name="create-the-packing-slip"></a>梱包明細の作成

次に、販売注文に対して梱包明細を作成できます。 梱包明細の転記時に収益は認識されません。 販売注文が確認されなかった場合、梱包明細を転記しても収益額の計算は行われません。 また、予定収益認識スケジュールまたは最終収益認識スケジュールの作成もトリガーされません。 梱包明細に対する収益を繰り延べるように品目のモデル グループが設定されている場合は、請求書の転記で使用される新しい繰延収益勘定ではなく、現在の転記プロファイルの勘定科目を使用して転記が続行されます。

## <a name="create-the-invoice"></a>請求書の作成

最後の手順は、販売注文の請求です。 請求書の伝票を確認すると、品目 S0001 と S0008 の収益が繰延 (321.21 + 160.61 = 481.82 ドル) になり、品目 S0012 の残余金額が収益 (1017.18) に転記されたことがわかります。 これらの値は、販売注文明細行の合計に一致する 1,499 ドルに加算されます。

[![伝票トランザクション。](./media/revenue-recognition-so-voucher-transactions.png)](./media/revenue-recognition-so-voucher-transactions.png)

請求書が作成された後、収益認識のための **収益額の配賦**、**新しい注文明細行への価格再配賦**、および **収益認識スケジュール** ボタンが使用できるようになりますが、**収益額配賦の更新** および **予定収益認識スケジュール** ボタンは使用できません。

[![利用可能な収益認識ボタンの可用性。](./media/revenue-recognition-so-basic-after-invoice-buttons.png)](./media/revenue-recognition-so-basic-after-invoice-buttons.png)

**収益額の配賦** ボタンはまだ使用可能で、収益額の計算を表示できます。 販売注文を確認後に何も変更しなかった場合は、請求書を転記しても、**認識する収益** フィールドで計算された金額は変更されません。

予定収益認識スケジュールが削除され、最終収益認識スケジュールに置き換えられます。 収益スケジュールの詳細は販売注文明細行ごとに管理され、契約上の責務が満たされたときに、繰延収益を実際の収益にリリースするために使用されます。

[![最終収益認識スケジュール。](./media/revenue-recognition-so-revenue-recognition-schedule.png)](./media/revenue-recognition-so-revenue-recognition-schedule.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
