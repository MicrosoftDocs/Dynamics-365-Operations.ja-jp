---
title: 収集された推奨事項の手動作成
description: このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の顧客のために、製品リストを手動で作成および管理する方法を説明します。
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e9ce8887f3cd7da0e250d3b0ffe96b222953de44
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965356"
---
# <a name="manually-create-curated-recommendations"></a>収集された推奨事項の手動作成

[!include [banner](includes/banner.md)]

このトピックでは、小売業者が Microsoft Dynamics 365 Commerce の顧客のために、製品の推奨リストを手動で作成および管理する方法を説明します。

キュレーション リストとは、ユーザーによって作成され、精選された、個々のコンテンツの集合のことです。  

## <a name="create-a-new-list"></a>新しいリストの作成

精選された製品推奨事項リストを作成するには、次の手順に従います。

1. **小売りとコマース &gt; 製品推奨事項 &gt; 推奨リスト** に移動します。
1. **新規** を選択します。
1. **リスト ID** フィールドに値を入力します。
1. **リスト名** フィールドに値を入力します。
    - **リスト名** は、**製品収集** モジュールの精選されたリスト セクションに表示されるリストのタイトルです。
1. リストに製品を追加するには、**製品の追加** を選択します。
1. リスト上で製品の表示順を変えるには、**表示順** 列に値を入力します。
    - 2 つの製品が同じ表示順の値を持つ場合、それら 2 つの最終的な並び順は、バック オフィスとは異なることがあります。
1. **保存** を選択してリストを保存します。

## <a name="example-list"></a>リストの例

![バック オフィスのキュレーション リストの例](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>追加リソース

[製品推奨事項の概要](product-recommendations.md)

[Dynamics 365 Commerce 環境で Azure Data Lake Storage を有効化する](enable-adls-environment.md)

[製品推奨事項の有効化](enable-product-recommendations.md)

[カスタマイズされた推奨事項の有効化](personalized-recommendations.md)

[カスタマイズされた推奨事項のオプト アウト](personalization-gdpr.md)

["類似したルックを買う" 推奨を有効にする](shop-similar-looks.md)

[POS での製品推奨事項の追加](product.md)

[トランザクション画面への推奨事項の追加](add-recommendations-control-pos-screen.md)

[AI-ML 推奨事項結果の調整](modify-product-recommendation-results.md)

[推奨事項とデモ データの作成](product-recommendations-demo-data.md)

[製品推奨事項に関するよく寄せられる質問](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]