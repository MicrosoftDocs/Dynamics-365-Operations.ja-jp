---
title: ギフト カード モジュール
description: このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。
author: anupamar-ms
ms.date: 04/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8db7e597241f1fd552f6b960c2b57b0ba83da949
ms.sourcegitcommit: efde05c758b2e02960760d875569d780d77d5550
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/29/2021
ms.locfileid: "5962766"
---
# <a name="gift-card-module"></a>ギフト カード モジュール

[!include [banner](includes/banner.md)]

このトピックでは、ギフト カード モジュールと、Microsoft Dynamics 365 Commerce のサイト ページにそれを追加する方法について説明します。

ギフト カード モジュールは、精算モジュールで使用することができ、電子商取引で使用される一般的な支払い方法であるギフトカードを受け付けることができます。 ギフト カード モジュールは Dynamics 365、SVS、Givex ギフト カードをサポートしています。 SVS と Givex のギフト カードは、Adyen の支払プロバイダーで経由で引き換えることができます。 SVS や Givex などの外部ギフト カードのサポートの詳細については、[外部ギフト カードのサポート](./dev-itpro/gift-card.md) を参照してください。

> [!NOTE]
> 精算フロー中の SVS および Givex ギフトカードの引き換えは、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能です。 

ギフト カード モジュールは2つ使用できます。

- **ギフト カード** – このモジュールは、精算ページで使用でき、支払/入金としてギフトカードを使用できます。 
- **ギフト カードの残高** – このモジュールは、ギフトカードの残高を確認するために任意のページで使用できます。 このモジュールは、コマースのリリース 10.0.14 およびこれ以降でのみ利用できます。

> [!NOTE]
> ギフトカード残高チェック モジュールのサポートは、Dynamics 365 Commerce の営々ース バージョン 10.0.14 で使用可能です。

以下の図は、精算ページにおけるギフト カード モジュールの例を示しています。

![ギフト カード モジュールの例](./media/ecommerce-giftcard.PNG)

## <a name="module-properties"></a>モジュール プロパティ

- **追加フィールドの表示** – このプロパティでは、常に既定で表示されるギフト カード番号に加えて、ギフト カードを表示するフィールドを定義します。 たとえば、一部のギフト カードでは、個人識別番号 (PIN) の表示をサポートしており、他ののギフト カードでは、PIN と有効期限の表示をサポートしています。 または、このプロパティを "なし" に設定して、ギフト カード番号のみを表示し、追加フィールドは表示しないようにすることもできます。

サポートされている値:
-   暗証番号 (PIN)
-   有効期限
-   PIN と 有効期限 
-   None

## <a name="site-settings-for-gift-card-modules"></a>ギフト カード モジュールのサイト設定

コマース サイト ビルダーの **サイト設定 \> 拡張子** には、**サポートされているギフト カード タイプ** と呼ばれるギフト カード モジュール設定があります。 この設定は 3 つの値をサポートします:
- **Dynamics 365 ギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Dynamics 365 ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。
- **SVS と Givex のギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Givex や SVS ギフト カードの償還しかできなくなります。 この設定は、E コマース サイトのサインイン ユーザーと匿名ユーザーに対してサポートされます。
- **Dynamics 365、SVS、Givex のギフト カード** – この設定が適用されている場合、ギフト カード モジュールは Dynamics 365、Givex、SVS ギフト カードを償還できます。 この設定は、E コマース サイトのサインイン ユーザーに対してのみサポートされます。

> [!IMPORTANT]
> これらの設定は、Dynamics 365 Commerce のリリース バージョン 10.0.11 で使用可能であり 、SVS や Givex のギフトカードに対応する必要がある場合にのみ必要となります。 古いバージョンの Dynamics 365 Commerce を更新する場合は、appsettings.json ファイルを手動で更新する必要があります。 appsettings.json ファイルを更新する手順については、[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file)を参照してください 。 

## <a name="extend-internal-gift-cards-for-use-in-e-commerce-storefronts"></a>電子商取引店舗で使用する内部ギフト カードの拡張

既定では、内部ギフト カードは電子商取引店舗で使用するのに最適化されていません。 したがって、内部ギフト カードを支払に使用できるようにする前に、セキュリティを向上させる拡張機能を使用して構成する必要があります。 内部ギフト カードを運用で使用できるようにする前に拡張する必要があるギフト カード領域を次に示します。

- **ギフト カード番号** – 番号順序は、内部ギフト カードにギフト カード番号を生成するために使用されます。 番号順序は簡単に予測できるので、ギフト カード番号の生成を拡張し、発行されるギフト カード番号に対してランダムで暗号化された安全な文字列を使用する必要があります。
- **GetBalance** – **GetBalance** API はギフト カードの残高を検索するために使用されます。 既定では、この API は公開されています。 ギフト カードの残高を検索するのに PIN が必要でない場合、ブルートフォース攻撃が **GetBalance** API を使用し、残高のあるギフト カード番号を検索しようとするリスクがあります。 内部ギフト カードの PIN 要件と API 調整の両方の実装は、リスクを軽減するのに役立ちます。
- **PIN** – 既定では、内部ギフト カードでは PIN はサポートされていません。 残高の検索に PIN が必要となるようにするために、内部ギフト カードを拡張する必要があります。 この機能を使用して、誤った PIN 入力を連続して試行した後でギフト カードをロックすることもできます。

## <a name="enable-gift-card-payments-for-guest-checkout"></a>ゲスト チェックアウトに対するギフト カードの支払を有効にする

既定では、ゲスト (匿名) のチェックアウトに対してギフト カードの支払は有効になっていません。 有効にするには、次の手順に従います。

1. Commerce 本部で、**Retail と Commerce \> チャネルの設定 \> POS 設定 \> POS \> POS 操作** の順に移動します。
1. グリッドのヘッダーを選択したまま (または右クリック)、**列を挿入** を選択します。
1. **列を挿入** ダイアログ ボックスで、**AllowAnonymousAccess** チェック ボックスを選択します。
1. **更新プログラム** を選択します。
1. 操作 **520** (ギフト カード残高) および **214** の場合、**AllowAnonymousAccess** の値を **1** に設定します。
1. **保存** を選択します。
1. チャネル データベースへ変更を同期するために、**1090** スケジューラ ジョブを実行します。 

## <a name="add-a-gift-card-module-to-a-page"></a>ギフト カード モジュールをページに追加する

ギフト カード モジュールをチェックアウト ページに追加し、必要なプロパティを設定する方法については、[チェックアウト モジュール](add-checkout-module.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[買い物カゴ モジュール](add-cart-module.md)

[買い物カゴ アイコン モジュール](cart-icon-module.md)

[チェックアウト モジュール](add-checkout-module.md)

[支払モジュール](payment-module.md)

[出荷先住所モジュール](ship-address-module.md)

[配送オプション モジュール](delivery-options-module.md)

[集荷情報モジュール](pickup-info-module.md)

[注文詳細のモジュール](order-confirmation-module.md)

[外部ギフト カードのサポート](./dev-itpro/gift-card.md)

[SDK およびモジュール ライブラリの更新](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
