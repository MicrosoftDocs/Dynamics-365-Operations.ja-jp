---
title: 自動化エンティティ格納更新
description: このトピックでは自動化エンティティ格納更新を有効にする方法について説明します。
author: MilindaV2
manager: AnnBe
ms.date: 01/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: AutomatedEntityStoreRefresh
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27661
ms.assetid: 861cfa94-c6f3-4c84-89ac-22c78bf6b7a4
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca7584ce242bbc4c4545b230c3d6cc3483aff065
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1502930"
---
# <a name="automated-entity-store-refresh"></a>自動化エンティティ格納更新

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概要

エンティティ格納が自動化され、システムにより管理されます。 管理者はシステム バッチ スケジュールを使用してエンティティ格納更新をスケジュールまたは監視する必要はありません。 更新操作は予想待機時間に基づいています。 この機能は、Platform update 23 で有効化されます。 管理者として、この機能を使用するためにオプトインを実行する必要があります。

## <a name="enable-automated-refresh"></a>自動化更新を有効にする
以下の手順を完了して自動化エンティティ格納更新を有効にします。

1. **システム管理** > **セットアップ** > **エンティティ格納** の順に移動します。 **エンティティ店舗** ページで、メッセージに、**自動エンティティ格納更新** オプションに切り替えることができることが示されます。 このオプションは、システムによって管理されます。 管理者はエンティティ格納更新をスケジュールまたは監視する必要はありません。

2. **今すぐ切り替える** を選択します。

  > [!IMPORTANT]
  > このアクションは、元に戻すことはできません。 **自動エンティティ格納更新** オプションに切り替えた後、古いユーザー インターフェイス (UI) エクスペリエンスに戻すことはできません。

3. **はい** を選択して続行します。

新しいエクスペリエンスが表示されます。

![新しい UI エクスペリエンス](./media/entity-store-data-lake-3.JPG)

新しいエクスペリエンスをオンにすると、それぞれの集計の測定で更新を定義できます。 次の更新オプションを選択できます。

- 1 時間ごと
- 1 日に 2 回
- 1 日に 1 回
- 1 週間に 1 回

**更新** ボタンをクリックすることにより、管理者が必要に応じて任意の集計測定を更新することができます。 追加のオプションは、将来のプラットフォーム更新プログラムで追加されます。 これらのオプションには、リアルタイム更新のオプションが含められます。

> [!IMPORTANT]
> 自動化更新を有効にすると、システムは集計測定の更新を無効にすることができます。 集計測定に戻って、適切な更新間隔が適用されていることを検証する必要があります。
