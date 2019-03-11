---
title: AX 2009 の移行 － パッケージのインポート
description: このトピックは、Microsoft Dynamics AX 2009 から Microsoft Dynamics 365 for Finance and Operations に移行済みデータ パッケージをインポートする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 676c38e8d8134448210097ab634010bba194ad97
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369673"
---
# <a name="ax-2009-migration--import-packages"></a>AX 2009 の移行 - パッケージのインポート

[!include [banner](../includes/banner.md)]

データは、正しい順序で配列された論理的に関連するエンティティのグループにインポートできます。 Microsoft Dynamics 365 for Finance and Operations に移行する Microsoft Dynamics AX 2009 データをインポートするための、以下の 3 つのオプションがあります。

- AX 2009
- Finance and Operations

## <a name="ax-2009"></a>AX 2009
移行のデータは、ソース システムから直接インポートできます。 以下の手順を実行します。

1. AX 2009 の、ナビゲーション ウィンドウで、**データ移行** をクリックします。
2. **共通** \> **移行グループの作成** に移動します。
3. **移行グループ** フォームで、エクスポートする移行グループを選択し、**今すぐエクスポート** をクリックします。
4. **データのエクスポート** フォームで、**ターゲットにパッケージをインポートする** チェック ボックスをオンにし、**OK** をクリックします。

## <a name="finance-and-operations"></a>Finance and Operations
Finance and Operations 環境を使用して、移行のデータをインポートできます。 以下の手順を実行します。

1. 管理者ロールを使用して、Finance and Operations 環境にログインします。
2. ダッシュボードで、**データ管理**ワークスペースを選択します。
3. **インポート** を選択します。
4. パッケージの名前を入力し、**ソースのデータ形式** フィールドで **パッケージ** を選択します。
5. **アップロード** を選択し、インポートするデータの場所から適切なパッケージ ファイルを選択します。 パッケージからすべてのファイルがインポートされます。

