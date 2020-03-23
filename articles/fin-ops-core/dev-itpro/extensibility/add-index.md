---
title: 拡張機能を使用してテーブルにインデックスを追加
description: このトピックでは、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 03/09/2020
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
ms.openlocfilehash: a93814746d9426417ef402cd1bd339234e668484
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112276"
---
# <a name="add-indexes-to-tables-through-extension"></a>拡張機能を使用してテーブルにインデックスを追加

[!include [banner](../includes/banner.md)]

多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。 したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。 拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。 既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。 新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。

次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。

![新しいインデックス](media/AddIndex.jpg) 

> [!WARNING]
> 固有のインデックスを作成するのに、この手法は用いないでください。 この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。 この機能は、将来のプラットフォーム リリースでは削除されます。
