---
title: 資産表示
description: このトピックでは、資産管理の資産表示について説明します。
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectTree, EntAssetFunctionalLocationTree
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0256cc86dc306c8addb37d2c8f335470b19177a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5019407"
---
# <a name="asset-view"></a>資産表示

[!include [banner](../../includes/banner.md)]

 

このトピックでは、資産管理の資産表示について説明します。 **資産表示** ページには、ツリー ビューに有効な資産と機能的な場所が表示されます。 したがって、機能的な場所への資産関係の概要を簡単に取得できます。 さらに、機能的な場所、資産、および関連する部品表 (BOMs) に関する詳細情報を表示できます。 また、資産に関連する有効なメンテナンス要求とワーク オーダーの概要をすばやく取得することもできます。

1. **資産管理** \> **共通** \> **資産** \> **資産表示** を選択します。
2. ページに表示されるビューを変更するには、**表示** フィールドで新しい値を選択します。

    > [!NOTE]
    > **資産表示** ページを開いたときに表示される既定のビューは、**資産管理パラメーター** ページの **資産** タブの **表示** フィールドで選択した値によって異なります。 (**資産管理** \> **設定** \> **資産管理パラメーター**)。

ページの右側に、クイック タブは選択したビューの詳細を表示します。

ツリー ビューの上に表示される階層リンク軌跡には、ツリー ビューで現在選択されているものが表示されます。 この階層リンク証跡は、次の形式を使用します。

機能的な場所 ID / 機能的な場所 ID (複数の機能的な場所がある場合) \> 資産 ID / 資産 ID (複数の資産がある場合) - 品目番号。

ツリー ビューで資産を選択した場合は、**有効な要求** または **有効なワーク オーダー** を選択して、資産に関連するメンテンナンス要求またはワーク オーダーを表示できます。 **開く** \> **機能的な場所**、**資産**、または **資産 BOM** を選択して、関連ビューを開くこともできます。

**表示** フィールドで選択できる **資産の機能的な場所** オプションは、資産を選択できる任意の資産ルックアップでも使用できます。 たとえば、[資産の作成](../objects/create-an-object.md)、メンテナンス要求の作成、ワーク オーダーの作成など、ツリー ビューが **資産表示** タブに表示されます。
