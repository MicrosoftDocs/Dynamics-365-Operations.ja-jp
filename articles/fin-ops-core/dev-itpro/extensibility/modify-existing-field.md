---
title: 拡張機能を使用したテーブル内の既存のフィールドの変更
description: この記事では、テーブル内の既存のフィールドを変更する方法について説明します。
author: ivanv-microsoft
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.custom: 268724
ms.assetid: ''
ms.openlocfilehash: 707fb3f33015f7f974c9618db7cdd3dd27527c68
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270795"
---
# <a name="modify-existing-fields-in-a-table-through-extension"></a>拡張機能を使用したテーブル内の既存のフィールドの変更

[!include [banner](../includes/banner.md)]

テーブル内の既存のフィールドのプロパティを変更するには、まずテーブルの拡張を作成する必要があります。 次のプロパティを変更することができます。

- **ラベル**
- **ヘルプ テキスト**
- **国地域コード**
- **拡張データ型** - 現在選択されている EDT から派生した拡張データ型 (EDT) のみを選択できます。 プロパティ シートのルックアップはフィルタリングされ、それらの EDT のみが表示されます。 たとえば、InventTable 上のテーブルの **幅** フィールドで EDT を編集する場合は、 **BOMMeasureWidth** を基にして EDT を作成することができます。次に、 **InventTable** 拡張子の **幅** フィールドで、 **拡張データ型** プロパティを変更します。 この方法で、新しいパッケージが配置されるときに、ユーザー インターフェイスで **幅** フィールドの外観を変更できます。

![既存のフィールドを変更します。](media/modify-table-property.jpg) 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
