---
title: 拡張可能なテーブルの書き込み
description: このトピックでは、拡張可能テーブルを書き込む方法について説明します。
author: MichaelFruergaardPontoppidan
manager: AnnBe
ms.date: 09/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 268724
ms.assetid: ''
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2018-09-09
ms.dyn365.ops.version: Platform update 20
ms.openlocfilehash: d0bcce9ada0da548df3f43f2a26c825d8d4574d7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408845"
---
# <a name="write-extensible-tables"></a>拡張可能なテーブルの書き込み
[!include [banner](../includes/banner.md)]

テーブルには、拡張担当者がフィールド、フィールド グループ、インデックス、関係、メソッドなどを追加できる豊富な拡張モデルがあります。

## <a name="unique-indexes"></a>一意のインデックス
拡張により固有のインデックスを変更することはできません。 固有のインデックスは、テーブルの制約を定義し、多くの場合、テーブルにおける行のキーも定義します。 このような変更はテーブルの内容を変更するため、固有のインデックスを変更することは許可されていません。 したがって、テーブルを定義するソリューションの将来のバージョン、またはテーブルを消費する他のソリューションと論理競合が発生する可能性が高くなります。

現在または将来、変更されると考えられる固有のインデックスを避けてください。 たとえば、色、サイズ、スタイル、およびコンフィギュレーションなど、製品分析コードに固有のインデックスを作成しないでください。 代わりに、新しい製品分析コードが追加された場合にインデックスを変更しなくてもかまわないように、特徴的製品バリアントに固有のインデックスを作成します。

複数の列で拡張可能な一意制約を必要とする場合、列の値のハッシュを作成することを検討します。 例については、NumberSequenceScope テーブルを参照してください。

## <a name="data-events"></a>データ イベント
テーブルには、自動的に発生する多くの事前定義データ イベントがあります。

**doInsert()**、**doUpdate()**、**doDelete()** の呼び出しを回避してください。 これらのメソッドは、データ イベントが発生することを防ぎ、テーブルの拡張が困難になります。 代わりに、**insert()**、**update()**、**delete()** を呼び出してください。

## <a name="field-groups"></a>フィールド グループ
必ず、関連するフィールドをグループ化するため、フォームおよびレポートを構築するために、フィールド グループを使用します。 一貫してこの方法を使用することで、フィールド グループを拡張することによって、追加フィールドをフォームやレポートに表示する拡張を有効にします。


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]