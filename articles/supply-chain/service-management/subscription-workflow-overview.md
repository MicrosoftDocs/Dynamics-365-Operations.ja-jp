---
title: 定期売買ワークフローの概要
description: このトピックでは、定期売買ワークフローの概要を示します。
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f023ddd8d6f9350702f687763b53b057baa9aed8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431915"
---
# <a name="subscription-workflow-overview"></a>定期売買ワークフローの概要 

[!include [banner](../includes/banner.md)]


自分が照明法人の定期売買管理者で、法人が照明装置メンテナンスの定期売買を提供しているとします。 また、顧客が会社に連絡して照明装置メンテナンスの年間定期売買を購入するとします。

## <a name="setting-up-subscriptions"></a>定期売買の設定

定期売買を設定するには、まず新しいサービス合意の定期売買グループを作成するか、定期売買グループが存在することを確認する必要があります。 定期売買グループが存在する場合は、1 年を通して顧客に請求を行い、販売収益を毎月見越計上するように定期売買グループを設定する必要があります。 定期売買の設定方法の詳細については、「[定期売買グループの設定](set-up-subscription-groups.md)」を参照してください。

定期売買グループを作成したら、定期売買を作成できるようになります。 サービスの定期売買を作成する方法の詳細については、[定期売買グループからのサービスの定期売買の作成](create-service-subscriptions-from-subscription-group.md)を参照してください。

## <a name="create-and-modify-subscription-transactions"></a>定期売買トランザクションの作成および変更

定期売買を設定したら、最初の請求期間 (1 年間) の定期売買手数料トランザクションを作成します。 トランザクションのタイプは **通常** です。 したがって、作成できる定期売買トランザクションは、**期間タイプ** フォームで事前に作成した期間に対応する開始日と終了日を持つトランザクションに限られます。 手数料トランザクションの詳細については、[定期売買手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。

顧客に対して定期売買を設定したら、すべての表示価格から 10 パーセント値引きしてサービスを提供するという交渉が成立したことを考慮します。 したがって、作成したトランザクション手数料の価格を下方修正する必要があります。

その日のうちに顧客から電話があり、照明装置のサービス合意を求めてはいるものの、年内に新しい照明装置を導入する予定との連絡を受けました。 したがって、必要なメンテナンス対象期間は 2013 年 10 月までのみであることがわかりました。 顧客の定期売買の月数を下方修正するには、タイプが **下方修正日数** である新しい定期売買手数料トランザクションを作成します。 日数を下方修正する方法の詳細については、[定期売買手数料の日数の引き下げ](reduce-the-days-on-subscription-fees.md)を参照してください。

## <a name="invoice-and-accrue-subscription-transactions"></a>定期売買トランザクションの請求および見越計上

定期売買の設定が完了し、顧客に対して定期売買の請求を行う準備が整いました。 定期売買の請求方法の詳細については、「[定期売買トランザクションの請求](invoice-subscription-transactions.md)」を参照してください。

2 日後に顧客から電話があり、定期売買をユーロではなく米ドルで請求するように依頼されました。 このため、訂正票に加えて、正しい通貨で新しい定期売買トランザクションを作成します。 定期売買トランザクションの貸方への記入方法の詳細については、「[定期売買トランザクションの貸方記入](credit-subscription-transactions.md)」を参照してください。

毎月月末に、顧客の定期売買からの 1 か月分の収益を損益勘定および仕掛品勘定に見越計上します。 定期売買の収益を見越計上方法の詳細については、[未収の定期売買収益](accrue-subscription-revenue.md)を参照してください。

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]