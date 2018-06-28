---
title: "テーブルの既存のフィールドの変更"
description: "このトピックでは、テーブル内の既存のフィールドを変更する方法について説明します。"
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: 
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: 73d4b465c15adb768c14e37d0023c99d1841ce8d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="modify-an-existing-field-in-a-table"></a>テーブルの既存のフィールドの変更

[!include [banner](../includes/banner.md)]

テーブル内の既存のフィールドのプロパティを変更するには、まずテーブルの拡張を作成する必要があります。 次のプロパティを変更することができます。

- **ラベル**
- **ヘルプ テキスト**
- **国地域コード**
- **拡張データ型** - 現在選択されている EDT から派生した拡張データ型 (EDT) のみを選択できます。 プロパティ シートのルックアップはフィルタリングされ、それらの EDT のみが表示されます。 たとえば、InventTable テーブルの**重量**フィールドで EDT を編集するには、**BOMMeasureWidth** に基づく派生した EDT を作成できます。次に、**InventTable** 拡張子の**重量**フィールドで、**拡張データ型**プロパティを変更します。 この方法で、新しいパッケージが配置されるときに、ユーザー インターフェイスで**幅**フィールドの外観を変更できます。

![既存のフィールドの変更](media/modify-table-property.jpg) 

