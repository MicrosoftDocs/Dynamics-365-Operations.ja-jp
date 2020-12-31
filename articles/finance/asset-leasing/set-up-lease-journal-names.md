---
title: リース仕訳帳名の設定
description: このトピックでは、リース仕訳帳の名前を定義する方法について説明します。 リース仕訳帳の名前は、資産リースで発生したエントリが転記される仕訳帳を指定します。
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: e8b1b908dfd6d1d6072b6efa83f13ae5784c85c1
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445377"
---
# <a name="set-up-lease-journal-names"></a>リース仕訳帳名の設定

[!include [banner](../includes/banner.md)]

リース仕訳帳の名前は、資産リース トランザクションが転記される仕訳帳を指定します。 **資産リース** 仕訳帳タイプに割り当てられている仕訳帳名のみが、**資産リース パラメーター** ページの **初期認識** フィールドと **月次仕訳帳名** フィールドに表示されます。 **請求仕訳帳名** フィールドに割り当てることができるのは、**仕入先請求書記録** 仕訳帳タイプだけです。

リース仕訳帳の名前をコンフィギュレーションするには、次の手順に従います。

1. **資産絵イース \> 設定 \> 資産リース パラメーター** の順に移動します。
2. **一般** タブの **初期認識仕訳帳名** フィールドで、仕訳帳を選択します。 すべての初期認識仕訳帳エントリは、この仕訳帳名に転記されます。
3. **請求書仕訳帳名** フィールドで、仕訳帳を選択します。 **仕入先への支払** オプションがリース帳簿に対して **はい** に設定されている場合は、リースおよび経費の支払請求書がこの仕訳帳名に転記されます。
4. **リース仕訳帳名** フィールドで、仕訳帳を選択します。 すべての減価償却、利息、および短期再分類のエントリは、この仕訳帳名に転記されます。 **仕入先への支払** オプションがリース帳簿に対して **いいえ** に設定されている場合は、リース支払および経費エントリもこの仕訳帳名に転記されます。
