---
title: 二重書き込みウィザードを使用して環境をリンクする
description: このトピックでは、二重書き込みウィザードを使用して財務と運用アプリ環境を Dataverse 環境にリンクする方法について説明します。
author: nhelgren
ms.date: 05/08/2020
ms.topic: article
audience: Developer
ms.reviewer: tfehr
ms.search.region: Global
ms.author: nhelgren
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65f886169968170d247d5a50d91744de435bd57b
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/31/2022
ms.locfileid: "8061561"
---
# <a name="use-the-dual-write-wizard-to-link-your-environments"></a>二重書き込みウィザードを使用して環境をリンクする

[!include [banner](../../includes/banner.md)]



1. Dataverse 環境にリンクする財務と運用アプリ環境にサイン インします。
2. **ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。

    ![二重書き込みタイル。](media/navigate-to-data-management.png)

> [!NOTE]
> 財務と運用アプリにアクセスできず、環境に変更を加える必要がある場合は、[データ統合管理者ポータル](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftip.dataintegrator.trafficmanager.net%2FdualWrite%3Faxenv%3Ddxxxxxxxxx.cloudax.dynamics.com&data=04%7C01%7Csushmu%40microsoft.com%7C63cee32877c141d7c55108d96c9d49ba%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637660245076784515%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=71dmOTyAgXpSHrwx4OVahwoFJLclbIsAW2DIVwZFUhk%3D&reserved=0) へのリンクを使用して、管理ページに直接移動することもできます。
> 
3. **環境への新しいリンク** を選択して、**Dataverse へのリンク設定** ウィザードを開きます。
4. **環境の選択** ページには、サインインしたユーザーが環境管理者であるすべての Dataverse 環境が一覧表示されます。リンク先の Dataverse 環境を選択し、**次へ** を選択します。

    ![環境ページを選択します。](media/data-service-environment.png)

5. 法人を選択して、**次へ** を選択します。

    ![法人の手順を選択します。](media/select-legal-entities.png)

    正常性チェックを実行し、システムが二重書き込みを有効にするための要件を満たしていることを確認します。 正常性チェックでは、すべての前提条件が完了していることも確認します。 いずれかの正常性チェックが失敗した場合は、次の手順に進む前に、すべての前提条件を完了していることを確認してください。

    次の例では、アプリを接続するためのアクセスが許可されているかどうかのテストが失敗しました。 この場合、最初に適切なアプリケーション ID を作成して、アプリを接続するためのアクセス許可を付与する必要があります。 その後、ウィザードを再実行する必要があります。

    ![正常性チェック ページ。](media/health-check.png)

6. 概要、プライバシー通知、同意を確認し、**作成** を選択します。

財務と運用アプリを Dataverse 環境にリンクしました。 

> [!NOTE]
> テーブル マップが表示されない場合、または空白のページが表示される場合は、システム要件と前提条件の一部としてインストールした二重書き込みアプリケーション オーケストレーション ソリューションを **適用** してください。

7. 二重書き込みアプリケーション オーケストレーション ソリューションを適用します。

    財務と運用アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたばかりのテーブル マップを適用します。 ソリューションを適用すると、既定のテーブル マップが公開されていることが確認できます。

     ![テーブル マップを適用します。](media/apply-entity-maps.png)

Microsoft が公開した二重書き込みテーブル マップ ソリューションを環境に正常にインポートして適用しました。

![テーブル マップは正常にリンクされました。](media/entity-maps-linked.png)


## <a name="next-steps"></a>次のステップ

[テーブル マップの二重書き込みの有効化](enable-entity-map.md)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
