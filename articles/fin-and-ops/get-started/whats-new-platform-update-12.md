---
title: Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 の新機能または変更された機能について説明します。 このバージョンは 2017 年 11 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: tfehr
ms.search.scope: Operations
ms.custom: ''
ms.assetid: e577d51d-42d2-47c5-b388-93c8219c692a
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-09-30
ms.dyn365.ops.version: Platform update 12
ms.openlocfilehash: a38085c75e070b71dcd81c16c293fd154833297f
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510858"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-12-november-2017"></a>Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 (2017 年 11 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations, Enterprise Edition プラットフォーム更新プログラム 12 の新機能または変更された機能について説明します。 このバージョンは 2017 年 11 月にリリースされ、ビルド番号は 7.0.4709 です。

新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。 プラットフォーム更新プログラム 12 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=863949) を参照してください。

## <a name="browser-client--discover-and-learn-currently-available-keyboard-shortcuts"></a>ブラウザー クライアント - 現在利用可能なキーボード ショートカットを見つけて学ぶ

キーボード ショートカットの説明書を検索する必要がなくなりました。 代わりに、ユーザー インターフェイスから直接、現在利用可能なキーボード ショートカットを見つけることができるようになりました。 コントロールを右クリックし、**ショートカットの表示** を選択します。 これにより、ページの場所に応じて使用できるショートカットが一覧表示されたダイアログボックスが開きます。 

詳細については、「[キーボード ショートカット](shortcut-keys.md)」を参照してください。

## <a name="development-and-build-environments-in-a-customer-lcs-implementation-project-are-monitored-and-managed-by-microsoft"></a>顧客の LCS 実装プロジェクトの開発環境とビルド環境は、Microsoft によって監視および管理されています。

お客様が Finance and Operations の運用または実装を行っている顧客の場合、開発、テスト、および運用を有効にする環境のセットが提供されます。 サンドボックス (階層 2) と実稼働環境は、Microsoft によって管理されていますが、IT スタッフが開発者とビルド環境の管理を担当します。 この機能では、開発者および開発者環境およびビルド環境を含む、Microsoft サブスクリプションで実行中の Lifecycle Services (LCS) 実装プロジェクト内のすべての環境が、Microsoft によりモニターおよび管理されます。 これにより、IT スタッフは、セキュリティ パッチの適用やこれらの環境への更新など、セキュリティの監視と管理を行う必要がなくなります。 これは、オンプレミスまたは顧客またはパートナーの Microsoft Azure サブスクリプションで実行される開発環境およびビルド環境には影響しません。

開発者が実行する開発およびアプリケーション管理タスクは、開発仮想マシン (VM) のローカル管理者権限を必要とせずに実行できます。 顧客は、Microsoft のサブスクリプションで実行されている開発環境およびビルド環境の VM 管理者アカウントにアクセスすることはできません。

詳細については、この LCS ブログ トピック、[制限された管理者のアクセス](https://blogs.msdn.microsoft.com/lcs/2017/10/31/restricted-admin-access-with-platform-12-updates/) を参照してください。

## <a name="enabling-sql-triggers-in-bring-your-own-database-byod"></a>「独自のデータベースを戻す」 (BYOD) で、SQL トリガーを有効にします。

BYOD とも呼ばれる「自分のデータベースの持ち込み」機能により Dynamics 365 for Finance and Operations から 独自の SQL Azure データベースに段階的にデータ エンティティをエクスポートできます。 現時点で、出力先データベースに SQL データベース トリガーがある場合、BYOD プロセスは効率的なバルク データ転送を有効にするためにトリガーをバイパスします。

エクスポートされたデータまたは BYOD のために、独自のデータベースで SQL データベース トリガーを使用できるようになりました。 これにより、下流のプロセスが BYOD プロセスと容易に統合できるようになります。

## <a name="export-b2b-users-to-azure-ad"></a>B2B ユーザーの Azure AD へのエクスポート

企業間 (B2B) ユーザーを Azure Active Directory (Azure AD) に自動的にエクスポートすることができます。

過去には、B2B ユーザーは .csv ファイルに手動でエクスポートされていました。 その後、Azure AD テナントの管理者は、このファイルを使用して Azure ポータルを使用してユーザーを Azure AD に手動で追加する必要があります。

自動エクスポート機能を有効にするには、ワンタイム設定と構成プロセスを完了する必要があります。 このプロセスが完了したら、新しいユーザーのプロビジョニング ワークフロー タスクを使用して、Azure AD に B2B ユーザーを自動的にエクスポートできます。

1回限りの設定とコンフィギュレーションでは、次のことが必要になります。

- Azure AD で B2B 招待サービス アプリケーションを設定します。
- Finance and Operations で B2B 招待サービスの設定のコンフィギュレーションをします。

詳細については、[Azure AD に B2B ユーザーをエクスポート](../../dev-itpro/sysadmin/implement-b2b.md)を参照してください。

## <a name="personalizations-can-easily-be-shared-with-one-or-more-roles-in-your-organization"></a>個人用設定は、組織の 1 つまたは複数の役割と簡単に共有できます。

個人用設定機能では、ラベルの名前を変更する、コントロールを追加、移動、非表示にする、サイズを変更する、アプリケーション全体のフォームでグリッド列を追加または並べ替えるなど、ユーザー インターフェイスに変更を加えることができます。 個人用設定では、エンド ユーザーが、アプリケーション内と Power BI のコンテンツを示す新しいワークスペースを作成することが可能です。 これらの機能により、アプリケーションのカスタマイズを行う必要性が減り、代わりにユーザーが必要なユーザー インターフェイスを最初から作成したり、既製のコンテンツを修正して作成することができます。

管理者は、ユーザーが行った個人用設定をエクスポートする機能を既に持っており、インポート プロセスを使用して組織内のロールに適用します。 パーソナル化をインポートすることなく、管理者がパーソナル化管理フォームからパーソナル化を他のユーザーと共有できるようにすることで簡素化されます。

また、この機能により、管理者は個人用設定を適用する方法をより細かく制御できます。 既存の個人用設定を置き換えるのではなく、管理者は任意で既存の個人用設定に新しい個人用設定を追加することを選択できます。

## <a name="reporting-document-routing-agent-scale-improvements"></a>レポート: ドキュメント回覧エージェントのスケールの強化

ドキュメント回覧エージェントは、さらにネットワーク プリンター デバイスをサポートできるように拡張されています。 最大 50 のネットワーク プリンターをサポートする機能により、クライアントは一般的な印刷作業負荷を処理するための準備ができています。 インテリジェントなドキュメント キュー管理を活用する最新のプラットフォーム更新プログラムを展開した後、ドキュメント回覧エージェントをアップグレードするだけです。

> [!NOTE]
> 最新バージョンのドキュメント ルーティング エージェントを、会社のドメインでホストされているローカルのプリント サーバーに配置するには、次のインストールの指示を参照してください。[プリンター デバイスを有効にするためにドキュメント ルーティング エージェントをインストールする](../../dev-itpro/analytics/install-document-routing-agent.md)。

## <a name="table-extension--previewpartref-property"></a>テーブル拡張 - PreviewPartRef プロパティ

このリリースには、テーブル拡張を介して **PreviewPartRef** プロパティの値を変更する機能が含まれています。 この機能を使用すると、TMSRoute のプレビューの強化など、既存へのプレビューを強化できます。
