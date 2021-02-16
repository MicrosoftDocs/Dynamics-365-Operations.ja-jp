---
title: Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 8 (2017 年 6 月) の新機能および変更された機能
description: このトピックでは、Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 8 の新機能または変更された機能について説明します。 このバージョンは 2017 年 6 月にリリースされました。
author: tonyafehr
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Developer, IT Pro
ms.reviewer: josaw
ms.custom: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 89ff3d9779967129d6e558e6d0e53c75cdd10d47
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4693126"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-finance-and-operations-enterprise-edition-platform-update-8-june-2017"></a>Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 8 (2017 年 6 月) の新機能および変更された機能

[!include [banner](../includes/banner.md)]

このトピックでは、Dynamics 365 for Finance and Operations Enterprise Edition プラットフォーム更新プログラム 8 の新機能または変更された機能について説明します。 このバージョンは 2017 年 6 月にリリースされ、ビルド番号は 7.0.4565.16212 です。

> [!NOTE]
> 現在、Dynamics 365 for Operations (オンプレミス) の名前は変更されています。 通信およびライセンス ガイド全体で参照される Dynamics 365 for Operations (オンプレミス) が表示されます。 製品を展開する際に表示される製品名は、Dynamics 365 for Finance and Operations Enterprise Edition です。 これらの名前はどちらも同じ製品を指しています。

新機能についての補足情報の検索および開発中の新機能に関する詳細については、[Dynamics 365 ロードマップ](https://roadmap.dynamics.com/) を参照してください。 プラットフォーム更新プログラム 8 に含まれるバグ修正の詳細については、Lifecycle Services (LCS) にログインし、この [サポート技術情報記事](https://go.microsoft.com/fwlink/?linkid=852224) を参照してください。

## <a name="introducing-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Dynamics 365 for Finance and Operations Enterprise Edition を含みます

ユーザーと開発者に対して、更新された製品名 ("Microsoft Dynamics 365 for Finance and Operations Enterprise Edition") と製品アイコンが Web クライアントに表示されます。 一部のプラットフォームのコンポーネント (たとえば、開発者ツールおよびモバイル アプリケーション) によって共有される Dynamics 365 for Finance and Operations、Dynamics 365 for Retail、および Dynamics 365 Human Resources は、"Dynamics 365 Unified Operations." と表示されるようになりました。

## <a name="development-and-customization--changing-the-extended-data-type-edt-on-a-table-field-using-table-extensions"></a>開発およびカスタマイズ - テーブル拡張を使用してテーブル フィールドの拡張データ タイプ (EDT) を変更する

開発者は、テーブル拡張機能を使用して、テーブル フィールドの **拡張データ型** (EDT) プロパティを変更できます。 開発者は、現在のものから派生した EDT のみを選択できます。 詳細については、[拡張機能およびオーバーレイによるカスタマイズ](../../dev-itpro/extensibility/customization-overlayering-extensions.md)を参照してください。

## <a name="improved-viewing-experience-for-application-reports"></a>アプリケーション レポートの表示エクスペリエンスの強化

Dynamics 365 for Finance and Operations Enterprise Edition の分析レポートおよび運用レポートとやり取りする際、顧客にとって改善された新しい表示エクスペリエンスがあります。 この変更により、PDF ファイルとしてレンダリングされるか、プリンタに直接送信されるときに生成されるドキュメントの簡素化されたツールバーとクリア プレビューが提供されます。 現在までに、顧客は SQL Server Reporting Services (SSRS) によって 110 万件以上のドキュメント レポートを作成しています。 さらに、Dynamics 365 for Finance and Operations Enterprise Edition (2017 年 7 月) には、Power BI Desktop を使用して作成された 20 以上の分析レポートが含まれています。 この機能は、ドキュメントと分析スタイルのアプリケーション レポートの両方と対話しながら、大幅に強化された表示エクスペリエンスを提供します。
顧客のメリット。

- **信頼性** - 顧客には、ドキュメントがプリンターに直接送信されたときの出力と一致するビューが表示されるようになりました。 直接のフィードバックに基づいて、画面上でレポートを表示する最も一般的なユース ケースは他のユーザーと共有される出力をプレビューすることです。ほとんどの場合、電子メールが使用されます。 現在、税金は SSRS によって作成された文書により合致するスクリーン表記に依存して利用できます。
- **シンプルさ** - ユーザーは、比較的小さな画面のモバイル デバイスを使用してアプリケーション レポートを十分に操作できます。 これらのデバイスでは、画面のインチ間隔が重要です。 ページ キャプションを削除することで、ユーザーにとってアプリケーション レポートを表示したり操作するための画面スペースがより広くなります。

## <a name="table-browser-is-now-in-read-only-mode"></a>テーブル ブラウザーが読み取り専用モードになりました

ランタイム環境 (サンドボックス Tier-2 および実稼働) でテーブル ブラウザー フォームが読み取り専用モードになりました。

開発者が開発環境でテスト データをすばやく作成して編集できるように、テーブル ブラウザー フォームが設計されています。 これはランタイム環境でシステム管理者にも使用できました。 現在のプラットフォーム更新プログラム 8 では、システム管理者はランタイム環境で読み取り専用モードでのみテーブル ブラウザにアクセスできます。これは、システム管理者が稼働中のシステム データを誤って編集したり削除したりしたときに、人為的なエラーが発生したことを受けての対応です。

## <a name="deployment-option-on-premises"></a>配置オプション (オンプレミス)

組織によっては、クラウドに自社のミッション クリティカルなデータを格納する準備ができていません。 この要件は、多くの場合、業界の規制、国または地理的なクラウドの採用、最近のデータセンターへの投資、または組織のエンタープライズ標準によるものです。 これらの顧客については、クラウドに格納する、業務データを必要としない新しい配置オプションについてお知らせできるのをうれしく思います。

この展開オプションは、を Microsoft クラウドに複製することなく、社内のビジネス プロセスの実行、ローカル トランザクションのサポート、ローカルの格納をサポートします。 そのような場合、Microsoft クラウド (クラウドとエッジのシナリオで参照) での業務データの一般的なレプリケーションはオフになります。

データのクラウド同期により、Microsoft は業務プロセスにインテリジェンスを組み込むことができます。埋め込まれた分析、機械学習、および広範囲の機能は、Microsoft クラウドで最も効果的に提供されます。 このオプションでは、顧客はビジネス データのクラウド同期をオンまたはオフにするオプションを選択できるようになりました。 顧客がクラウド同期をオフにしている場合、業務データにその受託者の境界が残ることはありません。 また、クラウド データ同期がオフになっている場合、埋め込み Power BI、集計ビュー、Azure Machine Learning などの関数は使用できません。 顧客は、クラウドへのデータ同期をオンにするだけで、組み込みインテリジェンス機能を利用することができます。

オンプレミス ビジネス データおよびクラウド データ同期の両方の環境はクラウド + Edge 配置オプションと呼ばれます。 これらのオプションの相違をより詳しく比較するには、表を参照してください。

診断、監視、使用状況の遠隔測定、および生産の更新など、クラウド ベースのアプリケーション ライフ サイクル管理 (ALM) 機能は、Microsoft Dynamics Lifecycle Services (LCS) を通じて提供されます。 LCS は、すべての配置オプションでの Dynamics 365 for Finance and Operations ソリューションの効率的な維持および運用に必要です。 クラウド サービスを稼働させてから 1 年近く経った今、LCS ベースの管理により、さらに予測可能な配置が可能になり、より優れたサポートとサービス エクスペリエンスをお客様に提供できるようになりました。 Finance and Operations のすべての配置オプションではその操作のために LCS が必要です。

オンプレミス配置シナリオでは、アプリケーション サーバーおよび SQL データベースは顧客またはパートナーのデータ センター内で実行されます。 顧客とパートナーは、業務プロセスの設計、オンプレミス ノードに展開するためのソフトウェア イメージの作成と展開、システム ヘルス ダッシュボードのオンプレミス ノードの監視、およびメンテナンスを含むマイクロソフト クラウドの LCS を通じてアプリケーション ライフサイクルを管理します。 Microsoft のイノベーションです。

詳細については、[ビジネスに適したクラウド オプション](https://community.dynamics.com/b/msftdynamicsblog/archive/2017/02/06/the-right-cloud-option-for-your-business) を参照してください。 このブログ記事は、「ローカル ビジネス データ」展開機能を参照しています。 これは、製品とドキュメントの「オンプレミス」と呼ばれる機能です。
