---
title: 売上税支払の作成
description: 売上税の決済と転記のジョブは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee69cfee672be1571fd5cc630e33601bb5a48eac
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846562"
---
# <a name="create-a-sales-tax-payment"></a>売上税支払の作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

売上税の決済と転記のジョブは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。

1. [税] > [申告] > [売上税] > [売上税の決済と転記] の順に移動します。
2. [決済期間] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. [開始日] フィールドに日付を入力します。
    * [訂正を含める] オプションが [総勘定元帳のパラメータ] のページで選択されていない場合、決済は、異なるバージョンについて処理できます。 [オリジナル] は決済期間の最初の決済で、1 つの間隔について 1 回のみ処理できます。 最新の修正は、オリジナル バージョンの作成後に転記された売上税トランザクションを決済します。   
5. [トランザクション日付] フィールドに、日付を入力します。
6. [OK] をクリックします。

