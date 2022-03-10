---
title: サブスクリプション ワークフローの概要
description: このトピックでは、サブスクリプション ワークフローの概要を示します。
author: kamaybac
ms.date: 05/07/2018
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup, SMASubscriptionCreateDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd1484563e9650b9ddae543e3440eec2a3ed075c
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2022
ms.locfileid: "7983048"
---
# <a name="subscription-workflow-overview"></a>サブスクリプション ワークフローの概要 

[!include [banner](../includes/banner.md)]


自分が照明法人のサブスクリプション管理者で、法人が照明装置メンテナンスのサブスクリプションを提供しているとします。 また、顧客が会社に連絡して照明装置メンテナンスの年間サブスクリプションを購入するとします。

## <a name="setting-up-subscriptions"></a>サブスクリプションの設定

サブスクリプションを設定するには、まず新しいサービス合意のサブスクリプション グループを作成するか、サブスクリプション グループが存在することを確認する必要があります。 サブスクリプション グループが存在する場合は、1 年を通して顧客に請求を行い、販売収益を毎月見越計上するようにサブスクリプション グループを設定する必要があります。 サブスクリプションの設定方法の詳細については、「[サブスクリプション グループの設定](set-up-subscription-groups.md)」を参照してください。

サブスクリプション グループを作成したら、サブスクリプションを作成できるようになります。 サービス サブスクリプションを作成する方法の詳細については、[サブスクリプション グループからのサービス サブスクリプションの作成](create-service-subscriptions-from-subscription-group.md)を参照してください。

## <a name="create-and-modify-subscription-transactions"></a>サブスクリプション トランザクションの作成および変更

サブスクリプションを設定したら、最初の請求期間 (1 年間) のサブスクリプション手数料トランザクションを作成します。 トランザクションのタイプは **通常** です。 したがって、作成できるサブスクリプション トランザクションは、**期間タイプ** フォームで事前に作成した期間に対応する開始日と終了日を持つトランザクションに限られます。 手数料トランザクションの詳細については、[サブスクリプション手数料トランザクションの作成](create-subscription-fee-transactions.md)を参照してください。

顧客に対してサブスクリプションを設定したら、すべての表示価格から 10 パーセント値引きしてサービスを提供するという交渉が成立したことを考慮します。 したがって、作成したトランザクション手数料の価格を下方修正する必要があります。

その日のうちに顧客から電話があり、照明装置のサービス合意を求めてはいるものの、年内に新しい照明装置を導入する予定との連絡を受けました。 したがって、必要なメンテナンス対象期間は 2013 年 10 月までのみであることがわかりました。 顧客のサブスクリプションの月数を下方修正するには、タイプが **下方修正日数** である新しいサブスクリプション手数料トランザクションを作成します。 日数を下方修正する方法の詳細については、[サブスクリプション手数料の日数の引き下げ](reduce-the-days-on-subscription-fees.md)を参照してください。

## <a name="invoice-and-accrue-subscription-transactions"></a>サブスクリプション トランザクションの請求および見越計上

サブスクリプションの設定が完了し、顧客に対してサブスクリプションの請求を行う準備が整いました。 サブスクリプションの請求方法の詳細については、「[サブスクリプション トランザクションの請求](invoice-subscription-transactions.md)」を参照してください。

2 日後に顧客から電話があり、サブスクリプションをユーロではなく米ドルで請求するように依頼されました。 このため、訂正票に加えて、正しい通貨で新しいサブスクリプション トランザクションを作成します。 サブスクリプション トランザクションの貸方への記入方法の詳細については、「[サブスクリプション トランザクションの貸方記入](credit-subscription-transactions.md)」を参照してください。

毎月月末に、顧客のサブスクリプションからの 1 か月分の収益を損益勘定および仕掛品勘定に見越計上します。 サブスクリプションの収益を見越計上方法の詳細については、[未収のサブスクリプション収益](accrue-subscription-revenue.md)を参照してください。

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]