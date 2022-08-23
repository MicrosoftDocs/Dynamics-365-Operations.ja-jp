---
title: 顧客作成モードを非同期化するに関するよくあるご質問
description: この記事は、Microsoft Dynamics 365 Commerce で非同期顧客の作成についてよく寄せられる質問に対する回答を提供します。
author: gvrmohanreddy
ms.date: 08/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 35c999695ed33c4fc9731a5b8dd4d679cf55fa44
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229874"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>顧客作成モードを非同期化するに関するよくあるご質問

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

この記事は、Microsoft Dynamics 365 Commerce で非同期 (async) 顧客の作成についてよく寄せられる質問に対する回答を提供します。

### <a name="why-cant-i-enable-the-enable-editing-customers-in-asynchronous-mode-feature"></a>"非同期モードでの顧客の編集を有効にする" 機能を有効にできないのはなぜですか？

**非同期モード機能での顧客の 編集の有効化を有効にする** 前に、次の機能を有効にする必要があります。

- 顧客注文および顧客トランザクションのパフォーマンス向上
- 顧客の拡張非同期作成を有効にする
- 顧客住所の非同期作成の有効化

### <a name="why-do-i-still-see-real-time-service-calls-made-to-commerce-headquarters-after-the-enable-editing-customers-in-asynchronous-mode-feature-is-enabled"></a>"非同期モードでの顧客の編集を有効にする" 機能が有効になっていると、なぜ Commerce Headquarters に対するリアルタイム サービス コールが表示されるのですか。

この問題は、機能の状態および他のチャンネル メタデータがチャンネルと同期するために Commerce Data Exchange (CDX) ジョブが実行されていない場合に発生します。 シナリオを再試行する前に、Commerce Headquarters で次の CDX ジョブが実行されている必要があります。

- 1110 (グローバル構成)
- 1010 (顧客)
- 1070 (チャネル構成)

CDX ジョブの実行後、Commerce Scale Unit (CSU) にキャッシュされたデータが Commerce Headquarters にすぐに反映されない場合があります。

### <a name="why-doesnt-commerce-headquarters-show-customer-creation-or-updates-from-the-point-of-sale-pos-or-e-commerce-channel"></a>Commerce Headquarters では、POS (POS) または電子コマース チャンネルからの顧客の作成や更新が表示されるのでは、なぜですか。

次のアクションが、記載されている順に実行されたとします。

1. **RETAILASYNCCUSTOMERV2**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERILIATION**、および **RETAILASYNCCUSTTRIBUTBUT 2** の各テーブルに格納されている同期顧客データを Commerce Headquarters で使用できる状態にするための CDX P ジョブを実行します。
1. Commerce Headquarters で **顧客とチャンネル要求の同期** のバッチ ジョブを実行します。 バッチ ジョブが 正常に実行された後で、前述のテーブルから正常に処理されたレコードはすべて **OnlineOperationCompleted** フィールドを **1** に設定します。
