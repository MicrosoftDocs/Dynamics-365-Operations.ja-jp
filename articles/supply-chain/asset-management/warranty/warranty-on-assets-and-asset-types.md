---
title: 資産および資産タイプに対する保証
description: この記事では、資産管理で資産および資産タイプの保証を設定する方法について説明します。
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fa4fe7af46996e8de76ea61d5395327e7617e736
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906127"
---
# <a name="warranties-on-assets-and-asset-types"></a>資産および資産タイプに対する保証

[!include [banner](../../includes/banner.md)]

 


この記事では、資産管理で資産および資産タイプの保証を設定する方法について説明します。

## <a name="set-up-a-warranty-on-an-asset-type"></a>資産タイプに対する保証の設定

1. **資産管理** \> **設定** \> **資産タイプ** \> **資産タイプ** を選択します。
2. 左ウィンドウで、仕入先保証契約を関連付ける資産タイプを選択し、**資産タイプの既定値** を選択します。
3. **一般** クイックタブの、**仕入先保証** フィールドで、契約を選択します。

## <a name="set-up-a-warranty-on-an-asset"></a>資産に対する保証の設定

1. **資産管理** \> **共通** \> **資産** \> **全資産** を選択します。
2. 資産を選択し、**編集** を選択します。
3. **仕入先** クイック タブ、**仕入先保証** セクションの **保証** フィールドで、保証契約を選択します。
4. **保証開始日** と **保証終了日** フィールドで、開始日と終了日を選択します。

    > [!IMPORTANT]
    > ワーク オーダーの **保証開始日** フィールドで日付が選択されている場合、保証はその日付のワーク オーダーに対して有効になります。 ワーク オーダーを作成すると、**保証開始日** フィールドは自動的に作成日に設定されます。 ただし、この日付は、保証契約の開始日などに変更することができます。
    >
    > ![ワーク オーダー ページ。](media/02-warranty.png)

> [!NOTE]
> 仕入先保証の対象となる資産のワーク オーダーを作成する場合、そのワーク オーダーの期間中に予定された開始日があると、保証契約に関する通知が表示されます。 その後、必要に応じて、ワーク オーダーをキャンセルできます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]