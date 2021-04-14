---
title: 連続スケジュールの定義
description: このトピックでは、連続プログラム (それ以外の場合は、繰り返し注文とも呼ばれます) の設定について説明します。
author: josaw1
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8414377ddec0e001f003f842866725eb58bd75a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791610"
---
# <a name="define-continuity-schedules"></a>連続スケジュールの定義

[!include [banner](../includes/banner.md)]

このトピックでは、連続プログラム (それ以外の場合は、繰り返し注文とも呼ばれます) の設定について説明します。 このトピックでは、デモ データの会社 USRT を使用します。


## <a name="create-continuity-program"></a>連続プログラムの作成
1. Retail と Commerce > 連続 > 連続プログラムの順に移動します。
2. [新規] をクリックします。
3. スケジュール ID フィールドで、[連続スケジュール ID] と入力します。
4. [注文の開始] フィールドで、「最初のイベント」を選択します。
    * 顧客が連続プログラムの新しい注文を配置する場合は、どの製品を出荷するかについて 2 つのオプションがあります: 1。 最初のイベント: 連続プログラムで最初の製品を出荷します。  2. 現在のイベント: 現在の製品が出荷されます。 例えば、 3 か月間のプログラムで、顧客はプログラムの 3 番目を受け取ります。  
5. 注文の開始日を確認するには、[はい] を選択します。
6. [明細行の追加] をクリックします。
7. [品目番号] フィールドで、最初の品目番号 (0013) を入力します。
8. [CP] と入力します。
9. 最初の製品が注文できる日付を入力します。
10. [行の追加] をクリックします。
11. [品目番号] フィールドで「0014」と入力します。
12. 日付間隔コードフィールドで、値をオフにすると、フィールドは空になります。
    * この手順で、日付範囲をオフにします。 最初の品目の増分日付として開始日付を設定します。  
13. ここでは、製品を出荷する間隔を入力します。 タイプ「30」。
    * 月ごとのプログラムの場合、間隔は 30 日と入力します。  
14. [明細行の追加] をクリックします。
15. [品目番号] フィールドで「0015」と入力します。
16. [終了] と入力します。
17. [保存] をクリックします。

## <a name="assign-to-continuity-item"></a>連続品目に割り当てます
1. [製品情報管理] > [製品] > [リリースされた製品] の順に移動します。
2. 品目「0016」を選択します。
    * この手順では、品目番号 0016 を選択します。 通常、コール センターの販売注文時に適用される、追加の連続ビジネス ロジックがあるリリースされた製品を作成しています。  
3. 一覧で、選択された行のリンクをクリックします。
4. [編集] をクリックします。
5. [販売] セクションを展開または折りたたみます。
6. ここでは、この品目が示す連続プログラムを入力します。 前に作成したスケジュール ID を入力します。
    * この品目がコールセンターで販売される場合、追加のビジネス ロジックは、選択した連続プログラムから適用されます。  
7. [保存] をクリックします。



[!INCLUDE[footer-include](../../includes/footer-banner.md)]