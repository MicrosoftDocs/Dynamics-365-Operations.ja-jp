---
title: プロセス製造向けの生産ジョブの順序付け
description: この手順では、色と梱包サイズの優先順位に従って計画オーダーを配列する方法を示す 1 例として、塗料製品が使用されます。
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db2c881f60b6e5251e2bcdf198da9e1c9f39a0e6
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4431921"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a>プロセス製造向けの生産ジョブの順序付け

[!include [banner](../../includes/banner.md)]

この手順では、色と梱包サイズの優先順位に従って計画オーダーを配列する方法を示す 1 例として、塗料製品が使用されます。 この手順の作成に使用するデモ データの会社は USPI です。 この手順は、生産の計画者を対象としています。


## <a name="run-master-planning-for-uspi"></a>USPI のマスター プランを実行します。
1. [マスター プラン] > [マスター プラン] > [実行] > [マスター プラン] の順に移動します。
2. [マスター プラン] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
3. 一覧で、選択された行のリンクをクリックします。
    * マスター プランを選択します。  
4. [OK] をクリックします。
    * これは、順序のプロセスを含むマスター プランを開始します。 このプロセスには数分かかる場合があります。  

## <a name="view-planned-orders-for-the-paint-products"></a>塗料製品の計画オーダーを表示します。
1. [マスター プラン] > [マスタープラン] > [計画オーダー]　の順に移動します。
2. 情報ボックスで品目の詳細を展開します。
3. 情報ボックスでスケジュールの詳細を展開します。
4. [計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
5. 一覧で、目的のレコードを見つけ、選択します。
    * マスター プランを選択します。  
6. 一覧で、選択された行のリンクをクリックします。
7. クイック フィルターを使用して、'P300' の値で品目番号フィールドにフィルターを適用します。
    * 右へスクロールしてロック解除すると、注文日と配送日を確認できます。 これらの品目が今日の注文日であることと、計画オーダーの出荷日が製品名に示す色や梱包サイズの優先順位後に配列されていないことに注意してください。 品目番号をポイントすると、製品名と優先順位を確認することができます。  

## <a name="sequence-planned-orders-for-paint"></a>塗料の順序付き計画オーダー
1. ページを閉じます。
2. [マスター プラン] > [マスター プラン] > [順序付き計画オーダー] の順に移動します。
3. 情報ボックスで品目の詳細を展開します。
4. 情報ボックスでスケジュールの詳細を展開します。
    * 注記: ここでは、計画オーダーの開始日/開始時刻が 28 日間のバケット期間内に色と梱包サイズに従って配列されていることが分かります。 これらの期間はフィールド キャンペーンの数によって定義されます。 順序付き計画オーダーのフォームは一般的な計画オーダー フォームと同様に動作し、生産計画担当者は、ここで計画オーダーを確定できます。  
5. すべての行をマークします。
6. [承認] をクリックします。
    * これは、選択した順序のアクションを含む計画オーダーを延期するか、または繰り上げるかについて更新します。  

## <a name="verify-the-sequence-of-the-planned-orders"></a>計画オーダーの順序を確認します。
1. ページを閉じます。
2. [マスター プラン] > [マスタープラン] > [計画オーダー]　の順に移動します。
3. 情報ボックスで品目の詳細を展開します。
4. 情報ボックスでスケジュールの詳細を展開します。
5. [計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
    * マスター プランを選択します。  
7. 一覧で、選択された行のリンクをクリックします。
8. クイック フィルターを使用して、'P300' の値で品目番号フィールドにフィルターを適用します。
    * 今の注文が、色やサイズの優先順位に従って配列されていないと、計画オーダーが最も早い注文日付および配送日で開始することに注意してください。 スケジュールの詳細情報ボックスの注文日付列、または開始日を検証します。  

