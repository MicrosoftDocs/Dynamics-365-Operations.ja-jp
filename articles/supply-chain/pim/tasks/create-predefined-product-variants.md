---
title: 事前定義された製品バリアントの作成
description: この手順では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントの作成を説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: baf1e41d0071a4c78d2a0f43548e44ae9d426580
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844780"
---
# <a name="create-predefined-product-variants"></a>事前定義された製品バリアントの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順では、製品分析コードの組み合わせを使用する製品マスターの製品バリアントの作成を説明します。 この手順の作成に使用されるデモ データ会社は USMF です。


## <a name="create-a-product-master"></a>製品マスターの作成
1. [製品情報管理] > [製品] > [製品マスター] の順に移動します。
2. [新規] をクリックします。
3. [製品番号] フィールドに値を入力します。
    * [製品番号] フィールドに番号順序が設定されていない場合は、製品番号の手動入力のみ必須です。 つまり、番号順序がフィールドに設定されている場合、手順を省略します。  
4. [製品名] フィールドに値を入力します。
5. [製品分析コード グループ] フィールドで、値を入力または選択します。
    * 製品分析コード グループ SizeCol (サイズおよび色) を選択します。  
6. [OK] をクリックします。

## <a name="add-product-dimensions"></a>製品分析コードの追加
1. [製品分析コード] をクリックします。
    * この例では、手動で製品分析コードを入力する方法を示します。 使用する製品分析コードの値を含むサイズ、色、またはスタイル グループを選択することもできます。  
2. [新規] をクリックします。
3. 一覧で、選択された行をマークします。
4. [サイズ] フィールドで値を入力または選択します。
5. [名前] フィールドに値を入力します。
6. [新規] をクリックします。
7. 一覧で、選択された行をマークします。
8. [サイズ] フィールドで値を入力または選択します。
9. [名前] フィールドに値を入力します。
10. [色] タブをクリックします。
11. [新規] をクリックします。
12. 一覧で、選択された行をマークします。
13. [色] フィールドで値を入力または選択します。
14. [名前] フィールドに値を入力します。
15. [新規] をクリックします。
16. 一覧で、選択された行をマークします。
17. [色] フィールドで値を入力または選択します。
18. [名前] フィールドに値を入力します。
19. [保存] をクリックします。
20. ページを閉じます。

## <a name="generate-product-variants"></a>製品バリアントの生成
1. [製品バリアント] をクリックします。
2. [バリアント修正候補] をクリックします。
3. [すべて選択] をクリックします。
    * この例では、すべての可能なバリアントが選択されます。 可能な製品分析コードの組み合わせのサブセットのみをバリアントの作成に使用する場合、個々のエントリを選択できます。  
4. [作成] をクリックします。
    * 製品分析コードの値の組み合わせに基づいてすべてのバリアントの説明を生成できます。 説明はオプションです。  
5. [保存] をクリックします。

