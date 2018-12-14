---
title: "職位階層および Visio へのエクスポートでのテキストの切り捨てを回避します。"
description: "このトピックでは、顧客が Microsoft Dynamics 365 for Talent で職位階層を表示したときに、個人名と職位の名前が切り捨てられる問題を解決する方法について説明します。 テキストの切り捨ては、スクリーン ショットを取ったり、階層を印刷するのを難しくする可能性があります。"
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: b688a396e3b384aedb06c470b1634150ae7aa038
ms.contentlocale: ja-jp
ms.lasthandoff: 12/04/2018

---

# <a name="avoid-text-truncation-on-the-position-hierarchy-and-export-to-visio"></a>職位階層および Visio へのエクスポートでのテキストの切り捨てを回避します。

[!include [banner](includes/banner.md)]

**払出**

顧客が Microsoft Dynamics 365 for Talent で職位階層を表示するとき、個人名と職位の名前は切り捨てられます。 したがって、スクリーン ショットを取ったり、階層を印刷および配布することが難しくなります。

![職位階層](media/position-h.png)

**原因**

この動作は仕様です。

**解像度**

残念ながら、ユーザーがテキストのサイズを簡単に変更することはできません。 ただし、Talent から職位階層をエクスポートし、Microsoft Visio にインポートすることはできます。 次の記事は Microsoft Dynamics AX 2012 用に書かれたものですが、そのプロセスは Talent にも適用されます: [Microsoft Visio に職位階層をエクスポートする](https://docs.microsoft.com/en-us/dynamicsax-2012/appuser-itpro/export-a-position-hierarchy-to-microsoft-visio)。

Visio にエクスポートするには、次の手順を実行します。

1. Talent で、**職位**リスト ページを開きます。

    組織構造図に詳細情報を含めるには、**職位**リストにフィールドを追加して、この手順の後半でウィザードを使用するときに利用できるようにします。

2. アクション ウィンドウで、**Microsoft Office で開く**ボタンを選択し、次に **Excel にエクスポート**で、**職位**を選択します。 または、Ctrl + T キーを押します。

    ![Excel に職位リスト ページをエクスポートする](media/org-admin.png)

3. エクスポートする Excel ファイルを保存します。

    ![Excel のダイアログ ボックスへエクスポートする](media/export-excel.png)

4. Visio では、**Visio - 新規作成**を選択してから、**業務**テンプレート カテゴリを選択します。

    ![新しいダイアグラム](media/new.png)

5. **組織図のウィザード**を選択してから、**作成**を選択します。

    ![組織図のウィザードのダイアログ ボックス](media/orgchart-wizard.png)

6. **既にファイルまたはデータベースに保存されている情報**を選択してから、**次へ**を選択します。

    ![組織図のウィザード 1](media/orgchart-wizard7.png)

7. **テキスト、Org Plus (\*.txt)、または Excel ファイル**を選択してから**次へ**を選択します。

    ![組織図のウィザード 2](media/orgchart-wizard3.png)

8. 職位階層を含む、エクスポートした Excel ファイルを参照して選択し、**次へ**を選択します。

    ![組織図のウィザード 3](media/orgchart-wizard2.png)

9. **名前**フィールドを**職位**に設定し、**報告先**フィールドを**報告先職位**に設定してから、**次へ**を選択します。

    ![組織図のウィザード 4](media/orgchart-wizard1.png)

10. 各ノードに表示するフィールドを選択してから、**次へ**を選択します。

    ![組織図のウィザード 5](media/orgchart-wizard5.png)

11. **職位**列に**図形のデータ フィールド**リストを追加してから、**次へ**を選択します。

    ![組織図のウィザード 6](media/orgchart-wizard6.png)

12. 図は現在使用できません。 このため、次のページで**次へ**を選択します。
13. **ウィザードで組織図をページに自動的に分割する**を選択します。

    ![組織図のウィザード 7](media/orgchart-wizard4.png)

14. **完了** を選択します。

    構造にない職位がある場合、ダイアグラムに含めることが求められます。

Visio で生成されたダイアグラムは、個別のワークシートに各マネージャを表示します。

ダイアグラムに含めるように選択したフィールドに基づいて、各ノードは Visio ファイルが生成されるときに適切な情報を表示します。

![階層ダイアグラム](media/hierarchy.png)

**追加のオプション**

Talent では、**人員**ワークスペースを使用して、いくつかの階層関連の情報を表示できる場合があります。

