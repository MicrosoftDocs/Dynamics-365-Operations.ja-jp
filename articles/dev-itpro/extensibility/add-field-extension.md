---
title: 拡張機能を使用してテーブルにフィールドを追加
description: このトピックでは、テーブル拡張機能を使用してテーブルにフィールドを追加する方法について説明します。
author: ivanv-microsoft
manager: AnnBe
ms.date: 06/20/2017
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
ms.openlocfilehash: 88a99d87aaea7cd21b0b78197972ab931a510f2c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369163"
---
# <a name="add-fields-to-tables-through-extension"></a>拡張機能を使用してテーブルにフィールドを追加

[!include [banner](../includes/banner.md)]

既存のテーブルに新しいフィールドを追加するには、まずテーブル拡張を作成する必要があります。 たとえば、リリース済製品の半径を持つフィールドを追加するには、次の図に示すように、モデル内で InventTable テーブルの拡張機能を作成する必要があります。

![拡張子の作成](media/TableNewField01.jpg) 

モデル内でフィールドをテーブルに追加するのと同様に、フィールドを拡張機能に追加することができるようになりました。 2 つの方法を使用することができます。

+ デザイナーで、**フィールド** ノードを右クリックし、**新規**を選択してから、追加するフィールドのタイプを選択します。
+ プロジェクトから既存の Extended Data Type または Base Enumeration を**フィールド**ノードにドラッグします。

完了したら、新しいフィールドのプロパティを変更できます。 次の図では、**ラベル** プロパティのみが変更されました。

![新しいフィールドのプロパティの変更](media/TableNewField02.jpg)

必要に応じて、新しいフィールドを既存のフィールド グループのいずれか、または作成する新しいフィールド グループに追加することができるようになりました。 次の図では、**半径**フィールドが **PhysicalDimensions** フィールド グループに追加されました。

![フィールド グループへの新しいフィールドの追加](media/TableNewField03.jpg)

コンパイルとデータベースの同期の後、ユーザー インターフェイスで新しいフィールドを表示および編集することができます。

![ユーザー インターフェイスの新しいフィールド](media/TableNewField04.jpg)
