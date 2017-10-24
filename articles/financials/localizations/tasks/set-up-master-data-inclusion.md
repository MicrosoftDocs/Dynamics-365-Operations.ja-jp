--- 
title: "複数の転記階層の損金算入額のマスター データの設定 (日本)"
description: "この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: aacd7146dbdf260e11b6d70d5e6c0976132a4452
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-master-data-for-inclusion-of-deductible-expenses-for-multiple-posting-layers-japan"></a>複数の転記階層の損金算入額のマスター データの設定 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。 この手順を完了する前に、 [固定資産コンフィギュレーション キー] を選択する必要があります。 この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="depreciation-settlement-rules"></a>減価償却決済ルール
1. [固定資産] > [設定] > [減価償却決済ルール] の順に移動します。
    * オプション: 決済ルール テーブルが空の場合、既定のルールをインポートするかどうかの確認を求められます。 [OK] をクリックして、既定のルールをインポートします。  
2. [新規] をクリックします。
3. [償却超過額] フィールドで、オプションを選択します。
    * [償却超過額] = [普通償却] を選択します。  
4. [償却不足額] フィールドで、オプションを選択します。
    * [償却不足額] = [割増償却 (準備金)] を選択します。  
5. [OK] をクリックします。
6. [ルール タイプでフィルター] フィールドで、オプションを選択します。
    * [ルール タイプでフィルター] = [償却超過額/償却不足額の繰越] を選択します。  
7. [ルールの編集] をクリックします。
8. [繰越期間 (年)] フィールドに番号を入力します。
    * この例では、 5 を入力します。  
9. [OK] をクリックします。

## <a name="book"></a>予約
1. [固定資産] > [設定] > [帳簿] の順に移動します。
2. [新規] をクリックします。
3. [帳簿] フィールドに値を入力します。
    * この例では、Book = RBです。  
4. [説明] フィールドに値を入力します。
5. [一般] セクションを展開します。
    * コアの固定資産の機能に従ってパラメーターをコンフィギュレーションします。  
6. 取得済み帳簿のセクションを展開します。
7. これを参照する税関連帳簿を選択します。
    * 取得タイプで取得済みの帳簿を追加する場合、税関連帳簿を自動的に取得することによって作業が簡素化されます。  例: NSL_TAX  
8. [保存] をクリックします。
9. クイック フィルターを使用して、レコードを見つけます。 たとえば、「NSL_TAX」の値を含む [帳簿] フィールドでフィルターします。
    * 現在の関連帳簿で精算が実行される税関連帳簿を検索します。  
10. [一般] セクションを展開します。
11. [参照先帳簿] フィールドで、値を入力します。
    * 作成した帳簿を入力します。  
12. [保存] をクリックします。
13. ページを閉じます。


