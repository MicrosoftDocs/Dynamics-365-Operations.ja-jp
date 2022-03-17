---
title: 分散ハイブリッド トポロジのスケール ユニットを試す
description: このトピックでは、製造業や倉庫管理のワークロードを対象とした、クラウドとエッジのスケール ユニットの試用方法について説明します。
author: perlynne
ms.date: 03/03/2022
ms.topic: article
ms.search.form: ScaleUnitWorkloadsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-03-03
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 04fd79f3c582ae9ac51882f73410477efaa35496
ms.sourcegitcommit: b52ff5dfd32580121f74a5f262e5c2495e39d578
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2022
ms.locfileid: "8376246"
---
# <a name="try-out-scale-units-in-a-distributed-hybrid-topology"></a>分散ハイブリッド トポロジのスケール ユニットを試す

[!include [banner](../includes/banner.md)]

分散型ハイブリッド トポロジを試す手順は簡単です。 最初のステージでは、カスタマイズを検証して、分散トポロジで機能することを確認する必要があります。 これには 2 つのオプションがあります。

## <a name="option-1-evaluate-customizations-in-development-environments"></a>オプション 1: 開発環境でのカスタマイズを評価する

サンドボックス環境を導入する前に、ワンボックス環境 (Tier-1 環境) など開発環境でのスケールユニットを検討し、プロセス、カスタマイズ、ソリューションの検証を行うことをお勧めします。 このステージでは、データとカスタマイズが 1 ボックス環境に適用されます。 エンタープライズ ハブとスケール ユニットの両方の役割を担うことができ、1 つの環境で運用することができます。 また、開発環境を 2 つ用意し、一方をハブの役割、もう一方をスケール ユニットの役割とすることも可能です。 この設定によって、問題を特定して修正する最善の方法を提供します。 このステージを完了するために、最新の[早期アクセス (PEAP)](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxURUFWTjQzTzg0UUk5RkJHMDFEMVlSSDFEQy4u) ビルドも使用できます。

[1 ボックス開発環境用のスケール ユニット配置ツール](https://github.com/microsoft/SCMScaleUnitDevTools) を使用して、環境のインストールと保守を行う必要があります。 これらのツールにより、1 つまたは 2 つのワンボックス環境でハブとスケール ユニットを構成することができます。 このツールは、バイナリ リリースとソースコードの両方を GitHub で提供しています。 ツールの使用方法を説明した[ステップ バイ ステップの使用ガイド](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide) が掲載されているプロジェクトの Wiki をご覧ください。 [ローカル業務データ (LBD) を使用してカスタム ハードウェアにエッジ スケール ユニットを配置する場合は](cloud-edge-edge-scale-units-lbd.md)、別のプロセスに従う必要があります。

## <a name="option-2-acquire-add-ins-and-deploy-in-your-sandbox-environments"></a>オプション 2: アドインを入手し、サンドボックス環境に配置する

分散ハイブリッド トポロジを試すには、2 つのサンドボックス環境 (tier 2) を用意する必要があります。1 つはお客様のデータ (エンタープライズ ハブ)、もう 1 つはスケール ユニット用で、「空のデータ」 が入っているものです。

少なくとも 1 つのクラウドまたはエッジ スケール単位でアドインを取得する必要があります。 [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/) にはプロジェクトと環境の対応するスロットが付与され、[スケール ユニット マネージャ ポータル](https://aka.ms/SCMSUM) を利用してスケール単位の環境を展開できるようになります。

マイクロソフトのサポートに連絡して、サンドボックス環境を有効にするように要請してください。

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
