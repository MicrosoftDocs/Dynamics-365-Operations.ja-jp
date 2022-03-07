---
title: 組織管理ホーム ページ
description: このトピックでは、組織で役立つリソースを示します。
author: sericks007
ms.date: 08/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "20421"
- intro-internal
ms.assetid: 7aa24a03-d172-47e9-81f8-ebd39e80bc60
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04d188b0bf7d7fc7064467e1e05199d0eb90b4d0276a3c0c01ad8f9be78e76e8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759899"
---
# <a name="organization-administration-home-page"></a>組織管理ホーム ページ

[!include [banner](../includes/banner.md)]

このトピックのポイントは、組織と業務を円滑かつ効率的に操作するよう、パワー ユーザーと管理者がシステムをコンフィギュレーションするのに役立ちます。

ここに表示されるコンテンツの多くは、**組織管理** モジュールでの機能に適用されます。 ただし、レコード テンプレートを作成および使用するなどの、組織をより効率的に実行するのに役立つ任意のモジュールで実行できる、いくつかのタスクがあります。

## <a name="number-sequences"></a>番号順序

番号順序は、ID が必要なマスター データ レコードおよびトランザクション レコードに対して読みやすい固有の ID を生成するために使用されます。 ID が必要なマスタ データ レコードまたはトランザクション レコードは、*参照* と呼ばれます。 参照先に新しいレコードを作成するには、事前に番号順序を設定して参照先に関連付ける必要があります。

- [番号順序の概要](number-sequence-overview.md)
- [ウィザードを使用した番号順序の設定](tasks/set-up-number-sequences-wizard.md) (タスク ガイド)
- [番号順序を個別に設定する](tasks/set-up-number-sequences-individual-basis.md) (タスク ガイド)

## <a name="organizations"></a>組織

組織とは、業務プロセスを実行や目標の達成を協力して行う人々の集まりです。 組織階層とは、業務を構成する組織の関係を表すものです。

組織と組織階層を設定する前に、組織をシミュレーションする方法を確認してください。 組織モデルは、実装と業務プロセスに重要な影響を与えます。

- [組織と組織階層の概要](organizations-organizational-hierarchies.md)
- [組織階層の計画](plan-organizational-hierarchy.md)
- [組織階層の作成](tasks/create-organization-hierarchy.md) (タスク ガイド)
- [法人の作成](tasks/create-legal-entity.md) (タスク ガイド)
- [作業単位の作成](tasks/create-operating-unit.md) (タスク ガイド)

## <a name="address-books"></a>アドレス帳

グローバル アドレス帳は、連携する会社のすべての内部および外部担当者と組織が格納されている必要があるマスター データに対する中央リポジトリです。 関係者レコードに関連付けられているデータには、関係者の名前、住所、および連絡先情報が含まれます。

グローバル アドレス帳を作成すると、必要に応じて組織の各会社別または事業品目別のアドレス帳など追加のアドレス帳を作成できます。

- [グローバル アドレス帳の概要](overview-global-address-book.md)
- [グローバル アドレス帳およびその他のアドレス帳の計画](plan-configuration-global-address-book-additional-address-books.md)
- [グローバル アドレス帳の構成](tasks/configure-global-address-book.md)
- [アドレス帳に関するよく寄せられる質問](qa-address-books.md)

## <a name="workflow"></a>ワークフロー

ワークフローは、個々のワークフローまたは業務プロセスを作成できるシステムです。 ワークフローを作成する場合、タスクを完了し、決定を下し、ドキュメントを承認するユーザーを示すことによって、システムにおけるドキュメントの流れ (移動) を指定します。

- [ワークフロー システムの概要](overview-workflow-system.md)
- [ワークフロー要素](workflow-elements.md)
- [ワークフローの承認プロセスでのアクション](workflow-actions.md)
- [ワークフローの作成の概要](create-workflow.md)

## <a name="electronic-signatures"></a>電子署名

電子署名は、コンピューティング プロセスの開始者または承認者を確認するための ID です。 一部の業界では、電子署名は手書きの署名と同じだけの法的拘束力があります。 製薬、飲食料品、航空防衛などの規制対象業界では、規制準拠要件として電子署名が義務付けられています。

重要なビジネス プロセスに電子署名を使用できます。 組み込みの電子署名機能を持つプロセスもあります。 任意のデータベース テーブルおよびフィールド用にカスタム署名要求を作成することもできます。

- [電子署名の概要](electronic-signature-overview.md)
- [電子署名の設定](tasks/set-up-electronic-signatures.md) (タスク ガイド)

## <a name="case-management"></a>ケース管理

ケースの計画、追跡、および分析を行うことで、同様の問題に使用できる効率的な解決策を作成できます。 たとえば、顧客サービス担当者または一般人事担当者がケースを作成することで、より効率的なケースを対処したり解決するのに役立つ情報をナレッジ記事で検索できるようになります。

- [ケース管理の概要](cases.md)
- [ケース カテゴリ セキュリティの計画、ケース プロセス、およびケース カテゴリ](plan-case-management.md)

## <a name="record-templates"></a>レコード テンプレート

レコード テンプレートでは、レコードをもっと迅速に作成することができます。 よく使用されるフィールド値を新しいレコードごとに明示的に入力する必要をなくなるようにする、レコード テンプレートを作成できます。

- [レコード テンプレートの概要](record-templates.md)
- [データ入力を容易にするレコード テンプレートの作成](../../dev-itpro/data-entities/tasks/create-record-template-facilitate-data-entry.md) (タスク ガイド)
- [レコード テンプレートを使用した新しいレコードの作成](../../dev-itpro/data-entities/tasks/use-record-template-new-record.md) (タスク ガイド)

## <a name="general-organization-administration"></a>一般的な組織管理

- [バナーまたはロゴの変更](../get-started/tasks/change-banner-or-logo.md) (タスク ガイド)
- [ドキュメント管理のコンフィギュレーション](configure-document-management.md)
- [電子メールのコンフィギュレーションと送信](configure-email.md)
- [日時データとタイム ゾーン](date-time-zones.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]