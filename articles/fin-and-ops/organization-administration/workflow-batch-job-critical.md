---
title: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
description: ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション
author: aneesmsft
manager: AnnBe
ms.date: 05/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 9dc45189-6e7e-4207-ad78-dbbb644dd1ce
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2017-05-19
ms.dyn365.ops.version: Platform update 6
ms.openlocfilehash: 98b89f4a11fc0c791358cbec8e617bb8417c11d3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369038"
---
# <a name="configure-the-workflow-message-processing-batch-job-as-critical"></a>ワークフロー メッセージ処理バッチ ジョブの重要なものとしてのコンフィギュレーション

[!include [banner](../includes/banner.md)]

ワークフロー システムでは、さまざまなバッチ ジョブを使用します。 **ワークフロー メッセージ処理**は、ワークフロー メッセージを処理するために使用される重要なバッチ ジョブです。 ワークフローが組織の重要なコンポーネントである場合は、**ワークフロー メッセージ処理**バッチ ジョブを重要なものとして構成することを検討する必要があります。

**処理中のワークフロー メッセージ** バッチジョブを重要なものとしてコンフィギュレーションすることにより、システムはその状態を積極的に追跡します。 重要なバッチ ジョブが失敗したとき、サポート チームは、不具合の原因となった可能性のある問題を解決するために、不具合をよく観察して措置を講じることができます。

**ワークフロー メッセージ処理**バッチ ジョブを重要なものとしてコンフィギュレーションするには、これらの手順に従います。

1. **バッチ ジョブ** ページに移動します。
2. クイック フィルターを使用して**ワークフロー メッセージ処理**を検索します。
3. **ワークフロー メッセージ処理** バッチ ジョブを選択します。
4. アクション ウィンドウの**編集**をクリックします。
5. **重要なジョブ** チェック ボックスをオンにします。
6. アクション ウィンドウの**保存**をクリックします。
