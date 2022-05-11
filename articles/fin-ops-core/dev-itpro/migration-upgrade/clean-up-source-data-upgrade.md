---
title: Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations にアップグレードするためにソース データをクリーンアップする
description: このトピックでは、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) へのアップグレードの一環としてソース データをクリーンアップする方法について説明します。
author: ttreen
ms.date: 04/26/2022
ms.topic: article
audience: Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: ttreen
ms.search.validFrom: ''
ms.search.form: 2022-04-08
ms.openlocfilehash: e5ff56438b2823e70443121a7c24c746934d0828
ms.sourcegitcommit: 5130446fd5327595b2d67e67cbd1b5661bb2983c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/27/2022
ms.locfileid: "8648754"
---
# <a name="clean-up-source-data-for-upgrade-from-microsoft-dynamics-ax-2012-to-dynamics-365-finance--operations"></a>Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations にアップグレードするためにソース データをクリーンアップする

[!include [banner](../includes/banner.md)]

このトピックでは、Microsoft Dynamics AX 2012 から Dynamics 365 Finance + Operations (on-premises) へのアップグレードの一環としてソース データをクリーンアップする方法について説明します。

## <a name="background"></a>背景

時間の経過と共に、Dynamics AX 2012 データベースはサイズが増大することがあります。 アップグレードの前に、データを削除またはアーカイブすることで、データベースのサイズを小さくすることができます。 これにより、データ アップグレードの完了までに要する時間を削減できます。

## <a name="clean-up-operations"></a>クリーンアップの工程

Dynamics 365 Finance + Operations にアップグレードする前に、次のクリーンアップ操作を実行する必要があります。

### <a name="run-the-dynamics-ax-intelligent-data-management-framework-tool"></a>Dynamics AX Intelligent Data Management Framework ツールを実行する

Dynamics AX Intelligent Data Management Framework (IDMF) ツールは現在更新されていませんが、Dynamics AX 2012 データベースのデータをアーカイブまたは削除するために使用できます。 詳細については、[Dynamics AX Intelligent Data Management Framework](/dynamicsax-2012/appuser-itpro/microsoft-dynamics-ax-intelligent-data-management-framework-idmf) を参照してください。

### <a name="clean-up-batch-job-history-tables"></a>バッチ ジョブ履歴テーブルのクリーンアップ

SQL から直接、またはカスタム X++ ジョブ経由で、次のテーブルを完全にまたは部分的にクリーンアップできます。 すぐに使用できるクリーンアップ スクリプトはありません。 したがって、開発は各自行う必要があります。

- BatchJobHistory
- BatchHistory
- BatchConstraintsHistory
