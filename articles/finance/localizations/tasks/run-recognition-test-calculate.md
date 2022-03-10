---
title: 認識テストの実行と個別資産の減損損失の計算
description: このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetImpairmentRecognitionTest_JP, SysQueryForm, AssetImpairmentCreateTest_JP, AssetImpairmentRecognitionTestResult_JP
audience: Application User
ms.reviewer: kfend
ms.search.region: Japan
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8b5fb158d8e56f7263be9892c079d025fe763a7c707f285762286d66ed8f6f8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742842"
---
# <a name="run-the-recognition-test-and-calculate-the-impairment-amount-on-individual-assets"></a>認識テストの実行と個別資産の減損損失の計算

[!include [banner](../../includes/banner.md)]

このタスクは、認識テストの実行方法および個々の資産の減損金額の計算方法について説明します。



このタスクを完了するには、個々の資産の減損インジケーターを管理しておく必要があります。



このタスクは デモ データ会社 JPMF を使用して作成されました。


## <a name="impairment-recognition-test"></a>減損認識テスト
1. [固定資産] > [定期処理タスク] > [個別資産の減損] > [減損認識テスト] の順に移動します。
2. [クエリ] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、[固定資産グループ] 行を選択します。  
4. [基準] フィールドに値を入力します。
    * 例: TOOL-M  
5. [OK] をクリックします。
    * 減損インジケーターを構成済の、3つの固定資産が表示されることを確認します。  
    * TOOLM-000006 に減損損失調整はありませんが、TOOLM-000007 および TOOLM-000008 の減損損失調整はそれぞれ -1,750,000.00 と -2,250,000.00 です。  
6. [減損の保存] をクリックして、ドロップ ダイアログを開きます。
7. [説明] フィールドに値を入力します。
8. [日付] フィールドに日付を入力します。
9. [OK] をクリックします。
    * 減損固定資産の確認フォームが表示されます。  
    * [減損テスト ID] は有効です。     後に [提案と転記] で使用するため、[減損テスト ID] を忘れないでください。   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]