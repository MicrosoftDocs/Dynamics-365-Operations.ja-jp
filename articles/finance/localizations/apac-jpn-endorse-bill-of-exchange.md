---
title: 日本での受取手形の裏書による仕入先への支払
description: このトピックには、日本で仕入先に支払うための受取手形 (BOE) の裏書に関する情報が含まれています。
author: yijialuan
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustBillOfExchangeEndorseListPage, CustBillOfExchangeEndorseToVendor
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 28791
ms.search.region: Japan
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3b58c7f09ba4ed6cc5869fa691c02b8a0b55d56
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772884"
---
# <a name="pay-a-vendor-by-endorsing-a-bill-of-exchange-for-japan"></a>日本での受取手形の裏書による仕入先への支払

[!include [banner](../includes/banner.md)]

日本では、多くの場合、為替手形 (BOE) は仕入先に裏書きされ、支払方法として使用されます。 BOEs のリスト ページでは、BOE のライフ サイクルの集中管理を提供します。

BOE の管理を開始するには、為替手形振出仕訳帳を開きます。 このタイプの仕訳帳を転記すると、BOE ステータスが**振出**の場合、次のステージの BOE のライフ サイクルを管理できます。

## <a name="endorsea-boe-to-a-vendor"></a>仕入先に対する BOE の裏書
リスト ページには、振り出された顧客の BOE が表示されます。 一つ以上の仕入先に裏書きする BOE を選択できます。 ただし、複数の BOE がオンの場合、それらに裏書きする前に、**振出**ステータスがすべてに必要です。 会計伝票は裏書きした BOE の勘定と買掛金勘定の残高の変更を記録するために生成されます。

## <a name="settle-vendor-transactions"></a>仕入先トランザクションの決済
BOE が裏書きされると **裏書済**ステータスに変更されます。 買掛金勘定のユーザーが仕入先請求書に対して、仕入先トランザクションを決済できます。 仕入先トランザクションの決済時に BOE 自体のステータスは変更されません。

## <a name="settle-endorsed-boes"></a>裏書済 BOE の決済
BOE のライフ サイクルは、BOE が支払われる、または期限切れになった時点で終了します。 裏書きした BOE の場合、BOE を選択し、裏書を決済できます。 会計伝票は裏書きした BOE の勘定と振出済 BOE の勘定の残高の変更を記録するために生成されます。

## <a name="reserve-endorsement"></a>裏書の引当
BOE の状態が**裏書済**の場合、裏書引当を行うことができます。

## <a name="additional-resources"></a>その他のリソース
- [顧客の受取手形の裏書による仕入先トランザクションの支払](./tasks/pay-vendor-transaction.md)
- [裏書済受取手形の取消](./tasks/reverse-endorsed-bill-exchange.md)
- [顧客の為替手形の裏書きによって日本の支払を設定します](./tasks/setup-japan-payment-endorsing-customer-bill-exchange.md)
- [裏書済受取手形の決済](./tasks/settle-endorsed-bill-exchange.md)

