---
title: Finance Insights の構成
description: このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。
author: ShivamPandey-msft
ms.date: 1/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 5668d3ddff777645b4f1c6608f025d0c5a63208a
ms.sourcegitcommit: 03fa7556840aa59f825697f6f9edeb58ea673fca
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/04/2021
ms.locfileid: "7752981"
---
# <a name="configuration-for-finance-insights"></a>Finance Insights の構成

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance insights では、Dataverse を使用した Microsoft Dynamics 365 Finance、Azure、AI Builder の機能を組み合わせて、強力な予測ツールを提供します。 このトピックでは、Finance Insights で使用できる機能をシステムで使用できるようにするための構成手順について説明します。 このトピックの手順を正しく実行するには、[Power Portal 管理センター](https://admin.powerplatform.microsoft.com/)のシステム管理者とシステム カスタマイザー、Dynamics 365 Finance におけるシステム管理者アクセス権、および Microsoft Dynamics Lifecycle Services (LCS) の環境作成アクセス権が必要です。

> [!NOTE]
> 次の Finance Insights の設定方法は、Dynamics 365 Finance バージョン 10.0.21 以降で有効です。

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance のデプロイ

環境をデプロイするには、これらの手順に従います。

1. LCS で、Dynamics 365 Finance 環境を作成または更新します。 この環境では、アプリのバージョン 10.0.21 以降が必要です。

    > [!NOTE]
    > この環境は、高可用性 (HA) 環境である必要があります。 (このタイプの環境は、Tier 2 環境とも呼ばれます)。詳細については、[環境の計画](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md)を参照してください。

2. サンドボックス環境で Finance insights を構成している場合は、予測を機能させる前に、本番データをその環境にコピーする必要がある場合があります。 予測モデルでは、複数年分のデータを用いて予測値を構築します。 Contoso のデモ データには、予測モデルを適切にトレーニングさせるだけの十分な過去のデータが含まれていません。 

## <a name="configure-dataverse"></a>Dataverse のコンフィギュレーション

以下の手順で、Finance insights に Dataverse を構成します。

- LCS で、環境のページを開き、**Power Platform 統合** のセクションがすでに設定されていることを確認します。

    - 既に設定されている場合、 Finance 環境にリンクされている Dataverse の環境名が表示されます。
    - まだ設定されていない場合は、**設定** を選択します。 Dataverse 環境の設定には最大で 1 時間ほどかかる場合があります。 設定が正常に完了している場合、Finance 環境にリンクされている Dataverse の環境名が表示されます。

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

## <a name="feedback-and-support"></a>フィードバックとサポート

フィードバックに興味のある方、サポートが必要な方は、[Finance insights (プレビュー)](mailto:fiap@microsoft.com) にメールでお問い合わせください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
