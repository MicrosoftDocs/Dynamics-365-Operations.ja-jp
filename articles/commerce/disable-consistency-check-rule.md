---
title: トランザクション検証プロセスで使用されるルールを無効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce のトランザクション検証ルールを無効にする機能について説明します。
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
ms.openlocfilehash: cdaea51b4c84e6a62f0eb9412315ae77b4c11503
ms.sourcegitcommit: 9c2bc045eafc05b39ed1a6b601ccef48bd62ec55
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/14/2021
ms.locfileid: "7919530"
---
# <a name="disable-rules-used-in-the-transaction-validation-process"></a>トランザクション検証プロセスで使用されるルールを無効にする

[!include [banner](../includes/banner.md)]

小売業者に固有の業務シナリオとプロセスが実現します。 そのため、コマース トランザクション検証プロセスに含まれるあらゆるルールが、すべての小売業者に適用されるとは限りません。 差異を調節するため、Microsoft Dynamics 365 Commerce には、適用されないルールを無効にするための機能が用意されています。

環境内のトランザクション検証プロセスで使用できるルールの一覧を表示し、各ルールの状態を確認するには、**Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** の順に移動して、**トランザクションの検証** タブを選択します。有効なすべてのルールは、**店舗トランザクションの検証** プロセス中にトランザクションを検証するために使用され、トランザクションを収集してトランザクション明細書に転記するために渡す必要があります。

既定では、すべてのルールの状態が **有効** に設定されています。 そのため、すべてのルールを使用して小売トランザクションを検証してからコマース トランザクション明細書に取り込めます。 ルールを無効にするには、状態を **無効** に変更します。 **店舗トランザクションの検証** プロセス中にトランザクションが検証される場合、無効になっているルールは考慮されません。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
