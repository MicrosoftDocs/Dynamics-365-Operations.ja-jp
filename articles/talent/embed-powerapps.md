---
title: Dynamics 365 Human Resources の Power Apps アプリの埋め込み
description: このトピックでは、Microsoft Power Apps メニュー項目がシステム管理モジュールから消えてしまう問題を解決する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8275a8a7c68fa13d6b9880c4c411deaa2dcbb998
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4461716"
---
# <a name="embed-power-apps-apps-in-dynamics-365-human-resources"></a>Dynamics 365 Human Resources の Power Apps アプリの埋め込み

**問題点**

**Power Apps** メニュー項目が **システム管理** モジュールから消えました。

**原因**

ユーザー インターフェイス (UI) のデザインが変更され、Microsoft Power Apps が標準の個人用設定モデルに含まれるようになりました。

**解像度**

Power Apps が埋め込まれる方法が変更されました。 Power Apps は個人用設定モデルによって追加されます。 Power Apps は、Microsoft Dynamics 365 Talent のほとんどすべてのページに追加できます。

Power Apps を Talent に埋め込む方法の詳細については、[Power Apps の埋め込み](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps)を参照してください。

変更前にアプリを埋め込んだ Power Apps の顧客は、新しいモデルにアップグレードする必要があります。

**Power Apps** ボタンは、Talent のほとんどすべてのページの右上隅にあります。 このボタンを使用して、アプリを挿入することができます。

次に例を示します。

1. **人事管理\>リンク\>作業者\>従業員** に移動します。
2. **Power Apps** ボタンを選択し、**Power Apps からアプリを追加** をクリックします。

    ![Power Apps ボタン](media/png.png)

3. **Power Apps からアプリを追加** ダイアログ ボックスのフィールドに入力します。

    ![Power Apps からアプリを追加ダイアログボックス](media/insert-powerapp.png)

または、次の手順に従います。

1. ページのアクション ウィンドウの **オプション** タブ上の **個人用設定** グループで、**このページのパーソナライズ** を選択します。

    ![オプション タブのグループをパーソナライズする](media/options.png)

    個人用設定ツール バーが表示されます。

2. ツール バーで、**Power Apps からアプリを追加** を選択します。

    ![個人用設定ツールバーを使用して Power Apps からアプリを追加する](media/powerapp-bar.png)
