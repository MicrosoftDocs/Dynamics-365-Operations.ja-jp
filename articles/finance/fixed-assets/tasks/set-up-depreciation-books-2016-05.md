---
title: 減価償却簿の設定
description: この手順では、新しい減価償却簿を作成し、それを固定資産グループに関連付けるプロセスを順を追って説明します。
author: moaamer
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 42b8a15ac60fd2620c600d78b84a25e3caf6d2bf
ms.sourcegitcommit: 62ca651c94e61aaa69cfa59e861f263f89d01c4a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/03/2021
ms.locfileid: "7883623"
---
# <a name="set-up-depreciation-books"></a>減価償却簿の設定 

[!include [banner](../../includes/banner.md)]

この手順では、新しい減価償却簿を作成し、それを固定資産グループに関連付けるプロセスを順を追って説明します。 

## <a name="create-a-depreciation-book"></a>減価償却簿の作成
1. [固定資産] > [設定] > [減価償却簿] の順に移動します。
2. [新規] をクリックします。
3. [減価償却簿] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [減価償却の計算] チェック ボックスをオンまたはオフにします。
6. [減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
7. 一覧で、目的の減価償却プロファイルを見つけ、選択します。
8. 一覧で、選択された行のリンクをクリックします。
9. [代替減価償却プロファイル] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、目的の減価償却プロファイルを選択します。
11. 一覧で、選択された行のリンクをクリックします。
    * 特別減価償却プロファイルは、特殊な状況で資産の割増償却に使用されます。 たとえば、自然災害の結果の減価償却を記録する場合などに、このフィールドを使用できます。  
12. [基準調整を含む減価償却調整を作成する] チェック ボックスをオンまたはオフにします。
13. [カレンダー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
14. 一覧で、選択された行のリンクをクリックします。

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a>減価償却簿を固定資産グループに関連付ける
1. [固定資産グループ] をクリックします。
2. [固定資産グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、目的のレコードを見つけ、選択します。
4. 一覧で、選択された行のリンクをクリックします。
5. [減価償却方法] フィールドで、オプションを選択します。
6. [耐用年数] フィールドに数値を入力します。
    * 耐用年数を設定した後に減価償却期間のフィールド値が計算されます。  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
