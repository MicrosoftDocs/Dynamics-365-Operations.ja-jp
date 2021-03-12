---
title: 集荷情報モジュール
description: このトピックでは、集荷情報モジュールと、Microsoft Dynamics 365 Commerce のチェックアウト ページにそれを追加する方法について説明します。
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d04e2650f9c601d008ebf19080059b70416d7917
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000612"
---
# <a name="pickup-information-module"></a>集荷情報モジュール

[!include [banner](includes/banner.md)]

このトピックでは、集荷情報モジュールと、Microsoft Dynamics 365 Commerce のチェックアウト ページにそれを追加する方法について説明します。

集荷情報モジュールをチェックアウト モジュールで使用して、注文集荷情報を表示することができます。 顧客は、使用可能な集荷日時を表示したり、注文を集荷するための適切な時間を選択したりできます。 たとえば、顧客は 3 月 21 日の午後 3 時にサンフランシスコの店舗から注文を受け取ることを選択できます。

Commerce 本社では、適切な店舗の集荷時間帯がコンフィギュレーションされている必要があります。 詳細については、[顧客集荷の時間スロットの作成と更新](dev-itpro/pickup-timeslots.md)を参照してください。

集荷情報モジュールがチェックアウト ページに作成されていても、集荷用に選択されている店舗に対して時間帯が定義されていない場合は、モジュールに情報が表示されますが、ユーザーは時間帯時間帯を選択できません。 時間帯は省略可能であり、注文する必要はありません。

複数の店舗で集荷するために複数の品目が選択されている場合は、集荷モジュールを使用して、時間帯を使用できる場合に、ユーザーが各店舗の時間帯を選択できます。

> [!NOTE]
> 時間帯とチェックアウト集荷情報モジュールのサポートは、Dynamics 365 Commerce バージョン 10.0.15 以降で利用できます。

次の図は、チェックアウト ページの集荷情報モジュールを使用した時間帯の選択例を示しています。

![チェックアウト ページの集荷情報モジュールの例](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **見出し** – モジュールの見出しを入力します。

## <a name="show-time-slot-information-after-an-order-is-placed"></a>発注後に時間帯情報を表示する

注文が行われると、選択した時間帯に関する情報が [注文確認モジュール](order-confirmation-module.md)と[注文明細モジュール](account-management.md#order-details-page)に表示されます。 この 2 つのモジュールには、**時間帯情報の表示** プロパティがあります。 注文プロセス中に選択した時間帯を表示できるようにするには、このプロパティを **True** に設定する必要があります。

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a>チェックアウト集荷情報モジュールをページに追加する

集荷情報モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md)を参照してください。

次の図は、集配明細行品目の時間帯を含む電子商取引のチェックアウト ページの例を示しています。

![集配明細行品目の時間帯を含む電子商取引のチェックアウト ページの例](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a>追加リソース

[顧客集荷の時間スロットの作成と更新](dev-itpro/pickup-timeslots.md)

[チェックアウト モジュール](add-checkout-module.md)

[注文確認モジュール](order-confirmation-module.md)

[注文詳細のモジュール](account-management.md)
