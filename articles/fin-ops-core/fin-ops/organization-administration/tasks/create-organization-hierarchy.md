---
title: 組織階層の作成
description: 組織階層を作成するには、次の手順に従います。
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dde06f758be57fb646696c861218565476abcadc
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140562"
---
# <a name="create-an-organization-hierarchy"></a>組織階層の作成

[!include [banner](../../includes/banner.md)]

組織階層を作成するには、次の手順に従います。 業務について、さまざまな観点から表示と報告を行う組織階層を使用できます。 たとえば、税金、法律、または法令についての報告に使用する 1 つの階層を設定できます。 法的に必須でなくても、内部報告に使用する財務情報を報告する別の階層を設定できます。 

組織階層を作成する前に、組織を作成する必要があります。 詳細については、「法人の作成」 または 「作業単位の作成」 のタスクを参照してください。 また、部署およびチームも作成できます。 

この手順の作成に使用するデモ データの会社は USMF です。

## <a name="create-a-hierarchy"></a>階層の作成
1. **ナビゲーション ウィンドウ > モジュール > 組織管理 > 組織 > 組織階層**の順に移動します。
2. **アクション ウィンドウ**で、**新規**をクリックします。
3. **名前**フィールドに値を入力します。
4. **目的**セクションで、**目的の割り当て**をクリックします。
5. 一覧で、目的のレコードを見つけ、選択します。 組織階層に割り当てる目的を選択します。  
6. **割り当て済の階層**セクションで、**追加**をクリックします。
7. 一覧で、選択された行をマークします。 作成した階層を検索します。  
8. **OK**をクリックします。

## <a name="add-organizations-to-the-hierarchy"></a>階層への組織の追加
1. 一覧で、目的のレコードを見つけ、選択します。 階層を選択します。  
2. **割り当て済の階層**セクションで、**セクションで**をクリックします。
    - 必要に応じて組織を追加します。  
    - 組織を追加するには、**編集**、 次に**挿入**をクリックして組織を追加します。 変更が完了したら、ドラフトを**保存**または変更を**公開**できます。  

