---
title: バリアント グループの作成
description: この記事では、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。
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
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
ms.openlocfilehash: 507076259c2d9dfe97a0e24d253b5ac0a8325fe2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270103"
---
# <a name="create-a-variant-group"></a>バリアント グループの作成


[!include [banner](includes/banner.md)]

この記事では、Microsoft Dynamics 365 Commerce で製品のサイズ、スタイル、または色バリアント グループを作成する方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce は、製品に対して複数のバリアントをサポートしています。 異なる製品カテゴリに対してさまざまなバリアント グループを設定するのが最適です。 たとえば、XS、S、M、L、および XL サイズの T シャツに対してサイズ グループを作成したり、使用可能なすべての製品の色を含むようにカラー グループを作成したりすることができます。 製品を追加する前に、バリアント グループを追加する必要があります。

この記事では、サイズ グループを作成し、コンフィギュレーションします。 同じような手順を使用して、スタイル グループおよびカラー グループの追加およびコンフィギュレーションをすることができます。

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

![サイズ グループを作成します。](media/Size-Groups.png)

## <a name="additional-resources"></a>追加リソース

[製品情報の概要](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[小売製品の設定](set-up-retail-products.md)

[製品分析コード](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
