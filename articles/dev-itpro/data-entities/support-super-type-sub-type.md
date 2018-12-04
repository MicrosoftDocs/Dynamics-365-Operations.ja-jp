---
title: "スーパー タイプおよびサブ タイプ"
description: "データ エンティティの継承パターンのサポートについて説明します。"
author: Sunil-Garg
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 25331
ms.assetid: d59cefc0-be94-42e9-a22e-87493985dbcd
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 448ab6deb50e63fd63c7501aea1c9b6991a94cd8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="super-types-and-sub-types"></a>スーパー タイプおよびサブ タイプ

[!include [banner](../includes/banner.md)]

データ エンティティの継承パターンのサポートについて説明します。

## <a name="patterns"></a>パターン

継承を含むテーブルのエンティティを作成する方法はいくつかあります。

- **データ ソースとしてのリーフ/具象型:** 具象型をデータソースとして使用すると、基本型と現在の型の両方のフィールドが表示されます。 たとえば、次のスクリーン ショットでは、DirPerson がデータ ソースである場合、DirPerson および DirPartytable の両方からのデータ ソース フィールドを表示します。

    [![sub1](./media/sub1.png)](./media/sub1.png)

    [![sub2](./media/sub2-419x1024.png)](./media/sub2.png)

- **データ ソースとしての抽象タイプ/非リーフ:** 非リーフ タイプをデータ ソースとして使用する場合、基準タイプと現在のタイプの両方にフィールドが表示されますが、派生型のフィールドは表示されません。 次のスクリーン ショットに示すように、派生型からのフィールドは派生データ ソースから追加される必要があります。

    [![sub3](./media/sub3.png)](./media/sub3.png)

## <a name="data-entity-view-wizard"></a>データ エンティティの表示ウィザード
**データ エンティティ ビュー** ウィザードを使用すると、継承に含まれるテーブルがプライマリ データ ソース (および追加データ ソース) である場所で、データ エンティティを作成することができます。

> [!NOTE]
> 現在、ウィザードは派生データ ソースをサポートしていません。 現在の型または基本データ型からフィールドのみを表示します。 エンティティを作成した後、手動で派生データ ソースを表示するよう変更できます。

次のスクリーン ショットは、DirPartyTable がプライマリ データ ソースである、ウィザードを使用して作成されたデータ エンティティを示しています。

[![sub4](./media/sub4.png)](./media/sub4.png)

1. データ ソース テーブルを **DirPartyTabl** に更新します。

    [![sub5](./media/sub5.png)](./media/sub5.png)

2. データ ソース テーブルを **DirPartyTable** に更新します。

    [![sub6](./media/sub6.png)](./media/sub6.png)

## <a name="run-time"></a>実行時間
継承に関連するエンティティの実行時動作があります。

### <a name="creating-entities-for-specified-types"></a>指定したタイプのエンティティを作成しています

この例では、個別の**個人**および**組織**エンティティを作成します。 **担当者** エンティティのプライマリ データ ソースは DirPerson で、**組織** エンティティのプライマリ データ ソースは DirOrganization です。 この方法は、次のスクリーン ショットに反映されていますが、特別なランタイム コードを記述する必要はありません。

[![sub7](./media/sub7.png)](./media/sub7.png)

[![sub8](./media/sub8-419x1024.png)](./media/sub8.png)

### <a name="creating-entities-for-generalized-types"></a>一般化されたタイプのエンティティを作成しています

この例では、単一のエンティティである**パーティ**を作成して、**個人**および**組織**の両方に使用できます。 プライマリ データ ソースが DirPartyTable で、派生データ ソースが DirPerson と DirOrganization です。 新しいエンティティには、次のようなフィールドが含まれています。

- **一般的な属性** -**個人**または**組織**に固有ではない属性 (例: **名前**) これらのフィールドは、DirPartyTable にマップされます。
- **個人の固有の属性** – **性別**、**配偶者の有無**など。 これらのフィールドは、派生データ ソース DirPartyTable\_DirPerson にマップされます。
- **組織に固有の属性** – **OrgNumber**、**ABC** などです。 これらのフィールドは、派生データ ソース DirPartyTable\_DirOrganization にマップされます。

[![sub9](./media/sub9.png)](./media/sub9.png)

デザイン時のタスクとして、ひとつのデータエンティティで基本型と複数の派生型のフィールドをマッピングします。 ただし、実行時に、各派生型が作成されるときを指定する必要があります。 これは、**InstanceRelationType** などのフィールドに基づいても、異なるタイプを表す **String** を使用するように計算カラムを作成もできます。 **関係者**エンティティの例で、**PartyType** 計算列を作成して**個人**および**組織**の派生型を表すことができます。 次のコード スニペットは、このアプローチを示しています。

[![sub10](./media/sub10.png)](./media/sub10.png)

この例では、**関係者**タイプは DirPartyTable の **InstanceRelationType** 列を使用して計算されます。 この方法は、データを読み取るために機能します。 ただし、**作成**または**更新**操作を行うには、タイプに基づいて、データ エンティティの **initializeEntityDataSource** メソッドを上書きするコードを記述する必要があり、およびデータ ソースの実行時コンテキスト バッファに対する派生型の正しいインスタンスを設定する必要があります。

[![sub11](./media/sub11.png)](./media/sub11.png)

