---
title: 拡張機能によって、フォームにデータ ソースを追加
description: このトピックでは、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
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
ms.openlocfilehash: 9833ff94fe06bd9e467527e276cc431ca16fa644
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866224"
---
# <a name="add-data-sources-to-forms-through-extension"></a>拡張機能によって、フォームにデータ ソースを追加

[!include [banner](../includes/banner.md)]

多くの場合、既存のテーブルに保管されている情報は、顧客の要求を満たしていません。 したがって、追加のテーブルを作成し、それらのテーブルのデータをページに表示する必要があります。

拡張機能を介して既存のフォームに新しいデータ ソースを追加することができます。 以下の手順を実行します。

1. 拡張モデルでは、選択したフォームにフォームの拡張機能を作成します。
1. フォーム拡張を右クリックし、**新しいデータ ソース** を選択します。

    ![フォーム データ ソースの追加](media/AddFormDataSource01.jpg)

1. **テーブル** プロパティと、データ ソースのその他のプロパティを指定します。 たとえば、データ ソースが、フォームの他のデータ ソースにリンクする方法を定義します。 
1. 次の図に示すように、フィールドを新しいデータ ソースからフォーム デザインにドラッグします。

    ![データ ソースからフォーム デザインへのフィールドの追加](media/AddFormDataSource02.jpg)

1. 同様の方法で、既存のデータ ソースからフィールドを追加できます。 たとえば、次の図に示すように、フォームの背後にあるテーブルは、追加のフィールドで拡張された可能性があります。

    ![追加のフィールドを持つデータ ソース](media/AddFormDataSource03.jpg)

    > [!TIP]
    > フォーム拡張データ ソースを右クリックしてから、**復元** を選択し、新しいフィールドがリストに表示されるようにする場合があります。

1. 次の図に示されるように、これらの新しいフィールドおよびテーブル内でデータを表示して編集できるようになりました。

    ![新しいフィールド](media/AddFormDataSource04.jpg)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]