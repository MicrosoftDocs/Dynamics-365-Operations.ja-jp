---
title: 認識テストの作成および確認
description: 日本では、減損は 2 つの主要なステップにより処理されます。
author: kfend
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: AssetImpairmentManageTestResult_JP, AssetImpairmentRecognition_JP
ms.openlocfilehash: 0115c2ef03d5b26212d690cb222d1b98761bf259
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283798"
---
# <a name="create-and-confirm-recognition-test"></a>認識テストの作成および確認

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
