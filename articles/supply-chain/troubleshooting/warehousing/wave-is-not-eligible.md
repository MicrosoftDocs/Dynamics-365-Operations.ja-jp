---
title: ウェーブがクリーンアップの使用に適さない
description: ウェーブがクリーンアップの使用に適さない
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWaveTable_WHSWaveProcessingDataCleanup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 99d76b6a90045be7630785769b11e43abaf4b789b1c4a134050b6ee396c71199
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778509"
---
# <a name="wave-isnt-eligible-for-cleanup"></a>ウェーブがクリーンアップの使用に適さない

エラー コード: WaveNotEligibleForCleanup

## <a name="symptoms"></a>現象

システムは次のエラー メッセージを表示します。

> ウェーブ %1 はクリーンアップに適しません。

ウェーブ データは、クリーンアップできません。  

## <a name="cause"></a>原因

次のいずれかの条件で示されているように、ウェーブは、現在処理されています。

- **ウェーブの状態** フィールドは *実行中* に設定されます。
- アクション ウィンドウの **ウェーブ** タブにある **ウェーブ** グループで **バッチ ジョブ** を選択すると、**状態** フィールドが *終了済*、*エラー*、または *キャンセル済* に設定されません。 したがって、バッチ ジョブは現在実行中です。

## <a name="resolution"></a>解像度

アクション ウィンドウの **ウェーブ** タブの **ウェーブ** グループで、**バッチ ジョブ** を選択し、次のいずれかの手順に従います。

- **状態** フィールドが *実行中* に設定されている場合: アクション ウィンドウの **バッチ ジョブ** タブにある **バッチ ジョブ** グループで、**タスクの表示** を選択します。 **バッチ タスク** ページを更新すると、進捗状況を追跡することができます。
- **状態** フィールドが *実行中* に設定されていない場合: アクション ウィンドウの **バッチ ジョブ** タブにある **機能** グループで、**状態の変更** を選択します。 **新しい状態の選択** フィールドで、*待機中* を選択します。 その後、**OK** を選択します。
