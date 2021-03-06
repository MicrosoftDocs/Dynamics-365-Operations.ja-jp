---
title: クライアントの接続が切断される
description: この記事では、顧客が自身の環境から切断され、またその理由が分からない場合の対処方法について説明します。
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fcb7e5e3230aee9f6c04e4854c8eea836ae14c7f
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053422"
---
# <a name="client-disconnects"></a>クライアントの接続が切断される

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**環境の詳細** 

この問題は、すべての環境で発生する可能性があります。
 
**現象** 

顧客は自身の環境から切断され、またその理由が分かりません。 顧客は、次のエラー メッセージのいずれかを受け取ります。

- 接続が失われました。 作業を続行するには、閉じるをクリックします。
- ネットワーク接続が失われた可能性があります。もう一度実行するには [再試行] をクリックしてください。

**赤いフラグ**

この問題は、ユーザーが実装のステージで、実稼働環境とテスト環境の間で情報を比較していて、セッション間で移動していることを忘れている場合によく発生します。 ユーザーがこのステージにいる場合は、この問題が発生する可能性が高くなります。

**問題点** 

**ブラウザーの種類:** Google Chrome Internet Explorer、および Microsoft Edge

Microsoft Dynamics 365 Human Resources は、2 つの異なるセッションが同じユーザーと同じブラウザー タイプで同時に開いているときにユーザーを切断します。 (たとえば、ユーザー A が Chrome で環境 1 と環境 2 の両方を表示しています。) ユーザーがブラウザーの別のウィンドウを開いているのか、別のタブを開いているのかは関係ありません。 同じユーザー資格情報が、同じブラウザー タイプで同時に環境 1 と環境 2 の両方へのサインインに使用される場合、人事管理はセッションのいずれかを切断します。

**ソリューション**

特定のブラウザー タイプにつき 1 つだけの環境が開いていることを確認します。 ユーザーは、同じ環境 (つまり、同じブラウザの複数のタブ) に対して複数のセッションを開くことができます。

同時に 2 つの環境間を移動するユーザーは、異なるブラウザー タイプで各環境を開く必要があります。 (たとえば、ユーザー A は Chrome で環境 1 を、Microsoft Edge で環境 2 を表示できます。)


[!INCLUDE[footer-include](../includes/footer-banner.md)]