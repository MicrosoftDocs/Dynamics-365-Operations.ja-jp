---
title: "Talent のクライアントが切断される"
description: "このトピックでは、顧客が自身の環境から切断され、またその理由が分からない場合の対処方法について説明します。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 4f96b986059c179268f8a96ea7e7725831a93524
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="talent-client-disconnects"></a>Talent のクライアントが切断される

[!include [banner](includes/banner.md)]

**環境の詳細** 

この問題は、すべての環境で発生する可能性があります。
 
**現象** 

顧客は自身の環境から切断され、またその理由が分かりません。 顧客は、次のエラー メッセージのいずれかを受け取ります。

- 接続が失われました。 作業を続行するには、閉じるをクリックします。
- ネットワーク接続が失われた可能性があります。もう一度実行するには [再試行] をクリックしてください。

**赤いフラグ**

この問題は、ユーザーが実装のステージで、実稼働環境とテスト環境の間で情報を比較していて、セッション間で移動していることを忘れている場合によく発生します。 ユーザーがこのステージにいる場合は、この問題が発生する可能性が高くなります。

**払出** 

**ブラウザー タイプ:** Google Chrome、Internet Explorer、および Microsoft Edge

Microsoft Dynamics 365 for Talent プラットフォームは、2 つの異なるセッションが同じユーザーと同じブラウザー タイプで同時に開いているときにユーザーを切断します。 (たとえば、ユーザー A が Chrome で環境 1 と環境 2 の両方を表示しています。) ユーザーがブラウザーの別のウィンドウを開いているのか、別のタブを開いているのかは関係ありません。 同じユーザー資格情報が、同じブラウザー タイプで同時に環境 1 と環境 2 の両方へのサインインに使用される場合、Talent はセッションのいずれかを切断します。

**ソリューション**

特定のブラウザー タイプにつき 1 つだけの環境が開いていることを確認します。 ユーザーは、同じ環境 (つまり、同じブラウザの複数のタブ) に対して複数のセッションを開くことができます。

同時に 2 つの環境間を移動するユーザーは、異なるブラウザー タイプで各環境を開く必要があります。 (たとえば、ユーザー A は Chrome で環境 1 を、Microsoft Edge で環境 2 を表示できます。)

