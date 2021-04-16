---
title: 源泉徴収税の支払を作成する
description: 源泉所得税の支払と転記のジョブの手順では、源泉所得税口座の未払金から源泉所得税の残高を精算し、所定の期間の源泉所得税精算口座に相殺します。 このトピックでは、源泉徴収税の支払を設定する手順を示します。
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: 72d80fbb3b2448f4b89fa7d7fa580387e1a3621c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832949"
---
# <a name="create-a-withholding-tax-payment"></a>源泉徴収税の支払を作成する

源泉所得税の支払と転記のジョブの手順では、源泉所得税口座の未払金から源泉所得税の残高を精算し、所定の期間の源泉所得税精算口座に相殺します。 このトピックでは、源泉徴収税の支払を設定する手順を示します。

> [!NOTE] 
> (売掛金管理から)源泉徴収税の支払を計算する際は、源泉徴収税の相殺は考慮されません。

1. **ナビゲーション ウィンドウ > モジュール > 税 > 申告 > 源泉徴収税 > 源泉徴収税の支払** の順に移動します。
2. **決済期間** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. **開始日** フィールドに日付を入力します。
5. **トランザクション日付** フィールドに、日付を入力します。
6. **更新** を選択すると、源泉徴収税の支払伝票が源泉徴収税決済勘定に転記されます。
7. **OK** をクリックします。

![源泉徴収税支払に使用するパラメーター](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]