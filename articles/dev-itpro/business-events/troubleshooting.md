---
title: ビジネス イベントのトラブルシューティング
description: このトピックでは、ビジネス イベントのトラブルシューティングについて説明します。
author: Sunil-Garg
manager: AnnBe
ms.date: 02/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global for most topics. Set Country/Region name for localizations
ms.author: sunilg
ms.search.validFrom: Platform update 24
ms.dyn365.ops.version: 2019-02-28
ms.openlocfilehash: 6f6cdc482ba184549a4e160fb5431a03c53d4bf6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1505427"
---
# <a name="troubleshoot-business-events"></a>ビジネス イベントのトラブルシューティング

[!include[banner](../includes/banner.md)]

このトピックでは、ビジネス イベントに関する問題を解決するためのヒントをいくつか示します。

**エラー: エンドポイントを作成できません。例外メッセージ: キー コンテナー「https://[KeyVaultName].vault.azure.net/」からのシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。AADSTS700016: 識別子を持つアプリケーション「7e28cb03-dc28-43b5-b129-e13dcfb4b1fb」は、ディレクトリ 「ee3fe5c6-26af-42b1-9acf-5ee38e6ead6e」で見つかりませんでした。** 

これは、アプリケーションがテナントの管理者によってインストールされていないか、テナントのユーザーによって同意されていない場合に発生する可能性があります。 認証要求を間違ったテナントに送信した可能性があります。

**エラー: 追跡 ID: 19dc9946-45b6-4335-9676-6a133dbf4000 相関関係 ID: ecbc8a80-f9d0-41ec-9c8f-d334d050bd64 タイムスタンプ : 2019-02-06 23:27:06Z**

このエラーは、**Azure Active Directory アプリケーション ID** フィールドの値が正しくないことを意味します。 顧客の Azure ポータルの **Azure Active Directory アプリケーション ID** の値を **Azure Active Directory > アプリケーションの登録**で確認します。

**エラー: エンドポイントを作成できません。例外メッセージ: キー コンテナー「https://[KeyVaultName].vault.azure.net/」からシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。要求の送信中にエラーが発生しました。**

このエラーは、**Key Vault DNS Name** フィールドの値が正しくないことが原因です。 これを解決するには、顧客の Azure ポータルに移動して、キー コンテナーのオブジェクトを開きます。 **概要**セクションで、**Key Vault DNS 名**値を確認します。

**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 40103: 無効な認証トークンの署名、リソース: sb://[ServiceBusName]. servicebus.windows.net/[QueueName]。TrackingId:cd0eccaa-1717-4f97-b837-4cd7eda99af4_G13、SystemTracker:[ServiceBusName]. servicebus.windows.net:[QueueName]、Timestamp:2019-02-06T23:36:54**

顧客の Key Vault シークレットの値が予想が正しくない可能性があります。 **Key Vault シークレット**の値を確認し、エンドポイントのタイプが正しいことを確認します。

**エラー: エンドポイントを作成できません。例外メッセージ: key vault 「https://[KeyVaultName].vault.azure.net/」からシークレット「[KeyValueSecretName]」を取得中にエラーが発生しました。アクセスが拒否されました。**

**Azure Active Directory アプリケーション ID** に Key Vault での適切なアクセス許可がない可能性あります。 これを解決するには、Azure ポータルに移動して、**Key Vault** のオブジェクトを開きます。 **アクセス ポリシー**に移動し、キー、シークレット、および証明書の管理テンプレートを使用して、AAD アプリケーションを追加します。

**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 40400: エンドポイントが見つかりません。リソース: sb://[ServiceBusName].servicebus.windows.net/[QueueName].**

この問題は、キュー/トピック/ハブ名が正しくないことが原因です。 Azure ポータルのサービス バスにアクセスし、**名**フィールドを確認し、**トピック**または**キュー**名を確認します。 イベント ハブである場合、Azure の**イベント ハブ**オブジェクトに移動し、**ハブ**名を検証します。

**エラー: テスト イベントをエンドポイントに送信することができません。例外メッセージ: 要求の送信中にエラーが発生しました。**

**エンドポイント URL** フィールドのエンドポイントの指定された値が正しくない可能性があります。 Azure ポータルの**イベント グリッド**オブジェクトに移動し、**イベント グリッド**を開きます。 **概要**セクションで、この値が**トピック エンドポイント**になります。

**ビジネス イベントはカタログに表示されません**

ビジネス イベント カタログは、データベース全体の同期中に作成されます。その結果、以下に示すように、新しいビジネス イベントを確認するためにカタログを手動で更新する必要がある使用例がいくつかあります。 手動更新は **管理 > ビジネス イベント カタログの再構築** に移動することによってカタログから呼び出すことができます。

Visual Studio でビジネス イベントを実装中のときは、新しくコード化されたビジネス イベントがカタログに表示されない場合があります。

ワークフロー要素やステップなどの新しいワークフローが構成されていると、ビジネス イベント カタログに表示されない場合があります。

他の状況では、特定のビジネス イベントが表示されない場合、手動更新を行うと問題が解決する可能性があります。

**ビジネス イベントが発生した場合や、またはビジネス イベントが Service Bus トピックに表示されない場合、フロー アプリはトリガーされません**

通常、これはビジネス イベント バッチのプロセッサが実行されていないことを示します。 その結果、ビジネス イベントがエンドポイントに送信されるよう処理されません。 バッチ プロセッサは **システム パラメーター > ビジネス イベント - プレビュー** タブから起動できます。 ビジネス イベントを確実に継続して処理するには、ジョブを定期的にバッチで実行するようにスケジュールする必要があります。
