---
title: ハードウェア ステーションの作成と関連付け
description: この手順では、新しいハードウェア ステーションを作成する方法を説明します。
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adbd5ef1cafe778cf897aafb05c77fca89be3e20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964923"
---
# <a name="create-and-associate-a-hardware-station"></a>ハードウェア ステーションの作成と関連付け

[!include [banner](../includes/banner.md)]

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
13. Retail および Commerce > チャネル > すべての店舗の順に移動します。
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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]