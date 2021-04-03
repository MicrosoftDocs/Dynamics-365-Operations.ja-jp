---
title: 次回の支払のために保存するオプションが表示されない
description: このトピックでは、e コマース サイトのチェックアウト ページで次回の支払のために保存するチェック ボックスが e コマース サイトのチェックアウト ページの支払方法で表示されない場合に役立つトラブルシューティング ガイドを示します。
author: Reza-Assadi
manager: AnnBe
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
ms.openlocfilehash: 3a4fbcd522651ed1b82b72b751ff6ead44c94a71
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585413"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>「次回の支払のために保存する」 オプションが表示されない

[!include [banner](../../includes/banner.md)]

このトピックでは、**次回の支払のために保存する** チェック ボックスが e コマース サイトのチェックアウト ページの **支払方法** の下に表示されない場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

**次回の支払のために保存する** チェックボックスは e コマース サイトのチェックアウト ページの **支払方法** セクションに表示されません。

次の図は、**次回の支払のために保存する** チェック ボックスを含むチェックアウト ページの例を示しています。

![支払いモジュールの次回の支払のために保存するチェック ボックス](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>解像度

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認する

Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認するためには、次の手順を実行します。

1. **Retail と Commerce \>チャネル\>オンライン ストア** に移動します。
1. オンライン ストアを選択します。
1. **支払口座** クイック タブで **e コマースでの支払情報の保存を許可する** フィールドが **True** に設定されていることを確認します。

![Commerce 本部で e コマース フィールドに支払情報の保存を許可する](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>追加リソース

[支払モジュール](../payment-module.md)

[オンライン支払手段を Adyen コネクタで保存](../dev-itpro/adyen-connector-listPI.md)
