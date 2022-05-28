---
title: 会社間取引の設定
description: このトピックでは、会社間取引を設定する方法について説明します
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: CustTable, VendTable, EcoResProductListPage, InterCompanyTradingRelationSetupCustomer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 5080267568f4d0626d2c727efb533295e7d8e397
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8669407"
---
# <a name="set-up-intercompany-trade"></a>会社間取引の設定

[!include [banner](../../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management で会社間取引を実行できるようにするには、顧客と仕入先を会社間取引を実行するように設定する必要があります。 また、買掛金勘定、売掛金勘定、調達、販売、販売とマーケティングも設定する必要があります。

## <a name="before-you-set-up-intercompany-trade"></a>会社間取引を設定する前に

会社間取引を設定する前に、どの顧客が会社間顧客で、どの仕入先が会社間仕入先であるかを決める必要があります。 Microsoft Dynamics 365 Supply Chain Management の法人ごとに、特定の会社間顧客または仕入先との会社間取引関係に適用する取引ポリシーを決める必要があります。

特に、ユーザーとその組織は、会社間パラメーターをよく理解することをお勧めします。

- 各法人で会社間取引を担当するマネージャーと設定の影響について話し合う。
- 各法人に適切な値を設定する。

## <a name="set-up-trading-relations"></a>取引関係の設定

顧客と仕入先の会社間取引を設定する手順は、次のとおりです。

1. **売掛金勘定 \> 顧客 \> すべての顧客** の順に移動します。
1. 顧客 ID を選択します。
1. アクション ペインの **全般** タブで **会社間** を選択します。
1. 顧客アカウントの会社間設定パラメーターを指定します。 これらのパラメーターには、対応する仕入先と仕入先アカウントを含む法人が含まれます。 パラメーターには、発注書ポリシー、販売注文ポリシー、値のマッピング、販売契約と購買契約のポリシーも含まれます。 さらに、他の法人で顧客アカウントまたは仕入先アカウントのどちらの基準データ値を使用するかも指定します。
1. 法人の残りの会社間顧客について、手順 1 から 4 を繰り返します。
1. **買掛金勘定 \> 仕入先 \> すべての仕入先** に移動します。
1. 仕入先アカウントを選択します。
1. アクション ペインの **全般** タブで **会社間** を選択します。
1. 仕入先アカウントの会社間設定パラメーターを指定します。 これらのパラメーターには、対応する顧客と顧客アカウントを含む法人が含まれます。 このパラメーターには、販売注文ポリシー、発注書ポリシー、値のマッピング、購買契約と販売契約のポリシーも含まれます。 さらに、他の法人で仕入先アカウントまたは顧客アカウントのどちらの基準データ値を使用するかも指定します。
1. 法人の残りの会社間仕入先について、手順 6 から 9 を繰り返します。

## <a name="set-up-products"></a>製品の設定

顧客と仕入先の会社間取引を設定する手順は、次のとおりです。

1. **製品情報管理 \> 製品 \> すべての製品と製品マスター** の順に移動します。
1. 会社間取引を行う法人にリリースされる製品を定義します。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
