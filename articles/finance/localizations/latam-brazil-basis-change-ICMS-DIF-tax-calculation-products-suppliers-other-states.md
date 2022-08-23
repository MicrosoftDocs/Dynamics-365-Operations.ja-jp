---
title: 他の州の仕入先からの製品に対する ICMS-DIF 税計算の基準の変更
description: この記事では、財務文書が Rio Grande do Sul (RS) or São Paulo (SP) のブラジルの州で受信された時の、ICMS-DIF 税タイプの計算について説明します。
author: Kai-Cloud
ms.date: 06/21/2022
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
ms.openlocfilehash: 1bd9982a3804778a27203b4311682ee8bc3c4841
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218652"
---
# <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-from-suppliers-in-other-states"></a>他の州の仕入先からの製品に対する ICMS-DIF 税算定の基準の変更 (デュアル ベース)

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
    - **基準金額** フィールドで、**行ごとの正味金額** を選択します。
    - 会計年度値が **3** の課税コードである場合に、その課税コードを定義します。 この方法で、**会計帳簿** モジュールを有効にすると、調整トランザクションが自動的に作成されます。
    - 売上税グループの構成で 、**ICMS-DIF** 売上税コードに対して **利用税** オプションを選択します。

### <a name="use-the-delta-tax-rate-in-the-configuration-of-dual-base-icms-dif-sales-tax-codes"></a>デュアル ベースの ICMS-DIF 消費税コードでデルタ税率を使用します

前に説明した設定を使用すると、**ICMS-DIF** 消費税コードがデュアル ベース ルールで計算されます。 ただし、表面税率は 18% になり、シンプルなベース ルールの 6% の税率とは異なります。 この差異によって、会計ドキュメントと税務報告で不整合の問題が発生します。 Microsoft Dynamics 365 Finance のバージョン 10.0.29 では、**機能管理** にある **(ブラジル) デュアル ベース ケースの ICMS-DIF 税コードでデルタ税率を構成する** 機能を有効にして、不整合を解決することができます。

- 前のセクションのステップの他に、**消費税の消費税** フィールドで **ICMS 12** 消費税コードを選択します。
- **ICMS-DIF** 消費税コードの税率を 18% に設定します。 **割合/金額** フィールドには、表面税率が 6% と表示されます。

> [!NOTE]
> **ICMS-DIF** と **ICMS 12** 消費税コードは、同じ消費税グループに割り当てる必要があります。

## <a name="basis-change-dual-base-in-icms-dif-tax-calculations-for-products-to-non-taxpayer-consumers-difal-in-other-states"></a>他州の非納税消費者 (DIFAL) への製品に対する ICMS-DIF 税算定の基準の変更 (デュアル ベース)

**機能管理** で **(ブラジル) 販売トランザクションの ICMS-DIFAL のデュアル ベース算定** 機能を有効にして、他州からの非納税者向け取引に関する ICMS-DIF の基準変更をサポートします。 サンプルの ICMS-DIF 消費税コードは、販売注文トランザクションと自由形式請求書トランザクションで有効になります。

**機能管理** で **(ブラジル) 機能の IPI ケースの ICMS-DIFAL で使用するデュアル ベース算定** 機能を有効にして、別の州からの非納税消費者との取引が、IPI (Imposto sobre Prodsims Industrializados) の責任を負うシナリオをサポートします。 IPI 消費税コードの税額が認識され、ICMS-DIFAL 税基準に適用されます。

- 販売注文または自由形式の請求書のヘッダーで、**会計情報** FastTab の **最終ユーザー** オプションを **はい** に設定する必要があります。
- 発注書または仕入先請求書のヘッダーで、**会計情報** FastTab の **使用と消費** オプションを **はい** に設定する必要があります。
