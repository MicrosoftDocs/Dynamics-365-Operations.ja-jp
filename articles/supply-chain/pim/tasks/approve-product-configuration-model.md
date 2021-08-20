---
title: 製品コンフィギュレーション モデルの承認
description: この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 208dd55720a54ef1516f2691811ff9c86e5b132d3e5c459a048f5889faec24fd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735186"
---
# <a name="approve-a-product-configuration-model"></a>製品コンフィギュレーション モデルの承認

[!include [banner](../../includes/banner.md)]

この手順を実行するには、少なくとも 1 つの製品コンフィギュレーション モデルが必要です。 この手順では、デモ データの会社 USMF の [ハイエンド スピーカー] モデルが使用されています。 このモデルは既に承認済ですが、手順は、プロセス全体について説明します。

1. **製品情報管理\>製品\>製品コンフィギュレーション モデル** の順にクリックします。
1. 一覧で、目的のレコードを見つけ、選択します。
    * この手順の [ハイエンド スピーカー] モデルを選択します。  
1. **バージョン** を選択します。
1. **新規** を選択します。
1. **製品番号** フィールドで、値を入力または選択します。
    * 製品への参照は、製品コンフィギュレーション モデルのバージョンを表します。 制約ベースのコンフィギュレーション テクノロジがある製品マスターのみこの一覧に表示されます。  
1. **開始日** フィールドに日付を入力します。
    * 製品モデル バージョンがある場合選択します。  
1. **終了日** フィールドに、日付を入力します。
    * この製品モデル バージョンの有効期限が切れる場合は終了日を、または [なし] を選択します。  
1. **承認** を選択してドロップ ダイアログを開きます。
1. **承認者** フィールドで、値を入力または選択します。
    * 工程の使用のために製品モデルの承認を担当する個人を選択します。  
1. **OK** を選択します。
1. **価格決定方法** フィールドで、オプションを選択します。
    * 製品モデルのバージョンを有効化します。 1 度に、1 つの製品モデルに対して、1 つの製品のみ有効にできます。  
1. ページを閉じます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]