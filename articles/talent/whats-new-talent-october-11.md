---
title: Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 15 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent Core HR の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a50819d579c0ea42aac3f9a18fbcbf0d2cb9ca26
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518485"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-october-15-2018"></a>Dynamics 365 for Talent Core HR の新機能および変更された機能 (2018 年 10 月 15 日)

[!include [banner](includes/banner.md)]

**ビルド 8.1.1056**

このトピックでは、Core HR の新機能または変更された機能について説明します。


## <a name="changes"></a>変更
その他の修正プログラムに加え、次の更新プログラムが今回のリリースで行われました。
- 最終勤務日は、採用時または雇用終了日を設定した時に設定されるようになりました。
- 米国コンプライアンスの参照は、非米国企業の場合に削除されました (ACA, ADA, and I9)。
- 無効な日付 (1900 年 1 月 1 日) が分析ページで非表示になりました。

## <a name="known-issue"></a>既知の問題

**問題:** 作業者に新しい添付ファイルを追加する場合、**新規**および**編集**ボタンは灰色表示です。**回避策:** 添付ファイル ページを開く前に、**作業者**ページの Factbox が閉じていることを確認します。 **作業者**ページが読み込まれる時、FactBoxes が閉じている場合には、添付ファイルボタンが有効になります。 (この問題は次のプラットフォーム更新プログラムで修正されます。)
