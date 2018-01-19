--- 
title: "小売店舗の明細書の作成、計算、および転記"
description: "この手順では、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 42ab631e29a7fae1140acd41ad80c13e55ca1404
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="create-calculate-and-post-a-statement-for-a-retail-store"></a>小売店舗の明細書の作成、計算、および転記

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、店舗の明細書を作成、計算、および転記する手動のステップについて説明します。 同じタスクにコンフィギュレーションできるバッチ ジョブもあります。 他のトピックで、バッチ ジョブをコンフィギュレーションし、実行するための手順を検索できます。 この手順を完了するには、POS で完了して Dynamics AX で取り出されたトランザクションが必要です。 この記録では、デモ データの会社 USRT を使用します。 この手順は、Microsoft Dynamics AX を参照する場合があります。 Dynamics AX は現在 Microsoft Dynamics 365 for Operations と呼ばれていることに注意してください。

1. すべてのワークスペース > .. に移動します > 小売店舗の財務。
2. [新しい明細書] をクリックします。
3. [店舗番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. 一覧で、選択された行のリンクをクリックします。
5. [OK] をクリックします。
    * [設定グループ] には、どのトランザクションを明細書に含めるか、どのように明細行にグループ化するかを制御する設定があります。 [設定グループ] を開き、これらの設定を変更することもできますが、既定値を使用することもできます。  
    * [明細書の方法] フィールドで明細行をグループ化する方法を定義します。  
    * 特定のスタッフ メンバーまたはレジスターの明細書のみ計算する場合、スタッフ メンバーまたはレジスターを選択します。  
6. [決済方法] フィールドで、オプションを選択します。
7. [明細書の計算] をクリックします。
8. [はい] をクリックします。
    * 明細書を計算した後、各支払方法の合計金額と使用された明細書の方法が記された行が作成されます。  
    * 入力、または更新する必要がある場合、各行に計算済金額を入力します。 計算済フィールドには、POS で実行した支払/入金申告の金額が表示されます。  
9. [明細書の転記] をクリックします。
10. [閉じる] をクリックします。
11. [小売りとコマース] > [チャンネル] > [小売店舗の財務] の順に移動します。
12. [転記済明細書] のタブをクリックします。


