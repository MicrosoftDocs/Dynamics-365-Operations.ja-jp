---
title: アプリケーション コネクタ
description: この記事では、Microsoft Power Automate および Logic Appsのアプリケーション コネクタに関する情報を提供します。
author: peakerbl
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: d20c935215104f09a0e3539848070a7a7c616980
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/01/2022
ms.locfileid: "9108313"
---
# <a name="application-connector"></a>アプリケーション コネクタ

[!include[banner](../includes/banner.md)]

アプリケーション コネクタを使用して Microsoft Power Automate、Power Apps、データ インテグレーター、および Logic Apps を財務と運用に統合できます。 外部アプリケーションは、有効なトリガーとアクションを使用することで、それらと統合することできます。

> [!IMPORTANT]
> アプリケーション の コネクタ は Dynamics 365 Finance + Operations (on-premises) インスタンスとの統合には使用できません。

## <a name="prerequisites"></a>必要条件
先に進む前に、コネクタについて理解するための前提条件として、次のトピックをお読みください。

- [コネクタ](/connectors/) 
- [データ管理パッケージ REST API](data-management-api.md)
- [データ プロトコル (OData) を開く](odata.md) 
- [定期統合](recurring-integrations.md) 

## <a name="triggers"></a>トリガー
ビジネス イベントは、*ビジネス イベントが発生した場合* にトリガーを使用して公開されます。 ビジネス イベントに関する詳細については、[Microsoft Power Automate](../business-events/business-events-flow.md) のビジネス イベントおよび[ビジネス イベント](../business-events/home-page.md)を参照してください。

## <a name="actions"></a>アクション

このセクションでは、コネクタで使用できるアクションについて説明します。

**レコードの取得**

このアクションは、ターゲット インスタンスから特定のデータ エンティティのレコードをフェッチするために使用できます。

*インスタンス* は、コネクタが接続するアプリケーションのターゲット インスタンスの URL を参照します。 予測値は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。

*エンティティ名* は、レコードをフェッチする必要があるデータ エンティティを参照します。 ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。

*オブジェクト ID* は、フェッチする必要のあるレコードを一意に識別するために指定する必要のある主キーのフィールドを参照します。 エンティティで定義されている順序で、コンマ区切りの値のリストとして値を指定する必要があります。

**レコードの作成**

このアクションを使用して、データ エンティティのデータ レコードを作成できます。

*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。

*エンティティ名* は、レコードを作成する必要があるデータ エンティティを参照します。 ドロップダウン メニューは、ターゲット環境のデータ エンティティの一覧を表示します。

表示されるフィールドの一覧は、選択したデータ エンティティに基づいて異なります。

**レコードの更新**

このアクションを使用して、データ エンティティの既存のデータ レコードを更新できます。 使用方法は、レコード アクションの作成と同じです。

**レコードの削除**

このアクションを使用して、データ エンティティの既存のデータ レコードを削除できます。 使用方法は、レコード アクションの取得と同じです。

**アクションの実行**

このアクションを使用して、ビジネス アクションを実行するメソッドをデータ エンティティ上で呼び出すことができます。

*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。

*アクション* は、実行する必要があるデータ エンティティ上のメソッドを参照します。 表示されるフィールドの一覧は、選択したメソッドに基づいて異なります。 これらのフィールドは、選択したメソッドのパラメーターを表します。

**エンティティの一覧を取得する**

このアクションを使用してエンティティの一覧を取得し、開発中のアプリで使用することができます。

*インスタンス* は、コネクタが接続するターゲット インスタンスの URL を参照します。 この値の構文は、「https://」' 接頭語のない URL を入力するか、またはドロップダウン メニューからいずれかを選択します。 これは、Power Automate、Power Apps、ロジック アプリなどの特定のクライアントへのサインインに使用されたユーザー アカウントの Azure Active Directory テナントに配置されている、すべての環境のリストです。

**テーブルに存在するリスト項目**

このアクションは、エンティティからレコードの一覧を取得するために使用できます。 このアクションは、会社間でのデータの読み取りをサポートします。



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

