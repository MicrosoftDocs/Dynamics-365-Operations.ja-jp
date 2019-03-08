---
title: 認識テストの作成および確認
description: 日本では、減損は 2 つの主要なステップにより処理されます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentManageTestResult_JP, AssetImpairmentRecognition_JP
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 752e7d357575eaee681530403e3ee7eeea8f572b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "371099"
---
# <a name="create-and-confirm-recognition-test"></a>認識テストの作成および確認

[!include [task guide banner](../../includes/task-guide-banner.md)]

日本では、減損は 2 つの主要なステップにより処理されます。 最初のステップは、減損が必要かどうかをテストすることです。 2 番目のステップでは、必要に応じて減損金額を計算します。 



このタスクでは、認識テストでの 2 つのステップのプロセスの実行および転記の準備方法について説明します。 



この手順を完了するためには、[固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して作成されました。

1. [固定資産] > [定期処理タスク] > [減損の認識] の順に移動します (方法 I: CGU より大きいグループを使用)。
    * 方法 2 の場合は、[固定資産] > [定期処理タスク] > [減損認識] の順に移動します (方法 II: CGU への共有資産/営業権の帳簿価額の配賦)。  
2. [新規] をクリックします。
3. [CGU グループ] フィールドに値を入力します。
4. [日付] フィールドに日付を入力します。
    * 減損トランザクションを転記する日付を入力します。  
5. [説明] フィールドに値を入力します。
6. [保存] をクリックします。
7. [認識テスト] をクリックします。
8. [テストの実行] をクリックします。
    * 認識テストでは、正味簿価額の合計を各資産グループの値引前キャッシュ フローと比較して、減損額の計算が必要かどうかを決定します。  
9. [計算] をクリックします。
    * テスト結果が「はい」の場合は、認識テストでは正味簿価額から回収可能金額を差し引いて減損の調整金額を決定します。 減損の調整額は転記のため、固定資産ごとに配分されます。  
10. [確認] をクリックします。
    * 確認済の認識テストだけを転記することができます。  
11. [はい] をクリックします。

