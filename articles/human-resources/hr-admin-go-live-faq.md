---
title: Go-Live に関するよく寄せられる質問
description: このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ca6c89f5f6dc4660a77587112526a6516f683f64ce95a9a83f39add119d2ee12
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731398"
---
# <a name="go-live-faq"></a>Go-Live に関するよく寄せられる質問 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

このトピックでは、Dynamics 365 Human Resources 実装プロジェクトの Go-Live についてよく寄せられる質問を一覧表示します。 

## <a name="when-can-i-configure-and-request-my-production-environment"></a>実稼働環境をいつ構成および要求できますか ? 

一般に、次の基準を満たすことによって、運用環境が展開されます :

- すべてのカスタマイズのコードが完了していること。
- ユーザー受け入れテスト (UAT) が完了していること。
- 顧客がソリューションと UAT にサインオフしている。
- Go-live にあたってブロッキングの問題がないこと。 

対象の顧客がこの段階にある場合、Microsoft FastTrack チームはプロジェクトチームと協力して Go-live の評価を行います。 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a>運用環境を展開するための前提条件 

前提条件の一覧については、  [Go-Live の準備](hr-admin-go-live-prepare.md) を参照してください。 

## <a name="what-is-a-go-live-assessment"></a>運用運用に関する評価について  

Go-live 評価/レビューは、 [Microsoft FastTrack プログラム](/dynamics365/fasttrack/)の一部です。 レビュー中に、ソリューション アーキテクトは、実装プロジェクトが成功した切替および Go-live の準備が整っているかどうかを評価します。 このレビューは、実稼働環境で準備を開始する前に、すべての実装プロジェクトで必須です。 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a>当社のサンドボックス環境は、米国中部のデータセンターに配置されています。 運用環境を米国西部のデータセンターに展開したいと考えています。 運用環境の構成で、データ センターに米国西部を選択できますか？ 

LCS は、人事環境を導入する際に異なるデータセンターを選択することを制限しませんが、異なるデータセンターを選択しないことを強くお勧めします。  

運用環境を米国西部のデータセンターに配置するには、まずサンドボックス環境を米国西部のデータセンターに再展開してテストし、サインオフする必要があります。 

適切なデータセンターを選択する方法については、[ネットワーク要件](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements)を参照してください。 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a>人事環境では、Azureリソースに対してどのレベルのアクセス許可が必要ですか？  

人事環境へのアクセスは制限されています。 仮想マシン (VM) または Microsoft インターネット インフォメーション サービス (IIS) にアクセスすることはできません。 また、Microsoft SQL Server Management Studio 経由でデータベースにアクセスすることはできません。 

Azureリソースや Dynamics 365 Human Resources 環境に直接アクセスすることはできませんが 、データへのアクセスに使用できる追加機能があります。

- Azure SQL データベースを独自の Azure テナントに展開し、BYOD (Bring Your Own Device) 機能を使用してデータを同期させることができます。 詳細については、[独自のデータベースを導入する (byod)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)を参照してください。

- Dataverse の統合を使用して、選択したエンティティを Dataverse データベースに同期することができます。 詳細については、[Dataverse の表](hr-developer-entities.md)を参照してください。 

## <a name="how-often-is-my-production-database-backed-up"></a>どのくらいの頻度で生産データベースがバックアップされますか。 

データベースは、以下の頻度で自動バックアップで保護されます :

| バックアップのタイプ | 頻度 |
| --- | --- |
| データベースのフル バックアップ | 毎週 |
| データベースの差分バックアップ | 12 - 24 時間ごと |
| トランザクション ログのバックアップ | 5 - 10 分ごと |

マイクロソフトでは、過去 14 日間において、ポイントインタイム リストア (PITR) を可能にする十分なバックアップが保持されています。 

詳細については、 [SQL Database の自動バックアップについて](/azure/azure-sql/database/automated-backups-overview?tabs=single-database) を参照してください。 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a>生産データベースのバックアップのコピーを要求できますか。 

No. ただし、運用環境をサンドボックス環境にコピーするデータベースの更新サービス リクエストを送信することはできます。 Azure SQL データベースを独自の Azure テナントに展開し、BYOD 機能を使用して運用環境からデータを同期させることができます。 詳細については、[独自のデータベースを導入する (byod)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md)を参照してください。 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a>サンドボックス環境を運用稼働環境に移行する方法について 

環境をサンドボックスから運用環境に移動するコピー機能は使用できないため、データパッケージを使用してデータを運用環境に移動する必要があります。  

プロジェクト全体にわたってサンドボックスで構成されているエンティティの一覧を明確にしておくことをお勧めします。 次に、go-live に必要なデータパッケージのカットオーバーと移行のプロセスをテストします。 運用環境の準備ができたら、データパッケージを手動で運用環境に移行する必要があります。 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a>運用環境がダウンした場合の対応について 

運用環境の稼働不能状態を報告するには、  [稼働停止のレポート](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md) で説明されているプロセスに従います。 

 ## <a name="see-also"></a>参照

 [Go-Live の準備](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]