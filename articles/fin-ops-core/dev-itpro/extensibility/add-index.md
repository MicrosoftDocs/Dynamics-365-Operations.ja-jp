---
title: 拡張機能を使用してテーブルにインデックスを追加
description: この記事では、テーブルにインデックスを追加する方法について説明します。
author: ivanv-microsoft
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: josaw
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2017-06-01
ms.dyn365.ops.version: Platform update 4
ms.custom: 268724
ms.assetid: ''
ms.openlocfilehash: 6a0faa07107e3763705bc916aa1b68aa8ae0afc7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9270987"
---
# <a name="add-indexes-to-tables-through-extension"></a>拡張機能を使用してテーブルにインデックスを追加

[!include [banner](../includes/banner.md)]

多くの場合、後で追加データを保管できるようにテーブルを拡張しますが、新しいフィールドの基準となるデータにも素早くアクセスすることができます。 したがって、専用の索引を使用してデータベース検索を高速化すると、多くの場合有益です。 拡張機能を介して既存のテーブルに新しいインデックスを追加することができます。 既存のテーブルにインデックスを追加するには、選択したテーブルを拡張してから、新しいテーブルにインデックスを作成するのと同じようにインデックスを作成します。 新しいインデックスの一部になるように、新しいフィールドおよび既存のフィールドの両方を追加することができます。

次の図では、InventTable の拡張機能を使用して、InventTable テーブルに新しいフィールドのインデックスを定義します。

![新しいインデックス。](media/AddIndex.jpg) 

> [!WARNING]
> 固有のインデックスを作成するのに、この手法は用いないでください。 この変更は、他の独立系ソフトウェア ベンダー (ISV) のソリューションが同じ環境に展開されている場合、そのソリューションを破壊する可能性のある侵入的な変更です。 この機能は、将来のプラットフォーム リリースでは削除されます。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
