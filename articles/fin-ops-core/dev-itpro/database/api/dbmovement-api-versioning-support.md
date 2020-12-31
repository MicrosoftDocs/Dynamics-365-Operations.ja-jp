---
title: データベース移動 API - バージョン管理とサポート
description: このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) のバージョン管理と重大な変更ポリシーの概要について説明します。
author: laneswenka
manager: AnnBe
ms.date: 02/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: laswenka
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 897f7dccfe6b2be984e277862cda7a61547b6dbc
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681116"
---
# <a name="versioning-and-support"></a>バージョン管理とサポート

[!include [banner](../../includes/banner.md)]

このトピックでは、データベース移動アプリケーション プログラミング インターフェイス (API) のバージョン管理と重大な変更ポリシーの概要について説明します。

## <a name="support-and-deprecation-information"></a>サポートおよび廃止に関する情報

REST API の新しいバージョンがリリースされると、それ以前のバージョンは破棄されます。 Microsoft は、API エンドポイントを廃止する少なくとも 6 か月前に廃止されたバージョンを宣言します。

API のバージョン番号を増やす (たとえば v1 から v2 に) ことにより、Microsoft は最も低いバージョン (この例では v1) が直ちに廃止され、通知の 6 か月後にサポートされなくなります。 ただし、Microsoft はサービスの正常性およびセキュリティ問題に対するこのポリシーの例外を作成する可能性があります。

API が廃止済としてマークされている場合は、**VersionEOL** (バージョンのサポート終了) フィールドに日付値が入力されます。 したがって、このフィールドを事前に監視して、今後の変更を計画することができます。

### <a name="compatible-and-breaking-changes"></a>互換性のある重大な変更

Microsoft では、プライベート プレビュー グループにおける API 変更の詳細を指定します。 変更が本質的に中断されない場合、API のバージョン番号は変わりません。 変更が本質的に中断される場合、Microsoft は API のバージョン番号を大きくします。

重大な変更の例を次に示します。

* URL または基本要求/応答が変更されます。
* 宣言されたプロパティが削除または名前変更されたか、またはタイプが変更されています。
* API または API パラメーターは削除されるか、名前変更されます。
* 必要な要求パラメーターが追加されます。

中断されない変更の例を次に示します。

* nullable または既定値を持つプロパティが追加されます。
* 列挙にメンバーが追加されます。
* ページングが既存のコレクションに導入されます。
* エラーコードが変更されます。
* 要求または応答のプロパティの順序が変更されます。

### <a name="example-of-versioneol-in-a-response-contract"></a>応答契約での VersionEOL の例

次の例は、JavaScript Object Notation (JSON) 形式の応答契約を示します。 すべての応答契約には、**VersionEOL** プロパティがあり、Microsoft .NET フレームワークから DateMax() の既定値があります。 アプリケーションは、Microsoft からの応答でこのフィールドの値を監視して、Microsoft が特定のエンドポイントまたは API バージョン全体を廃止した場合にすぐに警告を受け取ることができます。

```json
{
    "IsSuccess": true,
    "OperationActivityId": "55eb4327-9346-4c7b-82bd-fe8ef15112c6",
    "ErrorMessage": null,
    "VersionEOL": "9999-12-31T23:59:59.9999999"
}
```
