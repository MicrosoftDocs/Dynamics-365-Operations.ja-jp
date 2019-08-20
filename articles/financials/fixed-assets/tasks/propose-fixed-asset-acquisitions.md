---
title: 固定資産の取得の提案
description: このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, LedgerJournalTable, LedgerJournalTransAsset, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b35b13dc266fd5bccde437526400832d394b9aa
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839908"
---
# <a name="propose-fixed-asset-acquisitions"></a>固定資産の取得の提案

[!include [task guide banner](../../includes/task-guide-banner.md)]

このトピックでは、固定資産仕訳帳の取得提案を使用して固定資産を取得する方法について説明します。 これは USMF の法人に対して経理担当ロールとデモ データを使用します。

1. ナビゲーション ペインで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳**に移動します。
2. **新規** を選択します。
3. **名前**フィールドで値を入力または選択します。
4. アクション ペインで、**明細行**を選択します。
5. **提案**を選択します。
6. **取得提案**を選択します。
7. **フィルター**を選択します。 **リセット**を選択すると、前の値をクリアします。
8. **固定資産番号**の行を選択します。
9. **基準**フィールドで、値を入力または選択します。 この提案と一緒に取得したい固定資産の残余基準を設定します。  
10. **OK** を 2 回選択して、ウィンドウを終了します。
- 作成したトランザクション明細行を確認します。  
- 帳簿で設定された取得日付と取得価格が付いている固定資産のみが取得提案に含まれます。  
11. ページで、**帳簿**タブを選択します。
12. **投稿**を選択します。

