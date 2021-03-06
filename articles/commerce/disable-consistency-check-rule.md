---
title: 小売トランザクションの整合性チェックのルールを無効にする
description: このトピックでは、Microsoft Dynamics 365 Commerce に導入されたトランザクションの整合性チェックのルールを無効にする機能について説明します。
author: josaw1
ms.date: 10/15/2019
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
ms.openlocfilehash: ce2abe7e15773edc3122a1bfdf40f3b830e8790e
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792898"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>小売トランザクションの整合性チェックのルールを無効にする 

[!include [banner](../includes/banner.md)]

小売業者に固有の業務シナリオとプロセスが実現します。 したがって、コマース トランザクション整合性チェックに既定で含まれるあらゆるルールが、すべての小売業者に適用されるとは限りません。 差異を調節するため、Microsoft Dynamics 365 Commerce には、適用されないルールを無効にするための機能が用意されています。

ご利用中の環境内にある小売トランザクション整合性チェックで使用できるルールの一覧を表示したり、各ルールの状態を表示したりするには、**Retail と Commerce \>本社の設定 \> パラメーター \> Commerce パラメーター** に移動し、**トランザクションの検証** タブをクリックします。

既定では、すべてのルールの状態が **有効** に設定されています。 したがって、すべてのルールを使用して小売トランザクションを検証してからコマース明細書に取り込まれます。 ルールを無効にするには、状態を **無効** に変更します。 明細書の計算プロセス中にトランザクションが検証されている場合、無効になっているルールは考慮されません。

有効になっているルールに関係なく、検証プロセス全体を回避するには **Retail と Commerce \> 本社の設定 \> パラメーター \> Commerce パラメーター** に移動し、**トランザクションの検証** タブで、**Commerce トランザクションの整合性チェックの無効化** オプション **はい** に設定します。 このオプションを **いいえ** に設定すると、ユーザー インターフェイス (UI) から **はい** に設定し直すことはできません。


[!INCLUDE[footer-include](../includes/footer-banner.md)]