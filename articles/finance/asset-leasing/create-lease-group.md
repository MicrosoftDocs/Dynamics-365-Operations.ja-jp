---
title: リース グループの作成
description: このトピックでは、リース グループを設定する方法について説明します。 新しいリースを作成するには、リース グループが必要です。
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseGroupTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 49a905e9f27f01898628e88c7af781aed1f25ec7
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714148"
---
# <a name="create-a-lease-group"></a>リース グループの作成

[!include [banner](../includes/banner.md)]

このトピックでは、リース グループを設定する方法について説明します。 新しいリースを作成するには、リース グループが必要です。 リース帳簿は、各リース グループに関連付けられています。 リース帳簿は、各リースで作成しなければならない既定の帳簿を決定します。 **リース転記パラメーター** ページでは、特定のアカウントをリース グループに割り当てることができます。

## <a name="create-a-lease-book-and-add-a-lease-group"></a>リース帳簿を作成し、リース グループを追加する

1. **資産リース \> 設定 \> リース グループ** の順に移動します。
2. アクション ウィンドウで **新規** を選択して、リース グループを追加します。 新しい行がグリッドに追加されます。
3. 新しい行の **リース グループ** フィールドに値を入力します。
4. **説明** フィールドで値を入力します。

先ほど入力した情報が、**リースの追加** ページの **リースグループ** フィールドに追加されます。

## <a name="associate-a-book-with-a-lease-group"></a>リース グループへの帳簿の関連付け

リース グループの作成後は、各グループに帳簿を割り当てることができます。 リースを作成してリースグループに割り当てると、そのリースグループに関連付けられた帳簿ごとに一連のスケジュールが作成されます。

> [!NOTE]
> 帳簿をリース グループに割り当てるには、あらかじめ設定しておく必要があります。

1. **資産リース \> 設定 \> リース グループ** の順に移動します。
2. リース グループを選択し、**帳簿** を選択し ます。
3. **新規** を選択し、**帳簿タイプ** フィールドで、リース グループに割り当てる帳簿を選択します。 リースをさまざまな方法で計上する必要がある場合は、複数の帳簿をリース グループに割り当てることができます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
