---
title: 電子商取引のデジタル ギフト カード
description: Microsoft Dynamics 365 Commerce の電子商取引の実装におけるデジタルギフトカードの機能について説明します。 重要な構成の手順の概要についても説明しています。
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5a88bef72e13b7b0d948bfd7617cb1dbbcd9ce49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982669"
---
# <a name="e-commerce-digital-gift-cards"></a>電子商取引のデジタル ギフト カード

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Microsoft Dynamics 365 Commerce の電子商取引の実装におけるデジタルギフトカードの機能について説明します。 重要な構成の手順の概要についても説明しています。

Dynamics 365 Commerce では、デジタル ギフト カードの購入は、システ内のその他製品の購入と同じフローです。 追加のモジュールを構成する必要はありません。 複数のギフト カードをカートに追加した場合、そのギフト カード品目は1つの販売行には集計されません。 この動作は、各販売の明細行が個別のギフト カード番号を使用して請求を行うため必要となります。

デジタル ギフト カードの購入は Dynamics 365 Commerce 10.0.16 以降でサポートされます。

次の図は、Fabrikam の電子商取引サイトのデジタル ギフト カードの製品詳細ページ (PDP) の例を示しています。

![Fabrikam 電子商取引サイトのデジタル ギフト カード PDP の例](./media/GiftcardPDP.PNG)

## <a name="turn-on-the-digital-gift-card-feature-in-commerce-headquarters"></a>Commerce 本部のデジタル ギフト カード機能を有効にする

デジタル ギフト カードの購入フローを Dynamics 365 Commerce で実行するには、Commerce 本部で **電子商取引機能の購買ギフト カード** 機能を有効にする必要があります。 Commerce 本部の **機能管理** ワークスペースには、以下の図のような特徴があります。

![Commerce 本部の機能管理ワークスペース](./media/Featureflag.PNG)

## <a name="configure-a-digital-gift-card-in-commerce-headquarters"></a>Commerce 本部のデジタル ギフト カードを構成する

デジタル ギフトカード製品は Commerce 本部で構成する必要があります。 このプロセスは、他の製品のプロセスと共通しています。 ただし、次の重要な手順は、購買用ギフト カードの構成に固有のものです。 製品の作成および構成方法の詳細については、[Commerce で新製品を作成する](create-new-product-commerce.md) を参照してください。

- **新しい製品** ダイアログ ボックスでデジタル ギフト カード製品を構成する場合は、**製品タイプ** フィールドを **サービス** に設定します。 (ダイアログ ボックスを開くには、 **小売およびコマース \> 製品とカテゴリ \> カテゴリ別製品** に移動し、**新規** を選択します。) **サービス** タイプの商品は、注文を行う前に利用可能な在庫が確認されません。 詳細については、[新しい製品の作成](create-new-product-commerce.md#create-a-new-product) を参照してください。
- **コマース パラメーター** ページの **転記** タブで、次の図に示すように、**ギフト カード製品** フィールドを **デジタル ギフト カード** に設定する必要があります。 商品が外部ギフトカードの場合は、[外部ギフト カードへの対応](./dev-itpro/gift-card.md)を参照してください。

    ![Commerce 本部のギフト カード製品フィールド](./media/PostGiftcard.png)

- ギフト カードで、定義済の複数の金額 ($25、$50、$100 など) に対応する必要がある場合は、**サイズ** 分析コードを使用して、定義済金額を設定する必要があります。 定義済の各金額はバリアント型です。 詳細については、[製品分析コード](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)を参照してください。
- 顧客がギフト カードのカスタム金額を指定できるようにする必要がある場合は、最初にカスタム金額を許可するバリアントを設定します。 次に、**カテゴリ内のリリース済み製品** ページで製品を開き、 **Commerce** クイックタブで、**価格のキー** フィールドを、次の図に示すように **新しい価格内の必須キー** に設定します。 この設定により、顧客が PDP で製品を参照する際に価格を入力できます。

    ![Commerce 本部の価格フィールドのキー](./media/KeyInPrice.png)

- デジタル ギフト カードの配信モードを **電子** に設定する 必要があります。 **配送方法** ページ (**小売およびコマース  \> チャネルの設定 \> 配送方法**) で、一覧ペインで配送方法に **電子** を選択し、 次の図に示すように、**製品** クイックタブでグリッドにデジタル ギフト カード製品を追加します。 詳細については、[配送方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery) を参照してください。

    ![Commerce 本部の配信モードページのデジタル ギフトカード商品](./media/ElectronicMode.PNG)

- オンライン機能プロファイルが作成され、Commerce 本部のオンライン ストアに関連付けられている必要があります。 機能プロファイルで、**製品の集計** オプションを **はい** に設定します。 この設定により、ギフト カードを除くすべての品目が集計されます。 詳細については、[オンライン機能プロファイルの作成](online-functionality-profile.md)を参照してください。
- ギフト カードの請求後に顧客にメールが届くようにするには、**電子メール通知プロファイル** ページに新しいメール通知タイプを作成し、**電子メール通知タイプ** フィールドを **ギフト カードの発行** に設定します。 詳細については、[電子メールの通知プロファイルの設定](email-notification-profiles.md) を参照してください。

## <a name="add-product-images-to-the-commerce-site-builder-media-library"></a>Commerce サイト ビルダー メディア ライブラリに製品画像を追加する

デジタル ギフト カード製品の製品イメージを Commerce サイト ビルダのメディア ライブラリに追加する必要があります。 ギフト カード イメージ ファイルのファイル名が、製品イメージのサイトの命名規則に従っている必要があります。 詳細については、[画像のアップロード](dam-upload-images.md)を参照してください。

## <a name="configure-a-custom-amount-for-a-digital-gift-card-in-commerce-site-builder"></a>Commerce サイト ビルダでデジタル ギフト カードのカスタム金額を構成する

デジタル ギフト カードがカスタム金額を許容するように構成されている場合は、この動作は、サイトの PDP で使用される [購入ボックス モジュール](add-buy-box.md) でも有効にする必要があります。 購入ボックス モジュールは、カスタム金額を許可するモジュールの構成に対応しています。 また、カスタム金額に対して許可される最小額と最大金額を定義できます。

Commerce サイト ビルダでデジタル ギフト カードのカスタム金額を構成します。

1. サイトの PDP で使用されている [購入ボックス モジュール] に移動します。 この購入ボックス モジュールは、フラグメント、テンプレート、またはページで実装されている場合があります。
1. **編集** を選択します。
1. 右側のプロパティ ウィンドウで、**カスタム価格を許可する** チェック ボックスをオンにします。
1. オプション : カスタム金額の最小金額と最大金額を定義するには、**最大価格** と **最小価格** に金額を入力します。
1. **編集の終了** を選択し、**公開** を選択します。

## <a name="additional-resources"></a>追加リソース

[購入ボックス モジュール](add-buy-box.md)

[チェックアウト モジュール](add-checkout-module.md)

[カート モジュール](add-cart-module.md)

[Commerce での新しい製品の作成](create-new-product-commerce.md)

[荷渡方法の設定](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[製品分析コード](https://docs.microsoft.com/dynamics365/supply-chain/pim/product-dimensions?toc=/dynamics365/retail/toc.json)

[電子メール通知プロファイルの設定](email-notification-profiles.md)

[オンライン機能プロファイルの作成](online-functionality-profile.md)

[外部ギフト カードのサポート](./dev-itpro/gift-card.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]