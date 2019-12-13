---
title: Dynamics 365 Retail の製品評価の同期
description: このトピックでは、Microsoft Dynamics 365 Retailで製品評価を同期する方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: db5a4e1f78797d20ded2274cc99bef422fd50acc
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698168"
---
# <a name="sync-product-ratings-in-dynamics-365-retail"></a>Dynamics 365 Retail の製品評価の同期

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Retailで製品評価を同期する方法について説明します。

## <a name="overview"></a>概要

販売時点管理 (POS) およびコール センターなどのオムニチャネルで製品評価を使用するには、評価およびレビュー サービスからの製品評価を Retail チャネル データベースにインポートする必要があります。 製品評価をオムニチャネルで使用可能にした場合、顧客が販売担当者との対話を間接的に行うのに役立ちます。

このトピックでは、次のタスクについて説明します。

1. 製品評価をインポートする Retail バッチ ジョブをコンフィギュレーションします。
1. 製品評価の同期のバッチ ジョブが正常に行われたことを確認します。
1. POS で製品評価を使用可能にします。

## <a name="configure-a-retail-batch-job-to-import-product-ratings"></a>製品評価をインポートする Retail バッチ ジョブのコンフィギュレーション

> [!IMPORTANT]
> 開始する前に、バージョン 10.0.6 またはそれ以降の Retail がインストールされていることを確認してください。

### <a name="initialize-the-retail-scheduler"></a>小売用スケジューラの初期化

小売のスケジューラを初期化するには、次の手順に従います。

1. **小売 \> 本社の設定 \> 小売用スケジューラ \> 小売用スケジューラの初期化**に移動します。 または、「小売用スケジューラの初期化」を検索します。
1. **Retail スケジューラの初期化** ダイアログ ボックスで、**既存のコンフィギュレーションの削除** オプションが**いいえ**に設定されていることを確認し、**OK** を選択します。

### <a name="verify-the-retailproductrating-subjob"></a>RetailProductRating サブジョブの検証

**RetailProductRating** サブジョブが存在していることを検証するには、以下の手順に従います。

1. **小売 \> 本社の設定 \> 小売用スケジューラ \>スケジューラ サブジョブ**に移動します。 または、「スケジューラ サブジョブ」を検索します。
1. サブジョブ リストで、**RetailProductRating** サブジョブを検索します。

次の図は、Retail のサブジョブの詳細ページの例を表示しています。

![RetailProductRating サブジョブの詳細](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> **RetailProductRating** サブジョブを検索できない場合、Retail スケジューラーを初期化する前に、**同期製品の評価**ジョブおよび **1040 CDX** ジョブが既に実行されている可能性があります。 この場合、次の手順に従って**完全データ同期**ジョブを実行します。
>
> 1. **小売 \> 本社の設定 \> 小売用スケジューラ \> チャネル データベース**の順に移動します。 または、「チャネル データベース」を検索します。
> 1. 同期するチャネル データベースを選択します。
> 1. アクション ウィンドウで、**完全なデータの同期**を選択します。
> 1. **配送スケジュールの選択**ドロップダウン ダイアログ ボックスで、**1040 - 製品**を選択し、**OK** を選択します。
> 1. 前の手順を繰り返して、**RetailProductRating** サブジョブが作成されていることを確認します。

### <a name="import-product-ratings"></a>製品評価のインポート

評価およびレビュー サービスから製品評価を Retail にインポートするには、次の手順に従います。

1. **小売 \> 本社の設定 \> 小売用スケジューラ \> 製品評価の同期ジョブ**に移動します。 または、「製品評価の同期ジョブ」を検索します。
1. **製品評価のプル** ダイアログ ボックスの**バックグラウンドで実行**クイック タブで、**定期的なアイテム**を選択します。
1. **定期的なアイテムの定義** ダイアログ ボックスで、定期的なアイテムのパターンを設定します。 (提案される値は 2 時間です) 1 時間未満の定期的なアイテムをスケジュールしないでください。
1. **OK** を選択します。
1. **バッチ処理**オプションを**はい**に設定します。 この設定によりログを監査して、バッチ ジョブの実行状況を確認できるようになります。
1. バッチ ジョブをスケジュールするには、**OK** を選択します。

次の図は、Retail のバッチ ジョブ コンフィギュレーションの例を表示しています。

![製品評価の同期バッチ ジョブのコンフィギュレーション](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a>製品評価の同期のバッチ ジョブが正常に行われたことの確認

**製品評価の同期**バッチ ジョブが正常に行われたことを確認するには、次の手順に従います。

1. **Retail \> システム管理者 \> 照会\> バッチ ジョブ**に移動するか、または Retail 専用の最小在庫管理単位 (SKU) を使用している場合、代わりに **Retail \> 照会およびレポート \> バッチ ジョブ**を使用します。 または、「バッチ ジョブ」を検索します。
1. バッチ ジョブの詳細を表示するには、バッチ ジョブ リストの**ジョブの説明**の列で、「製品評価をプル」を含む説明を検索します。
1. ジョブ ID を選択して、開始予定日/時刻および定期的なアイテムのテキストなどのバッチ ジョブの詳細を表示します。

次の図は、バッチ ジョブが 2 時間間隔で実行するようにスケジュールされている場合の、Retail でのバッチ ジョブの詳細の例を表示しています。

![製品評価の同期バッチ ジョブの詳細](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a>POS で製品評価を使用可能にする

Dynamics 365 Commerce の評価およびレビュー ソリューションは、オムニチャネル ソリューションです。 ただし、既定では、製品の評価は POS に表示されません。 販売担当者が店舗の顧客に評価とレビューを表示するには、POS で製品評価を有効にする必要があります。

POS で製品の評価を有効にするには、次の手順に従います。

1. **Retail \> Retail の設定 \> パラメーター \> Retail のパラメーター**の順にクリックします。 または、「Retail のパラメーター」を検索します。
1. **コンフィギュレーション パラメーター** タブで、**新規**を選択します。
1. **RatingsAndReviews.EnableProductRatingsForRetailStores**などの名前を入力し、値を**はい**に設定します。
1. **保存** を選択します。
1. **小売 \> 小売 IT \> 配送スケジュール**の順に移動します。 また、「配送スケジュール」を検索します。
1. ジョブ リストで、**1110** (**グローバル構成**) を選択し、**今すぐ実行**を選択します。
1. ジョブが正常に実行された後、製品の評価が POS に表示されていることを確認します。

次の図は、POS で製品評価を有効にするための Retail パラメーターのコンフィギュレーションの例を表示しています。

![POS での製品評価の Retail パラメーターのコンフィギュレーション](media/rnr-hq-enable-ratings-in-pos.png)

以下の図は、POS の製品評価の例を表示しています。

![POS での製品評価](media/rnr-pos-catalog-ratings.png)

次の図は、コール センター チャネルの製品評価の例を表示しています。

![コール センター チャネルの製品評価](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a>追加リソース

[評価とレビューの概要](ratings-reviews-overview.md)

[評価とレビューを使用するためのオプト イン](opt-in-ratings-reviews.md)

[評価とレビューの管理](manage-reviews.md)

[評価とレビューのコンフィギュレーション](configure-ratings-reviews.md)
