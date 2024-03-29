---
title: 会社間計画の作成
description: この手順では、会社間計画を作成する方法を示します。
author: t-benebo
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2486ce6f03d03982a7ae9c43af447923aabfed2
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469564"
---
# <a name="create-an-intercompany-plan"></a>会社間計画の作成

[!include [banner](../../includes/banner.md)]

この手順では、会社間計画を作成する方法を示します。 この手順の作成に使用するデモ データの会社は USMF です。

## <a name="set-up-an-intercompany-planning-group"></a>会社間計画グループを設定する

1. **ナビゲーション ウィンドウ** で、**モジュール > マスター プラン > 設定 > 会社間計画グループ** の順に移動します。
2. クイック フィルターを使用して、レコードを見つけます。 たとえば、値「10」を含む [名前] フィールドをフィルター処理します。
3. 一覧で、選択された行をマークします。
4. **削除** を選択します。 この手順は、会社間の計画実行の期間を短縮するのに必要です。   会社間計画では、最下位のスケジューリングシーケンスから始まる計画グループにおける会社のマスタープランが実施されます。  
5. **はい** を選択します。
6. ページを閉じます。

## <a name="create-an-intercompany-master-plan"></a>会社間マスター プランの作成

1. **ナビゲーション ウィンドウ** で、**モジュール > マスター プラン > ワークスペース > マスター プラン** の順に移動します。
2. **会社間マスター プラン** を選択します。  
3. **会社間計画グループ** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。
4. 一覧で、選択した行のリンクを選択します。 会社間計画グループ 10を選択する  
5. **会社間計画の繰り返し回数** フィールドで、'2' と入力します。 会社間計画グループ10にはメンバーが2名います。 顧客の会社 (DEMF) にソースの会社 (USMF) の遅延を反映させるには、両方の会社で会社間計画を実行する必要があります。 最初の繰り返しが需要を反映し、ソースの会社 (USMF)の遅延を識別します。 2番目の繰り返しはUSMFからDEMFへの遅延を反映します。  
6. **最初の繰り返し** フィールドで、'再生成' を選択します。
7. **後の繰り返し** フィールドで、'再生成' を選択します。
8. **スレッド数** フィールドに数値を入力します。 これは、計画に使用される並行スレッドの数を表します。  
9. **OK** を選択します。

## <a name="view-the-result-of-the-plan"></a>計画の結果を表示する

1. **計画** フィールドで、ドロップ ダウン ボタンを選択し、ルックアップを開きます。
2. 一覧で、選択した行のリンクを選択します。 StaticPlan のリンクを選択します。 会社USMFにいる必要があります。  
3. **計画オーダー** を選択します。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]