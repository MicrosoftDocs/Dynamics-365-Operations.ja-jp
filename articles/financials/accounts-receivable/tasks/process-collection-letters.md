--- 
title: "督促状の処理"
description: "この手順では、督促状の作成、印刷、および転記の方法を示します。"
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>督促状の処理

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、督促状の作成、印刷、および転記の方法を示します。 このタスクでは、USMF というデモ会社を使用します。


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>転記プロファイルでの督促状シーケンスの設定
1. [貸方転記および取立] > [設定] > [顧客転記プロファイル] の順に移動します。
2. [編集] をクリックします。
    * ドロップダウン リストから督促状の順序を選択します。 この転記プロファイルを使用するトランザクションで督促状を生成したくないなら、フィールドを空白のままにします。  
    * テーブル制限タブで、督促状の処理方法を変更することができます。 このフィールドが [はい] に設定されているなら、督促状はこの転記プロファイルに対して作成されます。  
3. ページを閉じます。

## <a name="create-collection-letters"></a>督促状の作成
1. [貸方転記および取立] > [督促状] > [督促状の作成] の順に移動します。
    * レターを収集するトランザクション タイプを選択する必要があります。 これらのタイプのすべての未処理トランザクションがこの計算に含まれます。  
2. [督促状] フィールドで、オプションを選択します。
3. 督促状の日付を入力します。
    * 2 つの転記プロファイルのオプションがあります: [口座] – 各利子計算書の顧客 ID に割り当てられた転記プロファイルを使用します。   選択 – [転記プロファイル] フィールドで選択した転記プロファイルを使用します。  
    * [使用する転記プロファイル] で [選択] に変更した場合、転記プロファイルを選択します。  
4. [対象に含めるレコード] セクションを展開します。
5. [フィルター] をクリックします。
6. [基準] フィールドで、[基準] フィールドで、[顧客 ID] を入力します。 たとえば、「US-001」と入力します。
7. [OK] をクリックします。
8. [OK] をクリックします。

## <a name="print-collection-letters"></a>督促状の印刷
1. [貸方転記および取立] > [督促状] > [督促状の確認と処理] の順に移動します。
2. [ステータス] フィールドで [作成済] を選択します。
3. [印刷済] フィールドで、「印刷せず」を選択します。
4. [印刷] をクリックします。
5. [督促状の注記] をクリックします。
6. [対象に含めるレコード] セクションを展開します。
7. 転記の締日を入力します。
8. 督促状を印刷するために [OK] をクリックします。

## <a name="post-the-collection-letter"></a>督促状の転記
1. [転記] をクリックします。
2. 督促状の転記日付を入力します。
3. [対象に含めるレコード] セクションを展開します。
4. [OK] をクリックします。
5. [ステータス] フィールドで [転記済] を選択します。
6. [印刷済] フィールドで、オプションを選択します。


