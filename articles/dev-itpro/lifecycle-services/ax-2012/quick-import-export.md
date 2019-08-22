---
title: 簡易インポートとエクスポート
description: 簡易インポート/エクスポートの目的は、より少ない手順でインポートとエクスポートを実行できるようにすることです。
author: margoc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: dynamics-ax-2012
ms.service: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: AX 2012
ms.custom: 89041
ms.assetid: 990d64e6-d436-4c79-9bb5-bf8c5c5a048f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 2012 R3 CU8
ms.openlocfilehash: 7655de1399c49328bae1736c796325e546796bd5
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850516"
---
# <a name="quick-import-export"></a>簡易インポートとエクスポート

[!include [banner](../../includes/banner.md)]

簡易インポート/エクスポートの目的は、より少ない手順でインポートとエクスポートを実行できるようにすることです。

ユーザーがインポートまたはエクスポートの簡易なジョブを迅速に実行できるよう [簡易インポート/エクスポート] 機能を追加しました。 原則的にこの機能は、ファイルがシステムに自動的にマップしており、ユーザーは高度なマッピングを行ったりインポートまたはエクスポート ジョブを繰り返し作成する必要はない、というシナリオ内で使用します。

- この機能は、追加設定なしでの使用、さらにカスタム エンティティ両方の操作をサポートします。
- ファイルからインポートすることができ、ODBC データ ソースを使用している場合は、インポートを定義するクエリを選択します。
- AX またはファイルのいずれかのソース データ形式を事前に定義しておく必要があり、それらの場所が決まっています。
- 簡易インポート/エクスポートを使用するために処理グループを作成する必要はありません。それはインポートまたはエクスポート ジョブを実行するとき自動的にシステムにより作成されます。 簡易インポート/エクスポートによりインポートされたデータの履歴を保存するよう選択することもできます。

  簡易インポート/エクスポートは、DIXF の概念に精通しているという前提で使用するように注意してください。



