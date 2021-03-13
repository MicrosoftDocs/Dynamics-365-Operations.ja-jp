---
title: サービス注文を自動で作成します
description: サービス契約が有効期間にあるサービス契約に基づいてサービス注文を生成できます。
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 53369ef2b7ff93ae4f0523accbc31cc88575a383
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010675"
---
# <a name="automatically-create-service-orders"></a>サービス注文を自動で作成します 

[!include [banner](../includes/banner.md)]


サービス契約が有効期間にあるサービス契約に基づいてサービス注文を生成できます。

サービス契約から生成したサービス注文は、すべてそのサービス契約に関連付けられます。

サービス注文は、以下の設定から自動的に生成されます。

  - サービス契約明細行で設定されたサービス契約期間。 サービス契約期間は、サービス注文明細行が作成される頻度を示します。 詳細については、[サービス期間](service-intervals.md) を参照してください。

  - サービス期間の定義として **サービス注文の作成** フォームの **開始日** および **終了日** フィールドで指定した期間。 詳細については、[サービス注文の自動作成](create-service-orders-automatically.md) を参照してください。

  - サービス合意ヘッダーの **サービス注文の組み合わせ** オプション。 このオプションは、サービス契約から生成されたサービス注文明細行が、従業員、サービス タスク、サービス対象、またはサービス契約に応じて、サービス注文を連結するかを定義します。 詳細については、[サービス注文の組み合わせ](combine-service-orders.md) を参照してください。

  - サービス合意項目の **時間枠** オプション。 時間枠では、計算日に関連してサービス注文明細行が移動できる範囲を定義します。 詳細については、[時間枠](time-windows.md) を参照してください。


> [!NOTE]
> <P>サービス注文に指定された日が<STRONG>サービス管理パラメーター</STRONG>フォームで選択したカレンダーでオープンでない場合、カレンダーに不一致があることをメッセージが示します。 このメッセージは無視できます。カレンダー上でその日が終了していてもサービス注文は作成されます。</P>

## <a name="example-1"></a>例 1

サービス合意の期間は 2012 年 1 月 1 日～ 2012 年 12 月 31 日です。 **サービス注文の作成** フォームで指定するサービス期間が 2012 年 11 月 1日～ 2013 年 2 月 1 日の場合、サービス注文が 2012 年 11 月 1 日～ 2012年 12 月 31 日で作成されます。

## <a name="example-2"></a>例 2

サービス合意の期間は 2012 年 1 月 1 日～ 2012 年 12 月 31 日です。 このサービス合意に 2 つのサービス合意項目が関連付けられています。 最初のサービス合意項目は、開始日が 2012 年 1 月 2 日で、終了日が 2012 年 3 月 1 日です。 2 つ目のサービス合意項目は、開始日が 2012 年 4 月 1 日で、終了日が 2012 年 12 月 31 日です。 **サービス注文の作成** フオームで指定する期間は、2012 年 10 月 1 日～ 2012年 12 月 31 日です。 この場合、最初の合意項目の開始日と終了日が、サービス注文に指定した期間よりも前の日付であるため、サービス注文は 2 番目の合意項目に対してのみ生成されます。

  


