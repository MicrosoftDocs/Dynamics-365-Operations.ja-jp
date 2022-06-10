---
title: 売買契約は、却下された RFQ から作成できる
description: 売買契約は、却下された RFQ から作成できます。 RFQ 明細行が受理されていない場合でも、システムは売買契約仕訳帳の作成を妨げない
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 92731f0f56e6eba05043403c121939accbe26c05
ms.sourcegitcommit: 220101d2511a3164572226294ef090a43a1e6cdd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/23/2022
ms.locfileid: "8789243"
---
# <a name="trade-agreements-can-be-created-from-rejected-rfqs"></a>売買契約は、却下された RFQ から作成できる

## <a name="symptoms"></a>現象

売買契約は、却下された RFQ から作成できます。 したがって、RFQ 明細行が受理されていない場合でも、システムは売買契約仕訳帳の作成を妨げません。

## <a name="resolution"></a>解決策

これは予想される動作です。 承認されたかまたは却下されたかに関係なく、見積依頼 (RFQ) に対するすべての返信は、売買契約を作成できます。 詳細については、[見積依頼 (RFQ) の概要](/dynamics365/supply-chain/procurement/request-quotations) を参照してください。
