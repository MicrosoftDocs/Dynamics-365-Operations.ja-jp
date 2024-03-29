---
title: 付帯サービス請求金額としての燃料インデックスの配送業者への関連付け
description: このガイドでは、付帯サービスの割り当て、配送業者付帯サービス請求金額、燃料割増金の付帯サービス マスターの作成方法、および配送業者の燃料インデックスの配送業者への割り当て方法を示します。
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2df77fe94156e2b60b77fa1c995ea10eab048a0
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8670555"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>付帯サービス請求金額としての燃料インデックスの配送業者への関連付け

[!include [banner](../../includes/banner.md)]

このガイドでは、付帯サービスの割り当て、配送業者付帯サービス請求金額、燃料割増金の付帯サービス マスターの作成方法、および配送業者の燃料インデックスの配送業者への割り当て方法を示します。 このガイドを実行する前に、配送業者の燃料インデックスを設定する必要があります。 これを行うには、"配送業者の燃料インデックスの設定" ガイドを使用できます。 これらの設定タスクは、通常、物流マネージャーが実行します。 この手順の作成に使用されたデモ データの会社は、USMF です。


## <a name="create-an-accessorial-master"></a>付帯サービス マスターの作成
1. [輸送管理] > [設定] > [評価] > [付帯サービス マスター] に移動します。
2. [新規] をクリックします。
3. [配送付帯サービス マスター] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [保存] をクリックします。

## <a name="create-a-carrier-accessorial-charge"></a>配送業者付帯サービス請求金額の作成
1. [輸送管理] > [設定] > [評価] > [輸送業者の付帯サービス請求金額] に移動します。
2. [新規] をクリックします。
3. [配送付帯サービス ID] フィールドに値を入力します。
4. [出荷の配送業者] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、トラックの配送業者を選択します。  
6. 一覧で、選択された行のリンクをクリックします。
7. [配送サービス] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
8. 一覧で、選択された行のリンクをクリックします。
9. [配送付帯サービス マスター] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
10. 一覧で、目的のレコードを見つけ、選択します。
    * この例では、新しく作成された配送付帯サービス マスターを選択します。  
11. [保存] をクリックします。

## <a name="create-an-accessorial-assignment"></a>付帯サービス割り当ての作成
1. [付帯サービス割り当て] をクリックします。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [基準] セクションの展開を切り替えます。
    * 基準では、燃料割増金を常に適用できます。また、この例の場合には、特定の地域内でのみ適用することができます。  
5. [発送元郵便番号] フィールドに値を入力します。
6. [配送先郵便番号] フィールドに値を入力します。
7. [計算] セクションの展開を切り替えます。
    * 計算セクションでは、燃料割増金の計算方法を指定できます。 この計算は、計算を基準として選択した付帯サービス単位によって異なります。  
8. [付帯サービス手数料タイプ] フィールドで、「燃料割増金」を選択します。
9. [付帯サービス単位] フィールドで、「マイレージ」を選択します。
10. [地域] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
11. 一覧で、選択された行のリンクをクリックします。
12. [保存] をクリックします。

## <a name="update-the-carrier-rating-profile"></a>配送業者の評価プロファイルの更新
1. [輸送管理] > [設定] > [配送業者] > [出荷の配送業者] の順に移動します。
2. 一覧で、目的のレコードを見つけ、選択します。
3. [評価プロファイル] セクションの展開を切り替えます。
4. [編集] をクリックします。
5. [配送業者の燃料インデックス] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、選択された行のリンクをクリックします。
7. [保存] をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]