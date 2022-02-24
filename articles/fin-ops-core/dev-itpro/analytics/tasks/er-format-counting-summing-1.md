---
title: ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)
description: 次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1742582057cc912d8e6f90eb14e9e4cdcd193608
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684718"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-1---create-format"></a>ER 棚卸および集計を行うための形式のコンフィギュレーション (第 1 部 - 形式の作成)

[!include [banner](../../includes/banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。 これらの手順はどのタイプの企業でも実施できます。

この手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。

この手順は Dynamics 365 for Operations バージョン 1611 に追加された機能です。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft 提供の設定リストにアクセスする
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
    * 「Litware, Inc.」 であることを確認してください。 プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。  
2. Litware, Inc. を選択します プロバイダー
3. [リポジトリ] をクリックします。
    * 「運営リソース」のストックがすでにある場合、現在のサブタスクの残りの手順を省略します。  
4. [追加] をクリックしてドロップ ダイアログを開きます。
5. [設定リポジトリ タイプ] フィールドで、「運営 リソース」と入力します。
6. [リポジトリの作成] をクリックします。
7. [OK] をクリックします。

## <a name="get-the-intrastat-configurations-provided-by-microsoft"></a>Microsoft 提供のイントラスタット コンフィギュレーションを取得する
1. [開く] をクリックします。
2. ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。
3. [インポート] をクリックします。
    * [選択した設定のバージョン1.1のインポート] をクリックします。  
4. [はい] をクリックします。
5. ページを閉じます。
6. ページを閉じます。
7. [コンフィギュレーションをレポートする] をクリックします。
8. ツリーで、「Intrastat model」を展開します。
9. ツリーで、「イントラスタットmodel\Intrastat (DE)を選択します。

