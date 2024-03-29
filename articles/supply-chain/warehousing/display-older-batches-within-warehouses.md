---
title: モバイル デバイスで倉庫内の古いバッチの表示を構成する
description: この記事では、作業明細行の現在のロケーションより古いバッチのロケーションのリストを表示するようにモバイル デバイスを設定する方法について説明します。
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5788b42483f2c3046b0d20f45115b98d62cce213
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900538"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a>モバイル デバイスで倉庫内の古いバッチの表示をコンフィギュレーション

[!include [banner](../includes/banner.md)]

**倉庫内の古いバッチの表示** コンフィギュレーションにより、作業明細行の現在の場所よりも古いバッチの場所の一覧を表示できます。 表示される場所のリストには、有効期限のある古いバッチに関する情報と各バッチの現物在庫が含まれています。 新しい場所から選択するか、現在の場所から引き続き選択することができます。 
- 新しい場所からのピッキング - ピッキングする新しい場所を選択すると、現在の作業明細行は新しい場所を使用するように更新され、新しい場所で通常通り作業が続行されます。 新しい場所を有効にするには、作業明細行全体に十分な利用可能な数量がある必要があります。 必要な数量が利用できない場合、作業明細行は更新されず、リストが表示されます。 
- 現在の場所からピッキングを続行 - 現在の作業明細行の場所を続行すると、作業明細行の数量は元の場所から引き続き選択されます。

## <a name="where-it-applies"></a>該当する場所
倉庫内の古いバッチをモバイル デバイス メニュー項目で設定し、アイテムより下のバッチの選択に影響します。

## <a name="set-up-display-older-batches-within-warehouse"></a>倉庫内の古いバッチの表示を設定する
**最も古いバッチのピッキング** オプションを **警告** に設定すると、**倉庫内の古いバッチの表示** コンフィギュレーションはモバイル デバイスのメニュー項目で使用できます。

- **倉庫管理** > **設定** > **モバイル デバイス** > **モバイル デバイスのメニュー項目** の順に、メニュー項目で **既存の作業の使用** を **はい** に設定し、**最も古いバッチのピッキング** フィールドで **警告** を選択します。 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]