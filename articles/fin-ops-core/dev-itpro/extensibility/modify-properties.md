---
title: 拡張機能を使用して、テーブルのプロパティを変更する
description: このトピックでは、拡張機能を使用してテーブルのプロパティを変更する方法について説明します。
author: ivanv-microsoft
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 825563ebf7d1ea7f5f389d3533687c801ed0c7d6
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865874"
---
# <a name="modify-table-properties-through-extension"></a>拡張機能を使用して、テーブルのプロパティを変更する

[!include [banner](../includes/banner.md)]

テーブルのプロパティを変更するには、そのテーブルの拡張を作成する必要があります。 アプリケーション エクスプローラーで、テーブルを右クリックしてから **拡張機能を作成** を選択します。 次の図に示すとおり、新しいテーブル拡張機能は、選択したプロジェクトに作成されます。

![テーブル拡張子の作成](media/ModifyPropertiesOnTable.jpg) 

プロパティ シートで、次のプロパティを変更することができるようになりました。

+ 作成者
+ 作成日時
+ 修正者
+ 変更日時
+ 国地域コード

**作成者**、**作成日時**、**更新者**、または **変更日時** プロパティを **はい** に設定することにより、対応するフィールドがテーブルに追加されることを保証します。 レコードが作成または更新されると、ユーザーに関する、対応する追跡情報がテーブルに格納されます。 ベース テーブルで **はい** に設定されている場合、これらのプロパティを **いいえ** に設定することはできません。

国または地域コードを一覧に追加することにより、システムが指定された国または地域のコンテキストで実行されているときに、対応するテーブルが適用されることを保証できます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]