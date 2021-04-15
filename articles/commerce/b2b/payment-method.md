---
title: B2B eコマース サイト用の顧客アカウントの支払方法の構成
description: このトピックでは、企業間 (B2B) の eコマースサイトに対して顧客勘定の支払方法を構成する方法について説明します。
author: josaw1
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 62e8f4949dcea1cb201bece171991047ce28da04
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799808"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>B2B eコマース サイト用の顧客アカウントの支払方法の構成

[!include [banner](../../includes/banner.md)]

このトピックでは、企業間 (B2B) の eコマースサイトに対して顧客勘定の支払方法を構成する方法について説明します。

小売業者は、eコマースチャネルで販売する商品やサービスと引き換えに、様々なタイプの支払いを受け入れることができます。 小売業者が受け入れる各支払タイプは、システムの設定時に Microsoft Dynamics 365 Commerce でコンフィギュレーションする必要があります。 B2B e コマース サイトでは、顧客勘定 (または"勘定上") の支払方法がサポートされている必要があります。 

## <a name="prerequisites"></a>必要条件

1. Commerce 本部の顧客勘定の支払い方法を追加します。
2. 顧客勘定の支払方法を eコマースチャネルに関連付けます。
3. Commerce 本部の **小売およびコマース \> 顧客 \> すべての顧客\>支払** で顧客に対して **内金を許可** が有効になっている必要があります。 また、Commerce 本部の **小売りとコマース \> 顧客 \> すべての顧客 \> 与信および回収** で **クレジットの制限** パラメーターが顧客に対して適切に設定されていることを確認してください。 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>Commerce サイトビルダーで顧客勘定の支払い方法を有効にする 

Commerce サイトビルダーで顧客勘定の支払い方法を有効にするには、次の手順に従います。

1. **サイト 設定 \> 拡張機能** に移動します。
1. **顧客勘定支払を有効にする** プロパティを **B2B 顧客に対して有効化する** に設定します。 
1. **保存と公開** を選択します。

> [!NOTE]
> 新しいサイト設定は、app.settings.json ファイルがが更新された後にのみ有効になります。 詳細については、[SDK およびモジュール ライブラリの更新プログラム](../e-commerce-extensibility/sdk-updates.md)を参照してください。

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>B2B e コマース サイトのチェック アウト ページで顧客勘定の支払方法を有効にする

B2B e コマース サイトのチェック アウト ページで顧客勘定の支払方法を有効にするには、次の手順に従います。

1. Commerce サイト ビルダで、B2B 電eコマース サイトのチェックアウト モジュールを含むチェック アウト ページまたはチェックアウト ページの特定部分を編集します。
1. **チェックアウト セクションのコンテナ** スロットで、**モジュールの追加** を選択 し、**顧客勘定の支払** モジュールを追加します。
1. 省略記号 (**...**) を選択して、必要に応じて **上へ移動** または **下へ移動** を選択して、**顧客アカウントの支払い** モジュールを配置します。
1. **保存** を選択し、 **編集の完了** を選択してページにチェックインし、**発行** を選択して公開します。

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>顧客勘定の支払い方法が有効化されており、公開されていることを確認する

顧客勘定の支払い方法が有効化されており、公開されていることを確認するには、次の手順に従います。

1. eコマース サイトにサインインします。
1. 買い物カゴに製品を追加します。
1. チェックアウトのページに移動します。 新しい **顧客勘定** の支払方法が表示されます。

## <a name="additional-resources"></a>追加リソース

[B2B eコマース サイトの設定](set-up-b2b-site.md)

[B2B 組織の組織モデリング階層の作成](org-model.md)

[B2B eコマース サイトでのビジネス パートナー ユーザーの管理](manage-b2b-users.md)

[B2B eコマース サイトの製品数量制限の設定](quantity-limits.md)

[SDK およびモジュール ライブラリの更新](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]