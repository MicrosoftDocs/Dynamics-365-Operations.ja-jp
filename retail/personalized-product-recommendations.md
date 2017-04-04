---
title: Personalized product recommendations overview
description: "Dynamics 365 for Operationsでは、(POS)のPOSデバイスの製品の推奨事項を表示できます。 ベスト プラクティスは別の顧客はオンラインと実店舗で購入した顧客が、品目欲しい基づく品目のリストに必要な発注の履歴、品目にかもしがあります。品目です。 大規模カタログの小売業者に対して、ベスト プラクティスは、製品の検出の顧客ができます。 顧客の対象に、購買既に対象となる製品の展示して製品の推奨事項を販売の小売業者のグループ化および関連品目を販売する顧客の管理を高めることができます。 Dynamics 365 for Operationsでは、製品の推奨事項が認識サービスおよびMicrosoftのAzureの機械学習によって動力が割り当てられます。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: af1f4ba1ed5efe0e35d08d37d09e7ada4a4c1b7a
ms.lasthandoff: 03/31/2017


---

# <a name="personalized-product-recommendations-overview"></a>Personalized product recommendations overview

Dynamics 365 for Operationsでは、(POS)のPOSデバイスの製品の推奨事項を表示できます。 ベスト プラクティスは別の顧客はオンラインと実店舗で購入した顧客が、品目欲しい基づく品目のリストに必要な発注の履歴、品目にかもしがあります。品目です。 大規模カタログの小売業者に対して、ベスト プラクティスは、製品の検出の顧客ができます。 顧客の対象に、購買既に対象となる製品の展示して製品の推奨事項を販売の小売業者のグループ化および関連品目を販売する顧客の管理を高めることができます。 Dynamics 365 for Operationsでは、製品の推奨事項が認識サービスおよびMicrosoftのAzureの機械学習によって動力が割り当てられます。

<a name="scenarios"></a>シナリオ
---------

次のPOSのシナリオの製品の推奨事項が有効になります。 これはクラウドPOSの現代 (MPOS) を使用できます。

1.  **製品の詳細**ページ:

-   店舗の関連が退**製品の詳細**を参照する場合、チャンネルに前のトランザクションを表示、ベスト プラクティス エンジンが低いまとめて購入するために追加の品目を表示するときのページ。
-   店舗の関連のトランザクションに顧客を追加し、それぞれ**製品の詳細**ページを参照する場合、ベスト プラクティス エンジンは、顧客のトランザクション履歴を使用して、カスタマイズされた報酬認定を提供します。

[![のproddetails] (。/media/proddetails.png) ] (。/media/proddetails.png) 

1.  **トランザクション: **ページ

-   ベスト プラクティス エンジンは、全体の品目の一覧に基づいて品目が表示されます。
-   店舗の関連のトランザクションに顧客を追加すると、ベスト プラクティス エンジンは、の顧客のトランザクション履歴と品目の一覧を使用して個人のベスト プラクティスを提供します。

**メモ**のベスト プラクティスを表示する**トランザクション**ページ、小売業者Dynamics 365 for Operationsの画面レイアウトを更新する必要があります。 **ベスト プラクティス**制御が**トランザクション**ページになる必要があります。 [![] transactionscreenmultipleproductslargemessengersbag-5 (。/media/transactionscreenmultipleproductslargemessengersbag-5.jpg) ] (。/media/transactionscreenmultipleproductslargemessengersbag-5.jpg) 

1.  **顧客詳細**ページ:
    -   ベスト プラクティス エンジンは、ユーザーidに基づいて品目および顧客の欲しいWeight品目のリストが表示されます。

[![のcustomerdetailsrecommendations] (。/media/customerdetailsrecommendations.png) ] (。/media/customerdetailsrecommendations.png) 

## <a name="configure-dynamics-365-for-operations-to-enable-pos-recommendations"></a>POSのベスト プラクティスを有効にする場合は、Dynamics 365 for Operationsを設定します。
製品の推奨事項を設定するには、次を実行する必要があります。

1.  正しいの選択したことを確認してください**法人**。
2.  移動の**エンティティの店舗**、**小売販売**選択し、[]をクリックします。**更新**。** **これは、上のデータベースのデモ データ (またはデータ) を使用して、エンティティの店舗に移動します。
3.  オプション: トランザクションの画面のベスト プラクティスを表示するには、レイアウト**画面、**選択し、画面レイアウトを起動し、**画面レイアウト デザイナー**、** ** [落とします**ベスト プラクティス制御**、必要な実行します。
4.  **パラメータをRetailする**、[**機械説明します** **、[はい**)。** POSのベスト プラクティスを有効にします。**。
5.  POSのベスト プラクティスを表示するには、実行グローバル組織ジョブ** 1110 **。 変更を反映すると、POS画面レイアウト デザイナーに、実行するチャンネルの構成ジョブ1070を**行われた**。

## <a name="how-does-it-work"></a>こののしくみを[] () または。
**エンティティの店舗**エンティティを更新すると、次のアクションはとられます。

-   認識サービスに必要な工程の運用、データベースのDynamics 365からフォームのデータは得られ、エンティティの店舗に送信されます。
-   Azureデータ ファクトリ(ADF)からデータをADFの活動の一部としてハイブのスクリプトを使用してデータを清潔にするのに使用されます。 清潔にされるデータにブロブの保管に保存されます。
-   API認識サービスによってブロブの記憶域のデータが推奨事項モデルを実施するのに使用されます。

**有効なベスト プラクティス**付けたり、コンフィギュレーション ジョブを実行すると、次のアクションはとられます。

-   モデル資格情報とIDはAPIから取得され、工程の運用、データベース365 for Operations、AOSのweb.config、およびRetailサーバーに保存されます。
-   オンライン モードのMPOSおよびクラウドPOSの製品の推奨事項についての通話が受取済を付けることができるようにモデル資格情報とIDはCRTに使用可能になります。


<a name="see-also"></a>参照
--------

[POSのデバイス追加します。] (追加推奨事項制御pos screen.md) トランザクションのページに報酬認定を制御します。


