---
title: 拡張機能を使用して、テーブルのプロパティを変更する
description: このトピックでは、拡張機能を使用してテーブルのプロパティを変更する方法について説明します。
author: ivanv-microsoft
ms.date: 08/20/2021
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 81d81e09305faf3ba69176394830dafd159499bd
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781296"
---
# <a name="modify-table-properties-through-extension"></a>拡張機能を使用して、テーブルのプロパティを変更する

[!include [banner](../includes/banner.md)]

テーブルのプロパティを変更するには、そのテーブルの拡張を作成する必要があります。 アプリケーション エクスプローラーで、テーブルを右クリックしてから **拡張機能を作成** を選択します。 次の図に示すとおり、新しいテーブル拡張機能は、選択したプロジェクトに作成されます。

![テーブル拡張子を作成します。](media/ModifyPropertiesOnTable.jpg) 

プロパティ シートで、次のプロパティを変更することができるようになりました。

+ 国地域コード
+ 作成者
+ 作成日時
+ フォーム参照
+ 変更者
+ 変更日時
+ プレビュー パート参照
+ タグ
+ タイトル フィールド 1
+ タイトル フィールド 2

**作成者**、**作成日時**、**更新者**、または **変更日時** プロパティを **はい** に設定することにより、対応するフィールドがテーブルに追加されることを保証します。 レコードが作成または更新されると、ユーザーに関する、対応する追跡情報がテーブルに格納されます。 ベース テーブルで **はい** に設定されている場合、これらのプロパティを **いいえ** に設定することはできません。

国または地域コードを一覧に追加することにより、システムが指定された国または地域のコンテキストで実行されているときに、対応するテーブルが適用されることを保証できます。

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
