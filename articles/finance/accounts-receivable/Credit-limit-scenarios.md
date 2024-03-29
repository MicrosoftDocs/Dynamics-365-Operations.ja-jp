---
title: 与信限度額のシナリオ
description: この記事では、顧客が顧客与信限度額グループに属している場合に、顧客の与信限度額を確認する方法について説明します。
author: JodiChristiansen
ms.date: 06/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-06-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 60b17a6b7f57b468610974ae9bd05b7db3584cc1
ms.sourcegitcommit: 85141b21ac90f3db1b378c21f9c7f3d8f74e182f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/09/2022
ms.locfileid: "9130258"
---
# <a name="credit-limit-scenarios"></a>与信限度額のシナリオ

与信管理では、顧客レベルで顧客に与信限度額を割り当てることができます。 各顧客を *顧客与信限度額グループ* に割り当てることができ、各グループには与信限度額が割り当てられます。 そのため、与信管理では、グループ レベルでも顧客に与信限度額を割り当てることができます。 同じ顧客与信グループに割り当てられているすべての顧客の与信限度額は同じです。

一般に、グループの与信限度額は個々の与信限度額の前にチェックされます。 個々の与信限度額がグループの与信限度額を上書きするとは限りません。

この記事では、顧客与信グループと個々の与信限度額に関連する 5 つのシナリオについて説明します。

## <a name="the-customer-group-credit-limit-is-more-than-the-individual-credit-limit"></a>顧客グループの与信限度額は個々の与信限度額よりも多くなる

たとえば、顧客の個々の与信限度額は $10,000 になります。 顧客が顧客与信グループに割り当てられた場合、そのグループの与信限度額は $15,000 になります。 この場合、顧客の「有効な与信限度額」は $10,000 になります。これは、この金額がグループ限度額よりも少ないためです。 ブロック ルールでは、最初にグループの限度を確認します。 その後、個々の限度が確認されます。 $10,000 を超える販売注文はブロックされます。

## <a name="the-individual-credit-limit-is-more-than-the-customer-group-credit-limit"></a>個別の与信限度額は顧客のグループ与信限度額よりも多くなる

たとえば、顧客の個々の与信限度額は $20,000 になります。 顧客が顧客与信グループに割り当てられた場合、そのグループの与信限度額は $15,000 になります。 この場合、ブロック ルールは常時グループの限度額を最初に確認するので、顧客の有効な与信限度額は $15,000 になります。 $15,000 を超える販売注文はブロックされます。

## <a name="the-individual-credit-limit-is-set-to-000-and-mandatory-credit-limit-is-set-to-yes"></a>個別の与信限度額が 0.00 に設定され、与信限度確認必須が有効に設定される

顧客の個別の与信限度額が **0.00** で、**与信限度確認必須** オプションが **はい** に設定されている場合、顧客が顧客与信グループに割り当てられている場合でも、顧客の有効与信限度額は $0.00 になります。 このようにして、顧客をグループに追加できますが、すべての注文は与信管理に移動します。

## <a name="the-individual-credit-limit-is-set-to-000-and-unlimited-credit-limit-is-set-to-yes"></a>個々の与信限度額が 0.00 に設定され、無制限の与信限度額が有効に設定される

顧客の個々の与信限度額が **0.00** で、**無制限の与信限度額** オプションが **はい** に設定されている場合、顧客が顧客与信グループに割り当てられている場合でも、顧客の与信は無制限になります。

## <a name="the-individual-credit-limit-is-set-to-000-and-the-customer-is-part-of-a-customer-credit-group"></a>顧客が顧客与信グループに割り当てられた場合、個々の与信限度額は $0.00 になる

たとえば、顧客の与信限度額は **0.00** に設定され、**無制限の与信限度額** オプションは **いいえ** に、**与信限度確認必須** オプションは **いいえ** に設定されます。 顧客が顧客与信グループに割り当てられた場合、そのグループの与信限度額は $15,000 になります。 この場合、顧客の有効与信限度額はグループの与信限度額 $15,000 になります。 したがって、この金額を超える販売注文はブロックされます。 この動作により、与信限度額は有効化され、個々の顧客レベルではなく顧客与信グループ レベルで管理されます。 同じグループに割り当てられているすべての顧客の与信限度額は同じです。
