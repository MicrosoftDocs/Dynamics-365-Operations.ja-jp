---
title: リソース キャパシティの同期
description: このトピックでは、カレンダーとプロジェクトの間でリソースの能力を同期化する方法について説明します。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760592"
---
# <a name="synchronize-resource-capacity"></a>リソース キャパシティの同期

[!include [banner](../includes/banner.md)]

リソース同期のプロセスは、カレンダーの情報および基準カレンダーがプロジェクトのリソース スケジューリングにトリクルダウンするのを保証するために役立ちます。 カレンダーが変更される場合、プロセスはプロジェクト リソースのスケジューリングに必要な更新を行います。 カレンダーのリソースの情報が事前に同期化されているため、プロセスもパフォーマンスを向上させるのに役立ちます。 したがって、リソースのスケジューリング情報の更新がより迅速に行われます。 一つずつ作成する代わりに、バッチとしてプロセスをスケジューリングすることをお勧めします。 それ以外の場合は、情報が最後に同期された包含日付を忘れるリスクがあります。 包含日付を使用しない場合、日付の同期時にギャップが発生します。

![カレンダーの同期](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>リソース能力のロールアップを同期

同期プロセスは、すべてのリソース カレンダー情報と同期するように設計されています。 この情報には、プロジェクトのリソース カレンダー能力テーブルの変更についての基準カレンダーの情報が含まれます。 新しいリソースがプロジェクトに追加されると、同期により、更新されたカレンダー情報が使用可能になります。 この同期はいつでも実行できます。

バッチを使用することをお勧めします。 確保済能力の同期中に、このオプションを使用できます。

1. **プロジェクト管理および会計** &gt; **定期処理** &gt; **能力の同期** &gt; **リソース能力のロールアップを同期**の順に選択します。
2. 次の表でオプションを設定します。

    | オプション      | 説明 |
    |-------------|-------------|
    | 期間コード | 必要に応じて、リソース能力のロールアップの同期プロセス用に開始日と終了日を設定する、一般会計の日付間隔コードを選択します。 |
    | 入社日  | リソース能力のロールアップの同期プロセスの開始日を入力します。 |
    | 終了日    | リソース能力のロールアップの同期プロセスの終了日を入力します。 |

[![同期プロセス](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)
