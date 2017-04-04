---
title: "マスター プラン"
description: "会社の日常業務をサポートするさまざまなマスタ プランを使用して、監視対象のシミュレーションし、内部パフォーマンスまたは顧客の満足度に関するポリシーなどの会社のポリシーを実施します。各計画の戦略の。"
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 29bb560c11e63938bea73ed8471c27563b546f8f
ms.lasthandoff: 03/31/2017


---

# <a name="master-plans"></a>マスター プラン

会社の日常業務をサポートするさまざまなマスタ プランを使用して、監視対象のシミュレーションし、内部パフォーマンスまたは顧客の満足度に関するポリシーなどの会社のポリシーを実施します。各計画の戦略の。 

**マスター プラン**ページでマスター プランを構成することができます。

プランには次の 2 つのタイプがあります。
-   **静的マスター プラン**: マスター プランの計算では、現在のデータを使用して正味必要量プランが生成されます。 このプランは、次回のマスター プランの実行まで変わりません。 これは、購買担当者や生産計画担当者など、さまざまな従業員が意思決定の基準として使用し、日常業務を遂行するための業務プランです。
-   **動的マスタ プラン**: このプランは、マスター プランによって生成された同じ正味必要量プランで開始されます。 ただし、マスター データが変更されるたびに動的プランを更新できます。 これは、新しい販売注文を作成した場合などです。 これにより、他のユーザーがそれぞれの作業過程で使用している静的マスタ プランには影響を与えずに、注文のネットワークの変化や品目の在庫状態を監視することができます。

会社で動的マスター プランのみを使用する場合もあれば、静的マスター プランと動的マスター プランの両方を使用する場合もあります。 また、特定の戦略の反映や特定の問題への対処を目的として任意のマスタ プランをコンフィギュレーションすることもできます。 例は次のとおりです。
-   欠品を防ぐために在庫レベルの設定を高くする。
-   信頼できない仕入先への対策として安全マージンを長めに設定する。

このほか、マスター プランを実行するたびに新しい必要量プランを使用して更新されるように、初期動的マスター プランを設定することもできます。 **マスター プラン パラメータ**ページでこれらの設定を指定できます。



<a name="see-also"></a>参照
--------

[補充設定](coverage-settings.md)

[マスタ スケジューリングの戦術的な、工程な計画を分割します (http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)]

[マスタ プラン: 空電と動的マスタ プランを使用するか、または一つの計画を使用します。] (https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)


