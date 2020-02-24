---
title: 小売価格レポート
description: このトピックでは、さまざまな製品の今後の価格変更を表示するために使用できる価格レポート機能の概要を提供します。
author: shajain
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16181
ms.assetid: b1b57734-1406-4ed6-8e28-21c705ee17e2
ms.search.region: global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2019-01-18
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 91c0a96abdd7df9e85e63ca6b1b47a57f3f401eb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023207"
---
# <a name="retail-price-reports"></a>小売価格レポート

[!include [banner](includes/banner.md)]


顧客に競争力のある価格を提供するために、小売業者はしばしば製品の価格を変更します。 店舗マネージャーは、店舗の棚に表示されている価格を更新するために必要なリソースを計画できるように、最新または今後の価格変更に簡単にアクセスできる機能を求めています。 Retail のリリース 10.0 で、店舗マネージャーが**価格**レポートを開くには、**すべての店舗 \> 店舗 \> 価格レポート**に移動し、その店舗に関連する製品の更新された価格を表示します。 

価格レポートを有効にするには、**店舗の価格レポートを有効にする**パラメーターをオンにする必要があります。 このパラメーターは、**コマース パラメーター \> 割引 \> その他**タブにあります。**価格レポート** ページを開くと、さまざまな構成のダイアログ ボックスが表示されます。 使用可能な構成は次のとおりです。

| 構成 | 説明 |
|---|---|
| 開始日 / 終了日| 価格レポートが生成される日付範囲。 期間は現在 7 日間に制限されています。 |
| チャネル| 価格レポートが生成される店舗。 |
| 使用可能な在庫がある製品を表示| これを**はい**に設定すると、現在店舗に現物在庫がある製品のみの価格が表示されます。 |
| バリアントの価格を表示 | これを**はい**に設定すると、製品マスターと共にバリアントの価格が表示されます。 行数が非常に増加するために、バリアント固有の価格がある場合はこれを**オン**にする必要があります。 将来のリリースでは、分析コードに基づく価格を有効にし、店舗マネージャーが表示する価格の分析コードを選択できるようにします。 |
| 価格変更のある製品の表示 | これを**はい**設定すると、価格が変更された日付のみの価格が表示されます。 選択した**開始日**から*1 日前*の価格が常に表示され、それにより店舗マネージャーは選択した期間に価格変更がない製品を簡単に識別でき、また現在の価格も確認できます。 |

レポートが生成された後、追加のフィルタリング ニーズに合わせて Excel ファイルをダウンロードできます。 価格レポートを使用して、過去の日付の製品の価格履歴を確認することもできます。