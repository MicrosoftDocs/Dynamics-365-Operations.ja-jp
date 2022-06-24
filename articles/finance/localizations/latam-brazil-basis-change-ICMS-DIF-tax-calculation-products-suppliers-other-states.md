---
title: 他の州の仕入先からの製品に対する ICMS-DIF 税計算の基準の変更
description: この記事では、財務文書が Rio Grande do Sul (RS) or São Paulo (SP) のブラジルの州で受信された時の、ICMS-DIF 税タイプの計算について説明します。
author: Kai-Cloud
ms.date: 1/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-1-17
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 1fde18c79f375db4db6bc52cdb5c40a61625ae63
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868265"
---
# <a name="basis-change-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>他の州の仕入先からの製品に対する ICMS-DIF 税計算の基準の変更

この記事では、財務文書が Rio Grande do Sul (RS) or São Paulo (SP) のブラジルの州で受信された時の、**ICMS-DIF** 税タイプの計算について説明します。

州法の定義に従って、収集される Imposto sobre Circulação de Mercadorias e Serviços (ICMS) は、次の規則に従う必要があります。

*収集する ICMS* = ([(*運用額* – *ソースからの ICMS*) ÷ (1 – *内部 ICMS %*)] × *内部 ICMS %*) – *ソースからの ICMS 額*

## <a name="example"></a>例

RS 州内の修正プログラムの会社は、SP 州の仕入先から購買の会計ドキュメントを受け取ります。 この会社は、RS 州 (18%) と SP 州 (12%) との間の ICMS の割合の差を収集する必要があります。 ただし、基準は前のルールに従って計算する必要があります。

- **運用額:** 1,000.00 ブラジル レアル (R$ 1,000.00)
- **ICMS 州間取引:** R$ 120.00
- **RS 州の ICMS %:** 18%
- **RS 州で回収する ICMS:**  (\[(1,000 – 120) ÷ (1 – 0.18)\] × 0.18 ) – 120 = R$ 73.17 

## <a name="resolution"></a>解決策

RS 州のルールに従って差分 ICMS (ICMS-DIF) を計算するには、次の方法で売上税コードと売上税グループを設定する必要があります。

1. 12% の ICMS を受け取る (他の州の場合) 売上税コードを作成します。 このコードは、仕入先からの税収入金額を登録するために使用されます。
2. ICMS-DIF を収集する売上税コードを作成します。 この売上税コードは、18% と12% の差を定義するために、パーセント金額が18% (自分の州の場合) である必要があります。 税タイプを **ICMS-DIF** に設定します。 この売上税コードは、計算パラメータで次の方法で定義する必要があります。

    - **発生元** フィールドで、**総額のパーセンテージ** を選択します。
    - **基準金額** フィールドで、行ごとの **正味金額** または **請求書残高の正味金額** を選択します。
    - 会計年度値が **3** の課税コードである場合に、その課税コードを定義します。 この方法で、**会計帳簿** モジュールを有効にすると、調整トランザクションが自動的に作成されます。
    - 売上税グループの構成で 、**ICMS-DIF** 売上税コードに対して **利用税** オプションを選択します。
