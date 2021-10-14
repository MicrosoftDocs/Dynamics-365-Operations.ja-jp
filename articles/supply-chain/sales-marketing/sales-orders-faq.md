---
title: 販売注文に関するよく寄せられる質問
description: このページでは、Dynamics 365 Supply Chain Management の販売注文の処理時によく寄せられる質問を取り上げます。
author: Henrikan
ms.date: 06/24/2021
ms.topic: troubleshooting
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 3cee75b1d740e7cb414c674157dde0146e8faa50
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7571620"
---
# <a name="sales-order-faqs"></a>販売注文に関するよくある質問

このページでは、Dynamics 365 Supply Chain Management の販売注文の処理時によく寄せられる質問を取り上げます。

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a>需要を満たすために注文書を販売注文にリンクすることはできますか。

販売注文からの発注書を作成することができます。 詳細については、[販売注文から発注書を作成する](/dynamics365/supply-chain/sales-marketing/tasks/create-purchase-order-sales-order) をご覧ください。

## <a name="can-i-cancel-or-delete-a-sales-order-or-return-order"></a>販売注文または返品注文をキャンセルまたは削除できますか?

*作成済* 状態の販売注文および返品注文のみをキャンセルできます。 詳細については、[返品注文のキャンセル](/dynamics365/supply-chain/service-management/cancel-return-order) を参照してください。

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a>削除された請求済販売注文を元に戻すことはできますか ?

請求済の販売注文が誤って削除された場合、復元したり、詳細を確認したりすることができます。

**顧客勘定 \> トランザクション \> 元の文書 \> 詳細の表示** の順に移動します。 目的の請求書を検索し、それを選択して、詳細を表示します。 この詳細には、販売注文の参照が含まれます。 また、このページから販売注文の詳細にアクセスできるようにする必要があります。

## <a name="how-do-i-delete-orphaned-sales-order-records"></a>孤立した販売注文レコードをどのように削除しますか?

孤立した販売注文レコードをクリーンアップするには、次のいずれかの場所に移動して、*販売注文の削除* の定期処理ジョブを実行します。

- 販売とマーケティング \> 定期的なタスク \> クリーンアップ \> 半日注文の削除
- 小売りおよびコマース \>小売業およびコマース IT \> クリーンアップ \> 販売注文の削除

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a>既に転記されている請求書のコミッションを計算する方法はありますか。

Supply Chain Management は、転記された請求書のコミッションの計算は現在サポートしていません。
