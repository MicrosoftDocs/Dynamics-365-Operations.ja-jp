---
title: 電子申告を使用した詳細な口座調整インポートの設定
description: この記事では、電子申告を使用して、詳細な口座調整インポート プロセスを設定する方法について説明します。
author: angelad116
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
ms.openlocfilehash: d24e117b21e291dba1e41d9fa15187b84ff795cf
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752723"
---
# <a name="set-up-advanced-bank-reconciliation-import-by-using-electronic-reporting"></a>電子申告を使用した詳細な口座調整インポートの設定

[!include [banner](../includes/banner.md)]

詳細な口座調整機能では、電子口座取引明細書をインポートし、Microsoft Dynamics 365 Finance での銀行トランザクションに合わせて自動的に調整することができます。 この資料では、口座取引明細書のインポート機能を設定する方法について説明します。 口座取引明細書のインポートの設定は、電子口座取引明細書の形式によって異なります。 Microsoft Dynamics 365 Finance は、ISO20022、MT940、BAI2 の 3 つの口座取引明細書の形式を包括的にサポートしています。 

## <a name="set-up-the-electronic-reporting-configuration"></a>電子レポート構成の設定

1. **ワークスペース \> 電子レポート** に移動します。
2. **Microsoft** 構成プロバイダーのタイルで、**リポジトリ** を選択します。
3. **グローバル** を選択し、 **開く** を選択します。
4. リポジトリへの接続を確立する必要がある場合は、ダイアログ ボックスで青色のリンクを選択します。
5. コンフィギュレーション リストで、**詳細な口座調整明細書モデル \> ABR BAI2 形式** を見つけます。
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


## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>口座取引明細書の形式と技術的な配置の例
詳細な口座調整のインポート ファイルの技術的な配置の定義、および 3 つの関連する口座取引明細書のサンプル ファイルの例を以下に示します。[インポート ファイルの例](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| 技術的なレイアウトの定義                             | 口座取引明細書のサンプル ファイル          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)     |
| DynamicsAXISO20022Layout | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)     |

