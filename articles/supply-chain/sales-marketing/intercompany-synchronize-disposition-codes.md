---
title: 廃棄コードの同期
description: このトピックでは、会社間商取引の廃棄コードの同期について説明します
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 04a25324e79a1f9cb30a7da19d648bda995ba7b2
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548371"
---
# <a name="synchronize-intercompany-disposition-codes"></a>会社間廃棄コードの同期

[!include [banner](../../includes/banner.md)]

会社間返品をサポートするため、Microsoft Dynamics 365 Supply Chain Management では、外部定義の廃棄コードを対応する内部廃棄コードにマップすることができます。 会社間グループが設定されている場合、相互にマップされる 2 社の処分アクションが同じである必要があります。 異なる場合、同期プロセスは失敗します。

## <a name="about-disposition-codes-for-three-legged-direct-returns"></a>3 社間の直接返品の廃棄コードについて

廃棄コードは、会社間販売注文書明細行から元の販売注文明細行に同期されます。 ただし、同期が元の販売注文明細行に与える直接的な影響は 1 つだけです。 この影響とは、雑費明細行が、会社 A で設定されている廃棄コードと雑費に基づいて削除されることです。会社 A は返品注文を作成する会社です。

3 社間直納グループでは、すべての処分アクションが会社間販売注文明細行でサポートされます。 ただし、製品を顧客に返品する場合は、元の注文で指定されている顧客の配送先住所と返品注文の配送先住所が一致していることを確認する必要があります。

> [!NOTE]
> 発注書の廃棄コードはありません。 したがって、会社間販売注文書から元の返品注文への廃棄コードの同期は、販売注文から販売注文へ実行する必要があります。

## <a name="replacing-returned-items"></a>返品品目の交換

返品品目を交換する場合、会社 B で交換注文が既に作成されていると、廃棄コードは選択できず、会社 A で追加の交換注文が作成されません。

## <a name="rules-for-intercompany-direct-deliveries"></a>会社間直納のルール

会社間直納に関係するシナリオでは、次の一般ルールが元の返品注文に適用されます:

- 元の販売注文明細行に対する処分アクションが、貸方と仕損、貸方、顧客に返品のいずれかである場合、貸方の処分アクションが適用されます。 ただし、顧客に返品のアクション コードは、既存の明細行と会社間販売注文から新たに同期された明細行で、正味金額を 0 (ゼロ) に設定します。 また、仕損明細行は同期されません。 会社間販売注文書に明細行を追加しても、正の数量と仕損の処分アクション (貸方と仕損や置換と仕損など) の販売注文には同期されません。
- 貸方と置換または仕損と置換の基になる処分アクションは、取り消されません。 貸方と置換または仕損と置換の処分アクションとして処理されます。 このルールは、会社 A で仕損明細行が作成されず、会社 B (返品品目を受け取った会社) で交換注文が作成されない場合でも適用されます。 交換注文は、梱包明細の更新が実行された場合にのみ会社 A で作成されます。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
