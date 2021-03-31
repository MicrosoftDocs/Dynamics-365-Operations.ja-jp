---
title: 製品コンフィギュレーション モデルの承認
description: この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 191aff59b16fb8c7caf6b5c7f822f1a0a077fc9f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212081"
---
# <a name="approve-a-product-configuration-model"></a>製品コンフィギュレーション モデルの承認

[!include [banner](../../includes/banner.md)]

この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。 この手順では、デモ データの会社 USMF の [ハイエンド スピーカー] モデルが使用されています。 このモデルは既に承認済ですが、手順は、プロセス全体について説明します。

1. [製品バリアント モデルの定義] をクリックします。
2. [製品コンフィギュレーション モデル] をクリックします。
3. 一覧で、目的のレコードを見つけ、選択します。
    * この手順の [ハイエンド スピーカー] モデルを選択します。  
4. [バージョン] をクリックします。
5. [新規] をクリックします。
6. [製品番号] フィールドで、値を入力または選択します。
    * 製品への参照は、製品コンフィギュレーション モデルのバージョンを表します。 制約ベースのコンフィギュレーション テクノロジがある製品マスターのみこの一覧に表示されます。  
7. [開始日] フィールドに日付を入力します。
    * 製品モデル バージョンがある場合選択します。  
8. [終了日] フィールドで、日付を入力します。
    * この製品モデル バージョンの有効期限が切れる場合は終了日を、または [なし] を選択します。  
9. [承認] をクリックすると、ドロップ ダイアログが開きます。
10. [承認者] フィールドで、値を入力または選択します。
    * 工程の使用のために製品モデルの承認を担当する個人を選択します。  
11. [OK] をクリックします。
12. [価格決定方法] フィールドで、オプションを選択します。
    * 製品モデルのバージョンを有効化します。 1 度に、1 つの製品モデルに対して、1 つの製品のみ有効にできます。  
13. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]