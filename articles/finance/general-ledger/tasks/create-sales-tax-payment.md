---
title: 消費税支払の作成
description: 売上税の決済と転記のジョブでは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。
author: twheeloc
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0b6c67a547e42ab4d7b7ba9f456a29c6b3d22e491e3a8ad0481a0144491087
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763169"
---
# <a name="create-a-sales-tax-payment"></a>消費税支払の作成

[!include [banner](../../includes/banner.md)]

売上税の決済と転記のジョブでは、売上税勘定の売上税残高を決済して、特定の期間の売上税決済勘定と相殺します。

1. **税 > 申告 > 売上税 > 売上税の決済と転記** の順に移動します。
2. **決済期間** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
4. **開始日** フィールドに日付を入力します。
    * **訂正を含める** オプションが **総勘定元帳のパラメーター** のページで選択されていない場合、決済処理で異なるバージョンを処理できます。 [オリジナル] は決済期間の最初の決済であり、1 つのサイクル間隔で 1 回のみ処理できます。 最新の修正は、オリジナル バージョンの作成後に転記された売上税のトランザクションを決済します。   
5. **トランザクション日付** フィールドに、日付を入力します。
6. **OK** をクリックします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]