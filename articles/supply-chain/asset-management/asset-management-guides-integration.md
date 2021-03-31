---
title: Dynamics 365 Supply Chain Management（資産管理）と Dynamics 365 Guides を統合する
description: このトピックでは、Microsoft Dynamics 365 Supply Chain Management の資産管理モジュールを Dynamics 365 Guides に統合して、日々のサービスやメンテナンスのワークフローで Mixed Reality ガイドを活用する方法について説明します。
author: kamaybac
manager: tfehr
ms.date: 04/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2020-04-28
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: e3e9e74397faec12f6eecff1f562fd9d731ac5e2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230155"
---
# <a name="integrate-dynamics-365-supply-chain-management-asset-management-with-dynamics-365-guides"></a>Dynamics 365 Supply Chain Management（資産管理）と Dynamics 365 Guides を統合する

Dynamics 365 Supply Chain Management の **資産管理** モジュールを Microsoft Dynamics 365 Guides に統合することで、日々のサービスやメンテナンスのワークフローで、Mixed Reality ガイドを活用することができます。 ガイドが資産管理の作業指示に関連付けられている場合、Supply Chain Management（Dynamics 365）モバイル アプリで作業指示のメンテナンス チェック リストを開いた作業員は、ガイドが利用可能であることを確認してください。 続いて、作業者は Dynamics 365 Guides HoloLens アプリでガイドを検索して開いてください。

## <a name="prerequisites"></a>必要条件

資産管理ワークオーダーにガイドを適用するには、次の前提条件を実行する必要があります：

- [Dynamics 365 Supply Chain Management の設定](../../fin-ops-core/fin-ops/index.md) バージョン 10.0.9 またはそれ以降。
- [Supply Chain Management アプリに対してデュアル書き込みを有効化します](../../fin-ops-core/dev-itpro/data-entities/dual-write/enable-dual-write.md)。
- **MRGuidesFeature** 機能の [フライトを有効](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md#features-flighted-in-data-management-and-enabling-flighted-features) にします。 （実稼働環境の場合は、最初にサポート チケットを送信して、テナントを flighting グループに追加する必要があります。）
- **ライセンスの構成** ページで、[次の構成キーを有効にします](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/license-code-and-configuration-key-reference)：

    - 資産管理 \> 資産管理の Mixed Reality
    - Mixed reality \> Mixed reality ガイド

- [Dynamics 365 Guides の設定](https://docs.microsoft.com/dynamics365/mixed-reality/guides/setup#step-2-create-a-common-data-service-environment-and-install-the-dynamics-365-guides-solution) バージョン 200.0.0.96 またはそれ以降。

## <a name="use-dynamics-365-guides-with-asset-management"></a>Dynamics 365 Guides と資産管理を併用する

ガイドを関連付けるには、資産管理のメンテナンス チェックリストの行を使用します。 メンテナンス チェックリストのテンプレート、メンテナンス作業タイプは、3つともメンテナンス チェックリストの行が含まれているため、作業指示書を使って関連付けを行うことができます。 テンプレートは、それを使用するすべてのメンテナンス作業タイプに関連付けることができるため、テンプレートを使用して時間を節約できます。 たとえば、メンテナンス作業タイプに関連付けられているガイドは、その作業タイプを指定するすべての作業指示書に自動的に関連付けられます。 一方、作業指示書に直接関連付けられているガイドは、その作業指示書にしか存在しません。

### <a name="associate-a-guide-with-a-maintenance-checklist-template"></a>メンテナンス チェックリストのテンプレートをガイドに関連付ける

メンテナンス チェックリストのテンプレートをガイドに関連付けるには、次の手順に従ってください。

1. Dynamics 365 Guides PC と HoloLens アプリを使用してガイドを作成します。 ガイドの作成方法については、以下のトピックを参照してください：

    - [PC アプリを使用してガイドを作成する](https://docs.microsoft.com/dynamics365/mixed-reality/guides/pc-app-overview)
    - [HoloLens アプリを使用してホログラムを配置します](https://docs.microsoft.com/dynamics365/mixed-reality/guides/hololens-app-overview)

1. Supply Chain Management で、[メンテナンス チェックリストのテンプレートを作成](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-checklist-template) します。
1. 新しいメンテナンス チェックリストで、作成したガイドとメンテナンス チェックリストの明細を関連付けます。

    1. **メンテナンス チェックリスト** のクイックタブで、ガイドを関連付ける明細行を選択します。
    1. **関連するガイド** のクイックタブで、**ガイドの追加** を選択します。

        ![メンテナンス チェックリストのテンプレートをガイドに関連付ける](media/am-guides-integration-add-guide.png "メンテナンス チェックリストのテンプレートをガイドに関連付ける")

    1. **名前** フィールドで、ガイドを選択し、**保存** を選択します。

        ![名前フィールドでガイドを選択します](media/am-guides-integration-select-guide.png "名前フィールドでガイドを選択します")

1. メンテナンス チェックリストのテンプレートを作業タイプに関連付ける：

    1. [メンテナンス作業タイプを作成する](setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md#create-a-maintenance-job-type)か、既存のメンテナンス作業タイプを選択します。
    1. アクション ウィンドウで、**メンテナンス作業タイプの既定値** を選択します。

        ![メンテナンス作業タイプの既定値のページ](media/am-guides-integration-job-defaults.png "メンテナンス作業タイプの既定値のページ")

    1. 行を作成し、**保存** を選択します。

        ![行の作成](media/am-guides-integration-add-line.png "行の作成を行います") を行います

    1. アクション ウィンドウで、**メンテナンス チェックリスト** を選択します。

        ![メンテナンス チェックリスト ボタン](media/am-guides-integration-maintenance-checklist.png "メンテナンス チェックリスト ボタン")

    1. **メンテナンス チェックリスト** のクイックタブで、行を追加し、**タイプ** フィールドの値を **テンプレート** に変更し ます。

        ![種別の値を変更する](media/am-guides-integration-checklist-lines.png "種別の値を変更する")

    1. **行の詳細** クイックタブの **テンプレート** フィールドで、ガイドを関連付けたテンプレートを選択し、**保存** を選択します。

        ![テンプレートを選択します](media/am-guides-integration-checklist-line-details.png "テンプレートを選択します")

1. [作業指示書を作成](work-orders/manually-created-workorders.md#create-work-order) し、ガイドに関連付けられているメンテナンス チェックリストのテンプレートを使用するメンテナンス作業タイプを選択します。 ガイドが自動的に作業指示書に関連付けられます。

    ![メンテナンス作業タイプを選択する](media/am-guides-integration-create-work-order.png "メンテナンス作業タイプを選択する")

1. 作業指示書と作業者に関連付けられているガイドを表示します。

    1. [資産管理のモバイル ワークスペース](asset-management-mobile-workspace.md) を開いて、作業指示書にアクセスします。
    1. 作業指示書の [メンテナンス チェックリストを開きます](asset-management-mobile-workspace.md#view-maintenance-checklist-on-a-work-order-job)。
    1. チェックリストの明細行を選択して、関連するガイドを表示します。

        ![チェックリスト明細行に関連付けられているガイド](media/am-guides-integration-show-guide.png "チェックリスト明細行に関連付けられているガイド")

    1. HoloLens のガイドを開きます。

        ![HoloLens のガイドを開く](media/am-guides-integration-hololens-select.png "HoloLens のガイドを開きます")

> [!NOTE]
> また、作業指示書や作業タイプのメンテナンス チェックリストにガイドを直接関連付けることもできます。

> [!IMPORTANT]
> メンテナンス チェックリストのテンプレートを既定のメンテナンス作業タイプに関連付けた場合、そのテンプレートにリンクされているガイドは、 **メンテナンス ジョブ タイプの既定値 ページの **関連するガイド** クイックタブには表示されません**。 ただし、**関連するガイド** のクイックタブでは、その作業タイプが作業指示に適用された後にこのガイドが表示されます。

## <a name="see-also"></a>参照

- [二重書き込みの概要](../../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview.md)
- [資産管理の概要](index.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]