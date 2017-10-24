---
title: "カスタマイズされた製品の推奨事項の概要"
description: "Dynamics 365 for Retail では、POS (営業拠点) デバイスに製品の推奨事項を表示することができます。 推奨事項は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目のことです。 大規模カタログの小売業者には、製品の発見に役立つ推奨事項があります。 製品の推奨事項は、顧客の関心と購買習慣を対象とした製品を展示することで、アップセルおよびクロスセルを行う小売業者を支援し、顧客維持を強化することができます。 Dynamics 365 for Retail では、認知サービスと Microsoft Azure 機械学習によって、小売りと製品の推奨が強化されます。"
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a>カスタマイズされた製品の推奨事項の概要

[!include[banner](includes/banner.md)]


> [!NOTE]
> この機能は、現在サンドボックスおよび生産 (高可用性) 配置トポロジにのみ使用できます。 

Dynamics 365 for Retail では、POS (営業拠点) デバイスに製品の推奨事項を表示することができます。 推奨事項は、顧客の購買履歴、欲しい物のリストの品目、他の顧客がオンラインや従来型の店舗で購入した品目に基づいた興味を持ちそうな品目のことです。 大規模カタログの小売業者には、製品の発見に役立つ推奨事項があります。 製品の推奨事項は、顧客の関心と購買習慣を対象とした製品を展示することで、アップセルおよびクロスセルを行う小売業者を支援し、顧客維持を強化することができます。 Dynamics 365 for Retail では、認知サービスと Microsoft Azure 機械学習によって、小売りと製品の推奨が強化されます。


<a name="scenarios"></a>シナリオ
---------

製品推奨事項は、以下の POS シナリオで使用可能です。 これらは、Cloud POS または Modern POS (MPOS) で利用できます。

1.  [**製品の詳細**] ページ:

-   店舗スタッフが、異なるチャネル間で以前のトランザクションを調べるときに、[**製品の詳細**] ページを参照する場合、推薦エンジンは、一緒に購入される可能性が高い追加アイテムを提案します。
-   店舗スタッフが顧客をトランザクションに追加し、[**製品の詳細**] を参照する場合、推奨エンジンは、顧客の取引履歴を使用してパーソナライズされた推奨事項を提供します。

[![proddetails](./media/proddetails.png)](./media/proddetails.png)

2.  [**トランザクション**] ページ:

-   推薦エンジンは、バスケット内のアイテムの全リストに基づいて品目を提案します。
-   店舗スタッフが顧客をトランザクションに追加する場合、推奨エンジンは、顧客のトランザクション履歴とバスケット内の品目のリストを使用して個人的な推奨を提供します。

> [!NOTE]
> [**トランザクション**] ページに推奨事項を表示するには、小売業者は Dynamics 365 for Retail の画面レイアウトを更新する必要があります。 [**推奨事項**] コントロールは、[**トランザクション**] ページにドロップする必要があります。 [![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)

3.  [**顧客の詳細**] ページ:
    -   推薦エンジンは、ユーザ ID および顧客の希望リストの品目に基づいて、品目を提案します。

[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a>Dynamics 365 for Retail を構成して POS 推奨事項を有効にします。
製品の推奨事項を設定するには、次の設定を行う必要があります。

1.  正しい [**法人**] を選択したことを確認してください。
2.  [**エンティティ ストア**] にナビゲートし、[**小売販売**] を選択して、[**更新**] をクリックします。これにより、運用データベースのデモ データ (またはデータ) が使用され、エンティティ ストアに転送します。
3.  オプション: トランザクション画面に推奨事項を表示するには、[**画面レイアウト**] に移動して画面レイアウトを選択し、[**画面レイアウト デザイナー**] を起動し、必要に応じて [**レコメンデーション**] コントロールを削除します。
4.  [**小売パラメーター**] に移動し、[**機械学習**] を選択し、[**POS 推奨事項の有効化**] で [**はい**] を選択します。
5.  POS に関する推奨事項を表示するには、グローバル構成ジョブ [**1110**] を実行します。 POS 画面レイアウト設計者の変更を反映するには、チャネル構成ジョブ [**1070**] を実行します。

## <a name="how-does-it-work"></a>[]() どのような仕組みですか?
[**エンティティ ストア**] エンティティを更新すると、次のアクションが実行されます。

-   認識サービスによって必要とされる形式のデータは、Dynamics 365 for Retail 運用データベースから抽出され、エンティティ ストアに送信されます。
-   このデータは、Azure Data Factory (ADF) によって ADF アクティビティの一部として Hive スクリプトを使用してデータをクレンジングするために使用されます。 クレンジングされたデータは、BLOB ストレージに保存されます。
-   BLOB ストレージからのデータは、Cognitive サービス API によって推奨モデルをトレーニングするために使用されます。

[**推奨事項の有効化**] をオンにして構成ジョブを実行すると、次の操作が実行されます。

-   モデル資格情報と ID は API から取得され、Dynamics 365 for Retail 運用データベース、AOS 用 web.config、および小売サーバーに格納されます。
-   モデルの資格情報と ID は CRT で利用できるようになっており、オンライン モードで Cloud POS と MPOS からの製品推奨事項を守ることができます。


<a name="see-also"></a>参照
--------

[POS デバイスのトランザクション ページへのレコメンデーション コントロールの追加](add-recommendations-control-pos-screen.md)




