---
title: 部分的な数量作業に対して在庫ステータスの変更を行う
description: このページでは、作業者がバッチの一部の数量の在庫ステータスを変更できるようにするために、適切な設定を使用してメニュー項目を作成する方法について説明します。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476826"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>部分的な数量作業に対して在庫ステータスの変更を有効にする

## <a name="symptoms"></a>現象

バッチの一部の数量の在庫ステータスを変更する必要があります。

## <a name="resolution"></a>解決策

作業者がこの変更を行うことができるようにするには、倉庫管理モバイル アプリのメニュー項目を作成します。 **モバイル デバイスのメニュー項目** ページで、次の設定を持つメニュー項目を作成 (または編集) します。

- **モード:** *作業*
- **既存の作業を使用する :** *いいえ*
- **作業作成プロセス:** *移動*
- **在庫状態の表示:** *はい*

必要に応じて、ページの他のフィールドを設定できます。
