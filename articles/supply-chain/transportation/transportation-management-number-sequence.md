---
title: 輸送管理番号順序
description: このトピックでは、輸送管理用の番号順序の設定方法について説明します。
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2c3f087ac76412cd2dce93dcb31b796ce2cb3bc4
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/29/2020
ms.locfileid: "4432427"
---
# <a name="transportation-management-number-sequence"></a>輸送管理番号順序

[!include [banner](../includes/banner.md)]

さまざまな製品番号を設定するには、輸送管理モジュールの **番号順序** ページを使用します。 製品番号は、配送業者が各出荷の進行状況を整理および追跡するために使用します。

## <a name="create-a-number-sequence-for-a-pro-number"></a>製品番号の番号順序の作成

製品番号の番号順序を作成するには、次の操作を行います。

1. **輸送管理 \> 設定 \> 配送業者 \> 番号順序** に移動します。
1. **新規作成** を選択して、新しい番号順序を作成します。
1. 番号順序のための固有 ID および説明のついた名前を入力します。
1. **番号順序タイプ** フィールドでは、*製品番号* のみ選択できます。
1. **チェック ディジット** フィールドでは、*チェック ディジット* が唯一のオプションであり、汎用エンジンとして設定されています。
1. **シーケンス** クイックタブに、順序に関する情報を入力します。
1. ページを閉じます。

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a>出荷配送業者への番号順序のリンク

配送業者に番号順序をリンクするには、次の操作を行います。

1. **輸送管理 \> 設定 \> 配送業者 \> 出荷の配送業者** に移動します。
1. 出荷配送業者を選択します。
1. **編集** を選択します。
1. **概要** クイックタブで、**製品番号順序** フィールドのオプションを選択します。
1. ページを閉じます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]