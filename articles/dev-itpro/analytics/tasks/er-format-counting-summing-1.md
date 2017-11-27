--- 
title: "電子申告 (ER) 用の棚卸および集計を行うための形式を作成する"
description: "次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。"
author: NickSelin
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5d4f57ae2a309d9e15c1afe60c3e91d7d7eb3870
ms.openlocfilehash: 3c4ae958a03d4681a85f5b83d81fe64b9ac99cf5
ms.contentlocale: ja-jp
ms.lasthandoff: 11/02/2017

---
# <a name="create-format-for-counting-and-summing-for-electronic-reporting-er"></a>電子申告 (ER) 用の棚卸および集計を行うための形式を作成する

[!include[task guide banner](../../includes/task-guide-banner.md)]

次の手順では、システム管理者または電子レポート開発者のロールに指定されたユーザーが、生成済みのテキスト出力に基づく計算と集計の電子レポート（ER）フォーマットをどのように環境設定するのかについて示します。 これらの手順はどのタイプの企業でも実施できます。

これらの手順を完了するには、先に「コンフィギュレーション プロバイダーの作成および有効なプロバイダーとしてのマーク付け」の手順の各ステップを完了する必要があります。

この手順は、Dynamics 365 for Operations、バージョン 1611 に追加された機能です。


## <a name="get-access-to-the-list-of-configurations-provided-by-microsoft"></a>Microsoft 提供の設定リストにアクセスする
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
    * Litware, Inc. を確認します プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。  
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


