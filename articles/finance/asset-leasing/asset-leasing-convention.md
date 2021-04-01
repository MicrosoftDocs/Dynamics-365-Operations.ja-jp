---
title: 資産リース規則
description: このトピックは、リース資産の規則について説明します。
author: moaamer
manager: Ann Beebe
ms.date: 1/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 7072c34ccbffc6bf135f55fd594cac4d9ea5a463
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5237519"
---
# <a name="asset-leasing-conventions"></a>資産リース規則

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

このトピックは、リース資産の規則について説明します。 リース規則は、リース帳簿の開始日を決定するために使用されます。 リース規則が **なし** に設定されている場合、開始日はリースの開始日と同じになります (**リース開始日** フィールドの値)。 リース規則が **満 1 か月** 設定されている場合、開始日はリースを開始した月の最初の日になります。

その開始日によって、負債償却および資産減価償却スケジュールの期間の開始日が決まります。 支払利息と減価償却費は、関連するスケジュールの期間終了日に転記されます。 初期認識および調整仕訳入力は、開始日に転記されます。

> [!NOTE]
> リース規則機能は、機能管理でオンにする必要があります。 **管理機能** ワークスペースで、**資産リースのリース規則** 機能を探して選択し、**今すぐ有効にする** を選択します。

リース規則は、リース資産帳簿の設定に割り当てられます。

リース規則を表示または割り当てるには、次の手順に従います。

1. **資産リース \> 設定 \> リース帳簿** の順に移動します。
2. **リース規則** フィールドで、次のいずれかの値を選択します。

    | リース規則 | 説明 |
    |--------------------|-------------|
    | None               | 開始日はリースの開始日と同じ日付なので、負債償却スケジュールと資産減価償却スケジュールの初日はリースの開始日です。 終了日は 1 か月後です。 リース規則は、利息が毎月の最終日に転記されることを保証しません。 |
    | 全月         | 開始日をその月のどの日付でも設定できるリースの場合、負債償却スケジュールおよび資産減価償却スケジュールでは、その月の初日に経費が発生します。 このリース規則により、その月全体の利息が各月の最終日に発生します。 |

3. **保存** を選択します。

リースが作成されると、リース用に入力された開始日と、帳簿に対して指定されているリース規則に基づいて、各帳簿の開始日が自動的に入力されます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]