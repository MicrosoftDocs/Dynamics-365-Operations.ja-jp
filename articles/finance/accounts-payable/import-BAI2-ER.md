---
title: 電子申告を使用した詳細な口座調整インポートの設定
description: このトピックでは、電子申告を使用して、BAI2 取引明細書の詳細な口座調整インポート プロセスを設定する方法について説明します。
author: panolte
ms.date: 03/30/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.25
ms.openlocfilehash: 39f1d8ba561ab0e36346f1dfb4f70df318c92a37
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544503"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>電子申告を使用した詳細な口座調整インポートの設定

[!include [banner](../includes/banner.md)]

詳細な口座調整機能では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。 このトピックでは、BAI2 口座取引明細書のインポート機能を設定する方法について説明します。

## <a name="set-up-the-electronic-reporting-configuration"></a>電子レポート構成の設定

1. **ワークスペース \> 電子レポート** に移動します。
2. **Microsoft** 構成プロバイダーのタイルで、**リポジトリ** を選択します。
3. **グローバル** を選択し、 **開く** を選択します。
4. リポジトリへの接続を確立する必要がある場合は、ダイアログ ボックスで青色のリンクを選択します。
5. コンフィギュレーション リストで、**口座取引明細書モデル \> BAI2 の口座取引明細書モデル** を見つけます。
6. **BAI2** 形式を選択します。
7. **バージョン** クイック タブで、最新のバージョンを選択して、**インポート** を選択します。

## <a name="set-up-the-bank-statement-format"></a>口座取引明細書の形式の設定

1. **現金および銀行管理 \> 設定 \> 詳細な口座調整の設定 \> 口座取引明細書の形式** の順に移動します。
2. **新規** を選択します。
3. **取引明細書形式** と **名前** フィールドを設定します。
4. **一般的な電子インポート形式** チェックボックスを選択します。
5. **インポート形式構成** フィールドを **BAI2** 形式に設定します。

## <a name="set-up-the-bank-account"></a>銀行口座の設定

1. **現金および銀行管理\>銀行口座\>銀行口座** に移動します。
2. 銀行口座を開きます。
3. **調整** クイックタブで、**詳細な口座調整** オプションを **はい** に設定します。
4. **明細書形式** フィールドを、先ほど作成した **BAI2** 形式に設定します。

## <a name="import-the-bank-statement"></a>口座取引明細書のインポート

1. **現金および銀行管理 \> 口座取引明細書調整 \> 口座取引明細書** に移動します。
2. **口座取引明細書** ページの最上部で、**取引明細書のインポート** を選択します。
3. **銀行口座** フィールドを取引明細書の銀行口座に設定します。
4. **明細書形式** フィールドを、先ほど作成した **BAI2** 形式に設定します。
5. **参照** を選択し、**BAI** ファイルを選択します。
6. **アップロード** を選択します。
7. **OK** を選択し、選択したファイルをインポートします。
