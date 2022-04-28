---
title: 電子レポートを使用した確認後支払ファイルの設定および生成
description: このトピックでは、電子レポートを使用して確認後支払いを設定する方法について説明します。
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 43dd1a9cba1fe8df5cff26fe76af7e2957a0d6a4
ms.sourcegitcommit: cf7d4af11bf85638ee831a28ea5ee1a1e041a675
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/04/2022
ms.locfileid: "8544487"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>電子レポートを使用した確認後支払ファイルの設定および生成

確認後支払を設定し、銀行に渡す小切手の電子リストを生成します。 次に、小切手が銀行に提出されたら、銀行はそれを小切手リストと比較します。 小切手がリストの小切手と一致する場合、銀行は小切手を決済します。 小切手がリスト内の小切手と一致しない場合、銀行は確認のために小切手を保留にします。

## <a name="set-up-the-electronic-reporting-configuration"></a>電子レポート構成の設定

1. **ワークスペース \> 電子レポート** に移動します。
2. **Microsoft** 構成プロバイダーのタイルで、**リポジトリ** を選択します。
3. **グローバル** を選択し、 **開く** を選択します。
4. リポジトリへの接続を確立する必要がある場合は、ダイアログ ボックスで青色のリンクを選択します。
5. 構成リストで、**確認後支払モデル \> 確認後支払形式** を探して選択します。
6. **バージョン** クイック タブで、最新のバージョンを選択して、**インポート** を選択します。

## <a name="set-up-a-positive-pay-format"></a>確認後支払形式の設定

1. **現金および銀行管理 \> 設定 \> 確認後支払形式** に移動します。
2. **新規** を選択します。
3. **支払形式** と **説明** フィールドを設定します。
4. **一般的な電子エクスポート形式** チェックボックスを選択します。
5. **エクスポート形式構成** フィールドを **確認後支払形式** に設定します。

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>銀行口座への確認後支払形式の割り当て

1. **現金および銀行管理 \> 銀行口座 \> 銀行口座** に移動します。
2. 銀行口座を開きます。
3. **一般** クイック タブで、**確認後支払** フィールドを以前に作成された形式に設定します。
4. **確認後支払開始日** フィールドを現在の日付に設定します。

## <a name="generate-a-positive-pay-file"></a>確認後支払ファイルの生成

1. **現金および銀行管理 \> 銀行口座 \> 銀行口座** に移動します。
2. 確認後支払が設定される銀行口座を開きます。
3. **支払の管理 \>確認後支払 \> 確認後支払ファイル** を選択します。
4. **締め日** フィールドを設定します。 この日付の前に生成された小切手が含まれます。

結果の XML ファイルがダウンロードされます。
