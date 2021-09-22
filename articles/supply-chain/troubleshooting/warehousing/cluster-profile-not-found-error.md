---
title: クラスター プロファイルが見つかりませんでした
description: 入庫倉庫操作を実行すると、クラスター プロファイルが見つからないというエラーが表示される場合があります。 クラスター プロファイルが正しく設定されていることを確認してください。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476920"
---
# <a name="cluster-profile-cant-be-found"></a>クラスター プロファイルが見つかりません

## <a name="symptoms"></a>現象

入庫倉庫操作を行う場合、次のエラー メッセージが表示される場合があります。

> 「品質指示 %1 が生成されました。 クラスター プロファイルが見つかりませんでした。 コンフィギュレーションを確認してください。」

このエラー メッセージは、品質管理 (QMS) が有効になっている入庫プロセスに関連しています。 環境内のコンフィギュレーションによっては、エラー メッセージを生成するトランザクションに関する詳細情報を追加すると、問題を修正できる場合があります。

## <a name="resolution"></a>解決策

最初に、クラスター ピッキング設定を確認し、クラスター プロファイルが正しく設定されていることを確認します。 クラスター プロファイルが設定されていない場合は、モバイル デバイスのメニュー項目をクラスター ピッキングに使用することはできません。 環境によっては、その他の関連するコンフィギュレーションも検討する必要があります。
