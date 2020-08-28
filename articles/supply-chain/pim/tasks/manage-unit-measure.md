---
title: 測定単位の管理
description: この手順は、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の変換ルールの定義方法を示します。
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8b432e1ec8a26b54574c417e618ded694b19556
ms.sourcegitcommit: 59a9e840989bc9f2c7004efa3499b69c09a91b06
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677883"
---
# <a name="manage-unit-of-measure"></a>測定単位の管理

[!include [banner](../../includes/banner.md)]

この手順は、測定単位の定義方法、単位の翻訳の提供方法とその説明、および関連する単位の変換ルールの定義方法を示します。 デモ データまたは独自のデータを使用して、この手順を確認できます。

1. **ナビゲーション ウィンドウ > モジュール > 製品情報管理 > リリース済製品の保守**の順に移動します。
2. **単位**をクリックします。

## <a name="create-a-unit-of-measure"></a>測定単位の作成
1. **新規** をクリックします。
2. **単位**フィールドに値を入力します。 測定単位を参照するときに使用する ID または記号を入力します。  
3. **説明**フィールドで、値を入力します。 システム言語で測定単位の内容を示す名前を入力します。  
4. **単位クラス** フィールドで、オプションを選択します。 単位クラスは、測定単位が含まれる、領域、質量、または数量などの論理グループを定義します。  
5. **小数点以下の精度**フィールドに数値を入力します。 測定単位に対する計算を完了する場合、変換後の測定単位を丸める必要があるときの小数点以下の桁数を指定します。  
6. **保存**をクリックします。

## <a name="define-unit-translations"></a>単位の変換の定義
1. **アクション ウィンドウ** で **単位のテキスト** をクリックします。
2. **新規** をクリックします。 顧客または仕入先の固有言語で外部ドキュメントに使用する測定単位を表す ID または記号の翻訳を作成するには、単位テキストを使用します。  
3. **言語**フィールドで値を入力または選択します。
4. **テキスト** フィールドに値を入力します。
5. **保存**をクリックします。
6. ページを閉じます。
7. **アクション ウィンドウ** で **翻訳済単位の説明**をクリックします。
8. **新規** をクリックします。 測定単位に言語固有の説明を定義します。  
9. **言語**フィールドで値を入力または選択します。
10. **説明**フィールドで、値を入力します。
11. **保存**をクリックします。
12. ページを閉じます。

## <a name="define-unit-conversion-rules"></a>単位換算ルールの定義
1. **アクション ウィンドウ**で**単位の換算**をクリックします。 選択された単位クラスでの、他の測定単位への（からの）測定単位の変換に関するルールを定義します。  
2. **新規**をクリックすると、ドロップ ダイアログが開きます。
3. **係数**フィールドに数値を入力します。 [開始単位] から [終了単位] を導くための換算率。 たとえば、センチメートルからメートルへの換算率は 100 になります (100 センチメートル = 1 メートル)。  
4. **終了単位**フィールドで値を入力または選択します。
5. **丸め**フィールドで、オプションを選択します。 変換された値の丸め方法を定義します。  
6. **OK**をクリックします。
7. ページを閉じます。

