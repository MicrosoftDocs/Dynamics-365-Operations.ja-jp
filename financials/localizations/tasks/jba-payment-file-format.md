--- 
title: "JBA 支払ファイル形式の有効化 (日本)"
description: "日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。"
author: ShylaThompson
manager: AnnBe
ms.date: 09/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Japan
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 1eac1ca7b6950e8dc1f30a6a64838a096ea2535a
ms.contentlocale: ja-jp
ms.lasthandoff: 07/27/2017

---
# <a name="enable-the-jba-payment-file-format-japan"></a>JBA 支払ファイル形式の有効化 (日本)

[!include[task guide banner](../../includes/task-guide-banner.md)]

日本では、電子資金決済 (EFT) のファイル形式は全国銀行協会 (JBA) により指定されています。 



この手順では、JBA の支払モデルのインポートおよび仕入先の支払方法に対する JBA の支払ファイルの有効化について説明します。 



この手順は、デモ データ会社 JPMF を使用して作成されました。


## <a name="import-the-jba-payment-model"></a>JBA 支払モデルのインポート
1. [組織管理] > [ワークスペース] > [電子申告] の順に移動します。
2. [リポジトリ] をクリックします。
3. [開く] をクリックします。
4. ツリー内で、[支払モデル] \JBA [支払いモデル] \JBA [支払ファイル (JP)] を選択します。
5. [インポート] をクリックします。
6. [はい] をクリックします。

## <a name="use-the-jba-payment-file-in-the-vendor-method-of-payment"></a>仕入先の支払方法での JBA 支払ファイルの使用
1. [買掛金勘定] > [支払設定] > [支払方法] の順に移動します。
2. [編集] をクリックします。
3. [ファイル形式] セクションを展開または折りたたみます。
4. [一般的な電子申告] チェック ボックスを選択します。
5. [書式設定のコンフィギュレーションのエクスポート] フィールドで、ドロップダウン ボタンをクリックしてルックアップを開きます。
6. 一覧で、JBA [支払ファイル (JP)] を選択します。
7. [保存] をクリックします。


