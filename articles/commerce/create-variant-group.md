---
title: バリアント グループの作成
description: このトピックでは、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e19d9a2549fa9957126592f3db7e468147997261
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965154"
---
# <a name="create-a-variant-group"></a>バリアント グループの作成


[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce は、製品に対して複数のバリアントをサポートしています。 異なる製品カテゴリに対してさまざまなバリアント グループを設定するのが最適です。 たとえば、XS、S、M、L、および XL サイズの T シャツに対してサイズ グループを作成したり、使用可能なすべての製品の色を含むようにカラー グループを作成したりすることができます。 製品を追加する前に、バリアント グループを追加する必要があります。

このトピックでは、サイズ グループを作成し、コンフィギュレーションします。 同じような手順を使用して、スタイル グループおよびカラー グループの追加およびコンフィギュレーションをすることができます。

## <a name="create-a-size-group"></a>サイズ グループの作成

サイズ グループを作成するには、次の手順に従います。
 
1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> バリアント グループ \> サイズ グループ** の順に移動します。
1. アクション ウィンドウで、**新規** を選択します。
1. **サイズ グループ** ボックスで、サイズ グループの名前を入力します。
1. **説明** ボックスに、適切な説明を入力します。
1. アクション ウィンドウで、**保存** を選択します。

## <a name="add-attributes-to-the-size-group"></a>サイズ グループへの属性の追加

サイズ グループに属性を追加するには、次の手順に従います。

1. ナビゲーション ウィンドウで、**モジュール \> Retail と Commerce \> 製品とカテゴリ \> バリアント グループ \> サイズ グループ** の順に移動
1. ナビゲーション ウィンドウで、サイズ グループを選択します。
1. **サイズ グループ明細行** の下で、**追加** を選択します。
1. **サイズ** ボックスで、サイズを表す文字列を入力します (たとえば、「XL」)。
1. **サイズ名** ボックスで、サイズの名前を入力します (たとえば、「特大」)。
1. **補充重量** ボックスに、補充重量を表す番号を入力します。
1. **バーコードの番号** ボックスに、バーコードを表す番号を入力します。
1. **表示順序** ボックスに、表示順序を表す番号を入力します。
1. サイズの追加が完了したら、アクション ウィンドウの **保存** を選択します。

次の図は、「カジュアル シャツのサイズ」のサイズ グループの例を示しています。

![サイズ グループの作成](media/create-variant-group.png)

## <a name="additional-resources"></a>追加リソース

[製品情報の概要](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[小売製品の設定](set-up-retail-products.md)

[製品分析コード](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
