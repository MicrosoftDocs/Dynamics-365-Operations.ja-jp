---
title: 既定の支払サービスに関連する注文の同期エラー
description: この記事では、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: aa57366fb8f351a8275c947220de78fe809b7b5a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9276692"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>既定の支払サービスに関連する注文の同期エラー

[!include [banner](../../includes/banner.md)]

この記事では、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

オンライン注文を同期すると、次のエラー メッセージが表示されます。「クレジット カード トランザクションを処理するには既定の支払サービスが必要です。」

![既定の支払サービス エラーの欠落。](media/default-payment-method-error.jpg)

## <a name="resolution"></a>解決策

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce 本社で既定の支払サービスを確認または設定する

Commerce 本社で既定の支払サービスを確認または設定するには、次の手順に従います。

1. **売掛金勘定 \> 支払設定 \> 支払サービス** の順に移動します。
1. 1 つの支払サービスに対して、**新しいクレジット カードの既定のプロセッサ** オプションが **はい** に設定されていることを確認してください。

## <a name="additional-resources"></a>追加リソース

[クレジット カードの設定、認証、および取得](../../finance/accounts-receivable/credit-card-authorizations.md)
