---
title: 輸送管理での運賃の調整
description: このトピックでは、運賃調整プロセスについて説明します。
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac07155e4dde77689b1994abfb8b30f45d5a5a30
ms.sourcegitcommit: b6686265314499056690538eaa95ca51cff7c720
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5014511"
---
# <a name="reconcile-freight-in-transportation-management"></a>輸送管理での運賃の調整

[!include [banner](../includes/banner.md)]

このトピックでは、運賃調整プロセスについて説明します。

運賃の調整は手動で行うか、あるいは自動的に実行するよう設定することができます。 運賃の自動調整を使用する場合は、どの運賃請求書が自動的に照合されるかを決定する基準を定義する監査マスターを設定する必要があります。

## <a name="the-freight-reconciliation-process"></a>運賃調整プロセス

運賃は、関連する出荷配送業者に関連付けられているレート エンジンによって計算されます。 積荷が確認されると、運賃請求書が生成され、そこに運賃が転送されます。 運賃は通常の請求プロセスに使用される設定に応じて、関連する元伝票 (発注書、販売注文、または移動オーダー) に雑費として配賦されます。 運賃調整プロセス (照合プロセスとも呼ばれます) は、出荷配送業者から運賃請求書が到着次第開始できます。 請求書は電子ファイルで、または紙面で受領することができます。 紙の請求書を受領した場合は、運賃請求書をテンプレートとして使用して電子請求書を生成できます。

[![運賃調整プロセス](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>手動調整

運賃を手動で調整する場合は、請求書の各明細行を、運賃請求書の明細行または請求対象となっている積荷の明細行と照合する必要があります。 この照合は **運賃請求書と請求書の照合** ページで行います。 請求明細行の金額が運賃請求書の金額と一致しない場合は、差額を調整する理由を選択する必要があります。 調整する理由が複数ある場合は、一致しない金額をそれら全体に分割できます。 調整の理由によって、差額の総勘定元帳への転記方法が決定されます。 請求書の全額の調整が明確にされると、承認のため送信され、仕訳帳が転記されます。 次の図で、運賃請求書の生成および運賃調整の方法を示します。

[![運賃調整のタスク](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)

## <a name="automatic-reconciliation"></a>自動調整

自動調整を使用する場合は、調整のスケジュール、および請求書や使用する出荷配送業者を指定する必要があります。 請求明細行と運賃請求書の照合は、監査マスターの設定および運賃請求書タイプに従って行われます。 自動調整の実行後、システムが照合できないすべての請求書を処理する必要があります。 支払に向けすべての請求書を転記する前に、これらの請求書を手動で処理する必要があります。

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a>自動または手動の調整を使用した運賃請求書との運賃請求書の照合

*照合* は、各運賃請求書に対応する運賃請求書を探すプロセスです。 請求書明細行を 1 対 1 で照合するか (手動照合) するか、利用可能なすべての請求書を一度に照合します (自動照合)。

### <a name="auto-matching"></a>自動照合

複数の運賃請求書を同じ運賃請求書に照合する場合は、自動照合のプロセスは次のように機能します。

1. 一致しない運賃請求書はすべて金額で並べ替えされ、最大金額が最初に表示されます。
1. 運賃請求書は、運賃請求書の金額が正の金額が残るまで、1 対 1 で照合されます。
1. 監査マスターの設定と運賃請求書の残額に応じて、残りの金額が設定されます。

### <a name="manual-matching"></a>手動による照合

正の金額を持つすべての運賃請求書を照合できます。 自動照合と同様に、ユーザーは運賃請求書を負の金額と完全に一致しない運賃請求書と照合することができます。

### <a name="example"></a>例

金額が 1500 の運賃請求書 (FB) がある場合に、次の設定に従って各請求書に1つの請求明細を含む 3 件の運賃請求書を作成したとします。

- 元の運賃請求書 (BS) : 金額 1500
- 請求書 1 (Inv1): 金額 1000
- 請求書 2 (Inv2): 金額 600
- 請求書 3 (Inv3): 金額 -100

#### <a name="automatic-matching-result"></a>自動照合結果

自動照合は次の順序で実行されます。

1. すべての運賃請求書を金額で降順に並べ替える: Inv1 -> Inv2 -> Inv3。
1. Inv1 と FB を照合します。 Inv1 の一致金額が 1000、残りの金額が 500 の場合、ステータスは *部分的に一致* に設定されています。
1. Inv2 と FB を照合します。 Inv2 の一致金額が 500、残りの金額が 0 の場合、ステータスは *完全に一致* に設定されています。
1. FB は完全に一致するので、EDV3 は処理されません。

#### <a name="manual-matching-result"></a>手動照合結果

手動照合の場合、次の例に示す順序で結果が異なります。

##### <a name="manual-matching-case-1"></a>手動照合ケース 1

この例で手動照合を行う 1 つの方法は、次のように処理します。

1. Inv1 と FB を照合します。 FB の残金額が 500 ある場合、ステータスは *部分的に一致* に設定されます。
1. Inv2 と FB を照合します。 Inv2 の一致金額が 500、残りの金額が 0 の場合、ステータスは *完全に一致* に設定されています。
1. Inv3 と手動照合を行う場合は、一致しない運賃請求書は見つかりません。

このケースは基本的に自動照合と同じです

##### <a name="manual-matching-case-2"></a>手動照合ケース 2

この例で手動照合を行うもう一つの方法は、次のように処理します。

1. Inv3 と FB を照合します。 これで、残額が 1600 で、1500 を超える金額から負の 100 が差し引かれた金額になります。 FB と Inv3 の両方が -100 と一致します。
1. INv1 と Inv 2 を FB と一つずつ一致させます。 FB は完全に一致します。

この例に示すように、運賃請求書と負の金額の照合は手動でのみ行う必要があります。 これにより、照合順序を制御できるので、運賃請求書を負の金額と完全に照合できない運賃請求書と照合することができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]