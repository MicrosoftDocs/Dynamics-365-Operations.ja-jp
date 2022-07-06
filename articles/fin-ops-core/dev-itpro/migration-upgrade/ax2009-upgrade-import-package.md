---
title: AX 2009 の移行 － パッケージのインポート
description: この記事は、Microsoft Dynamics AX 2009 から財務と運用に移行されたデータ パッケージをインポートする方法について説明します。
author: kfend
ms.date: 09/13/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: e8741fb477e234b924d2ebb1d2df300e93880c8f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866241"
---
# <a name="ax-2009-migration--import-packages"></a>AX 2009 の移行 - パッケージのインポート

[!include [banner](../includes/banner.md)]

データは、正しい順序で配列された論理的に関連するエンティティのグループにインポートできます。 移行する Microsoft Dynamics AX 2009 データをインポートするために、以下の 3 つのオプションがあります。

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

1. 管理者ロールを使用して、環境にログインします。
2. ダッシュボードで、**データ管理** ワークスペースを選択します。
3. **インポート** を選択します。
4. パッケージの名前を入力し、**ソースのデータ形式** フィールドで **パッケージ** を選択します。
5. **アップロード** を選択し、インポートするデータの場所から適切なパッケージ ファイルを選択します。 パッケージからすべてのファイルがインポートされます。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]