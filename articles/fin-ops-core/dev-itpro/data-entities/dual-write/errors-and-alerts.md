---
title: エラー管理と警告通知
description: このトピックでは、問題のトラブルシューティングに役立つエラー ログと警告通知について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e27a441ddbeeac1e64c77168414177191cba4f5f
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744707"
---
# <a name="error-management-and-alert-notifications"></a>エラー管理と警告通知

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Microsoft は、エラーに強い二重書き込みを実現するために、多くの時間と労力を費やしてきました。 ただし、二重書き込み用のテーブル マップを有効にしている間または後に、問題が発生した場合は、特定のテーブル マップを選択して、それらのすべてのアクティビティとエラーの統合ビューを取得できます。 この統合ビューには、エラー ログが含まれています。 目標は、テーブル マップのアクティビティの単一ビューを提供することにより、トラブルシューティングを支援することです。

## <a name="consolidated-error-management"></a>統合されたエラー管理

アクティビティ ログは、特定のテーブル マップが **実行していません** の状態から **実行中** 状態に移行するイベントの時系列一覧を提供します。 たとえば、一覧には、作成されたマッピング、列マッピングの更新、実行されたマッピングを含めることができます。 さらに、エラーが発生した場合は、ログをダウンロードして、次のレベルの詳細を取得できます。

![アクティビティ ログの表示](media/activity-log.png)

Finance and Operations アプリ と Dataverse の間で既存のデータをコピーしているときに問題が発生した場合、**初回同期の詳細** タブにエラー数が表示されます。 また、原因となっているエラーを修正した後、実行を再実行することもできます。

![エラーの修正と再実行](media/fix-error-rerun.png)

さらにドリル ダウンして、エラーが発生した同期の方向を表示できます。 この情報は、トラブルシューティングの範囲を絞り込むのに役立ちます。

![同期方向エラーの表示](media/sync-direction-error.png)

同様に、**キャッチ アップ エラー** タブは、一時停止状態から再開したときの問題のトラブルシューティングに役立ちます。

## <a name="alert-notifications"></a>警告の通知

管理者は、1 つ以上の警告設定を作成して、計画的または計画外のメンテナンスのケースを処理することができます。 たとえば、ネットワーク エラーなどが原因で特定のエラーしきい値に達した場合に、電子メールで通知するように、二重書き込みシステムを設定できます。 二重書き込みシステムは、ユーザーの代わりにアクションを実行することもできます。 たとえば、二重書き込みを一時停止または停止することができます。

次の図は、**アプリケーション エラー** タイプのエラーが 15 分以内に 10 回発生した場合に、二重書き込みが一時停止する例を示しています。

![1 つ以上の警告設定の作成](media/create-alert-settings.png)

**警告設定の作成** を選択することにより、追加の警告を作成できます。 また、個人またはグループのどちらに通知を送信するかを選択したり、二重書き込みシステムがユーザーに代わりにアクションを実行するかどうかを選択することもできます。

![警告の作成と通知の送信](media/create-alert-notification.png)

この機能は、計画外のメンテナンスがある場合に特に便利です。 たとえば、アプリの 1 つが使用できなくなり、定義したしきい値に基づいて、二重書き込みが一時停止状態になり、すべての新しい要求がキューに入れられるます (つまり、それらは失われません)。 基になる問題を修正し、両方のアプリが正常に実行されたら、一時停止状態から再開できます。 更新はキューから読み戻され、復元されたアプリに書き込まれます。

## <a name="next-steps"></a>次のステップ

[アプリケーション ライフサイクル管理](app-lifecycle-management.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]