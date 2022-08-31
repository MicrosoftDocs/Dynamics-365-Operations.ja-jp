---
title: 拡張機能によって、フォームにデータ ソースを追加
description: この記事では、拡張機能を使用して、既存のフォームに新しいデータ ソースを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: Platform update 4
ms.custom: 268724
ms.assetid: ''
ms.openlocfilehash: c37a3d7c60c6d03c80207d27614d432e0f7ec613
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270995"
---
# <a name="add-data-sources-to-forms-through-extension"></a>拡張機能によって、フォームにデータ ソースを追加

[!include [banner](../includes/banner.md)]

多くの場合、既存のテーブルに保管されている情報は、顧客の要求を満たしていません。 したがって、追加のテーブルを作成し、それらのテーブルのデータをページに表示する必要があります。

拡張機能を介して既存のフォームに新しいデータ ソースを追加することができます。 以下の手順を実行します。

1. 拡張モデルでは、選択したフォームにフォームの拡張機能を作成します。
1. フォーム拡張を右クリックし、**新しいデータ ソース** を選択します。

    ![フォーム データ ソースを追加します。](media/AddFormDataSource01.jpg)

1. **テーブル** プロパティと、データ ソースのその他のプロパティを指定します。 たとえば、データ ソースが、フォームの他のデータ ソースにリンクする方法を定義します。 
1. 次の図に示すように、フィールドを新しいデータ ソースからフォーム デザインにドラッグします。

    ![データ ソースからフォーム デザインへフィールドを追加します。](media/AddFormDataSource02.jpg)

1. 同様の方法で、既存のデータ ソースからフィールドを追加できます。 たとえば、次の図に示すように、フォームの背後にあるテーブルは、追加のフィールドで拡張された可能性があります。

    ![追加のフィールドを持つデータ ソース。](media/AddFormDataSource03.jpg)

    > [!TIP]
    > フォーム拡張データ ソースを右クリックしてから、**復元** を選択し、新しいフィールドがリストに表示されるようにする場合があります。

1. 次の図に示されるように、これらの新しいフィールドおよびテーブル内でデータを表示して編集できるようになりました。

    ![新しいフィールド。](media/AddFormDataSource04.jpg)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
