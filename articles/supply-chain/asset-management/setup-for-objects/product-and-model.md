---
title: 資産メーカーとモデル
description: このトピックでは、資産管理で資産メーカーと関連モデルを設定する方法について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1eca3112b95bc7d1a049f101fc1d461272a63aa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5022259"
---
# <a name="asset-manufacturers-and-models"></a>資産メーカーとモデル

[!include [banner](../../includes/banner.md)]

 

このトピックでは、資産管理で資産メーカーと関連モデルを設定する方法について説明します。 モデルは、資産タイプに関連付けることができます。

## <a name="set-up-product-model-relations"></a>製品 - モデルの関係を設定

1. **資産管理** \> **設定** \> **資産** \> **メーカーとモデル** を選択します。
2. **新規** を選択して、新しい製品を作成します。
3. **メーカー** フィールドに、資産メーカーの名前を入力します。
4. **説明** フィールドに説明を入力します。
5. **モデル** クイック タブで、**追加** を選択して、資産メーカーに関連する資産モデルを作成します。
6. **モデル** フィールドに、資産モデルの名前を入力します。
7. **説明** フィールドに説明を入力します。
8. **資産タイプ** フィールドで、メーカー モデルが関連する資産タイプを選択します。

    > [!NOTE]
    > **資産タイプ** ルックアップで、資産タイプ、メーカー、およびモデルの関係を設定することもできます。 詳細については、[資産タイプ](../setup-for-objects/object-types.md)を参照してください。

    **詳細** クイック タブ、**モデル** フィールドには、選択した資産メーカーで設定されている資産モデルの数が表示されます。 **資産** フィールドには、選択したメーカーを使用している資産の数が表示されます。
    
    **資産** フィールドには、メーカー モデルを使用しているオブジェクトの数が表示されます。

> [!NOTE]
> 資産タイプは、資産メーカー モデルの関係を持たないことも、1 つの資産メーカー モデルに関連付けることも、複数の資産メーカー モデルに関連付けることもできます。 資産タイプが 1 つのメーカー モデルに関連している場合、**メーカー モデル** ルックアップで設定された組み合わせのみが、資産タイプ、メーカー、およびモデルの組み合わせを設定できる資産管理ページで選択できます。 これらのページには、**全資産**、**資産サービス レベル**、**ジョブ タイプの既定値**、および **メンテナンス予算明細行** が含まれます。 一部の資産タイプがメーカー モデルに関連していない場合、それらの資産タイプ、および資産タイプとは関係のないメーカー モデルのみがページに表示されます。

## <a name="select-a-manufacturer-and-model-on-an-object"></a>オブジェクトのメーカーとモデルを選択

1. **資産管理** \> **共通** \> **資産** \> **全資産** を選択します。
2. **資産** 列で、資産のリンクを選択します。 **詳細** ページが表示されます。
3. **編集** を選択します。
4. **一般** クイック タブで、**メーカー** および **モデル** フィールドの値を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]