---
title: Commerce での新しい製品の作成
description: この記事では、Microsoft Dynamics 365 Commerce に新しい製品を作成する方法について説明します。
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 654ba19b0bc96ab40c8c27106fd819faa85a4ce8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270184"
---
# <a name="create-a-new-product-in-commerce"></a>Commerce での新しい製品の作成


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce に新しい製品を作成する方法について説明します。

## <a name="overview"></a>概要

製品は、主に、製品番号、名前、および説明によって定義されます。 しかし、製品またはサービスを説明するためには、他のデータも必要です:

## <a name="create-a-new-product"></a>新しい製品の作成

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> カテゴリ別製品** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **製品タイプ** ドロップダウン リストで、**品目** または **サービス** のいずれかを選択します。
1. **製品サブタイプ** ドロップ ダウン リストで、**製品** (製品にバリアントが含まれていない場合) または **製品マスター** (製品にバリアントがある場合) を選択します。
1. **製品番号** ボックスで、製品番号を事前に登録していない場合は、製品番号を入力します。
1. **製品名** ボックスに、製品名を入力します。
1. **検索名** ボックスに、検索名を入力します。
1. **小売りカテゴリ** ドロップ ダウン リストで、適切なカテゴリを選択します。
1. 製品がキットの場合は、**製品キット** の **はい** を選択します。
1. 製品サブタイプが製品マスターの場合は、サポートされているバリアントを含めるために **製品分析コードグループ** を設定します。 オプションには、**色**、**サイズ**、**スタイル**、および **構成** が含まれます。 必要に応じて、追加の製品分析コードグループを作成する必要があります。
1. **コンフィギュレーション テクノロジ** ドロップ ダウン リストで、適切なオプションを選択します。
1. **OK** を選択します。

次の図は、製品が追加された例を示しています。

![製品を作成します。](media/create-new-product.png)

製品を追加すると、**製品説明**、**バリアント グループ**、**分析コードグループ**、**製品属性**、**関連製品** などの追加データを設定できます。

次の図は、製品の詳細を示しています。

![製品の詳細。](media/create-new-product-2.png)

### <a name="create-product-variants"></a>製品バリアントの作成

製品サブタイプが **製品マスター** の場合は、特定のバリアントを作成する必要があります。 

製品バリアントを作成するには、次の手順に従います。

1. アクション ウィンドウで、**製品バリアント** を選択します。
1. アクション ウィンドウでバリアント グループが選択されている場合は **バリアントの提案* を選択します。
1. 製品に対してサポートするバリアントを選択します。
1. **作成** を選択します。

## <a name="release-a-product"></a>製品のリリース

製品を販売するには、まず、それを法人にリリースする必要があります。

1. 製品ページで、**リリース製品** を選択します。

    ![リリース製品。](media/create-new-product-3.png)

1. リリースする製品を選択し、**次へ** を選択します。

    ![リリースする製品を選択します。](media/create-new-product-4.png)

1. リリースする製品バリアントのセットを選択し、**次へ** を選択します。

    ![リリースするバリアントを選択します。](media/create-new-product-5.png)

1. 法人を選択し、**次へ** を選択します。

    ![法人を選択します。](media/create-new-product-6.png)

1. **完了** を選択します。

    ![製品リリースを完了します。](media/create-new-product-7.png)

## <a name="configure-a-released-product"></a>リリースされた製品をコンフィギュレーションする

製品がリリースされた後、製品に価格を追加することを含む、追加のコンフィギュレーションが必要になります。

1. ナビゲーション ウィンドウで、**モジュール \> 小売りとコマース \> 製品とカテゴリ \> カテゴリ別リリース済製品** の順に移動します。
1. リリースされた製品の製品カテゴリ ノードを選択し、製品リストから製品を選択します。
1. アクション ウィンドウで、**編集** を選択します。
1. **購買** セクションで、**単位**、**価格**、および **数量** を含む、必要なプロパティをコンフィギュレーションします。
1. アクションウィンドウで、**検証** を選択して、欠落しているフィールドについてエラーが報告されないことを確認します。
1. アクション ウィンドウで、**保存** を選択します。

次の図は、リリースされた製品のコンフィギュレーションの例を示しています。

![リリースされた製品をコンフィギュレーションします。](media/create-new-product-8.png)

## <a name="additional-resources"></a>追加リソース

[法人を作成します](channels-legal-entities.md)

[バリアント グループの作成](create-variant-group.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
