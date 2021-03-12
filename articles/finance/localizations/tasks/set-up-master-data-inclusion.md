---
title: 複数の転記階層の損金算入額のマスター データの設定
description: この手順では、固定資産ルールと、複数の転記階層の損金算入額に必要なマスター データの作成について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetAdvancedRule_JP, AssetAdvancedRuleCreateEdit_JP,  AssetBookTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 25b6fca9c59cf2489feb3ab27fbfb2453e9ff571
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988117"
---
# <a name="set-up-master-data-for-inclusion-of-deductible-expenses-for-multiple-posting-layers"></a>複数の転記階層の損金算入額のマスター データの設定

[!include [banner](../../includes/banner.md)]

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

