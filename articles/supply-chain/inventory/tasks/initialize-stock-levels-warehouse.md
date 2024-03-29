---
title: 倉庫の在庫レベルの初期化
description: この手順では、在庫移動仕訳帳を使用して手持在庫を手動で更新する方法を示します。
author: yufeihuang
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 264dabf9c1c10c3d2cee3e0c942abbfa249f21f5
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/29/2021
ms.locfileid: "7565882"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a>倉庫の在庫レベルの初期化

[!include [banner](../../includes/banner.md)]

この手順では、在庫移動仕訳帳を使用して手持在庫を手動で更新する方法を示します。 (データ エンティティのトランザクションをインポートして手持在庫を更新することもできます。) 仕訳帳名、品目の設定、転記プロファイル、勘定などのすべての前提条件が揃っているデモ データの会社 USMF でこのガイドを実行できます。 このガイドでは、使用する品目および分析コードに対して特定の値が提示されます。 別の品目を選択する場合は、別の分析コードの値を入力する必要がある場合があります。

1. [在庫管理] > [仕訳入力] > [品目] > [移動] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
4. [IMov] を選択します。
    * 異なる事業目的ごとに異なる仕訳帳名のテンプレートを使用することをお勧めします。  
5. 一覧で、選択された行のリンクをクリックします。
6. [相手勘定] フィールドに値「140200」を指定します。
    * これは、仕訳帳明細行で既定の勘定となる相手勘定です。 既定値を上書きして、行ごとに異なる相殺勘定を割り当てることができます。  
7. [OK] をクリックします。
8. [新規] をクリックします。
9. [品目番号] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 品目 A0001 を選択します。
11. 一覧で、選択された行のリンクをクリックします。
12. [在庫分析コード] タブをクリックします。
13. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
14. サイト 1 を選択します。
15. [倉庫] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
16. 倉庫 13 を選択します。
17. 一覧で、選択された行のリンクをクリックします。
18. [場所] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
19. 場所 13 を選択します。
20. [数量] フィールドに数値を入力します。
21. [保存] をクリックします。
22. [転記] をクリックします。
23. [すべての転記エラーを新しい仕訳帳に転送] チェック ボックスをオンまたはオフにします。
    * このオプションを有効にすると、転記が失敗する明細行は新しい仕訳帳にコピーされます。 ログにある情報を使用して問題を修正してから明細行を再転記できます。  
24. [OK] をクリックします。
25. ページを閉じます。
26. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]