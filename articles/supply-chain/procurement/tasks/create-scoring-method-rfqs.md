---
title: RFQ のスコア方法の作成
description: この手順では、スコア方法を作成する方法を示します。
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 738768a6756db83a6855756ef48fffb4a5874b4a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021382"
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

