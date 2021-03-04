---
title: タスク管理のコンフィギュレーション
description: このトピックでは、Microsoft Dynamics 365 Commerce においてタスク管理機能をコンフィギュレーションする方法について説明します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 9a4775c2dba2b9aa8e671ab6c246000303b3a37e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413818"
---
# <a name="configure-task-management"></a>タスク管理のコンフィギュレーション

[!include [banner](includes/banner.md)]

このトピックでは、Microsoft Dynamics 365 Commerce においてタスク管理機能をコンフィギュレーションする方法について説明します。

## <a name="overview"></a>概要

Dynamics 365 Commerce のマネージャーおよび従業員が Commerce のタスク管理機能を使用できるようにする前に、タスク管理をコンフィギュレーションする必要があります。 コンフィギュレーションの手順には、マネージャーおよび従業員へのアクセス許可の付与、販売時点管理 (POS) クライアントへのアクセス許可の配分、POS 通知の設定、および POS アプリケーションのホーム ページでの **タスク** タイルのコンフィギュレーションが含まれます。

## <a name="configure-permissions-for-store-managers"></a>店舗マネージャーのアクセス許可のコンフィギュレーション

指定された店舗の作業者はすべて、店舗に割り当てられているすべてのタスクを表示できます。 また、割り当てられているタスクの状態を更新することもできます。 ただし、店舗のマネージャーなどのペルソナは、店舗に割り当てられているタスクを管理したり、単一目的のタスクを作成したりするするには、タスク管理のアクセス許可が必要です。

店舗のマネージャーに対してタスク管理のアクセス許可をコンフィギュレーションするには、次の手順に従います。

1. **Retail と Commerce \> 従業員 \> アクセス許可グループ** に移動します。
1. 特定のアクセス許可グループ (たとえば、**マネージャー** など) を選択し、**編集** を選択します。
1. **アクセス許可** クイック タブで、**タスク管理を許可** オプションを **はい** に設定します。
1. **通知** クイック タブで **タスク管理** 操作を追加し、**表示順序** フィールドに値を入力します。 たとえば、**注文のフルフィルメント** 操作の **表示順序** がすでに **1** である場合、**2** を入力します。
    
> [!NOTE]
> マネージャー以外のペルソナに POS におけるタスク管理のアクセス許可がある場合、個々のユーザーにアクセス許可を付与できます。 または、マネージャー以外に対してアクセス許可グループを作成し、**タスク管理を許可** オプションを **はい** に設定することもできます。

次の図は、店舗のマネージャーに対してタスク管理のアクセス許可をコンフィギュレーションする方法を示しています。

![店舗のマネージャーに対するタスク管理のアクセス許可のコンフィギュレーション](media/HQ-POS-Tasks-Notifications-User-Permission.png)

## <a name="configure-permissions-for-employees"></a>従業員のアクセス許可のコンフィギュレーション

従業員がタスク リストの作成、割り当て基準の管理、および定期的なアイテムのタスク リストのコンフィギュレーションを行うには、アクセス許可が必要です。 これらのアクセス許可をコンフィギュレーションするには、従業員を **Retail タスク マネージャー** ロールに割り当てます。

従業員に対してアクセス許可をコンフィギュレーションするには、次の手順に従います。

1. **Retail と Commerce \> 従業員 \> ユーザー** へ移動します。
1. 従業員を選択します。
1. **ユーザーのロール** クイック タブで、**ロールの割り当て** をクリックします。
1. **ユーザーへのロールの割り当て** ダイアログ ボックスで **Retail タスク マネージャー** ロールを選択し、**OK** を選択します。

## <a name="distribute-permissions-to-pos-clients"></a>POS クライアントへのアクセス許可の配分

従業員が POS クライアントを使用できるようにする前に、それらのクライアントにアクセス許可を配分し、同期する必要があります。

POS クライアントにアクセス許可を配分するには、次の手順に従います。

1. **Retail とコマース \> Retail とコマース IT \> 配送スケジュール** の順に移動します。
1. **1060** (**スタッフ**) 配分スケジュールを選択し、**今すぐ実行** を選択します。
1. **1070** (**チャンルのコンフィギュレーション**) 配分スケジュールを選択し、**今すぐ実行** を選択します。

## <a name="configure-pos-notifications-for-tasks"></a>タスクの POS 通知のコンフィギュレーション

POS アプリケーションで通知を使用可能にするには、タスク管理をコンフィギュレーションする必要があります。

タスクに対して POS 通知をコンフィギュレーションするには、次の手順に従います。

1. **Retail および Commerce \> チャネル設定 \> POS 設定 \> POS \> POS 操作** に移動します。
1. **1400** (**タスク管理**) 操作を検索し、**通知の有効化** チェック ボックスをオンにします。

次の図は、**POS 操作** ページの **タスク管理** 操作を示しています。

![POS 操作ページのタスク管理操作](media/HQ-POS-Tasks-Notifications.png)

POS 通知をコンフィギュレーションする方法の詳細については、[販売時点管理 (POS) の注文通知の表示](notifications-pos.md) を参照してください。

## <a name="configure-the-tasks-tile-on-a-pos-application-home-page"></a>POS アプリケーションのホーム ページのタスク タイルのコンフィギュレーション

POS アプリケーションのホーム ページの **タスク** タイルをコンフィギュレーションする前に、POS 画面レイアウトへ新しいボタンのコンフィギュレーションおよび追加を行う方法の詳細について、[販売時点管理 (POS) の画面レイアウト](pos-screen-layouts.md) を参照してください。

POS アプリケーションのホーム ページの **タスク** タイルをコンフィギュレーションするには、次の手順に従います。

1. **Retail とコマース \> チャネル設定 \> POS 設定 \> POS \> 画面レイアウト** の順に移動します。
1. 画面レイアウトを選択し、レイアウト サイズを選択して、ボタン グリッドを選択します。
1. **ボタン グリッド** クイック タブで、**デザイナー** を選択して、選択したボタン グリッドを編集します。
1. ホーム ページの適切なセクションに **タスク** タイルを追加します。

次の図は、POS ホーム ページの **タスク** タイルの例を示しています。

![POS ホーム ページのタスク タイル](media/POS-home-screen-tasks-button-image.png)

## <a name="additional-resources"></a>追加リソース

[タスク管理の概要](task-mgmt-overview.md)

[タスク リストの作成およびタスクの追加](task-mgmt-create-lists.md)

[店舗または従業員へのタスク リストの割り当て](task-mgmt-assign-lists.md)

[POS におけるタスクの管理](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]