---
title: Finance and Operations コネクタ
description: このトピックでは、Finance and Operations Connector for Microsoft Flow およびロジック アプリの情報を提供します。
author: Sunil-Garg
manager: AnnBe
ms.date: 03/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: ''
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 36aff7651cb7947c6c735a752a6f5f07c0e84a23
ms.sourcegitcommit: e597ac963d541f521d253697bbf26ce1ca8630a3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/02/2019
ms.locfileid: "949234"
---
# <a name="finance-and-operations-connector"></a>Finance and Operations コネクタ

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Dynamics 365 for Finance and Operations Connector を使用して Microsoft Flow、PowerApps、データ インテグレーター、およびロジック アプリを Dynamics 365 for Finance and Operations のインスタンスと統合できます。 統合で使用可能なアクションを使って、ターゲット インスタンスでの作成、更新、または削除の操作に影響を与えることができます。 

## <a name="prerequisites"></a>必要条件
先に進む前に、コネクタについて理解するための前提条件として、次のトピックをお読みください。

- [コネクタ](https://docs.microsoft.com/en-us/connectors/) 
- [データ管理パッケージ REST API](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/data-management-api?toc=/fin-and-ops/toc.json)
- [データ プロトコル (OData) を開く](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/odata?toc=/fin-and-ops/toc.json) 
- [定期統合](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/data-entities/recurring-integrations?toc=/fin-and-ops/toc.json) 

## <a name="triggers"></a>トリガー
Finance and Operations のビジネス イベントは、*ビジネス イベントが発生した場合*にトリガーを使用して公開されます。 ビジネス イベントに関する詳細については、[Microsoft Flow](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-flow) のビジネス イベントおよび[ビジネス イベント](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/home-page)を参照してください。

## <a name="actions"></a>アクション

このセクションでは、Dynamics 365 for Finance and Operations Connector で使用できりうアクションについて説明します。

**レコードの取得**

このアクションを使用して、Finance and Operations のターゲット インスタンスから特定のデータ エンティティのレコードをフェッチできます。

*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。 予測値は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。

*エンティティ名前*は、レコードをフェッチする必要がある Finance and Operations 内のデータ エンティティを参照します。 ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。

*オブジェクト ID* は、フェッチする必要のあるレコードを一意に識別するために指定する必要のある主キーのフィールドを参照します。 次の構文の後にキーを指定する必要があります。

**レコードの作成**

このアクションを使用して、データ エンティティのデータ レコードを作成できます。

*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。

*エンティティ名前*は、レコードを作成する必要がある Finance and Operations 内のデータ エンティティを参照します。 ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。

表示されるフィールドの一覧は、選択したデータ エンティティに基づいて異なります。

**レコードの更新**

このアクションを使用して、データ エンティティの既存のデータ レコードを更新できます。 使用方法は、レコード アクションの作成と同じです。

**レコードの削除**

このアクションを使用して、データ エンティティの既存のデータ レコードを削除できます。 使用方法は、レコード アクションの取得と同じです。

**アクションの実行**

このアクションを使用して、ビジネス アクションを実行するメソッドをデータ エンティティ上で呼び出すことができます。

*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。

*アクション*は、Finance and Operations で実行する必要があるデータ エンティティ上のメソッドを参照します。 表示されるフィールドの一覧は、選択したメソッドに基づいて異なります。 これらのフィールドは、選択したメソッドのパラメーターを表します。

**エンティティの一覧を取得する**

このアクションを使用してエンティティの一覧を取得し、開発中のアプリで使用することができます。

*インスタンス* は、コネクタが接続する Dynamics 365 for Finance and Operations のターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Microsoft Flow、PowerApps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory に配置されている、すべての Finance and Operations 環境のリストです。
