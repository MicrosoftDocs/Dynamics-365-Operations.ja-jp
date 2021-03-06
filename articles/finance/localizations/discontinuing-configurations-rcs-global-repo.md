---
title: RCS グローバル リポジトリのコンフィギュレーションの中止
description: このトピックでは、RCS グローバル リポジトリのコンフィギュレーションを中止する方法について説明します。
author: JaneA07
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-02-02
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 2bd22e991de376cfd93f75158f1f29716d2559e1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018736"
---
# <a name="discontinue-configurations-in-the-rcs-global-repository"></a>RCS グローバル リポジトリのコンフィギュレーションの中止

[!include [banner](../includes/banner.md)]

このトピックでは、RCS グローバル リポジトリのコンフィギュレーションを中止する方法について説明します。 以前は、不要になったコンフィギュレーションのみを削除できました。 現在は、RCS グローバル リポジトリでリリースされたコンフィギュレーションを **中止** としてマークできるようになりました。 この機能によって、次の操作も実行できます。 
 
 - コンフィギュレーションの中止が予定されている場合は、事前に通知してください。
 - 代替コンフィギュレーションに適用される詳細を含めます。
 - 特定のコンフィギュレーションに **サポート終了日** を設定し、いつ中止されるかをユーザーに通知します。

コンフィギュレーション バージョンを中止する場合は、次のオプション情報を指定できます。

  - **代替コンフィギュレーション**
  - **代替コンフィギュレーション バージョン**
  - **自由書式の注記**: このフィールドを使用して、ドキュメントへのリンクや参照を提供します
  - **サポート終了日**: このフィールドは、現在の構成/バージョンのサポート終了日を示します。 この日付は手動で更新する必要があります。
  
コンフィギュレーションを中止するには、次の手順を実行します。 

1. **すべてのバージョン** を **はい** に設定して、1 回の操作で 1 つのバージョンを中止するか、同じ設定のすべてのバージョンを中止するかを選択します。 
2. **中止** パラメーターを **はい** に設定します。
3. **OK** を選択すると、コンフィギュレーションが中止されます。 変更を保存すると、**中止日** フィールドが設定されます。

![コンフィギュレーション中止の情報](media/Discontinue-details-2.png)
  
いつでもコンフィギュレーションを **共有** に戻したり、中止情報を調整することができます。 コンフィギュレーションを共有する場合は、**サポート終了日** と、中止に関連するその他すべての情報を指定して、将来の中止計画を示します。

計画された中止に関する情報を共有する場合は、実際にコンフィギュレーションを中止する前に、ユーザーは置換に関連するすべてのフィールドを事前に入力できますが、**中止** パラメーターは **いいえ** に設定したままにします。

> [!NOTE]
> 中止はコンフィギュレーションの操作を制限しません。 コンフィギュレーションのインポート、実行、または派生を続行できます。これらのフィールドは情報提供のため使用されます。

## <a name="finance-supports-displaying-this-information-starting-in-version-10014"></a>Finance はバージョン 10.0.14 からこの情報表示をサポート

バージョン 10.0.14 以降、Dynamics 365 Finance は中止情報の表示をサポートしています。 **グローバル リポジトリ** ページで、中止に関連する最新の情報を参照できます。 既定では、中止されたコンフィギュレーションは除外されます。
  
**インポートされたコンフィギュレーション** (ERSolutionTable) ページには、インポート時に既に中止されたコンフィギュレーションが表示されます。 インポート後に中止されたコンフィギュレーションの場合、**コンフィギュレーション更新のインポート** ジョブを実行することにより、中止情報を同期できます。


