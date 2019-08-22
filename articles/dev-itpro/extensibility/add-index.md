---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 01d8f3c7ff1b8bcc666d1e85f16c2bb4ad535d48
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/30/2019
ms.locfileid: "1794866"
---
# <a name="add-indexes-to-tables-through-extension"></a>拡張機能を使用してテーブルにインデックスを追加

[!include [banner](../includes/banner.md)]

多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。 したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。 拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。 既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。 新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。

次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> 固有のインデックスを作成するのに、この手法は用いないでください。 この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。 この機能は、将来のプラットフォーム リリースでは削除されます。

## <a name="extend-standard-indexes"></a>標準インデックスの拡張

標準インデックスを拡張して追加の (含まれる) 列を追加できますが、これにはいくつか条件があります:

+   インデックスが非クラスター化されています。
+   インデックスが一意ではありません。

標準インデックスの拡張には、次の制約が適用されます:

+   既存の列を削除できません。
+ 既存の列の順序を変更できません。
+   標準インデックスを無効化できません。
