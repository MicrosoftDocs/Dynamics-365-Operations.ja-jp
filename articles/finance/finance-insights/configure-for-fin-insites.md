---
title: Finance Insights の構成
description: このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ec7e6a7e616e239128281ba669c8bbbfc5e3c7a
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710617"
---
# <a name="configuration-for-finance-insights"></a>Finance Insights の構成

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights では、Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、組織に強力な予測ツールを提供します。 このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。 このトピックの手順を正しく実行するには、[Power Portal 管理センター](https://admin.powerplatform.microsoft.com/)のシステム管理者とシステム カスタマイザー、Dynamics 365 Finance におけるシステム管理者アクセス権、および Microsoft Dynamics Lifecycle Services (LCS) の環境作成アクセス権が必要です。

> [!NOTE]
> 次の Finance Insights の設定方法は、Dynamics 365 Finance バージョン 10.0.21 以降で有効です。

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance のデプロイ

環境をデプロイするには、これらの手順に従います。

1. LCS で、Dynamics 365 Finance 環境を作成または更新します。 この環境では、アプリのバージョン 10.0.21 以降が必要です。

    > [!NOTE]
    > この環境は、高可用性 (HA) 環境である必要があります。 (このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。

2. サンドボックス環境で Finance insights を構成している場合は、予測を機能させる前に、本番データをその環境にコピーする必要がある場合があります。 予測モデルでは、複数年分のデータを用いて予測値を構築します。 Contoso のデモ データには、予測モデルを適切にトレーニングさせるだけの十分な過去のデータが含まれていません。 

## <a name="configure-your-azure-ad-tenant"></a>Azure AD テナントの構成

Azure Active Directory (Azure AD) は、Dataverse および Microsoft Power Platform のアプリケーションで使用できるように構成する必要があります。 この構成では、LCSの **プロジェクト セキュリティ ロール** フィールドで **プロジェクト所有者** ロールまたは **環境マネージャ** ロールがユーザーに割り当てられている必要があります。

次の設定が完了していることを確認します:

- **システム管理者** および **システム カスタマイザー** のアクセスが Power Portal 管理センターにある。
- Dynamics 365 Finance または同等のライセンスが、Finance Insights アドインをインストールするユーザーに適用されている。

以下の Azure AD アプリが Azure AD に登録されています。

|  申請書                             | アプリ ID                               |
|------------------------------------------|--------------------------------------|
| Microsoft Dynamics ERP マイクロサービス CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    
## <a name="configure-dataverse"></a>Dataverse のコンフィギュレーション

以下の手順で、Finance insights に Dataverse を構成します。

- LCS で、環境のページを開き、**Power Platform 統合** のセクションがすでに設定されていることを確認します。

    - Dataverse が既に設定されている場合、Finance 環境にリンクされている Dataverse の環境名が表示されます。
    - Dataverse がまだ設定されていない場合は、**設定** を選択します。 Dataverse 環境の設定には 1 時間ほどかかる場合があります。 設定が正常に完了すると、Finance 環境にリンクされている Dataverse の環境名が表示されます。
    - この統合が既存の Microsoft Power Platform 環境で設定されている場合は、リンクされた環境が無効な状態でないことを管理者に確認してください。

        詳細については、[Power Platform 統合の有効化](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) を参照してください。 

        Microsoft Power Platform 管理者サイトを開くには、<https://admin.powerplatform.microsoft.com/environments> へ移動します。

## <a name="configure-the-finance-insights-add-in"></a>Finance Insights アドインの構成

既に Finance Insights アドインをインストールしていた場合は、アンインストールしてから次の手順を実行してください。

> [!NOTE]
> LCS にデータ レイク アドイン データを既にインストールしている場合、Finance Insights がそれを使用して予測に必要なデータを保存します。 LCS にデータ レイク アドインをまだインストールしていない場合、Finance Insights アドインが、マネージド データ ファイルを自動的に作成します。

以下の手順で Finance insights アドインをインストールします。

1. LCS にログインし、ページの右側にある環境名の下の **完全な詳細** を選択し ます。
2. **環境アドイン** セクションで、**新しいアドインのインストール** を選択します。
3. **Finance insights** アドインを選択します。
4. 契約条件に合意し、**インストール** を選択します。

アドインのインストールに数分かかる場合があります。

## <a name="one-last-thing"></a>最後の注意点...

アドインが正常にインストールされた後、Dynamics 365 Finance の **機能管理** ワークスペースで Finance Insights 機能を有効にできるようになるまで最大 1 時間かかる可能性があります。 待てない場合は、**Insights のプロビジョニング状態の確認** プロセスを手動で実行できます。 

1. Dynamics 365 Finance で、**システム管理 \> 設定 \> プロセスの自動化** の順に移動します。
2. **バックグラウンド プロセス** タブで、**Insights のプロビジョニング状態の確認** を見つけて、**編集** を選択します。
3. **次の実行** フィールドを現在の時刻の 30 分前に設定します。

   この変更により、**Insights のプロビジョニング状態の確認プロセス** が直ちに実行されます。

   **Insights のプロビジョニング状態の確認** プロセスが正常に実行された後、**機能管理** ワークスペースで Finance Insights 機能を有効にできます。

> [!NOTE]
> **Insights のプロビジョニング状態の確認** プロセスが実行しない場合は、**システム管理** > **照会** > **バッチ ジョブ** にアクセスします。 **プロセス 自動化ポーリング システム** フィールドで、プロセスを開始するために値を **待機中** に変更します。 
> 
## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックに興味のある方、サポートが必要な方は、[Finance insights (プレビュー)](mailto:fiap@microsoft.com) にメールでお問い合わせください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
