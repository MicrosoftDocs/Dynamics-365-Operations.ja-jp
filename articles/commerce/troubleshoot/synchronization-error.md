---
title: 既定の支払サービスに関連する注文の同期エラー
description: このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715239"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>既定の支払サービスに関連する注文の同期エラー

[!include [banner](../../includes/banner.md)]

このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。

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