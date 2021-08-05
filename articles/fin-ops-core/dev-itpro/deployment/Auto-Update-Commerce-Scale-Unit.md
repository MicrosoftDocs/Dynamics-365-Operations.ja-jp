---
title: Commerce Scale Unit の自動更新 (クラウド)
description: このトピックでは、Commerce Scale Unit (クラウド) の自動更新について説明します。
author: AamirAllaq
manager: tonyafehr
ms.date: 07/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Retail, Operations
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2020-07-13
ms.dyn365.ops.version: 8
ms.openlocfilehash: fcc043bba3a9d93f7ca0e1b100a895a4caea191e
ms.sourcegitcommit: cef2986e24d0510957b5db742545c266dec4275c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/19/2021
ms.locfileid: "6645014"
---
# <a name="auto-update-for-commerce-scale-unit-cloud"></a>Commerce Scale Unit の自動更新 (クラウド)
[!include[banner](../includes/banner.md)]


現在、この機能はクラウドでホストされている Commerce Scale Unit に適用されます。 自己ホストされている Commerce Scale Unit は含まれていないので、自分で更新する必要があります。

Commerce Scale Unit の自動更新は、[1 つのバージョン](../lifecycle-services/oneversion-overview.md)の自動更新を有効にします。 Commerce Scale Unit の自動更新には、既存のすべての 1 つのバージョンのプロセス、ポリシー、およびスケジュールが適用されます。


>[!Note]
> Commerce Scale Unit の自動更新は段階的に顧客へリリースされ、2021 年度末までにすべての顧客が利用可能になる予定です。

## <a name="limitations"></a>制限
現在、次の制限が存在し、今後の更新プログラムで解決される予定です。

- アプリ内通知は使用できません。
- サンドボックス UAT 環境に複数の Commerce Scale Unit がある場合、その環境の最初の Commerce Scale Unit (アルファベット順) のみに基づいて Commerce Scale Unit の自動更新が行われます。 各サンドボックス UAT 環境の残りの Commerce Scale Unit は、自分で更新する必要があります。
- 現在、Commerce Scale Unit の自動更新は、初回リリースのお客様は利用できないため、プレビュー アーリー アクセス プログラム (PEAP) には適用できません。

## <a name="downtime-duration-and-impact"></a>ダウンタイム期間と影響

Commerce HQ および Commerce Scale Unit (クラウド) の更新プログラムは、順番に適用されます。 通常、ダウンタイム期間は 1 時間ですが、データ量や地域によって異なります。 実稼働環境でダウンタイム期間を見積もる場合、サンド ボックス UAT 環境の Commerce Scale Unit を自分で更新するか、または Commerce HQ と Lifecycle Services (LCS) の Commerce Scale Unit の両方の合計更新期間を確認することができます。

> [!NOTE]
> ダウンタイム期間は、各更新プログラムおよびデータ量によって異なります。 実際のダウンタイム期間を見積もる場合、サンドボックス UAT 環境に運用環境と同じデータがあることを確認してください。 これを行うには、[データベースの更新](../database/database-refresh.md)の手順に従います。 ダウンタイム期間の見積もりを行う予定のサンドボックス UAT 環境でも同じ更新プログラムを適用する必要があります。

冗長性の業務ニーズがある小売業者のため、Modern POS オフライン機能では、インターネットから切断中またはクラウド環境の更新中にコア POS 処理を使用できます。 Commerce Scale Unit を運用している店舗では、サポート クラウド メンテナンス期間中もコア POS 処理のサポートを伴う処理を継続します。 詳細については、[オンラインおよびオフライン販売時点管理 (POS) 処理](../../../commerce/pos-operations.md)を参照してください。

## <a name="version-support-and-backward-compatibility"></a>バージョンのサポートと下位互換性
店舗内のすべてのコンポーネントは、サポートを維持するために、12 か月以内にリリースされたソフトウェアを実行している必要があります。 ユーザーには、自己ホスト コンポーネントを更新し (店舗かプライベートで管理するデータ センターにインストールされているコンポーネントなど)、これらのコンポーネントのインストールされているバージョンが積極的にサポートされていることを確認する責任があります。

クラウドにホストされているコンポーネントの更新では、そのバージョンのリリース日から 12 か月間、小売業者によって自己ホストされるコンポーネント バージョンとの下位互換性が保持され続けます (店舗またはプライベート データ センターにインストールされているコンポーネントなど - Modern Point of Sale、Commerce Scale Unit、および Hardware Station)。 自己ホストされているコンポーネントは、クラウドでホストされているコンポーネントと同時に更新する必要はなく、独立したリズムで更新できるため、店舗に更新プログラムを展開する時間があります。

## <a name="updating-in-store-components"></a>店舗内コンポーネントを更新する
店舗ごとに手動で自己ホストされているコンポーネントを更新するか、Microsoft System Center Configuration Manager または Microsoft Intune などの一括更新ツールを使用するかを選択することができます。

Commerce Scale Unit の自動更新を使用して、店舗内コンポーネントに対する更新プログラムをフェーズ内で展開することができます。 これを実現するために、次のコントロールが使用可能です。

- **画面レイアウト デザイナー**: POS のほとんどのビジュアル要素は、顧客組織の管理ユーザーによって構成され、集中管理されます。 つまり、対応する画面レイアウトに含まれるように明示的に設定されていない限り、新しい POS の操作は POS に自動的に表示されません。 画面レイアウトは、画面レイアウト デザイナーを使用して構成され、店舗または POS デバイスに固有の場合があります。 詳細については、[POS ユーザー インターフェイスのビジュアル コンフィギュレーション](../../../commerce/pos-screen-layouts.md)を参照してください。
- **機能プロファイル、POS のアクセス許可、Commerce パラメーター** – POS 機能の要素の多くは通常、ユーザーがコンフィギュレーション可能です。 これは、機能プロファイル、POS のアクセス許可、Commerce パラメーター、または該当するシナリオにおけるデバイス、レジスター、店舗、またはユーザー レベルの機能の管理を可能にするその他のコントロールを通じて設定できます。
- **Modern POS および Commerce Scale Unit** – Modern POS および Commerce Scale Unit は小売業者によって自己ホストされるため、いずれかのコンポーネントを含むトポロジによっては、個別 (および低速) のリズムかつクラウド専用トポロジより細かい方法での更新の展開が可能になります。
- **機能のフラグ** - Commerce HQ で構成可能な機能のフラグの追加のコントロールにより、選択的に機能のオン/オフを切り替えることができます。
