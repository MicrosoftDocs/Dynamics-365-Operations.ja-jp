---
title: 顧客作成モードを非同期化するに関するよくあるご質問
description: この記事は、Microsoft Dynamics 365 Commerce で非同期顧客の作成についてよく寄せられる質問に対する回答を提供します。
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-12-17
ms.openlocfilehash: 64c895fb9f3e55f7680759fa72626be6660aa67c
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690205"
---
# <a name="asynchronous-customer-creation-mode-faq"></a>顧客作成モードを非同期化するに関するよくあるご質問

[!include [banner](includes/banner.md)]

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

1. Commerce headquarters で CDX P-ジョブを実行して、同期顧客データが **RETAILASYNCCUSTOMERV2**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERCONTACT**、**RETAILASYNCCUSTOMERILIATION**、および **RETAILASYNCCUSTTRIBUTBUT 2** に格納していることを確認します。
1. Commerce Headquarters で **顧客とチャンネル要求の同期** のバッチ ジョブを実行します。 バッチ ジョブが 正常に実行された後で、前述のテーブルから正常に処理されたレコードはすべて **OnlineOperationCompleted** フィールドを **1** に設定します。

### <a name="how-do-i-know-which-customer-management-in-asynchronous-mode-operation-has-failed-and-how-do-i-make-changes-if-they-are-required"></a>非同期モードの操作で失敗した顧客管理を確認し、必要に応じて変更を加える方法は?

すべての非同期モードの操作とその同期ステータスを表示するには、Commerce Headquarters で **Commerce と Retail \> 顧客 \> 顧客同期ステータス** に移動します。 変更するには、特定の操作を編集し、フィールドを更新し、**保存** を選択して、**同期** を選択して変更を同期します。

