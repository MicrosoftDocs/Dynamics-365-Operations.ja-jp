---
title: 計画オーダーの承認
description: このトピックでは、計画最適化でサポートされる計画された注文の承認について説明します。
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983572"
---
# <a name="approve-planned-orders"></a>計画オーダーの承認

[!include [banner](../../includes/banner.md)]

このトピックでは、計画最適化で計画された注文のステータスを更新する方法について説明します。

計画された注文の承認は、計画オーダーから確定された注文を作成する方法としては任意のステップであることに留意してください。 修正済の計画された注文を承認することを推奨します。それ以外の場合は、編集は無視され、次の計画の実行時に上書きされます。

![計画された注文フロー](media/approved-planned-orders-1.png)

**状態** フィールドでは、以下の値を使用して進捗状況を表示します :

- **未処理 :** マスタープ ランンが計画された注文を生成する場合、計画された注文は *未処理* の状態となります。 この状態になっている計画された注文は、次の計画実行時に削除されます。
- **完了 :** 計画された注文を確定しないと判断した場合は、状態を *完了* に変更して、この計画された注文の評価を完了したことを表わします。 *未処理* と *完了* の状態 は、システムによって同じように扱われることに注意してください。
- **承認済 :** 編集を維持する場合や、計画された注文を確定する場合は、*承認済み* に変更してください。 *承認済みの* 状態で計画された注文は、マスタープランで固定され、供給が見込まれているとみなされるため、後のマスタープランの実行中に変更や削除されません。 これを達成するため、計画ロジックはマスター プラン中に、*承認済* 計画オーダーを古い計画バージョンから新しい計画バージョンにコピーします。 ただし、 *承認済* の計画された注文は、特定のマスタープラン内でのみ供給されると見なされます。

計画された注文は、**マスター プラン** ワークスペース、**計画オーダー** リスト、または **計画製造オーダー**、**計画発注書**、**計画移動** リストから管理できます。
