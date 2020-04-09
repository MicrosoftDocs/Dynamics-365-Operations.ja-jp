---
title: 資産グループへの共有資産とのれんの帳簿価額の配賦
description: この手順では、各資産グループへの共有資産と営業権の帳簿価額の配賦について説明します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetImpairmentSharedAssetAlloc_JP, AssetImpairmentPopulateAllocation_JP
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dc3dd74db70ba239c3c8d20ceb271e25c38673b8
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138387"
---
# <a name="allocate-carrying-amount-of-shared-asset-and-goodwill-to-cash-generating-units"></a>資産グループへの共有資産とのれんの帳簿価額の配賦

[!include [banner](../../includes/banner.md)]

この手順では、各資産グループへの共有資産と営業権の帳簿価額の配賦について説明します。 配賦は CGU グループを有効化する前に行う必要があります。



日本では、共有資産とのれんの減損会計に、次の 2 つの方法が許可されています。 

方法 1: キャッシュ生成単位 (CGU) より大きい単位を対象にする。 

方法 2: 共有資産 / 営業権の帳簿価額を CGU に配賦する。 

この手順は、方法 2 を使用した CGU グループにのみ適用されます。 



この手順を完了する前に [固定資産コンフィギュレーション キー] を選択する必要があります。



この手順は、デモ データ会社 JPMF を使用して完成されました。



1. [固定資産] > [設定] > [減損] > [共有資産と営業権の正味簿価額の配賦] の順に移動します。
    * 営業権および共有資産の配賦は方法 2 を用いた CGU グループにのみ適用され、また配賦は CGU グループを有効化する前に行う必要があります。  
2. [割合] フィールドに数値を入力します。
3. 次の資産グループの選択
4. [割合] フィールドに数値を入力します。
5. [配賦の設定] をクリックします。
    * 前のステップを繰り返して個別に比率をコンフィギュレーションすることもできます。  
6. 一覧で、すべての行のマークを設定または解除します。
7. [OK] をクリックします。

