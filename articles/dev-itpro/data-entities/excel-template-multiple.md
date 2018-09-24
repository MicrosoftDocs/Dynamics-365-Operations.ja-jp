---
title: "複数のワークシートを含む Excel データ エンティティ テンプレートからのデータ インポート"
description: "このトピックでは、Excel データ エンティティ テンプレートを使用して、Microsoft Dynamics 365 for Finance and Operations にデータをインポートする方法について説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 01/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application user
ms.reviewer: margoc
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 48239b48cbc24e34d74bbac36e8f827a15d7b840
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="import-data-from-excel-data-entity-templates-that-have-multiple-worksheets"></a>複数のワークシートを含む Excel データ エンティティ テンプレートからのデータ インポート

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations のデータ管理は、データ エンティティ用の Microsoft Excel ベースのテンプレートをサポートしています。 これらのテンプレートには、1 つまたは複数のワークシートを含めることができます。 複数のワークシートを含むテンプレートは、1つのファイルでデータを管理し、複数のデータ エンティティにインポートすると便利な場合によく使用されます。 サイトや倉庫の例があります。

## <a name="upload-a-file-once-and-map-it-to-all-entities"></a>ファイルを一度アップロードし、すべてのエンティティにマップする
**サイト**および**倉庫**と呼ばれるワークシートを持つ Excel ファイルが 1 つある場合の例を考えてみましょう。 データ インポート プロジェクトを設定するには、最初のデータ エンティティ、**サイト**を追加してからファイルをアップロードします。 このエンティティをしようするために**サイト**をワークシートとして選択することができます。

**ファイルの追加** フォームを残さずに第 2 のエンティティ **倉庫** を追加すると、ワークシートの参照により、ファイルを再度アップロードせずに **倉庫** ワークシートを選択できるようになります。 新しいファイルをアップロードする唯一の理由は、**倉庫**のデータが他のファイルにある場合だけです。

![複数のワークシート](./media/AddFileMultipleWorkSheets.png)

## <a name="fix-worksheet-to-entity-mapping"></a>エンティティ マッピングへのワークシートの修正

インポート ジョブのデータ エンティティへのワークシートのマッピングは、グリッドから固定することができます。 グリッドの **ワークシート** 列には、マップされたファイルのワークシートが表示されます。 ドロップダウン メニューから別のワークシートを選択することができます。 選択したワークシートがすでにデータ プロジェクト内のエンティティにマップされている場合は、変更を確認するメッセージが表示されます。 グリッド内のすべてのマッピングを修正することをお勧めします。

![ワークシート マッピングの更新](./media/UpdateMappings.png)

## <a name="re-map-to-a-new-file"></a>新しいファイルに再マップします

同じファイルの新しいバージョンまたは完全に新しいファイルをデータ プロジェクトの既存のエンティティにアップロードする必要がある場合は、**ファイルの追加**エクスペリエンスを使用して、エンティティを最初に追加した時のように、再度追加します。 続行する前に、システムはデータ プロジェクト内の既存のエンティティを上書きすることを確認します。 再度追加されない (または上書きされた) エンティティは、以前のファイルから以前のマッピングを保持し続けます。

## <a name="upload-a-file-using-run-project"></a>プロジェクトを実行してファイルをアップロードする

**プロジェクトを実行** オプションを使用して Excel ファイルをアップロードして、インポート プロジェクトを実行することができます。 データ プロジェクト内のデータ エンティティの既存のマッピングと同じワークシートを持つファイルのみをアップロードするように注意する必要があります。 新しくアップロードされたファイルにワークシートが見つからない場合、システムはエラーを表示してインポートを停止します。 エンティティに対してワークシートへのマッピングを変更する必要がある場合は、**プロジェクトを実行** エクスペリエンスのファイルを使用する前に、データプロジェクト内のマッピングを最初にデータプロジェクト内から更新する必要があります。

