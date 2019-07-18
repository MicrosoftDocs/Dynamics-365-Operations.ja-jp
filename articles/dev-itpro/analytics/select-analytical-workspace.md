---
title: PowerBI.comからの分析ワークスペースの選択
description: このトピックでは、PowerBI.comでホストされているレポートを選択してアプリケーション ワークスペースで使用する方法について説明します。
author: tjvass
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Platform update 26
ms.openlocfilehash: add3f3ae779b06b3f114cef16984c14dff2c1791
ms.sourcegitcommit: 9f762fa89c5b432667aa156c22d679a7f601952d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/08/2019
ms.locfileid: "1731106"
---
# <a name="select-analytical-workspaces-from-powerbicom"></a>PowerBI.comからの分析ワークスペースの選択

[!include[banner](../includes/banner.md)]

## <a name="analytical-workspaces"></a>分析ワークスペース

アプリケーション スイートにバンドルされている分析ワークスペースは、ユーザーにビジネス データに関する適切な洞察を提供します。 ただし、場合によっては、標準レポートを組織のユーザー専用に設計されたカスタムレポートに置き換えることが必要になることがあります。

PowerBI.comが提供するワールドクラスのツールを使用すると、外部ソースからのデータを使用するマッシュアップ ビューを含む分析レポートを生成できます。 Microsoft Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 26 ( 2019 年 5 月) で、パワー ユーザーは標準埋め込みレポートをPowerBI.comでホストされているレポートと置き換えることができます。

> [!IMPORTANT]
> このトピックで説明する機能は、個人用設定ではありません。 分析ワークスペースのカスタマイズは、有効な法人のすべてのユーザーに適用されます。

### <a name="motivations-for-embedding-powerbicom-reports"></a>PowerBI.comレポートの埋め込みの動機

標準レポートは、特定のビジネスペルソナ向けにカスタマイズされた情報を提供しますが、場合によっては組織でカスタムレポートを作成することをお勧めします。 Finance and Operationsにより、パワー ユーザーはPowerBI.comでホストされまた組織のメンバと共有できるカスタムレポートを奨励することができます。

ここでは、PowerBI.comでホストされているレポートを選択する場合の主な動機をいくつか示します。

- PowerBI.comレポートは、外部データソースを使用し、Finance and Operations外部からアクセスできるデータ マッシュ アップをサポートします。
- レポートは、PowerBI.comでホストされ、ワン ボックス配置でアプリケーションに埋め込まれるカスタム ソリューションのデモンストレーションに適しています。
- Microsoft Power BIプレミアムサービスを使用している組織では、標準レポートを強化したいと考えています。

### <a name="embed-a-powerbicom-report-in-an-analytical-workspace"></a>分析ワークスペースへのPowerBI.comレポートの埋め込み

標準レポートを置き換えるには、システム レポート エディター セキュリティ グループのメンバーである必要があります。 このセキュリティ グループ メンバーは、標準レポートをカスタマイズするためのアプリケーション ワークスペースのオプションにアクセスできます。 次の例は、標準分析レポートを、PowerBI.comでホストされているカスタム レポートに置き換える方法を示しています。

1. Finance and Operations にログインし、カスタマイズするアプリケーション レポートを開きます。 この例では、 **報酬管理** ワークスペースに埋め込まれている標準分析レポートを置換します。

    ![報酬管理ワークスペース](media/compensation-management-workspace.png)

2. **分析** タブを選択すると、ワークスペースの埋め込み分析レポートにアクセスできます。

    ![報酬管理分析ワークスペースの [分析] タブ](media/compensation-management-analytics.png)

    デフォルトでは、Finance and Operations アプリケーション に含まれている標準分析ワークスペース ソリューションが表示されます。 このソリューションのレポートは、プロビジョニング プロセス中に環境に合わせて自動的に配置および設定されます。

    > [!NOTE]
    > 分析ワークスペースには、専用の環境に対してのみ使用できるホストされた Power BI サービスが必要です。 詳細については、ブログ投稿 [1-Box 環境での分析ワークスペースおよびレポートへのアクセス](https://blogs.msdn.microsoft.com/dynamicsaxbi/2017/07/29/accessing-analytical-workspaces-on-1box-environment/) を参照してください。

3. アクション ペインの **オプション** タブの **Power BI** グループで、 **分析の選択** を選択して **Power BIレポート** ダイアログボックスを開きます。

    ![Power BIレポート ダイアログ ボックス](media/select-powerbi-report-analytics.png)

    このダイアログボックスでは、PowerBI.comサービスで共有されているレポートの中から選択することができます。 レポートはワークスペース毎に編成されています。

4. ドロップダウン リストで、レポートを含むワークスペースを選択します。
5. アプリケーション ワークスペースに埋め込むレポートを選択し、 **OK** を選択します。
6. ワークスペースの更新を表示するには、ページを再度読み込む必要があります。 ワークスペースから移動して戻ってくるか、ブラウザーを更新します。
7. **報酬管理** ワークスペースで、 **分析** タブを選択し、分析ワークスペースに埋め込まれた PowerBI.com レポートにアクセスします。

    ![カスタム分析ワークスペース](media/custom-powerbi-report-analytics.png)

### <a name="revert-to-the-standard-solution"></a>標準ソリューションに戻す

PowerBI.comレポートをアプリケーションワークスペースに埋め込んだ後、そのレポートに対する更新は、Finance and Operationsのユーザー向けにすぐに反映されます。 ただし、レポートを別の PowerBI.com ソリューションに置き換えるには、まず、標準のアプリケーション ソリューションに戻す必要があります。 次の手順に従って、標準のアプリケーションソリューションに戻します。

1. アクション ペインの **オプション** タブの **Power BI** グループで **分析の復元** を選択してください。

    ![[分析の復元] ボタン](media/restore-powerbi-report-analytics.png)

2. ワークスペースの更新を表示するには、ページを再度読み込む必要があります。 ワークスペースから移動して戻ってくるか、ブラウザーを更新します。
3. **報酬管理** ワークスペースで、**分析** タブを選択し、分析ワークスペースに埋め込まれた 標準ソリューション にアクセスします。
