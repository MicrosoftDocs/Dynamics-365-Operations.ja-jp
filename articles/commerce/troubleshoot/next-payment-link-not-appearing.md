---
title: 次回の支払のために保存するオプションが表示されない
description: この記事では、eコマース サイトのチェックアウト ページで次回の支払のために保存するチェック ボックスが eコマース サイトのチェックアウト ページの支払方法で表示されない場合に役立つトラブルシューティング ガイドを示します。
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
ms.openlocfilehash: d0b398a4ffc5fb698ea04ba8642d05ccd4caf04c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287487"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>「次回の支払のために保存する」 オプションが表示されない

[!include [banner](../../includes/banner.md)]

この記事では、**次回の支払のために保存する** チェック ボックスが eコマース サイトのチェックアウト ページの **支払方法** の下に表示されない場合に役立つトラブルシューティング ガイドを示します。

## <a name="description"></a>説明

**次回の支払のために保存する** チェックボックスは eコマース サイトのチェックアウト ページの **支払方法** セクションに表示されません。

次の図は、**次回の支払のために保存する** チェック ボックスを含むチェックアウト ページの例を示しています。

![支払いモジュールの次回の支払のために保存するチェック ボックス。](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>解決策

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認する

Commerce 本社で Ayden 向け Dynamics 365 Payment Connector が正しく構成されていることを確認するためには、次の手順を実行します。

1. **Retail と Commerce \>チャネル\>オンライン ストア** に移動します。
1. オンライン ストアを選択します。
1. **支払口座** クイック タブで **e コマースでの支払情報の保存を許可する** フィールドが **True** に設定されていることを確認します。

![Commerce 本部で e コマース フィールドに支払情報の保存を許可する。](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>追加リソース

[支払モジュール](../payment-module.md)

[オンライン支払手段を Adyen コネクタで保存](../dev-itpro/adyen-connector-listPI.md)
