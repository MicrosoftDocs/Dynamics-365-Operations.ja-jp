---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 07/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: 7726d1cc6ed061ad9078ef2fc5667daa665ebd2b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537401"
---
# <a name="add-indexes-to-tables-through-extension"></a>拡張機能を使用してテーブルにインデックスを追加

[!include [banner](../includes/banner.md)]

多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。 したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。 拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。 既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。 新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。

> [!NOTE]
> 新しいインデックスを作成することができます。 ただし、既存のインデックスを変更することはできません。

次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> 固有のインデックスを作成するのに、この手法は用いないでください。 この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。 この機能は、将来のプラットフォーム リリースでは削除されます。
