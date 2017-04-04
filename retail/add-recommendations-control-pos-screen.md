---
title: "POSのデバイスのトランザクションのページにベスト プラクティス コントロールを追加します。"
description: "このトピックでは、Microsoft Dynamics 365の画面レイアウト デザイナーを使用して(POS)のPOSデバイスのトランザクションの画面にベスト プラクティス コントロールを追加する方法について説明します。"
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 2377b1639a3c95fe6bba4754c4069cc12043e3d3
ms.lasthandoff: 03/31/2017


---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a>POSのデバイスのトランザクションのページにベスト プラクティス コントロールを追加します。

このトピックでは、Microsoft Dynamics 365の画面レイアウト デザイナーを使用して(POS)のPOSデバイスのトランザクションの画面にベスト プラクティス コントロールを追加する方法について説明します。

工程にMicrosoft Dynamics 365 for Operationsを使用すると、POSのデバイスの製品の推奨事項を表示できます。 *Recommendations*そのほかの顧客はオンラインと実店舗で購入した顧客が、品目欲しい基づく品目のリストに必要な発注の履歴、品目にかもしがあります。品目です。 製品の推奨事項を表示するには、画面レイアウト デザイナーを使用してトランザクションの画面にコントロールを追加する必要があります。

## <a name="open-layout-designer"></a>レイアウト デザイナーを開きます。
1.  ** [小売りとコマース** ** &gt; 設定されている**チャンネルは、実行 &gt; **設定されているPOS ** &gt; ** ** &gt; ** POS画面レイアウト**。
2.  コントロールを追加する画面をすばやく検索、フィルタを使用します。 たとえば、で**画面レイアウトID **フィールドに正「F2CP16の値を使用してフィルタ処理します: 」9M。
3.  一覧で、目的のレコードを見つけ、選択します。 たとえば、「名前を選択します: F2CP16: 9Mの画面レイアウトID: F2CP16: 」9M。
4.  [**レイアウト デザイナー**。
5.  レイアウト デザイナーを起動するためにプロンプトに従います。 資格情報の場合はメッセージが表示されたら、レイアウト デザイナーが**画面レイアウト**ページから起動時に使用中の同じ資格情報を入力します。
6.  ログインすると、およびに類似したページに、表示されます。 レイアウトは、店舗に対して行われたカスタマイズによって異なります。

[![screenlayout pic1] (。/media/screenlayout pic1.png) ] (。/media/screenlayout pic 1.pngは、表示オプションを選択します。
-----------------------

使用できる二つのコンフィギュレーション オプションがあります。 店舗の変更を行って選択し、コントロールのセットアップを完了残りの手順に従って、オプションを。 二つのオプションは次のとおりです:
-   報酬認定が表示されますです。
-   A **ベスト プラクティス画面の右側のグリッドに**タブが表示されます。

#### <a name="to-make-recommendations-always-visible"></a>ベスト プラクティスを常に対して表示されるようにします。

1.  これが左に顧客のパネル高さと同じになるようにトランザクション明細行の詳細]領域の高さを減少します。[] (。/media/pic-2.png![) [screenlayout pic 2] (。/media/screenlayout pic2.png) ] (。/media/screenlayout pic2.png) 
2.  左側のメニューから、トランザクション明細行の詳細]領域およびトランザクションの画面のワーク センターの下部のボタン グリッドの間で推奨事項をドラッグ アンド ドロップします。 コントロールのサイズを変更すると、その地域で合う。[] (。/media/pic-3.png![) [screenlayout pic 3] (。/media/screenlayout pic3.png) ] (。/media/screenlayout pic3.png) 
3.  レイアウト デザイナーを保存して終了する** X **クリックします。
4.  Dynamics 365 for Operationsでは、** [小売りとコマース** ** &gt; 小売するIT **を移動する &gt; **配分のスケジュール**。
5.  一覧で、選択します** 1090の登録**。
6.  [**、実行**。

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a>ベスト プラクティス タブを画面の右側のボタン グリッドに追加します。

1.  ページの右側にあるボタン グリッドの最後のタブの下部に空白を右クリックします。
2.  **カスタマイズ**クリックします。[![pic5] (。/media/pic-5.png) ] (。/media/pic-5.png) 
3.  [**新しいタブ**。
4.  [で追加する新しいタブを検索します。 スクロールする必要があります。
5.  **目次**ボックスで、[**推奨される製品**。 [![pic6] (。/media/pic-6.png) ] (。/media/pic-6.png) 
6.  ** **ラベル]フィールドで、ベスト プラクティス タブの名前を入力します。 たとえば、「推奨される製品」と入力します。
7.  では**画像**画像]フィールドで、タブに表示される場合に選択します。
8.  Click **OK**. 新しいタブ、ボタン グリッドに表示されます。
9.  レイアウト デザイナーを保存して終了する** X **クリックします。
10. Dynamics 365 for Operationsでは、** [小売りとコマース** ** &gt; 小売するIT **を移動する &gt; **配分のスケジュール**。
11. 一覧で、選択します** 1090の登録**。
12. [**、実行**。


<a name="see-also"></a>参照
--------

[カスタマイズされた製品の推奨事項の概要] (カスタマイズ製品recommendations.md) 


