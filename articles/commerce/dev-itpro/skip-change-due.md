---
title: POS の「お釣りの支払い」ダイアログ ボックスをスキップする
description: この記事では、トランザクションが完全に支払われていてお釣りが必要ない場合に、販売時点管理 (POS) で「お釣りの支払い」ダイアログ ボックスをスキップする方法について説明します。
author: BrianShook
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: brshoo
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 202019f701a3fc6d7b16416246450d593dac9a9a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864907"
---
# <a name="skip-change-due-dialog-box-in-pos"></a>POS の「お釣りの支払い」ダイアログ ボックスをスキップする

[!include [banner](../includes/banner.md)]

この記事では、トランザクションが完全に支払われていてお釣りを支払う必要がない場合に、販売時点管理 (POS) で **お釣りの支払い** ダイアログ ボックスをスキップする方法について説明します。

POS での支払いでは、クレジットの使用率が高まっているため、ほとんどのトランザクションで顧客にお釣りを支払う必要がなくなっています。 Dynamics 365 Commerce では、実際に顧客に対してお釣りを支払う必要がない限り、**お釣りの支払い** ダイアログをスキップするように POS を構成できます。 **お釣りの支払い** ダイアログ ボックスは、ギフト レシートのレシート形式が、**必要時** に印刷するように構成されている場合にも表示されます。 ギフト レシートが **必要時** に印刷するように構成されている場合 は、ギフト レシートを印刷するためのオプションが **お釣りの支払い** ダイアログ ボックスに含まれ、**お釣りの支払いをスキップ** の構成が上書きされます。

## <a name="configure-property-to-skip-change-due-dialog-box"></a>プロパティを構成して **お釣りの支払い** ダイアログ ボックスをスキップする

**お釣りの支払い** ダイアログ ボックスをスキップするように構成するプロパティは、店舗レベルの設定の **機能プロファイル** レベルにあります。 

プロパティを構成するには、次の手順に従います。

1. ダイアログ ボックスをスキップする店舗の **機能プロファイル** を検索します。
1. 目的の店舗の機能プロファイルを開き、**編集** を選択します。 
1. **機能** クイック タブを展開します。 **端末** 小見出しの下の、**お釣りの支払い** フィールドで、**ゼロのときにスキップ** を選択します。 
1. **保存** を選択してから、**1070** チャネル構成配布スケジュールを実行します。
1. 変更が同期されたら、POS からサインアウトし、再度サインインします。 **お釣りの支払い** ダイアログ ボックスが表示されないことを確認するために、顧客にお釣りを支払う必要のないトランザクションを作成します。  

## <a name="additional-resources"></a>追加リソース

[支払方法](../payment-methods.md)

[クレジット カードの設定、認証、および取得](../../finance/accounts-receivable/credit-card-authorizations.md)

[販売時点管理 (POS) 用の現金貨幣単位のコンフィギュレーション](../cash-denominations.md)

[クレジット カード処理のコンフィギュレーション](../tasks/configure-credit-card-processing.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]