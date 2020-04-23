---
title: 例外処理の倉庫作業をキャンセルする
description: このトピックでは、倉庫の監督がブロックされた作業を処理できるようにする、キャンセル作業機能について説明します。
author: omulvad
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTroubIeshootingSeIfService
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2019-10-1
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cb725885fb48293a08915f13a4fb14085e930444
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205808"
---
# <a name="cancel-warehouse-work-for-exception-handling"></a>例外処理の倉庫作業をキャンセルする

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management のキャンセル作業機能を使用して、管理者ユーザーは、現在進行中の特定の倉庫作業をキャンセルできますが、それがシステムによってブロックされたり、例外的な状況では完了できなかったりします。 この機能は、矛盾したデータを修復する SQL 修正スクリプトに対する魅力的で安全な代替手段です。 ただし、これらのスクリプトは通常 IT プロフェッショナルから要求されますが、会社の管理者権限を持つユーザーはこのキャンセル作業機能を使用できます。

**倉庫管理** \> **定期処理のタスク** \> **クリーンアップ \> キャンセル作業**で、キャンセル作業機能にアクセスできます。 **キャンセル作業**ダイアログ ボックスで、キャンセルする作業の作業 ID を指定し、**OK** を選択します。

## <a name="warehouse-work-that-can-be-canceled"></a>キャンセルできる倉庫作業

倉庫ピッキング工程中に、作業者は保管場所からユーザーの場所にピッキングされた数量を登録したが、プット工程を登録できない場合があります。 一貫性のない倉庫データは、作業がブロックされる理由になりますが、常にそうとは限りません。

作業ヘッダーの**キャンセル** ボタンを使用してアクセスできる通常のキャンセル機能とは異なり、キャンセル作業機能では、最後に完了した作業明細行が**プット** タイプの作業明細行である必要はありません。 つまり、キャンセル作業機能では、作業明細行の品目の数量がユーザーの場所にある場合でも、取消ロジックを実行できます。

> [!NOTE]
> 業務上の理由からキャンセルする必要がある作業の場合、倉庫ユーザーは作業ページで通常のキャンセル機能を引き続き使用する必要があります。

**販売**、**移動の出庫**、**原材料ピッキング**、または**補充**タイプの作業のみ、キャンセル作業機能を使用してキャンセルできます。 取消ロジックは、凍結された原材料ピッキング作業または通常のキャンセル機能を使用してキャンセルされる作業に対して実行されることはありません (前の注記を参照)。

作業をブロック解除するには、システムは残りの作業明細行をキャンセルし、ユーザーが指定した作業 ID に関連付けられている倉庫データを修正します。 その後、影響を受ける品目数量を含む、通常の倉庫処理工程を再開できます。

作業がキャンセルされた後に影響を受ける品目を特定の場所に配置するには、ユーザーはモバイル デバイスで在庫移動または数量調整操作を使用する必要があります。
