---
title: バッチ内の月次仕訳入力の作成
description: このトピックでは、バッチで仕訳入力を作成し、月別のリース経費を記録する際の効率を高める方法について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a2293f6bd3ce66832996652c3bfca0fc4bc73782
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445384"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a>バッチ内の月次仕訳入力の作成

[!include [banner](../includes/banner.md)]

このトピックでは、バッチで仕訳入力を作成し、月別のリース経費を記録する際の効率を高める方法について説明します。 バッチ処理を使用すると、複数のスケジュールから仕訳入力を作成できます。 これらの仕訳入力には、リース支払、負債償却費、使用権 (ROU) 資産償却、履行費用経費が含まれます。 また、バッチ処理を利用して、複数のリースの初期認識を同時に行ったり、複数のリースの移行調整を同時に行うこともできます。

バッチ ジョブの設定や、複数のリースの支払請求書、減価償却、利息を処理するには、**資産リース \> 定期処理 \> バッチ仕訳作成** に移動します。 表示されるダイアログ ボックスで、仕訳入力の作成元となるスケジュールを選択できます。 また、特定のエンティティ、リース グループ、またはリース ブックに対してバッチ処理を実行するかどうかを指定することもできます

> [!NOTE]
> 負債の償却予定額、支払額、減価償却費、費用の計上は、リース取引開始時に認識したものを転記した後に行います。
>
> 仕訳入力は作成されますが、**実行** コマンドを選択するまでは転記されません。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]