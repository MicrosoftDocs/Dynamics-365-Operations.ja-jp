---
title: 電子請求の設定
description: この記事では、電子請求を設定および構成するプロセスの概要を説明します。
author: gionoder
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: de94843c1e98a8788375bd41def587a64baea07d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272182"
---
# <a name="electronic-invoicing-setup"></a>電子請求の設定

[!include [banner](../includes/banner.md)]

この記事では、電子請求を設定および構成するプロセスの概要を説明します。 ここで指定した順序で設定手順を完了する必要があります。 ステップが必須であるにもかかわらずスキップした場合、機能が正常に機能しなくなり、後続のステップまたは機能の使用時に複数のエラーが発生します。 

始める前に、すべての主要コンポーネントが正しく設定されていること、Regulatory Configuration Service (RCS) にサインアップして RCS のインスタンスがあること、電子請求アドインが Microsoft Dynamics 365 Finance または Dynamics 365 Supply Chain Management 環境に対してインストールされていることを確認してください。 詳細については、[サインアップして電子請求をインストールする](e-invoicing-install-add-in-microservices-lcs.md) を参照してください。

次に、電子請求の処理に必要な Azure リソースを設定します。 詳細については、[電子請求のための Azure リソースの設定](e-invoicing-set-up-azure-resources.md) を参照してください。

主要コンポーネントの構成後は、RCS を使用して電子請求の主要論理コンポーネントを設定します。 まず、管理するサービス環境の数を定義します。 この方法で、論理データおよび構成のパーティション分割を定義して、開発環境またはテスト環境と運用環境の間に境界を確保します。 開発プロセスを柔軟に設定するには、複数の個別の開発環境とテスト環境が必要な場合があります。 サービス環境の定義に加えて、Finance または Supply Chain Management などのビジネス アプリケーションへのリンクを RCS から直接設定して、電子請求による適切な操作に必要なパラメーターを設定します。 環境の詳細については、[サービス環境](e-invoicing-service-environments.md) を参照してください。

すべてを設定した後に、電子ドキュメントを処理してデータ変換したり、グローバル リポジトリからドキュメントをインポートするさまざまなシナリオを定義する独自のグローバリゼーション機能を作成できます。 グローバリゼーション機能の使用方法の詳細については、[グローバリゼーション機能の使用](e-invoicing-working-globalization-features.md) を参照してください。

受信電子ドキュメントを処理するために、メールまたは SharePoint との統合が必要なシナリオがある場合、これらのチャネルの設定および使用方法の詳細については、[受信した電子ドキュメントの処理](e-invoicing-process-incoming-electronic-documents.md) を参照してください。
