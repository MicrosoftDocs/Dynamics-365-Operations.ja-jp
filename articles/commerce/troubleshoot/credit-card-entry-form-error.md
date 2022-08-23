---
title: チェックアウト時に、クレジット カード エントリ ページにエラーが表示される
description: この記事では、支払方法セクションが読み込まれずエラーが表示される場合に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: 25f0dde83efff7c1d9a2a456270f5d48047f44ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269758"
---
# <a name="credit-card-entry-page-shows-an-error-at-checkout"></a>チェックアウト時に、クレジット カード エントリ ページにエラーが表示される

[!include [banner](../../includes/banner.md)]

この記事では、**支払方法** セクションが読み込まれずエラーが表示される場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

オンライン ストアのチェックアウト ページを開く際、**支払方法** セクションが読み込まれず、次のエラー メッセージが表示されます: 「問題が発生しました。 後でもう一度お試しください。」

![支払モジュール エラー。](media/payment-module-error.jpg)

## <a name="resolution"></a>解決策

### <a name="wait-for-the-commerce-scale-unit-cache-to-expire"></a>Commerce Scale Unit キャッシュの有効期限が切れるのを待つ

オンライン ストアのチェックアウト ページの支払サービス設定は、Commerce Scale Unit にキャッシュされ、e コマース サイトに表示されるまでに、最大 15 分かかる場合があります。 これらの支払サービス設定には、マーチャント口座 ID、クラウド API キー、および支払方法に関連するさまざまなコンフィギュレーション設定の変更が含まれます。

## <a name="additional-resources"></a>追加リソース

[オンライン チャネルの設定](../channel-setup-online.md)
