---
title: "輸送管理での運賃の調整"
description: "この項目では、運賃調整プロセスについて説明します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSInvoiceTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 722c52c22a98317dd67887f50fc95f3e3764ed83
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="reconcile-freight-in-transportation-management"></a>輸送管理での運賃の調整

[!include[banner](../includes/banner.md)]


この項目では、運賃調整プロセスについて説明します。

運賃の調整は手動で行うか、あるいは自動的に実行するよう設定することができます。 運賃の自動調整を使用する場合は、どの運賃請求書が自動的に照合されるかを決定する基準を定義する監査マスターを設定する必要があります。

## <a name="the-freight-reconciliation-process"></a>運賃調整プロセス
運賃は、関連する出荷配送業者に関連付けられているレート エンジンによって計算されます。 積荷が確認されると、運賃請求書が生成され、そこに運賃が転送されます。 運賃は通常の請求プロセスに使用される設定に応じて、関連する元伝票 (発注書、販売注文、または移動オーダー) に雑費として配賦されます。 運賃調整プロセス (照合プロセスとも呼ばれます) は、出荷配送業者から運賃請求書が到着次第開始できます。 請求書は電子ファイルで、または紙面で受領することができます。 紙の請求書を受領した場合は、運賃請求書をテンプレートとして使用して電子請求書を生成できます。 

[![運賃調整プロセス](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)

## <a name="manual-reconciliation"></a>手動調整
運賃を手動で調整する場合は、請求書の各明細行を、運賃請求書の明細行または請求対象となっている積荷の明細行と照合する必要があります。 この照合は [**運賃請求書と請求書の照合**] ページで行います。 請求明細行の金額が運賃請求書の金額と一致しない場合は、差額を調整する理由を選択する必要があります。 調整する理由が複数ある場合は、一致しない金額をそれら全体に分割できます。 調整の理由によって、差額の総勘定元帳への転記方法が決定されます。 請求書の全額の調整が明確にされると、承認のため送信され、仕訳帳が転記されます。 次の図は、Microsoft Dynamics 365 for Finance and Operations での運賃請求書の生成および運賃調整の方法を示しています。 
[![Dynamics AX での運賃調整タスク](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)
## <a name="automatic-reconciliation"></a>自動調整
自動調整を使用する場合は、調整のスケジュール、および請求書や使用する出荷配送業者を指定する必要があります。 請求明細行と運賃請求書の照合は、監査マスターの設定および運賃請求書タイプに従って行われます。 自動調整の実行後、システムが照合できないすべての請求書を処理する必要があります。 支払に向けすべての請求書を転記する前に、これらの請求書を手動で処理する必要があります。




