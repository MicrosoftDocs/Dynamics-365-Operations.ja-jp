---
title: LCS にタスク ガイドを保存して再生する
description: この記事では、タスク Guides を Microsoft Dynamics Lifecycle Services (LCS) に保存し、それらを再生する方法について説明します。
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c81c345932e0e3dce4b13104222ed9f668a3c460
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113326"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>LCS にタスク ガイドを保存して再生する

**環境の詳細** 

Microsoft Dynamics Lifecycle Services (LCS) 経由で配置された Microsoft Dynamics 365 Human Resources

**払出**

顧客は自分の LCS プロジェクトに新しいタスクの記録を保存し、保存されているタスク ガイドを再生することを希望しています。

**解像度**

LCS にタスク記録を保存するには、次の手順に従います。

1. LCS にサインインして、プロジェクトを選択します。
2. **ビジネス プロセス モデラー** タイルを選択します。
3. 「更新された BPM エクスペリエンス。」でページを表示する
4. ライブラリを選択してから、**コピー** を選択します。
5. ビジネス プロセス モデラー (BPM) モデルの名前を入力します。
6. LCS から人事管理にログインします。
7. **検索** フィールドで、**ヘルプ** と入力します。 Lifecycle Services ヘルプが開きます。
8. Lifecycle Services のヘルプ構成の **更新** ボタンを選択します。

    新しい有効な BPM ライブラリが表示されます。

9. ページを閉じます。
10. タスク記録を作成します。
11. 完了したら、**Lifecycle Services に保存** を選択します。

    ![Lifecycle Services に保存](media/task-guides.png)

12. タスク記録を保存する BPM ライブラリとノードを選択します。

LCS からタスク ガイドを再生するにはこれらの手順に従います。

1. タスク レコーダーを開始します。
2. **LCS から開く** を選択します。
3. タスク ガイドが保存されているライブラリと BPM ノードを選択します。
4. タスク ガイドを開きます。
