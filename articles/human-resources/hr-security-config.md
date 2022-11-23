---
title: 仮想テーブル ベースの統合に関するセキュリティ構成の概念
description: この記事では、Microsoft Dynamics 365 Human Resources と他のシステムの統合を構築するアーキテクチャについて説明します。
author: twheeloc
ms.date: 11/19/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 219ceb0adae0cee5f74a39140ab74af9fdac1eb6
ms.sourcegitcommit: ea79bf014bbf495ac8e28db29502c8bd85a75f32
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/11/2022
ms.locfileid: "9759655"
---
# <a name="security-configuration-concepts-for-virtual-table-based-integrations"></a>仮想テーブル ベースの統合に関するセキュリティ構成の概念

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

この記事では、[Microsoft Dataverse 仮想テーブル (エンティティ )](/dev-itpro/power-platform/virtual-entities-overview) を使用して Dynamics 365 Human Resources とサードパーティ製システムとの統合を構築するためのアーキテクチャについて説明します。 この記事では、セキュリティ構成と、機能的で安全なシステムを構築するためにシステム境界間で必要な認証および承認の側面に焦点を当てています。

## <a name="prerequisite-reference-articles"></a>前提となる参照記事

以下の記事では、この記事の概念に関する詳細情報を提供します:

- [仮想エンティティの概要](/dev-itpro/power-platform/virtual-entities-overview)
- [仮想テーブル (エンティティ) の使用を開始する](/developer/data-platform/virtual-entities/get-started-ve)
- [マルチ テナント サーバー間認証を使用する (Microsoft Dataverse)](/developer/data-platform/use-multi-tenant-server-server-authentication)
- [Microsoft Dataverse (Dataverse) で OAuth 認証を使用する](/developer/data-platform/authenticate-oauth)
- [Microsoft ID プラットフォームでの OAuth 2.0 クライアント資格情報フロー](/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)
- [認証と承認](/dev-itpro/power-platform/authentication-and-authorization)

## <a name="architecture"></a>アーキテクチャ 

次のアーキテクチャ図は、仮想テーブル (エンティティ) を使用する統合に関する主要な概念を示しています。

![仮想テーブル ベースの統合。](./media/Hosts.jpg)

上記の図のいくつかの要素について説明します:

- **Microsoft** – Microsoft は、顧客に代わりさまざまな Dynamics 365 製品をホストおよび運用しています。

    - **Azure Active Directory (Azure AD) テナント C** – Microsoft が所有する Azure AD テナント。 Dynamics 365 アプリケーションが登録されているテナントです。

- **統合パートナー**

    - **統合システム** – Dynamics 365 に統合されるシステム。 給与システムや、Dynamics 365 に保存されているデータに依存するシステムの場合もあります。
    - **アダプター** – Dynamics 365 と統合システムの両方とやり取りする役割を担うソフトウェアまたはサービス。

        > [!NOTE]
        > アダプターが複数の Dynamics 365 の顧客によって使用されることを想定している場合、Azure AD にマルチテナント アプリケーションとして登録されることが期待されます。

    - **Azure AD テナント A** – 統合パートナーが所有する Azure AD テナント。 アダプターのアプリケーション ID が登録されているテナントです。

- **相互顧客** – Dynamics 365 Human Resources と統合パートナーのソリューションを実装する顧客。

    - **Dynamics 365 Finance または Human Resources** – 統合システムに必要な顧客データを含む Dynamics 365 Finance または Human Resources の顧客固有のインスタンス。
    - **Dataverse** – Finance または Human Resources のいずれかに接続されている顧客固有の Dataverse 環境。 Dataverse は、Dynamics 365 データとの対話用の Web API を提供します。
    - **Azure AD テナント B** – 顧客の Azure AD テナント。 ID プロバイダー (承認サーバー) として機能し、呼び出し元が顧客の Dataverse インスタンスを呼び出すことを承認するトークンを発行します。

## <a name="basic-request-flow"></a>基本的な要求フロー

このセクションでは、統合に関連する一般的な要求の基本フローについて説明します。 この記事の前述のアーキテクチャ図を参照しています。

一般的な要求では、アダプターが Dynamics 365 にデータを照会し、そのデータを統合システムに保存および同期する必要があります。

1. アダプターは、Dataverse Web API を呼び出して関連データを照会します。

    > [!NOTE]
    > 認証が前提条件であり、トークン取得はプロセスの主要な部分です。 認証については、[システム境界における認証と承認](#authentication-and-authorization-at-system-boundaries) セクションで説明します。

    この呼び出しは、仮想テーブルを通じて公開されるアプリケーション データを照会するために Dataverse Web API に対して行われます。 (図の "2. 初期同期" と "3. 差分同期" を参照してください。)

2. Dataverse は、仮想エンティティ プラグイン (図では "仮想テーブル プロキシ") により仮想テーブルをクエリすることで要求を処理します。 Dataverse 要求は、Finance または Human Resources のデータベースに物理的に格納されたデータを照会するために、Finance または Human Resources の仮想エンティティ サービスに転送されます。
3. Finance または Human Resources の仮想エンティティ サービスは、仮想エンティティに対する要求を、Dataverse 仮想エンティティをバックアップする Finance または Human Resources エンティティに対するクエリに変換します。 データはデータベースから取得され、Dataverse エンティティ表現に変換され、呼び出し元に返されます。
4. アダプターは必要なマッピングとデータ変換を完了し、統合システムを呼び出して、統合システム データベースにデータを保持します。 (図の "4. "データの保存" を参照してください。)

## <a name="authentication-and-authorization-at-system-boundaries"></a>システム境界での認証と承認

*認証* は、ユーザーまたはアプリケーションの ID が証明されていることを検証し、ユーザーまたはアプリケーションが本人であることを確認します。 *認証* は、ユーザーまたはアプリケーションに、特定のアプリケーション レベルのアクセス許可を付与します。 詳細については、[認証と承認](/azure/active-directory/develop/authentication-vs-authorization) を参照してください。

この記事で前述したアーキテクチャ図では、システム間呼び出しのほとんどにアダプターが関係しています。 アダプターは、次の呼び出しを行うために自身を認証する必要があります:

- Dataverse への呼び出し
- 統合システムへの呼び出し

図のシステム境界を確認します。 システム間のすべての Web 要求は認証される必要があり、データが呼び出し元に返される前にアプリケーション レベルの認証チェックを渡す必要があります。 Finance または Human Resources によってサポートされる Dynamics 365 仮想テーブルに対する要求については、認証および承認チェックは、次のシステム境界で適用されます:

- アダプターと Dataverse Web API (OData) エンドポイント間の呼び出し
- Dataverse 仮想エンティティ プラグインと Finance または Human Resources 仮想エンティティ サービスの間の呼び出し

どちらの場合も、認証チェックが最初に行われます。 その後、アプリケーション レベルの認証チェックが行われ、認証されたユーザーまたはアプリケーションに、要求されたデータを取得するための適切なアプリケーション レベルの権限があることを確認します。

Dataverse を呼び出す認証は、Dataverse への Web 要求に HTTP ヘッダーとして含める必要があるベアラー トークンを通じて処理されます。 アダプターは、テナント B の Azure AD インスタンスからトークンを取得する必要があります。 (図の "1. "トークンの取得" を参照してください。) Azure AD は認証フローで ID プロバイダーとして機能します。

アダプターは、アプリケーションID (Azure AD テナント A に登録されている非シークレット) と、アダプター アプリケーションだけが持つアプリケーション シークレットまたは証明書を提供することで認証を行います。

ユーザーまたはアプリケーションが認証され、Dataverse を呼び出すと、Dataverse レベルの認証チェックは各要求に対して行われます。 これらのチェックにより、呼び出し元 (図で "\<guid A\>" と指定されているアダプター アプリケーションの ID) に適切なアプリケーション アクセス許可があることが確認されます。 アプリケーション レベルの認証は、アダプターのアプリケーション ID を表すアプリケーション ユーザーにより、Dataverse で管理されます。 アプリケーション レベルのアクセス許可は、特定の Dataverse 定義されたアプリケーション ロールへのアクセスを許可することで管理されます。 これらのロールは、アプリケーションに詳細な権限を提供します。

より詳細なガイダンスについては、[マルチ テナントのサーバー間認証を使用する](/power-apps/developer/data-platform/use-multi-tenant-server-server-authentication) を参照してください。

Dataverse レベルのアプリケーションのアクセス許可チェックに合格すると、仮想エンティティ プラグインが Finance または Human Resources 環境の仮想エンティティ サービス エンドポイントに呼び出します。 この呼び出しにはサーバー間 (S2S) 認証が使用されます。 財務と運用の仮想データ ソース構成レコードで構成された ID とシークレットを使用します。

![サンドボックス環境の財務と運用の仮想データ ソース構成レコード。](./media/sandbox.jpg)

詳細については、[Dataverse 仮想エンティティの構成](/dev-itpro/power-platform/admin-reference) を参照してください。

Dataverse 仮想エンティティ プラグインから Finance または Human Resources への呼び出しには、アダプターから Dataverse への元の呼び出しのアダプター ID (アーキテクチャ図で "\<guid A\>" と指定されている ID) が含まれます。 仮想エンティティ データ ソースが正しく構成され、S2S 認証チェックに合格した場合、Finance または Human Resources の仮想エンティティ サービスは、元の呼び出し (アダプター、\<guid A\>) のコンテキストでクエリを実行します。 Finance または Human Resources レベルでアプリケーションのアクセス許可チェック (認証) が行われ、クエリによって要求されるデータ エンティティにアクセスするために必要な権限がアダプターにあることが確認されます。

Finance および Human Resources のセキュリティは、次の方法で管理されます:

1. アダプター ID (\<guid A\>) を特定の Finance または Human Resources のユーザーにマッピングすることによって。 このマッピングは、**Azure Active Directory アプリケーション** ページで行われます。 詳細については、[外部アプリケーションを登録する](/dev-itpro/data-entities/services-home-page.md#register-your-external-application) をご覧ください。
2. Finance または Human Resources のユーザーに適切なアプリケーション レベルのロール、職務、権限を与えることによって。 詳細については、[ロールベース セキュリティ](/dev-itpro/sysadmin/role-based-security)を参照してください。

アダプター アプリケーション (\<guid A\>) に、要求されたデータへのアクセスに必要な権限が与えられている場合、次のイベントが発生します:

1. クエリが実行されます。
2. データは Dataverse エンティティ ページに戻って変換されます。
3. データはアダプターに返されます。

> [!IMPORTANT]
> 開発時は、管理者ロールを持つ Finance または Human Resources のユーザーを使用してアダプターを実行できます。 ただし、運用環境では、アダプターを管理者権限で実行しないでください。

## <a name="key-takeaways"></a>重要なポイント

仮想テーブルまたはエンティティ アーキテクチャの重要な意味を次に示します:

- Human Resources によってサポートされる仮想テーブルのセキュリティ構成は、Human Resources で管理されます。
- 顧客 (この記事で前述したアーキテクチャ図の "相互顧客") は、統合アダプタ ID (図では "\<guid A\>" と指定) に与えられる権限を完全に制御できます。
- Human Resources 環境の適切なセキュリティ構成は、顧客の責任となります。 アダプターを作成する統合パートナーは、アダプターに必要な権限に関するガイダンスを提供する必要があります。
