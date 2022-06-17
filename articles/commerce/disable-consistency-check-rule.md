---
title: トランザクション検証プロセスで使用されるルールを無効にする
description: この記事では、Microsoft Dynamics 365 Commerce のトランザクション検証ルールを無効にする機能について説明します。
author: analpert
ms.date: 12/11/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d566aa3b829dad281528925a341382f9637fdba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8884879"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>トランザクション検証プロセスで使用されるルールを無効にする

[!include [banner](../includes/banner.md)]

小売業者に固有の業務シナリオとプロセスが実現します。 そのため、コマース トランザクション検証プロセスに含まれるあらゆるルールが、すべての小売業者に適用されるとは限りません。 差異を調節するため、Microsoft Dynamics 365 Commerce には、適用されないルールを無効にするための機能が用意されています。

環境内のトランザクション検証プロセスで使用できるルールの一覧を表示し、各ルールの状態を確認するには、**Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** の順に移動して、**トランザクションの検証** タブを選択します。有効なすべてのルールは、**店舗トランザクションの検証** プロセス中にトランザクションを検証するために使用され、トランザクションを収集してトランザクション明細書に転記するために渡す必要があります。

既定では、すべてのルールの状態が **有効** に設定されています。 そのため、すべてのルールを使用して小売トランザクションを検証してからコマース トランザクション明細書に取り込めます。 ルールを無効にするには、状態を **無効** に変更します。 **店舗トランザクションの検証** プロセス中にトランザクションが検証される場合、無効になっているルールは考慮されません。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
