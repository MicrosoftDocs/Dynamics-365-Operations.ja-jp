---
title: "為替手形の裏書による仕入先への支払"
description: "日本では、多くの場合、為替手形 (BOEs) は仕入先に裏書きされ、支払方法として使用されます。 Microsoft Dynamics 365 for Operations の BOE のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。"
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28791
ms.assetid: f0ed3209-2d1a-4208-ba45-192e88baed53
ms.search.region: Japan
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 173d6c5760c876e04f7cbad74cd5a30fceea22c5
ms.contentlocale: ja-jp
ms.lasthandoff: 04/25/2017


---

# <a name="pay-a-vendor-by-endorsing-a-bill-of-exchange"></a>為替手形の裏書による仕入先への支払

[!include[banner](../includes/banner.md)]


日本では、多くの場合、為替手形 (BOEs) は仕入先に裏書きされ、支払方法として使用されます。 Microsoft Dynamics 365 for Operations の BOE のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。

Dynamics 365 for Operations の BOE の管理を開始するには、受取手形振出仕訳帳を開きます。 このタイプの仕訳帳を転記すると、BOE ステータスが**振出**の場合、次のステージの BOE のライフ サイクルを管理できます。

## <a name="endorse-a-boe-to-a-vendor"></a>仕入先に対する BOE の裏書
リスト ページには、振り出された顧客の BOE が表示されます。 一つ以上の仕入先に裏書きする BOE を選択できます。 ただし、複数の BOE がオンの場合、それらに裏書きする前に、**振出**ステータスがすべてに必要です。 会計伝票は裏書きした BOE の勘定と買掛金勘定の残高の変更を記録するために生成されます。

## <a name="settle-vendor-transactions"></a>仕入先トランザクションの決済
BOE が裏書きされると **裏書済**ステータスに変更されます。 買掛金勘定のユーザーが仕入先請求書に対して、仕入先トランザクションを決済できます。 仕入先トランザクションの決済時に BOE 自体のステータスは変更されません。

## <a name="settle-endorsed-boes"></a>裏書済 BOE の決済
BOE のライフ サイクルは、BOE が支払われる、または期限切れになった時点で終了します。 裏書きした BOE の場合、BOE を選択し、裏書を決済できます。 会計伝票は裏書きした BOE の勘定と振出済 BOE の勘定の残高の変更を記録するために生成されます。

## <a name="reserve-endorsement"></a>裏書の引当
BOE の状態が**裏書済**の場合、裏書引当を行うことができます。




