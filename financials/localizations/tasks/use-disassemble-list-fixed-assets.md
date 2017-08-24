--- 
title: "固定資産の分解一覧の使用 (日本)"
description: "日本では、固定資産のコンポーネントを在庫に移転できます。"
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: f65bf166a25f3f493c52b06d12b414a1924f86a5
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="use-disassemble-list-for-fixed-assets-japan"></a>固定資産の分解一覧の使用 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

日本では、固定資産のコンポーネントを在庫に移転できます。 



このタスクでは、分解の一覧を使用して固定資産の評価減を行うと同時に、棚卸資産を作成するプロセスを説明します。



このタスクを完了するには、先に「固定資産の組み立て一覧の使用」の作業を完了する必要があります。 



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="enter-the-disassembly-list"></a>分解リストを入力します。
1. [固定資産] > [固定資産] > [固定資産] に移動します。
2. 一覧で、選択された行をマークします。
3. [アクション] ウィンドウで、[固定資産] をクリックします。
4. [コンポーネント] をクリックします。
5. 一覧で、選択された行をマークします。
6. [分解リストに追加] をクリックします。
7. [追加] フィールドに数値を入力します。
8. [OK] をクリックします。
9. [分解リスト] タブをクリックします。
    * レコードが分解の一覧に追加されたことを確認します。  
    * オプション: [追加] をクリックして、分解の一覧に品目を追加することもできます。  
10. [価格の計算] をクリックすると、ドロップ ダイアログが開きます
11. [計算] をクリックします。
    * 原価が更新されていることを確認します。  
    * 市場価値を変更できます。 これは固定資産の評価減の貸方金額として仕訳帳に入力されます。  

## <a name="post-the-disassembly-list"></a>分解リストの転記
1. 次の順に移動します: [固定資産] > > [固定資産仕訳帳]。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [明細行] をクリックします。
5. [日付] フィールドに日付を入力します。
6. [トランザクション タイプ] フィールドで [評価減調整] を選択します。
7. [勘定] フィールドで、任意の値を指定します。
    * 分解の一覧にある貸方金額が、原価として自動的に取得されていることを確認します。  
    * 貸方金額を変更できます。  
8. [転記] をクリックします。


