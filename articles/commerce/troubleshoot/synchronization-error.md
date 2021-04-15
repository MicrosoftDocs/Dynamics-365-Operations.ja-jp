---
title: 既定の支払サービスに関連する注文の同期エラー
description: このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801438"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>既定の支払サービスに関連する注文の同期エラー

[!include [banner](../../includes/banner.md)]

このトピックでは、オンライン注文の同期時に発生する可能性があるエラーの修正に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

オンライン注文を同期すると、次のエラー メッセージが表示されます。「クレジット カード トランザクションを処理するには既定の支払サービスが必要です。」

![既定の支払サービス エラーの欠落](media/default-payment-method-error.jpg)

## <a name="resolution"></a>解像度

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce 本社で既定の支払サービスを確認または設定する

Commerce 本社で既定の支払サービスを確認または設定するには、次の手順に従います。

1. **売掛金勘定 \> 支払設定 \> 支払サービス** の順に移動します。
1. 1 つの支払サービスに対して、**新しいクレジット カードの既定のプロセッサ** オプションが **はい** に設定されていることを確認してください。

## <a name="additional-resources"></a>追加リソース

[クレジット カードの設定、認証、および取得](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
