--- 
title: "ハードウェア ステーションの作成"
description: "この手順では、新しいハードウェア ステーションを作成する方法を説明します。"
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
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
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: 3551e37c6aae37c01b5cacff8b908faaf75fb3e2
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="create-hardware-stations"></a>ハードウェア ステーションの作成

[!include [task guide banner](../includes/task-guide-banner.md)]

この手順では、新しいハードウェア ステーションを作成する方法を説明します。 新しいハードウェア プロファイルは、あらかじめ定義された店舗 (チャンネル) に新しいハードウェア ステーションを追加するために作成および使用されます。 この手順では、デモ データの会社 USRT を使用します。

1. Commerce エッセンシャル > チャンネル >.. に移動します > .. > .. > ハードウェア ステーションのプロファイル。
2. [新規] をクリックします。
3. [ハードウェア ステーション ID] フィールドで、「TestHWProfile」を入力します。
4. [名前] フィールドに値を入力します。
5. [ポート番号] フィールドに数を入力します。
6. [ハードウェア プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的のレコードを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [パッケージ名] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、選択された行のリンクをクリックします。
    * これは新しい環境が含まれる標準パッケージです。 バージョン番号が異なる場合があります。  
11. [保存] をクリックします。
12. ページを閉じます。
13. [小売りとコマース] > [チャンネル] > [すべての小売店舗] に移動します。
14. 一覧で行 17 を選択します。
    * デモ データの会社 USRT を使用している場合、ヒューストン店となります。  
15. 一覧で、選択された行のリンクをクリックします。
16. [ハードウェア ステーション] セクションの展開を切り替えます。
17. [追加] をクリックします。
18. 一覧で、選択された行をマークします。
19. [プロファイル ID] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
20. 一覧で、目的のレコードを見つけ、選択します。
    * これは、前の手順で作成した新しいハードウェア ステーションのプロファイルである必要があります。  
21. 一覧で、選択された行のリンクをクリックします。
22. [ホスト名] フィールドに値を入力します。
23. [EFT ターミナル ID] フィールドに値を入力します。
24. [保存] をクリックします。


