---
title: 停止された販売注文明細行の梱包明細を転記できない
description: 停止された販売注文明細行の梱包明細を転記できない
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462853"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>停止された販売注文明細行の梱包明細を転記できない

エラーコード: SYS13203

## <a name="symptoms"></a>現象

積荷のために梱包明細を生成しようとすると、次のエラー メッセージが表示されます:

> 出荷 A の数量を取得できないことを確認した後で販売注文明細を停止すると、梱包明細を転記できません。

## <a name="cause"></a>原因

関連する販売注文明細行が 1 つ以上停止されている場合、その販売注文はそれ以上処理されません。 特にこの場合、システムは注文の梱包明細を転記しません。

たとえば、顧客から電話がかかってきて注文をキャンセルされたため、注文明細行を 1 行以上停止するようユーザーが決定した場合などです。 ただし、出荷の出荷が既に確認済である場合は、販売注文を含む出荷は物理的に倉庫から出庫します。つまり、販売注文明細行の停止は影響を受け取しません。 出荷を物理的に停止することは不可能になったので、梱包明細を転記できるよう明細行を解除することもできます。 その後、キャンセルされた注文を返品として処理する必要があります。

## <a name="resolution"></a>解決策

梱包明細を転記するには、次の手順に従って関連する販売注文明細行がいずれも停止しない必要があります。

1. **すべての販売注文 \> 販売とマーケティング \>すべての販売注文** の順に移動します。
1. 問題が発生している販売注文を見つけて開きます。
1. **販売注文明細行** クイック タブで、販売注文の明細行を選択します。
1. **行の詳細** クイック タブで、**一般** タブを開き、**停止** フィールドが *いいえ* に設定された状態を確認します。
1. 関連するすべての販売明細行が停止されなくなるまで作業を続行します。
1. 再度、積荷または販売注文の梱包明細を転記してください。
