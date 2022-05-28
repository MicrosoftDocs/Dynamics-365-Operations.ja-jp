---
title: 会社間顧客請求書の支払を自動的に登録する
description: このトピックでは、会社間顧客請求書の支払を自動的に登録する方法について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: dbd06b21d736d1e247cd087e5bb86fbe641352e6
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669435"
---
# <a name="register-payments-automatically-for-intercompany-customer-invoices"></a>会社間顧客請求書の支払を自動的に登録する

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management では、会社間顧客請求書が転記された時点で、顧客トランザクションが作成されます。 この顧客トランザクションは決済されるまで、つまり支払済になるまで未処理の状態です。 対応する会社間発注書が請求書更新されると、顧客トランザクションと一致する仕入先トランザクションが作成されます。 この仕入先トランザクションも決済されるまで未処理の状態です。 差異のリスクを減らすために、買掛金勘定支払仕訳帳の転記時に、売掛金勘定支払仕訳帳を自動的に作成して転記できます。

1. **販売とマーケティング \> 顧客 \> すべての顧客** に移動します。
1. アクション ペインの **全般** タブで **会社間** を選択します。
1. 販売注文の **会社間** ページで会社間売掛金勘定支払を設定するには 、**販売注文ポリシー** リンクを選択します。
1. **支払仕訳帳** フィールドで、会社間仕入先支払を登録する売掛金勘定支払仕訳帳を選択します。 これは **売掛金勘定パラメーター** ページで設定します。
1. この仕訳帳に自動的に転記する場合は、**仕訳帳の自動転記** チェック ボックスを選択します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
