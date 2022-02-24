---
title: オンライン チャンネルの作成およびチャンネルの属性の定義
description: この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8e92e28c721692ed92fa931ed899c48678622349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964797"
---
# <a name="create-online-channel-and-define-channel-attributes"></a>オンライン チャンネルの作成およびチャンネルの属性の定義

[!include [banner](../includes/banner.md)]

この手順では、新しいオンライン チャンネルを作成し、組織階層に追加する手順を説明しています。 新しいオンライン チャンネルを作成する前に、組織階層を作成する必要があります。 この手順では、デモ データの会社 USRT を使用します。


## <a name="create-a-new-online-channel"></a>新しいオンライン チャンネルの作成
1. Retail と Commerce > チャネル > オンライン ストアに移動します。
2. [新規] をクリックします。
3. [名前] フィールドに値を入力します。
4. [倉庫] フィールドで、値を入力または選択します。
5. [ストア タイムゾーン] フィールドで、オプションを選択します。
6. [既定の顧客] フィールドで、値を入力または選択します。
7. [顧客のアドレス帳] フィールドで、値を入力または選択します。
8. [支払条件] フィールドで値を入力または選択します。
9. [支払方法] フィールドで値を入力または選択します。
10. [電子メール通知 プロファイル] フィールドで値を入力するか選択します。
11. [財務分析コード] セクションを展開します。
12. [事業単位] フィールドで値を入力または選択します。
    * 同様に、そのほかの既定の分析コードの値を設定します。  
13. [保存] をクリックします。

## <a name="add-the-online-channel-to-organization-hierarchy"></a>組織階層にオンライン チャンネルを追加します
1. ページを閉じます。
2. [組織管理] > [組織] > [組織階層] の順に移動します。
3. 一覧で、目的のレコードを見つけ、選択します。
4. [表示] をクリックします。
5. [編集] をクリックします。
    * 新しいチャンネルを挿入する階層ノードを選択できます。  
6. [挿入] をクリックします。
7. Commerce チャネルをクリックします。
8. [OK] をクリックします。
9. [発行] をクリックして、ドロップ ダイアログを開きます。
10. [有効日] フィールドに日時を入力します。
11. [発行] をクリックします。

## <a name="configure-orders-for-near-real-time-notification"></a>ほぼリアルタイムのオーダー通知のコンフィギュレーション
1. Retail と Commerce > バックオフィスの設定 > パラメーター > Commerce パラメーターの順に移動します。
2. 電子商取引 オーダー作成のリアルタイム サービス使用を、「はい」に設定します。
3. チャンネル データベースへの同期変更に、1070 配送スケジュールを実行します。 


