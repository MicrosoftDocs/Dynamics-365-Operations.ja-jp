---
title: POS の製品推奨事項
description: このトピックでは、POS (販売時点管理) デバイスでの製品推奨事項の使用について説明します。
author: bebeale
manager: AnnBe
ms.date: 10/01/19
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 98c84e987c40adf136d0240117f7b0f119bf2f59
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811120"
---
# <a name="product-recommendations-on-pos"></a>POS の製品推奨事項

[!include [banner](includes/banner.md)]

製品の推奨事項は、本質的に、すべての小売スペースにまたがる変形力のあるビジネス アプリケーションであり、リッチで魅力的な、カスタマイズされた製品検索エクスペリエンスを作成します。 POS にこの機能を実装するには、[POS デバイスに推奨事項を追加する方法](add-recommendations-control-pos-screen.md)の手順に従ってください。 

製品推奨機能の詳細については、[製品推奨事項の概要](../commerce/product-recommendations.md)を参照してください。 

## <a name="scenarios"></a>シナリオ

製品推奨事項は、以下の POS シナリオで使用可能です。 これらは、Cloud POS または Modern POS (MPOS) で利用できます。

1. **製品の詳細** ページ:

    - 店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに**製品の詳細** ページを参照する場合、推奨サービスは、一緒に購入される可能性が高い追加アイテムを提案します。

    [![製品詳細ページの推奨事項](./media/proddetails.png)](./media/proddetails.png)

2. **トランザクション** ページ:

    - 推奨エンジンは、一緒に頻繁に購入されるバスケット内の品目の一覧全体に基づいて、品目を提案します。

    > [!NOTE]
    > **トランザクション** ページに推奨事項を表示するには、小売業者は Dynamics 365 for Retail の画面レイアウトを更新する必要があります。 **推奨事項** コントロールは、**トランザクション** ページにドロップする必要があります。

    [![トランザクション ページの推奨事項](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

## <a name="configure-dynamics-365-retail-to-enable-pos-recommendations"></a>Dynamics 365 Retail をコンフィギュレーションして POS 推奨事項を有効化する

製品推奨事項を設定するには、次の手順を実行します。

1. サービスが **10.0.6 ビルド**に更新されていることを確認します。
2. ビジネスで[製品推奨事項を有効化する](../commerce/enable-product-recommendations.md)の指示に従ってください。
3. オプション: トランザクション画面に推奨事項を表示するには、**画面レイアウト** に移動して画面レイアウトを選択し、**画面レイアウト デザイナー** を起動し、必要に応じて **レコメンデーション** コントロールを削除します。
4. **小売パラメーター** に移動し、**機械学習** を選択し、**POS 推奨事項の有効化** で **はい** を選択します。
5. POS に関する推奨事項を表示するには、グローバル構成ジョブ **1110** を実行します。 POS 画面レイアウト設計者の変更を反映するには、チャネル構成ジョブ **1070** を実行します。



## <a name="troubleshoot-issues-where-you-have-product-recommendations-already-enabled"></a>[製品推奨事項] が既に有効な場合の問題のトラブルシューティング

- **小売パラメーター** \> **推奨事項リスト** \> **製品推奨事項の無効化**に移動し、**グローバル構成ジョブ \[9999\]** を実行します。 
- **画面レイアウト デザイナー** を使用して **推奨事項コントロール** をトランザクション画面に追加した場合、それも削除してください。
- 他にご質問がある場合は、[製品推奨事項に関するよく寄せられる質問](../commerce/faq-recommendations.md) を参照してください。

## <a name="additional-resources"></a>追加リソース

[POS デバイスのトランザクション画面への推奨事項コントロールの追加](add-recommendations-control-pos-screen.md)

[製品推奨事項の概要](../commerce/product-recommendations.md)

[製品推奨事項の有効化](../commerce/enable-product-recommendations.md) 
