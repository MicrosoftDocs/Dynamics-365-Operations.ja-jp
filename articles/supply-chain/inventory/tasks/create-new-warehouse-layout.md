---
title: 新しい倉庫レイアウトの作成
description: この手順は、倉庫での場所に関する情報を設定する方法を示します。
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, DefaultDashboard, InventLocation, WMSLocationWizard
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26314f9015feded41f105814b85069fff0c62964
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "360535"
---
# <a name="create-a-new-warehouse-layout"></a>新しい倉庫レイアウトの作成

[!include [task guide banner](../../includes/task-guide-banner.md)]

この手順は、倉庫での場所に関する情報を設定する方法を示します。 これは、[在庫管理] モジュールで「基本倉庫」を使用して作成された倉庫のみが対象で、[倉庫管理] モジュールで作成された倉庫には適用されません。 デモ データの会社 USMF のこの手順を使うか、または独自のデータを使うことができます。


## <a name="set-the-default-location-capacity"></a>既定の場所の能力を設定します
1. [在庫管理] > [設定] > [在庫および倉庫管理パラメーター] を表示します。
2. [場所] タブをクリックします。
3. [標準の幅] フィールドに数値を入力します。
4. [標準の奥行き] フィールドに数値を入力します。
5. [標準の高さ] フィールドに数値を入力します。
6. [保存] をクリックします。
7. ページを閉じます。

## <a name="define-the-location-name-format"></a>場所の名前の形式を定義します。
1. [在庫管理] > [設定] > [在庫詳細] > [倉庫] の順に移動します。
2. [新規] をクリックします。
3. [倉庫] フィールドに値を入力します。
4. [名前] フィールドに値を入力します。
5. [サイト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。
6. 一覧で、目的のレコードを見つけ、選択します。
7. 場所の名前セクションの展開を切り替えます。
    * このセクションのオプションは、場所の名前の既定の形式を定義します。 上記の例では、通路番号、ラック番号、棚番号が含まれます。  
8. [通路を含める] オプションをオンに設定します。
9. [ラックを含める] オプションをオンに設定します。 
10. ラックの [形式] フィールドに値を入力します。
    * 例: -##  
11. [棚を含める] オプションをオンに設定します。
12. 棚の [形式] フィールドに値を入力します。
    * 例: -##  

## <a name="define-warehouse-locations"></a>倉庫の場所の定義
1. アクション ペインで [倉庫] をクリックします。
2. [場所ウィザード] をクリックします。
3. [次へ] をクリックします。
4. [出荷ドック] オプションを選択解除します。
5. [バルク場所] オプションを選択解除します。
6. [次へ] をクリックします。
7. [次へ] をクリックします。
8. [次へ] をクリックします。
9. [次へ] をクリックします。
10. [次へ] をクリックします。
11. [次へ] をクリックします。
12. [次へ] をクリックします。
    * このページに表示される物理的な寸法は、この手順の開始時に指定したものであることに注意してください。  
13. [次へ] をクリックします。
14. [完了] をクリックします。
15. ページを閉じます。
16. ページを更新します。

