---
title: レジスターの作成と関連付け
description: この手順では、販売時点管理 (POS) レジスターを作成する方法を示します。
author: rubencdelgado
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailTerminalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ac5135d0606ffc9816c841637aa032826f87e28
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023172"
---
# <a name="create-and-associate-registers"></a>レジスターの作成と関連付け

[!include[task guide banner](../includes/task-guide-banner.md)]

この手順では、販売時点管理 (POS) レジスターを作成する方法を示します。 この手順では、デモ データ会社 USRT を使用します。

1. [小売りとコマース] > [チャンネル設定] > [POS 設定] > [レジスター] の順に移動します。
2. [新規] をクリックします。
3. [レジスター番号] フィールドに、新しいレジスターの ID を入力します。
    * レジスター ID には、レジスターを所属する店舗とその店舗内の場所にマップするためのコードが通常含まれます。  
4. [名前] フィールドに、レジスターの内容を説明する名前を入力します..
5. [店舗番号] フィールドで、値を入力または選択します。
6. [ハードウェア プロファイル] フィールドで、値を入力または選択します。
    * ハードウェア プロファイルはキャッシュ ドロワーやレシート プリンターなど、レジスターに接続される小売周辺機器を指定するのに使用されます。  
7. [ビジュアル プロファイル] フィールドで、値を入力または選択します。
    * 視覚プロファイルは POS のバックグラウンド、ログイン ページ、および POS のテーマで使用されている画像を指定するのに使用されます。  
8. [EFT POS レジスター番号] フィールドに値を入力します。
    * EFT POS レジスター番号はどの支払ターミナルが認証要求を送信しているかを支払処理担当者に通知するために使用されます。 この値は、「ターミナル ID」、または「TID」と呼ばれます。 TID は、支払デバイスのステッカーの明細行から見つけることができます。  
9. [保存] をクリックします。

