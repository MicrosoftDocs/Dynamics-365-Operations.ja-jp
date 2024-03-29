---
title: RFQ のスコア方法の作成
description: この手順では、スコア方法を作成する方法を示します。
author: GalynaFedorova
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a6b715caa57d8ceb2e91af88538fa735568a997
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2022
ms.locfileid: "8671062"
---
# <a name="create-a-scoring-method-for-rfqs"></a>RFQ のスコア方法の作成

[!include [banner](../../includes/banner.md)]

この手順では、スコア方法を作成する方法を示します。 スコア方法は、見積依頼 (RFQ) の回答として送信する入札を比較するために使用できる一連の基準です。 たとえば、仕入先の過去のパフォーマンスを評価、環境に優しい会社かどうか、良い協力者であるかを評価、または価格に基づく入札の比較をする場合があります。 入札タイプの RFQs の規定のスコア方法として、スコア方法を入札タイプと関連付けることができます。 通常、これらのタスクを実施するのは、購買マネージャーです。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。

1. [調達] > [設定] > [見積依頼] > [スコア方法] の順に移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [説明] フィールドに値を入力します。
5. [保存] をクリックします。
6. [新規] をクリックします。
7. [名前] フィールドに値を入力します。
8. [説明] フィールドに値を入力します。
    * この説明は、スコア方法が RFQ に対して選択された場合、スコア方法の名前とともに表示されます。  
9. [範囲の開始] フィールドに数値を入力します。
    * 調達担当者がスコアとして入力できる範囲を制限します。 RFQ に複数のスコア基準がある場合、入力した基準が相互に追加され、さらに入札が比較できるよう合計が使用可能になります。  
10. [範囲の終了] フィールドに数値を入力します。
11. [新規] をクリックします。
12. [名前] フィールドに値を入力します。
13. [説明] フィールドに値を入力します。
14. [範囲の開始] フィールドに数値を入力します。
15. [範囲の終了] フィールドに数値を入力します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]