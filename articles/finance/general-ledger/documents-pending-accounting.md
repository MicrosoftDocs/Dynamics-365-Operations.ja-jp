---
title: 会計を保留するドキュメント
description: この記事では、会計を保留するドキュメントのページに記載されている機能を使用する方法を説明します。
author: ryanCCarlson2
ms.date: 09/02/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: f37d46659b2fc5bf9933719811a7b90cc4e80f52
ms.sourcegitcommit: 6bd8822f7aa781d596b70956bead834117cf302c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709252"
---
# <a name="documents-pending-accounting"></a>会計を保留するドキュメント

[!include [banner](../includes/banner.md)]

この記事では、**会計を保留するドキュメント** のページに記載されている機能を使用する方法を説明します。

Microsoft Dynamics 365 Finance 10.0.30 では、**パフォーマンスが改善された元伝票の会計フレームワーク** の機能が利用可能です。 この機能により、元伝票の転記処理が改善されます。自由書式の請求書の転記処理から始まり、ドキュメントの転記なども可能になります。

この機能を有効にすると、会計生成および一般会計に転送される会計の全詳細を作成する *仕訳* 処理とは別に補助元帳ドキュメントの転記が行われます。 たとえば、自由形式の請求書転記プロセスでは、**売掛金勘定** モジュールの顧客請求書が、すべての会計が生成される前に記録されます。 このパフォーマンスが改善された機能により、会計の生成が遅れている場合に顧客請求書をよりすばやく記録できます。

**会計を保留するドキュメント** のページで次のボタンを使用できます。

- **会計の生成** – 仕訳中の勘定生成を保留しているドキュメントを送信します。
- **配分の表示** – 一覧で選択したドキュメントの会計配分を表示します。
- **エラー ログの表示** – 会計状態がエラーを示すドキュメントが存在する場合にエラー メッセージの詳細を表示します。 明細行の **エラー ログ** のリンクを選択すると、同じエラー メッセージの詳細を表示できます。

会計生成は **会計フレームワーク プロセッサ** という名称のプロセス自動化バックグラウンド プロセスで行われます。 すべてのプロセス自動化の構成および設定の詳細については、[プロセスの自動化](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md)を参照してください。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
