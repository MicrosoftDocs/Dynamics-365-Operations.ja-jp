---
title: 陸揚原価の調達パラメーター
description: この記事では、陸揚原価モジュールを使用する場合に、関連する調達パラメーターを設定する方法について説明します。
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905982"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>陸揚原価の調達パラメーター

[!include [banner](../../includes/banner.md)]

**調達パラメーター** ページには、**陸揚原価** モジュールを使用する場合に特に関連するいくつかの設定があります。 **調達パラメーター** ページから開く **注文明細行の更新** ダイアログ ボックスを使用して、発注書ヘッダーで変更が加えられたときに発注書明細行を自動的に更新するかどうかを指定します。

この設定を完了するには、次の手順に従います。

1. **調達 \> セットアップ \> 調達パラメーター** の順に移動します。
1. **全般** タブで 、 **注文明細行の更新** リンクを選択します。
1. **注文明細行の更新** ダイアログ ボックスには、注文ヘッダーのフィールドが一覧表示され、注文明細行の関連フィールドに自動更新を適用することもできます。 一覧の各フィールドを次のいずれかの値に設定します。

    - **常時** – 注文ヘッダーの更新時に注文明細行が自動的に更新されます。
    - **なし** – 注文ヘッダーの更新時に注文明細行を決して更新しません。
    - **プロンプト** – 注文明細行を更新するかどうかを選択するように求められます。
