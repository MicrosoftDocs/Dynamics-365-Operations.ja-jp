---
title: 小売トランザクションの整合性チェックのルールを無効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce に導入された小売トランザクションの整合性チェックのルールを無効にする機能について説明します。
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: b11b901fafc3907e9d3cae5cd554cc9a868a414c
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004346"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>小売トランザクションの整合性チェックのルールを無効にする 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

小売業者に固有の業務シナリオとプロセスが実現します。 したがって、コマース トランザクション整合性チェックに既定で含まれるあらゆるルールが、すべての小売業者に適用されるとは限りません。 差異を調節するため、Microsoft Dynamics 365 Commerce には、適用されないルールを無効にするための機能が用意されています。

ご利用中の環境内にある小売トランザクション整合性チェックで使用できるルールの一覧を表示したり、各ルールの状態を表示したりするには、**Retail と Commerce \>本社の設定 \> パラメーター \> コマース パラメーター** に移動し、**トランザクションの検証** タブをクリックします。

既定では、すべてのルールの状態が **有効** に設定されています。 したがって、すべてのルールを使用して小売トランザクションを検証してからコマース明細書に取り込まれます。 ルールを無効にするには、状態を **無効**に変更します。 明細書の計算プロセス中にトランザクションが検証されている場合、無効になっているルールは考慮されません。

有効になっているルールに関係なく、検証プロセス全体を回避するには **Retail と Commerce \> 本社の設定 \> パラメーター \> コマース パレメーター**に移動し、**トランザクションの検証** タブで、**コマース トランザクションの整合性チェックの無効化** オプション **はい** に設定します。 このオプションを **いいえ** に設定すると、ユーザー インターフェイス (UI) から **はい** に設定し直すことはできません。
