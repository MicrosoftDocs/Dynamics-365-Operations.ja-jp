--- 
title: "会社間計画の作成"
description: "この手順では、会社間計画を作成する方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 7c7f466add55fb9a24c3fb8f1f92df712a8622e3
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="create-an-intercompany-plan"></a>会社間計画の作成

[!include[task guide banner](../../includes/task-guide-banner.md)]

この手順では、会社間計画を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。


## <a name="set-up-an-intercompany-planning-group"></a>会社間計画グループを設定する 
1. [会社間計画グループ] に進みます。
    * [マスター プラン] > [設定] > [会社間計画グループ]  
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、値「10」を含む [名前] フィールドをフィルター処理します。
3. 一覧で、選択された行をマークします。
4. [削除] をクリックします。
    * この手順は、会社間の計画実行の期間を短縮するのに必要です。   会社間計画では、最下位のスケジューリングシーケンスから始まる計画グループにおける会社のマスタープランが実施されます。  
5. [はい] をクリックします。
6. ページを閉じます。

## <a name="create-an-intercompany-plan"></a>会社間計画の作成
1. [会社間マスター プラン] をクリックします。
    * これはマスタープランのワークスペースにあります。  
2. [会社間計画グループ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * 会社間計画グループ 10を選択する  
4. [会社間計画の繰り返し回数] フィールドで、「2」と入力します。
    * 会社間計画グループ10にはメンバーが2名います。 顧客の会社 (DEMF) にソースの会社 (USMF) の遅延を反映させるには、両方の会社で会社間計画を実行する必要があります。 最初の繰り返しが需要を反映し、ソースの会社 (USMF)の遅延を識別します。 2番目の繰り返しはUSMFからDEMFへの遅延を反映します。  
5. [最初の繰り返し] フィールドで、オプションを選択します。
6. [最初の繰り返し] フィールドで、[再生成] を選択します。
7. [後の繰り返し] フィールドで、[再生成] を選択します。
8. [スレッド数] フィールドに数値を入力します。
    * これは、計画に使用される並行スレッドの数を表します。  
9. [OK] をクリックします。

## <a name="view-the-result-of-the-plan"></a>計画の結果を表示する
1. [計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
2. 一覧で、選択された行のリンクをクリックします。
    * StaticPlanのリンクをクリックします。 会社USMFにいる必要があります。  
3. [計画オーダー] をクリックします。


