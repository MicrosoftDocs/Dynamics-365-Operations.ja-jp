---
title: AX 2009 の移行 － パッケージのエクスポート
description: このトピックは、Microsoft Dynamics AX 2009 から Finance and Operations に移行するためにデータ パッケージをエクスポートする方法について説明します。
author: kfend
manager: AnnBe
ms.date: 06/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2018-06-21
ms.dyn365.ops.version: Platform update 17
ms.openlocfilehash: 947f2e91b719e785e515d558289de88caf96ad15
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183171"
---
# <a name="ax-2009-migration--export-packages"></a>AX 2009 の移行 - パッケージのエクスポート

[!include [banner](../includes/banner.md)]

Microsoft Dynamics AX 2009 のデータのインポート/エクスポート フレームワーク (DIXF) サービスを使用して、Finance and Operations に移行する必要があるデータを取得することができます。 エクスポート プロセスは、ジョブ ID を使用して行われます。 エクスポートする場合は、エクスポート ジョブを定義する方法を指定できます。 エクスポートするソース データ、変換値、およびフィールド マップを選択できます。 各ソースにクエリを適用して、エクスポートされる内容を制限することもできます。

データ移行ツール (DMT) が生成するエクスポート パッケージは、1 つまたは複数のデータ エンティティで構成できます。 標準的なデータ パッケージは、インポートなどの特定のタスクのエンティティ グループで構成されています。 たとえば、システムの設定に必要なデータ エンティティは、1 つのデータ パッケージの一部である可能性があります。 データ パッケージの形式は、パッケージ マニフェスト、パッケージ ヘッダー、および含まれているデータ エンティティの追加ファイルを含む圧縮ファイルです。

データ パッケージを作成する前に、何を含める必要があるかを計画します。 この方法で、正しいエンティティ、エンティティの順序、およびフィールドが含まれていることを保証します。

データ パッケージをエクスポートするには、これらの手順に従います。

1. AX 2009 の、ナビゲーション ウィンドウで、**データ移行** \> **共通** \> **移行グループの作成** の順にクリックします。
2. **移行グループ** フォームで、エクスポートする移行グループを選択し、**今すぐエクスポート** をクリックします。
3. **データのエクスポート** フォームで、必要に応じてエクスポート ファイル パスを更新し、**OK** をクリックします。
