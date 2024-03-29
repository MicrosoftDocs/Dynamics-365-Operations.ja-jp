---
title: マスター プランの概要
description: 会社の日常業務のサポート、監視を要する多様な計画戦略のシミュレーション、社内の業績や顧客満足に関するポリシーの実装など、さまざまな目的のマスター プランを使用します。
author: t-benebo
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1b3d30d9ef2f08c2cb7b2ca022ff1a816567a247
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2022
ms.locfileid: "8468758"
---
# <a name="master-plans-overview"></a>マスター プランの概要

[!include [banner](../includes/banner.md)]

会社の日常業務のサポート、監視を要する多様な計画戦略のシミュレーション、社内の業績や顧客満足に関するポリシーの実装など、さまざまな目的のマスター プランを使用します。

**マスター プラン** ページでマスター プランを構成することができます。

プランには次の 2 つのタイプがあります。

- **静的マスター プラン**: マスター プランの計算では、現在のデータを使用して正味必要量プランが生成されます。 このプランは、次回のマスター プランを実行するか、手動でプランを変更するまで変わりません。 これは、購買担当者や生産計画担当者など、さまざまな従業員が意思決定の基準として使用し、日々の活動を遂行するための業務プランです。
- **動的マスタ プラン**: このプランは、マスター プランによって生成された同じ正味必要量プランで開始されます。 ただし、マスター データが変更されるたびに動的プランを更新できます。 これは、新しい販売注文を作成した場合などです。 これにより、他のユーザーがそれぞれの作業過程で使用している静的マスタ プランには影響を与えずに、注文のネットワークの変化や品目の在庫状態を監視することができます。

会社で動的マスター プランのみを使用する場合もあれば、静的マスター プランと動的マスター プランの両方を使用する場合もあります。 また、特定の戦略の反映や特定の問題への対処を目的として任意のマスタ プランをコンフィギュレーションすることもできます。 例は次のとおりです。

- 欠品を防ぐために在庫レベルの設定を高くする。
- 信頼できない仕入先への対策として安全マージンを長めに設定する。

このほか、マスター プランを実行するたびに新しい必要量プランを使用して更新されるように、初期動的マスター プランを設定することもできます。 **マスター プラン パラメータ** ページでこれらの設定を指定できます。

## <a name="additional-resources"></a>その他のリソース

- [補充設定](coverage-settings.md)
- [マスター スケジューリングの戦術的な計画と実施計画の分割](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [マスター プラン: 静的および動的マスター プランまたは 1 つの計画のどちらを使用するか。](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
