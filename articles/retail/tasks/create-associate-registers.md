--- 
title: "レジスターの作成と関連付け"
description: "この手順では、販売時点管理 (POS) レジスターを作成する方法を示します。"
author: rubencdelgado
manager: AnnBe
ms.date: 10/05/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6a95019e50bcc060165dab3e6aa2b3ca8a897bf3
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

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


