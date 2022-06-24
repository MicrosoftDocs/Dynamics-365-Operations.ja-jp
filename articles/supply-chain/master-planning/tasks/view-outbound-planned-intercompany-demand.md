---
title: 出庫の計画企業内需要を表示する
description: この記事では、出庫の計画企業内需要を表示する方法を示す手順について説明します。
author: t-benebo
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dcdea0af5cb522646bc63c7e5ef1d4e54e0a3547
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8895644"
---
# <a name="view-outbound-planned-intercompany-demand"></a>出庫の計画企業内需要を表示する

[!include [banner](../../includes/banner.md)]

この手順では、会社間仕入先によって達成されるすべての計画オーダーを表示する方法を示します。 この手順の作成に使用するデモ データの会社は DEMF です。

1. **マスター プラン** を選択します。
2. **計画** フィールドで値を入力または選択します。
    * **計画** フィールドで、プラン *10* を選択します。  
3. *実行* を選択します。
4. **スレッド数** フィールドに数値を入力します。
    * これは、マスタ プランに使用する並行スレッドの数を表します。  
5. **OK** を選択します。
    * しばらく時間がかかる場合があります  
6. **計画企業内需要** を選択します。
7. **出庫の計画企業内需要** を選択します。
    * このページは、内部サプライ チェーンの仕入先によって達成されるすべての計画需要の概要を提供します。  
8. **上流の需要の詳細** セクションを展開します。
    * このセクションでは、どのように需要が達成されるかについての詳細を確認することができます。 ここで追加情報を表示する前に、提供会社で実行するマスター プランを待機する必要があります。  

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
