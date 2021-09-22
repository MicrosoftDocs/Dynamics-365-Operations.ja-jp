---
title: 作業タイプとして在庫状態の変更を選択できない
description: この作業タイプはシステム プロセスでのみ使用されるので、在庫状態変更用の作業テンプレート行を作成できません。 別の作業タイプを選択してください。
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ad7f26f3235d15779583f9cdadeb4e6dca16242a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476910"
---
# <a name="cant-select-inventory-status-change-in-the-work-type-column"></a>作業タイプ列で在庫状態の変更を選択できない

## <a name="symptoms"></a>現象

Microsoft Dynamics 365 Supply Chain Management を構成する際、次のエラー メッセージが表示される場合があります。

> この作業タイプが有効でないため、在庫状態変更用の作業テンプレート行を作成できません。 別の作業タイプを選択してください。

## <a name="resolution"></a>解決策

この動作は仕様です。 *在庫ステータス変更* 作業タイプは、システム プロセスでのみ使用されます。 この値は構成できません。 作業タイプのリストは列挙として固定されているため、追加のエントリを **作業タイプ** ドロップダウン メニューからフィルターで除外することはできません。
