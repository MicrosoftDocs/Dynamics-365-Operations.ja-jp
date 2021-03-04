---
title: 二重書き込みウィザードを使用して環境をリンクする
description: このトピックでは、二重書き込みウィザードを使用して、Finance and Operations アプリ環境を Dataverse 環境にリンクする方法について説明します。
author: sabinn-msft
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Developer
ms.reviewer: v-douklo
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sabinn
ms.search.validFrom: 2020-03-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4a8ebe8f06d94452e5d967db9907977b8eece420
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/04/2021
ms.locfileid: "4822177"
---
# <a name="use-the-dual-write-wizard-to-link-your-environments"></a>二重書き込みウィザードを使用して環境をリンクする

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



1. Dataverse 環境にリンクする Finance and Operations アプリ環境にサインインします。
2. **ワークスペース \> データ管理** に移動して、**デュアル書き込み** のタイルを選択します。

    ![二重書き込みタイル](media/navigate-to-data-management.png)

3. **環境への新しいリンク** を選択して、**Dataverse へのリンク設定** ウィザードを開きます。
4. **環境の選択** ページには、サインインしたユーザーが環境管理者であるすべての Dataverse 環境が一覧表示されます。リンク先の Dataverse 環境を選択し、**次へ** を選択します。

    ![環境ページを選択する](media/data-service-environment.png)

5. 法人を選択して、**次へ** を選択します。

    ![法人の選択手順](media/select-legal-entities.png)

    正常性チェックを実行し、システムが二重書き込みを有効にするための要件を満たしていることを確認します。 正常性チェックでは、すべての前提条件が完了していることも確認します。 いずれかの正常性チェックが失敗した場合は、次の手順に進む前に、すべての前提条件を完了していることを確認してください。

    次の例では、アプリを接続するためのアクセスが許可されているかどうかのテストが失敗しました。 この場合、最初に適切なアプリケーション ID を作成して、アプリを接続するためのアクセス許可を付与する必要があります。 その後、ウィザードを再実行する必要があります。

    ![正常性チェック ページ](media/health-check.png)

6. 概要、プライバシー通知、同意を確認し、**作成** を選択します。

Finance and Operations アプリを Dataverse 環境にリンクしました。 

> [!NOTE]
> テーブル マップが表示されない場合、または空白のページが表示される場合は、システム要件と前提条件の一部としてインストールした二重書き込みアプリケーション オーケストレーション ソリューションを **適用** してください。

7. 二重書き込みアプリケーション オーケストレーション ソリューションを適用します。

    Finance and Operations アプリの **二重書き込み** ページで、**ソリューションの適用** を選択し、ダウンロードしてインストールしたテーブル マップを適用します。 ソリューションを適用すると、既定のテーブル マップが公開されていることが確認できます。

     ![テーブル マップを適用する](media/apply-entity-maps.png)

Microsoft が公開した二重書き込みテーブル マップ ソリューションを環境に正常にインポートして適用しました。

![テーブル マップは正常にリンクされました](media/entity-maps-linked.png)


## <a name="next-steps"></a>次のステップ

[テーブル マップの二重書き込みの有効化](enable-entity-map.md)
