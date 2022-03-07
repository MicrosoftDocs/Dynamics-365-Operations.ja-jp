---
title: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
description: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
author: ChrisGarty
ms.date: 05/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob
audience: IT Pro
ms.reviewer: sericks
ms.assetid: 9dc45189-6e7e-4207-ad78-dbbb644dd1ce
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2017-05-19
ms.dyn365.ops.version: Platform update 6
ms.openlocfilehash: 66019d7c7464edb557a5bc41a48a7e9cd2ddfff6
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070920"
---
# <a name="configure-the-workflow-message-processing-batch-job-as-critical"></a>ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

ワークフロー システムでは、さまざまなバッチ ジョブを使用します。 **ワークフロー メッセージ処理** は、ワークフロー メッセージを処理するために使用される重要なバッチ ジョブです。 ワークフローが組織の重要なコンポーネントである場合は、**ワークフロー メッセージ処理** バッチ ジョブを重要なものとして構成することを検討する必要があります。

**処理中のワークフロー メッセージ** バッチジョブを重要なものとしてコンフィギュレーションすることにより、システムはその状態を積極的に追跡します。 重要なバッチ ジョブが失敗したとき、サポート チームは、不具合の原因となった可能性のある問題を解決するために、不具合をよく観察して措置を講じることができます。

**ワークフロー メッセージ処理** バッチ ジョブを重要なものとしてコンフィギュレーションするには、これらの手順に従います。

1. **バッチ ジョブ** ページに移動します。
2. クイック フィルターを使用して **ワークフロー メッセージ処理** を検索します。
3. **ワークフロー メッセージ処理** バッチ ジョブを選択します。
4. アクション ウィンドウの **編集** をクリックします。
5. **重要なジョブ** チェック ボックスをオンにします。
6. アクション ウィンドウの **保存** をクリックします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]