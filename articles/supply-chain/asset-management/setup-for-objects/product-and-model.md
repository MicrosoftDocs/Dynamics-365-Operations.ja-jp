---
title: 資産メーカーとモデル
description: この記事では、資産管理で資産メーカーと関連モデルを設定する方法について説明します。
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetProductLookup, EntAssetModelLookup, EntAssetProduct
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b00cb62926f3a482ec655235b6e2f5880edbcd04
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016278"
---
# <a name="asset-manufacturers-and-models"></a>資産メーカーとモデル

[!include [banner](../../includes/banner.md)]

 

この記事では、資産管理で資産メーカーと関連モデルを設定する方法について説明します。 モデルは、資産タイプに関連付けることができます。

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

1. **資産管理** \> **_資産_* \> **すべての資産** を選択します。
2. **資産** 列で、資産のリンクを選択します。 **詳細** ページが表示されます。
3. **編集** を選択します。
4. **一般** クイック タブで、**メーカー** および **モデル** フィールドの値を選択します。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]