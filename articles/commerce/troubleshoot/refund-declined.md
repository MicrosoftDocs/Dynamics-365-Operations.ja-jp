---
title: 返品注文の払戻が拒否される
description: この記事には、請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なるため、返品注文の払戻が拒否された場合に役立つトラブルシューティング ガイドが含まれます。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: d8d1c40673d4b159a7b7bf00bf6011ba45f47edd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268235"
---
# <a name="refund-on-a-return-order-is-declined"></a>返品注文の払戻が拒否される

[!include [banner](../../includes/banner.md)]

この記事には、請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なるため、返品注文の払戻が拒否された場合に役立つトラブルシューティング ガイドが含まれます。

## <a name="description"></a>説明

返品注文の請求に使用されるクレジット カードが、元の支払認証時に使用されたカードと異なる場合、払戻は拒否されます。 次のエラーメッセージが表示されます。「一部の支払が転記に対して正しいステータスではありません。 請求する前に、すべての支払のステータスを再検証してください。」

支払承認の詳細には、次のエラー メッセージが含まれます。「Adyen gateway SendRequest() failed with status 'InternalServerError'.22144; Empty response returned from Adyen.(22001);」

![返品注文のエラーで払戻が拒否される。](media/refund-order-decline.jpg)

## <a name="resolution"></a>解決策

### <a name="enable-blind-returns-in-adyen"></a>Adyen のブラインド返品の有効化

ブラインド返品を有効にするには、[Adyen 向け Dynamics 365 Payment Connector の問題のトラブルシューティング](adyen-support.md) の手順に従って、Adyen サポート チームに連絡し、Adyen のマーチャント口座でブラインド返品を有効にするように要求します。

## <a name="additional-resources"></a>追加リソース

[Adyen 向け Dynamics 365 Payment Connector](../dev-itpro/adyen-connector.md)

[Dynamics 365 の Adyen 支払コネクタを設定](https://docs.adyen.com/plugins/microsoft-dynamics)
