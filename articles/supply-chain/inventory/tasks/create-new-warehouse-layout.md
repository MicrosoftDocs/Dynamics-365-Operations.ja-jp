---
title: 新しい倉庫レイアウトの作成
description: このトピックでは、倉庫での場所に関する情報を設定する方法を説明します。
author: perlynne
manager: tfehr
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09666e95cc90913f1bf8555b9ff2c48aa55369ed
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432228"
---
# <a name="create-a-new-warehouse-layout"></a>新しい倉庫レイアウトの作成

[!include [banner](../../includes/banner.md)]

このトピックでは、倉庫での場所に関する情報を設定する方法を説明します。 これは、[在庫管理] モジュールで「基本倉庫」を使用して作成された倉庫のみが対象で、[倉庫管理] モジュールで作成された倉庫には適用されません。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。


## <a name="set-the-default-location-capacity"></a>既定の場所の能力を設定します
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫および倉庫管理パラメーター** の順に移動します。
2. **場所** タブを選択します。
3. **標準の幅** フィールドに数値を入力します。
4. **標準の奥行き** フィールドに数値を入力します。
5. **標準の高さ** フィールドに数値を入力します。
6. **保存** を選択します。
7. ページを閉じます。

## <a name="define-the-location-name-format"></a>場所の名前の形式を定義します。
1. ナビゲーション ウィンドウで、**モジュール > 在庫管理 > 設定 > 在庫詳細 > 倉庫** の順に移動します。
2. **新規** を選択します。
3. **倉庫** フィールドに値を入力します。
4. **名前** フィールドに値を入力します。
5. **サイト** フィールドで、ルックアップの目的のレコードを選択します。
6. **場所の名前** セクションの展開を切り替えます。 このセクションのオプションは、場所の名前の既定の形式を定義します。 上記の例では、通路番号、ラック番号、棚番号が含まれます。  
7. **通路を含める** オプションを **はい** に設定します。
8. **ラックを含める** オプションを **はい** に設定します。 
9. ラックの **形式** フィールドに値を入力します。
10. **棚を含める** オプションを **はい** に設定します。
11. 棚の **形式** フィールドに値を入力します。

## <a name="define-warehouse-locations"></a>倉庫の場所の定義
1. アクション ウィンドウで、**倉庫** を選択します。
2. **場所ウィザード** を選択します。
3. **次へ** を選択します。
4. **出荷ドック** オプションを選択解除します。
5. **バルク場所** オプションを選択解除します。
6. **完了** を選択するオプションが表示されるまで、**次へ** を選択します。
7. ページを閉じます。
8. ページを更新します。

