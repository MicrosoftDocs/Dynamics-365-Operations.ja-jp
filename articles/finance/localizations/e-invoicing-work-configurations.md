---
title: 構成の使用
description: このトピックでは、グローバリゼーション機能ワークスペースから電子レポート (ER) 構成を操作する場合の主要なシナリオの概要を示します。
author: dkalyuzh
ms.date: 01/26/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4318399ee58ed54b29f8d360345b8930238ea9f2
ms.sourcegitcommit: ffdb6794746ffe5461f9dcf34ed8e64976d22d2d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/02/2022
ms.locfileid: "8371710"
---
# <a name="work-with-configurations"></a>構成を使う

[!include [banner](../includes/banner.md)]

電子レポート (ER) 構成は、電子請求機能のコンポーネントの主要なセットの 1 つです。 ER 構成には、ファイル構造の設定と、データを変換するための変換ルールのセットがあります。

- **Export ER 形式の構成** - この構成は、統合内部構造 (ERモデル) から電子ファイル形式にデータを変換します。
- **ER 形式の構成のインポート** - この構成は、統合内部構造 (ERモデル) から電子ファイル形式にデータを変換します。

定義済の形式で送信電子ファイルを生成する他に、外部 Web サービスから受信メッセージを応答として受信するために ER 構成が広く使用されています。 この機能を使用すると、構成可能なロジックを構築して、外部チャンネルとの通信の結果を取得し、それらの結果 (コード、メッセージ、ログ) をユーザーが読み取り可能な構造に変換して、その情報をクライアント アプリケーションに渡します。

電子請求機能で ER 構成 の使用を開始するには、それらを機能にリンクして、現在の機能バージョンの **構成** タブで使用可能にする必要があります。 リンクされた ER 構成を使用するには、**追加**、**削除**、**編集**、または **表示** を選択します。

ER 構成にリンクを追加するには、その構成が Regulatory Configuration Service (RCS) リポジトリに存在している必要があります。 RCS リポジトリで使用できる ER 構成を確認するには、次の手順に従います。

1. RCS アカウントにサインインします。
2. **構成** セクションの、**電子申告** ワークスペースで、**申告の構成** タイルを選択します。

新しい ER 構成の作成方法、またはグローバル リポジトリから既存の ER 構成をインポートする方法の詳細については、[電子レポート](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md) を参照してください。

リンクされた ER 構成を調整するには、現在の電子請求機能の **構成** タブで **編集** を選択します。 ER 構成のバージョンが自動的に作成されます。 現在のバージョンが有効な構成プロバイダーによって作成されたバージョンと異なる場合は、構成プロバイダーを使用する派生バージョンが作成されます。 現在のバージョンが有効な構成プロバイダーによって作成された場合は、新しいバージョンが作成されます。 どちらの場合も、作成するバージョンを変更し、必要なすべての更新を自動的に実行できます。
