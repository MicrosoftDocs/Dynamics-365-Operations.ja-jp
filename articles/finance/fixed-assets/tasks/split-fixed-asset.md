---
title: 固定資産の分割
description: このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85ccf187e77faf338ac29452d823c3652b806a21
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138118"
---
# <a name="split-a-fixed-asset"></a>固定資産の分割

[!include [banner](../../includes/banner.md)]

このトピックでは、1 つの資産帳簿を、新しい資産帳簿に分割する方法について説明します。 これは、経理担当ロールと USMF デモ データを使用します。


## <a name="create-a-new-fixed-asset"></a>新しい固定資産の作成
1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 固定資産 > 固定資産**の順に移動します。
2. **新規** を選択します。
3. **固定資産グループ** フィールドで、値を入力または選択します。 分割処理で使用する固定資産番号を確認します。  
4. **名前**フィールドに値を入力します。
5. フォームを閉じます。

## <a name="split-a-fixed-asset"></a>固定資産の分割
1. 一覧で、分割する固定資産のリンクを選択します。
2. **帳簿**を選択します。 新しい資産に分割する帳簿を選択します。  
3. **機能**を選択します。
4. **固定資産の分割**を選択します。
5. **分割先固定資産**フィールドで、値を入力または選択します。
6. **次の帳簿まで**フィールドで、ドロップダウン ボタンをクリックし、ルックアップを開きます。
7. **トランザクション日付**フィールドに、日付を入力します。
8. **割合**フィールドに数を入力します。
9. **仕訳帳名**フィールドで、値を入力または選択します。
10. **OK** を選択します。

## <a name="post-the-journal-transaction"></a>仕訳帳トランザクションの転記
1. ナビゲーション ウィンドウで、**モジュール > 固定資産 > 仕訳入力 > 固定資産仕訳帳**に移動します。
2. リストで、分割処理で作成された仕訳帳を選択します。
3. **明細行** を選択します。

    - 作成した仕訳帳明細行を確認します。  
    - 取得原価調整トランザクションは、指定した割合で分割処理中に元の資産の価値を減らすために作成されます。  
    - 取得トランザクションは、新しい資産に対して同じ金額で作成されます。  

4. **投稿**を選択します。

